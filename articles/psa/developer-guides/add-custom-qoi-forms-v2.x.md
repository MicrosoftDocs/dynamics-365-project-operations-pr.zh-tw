---
title: 新增自訂實體表單 (Project Service Automation 2.x)
description: 本主題提供有關在 Dynamics 365 Project Service Automation 2.x 中如何為商機、報價、訂單或發票新增自訂實體表單的資訊。
author: makk
manager: kfend
ms.custom:
- dyn365-projectservice
ms.date: 3/14/2019
ms.topic: article
ms.service: business-applications
ms.author: makk
audience: admin
search.audienceType:
- admin
- customizer
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: 57d4b9aad433af6d3e73369c76f2793f349c6965
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073190"
---
# <a name="add-new-custom-entity-forms-project-service-automation-2x"></a><span data-ttu-id="5e432-103">新增自訂實體表單 (Project Service Automation 2.x)</span><span class="sxs-lookup"><span data-stu-id="5e432-103">Add new custom entity forms (Project Service Automation 2.x)</span></span>

## <a name="type-field"></a><span data-ttu-id="5e432-104">類型欄位</span><span class="sxs-lookup"><span data-stu-id="5e432-104">Type field</span></span> 

<span data-ttu-id="5e432-105">Dynamics 365 Project Service Automation 依賴商機、報價、訂單或發票實體的 **類型** ( **msdyn\_ordertype** ) 欄位，將這些實體的 **工作型** 版本與 **項目型** 及 **服務型** 版本區分開來。</span><span class="sxs-lookup"><span data-stu-id="5e432-105">Dynamics 365 Project Service Automation relies on the **Type** ( **msdyn\_ordertype** ) field of the Opportunity, Quote, Order, and Invoice entities to distinguish **work-based** versions of these entities from **item-based** and **service-based** versions.</span></span> <span data-ttu-id="5e432-106">這些實體的工作型版本是由 PSA 所處理。</span><span class="sxs-lookup"><span data-stu-id="5e432-106">Work-based versions of these entities are handled by PSA.</span></span> <span data-ttu-id="5e432-107">解決方案用戶端及伺服器端的許多商務規則都相依於 **類型** 欄位。</span><span class="sxs-lookup"><span data-stu-id="5e432-107">Lots of business logic on the client side and server side of the solution depends on the **Type** field.</span></span> <span data-ttu-id="5e432-108">因此，建立實體時，使用正確的值來初始化欄位，非常重要。</span><span class="sxs-lookup"><span data-stu-id="5e432-108">Therefore, it's important that the field be initialized with a correct value when the entities are created.</span></span> <span data-ttu-id="5e432-109">不正確的值可能會產生不正確的行為，而且部分商務規則可能無法正確執行。</span><span class="sxs-lookup"><span data-stu-id="5e432-109">An incorrect value can cause incorrect behaviors, and some business logic might not run correctly.</span></span>

## <a name="automatic-form-switching"></a><span data-ttu-id="5e432-110">自動表單切換</span><span class="sxs-lookup"><span data-stu-id="5e432-110">Automatic form switching</span></span>

<span data-ttu-id="5e432-111">為了避免因不正確初始化和編輯銷售實體記錄而導致可能的資料損壞和非預期行為，PSA 目前已在內建表單中包含自動表單切換邏輯。</span><span class="sxs-lookup"><span data-stu-id="5e432-111">To avoid potential data corruption and unexpected behaviors that are caused by incorrect initialization and editing of the sales entity records, PSA now includes logic for automatic form switching in out-of-box forms.</span></span> <span data-ttu-id="5e432-112">此邏輯會將使用者帶到正確的表單，以處理工作型版本或任何其他類型的商機、報價、訂單或發票實體。</span><span class="sxs-lookup"><span data-stu-id="5e432-112">This logic takes users to the correct form for working with the work-based version or any other type of Opportunity, Quote, Order, or Invoice entity.</span></span> <span data-ttu-id="5e432-113">使用者開啟商機、報價、訂單或發票實體的工作型版本時，表單會切換至 **專案資訊** 。</span><span class="sxs-lookup"><span data-stu-id="5e432-113">When a user opens the work-based version of an Opportunity, Quote, Order, or Invoice entity, the form is switched to **Project Information**.</span></span>

<span data-ttu-id="5e432-114">自動表單切換邏輯依賴 **formId** 值與 **msdyn\_ordertype** 欄位之間的對應。</span><span class="sxs-lookup"><span data-stu-id="5e432-114">The automatic form switching logic relies on the mapping between the **formId** value and the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="5e432-115">所有的內建表單都已新增至該對應。</span><span class="sxs-lookup"><span data-stu-id="5e432-115">All out-of-box forms have been added to that mapping.</span></span> <span data-ttu-id="5e432-116">不過，自訂表單必須手動新增，以指出其所需處理的實體版本。</span><span class="sxs-lookup"><span data-stu-id="5e432-116">However, custom forms must be manually added to indicate which version of the entity they are intended to handle.</span></span> <span data-ttu-id="5e432-117">這是以 **msdyn\_ordertype** 欄位為依據。</span><span class="sxs-lookup"><span data-stu-id="5e432-117">This is based on the **msdyn\_ordertype** field.</span></span> <span data-ttu-id="5e432-118">如果對應中找不到表單切換，邏輯會根據儲存在實體之 **msdyn\_ordertype** 欄位中的值，切換至內建表單。</span><span class="sxs-lookup"><span data-stu-id="5e432-118">If the form switching is missing from the mapping, logic will switch to the out-of-box form, based on the value that is saved in the **msdyn\_ordertype** field of the entity.</span></span>

## <a name="add-custom-forms-and-turn-on-the-form-switching-logic"></a><span data-ttu-id="5e432-119">新增自訂表單並開啟表單切換邏輯</span><span class="sxs-lookup"><span data-stu-id="5e432-119">Add custom forms and turn on the form switching logic</span></span>

<span data-ttu-id="5e432-120">下列範例顯示如何新增自訂表單 **我的專案資訊** ，讓它與工作型商機搭配使用。</span><span class="sxs-lookup"><span data-stu-id="5e432-120">The following example shows how to add a custom form, **My Project Information** , so that it works with work-based opportunities.</span></span> <span data-ttu-id="5e432-121">同樣的程序也會用來新增自訂表單，讓這些表單使用報價、訂單和發票。</span><span class="sxs-lookup"><span data-stu-id="5e432-121">The same process is used to add custom forms so that they work with quotes, orders, and invoices.</span></span>

<span data-ttu-id="5e432-122">依照下列步驟建立 **專案資訊** 表單的自訂版本。</span><span class="sxs-lookup"><span data-stu-id="5e432-122">Follow these steps to create a custom version of the **Project Information** form.</span></span>

1. <span data-ttu-id="5e432-123">在商機實體中，開啟 **專案資訊** 表單，然後以名稱 **我的專案資訊** 來儲存複本。</span><span class="sxs-lookup"><span data-stu-id="5e432-123">In the Opportunity entity, open the **Project Information** form, and save a copy under the name **My Project Information**.</span></span>
2. <span data-ttu-id="5e432-124">開啟新表單，然後在屬性中，確定有 **專案資訊** 表單的表單初始化指令碼存在。</span><span class="sxs-lookup"><span data-stu-id="5e432-124">Open the new form, and then, in the properties, make sure that the form initialization scripts from the **Project Information** form are present.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="5e432-125">請勿移除指令碼。</span><span class="sxs-lookup"><span data-stu-id="5e432-125">Don't remove the scripts.</span></span> <span data-ttu-id="5e432-126">否則，部分資料的初始化可能會不正確。</span><span class="sxs-lookup"><span data-stu-id="5e432-126">Otherwise, some data might be initialized incorrectly.</span></span>

3. <span data-ttu-id="5e432-127">確認 **類型** ( **msdyn\_ordertype** ) 欄位是否存在於表單中。</span><span class="sxs-lookup"><span data-stu-id="5e432-127">Verify that the **Type** ( **msdyn\_ordertype** ) field is present in the form.</span></span> 

    > [!IMPORTANT]
    > <span data-ttu-id="5e432-128">請勿移除此欄位。</span><span class="sxs-lookup"><span data-stu-id="5e432-128">Don't remove this field.</span></span> <span data-ttu-id="5e432-129">否則，初始化指令碼將會失敗。</span><span class="sxs-lookup"><span data-stu-id="5e432-129">Otherwise, the initialization scripts will fail.</span></span>

4. <span data-ttu-id="5e432-130">尋找新表單的 **formId** 值。</span><span class="sxs-lookup"><span data-stu-id="5e432-130">Find the **formId** value of the new form.</span></span> <span data-ttu-id="5e432-131">您可以使用兩種不同方式完成此步驟：</span><span class="sxs-lookup"><span data-stu-id="5e432-131">You can complete this step in two ways:</span></span>

    - <span data-ttu-id="5e432-132">將 **我的專案資訊** 表單匯出為未受管理的解決方案組件，然後查詢所匯出解決方案之 customization.xml 檔案中的 **formId** 值。</span><span class="sxs-lookup"><span data-stu-id="5e432-132">Export the **My Project Information** form as part of an unmanaged solution, and then look up the **formId** value in the customization.xml file of the exported solution.</span></span>
    - <span data-ttu-id="5e432-133">在表單編輯器中開啟 **我的專案資訊** 表單，然後在 URL 中尋找 **fromId** 參數旁邊的全域唯一識別碼 (GUID)，如下圖所示。</span><span class="sxs-lookup"><span data-stu-id="5e432-133">Open the **My Project Information** form in the form editor, and then look for the globally unique identifier (GUID) next to the **fromId** parameter in the URL, as shown in the following illustration.</span></span>

    ![新表單在 URL 中的 formId 值](media/how-to-add-custom-forms-in-v2.0.png)

5. <span data-ttu-id="5e432-135">編輯 msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js Web 資料以建立 **msdyn\_ordertype** mapping for the **formId** 值。</span><span class="sxs-lookup"><span data-stu-id="5e432-135">Create an **msdyn\_ordertype** mapping for the **formId** value by editing the msdyn\_/SalesDocument/PSSalesDocumentCustomFormIds.js web resource.</span></span> <span data-ttu-id="5e432-136">將程式碼從資源移除，然後取代為下列程式碼。</span><span class="sxs-lookup"><span data-stu-id="5e432-136">Remove the code from the resource, and replace it with the following code.</span></span>

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

6. <span data-ttu-id="5e432-137">儲存然後發佈自訂。</span><span class="sxs-lookup"><span data-stu-id="5e432-137">Save and then publish the customizations.</span></span>
