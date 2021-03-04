---
title: 為什麼費用成本實際值上的價格會預設為零？
description: 排解費用成本實際值上的價格為何預設為 0 的問題。
author: rumant
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/22/2018
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: f6ea664f9f38621ce5d1b0dd033d7df491f845ff
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5146338"
---
# <a name="why-is-the-price-defaulting-to-zero-on-expense-cost-actuals"></a>為什麼費用成本實際值上的價格會預設為零

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

本常見問題集適用於交易類別設為 [費用] 且交易類型為 [成本] 的費用實際值。

## <a name="troubleshooting-cost-rates-on-expense-cost-actuals"></a>排解有關費用成本實際值的成本費率問題

移至相關的費用項目，並確定費用項目欄位中有金額。 如果原始費用項目沒有填入金額欄位，您就找到了問題所在。
 
若要解決此問題，請重新建立包含有效金額的費用項目，並予以核准。
