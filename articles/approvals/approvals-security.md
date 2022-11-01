---
title: 安全性與核准
description: 本文說明在 Microsoft Dynamics 365 Project Operations 中使用核准的安全性設定。
author: stsporen
ms.date: 08/29/2022
ms.topic: security
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 0dcadaa142bf46e4c54f160759602ac749022108
ms.sourcegitcommit: 73aff2b3c5e5b8a2254735b0b25931cbb6754c87
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/20/2022
ms.locfileid: "9709387"
---
# <a name="security-and-approvals"></a>安全性與核准

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

Microsoft Dynamics 365 Project Operations 使用兩種資訊安全角色，以允許核准時間、費用和材料項目：

- 專案核准者
- 專案核准者管理員

## <a name="project-approver"></a>專案核准者

您必須有 **專案核准者** 資訊安全角色，以核准專案時間、費用和材料項目。 您也必須具有權存取相關的相關實體，例如 **Project**。 該存取權可由具有 **專案經理** 角色的人員指派。 此外，您必須是專案的團隊成員，並將標記為核准者。

若要核准非專案項目，您必須是提交者的經理。

## <a name="project-approver-admin"></a>專案核准者管理員

> [!NOTE]
> 您必須先啟用[核准集](approval-sets.md)功能，才能使用「專案核准者管理員」功能。

**專案核准者管理員** 資訊安全角色可讓使用者繞過原則，並允許核准所有專案中的項目。 指派此角色時，會略過需要團隊成員資格並標記為核准者的驗證邏輯。 您必須可以透過指派給您的資訊安全角色存取相應的相關資料表，例如 **專案**。

系統使用者內容略過驗證的方式與專案核准者管理員資訊安全角色相同。
