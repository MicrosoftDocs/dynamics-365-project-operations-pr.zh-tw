---
title: 建立手動預估發票 - 精簡
description: 本主題提供有關在 Project Operations 中建立手動預估發票的資訊。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 104c2f3f7f0ca0682158d0f7fa0f50a4967e6dd0
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274178"
---
# <a name="create-a-manual-proforma-invoice---lite"></a>建立手動預估發票 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_

在 Dynamics 365 Project Operations 中，您可以視需要手動建立預估發票。 您可以從 **專案合約** 清單頁面，或從 **專案合約** 詳細資料頁面手動建立預估發票。

##  <a name="project-contracts-list-page"></a>專案合約清單頁面

從 **專案合約** 清單頁面中，選取一個或多個專案合約，並為所有已選取的記錄建立發票。

系統會進行檢查，以了解哪些所選專案合約的 **已準備好開立發票** 待處理項目日期是在今天之前。 系統會從這些合約建立草稿預估發票。 如果專案合約有多個客戶，則可能會每個客戶建立一張發票，以及每個專案合約建立多張發票。

所有已建立的專案發票都可以在 **銷售** 區域 **帳單** 區段的 **發票** 頁面上找到。

## <a name="project-contract-details-page"></a>專案合約詳細資料頁面

您也可以從 **專案合約** 詳細資料頁面建立預估發票 。 系統會確認專案合約的 **已準備好開立發票** 待處理項目日期是否在今天之前。 系統會從這些合約，根據每個合約服務內容的客戶數目建立草稿預估發票。

當有已建立的單一預估發票時，**發票** 頁面會開啟。 如果該專案合約已建立多份發票，則 **發票** 清單頁面會開啟，以顯示所有的已建立發票。


[!INCLUDE[footer-include](../../includes/footer-banner.md)]