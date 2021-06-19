---
title: 專案型更正發票
description: 本主題提供有關如何在 Project Operations 中建立和確認專案型更正發票的資訊。
author: rumant
ms.date: 03/29/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: f6b6670f823577bf7f784443f97f0b77e1e9a6aa
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6012261"
---
# <a name="corrective-project-based-invoices"></a>專案型更正發票

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

確認過的專案發票可進行更正以處理與客戶及專案經理議定的變更或貸記。

若要對已確認的發票進行編輯，請開啟已確認的發票，然後選取 **更正此發票**。 

> [!NOTE]
> 除非專案發票已確認，或是專案型發票有預付金和保留款或者預付金及保留款對帳差異協調，否則無法使用此選取項目。

新的草稿發票會從已確認的發票中建立。 所有來自先前已確認發票的發票明細詳細資料都會複製到新的草稿中。 以下是了解新更正發票中明細詳細資訊的一些要點：

- 所有數量都會更新為零。 Dynamics 365 Project Operations 假設所有已開立發票的項目都已完全貸記。 如有需要，您可以手動更新這些數量以反映要開立發票的數量，而不是貸記的數量。 應用程式會根據您輸入的數量，計算貸記的數量。 此金額會反映在確認更正後發票時所建立的實際值中。 如果您要對稅金金額進行變更，就必須輸入正確的稅額，而不是貸記的稅額。
- 里程碑更正一律以完全貸記的方式處理。


> [!IMPORTANT]
> 對於做為對其他已開發票收費之更正的發票明細詳細資料，**更正** 欄位會設定為 **是**。 對於已更正發票明細詳細資料的發票，**有更正** 欄位會設定為 **是**。

## <a name="actuals-created-when-a-corrective-invoice-is-confirmed"></a>確認更正發票時所建立的實際值

下表列出在確認更正發票時所建立的實際值。

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
開立先前已開發票材料交易的全額貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
材料原始發票明細詳細資料上數量和金額的已開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
材料原始發票明細詳細資料上數量和金額的新增未開單銷售實際值。
                </p>
            </td>
        </tr>
        <tr>
            <td width="216" rowspan="3" valign="top">
                <p>
開立物料交易的部分貸記發票。
                </p>
            </td>
            <td width="408" valign="top">
                <p>
材料原始發票明細詳細資料上已開發票數量及金額的已開單銷售沖銷。
                </p>
            </td>
        </tr>
        <tr>
            <td width="408" valign="top">
                <p>
對已編輯發票明細詳細資料、該項沖銷和等額已開單銷售實際值上數量和金額應收費的新增未開單銷售實際值。
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
里程碑的發票狀態已從<b>客戶發票已過帳</b>更新為<b>已準備好開立發票</b>。
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
不支援此案例。
                </p>
            </td>
        </tr>       
    </tbody>
</table>


[!INCLUDE[footer-include](../includes/footer-banner.md)]
