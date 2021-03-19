---
title: 安全性模型
description: 此主題提供有關 Dynamics 365 Project Operations 中安全性模型的資訊。
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 3f65d13809fef342be8bec682c11d95c4d9e9b19
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276788"
---
# <a name="security-model"></a><span data-ttu-id="c23d1-103">安全性模型</span><span class="sxs-lookup"><span data-stu-id="c23d1-103">Security Model</span></span>

<span data-ttu-id="c23d1-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="c23d1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c23d1-105">Microsoft Dynamics 365 Project Operations 包含獨特的安全性模型，允許與 Microsoft Office 群組協同合作的角色型業務安全性模型。</span><span class="sxs-lookup"><span data-stu-id="c23d1-105">Microsoft Dynamics 365 Project Operations contains a unique security model that allows for a role-based business security model that collaborates with Microsoft Office Groups.</span></span> 


## <a name="security-roles"></a><span data-ttu-id="c23d1-106">安全性角色</span><span class="sxs-lookup"><span data-stu-id="c23d1-106">Security roles</span></span>
<span data-ttu-id="c23d1-107">Project Operations 前端功能包含下列角色：</span><span class="sxs-lookup"><span data-stu-id="c23d1-107">Project Operations front-end capabilities include the following roles:</span></span>

| <span data-ttu-id="c23d1-108">角色</span><span class="sxs-lookup"><span data-stu-id="c23d1-108">Role</span></span>                          | <span data-ttu-id="c23d1-109">描述</span><span class="sxs-lookup"><span data-stu-id="c23d1-109">Description</span></span>                                                                                                                                                                 | <span data-ttu-id="c23d1-110">Scope</span><span class="sxs-lookup"><span data-stu-id="c23d1-110">Scope</span></span> |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| <span data-ttu-id="c23d1-111">實務經理</span><span class="sxs-lookup"><span data-stu-id="c23d1-111">Practice manager</span></span>              | <span data-ttu-id="c23d1-112">支援跨專案報表。</span><span class="sxs-lookup"><span data-stu-id="c23d1-112">Supports cross-project reporting.</span></span>                                                                                                            | <span data-ttu-id="c23d1-113">營業單位</span><span class="sxs-lookup"><span data-stu-id="c23d1-113">Business unit</span></span>              |
| <span data-ttu-id="c23d1-114">專案核准者</span><span class="sxs-lookup"><span data-stu-id="c23d1-114">Project approver</span></span>              | <span data-ttu-id="c23d1-115">核准專案的時間和費用。</span><span class="sxs-lookup"><span data-stu-id="c23d1-115">Approves time and expenses against a project.</span></span>                                                                                                                              | <span data-ttu-id="c23d1-116">營業單位</span><span class="sxs-lookup"><span data-stu-id="c23d1-116">Business unit</span></span> |
| <span data-ttu-id="c23d1-117">專案帳務管理員</span><span class="sxs-lookup"><span data-stu-id="c23d1-117">Project billing administrator</span></span> | <span data-ttu-id="c23d1-118">建立發票提案。</span><span class="sxs-lookup"><span data-stu-id="c23d1-118">Creates the invoice proposal.</span></span>                                                                                                                                                 | <span data-ttu-id="c23d1-119">營業單位</span><span class="sxs-lookup"><span data-stu-id="c23d1-119">Business unit</span></span> |
| <span data-ttu-id="c23d1-120">專案經理</span><span class="sxs-lookup"><span data-stu-id="c23d1-120">Project manager</span></span>               | <span data-ttu-id="c23d1-121">建立專案計劃並要求資源。</span><span class="sxs-lookup"><span data-stu-id="c23d1-121">Creates the project plan and requests resources.</span></span>                                                                                                                              | <span data-ttu-id="c23d1-122">營業單位</span><span class="sxs-lookup"><span data-stu-id="c23d1-122">Business unit</span></span> |
| <span data-ttu-id="c23d1-123">專案資源</span><span class="sxs-lookup"><span data-stu-id="c23d1-123">Project resource</span></span>              | <span data-ttu-id="c23d1-124">可供預約和報告時間的團隊成員。</span><span class="sxs-lookup"><span data-stu-id="c23d1-124">Team members who can be booked and report time.</span></span>                                                                                                          | <span data-ttu-id="c23d1-125">營業單位</span><span class="sxs-lookup"><span data-stu-id="c23d1-125">Business unit</span></span>|
| <span data-ttu-id="c23d1-126">資源管理員</span><span class="sxs-lookup"><span data-stu-id="c23d1-126">Resource manager</span></span>              | <span data-ttu-id="c23d1-127">所有資源管理功能 (例如履行資源要求和預約)，分別支援混合式「專案經理 + 資源管理員」設定以及單一和集中式資源管理員角色。</span><span class="sxs-lookup"><span data-stu-id="c23d1-127">All resource management functions, such as fulfill resource requests and bookings, separated to support a hybrid Project manager + Resource manager configuration and a single and centralized Resource manager role.</span></span> | <span data-ttu-id="c23d1-128">營業單位</span><span class="sxs-lookup"><span data-stu-id="c23d1-128">Business unit</span></span> |


<span data-ttu-id="c23d1-129">Microsoft Project 網頁版包含下列角色：</span><span class="sxs-lookup"><span data-stu-id="c23d1-129">Microsoft Project for the Web includes the following roles:</span></span>

| <span data-ttu-id="c23d1-130">角色</span><span class="sxs-lookup"><span data-stu-id="c23d1-130">Role</span></span>           | <span data-ttu-id="c23d1-131">描述</span><span class="sxs-lookup"><span data-stu-id="c23d1-131">Description</span></span>                                                                                                        | <span data-ttu-id="c23d1-132">Scope</span><span class="sxs-lookup"><span data-stu-id="c23d1-132">Scope</span></span>  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| <span data-ttu-id="c23d1-133">專案使用者</span><span class="sxs-lookup"><span data-stu-id="c23d1-133">Project user</span></span>   | <span data-ttu-id="c23d1-134">專案的共同作業使用者，他們可以建立自己的專案，並檢視任何與其共用的專案。</span><span class="sxs-lookup"><span data-stu-id="c23d1-134">Collaborative user of Project   who is able to create their own projects and view any projects shared with   them.</span></span> | <span data-ttu-id="c23d1-135">使用者</span><span class="sxs-lookup"><span data-stu-id="c23d1-135">User</span></span>   |
| <span data-ttu-id="c23d1-136">專案系統</span><span class="sxs-lookup"><span data-stu-id="c23d1-136">Project system</span></span> | <span data-ttu-id="c23d1-137">用於應用程式內容的角色。</span><span class="sxs-lookup"><span data-stu-id="c23d1-137">Role used for application   context.</span></span> <span data-ttu-id="c23d1-138">客戶不應使用此系統角色。</span><span class="sxs-lookup"><span data-stu-id="c23d1-138">Customers should not use this system role.</span></span>                                    | <span data-ttu-id="c23d1-139">全域</span><span class="sxs-lookup"><span data-stu-id="c23d1-139">Global</span></span> |

## <a name="security-enforcement"></a><span data-ttu-id="c23d1-140">安全性強制</span><span class="sxs-lookup"><span data-stu-id="c23d1-140">Security enforcement</span></span>
<span data-ttu-id="c23d1-141">在專案層級執行的動作會已登入使用者的內容中執行。</span><span class="sxs-lookup"><span data-stu-id="c23d1-141">Actions that are performed at the project level are performed in the context of the logged in user.</span></span> <span data-ttu-id="c23d1-142">這表示要建立、開啟或刪除專案，使用者就必須具有可在 CDS 中使用的存取權。</span><span class="sxs-lookup"><span data-stu-id="c23d1-142">This means that in order to create, open, or delete a project, the user is required to have access available in CDS.</span></span> <span data-ttu-id="c23d1-143">CDS 中的存取權可能會透過平台提供的任何可能機制來授與。</span><span class="sxs-lookup"><span data-stu-id="c23d1-143">Access in CDS may be granted through any of the possible mechanisms included in the platform.</span></span> <span data-ttu-id="c23d1-144">例如，範圍較大的使用者可以存取專案，或者如果已執行授與使用者存取權的明確專案共用動作。</span><span class="sxs-lookup"><span data-stu-id="c23d1-144">For example, a user with a larger scope may access the project or if an explicit project share action has been performed which grants the user access.</span></span>

<span data-ttu-id="c23d1-145">在 Project Operations 中建立專案時，請務必要考慮這一點。</span><span class="sxs-lookup"><span data-stu-id="c23d1-145">It's important to consider this when creating projects in Project Operations.</span></span>

## <a name="modern-group-collaboration-with-project-operations"></a><span data-ttu-id="c23d1-146">使用 Project Operations 的新式群組共同作業</span><span class="sxs-lookup"><span data-stu-id="c23d1-146">Modern group collaboration with Project Operations</span></span>
<span data-ttu-id="c23d1-147">Project 網頁版和 Project Operations 支援新式共同作業群組。</span><span class="sxs-lookup"><span data-stu-id="c23d1-147">Project for the Web and Project Operations support modern groups for collaboration.</span></span> <span data-ttu-id="c23d1-148">透過群組新增至專案的使用者可以編輯專案計劃。</span><span class="sxs-lookup"><span data-stu-id="c23d1-148">Users added to the project through a group are able to edit the project plan.</span></span>

<span data-ttu-id="c23d1-149">Project 網頁版會自動在指派時將使用者新增至群組。</span><span class="sxs-lookup"><span data-stu-id="c23d1-149">Project for the Web adds users to the group automatically upon assignment.</span></span>

<span data-ttu-id="c23d1-150">群組允許專案權限，並且可以支援共同處理共同作業成品。</span><span class="sxs-lookup"><span data-stu-id="c23d1-150">Groups allow the permissions of the project and supporting collaboration artifacts to be worked on collaboratively.</span></span> <span data-ttu-id="c23d1-151">下圖描述執行群組指派程序時發生的事件和狀態變更。</span><span class="sxs-lookup"><span data-stu-id="c23d1-151">The following diagram depicts the events and state changes that happen during the group assignment process.</span></span>

<span data-ttu-id="c23d1-152">Project Operations 不會透過隱含式動作建立群組，只會透過按下群組的明確動作這樣做。</span><span class="sxs-lookup"><span data-stu-id="c23d1-152">Project Operations does not create a group through implicit action and only does so through the explicit action of pressing groups.</span></span>

<span data-ttu-id="c23d1-153">**群組管理** 對話方塊中的群組成員搜尋，僅限於已設定為環境安全性群組之一部分的人員。</span><span class="sxs-lookup"><span data-stu-id="c23d1-153">Group member search in the **Group management** dialog, is limited to those who are set as part of the environment's security group.</span></span> <span data-ttu-id="c23d1-154">如需詳細資訊，請參閱[控制使用者對環境的存取：安全性群組和授權](https://docs.microsoft.com/power-platform/admin/control-user-access)。</span><span class="sxs-lookup"><span data-stu-id="c23d1-154">For more information, see [Control user access to environments: security groups and licenses](https://docs.microsoft.com/power-platform/admin/control-user-access).</span></span>

![群組模式](./media/groupsmode.png)

1. <span data-ttu-id="c23d1-156">專案已建立並且由建立使用者所擁有。</span><span class="sxs-lookup"><span data-stu-id="c23d1-156">The Project is created and owned by the creating User.</span></span>
2. <span data-ttu-id="c23d1-157">專案負責人會更新為團隊。</span><span class="sxs-lookup"><span data-stu-id="c23d1-157">The Project owner is updated to the team.</span></span>
3. <span data-ttu-id="c23d1-158">負責人團隊會對應至指定的或建立的 Office 群組。</span><span class="sxs-lookup"><span data-stu-id="c23d1-158">The Owner team is mapped to the specified or created Office Group.</span></span>
4. <span data-ttu-id="c23d1-159">專案的原始負責人會新增至 Office 群組。</span><span class="sxs-lookup"><span data-stu-id="c23d1-159">The original owner of the Project is added to the Office Group.</span></span>

## <a name="deployment-recommendation"></a><span data-ttu-id="c23d1-160">部署建議</span><span class="sxs-lookup"><span data-stu-id="c23d1-160">Deployment recommendation</span></span>
<span data-ttu-id="c23d1-161">隨著 Office 群組共同作業模型的演變，將會不斷新增功能，與時俱進地提供更精細的控制。</span><span class="sxs-lookup"><span data-stu-id="c23d1-161">As the Office group collaboration model evolves, functionality will be added to provide more detailed control over time.</span></span> <span data-ttu-id="c23d1-162">現今部署 Project Operations 的使用者，最好還是將重點放在傳統 Microsoft Dynamics 365 安全性模型上。</span><span class="sxs-lookup"><span data-stu-id="c23d1-162">Customers that deploy Project Operations today are encouraged to focus on a traditional Microsoft Dynamics 365 security model.</span></span>

<span data-ttu-id="c23d1-163">如需詳細資訊，請參閱 [Common Data Service 中的安全性](https://docs.microsoft.com/power-platform/admin/wp-security)。</span><span class="sxs-lookup"><span data-stu-id="c23d1-163">For more information, see [Security in Common Data Service](https://docs.microsoft.com/power-platform/admin/wp-security).</span></span>

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a><span data-ttu-id="c23d1-164">Project Operations 和 Microsoft Dynamics 365 Finance 安全性</span><span class="sxs-lookup"><span data-stu-id="c23d1-164">Project Operations and Microsoft Dynamics 365 Finance security</span></span>
<span data-ttu-id="c23d1-165">Project Operations 包含下列角色：</span><span class="sxs-lookup"><span data-stu-id="c23d1-165">Project Operations includes the following roles:</span></span>

- <span data-ttu-id="c23d1-166">專案經理</span><span class="sxs-lookup"><span data-stu-id="c23d1-166">Project manager</span></span>
- <span data-ttu-id="c23d1-167">專案會計師</span><span class="sxs-lookup"><span data-stu-id="c23d1-167">Project accountant</span></span>

<span data-ttu-id="c23d1-168">如需有關 Finance 中安全性的詳細資訊，請參閱[角色型安全性](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security)。</span><span class="sxs-lookup"><span data-stu-id="c23d1-168">For more information about security in Finance, see [Role-based security](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security).</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]