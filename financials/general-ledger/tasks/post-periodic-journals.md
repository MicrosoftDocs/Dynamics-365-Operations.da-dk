--- 
title: "Bogføre periodiske kladder"
description: "Periodiske kladder kaldes også gentagelseskladder, da beløb, tekst og andre oplysninger gentages, hver gang den periodiske kladde hentes."
author: aprilolson
manager: AnnBe
ms.date: 02/24/2016
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
ms.openlocfilehash: b1b1b857428ca1ee36496f82c79a17eb157c8dd8
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---
# <a name="post-periodic-journals"></a>Bogføre periodiske kladder

[!include[task guide banner](../../includes/task-guide-banner.md)]

Periodiske kladder kaldes også gentagelseskladder, da beløb, tekst og andre oplysninger gentages, hver gang den periodiske kladde hentes. Når du opretter den periodiske kladde, angiver du periodeintervallet for gentagelsen, eksempelvis dage eller måneder. Denne opgaveguide opretter en periodisk kladde med en månedlig gentagelse.



1. Gå til Finans > Periodiske opgaver > Periodiske kladder.
2. Klik på Ny.
3. Indtast eller vælg en værdi i feltet Navn.
4. Klik op linket i den valgte række på listen.
5. Skriv en værdi i feltet Beskrivelse.
    * Beskrivelsen vil være navnet på den periodiske kladde, når den hentes senere, så sørg for at give den et navn, der er relevant.  
6. Klik på Linjer.
    * En periodisk kladde vil typisk omfatte flere kladdelinjer. denne opgaveguide tilføjer dog kun én linje.  
7. Indtast en dato i feltet Dato.
    * Feltet Dato indeholder bogføringsdatoen for den næste overførsel til kassekladden. For journaler, der vil blive hentet hver måned, anbefales det at bruge datoen i den måned, hvor den bogføres, typisk den første eller den sidste dato i perioden. Det er muligt at lade feltet være tomt og give en dato, når kladden er hentet, ved hjælp af feltet Tom dato.    Feltet opdateres automatisk til den næste tilbagevendende dato, når der hentes transaktioner.  
8. I feltet Konto skal du specificere de ønskede værdier.
9. Skriv en værdi i feltet Beskrivelse.
10. Luk siden.
11. Angiv et tal i feltet Debet.
12. I feltet Modkonto skal du specificere de ønskede værdier.
13. Vælg "Måneder" i feltet Enhed.
14. Angiv "1" feltet Antal enheder.
15. Indtast en dato i feltet Sidste dato.
    * Angivelse af sidste dato i den forløbne periode vil forhindre, at gentagelseskladden ved en fejltagelse oprettes i den forkerte startperiode. Sidste dato opdateres senere, hver gang den periodiske kladde hentes.  
16. Klik på Gem.
17. Gå til Standarddashboard.
18. Gå til Finans > Kladdeposteringer > Finanskladder.
19. Klik på Ny.
20. Indtast eller vælg en værdi i feltet Navn.
21. Find og vælg den ønskede post på listen.
22. Klik op linket i den valgte række på listen.
23. Skriv en værdi i feltet Beskrivelse.
24. Klik på Linjer.
25. Klik på Periodisk kladde.
26. Klik på Hent kladde.
27. Indtast en dato i feltet Til dato.
    * Til datoen fungerer som skæringsdato for de periodiske bilagslinjer. Baseret på gentagelsesindstilling, Sidste dato og Til dato kan den samme linje indgå mere end én gang i den kladde, der er resultatet. Til dato opdateres automatisk på basis af sessionsdatoen for sidste gang, den periodiske linje blev overført til en kladde.  
28. Skriv eller vælg en værdi i feltet Nummer på periodisk kladde.
29. Klik op linket i den valgte række på listen.
30. Klik på OK.
    * Periodisk kladde kan nu gennemgås, godkendes eller bogføres afhængigt af krav og konfiguration.  

