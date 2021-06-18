---
title: 專案報價明細概觀
description: 本主題提供有關使用專案報價明細進行專案工作的資訊。
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 72feb791e48c9bacd4a0b7ea5cd77ddc8eb5f514
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5996286"
---
# <a name="project-quote-lines-overview"></a>專案報價明細概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

專案型報價明細是為了協助在業務開發上估計專案工作而設計。 專案型報價明細的結構已運用下列概念針對專案估計值進行擴充：

- 計費方式
- 專案對應
- 已包含交易分類
- 不得超過限制
- 可收費率設定
- 使用報價明細詳細資料的估計
- 報價明細客戶

下表提供有關專案型報價明細的 **一般** 索引標籤上的欄位資訊。 這些欄位可協助為專案工作設定詳細的全新估計基礎。

| **欄位** | **描述** | **下游影響** |
| --- | --- | --- |
| 名字 | 報價明細的名稱，應可協助您找出估計中報價的分立元件。 | 已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| 計費方式 | 在根據商機所建立的報價上，此值是從商機明細的對應欄位複製而來。 此欄位包含 Dynamics 365 Project Operations 支援的兩個主要合約模型：</br>- 固定價格</br>- 時間和材料。| 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| Project | 使用此選用欄位來找出將在此業務開發上用來交付工作的專案。 將專案對應至報價明細時，不僅有助於設定應收費工作，而且還可協助將專案型估計值提供給報價明細做為報價明細詳細資料。 未將專案對應至專案型報價明細時，應藉由建立每個報價明細詳細資料，手動建立估計值。 | 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| 包括時間 | **是**/**否** 旗標指示所選專案的時間交易或人力成本是否會包含在此報價明細的估計值中。 **否** 值表示時間交易或人力成本不會包含在此報價明細的估計值中。 **是** 值表示時間交易或人力成本會包含在此報價明細的估計值中。 | 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| 包括費用 | **是**/**否** 旗標指示所選專案的費用成本是否會包含在此報價明細的估計值中。 **否** 值表示費用成本不會包含在此報價明細的估計值中。 **是** 值表示費用成本會包含在此報價明細的估計值中。 | 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| 包括服務費 | **是**/**否** 旗標指示所選專案的服務費是否會包含在此報價明細的估計值中。 **否** 值表示服務費不會包含在此報價明細的估計值中。 **是** 值表示服務費會包含在此報價明細的估計值中。 | 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| 報價金額 | 這是針對所有為此專案型報價明細預測之工作，報價給客戶的金額。 在根據商機所建立的報價上，此值是從商機明細的 **客戶預算** 欄位複製而來。 專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的金額。 | 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| 估計稅額 | 這是可編輯的欄位，以供使用者在報價明細上新增估計稅金。 專案型報價明細含有明細詳細資料時，此欄位會遭鎖定而無法加以編輯，並且會彙總列出報價明細詳細資料上的稅額。 | 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| 稅後報價金額 | 此欄位是稅後報價明細金額，並且為唯讀。 此欄位中的金額是以 *報價金額 + 稅金* 計算而得。 | 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| 不得超過限制 | 此欄位是可編輯的欄位，只能在帳務方式為 **時間和材料** 的專案型報價明細上使用。 | 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |
| 客戶預算 | 此欄位是可編輯的欄位，如果報價是根據商機所建立，則該欄位是從商機明細的對應欄位複製而來。 | 此欄位值已複製到報價成交時從此報價明細中建立的專案合約服務內容。 |

## <a name="validation-rules-for-fields-on-the-general-tab-of-project-based-quote-lines"></a>專案型報價明細的 [一般] 索引標籤上的欄位驗證規則

**規則 1**：所選專案上的特定交易分類只能包含在報價的一個專案型報價明細中。

**規則 2**：如果商機有多個報價，則可以有來自各種全都參考相同專案且包含相同交易分類之不同報價的報價明細。

**規則 3**：如果報價不屬於同一個商機，則不能包含相同的專案和交易分類。

<table border="1" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="61" valign="top">
                <p>
                    <strong>商機</strong>
                </p>
            </td>
            <td width="41" valign="top">
                <p>
                    <strong>報價</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>報價明細</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>包含時間</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>包含費用</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>包括</strong>
                </p>
                <p>
                    <strong>服務費</strong>
                </p>
            </td>
            <td width="54" valign="top">
                <p>
                    <strong>有效/無效</strong>
                </p>
            </td>
            <td width="308" valign="top">
                <p>
                    <strong>原因</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
無效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
違反規則 #1。 P1 專案上的時間、費用和服務費已包含在報價明細 QL1 與 QL2 中。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
無 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
無效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
違反規則 #1。 P1 專案上的時間和服務費已包含在報價明細 QL1 與 QL2 中。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
無 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
有效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                 <p>
P1 專案上的時間和服務費已包含在 QL1 中。
P1 專案上的費用已包含在 QL2 中。
要包含在每個報價明細的項目中沒有重疊，因此有效。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
無 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
無 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="54" rowspan="2" valign="top">
                <p>
無效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
違反上述規則 #1 </p>
                <p>
Q1 包含整個專案 P1 的時間、費用和服務費。
                </p>
                <p>
QL2 包含整個專案 P1 的時間、費用和服務費，並與 Q1 中包含的項目重疊。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="54" valign="top">
                <p>
有效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
根據規則 #2，Q1 和 Q2 是同一個商機上的兩個報價，因此都可以對專案的相同元件進行估計。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 2 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
第 2 季的 QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="54" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
            </td>
            <td width="41" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="54" valign="top">
            </td>
            <td width="308" valign="top">
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O1 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="54" valign="top">
                <p>
有效 </p>
            </td>
            <td width="308" rowspan="2" valign="top">
                <p>
根據規則 #3，Q1 和 Q2 是兩個各在不同商機上的報價，因此無法對相同專案的相同元件進行估計。
                </p>
            </td>
        </tr>
        <tr>
            <td width="61" valign="top">
                <p>
O2 </p>
            </td>
            <td width="41" valign="top">
                <p>
第 1 季 </p>
            </td>
            <td width="42" valign="top">
                <p>
QL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="48" valign="top">
                <p>
.是 </p>
            </td>
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="54" valign="top">
                <p>
無效 </p>
            </td>
        </tr>
    </tbody>
</table>



[!INCLUDE[footer-include](../includes/footer-banner.md)]
