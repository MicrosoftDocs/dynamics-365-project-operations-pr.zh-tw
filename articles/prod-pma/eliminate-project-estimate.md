---
title: 銷除專案估計值
description: 本主題提供有關完成專案估計後銷除其估計值的資訊。
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
ms.openlocfilehash: 8bda8a7357e883b948449b2a19bea476996dde3c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073049"
---
# <a name="eliminate-a-project-estimate"></a><span data-ttu-id="cd20e-103">銷除專案估計值</span><span class="sxs-lookup"><span data-stu-id="cd20e-103">Eliminate a project estimate</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd20e-104">專案預估值為專案中預估與排定的作業提供財務檢視表。</span><span class="sxs-lookup"><span data-stu-id="cd20e-104">Project estimates provide the financial view for work that is estimated and scheduled for a project.</span></span> <span data-ttu-id="cd20e-105">若要使用專案的估計值，您必須將專案附加至估計專案。</span><span class="sxs-lookup"><span data-stu-id="cd20e-105">To work with estimates for a project, you must attach the project to an estimate project.</span></span> <span data-ttu-id="cd20e-106">估計專案永遠都是根據現有的專案來建立，但是多個專案可以參考單一估計專案。</span><span class="sxs-lookup"><span data-stu-id="cd20e-106">An estimate project is always based on an existing project, however multiple projects can refer to a single estimate project.</span></span> <span data-ttu-id="cd20e-107">只有固定價格和投資專案可以附加至估計專案，而且這些專案與估計專案同屬於一個專案群組。</span><span class="sxs-lookup"><span data-stu-id="cd20e-107">Only fixed-price and investment projects can be attached to estimate projects, and those projects must belong to the same project group as the estimate project.</span></span>

<span data-ttu-id="cd20e-108">若要銷除估計專案，此專案必須已完成。</span><span class="sxs-lookup"><span data-stu-id="cd20e-108">To eliminate an estimate project, it must be complete.</span></span> <span data-ttu-id="cd20e-109">下列步驟說明如何銷除估計值。</span><span class="sxs-lookup"><span data-stu-id="cd20e-109">The following steps explain how to eliminate an estimate.</span></span>

1. <span data-ttu-id="cd20e-110">移至 **專案管理與會計** > **所有專案** ，然後開啟專案。</span><span class="sxs-lookup"><span data-stu-id="cd20e-110">Go to **Project management and accounting** > **All Projects** and open the project.</span></span> 
2. <span data-ttu-id="cd20e-111">在 **管理** 索引標籤上，選取 **估計值** ，然後在 **估計值** 頁面選取 **銷除** 。</span><span class="sxs-lookup"><span data-stu-id="cd20e-111">On the **Manage** tab, select **Estimates** , and on the **Estimate** page select **Eliminate**.</span></span>
3. <span data-ttu-id="cd20e-112">在 **銷除估計值** 頁面的 **一般** 索引標籤上，設定下列選項：</span><span class="sxs-lookup"><span data-stu-id="cd20e-112">On the **Eliminate estimate** page on the **General** tab, set the following options:</span></span>

   - <span data-ttu-id="cd20e-113">**期間代碼** ：選取期間代碼以選擇適當的估計專案。</span><span class="sxs-lookup"><span data-stu-id="cd20e-113">**Period code** : Select the period code to choose the appropriate estimate projects.</span></span> 
   - <span data-ttu-id="cd20e-114">**估計日期** ：選取適當的估計日期以進行銷除。</span><span class="sxs-lookup"><span data-stu-id="cd20e-114">**Estimate date** : Select the appropriate estimate date for elimination.</span></span>
   - <span data-ttu-id="cd20e-115">**銷除但顯示 WIP 警告** ：啟用此選項可在銷除與進行中工作 (WIP) 相關的估計值時，提供通知。</span><span class="sxs-lookup"><span data-stu-id="cd20e-115">**Eliminate with WIP warnings** : Enable this option to provide notification when an estimate that is associated with a work in progress (WIP) will be eliminated.</span></span> <span data-ttu-id="cd20e-116">未啟用此選項時，如果有任何非估計交易，則無法繼續進行銷除。</span><span class="sxs-lookup"><span data-stu-id="cd20e-116">When this option is not enabled, elimination can’t continue if any non-estimated transactions exist.</span></span> 
   > [!NOTE]
   > <span data-ttu-id="cd20e-117">只有在銷除是套用至估計專案時，才能使用此選項。</span><span class="sxs-lookup"><span data-stu-id="cd20e-117">This option is available only when elimination is applied to an estimate project.</span></span> <span data-ttu-id="cd20e-118">如果您使用定期過帳，則無法使用此選項。</span><span class="sxs-lookup"><span data-stu-id="cd20e-118">It is not available if you are using periodic postings.</span></span> <span data-ttu-id="cd20e-119">此設定可在 **非估計交易存在時允許銷除** 欄位群組中，與 **專案參數** 頁面的 **估計值** 索引標籤上的設定搭配使用。</span><span class="sxs-lookup"><span data-stu-id="cd20e-119">This setting works with the settings on the **Estimate** tab on the **Project parameters** page, in the **Allow elimination when non-estimated transactions exist** field group.</span></span>
   - <span data-ttu-id="cd20e-120">**將階段設定為已完成** ：啟用此選項可在執行銷除後，將估計專案的階段設定為 **已完成** 。</span><span class="sxs-lookup"><span data-stu-id="cd20e-120">**Set stage to Finished** : Enable this option to set the estimate project’s stage to **Finished** after you run the elimination.</span></span>
   - <span data-ttu-id="cd20e-121">**列印估計值清單** ：選取列印估計值清單時要包含的資訊。</span><span class="sxs-lookup"><span data-stu-id="cd20e-121">**Print estimate list** : Select the information to be included when the estimate list is printed.</span></span>
   - <span data-ttu-id="cd20e-122">**顯示資訊日誌** ：啟用此選項以顯示資訊日誌。</span><span class="sxs-lookup"><span data-stu-id="cd20e-122">**Show Infolog** : Enable this option to display the Infolog.</span></span>
   - <span data-ttu-id="cd20e-123">**過帳日期** ：選擇估計值的總帳過帳日期。</span><span class="sxs-lookup"><span data-stu-id="cd20e-123">**Posting date** : Choose the ledger posting date of the estimate.</span></span>

4.  <span data-ttu-id="cd20e-124">選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="cd20e-124">Select **OK**.</span></span>
5. <span data-ttu-id="cd20e-125">銷除程序完成之後，會以負值顯示已銷除的估計專案。</span><span class="sxs-lookup"><span data-stu-id="cd20e-125">After the elimination process is complete, the eliminated estimate project is displayed with a negative value.</span></span> 

<span data-ttu-id="cd20e-126">如果您無意銷除估計值，則可以選取已銷除的估計值，並選取 **反轉銷除** 。</span><span class="sxs-lookup"><span data-stu-id="cd20e-126">If you did not intend to eliminate an estimate, you can select the eliminated estimate and select **Reverse elimination**.</span></span>   
