---
title: 範例資料安裝
description: 本主題提供有關安裝 Project Service Automation 其中範例資料的資訊。
ms.custom: dyn365-projectservice
ms.date: 11/08/2018
ms.reviewer: johnmichalak
ms.suite: ''
applies_to: Dynamics 365 Project Service Automation
author: ruhercul
ms.author: ruhercul
search.audienceType: IT Pro, Developer
search.app: ''
ms.openlocfilehash: 952f3c3c037bb8459bdd1400288c4ea8604ce282
ms.sourcegitcommit: c0792bd65d92db25e0e8864879a19c4b93efb10c
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 04/14/2022
ms.locfileid: "8581826"
---
# <a name="sample-data-installation-for-the-project-service-application"></a>Project Service 應用程式的範例資料安裝

[!include [banner](../includes/psa-now-project-operations.md)]

為了協助您建立自己的示範環境，Microsoft 提供可下載的範例資料套件，展示應用程式的功能。 有兩種類型的範例資料套件：
- 參考/設定資料
- 示範資料 (參考/設定交易資料，例如工單和專案)

範例 **參考** 資料套件有三種不同的套件可下載，因此您可以只安裝 Project Service 或只安裝 Field Service 的資料，也可以同時安裝兩個應用程式的範例資料。

範例設定/參考資料套件如下：

- [**V902PSMasterData** - 僅限 Project Service 3.x 版](https://go.microsoft.com/fwlink/?linkid=2026540&clcid=0x409)

- [**V902FSMasterData** - 僅限 Field Service 8.x 版](https://go.microsoft.com/fwlink/?linkid=2026536&clcid=0x409)

- [**V902FPSMasterData** - Field Service 8.x 和 Project Service 3.x](https://go.microsoft.com/fwlink/?linkid=2026041&clcid=0x409)

最新的 **示範** 資料套件是：

 - [**FPSDemoData** - Field Service 8.x 和 Project Service 3.x](https://aka.ms/fpsdemodatapackage)

   安裝指示在要建立和設定區段的使用者方面稍有不同，但其他部分與先前 [**部落格文章**](https://aka.ms/fpsdemodatablog)中的內容相同。 這個套件提供精簡的示範資料集，需要約 3 個小時來安裝。

這些範例資料套件僅提供英文版。

> [!IMPORTANT]
> **沒有方法可以解除安裝範例資料。** 您只能將這些套件安裝在示範、評估、訓練或測試系統。 另請注意，不支援安裝個別套件後再安裝其他個別封裝。 (換句話說，您無法在 **PSMasterData** 之後安裝 **FSMasterData**，反之亦然)。如果您日後任何時候覺得需要這兩個應用程式的範例資料，就應該安裝 **v902FPSMasterData** 套件。

安裝其中任一範例資料套件時，安裝程序會執行下列動作：

- 建立或設定使用 Project Service、Field Service 或這兩個應用程式時的預設參數 (若適用)。

- 匯入應用程式的範例資料 (例如可預約資源、應用程式特定角色、銷售與成本價目表、組織單位、銷售處理記錄以及其他實體) 以示範主要功能。  

您可以透過 **示範資料** 套件，取得上述及其他交易資料，例如工單和專案。

想要知道可以使用範例資料示範哪些功能嗎？ 請參閱[技術注意事項](#technical-notes)中的 Fabrikam Robotics 虛構案例。

如果您有安裝這些範例資料套件的疑問，請[透過 fpsdemodata@microsoft.com 傳送電子郵件給我們](mailto:fpsdemodata@microsoft.com)。

## <a name="requirements"></a>需求

安裝通訊協定假設您的目標執行個體 (組織) 的相關資訊如下：

- 基礎語言為英文，而基準貨幣為美元 (USD,$)。

- 組織還沒有 Project Service 或 Field Service 資料，或是只有隨附於任何新組織的基本預設資料。

- 已安裝正確版本的商務應用程式：
       
    - **FPSDemoData 或 v902FPSMasterData：** 組織已安裝 Field Service 8.x 版和 Project Service 3.x 版。

    - **v902PSMasterData：** 組織已安裝 Project Service 3.x 版。

    - **v902FSMasterData：** 組織已安裝 Field Service 8.x 版。

> [!NOTE]
> 如果您需要在已經有資料的現有 Project Service 和 Field Service 試用版或示範環境之上安裝範例資料 (不建議)，就必須暫停安裝程式所執行的安全性預檢。 如需詳細資訊，請參閱下面的技術注意事項。

## <a name="prepare-for-installation"></a>準備安裝

您必須在使用最新版 Windows (最好是 Windows 10) 的電腦上執行安裝程式。

您必須規劃讓電腦保持與網路連線，並且讓安裝執行長達 **1 小時** 以取得 **設定/參考資料**。 (安裝通常需要約 30 分鐘來取得 **FPSMasterData**，其中包含這兩個應用程式的範例資料)。至於 **FPSDemoData**，安裝則需要約 **3 小時**。

電腦必須關閉螢幕保護裝置功能。 否則，螢幕保護裝置開始啟動時，安裝可能會遺失工作階段認證 (除非您讓工作階段自始至終都保持在使用中狀態)。

> [!div class="mx-imgBorder"]
> ![關閉螢幕保護裝置後的螢幕保護裝置設定螢幕擷取畫面。](media/sample-data-1.png)

## <a name="download-and-unpack"></a>下載並解壓縮

Project Service 及 Field Service 的範例資料安裝程式是以自動解壓縮可執行檔的形式來發佈。 檔案名稱可能因範例資料套件而異，除此之外，不論您安裝的是哪個套件，步驟都一樣。

下載套件後，執行 .exe 檔案，然後接受條款及條件，即可將壓縮的 zip 檔案解壓縮。 接著需要將該檔案的內容解壓縮到電腦上的資料夾。

依據作業系統及安全性設定，您可能需要在解壓縮 zip 檔案之後執行下列步驟：

1. 在 **v902FPSMasterData** / **PackageDeployer_FPSDemoData** 資料夾中尋找 **FPSDemoData.dll** 檔案，並以滑鼠右鍵按一下該檔案。

2. 選擇 **解除封鎖**。

3. 選取 **套用**。

4. 選取 **確定**。


## <a name="create-or-configure-users"></a>建立或設定使用者

**FPSDemoData** 套件需要六位使用者，而 **FPSMasterData** 套件則需要一位使用者。 請參閱適用於您的範例資料套件的正確套件。

## <a name="create-or-configure-users---setupreference-data-packages"></a>建立或設定使用者 - 設定/參考資料套件

**FPSMasterData** 套件是設計要透過一個名為 Spencer Low 的使用者使用下述設定值來進行安裝。 若要正確安裝套件，您必須在環境中建立 (或暫時重新命名) 使用者以符合傳入的範例資料設定。

若要建立或設定使用者，請移至 **設定** > **安全性** > **使用者**，然後執行下列動作：

1. 將 UserFullname="Spencer Low" 且使用者名稱為 "spencerl" (**小寫**) 的使用者設定為專案經理及實務經理角色。

2. 選取 **Spencer Low** 使用者，然後選取 **管理角色**。 尋找並選取 **系統管理員** 角色，然後選取 **確定** 以授與 Spencer Low 完整的系統管理員權限。 必須執行此步驟，才能確保範例記錄是使用正確的使用者擁有權所建立，因而可以正確填入檢視表。

3. 在已下載的套件中，您需要使用預設使用者內容的電子郵件地址來更新資料對應檔。 若要這樣做，請開啟 **PkgFolder**，再找出 **ImportUserMapFile.xml** 檔案，然後在記事本 (Visual Studio 或其他 XML 編輯器) 中開啟該檔案。 將 **DefaultUserToMapTo=** 欄位設定為 Spencer Low 使用者的電子郵件地址。

4. 如果使用的不是使用者名稱為 **spencerl** 的 Spencer Low，則需要更新額外的檔案。 開啟 **DemoDataPreImportConfig.xml** 檔案，然後尋找 **userstocreateandconfigure** 標籤。 使用 Spencer Low 使用者的使用者名稱更新 **\<login\>** 標籤。 如需詳細資訊，請參閱[技術注意事項](#technical-notes)。

## <a name="create-or-configure-users---demo-data-package"></a>建立或設定使用者 - 示範資料套件

示範資料套件需要六位使用者。 為了讓套件正確安裝，請執行下列動作：

 1. 移至 **設定** > **安全性** > **使用者**，建立使用者或暫時重新命名現有使用者以符合接收範例資料設定。
 
    只有角色型示範才需要這些角色。  
    - 使用者全名 = "David So"，擔任現場服務技師   
    - 使用者全名 = "Jamie Reding"，擔任客戶服務與現場服務調度員   
    - 使用者全名 = "Molly Clark"，擔任客戶經理   
    - 使用者全名 = "Spencer Low"，擔任執業與專案管理  
    - 使用者全名 = "Spencer Low"，擔任團隊成員   
    - 使用者全名 = "William Contoso"
  
2. 為了匯入示範資料，請將系統管理員角色指派給上述六位使用者，讓範例記錄正確匯入。 

3. 開啟 **PkgFolder**，然後尋找並開啟 **ImportUserMapFile.xml**。 將 **New=** 欄位更新為系統中對應使用者的電子郵件地址。

   > [!div class="mx-imgBorder"]
   > ![UserMapFile 的螢幕擷取畫面。](media/sample-data-7.png)

4. 如果 "Spencer Low" 全名使用者的使用者識別碼與 **"spencerl"** 不同，您必須更新額外的檔案。 開啟 **DemoDataPreImportConfig.xml**，並尋找 **userstocreateandconfigure** 標籤。 以 loginId (區分大小寫) 來更新 **\<login\>** 標籤。 

5. 第一個使用者的行事曆 (在 **userstocreateandconfigure** 標籤中) 會在匯入示範資料時，用來填入所有可預約資源的工作時數。 瀏覽至 **設定** > **安全性** > **使用者**、尋找您 "Spencer Low" 使用者，然後開啟 [工作時數] 選項。 編輯現有的工作時數，並選取 **從開始到結束整個週期性每週排程** 選項。 確認 **工作時數設定為星期一至星期五上午 8 時 - 下午 5 時 (9 小時)，以及時區設定為太平洋時間 (美國和加拿大)**。 必須這樣才能確保專案及排程面板如預期般顯示。

**建議：** 考慮立即建立您組織的資料備份，以防範例資料安裝過程中發生錯誤時，您需要回復到起始點。 如需詳細資訊，請參閱[備份與還原執行個體](/dynamics365/customer-engagement/admin/backup-restore-instances)。

## <a name="run-the-package-deployer"></a>執行 Package Deployer

1. 在 **v902FPSMasterData** 或 **PackageDeployer_FPSDemoData** 資料夾中尋找並執行 **PackageDeployer.exe**。

2. 接受條款及條件。

3. 在下一個視窗中：

   a. 選取部署類型 **Office 365**。

   b. 使用系統管理員使用者在 [建立或設定使用者] 中的使用者和密碼 (「Spencer Low」的使用者名稱為「spencerl」)。

   c. 確定 **顯示可用組織清單** 已選取。

      > [!div class="mx-imgBorder"]
      > ![已選取 [顯示可用組織清單] 的 Package Deployer 視窗螢幕擷取畫面](media/sample-data-2.png)

4. 選取您要安裝範例資料所在的組織。

5. 選取 **下一步**，直到您看到 **示範資料安裝程式** 對話方塊。

   > [!div class="mx-imgBorder"]
   > ![示範資料安裝程式狀態視窗的螢幕擷取畫面。](media/sample-data-3.png)

6. 繼續之前，請注意，安裝範例資料最多可能需要花費一個小時 (通常不到 10 分鐘)。 您必須確保電腦在整個安裝過程中保持開啟且連線至網路，以及您的工作階段維持在使用中狀態。   

7. 當您準備好時，按 **下一步** 以開始範例資料安裝程序。 載入範例資料後，按一下 **完成**。

## <a name="verify-the-sample-data-installation"></a>驗證範例資料安裝

進行完整性檢查時，確認 Fabrikam Robotics 虛構案例中列出的記錄筆數和實體類型依預期顯示。

範例資料完全載入之後，以 Spencer Low 使用者身分登入，並確認下列各項：

- 如果 Project Service 應用程式已安裝，請移至 **Project Service** > **設定** > **價目表**。 確認資料集中的每個國家/地區都有適當貨幣的帳單費率和成本費率。

- 如果 Project Service 應用程式已安裝，請移至 **Universal Resource Scheduling** > **設定** > **業務單位**。 確認使用適當貨幣的成本價目表已經與每個組織單位 (不含市/鎮項目) 建立關聯。 如果有任何遺漏，請尋找正確的成本價目表並與之建立關聯。

- 如果 Field Service 應用程式已安裝，請移至 **Project Service** > **設定** > **價目表**。 確認有帳單費率和成本費率存在。 移至 **Field Service** > **設定** > **價目表**，然後檢查資料集中的每個國家/地區是否有適當貨幣的帳單費率和成本費率。

  > [!div class="mx-imgBorder"]
  > ![使用中價目表的螢幕擷取畫面。](media/sample-data-4.png)

  > [!div class="mx-imgBorder"]
  > ![使用中組織單位的螢幕擷取畫面。](media/sample-data-5.png)

## <a name="technical-notes"></a>技術注意事項

請參閱下文以取得有關安裝此資料的技術詳細資料。

### <a name="installing-sample-data-on-top-of-existing-data-not-recommended"></a>在現有資料之上安裝範例資料 (不建議)

如果您需要在已經有資料的現有 Field Service 或 Project Service 試用版或示範環境之上安裝範例資料，就必須暫停安裝程式所執行的安全性預檢。

若要執行此動作，請移至 **PkgFolder** 資料夾，找出 **DemoDataPreImportConfig.xml** 檔案，並在記事本 (或其他 XML 編輯器) 中開啟該檔案。

尋找下列值，然後將設定值從 true 變更為 false：

```alias
<TerminateOnPreCheckFailure>true</TerminateOnPreCheckFailure>
```

這項變更會導致安裝程式略過一些重要的安全性檢查，包括：

- 確認沒有多個使用中 **組織單位** 記錄，然後將其重新命名為 **Fabrikam US**。

- 確認沒有多個使用中 **工作範本** 記錄。

- 確認沒有多個使用中 **專案參數** 記錄，然後將該項目重新命名為 **參數**。

### <a name="configuration-components"></a>設定元件

此預先匯入設定檔中有數個其他設定元件。 適用於技術使用者的其中一些元件包括：

- **\<RequiredSolutions\>** 指定先決條件解決方案安裝及其版本號碼。

- **\<InstallSampleData\>** 控制是否安裝應用程式立即可用的範例資料。

    - false - 略過此內建資料 (可移除) 的安裝

    - true - 在安裝 FS 和 PSA 範例資料的同時安裝內建資料

- **\<PreImportDataCollection\>** 指定要在安裝主要範例資料之前先匯入一般檔案資料對應及相關記錄。

- **\<EntitiesToEnableScheduling\>** 指定必須為 Microsoft Dynamics Scheduling (亦稱為 Universal Resource Scheduling) 中的預約啟用哪些實體。

- **\<UsersToCreateAndConfigure\>** 指定將會在執行範例資料匯入之前建立的可預約資源 (若尚不存在)。 請注意，來源系統範例資料可預約資源，與每個資源全名及登入上的目標系統可預約資源記錄都相符。 因此，無法變更此預先設定檔中的名稱，除非您先使用這些名稱將範例資料匯入至目標系統，再將 [可預約資源] 重新命名為您想要隨同 [啟用使用者] 記錄一起設定的名稱，然後再次匯出資料以供匯入至您最終的目的地系統 (相應更新 **ImportUserMapFile.xml** 的舊項目和新項目)。

- **\<PluginsToDisable\>** 指定極其分立的明細項目外掛程式，這些外掛程式必須在進行範例資料匯入時停用並在之後重新啟用。

### <a name="fabrikam-robotics-fictitious-scenario"></a>Fabrikam Robotics 虛構案例

Field Service 和 Project Service 範例參考資料套件會安裝 **Fabrikam Manufacturing 主要資料 (v3.0.0.0) 解決方案**，以及大約 4,000 筆記錄和大約 40 個不同實體。 Field Service 或 Project Service 的個別範例資料套件包含應用程式各自 **v902FPSMasterData** 範例資料的子集。 **示範資料** 套件會安裝 **Fabrikam Manufacturing 示範資料 (v3.0.0.7) 解決方案**，包含 148 個實體約 22,000 筆的記錄。

虛構公司 Fabrikam Robotics 是電子裝置裝配線機器人的製造商，因其產品的品質、創新以及可信賴的客戶服務 (包括安裝規劃、實作與持續維護服務) 而聞名。 Fabrikam 總部設於美國 (Fabrikam US)，並且在法國、印度、英國和瑞士都有專案服務企業營運據點。

現場服務業務營運主要集中在美國境內，多半以大西雅圖區為服務範圍。 該公司著重於運用物聯網 (IoT) 連線能力來監控客戶資產效能，以及逐漸益發積極主動的上門服務。

範例資料的高階概觀，如下所述：

- 一般範例資料元素 (兩個應用程式都有包含)

    - 1 個使用者

    - 71 個帳戶

    - 137 個連絡人

    - 各種交易類型和類別

    - 50 項產品 1 張價目表

    - 14 份價格/成本清單

    - 2 個分 3 等級 (評等值) 的評等模型，涵蓋 31 個特性 (資源技能)

- Project Service

    - 8 個組織單位

    - 6 個角色特定使用率層級

    - 2 千 8 百多種角色價格規格

- Field Service

    - 4 個領域

    - 5 種工單類型

    - 22 項客戶資產

    - 9 個有各種相關資源特性 (9)、服務 (13) 及服務工作 (13) 的事件類型
   
**示範資料** 套件會安裝約 179 份工單、12 項專案以及相關聯的交易資料。 

### <a name="change-the-work-hours-for-sample-resources"></a>變更範例資源的工作時數

根據預設，所有可預約資源都會有 24 工作時數行事曆。

如果您需要變更範例可預約資源的工作時數，請移至 **Universal Resource Scheduling** > **排程** > **排程資源**。

選取使用者 (例如，Spencer Low)，並將 Spencer 的工作時數變更為您想要套用至多個使用者的時數。 移至 **Universal Resource Scheduling** > **設定** > **工作時數範本**，然後編輯 **預設工作範本** 記錄。 在 **範本資源** 欄位中，選取具有您要套用至其他資源之工作時數的使用者。 移至 **Universal Resource Scheduling** > **排程** > **資源** > **使用中的可預約資源**。 選取您要變更的資源，然後選取 **設定行事曆**。 在在 **工作範本** 下拉式清單中，選取 **預設工作時數** 範本或其他含有正確範本化資源的範本。 當您移至排程面板時，您應該會看到資源的工作時數現在已更新。

> [!div class="mx-imgBorder"]
> ![使用中可預約資源的螢幕擷取畫面。](media/sample-data-6.png)


[!INCLUDE[footer-include](../includes/footer-banner.md)]