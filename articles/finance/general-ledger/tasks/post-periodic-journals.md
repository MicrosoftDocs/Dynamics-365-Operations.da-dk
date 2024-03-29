---
title: Bogføre periodiske kladder
description: Periodiske kladder kaldes også gentagelseskladder, da beløb, tekst og andre oplysninger gentages, hver gang den periodiske kladde hentes.
author: aprilolson
ms.date: 11/21/2022
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTable, LedgerJournalTransPeriodic, LedgerJournalTransDaily
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: bdc1d9f67a515e3cdc45e173b88982feceb0ebfd
ms.sourcegitcommit: fb9b6969218f2b82f0a4c72bfad75387fe00395c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/22/2022
ms.locfileid: "9799361"
---
# <a name="post-periodic-journals"></a>Bogføre periodiske kladder

[!include [banner](../../includes/banner.md)]

Periodiske kladder kaldes også gentagelseskladder, da beløb, tekst og andre oplysninger gentages, hver gang den periodiske kladde hentes. Når du opretter den periodiske kladde, angiver du periodeintervallet for gentagelsen, eksempelvis dage eller måneder. Denne opgaveguide opretter en periodisk kladde med en månedlig gentagelse.

1. Gå til **Navigationsrude > Moduler > Finans > Periodiske opgaver > Periodiske kladder**.
2. Klik på **Ny**.
3. Indtast eller vælg en værdi i feltet **Navn**.
4. Klik op linket i den valgte række på listen.
5. Indtast en værdi i feltet **Beskrivelse**. Beskrivelsen vil være navnet på den periodiske kladde, når den hentes senere, så sørg for at give den et navn, der er relevant.
6. Klik på **Linjer** i **Handlingsrude**. En periodisk kladde vil typisk omfatte flere kladdelinjer. Denne opgaveguide tilføjer dog kun én linje.
7. Indtast en dato i feltet **Dato**. Feltet **Dato** indeholder bogføringsdatoen for den næste overførsel til kassekladden. For journaler, der vil blive hentet hver måned, anbefales det at bruge datoen i den måned, hvor den bogføres. Dette er typisk den første eller sidste dato i perioden. Det er muligt at lade feltet **Dato** være tomt og angive en dato, når kladden er hentet, ved hjælp af feltet **Tom dato**. Feltet opdateres automatisk til den næste tilbagevendende dato, når der hentes transaktioner. 
8. I feltet **Konto** skal du angive de ønskede værdier.
9. Vælg en værdi i feltet **Beskrivelse**.
10. Luk siden.
11. Angiv et tal i feltet **Debet**.
12. I feltet **Modkonto** skal du specificere de ønskede værdier.
13. Vælg **Måneder** i feltet **Enhed**.
14. Angiv **1** i feltet **Antal enheder**.
15. Indtast en dato i feltet **Sidste dato**. Angivelse af sidste dato i den forløbne periode vil forhindre, at gentagelseskladden ved en fejltagelse oprettes i den forkerte startperiode. Sidste dato opdateres senere, hver gang den periodiske kladde hentes. 
16. Klik på **Gem**.
17. Gå til **Navigationsrude > Moduler > Finans > Kladdeposteringer > Finanskladder**.
18. Klik på **Ny**.
19. Indtast eller vælg en værdi i feltet **Navn**.
20. Find og vælg den ønskede post på listen.
21. Klik op linket i den valgte række på listen.
22. Indtast en værdi i feltet **Beskrivelse**.
23. Klik på **Linjer** i **Handlingsrude**.
24. Klik i **handlingsruden** på **Periodisk kladde**.
25. Klik på **Hent kladde**.
26. Indtast en dato i feltet **Til dato**. **Til dato** fungerer som skæringsdato for de periodiske bilagslinjer. Baseret på gentagelsesindstilling, **Sidste dato** og **Til dato** kan den samme linje indgå mere end én gang i den kladde, der er resultatet. **Til dato** opdateres automatisk på basis af sessionsdatoen for sidste gang, den periodiske linje blev overført til en kladde. 
27. Skriv eller vælg en værdi i feltet **Nummer på periodisk kladde**.
28. Klik op linket i den valgte række på listen.
29. Klik på **OK**. Periodisk kladde kan nu gennemgås, godkendes eller bogføres afhængigt af krav og konfiguration.   


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
