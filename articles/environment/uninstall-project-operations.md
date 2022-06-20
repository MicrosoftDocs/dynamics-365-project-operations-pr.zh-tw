---
title: 取消安裝 [Dynamics 365 Project Operations]
description: 本文提供有關如何解除安裝 Dynamics 365 Project Operations 的資訊。
author: stsporen
ms.date: 11/09/2021
ms.topic: article
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 33a505594d6db47b4f8a0c8a630a0836f424e7d5
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8911954"
---
# <a name="uninstall-dynamics-365-project-operations"></a>取消安裝 [Dynamics 365 Project Operations] 

_**適用於：** 資源/非庫存型案例適用的 Project Operations_

若要解除安裝 Dynamics 365 Project Operations，您必須指派系統管理員的角色。

1. 移至 **設定** > **解決方案**。

    ![頁面設定。](./media/uninstall-proj-ops-solutions.png)
  
2. 依照下表中所列的正確順序移除解決方案。 

    | 步驟 | 解決方案名稱                                    | 附註                                                                                         |
    |------|----------------------------------------------------|----------------------------------------------------------------------------------------------|
    | 1 | msdyn_ProjectServiceUpgrade_managed.cab            | 如果找不到，請略過此解決方案。                                                            |
    | 2 | ProjectOperations_Anchor                           | 如果找不到，請略過此解決方案。                                                            |
    | 3 | Dynamics365ProjectOperationsDualWriteEntityMaps    | 如果找不到，請略過此解決方案。                                                            |
    | 4 | Dynamics365ProjectOperationsDualWrite              | 如果找不到，請略過此解決方案。                                                            |
    | 5 | ProjectService                                     | 沒有其他附註。                                                                         |
    | 6 | ProjectServiceCore_Patch                           | 沒有其他附註。                                                                         |
    | 7 | ProjectServiceCore                                 | 沒有其他附註。                                                                         |
    | 8 | ProjectServiceDeprecatedComponents                 | 如果找不到，請略過此解決方案。                                                            |
    | 9 | FieldServiceCommon                                 | 使用 Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 進行雙動寫入時需要。   |
    | 10 | msdyn_AssetCommon                                  | 使用 Dynamics 365 Finance 或 Dynamics 365 Supply Chain Management 進行雙動寫入時需要。   |
    | 11 | msdyn_TESA_Anchor                                  | Dynamics 365 Field Service 需要。                                                     |
    | 12 | msdyn_TESA_Patch                                   | Dynamics 365 Field Service 需要。                                                     |
    | 13 | msdyn_TESA                                         | Dynamics 365 Field Service 需要。                                                     |
    | 14 | ResourceSchedulingControls                         | Dynamics 365 Field Service 需要。                                                     |
    | 15 | MicrosoftDynamicsScheduling3_CumulativePatch       | Dynamics 365 Field Service 需要。                                                     |
    | 16 | MicrosoftDynamicsScheduling_Patch_xx               | Dynamics 365 Field Service 需要。                                                     |
    | 17 | MicrosoftDynamicsScheduling                        | Dynamics 365 Field Service 需要。                                                     |
    | 18 | Dynamics365FinanceAndOperationsAnchor              | 如果找不到，請略過此解決方案。                                                            |
    | 19 | Dynamics365Notes                                   | 如果找不到，請略過此解決方案。                                                            |
    | 20 | Dynamics365FinanceAndOperationsDualWriteEntityMaps | 如果找不到，請略過此解決方案。                                                            |
    | 21 | DualWriteCore                                      | 如果找不到，請略過此解決方案。                                                            |
    | 22 | Dynamics365AssetManagementApp                      | 如果找不到，請略過此解決方案。                                                            |
    | 23 | Dynamics365AssetManagement                         | 如果找不到，請略過此解決方案。                                                            |
    | 24 | Dynamics365SupplyChainExtended                     | 如果找不到，請略過此解決方案。                                                            |
    | 25 | Dynamics365FinanceExtended                         | 如果找不到，請略過此解決方案。                                                            |
    | 26 | HCMCommon                                          | 如果找不到，請略過此解決方案。                                                            |
    | 27 | Dynamics365FinanceAndOperationsCommon              | 如果找不到，請略過此解決方案。                                                            |
    | 28 | 當事人                                              | 如果找不到，請略過此解決方案。                                                            |
    | 29 | Dynamics365Company                                 | 如果找不到，請略過此解決方案。                                                            |
    | 30 | CurrencyExchangeRates                              | 如果找不到，請略過此解決方案。                                                            |
    | 31 | AssetCommon                                        | 如果找不到，請略過此解決方案。                                                            |
