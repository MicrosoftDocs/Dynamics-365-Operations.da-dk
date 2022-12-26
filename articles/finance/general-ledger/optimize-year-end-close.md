---
title: Optimer årsafslutning
description: I denne artikel beskrives tilføjelsesprogrammet Optimer årsslutning, der er tilgængeligt for processen til afslutning af finansår.
author: moaamer
ms.date: 12/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerClosingSheet
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14091
ms.assetid: c64eed1d-df17-448e-8bb6-d94d63b14607
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2022-11-28
ms.dyn365.ops.version: AX 10.0.0
ms.openlocfilehash: bc6ab7e36f37707442f8d5d5b6e0d5f5d42e2171
ms.sourcegitcommit: 0c927fcb3afd34d870391f05b5393a4673d916e5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/08/2022
ms.locfileid: "9831523"
---
# <a name="optimize-year-end-close"></a>Optimer årsafslutning 

Tilføjelsesprogrammet Optimer årsafslutning til Microsoft Dynamics 365 Finance gør det muligt at køre årsafslutning uden for forekomsten af AOS (Application Object Server) til Dynamics 365 Finance-ressourcer. Det bruger mikroserviceteknologi. De fordele, der er tilknyttet funktionen Optimer årsafslutning, omfatter forbedret ydeevne og minimal påvirkning af SQL-databasen under kørsel af årsafslutning.

>[!NOTE]
> Den optimerede årsslutslut er tilgængelig på Microsoft Dynamics 365 Finance version 10.0.31. Denne funktion er blevet tilbageporteret til Dynamics Finance versions 10.0.30 og 10.0.29, og du skal tage den seneste kvalitetsopdatering.   

Hvis du vil bruge funktionen Optimer årsafslutning, skal du udføre følgende opgaver:

1. Installer tilføjelsesprogrammet Optimer årsafslutning fra dit projekt i Microsoft Dynamics Lifecycle Service.
2. Aktivér funktionen **Optimer årsafslutning** i Funktionsstyring.

> [!NOTE]
> Du kan stadig bruge den aktuelle funktion til årsafslutning for Finance ved at deaktivere funktionen **Optimer årsafslutning** i Funktionsstyring.

## <a name="improved-performance"></a>Forbedret ydeevne

Funktionen **Optimer årsafslutning** er udviklet til at sætte skub i årsafslutningsbehandlingen, specielt for kunder, der har store mængder data. Når årsafslutning kører på en tjeneste, udlæses den tunge behandling fra Finance-ressourcer for at reducere behandlingstiden og frigøre de ressourcer, der kan påvirke andre brugeres daglige drift.

Funktionen **Optimer årsafslutning** kan hjælpe dig med at nå følgende mål:

- Forbedret ydeevne af årsafslutningen ved at reducere kørselstiden.
- Reducere indvirkningen på andre processer under kørslen af årsafslutning.
- Forbedre rapportering og reguleringer af årets resultater, da kørslen af årsafslutning tager mindre tid.

## <a name="new-options-and-visibility"></a>Nye muligheder og synlighed

Når funktionen **Optimer årsafslutning** er aktiveret, tilføjes de to nye kolonner, **Resultater** og **Status**, følgende steder:

- På siden **Årsafslutning**
- I dialogboksen **Resultater af årsafslutning**
- I indstillingerne **Saldo for overførsel af økonomisk dimension** på siden **Skabelon til årsafslutning**

I følgende illustration vises et eksempel på kolonnerne **Resultat** og **Status** på siden **Årsafslutning**. Du kan vælge linket **Vis resultater** i kolonnen **Resultater** for at åbne resultaterne af årsafslutningen. Kolonnen **Status** viser den aktuelle tilstand af årsafslutningsprocessen. De nye kolonner giver derfor mulighed for at se, hvordan årsafslutningsprocessen skrider frem.

[![Resultater- og Status-kolonner på årsafslutningssiden.](./media/Optimize-year-end-close-Image3.png)](./media/Optimize-year-end-close-Image3.png)

Når funktionen til **Optimer årsafslutning** er aktiveret, bliver oversigtspanelet **Økonomiske dimensioner for balance** tilgængeligt på siden **Skabelon til årsafslutning**. Du kan bruge dette oversigtspanel til at angive økonomiske dimensioner for balance, når du lukker et år. Denne egenskab er parallel med den egenskab, der allerede er tilgængelig for driftskonti.

[![Oversigtspanel for økonomiske dimensioner for balance](./media/Optimize-year-end-close-Image4.png)](./media/Optimize-year-end-close-Image4.png)

## <a name="architecture-and-data-flow"></a>Arkitektur og dataflow

Hvis du vil bruge funktionen **Optimer årsafslutning** og køre årsafslutningen på en mikroservice, skal du installere tilføjelsesprogrammet **Optimer årsafslutning fra Lifecycle Services** og derefter aktivere funktionen **Optimer årsafslutning** i Funktionsstyring.

Som følgende illustration viser, kontrollerer behandlingen af årsafslutning, at tilføjelsesprogrammet er installeret, og at funktionen er aktiveret. Hvis begge forudsætninger er opfyldt, køres årsafslutningen på mikroservicen.

[![Dataflowdiagram.](./media/Optimize-year-end-close-Image5.png)](./media/Optimize-year-end-close-Image5.png)

## <a name="high-level-flow-for-year-end-close-processing"></a>Flow på højt niveau for behandling af årsafslutning

1. Årsafslutningen starter i Finance ved **Finans \> Luk periode \> Årsafslutning**. Processen opretter lukning af batchjob og opgaver for de juridiske enheder, der lukkes.
2. Årsafslutningen bestemmer, om årsafslutningen skal køres på mikroservicen eller på den aktuelle lukkelogik.

    - Hvis tilføjelsesprogrammet **Optimer årsafslutning** er installeret i Lifecycle Services, og funktionen **Optimer årsafslutning** er aktiveret i Funktionsstyring, køres årsafslutningen på mikroservicen.

        1. Funktionen Optimer årsafslutning opretter et servicejob for årsafslutning for hver juridiske enhed, der lukkes, og kører derefter årsafslutningslogikken. Mikroservicen udfører årsafslutningen.
        2. Finance lytter til årsafslutningen på mikroservicen for at finde ud af, hvornår mikroservicen er færdig. Resultaterne af årsafslutningen opdateres derefter på siden **Årsafslutning** i Finance.

    - Ellers køres årsafslutningen på den aktuelle lukkelogik.
