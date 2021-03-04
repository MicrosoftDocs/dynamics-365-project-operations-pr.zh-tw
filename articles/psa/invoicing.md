---
title: 在 Project Service Automation 中開立發票
description: 本主題提供有關開立發票的資訊。
author: rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 08/03/2020
ms.topic: article
ms.service: business-applications
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 0855e85c1f09d29d3ecb49ba517fd3043ae11140
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5151378"
---
# <a name="invoicing-in-project-service-automation"></a>在 Project Service Automation 中開立發票

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在 Dynamics 365 Project Service Automation 中開立發票非常有用，因為這可讓專案經理在為客戶建立發票前有另一層級的核准。 第一層核准是在專案團隊成員送出的時間和費用項目經過核准時完成。

PSA 不是為了產生客戶面向發票而設計，原因如下：

- 其中未包含稅務資訊。
- 無法使用正確設定的匯率，將其他貨幣轉換為發票貨幣。
- 無法正確格式化發票，以供列印。

但您可以改用財務或會計系統來建立客戶面向發票，使用 PSA 所產生發票提案中的資訊。

## <a name="creating-project-invoices-in-psa"></a>在 PSA 中建立專案發票

您可以一次建立一份專案發票，或是大量建立。 您可以手動建立專案發票，也可以進行設定以便在自動執行中產生。

### <a name="manually-create-project-invoices-in-psa"></a>在 PSA 中手動建立專案發票

從 **專案合約** 清單頁面，您可以分別為每個專案合約建立專案發票，或者可以為多個專案合約大量建立發票。

依照此步驟，建立特定專案合約的發票。

- 在 **專案合約** 清單頁面上，開啟專案合約，然後選取 **建立發票**。

    ![建立特定專案合約的專案發票](media/CreateProjectInvoicesOneByOne.png)

    發票會針對狀態為 **已準備好開立發票** 的所選專案合約的所有交易來產生。 這些交易包括時間、費用、里程碑和產品型合約服務內容。

請依照下列步驟大量建立發票。

1. 在 **專案合約** 清單頁面上，選取一個或多個您必須為其建立發票的專案合約，然後選取 **建立專案發票**。

    ![大量建立專案發票](media/CreateProjectInvoicesBulk.png)

    出現一則警告訊息通知您，建立發票之前可能會有一段延遲。 也會顯示程序。

2. 選取 **確定** 以關閉訊息方塊。

    發票會針對狀態為 **已準備好開立發票** 的合約服務內容的所有交易來產生。 這些交易包括時間、費用、里程碑和產品型合約服務內容。

3. 若要檢視已產生的發票，請移至 **銷售**\>**帳務**\>**發票**。 您會看到每個專案合約的一份發票。

### <a name="set-up-automated-creation-of-project-invoices-in-psa"></a>在 PSA 中設定自動建立專案發票

請依照下列步驟，在 PSA 中設定自動化發票執行。

1. 移至 **Project Service** \> **設定** \> **批次工作**。
2. 建立批次工作，並將其命名為 **PSA 建立發票**。 批次工作的名稱必須包含「建立發票」一詞。
3. 在 **工作類型** 欄位中，選取 **無**。 **每日頻率** 和 **使用中** 選項預設會設定為 **是**。
4. 選取 **執行工作流程**。 在 **查詢記錄** 對話方塊中，您會看到三個工作流程：

    - ProcessRunCaller
    - ProcessRunner
    - UpdateRoleUtilization

5. 選取 **ProcessRunCaller**，然後選取 **新增**。
6. 在下一個對話方塊中選取 **確定**。 **睡眠** 工作流程後面會跟著 **程序** 工作流程。

    您也可以選取步驟 5 中的 **ProcessRunner**。 然後，當您選取 **確定** 時，**程序** 工作流程後面會接著 **睡眠** 工作流程。

**ProcessRunCaller** 和 **ProcessRunner** 工作流程會建立發票。 **ProcessRunCaller** 會呼叫 **ProcessRunner**。 **ProcessRunner** 是實際建立發票的工作流程。 它會處理所有需要建立發票的合約服務內容，然後為這些服務內容建立發票。 為了確定必須建立其發票的合約服務內容，工作會查看合約服務內容的發票執行日期。 如果屬於一個合約的合約服務內容具有相同的發票執行日期，則會將交易合併成一個有兩個發票明細的發票。 如果沒有要要建立其發票的交易，則工作會跳過發票建立作業。

**ProcessRunner** 執行完畢後，會呼叫 **ProcessRunCaller**、提供結束時間，然後關閉。 **ProcessRunCaller** 接著啟動計時器，從指定的結束時間開始執行 24 小時。 計時器結束時，會關閉 **ProcessRunCaller**。

用於建立發票的批次處理工作是週期性工作。 如果此批次處理已執行多次，就會建立工作的多個執行個體，並造成錯誤。 因此，您只能啟動批次處理一次，並且只有在其停止執行時才要重新啟動此工作。

> [!NOTE]
> Project Service Automation 中的批次開立發票只會針對發票排程所設定的專案合約服務內容執行。 使用固定價格計費方式的合約服務內容必須已設定里程碑。 使用時間和材料計費方式的專案合約服務內容必須設定以日期為依據的發票排程。 [報價和報價明細](basic-quote-lines.md#invoice-schedule)主題中已提供有關在以報價明細為根據之專案的內容中設定開立發票頻率的資訊。 這同樣適用於專案型合約服務內容。      
 
### <a name="edit-a-draft-psa-invoice"></a>編輯草稿 PSA 發票

建立草稿專案發票時，所有在時間及費用項目獲核准時建立的未開單銷售交易都會提取到發票上。 發票仍處於草稿階段時，您可以進行下列調整：

- 刪除或編輯發票明細詳細資料。
- 編輯和調整數量與帳單類型。
- 直接將時間、費用和服務費新增為發票上的交易。 如果發票明細對應至允許這些交易分類的合約服務內容，您可以使用此功能。

選取 **確認** 以確認發票。 確認動作是單向動作。 選取 **確認** 時，系統會設定發票為唯讀，並從每個發票明細的每個發票明細詳細資料建立已開單銷售實際值。 如果發票明細詳細資料參照未開單銷售，則系統還會沖回未開單銷售實際值。 (任何從時間或費用項目建立的發票明細詳細資料都會參照未開單銷售實際值)。總帳整合系統可以使用此沖回來反轉專案進行中工作 (WIP) 以作會計用途。

### <a name="correct-a-confirmed-psa-invoice"></a>更正已確認的 PSA 發票

已確認的 PSA 發票可加以編輯 (更正)。 更正已確認發票時，會建立新的草稿更正發票。 因為假設您要從原始發票中沖回所有交易和數量，此更正發票會包含原始發票中的所有交易，而其上所有數量皆為 0 (零)。

如果任何交易都不需要更正，您可以從草稿更正發票移除這些交易。 如果您想要沖回或回復部分數量，則可以編輯明細詳細資料上的 **數量** 欄位。 如果開啟發票明細詳細資料，您可以查看原始發票數量。 然後就可以編輯目前發票數量，使其小於或等於原始發票數量。

確認更正發票時，會沖回原始已開單銷售實際值，並建立新的已開單銷售實際值。 如果數量已減少，則差額也會導致建立新的未開單銷售實際值。 例如，如果原始已開單銷售是八小時，且更正發票明細詳細資料的數量已減少為六小時，則 PSA 會沖回原始已開單銷售明細，並建立兩個新的實際值：

- 六小時的已開單銷售實際。
- 剩餘兩個小時的未開單銷售實際值。 依據與客戶的協商，此交易可以稍後再開帳單，或標示為不應收費。
