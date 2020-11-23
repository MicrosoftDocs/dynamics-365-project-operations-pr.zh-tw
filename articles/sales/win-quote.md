---
title: 關閉報價
description: 本主題提供有關在 Project Operations 中關閉報價的資訊。
author: rumant
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 47804db0144c2b0f9dee2c60518e8aba6fb27473
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4124673"
---
# <a name="close-a-quote"></a><span data-ttu-id="14252-103">關閉報價</span><span class="sxs-lookup"><span data-stu-id="14252-103">Close a quote</span></span>

<span data-ttu-id="14252-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="14252-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="14252-105">專案報價可以當做 [成交] 或 [未成交] 來關閉。</span><span class="sxs-lookup"><span data-stu-id="14252-105">A project quote can be closed as Won or Lost.</span></span> <span data-ttu-id="14252-106">Microsoft Dynamics 365 Project Operations 中的報價不支援啟用和修訂功能，因此您可以關閉草稿報價。</span><span class="sxs-lookup"><span data-stu-id="14252-106">Because the functions Activate and Revise are not supported on quotes in Microsoft Dynamics 365 Project Operations, you can close a draft quote.</span></span>

## <a name="close-a-quote-as-won"></a><span data-ttu-id="14252-107">以成交關閉報價</span><span class="sxs-lookup"><span data-stu-id="14252-107">Close a quote as Won</span></span>

<span data-ttu-id="14252-108">以 [成交] 狀態關閉專案報價，會將報價的狀態設定為 **已關閉**，並將狀態原因設定為 **成交**。</span><span class="sxs-lookup"><span data-stu-id="14252-108">Closing a project quote as Won will set the status of the quote to **Closed** and status reason to **Won**.</span></span> <span data-ttu-id="14252-109">關閉報價會將其設定為唯讀，並建立包含所有報價資訊的草稿專案合約。</span><span class="sxs-lookup"><span data-stu-id="14252-109">Closing the quotes makes it read-only and creates a draft project contract with all the quote information.</span></span> <span data-ttu-id="14252-110">已關閉的報價無法重新開啟，因此關閉報價之前，確認對話方塊將會確認您的變更。</span><span class="sxs-lookup"><span data-stu-id="14252-110">Because a closed quote can't be reopened, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="14252-111">Project Operations 的 [專案管理與會計] 模組也已提供根據專案合約所建立的專案報價。</span><span class="sxs-lookup"><span data-stu-id="14252-111">The project contract created from a project quote is also made available in the Project management and accounting module of Project Operations.</span></span> <span data-ttu-id="14252-112">如果專案合約未對應至其任何明細上的專案，則此專案合約會提供做為非使用中專案合約，並在專案至少對應到其中一項合約明細時變成使用中狀態。</span><span class="sxs-lookup"><span data-stu-id="14252-112">If a project contract is not mapped to a project on any of its lines, this project contract is made available as an inactive project contract and becomes active as soon as a project is mapped to at least one of its contract lines.</span></span>

<span data-ttu-id="14252-113">如果報價已附加至商機，商機上的任何其他專案報價都會自動以 [未成交] 關閉。</span><span class="sxs-lookup"><span data-stu-id="14252-113">If the quote is attached to an opportunity, any other project quotes on the opportunity are automatically closed as Lost.</span></span>

### <a name="financial-impact-of-closing-a-quote-as-won"></a><span data-ttu-id="14252-114">以成交關閉報價的財務影響</span><span class="sxs-lookup"><span data-stu-id="14252-114">Financial impact of closing a quote as Won</span></span>

<span data-ttu-id="14252-115">如果專案仍附加至草稿報價時，已有任何記錄在其中的時間實際值，則只會記錄時間或費用的成本。</span><span class="sxs-lookup"><span data-stu-id="14252-115">If there have been any actuals for time recorded on a project while it is still attached to a draft quote, only the cost of the time or expense is recorded.</span></span> <span data-ttu-id="14252-116">以 [成交] 關閉報價之後，應用程式會沖銷舊的成本實際值並重新建立新的成本實際值，以重構成本。</span><span class="sxs-lookup"><span data-stu-id="14252-116">After a quote is closed as Won, the application will refactor the costs by reversing the older cost actuals and re-creating new cost actuals.</span></span> <span data-ttu-id="14252-117">應用程式會根據相關聯專案合約服務內容的帳務方式處理這些成本實際值。</span><span class="sxs-lookup"><span data-stu-id="14252-117">The application will process these cost actuals based on the Billing method of the associated project contract line.</span></span> <span data-ttu-id="14252-118">如果成本實際值參考時間和材料合約服務內容，系統就會自動在關閉報價並建立專案合約時建立對應的未開單銷售實際值。</span><span class="sxs-lookup"><span data-stu-id="14252-118">If the cost actuals reference a time and material contract line, the system will automatically create corresponding unbilled sales actuals for when the quote is closed and the project contract is created.</span></span> <span data-ttu-id="14252-119">如果成本實際值參考固定價格固定價格專案，則應用程式會根據專案合約客戶的分割帳單規則停止重新處理成本實際值。</span><span class="sxs-lookup"><span data-stu-id="14252-119">If the cost actuals reference a fixed price contract line, the application will stop reprocessing the cost actuals based on the split billing rules for the project contract customers.</span></span>

<span data-ttu-id="14252-120">所有重新處理的實際值皆可在 [專案管理與稽核] 模組中取得，以供專案會計師審查、更新並過帳至總帳。</span><span class="sxs-lookup"><span data-stu-id="14252-120">All reprocessed actuals are available in the Project management and accounting module for the Project accountant to review, update, and post to the General ledger.</span></span> 

## <a name="close-a-quote-as-lost"></a><span data-ttu-id="14252-121">以未成交關閉報價</span><span class="sxs-lookup"><span data-stu-id="14252-121">Close a quote as Lost</span></span>

<span data-ttu-id="14252-122">以 [未成交] 關閉專案報價，會將狀態設定為 **已關閉**，而將狀態原因設定為 **未成交**。</span><span class="sxs-lookup"><span data-stu-id="14252-122">Closing a project quote as Lost will set the status to **Closed** and status reason to **Lost**.</span></span> <span data-ttu-id="14252-123">關閉報價會將其設定為唯讀。</span><span class="sxs-lookup"><span data-stu-id="14252-123">Closing the quote makes it read-only.</span></span> <span data-ttu-id="14252-124">已關閉的報價無法重新開啟，因此關閉報價之前，確認對話方塊會確認您的變更。</span><span class="sxs-lookup"><span data-stu-id="14252-124">Because a closed quote can't be reopened and, before you close a quote, a confirmation dialog will confirm your changes.</span></span>

<span data-ttu-id="14252-125">如果以 [未成交] 關閉的專案報價有任何明細參考專案時，該專案也會標示為 [已關閉]，而且還會取消那天以後的所有資源預約。</span><span class="sxs-lookup"><span data-stu-id="14252-125">If the project quote that is closed as Lost has a project referenced on any of its lines, that project is also marked as Closed and any resource bookings from that day forward are canceled.</span></span>

> [!NOTE]
> <span data-ttu-id="14252-126">在 Project Operations 中，以 [成交] 或 [未成] 交關閉報價並不會影響商機的狀態，商機仍將保持開啟，直到手動將其關閉為止。</span><span class="sxs-lookup"><span data-stu-id="14252-126">In Project Operations, closing a quote as Won or Lost will not impact that status of the Opportunity, which will remain open until it is manually closed.</span></span>
