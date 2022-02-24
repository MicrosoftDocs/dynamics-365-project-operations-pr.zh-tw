---
title: 設定公司之間的專案發票開立
description: 本主題說明如何設定您組織中兩家公司之間的專案發票開立。
author: Yowelle
manager: AnnBe
ms.date: 07/29/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: VendTable, InterCompanyTradingRelationSetupVendor, SysDataAreaSelectLookup, ProjParameters, ProjPosting, ProjTransferPrice
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 1cb53cb63ee11082146455ec9f13790501dc3d1d
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073055"
---
# <a name="configure-intercompany-project-invoicing"></a>設定公司之間的專案發票開立

[!include [banner](../../includes/banner.md)]

本主題說明如何設定您組織中兩家公司之間的專案發票開立。 此工作會使用 USSI 資料集。

1. 在導覽窗格中，移至 **模組 > 應付帳款 > 供應商 > 所有供應商**。
2. 在 **所有供應商** 清單中，尋找並選取所需的記錄。
3. 在動作窗格上，選取 **一般**。
4. 選取 **公司之間**。
5. 將 **使用中** 設定為 **是** 以啟用公司間的交易。
6. 在 **客戶公司** 欄位中，輸入或選取值。
7. 在 **我的客戶** 欄位中，輸入或選取值。
8. 選取 **儲存**。
9. 關閉頁面以返回首頁。
10. 在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 專案管理與會計參數**。
11. 選取 **公司之間** 索引標籤。
12. 將滑桿移到 **是**，以啟用公司間的資源排程和時程表。
13. 在清單中，標記所選取的列。
14. 選取 **新增**。
15. 在 **瀏覽法律實體** 欄位中，輸入或選取值。
16. 選取 **應計收入** 核取方塊。
17. 在 **預設時程表類別** 欄位中，輸入或選取值。
18. 在 **預設費用類別** 欄位中，輸入或選取值。
19. 選取 **儲存**。
20. 關閉頁面。
21. 在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 過帳 > 總帳過帳設定**。
22. 在 **總帳會計科目類型** 欄位中，選取選項。
23. 選取 **新增**。
24. 在 **主要會計科目** 欄位中，指定所需的值。
25. 選取 **儲存**。
26. 關閉頁面。
27. 在導覽窗格中，移至 **模組 > 專案管理與會計 > 設定 > 價格 > 轉撥價格**。
28. 選取 **新增**。
29. 在 **生效日期** 欄位中，輸入日期。
30. 在 **瀏覽法律實體** 欄位中，輸入或選取值。
31. 在 **轉撥價格模型** 欄位中，選取選項。
32. 在 **定價** 欄位中，輸入數字。
33. 選取 **儲存**。

