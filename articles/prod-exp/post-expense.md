---
title: 將費用報表過帳
description: 本主題說明如何將費用報表過帳至總帳。
author: saraschi2
manager: AnnBe
ms.date: 02/26/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: TrvPerDiems
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 2d008ef8dd55550431fbb9e329cd7d9428a08831
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073142"
---
# <a name="post-an-expense-report"></a><span data-ttu-id="8d886-103">將費用報表過帳</span><span class="sxs-lookup"><span data-stu-id="8d886-103">Post an expense report</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8d886-104">費用報表經核准並轉入一般帳目之後，即可將其過帳至總帳。</span><span class="sxs-lookup"><span data-stu-id="8d886-104">After an expense report has been approved and transferred to the general journal, it can be posted to the general ledger.</span></span> <span data-ttu-id="8d886-105">將費用報表過帳時，系統會識別符合退還加值稅 (VAT) 資格的費用。</span><span class="sxs-lookup"><span data-stu-id="8d886-105">When you post an expense report, expenses that are eligible for recovery of value-added tax (VAT) are identified.</span></span> <span data-ttu-id="8d886-106">驗證和退還加值稅付款的工作會指派給負責驗證費用報表的員工。</span><span class="sxs-lookup"><span data-stu-id="8d886-106">The task of verifying and recovering VAT payments is assigned to the employee who is responsible for verifying the expense report.</span></span>

<span data-ttu-id="8d886-107">如果費用報表上的費用是向該員工雇用公司以外的公司收取，您必須驗證應收這些費用的公司以及應付這些費用的公司。</span><span class="sxs-lookup"><span data-stu-id="8d886-107">If expenses on an expense report are charged to a company other than the company that employs the employee, you must verify the company that those expenses are owed to and the company that the expenses are owed from.</span></span> <span data-ttu-id="8d886-108">例如，提交費用報表的員工任職於 DAT 公司，但是向 DIR 公司收取了費用。</span><span class="sxs-lookup"><span data-stu-id="8d886-108">For example, the employee who submitted an expense report works for the DAT company but charged an expense to the DIR company.</span></span> <span data-ttu-id="8d886-109">在這種情況下，DAT 是應付費用的公司，而 DIR 是應收費用的公司。</span><span class="sxs-lookup"><span data-stu-id="8d886-109">In this case, DAT is the company that the expense is owed to, and DIR is the company that the expense is owed from.</span></span> <span data-ttu-id="8d886-110">驗證這些帳目明細之後，您可以將費用明細過帳至總帳。</span><span class="sxs-lookup"><span data-stu-id="8d886-110">After you verify these journal lines, you can post the expense lines to the general ledger.</span></span>

<span data-ttu-id="8d886-111">若要將費用報表過帳，請在 **核准的費用報表** 頁面上選取費用報表，然後在動作窗格中選取 **過帳** 。</span><span class="sxs-lookup"><span data-stu-id="8d886-111">To post an expense report, on the **Approved expense reports** page, select the expense report, and then, on the Action Pane, select **Post**.</span></span>

<span data-ttu-id="8d886-112">您也可以同時將清單中所有的費用報表過帳。</span><span class="sxs-lookup"><span data-stu-id="8d886-112">You can also post all the expense reports in the list at the same time.</span></span> <span data-ttu-id="8d886-113">選取所有費用報表，然後選取 **過帳** 。</span><span class="sxs-lookup"><span data-stu-id="8d886-113">Select all the expense reports, and then select **Post**.</span></span>
