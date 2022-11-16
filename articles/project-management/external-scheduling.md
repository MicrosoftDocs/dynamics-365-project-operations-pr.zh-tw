---
title: 外部排程
description: 本文提供外部排程的相關資訊。
author: ruhercul
ms.date: 10/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: ruhercul
ms.openlocfilehash: 746fb3a7c812b2b387ec707e58796d02d2473847
ms.sourcegitcommit: b1a5b9bb8b826678fc52f1d5a3d199a71caccb0a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 11/03/2022
ms.locfileid: "9736956"
---
# <a name="external-scheduling"></a>外部排程

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

外部排程模式讓您可以本機方式建立、更新和刪除與分工結構圖 (WBSs) 有關的實體，但不會遇到目前由 Microsoft Project for the Web 強制執行的限制。 它也提供有限的驗證。 此模式只能由下列客戶使用：

- 具有 Project Operations 所提供，在排程邏輯外定義 WBS 時所需之工具的客戶
- 必須管理排程階層、相關性或工作期間的客戶

> [!IMPORTANT]
> 非正確輸入在 WBS 相關實體中的資料，可能不會在資源協調網格、預估網格、追蹤網格或資源指派網格中呈現。

## <a name="configuration"></a>Configuration

此功能預設為啟用。 但是，在專案開箱即用的主頁面上，相關欄位預設為不可見。 若要啟用欄位，請在 Maker portal 中，打開專案實體的主頁面，選取 **排程引擎** 欄位，然後變更欄位為 **預設為可見**。 如果您不使用開箱即用的專案主頁面，請編輯現有的頁面，並新增 **排程引擎** 欄位。

## <a name="settings"></a>設定

若要使用外部排程模式，您必須先建立新專案，並在專案主頁面的下拉式清單中選取 **外部排程的** 排程引擎。 為專案設定好此模式後，便無法變更。

## <a name="viewing-the-wbs"></a>查看 WBS

如果專案是外部排程的，則會限制該專案存取 Project for the Web。 若要查看 WBS，您必須移至顯示完整 WBS 的追蹤網格。

## <a name="creating-and-editing-the-wbs"></a>建立和編輯 WBS

如果專案已啟用外部排程，您必須定義所有與 WBS 相關實體的資料 (包括工作、團隊成員、資源指派及相關性) 。

下圖顯示專案規劃的資料模型。

![專案規劃資料模型。](media/projectplanningdatamodel.png)

## <a name="functional-limitations"></a>功能限制

外部排程的專案不被允許進行下列作業。

### <a name="project-planning"></a>專案規劃

- **複製專案** – 外部排程的專案不支援此作業。
- **移動專案** – 專案開始日期的變更，將不會移動 WBS 中的工作或資源指派起始。
- **更新專案經理** – 變更專案主頁面上的專案經理，不會自動建立新專案團隊成員，需等到專案轉換後，才會進行。
- **更新專案的工時範本** – 變更專案的工時範本不會重新計算專案的排程。
- **資源指派分布** – 建立資源指派並不會自動更新 **mdyn \_PlannedWork** 欄位。 此欄位是用來儲存資源指派工作的分布。 如果您在資源指派網格或資源協調網格中顯示階段性工作，則您必須定義有效的資源指派分布。 這些分布必須可以正確格式化，才能同時觸發成本分布和銷售價格分布的計算。 我們建議您建立由 Project for the Web 排程的測試專案，然後檢視相關資料，以確認需求與格式設定。

### <a name="resource-management"></a>資源管理

- **一般資源履行** – 一般資源履行不支援外部排程的專案。 嘗試完成有效的開放需求將會建立新的專案團隊成員，但是不會刪除一般團隊成員，或是取代任何現有資源指派上的一般團隊成員。
- **刪除團隊成員** – 刪除團隊成員不會自動刪除資源指派。

### <a name="quoting-and-contracting"></a>報價和簽約

- **匯入報價行和合約行詳細資料** – 當報價或合約行詳細資料是從專案匯入時，該應用程式已經過測試，在每個工作以 20 個指派為限的基礎上，在 WBA 中最多僅支援 500 個工作。

### <a name="actuals-and-invoicing"></a>實際值與發票

- 雖然 WBS 與財務交易之間的現有驗證並無改變，但是您必須遵從開箱即用的資料模型，才能確保所有下游交易都如期執行。
