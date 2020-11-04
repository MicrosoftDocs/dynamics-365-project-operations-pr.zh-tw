---
title: 建立和套用供應商付款保留條款
description: 本主題提供有關如何設定和維護供應商付款保留條款的資訊。
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 1970a24a5073de6af43db1f1c068332c9ba9c8fe
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073133"
---
# <a name="create-and-apply-vendor-payment-retention-terms"></a><span data-ttu-id="5a26f-103">建立和套用供應商付款保留條款</span><span class="sxs-lookup"><span data-stu-id="5a26f-103">Create and apply vendor payment retention terms</span></span>

[!include [banner](../includes/banner.md)] 

<span data-ttu-id="5a26f-104">您的組織想要保留一部分支付供應商的款項時，為專案設定供應商付款保留條款十分有用。</span><span class="sxs-lookup"><span data-stu-id="5a26f-104">Setting up vendor payment retention terms for a project is useful when your organization wants to retain part of the payments made to a vendor.</span></span> <span data-ttu-id="5a26f-105">例如，當您想要在交貨的產品符合您的期望之前扣留對供應商的付款時。</span><span class="sxs-lookup"><span data-stu-id="5a26f-105">For example, when you want to hold payment to a vendor until the products delivered meet your expectations.</span></span> <span data-ttu-id="5a26f-106">協商供應商合約時，您可以指定供應商付款保留條款。</span><span class="sxs-lookup"><span data-stu-id="5a26f-106">Vendor payment retention terms can be specified when you negotiate a vendor contract.</span></span>

## <a name="create-vendor-payment-retention-terms"></a><span data-ttu-id="5a26f-107">建立供應商付款保留條款</span><span class="sxs-lookup"><span data-stu-id="5a26f-107">Create vendor payment retention terms</span></span>

<span data-ttu-id="5a26f-108">您可以輸入保留支付供應商款項的百分比，以及先前保留金額要發還的百分比。</span><span class="sxs-lookup"><span data-stu-id="5a26f-108">You can enter the percentage of vendor payment for retention and the percentage of the previously retained amounts to be released.</span></span> <span data-ttu-id="5a26f-109">金額會自動保留在供應商發票上，直到合約達到指定的完成狀態。</span><span class="sxs-lookup"><span data-stu-id="5a26f-109">Amounts are automatically retained on vendor invoices until the contract reaches the specified state of completion.</span></span> <span data-ttu-id="5a26f-110">設定保留條款之後，您可以將這些條款套用至該供應商的任何專案。</span><span class="sxs-lookup"><span data-stu-id="5a26f-110">After you set up the retention terms, you can apply them to any project for that vendor.</span></span>

<span data-ttu-id="5a26f-111">使用下列步驟，設定並維護供應商付款保留條款。</span><span class="sxs-lookup"><span data-stu-id="5a26f-111">Use the following steps to set up and maintain retention terms for vendor payments.</span></span> 

1. <span data-ttu-id="5a26f-112">移至 **專案管理與會計** > **保留** > **供應商付款保留條款** 。</span><span class="sxs-lookup"><span data-stu-id="5a26f-112">Go to **Project management and accounting** > **Retention** > **Vendor payment retention terms**.</span></span>
2. <span data-ttu-id="5a26f-113">選取 **新增** 以新增供應商付款保留條款。</span><span class="sxs-lookup"><span data-stu-id="5a26f-113">Select **New** to add a new vendor retention term.</span></span> <span data-ttu-id="5a26f-114">系統會自動輸入新條款的 **規則識別碼** 值。</span><span class="sxs-lookup"><span data-stu-id="5a26f-114">The **Rule ID** value for the new term is automatically entered.</span></span> 
3. <span data-ttu-id="5a26f-115">在 **描述** 欄位中輸入簡短描述，然後在 **條款** 快速分頁中選取 **新增明細** 以輸入下列各項的條款值：</span><span class="sxs-lookup"><span data-stu-id="5a26f-115">Enter a brief description in the **Description** field, and on the **Terms** FastTab, select **Add line** to enter term values for the following:</span></span>

   - <span data-ttu-id="5a26f-116">**交貨單位百分比** ：輸入條款的完成百分比。</span><span class="sxs-lookup"><span data-stu-id="5a26f-116">**Percentage of units delivered** : Enter a percentage of completion for the term.</span></span> <span data-ttu-id="5a26f-117">金額會自動保留在供應商發票上，直到專案完工程度等於指定的百分比為止。</span><span class="sxs-lookup"><span data-stu-id="5a26f-117">Amounts are automatically retained on vendor invoices until the project stage of completion is equal to the specified percentage.</span></span> <span data-ttu-id="5a26f-118">例如，如果您輸入 50.00，則金額會保留直到專案完成 50% 為止。</span><span class="sxs-lookup"><span data-stu-id="5a26f-118">For example, if you enter 50.00, amounts are retained until the project is 50 percent completed.</span></span>
   - <span data-ttu-id="5a26f-119">**要保留的百分比** ：輸入要保留的供應商發票金額百分比。</span><span class="sxs-lookup"><span data-stu-id="5a26f-119">**Percentage to retain** : Enter a percentage of the vendor invoice amount to be retained.</span></span> <span data-ttu-id="5a26f-120">例如，如果您輸入 10.00，則會保留供應商發票的 10% 金額，直到專案達到 **交貨單位百分比** 欄位中所設定的完成百分比為止。</span><span class="sxs-lookup"><span data-stu-id="5a26f-120">For example, if you enter 10.00, then 10 percent of the amount on a vendor invoice is retained until the project reaches the percentage of completion as set in the **Percentage of units delivered field**.</span></span>
   - <span data-ttu-id="5a26f-121">**要發還的百分比** ：選取 **新增明細** 以輸入任何先前已保留金額按照選定專案完成等級所要發還的百分比。</span><span class="sxs-lookup"><span data-stu-id="5a26f-121">**Percentage to release** : Select **Add line** to enter a percentage of any previously retained amounts to be released for the selected level of project completion.</span></span>

> [!NOTE]
> <span data-ttu-id="5a26f-122">如果您有多個不同專案完成等級的里程碑，請為每個保留規則輸入個別供應商付款保留條款。</span><span class="sxs-lookup"><span data-stu-id="5a26f-122">If you have more than one milestone for different levels of project completion, enter a separate vendor retention term line for each retention rule.</span></span> <span data-ttu-id="5a26f-123">每條明細都可以針對每個規定的專案完成等級指定不同的保留百分比和不同的發還百分比。</span><span class="sxs-lookup"><span data-stu-id="5a26f-123">Each line can specify a different retention percentage and a different release percentage for each designated level of project completion.</span></span>

<span data-ttu-id="5a26f-124">建立供應商的供應商付款保留條款之後，您可以將這些條款套用至專案。</span><span class="sxs-lookup"><span data-stu-id="5a26f-124">After you create vendor retention terms for a vendor, you can apply the terms to a project.</span></span>

## <a name="apply-vendor-retention-terms-to-a-project"></a><span data-ttu-id="5a26f-125">將供應商付款保留條款套用至專案</span><span class="sxs-lookup"><span data-stu-id="5a26f-125">Apply vendor retention terms to a project</span></span>

1. <span data-ttu-id="5a26f-126">移至 **專案管理與會計** > **專案** > **所有專案** ，然後從專案清單頁面開啟專案。</span><span class="sxs-lookup"><span data-stu-id="5a26f-126">Go to **Project management and accounting** > **Projects** > **All projects** and open a project from the project list page.</span></span>
2. <span data-ttu-id="5a26f-127">在 **供應商合約** 快速分頁中，選取 **新增明細** 。</span><span class="sxs-lookup"><span data-stu-id="5a26f-127">On the **Vendor agreements** FastTab, select **Add line**.</span></span>
3. <span data-ttu-id="5a26f-128">在 **客戶代碼** 欄位中，選取下列其中一個選項：</span><span class="sxs-lookup"><span data-stu-id="5a26f-128">In the **Account code field** , select one of the following options:</span></span> 

   - <span data-ttu-id="5a26f-129">**表格** ：供應商付款保留條款適用於單一供應商。</span><span class="sxs-lookup"><span data-stu-id="5a26f-129">**Table** : The vendor retention terms apply to a single vendor.</span></span>
   - <span data-ttu-id="5a26f-130">**群組** ：供應商付款保留條款適用於供應商群組中的所有供應商。</span><span class="sxs-lookup"><span data-stu-id="5a26f-130">**Group** : The vendor retention terms apply to all vendors in a vendor group.</span></span>
   - <span data-ttu-id="5a26f-131">**全部** ：供應商付款保留條款適用於所有供應商。</span><span class="sxs-lookup"><span data-stu-id="5a26f-131">**All** : The vendor retention terms apply to all vendors.</span></span>

4. <span data-ttu-id="5a26f-132">在 **供應商/供應商群組** 欄位中，選取套用供應商付款保留條款的供應商或供應商群組。</span><span class="sxs-lookup"><span data-stu-id="5a26f-132">In the **Vendor/Vendor group field** , select the vendor or vendor group to which the vendor retention terms apply.</span></span> <span data-ttu-id="5a26f-133">如果在上一個步驟中選取 **全部** ，則此欄位無法使用。</span><span class="sxs-lookup"><span data-stu-id="5a26f-133">If you selected **All** in the previous step, this field is unavailable.</span></span>
5. <span data-ttu-id="5a26f-134">在 **供應商付款保留條款** 欄位中，選取您在上一個步驟中建立的保留條款。</span><span class="sxs-lookup"><span data-stu-id="5a26f-134">In the **Vendor retention terms** field, select the retention terms that you created in the previous procedure.</span></span>
6. <span data-ttu-id="5a26f-135">如果供應商的專案還有設定背靠背 (PWP) 條款，請在 **PWP 閾值百分比** 欄位中輸入專案的閾值百分比。</span><span class="sxs-lookup"><span data-stu-id="5a26f-135">If the project also has pay-when-paid (PWP) terms set up for the vendor, enter the threshold percentage for the project in the **PWP threshold percentage** field.</span></span>

<span data-ttu-id="5a26f-136">供應商付款保留條款也會顯示在您為供應商建立的採購單上。</span><span class="sxs-lookup"><span data-stu-id="5a26f-136">The vendor retention terms are also displayed on purchase orders that you create for the vendor.</span></span>
