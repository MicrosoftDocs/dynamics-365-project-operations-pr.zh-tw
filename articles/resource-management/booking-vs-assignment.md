---
title: 預約與指派的比較
description: 本主題提供有關資源預約與資源指派之間差異的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 8fe6937dfdfe137f28917c16da1d7dc6155284ae
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4130208"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="bf3b2-103">預約與指派的比較</span><span class="sxs-lookup"><span data-stu-id="bf3b2-103">Bookings vs assignments</span></span>

<span data-ttu-id="bf3b2-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="bf3b2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="bf3b2-105">預約是為專案進行的已確認或未確認資源配置。</span><span class="sxs-lookup"><span data-stu-id="bf3b2-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="bf3b2-106">已確認預約會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="bf3b2-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="bf3b2-107">預約代表團隊的組織概念，以便其了解資源如何參與各種專案。</span><span class="sxs-lookup"><span data-stu-id="bf3b2-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="bf3b2-108">Dynamics 365 Project Operations 將預約視為專案層級概念。</span><span class="sxs-lookup"><span data-stu-id="bf3b2-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="bf3b2-109">與預約不同的是，指派是資源對專案排程中工作的承諾用量。</span><span class="sxs-lookup"><span data-stu-id="bf3b2-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="bf3b2-110">資源可以具名或一般資源。</span><span class="sxs-lookup"><span data-stu-id="bf3b2-110">The resources can be named or generic.</span></span> 

<span data-ttu-id="bf3b2-111">資源預約的加總通常等於資源在一個或多個工作中的指派總和。</span><span class="sxs-lookup"><span data-stu-id="bf3b2-111">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="bf3b2-112">不過，Project Operations 不會強制這樣的一致性。</span><span class="sxs-lookup"><span data-stu-id="bf3b2-112">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="bf3b2-113">**協調** 檢視表會向專案經理顯示資源預約與指派不一致的地方。</span><span class="sxs-lookup"><span data-stu-id="bf3b2-113">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>
