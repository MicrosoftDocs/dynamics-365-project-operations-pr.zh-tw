---
title: 預約與指派的比較
description: 本主題提供有關資源預約與資源指派之間差異的資訊。
author: ruhercul
ms.date: 01/08/2021
ms.topic: article
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 3c1a1003af0b23c4be44fefac0b3c4ea725f96b2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012756"
---
# <a name="bookings-vs-assignments"></a><span data-ttu-id="70619-103">預約與指派的比較</span><span class="sxs-lookup"><span data-stu-id="70619-103">Bookings vs assignments</span></span>

<span data-ttu-id="70619-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="70619-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="70619-105">預約是為專案進行的已確認或未確認資源配置。</span><span class="sxs-lookup"><span data-stu-id="70619-105">Bookings are the hard or soft allocation of resources to a project.</span></span> <span data-ttu-id="70619-106">已確認預約會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="70619-106">Hard bookings consume a resource's capacity.</span></span> <span data-ttu-id="70619-107">預約代表團隊的組織概念，以便其了解資源如何參與各種專案。</span><span class="sxs-lookup"><span data-stu-id="70619-107">Bookings represent organizational concepts for teams so that they can understand how resources will be engaged across various projects.</span></span> <span data-ttu-id="70619-108">Dynamics 365 Project Operations 將預約視為專案層級概念。</span><span class="sxs-lookup"><span data-stu-id="70619-108">Dynamics 365 Project Operations considers bookings a project-level concept.</span></span> 

<span data-ttu-id="70619-109">與預約不同的是，指派是資源對專案排程中工作的承諾用量。</span><span class="sxs-lookup"><span data-stu-id="70619-109">Unlike bookings, assignments are the commitment of resources to project tasks in the project schedule.</span></span> <span data-ttu-id="70619-110">資源可以具名或一般資源。</span><span class="sxs-lookup"><span data-stu-id="70619-110">The resources can be named or generic.</span></span>  <span data-ttu-id="70619-111">當資源需求是衍生自專案工作指派時，Project Operations 會使用資源指派的努力分佈，來建置資源需求詳細資料的分佈。</span><span class="sxs-lookup"><span data-stu-id="70619-111">When a resource requirement is derived from the project task assignments, Project Operations uses the effort contours of the resources assignment to build the contours of the resource requirement details.</span></span> <span data-ttu-id="70619-112">但是，不會保留資源指派參考。</span><span class="sxs-lookup"><span data-stu-id="70619-112">However, a refence to the resource assignments isn't maintained.</span></span> <span data-ttu-id="70619-113">對衍生自資源需求的預約進行更新不會更新任何資源指派。</span><span class="sxs-lookup"><span data-stu-id="70619-113">Updates to the bookings derived from the resource requirement don't update any resource assignments.</span></span>

<span data-ttu-id="70619-114">資源預約的加總通常等於資源在一個或多個工作中的指派總和。</span><span class="sxs-lookup"><span data-stu-id="70619-114">Typically, the sum of the bookings for a resource will equal the sum of the resource's assignments across one or many tasks.</span></span> <span data-ttu-id="70619-115">不過，Project Operations 不會強制這樣的一致性。</span><span class="sxs-lookup"><span data-stu-id="70619-115">However, Project Operations doesn't enforce this agreement.</span></span> <span data-ttu-id="70619-116">**協調** 檢視表會向專案經理顯示資源預約與指派不一致的地方。</span><span class="sxs-lookup"><span data-stu-id="70619-116">The **Reconciliation** view shows the Project manager places where a resource's bookings and assignments don't agree.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]