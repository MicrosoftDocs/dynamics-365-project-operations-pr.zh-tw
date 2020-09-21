---
title: 時間與材料專案的專案銷售訂單
description: 本主題說明如何為時間與材料專案建立專案型銷售訂單。
author: KimANelson
manager: AnnBe
ms.date: 04/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: 05ab0cf6-318c-42de-ba56-3e662283497e
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2019-04-05
ms.dyn365.ops.version: AX 10.0.2
ms.openlocfilehash: 446c73e9491b1892847caf7e843c802292107ef9
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749869"
---
# <a name="project-sales-orders-for-time-and-material-projects"></a><span data-ttu-id="82baa-103">時間與材料專案的專案銷售訂單</span><span class="sxs-lookup"><span data-stu-id="82baa-103">Project sales orders for time and material projects</span></span>

[!include[banner](../includes/banner.md)]
[!include[banner](../includes/preview-banner.md)]

<span data-ttu-id="82baa-104">本主題說明如何建立專案的銷售訂單。</span><span class="sxs-lookup"><span data-stu-id="82baa-104">This topic describes how to create a sales order for a project.</span></span> <span data-ttu-id="82baa-105">您只能為**時間與材料**類型的專案建立銷售訂單。</span><span class="sxs-lookup"><span data-stu-id="82baa-105">Sales orders can only be created for projects of type **time and material**.</span></span>

<span data-ttu-id="82baa-106">如果時間與材料專案在專案合約上有多個資金來源，您必須在**專案管理與會計參數**頁面上啟用**允許具有多個資金來源的專案銷售訂單**。</span><span class="sxs-lookup"><span data-stu-id="82baa-106">If a time and material project has multiple funding sources on the project contract, you must enable the **Allow sales orders for projects with multiple funding sources** parameter on the **Project management and accounting parameters** page.</span></span> 

> [!NOTE]
> - <span data-ttu-id="82baa-107">對具有多個資金來源的專案銷售訂單的支援，是從應用程式版本 10.0.2 和更新版本開始提供。</span><span class="sxs-lookup"><span data-stu-id="82baa-107">Support for project sales orders with multiple funding sources is available starting with application release 10.0.2 and higher.</span></span>
> - <span data-ttu-id="82baa-108">用來啟用支援具有多個資金來源的專案銷售訂單的參數會在 2020 年 4 月發行浪潮中移除，此後一律啟用這項功能。</span><span class="sxs-lookup"><span data-stu-id="82baa-108">The parameter to enable the support for project sales orders with multiple funding sources will be removed in the April 2020 release wave, after which the functionality will always be enabled.</span></span>

<span data-ttu-id="82baa-109">您可以用兩種方式建立專案型銷售訂單：</span><span class="sxs-lookup"><span data-stu-id="82baa-109">You can create project-based sales orders in two ways:</span></span>

- <span data-ttu-id="82baa-110">移至專案本身。</span><span class="sxs-lookup"><span data-stu-id="82baa-110">Go to the project itself.</span></span> <span data-ttu-id="82baa-111">在動作窗格中，選取**管理 > 專案工作 > 銷售訂單**。</span><span class="sxs-lookup"><span data-stu-id="82baa-111">On the Action Pane, select **Manage > Item tasks > Sales order**.</span></span> <span data-ttu-id="82baa-112">專案資訊會預設為專案中的銷售訂單。</span><span class="sxs-lookup"><span data-stu-id="82baa-112">The project information will default to the sales order from the project.</span></span> <span data-ttu-id="82baa-113">如果專案合約有多個資金來源，您必須選取資金來源，才能設定銷售訂單的客戶。</span><span class="sxs-lookup"><span data-stu-id="82baa-113">If the project contract has more than one funding source, you will need to select the funding source to set the customer for the sales order.</span></span> <span data-ttu-id="82baa-114">如果專案只有一個資金來源，就會自動設定客戶。</span><span class="sxs-lookup"><span data-stu-id="82baa-114">If there is only one funding source for the project, the customer will be automatically set.</span></span>
- <span data-ttu-id="82baa-115">移至**所有銷售訂單**清單頁面，並建立新的銷售訂單。</span><span class="sxs-lookup"><span data-stu-id="82baa-115">Go to the **All sales order** list page and create a new sales order.</span></span> <span data-ttu-id="82baa-116">您需要選取銷售訂單的專案。</span><span class="sxs-lookup"><span data-stu-id="82baa-116">You will need to select the project for the sales order.</span></span> <span data-ttu-id="82baa-117">選取專案之後，將會從資金來源設定客戶，如果專案合約有多個資金來源，則需要選取資金來源。</span><span class="sxs-lookup"><span data-stu-id="82baa-117">After the project is selected, the customer will be set from the funding source or you will need to select the funding source if the project contract has multiple funding sources.</span></span>

