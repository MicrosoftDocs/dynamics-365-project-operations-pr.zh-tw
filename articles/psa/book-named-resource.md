---
title: 透過資源需求預約具名資源
description: 本主題提供有關為一般資源需求預約具名資源的資訊。
author: JohnPBurrows
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 50858d4fc55285b2e91117c6cbfb2419931b4197
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5291024"
---
# <a name="book-named-resources-from-resource-requirements"></a><span data-ttu-id="4f7b8-103">透過資源需求預約具名資源</span><span class="sxs-lookup"><span data-stu-id="4f7b8-103">Book named resources from resource requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="4f7b8-104">您可以預約具名資源，以取代有資源需求的一般資源。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-104">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="4f7b8-105">在 Project Service Automation (PSA) 的 **專案** 頁面上，按一下 **團隊** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-105">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab.</span></span>
2. <span data-ttu-id="4f7b8-106">從清單中選取具有資源需求的一般資源，然後按一下 **預約**。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-106">Select the generic resource that has a resource requirement from the list and then click **Book**.</span></span> <span data-ttu-id="4f7b8-107">或者，開啟資源需求，然後按一下 **預約**。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-107">Or, open the resource requirement and then click **Book**.</span></span>


![預約一般團隊成員](media/RM-how-to-14.png)


3. <span data-ttu-id="4f7b8-109">在 **排程小幫手** 頁面上，選取要預約到專案團隊的具名資源，然後按一下 **預約**。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then click **Book**.</span></span>

![使用排程小幫手預約一般團隊成員](media/RM-how-to-15.png)

<span data-ttu-id="4f7b8-111">預約由具名資源完成並履行後，將會以具名資源取代一般資源。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-111">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

![具名團隊成員取代一般團隊成員](media/RM-how-to-16.png)

<span data-ttu-id="4f7b8-113">排程上的指派也會以具名資源來更新。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-113">The assignments on the schedule are updated with the named resource as well.</span></span>

![指派給專案工作的具名團隊成員](media/RM-how-to-17.png)

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="4f7b8-115">使用多個履行具名資源履行一般資源</span><span class="sxs-lookup"><span data-stu-id="4f7b8-115">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="4f7b8-116">使用多個具名資源來履行一般資源的需求，類似於指派單一具名資源。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-116">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="4f7b8-117">例如，有一項期間為五天且投入量為 120 小時的工作。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-117">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="4f7b8-118">這項工作無法由一週五天按一般八小時工作的資源完成。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-118">This task can't be completed by one resource that works a typical eight-hour day over a five day week.</span></span> 

![一項需要在五天內投入 120 小時完成的工作](media/RM-how-to-21.png)

<span data-ttu-id="4f7b8-120">此需求適合 120 小時為期五天 (每天 24 小時) 的機器人工程處理。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-120">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

![每天需求](media/RM-how-to-22.png)

<span data-ttu-id="4f7b8-122">這是一個需要多個具名資源來完成一般資源要求的範例。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-122">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="4f7b8-123">您需要預約多個資源來履行需求。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-123">You will need to book multiple resources to fulfill the requirement.</span></span>

![預約多個資源來履行需求](media/RM-how-to-23.png)

<span data-ttu-id="4f7b8-125">這種案例的主要區別在於，一般資源仍保留在指派給工作的團隊中，而預約的具名資源團隊成員並未指派為職位的一部分。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-125">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="4f7b8-126">專案經理可以視需要指派工作至具名資源。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-126">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="4f7b8-127">**協調** 檢視表可協助專案經理將跨多個資源的預約細分為工作指派。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-127">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="4f7b8-128">系統不自動這樣做，因為在任何較上述簡單範例的複雜的案例中，例如您有大量產生需求的工作時，專案經理要如何指派的意向，必須由系統進行假設。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-128">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement, the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="4f7b8-129">因為系統無法了解意向，假設可能與預期有所不同，並且會發生不正確或不可預測的結果。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-129">Because the system can't understand intent, chances are that the assumptions will be different than intended and an incorrect or unpredictable result will happen.</span></span> <span data-ttu-id="4f7b8-130">可預知的結果是，在專案經理透過 **協調** 檢視表的協助審慎建立指派之前，一般資源仍保留已指派的狀態。</span><span class="sxs-lookup"><span data-stu-id="4f7b8-130">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]