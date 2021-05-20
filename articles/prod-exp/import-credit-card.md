---
title: 匯入和維護信用卡交易
description: 本主題說明如何匯入和維護費用相關信用卡交易。 您可以設定這些交易，讓交易按照週期性排程自動進行匯入，也可以在需要時手動匯入這些交易。
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951064"
---
# <a name="import-and-maintain-credit-card-transactions"></a>匯入和維護信用卡交易

您可以設定費用相關信用卡交易，以便按照定期排程自動匯入這些交易。 或者，也可以在需要時手動匯入交易。 信用卡交易會透過信用卡交易資料實體進行匯入。

如需資料實體的詳細資訊，請參閱[資料實體](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities)。

## <a name="import-credit-card-transactions"></a>匯入信用卡交易

1. 在 **信用卡交易** 頁面上，選取 **匯入交易**。 如果您是第一次開啟資料管理，則系統必須先更新資料實體的清單，您才能繼續進行。
2. 在 **名稱** 方塊中，輸入匯入工作的唯一名稱。
3. 在 **來源資料格式** 欄位中，選取包含要匯入之信用卡交易的檔案格式。
4. 選取 **上傳**，然後尋找並選取要匯入的檔案。
5. 上傳檔案之後，選取圖標上的 **檢視對應** 連結，以驗證信用卡交易檔案與信用卡交易資料實體欄的對應。 如果發生對應錯誤，或者您必須變更對應時，請從 **對應視覺化效果** 索引標籤或 **對應詳細資料** 索引標籤中進行對應變更。
6. 若要將信用卡交易自動化，請選取 **建立定期資料作業**。 您可以接著設定可定義多久匯入一次信用卡交易的週期。 設定完畢後，選取 **確定**。
7. 若要立即匯入選取的檔案，請選取 **匯入**。
8. 如果匯入時發生錯誤，您可以檢視執行記錄檔或暫存資料，了解必須修正的錯誤以確保成功匯入。

> [!NOTE]
> 如果您必須匯入多個檔案格式，則必須為每個格式類型建立不同的匯入工作。

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a>重新指派離職員工的信用卡交易

員工記錄終止後，即會停用該員工的 Active Directory Domain Services (AD DS) 帳戶。 不過，可能會有仍須認列為費用和進行報銷的有效信用卡交易。 您可以從 **信用卡交易** 頁面中，為任何有相關員工已離職的信用卡交易重新指派員工。

選取一個或多個信用卡交易，然後選取 **重新指派交易**。 您可以接著選取其他員工，將信用卡交易指派給他。 重新指派信用卡交易之後，就可以選取這些交易以列入費用報表，並透過通常的費用報表報銷程序來支付。


[!INCLUDE[footer-include](../includes/footer-banner.md)]