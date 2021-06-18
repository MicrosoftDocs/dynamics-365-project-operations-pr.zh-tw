---
title: Microsoft Project Client 整合
description: 規劃和維護專案排程可能會很複雜，因此專案經理必須使用可協助他們管理這項工作的工具。 與 Microsoft Project Client 的整合可提供支援來開啟和管理專案分工結構圖。
author: Yowelle
ms.date: 12/11/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ProjWbsTemplate
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2017-12-04
ms.dyn365.ops.version: 7.2999999999999998
ms.openlocfilehash: 032d726bb6206c563b573f30d13fe2697a13c949
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5999436"
---
# <a name="microsoft-project-client-integration"></a>Microsoft Project Client 整合

[!include [banner](../includes/banner.md)]

規劃和維護專案排程可能會很複雜，因此專案經理必須使用可協助他們管理這項工作的工具。 與 Microsoft Project Client 的整合可提供支援來開啟和管理專案分工結構圖。 專案經理可以將任何變更發佈回 Dynamics 365 Finance 專案分工結構圖。

> [!NOTE]
> 如果您使用的是 7 月更新 (10.0.4 版)，則必須安裝 KB 4054797 和 4055884。

## <a name="configure-the-microsoft-project-client-add-in"></a>設定 Microsoft Project Client 增益集
若要啟用與 Microsoft Project Client 的整合，您必須在使用者的用戶端 Microsoft Project 應用程式中安裝 Microsoft Dynamics 365 增益集。 這可以藉由開啟 **專案管理工作區** 來完成。

•   在工作區的 **連結** > **設定** 區段中按一下 **設定 Project Client 增益集**。

•   按一下 **開啟**，然後在出現提示時按一下 **執行**。

## <a name="open-and-edit-an-existing-draft-work-breakdown-structure-in-microsoft-project-client"></a>在 Microsoft Project Client 中開啟並編輯現有的草稿分工結構圖
如果 Dynamics 365 Finance 中的專案已建立分工結構圖，且分工結構圖為草稿狀態，則可以在 Microsoft Project Client 應用程式中開啟該分工結構圖。 若要從 **專案** 頁面中開啟，請按一下 **計劃** 索引標籤中的 **在 Microsoft Project 中開啟** 連結。您也可以按一下 **Microsoft Dynamics 365** 索引標籤中的 **開啟**，從 Microsoft Project Client 應用程式中開啟此頁面。從清單選取 **實體** 和 **專案**。

> [!NOTE]
> 如果您使用的瀏覽器是 Internet Explorer，則需要按一下 **儲存**，以手動方式從下載檔案的位置開啟。 或者，按一下 **儲存後開啟**，以在 Microsoft Project Client 中開啟檔案。 不要在儲存時將將檔案名稱重新命名。

使用 Microsoft Project Client 對檔案進行編輯前，必須先將其簽出。按一下 **Microsoft Dynamics 365** 索引標籤中的 **簽出**。這可防止其他使用者同時從 Finance 中編輯分工結構圖。 若要在完成任何編輯後發佈分工結構圖，請按一下 **Microsoft Dynamics 365** 索引標籤上的 **簽入**。

如果已在 Finance 中新增專案團隊至專案，則會以團隊成員填入資源清單中。 如果尚未將專案團隊新增至專案，您可以按一下 **Microsoft Dynamics 365** 索引標籤上的 **資源** 按鈕選取資源，並在 Microsoft Project Client 中建立團隊。 

下列資料會在進行簽入程序時同步回到 Finance：

•   任務名稱

•   開始日期

•   完成日期

•   前置任務

Predecessors資源名稱

•   類別

•   資源類別

•   工作時數

•   附註

•   優先順序

> [!NOTE]
> 如果您將任何其他欄新增至 Microsoft Project Client 檔案，則這些欄不會儲存至此檔案，也不會在重新開啟檔案時顯示該檔案。

## <a name="create-the-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>使用 Microsoft Project Client 建立現有專案的分工結構圖
若要使用 Microsoft Project Client 建立新的分工結構圖，請依照下列步驟進行：


1.  開啟 Microsoft Project Client。

2.  在 **Microsoft Dynamics 365** 索引標籤中，按一下 **開啟**。

3.  選取專案的 **舊版實體**。

4.  選取 **專案**。

5.  按一下 **Microsoft Dynamics 365** 索引標籤上的 **簽出**。

6.  準備好發佈至 Finance 時，按一下 **Microsoft Dynamics 365** 索引標籤上的 **簽入**。

## <a name="replace-the-existing-work-breakdown-structure-for-an-existing-project-using-microsoft-project-client"></a>使用 Microsoft Project Client 取代現有專案的現有分工結構圖
若要使用 Microsoft Project Client 建立新的分工結構圖，並取代現有專案的現有分工結構圖，請依照下列步驟進行：

1.  開啟 Microsoft Project Client。

2.  在 Microsoft Project Client 中建立排程。

3.  在 **Microsoft Dynamics 365** 索引標籤中，按一下 **儲存變更** > **取代現有的專案**。

4.  選取專案的 **舊版實體**。

5.  選取 **專案**。

6.  按一下 **確定**。

## <a name="create-a-new-project-from-within-microsoft-project-client"></a>從 Microsoft Project Client 中建立新專案


1.  開啟 Microsoft Project Client。

2.  在 Microsoft Project Client 中建立排程。

3.  在 **Microsoft Dynamics 365** 索引標籤中，按一下 **儲存變更** > **儲存至新專案**。

4.  選取專案的 **舊版實體**。

5.  如有需要，輸入 **專案識別碼**。

6.  輸入 **專案名稱**。

7.  選取 **專案類型**、**專案群組** 和 **專案合約識別碼**。 或者，也可以按一下 **新增** 來建立新的專案合約。

8.  選取要用於資源分配的 **行事曆**。

11. 按一下 **確定**。


[!INCLUDE[footer-include](../includes/footer-banner.md)]