---
title: 建立工作時數範本
description: 本主題說明如何建立 Project Service 中的工作時數範本。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
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
ms.openlocfilehash: 525f601ad6fee902cb6d5c128b596cc2d33f30c4
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981245"
---
# <a name="create-a-work-hours-template-project-service"></a><span data-ttu-id="7ba35-103">建立工作時數範本 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="7ba35-103">Create a work hours template (Project Service)</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="7ba35-104">若要建立和管理專案，您必須將行事曆範本套用至專案。</span><span class="sxs-lookup"><span data-stu-id="7ba35-104">To create and manage a project, you must apply a calendar template to the project.</span></span> <span data-ttu-id="7ba35-105">行事曆範本會定義下列專案屬性：</span><span class="sxs-lookup"><span data-stu-id="7ba35-105">The calendar template defines the following project attributes:</span></span>

- <span data-ttu-id="7ba35-106">工作時數，包括開始和結束時間</span><span class="sxs-lookup"><span data-stu-id="7ba35-106">Working hours, including start and end time</span></span>
- <span data-ttu-id="7ba35-107">工作日</span><span class="sxs-lookup"><span data-stu-id="7ba35-107">Working days</span></span>
- <span data-ttu-id="7ba35-108">行事曆例外，例如非工作日</span><span class="sxs-lookup"><span data-stu-id="7ba35-108">Calendar exceptions such as non-working days</span></span>

<span data-ttu-id="7ba35-109">套用至專案的行事曆範本是組織設定中所定義行事曆範本的複本。</span><span class="sxs-lookup"><span data-stu-id="7ba35-109">The calendar template that's applied to a project is a copy of the calendar template defined in your organization’s settings.</span></span>

> [!NOTE]
> <span data-ttu-id="7ba35-110">如果您變更行事曆範本，這些變更不會傳播到專案的工作時數。</span><span class="sxs-lookup"><span data-stu-id="7ba35-110">If you change the calendar template, those changes don't propagate to the working hours of the project.</span></span> <span data-ttu-id="7ba35-111">若要變更專案的工作時數，必須套用新的範本。</span><span class="sxs-lookup"><span data-stu-id="7ba35-111">To change the working hours of the project, a new template must be applied.</span></span>

<span data-ttu-id="7ba35-112">若要為您的組織建立行事曆範本，有兩個重要需求：</span><span class="sxs-lookup"><span data-stu-id="7ba35-112">To create a calendar template for your organization, there are two key requirements:</span></span>

- <span data-ttu-id="7ba35-113">使用新的或現有的可預約資源定義範本所需的工作時數。</span><span class="sxs-lookup"><span data-stu-id="7ba35-113">Define the desired working hours of the template using a new or existing bookable resource.</span></span>
- <span data-ttu-id="7ba35-114">建立新的行事曆範本，並將範本與可預約資源產生關聯。</span><span class="sxs-lookup"><span data-stu-id="7ba35-114">Create a new calendar template and associate the template with the bookable resource.</span></span>

<span data-ttu-id="7ba35-115">**定義範本的工作時數**</span><span class="sxs-lookup"><span data-stu-id="7ba35-115">**Define the working hours of the template**</span></span>

1. <span data-ttu-id="7ba35-116">移至 **資源** \> **資源**。</span><span class="sxs-lookup"><span data-stu-id="7ba35-116">Go to **Resources** \> **Resources**.</span></span>
2. <span data-ttu-id="7ba35-117">建立要在行事曆範本中參考的新資源，或選取現有的資源。</span><span class="sxs-lookup"><span data-stu-id="7ba35-117">Create a new resource to reference in the calendar template, or select an existing resource.</span></span>
3. <span data-ttu-id="7ba35-118">選擇 資源的 **工作時數** 索引標籤，並完成[設定資源的工作時數](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource)中的指示以設定行事曆規則。</span><span class="sxs-lookup"><span data-stu-id="7ba35-118">Select the **Work Hours** tab of the resource and complete the instructions in [Set work hours for a resource](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource) to configure the calendar rules.</span></span>

<span data-ttu-id="7ba35-119">**建立新的行事曆範本**</span><span class="sxs-lookup"><span data-stu-id="7ba35-119">**Create a new calendar template**</span></span>

1. <span data-ttu-id="7ba35-120">移至 **設定** \> **事曆範本**。</span><span class="sxs-lookup"><span data-stu-id="7ba35-120">Go to **Settings** \> **Calendar Template**.</span></span>
2. <span data-ttu-id="7ba35-121">選取 **新增**，然後輸入名稱、描述和範本資源。</span><span class="sxs-lookup"><span data-stu-id="7ba35-121">Select **New**, and enter a name, description, and template resource.</span></span>


> [!NOTE]
> <span data-ttu-id="7ba35-122">在行事曆範本中參考資源時，資源行事曆的複本會與行事曆範本產生關聯。</span><span class="sxs-lookup"><span data-stu-id="7ba35-122">When a resource is referenced in a calendar template, a copy of the resource’s calendar is associated with the calendar template.</span></span> <span data-ttu-id="7ba35-123">如果複本範本的工作時數變更，這些變更不會傳播到行事曆範本。</span><span class="sxs-lookup"><span data-stu-id="7ba35-123">If the working hours of the copied template change, those changes will not propagate to the calendar template.</span></span>


### <a name="see-also"></a><span data-ttu-id="7ba35-124">請參閱</span><span class="sxs-lookup"><span data-stu-id="7ba35-124">See Also</span></span>  
 [<span data-ttu-id="7ba35-125">設定資源</span><span class="sxs-lookup"><span data-stu-id="7ba35-125">Set up resources</span></span>](../psa/set-up-resources.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
