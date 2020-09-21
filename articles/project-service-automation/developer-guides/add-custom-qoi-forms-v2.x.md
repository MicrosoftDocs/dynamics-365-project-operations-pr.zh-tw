---
title: 新增自訂實體表單 (Project Service Automation 2.x)
description: 本主題提供有關在 Dynamics 365 Project Service Automation 2.x 中如何為商機、報價、訂單或發票新增自訂實體表單的資訊。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.prod: Project Service
ms.service: business-applications
ms.assetid: 9eb9fc5e-4c7d-466c-9362-fdb0faa30506
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
ms.openlocfilehash: 2bd955ad3eb26d31676ac4ad387baccaee913cd2
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749826"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a>新增自訂實體表單 (Project Service Automation 2.x)

## <a name="type-field"></a>類型欄位 

Dynamics 365 Project Service Automation 依賴商機、報價、訂單或發票實體的**類型** (**msdyn\_ordertype**) 欄位，將這些實體的**工作型**版本與**項目型**及**服務型**版本區分開來。 這些實體的工作型版本是由 PSA 所處理。 解決方案用戶端及伺服器端的許多商務規則都相依於 **類型**欄位。 因此，建立實體時，使用正確的值來初始化欄位，非常重要。 不正確的值可能會產生不正確的行為，而且部分商務規則可能無法正確執行。

## <a name="automatic-form-switching"></a>自動表單切換

為了避免因不正確初始化和編輯銷售實體記錄而導致可能的資料損壞和非預期行為，PSA 目前已在內建表單中包含自動表單切換邏輯。 此邏輯會將使用者帶到正確的表單，以處理工作型版本或任何其他類型的商機、報價、訂單或發票實體。 使用者開啟商機、報價、訂單或發票實體的工作型版本時，表單會切換至**專案資訊**。

自動表單切換邏輯依賴 **formId** 值與 **msdyn\_ordertype** 欄位之間的對應。 所有的內建表單都已新增至該對應。 不過，自訂表單必須手動新增，以指出其所需處理的實體版本。 這是以 **msdyn\_ordertype** 欄位為依據。 如果對應中找不到表單切換，邏輯會根據儲存在實體之 **msdyn\_ordertype** 欄位中的值，切換至內建表單。

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a>新增自訂表單並開啟表單切換邏輯

下列範例顯示如何新增自訂表單**我的專案資訊**，讓它與工作型商機搭配使用。 同樣的程序也會用來新增自訂表單，讓這些表單使用報價、訂單和發票。

依照下列步驟建立**專案資訊**表單的自訂版本。

1. 在商機實體中，開啟**專案資訊**表單，然後以名稱**我的專案資訊**來儲存複本。
2. 開啟新表單，然後在屬性中，確定有**專案資訊**表單的表單初始化指令碼存在。 

    > [!IMPORTANT]
    > 請勿移除指令碼。 否則，部分資料的初始化可能會不正確。

3. 確認**類型** (**msdyn\_ordertype**) 欄位是否存在於表單中。 

    > [!IMPORTANT]
    > 請勿移除此欄位。 否則，初始化指令碼將會失敗。

4. 尋找新表單的 **formId** 值。 您可以使用兩種不同方式完成此步驟：

    - 將**我的專案資訊**表單匯出為未受管理的解決方案組件，然後查詢所匯出解決方案之 customization.xml 檔案中的 **formId** 值。
    - 在表單編輯器中開啟**我的專案資訊**表單，然後在 URL 中尋找 **fromId** 參數旁邊的全域唯一識別碼 (GUID)，如下圖所示。

    ![新表單在 URL 中的 formId 值](media/how-to-add-custom-forms-in-v2.0.png)

5. 編輯 msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js Web 資料以建立 **msdyn\_ordertype** mapping for the **formId** 值。 將程式碼從資源移除，然後取代為下列程式碼。

    ```javascript
    define(["require", "exports"], function (require, exports) {
        "use strict";
        var SalesDocumentCustomFormIds = (function () {
            function SalesDocumentCustomFormIds() {
            }
            SalesDocumentCustomFormIds.overwriteFormIds = function (mappedFormIds) {
                /*
                ---- Notes ----
                mappedFormIds[SalesEntity][OrderType] => The array of forms IDs that support particular entity and order type
                Add or overwrite customized formId for the particular entity and order type by calling:
                    mappedFormIds[<EntityType>][<msdyn_ordertype>].push("<formId>");
                Allowed msdyn_ordertype values for reference:
                    ServiceBased: 690970002 (Field Service version of the entity)
                    WorkBased: 192350001 (PSA version of the entity)
                    ItemBased: 192350000 (Regular out of the box entity)
                Uncomment and update one of the following lines to register custom PSA form for required entity:
                */      
                //mappedFormIds[1][192350001].push("<formId>"); //Quote
                //mappedFormIds[5][192350001].push("<formId>"); //Quote Line
                //mappedFormIds[2][192350001].push("<formId>"); //Sales Order
                //mappedFormIds[6][192350001].push("<formId>"); //Sales Order Line
                // In this example we have added new form for Opportunity
                mappedFormIds[0][192350001].push("192EE537-DCC4-45D3-B7AF-EA694B9113D2"); //Opportunity
                //mappedFormIds[4][192350001].push("<formId>"); //Opportunity Line
            };
            return SalesDocumentCustomFormIds;
        }());
        exports.default = SalesDocumentCustomFormIds;
    });
    ```

6. 儲存然後發佈自訂。
