---
title: 單位和單位群組
description: 此主題提供有關如何在 Dynamics 365 Project Operations 中建立單位和單位群組的資訊。
author: rumant
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 646e20189efb4aab56972f01a52b1bff19f2e79f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996061"
---
# <a name="units-and-unit-groups"></a><span data-ttu-id="5fb86-103">單位和單位群組</span><span class="sxs-lookup"><span data-stu-id="5fb86-103">Units and unit groups</span></span>

<span data-ttu-id="5fb86-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="5fb86-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5fb86-105">單位是用來計算您所銷售產品或服務的數量或計量。</span><span class="sxs-lookup"><span data-stu-id="5fb86-105">Units are the quantities or measurements that you sell your products or services in.</span></span> <span data-ttu-id="5fb86-106">例如，如果您銷售園藝材料，可能也會銷售整包、整盒和整個貨架為單位的種子。</span><span class="sxs-lookup"><span data-stu-id="5fb86-106">For example, if you sell gardening supplies, you might sell seeds in units of packets, boxes, and pallets.</span></span> <span data-ttu-id="5fb86-107">單位群組是這些不同單位的集合。</span><span class="sxs-lookup"><span data-stu-id="5fb86-107">A unit group is a collection of these different units.</span></span>

<span data-ttu-id="5fb86-108">若要完成本主題中的步驟，請確定您已獲指派系統管理員或 Sales Professional Manager 角色，或擁有同等權限。</span><span class="sxs-lookup"><span data-stu-id="5fb86-108">To complete the steps in this topic, make sure that you have been assigned to the System Administrator or Sales Professional Manager role or have equivalent permissions.</span></span>

## <a name="create-a-unit-group"></a><span data-ttu-id="5fb86-109">建立單位群組</span><span class="sxs-lookup"><span data-stu-id="5fb86-109">Create a unit group</span></span>

1. <span data-ttu-id="5fb86-110">在網站地圖中，選取 **單位**。</span><span class="sxs-lookup"><span data-stu-id="5fb86-110">In the site map, select **Units**.</span></span>
2. <span data-ttu-id="5fb86-111">選取 **新增，並** 在 **建立單位群組** 對話方塊中，輸入單位名稱。</span><span class="sxs-lookup"><span data-stu-id="5fb86-111">Select **New**, and in the **Create Unit Group** dialog box, enter the unit name.</span></span>
3. <span data-ttu-id="5fb86-112">在 **主要單位** 欄位中，輸入銷售產品的最小一般度量單位。</span><span class="sxs-lookup"><span data-stu-id="5fb86-112">In the **Primary unit** field, enter the lowest common unit of measure that the product will be sold in.</span></span> <span data-ttu-id="5fb86-113">例如，您可以輸入「件」或「盎司」。</span><span class="sxs-lookup"><span data-stu-id="5fb86-113">For example, you might enter "piece" or "ounce".</span></span>
4. <span data-ttu-id="5fb86-114">選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="5fb86-114">Select **OK**.</span></span>

## <a name="add-units-to-a-unit-group"></a><span data-ttu-id="5fb86-115">將單位新增至單位群組</span><span class="sxs-lookup"><span data-stu-id="5fb86-115">Add units to a unit group</span></span>

1. <span data-ttu-id="5fb86-116">開啟單位群組，並在 **相關** 索引標籤中選取 **單位**。</span><span class="sxs-lookup"><span data-stu-id="5fb86-116">Open a unit group, and on the **Related** tab, select **Units**.</span></span> <span data-ttu-id="5fb86-117">您將會看到主要單位已新增。</span><span class="sxs-lookup"><span data-stu-id="5fb86-117">You will see that the primary unit is already added.</span></span>
2. <span data-ttu-id="5fb86-118">選取 **新增單位**，並在 **快速建立：單位** 頁面的 **名稱** 欄位中，輸入單位的名稱。</span><span class="sxs-lookup"><span data-stu-id="5fb86-118">Select **Add New Unit**, and on the **Quick Create: Unit** page, in the **Name** field, enter the nanem of the unit.</span></span>
3. <span data-ttu-id="5fb86-119">在 **數量** 欄位中，輸入單位包含的數量。</span><span class="sxs-lookup"><span data-stu-id="5fb86-119">In the **QUantity** field, enter the quantity that the unit will contain.</span></span> <span data-ttu-id="5fb86-120">例如，如果一盒含有兩件，請輸入「2」。</span><span class="sxs-lookup"><span data-stu-id="5fb86-120">For example, if a box contains two pieces, enter "2".</span></span> 
4. <span data-ttu-id="5fb86-121">在 **基礎單位** 欄位中，選取基礎單位以建立單位的最小度量單位。</span><span class="sxs-lookup"><span data-stu-id="5fb86-121">In the **Base unit** field, select a base unit to establish the lowest unit of measurement for the unit.</span></span> <span data-ttu-id="5fb86-122">例如，您可能會選取 [件]。</span><span class="sxs-lookup"><span data-stu-id="5fb86-122">For example, you might select "Piece".</span></span>
5. <span data-ttu-id="5fb86-123">選取 **儲存**：</span><span class="sxs-lookup"><span data-stu-id="5fb86-123">Select **Save**:</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]