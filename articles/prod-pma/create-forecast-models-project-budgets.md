---
title: 建立專案預算的預測模型
description: 本主題說明如何為剩餘預算建立預測模型。
author: Yowelle
manager: AnnBe
ms.date: 04/24/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: andchoi
ms.dyn365.ops.version: 7
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 32a436d240f5535ff15f8bc3b8ba9be2d1d4da17
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073132"
---
# <a name="create-forecast-models-for-project-budgets"></a><span data-ttu-id="3cffd-103">建立專案預算的預測模型</span><span class="sxs-lookup"><span data-stu-id="3cffd-103">Create forecast models for project budgets</span></span> 

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3cffd-104">本主題說明如何為剩餘預算建立預測模型。</span><span class="sxs-lookup"><span data-stu-id="3cffd-104">This topic describes how to create a forecast model for remaining budgets.</span></span> <span data-ttu-id="3cffd-105">受預算控制的專案會使用兩種類型的預算：原始和剩餘。</span><span class="sxs-lookup"><span data-stu-id="3cffd-105">A project that is subject to budget control uses two types of budgets: original and remaining.</span></span> <span data-ttu-id="3cffd-106">建立專案預算時，您必須指定已在 **預測模型** 頁面中建立的原始及剩餘預算預測模型。</span><span class="sxs-lookup"><span data-stu-id="3cffd-106">When you create a project budget, you must specify the original and remaining budget forecast models that were created in the **Forecast models** page.</span></span> <span data-ttu-id="3cffd-107">當您認可專案預算時，系統會根據指定的模型建立專案預算。</span><span class="sxs-lookup"><span data-stu-id="3cffd-107">Project budgets based on the specified models are created when you commit the project budget.</span></span>

> [!NOTE]
> <span data-ttu-id="3cffd-108">預算控制所用的預測模型不能有子模型，也不可做為子模型。</span><span class="sxs-lookup"><span data-stu-id="3cffd-108">A forecast model that is used for budget control can’t have a submodel or be used as a submodel.</span></span>

1. <span data-ttu-id="3cffd-109">選取 **專案管理與會計** > **設定** > **預測**  > **預測模型** 。</span><span class="sxs-lookup"><span data-stu-id="3cffd-109">Select **Project management and accounting** > **Setup** > **Forecasts**  > **Forecast models**.</span></span>
2. <span data-ttu-id="3cffd-110">選取 **新增** 建立新的預測模型，然後輸入新模型的模型識別碼及名稱。</span><span class="sxs-lookup"><span data-stu-id="3cffd-110">Select **New** to create a new forecast model, and then enter a model ID number and name for the new model.</span></span> 
3. <span data-ttu-id="3cffd-111">將 **已停止** 選項設定為 **是** ，以防止對預測模型的預測明細進行任何變更。</span><span class="sxs-lookup"><span data-stu-id="3cffd-111">Set the **Stopped** option to **Yes** to prevent any changes to the forecast lines for the forecast model.</span></span> 
4. <span data-ttu-id="3cffd-112">如果與模型相關的預測明細應在總帳中產生現金流預測，請將 **包含在現金流預測中** 設定為 **是** 。</span><span class="sxs-lookup"><span data-stu-id="3cffd-112">If the forecast lines that the model is associated with should generate cash flow forecasts in the general ledger, set **Include in Cash flow forecasts** to **Yes.**</span></span> 
5. <span data-ttu-id="3cffd-113">若要使用專案日期做為發票日期，請將 **預測發票日期** 設定為 **是** 。</span><span class="sxs-lookup"><span data-stu-id="3cffd-113">To use the project date as the invoice date, set **Forecast Invoice date** to **Yes**.</span></span> 
6. <span data-ttu-id="3cffd-114">在 **預算類型** 欄位中，選取下列其中一個模型類型：</span><span class="sxs-lookup"><span data-stu-id="3cffd-114">In the **Budget type** field, select one of the following model types:</span></span>

   - <span data-ttu-id="3cffd-115">**原始預算** ：使用建立和核准初始預算時所認可的原始預算金額。</span><span class="sxs-lookup"><span data-stu-id="3cffd-115">**Original budget** : Use the original budget amounts that are committed when the initial budget is created and approved.</span></span>
   - <span data-ttu-id="3cffd-116">**剩餘預算** ：使用專案生命週期中的剩餘預算金額。</span><span class="sxs-lookup"><span data-stu-id="3cffd-116">**Remaining budget** : Use the remaining budget amounts during the life of the project.</span></span> <span data-ttu-id="3cffd-117">此預測模型中的餘額會根據實際交易減少，並隨預算修正增減。</span><span class="sxs-lookup"><span data-stu-id="3cffd-117">The balances in this forecast model are reduced by actual transactions and increased or decreased by budget revisions.</span></span>
   - <span data-ttu-id="3cffd-118">**結轉** ：使用專案的結轉預算金額。</span><span class="sxs-lookup"><span data-stu-id="3cffd-118">**Carry-forward** : Use the carry-forward budget amounts for the project.</span></span> <span data-ttu-id="3cffd-119">[結轉] 是選用程序，可執行以將未使用的預算金額從一個會計年度移轉至另一個。</span><span class="sxs-lookup"><span data-stu-id="3cffd-119">Carry-forward is an optional process that can be run to transfer unused budget amounts from one fiscal year to another.</span></span>

7. <span data-ttu-id="3cffd-120">視需要設定下列選項：</span><span class="sxs-lookup"><span data-stu-id="3cffd-120">Set the following options as required:</span></span>

   - <span data-ttu-id="3cffd-121">啟用 **預測發票日期** 以使用專案日期做為發票日期。</span><span class="sxs-lookup"><span data-stu-id="3cffd-121">Enable **Forecast invoice date** to use the project date as the invoice date.</span></span>
   - <span data-ttu-id="3cffd-122">啟用 **使用 WIP 進行預測** 以根據進行中工作 (WIP) 進行預測，然後選取 WIP 類型。</span><span class="sxs-lookup"><span data-stu-id="3cffd-122">Enable **Forecast with WIP** to forecast based on work in progress (WIP), and then select the type of WIP.</span></span> 
   - <span data-ttu-id="3cffd-123">您可以保留預設為 **無** 的 **預算類型** ，或輸入新的類型。</span><span class="sxs-lookup"><span data-stu-id="3cffd-123">You can keep the default **Budget type** as **None** or enter a new type.</span></span> <span data-ttu-id="3cffd-124">變更記錄之後，您就無法變更預算類型。</span><span class="sxs-lookup"><span data-stu-id="3cffd-124">The budget type can't be changed after you change a record.</span></span>     
    > [!NOTE]
    > <span data-ttu-id="3cffd-125">如果您變更預設預算類型，則所有其他選項都會無法用於更新，而且您也無法重複使用此預測模型。</span><span class="sxs-lookup"><span data-stu-id="3cffd-125">If you change the default budget type, all other options will become unavailable for updates, and you can't reuse this forecast model.</span></span> 
   


 

