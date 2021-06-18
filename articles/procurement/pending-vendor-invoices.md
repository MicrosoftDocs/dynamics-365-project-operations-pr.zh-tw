---
title: 使用待處理廠商發票購買非庫存材料
description: 本主題說明如何記錄待處理廠商發票。
author: sigitac
ms.date: 04/12/2021
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: b5e6632d73c8a211b1f0d568be8e10ef47be77e2
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5993772"
---
# <a name="purchase-non-stocked-materials-using-a-pending-vendor-invoice"></a><span data-ttu-id="b08c3-103">使用待處理廠商發票購買非庫存材料</span><span class="sxs-lookup"><span data-stu-id="b08c3-103">Purchase non-stocked materials using a pending vendor invoice</span></span>

<span data-ttu-id="b08c3-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="b08c3-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="b08c3-105">公司採購專案的非庫存材料時，系統會立即將此記錄至專案的成本。</span><span class="sxs-lookup"><span data-stu-id="b08c3-105">As a company procures non-stocked materials for a project, the costs can be immediately recorded against the project.</span></span> 

<span data-ttu-id="b08c3-106">例如，Contoso Robotics US 正在執行設備更新專案，並需要軟體授權。</span><span class="sxs-lookup"><span data-stu-id="b08c3-106">For example, Contoso Robotics US is performing an equipment renewal project and needs software licenses.</span></span> <span data-ttu-id="b08c3-107">這些授權是從協力廠商所採購。</span><span class="sxs-lookup"><span data-stu-id="b08c3-107">These licenses are procured from a third-party vendor.</span></span>  <span data-ttu-id="b08c3-108">應付帳款記帳員會使用 Dynamics 365 Finance 來記錄待處理廠商發票單據，並將授權成本直接歸入設備更新專案。</span><span class="sxs-lookup"><span data-stu-id="b08c3-108">Using Dynamics 365 Finance, the Accounts payable clerk records a pending vendor invoice document and attributes the license costs directly against the equipment renewal project.</span></span> 

> [!IMPORTANT]
> <span data-ttu-id="b08c3-109">使用本主題中所述的功能之前，請先檢閱並套用必要的設定。</span><span class="sxs-lookup"><span data-stu-id="b08c3-109">Before you use the functionality described in this topic, review and apply the required configurations.</span></span> <span data-ttu-id="b08c3-110">如需詳細資訊，請參閱[啟用非庫存材料和待處理廠商發票](configure-materials-nonstocked.md)。</span><span class="sxs-lookup"><span data-stu-id="b08c3-110">For more information, see [Enable non-stocked materials and pending vendor invoices](configure-materials-nonstocked.md).</span></span> 

## <a name="post-a-project-related-pending-vendor-invoice"></a><span data-ttu-id="b08c3-111">過帳專案相關的待處理廠商發票</span><span class="sxs-lookup"><span data-stu-id="b08c3-111">Post a project-related pending vendor invoice</span></span> 

<span data-ttu-id="b08c3-112">待處理廠商發票可以記錄在 **待處理廠商發票** 頁面上 (**應付帳款** > **發票** > **待處理廠商發票**)。</span><span class="sxs-lookup"><span data-stu-id="b08c3-112">Pending vendor invoices can be recorded on the **Pending vendor invoices** page (**Accounts payable** > **Invoices** > **Pending vendor invoices**).</span></span> <span data-ttu-id="b08c3-113">完成下列步驟，以過帳專案相關的待處理廠商發票：</span><span class="sxs-lookup"><span data-stu-id="b08c3-113">Complete the following steps to post a project-related pending vendor invoice:</span></span>

1. <span data-ttu-id="b08c3-114">移至 **應付帳款** > **發票**，並選取 **新增**。</span><span class="sxs-lookup"><span data-stu-id="b08c3-114">Go to **Accounts payable** > **Invoices** and select **New**.</span></span> 
2. <span data-ttu-id="b08c3-115">在 **發票科目** 欄位中，選取廠商，然後在 **編號** 欄位中輸入廠商發票識別碼。</span><span class="sxs-lookup"><span data-stu-id="b08c3-115">In the **Invoice account** field, select a vendor and in the **Number** field, enter the vendor invoice identification.</span></span>
3. <span data-ttu-id="b08c3-116">將一行明細新增至廠商發票，然後在 **項目編號** 欄位中，選取從廠商所購買的非庫存項目。</span><span class="sxs-lookup"><span data-stu-id="b08c3-116">Add a line to the vendor invoice and in the **Item number** field, select the non-stocked item purchased from the vendor.</span></span> 

    > [!NOTE]
    > <span data-ttu-id="b08c3-117">以採購類別為依據的廠商發票明細無法記錄在專案的帳上。</span><span class="sxs-lookup"><span data-stu-id="b08c3-117">Vendor invoice lines that are based on a procurement category can't be recorded against the project.</span></span> 
    
5. <span data-ttu-id="b08c3-118">新增購買的數量。</span><span class="sxs-lookup"><span data-stu-id="b08c3-118">Add the quantity purchased.</span></span> <span data-ttu-id="b08c3-119">系統會根據非庫存項目價格設定來填入單價。</span><span class="sxs-lookup"><span data-stu-id="b08c3-119">The system will populate the unit price based on the non-stocked item price configuration.</span></span> 
6. <span data-ttu-id="b08c3-120">確認該行明細上的總計金額及其他必要詳細資料。</span><span class="sxs-lookup"><span data-stu-id="b08c3-120">Verify the total amount and other required details on the line.</span></span>
7. <span data-ttu-id="b08c3-121">在明細詳細資料的 **專案** 索引標籤上，選取將此項目記錄至其帳上之專案的識別碼。</span><span class="sxs-lookup"><span data-stu-id="b08c3-121">On the line details, on the **Project** tab, select the ID of the project that this item will be recorded to.</span></span>
8. <span data-ttu-id="b08c3-122">或者，選取活動編號，並更新專案類別和明細屬性。</span><span class="sxs-lookup"><span data-stu-id="b08c3-122">Optionally, select the activity number, and update the project category and line property.</span></span>
9. <span data-ttu-id="b08c3-123">過帳待處理廠商發票。</span><span class="sxs-lookup"><span data-stu-id="b08c3-123">Post pending vendor invoice.</span></span> <span data-ttu-id="b08c3-124">將發票過帳時，系統會記錄：</span><span class="sxs-lookup"><span data-stu-id="b08c3-124">When the invoice is posted, the system records:</span></span>
    
    - <span data-ttu-id="b08c3-125">廠商結餘金額。</span><span class="sxs-lookup"><span data-stu-id="b08c3-125">The vendor balance amount.</span></span>
    - <span data-ttu-id="b08c3-126">銷售稅金額。</span><span class="sxs-lookup"><span data-stu-id="b08c3-126">The sales tax amount.</span></span>
    - <span data-ttu-id="b08c3-127">將專案帳上的成本記錄至採購整合科目。</span><span class="sxs-lookup"><span data-stu-id="b08c3-127">The cost against the project is recorded to the procurement integration account.</span></span>
    - <span data-ttu-id="b08c3-128">Dataverse 中的專案實際交易。</span><span class="sxs-lookup"><span data-stu-id="b08c3-128">The project actual transaction in Dataverse.</span></span> <span data-ttu-id="b08c3-129">使用 [Project Operations 整合帳目](../project-accounting/project-operations-integration-journal.md)進一步處理此交易。</span><span class="sxs-lookup"><span data-stu-id="b08c3-129">This transaction is further processed using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="b08c3-130">過帳此帳目會將採購整合科目中的金額轉入專案成本科目。</span><span class="sxs-lookup"><span data-stu-id="b08c3-130">Posting this journal moves the amount from the procurement integration account to the project cost account.</span></span>
