---
title: 費用項目 (精簡)
description: 本主題提供有關如何在精簡部署中處理費用項目的資訊。
author: stsporen
ms.date: 11/19/2020
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: 774bf2f8f54d2e314740fbad40ea15ce83d38297
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578330"
---
# <a name="expense-entry-lite"></a>費用項目 (精簡)

_**適用於：** 精簡部署 - 交易至開立預估發票_

基本 (或精簡) 費用管理是用於記錄簡單費用的功能。 您可以針對專案來記錄費用，然後專案核准者會審查並核准這些費用。

如需有關 Dynamics 365 Project Operations 中費用功能的詳細資訊，請參閱[費用概觀](expense-overview.md)。

## <a name="capture-a-basic-expense"></a>擷取基本費用

您可以擷取您的費用，以便將其提交給核准者。

1. 移至 **費用**，然後選取 **新增**。
2. 在 **新增費用** 頁面上，輸入必要的費用資訊，然後選取 **儲存**。

## <a name="submit-a-basic-expense"></a>提交基本費用

完成擷取所有的費用，且已準備好進行核准之後，您必須提交這些費用。

1. 移至 **費用**，然後選取費用。 或者，使用標題上的核取方塊來選取所有的費用。
2. 選取 **送出**。 系統會處理選取的項目，然後建立費用核准要求。

## <a name="add-an-attachment"></a>新增附件

您可能必須為核准者提供費用的額外文件。 您可以在費用項目的時間表中附加收據。 選取 **編輯** 並在 **時間表** 區段中選取迴紋針圖示以附加收據。

## <a name="recall-a-basic-expense"></a>回收基本費用

錯誤提交費用時，您可以將其回收。 回收費用項目所需的時間取決於其核准階段。  如果核准者尚未核准該項目，回收就會立即進行。 不過，如果項目已獲核准，則會要求核准者核准回收並沖銷交易。

1. 移至 **費用**，然後在費用清單中，選取要回收的費用。
2. 選取 **回收**。 如果費用項目尚未獲核准，系統會立即將其回收。 如果費用項目已核准，則會建立回收要求以通知核准者您要沖銷費用。 核准者會接著確認他可以完成沖銷，並將該項目退回。

## <a name="delete-a-basic-expense"></a>刪除基本費用

您可以刪除尚未提交的費用。 若要刪除已提交的費用，您必須先將其回收。

## <a name="see-also"></a>請參閱

- [核准概觀](../approvals/approvals-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]