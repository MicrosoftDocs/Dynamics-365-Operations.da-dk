---
title: Planlægning med uendelig kapacitet
description: Dette emne indeholder oplysninger om planlægning med uendelig kapacitet for planlægningsoptimering. Det beskriver også de aktuelle funktionsbegrænsninger.
author: crytt
ms.date: 09/21/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: 10.0.22
ms.openlocfilehash: 9e1e423aaed06f6bb2b42e27d41c2aef46ffe104
ms.sourcegitcommit: b5f2d88ff4e0a234fa6b9ee33516425e54ff2c3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/21/2021
ms.locfileid: "7506801"
---
# <a name="scheduling-with-infinite-capacity"></a>Planlægning med uendelig kapacitet

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* introducerer en planlægning, der er baseret på ruteoplysninger. Det giver dig mulighed for at planlægge job ud fra en lang række ruteopsætninger. Planlægning for planlægningsoptimering dækker ofte anvendte ruteindstillinger, herunder rækkefølgen af ruteoperationer eller krav til ruteoperationsressourcer.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Aktivere funktionen til planlægning med uendelig kapacitet

Før du kan bruge denne funktion, skal den være slået til i dit system. Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til. I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:

- **Modul:** *Varedisponering*
- **Funktionsnavn:** *Uendelig kapacitetsplanlægning til Planlægningsoptimering*

Yderligere oplysninger om denne funktion finder du i [Planlægning med ressourcevalg baseret på egenskab](capability-based-scheduling.md).

## <a name="added-functionality"></a>Tilføjet funktonalitet

Funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* muliggør finplanlægning, der er baseret på ruteoplysninger. Derfor kan en ruteopsætning bruges til at planlægge produktionsprocesser. Selvom denne funktion har visse begrænsninger, som den indbyggede varedisponering ikke har, understøtter den de mest almindelige funktioner, der kræves til fremstillingsscenarier.

Denne funktion tager både højde for *simple ruter* og *rutenetværk*. Ved at bruge feltet **Næste** på en ruteoperation kan du konfigurere komplekse ruter med flere startpunkter og flere operationer, der kører parallelt. Systemet tager højde for komplekse rutestrukturer af denne type under planlægning.

Funktionen understøtter desuden *parallelle operationer* i ruter. Hvis du bruger indstillingerne *Primær* og *Sekundær* i feltet **Prioritet** på ruteoperationer, kan du definere en rutestruktur, hvor én ruteoperation er den primære operation, og en anden operation er den sekundære. I dette tilfælde tager systemet højde for rutestrukturer under planlægning.

Under planlægningsprocessen tager systemet også højde for de *ressourcekrav*, der er angivet for en operation. Systemet bruger ressourcekrav til at bestemme, hvilke ressourcer der kræves for at udføre operationen. Aktuelt understøtter funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* følgende typer ressourcekrav:

- Ressourcetype
- Ressource
- Ressourcegruppe
- Egenskab (Yderligere oplysninger finder du i [Planlægning med ressourcevalg baseret på egenskab](capability-based-scheduling.md).)

> [!NOTE]
> Krav, der er relateret til personale, for eksempel kompetencer eller certifikatkrav, understøttes ikke endnu.

Funktionen understøtter også de operationelle egenskaber **Opstillingstid** og **Kørselstid**. Når du angiver disse egenskaber i en ruteoperation, opretter planlægningsprocessen de relevante opstillings- og procesjob.

Kort sagt understøtter planlægning for planlægningsoptimering de scenarier, der anvendes oftest. Du kan oprette ruten, tilføje primære og sekundære operationer, definere næste operationer, tilføje ressourcekrav og tilføje opstillingstid og kørselstid. Der tages derefter højde for disse oplysninger under planlægningen.

## <a name="limitations"></a>Begrænsninger

Der gælder følgende begrænsninger, når du bruger planlægning til planlægningsoptimering:

- Funktionen understøtter kun uendelig kapacitet.
- Funktionen understøtter ikke funktioner til ressourcebelastning.
- Funktionen tager ikke højde for rutespild.
- Funktionen understøtter kun *Varighed* som det primære ressourcevalg.

Bemærk, at funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* forbedres løbende. Microsoft forventer at introducere understøttelse af flere planlægningsindstillinger i fremtidige versioner.
