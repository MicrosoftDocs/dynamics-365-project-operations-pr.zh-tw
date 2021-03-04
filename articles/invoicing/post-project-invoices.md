---
title: 發票開立程序概觀
description: 本主題提供在資源/非庫存型案例適用的 Project Operations 中開立發票的程序概觀。
author: sigitac
manager: Annbe
ms.date: 01/29/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: fbc1519b6cbcf231cfa89df8b7843d11a8904e49
ms.sourcegitcommit: b4298ca4729643c1040ef35dde8c67f829461ce7
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/29/2021
ms.locfileid: "5089214"
---
# <a name="invoicing-process-overview"></a><span data-ttu-id="21b98-103">發票開立程序概觀</span><span class="sxs-lookup"><span data-stu-id="21b98-103">Invoicing process overview</span></span>

<span data-ttu-id="21b98-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="21b98-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="21b98-105">資源/非庫存型案例適用的 Project Operations 提供同時配合專案經理與應收帳款人員/專案會計師需求所訂製的完整功能。</span><span class="sxs-lookup"><span data-stu-id="21b98-105">Project Operations for resource/non-stocked based scenarios offers comprehensive capabilities tailored to fit the needs of both Project manager and Accounts receivable clerk/project accountant.</span></span> <span data-ttu-id="21b98-106">在發票開立程序中，專案經理負責管理專案帳務積存，而應收賬款人員/專案會計師則建立合規且準確的客戶面向發票憑證。</span><span class="sxs-lookup"><span data-stu-id="21b98-106">For the invoicing process, the Project manager manages the project billing backlog and the Accounts receivable clerk/project accountant creates a compliant and accurate customer-facing invoice document.</span></span>

![發票開立流程圖](./media/invoicing-flow.png)

<span data-ttu-id="21b98-108">專案合約服務內容會定義相關聯專案交易的帳務方式。</span><span class="sxs-lookup"><span data-stu-id="21b98-108">The project contract line defines the billing method for associated project transactions.</span></span> <span data-ttu-id="21b98-109">當專案經理核准時間和費用交易時，系統會在 **專案實際值** 實體中記錄這些交易，並將資訊傳送至 Dynamics 365 Finance 中的 **專案管理與會計** 模組。</span><span class="sxs-lookup"><span data-stu-id="21b98-109">When the Project manager approves time and expense transactions, the system records the transactions in the **Project Actuals** entity and sends the information to the **Project management and accounting** module in Dynamics 365 Finance.</span></span> <span data-ttu-id="21b98-110">專案會計師接著使用 [Project Operations 整合帳目](../project-accounting/project-operations-integration-journal.md)對這些記錄進行審查和過帳。</span><span class="sxs-lookup"><span data-stu-id="21b98-110">The Project accountant then reviews and posts the records using the [Project Operations Integration journal](../project-accounting/project-operations-integration-journal.md).</span></span> <span data-ttu-id="21b98-111">此帳目包含專案實際值的重要會計詳細資料，例如帳單、銷售稅群組、帳單項目銷售稅群組和財務維度。</span><span class="sxs-lookup"><span data-stu-id="21b98-111">This journal includes important accounting details for project actuals, such as billing, sales tax group, billing item sales tax group, and financial dimensions.</span></span>

<span data-ttu-id="21b98-112">專案經理可以在[時間和材料帳務積存](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog)中使用時間和材料帳務方式，以及在[固定價格里程碑](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones)中使用固定價格帳務方式，來審查未開單銷售交易。</span><span class="sxs-lookup"><span data-stu-id="21b98-112">The Project manager can review unbilled sales transactions using the time and material billing method in the [Time and material billing backlog](../proforma-invoicing/manage-billing-backlog.md#time-and-material-billing-backlog) and fixed price billing in [Fixed price milestones](../proforma-invoicing/manage-billing-backlog.md#fixed-price-milestones).</span></span> <span data-ttu-id="21b98-113">這些檢視表可讓您篩選並選取需要包含在下一個帳單週期中的交易，然後將訊息交易標示為 **已準備好開立發票**。</span><span class="sxs-lookup"><span data-stu-id="21b98-113">These views allow you to filter and select transactions that need to be included in the next billing cycle and then mark them as **Ready to Invoice**.</span></span>

<span data-ttu-id="21b98-114">您可以[手動建立預估發票](../proforma-invoicing/create-manual-proforma-invoice.md)，或使用[週期程序](../proforma-invoicing/configure-automated-invoice-creation.md)。</span><span class="sxs-lookup"><span data-stu-id="21b98-114">You can [manually create a proforma invoice](../proforma-invoicing/create-manual-proforma-invoice.md) or use a [periodic process](../proforma-invoicing/configure-automated-invoice-creation.md).</span></span> <span data-ttu-id="21b98-115">專案經理可以視需要[調整草稿預估發票](../proforma-invoicing/manage-proforma-invoice.md)，然後確認該發票。</span><span class="sxs-lookup"><span data-stu-id="21b98-115">The Project manager can [adjust a draft proforma invoice](../proforma-invoicing/manage-proforma-invoice.md) as needed and then confirm it.</span></span>

<span data-ttu-id="21b98-116">確認的預估發票會傳送至 Finance 中的 **專案管理與會計** 模組。</span><span class="sxs-lookup"><span data-stu-id="21b98-116">The confirmed proforma invoice is sent to the **Project management and accounting** module in Finance.</span></span> <span data-ttu-id="21b98-117">專案會計師會對專案發票提案進行格式化和更新，然後將此憑證過帳並加以列印。</span><span class="sxs-lookup"><span data-stu-id="21b98-117">The Project accountant formats and updates the project invoice proposal, and then posts and prints the document.</span></span> <span data-ttu-id="21b98-118">已過帳的專案發票會記錄在總帳以及客戶和專案的子分類帳中。</span><span class="sxs-lookup"><span data-stu-id="21b98-118">Posted project invoices are recorded in the General ledger, as well as the Customer and Project subledgers.</span></span>
