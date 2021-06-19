---
title: 技能和熟練度模型
description: 此主題提供有關如何使用技能和熟練模型的資訊。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
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
ms.openlocfilehash: 976650cc71b0cdb75d5ce2d7532cd78bd91d3670
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6008661"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="f88eb-103">技能和熟練度模型</span><span class="sxs-lookup"><span data-stu-id="f88eb-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="f88eb-104">技能是在 Dynamics 365 Project Service Automation 與 (如果存在) Dynamics 365 Field Service 之間共用的資源特性。</span><span class="sxs-lookup"><span data-stu-id="f88eb-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="f88eb-105">若要在 Project Service Automation 中維護技能存放庫，請移至 **資源** \> **資源技能**。</span><span class="sxs-lookup"><span data-stu-id="f88eb-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![資源技能](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="f88eb-107">使用熟練度模型來評等資源</span><span class="sxs-lookup"><span data-stu-id="f88eb-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="f88eb-108">資源的技能由熟練程度模型所評等。</span><span class="sxs-lookup"><span data-stu-id="f88eb-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="f88eb-109">個別評等是在熟練度模型中。</span><span class="sxs-lookup"><span data-stu-id="f88eb-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="f88eb-110">若要建立熟練度模型，請移至 **資源**\>**熟練度模型**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="f88eb-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="f88eb-111">在新的評等模型中，指定最小評等值、最大評等值以及要加以評等的實體。</span><span class="sxs-lookup"><span data-stu-id="f88eb-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="f88eb-112">在 **評等值** 子格中，您可以定義從最小值到最大值的不同評等值。</span><span class="sxs-lookup"><span data-stu-id="f88eb-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![定義的最小與最大評等](media/Resource-Management-image85.png)

<span data-ttu-id="f88eb-114">這些評等值會顯示在 **資源需求**、**排程面板和** 和 **排程小幫手** 篩選上。</span><span class="sxs-lookup"><span data-stu-id="f88eb-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]