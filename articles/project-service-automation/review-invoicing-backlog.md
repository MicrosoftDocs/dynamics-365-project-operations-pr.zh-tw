---
title: 檢閱專案與專案合約上的開立發票待辦項目
description: 此主題提供有關如何檢閱時間、費用及產品待辦項目的資訊，以及說明如何將這些待辦項目標示為已準備好開立發票。
author: rumant
manager: kfend
ms.service: business-applications
ms.custom:
- dyn365-projectservice
ms.date: 03/11/2019
ms.topic: article
ms.prod: ''
ms.technology: Microsoft Dynamics 365 Project Service Automation 2.x and 3.x
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
ms.openlocfilehash: db15ea136b9939c0a0631936bcadab538bf2dd4a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749964"
---
# <a name="review-the-invoicing-backlog-on-projects-and-project-contracts"></a><span data-ttu-id="030f1-103">檢閱專案與專案合約上的開立發票待辦項目</span><span class="sxs-lookup"><span data-stu-id="030f1-103">Review the invoicing backlog on projects and project contracts</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="030f1-104">當交易已準備好可以建立並處理發票時，該交易應標示**已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="030f1-104">When a transaction is ready to have an invoice created and processed, the transaction should be marked **Ready to invoice**.</span></span> <span data-ttu-id="030f1-105">本主題說明可以建立的交易類型。</span><span class="sxs-lookup"><span data-stu-id="030f1-105">This topic describes the types of transactions that can be created.</span></span>

## <a name="review-the-time-and-material-billing-backlog"></a><span data-ttu-id="030f1-106">檢閱時間和資料帳務待辦項目</span><span class="sxs-lookup"><span data-stu-id="030f1-106">Review the time and material billing backlog</span></span>

<span data-ttu-id="030f1-107">專案的時間或費用項目已送出並獲核准時，PSA 會建立專案實際值。</span><span class="sxs-lookup"><span data-stu-id="030f1-107">When a time or expense entry is submitted and approved for a project, PSA creates a project actual.</span></span> <span data-ttu-id="030f1-108">如果專案和交易分類的組合已對應至時間和材料專案的合約服務內容，則該項目獲核准時，就會建立兩個實際值：</span><span class="sxs-lookup"><span data-stu-id="030f1-108">If the combination of the project and the transaction class are mapped to a contract line for a time-and-materials project, two actuals are created when the entry is approved:</span></span>

- <span data-ttu-id="030f1-109">成本實際值</span><span class="sxs-lookup"><span data-stu-id="030f1-109">Cost actual</span></span> 
- <span data-ttu-id="030f1-110">未開單銷售實際值</span><span class="sxs-lookup"><span data-stu-id="030f1-110">Unbilled sales actual</span></span>

<span data-ttu-id="030f1-111">未開單銷售實際值代表帳務待辦項目，且其帳單狀態必須設定為**已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="030f1-111">Unbilled sales actuals represent the billing backlog, and their billing status must be set to **Ready to Invoice**.</span></span> <span data-ttu-id="030f1-112">建立專案發票時，標示為**已準備好開立發票**的未開單銷售實際值會複製到發票明細詳細資料。</span><span class="sxs-lookup"><span data-stu-id="030f1-112">When a project invoice is created, unbilled sales actuals that are marked **Ready to Invoice** are copied over as invoice line details.</span></span>

<span data-ttu-id="030f1-113">若要檢閱時間和材料的帳務待辦項目，請移至**銷售** \> **帳務** \> **時間和資料帳務待辦項目**。</span><span class="sxs-lookup"><span data-stu-id="030f1-113">To review the billing backlog for time and materials, go to **Sales** \> **Billing** \> **Time and Material Billing Backlog**.</span></span> <span data-ttu-id="030f1-114">選取所有已準備好開立發票的未開單銷售實際值，然後選取**已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="030f1-114">Select all the unbilled sales actuals that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="030f1-115">這些實際值的帳單狀態會變更為**已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="030f1-115">The billing status of these actuals is changed to **Ready to Invoice**.</span></span>

![時間和資料帳務待辦項目](media/TMBacklog.png)

## <a name="review-the-product-billing-backlog"></a><span data-ttu-id="030f1-117">檢閱產品帳務待辦項目</span><span class="sxs-lookup"><span data-stu-id="030f1-117">Review the product billing backlog</span></span>

<span data-ttu-id="030f1-118">在 PSA 中，如果專案合約有產品型合約服務內容，每當為專案合約建立發票時，都會考慮這些服務內容來開立發票。</span><span class="sxs-lookup"><span data-stu-id="030f1-118">In PSA, when a project contract has product-based contract lines, those lines are considered for invoicing whenever an invoice is created for the project contract.</span></span> <span data-ttu-id="030f1-119">任何有合約服務內容標示為**已準備好開立發票**的產品都會複製到專案發票上做為專案發票明細。</span><span class="sxs-lookup"><span data-stu-id="030f1-119">Any product that has contract lines that are marked **Ready to Invoice** is copied over to the project invoice as project invoice lines.</span></span>

<span data-ttu-id="030f1-120">若要檢閱產品的帳務待辦項目，請移至**銷售**\>**帳務**\>**產品帳務待辦項目**。</span><span class="sxs-lookup"><span data-stu-id="030f1-120">To review the billing backlog for products, go to **Sales** \> **Billing** \> **Product Billing Backlog**.</span></span> <span data-ttu-id="030f1-121">選取所有已準備好開立發票的產品型合約服務內容，然後選取**已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="030f1-121">Select all the product-based contract lines that are ready to be invoiced, and then select **Ready to Invoice**.</span></span> <span data-ttu-id="030f1-122">這些服務內容的帳單狀態會變更為**已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="030f1-122">The billing status of these lines is changed to **Ready to Invoice**.</span></span>

![產品帳務待辦項目](media/ProductBacklog.png)

## <a name="review-billing-milestones-on-fixed-price-contracts"></a><span data-ttu-id="030f1-124">檢閱固定價格合約上的帳單里程碑</span><span class="sxs-lookup"><span data-stu-id="030f1-124">Review billing milestones on fixed-price contracts</span></span>

<span data-ttu-id="030f1-125">每個具有固定價格帳務方式的專案合約服務內容都必須定義合約里程碑。</span><span class="sxs-lookup"><span data-stu-id="030f1-125">Each project contract line that has a fixed-price billing method must define contract milestones.</span></span> <span data-ttu-id="030f1-126">只有合約里程碑已標示為**已準備好開立發票**時，才能為這些合約里程碑開立發票。</span><span class="sxs-lookup"><span data-stu-id="030f1-126">These contract milestones can be invoiced only if they are marked **Ready to Invoice**.</span></span> 

<span data-ttu-id="030f1-127">若要檢閱帳單里程碑，請移至**銷售** \> **帳務**\>**固定價格里程碑**。</span><span class="sxs-lookup"><span data-stu-id="030f1-127">To review billing milestones, go to **Sales** \> **Billing** \> **Fixed Price Milestones**.</span></span> <span data-ttu-id="030f1-128">選取已準備好開立發票的里程碑，然後選取**已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="030f1-128">Select the milestones that are ready to be invoiced, and then select **Ready to invoice**.</span></span> <span data-ttu-id="030f1-129">這些里程碑的帳單狀態會變更為**已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="030f1-129">The billing status of these milestones is changed to **Ready to Invoice**.</span></span>

![固定價格里程碑](media/FPBacklog.png)
