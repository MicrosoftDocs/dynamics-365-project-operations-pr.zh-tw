---
title: 有關核准的開發人員注意事項
description: 本主題提供另外有關使用核准的開發人員資訊。
author: stsporen
manager: Annbe
ms.date: 11/09/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: d58c776b0341c08b0292e1b459a7d7ebac550bcc
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5290259"
---
# <a name="developer-notes-for-approvals"></a><span data-ttu-id="d0749-103">有關核准的開發人員注意事項</span><span class="sxs-lookup"><span data-stu-id="d0749-103">Developer notes for Approvals</span></span>

<span data-ttu-id="d0749-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="d0749-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d0749-105">Dynamics 365 Project Operations 包含可確保經歷各個核准階段正確進行記錄轉換的驗證邏輯。</span><span class="sxs-lookup"><span data-stu-id="d0749-105">Dynamics 365 Project Operations includes validation logic that ensures correct record transition through the approval stages.</span></span> <span data-ttu-id="d0749-106">正確的記錄轉換可確保：</span><span class="sxs-lookup"><span data-stu-id="d0749-106">Correct record transitions ensure:</span></span> 

  - <span data-ttu-id="d0749-107">所有的支援列都是在相關的資料表 (例如帳目和實際值) 中建立。</span><span class="sxs-lookup"><span data-stu-id="d0749-107">All supporting rows are created in related tables, such as journals and actuals.</span></span>
  - <span data-ttu-id="d0749-108">繼續進行之前，核准者會先標示為專案中的 **專案核准者**。</span><span class="sxs-lookup"><span data-stu-id="d0749-108">The approver is marked as a **Project Approver** in the project before proceeding.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]