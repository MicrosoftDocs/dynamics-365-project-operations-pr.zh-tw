---
title: 從項目需求接收採購單上的項目
description: 本主題說明如何從項目需求接收採購單上的項目。
author: Yowelle
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a5b3622458da957ed150311f6ea75d5f1444d5f1
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073163"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a><span data-ttu-id="aa23f-103">從項目需求接收採購單上的項目</span><span class="sxs-lookup"><span data-stu-id="aa23f-103">Receive items on purchase order from item requirement</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="aa23f-104">本主題說明如何從項目需求接收採購單上的項目。</span><span class="sxs-lookup"><span data-stu-id="aa23f-104">This topic explains how to receive items on a purchase order from an item requirement.</span></span>

<span data-ttu-id="aa23f-105">您可以使用項目需求 (而不是項目交易)，計劃好就在實際使用項目之前交貨、建立採購單、將項目納入交易合約架構中，以及將項目需求包含在生產規劃中。</span><span class="sxs-lookup"><span data-stu-id="aa23f-105">By using an item requirement instead of an item transaction, you can plan for delivery just before the item is actually used, create a purchase order, include the item in the trade-agreement framework, and include the item requirement in production planning.</span></span> 

<span data-ttu-id="aa23f-106">此工作會使用 USSI 資料集。</span><span class="sxs-lookup"><span data-stu-id="aa23f-106">This task uses the USSI data set.</span></span>

1. <span data-ttu-id="aa23f-107">在導覽窗格中，移至 **模組 > 專案管理與會計 > 專案 > 所有專案** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-107">In the navigation pane, go to **Modules > Project management and accounting > Projects > All projects**.</span></span>
2. <span data-ttu-id="aa23f-108">在清單中，選取所需列中的連結。</span><span class="sxs-lookup"><span data-stu-id="aa23f-108">In the list, select the link in the desired row.</span></span>
3. <span data-ttu-id="aa23f-109">在動作窗格上，選取 **計劃** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-109">On the Action Pane, select **Plan**.</span></span>
4. <span data-ttu-id="aa23f-110">選取 **項目需求** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-110">Select **Item requirements**.</span></span>
5. <span data-ttu-id="aa23f-111">選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-111">Select **New**.</span></span>
6. <span data-ttu-id="aa23f-112">在新的列中，輸入或選取 **項目編號** 欄位中的值。</span><span class="sxs-lookup"><span data-stu-id="aa23f-112">In the new row, enter or select a value in the **Item number** field.</span></span>
7. <span data-ttu-id="aa23f-113">在 **數量** 欄位中，輸入數字。</span><span class="sxs-lookup"><span data-stu-id="aa23f-113">In the **Quantity** field, enter a number.</span></span>
8. <span data-ttu-id="aa23f-114">選取 **儲存** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-114">Select **Save**.</span></span>
9. <span data-ttu-id="aa23f-115">在動作窗格上，選取 **管理** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-115">On the Action Pane, select **Manage**.</span></span>
10. <span data-ttu-id="aa23f-116">選取 **函數** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-116">Select **Functions**.</span></span>
11. <span data-ttu-id="aa23f-117">選取 **建立採購單** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-117">Select **Create purchase order**.</span></span>
12. <span data-ttu-id="aa23f-118">選取 **全部包含** 核取方塊。</span><span class="sxs-lookup"><span data-stu-id="aa23f-118">Select the **Include all** check box.</span></span>
13. <span data-ttu-id="aa23f-119">在 **供應商客戶** 欄位中，輸入或選取值。</span><span class="sxs-lookup"><span data-stu-id="aa23f-119">In the **Vendor account** field, enter or select a value.</span></span>
14. <span data-ttu-id="aa23f-120">選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-120">Select **OK**.</span></span>
15. <span data-ttu-id="aa23f-121">在導覽窗格中，移至 **模組 > 應付帳款 > 採購單 > 所有採購單** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-121">In the navigation pane, go to **Modules > Accounts payable > Purchase orders > All purchase orders**.</span></span>
16. <span data-ttu-id="aa23f-122">在清單中，選取所需列中的連結。</span><span class="sxs-lookup"><span data-stu-id="aa23f-122">In the list, select the link in the desired row.</span></span>
17. <span data-ttu-id="aa23f-123">在動作窗格上，選取 **購買** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-123">On the Action Pane, select **Purchase**.</span></span>
18. <span data-ttu-id="aa23f-124">選取 **確認** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-124">Select **Confirm**.</span></span>
19. <span data-ttu-id="aa23f-125">在動作窗格上，選取 **接收** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-125">On the Action Pane, select **Receive**.</span></span>
20. <span data-ttu-id="aa23f-126">選取 **產品收據** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-126">Select **Product receipt**.</span></span>
21. <span data-ttu-id="aa23f-127">在 **產品收據** 欄位中，輸入值。</span><span class="sxs-lookup"><span data-stu-id="aa23f-127">In the **Product receipt** field, type a value.</span></span>
22. <span data-ttu-id="aa23f-128">選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="aa23f-128">Select **OK**.</span></span>

