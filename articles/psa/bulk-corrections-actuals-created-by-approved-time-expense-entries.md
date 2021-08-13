---
title: 大量更正由核准時間和費用分錄所建立的實際值
description: 本主題說明系統管理員如何對先前核准的時間或費用分錄進行單一或大量更正 (如果計費未完成)。
author: rumant
ms.date: 04/02/2020
ms.topic: article
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: rumant
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
search.app:
- ProjectOperations
ms.openlocfilehash: 88706946e5c5c59be996640f4c7b37e958c1cf1d9fd14c72c0c6dc854a77dab4
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6995391"
---
# <a name="bulk-corrections-of-actuals-created-by-approved-time-and-expense-entries"></a>大量更正由核准時間和費用分錄所建立的實際值

[!include [banner](../includes/psa-now-project-operations.md)]

時間或費用分錄有時可能會輸入不正確。 例如，顧問可能會在建立時間分錄時選取錯誤的日期，或在輸入費用時顛倒數字順序。 如果顧問無法對已提交的分錄進行更新，管理員可以直接更正專案的分錄。

若要完成本主題中的程序，您需要系統管理員權限。

## <a name="correct-approved-time-entries"></a>更正核准的時間分錄     

完成下列步驟以更正專案的單一或多個時間分錄。

1. 在 **銷售** 區域中，選取 **交易**，然後選取 **核准的時間**。 

2. 在 **核准的時間** 清單中，尋找並選取一個或多個要更正的已核准時間分錄。 您可以使用篩選來找出相關的分錄。 例如，您可能會根據專案識別碼進行篩選，然後選取所有具有該專案識別碼的已核准時間分錄。

3. 選取 **更正分錄**。 系統會自動使用指派的類型 **時間更正** 建立新的更正帳目。 您選取的分錄會新增至此帳目。 

4. 在 **新增帳目** 頁面上，輸入更正帳目的 **描述**，然後選取 **時間分錄更正** 索引標籤。  
5. 在 **時間分錄的新值** 區段中，視需要以正確的資訊來更新欄位。 例如，您可以變更指派的專案或可預約資源。

6. 選取 **預覽**。 在對話方塊中選取 **確定**。 在 **帳目明細** 索引標籤中，您可以檢視與所選已沖回時間分錄相關的原始實際值清單以及所建立已更正的對應明細。 如果需要進行其他更正，請重複步驟 5 和 6。 

> [!NOTE]
> 所有已更正的實際值都會有與您在 **時間分錄的新值** 區段中所選值相同的值。

7. 如果更正結果顯示如預期，請選取 **確認**。 在對話方塊中選取 **確定**。

8. 返回 **銷售** 區域、選取 **專案**，然後開啟您剛為其更新時間分錄的專案。 

9. 在 **專案** 頁面的 **實際值** 索引標籤上，檢視您所進行的變更。 

> [!NOTE]
> 如果看不到 **實際值** 索引標籤，請選取 **相關** > **實際值**。  

10. 在 **實際值相關檢視表** 清單中，您可以看到仍然列出已沖回的原始時間分錄，就像是對應的已更正時間分錄一樣。 

例如，下圖有兩個數量為 8.00 的明細項目，在 [金額] 欄中列出借記。 此外，還有兩項數量為 -8.00 的明細項目，在 [金額] 欄中顯示貸記金額。 這些更正會將數量顯示為零。

![實際值相關檢視表清單。](https://github.com/MicrosoftDocs/dynamics-365-customer-engagement-pr/blob/bulk-corrections-actuals-created-by-approved-time-expense-entries.md/time-actuals.png)
 
## <a name="correct-approved-expense-entries"></a>更正核准的費用分錄

完成下列步驟，以更正一個或多個費用分錄。 

1. 在 **銷售** 區域的左導覽窗格中，選取 **交易** 底下的 **核准的費用**。

2. 在 **核准的費用** 清單中，選取您要更正的專案，然後選取 **更正分錄**。 系統會自動使用指派的類型 **費用更正** 建立新的更正帳目。 

3. 在 **新增帳目** 頁面上，輸入更正的 **描述**，然後在 **費用更正** 索引標籤的 **費用的新值** 區段中，選取要針對所選費用明細進行更正的資料欄位。 例如，您可以將費用指派給其他 **專案**，或是更正 **費用類別**、**費用日期** 或 **可預約資源**。

4. 選取 **預覽**。 在對話方塊中選取 **確定**。 

5. 確認 **帳目明細** 索引標籤上的更新結果。您可以檢視與所選已沖回費用分錄相關的原始實際值清單以及所建立已更正的對應明細。

6. 如果更正的值符合預期，請選取 **確認**。 在對話方塊中選取 **確定**。 如果值顯示未如預期，請選取 **取消** 以返回 **核准的費用** 清單。 重複步驟 2 到 5。 

> [!NOTE]
> 已更正的實際值會有與您在 **費用的新值** 區段中所選值相同的值。

7. 確認更正帳目之後，瀏覽回到您所更新的專案，以檢視您的變更。  

8. 在專案頁面的 **實際值** 索引標籤上，檢閱 **實際值相關檢視表**。 原始分錄和更正分錄會列出。 下圖顯示原始費用分錄金額以及對應的已更正費用分錄金額。 

![費用實際值。](https://user-images.githubusercontent.com/60806505/77122219-4cd52900-69fa-11ea-8349-ccd2ffebf640.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]