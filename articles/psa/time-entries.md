---
title: 建立時間項目
description: 此主題提供有關如何建立時間項目的資訊。
author: rumant
manager: kfend
ms.service: dynamics-365-customerservice
ms.custom:
- dyn365-projectservice
ms.date: 05/20/2019
ms.topic: article
ms.author: rumant
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 878413a24baa340b745a045a6991a63a00851c8b
ms.sourcegitcommit: 5c4c9bf3ba018562d6cb3443c01d550489c415fa
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 10/16/2020
ms.locfileid: "4073087"
---
# <a name="create-time-entries"></a><span data-ttu-id="c4f44-103">建立時間項目</span><span class="sxs-lookup"><span data-stu-id="c4f44-103">Create time entries</span></span>

[!INCLUDE[cc-applies-to-psa-app-3.x](../includes/cc-applies-to-psa-app-3x.md)]

<span data-ttu-id="c4f44-104">在舊版 Dynamics 365 Project Service Automation 中，時間項目是以週為單位輸入。</span><span class="sxs-lookup"><span data-stu-id="c4f44-104">In previous versions of Dynamics 365 Project Service Automation, time entries were entered on a weekly basis.</span></span> <span data-ttu-id="c4f44-105">在 Project Service Automation 版本 3 中，則按每日單位輸入時間項目。</span><span class="sxs-lookup"><span data-stu-id="c4f44-105">In version 3 of Project Service Automation, time entries are entered on a daily basis.</span></span> <span data-ttu-id="c4f44-106">不過，在建立幾個時間項目之後，您可以大量建立或複製這些項目。</span><span class="sxs-lookup"><span data-stu-id="c4f44-106">However, after a few time entries have been created, you can bulk create or copy them.</span></span>

## <a name="create-a-time-entry"></a><span data-ttu-id="c4f44-107">建立時間項目</span><span class="sxs-lookup"><span data-stu-id="c4f44-107">Create a time entry</span></span>

<span data-ttu-id="c4f44-108">依照下列步驟建立建立時間項目。</span><span class="sxs-lookup"><span data-stu-id="c4f44-108">Follow these steps to create a time entry.</span></span>

1. <span data-ttu-id="c4f44-109">在 **時間項目** 頁面，選取 **新增** 。</span><span class="sxs-lookup"><span data-stu-id="c4f44-109">On the **Time Entries** page, select **New**.</span></span>
2. <span data-ttu-id="c4f44-110">在 **快速建立：時間項目** 對話方塊中，以分鐘、小時或天為單位輸入時間項目的期間。</span><span class="sxs-lookup"><span data-stu-id="c4f44-110">In the **Quick Create: Time Entry** dialog box, enter the duration of the time entry in minutes, hours, or days.</span></span> <span data-ttu-id="c4f44-111">期間必須以下列格式來輸入： *x* 分鐘、 *x* 小時或 *x* 天。</span><span class="sxs-lookup"><span data-stu-id="c4f44-111">The duration must be entered in the following format: *x* minutes, *x* hours, or *x* days.</span></span> <span data-ttu-id="c4f44-112">時數和天數也可以輸入成小數值，例如 *x.x* 小時或 *x.x* 天。</span><span class="sxs-lookup"><span data-stu-id="c4f44-112">Hours and days can also be entered as decimal values, such as *x.x* hours or *x.x* days.</span></span>
3. <span data-ttu-id="c4f44-113">選取時間項目類型和您要輸入時間項目的專案。</span><span class="sxs-lookup"><span data-stu-id="c4f44-113">Select the type of time entry and the project that you're entering the time entry for.</span></span>
4. <span data-ttu-id="c4f44-114">在 **專案工作** 欄位中，尋找此時間項目的工作。</span><span class="sxs-lookup"><span data-stu-id="c4f44-114">In the **Project Task** field, find the task for this time entry.</span></span>

    > [!NOTE]
    > <span data-ttu-id="c4f44-115">如果您要為未指派給使用者的工作建立時間項目，請選取 **專案工作** 欄位中的 **搜尋** 按鈕、選取 **變更檢視表** ，然後選取 **所有使用中專案工作** 以列出所有工作。</span><span class="sxs-lookup"><span data-stu-id="c4f44-115">If you're creating a time entry for a task that isn't assigned to a user, in the **Project Task** field, select the **Search** button, select **Change View** , and then select **All Active Project Tasks** to list all tasks.</span></span>

5. <span data-ttu-id="c4f44-116">輸入描述 (如果需要描述)，然後選取 **儲存後關閉** 。</span><span class="sxs-lookup"><span data-stu-id="c4f44-116">Enter a description, if a description is required, and then select **Save and Close**.</span></span>

<span data-ttu-id="c4f44-117">建立並儲存時間項目之後，您可以在時間輸入網格中進行編輯。</span><span class="sxs-lookup"><span data-stu-id="c4f44-117">After the time entry is created and saved, you can edit it in the time entry grid.</span></span> <span data-ttu-id="c4f44-118">時間輸入網格支援兩種格式：</span><span class="sxs-lookup"><span data-stu-id="c4f44-118">The time entry grid supports two formats:</span></span>

- <span data-ttu-id="c4f44-119">您可以輸入 **hh:mm** 格式的時間項目。</span><span class="sxs-lookup"><span data-stu-id="c4f44-119">You can enter time entries in **hh:mm** format.</span></span> <span data-ttu-id="c4f44-120">這種格式會接著轉換為時數和分數。</span><span class="sxs-lookup"><span data-stu-id="c4f44-120">This format is then converted to hours and fractions.</span></span>
- <span data-ttu-id="c4f44-121">您可以直接輸入時數和分數。</span><span class="sxs-lookup"><span data-stu-id="c4f44-121">You can enter hours and fractions directly.</span></span>

<span data-ttu-id="c4f44-122">請注意，小時的分數並不是分鐘。</span><span class="sxs-lookup"><span data-stu-id="c4f44-122">Note that the fractions of an hour aren't minutes.</span></span> <span data-ttu-id="c4f44-123">因此，1.5 小時代表 1 小時 30 分鐘。</span><span class="sxs-lookup"><span data-stu-id="c4f44-123">Therefore, 1.5 hours represents 1 hour and 30 minutes.</span></span> <span data-ttu-id="c4f44-124">同樣的規則也適用於天的分數。</span><span class="sxs-lookup"><span data-stu-id="c4f44-124">The same rule applies to fractions of a day.</span></span> <span data-ttu-id="c4f44-125">一天為 24 個小時，而 0.5 天即表示 12 個小時。</span><span class="sxs-lookup"><span data-stu-id="c4f44-125">One day is 24 hours, and 0.5 days represents 12 hours.</span></span>

## <a name="bulk-create-time-entries"></a><span data-ttu-id="c4f44-126">大量建立時間項目</span><span class="sxs-lookup"><span data-stu-id="c4f44-126">Bulk create time entries</span></span>

<span data-ttu-id="c4f44-127">建立幾個時間項目之後，您可以使用複製這些項目以大量建立其他時間項目。</span><span class="sxs-lookup"><span data-stu-id="c4f44-127">After a few time entries have been created, you can copy them to create additional time entries in bulk.</span></span>

1. <span data-ttu-id="c4f44-128">在 **時間項目** 頁面上，選取 **複製週次** 。</span><span class="sxs-lookup"><span data-stu-id="c4f44-128">On the **Time Entries** page, select **Copy Week**.</span></span>
2. <span data-ttu-id="c4f44-129">在 **開始期間** 欄位群組中，使用 **開始日期** 和 **結束日期** 欄位來定義要從中複製時間項目的日期範圍。</span><span class="sxs-lookup"><span data-stu-id="c4f44-129">In the **From Period** field group, in the **Start Date** and **End Date** fields, define the date range to copy time entries from.</span></span>
3. <span data-ttu-id="c4f44-130">在 **結束期間** 欄位群組的 **開始日期** 欄位中，指定建立時間項目的日期。</span><span class="sxs-lookup"><span data-stu-id="c4f44-130">In the **To Period** field group, in the **Start Date** field, specify the date to create time entries for.</span></span>
4. <span data-ttu-id="c4f44-131">選取 **複製** 以建立與 **結束期間** 欄位群組所指定星期幾相對應的時間項目複本。</span><span class="sxs-lookup"><span data-stu-id="c4f44-131">Select **Copy** to create a copy of the time entries that correspond to the day of the week that is specified in the **To Period** field group.</span></span> <span data-ttu-id="c4f44-132">例如，將上週星期一的時間項目複製到 **結束期間** 欄位群組所指定之週的星期一。</span><span class="sxs-lookup"><span data-stu-id="c4f44-132">For example, the time entry for Monday of last week is copied to Monday of the week that is specified in the **To Period** field group.</span></span>

## <a name="import-data-for-time-entries"></a><span data-ttu-id="c4f44-133">匯入時間項目的資料</span><span class="sxs-lookup"><span data-stu-id="c4f44-133">Import data for time entries</span></span>

<span data-ttu-id="c4f44-134">您可以從專案預約和指派匯入資料。</span><span class="sxs-lookup"><span data-stu-id="c4f44-134">You can import data from project bookings and assignments.</span></span> <span data-ttu-id="c4f44-135">匯入資料時，您可以指定要匯入的預約日期範圍，然後明確選取應建立為 **草稿** 時間項目的預約。</span><span class="sxs-lookup"><span data-stu-id="c4f44-135">When you import data, you can specify the date range of the bookings to import and then explicitly select the bookings that should be created as **Draft** time entries.</span></span>

## <a name="group-by-sort-search-and-filter-capabilities"></a><span data-ttu-id="c4f44-136">群組依據、排序、搜尋及篩選功能</span><span class="sxs-lookup"><span data-stu-id="c4f44-136">Group by, sort, search, and filter capabilities</span></span>

<span data-ttu-id="c4f44-137">您可以依據欄中指定的維度來分組和篩選時間項目。</span><span class="sxs-lookup"><span data-stu-id="c4f44-137">You can group and filter time entries by the dimensions that are specified in the columns.</span></span> <span data-ttu-id="c4f44-138">在 **群組依據** 欄位中，選取要用來篩選時間項目的維度。</span><span class="sxs-lookup"><span data-stu-id="c4f44-138">In the **Group by** field, select the dimension to use to filter time entries.</span></span> <span data-ttu-id="c4f44-139">您也可以使用欄標題上的排序箭頭，依遞增或遞減順序排序時間項目記錄。</span><span class="sxs-lookup"><span data-stu-id="c4f44-139">You can also sort the time entry records in ascending or descending order by using the sort arrow on the column headings.</span></span> <span data-ttu-id="c4f44-140">此外，還可以選取欄標題上的 **篩選** 按鈕來顯示或隱藏項目，然後在 **搜尋** 方塊中輸入要依據專案名稱、專案工作、時間項目或資源用來搜尋時間項目的文字。</span><span class="sxs-lookup"><span data-stu-id="c4f44-140">Additionally, you can show or hide entries by selecting the **Filter** button on the column headings, and then, in the **Search** box, entering the text that should be used to search for time entries by project name, project task, time entry, or resource.</span></span>
