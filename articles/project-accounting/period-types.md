---
title: 期間類型
description: 此主題提供有關如何設定營收估計的期間類型的資訊。
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 07cc9cde5fab10accb1fd6efede58926918f614c
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6013476"
---
# <a name="period-types"></a>期間類型

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

期間類型定義了估計專案營收的頻率。 此主題提供有關如何設定營收估計的期間類型的資訊。 

## <a name="create-and-work-with-period-types"></a>建立與使用期間類型
若要建立和使用期間類型，請完成下列步驟：

1. 在您的 Dynamics 365 Finance 環境中，移至 **專案管理和會計** > **設定** > **估計值** > **期間類型**。
2. 選取 **新增** 以建立新的期間類型。 輸入名稱和描述。
3. 在 **頻率** 欄位中選取值：

    - 如果您選取 **週**、**兩週**、**半月**、**月**、**日**、**季** 或 **年**，就會使用行事曆來產生期間。 
    - 如果您選取 **分類帳期間**，則會使用總帳設定中的分類帳期間來產生期間。
    - 如果您選取 **無限制**，則可以指定自訂期間。
4. 選取期間類型記錄，然後選取 **產生期間**，以建立期間類型的期間。 根據您所選取的期間頻率，您可以選擇指定開始日期或要產生的期間數。
5. 選取 **期間** 以檢閱產生的期間。



[!INCLUDE[footer-include](../includes/footer-banner.md)]