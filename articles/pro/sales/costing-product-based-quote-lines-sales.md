---
title: 計算產品型報價明細的成本
description: 本主題提供有關將成本價套用至產品型報價明細的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: d21ab159294cac66ffeb8abcf0943b4babd7b360
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4118913"
---
# <a name="costing-product-based-quote-lines"></a><span data-ttu-id="a2b0a-103">計算產品型報價明細的成本</span><span class="sxs-lookup"><span data-stu-id="a2b0a-103">Costing product-based quote lines</span></span>

<span data-ttu-id="a2b0a-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="a2b0a-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="a2b0a-105">Dynamics 365 Project Operations 中的產品報價明細也會有 **成本價** 欄位。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-105">Product-based quote lines in Dynamics 365 Project Operations also have a **Cost Price** field.</span></span> <span data-ttu-id="a2b0a-106">此欄位會用來追蹤報價明細上的產品成本價，並用於進行下游續獲利率計算。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-106">This field is used to track the cost price for the product on the quote line and for downstream profitability calculations.</span></span>

<span data-ttu-id="a2b0a-107">建立產品類別目錄產品的產品型報價明細時，產品型報價明細的成本預設會使用產品類別目錄中的 **標準成本** 欄位。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-107">When a product-based quote line is created for a catalog product, the cost of the product-based quote line is defaulted from the **Standard Cost** field in the product catalog.</span></span> <span data-ttu-id="a2b0a-108">產品類別目錄中的標準成本欄位是以組織的基準貨幣來設定。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-108">The standard cost field in the product catalog is set up in the Organization's base currency.</span></span> <span data-ttu-id="a2b0a-109">產品型報價明細上的預設單位成本會轉換為報價上的銷售貨幣。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-109">The default unit cost on the product-based quote line is converted to the sales currency on the quote.</span></span>

## <a name="unit-cost-on-a-product-based-quote-line"></a><span data-ttu-id="a2b0a-110">產品型報價明細的單位成本</span><span class="sxs-lookup"><span data-stu-id="a2b0a-110">Unit cost on a product-based quote line</span></span>

<span data-ttu-id="a2b0a-111">產品型報價明細上設有單位成本的目的是為了讓每次銷售的產品各有不同的成本。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-111">The purpose of having a unit cost on a product-based quote line is to allow for different costs for a product for each sale.</span></span> <span data-ttu-id="a2b0a-112">這不是常見的案例，但是產品的成本有時可能會由供應商視最終銷售的客戶而定打折扣。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-112">This is not a typical scenario, but sometimes the cost of the product may be discounted by the supplier depending on the customer of the final sale.</span></span>

<span data-ttu-id="a2b0a-113">例如：</span><span class="sxs-lookup"><span data-stu-id="a2b0a-113">For example:</span></span>

<span data-ttu-id="a2b0a-114">Fabrikam Robotics 正在 A Datum Corporation 的裝配線上安裝機器人手臂。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-114">Fabrikam Robotics is installing robotic arms at A Datum Corporation's assembly lines.</span></span> <span data-ttu-id="a2b0a-115">Fabrikam 提供安裝服務，但機器人手臂是從 Trey Robotics 取得。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-115">Fabrikam provides installation services but the robotic arms are procured from Trey robotics.</span></span> <span data-ttu-id="a2b0a-116">如果在 A Datum Corporation 安裝機器人手臂會為 Trey 的機器人手臂開拓新市場，Trey 可能會向 Fabrikam 提供這筆交易的特殊折扣。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-116">If the installation of robotic arms at A Datum Corporation opens a new industry vertical for Trey's robotic arms, Trey could give a special discount for this deal to Fabrikam.</span></span>

<span data-ttu-id="a2b0a-117">在此情況下，Fabrikam 會為機器人手臂建立產品型報價明細，並為此報價輸入每單位成本的特價優惠。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-117">In this case, Fabrikam will create product-based quote line for Robotic Arms and input a special per unit cost for this quote.</span></span> <span data-ttu-id="a2b0a-118">這項成本與 Trey 機器人手臂的標準成本不同。</span><span class="sxs-lookup"><span data-stu-id="a2b0a-118">This cost is different from the standard cost of Trey Robotic Arms.</span></span>
