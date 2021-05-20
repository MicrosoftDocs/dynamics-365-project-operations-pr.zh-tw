---
title: 使用複製專案來開發專案範本
description: 本主題提供有關如何使用 [複製專案] 自訂動作建立專案範本的資訊。
author: stsporen
manager: Annbe
ms.date: 01/21/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: cc17df0c73b276048f7c4b04bd9dc6644e828dc0
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5949804"
---
# <a name="develop-project-templates-with-copy-project"></a>使用複製專案來開發專案範本

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Dynamics 365 Project Operations 支援複製專案，並將任何指派回復為代表角色之一般資源的能力。 客戶可以使用此功能來建立基本專案範本。

選取 **複製專案** 時，目標專案的狀態會更新。 使用 **狀態原因** 來判斷複製動作何時完成。 選取 **複製專案** 時，如果在目標專案實體中偵測不到目標日期，也會將專案的開始日期更新為目前的開始日期。

## <a name="copy-project-custom-action"></a>複製專案自訂動作 

### <a name="name"></a>名稱 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>輸入參數
有三個輸入參數：

| 參數          | 鍵入   | 值                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** 或 **{"clearTeamsAndAssignments":true}** |
| SourceProject      | 實體參考 | 來源專案 |
| 目標             | 實體參考 | 目標專案 |


- **{"clearTeamsAndAssignments":true}**：Project 網頁版的預設行為，並將移除所有指派和團隊成員。
- **{"removeNamedResources":true}**：Project Operations 的預設行為，並將指派還原為一般資源。

如需更多有關動作的預設行為，請參閱[使用 Web API 動作](/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>指定要複製的欄位 
呼叫動作時，**複製專案** 會查看專案檢視表 **複製專案欄**，以判斷要在複製專案時複製哪些欄位。


### <a name="example"></a>範例
下列範例顯示如何使用已設定的 **removeNamedResources** 參數來呼叫 **CopyProject** 自訂動作。
```C#
{
    using System;
    using System.Runtime.Serialization;
    using Microsoft.Xrm.Sdk;
    using Newtonsoft.Json;

    [DataContract]
    public class ProjectCopyOption
    {
        /// <summary>
        /// Clear teams and assignments.
        /// </summary>
        [DataMember(Name = "clearTeamsAndAssignments")]
        public bool ClearTeamsAndAssignments { get; set; }

        /// <summary>
        /// Replace named resource with generic resource.
        /// </summary>
        [DataMember(Name = "removeNamedResources")]
        public bool ReplaceNamedResources { get; set; }
    }

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
            targetProject["msdyn_subject"] = "Example Project";
            targetProject.Id = organizationService.Create(targetProject);

            ProjectCopyOption copyOption = new ProjectCopyOption();
            copyOption.ReplaceNamedResources = true;

            CallCopyProjectAPI(sourceProject.ToEntityReference(), targetProject.ToEntityReference(), copyOption);
            Console.WriteLine("Done ...");
        }

        private void CallCopyProjectAPI(EntityReference sourceProject, EntityReference TargetProject, ProjectCopyOption projectCopyOption)
        {
            OrganizationRequest req = new OrganizationRequest("msdyn_CopyProjectV2");
            req["SourceProject"] = sourceProject;
            req["Target"] = TargetProject;
            req["ProjectCopyOption"] = JsonConvert.SerializeObject(projectCopyOption);
            OrganizationResponse response = organizationService.Execute(req);
        }
    }
}
```


[!INCLUDE[footer-include](../includes/footer-banner.md)]