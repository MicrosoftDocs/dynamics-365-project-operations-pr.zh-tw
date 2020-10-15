---
title: 排程小幫手概觀
description: 本主題提供有關使用排程小幫手來預約資源的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: da551e805f395e466952df1dbb7d193bdddba358
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907936"
---
# <a name="schedule-assistant-overview"></a><span data-ttu-id="f31dd-103">排程小幫手概觀</span><span class="sxs-lookup"><span data-stu-id="f31dd-103">Schedule assistant overview</span></span>

<span data-ttu-id="f31dd-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="f31dd-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="f31dd-105">排程小幫手會根據專案經理定義的需求來預約資源。</span><span class="sxs-lookup"><span data-stu-id="f31dd-105">The Schedule assistant is used to book resources based on requirements defined by the Project manager.</span></span> <span data-ttu-id="f31dd-106">排程小幫手依賴資源需求中提供的參數來尋找資源。</span><span class="sxs-lookup"><span data-stu-id="f31dd-106">The schedule assistant relies on the parameters provided in the resource requirement to find the resource.</span></span> <span data-ttu-id="f31dd-107">排程小幫手會建議符合相關需求 (例如時間範圍或所需技能) 的資源。</span><span class="sxs-lookup"><span data-stu-id="f31dd-107">The Schedule assistant recommends resources that match relevant requirements, like time windows or skills needed.</span></span>

<span data-ttu-id="f31dd-108">找出適當的資源後，資源管理員或專案經理就可以將資源預約給工作。</span><span class="sxs-lookup"><span data-stu-id="f31dd-108">After suitable resources are identified, the Resource or Project manager can book the resource to the work.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="f31dd-109">先決條件</span><span class="sxs-lookup"><span data-stu-id="f31dd-109">Prerequisites</span></span>

<span data-ttu-id="f31dd-110">排程小幫手是 Universal Resource Scheduling 解決方案的一部分。</span><span class="sxs-lookup"><span data-stu-id="f31dd-110">The Schedule assistant is a part of the Universal Resource Scheduling solution.</span></span> <span data-ttu-id="f31dd-111">此解決方案隨附於 Dynamics 365 Project Operations、Dynamics 365 Field Service 和 Dynamics 365 Customer Service，並且會與這些解決方案一併安裝。</span><span class="sxs-lookup"><span data-stu-id="f31dd-111">This solution is included and installed with Dynamics 365 Project Operations, Dynamics 365 Field Service, and Dynamics 365 Customer Service.</span></span>

## <a name="matching-requirements-and-resources"></a><span data-ttu-id="f31dd-112">比對需求與資源</span><span class="sxs-lookup"><span data-stu-id="f31dd-112">Matching requirements and resources</span></span>

<span data-ttu-id="f31dd-113">產生的資源需求是根據一些詳細資料，例如：</span><span class="sxs-lookup"><span data-stu-id="f31dd-113">A generated resource requirement is based on details such as:</span></span>

-   <span data-ttu-id="f31dd-114">特性</span><span class="sxs-lookup"><span data-stu-id="f31dd-114">Characteristics</span></span>
-   <span data-ttu-id="f31dd-115">角色</span><span class="sxs-lookup"><span data-stu-id="f31dd-115">Roles</span></span>
-   <span data-ttu-id="f31dd-116">業務單位</span><span class="sxs-lookup"><span data-stu-id="f31dd-116">Business units</span></span>
-   <span data-ttu-id="f31dd-117">資源喜好設定</span><span class="sxs-lookup"><span data-stu-id="f31dd-117">Resource preferences</span></span>
-   <span data-ttu-id="f31dd-118">投入量分佈</span><span class="sxs-lookup"><span data-stu-id="f31dd-118">Effort contours</span></span>
-   <span data-ttu-id="f31dd-119">時區</span><span class="sxs-lookup"><span data-stu-id="f31dd-119">Time zone</span></span>

<span data-ttu-id="f31dd-120">排程小幫手使用這些詳細資料來篩選資源。</span><span class="sxs-lookup"><span data-stu-id="f31dd-120">The Schedule assistant uses these details to filter resources.</span></span>

## <a name="launch-the-schedule-assistant"></a><span data-ttu-id="f31dd-121">啟動排程小幫手</span><span class="sxs-lookup"><span data-stu-id="f31dd-121">Launch the Schedule assistant</span></span>

<span data-ttu-id="f31dd-122">有兩種方式可以用來啟動排程小幫手。</span><span class="sxs-lookup"><span data-stu-id="f31dd-122">There are two ways in which the schedule assistant is launched.</span></span> <span data-ttu-id="f31dd-123">如果您使用的是混合模式，則可以在團隊成員網格中選取任何有未履行資源需求的團隊成員，然後選取**預約**。</span><span class="sxs-lookup"><span data-stu-id="f31dd-123">If you're using the hybrid mode, in the team member grid you can select any team member with an unfulfilled resource requirement, and then select **Book**.</span></span> <span data-ttu-id="f31dd-124">如果您使用的是集中模式，則資源管理員會尋找並選取資源。</span><span class="sxs-lookup"><span data-stu-id="f31dd-124">If you're using the central mode, the Resource manager finds and selects the resource.</span></span>

## <a name="schedule-assistant-filters"></a><span data-ttu-id="f31dd-125">排程小幫手篩選</span><span class="sxs-lookup"><span data-stu-id="f31dd-125">Schedule assistant filters</span></span>

<span data-ttu-id="f31dd-126">排程小幫手執行之後，資源需求的詳細資料會在左窗格中顯示為篩選後的值。</span><span class="sxs-lookup"><span data-stu-id="f31dd-126">After the Schedule assistant runs, the details from the resource requirement are displayed as filtered values in the left pane.</span></span> <span data-ttu-id="f31dd-127">資源管理員或專案經理可將篩選調整成符合排程需求以微調結果。</span><span class="sxs-lookup"><span data-stu-id="f31dd-127">The Resource manager or the Project manager can fine-tune results by adjusting filters to meet the scheduling needs.</span></span>

<span data-ttu-id="f31dd-128">篩選窗格會顯示工作相關選項，包括：</span><span class="sxs-lookup"><span data-stu-id="f31dd-128">The filter pane shows work-related options, including:</span></span>

-   <span data-ttu-id="f31dd-129">工作開始和結束</span><span class="sxs-lookup"><span data-stu-id="f31dd-129">Work start and end</span></span>
-   <span data-ttu-id="f31dd-130">特性</span><span class="sxs-lookup"><span data-stu-id="f31dd-130">Characteristics</span></span>
-   <span data-ttu-id="f31dd-131">角色</span><span class="sxs-lookup"><span data-stu-id="f31dd-131">Roles</span></span>
-   <span data-ttu-id="f31dd-132">組織單位</span><span class="sxs-lookup"><span data-stu-id="f31dd-132">Organizational units</span></span>
-   <span data-ttu-id="f31dd-133">資源供應公司</span><span class="sxs-lookup"><span data-stu-id="f31dd-133">Resourcing company</span></span>
-   <span data-ttu-id="f31dd-134">資源類型</span><span class="sxs-lookup"><span data-stu-id="f31dd-134">Resource types</span></span>
-   <span data-ttu-id="f31dd-135">偏好的資源</span><span class="sxs-lookup"><span data-stu-id="f31dd-135">Preferred resources</span></span>
