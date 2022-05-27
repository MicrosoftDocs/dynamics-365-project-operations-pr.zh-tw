---
title: 新式核准的升級考量
description: 本主題探討啟用新式核准功能時，系統管理員應納入考量的要點。
author: stsporen
ms.date: 01/31/2022
ms.topic: article
ms.reviewer: johnmichalak
ms.author: stsporen
ms.openlocfilehash: a3757f057a801318feccde9be3e49c7b40fa8fcb
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8578376"
---
# <a name="upgrade-considerations-for-modern-approvals"></a>新式核准的升級考量 

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

在 2022 年 4 月第 1 段發行浪潮中，預設會啟用新式核准功能。 此功能改善核准邏輯的可靠性，並確保您可以在核准邏輯失敗時判斷出原因。

在此變更過程中，也會更新專案核准的狀態變更。 狀態會立即從 **已提交** 直接進入 **已核准**。 **擱置** 不再是核准的狀態。 若要判斷核准是否在擱置中，請確認此核准屬於核准集的一部分，並檢閱附加核准集的狀態。

## <a name="before-you-upgrade"></a>升級之前

升級至新式核准之前，請確定您沒有任何擱置中的核准。 新式核准不使用 **擱置** 狀態。 因此，將不會處理任何在升級後仍標示為 **擱置** 的核准。

## <a name="after-you-upgrade"></a>升級之後

升級至新式核准之後，系統管理員必須驗證是否已啟用處理核准的雲端流程。

1. 登入 [flow.microsoft.com](https://flow.microsoft.com)
2. 在頁面右上方，將環境切換至您已升級的環境。
3. 選取 **解決方案**，以列出環境中已安裝的解決方案。
4. 在解決方案清單中，選取 **Project Operations** 或 **Project Service**。
5. 將篩選條件從 **全部** 變更為 **雲端流程**。
6. 確認 **Project Service – 週期性地排程專案核准集** 選項是否已設定為 **開啟**。 如果不是，請選取流程，然後選取 **開啟**。
7. 檢閱 **設定** 區域中的 **系統作業** 清單，確認是否會每隔五分鐘進行處理一次。

## <a name="short-term-rollback"></a>短期復原

如果您無法接受變更，或者此功能發生嚴重問題，則可以執行下列步驟暫時還原到原始核准流程：
1. 登入您的環境，並確認沒有任何擱置的核准。
2. 移至 **設定** > **專案參數**。
3. 選取 **功能控制**，然後選取 **新式核准** 以關閉功能。

## <a name="removing-the-feature-flag"></a>移除功能旗標

在 2022 年 10 月第 2 段更新浪潮中，將會移除關閉此功能的功能。

[!INCLUDE[footer-include](../includes/footer-banner.md)]
