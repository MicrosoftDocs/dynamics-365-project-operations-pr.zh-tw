---
title: 設定專案合約服務內容的應收費元件
description: 本文提供有關如何在 Project Operations 中將應收費元件新增至合約服務內容的資訊。
author: rumant
ms.date: 10/08/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: 33296c93964cc88499e7a98d499b99463e59d62a
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/05/2022
ms.locfileid: "9825554"
---
# <a name="configure-chargeable-components-of-a-project-contract-line"></a>設定專案合約服務內容的應收費元件

_**適用於：** 精簡部署 - 交易至開立預估發票、資源/非庫存型案例適用的 Project Operations_

專案合約服務內容有 *內含* 元件和 *應收費* 元件。

內含元件是受限於下列各項的元件：

  - 帳務方式和客戶分割
  - 不得超過限制 
  - 專案型合約服務內容上定義的發票週期設定

您可以使用 **帳單類型** 欄位將一部分內含元件標示為應收費。 **帳單類型** 欄位是選項組，允許在合約服務內容的情境下使用下列值：

  - 應收費
  - 不應收費

您可以在工作、角色和交易類別上定義應收費元件。

可收費率是在專案合約服務內容的工作上所定義，並套用至服務內容所包含的所有交易分類。 如果合約服務內容上的 **包含工作** 欄位為空白或已設定為 **整個專案**，則沒有提供 **應收費工作** 索引標籤。

專案合約服務內容的角色上所定義的可收費率只能套用至 **時間** 交易分類。 如果合約服務內容上的 **包含時間** 欄位為空白或已設定為 **否**，則沒有提供 **應收費角色** 索引標籤。

專案合約服務內容的交易類別上所定義的可收費率只能套用至 **費用** 交易分類。 如果 **包含費用** 欄位已設定為 **否**，則沒有提供 **應收費類別** 索引標籤。

### <a name="update-a-project-task-as-chargeable-or-non-chargeable"></a>將專案工作更新為應收費或不應收費

專案工作在能使下列設定變成可行的特定合約服務內容上可以是應收費，也可以是不應收費：

如果專案型合約服務內容包含 **時間**，且特定工作 **T1** 與其建立為應收費關聯。 如果有第二個合約服務內容，其中包含 **費用** 時，您可以將合約服務內容的 T1 工作關聯為不應收費。 結果是，工作中所記錄的所有時間都是應收費的，而所有費用都是不應收費的。

工作的帳單類型可以在合約服務內容的 **應收費工作** 索引標籤上，透過更新合約服務內容工作子格上的 **帳單類型** 欄位來進行設定。 或者，也可以在顯示與工作相關之合約服務內容的專案工作帳單設定子格中更新 **帳單類型** 欄位。

### <a name="update-a-role-as-chargeable-or-non-chargeable"></a>將角色更新為應收費或不應收費

角色在特定合約服務內容上，可以是應收費，也可以是不應收費。

您可以在合約服務內容的 **應收費角色** 索引標籤上設定角色的帳單類型。 若要這樣，請更新 **應收費角色** 子格上的 **帳單類型** 欄位。

### <a name="update-a-transaction-category-as-chargeable-or-non-chargeable"></a>將交易類別更新為應收費或不應收費

交易類別在特定合約服務內容上，可以是應收費，也可以是不應收費。

您可以在專案型合約服務內容的 **應收費類別** 索引標籤上設定交易的帳單類型。 若要這樣，請更新 **應收費類別** 子格上的 **帳單類型** 欄位。

### <a name="resolve-chargeability"></a>解析可收費率

只有在下列情況下，才能將針對時間建立的估計值或實際值視為應收費：

   - **時間** 已包含在合約服務內容中。
   - **角色** 已在合約服務內容中設定為應收費。
   - **包含的工作** 已在合約服務內容上設定為 **選取的工作**。
 
 如果這三種情況成立，工作就會設定為應收費。 

只有在下列情況下，才能將針對費用建立的估計值或實際值視為應收費：

   - **費用** 已包含在合約服務內容中
   - **交易類別** 已在合約服務內容中設定為應收費
   - **包含的工作** 已在合約服務內容上設定為 **選取的工作**
  
 如果這三種情況成立，**工作** 就會設定為應收費。 

只有在下列情況下，才能將針對材料建立的估計值或實際值視為應收費：

   - **材料** 已包含在合約服務內容中
   - **包含的工作** 已在合約服務內容上設定為 **選取的工作**

如果這兩種情況成立，**工作** 就會設定為應收費。 

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>包含時間</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>包含費用</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>包含材料</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
                    <strong>包含的工作</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>角色</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>類別</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>工作​​</strong>
                    <strong></strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
                    <strong>可收費率影響</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整個專案 </p>
            </td>
            <td width="65" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="70" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="65" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>應收費</strong>
                </p>
                <p>
費用實際值的帳單類型：<strong>應收費</strong>
                </p>
                <p>
材料實際值的帳單類型：<strong>應收費</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
僅限選取的工作 </p>
            </td>
            <td width="65" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="70" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="65" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>應收費</strong>
                </p>
                <p>
費用實際值的帳單類型：<strong>應收費</strong>
                </p>
                <p>
材料實際值的帳單類型：<strong>應收費</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
僅限選取的工作 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="65" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>不應收費</strong>
                </p>
                <p>
費用實際值的帳單類型：應收費 </p>
                <p>
材料實際值的帳單類型：應收費 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
僅限選取的工作 </p>
            </td>
            <td width="65" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="70" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>不應收費</strong>
                </p>
                <p>
費用實際值的帳單類型：<strong>不應收費</strong>
                </p>
                <p>
材料實際值的帳單類型：<strong>不應收費</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
僅限選取的工作 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>不應收費</strong>
                </p>
                <p>
費用實際值的帳單類型：<strong>不應收費</strong>
                </p>
                <p>
材料實際值的帳單類型：<strong>不應收費</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
僅限選取的工作 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>不應收費</strong>
                </p>
                <p>
費用實際值的帳單類型：<strong>不應收費</strong>
                </p>
                <p>
材料實際值的帳單類型：應收費 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>無</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整個專案 </p>
            </td>
            <td width="65" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>應收費</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>無法使用</strong>
                </p>
                <p>
費用實際值的帳單類型：應收費 </p>
                <p>
材料實際值的帳單類型：應收費 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
                    <strong>無</strong>
                </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整個專案 </p>
            </td>
            <td width="65" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>無法使用</strong>
                </p>
                <p>
費用實際值的帳單類型：<strong>不應收費</strong>
                </p>
                <p>
材料實際值的帳單類型：應收費 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>無</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整個專案 </p>
            </td>
            <td width="65" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="70" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="65" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：應收費 </p>
                <p>
費用實際值的帳單類型：<strong>無法使用</strong>
                </p>
                <p>
材料實際值的帳單類型：應收費 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
                    <strong>無</strong>
                </p>
            </td>
            <td width="63" valign="top">
                <p>
.是 </p>
            </td>
            <td width="75" valign="top">
                <p>
整個專案 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="65" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>不應收費</strong>
                </p>
                <p>
費用實際值的帳單類型：<strong>無法使用</strong>
                </p>
                <p>
材料實際值的帳單類型：應收費 </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>無</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
整個專案 </p>
            </td>
            <td width="65" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="70" valign="top">
                <p>
應收費 </p>
            </td>
            <td width="65" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：應收費 </p>
                <p>
費用實際值的帳單類型：應收費 </p>
                <p>
材料實際值的帳單類型：<strong>無法使用</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="70" valign="top">
                <p>
.是 </p>
            </td>
            <td width="78" valign="top">
                <p>
.是 </p>
            </td>
            <td width="63" valign="top">
                <p>
                    <strong>無</strong>
                </p>
            </td>
            <td width="75" valign="top">
                <p>
整個專案 </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="70" valign="top">
                <p>
                    <strong>不應收費</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
無法設定 </p>
            </td>
            <td width="350" valign="top">
                <p>
時間實際值的帳單：<strong>不應收費</strong>
                </p>
                <p>
費用實際值的帳單類型：<strong>不應收費</strong>
                </p>
                <p>
材料實際值的帳單類型：<strong>無法使用</strong>
                </p>
            </td>
        </tr>
    </tbody>
</table>





[!INCLUDE[footer-include](../../includes/footer-banner.md)]
