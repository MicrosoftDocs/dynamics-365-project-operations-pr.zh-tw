---
title: 貸記和已更正的發票
description: 本主題提供有關 Project Operations 中已更正發票的資訊
author: rumant
manager: Annbe
ms.date: 10/15/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d2187627439d42b37222dce0a491c62dafc358d5
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073107"
---
# <a name="credits-and-corrected-invoices"></a>貸記和已更正的發票

_**適用於：** 精簡部署 - 交易至開立預估發票_

確認過的專案發票可進行更正以處理與客戶及專案經理議定的變更或貸記。

若要對已確認的發票進行編輯，請開啟已確認的發票，然後選取 **更正此發票** 。 

> [!NOTE]
> 除非專案發票已確認，否則不提供此選取項目。

新的草稿發票會從已確認的發票中建立。 所有來自先前已確認發票的發票明細詳細資料都會複製到新的草稿中。 以下是了解新更正發票中明細詳細資訊的一些要點：

- 所有數量都會更新為零。 應用程式假設所有已開發票的項目都已完全貸記。 如有需要，您可以手動更新這些數量以反映要開立發票的數量，而不是貸記的數量。 應用程式會根據您輸入的數量，計算貸記的數量。 此金額會反映在確認更正後發票時所建立的實際值中。 如果您要對稅金金額進行變更，就必須輸入正確的稅額，而不是貸記的稅額。
- 不會複製先前已確認的產品型合約服務內容。 不支援處理對產品型專案發票的更正。
- 里程碑更正一律以完全貸記的方式處理。
- 如果開立了金額不正確的發票給客戶，則可以更正保留款或預付金的金額。
- 如果使用了不正確的金額對先前已確認發票上的收費進行協調，則可以更正保留款及預付金的對帳單。

> [!IMPORTANT]
> 對其他已開發行票的收費做更正的發票明細詳細資料，其 **更正** 欄位會設定為 **是** 。 已更正發票明細詳細資料的發票具有名為 **有更正** 的欄位，此欄位也會設定為 **是** 。

## <a name="actuals-created-on-confirmation-of-a-corrective-invoice"></a>在確認更正發票時所建立的實際值：

以下是應用程式在確認前根據已對草稿更正發票執行之作業進行更正確認時所建立的實際值。

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
            <td width="216" rowspan="4" valign="top">
                <p>
確認已開發票預付金或保留款的更正。<strong></strong>
                </p>
            </td>
            <td width="408" valign="top">
                <p>
為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。 此金額為正數，因為這是要用來抵消開立保留款或預付金發票時所建立的負數金額。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
已開單銷售沖銷是針對保留款或預付金的金額建立來沖銷原始已開單銷售。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
新的已開單銷售實際值是針對根據保留款或預付金更正之發票明細的更正金額所建立。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
根據保留款或預付金更正之發票明細金額為負數的未開單銷售實際值，用於協調對帳差異。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="4" valign="top">
                <p>
對先前已協調保留款或預付金的更正確認。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
為協調對帳差異所建立的保留款或預付金未開單銷售沖銷。 此金額為正數，要用來抵消先前進行對帳差異協調時所建立的負數金額。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
先前發票金額的已開單銷售沖銷實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
套用於更正後發票之已更正保留款金額的新開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
更正後剩餘保留款或預付金為負數金額的未開單銷售實際值，這會用來對後來的發票進行對帳差異協調。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
對先前已開發票的時間交易開立全額貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始時間發票明細詳細資料上時數及金額的已開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始時間發票明細詳細資料上時數及金額的新增未開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
對時間交易開立部分貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始時間發票明細詳細資料上已開發票時數及金額的已開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
應按照編輯後發票明細詳細資料上時數及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
應按照扣減發票明細詳細資料上已更正數字後剩餘時數及金額收費的新增未開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
對先前已開發票的費用交易開立全額貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始費用發票明細詳細資料上數量及金額的已開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始費用發票明細詳細資料上數量及金額的新增未開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
對先前已開發票的費用交易開立部分貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始費用發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
應按照更正後發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
應按照扣減發票明細詳細資料上已更正數字後剩餘數量及金額收費的新增未開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
對先前已開發票的服務費交易開立全額貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始服務費發票明細詳細資料上數量及金額的已開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
原始服務費發票明細詳細資料上數量及金額的新增未開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="2" valign="top">
                <p>
對先前已開發票的服務費交易開立部分貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始服務費發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
應按照編輯後更正發票明細詳細資料上數量及金額收費的新增未開單銷售實際值、對此值的沖銷，以及等值已開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
對先前已開發票的里程碑交易開立全額貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
原始里程碑發票明細詳細資料上金額的已開單銷售沖銷。
                </p>
                <p>
專案合約服務內容的里程碑發票或帳單狀態已更新為 **已準備好開立發票** 。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
對先前已開發票的里程碑交易開立部分貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
不支援 </p>
            </td>
        </tr>
        <tr>
            <td width="216" valign="top">
                <p>
先前已開發票產品型合約服務內容的貸記和更正。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
不支援 </p>
            </td>
        </tr>
    </tbody>
</table>
