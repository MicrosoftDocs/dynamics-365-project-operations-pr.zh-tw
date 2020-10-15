---
title: 擴充時間項目
description: 本主題提供有關開發人員如何擴充時間項目控制項的資訊。
author: stsporen
manager: Annbe
ms.date: 10/01/2020
ms.topic: article
ms.service: dynamics-365-customerservice
ms.reviewer: kfend
ms.author: stsporen
ms.openlocfilehash: 93f411ad7c86beefcc35e7799a03987dacdcd62b
ms.sourcegitcommit: 5a29adce48133e09f051929e8544d6c2c93c025d
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/02/2020
ms.locfileid: "3930870"
---
# <a name="extending-time-entries"></a><span data-ttu-id="a90d2-103">擴充時間項目</span><span class="sxs-lookup"><span data-stu-id="a90d2-103">Extending time entries</span></span>

<span data-ttu-id="a90d2-104">_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_</span><span class="sxs-lookup"><span data-stu-id="a90d2-104">_**Applies To:** Project Operations for resource/non-stocked based scenarios, Lite deployment - deal to proforma invoicing_</span></span>

<span data-ttu-id="a90d2-105">Dynamics 365 Project Operations 包含可擴充的時間項目自訂控制項。</span><span class="sxs-lookup"><span data-stu-id="a90d2-105">Dynamics 365 Project Operations includes an extendable time entry custom control.</span></span> <span data-ttu-id="a90d2-106">此控制項包含下列功能：</span><span class="sxs-lookup"><span data-stu-id="a90d2-106">This control includes the following features:</span></span>

- <span data-ttu-id="a90d2-107">輸入橫跨一週的時間</span><span class="sxs-lookup"><span data-stu-id="a90d2-107">Enter time horizontally over a week</span></span>
- <span data-ttu-id="a90d2-108">依日、列或週的總計</span><span class="sxs-lookup"><span data-stu-id="a90d2-108">Totals by day, row, or week</span></span>
- <span data-ttu-id="a90d2-109">複製列或週</span><span class="sxs-lookup"><span data-stu-id="a90d2-109">Copy rows or weeks</span></span>
- <span data-ttu-id="a90d2-110">透過 HH:mm 或 HH.hh (自動轉換為 HH.hh) 輸入的時間項目</span><span class="sxs-lookup"><span data-stu-id="a90d2-110">Time entry through HH:mm or HH.hh (automatically converts to HH.hh)</span></span>
- <span data-ttu-id="a90d2-111">從指派、預約或約會匯入</span><span class="sxs-lookup"><span data-stu-id="a90d2-111">Import from assignments, bookings or appointments</span></span>

<span data-ttu-id="a90d2-112">時間項目可在兩個區域中進行擴充：</span><span class="sxs-lookup"><span data-stu-id="a90d2-112">Extending time entries is possible in two areas:</span></span>
- [<span data-ttu-id="a90d2-113">新增自訂時間項目供自己使用</span><span class="sxs-lookup"><span data-stu-id="a90d2-113">Add custom time entries for your own use</span></span>](#add)
- [<span data-ttu-id="a90d2-114">自訂每週時間項目控制項</span><span class="sxs-lookup"><span data-stu-id="a90d2-114">Customize the weekly Time Entry control</span></span>](#customize)

## <a name="add-custom-time-entries-for-your-own-use"></a><a name="add"></a><span data-ttu-id="a90d2-115">新增自訂時間項目供自己使用。</span><span class="sxs-lookup"><span data-stu-id="a90d2-115">Add custom time entries for your own use.</span></span>

<span data-ttu-id="a90d2-116">時間項目是設計要用於多個案例的核心實體。</span><span class="sxs-lookup"><span data-stu-id="a90d2-116">Time entries are a core entity that is designed to be used for multiple scenarios.</span></span> <span data-ttu-id="a90d2-117">在 2020 年 4 月第 1 段浪潮中，推出了提供**設定**實體和**時間項目使用者**資訊安全角色的 TESA 核心解決方案。</span><span class="sxs-lookup"><span data-stu-id="a90d2-117">In April Wave 1 2020, the TESA core solution was introduced, which provides a **Settings** entity and a new **Time Entry User** security role.</span></span> <span data-ttu-id="a90d2-118">其中也包含與 **msdyn_duration** 有直接關聯的新欄位 **msdyn_start** 和 **msdyn_end**。</span><span class="sxs-lookup"><span data-stu-id="a90d2-118">The new fields, **msdyn_start** and **msdyn_end** which have a direct relation to **msdyn_duration**, were also included.</span></span> <span data-ttu-id="a90d2-119">新的實體、資訊安全角色及欄位讓您有更統一的方法可以跨多個產品處理時間。</span><span class="sxs-lookup"><span data-stu-id="a90d2-119">The new entity, security role, and fields allow for a more unified approach to time across multiple products.</span></span>


### <a name="time-source-entity"></a><span data-ttu-id="a90d2-120">時間來源實體</span><span class="sxs-lookup"><span data-stu-id="a90d2-120">Time Source Entity</span></span>
| <span data-ttu-id="a90d2-121">欄位</span><span class="sxs-lookup"><span data-stu-id="a90d2-121">Field</span></span> | <span data-ttu-id="a90d2-122">描述</span><span class="sxs-lookup"><span data-stu-id="a90d2-122">Description</span></span> | 
|-------|------------|
| <span data-ttu-id="a90d2-123">名字</span><span class="sxs-lookup"><span data-stu-id="a90d2-123">Name</span></span>  | <span data-ttu-id="a90d2-124">時間來源實體的名稱，在建立時間項目過程中用作選取值。</span><span class="sxs-lookup"><span data-stu-id="a90d2-124">The name of the Time Source entry used as the selection value during time entry creation.</span></span> |
| <span data-ttu-id="a90d2-125">預設時間來源 [時間來源：isdefault]</span><span class="sxs-lookup"><span data-stu-id="a90d2-125">Default Time Source [Time Source: isdefault]</span></span> | <span data-ttu-id="a90d2-126">根據預設，在預設時間來源上只能標示一個時間來源。</span><span class="sxs-lookup"><span data-stu-id="a90d2-126">By default, only one Time Source may be marked at the default time source.</span></span> <span data-ttu-id="a90d2-127">此功能允許輸入項目預設為時間來源 (如果未指定的話)。</span><span class="sxs-lookup"><span data-stu-id="a90d2-127">This capability allows for entries to default to a time source if one isn't specified.</span></span> |
|<span data-ttu-id="a90d2-128">時間來源類型 [時間來源：sourcetype]</span><span class="sxs-lookup"><span data-stu-id="a90d2-128">Time Source Type [Time Source: sourcetype]</span></span> | <span data-ttu-id="a90d2-129">來源類型是允許將時間來源關聯至應用程式的選項 (時間項目來源類型)。</span><span class="sxs-lookup"><span data-stu-id="a90d2-129">The source type is an option (Time Entry Source Type) that allows for the association of the time source to an app.</span></span> <span data-ttu-id="a90d2-130">新增其他的應用程式時，其他值將會新增至此選項組。</span><span class="sxs-lookup"><span data-stu-id="a90d2-130">Additional values will be added to this option set as additional applications are added.</span></span> <span data-ttu-id="a90d2-131">請注意，Microsoft 會保留大於 190,000,000 的值。</span><span class="sxs-lookup"><span data-stu-id="a90d2-131">Note that Microsoft reserves values greater than 190,000,000.</span></span>|


### <a name="time-entries-and-the-time-source-entity"></a><span data-ttu-id="a90d2-132">時間項目和時間來源實體</span><span class="sxs-lookup"><span data-stu-id="a90d2-132">Time entries and the Time Source Entity</span></span>
<span data-ttu-id="a90d2-133">每個時間項目都會與時間來源記錄建立關聯。</span><span class="sxs-lookup"><span data-stu-id="a90d2-133">Each time entry is associated to a time source record.</span></span> <span data-ttu-id="a90d2-134">此記錄可決定應用程式應如何處理時間項目以及應由哪些應用程式來處理。</span><span class="sxs-lookup"><span data-stu-id="a90d2-134">This record determines how and which applications should process the time entry.</span></span>

<span data-ttu-id="a90d2-135">時間項目永遠都是一個已連結開始、結束及期間的時間連續區塊。</span><span class="sxs-lookup"><span data-stu-id="a90d2-135">Time entries are always one contiguous block of time with the start, end, and duration linked.</span></span>

<span data-ttu-id="a90d2-136">邏輯會自動在下列情況中更新時間項目記錄：</span><span class="sxs-lookup"><span data-stu-id="a90d2-136">The logic will automatically update the time entry record in the following situations:</span></span>

- <span data-ttu-id="a90d2-137">如果提供下列三個欄位中的兩個，則會自動計算第三個欄位</span><span class="sxs-lookup"><span data-stu-id="a90d2-137">If two of the three following fields are provided, the third is calculated automatically</span></span> 

    - <span data-ttu-id="a90d2-138">**msdyn_start**</span><span class="sxs-lookup"><span data-stu-id="a90d2-138">**msdyn_start**</span></span>
    - <span data-ttu-id="a90d2-139">**msdyn_end**</span><span class="sxs-lookup"><span data-stu-id="a90d2-139">**msdyn_end**</span></span>
    - <span data-ttu-id="a90d2-140">**msdyn_duration**</span><span class="sxs-lookup"><span data-stu-id="a90d2-140">**msdyn_duration**</span></span>

- <span data-ttu-id="a90d2-141">欄位 **msdyn_start** 和 **msdyn_end** 是時區感知欄位。</span><span class="sxs-lookup"><span data-stu-id="a90d2-141">The fields, **msdyn_start** and **msdyn_end** are timezone aware.</span></span>
- <span data-ttu-id="a90d2-142">只有指定 **msdyn_date** 和 **msdyn_duration** 所建立的時間項目將會從午夜開始，而 **msdyn_start** 和 **msdyn_end** 此會相應進行更新。</span><span class="sxs-lookup"><span data-stu-id="a90d2-142">Time entries created with only **msdyn_date** and **msdyn_duration** specified will start at midnight, and **msdyn_start** and **msdyn_end** will be updated accordingly.</span></span>

#### <a name="time-entry-types"></a><span data-ttu-id="a90d2-143">時間項目類型</span><span class="sxs-lookup"><span data-stu-id="a90d2-143">Time entry types</span></span>

<span data-ttu-id="a90d2-144">時間項目記錄的關聯類型會定義相關聯應用程式在提交流程中的行為。</span><span class="sxs-lookup"><span data-stu-id="a90d2-144">Time entry records have an associated type that defines behavior in the submission flow for the associated application.</span></span>

|<span data-ttu-id="a90d2-145">標籤</span><span class="sxs-lookup"><span data-stu-id="a90d2-145">Label</span></span> | <span data-ttu-id="a90d2-146">值</span><span class="sxs-lookup"><span data-stu-id="a90d2-146">Value</span></span>|
|-----|-----|
|<span data-ttu-id="a90d2-147">休息</span><span class="sxs-lookup"><span data-stu-id="a90d2-147">On break</span></span>   |<span data-ttu-id="a90d2-148">192,355,000</span><span class="sxs-lookup"><span data-stu-id="a90d2-148">192,355,000</span></span>|
|<span data-ttu-id="a90d2-149">差旅</span><span class="sxs-lookup"><span data-stu-id="a90d2-149">Travel</span></span> | <span data-ttu-id="a90d2-150">192,355,001</span><span class="sxs-lookup"><span data-stu-id="a90d2-150">192,355,001</span></span>|
|<span data-ttu-id="a90d2-151">加班時間</span><span class="sxs-lookup"><span data-stu-id="a90d2-151">Overtime</span></span>   | <span data-ttu-id="a90d2-152">192,354,320</span><span class="sxs-lookup"><span data-stu-id="a90d2-152">192,354,320</span></span>|
|<span data-ttu-id="a90d2-153">工作</span><span class="sxs-lookup"><span data-stu-id="a90d2-153">Work</span></span>   | <span data-ttu-id="a90d2-154">192,350,000</span><span class="sxs-lookup"><span data-stu-id="a90d2-154">192,350,000</span></span>|
|<span data-ttu-id="a90d2-155">缺席</span><span class="sxs-lookup"><span data-stu-id="a90d2-155">Absence</span></span>    | <span data-ttu-id="a90d2-156">192,350,001</span><span class="sxs-lookup"><span data-stu-id="a90d2-156">192,350,001</span></span>|
|<span data-ttu-id="a90d2-157">休假</span><span class="sxs-lookup"><span data-stu-id="a90d2-157">Vacation</span></span>   | <span data-ttu-id="a90d2-158">192,350,002</span><span class="sxs-lookup"><span data-stu-id="a90d2-158">192,350,002</span></span>|



## <a name="customize-the-weekly-time-entry-control"></a><a name="customize"></a><span data-ttu-id="a90d2-159">自訂每週時間項目控制項</span><span class="sxs-lookup"><span data-stu-id="a90d2-159">Customize the weekly Time Entry control</span></span>
<span data-ttu-id="a90d2-160">開發人員可以將額外的欄位和查詢新增至其他實體，並實作自訂商務規則以支援其業務案例。</span><span class="sxs-lookup"><span data-stu-id="a90d2-160">Developers can add additional fields and lookups to other entities, and implement custom business rules to support their business scenarios.</span></span>

### <a name="add-custom-fields-with-lookups-to-other-entities"></a><span data-ttu-id="a90d2-161">新增具有其他實體查詢的自訂欄位</span><span class="sxs-lookup"><span data-stu-id="a90d2-161">Add custom fields with lookups to other entities</span></span>
<span data-ttu-id="a90d2-162">有三個主要步驟將自訂欄位新增至每週時間輸入網格。</span><span class="sxs-lookup"><span data-stu-id="a90d2-162">There are three main steps to adding a custom field to the weekly time entry grid.</span></span>

- <span data-ttu-id="a90d2-163">將自訂欄位新增至 [快速建立] 對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a90d2-163">Add the custom field to the quick create dialog box.</span></span>
- <span data-ttu-id="a90d2-164">設定網格以顯示自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="a90d2-164">Configure the grid to show the custom field.</span></span>
- <span data-ttu-id="a90d2-165">將自訂欄位新增至列編輯工作流程或儲存格編輯工作流程。</span><span class="sxs-lookup"><span data-stu-id="a90d2-165">Add the custom field to either the row edit task flow or the cell edit task flow.</span></span>

<span data-ttu-id="a90d2-166">您也必須確定新欄位在列或儲存格編輯工作流程中有必要的驗證。</span><span class="sxs-lookup"><span data-stu-id="a90d2-166">You must also make sure that the new field has the required validations in the row or cell edit task flow.</span></span> <span data-ttu-id="a90d2-167">在此步驟中，您必須根據時間項目狀態鎖定欄位。</span><span class="sxs-lookup"><span data-stu-id="a90d2-167">As part of this step, you must lock the field based on the time entry status.</span></span>

#### <a name="add-the-custom-field-to-the-quick-create-dialog-box"></a><span data-ttu-id="a90d2-168">將自訂欄位新增至 [快速建立] 對話方塊</span><span class="sxs-lookup"><span data-stu-id="a90d2-168">Add the custom field to the quick create dialog box</span></span>
<span data-ttu-id="a90d2-169">您必須將自訂欄位新增至**時間項目快速建立**對話方塊。</span><span class="sxs-lookup"><span data-stu-id="a90d2-169">You must add the custom field to the **Create Time Entry Quick Create** dialog box.</span></span> <span data-ttu-id="a90d2-170">使用者可以接著在新增時間項目時，選取**新增**來輸入值。</span><span class="sxs-lookup"><span data-stu-id="a90d2-170">Users can then enter a value when they add time entries by selecting **New**.</span></span>

#### <a name="configure-the-grid-to-show-the-custom-field"></a><span data-ttu-id="a90d2-171">設定網格以顯示自訂欄位</span><span class="sxs-lookup"><span data-stu-id="a90d2-171">Configure the grid to show the custom field</span></span>
<span data-ttu-id="a90d2-172">有兩個方法可以將自訂欄位新增至每週時間輸入網格：</span><span class="sxs-lookup"><span data-stu-id="a90d2-172">There are two ways add a custom field to the weekly time entry grid:</span></span>

  - <span data-ttu-id="a90d2-173">自訂檢視表並新增自訂欄位</span><span class="sxs-lookup"><span data-stu-id="a90d2-173">Customize a view and add a custom field</span></span>
  - <span data-ttu-id="a90d2-174">建立新的預設自訂時間項目</span><span class="sxs-lookup"><span data-stu-id="a90d2-174">Create a new default custom time entry</span></span> 


<span data-ttu-id="a90d2-175">**自訂檢視表並新增自訂欄位**</span><span class="sxs-lookup"><span data-stu-id="a90d2-175">**Customize a view and add a custom field**</span></span>

<span data-ttu-id="a90d2-176">您可以自訂**我的每週時間項目**檢視表，並將自訂欄位新增至其中。</span><span class="sxs-lookup"><span data-stu-id="a90d2-176">You can customize the **My Weekly Time Entries** view and add the custom field to it.</span></span> <span data-ttu-id="a90d2-177">您可以在檢視表中編輯這些屬性，以選擇網格中自訂欄位的位置和大小。</span><span class="sxs-lookup"><span data-stu-id="a90d2-177">You can choose the position and size of the custom field in the grid by editing those properties in the view.</span></span>

<span data-ttu-id="a90d2-178">**建立新的預設自訂時間項目**</span><span class="sxs-lookup"><span data-stu-id="a90d2-178">**Create a new default custom time entry**</span></span> 

<span data-ttu-id="a90d2-179">除了您要包含在網格中的欄之外，此檢視表應也包含**描述**及**外部註解**欄位。</span><span class="sxs-lookup"><span data-stu-id="a90d2-179">This view should contain the **Description** and **External Comments** fields, in addition to the columns that you want to have in the grid.</span></span> 

1. <span data-ttu-id="a90d2-180">在檢視表中編輯這些屬性，以選擇網格的位置、大小和預設排序順序。</span><span class="sxs-lookup"><span data-stu-id="a90d2-180">Choose the position, size, and default sort order of the grid by editing those properties in the view.</span></span> 
2. <span data-ttu-id="a90d2-181">設定此檢視表的自訂控制項，使其成為**時間項目網格**控制項。</span><span class="sxs-lookup"><span data-stu-id="a90d2-181">Configure the custom control for this view so that it's a **Time Entry Grid** control.</span></span> 
3. <span data-ttu-id="a90d2-182">將此控制項新增至檢視表，然後選取該控制項以用於網頁、手機及平板電腦。</span><span class="sxs-lookup"><span data-stu-id="a90d2-182">Add this control to the view, and select it for web, phone, and tablet.</span></span> 
4. <span data-ttu-id="a90d2-183">設定每週時間項目網格的參數。</span><span class="sxs-lookup"><span data-stu-id="a90d2-183">Configure the parameters for the weekly time entry grid.</span></span> <span data-ttu-id="a90d2-184">將**開始日期**欄位設定為 **msdyn_date**、將**期間**欄位設定為 **msdyn_duration**，以及並將**狀態**欄位設定為 **msdyn_entrystatus**。</span><span class="sxs-lookup"><span data-stu-id="a90d2-184">Set the **Start Date** field to **msdyn_date**, set the **Duration** field to **msdyn_duration**, and set the **Status** field to **msdyn_entrystatus**.</span></span> 
5. <span data-ttu-id="a90d2-185">在預設檢視表中，**唯讀狀態清單**欄位設定為 **192350002,192350003,192350004**、**列編輯工作流程**欄位設定為 **msdyn_timeentryrowedit**，以及**儲存格編輯工作流程**欄位已設定為 **msdyn_timeentryedit**。</span><span class="sxs-lookup"><span data-stu-id="a90d2-185">For the default view, the **Read-only Status List** field is set to **192350002,192350003,192350004**, the **Row Edit Task Flow** field is set to **msdyn_timeentryrowedit**, and the **Cell Edit Task Flow** field is set to **msdyn_timeentryedit**.</span></span> 
6. <span data-ttu-id="a90d2-186">您可以自訂這些欄位以新增或移除唯讀狀態，或是使用不同的工作型體驗 (TBX) 進行列或儲存格編輯。</span><span class="sxs-lookup"><span data-stu-id="a90d2-186">You can customize these fields to add or remove read-only status, or to use a different task-based experience (TBX) for row or cell editing.</span></span> <span data-ttu-id="a90d2-187">這些欄位應繫結至靜態值。</span><span class="sxs-lookup"><span data-stu-id="a90d2-187">These fields should be bound to a static value.</span></span>


> [!NOTE] 
> <span data-ttu-id="a90d2-188">這兩個選項都會移除**專案**與**專案工作**實體的一些預設的篩選，讓實體的所有查詢檢視表都能看得到。</span><span class="sxs-lookup"><span data-stu-id="a90d2-188">Both options will remove some out-of-box filtering on **Project** and **Project Task** entities so that all lookup views for the entities will be visible.</span></span> <span data-ttu-id="a90d2-189">在預設情況下，只會顯示相關的查詢檢視表。</span><span class="sxs-lookup"><span data-stu-id="a90d2-189">Out-of-the-box, only the relevant lookup views are visible.</span></span>
<span data-ttu-id="a90d2-190">您必須為自訂欄位判斷適當的工作流程。</span><span class="sxs-lookup"><span data-stu-id="a90d2-190">You must determine the appropriate task flow for the custom field.</span></span> <span data-ttu-id="a90d2-191">最可能的一點是，如果您將欄位新增至網格，則該欄位應該會移至用於套用至整列時間項目之欄位的列編輯工作流程。</span><span class="sxs-lookup"><span data-stu-id="a90d2-191">Most likely, if you added the field to the grid, it should go in the row edit task flow that is used for fields that apply to the whole row of time entries.</span></span> <span data-ttu-id="a90d2-192">如果自訂欄位每天都會有唯一值 (例如**結束時間**的自訂欄位)，則應進入儲存格編輯工作流程。</span><span class="sxs-lookup"><span data-stu-id="a90d2-192">If the custom field has a unique value every day, such as a custom field for **End time**, it should go in the cell edit task flow.</span></span>

<span data-ttu-id="a90d2-193">若要將自訂欄位新增至工作流程，請將**欄位**元素拖曳至頁面的適當位置，然後設定欄位屬性。</span><span class="sxs-lookup"><span data-stu-id="a90d2-193">To add the custom field to a task flow, drag a **Field** element into the appropriate position on the page, and then set the field properties.</span></span> <span data-ttu-id="a90d2-194">將**來源**屬性設定為**時間項目**，並將**資料欄位**屬性設定為自訂欄位。</span><span class="sxs-lookup"><span data-stu-id="a90d2-194">Set the **Source** property to **Time Entry**, and set the **Data Field** property to the custom field.</span></span> <span data-ttu-id="a90d2-195">**欄位**屬性會指定在 TBX 頁面上的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a90d2-195">The **Field** property specifies the display name on the TBX page.</span></span> <span data-ttu-id="a90d2-196">選取**套用**儲存對欄位的變更，然後選取**更新**以儲存對頁面的變更。</span><span class="sxs-lookup"><span data-stu-id="a90d2-196">Select **Apply** to save your changes to the field, and then select **Update** to save your changes to the page.</span></span>

<span data-ttu-id="a90d2-197">若要改用新的自訂 TBX 頁面，請建立新的程序。</span><span class="sxs-lookup"><span data-stu-id="a90d2-197">To use a new custom TBX page instead, create a new process.</span></span> <span data-ttu-id="a90d2-198">將類別設定為**商務程序流程**、將實體設定為**時間項目**，以及將商務程序類型設定為**以工作流程方式執行程序**。</span><span class="sxs-lookup"><span data-stu-id="a90d2-198">Set the category to **Business Process Flow**, set the entity to **Time Entry**, and set the business process type to **Run process as a task flow**.</span></span> <span data-ttu-id="a90d2-199">在**屬性**底下，**頁面名稱**屬性應設定為頁面的顯示名稱。</span><span class="sxs-lookup"><span data-stu-id="a90d2-199">Under **Properties**, the **Page name** property should be set to the display name for the page.</span></span> <span data-ttu-id="a90d2-200">將所有相關欄位新增至 TBX 頁面。</span><span class="sxs-lookup"><span data-stu-id="a90d2-200">Add all the relevant fields to the TBX page.</span></span> <span data-ttu-id="a90d2-201">儲存並啟用程序，然後將相關工作流程的自訂控制項屬性更新為程序中的**名稱**值。</span><span class="sxs-lookup"><span data-stu-id="a90d2-201">Save and activate the process, and then update the custom control property for the relevant task flow to the value of **Name** on the process.</span></span>

### <a name="add-new-option-set-values"></a><span data-ttu-id="a90d2-202">新增選項組值</span><span class="sxs-lookup"><span data-stu-id="a90d2-202">Add new option set values</span></span>
<span data-ttu-id="a90d2-203">若要將選項組值新增至現成可用欄位，請開啟欄位的編輯頁面，然後在**類型**底下選取選項組旁邊的**編輯**。</span><span class="sxs-lookup"><span data-stu-id="a90d2-203">To add option set values to an out-of-box field, open the editing page for the field, and then, under **Type**, select **Edit** next to the option set.</span></span> <span data-ttu-id="a90d2-204">接下來，新增具有自訂標籤與色彩的新選項。</span><span class="sxs-lookup"><span data-stu-id="a90d2-204">Next, add a new option that has a custom label and color.</span></span> <span data-ttu-id="a90d2-205">如果您想要加入新的時間項目狀態，請將現成可用欄位命名為**項目狀態**，而不是**狀態**。</span><span class="sxs-lookup"><span data-stu-id="a90d2-205">If you want to add a new time entry status, the out-of-box field is named **Entry Status**, not **Status**.</span></span>

### <a name="designate-a-new-time-entry-status-as-read-only"></a><span data-ttu-id="a90d2-206">將新的時間項目狀態指定為唯讀</span><span class="sxs-lookup"><span data-stu-id="a90d2-206">Designate a new time entry status as read-only</span></span>
<span data-ttu-id="a90d2-207">若要將新的時間項目狀態指定為唯讀，請將新的時間項目值新增至**唯讀狀態清單**屬性。</span><span class="sxs-lookup"><span data-stu-id="a90d2-207">To designate a new time entry status as read-only, add the new time entry value to the **Read-only Status List** property.</span></span> <span data-ttu-id="a90d2-208">將會針對有新狀態的列，鎖定其時間輸入網格的可編輯部分。</span><span class="sxs-lookup"><span data-stu-id="a90d2-208">The editable part of the time entry grid will be locked for rows that have the new status.</span></span>
<span data-ttu-id="a90d2-209">接下來，新增商務規則以鎖定**時間項目列編輯**和**時間項目編輯** TBX 頁面上的所有欄位。</span><span class="sxs-lookup"><span data-stu-id="a90d2-209">Next, add business rules to lock all the fields on the **Time Entry Row Edit** and **Time Entry Edit** TBX pages.</span></span> <span data-ttu-id="a90d2-210">您可以開啟頁面的商務程序流程編輯器，然後選取**商務規則**來存取這些頁面的商務規則。</span><span class="sxs-lookup"><span data-stu-id="a90d2-210">You can access the business rules for these pages by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="a90d2-211">您可以將新狀態新增至現有商務規則中的條件，也可以為新狀態新增商務規則。</span><span class="sxs-lookup"><span data-stu-id="a90d2-211">You can add the new status to the condition in the existing business rules, or you can add a new business rule for the new status.</span></span>

### <a name="add-custom-validation-rules"></a><span data-ttu-id="a90d2-212">新增自訂驗證規則</span><span class="sxs-lookup"><span data-stu-id="a90d2-212">Add custom validation rules</span></span>
<span data-ttu-id="a90d2-213">您有兩個可以為每週時間項目網格體驗新增的驗證規則類型：</span><span class="sxs-lookup"><span data-stu-id="a90d2-213">There are two types of validation rules that you can add for the weekly time entry grid experience:</span></span>

- <span data-ttu-id="a90d2-214">可在快速建立對話方塊和 TBX 頁面上使用的用戶端商務規則。</span><span class="sxs-lookup"><span data-stu-id="a90d2-214">Client-side business rules that work in quick create dialog boxes and on TBX pages.</span></span>
- <span data-ttu-id="a90d2-215">適用於所有時間項目更新的伺服器端外掛程式驗證。</span><span class="sxs-lookup"><span data-stu-id="a90d2-215">Server-side plug-in validations that apply to all time entry updates.</span></span>

#### <a name="business-rules"></a><span data-ttu-id="a90d2-216">商務規則</span><span class="sxs-lookup"><span data-stu-id="a90d2-216">Business rules</span></span>
<span data-ttu-id="a90d2-217">使用商務規則鎖定和解除鎖定欄位、在欄位中輸入預設值，然後定義驗證，要求資訊只能來自目前時間項目記錄。</span><span class="sxs-lookup"><span data-stu-id="a90d2-217">Use business rules to lock and unlock fields, enter default values in fields, and define validations that require information only from the current time entry record.</span></span> <span data-ttu-id="a90d2-218">您可以開啟 TBX 頁面的商務程序流程編輯器，然後選取**商務規則**來存取此頁面的商務規則。</span><span class="sxs-lookup"><span data-stu-id="a90d2-218">You can access the business rules for a TBX page by opening the business process flow editor for the page and then selecting **Business Rules**.</span></span> <span data-ttu-id="a90d2-219">您可以接著編輯現有的商務規則，或新增商務規則。</span><span class="sxs-lookup"><span data-stu-id="a90d2-219">You can then edit the existing business rules or add a new business rule.</span></span> <span data-ttu-id="a90d2-220">如果還要更多的自訂驗證，您可以使用商務規則來執行 JavaScript。</span><span class="sxs-lookup"><span data-stu-id="a90d2-220">For even more customized validations, you can use a business rule to run JavaScript.</span></span>

#### <a name="plug-in-validations"></a><span data-ttu-id="a90d2-221">外掛程式驗證</span><span class="sxs-lookup"><span data-stu-id="a90d2-221">Plug-in validations</span></span>
<span data-ttu-id="a90d2-222">對於任何需要內容超過單一時間項目記錄所能提供範圍的驗證，或是對於任何要在網格中對內嵌更新執行的驗證，您應該使用外掛程式驗證。</span><span class="sxs-lookup"><span data-stu-id="a90d2-222">You should use plug-in validations for any validations that require more context than is available in a single time entry record, or for any validations that you want to run on inline updates in the grid.</span></span> <span data-ttu-id="a90d2-223">若要完成驗證，請在**時間項目**實體上建立自訂外掛程式。</span><span class="sxs-lookup"><span data-stu-id="a90d2-223">To complete the validation, create a custom plug-in on the **Time Entry** entity.</span></span>
