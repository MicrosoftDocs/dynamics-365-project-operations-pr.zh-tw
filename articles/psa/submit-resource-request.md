---
title: 送出資源要求
description: 本主題提供有關送出專案資源要求的資訊。
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 12/1/2018
ms.topic: article
author: JohnPBurrows
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 8976ca2360be8676350178059615c59995544a71
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5282233"
---
# <a name="submitting-a-resource-request"></a><span data-ttu-id="be4ac-103">送出資源要求</span><span class="sxs-lookup"><span data-stu-id="be4ac-103">Submitting a resource request</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="be4ac-104">您可以將產生的資源需求當做資源要求送出。</span><span class="sxs-lookup"><span data-stu-id="be4ac-104">You can submit a generated resource requirement as a resource request.</span></span> <span data-ttu-id="be4ac-105">隨後會將要求傳送給資源管理員來履行。</span><span class="sxs-lookup"><span data-stu-id="be4ac-105">The request is then sent to a resource manager for fulfillment.</span></span>

1. <span data-ttu-id="be4ac-106">在 Project Service Automation (PSA) 的 **專案** 頁面上，按一下 **團隊** 索引標籤以檢視可預約資源清單。</span><span class="sxs-lookup"><span data-stu-id="be4ac-106">In Project Service Automation (PSA), on the **Projects** page, click the **Team** tab to view a list bookable resources.</span></span> 
2. <span data-ttu-id="be4ac-107">從清單中選取具有資源需求的一般資源，然後按一下 **送出要求**。</span><span class="sxs-lookup"><span data-stu-id="be4ac-107">Select the generic resource that has a resource requirement from the list and then click **Submit Request**.</span></span>

![送出資源要求](media/RM-how-to-18.png)

<span data-ttu-id="be4ac-109">一般團隊成員的要求狀態會變更為 **已送出**。</span><span class="sxs-lookup"><span data-stu-id="be4ac-109">The request status of the generic team member will change to **Submitted**.</span></span>

<span data-ttu-id="be4ac-110">資源管理員履行要求之後，如果資源管理員是使用具名資源的預約來履行要求，則會以具名資源取代一般資源。</span><span class="sxs-lookup"><span data-stu-id="be4ac-110">After the request is fulfilled by the resource manager, the generic resource will be replaced by a named resource if the resource manager fulfills the request with the booking of a named resource.</span></span> <span data-ttu-id="be4ac-111">否則，一般資源仍保留在團隊中，如果資源管理員已提案建議具名資源，則要求狀態將會變更為 **需要檢閱**。</span><span class="sxs-lookup"><span data-stu-id="be4ac-111">Otherwise, the generic resource will remain on the team and the request status will change to **Needs Review**, if the resource manager has proposed a named resource.</span></span>


[!INCLUDE[footer-include](../includes/footer-banner.md)]