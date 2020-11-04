---
title: 一般資源需求履行
description: 本主題提供有關如何為一般資源需求預約具名資源的資訊。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 6bb7c185656ff87bb3ca24209594c07d25862d70
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072941"
---
# <a name="generic-resource-requirement-fulfillment"></a><span data-ttu-id="61c30-103">一般資源需求履行</span><span class="sxs-lookup"><span data-stu-id="61c30-103">Generic resource requirement fulfillment</span></span>

<span data-ttu-id="61c30-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="61c30-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="61c30-105">您可以預約具名資源，以取代有資源需求的一般資源。</span><span class="sxs-lookup"><span data-stu-id="61c30-105">You can book a named resource to replace generic resource that has a resource requirement.</span></span>

1. <span data-ttu-id="61c30-106">在 **專案** 頁面上，選取 **團隊** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="61c30-106">On the **Projects** page, select the **Team** tab.</span></span>
2. <span data-ttu-id="61c30-107">從清單中選取具有資源需求的一般資源，然後選取 **預約** 。</span><span class="sxs-lookup"><span data-stu-id="61c30-107">Select the generic resource that has a resource requirement from the list, and then select **Book**.</span></span> <span data-ttu-id="61c30-108">或者，開啟資源需求，然後選取 **預約** 。</span><span class="sxs-lookup"><span data-stu-id="61c30-108">Or, open the resource requirement and then select **Book**.</span></span>
3. <span data-ttu-id="61c30-109">在 **排程小幫手** 頁面上，選取要預約到專案團隊的具名資源，然後選取 **預約** 。</span><span class="sxs-lookup"><span data-stu-id="61c30-109">On the **Schedule Assistant** page, select a named resource to book onto your project team and then select **Book**.</span></span>

<span data-ttu-id="61c30-110">預約由具名資源完成並履行後，將會以具名資源取代一般資源。</span><span class="sxs-lookup"><span data-stu-id="61c30-110">When the booking is complete and fulfilled by a named resource, the generic resource is replaced with the named resource.</span></span>

<span data-ttu-id="61c30-111">排程上的指派也會以具名資源來更新。</span><span class="sxs-lookup"><span data-stu-id="61c30-111">The assignments on the schedule are updated with the named resource as well.</span></span>

## <a name="fulfill-a-generic-resource-with-multiple-named-resources"></a><span data-ttu-id="61c30-112">使用多個履行具名資源履行一般資源</span><span class="sxs-lookup"><span data-stu-id="61c30-112">Fulfill a generic resource with multiple named resources</span></span>
<span data-ttu-id="61c30-113">使用多個具名資源來履行一般資源的需求，類似於指派單一具名資源。</span><span class="sxs-lookup"><span data-stu-id="61c30-113">Fulfilling a requirement for a generic resource with multiple named resources is similar to assigning a single named resource.</span></span> <span data-ttu-id="61c30-114">例如，有一項期間為五天且投入量為 120 小時的工作。</span><span class="sxs-lookup"><span data-stu-id="61c30-114">For example, there is a task with a duration of five days and 120 hours of effort.</span></span> <span data-ttu-id="61c30-115">這項工作無法由一般以五天為一週、每天工作八小時的資源完成。</span><span class="sxs-lookup"><span data-stu-id="61c30-115">This task can't be completed by one resource that works a typical eight-hour day over a five-day week.</span></span> 

<span data-ttu-id="61c30-116">此需求適合 120 小時為期五天 (每天 24 小時) 的機器人工程處理。</span><span class="sxs-lookup"><span data-stu-id="61c30-116">The requirement is for 120 hours of robotics engineering over five days, which is 24 hours per day.</span></span>

<span data-ttu-id="61c30-117">這是一個需要多個具名資源來完成一般資源要求的範例。</span><span class="sxs-lookup"><span data-stu-id="61c30-117">This is an example of when multiple named resources are needed to fulfill a generic resource request.</span></span> <span data-ttu-id="61c30-118">您需要預約多個資源來履行需求。</span><span class="sxs-lookup"><span data-stu-id="61c30-118">You will need to book multiple resources to fulfill the requirement.</span></span>

<span data-ttu-id="61c30-119">這種案例的主要區別在於，一般資源仍保留在指派給工作的團隊中，而預約的具名資源團隊成員並未指派為職位的一部分。</span><span class="sxs-lookup"><span data-stu-id="61c30-119">The main difference in this scenario is that the generic resource remains on the team assigned to the task, and the booked named resource team members are not assigned as part of the position.</span></span> <span data-ttu-id="61c30-120">專案經理可以視需要指派工作至具名資源。</span><span class="sxs-lookup"><span data-stu-id="61c30-120">The project manager can assign the work as appropriate to the named resources.</span></span> <span data-ttu-id="61c30-121">**協調** 檢視表可協助專案經理將跨多個資源的預約細分為工作指派。</span><span class="sxs-lookup"><span data-stu-id="61c30-121">The **Reconciliation** view can assist a project manager in breaking up the bookings across multiple resources to task assignments.</span></span> <span data-ttu-id="61c30-122">系統不自動這樣做，因為在任何比上述簡單範例還要複雜的案例中 (例如您有大量產生需求的工作時，或專案經理要如何指派的意向)，都必須由系統進行假設。</span><span class="sxs-lookup"><span data-stu-id="61c30-122">This is not done automatically because in any scenario more complicated than the simple example above, such as where you have a bundle of tasks making up the requirement or the intent of how the project manager wants to assign, needs to be assumed by the system.</span></span> <span data-ttu-id="61c30-123">因為系統無法了解意向，假設可能會與預期的不同，而且會發生不正確或不可預測的結果。</span><span class="sxs-lookup"><span data-stu-id="61c30-123">Because the system can't understand intent, it's likely that the assumptions will be different than intended and an incorrect or unpredictable result will occur.</span></span> <span data-ttu-id="61c30-124">可預知的結果是，在專案經理透過 **協調** 檢視表的協助審慎建立指派之前，一般資源仍保留已指派的狀態。</span><span class="sxs-lookup"><span data-stu-id="61c30-124">The predictable outcome is that the generic resource remains assigned until the project manager deliberately creates assignments, with the assistance of the **Reconciliation** view.</span></span>


