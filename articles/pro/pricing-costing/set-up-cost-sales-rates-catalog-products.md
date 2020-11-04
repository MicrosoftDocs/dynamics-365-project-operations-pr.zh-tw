---
title: 設定產品類別目錄產品的成本及銷售費率
description: 本主題提供有關如何為產品類別目錄中的項目設定成本及銷售費率的資訊。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d5178a9143536bf4b2573403125325017861cdd5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073063"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products"></a><span data-ttu-id="7de18-103">設定產品類別目錄產品的成本及銷售費率</span><span class="sxs-lookup"><span data-stu-id="7de18-103">Set up cost and sales rates for catalog products</span></span>

<span data-ttu-id="7de18-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="7de18-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="7de18-105">在 Dynamics 365 Project Operations 中設定產品類別目錄項目的定價，與在 Dynamics 365 Sales 中設定的方式相同。</span><span class="sxs-lookup"><span data-stu-id="7de18-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="7de18-106">由於無法在 Project Operations 中估計或使用專案上的產品，因此不需要在報價和合約的專案價目表上設定產品類別目錄價格。</span><span class="sxs-lookup"><span data-stu-id="7de18-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="7de18-107">產品類別目錄價格必須在報價、合約或客戶的 **產品價格** 欄位中進行設定。</span><span class="sxs-lookup"><span data-stu-id="7de18-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="7de18-108">不要在這些實體的專案價目表中設定產品類別目錄價格。</span><span class="sxs-lookup"><span data-stu-id="7de18-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="7de18-109">專案價目表是 Project Operations 所專有。</span><span class="sxs-lookup"><span data-stu-id="7de18-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="7de18-110">其中有可將價目表從報價複製到合約的應用程式特定商務邏輯。</span><span class="sxs-lookup"><span data-stu-id="7de18-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="7de18-111">結果是合約特定專案價目表。</span><span class="sxs-lookup"><span data-stu-id="7de18-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="7de18-112">如果報價的專案價目表變得太大，則複製作業可能會延遲報價成交程序。</span><span class="sxs-lookup"><span data-stu-id="7de18-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="7de18-113">不會複製產品價目表，以在合約上建立自訂價目表。</span><span class="sxs-lookup"><span data-stu-id="7de18-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="7de18-114">這表示產品價目表不會影響報價成交程序的效能。</span><span class="sxs-lookup"><span data-stu-id="7de18-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
