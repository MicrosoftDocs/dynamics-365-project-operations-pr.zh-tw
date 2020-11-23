---
title: 資源估計值
description: 本主題提供有關如何在 Project Operations 中計算資源估計值的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 454b8931db53739a7bc19364911109802a1ed087
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4127340"
---
# <a name="resource-estimates"></a><span data-ttu-id="71721-103">資源估計值</span><span class="sxs-lookup"><span data-stu-id="71721-103">Resource estimates</span></span>

<span data-ttu-id="71721-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="71721-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="71721-105">資源估計值來自分工結構圖中定義的分時期投入量以及適用的定價維度。</span><span class="sxs-lookup"><span data-stu-id="71721-105">Resource estimates come from time-phased effort that is defined in the work breakdown structure along with applicable pricing dimensions.</span></span> <span data-ttu-id="71721-106">計算方式通常是 **每個角色的每小時費率 x 時數**。</span><span class="sxs-lookup"><span data-stu-id="71721-106">Typically, the calculation is **rate/hr for each role x hours.**</span></span> <span data-ttu-id="71721-107">每個資源的分時期投入量都會儲存在資源指派記錄中。</span><span class="sxs-lookup"><span data-stu-id="71721-107">The time-phased effort for each resource is stored in the resource assignment record.</span></span> <span data-ttu-id="71721-108">定價會儲存在預先定義的價目表中。</span><span class="sxs-lookup"><span data-stu-id="71721-108">The pricing is stored in a pre-defined price list.</span></span> <span data-ttu-id="71721-109">單位轉換是根據適用的價目表來套用。</span><span class="sxs-lookup"><span data-stu-id="71721-109">Unit conversion is applied based on the applicable price list.</span></span>

![資源估計值](./media/navigation12.png)

## <a name="default-cost-price-and-cost-currency"></a><span data-ttu-id="71721-111">預設成本價與成本貨幣</span><span class="sxs-lookup"><span data-stu-id="71721-111">Default cost price and cost currency</span></span>

<span data-ttu-id="71721-112">成本價預設會使用組織單位。</span><span class="sxs-lookup"><span data-stu-id="71721-112">Cost prices are defaulted from the Organizational Unit.</span></span>

## <a name="default-bill-rate-and-sales-currency"></a><span data-ttu-id="71721-113">預設帳單費率與銷售貨幣</span><span class="sxs-lookup"><span data-stu-id="71721-113">Default bill rate and sales currency</span></span>

<span data-ttu-id="71721-114">每筆交易會套用售價一次。</span><span class="sxs-lookup"><span data-stu-id="71721-114">Sales prices are applied once per deal.</span></span> <span data-ttu-id="71721-115">銷售價目表的階層預設如下：</span><span class="sxs-lookup"><span data-stu-id="71721-115">The hierarchy for sale price list defaulting is as follows:</span></span>

1. <span data-ttu-id="71721-116">組織</span><span class="sxs-lookup"><span data-stu-id="71721-116">Organization</span></span>
2. <span data-ttu-id="71721-117">客戶</span><span class="sxs-lookup"><span data-stu-id="71721-117">Customer</span></span>
3. <span data-ttu-id="71721-118">報價/合約</span><span class="sxs-lookup"><span data-stu-id="71721-118">Quote/contract</span></span>
