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
# <a name="develop-project-templates-with-copy-project"></a><span data-ttu-id="cec13-103">使用複製專案來開發專案範本</span><span class="sxs-lookup"><span data-stu-id="cec13-103">Develop project templates with Copy Project</span></span>

<span data-ttu-id="cec13-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="cec13-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="cec13-105">Dynamics 365 Project Operations 支援複製專案，並將任何指派回復為代表角色之一般資源的能力。</span><span class="sxs-lookup"><span data-stu-id="cec13-105">Dynamics 365 Project Operations supports the ability to copy a project and revert any assignments back to the generic resources that represent the role.</span></span> <span data-ttu-id="cec13-106">客戶可以使用此功能來建立基本專案範本。</span><span class="sxs-lookup"><span data-stu-id="cec13-106">Customers can use this functionality to build basic project templates.</span></span>

<span data-ttu-id="cec13-107">選取 **複製專案** 時，目標專案的狀態會更新。</span><span class="sxs-lookup"><span data-stu-id="cec13-107">When you select **Copy Project**, the status of the target project is updated.</span></span> <span data-ttu-id="cec13-108">使用 **狀態原因** 來判斷複製動作何時完成。</span><span class="sxs-lookup"><span data-stu-id="cec13-108">Use **Status Reason** to determine when the copy action is complete.</span></span> <span data-ttu-id="cec13-109">選取 **複製專案** 時，如果在目標專案實體中偵測不到目標日期，也會將專案的開始日期更新為目前的開始日期。</span><span class="sxs-lookup"><span data-stu-id="cec13-109">Selecting **Copy Project** also updates the start date of the project to the current start date if no target date is detected in the target project entity.</span></span>

## <a name="copy-project-custom-action"></a><span data-ttu-id="cec13-110">複製專案自訂動作</span><span class="sxs-lookup"><span data-stu-id="cec13-110">Copy Project custom action</span></span> 

### <a name="name"></a><span data-ttu-id="cec13-111">名稱</span><span class="sxs-lookup"><span data-stu-id="cec13-111">Name</span></span> 

<span data-ttu-id="cec13-112">**msdyn_CopyProjectV2**</span><span class="sxs-lookup"><span data-stu-id="cec13-112">**msdyn_CopyProjectV2**</span></span>

### <a name="input-parameters"></a><span data-ttu-id="cec13-113">輸入參數</span><span class="sxs-lookup"><span data-stu-id="cec13-113">Input parameters</span></span>
<span data-ttu-id="cec13-114">有三個輸入參數：</span><span class="sxs-lookup"><span data-stu-id="cec13-114">There are three input parameters:</span></span>

| <span data-ttu-id="cec13-115">參數</span><span class="sxs-lookup"><span data-stu-id="cec13-115">Parameter</span></span>          | <span data-ttu-id="cec13-116">鍵入</span><span class="sxs-lookup"><span data-stu-id="cec13-116">Type</span></span>   | <span data-ttu-id="cec13-117">值</span><span class="sxs-lookup"><span data-stu-id="cec13-117">Values</span></span>                                                   | 
|--------------------|--------|----------------------------------------------------------|
| <span data-ttu-id="cec13-118">ProjectCopyOption</span><span class="sxs-lookup"><span data-stu-id="cec13-118">ProjectCopyOption</span></span>  | <span data-ttu-id="cec13-119">String</span><span class="sxs-lookup"><span data-stu-id="cec13-119">String</span></span> | <span data-ttu-id="cec13-120">**{"removeNamedResources":true}** 或 **{"clearTeamsAndAssignments":true}**</span><span class="sxs-lookup"><span data-stu-id="cec13-120">**{"removeNamedResources":true}** or **{"clearTeamsAndAssignments":true}**</span></span> |
| <span data-ttu-id="cec13-121">SourceProject</span><span class="sxs-lookup"><span data-stu-id="cec13-121">SourceProject</span></span>      | <span data-ttu-id="cec13-122">實體參考</span><span class="sxs-lookup"><span data-stu-id="cec13-122">Entity Reference</span></span> | <span data-ttu-id="cec13-123">來源專案</span><span class="sxs-lookup"><span data-stu-id="cec13-123">Source Project</span></span> |
| <span data-ttu-id="cec13-124">目標</span><span class="sxs-lookup"><span data-stu-id="cec13-124">Target</span></span>             | <span data-ttu-id="cec13-125">實體參考</span><span class="sxs-lookup"><span data-stu-id="cec13-125">Entity Reference</span></span> | <span data-ttu-id="cec13-126">目標專案</span><span class="sxs-lookup"><span data-stu-id="cec13-126">Target Project</span></span> |


- <span data-ttu-id="cec13-127">**{"clearTeamsAndAssignments":true}**：Project 網頁版的預設行為，並將移除所有指派和團隊成員。</span><span class="sxs-lookup"><span data-stu-id="cec13-127">**{"clearTeamsAndAssignments":true}**: Thee default behavior for Project for the Web, and will remove all assignments and team members.</span></span>
- <span data-ttu-id="cec13-128">**{"removeNamedResources":true}**：Project Operations 的預設行為，並將指派還原為一般資源。</span><span class="sxs-lookup"><span data-stu-id="cec13-128">**{"removeNamedResources":true}** The default behavior for Project Operations, and will revert assignments to generic resources.</span></span>

<span data-ttu-id="cec13-129">如需更多有關動作的預設行為，請參閱[使用 Web API 動作](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span><span class="sxs-lookup"><span data-stu-id="cec13-129">For more defaults on actions, see [Use Web API actions](/powerapps/developer/common-data-service/webapi/use-web-api-actions)</span></span>

## <a name="specify-fields-to-copy"></a><span data-ttu-id="cec13-130">指定要複製的欄位</span><span class="sxs-lookup"><span data-stu-id="cec13-130">Specify fields to copy</span></span> 
<span data-ttu-id="cec13-131">呼叫動作時，**複製專案** 會查看專案檢視表 **複製專案欄**，以判斷要在複製專案時複製哪些欄位。</span><span class="sxs-lookup"><span data-stu-id="cec13-131">When the action is called, **Copy Project** will look at the project view **Copy Project Columns** to determine which fields to copy when the project is copied.</span></span>


### <a name="example"></a><span data-ttu-id="cec13-132">範例</span><span class="sxs-lookup"><span data-stu-id="cec13-132">Example</span></span>
<span data-ttu-id="cec13-133">下列範例顯示如何使用已設定的 **removeNamedResources** 參數來呼叫 **CopyProject** 自訂動作。</span><span class="sxs-lookup"><span data-stu-id="cec13-133">The following example shows how to call the **CopyProject** custom action with the **removeNamedResources** parameter set.</span></span>
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