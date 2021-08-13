---
title: 建立自訂定價維度解決方案
description: 本主題提供如何為自訂定價維度建立解決方案的資訊。
author: Rumant
ms.date: 11/09/2020
ms.topic: article
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 753f0c4496bafd43d7e4a399cedeb355c2163c7ce56d932b2c786d5f2e672b6b
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6992196"
---
# <a name="create-a-solution-for-custom-pricing-dimensions"></a>建立自訂定價維度解決方案

 _**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_ 

>[!IMPORTANT]
>所有自訂定價維度變更都必須是在另一個的解決方案中。 這個重要的最佳做法提供您日後視需要更新或移除變更的彈性、有助於重複使用您的工作，以及讓您更便於將變更移植到另一個執行個體。 進行所有必要變更之後，將此解決方案匯出為 **受管理的** 解決方案，再將其匯入至其他執行個體即可重複使用。

## <a name="create-a-solution-for-custom-pricing-dimensions"></a>建立自訂定價維度解決方案

1.  選取 **設定** > **解決方案**，然後選取 **新增**。
2.  將解決方案命名為 *<your organization name> 定價維度*。
3. 輸入其餘必要資訊，然後選取 **儲存**。

  ![建立自訂定價維度解決方案。](./media/Creation-of-custom-pricing-dimension-solution.png)
 
## <a name="add-all-required-entities-and-related-components-to-the-pricing-dimension-solution"></a>將所有必要的實體及相關元件新增至定價維度解決方案

將下列 Project Service 實體新增至定價解決方案中，以在定價解決方案中進行重要的架構變更。 在您完成此程序之後，實體將會識別新的定價維度。

1.  選取 **設定** > **解決方案**，然後按兩下 **<*您的組織名稱*> 定價維度**。
2.  在方案總管的左導覽窗格中，選取 **新增現有的** >  **實體**。
3.  在 **解決方案元件** 對話方塊中，選取下列實體：
 
   - **實際**
   - **可預約資源**
   - **估計明細**
   - **專案工作**
   - **發票明細詳細資料**
   - **帳目明細**
   - **專案合約服務內容詳細資料**
   - **專案團隊成員**
   - **報價明細詳細資料**
   - **角色價格加成**
   - **角色價格**
   - **時間項目**
 
   ![新增現有實體自訂定價維度解決方案。](./media/Existing-entities-to-PD-solution.png)
 
 4. 針對每個實體，複查要新增的元件，以及每個實體的最終實體資產清單。 

   >[!NOTE]
   > 包含所選每個實體的所有表單和檢視表。

  ![已新增實體。](./media/solution-component-selection.png)


5.  當系統提示您包括所選取實體的任何相依實體時，請選取 **不，請勿包括必要元件**。

    ![包括相依實體。](./media/Do-not-include-required.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]