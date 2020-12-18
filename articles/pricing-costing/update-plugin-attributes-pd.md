---
title: 使用新的定價維度來更新外掛程式屬性
description: 此主題提供有關如何更新定價維度的外掛程式屬性的資訊。
author: rumant
manager: Annbe
ms.date: 11/18/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 9b0cf48318d0b9e94c4be0d3775b54e83832c1b7
ms.sourcegitcommit: 573be7e36604ace82b35e439cfa748aa7c587415
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/25/2020
ms.locfileid: "4643208"
---
# <a name="update-plug-in-attributes-with-new-pricing-dimensions"></a><span data-ttu-id="01e65-103">使用新的定價維度來更新外掛程式屬性</span><span class="sxs-lookup"><span data-stu-id="01e65-103">Update plug-in attributes with new pricing dimensions</span></span>

<span data-ttu-id="01e65-104">此主題提供有關如何更新定價維度的外掛程式屬性的資訊。</span><span class="sxs-lookup"><span data-stu-id="01e65-104">This topic provides information about how to update plug-in attributes for pricing dimensions.</span></span>

> [!NOTE]
> <span data-ttu-id="01e65-105">此主題只適用於 Dynamics 365 Project Operations 中的報價及合約功能。</span><span class="sxs-lookup"><span data-stu-id="01e65-105">This topic is only applicable to the quote and contract features in Dynamics 365 Project Operations.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="01e65-106">先決條件</span><span class="sxs-lookup"><span data-stu-id="01e65-106">Prerequisites</span></span>
<span data-ttu-id="01e65-107">在您完成此主題中的步驟之前，您必須已完成下列主題中的程序：</span><span class="sxs-lookup"><span data-stu-id="01e65-107">Before you complete the steps in this topic, you must have completed the procedures in the following topics:</span></span>

  - [<span data-ttu-id="01e65-108">建立自訂欄位和實體</span><span class="sxs-lookup"><span data-stu-id="01e65-108">Create custom fields and entities</span></span>](create-custom-fields-entities-pricing-dimensions.md) 
  - [<span data-ttu-id="01e65-109">將自訂欄位新增至價格設定與交易實體</span><span class="sxs-lookup"><span data-stu-id="01e65-109">Add custom fields to price setup and transactional entities</span></span>](add-custom-fields-price-setup-transactional-entities.md)
  - <span data-ttu-id="01e65-110">[將自訂欄位設定為定價維度](set-up-custom-fields-pricing-dimensions.md)。</span><span class="sxs-lookup"><span data-stu-id="01e65-110">[Set up custom fields as pricing dimensions](set-up-custom-fields-pricing-dimensions.md).</span></span> 
  
<span data-ttu-id="01e65-111">如果您尚未完成這些程序，請先完成然後再回到本主題。</span><span class="sxs-lookup"><span data-stu-id="01e65-111">If you haven't completed those procedures, complete them and then return to this topic.</span></span>

## <a name="register-a-plug-in"></a><span data-ttu-id="01e65-112">註冊外掛程式</span><span class="sxs-lookup"><span data-stu-id="01e65-112">Register a plug-in</span></span>
<span data-ttu-id="01e65-113">當報價明細詳細資料建立於專案報價明細的 **報價明細** 頁面時，系統會建立兩個估計明細。</span><span class="sxs-lookup"><span data-stu-id="01e65-113">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines.</span></span> <span data-ttu-id="01e65-114">其中一個明細用於成本面估計，另一個用於銷售面估計。</span><span class="sxs-lookup"><span data-stu-id="01e65-114">One line is for the cost side of the estimate and the other line is for sales the side.</span></span> <span data-ttu-id="01e65-115">這同樣適用於專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="01e65-115">This is the same  for project contract lines.</span></span>

<span data-ttu-id="01e65-116">對成本面欄位數量或欄位進行變更時，銷售面也會進行該變更。</span><span class="sxs-lookup"><span data-stu-id="01e65-116">When you make a change to the quantity or a field on the cost side, that change is also made on the sales side.</span></span> <span data-ttu-id="01e65-117">這是可能的，因為 Quotelinedetail 和 contractline 詳細資料實體的 PreOperation 外掛程式會將成本面的特定屬性連接至交易的銷售面。</span><span class="sxs-lookup"><span data-stu-id="01e65-117">This is possible because the PreOperation plug-ins on Quotelinedetail and contractline detail entities connect specific attributes on the cost side to the sales side of the transaction.</span></span> <span data-ttu-id="01e65-118">如果您需要對銷售面的定價維度值所做的變更也要在成本面進行，在變更定價維度後，必須重新註冊下列外掛程式。</span><span class="sxs-lookup"><span data-stu-id="01e65-118">If you need changes made to the pricing dimension values on the sales side to also be made on the cost side, the following plug-ins must be re-registered after making changes to a pricing dimension.</span></span>

<span data-ttu-id="01e65-119">以下是要更新並重新註冊的外掛程式：</span><span class="sxs-lookup"><span data-stu-id="01e65-119">These are the plug-ins to update and re-register:</span></span>

- <span data-ttu-id="01e65-120">PreOperationContractLineDetailUpdate - **更新 msdyn_orderlinetransaction**</span><span class="sxs-lookup"><span data-stu-id="01e65-120">PreOperationContractLineDetailUpdate - **Update msdyn_orderlinetransaction**</span></span>
- <span data-ttu-id="01e65-121">PreOperationQuoteLineDetailUpdate - **更新 msdyn_quotelinetransaction**</span><span class="sxs-lookup"><span data-stu-id="01e65-121">PreOperationQuoteLineDetailUpdate - **Updates msdyn_quotelinetransaction**</span></span>

<span data-ttu-id="01e65-122">請完成下列步驟，更新並重新註冊外掛程式。</span><span class="sxs-lookup"><span data-stu-id="01e65-122">Complete the following steps to update and re-register the plug-ins.</span></span>

1. <span data-ttu-id="01e65-123">開啟 **PluginRegistrationTool**，並連接至您的 Project Operations Dataverse 環境。</span><span class="sxs-lookup"><span data-stu-id="01e65-123">Open **PluginRegistrationTool** and connect to your Project Operations Dataverse environment.</span></span>
2. <span data-ttu-id="01e65-124">選取 **搜尋**，然後輸入要更新之外掛程式的前幾個字母。</span><span class="sxs-lookup"><span data-stu-id="01e65-124">Select **Search**, and type in the first few letters of the plug-in to be updated.</span></span>
3. <span data-ttu-id="01e65-125">找到外掛程式後，選取該外掛程式，然後選取 **在主要表單上選取**。</span><span class="sxs-lookup"><span data-stu-id="01e65-125">After the plug-in is found, select it, and then select **Select on Main Form**.</span></span>
4. <span data-ttu-id="01e65-126">選取 **更新 msdyn_orderlinetransaction** 步驟、按一下滑鼠右鍵，然後選取 **更新**。</span><span class="sxs-lookup"><span data-stu-id="01e65-126">Select the **Update msdyn_orderlinetransaction** step, right-click, and then select **Update**.</span></span>
5. <span data-ttu-id="01e65-127">在 **更新** 對話方塊頁面中，選取篩選屬性中的省略符號 (**...**)。</span><span class="sxs-lookup"><span data-stu-id="01e65-127">In the **Update** dialog page, select the ellipsis (**...**) in the filtering attributes.</span></span>
6. <span data-ttu-id="01e65-128">篩選屬性視窗隨即開啟，並提供實體和定價維度中的所有屬性清單。</span><span class="sxs-lookup"><span data-stu-id="01e65-128">The filtering attributes window opens and provides a list of all attributes in the entity and the pricing dimensions.</span></span> <span data-ttu-id="01e65-129">選取定價維度屬性的核取方塊。</span><span class="sxs-lookup"><span data-stu-id="01e65-129">Select the check boxes for the pricing dimension attributes.</span></span>
7. <span data-ttu-id="01e65-130">選取 **確定** 關閉頁面，然後選取 **更新步驟**。</span><span class="sxs-lookup"><span data-stu-id="01e65-130">Select **OK** to close the page, and then select **Update Step**.</span></span>
8. <span data-ttu-id="01e65-131">對第二個外掛程式 **PreOperationQuoteLineDetail** 重複步驟 2 到 7。</span><span class="sxs-lookup"><span data-stu-id="01e65-131">Repeat steps 2-7 for the second plug-in, **PreOperationQuoteLineDetail**.</span></span> <span data-ttu-id="01e65-132">對第二個外掛程式，您需更新 **msdyn_quotelinetransaction 的更新** 步驟。</span><span class="sxs-lookup"><span data-stu-id="01e65-132">For this plug-in, you need to update the **Update of msdyn_quotelinetransaction** step.</span></span>
9. <span data-ttu-id="01e65-133">關閉 **PluginRegistrationTool**。</span><span class="sxs-lookup"><span data-stu-id="01e65-133">Close **PluginRegistrationTool**.</span></span>
