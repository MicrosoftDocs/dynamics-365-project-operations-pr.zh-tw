---
title: 專案發票整合
description: 本主題提供有關用於開立客戶發票之 Project Operations 雙重寫入整合的資訊。
author: sigitac
ms.date: 04/26/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 1e7294360f041b030efca225c6754fe3bbc0eadf
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581228"
---
# <a name="project-invoice-integration"></a>專案發票整合

本主題提供有關用於開立客戶發票之 Project Operations 雙重寫入整合的資訊。

在 Project Operations 中，專案經理會管理專案帳務積存，並在 Microsoft Dataverse 中為客戶建立預估發票。 應收帳款記帳員或專案會計師會根據此預估發票，建立客戶面向發票。 雙重寫入整合可確保預估發票詳細資料會同步處理至財務和營運應用程式。 將客戶面向發票過帳之後，系統 會根據會計詳細資料更新 Dataverse 中的相關專案實際值。 下圖提供此項整合的高階概念概觀。

   ![專案發票整合。](./media/DW5Invoicing.png)

專案經理在 Dataverse 中確認預估發票之後，會使用雙重寫入資料表對應 **專案發票提案 V2 (發票)** 將預估發票標題資訊同步處理至財務和營運應用程式。 這是從 Dataverse 到財務和營運應用程式的單向整合。 不支援直接在財務和營運應用程式中建立或刪除專案發票提案。

Dataverse 中的發票確認還會觸發商務規則，在 **實際值** 實體中建立帳務相關記錄。 這些記錄是使用雙重寫入資料表對應 **Project Operations 整合實際值 (msdyn\_actuals)** 來同步處理至 Finance and Operations。 如需詳細資訊，請參閱[專案估計值和實際值](resource-dual-write-estimates-actuals.md)。 

專案發票提案明細是由定期程序 **從臨時表格匯入** 所建立。 此程序是根據 **實際值臨時表格** 資料表中的已開單銷售實際值詳細資料來執行。 如需詳細資訊，請參閱[管理專案發票提案](../invoicing/format-update-project-invoice-proposals.md#create-project-invoice-proposals)。 
