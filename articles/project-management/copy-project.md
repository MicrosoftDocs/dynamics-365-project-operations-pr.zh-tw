---
title: 複製專案
description: 本主題提供有關在 Dynamics 365 Project Operations 中複製專案的資訊。
author: ruhercul
ms.date: 03/07/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: e9b637d2d282d123dfacb8a295292ea06549aa1e
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8574420"
---
# <a name="copy-a-project"></a>複製專案

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

在 Dynamics 365 Project Operations 中，您可以選取 **專案** 表單上的 **複製專案**，快速建置新專案。 若要複製專案，請開啟想要複製的專案，然後選取 **複製專案**。 此動作會複製下列項目：

- 專案屬性 
- 分工結構圖
- 專案團隊成員
- 專案估計值
- 專案費用估計
- 專案材料估計值
- 專案檢查清單
- 專案貯體

## <a name="project-properties"></a>專案屬性

複製專案時，會複製下列欄位中的值。

| 欄位 | Project Operations 非庫存材料 | Project Operations Lite | Project for the Web |
|-------|------------------------------------------|-------------------------|---------------------|
| 姓名 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| 名稱 | :heavy_check_mark: | :heavy_check_mark: | |
| 客戶 | :heavy_check_mark: | :heavy_check_mark: | |
| 行事曆範本 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| 貨幣 | :heavy_check_mark: | :heavy_check_mark: | |
| 合約單位 | :heavy_check_mark: | :heavy_check_mark: | |
| 負責公司 | :heavy_check_mark: | | |
| 專案經理 | :heavy_check_mark: | :heavy_check_mark: | :heavy_check_mark: |
| 執行狀態 | :heavy_check_mark: | :heavy_check_mark: | |
| 整體專案狀態 | :heavy_check_mark: | :heavy_check_mark: | |
| 意見 | :heavy_check_mark: | :heavy_check_mark: | |
| 估計值 | :heavy_check_mark: | :heavy_check_mark: | |
| <p>估計開始日期</p><p><strong>注意：</strong>此欄位指定從複本建立專案的日期。 | :heavy_check_mark: | :heavy_check_mark: | |
| <p>預計完成日期</p><p><strong>注意：</strong>此欄位中的日期是根據從複本所建立之新專案的開始日期進行調整。</p> | :heavy_check_mark: | :heavy_check_mark: | |
| 投入 (小時) | :heavy_check_mark: | :heavy_check_mark: | |
| 估計人力成本 | :heavy_check_mark: | :heavy_check_mark: | |
| 估計費用成本 | :heavy_check_mark: | :heavy_check_mark: | |
| 估計材料成本 | | :heavy_check_mark: | |

> [!NOTE]
> 複製專案是長時間執行的作業。 也會複製專案記錄、其相關屬性以及許多相關實體。 由於作業執行時間很長，因此開始複製後，除非複製作業完成，否則會一直鎖定目標專案頁面，無法進行編輯。

## <a name="work-breakdown-structure"></a>分工結構圖

複製專案時，會複製整個資源載入的分工結構圖。 具名資源會以一般資源來取代。 如果具名資源與一般資源的工作時數不同，則會重新計算排程，而工作期間可能會變更。

## <a name="project-team-members"></a>專案團隊成員

從來源專案複製專案團隊時，會複製一般資源。 一般資源指派也會保持與原先在來源專案中的一樣。 具名資源將會轉換為一般團隊成員。

> [!NOTE]
> 不會在 Project for the Web 中複製團隊成員和指派。

## <a name="estimates"></a>估計值

複製專案時，會從來源專案複製資源、費用及材料估計明細。 

如需有關如何以程式設計方式存取 [複製專案] 的詳細資訊，請參閱[使用 [複製專案] 開發專案範本](dev-copy-project.md)。

## <a name="quotes-and-contracts"></a>報價和合約

報價和合約未連結至目的地專案。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
