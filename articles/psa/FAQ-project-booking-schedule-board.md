---
title: 從排程面板建立專案預約
description: 本主題提供有關如何從排程面板建立專案預約的資訊。
author: ruhercul
ms.custom:
- dyn365-projectservice
ms.date: 9/26/2019
ms.topic: article
ms.author: ruhercul
audience: Admin
search.audienceType:
- admin
- customizer
- enduser
search.app:
- D365CE
- D365PS
- ProjectOperations
ms.openlocfilehash: 513f7fe75cfb7b1658b4be71ed0a17da7b64a1023992e1dada9adca8f0dbf21e
ms.sourcegitcommit: 7f8d1e7a16af769adb43d1877c28fdce53975db8
ms.translationtype: HT
ms.contentlocale: zh-TW
ms.lasthandoff: 08/06/2021
ms.locfileid: "6987606"
---
# <a name="create-a-project-booking-from-the-schedule-board"></a>從排程面板建立專案預約

[!include [banner](../includes/psa-now-project-operations.md)]

您可以直接將資源從 **團隊** 索引標籤預約到專案，做法是在專案的專案團隊索引標籤上預約，或是從一般團隊成員指派產生資源需求，然後透過專案團隊成員履行產生的需求。

您也可以直接從排程面板將資源預約到專案。 有三種方式來完成此動作：

- **透過產生的資源需求預約：** 建立一般資源並於專案中指派工作之後，就可以產生資源需求。

- **從主要需求預約：** 主要需求會顯示在 **專案** 索引標籤的排程面板上。 

- **透過新的資源需求預約**：您可以從頭開始建立資源需求，並將其與專案產生關聯。 在排程面板中，資源需求會出現在 **開啟需求** 索引標籤上。

## <a name="book-from-a-generated-resource-requirement"></a>透過產生的資源需求預約

您可以建立一般資源，再將其指派給專案中的一個或多個工作。 然後就可以從一般選團隊成員產生資源需求。 

1.  在排程面板中，此資源會出現在 **開啟需求** 索引標籤上。如果您有許多開啟需求，可能就需要使用網格上的欄篩選。 

    ![排程面板上的開啟需求索引標籤。](media/FAQ-Project-Booking-Schedule-Board-1.png "預約及指派表格的螢幕擷取畫面")

2. 選取需求。 **尋找可用性** 索引標籤會顯示在所選列的上方。
 
3. 選取索引標籤時，排程面板的 [排程小幫手] 模式會開啟，然後篩選符合資源需求的可用資源。 在那之後，即可預約資源。

4. 您也可以將所選取的列從排程面板底部拖放到上方網格中的資源儲存格。 放下需求時，這會在右側開啟 **建立資源預約** 面板。

    選取 **預約** 就會將資源預約到專案團隊。

![建立資源預約面板。](media/FAQ-Project-Booking-Schedule-Board-6.png "")
 

## <a name="book-from-the-primary-requirement"></a>從主要需求預約

在 Project Service 中建立專案會自動建立稱為「主要需求」的資源需求。 這是在不產生需求，或從頭開始建立需求的情況下，用來快速透過排程面板預約資源的空白需求。 因為需求是空的，您必須指定日期以及配置方法和時數 (如果適用)。 

1. 若要使用主要需求預約資源，請在排程面板上選取 **專案** 索引標籤。如果您有許多專案，您可能需要使用 **專案** 欄上的欄篩選。

   ![排程面板上的欄篩選。](media/FAQ-Project-Booking-Schedule-Board-2.png "預約及指派表格的螢幕擷取畫面")

2. 選取僅以專案名稱做為其名稱且期間為零 (0) 的需求。

3. 選取列上顯示的 **尋找可用性** 索引標籤。 這會讓排程面板進入 [排程小幫手] 模式，並顯示可以預約到專案的可用資源。

4. 因為 **主要需求** 是期間為零 (0) 的空白需求，當您選取和預約資源時，必須在 **建立資源預約** 面板上設定期間。

5. 您也可以選取排程面板底部的 **專案主要需求**，再將其拖放到要預約的資源。
 
    因為 **主要需求** 是期間為零 (0) 的空白需求，當您選取和預約資源時，必須在 **建立資源預約** 面板上設定期間。
 
    當您在排程面板上透過 **主要需求** 預約資源時，不做任何指派，也能將資源新增至專案團隊。
 
## <a name="book-from-a-new-resource-requirement"></a>透過新的資源需求預約
完成下列步驟，以透過新的資源需求預約。 

1. 移至 **資源需求**，然後選取 **新增** 以建立新的資源需求。

2. 在 **專案** 索引標籤上，選取要將需求與專案建立關聯的專案。
 
    在排程面板上，這個新需求會在排程面板上顯示為您可以履行的 **開啟需求**。

3. 預約資源以將該資源新增至專案團隊。

4. 現在資源已預約，您必須以手動方式指派工作。



[!INCLUDE[footer-include](../includes/footer-banner.md)]