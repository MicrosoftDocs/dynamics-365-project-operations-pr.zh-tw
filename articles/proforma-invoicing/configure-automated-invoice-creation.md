---
title: 設定自動發票建立作業
description: 本主題提供有關如何將系統設定成自動產生發票的資訊。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 4e7572f2bc6201960ac01ce521adf39ac2577dbe
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072889"
---
# <a name="configure-automatic-invoice-creation"></a><span data-ttu-id="979ac-103">設定自動發票建立作業</span><span class="sxs-lookup"><span data-stu-id="979ac-103">Configure automatic invoice creation</span></span>

<span data-ttu-id="979ac-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="979ac-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>


<span data-ttu-id="979ac-105">完成下列步驟，在 Dynamics 365 Project Operations 中設定自動化發票執行。</span><span class="sxs-lookup"><span data-stu-id="979ac-105">Complete the following steps to configure an automated invoice run in Dynamics 365 Project operations.</span></span>

1. <span data-ttu-id="979ac-106">移至 **設定** > **批次工作** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-106">Go to **Settings** > **Batch jobs**.</span></span>
2. <span data-ttu-id="979ac-107">建立批次工作，並將其命名為 **Project Operations 建立發票** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-107">Create a batch job, and name it **Project operations create invoices**.</span></span> <span data-ttu-id="979ac-108">批次工作的名稱必須包含「建立發票」一詞。</span><span class="sxs-lookup"><span data-stu-id="979ac-108">The name of the batch job must include the words "create invoices."</span></span>
3. <span data-ttu-id="979ac-109">在 **工作類型** 欄位中，選取 **無** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-109">In the **Job Type** field, select **None**.</span></span> <span data-ttu-id="979ac-110">**每日頻率** 和 **使用中** 選項預設會設定為 **是** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-110">By default, the **Frequency Daily** and **Is Active** options are set to **Yes**.</span></span>
4. <span data-ttu-id="979ac-111">選取 **執行工作流程** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-111">Select **Run Workflow**.</span></span> <span data-ttu-id="979ac-112">在 **查詢記錄** 對話方塊中，您會看到三個工作流程：</span><span class="sxs-lookup"><span data-stu-id="979ac-112">In the **Look Up Record** dialog box, you will see three workflows:</span></span>

    - <span data-ttu-id="979ac-113">ProcessRunCaller</span><span class="sxs-lookup"><span data-stu-id="979ac-113">ProcessRunCaller</span></span>
    - <span data-ttu-id="979ac-114">ProcessRunner</span><span class="sxs-lookup"><span data-stu-id="979ac-114">ProcessRunner</span></span>
    - <span data-ttu-id="979ac-115">UpdateRoleUtilization</span><span class="sxs-lookup"><span data-stu-id="979ac-115">UpdateRoleUtilization</span></span>

5. <span data-ttu-id="979ac-116">選取 **ProcessRunCaller** ，然後選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-116">Select **ProcessRunCaller** , and then select **Add**.</span></span>
6. <span data-ttu-id="979ac-117">在下一個對話方塊中選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-117">In the next dialog box, select **OK**.</span></span> <span data-ttu-id="979ac-118">**睡眠** 工作流程後面會跟著 **程序** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="979ac-118">A **Sleep** workflow is followed by a **Process** workflow.</span></span>

  > [!NOTE]
  > <span data-ttu-id="979ac-119">您也可以選取步驟 5 中的 **ProcessRunner** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-119">You can also select **ProcessRunner** in step 5.</span></span> <span data-ttu-id="979ac-120">然後，當您選取 **確定** 時， **程序** 工作流程後面會接著 **睡眠** 工作流程。</span><span class="sxs-lookup"><span data-stu-id="979ac-120">Then, when you select **OK** , a **Process** workflow is followed by a **Sleep** workflow.</span></span>

<span data-ttu-id="979ac-121">**ProcessRunCaller** 和 **ProcessRunner** 工作流程會建立發票。</span><span class="sxs-lookup"><span data-stu-id="979ac-121">The **ProcessRunCaller** and **ProcessRunner** workflows create invoices.</span></span> <span data-ttu-id="979ac-122">**ProcessRunCaller** 會呼叫 **ProcessRunner** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-122">**ProcessRunCaller** calls **ProcessRunner**.</span></span> <span data-ttu-id="979ac-123">**ProcessRunner** 是實際建立發票的工作流程。</span><span class="sxs-lookup"><span data-stu-id="979ac-123">**ProcessRunner** is the workflow that actually creates the invoices.</span></span> <span data-ttu-id="979ac-124">它會處理所有需要建立發票的合約服務內容，然後為這些服務內容建立發票。</span><span class="sxs-lookup"><span data-stu-id="979ac-124">It goes through all the contract lines that invoices must be created for, and it creates invoices for those lines.</span></span> <span data-ttu-id="979ac-125">為了確定必須建立其發票的合約服務內容，工作會查看合約服務內容的發票執行日期。</span><span class="sxs-lookup"><span data-stu-id="979ac-125">To determine the contract lines that invoices must be created for, the job looks at invoice run dates for the contract lines.</span></span> <span data-ttu-id="979ac-126">如果屬於一個合約的合約服務內容具有相同的發票執行日期，則會將交易合併成一個有兩個發票明細的發票。</span><span class="sxs-lookup"><span data-stu-id="979ac-126">If contract lines that belong to one contract have the same invoice run date, the transactions are combined into one invoice that has two invoice lines.</span></span> <span data-ttu-id="979ac-127">如果沒有要要建立其發票的交易，則工作會跳過發票建立作業。</span><span class="sxs-lookup"><span data-stu-id="979ac-127">If there are no transactions to create invoices for, the job skips invoice creation.</span></span>

<span data-ttu-id="979ac-128">**ProcessRunner** 執行完畢後，會呼叫 **ProcessRunCaller** 、提供結束時間，然後關閉。</span><span class="sxs-lookup"><span data-stu-id="979ac-128">After **ProcessRunner** has finished running, it calls **ProcessRunCaller** , provides the end time, and is closed.</span></span> <span data-ttu-id="979ac-129">**ProcessRunCaller** 接著啟動計時器，從指定的結束時間開始執行 24 小時。</span><span class="sxs-lookup"><span data-stu-id="979ac-129">**ProcessRunCaller** then starts a timer that runs for 24 hours from the specified end time.</span></span> <span data-ttu-id="979ac-130">計時器結束時，會關閉 **ProcessRunCaller** 。</span><span class="sxs-lookup"><span data-stu-id="979ac-130">At the end of the timer, **ProcessRunCaller** is closed.</span></span>

<span data-ttu-id="979ac-131">用於建立發票的批次處理工作是週期性工作。</span><span class="sxs-lookup"><span data-stu-id="979ac-131">The batch process job for creating invoices is a recurrent job.</span></span> <span data-ttu-id="979ac-132">如果此批次處理已執行多次，就會建立工作的多個執行個體，並造成錯誤。</span><span class="sxs-lookup"><span data-stu-id="979ac-132">If this batch process is run many times, multiple instances of the job are created and cause errors.</span></span> <span data-ttu-id="979ac-133">因此，您只能啟動批次處理一次，並且只有在其停止執行時才要重新啟動此工作。</span><span class="sxs-lookup"><span data-stu-id="979ac-133">Therefore, you should start the batch process only one time, and you should restart it only if it stops running.</span></span>

> [!NOTE]
> <span data-ttu-id="979ac-134">批次開立發票只會對發票排程所設定的專案合約服務內容來執行。</span><span class="sxs-lookup"><span data-stu-id="979ac-134">Batch invoicing only runs for project contract lines that are configured by invoice schedules.</span></span> <span data-ttu-id="979ac-135">使用固定價格計費方式的合約服務內容必須已設定里程碑。</span><span class="sxs-lookup"><span data-stu-id="979ac-135">A contract line with a fixed price billing method must have milestones configured.</span></span> <span data-ttu-id="979ac-136">使用時間和材料計費方式的專案合約服務內容必須設定以日期為依據的發票排程。</span><span class="sxs-lookup"><span data-stu-id="979ac-136">A project contract line with a time and material billing method will need a date-based invoice schedule set up.</span></span> <span data-ttu-id="979ac-137">這同樣適用於專案型合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="979ac-137">The same applies to a project-based contract line.</span></span>     
