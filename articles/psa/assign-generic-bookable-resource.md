---
title: 指派一般可預約資源至工作與專案團隊
description: 這主題提供有關為工作與專案團隊預約一般資源的資訊。
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 12/11/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: ca0999ae5413d824dd1384fe2262e5226695a5f8
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073011"
---
# <a name="assign-generic-bookable-resources-to-a-task-and-generate-resource-requirements"></a><span data-ttu-id="8976a-103">指派一般可預約資源至工作，並產生資源需求</span><span class="sxs-lookup"><span data-stu-id="8976a-103">Assign generic bookable resources to a task and generate resource requirements</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="8976a-104">除了預約和指派具名或實際的資源給專案之外，您還可以將一般資源指派至專案工作。</span><span class="sxs-lookup"><span data-stu-id="8976a-104">In addition to booking and assigning named or real resources to your project, you can assign generic resources to project tasks.</span></span> <span data-ttu-id="8976a-105">在您準備好以具名資源來為專案配置人員之前，這些資源可以做為具名資源的預留位置。</span><span class="sxs-lookup"><span data-stu-id="8976a-105">These resources can serve as placeholders for named resources until you are ready to staff your project with named resources.</span></span> 

1. <span data-ttu-id="8976a-106">在 Project Service Automation (PSA) 中，開啟 **專案** 頁面，然後移至 **排程** 索引標籤，在排程的 **資源** 儲存格中輸入一般資源的職位名稱。</span><span class="sxs-lookup"><span data-stu-id="8976a-106">In Project Service Automation (PSA), open the **Project** page and on the **Schedule** tab, enter the position name of the generic resource in the **Resource** cell of the schedule.</span></span> <span data-ttu-id="8976a-107">或者，按一下儲存格中的 **資源** 圖示以開啟資源選擇器，然後輸入您要建立的一般資源的名稱。</span><span class="sxs-lookup"><span data-stu-id="8976a-107">Or, click the **Resource** icon in the cell to open the resource picker and then enter the name of the generic resource that you want to create.</span></span>

![建立和指派一般團隊成員](media/RM-how-to-9.png)

<span data-ttu-id="8976a-109">這會開啟 **快速建立：專案團隊成員** 面板。</span><span class="sxs-lookup"><span data-stu-id="8976a-109">This will open the **Quick Create: Project Team Member** panel.</span></span> 

2. <span data-ttu-id="8976a-110">輸入一般資源團隊成員的角色與組織單位，然後按一下 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="8976a-110">Enter the role and organization unit of the generic resource team member and then click **Save**.</span></span>

![一般團隊成員快速建立](media/RM-how-to-10.png)

3. <span data-ttu-id="8976a-112">建立新的一般資源團隊成員之後，便會將其指派給工作。</span><span class="sxs-lookup"><span data-stu-id="8976a-112">After you have created the new generic resource team member, it is assigned to the task.</span></span> <span data-ttu-id="8976a-113">您可以繼續將該一般資源指派給工作排程中的其他工作。</span><span class="sxs-lookup"><span data-stu-id="8976a-113">You can continue to assign that generic resource to other tasks in the task schedule.</span></span>

![將現有的一般團隊成員指派給工作](media/RM-how-to-11.png)

4. <span data-ttu-id="8976a-115">指派了一般資源之後，即可產生資源需求，並透過直接將資源要求預約或送出給資源管理員來履行該需求。</span><span class="sxs-lookup"><span data-stu-id="8976a-115">After you have assigned the generic resource, you can generate a resource requirement and fulfill it by directly booking or submitting a resource request to a resource manager.</span></span>

![產生一般團隊成員的需求](media/RM-how-to-12.png)

<span data-ttu-id="8976a-117">在團隊成員網格中，除了可以使用上述資源選擇器之外，還可以直接新增一般資源。</span><span class="sxs-lookup"><span data-stu-id="8976a-117">On the team member grid, in addition to being able to use the resource picker as mentioned above, you can add generic resources directly.</span></span> <span data-ttu-id="8976a-118">資源會因為根據 **快速建立：專案團隊成員** 面板所指定開始/結束日期與配置方法所產生的資源需求而新增。</span><span class="sxs-lookup"><span data-stu-id="8976a-118">The resources are added with a resource requirement that is based on the start/end dates and allocation method specified in the **Quick Create: Project Team Member** panel.</span></span>

<span data-ttu-id="8976a-119">如果直接新增一般團隊成員，然後將更多工作指派給一般資源，超過這些工作所獲必須要時數所能支援的範圍時，您就可以看出差異。</span><span class="sxs-lookup"><span data-stu-id="8976a-119">You can see a difference if you add the generic team member directly and then assign more tasks to the generic resource than they have required hours to cover.</span></span> <span data-ttu-id="8976a-120">按一下 **產生需求** ，重新產生需求以平衡工作指派所需的時數。</span><span class="sxs-lookup"><span data-stu-id="8976a-120">Click **Generate Requirement** to regenerate the requirement to balance the required hours against assignments.</span></span>

<span data-ttu-id="8976a-121">您也可以按一下團隊網格中的 **資源需求** 連結，以開啟需求並新增技能、偏好資源等。</span><span class="sxs-lookup"><span data-stu-id="8976a-121">You can also click the **Resource requirement** link in the team grid to open the requirement and add skills, preferred resources, etc.</span></span>

![資源需求](media/RM-how-to-13.png)

