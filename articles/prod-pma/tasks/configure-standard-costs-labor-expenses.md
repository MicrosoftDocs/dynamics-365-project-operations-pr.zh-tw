---
title: 設定人力和費用的標準成本
description: 本主題說明如何設定專案的人力和費用標準成本。
author: Yowelle
manager: AnnBe
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjCostPriceHour, ProjSalesPriceHour, ProjCostPriceExpense, ProjSalesPriceCost
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b3eb6b1d4d75b095383689dd53a59a15fe9e884a
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073053"
---
# <a name="configure-standard-costs-for-labor-and-expenses"></a>設定人力和費用的標準成本

[!include [banner](../../includes/banner.md)]

本主題說明如何設定專案的人力和費用標準成本。 此工作會使用 USSI 資料集。

1. 在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 成本價 (小時)** 。
2. 選取 **新增** 。
3. 在 **生效日期** 欄位中，輸入日期。
4. 在 **成本價** 欄位中，輸入數字。 您可以設定專案類別的標準成本價，也可以依工作者編號、專案編號、類別、日期或任何這些項目的組合來設定成本價。 所套用的成本價是詳細等級最高的成本價。  
5. 選取 **儲存** 。
6. 在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 售價 (小時)** 。
7. 選取 **新增** 。
8. 在 **生效日期** 欄位中，輸入日期。
9. 在 **有效期間** 欄位中，選取選項。
10. 在 **定價** 欄位中，輸入數字。 您可以設定工時交易或專案類別設的標準售價。 您也可以依工作者編號、專案編號、類別、交易日期或這些項目的任意組合來設定售價。 工作者在工時日記帳輸入交易時所套用的實際售價是詳細等級最高的售價。 例如，如果一般售價和工作者特定售價都已設定，則會使用工作者特定售價。  
11. 選取 **儲存** 。
12. 關閉頁面。
13. 在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 成本價 (費用)** 。
14. 選取 **新增** 。
15. 在 **生效日期** 欄位中，輸入日期。
16. 在 **成本價** 欄位中，輸入數字。 您可以填入多個欄位，但這是儲存記錄所需的最少欄位。  
17. 選取 **儲存** 。
18. 在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 售價 (費用)** 。
19. 選取 **新增** 。
20. 在 **生效日期** 欄位中，輸入日期。
21. 在 **有效期間** 欄位中，選取選項。
22. 在 **定價** 欄位中，輸入數字。 工作者在費用日記帳輸入交易時所套用的實際售價是詳細等級最高的售價。 例如，如果一般售價和工作者特定售價都已設定，則會使用工作者特定售價。  
23. 選取 **儲存** 。

