---
title: 費用估計值
description: 本主題提供有關定義或估計專案型費用的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 2afe4ff2f84fc5426c409e6314da73b11a4de281
ms.sourcegitcommit: 56c42d7f5995a674426a1c2a81bae897dceb391c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/01/2020
ms.locfileid: "3907944"
---
# <a name="expense-estimates"></a><span data-ttu-id="d70b8-103">費用估計值</span><span class="sxs-lookup"><span data-stu-id="d70b8-103">Expense estimates</span></span>
<span data-ttu-id="d70b8-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="d70b8-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d70b8-105">除了定義資源型評估值之外，Dynamics 365 Project Operations 還可讓專案經理每個專案的專案型費用。</span><span class="sxs-lookup"><span data-stu-id="d70b8-105">Along with defining resource-based estimates, Dynamics 365 Project Operations allows Project managers to define project-based expenses for each project.</span></span> <span data-ttu-id="d70b8-106">每個費用項目都可與特定專案工作或費用類別建立關聯。</span><span class="sxs-lookup"><span data-stu-id="d70b8-106">Each expense item can be associated with a specific project task or expense category.</span></span> <span data-ttu-id="d70b8-107">費用類別通常是在組織層級定義。</span><span class="sxs-lookup"><span data-stu-id="d70b8-107">Expense categories are typically defined at the organizational level.</span></span> <span data-ttu-id="d70b8-108">每個費用類別的定價通常是在下列階層中定義：</span><span class="sxs-lookup"><span data-stu-id="d70b8-108">Pricing for each expense category is typically defined in the following hierarchy:</span></span>

- <span data-ttu-id="d70b8-109">組織</span><span class="sxs-lookup"><span data-stu-id="d70b8-109">Organization</span></span>
- <span data-ttu-id="d70b8-110">客戶</span><span class="sxs-lookup"><span data-stu-id="d70b8-110">Customer</span></span>
- <span data-ttu-id="d70b8-111">報價/合約</span><span class="sxs-lookup"><span data-stu-id="d70b8-111">Quote/contract</span></span>

<span data-ttu-id="d70b8-112">完成下列步驟，以檢視、新增或刪除專案費用。</span><span class="sxs-lookup"><span data-stu-id="d70b8-112">Complete the following steps to view, add, or delete a project expense.</span></span>

1. <span data-ttu-id="d70b8-113">移至**專案**，然後選取您要處理的專案。</span><span class="sxs-lookup"><span data-stu-id="d70b8-113">Go to **Projects**, and select the project you want to work on.</span></span>
2. <span data-ttu-id="d70b8-114">選取**專案估計值**索引標籤，然後檢視專案費用清單。</span><span class="sxs-lookup"><span data-stu-id="d70b8-114">Select the **Project Estimates** tab and view the list of project expenses.</span></span>
3. <span data-ttu-id="d70b8-115">選取**新增費用**以新增費用。</span><span class="sxs-lookup"><span data-stu-id="d70b8-115">Select **New Expense** to add an expense.</span></span> <span data-ttu-id="d70b8-116">或者，選取要刪除的費用，然後選取**刪除費用**。</span><span class="sxs-lookup"><span data-stu-id="d70b8-116">Or, select an expense to delete, and then select **Delete Expense**.</span></span>

<span data-ttu-id="d70b8-117">下列屬性是針對每個費用明細項目所定義：</span><span class="sxs-lookup"><span data-stu-id="d70b8-117">The following attributes are defined for each expense line item:</span></span>

- <span data-ttu-id="d70b8-118">**類別**：用於描述專案中所產生所有費用的常見群組方式。</span><span class="sxs-lookup"><span data-stu-id="d70b8-118">**Category**: The common groupings used to describe all expenses incurred on a project.</span></span>
- <span data-ttu-id="d70b8-119">**開始日期**：預測產生費用的日期。</span><span class="sxs-lookup"><span data-stu-id="d70b8-119">**Start Date**: The date when the expense is forecasted to be incurred.</span></span>
- <span data-ttu-id="d70b8-120">**數量**：特定類別的費用項目估計數目。</span><span class="sxs-lookup"><span data-stu-id="d70b8-120">**Quantity**: The estimated number of expense items for a specific category.</span></span>
- <span data-ttu-id="d70b8-121">**單位成本價**：用於計算費用成本的單價。</span><span class="sxs-lookup"><span data-stu-id="d70b8-121">**Unit Cost Price**: The unit price used to calculate to cost of the expense.</span></span>
- <span data-ttu-id="d70b8-122">**單位售價**：用於計算費用售價的單價。</span><span class="sxs-lookup"><span data-stu-id="d70b8-122">**Unit Sales Price**: The unit price used to calculate the sale prices of the expense.</span></span>

