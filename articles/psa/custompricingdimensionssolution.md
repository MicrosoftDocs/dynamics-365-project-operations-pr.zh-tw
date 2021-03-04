---
title: 建立自訂定價維度解決方案
description: 本主題說明如何在建立自訂定價維度時建立自訂解決方案。
author: Rumant
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 10/01/2020
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
ms.openlocfilehash: 3810df9b875d017a8d639b5253b96275571898f3
ms.sourcegitcommit: 418fa1fe9d605b8faccc2d5dee1b04b4e753f194
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/10/2021
ms.locfileid: "5144628"
---
# <a name="create-custom-solutions-for-pricing-dimensions"></a>建立自訂定價維度解決方案

[!include [banner](../includes/psa-now-project-operations.md)]

> [!IMPORTANT]
> 所有自訂定價維度變更都必須是在另一個的解決方案中。 這個重要的最佳做法提供您日後視需要更新或移除變更的彈性、有助於重複使用您的工作，以及讓您更便於將這些變更移植到另一個執行個體。 進行必要變更之後，將此解決方案匯出為 **受管理的解決方案**，再將其匯入至其他執行個體，即可重複使用您的定價設定。

1. 選取 **設定** > **解決方案**，然後選取 **新增**。 
2. 將解決方案命名為 **\<your organization name> 定價維度**、輸入其餘必要資訊，然後選取 **儲存**。

> ![建立自訂定價維度解決方案](media/Creation-of-custom-pricing-dimension-solution.PNG)
  
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>將所有必要的實體及相關元件新增至定價維度解決方案
您必須將下列 Project Service 實體新增至您的定價方案。 完成此程序中的步驟，在定價方案中進行一些重要的結構描述變更，讓實體得知新的定價維度。

1. 選取 **設定** > **解決方案**，然後按兩下 **\<your organization name> 定價維度**。 
2. 在方案總管的左導覽窗格中，選取 **新增現有的** >  **實體**。
3. 在 **解決方案元件** 對話方塊中，選取下列實體：

- 實際
- 可預約資源
- 估計明細
- 專案工作
- 發票明細詳細資料
- 帳目明細
- 專案合約服務內容詳細資料
- 專案團隊成員
- 報價明細詳細資料
- 角色價格加成
- 角色價格 
- 時間項目 

> ![將現有實體新增至定價維度解決方案](media/Existing-entities-to-PD-solution.png)

> ![選取解決方案元件](media/Dimension-Components.png)

> [!NOTE]
> 請務必包含所選每個實體的所有表單和檢視表。

4. 系統提示您包含所選實體的任何相依實體時，選取 **否**。

> ![不要包括所有相關元件。](media/Do-not-include-required.png)


