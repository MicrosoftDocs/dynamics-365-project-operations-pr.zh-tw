---
title: 專案時間項目行動工作區
description: 本主題提供有關專案時間項目行動工作區的資訊。 此工作區可讓使用者使用行動裝置來輸入和儲存專案的時間。
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 8c786230ef2a497280885b827162561776e2eb00
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 03/24/2020
ms.locfileid: "3749927"
---
# <a name="project-time-entry-mobile-workspace"></a>專案時間項目行動工作區

[!include [banner](../includes/banner.md)]

本主題提供有關**專案時間項目**行動工作區的資訊。 此工作區可讓使用者使用行動裝置來輸入和儲存專案的時間。

此行動工作區旨在與 Dynamics 365 Unified Ops 行動應用程式搭配使用。 

## <a name="overview"></a>概觀
做為日常工作的一部分，專案資源經常是在現場或差旅途中。 **專案時間項目**行動工作區可讓使用者在他們選擇的行動裝置上，針對專案輸入其計費或非計費時間。 因此，專案資源可以隨時隨地記錄時間項目。 他們也可以檢視已記錄的時間項目。 

具體而言，在**專案時間項目**行動工作區中，使用者可以執行下列工作：

-   對任何選取的日期，輸入您花費在特定工作的小時數。
-   依專案名稱或客戶進行搜尋，尋找需要輸入時間的專案。
-   指定已花費時間的類別與活動。
-   針對專案記錄時間為計費或非計費。
-   選擇性輸入任何外部或內部意見。

## <a name="prerequisites"></a>先決條件
視組織已部署的 Microsoft Dynamics 365 版本而定，先決條件會有所不同。

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a>使用 Dynamics 365 Finance 時的先決條件
如果您的組織已部署 Finance，則系統系統管理員必須發佈 **專案時間項目**行動工作區。 如需指示，請參閱[發佈行動工作區](../../dev-itpro/mobile-apps/publish-mobile-workspace.md)。

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a>使用版本 1611 (含平台更新 3) 或更新版本時的先決條件
如果您的組織已部署版本 1611 (含平台更新 3) 或更新版本，則系統系統管理員必須完成下列先決條件。 

<table>
<thead>
<tr class="header">
<th>先決條件</th>
<th>角色</th>
<th>描述</th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td>實作 KB 4018050。</td>
<td>系統管理員</td>
<td>KB 4018050 是包含<strong>專案時間項目</strong>行動工作區的 X++ 更新或中繼資料 Hotfix。 若要實作 KB 4018050，您的系統系統管理員必須依照下列步驟進行。
<ol>
<li><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">從 Microsoft Dynamics Lifecycle Services (LCS) 下載中繼資料 Hotfix</a>。</li>
<li><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">安裝中繼資料 Hotfix</a>。</li>
<li><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">建立的可部署套件</a> (內含<strong>ApplicationSuite</strong> 和 <strong>ProjectMobile</strong> 模型)，然後將可部署套件上傳至 LCS。</li>
<li><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">套用可部署套件</a>。</li>

</ol></td>
</tr>
<tr class="even">
<td>發佈<strong>專案時間項目</strong>行動工作區。</td>
<td>系統管理員</td>
<td>請參閱<a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">發佈行動工作區</a>。</td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a>下載並安裝行動應用程式

下載並安裝 Finance and Operations 行動應用程式：

-   [適用於 Android 手機](https://go.microsoft.com/fwlink/?linkid=850662)
-   [適用於 iPhone](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a>登入行動應用程式
1.  在行動裝置上啟動應用程式。
2.  輸入您的 Dynamics 365 URL。
3.  第一次登入時，系統會提示您輸入您的使用者名稱和密碼。 輸入您的認證。
4.  登入後，會顯示您公司可用的工作區。 請注意，如果系統管理員稍後發佈了新的工作區，您就必須重新整理行動工作區的清單。

[![拖動以重新整理](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a>使用專案時間項目行動工作區來輸入時間
1.  在行動裝置上，選取**專案時間項目**工作區。
2.  選取**時間項目**。 隨即顯示本週的行事曆日期。
3.  針對所選取的日期，選取**動作** &gt; **新增輸入**。
4.  輸入要記錄的小時數。
5.  選取時間項目的專案。 清單會顯示已載入至您的應用程式中供離線使用的專案。 預設會載入 50 個項目，但是開發人員可以變更此數目。 如需詳細資訊，請參閱[平台行動](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。
6.  如果您的專案不在清單中，請選取**搜尋**。 依名稱搜尋，或切換為依專案名稱或客戶進行搜尋。
7.  選取類別。 清單會顯示已載入至您的應用程式中供離線使用的類別。 預設會載入 50 個項目，但是開發人員可以變更此數目。 如需詳細資訊，請參閱[平台行動](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。
8.  如果您的類別不在清單中，請選取**搜尋**。 依類別搜尋，或切換為依類別名稱進行搜尋。
9.  選取活動。 清單會顯示已載入至您的應用程式中供離線使用的活動。 預設會載入 50 個項目，但是開發人員可以變更此數目。 如需詳細資訊，請參閱[平台行動](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md)。
10. 如果您的活動不在清單中，請選取**搜尋**。 依活動編號搜尋，或切換為依目的進行搜尋。

11. 選取明細屬性。
12. 選用：輸入任何外部及內部意見。
13. 選取**完成**。
