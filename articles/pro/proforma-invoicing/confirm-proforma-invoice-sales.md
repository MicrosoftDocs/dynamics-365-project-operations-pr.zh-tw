---
title: 確認預估發票 - 精簡
description: 本主題提供有關在 Project Operations 中確認預估發票的資訊。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3b1818f20a0d54848939b689f87986154943c57a
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5274268"
---
# <a name="confirm-a-proforma-invoice---lite"></a>確認預估發票 - 精簡

_**適用於：** 精簡部署 - 交易至開立預估發票_


確認預估發票之後，專案發票的狀態會更新為 **已確認**。 確認發票時，它會變成唯讀。 從現在開始，發票僅於有任何客戶提議更正或賒帳，或是將發票標示為已付款時，才能進行更正。

下表列出系統所建立的實際值。 這些實際值是在確認草稿專案發票前對其執行特定作業時所建立。

<table border="0" cellspacing="0" cellpadding="0">
    <tbody>
        <tr>
            <td width="216" valign="top">
                <p>
                    <strong>案例</strong>
                </p>
            </td>
            <td width="808" valign="top">
                <p>
                    <strong>確認時建立的實際值</strong>
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
開立預付金 (或定額保留後隨用即扣型付款) 的發票 </p>
            </td>
            <td width="408" valign="top">
                <p>
類型為<strong>保留款</strong>的已開單銷售實際值是針對預付金 (或定額保留後隨用即扣型付款) 的金額所建立。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
要用於協調對帳差異之金額為負值的保留款或預付金未開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
在發票上將保留款或預付金的差異完全協調之後。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。 此金額為正值，因為這是要用來抵消開立保留款或預付金發票時所建立的負值金額。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
此發票金額的已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
在發票上將保留款或預付金的差異部分協調之後。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。 此金額為正值，因為這是要用來抵消開立保留款或預付金發票時所建立的負值金額。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
此發票金額的已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
要在未來發票上用於協調對帳差異之保留款或預付金剩餘金額的負數未開單銷售實際值。
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
應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、銷售實際值的沖銷，以及等值已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
不應對已編輯發票明細詳細資料在扣除更正過數字後剩餘時數及金額收費的新增未開單銷售實際值、銷售實際值的沖銷，以及等值已開單銷售實際值。
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
原始費用核准上的數量及金額的已開單銷售實際值 </p>
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
        <tr>
            <td width="216" valign="top">
                <p>
開立產品型合約服務內容的發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
其數量和金額來自產品型合約服務內容的產品明細已開單銷售實際值。
                </p>
            </td>
        </tr>
    </tbody>
</table>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]