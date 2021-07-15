---
title: 更正草稿專案發票提案的會計處理
description: 本主題說明如何調整草稿發票提案中的會計相關資訊。
author: sigitac
ms.date: 06/07/2021
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 387dc9a81db9c22f170b664152cbafeddf72d149
ms.sourcegitcommit: e93f436afbb92a312fc71b6371866f01927e49d5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/14/2021
ms.locfileid: "6251186"
---
# <a name="correct-the-accounting-on-draft-project-invoice-proposals"></a><span data-ttu-id="43c2b-103">更正草稿專案發票提案的會計處理</span><span class="sxs-lookup"><span data-stu-id="43c2b-103">Correct the accounting on draft project invoice proposals</span></span>

<span data-ttu-id="43c2b-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="43c2b-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="43c2b-105">專案發票的 *營運詳細資料* 是由預估發票上的專案經理進行維護。</span><span class="sxs-lookup"><span data-stu-id="43c2b-105">*Operational details* for project invoices are maintained by the project manager on a pro forma invoice.</span></span> <span data-ttu-id="43c2b-106">這些詳細資料包含有關必須開立發票之工時、費用、材料或里程碑的決定；費率；以及預付款與保留款金額的申請。</span><span class="sxs-lookup"><span data-stu-id="43c2b-106">These details include the decision about the hours, expenses, materials, or milestones that must be invoiced, the rates, and the application of advance and retainer amounts.</span></span> <span data-ttu-id="43c2b-107">確認原始預估發票後，您可建立並確認[更正預估發票](../proforma-invoicing/corrective-invoices.md)，以調整營運詳細資料。</span><span class="sxs-lookup"><span data-stu-id="43c2b-107">After you confirm the original pro forma invoice, you can adjust the operational details by creating and confirming a [corrective pro forma invoice](../proforma-invoicing/corrective-invoices.md).</span></span>

<span data-ttu-id="43c2b-108">專案發票的 *會計詳細資料* 是在客戶面向發票單據中進行維護。</span><span class="sxs-lookup"><span data-stu-id="43c2b-108">*Accounting details* for project invoices are maintained in a customer-facing invoice document.</span></span> <span data-ttu-id="43c2b-109">這些詳細資料包含套用至發票的銷售稅計算和財務維度。</span><span class="sxs-lookup"><span data-stu-id="43c2b-109">These details include the sales tax calculation and the financial dimensions that are applied to the invoice.</span></span> <span data-ttu-id="43c2b-110">本主題提供有關如何在草稿專案發票提案中調整這些會計詳細資料的詳細資訊。</span><span class="sxs-lookup"><span data-stu-id="43c2b-110">This topic provides details about how these accounting details can be adjusted on a draft project invoice proposal.</span></span>

## <a name="adjust-sales-tax"></a><span data-ttu-id="43c2b-111">調整銷售稅金</span><span class="sxs-lookup"><span data-stu-id="43c2b-111">Adjust sales tax</span></span>

<span data-ttu-id="43c2b-112">在發票提案文件中，可以直接調整預設帳單銷售稅群組和項目銷售稅群組。</span><span class="sxs-lookup"><span data-stu-id="43c2b-112">Default billing sales tax groups and item sales tax groups can be adjusted directly on the invoice proposal document.</span></span> <span data-ttu-id="43c2b-113">若要調整這些群組，請選取 **編輯**，然後在每個專案發票提案明細的 **銷售稅群組** 或 **項目銷售稅群組** 欄位中輸入新值。</span><span class="sxs-lookup"><span data-stu-id="43c2b-113">To adjust these groups, select **Edit**, and then, on each project invoice proposal line, enter a new value in the **Sales tax group** or **Item sales tax group** field.</span></span>

## <a name="adjust-financial-dimensions"></a><span data-ttu-id="43c2b-114">調整財務維度</span><span class="sxs-lookup"><span data-stu-id="43c2b-114">Adjust financial dimensions</span></span>

<span data-ttu-id="43c2b-115">在專案發票提案明細上，無法直接編輯財務維度。</span><span class="sxs-lookup"><span data-stu-id="43c2b-115">Financial dimensions can't be edited directly on a project invoice proposal line.</span></span> <span data-ttu-id="43c2b-116">相反地，請依照下列步驟，調整專案發票提案上的財務維度。</span><span class="sxs-lookup"><span data-stu-id="43c2b-116">Instead, follow these steps to adjust financial dimensions on a project invoice proposal.</span></span>

1. <span data-ttu-id="43c2b-117">在專案發票提案中，選取 **全部刪除** 以移除專案發票提案明細。</span><span class="sxs-lookup"><span data-stu-id="43c2b-117">On the project invoice proposal, select **Delete all** to remove the project invoice proposal lines.</span></span>

    > [!NOTE]
    > <span data-ttu-id="43c2b-118">只有在系統管理員啟用 **功能管理** 工作區中的 **使用資源型/非庫存案例適用的 Project Operations 時刪除發票提案明細** 之後，才可使用 **全部刪除** 按鈕 。</span><span class="sxs-lookup"><span data-stu-id="43c2b-118">The **Delete all** button is available only after the system administrator enables the **Delete invoice proposal lines when using Project Operations for resource based/ non-stocked scenarios** feature in the **Feature management** workspace.</span></span>

2. <span data-ttu-id="43c2b-119">調整財務維度：</span><span class="sxs-lookup"><span data-stu-id="43c2b-119">Adjust the financial dimensions:</span></span>

    - <span data-ttu-id="43c2b-120">**分期付款交易 (帳單里程碑)：** 移至 **所有專案** \> **管理** \> **分期付款交易**，並選取需要調整的里程碑。</span><span class="sxs-lookup"><span data-stu-id="43c2b-120">**On-account transactions (billing milestones):** Go to **All projects** \> **Manage** \> **On-account transactions**, and select the milestone that requires adjustment.</span></span> <span data-ttu-id="43c2b-121">然後，在 **財務維度** 索引標籤上，視需要更新各值。</span><span class="sxs-lookup"><span data-stu-id="43c2b-121">Then, on the **Financial dimensions** tab, update the values as required.</span></span>
    - <span data-ttu-id="43c2b-122">**時間、費用及材料交易：** 在 **已過帳的專案交易** 頁面上，選取 **調整會計** 以更新財務維度。</span><span class="sxs-lookup"><span data-stu-id="43c2b-122">**Time, expense, and material transactions:** On the **Posted project transactions** page, select **Adjust accounting** to update the financial dimensions.</span></span>

3. <span data-ttu-id="43c2b-123">完成財務維度值的調整後，移至 **專案管理與會計** \> **週期** \> **Project Operations 整合**，然後選取 **從臨時表格匯入** 以執行定期程序。</span><span class="sxs-lookup"><span data-stu-id="43c2b-123">After you've finished adjusting the financial dimension values, go to **Project management and accounting** \> **Periodic** \> **Project Operations integration**, and select **Import from staging table** to run the periodic process.</span></span> <span data-ttu-id="43c2b-124">該程序會使用更新的財務維度值來重新建立專案發票提案明細。</span><span class="sxs-lookup"><span data-stu-id="43c2b-124">That process uses the updated financial dimension values to re-create the project invoice proposal lines.</span></span> <span data-ttu-id="43c2b-125">接著會在過帳專案發票時，將更新的值用於子分類帳和總分類帳。</span><span class="sxs-lookup"><span data-stu-id="43c2b-125">The updated values are then used in the project subledger and general ledger when the project invoice is posted.</span></span>
