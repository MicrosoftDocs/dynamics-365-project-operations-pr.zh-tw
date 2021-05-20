---
title: 排程模式
description: 本主題提供有關排程模式的資訊。
author: ruhercul
manager: AnnBe
ms.date: 05/04/2021
ms.topic: article
ms.service: project-operations
ms.reviewer: kfend
ms.author: ruhercul
ms.openlocfilehash: fe54944999617b248ff925148a78601dd4be7aca
ms.sourcegitcommit: c45ceda833b30ad39861f5bcd3ba1bbfff11fe7a
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 05/04/2021
ms.locfileid: "5981425"
---
# <a name="scheduling-modes"></a><span data-ttu-id="c7dc0-103">排程模式</span><span class="sxs-lookup"><span data-stu-id="c7dc0-103">Scheduling modes</span></span>

<span data-ttu-id="c7dc0-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="c7dc0-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>


<span data-ttu-id="c7dc0-105">Dynamics 365 Project Operations 可讓組織定義他們如何在分工結構圖中管理工作中重要變數的變更。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-105">Dynamics 365 Project Operations provides the ability for organizations to define how they manage changes to key variables in tasks within the work breakdown structure.</span></span> <span data-ttu-id="c7dc0-106">根據組織的特定需求，專案經理可在建立專案時變更排程模式。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-106">Based on the specific needs of the organization, Project Managers can make changes to the scheduling mode when a project is created.</span></span>

<span data-ttu-id="c7dc0-107">Project Operations 中有三種可用的排程模式：</span><span class="sxs-lookup"><span data-stu-id="c7dc0-107">There are three scheduling modes available in Project Operations:</span></span>

  - <span data-ttu-id="c7dc0-108">固定期間 (這是預設模式)</span><span class="sxs-lookup"><span data-stu-id="c7dc0-108">Fixed duration (this is the default mode)</span></span>
  - <span data-ttu-id="c7dc0-109">固定工時</span><span class="sxs-lookup"><span data-stu-id="c7dc0-109">Fixed work</span></span>
  - <span data-ttu-id="c7dc0-110">固定單位</span><span class="sxs-lookup"><span data-stu-id="c7dc0-110">Fixed units</span></span>

<span data-ttu-id="c7dc0-111">受特定排程模式定義影響的值是由下列公式所決定：</span><span class="sxs-lookup"><span data-stu-id="c7dc0-111">The values impacted by the definition of a specific scheduling mode are determined by the following formula:</span></span>

  <span data-ttu-id="c7dc0-112">投入量 (*工作*) = 期間 x 單位</span><span class="sxs-lookup"><span data-stu-id="c7dc0-112">Effort (*Work*) = Duration x Units</span></span>

<span data-ttu-id="c7dc0-113">當您定義專案的排程模式時，即是在設定這其中一個值，而這些值隨後就無法變更。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-113">When you define a project’s scheduling mode, you are setting one of these values, which then can't be changed.</span></span> <span data-ttu-id="c7dc0-114">將此值保留為常數會將該值置於優先位置，通知系統不要在其他兩個值變更時變更此值。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-114">Holding this value as a constant places a priority on that value, which notifies the system not to change it when the other two values change.</span></span> <span data-ttu-id="c7dc0-115">下表提供有關選取特定模式所造成影響的資訊。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-115">The following table provides information about the impacts of selecting a specific mode.</span></span>

| <span data-ttu-id="c7dc0-116">**在此工作中**</span><span class="sxs-lookup"><span data-stu-id="c7dc0-116">**In this task**</span></span>             | <span data-ttu-id="c7dc0-117">**如果您修訂單位數**</span><span class="sxs-lookup"><span data-stu-id="c7dc0-117">**If you revise units**</span></span>   | <span data-ttu-id="c7dc0-118">**如果您修訂期間**</span><span class="sxs-lookup"><span data-stu-id="c7dc0-118">**If you revise duration**</span></span> | <span data-ttu-id="c7dc0-119">**如果您修訂投入量**</span><span class="sxs-lookup"><span data-stu-id="c7dc0-119">**If you revise effort**</span></span>  |
|----------------------|---------------------------|----------------------------|---------------------------|
| <span data-ttu-id="c7dc0-120">固定單位工作</span><span class="sxs-lookup"><span data-stu-id="c7dc0-120">Fixed units task</span></span>     | <span data-ttu-id="c7dc0-121">重新計算期間。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-121">Duration is recalculated.</span></span> | <span data-ttu-id="c7dc0-122">重新計算投入量。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-122">Effort is recalculated.</span></span>    | <span data-ttu-id="c7dc0-123">重新計算期間。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-123">Duration is recalculated.</span></span> |
| <span data-ttu-id="c7dc0-124">固定投入量工作</span><span class="sxs-lookup"><span data-stu-id="c7dc0-124">Fixed effort task</span></span>    | <span data-ttu-id="c7dc0-125">重新計算期間。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-125">Duration is recalculated.</span></span> | <span data-ttu-id="c7dc0-126">重新計算單位。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-126">Units are recalculated.</span></span>    | <span data-ttu-id="c7dc0-127">重新計算期間。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-127">Duration is recalculated.</span></span> |
| <span data-ttu-id="c7dc0-128">固定期間工作</span><span class="sxs-lookup"><span data-stu-id="c7dc0-128">Fixed duration task</span></span>  | <span data-ttu-id="c7dc0-129">重新計算投入量。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-129">Effort is recalculated.</span></span>   | <span data-ttu-id="c7dc0-130">重新計算投入量。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-130">Effort is recalculated.</span></span>    | <span data-ttu-id="c7dc0-131">重新計算單位。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-131">Units are recalculated.</span></span>   |

<span data-ttu-id="c7dc0-132">如需指定模式隱含意義的詳細資訊，請參閱[變更工作類型以取得更準確的排程](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72)。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-132">For more information about the implications of a given mode, see [Change the task type for more accurate scheduling](https://support.microsoft.com/en-us/office/change-the-task-type-for-more-accurate-scheduling-b0b969ad-45bc-4e9e-8967-435587548a72).</span></span> <span data-ttu-id="c7dc0-133">在主題中，使用的是 **工作** 一詞，而不是 **投入量**。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-133">In the topic, the term **Work** is used instead of **Effort**.</span></span>

## <a name="change-the-organizations-scheduling-mode"></a><span data-ttu-id="c7dc0-134">變更組織的排程模式</span><span class="sxs-lookup"><span data-stu-id="c7dc0-134">Change the organization’s scheduling mode</span></span>

<span data-ttu-id="c7dc0-135">完成下列步驟，以定義組織的排程模式。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-135">Complete the following steps to define the scheduling mode of an organization.</span></span>

1. <span data-ttu-id="c7dc0-136">移至 **設定** \> **一般** \> **參數**，然後選取專案參數。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-136">Go to **Settings** \> **General** \> **Parameters**, and then select the project parameter.</span></span> 
2. <span data-ttu-id="c7dc0-137">在 **專案參數** 頁面上，選取組織的預設排程模式，然後定義專案經理可在建立新專案時覆寫設定的能力。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-137">On the **Project Parameters** page, select the default scheduling mode for the organization, and then define ability for the Project manager to override the setting when creating a new project.</span></span>

## <a name="change-the-scheduling-mode-setting-on-a-project"></a><span data-ttu-id="c7dc0-138">變更專案的排程模式設定</span><span class="sxs-lookup"><span data-stu-id="c7dc0-138">Change the scheduling mode setting on a project</span></span>

<span data-ttu-id="c7dc0-139">如果組織允許專案經理覆寫預設排程模式，則專案經理可在建立新專案時進行該變更。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-139">If an organization allows the Project manager to override the default scheduling mode, the Project manager can make that change when they create a new project.</span></span> <span data-ttu-id="c7dc0-140">不過，儲存專案之後，就無法變更排程模式。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-140">However, after the project has been saved, the scheduling mode can't be changed.</span></span>

## <a name="copied-projects"></a><span data-ttu-id="c7dc0-141">複製的專案</span><span class="sxs-lookup"><span data-stu-id="c7dc0-141">Copied projects</span></span>

<span data-ttu-id="c7dc0-142">由於專案是在執行複製專案動作時所建立，因此專案經理無法設定排程模式。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-142">Because a project is created when the copy project action is taken, the Project manager can't set the scheduling mode.</span></span> <span data-ttu-id="c7dc0-143">目的地專案永遠預設為組織層級定義的模式。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-143">The destination project will always default to the mode defined at the organizational level.</span></span>

## <a name="copied-tasks"></a><span data-ttu-id="c7dc0-144">複製的工作</span><span class="sxs-lookup"><span data-stu-id="c7dc0-144">Copied tasks</span></span>

<span data-ttu-id="c7dc0-145">將工作從一個專案複製到另一個時，工作會繼承目的地專案的排程模式。</span><span class="sxs-lookup"><span data-stu-id="c7dc0-145">When a task is copied from one project to another, the task inherits the scheduling mode of the destination project.</span></span>
