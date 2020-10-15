---
title: 費用項目 (精簡)
description: 本主題提供有關如何在精簡部署中處理費用項目的資訊。
author: stsporen
manager: AnnBe
ms.date: 10/06/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 746d5d9ff56222e7d6b9b6e264db75d5814365c7
ms.sourcegitcommit: fd8ea1779db2bb39a428f459ae3293c4fd785572
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/06/2020
ms.locfileid: "3965743"
---
# <a name="expense-entry-lite"></a>費用項目 (精簡)

_**適用於：** 精簡部署 - 交易至開立預估發票_

基本 (或精簡) 費用管理是用於記錄簡單費用的功能。 您可以針對專案來記錄費用，然後專案核准者會審查並核准這些費用。

如需 Dynamics 365 Project Operations 中費用功能的詳細資訊，請參閱[費用概觀](expense-overview.md)。

## <a name="capture-a-basic-expense"></a>擷取基本費用

您可以擷取您的費用，以便將其提交給核准者。

1. 移至**費用**，然後選取**新增**。
2. 在**新增費用**頁面上，輸入必要的費用資訊，然後選取**儲存**。

## <a name="submit-a-basic-expense"></a>提交基本費用

完成擷取所有的費用，且已準備好進行核准之後，您必須提交這些費用。

1. 移至**費用**，然後選取費用。 或者，使用標題上的核取方塊來選取所有的費用。
2. 選取**送出**。 系統會處理選取的項目，然後建立費用核准要求。

## <a name="recall-a-basic-expense"></a>回收基本費用

錯誤提交費用時，您可以將其回收。 回收費用項目所需的時間取決於其核准階段。  如果核准者尚未核准該項目，回收就會立即進行。 不過，如果項目已獲核准，則會要求核准者核准回收並沖銷交易。

1. 移至**費用**，然後在費用清單中，選取要回收的費用。
2. 選取**回收**。 如果費用項目尚未獲核准，系統會立即將其回收。 如果費用項目已核准，則會建立回收要求以通知核准者您要沖銷費用。 核准者會接著確認他可以完成沖銷，並將該項目退回。

## <a name="delete-a-basic-expense"></a>刪除基本費用

您可以刪除尚未提交的費用。 若要刪除已提交的費用，您必須先將其回收。

## <a name="see-also"></a>請參閱

- [核准概觀](../approvals/approvals-overview.md)
