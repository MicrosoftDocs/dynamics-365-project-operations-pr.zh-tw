---
title: 轉包合約的狀態轉換
description: 本文說明在 Microsoft Dynamics 365 Project Operations 中建立、執行和關閉轉包合約時，該轉包合約上發生的狀態轉換。
author: rumant
ms.date: 12/03/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: b41e3d44a17c51778dd850c7d4a48351a5d44554
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8919728"
---
# <a name="state-transitions-on-a-subcontract"></a>轉包合約的狀態轉換 

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

本文說明 Microsoft Dynamics 365 Project Operations 中轉包合約的狀態轉換。 個別狀態會表示為草稿、已確認、已關閉或已取消。 下列影像表示狀態轉換。

![轉包合約狀態模型](../media/SubconStates.png)  

下表提供轉包合約生命週期的每個狀態在 Project Operations 中所代表之意義的描述。

| 州/省 | Description | 允許的轉換 |
| --- | --- | --- |
| 草稿 | 這表示轉包合約的初始狀態。 與廠商的交涉正在進行中。 這些服務內容和定價可能會有所修改。 此狀態下的轉包合約可以用來估計專案對資源和材料的需求並為此需求配置人員。 還可以在專案的時間、費用和材料使用方式中參考該轉包合約。 您可以編輯並刪除處於此狀態的轉包合約。 | 已確認 |
| 已確認 | 這表示轉包合約在與廠商就所要購買之定價及服務內容項目進行交涉後的階段已完成。 不過，已轉包資源實際的材料和/或工作交付仍在進行中。 此狀態下的轉包合約可以用來估計專案對資源和材料的需求並為此需求配置人員。 還可以在專案的時間、費用和材料使用方式中參考該轉包合約。 您無法編輯或刪除處於此狀態的轉包合約。 **取消** 按鈕可讓您取消已確認的轉包合約。 **重新開啟** 按鈕可讓您重新開啟轉包合約，使其回復到 **草稿** 狀態。 使用 **關閉** 按鈕來關閉已確認的轉包合約。 | 已關閉 <br> 已取消 <br> 草稿 |
| 已關閉 | 這表示轉包合約在已轉包資源實際交付材料和/或工作時的階段已完成。 此狀態下的轉包合約已無法用來估計專案對資源和材料的需求並為此需求配置人員。 此外，也無法在專案的時間、費用和材料使用方式中參考該轉包合約。 您無法編輯或刪除處於此狀態的轉包合約。 | None |
| 已取消 | 這表示不再需要轉包合約在已轉包資源實際交付材料和/或工作時的階段。 處於此狀態的轉包合約不能用來估計專案對資源和材料的需求並為其配置人員，也無法在專案的時間、費用和材料使用方式中加以參考。 您無法編輯或刪除處於此狀態的轉包合約。 | None |


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
