---
title: Project Operations 雙重寫入整合
description: 本主題提供 Project Operations 雙重寫入整合的概觀。
author: sigitac
ms.date: 04/28/2021
ms.topic: article
ms.prod: ''
ms.service: project-operations
ms.reviewer: kfend
ms.author: sigitac
ms.openlocfilehash: d9d6a7c367872219b4aca32aecb15d6837ebe296
ms.sourcegitcommit: 02f00960198cc78a5e96955a9e4390c2c6393bbf
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/28/2021
ms.locfileid: "5955648"
---
# <a name="project-operations-dual-write-integration-overview"></a><span data-ttu-id="ba013-103">Project Operations 雙重寫入整合概觀</span><span class="sxs-lookup"><span data-stu-id="ba013-103">Project Operations dual-write integration overview</span></span>

<span data-ttu-id="ba013-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations_</span><span class="sxs-lookup"><span data-stu-id="ba013-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios_</span></span>

<span data-ttu-id="ba013-105">Project Operations 使用[雙重寫入功能](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page)，在 Microsoft Dataverse 與 Dynamics 365 Finance 之間同步處理資料。</span><span class="sxs-lookup"><span data-stu-id="ba013-105">Project Operations uses [dual-write capabilities](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-home-page) to synchronize data across Microsoft Dataverse and Dynamics 365 Finance.</span></span>

<span data-ttu-id="ba013-106">下圖顯示資料如何在 Dataverse 與 Finance 之間整合的過程中進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ba013-106">The following illustration shows how data is synchronized as part of this integration between Dataverse and Finance.</span></span>

![Project Operations 資料流程概觀](./media/ProjectOperationsFlows.jpg)

<span data-ttu-id="ba013-108">Project Operations on Dataverse 使用 Power Platform 功能來提供新式使用者介面 (UI) 和簡易無程式碼/少量程式碼擴充性。</span><span class="sxs-lookup"><span data-stu-id="ba013-108">Project Operations on Dataverse provides a modern user interface (UI) and easy no-code/low-code extensibility using Power Platform capabilities.</span></span> <span data-ttu-id="ba013-109">專案經理、資源管理員、專案團隊成員及其他前台系統角色會在 Dataverse 上的 Project Operations 中執行他們的活動。</span><span class="sxs-lookup"><span data-stu-id="ba013-109">Project managers, Resource managers, Project team members, and other front-office personas, perform their activities in Project Operations on Dataverse.</span></span>

<span data-ttu-id="ba013-110">Finance 中的 Project Operations 提供專案會計及收入認列支援。</span><span class="sxs-lookup"><span data-stu-id="ba013-110">Project Operations in Finance provides project accounting and revenue recognition support.</span></span> <span data-ttu-id="ba013-111">Project Operations 會做為外掛程式插入 Finance 的銷售稅計算、貨幣匯率、財務維度報表等財務架構中。</span><span class="sxs-lookup"><span data-stu-id="ba013-111">Project Operations plugs in to the financial framework in Finance for sales tax calculation, currency exchange rates, financial dimension reporting, and more.</span></span> <span data-ttu-id="ba013-112">專案會計師體驗大多以 Finance 為基準。</span><span class="sxs-lookup"><span data-stu-id="ba013-112">The Project accountant experiences are mostly based in Finance.</span></span>

<span data-ttu-id="ba013-113">Project Operations 整合包含下列元件整合：</span><span class="sxs-lookup"><span data-stu-id="ba013-113">Project Operations integration consists of the following component integration:</span></span>


- [<span data-ttu-id="ba013-114">Project Operations 設定和設定資料整合</span><span class="sxs-lookup"><span data-stu-id="ba013-114">Project Operations setup and configuration data integration</span></span>](resource-dual-write-setup-integration.md) 
- [<span data-ttu-id="ba013-115">專案估計值和實際值</span><span class="sxs-lookup"><span data-stu-id="ba013-115">Project estimates and actuals</span></span>](resource-dual-write-estimates-actuals.md)
- [<span data-ttu-id="ba013-116">專案發票</span><span class="sxs-lookup"><span data-stu-id="ba013-116">Project invoices</span></span>](resource-dual-write-project-invoice.md)
- [<span data-ttu-id="ba013-117">費用管理</span><span class="sxs-lookup"><span data-stu-id="ba013-117">Expense management</span></span>](resource-dual-write-expense.md)
- [<span data-ttu-id="ba013-118">廠商發票</span><span class="sxs-lookup"><span data-stu-id="ba013-118">Vendor invoice</span></span>](resource-dual-write-vendor-invoice.md)
