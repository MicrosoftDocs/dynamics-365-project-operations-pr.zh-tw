---
title: 使用專案排程 API 與 Power Automate
description: 本文提供使用專案排程應用程式開發介面 (API) 的範例流程。
author: ruhercul
ms.date: 01/26/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 2527375ff3f3d631f3bb3de1458abb3b8838db54
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8916324"
---
# <a name="use-project-schedule-apis-with-power-automate"></a>使用專案排程 API 與 Power Automate

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

本文說明的範例流程示範使用 Microsoft Power Automate 建立完整專案計劃、建立作業集和更新實體的方法。 此範例示範如何建立專案、專案團隊成員、作業集、專案工作和資源指派。 本文還會說明如何更新實體以及執行作業集。

以下是在本文範例流程中所記載步驟的完整清單：

1. [建立PowerApps  觸發程式](#1)
2. [建立專案](#2)
3. [初始化團隊成員的變數](#3)
4. [建立一般團隊成員](#4)
5. [建立作業集](#5)
6. [建立專案貯體](#6)
7. [初始化連結狀態的變數](#7)
8. [初始化工作數目的變數](#8)
9. [初始化專案工作識別碼的變數](#9)
10. [執行直到](#10)
11. [設定專案工作](#11)
12. [建立專案工作](#12)
13. [建立資源指派](#13)
14. [遞減變數](#14)
15. [重新命名專案工作](#15)
16. [執行作業集](#16)

## <a name="assumptions"></a>假設

本文假設您具備 Dataverse 平台、雲端流程及專案排程應用程式開發介面 (API) 的基本知識。 如需詳細資訊，請參閱本文稍後的[參考資料](#references)。

## <a name="create-a-flow"></a>建立流程

### <a name="select-an-environment"></a>選取環境

您可以在環境中建立 Power Automate 流程。

1. 前往 <https://flow.microsoft.com>，並使用系統管理員認證登入。
2. 在右上角選取 **環境**。
3. 在清單中，選取已安裝 Dynamics 365 Project Operations 的環境 。

### <a name="create-a-solution"></a>建立解決方案

依照這些步驟建立[解決方案感知流程](/power-automate/overview-solution-flows)。 您可以建立有解決方案感知流程，更輕鬆地匯出流程以供日後使用。

1. 在導覽窗格中，選取 **解決方案**。
2. 在 **解決方案** 頁面上，選取 **新增解決方案**。
3. 在 **新增解決方案** 對話方塊中，設定必要的欄位，然後選取 **建立**。

## <a name="step-1-create-a-powerapps-trigger"></a><a id="1"></a>步驟 1：建立 PowerApps 觸發程序

1. 在 **解決方案** 頁面上，選取您所建立的解決方案，然後選取 **新增**。
2. 在左窗格中，選取 **雲端流程** \> **自動化** \> **雲端流程** \> **即時**。
3. 在 **流程名稱** 欄位中，輸入 **排程 API 示範流程**。
4. 在 **選擇觸發此流程的方式** 清單中，選取 **Power Apps**。 建立 Power Apps 觸發程序時，邏輯取決於身為作者的您。 在本文中，讓輸入參數保持空白以進行測試。
5. 選取 **建立**。

## <a name="step-2-create-a-project"></a><a id="2"></a>步驟 2：建立專案

依照下列步驟建立建立範例專案。

1. 在您建立的流程中，選取 **新增步驟**。

    ![新增新步驟](media/newstep.png)

2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **執行未繫結動作**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。

    ![選取作業。](media/chooseactiontab.png)

3. 在新的步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。

![重新命名步驟。](media/renamestep.png)

4. 將步驟重新命名為 **建立專案**。
5. 在 **動作名稱** 欄位中，選取 **msdyn\_CreateProjectV1**。
6. 在 **msdyn\_subject** 欄位底下，選取 **新增動態內容**。
7. 在 **運算式** 索引標籤的函數欄位中，輸 **專案名稱 - utcNow()**。
8. 選取 **確定**。

## <a name="step-3-initialize-a-variable-for-the-team-member"></a><a id="3"></a>步驟 3：初始化團隊成員的變數

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **初始化變數**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在新的步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **初始化團隊成員**。
5. 在 **名稱** 欄位中，輸入 **TeamMemberAction**。
6. 在 **類型** 欄位中，選取 **字串**。
7. 在 **值** 欄位中，輸入 **msdyn\_CreateTeamMemberV1**。

## <a name="step-4-create-a-generic-team-member"></a><a id="4"></a>步驟 4：建立一般團隊成員

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **執行未繫結動作**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在新的步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **建立團隊成員**。
5. 在 **動作名稱** 欄位的 **動態內容** 對話方塊中，選取 **TeamMemberAction**。
6. 在 **動作參數** 欄位中，輸入下列參數資訊。

    ```
    {
        "TeamMember": {
            "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projectteam",
            "msdyn_projectteamid": "@{guid()}",
            "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
            "msdyn_name": "ScheduleAPIDemoTM1"
        }
    } 
    ```

    以下是這些參數的說明：

    - **\@\@odata.type** – 實體名稱。 例如，輸入 **"Microsoft.Dynamics.CRM.msdyn\_projectteam"**。
    - **msdyn\_projectteamid** – 專案團隊識別碼的主索引鍵。 此值是全域唯一識別碼 (GUID) 運算式。   此識別碼是從運算式索引標籤中產生。

    - **msdyn\_project\@odata.bind** – 所屬專案的專案識別碼。 此值會是來自「建立專案」步驟回應中的動態內容。 確定您已輸入完整路徑，並在括弧之間加入動態內容。 需要引號。 例如，輸入 **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**。
    - **msdyn\_name** – 團隊成員的名稱。 例如，輸入 **"ScheduleAPIDemoTM1"**。

## <a name="step-5-create-an-operation-set"></a><a id="5"></a>步驟 5：建立作業集

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **執行未繫結動作**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在新的步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **建立作業集**。
5. 在 **動作名稱** 欄位中，選取 **msdyn\_CreateOperationSetV1** Dataverse 自訂動作。
6. 在 **描述** 欄位中，輸入 **ScheduleAPIDemoOperationSet**。
7. 在 **專案** 欄位中，輸入 **/msdyn\_projects(**。
8. 在 **動態內容** 對話方塊中，選取 **msdyn\_CreateProjectV1Response ProjectId**。
9. 在 **專案** 欄位中，輸入 **)**。

## <a name="step-6-create-a-project-bucket"></a><a id="6"></a>步驟 6：建立專案貯體

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **新增資料列**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在新的步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **建立貯體**。
5. 在 **資料表名稱** 欄位中，選取 **專案貯體**。
6. 在 **名稱** 欄位中，輸入 **ScheduleAPIDemoBucket1**。
7. 對於 **專案** 欄位，選取 **動態內容** 對話方塊中的 **msdyn\_CreateProjectV1Response ProjectId**。

## <a name="step-7-initialize-a-variable-for-the-link-status"></a><a id="7"></a>步驟 7：初始化連結狀態的變數

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **初始化變數**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在新的步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **初始化連結狀態**。
5. 在 **名稱** 欄位中，輸入 **linkstatus**。
6. 在 **類型** 欄位中，選取 **整數**。
7. 在 **值** 欄位中，輸入 **192350000**。

## <a name="step-8-initialize-a-variable-for-the-number-of-tasks"></a><a id="8"></a>步驟 8：初始化工作數目的變數

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **初始化變數**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在新的步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **初始化工作數目**。
5. 在 **名稱** 欄位中，輸入 **工作數目**。
6. 在 **類型** 欄位中，選取 **整數**。
7. 在 **值** 欄位中，輸入 **5**。

## <a name="step-9-initialize-a-variable-for-the-project-task-id"></a><a id="9"></a>步驟 9：初始化專案工作識別碼的變數

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **初始化變數**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在新的步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **Init ProjectTaskID**。
5. 在 **名稱** 欄位中，輸入 **工作數目**。
6. 在 **類型** 欄位中，選取 **字串**。
7. 在 **值** 欄位的運算式產生器中，輸入 **guid()**。

## <a name="step-10-do-until"></a><a id="10"></a>步驟 10：執行直到

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **執行直到**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 將條件陳述式中的第一個值設定為 **動態內容** 對話方塊中的 **工作數目** 變數。
4. 將條件設定為 **小於等於**。
5. 將條件陳述式中的第二個值設定為 **0**。

## <a name="step-11-set-a-project-task"></a><a id="11"></a>步驟 11：設定專案工作

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **設定變數**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在新的步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **設定專案工作**。
5. 在 **名稱** 欄位中，選取 **msdyn\_projecttaskid**。
6. 在 **值** 欄位的運算式產生器中，輸入 **guid()**。

## <a name="step-12-create-a-project-task"></a><a id="12"></a>步驟 12：建立專案工作

依照下列步驟，建立具有唯一識別碼且屬於目前專案及您所建立專案貯體的專案工作。

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **執行未繫結動作**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **建立專案工作**。
5. 在 **動作名稱** 欄位中，選取 **msdyn\_PssCreateV1**。
6. 在 **實體** 欄位中，輸入下列參數資訊。

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_project@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})",
        "msdyn_subject": "ScheduleAPIDemoTask1",
        "msdyn_projectbucket@odata.bind": "/msdyn_projectbuckets(@{outputs('Create_Project_Buckets')?['body/msdyn_projectbucketid']})",
        "msdyn_start": "@{addDays(utcNow(), 1)}",
        "msdyn_scheduledstart": "@{utcNow()}",
        "msdyn_scheduledend": "@{addDays(utcNow(), 5)}",
        "msdyn_LinkStatus": "192350000"
    }
    ```

    以下是這些參數的說明：

    - **\@\@odata.type** – 實體名稱。 例如，輸入 **"Microsoft.Dynamics.CRM.msdyn\_projecttask"**。
    - **msdyn\_projecttaskid** – 工作的唯一識別碼。 此值應設定為 **msdyn\_projecttaskid** 中的動態變數。
    - **msdyn\_project\@odata.bind** – 所屬專案的專案識別碼。 此值會是來自「建立專案」步驟回應中的動態內容。 確定您已輸入完整路徑，並在括弧之間加入動態內容。 需要引號。 例如，輸入 **"/msdyn\_projects(ADD DYNAMIC CONTENT)"**。
    - **msdyn\_subject** – 任何工作名稱。
    - **msdyn\_projectbucket\@odata.bind** – 包含工作的專案貯體。 此值會是來自「建立貯體」步驟回應中的動態內容。 確定您已輸入完整路徑，並在括弧之間加入動態內容。 需要引號。 例如，輸入 **"/msdyn\_projectbuckets(ADD DYNAMIC CONTENT)"**。
    - **msdyn\_start** – 開始日期的動態內容。 例如，明天會表示為 **"addDays(utcNow(), 1)"**。
    - **msdyn\_scheduledstart** – 排定的開始日期。 例如，明天會表示為 **"addDays(utcNow(), 1)"**。
    - **msdyn\_scheduleend** – 排定的結束日期。 選取未來的日期。 例如，指定 **"addDays(utcNow(), 5)"**。
    - **msdyn\_LinkStatus** – 連結狀態。 例如，輸入 **"192350000"**。

7. 對於 **OperationSetId** 欄位，選取 **動態內容** 對話方塊中的 **msdyn\_CreateOperationSetV1Response**。

## <a name="step-13-create-a-resource-assignment"></a><a id="13"></a>步驟 13：建立資源指派

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **執行未繫結動作**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **建立指派**。
5. 在 **動作名稱** 欄位中，選取 **msdyn\_PssCreateV1**。
6. 在 **實體** 欄位中，輸入下列參數資訊。

    ```
    {
        "@odata.type": "Microsoft.Dynamics.CRM.msdyn_resourceassignment",
        "msdyn_resourceassignmentid": "@{guid()}",
        "msdyn_name": "ScheduleAPIDemoAssign1",
        "msdyn_taskid@odata.bind": "/msdyn_projecttasks(@{variables('msdyn_projecttaskid')})",
        "msdyn_projectteamid@odata.bind": "/msdyn_projectteams(@{outputs('Create_Team_Member')?['body/TeamMemberId']})",
        "msdyn_projectid@odata.bind": "/msdyn_projects(@{outputs('Create_Project')?['body/ProjectId']})"
    }
    ```

7. 對於 **OperationSetId** 欄位，選取 **動態內容** 對話方塊中的 **msdyn\_CreateOperationSetV1Response**。

## <a name="step-14-decrement-a-variable"></a><a id="14"></a>步驟 14：遞減變數

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **遞減變數**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在 **名稱** 欄位中，選取 **工作數目**。
4. 在 **值** 欄位中，輸入 **1**。

## <a name="step-15-rename-a-project-task"></a><a id="15"></a>步驟 15：重新命名專案工作

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **執行未繫結動作**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **重新命名專案工作**。
5. 在 **動作名稱** 欄位中，選取 **msdyn\_PssUpdateV1**。
6. 在 **實體** 欄位中，輸入下列參數資訊。

    ```
    {
        "@@odata.type": "Microsoft.Dynamics.CRM.msdyn_projecttask",
        "msdyn_projecttaskid": "@{variables('msdyn_projecttaskid')}",
        "msdyn_subject": "ScheduleDemoTask1-UpdatedName"
    }
    ```

7. 對於 **OperationSetId** 欄位，選取 **動態內容** 對話方塊中的 **msdyn\_CreateOperationSetV1Response**。

## <a name="step-16-run-an-operation-set"></a><a id="16"></a>步驟 16：執行作業集

1. 在流程中，選取 **新增步驟**。
2. 在 **選擇作業** 對話方塊的搜尋欄位中，輸入 **執行未繫結動作**。 然後，在 **動作** 索引標籤上，選取結果清單中的作業。
3. 在步驟中，選取省略符號 (**...**)，然後選取 **重新命名**。
4. 將步驟重新命名為 **執行作業集**。
5. 在 **動作名稱** 欄位中，選取 **msdyn\_ExecuteOperationSetV1**。
6. 對於 **OperationSetId** 欄位，選取 **動態內容** 對話方塊中的 **msdyn\_CreateOperationSetV1Response OperationSetId**。

## <a name="references"></a>推薦人

- [如何將流程與 Dataverse 整合的概觀 - Power Automate](/power-automate/dataverse/overview?WT.mc_id=email)
- [使用專案排程 API 以對排程實體執行作業](schedule-api-preview.md)
- [雲端流程概觀 - Power Automate](/power-automate/overview-cloud?WT.mc_id=email)
- [解決方案感知流程概觀 - Power Automate](/power-automate/overview-solution-flows?WT.mc_id=email)
