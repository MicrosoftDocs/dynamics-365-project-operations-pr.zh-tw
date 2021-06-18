---
title: 解析估計值及實際值的成本價
description: 本主題提供有關如何解析估計值及實際值成本價的資訊。
author: rumant
ms.date: 04/09/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d81b521acbfd97127cf056bd41a3249c01108374
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6001371"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a><span data-ttu-id="46c36-103">解析估計值及實際值的成本價</span><span class="sxs-lookup"><span data-stu-id="46c36-103">Resolving cost prices for estimates and actuals</span></span>

<span data-ttu-id="46c36-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="46c36-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="46c36-105">為了解析成本價以及估計值與實際值的成本價目表，系統會使用相關專案的 **日期**、**貨幣** 和 **合約單位** 欄位中的資訊。</span><span class="sxs-lookup"><span data-stu-id="46c36-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="46c36-106">解析成本價目表之後，應用程式會解析成本費率。</span><span class="sxs-lookup"><span data-stu-id="46c36-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="46c36-107">解析時間實際及估計明細的成本費率</span><span class="sxs-lookup"><span data-stu-id="46c36-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="46c36-108">時間的估計明細是指專案上時間和資源指派的報價及合約服務內容詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46c36-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="46c36-109">解析成本價目表之後，系統會使用時間估計明細上的 **角色**、**資源供應公司** 和 **資源分配單位** 欄位，來比對價目表中的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="46c36-109">After a cost price list is resolved, the system uses the **Role**, **Resourcing Company**, and **Resourcing Unit** fields on the estimate line for Time to match against the role price lines in the price list.</span></span> <span data-ttu-id="46c36-110">這項比對作業假設您正在對人力成本使用現成可用的定價維度。</span><span class="sxs-lookup"><span data-stu-id="46c36-110">This match assumes that you are using out-of-the-box pricing dimensions for labor cost.</span></span> <span data-ttu-id="46c36-111">如果您將系統設定成比對排除或附加 **角色**、**資源供應公司** 及 **資源分配單位** 的欄位，則會使用不同的組合來擷取相符的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="46c36-111">If you configured the system to match fields instead of, or in addition to **Role**, **Resourcing Company**, and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="46c36-112">如果應用程式找到具有 **角色**、**資源供應公司** 及 **資源分配單** 位組合成本費率的角色價格明細，那就是預設成本費率。</span><span class="sxs-lookup"><span data-stu-id="46c36-112">If the application finds a role price line that has a cost rate for the **Role**, **Resourcing Company**, and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="46c36-113">如果應用程式找不到完全符合 **角色**、**資源供應公司** 與 **資源分配單位** 組合值的項目，則會擷取角色值符合但在 **資源分配單位** 及 **資源供應公司** 值為 Null 的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="46c36-113">If the application can't exactly match the combination of **Role**, **Resourcing Company**, and **Resourcing Unit** values, it will retrieve role price lines with a matching role value, but have null values for **Resourcing Unit** and **Resourcing Company**.</span></span> <span data-ttu-id="46c36-114">找到角色價格值符合的相符角色價格記錄之後，成本費率會根據該記錄設定預設值。</span><span class="sxs-lookup"><span data-stu-id="46c36-114">After a matching role price record with matching role price value is found, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="46c36-115">如果您設定不同的 **角色**、**資源供應公司** 及 **資源分配單位** 優先順序，或者您有其他較高優先順序的維度，則此行為也會相應變更。</span><span class="sxs-lookup"><span data-stu-id="46c36-115">If you configure a different prioritization of **Role**, **Resourcing Company**, and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="46c36-116">系統會擷取其值依序符合每一個價格維度值 (這些維度中值為 Null 的資料列，其優先順序排在最後) 的角色價格記錄。</span><span class="sxs-lookup"><span data-stu-id="46c36-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last in the priority order.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="46c36-117">解析費用實際及估計明細的成本費率</span><span class="sxs-lookup"><span data-stu-id="46c36-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="46c36-118">費用的估計明細是指專案上費用和費用估計明細的報價及合約服務內容詳細資料。</span><span class="sxs-lookup"><span data-stu-id="46c36-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="46c36-119">解析成本價目表之後，系統會使用費用估計明細上的 **類別** 與 **單位** 欄位組合，來比對解析後價目表中的 **類別價格** 明細。</span><span class="sxs-lookup"><span data-stu-id="46c36-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the estimate line for an expense to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="46c36-120">如果系統找到具有 **類別** 與 **單位** 欄位組合成本費率的類別價格明細，則預設使用該成本費率。</span><span class="sxs-lookup"><span data-stu-id="46c36-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="46c36-121">如果系統找不到相符的 **類別** 與 **單位** 值，或者可以找到相符類別價格明細，但定價方式並非 **單價**，則成本費率預設為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="46c36-121">If the system can't match the **Category** and **Unit** values, or if it is able to find a matching category price line but the pricing method is not **Price Per Unit**, the cost rate is defaulted to zero(0).</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a><span data-ttu-id="46c36-122">解析材料實際及估計明細上的成本費率</span><span class="sxs-lookup"><span data-stu-id="46c36-122">Resolving cost rates on actual and estimate lines for material</span></span>

<span data-ttu-id="46c36-123">材料估計明細是指材料的報價與合約服務內容詳細資料以及專案中的材料估計明細。</span><span class="sxs-lookup"><span data-stu-id="46c36-123">Estimate lines for material refer to the quote and contract line details for materials and the material estimate lines on a project.</span></span>

<span data-ttu-id="46c36-124">解析成本價目表之後，系統會使用材料估計值估計明細上的 **產品** 與 **單位** 欄位組合，來比對所解析價目表上的 **價目表項目** 明細。</span><span class="sxs-lookup"><span data-stu-id="46c36-124">After a cost price list is resolved, the system uses a combination of the **Product** and **Unit** fields on the estimate line for a material estimate to match against the **Price List Items** lines on the resolved price list.</span></span> <span data-ttu-id="46c36-125">如果系統找到具有 **產品** 與 **單位** 欄位組合成本費率的產品價格明細，則以該成本費率為預設值。</span><span class="sxs-lookup"><span data-stu-id="46c36-125">If the system finds a product price line that has a cost rate for the **Product** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="46c36-126">如果系統找不到符合 **產品** 和 **單位** 值的項目，則單位成本預設為零。</span><span class="sxs-lookup"><span data-stu-id="46c36-126">If the system can't match the **Product** and **Unit** values, the unit cost defaults to zero.</span></span> <span data-ttu-id="46c36-127">如果有相符的價目表項目明細，也會進行這樣的預設，但定價方式是根據產品中未定義的標準成本或目前成本而定。</span><span class="sxs-lookup"><span data-stu-id="46c36-127">This default will also happen if there is a matching price list item line, but the pricing method is based on a standard cost or current cost that isn't defined in the product.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
