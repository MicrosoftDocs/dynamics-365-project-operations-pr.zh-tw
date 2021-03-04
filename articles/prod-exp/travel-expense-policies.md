---
title: 設定費用原則
description: 您可以設定您的工作者在 Microsoft Dynamics 365 Finance 中輸入和提交費用報表和差旅申請時必須遵循的費用原則。
author: suvaidya
manager: AnnBe
ms.date: 05/20/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SysPolicyListPage, TrvPolicyRule
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: suvaidya
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ab99c0ec769eb2e0914fc7d993f83d20e2c327f6
ms.sourcegitcommit: 9f31b33ed6e7f1b49200a407913201a1337f3401
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 01/14/2021
ms.locfileid: "4960687"
---
# <a name="set-up-expense-policies"></a>設定費用原則

您可以定義您的工作者在輸入和提交費用報表和差旅申請時必須遵循的原則。         
實行費用原則可以協助您有效管理費用。         

例如，您可以設定紐約市住宿費用的原則，規定每夜費用不能超過美元 250。       
如果工作者提交住房費超過此金額的費用報表或差旅申請，系統就會通知        
工作者已超過費用原則的金額。 您可以在定義原則時設定工作者會收到的訊息        
。      
        
您可以定義三種類型的原則：         
        
- 警告 – 允許工作者提交費用報表或差旅申請，但會標示費用給所有核准者處理並        
  供稍後提報。        

- 錯誤 – 要求工作者必須先將費用修訂成符合原則，才能提交費用報表或差旅申請。       
 
 - 正當理由 – 要求工作者或經理必須先輸入超出原則金額的正當理由，才能提交費用報表或差旅申請。        

## <a name="policy-tips"></a>原則提示
以下是一些可在建立費用管理新原則時協助您的建議。 
* 原則有生效日期，如果原則的建立日期是在費用發生日期之後，則原則無法生效。 例如，如果您現在要建立新的原則以強制 $50 的最高餐費，則任何戳至昨天所輸入的現有費用都不會依據此原則進行檢查。
* 針對可逐條列舉的費用類別建立原則時，請考慮新增費用明細類型的條件。 有些原則 (例如，需要收據) 可能不適合逐條列舉的明細，只能套用至標題列或非逐條列舉的明細。 
* 預設會依據來源實體評估費用管理原則。 在公司間交易案例中，您可以將原則設定為改依目的地實體 (借用實體) 進行評估。 若要依據目的地實體執行原則，請開啟 **功能管理** 工作區中的 [依據借用法律實體評估費用原則] 功能。

## <a name="when-to-evaluate-policies"></a>評估原則的時機

在費用管理參數中，有選項供您選擇在儲存明細時或在提交費用報表時評估費用管理原則。 如果您選擇在儲存明細時進行評估，這可確保使用者及早了解一次全部完成其費用報表所需執行的工作。 否則，在提交至工作流程的過程中，如果結束時會進行驗證，您可以將原則評估延遲並節省時間。
