---
title: 管理 Office 365 行事曆中的專案和預約
description: 如何管理 Office 365 行事曆中的專案和預約
author: ruhercul
manager: kfend
ms.service: project-operations
ms.custom:
- dyn365-projectservice
ms.date: 8/03/2018
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365PS
- ProjectOperations
ms.openlocfilehash: f9ebfadf8a331fd6a8a86a9cc040dc8957db3b82
ms.sourcegitcommit: 3d78338773929121d17ec3386f6cb67bfb2272cc
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/27/2021
ms.locfileid: "5950299"
---
# <a name="manage-projects-and-bookings-in-your-calendar-project-service"></a><span data-ttu-id="ee972-103">管理行事曆中的專案和預約 (Project Service)</span><span class="sxs-lookup"><span data-stu-id="ee972-103">Manage projects and bookings in your calendar (Project Service)</span></span>

> [!Note]
> <span data-ttu-id="ee972-104">取代：此功能已被取代，不再可用。</span><span class="sxs-lookup"><span data-stu-id="ee972-104">DEPRECATED: This feature has been deprecated and is no longer available.</span></span>

[!include [banner](../includes/psa-now-project-operations.md)]

[!INCLUDE[cc-applies-to-psa-app-1x-2x](../includes/cc-applies-to-psa-app-1x-2x.md)]

[!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 

<span data-ttu-id="ee972-105">使用 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆，檢視私人約會、專案工作預約，以及現場服務工單指派。</span><span class="sxs-lookup"><span data-stu-id="ee972-105">View personal appointments, project-work bookings, and field service work order assignments using the [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="ee972-106">所有一切都在同一個地方，方便您管理一天的工作。</span><span class="sxs-lookup"><span data-stu-id="ee972-106">With everything in one place, it’s easy to manage your day.</span></span> <span data-ttu-id="ee972-107">您的會議、約會、預約及工作都可在 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆中處理。</span><span class="sxs-lookup"><span data-stu-id="ee972-107">Your meetings, appointments, bookings, and tasks are all available in your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span>  
  
 <span data-ttu-id="ee972-108">如果您使用 [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)]，還可以在 Project Service 時間項目檢視表中輸入您的個人約會。</span><span class="sxs-lookup"><span data-stu-id="ee972-108">If you’re using [!INCLUDE[pn_project_service_auto](../includes/pn-project-service-auto.md)], you can also enter your personal appointments in the Project Service time entry view.</span></span> <span data-ttu-id="ee972-109">這可讓專案經理和資源管理員得知您是否有空處理專案。</span><span class="sxs-lookup"><span data-stu-id="ee972-109">This lets project and resource managers know your availability for projects.</span></span> <span data-ttu-id="ee972-110">它還能幫您節省時間，因為您不必重複輸入私人約會的資訊。</span><span class="sxs-lookup"><span data-stu-id="ee972-110">It also saves you time, because you don’t have to enter info about your personal appointments twice.</span></span> <span data-ttu-id="ee972-111">您只要從行事曆將私人約會匯入到 Project Service 時間項目檢視表即可。</span><span class="sxs-lookup"><span data-stu-id="ee972-111">You can simply import your personal appointments from your calendar to Project Service time entry view.</span></span>  
  
 <span data-ttu-id="ee972-112">您的行事曆會將今天到未來四週內的專案和工單預約同步。</span><span class="sxs-lookup"><span data-stu-id="ee972-112">Your calendar will sync project and work order bookings from today to upcoming four weeks.</span></span> <span data-ttu-id="ee972-113">此設定不可變更。</span><span class="sxs-lookup"><span data-stu-id="ee972-113">This setting can’t be changed.</span></span>  
  
 <span data-ttu-id="ee972-114">僅支援從 PSA 到 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆的單向同步處理。</span><span class="sxs-lookup"><span data-stu-id="ee972-114">Syncing is only supported one way, from PSA to your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar.</span></span> <span data-ttu-id="ee972-115">您可以依相反順序進行同步處理。</span><span class="sxs-lookup"><span data-stu-id="ee972-115">You can sync in the reverse order.</span></span> 
  
 <span data-ttu-id="ee972-116">若要了解如何使用 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆，請參閱[商務用 Outlook 網頁版中的行事曆](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936)。</span><span class="sxs-lookup"><span data-stu-id="ee972-116">To learn how to use your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, see [Calendar in Outlook on the web for business](https://support.office.com/article/Calendar-in-Outlook-on-the-web-for-business-5219c457-d1fe-4c2f-9032-1a816b88e936).</span></span>  
  
## <a name="setup"></a><span data-ttu-id="ee972-117">安裝程式</span><span class="sxs-lookup"><span data-stu-id="ee972-117">Setup</span></span>  
 <span data-ttu-id="ee972-118">您需要先進行一些設定，才能在 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆上看見並管理您的預約。</span><span class="sxs-lookup"><span data-stu-id="ee972-118">Before you can see and manage your bookings on your [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar, you need to set a few things up.</span></span>  
  
- <span data-ttu-id="ee972-119">您必須有 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 全域管理員或系統管理員認證。</span><span class="sxs-lookup"><span data-stu-id="ee972-119">You will need to have [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] Global Administrator or System Administrator credentials.</span></span>  
  
- <span data-ttu-id="ee972-120">您的系統管理員需要設定電子郵件伺服器設定檔，而且每個使用者都必須設定他們的信箱。</span><span class="sxs-lookup"><span data-stu-id="ee972-120">Your Admin will need to configure the email server profile and each user will need to configure their mailbox.</span></span> [!INCLUDE[proc_more_information](../includes/proc-more-information.md)]<span data-ttu-id="ee972-121">[透過伺服器端同步處理設定電子郵件處理](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span><span class="sxs-lookup"><span data-stu-id="ee972-121">[Set up email processing through server-side synchronization](/dynamics365/customerengagement/on-premises/admin/set-up-server-side-synchronization-of-email-appointments-contacts-and-tasks)</span></span>  
  
## <a name="turn-on-synchronization-for-your-organization-admin-task"></a><span data-ttu-id="ee972-122">開啟您的組織的同步處理 (系統管理員工作)</span><span class="sxs-lookup"><span data-stu-id="ee972-122">Turn on synchronization for your organization (admin task)</span></span>  
  
1.  <span data-ttu-id="ee972-123">從主要功能表按一下 **設定** > **管理**。</span><span class="sxs-lookup"><span data-stu-id="ee972-123">From the main menu, click **Settings** > **Administration**.</span></span>  
  
2.  <span data-ttu-id="ee972-124">按一下 **系統設定**。</span><span class="sxs-lookup"><span data-stu-id="ee972-124">Click **System Settings**.</span></span>  
  
3.  <span data-ttu-id="ee972-125">按一下 **同步處理** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="ee972-125">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="ee972-126">在 **選取是否啟用同步處理資源預約** 底下，勾選 **與 Outlook 同步處理資源預約**。</span><span class="sxs-lookup"><span data-stu-id="ee972-126">Under **Select whether to enable syncing of resource booking with**, check the **Synchronize resource booking with Outlook**.</span></span>  
  
## <a name="turn-on-synchronization-for-your-user-profile-user-task"></a><span data-ttu-id="ee972-127">開啟使用者設定檔的同步處理 (使用者工作)</span><span class="sxs-lookup"><span data-stu-id="ee972-127">Turn on synchronization for your user profile (user task)</span></span>  
  
1.  <span data-ttu-id="ee972-128">按一下畫面右上角的 **設定** 按鈕。</span><span class="sxs-lookup"><span data-stu-id="ee972-128">Click the **Settings** button in the upper-right corner of the screen.</span></span>  
  
2.  <span data-ttu-id="ee972-129">按一下 **選項**。</span><span class="sxs-lookup"><span data-stu-id="ee972-129">Click **Options**.</span></span>  
  
3.  <span data-ttu-id="ee972-130">按一下 **同步處理** 索引標籤。</span><span class="sxs-lookup"><span data-stu-id="ee972-130">Click the **Synchronization** tab.</span></span>  
  
4.  <span data-ttu-id="ee972-131">在 **與 Outlook 同步處理資源預約** 底下，勾選 **與 Outlook 同步處理資源預約**。</span><span class="sxs-lookup"><span data-stu-id="ee972-131">Under **Resource booking sync with Outlook**, check the **Synchronization resource booking with Outlook**.</span></span>  
  
## <a name="import-your-personal-appointments-user-task"></a><span data-ttu-id="ee972-132">匯入您的私人約會 (使用者工作)</span><span class="sxs-lookup"><span data-stu-id="ee972-132">Import your personal appointments (user task)</span></span>  
 <span data-ttu-id="ee972-133">您可以從行事曆將私人約會匯入到 Project Service Automation 時間項目檢視表即可。</span><span class="sxs-lookup"><span data-stu-id="ee972-133">You can import your personal appointments from your calendar to Project Service Automation time entry view.</span></span>  
  
1. <span data-ttu-id="ee972-134">開啟 [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] 行事曆，並按一下 **匯入資料**。</span><span class="sxs-lookup"><span data-stu-id="ee972-134">Open [!INCLUDE[pn_office_365](../includes/pn-office-365.md)] calendar and click **Import Data**.</span></span>  
  
2. <span data-ttu-id="ee972-135">在 [篩選] 畫面中，選取 **來自 Exchange 的約會**，然後按一下 **套用**。</span><span class="sxs-lookup"><span data-stu-id="ee972-135">On the Filters screen, select **Appointments from Exchange** and then click **Apply**.</span></span>  
  
3. <span data-ttu-id="ee972-136">系統會將約會擷取到時間項目檢視表中，做為本週的建議項目。</span><span class="sxs-lookup"><span data-stu-id="ee972-136">The system will pull appointments into time entry view as suggested entries from the current week.</span></span> <span data-ttu-id="ee972-137">若要新增其他週的項目，請按一下 **上一週** 或 **下一週**。</span><span class="sxs-lookup"><span data-stu-id="ee972-137">To add entries for another week, click **Previous** or **Next**.</span></span>  
  
4. <span data-ttu-id="ee972-138">選取您要新增至 Project Service Automation 時間項目檢視表的約會。</span><span class="sxs-lookup"><span data-stu-id="ee972-138">Select the appointment that you want to add to Project Service Automation time entry view.</span></span>  
  
5. <span data-ttu-id="ee972-139">在 **時間項目** 快顯方塊中，選取適當的選項，以將約會轉換成 Project Service Automation 時間項目檢視表。</span><span class="sxs-lookup"><span data-stu-id="ee972-139">On the **Time Entry** popup box, select the appropriate options to convert the appointment to a Project Service Automation time entry view.</span></span>  
  
6. <span data-ttu-id="ee972-140">按一下 **儲存**。</span><span class="sxs-lookup"><span data-stu-id="ee972-140">Click **Save**.</span></span>  
  
### <a name="see-also"></a><span data-ttu-id="ee972-141">請參閱</span><span class="sxs-lookup"><span data-stu-id="ee972-141">See Also</span></span>  
 [<span data-ttu-id="ee972-142">時間、費用及共同作業指南</span><span class="sxs-lookup"><span data-stu-id="ee972-142">Time, Expense, and Collaboration Guide</span></span>](../psa/time-expense-collaboration-guide.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]