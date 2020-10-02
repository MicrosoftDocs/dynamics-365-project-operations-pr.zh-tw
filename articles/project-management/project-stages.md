---
title: 專案階段
description: 本主題提供有關 Microsoft Dynamics Project Operations 中所提供之專案階段的資訊。
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
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
ms.openlocfilehash: b11c67ebd21fdf423eeae2db8154f26787c2e64f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3897936"
---
# <a name="project-stages"></a><span data-ttu-id="b77af-103">專案階段</span><span class="sxs-lookup"><span data-stu-id="b77af-103">Project stages</span></span>

<span data-ttu-id="b77af-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="b77af-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b77af-105">專案階段為了反映專案進展時的狀態而設計。</span><span class="sxs-lookup"><span data-stu-id="b77af-105">Project stages are designed to reflect the state of the project as it progresses.</span></span> <span data-ttu-id="b77af-106">自訂可以用來讓系統自動更新階段的商務程序流程、Power Automate 或外掛程式擴充功能。</span><span class="sxs-lookup"><span data-stu-id="b77af-106">Customizations can be used to automatically update the stages with business process flows, Power Automate, or plug-in extensions.</span></span>

<span data-ttu-id="b77af-107">預設商務程序流程中已定義下列階段：</span><span class="sxs-lookup"><span data-stu-id="b77af-107">The following stages are defined in the default business process flow:</span></span>

- <span data-ttu-id="b77af-108">新的 ​​</span><span class="sxs-lookup"><span data-stu-id="b77af-108">New</span></span>
- <span data-ttu-id="b77af-109">報價</span><span class="sxs-lookup"><span data-stu-id="b77af-109">Quote</span></span>
- <span data-ttu-id="b77af-110">計劃</span><span class="sxs-lookup"><span data-stu-id="b77af-110">Plan</span></span>
- <span data-ttu-id="b77af-111">交付</span><span class="sxs-lookup"><span data-stu-id="b77af-111">Deliver</span></span>
- <span data-ttu-id="b77af-112">完成</span><span class="sxs-lookup"><span data-stu-id="b77af-112">Complete</span></span>
- <span data-ttu-id="b77af-113">關閉​​</span><span class="sxs-lookup"><span data-stu-id="b77af-113">Close</span></span> 

## <a name="new"></a><span data-ttu-id="b77af-114">新的 ​​</span><span class="sxs-lookup"><span data-stu-id="b77af-114">New</span></span>

<span data-ttu-id="b77af-115">建立專案時，專案階段會設定為 **新增**。</span><span class="sxs-lookup"><span data-stu-id="b77af-115">When you create a project, the project stage is set to **New**.</span></span> <span data-ttu-id="b77af-116">如果專案是從範本建立，則可能會有排程、估計值及團隊資料。</span><span class="sxs-lookup"><span data-stu-id="b77af-116">If the project was created from a template, it might have schedule, estimate, and team data.</span></span> <span data-ttu-id="b77af-117">否則，這會是專案的大綱，您必須輸入剩餘的元件。</span><span class="sxs-lookup"><span data-stu-id="b77af-117">Otherwise, it's an outline of the project, and the remaining components must be entered.</span></span>

## <a name="quote"></a><span data-ttu-id="b77af-118">報價</span><span class="sxs-lookup"><span data-stu-id="b77af-118">Quote</span></span>

<span data-ttu-id="b77af-119">將專案與報價建立關聯或從報價建立專案時，專案階段會設定為**報價**，而估計的開始和結束日期也會更新。</span><span class="sxs-lookup"><span data-stu-id="b77af-119">When you associate a project with a quote, or when you create a project from a quote, the project stage is set to **Quote**, and the estimated start and end dates are updated.</span></span> <span data-ttu-id="b77af-120">專案處於**報價**階段時，**專案實體**上的**銷售**索引標籤會顯示報價的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b77af-120">While the project is in the **Quote** stage, the **Sales** tab on the **Project Entity** page shows details of the quote.</span></span>

## <a name="plan"></a><span data-ttu-id="b77af-121">計劃</span><span class="sxs-lookup"><span data-stu-id="b77af-121">Plan</span></span>

<span data-ttu-id="b77af-122">當您贏得與專案相關聯的報價，且專案已進入**合約**階段時，專案階段會更新為**計劃**。</span><span class="sxs-lookup"><span data-stu-id="b77af-122">When you win a quote that is associated with a project, and the project is moved to the **Contract** phase, the project stage is updated to **Plan**.</span></span> <span data-ttu-id="b77af-123">專案處於**計劃**階段時，**專案實體**頁面會顯示合約的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b77af-123">While the project is in the **Plan** stage, the **Project Entity** page shows details of the contract.</span></span>

## <a name="deliver"></a><span data-ttu-id="b77af-124">交付</span><span class="sxs-lookup"><span data-stu-id="b77af-124">Deliver</span></span>

<span data-ttu-id="b77af-125">專案計劃完成，且您已準備好開始專案時，專案經理應將專案階段更新為**交付**，以顯示專案已開始。</span><span class="sxs-lookup"><span data-stu-id="b77af-125">When the project plan is completed, and you're ready to start the project, the project manager should update the project stage to **Deliver** to show that the project has started.</span></span>

## <a name="complete"></a><span data-ttu-id="b77af-126">完成</span><span class="sxs-lookup"><span data-stu-id="b77af-126">Complete</span></span> 

<span data-ttu-id="b77af-127">專案的工作完成後，專案經理就可以將階段更新為**完成**。</span><span class="sxs-lookup"><span data-stu-id="b77af-127">When the work for the project is completed, the project manager can update the stage to **Complete**.</span></span> <span data-ttu-id="b77af-128">專案經理藉由將專案階段更新為**完成**，指出工作已百分之百完成，但專案仍保持開啟狀態，讓您可以記錄任何擱置的時間或費用項目。</span><span class="sxs-lookup"><span data-stu-id="b77af-128">By updating the project stage to **Complete**, the project manager indicates that the work is 100-percent completed, but that the project is being kept open so that any pending time or expense entries can be recorded.</span></span>

## <a name="close"></a><span data-ttu-id="b77af-129">關閉</span><span class="sxs-lookup"><span data-stu-id="b77af-129">Close</span></span>

<span data-ttu-id="b77af-130">將專案所有的交易都記錄下來後，專案經理就可以將階段更新為**關閉**。</span><span class="sxs-lookup"><span data-stu-id="b77af-130">When all transactions are recorded for the project, the project manager can update the stage to **Close**.</span></span> <span data-ttu-id="b77af-131">此時，無法記錄任何交易，且專案會設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="b77af-131">At that point, no transactions can be recorded, and the project is set to read-only.</span></span>

