---
title: 建立自訂定價維度解決方案
description: 本主題說明如何在建立自訂定價維度時建立自訂解決方案。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144628"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a><span data-ttu-id="0b100-103">建立自訂定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="0b100-103">Create custom solutions for pricing dimensions</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> <span data-ttu-id="0b100-104">所有自訂定價維度變更都必須是在另一個的解決方案中。</span><span class="sxs-lookup"><span data-stu-id="0b100-104">All custom pricing dimension changes should be in a separate solution.</span></span> <span data-ttu-id="0b100-105">這個重要的最佳做法提供您日後視需要更新或移除變更的彈性、有助於重複使用您的工作，以及讓您更便於將這些變更移植到另一個執行個體。</span><span class="sxs-lookup"><span data-stu-id="0b100-105">This important best practice provides flexibility in the future to update or remove changes as needed, will help with re-use of your work, and makes it easier to port these changes to another instance.</span></span> <span data-ttu-id="0b100-106">進行必要變更之後，將此解決方案匯出為 **受管理的解決方案**，再將其匯入至其他執行個體，即可重複使用您的定價設定。</span><span class="sxs-lookup"><span data-stu-id="0b100-106">After you make the required changes, export this solution as a **Managed solution**, and import it into other instances to reuse your pricing setup.</span></span>

1. <span data-ttu-id="0b100-107">選取 **設定** > **解決方案**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="0b100-107">Select **Settings** > **Solutions**, and then select **New**.</span></span> 
2. <span data-ttu-id="0b100-108">將解決方案命名為 **\<your organization name> 定價維度**、輸入其餘必要資訊，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="0b100-108">Name the solution, **\<your organization name> pricing dimensions**, enter the remaining required information, and then select **Save**.</span></span>

> ![建立自訂定價維度解決方案](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a><span data-ttu-id="0b100-110">將所有必要的實體及相關元件新增至定價維度解決方案</span><span class="sxs-lookup"><span data-stu-id="0b100-110">Add all required entities and related components to the Pricing dimension solution</span></span>
<span data-ttu-id="0b100-111">您必須將下列 Project Service 實體新增至您的定價方案。</span><span class="sxs-lookup"><span data-stu-id="0b100-111">You will need to add the following Project Service entities to your pricing solution.</span></span> <span data-ttu-id="0b100-112">完成此程序中的步驟，在定價方案中進行一些重要的結構描述變更，讓實體得知新的定價維度。</span><span class="sxs-lookup"><span data-stu-id="0b100-112">Complete the steps in this procedure to make some important schema changes in the pricing solution so that the entities become aware of the new pricing dimensions.</span></span>

1. <span data-ttu-id="0b100-113">選取 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。</span><span class="sxs-lookup"><span data-stu-id="0b100-113">Select **Settings** > **Solutions**, and then double-click **\<your organization name> pricing dimensions**.</span></span> 
2. <span data-ttu-id="0b100-114">在方案總管的左導覽窗格中，選取 **新增現有的** >  **實體**。</span><span class="sxs-lookup"><span data-stu-id="0b100-114">In Solution Explorer, on the left navigation pane, select **Add Existing** > **Entities**.</span></span>
3. <span data-ttu-id="0b100-115">在 **解決方案元件** 對話方塊中，選取下列實體：</span><span class="sxs-lookup"><span data-stu-id="0b100-115">In the **Solution Components** dialog box, select the following entities:</span></span>

- <span data-ttu-id="0b100-116">實際</span><span class="sxs-lookup"><span data-stu-id="0b100-116">Actual</span></span>
- <span data-ttu-id="0b100-117">可預約資源</span><span class="sxs-lookup"><span data-stu-id="0b100-117">Bookable Resource</span></span>
- <span data-ttu-id="0b100-118">估計明細</span><span class="sxs-lookup"><span data-stu-id="0b100-118">Estimate Line</span></span>
- <span data-ttu-id="0b100-119">專案工作</span><span class="sxs-lookup"><span data-stu-id="0b100-119">Project Task</span></span>
- <span data-ttu-id="0b100-120">發票明細詳細資料</span><span class="sxs-lookup"><span data-stu-id="0b100-120">Invoice Line Detail</span></span>
- <span data-ttu-id="0b100-121">帳目明細</span><span class="sxs-lookup"><span data-stu-id="0b100-121">Journal Line</span></span>
- <span data-ttu-id="0b100-122">專案合約服務內容詳細資料</span><span class="sxs-lookup"><span data-stu-id="0b100-122">Project Contract Line Detail</span></span>
- <span data-ttu-id="0b100-123">專案團隊成員</span><span class="sxs-lookup"><span data-stu-id="0b100-123">Project Team Member</span></span>
- <span data-ttu-id="0b100-124">報價明細詳細資料</span><span class="sxs-lookup"><span data-stu-id="0b100-124">Quote Line Detail</span></span>
- <span data-ttu-id="0b100-125">角色價格加成</span><span class="sxs-lookup"><span data-stu-id="0b100-125">Role Price Markup</span></span>
- <span data-ttu-id="0b100-126">角色價格</span><span class="sxs-lookup"><span data-stu-id="0b100-126">Role Price</span></span> 
- <span data-ttu-id="0b100-127">時間項目</span><span class="sxs-lookup"><span data-stu-id="0b100-127">Time Entry</span></span> 

> ![將現有實體新增至定價維度解決方案](media/Existing-entities-to-PD-solution.png)

> ![選取解決方案元件](media/Dimension-Components.png)

> [!NOTE]
> <span data-ttu-id="0b100-130">請務必包含所選每個實體的所有表單和檢視表。</span><span class="sxs-lookup"><span data-stu-id="0b100-130">Make sure to include all forms and views for each of the entities selected.</span></span>

4. <span data-ttu-id="0b100-131">系統提示您包含所選實體的任何相依實體時，選取 **否**。</span><span class="sxs-lookup"><span data-stu-id="0b100-131">When prompted to include any dependent entities for the selected entities, select **No**.</span></span>

> ![不要包括所有相關元件。](media/Do-not-include-required.png)


