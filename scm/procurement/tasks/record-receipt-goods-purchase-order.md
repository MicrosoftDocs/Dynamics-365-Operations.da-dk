--- 
title: "Registrere modtagelsen af varer for indkøbsordren"
description: "Denne fremgangsmåde viser, hvordan du registrerer modtagelsen af varer direkte på en indkøbsordre."
author: FrankDahl
manager: AnnBe
ms.date: 08/23/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: fdahl
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: 01fbf4964dfcecab272204db9c3f5068ca1879cb
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="record-the-receipt-of-goods-on-the-purchase-order"></a>Registrere modtagelsen af varer for indkøbsordren

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne fremgangsmåde viser, hvordan du registrerer modtagelsen af varer direkte på en indkøbsordre. Du kan også registrere produktkvitteringen på lagerstedet og derefter bogføre det senere på indkøbsordren. Denne opgave udføres typisk af en indkøber eller en kreditorkoordinator. Eksemplet i denne vejledning kan bruges i demodatafirmaet USMF. Eksemplet indeholder trin til oprettelse af en enkelt indkøbsordre, så du kan afspille proceduren som en opgave. Hvis du bruger fremgangsmåden på dine egne data, skal du starte med underopgaven for postering af modtagelsen af varerne.


## <a name="prepare-a-new-purchase-order-for-receipt-of-goods"></a>Udarbejd en ny indkøbsordre for modtagelsen af varer
1. Gå til Indkøb og forsyning > Indkøbsordrer > Alle indkøbsordrer.
2. Klik på Ny.
3. Skriv "US-101" i feltet Kreditorkonto.
4. Klik på OK.
5. Indtast M0001 i feltet Varenummer.
6. Skriv 5 i feltet Antal.
7. Klik på Køb i handlingsruden.
8. Klik på Bekræft.

## <a name="record-receipt-of-goods"></a>Postér modtagelse af varer
1. Klik på Modtag i handlingsruden.
2. Klik på Produktkvittering.
    * I feltet Antal kan du vælge forskellige indstillinger for det antal, du vil modtage. Hvis der f.eks. tidligere er registreret et antal på lageret, kan du vælge Registreret antal.  I dette eksempel kan du bruge værdien i Bestilt antal.   
3. Skriv en hvilken som helst værdi i feltet Produktkvittering.
    * Dette felt bruges til at angive en reference, der skal bruges som bilag for produktkvitteringskladden.  
4. Udvid sektionen Linjer.
5. Angiv antallet til '4'.
    * Her kan du manuelt angive det antal, der modtages for hver linje på ordren.  
6. Skjul sektionen Linjer.
7. Klik på OK.
    * Varerne er nu registreret som modtaget på indkøbsordren, og der er oprettet en produktkvitteringskladde som dokument for at afspejle dette. Du kan bruge handlingen Produktkvittering til at gennemse de kladder, der er oprettet med indkøbsordren, og til at se, hvad der er modtaget, og hvornår.  


