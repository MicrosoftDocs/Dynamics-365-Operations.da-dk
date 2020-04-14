---
title: Registrere modtagelsen af varer for indkøbsordren
description: Dette emne beskriver, hvordan du registrerer modtagelsen af varer direkte på en indkøbsordre.
author: FrankDahl
manager: AnnBe
ms.date: 07/09/19
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: PurchTable, PurchCreateOrder, InventItemIdLookupPurchase, PurchEditLines
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 31690d58d32a93d4cba873e951c26856d3f9cc09
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/18/2020
ms.locfileid: "3147313"
---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Registrere modtagelsen af varer for indkøbsordren

[!include [banner](../../includes/banner.md)]

Dette emne beskriver, hvordan du registrerer modtagelsen af varer direkte på en indkøbsordre. Du kan også registrere produktkvitteringen på lagerstedet og derefter bogføre det senere på indkøbsordren. Denne opgave udføres typisk af en indkøber eller en kreditorkoordinator. Eksemplet i denne vejledning kan bruges i demodatafirmaet USMF. Eksemplet indeholder trin til oprettelse af en enkelt indkøbsordre, så du kan afspille proceduren som en opgave. Hvis du har brugt proceduren for dine egne data, skal du starte med underopgaven **Registrer modtagelsen af varer**.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Udarbejd en ny indkøbsordre for modtagelsen af varer
1. Gå til **Navigationsruden > Moduler > Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer**.
2. Vælg **Ny**.
3. I feltet **Leverandørkonto** skal du indtaste `US-101`.
4. Vælg **OK**.
5. I feltet **Varenummer** skal du indtaste `M0001`.
6. I feltet **Antal** skal du indtaste `5`.
7. Klik på **Køb** i handlingsruden.
8. Vælg **Bekræft**.

## <a name="record-receipt-of-goods"></a>Postér modtagelse af varer
1. Vælg **Modtag** i handlingsruden.
2. Vælg **Produktkvittering**. I feltet **Antal** kan du vælge forskellige indstillinger for det antal, du vil modtage. Hvis der f.eks. tidligere er registreret et antal på lageret, kan du vælge **Registreret antal**. I dette eksempel kan du bruge værdien **Bestilt antal**.
3. Udvid sektionen **Oversigt**.
4. Skriv en hvilken som helst værdi i feltet **Produktkvittering**. Dette felt bruges til at angive en reference, der skal bruges som bilag for produktkvitteringskladden.  
5. Udvid sektionen **Linjer**.
6. Angiv **Antal** til '4'. Her kan du manuelt angive det antal, der modtages for hver linje på ordren.  
7. Vælg **OK**. Varerne er nu registreret som modtaget på indkøbsordren, og der er oprettet en produktkvitteringskladde som dokument for at afspejle dette. Du kan bruge handlingen Produktkvittering til at gennemse de kladder, der er oprettet med indkøbsordren, og til at se, hvad der er modtaget, og hvornår.  

