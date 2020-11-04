---
title: 擴充時間項目
description: 本主題提供有關開發人員如何擴充時間項目控制項的資訊。
author: stsporen
manager: Annbe
ms.date: 10/08/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 190ad9e1f9ced690aee953ed992bf7aa2844c3b3
ms.sourcegitcommit: 11a61db54119503e82faec5f99c4273e8d1247e5
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4072895"
---
# <a name="extending-time-entries"></a><span data-ttu-id="cd861-103">擴充時間項目</span><span class="sxs-lookup"><span data-stu-id="cd861-103">Extending time entries</span></span>

<span data-ttu-id="cd861-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="cd861-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="cd861-105">Dynamics 365 Project Operations 包含可擴充的時間項目自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="cd861-105">Dynamics 365 Project Operations includes an extendable time entry custom control.</span></span> <span data-ttu-id="cd861-106">此控制項包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="cd861-106">This control includes the following features:</span></span>

- <span data-ttu-id="cd861-107">輸入橫跨一週的時間</span><span class="sxs-lookup"><span data-stu-id="cd861-107">Enter time horizontally over a week</span></span>
- <span data-ttu-id="cd861-108">依日、列或週的總計</span><span class="sxs-lookup"><span data-stu-id="cd861-108">Totals by day, row, or week</span></span>
- <span data-ttu-id="cd861-109">複製列或週</span><span class="sxs-lookup"><span data-stu-id="cd861-109">Copy rows or weeks</span></span>
- <span data-ttu-id="cd861-110">透過 HH:mm 或 HH.hh (自動轉換為 HH.hh) 輸入的時間項目</span><span class="sxs-lookup"><span data-stu-id="cd861-110">Time entry through HH:mm or HH.hh (automatically converts to HH.hh)</span></span>
- <span data-ttu-id="cd861-111">從指派、預約或約會匯入</span><span class="sxs-lookup"><span data-stu-id="cd861-111">Import from assignments, bookings, or appointments</span></span>

<span data-ttu-id="cd861-112">時間項目可在兩個區域中進行擴充：</span><span class="sxs-lookup"><span data-stu-id="cd861-112">Extending time entries is possible in two areas:</span></span>
- [<span data-ttu-id="cd861-113">新增自訂時間項目供自己使用</span><span class="sxs-lookup"><span data-stu-id="cd861-113">Add custom time entries for your own use</span></span>](#add)
- [<span data-ttu-id="cd861-114">自訂每週時間項目控制項</span><span class="sxs-lookup"><span data-stu-id="cd861-114">Customize the weekly Time Entry control</span></span>](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a><span data-ttu-id="cd861-115">新增自訂時間項目供自己使用</span><span class="sxs-lookup"><span data-stu-id="cd861-115">Add custom time entries for your own use</span></span>

<span data-ttu-id="cd861-116">時間項目是多個案例中所使用的核心實體。</span><span class="sxs-lookup"><span data-stu-id="cd861-116">Time entries are a core entity used in multiple scenarios.</span></span> <span data-ttu-id="cd861-117">在 2020 年 4 月第 1 段浪潮中，推出了 TESA 核心解決方案。</span><span class="sxs-lookup"><span data-stu-id="cd861-117">In April Wave 1 2020, the TESA core solution was introduced.</span></span> <span data-ttu-id="cd861-118">TESA 提供 **設定** 實體以及新的 **時間項目使用者** 資訊安全角色。</span><span class="sxs-lookup"><span data-stu-id="cd861-118">TESA provides a **Settings** entity and a new **Time Entry User** security role.</span></span> <span data-ttu-id="cd861-119">其中也包含與 **msdyn_duration** 有直接關聯的新欄位 **msdyn_start** 和 **msdyn_end** 。</span><span class="sxs-lookup"><span data-stu-id="cd861-119">The new fields, **msdyn_start** and **msdyn_end** , which have a direct relation to **msdyn_duration** , were also included.</span></span> <span data-ttu-id="cd861-120">新的實體、資訊安全角色及欄位讓您有更統一的方法可以跨多個產品處理時間。</span><span class="sxs-lookup"><span data-stu-id="cd861-120">The new entity, security role, and fields allow for a more unified approach to time across multiple products.</span></span>


### <a name="time-source-entity"></a><span data-ttu-id="cd861-121">時間來源實體</span><span class="sxs-lookup"><span data-stu-id="cd861-121">Time source entity</span></span>
| <span data-ttu-id="cd861-122">欄位</span><span class="sxs-lookup"><span data-stu-id="cd861-122">Field</span></span> | <span data-ttu-id="cd861-123">描述</span><span class="sxs-lookup"><span data-stu-id="cd861-123">Description</span></span> | 
|-------|------------|
| <span data-ttu-id="cd861-124">名字</span><span class="sxs-lookup"><span data-stu-id="cd861-124">Name</span></span>  | <span data-ttu-id="cd861-125">時間來源實體的名稱會在建立時間項目時用來做為選取值。</span><span class="sxs-lookup"><span data-stu-id="cd861-125">The name of the Time source entry used as the selection value when creating time entries.</span></span> |
| <span data-ttu-id="cd861-126">預設時間來源 [時間來源：isdefault]</span><span class="sxs-lookup"><span data-stu-id="cd861-126">Default Time Source [Time Source: isdefault]</span></span> | <span data-ttu-id="cd861-127">根據預設，能以預設標示的僅限一個時間來源。</span><span class="sxs-lookup"><span data-stu-id="cd861-127">By default, only one Time Source can be marked at the default.</span></span> <span data-ttu-id="cd861-128">這允許項目預設為時間來源 (如果未指定的話)。</span><span class="sxs-lookup"><span data-stu-id="cd861-128">This allows for entries to default to a time source if one isn't specified.</span></span> |
|<span data-ttu-id="cd861-129">時間來源類型 [時間來源：sourcetype]</span><span class="sxs-lookup"><span data-stu-id="cd861-129">Time Source Type [Time Source: sourcetype]</span></span> | <span data-ttu-id="cd861-130">來源類型是允許將時間來源關聯至應用程式的選項 (時間項目來源類型)。</span><span class="sxs-lookup"><span data-stu-id="cd861-130">The source type is an option (Time Entry Source Type) that allows for the association of the time source to an app.</span></span> <span data-ttu-id="cd861-131">Microsoft 會保留大於 190,000,000 的值。</span><span class="sxs-lookup"><span data-stu-id="cd861-131">Microsoft reserves values greater than 190,000,000.</span></span>|


### <a name="time-entries-and-the-time-source-entity"></a><span data-ttu-id="cd861-132">時間項目和時間來源實體</span><span class="sxs-lookup"><span data-stu-id="cd861-132">Time entries and the Time source entity</span></span>
<span data-ttu-id="cd861-133">每個時間項目都會與時間來源記錄建立關聯。</span><span class="sxs-lookup"><span data-stu-id="cd861-133">Each time entry is associated to a time source record.</span></span> <span data-ttu-id="cd861-134">此記錄可決定應用程式應如何處理時間項目以及應由哪些應用程式來處理。</span><span class="sxs-lookup"><span data-stu-id="cd861-134">This record determines how and which applications should process the time entry.</span></span>

<span data-ttu-id="cd861-135">時間項目永遠都是一個已連結開始、結束及期間的時間連續區塊。</span><span class="sxs-lookup"><span data-stu-id="cd861-135">Time entries are always one contiguous block of time with the start, end, and duration linked.</span></span>

<span data-ttu-id="cd861-136">邏輯會自動在下列情況中更新時間項目記錄：</span><span class="sxs-lookup"><span data-stu-id="cd861-136">The logic will automatically update the time entry record in the following situations:</span></span>

- <span data-ttu-id="cd861-137">如果提供下列三個欄位中的兩個，則會自動計算第三個欄位：</span><span class="sxs-lookup"><span data-stu-id="cd861-137">If two of the three following fields are provided, the third is calculated automatically:</span></span> 

    - <span data-ttu-id="cd861-138">**msdyn_start**</span><span class="sxs-lookup"><span data-stu-id="cd861-138">**msdyn_start**</span></span>
    - <span data-ttu-id="cd861-139">**msdyn_end**</span><span class="sxs-lookup"><span data-stu-id="cd861-139">**msdyn_end**</span></span>
    - <span data-ttu-id="cd861-140">**msdyn_duration**</span><span class="sxs-lookup"><span data-stu-id="cd861-140">**msdyn_duration**</span></span>

- <span data-ttu-id="cd861-141">欄位 **msdyn_start** 和 **msdyn_end** 是時區感知欄位。</span><span class="sxs-lookup"><span data-stu-id="cd861-141">The fields, **msdyn_start** and **msdyn_end** are timezone aware.</span></span>
- <span data-ttu-id="cd861-142">僅使用指定的 **msdyn_date** 和 **msdyn_duration** 所建立的時間項目將會從午夜開始。</span><span class="sxs-lookup"><span data-stu-id="cd861-142">Time entries created with only **msdyn_date** and **msdyn_duration** specified will start at midnight.</span></span> <span data-ttu-id="cd861-143">**msdyn_start** 和 **msdyn_end** 欄位也會相應更新。</span><span class="sxs-lookup"><span data-stu-id="cd861-143">The **msdyn_start** and **msdyn_end** fields will update accordingly.</span></span>

#### <a name="time-entry-types"></a><span data-ttu-id="cd861-144">時間項目類型</span><span class="sxs-lookup"><span data-stu-id="cd861-144">Time entry types</span></span>

<span data-ttu-id="cd861-145">時間項目記錄的關聯類型會定義相關聯應用程式在提交流程中的行為。</span><span class="sxs-lookup"><span data-stu-id="cd861-145">Time entry records have an associated type that defines the behavior in the submission flow for the associated application.</span></span>

|<span data-ttu-id="cd861-146">標籤</span><span class="sxs-lookup"><span data-stu-id="cd861-146">Label</span></span> | <span data-ttu-id="cd861-147">值</span><span class="sxs-lookup"><span data-stu-id="cd861-147">Value</span></span>|
|-----|-----|
|<span data-ttu-id="cd861-148">休息</span><span class="sxs-lookup"><span data-stu-id="cd861-148">On break</span></span>   |<span data-ttu-id="cd861-149">192,355,000</span><span class="sxs-lookup"><span data-stu-id="cd861-149">192,355,000</span></span>|
|<span data-ttu-id="cd861-150">差旅</span><span class="sxs-lookup"><span data-stu-id="cd861-150">Travel</span></span> | <span data-ttu-id="cd861-151">192,355,001</span><span class="sxs-lookup"><span data-stu-id="cd861-151">192,355,001</span></span>|
|<span data-ttu-id="cd861-152">加班時間</span><span class="sxs-lookup"><span data-stu-id="cd861-152">Overtime</span></span>   | <span data-ttu-id="cd861-153">192,354,320</span><span class="sxs-lookup"><span data-stu-id="cd861-153">192,354,320</span></span>|
|<span data-ttu-id="cd861-154">工作</span><span class="sxs-lookup"><span data-stu-id="cd861-154">Work</span></span>   | <span data-ttu-id="cd861-155">192,350,000</span><span class="sxs-lookup"><span data-stu-id="cd861-155">192,350,000</span></span>|
|<span data-ttu-id="cd861-156">缺席</span><span class="sxs-lookup"><span data-stu-id="cd861-156">Absence</span></span>    | <span data-ttu-id="cd861-157">192,350,001</span><span class="sxs-lookup"><span data-stu-id="cd861-157">192,350,001</span></span>|
|<span data-ttu-id="cd861-158">休假</span><span class="sxs-lookup"><span data-stu-id="cd861-158">Vacation</span></span>   | <span data-ttu-id="cd861-159">192,350,002</span><span class="sxs-lookup"><span data-stu-id="cd861-159">192,350,002</span></span>|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a><span data-ttu-id="cd861-160">自訂每週時間項目控制項</span><span class="sxs-lookup"><span data-stu-id="cd861-160">Customize the weekly Time entry control</span></span>
<span data-ttu-id="cd861-161">開發人員可以將額外的欄位和查詢新增至其他實體，並實作自訂商務規則以支援其業務案例。</span><span class="sxs-lookup"><span data-stu-id="cd861-161">Developers can add additional fields and lookups to other entities, and implement custom business rules to support their business scenarios.</span></span>

### <a name="add-custom-fields-with-lookups-to-other-entities"></a><span data-ttu-id="cd861-162">新增具有其他實體查詢的自訂欄位</span><span class="sxs-lookup"><span data-stu-id="cd861-162">Add custom fields with lookups to other entities</span></span>
<span data-ttu-id="cd861-163">有三個主要步驟將自訂欄位新增至每週時間輸入網格。</span><span class="sxs-lookup"><span data-stu-id="cd861-163">There are three main steps to adding a custom field to the weekly time entry grid.</span></span>

1. <span data-ttu-id="cd861-164">將自訂欄位新增至 [快速建立] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cd861-164">Add the custom field to the quick create dialog box.</span></span>
2. <span data-ttu-id="cd861-165">設定網格以顯示自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="cd861-165">Configure the grid to show the custom field.</span></span>
3. <span data-ttu-id="cd861-166">將自訂欄位新增至列編輯工作流程或儲存格編輯工作流程。</span><span class="sxs-lookup"><span data-stu-id="cd861-166">Add the custom field to the row edit task flow or the cell edit task flow.</span></span>

<span data-ttu-id="cd861-167">請確定新欄位在列或儲存格編輯工作流程中有必要的驗證。</span><span class="sxs-lookup"><span data-stu-id="cd861-167">Make sure that the new field has the required validations in the row or cell edit task flow.</span></span> <span data-ttu-id="cd861-168">在此步驟中，請根據時間項目狀態鎖定欄位。</span><span class="sxs-lookup"><span data-stu-id="cd861-168">As part of this step, lock the field based on the time entry status.</span></span>

### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a><span data-ttu-id="cd861-169">將自訂欄位新增至 [快速建立] 對話方塊</span><span class="sxs-lookup"><span data-stu-id="cd861-169">Add the custom field to the quick create dialog box</span></span>
<span data-ttu-id="cd861-170">將自訂欄位新增至 **時間項目快速建立** 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="cd861-170">Add the custom field to the **Create Time Entry Quick Create** dialog box.</span></span> <span data-ttu-id="cd861-171">然後在新增時間項目時，就可以選取 **新增** 來輸入值。</span><span class="sxs-lookup"><span data-stu-id="cd861-171">Then, when time entries are added, a value can be entered by selecting **New**.</span></span>

### <a name="configure-the-grid-to-show-the-custom-field"></a><span data-ttu-id="cd861-172">設定網格以顯示自訂欄位</span><span class="sxs-lookup"><span data-stu-id="cd861-172">Configure the grid to show the custom field</span></span>
<span data-ttu-id="cd861-173">有兩個方法可以將自訂欄位新增至每週時間輸入網格：</span><span class="sxs-lookup"><span data-stu-id="cd861-173">There are two ways add a custom field to the weekly time entry grid:</span></span>

  - <span data-ttu-id="cd861-174">自訂檢視表並新增自訂欄位</span><span class="sxs-lookup"><span data-stu-id="cd861-174">Customize a view and add a custom field</span></span>
  - <span data-ttu-id="cd861-175">建立新的預設自訂時間項目</span><span class="sxs-lookup"><span data-stu-id="cd861-175">Create a new default custom time entry</span></span> 


#### <a name="customize-a-view-and-add-a-custom-field"></a><span data-ttu-id="cd861-176">自訂檢視表並新增自訂欄位</span><span class="sxs-lookup"><span data-stu-id="cd861-176">Customize a view and add a custom field</span></span>

<span data-ttu-id="cd861-177">自訂 **我的每週時間項目** 檢視表，並將自訂欄位新增至其中。</span><span class="sxs-lookup"><span data-stu-id="cd861-177">Customize the **My Weekly Time Entries** view and add the custom field to it.</span></span> <span data-ttu-id="cd861-178">您可以編輯檢視表中的屬性，以選擇網格中自訂欄位的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="cd861-178">You can choose the position and size of the custom field in the grid by editing the properties in the view.</span></span>

#### <a name="create-a-new-default-custom-time-entry"></a><span data-ttu-id="cd861-179">建立新的預設自訂時間項目</span><span class="sxs-lookup"><span data-stu-id="cd861-179">Create a new default custom time entry</span></span>

<span data-ttu-id="cd861-180">除了您要包含在網格中的欄之外，此檢視表應也包含 **描述** 及 **外部註解** 欄位。</span><span class="sxs-lookup"><span data-stu-id="cd861-180">This view should contain the **Description** and **External Comments** fields, in addition to the columns that you want to have in the grid.</span></span> 

1. <span data-ttu-id="cd861-181">在檢視表中編輯這些屬性，以選擇網格的位置、大小和預設排序順序。</span><span class="sxs-lookup"><span data-stu-id="cd861-181">Choose the position, size, and default sort order of the grid by editing those properties in the view.</span></span> 
2. <span data-ttu-id="cd861-182">設定此檢視表的自訂控制項，使其成為 **時間項目網格** 控制項。</span><span class="sxs-lookup"><span data-stu-id="cd861-182">Configure the custom control for this view so that it's a **Time Entry Grid** control.</span></span> 
3. <span data-ttu-id="cd861-183">將此控制項新增至檢視表，然後選取該控制項以用於網頁、手機及平板電腦。</span><span class="sxs-lookup"><span data-stu-id="cd861-183">Add this control to the view, and select it for web, phone, and tablet.</span></span> 
4. <span data-ttu-id="cd861-184">設定每週時間項目網格的參數。</span><span class="sxs-lookup"><span data-stu-id="cd861-184">Configure the parameters for the weekly time entry grid.</span></span> 
5. <span data-ttu-id="cd861-185">將 **開始日期** 欄位設定為 **msdyn_date** 、將 **期間** 欄位設定為 **msdyn_duration** ，以及並將 **狀態** 欄位設定為 **msdyn_entrystatus** 。</span><span class="sxs-lookup"><span data-stu-id="cd861-185">Set the **Start Date** field to **msdyn_date** , set the **Duration** field to **msdyn_duration** , and set the **Status** field to **msdyn_entrystatus**.</span></span> 
6. <span data-ttu-id="cd861-186">在預設檢視表中， **唯讀狀態清單** 欄位會設定為 **192350002,192350003,192350004** 。</span><span class="sxs-lookup"><span data-stu-id="cd861-186">For the default view, the **Read-only Status List** field is set to **192350002,192350003,192350004**.</span></span> <span data-ttu-id="cd861-187">**列編輯工作流程** 欄位設定為 **msdyn_timeentryrowedit** 。</span><span class="sxs-lookup"><span data-stu-id="cd861-187">The **Row Edit Task Flow** field is set to **msdyn_timeentryrowedit**.</span></span> <span data-ttu-id="cd861-188">**儲存格編輯工作流程** 欄位設定為 **msdyn_timeentryedit** 。</span><span class="sxs-lookup"><span data-stu-id="cd861-188">The **Cell Edit Task Flow** field is set to **msdyn_timeentryedit**.</span></span> 
7. <span data-ttu-id="cd861-189">您可以自訂這些欄位以新增或移除唯讀狀態，或是使用不同的工作型體驗 (TBX) 進行列或儲存格編輯。</span><span class="sxs-lookup"><span data-stu-id="cd861-189">You can customize these fields to add or remove read-only status, or to use a different task-based experience (TBX) for row or cell editing.</span></span> <span data-ttu-id="cd861-190">這些欄位現已繫結至靜態值。</span><span class="sxs-lookup"><span data-stu-id="cd861-190">These fields are now bound to a static value.</span></span>


> [!NOTE] 
> <span data-ttu-id="cd861-191">這兩個選項都會移除 **專案** 與 **專案工作** 實體的一些現成可用篩選，讓實體的所有查詢檢視表都能看得到。</span><span class="sxs-lookup"><span data-stu-id="cd861-191">Both options will remove some out-of-box filtering on the **Project** and **Project Task** entities so that all lookup views for the entities will be visible.</span></span> <span data-ttu-id="cd861-192">在預設情況下，只會顯示相關的查詢檢視表。</span><span class="sxs-lookup"><span data-stu-id="cd861-192">Out-of-the-box, only the relevant lookup views are visible.</span></span>

<span data-ttu-id="cd861-193">判斷自訂欄位適用的工作流程。</span><span class="sxs-lookup"><span data-stu-id="cd861-193">Determine the appropriate task flow for the custom field.</span></span> <span data-ttu-id="cd861-194">如果您將欄位新增至網格，則該欄位應該會移至用於套用至整列時間項目之欄位的列編輯工作流程。</span><span class="sxs-lookup"><span data-stu-id="cd861-194">If you added the field to the grid, it should go in the row edit task flow that is used for fields that apply to the whole row of time entries.</span></span> <span data-ttu-id="cd861-195">如果自訂欄位每天都會有唯一值 (例如 **結束時間** 的自訂欄位)，則應進入儲存格編輯工作流程。</span><span class="sxs-lookup"><span data-stu-id="cd861-195">If the custom field has a unique value every day, such as a custom field for **End time** , it should go in the cell edit task flow.</span></span>

<span data-ttu-id="cd861-196">若要將自訂欄位新增至工作流程，請將 **欄位** 元素拖曳至頁面的適當位置，然後設定欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="cd861-196">To add the custom field to a task flow, drag a **Field** element into the appropriate position on the page, and then set the field properties.</span></span> <span data-ttu-id="cd861-197">將 **來源** 屬性設定為 **時間項目** ，並將 **資料欄位** 屬性設定為自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="cd861-197">Set the **Source** property to **Time Entry** , and set the **Data Field** property to the custom field.</span></span> <span data-ttu-id="cd861-198">**欄位** 屬性會指定在 TBX 頁面上的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="cd861-198">The **Field** property specifies the display name on the TBX page.</span></span> <span data-ttu-id="cd861-199">選取 **套用** 儲存對欄位的變更，然後選取 **更新** 以儲存對頁面的變更。</span><span class="sxs-lookup"><span data-stu-id="cd861-199">Select **Apply** to save your changes to the field, and then select **Update** to save your changes to the page.</span></span>

<span data-ttu-id="cd861-200">若要改用新的自訂 TBX 頁面，請建立新的程序。</span><span class="sxs-lookup"><span data-stu-id="cd861-200">To use a new custom TBX page instead, create a new process.</span></span> <span data-ttu-id="cd861-201">將類別設定為 **商務程序流程** 、將實體設定為 **時間項目** ，以及將商務程序類型設定為 **以工作流程方式執行程序** 。</span><span class="sxs-lookup"><span data-stu-id="cd861-201">Set the category to **Business Process Flow** , set the entity to **Time Entry** , and set the business process type to **Run process as a task flow**.</span></span> <span data-ttu-id="cd861-202">在 **屬性** 底下， **頁面名稱** 屬性應設定為頁面的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="cd861-202">Under **Properties** , the **Page name** property should be set to the display name for the page.</span></span> <span data-ttu-id="cd861-203">將所有相關欄位新增至 TBX 頁面。</span><span class="sxs-lookup"><span data-stu-id="cd861-203">Add all the relevant fields to the TBX page.</span></span> <span data-ttu-id="cd861-204">儲存並啟用此程序。</span><span class="sxs-lookup"><span data-stu-id="cd861-204">Save and activate the process.</span></span> <span data-ttu-id="cd861-205">將相關工作流程的自訂控制項屬性更新為程序中的 **名稱** 值。</span><span class="sxs-lookup"><span data-stu-id="cd861-205">Update the custom control property for the relevant task flow to the value of **Name** on the process.</span></span>

### <a name="add-new-option-set-values"></a><span data-ttu-id="cd861-206">新增選項組值</span><span class="sxs-lookup"><span data-stu-id="cd861-206">Add new option set values</span></span>
<span data-ttu-id="cd861-207">若要將選項組值新增至現成可用欄位，請開啟欄位的編輯頁面，然後在 **類型** 底下選取選項組旁邊的 **編輯** 。</span><span class="sxs-lookup"><span data-stu-id="cd861-207">To add option set values to an out-of-the-box field, open the editing page for the field, and under **Type** , select **Edit** next to the option set.</span></span> <span data-ttu-id="cd861-208">新增具有自訂標籤與色彩的新選項。</span><span class="sxs-lookup"><span data-stu-id="cd861-208">Add a new option that has a custom label and color.</span></span> <span data-ttu-id="cd861-209">如果您想要加入新的時間項目狀態，請將現成可用欄位命名為 **項目狀態** ，而不是 **狀態** 。</span><span class="sxs-lookup"><span data-stu-id="cd861-209">If you want to add a new time entry status, the out-of-the-box field is named **Entry Status** , not **Status**.</span></span>

### <a name="designate-a-new-time-entry-status-as-read-only"></a><span data-ttu-id="cd861-210">將新的時間項目狀態指定為唯讀</span><span class="sxs-lookup"><span data-stu-id="cd861-210">Designate a new time entry status as read-only</span></span>
<span data-ttu-id="cd861-211">若要將新的時間項目狀態指定為唯讀，請將新的時間項目值新增至 **唯讀狀態清單** 屬性。</span><span class="sxs-lookup"><span data-stu-id="cd861-211">To designate a new time entry status as read-only, add the new time entry value to the **Read-only Status List** property.</span></span> <span data-ttu-id="cd861-212">將會針對有新狀態的列，鎖定其時間輸入網格的可編輯部分。</span><span class="sxs-lookup"><span data-stu-id="cd861-212">The editable part of the time entry grid will be locked for rows that have the new status.</span></span>
<span data-ttu-id="cd861-213">接下來，新增商務規則以鎖定 **時間項目列編輯** 和 **時間項目編輯** TBX 頁面上的所有欄位。</span><span class="sxs-lookup"><span data-stu-id="cd861-213">Next, add business rules to lock all the fields on the **Time Entry Row Edit** and **Time Entry Edit** TBX pages.</span></span> <span data-ttu-id="cd861-214">您可以開啟頁面的商務程序流程編輯器，然後選取 **商務規則** 來存取這些頁面的商務規則。</span><span class="sxs-lookup"><span data-stu-id="cd861-214">You can access the business rules for these pages by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="cd861-215">您可以將新狀態新增至現有商務規則中的條件，也可以為新狀態新增商務規則。</span><span class="sxs-lookup"><span data-stu-id="cd861-215">You can add the new status to the condition in the existing business rules, or you can add a new business rule for the new status.</span></span>

### <a name="add-custom-validation-rules"></a><span data-ttu-id="cd861-216">新增自訂驗證規則</span><span class="sxs-lookup"><span data-stu-id="cd861-216">Add custom validation rules</span></span>
<span data-ttu-id="cd861-217">您有兩個可以為每週時間項目網格體驗新增的驗證規則類型：</span><span class="sxs-lookup"><span data-stu-id="cd861-217">There are two types of validation rules that you can add for the weekly time entry grid experience:</span></span>

- <span data-ttu-id="cd861-218">可在快速建立對話方塊和 TBX 頁面上使用的用戶端商務規則。</span><span class="sxs-lookup"><span data-stu-id="cd861-218">Client-side business rules that work in quick create dialog boxes and on TBX pages.</span></span>
- <span data-ttu-id="cd861-219">適用於所有時間項目更新的伺服器端外掛程式驗證。</span><span class="sxs-lookup"><span data-stu-id="cd861-219">Server-side plug-in validations that apply to all time entry updates.</span></span>

#### <a name="business-rules"></a><span data-ttu-id="cd861-220">商務規則</span><span class="sxs-lookup"><span data-stu-id="cd861-220">Business rules</span></span>
<span data-ttu-id="cd861-221">使用商務規則鎖定和解除鎖定欄位、在欄位中輸入預設值，然後定義驗證，要求資訊只能來自目前時間項目記錄。</span><span class="sxs-lookup"><span data-stu-id="cd861-221">Use business rules to lock and unlock fields, enter default values in fields, and define validations that require information only from the current time entry record.</span></span> <span data-ttu-id="cd861-222">您可以開啟 TBX 頁面的商務程序流程編輯器，然後選取 **商務規則** 來存取此頁面的商務規則。</span><span class="sxs-lookup"><span data-stu-id="cd861-222">You can access the business rules for a TBX page by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="cd861-223">您可以接著編輯現有的商務規則，或新增商務規則。</span><span class="sxs-lookup"><span data-stu-id="cd861-223">You can then edit the existing business rules or add a new business rule.</span></span> <span data-ttu-id="cd861-224">如果還要更多的自訂驗證，您可以使用商務規則來執行 JavaScript。</span><span class="sxs-lookup"><span data-stu-id="cd861-224">For even more customized validations, you can use a business rule to run JavaScript.</span></span>

#### <a name="plug-in-validations"></a><span data-ttu-id="cd861-225">外掛程式驗證</span><span class="sxs-lookup"><span data-stu-id="cd861-225">Plug-in validations</span></span>
<span data-ttu-id="cd861-226">對於任何需要內容超過單一時間項目記錄所能提供範圍的驗證，或是對於任何要在網格中對內嵌更新執行的驗證，請使用外掛程式驗證。</span><span class="sxs-lookup"><span data-stu-id="cd861-226">Use plug-in validations for any validations that require more context than is available in a single time entry record, or for any validations that you want to run on inline updates in the grid.</span></span> <span data-ttu-id="cd861-227">若要完成驗證，請在 **時間項目** 實體上建立自訂外掛程式。</span><span class="sxs-lookup"><span data-stu-id="cd861-227">To complete the validation, create a custom plug-in on the **Time Entry** entity.</span></span>

### <a name="copying-time-entries"></a><span data-ttu-id="cd861-228">複製時間項目</span><span class="sxs-lookup"><span data-stu-id="cd861-228">Copying time entries</span></span>
<span data-ttu-id="cd861-229">使用 **複製時間項目欄** 檢視表來定義要在時間輸入期間複製的欄位清單。</span><span class="sxs-lookup"><span data-stu-id="cd861-229">Use the view **Copy Time Entry Columns** to define the list of fields to copy during time entry.</span></span> <span data-ttu-id="cd861-230">**日期** 和 **期間** 是必要欄位，不可從檢視表移除。</span><span class="sxs-lookup"><span data-stu-id="cd861-230">**Date** and **Duration** are required fields and shouldn't be removed from the view.</span></span>
