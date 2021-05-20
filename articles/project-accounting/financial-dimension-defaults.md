---
title: 財務維度預設值
description: 本主題提供有關如何設定財務維度預設值的資訊。
author: sigitac
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 0a76447bb1a81a7157fccc0cd58eddd1eb5995de
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950119"
---
# <a name="financial-dimension-defaults"></a><span data-ttu-id="8ce88-103">財務維度預設值</span><span class="sxs-lookup"><span data-stu-id="8ce88-103">Financial dimension defaults</span></span>

<span data-ttu-id="8ce88-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="8ce88-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="8ce88-105">Dynamics 365 Project Operations 使用 Dynamics 365 Finance 中的[財務維度](/dynamics365/finance/general-ledger/financial-dimensions)架構，提供對專案子分類帳及總帳交易的其他見解。</span><span class="sxs-lookup"><span data-stu-id="8ce88-105">Dynamics 365 Project Operations uses the [Financial dimensions](/dynamics365/finance/general-ledger/financial-dimensions) framework in Dynamics 365 Finance to provide additional insights on project subledger and general ledger transactions.</span></span>

<span data-ttu-id="8ce88-106">您可以在客戶、專案資金來源、里程碑、專案合約服務內容或專案上設定預設財務維度。</span><span class="sxs-lookup"><span data-stu-id="8ce88-106">Default financial dimensions can be set on a customer, project funding source, milestone, project contract line, or project.</span></span>

## <a name="define-default-financial-dimensions-for-a-customer"></a><span data-ttu-id="8ce88-107">定義客戶的預設財務維度</span><span class="sxs-lookup"><span data-stu-id="8ce88-107">Define default financial dimensions for a customer</span></span>

<span data-ttu-id="8ce88-108">客戶維度預設值是在 Finance 中進行指定。</span><span class="sxs-lookup"><span data-stu-id="8ce88-108">Customer dimension defaults are specified in Finance.</span></span> <span data-ttu-id="8ce88-109">請完成下列步驟，以設定維度預設值。</span><span class="sxs-lookup"><span data-stu-id="8ce88-109">Complete the following steps to set dimension defaults.</span></span>

1. <span data-ttu-id="8ce88-110">移至 **應收帳款** > **客戶** > **所有客戶**。</span><span class="sxs-lookup"><span data-stu-id="8ce88-110">Go to **Accounts receivable** > **Customers** > **All customers**.</span></span>
2. <span data-ttu-id="8ce88-111">在 **客戶** 頁面的 **財務維度** 索引標籤中，設定特定客戶的財務維度值。</span><span class="sxs-lookup"><span data-stu-id="8ce88-111">On the **Customers** page, on the **Financial dimensions** tab, set the financial dimension values for specific customer.</span></span>

## <a name="define-default-financial-dimensions-for-project-contracts"></a><span data-ttu-id="8ce88-112">定義專案合約的預設財務維度</span><span class="sxs-lookup"><span data-stu-id="8ce88-112">Define default financial dimensions for project contracts</span></span>

<span data-ttu-id="8ce88-113">專案合約是在 Common Data Service (CDS) 中建立並進行維護。</span><span class="sxs-lookup"><span data-stu-id="8ce88-113">Project contracts are created and maintained in Common Data Service (CDS).</span></span> <span data-ttu-id="8ce88-114">專案合約的會計屬性是在 Finance 的 **專案管理與會計** 模組進行設定。</span><span class="sxs-lookup"><span data-stu-id="8ce88-114">Accounting attributes for project contracts are set in the **Project management and accounting** module in Finance.</span></span>

### <a name="set-financial-dimensions-for-a-project-funding-source"></a><span data-ttu-id="8ce88-115">設定專案資金來源的財務維度</span><span class="sxs-lookup"><span data-stu-id="8ce88-115">Set financial dimensions for a project funding source</span></span>

1. <span data-ttu-id="8ce88-116">移至 **專案管理與會計** > **專案** > **專案合約**。</span><span class="sxs-lookup"><span data-stu-id="8ce88-116">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="8ce88-117">選取要更新的記錄，然後選取 **專案合約** 索引標籤中的 **顯示預設會計**。</span><span class="sxs-lookup"><span data-stu-id="8ce88-117">Select the record you want to update, and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="8ce88-118">展開 **相關資訊**，然後選取 **資金來源** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="8ce88-118">Expand **Related information** and select the **Funding sources** tab.</span></span>
4. <span data-ttu-id="8ce88-119">設定財務維度預設值。</span><span class="sxs-lookup"><span data-stu-id="8ce88-119">Set the financial dimension defaults.</span></span> <span data-ttu-id="8ce88-120">請注意，預設會使用客戶帳戶中的財務維度。</span><span class="sxs-lookup"><span data-stu-id="8ce88-120">Notice that the financial dimensions default from the customer account.</span></span>

### <a name="set-financial-dimensions-for-a-project-contract-line"></a><span data-ttu-id="8ce88-121">設定專案合約服務內容的財務維度</span><span class="sxs-lookup"><span data-stu-id="8ce88-121">Set financial dimensions for a project contract line</span></span>

1. <span data-ttu-id="8ce88-122">移至 **專案管理與會計** > **專案** > **專案合約**。</span><span class="sxs-lookup"><span data-stu-id="8ce88-122">Go to **Project management and accounting** > **Projects** > **Project contracts**.</span></span>
2. <span data-ttu-id="8ce88-123">選取要更新的記錄，並選取 **專案合約** 索引標籤中的 **顯示預設會計**。</span><span class="sxs-lookup"><span data-stu-id="8ce88-123">Select the record you want to update and on the **Project contract** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="8ce88-124">展開 **相關資訊**，然後選取 **合約服務內容** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="8ce88-124">Expand **Related information** and select the **Contract lines** tab.</span></span>
4. <span data-ttu-id="8ce88-125">設定財務維度預設值。</span><span class="sxs-lookup"><span data-stu-id="8ce88-125">Set the financial dimension defaults.</span></span> <span data-ttu-id="8ce88-126">財務維度預設值可適用，並且只能與固定價格 (里程碑) 合約服務內容搭配使用。</span><span class="sxs-lookup"><span data-stu-id="8ce88-126">The financial dimension defaults are applicable and can be used only with Fixed price (milestone) contract lines.</span></span>

<span data-ttu-id="8ce88-127">這些預設值是在相關專案記帳交易和發票明細上使用。</span><span class="sxs-lookup"><span data-stu-id="8ce88-127">These defaults are used on related project on-account transactions and invoice lines.</span></span>

## <a name="define-default-financial-dimensions-for-projects"></a><span data-ttu-id="8ce88-128">定義專案的預設財務維度</span><span class="sxs-lookup"><span data-stu-id="8ce88-128">Define default financial dimensions for projects</span></span>

<span data-ttu-id="8ce88-129">專案是在 CDS 中建立並進行維護。</span><span class="sxs-lookup"><span data-stu-id="8ce88-129">Projects are created and maintained in CDS.</span></span> <span data-ttu-id="8ce88-130">專案的會計屬性是在 Finance 的 **專案管理與會計** 模組進行設定。</span><span class="sxs-lookup"><span data-stu-id="8ce88-130">Accounting attributes for projects are set in the **Project management and accounting** module in Finance.</span></span>

1. <span data-ttu-id="8ce88-131">移至 **專案管理與會計** > **專案** > **所有專案**。</span><span class="sxs-lookup"><span data-stu-id="8ce88-131">Go to **Project management and accounting** > **Projects** > **All projects**.</span></span>
2. <span data-ttu-id="8ce88-132">選取要更新的記錄，並選取 **專案** 索引標籤中的 **顯示預設會計**。</span><span class="sxs-lookup"><span data-stu-id="8ce88-132">Select the record that you want to update and on the **Project** tab, select **Show default accounting**.</span></span>
3. <span data-ttu-id="8ce88-133">展開 **相關資訊**，然後選取 **設定** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="8ce88-133">Expand **Related information** and select the **Setup** tab.</span></span>
4. <span data-ttu-id="8ce88-134">設定財務維度預設值。</span><span class="sxs-lookup"><span data-stu-id="8ce88-134">Set the financial dimension defaults.</span></span> <span data-ttu-id="8ce88-135">請注意，預設會使用客戶帳戶中的財務維度。</span><span class="sxs-lookup"><span data-stu-id="8ce88-135">Notice that financial dimensions default from the customer account.</span></span> <span data-ttu-id="8ce88-136">如果專案與包含多個專案合約客戶的合約服務內容相關聯，則會使用主要客戶來設定預設財務維度。</span><span class="sxs-lookup"><span data-stu-id="8ce88-136">If the project is associated with a contract line with multiple project contract customers, the primary customer is used to default financial dimensions.</span></span>

<span data-ttu-id="8ce88-137">專案預設財務維度會在 **Project Operations 整合帳目** 和相關專案發票明細上用來設定時間、費用及服務費交易的帳目明細預設值。</span><span class="sxs-lookup"><span data-stu-id="8ce88-137">Project default financial dimensions are used to set journal line defaults for time, expense, and fee transactions in the **Project Operations Integration Journal** and on related project invoice lines.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]