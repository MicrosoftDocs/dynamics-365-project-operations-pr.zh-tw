---
title: 使用待處理廠商發票來購買非庫存材料或採購類別
description: 本主題說明如何記錄待處理廠商發票。
author: sigitac
ms.date: 09/13/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: e81f7a54e304ae6fc9a9f2637124579b6e7b54e9
ms.sourcegitcommit: 9916f536a71b6a0078297402564ac79308ec6890
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/18/2022
ms.locfileid: "8612647"
---
# <a name="purchase-non-stocked-materials-or-procurement-categories-using-a-pending-vendor-invoice"></a>使用待處理廠商發票來購買非庫存材料或採購類別

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

當公司採購專案的非庫存材料或採購類別時，可立即將成本記錄在專案上。 

例如，Contoso Robotics US 正在進行設備更新專案，需要軟體授權。 這些授權是從協力廠商所採購。  使用 Dynamics 365 Finance 時，應付帳款職員會記錄待處理廠商發票單據，並將授權成本直接劃歸到設備更新專案上。 

> [!IMPORTANT]
> 使用本主題中所述的功能之前，請先檢閱並套用必要的設定。 如需詳細資訊，請參閱[啟用非庫存材料和待處理廠商發票](configure-materials-nonstocked.md)和[將採購類別與專案採購單及待處理廠商發票搭配使用](configure-procurement-categories.md)

## <a name="post-a-project-related-pending-vendor-invoice"></a>過帳專案相關的待處理廠商發票 

待處理廠商發票可以記錄在 **待處理廠商發票** 頁面上 (**應付帳款** > **發票** > **待處理廠商發票**)。 完成下列步驟，以過帳專案相關的待處理廠商發票：

1. 移至 **應付帳款** > **發票**，然後選取 **新增**。 
1. 在 **發票帳戶** 欄位中，選取廠商，然後在 **編號** 欄位中輸入廠商發票識別碼。
1. 將一項明細新增至廠商發票，然後在 **項目編號** 欄位中，選取從廠商購買的非庫存材料。 或者，在 **採購類別** 欄位中，選取從廠商購買的採購類別。   
1. 新增已購買的數量。 系統會根據非庫存材料價格設定填入單價。 
1. 確認該行明細上的總計金額及其他必要詳細資料。
1. 在明細詳細資料的 **專案** 索引標籤上，選取此項目要記錄到的專案的識別碼。
1. 選擇性：選取活動編號，並更新專案類別和明細屬性。
1. 過帳待處理廠商發票。 過帳此發票時，系統會記錄下列資訊：
    
    - 廠商結餘金額。
    - 銷售稅金額。
    - 將專案帳上的成本記錄至採購整合科目。
    - Dataverse 中的專案實際成本交易。  使用 [Project Operations 整合帳目](../project-accounting/project-operations-integration-journal.md)進一步處理此交易。 過帳此帳目會將採購整合科目中的金額轉入專案成本科目。 
    - 使用時間和材料帳務方式向專案客戶收費的購買項目。 此外，還會在 Dataverse 中為購買項目建立未開單銷售交易。 Dataverse 中的產品價目表會用於未開單銷售交易的售價及金額。
