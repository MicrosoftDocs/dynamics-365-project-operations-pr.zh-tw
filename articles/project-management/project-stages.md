---
title: 專案階段
description: 本主題提供有關 Microsoft Dynamics Project Operations 中所提供之專案階段的資訊。
author: ruhercul
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 079c3d2d16cf802d2b9ecc779577e6e390d92ddc
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996916"
---
# <a name="project-stages"></a>專案階段

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

專案階段為了反映專案進展時的狀態而設計。 自訂可以用來讓系統自動更新階段的商務程序流程、Power Automate 或外掛程式擴充功能。

預設商務程序流程中已定義下列階段：

- 新的 ​​
- 報價
- 計劃
- 交付
- 完成
- 關閉​​ 

## <a name="new"></a>新的 ​​

建立專案時，專案階段會設定為 **新增**。 如果專案是從範本建立，則可能會有排程、估計值及團隊資料。 否則，這會是專案的大綱，您必須輸入剩餘的元件。

## <a name="quote"></a>報價

將專案與報價建立關聯或從報價建立專案時，專案階段會設定為 **報價**，而估計的開始和結束日期也會更新。 專案處於 **報價** 階段時，**專案實體** 上的 **銷售** 索引標籤會顯示報價的詳細資料。

## <a name="plan"></a>計劃

當您贏得與專案相關聯的報價，且專案已進入 **合約** 階段時，專案階段會更新為 **計劃**。 專案處於 **計劃** 階段時，**專案實體** 頁面會顯示合約的詳細資料。

## <a name="deliver"></a>交付

專案計劃完成，且您已準備好開始專案時，專案經理應將專案階段更新為 **交付**，以顯示專案已開始。

## <a name="complete"></a>完成 

專案的工作完成後，專案經理就可以將階段更新為 **完成**。 專案經理藉由將專案階段更新為 **完成**，指出工作已百分之百完成，但專案仍保持開啟狀態，讓您可以記錄任何擱置的時間或費用項目。

## <a name="close"></a>關閉

將專案所有的交易都記錄下來後，專案經理就可以將階段更新為 **關閉**。 此時，無法記錄任何交易，且專案會設定為唯讀。



[!INCLUDE[footer-include](../includes/footer-banner.md)]