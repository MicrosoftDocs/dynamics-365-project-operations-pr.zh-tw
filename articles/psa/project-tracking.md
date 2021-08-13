---
title: 專案進度及成本耗用
description: 本主題提供有關如何追蹤專案進度和成本耗用的資訊。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 08/21/2020
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8bde19fbf1dd9f0c760455ecb7f7f2bd14a358d441bf024ec0cdefa42866f53e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987156"
---
# <a name="project-progress-and-cost-consumption"></a>專案進度及成本耗用

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

對照排程追蹤進度的需求會因行業不同而有所不同。 有些行業以細微等級進行追蹤，而其他行業則以較粗略等級進行追蹤。 本主題說明如何進行排程以符合您組織的需求。

## <a name="effort-tracking-view"></a>投入量追蹤檢視表

**投入量追蹤** 檢視表會追蹤排程中工作的進度。 這會將花費在一項工作的實際努力時數，與工作規劃的努力時數做比較。 Project Service Automation 使用下列公式來計算追蹤計量：

最初建立工作時：計劃成本會設定為完工估計成本。 在工作上記錄實際值之後，投入量 [追蹤] 檢視表中的計算過程如下

- 進度百分比 = 目前為止已花費實際投入量 ÷ 完工估計值 (EAC) 
- 尚未完工估計值 (ETC) = 完工估計值 (EAC) – 目前為止已花費實際投入量 
- EAC = 剩餘未完成投入量 + 目前為止已花費實際投入量 
- 預計投入量差異 = 計劃投入量 – EAC

Project Service Automation 會顯示對工作的投入量差異預測。 如果 EAC 大於計劃投入量，則推測工作需要比原先規劃還要多的時間。 因此，進度落後於排程。 如果 EAC 小於計劃投入量，則推測工作需要比原先規劃還要少的時間。 因此，進度較排程提前。

## <a name="reprojecting-effort"></a>重新推測投入量

修訂工作的原始預估值，對專案經理來說很平常。 專案重新推測是專案經理在專案目前狀態的考量下，對估計值所產生的看法。 然而，我們不建議專案經理變更基準數字，因為專案基準代表專案排程和成本預估值的既定事實原始資料，這是所有專案利害關係人都同意的。

有兩種專案經理可用來重新推測工作投入量的方法：

- 以新的對工作實際剩餘未完成投入量的估計值覆寫預設 ETC。 
- 以新的對工作實際進度的估計值覆寫預設進行百分比。

上述每一種方法都會導致重新計算工作的 ETC、EAC 和進度百分比，以及工作的預計投入量差異。 也會重新計算摘要工作的 EAC、ETC 和進度百分比，並產生最新的投入量差異預測。

## <a name="reprojection-of-effort-on-summary-tasks"></a>重新推測摘要工作的投入量

您可以重新推測摘要工作或容器工作的投入量。 不論使用者用於重新推測的是摘要工作的剩餘未完成投入量還是進度百分比，下列這組計算都會開始：

- 計算工作的 EAC、ETC 和進度百分比。
- 按照與工作上原始 EAC 相同的比例，將新的 EAC 分佈到下層工作。
- 對下至分葉節點工作的每一項個別工作計算新的 EAC。 
- 根據 EAC 值，對下至分葉節點的下層受影響工作重新計算其 ETC 和進度百分比。 這會產生對工作投入量差異的新預測。 
- 重新計算從摘要工作一直到根節點的 EAC。

### <a name="cost-tracking-view"></a>成本追蹤檢視表 

**成本追蹤** 檢視表會將工作已花費的實際成本與計劃成本進行比較。 

> [!NOTE]
> 此檢視表僅顯示人力成本，並不包含來自費用估計的成本。 

Project Service Automation 使用下列公式來計算追蹤計量：

建立工作時，計劃成本等於完工估計成本。 在工作上記錄實際值之後，投入量 **追蹤** 檢視表中的計算過程如下：

 - 成本耗用百分比 = 目前為止已花費實際成本 ÷ 工作的完工估計成本
 - 尚未完工成本 (CTC) = 完工估計成本 – 目前為止已花費實際成本
 - 完工估計成本 = CTC + 目前為止已花費實際成本
 - 預計成本差異 = 計劃成本 – 完工估計成本

成本差異預測會顯示在工作上。 如果完工估計成本大於計劃成本，則推測工作耗用比原先規劃還要多的成本。 因此，有預算超支的趨勢。 如果完工估計成本小於計劃成本，則推測工作耗用比原先規劃還要少的成本，並且有維持在預算內的趨勢。

## <a name="project-managers-reprojection-of-cost"></a>專案經理對成本的重新推測

重新推測投入量時，CTC、完工估計成本、成本耗用百分比和預計成本差異全都會在 **成本追蹤** 檢視表中重新計算。

## <a name="project-status-summary"></a>專案狀態摘要

追蹤 **投入量追蹤** 和 **成本追蹤** 檢視表中的資料時，會顯示專案根節點、摘要工作和分葉節點工作層級上的進度和成本耗用量。 專案 **實體** 頁面上的 **狀態** 區段會顯示專案層級狀態的摘要。

## <a name="status-summary-fields"></a>狀態摘要欄位

**整體專案狀態** 欄位是顯示專案整體狀態的可編輯欄位。 此欄位會使用色彩代碼 (例如綠色、黃色和紅色) 來表示風險增加。 **註解** 欄位可讓專案經理輸入關於狀態的特定註解。 **狀態更新時間** 欄位不可編輯的欄位，其值是指示狀態上次更新時的時間戳記。

**排程效能** 和 **成本績效** 欄位是從追蹤日期開始設定。 當 **投入量追蹤** 檢視表中根節點的排程與成本差異為正值時，您可以將這些欄位設定為 **提前**。 當根節點的排程與成本差異是負值時，您可以將其設定為 **落後**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]