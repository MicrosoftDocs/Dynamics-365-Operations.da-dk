---
title: Lager, luk
description: Som en del af processen til at udligne afgangsposteringerne med tilgangsposteringer, kan du også vælge at have Finans opdateret for at afspejle de justeringer, der er foretaget.
author: AndersGirke
manager: AnnBe
ms.date: 10/24/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventClosing
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 61973
ms.assetid: c210c882-6849-4704-b78c-a777dd6cfdb6
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: a705853ea27d117c99a00893b862348bbac0b9b0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1560777"
---
# <a name="inventory-close"></a>Lager, luk

[!include [banner](../includes/banner.md)]

Som en del af processen til at udligne afgangsposteringerne med tilgangsposteringer, kan du også vælge at have Finans opdateret for at afspejle de justeringer, der er foretaget.

Under processen til lagerlukning udlignes afgangsposteringer i forhold til tilgangsposteringer på baggrund af den metode til lagerværdi, der er valgt i varens varemodelgruppe. Som et led i udligningsprocessen kan du angive, at finansmodulet skal opdateres, så det afspejler de justeringer, der er foretaget. Indtil der er kørt lagerlukning og genberegning, bogføres afgangsposteringer dog til den beregnede løbende gennemsnitskostpris. 

Når der er kørt lagerlukning, kan du ikke længere bogføre i perioder, der ligger før den dato for lagerlukning, du angiver, medmindre du tilbagefører en fuldført lagerlukningsproces. Hvis der f.eks. køres lagerlukning for den periode, der slutter den 31. januar, kan du bogføre posteringer, der har en dato, der ligger før den 31. januar. 

Varer på lageret knyttes til en af to lagertyper: vare eller tjeneste. Lagerlukningen udfører de samme funktioner for begge typer. Men for servicevarer, udligner lagerlukningen stadig afgange med tilgange. 

Hvor ofte lagerlukningsprocessen kører, varierer fra virksomhed til virksomhed. Omfanget af transaktioner kan dog give et fingerpeg om, hvor ofte du skal køre lagerlukning. Generelt kører de fleste firmaer lagerlukning som en del af deres procedurer til lukning og afstemning ved månedens slutning.

## <a name="inventory-recalculation-and-the-general-ledger"></a>Lagergenberegning og finansmodulet
Hvis der skal foretages reguleringer af lageret og finansmodulet i løbet af en måned eller anden lagerperiode, kan du køre lagergenberegning eller lagerlukning i stedet. Under lagergenberegning sker der reguleringer, men ikke udligninger, af lagerposteringer. 

Under lagergenberegning bliver disponibel lagerbeholdning reguleret, lagertransaktioner justeres og genberegningen af lageret og lukning af lager køres. Disse opgaver påvirker alle finanskonti, der er knyttet til den oprindelige lagerpostering. 

**Eksempel** 

Når du opretter en indkøbsordre fra en salgsordre, bliver de finanskonti, der blev brugt til den oprindelige salgsordre, opdateret. Selvom finanskonti for den varegruppe, der er tildelt varen, blev ændret, efter at salgsordren er bogført, og en genberegning af lageret oprettede et reguleringsbeløb, bogføres justeringsbeløbet på de oprindelige finanskonti. Det regulerede beløb bogføres ikke til de nye finanskonti, der er knyttet til varen. 

Når opdateringen er fuldført, kan du gennemse det finansbilag, der er bogført som følge af en af disse opgaver.

1.  På siden **Lukning og regulering** skal du under fanen **Oversigt** vælge den opdatering, du vil gennemgå.
2.  Klik på **Detaljer**, og vælg derefter **Bilag**.

## <a name="effects-of-the-inventory-close-process-on-the-general-ledger"></a>Virkningerne af lagerlukningsprocessen i Finans
Flere af de opgaver, du kan udføre på siden **Lukning og regulering**, kan medføre en opdatering af finansmodulet. Eksempelvis opdateres finansmodulet, når du regulerer disponibel lagerbeholdning, regulerer lagertransaktioner, kører genberegning af lageret og lukker lageret. 

De finanskonti, der opdateres på grund af disse opgaver, er knyttet til den oprindelige lagerpostering. Hvis en salgsordre f.eks. afregnes med en indkøbsordre, bliver de finanskonti, der blev brugt til den oprindelige salgsordre, justeret. Funktionsmåden anvendes også, selvom finanskontiene for den varegruppe, der er tildelt varen, er ændret, siden salgsordren blev bogført. Når lagerlukningen opretter et udligningsbeløb, bogføres udligningsbeløbet stadig på de oprindelige finanskonti, og ikke på de nye finanskonti, som er tildelt til varen. Finansmodulet kan også opdateres, hvis du tilbagefører en lagerlukning. 

**Bemærkninger:**

-   Lagerlukning er ikke påkrævet, hvis du bruger metoden til evaluering af standardomkostninger.
-   Før du kører lukningsproceduren, kan du se en liste over varer, der ikke kan udlignes under opdateringen.
-   Det anbefales, at du kører lagerlukning i løbet af de mindst belastede timer for at fordele computerressourcerne så jævnt som muligt.

## <a name="the-inventory-close-log"></a>Få vist log for lagerlukning
Når lagerlukningen er udført, vises der evt. en meddelelse i meddelelsescentret om, at en enhedskostpris muligvis ikke er korrekt, fordi en postering ikke kunne udlignes helt. 

Før denne meddelelse vises, rapporterer systemet varenummeret og den berørte postering. Meddelelsen fortæller dig, at det kostbeløb, der bruges til denne postering, ikke blev opdateret på grund af lagerlukningen. Denne meddelelse vises, når en postering af typen afgang ikke kan udlignes. 

Under lagerlukningen kontrollerer systemet automatisk hver økonomisk dimension for at se, om der er flere afgange end tilgange frem til den angivne slutdato. Denne form for ubalance kan forekomme, når en lagertransaktion fra en indkøbsordre ikke er posteret fuldt ud økonomisk, fordi kreditorfakturaen endnu ikke er modtaget, eller fordi styklistekomponenter, der er medtaget i en produktion på et højere niveau, ikke er økonomisk bogført. (Underproduktionen kostprisberegnes ikke). I dette tilfælde vil den efterfølgende lukning ikke regulere alle afgange efter den korrekte kostpris, fordi der ikke er nok tilgangsoplysninger tilgængelige. 

For hver kørsel af lukningsproceduren angiver systemet, om en logfil, der indeholder advarsler, er gemt og kan ses. 

Hvis du får vist mange advarsler i meddelelsen, anbefales det, at du udfører følgende handlinger:

-   Foretag økonomisk opdatering af tilgange.
-   Udskyd slutdatoen.
-   Genovervej forretningsprocedurerne.

I nogle tilfælde kan du muligvis ikke gøre noget ved advarslerne. Hvis der f.eks. anvendes markering, og den markerede indkøbsordre har en økonomisk dato, der ligger efter slutdatoen, kan slutdatoen ikke ændres.

## <a name="reversing-a-completed-inventory-close"></a>Tilbageførsel af en fuldført lagerlukning
Nogle gange kan det være nødvendigt at tilbageføre en afsluttet lagerlukning for at ændre udligninger til den tilstand, de var i, før reguleringerne blev foretaget. Når du tilbagefører en afsluttet lagerlukning, åbnes lageret også igen for at gøre det muligt at bogføre i den periode, lagerlukningen dækker. Relaterede ændringer kan også foretages i Finans. Når du er færdig med at foretage justeringer, kan du køre lagerlukningen igen for den periode, du arbejder med. 

**Bemærk!** Det er kun den sidste lagerperiode, der blev lukket, som kan åbnes igen. Hvis du vil tilbageføre en tidligere lagerlukning, skal du tilbageføre hver efterfølgende lagerlukning for sig, og du skal starte med den seneste lukning.



