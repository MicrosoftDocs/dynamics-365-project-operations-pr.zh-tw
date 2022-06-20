---
title: 2021 年 12 月 - 資源/非庫存型案例適用的 Project Operations 新增功能
description: 本文提供有關資源/非庫存型案例適用 Project Operations 2021 年 12 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 12/09/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: 79ae9f49a4291d162a8a9bb6eb9a22d615773f6e
ms.sourcegitcommit: 6cfc50d89528df977a8f6a55c1ad39d99800d9b4
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 06/03/2022
ms.locfileid: "8910850"
---
# <a name="whats-new-december-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 12 月 - 資源/非庫存型案例適用的 Project Operations 新增功能

*適用於：資源/非庫存型案例適用的 Project Operations*

本文適用於 Microsoft Dynamics 365 Project Operations 的下列元件和版本：

- Dataverse 環境 4.27.0.195、4.27.0.242、4.27.0.244 版中的 Project Operations
- Dynamics 365 Finance 環境 10.0.23 版中的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能

- 改善系統管理員的疑難排解功能。 當使用者無法開啟專案時，系統管理員可以檢閱[專案排程記錄](../project-management/schedule-api-logs.md)中由 Project for the Web 所產生的非授權相關錯誤。
- [使用 Project for the Web 中的工作檢查清單](https://support.microsoft.com/office/use-task-checklists-in-microsoft-project-for-the-web-c69bcf73-5c75-4ad3-9893-6d6f92360e9c)。 在 Project for the Web 中，您可以將檢查清單新增至工作來追蹤特定項目。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。 如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果沒有啟用最新版本的對應，則部分功能可能會無法正確運作。 您可以在 **雙重寫入** 頁面的 **版本** 欄中檢視對應的使用中版本。 若要啟用新的對應版本，請選取 **資料表對應版本**、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的表格對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 規劃和追蹤 | 2392596 | 排程 API 現在允許更新 **剩餘未完成投入**、**已完成的投入** 和 **完成百分比** 欄位。 |
| 規劃和追蹤 | 2478497 | 排程 API 的 **活動編號** 和 **工作識別碼** 欄位在輸入時可以是空白，因為系統會使用自動編號來填入這些值。|
| 時間和費用 | 2468135 | 核准重試次數從五次減少為三次。 |
| 時間和費用 | 2468188 | 修正記錄文字超過 **註釋** 實體之 **notetext** 屬性中長度上限的問題。 |
| 帳單和定價 | 2488698 | 更新環境設定遺失從 Finance 填入之總帳實體記錄時出現的錯誤訊息。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 專案管理與會計 | [587187](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D587187&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225501421%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=qpKECMgKZe9sHGVZUhBxs%2F4ou3fXIiFFg2amMTJ6t9U%3D&amp;reserved=0) | 公司間收入科目只考慮未包含銷售稅群組的 **全部 - 所有明細**。 |
| 專案管理與會計 | [599568](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D599568&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225600986%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=IudfEjWmkNeiTsWmR%2Fu2oR0CnnCkffAshvqZJuF76q8%3D&amp;reserved=0) | 直線估計值計算不正確。 |
| 專案管理與會計 | [602728](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D602728&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227094434%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=Q2%2BveFHlGrzg4QHtqcgeqjyZSQkmpr%2Fku7oObKHMB9g%3D&amp;reserved=0) | 套用保留款之案例中的專案已開發票收入的過帳問題會導致憑單中的交易未達借貸平衡。 |
| 專案管理與會計 | [610906](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D610906&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227134259%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=xDBnz10T71GmOZt78ooFK3SYvmTLoC5fj1OftYNYDpY%3D&amp;reserved=0) | 改善與 Project Operations 實際值整合的效能。 |
| 專案管理與會計 | [618670](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D618670&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227203949%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=PqvHsTGLcQ3bYbUlzYABYhl7J9v2zbnjcOgm%2FTvXB20%3D&amp;reserved=0) | 如果時數成本交易使用 **永不使用總帳** 或 **無需總帳** 進行過帳，則使用者無法開立發票。 |
| 專案管理與會計 | [623818](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D623818&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227303517%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=LAfdEiuKG8DoGk8O48MRLuaKYDINhCyMAtrlpGvVAw0%3D&amp;reserved=0) | 如果其中一個帳目過帳失敗，且未處理剩餘的帳目，則批次工作會失敗。  |
| 差旅和費用 | [575378](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D575378&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225451644%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=3tW0ngQqcz8pdNFY8FVuFlsgv3l73HMgeQTLbzIAAOg%3D&amp;reserved=0) | 可以變更未附加費用的核准狀態。 |
| 差旅和費用 | [592997](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D592997&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225521336%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=0leQsokHcl2NLqePFXC6%2BuH1V5UNRWUIPx0wTUaB4vg%3D&amp;reserved=0) | 已提交至工作流程的費用報表可讓您建立新的費用明細。 |
| 差旅和費用 | [594853](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D594853&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225541248%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=5PINC45EBeV8PC0Cvtt0QPPJn0VYQ%2FRCjBmlEsZJCq4%3D&amp;reserved=0) | 您可以重設費用報表中未過帳的費用明細。 |
| 差旅和費用 | [599821](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D599821&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225610944%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=eb2CAb8L9IUDxDoukDcZQxNyI3TNQtFO%2FcjycucNj44%3D&amp;reserved=0) | 如果存在費用負責人是員工的未附加費用，您就無法啟用費用預付現金功能。 |
| 差旅和費用 | [601446](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D601446&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225650767%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=Z4CBMqrmYtlIEBWxzMEBf%2BXu5dlst7NnKcQ62yoV%2BWM%3D&amp;reserved=0) | 如果差旅請求設定為 null，則不應在費用標頭上啟用 **IsPreAuthorized**。 |
| 差旅和費用 | [601753](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D601753&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225660718%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=PVwbDhH5uqGJJZTNLddsHYlHsCknK%2FC%2FY%2Btg6fu8heo%3D&amp;reserved=0) | **費用管理** 中的 **計費** 欄位會在儲存費用時清除。 |
| 差旅和費用 | [602009](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D602009&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225680636%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=t3m29Vkxx8g96CvaDz%2FRzuciP2doP2xejomPl440wNs%3D&amp;reserved=0) | 刪除含有已選取 **從課稅項目排除** 之子類別的分項列舉時，費用報表的 **包含稅金** 滑桿會移到 **否**。 |
| 差旅和費用 | [607516](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D607516&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919225849894%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=%2BceTskfUl1kTe2XHk6QSYu9UN%2FE%2F9nP2gv20kVweURA%3D&amp;reserved=0) |會計事件為空白，且會計狀態不正確。 |
| 差旅和費用 | [617801](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D617801&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919226337756%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=L69x65xY6LQDS1u2sUbVX5QKEYgbDh6lld2Pm%2BSsUyI%3D&amp;reserved=0) | 將費用分攤到信用卡交易時，工作流程無法正確評估費用報表。 |
| 差旅和費用 | [575295](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D575295&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227074518%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=FyrzO1Yx%2BWLfw5arIrFiW07QZC%2F%2BpUk3ekx3g66X8bE%3D&amp;reserved=0) | 廠商銀行交易上不正確的報表貨幣金額會從費用報表過帳到關閉期間。 |
| 差旅和費用 | [610910](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D610910&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227134259%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=P6wVchjx9GcH7nZ07yg3%2FuEFht6Df7Ew5Z4hSL%2BQ8oY%3D&amp;reserved=0) | 在 [重新定義的費用報表] 功能中，即使建立費用時已變更付款方式，還是會填入費用明細的預設付款方式。 |
| 差旅和費用 | [617146](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D617146&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227193996%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=134C%2BXGuzA8GmM7ZjWYaiYQfNqnV9a1mEKuzrh0hzpw%3D&amp;reserved=0) | 如果啟用收據原則，您就無法提交費用報表。 |
| 差旅和費用 | [619783](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D619783&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227243778%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=pV1rLgOniDy3hXMHAtXeD9o4ZPTmyhZHd7O7zCUpLLs%3D&amp;reserved=0) | 當您提交費用報表時，會發生下列錯誤 **堆疊追蹤：公司不存在**。 |
| 差旅和費用 | [620773](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D620773&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227253737%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=%2B5ZZAsXV%2FM29%2Byg6JoGzwJFRa1Fi4NDj4BB38ZeYTH0%3D&amp;reserved=0) | 將未附加的交易重新加入至公司間費用的費用報表時，使用公司間費用明細進行分配，並不會更新法律實體。 |
| 差旅和費用 | [621967](https://nam06.safelinks.protection.outlook.com/?url=https:%2F%2Ffix.lcs.dynamics.com%2FIssue%2FDetails%2F?bugId%3D621967&amp;data=04%7C01%7Cjespers%40microsoft.com%7Cc1d2484c411149f3a93708d9a8583e14%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637725919227273644%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C3000&amp;sdata=RdiupzmL8Dp8nqQIHu9rGMTdJ%2FVVhqN5EIP5uFYS2W4%3D&amp;reserved=0) | 在與專案相關聯且使用匯入之信用卡交易所建立以外幣計價的費用報表中，廠商交易下使用報表貨幣的售價和金額計算不正確。 |
