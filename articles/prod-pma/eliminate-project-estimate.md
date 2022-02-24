---
title: 銷除專案估計值
description: 本主題提供有關完成專案估計後銷除其估計值的資訊。
author: Yowelle
manager: AnnBe
ms.date: 05/26/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 000eabdac41f30a6e7dd37e34b8fd91d7c51f6c4
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5270668"
---
# <a name="eliminate-a-project-estimate"></a>銷除專案估計值

[!include [banner](../includes/banner.md)]

專案預估值為專案中預估與排定的作業提供財務檢視表。 若要使用專案的估計值，您必須將專案附加至估計專案。 估計專案永遠都是根據現有的專案來建立，但是多個專案可以參考單一估計專案。 只有固定價格和投資專案可以附加至估計專案，而且這些專案與估計專案同屬於一個專案群組。

若要銷除估計專案，此專案必須已完成。 下列步驟說明如何銷除估計值。

1. 移至 **專案管理與會計** > **所有專案**，然後開啟專案。 
2. 在 **管理** 索引標籤上，選取 **估計值**，然後在 **估計值** 頁面選取 **銷除**。
3. 在 **銷除估計值** 頁面的 **一般** 索引標籤上，設定下列選項：

   - **期間代碼**：選取期間代碼以選擇適當的估計專案。 
   - **估計日期**：選取適當的估計日期以進行銷除。
   - **銷除但顯示 WIP 警告**：啟用此選項可在銷除與進行中工作 (WIP) 相關的估計值時，提供通知。 未啟用此選項時，如果有任何非估計交易，則無法繼續進行銷除。 
   > [!NOTE]
   > 只有在銷除是套用至估計專案時，才能使用此選項。 如果您使用定期過帳，則無法使用此選項。 此設定可在 **非估計交易存在時允許銷除** 欄位群組中，與 **專案參數** 頁面的 **估計值** 索引標籤上的設定搭配使用。
   - **將階段設定為已完成**：啟用此選項可在執行銷除後，將估計專案的階段設定為 **已完成**。
   - **列印估計值清單**：選取列印估計值清單時要包含的資訊。
   - **顯示資訊日誌**：啟用此選項以顯示資訊日誌。
   - **過帳日期**：選擇估計值的總帳過帳日期。

4.  選取 **確定**。
5. 銷除程序完成之後，會以負值顯示已銷除的估計專案。 

如果您無意銷除估計值，則可以選取已銷除的估計值，並選取 **反轉銷除**。   


[!INCLUDE[footer-include](../includes/footer-banner.md)]