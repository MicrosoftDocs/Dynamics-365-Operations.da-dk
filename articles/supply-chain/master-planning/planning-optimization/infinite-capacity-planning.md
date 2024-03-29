---
title: Planlægning med uendelig kapacitet
description: Denne artikel indeholder en beskrivelse af uendelig kapacitetsplanlægning. Det beskriver også de aktuelle funktionsbegrænsninger.
author: t-benebo
ms.date: 08/09/2022
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 7249734e5d2644145a36276dbc818a40b5962805
ms.sourcegitcommit: 491ab9ae2b6ed991b4eb0317e396fef542d3a21b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/03/2022
ms.locfileid: "9739999"
---
# <a name="scheduling-with-infinite-capacity"></a>Planlægning med uendelig kapacitet

[!include [banner](../../includes/banner.md)]

Funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* introducerer en planlægning, der er baseret på ruteoplysninger. Det giver dig mulighed for at planlægge job ud fra en lang række ruteopsætninger. Planlægning dækker ofte anvendte ruteindstillinger, herunder rækkefølgen af ruteoperationer eller krav til ruteoperationsressourcer.

## <a name="turn-the-infinite-capacity-scheduling-feature-on-or-off"></a>Slå funktionen til planlægning med uendelig kapacitet til eller fra

Før du kan bruge denne funktion, skal den være aktiveret i dit system. Fra og med Supply Chain Management version 10.0.29 er funktionen som standard aktiveret. Administratorer kan aktivere eller deaktivere denne funktion ved at søge efter funktionen *Uendelig kapacitetsplanlægning til planlægningsoptimering* i arbejdsområdet [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

Yderligere oplysninger om denne funktion finder du i [Planlægning med ressourcevalg baseret på egenskab](capability-based-scheduling.md).

## <a name="added-functionality"></a>Tilføjet funktonalitet

Funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* muliggør finplanlægning, der er baseret på ruteoplysninger. Derfor kan en ruteopsætning bruges til at planlægge produktionsprocesser. Selvom denne funktion har visse begrænsninger, som det udfasede varedisponeringsprogram ikke har, understøtter den de mest almindelige funktioner, der kræves til fremstillingsscenarier.

Denne funktion tager både højde for *simple ruter* og *rutenetværk*. Ved at bruge feltet **Næste** på en ruteoperation kan du konfigurere komplekse ruter med flere startpunkter og flere operationer, der kører parallelt. Systemet tager højde for komplekse rutestrukturer af denne type under planlægning.

Funktionen understøtter desuden *parallelle operationer* i ruter. Hvis du bruger indstillingerne *Primær* og *Sekundær* i feltet **Prioritet** på ruteoperationer, kan du definere en rutestruktur, hvor én ruteoperation er den primære operation, og en anden operation er den sekundære. I dette tilfælde tager systemet højde for rutestrukturer under planlægning.

Under planlægningsprocessen tager systemet også højde for de *ressourcekrav*, der er angivet for en operation. Systemet bruger ressourcekrav til at bestemme, hvilke ressourcer der kræves for at udføre operationen. Aktuelt understøtter funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* følgende typer ressourcekrav:

- Ressourcetype
- Ressource
- Ressourcegruppe
- Egenskab (Yderligere oplysninger finder du i [Planlægning med ressourcevalg baseret på egenskab](capability-based-scheduling.md).)

> [!NOTE]
>
> - Hvis ressourcen og/eller ressourcegruppen er indstillet til ubegrænset kapacitet, vil varedisponeringen betragte dem som ubegrænset kapacitet.
> - Krav, der er relateret til personale, for eksempel kompetencer eller certifikatkrav, understøttes ikke endnu.

Funktionen understøtter også de operationelle egenskaber **Opstillingstid** og **Kørselstid**. Når du angiver disse egenskaber i en ruteoperation, opretter planlægningsprocessen de relevante opstillings- og procesjob.

Kort sagt understøtter planlægning de scenarier, der anvendes oftest. Du kan oprette ruten, tilføje primære og sekundære operationer, definere næste operationer, tilføje ressourcekrav og tilføje opstillingstid og kørselstid. Der tages derefter højde for disse oplysninger under planlægningen.

## <a name="limitations"></a>Begrænsninger

Der gælder følgende begrænsninger, når du bruger *Uendelig kapacitetsplanlægning til planlægningsoptimering*:

- Funktionen understøtter kun uendelig kapacitet.
- Funktionen understøtter ikke funktioner til ressourcebelastning.
- Funktionen tager ikke højde for rutespild.
- Funktionen understøtter kun *Varighed* som det primære ressourcevalg.
