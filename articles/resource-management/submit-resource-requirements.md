---
title: 送出資源要求
description: 您可以將產生的資源需求當做資源要求送出。 隨後會將要求傳送給資源管理員來履行。
author: ruhercul
manager: Annbe
ms.date: 10/04/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 94cf0f0d88e9be2522936b45122ed0037434d4f3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072890"
---
# <a name="submit-a-resource-request"></a><span data-ttu-id="d5419-104">送出資源要求</span><span class="sxs-lookup"><span data-stu-id="d5419-104">Submit a resource request</span></span>

<span data-ttu-id="d5419-105">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="d5419-105">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="d5419-106">您可以將產生的資源需求當做資源要求送出。</span><span class="sxs-lookup"><span data-stu-id="d5419-106">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="d5419-107">隨後會將要求傳送給資源管理員來履行。</span><span class="sxs-lookup"><span data-stu-id="d5419-107">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="d5419-108">在 Dynamics 365 Project Operations 的 **專案** 頁面上，選取 **團隊** 索引標籤以檢視可預約資源清單。</span><span class="sxs-lookup"><span data-stu-id="d5419-108">In Dynamics 365 Project Operations, on the **Projects** page, select the **Team** tab to view a list of bookable resources.</span></span> 
2. <span data-ttu-id="d5419-109">從清單中選取具有資源需求的一般資源，然後按一下 **送出要求** 。</span><span class="sxs-lookup"><span data-stu-id="d5419-109">Select the generic resource that has a resource requirement from the list, and then click **Submit Request**.</span></span>

<span data-ttu-id="d5419-110">一般團隊成員的要求狀態會變更為 **已送出** 。</span><span class="sxs-lookup"><span data-stu-id="d5419-110">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="d5419-111">履行要求之後，如果資源管理員透過預約具名資源來履行要求，則會以具名資源取代一般資源。</span><span class="sxs-lookup"><span data-stu-id="d5419-111">After the request is fulfilled, the generic resource is replaced by a named resource if the resource manager fulfills the request by booking a named resource.</span></span> <span data-ttu-id="d5419-112">否則，如果資源管理員提案建議具名資源，則一般資源仍保留在團隊中，而且要求狀態會變更為 **需要檢閱** 。</span><span class="sxs-lookup"><span data-stu-id="d5419-112">Otherwise, if the resource manager proposes a named resource, the generic resource remains on the team and the request status will change to **Needs Review**.</span></span>
