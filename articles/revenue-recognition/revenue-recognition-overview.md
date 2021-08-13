---
title: 收入認列概觀
description: 本主題提供 Project Operations 中收入認列的資訊。
author: sigitac
ms.date: 11/16/2020
ms.topic: article
ms.reviewer: kfend
ms.author: sigitac
ms.custom: intro-internal
ms.openlocfilehash: 3d2fcf434a5086595e40f50afc2366eb806168085ae9212b5d25e3e9bd02e2c6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6988641"
---
# <a name="revenue-recognition-overview"></a>收入認列概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

在 Dynamics 365 Project Operations 中，收入認列原則會根據專案或專案的一部分所選取的帳務方式而有所不同。 本主題提供 Project Operations 中收入認列的資訊。

## <a name="transactions-accounted-using-time-and-material-billing-method"></a>使用時間和資料帳務方式記帳的交易

- 成本和收入認列是關聯的。 交易成本與未開單銷售使用 [Project Operations 整合帳目](../project-accounting/project-operations-integration-journal.md)過帳。
- 專案成本和營收設定檔判斷未開單銷售交易記錄是否已過帳至總帳。 如果已選取 **應計營收**，系統會在過帳期間使用 **WIP 銷售值** 和 **應計收入銷售值** 科目。 以下是此方法的範例。  

  | 交易類型 | 轉帳卡/信用卡 | 總數 |
  | --- | --- | --- |
  | WIP 銷售值 | 轉帳卡 | 100 |
  | 應計收入銷售值 | 信用卡 | 100 |

- 開立發票時認列收入。 在過帳期間，系統使用 **已開立發票營收** 科目。 以下是此方法的範例。  

  | 交易類型 | 轉帳卡/信用卡 | 總數 |
  | --- | --- | --- |
  | 客戶餘額 | 轉帳卡 | 120 |
  | 應付銷售稅 | 信用卡 | 20 |
  | 已開發票營收 | 信用卡 | 100 |

- 如果在過帳未開單銷售時營收已累計，系統將在開立發票時沖銷應計收入。

  | 交易類型 | 轉帳卡/信用卡 | 總數 |
  | --- | --- | --- |
  | WIP 銷售值 | 信用卡 | 100 |
  | 應計收入銷售值 | 轉帳卡 | 100 |

## <a name="transactions-accounted-using-the-fixed-price-billing-method"></a>使用固定價格帳務方式記帳的交易

- 成本和收入認列是分開的。 交易成本使用 [Project Operations 整合帳目](../project-accounting/project-operations-integration-journal.md)過帳。 不會建立未開單銷售交易。
- 如果專案成本和收入設定檔將 **用於專案完成計算的原則** 設定為 **無 WIP**，則可在開立發票時認列收入。 只將此方法用於短期、簡單專案。
- 可以使用固定價格營收預估值來認列收入（使用 **全部完工法** 或 **完成百分比營收認列** 方法）。

## <a name="additional-resources"></a>其他資源
[設定計費專案會計文章](../project-accounting/configure-accounting-billable-projects.md)

[固定價格營收估計專案](rev-rec-percentage-completion-method.md)

[管理營收預估值](rev-rec-completed-contract-method.md)

[完工成本法](cost-complete-methods.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]