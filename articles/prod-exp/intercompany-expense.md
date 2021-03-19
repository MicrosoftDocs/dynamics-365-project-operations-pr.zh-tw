---
title: 公司間費用
description: 本主題提供相關資訊，說明如何使用公司間費用，以將工作者的費用指派給執行工作所效勞的法律實體。
author: ShylaThompson
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d908a1c062f5b7f01cf340dcd6f7f24714a992bf
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5271523"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="4ad91-103">公司間費用</span><span class="sxs-lookup"><span data-stu-id="4ad91-103">Intercompany expenses</span></span>

<span data-ttu-id="4ad91-104">組織中的一個法律實體所雇用的工作者，可能會為同一個組織中的其他法律實體執行工作。</span><span class="sxs-lookup"><span data-stu-id="4ad91-104">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="4ad91-105">您可以使用公司間費用，將工作者的費用指派給執行工作所效勞的法律實體。</span><span class="sxs-lookup"><span data-stu-id="4ad91-105">You can use intercompany expenses to assign the worker’s expenses to the legal entity for which the  work was performed.</span></span> <span data-ttu-id="4ad91-106">雇用該工作者的法律實體稱為出借法律實體。</span><span class="sxs-lookup"><span data-stu-id="4ad91-106">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="4ad91-107">承擔工作者所產生費用的法律實體稱為借用法律實體。</span><span class="sxs-lookup"><span data-stu-id="4ad91-107">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="4ad91-108">在工作者可以建立並提交公司間費用之前，您必須先啟用公司間費用明細。</span><span class="sxs-lookup"><span data-stu-id="4ad91-108">Before a worker can create and submit intercompany expenses, you must enable intercompany expense lines.</span></span> <span data-ttu-id="4ad91-109">在出借法律實體的 **費用管理參數** 頁面上，選取 **允許公司間費用明細**。</span><span class="sxs-lookup"><span data-stu-id="4ad91-109">In the loaning legal entity, on the **Expense management parameters** page, select **Allow intercompany expense lines**.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="4ad91-110">公司間費用的稅金過帳</span><span class="sxs-lookup"><span data-stu-id="4ad91-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="4ad91-111">您必須先啟用總帳銷售稅設定中的功能，才能在費用報表中使用與出借 (來源) 法律實體 (而非借用 (目的地) 法律實體) 相關的課稅群組。</span><span class="sxs-lookup"><span data-stu-id="4ad91-111">Before you can use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you must enable the functionality in the General ledger sales tax setup.</span></span> <span data-ttu-id="4ad91-112">當 **公司間稅務過帳法律實體** 參數設定為 **來源**，且 **套用銷售稅課稅規則** 設定為 **否** 時，會使用出借法律實體的稅務組合。</span><span class="sxs-lookup"><span data-stu-id="4ad91-112">When the **Legal entity for intercompany tax posting** parameter is set to **Source** and **Apply sales tax taxation rules** is set to **No**, the tax combination for the loaning legal entity is used.</span></span> <span data-ttu-id="4ad91-113">如果將這同一個參數設定為 **目的地**，則會使用借用法律實體的稅務組合。</span><span class="sxs-lookup"><span data-stu-id="4ad91-113">When the same parameter is set to **Destination**, the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="4ad91-114">如果是在美國的法律實體，將此參數設定為 **來源** 時，也必須在新的 **總帳過帳群組** 頁面上設定 **應收銷售稅** 欄位。</span><span class="sxs-lookup"><span data-stu-id="4ad91-114">For legal entities in the United States, when the parameter is set to **Source**, the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="4ad91-115">會計引擎將會將此欄位中的資訊用於稅務相關的會計分錄。</span><span class="sxs-lookup"><span data-stu-id="4ad91-115">The accounting engine will use the information from this field for tax-related accounting entry.</span></span>   
<span data-ttu-id="4ad91-116">不論過帳的費用明細是否與專案有關，其行為都是一致的。</span><span class="sxs-lookup"><span data-stu-id="4ad91-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  


[!INCLUDE[footer-include](../includes/footer-banner.md)]