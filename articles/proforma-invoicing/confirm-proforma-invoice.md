---
title: 確認預估發票
description: 本主題提供有關確認預估發票的資訊。
author: rumant
manager: AnnBe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: b2ed241509d2643d841ce55777e6e316612f70b8
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5287858"
---
# <a name="confirm-a-proforma-invoice"></a>確認預估發票

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

確認預估發票之後，專案發票的狀態會更新為 **已確認**。 確認發票時，它會變成唯讀。 從現在開始，發票僅於有任何客戶提議更正或賒帳，或將其標示為已付款時，才能進行更正。

下表列出系統所建立的實際值。 這些實際值是在確認草稿專案發票前對其執行特定作業時所建立。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="416" valign="top">
                <p>
                    <strong>案例</strong>
                </p>
            </td>
            <td width="608" valign="top">
                <p>
                    <strong>確認時建立的實際值</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
不對草稿發票進行任何編輯，即開立時間交易發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始時間核准上的時數及金額的未開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始時間核准上的時數及金額的已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
開立減少數量時所編輯之時間交易的發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始時間核准上的時數及金額的未開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
不應對已編輯發票明細詳細資料在扣除更正過數字後剩餘時數及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
開立增加數量時所編輯之時間交易的發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始時間核准上的時數及金額的未開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
不對草稿發票進行任何編輯，即開立費用交易發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始費用核准上的時數及金額的未開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始費用核准上的數量及金額的已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
開立減少數量時所編輯之費用交易的發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始費用核准上的時數及金額的未開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
應按照編輯後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。 
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
不應對已編輯發票明細詳細資料在扣除更正過數字後剩餘數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
開立增加數量時所編輯之費用交易的發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始費用核准上的時數及金額的未開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
應按照編輯後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、未開單銷售實際值的沖銷，以及等值已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
開立服務費發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始帳目明細上的服務費金額的未開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始費用帳目明細上的數量及金額的已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
開立里程碑發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始里程碑在專案合約服務內容上的里程碑金額已開單銷售實際值。
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]