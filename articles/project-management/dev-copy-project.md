---
title: 使用複製專案來開發專案範本
description: 本主題提供有關如何使用 [複製專案] 自訂動作建立專案範本的資訊。
author: stsporen
manager: Annbe
ms.date: 10/07/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 0100c29873be6346614e958ef6ea0c77da2c9590
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4131603"
---
# <a name="develop-project-templates-with-copy-project"></a>使用複製專案來開發專案範本

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

Dynamics 365 Project Operations 支援複製專案以及將任何指派還原回一般資源 (代表角色) 的功能。 客戶可以使用此功能來建立基本專案範本。

選取 **複製專案** 時，目標專案的狀態會更新。 使用 **狀態原因** 來判斷複製動作何時完成。 選取 **複製專案** 時，如果在目標專案實體中偵測不到目標日期，也會將專案的開始日期更新為目前的開始日期。

## <a name="copy-project-custom-action"></a>複製專案自訂動作 

### <a name="name"></a>名稱 

**msdyn_CopyProjectV2**

### <a name="input-parameters"></a>輸入參數
有三個輸入參數：

| 參數          | 鍵入   | 值                                                   | 
|--------------------|--------|----------------------------------------------------------|
| ProjectCopyOption  | String | **{"removeNamedResources":true}** 或 **{"clearTeamsAndAssignments":true}** |
| SourceProject      | 實體參考 | 來源專案 |
| 目標             | 實體參考 | 目標專案 |


- **{"clearTeamsAndAssignments":true}**：Project 網頁版的預設行為，並將移除所有指派和團隊成員。
- **{"removeNamedResources":true}**：Project Operations 的預設行為，並將指派還原為一般資源。

如需更多有關動作的預設行為，請參閱[使用 Web API 動作](https://docs.microsoft.com/powerapps/developer/common-data-service/webapi/use-web-api-actions)

## <a name="specify-fields-to-copy"></a>指定要複製的欄位 
呼叫動作時，**複製專案** 會查看專案檢視表 **複製專案欄**，以判斷要在複製專案時複製哪些欄位。
