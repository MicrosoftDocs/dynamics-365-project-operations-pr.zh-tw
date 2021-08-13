---
title: 將轉包商設定為可預約資源
description: 本主題說明如何設定和維護從系統中使用者及連絡人所建立的轉包商資源，讓他們可以與 Microsoft Dynamics 365 Project Operations 中的轉包合約建立關聯。
author: rumant
ms.date: 07/28/2021
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c765e3c423e440f092c92f9bab75304914b0609447f1dc1c014f98801561b7a6
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6994176"
---
# <a name="set-up-subcontractors-as-bookable-resources"></a>將轉包商設定為可預約資源

[!include [banner](../../includes/dataverse-preview.md)]

_**適用於：** 精簡部署 - 交易至開立預估發票_

依照下列步驟，將轉包商設定為 Microsoft Dynamics 365 Project Operations 中的可預約資源。

1. 移至 **專案** \> **資源**，然後選取 **新增**。
2. 在 **新增可預約資源** 頁面的 **資源類型** 欄位中，選取下列其中一個選項：

    - **使用者** – 如果轉包商必須存取 Project Operations 以輸入時間或費用，請選取此資源類型。 如果選取 **使用者**，則轉包商需要有效的授權，才能存取系統。
    - **連絡人** 或 **客戶** – 如果轉包商不需要存取 Project Operations，但必須可供專案上的工作指派或預約使用，請選取這其中一個資源類型。 這兩個資源類型都無法提供系統的存取權。 選取 **客戶**，以可預約資源的身分來代表廠商的公司。 選取 **連絡人**，可代表廠商的個別員工。

3. 視選取的資源類型而定，系統會提示您選取對應的使用者、客戶或連絡人記錄。
4. 在 **工作者類型** 欄位中，選取 [合約工作者] 以將轉包商設定為可預約資源。

    > [!NOTE]
    > 如果讓 **工作者類型** 欄位保留空白，則會將可預約資源視為員工。

5. 如果已選取 **合約工作者** 做為工作者類型，請選取資源任職所在的廠商。
6. 選取資源的時區，然後選取 **儲存**。 若要將工作時數範本指派給可預約資源，您可以在 **可預約資源** 清單頁面上選取 **設定行事曆**。

為了與轉包合約服務內容建立關聯，可預約資源必須符合下列條件：

- 可預約資源必須是合約工作者。
- **連絡人** 資源類型的可預約資源必須與類型為連絡人的廠商帳戶建立關聯。 **使用者** 資源類型的可預約資源不需要與類型為連絡人的廠商帳戶建立關聯。
- **廠商** 欄位的可預約資源值必須與轉包合約的 **廠商** 欄位的值相符。

## <a name="update-the-type-of-worker-and-vendor-mapping-for-bookable-resources"></a>更新可預約資源的工作者類型及廠商對應

可預約資源的 **工作者類型** 欄位可判斷可預約資源是合約工作者還是員工。 **廠商** 欄位定義與可預約資源有關聯的廠商帳戶。 您將可預約資源與類型為連絡人的廠商建立關聯，即表示該連絡人是廠商公司的員工。

如果變更可預約資源的 **工作者類型** 及 **廠商** 欄位，則這些變更會影響日後任何對可預約資源所建立之新記錄 (例如時間項目) 進行的驗證。 不過，這些變更並不會使現有記錄失效。

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
