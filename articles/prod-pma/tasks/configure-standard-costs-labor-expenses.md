---
title: 設定人力和費用的標準成本
description: 本主題說明如何設定專案的人力和費用標準成本。
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073053"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a><span data-ttu-id="9fc45-103">設定人力和費用的標準成本</span><span class="sxs-lookup"><span data-stu-id="9fc45-103">Configure standard costs for labor and expenses</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="9fc45-104">本主題說明如何設定專案的人力和費用標準成本。</span><span class="sxs-lookup"><span data-stu-id="9fc45-104">This topic explains how to set up standard costs for labor and expenses for a project.</span></span> <span data-ttu-id="9fc45-105">此工作會使用 USSI 資料集。</span><span class="sxs-lookup"><span data-stu-id="9fc45-105">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="9fc45-106">在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 成本價 (小時)** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-106">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (hour)**.</span></span>
2. <span data-ttu-id="9fc45-107">選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-107">Select **New**.</span></span>
3. <span data-ttu-id="9fc45-108">在 **生效日期** 欄位中，輸入日期。</span><span class="sxs-lookup"><span data-stu-id="9fc45-108">In the **Effective date** field, enter a date.</span></span>
4. <span data-ttu-id="9fc45-109">在 **成本價** 欄位中，輸入數字。</span><span class="sxs-lookup"><span data-stu-id="9fc45-109">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="9fc45-110">您可以設定專案類別的標準成本價，也可以依工作者編號、專案編號、類別、日期或任何這些項目的組合來設定成本價。</span><span class="sxs-lookup"><span data-stu-id="9fc45-110">You can set up a standard cost price for the project category, or you can set up a cost price by worker number, project number, category, date, or any combination of these.</span></span> <span data-ttu-id="9fc45-111">所套用的成本價是詳細等級最高的成本價。</span><span class="sxs-lookup"><span data-stu-id="9fc45-111">The cost price that is applied is the cost price with the highest level of detail.</span></span>  
5. <span data-ttu-id="9fc45-112">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-112">Select **Save**.</span></span>
6. <span data-ttu-id="9fc45-113">在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 售價 (小時)** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-113">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (hour)**.</span></span>
7. <span data-ttu-id="9fc45-114">選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-114">Select **New**.</span></span>
8. <span data-ttu-id="9fc45-115">在 **生效日期** 欄位中，輸入日期。</span><span class="sxs-lookup"><span data-stu-id="9fc45-115">In the **Effective date** field, enter a date.</span></span>
9. <span data-ttu-id="9fc45-116">在 **有效期間** 欄位中，選取選項。</span><span class="sxs-lookup"><span data-stu-id="9fc45-116">In the **Valid for** field, select an option.</span></span>
10. <span data-ttu-id="9fc45-117">在 **定價** 欄位中，輸入數字。</span><span class="sxs-lookup"><span data-stu-id="9fc45-117">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="9fc45-118">您可以設定工時交易或專案類別設的標準售價。</span><span class="sxs-lookup"><span data-stu-id="9fc45-118">You can set up a standard sales price for hour transactions or for a project category.</span></span> <span data-ttu-id="9fc45-119">您也可以依工作者編號、專案編號、類別、交易日期或這些項目的任意組合來設定售價。</span><span class="sxs-lookup"><span data-stu-id="9fc45-119">You can also set up sales prices by worker number, project number, category, transaction date, or any combination of these.</span></span> <span data-ttu-id="9fc45-120">工作者在工時日記帳輸入交易時所套用的實際售價是詳細等級最高的售價。</span><span class="sxs-lookup"><span data-stu-id="9fc45-120">The actual sales price, which is applied when a worker enters a transaction in the Hour journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9fc45-121">例如，如果一般售價和工作者特定售價都已設定，則會使用工作者特定售價。</span><span class="sxs-lookup"><span data-stu-id="9fc45-121">For example, if both a general sales price and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
11. <span data-ttu-id="9fc45-122">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-122">Select **Save**.</span></span>
12. <span data-ttu-id="9fc45-123">關閉頁面。</span><span class="sxs-lookup"><span data-stu-id="9fc45-123">Close the page.</span></span>
13. <span data-ttu-id="9fc45-124">在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 成本價 (費用)** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-124">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Cost price (expense)**.</span></span>
14. <span data-ttu-id="9fc45-125">選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-125">Select **New**.</span></span>
15. <span data-ttu-id="9fc45-126">在 **生效日期** 欄位中，輸入日期。</span><span class="sxs-lookup"><span data-stu-id="9fc45-126">In the **Effective date** field, enter a date.</span></span>
16. <span data-ttu-id="9fc45-127">在 **成本價** 欄位中，輸入數字。</span><span class="sxs-lookup"><span data-stu-id="9fc45-127">In the **Cost price** field, enter a number.</span></span> <span data-ttu-id="9fc45-128">您可以填入多個欄位，但這是儲存記錄所需的最少欄位。</span><span class="sxs-lookup"><span data-stu-id="9fc45-128">Multiple fields can be filled in, but this is the minimum needed to save the record.</span></span>  
17. <span data-ttu-id="9fc45-129">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-129">Select **Save**.</span></span>
18. <span data-ttu-id="9fc45-130">在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 售價 (費用)** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-130">In the navigation pane, go to **Modules > Project management and accounting > Setup > Prices > Sales price (expense)**.</span></span>
19. <span data-ttu-id="9fc45-131">選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-131">Select **New**.</span></span>
20. <span data-ttu-id="9fc45-132">在 **生效日期** 欄位中，輸入日期。</span><span class="sxs-lookup"><span data-stu-id="9fc45-132">In the **Effective date** field, enter a date.</span></span>
21. <span data-ttu-id="9fc45-133">在 **有效期間** 欄位中，選取選項。</span><span class="sxs-lookup"><span data-stu-id="9fc45-133">In the **Valid for** field, select an option.</span></span>
22. <span data-ttu-id="9fc45-134">在 **定價** 欄位中，輸入數字。</span><span class="sxs-lookup"><span data-stu-id="9fc45-134">In the **Pricing** field, enter a number.</span></span> <span data-ttu-id="9fc45-135">工作者在費用日記帳輸入交易時所套用的實際售價是詳細等級最高的售價。</span><span class="sxs-lookup"><span data-stu-id="9fc45-135">The actual sales price, which is applied when a worker enters transactions in an expense journal, is the sales price with the highest level of detail.</span></span> <span data-ttu-id="9fc45-136">例如，如果一般售價和工作者特定售價都已設定，則會使用工作者特定售價。</span><span class="sxs-lookup"><span data-stu-id="9fc45-136">For example, if both a general and a worker-specific sales price are set up, the worker-specific sales price is used.</span></span>  
23. <span data-ttu-id="9fc45-137">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="9fc45-137">Select **Save**.</span></span>

