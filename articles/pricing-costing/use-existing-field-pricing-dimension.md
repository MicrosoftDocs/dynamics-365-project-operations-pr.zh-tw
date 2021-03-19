---
title: 做為定價維度的 Project Operations 欄位
description: 本主題提供有關在 Dynamics 365 Project Operations 中使用欄位做為定價維度的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 04b823e8237590a294ed0706e64d0ecb9d2cf56f
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274628"
---
# <a name="project-operations-fields-as-pricing-dimensions"></a><span data-ttu-id="cce44-103">做為定價維度的 Project Operations 欄位</span><span class="sxs-lookup"><span data-stu-id="cce44-103">Project Operations fields as pricing dimensions</span></span>

<span data-ttu-id="cce44-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="cce44-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cce44-105">**實際值** 實體有許多欄位可用來做為資源型定價的定價維度。</span><span class="sxs-lookup"><span data-stu-id="cce44-105">The **Actuals** entity has many fields that can be used as pricing dimensions for resource-based pricing.</span></span> <span data-ttu-id="cce44-106">例如，其中一個常用的欄位是 **可預約資源**。</span><span class="sxs-lookup"><span data-stu-id="cce44-106">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="cce44-107">可計費資源少於 20-30 個的小型公司可能會發現讓每項資源有各自特定的帳單費率與成本費率是比較簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="cce44-107">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="cce44-108">不過，隨著計費工作力擴增，資源特定費率可能會變得不切實際而無法維持。</span><span class="sxs-lookup"><span data-stu-id="cce44-108">However, as the billable workforce grows, resource-secific rates could become unrealistic to maintain.</span></span> <span data-ttu-id="cce44-109">資源成本和帳單費率會因為資源升遷、獲得更多經驗或取得一套不同的技能而開始變化。</span><span class="sxs-lookup"><span data-stu-id="cce44-109">Resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different set of skills.</span></span> 

<span data-ttu-id="cce44-110">另一個例子是交易類別的欄位。</span><span class="sxs-lookup"><span data-stu-id="cce44-110">Another example is that of transaction category.</span></span> <span data-ttu-id="cce44-111">客戶與實作者已使用交易類別將工作分類，並使用該欄位根據工作類別來估算價格和成本。</span><span class="sxs-lookup"><span data-stu-id="cce44-111">Customers and Implementers have used the transaction category to classify work and use the field to price and cost based on the category of work.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]