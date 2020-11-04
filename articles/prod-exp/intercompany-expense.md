---
title: 公司間費用
description: 組織中的一個法律實體所雇用的工作者，可能會為同一個組織中的其他法律實體執行工作。 在這種情況下，您可以使用公司間費用功能，將工作者的費用指派給為之執行工作的法律實體。
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
ms.openlocfilehash: 0967f23e4e1f8e0431c55d4d54554e7e90e2451c
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073147"
---
# <a name="intercompany-expenses"></a><span data-ttu-id="0c801-104">公司間費用</span><span class="sxs-lookup"><span data-stu-id="0c801-104">Intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c801-105">組織中的一個法律實體所雇用的工作者，可能會為同一個組織中的其他法律實體執行工作。</span><span class="sxs-lookup"><span data-stu-id="0c801-105">A worker who is employed by one legal entity in an organization might perform work for another legal entity in the same organization.</span></span> <span data-ttu-id="0c801-106">在這種情況下，您可以使用公司間費用功能，將工作者的費用指派給為之執行工作的法律實體。</span><span class="sxs-lookup"><span data-stu-id="0c801-106">In this situation, you can use the intercompany expense feature to assign the worker’s expenses to the legal entity for which the work was performed.</span></span> <span data-ttu-id="0c801-107">雇用該工作者的法律實體稱為出借法律實體。</span><span class="sxs-lookup"><span data-stu-id="0c801-107">The legal entity that employs the worker is called the loaning legal entity.</span></span> <span data-ttu-id="0c801-108">承擔工作者所產生費用的法律實體稱為借用法律實體。</span><span class="sxs-lookup"><span data-stu-id="0c801-108">The legal entity for which the worker incurs expenses is called the borrowing legal entity.</span></span> 

<span data-ttu-id="0c801-109">工作者在出借法律實體的 **費用管理參數** 頁面上針對他為不同法律實體執行的工作建立並提交費用之前，請選取 **允許公司間的費用明細** 選項。</span><span class="sxs-lookup"><span data-stu-id="0c801-109">Before a worker can create and submit expenses for work that is performed for a different legal entity, in the loaning legal entity, on the **Expense management parameters** page, select the **Allow intercompany expense lines** option.</span></span> 

## <a name="tax-posting-for-intercompany-expenses"></a><span data-ttu-id="0c801-110">公司間費用的稅金過帳</span><span class="sxs-lookup"><span data-stu-id="0c801-110">Tax posting for intercompany expenses</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="0c801-111">如果您想要在費用報表中使用與出借 (來源) 法律實體相關，而不是與借用 (目的地) 法律實體相關的課稅群組，就必須在總帳銷售稅設定中設定此關聯。</span><span class="sxs-lookup"><span data-stu-id="0c801-111">If you want to use tax groups that are associated with the loaning (source) legal entity instead of the borrowing (destination) legal entity in your expense report, you will need to configure this in the General ledger sales tax set up.</span></span> <span data-ttu-id="0c801-112">將總帳參數 **公司間稅金過帳法律實體** 設定為 **來源** ，並將 **套用銷售稅課稅規則** 設定為 **否** 時，將會使用出借法律實體的稅務組合。</span><span class="sxs-lookup"><span data-stu-id="0c801-112">When the General ledger parameter, **Legal entity for intercompany tax posting** is set to **Source** and **Apply sales tax taxation rules** is set to **No** , the tax combination for the loaning legal entity will be used.</span></span> <span data-ttu-id="0c801-113">如果將這同一個參數設定為 **目的地** ，則會使用借用法律實體的稅務組合。</span><span class="sxs-lookup"><span data-stu-id="0c801-113">When the same parameter is set to **Destination** , the tax combination for borrowing legal entity will be used.</span></span> <span data-ttu-id="0c801-114">如果是在美國的法律實體，將此參數設定為 **來源** 時，也必須在新的 **總帳過帳群組** 頁面上設定 **應收銷售稅** 欄位。</span><span class="sxs-lookup"><span data-stu-id="0c801-114">For legal entities in the United States, when the parameter is set to **Source** , the **Sales tax receivable** field must also be configured on the new **Ledger posting groups** page.</span></span> <span data-ttu-id="0c801-115">會計引擎將會將此欄位中的資訊用於稅務相關的會計分錄。</span><span class="sxs-lookup"><span data-stu-id="0c801-115">The accounting engine will use the information from this field for tax related accounting entry.</span></span>   
<span data-ttu-id="0c801-116">不論過帳的費用明細是否與專案有關，其行為都是一致的。</span><span class="sxs-lookup"><span data-stu-id="0c801-116">The behavior is consistent for expense lines posted with or without a project.</span></span>  
