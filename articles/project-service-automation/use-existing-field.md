---
title: 使用 Project Service 中現有的欄位做為定價維度
description: 本主題提供有關使用現有 Project Service 欄位做為定價維度的資訊。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: ed86e0c4-b2ea-4b3b-b9e3-cbfb3b512591
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: b280e2aeecc9d63fb65b77fad809edff817aff65
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749921"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a><span data-ttu-id="ff662-103">使用 Project Service 中現有的欄位做為定價維度</span><span class="sxs-lookup"><span data-stu-id="ff662-103">Use an existing field in Project Service as a pricing dimension</span></span>

<span data-ttu-id="ff662-104">Project Service Automation (PSA) 的**實際值**實體上有許多欄位，可以用來做為專案組織中資源型定價的定價維度。</span><span class="sxs-lookup"><span data-stu-id="ff662-104">Project Service Automation (PSA) has many fields on the **Actuals** entity that can be used as pricing dimensions for resource-based pricing in project organizations.</span></span> <span data-ttu-id="ff662-105">例如，其中一個常用的欄位是**可預約資源**。</span><span class="sxs-lookup"><span data-stu-id="ff662-105">For example, one common field is **Bookable Resource**.</span></span> <span data-ttu-id="ff662-106">可計費資源少於 20-30 個的小型公司可能會發現讓每項資源有各自特定的帳單費率與成本費率是比較簡單的方法。</span><span class="sxs-lookup"><span data-stu-id="ff662-106">Smaller companies that have fewer than 20-30 billable resources may find that having bill and cost rates specific to each resource is a simpler approach.</span></span> <span data-ttu-id="ff662-107">但是，可計費工作力 (員工人數) 會擴增，因此當資源成本和帳單費率開始隨著資源職位高升、經驗增加或取得其他技能集而改變時，要維持這種方法就會變得不切實際。</span><span class="sxs-lookup"><span data-stu-id="ff662-107">However, as the billable workforce grows, this could become unrealistic to maintain as resource cost and bill rates begin to vary as resources get promoted, gain more experience, or acquire a different skill sets.</span></span> <span data-ttu-id="ff662-108">由於這種方法對特定規模的公司仍然適用，因此請參閱主題[使用可預約資源做為定價維度](bookable-resource-pricing-dimension.md)，了解如何使用現有的 Project Service 欄位做為定價維度。</span><span class="sxs-lookup"><span data-stu-id="ff662-108">Because this approach still works for companies of a certain size, see the topic, [Use a bookable resource as a pricing dimension](bookable-resource-pricing-dimension.md) to understand how an existing Project Service field can be used as a pricing dimension.</span></span>

<span data-ttu-id="ff662-109">另一個例子是交易類別的欄位。</span><span class="sxs-lookup"><span data-stu-id="ff662-109">Another example is that of transaction category.</span></span> <span data-ttu-id="ff662-110">客戶與實作者已在 PSA 中使用交易類別來分類工作，並使用該欄位以根據工作類別來估算價格和成本。</span><span class="sxs-lookup"><span data-stu-id="ff662-110">Customers and Implementers have used the transaction category in PSA to classify work and use the field to price and cost based on the category of work.</span></span> <span data-ttu-id="ff662-111">如需詳細資訊，請參閱[使用交易類別做為定價維度](transaction-category-pricing-dimension.md)。</span><span class="sxs-lookup"><span data-stu-id="ff662-111">For more information, see [Use transaction category as a pricing dimension](transaction-category-pricing-dimension.md).</span></span>
