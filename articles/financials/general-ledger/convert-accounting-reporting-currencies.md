---
title: Omregne regnskabs- eller rapporteringsvalutaer
description: "Et firma, der skal ændre sin regnskabsvaluta eller rapporteringsvaluta, har to muligheder."
author: aprilolson
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 78223
ms.assetid: 31c56f9a-9c64-40a2-90e3-1969a760614b
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: ad840f4ed2cf27615e699a13fcd8be7f3c2cd5c8
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="convert-accounting-or-reporting-currencies"></a>Omregne regnskabs- eller rapporteringsvalutaer

[!INCLUDE [banner](../includes/banner.md)]

Et firma, der skal ændre sin regnskabsvaluta eller rapporteringsvaluta, har to muligheder. Den første mulighed er at oprette en ny virksomhed og starte forfra. Den anden mulighed er at køre processen til omregning af regnskabs- og rapporteringvaluta. Dette er en meget langvarig proces, der ændrer alle transaktioner i systemet. Før du kan køre processen, kræves der yderligere konfiguration.

## <a name="preparing-the-legal-entity-for-currency-conversion"></a>Forberede den juridiske enhed til en valutaomregning
Inden du kan omregne den juridiske enheds valuta, skal du gendanne alle beløb for værdiregulering af udenlandsk valuta til debitor- og kreditorkonti og lukke tidligere regnskabsår. Du skal også forberede databasen til omregning og foretage de nødvendige ændringer af kontoen i den juridiske enhed, som valutaomregningen skal foretages for. Når du har fuldført en valutaomregning, skal du udføre nogle ekstra procedurer. Du skal afstemme afrundingsdifferencer i omregnede beløb, genberegne handelsstatistik, journalisere finansposteringerne, begrænse adgangen til omregningsværktøjet og værdiregulere beløb i udenlandsk valuta for debitor-og kreditorkonti.

## <a name="setting-up-accounts-for-automatic-transactions"></a>Konfigurere konti til automatiske posteringer
Under processen til omregning af valuta bogøres gevinster eller tab eller øredifferencer på de konti, der er defineret på siden **Konti til automatisk posteringer**. Hovedkonti skal være tildelt følgende typer transaktion, før konverteringen køres:

-   Omregningsoverskud i regnskabsvaluta
-   Omregningsunderskud i regnskabsvaluta
-   Øredifference i regnskabsvaluta
-   Øredifference i rapporteringsvaluta
-   Årets resultat

## <a name="posting-rounding-differences-and-sum-recalculations"></a>Bogføre afrundingsdifferencer og genberegning af summer
Følgende oplysninger forklarer, hvor der kan forekomme differencer ved afrunding:

-   Hvis produktpriser er omregnet til 0 (nul), oprettes der en rapport, som viser produktnummeret, modultypen, prisen før omregningen og enheden.
-   Afrundingsdifferencer, der opstår mellem moms og finansmodulet, bogføres i finanskladden.
-   Værdireguleringsbeløb i udenlandsk valuta genberegnes, og debitor- og kreditorposteringsbeløb genberegnes.
-   Der oprettes debitor- og kreditorudligningsposter til afrundingsdifferencerne for hver debitor- og kreditorpostering.
-   Afrundingsdifferencer for debitorer og kreditorer bogføres i finanskladden.
-   Udligningskostbeløb og omkostningsreguleringsbeløb i lukkede lagerposteringer genberegnes.
-   Afrundingsdifferencer i Lagerstyring bogføres i finanskladden.
-   Den disponible lagerbeholdning genberegnes.
-   De samlede beløb i finanskladderne efterberegnes.
-   Afslutningsarkene i Finans efterberegnes.
-   Finanssaldiene efterberegnes.
-   Afrundingsdifferencer i Finans bogføres i finanskladden.
-   Primoposterne i Finans efterberegnes.
-   Slutbeløbet i finanssaldiene beregnes.

Hvis du konverterer til en ny finansregnskabsvaluta, og der er opstået en fejl i efterberegningen af de samlede beløb eller i bogføringen af afrundingsdifferencerne, skal du lukke siden **Valutaomregning for finanskonti**. De samlede beløb efterberegnes, og afrundingsdifferencerne bogføres.

## <a name="processing-the-currency-conversion"></a>Behandle valutaomregningen
Når du starter omregningsprocessen for valuta, skal alle brugere være logget af systemet. Du skal definere den nye regnskabs- eller rapporteringsvaluta og valutakurserne. Når du klikker på **OK**, kører processen kører, og alle transaktioner i systemet opdateres. Valutaomregning er en meget langvarig proces. Når den er fuldført, kan du se, at regnskabs- eller rapporteringsvalutaen er opdateret på siden **Finans**.

## <a name="completing-the-currency-conversion"></a>Fuldføre valutaomregningen
Efter valutaomregningen skal du generere alle afstemningsrapporter igen for at sikre, at alle omregnede beløb er korrekte.

-   Hvis omregning af finansregnskabsvalutaen medfører afrundingsdifferencer, bogføres disse differencer ikke ved hjælp af det bilag, hvor afrundingsdifferencen er opstået. Differencer bogføres i stedet ved hjælp af det registrerede bilag for omregningsposteringer. Efter omregningen inkluderer alle rapporter, der kontrollerer bilag og dato, derfor disse afrundingsdifferencer. Denne funktionsmåde er korrekt og kan ignoreres.
-   Hvis debitor- og kreditorafstemningsrapporterne viser et differencebeløb på totallinjen, og der ikke var et differencebeløb før omregningen, skal dette differencebeløb bogføres. Kontoen er samlekontoen for debitorer og kreditorer. Modkontoen er finanskontoen for omregningsunderskud eller omregningsoverskud.

Når alle finansposteringskladder er slettet, kan du journalisere finansposteringerne. Klik på **Finans** &gt; **Periodisk** &gt; **Kladder** &gt; **Journalisering**. Du kan værdiregulere beløb i udenlandsk valuta efter valutaomregningen, hvis værdireguleringen er påkrævet. Du kan værdiregulere beløb i udenlandsk valuta ved at vælge **Standard** i feltet **Metode** for værdireguleringen.

Yderligere oplysninger finder du i [Journaliser bogførte kladdeposteringer](tasks/journalize-posted-journal-entries.md).


