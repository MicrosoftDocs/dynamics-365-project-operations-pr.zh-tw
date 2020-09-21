---
title: 技能和熟練度模型
description: 此主題提供有關如何使用技能和熟練模型的資訊。
author: ruhercul
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 03/13/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.assetid: d55a6d72-905f-4b82-a9fe-0b6b082473a6
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
ms.openlocfilehash: fe4c9a62cd2ec1365daa09714fa6fa19210a7770
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749991"
---
# <a name="skills-and-proficiency-models"></a>技能和熟練度模型

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

技能是在 Dynamics 365 Project Service Automation 與 (如果存在) Dynamics 365 Field Service 之間共用的資源特性。 

若要在 Project Service Automation 中維護技能存放庫，請移至**資源** \> **資源技能**。 

> ![資源技能](media/Resource-Management-image84.png)

## <a name="use-proficiency-models-to-rate-resources"></a>使用熟練度模型來評等資源

資源的技能由熟練程度模型所評等。 個別評等是在熟練度模型中。 

1. 若要建立熟練度模型，請移至**資源**\>**熟練度模型**，然後選取**新增**。
2. 在新的評等模型中，指定最小評等值、最大評等值以及要加以評等的實體。
3. 在**評等值**子格中，您可以定義從最小值到最大值的不同評等值。

> ![定義的最小與最大評等](media/Resource-Management-image85.png)

這些評等值會顯示在**資源需求**、**排程面板和**和**排程小幫手**篩選上。
