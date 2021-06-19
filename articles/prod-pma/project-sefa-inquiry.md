---
title: 聯邦獎勵支出時間表查詢
description: 這份主題提供「聯邦獎勵支出時間表」查詢的相關資訊。
author: velofog
ms.date: 04/2/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PSNProjSEFAinquiry
audience: Application User
ms.devlang: ''
ms.reviewer: roschlom
ms.search.scope: Operations, Core
ms.tgt_pltfrm: ''
ms.custom: ''
ms.search.region: Global
ms.search.industry: public sector
ms.author: andchoi
ms.search.validFrom: 2020-4-01
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: a16b0fb097124e26da09e220a1239cd6df303f98
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "6010056"
---
# <a name="schedule-of-expenditures-of-federal-awards-inquiry"></a>聯邦獎勵支出時間表查詢

[!include [banner](../includes/banner.md)]

依據行政管理與預算局通函 A-133 (Office of Management and Budget Circular A-133)，接受聯邦基金資助的機構必須遵守稽核需求規定，這也稱為單一稽核。 稽核程序會用來定期報告聯邦補助款的收入與支出。 單一稽核報表的一部分內容會包含聯邦獎勵支出時間表 (Schedule of Expenditures of Federal Awards，SEFA)。

「聯邦獎勵支出時間表」查詢包含聯邦國內補助目錄 (Catalog of Federal Domestic Assistance，CFDA) 標題與編號、授權號碼、補助年度、提供資金的聯邦機構名稱，以及轉手撥款實體的名稱。 查詢是針對特定期間而為。 該期間通常與財務報表期間一致，也就是會計年度。

此查詢包括所選取日期範圍內有預估日期的補助款。 查詢的 **補助機構** 欄顯示受補助客戶，或就轉手撥款補助而言，則顯示補助機構。 對於轉手撥款補助，**轉手撥款機構** 欄會顯示受補助客戶。 如果補助款不是轉手撥款補助，此 **轉手撥款機構** 欄為空白。

## <a name="set-up-the-cfda-clusters"></a>設定 CFDA 叢集

您必須設定 CFDA 叢集，這些叢集可與「聯邦獎勵支出時間表」查詢中的 CFDA 編號產生關聯。

1. Go to **專案管理與會計 \> 設定 \> 補助款 \> 聯邦國內補助目錄叢集**。
2. 選取 **新增** 以建立 CFDA 叢集。
3. 輸入叢集名稱。
4. 選取 **儲存** 以儲存變更。

## <a name="set-up-cfda-numbers"></a>設定 CFDA 編號

您必須設定 CFDA 編號，這些編號可新增至補助款，並加入「聯邦獎勵支出時間表」查詢中。

1. Go to **專案管理與會計 \> 設定 \> 補助款 \> 聯邦國內補助目錄編號**。
2. 選取 **新增** 以建立 CFDA 編號。
3. 在 **編號** 欄中，輸入 CFDA 編號。
4. 按 **Tab** 鍵。
5. 在 **描述** 欄中，輸入 CFDA 標題。
6. 按 **Tab** 鍵。
7. 選擇性：在 **程式叢集** 欄位中，新增適當的 CFDA 叢集。
8. 選取 **儲存** 以儲存變更。

## <a name="set-up-grants-to-report-for-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>設定要申報「聯邦獎勵支出時間表」查詢的補助款

1. 移至 **專案管理與會計 \> 設定 \> 補助款**，然後選取現有的補助款。
2. 在 **設定** 快速分頁的 **聯邦國內補助目錄** 欄位中，指派 CFDA 編號。 補助款的 CFDA 編號決定要進行申報的 CFDA 叢集。
3. 在 **連絡人資訊** 快速分頁中，依照下列步驟輸入贈款者資訊：

    1. 在 **受補助客戶** 欄位中，輸入負責撥款的客戶。 如果是目前既有的補助款，可能已經輸入此資訊。
    2. 指出受補助客戶是否為資助者。 如果受補助客戶為資助者，就讓 **轉手撥款** 核取方塊保持清除。 如果有其他客戶是資助者，而受補助客戶負責支出和追蹤款項時，請選取 **轉手撥款** 核取方塊。

4. 如果您在上一個步驟中選取 **轉手撥款** 核取方塊，請在 **補助機構** 欄位中輸入提供補助款的客戶。 補助機構與受補助客戶不可以是相同的客戶。

以下是轉手撥款補助的範例：

聯邦政府資助某一州的基礎建設專案。 聯邦政府已提供資金給這個州用於開支。 在這種情況下，聯邦政府是補助機構，而該州是受補助客戶。

> [!NOTE] 
> 第一次開啟此功能時，系統會使用補助款現有的編號輸入初始 CFDA 編號。

## <a name="exclude-grants-from-sefa-reporting-based-on-the-grant-type"></a>根據補助款類型排除 SEFA 報表中的補助款

1. 移至 **專案管理與會計 \> 設定 \> 補助款 \> 補助款類型**。
2. 在 **預設資訊** 快速分頁上，選取 **從聯邦獎勵支出時間表中排除** 核取方塊。
3. 選取 **儲存** 以儲存變更。

## <a name="run-the-schedule-of-expenditures-of-federal-awards-inquiry"></a>執行「聯邦獎勵支出時間表」查詢

1. 移至 **專案管理與會計 \> 查詢與報表 \> 補助款查詢 \>聯邦獎勵支出時間表**。
2. 在 **參數** 區段中，依照下列步驟操作：

    1. 在 **日期間隔** 欄位中，選取日期間隔代碼。 或者，在 **開始日期** 和 **結束日期** 欄位中，定義日期間隔。
    2. 選用：若是只要包含已開單交易做為查詢中的營收，請將 **僅包含已開單營收** 選項設定為 **是**。

## <a name="columns"></a>資料行

「聯邦獎勵支出時間表」查詢包含下列各欄：

- 聯邦國內補助目錄叢集名稱
- 補助機構
- 轉手撥款機構
- 補助款名稱
- 補助款識別碼
- 補助款申請識別碼
- 聯邦國內補助目錄
- 收據
- 支出


[!INCLUDE[footer-include](../includes/footer-banner.md)]