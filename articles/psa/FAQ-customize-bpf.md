---
title: 如何自訂專案階段商務程序流程？
description: 有關如何自訂專案階段商務程序流程的概觀。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 10/11/2018
ms.topic: article
author: JohnPBurrows
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 0f95677c56b745bf7900ad503596c93f1e722281
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5286148"
---
# <a name="how-do-i-customize-the-project-stages-business-process-flow"></a><span data-ttu-id="1c28a-103">如何自訂專案階段商務程序流程？</span><span class="sxs-lookup"><span data-stu-id="1c28a-103">How do I customize the Project Stages business process flow?</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-2-4x-9-0-platform](../includes/cc-applies-to-psa-app-2-4x-9-0-platform.md)]
[!INCLUDE[cc-applies-to-psa-app-1x-8-2-platform](../includes/cc-applies-to-psa-app-1x-8-2-platform.md)]

<span data-ttu-id="1c28a-104">舊版 Project Service 應用程式有一個已知的限制，也就是專案階段商務程序流程中的階段名稱必須與預期的英文名稱 (**Quote**、**Plan**、**Close**) 完全相符。</span><span class="sxs-lookup"><span data-stu-id="1c28a-104">There's a known limitation in earlier versions of the Project Service application that the names of the stages in the Project Stages business process flow must exactly match the expected English names (**Quote**, **Plan**, **Close**).</span></span> <span data-ttu-id="1c28a-105">否則，需要使用英文階段名稱的商務規則就無法如預期般運作。</span><span class="sxs-lookup"><span data-stu-id="1c28a-105">Otherwise, the business logic, which relies on the English stage names, doesn't work as expected.</span></span> <span data-ttu-id="1c28a-106">這正是您在專案表單上看不到熟悉的動作 (例如 **切換程序** 或 **編輯程序**)，而且也不建議自訂商務程序流程的原因。</span><span class="sxs-lookup"><span data-stu-id="1c28a-106">That's why you don't see familiar actions such as **Switch Process** or **Edit Process** available on the project form, and customizing the business process flow isn't encouraged.</span></span> 

<span data-ttu-id="1c28a-107">版本 2.4.5.48 及更新版本已解決這項限制。</span><span class="sxs-lookup"><span data-stu-id="1c28a-107">This limitation has been addressed in version 2.4.5.48 and later.</span></span> <span data-ttu-id="1c28a-108">如果您需要針對舊版自訂預設商務程序流程，本文有提供建議的因應措施。</span><span class="sxs-lookup"><span data-stu-id="1c28a-108">This article provides suggested workarounds if you need to customize the default business process flow for earlier versions.</span></span>  

## <a name="business-logic-requires-an-exact-match-with-english-stage-names"></a><span data-ttu-id="1c28a-109">商務規則必須與英文階段名稱完全相符</span><span class="sxs-lookup"><span data-stu-id="1c28a-109">Business logic requires an exact match with English stage names</span></span>

<span data-ttu-id="1c28a-110">專案階段商務程序流程包含推動應用程式中下列行為的商務規則：</span><span class="sxs-lookup"><span data-stu-id="1c28a-110">The Project Stages business process flow includes business logic that drives the following behaviors in the app:</span></span>
- <span data-ttu-id="1c28a-111">當專案與報價有關聯時，程式碼會將商務程序流程設定為 **Quote** 階段。</span><span class="sxs-lookup"><span data-stu-id="1c28a-111">When the project is associated with a quote, the code sets the business process flow to the **Quote** stage.</span></span>
- <span data-ttu-id="1c28a-112">當專案與合約有關聯時，程式碼會將商務程序流程設定為 **Plan** 階段。</span><span class="sxs-lookup"><span data-stu-id="1c28a-112">When the project is associated with a contract, the code sets the business process flow to the **Plan** stage.</span></span>
- <span data-ttu-id="1c28a-113">商務程序流程進展到 **Close** 階段時，專案記錄會停用。</span><span class="sxs-lookup"><span data-stu-id="1c28a-113">When the business process flow is advanced to the **Close** stage, the project record is deactivated.</span></span> <span data-ttu-id="1c28a-114">停用專案時，系統會將專案表單和分工結構圖 (WBS) 設定為唯讀、將具名資源預約釋出，以及停用任何相關聯的價目表。</span><span class="sxs-lookup"><span data-stu-id="1c28a-114">When the project is deactivated, the project form and work breakdown structure (WBS) are set to read-only, the named resource bookings are released, and any associated price lists are deactivated.</span></span>

<span data-ttu-id="1c28a-115">此商務規則必須使用專案階段的英文名稱。</span><span class="sxs-lookup"><span data-stu-id="1c28a-115">This business logic relies on the English names for the project stages.</span></span> <span data-ttu-id="1c28a-116">這項對英文階段名稱的相依性就是我們為何不鼓勵自訂專案階段商務程序流程，以及您為何在專案實體上看不到常見商務程序流程動作 (如 **切換程序** 或 **編輯程序**) 的主要原因。</span><span class="sxs-lookup"><span data-stu-id="1c28a-116">This dependency on the English stage names is the main reason why customization of the Project Stages business process flow isn't encouraged, as well as why you don’t see the common business process flow actions like **Switch Process** or **Edit Process** on the project entity.</span></span>

## <a name="what-happens-if-the-stage-names-dont-match-the-english-names"></a><span data-ttu-id="1c28a-117">如果階段名稱與英文名稱不相符，會發生什麼情況？</span><span class="sxs-lookup"><span data-stu-id="1c28a-117">What happens if the stage names don't match the English names?</span></span>

<span data-ttu-id="1c28a-118">在 8.2 平台的 Project Service 應用程式 1.x 版中，當商務程序流程中的階段名稱與英文名稱不完全相符時，會將設定報價或合約正確階段或關閉專案的商務規則略過。</span><span class="sxs-lookup"><span data-stu-id="1c28a-118">In the Project Service app version 1.x on the 8.2 platform, when the stage names in the business process flow don’t match the English stage names exactly, the business logic that sets the right stage for quotes or contracts, or that closes the project, is skipped.</span></span> <span data-ttu-id="1c28a-119">不會顯示任何錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1c28a-119">No error messages are displayed.</span></span> <span data-ttu-id="1c28a-120">因此，您似乎可以自訂專案階段商務程序流程。</span><span class="sxs-lookup"><span data-stu-id="1c28a-120">Therefore it appears that you are able to customize the Project Stages business process flow.</span></span> <span data-ttu-id="1c28a-121">然而，您不會看到任何處理報價、合約及專案的自動程序關閉。</span><span class="sxs-lookup"><span data-stu-id="1c28a-121">However, you won’t see any of the automatic processes working for quotes, contracts, and project close.</span></span>

<span data-ttu-id="1c28a-122">在 9.0 平台的 Project Service 應用程式 2.4.4.30 版或更早版本中，商務程序流程發生了重大架構變更，而這需要改寫商務程序流程商務規則。</span><span class="sxs-lookup"><span data-stu-id="1c28a-122">In the Project Service app version 2.4.4.30 or earlier on the 9.0 platform, there was a significant architectural change to business process flows, which required a re-write of the business process flow business logic.</span></span> <span data-ttu-id="1c28a-123">如此一來，要是程序階段名稱不符合預期的英文名稱，您就會收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1c28a-123">As a result, if the process stage names don’t match the expected English names, you do receive an error message.</span></span> 

<span data-ttu-id="1c28a-124">因此，如果您想要自訂專案實體的專案階段商務程序流程，就只能將全新階段新增至專案實體的預設商務程序流程，同時讓 **報價**、**計劃** 和 **關閉** 階段保持原樣。</span><span class="sxs-lookup"><span data-stu-id="1c28a-124">Therefore, if you want to customize the Project Stages business process flow for the project entity, you can only add brand new stages to the default business process flow for the project entity, while keeping the **Quote**, **Plan**, and **Close** stages as-is.</span></span> <span data-ttu-id="1c28a-125">此限制可確保您不會從預期要在商務程序流程中使用英文階段名稱的商務規則上收到錯誤訊息。</span><span class="sxs-lookup"><span data-stu-id="1c28a-125">This restriction ensures that you don’t get errors from the business logic that expects the English stage names in the business process flow.</span></span>

<span data-ttu-id="1c28a-126">在版本 2.4.5.48 或更新版本中，本文所述的商務規則已從專案實體的預設商務程序流程中移除。</span><span class="sxs-lookup"><span data-stu-id="1c28a-126">In version 2.4.5.48 or later, the business logic described in this article has been removed from the default business process flow for the project entity.</span></span> <span data-ttu-id="1c28a-127">升級至該版本或更新版本將可讓您自訂商務程序流程，或以您自己的商務程序流程來取代預設的。</span><span class="sxs-lookup"><span data-stu-id="1c28a-127">Upgrading to that version or later will let you customize or replace the default business process flow with one of your own.</span></span> 

## <a name="workarounds-for-earlier-versions"></a><span data-ttu-id="1c28a-128">舊版適用的因應措施</span><span class="sxs-lookup"><span data-stu-id="1c28a-128">Workarounds for earlier versions</span></span>

<span data-ttu-id="1c28a-129">如果您不考慮升級，則可以透過下列兩種方式之一來自訂專案實體的專案階段商務程序流程：</span><span class="sxs-lookup"><span data-stu-id="1c28a-129">If upgrading isn't an option, you can customize the Project Stages business process flow for the project entity in one of these two ways:</span></span>

1. <span data-ttu-id="1c28a-130">新增其他階段至預設設定，同時保留 **報價**、**計劃** 和 **關閉** 的英文階段名稱。</span><span class="sxs-lookup"><span data-stu-id="1c28a-130">Add additional stages to the default configuration, while retaining the English stage names for **Quote**, **Plan**, and **Close**.</span></span>


![將階段新增至預設設定的螢幕擷取畫面](media/FAQ-Customize-BPF-1.png)
 
2. <span data-ttu-id="1c28a-132">建立您自己的商務程序流程，並將其設為專案實體的主要商務程序流程，這樣即可讓您使用任何您想要的階段名稱。</span><span class="sxs-lookup"><span data-stu-id="1c28a-132">Create your own business process flow and make it the primary business process flow for the project entity, which lets you have any stage names you want.</span></span> <span data-ttu-id="1c28a-133">不過，如果您想要使用相同的標準專案階段 **報價**、**計劃** 和 **關閉**，就必須進行一些會移除自訂階段名稱的自訂。</span><span class="sxs-lookup"><span data-stu-id="1c28a-133">However, if you want to use the same standard project stages **Quote**, **Plan**, and **Close**, you need to do some customizations that are driven off your custom stage names.</span></span> <span data-ttu-id="1c28a-134">較複雜的邏輯是在專案結尾的部分，您仍然可以只是藉由停用專案記錄來觸發。</span><span class="sxs-lookup"><span data-stu-id="1c28a-134">The more complex logic is in the closing of the project, which you can still trigger by just deactivating the project record.</span></span>

![BPF 自訂](media/FAQ-Customize-BPF-2.png)

### <a name="additional-considerations-for-project-service-app-version-24430-or-earlier-on-platform-90"></a><span data-ttu-id="1c28a-136">對於 9.0 平台的 Project Service 應用程式 2.4.4.30 版或更早版本的其他考量</span><span class="sxs-lookup"><span data-stu-id="1c28a-136">Additional considerations for Project Service app version 2.4.4.30 or earlier on platform 9.0</span></span>

<span data-ttu-id="1c28a-137">在 9.0 平台的 Project Service 應用程式 2.4.4.30 版或更早版本中，**依階段的專案** 圖表及專案清單檢視表中所用專案實體上的 **階段名稱** 欄位不會隨自訂商務程序流程一併更新，因為該欄位與預設專案階段商務程序流程相聯繫。</span><span class="sxs-lookup"><span data-stu-id="1c28a-137">In Project Service 2.4.4.30 or earlier on platform 9.0, with a custom business process flow the **Stage Name** field on the project entity used in the **Project By Stage** chart and project list views won’t update, because it’s coupled to the default Project Stages business process flow.</span></span> <span data-ttu-id="1c28a-138">您可以透過下列步驟解決此問題：</span><span class="sxs-lookup"><span data-stu-id="1c28a-138">You can address this issue with the following steps:</span></span>

- <span data-ttu-id="1c28a-139">新增自訂欄位，以擷取目前隨著使用者進展通過自訂商務程序流程而更新的商務程序流程階段。</span><span class="sxs-lookup"><span data-stu-id="1c28a-139">Add a custom field to capture the current business process flow stage that is updated as the user advances through the custom business process flow.</span></span>

- <span data-ttu-id="1c28a-140">將 **依階段的專案** 圖表修改為使用自訂欄位，而不使用預設設定。</span><span class="sxs-lookup"><span data-stu-id="1c28a-140">Modify the **Project By Stage** chart to work with your custom field instead of the default configuration.</span></span>

### <a name="steps-to-create-your-own-business-process-flow-for-the-project-entity"></a><span data-ttu-id="1c28a-141">自行建立專案實體的商務程序流程的步驟</span><span class="sxs-lookup"><span data-stu-id="1c28a-141">Steps to create your own business process flow for the project entity</span></span>

<span data-ttu-id="1c28a-142">若要自行建立專案實體的商務程序流程，請執行下列動作：</span><span class="sxs-lookup"><span data-stu-id="1c28a-142">To create your own business process flow for the project entity do the following:</span></span>

1. <span data-ttu-id="1c28a-143">移至 **設定** > **程序中心**。</span><span class="sxs-lookup"><span data-stu-id="1c28a-143">Go to **Settings** > **Process Center**.</span></span> <span data-ttu-id="1c28a-144">不要複製專案階段商務程序流程，因為這樣也會複製 Project Service 商務規則。</span><span class="sxs-lookup"><span data-stu-id="1c28a-144">Don’t copy the Project Stages business process flow because that also copies the Project Service business logic.</span></span>

  ![建立程序](media/FAQ-Customize-BPF-3.png)

2. <span data-ttu-id="1c28a-146">使用程序設計師來建立您想要的階段名稱。</span><span class="sxs-lookup"><span data-stu-id="1c28a-146">Use the Process Designer to create the stage names you want.</span></span> <span data-ttu-id="1c28a-147">如果您想要使用與 **報價**、**計劃** 及 **關閉** 預設階段相同的功能，就必須以您的自訂商務程序流程的階段名稱為基礎建立該功能。</span><span class="sxs-lookup"><span data-stu-id="1c28a-147">If you want the same functionality as the default stages for **Quote**, **Plan**, and **Close**, you’ll have to create that based on your custom business process flow’s stage names.</span></span>

   ![用來自訂 BPF 的程序設計師螢幕擷取畫面](media/FAQ-Customize-BPF-4.png) 

3. <span data-ttu-id="1c28a-149">在程序設計師中，按一下 **程序流程順序**，向上移動自訂商務程序流程超過專案階段商務程序流程以至清單頂端，藉此將其設為專案實體的主要業務程序流程。</span><span class="sxs-lookup"><span data-stu-id="1c28a-149">In the Process Designer, click **Order Process Flow** to make the custom business process flow the primary business process flow for the project entity by moving it above the Project Stages business process flow to the top of the list.</span></span>


   [<span data-ttu-id="1c28a-150">使用程序流程順序的螢幕擷取畫面</span><span class="sxs-lookup"><span data-stu-id="1c28a-150">Screenshot of using Order Process Flow</span></span>](media/FAQ-Customize-BPF-5-720.png)

### <a name="the-following-steps-apply-to-project-service-app-24430-or-earlier-on-the-90-platform"></a><span data-ttu-id="1c28a-151">下列步驟適用於 9.0 平台的 Project Service 應用程式 2.4.4.30 版或更早版本</span><span class="sxs-lookup"><span data-stu-id="1c28a-151">The following steps apply to Project Service app 2.4.4.30 or earlier on the 9.0 platform</span></span>

4. <span data-ttu-id="1c28a-152">將新的自訂欄位新增至專案實體，以擷取自訂商務程序流程中的自訂階段。</span><span class="sxs-lookup"><span data-stu-id="1c28a-152">Add a new custom field to the project entity to capture the custom stages in your custom business process flow.</span></span> <span data-ttu-id="1c28a-153">當自訂商務程序流程上的階段更新時，您必須新增商務規則 (外掛程式/工作流程)，才能更新此欄位。</span><span class="sxs-lookup"><span data-stu-id="1c28a-153">You’ll need to add business logic (plugin/workflow) to update this field when the stage on the custom business process flow is updated.</span></span>

   ![自訂專案實體的螢幕擷取畫面](media/FAQ-Customize-BPF-6-720.png)

5. <span data-ttu-id="1c28a-155">將 **依階段的專案** 圖表修改為使用階段的新自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="1c28a-155">Modify the **Project By Stage** chart to use your new custom field for stages.</span></span>

   ![使用 [依階段的專案] 圖表的螢幕擷取畫面](media/FAQ-Customize-BPF-7-720.png)

6. <span data-ttu-id="1c28a-157">將專案實體的任何檢視表修改為使用階段的新自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="1c28a-157">Modify any views for the project entity to include your new custom field for stages.</span></span>

   ![修改專案實體的檢視表的螢幕擷取畫面](media/FAQ-Customize-BPF-8-720.png)



[!INCLUDE[footer-include](../includes/footer-banner.md)]