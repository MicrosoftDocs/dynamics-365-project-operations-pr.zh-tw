---
title: 設定信用卡整合
description: 本主題說明如何使用與費用相關的信用卡交易。
author: suvaidya
manager: AnnBe
ms.date: 04/02/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.search.form: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.search.region: ''
ms.author: shylaw
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 72ff98f5985af4362cde3c9914e0d20247f1f09a
ms.sourcegitcommit: ca0fc078d1a12484eca193fe051b8442c0559db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/07/2021
ms.locfileid: "5866673"
---
# <a name="set-up-credit-card-integration"></a><span data-ttu-id="5e5c0-103">設定信用卡整合</span><span class="sxs-lookup"><span data-stu-id="5e5c0-103">Set up credit card integration</span></span>

<span data-ttu-id="5e5c0-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="5e5c0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="5e5c0-105">您可以設定費用相關信用卡交易，以便按照定期排程自動匯入這些交易。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-105">Expense-related credit card transactions can be set up so that they are automatically imported on a recurring schedule.</span></span> <span data-ttu-id="5e5c0-106">或者，也可以在需要時手動匯入交易。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-106">Alternatively, the transactions can be manually imported as they are required.</span></span> <span data-ttu-id="5e5c0-107">信用卡交易會透過信用卡交易資料實體進行匯入。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-107">The credit card transactions are imported through the credit card transactions data entity.</span></span>

## <a name="import-credit-card-transactions"></a><span data-ttu-id="5e5c0-108">匯入信用卡交易</span><span class="sxs-lookup"><span data-stu-id="5e5c0-108">Import credit card transactions</span></span>

<span data-ttu-id="5e5c0-109">若要匯入信用卡交易，請依照下列步驟進行：</span><span class="sxs-lookup"><span data-stu-id="5e5c0-109">To import credit card transactions, follow these steps:</span></span>

1. <span data-ttu-id="5e5c0-110">在 **信用卡交易** 頁面上，選取 **匯入交易**。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-110">On the **Credit card transactions** page, select **Import transactions**.</span></span> <span data-ttu-id="5e5c0-111">如果您是第一次開啟資料管理，則系統必須先更新資料實體的清單，您才能繼續進行。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-111">If you’re opening data management for the first time, the system must update the list of data entities before you can continue.</span></span>
2. <span data-ttu-id="5e5c0-112">在 **名稱** 欄位中，輸入對匯入工作的獨特描述。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-112">In the **Name** field, enter a unique description for the import job.</span></span>
3. <span data-ttu-id="5e5c0-113">在 **來源資料格式** 欄位中，選取包含要匯入之信用卡交易的檔案格式。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-113">In the **Source data format** field, select the format of the file that contains the credit card transactions to import.</span></span>
4. <span data-ttu-id="5e5c0-114">選取 **上傳**，然後尋找並選取要匯入的檔案。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-114">Select **Upload**, and then find and select the file to import.</span></span>
5. <span data-ttu-id="5e5c0-115">上傳檔案之後，選取圖標上的 **檢視對應** 連結，以驗證信用卡交易檔案與信用卡交易資料實體欄的對應。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-115">After the file has been uploaded, validate the mapping of the credit card transaction file and the columns of the credit card transactions data entity by selecting the **View map** link on the tile.</span></span> <span data-ttu-id="5e5c0-116">如果發生對應錯誤，或者您必須變更對應時，請從 **對應視覺化效果** 索引標籤或 **對應詳細資料** 索引標籤中進行對應變更。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-116">If there are mapping errors, or if you must change the mapping, make the mapping changes from either the **Mapping visualization** tab or the **Mapping details** tab.</span></span>
6. <span data-ttu-id="5e5c0-117">若要將信用卡交易自動化，請選取 **建立定期資料作業**。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-117">To automate the credit card transactions, select **Create recurring data job**.</span></span> <span data-ttu-id="5e5c0-118">您可以接著設定可定義多久匯入一次信用卡交易的週期。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-118">You can then set the recurrence that defines how often credit card transactions should be imported.</span></span> <span data-ttu-id="5e5c0-119">設定完畢後，選取 **確定**。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-119">When you’ve finished, select **OK**.</span></span>
7. <span data-ttu-id="5e5c0-120">若要立即匯入選取的檔案，請選取 **匯入**。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-120">To import the selected file now, select **Import**.</span></span>
8. <span data-ttu-id="5e5c0-121">如果匯入期間發生錯誤，您可以檢視執行記錄或暫存資料，以了解為確保匯入成功所須修正的錯誤。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-121">If errors occur during the import, you can view the execution log or staging data to see the errors that you must fix to help ensure a successful import.</span></span>

> [!NOTE]
> <span data-ttu-id="5e5c0-122">如果您需要匯入多種檔案格式，則必須為每種格式類型建立不同的匯入工作。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-122">If you need to import more than one file format, you must create separate import jobs for each format type.</span></span>

## <a name="reassign-the-credit-card-transactions-for-terminated-employees"></a><span data-ttu-id="5e5c0-123">重新指派離職員工的信用卡交易</span><span class="sxs-lookup"><span data-stu-id="5e5c0-123">Reassign the credit card transactions for terminated employees</span></span>

<span data-ttu-id="5e5c0-124">員工記錄終止後，即會停用該員工的 Active Directory Domain Services (AD DS) 帳戶。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-124">After an employee record is terminated, the employee’s Active Directory Domain Services (AD DS) account is disabled.</span></span> <span data-ttu-id="5e5c0-125">不過，可能會有仍須認列為費用和進行報銷的有效信用卡交易。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-125">However, there might be active credit card transactions that must still be expensed and reimbursed.</span></span> <span data-ttu-id="5e5c0-126">在 **信用卡交易** 頁面上，您可以為任何有相關聯員工離職的信用卡交易重新指派員工。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-126">On the **Credit card transactions** page, you can reassign the employee for any credit card transaction where the associated employee has been terminated.</span></span>

<span data-ttu-id="5e5c0-127">選取一個或多個信用卡交易，然後選取 **重新指派交易**。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-127">Select one or more credit card transactions, and then select **Reassign transactions**.</span></span> <span data-ttu-id="5e5c0-128">您可以接著選取其他員工，將信用卡交易指派給他。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-128">You can then select another employee to assign the credit card transactions to.</span></span> <span data-ttu-id="5e5c0-129">重新指派信用卡交易之後，就可以選取這些交易以列入費用報表，並透過通常的費用報表報銷程序來支付。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-129">After the credit card transactions have been reassigned, they can be selected for an expense report and paid through the usual process for expense report reimbursement.</span></span>

## <a name="delete-credit-card-transactions"></a><span data-ttu-id="5e5c0-130">刪除信用卡交易</span><span class="sxs-lookup"><span data-stu-id="5e5c0-130">Delete credit card transactions</span></span> 

<span data-ttu-id="5e5c0-131">匯入信用卡交易之後，有時可能需要刪除特定交易。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-131">Sometimes, after credit card transactions are imported, certain transactions may need to be deleted.</span></span> <span data-ttu-id="5e5c0-132">這可能是因為交易重複或因為資料可能不正確。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-132">This could be because the transactions are duplicates or because the data might isn't accurate.</span></span> <span data-ttu-id="5e5c0-133">系統管理員可以使用 **刪除信用卡交易** 功能來選取並刪除 **未附加** 至費用報表的信用卡交易。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-133">Admins can use the **"Delete credit card transactions"** feature to select and delete credit card transactions that are **not attached** to an expense report.</span></span> 

1. <span data-ttu-id="5e5c0-134">移至 **定期工作** > **刪除信用卡交易**。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-134">Go to **Periodic tasks** > **Delete credit card transactions**.</span></span>
2. <span data-ttu-id="5e5c0-135">選取 **篩選** 並提供資訊，以找出要納入的記錄。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-135">Select **Filter** and provide information to identify the records to include.</span></span>
3. <span data-ttu-id="5e5c0-136">選取 **確定** 以刪除記錄。</span><span class="sxs-lookup"><span data-stu-id="5e5c0-136">Select **OK** to delete the records.</span></span> 

[!INCLUDE[footer-include](../includes/footer-banner.md)]
