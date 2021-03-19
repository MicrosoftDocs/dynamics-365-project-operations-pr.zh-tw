---
title: 複製專案型報價
description: 本主題提供有關如何在 Project Operations 中複製專案型報價的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b1ce6c2b644319f2d822010a34c57c591f82edc9
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278138"
---
# <a name="copy-project-based-quotes"></a><span data-ttu-id="b989f-103">複製專案型報價</span><span class="sxs-lookup"><span data-stu-id="b989f-103">Copy project-based quotes</span></span>

<span data-ttu-id="b989f-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="b989f-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="b989f-105">您可以複製現有的專案報價，輕鬆地建立新的專案報價。</span><span class="sxs-lookup"><span data-stu-id="b989f-105">You can easily create a new Project quote by copying an existing one.</span></span> 

- <span data-ttu-id="b989f-106">若要複製專案報價，請在 **專案報價** 清單頁面或 **專案報價** 詳細資料頁面上，選取您要複製的專案報價，然後選取 **複製**。</span><span class="sxs-lookup"><span data-stu-id="b989f-106">To copy a Project quote, on the **Project Quotes** list page or the **Project Quote** details page, select the Project quote you want to copy, and then select **Copy**.</span></span>

<span data-ttu-id="b989f-107">這會開啟對話方塊頁面，您可以在其中輸入複製參數。</span><span class="sxs-lookup"><span data-stu-id="b989f-107">This will open a dialog page where you can enter the parameters of the copy.</span></span> <span data-ttu-id="b989f-108">下表列出對話方塊頁面中包含的欄位。</span><span class="sxs-lookup"><span data-stu-id="b989f-108">The following table lists the fields that are included in the dialog page.</span></span> <span data-ttu-id="b989f-109">視您選取的值而定，複製程序可能會變更。</span><span class="sxs-lookup"><span data-stu-id="b989f-109">Depending on the values you select, the copy process may change.</span></span>

| <span data-ttu-id="b989f-110">**欄位**</span><span class="sxs-lookup"><span data-stu-id="b989f-110">**Field**</span></span> | <span data-ttu-id="b989f-111">**描述**</span><span class="sxs-lookup"><span data-stu-id="b989f-111">**Description**</span></span> | <span data-ttu-id="b989f-112">**下游影響**</span><span class="sxs-lookup"><span data-stu-id="b989f-112">**Downstream impact**</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b989f-113">主題</span><span class="sxs-lookup"><span data-stu-id="b989f-113">Topic</span></span> | <span data-ttu-id="b989f-114">輸入目標報價的相關主題或名稱。</span><span class="sxs-lookup"><span data-stu-id="b989f-114">Enter the relevant topic, or name, of the target quote.</span></span> <span data-ttu-id="b989f-115">對話方塊開啟時，系統會將其設定為來源報價的主題，並在其後附加 **-複製**。</span><span class="sxs-lookup"><span data-stu-id="b989f-115">When the dialog opens, the system will set it to the topic of the source quote with **-copy** appended to it.</span></span> | |
| <span data-ttu-id="b989f-116">潛在客戶</span><span class="sxs-lookup"><span data-stu-id="b989f-116">Potential Customer</span></span> | <span data-ttu-id="b989f-117">參考客戶的公司或客戶記錄。</span><span class="sxs-lookup"><span data-stu-id="b989f-117">Reference to the customer's company or account record.</span></span> <span data-ttu-id="b989f-118">對話方塊開啟時，系統會將其設定為來源報價上的客戶。</span><span class="sxs-lookup"><span data-stu-id="b989f-118">When the dialog opens, the system will set it to the account on the source quote.</span></span> | <span data-ttu-id="b989f-119">此欄位是報價上的主要客戶。</span><span class="sxs-lookup"><span data-stu-id="b989f-119">This field is the primary customer on the quote.</span></span> |
| <span data-ttu-id="b989f-120">合約單位</span><span class="sxs-lookup"><span data-stu-id="b989f-120">Contracting Unit</span></span> | <span data-ttu-id="b989f-121">負責交付與此交易相關之專案的組織單位。</span><span class="sxs-lookup"><span data-stu-id="b989f-121">The organization unit that is responsible for the delivery of the project(s) associated with this deal.</span></span>
<span data-ttu-id="b989f-122">對話方塊開啟時，系統會將其設定為來源報價的合約單位。</span><span class="sxs-lookup"><span data-stu-id="b989f-122">When the dialog opens, the system will set it to the contracting unit of the source quote.</span></span> | <span data-ttu-id="b989f-123">合約單位是在完成交易後執行專案的公司部門。</span><span class="sxs-lookup"><span data-stu-id="b989f-123">Contracting unit is the division of the company that will execute the projects after the deal is closed.</span></span> <span data-ttu-id="b989f-124">每個合約單位都有貨幣。</span><span class="sxs-lookup"><span data-stu-id="b989f-124">Every contracting unit has a currency.</span></span> <span data-ttu-id="b989f-125">貨幣可用來報告執行專案期間所產生的估計和實際成本。</span><span class="sxs-lookup"><span data-stu-id="b989f-125">The currency is used to report estimated and actual costs incurred during the execution of the project.</span></span> |
| <span data-ttu-id="b989f-126">貨幣</span><span class="sxs-lookup"><span data-stu-id="b989f-126">Currency</span></span> | <span data-ttu-id="b989f-127">這是進行交易所用的貨幣。</span><span class="sxs-lookup"><span data-stu-id="b989f-127">This is the currency that the deal is transacted in.</span></span> <span data-ttu-id="b989f-128">對話方塊開啟時，系統會將其設定為來源報價的貨幣。</span><span class="sxs-lookup"><span data-stu-id="b989f-128">When the dialog opens, the system will set it to the currency of the source quote.</span></span> <span data-ttu-id="b989f-129">這可加以修改，如果有所變更，**複製定價** 欄位永遠設定為 **否**。</span><span class="sxs-lookup"><span data-stu-id="b989f-129">This can be modified and if it is change, the **Copy Pricing** field is always set to **No**.</span></span> <span data-ttu-id="b989f-130">這是因為來源報價的價目表不再有關聯。</span><span class="sxs-lookup"><span data-stu-id="b989f-130">This is because the price lists on source quote are no longer relevant.</span></span> | <span data-ttu-id="b989f-131">貨幣可用來預設價目表、建立對報價的財務估計值，以及最終在交易成交時開發票給客戶。</span><span class="sxs-lookup"><span data-stu-id="b989f-131">Currency is used to default a price list, to build a financial estimate on the quote,  and eventually to invoice the customer when the deal is won.</span></span> |
| <span data-ttu-id="b989f-132">要求的交貨日期</span><span class="sxs-lookup"><span data-stu-id="b989f-132">Requested Delivery Date</span></span> | <span data-ttu-id="b989f-133">這是客戶要求的交付日期。</span><span class="sxs-lookup"><span data-stu-id="b989f-133">This is the date of delivery requested by the customer.</span></span> | <span data-ttu-id="b989f-134">這會當做依特定頻率建立發票開立日期時的結束日期。</span><span class="sxs-lookup"><span data-stu-id="b989f-134">This is used as the end date when creating invoicing dates along a specific frequency.</span></span> |
| <span data-ttu-id="b989f-135">複製定價</span><span class="sxs-lookup"><span data-stu-id="b989f-135">Copy pricing</span></span> | <span data-ttu-id="b989f-136">[是/否] 值指示報價上的定價是否應從來源報價複製。</span><span class="sxs-lookup"><span data-stu-id="b989f-136">A Yes/No value indicates whether the pricing on the quote should be copied from the source quote.</span></span> | <span data-ttu-id="b989f-137">如果選取 **是**，則會將專案價目表和產品價目表參考從來源報價複製到目標報價。</span><span class="sxs-lookup"><span data-stu-id="b989f-137">If **Yes** is selected, the project price list and product price list references are copied from the source quote to the target quote.</span></span> <span data-ttu-id="b989f-138">如果選取 **否**，則根據帳戶或專案參數所設定的最新價目表，重新預設價目表。</span><span class="sxs-lookup"><span data-stu-id="b989f-138">If **No** is selected, price lists are re-defaulted based on the latest price lists that were set up on the account or project parameters.</span></span> |

<span data-ttu-id="b989f-139">選取對話方塊頁面上的 **確定** 時 ，系統會根據對話方塊中選取的參數，建立專案報價的複本。</span><span class="sxs-lookup"><span data-stu-id="b989f-139">When you select **OK** on the dialog page, the system creates a copy of the project quote based on the parameters selected in the dialog.</span></span> <span data-ttu-id="b989f-140">新的專案報價會開啟。</span><span class="sxs-lookup"><span data-stu-id="b989f-140">The new project quote opens.</span></span> 

> [!NOTE]
> <span data-ttu-id="b989f-141">下列資訊不會從來源報價複製到目標報價：</span><span class="sxs-lookup"><span data-stu-id="b989f-141">The following information is not copied from the Source to the Target quote:</span></span>
>
> - <span data-ttu-id="b989f-142">發票排程</span><span class="sxs-lookup"><span data-stu-id="b989f-142">Invoice schedules</span></span>
> - <span data-ttu-id="b989f-143">報價和報價明細客戶</span><span class="sxs-lookup"><span data-stu-id="b989f-143">Quote and quote line customers</span></span>
> - <span data-ttu-id="b989f-144">專案型報價明細上的專案參考 - 客戶預算資訊</span><span class="sxs-lookup"><span data-stu-id="b989f-144">Project reference on the project – based quote lines -Customer budget information</span></span>
>
><span data-ttu-id="b989f-145">由於此資訊極其明確專屬於每個報價，因此不會複製這些欄位和記錄。</span><span class="sxs-lookup"><span data-stu-id="b989f-145">Because this information is very specific to each quote, these fields and records are not copied.</span></span> <span data-ttu-id="b989f-146">將會複製專案與產品的報價明細、報價明細詳細資料的估計值，以及報價層級上不得超過的值。</span><span class="sxs-lookup"><span data-stu-id="b989f-146">Quote lines for projects and products, estimates on quote line details, and not-to-exceed values at the quote level are copied.</span></span> <span data-ttu-id="b989f-147">價格及成本費率預設值取決於 **複製參數** 對話方塊頁面上所選取的 **複製定價** 選項。</span><span class="sxs-lookup"><span data-stu-id="b989f-147">Price and cost rate defaults depend on the **Copy pricing** option selected on the **Copy parameters** dialog page.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]