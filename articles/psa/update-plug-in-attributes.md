---
title: 更新外掛程式屬性以包含新的定價維度
description: 此主題提供有關更新定價維度外掛程式屬性的資訊。
author: Rumant
manager: kfend
ms.custom: ''
ms.date: 11/19/2018
ms.topic: article
ms.service: dynamics-365-customerservice
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f215555dd7b29444e00499c0e731624e51057250
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073079"
---
# <a name="update-plug-in-attributes-to-include-new-pricing-dimensions"></a><span data-ttu-id="9a252-103">更新外掛程式屬性以包含新的定價維度</span><span class="sxs-lookup"><span data-stu-id="9a252-103">Update plug-in attributes to include new pricing dimensions</span></span>

> [!NOTE]
> <span data-ttu-id="9a252-104">如果您沒有使用 Project Service Automation (PSA) 報價和合約功能，可略過本主題。</span><span class="sxs-lookup"><span data-stu-id="9a252-104">If you are not using the Project Service Automation (PSA) Quoting and Contracting features, you can skip this topic.</span></span>

<span data-ttu-id="9a252-105">本主題假設您已完成[建立自訂欄位和實體](create-custom-fields-entities.md)、[將自訂欄位新增至價格設定與交易實體](field-references.md)以及[將自訂欄位設定為定價維度](set-up-pricing-dimensions.md)主題中的程序。</span><span class="sxs-lookup"><span data-stu-id="9a252-105">This topic assumes that you have completed the procedures in the topics, [Create custom fields and entities](create-custom-fields-entities.md), [Add custom fields to price setup and transactional entities](field-references.md), and [Set up custom fields as pricing dimensions](set-up-pricing-dimensions.md).</span></span> <span data-ttu-id="9a252-106">如果您尚未完成這些程序，請返回並加以完，然後再回到本主題。</span><span class="sxs-lookup"><span data-stu-id="9a252-106">If you haven't completed those procedures, go back and complete them and then return to this topic.</span></span>

<span data-ttu-id="9a252-107">在專案報價明細的 **報價明細** 頁面上建立報價明細詳細資料後，系統會在背景中建立兩個估計明細，其中一個明細用於成本面估計，另一個用於銷售面估計。</span><span class="sxs-lookup"><span data-stu-id="9a252-107">When a quote line detail is created on the **Quote Line** page for a project quote line, the system creates two estimate lines in the background -- one line for the cost side of the estimate and one for sales side.</span></span> <span data-ttu-id="9a252-108">這同樣適用於專案合約服務內容。</span><span class="sxs-lookup"><span data-stu-id="9a252-108">This is the same  for project contract lines.</span></span>

<span data-ttu-id="9a252-109">對成本面欄位數量或欄位進行變更時，該變更會傳播至銷售面。</span><span class="sxs-lookup"><span data-stu-id="9a252-109">When you make a change to the quantity or a field on the cost side, that change is propagated to the sales side.</span></span> <span data-ttu-id="9a252-110">這可能是因為下列外掛程式必須在變更定價維度後重新註冊的緣故。</span><span class="sxs-lookup"><span data-stu-id="9a252-110">This is possible because of the following plug-ins that must be re-registered after a change to pricing dimensions.</span></span>

- <span data-ttu-id="9a252-111">PreOperationContractLineDetailUpdate - 更新 **msdyn_orderlinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="9a252-111">PreOperationContractLineDetailUpdate - Updates **msdyn_orderlinetransaction**.</span></span>
- <span data-ttu-id="9a252-112">PreOperationQuoteLineDetailUpdate - 更新 **msdyn_quotelinetransaction**.</span><span class="sxs-lookup"><span data-stu-id="9a252-112">PreOperationQuoteLineDetailUpdate - Updates **msdyn_quotelinetransaction**.</span></span>

<span data-ttu-id="9a252-113">下列步驟將引導您逐步完成註冊外掛程式的程序。</span><span class="sxs-lookup"><span data-stu-id="9a252-113">The following steps walk you through the process of registering the plug-ins.</span></span>

1. <span data-ttu-id="9a252-114">開啟 **PluginRegistrationTool** 並連接至您的線上執行個體。</span><span class="sxs-lookup"><span data-stu-id="9a252-114">Open the **PluginRegistrationTool** and connect to your online instance.</span></span>
2. <span data-ttu-id="9a252-115">按一下 **搜尋** ，然後搜尋要更新的外掛程式。</span><span class="sxs-lookup"><span data-stu-id="9a252-115">Click **Search** and search for the plug-in to be updated.</span></span>

 ![搜尋樹狀結構的螢幕擷取畫面](media/PRT-1.png)

3. <span data-ttu-id="9a252-117">找到外掛程式後，選取該外掛程式，然後按一下 **在主要表單上選取** 。</span><span class="sxs-lookup"><span data-stu-id="9a252-117">After the plug-in is found, select it and then click **Select on Main Form**.</span></span>

4. <span data-ttu-id="9a252-118">選取要更新外掛程式的步驟，按一下滑鼠右鍵，然後選取 **更新** 。</span><span class="sxs-lookup"><span data-stu-id="9a252-118">Select the step of the plug-in to be updated, right-click, and then select **Update**.</span></span>

 ![要更新的外掛程式螢幕擷取畫面](media/PRT-2.png)
 
5. <span data-ttu-id="9a252-120">在更新視窗中，按一下篩選屬性中的省略符號 ( **...** )。</span><span class="sxs-lookup"><span data-stu-id="9a252-120">In the update window, click the ellipsis ( **...** ) in the filtering attributes.</span></span>

 ![更新現有步驟設定資訊的螢幕擷取畫面](media/PRT-3.png)
 
6. <span data-ttu-id="9a252-122">選取定價屬性核取方塊。</span><span class="sxs-lookup"><span data-stu-id="9a252-122">Select the pricing attribute check boxes.</span></span>

 ![螢幕擷取畫面顯示定價屬性的核取方塊選擇](media/PRT-4.png)

7. <span data-ttu-id="9a252-124">按一下 **確定** 關閉頁面，然後選取 **更新步驟** 。</span><span class="sxs-lookup"><span data-stu-id="9a252-124">Click **OK** to close the page and then select **Update Step**.</span></span>

 ![螢幕擷取畫面顯示 [更新步驟] 按鈕](media/PRT-5.png)
 
8. <span data-ttu-id="9a252-126">對第二個外掛程式 **PreOperationQuoteLineDetail - msdyn_quotelinetransaction 的更新** 重複此程序。</span><span class="sxs-lookup"><span data-stu-id="9a252-126">Repeat this process for the second plug-in, **PreOperationQuoteLineDetail - Update of msdyn_quotelinetransaction**.</span></span>

9. <span data-ttu-id="9a252-127">關閉外掛程式註冊工具</span><span class="sxs-lookup"><span data-stu-id="9a252-127">Close the plug-in registration tool.</span></span>

