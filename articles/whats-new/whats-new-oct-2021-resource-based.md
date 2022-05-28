---
title: 2021 年 10 月新增功能 - 資源/非庫存型案例適用的 Project Operations
description: 本主題提供有關資源/非庫存型案例適用 Project Operations 2021 年 10 月發行版本中所提供之品質更新的資訊。
author: sigitac
ms.date: 10/06/2021
ms.topic: article
ms.prod: ''
ms.reviewer: johnmichalak
ms.author: sigitac
ms.openlocfilehash: c64ef1e2ba9e33b2ca7575a40cc51e0ae987a9f8
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8598478"
---
# <a name="whats-new-october-2021---project-operations-for-resourcenon-stocked-based-scenarios"></a>2021 年 10 月新增功能 - 資源/非庫存型案例適用的 Project Operations

*適用於：資源/非庫存型案例適用的 Project Operations*

此主題適用於下列 Dynamics 365 Project Operations 元件和版本：

   - Microsoft Dataverse 環境版本 4.25.0.91 中的 Project Operations
   - Dynamics 365 Finance 環境 10.0.21 版中的專案管理與會計

## <a name="features-included-in-this-release"></a>此版本包含的功能

此版本包含下列功能：

- [專案採購單](../procurement/non-stocked-materials-project-purchase-orders.md)現在可用於負責對專案採購進行管理/集中處理的採購部門的。
- [廠商留成](../procurement/vendor-retention-overview.md)允許您保留一部分支付給廠商的款項。

## <a name="project-operations-dual-write-maps-updates"></a>Project Operations 雙重寫入對應更新

此版本中沒有 Project Operations 雙重寫入對應的更新。 如需 Project Operations 雙重寫入對應的最新清單和版本，請參閱 [Project Operations 雙重寫入對應版本](../environment/resource-dual-write-maps.md)。

更新 Project Operations Dataverse 解決方案和 Finance 解決方案版本時，請務必在您的環境中執行最新版本的對應，並啟用所有相關的表格對應。 如果未啟用最新版本的對應，特定功能可能無法正確運作。 您可以在雙重寫入頁面的版本欄中查看對應的使用中版本。 若要啟用新的對應版本，請選取資料表對應版本、選取最新版本，然後儲存選取的版本。 如果您已對現成可用的資料表對應進行自訂，請重新套用變更。 如需詳細資訊，請參閱[解決方案生命週期管理](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/app-lifecycle-management)。

如果開始進行對應時發生問題，請依照《雙重寫入疑難排解指南》中[對應上的遺失資料資料行問題](/dynamics365/fin-ops-core/dev-itpro/data-entities/dual-write/dual-write-troubleshooting-finops-upgrades#missing-table-columns-issue-on-maps)一節的指示操作。

## <a name="quality-updates"></a>品質更新

### <a name="project-operations-on-dataverse"></a>Dataverse 上的 Project Operations

| **功能區域** | **參考編號** | **品質更新** |
| --- | --- | --- |
| 帳單和定價 | 2209402 | 更正確認專案合約時造成無法開立保留款金額發票的驗證。 |
|   商機管理 | 2227414 | **產品**、**目錄外** 和 **IsProductOverriden** 欄位會複製到報價明細詳細資料和合約服務內容詳細資料。 |
| 帳單和定價 | 2338357 | 選取專案時，材料使用記錄中的貨幣必須預設為專案的貨幣。 |
| 時間和費用 | 2414777 | 當費用或時間項目有多個相關聯的專案核准時，一定可以取消核准。 |

### <a name="project-management-and-accounting-on-dynamics-365-finance"></a>Dynamics 365 Finance 中的專案管理與會計

| 功能區域 | 參考編號 | 品質更新 |
| --- | --- | --- |
| 專案管理與會計 | [412077](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D412077&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020681298%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=JT2OvagELTPqep4rOiFTwGYF80KkgSHgBJmd%2BHBBgA8%3D&amp;reserved=0) | 允許採購經理角色存取一個法律實體時，也會篩選對所有法律實體中所有專案的存取。 |
| 專案管理與會計 | [555604](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D555604&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020701214%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=NGAT/5r0sezqdisYP%2BDzyFDDi5f9gyrr5ZhJZaDLV0k%3D&amp;reserved=0) | 啟用 **啟用專案合約貨幣以計算估計值** 功能時，估計值消除失敗。 |
| 專案管理與會計 | [564701](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D564701&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020731079%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=IyhrFb59YBXjNpJdtPhlEDxoYiFCTrqzQtKZsBZk2DM%3D&amp;reserved=0) | [FRA] 將廠商留成和預付款套用至採購單發票時，未正確計算上次付款的優惠稅額。 |
| 專案管理與會計 | [569250](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D569250&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020741035%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=YcB6z9MvvtiyT9d8g2GkHXDUcNfnPdxlYsHblbk%2BCXs%3D&amp;reserved=0) | WIP 過帳至總帳時使用不正確的金額過帳。 |
| 專案管理與會計 | [581167](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D581167&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020989941%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=9UjX3lX/DOJOPiz%2BlYVge5F3Tpbb%2BUBaN7PVXkpwYJE%3D&amp;reserved=0) | 專案發票報表跳過幾行明細。 |
| 專案管理與會計 | [598810](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D598810&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021408104%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=f2oJYnmjpfUiIKvF6qfLsBcfTjoSOq955%2B87%2BSIh0Io%3D&amp;reserved=0) | 專案發票過帳批次有問題，即使尚未產生發票明細，則該批次仍會處理並過帳發票提案。 |
| 專案管理與會計 | [578970](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D578970&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021876048%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=JMg%2BIRbLiSKeIXN/JArWC3hSGFhNhabERbuKzGBKCC8%3D&amp;reserved=0) | 更新 [建立專案估計值] 批次工作以支援執行多個子工作。 |
| 專案管理與會計 | [586034](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586034&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021895962%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MRGsdBRM5spFKDJZ/IjrAoWy%2BGTyFVyUU7SCfFJSj6g%3D&amp;reserved=0) | 憑單交易未依「XXXX/XX/XX」事項達到借貸平衡 (會計貨幣：0.00 - 報表貨幣： 0.01)。 |
| 專案管理與會計 | [596669](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D596669&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021955698%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=IpJrV7LW0CegdNrRXfDqBhLEsy8tlSvlaipvZBQFZVg%3D&amp;reserved=0) | 法律實體的免稅號碼未顯示在列印的專案發票上。 |
| 專案管理與會計 | [598109](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D598109&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021975611%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=erjkqXSdKwjU62xNiVEJomzc5JoiiC9U7f6ofrv4KGE%3D&amp;reserved=0) | 套用了 KB 4619395 之後，不支援過帳估計值時的連續編號序列。 |
| 專案管理與會計 | [602677](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D602677&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022015436%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=4TBJC6dKbgZxWQTlyDkTm%2BzHpL%2BJx5ZcueNWkMJfUK4%3D&amp;reserved=0) | 發票過帳的 WIP 沖回值與時間項目的原始過帳 WIP 值不同。 |
| 專案管理與會計 | [602728](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D602728&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022015436%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=Ux5tLxoBzA%2BJtbf5MhLB63/GNJqYcBg8PH4tncXLTsM%3D&amp;reserved=0) | 由於與專案已開立發票的收入在已套用保留款的案例中發生過帳問題，憑單交易未正確達到借貸平衡。 |
| 專案管理與會計 | [607324](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D607324&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642022065219%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=I/SwbTsPpFvMkxLIK7JpligW%2B4nlObh3nCCSppVGvhE%3D&amp;reserved=0) | 只會一期的專案估計值。 |
| 差旅和費用 | [551911](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D551911&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020701214%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=fDFL3GM5jXJAzIzxwRlOIaq3/ytSHXnpIzGsC4Jjphg%3D&amp;reserved=0) | 差旅申請原則遭忽略，直接在不發生錯誤的情況下核准工作流程。 |
| 差旅和費用 | [563752](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D563752&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020731079%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=SVrkNdniaVfhOjc3Brf1gtrFv3SJpPNQ4JYOGnCOxlQ%3D&amp;reserved=0) | 費用明細專案識別碼、應計費項目和活動編號未儲存在行動費用應用程式中。 |
| 差旅和費用 | [569458](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D569458&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020750990%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=cC33gCOlM8aa3jR5Hy1Hubf5bszsu2YWwraLLrIYCYk%3D&amp;reserved=0) | 即使費用明細沒有附加收據，**附加的收據** 欄位仍會設定為 **是**。 |
| 差旅和費用 | [571334](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D571334&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020760950%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=Y6dd19CzWyWPa%2BItpWXBEgUuSx8evJxth6VslSRMYsg%3D&amp;reserved=0) | 嘗試將費用類別變更為 **個人** 時，會出現錯誤訊息。 |
| 差旅和費用 | [572783](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D572783&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020770904%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=nugD/4Rj3d8CNanZf%2BY3vNm9aRqHoh5vF/bHFZD9UxE%3D&amp;reserved=0) | 在費用報表上分割信用卡交易之後，您無法編輯上層費用或附加收據。 |
| 差旅和費用 | [574252](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574252&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020790818%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=uKYIlgBpKju4jBH%2BK8GXVKCgi6kxSG1AxXVvF75WsbA%3D&amp;reserved=0) | 費用原則對包含專案識別碼的公司間交易無法正確發揮作用。 |
| 差旅和費用 | [574489](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574489&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020800774%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=ErBwfDvDtWWzEJP3STHd5kzPjTe7%2B4nCeG02kH64dWU%3D&amp;reserved=0) | 已過帳的費用報表缺少過帳日期。 |
| 差旅和費用 | [574504](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D574504&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642020800774%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=SeW6L68CNpJ86TJ2aNqLZoTMq5PHRfu3542mNkKqf%2Bg%3D&amp;reserved=0) | 費用行動應用程式有付款方式問題。 |
| 差旅和費用 | [584799](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D584799&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021129331%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=4Q%2B/R9wPra2P/%2BEk63qgSenyNoJMa5OJsBv2Nn9s%2B%2Bo%3D&amp;reserved=0) | 一個工作人員建立的差旅申請可以用於另一個工作人員的費用報表，而且可以在委派日期之前使用該差旅申請。 |
| 差旅和費用 | [586023](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586023&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021169156%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=d9Kmf1ng415Uw0U4aQ5N%2B0RboRmjDW1S2lt91rG9ofc%3D&amp;reserved=0) | 建立費用時，變更財務維度值無法在 **費用管理** 工作區的會計分配層級正確更新。 |
| 差旅和費用 | [586081](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D586081&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021179116%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=LlWjcIANIl1gudmiD4WIsluKkF21w9EgVC5uDvBOzg4%3D&amp;reserved=0) | 主要費用明細核准狀態未與分項列出的明細工作流程核准狀態進行同步處理。 |
| 差旅和費用 | [590544](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D590544&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021318495%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MolkGywocB%2BG404npaOv7fcfunnlDUGgAYFOcw8OlKg%3D&amp;reserved=0) | 如果在費用管理參數中啟用 **退稅**，則會在過帳費用報表時發生錯誤。 |
| 差旅和費用 | [564851](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D564851&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021856138%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=YBsBJdzH%2BqbGzq07u7WILEs%2Bi5Ap6WYzqWnpGWcI4Ac%3D&amp;reserved=0) | 代理人無法為離職員工刪除費用憑證。 |
| 差旅和費用 | [587306](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D587306&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021905919%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=TbWDuK1sHY//jTw%2BmehJG3M3N3feEl2oRkTMTkqWOVE%3D&amp;reserved=0) | 刪除費用明細需要較長時間，並影響效能。 |
| 差旅和費用 | [600455](https://nam06.safelinks.protection.outlook.com/?url=https://fix.lcs.dynamics.com/Issue/Details/?bugId%3D600455&amp;data=04%7C01%7Cjespers%40microsoft.com%7C1ece6f38724a460c13bc08d96784b455%7C72f988bf86f141af91ab2d7cd011db47%7C1%7C0%7C637654642021995524%7CUnknown%7CTWFpbGZsb3d8eyJWIjoiMC4wLjAwMDAiLCJQIjoiV2luMzIiLCJBTiI6Ik1haWwiLCJXVCI6Mn0%3D%7C1000&amp;sdata=MH0sIRbAKhNNyAgYZzO9NovWHM7ZWKsoZYqXCIVHJ5A%3D&amp;reserved=0) | **TrvExpTrans** 會因為只刪除 **SourceDocumentLine** 而產生孤立 **TaxUncommitted** 記錄。 |
