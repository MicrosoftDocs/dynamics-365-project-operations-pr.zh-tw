---
title: 設定其他參數設定
description: 如何設定 Project Service 中的其他參數設定
author: JohnPBurrows
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: de2fe830-4313-4711-b03b-76d56bf56cb6
ms.author: jburrows
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: f3e110163088f8e3b78da9f273113d74775bf24c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3750008"
---
# <a name="configure-additional-parameter-settings-project-service"></a><span data-ttu-id="4cd11-103">設定其他參數設定 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="4cd11-103">Configure additional parameter settings (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="4cd11-104">您在前幾個主題中設定項目之後，需要設定其他專案參數以用於專案。</span><span class="sxs-lookup"><span data-stu-id="4cd11-104">Once you’ve configured the items in previous topics, you need to set additional project parameters to use for your projects.</span></span> <span data-ttu-id="4cd11-105">首次安裝 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]時，您已建立參數設定，以便先建立 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] 運作所需的所有記錄。</span><span class="sxs-lookup"><span data-stu-id="4cd11-105">When you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you created a parameters setting to first create all the records required for [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)] to work.</span></span> <span data-ttu-id="4cd11-106">現在要回頭設定這些設定的額外欄位。</span><span class="sxs-lookup"><span data-stu-id="4cd11-106">Now it’s time to go back and configure additional fields for these settings.</span></span>  
  
 <span data-ttu-id="4cd11-107">您將需要進行下列設定：</span><span class="sxs-lookup"><span data-stu-id="4cd11-107">You’ll need to have configured the following settings:</span></span>  
  
-   <span data-ttu-id="4cd11-108">組織單位</span><span class="sxs-lookup"><span data-stu-id="4cd11-108">Organizational unit</span></span>  
  
-   <span data-ttu-id="4cd11-109">發票週期</span><span class="sxs-lookup"><span data-stu-id="4cd11-109">Invoice frequency</span></span>  
  
-   <span data-ttu-id="4cd11-110">工作時數範本</span><span class="sxs-lookup"><span data-stu-id="4cd11-110">Work hours template</span></span>  
  
-   <span data-ttu-id="4cd11-111">價目表</span><span class="sxs-lookup"><span data-stu-id="4cd11-111">Price list</span></span>  
 
<span data-ttu-id="4cd11-112">在此步驟中，您也會指出想要的資源配置類型：</span><span class="sxs-lookup"><span data-stu-id="4cd11-112">In this step, you’ll also indicate what type of resource allocation you want:</span></span>  
  
- <span data-ttu-id="4cd11-113">**集中**。</span><span class="sxs-lookup"><span data-stu-id="4cd11-113">**Central**.</span></span> <span data-ttu-id="4cd11-114">只有資源管理員可以配置資源至專案。</span><span class="sxs-lookup"><span data-stu-id="4cd11-114">Only resource managers can allocate resources to projects.</span></span>  
  
- <span data-ttu-id="4cd11-115">**混合式**。</span><span class="sxs-lookup"><span data-stu-id="4cd11-115">**Hybrid**.</span></span> <span data-ttu-id="4cd11-116">資源管理員、專案經理和客戶經理都可以配置資源至專案。</span><span class="sxs-lookup"><span data-stu-id="4cd11-116">Resource managers, project managers, and account managers can allocate resources to projects.</span></span>  
  
 
<span data-ttu-id="4cd11-117">若要設定專案參數：</span><span class="sxs-lookup"><span data-stu-id="4cd11-117">To set project parameters:</span></span>  
  
1. <span data-ttu-id="4cd11-118">移至 **Project Service > 參數**。</span><span class="sxs-lookup"><span data-stu-id="4cd11-118">Go to **Project Service > Parameters**.</span></span>  
  
2. <span data-ttu-id="4cd11-119">按一下您要設定的參數設定 (您首次安裝 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]時建立的設定)，或按一下**新增**建立新設定。</span><span class="sxs-lookup"><span data-stu-id="4cd11-119">Click the parameters setting you want to configure (the one you created when you first installed [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]), or click **New** to create a new one.</span></span>  
  
3. <span data-ttu-id="4cd11-120">在**一般**區域中，設定專案參數的所有選項。</span><span class="sxs-lookup"><span data-stu-id="4cd11-120">In the **General** area, set all the options for your project parameters.</span></span>  
  
4. <span data-ttu-id="4cd11-121">在**價目表**區域中，按一下 **+** 新增價目表，在**專案參數價目表**下拉式清單中選取一個價目表，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="4cd11-121">In the **Price List** area, click **+** to add a price list, select a price list in the **Project Parameter Price List** drop-down list, and then click **Save**.</span></span>  
  
5. <span data-ttu-id="4cd11-122">按一下畫面右下角的**儲存**按鈕。</span><span class="sxs-lookup"><span data-stu-id="4cd11-122">Click the **Save** button in the bottom right corner of the screen.</span></span>  

> [!NOTE]
> <span data-ttu-id="4cd11-123">必須保留 Project Service 的專案參數記錄，才能正常運作。</span><span class="sxs-lookup"><span data-stu-id="4cd11-123">The project parameter record must be maintained for Project Service to function correcly.</span></span> <span data-ttu-id="4cd11-124">不可刪除此記錄。</span><span class="sxs-lookup"><span data-stu-id="4cd11-124">This record should not be deleted.</span></span>

### <a name="see-also"></a><span data-ttu-id="4cd11-125">請參閱</span><span class="sxs-lookup"><span data-stu-id="4cd11-125">See Also</span></span>  
 [<span data-ttu-id="4cd11-126">設定資源</span><span class="sxs-lookup"><span data-stu-id="4cd11-126">Set up resources</span></span>](../project-service/set-up-resources.md)
