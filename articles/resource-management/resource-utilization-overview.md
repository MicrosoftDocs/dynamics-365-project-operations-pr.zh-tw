---
title: 資源使用率概觀
description: 本主題提供 Project Operations 中資源使用率的資訊。
author: ruhercul
manager: Annbe
ms.date: 11/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 4d66b5fc642ef53adf1169ce891a7a5fa26b07d6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279308"
---
# <a name="resource-utilization-overview"></a><span data-ttu-id="e23dd-103">資源使用率概觀</span><span class="sxs-lookup"><span data-stu-id="e23dd-103">Resource utilization overview</span></span>

<span data-ttu-id="e23dd-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="e23dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e23dd-105">資源可以有目標計費使用率。</span><span class="sxs-lookup"><span data-stu-id="e23dd-105">Resources can have a target billable utilization.</span></span> <span data-ttu-id="e23dd-106">此目標使用率會定義為資源預設角色的屬性，或是透過個別可預約資源的記錄來設定。</span><span class="sxs-lookup"><span data-stu-id="e23dd-106">This target utilization is defined as an attribute on a resource's default role or set on the record of the individual bookable resource.</span></span> <span data-ttu-id="e23dd-107">使用率計算是根據資源使用核准的時間項目所報告的實際時數來進行。</span><span class="sxs-lookup"><span data-stu-id="e23dd-107">Utilization calculations are based on the actual hours that resources have reported by using approved time entries.</span></span>

<span data-ttu-id="e23dd-108">下列公式用於計算使用率：</span><span class="sxs-lookup"><span data-stu-id="e23dd-108">The following formulas are used to calculate utilization:</span></span>

  - <span data-ttu-id="e23dd-109">計費使用率 = 應收費實際時數 ÷ 資源產能</span><span class="sxs-lookup"><span data-stu-id="e23dd-109">Billable utilization = Chargeable actual hours ÷ Resource capacity</span></span>
  - <span data-ttu-id="e23dd-110">非計費使用率 = 帳單類型識別碼為 [不應收費]、[附贈] 或 [不適用] 的實際時間 ÷ 資源產能</span><span class="sxs-lookup"><span data-stu-id="e23dd-110">Non-billable utilization = Actual time with billing type ID = Non-chargeable, Complementary, or Not available ÷ Resource capacity</span></span>
  - <span data-ttu-id="e23dd-111">內部 = 無銷售合約的實際時間 ÷ 資源產能</span><span class="sxs-lookup"><span data-stu-id="e23dd-111">Internal = Actual time with no sales contract ÷ Resource capacity</span></span>
  - <span data-ttu-id="e23dd-112">資源產能 = 資源工作時數 – 不在辦公室 – 非工作天數</span><span class="sxs-lookup"><span data-stu-id="e23dd-112">Resource capacity = Resource work hours – Out-of-office – Non-working days</span></span>

<span data-ttu-id="e23dd-113">您可以在 **資源** 窗格中找到 **資源使用率** 檢視表。</span><span class="sxs-lookup"><span data-stu-id="e23dd-113">You can find the **Resource Utilization** view in the **Resources** pane.</span></span>

<span data-ttu-id="e23dd-114">網格中的每個儲存格表示一個週期 (例如日、週或月) 中資源的計費使用率百分比。</span><span class="sxs-lookup"><span data-stu-id="e23dd-114">Each cell in the grid represents the billable utilization percentage of the resource in a period, such as a day, week, or month.</span></span> <span data-ttu-id="e23dd-115">下列公式用於設定儲存格的色彩：</span><span class="sxs-lookup"><span data-stu-id="e23dd-115">The following formulas are used to color the cells:</span></span>

  - <span data-ttu-id="e23dd-116">**綠色**：計費使用率 >= 資源目標使用率</span><span class="sxs-lookup"><span data-stu-id="e23dd-116">**Green**: Billable utilization >= Resource target utilization</span></span>
  - <span data-ttu-id="e23dd-117">**黃色**：目標使用率 – 20 <= 計費使用率 < 目標使用率</span><span class="sxs-lookup"><span data-stu-id="e23dd-117">**Yellow**: Target utilization – 20 <= Billable utilization < Target utilization</span></span>
  - <span data-ttu-id="e23dd-118">**紅色**：計費使用率 < 目標使用率 - 20</span><span class="sxs-lookup"><span data-stu-id="e23dd-118">**Red**: Billable utilization < Target utilization – 20</span></span>

<span data-ttu-id="e23dd-119">因為 **資源使用率** 檢視表以排程面板為基礎，所以您可以使用排程面板的篩選功能來篩選結果。</span><span class="sxs-lookup"><span data-stu-id="e23dd-119">Because the **Resource Utilization** view is based on the Schedule Board, you can use the filtering capabilities of the Schedule Board to filter your results.</span></span>

<span data-ttu-id="e23dd-120">網格要求您必須對角色或個別資源設定目標使用率。</span><span class="sxs-lookup"><span data-stu-id="e23dd-120">The grid requires that you set a target utilization on either the role or the individual resource.</span></span> <span data-ttu-id="e23dd-121">若要進行此設定，請移至 **資源** > **資源角色**。</span><span class="sxs-lookup"><span data-stu-id="e23dd-121">To do this setup, go to **Resources** > **Resource roles**.</span></span>

<span data-ttu-id="e23dd-122">此外，還必須將預設角色指派給每個可預約資源。</span><span class="sxs-lookup"><span data-stu-id="e23dd-122">Additionally, a default role must be assigned to each bookable resource.</span></span> <span data-ttu-id="e23dd-123">移至 **資源** > **資源**。</span><span class="sxs-lookup"><span data-stu-id="e23dd-123">Go to **Resources** > **Resources**.</span></span> <span data-ttu-id="e23dd-124">在 **Project Service** 索引標籤上，確認已定義資源角色，且 **是預設值** 欄位已設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="e23dd-124">On the **Project Service** tab, verify that a resource role is defined, and that the **Is Default** field is set to **Yes**.</span></span> <span data-ttu-id="e23dd-125">您可以新增其他角色，其中 **是預設值** = **否**。</span><span class="sxs-lookup"><span data-stu-id="e23dd-125">You can add additional roles where **Is Default** = **No**.</span></span> <span data-ttu-id="e23dd-126">**是預設值** = **是** 的角色會用來對照該角色的目標來評估資源的使用率。</span><span class="sxs-lookup"><span data-stu-id="e23dd-126">The role where the **Is Default** = **Yes** is used to evaluate the resource's utilization against the target for that role.</span></span>

<span data-ttu-id="e23dd-127">在 **Project Service** 索引標籤上，您也可以設定資源的個別目標使用率。</span><span class="sxs-lookup"><span data-stu-id="e23dd-127">On the **Project Service** tab, you can also set an individual target utilization for the resource.</span></span> <span data-ttu-id="e23dd-128">使用率計算接著會使用該目標使用率來評估資源的目標，而不是資源預設角色的目標。</span><span class="sxs-lookup"><span data-stu-id="e23dd-128">The utilization calculation then uses that target utilization to evaluate the resource's target instead of the target of the resource's default role.</span></span>

<span data-ttu-id="e23dd-129">只有當資源在網格所顯示週期內有獲核准的應收費時間時，才會顯示資源的使用率。</span><span class="sxs-lookup"><span data-stu-id="e23dd-129">Utilization is only shown for a resource if that resource has approved, chargeable time during the period shown in the grid.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]