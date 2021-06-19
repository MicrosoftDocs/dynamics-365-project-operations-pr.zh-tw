---
title: 資源管理常見問題集
description: 本主題提供關於資源管理的常見問題解答。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
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
ms.openlocfilehash: 25e069beaffc9081a5516449d55b5c9304c23b0f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008751"
---
# <a name="resource-management-faq"></a><span data-ttu-id="82867-103">資源管理常見問題集</span><span class="sxs-lookup"><span data-stu-id="82867-103">Resource management FAQ</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

## <a name="what-is-the-difference-between-a-team-member-and-a-resource-requirement"></a><span data-ttu-id="82867-104">團隊成員與資源需求之間有何區別？</span><span class="sxs-lookup"><span data-stu-id="82867-104">What is the difference between a team member and a resource requirement?</span></span>

<span data-ttu-id="82867-105">專案團隊成員可以指派給工作、預約或過量預約，以及設定為核准者。</span><span class="sxs-lookup"><span data-stu-id="82867-105">A project team member can be assigned to tasks, booked or overbooked, and set as an approver.</span></span> <span data-ttu-id="82867-106">資源需求沒有專案團隊成員也能存在，就像索求的草稿附註一樣。</span><span class="sxs-lookup"><span data-stu-id="82867-106">A resource requirement can exist without a project team member, as a draft note of demand.</span></span> 

## <a name="what-is-the-difference-between-proposed-and-soft-booked-hours"></a><span data-ttu-id="82867-107">提案時數與未確認預約時數之間有何區別？</span><span class="sxs-lookup"><span data-stu-id="82867-107">What is the difference between proposed and soft-booked hours?</span></span>

<span data-ttu-id="82867-108">提案時數與未確認預約時數在顯示性上不同。</span><span class="sxs-lookup"><span data-stu-id="82867-108">Proposed hours and soft-booked hours differ in visibility.</span></span> <span data-ttu-id="82867-109">提案的時數僅顯示給資源管理員以及使用資源要求提出索求的專案經理。</span><span class="sxs-lookup"><span data-stu-id="82867-109">Proposed hours are visible only to resource managers and the project manager who initiated the demand by using a resource request.</span></span> <span data-ttu-id="82867-110">未確認預約時數可顯示給任何有權存取排程面板的使用者。</span><span class="sxs-lookup"><span data-stu-id="82867-110">Soft-booked hours are visible to anyone who has access to the Schedule Board.</span></span>

## <a name="how-can-i-see-the-soft-booked-hours-for-resources-on-a-team"></a><span data-ttu-id="82867-111">如何在團隊中看到資源的未確認預約時數？</span><span class="sxs-lookup"><span data-stu-id="82867-111">How can I see the soft-booked hours for resources on a team?</span></span>

<span data-ttu-id="82867-112">在您預約資源需求時，可以進行未確認預約。</span><span class="sxs-lookup"><span data-stu-id="82867-112">Soft bookings can made when you book a resource requirement.</span></span> <span data-ttu-id="82867-113">在專案團隊上未確認預約的資源，會顯示為具有未確認預約時數的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="82867-113">Resources that are soft-booked on a project team appear as team members who have soft-booked hours.</span></span> <span data-ttu-id="82867-114">這些成員也會在排程面板上出現。</span><span class="sxs-lookup"><span data-stu-id="82867-114">They also appear on the Schedule Board.</span></span>

## <a name="how-do-i-change-the-required-hours-and-the-start-and-end-dates-for-a-resource-generic-or-named-that-i-booked"></a><span data-ttu-id="82867-115">如何變更我已預約之資源 (一般或具名) 的需要時數以及開始和結束日期？</span><span class="sxs-lookup"><span data-stu-id="82867-115">How do I change the required hours, and the start and end dates, for a resource (generic or named) that I booked?</span></span>

<span data-ttu-id="82867-116">預約資源之後，選取 **維護預約** 即可進行任何必要的變更。</span><span class="sxs-lookup"><span data-stu-id="82867-116">After resources are booked, select **Maintain Bookings** to make any changes that are required.</span></span>

## <a name="what-resources-types-does-project-service-automation-support"></a><span data-ttu-id="82867-117">Project Service Automation 支援哪些資源類型？</span><span class="sxs-lookup"><span data-stu-id="82867-117">What resources types does Project Service Automation support?</span></span>

<span data-ttu-id="82867-118">**使用者** 和 **連絡人** 是唯一在 Dynamics 365 Project Service Automation 中支援的資源類型。</span><span class="sxs-lookup"><span data-stu-id="82867-118">**User** and **Contact** are the only resource types that are supported in Dynamics 365 Project Service Automation.</span></span> <span data-ttu-id="82867-119">雖然您可以建立其他類型的資源 (例如, **設備** 和 **群組**)，但是不支援這些資源的端對端使用案例。</span><span class="sxs-lookup"><span data-stu-id="82867-119">Although you can create other types of resources (for example, **Equipment** and **Group**), no end-to-end use case is supported for them.</span></span>

## <a name="what-is-the-difference-between-an-assignment-and-a-booking"></a><span data-ttu-id="82867-120">指派與預約之間有何區別？</span><span class="sxs-lookup"><span data-stu-id="82867-120">What is the difference between an assignment and a booking?</span></span>

<span data-ttu-id="82867-121">指派是在專案排程中對專案工作的資源指派。</span><span class="sxs-lookup"><span data-stu-id="82867-121">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="82867-122">資源可以是實際或一般資源。</span><span class="sxs-lookup"><span data-stu-id="82867-122">The resources can be either real or generic resources.</span></span> <span data-ttu-id="82867-123">預約是為專案進行的已確認或未確認資源配置。</span><span class="sxs-lookup"><span data-stu-id="82867-123">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="82867-124">已確認預約會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="82867-124">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="82867-125">對於實際資源，預約與指派最好要一致，因為兩者並無差別。</span><span class="sxs-lookup"><span data-stu-id="82867-125">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="82867-126">但是，PSA 不會強制這樣的一致性。</span><span class="sxs-lookup"><span data-stu-id="82867-126">However, PSA doesn't enforce this agreement.</span></span> <span data-ttu-id="82867-127">協調檢視表會向專案經理顯示資源預約與指派不一致的地方。</span><span class="sxs-lookup"><span data-stu-id="82867-127">The Reconciliation view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]