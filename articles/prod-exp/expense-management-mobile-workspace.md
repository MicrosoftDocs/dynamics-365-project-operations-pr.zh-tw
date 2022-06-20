---
title: 費用管理行動工作區
description: 本文提供費用管理行動工作區的相關資訊。 此工作區允許使用者擷取並上傳收據，讓他們可以稍後將收據附加至費用報表。 使用者也可以使用附加的收據快速建立費用明細，並建立和管理他們的費用報表。
author: suvaidya
ms.date: 12/01/2017
ms.topic: article
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: aba8073fcf788f94bbcc622ab963426d230e9999
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8920878"
---
# <a name="expense-management-mobile-workspace"></a>費用管理行動工作區

本文提供 **費用管理** 行動工作區的相關資訊。 此工作區允許使用者擷取並上傳收據，讓他們可以稍後將收據附加至費用報表。 使用者也可以使用附加的收據快速建立費用明細，並建立和管理他們的費用報表。 此外，核准者還可以使用 **費用管理** 行動工作區來檢視指派給他們的費用報表，並核准或拒絕這些費用報表。


此行動工作區旨在與 Dynamics 365 Unified Ops 行動應用程式搭配使用。


## <a name="overview"></a>概觀

許多組織都需要將收據複本附加至員工所提交請求報銷的差旅相關或業務相關費用報表。 **費用管理** 行動工作區可讓使用者使用附加的收據相片，在行動裝置上快速建立新的費用明細。 或者，使用者也可以擷取收據的相片，稍後再將其附加至費用報表。 員工還可以建立和管理其費用報表，然後使用行動裝置提交這些報表以請求核准和報銷。


明確地說，**費用管理** 行動工作區可讓使用者執行下列工作：

- 拍攝收據的相片，並將其上傳至 Dynamics 365 Finance。 您可以稍後再將該相片附加至費用報表。
- 上傳檔案做為已擷取的收據。 您可以稍後再將該檔案附加至費用報表。
- 使用附加的收據建立新的費用明細。 您可以稍後再將明細項目新增至費用報表，並提交以請求核准和報銷。

您也可以使用下列功能：

- 建立新的費用報表。
- 將信用卡交易記錄以及其他先前建立的費用附加至費用報表。
- 為費用報表建立新的費用。
- 拍攝收據的相片，或上傳檔案做為已擷取的收據，以將收據附加至費用報表的任何費用。
- 根據公司的費用原則，將來賓名單新增至費用。
- 根據公司的費用原則，逐條列舉費用。
- 提交費用報表以請求核准和報銷。
- 核准或拒絕您受指派為核准者的費用報表。

## <a name="prerequisites"></a>先決條件
視組織已部署的版本而定，先決條件會有所不同。

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>使用 Dynamics 365 Finance 時的先決條件 
如果您的組織已部署 Finance，則系統系統管理員必須發佈 **費用管理** 行動工作區。 如需指示，請參閱[發佈行動工作區](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace)。

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>使用版本 1611 (含平台更新 3) 或更新版本時的先決條件
如果您的組織已部署版本 1611 (含平台更新 3) 或更新版本，則系統系統管理員必須完成下列先決條件。 

<table>
<thead>
<tr class="header">
<th>先決條件</th>
<th>角色</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>實作 KB 4019015。</td>
<td>系統管理員</td>
<td>KB 4019015 是包含<strong>費用管理</strong>行動工作區的 X++ 更新或中繼資料 Hotfix。 若要實作 KB 4019015，您的系統系統管理員必須依照下列步驟進行。
<ol>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#download-the-hotfix-from-lcs">從 Microsoft Dynamics Lifecycle Services (LCS) 下載中繼資料 Hotfix</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/migration-upgrade/install-metadata-hotfix-package#install-the-metadata-hotfix-package">安裝中繼資料 Hotfix</a>。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/create-apply-deployable-package">建立的可部署套件</a> (內含 <strong>ApplicationSuite</strong> 和 <strong>ExpenseMobile</strong> 模型)，然後將可部署套件上傳至 LCS。</li>
<li><a href="/dynamics365/fin-ops-core/dev-itpro/deployment/apply-deployable-package-system">套用可部署套件</a>。</li>
</ol></td>
</tr>
<tr class="even">
<td>傳回<strong>費用管理</strong>行動工作區。</td>
<td>系統管理員</td>
<td>請參閱<a href="/dynamics365/fin-ops-core/dev-itpro/mobile-apps/publish-mobile-workspace">發佈行動工作區</a>。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-dynamics-365-for-operations-mobile-app"></a>下載並安裝 Dynamics 365 for Operations 行動應用程式
下載並安裝 Dynamics 365 Unified Ops 行動應用程式：

- [適用於 Android 手機](https://go.microsoft.com/fwlink/?linkid=850662)
- [適用於 iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>登入行動應用程式
1. 在行動裝置上啟動應用程式。
2. 輸入您的 Dynamics 365 URL。
4. 第一次登入時，系統會提示您輸入您的使用者名稱和密碼。 輸入您的認證。
5. 登入後，會顯示您公司可用的工作區。 請注意，如果系統管理員稍後發佈了新的工作區，您就必須重新整理行動工作區的清單。


[![拖動以重新整理。](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="capture-a-receipt-by-using-the-expense-management-mobile-workspace"></a>使用費用管理行動工作區來擷取收據

1. 在行動裝置上，開啟 **費用管理** 工作區。
2. 選取 **擷取收據**。
3. 選取 **拍攝相片** 或 **選擇影像**。
4. 依照下列其中一個驟操作︰

    - 如果選取了 **拍攝相片**，請執行下列步驟：

        1. 您會進入行動裝置上的相機，以便拍攝收據的相片。 完成拍照後，選取 **確定** 以接受相片。
        2. 選擇性：輸入相片的名稱，然後輸入任何附註。

    - 如果選取了 **選擇影像**，請執行下列步驟：

        1. 選取清單中的影像。
        2. 選擇性：輸入影像的名稱，然後輸入任何附註。

5. 選取 **完成**。

## <a name="quickly-enter-expenses-by-using-the-expense-management-mobile-workspace"></a>使用費用管理行動工作區快速輸入費用
1. 在行動裝置上，開啟 **費用管理** 工作區。
2. 選取 **快速費用輸入**。
3. 選取費用的類別。 您會看到已載入至應用程式供離線使用的費用類別清單。 預設會載入 50 個項目，但是開發人員可以變更此數目。 如需詳細資訊，開發人員應參閱[平台行動](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)。 如果您的類別不在清單中，請選取 **搜尋** 進行線上搜尋。 依費用類別搜尋，或切換為依費用類型進行搜尋。
4. 輸入費用的交易日期。
5. 選擇性：輸入費用的商家。
6. 輸入費用的金額。
7. 選取費用的貨幣。 您會看到已載入至應用程式供離線使用的貨幣代碼清單。 預設會載入 400 種貨幣，但是開發人員可以變更此數目。 如需詳細資訊，開發人員應參閱[平台行動](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)。 如果您的貨幣不在清單中，請選取 **搜尋** 進行線上搜尋。 依貨幣搜尋，或切換為依名稱進行搜尋。
8. 選取 **拍攝相片** 或 **選擇影像**。
9. 依照下列其中一個驟操作︰

    - 如果選取了 **拍攝相片**，您會進入行動裝置上的相機，以便拍攝收據的相片。 完成拍照後，選取 **確定** 以接受相片。
    - 如果選取了 **選擇影像**，請選取清單中的影像。

10. 選取 **完成**。

## <a name="approve-an-expense-report-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>使用費用管理行動工作區核准費用報表 (如果您使用 2017 年 7 月更新)
1. 在行動裝置上，開啟 **費用管理** 工作區。
2. **費用核准** 會顯示指派給您進行核准的費用報表數目。 此數目約每隔 30 分鐘更新一次。 選取 **費用核准**。

    隨即顯示指派給您進行核准的費用報表清單。
    
3. 選取費用報表以檢視其費用詳細資料。
4. 選取費用以檢視其詳細資料。 費用顯示的資訊包括任何收據、來賓和逐條列舉項目詳細資料。
5. 回到 **費用報表** 頁面，選取以核准或拒絕費用報表。
6. 輸入任何關於核准動作的意見。
7. 選取 **完成**。

## <a name="create-a-new-expense-report-and-submit-it-for-approval-by-using-the-expense-management-mobile-workspace-if-you-use-the-july-2017-update"></a>使用費用管理行動工作區 (如果您使用 2017 年 7 月更新)，建立新的費用報表並提交報表請求核准
1. 在行動裝置上，開啟 **費用管理** 工作區。
2. 選取 **費用輸入**。
3. 選取 **新增報表**，或選取清單中現有的費用報表。
4. 新增費用報表時，輸入用途以及任何其他可用的資訊。 這項資訊根據您的公司設定費用管理的方式而有所不同。
5. 選取 **完成**。
6. 若要將現有費用 (例如信用卡交易) 新增至費用報表，請選取 **附加**。
7. 選取清單中的一項或多項費用。
8. 選取 **完成**。
9. 若要將新費用新增至費用報表，請選取 **新增費用**。
10. 選取費用的類別。 您會看到已載入至應用程式供離線使用的費用類別清單。 預設會載入 50 個項目，但是開發人員可以變更此數目。 如需詳細資訊，開發人員應參閱[平台行動](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)。 如果您的類別不在清單中，請選取 **搜尋** 進行線上搜尋。 依費用類別搜尋，或切換為依費用類型進行搜尋。
11. 選擇性：輸入費用的商家。
12. 輸入費用的交易日期。
13. 輸入費用的金額。
14. 選取費用的貨幣。 您會看到已載入至應用程式供離線使用的貨幣代碼清單。 預設會載入 400 種貨幣，但是開發人員可以變更此數目。 如需詳細資訊，開發人員應參閱[平台行動](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)。 如果您的貨幣不在清單中，請選取 **搜尋** 進行線上搜尋。 依貨幣搜尋，或切換為依名稱進行搜尋。
15. 選取 **完成**。
16. 若要將更多詳細資料新增至費用，請選取 **新增更多詳細資料**。 可用的欄位取決於公司的費用管理設定。
17. 如果公司原則需要費用的收據，請選取 **收據**，然後執行下列步驟：

    1. 選取 **擷取收據** 或 **附加收據**。
    2. 依照下列其中一個驟操作︰

        - 如果選取了 **擷取收據**，請執行下列步驟：

            1. 選取 **拍攝相片** 或 **選擇影像**。
            2. 依照下列其中一個驟操作︰

                - 如果選取了 **拍攝相片**，請執行下列步驟：

                    1. 您會進入行動裝置上的相機，以便拍攝收據的相片。 完成拍照後，選取 **確定** 以接受相片。
                    2. 選擇性：輸入相片的名稱，然後輸入任何附註。

                - 如果選取了 **選擇影像**，請執行下列步驟：

                    1. 選取清單中的影像。
                    2. 選擇性：輸入影像的名稱，然後輸入任何附註。

            3.  選取 **完成**。

        - 如果選取了 **附加收據**，請執行下列步驟：

            1.  選取清單中的一個或多個影像。
            2.  選取 **完成**。

    3. 選取 **返回** 按鈕回到費用詳細資料。

18. 如果公司原則需要費用支出所接待的來賓，請選取 **來賓**，然後執行下列步驟：

    1. 選取 **來賓**、**先前來賓** 或 **同事**。
    2. 依照下列其中一個驟操作︰

        - 如果選取了 **來賓**，請執行下列步驟：

            1. 輸入來賓的姓名。
            2. 選擇性：輸入來賓的組織和/或國家/地區。
            3. 輸入來賓的職稱。
            4. 選取 **完成**。

        - 如果選取了 **先前來賓**，請執行下列步驟：

            1. 選取清單中的一個或多個先前來賓。 您會看到已載入至應用程式供離線使用的先前來賓清單 (這些來賓已新增至先前的費用報表)。 預設會載入 50 個項目，但是開發人員可以變更此數目。 如需詳細資訊，開發人員應參閱[平台行動](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)。 如果您的先前來賓不在清單中，請選取 **搜尋** 進行線上搜尋。 依姓名搜尋，或切換為依組織、國家/地區或職稱進行搜尋。
            2. 選取 **完成**。

        - 如果選取了 **同事**，請執行下列步驟：

            1. 選取清單中的一個或多個同事。 您會看到已載入至應用程式供離線使用的同事清單。 預設會載入 50 個項目，但是開發人員可以變更此數目。 如需詳細資訊，開發人員應參閱[平台行動](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)。 如果您的同事不在清單中，請選取 **搜尋** 進行線上搜尋。 依姓名搜尋，或切換為依公司或職稱進行搜尋。
            2. 選取 **完成**。

    3. 選取 **返回** 按鈕回到費用詳細資料。

19. 如果公司原則需要逐條列舉費用，請選取 **逐條列舉**，然後執行下列步驟：

    1. 選取要逐條列舉的第一個日期。
    2. 選取 **新增逐條列舉項目**。
    3. 選取費用逐條列舉項目的子類別。 您會看到已載入至應用程式供離線使用的費用子類別清單。 預設會載入 50 個項目，但是開發人員可以變更此數目。 如需詳細資訊，開發人員應參閱[平台行動](/dynamics365/fin-ops-core/dev-itpro/mobile-apps/platform/mobile-platform-home-page)。 如果您的子類別不在清單中，請選取 **搜尋** 進行線上搜尋。 依費用子類別名稱進行搜尋。
    4. 輸入逐條列舉項目的交易金額。
    5. 若有必要，請編輯交易日期。
    6. 選取 **完成**。
    7. 重複上述步驟，直到您將所選日期的所有逐條列舉項目新增完畢為止。
    8. 還有其他日期時，您可以選取 **複製到下一天**，將逐條列舉項目複製到下一天。 或者，也可以選取要逐條列舉的日期，然後依照對第一個日期進行逐條列舉的方式，新增逐條列舉項目。
    9. 完成費用的逐條列舉之後，選取 **返回** 按鈕回到費用詳細資料。

20. 選取 **返回** 按鈕回到 **費用報表** 頁面。
21. 重複上述步驟，直到將所有費用新增完畢為止。
22. 選取 **送出**。
23. 輸入任何關於核准者的意見。
24. 選取 **完成**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]