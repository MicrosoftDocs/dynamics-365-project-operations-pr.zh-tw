---
title: 預約與指派的比較
description: 本主題提供有關資源預約與資源指派之間差異的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fa99783e52dbcdeaf80bbfd03df0f458f86b5e99
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072845"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="f5a2d-103">預約與指派的比較</span><span class="sxs-lookup"><span data-stu-id="f5a2d-103">Bookings vs assignments</span></span>

<span data-ttu-id="f5a2d-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="f5a2d-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f5a2d-105">預約是為專案進行的已確認或未確認資源配置。</span><span class="sxs-lookup"><span data-stu-id="f5a2d-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="f5a2d-106">已確認預約會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="f5a2d-106">Hard bookings consume a resource's capacity.</span></span> 

<span data-ttu-id="f5a2d-107">指派是在專案排程中對專案工作的資源指派。</span><span class="sxs-lookup"><span data-stu-id="f5a2d-107">Assignments are the assignment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="f5a2d-108">資源可以是實際或一般資源。</span><span class="sxs-lookup"><span data-stu-id="f5a2d-108">The resources can be real or generic.</span></span> 

<span data-ttu-id="f5a2d-109">對於實際資源，預約與指派最好要一致，因為兩者並無差別。</span><span class="sxs-lookup"><span data-stu-id="f5a2d-109">Ideally, for real resources, the bookings and assignments should agree, because they don't differ.</span></span> <span data-ttu-id="f5a2d-110">不過，Microsoft Dynamics Project Operations 不會強制這樣的一致性。</span><span class="sxs-lookup"><span data-stu-id="f5a2d-110">However, Microsoft Dynamics Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="f5a2d-111">**協調** 檢視表會向專案經理顯示資源預約與指派不一致的地方。</span><span class="sxs-lookup"><span data-stu-id="f5a2d-111">The **Reconciliation** view shows a project manager places where a resource's bookings and assignments don't agree.</span></span>
