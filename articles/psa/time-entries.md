---
title: 建立時間項目
description: 此主題提供有關如何建立時間項目的資訊。
author: rumant
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.reviewer: johnmichalak
ms.openlocfilehash: 4b8f88da372cd56b19bed82ad6918da6ddd6f202
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8593510"
---
# <a name="create-time-entries"></a>建立時間項目

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

在舊版 Dynamics 365 Project Service Automation 中，時間項目是以週為單位輸入。 在 Project Service Automation 版本 3 中，則按每日單位輸入時間項目。 不過，在建立幾個時間項目之後，您可以大量建立或複製這些項目。

## <a name="create-a-time-entry"></a>建立時間項目

依照下列步驟建立建立時間項目。

1. 在 **時間項目** 頁面，選取 **新增**。
2. 在 **快速建立：時間項目** 對話方塊中，以分鐘、小時或天為單位輸入時間項目的期間。 期間必須以下列格式來輸入：*x* 分鐘、*x* 小時或 *x* 天。 時數和天數也可以輸入成小數值，例如 *x.x* 小時或 *x.x* 天。
3. 選取時間項目類型和您要輸入時間項目的專案。
4. 在 **專案工作** 欄位中，尋找此時間項目的工作。

    > [!NOTE]
    > 如果您要為未指派給使用者的工作建立時間項目，請選取 **專案工作** 欄位中的 **搜尋** 按鈕、選取 **變更檢視表**，然後選取 **所有使用中專案工作** 以列出所有工作。

5. 輸入描述 (如果需要描述)，然後選取 **儲存後關閉**。

建立並儲存時間項目之後，您可以在時間輸入網格中進行編輯。 時間輸入網格支援兩種格式：

- 您可以輸入 **hh:mm** 格式的時間項目。 這種格式會接著轉換為時數和分數。
- 您可以直接輸入時數和分數。

請注意，小時的分數並不是分鐘。 因此，1.5 小時代表 1 小時 30 分鐘。 同樣的規則也適用於天的分數。 一天為 24 個小時，而 0.5 天即表示 12 個小時。

## <a name="bulk-create-time-entries"></a>大量建立時間項目

建立幾個時間項目之後，您可以使用複製這些項目以大量建立其他時間項目。

1. 在 **時間項目** 頁面上，選取 **複製週次**。
2. 在 **開始期間** 欄位群組中，使用 **開始日期** 和 **結束日期** 欄位來定義要從中複製時間項目的日期範圍。
3. 在 **結束期間** 欄位群組的 **開始日期** 欄位中，指定建立時間項目的日期。
4. 選取 **複製** 以建立與 **結束期間** 欄位群組所指定星期幾相對應的時間項目複本。 例如，將上週星期一的時間項目複製到 **結束期間** 欄位群組所指定之週的星期一。

## <a name="import-data-for-time-entries"></a>匯入時間項目的資料

您可以從專案預約和指派匯入資料。 匯入資料時，您可以指定要匯入的預約日期範圍，然後明確選取應建立為 **草稿** 時間項目的預約。

## <a name="group-by-sort-search-and-filter-capabilities"></a>群組依據、排序、搜尋及篩選功能

您可以依據欄中指定的維度來分組和篩選時間項目。 在 **群組依據** 欄位中，選取要用來篩選時間項目的維度。 您也可以使用欄標題上的排序箭頭，依遞增或遞減順序排序時間項目記錄。 此外，還可以選取欄標題上的 **篩選** 按鈕來顯示或隱藏項目，然後在 **搜尋** 方塊中輸入要依據專案名稱、專案工作、時間項目或資源用來搜尋時間項目的文字。


[!INCLUDE[footer-include](../includes/footer-banner.md)]
