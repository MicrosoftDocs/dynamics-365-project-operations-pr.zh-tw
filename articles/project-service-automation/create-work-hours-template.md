---
title: 建立工作時數範本
description: 如何建立 Project Service 中的工作時數範本
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: 1a519487-25f1-4e9d-b739-1c1becf1d649
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: 5e7ef4af5f22419cccd8f29ea2a0a0a21a75875a
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749942"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="a01d9-103">建立工作時數範本 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="a01d9-103">Create a work hours template (Project Service)</span></span>

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

<span data-ttu-id="a01d9-104">在您能夠建立專案排程之前，需要先設定專案行事曆，以定義排程中每天要涵蓋的工作時數以及所有公休日。</span><span class="sxs-lookup"><span data-stu-id="a01d9-104">Before you can create project schedules, you need to set up a project calendar that defines the number of working hours to accommodate per day in the schedule and any business closures.</span></span> <span data-ttu-id="a01d9-105">使用工作時數範本即可進行此作業，範本中包含有關每天工作時數、休假及任何其他公休日的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="a01d9-105">You do this with a work hours template, which contains details about work hours per day, days off, and any other business closures.</span></span>  
  
 <span data-ttu-id="a01d9-106">當您建立專案時，將工作範本與專案行事曆建立關聯，即可為專案套用排程。</span><span class="sxs-lookup"><span data-stu-id="a01d9-106">When you’re creating a project, you associate a work template to the project calendar to apply the schedule for the project.</span></span>  
  
 <span data-ttu-id="a01d9-107">有兩種方式可建立工作時數範本：</span><span class="sxs-lookup"><span data-stu-id="a01d9-107">There are two ways you can create a work hours template:</span></span>  
  
-   <span data-ttu-id="a01d9-108">依據資源的行事曆建立工作時數範本。</span><span class="sxs-lookup"><span data-stu-id="a01d9-108">Create a work hours template based on a resource’s calendar.</span></span>  
  
-   <span data-ttu-id="a01d9-109">建立新的工作時數範本。</span><span class="sxs-lookup"><span data-stu-id="a01d9-109">Create a new work hours template.</span></span>  
  
#### <a name="to-create-a-work-hours-template-based-on-a-resources-calendar"></a><span data-ttu-id="a01d9-110">依據資源的行事曆建立工作時數範本</span><span class="sxs-lookup"><span data-stu-id="a01d9-110">To create a work hours template based on a resource’s calendar</span></span>  
  
1.  <span data-ttu-id="a01d9-111">移至 **Project Service > 資源**。</span><span class="sxs-lookup"><span data-stu-id="a01d9-111">Go to **Project Service > Resources**.</span></span>  
  
2.  <span data-ttu-id="a01d9-112">選取要做為工作時數的依據的資源。</span><span class="sxs-lookup"><span data-stu-id="a01d9-112">Select the resource you want to base your work hours on.</span></span>  
  
3.  <span data-ttu-id="a01d9-113">按一下**將行事曆儲存為**，輸入工作時數範本的名稱，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="a01d9-113">Click **Save Calendar As**, enter a name for the work hours template, and then click **Save**.</span></span>  
  
4.  <span data-ttu-id="a01d9-114">完成變更選項時，按一下**儲存後關閉**。</span><span class="sxs-lookup"><span data-stu-id="a01d9-114">When you’re done changing options, click **Save and Close**.</span></span>  
  
5.  <span data-ttu-id="a01d9-115">按一下畫面右下角的**儲存**按鈕。</span><span class="sxs-lookup"><span data-stu-id="a01d9-115">Click the **Save** button at the bottom right corner of the screen.</span></span>  
  
#### <a name="to-create-a-new-work-hours-template"></a><span data-ttu-id="a01d9-116">建立新的工作時數範本</span><span class="sxs-lookup"><span data-stu-id="a01d9-116">To create a new work hours template</span></span>  
  
1.  <span data-ttu-id="a01d9-117">移至 **Project Service > 工作時數範本**。</span><span class="sxs-lookup"><span data-stu-id="a01d9-117">Go to **Project Service > Work Hours Templates**.</span></span>  
  
2.  <span data-ttu-id="a01d9-118">按一下**新增**。</span><span class="sxs-lookup"><span data-stu-id="a01d9-118">Click **New**.</span></span>  
  
3.  <span data-ttu-id="a01d9-119">輸入工作時數範本的名稱。</span><span class="sxs-lookup"><span data-stu-id="a01d9-119">Enter a name for the work hours template.</span></span>  
  
4.  <span data-ttu-id="a01d9-120">選取要做為工作時數依據的資源，然後按一下**儲存**。</span><span class="sxs-lookup"><span data-stu-id="a01d9-120">Select a resource to base the work hours on, and then click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="a01d9-121">請參閱</span><span class="sxs-lookup"><span data-stu-id="a01d9-121">See Also</span></span>  
 [<span data-ttu-id="a01d9-122">設定資源</span><span class="sxs-lookup"><span data-stu-id="a01d9-122">Set up resources</span></span>](../project-service/set-up-resources.md)
