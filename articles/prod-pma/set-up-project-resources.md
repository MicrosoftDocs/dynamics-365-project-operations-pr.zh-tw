---
title: 設定專案資源
description: 本主題提供有關設定或要求專案資源的資訊。
author: Yowelle
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjProjectsListPage
audience: Application User
ms.reviewer: johnmichalak
ms.custom: 82022
ms.assetid: bd2fb375-84c6-428a-8e54-f0f719045898
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a9af71fe0638a5601ded3f0e80301ae5dfa198c1
ms.sourcegitcommit: 2c2a5a11d446adec2f21030ab77a053d7e2da28e
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2022
ms.locfileid: "8682565"
---
# <a name="set-up-project-resources"></a>設定專案資源

[!include [banner](../includes/banner.md)]

您必須設定行事曆，並將其與員工或工作者建立關聯。 行事曆會用來排定專案以及專案所保留資源的工作時間。 在行事曆設定期間，專案經理可以在資源最佳化的過程中進行資源撫平。 根據行事曆排程，可以對資源加以限制。 您可以在 **行事曆** 頁面上設定行事曆。

將工作者設定為專案資源時，您可以選取任職於資源需要進行設定之公司中的工作者。 或者，也可以從您組織中的其他公司選取工作者。 這些工作者稱為公司間的資源。

下列程序說明如何將工作者設定為公司中的專案資源，以及如何設定公司間的專案資源。

## <a name="set-up-a-worker-as-a-project-resource"></a>將工作者設定為專案資源

1. 在 **工作者** 頁面的 **工作者** 清單中，選取您要新增為專案資源的工作者，然後開啟工作者記錄。
2. 在動作窗格中，選取 **專案** &gt; **設定** &gt; **專案設定**。
3. 選取行事曆，然後關閉頁面。

您也可以將資源的預設專案指定為預先指派的類型。 當資源管理員或專案經理預先知道資源要處理哪些專案時，可以使用預先指派。 也可以根據專案贊助者或客戶的要求使用預先指派。 若要預先指派專案，請在 **指派專案** 頁面的 **專案** 索引標籤上，從 **剩餘專案** 清單中選取適當的專案。

## <a name="set-up-an-intercompany-resource"></a>設定公司間的資源

將工作者設定為公司間的資源時，您在出借公司和借用公司中都必須完成設定。

### <a name="in-the-lending-company"></a>在出借公司中

1. 在 Finance 中，確認已選取出借公司，然後完成上一節「將工作者設定為專案資源」中的程序。
2. 在 **公司間會計** 頁面，選取 **新增**。
3. 在 **法律實體識別碼** 欄位中，選取出借公司。 適當填入剩餘欄位，然後選取 **儲存**。
4. 在 **轉撥價格** 頁面，選取 **新增**。
5. 在 **借用法律實體** 欄位中，選取適當的公司。
6. 若只要出借您在本節開始時所建立的資源給借用公司，請在 **資源** 欄位中，選取您所建立資源的名稱。 若要讓出借公司的所有資源皆可供借用公司使用，請讓 **資源** 欄位保持空白。
7. 在 **專案管理與會計參數** 頁面的 **公司之間** 索引標籤上，將 **啟用公司間的資源排程和時程表** 選項設定為 **是**。

### <a name="in-the-borrowing-company"></a>在借用公司中

- 在 **資源清單** 頁面的搜尋篩選中，輸入出借公司所建立資源的名稱，以確認該名稱是否已包含在借用公司的資源清單中。

## <a name="request-project-resources"></a>要求專案資源
專案資源排程的功能只能讓資源管理員在業務開發或專案上發佈人員配置資源。 若要啟用此功能，請完成下列工作，或確認這些工作是否已完成：

- 設定編號序列。
- 設定專案管理與會計工作流程。
- 啟用資源要求工作流程。

完成上述工作之後，您可以視需要完成下列工作：

- 從未確認預約的人員配置資源建立資源要求。
- 監視資源要求。
- 履行資源要求。
- 從 WBS 要求人員配置資源。
- 在沒有要求人員配置資源的情況下，將資源預約給專案。


[!INCLUDE[footer-include](../includes/footer-banner.md)]