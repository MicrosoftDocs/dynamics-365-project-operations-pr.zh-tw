---
title: 單位和單位群組
description: 此主題提供有關如何在 Dynamics 365 Project Operations 中建立單位和單位群組的資訊。
author: rumant
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
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 345a4f38ad0bc5acddb90cfd8cb3e92154e46513
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073119"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="2de39-103">單位和單位群組</span><span class="sxs-lookup"><span data-stu-id="2de39-103">Units and unit groups</span></span>

<span data-ttu-id="2de39-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="2de39-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="2de39-105">單位是用來計算您所銷售產品或服務的數量或計量。</span><span class="sxs-lookup"><span data-stu-id="2de39-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="2de39-106">例如，如果您銷售園藝材料，可能也會銷售整包、整盒和整個貨架為單位的種子。</span><span class="sxs-lookup"><span data-stu-id="2de39-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="2de39-107">單位群組是這些不同單位的集合。</span><span class="sxs-lookup"><span data-stu-id="2de39-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="2de39-108">若要完成本主題中的步驟，請確定您已獲指派系統管理員或 Sales Professional Manager 角色，或擁有同等權限。</span><span class="sxs-lookup"><span data-stu-id="2de39-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="2de39-109">建立單位群組</span><span class="sxs-lookup"><span data-stu-id="2de39-109">Create a unit group</span></span>

1. <span data-ttu-id="2de39-110">在網站地圖中，選取 **單位** 。</span><span class="sxs-lookup"><span data-stu-id="2de39-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="2de39-111">選取 **新增，並** 在 **建立單位群組** 對話方塊中，輸入單位名稱。</span><span class="sxs-lookup"><span data-stu-id="2de39-111">Select **New** , and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="2de39-112">在 **主要單位** 欄位中，輸入銷售產品的最小一般度量單位。</span><span class="sxs-lookup"><span data-stu-id="2de39-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="2de39-113">例如，您可以輸入「件」或「盎司」。</span><span class="sxs-lookup"><span data-stu-id="2de39-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="2de39-114">選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="2de39-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="2de39-115">將單位新增至單位群組</span><span class="sxs-lookup"><span data-stu-id="2de39-115">Add units to a unit group</span></span>

1. <span data-ttu-id="2de39-116">開啟單位群組，並在 **相關** 索引標籤中選取 **單位** 。</span><span class="sxs-lookup"><span data-stu-id="2de39-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="2de39-117">您將會看到主要單位已新增。</span><span class="sxs-lookup"><span data-stu-id="2de39-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="2de39-118">選取 **新增單位** ，並在 **快速建立：單位** 頁面的 **名稱** 欄位中，輸入單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="2de39-118">Select **Add New Unit** , and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="2de39-119">在 **數量** 欄位中，輸入單位包含的數量。</span><span class="sxs-lookup"><span data-stu-id="2de39-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="2de39-120">例如，如果一盒含有兩件，請輸入「2」。</span><span class="sxs-lookup"><span data-stu-id="2de39-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="2de39-121">在 **基礎單位** 欄位中，選取基礎單位以建立單位的最小度量單位。</span><span class="sxs-lookup"><span data-stu-id="2de39-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="2de39-122">例如，您可能會選取 [件]。</span><span class="sxs-lookup"><span data-stu-id="2de39-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="2de39-123">選取 **儲存** ：</span><span class="sxs-lookup"><span data-stu-id="2de39-123">Select **Save** :</span></span>
