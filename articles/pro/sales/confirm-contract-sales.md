---
title: 確認專案合約
description: 本主題提供有關如何在 Project Operations 中確認合約的資訊。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: d807d3631f40a93ec7dbd918b64c287fd4875c79
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5273818"
---
# <a name="confirm-a-project-contract"></a><span data-ttu-id="00539-103">確認專案合約</span><span class="sxs-lookup"><span data-stu-id="00539-103">Confirm a project contract</span></span>

<span data-ttu-id="00539-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="00539-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="00539-105">Dynamics 365 Project Operations 中的專案合約可以使用 **已確認** 的原因進入使用中狀態，或使用 **未成交** 的原因進入已關閉狀態。</span><span class="sxs-lookup"><span data-stu-id="00539-105">A project contract in Dynamics 365 Project Operations can be active with a reason of **Confirmed**, or closed with a reason of **Lost**.</span></span> <span data-ttu-id="00539-106">確認專案合約時，狀態會從 **草稿** 更新為 **使用中**，而且狀態原因為 **已確認**。</span><span class="sxs-lookup"><span data-stu-id="00539-106">When you confirm a project contract, the status updates from **Draft** to **Active** and the status reason is **Confirmed**.</span></span> <span data-ttu-id="00539-107">您無法編輯或重新開啟使用中或已關閉的合約。</span><span class="sxs-lookup"><span data-stu-id="00539-107">An active or closed contract can't be edited or reopened.</span></span> 

### <a name="financial-impact-of-confirming-a-project-contract"></a><span data-ttu-id="00539-108">確認專案合約所產生的財務影響</span><span class="sxs-lookup"><span data-stu-id="00539-108">Financial impact of confirming a project contract</span></span>

<span data-ttu-id="00539-109">確認專案合約之後，應用程式會沖銷舊的成本實際值並建立新的成本實際值，以重新計算成本。</span><span class="sxs-lookup"><span data-stu-id="00539-109">After a project contract is confirmed, the application recalculates the costs by reversing the older cost actuals and creating new cost actuals.</span></span> <span data-ttu-id="00539-110">接著會根據相關聯專案合約服務內容的帳務方式處理新的成本實際值。</span><span class="sxs-lookup"><span data-stu-id="00539-110">The new cost actuals are then processed based on the billing method of the associated project contract line.</span></span> <span data-ttu-id="00539-111">如果成本實際值參考時間和材料合約服務內容，則應用程式會自動重新建立對應的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="00539-111">If the cost actuals reference a Time and Material contract line, the application automatically re-creates corresponding unbilled sales actuals.</span></span> <span data-ttu-id="00539-112">如果成本實際值參考固定價格合約服務內容，則應用程式會停止重新處理成本實際值。</span><span class="sxs-lookup"><span data-stu-id="00539-112">If the cost actuals reference a Fixed Price contract line, the application stops reprocessing the cost actuals.</span></span>

<span data-ttu-id="00539-113">系統會評估對實際值的不得超過限制、可收費率設定、定價和成本計算，並在確認程序期間加以更新。</span><span class="sxs-lookup"><span data-stu-id="00539-113">Not-to-exceed limits, chargeability setup, and pricing and costing on the actuals is evaluated and then updated as part of the confirmations process.</span></span>

## <a name="close-a-project-contract-as-lost"></a><span data-ttu-id="00539-114">以未成交關閉專案合約</span><span class="sxs-lookup"><span data-stu-id="00539-114">Close a project contract as lost</span></span>

<span data-ttu-id="00539-115">以未成交關閉專案合約時，合約狀態會更新為 **已關閉**，而且狀態原因為 **未成交**。</span><span class="sxs-lookup"><span data-stu-id="00539-115">When you close a project contract as lost, the contract status is updated to **Closed** and the status reason is **Lost**.</span></span> <span data-ttu-id="00539-116">專案合約會變成唯讀。</span><span class="sxs-lookup"><span data-stu-id="00539-116">The project contract becomes read-only.</span></span> <span data-ttu-id="00539-117">因為您無法重新開啟已關閉的專案合約，系統會在變更完成之前提供確認對話方塊。</span><span class="sxs-lookup"><span data-stu-id="00539-117">A confirmation dialog is provided before the changes are complete because you can't reopen a closed project contract.</span></span>

<span data-ttu-id="00539-118">如果以未成交關閉的專案合約在其服務內容中參考某個專案，也會將這個專案標示為已關閉。</span><span class="sxs-lookup"><span data-stu-id="00539-118">If the project contract that is closed as lost references a project on its lines, that project is also marked as closed.</span></span> <span data-ttu-id="00539-119">任何從那天以後的資源預約都會取消。</span><span class="sxs-lookup"><span data-stu-id="00539-119">Any resource bookings from that day forward are canceled.</span></span> <span data-ttu-id="00539-120">專案合約中任何尚未列於發票的未開單銷售實際值都將予以沖銷。</span><span class="sxs-lookup"><span data-stu-id="00539-120">Any unbilled sales actuals on the project contract that aren't already on an invoice, will be reversed.</span></span>

> [!NOTE]
> <span data-ttu-id="00539-121">在 Dynamics 365 Project Operations 中，以未成交來關閉專案合約並不會影響相關商機的狀態。</span><span class="sxs-lookup"><span data-stu-id="00539-121">In Dynamics 365 Project Operations, closing a project contract as lost will not impact that status of the associated opportunity.</span></span> <span data-ttu-id="00539-122">商機仍將保持開啟，並必須以手動方式關閉。</span><span class="sxs-lookup"><span data-stu-id="00539-122">The opportunity will remain open and must be manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]