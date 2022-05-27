---
title: 定義費用原則
description: 您可以定義您的工作者在輸入和提交費用報表和差旅申請時必須遵循的費用原則。
author: suvaidya
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.search.form: ''
audience: Application User
ms.reviewer: johnmichalak
ms.search.scope: ''
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: ''
ms.dyn365.ops.version: ''
ms.openlocfilehash: 8ae6de664fc18a00fd6d3d6c8177daa95da5754d
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8576904"
---
# <a name="define-expense-policies"></a>定義費用原則

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

您可以定義您的工作者在輸入和提交費用報表和差旅申請時必須遵循的原則。         
實行費用原則可以協助您有效管理費用。         

例如，您可以設定紐約市住宿費用的原則，規定每夜費用不能超過美元 250。       
如果工作者提交住房費超過此金額的費用報表或差旅申請，系統就會通知         
工作者已超過費用原則的金額。 您可以在定義原則時設定工作者會收到的訊息        
。      
        
您可以定義三種類型的原則：         
        
- **警告**：允許工作者提交費用報表或差旅申請，但會標示費用給所有核准者處理並         
  供稍後提報。        

- **錯誤**：要求工作者必須先將費用修訂成符合原則，才能提交費用報表或差旅申請。        
 
 - **正當理由**：要求工作者或經理必須先輸入超出原則金額的正當理由，才能提交費用報表或差旅申請。        

## <a name="policy-tips"></a>原則提示
以下是一些可在建立費用管理新原則時協助您的建議： 

- 原則有生效日期，這表示如果原則的建立日期是在費用發生日期之後，則原則無法生效。 例如，您今天建立新原則以強制 $50 的餐費上限。 任何截至昨天的現有費用都不會根據此原則進行檢查。
- 針對可逐條列舉的費用類別建立原則時，請考慮新增費用明細類型的條件。 有些原則 (例如，要求附上收據) 可能對逐條列舉的明細沒有意義。 在這種情況下，只會將原則套用至標題列或非逐條列舉的明細。 
- 預設會依據來源實體評估費用管理原則。 在公司間交易案例中，您可以將原則設定為改依目的地實體 (借用實體) 進行評估。 若要依據目的地實體執行原則，請開啟 **功能管理** 工作區中的 **依據借用法律實體評估費用原則** 功能。

## <a name="when-to-evaluate-policies"></a>評估原則的時機

在費用管理參數中，您可以選擇在儲存明細時或在提交費用報表時評估費用管理原則。 如果您選擇在儲存明細時進行評估，則使用者可以較早了解一次全部完成其費用報表所需執行的工作。 否則您可以在提交至工作流程的過程中，將原則評估延遲，並透過在結束時驗證的方式節省時間。


[!INCLUDE[footer-include](../includes/footer-banner.md)]