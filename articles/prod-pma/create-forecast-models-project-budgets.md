---
title: 建立專案預算的預測模型
description: 本主題說明如何為剩餘預算建立預測模型。
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073132"
---
# <a name="create-forecast-models-for-project-budgets"></a>建立專案預算的預測模型 

[!include [banner](../includes/banner.md)]

本主題說明如何為剩餘預算建立預測模型。 受預算控制的專案會使用兩種類型的預算：原始和剩餘。 建立專案預算時，您必須指定已在 **預測模型** 頁面中建立的原始及剩餘預算預測模型。 當您認可專案預算時，系統會根據指定的模型建立專案預算。

> [!NOTE]
> 預算控制所用的預測模型不能有子模型，也不可做為子模型。

1. 選取 **專案管理與會計** > **設定** > **預測**  > **預測模型** 。
2. 選取 **新增** 建立新的預測模型，然後輸入新模型的模型識別碼及名稱。 
3. 將 **已停止** 選項設定為 **是** ，以防止對預測模型的預測明細進行任何變更。 
4. 如果與模型相關的預測明細應在總帳中產生現金流預測，請將 **包含在現金流預測中** 設定為 **是** 。 
5. 若要使用專案日期做為發票日期，請將 **預測發票日期** 設定為 **是** 。 
6. 在 **預算類型** 欄位中，選取下列其中一個模型類型：

   - **原始預算** ：使用建立和核准初始預算時所認可的原始預算金額。
   - **剩餘預算** ：使用專案生命週期中的剩餘預算金額。 此預測模型中的餘額會根據實際交易減少，並隨預算修正增減。
   - **結轉** ：使用專案的結轉預算金額。 [結轉] 是選用程序，可執行以將未使用的預算金額從一個會計年度移轉至另一個。

7. 視需要設定下列選項：

   - 啟用 **預測發票日期** 以使用專案日期做為發票日期。
   - 啟用 **使用 WIP 進行預測** 以根據進行中工作 (WIP) 進行預測，然後選取 WIP 類型。 
   - 您可以保留預設為 **無** 的 **預算類型** ，或輸入新的類型。 變更記錄之後，您就無法變更預算類型。     
    > [!NOTE]
    > 如果您變更預設預算類型，則所有其他選項都會無法用於更新，而且您也無法重複使用此預測模型。 
   


 



[!INCLUDE[footer-include](../includes/footer-banner.md)]