---
title: 同步處理資源產能
description: 本主題提供有關如何跨行事曆與專案同步處理資源產能的資訊。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8bde3c434680f0651293cbce13ecdce945c3a743
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5997501"
---
# <a name="synchronize-resource-capacity"></a><span data-ttu-id="0cfd1-103">同步處理資源產能</span><span class="sxs-lookup"><span data-stu-id="0cfd1-103">Synchronize resource capacity</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0cfd1-104">資源同步處理的程序有助於保證行事曆及基準行事曆的資訊會逐漸滲入專案資源排程中。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-104">The processes for resource synchronization help guarantee that information for the calendar and base calendar trickles down into project resource scheduling.</span></span> <span data-ttu-id="0cfd1-105">如果行事曆已變更，此程序就會對專案資源排程進行必要的更新。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-105">If the calendar is changed, the processes make the required updates to the scheduling of project resources.</span></span> <span data-ttu-id="0cfd1-106">此程式也有助於改善效能，因為會提前同步處理行事曆的資源資訊。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-106">The processes also help improve performance, because the calendar's resource information is synchronized in advance.</span></span> <span data-ttu-id="0cfd1-107">因此會加快進行對資源排程資訊的更新。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-107">Therefore, updates to resource scheduling information occur more quickly.</span></span> <span data-ttu-id="0cfd1-108">建議您以批次方式排定這些程序，而不是逐次排定。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-108">We recommend that you schedule the processes as a batch instead of one at a time.</span></span> <span data-ttu-id="0cfd1-109">否則，會有人忘記上次同步處理資訊時包含的日期。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-109">Otherwise, there is a risk that someone will forget the inclusive dates when the information was last synchronized.</span></span> <span data-ttu-id="0cfd1-110">如果沒有使用包含的日期，就會在進行日期同步處理時出現期間缺口。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-110">If inclusive dates aren't used, gaps can occur during date synchronization.</span></span>

![行事曆同步處理](./media/projectresourcing04-1024x471.jpg)

## <a name="synchronize-resource-capacity-roll-ups"></a><span data-ttu-id="0cfd1-112">同步處理資源產能彙總</span><span class="sxs-lookup"><span data-stu-id="0cfd1-112">Synchronize resource capacity roll-ups</span></span>

<span data-ttu-id="0cfd1-113">同步處理程序是專為同步處理所有資源行事曆資訊而設計。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-113">The synchronization process is designed to synchronize all resource calendar information.</span></span> <span data-ttu-id="0cfd1-114">此資訊包含有關任何對專案資源行事曆產能資料表所做變更的基準行事曆資訊。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-114">This information includes base calendar information about any changes to the project's Resource calendar capacity table.</span></span> <span data-ttu-id="0cfd1-115">如果專案中新增了新資源，同步處理有助於保證有更新過的行事曆資訊可供使用。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-115">If new resources are added in the project, synchronization helps guarantee that the updated calendar information is available.</span></span> <span data-ttu-id="0cfd1-116">此同步處理作業隨時都可以進行。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-116">This synchronization can be done at any time.</span></span>

<span data-ttu-id="0cfd1-117">建議您使用批次。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-117">We recommend that you use a batch.</span></span> <span data-ttu-id="0cfd1-118">有選項可在產能保留同步處理期間使用。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-118">The options are available during synchronization of capacity reservations.</span></span>

1. <span data-ttu-id="0cfd1-119">選取 **專案管理與會計** &gt; **定期** &gt; **產能同步處理** &gt; **同步處理資源產能彙總**。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-119">Select **Project management and accounting** &gt; **Periodic** &gt; **Capacity synchronization** &gt; **Synchronize resources capacity roll-ups**.</span></span>
2. <span data-ttu-id="0cfd1-120">設定下表中的選項。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-120">Set the options in the following table.</span></span>

    | <span data-ttu-id="0cfd1-121">選項</span><span class="sxs-lookup"><span data-stu-id="0cfd1-121">Option</span></span>      | <span data-ttu-id="0cfd1-122">描述</span><span class="sxs-lookup"><span data-stu-id="0cfd1-122">Description</span></span> |
    |-------------|-------------|
    | <span data-ttu-id="0cfd1-123">期間代碼</span><span class="sxs-lookup"><span data-stu-id="0cfd1-123">Period code</span></span> | <span data-ttu-id="0cfd1-124">選擇性選取總帳日期間隔代碼，以設定資源產能彙總同步處理程序的開始和結束日期。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-124">Optionally select the General ledger date interval code to set the start and end dates for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="0cfd1-125">開始日期</span><span class="sxs-lookup"><span data-stu-id="0cfd1-125">Start date</span></span>  | <span data-ttu-id="0cfd1-126">輸入資源產能彙總同步處理程序的開始日期。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-126">Enter the start date for the synchronization process for resource capacity roll-ups.</span></span> |
    | <span data-ttu-id="0cfd1-127">結束日期</span><span class="sxs-lookup"><span data-stu-id="0cfd1-127">End date</span></span>    | <span data-ttu-id="0cfd1-128">輸入資源產能彙總同步處理程序的結束日期。</span><span class="sxs-lookup"><span data-stu-id="0cfd1-128">Enter the end date for the synchronization process for resource capacity roll-ups.</span></span> |

<span data-ttu-id="0cfd1-129">[![同步處理程序](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span><span class="sxs-lookup"><span data-stu-id="0cfd1-129">[![Synchronization process](./media/projectresourcing09.jpg)](./media/projectresourcing09.jpg)</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]