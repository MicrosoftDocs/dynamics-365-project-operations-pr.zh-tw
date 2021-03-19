---
title: 設定保留款排程
description: 此主題提供如何在 Project Operations 中設定保留款排程的資訊。
author: rumant
manager: Annbe
ms.date: 10/22/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d90781407f11c93b9fb9e0cd2446e102e216b8db
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5272243"
---
# <a name="set-up-a-retainer-schedule"></a><span data-ttu-id="21769-103">設定保留款排程</span><span class="sxs-lookup"><span data-stu-id="21769-103">Set up a retainer schedule</span></span>

<span data-ttu-id="21769-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="21769-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="21769-105">在 Dynamics 365 Project Operations 的 **專案合約** 頁面上設定保留款排程。</span><span class="sxs-lookup"><span data-stu-id="21769-105">Retainer schedules are set up on the **Project Contract** page in Dynamics 365 Project Operations.</span></span>

1. <span data-ttu-id="21769-106">在 **專案合約** 頁面的 **預付款和保留款** 索引標籤中，選取 **設定保留款排程**。</span><span class="sxs-lookup"><span data-stu-id="21769-106">On the **Project Contract** page, on the **Advances and Retainers** tab, select **Set up retainer schedule**.</span></span>
2. <span data-ttu-id="21769-107">在開啟的對話方塊頁面上，會顯示下表列出的欄位。</span><span class="sxs-lookup"><span data-stu-id="21769-107">On the dialog page that opens, the fields listed in the following table are shown.</span></span> <span data-ttu-id="21769-108">下表給出了所輸入的值如何影響將建立的保留款排程的想法。</span><span class="sxs-lookup"><span data-stu-id="21769-108">The table gives an idea on how the entered values impact or influence the retainer schedule that will be created.</span></span>

| <span data-ttu-id="21769-109">欄位</span><span class="sxs-lookup"><span data-stu-id="21769-109">Field</span></span> | <span data-ttu-id="21769-110">描述</span><span class="sxs-lookup"><span data-stu-id="21769-110">Description</span></span> | <span data-ttu-id="21769-111">下游影響</span><span class="sxs-lookup"><span data-stu-id="21769-111">Downstream impact</span></span> |
| --- | --- | --- |
| <span data-ttu-id="21769-112">專案合約客戶</span><span class="sxs-lookup"><span data-stu-id="21769-112">Project Contract Customer</span></span> | <span data-ttu-id="21769-113">要為合約上的哪個客戶開立此保留款或預付金的發票。</span><span class="sxs-lookup"><span data-stu-id="21769-113">The customer on the contract who will be invoiced for this retainer or advance.</span></span> | <span data-ttu-id="21769-114">如果合約上有多個客戶，而您想要為其中每一個客戶開立特定保留款或預付款金額的發票時，請為每個客戶手動建立一個發票。</span><span class="sxs-lookup"><span data-stu-id="21769-114">If you have multiple customers on the contract, and if you need to invoice each of them for a specific retainer or advance amount, manually create one invoice for each customer.</span></span> |
| <span data-ttu-id="21769-115">保留款排程開始</span><span class="sxs-lookup"><span data-stu-id="21769-115">Retainer Schedule Start</span></span> | <span data-ttu-id="21769-116">輸入保留款排程的開始日期。</span><span class="sxs-lookup"><span data-stu-id="21769-116">Enter the start date of the retainer schedule.</span></span> | <span data-ttu-id="21769-117">此日期可能不是建立第一個保留款或預付金的日期。</span><span class="sxs-lookup"><span data-stu-id="21769-117">This date may not be the date on which the first retainer or advance is created.</span></span> <span data-ttu-id="21769-118">建立第一個保留款或預付金的日期也會受到發票頻率的影響。</span><span class="sxs-lookup"><span data-stu-id="21769-118">The date on which the first retainer or advance is created, is also influenced by the invoice frequency.</span></span> |
| <span data-ttu-id="21769-119">保留款排程結束</span><span class="sxs-lookup"><span data-stu-id="21769-119">Retainer Schedule End</span></span> | <span data-ttu-id="21769-120">輸入保留款排程的結束日期。</span><span class="sxs-lookup"><span data-stu-id="21769-120">Enter the end date of the retainer schedule.</span></span> | <span data-ttu-id="21769-121">此日期可能不是建立最後一個保留款或預付金的日期。</span><span class="sxs-lookup"><span data-stu-id="21769-121">This date may not be the date on which the last retainer or advance is created.</span></span> <span data-ttu-id="21769-122">建立最後一個保留款或預付金的日期也會受到發票頻率的影響。</span><span class="sxs-lookup"><span data-stu-id="21769-122">The date on which the last retainer or advance is created is also influenced by the invoice frequency.</span></span> |
| <span data-ttu-id="21769-123">要建立的保留款數目</span><span class="sxs-lookup"><span data-stu-id="21769-123">Number of Retainers to Create</span></span> | <span data-ttu-id="21769-124">當您輸入要建立的保留款數目時，系統會使用開始日期和頻率來建立此欄位中的數目。</span><span class="sxs-lookup"><span data-stu-id="21769-124">When you enter the number of retainers to create, the system uses the start date and frequency to create the number in this field.</span></span> | <span data-ttu-id="21769-125">手動更新此欄位時，系統會忽略 **保留款排程結束** 欄位中的值，而是建立特定數目的保留款或預付款。</span><span class="sxs-lookup"><span data-stu-id="21769-125">When this field is manually updated, the system ignores the value in the **Retainer Schedule End** field and instead creates the specific number of retainers or advances.</span></span> |
| <span data-ttu-id="21769-126">發票頻率</span><span class="sxs-lookup"><span data-stu-id="21769-126">Invoice Frequency</span></span> | <span data-ttu-id="21769-127">應用程式建立保留款和預付款的頻率。</span><span class="sxs-lookup"><span data-stu-id="21769-127">How often the application will create retainers and advances.</span></span> | <span data-ttu-id="21769-128">此值會直接影響保留款和預付款的數目，以及建立的日期。</span><span class="sxs-lookup"><span data-stu-id="21769-128">This value directly influences the number of retainers and advances and the created dates.</span></span> |
| <span data-ttu-id="21769-129">總金額</span><span class="sxs-lookup"><span data-stu-id="21769-129">Total Amount</span></span> | <span data-ttu-id="21769-130">總計金額是指分割成要建立的各個保留款或預付款的金額。</span><span class="sxs-lookup"><span data-stu-id="21769-130">The total amount is the amount that is split into the individual retainer or advance payments that will be created.</span></span> | <span data-ttu-id="21769-131">此欄位沒有任何下游影響。</span><span class="sxs-lookup"><span data-stu-id="21769-131">There's no downstream impact for this field.</span></span> |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]