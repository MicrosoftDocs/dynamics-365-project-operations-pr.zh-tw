---
title: 聯邦獎勵支出時間表查詢
description: 這份主題提供「聯邦獎勵支出時間表」查詢的相關資訊。
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010056"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="50a31-103">聯邦獎勵支出時間表查詢</span><span class="sxs-lookup"><span data-stu-id="50a31-103">Schedule of Expenditures of Federal Awards inquiry</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="50a31-104">依據行政管理與預算局通函 A-133 (Office of Management and Budget Circular A-133)，接受聯邦基金資助的機構必須遵守稽核需求規定，這也稱為單一稽核。</span><span class="sxs-lookup"><span data-stu-id="50a31-104">According to Office of Management and Budget Circular A-133, agencies that receive federal funds are subject to audit requirements, which are also known as single audits.</span></span> <span data-ttu-id="50a31-105">稽核程序會用來定期報告聯邦補助款的收入與支出。</span><span class="sxs-lookup"><span data-stu-id="50a31-105">The audit process is used to report on the revenues and expenditures of federal grants on a recurring basis.</span></span> <span data-ttu-id="50a31-106">單一稽核報表的一部分內容會包含聯邦獎勵支出時間表 (Schedule of Expenditures of Federal Awards，SEFA)。</span><span class="sxs-lookup"><span data-stu-id="50a31-106">Part of the single audit report includes the Schedule of Expenditures of Federal Awards (SEFA).</span></span>

<span data-ttu-id="50a31-107">「聯邦獎勵支出時間表」查詢包含聯邦國內補助目錄 (Catalog of Federal Domestic Assistance，CFDA) 標題與編號、授權號碼、補助年度、提供資金的聯邦機構名稱，以及轉手撥款實體的名稱。</span><span class="sxs-lookup"><span data-stu-id="50a31-107">The Schedule of Expenditures of Federal Awards inquiry includes the Catalog of Federal Domestic Assistance (CFDA) title and number, the grant number, the year of the grant, the name of the federal agency that provides the funds, and the name of the pass-through entity.</span></span> <span data-ttu-id="50a31-108">查詢是針對特定期間而為。</span><span class="sxs-lookup"><span data-stu-id="50a31-108">The inquiry is for a specific period.</span></span> <span data-ttu-id="50a31-109">該期間通常與財務報表期間一致，也就是會計年度。</span><span class="sxs-lookup"><span data-stu-id="50a31-109">Typically, that period is the same as the financial statement period, which is a fiscal year.</span></span>

<span data-ttu-id="50a31-110">此查詢包括所選取日期範圍內有預估日期的補助款。</span><span class="sxs-lookup"><span data-stu-id="50a31-110">The inquiry includes grants that have projection dates in the selected date range.</span></span> <span data-ttu-id="50a31-111">查詢的 **補助機構** 欄顯示受補助客戶，或就轉手撥款補助而言，則顯示補助機構。</span><span class="sxs-lookup"><span data-stu-id="50a31-111">The **Grantor agency** column of the inquiry shows the grant customer or, for a pass-through grant, the grantor agency.</span></span> <span data-ttu-id="50a31-112">對於轉手撥款補助，**轉手撥款機構** 欄會顯示受補助客戶。</span><span class="sxs-lookup"><span data-stu-id="50a31-112">For a pass-through grant, the **Pass-through agency** column shows the grant customer.</span></span> <span data-ttu-id="50a31-113">如果補助款不是轉手撥款補助，此 **轉手撥款機構** 欄為空白。</span><span class="sxs-lookup"><span data-stu-id="50a31-113">If the grant isn't a pass-through grant, the **Pass-through agency** column is blank.</span></span>

## <a name="set-up-the-cfda-clusters"></a><span data-ttu-id="50a31-114">設定 CFDA 叢集</span><span class="sxs-lookup"><span data-stu-id="50a31-114">Set up the CFDA clusters</span></span>

<span data-ttu-id="50a31-115">您必須設定 CFDA 叢集，這些叢集可與「聯邦獎勵支出時間表」查詢中的 CFDA 編號產生關聯。</span><span class="sxs-lookup"><span data-stu-id="50a31-115">You must set up the CFDA clusters that can be associated with CFDA numbers in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="50a31-116">Go to **專案管理與會計 \> 設定 \> 補助款 \> 聯邦國內補助目錄叢集**。</span><span class="sxs-lookup"><span data-stu-id="50a31-116">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance clusters**.</span></span>
2. <span data-ttu-id="50a31-117">選取 **新增** 以建立 CFDA 叢集。</span><span class="sxs-lookup"><span data-stu-id="50a31-117">Select **New** to create a CFDA cluster.</span></span>
3. <span data-ttu-id="50a31-118">輸入叢集名稱。</span><span class="sxs-lookup"><span data-stu-id="50a31-118">Enter the cluster name.</span></span>
4. <span data-ttu-id="50a31-119">選取 **儲存** 以儲存變更。</span><span class="sxs-lookup"><span data-stu-id="50a31-119">Select **Save** to save your changes.</span></span>

## <a name="set-up-cfda-numbers"></a><span data-ttu-id="50a31-120">設定 CFDA 編號</span><span class="sxs-lookup"><span data-stu-id="50a31-120">Set up CFDA numbers</span></span>

<span data-ttu-id="50a31-121">您必須設定 CFDA 編號，這些編號可新增至補助款，並加入「聯邦獎勵支出時間表」查詢中。</span><span class="sxs-lookup"><span data-stu-id="50a31-121">You must set up CFDA numbers that can be added to grants and included in the Schedule of Expenditures of Federal Awards inquiry.</span></span>

1. <span data-ttu-id="50a31-122">Go to **專案管理與會計 \> 設定 \> 補助款 \> 聯邦國內補助目錄編號**。</span><span class="sxs-lookup"><span data-stu-id="50a31-122">Go to **Project management and accounting \> Setup \> Grants \> Catalog of Federal Domestic Assistance numbers**.</span></span>
2. <span data-ttu-id="50a31-123">選取 **新增** 以建立 CFDA 編號。</span><span class="sxs-lookup"><span data-stu-id="50a31-123">Select **New** to create a CFDA number.</span></span>
3. <span data-ttu-id="50a31-124">在 **編號** 欄中，輸入 CFDA 編號。</span><span class="sxs-lookup"><span data-stu-id="50a31-124">In the **Number** column, enter the CFDA number.</span></span>
4. <span data-ttu-id="50a31-125">按 **Tab** 鍵。</span><span class="sxs-lookup"><span data-stu-id="50a31-125">Press the **Tab** key.</span></span>
5. <span data-ttu-id="50a31-126">在 **描述** 欄中，輸入 CFDA 標題。</span><span class="sxs-lookup"><span data-stu-id="50a31-126">In the **Description** column, enter the CFDA title.</span></span>
6. <span data-ttu-id="50a31-127">按 **Tab** 鍵。</span><span class="sxs-lookup"><span data-stu-id="50a31-127">Press the **Tab** key.</span></span>
7. <span data-ttu-id="50a31-128">選擇性：在 **程式叢集** 欄位中，新增適當的 CFDA 叢集。</span><span class="sxs-lookup"><span data-stu-id="50a31-128">Optional: In the **Program cluster** field, add the appropriate CFDA cluster.</span></span>
8. <span data-ttu-id="50a31-129">選取 **儲存** 以儲存變更。</span><span class="sxs-lookup"><span data-stu-id="50a31-129">Select **Save** to save your changes.</span></span>

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="50a31-130">設定要申報「聯邦獎勵支出時間表」查詢的補助款</span><span class="sxs-lookup"><span data-stu-id="50a31-130">Set up grants to report for the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="50a31-131">移至 **專案管理與會計 \> 設定 \> 補助款**，然後選取現有的補助款。</span><span class="sxs-lookup"><span data-stu-id="50a31-131">Go to **Project management and accounting \> Grants \> Grants**, and select an existing grant.</span></span>
2. <span data-ttu-id="50a31-132">在 **設定** 快速分頁的 **聯邦國內補助目錄** 欄位中，指派 CFDA 編號。</span><span class="sxs-lookup"><span data-stu-id="50a31-132">On the **Setup** FastTab, in the **Catalog of Federal Domestic Assistance** field, assign the CFDA number.</span></span> <span data-ttu-id="50a31-133">補助款的 CFDA 編號決定要進行申報的 CFDA 叢集。</span><span class="sxs-lookup"><span data-stu-id="50a31-133">The CFDA number on the grant determines the CFDA cluster for reporting.</span></span>
3. <span data-ttu-id="50a31-134">在 **連絡人資訊** 快速分頁中，依照下列步驟輸入贈款者資訊：</span><span class="sxs-lookup"><span data-stu-id="50a31-134">On **Contact information** FastTab, enter the grantor information by following these steps:</span></span>

    1. <span data-ttu-id="50a31-135">在 **受補助客戶** 欄位中，輸入負責撥款的客戶。</span><span class="sxs-lookup"><span data-stu-id="50a31-135">In the **Grant customer** field, enter the customer who is responsible for the grant.</span></span> <span data-ttu-id="50a31-136">如果是目前既有的補助款，可能已經輸入此資訊。</span><span class="sxs-lookup"><span data-stu-id="50a31-136">For an existing grant, this information might already be entered.</span></span>
    2. <span data-ttu-id="50a31-137">指出受補助客戶是否為資助者。</span><span class="sxs-lookup"><span data-stu-id="50a31-137">Indicate whether the grant customer is the funder.</span></span> <span data-ttu-id="50a31-138">如果受補助客戶為資助者，就讓 **轉手撥款** 核取方塊保持清除。</span><span class="sxs-lookup"><span data-stu-id="50a31-138">If the grant customer is the funder, leave the **Pass-through** check box cleared.</span></span> <span data-ttu-id="50a31-139">如果有其他客戶是資助者，而受補助客戶負責支出和追蹤款項時，請選取 **轉手撥款** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="50a31-139">If another customer is the funder, and the grant customer is responsible for spending and tracking the money, select the **Pass-through** check box.</span></span>

4. <span data-ttu-id="50a31-140">如果您在上一個步驟中選取 **轉手撥款** 核取方塊，請在 **補助機構** 欄位中輸入提供補助款的客戶。</span><span class="sxs-lookup"><span data-stu-id="50a31-140">If you selected the **Pass-through** check box in the previous step, in the **Grantor agency** field, enter the customer who provided the grant.</span></span> <span data-ttu-id="50a31-141">補助機構與受補助客戶不可以是相同的客戶。</span><span class="sxs-lookup"><span data-stu-id="50a31-141">The grantor agency and the grant customer can't be the same customer.</span></span>

<span data-ttu-id="50a31-142">以下是轉手撥款補助的範例：</span><span class="sxs-lookup"><span data-stu-id="50a31-142">Here is an example of a pass-through grant:</span></span>

<span data-ttu-id="50a31-143">聯邦政府資助某一州的基礎建設專案。</span><span class="sxs-lookup"><span data-stu-id="50a31-143">The federal government funded an infrastructure project for a state.</span></span> <span data-ttu-id="50a31-144">聯邦政府已提供資金給這個州用於開支。</span><span class="sxs-lookup"><span data-stu-id="50a31-144">The federal government gave the money to the state to spend.</span></span> <span data-ttu-id="50a31-145">在這種情況下，聯邦政府是補助機構，而該州是受補助客戶。</span><span class="sxs-lookup"><span data-stu-id="50a31-145">In this case, the federal government is the grantor agency, and the state is the grant customer.</span></span>

> [!NOTE] 
> <span data-ttu-id="50a31-146">第一次開啟此功能時，系統會使用補助款現有的編號輸入初始 CFDA 編號。</span><span class="sxs-lookup"><span data-stu-id="50a31-146">When you first turn on the feature, initial CFDA numbers will be entered by using the existing numbers on grants.</span></span>

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a><span data-ttu-id="50a31-147">根據補助款類型排除 SEFA 報表中的補助款</span><span class="sxs-lookup"><span data-stu-id="50a31-147">Exclude grants from SEFA reporting based on the grant type</span></span>

1. <span data-ttu-id="50a31-148">移至 **專案管理與會計 \> 設定 \> 補助款 \> 補助款類型**。</span><span class="sxs-lookup"><span data-stu-id="50a31-148">Go to **Project management and accounting \> Setup \> Grants \> Grant types**.</span></span>
2. <span data-ttu-id="50a31-149">在 **預設資訊** 快速分頁上，選取 **從聯邦獎勵支出時間表中排除** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="50a31-149">On the **Default information** FastTab, select the **Exclude from Schedule of Expenditures of Federal Awards** check box.</span></span>
3. <span data-ttu-id="50a31-150">選取 **儲存** 以儲存變更。</span><span class="sxs-lookup"><span data-stu-id="50a31-150">Select **Save** to save your changes.</span></span>

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a><span data-ttu-id="50a31-151">執行「聯邦獎勵支出時間表」查詢</span><span class="sxs-lookup"><span data-stu-id="50a31-151">Run the Schedule of Expenditures of Federal Awards inquiry</span></span>

1. <span data-ttu-id="50a31-152">移至 **專案管理與會計 \> 查詢與報表 \> 補助款查詢 \>聯邦獎勵支出時間表**。</span><span class="sxs-lookup"><span data-stu-id="50a31-152">Go to **Project management and accounting \> Inquiries and reports \> Grant inquiry \> Schedule of Expenditures of Federal Awards**.</span></span>
2. <span data-ttu-id="50a31-153">在 **參數** 區段中，依照下列步驟操作：</span><span class="sxs-lookup"><span data-stu-id="50a31-153">In the **Parameters** section, follow these steps:</span></span>

    1. <span data-ttu-id="50a31-154">在 **日期間隔** 欄位中，選取日期間隔代碼。</span><span class="sxs-lookup"><span data-stu-id="50a31-154">In the **Date interval** field, select the code for the date interval.</span></span> <span data-ttu-id="50a31-155">或者，在 **開始日期** 和 **結束日期** 欄位中，定義日期間隔。</span><span class="sxs-lookup"><span data-stu-id="50a31-155">Alternatively, in the **From date** and **To date** fields, define the date interval.</span></span>
    2. <span data-ttu-id="50a31-156">選用：若是只要包含已開單交易做為查詢中的營收，請將 **僅包含已開單營收** 選項設定為 **是**。</span><span class="sxs-lookup"><span data-stu-id="50a31-156">Optional: To include only billed transactions as revenue in the inquiry, set the **Include only billed revenues** option to **Yes**.</span></span>

## <a name="columns"></a><span data-ttu-id="50a31-157">資料行</span><span class="sxs-lookup"><span data-stu-id="50a31-157">Columns</span></span>

<span data-ttu-id="50a31-158">「聯邦獎勵支出時間表」查詢包含下列各欄：</span><span class="sxs-lookup"><span data-stu-id="50a31-158">The Schedule of Expenditures of Federal Awards inquiry includes the following columns:</span></span>

- <span data-ttu-id="50a31-159">聯邦國內補助目錄叢集名稱</span><span class="sxs-lookup"><span data-stu-id="50a31-159">Catalog of Federal Domestic Assistance cluster name</span></span>
- <span data-ttu-id="50a31-160">補助機構</span><span class="sxs-lookup"><span data-stu-id="50a31-160">Grantor agency</span></span>
- <span data-ttu-id="50a31-161">轉手撥款機構</span><span class="sxs-lookup"><span data-stu-id="50a31-161">Pass-through agency</span></span>
- <span data-ttu-id="50a31-162">補助款名稱</span><span class="sxs-lookup"><span data-stu-id="50a31-162">Grant name</span></span>
- <span data-ttu-id="50a31-163">補助款識別碼</span><span class="sxs-lookup"><span data-stu-id="50a31-163">Grant ID</span></span>
- <span data-ttu-id="50a31-164">補助款申請識別碼</span><span class="sxs-lookup"><span data-stu-id="50a31-164">Grant application ID</span></span>
- <span data-ttu-id="50a31-165">聯邦國內補助目錄</span><span class="sxs-lookup"><span data-stu-id="50a31-165">Catalog of Federal Domestic Assistance</span></span>
- <span data-ttu-id="50a31-166">收據</span><span class="sxs-lookup"><span data-stu-id="50a31-166">Receipts</span></span>
- <span data-ttu-id="50a31-167">支出</span><span class="sxs-lookup"><span data-stu-id="50a31-167">Expenditures</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]