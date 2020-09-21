---
title: 專案採購單
description: 本文說明各種可用來建立專案採購單的方法。 您使用的方法取決於採購單的用途，以及專案的採購項目何時取用和收費。
author: KimANelson
manager: AnnBe
ms.date: 09/14/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjTable
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 83972
ms.assetid: 247e4d72-610b-4fa5-9873-601ed0f4b2d6
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a4975b9f9e20906fb1259e36a07d8ef3db4f4fee
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749902"
---
# <a name="purchase-orders-for-a-project"></a>專案採購單

[!include [banner](../includes/banner.md)]

本文說明各種可用來建立專案採購單的方法。 您使用的方法取決於採購單的用途，以及專案的採購項目何時取用和收費。

### <a name="methods-for-creating-a-purchase-order"></a>建立採購單的方法

您可以使用下列其中一個方法，在 [專案管理與會計] 中建立採購單。 採購單的用途決定採購單何時使用，以及因此在何時向專案收取項目的費用。

<table>
<colgroup>
<col width="33%" />
<col width="33%" />
<col width="33%" />
</colgroup>
<thead>
<tr class="header">
<th>方法</th>
<th>用途</th>
<th>取用項目</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>直接從專案建立採購單。</td>
<td>使用此方法，向外部供應商購買要在專案上取用的項目。 您可以用兩種方式建立採購單：
<ul>
<li>從專案本身。 在此情況下，已經為採購單定義專案。</li>
<li>瀏覽至專案採購單。 您必須供應商和專案都選取，才能建立其採購單。</li>
</ul></td>
<td>更新供應商發票時，會取用項目。</td>
</tr>
<tr class="even">
<td>從銷售訂單建立採購單。</td>
<td>從專案建立銷售訂單時，使用此方法來購買項目。</td>
<td>開立銷售訂單的發票給客戶時，會取用項目。</td>
</tr>
<tr class="odd">
<td>從項目需求建立採購單。</td>
<td>從專案建立項目需求時，使用此方法來購買項目。</td>
<td>更新項目需求裝箱單時，會取用項目。</td>
</tr>
</tbody>
</table>

> [!NOTE] 
> 更新供應商發票或裝箱單時，系統會提示更新項目需求上的裝箱單。

如需詳細資訊，請參閱[從項目需求擷取採購單上的項目](tasks/receive-items-purchase-order-item-requirement.md)。

