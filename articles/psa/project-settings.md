---
title: 專案設定
description: 本主題提供有關專案管理設定的資訊。
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 03/01/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: b2cda6bfd7f152ee948cf49fab91aed475968a09
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123098"
---
# <a name="project-settings"></a>專案設定

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

使用下列設定來存取專案規劃功能。

## <a name="work-template"></a>工作範本

為了建立專案排程，您會建立專案行事曆範本，以定義每天的工作時數以及所有公休日。 若要建立專案行事曆範本，您可以將工作範本與專案的 **行事曆範本** 欄位建立關聯。 依照下列步驟建立建立工作範本。

1. 在 PSA 的左導覽窗格中，按一下 **資源**。 
2. 在 **資源** 清單頁面上，開啟使用者記錄，然後選取 **顯示工作時數**。

  > [!NOTE]
  > 請確定您已允許瀏覽器頁面出現快顯。 這可讓您看到資源設定的工作時數。
  
3. 在 **每月檢視表** 索引標籤中，按一下 **設定**。 有三個選項的清單會出現： 

  - 新增每週排程
  - 一日工作行事曆
  - 休假

> ![設定選項](media/project-13.png)

4. 選取 **新增每週排程**，然後設定此資源排程的選項。 您可以設定週期性每週排程、每天時數參數、公休日等等。
5. 設定日期範圍、選取 **儲存**，然後按一下 **關閉**。 
6. 返回 **資源** 清單頁面，並選取您設定其工作時數的資源。 
7. 選取 **設定行事曆為** 以設定工作範本。 
8. 在 **工作範本** 對話方塊中輸入工作範本的名稱，然後選取 **套用**。 

您現在可以將工作範本與專案行事曆範本建立關聯。

## <a name="resource-roles"></a>資源角色

*資源角色* 一詞是指人員必須具備才能執行專案中一組特定工作的一組技能、專長和認證。 PSA 可讓您根據資源的關聯角色來為資源的時間估算成本並開單收費。 每個組織都必須使用 **Project Service** 功能表的左側導覽來設定這些角色。

每個組織都必須在 **使用中資源類別** 頁面上設定這些角色。 若要開啟此頁面，請選取左導覽窗格中的 **資源角色**。

## <a name="price-lists"></a>價目表

價目表可讓您針對組織中的資源角色、費用類別、產品及其他元素設定成本和售價。 設定必須為專案交付之工作的財務估計值之前，您應該建立支援成本和銷售價目表。 在參數區段中，您也應該設定套用至所有於組織建立之專案的預設成本和銷售價目表。 在 **使用中專案參數** 頁面上，確定您已設定預設成本和銷售價目表。
