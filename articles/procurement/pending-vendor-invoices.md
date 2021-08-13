---
title: 使用待處理廠商發票購買非庫存材料
description: 本主題說明如何記錄待處理廠商發票。
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 2ce9f244eaa549742aeb55024ca9ef4d82cde1bd4a5b9c7f8c762cf72e0da83f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "7009026"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a>使用待處理廠商發票購買非庫存材料

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

公司採購專案的非庫存材料時，系統會立即將此記錄至專案的成本。 

例如，Contoso Robotics US 正在執行設備更新專案，並需要軟體授權。 這些授權是從協力廠商所採購。  應付帳款記帳員會使用 Dynamics 365 Finance 來記錄待處理廠商發票單據，並將授權成本直接歸入設備更新專案。 

> [!IMPORTANT]
> 使用本主題中所述的功能之前，請先檢閱並套用必要的設定。 如需詳細資訊，請參閱[啟用非庫存材料和待處理廠商發票](configure-materials-nonstocked.md)。 

## <a name="post-a-project-related-pending-vendor-invoice"></a>過帳專案相關的待處理廠商發票 

待處理廠商發票可以記錄在 **待處理廠商發票** 頁面上 (**應付帳款** > **發票** > **待處理廠商發票**)。 完成下列步驟，以過帳專案相關的待處理廠商發票：

1. 移至 **應付帳款** > **發票**，並選取 **新增**。 
2. 在 **發票科目** 欄位中，選取廠商，然後在 **編號** 欄位中輸入廠商發票識別碼。
3. 將一行明細新增至廠商發票，然後在 **項目編號** 欄位中，選取從廠商所購買的非庫存項目。 

    > [!NOTE]
    > 以採購類別為依據的廠商發票明細無法記錄在專案的帳上。 
    
5. 新增購買的數量。 系統會根據非庫存項目價格設定來填入單價。 
6. 確認該行明細上的總計金額及其他必要詳細資料。
7. 在明細詳細資料的 **專案** 索引標籤上，選取將此項目記錄至其帳上之專案的識別碼。
8. 或者，選取活動編號，並更新專案類別和明細屬性。
9. 過帳待處理廠商發票。 將發票過帳時，系統會記錄：
    
    - 廠商結餘金額。
    - 銷售稅金額。
    - 將專案帳上的成本記錄至採購整合科目。
    - Dataverse 中的專案實際交易。 使用 [Project Operations 整合帳目](../project-accounting/project-operations-integration-journal.md)進一步處理此交易。 過帳此帳目會將採購整合科目中的金額轉入專案成本科目。
