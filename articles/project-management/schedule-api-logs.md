---
title: 專案排程記錄
description: 本文提供的資訊與範例，可協助您使用專案排程記錄來追蹤與專案排程服務及專案排程 API 相關的失敗。
author: ruhercul
ms.date: 11/30/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: c57419642e90e4def01f2cd2474c9e82dc162b86
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923685"
---
# <a name="project-scheduling-logs"></a>專案排程記錄

_**適用於：** 資源/非庫存型案例適用的 Project Operations 精簡部署 - 交易至開立預估發票_、_Project for the Web_

Microsoft Dynamics 365 Project Operations 使用 [Project for the Web](https://support.microsoft.com/office/what-is-project-for-the-web-c19b2421-3c9d-4037-97c6-f66b6e1d2eb5) 做為主要排程引擎。 Project Operations 不使用標準 Microsoft Dataverse Web 應用程式開發介面 (API)，而是使用新的專案排程 API 來建立、更新和刪除專案工作、資源指派、工作相依性、專案貯體和專案團隊成員。 不過，以程式設計方式對分工結構圖 (WBS) 實體執行建立、更新或刪除作業時，可能會發生錯誤。 為了追蹤這些錯誤和作業歷程記錄，我們已實作兩個新的系統管理記錄：**作業集** 和 **專案排程服務 (PSS)**。 若要存取這些記錄，請移至 **設定** \> **排程整合**。

下圖顯示專案排程記錄的資料模型。

![專案排程記錄的資料模型。](media/LOGDATAMODEL.jpg)

## <a name="operation-set-log"></a>作業集記錄

作業集會追蹤作業集的執行情形，該作業集會用來對專案、專案工作、資源指派、工作相依性、專案貯體和專案團隊成員，以批次方式執行一項或多項建立、更新或刪除作業。 **作業所處狀態** 欄位會顯示作業集的整體狀態。 作業集承載的詳細資料會擷取到相關的作業集詳細資料記錄中。

### <a name="operation-set"></a>作業集

下表顯示與 **作業集** 實體相關的欄位。

| SchemaName            | Description                                                                                                  | DisplayName            |
|-----------------------|--------------------------------------------------------------------------------------------------------------|------------------------|
| msdyn_completedon     | 作業集的完成或失敗日期/時間。                                                | CompletedOn            |
| msdyn_correlationid   | 要求的 **correlationId** 值。                                                                  | CorrelationId          |
| msdyn_description     | 作業集的描述。                                                                        | Description            |
| msdyn_executedon      | 記錄的執行日期/時間。                                                                       | 執行日期            |
| msdyn_operationsetId  | 實體執行個體的唯一識別碼。                                                                   | OperationSet           |
| msdyn_Project         | 與作業集相關的專案。                                                            | Project                |
| msdyn_projectid       | 要求的 **projectId** 值。                                                                      | ProjectId (已取代) |
| msdyn_projectName     | 不適用。                                                                                              | 不適用         |
| msdyn_PSSErrorLog     | 與作業集相關之專案排程服務錯誤記錄的唯一識別碼。 | PSS 錯誤記錄          |
| msdyn_PSSErrorLogName | 不適用。                                                                                              | 不適用         |
| msdyn_status          | 作業集的狀態。                                                                             | 執行狀態                 |
| msdyn_statusName      | 不適用。                                                                                              | 不適用         |
| msdyn_useraadid       | 此要求所屬使用者的 Azure Active Directory (Azure AD) 物件識別碼。                     | UserAADID              |

### <a name="operation-set-detail"></a>作業集詳細資料

下表顯示與 **作業集詳細資料** 實體相關的欄位。

| SchemaName                 | Description                                                                                 | DisplayName           |
|----------------------------|---------------------------------------------------------------------------------------------|-----------------------|
| msdyn_cdspayload           | 要求的序列化 Dataverse 欄位。                                            | CdsPayload            |
| msdyn_entityname           | 要求的實體名稱。                                                     | EntityName            |
| msdyn_httpverb             | 要求方法。                                                                         | HTTP 動詞命令 (已取代) |
| msdyn_httpverbName         | 不適用。                                                                             | 不適用        |
| msdyn_operationset         | 記錄所屬作業集的唯一識別碼。                      | OperationSet          |
| msdyn_operationsetdetailId | 實體執行個體的唯一識別碼。                                                  | OperationSet 詳細資料   |
| msdyn_operationsetName     | 不適用。                                                                             | 不適用        |
| msdyn_operationtype        | 作業集詳細資料的作業類型。                                             | OperationType         |
| msdyn_operationtypeName    | 不適用。                                                                             | 不適用        |
| msdyn_psspayload           | 要求的系列化專案排程服務欄位。                           | PssPayload            |
| msdyn_recordid             | 要求記錄的識別碼。                                                       | 記錄識別碼             |
| msdyn_requestnumber        | 自動產生的編號，可識別收到要求的順序。 | 要求編號        |

## <a name="project-scheduling-service-error-logs"></a>專案排程服務錯誤記錄

專案排程服務錯誤記錄會擷取專案排程服務嘗試 **儲存** 或 **開啟** 使用者時發生的失敗。 有三種支援的案例會產生這些記錄：

- 使用者起始的動作發生重大失敗 (例如，因缺少權限而無法建立指派)。
- 專案排程服務無法以程式設計方式對實體進行建立、更新、刪除，或執行任何其他串聯作業。
- 記錄無法開啟時 (例如，開啟專案時，或更新團隊成員的資訊時)，使用者遇到錯誤。

### <a name="project-scheduling-service-log"></a>專案排程服務記錄

下表顯示專案排程服務記錄中包含的欄位。

| SchemaName          | Description                                                                    | DisplayName    |
|---------------------|--------------------------------------------------------------------------------|----------------|
| msdyn_CallStack     | 例外狀況的呼叫堆疊。                                               | 呼叫堆疊     |
| msdyn_correlationid | 錯誤的相互關聯識別碼。                                               | CorrelationId  |
| msdyn_errorcode     | 用來儲存 Dataverse 錯誤碼或 HTTP 錯誤碼的欄位。 | 錯誤碼     |
| msdyn_HelpLink      | 公開說明文件的連結。                                       | 說明連結      |
| msdyn_log           | 專案排程服務中的記錄。                                   | 記錄            |
| msdyn_project       | 與錯誤記錄相關聯的專案。                             | Project        |
| msdyn_projectName   | 專案的名稱 (如果會保存作業集的承載的話)。 | 不適用 |
| msdyn_psserrorlogId | 實體執行個體的唯一識別碼。                                     | PSS 錯誤記錄  |
| msdyn_SessionId     | 專案工作階段識別碼。                                                        | 工作階段識別碼     |

## <a name="error-log-cleanup"></a>錯誤記錄清理

預設可以每隔 90 天清理專案排程服務錯誤記錄和作業集記錄一次。 任何超過 90 天的記錄都會遭刪除。 不過，系統管理員可以在 **專案參數** 頁面上變更 **msdyn_StateOperationSetAge** 欄位的值，來調整清理範圍，使其介於 1 到 120 天之間。 有數種變更此值的方法可供使用：

- 建立自訂頁面，並新增 **過時的作業集存留期間** 欄位，以自訂 **專案參數** 實體。
- 使用採用 [WebApi 軟體開發套件 (SDK)](/powerapps/developer/model-driven-apps/clientapi/reference/xrm-webapi/updaterecord) 的用戶端程式碼。
- 在模型導向應用程式中使用採用 Xrm SDK **updateRecord** 方法 (用戶端 API 參考) 的服務 SDK 程式碼。 Power Apps 包含 **updateRecord** 方法的描述以及支援的參數。

    ```C#
    Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter').then(function (response) {
        parameter = response.entities[0];
        var staleOperationValue = prompt("All records older than (x) days will be deleted, please enter X between 1 to 90 days", 1)
        var newData = {};
        newData.msdyn_projectparameterid = parameter.msdyn_projectparameterid;
        newData.msdyn_staleoperationsetage = parseInt(staleOperationValue);
        Xrm.WebApi.updateRecord("msdyn_projectparameter", parameter.msdyn_projectparameterid, newData).then(
            function success(result) {
                console.log("Project Parameter: Stale Operation Expiry is set to: " + newData.msdyn_staleoperationsetage);
                // perform operations on record update
                Xrm.WebApi.retrieveMultipleRecords('msdyn_projectparameter')
                .then(function (response2) { console.log("Confirmed Project Parameter: Stale Operation Expiry is set to: " + response2.entities[0].msdyn_staleoperationsetage) });
            },
            function (error) {
                console.log("Failed to Update Project Ednpoint with error: " + error.message);
            // handle error conditions
            }
        );
    });
    ```
