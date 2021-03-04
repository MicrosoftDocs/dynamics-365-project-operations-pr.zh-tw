---
title: 核准概觀
description: 本主題提供有關在 Project Operations 中處理核准的資訊。
author: stsporen
manager: Annbe
ms.date: 10/05/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 14c6914cf9b5fb52e7554e51604e79f0920064df
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4123818"
---
# <a name="approvals-overview"></a>核准概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

時間及費用提交會在核准工作流程中移動。 項目獲核准後，會在實際值中記錄交易，或在排程中的預約時間。

## <a name="approvals-workflow"></a>核准工作流程
當您建立並送出時間或費用項目時，系統會建立核准項目。 專案核准者或您的經理會審查並核准您的項目。 如果此項目與專案相關，當該項目獲核准時，就會建立實際值。 這樣就可以追蹤成本和帳單。 

## <a name="approve-an-entry"></a>核准項目
**核准** 表單可讓您在不同的檢視表之間切換，以便檢視不同類型的核准。
  
1. 移至 **核准** 表單，並選取 **費用**、**時間** 或 **回收**。
2. 審查每個核准項目，並選取您要核准的項目。
3. 選取 **核准** 以核准選取的項目。
系統會處理這些項目，並建立實際值或預約。

## <a name="reject-an-entry"></a>拒絕項目
身為專案核准者，您可能需要將項目退送回使用者以進行更正。
  
1. 移至 **核准** 表單，然後選取要拒絕的項目。 
2. 選取 **拒絕**。
3. 選擇性 - 在 **拒絕註解** 對話方塊中新增留言，以告知使用者項目遭拒的原因。
4. 選取 **確定**。 將項目退回給使用者。
  
## <a name="recall-entries"></a>回收項目
有時，您可能需要回收已送出的項目。 如果項目尚未獲核准，則會立即將其退回。 不過，已獲核准的項目可能會有重大影響。 您必須有專案核准者核准回收，才能在實際值中沖銷交易。

## <a name="specify-project-approvers"></a>指定專案核准者
每個專案都會有數個專案團隊成員。 您可以指定哪些團隊成員兼任專案核准者。

1. 移至 **專案** 表單，然後從清單中開啟專案。
2. 在 **團隊** 索引標籤上，選取將成為專案核准者的團隊成員，然後選取 **編輯**。
3. 將 **專案核准者** 欄位設定為 **是**。
4. 選取 **儲存**。
5. 重複步驟 2-4，以新增或編輯其他專案核准者。

## <a name="configure-the-users-manager"></a>設定使用者的經理

1. 移至 **設定** > **安全性** > **使用者**。
2. 選取您要指派經理的使用者，然後從 **組織資訊** 區域的清單中選取經理。 
3. 選取 **儲存**。




[!INCLUDE[footer-include](../includes/footer-banner.md)]