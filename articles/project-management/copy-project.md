---
title: 複製專案
description: 本主題提供有關在 Dynamics 365 Project Operations 中複製專案的資訊。
author: ruhercul
manager: AnnBe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 53c72e5fd680eb28128644788752368705440445
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131783"
---
# <a name="copy-a-project"></a>複製專案

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

有了 Dynamics 365 Project Operations，您就可以選取 **專案** 表單上的 **複製專案** 快速建置新的專案。 若要複製專案，請開啟想要複製的專案，然後選取 **複製專案**。 此動作會複製：

- 專案屬性
- 分工結構圖
- 專案團隊成員
- 專案估計值
- 專案費用估計

## <a name="project-properties"></a>專案屬性

複製專案時，會複製下列欄位中的值：

- 名字
- 描述
- 客戶
- 行事曆範本
- 貨幣
- 合約單位
- 專案經理
- Status
- 整體專案狀態
- 註解
- 估計值
- 估計開始日期
- 完成日期
- 投入 (小時)
- 估計人力成本
- 估計費用成本

## <a name="work-breakdown-structure"></a>分工結構圖

複製專案時，會複製整個資源載入的分工結構圖。 具名資源會以一般資源來取代。 如果具名資源的工作時數與一般資源的不同，則會重新計算排程，而且工作期間可能會變更。

## <a name="project-team-members"></a>專案團隊成員

從來源專案複製專案團隊時，會複製一般資源。 一般資源指派也會保持與原先在來源專案中的一樣。 具名資源將會轉換為一般團隊成員。

## <a name="estimates"></a>估計值

複製專案時，會從來源專案複製資源及費用估計明細。 

如需有關如何以程式設計方式存取 [複製專案] 的詳細資訊，請參閱[使用 [複製專案] 開發專案範本](dev-copy-project.md)。
