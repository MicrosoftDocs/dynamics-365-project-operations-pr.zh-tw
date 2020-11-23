---
title: 管理專案報價
description: 本主題提供有關專案報價的資訊。
author: rumant
manager: Annbe
ms.date: 10/26/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: 3c33adabbd03cca19ae5e7f401f08a716e9242b2
ms.sourcegitcommit: 625878bf48ea530f3381843be0e778cebbbf1922
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/30/2020
ms.locfileid: "4177816"
---
# <a name="manage-project-quotes"></a><span data-ttu-id="c68f1-103">管理專案報價</span><span class="sxs-lookup"><span data-stu-id="c68f1-103">Manage project quotes</span></span>

<span data-ttu-id="c68f1-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="c68f1-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="c68f1-105">在 Dynamics 365 Project Operations 中，專案報價的設計目的是為了協助建置專案工作的提案。</span><span class="sxs-lookup"><span data-stu-id="c68f1-105">In Dynamics 365 Project Operations, project quotes are designed to help build proposals for project work.</span></span> <span data-ttu-id="c68f1-106">在 Project Operations 中，專案報價的結構是針對具有以下元件的專案提案而建構的：</span><span class="sxs-lookup"><span data-stu-id="c68f1-106">The structure of a project quote in Project Operations is structured for project proposals with the following components:</span></span>

  - <span data-ttu-id="c68f1-107">報價明細，識別將呈現為高階元件之工作的離散元件。</span><span class="sxs-lookup"><span data-stu-id="c68f1-107">Quote lines that identify the discrete components of work that will be presented as high-level components.</span></span>
  - <span data-ttu-id="c68f1-108">報價明細詳細資料，識別並估計每個高階元件或報價明細的工作。</span><span class="sxs-lookup"><span data-stu-id="c68f1-108">Quote line details that identify and estimate the work for each high-level component or quote line.</span></span> <span data-ttu-id="c68f1-109">排程或日期估計，以及關聯至報價明細的工作財務方面。</span><span class="sxs-lookup"><span data-stu-id="c68f1-109">Schedule or date estimates and the financial aspects for the work are tied to that quote line.</span></span>
  - <span data-ttu-id="c68f1-110">會為每個報價明細設定合約模型與應收費元件。</span><span class="sxs-lookup"><span data-stu-id="c68f1-110">Contracting models and chargeable components are set up for each quote line.</span></span> <span data-ttu-id="c68f1-111">此設定有助於估計每個報價明細和整體報價的營收、支出和獲利率的分佈。</span><span class="sxs-lookup"><span data-stu-id="c68f1-111">This set up helps estimate the spread of revenue, spend, and profitability for each quote line and the overall quote.</span></span>

## <a name="view-all-project-based-quotes"></a><span data-ttu-id="c68f1-112">檢視所有專案型報價</span><span class="sxs-lookup"><span data-stu-id="c68f1-112">View all project-based quotes</span></span>

<span data-ttu-id="c68f1-113">您可以在 **報價** 清單頁面上看到所有專案報價的清單。</span><span class="sxs-lookup"><span data-stu-id="c68f1-113">A list of all the project quotes can be seen from the **Quotes** list page.</span></span> 

1. <span data-ttu-id="c68f1-114">移至 **銷售** > **報價**。</span><span class="sxs-lookup"><span data-stu-id="c68f1-114">Go to **Sales** > **Quotes**.</span></span> <span data-ttu-id="c68f1-115">會顯示系統中所有專案報價的清單。</span><span class="sxs-lookup"><span data-stu-id="c68f1-115">A list of all your project quotes in the system are shown.</span></span> 
2. <span data-ttu-id="c68f1-116">使用 **檢視表切換器** 選取報價的其他篩選過的檢視。</span><span class="sxs-lookup"><span data-stu-id="c68f1-116">Use the **View Switcher** to select other filtered views of the quotes.</span></span> <span data-ttu-id="c68f1-117">您可以使用自訂篩選準則來設定自己的檢視和導覽選項。</span><span class="sxs-lookup"><span data-stu-id="c68f1-117">Using custom filter criteria, you can configure your own views and navigation options.</span></span>

<span data-ttu-id="c68f1-118">您可以從此清單頁面或詳細資料頁面建立或刪除報價。</span><span class="sxs-lookup"><span data-stu-id="c68f1-118">Quotes can be created or deleted from this list page or detail pages.</span></span>
