--- 
title: Oversigt over kreditorbetalinger
description: "Denne opgaveguide fører dig gennem forskellige metoder, der bruges til at oprette kreditorbetalinger, herunder hvordan du bruger et betalingsforslag eller manuelt angiver en engangsbetaling."
author: kweekley
manager: AnnBe
ms.date: 10/30/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: cafd499e849570cae7b7f58bf2d487a7ac0093e6
ms.openlocfilehash: e9a94231f755ff23bb442d62e90daff8f2d1f4fb
ms.contentlocale: da-dk
ms.lasthandoff: 10/30/2017

---
# <a name="vendor-payment-overview"></a>Oversigt over kreditorbetalinger

[!include [task guide banner](../../includes/task-guide-banner.md)]

Denne opgaveguide fører dig gennem forskellige metoder, der bruges til at oprette kreditorbetalinger, herunder hvordan du bruger et betalingsforslag eller manuelt angiver en engangsbetaling. Denne procedure bruger demofirmaet USMF.

1. Gå til Kreditor > Betalinger > Betalingskladde.
2. Klik på Ny.
3. Vælg den betalingskladde, som skal gemmes til kreditorbetalinger. 
4. Vælg kladden, eller angiv den manuelt.
5. Klik på Linjer.
6. Klik på Betalingsforslag.
7. Klik på Opret betalingsforslag.
    * Betalingsforslaget er en forespørgsel, der bruges til at vælge fakturaer til betaling. Du kan redigere listen over fakturaer, der skal betales, før du opretter eller genererer kreditorbetalingerne.  
8. Vælg fakturaer til betaling efter forfaldsdato, kasserabat eller begge dele. 
9. Indtast datoen for at sammenligne med forfaldsdatoen eller kasserabatten. 
10. Valgfrit: Angiv en betalingsdato, der bruges til alle betalinger.
    * Den dato, der angives her, bliver betalingsdatoen for alle de betalinger, der er oprettet, uanset forfaldsdato eller kasserabatdatoen.  
11. Valgfrit: Angiv en dato for minimumsbetaling der kan anvendes som betalingsdato.
    * Dato for minimumsbetaling bliver den tidligste dato, der blev brugt, da betalingerne blev oprettet. Hvis en faktura f.eks. har en forfaldsdato, der efter datoen for minimumsbetaling, bliver forfaldsdatoen betalingsdatoen i stedet for datoen for minimumsbetaling, så fakturaen betales på den seneste mulige dato.  
12. Angiv ekstra forespørgselsrestriktioner under Poster, der skal medtages.
    * Filteret bruges ofte til at begrænse de fakturaer, der er udvalgt til betaling efter kreditorgruppe eller betalingsmåde. For eksempel kan du tilføje et filter for kun at betale fakturaer ved indtjekning af denne kørsel af betaling.  
13. Angiv yderligere forespørgselsrestriktioner eller betalingsstandarder. 
    * Yderligere parametre kan bruges til at definere betalingsvalutaen eller aktiverer centraliserede betalinger for denne lønkørsel.  
14. Klik på OK.
    * Når du klikker på OK, vises resultaterne af forespørgslen. Hvis du ikke vil have vist listen over fakturaer, der er valgt til betaling, kan du gå tilbage til oversigtspanelet Parametre og ændre indstillingen Opret betalinger uden projektfaktura = Ja.  
15. Vælg knappen Vis oversigt over betalinger for at få vist de betalinger, der oprettes for kreditoren i den valgte faktura.
16. Vælg Skjul oversigt over betalinger for at skjule betalingerne. 
17. Klik på Opret betalinger.
    * Før du vælger Opret betalinger, kan du højreklikke på gitteret og eksportere listen over fakturaer til Excel. Knappen Opret betalinger opretter kreditorbetalinger i betalingskladden.  
18. Scan dine betalinger, og sørg for, at betalingsmåden er defineret for alle betalinger. 
    * Hvis du genererer betalinger, såsom at udskrive en check eller oprette en elektronisk betaling, skal betalingsmåden defineres. Betalingsmåden vælger også som standard den bankkonto, hvorfra betalingen foretages.  
19. Klik på Ny for at oprette en engangsbetalings.
    * En engangsbetaling kan føjes til en betalingskladde når som helst før bogføringen. Dette gøres ved at klikke på knappen Ny og derefter tilføje betalingsoplysningerne manuelt frem for at bruge Betalingsforslaget.  
20. Vælg den kreditor, som betalingen skal foretages til.
21. Hvis der findes en faktura til betaling, skal du vælge Udlign transaktioner for at vælge fakturaen til betaling.
    * Hvis dette er en forudbetaling, er dette trin valgfrit. Du kan oprette betalingen uden at vælge nogen faktura.  
22. Markér de fakturaer, der skal betales.
    * Hvis du bruger Udlign transaktioner til at vælge fakturaer til betaling, beregnes betalingsbeløbet automatisk baseret på de fakturaer, du markerer til betaling, og det beløb du indtaster i Beløb, der skal udlignes.  
23. Klik på OK.
24. Hvis du vil slette en betaling, skal du markere rækken.
25. Klik på Slet.
    * Sletning af en betaling sletter kun betalingen. Fakturaer markeret til betaling vil stadig være tilgængelige for betaling af en anden betaling.  
26. Klik på Ja.
27. Vælg Generer betaling for at udskrive checks eller oprette den elektroniske betalingsfil.
28. Vælg den betalingsmåde, du vil generere.
    * Betalingskladden kan indeholde betalinger til både checks og elektroniske betalinger, men du kan kun oprette én betalingstype ad gangen.  
29. Vælg den bankkonto, hvorfra du vil generere betalinger.
30. Klik på OK.
    * Betalinger kan kun oprettes for betalinger, der svarer til den betalingsmåde og bankkonto, du har valgt.  
31. Hvis du genererer checks, skal du vælge Dokument for at sikre den korrekte printerdestination for checkene.
32. Klik på OK.
33. Klik på OK for at generere betalingerne.
34. Klik på Bogfør, hvis alle betalingerne er godkendte og genererede. 


