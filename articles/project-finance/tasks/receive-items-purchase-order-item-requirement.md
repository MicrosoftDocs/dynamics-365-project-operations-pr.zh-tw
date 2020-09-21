---
title: 從項目需求接收採購單上的項目
description: 本主題說明如何從項目需求接收採購單上的項目。
author: KimANelson
manager: AnnBe
ms.date: 08/06/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage, ProjTable, ProjSalesItemReq, InventItemIdLookupSimple, PurchCreateFromSalesOrder, VendAccountItemLookup, PurchTable, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.assetid: c61e3a5e-da3d-4f4c-87fa-03dea19f6936
ms.author: knelson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c5ed287aa24aff647ef1dc625f9e9f5f086ee662
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749850"
---
# <a name="receive-items-on-purchase-order-from-item-requirement"></a>從項目需求接收採購單上的項目

[!include [task guide banner](../../includes/task-guide-banner.md)]

本主題說明如何從項目需求接收採購單上的項目。

您可以使用項目需求 (而不是項目交易)，計劃好就在實際使用項目之前交貨、建立採購單、將項目納入交易合約架構中，以及將項目需求包含在生產規劃中。 

此工作會使用 USSI 資料集。

1. 在導覽窗格中，移至**模組 > 專案管理與會計 > 專案 > 所有專案**。
2. 在清單中，選取所需列中的連結。
3. 在動作窗格上，選取**計劃**。
4. 選取**項目需求**。
5. 選取**新增**。
6. 在新的列中，輸入或選取**項目編號**欄位中的值。
7. 在**數量**欄位中，輸入數字。
8. 選取**儲存**。
9. 在動作窗格上，選取**管理**。
10. 選取**函數**。
11. 選取**建立採購單**。
12. 選取**全部包含**核取方塊。
13. 在**供應商客戶**欄位中，輸入或選取值。
14. 選取**確定**。
15. 在導覽窗格中，移至**模組 > 應付帳款 > 採購單 > 所有採購單**。
16. 在清單中，選取所需列中的連結。
17. 在動作窗格上，選取**購買**。
18. 選取**確認**。
19. 在動作窗格上，選取**接收**。
20. 選取**產品收據**。
21. 在**產品收據**欄位中，輸入值。
22. 選取**確定**。

