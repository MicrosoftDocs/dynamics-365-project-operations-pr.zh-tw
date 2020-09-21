---
title: 專案時程表行動應用程式
description: 本主題提供有關 Microsoft Dynamics 365 Project Timesheet 行動應用程式的資訊。 專案時程表行動應用程式可讓使用者在其行動裝置上提交和核准專案的時程表。
author: abruer
manager: AnnBe
ms.date: 04/08/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: e2eb387f-5bb3-419c-953b-3bbc2f050059
ms.search.region: Global
ms.search.industry: Service industries
ms.author: josaw1
ms.dyn365.ops.version: 10
ms.search.validFrom: 2019-01-15
ms.openlocfilehash: 6cd4629e9380fbe3d1839ba31a819c9057d1258c
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749939"
---
# <a name="project-timesheet-mobile-application"></a>專案時程表行動應用程式

[!include [banner](../includes/banner.md)]

## <a name="overview"></a>概觀

Microsoft Dynamics 365 Project Timesheet 行動應用程式 (iPhone 或 Android) 可讓使用者在其行動裝置上提交和核准專案的時程表。 此行動應用程式會顯露位於 Dynamics 365 Finance [專案管理與會計] 區域中的程表功能，並提高使用者生產力與效率，以及適時啟用專案時程表的輸入與核准。

## <a name="download-and-install-the-mobile-app"></a>下載並安裝行動應用程式

從您裝置的行動市集下載並安裝適用於 Android 或 iPhone 的 Microsoft Dynamics 365 Project Timesheet 行動應用程式。

## <a name="enable-the-app"></a>啟用應用程式 

在 Finance 中，必須啟用專案時程表行動應用程式。 若要啟用此功能，請移至**專案管理與會計參數 \> 時程表**，然後選取**啟用 Microsoft Dynamics 365 Project Timesheet** 參數。

## <a name="sign-in-to-the-app"></a>登入應用程式

1.  在行動裝置上啟動應用程式。

2.  輸入您的 Finance URL。

3.  第一次登入時，系統會提示您輸入您的使用者名稱和密碼。 輸入您的認證。

4.  您會登入您的預設公司。

## <a name="submit-a-project-timesheet"></a>提交專案時程表

您可以在應用程式中建立並提交專案時程表。 您可以根據先前的時程表、已儲存的明細或專案指派的資訊建立新的時程表。 如果已指定您做為代理人，輸入您也可以為其他工作者輸入時程表。 若要將時程表建立為代理人，請選取**功能表**按鈕，然後選取資源名稱。

時程表頁面會根據目前日期，為時程表期間建立新的時程表。 將會顯示工作週。 如果時程表期間涵蓋多週，您可以從 [工作週] 索引標籤選取另一個工作週。
如果目前日期有時程表，就會顯示該時程表。 如果您需要在不同的時程表期間建立新的時程表，請選取**功能表**按鈕，然後選取**新增時程表**。

您可以按一下**新增時間**動作或**複製時間來源**動作來輸入專案資訊。 **複製時間來源**動作會複製專案明細資訊，但不會複製時數。 **複製時間來源**功能表包含下列選項：

- **從現有時程表複製** - 從現有的時程表複製時程表列。

- **從我的最愛複製** - 使用您選擇做為 [我的最愛] 的時程表設定，建立新的時程表行。

- **從指派複製** - 從指派的專案建立新的時程表列。

顯示的專案資訊取決於您在**專案管理與會計參數**頁面所定義的行動參數。

在**法律實體**欄位中，選取您為其執行專案工作的法律實體。 **法律實體**欄位只有在您的法律實體已啟用公司間的時程表支援時，才會提供。

選取與時程表專案相關聯的客戶。 在 Android 上的初始發行版本，不支援根據客戶輸入資料，因為您必須先選取專案。 如果您先選取專案，就會自動填入**客戶**欄位。

在**專案**欄位中，選取您要輸入時間的專案。 **客戶**欄位會自動填入。

客戶和專案查詢可讓您同時跨客戶與專案進行搜尋。

視需要選取**類別**、**活動**、**明細屬性**、**銷售課稅群組**和**項目銷售課稅群組**欄位中的資訊。 可以覆寫這些欄位。

**明細屬性**欄位應根據 [專案管理與會計參數] 設定為預設值。 啟用專案/類別和類別/資源參數時，**明細屬性**值會設定為您已為此驗證定義的預設值。 專案/類別和類別/資源參數未啟用時，**明細屬性**值會根據**專案管理與會計參數**頁面上的**啟用預設明細屬性**欄位設定預設值。 可以覆寫**明細屬性**值。

選取要新增時間的日期。 輸入您每天工作的小時數。

若要新增對於您輸入時數的註解，請按一下**新增註解**，然後輸入給內部對象、客戶對象或兩者的註解。
專案經理可以檢視內部註解。 客戶註解會包含在發票中。

若要將該明細儲存為 [我的最愛]，請選取核取方塊，然後按一下**儲存為我的最愛**。

行動應用程式不提供財務維度及附件支援。

視需要繼續新增專案明細，以完成您的時程表。

按一下**提交**，將時程表傳送至核准工作流程。

## <a name="review-timesheets"></a>審查時程表

您可以在功能表中找到需要審查的時程表清單。 此選項只有在將您指定為工作流程核准者時，才會提供。 支援標題和明細核准。 明細等級核准提供標示一行或多行明細以供核准的功能。 審查時程表資訊之後，按一下**核准**、**委派**或**退回**以繼續工作流程。
