---
title: 在 iOS 和 Android 上實作 Microsoft Dynamics 365 Project Timesheet 行動應用程式的自訂欄位
description: 本主題提供使用擴充功能實作自訂欄位的一般模式。
author: Yowelle
manager: AnnBe
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 10.0.3
ms.search.validFrom: 2019-05-29
ms.openlocfilehash: 1ea1ca002a8f68f86808831b398e452244471322
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073050"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a>在 iOS 和 Android 上實作 Microsoft Dynamics 365 Project Timesheet 行動應用程式的自訂欄位

[!include [banner](../includes/banner.md)]

本主題提供使用擴充功能實作自訂欄位的一般模式。 下列主題內容涵蓋：

- 自訂欄位架構支援的各種資料類型
- 如何在時程表項目上顯示唯讀或可編輯欄位，以及將使用者提供的值儲存回資料庫
- 如何在時程表標題上顯示唯讀欄位
- 如何整合其他自訂，以在欄位中輸入預設值並執行其他驗證

## <a name="audience"></a>對象

本主題適合要將自訂欄位整合至 Apple iOS 和 Google Android 適用版 Microsoft Dynamics 365 Project Timesheet 行動應用程式中的開發人員。 假設讀者熟悉 X++ 開發工作和專案時程表功能。

## <a name="data-contract--tstimesheetcustomfield-x-class"></a>資料合約 – TSTimesheetCustomField X++ 類別

**TSTimesheetCustomField** 類別是 X++ 資料合約類別，表示有關時程表功能自訂欄位的資訊。 TSTimesheetDetails 資料合約和 TSTimesheetEntry 資料合約，都會傳遞自訂欄位物件清單，以顯示行動應用程式中的自訂欄位。

- **TSTimesheetDetails** - 時程表標題合約。
- **TSTimesheetEntry** - 時程表交易合約。 這些有相同專案資訊及 **timesheetLineRecId** 值之物件的群組構成一行內容。

### <a name="fieldbasetype-types"></a>fieldBaseType (類型)

**TsTimesheetCustom** 物件上的 **FieldBaseType** 屬性決定出現應用程式中欄位的類型。 下列支援的 **類型** 值。

| 類型值 | 類型​​              | 附註​​ |
|-------------|-------------------|-------|
| 12           | 字串 (和列舉) | 欄位會顯示為文字欄位。 |
| 7           | Integer           | 值會顯示為沒有小數位數的數字。 |
| 2           | 實數              | 值會顯示為含有小數位數的數字。<p>若要在應用程式中將實數值顯示為貨幣，請使用 **fieldExtenededType** 屬性。 您可以使用 **numberOfDecimals** 屬性來設定顯示的小數位數。</p> |
| 3           | 日期              | 日期格式是由使用者的 **日期、時間及數字格式** 設定所決定，此設定是在 **使用者選項** 的 **語言和國家/地區喜好設定** 底下指定。 |
| 4           | Boolean           | |
| 15          | GUID              | |
| 16          | Int64             | |

- 如果 **TSTimesheetCustomField** 物件上未提供 **stringOptions** 屬性，則會為使用者提供任意格式的文字欄位。

    **stringLength** 屬性可用來設定使用者所能輸入的最大字串長度。

- 如果 **TSTimesheetCustomField** 物件已提供 **stringOptions** 屬性，則這些清單元素是使用者只能使用選項按鈕 (圓形按鈕) 選擇的值。

    在這種情況下，字串欄位可以做為供使用者輸入之用的列舉值。 若要將值做為列舉儲存至資料庫，請先手動將字串值對應回列舉值，再使用命令鏈結儲存至資料庫 (如需範例請參閱本主題稍後的「使用 TSTimesheetEntryService 類別中的命令鏈結，將時程表項目從應用程式儲存回資料庫」一節)。

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a>fieldExtendedType (TSCustomFieldExtendedType)

可以使用此屬性將實數值格式化為貨幣。 此方法只有在 **fieldBaseType** 值為 **實數** 時才適用。

- **TSCustomFieldExtendedType:None** – 未套用任何格式設定。
- **TSCustomFieldExtendedType::Currency** – 將值格式化為貨幣。

    當貨幣格式為使用中狀態時，可以使用 **stringValue** 欄位傳遞應顯示在應用程式中的貨幣代碼。 此值是唯讀值。

    **realValue** 欄位包含應儲存至資料庫的金額。

### <a name="fieldsection-tscustomfieldsection"></a>fieldSection (TSCustomFieldSection)

您可以使用此屬性指定自訂欄位應出現在應用程式中的位置。

- **TSCustomFieldSection::Header** – 此欄位會出現在應用程式的 **檢視更多詳細資料** 區段中。 這些欄位一律是唯讀。
- **TSCustomFieldSection::Line** – 此欄位會在時程表項目的所有內建行欄位之後出現。 這些欄位可能是可編輯或唯讀的欄位。

### <a name="fieldname-fieldnameshort"></a>fieldName (FieldNameShort)

將應用程式提供的值儲存回資料庫時，此屬性會識別欄位。

### <a name="tablename-tablenameshort"></a>tableName (TableNameShort)

將應用程式提供的值儲存回資料庫時，此屬性會識別欄位。

### <a name="iseditable-noyes"></a>isEditable (NoYes)

將此屬性設定為 **是** ，以指定時程表項目區段中的欄位應可供使用者編輯。 將屬性設定為 **否** ，使欄位成為唯讀欄位。

### <a name="ismandatory-noyes"></a>isMandatory (NoYes)

將此屬性設定為 **是** ，以指定時程表項目區段中的欄位應為必要欄位。

### <a name="label-str"></a>標籤 (str)

此屬性指定在應用程式中欄位旁顯示的標籤。

### <a name="stringoptions-list-of-strings"></a>stringOptions (字串清單)

此屬性只有在 **fieldBaseType** 設定為 **字串** 時才適用。 如果 **stringOptions** 已設定，可透過選項按鈕 (圓形按鈕) 使用的字串值是由清單中的字串所指定。 如果未提供任何字串，則允許在字串欄位中輸入任意格式的文字 (如需範例，請參閱本主題稍後的「使用 TSTimesheetEntryService 類別中的命令鏈結，將時程表項目從應用程式儲存回資料庫」一節)。

### <a name="stringlength-int"></a>stringLength (int)

此屬性指定字串欄位的最大長度。 這只有在 **fieldBaseType** 設定為 **字串** 時才適用。

### <a name="numberofdecimals-int"></a>numberOfDecimals (int)

此屬性指定實數欄位顯示的小數位數。 這只有在 **fieldBaseType** 設定為 **實數** 時才適用。

### <a name="ordersequence-int"></a>orderSequence (int)

此屬性可在指定了多個自訂欄位時，控制自訂欄位顯示在應用程式中所依照的順序。 編號較小的欄位會先顯示。

### <a name="booleanvalue-boolean"></a>booleanValue (布林值)

對於 **布林值** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞布林值的欄位。

### <a name="guidvalue-guid"></a>guidValue (guid)

對於 **GUID** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞全域唯一識別碼 (GUID) 值的欄位。

### <a name="int64value-int64"></a>int64Value (int64)

對於 **Int64** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞 Int64 值的欄位。

### <a name="intvalue-int"></a>intValue (int)

對於 **Int** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞 Int 值的欄位。

### <a name="realvalue-real"></a>realValue (實數)

對於 **實數** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞實數值的欄位。

### <a name="stringvalue-str"></a>stringValue (str)

對於 **字串** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞字串值的欄位。 這也會用於格式設為貨幣的 **實數** 類型欄位。 在這些欄位中，此屬性會用來將貨幣代碼傳遞至應用程式。

### <a name="datevalue-date"></a>dateValue (日期)

對於 **日期** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞日期值的欄位。

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a>在時程表項目區段中顯示並儲存自訂欄位

以下是建立時程表項目的行動應用程式螢幕擷取畫面。 此畫面顯示 [時間項目] 區段 (稱為「測試字串」) 中的內建欄位和自訂欄位，其中已經設定「第二個選項」的列舉值。

![應用程式中的測試字串自訂欄位](media/timesheet-entry.jpg)



以下是使用者為 [測試字串] 自訂欄位選取其中一個可用列舉值的行動應用程式螢幕擷取畫面。  這兩個選項是顯示為選項按鈕的 [第一個選項] 和 [第二個選項]。 目前已選取第二個選項。

![[測試字串] 自訂欄位的選項按鈕 (圓形按鈕)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a>擴充 TSTimesheetLine 資料表，使其中含有自訂欄位

在一般案例中，時程表項目區段中自訂欄位的資料很可能會儲存至 TSTimesheetLine 資料表。 不過，如果資料可以根據提供的 TSTimesheetTrans 記錄來擷取，或者資料沒有特定記錄內容 (例如，如果欄位在專案參數中設定為唯讀)，則可以使用其他資料表。

請注意，自訂欄位不一定有任何支援資料庫記錄。 這些欄位可以根據 X++ 邏輯動態產生。 此方法在唯讀案例中很實用 (如需動態產生自訂欄位值的範例，請參閱「使用 TSTimesheetDetails 類別中的命令鏈結、buildCustomFieldListForHeader 方法來填入時程表詳細資料」一節)。

以下是應用程式物件樹狀結構的 Visual Studio 螢幕擷取畫面。 此畫面顯示 TSTimesheetLine 資料表的擴充功能，其中 TestLineString 欄位已新增為自訂欄位。

![行字串](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a>使用 TSTimesheetSettings 類別在 buildCustomFieldList 方法中的命令鏈結，以在時程表項目區段中顯示欄位

此程式碼會控制應用程式中欄位的顯示設定。 例如，會控制欄位類型、標籤、欄位是否必填，以及欄位顯示所在的區段。

下列範例在時間項目上顯示字串欄位。 此欄位有兩個選項： **第一個選項** 和 **第二個選項** ，可透過選項按鈕 (圓形按鈕) 來使用。 應用程式中的欄位會與新增至 TSTimesheetLine 資料表的 **TestLineString** 欄位相關聯。

請注意，使用 **TSTimesheetCustomField::newFromMetatdata()** 方法來簡化下列自訂欄位屬性的初始化： **fieldBaseType** 、 **tableName** 、 **fieldname** 、 **標籤** 、 **isEditable** 、 **isMandatory** 、 **stringLength** 和 **numberOfDecimals** 。 您也可以依自己喜好手動設定這些參數。

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('Second option');
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a>使用 TSTimesheetEntry 類別在 buildCustomFieldListForEntry 方法中的命令鏈結，以在時程表項目中輸入值

**BuildCustomFieldListForEntry** 方法可在行動應用程式中用來輸入已儲存時程表行上的值。 這會接受 TSTimesheetTrans 記錄做為參數。 該記錄中的欄位可以用來填入應用程式中的自訂欄位值。

```xpp
...
[ExtensionOf(classStr(TsTimesheetEntry))]
final class TsTimesheetEntry_Extension
{
    protected List buildCustomFieldListForEntry(TSTimesheetTrans _tsTimesheetTrans)
    {
        List customFieldList = next buildCustomFieldListForEntry(_tsTimesheetTrans);
        TSTimesheetLine tsTimesheetLine = _tsTimesheetTrans.timesheetLine();
        TSTimesheetCustomField tsTimesheetCustomField;
        tsTimesheetCustomField =
        TSTimesheetCustomField::newFromMetadata(tableNum(TsTimesheetLine),
        fieldNum(TSTimesheetLine, TestLineString));
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Line);
        tsTimesheetCustomField.parmOrderSequence(1);
        tsTimesheetCustomField.parmStringValue(tsTimesheetLine.TestLineString);
        List stringOptions = new List(Types::String);
        stringOptions.addEnd('First option');
        stringOptions.addEnd('second option;);
        tsTimesheetCustomField.parmStringOptions(stringOptions);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a>使用 TSTimesheetEntryService 類別中的命令鏈結，將應用程式中的時程表項目儲存回資料庫

若要以一般使用方式將自訂欄位儲存回資料庫，您必須擴充多個方法：

- **TimesheetLineNeedsUpdating** 方法會用來判斷行記錄是否已由應用程式中的使用者所變更，以及是否必須儲存至資料庫。 如果不需顧慮效能，則可以簡化此方法，使其永遠傳回 **是** 。
- 您可以擴充 **populateTimesheetLineFromEntryDuringCreate** 和 **populateTimesheetLineFromEntryDuringUpdate** 方法，讓這些方法從提供的 TSTimesheetEntry 資料合約記錄輸入 TSTimesheetLine 資料庫記錄中的值。 在後面的範例中，請注意資料庫欄位與輸入欄位之間的對應是如何透過 X++ 程式碼手動完成。
- 如果對應至 **TSTimesheetEntry** 物件的自訂欄位必須寫回至 TSTimesheetLineweek 資料庫資料表，您對，如果則為擴充 **populateTimesheetWeekFromEntry** 方法。

> [!NOTE]
> 下列範例會將使用者選取的 **firstOption** 或 **secondOption** 值做為原始字串值儲存至資料庫。 如果資料庫欄位是 **列舉** 類型的欄位，則可以將這些值手動對應至列舉值，然後儲存至資料庫表中的列舉欄位。

```xpp
...
[ExtensionOf(classStr(TSTimesheetEntryService))]
final class TSTimesheetEntryService_Extension
{
    protected boolean timesheetLineNeedsUpdating(TSTimesheetLine _tsTimesheetLine,
    TsTimesheetEntry _tsTimesheetEntry)
    {
        boolean ret = next timesheetLineNeedsUpdating(_tsTimesheetLine,
        _tsTimesheetEntry);
        if (!ret)
        {
            */ Loop through custom fields to see if value needs updating*/
            ListEnumerator enumerator =  _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    */ If Custom field value for TestLineString field has changed, We need to update the timesheet line.*/
                    if (_tsTimesheetLine.TestLineString != customField.parmStringValue())
                    {
                        ret = true;
                    }
                }
            }
        }
        return ret;
    }
    protected void populateTimesheetLineFromEntryDuringCreate(TSTimesheetLine
    _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
    {
        next populateTimesheetLineFromEntryDuringCreate(_tsTimesheetLine,
        _tsTimesheetEntry);
        this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
        _tsTimesheetEntry);
        }
        protected void populateTimesheetLineFromEntryDuringUpdate(TSTimesheetLine
        \_tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            next populateTimesheetLineFromEntryDuringUpdate(_tsTimesheetLine,
            _tsTimesheetEntry);
            this.populateTimesheetLineFromCustomFields(_tsTimesheetLine,
            _tsTimesheetEntry);
        }
        private void populateTimesheetLineFromCustomFields(TSTimesheetLine
        _tsTimesheetLine, TSTimesheetEntry _tsTimesheetEntry)
        {
            ListEnumerator enumerator =
            _tsTimesheetEntry.parmCustomFields().getEnumerator();
            while (enumerator.moveNext())
            {
                TSTimesheetCustomField customField = enumerator.current();
                if (customField.parmFieldName() == fieldId2Name(tableNum(TsTimesheetLine),
                fieldNum(TSTimesheetLine, TestLineString)))
                {
                    _tsTimesheetLine.TestLineString = customField.parmStringValue();
                }
            }
        }
    }
...
```

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a>在時程表標題區段中顯示自訂欄位

以下是使用者檢視時程表的行動應用程式螢幕擷取畫面。 已選取右上角的 [其他資訊] 按鈕來顯示 [檢視更多詳細資料] 選項。  

![[檢視更多詳細資料] 命令](media/show-more.png)

以下是顯示時程表 [其他] 區段的行動應用程式螢幕擷取畫面。 已將名為「此時程表的利用率 (自訂計算欄位)」的自訂欄位新增至時程表標題區段。 自訂欄位上已設定「0.667」的唯讀值。

![其他區段](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a>擴充 TSTimesheetTable 資料表，使其中含有自訂欄位

在一般案例中，很可能會從 TSTimesheetHeader 資料表提取標題區段中自訂欄位的資料。 不過，如果資料可以根據提供的 TSTimesheetTable 記錄來擷取，或者資料沒有特定記錄內容 (例如，如果欄位在專案參數中設定為唯讀)，則可以使用其他資料表。

請注意，自訂欄位不一定有任何支援資料庫記錄。 這些欄位可以根據 X++ 邏輯動態產生。 下面的範例會說明此方法。

標題區段的欄位在應用程式中永遠為唯讀。

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a>使用 TSTimesheetSettings 類別在 buildCustomFieldList 方法中的命令鏈結，以在標題區段中顯示欄位

此程式碼會控制應用程式中欄位的顯示設定。 例如，會控制欄位類型、標籤、欄位是否必填，以及欄位顯示所在的區段。

下列範例說明標題區段在應用程式中的計算值。

```xpp
...
[ExtensionOf(classStr(TsTimesheetSettings))]
final class TSTimesheetSettings_Extension
{
    protected List buildCustomFieldList()
    {
        List customFieldList = next buildCustomFieldList();
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a>使用 TSTimesheetDetails 類別在 buildCustomFieldListForHeader 方法中的命令鏈結，以填入時程表詳細資料

**buildCustomFieldListForHeader** 方法可在行動應用程式中用來填入時程表標題詳細資料。 這會接受 TSTimesheetTable 記錄做為參數。 該記錄中的欄位可以用來填入應用程式中的自訂欄位值。 下列範例不會從資料庫讀取任何值。 反而是使用 X++ 邏輯來產生接著在應用程式中顯示的計算值。


```xpp
...
[ExtensionOf(classStr(TSTimesheetDetails))]
final class TSTimesheetDetails_Extension
{
    protected List buildCustomFieldListForHeader(TSTimesheetTable
    _tsTimesheetTable)
    {
        List customFieldList = next buildCustomFieldListForHeader(_tsTimesheetTable);
        TSTimesheetCustomField tsTimesheetCustomField;

        */ Computed utilization rate*/
        tsTimesheetCustomField = new TSTimesheetCustomField();
        tsTimesheetCustomField.parmFieldBaseType(Types::Real);
        tsTimesheetCustomField.parmLabel("Utilization rate of this timesheet (computed
        custom field)");
        tsTimesheetCustomField.parmFieldSection(TSCustomFieldSection::Header);
        tsTimesheetCustomField.parmOrderSequence(2);
        tsTimesheetCustomField.parmNumberOfDecimals(3);
        real utilizationRate = 0;
        if (_tsTimesheetTable.totalHours() != 0)
        {
            utilizationRate = _tsTimesheetTable.totalHoursBillable() /
            _tsTimesheetTable.totalHours();
        }
        tsTimesheetCustomField.parmRealValue(utilizationRate);
        customFieldList.addEnd(tsTimesheetCustomField);
        return customFieldList;
    }
}
...
```

## <a name="other-configurabilityextensibility-opportunities"></a>其他可設定性/擴充性商機

### <a name="adding-additional-validation-for-the-app"></a>為應用程式新增其他驗證

時程表功能在資料庫層級的現有邏輯仍可依預期正常運作。 若要中斷完成儲存或提交作業並顯示特定錯誤訊息，您可以透過擴充命令鏈結，將 **擲回錯誤 (「傳送訊息給使用者」)** 新增至程式碼。 以下是三個實用擴充方法的範例：

- 如果 TSTimesheetLine 資料表上的 **validateWrite 在** 時程表行的儲存作業期間傳回 **否** ，則行動應用程式中會顯示錯誤訊息。
- 如果 TSTimesheetTable 資料表上的 **validateSubmit** 在應用程式的時程表行提交期間傳回 **否** ，則會向使用者顯示錯誤訊息。
- 在對 TSTimesheetLine 資料表執行 **插入** 方法時填入欄位 (例如， **明細屬性** ) 的邏輯，仍將執行。

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a>透過設定隱藏內建欄位並將其標記為唯讀

您可以在行動應用程式中，透過專案參數將內建欄位設定為唯讀，或加以隱藏。 在 **專案管理與會計參數** 頁面的 **時程表** 索引標籤上，設定 **行動時程表** 區段中的選項。

![專案參數](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a>變更可透過擴充功能進行選取的活動

可供專案選取的活動是透過 **TsTimesheetProjectService** 類別中的 **getActivitiesForProject()** 和 **getActivityQuery()** 方法所填入。 您可以使用命令鏈結變更此行為，以符合可供特定專案選取之活動的商務案例。

### <a name="entering-a-default-project-category-on-timesheet-entries"></a>在時程表項目上輸入預設專案類別

在時程表項目上輸入預設專案類別會三個層級上進行。 您可以使用命令鏈結擴充任何或所有這些層級的行為，以實現所需的行為。 使用的階層如下：

1. 應用程式嘗試將預設類別從專案資源中放入。 此預設類別是在 **TSTimesheetSettingsService** 類別的 **getCurrentUserResource** 及 **getDelegatedResourcesForCurrentUser** 方法中所設定。
2. 如果未在專案資源層級提供預設類別，應用程式會嘗試從專案活動中提取此類別。 此預設類別是在 **TSTimesheetProjectService** 類別的 **getActivitiesForProject** 方法中所設定。
3. 如果未在專案活動層級提供預設類別，則會從專案參數中接受預設類別。 此預設類別是在 **TSTimesheetProjectService** 類別的 **getProjectDetailsbyRule** 方法中所設定。


[!INCLUDE[footer-include](../includes/footer-banner.md)]