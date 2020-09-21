---
title: 專案階段
description: 本主題提供有關專案階段的資訊。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 983c25a0-ed21-4151-a109-b385a88285fa
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 70aa057e127df7ba925e84f5d056a06a4cc8833e
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749889"
---
# <a name="project-stages"></a><span data-ttu-id="e6086-103">專案階段</span><span class="sxs-lookup"><span data-stu-id="e6086-103">Project stages</span></span> 

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e6086-104">專案階段會更新，以反映專案進展時的狀態。</span><span class="sxs-lookup"><span data-stu-id="e6086-104">Project stages are updated to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="e6086-105">預設商務程序流程會自動更新專案階段的部分階段，而其他階段則由專案經理手動進行更新。</span><span class="sxs-lookup"><span data-stu-id="e6086-105">The default business process flow automatically updates some stages of the project while others are manually updated by the project manager.</span></span> 

<span data-ttu-id="e6086-106">下列階段已在預設 BPF 中定義：</span><span class="sxs-lookup"><span data-stu-id="e6086-106">The following stages are defined in the default BPF:</span></span>

- <span data-ttu-id="e6086-107">新增</span><span class="sxs-lookup"><span data-stu-id="e6086-107">New</span></span>
- <span data-ttu-id="e6086-108">報價</span><span class="sxs-lookup"><span data-stu-id="e6086-108">Quote</span></span>
- <span data-ttu-id="e6086-109">計劃</span><span class="sxs-lookup"><span data-stu-id="e6086-109">Plan</span></span>
- <span data-ttu-id="e6086-110">交付</span><span class="sxs-lookup"><span data-stu-id="e6086-110">Deliver</span></span>
- <span data-ttu-id="e6086-111">完成</span><span class="sxs-lookup"><span data-stu-id="e6086-111">Complete</span></span>
- <span data-ttu-id="e6086-112">關閉</span><span class="sxs-lookup"><span data-stu-id="e6086-112">Close</span></span> 

## <a name="new"></a><span data-ttu-id="e6086-113">新增</span><span class="sxs-lookup"><span data-stu-id="e6086-113">New</span></span>

<span data-ttu-id="e6086-114">建立專案時，專案階段會設定為 **新增**。</span><span class="sxs-lookup"><span data-stu-id="e6086-114">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="e6086-115">如果專案是從範本建立，則可能會有排程、估計值及團隊資料。</span><span class="sxs-lookup"><span data-stu-id="e6086-115">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="e6086-116">否則，就只是專案的大綱，您必須輸入剩餘的元件。</span><span class="sxs-lookup"><span data-stu-id="e6086-116">Otherwise, it's just an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="e6086-117">報價</span><span class="sxs-lookup"><span data-stu-id="e6086-117">Quote</span></span>

<span data-ttu-id="e6086-118">將專案與報價建立關聯或從報價建立專案時，專案階段會設定為**報價**，而估計的開始和結束日期也會更新。</span><span class="sxs-lookup"><span data-stu-id="e6086-118">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="e6086-119">專案處於**報價**階段時，**專案實體**上的**銷售**索引標籤會顯示報價的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e6086-119">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="e6086-120">計劃</span><span class="sxs-lookup"><span data-stu-id="e6086-120">Plan</span></span>

<span data-ttu-id="e6086-121">當您贏得與專案相關聯的報價，且專案已進入**合約**階段時，專案階段會更新為**計劃**。</span><span class="sxs-lookup"><span data-stu-id="e6086-121">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="e6086-122">專案處於**計劃**階段時，**專案實體**頁面會顯示合約的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="e6086-122">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="e6086-123">交付</span><span class="sxs-lookup"><span data-stu-id="e6086-123">Deliver</span></span>

<span data-ttu-id="e6086-124">專案計劃完成，且您已準備好開始專案時，專案經理應將專案階段更新為**交付**，以顯示專案已開始。</span><span class="sxs-lookup"><span data-stu-id="e6086-124">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="e6086-125">完成</span><span class="sxs-lookup"><span data-stu-id="e6086-125">Complete</span></span> 

<span data-ttu-id="e6086-126">專案的工作完成後，專案經理就可以將階段更新為**完成**。</span><span class="sxs-lookup"><span data-stu-id="e6086-126">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="e6086-127">專案經理藉由將專案階段更新為**完成**，指出工作已百分之百完成，但專案仍保持開啟狀態，讓您可以記錄任何擱置的時間或費用項目。</span><span class="sxs-lookup"><span data-stu-id="e6086-127">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="e6086-128">關閉</span><span class="sxs-lookup"><span data-stu-id="e6086-128">Close</span></span>

<span data-ttu-id="e6086-129">將專案所有的交易都記錄下來後，專案經理就可以將階段更新為**關閉**。</span><span class="sxs-lookup"><span data-stu-id="e6086-129">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="e6086-130">此時，無法記錄任何交易，且專案會設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="e6086-130">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>
