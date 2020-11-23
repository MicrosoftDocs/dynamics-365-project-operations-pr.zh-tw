---
title: 設定產品類別目錄產品的成本及銷售費率 - 精簡
description: 本主題提供有關如何為產品類別目錄中的項目設定成本及銷售費率的資訊。
author: rumant
manager: Annbe
ms.date: 10/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 135b182af73bdab7a3520589431332ad059ec497
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2020
ms.locfileid: "4176691"
---
# <a name="set-up-cost-and-sales-rates-for-catalog-products---lite"></a><span data-ttu-id="41e2a-103">設定產品類別目錄產品的成本及銷售費率 - 精簡</span><span class="sxs-lookup"><span data-stu-id="41e2a-103">Set up cost and sales rates for catalog products - lite</span></span>

<span data-ttu-id="41e2a-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="41e2a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="41e2a-105">在 Dynamics 365 Project Operations 中設定產品類別目錄項目的定價，與在 Dynamics 365 Sales 中設定的方式相同。</span><span class="sxs-lookup"><span data-stu-id="41e2a-105">Setting up pricing for product catalog items in Dynamics 365 Project Operations is the same as in Dynamics 365 Sales.</span></span>

<span data-ttu-id="41e2a-106">由於無法在 Project Operations 中估計或使用專案上的產品，因此不需要在報價和合約的專案價目表上設定產品類別目錄價格。</span><span class="sxs-lookup"><span data-stu-id="41e2a-106">Because products can't be estimated or used on projects in Project Operations, there is no need to set product catalog prices on project price lists for quotes and contracts.</span></span>

<span data-ttu-id="41e2a-107">產品類別目錄價格必須在報價、合約或客戶的 **產品價格** 欄位中進行設定。</span><span class="sxs-lookup"><span data-stu-id="41e2a-107">Product catalog prices should be set up in the **Product Price** field of a quote, contract, or account.</span></span> <span data-ttu-id="41e2a-108">不要在這些實體的專案價目表中設定產品類別目錄價格。</span><span class="sxs-lookup"><span data-stu-id="41e2a-108">Don't set up product catalog prices in the project price lists for these entities.</span></span> <span data-ttu-id="41e2a-109">專案價目表是 Project Operations 所專有。</span><span class="sxs-lookup"><span data-stu-id="41e2a-109">Project price lists are exclusive to Project Operations.</span></span> <span data-ttu-id="41e2a-110">其中有可將價目表從報價複製到合約的應用程式特定商務邏輯。</span><span class="sxs-lookup"><span data-stu-id="41e2a-110">There is application-specific business logic that copies the price lists from a quote to a contract.</span></span> <span data-ttu-id="41e2a-111">結果是合約特定專案價目表。</span><span class="sxs-lookup"><span data-stu-id="41e2a-111">The result is a contract-specific project price list.</span></span> <span data-ttu-id="41e2a-112">如果報價的專案價目表變得太大，則複製作業可能會延遲報價成交程序。</span><span class="sxs-lookup"><span data-stu-id="41e2a-112">The copy operation can delay the quote win process if the project price list on the quote gets too large.</span></span> <span data-ttu-id="41e2a-113">不會複製產品價目表，以在合約上建立自訂價目表。</span><span class="sxs-lookup"><span data-stu-id="41e2a-113">Product price lists aren't copied to create custom price lists on contracts.</span></span> <span data-ttu-id="41e2a-114">這表示產品價目表不會影響報價成交程序的效能。</span><span class="sxs-lookup"><span data-stu-id="41e2a-114">This means that product price lists don't impact the performance of the quote win process.</span></span>
