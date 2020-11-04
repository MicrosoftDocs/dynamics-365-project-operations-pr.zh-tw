---
title: 管理時區
description: 建立專案時，其時區取決於所套用工作時數範本中定義的時區。
author: ruhercul
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 27f58f0dacc3404119a719547ad374629c740740
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072934"
---
# <a name="manage-time-zones"></a>管理時區

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_


## <a name="projects"></a>專案

建立專案時，時區取決於所套用工作時數範本中定義的時區。 在 **專案** 上，日期一律相對於每個索引標籤 ( **工作** 索引標籤除外) 中已登入的使用者。當您檢視分工結構圖時，日期永遠以專案的時區來顯示。

## <a name="tasks"></a>工作

建立工作時，開始時間、結束時間和小時/天都是由專案的工作時數所控制。 例如，如果工作是使用時區為 -8 PST 的專案所建立，而且其工作時間為星期一到星期五上午 9:00 至下午 5:00，則任何未使用指派所建立的工作都會遵循專案行事曆的開始時間和結束時間。

## <a name="manage-resources-with-time-zones"></a>使用時區來管理資源

若要在使用 **延伸預約** 時獲得準確且可預測的結果，必須符合兩個重要先決條件：  

- 使用者必須設定其裝置的時區，使其符合系統 **個人化設定** 中所定義的時區。
 
  ![Windows 10 的時區設定](media/reconcile-assignments-03.png)

  ![個人化設定中的時區設定](media/reconcile-assignments-04.png)
 
- 可預約資源至少必須有一分鐘的工作時間，與用於定義所要求之展延的分佈重疊。 例如，工作時間介於上午 9:00 至下午 7:00 之間的下列資源。 

  ![資源分佈的比較](media/reconcile-assignments-05.png)

下表顯示：

- 專案行事曆範本
- 資源 A：此資源有相同的行事曆，並且與專案位於同一個時區。 此預約的開始時間會是上午 9:00。
- 資源 B：此資源與專案位於不同的時區，兩者在其各自時區中的開始時間皆為上午 7:00。 不過，這些預約會從上午 9:00 開始，因為這是指派分佈的最早開始時間。
- 資源 C 和 D：這些資源位於不同的時區，兩者不僅彼此互異，也與專案不相同，而其預約開始時間不早於各自的可用開始時間。

|實體  |行事曆  |
|-|-|
|專案行事曆範本   | ![專案行事曆](media/reconcile-assignments-06.png) |
|資源 A  | ![資源 A 行事曆](media/reconcile-assignments-06.png) |
|資源 B  |  ![資源 B 行事曆](media/reconcile-assignments-07.png) |
|資源 C  |  ![資源 C 行事曆](media/reconcile-assignments-08.png) |
|資源 D  | ![資源 D 行事曆](media/reconcile-assignments-09.png)  |
 
當您瀏覽至 **協調** 檢視表時，會顯示資源指派以及相關聯的預約短缺。

![延長前的協調檢視表](media/reconcile-assignments-10.png)

每個資源都使用了延長預約功能之後，每個資源都會成功延長預約，因為每個資源的時數都與短缺的分佈重疊。

![展長後的協調檢視表](media/reconcile-assignments-11.png) 

請注意，仔細查看預約的詳細資料，就會顯示預約開始時間中的差異。 預約不會比指派分佈的開始時間更早開始，也不會早於資源的可用開始時間。

![資源在排程面板中的新預約](media/reconcile-assignments-12.png)
