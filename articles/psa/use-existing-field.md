---
title: 使用 Project Service 中現有的欄位做為定價維度
description: 本主題提供有關使用現有 Project Service 欄位做為定價維度的資訊。
author: Rumant
ms.custom:
- dyn365-projectservice
ms.date: 11/19/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 3d8251b4516b4598c9c92779c59b9609d8113ac9
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8580124"
---
# <a name="use-an-existing-field-in-project-service-as-a-pricing-dimension"></a>使用 Project Service 中現有的欄位做為定價維度

[!include [banner](../includes/psa-now-project-operations.md)]

Project Service Automation (PSA) 的 **實際值** 實體上有許多欄位，可以用來做為專案組織中資源型定價的定價維度。 例如，其中一個常用的欄位是 **可預約資源**。 可計費資源少於 20-30 個的小型公司可能會發現讓每項資源有各自特定的帳單費率與成本費率是比較簡單的方法。 不過，隨著可計費工作力 (員工人數) 擴增，當資源成本和帳單費率開始因資源職位高升、經驗增加或取得其他技能集而改變時，要維持特定費率就會變得不切實際。 由於這種方法對特定規模的公司仍然適用，因此請參閱[使用可預約資源做為定價維度](bookable-resource-pricing-dimension.md)，以了解如何使用現有的 Project Service 欄位做為定價維度。

另一個例子是交易類別的欄位。 客戶與實作者已在 PSA 中使用交易類別來分類工作，並使用該欄位以根據工作類別來估算價格和成本。 如需詳細資訊，請參閱[使用交易類別做為定價維度](transaction-category-pricing-dimension.md)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
