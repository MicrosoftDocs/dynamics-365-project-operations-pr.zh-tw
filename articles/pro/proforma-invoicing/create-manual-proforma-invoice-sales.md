---
title: 建立手動預估發票 - 精簡
description: 本主題提供有關在 Project Operations 中建立手動預估發票的資訊。
author: rumant
manager: Annbe
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 5a924de6efc377e28a20e038e7deac04616b95aa
ms.sourcegitcommit: 2b74edd31f38410024a01124c9202a4d94464d04
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 12/17/2020
ms.locfileid: "4764493"
---
# <a name="create-a-manual-proforma-invoice---lite"></a><span data-ttu-id="613a2-103">建立手動預估發票 - 精簡</span><span class="sxs-lookup"><span data-stu-id="613a2-103">Create a manual proforma invoice - lite</span></span>

<span data-ttu-id="613a2-104">_**適用於：** 精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="613a2-104">_**Applies To:** Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="613a2-105">在 Dynamics 365 Project Operations 中，您可以視需要手動建立預估發票。</span><span class="sxs-lookup"><span data-stu-id="613a2-105">In Dynamics 365 Project Operations, proforma invoices can be created manually as needed.</span></span> <span data-ttu-id="613a2-106">您可以從 **專案合約** 清單頁面，或從 **專案合約** 詳細資料頁面手動建立預估發票。</span><span class="sxs-lookup"><span data-stu-id="613a2-106">You can manually create a proforma invoice from the **Project Contracts** list page or from the **Project Contract** details page.</span></span>

##  <a name="project-contracts-list-page"></a><span data-ttu-id="613a2-107">專案合約清單頁面</span><span class="sxs-lookup"><span data-stu-id="613a2-107">Project Contracts list page</span></span>

<span data-ttu-id="613a2-108">從 **專案合約** 清單頁面中，選取一個或多個專案合約，並為所有已選取的記錄建立發票。</span><span class="sxs-lookup"><span data-stu-id="613a2-108">From **Project Contracts** list page, select one or more project contracts, and create invoices for all of the selected records.</span></span>

<span data-ttu-id="613a2-109">系統會進行檢查，以了解哪些所選專案合約的 **已準備好開立發票** 待處理項目日期是在今天之前。</span><span class="sxs-lookup"><span data-stu-id="613a2-109">The system checks to see which of the selected project contracts has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="613a2-110">系統會從這些合約建立草稿預估發票。</span><span class="sxs-lookup"><span data-stu-id="613a2-110">From those contracts, the system creates draft proforma invoices.</span></span> <span data-ttu-id="613a2-111">如果專案合約有多個客戶，則可能會每個客戶建立一張發票，以及每個專案合約建立多張發票。</span><span class="sxs-lookup"><span data-stu-id="613a2-111">If a project contract has multiple customers, there may be one invoice created per customer, and multiple invoices per project contract.</span></span>

<span data-ttu-id="613a2-112">所有已建立的專案發票都可以在 **銷售** 區域 **帳單** 區段的 **發票** 頁面上找到。</span><span class="sxs-lookup"><span data-stu-id="613a2-112">All of the created project invoices are available on the **Invoice** page in the **Billing** section of the **Sales** area.</span></span>

## <a name="project-contract-details-page"></a><span data-ttu-id="613a2-113">專案合約詳細資料頁面</span><span class="sxs-lookup"><span data-stu-id="613a2-113">Project Contract details page</span></span>

<span data-ttu-id="613a2-114">您也可以從 **專案合約** 詳細資料頁面建立預估發票 。</span><span class="sxs-lookup"><span data-stu-id="613a2-114">A proforma invoice can also be created from the **Project Contract** details page.</span></span> <span data-ttu-id="613a2-115">系統會確認專案合約的 **已準備好開立發票** 待處理項目日期是否在今天之前。</span><span class="sxs-lookup"><span data-stu-id="613a2-115">The system verifies the project contract has a **Ready to Invoice** backlog dated before today's date.</span></span> <span data-ttu-id="613a2-116">系統會從這些合約，根據每個合約服務內容的客戶數目建立草稿預估發票。</span><span class="sxs-lookup"><span data-stu-id="613a2-116">From these contracts, the system creates draft proforma invoices based on the number of customers on each contract line.</span></span>

<span data-ttu-id="613a2-117">當有已建立的單一預估發票時，**發票** 頁面會開啟。</span><span class="sxs-lookup"><span data-stu-id="613a2-117">When there's a single proforma invoice created, the **Invoice** page opens.</span></span> <span data-ttu-id="613a2-118">如果該專案合約已建立多份發票，則 **發票** 清單頁面會開啟，以顯示所有的已建立發票。</span><span class="sxs-lookup"><span data-stu-id="613a2-118">If multiple invoices are created for that project contract, the **Invoices** list page opens to show all of the created invoices.</span></span>
