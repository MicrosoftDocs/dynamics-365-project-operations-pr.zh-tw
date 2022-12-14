---
title: 專案合約服務內容概觀
description: 本文提供有關在 Project Operations 中使用專案合約服務內容的資訊。
author: rumant
ms.date: 10/28/2020
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: rumant
ms.openlocfilehash: f5a529233692a39b0674417cd4ea225e40243086
ms.sourcegitcommit: e0cbbe7c6f03d4978134405cf04bd8bc1d019f65
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/05/2022
ms.locfileid: "9824616"
---
# <a name="project-contract-lines-overview"></a>專案合約服務內容概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 中的專案型合約服務內容，旨在保留業務開發的專案工作特定元件的估計和計費合約。 專案型合約服務內容的結構是針對專案評估和計費案例進行延伸，有下列概念：

- 帳務方式
- 專案和工作對應
- 已包含交易分類
- 不得超過限制
- 可收費率設定
- 使用合約服務內容詳細資料進行估計
- 合約服務內容客戶

下表包含專案合約服務內容的 **一般** 索引標籤上的欄位，可協助為專案工作的詳細、基礎估計和帳單安排奠定基礎。

| 欄位 | 描述 | 下游影響 |
| --- | --- | --- |
| **名稱** | 合約服務內容的名稱。 這可識別所估計合約的獨立元件。 對於根據報價建立的專案合約，此值會從專案型報價明細的對應值中複製。 | 在建立發票時，會複製到從此合約服務內容建立的專案發票明細上的名稱。 |
| **計費方式** | 對於根據報價建立的專案合約，此值會從報價明細的對應欄位複製。 這是一個選項組，代表 Project Operations 所支援的兩種主要合約模型：</br>- **固定價格**</br>- **時間和資料** | 根據參考之合約服務內容的計費方式，將處理實際交易。 如果實際值參考的合約服務內容有時間和資料計費方式，就會建立成本和未開單銷售實際記錄。 如果實際值參考的合約服務內容有固定價格計費方式，則只會建立成本實際值。 |
| **Project** | 您可以使用這個欄位來找出用來在此業務開發中傳遞工作的專案。 | 此值將會與 **包含的工作** 及 **包含的交易分類** 搭配使用，以解析實際或估計明細記錄上的合約服務內容參考。 |
| **包含的工作** | 表示此合約服務內容是否包含所選取專案的所有專案工作，或只包含部分工作。 這是選項組，其可能的值如下：</br>- **所有專案工作**</br>- - **僅限選取的專案工作**。 此欄位中的空白值等於選取 **所有專案工作**。 | 如果選取 **僅限選取的工作**，您可以選取特定工作，並在 **專案** 頁面的 **工作帳單設定** 索引標籤上，將它們關聯至此合約服務內容。 此值將與 **專案** 及 **包含的交易** 類別搭配使用，以解析實際值或估計明細記錄上的合約服務內容參考。 |
| **包括時間** | **是**/**否** 值表示此合約服務內容中是否包含所選專案的時間交易或人力成本。 **否** 值表示時間交易或人力成本不會包括在此合約服務內容上。 **是** 值表示會包含。 | 此值會與專案一起用來解析實際或估計明細記錄上的合約服務內容參考。 |
| **包括費用** | **是**/**否** 值表示此合約服務內容中是否包含所選專案的費用成本。 **否** 值表示費用成本不會包括在此合約服務內容上。 **是** 值表示會包含。 | 此值會與專案一起用來解析實際或估計明細記錄上的合約服務內容參考。 |
| **包含的材料** | **是**/**否** 值表示此合約服務內容中是否包含所選專案的材料成本。 **否** 值表示此合約服務內容中將不包含所選專案的材料成本。 **是** 值表示會包含。 | 此值會與專案一起用來解析實際或估計明細記錄上的合約服務內容參考。 |
| **包括服務費** | **是**/**否** 值表示此合約服務內容中是否包含所選專案的服務費成本。 **否** 值表示服務費不會包括在此合約服務內容上。 **是** 值表示會包含。 | 此值會與專案一起用來解析實際或估計明細記錄上的合約服務內容參考。 |
| **合約金額** | 在固定價格合約服務內容上，此金額是已同意的值，將針對與此合約服務內容相關聯的所有工作元件，開發票給客戶。 在時間和資料合約服務內容上，此金額是估計值，將針對與此合約服務內容相關聯的所有工作元件，開發票給客戶。 對於根據報價建立的專案合約，此值會從報價明細的對應欄位複製。 當專案型合約服務內容有明細詳細資料時，會鎖定此欄位不予編輯，並根據合約服務內容詳細資料的金額進行匯總。 | 當合約服務內容有明細詳細資料時，可變更明細詳細資料的金額，以修改此值。 在固定價格合約服務內容上，此值是用來產生週期帳單里程碑上的稅前金額。 |
| **估計稅額** | 使用者可以編輯此欄位，以在合約服務內容上輸入估計的稅額。 當專案型合約服務內容有明細詳細資料時，會鎖定此欄位不予編輯，並根據合約服務內容詳細資料的稅額進行匯總。 | 當合約服務內容有明細詳細資料時，可變更明細詳細資料的稅額，以修改此值。 在固定價格合約服務內容上，此值是用來產生週期帳單里程碑上的稅金。 |
| **稅後合約金額** | 稅後合約服務內容金額。 此欄位為唯讀，其計算方式為 **合約金額 + 稅金**。 | 在固定價格合約服務內容上，此值是用來產生週期帳單里程碑。 |
| **不得超過限制** | 使用者可以編輯此欄位，而此欄位只能用於將計費方式設定為時間與資料的專案型合約服務內容。 | 使用者可以編輯此欄位。 當時間和資料的實際值參考此合約服務內容的時間和資料時，實際值的金額會根據合約服務內容的不得超過限制進行評估。 在考慮已經花費和認可的金額之後，完成此評估。 |
| **客戶預算** | 如果合約是從報價建立的，則此欄位可編輯，並從報價明細的對應欄位複製。 | 此欄位只用於提供資訊，對下游沒有任何意義。 |

## <a name="validation-rules-for-the-options-on-the-general-tab-of-project-based-contract-lines"></a>專案型合約服務內容的一般索引標籤的選項驗證規則

規則 1：如果 **包含的工作** 欄位為空白，或設為 **所有專案工作**，則專案的所有工作都會包括在合約服務內容上。

規則 2：當 **包含的工作** 欄位空白或將已明確設定為 **所有專案工作** 時，專案和特定交易類別只能包含於合約的一個專案型合約服務內容。

規則 3：當 **包含的工作** 欄位設定為 **僅限選取的專案工作** 時，專案和特定交易類別可以包含於合約的多個專案型合約服務內容。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="43" valign="top">
                <p>
                    <strong>合約</strong>
                </p>
            </td>
            <td width="65" valign="top">
                <p>
                    <strong>合約服務內容</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>Project</strong>
                </p>
            </td>
            <td width="67" valign="top">
                <p>
                    <strong>包含的工作</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>包括時間</strong>
                </p>
            </td>
            <td width="48" valign="top">
                <p>
                    <strong>包括費用</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>包含的材料</strong>
                </p>
            </td>
            <td width="42" valign="top">
                <p>
                    <strong>包括​​</strong>
                </p>
                <p>
                    <strong>費用</strong>
                </p>
            </td>
            <td width="53" valign="top">
                <p>
                    <strong>有效/無效</strong>
                </p>
            </td>
            <td width="250" valign="top">
                <p>
                    <strong>原因</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
無效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
違反規則 #2。 P1 專案的時間、費用、材料和服務費包含在合約服務內容 CL1 及 CL2 中。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
無效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
違反規則 #2。 P1 專案的時間、材料和服務費包含在合約服務內容 CL1 及 CL2 中。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
有效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
P1 專案的時間、材料和服務費包含在 CL1 中。
                </p>
                <ul>
                    <li>
P1 專案上的費用已包含在 CL2 中。
                    </li>
                </ul>
                <p>
每個合約服務內容所包含的內容之間沒有任何重疊，因此有效。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
無 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
僅限選取的工作 </p>
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
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
無效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
違反規則 #2 </p>
                <p>
C1 包含專案 P1 上工作子集的時間、材料、費用和服務費。
                </p>
                <p>
CL2 包含整個專案 P1 的時間、材料、費用和服務費，因此與 C1 中所包含的內容重疊。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
空白 </p>
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
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
            </td>
            <td width="65" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="67" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="48" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="42" valign="top">
            </td>
            <td width="53" valign="top">
            </td>
            <td width="250" valign="top">
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL1 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
僅限選取的工作 </p>
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
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
            <td width="53" rowspan="2" valign="top">
                <p>
有效 </p>
            </td>
            <td width="250" rowspan="2" valign="top">
                <p>
根據規則 3 </p>
                <p>
C1 包含專案 P1 上工作子集的時間、材料、費用和服務費。
                </p>
                <p>
CL2 包含專案 P1 的工作子集的時間、材料、費用和服務費。
                </p>
                <p>
唯一的額外驗證是要求 CL1 上的工作子集與 CL2 上的工作子集不同，以確保其間沒有任何重疊。 建立與工作的關聯時，系統會完成此作業。
                </p>
            </td>
        </tr>
        <tr>
            <td width="43" valign="top">
                <p>
C1 </p>
            </td>
            <td width="65" valign="top">
                <p>
CL2 </p>
            </td>
            <td width="42" valign="top">
                <p>
P1 </p>
            </td>
            <td width="67" valign="top">
                <p>
僅限選取的工作 </p>
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
            <td width="42" valign="top">
                <p>
.是 </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
