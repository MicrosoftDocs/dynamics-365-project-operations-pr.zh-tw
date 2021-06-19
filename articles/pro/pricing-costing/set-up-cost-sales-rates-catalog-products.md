---
title: 設定產品類別目錄產品的成本及銷售費率 - 精簡
description: 本主題提供有關如何為產品類別目錄中的項目設定成本及銷售費率的資訊。
author: rumant
ms.date: 10/09/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4995859696c844e99593139f63dffbf86a52f2f0
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6004303"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="42a4d-103">設定產品類別目錄產品的成本及銷售費率 - 精簡</span><span class="sxs-lookup"><span data-stu-id="42a4d-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="42a4d-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="42a4d-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="42a4d-105">在 Dynamics 365 Project Operations 中設定產品類別目錄項目定價的方式與在 Dynamics 365 Sales 中的相同。</span><span class="sxs-lookup"><span data-stu-id="42a4d-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="42a4d-106">在 Project Operations 中，無法在專案上估計或使用產品，因此不需要在報價和合約的專案價目表中設定產品類別目錄價格。</span><span class="sxs-lookup"><span data-stu-id="42a4d-106">In Project Operations, products can't be estimated or used on projects, so product catalog prices don't need to be set on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="42a4d-107">請使用報價、合約或客戶的 **產品價格** 欄位來設定產品類別目錄價格。</span><span class="sxs-lookup"><span data-stu-id="42a4d-107">Use the **Product Price** field of a quote, contract, or account to set up product catalog prices.</span></span> <span data-ttu-id="42a4d-108">不要在專案價目表中設定產品類別目錄價格。</span><span class="sxs-lookup"><span data-stu-id="42a4d-108">Don't set up product catalog prices in the project price lists.</span></span> <span data-ttu-id="42a4d-109">專案價目表是 Project Operations 所專有。</span><span class="sxs-lookup"><span data-stu-id="42a4d-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="42a4d-110">應用程式特定的商務規則會將報價的價目表複製到合約。</span><span class="sxs-lookup"><span data-stu-id="42a4d-110">Application-specific business logic copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="42a4d-111">結果是合約特定專案價目表。</span><span class="sxs-lookup"><span data-stu-id="42a4d-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="42a4d-112">如果報價的專案價目表變得太大，則複製作業可能會延遲報價成交程序。</span><span class="sxs-lookup"><span data-stu-id="42a4d-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="42a4d-113">不會複製產品價目表，以在合約上建立自訂價目表。</span><span class="sxs-lookup"><span data-stu-id="42a4d-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="42a4d-114">因為沒有涉及複製，報價程序的效能不受影響。</span><span class="sxs-lookup"><span data-stu-id="42a4d-114">Because there's no copying involved, the performance of the quote process isn't affected.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]