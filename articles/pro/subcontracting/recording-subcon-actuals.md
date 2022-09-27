---
title: 記錄已轉包元件的時間、費用及材料使用方式
description: 本文說明 Microsoft Dynamics 365 Project Operations 如何追蹤已轉包元件的專案上所記錄的時間、費用及材料使用方式。
author: rumant
ms.date: 09/14/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b82c14412cfb0405040902a2329c3b6692422d89
ms.sourcegitcommit: 08eb3be9eda44e9446c43ed9b6aefd58d77927c5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/15/2022
ms.locfileid: "9522503"
---
# <a name="recording-time-expenses-and-material-usage-on-projects-for-subcontracted-components"></a>在已轉包元件的專案上記錄時間、費用及材料使用方式

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

本文說明 Microsoft Dynamics 365 Project Operations 如何追蹤已轉包元件的專案上所記錄的時間、費用及材料使用方式。

## <a name="costing-for-subcontractor-time-on-projects"></a>計算專案的轉包商時間成本
在 Project Operations 中，合約工作者可以當做員工，以類似的方式來記錄專案的時間。 在專案和/或專案工作上輸入時間時，合約工作者可以選取特定的轉包合約和轉包合約服務內容。

當合約工作者所提交的時間獲核准時，將會使用針對該合約工作者資源在轉包合約之採購價目表的 **角色價格** 區段中所設定的單位成本費率來記錄專案成本。

## <a name="costing-for-subcontracted-expenses-on-projects"></a>計算專案已轉包費用的成本
輸入專案所產生的費用時，您可以在費用項目上選取轉包合約和轉包合約服務內容。 

當此費用項目經提交且獲核准時，將會根據針對該交易類別在轉包合約之採購價目表的 **類別價格** 區段中所設定的單位成本，將費用成本記錄在專案上。

## <a name="costing-for-subcontracted-materials-on-projects"></a>計算專案已轉包材料的成本
輸入專案的材料使用方式時，您可以在材料使用記錄上選取轉包合約和轉包合約服務內容。 當材料使用記錄經提交且獲核准時，將會根據針對該交易類別在轉包合約之採購價目表的 **類別價格** 區段中所設定的單位成本，將材料成本記錄在專案上。

也可以在專案上記錄目錄外產品的材料使用方式。 這種類型的材料使用方式也可以連結至轉包合約和轉包合約服務內容。 記錄目錄外產品的材料使用方式時，您需要輸入目錄外產品的的單位成本。 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
