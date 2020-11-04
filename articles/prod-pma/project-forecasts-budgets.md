---
title: 專案預測和預算
description: Microsoft Dynamics 365 Finance 提供專案預測和專案預算來管理和控制您的專案。
author: Yowelle
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ForecastModel, ProjYearEndProcess
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 23501
ms.assetid: 4e6d1384-19a2-4232-b3f3-d2590c218bd7
ms.search.region: Global
ms.author: andchoi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f99c00effbb0678f1f55e5068a7128cbfb86f5ce
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073109"
---
# <a name="project-forecasts-and-budgets"></a>專案預測和預算

[!include [banner](../includes/banner.md)]

有兩種方法可以管理和控制您的專案：專案預測和專案預算。 

如果您的組織有運營層面的遠景，並且重視源自特定交易的營收和成本時，您可以使用預測。 如果組織更多側重於財務金額，則使用專案預算。 

專案預測與專案預算都會使用預測模型來掌握預計交易金額。 

每個方法各有其優點。 為組織選擇方法之前，您應該先考慮下列幾點。

|   配置方法       |           專案預測            |        專案預算                           |
|---------------------------|------------------------------------------|----------------------------------------------------|
| **期間配置**     | 您不可在會計週期內明確配置交易。 反而是，根據專案的生命週期建立預測和控制預測。 因為預測是根據特定日期進行，您必須從日期推斷期間。 | 您可以在整個專案或會計週期內配置交易。 如果您在某段期間進行配置，則可以將未使用的金額結轉到下一個會計週期。 |
| **檢視交易**  | 您可以在預測表單中檢視交易，您可以在其中查看整個公司和所有專案的預測，而不考慮階層為何。 為了專注於特定專案，您必須篩選資料。                                       | 您可以檢視單一專案階層的預算交易。 因此，可以檢視上層專案或其子專案的交易詳細資料。                 |
| **交易變數** | 輸入預測交易時，您可以使用實際交易所存在的每個屬性。 這樣預測中就可以有更多詳細資料。 例如，您可以輸入數量、工作者、項目或明細屬性的詳細資料。         | 輸入預算詳細資料時，您只能使用金額、類別和活動。                    |
| **安全性**              | 預測是根據您在預測表單中輸入的交易所建立，並不涉及程序控制機制。 任何具有預測表單權限的工作者，都無需核准即可修訂資訊。                                        | 預算使用工作流程系統，這會啟用變更管理，讓您保留修訂歷程記錄。         |
| **項目類型**           | 預測交易項目是根據單位數目以及成本價和銷售單價所建立。  | 預算詳細資料是根據金額 (在成本與營收之間分割) 所建立。                                          |
| **預測模型**       | 因為每個預測都必須與一個模型相關聯，您可以建立多個預測模型，也可以設定子模型。           | 專案預算會限制用於編列預算的預測模型。 較少的預測模型可以協助增進推測的一致性。                           |
| **成本超支**         | 您只能允許或禁止輸入會導致成本超支的交易。   | 專案預算功能為使用者提供其他控制選項。 您可以允許警告和超支。                    |
| **控制項**               | 預測控制是使用預測扣減來執行。 實際金額沒有任何稽核線索，也會從預測交易餘額中減去。 這會讓實際交易發生位置的追蹤更加困難。                   | 在專案預算控制中，會從剩餘預算的金額中減去實際金額。 這樣可讓稽核線索更清楚。                                   |

## <a name="project-forecasts"></a>專案預測
使用專案預測時，您可以在預測表單中針對每個交易類型輸入預測交易。 每個適用於實際交易的屬性都可用於預測交易 置 (例如，明細獲利率、明細屬性、工作者或描述)。 您也可以推估發生成本後經過多久時間，才會開立發票給客戶。 

專案預測交易記錄是根據單位和金額所建立。 

您必須將每個專案預測與一個預測模型建立關聯。 當您輸入預測交易時，系統會自動建議預測模型。 預測模型可當做預測交易的容器。 

您可以將預測模型指定為模型的子模型。 這可讓您依地區、時段或部門進行預測。 您可以複製模型中的預測交易來建立新模型，也可以將交易轉移至總帳。 因為預測與模型之間有一對一關聯，每個預測模型都會為專案建立不同的預算。 

預測模型可以使用預測扣減做為專案的控制機制。 在預測扣減中，實際交易會減少預測交易餘額。 不過，預測扣減是套用至階層中最上層的專案，因此只能對預測中的變化提供有限的觀點。 例如，如果工作者與子專案有關聯，則該工作者的實際交易會過帳至上層專案。 這可能讓追蹤變更難以進行，因為您無法輕易判斷哪些交易在子專案中造成對預測金額的扣減。 因此，您最好建立預測模型的複本以作預測扣減之用。 您可以接著使用報表來檢視原先預測的內容。 

您可以修訂、複製、刪除專案預測，或將其轉移至總帳預算。 不過，其中沒有程序控制。 任何具有預測表單權限的工作者，都無需審查即可進行修訂。

-   **修訂** – 您可以在建立原始項目所在的那個表單中修訂預測交易。
-   **複製或刪除** – 複製預測交易時，您可以將一個預測模型的交易明細複製到另一個預測模型。 刪除預測時，您會從預測模型中刪除預測交易。 若要限制複製或刪除的預測交易，請選取特定交易類型和日期。 這可讓您只複製或刪除預測的特定部分。
-   **轉移** – 將專案預測轉移到總帳預算時，您會將預測模型的預測交易轉移到總帳預算。 您可以在轉移專案預測所到的總帳預算中，覆寫任何先前轉移的交易。

## <a name="project-budgets"></a>專案預算
專案預算功能是比預測功能更為簡單的方法，雖然確實與預測模型整合在一起。 此功能使用單一輸入表單取得原始預算詳細資料和修訂，並允許僅根據金額、類別或活動進行推測。 

在專案預算中，所有原始預算和修訂必須傳送至專案工作流程進行核准。 工作流程提供您更大的程序控制能力，並且會建立變更歷程記錄。 

專案預算編列類似於總帳預算編列，但是設定起來更快、更輕鬆。 總帳預算中的許多選項 (例如數字序列或貨幣) 不一定是單獨針對專案進行設定。

專案預算會自動與兩個預測模型建立關聯，一個用於原始預算，另一個用於剩餘預算。 因此，基於預測模型建立的報表可以使用預算資料。 認可專案預算時，系統會根據相關聯的模型 (用於報表和控制目的) 建立預測交易。

## <a name="forecast-models"></a>預測模型
預測模型具有單層階層。 這表示一個專案預測必須與一個預測模型建立關聯。

如果您使用專案預測，則可以將模型識別為子模型。 您可以接著依部門、時段或地區分別建立預測。 例如，您可以建立一年的預測模型，然後針對區域負責人提交的東北、東南、西北和西南地區預測建立子模型。 您可以選取可用報表中的不同選項，依總預測或依子模型來檢視資訊。


