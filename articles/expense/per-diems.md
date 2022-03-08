---
title: 每日津貼
description: 本主題提供有關費用管理中所用每日津貼規則的資訊。
author: suvaidya
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: suvaidya
ms.openlocfilehash: 192164094231fa2da47806cd9c2ccaba8321c83a1464fc8724fa0d0a7618660f
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6986391"
---
# <a name="per-diems"></a>每日津貼

_**適用於：** 資源/非庫存型案例適用的 Project Operations_


每日津貼是支付給出差工作者的補貼。 在費用管理中，您可以建立各種差旅狀況的每日津貼規則。 每日津貼費率可以根據一年時節、出差地點或兩者來定。 建立每日津貼規則時，您可以指定如果工作者獲得免費贈送的餐飲或服務時，每日津貼費率會扣留的百分比。 您也可以設定每日津貼費率可套用至工作者差旅的最小及最大時數。

## <a name="configuration"></a>組態 

1. 若要新增每日津貼地點，請移至 **設定** > **計算和代碼** > **每日津貼地點**。
2. 針對上述新增的每個地點，選取在住宿、餐飲及其他費用的特定開始與結束日期之間有效的每日津貼費率和貨幣。 每日津貼費率和貨幣是在 **設定** > **計算和代碼** > **每日津貼** 底下進行設定。
3. 在 **每日津貼地點** 頁面上，設定每日津貼費率分級。 每日津貼費率分級可讓您定義住宿、餐飲及其他費用每日補貼的分割百分比。 
4. 若要指定早餐、午餐或晚餐的餐費百分比，請更新 **每日津貼** 索引標籤 **費用管理參數** 頁面上的欄位 。 
    
## <a name="submit-expenses-using-per-diem"></a>提交使用每日津貼的費用
若要提交使用每日津貼的費用，請在建立費用報表時使用 **每日津貼** 費用類別。 輸入 **每個津貼開始日期**、**到目前為止的每日津貼** 和 **每日津貼地點**。 金額會根據所選地點的每日津貼費率進行計算，而餐費扣減則是根據每日津貼費率分級所計算。


[!INCLUDE[footer-include](../includes/footer-banner.md)]