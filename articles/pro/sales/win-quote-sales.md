---
title: 結束報價 - 精簡
description: 本主題提供有關在 Project Operations 中關閉報價的資訊。
author: rumant
ms.date: 10/01/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 75345fed57dcbdb84f2a82587c7d0c152530c72b
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5994126"
---
# <a name="close-a-quote---lite"></a><span data-ttu-id="33212-103">結束報價 - 精簡</span><span class="sxs-lookup"><span data-stu-id="33212-103">Close a quote - lite</span></span>

<span data-ttu-id="33212-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="33212-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="33212-105">專案報價可以當做 [成交] 或 [未成交] 來關閉。</span><span class="sxs-lookup"><span data-stu-id="33212-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="33212-106">您可以關閉草稿報價，因為 Microsoft Dynamics 365 Project Operations 不支援對報價進行的啟用和修訂作業。</span><span class="sxs-lookup"><span data-stu-id="33212-106">A draft quote can be closed because the Activate and Revise operations on quotes isn't supported in Microsoft Dynamics 365 Project Operations.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="33212-107">以成交關閉報價</span><span class="sxs-lookup"><span data-stu-id="33212-107">Close a quote as Won</span></span>

<span data-ttu-id="33212-108">將專案報價關閉為 [成交] 時，狀態會設定為 [已關閉]，而狀態原因是 [成交]。</span><span class="sxs-lookup"><span data-stu-id="33212-108">When you close a project quote as Won, the status is set to Closed and the status reason is Won.</span></span> <span data-ttu-id="33212-109">關閉報價會將專案報價變成唯讀，並建立包含報價資訊的草稿專案合約。</span><span class="sxs-lookup"><span data-stu-id="33212-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="33212-110">因為無法重新開啟已關閉的報價，確認對話方塊將會確認您的變更。</span><span class="sxs-lookup"><span data-stu-id="33212-110">Because a closed quote can't be reopened, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="33212-111">如果報價已附加至商機，商機上的任何其他專案報價都會自動以 [未成交] 關閉。</span><span class="sxs-lookup"><span data-stu-id="33212-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="33212-112">以成交關閉報價的財務影響</span><span class="sxs-lookup"><span data-stu-id="33212-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="33212-113">如果仍附加至草稿報價時，專案上的時間有任何實際值，則只會記錄時間或費用的成本。</span><span class="sxs-lookup"><span data-stu-id="33212-113">If there are any actuals for time on a project while is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="33212-114">以 [成交] 關閉報價之後，應用程式會沖銷舊的成本實際值並重新建立新的成本實際值，以重構成本。</span><span class="sxs-lookup"><span data-stu-id="33212-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="33212-115">應用程式會根據相關聯專案合約服務內容的帳務方式處理這些成本實際值。</span><span class="sxs-lookup"><span data-stu-id="33212-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="33212-116">如果成本實際值參考時間和材料合約服務內容，就會在關閉報價並建立專案合約時，建立其對應的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="33212-116">If the cost actuals reference a time and material contract line, corresponding unbilled sales actuals are created for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="33212-117">如果成本實際值參考固定價格合約服務內容，則應用程式會停止重新處理根據專案合約客戶分割帳單規則所定的成本實際值。</span><span class="sxs-lookup"><span data-stu-id="33212-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals that are based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="33212-118">以未成交關閉報價：</span><span class="sxs-lookup"><span data-stu-id="33212-118">Closing a quote as lost:</span></span>

<span data-ttu-id="33212-119">將專案報價關閉為 [未成交] 時，狀態會設定為 [已關閉]，而狀態原因是 [未成交]。</span><span class="sxs-lookup"><span data-stu-id="33212-119">When you close a project quote as Lost, the status is set to Closed and status reason is Lost.</span></span> <span data-ttu-id="33212-120">關閉報價會將專案報價設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="33212-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="33212-121">已關閉的報價無法重新開啟，因此關閉報價之前，確認對話方塊會確認您的變更。</span><span class="sxs-lookup"><span data-stu-id="33212-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="33212-122">如果以 [未成交] 關閉的專案報價參考其任一明細上專案，該專案也會標示為 [已關閉]。</span><span class="sxs-lookup"><span data-stu-id="33212-122">If the project quote that is closed as Lost references a project on any of its lines, that project is also marked as Closed.</span></span> <span data-ttu-id="33212-123">任何從那天以後的資源預約都會取消。</span><span class="sxs-lookup"><span data-stu-id="33212-123">Any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="33212-124">在 Project Operations 中，以 [成交] 或 [未成] 交關閉報價並不會影響商機的狀態，商機仍將保持開啟，直到手動將其關閉為止。</span><span class="sxs-lookup"><span data-stu-id="33212-124">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]