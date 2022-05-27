---
title: 核准概觀
description: 本主題提供有關在 Project Operations 中處理核准的資訊。
author: stsporen
ms.date: 03/31/2021
ms.topic: overview
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 735cd820011a4badb83dbf6540ffe9c49f960ca1
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576168"
---
# <a name="approvals-overview"></a>核准概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

時間、費用和材料使用送出項會經歷核准工作流程。 項目獲核准後，會在實際值中記錄交易，或在排程中的預約時間。

## <a name="approvals-workflow"></a>核准工作流程
當您建立並送出時間、費用或材料使用項目時，會建立核准記錄。 專案核准者或經理會審查並核准該項目。 如果項目與專案相關，則會在其獲核准時建立實際值。 這樣就可以追蹤成本和帳單。

## <a name="approve-an-entry"></a>核准項目
**核准** 頁面可讓您在不同的檢視表間切換，以便您查看不同類型的核准。
  
1. 移至 **核准** 頁面，並選取 **費用**、**時間**、**材料使用** 或 **回收**。
2. 審查每個核准項目，並選取您要核准的項目。
3. 選取 **核准** 以核准選取的項目。
系統會處理這些項目並建立實際值。

## <a name="reject-an-entry"></a>拒絕項目
身為專案核准者，您可能需要將項目退送回使用者以進行更正。
  
1. 移至 **核准** 頁面，然後選取要拒絕的項目。 
2. 選取 **拒絕**。
3. (選擇性) 在 **拒絕註解** 對話方塊中新增留言，以告知使用者該項目被拒的原因。
4. 選取 **確定**。 將項目退回給使用者。
  
## <a name="cancel-approval"></a>取消核准
在某些情況下，您可能需要取消先前核准的項目。 取消先前已核准的項目會有財務影響。 

## <a name="approving-recall-requests"></a>核准回收要求
在某些情況下，顧問可能需要回收先前核准的項目。 取消先前已核准的項目會有財務影響。 必須有專案核准者，才能核准回收以沖回實際值中的交易。

## <a name="specify-project-approvers"></a>指定專案核准者
每個專案都會有數個專案團隊成員。 您可以指定哪些團隊成員兼任專案核准者。

1. 移至 **專案** 頁面，然後從清單中開啟專案。
2. 在 **團隊** 索引標籤上，選取將成為專案核准者的團隊成員，然後選取 **編輯**。
3. 將 **專案核准者** 欄位設定為 **是**。
4. 選取 **儲存**。
5. 重複步驟 2-4，以新增或編輯其他專案核准者。

## <a name="configure-the-users-manager"></a>設定使用者的經理

1. 移至 **設定** > **安全性** > **使用者**。
2. 選取您要指派經理的使用者，然後從 **組織資訊** 區域的清單中選取經理。 
3. 選取 **儲存**。




[!INCLUDE[footer-include](../includes/footer-banner.md)]
