---
title: 解析估計值及實際值的銷售價
description: 本主題提供有關如何解析估計值及實際值之銷售費率的資訊。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b4ae5b3c4a4378330caed97011f55ca11175e644
ms.sourcegitcommit: f8edff6422b82fdf2cea897faa6abb51e2c0c3c8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/21/2020
ms.locfileid: "4087843"
---
# <a name="resolve-sales-prices-for-estimates-and-actuals"></a><span data-ttu-id="10f5d-103">解析估計值及實際值的銷售價</span><span class="sxs-lookup"><span data-stu-id="10f5d-103">Resolve sales prices for estimates and actuals</span></span>

<span data-ttu-id="10f5d-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="10f5d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="10f5d-105">在 Dynamics 365 Project Operations 中解析估計值和實際值的銷售價時，系統會先使用相關專案報價或合約的日期和貨幣來解析銷售價目表。</span><span class="sxs-lookup"><span data-stu-id="10f5d-105">When sales prices on estimates and actuals are resolved in Dynamics 365 Project Operations, the system first uses the date and currency of the related project quote or contract to resolve the sales price list.</span></span> <span data-ttu-id="10f5d-106">解析銷售價目表之後，系統會解析銷售或帳單費率。</span><span class="sxs-lookup"><span data-stu-id="10f5d-106">After the sales price list is resolved, the system resolves the sales or bill rate.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="10f5d-107">解析時間實際及估計明細的銷售費率</span><span class="sxs-lookup"><span data-stu-id="10f5d-107">Resolve sales rates on actual and estimate lines for time</span></span>

<span data-ttu-id="10f5d-108">在 Project Operations 中，時間估計明細會用來表示時間的報價明細與合約服務內容詳細資料以及專案上的資源指派。</span><span class="sxs-lookup"><span data-stu-id="10f5d-108">In Project Operations, estimate lines for time are used to denote the quote line and contract line details for time and the resource assignments on the project.</span></span>

<span data-ttu-id="10f5d-109">解析銷售的價目表之後，系統會完成下列步驟以設定預設帳單費率。</span><span class="sxs-lookup"><span data-stu-id="10f5d-109">After a price list for sales is resolved, the system completes the following steps to default the bill rate.</span></span>

1. <span data-ttu-id="10f5d-110">系統會使用時間估計明細上的 **角色** 、 **資源供應公司** 和 **資源分配單位** 欄位，來比對解析後價目表中的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="10f5d-110">The system uses the **Role** , **Resourcing Company** , and **Resourcing Unit** fields on the estimate line for time, to match against the role price lines in the resolved price list.</span></span> <span data-ttu-id="10f5d-111">這項比對作業假設您使用的是帳單費率的現成可用定價維度。</span><span class="sxs-lookup"><span data-stu-id="10f5d-111">This matching assumes that out-of-box pricing dimensions for bill rates are being used.</span></span> <span data-ttu-id="10f5d-112">如果您已根據任何排除或搭配 **角色** 、 **資源供應公司** 及 **資源分配單位** 的其他欄位進行定價設定，則那會是用來擷取相符角色價格明細的組合。</span><span class="sxs-lookup"><span data-stu-id="10f5d-112">If you have configured pricing based on any other fields instead of, or in addition to **Role** , **Resourcing Company** , and **Resourcing Unit** , then that is the combination that will be used to retrieve a matching role price line.</span></span>
2. <span data-ttu-id="10f5d-113">如果系統找到具有 **角色** 、 **資源供應公司** 與 **資源分配單位** 欄位組合帳單費率的角色價格明細，則預設使用該帳單費率。</span><span class="sxs-lookup"><span data-stu-id="10f5d-113">If the system finds a role price line that has a bill rate for the **Role** , **Resourcing Company** , and **Resourcing Unit** field combination, then that bill rate is defaulted.</span></span>
3. <span data-ttu-id="10f5d-114">如果系統無法找到與 **角色** 、 **資源供應公司** 及 **資源分配單位** 欄位值相符的項目，則會擷取具有相符角色但 **資源單位** 值為 Null 的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="10f5d-114">If the system is unable to match the **Role** , **Resourcing Company** , and **Resourcing Unit** field values, then it retrieves role price lines with a matching role but null values of **Resource Unit**.</span></span> <span data-ttu-id="10f5d-115">系統找到相符角色價格記錄之後，就會將帳單費率預設為該記錄。</span><span class="sxs-lookup"><span data-stu-id="10f5d-115">After the system finds a matching role price record, it will default the bill rate from that record.</span></span> <span data-ttu-id="10f5d-116">這項比對假設 **角色** 與 **資源分配單位** 相對優先順序的現成可用設定為銷售定價維度。</span><span class="sxs-lookup"><span data-stu-id="10f5d-116">This matching assumes an out-of-the-box configuration for the relative priority of **Role** vs **Resourcing Unit** as a sales pricing dimension.</span></span>

> [!NOTE]
> <span data-ttu-id="10f5d-117">如果您已設定不同的 **角色** 、 **資源供應公司** 及 **資源分配單位** 優先順序，或者您有其他較高優先順序的維度，則此行為也會相應變更。</span><span class="sxs-lookup"><span data-stu-id="10f5d-117">If you configured a different prioritization of **Role** , **Resourcing Company** , and **Resourcing Unit** , or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="10f5d-118">系統會依照以那些含 Null 值列的定價維度居後的優先順序，擷取其值符合每個定價維度值的角色價格記錄。</span><span class="sxs-lookup"><span data-stu-id="10f5d-118">The system retrieves the role price records with matching values of each of the pricing dimension values in the order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolve-sales-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="10f5d-119">解析費用實際及估計明細的銷售費率</span><span class="sxs-lookup"><span data-stu-id="10f5d-119">Resolve sales rates on actual and estimate lines for expense</span></span>

<span data-ttu-id="10f5d-120">在 Project Operations 中，費用估計明細會用來表示費用的報價明細與合約服務內容詳細資料以及專案上的費用估計明細。</span><span class="sxs-lookup"><span data-stu-id="10f5d-120">In Project Operations, estimate lines for expense are used to denote the quote line and contract line details for expenses and the expense estimate lines on the project.</span></span>

<span data-ttu-id="10f5d-121">解析銷售的價目表之後，系統會完成下列步驟以設定預設單位銷售價。</span><span class="sxs-lookup"><span data-stu-id="10f5d-121">After a price list for sales is resolved, the system completes the following steps to default the unit sales price.</span></span>

1. <span data-ttu-id="10f5d-122">系統會使用費用估計明細上的 **類別** 與 **單位** 欄位組合，來比對解析後價目表中的類別價格明細。</span><span class="sxs-lookup"><span data-stu-id="10f5d-122">The system uses the **Category** and **Unit** field combination on the estimate line for expense to match against the category price lines in the price list that was resolved.</span></span>
2. <span data-ttu-id="10f5d-123">如果系統找到具有 **類別** 與 **單位** 欄位組合銷售費率的類別價格明細，則預設使用該銷售費率。</span><span class="sxs-lookup"><span data-stu-id="10f5d-123">If the system finds a category price line that has a sales rate for the **Category** and **Unit** field combination, then that sales rate is defaulted.</span></span>
3. <span data-ttu-id="10f5d-124">如果系統找到相符的類別價格明細，則可能會使用定價方式來設定預設銷售價。</span><span class="sxs-lookup"><span data-stu-id="10f5d-124">If the system finds a matching category price line, the pricing method may be used to default the sales price.</span></span> <span data-ttu-id="10f5d-125">下表顯示 Project Operations 中的費用價格預設行為。</span><span class="sxs-lookup"><span data-stu-id="10f5d-125">The following table below shows the expense price defaulting behavior in Project Operations.</span></span>

    | <span data-ttu-id="10f5d-126">內容</span><span class="sxs-lookup"><span data-stu-id="10f5d-126">Context</span></span> | <span data-ttu-id="10f5d-127">定價方式</span><span class="sxs-lookup"><span data-stu-id="10f5d-127">Pricing method</span></span> | <span data-ttu-id="10f5d-128">已預設的價格</span><span class="sxs-lookup"><span data-stu-id="10f5d-128">Price defaulted</span></span> |
    | --- | --- | --- |
    | <span data-ttu-id="10f5d-129">估計值</span><span class="sxs-lookup"><span data-stu-id="10f5d-129">Estimate</span></span> | <span data-ttu-id="10f5d-130">單價</span><span class="sxs-lookup"><span data-stu-id="10f5d-130">Price per unit</span></span> | <span data-ttu-id="10f5d-131">根據類別價格明細</span><span class="sxs-lookup"><span data-stu-id="10f5d-131">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="10f5d-132">依照成本</span><span class="sxs-lookup"><span data-stu-id="10f5d-132">At cost</span></span> | <span data-ttu-id="10f5d-133">0.00</span><span class="sxs-lookup"><span data-stu-id="10f5d-133">0.00</span></span> |
    | &nbsp; | <span data-ttu-id="10f5d-134">成本加成</span><span class="sxs-lookup"><span data-stu-id="10f5d-134">Markup over cost</span></span> | <span data-ttu-id="10f5d-135">0.00</span><span class="sxs-lookup"><span data-stu-id="10f5d-135">0.00</span></span> |
    | <span data-ttu-id="10f5d-136">實際</span><span class="sxs-lookup"><span data-stu-id="10f5d-136">Actual</span></span> | <span data-ttu-id="10f5d-137">單價</span><span class="sxs-lookup"><span data-stu-id="10f5d-137">Price per unit</span></span> | <span data-ttu-id="10f5d-138">根據類別價格明細</span><span class="sxs-lookup"><span data-stu-id="10f5d-138">Based on the category price line</span></span> |
    | &nbsp; | <span data-ttu-id="10f5d-139">依照成本</span><span class="sxs-lookup"><span data-stu-id="10f5d-139">At cost</span></span> | <span data-ttu-id="10f5d-140">根據相關成本實際值</span><span class="sxs-lookup"><span data-stu-id="10f5d-140">Based on the related cost actual</span></span> |
    | &nbsp; | <span data-ttu-id="10f5d-141">成本加成</span><span class="sxs-lookup"><span data-stu-id="10f5d-141">Markup over cost</span></span> | <span data-ttu-id="10f5d-142">在相關成本實際值的單位成本費率上套用類別價格明細所定義的加成</span><span class="sxs-lookup"><span data-stu-id="10f5d-142">By applying a markup as defined by the category price line on the unit cost rate of the related cost actual</span></span> |

4. <span data-ttu-id="10f5d-143">如果系統無法找到相符的 **類別** 和 **單位** 欄位值，則銷售費率預設為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="10f5d-143">If the system is unable to match the **Category** and **Unit** field values, the sales rate defaults to zero(0).</span></span>
