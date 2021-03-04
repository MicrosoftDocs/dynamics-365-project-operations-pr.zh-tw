---
title: 在分工結構圖範本上設定角色
description: 本主題提供有關在分工結構圖範本上設定角色資訊的資訊。
author: Yowelle
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 143f1094c653fb7ac0e026b7875aa162a3eb83f7
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072976"
---
# <a name="set-up-roles-on-work-breakdown-structure-templates"></a>在分工結構圖範本上設定角色

[!include [banner](../includes/banner.md)]

專案經理可以設定可在他們為新專案建立 WBS 時套用的分工結構圖 (WBS) 範本。 專案經理可以在建立範本時新增角色。 使用下列程序，將角色指派至 WBS 範本。

1. 選取 **專案管理與會計** > **設定** > **專案** > **分工結構圖範本** 。
2. 選取所選 WBS 範本的 **詳細資料** 。
3. 選取清單中的工作，然後在 **角色** 欄位中，選取要指派給工作的角色。

## <a name="work-with-a-wbs"></a>使用 WBS

您可以建立新的 WBS，也可以從現有 WBS 範本複製 WBS。 專案經理可以將角色指派至 WBS 中的新工作，輕鬆地管理資源。 取得資源後，或找出可用於工作的已確認資源後，您可以取代角色。 這項彈性讓專案經理可以執行下列工作：

- 確定 WBS 工作封裝所需的資源數目。
- 估計專案成本。
- 決定初步預算。
- 根據角色和資源估計活動期間。
- 根據可用的專案資訊，擬定一些專案管理計劃。

WBS 新增了其他選項，以便善加運用功能。

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th>選項</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>資源指派</td>
<td>在 WBS 中檢視工作的已指派資源、日期、工作時數和預約類型。</td>
</tr>
<tr class="even">
<td>自動產生團隊</td>
<td>使用與工作相關聯的角色，自動新增規劃的資源。 Finance 會使用根據角色的多重準則決策分析，自動建議規劃的資源。 為 WBS 中的工作設定角色和投入量 (小時) 之後，並在結構已發行之後，選取<strong>自動產生團隊</strong>。 所需數目的已規劃資源會新增至 WBS 和<strong>專案與團隊排程</strong>索引標籤 。</td>
</tr>
<tr class="odd">
<td>資源 (下拉式清單)</td>
<td>在<strong>啟動資源指派</strong>頁面上，您可以根據指定的期間，選取要進行最確認預約或未確認預約的資源。 您可以調整檢視設定，以查看並設定資源活動的期間。 您可以使用下列選項，在工作封裝層級選取並指派資源：
<ul>
<li><strong>接受</strong> – 確認對指派至工作的資源所做的變更。</li>
<li><strong>取消</strong> – 取消對指派至工作的資源所做的變更。</li>
<li><strong>自動指派</strong> – 自動選取找到適配角色的可用人員配置資源，並將其指派至所選取的工作。</li>
</ul></td>
</tr>
</tbody>
</table>

1. 在 **所有專案** 頁面上，選取 **XYZ 升級階段 2** 專案。
2. 選取 **計劃** > **活動** > **分工結構圖** 。
3. 選取 **新增** 以已下列等級一的活動新增至 WBS：

    - 起始
    - 規劃
    - 正在執行
    - 監視與控制
    - 關閉​​

4. 設定日期和投入量 (小時)，如下圖所示。

    [![設定日期和投入量](./media/projectresourcing10.jpg)](./media/projectresourcing10.jpg)

5. 選取 **起始** 工作列，然後在 **角色** 欄位中選取 **資深專案經理** 。
6. 選取 **發行** 。
7. 在同一列的 **資源** 欄位中，選取 **Daniel Goldschmidt** ，然後選取 **接受** 。
8. 選取 **規劃** 工作列，然後在 **角色** 欄位中選取 **商務分析師** 。
9. 選取 **發佈** ，然後選取 **自動產生團隊** 。
10. 在出現的訊息方塊中，選取 **是** 。
11. 在 **資源** 欄位中，確認值是否為 **商務分析師 1** 。
12. 對於 **商務分析師 1** 資源，開啟其查詢，然後選取 **啟動資源指派** 。 然後選取工作的工作者。
13. 選取 **未確認指派** &gt; **完整產能** 。

    > [!NOTE] 
    > 您不會收到指出指定的資源目前為 2 的警告，因為資源數目仍保持為 1。

14. 在 **分工結構圖** 頁面上，驗證 WBS 中的資源指派，然後選取 **儲存** 。


[!INCLUDE[footer-include](../includes/footer-banner.md)]