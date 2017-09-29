--- 
title: "Fastlægge betingelser for debitorbetaling"
description: "Denne procedure definerer opsætning af en kasserabat og forfaldsdato."
author: aprilolson
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f01d88149074b37517d00f03d8f55e1199a5198f
ms.openlocfilehash: c871421254be6b0e9443fdf596932776d64428ae
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="establish-customer-payment-terms"></a>Fastlægge betingelser for debitorbetaling

[!include[task guide banner](../../includes/task-guide-banner.md)]

Denne procedure definerer opsætning af en kasserabat og forfaldsdato. Denne opgaveguide anvender demofirmaet USMF.

1. Gå til Debitor > Betalingsopsætning > Betalingsdage.
    * Opsætningen af betalingsbetingelserne er delt for Debitor og Kreditor. Hvis du definerer den i modulet, bliver den også tilgængelig i det andet modul. Til denne opgaveguide angiver jeg alle betalingsbetingelserne under Debitor.  
2. Klik på Ny.
    * Opret en betalingsdag, hvis betalingsbetingelserne kræver en bestemt dag i ugen (mandag, tirsdag osv.) eller en bestemt dato i måneden (5., 10 osv).  
3. Angiv et id for betalingsdagen i feltet Betalingsdag.
4. Angiv en beskrivelse af betalingsdagen i feltet Beskrivelse.
5. Vælg enten Uge eller Måned i feltet Uge/Måned.
    * Hvis du vil angive en dag i ugen, såsom mandag, skal du vælge Uge. Hvis du vil angive en dato i måneden, såsom den 10., skal du vælge Måned. Væld Måned i dette eksempel.  
6. Angiv en dato i feltet Dag i måned.
    * Datoen skal angives som et tal, f.eks "10" og ikke "10.".  
7. Klik på Gem.
8. Luk siden.
9. Gå til Debitor > Betalingsopsætning > Betalingsbetingelse.
10. Klik på Ny.
    * Betalingsbetingelser bruges til at definere, hvordan forfaldsdatoer beregnes. Opsætningen af datoen for kasserabatten er defineret på en separat side.  
11. Angiv et id i feltet Betalingsbetingelser.
12. Indtast en beskrivelse i feltet Beskrivelse.
13. Vælg en betalingsmetode, f.eks. Efterkrav, Aktuel måned osv.
    * Betalingsmåden bruges til at definere starten for, hvordan forfaldsdatoen beregnes.  Net bruges for eksempel, hvis forfaldsdatoen altid er et angivet antal måneder eller dage efter fakturadatoen. Efterkrav kan bruges i tilfælde, hvor betalingen skal falde ved fakturering, så der ikke beregnes en forfaldsdato. Vælg Indeværende måned for denne opgaveguide.  
14. Vælg en betalingsdag, hvis en bestemt dag i ugen eller dato medtages i beregningen.
    * Du kan angive et antal i måneder eller dage, afhængigt af dine betalingsbetingelser. Eller du kan bruge betalingsplanen eller betalingsdagen, som skal "tilføjes" til slutningen af betalingsmåden. Hvis forfaldsdatoen altid vil være den 10. i næste måned, skal du vælge den 10. som betalingsdag.  
15. Klik på Gem.
16. Luk siden.
17. Gå til Debitor > Betalingsopsætning > Kasserabatter.
18. Klik på Ny.
    * Denne side bruges til at definere, hvordan kasserabatdatoen beregnes.  
19. Angiv et id i feltet Kasserabat.
20. Indtast en beskrivelse i feltet Beskrivelse.
21. Hvis der findes en lagdelt kasserabat, kan du vælge Næste rabatkode, der er relevant efter denne nye kasserabat.
22. Angiv antal dage, der bruges til at beregne kasserabatdatoen.
    * Hvis der vælges nettoprincip, føjes antallet af dage til fakturadatoen for at beregne kasserabatdatoen.  
23. Angiv procentdelen af kasserabatten.
24. Angiv den hovedkonto, som kasserabatten bogfører til for debitorfakturaer.
25. Vælg en indstilling i feltet Rabatmodkonti.
    * Hvis du vælger "Konti på fakturalinjer", bogføres kasserabatten til samme aktiv/udgiftshovedkonto på linjerne i kreditorfakturaen. Kasserabatten"Brug hovedkonto til kreditorfakturaer", bogføres kasserabatten til den hovedkonto, du definerer i "Hovedkonto for kreditorfakturaer". I dette eksempel skal du vælge "Brug hovedkonto til kreditorfakturaer".  
26. Angiv den hovedkonto, som kasserabatten bogfører til for kreditorfakturaer.
27. Klik på Gem.

