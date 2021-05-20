---
title: 定義專案行事曆
description: 本主題提供有關如何將行事曆範本套用至專案以追蹤專案排程的資訊。
author: ruhercul
manager: AnnBe
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
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
ms.openlocfilehash: 1d5642d7a2246dc878b2bc4f504f138b71d29a69
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981290"
---
# <a name="define-project-calendars"></a><span data-ttu-id="8fa67-103">定義專案行事曆</span><span class="sxs-lookup"><span data-stu-id="8fa67-103">Define project calendars</span></span>

<span data-ttu-id="8fa67-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="8fa67-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="8fa67-105">若要建立和管理專案，您必須將行事曆範本套用至專案。</span><span class="sxs-lookup"><span data-stu-id="8fa67-105">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="8fa67-106">行事曆範本會定義下列專案屬性：</span><span class="sxs-lookup"><span data-stu-id="8fa67-106">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="8fa67-107">工作時數，包括開始和結束時間</span><span class="sxs-lookup"><span data-stu-id="8fa67-107">Working hours, including start and end time</span></span>
- <span data-ttu-id="8fa67-108">工作日</span><span class="sxs-lookup"><span data-stu-id="8fa67-108">Working days</span></span>
- <span data-ttu-id="8fa67-109">行事曆例外，例如非工作日</span><span class="sxs-lookup"><span data-stu-id="8fa67-109">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="8fa67-110">套用至專案的行事曆範本是組織設定中所定義行事曆範本的複本。</span><span class="sxs-lookup"><span data-stu-id="8fa67-110">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="8fa67-111">如果您變更行事曆範本，這些變更不會傳播到專案的工作時數。</span><span class="sxs-lookup"><span data-stu-id="8fa67-111">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="8fa67-112">若要變更專案的工作時數，必須套用新的範本。</span><span class="sxs-lookup"><span data-stu-id="8fa67-112">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="8fa67-113">若要為您的組織建立行事曆範本，有兩個重要需求：</span><span class="sxs-lookup"><span data-stu-id="8fa67-113">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="8fa67-114">使用新的或現有的可預約資源定義範本所需的工作時數。</span><span class="sxs-lookup"><span data-stu-id="8fa67-114">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="8fa67-115">建立新的行事曆範本，並將範本與可預約資源產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8fa67-115">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="8fa67-116">**定義範本的工作時數**</span><span class="sxs-lookup"><span data-stu-id="8fa67-116">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="8fa67-117">移至 **資源** \> **資源**。</span><span class="sxs-lookup"><span data-stu-id="8fa67-117">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="8fa67-118">建立要在行事曆範本中參考的新資源，或選取現有的資源。</span><span class="sxs-lookup"><span data-stu-id="8fa67-118">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="8fa67-119">選擇 資源的 **工作時數** 索引標籤，並完成[設定資源的工作時數](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource)中的指示以設定行事曆規則。</span><span class="sxs-lookup"><span data-stu-id="8fa67-119">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="8fa67-120">**建立新的行事曆範本**</span><span class="sxs-lookup"><span data-stu-id="8fa67-120">**Create a new calendar template**</span></span>

1. <span data-ttu-id="8fa67-121">移至 **設定** \> **事曆範本**。</span><span class="sxs-lookup"><span data-stu-id="8fa67-121">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="8fa67-122">選取 **新增**，然後輸入名稱、描述和範本資源。</span><span class="sxs-lookup"><span data-stu-id="8fa67-122">Select **New**, and enter a name, description, and template resource.</span></span>

> [!NOTE]
> <span data-ttu-id="8fa67-123">在行事曆範本中參考資源時，資源行事曆的複本會與行事曆範本產生關聯。</span><span class="sxs-lookup"><span data-stu-id="8fa67-123">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="8fa67-124">如果複本範本的工作時數變更，這些變更不會傳播到行事曆範本。</span><span class="sxs-lookup"><span data-stu-id="8fa67-124">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>

<span data-ttu-id="8fa67-125">您現在可以將工作範本與專案行事曆範本建立關聯。</span><span class="sxs-lookup"><span data-stu-id="8fa67-125">You can now associate the work template with a project calendar template.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]

