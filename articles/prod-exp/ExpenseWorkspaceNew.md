---
title: 重新設計的費用報表
description: 本主題提供有關 Microsoft Dynamics 365 Finance 中費用報表項目重新設計和顛覆想像體驗的資訊。 新的體驗簡化完成費用報表的程序，並減少所需的時間。
author: ryansandness
manager: AnnBe
ms.date: 06/14/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2019-6-30
ms.dyn365.ops.version: 10.0.3
ms.openlocfilehash: d076c0a596940cb08433f7ee57dea54903f6078f
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960237"
---
# <a name="redesigned-expense-reports"></a><span data-ttu-id="9fd36-104">重新設計的費用報表</span><span class="sxs-lookup"><span data-stu-id="9fd36-104">Redesigned expense reports</span></span>

<span data-ttu-id="9fd36-105">費用報表項目經過重新設計，可以簡化完成費用報表的程序，並減少所需的時間。</span><span class="sxs-lookup"><span data-stu-id="9fd36-105">Expense report entry has been redesigned to simplify the process of completing expense reports and decrease the time that is required.</span></span> <span data-ttu-id="9fd36-106">以下是新的費用體驗的主要元件：</span><span class="sxs-lookup"><span data-stu-id="9fd36-106">Here are the major components of the new expense experience:</span></span>

- <span data-ttu-id="9fd36-107">新的費用管理工作區，可讓您存取您的代理人的費用。</span><span class="sxs-lookup"><span data-stu-id="9fd36-107">A new expense management workspace that lets you access your delegate's expenses.</span></span>
- <span data-ttu-id="9fd36-108">新的收據配比體驗，可以更清楚顯示標題層級的收據，並簡化附加收據至費用明細的程序。</span><span class="sxs-lookup"><span data-stu-id="9fd36-108">A new receipt matching experience to better show header-level receipts and simplify the process of attaching receipts to expense lines.</span></span>
- <span data-ttu-id="9fd36-109">新的唯讀網格，可讓您檢視更多費用明細和其他資料欄。</span><span class="sxs-lookup"><span data-stu-id="9fd36-109">A new read-only grid that lets you view many more expense lines and additional columns of data.</span></span> <span data-ttu-id="9fd36-110">您現在可以查看所有逐條列舉和分割的明細，以及其上層費用。</span><span class="sxs-lookup"><span data-stu-id="9fd36-110">You can now see all itemized and split lines, together with their parent expenses.</span></span>
- <span data-ttu-id="9fd36-111">用於編輯費用的簡化窗格。</span><span class="sxs-lookup"><span data-stu-id="9fd36-111">A simplified pane for editing expenses.</span></span>
- <span data-ttu-id="9fd36-112">重新設計過的錯誤、警告及原則訊息，有助於保證您掌握正確的來龍去脈，可以了解問題是什麼以及如何解決。</span><span class="sxs-lookup"><span data-stu-id="9fd36-112">Redesigned error, warning, and policy messages to help guarantee that you have the correct context to understand what the issue is and how to resolve it.</span></span> <span data-ttu-id="9fd36-113">Microsoft 已移除許多在使用者有機會完成其工作並解決問題之前顯示的訊息，例如逐條列舉不完整訊息。</span><span class="sxs-lookup"><span data-stu-id="9fd36-113">Microsoft has removed many messages that appeared before users had an opportunity to complete their tasks and address the issues, such as the incomplete itemization message.</span></span>
- <span data-ttu-id="9fd36-114">用於指定哪些欄位是您組織所需要、哪些欄位是選用，以及哪些欄位是不可擷取欄位的新頁面。</span><span class="sxs-lookup"><span data-stu-id="9fd36-114">A new page for specifying which fields are required by your organization, which fields are optional, and which fields should not be captured.</span></span> <span data-ttu-id="9fd36-115">此頁面將有助於減少使用者必須設定的欄位數目。</span><span class="sxs-lookup"><span data-stu-id="9fd36-115">This page will help reduce the number of fields that users must to set.</span></span>
- <span data-ttu-id="9fd36-116">新的費用報表外觀與風格，讓報表看起來不再像是專為會計人員設計的一樣。</span><span class="sxs-lookup"><span data-stu-id="9fd36-116">A new look and feel for expense reports, so that the reports no longer seem as though they were designed for accounting personas.</span></span>

<span data-ttu-id="9fd36-117">若要開啟新的體驗，請使用 **功能管理** 工作區來開啟 **顛覆想像的費用報表** 功能。</span><span class="sxs-lookup"><span data-stu-id="9fd36-117">To turn on the new experience, use the **Feature management** workspace to turn on the **Expense reports re-imagined** feature.</span></span> <span data-ttu-id="9fd36-118">下列動作會在您開啟此功能時發生：</span><span class="sxs-lookup"><span data-stu-id="9fd36-118">When you turn on this feature, the following actions occur:</span></span>

- <span data-ttu-id="9fd36-119">現有的費用工作區會用新的工作區來取代。</span><span class="sxs-lookup"><span data-stu-id="9fd36-119">The existing expense workspace is replaced with the new workspace.</span></span>
- <span data-ttu-id="9fd36-120">新增費用欄位顯示性的新功能表項目。</span><span class="sxs-lookup"><span data-stu-id="9fd36-120">A new menu item for expense field visibility is added.</span></span>
- <span data-ttu-id="9fd36-121">不會移除費用報表 (現有頁面) 或費用報表欄位的任何現有功能表項目。</span><span class="sxs-lookup"><span data-stu-id="9fd36-121">No existing menu items for expense reports (the existing page) or expense report fields are removed.</span></span>
- <span data-ttu-id="9fd36-122">工作流程和任何核准仍會帶您進入現有的費用報表頁面。</span><span class="sxs-lookup"><span data-stu-id="9fd36-122">Workflows and any approvals still take you to the existing expense reports page.</span></span>

## <a name="getting-started-video-for-new-users"></a><span data-ttu-id="9fd36-123">新使用者適用的開始使用影片</span><span class="sxs-lookup"><span data-stu-id="9fd36-123">Getting started video for new users</span></span>

> [!VIDEO https://www.microsoft.com/videoplayer/embed/RE2Y7gO]

<span data-ttu-id="9fd36-124">[Dynamics 365 for Finance and Operations 中的費用體驗](https://youtu.be/Ocy-MsTvEE0)影片 (如上所示) 已加入 YouTube 上提供的 [Finance and Operations 播放清單](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW)中。</span><span class="sxs-lookup"><span data-stu-id="9fd36-124">The [Expense experience in Dynamics 365 for Finance and Operations](https://youtu.be/Ocy-MsTvEE0) video (shown above) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="new-features"></a><span data-ttu-id="9fd36-125">新功能</span><span class="sxs-lookup"><span data-stu-id="9fd36-125">New features</span></span>

| <span data-ttu-id="9fd36-126">新功能</span><span class="sxs-lookup"><span data-stu-id="9fd36-126">New feature</span></span> | <span data-ttu-id="9fd36-127">描述</span><span class="sxs-lookup"><span data-stu-id="9fd36-127">Description</span></span> |
|---|----|
| <span data-ttu-id="9fd36-128">費用欄位顯示性</span><span class="sxs-lookup"><span data-stu-id="9fd36-128">Expense field visibility</span></span> | <span data-ttu-id="9fd36-129">新的設定頁面可讓您指定組織應停用的欄位、必填的欄位，以及建議的欄位。</span><span class="sxs-lookup"><span data-stu-id="9fd36-129">A new setup page lets you specify which fields should be disabled for an organization, which fields should be required, and which fields are recommended.</span></span> |
| <span data-ttu-id="9fd36-130">必填欄位</span><span class="sxs-lookup"><span data-stu-id="9fd36-130">Required fields</span></span> | <span data-ttu-id="9fd36-131">新的簡單設定可讓您讓建立一些必要的欄位，而不需使用原則架構。</span><span class="sxs-lookup"><span data-stu-id="9fd36-131">New simple configuration lets you make some fields required without having to use the policy framework.</span></span> |
| <span data-ttu-id="9fd36-132">選用欄位</span><span class="sxs-lookup"><span data-stu-id="9fd36-132">Optional fields</span></span> | <span data-ttu-id="9fd36-133">已新增選用欄位的第二個頁面。</span><span class="sxs-lookup"><span data-stu-id="9fd36-133">A second page for optional fields is added.</span></span> <span data-ttu-id="9fd36-134">如此一來，員工就不會覺得他們必須設定欄位，但仍然可以輕鬆存取這些欄位。</span><span class="sxs-lookup"><span data-stu-id="9fd36-134">In this way, employees won't feel as if they must set the fields, but the fields are still easily accessible.</span></span> |
| <span data-ttu-id="9fd36-135">新增未附加的收據</span><span class="sxs-lookup"><span data-stu-id="9fd36-135">Add unattached receipts</span></span> | <span data-ttu-id="9fd36-136">將未附加的收據新增至費用報表的功能在工作區和費用報表中變得更加明顯。</span><span class="sxs-lookup"><span data-stu-id="9fd36-136">The ability to add unattached receipts to expense report is more visible from the workspace and on the expense report.</span></span> |
| <span data-ttu-id="9fd36-137">改善的訊息</span><span class="sxs-lookup"><span data-stu-id="9fd36-137">Improved messaging</span></span> | <span data-ttu-id="9fd36-138">更容易看清楚含有警告或錯誤的費用明細。</span><span class="sxs-lookup"><span data-stu-id="9fd36-138">There is better visibility into expense lines that have warnings or errors.</span></span> |
| <span data-ttu-id="9fd36-139">減少訊息列中的訊息</span><span class="sxs-lookup"><span data-stu-id="9fd36-139">Reduction in messages in the message bar</span></span>| <span data-ttu-id="9fd36-140">將資訊日誌訊息的數目已減少，並且已盡力避免重複的訊息出現在許多案例中。</span><span class="sxs-lookup"><span data-stu-id="9fd36-140">The number of Infolog messages was decreased, and an effort was made to prevent duplicate messages from appearing in many cases.</span></span> |
| <span data-ttu-id="9fd36-141">將通用動作群組在一起</span><span class="sxs-lookup"><span data-stu-id="9fd36-141">Grouped together common actions</span></span> | <span data-ttu-id="9fd36-142">介面已清理，並且加入了新的適用於大多數一般明細層級動作的動作按鈕，以及用於標題和其他較不常用動作的省略符號按鈕 (...) 。</span><span class="sxs-lookup"><span data-stu-id="9fd36-142">The interface was cleaned up with the addition of a new actions button for most of the common line-level actions and the addition of an ellipsis button (...) for header and other less frequent actions.</span></span> |
| <span data-ttu-id="9fd36-143">提升顯示性的新增工作區</span><span class="sxs-lookup"><span data-stu-id="9fd36-143">New workspace to increase visibility</span></span> | <span data-ttu-id="9fd36-144">新的工作區將功能與連結統合，使用者可用來移至不同的區域。</span><span class="sxs-lookup"><span data-stu-id="9fd36-144">A new workspace unifies features and links that let users move to different areas.</span></span> |
| <span data-ttu-id="9fd36-145">在建立費用過程中新增現有的費用和收據</span><span class="sxs-lookup"><span data-stu-id="9fd36-145">Add existing expenses and receipts during expense creation</span></span> | <span data-ttu-id="9fd36-146">建立費用報表時，您可以新增所有或所選的費用和收據。</span><span class="sxs-lookup"><span data-stu-id="9fd36-146">When you create expense reports, you can add all or selected expenses and receipts.</span></span> |
| <span data-ttu-id="9fd36-147">匯率計算機</span><span class="sxs-lookup"><span data-stu-id="9fd36-147">Exchange rate calculator</span></span> | <span data-ttu-id="9fd36-148">您可以新增匯率計算機，用來計算現款支付的多重貨幣交易匯率。</span><span class="sxs-lookup"><span data-stu-id="9fd36-148">An exchange rate calculator is added that lets you calculate the exchange rate for out-of-pocket multicurrency transactions.</span></span> |
| <span data-ttu-id="9fd36-149">儲存並新增費用明細</span><span class="sxs-lookup"><span data-stu-id="9fd36-149">Save and add new expense lines</span></span> | <span data-ttu-id="9fd36-150">輸入新的費用時，可以使用 **儲存** 和 **新增** 按鈕，協助您快速輸入費用明細。</span><span class="sxs-lookup"><span data-stu-id="9fd36-150">**Save** and **New** buttons are available when new expenses are entered, to help you quickly enter expense lines.</span></span> |
| <span data-ttu-id="9fd36-151">更清楚地查看分割和逐條列舉的明細</span><span class="sxs-lookup"><span data-stu-id="9fd36-151">Better visibility into split and itemized lines</span></span> | <span data-ttu-id="9fd36-152">逐條列舉和分割的明細會直接新增至費用清單以增加顯示性，並協助您輕鬆判斷是否發生原則錯誤或其他錯誤。</span><span class="sxs-lookup"><span data-stu-id="9fd36-152">Itemized and split lines are added directly to the list of expenses, to increase visibility and help you easily determine whether there are policy errors or other errors.</span></span> |
| <span data-ttu-id="9fd36-153">進行逐條列舉時顯示收據</span><span class="sxs-lookup"><span data-stu-id="9fd36-153">Show receipts during itemization</span></span> | <span data-ttu-id="9fd36-154">進行逐條列舉時可以顯示收據。</span><span class="sxs-lookup"><span data-stu-id="9fd36-154">Receipts can be shown during itemization.</span></span> |

<span data-ttu-id="9fd36-155">初次發行版本側重於費用項目案例。</span><span class="sxs-lookup"><span data-stu-id="9fd36-155">The initial release is focused on expense entry scenarios.</span></span> <span data-ttu-id="9fd36-156">任何費用報表審查或核准案例都會繼續使用現有的費用項目頁面。</span><span class="sxs-lookup"><span data-stu-id="9fd36-156">Any expense report review or approval scenario will continue to use the existing expense entry page.</span></span>

<span data-ttu-id="9fd36-157">下列功能出現在現有的頁面，但在新頁面中還不存在。</span><span class="sxs-lookup"><span data-stu-id="9fd36-157">The following features are present on the existing page but aren't yet present on the new page.</span></span> <span data-ttu-id="9fd36-158">這些功能會在接下來幾次發行的版本中重新推出：</span><span class="sxs-lookup"><span data-stu-id="9fd36-158">These features will be reintroduced over the next several releases:</span></span>

- <span data-ttu-id="9fd36-159">核准</span><span class="sxs-lookup"><span data-stu-id="9fd36-159">Approvals</span></span>
- <span data-ttu-id="9fd36-160">應付帳款核准以及編輯會計帳目的功能</span><span class="sxs-lookup"><span data-stu-id="9fd36-160">Accounts payable approvals and the ability to edit the accounting</span></span>
- <span data-ttu-id="9fd36-161">多個進入點</span><span class="sxs-lookup"><span data-stu-id="9fd36-161">Multiple entry points</span></span>
- <span data-ttu-id="9fd36-162">差旅申請整合</span><span class="sxs-lookup"><span data-stu-id="9fd36-162">Travel requisition integration</span></span>
- <span data-ttu-id="9fd36-163">費用欄位顯示性的資料實體</span><span class="sxs-lookup"><span data-stu-id="9fd36-163">Data entity for expense field visibility</span></span>
- <span data-ttu-id="9fd36-164">每日津貼費用項目</span><span class="sxs-lookup"><span data-stu-id="9fd36-164">Entry for per-diem expenses</span></span>
- <span data-ttu-id="9fd36-165">明細層級工作流程</span><span class="sxs-lookup"><span data-stu-id="9fd36-165">Line-level workflow</span></span>
- <span data-ttu-id="9fd36-166">暫時核准者支援</span><span class="sxs-lookup"><span data-stu-id="9fd36-166">Interim approver support</span></span>
- <span data-ttu-id="9fd36-167">進階逐條列舉</span><span class="sxs-lookup"><span data-stu-id="9fd36-167">Advanced itemization</span></span>
