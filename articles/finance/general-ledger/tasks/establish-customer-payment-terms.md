---
title: Fastlægge betingelser for debitorbetaling
description: Denne procedure definerer opsætning af en kasserabat og forfaldsdato.
author: aprilolson
ms.date: 08/29/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: PaymDay, PaymTerm, CashDisc
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9b2ae5e63a2efb4bc913efa4d88c65a70133a2d9
ms.sourcegitcommit: f96e5dec5a808d9819d2a23b8e15ce00aeff475b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/10/2022
ms.locfileid: "9752770"
---
# <a name="establish-customer-payment-terms"></a>Fastlægge betingelser for debitorbetaling

[!include [banner](../../includes/banner.md)]

Denne procedure definerer opsætning af en kasserabat og forfaldsdato. Denne opgaveguide anvender demofirmaet USMF.

1. Gå til **Navigationsrude > Moduler > Debitor > Betalingsopsætning > Betalingsdage**. Opsætningen af **Betalingsbetingelser** er fælles for **Debitor** og **Kreditor**. Hvis du definerer den i modulet, bliver den også tilgængelig i det andet modul. Til denne opgaveguide er alle betalingsbetingelserne konfigureret under **Debitor**.
2. Klik på **Ny**. Opret en betalingsdag, hvis betalingsbetingelserne kræver en bestemt dag i ugen (mandag, tirsdag osv.) eller en bestemt dato i måneden (5., 10 osv). 
3. Angiv et id i feltet **Betalingsdag**.
4. Angiv en beskrivelse af betalingsdagen i feltet **Beskrivelse**.
5. Vælg enten 'Uge' eller 'Måned' i feltet **Uge/Måned**. Hvis du vil angive en dag i ugen, såsom mandag, skal du vælge Uge. Hvis du vil angive en dato i måneden, såsom den 10., skal du vælge Måned. Væld Måned i dette eksempel. 
6. Angiv en dato i feltet **Dag i måned**. Datoen skal angives som et tal, f.eks "10" og ikke "10.". 
7. Klik på **Gem**.
8. Luk siden.
9. Gå til **Navigationsrude > Moduler > Debitor > Betalingsopsætning > Betalingsbetingelser**. 

>[!NOTE] 
>Hvis **Betalingsbetingelser** er **Kontant**, skal feltet **Kontantbetaling** på siden **Betalingsbetingelser** være **Nej**.

10. Klik på **Ny**. **Betalingsbetingelser** bruges til at definere, hvordan forfaldsdatoer beregnes. Opsætningen af datoen for kasserabatten er defineret på en separat side. 
11. Angiv et id i feltet **Betalingsbetingelser**.
12. Indtast en beskrivelse i feltet **Beskrivelse**.
13. Vælg en **Betalingsmetode**, f.eks. **pr. efterkrav**, **Netto**, **Indeværende måned** osv. **Betalingsmetoden** bruges til at definere starten på, hvordan forfaldsdatoen skal beregnes. **Net** bruges for eksempel, hvis forfaldsdatoen altid er et angivet antal måneder eller dage efter fakturadatoen. **Pr efterkrav** kan bruges i tilfælde, hvor betalingen skal falde ved fakturering, så der ikke beregnes en forfaldsdato. Vælg **Aktuel måned** for denne opgaveguide.  
14. Vælg en **betalingsdag**, hvis en bestemt dag i ugen eller dato medtages i beregningen. Du kan angive et antal i måneder eller dage, afhængigt af dine betalingsbetingelser. Eller du kan bruge **betalingsplanen** eller **betalingsdagen**, som skal 'føjes' til slutningen af **betalingsmåden**. Hvis forfaldsdatoen altid vil være den 10. i næste måned, skal du vælge den 10. som **betalingsdag**. Hvis du bruger en **betalingskalender**, kan du definere, hvordan forfaldsdatoen skal bestemmes, når den beregnede dato lander på en ikke-arbejdsdag. Den første forfaldsdato beregnes ved hjælp af kalenderdage. Hvis den beregnede dato lander på en arbejdsdag, kan du justere den beregnede forfaldsdato til enten den næste eller en tidligere arbejdsdag.
15. Klik på **Gem**.
16. Luk siden.
17. Gå til **Debitor > Betalingsopsætning > Kasserabatter**.
18. Klik på **Ny**. Denne side bruges til at definere, hvordan kasserabatdatoen beregnes. 
19. Angiv et id i feltet **Kasserabat**.
20. Indtast en beskrivelse i feltet **Beskrivelse**.
21. Hvis der findes en lagdelt kasserabat, kan du vælge **Næste rabatkode**, der er relevant efter denne nye kasserabat.
22. I feltet **Dage** skal du angive antallet af dage, der bruges til at beregne kasserabatdatoen. Hvis der vælges **Nettoprincip**, føjes antallet af dage til fakturadatoen for at beregne kasserabatdatoen.  
23. Angiv procenten af kasserabatten i feltet **Rabatprocent**.
24. I **Hovedkonto til debitorrabatter** skal du angive den hovedkonto, som kasserabatten skal bogføres på for debitorfakturaer.
25. Vælg en indstilling i feltet **Rabatmodkonti**. Hvis du vælger "Konti på fakturalinjer", bogføres kasserabatten til samme aktiv/udgiftshovedkonto på linjerne i kreditorfakturaen. Kasserabatten **Brug hovedkonto til kreditorfakturaer**, bogføres kasserabatten til den hovedkonto, du definerer i **Hovedkonto for kreditorfakturaer**. I dette eksempel skal du vælge **Brug hovedkonto til kreditorfakturaer**. 
26. I **Hovedkonto til kreditorrabatter** skal du angive den hovedkonto, som kasserabatten skal bogføres på for kreditorfakturaer.
27. Klik på **Gem**.



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
