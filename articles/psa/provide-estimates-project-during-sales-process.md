---
title: 在銷售處理期間提供專案的工作估計值
description: 如何在 Project Service 的銷售處理期間提供專案的工作估計值
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: e9382127b2ce0b157d681fc77d67200ba9c5e59d
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147958"
---
# <a name="provide-work-estimates-for-a-project-during-the-sales-process-project-service"></a><span data-ttu-id="2ba9b-103">在銷售處理期間提供專案的工作估計值 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="2ba9b-103">Provide work estimates for a project during the sales process (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="2ba9b-104">在銷售處理期間，您可以使用報價明細從頭計算出銷售估計值。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-104">During the sales process, you can work out sales estimates from the ground up with quote lines.</span></span> [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] <span data-ttu-id="2ba9b-105">中的[!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]功能提供更科學且更決定性的方式擬訂銷售估計值，藉由在分工結構圖中細分工作項目和建立相關屬性的關聯供專案估計值使用。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-105">capabilities in [!INCLUDE[pn_dynamics_crm](../includes/pn-dynamics-crm.md)] provide a more scientific and deterministic way of coming up with sales estimates by breaking down work items and associating relevant attributes that contribute toward the estimates for the project in the work breakdown structure.</span></span>  
  
 <span data-ttu-id="2ba9b-106">當您成功銷售時，可以使用專案計劃中關聯的分工結構圖，視需要微調以順利完成您的專案。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-106">Once you win the sale, you can use the associated work breakdown structure in your project plan, refining it as necessary for successful completion of your project.</span></span>  
  
## <a name="link-a-project-to-a-quote-line"></a><span data-ttu-id="2ba9b-107">連結專案與報價明細</span><span class="sxs-lookup"><span data-stu-id="2ba9b-107">Link a project to a quote line</span></span>  
 <span data-ttu-id="2ba9b-108">建立專案為主的報價明細時，可以從報價明細建立新專案。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-108">When creating a project-based quote line, you can create a new project from the quote line.</span></span> <span data-ttu-id="2ba9b-109">然後可以使用專案範本，這些範本是組織常用的預先設定標準專案計劃和財務估計值，或者過去專案的專案計劃和估計值複本。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-109">You can then use project templates, which are either pre-configured standard project plans and financial estimates common to your organization, or a copy of a project plan and estimates from a past project.</span></span> <span data-ttu-id="2ba9b-110">當您建立專案時，選擇專案範本會提供微調專案規劃、估計值與角色需求的基礎。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-110">When you create a project, choosing a project template provides a basis to refine the project plan, estimates, and role requirements.</span></span> <span data-ttu-id="2ba9b-111">透過從報價建立自己的專案，專案會自動與報價明細建立關聯。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-111">By creating your project from the quote, the project is automatically associated with the quote line.</span></span>  
  
## <a name="project-estimate-components"></a><span data-ttu-id="2ba9b-112">專案估計元件</span><span class="sxs-lookup"><span data-stu-id="2ba9b-112">Project estimate components</span></span>  
 <span data-ttu-id="2ba9b-113">專案中的分工結構圖提供細分工作的方式，會維護工作階層，以及指派完成每項工作所需的努力估計值。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-113">The work breakdown structure in a project provides a way to break down work into tasks, maintain a hierarchy of tasks, and assign an estimate of effort required to complete each task.</span></span> <span data-ttu-id="2ba9b-114">您也可以將角色與工作建立關聯，以指出完成工作和排程所需的資源類型的估計值。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-114">You can also associate roles to a task to indicate an estimate of the type of resource required to complete a task and a schedule.</span></span>  
  
 <span data-ttu-id="2ba9b-115">分工結構圖可幫助您判斷工作量和排程估計值。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-115">The work breakdown structure helps you determine work effort and schedule estimates.</span></span> <span data-ttu-id="2ba9b-116">根據預設，專案會使用您先前定義的預設價目表。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-116">By default, the project uses default price lists that you defined earlier.</span></span> <span data-ttu-id="2ba9b-117">價目表中定義的成本和售價有助於判斷專案工作細項的財務估計值。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-117">The cost and sales prices defined in the price lists help determine financial estimates for the project’s work breakdown.</span></span>  
  
 <span data-ttu-id="2ba9b-118">如果您的專案與報價相關，而報價的價目表與預設不同，則報價的價目表會用於財務估計值。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-118">If your project is associated with a quote, and the quote has a different price list from the default, the quote’s price list is used for financial estimates.</span></span>  
  
## <a name="import-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="2ba9b-119">從專案將估計值匯入至報價</span><span class="sxs-lookup"><span data-stu-id="2ba9b-119">Import estimates from a project into a quote</span></span>  
 <span data-ttu-id="2ba9b-120">一旦專案中有專案估計值，就可以將這些估計值匯入報價明細中：</span><span class="sxs-lookup"><span data-stu-id="2ba9b-120">Once you have project estimates in the project, you can import these estimates into the quote line:</span></span>  
  
-   <span data-ttu-id="2ba9b-121">在 **報價明細詳細資料** 中，按一下 **從估計值匯入**。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-121">In **Quote Line Details**, click **Import from estimates**.</span></span> 

-   <span data-ttu-id="2ba9b-122">選取要匯入依交易類型、角色或分工結構圖節點層級摘要的專案估計值。</span><span class="sxs-lookup"><span data-stu-id="2ba9b-122">Select whether to import project estimates summarized by transaction type, role, or work breakdown structure node level.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="2ba9b-123">請參閱</span><span class="sxs-lookup"><span data-stu-id="2ba9b-123">See Also</span></span>  
 [<span data-ttu-id="2ba9b-124">專案經理指南</span><span class="sxs-lookup"><span data-stu-id="2ba9b-124">Project Manager Guide</span></span>](../psa/project-manager-guide.md)
