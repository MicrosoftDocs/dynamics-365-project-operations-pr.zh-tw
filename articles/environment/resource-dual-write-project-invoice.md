---
title: 專案發票整合
description: 本主題提供有關用於開立客戶發票之 Project Operations 雙重寫入整合的資訊。
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7407c98aad79806dcbaf25e81ff3e08397b41ffe
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996556"
---
# <a name="project-invoice-integration"></a>專案發票整合

本主題提供有關用於開立客戶發票之 Project Operations 雙重寫入整合的資訊。

在 Project Operations 中，專案經理會管理專案帳務積存，並在 Microsoft Dataverse 中為客戶建立預估發票。 應收帳款記帳員或專案會計師會根據此預估發票，建立客戶面向發票。 雙重寫入整合可確保將預估發票詳細資料同步處理至 Finance and Operations 應用程式。 將客戶面向發票過帳之後，系統 會根據會計詳細資料更新 Dataverse 中的相關專案實際值。 下圖提供此項整合的高階概念概觀。

   ![專案發票整合](./media/DW5Invoicing.png)

專案經理在 Dataverse 中確認預估發票之後，預估發票標題資訊會使用雙重寫入資料表對應 **專案發票提案 V2 (發票)** 同步處理至 Finance and Operations 應用程式。 這是從 Dataverse 到 Finance and Operations 應用程式的單向整合。 不支援直接在 Finance and Operations 應用程式中建立或刪除專案發票提案。

Dataverse 中的發票確認還會觸發商務規則，在 **實際值** 實體中建立帳務相關記錄。 這些記錄是使用雙重寫入資料表對應 **Project Operations 整合實際值 (msdyn\_actuals)** 同步處理至 Finance and Operations。 如需詳細資訊，請參閱[專案估計值和實際值](resource-dual-write-estimates-actuals.md)。 

專案發票提案明細是由定期程序 **從臨時表格匯入** 所建立。 此程序是根據 **實際值臨時表格** 資料表中的已開單銷售實際值詳細資料來執行。 如需詳細資訊，請參閱[管理專案發票提案](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)。 
