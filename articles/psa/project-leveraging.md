---
title: 銷售估計和專案
description: 本主題提供有關如何利用銷售處理中的排程和估計的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
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
ms.openlocfilehash: d8bb380519759659dc1b4151b62228a626ee7a26
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120668"
---
# <a name="sales-estimates-and-projects"></a><span data-ttu-id="d018a-103">銷售估計和專案</span><span class="sxs-lookup"><span data-stu-id="d018a-103">Sales estimates and projects</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="d018a-104">在銷售處理期間，您可以將專案連結至銷售報價來建立銷售估計。</span><span class="sxs-lookup"><span data-stu-id="d018a-104">During the sales process, you can create sales estimates by linking a project to a sales quote.</span></span> <span data-ttu-id="d018a-105">如此一來，就能在銷售處理期間進行具有決定性的估計，以便利用專案排程和估計功能。</span><span class="sxs-lookup"><span data-stu-id="d018a-105">In this way, deterministic estimation can occur during the sales process, to take advantage of project scheduling and estimation capabilities.</span></span> <span data-ttu-id="d018a-106">如果銷售完成，用作銷售估計目的排程就可以用來做為進一步改善專案計劃的基礎。</span><span class="sxs-lookup"><span data-stu-id="d018a-106">If the sale goes through, the schedule that was used for sales estimation purposes can be used as the basis for further refinement of the project plan.</span></span>

## <a name="linking-a-project-to-a-quote-line"></a><span data-ttu-id="d018a-107">連結專案與報價明細</span><span class="sxs-lookup"><span data-stu-id="d018a-107">Linking a project to a quote line</span></span>

<span data-ttu-id="d018a-108">建立專案型報價明細時，您可以建立新專案，或是與 **報價明細** 頁面上的現有專案建立關聯。</span><span class="sxs-lookup"><span data-stu-id="d018a-108">When you create a project-based quote line, you can create a new project or associate an existing project pn the **Quote Line** page.</span></span> 

> ![報價明細表單](media/project-8.png)
 
<span data-ttu-id="d018a-110">從報價明細詳細資料建立新專案時，您可以利用專案範本。</span><span class="sxs-lookup"><span data-stu-id="d018a-110">When you create a new project from the quote line details, you can take advantage of project templates.</span></span> <span data-ttu-id="d018a-111">專案範本是表示組織中特具代表性之專案計劃與財務估計的模型專案。</span><span class="sxs-lookup"><span data-stu-id="d018a-111">Project templates are model projects that represent standard project plans and financial estimates that are typical in an organization.</span></span> <span data-ttu-id="d018a-112">這些範本也可能表示過去專案的專案計劃及估計複本。</span><span class="sxs-lookup"><span data-stu-id="d018a-112">They can also represent copies of project plans and estimates from past projects.</span></span>

> ![報價明細詳細資料](media/project-9.png)
  
<span data-ttu-id="d018a-114">從報價建立您的專案時，專案會自動與報價明細建立關聯。</span><span class="sxs-lookup"><span data-stu-id="d018a-114">When you create the project from the quote, the project is automatically associated with the quote line.</span></span>

## <a name="components-of-estimates-in-a-project"></a><span data-ttu-id="d018a-115">專案中的估計元件</span><span class="sxs-lookup"><span data-stu-id="d018a-115">Components of estimates in a project</span></span>

<span data-ttu-id="d018a-116">排程可讓您將作業分成工作、維持工作的階層、判斷完成工作所需的資源，以及指派完成工作所需投入努力的估計。</span><span class="sxs-lookup"><span data-stu-id="d018a-116">A schedule lets you divide work into tasks, maintain a hierarchy of tasks, determine what resources are required to complete a task, and assign an estimate of the effort that is required to complete a task.</span></span>

<span data-ttu-id="d018a-117">您可以使用 **專案** 頁面 **排程** 索引標籤上的欄位，來定義工作投入和排程估計。</span><span class="sxs-lookup"><span data-stu-id="d018a-117">You can define the work effort and schedule estimates by using the fields on the **Schedule** tab of the **Project** page.</span></span> <span data-ttu-id="d018a-118">由於價目表與專案相關聯，因此財務估計會使用價目表中定義的成本和銷售價格進行計算。</span><span class="sxs-lookup"><span data-stu-id="d018a-118">Because a price list is associated with the project, financial estimates are calculated by using cost and sales prices that are defined in the price list.</span></span>

## <a name="importing-estimates-from-a-project-into-a-quote"></a><span data-ttu-id="d018a-119">從專案將估計值匯入至報價</span><span class="sxs-lookup"><span data-stu-id="d018a-119">Importing estimates from a project into a quote</span></span>

<span data-ttu-id="d018a-120">定義專案估計值之後，您可以將這些值匯入至報價明細。</span><span class="sxs-lookup"><span data-stu-id="d018a-120">After you define project estimates, you can import them into the quote line.</span></span> <span data-ttu-id="d018a-121">在 **報價明細詳細資料** 頁面上，選取功能區上的 **從估計值匯入**，以依據交易類型、角色或工作層級來摘要專案估計值。</span><span class="sxs-lookup"><span data-stu-id="d018a-121">On the **Quote Line Details** page, select **Import from estimates** on the ribbon to summarize project estimates by transaction type, role, or task level.</span></span>
