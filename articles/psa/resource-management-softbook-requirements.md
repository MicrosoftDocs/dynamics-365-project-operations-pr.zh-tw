---
title: 未確認預約需求
description: 本主題提供有關如何以未確認預約方式預約需求的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/28/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 736d59976ad0f456a694cedbb28b516c90632fe6
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282908"
---
# <a name="soft-book-requirements"></a><span data-ttu-id="7cc3e-103">未確認預約需求</span><span class="sxs-lookup"><span data-stu-id="7cc3e-103">Soft-book requirements</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

<span data-ttu-id="7cc3e-104">資源需求可以進行已確認預約。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-104">A resource requirement can be hard-booked.</span></span> <span data-ttu-id="7cc3e-105">已確認預約會建立耗用資源產能的提案。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-105">A hard booking creates a proposal that consumes a resource's capacity.</span></span> <span data-ttu-id="7cc3e-106">提案接著會傳送回到要求者以取得核准。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-106">The proposal is then sent back to the requester for approval.</span></span> <span data-ttu-id="7cc3e-107">未確認預約會暫時將資源新增至專案團隊，並且在排程面板上的狀態有所不同，但不會耗用資源的產能。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-107">A soft booking tentatively adds a resource to a project team and has a different status on the Schedule Board, but it doesn't consume the resource's capacity.</span></span> <span data-ttu-id="7cc3e-108">若要以未確認預約方式從排程面板預約資源，請將 **預約狀態** 欄位設定為 **未確認**。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-108">To soft-book a resource from the Schedule Board, set the **Booking Status** field to **Soft**.</span></span>

![預約狀態設定為 [未確認]](media/Resource-Management-image77.png)

<span data-ttu-id="7cc3e-110">當 **團隊** 索引標籤進入 **具名團隊成員** 檢視表時，資源就會顯示在其中。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-110">When the **Team** tab is in the **Named Team Members** view, the resource appears there.</span></span> <span data-ttu-id="7cc3e-111">**未確認預約時數** 欄會報告未確認預約時數。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-111">The soft-booked hours are reported in the **Soft Booked Hours** column.</span></span>

![[具名團隊成員] 檢視表中的未確認預約時數](media/Resource-Management-image78.png)

<span data-ttu-id="7cc3e-113">無法將未確認預約的團隊成員指派給工作。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-113">Soft-booked team members can be assigned to tasks.</span></span>

![指派給工作的未確認預約團隊成員](media/Resource-Management-image79.png)

<span data-ttu-id="7cc3e-115">在 **協調** 索引標籤上，不會顯示未確認預約資源的任何預約，因為 **協調** 索引標籤只會考慮已確認預約。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-115">On the **Reconciliation** tab, no bookings are shown for a soft-book resource, because the **Reconciliation** tab considers only hard-bookings.</span></span>

![未確認預約資源在 [協調] 索引標籤上沒有預約](media/Resource-Management-image80.png)

> [!NOTE]
> <span data-ttu-id="7cc3e-117">您無法從一般團隊成員所產生的需求對資源進行未確認預約。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-117">You can't soft-book a resource from a requirement that was generated from a generic team member.</span></span>

<span data-ttu-id="7cc3e-118">在排程面板上，資源的未確認預約會使用不同的色彩來標示。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-118">On the Schedule Board, a different coloring is used for soft bookings for a resource.</span></span>

![排程面板上的未確認預約](media/Resource-Management-image81.png)

<span data-ttu-id="7cc3e-120">若要將未確認預約轉換成已確認預約，請在排程板上以滑鼠右鍵按一下未確認預約，然後選取 **變更狀態** \> **已確認預約** \> **已確認**。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-120">To convert a soft booking to a hard booking, on the Schedule Board, right-click the soft booking, and then select **Change Status** \> **Hard Book** \> **Hard**.</span></span>

![將預約狀態變更為 [已確認]](media/Resource-Management-image82.png)

<span data-ttu-id="7cc3e-122">預約已變更，而且排程面板上的狀態也已變更。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-122">The booking is changed, and the status is changed on the Schedule Board.</span></span> <span data-ttu-id="7cc3e-123">預約狀態現在是 **已確認**，因此資源會顯示為已預約，而且其產能和可用性也會進行調整。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-123">Because the booking status is now **Hard**, the resource is shown as booked, and its capacity and availability are adjusted.</span></span>

<span data-ttu-id="7cc3e-124">您可以使用相同的方法，從排程面板中取消已確認預約或未確認預約。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-124">You can use the same method to cancel a hard booking or a soft booking from the Schedule Board.</span></span>

<span data-ttu-id="7cc3e-125">若要在專案的 **團隊** 索引標籤上將未確認預約資源轉換會已確認預約，請選取該資源，然後選取 **確認**。</span><span class="sxs-lookup"><span data-stu-id="7cc3e-125">To convert a resource that is soft-booked to hard-booked on the project's **Team** tab, select the resource, and then select **Confirm**.</span></span>

![確認命令](media/Resource-Management-image83.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]