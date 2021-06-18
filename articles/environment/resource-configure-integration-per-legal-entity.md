---
title: 設定每個法律實體的 Project Operations 整合
description: 本主題提供有關在 Project Operations 中依法律實體設定整合的資訊。
author: sigitac
ms.date: 10/21/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: e5a12de275a9f886434da45fbbed5140e3913d83
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6000066"
---
# <a name="configure-project-operations-integration-per-legal-entity"></a><span data-ttu-id="7e5c6-103">設定每個法律實體的 Project Operations 整合</span><span class="sxs-lookup"><span data-stu-id="7e5c6-103">Configure Project Operations integration per legal entity</span></span> 

<span data-ttu-id="7e5c6-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="7e5c6-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="7e5c6-105">本主題為您逐步解說設定每個法律實體的 Dynamics 365 Project Operations 所需的步驟。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-105">This topic walks you through the steps required to configure Dynamics 365 Project Operations per legal entity.</span></span>

## <a name="enable-feature-keys-in-dynamics-365-finance"></a><span data-ttu-id="7e5c6-106">在 Dynamics 365 Finance 中啟用功能金鑰</span><span class="sxs-lookup"><span data-stu-id="7e5c6-106">Enable feature keys in Dynamics 365 Finance</span></span>

<span data-ttu-id="7e5c6-107">完成下列步驟以啟用必要的功能。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-107">Complete the following steps to enable required features.</span></span>

1. <span data-ttu-id="7e5c6-108">在 Dynamics 365 Finance 中，移至 **功能管理** 工作區。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-108">In Dynamics 365 Finance, go to the **Feature Management** workspace.</span></span>
2. <span data-ttu-id="7e5c6-109">在 **功能** 清單中，尋找並啟用下列功能：</span><span class="sxs-lookup"><span data-stu-id="7e5c6-109">In **Feature list**, find and enable the following features:</span></span>
  
    - <span data-ttu-id="7e5c6-110">**為專案啟用多個合約服務內容**</span><span class="sxs-lookup"><span data-stu-id="7e5c6-110">**Enable multiple contract lines for a project**</span></span>
    - <span data-ttu-id="7e5c6-111">**在 Dynamics 365 Customer Engagement 上啟用 Project Operations**</span><span class="sxs-lookup"><span data-stu-id="7e5c6-111">**Enable Project Operations on Dynamics 365 Customer Engagement**</span></span>

> [!NOTE]
> <span data-ttu-id="7e5c6-112">如果沒有看到 **功能金鑰** 列出，請確認您的 Finance 版本是否符合最低版本需求 (已套用品質更新的應用程式 10.0.13 版或更新版本)。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-112">If you don't see **Feature keys** listed, verify that your Finance version meets the minimum version requirement (application version 10.0.13 with all quality updates applied or higher).</span></span> <span data-ttu-id="7e5c6-113">選取 **檢查更新** 以重新整理功能清單。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-113">Select **Check for updates** to refresh the feature list.</span></span>

## <a name="define-the-project-operations-deployment-scenario-for-a-legal-entity"></a><span data-ttu-id="7e5c6-114">定義法律實體適用的 Project Operations 部署案例</span><span class="sxs-lookup"><span data-stu-id="7e5c6-114">Define the Project Operations deployment scenario for a legal entity</span></span>

<span data-ttu-id="7e5c6-115">您可以在法律實體層級啟用 Dynamics 365 Customer Engagement 上的 Project Operations。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-115">You can enable Project Operations on Dynamics 365 Customer Engagement on a legal entity level.</span></span> <span data-ttu-id="7e5c6-116">您在 Dynamics 365 Customer Engagement 上可以有一個使用資源/非庫存型案例適用 Project Operations 的法律實體。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-116">You can have one legal entity using Project Operations on Dynamics 365 Customer Engagement for resource/non-stocked based scenarios.</span></span> <span data-ttu-id="7e5c6-117">在相同的環境中，您可以有另一個使用庫存/生產訂單案例適用 Project Operations 的法律實體。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-117">In the same environment, you can have another legal entity using Project Operations for stocked/production order scenarios.</span></span>

1. <span data-ttu-id="7e5c6-118">在 Dynamics 365 Finance 中，移至 **專案管理與會計** > **設定** > **全域專案管理與會計參數**。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-118">In Dynamics 365 Finance, go to **Project management and accounting** > **Setup** > **Global project management and accounting parameters**.</span></span>
2. <span data-ttu-id="7e5c6-119">在可用法律實體清單中，選取要在 Dynamics 365 Customer Engagement 功能上啟用多個合約服務內容和 Project Operations 的實體。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-119">In the list of available legal entities, select entities where multiple contract lines and Project Operations on Dynamics 365 Customer Engagement features will be enabled.</span></span> <span data-ttu-id="7e5c6-120">讓將要使用庫存/生產訂單案例適用 Project Operations 的法律實體保持未選取狀態。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-120">Leave legal entities that will be using Project Operations for stocked/production order scenarios unselected.</span></span>

> [!NOTE]
> <span data-ttu-id="7e5c6-121">只有在法律實體未包含任何現有的專案時，才能選取該法律實體。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-121">A legal entity can be selected only if it doesn't have any existing projects.</span></span>

## <a name="configure-project-management-and-accounting-parameters"></a><span data-ttu-id="7e5c6-122">設定專案管理與會計參數</span><span class="sxs-lookup"><span data-stu-id="7e5c6-122">Configure Project management and accounting parameters</span></span>

<span data-ttu-id="7e5c6-123">每個在 Dynamics 365 Customer Engagement 上使用 Project Operations 的法律實體都需要一組預設參數。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-123">Each legal entity using Project Operations on Dynamics 365 Customer Engagement needs a set of default parameters.</span></span> <span data-ttu-id="7e5c6-124">這些參數是在 **專案管理與會計參數** 頁面的 **Project Operations** 索引標籤上進行設定。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-124">These parameters are configured on the **Project Operations** tab on the **Project management and accounting parameters** page.</span></span> <span data-ttu-id="7e5c6-125">這些參數包括：</span><span class="sxs-lookup"><span data-stu-id="7e5c6-125">The parameters are:</span></span>

  - <span data-ttu-id="7e5c6-126">**帳單類型預設值**：Project Operations 使用固定一組必須對應至 Finance 明細屬性的帳單類型預設值。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-126">**Billing type defaults**: Project Operations uses a fixed set of billing type defaults that must be mapped to line properties Finance.</span></span> <span data-ttu-id="7e5c6-127">建立下列每個帳單類型的記錄：**未指定**、**應收費**、**不應收費**、**附贈** 和 **無法使用**。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-127">Create a record for each billing type: **Not specified**, **Chargeable**, **Non-chargeable**, **Complimentary**, and **Not available**.</span></span>
  - <span data-ttu-id="7e5c6-128">**專案類別預設值**：選取每個交易類型要使用的預設專案類別。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-128">**Project category defaults**: Select the default project categories to be used for each transaction type.</span></span> <span data-ttu-id="7e5c6-129">這些預設值將用於 **Project Operations 整合帳目** 以及未指定專案實際值交易類別的估計值。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-129">These defaults will be used in the **Project Operations Integration journal** and in estimates where no transaction category is specified for the project actual.</span></span>
  - <span data-ttu-id="7e5c6-130">**預測**：選取時間和費用估計值要使用的預測模型。</span><span class="sxs-lookup"><span data-stu-id="7e5c6-130">**Forecasts**: Select the forecast model to be used for time and expense estimates.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]