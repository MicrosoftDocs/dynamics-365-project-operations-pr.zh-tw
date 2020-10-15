---
title: 產品型商機明細
description: 本主題提供有關如何 Project Operations 中產品型商機明細的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 17ffcf8dc94d42102115281d281d6b553cf1fa17
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896226"
---
# <a name="product-based-opportunity-lines"></a><span data-ttu-id="e6d7a-103">產品型商機明細</span><span class="sxs-lookup"><span data-stu-id="e6d7a-103">Product-based opportunity lines</span></span>

<span data-ttu-id="e6d7a-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="e6d7a-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="e6d7a-105">產品型商機明細是商機上的明細項目。</span><span class="sxs-lookup"><span data-stu-id="e6d7a-105">Product-based opportunity lines are line items on the Opportunity.</span></span> <span data-ttu-id="e6d7a-106">這些明細會在任何其他加值服務的最終發票上提供給客戶做為相異的明細項目。</span><span class="sxs-lookup"><span data-stu-id="e6d7a-106">These lines are delivered to the customer as distinct line items on the eventual invoice without any other value-added services.</span></span> <span data-ttu-id="e6d7a-107">不會對任何相關專案的工作追蹤相關花費與耗用。</span><span class="sxs-lookup"><span data-stu-id="e6d7a-107">The associated spend and consumption isn't tracked on tasks of any related projects.</span></span>

<span data-ttu-id="e6d7a-108">產品型明細可以是類別目錄項目或目錄外產品。</span><span class="sxs-lookup"><span data-stu-id="e6d7a-108">Product-based lines can be catalog items or write-in products.</span></span> <span data-ttu-id="e6d7a-109">商機的產品型明細上大部分功能都採用 Dynamics 365 Sales 應用程式所提供的功能。</span><span class="sxs-lookup"><span data-stu-id="e6d7a-109">Most of the functionality on an Opportunity's product-based lines follows the functionality provided by the Dynamics 365 Sales application.</span></span> <span data-ttu-id="e6d7a-110">如需產品型商機明細的詳細資訊，請參閱[將產品新增至商機](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity)。</span><span class="sxs-lookup"><span data-stu-id="e6d7a-110">For more information about product-based opportunity lines, see [Add products to an opportunity](https://docs.microsoft.com/dynamics365/sales-enterprise/add-products-opportunity).</span></span>

<span data-ttu-id="e6d7a-111">一個關於專案型商機所特有產品型商機明細的概念就是**客戶預算**。</span><span class="sxs-lookup"><span data-stu-id="e6d7a-111">One concept about product-based opportunity lines that is specific to project-based opportunities is **Customer Budget**.</span></span> <span data-ttu-id="e6d7a-112">使用此欄位來追蹤客戶願意為該明細項目支付的金額。</span><span class="sxs-lookup"><span data-stu-id="e6d7a-112">Use this field to track the amount the customer is willing to pay for the line item.</span></span>

<span data-ttu-id="e6d7a-113">如果商機摘要的營收方式設定為**系統計算**，則會跨產品型與專案型明細彙總預算值，以計算估計營收。</span><span class="sxs-lookup"><span data-stu-id="e6d7a-113">If the revenue method of the Opportunity summary is set to **System Calculated**, the customer budget values across product- and project-based lines are summarized to calculate the estimated revenue.</span></span>
