---
title: 產品
description: 本主題提供產品類別目錄的相關資訊，您可以使用類別目錄來向客戶提供有關組織所提供產品及定價的資訊。
author: rumant
manager: AnnBe
ms.date: 09/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-customerservice
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: ''
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: suvaidya
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-10-01
ms.openlocfilehash: 28397fd49ad4cdb2c820ef4b6f198f410995ba0f
ms.sourcegitcommit: a2c3cd49a3b667b8b5edaa31788b4b9b1f728d78
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 09/28/2020
ms.locfileid: "3898701"
---
# <a name="products"></a>產品

_**適用於：** 資源/非庫存型案例適用的 Project Operations、精簡部署 - 交易至開立預估發票_

產品是企業的骨幹。 Dynamics 365 Sales Professional 中的產品類別目錄是產品與其價格資訊的集合。 快速建立產品類別目錄，讓銷售代表更容易提高其銷售。

## <a name="add-a-product"></a>新增產品

1.  確定您具有 Sales Manager Professional 或系統管理員角色，以便在 Dynamics 365 Sales Professional 新增產品。
2.  在網站地圖的**設定**下方，選取**產品**。
3.  選取**新增產品**，並填入下列資訊：

    -  **名稱**
    -  **產品識別碼**
    -  **上層**：選取產品的上層產品系列。 如果您要在產品系列中建立下層產品，請在此處填入上層產品系列的名稱。 儲存記錄之後，無法變更此名稱。
    -  **有效期自**/**有效期到**：選取**有效期自**和**有效期到**日期，以定義產品的有效期間。
    -  **單位群組**：選取單位群組。 單位群組是各種產品銷售單位的集合，用於定義個別項目如何組成更大的數量。 例如，如果您新增種子做為產品，就可以建立稱為「種子」的單位群組，並將其主要單位定義為「包」。
    -  **預設單位**：選取產品銷售時最常使用的單位。 單位是用來計算您所銷售產品的數量或計量。 例如，如果您新增種子做為產品，就可以採用包、盒或貨架做為銷售單位。 這裡面每一種都會變成產品的單位。 如果種子幾乎都是以「包」為單位銷售，則選取它做為單位。
    -  **預設價目表**：如果這是新產品，則此欄位為唯讀。 您必須先完成所有必填欄位並儲存記錄之後，才能選取預設價目表。 雖然預設價目表不是必要項目，但是在儲存產品記錄之後，最好設定每個產品的預設價目表。 這樣，如果客戶記錄未含價目表，Sales 就可以使用預設價目表來產生報價、訂單和發票。
    -  **支援小數點**：輸入介於 0 到 5 之間的整數。 如果這項產品無法分成含小數點的數量，請輸入 0。 如果產品沒有相關價目表，將針對此欄位中的值，驗證報價、訂單或發票產品記錄中**數量**欄位的有效位數。
    -  **主題**：將產品與主題建立關聯。 您可以利用主體來分類您的產品以及篩選報表。

4.  選取**儲存**。
5.  在**其他詳細資料**索引標籤的**價目表項目**區段中，選取**更多命令**圖示，然後選取**新增價目表項目**。
7.  在**其他詳細資料**索引標籤的**產品關聯**區段中，選取**更多命令**圖示，然後選取**新增產品關聯**。
8.  在**新增產品關聯**表單中，輸入下列詳細資料，然後選取命令列上的**儲存後關閉**：

    -   **相關產品**：選取所需的產品以做為相關產品新增至您正在處理的現有產品記錄。
    -   **銷售關聯類型**：選取要新增產品為向上銷售、交叉銷售、配件或替代產品。
    -   **方向**：選取產品之間的關聯為單向或雙向。 當您選取單向時，您在**相關產品**中選取的產品將會顯示為現有產品的建議，但反向則不然。

9.  在產品表單上，選取**儲存**。

## <a name="import-products"></a>匯入產品

您可以使用匯入範本，將大量產品資料帶入 Dynamics 365 Sales。

## <a name="revise-a-product"></a>修訂產品

視需要快速修訂產品的屬性並重新發行資訊以保持產品存貨的最新狀態，讓銷售專員可以查看最新的庫存變更。

1.  請確定您具有下列其中一個資訊安全角色或同等的權限：系統管理員、系統自訂員、銷售經理、業務副總、行銷副總或 CEO 商務經理人。
2.  在網站地圖中，選取**產品**。
3.  開啟您要變更的使用中產品，然後在命令列上選取**修訂**。
4.  在**確認修訂**對話方塊中選取**確認**。 這樣會將產品狀態變更為**修訂中**。
5.  完成變更後，在命令列上選取**發行**。

    > [!TIP]
    > 若要還原變更並繼續使用產品的最新使用中版本，請選取**還原**。 這樣會將產品的狀態變更為**使用中**。

## <a name="clone-a-product"></a>再製產品 

當您建立新產品時，再製現有產品可以節省時間。 這樣做會建立原始記錄的複本，包含所有詳細資料，但不包括名稱和 ID。

1.  請確定您具有下列其中一個資訊安全角色或同等的權限：系統管理員、系統自訂員、銷售經理、業務副總、行銷副總或 CEO 商務經理人。
2.  在網站地圖中，選取**產品**。
3.  選取要再製的產品記錄，然後選取命令列的**再製**。 確認對話方塊隨即出現。
4.  選取**確認**。

新的產品記錄會開啟，其中顯示與原始產品記錄相同的詳細資料，但名稱和 ID 不同。

## <a name="retire-a-product"></a>淘汰產品 

如果您的組織不再銷售某一項產品，請將該產品淘汰，以便不再對銷售人員提供該產品。

1.  請確定您具有系統管理員或 Sales Professional Manager 角色或同等的權限。
2.  在網站地圖中，選取**產品**。
3.  開啟您要淘汰的使用中產品，然後在命令列上選取**淘汰**。
4.  在**確認淘汰**對話方塊中選取**確認**。


## <a name="delete-a-product"></a>刪除產品

若要停止銷售產品，請將它刪除。

> [!IMPORTANT]
> 刪除的記錄無法復原。

1.  請確定您具有系統管理員或 Sales Professional Manager 角色或同等的權限。
2.  在網站地圖中，選取**產品**。
3.  選取要刪除的產品記錄，然後選取命令列的**刪除**。
4.  在**確認刪除**對話方塊中選取**繼續**。
 
 ## <a name="quantity-factors-for-products"></a>產品的數量因數

數量因素支援訂閱型產品的銷售。 對於訂閱型產品，報價或專案合約服務內容上的數量會以使用者的月數來表示。

訂閱軟體的價格通常在目錄中儲存為每個月每個使用者的價格。 但是，您可以改用其他時間描述。 在銷售處理期間，報價明細的價格通常是由 IT 銷售專員議定並打折扣的每個使用者、每個月的價格。 每筆交易都有不同的使用者數目和不同的訂閱月數。 用來計算報價明細金額的數量，是使用者人數與訂閱月數的乘積。

數量因數依賴產品屬性。 設定產品的特定屬性時，您可以將這其中一部分屬性或所有屬性標示為數量因數。

系統會驗證是否只有含有數值資料類型的數值屬性或產品屬性，才會標記為數量因數。 將設定數量因數的產品新增至報價明細時，報價明細上的**數量**欄位會變成唯讀欄位。 輸入數量因數的產品屬性值之後，系統會計算報價明細的數量。

例如 (若有下列屬性的話)： 

- **使用者數**：使用者的數目 
- **月數**：訂閱的月期數
- **產品 SKU** 

您可以編輯產品明細的屬性，將**使用者數**和**月數**屬性標示為數量因數。 
