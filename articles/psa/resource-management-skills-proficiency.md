---
title: 技能和熟練度模型
description: 此主題提供有關如何使用技能和熟練模型的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
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
ms.openlocfilehash: c7da8b2a7eda51b2aa7cf04e325a92f33d834efc
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5147463"
---
# <a name="skills-and-proficiency-models"></a><span data-ttu-id="300c3-103">技能和熟練度模型</span><span class="sxs-lookup"><span data-stu-id="300c3-103">Skills and proficiency models</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="300c3-104">技能是在 Dynamics 365 Project Service Automation 與 (如果存在) Dynamics 365 Field Service 之間共用的資源特性。</span><span class="sxs-lookup"><span data-stu-id="300c3-104">Skills are resource characteristics that are shared between Dynamics 365 Project Service Automation and if present, Dynamics 365 Field Service.</span></span> 

<span data-ttu-id="300c3-105">若要在 Project Service Automation 中維護技能存放庫，請移至 **資源** \> **資源技能**。</span><span class="sxs-lookup"><span data-stu-id="300c3-105">To maintain the repository of skills in Project Service Automation, go to **Resources** \> **Resource Skills**.</span></span> 

> ![資源技能](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a><span data-ttu-id="300c3-107">使用熟練度模型來評等資源</span><span class="sxs-lookup"><span data-stu-id="300c3-107">Use proficiency models to rate resources</span></span>

<span data-ttu-id="300c3-108">資源的技能由熟練程度模型所評等。</span><span class="sxs-lookup"><span data-stu-id="300c3-108">Skills for resources are rated by proficiency models.</span></span> <span data-ttu-id="300c3-109">個別評等是在熟練度模型中。</span><span class="sxs-lookup"><span data-stu-id="300c3-109">The individual ratings are in a proficiency model.</span></span> 

1. <span data-ttu-id="300c3-110">若要建立熟練度模型，請移至 **資源**\>**熟練度模型**，然後選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="300c3-110">To create a proficiency model, go to **Resources** \> **Proficiency Models**, and then select **New**.</span></span>
2. <span data-ttu-id="300c3-111">在新的評等模型中，指定最小評等值、最大評等值以及要加以評等的實體。</span><span class="sxs-lookup"><span data-stu-id="300c3-111">In the new rating model, specify the minimum rating value, the maximum rating value, and the entity that is being rated.</span></span>
3. <span data-ttu-id="300c3-112">在 **評等值** 子格中，您可以定義從最小值到最大值的不同評等值。</span><span class="sxs-lookup"><span data-stu-id="300c3-112">In the **Rating Values** subgrid, you can define the different rating values, from the minimum to the maximum.</span></span>

> ![定義的最小與最大評等](media/Resource-Management-image85.png)

<span data-ttu-id="300c3-114">這些評等值會顯示在 **資源需求**、**排程面板和** 和 **排程小幫手** 篩選上。</span><span class="sxs-lookup"><span data-stu-id="300c3-114">These rating values are shown on the **Resource Requirements**, **Schedule Board**, and **Schedule Assistant** filters.</span></span>
