---
title: 匯入和維護信用卡交易
description: 本主題說明如何匯入和維護費用相關信用卡交易。 您可以設定這些交易，讓交易按照週期性排程自動進行匯入，也可以在需要時手動匯入這些交易。
author: KimANelson
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPbsMainDataLines
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 274023
ms.assetid: 3605eda1-a7ed-4675-8031-5279c5a8f5e4
ms.search.region: Global
ms.author: suvaidya
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: c434356c08e8490931bd60ea5b10fe2706cb0f51
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5951064"
---
# <a name="import-and-maintain-credit-card-transactions"></a><span data-ttu-id="728d0-104">匯入和維護信用卡交易</span><span class="sxs-lookup"><span data-stu-id="728d0-104">Import and maintain credit card transactions</span></span>

<span data-ttu-id="728d0-105">您可以設定費用相關信用卡交易，以便按照定期排程自動匯入這些交易。</span><span class="sxs-lookup"><span data-stu-id="728d0-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="728d0-106">或者，也可以在需要時手動匯入交易。</span><span class="sxs-lookup"><span data-stu-id="728d0-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="728d0-107">信用卡交易會透過信用卡交易資料實體進行匯入。</span><span class="sxs-lookup"><span data-stu-id="728d0-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

<span data-ttu-id="728d0-108">如需資料實體的詳細資訊，請參閱[資料實體](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities)。</span><span class="sxs-lookup"><span data-stu-id="728d0-108">For more information about data entities, see [Data entities](/dynamics365/fin-ops-core/dev-itpro/data-entities/data-entities).</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="728d0-109">匯入信用卡交易</span><span class="sxs-lookup"><span data-stu-id="728d0-109">Import credit card transactions</span></span>

1. <span data-ttu-id="728d0-110">在 **信用卡交易** 頁面上，選取 **匯入交易**。</span><span class="sxs-lookup"><span data-stu-id="728d0-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="728d0-111">如果您是第一次開啟資料管理，則系統必須先更新資料實體的清單，您才能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="728d0-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="728d0-112">在 **名稱** 方塊中，輸入匯入工作的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="728d0-112">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="728d0-113">在 **來源資料格式** 欄位中，選取包含要匯入之信用卡交易的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="728d0-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="728d0-114">選取 **上傳**，然後尋找並選取要匯入的檔案。</span><span class="sxs-lookup"><span data-stu-id="728d0-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="728d0-115">上傳檔案之後，選取圖標上的 **檢視對應** 連結，以驗證信用卡交易檔案與信用卡交易資料實體欄的對應。</span><span class="sxs-lookup"><span data-stu-id="728d0-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="728d0-116">如果發生對應錯誤，或者您必須變更對應時，請從 **對應視覺化效果** 索引標籤或 **對應詳細資料** 索引標籤中進行對應變更。</span><span class="sxs-lookup"><span data-stu-id="728d0-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="728d0-117">若要將信用卡交易自動化，請選取 **建立定期資料作業**。</span><span class="sxs-lookup"><span data-stu-id="728d0-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="728d0-118">您可以接著設定可定義多久匯入一次信用卡交易的週期。</span><span class="sxs-lookup"><span data-stu-id="728d0-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="728d0-119">設定完畢後，選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="728d0-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="728d0-120">若要立即匯入選取的檔案，請選取 **匯入**。</span><span class="sxs-lookup"><span data-stu-id="728d0-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="728d0-121">如果匯入時發生錯誤，您可以檢視執行記錄檔或暫存資料，了解必須修正的錯誤以確保成功匯入。</span><span class="sxs-lookup"><span data-stu-id="728d0-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="728d0-122">如果您必須匯入多個檔案格式，則必須為每個格式類型建立不同的匯入工作。</span><span class="sxs-lookup"><span data-stu-id="728d0-122">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="728d0-123">重新指派離職員工的信用卡交易</span><span class="sxs-lookup"><span data-stu-id="728d0-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="728d0-124">員工記錄終止後，即會停用該員工的 Active Directory Domain Services (AD DS) 帳戶。</span><span class="sxs-lookup"><span data-stu-id="728d0-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="728d0-125">不過，可能會有仍須認列為費用和進行報銷的有效信用卡交易。</span><span class="sxs-lookup"><span data-stu-id="728d0-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="728d0-126">您可以從 **信用卡交易** 頁面中，為任何有相關員工已離職的信用卡交易重新指派員工。</span><span class="sxs-lookup"><span data-stu-id="728d0-126">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="728d0-127">選取一個或多個信用卡交易，然後選取 **重新指派交易**。</span><span class="sxs-lookup"><span data-stu-id="728d0-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="728d0-128">您可以接著選取其他員工，將信用卡交易指派給他。</span><span class="sxs-lookup"><span data-stu-id="728d0-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="728d0-129">重新指派信用卡交易之後，就可以選取這些交易以列入費用報表，並透過通常的費用報表報銷程序來支付。</span><span class="sxs-lookup"><span data-stu-id="728d0-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]