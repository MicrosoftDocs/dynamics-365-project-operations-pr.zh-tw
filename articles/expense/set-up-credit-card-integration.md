---
title: 設定信用卡整合
description: 本主題說明如何匯入和維護費用相關信用卡交易。
author: suvaidya
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 12c7971204b485ee7cb222cd9cffdfdfde93dcf4
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072959"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="5aea4-103">設定信用卡整合</span><span class="sxs-lookup"><span data-stu-id="5aea4-103">Set up credit card integration</span></span>

<span data-ttu-id="5aea4-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="5aea4-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5aea4-105">您可以設定費用相關信用卡交易，以便按照定期排程自動匯入這些交易。</span><span class="sxs-lookup"><span data-stu-id="5aea4-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="5aea4-106">或者，也可以在需要時手動匯入交易。</span><span class="sxs-lookup"><span data-stu-id="5aea4-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="5aea4-107">信用卡交易會透過信用卡交易資料實體進行匯入。</span><span class="sxs-lookup"><span data-stu-id="5aea4-107">The credit card transactions are imported through the Credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="5aea4-108">匯入信用卡交易</span><span class="sxs-lookup"><span data-stu-id="5aea4-108">Import credit card transactions</span></span>

1. <span data-ttu-id="5aea4-109">在 **信用卡交易** 頁面上，選取 **匯入交易** 。</span><span class="sxs-lookup"><span data-stu-id="5aea4-109">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="5aea4-110">如果您是第一次開啟資料管理，則系統必須先更新資料實體的清單，您才能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="5aea4-110">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="5aea4-111">在 **名稱** 方塊中，輸入匯入工作的唯一名稱。</span><span class="sxs-lookup"><span data-stu-id="5aea4-111">In the **Name** field, enter a unique description of the import job.</span></span>
3. <span data-ttu-id="5aea4-112">在 **來源資料格式** 欄位中，選取包含要匯入之信用卡交易的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="5aea4-112">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="5aea4-113">選取 **上傳** ，然後尋找並選取要匯入的檔案。</span><span class="sxs-lookup"><span data-stu-id="5aea4-113">Select **Upload** , and then find and select the file to import.</span></span>
5. <span data-ttu-id="5aea4-114">上傳檔案之後，選取圖標上的 **檢視對應** 連結，以驗證信用卡交易檔案與信用卡交易資料實體欄的對應。</span><span class="sxs-lookup"><span data-stu-id="5aea4-114">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the Credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="5aea4-115">如果發生對應錯誤，或者您必須變更對應時，請從 **對應視覺化效果** 索引標籤或 **對應詳細資料** 索引標籤中進行對應變更。</span><span class="sxs-lookup"><span data-stu-id="5aea4-115">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="5aea4-116">若要將信用卡交易自動化，請選取 **建立定期資料作業** 。</span><span class="sxs-lookup"><span data-stu-id="5aea4-116">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="5aea4-117">您可以接著設定可定義多久匯入一次信用卡交易的週期。</span><span class="sxs-lookup"><span data-stu-id="5aea4-117">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="5aea4-118">設定完畢後，選取 **確定** 。</span><span class="sxs-lookup"><span data-stu-id="5aea4-118">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="5aea4-119">若要立即匯入選取的檔案，請選取 **匯入** 。</span><span class="sxs-lookup"><span data-stu-id="5aea4-119">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="5aea4-120">如果匯入時發生錯誤，您可以檢視執行記錄檔或暫存資料，了解必須修正的錯誤以確保成功匯入。</span><span class="sxs-lookup"><span data-stu-id="5aea4-120">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help guarantee a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="5aea4-121">如果您必須匯入多個檔案格式，則必須為每個格式類型建立不同的匯入工作。</span><span class="sxs-lookup"><span data-stu-id="5aea4-121">If you must import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="5aea4-122">重新指派離職員工的信用卡交易</span><span class="sxs-lookup"><span data-stu-id="5aea4-122">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="5aea4-123">員工記錄終止後，即會停用該員工的 Active Directory Domain Services (AD DS) 帳戶。</span><span class="sxs-lookup"><span data-stu-id="5aea4-123">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="5aea4-124">不過，可能會有仍須認列為費用和進行報銷的有效信用卡交易。</span><span class="sxs-lookup"><span data-stu-id="5aea4-124">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="5aea4-125">您可以從 **信用卡交易** 頁面中，為任何有相關員工已離職的信用卡交易重新指派員工。</span><span class="sxs-lookup"><span data-stu-id="5aea4-125">From the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="5aea4-126">選取一個或多個信用卡交易，然後選取 **重新指派交易** 。</span><span class="sxs-lookup"><span data-stu-id="5aea4-126">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="5aea4-127">您可以接著選取其他員工，將信用卡交易指派給他。</span><span class="sxs-lookup"><span data-stu-id="5aea4-127">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="5aea4-128">重新指派信用卡交易之後，就可以選取這些交易以列入費用報表，並透過通常的費用報表報銷程序來支付。</span><span class="sxs-lookup"><span data-stu-id="5aea4-128">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>
