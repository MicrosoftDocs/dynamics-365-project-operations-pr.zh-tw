---
title: 關閉定價維度
description: 本主題顯示如何設定 Project Service 解決方案中的定價維度。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/06/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 689e5a8d-e39a-471d-a6c4-7e2fc3bb5590
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: 5cf2cd86fb1eba50c8e08b2bd624669ab0b1deb3
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749953"
---
# <a name="turn-off-a-pricing-dimension"></a><span data-ttu-id="a5994-103">關閉定價維度</span><span class="sxs-lookup"><span data-stu-id="a5994-103">Turn off a pricing dimension</span></span>

<span data-ttu-id="a5994-104">您可能每隔幾年就需要檢閱並更新您的定價策略。</span><span class="sxs-lookup"><span data-stu-id="a5994-104">You may need to review and update your pricing strategy every few years.</span></span> <span data-ttu-id="a5994-105">任何您所進行的更新可能都需要您關閉現有的定價維度，並建立新的定價維度。</span><span class="sxs-lookup"><span data-stu-id="a5994-105">Any updates you make might require that you turn off an existing pricing dimension and create a new one.</span></span> <span data-ttu-id="a5994-106">例如，您可能先前已依**角色**定價，但現在決定依據**工作經驗**進行定價。</span><span class="sxs-lookup"><span data-stu-id="a5994-106">For example, you may have previously priced by **Role**, but now you have decided to price by **Work Experience**.</span></span> <span data-ttu-id="a5994-107">這可能要求您必須關閉以**角色**為定價維度的設定，並將**工作經驗**建立為新的定價維度。</span><span class="sxs-lookup"><span data-stu-id="a5994-107">This may require you to turn off **Role** as a pricing dimension and create **Work Expereince** as a new pricing dimension.</span></span> 

<span data-ttu-id="a5994-108">關閉定價維度 (不論是預設還是自訂否) 的動作，都可以藉由將定價維度的**適用於成本**和**適用於銷售**欄位設定為**否**來完成。</span><span class="sxs-lookup"><span data-stu-id="a5994-108">Turning off a pricing dimension, regardless if it is out-of-the-box or custom, can be done by setting the **Applicable to Cost** and **Applicable to Sales** fields of the Pricing Dimension to **No**.</span></span>

<span data-ttu-id="a5994-109">不過，這樣做時，可能會收到下列錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="a5994-109">However, when you do this, you might receive the following error message.</span></span>

![關閉定價維度時可能發生商務程序錯誤](media/Business-Process-Error.png)


<span data-ttu-id="a5994-111">此錯誤訊息表示存在先前為所要關閉維度設定的價格記錄。</span><span class="sxs-lookup"><span data-stu-id="a5994-111">This error message indicates that there are price records that were previously set up for the dimension that is being turned off.</span></span> <span data-ttu-id="a5994-112">必須先刪除參照該維度的所有**角色價格**和**角色價格加成**記錄，才能將維度的適用性設為**否**。</span><span class="sxs-lookup"><span data-stu-id="a5994-112">All **Role Price** and **Role Price Markup** records that refer to a dimension must be deleted before the dimension’s applicability can be to set to **No**.</span></span> <span data-ttu-id="a5994-113">此規則適用於內建定價維度以及任何您可能已建立的自訂定價維度。</span><span class="sxs-lookup"><span data-stu-id="a5994-113">This rule applies to both out-of-the-box pricing dimensions and any custom pricing dimensions that you may have created.</span></span> <span data-ttu-id="a5994-114">這項驗證的原因在於 Project Service 有一個限制，每個**角色價格**記錄都必須有一個唯一的維度組合。</span><span class="sxs-lookup"><span data-stu-id="a5994-114">The reason for this validation is because Project Service has a constraint that each **Role Price** record must have a unique combination of dimensions.</span></span> <span data-ttu-id="a5994-115">例如，在名為 **2018 年美國成本費率**的價目表中，您有下列**角色價格**列。</span><span class="sxs-lookup"><span data-stu-id="a5994-115">For example, on a price list called **US Cost Rates 2018**, you have the following **Role price** rows.</span></span> 

| <span data-ttu-id="a5994-116">標準職稱</span><span class="sxs-lookup"><span data-stu-id="a5994-116">Standard Title</span></span>         | <span data-ttu-id="a5994-117">組織單位</span><span class="sxs-lookup"><span data-stu-id="a5994-117">Org Unit</span></span>    |<span data-ttu-id="a5994-118">單位</span><span class="sxs-lookup"><span data-stu-id="a5994-118">Unit</span></span>   |<span data-ttu-id="a5994-119">價格</span><span class="sxs-lookup"><span data-stu-id="a5994-119">Price</span></span>  |<span data-ttu-id="a5994-120">貨幣</span><span class="sxs-lookup"><span data-stu-id="a5994-120">Currency</span></span>  |
| -----------------------|-------------|-------|-------|----------|
| <span data-ttu-id="a5994-121">系統工程師</span><span class="sxs-lookup"><span data-stu-id="a5994-121">Systems Engineer</span></span>|<span data-ttu-id="a5994-122">Contoso US</span><span class="sxs-lookup"><span data-stu-id="a5994-122">Contoso US</span></span>|<span data-ttu-id="a5994-123">Hour</span><span class="sxs-lookup"><span data-stu-id="a5994-123">Hour</span></span>| <span data-ttu-id="a5994-124">100</span><span class="sxs-lookup"><span data-stu-id="a5994-124">100</span></span>|<span data-ttu-id="a5994-125">USD</span><span class="sxs-lookup"><span data-stu-id="a5994-125">USD</span></span>|
| <span data-ttu-id="a5994-126">資深系統工程師</span><span class="sxs-lookup"><span data-stu-id="a5994-126">Senior Systems Engineer</span></span>|<span data-ttu-id="a5994-127">Contoso US</span><span class="sxs-lookup"><span data-stu-id="a5994-127">Contoso US</span></span>|<span data-ttu-id="a5994-128">Hour</span><span class="sxs-lookup"><span data-stu-id="a5994-128">Hour</span></span>| <span data-ttu-id="a5994-129">150</span><span class="sxs-lookup"><span data-stu-id="a5994-129">150</span></span>| <span data-ttu-id="a5994-130">USD</span><span class="sxs-lookup"><span data-stu-id="a5994-130">USD</span></span>|


<span data-ttu-id="a5994-131">當您關閉以**標準職稱**為定價維度的設定，而 Project Service 定價引擎搜尋價格時，它只會使用輸入內容中的**組織單位**值。</span><span class="sxs-lookup"><span data-stu-id="a5994-131">When you turn off **Standard Title** as the pricing dimension, and the Project Service pricing engine searches for a price, it will only use the **Org Unit** value from the input context.</span></span> <span data-ttu-id="a5994-132">如果輸入內容的**組織單位**是「Contoso US」，則結果並非決定性，因為這兩個列都會相符。</span><span class="sxs-lookup"><span data-stu-id="a5994-132">If the **Org Unit** of the input context is “Contoso US”, the result will be non-deterministic because both the rows will match.</span></span> <span data-ttu-id="a5994-133">為了避免這種案例，當您建立**角色價格**記錄時，Project Service 會驗證維度組合是否為唯一。</span><span class="sxs-lookup"><span data-stu-id="a5994-133">To avoid this scenario, when you create **Role Price** records, Project Service validates that the combination of dimensions is unique.</span></span> <span data-ttu-id="a5994-134">如果維度在建立**角色價格**記錄後已關閉，則可能會違反此限制。</span><span class="sxs-lookup"><span data-stu-id="a5994-134">If the dimension is turned off after the **Role Price** records are created, this constraint can be violated.</span></span> <span data-ttu-id="a5994-135">因此，關閉維度之前，必須先刪除所有已填入該維度值的**角色價格**和**角色價格加成**列。</span><span class="sxs-lookup"><span data-stu-id="a5994-135">Therefore, it is required that before you turn off a dimension, you delete all **Role Price** and **Role Price Markup** rows that have that dimension value populated.</span></span>

