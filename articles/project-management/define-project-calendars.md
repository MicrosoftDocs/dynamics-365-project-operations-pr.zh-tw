---
title: 定義專案行事曆
description: 本主題提供有關使用專案行事曆追蹤專案排程的資訊。
author: ruhercul
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 774399f2c02d8434c9c042c3a9f995792893bfce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073170"
---
# <a name="define-project-calendars"></a><span data-ttu-id="5cad7-103">定義專案行事曆</span><span class="sxs-lookup"><span data-stu-id="5cad7-103">Define project calendars</span></span>

<span data-ttu-id="5cad7-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="5cad7-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5cad7-105">為了建立專案排程，您會建立專案行事曆範本，以定義每天的工作時數以及所有公休日。</span><span class="sxs-lookup"><span data-stu-id="5cad7-105">To create a project schedule, you create a project calendar template that defines the number of working hours per day and any business closures.</span></span> <span data-ttu-id="5cad7-106">若要建立專案行事曆範本，您可以將工作範本與專案的 **行事曆範本** 欄位建立關聯。</span><span class="sxs-lookup"><span data-stu-id="5cad7-106">To create a project calendar template, you associate a work template with the **Calendar template** field for the project.</span></span> <span data-ttu-id="5cad7-107">依照下列步驟建立建立工作範本。</span><span class="sxs-lookup"><span data-stu-id="5cad7-107">Follow these steps to create a work template.</span></span>

1. <span data-ttu-id="5cad7-108">在左導覽窗格中，選取 **資源** 。</span><span class="sxs-lookup"><span data-stu-id="5cad7-108">In the left navigation pane, select **Resources**.</span></span> 
2. <span data-ttu-id="5cad7-109">在 **資源** 清單頁面上，開啟使用者記錄，然後選取 **顯示工作時數** 。</span><span class="sxs-lookup"><span data-stu-id="5cad7-109">On the **Resources** list page, open a user record, and then select **Show Work Hours**.</span></span>

  > [!NOTE]
  > <span data-ttu-id="5cad7-110">請確定您已允許瀏覽器頁面出現快顯。</span><span class="sxs-lookup"><span data-stu-id="5cad7-110">Make sure that you allow pop-ups on the browser page.</span></span> <span data-ttu-id="5cad7-111">這可讓您看到資源設定的工作時數。</span><span class="sxs-lookup"><span data-stu-id="5cad7-111">This lets you see the work hours set for the resource.</span></span>
  
3. <span data-ttu-id="5cad7-112">在 **每月檢視表** 索引標籤中，選取 **設定** 。</span><span class="sxs-lookup"><span data-stu-id="5cad7-112">On the **Monthly View** tab, select **Set Up**.</span></span> <span data-ttu-id="5cad7-113">有三個選項的清單會出現：</span><span class="sxs-lookup"><span data-stu-id="5cad7-113">A list of three options appears:</span></span> 

  - <span data-ttu-id="5cad7-114">新增每週排程</span><span class="sxs-lookup"><span data-stu-id="5cad7-114">New Weekly Schedule</span></span>
  - <span data-ttu-id="5cad7-115">一日工作行事曆</span><span class="sxs-lookup"><span data-stu-id="5cad7-115">Work Schedule for One Day</span></span>
  - <span data-ttu-id="5cad7-116">休假</span><span class="sxs-lookup"><span data-stu-id="5cad7-116">Time Off</span></span>

4. <span data-ttu-id="5cad7-117">選取 **新增每週排程** ，然後設定此資源排程的選項。</span><span class="sxs-lookup"><span data-stu-id="5cad7-117">Select **New Weekly Schedule** , and then set the options for this resource schedule.</span></span> <span data-ttu-id="5cad7-118">您可以設定週期性每週排程、每天時數參數、公休日等等。</span><span class="sxs-lookup"><span data-stu-id="5cad7-118">You can set a recurring weekly schedule, daily hour parameters, business closures, and more.</span></span>
5. <span data-ttu-id="5cad7-119">設定日期範圍、選取 **儲存** ，然後選取 **關閉** 。</span><span class="sxs-lookup"><span data-stu-id="5cad7-119">Set the date range, select **Save** , and then select **Close**.</span></span> 
6. <span data-ttu-id="5cad7-120">返回 **資源** 清單頁面，並選取您設定其工作時數的資源。</span><span class="sxs-lookup"><span data-stu-id="5cad7-120">Go back to the **Resources** list page, and select the resource that you set the work hours for.</span></span> 
7. <span data-ttu-id="5cad7-121">選取 **設定行事曆為** 以設定工作範本。</span><span class="sxs-lookup"><span data-stu-id="5cad7-121">Select **Set Calendar As** to set the work template.</span></span> 
8. <span data-ttu-id="5cad7-122">在 **工作範本** 對話方塊中輸入工作範本的名稱，然後選取 **套用** 。</span><span class="sxs-lookup"><span data-stu-id="5cad7-122">In the **Work Template** dialog box, enter a name for the work template, and then select **Apply**.</span></span> 

<span data-ttu-id="5cad7-123">您現在可以將工作範本與專案行事曆範本建立關聯。</span><span class="sxs-lookup"><span data-stu-id="5cad7-123">You can now associate the work template with a project calendar template.</span></span>
