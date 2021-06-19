---
title: 在 iOS 和 Android 上實作 Microsoft Dynamics 365 Project Timesheet 行動應用程式的自訂欄位
description: 本主題提供使用擴充功能實作自訂欄位的一般模式。
author: Yowelle
ms.date: 05/29/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 23b002559dcbb9118ccb2b36d70707ccb37b19ad
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6003011"
---
# <a name="implement-custom-fields-for-the-microsoft-dynamics-365-project-timesheet-mobile-app-on-ios-and-android"></a><span data-ttu-id="5e921-103">在 iOS 和 Android 上實作 Microsoft Dynamics 365 Project Timesheet 行動應用程式的自訂欄位</span><span class="sxs-lookup"><span data-stu-id="5e921-103">Implement custom fields for the Microsoft Dynamics 365 Project Timesheet mobile app on iOS and Android</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="5e921-104">本主題提供使用擴充功能實作自訂欄位的一般模式。</span><span class="sxs-lookup"><span data-stu-id="5e921-104">This topic provides common patterns for using extensions to implement custom fields.</span></span> <span data-ttu-id="5e921-105">下列主題內容涵蓋：</span><span class="sxs-lookup"><span data-stu-id="5e921-105">The following topics are covered:</span></span>

- <span data-ttu-id="5e921-106">自訂欄位架構支援的各種資料類型</span><span class="sxs-lookup"><span data-stu-id="5e921-106">The various data types that the custom field framework supports</span></span>
- <span data-ttu-id="5e921-107">如何在時程表項目上顯示唯讀或可編輯欄位，以及將使用者提供的值儲存回資料庫</span><span class="sxs-lookup"><span data-stu-id="5e921-107">How to show read-only or editable fields on timesheet entries, and save user-provided values back to the database</span></span>
- <span data-ttu-id="5e921-108">如何在時程表標題上顯示唯讀欄位</span><span class="sxs-lookup"><span data-stu-id="5e921-108">How to show read-only fields on the timesheet header</span></span>
- <span data-ttu-id="5e921-109">如何整合其他自訂，以在欄位中輸入預設值並執行其他驗證</span><span class="sxs-lookup"><span data-stu-id="5e921-109">How to integrate other custom business logic to enter default values in fields and do additional validation</span></span>

## <a name="audience"></a><span data-ttu-id="5e921-110">對象</span><span class="sxs-lookup"><span data-stu-id="5e921-110">Audience</span></span>

<span data-ttu-id="5e921-111">本主題適合要將自訂欄位整合至 Apple iOS 和 Google Android 適用版 Microsoft Dynamics 365 Project Timesheet 行動應用程式中的開發人員。</span><span class="sxs-lookup"><span data-stu-id="5e921-111">This topic is intended for developers who are integrating their custom fields into the Microsoft Dynamics 365 Project Timesheet mobile application that is available for Apple iOS and Google Android.</span></span> <span data-ttu-id="5e921-112">假設讀者熟悉 X++ 開發工作和專案時程表功能。</span><span class="sxs-lookup"><span data-stu-id="5e921-112">The assumption is that readers are familiar with X++ development and project timesheet functionality.</span></span>

## <a name="data-contract--tstimesheetcustomfield-x-class"></a><span data-ttu-id="5e921-113">資料合約 – TSTimesheetCustomField X++ 類別</span><span class="sxs-lookup"><span data-stu-id="5e921-113">Data contract – TSTimesheetCustomField X++ class</span></span>

<span data-ttu-id="5e921-114">**TSTimesheetCustomField** 類別是 X++ 資料合約類別，表示有關時程表功能自訂欄位的資訊。</span><span class="sxs-lookup"><span data-stu-id="5e921-114">The **TSTimesheetCustomField** class is the X++ data contract class that represents information about a custom field for timesheet functionality.</span></span> <span data-ttu-id="5e921-115">TSTimesheetDetails 資料合約和 TSTimesheetEntry 資料合約，都會傳遞自訂欄位物件清單，以顯示行動應用程式中的自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-115">Lists of the custom field objects are passed on both the TSTimesheetDetails data contract and the TSTimesheetEntry data contract to show custom fields in the mobile app.</span></span>

- <span data-ttu-id="5e921-116">**TSTimesheetDetails** - 時程表標題合約。</span><span class="sxs-lookup"><span data-stu-id="5e921-116">**TSTimesheetDetails** - The timesheet header contract.</span></span>
- <span data-ttu-id="5e921-117">**TSTimesheetEntry** - 時程表交易合約。</span><span class="sxs-lookup"><span data-stu-id="5e921-117">**TSTimesheetEntry** - The timesheet transaction contract.</span></span> <span data-ttu-id="5e921-118">這些有相同專案資訊及 **timesheetLineRecId** 值之物件的群組構成一行內容。</span><span class="sxs-lookup"><span data-stu-id="5e921-118">Groups of these objects that have the same project information and **timesheetLineRecId** value constitute a line.</span></span>

### <a name="fieldbasetype-types"></a><span data-ttu-id="5e921-119">fieldBaseType (類型)</span><span class="sxs-lookup"><span data-stu-id="5e921-119">fieldBaseType (Types)</span></span>

<span data-ttu-id="5e921-120">**TsTimesheetCustom** 物件上的 **FieldBaseType** 屬性決定出現應用程式中欄位的類型。</span><span class="sxs-lookup"><span data-stu-id="5e921-120">The **FieldBaseType** property on the **TsTimesheetCustom** object determines the type of the field that appears in the app.</span></span> <span data-ttu-id="5e921-121">下列支援的 **類型** 值。</span><span class="sxs-lookup"><span data-stu-id="5e921-121">The following **Types** values that are supported.</span></span>

| <span data-ttu-id="5e921-122">類型值</span><span class="sxs-lookup"><span data-stu-id="5e921-122">Types value</span></span> | <span data-ttu-id="5e921-123">類型​​</span><span class="sxs-lookup"><span data-stu-id="5e921-123">Type</span></span>              | <span data-ttu-id="5e921-124">附註​​</span><span class="sxs-lookup"><span data-stu-id="5e921-124">Notes</span></span> |
|-------------|-------------------|-------|
| <span data-ttu-id="5e921-125">0</span><span class="sxs-lookup"><span data-stu-id="5e921-125">0</span></span>           | <span data-ttu-id="5e921-126">字串 (和列舉)</span><span class="sxs-lookup"><span data-stu-id="5e921-126">String (and Enum)</span></span> | <span data-ttu-id="5e921-127">欄位會顯示為文字欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-127">The field appears as a text field.</span></span> |
| <span data-ttu-id="5e921-128">7</span><span class="sxs-lookup"><span data-stu-id="5e921-128">1</span></span>           | <span data-ttu-id="5e921-129">Integer</span><span class="sxs-lookup"><span data-stu-id="5e921-129">Integer</span></span>           | <span data-ttu-id="5e921-130">值會顯示為沒有小數位數的數字。</span><span class="sxs-lookup"><span data-stu-id="5e921-130">The value is shown as a number without decimal places.</span></span> |
| <span data-ttu-id="5e921-131">2</span><span class="sxs-lookup"><span data-stu-id="5e921-131">2</span></span>           | <span data-ttu-id="5e921-132">實數</span><span class="sxs-lookup"><span data-stu-id="5e921-132">Real</span></span>              | <span data-ttu-id="5e921-133">值會顯示為含有小數位數的數字。</span><span class="sxs-lookup"><span data-stu-id="5e921-133">The value is shown as a number that has decimal places.</span></span><p><span data-ttu-id="5e921-134">若要在應用程式中將實數值顯示為貨幣，請使用 **fieldExtenededType** 屬性。</span><span class="sxs-lookup"><span data-stu-id="5e921-134">To show the real value as a currency in the app, use the **fieldExtenededType** property.</span></span> <span data-ttu-id="5e921-135">您可以使用 **numberOfDecimals** 屬性來設定顯示的小數位數。</span><span class="sxs-lookup"><span data-stu-id="5e921-135">You can use the **numberOfDecimals** property to set the number of decimal places that are shown.</span></span></p> |
| <span data-ttu-id="5e921-136">3</span><span class="sxs-lookup"><span data-stu-id="5e921-136">3</span></span>           | <span data-ttu-id="5e921-137">日期</span><span class="sxs-lookup"><span data-stu-id="5e921-137">Date</span></span>              | <span data-ttu-id="5e921-138">日期格式是由使用者的 **日期、時間及數字格式** 設定所決定，此設定是在 **使用者選項** 的 **語言和國家/地區喜好設定** 底下指定。</span><span class="sxs-lookup"><span data-stu-id="5e921-138">Date formats are determined by the user's **Date, times, and number format** setting that is specified under **Language and country/region preference** in **User options**.</span></span> |
| <span data-ttu-id="5e921-139">4</span><span class="sxs-lookup"><span data-stu-id="5e921-139">4</span></span>           | <span data-ttu-id="5e921-140">Boolean</span><span class="sxs-lookup"><span data-stu-id="5e921-140">Boolean</span></span>           | |
| <span data-ttu-id="5e921-141">15</span><span class="sxs-lookup"><span data-stu-id="5e921-141">15</span></span>          | <span data-ttu-id="5e921-142">GUID</span><span class="sxs-lookup"><span data-stu-id="5e921-142">GUID</span></span>              | |
| <span data-ttu-id="5e921-143">16</span><span class="sxs-lookup"><span data-stu-id="5e921-143">16</span></span>          | <span data-ttu-id="5e921-144">Int64</span><span class="sxs-lookup"><span data-stu-id="5e921-144">Int64</span></span>             | |

- <span data-ttu-id="5e921-145">如果 **TSTimesheetCustomField** 物件上未提供 **stringOptions** 屬性，則會為使用者提供任意格式的文字欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-145">If the **stringOptions** property isn't provided on the **TSTimesheetCustomField** object, a free-text field is provided to the user.</span></span>

    <span data-ttu-id="5e921-146">**stringLength** 屬性可用來設定使用者所能輸入的最大字串長度。</span><span class="sxs-lookup"><span data-stu-id="5e921-146">The **stringLength** property can be used to set the maximum string length that users can enter.</span></span>

- <span data-ttu-id="5e921-147">如果 **TSTimesheetCustomField** 物件已提供 **stringOptions** 屬性，則這些清單元素是使用者只能使用選項按鈕 (圓形按鈕) 選擇的值。</span><span class="sxs-lookup"><span data-stu-id="5e921-147">If the **stringOptions** property is provided on the **TSTimesheetCustomField** object, those list elements are the only values that users can select by using option buttons (radio buttons).</span></span>

    <span data-ttu-id="5e921-148">在這種情況下，字串欄位可以做為供使用者輸入之用的列舉值。</span><span class="sxs-lookup"><span data-stu-id="5e921-148">In this case, the string field can act as an enum value for the purpose of user entry.</span></span> <span data-ttu-id="5e921-149">若要將值做為列舉儲存至資料庫，請先手動將字串值對應回列舉值，再使用命令鏈結儲存至資料庫 (如需範例請參閱本主題稍後的「使用 TSTimesheetEntryService 類別中的命令鏈結，將時程表項目從應用程式儲存回資料庫」一節)。</span><span class="sxs-lookup"><span data-stu-id="5e921-149">To save the value to the database as an enum, manually map the string value back to the enum value before you save to the database by using chain of command (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="fieldextendedtype-tscustomfieldextendedtype"></a><span data-ttu-id="5e921-150">fieldExtendedType (TSCustomFieldExtendedType)</span><span class="sxs-lookup"><span data-stu-id="5e921-150">fieldExtendedType (TSCustomFieldExtendedType)</span></span>

<span data-ttu-id="5e921-151">可以使用此屬性將實數值格式化為貨幣。</span><span class="sxs-lookup"><span data-stu-id="5e921-151">You can use this property to format real values as currency.</span></span> <span data-ttu-id="5e921-152">此方法只有在 **fieldBaseType** 值為 **實數** 時才適用。</span><span class="sxs-lookup"><span data-stu-id="5e921-152">This approach is applicable only when the **fieldBaseType** value is **Real**.</span></span>

- <span data-ttu-id="5e921-153">**TSCustomFieldExtendedType:None** – 未套用任何格式設定。</span><span class="sxs-lookup"><span data-stu-id="5e921-153">**TSCustomFieldExtendedType:None** – No formatting is applied.</span></span>
- <span data-ttu-id="5e921-154">**TSCustomFieldExtendedType::Currency** – 將值格式化為貨幣。</span><span class="sxs-lookup"><span data-stu-id="5e921-154">**TSCustomFieldExtendedType::Currency** – Format the value as currency.</span></span>

    <span data-ttu-id="5e921-155">當貨幣格式為使用中狀態時，可以使用 **stringValue** 欄位傳遞應顯示在應用程式中的貨幣代碼。</span><span class="sxs-lookup"><span data-stu-id="5e921-155">When currency formatting is active, the **stringValue** field can be used pass the currency code that should be shown in the app.</span></span> <span data-ttu-id="5e921-156">此值是唯讀值。</span><span class="sxs-lookup"><span data-stu-id="5e921-156">The value is a read-only value.</span></span>

    <span data-ttu-id="5e921-157">**realValue** 欄位包含應儲存至資料庫的金額。</span><span class="sxs-lookup"><span data-stu-id="5e921-157">The **realValue** field contains the money amount that should be saved to the database.</span></span>

### <a name="fieldsection-tscustomfieldsection"></a><span data-ttu-id="5e921-158">fieldSection (TSCustomFieldSection)</span><span class="sxs-lookup"><span data-stu-id="5e921-158">fieldSection (TSCustomFieldSection)</span></span>

<span data-ttu-id="5e921-159">您可以使用此屬性指定自訂欄位應出現在應用程式中的位置。</span><span class="sxs-lookup"><span data-stu-id="5e921-159">You can use this property specify where the custom field should appear in the app.</span></span>

- <span data-ttu-id="5e921-160">**TSCustomFieldSection::Header** – 此欄位會出現在應用程式的 **檢視更多詳細資料** 區段中。</span><span class="sxs-lookup"><span data-stu-id="5e921-160">**TSCustomFieldSection::Header** – The field will appear in the **View more details** section in the app.</span></span> <span data-ttu-id="5e921-161">這些欄位一律是唯讀。</span><span class="sxs-lookup"><span data-stu-id="5e921-161">These fields are always read-only.</span></span>
- <span data-ttu-id="5e921-162">**TSCustomFieldSection::Line** – 此欄位會在時程表項目的所有內建行欄位之後出現。</span><span class="sxs-lookup"><span data-stu-id="5e921-162">**TSCustomFieldSection::Line** – The field will appear after all the out-of-box line fields on timesheet entries.</span></span> <span data-ttu-id="5e921-163">這些欄位可能是可編輯或唯讀的欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-163">These fields can be either editable or read-only.</span></span>

### <a name="fieldname-fieldnameshort"></a><span data-ttu-id="5e921-164">fieldName (FieldNameShort)</span><span class="sxs-lookup"><span data-stu-id="5e921-164">fieldName (FieldNameShort)</span></span>

<span data-ttu-id="5e921-165">將應用程式提供的值儲存回資料庫時，此屬性會識別欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-165">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="tablename-tablenameshort"></a><span data-ttu-id="5e921-166">tableName (TableNameShort)</span><span class="sxs-lookup"><span data-stu-id="5e921-166">tableName (TableNameShort)</span></span>

<span data-ttu-id="5e921-167">將應用程式提供的值儲存回資料庫時，此屬性會識別欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-167">This property identifies the field when values that the app provides are saved back to the database.</span></span>

### <a name="iseditable-noyes"></a><span data-ttu-id="5e921-168">isEditable (NoYes)</span><span class="sxs-lookup"><span data-stu-id="5e921-168">isEditable (NoYes)</span></span>

<span data-ttu-id="5e921-169">將此屬性設定為 **是**，以指定時程表項目區段中的欄位應可供使用者編輯。</span><span class="sxs-lookup"><span data-stu-id="5e921-169">Set this property to **Yes** to specify that the field in the timesheet entry section should be editable by users.</span></span> <span data-ttu-id="5e921-170">將屬性設定為 **否**，使欄位成為唯讀欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-170">Set the property to **No** to make the field read-only.</span></span>

### <a name="ismandatory-noyes"></a><span data-ttu-id="5e921-171">isMandatory (NoYes)</span><span class="sxs-lookup"><span data-stu-id="5e921-171">isMandatory (NoYes)</span></span>

<span data-ttu-id="5e921-172">將此屬性設定為 **是**，以指定時程表項目區段中的欄位應為必要欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-172">Set this property to **Yes** to specify that the field in the timesheet entry section should be mandatory.</span></span>

### <a name="label-str"></a><span data-ttu-id="5e921-173">標籤 (str)</span><span class="sxs-lookup"><span data-stu-id="5e921-173">label (str)</span></span>

<span data-ttu-id="5e921-174">此屬性指定在應用程式中欄位旁顯示的標籤。</span><span class="sxs-lookup"><span data-stu-id="5e921-174">This property specifies the label that is shown next the field in the app.</span></span>

### <a name="stringoptions-list-of-strings"></a><span data-ttu-id="5e921-175">stringOptions (字串清單)</span><span class="sxs-lookup"><span data-stu-id="5e921-175">stringOptions (List of Strings)</span></span>

<span data-ttu-id="5e921-176">此屬性只有在 **fieldBaseType** 設定為 **字串** 時才適用。</span><span class="sxs-lookup"><span data-stu-id="5e921-176">This property is applicable only when **fieldBaseType** is set to **String**.</span></span> <span data-ttu-id="5e921-177">如果 **stringOptions** 已設定，可透過選項按鈕 (圓形按鈕) 使用的字串值是由清單中的字串所指定。</span><span class="sxs-lookup"><span data-stu-id="5e921-177">If **stringOptions** is set, the string values that are available for selection via option buttons (radio buttons) are specified by the strings in the list.</span></span> <span data-ttu-id="5e921-178">如果未提供任何字串，則允許在字串欄位中輸入任意格式的文字 (如需範例，請參閱本主題稍後的「使用 TSTimesheetEntryService 類別中的命令鏈結，將時程表項目從應用程式儲存回資料庫」一節)。</span><span class="sxs-lookup"><span data-stu-id="5e921-178">If no strings are provided, free-text entry in the string field is allowed (see the “Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database” section later in this topic for an example).</span></span>

### <a name="stringlength-int"></a><span data-ttu-id="5e921-179">stringLength (int)</span><span class="sxs-lookup"><span data-stu-id="5e921-179">stringLength (int)</span></span>

<span data-ttu-id="5e921-180">此屬性指定字串欄位的最大長度。</span><span class="sxs-lookup"><span data-stu-id="5e921-180">This property specifies the maximum length for a string field.</span></span> <span data-ttu-id="5e921-181">這只有在 **fieldBaseType** 設定為 **字串** 時才適用。</span><span class="sxs-lookup"><span data-stu-id="5e921-181">It's applicable only when **fieldBaseType** is set to **String**.</span></span>

### <a name="numberofdecimals-int"></a><span data-ttu-id="5e921-182">numberOfDecimals (int)</span><span class="sxs-lookup"><span data-stu-id="5e921-182">numberOfDecimals (int)</span></span>

<span data-ttu-id="5e921-183">此屬性指定實數欄位顯示的小數位數。</span><span class="sxs-lookup"><span data-stu-id="5e921-183">This property specifies the number of decimal places that are shown for a real field.</span></span> <span data-ttu-id="5e921-184">這只有在 **fieldBaseType** 設定為 **實數** 時才適用。</span><span class="sxs-lookup"><span data-stu-id="5e921-184">It's applicable only when **fieldBaseType** is set to **Real**.</span></span>

### <a name="ordersequence-int"></a><span data-ttu-id="5e921-185">orderSequence (int)</span><span class="sxs-lookup"><span data-stu-id="5e921-185">orderSequence (int)</span></span>

<span data-ttu-id="5e921-186">此屬性可在指定了多個自訂欄位時，控制自訂欄位顯示在應用程式中所依照的順序。</span><span class="sxs-lookup"><span data-stu-id="5e921-186">This property controls the order in which the custom fields are shown in the app when more than one custom field is specified.</span></span> <span data-ttu-id="5e921-187">編號較小的欄位會先顯示。</span><span class="sxs-lookup"><span data-stu-id="5e921-187">Fields that have lower numbers are shown first.</span></span>

### <a name="booleanvalue-boolean"></a><span data-ttu-id="5e921-188">booleanValue (布林值)</span><span class="sxs-lookup"><span data-stu-id="5e921-188">booleanValue (boolean)</span></span>

<span data-ttu-id="5e921-189">對於 **布林值** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞布林值的欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-189">For fields of the **Boolean** type, this property passes the Boolean value of the field between the server and the app.</span></span>

### <a name="guidvalue-guid"></a><span data-ttu-id="5e921-190">guidValue (guid)</span><span class="sxs-lookup"><span data-stu-id="5e921-190">guidValue (guid)</span></span>

<span data-ttu-id="5e921-191">對於 **GUID** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞全域唯一識別碼 (GUID) 值的欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-191">For fields of the **GUID** type, this property passes the globally unique identifier (GUID) value of the field between the server and the app.</span></span>

### <a name="int64value-int64"></a><span data-ttu-id="5e921-192">int64Value (int64)</span><span class="sxs-lookup"><span data-stu-id="5e921-192">int64Value (int64)</span></span>

<span data-ttu-id="5e921-193">對於 **Int64** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞 Int64 值的欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-193">For fields of the **Int64** type, this property passes the int64 value of the field between the server and the app.</span></span>

### <a name="intvalue-int"></a><span data-ttu-id="5e921-194">intValue (int)</span><span class="sxs-lookup"><span data-stu-id="5e921-194">intValue (int)</span></span>

<span data-ttu-id="5e921-195">對於 **Int** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞 Int 值的欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-195">For fields of the **Int** type, this property passes the int value of the field between the server and the app.</span></span>

### <a name="realvalue-real"></a><span data-ttu-id="5e921-196">realValue (實數)</span><span class="sxs-lookup"><span data-stu-id="5e921-196">realValue (real)</span></span>

<span data-ttu-id="5e921-197">對於 **實數** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞實數值的欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-197">For fields of the **Real** type, this property passes the real value of the field between the server and the app .</span></span>

### <a name="stringvalue-str"></a><span data-ttu-id="5e921-198">stringValue (str)</span><span class="sxs-lookup"><span data-stu-id="5e921-198">stringValue (str)</span></span>

<span data-ttu-id="5e921-199">對於 **字串** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞字串值的欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-199">For fields of the **String** type, this property passes the string value of the field between the server and the app.</span></span> <span data-ttu-id="5e921-200">這也會用於格式設為貨幣的 **實數** 類型欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-200">It's also used for fields of the **Real** type that are formatted as currency.</span></span> <span data-ttu-id="5e921-201">在這些欄位中，此屬性會用來將貨幣代碼傳遞至應用程式。</span><span class="sxs-lookup"><span data-stu-id="5e921-201">For those fields, the property is used to pass the currency code to the app.</span></span>

### <a name="datevalue-date"></a><span data-ttu-id="5e921-202">dateValue (日期)</span><span class="sxs-lookup"><span data-stu-id="5e921-202">dateValue (date)</span></span>

<span data-ttu-id="5e921-203">對於 **日期** 類型的欄位，此屬性會在伺服器與應用程式之間傳遞日期值的欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-203">For fields of the **Date** type, this property passes the date value of the field between the server and the app.</span></span>

## <a name="show-and-save-a-custom-field-in-the-timesheet-entry-section"></a><span data-ttu-id="5e921-204">在時程表項目區段中顯示並儲存自訂欄位</span><span class="sxs-lookup"><span data-stu-id="5e921-204">Show and save a custom field in the timesheet entry section</span></span>

<span data-ttu-id="5e921-205">以下是建立時程表項目的行動應用程式螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="5e921-205">Below is a screenshot from the mobile app of a timesheet entry creation.</span></span> <span data-ttu-id="5e921-206">此畫面顯示 [時間項目] 區段 (稱為「測試字串」) 中的內建欄位和自訂欄位，其中已經設定「第二個選項」的列舉值。</span><span class="sxs-lookup"><span data-stu-id="5e921-206">It shows the out-of-box fields and a custom field in the "Time entry" section called "Test string" with an enum value of "Second option" already set.</span></span>

![應用程式中的測試字串自訂欄位](media/timesheet-entry.jpg)



<span data-ttu-id="5e921-208">以下是使用者為 [測試字串] 自訂欄位選取其中一個可用列舉值的行動應用程式螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="5e921-208">Below is a screenshot from the mobile app of the user selecting one of the enum options available for the "Test string" custom field.</span></span>  <span data-ttu-id="5e921-209">這兩個選項是顯示為選項按鈕的 [第一個選項] 和 [第二個選項]。</span><span class="sxs-lookup"><span data-stu-id="5e921-209">The two options are "First option" and "Second option" shown as radio buttons.</span></span> <span data-ttu-id="5e921-210">目前已選取第二個選項。</span><span class="sxs-lookup"><span data-stu-id="5e921-210">The second option is currently selected.</span></span>

![[測試字串] 自訂欄位的選項按鈕 (圓形按鈕)](media/enum-option.jpg)



### <a name="extend-the-tstimesheetline-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="5e921-212">擴充 TSTimesheetLine 資料表，使其中含有自訂欄位</span><span class="sxs-lookup"><span data-stu-id="5e921-212">Extend the TSTimesheetLine table so that it has a custom field</span></span>

<span data-ttu-id="5e921-213">在一般案例中，時程表項目區段中自訂欄位的資料很可能會儲存至 TSTimesheetLine 資料表。</span><span class="sxs-lookup"><span data-stu-id="5e921-213">In typical scenarios, it's likely that the data for a custom field in the timesheet entry section will be saved to the TSTimesheetLine table.</span></span> <span data-ttu-id="5e921-214">不過，如果資料可以根據提供的 TSTimesheetTrans 記錄來擷取，或者資料沒有特定記錄內容 (例如，如果欄位在專案參數中設定為唯讀)，則可以使用其他資料表。</span><span class="sxs-lookup"><span data-stu-id="5e921-214">However, other tables can be used if the data can be retrieved based on a TSTimesheetTrans record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="5e921-215">請注意，自訂欄位不一定有任何支援資料庫記錄。</span><span class="sxs-lookup"><span data-stu-id="5e921-215">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="5e921-216">這些欄位可以根據 X++ 邏輯動態產生。</span><span class="sxs-lookup"><span data-stu-id="5e921-216">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="5e921-217">此方法在唯讀案例中很實用 (如需動態產生自訂欄位值的範例，請參閱「使用 TSTimesheetDetails 類別中的命令鏈結、buildCustomFieldListForHeader 方法來填入時程表詳細資料」一節)。</span><span class="sxs-lookup"><span data-stu-id="5e921-217">This approach can be useful in read-only scenarios (see the “Use chain of command on the TSTimesheetDetails class, buildCustomFieldListForHeader method to fill in timesheet details” section for an example of dynamically generated custom field values.)</span></span>

<span data-ttu-id="5e921-218">以下是應用程式物件樹狀結構的 Visual Studio 螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="5e921-218">Below is a screenshot from Visual Studio of the Application Object Tree.</span></span> <span data-ttu-id="5e921-219">此畫面顯示 TSTimesheetLine 資料表的擴充功能，其中 TestLineString 欄位已新增為自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-219">It shows an extension of the TSTimesheetLine table with the TestLineString field added as a custom field.</span></span>

![行字串](media/b6756b4a3fc5298093327a088a7710fd.png)

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-timesheet-entry-section"></a><span data-ttu-id="5e921-221">使用 TSTimesheetSettings 類別在 buildCustomFieldList 方法中的命令鏈結，以在時程表項目區段中顯示欄位</span><span class="sxs-lookup"><span data-stu-id="5e921-221">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the timesheet entry section</span></span>

<span data-ttu-id="5e921-222">此程式碼會控制應用程式中欄位的顯示設定。</span><span class="sxs-lookup"><span data-stu-id="5e921-222">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="5e921-223">例如，會控制欄位類型、標籤、欄位是否必填，以及欄位顯示所在的區段。</span><span class="sxs-lookup"><span data-stu-id="5e921-223">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="5e921-224">下列範例在時間項目上顯示字串欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-224">The following example shows a string field on time entries.</span></span> <span data-ttu-id="5e921-225">此欄位有兩個選項：**第一個選項** 和 **第二個選項**，可透過選項按鈕 (圓形按鈕) 來使用。</span><span class="sxs-lookup"><span data-stu-id="5e921-225">This field has two options, **First option** and **Second option**, that are available via option buttons (radio buttons).</span></span> <span data-ttu-id="5e921-226">應用程式中的欄位會與新增至 TSTimesheetLine 資料表的 **TestLineString** 欄位相關聯。</span><span class="sxs-lookup"><span data-stu-id="5e921-226">The field in the app is associated with the **TestLineString** field that is added to the TSTimesheetLine table.</span></span>

<span data-ttu-id="5e921-227">請注意，使用 **TSTimesheetCustomField::newFromMetatdata()** 方法來簡化下列自訂欄位屬性的初始化：**fieldBaseType**、**tableName**、**fieldname**、**標籤**、**isEditable**、**isMandatory**、**stringLength** 和 **numberOfDecimals**。</span><span class="sxs-lookup"><span data-stu-id="5e921-227">Note the use of the **TSTimesheetCustomField::newFromMetatdata()** method to simplify the initialization of the custom field properties: **fieldBaseType**, **tableName**, **fieldname**, **label**, **isEditable**, **isMandatory**, **stringLength**, and **numberOfDecimals**.</span></span> <span data-ttu-id="5e921-228">您也可以依自己喜好手動設定這些參數。</span><span class="sxs-lookup"><span data-stu-id="5e921-228">You can also set these parameters manually, as you prefer.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforentry-method-of-the-tstimesheetentry-class-to-enter-values-in-a-timesheet-entry"></a><span data-ttu-id="5e921-229">使用 TSTimesheetEntry 類別在 buildCustomFieldListForEntry 方法中的命令鏈結，以在時程表項目中輸入值</span><span class="sxs-lookup"><span data-stu-id="5e921-229">Use chain of command on the buildCustomFieldListForEntry method of the TSTimesheetEntry class to enter values in a timesheet entry</span></span>

<span data-ttu-id="5e921-230">**BuildCustomFieldListForEntry** 方法可在行動應用程式中用來輸入已儲存時程表行上的值。</span><span class="sxs-lookup"><span data-stu-id="5e921-230">The **buildCustomFieldListForEntry** method is used to enter values on the saved timesheet lines in the mobile app.</span></span> <span data-ttu-id="5e921-231">這會接受 TSTimesheetTrans 記錄做為參數。</span><span class="sxs-lookup"><span data-stu-id="5e921-231">It takes a TSTimesheetTrans record as a parameter.</span></span> <span data-ttu-id="5e921-232">該記錄中的欄位可以用來填入應用程式中的自訂欄位值。</span><span class="sxs-lookup"><span data-stu-id="5e921-232">Fields from that record can be used to fill in the custom field value in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-tstimesheetentryservice-class-to-save-a-timesheet-entry-from-the-app-back-to-the-database"></a><span data-ttu-id="5e921-233">使用 TSTimesheetEntryService 類別中的命令鏈結，將應用程式中的時程表項目儲存回資料庫</span><span class="sxs-lookup"><span data-stu-id="5e921-233">Use chain of command on the TSTimesheetEntryService class to save a timesheet entry from the app back to the database</span></span>

<span data-ttu-id="5e921-234">若要以一般使用方式將自訂欄位儲存回資料庫，您必須擴充多個方法：</span><span class="sxs-lookup"><span data-stu-id="5e921-234">To save a custom field back to the database in typical usage, you must extend multiple methods:</span></span>

- <span data-ttu-id="5e921-235">**TimesheetLineNeedsUpdating** 方法會用來判斷行記錄是否已由應用程式中的使用者所變更，以及是否必須儲存至資料庫。</span><span class="sxs-lookup"><span data-stu-id="5e921-235">The **timesheetLineNeedsUpdating** method is used to determine whether the line record has been changed by the user in the app and must be saved to the database.</span></span> <span data-ttu-id="5e921-236">如果不需顧慮效能，則可以簡化此方法，使其永遠傳回 **是**。</span><span class="sxs-lookup"><span data-stu-id="5e921-236">If performance isn't a concern, this method can be simplified so that it always returns **true**.</span></span>
- <span data-ttu-id="5e921-237">您可以擴充 **populateTimesheetLineFromEntryDuringCreate** 和 **populateTimesheetLineFromEntryDuringUpdate** 方法，讓這些方法從提供的 TSTimesheetEntry 資料合約記錄輸入 TSTimesheetLine 資料庫記錄中的值。</span><span class="sxs-lookup"><span data-stu-id="5e921-237">The **populateTimesheetLineFromEntryDuringCreate** and **populateTimesheetLineFromEntryDuringUpdate** methods can be extended so that they enter values in the TSTimesheetLine database record from the TSTimesheetEntry data contract record that is provided.</span></span> <span data-ttu-id="5e921-238">在後面的範例中，請注意資料庫欄位與輸入欄位之間的對應是如何透過 X++ 程式碼手動完成。</span><span class="sxs-lookup"><span data-stu-id="5e921-238">In the example that follows, notice how the mapping between the database field and the entry field is manually done via X++ code.</span></span>
- <span data-ttu-id="5e921-239">如果對應至 **TSTimesheetEntry** 物件的自訂欄位必須寫回至 TSTimesheetLineweek 資料庫資料表，您對，如果則為擴充 **populateTimesheetWeekFromEntry** 方法。</span><span class="sxs-lookup"><span data-stu-id="5e921-239">The **populateTimesheetWeekFromEntry** method can also be extended if the custom field that is mapped to the **TSTimesheetEntry** object must write back to the TSTimesheetLineweek database table.</span></span>

> [!NOTE]
> <span data-ttu-id="5e921-240">下列範例會將使用者選取的 **firstOption** 或 **secondOption** 值做為原始字串值儲存至資料庫。</span><span class="sxs-lookup"><span data-stu-id="5e921-240">The following example saves the **firstOption** or **secondOption** value that the user selects to the database as a raw string value.</span></span> <span data-ttu-id="5e921-241">如果資料庫欄位是 **列舉** 類型的欄位，則可以將這些值手動對應至列舉值，然後儲存至資料庫表中的列舉欄位。</span><span class="sxs-lookup"><span data-stu-id="5e921-241">If the database field is a field of the **Enum** type, those values can be manually mapped to an enum value and then saved to an enum field on the database table.</span></span>

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

## <a name="show-a-custom-field-in-the-timesheet-header-section"></a><span data-ttu-id="5e921-242">在時程表標題區段中顯示自訂欄位</span><span class="sxs-lookup"><span data-stu-id="5e921-242">Show a custom field in the timesheet header section</span></span>

<span data-ttu-id="5e921-243">以下是使用者檢視時程表的行動應用程式螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="5e921-243">Below is a screenshot from the mobile app of a user viewing a timesheet.</span></span> <span data-ttu-id="5e921-244">已選取右上角的 [其他資訊] 按鈕來顯示 [檢視更多詳細資料] 選項。</span><span class="sxs-lookup"><span data-stu-id="5e921-244">The "More information" button has been selected in the upper-right corner to show the "View more details" option.</span></span>  

![[檢視更多詳細資料] 命令](media/show-more.png)

<span data-ttu-id="5e921-246">以下是顯示時程表 [其他] 區段的行動應用程式螢幕擷取畫面。</span><span class="sxs-lookup"><span data-stu-id="5e921-246">Below is a screenshot from the mobile app showing the “More” section of a timesheet.</span></span> <span data-ttu-id="5e921-247">已將名為「此時程表的利用率 (自訂計算欄位)」的自訂欄位新增至時程表標題區段。</span><span class="sxs-lookup"><span data-stu-id="5e921-247">A custom field called “Utilization rate of this timesheet (computed custom field)” has been added to the timesheet header section.</span></span> <span data-ttu-id="5e921-248">自訂欄位上已設定「0.667」的唯讀值。</span><span class="sxs-lookup"><span data-stu-id="5e921-248">A read-only value of "0.667" is set on the custom field.</span></span>

![其他區段](media/more-section.jpg)

### <a name="extend-the-tstimesheettable-table-so-that-it-has-a-custom-field"></a><span data-ttu-id="5e921-250">擴充 TSTimesheetTable 資料表，使其中含有自訂欄位</span><span class="sxs-lookup"><span data-stu-id="5e921-250">Extend the TSTimesheetTable table so that it has a custom field</span></span>

<span data-ttu-id="5e921-251">在一般案例中，很可能會從 TSTimesheetHeader 資料表提取標題區段中自訂欄位的資料。</span><span class="sxs-lookup"><span data-stu-id="5e921-251">In typical scenarios, it's likely that the data for a custom field in the header section will be pulled from the TSTimesheetHeader table.</span></span> <span data-ttu-id="5e921-252">不過，如果資料可以根據提供的 TSTimesheetTable 記錄來擷取，或者資料沒有特定記錄內容 (例如，如果欄位在專案參數中設定為唯讀)，則可以使用其他資料表。</span><span class="sxs-lookup"><span data-stu-id="5e921-252">However, other tables can be used if the data can be retrieved based on a TSTimesheetTable record that is provided, or if it doesn't have specific record context (for example, if the field is set as read-only in the project parameters).</span></span>

<span data-ttu-id="5e921-253">請注意，自訂欄位不一定有任何支援資料庫記錄。</span><span class="sxs-lookup"><span data-stu-id="5e921-253">Note that custom fields don't have to have any backing database records.</span></span> <span data-ttu-id="5e921-254">這些欄位可以根據 X++ 邏輯動態產生。</span><span class="sxs-lookup"><span data-stu-id="5e921-254">They can be dynamically generated based on X++ logic.</span></span> <span data-ttu-id="5e921-255">下面的範例會說明此方法。</span><span class="sxs-lookup"><span data-stu-id="5e921-255">The example that follows shows this approach.</span></span>

<span data-ttu-id="5e921-256">標題區段的欄位在應用程式中永遠為唯讀。</span><span class="sxs-lookup"><span data-stu-id="5e921-256">Fields in the header section are always read-only in the app.</span></span>

### <a name="use-chain-of-command-on-the-buildcustomfieldlist-method-of-the-tstimesheetsettings-class-to-show-a-field-in-the-header-section"></a><span data-ttu-id="5e921-257">使用 TSTimesheetSettings 類別在 buildCustomFieldList 方法中的命令鏈結，以在標題區段中顯示欄位</span><span class="sxs-lookup"><span data-stu-id="5e921-257">Use chain of command on the buildCustomFieldList method of the TSTimesheetSettings class to show a field in the header section</span></span>

<span data-ttu-id="5e921-258">此程式碼會控制應用程式中欄位的顯示設定。</span><span class="sxs-lookup"><span data-stu-id="5e921-258">This code controls the display settings for the field in the app.</span></span> <span data-ttu-id="5e921-259">例如，會控制欄位類型、標籤、欄位是否必填，以及欄位顯示所在的區段。</span><span class="sxs-lookup"><span data-stu-id="5e921-259">For example, it controls the type of field, the label, whether the field is mandatory, and what section the field appears in.</span></span>

<span data-ttu-id="5e921-260">下列範例說明標題區段在應用程式中的計算值。</span><span class="sxs-lookup"><span data-stu-id="5e921-260">The following example shows a computed value in the header section in the app.</span></span>

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

### <a name="use-chain-of-command-on-the-buildcustomfieldlistforheader-method-of-the-tstimesheetdetails-class-to-fill-in-timesheet-details"></a><span data-ttu-id="5e921-261">使用 TSTimesheetDetails 類別在 buildCustomFieldListForHeader 方法中的命令鏈結，以填入時程表詳細資料</span><span class="sxs-lookup"><span data-stu-id="5e921-261">Use chain of command on the buildCustomFieldListForHeader method of the TSTimesheetDetails class to fill in timesheet details</span></span>

<span data-ttu-id="5e921-262">**buildCustomFieldListForHeader** 方法可在行動應用程式中用來填入時程表標題詳細資料。</span><span class="sxs-lookup"><span data-stu-id="5e921-262">The **buildCustomFieldListForHeader** method is used to fill in the timesheet header details in the mobile app.</span></span> <span data-ttu-id="5e921-263">這會接受 TSTimesheetTable 記錄做為參數。</span><span class="sxs-lookup"><span data-stu-id="5e921-263">It takes a TSTimesheetTable record as a parameter.</span></span> <span data-ttu-id="5e921-264">該記錄中的欄位可以用來填入應用程式中的自訂欄位值。</span><span class="sxs-lookup"><span data-stu-id="5e921-264">Fields from that record can be used to fill in the custom field value in the app.</span></span> <span data-ttu-id="5e921-265">下列範例不會從資料庫讀取任何值。</span><span class="sxs-lookup"><span data-stu-id="5e921-265">The following example doesn't read any values from the database.</span></span> <span data-ttu-id="5e921-266">反而是使用 X++ 邏輯來產生接著在應用程式中顯示的計算值。</span><span class="sxs-lookup"><span data-stu-id="5e921-266">Instead, it uses X++ logic to generate a computed value that is then shown in the app.</span></span>


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

## <a name="other-configurabilityextensibility-opportunities"></a><span data-ttu-id="5e921-267">其他可設定性/擴充性商機</span><span class="sxs-lookup"><span data-stu-id="5e921-267">Other configurability/extensibility opportunities</span></span>

### <a name="adding-additional-validation-for-the-app"></a><span data-ttu-id="5e921-268">為應用程式新增其他驗證</span><span class="sxs-lookup"><span data-stu-id="5e921-268">Adding additional validation for the app</span></span>

<span data-ttu-id="5e921-269">時程表功能在資料庫層級的現有邏輯仍可依預期正常運作。</span><span class="sxs-lookup"><span data-stu-id="5e921-269">Existing logic for timesheet functionality at the database level will still work as expected.</span></span> <span data-ttu-id="5e921-270">若要中斷完成儲存或提交作業並顯示特定錯誤訊息，您可以透過擴充命令鏈結，將 **擲回錯誤 (「傳送訊息給使用者」)** 新增至程式碼。</span><span class="sxs-lookup"><span data-stu-id="5e921-270">To interrupt the completion of save or submit operations and show a specific error message, you can add **throw error("message to user")** to the code via a chain of command extension.</span></span> <span data-ttu-id="5e921-271">以下是三個實用擴充方法的範例：</span><span class="sxs-lookup"><span data-stu-id="5e921-271">Here are three examples of useful extensible methods:</span></span>

- <span data-ttu-id="5e921-272">如果 TSTimesheetLine 資料表上的 **validateWrite 在** 時程表行的儲存作業期間傳回 **否**，則行動應用程式中會顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="5e921-272">If **validateWrite** on the TSTimesheetLine table returns **false** during a save operation for a timesheet line, an error message is shown in the mobile app.</span></span>
- <span data-ttu-id="5e921-273">如果 TSTimesheetTable 資料表上的 **validateSubmit** 在應用程式的時程表行提交期間傳回 **否**，則會向使用者顯示錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="5e921-273">If **validateSubmit** on the TSTimesheetTable table returns **false** during timesheet submission in the app, an error message is shown to the user.</span></span>
- <span data-ttu-id="5e921-274">在對 TSTimesheetLine 資料表執行 **插入** 方法時填入欄位 (例如，**明細屬性**) 的邏輯，仍將執行。</span><span class="sxs-lookup"><span data-stu-id="5e921-274">Logic that fills in fields (for example, **Line Property**) during the **insert** method on the TSTimesheetLine table will still run.</span></span>

### <a name="hiding-and-marking-out-of-box-fields-as-read-only-via-configuration"></a><span data-ttu-id="5e921-275">透過設定隱藏內建欄位並將其標記為唯讀</span><span class="sxs-lookup"><span data-stu-id="5e921-275">Hiding and marking out-of-box fields as read-only via configuration</span></span>

<span data-ttu-id="5e921-276">您可以在行動應用程式中，透過專案參數將內建欄位設定為唯讀，或加以隱藏。</span><span class="sxs-lookup"><span data-stu-id="5e921-276">From the project parameters, you can make out-of-box fields read-only or hidden in the mobile app.</span></span> <span data-ttu-id="5e921-277">在 **專案管理與會計參數** 頁面的 **時程表** 索引標籤上，設定 **行動時程表** 區段中的選項。</span><span class="sxs-lookup"><span data-stu-id="5e921-277">Set the options in the **Mobile timesheets** section on the **Timesheet** tab of the **Project management and accounting parameters** page.</span></span>

![專案參數](media/5753b8ecccd1d8bb2b002dd538b3f762.png)

### <a name="changing-the-activities-that-are-available-for-selection-via-extensions"></a><span data-ttu-id="5e921-279">變更可透過擴充功能進行選取的活動</span><span class="sxs-lookup"><span data-stu-id="5e921-279">Changing the activities that are available for selection via extensions</span></span>

<span data-ttu-id="5e921-280">可供專案選取的活動是透過 **TsTimesheetProjectService** 類別中的 **getActivitiesForProject()** 和 **getActivityQuery()** 方法所填入。</span><span class="sxs-lookup"><span data-stu-id="5e921-280">The activities that are available for selection for a project are filled in via the **getActivitiesForProject()** and **getActivityQuery()** methods in the **TsTimesheetProjectService** class.</span></span> <span data-ttu-id="5e921-281">您可以使用命令鏈結變更此行為，以符合可供特定專案選取之活動的商務案例。</span><span class="sxs-lookup"><span data-stu-id="5e921-281">You can use chain of command to change this behavior to match your business scenario for the activities that are available for selection for a specific project.</span></span>

### <a name="entering-a-default-project-category-on-timesheet-entries"></a><span data-ttu-id="5e921-282">在時程表項目上輸入預設專案類別</span><span class="sxs-lookup"><span data-stu-id="5e921-282">Entering a default project category on timesheet entries</span></span>

<span data-ttu-id="5e921-283">在時程表項目上輸入預設專案類別會三個層級上進行。</span><span class="sxs-lookup"><span data-stu-id="5e921-283">Entry of a default project category on timesheet entries occurs at three levels.</span></span> <span data-ttu-id="5e921-284">您可以使用命令鏈結擴充任何或所有這些層級的行為，以實現所需的行為。</span><span class="sxs-lookup"><span data-stu-id="5e921-284">You can use chain of command to extend the behavior at any or all of these levels to achieve the desired behavior.</span></span> <span data-ttu-id="5e921-285">使用的階層如下：</span><span class="sxs-lookup"><span data-stu-id="5e921-285">The following hierarchy is used:</span></span>

1. <span data-ttu-id="5e921-286">應用程式嘗試將預設類別從專案資源中放入。</span><span class="sxs-lookup"><span data-stu-id="5e921-286">The app tries to put the default category from the project resource.</span></span> <span data-ttu-id="5e921-287">此預設類別是在 **TSTimesheetSettingsService** 類別的 **getCurrentUserResource** 及 **getDelegatedResourcesForCurrentUser** 方法中所設定。</span><span class="sxs-lookup"><span data-stu-id="5e921-287">This default category is set in the **getCurrentUserResource** and **getDelegatedResourcesForCurrentUser** methods in the **TSTimesheetSettingsService** class.</span></span>
2. <span data-ttu-id="5e921-288">如果未在專案資源層級提供預設類別，應用程式會嘗試從專案活動中提取此類別。</span><span class="sxs-lookup"><span data-stu-id="5e921-288">If the default category isn't provided at the project resource level, the app tries to pull it from the project activity.</span></span> <span data-ttu-id="5e921-289">此預設類別是在 **TSTimesheetProjectService** 類別的 **getActivitiesForProject** 方法中所設定。</span><span class="sxs-lookup"><span data-stu-id="5e921-289">This default category is set in the **getActivitiesForProject** method in the **TSTimesheetProjectService** class.</span></span>
3. <span data-ttu-id="5e921-290">如果未在專案活動層級提供預設類別，則會從專案參數中接受預設類別。</span><span class="sxs-lookup"><span data-stu-id="5e921-290">If the default category isn't provided at the project activity level, the default category it taken from the project parameters.</span></span> <span data-ttu-id="5e921-291">此預設類別是在 **TSTimesheetProjectService** 類別的 **getProjectDetailsbyRule** 方法中所設定。</span><span class="sxs-lookup"><span data-stu-id="5e921-291">This default category is set in the **getProjectDetailsbyRule** method in the **TSTimesheetProjectService** class.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]