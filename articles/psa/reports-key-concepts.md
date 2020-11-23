---
title: 重要概念
description: 本主題提供有關 Project Service Automation 中資源管理重要概念的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: 862e277d8109e810401bdecd4c45c2696275f8a8
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4120353"
---
# <a name="key-concepts"></a><span data-ttu-id="7f1f5-103">重要概念</span><span class="sxs-lookup"><span data-stu-id="7f1f5-103">Key concepts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7f1f5-104">下表定義 Dynamics 365 Project Service Automation 應用程式中使用的重要概念。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-104">The following table defines key concepts that are used in the Dynamics 365 Project Service Automation app.</span></span>

| <span data-ttu-id="7f1f5-105">概念</span><span class="sxs-lookup"><span data-stu-id="7f1f5-105">Concept</span></span>                    | <span data-ttu-id="7f1f5-106">定義</span><span class="sxs-lookup"><span data-stu-id="7f1f5-106">Definition</span></span> |
|----------------------------|------------|
| <span data-ttu-id="7f1f5-107">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="7f1f5-107">Project team member</span></span>        | <span data-ttu-id="7f1f5-108">身為專案團隊的一分子，專案團隊成員可以是有預約的具名資源、沒有預約的具名資源，或是一般資源。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-108">As part of the project team, a project team member can be a named resource that has bookings, a named resource that doesn't have bookings, or a generic resource.</span></span> <span data-ttu-id="7f1f5-109">一般資源沒有預約、適用範圍局限於專案，並且在整個專案中沒有產能限制。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-109">Generic resources don't have bookings, are local to the project, and don't have capacity constraints across projects.</span></span> |
| <span data-ttu-id="7f1f5-110">專案一般資源</span><span class="sxs-lookup"><span data-stu-id="7f1f5-110">Project generic resource</span></span>   | <span data-ttu-id="7f1f5-111">資源預留位置，可讓您形成團隊並配置專案計劃的人員，而不需知道具名資源。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-111">A resource placeholder that lets you form a team and staff a project plan without having to know the named resource.</span></span> <span data-ttu-id="7f1f5-112">專案行事曆會用作一般資源的行事曆。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-112">The project calendar is used as the generic resource's calendar.</span></span> <span data-ttu-id="7f1f5-113">您可以將一般資源新增至專案團隊並指派給工作。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-113">Generic resources can be added to a project team and assigned to tasks.</span></span> |
| <span data-ttu-id="7f1f5-114">已預約時數</span><span class="sxs-lookup"><span data-stu-id="7f1f5-114">Booked hours</span></span>               | <span data-ttu-id="7f1f5-115">資源時數是以確定方式針對專案所預約，有助於保證完成專案工作。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-115">Resource hours are hard-booked against a project to help guarantee that the project work is completed.</span></span> <span data-ttu-id="7f1f5-116">已預約的時數會耗用資源的整體資源。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-116">Booked hours are consumed from the resource's overall capacity.</span></span> <span data-ttu-id="7f1f5-117">預約只對具名資源進行，而不針對一般資源。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-117">Bookings are against named resources only, not against generic resources.</span></span> |
| <span data-ttu-id="7f1f5-118">已指派的時數</span><span class="sxs-lookup"><span data-stu-id="7f1f5-118">Assigned hours</span></span>             | <span data-ttu-id="7f1f5-119">資源時數是在專案排程中指派給工作。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-119">Resource hours are assigned to tasks in the project schedule.</span></span> <span data-ttu-id="7f1f5-120">指派可以對具名資源或一般資源進行。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-120">Assignments can be against either named resources or generic resources.</span></span> <span data-ttu-id="7f1f5-121">指派與預約無關，互不影響。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-121">Assignments can be independent of bookings.</span></span> |
| <span data-ttu-id="7f1f5-122">需要的時數</span><span class="sxs-lookup"><span data-stu-id="7f1f5-122">Required hours</span></span>             | <span data-ttu-id="7f1f5-123">需要但尚未由具名資源履行的產能。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-123">The capacity that is required, but that isn't yet fulfilled by a named resource.</span></span> <span data-ttu-id="7f1f5-124">需要的時數只與已產生資源需求的一般團隊成員相關。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-124">Required hours are relevant only for generic team members that have generated resource requirements.</span></span> |
| <span data-ttu-id="7f1f5-125">索求</span><span class="sxs-lookup"><span data-stu-id="7f1f5-125">Demand</span></span>                     | <span data-ttu-id="7f1f5-126">目前和近期工作負載。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-126">The current and incoming workload.</span></span> <span data-ttu-id="7f1f5-127">在 Project Service Automation 中，索求會顯示為資源需求或資源要求。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-127">In Project Service Automation, demand is shown as resource requirements or resource requests.</span></span> |
| <span data-ttu-id="7f1f5-128">資源需求</span><span class="sxs-lookup"><span data-stu-id="7f1f5-128">Resource requirement</span></span>       | <span data-ttu-id="7f1f5-129">用來為所需資源擷取需要時數、開始和結束日期、技能、地理位置及其他定價維度的實體。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-129">An entity that is used to capture required hours, start and end dates, skills, geography, and other pricing dimensions for the required resources.</span></span> <span data-ttu-id="7f1f5-130">資源需求是由專案團隊成員所產生，或是個別建立的。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-130">Resource requirements are either generated from project team members or individually created.</span></span> |
| <span data-ttu-id="7f1f5-131">資源要求</span><span class="sxs-lookup"><span data-stu-id="7f1f5-131">Resource request</span></span>           | <span data-ttu-id="7f1f5-132">用來當做「信封」傳遞必須由資源管理員履行之資源需求的實體。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-132">An entity that is used as an "envelope" to carry the resource requirement that must be fulfilled by a resource manager.</span></span> |
| <span data-ttu-id="7f1f5-133">資源預設角色</span><span class="sxs-lookup"><span data-stu-id="7f1f5-133">Resource default role</span></span>      | <span data-ttu-id="7f1f5-134">資源據以分為群組供計算使用率的角色。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-134">The role that a resource is grouped under for utilization calculation.</span></span> <span data-ttu-id="7f1f5-135">已假定資源具有角色所需的技能，且符合該角色的目標使用率。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-135">The resource is assumed to have the required skills for the role and to meet the target utilization for that role.</span></span> |
| <span data-ttu-id="7f1f5-136">資源組織單位</span><span class="sxs-lookup"><span data-stu-id="7f1f5-136">Resource organization unit</span></span> | <span data-ttu-id="7f1f5-137">將資源指派至的組織單位。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-137">The organizational unit that a resource is assigned to.</span></span> |
| <span data-ttu-id="7f1f5-138">分佈</span><span class="sxs-lookup"><span data-stu-id="7f1f5-138">Contour</span></span>                    | <span data-ttu-id="7f1f5-139">工作、需求或指派時數在細分成每日分佈時的說法。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-139">Task, requirement, or assignment hours as they are broken down into a daily distribution.</span></span> <span data-ttu-id="7f1f5-140">例如，一項為期五天的 40 小時工作，可在五天期間內分佈為每天 8 小時的工作。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-140">For example, a five-day, 40-hour task can be contoured into eight hours per day over five days.</span></span> |
| <span data-ttu-id="7f1f5-141">協調檢視表</span><span class="sxs-lookup"><span data-stu-id="7f1f5-141">Reconciliation view</span></span>        | <span data-ttu-id="7f1f5-142">顯示每個專案團隊成員預約與指派的檢視表。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-142">A view that shows the bookings and assignments for each project team member.</span></span> <span data-ttu-id="7f1f5-143">此檢視表可讓專案經理尋找預約與指派之間是否有任何不相符，如果出現任何不相符，即採取更正動作。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-143">This view lets the project manager look for any mismatch between bookings and assignments, and to take corrective action if any mismatch occurs.</span></span> |
| <span data-ttu-id="7f1f5-144">工作時數</span><span class="sxs-lookup"><span data-stu-id="7f1f5-144">Work hours</span></span>                 | <span data-ttu-id="7f1f5-145">用來識別資源產能以及工作時間和非工作時間的實體。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-145">An entity that is used to identify resource capacity, and working and non-working hours.</span></span> <span data-ttu-id="7f1f5-146">此實體也稱為資源行事曆。</span><span class="sxs-lookup"><span data-stu-id="7f1f5-146">This entity is also referred to as the resource calendar.</span></span> |
