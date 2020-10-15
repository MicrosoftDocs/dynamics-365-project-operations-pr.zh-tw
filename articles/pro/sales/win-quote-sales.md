---
title: 關閉報價
description: 本主題提供有關在 Project Operations 中關閉報價的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: cc3b2cdeb1ac46b7d927c1f96e94e9154d3eebf8
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3896181"
---
# <a name="close-quotes"></a><span data-ttu-id="a3418-103">關閉報價</span><span class="sxs-lookup"><span data-stu-id="a3418-103">Close quotes</span></span> 

<span data-ttu-id="a3418-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="a3418-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a3418-105">專案報價可以當做 [成交] 或 [未成交] 來關閉。</span><span class="sxs-lookup"><span data-stu-id="a3418-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="a3418-106">Microsoft Dynamics 365 Project Operations 不支援對報價的啟用和修訂作業，因此可以關閉草稿報價。</span><span class="sxs-lookup"><span data-stu-id="a3418-106">The Activate and Revise operations on quotes is not supported in Microsoft Dynamics 365 Project Operations, so a draft quote can be closed.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="a3418-107">以成交關閉報價</span><span class="sxs-lookup"><span data-stu-id="a3418-107">Close a quote as Won</span></span>

<span data-ttu-id="a3418-108">以 [成交] 狀態關閉專案報價，會關閉報價，並將其狀態設定為 [已關閉]，以及將狀態原因設定為 [成交]。</span><span class="sxs-lookup"><span data-stu-id="a3418-108">Closing a project quote as Won will close the quote with the status set to Closed and the status reason set to Won.</span></span> <span data-ttu-id="a3418-109">關閉報價會將專案報價變成唯讀，並建立包含報價資訊的草稿專案合約。</span><span class="sxs-lookup"><span data-stu-id="a3418-109">Closing the quote makes the project quote read-only and creates a draft project contract that contains the quote information.</span></span> <span data-ttu-id="a3418-110">已關閉的報價無法重新開啟，由於無法重新開啟已關閉的報價，而且變更是無法復原的，因此完成變更之前會出現確認對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a3418-110">Because a closed quote can't be reopened, a confirmation dialog There is a confirmation dialog before the changes are done since a closed quote cannot be re-opened and the changes are irreversible.</span></span>

<span data-ttu-id="a3418-111">如果報價已附加至商機，商機上的任何其他專案報價都會自動以 [未成交] 關閉。</span><span class="sxs-lookup"><span data-stu-id="a3418-111">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="a3418-112">以成交關閉報價的財務影響</span><span class="sxs-lookup"><span data-stu-id="a3418-112">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="a3418-113">如果專案仍附加至草稿報價時，已有任何記錄在其中的時間實際值，則只會記錄時間或費用的成本。</span><span class="sxs-lookup"><span data-stu-id="a3418-113">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="a3418-114">以 [成交] 關閉報價之後，應用程式會沖銷舊的成本實際值並重新建立新的成本實際值，以重構成本。</span><span class="sxs-lookup"><span data-stu-id="a3418-114">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="a3418-115">應用程式會根據相關聯專案合約服務內容的帳務方式處理這些成本實際值。</span><span class="sxs-lookup"><span data-stu-id="a3418-115">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="a3418-116">如果成本實際值參考時間和材料合約服務內容，系統就會自動在關閉報價並建立專案合約時建立對應的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="a3418-116">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="a3418-117">如果成本實際值參考固定價格固定價格專案，則應用程式會根據專案合約客戶的分割帳單規則停止重新處理成本實際值。</span><span class="sxs-lookup"><span data-stu-id="a3418-117">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

## <a name="closing-a-quote-as-lost"></a><span data-ttu-id="a3418-118">以未成交關閉報價：</span><span class="sxs-lookup"><span data-stu-id="a3418-118">Closing a quote as lost:</span></span>

<span data-ttu-id="a3418-119">以 [未成交] 關閉專案報價，會將狀態設定為 [已關閉]，而將狀態原因設定為 [未成交]。</span><span class="sxs-lookup"><span data-stu-id="a3418-119">Closing a project quote as Lost will set the status to Closed and status reason to Lost.</span></span> <span data-ttu-id="a3418-120">關閉報價會將專案報價設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="a3418-120">Closing the quote makes the project quote read-only.</span></span> <span data-ttu-id="a3418-121">已關閉的報價無法重新開啟，因此關閉報價之前，確認對話方塊會確認您的變更。</span><span class="sxs-lookup"><span data-stu-id="a3418-121">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="a3418-122">如果以 [未成交] 關閉的專案報價有任何明細參考專案時，該專案也會標示為 [已關閉]，而且還會取消那天以後的所有資源預約。</span><span class="sxs-lookup"><span data-stu-id="a3418-122">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="a3418-123">在 Project Operations 中，以 [成交] 或 [未成] 交關閉報價並不會影響商機的狀態，商機仍將保持開啟，直到手動將其關閉為止。</span><span class="sxs-lookup"><span data-stu-id="a3418-123">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
