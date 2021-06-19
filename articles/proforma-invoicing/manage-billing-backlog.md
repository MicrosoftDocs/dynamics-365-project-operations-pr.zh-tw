---
title: 管理帳務積存
description: 本主題提供有關如何在 Project Operations 中檢視和處理帳務積存的資訊。
author: rumant
ms.date: 04/05/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d7c242937cd9dd277f8d92b7a29333c1fa272e5f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6011901"
---
# <a name="manage-billing-backlog"></a><span data-ttu-id="62d23-103">管理帳務積存</span><span class="sxs-lookup"><span data-stu-id="62d23-103">Manage billing backlog</span></span>

<span data-ttu-id="62d23-104">**適用於：** 資源/非庫存型案例適用的 Project Operations</span><span class="sxs-lookup"><span data-stu-id="62d23-104">_ **Applies To:** Project Operations for resource/non-stocked based scenarios</span></span>

<span data-ttu-id="62d23-105">Dynamics 365 Project Operations 有可協助管理帳務積存的專用檢視表。</span><span class="sxs-lookup"><span data-stu-id="62d23-105">Dynamics 365 Project Operations has dedicated views to help manage the billing backlog.</span></span> <span data-ttu-id="62d23-106">若要管理帳務積存，請在 **帳務** 底下選取 **銷售** 區域中的連結。</span><span class="sxs-lookup"><span data-stu-id="62d23-106">To manage the billing backlog, select the links in the **Sales** area, under **Billing**.</span></span> 

<span data-ttu-id="62d23-107">可以使用下列檢視表：</span><span class="sxs-lookup"><span data-stu-id="62d23-107">The following views available:</span></span>

- <span data-ttu-id="62d23-108">保留款和預付款</span><span class="sxs-lookup"><span data-stu-id="62d23-108">Retainers and Advances</span></span>
- <span data-ttu-id="62d23-109">可用的保留款和預付款</span><span class="sxs-lookup"><span data-stu-id="62d23-109">Available Retainers and Advances</span></span>
- <span data-ttu-id="62d23-110">固定價格里程碑</span><span class="sxs-lookup"><span data-stu-id="62d23-110">Fixed Price Milestones</span></span>
- <span data-ttu-id="62d23-111">時間和資料帳務積存</span><span class="sxs-lookup"><span data-stu-id="62d23-111">Time and Material Billing Backlog</span></span>

## <a name="retainers-and-advances"></a><span data-ttu-id="62d23-112">保留款和預付款</span><span class="sxs-lookup"><span data-stu-id="62d23-112">Retainers and Advances</span></span>

<span data-ttu-id="62d23-113">**保留款和預付款** 檢視表會列出所有專案合約上的保留款和預付款。</span><span class="sxs-lookup"><span data-stu-id="62d23-113">The **Retainers and Advances** view lists the retainers and advances across all project contracts.</span></span> <span data-ttu-id="62d23-114">開立保留款或預付金的發票之後，預付款的金額即可供使用。</span><span class="sxs-lookup"><span data-stu-id="62d23-114">After a retainer or advance is invoiced, the amount of the advance becomes available to use.</span></span>

## <a name="available-retainers-and-advances"></a><span data-ttu-id="62d23-115">可用的保留款和預付款</span><span class="sxs-lookup"><span data-stu-id="62d23-115">Available Retainers and Advances</span></span>

<span data-ttu-id="62d23-116">**可用的保留款和預付款** 檢視表會列出所有專案合約上所有可用的保留款和預付款。</span><span class="sxs-lookup"><span data-stu-id="62d23-116">The **Available Retainers and Advances** view lists all available retainers and advances across all project contracts.</span></span> <span data-ttu-id="62d23-117">開立保留款或預付金的發票之後，預付款的金額即可供使用，並且會新增至清單。</span><span class="sxs-lookup"><span data-stu-id="62d23-117">After a retainer or advance is invoiced, the amount of the advance becomes available to use and is added to the list.</span></span> <span data-ttu-id="62d23-118">完全使用了保留款和預付款的金額之後，就會從清單中移除。</span><span class="sxs-lookup"><span data-stu-id="62d23-118">After the amount of the retainer or advance is used completely, it's removed from the list.</span></span>

## <a name="fixed-price-milestones"></a><span data-ttu-id="62d23-119">固定價格里程碑</span><span class="sxs-lookup"><span data-stu-id="62d23-119">Fixed Price Milestones</span></span>

<span data-ttu-id="62d23-120">**固定價格里程碑** 檢視表會列出所有合約服務內容上的所有固定價格里程碑。</span><span class="sxs-lookup"><span data-stu-id="62d23-120">The **Fixed Price Milestones** view lists all fixed price milestones across all project contract lines.</span></span> <span data-ttu-id="62d23-121">從此檢視表中，可以將單一或多個里程碑標示為 **已準備好開立發票** 或 **尚未準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="62d23-121">From this view, single or multiple milestones can be marked as **Ready to invoice** or **Not ready to invoice**.</span></span> <span data-ttu-id="62d23-122">將里程碑標示為 **已準備好開立發票**，會使其可供放入草稿發票中。</span><span class="sxs-lookup"><span data-stu-id="62d23-122">Marking a milestone as **Ready to invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="62d23-123">多客戶合約服務內容採用固定價格帳務方式時，系統會為合約服務內容上的每個客戶建立里程碑。</span><span class="sxs-lookup"><span data-stu-id="62d23-123">When multi-customer contract lines have a fixed price billing method, a milestone is created for each customer on the contract line.</span></span> <span data-ttu-id="62d23-124">您可以建立里程碑，然後將其分割成個別客戶專屬的里程碑記錄。</span><span class="sxs-lookup"><span data-stu-id="62d23-124">A milestone can be created and then split into individual customer-specific milestone records.</span></span> <span data-ttu-id="62d23-125">此分割是在內部產生，並依照合約服務內容為每個客戶定義的帳單分割百分比來進行。</span><span class="sxs-lookup"><span data-stu-id="62d23-125">This split is internal and in accordance with the billing percentage split defined for each customer on the contract line.</span></span> <span data-ttu-id="62d23-126">在 **固定價格里程碑** 檢視表中，您會看到個別客戶專屬的里程碑記錄。</span><span class="sxs-lookup"><span data-stu-id="62d23-126">In the **Fixed Price Milestones** view, you will see the individual customer-specific milestone records.</span></span> <span data-ttu-id="62d23-127">這其中每一個里程碑記錄都可以分別從此檢視表中標示為 **已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="62d23-127">Each of these milestone records can be marked as **Ready to Invoice** separately from this view.</span></span> <span data-ttu-id="62d23-128">將一個或多個相關里程碑分割標示為 **已準備好開立發票** 時，標題狀態會從 **未開始** 更新為 **進行中**。</span><span class="sxs-lookup"><span data-stu-id="62d23-128">When one or more of the related milestone splits are marked as **Ready to Invoice**, the header status updates to **In Progress** from **Not Started**.</span></span> <span data-ttu-id="62d23-129">當所有里程碑分割都已開立發票時，標題里程碑狀態會更新為 **已完成**。</span><span class="sxs-lookup"><span data-stu-id="62d23-129">When all of the milestone splits are invoiced, the header milestone status updates to **Completed**.</span></span>

<span data-ttu-id="62d23-130">草稿發票上的里程碑會以 **客戶發票已建立** 的帳單狀態顯示在此檢視表中。</span><span class="sxs-lookup"><span data-stu-id="62d23-130">A milestone on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="62d23-131">草稿發票已確認時，該記錄的帳單狀態會更新為 **客戶發票已過帳**。</span><span class="sxs-lookup"><span data-stu-id="62d23-131">When the draft invoice is confirmed, the billing status on the record is updated to **Customer Invoice Posted**.</span></span> 

> [!NOTE] 
> <span data-ttu-id="62d23-132">不要使用自訂程式碼更新此狀態值。</span><span class="sxs-lookup"><span data-stu-id="62d23-132">Do not update this status value by using custom code.</span></span> <span data-ttu-id="62d23-133">使用自訂程式碼更新這些狀態值時，Project Operations 將無法正確運作。</span><span class="sxs-lookup"><span data-stu-id="62d23-133">Project Operations doesn't function correctly when these status values are updated with custom code.</span></span>

## <a name="time-and-material-billing-backlog"></a><span data-ttu-id="62d23-134">時間和資料帳務積存</span><span class="sxs-lookup"><span data-stu-id="62d23-134">Time and Material Billing Backlog</span></span>

<span data-ttu-id="62d23-135">**時間和材料帳務積存** 檢視表會列出系統中所有專案合約上的所有尚未開立發票的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="62d23-135">The **Time and Material Billing Backlog** view lists all unbilled sales actuals across all project contracts in the system that haven't been invoiced.</span></span> <span data-ttu-id="62d23-136">可以透過此檢視表將單一或多個未開單銷售實際值標示為 **已準備好開立發票** 或 **尚未準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="62d23-136">Single or multiple unbilled sales actuals can be marked as **Ready to Invoice** or **Not Ready to Invoice** from this view.</span></span> <span data-ttu-id="62d23-137">將未開單銷售實際值標示為 **已準備好開立發票**，此實際值即可用來放置在草稿發票上。</span><span class="sxs-lookup"><span data-stu-id="62d23-137">Marking an unbilled sales actual as **Ready to Invoice** makes it available to be put on a draft invoice.</span></span>

<span data-ttu-id="62d23-138">**不得超過** 狀態為 **失敗** 的未開單銷售實際值無法標示為 **已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="62d23-138">Unbilled sales actuals with a **Not-to-Exceed** status of **Failed** can't be marked as **Ready to Invoice**.</span></span> <span data-ttu-id="62d23-139">如果需要將實際值標示為 **已準備好開立發票**，請在已認可的合約服務內容上重設其他實際值的狀態，然後重新評估 **不得超過** 狀態。</span><span class="sxs-lookup"><span data-stu-id="62d23-139">If the actuals need to be marked as **Ready to Invoice**, reset the status on other actuals on the contract line that are committed, and then re-evaluate the **Not-to-Exceed** status.</span></span>

<span data-ttu-id="62d23-140">如果多客戶合約服務內容採用時間和材料帳單方式，當時間和費用獲得核准時，系統會根據每位客戶定義的帳單百分比分割，為合約服務內容上的每個客戶都建立一個未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="62d23-140">If multi-customer contract lines have a time and material billing method, when time and expenses are approved, one unbilled sales actual is created for each customer on the contract line according to the billing percentage split defined for each of the customers.</span></span> <span data-ttu-id="62d23-141">在 **時間和材料帳務積存** 檢視表中，您會看到這些客戶專屬的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="62d23-141">In the **Time and Material Billing Backlog** view, you will see these individual customer-specific unbilled sales actuals.</span></span> <span data-ttu-id="62d23-142">這其中每一個未開單銷售實際值記錄都可以分別從此檢視表中標示為 **已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="62d23-142">Each of these unbilled sales actual records can be marked as **Ready to Invoice** separately from this view.</span></span>

<span data-ttu-id="62d23-143">草稿發票上的未開單銷售實際值會以 **客戶發票已建立** 的帳單狀態顯示在此檢視表中。</span><span class="sxs-lookup"><span data-stu-id="62d23-143">An unbilled sales actual that's on a draft invoice is shown in this view with a billing status of **Customer Invoice Created**.</span></span> <span data-ttu-id="62d23-144">確認草稿發票時，此記錄的帳單狀態會更新為 **客戶發票已過帳**。</span><span class="sxs-lookup"><span data-stu-id="62d23-144">When the draft invoice is confirmed, the billing status on this record is updated to **Customer Invoice Posted**.</span></span> 

> [!NOTE] 
> <span data-ttu-id="62d23-145">不要使用自訂程式碼更新此狀態值。</span><span class="sxs-lookup"><span data-stu-id="62d23-145">Do not update this status value by using custom code.</span></span> <span data-ttu-id="62d23-146">使用自訂程式碼更新這些狀態值時，Project Operations 將無法正確運作。</span><span class="sxs-lookup"><span data-stu-id="62d23-146">Project Operations doesn't function correctly when these status values are updated with custom code.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
