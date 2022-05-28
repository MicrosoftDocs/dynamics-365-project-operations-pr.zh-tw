---
title: 設定內部專案會計
description: 本主題提供有關如何為 Project Operations 內部專案設定會計實務的資訊。
author: sigitac
ms.date: 10/09/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 9da72d8dbf720e380a49a1010caca472ee024783
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8597834"
---
# <a name="configure-accounting-for-internal-projects"></a>設定內部專案會計

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

內部專案可讓公司追蹤與免收客戶費用活動相關的成本。 內部專案的範例包括：

- 開發產品 (例如行動應用程式)，以及追蹤與開發相關聯的成本。
- 管理售前時間與費用。 如果報價已成交，則可以稍後再將此售前內部專案轉換成計費專案。

任何未與 Dynamics 365 Project Operations 中合約建立關聯的專案都會視為內部專案。 專案成本與營收設定檔不會用來決定專案的會計規則。 內部專案成本一律使用損益原則進行過帳。 用於過帳的總帳科目是在 **總帳過帳設定** 頁面上定義。

- 時間交易的過帳方式是，借記 **成本** 科目，並貸記 **薪資分攤** 科目。
- 費用交易的過帳方式是，借記 **成本** 科目，並貸記 **費用抵銷科目**。
- 項目交易是透過借記 **成本** 科目和貸記 **成本項目** 科目來過帳。

將交易過帳到專案之後，如果專案與專案合約相關聯，則系統會沖銷所有累計交易，並建立新的計費交易。 計費交易遵循各自定義於專案成本與營收設定檔的會計規則。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
