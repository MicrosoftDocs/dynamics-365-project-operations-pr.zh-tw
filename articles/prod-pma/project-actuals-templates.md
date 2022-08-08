---
title: 將專案實際值從 Project Service Automation 直接同步處理至要在財務和營運中進行過帳的專案整合帳目
description: 本文說明用來將 Microsoft Dynamics 365 Project Service Automation 中的專案實際值直接同步處理至財務和營運的範本及基礎工作。
author: Yowelle
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: 34a0a0f7277777895077d221cd95e8d962d2a902
ms.sourcegitcommit: a798fed5c59e3fefa62cdfa42c852d529b33fd35
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/18/2022
ms.locfileid: "9028968"
---
# <a name="synchronize-project-actuals-directly-from-project-service-automation-to-the-project-integration-journal-for-posting-in-finance-and-operations"></a>將專案實際值從 Project Service Automation 直接同步處理至要在財務和營運中進行過帳的專案整合帳目

[!include[banner](../includes/banner.md)]

本文說明用來將 Dynamics 365 Project Service Automation 中的專案實際值直接同步處理至 Dynamics 365 Finance 的範本及基礎工作。

範本會將交易從 Project Service Automation 同步處理至 Finance 中的暫存表格。 完成同步處理後，您 **必須** 將資料從暫存表格匯入至整合日記帳中。

> [!NOTE]
> - 專案實際值整合是在 8.0.1 版中開始提供。
> - 如果您在安裝 KB 4132657 和 KB 4132660 之後使用 Enterprise Edition 7.3.0，則可以使用範本來整合專案工作、費用交易類別、工時估計、費用估計值和實際值，以及設定功能鎖定。 如果您必須重設會計分配，建議您還要安裝 KB 4131710。
> - 如果您使用 7.3.0 版，而且要將費用交易從 Project Service Automation 那裡帶過來，則必須安裝 KB 4345320，才能將這些費用包含在專案發票中。
> - 如果您在 Project Service Automation 中輸入時間或費用交易的銷售稅額，則必須安裝 Project Service Automation 更新 7。 否則，稅金實際值不會連結至相關的時間或費用實際值，而這些實際值不會同步處理至 Finance。 如需詳細資訊，請連絡支援人員。

## <a name="data-flow-for-project-service-automation-to-finance"></a>Project Service Automation 至 Finance 的資料流程

Project Service Automation 至 Finance 整合解決方案會使用資料整合功能，跨 Project Service Automation 與 Finance 的執行個體來同步處理資料。 可與資料整合功能搭配使用的整合範本會啟用有關專案實際值從 Project Service Automation 到 Finance 的資料流程。

下圖這些顯示如何在 Project Service Automation 與 Finance 之間同步處理資料。

[![Project Service Automation 與財務和營運整合的資料流程。](./media/ProjectActualsFlow.jpg)](./media/ProjectActualsFlow.jpg)

## <a name="project-actuals-from-project-service-automation"></a>Project Service Automation 中的專案實際值

### <a name="template-and-tasks"></a>範本與工作

若要存取可用範本，請在 Microsoft Power Apps 系統管理中心選取 **專案**，然後選取右上角的 **新增專案** 以選取公用範本。

下列範本與基礎工作會用來將專案實際值從 Project Service Automation 同步處理至 Finance：

- **資料整合中範本的名稱：** 專案實際值 (PSA 至 Fin 和 Ops)
- **專案中工作的名稱：**

    - 實際值
    - TransactionConnections

### <a name="entity-set"></a>實體集

| Project Service Automation | 財務                                   |
|----------------------------|----------------------------------------------------------|
| 實際值                    | 專案實際值的整合實體                   |
| 交易人脈    | 專案交易關聯的整合實體 |

### <a name="entity-flow"></a>實體流程

專案實際值是在 Project Service Automation 中進行管理，並同步處理至 Finance 中的專案整合日記帳。 會計系統將會根據預設財務維度和過帳設定來套用。

### <a name="prerequisites"></a>先決條件

實際值同步處理發生之前，您必須先設定 Project Service Automation 整合參數，並同步處理專案、專案工作以及專案費用交易類別。

### <a name="power-query"></a>Power Query

在專案實際值範本中，您必須使用 Microsoft Power Query for Excel 來完成這些工作：

- 將 Project Service Automation 中的交易類型轉換為 Finance 中的正確交易類型。 此轉換已經在「專案實際值 (PSA 至 Fin 和 Ops)」範本中定義。
- 將 Project Service Automation 中的帳單類型轉換為 Finance 中的正確帳單類型。 此轉換已經在「專案實際值 (PSA 至 Fin 和 Ops)」範本中定義。 然後，根據 **Project Service Automation 整合參數** 頁面上的設定，將帳單類型對應至明細屬性。
- 篩選為必須與此範本同步處理的特定資源組織單位。
- 如果公司間時間或公司間費用實際值會同步處理至 Finance，您必須將合約組織單位轉換為 Finance 中的正確法律實體。 在「專案實際值 (PSA 至 Fin 和 Ops)」範本中，根據示範資料定義條件欄。 您必須將上次插入的條件欄更新為正確的法律實體。 否則，可能會發生整合錯誤，或者可能會將不正確的實際值交易匯入至 Finance 中。
- 如果公司間時間或公司間費用實際值不會同步處理至 Finance，就必須從範本中移除上次插入的條件欄。 否則，可能會發生整合錯誤，或者可能會將不正確的實際值交易匯入至 Finance 中。

#### <a name="contract-organizational-unit"></a>合約組織單位
若要更新範本中插入的條件欄，請按一下 **對應** 箭頭以開啟對應。 選取 **進階查詢和篩選** 連結以開啟 Power Query。

- 如果您使用的是預設專案實際值 (PSA 至 Fin and Ops) 範本，請在 Power Query 的 **已套用的步驟** 區段中選取最後一個 **插入的條件**。 在 **函數** 項目中，將 **USSI** 取代為應與整合搭配使用的法律實體名稱。 視需要將其他條件新增至 **函數** 項目，並將 **否則** 條件從 **USMF** 更新為正確的法律實體。
- 如果要建立新範本，您必須新增該欄才能支援公司間的時間與費用。 選取 **新增條件欄**，並輸入該欄的名稱，例如 **LegalEntity**。 輸入該欄的條件，如果 **msdyn\_contractorganizationalunitid.msdyn\_name** 是 \<organizational unit\>，則為 \<enter the legal entity\>；否則為 Null。

### <a name="template-mapping-in-data-integration"></a>資料整合中的範本對應

下圖顯示資料整合中的範本工作對應範例。 此對應顯示會從 Project Service Automation 同步處理至 Finance 的欄位資訊。

[![範本對應 - 實際值。](./media/ActualsMapping.jpg)](./media/ActualsMapping.jpg)

[![範本對應 - 交易人脈。](./media/TransactionConnections.jpg)](./media/TransactionConnections.jpg)

## <a name="import-from-staging-table-after-integration-from-project-service-automation"></a>從 Project Service Automation 整合之後從暫存表格匯入

[從暫存表格匯入] 定期程序必須在實際值從 Project Service Automation 同步處理後執行。 此程序會將專案交易從暫存表格匯入至 Project Service Automation 整合日記帳，其中會套用會計功能，並且可以過帳匯入的交易。 建議您在批次模式下執行此程序；您可以選擇性將此程序設定為以定期批次方式執行。

## <a name="update-actuals-from-finance"></a>從 Finance 更新實際值

### <a name="template-and-tasks"></a>範本與工作

以下範本及基礎工作會用於將已過帳專案交易的憑單編號和銷售稅金，從 Finance 同步處理至Project Service Automation：

- **資料整合中範本的名稱：** 專案實際值更新 (Fin Ops 至 PSA)
- **專案中工作的名稱：**

    - 實際值 
    - TransactionConnections

### <a name="entity-set"></a>實體集

| 財務                                                  | Project Service Automation |
|----------------------------------------------------------|----------------------------|
| 專案實際值的整合實體                   | 實際值                    |
| 專案交易關聯的整合實體 | 交易人脈    |

### <a name="entity-flow"></a>實體流程

專案實際值是在 Project Service Automation 中進行管理，並同步處理至 Finance 中的專案整合日記帳。 在 Finance 中過帳實際值之後，這些實際值會在 Project Service Automation 中更新為 Finance 中的憑單編號。 如果在 Finance 中新增了銷售稅金，則會在 Project Service Automation 中建立新的稅金實際值。

### <a name="power-query"></a>Power Query

在專案實際值更新範本中，您必須使用 Power Query 來完成這些工作：

- 將 Finance 中的交易類型轉換為 Project Service Automation 中的正確交易類型。 此轉換已經在「專案實際值更新 (Fin Ops 至 PSA)」範本中定義。
- 將 Finance 中的帳單類型轉換為 Project Service Automation 中的正確帳單類型。 此轉換已經在「專案實際值更新 (Fin Ops 至 PSA)」範本中定義。

### <a name="template-mapping-in-data-integration"></a>資料整合中的範本對應

下圖顯示資料整合中的範本工作對應範例。 此對應顯示會從 Finance 同步處理至 Project Service Automation 的欄位資訊。

[![範本對應 - 實際值更新。](./media/ActualsUpdateMapping.jpg)](./media/ActualsUpdateMapping.jpg)

[![範本對應 - 交易更新。](./media/TransactionConnectionsUpdate.jpg)](./media/TransactionConnectionsUpdate.jpg)


[!INCLUDE[footer-include](../includes/footer-banner.md)]