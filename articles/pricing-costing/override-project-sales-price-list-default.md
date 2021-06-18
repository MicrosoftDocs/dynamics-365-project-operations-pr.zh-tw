---
title: 覆寫專案銷售價目表
description: 此主題提供建立自訂銷售價目表的相關資訊。
author: rumant
ms.date: 10/22/2020
ms.topic: article
ms.prod: ''
ms.reviewer: kfend
ms.author: rumant
ms.openlocfilehash: db2ff6acaad6ab4cbcc98d3d5b06b36ed23b758f
ms.sourcegitcommit: 40f68387f594180af64a5e5c748b6efa188bd300
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/10/2021
ms.locfileid: "5995071"
---
# <a name="override-project-sales-price-lists"></a><span data-ttu-id="d7c34-103">覆寫專案銷售價目表</span><span class="sxs-lookup"><span data-stu-id="d7c34-103">Override project sales price lists</span></span>

<span data-ttu-id="d7c34-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="d7c34-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

## <a name="customer-specific-project-price-lists"></a><span data-ttu-id="d7c34-105">客戶特定的專案價目表</span><span class="sxs-lookup"><span data-stu-id="d7c34-105">Customer-specific project price lists</span></span>

<span data-ttu-id="d7c34-106">客戶特定的價格合約可以設定為 Dynamics 365 Project Operations 中客戶記錄上的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="d7c34-106">Customer-specific price agreements can be set up as project price lists on an account record in Dynamics 365 Project Operations.</span></span>

<span data-ttu-id="d7c34-107">若要設定客戶特定的專案價目表，請在 **銷售** 區域中瀏覽至客戶記錄。</span><span class="sxs-lookup"><span data-stu-id="d7c34-107">To set up a customer-specific project price list, in the **Sales** area, navigate to the account record.</span></span>

1. <span data-ttu-id="d7c34-108">開啟 **帳戶** 清單頁面。</span><span class="sxs-lookup"><span data-stu-id="d7c34-108">Open the **Accounts** list page.</span></span>
2. <span data-ttu-id="d7c34-109">找到並按兩下客戶記錄以開啟 **帳戶** 詳細資料頁面。</span><span class="sxs-lookup"><span data-stu-id="d7c34-109">Locate and double-click a customer record to open the **Account** details page.</span></span>
3. <span data-ttu-id="d7c34-110">在 **專案價目表** 索引標籤上，選擇 **+ 新增專案價目表**。</span><span class="sxs-lookup"><span data-stu-id="d7c34-110">On the **Project Price lists** tab, select **+ New Project Price List**.</span></span>
4. <span data-ttu-id="d7c34-111">在 **新的專案價目表** 頁面上，從下拉清單中選擇價目表。</span><span class="sxs-lookup"><span data-stu-id="d7c34-111">On the **New Project Price List** page, select a price list from the drop-down.</span></span> <span data-ttu-id="d7c34-112">只會包含內容已設定為 **銷售** 且其貨幣符合帳戶貨幣的價目表。</span><span class="sxs-lookup"><span data-stu-id="d7c34-112">Only price lists that have the context set to **Sales** and whose currency matches the account currency are included.</span></span>
5. <span data-ttu-id="d7c34-113">命名關聯，然後選取 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="d7c34-113">Name the association, and then select **Save**.</span></span> <span data-ttu-id="d7c34-114">隨即建立客戶特定的專案價目表。</span><span class="sxs-lookup"><span data-stu-id="d7c34-114">A customer-specific project price list is created.</span></span> <span data-ttu-id="d7c34-115">如果報價或專案合同的建立日期落在價目表的有效期內，則此價目表將用於為此客戶建立的專案報價或合約的預設專案價格。</span><span class="sxs-lookup"><span data-stu-id="d7c34-115">This price list will be used to default project prices on project quotes or contracts created for this customer where the created date of the quote or project contract falls within the date effectivity of the price list.</span></span>

## <a name="custom-pricing-on-project-quotes"></a><span data-ttu-id="d7c34-116">專案報價的自訂定價</span><span class="sxs-lookup"><span data-stu-id="d7c34-116">Custom pricing on project quotes</span></span>

<span data-ttu-id="d7c34-117">在專案報價中，您可以有以預設標準價目表開頭的專案定價，該價目表預設為客戶或專案參數的預設值。</span><span class="sxs-lookup"><span data-stu-id="d7c34-117">On project quotes, you can have project pricing that starts with a default standard price list that defaults from the customer or from the project parameters.</span></span>

<span data-ttu-id="d7c34-118">當您需要針對特定報價進行與專案相關工作的自訂定價時，可以從專案價目表關聯實體獲取。</span><span class="sxs-lookup"><span data-stu-id="d7c34-118">When you need custom pricing for project-related work on a particular quote, you can get that from the project price lists associated entity.</span></span>

<span data-ttu-id="d7c34-119">完成以下步驟以設定報價特定的專案定價。</span><span class="sxs-lookup"><span data-stu-id="d7c34-119">Complete the following steps to set up quote-specific project pricing.</span></span>

1. <span data-ttu-id="d7c34-120">開啟專案報價並選擇 **專案價目表** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="d7c34-120">Open the project quote and select the **Project Price Lists** tab.</span></span>
2. <span data-ttu-id="d7c34-121">在子格中，選取 **建立自訂定價**。</span><span class="sxs-lookup"><span data-stu-id="d7c34-121">In the subgrid, select **Create custom pricing**.</span></span>

<span data-ttu-id="d7c34-122">附加到報價的所有專案價目表都會複製到新的價目表。</span><span class="sxs-lookup"><span data-stu-id="d7c34-122">All the project price lists that are attached to the quote are copied to new price lists.</span></span> <span data-ttu-id="d7c34-123">新價目表的名稱會反映報價的名稱，並具有建立這些價目表的日期時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d7c34-123">The names of the new price lists reflect the name of quote with a date-time stamp for when these price lists were created.</span></span>

<span data-ttu-id="d7c34-124">您可以使用每個價目表，並更新人力 (角色價格) 和費用 (類別價格) 價格。</span><span class="sxs-lookup"><span data-stu-id="d7c34-124">You can use each of those price lists and make updates to labor (role price) and expense (category price) prices.</span></span> <span data-ttu-id="d7c34-125">這些價格僅適用於此專案報價。</span><span class="sxs-lookup"><span data-stu-id="d7c34-125">These prices will only be applicable to this project quote.</span></span>

## <a name="price-lists-on-a-project-contract"></a><span data-ttu-id="d7c34-126">專案合約上的專案清單</span><span class="sxs-lookup"><span data-stu-id="d7c34-126">Price lists on a project contract</span></span>

<span data-ttu-id="d7c34-127">在專案合約中，專案定價始終預設為自訂價目表，其中附有合約名稱和附加到名稱的建立日期時間戳記。</span><span class="sxs-lookup"><span data-stu-id="d7c34-127">On a project contract, project pricing always defaults as a custom price list with the name of contract and the created date time stamp appended to the name.</span></span> <span data-ttu-id="d7c34-128">無論合約是在贏得報價時建立的，還是從零開始建立合約，都是如此。</span><span class="sxs-lookup"><span data-stu-id="d7c34-128">This is true whether the contract was created when the quote was won or if the contract was created from scratch.</span></span> <span data-ttu-id="d7c34-129">如果需要，您可以移除與自訂價目表的此關聯，並將標準價目表關聯至專案合約。</span><span class="sxs-lookup"><span data-stu-id="d7c34-129">If needed, you can remove this association to the custom price list and associate a standard price list to the project contract instead.</span></span>

<span data-ttu-id="d7c34-130">當您將標準價目表與報價或合約上的專案價目表關聯時，對價目表中的價格所做的任何變更都將影響使用價目表的所有報價和合約。</span><span class="sxs-lookup"><span data-stu-id="d7c34-130">When you associate a standard price list to the project price lists on quote or contract, any changes made to the prices in the price list will impact all quotes and contracts that use the price list.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]