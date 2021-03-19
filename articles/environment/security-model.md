---
title: 安全性模型
description: 此主題提供有關 Dynamics 365 Project Operations 中安全性模型的資訊。
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 3f65d13809fef342be8bec682c11d95c4d9e9b19
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5276788"
---
# <a name="security-model"></a>安全性模型

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

Microsoft Dynamics 365 Project Operations 包含獨特的安全性模型，允許與 Microsoft Office 群組協同合作的角色型業務安全性模型。 


## <a name="security-roles"></a>安全性角色
Project Operations 前端功能包含下列角色：

| 角色                          | 描述                                                                                                                                                                 | Scope |
|-------------------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------|
| 實務經理              | 支援跨專案報表。                                                                                                            | 營業單位              |
| 專案核准者              | 核准專案的時間和費用。                                                                                                                              | 營業單位 |
| 專案帳務管理員 | 建立發票提案。                                                                                                                                                 | 營業單位 |
| 專案經理               | 建立專案計劃並要求資源。                                                                                                                              | 營業單位 |
| 專案資源              | 可供預約和報告時間的團隊成員。                                                                                                          | 營業單位|
| 資源管理員              | 所有資源管理功能 (例如履行資源要求和預約)，分別支援混合式「專案經理 + 資源管理員」設定以及單一和集中式資源管理員角色。 | 營業單位 |


Microsoft Project 網頁版包含下列角色：

| 角色           | 描述                                                                                                        | Scope  |
|----------------|--------------------------------------------------------------------------------------------------------------------|--------|
| 專案使用者   | 專案的共同作業使用者，他們可以建立自己的專案，並檢視任何與其共用的專案。 | 使用者   |
| 專案系統 | 用於應用程式內容的角色。 客戶不應使用此系統角色。                                    | 全域 |

## <a name="security-enforcement"></a>安全性強制
在專案層級執行的動作會已登入使用者的內容中執行。 這表示要建立、開啟或刪除專案，使用者就必須具有可在 CDS 中使用的存取權。 CDS 中的存取權可能會透過平台提供的任何可能機制來授與。 例如，範圍較大的使用者可以存取專案，或者如果已執行授與使用者存取權的明確專案共用動作。

在 Project Operations 中建立專案時，請務必要考慮這一點。

## <a name="modern-group-collaboration-with-project-operations"></a>使用 Project Operations 的新式群組共同作業
Project 網頁版和 Project Operations 支援新式共同作業群組。 透過群組新增至專案的使用者可以編輯專案計劃。

Project 網頁版會自動在指派時將使用者新增至群組。

群組允許專案權限，並且可以支援共同處理共同作業成品。 下圖描述執行群組指派程序時發生的事件和狀態變更。

Project Operations 不會透過隱含式動作建立群組，只會透過按下群組的明確動作這樣做。

**群組管理** 對話方塊中的群組成員搜尋，僅限於已設定為環境安全性群組之一部分的人員。 如需詳細資訊，請參閱[控制使用者對環境的存取：安全性群組和授權](https://docs.microsoft.com/power-platform/admin/control-user-access)。

![群組模式](./media/groupsmode.png)

1. 專案已建立並且由建立使用者所擁有。
2. 專案負責人會更新為團隊。
3. 負責人團隊會對應至指定的或建立的 Office 群組。
4. 專案的原始負責人會新增至 Office 群組。

## <a name="deployment-recommendation"></a>部署建議
隨著 Office 群組共同作業模型的演變，將會不斷新增功能，與時俱進地提供更精細的控制。 現今部署 Project Operations 的使用者，最好還是將重點放在傳統 Microsoft Dynamics 365 安全性模型上。

如需詳細資訊，請參閱 [Common Data Service 中的安全性](https://docs.microsoft.com/power-platform/admin/wp-security)。

## <a name="project-operations-and-microsoft-dynamics-365-finance-security"></a>Project Operations 和 Microsoft Dynamics 365 Finance 安全性
Project Operations 包含下列角色：

- 專案經理
- 專案會計師

如需有關 Finance 中安全性的詳細資訊，請參閱[角色型安全性](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/sysadmin/role-based-security)。




[!INCLUDE[footer-include](../includes/footer-banner.md)]