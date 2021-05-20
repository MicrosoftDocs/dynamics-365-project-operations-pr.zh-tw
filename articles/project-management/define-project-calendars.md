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
# <a name="define-project-calendars"></a>定義專案行事曆

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

若要建立和管理專案，您必須將行事曆範本套用至專案。 行事曆範本會定義下列專案屬性：

- 工作時數，包括開始和結束時間
- 工作日
- 行事曆例外，例如非工作日

套用至專案的行事曆範本是組織設定中所定義行事曆範本的複本。

> [!NOTE]
> 如果您變更行事曆範本，這些變更不會傳播到專案的工作時數。 若要變更專案的工作時數，必須套用新的範本。

若要為您的組織建立行事曆範本，有兩個重要需求：

- 使用新的或現有的可預約資源定義範本所需的工作時數。
- 建立新的行事曆範本，並將範本與可預約資源產生關聯。

**定義範本的工作時數**

1. 移至 **資源** \> **資源**。
2. 建立要在行事曆範本中參考的新資源，或選取現有的資源。
3. 選擇 資源的 **工作時數** 索引標籤，並完成[設定資源的工作時數](https://docs.microsoft.com/dynamics365/field-service/set-work-hours-resource)中的指示以設定行事曆規則。

**建立新的行事曆範本**

1. 移至 **設定** \> **事曆範本**。
2. 選取 **新增**，然後輸入名稱、描述和範本資源。

> [!NOTE]
> 在行事曆範本中參考資源時，資源行事曆的複本會與行事曆範本產生關聯。 如果複本範本的工作時數變更，這些變更不會傳播到行事曆範本。

您現在可以將工作範本與專案行事曆範本建立關聯。


[!INCLUDE[footer-include](../includes/footer-banner.md)]

