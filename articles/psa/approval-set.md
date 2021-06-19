---
title: 核准集
description: 本主題提供有關核准集、要求以及這些作業子集的資訊。
author: stsporen
manager: tfehr
ms.date: 05/28/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: ac73313420029ece740d0bdb9c21c7abaa9defc6
ms.sourcegitcommit: fc96c6eb9a2094f9fa3d1ae39646730ef9d558ba
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/28/2021
ms.locfileid: "6116861"
---
# <a name="approval-sets"></a><span data-ttu-id="e9ace-103">核准集</span><span class="sxs-lookup"><span data-stu-id="e9ace-103">Approval sets</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="e9ace-104">核准集會將核准要求集合成較小型作業子集的群組。</span><span class="sxs-lookup"><span data-stu-id="e9ace-104">Approval sets group approval requests together into smaller subsets of operations.</span></span> <span data-ttu-id="e9ace-105">這種群組方式可讓各項核准按照專案依序處理，並允許重試和排序。</span><span class="sxs-lookup"><span data-stu-id="e9ace-105">This grouping allows approvals to be processed in order by Project and allows for retrying and sequencing.</span></span> <span data-ttu-id="e9ace-106">群組功能可改善對大量核准記錄的核准處理可靠性和可追蹤性。</span><span class="sxs-lookup"><span data-stu-id="e9ace-106">Grouping improves the reliability and traceability of approval processing for large volumes of approvals.</span></span>

<span data-ttu-id="e9ace-107">核准集表示其相關記錄的整體處理狀態。</span><span class="sxs-lookup"><span data-stu-id="e9ace-107">Approval sets indicate the overall processing state of their related records.</span></span> <span data-ttu-id="e9ace-108">使用核准集來處理核准記錄時，該記錄會從 **已提交** 移至 **已核准** 狀態，並解除與核准集的連結。</span><span class="sxs-lookup"><span data-stu-id="e9ace-108">When an approval record is processed using an approval set, the record moves from **Submitted** to **Approved**, and is unlinked from the approval set.</span></span> <span data-ttu-id="e9ace-109">如果記錄在提交供核准時失敗，則記錄仍會保持在 **已提交** 狀態，而核准集會標示為失敗。</span><span class="sxs-lookup"><span data-stu-id="e9ace-109">If a record fails when it is submitted for approval, the record remains in a status of **Submitted** and the approval set is marked as failed.</span></span> <span data-ttu-id="e9ace-110">核准集會記錄失敗的錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="e9ace-110">The approval set logs the error message of the failure.</span></span>

## <a name="processing-approvals-and-approval-sets"></a><span data-ttu-id="e9ace-111">處理核准和核准集</span><span class="sxs-lookup"><span data-stu-id="e9ace-111">Processing approvals and approval sets</span></span>
<span data-ttu-id="e9ace-112">已排入佇列等待處理的核准會顯示在 **處理核准** 檢視表中。</span><span class="sxs-lookup"><span data-stu-id="e9ace-112">Approvals that are queued for processing are visible in the **Processing Approvals** view.</span></span> <span data-ttu-id="e9ace-113">系統會嘗試以非同步方式處理所有專案，包括會在前一次嘗試失敗時重試核准。</span><span class="sxs-lookup"><span data-stu-id="e9ace-113">The system tries to process all the entries multiple times asynchronously, including retrying an approval if previous attempts failed.</span></span>

<span data-ttu-id="e9ace-114">**核准集存留期** 欄位會記錄將此集合標示為失敗前，剩餘的嘗試處理次數。</span><span class="sxs-lookup"><span data-stu-id="e9ace-114">The **Approval Set Lifetime** field records the number of attempts left to process the set before it's marked as failed.</span></span>

## <a name="failed-approvals-and-approval-sets"></a><span data-ttu-id="e9ace-115">失敗的核准和核准集</span><span class="sxs-lookup"><span data-stu-id="e9ace-115">Failed approvals and approval sets</span></span>
<span data-ttu-id="e9ace-116">**失敗的核准** 檢視表會列出所有需要使用者介入的核准。</span><span class="sxs-lookup"><span data-stu-id="e9ace-116">The **Failed Approvals** view lists all approvals that require user intervention.</span></span> <span data-ttu-id="e9ace-117">開啟相關聯的核准集記錄，找出失敗原因。</span><span class="sxs-lookup"><span data-stu-id="e9ace-117">Open the associated approval set logs to identify the cause of the failure.</span></span>
<span data-ttu-id="e9ace-118">選取 **重試** 會增加核准集存留期計數、將核准集移回 **處理中** 狀態，並嘗試處理其餘的記錄。</span><span class="sxs-lookup"><span data-stu-id="e9ace-118">Selecting **Retry** adds to the approval set lifetime count, moves the approval set back to a status of **Processing**, and attempts to process the remaining records.</span></span>

## <a name="configure-approval-sets"></a><span data-ttu-id="e9ace-119">設定核准集</span><span class="sxs-lookup"><span data-stu-id="e9ace-119">Configure approval sets</span></span>

###  <a name="enable-the-approval-sets-feature"></a><span data-ttu-id="e9ace-120">啟用核准集功能</span><span class="sxs-lookup"><span data-stu-id="e9ace-120">Enable the Approval sets feature</span></span>
<span data-ttu-id="e9ace-121">啟用核准集功能之前，請先確認目前沒有任何核准在處理中。</span><span class="sxs-lookup"><span data-stu-id="e9ace-121">Before you enable the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="e9ace-122">移至 **專案參數** 頁面，並選取 **功能控制** > **啟用現代化核准**。</span><span class="sxs-lookup"><span data-stu-id="e9ace-122">Go to the **Project parameters** page and select **Feature Control** > **Enable Modern Approvals**.</span></span>

### <a name="turn-off-the-approval-sets-feature"></a><span data-ttu-id="e9ace-123">關閉核准集功能</span><span class="sxs-lookup"><span data-stu-id="e9ace-123">Turn off the Approval sets feature</span></span>
<span data-ttu-id="e9ace-124">關閉核准集功能之前，請先確認目前沒有任何核准在處理中。</span><span class="sxs-lookup"><span data-stu-id="e9ace-124">Before you turn off the Approval sets feature, verify that there are no approvals currently being processed.</span></span>

- <span data-ttu-id="e9ace-125">移至 **專案參數** 頁面，並選取 **功能控制** > **停用現代化核准**。</span><span class="sxs-lookup"><span data-stu-id="e9ace-125">Go to the **Project Parameters** page and select **Feature Control** > **Disable Modern Approvals**.</span></span>

### <a name="configuring-the-asynchronous-threshold"></a><span data-ttu-id="e9ace-126">設定非同步閾值</span><span class="sxs-lookup"><span data-stu-id="e9ace-126">Configuring the asynchronous threshold</span></span> 
<span data-ttu-id="e9ace-127">如果建立了核准集，當所選取待核准的記錄數目超過指示的閾值時，處理作業就會移至背景。</span><span class="sxs-lookup"><span data-stu-id="e9ace-127">When approval sets are created, processing moves to the background when the selected number of records for approval exceeds the indicated threshold.</span></span> <span data-ttu-id="e9ace-128">使用 **非同步閾值** 欄位來設定何時應同步或非同步執行核准處理。</span><span class="sxs-lookup"><span data-stu-id="e9ace-128">Use the **Asynchronous Threshold** field to configure when approval processing should be run synchronously or asynchronously.</span></span>
<span data-ttu-id="e9ace-129">有效值為：</span><span class="sxs-lookup"><span data-stu-id="e9ace-129">Valid values are:</span></span>

  - <span data-ttu-id="e9ace-130">零：所有要求都必須以非同步方式來處理。</span><span class="sxs-lookup"><span data-stu-id="e9ace-130">Zero: All requests should be processed asynchronously.</span></span> 
  - <span data-ttu-id="e9ace-131">大於零的數字：只有在提交核准的數目超過此值時，才會以非同步方式處理核准。</span><span class="sxs-lookup"><span data-stu-id="e9ace-131">Numbers greater than zero: Approvals are processed asynchronously only when the submitted number of approvals exceeds this value.</span></span>

[!INCLUDE[footer-include](../includes/footer-banner.md)]
