---
title: 解析專案估計值及實際值的成本價
description: 本主題提供有關如何在專案估計值和實際值上解析成本價的資訊。
author: rumant
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 6b42bc97251aec7259d314fe51b3a012edf597aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004386"
---
# <a name="resolve-cost-prices-on-project-estimates-and-actuals"></a><span data-ttu-id="36e66-103">解析專案估計值及實際值的成本價</span><span class="sxs-lookup"><span data-stu-id="36e66-103">Resolve cost prices on project estimates and actuals</span></span> 

<span data-ttu-id="36e66-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="36e66-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="36e66-105">為了解析成本價以及估計值與實際值的成本價目表，系統會使用相關專案的 **日期**、**貨幣** 和 **合約單位** 欄位中的資訊。</span><span class="sxs-lookup"><span data-stu-id="36e66-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="36e66-106">解析成本價目表之後，應用程式會解析成本費率。</span><span class="sxs-lookup"><span data-stu-id="36e66-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="36e66-107">解析時間實際及估計明細的成本費率</span><span class="sxs-lookup"><span data-stu-id="36e66-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="36e66-108">時間的估計明細是指專案上時間和資源指派的報價及合約服務內容詳細資料。</span><span class="sxs-lookup"><span data-stu-id="36e66-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="36e66-109">解析成本價目表之後，時間估計明細上的 **角色** 和 **資源分配單位** 欄位會與價目表中的角色價格明細進行比對。</span><span class="sxs-lookup"><span data-stu-id="36e66-109">After a cost price list is resolved, the **Role** and **Resourcing Unit** fields on the estimate line for Time are matched against the role price lines in the price list.</span></span> <span data-ttu-id="36e66-110">這種比對假設您是使用標準定價維度來計算人力成本。</span><span class="sxs-lookup"><span data-stu-id="36e66-110">This match assumes that you're using the standard pricing dimensions for labor cost.</span></span> <span data-ttu-id="36e66-111">如果您將系統設定成比對排除或附加 **角色** 和 **資源分配單位** 的欄位，則會使用不同的組合來擷取相符的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="36e66-111">If you configured the system to match fields instead of, or in addition to **Role** and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="36e66-112">如果應用程式找到具有 **角色** 與 **資源分配單位** 組合成本費率的角色價格明細，那就是預設成本費率。</span><span class="sxs-lookup"><span data-stu-id="36e66-112">If the application finds a role price line that has a cost rate for the **Role** and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="36e66-113">如果應用程式找不到與 **角色** 及 **資源分配單位** 值相符的項目，則會擷取具有相符角色但 **資源分配單位** 值為 Null 的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="36e66-113">If the application can't match the **Role** and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="36e66-114">找到相符的角色價格記錄之後，成本費率將預設為該記錄中的預設值。</span><span class="sxs-lookup"><span data-stu-id="36e66-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="36e66-115">如果您設定不同的 **角色** 及 **資源分配單位** 優先順序，或者您有其他較高優先順序的維度，則此行為也會相應變更。</span><span class="sxs-lookup"><span data-stu-id="36e66-115">If you configure a different prioritization of **Role** and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="36e66-116">系統會依照以那些有列值為 Null 之定價維度居後的優先順序，擷取其值符合每個定價維度值的角色價格記錄。</span><span class="sxs-lookup"><span data-stu-id="36e66-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="36e66-117">解析費用實際及估計明細的成本費率</span><span class="sxs-lookup"><span data-stu-id="36e66-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="36e66-118">費用的估計明細是指專案上費用和費用估計明細的報價及合約服務內容詳細資料。</span><span class="sxs-lookup"><span data-stu-id="36e66-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="36e66-119">解析成本價目表之後，系統會使用費用估計明細上的 **類別** 和 **單位** 欄位組合，來與已解析價目表上的 **類別價格** 明細進行比對。</span><span class="sxs-lookup"><span data-stu-id="36e66-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the expense estimate line to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="36e66-120">如果系統找到具有 **類別** 與 **單位** 欄位組合成本費率的類別價格明細，則預設使用該成本費率。</span><span class="sxs-lookup"><span data-stu-id="36e66-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="36e66-121">如果系統找不到與 **類別** 及 **單位** 值相符的項目，或者找得到相符的類別價格明細，但定價方式不是 **單價** 時，成本費率會預設為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="36e66-121">If the system can't match the **Category** and **Unit** values, or if it's able to find a matching category price line but the pricing method isn't **Price Per Unit**, the cost rate defaults to zero(0).</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-material"></a><span data-ttu-id="36e66-122">解析材料實際及估計明細上的成本費率</span><span class="sxs-lookup"><span data-stu-id="36e66-122">Resolving cost rates on actual and estimate lines for Material</span></span>

<span data-ttu-id="36e66-123">材料的估計明細是指材料的報價與合約服務內容詳細資料以及專案中的材料估計明細。</span><span class="sxs-lookup"><span data-stu-id="36e66-123">Estimate lines for Material refer to the quote and contract line details for materials and the material estimate lines on a project.</span></span>

<span data-ttu-id="36e66-124">解析成本價目表之後，系統會使用材料估計值估計明細上的 **產品** 與 **單位** 欄位組合，來比對所解析價目表上的 **價目表項目** 明細。</span><span class="sxs-lookup"><span data-stu-id="36e66-124">After a cost price list is resolved, the system uses a combination of the **Product** and **Unit** fields on the estimate line for a material estimate to match against the **Price List Items** lines on the resolved price list.</span></span> <span data-ttu-id="36e66-125">如果系統找到具有 **產品** 與 **單位** 欄位組合成本費率的產品價格明細，則以該成本費率為預設值。</span><span class="sxs-lookup"><span data-stu-id="36e66-125">If the system finds a product price line that has a cost rate for the **Product** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="36e66-126">如果系統找不到符合 **產品** 與 **單位** 值的項目，或是找得到相符的價目表項目明細，但定價方式是根據標準成本或目前成本，而產品中並未定義這任一成本時，單位成本會預設為零。</span><span class="sxs-lookup"><span data-stu-id="36e66-126">If the system can't match the **Product** and **Unit** values, or if it's able to find a matching price list item line but the pricing method is based on Standard cost or Current cost and neither is defined on the product, the unit cost defaults to zero.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
