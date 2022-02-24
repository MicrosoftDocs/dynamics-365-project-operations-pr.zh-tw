---
title: 使用 OCR 擷取收據
description: 本主題提供有關使用光學字元辨識 (OCR) 處理收據的資訊。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: fd0cb0fb094260fa3e82d7a2f200f328a39dd7a1
ms.sourcegitcommit: f78087174a8512199a1bcbd7e8610bbc80e64801
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/04/2021
ms.locfileid: "5499841"
---
# <a name="capture-a-receipt-using-ocr"></a>使用 OCR 擷取收據

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

費用項目因採用光學字元辨識 (OCR) 處理收據而有所增強。 此功能是專為改善使用者建立費用報表時的體驗而設計。

## <a name="key-features"></a>主要功能

- 系統會從收據中擷取商家名稱、日期和總金額。
- 系統會嘗試將未附加的收據與未附加的費用交易進行比對。
- 您可以從收據建立手動輸入的費用交易。

## <a name="attach-receipts-to-an-expense-report"></a>將收據附加至費用報表

若要在建立費用報表時自動附加包含信用卡交易的收據，請完成下列步驟。

  1. 開啟 **費用管理** 工作區。
  2. 在 **收據** 索引標籤上，確認是否存在未附加的收據。 您也可以在 **收據** 索引標籤中上傳收據。
  3. 在 **費用** 索引標籤上，確認是否存在未附加的費用。 費用管理員通常會從信用卡提供者匯入這些費用。
  4. 選取 **新增費用報表**。 請注意，現在也可以在建立費用報表時，包含費用和收據。 如果同時新增費用和收據，就會觸發收據與費用的自動比對。

## <a name="create-or-match-receipts-to-an-expense-report"></a>建立或比對費用報表的收據
若要建立費用，或從收據中比對費用，請完成下列步驟。

  1. 在費用報表的 **收據** 索引標籤上，選取 **新增收據** 以附加收據。
  2. 在收據的已上傳影像下方，注意 **建立** 與 **比對** 選項。

      - 選取 **建立** 以建立手動輸入的費用交易，並填入從收據擷取的值。
      - 如果您選取 **比對**，系統就會嘗試將現有的費用與收據進行比對。

## <a name="installation"></a>安裝

若要使用這些進階費用功能，請安裝 Microsoft Dynamics 365 Finance 的費用管理服務增益集，並在您的執行個體中開啟這些功能。 您可以從 Microsoft Dynamics Lifecycle Services (LCS) 的專案中存取增益集。

1. 登入 LCS，並開啟所需的環境。
2. 移至 **完整詳細資料**。
3. 選取 **維護**，或向下捲動至 **環境增益集** 快速分頁。
4. 選取 **安裝新的增益集**。
5. 選取 **費用管理服務**。
6. 遵循安裝指南，並同意條款及條件。
7. 選取 **安裝**。

在 **功能管理** 工作區中，開啟下列功能：

- 重新設計的費用報表
- 自動比對並從收據建立費用

下列動作會在您開啟這些功能時發生：

- 現有的 **費用管理** 工作區會用新的工作區來取代。
- 新增費用欄位顯示性的新功能表項目。
- 您仍然可以開啟先前的 **費用報表** 頁面，方法是移至 **費用管理 > 我的費用 > 費用報表**。
- 工作流程和任何核准仍會帶您進入現有的費用報表頁面。
- 收據將會透過 Microsoft Azure Cognitive Services 進行處理，並擷取和新增中繼資料。
- 已新增選項，這個選項可讓您建立包含比對相符之未附加收據的費用報表。
- 新增至費用報表的選項會讓您從收據建立費用明細，或是會嘗試將現有收據與現有費用明細進行比對。

## <a name="frequently-asked-questions"></a>常見問題集

**Microsoft 是否會將我的資料用於其模型？**

否，Microsoft 已經建立其收據處理服務的一般機器學習模型。 此模型並非根據您上傳的收據所建立。

**什麼地方會提供並處理此功能？**

目前支援美國地區。

**我的收據哪裡去了？**

Finance 會連絡 Cognitive Services 來擷取欄位資料。 進行處理時，Cognitive Services 會保留您的收據複本最長 24 小時。 完成處理後，Cognitive Services 將會移除收據。 收據仍然儲存在 Finance 中。

如需詳細資訊，請參閱[使用表單辨識器的新功能來啟用收據瞭解](https://azure.microsoft.com/blog/enable-receipt-understanding-with-form-recognizer-s-new-capability/)。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
