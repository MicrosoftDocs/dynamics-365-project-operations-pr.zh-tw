---
title: 資源管理模式概觀
description: 本主題提供有關 Dynamics 365 Project Operations 中資源管理功能的資訊。
author: ruhercul
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: 872f4f2878f474e16674932f23fe192c6a8de6eb
ms.sourcegitcommit: fa32b1893286f20271fa4ec4be8fc68bd135f53c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 02/15/2021
ms.locfileid: "5279443"
---
# <a name="resource-management-modes-overview"></a>資源管理模式概觀

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_


Dynamics 365 Project Operations 支援兩種模式，讓您執行整體預約流程。 管理模式是以專案參數來定義，如果您的業務需求變更，則可加以修改。    

## <a name="central-mode"></a>集中模式
對於將資源集中配置給專案的組織，集中模式提供的方式確保專案經理可以在專案層級定義資源需求。 履行資源需求的職責已委派給資源經理。 專案經理可以接受或拒絕資源管理員提議的資源。

![集中模式](./media/resource-management-central.png)

若要使用集中模式管理資源，請參閱：

- [指派一般可預約資源至工作，並產生資源需求](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [透過資源需求預約具名資源](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)
- [送出資源要求](https://docs.microsoft.com/dynamics365/project-service/submit-resource-request)
- [履行資源要求](https://docs.microsoft.com/dynamics365/project-service/resource-management-fulfill-requests)
- [接受或拒絕資源要求提案的專案資源](https://docs.microsoft.com/dynamics365/project-service/accept-reject-proposed-resource)

## <a name="hybrid-mode"></a>混合模式
對於需要彈性配置資源的組織，混合模式使專案經理和資源管理員能夠預約資源。

![混合模式](./media/resource-management-hybrid.png)

除了支援的集中模式程序之外，也請參閱下列主題，以便在混合模式下管理所有其他支援的預約流程：

將資源直接預約給專案：
- [將具名可預約資源預約給專案團隊並指派工作](https://docs.microsoft.com/dynamics365/project-service/assign-named-bookable-resource)

透過資源需求預約資源：
- [指派一般可預約資源至工作，並產生資源需求](https://docs.microsoft.com/dynamics365/project-service/assign-generic-bookable-resource)
- [透過資源需求預約具名資源](https://docs.microsoft.com/dynamics365/project-service/book-named-resource)


[!INCLUDE[footer-include](../includes/footer-banner.md)]