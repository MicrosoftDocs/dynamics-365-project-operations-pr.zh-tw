---
title: 定義技能和熟練度
description: 此主題提供有關如何設定熟練模型以評等資源的資訊。
author: ruhercul
manager: AnnBe
ms.date: 09/23/2020
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
ms.author: ruhercul
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 24538ed1d610a0cae4c2badc0fd33c2f738a8338
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072940"
---
# <a name="define-skills-and-proficiencies"></a>定義技能和熟練度

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

技能是在 Dynamics 365 Project Operations 與 (如果存在) Dynamics 365 Field Service 之間共用的資源特性。 

- 若要在 Project Operations 中維護技能存放庫，請移至 **資源** \> **資源技能** 。 

## <a name="use-proficiency-models-to-rate-resources"></a>使用熟練度模型來評等資源

資源的技能由熟練程度模型所評等。 個別評等是在熟練度模型中。 

1. 若要建立熟練度模型，請移至 **資源**\>**熟練度模型** ，然後選取 **新增** 。
2. 在新的評等模型中，指定最小評等值、最大評等值以及要加以評等的實體。
3. 在 **評等值** 子格中，您可以定義從最小值到最大值的不同評等值。


這些評等值會顯示在 **資源需求** 、 **排程面板和** 和 **排程小幫手** 篩選上。
