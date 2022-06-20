---
title: 排程模式
description: 本文提供排程模式的相關資訊。
author: ruhercul
ms.date: 05/28/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 3cbe14f8d458c5d9631e0595912afa8cbb87b9de
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8923638"
---
# <a name="scheduling-modes"></a>排程模式

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_


Dynamics 365 Project Operations 可讓組織定義他們如何在分工結構圖中管理工作中重要變數的變更。 根據組織的特定需求，專案經理可在建立專案時變更排程模式。

Project Operations 中有三種可用的排程模式：

  - 固定期間 (這是預設模式)
  - 固定投入量 (*工作*)
  - 固定單位

受特定排程模式定義影響的值是由下列公式所決定：

  投入量 = 期間 x 單位

當您定義專案的排程模式時，即是在設定這其中一個值，而這些值隨後就無法變更。 將此值保留為常數會將該值置於優先位置，通知系統不要在其他兩個值變更時變更此值。 下表提供有關選取特定模式所造成影響的資訊。

| **在此工作中**             | **如果您修訂單位數**   | **如果您修訂期間** | **如果您修訂投入量**  |
|----------------------|---------------------------|----------------------------|---------------------------|
| 固定單位工作     | 重新計算期間。 | 重新計算投入量。    | 重新計算期間。 |
| 固定投入量工作    | 重新計算期間。 | 重新計算單位。    | 重新計算期間。 |
| 固定期間工作  | 重新計算投入量。   | 重新計算投入量。    | 重新計算單位。   |

如需指定模式隱含意義的詳細資訊，請參閱[變更工作類型以取得更準確的排程](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72)。 文章中的用語是 **工作** 而不是 **投入量**。

## <a name="change-the-organizations-scheduling-mode"></a>變更組織的排程模式

完成下列步驟，以定義組織的排程模式。

1. 移至 **設定** \> **一般** \> **參數**，然後選取專案參數。 
2. 在 **專案參數** 頁面上，選取組織的預設排程模式，然後定義專案經理可在建立新專案時覆寫設定的能力。

## <a name="change-the-scheduling-mode-setting-on-a-project"></a>變更專案的排程模式設定

如果組織允許專案經理覆寫預設排程模式，則專案經理可在建立新專案時進行該變更。 不過，儲存專案之後，就無法變更排程模式。

## <a name="copied-projects"></a>複製的專案

由於專案是在執行複製專案動作時所建立，因此專案經理無法設定排程模式。 目的地專案永遠預設為組織層級定義的模式。

## <a name="copied-tasks"></a>複製的工作

將工作從一個專案複製到另一個時，工作會繼承目的地專案的排程模式。
