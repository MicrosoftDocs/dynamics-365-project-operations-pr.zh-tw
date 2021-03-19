---
title: 固定價格營收估計值專案
description: 此主題提供有關專案中固定價格營收的資訊。
author: sigitac
manager: Annbe
ms.date: 11/16/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: 7cf4d7853f7fedaeeeba99bc589f39989b924423
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5278903"
---
# <a name="fixed-price-revenue-estimate-projects"></a><span data-ttu-id="de177-103">固定價格營收估計值專案</span><span class="sxs-lookup"><span data-stu-id="de177-103">Fixed price revenue estimate projects</span></span> 

<span data-ttu-id="de177-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="de177-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="de177-105">當您使用 Dynamics 365 Project Operations 中的下列屬性在 Microsoft Dataverse 上建立專案合約服務內容時，系統會自動建立固定價格營收估計值專案。</span><span class="sxs-lookup"><span data-stu-id="de177-105">When you create a project contract line with the following attributes in Dynamics 365 Project Operations on Microsoft Dataverse, the system automatically creates a fixed price revenue estimate project.</span></span> <span data-ttu-id="de177-106">此專案中的資訊會根據下列項目而定：</span><span class="sxs-lookup"><span data-stu-id="de177-106">The information in this project is based on the following:</span></span>

  - <span data-ttu-id="de177-107">固定價格帳務方式。</span><span class="sxs-lookup"><span data-stu-id="de177-107">A fixed price billing method.</span></span>
  - <span data-ttu-id="de177-108">相關專案。</span><span class="sxs-lookup"><span data-stu-id="de177-108">An associated project.</span></span>
  - <span data-ttu-id="de177-109">在 **專案合約服務內容** 索引標籤上的 **發票清單** 索引標籤中，至少定義了一個里程碑。</span><span class="sxs-lookup"><span data-stu-id="de177-109">At least one milestone defined on the **Invoice schedule** tab on the **Project contract line** page.</span></span>

## <a name="review-fixed-price-revenue-estimates-projects"></a><span data-ttu-id="de177-110">檢閱固定價格營收估計值專案</span><span class="sxs-lookup"><span data-stu-id="de177-110">Review fixed price revenue estimates projects</span></span>
<span data-ttu-id="de177-111">若要檢閱固定價格營收估計值專案，請完成下列步驟：</span><span class="sxs-lookup"><span data-stu-id="de177-111">To review fixed price revenue estimates projects, complete the following steps:</span></span>

1. <span data-ttu-id="de177-112">在 Dynamics 365 Finance 環境中，移至 **專案管理與會計** > **專案** > **固定價格營收估計值專案**。</span><span class="sxs-lookup"><span data-stu-id="de177-112">In the Dynamics 365 Finance environment, go to **Projects management and accounting** > **Projects** > **Fixed price revenue estimate projects**.</span></span>
2. <span data-ttu-id="de177-113">選取您要查看的專案，並按兩下 **估計專案識別碼** 以開啟該記錄，並審查專案的詳細資料。</span><span class="sxs-lookup"><span data-stu-id="de177-113">Select the project that you want to view and double-click the **Estimate project ID** to open the record and review the details of the project.</span></span>
3. <span data-ttu-id="de177-114">展開 **專案** 索引標籤。您會在 **選取的專案** 網格中看到一個專案。</span><span class="sxs-lookup"><span data-stu-id="de177-114">Expand the **Project** tab. You will see one project in the **Selected projects** grid.</span></span> <span data-ttu-id="de177-115">系統會將此專案用做為預設專案，因為它是與專案合約服務內容相關聯的專案。</span><span class="sxs-lookup"><span data-stu-id="de177-115">The system uses this as default project because it is the project associated to the project contract line.</span></span> 
4. <span data-ttu-id="de177-116">若要變更關聯，請選取其他專案，並將它們新增至 **選取的專案** 網格。</span><span class="sxs-lookup"><span data-stu-id="de177-116">To change the association, select additional projects and add them to the **Selected projects** grid.</span></span> <span data-ttu-id="de177-117">如果在此網格中選取多個專案，則會為所有選取的專案計算專案完成百分比和營收估計值。</span><span class="sxs-lookup"><span data-stu-id="de177-117">If multiple projects are selected in this grid, the project percentage completion and revenue estimates are calculated together for of the all selected projects.</span></span>

  <span data-ttu-id="de177-118">專案成本、營收設定檔、成本範本以及期間代碼可以手動設定。</span><span class="sxs-lookup"><span data-stu-id="de177-118">Project cost, revenue profile, cost template, and the period code can be set manually.</span></span> <span data-ttu-id="de177-119">如果不是手動設定，則這些值將預設為使用為專案成本和營收設定檔所設定規則在專案的第一次估計值計算。</span><span class="sxs-lookup"><span data-stu-id="de177-119">If they aren't set manually, the values default during the first estimate calculation for the project using the rules configured for project cost and revenue profiles.</span></span>



[!INCLUDE[footer-include](../includes/footer-banner.md)]