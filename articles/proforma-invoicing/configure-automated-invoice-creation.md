---
title: 設定自動發票建立作業
description: 本主題提供有關如何將系統設定成自動產生發票的資訊。
author: rumant
ms.date: 10/13/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: dffa95c163f7f8d5074e02cd56d6f1ed429a7c72
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6005331"
---
# <a name="configure-automatic-invoice-creation"></a>設定自動發票建立作業

_**適用於：** 資源/非庫存型案例適用的 Project Operations_


完成下列步驟，在 Dynamics 365 Project Operations 中設定自動化發票執行。

1. 移至 **設定** > **批次工作**。
2. 建立批次工作，並將其命名為 **Project Operations 建立發票**。 批次工作的名稱必須包含「建立發票」一詞。
3. 在 **工作類型** 欄位中，選取 **無**。 **每日頻率** 和 **使用中** 選項預設會設定為 **是**。
4. 選取 **執行工作流程**。 在 **查詢記錄** 對話方塊中，您會看到三個工作流程：

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. 選取 **ProcessRunCaller**，然後選取 **新增**。
6. 在下一個對話方塊中選取 **確定**。 **睡眠** 工作流程後面會跟著 **程序** 工作流程。

  > [!NOTE]
  > 您也可以選取步驟 5 中的 **ProcessRunner**。 然後，當您選取 **確定** 時，**程序** 工作流程後面會接著 **睡眠** 工作流程。

**ProcessRunCaller** 和 **ProcessRunner** 工作流程會建立發票。 **ProcessRunCaller** 會呼叫 **ProcessRunner**。 **ProcessRunner** 是實際建立發票的工作流程。 它會處理所有需要建立發票的合約服務內容，然後為這些服務內容建立發票。 為了確定必須建立其發票的合約服務內容，工作會查看合約服務內容的發票執行日期。 如果屬於一個合約的合約服務內容具有相同的發票執行日期，則會將交易合併成一個有兩個發票明細的發票。 如果沒有要要建立其發票的交易，則工作會跳過發票建立作業。

**ProcessRunner** 執行完畢後，會呼叫 **ProcessRunCaller**、提供結束時間，然後關閉。 **ProcessRunCaller** 接著啟動計時器，從指定的結束時間開始執行 24 小時。 計時器結束時，會關閉 **ProcessRunCaller**。

用於建立發票的批次處理工作是週期性工作。 如果此批次處理已執行多次，就會建立工作的多個執行個體，並造成錯誤。 因此，您只能啟動批次處理一次，並且只有在其停止執行時才要重新啟動此工作。

> [!NOTE]
> 批次開立發票只會對發票排程所設定的專案合約服務內容來執行。 使用固定價格計費方式的合約服務內容必須已設定里程碑。 使用時間和材料計費方式的專案合約服務內容必須設定以日期為依據的發票排程。 這同樣適用於專案型合約服務內容。     


[!INCLUDE[footer-include](../includes/footer-banner.md)]