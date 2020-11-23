---
title: 解析估計值及實際值的成本價
description: 本主題提供有關如何解析估計值及實際值成本價的資訊。
author: rumant
manager: Annbe
ms.date: 10/13/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: c447e725753d738662f33cc9a5f20ec1a72b2e18
ms.sourcegitcommit: 4cf1dc1561b92fca4175f0b3813133c5e63ce8e6
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/28/2020
ms.locfileid: "4119679"
---
# <a name="resolving-cost-prices-for-estimates-and-actuals"></a><span data-ttu-id="3724c-103">解析估計值及實際值的成本價</span><span class="sxs-lookup"><span data-stu-id="3724c-103">Resolving cost prices for estimates and actuals</span></span>

<span data-ttu-id="3724c-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="3724c-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="3724c-105">為了解析成本價以及估計值與實際值的成本價目表，系統會使用相關專案的 **日期**、**貨幣** 和 **合約單位** 欄位中的資訊。</span><span class="sxs-lookup"><span data-stu-id="3724c-105">To resolve cost prices and the cost price list for estimates and actuals, the system uses the information in the **Date**, **Currency**, and **Contracting Unit** fields of the related project.</span></span> <span data-ttu-id="3724c-106">解析成本價目表之後，應用程式會解析成本費率。</span><span class="sxs-lookup"><span data-stu-id="3724c-106">After the cost price list is resolved, the application resolves the cost rate.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-time"></a><span data-ttu-id="3724c-107">解析時間實際及估計明細的成本費率</span><span class="sxs-lookup"><span data-stu-id="3724c-107">Resolving cost rates on actual and estimate lines for Time</span></span>

<span data-ttu-id="3724c-108">時間的估計明細是指專案上時間和資源指派的報價及合約服務內容詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3724c-108">Estimate lines for Time refer to the quote and contract line details for time and resource assignments on a project.</span></span>

<span data-ttu-id="3724c-109">解析成本價目表之後，系統會使用時間估計明細上的 **角色**、**資源供應公司** 和 **資源分配單位** 欄位，來比對價目表中的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="3724c-109">After a cost price list is resolved, the system uses the **Role**, **Resourcing Company**, and **Resourcing Unit** fields on the estimate line for Time to match against the role price lines in the price list.</span></span> <span data-ttu-id="3724c-110">這項比對作業假設您正在對人力成本使用現成可用的定價維度。</span><span class="sxs-lookup"><span data-stu-id="3724c-110">This match assumes that you are using out-of-the-box pricing dimensions for labor cost.</span></span> <span data-ttu-id="3724c-111">如果您將系統設定成比對排除或附加 **角色**、**資源供應公司** 及 **資源分配單位** 的欄位，則會使用不同的組合來擷取相符的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="3724c-111">If you configured the system to match fields instead of, or in addition to **Role**, **Resourcing Company**, and **Resourcing Unit**, then a different combination will be used to retrieve a matching role price line.</span></span> <span data-ttu-id="3724c-112">如果應用程式找到具有 **角色**、**資源供應公司** 及 **資源分配單** 位組合成本費率的角色價格明細，那就是預設成本費率。</span><span class="sxs-lookup"><span data-stu-id="3724c-112">If the application finds a role price line that has a cost rate for the **Role**, **Resourcing Company**, and **Resourcing Unit** combination, that is the default cost rate.</span></span> <span data-ttu-id="3724c-113">如果應用程式找不到與 **角色**、**資源供應公司** 及 **資源分配單位** 值相符的項目，則會擷取具有相符角色但 **資源分配單位** 值為 Null 的角色價格明細。</span><span class="sxs-lookup"><span data-stu-id="3724c-113">If the application can't match the **Role**, **Resourcing Company**, and **Resourcing Unit** values, then it retrieves role price lines with a matching role, but null values of the **Resourcing Unit**.</span></span> <span data-ttu-id="3724c-114">找到相符的角色價格記錄之後，成本費率將預設為該記錄中的預設值。</span><span class="sxs-lookup"><span data-stu-id="3724c-114">After it has a matching role price record, the cost rate defaults from that record.</span></span> 

> [!NOTE]
> <span data-ttu-id="3724c-115">如果您設定不同的 **角色**、**資源供應公司** 及 **資源分配單位** 優先順序，或者您有其他較高優先順序的維度，則此行為也會相應變更。</span><span class="sxs-lookup"><span data-stu-id="3724c-115">If you configure a different prioritization of **Role**, **Resourcing Company**, and **Resourcing Unit**, or if you have other dimensions that have higher priority, this behavior will change accordingly.</span></span> <span data-ttu-id="3724c-116">系統會依照以那些有列值為 Null 之定價維度居後的優先順序，擷取其值符合每個定價維度值的角色價格記錄。</span><span class="sxs-lookup"><span data-stu-id="3724c-116">The system retrieves role price records with values that match each of the pricing dimension values in order of priority with rows that have null values for those dimensions coming last.</span></span>

## <a name="resolving-cost-rates-on-actual-and-estimate-lines-for-expense"></a><span data-ttu-id="3724c-117">解析費用實際及估計明細的成本費率</span><span class="sxs-lookup"><span data-stu-id="3724c-117">Resolving cost rates on actual and estimate lines for Expense</span></span>

<span data-ttu-id="3724c-118">費用的估計明細是指專案上費用和費用估計明細的報價及合約服務內容詳細資料。</span><span class="sxs-lookup"><span data-stu-id="3724c-118">Estimate lines for Expense refer to the quote and contract line details for expenses and the expense estimate lines on a project.</span></span>

<span data-ttu-id="3724c-119">解析成本價目表之後，系統會使用費用估計明細上的 **類別** 與 **單位** 欄位組合，來比對解析後價目表中的 **類別價格** 明細。</span><span class="sxs-lookup"><span data-stu-id="3724c-119">After a cost price list is resolved, the system uses a combination of the **Category** and **Unit** fields on the estimate line for an expense to match against the **Category Price** lines on the resolved price list.</span></span> <span data-ttu-id="3724c-120">如果系統找到具有 **類別** 與 **單位** 欄位組合成本費率的類別價格明細，則預設使用該成本費率。</span><span class="sxs-lookup"><span data-stu-id="3724c-120">If the system finds a category price line that has a cost rate for the **Category** and **Unit** field combination, the cost rate is defaulted.</span></span> <span data-ttu-id="3724c-121">如果系統找不到相符的 **類別** 與 **單位** 值，或者可以找到相符類別價格明細，但定價方式並非 **單價**，則成本費率預設為零 (0)。</span><span class="sxs-lookup"><span data-stu-id="3724c-121">If the system can't match the **Category** and **Unit** values, or if it is able to find a matching category price line but the pricing method is not **Price Per Unit**, the cost rate is defaulted to zero(0).</span></span>
