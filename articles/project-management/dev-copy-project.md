---
title: 使用複製專案來開發專案範本
description: 本主題提供有關如何使用 [複製專案] 自訂動作建立專案範本的資訊。
author: stsporen
ms.date: 03/10/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 72aa2db7c717eeab85ada448c673bf702087baeb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8590888"
---
# <a name="develop-project-templates-with-copy-project"></a>使用複製專案來開發專案範本

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 支援複製專案，並將任何指派回復為代表角色之一般資源的能力。 客戶可以使用此功能來建立基本專案範本。

選取 **複製專案** 時，目標專案的狀態會更新。 使用 **狀態原因** 來判斷複製動作何時完成。 選取 **複製專案** 時，如果在目標專案實體中偵測不到目標日期，也會將專案的開始日期更新為目前的開始日期。

## <a name="copy-project-custom-action"></a>複製專案自訂動作

### <a name="name"></a>姓名 

msdyn\_CopyProjectV3

### <a name="input-parameters"></a>輸入參數

有三個輸入參數：

- **ReplaceNamedResources** 或 **ClearTeamsAndAssignments** – 僅設定其中一個選項。 不要同時設定兩者。

    - **\{"ReplaceNamedResources":true\}** – Project Operations 的預設行為。 任何具名資源都會取代為一般資源。
    - **\{"ClearTeamsAndAssignments":true\}** – Project for the Web 的預設行為。 所有指派和團隊成員都會遭移除。

- **SourceProject** – 要從中複製的來源專案的實體參考。 此參數不可為 Null。
- **Target** – 要複製到的目標專案的實體參考。 此參數不可為 Null。

下表提供這三個參數的摘要。

| 參數                | 類型​             | 數值                 |
|--------------------------|------------------|-----------------------|
| ReplaceNamedResources    | 布林值          | **True** 或 **False** |
| ClearTeamsAndAssignments | 布林值          | **True** 或 **False** |
| SourceProject            | 實體參考 | 來源專案    |
| Target                   | 實體參考 | 目標專案    |

如需更多有關動作的預設行為，請參閱[使用 Web API 動作](/powerapps/developer/common-data-service/webapi/use-web-api-actions)。

### <a name="validations"></a>驗證

下列驗證已完成。

1. Null 會檢查並擷取來源和目標專案，以確認這兩個專案都存在於組織中。
2. 系統會確認下列條件，以驗證目標專案是否適用於進行複製：

    - 先前沒有使用對專案進行的活動 (包括選取 **工作** 索引標籤)，而且專案是新建立的。
    - 先前沒有任何對此專案要求的複製或匯入，而且專案的狀態並非 **失敗**。

3. 作業不是使用 HTTP 進行呼叫。

## <a name="specify-fields-to-copy"></a>指定要複製的欄位

呼叫動作時，**複製專案** 會查看專案檢視表 **複製專案欄**，以判斷要在複製專案時複製哪些欄位。

### <a name="example"></a>範例

下列範例顯示如何設定 **removeNamedResources** 參數以呼叫 **CopyProjectV3** 自訂動作。

```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    public class CopyProjectSample
    {
        private IOrganizationService organizationService;

        public CopyProjectSample(IOrganizationService organizationService)
        {
            this.organizationService = organizationService;
        }

        public void SampleRun()
        {
            // Example source project GUID
            Guid sourceProjectId = new Guid("11111111-1111-1111-1111-111111111111");
            var sourceProject = new Entity("msdyn_project", sourceProjectId);

            Entity targetProject = new Entity("msdyn_project");
            targetProject["msdyn_subject"] = "Example Project - Copy";
            targetProject.Id = organizationService.Create(targetProject);

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption, true, false);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, bool replaceNamedResources = true, bool clearTeamsAndAssignments = false)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV3");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;

            if (replaceNamedResources)
            {
                req["ReplaceNamedResources"] = true;
            }
            else
            {
                req["ClearTeamsAndAssignments"] = true;
            }

            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```

[!INCLUDE[footer-include](../includes/footer-banner.md)]
