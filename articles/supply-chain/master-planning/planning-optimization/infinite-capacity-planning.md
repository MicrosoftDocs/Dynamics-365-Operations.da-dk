---
title: Planlægning med uendelig kapacitet
description: Dette emne indeholder oplysninger om planlægning med uendelig kapacitet for planlægningsoptimering. Det beskriver også de aktuelle funktionsbegrænsninger.
author: crytt
ms.date: 6/9/2021
ms.topic: article
ms.search.form: RouteInventProd
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-06-09
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fc40dc2bcf1969e4c566b624a9425638e69ab2a17892f035aeabb74068aadd14
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6718966"
---
# <a name="scheduling-with-infinite-capacity"></a>Planlægning med uendelig kapacitet

[!include [banner](../../includes/banner.md)]
[!INCLUDE [preview-banner](../../includes/preview-banner.md)]

Funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* introducerer en planlægning, der er baseret på ruteoplysninger. Det giver dig mulighed for at planlægge job ud fra en lang række ruteopsætninger. Planlægning for planlægningsoptimering dækker ofte anvendte ruteindstillinger, herunder rækkefølgen af ruteoperationer eller krav til ruteoperationsressourcer.

## <a name="turn-on-the-infinite-capacity-scheduling-feature"></a>Aktivere funktionen til planlægning med uendelig kapacitet

Hvis systemet ikke allerede indeholder den funktion, der er beskrevet i dette emne, skal du åbne arbejdsområdet [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering*.

## <a name="added-functionality"></a>Tilføjet funktonalitet

Funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* muliggør finplanlægning, der er baseret på ruteoplysninger. Derfor kan en ruteopsætning bruges til at planlægge produktionsprocesser. Selvom denne funktion har visse begrænsninger, som den indbyggede varedisponering ikke har, understøtter den de mest almindelige funktioner, der kræves til fremstillingsscenarier.

Denne funktion tager både højde for *simple ruter* og *rutenetværk*. Ved at bruge feltet **Næste** på en ruteoperation kan du konfigurere komplekse ruter med flere startpunkter og flere operationer, der kører parallelt. Systemet tager højde for komplekse rutestrukturer af denne type under planlægning.

Funktionen understøtter desuden *parallelle operationer* i ruter. Hvis du bruger indstillingerne *Primær* og *Sekundær* i feltet **Prioritet** på ruteoperationer, kan du definere en rutestruktur, hvor én ruteoperation er den primære operation, og en anden operation er den sekundære. I dette tilfælde tager systemet højde for rutestrukturer under planlægning.

Under planlægningsprocessen tager systemet også højde for de *ressourcekrav*, der er angivet for en operation. Systemet bruger ressourcekrav til at bestemme, hvilke ressourcer der kræves for at udføre operationen. Aktuelt understøtter funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* følgende typer ressourcekrav:

- Ressourcetype
- Ressource
- Ressourcegruppe
- Egenskab

> [!NOTE]
> Krav, der er relateret til personale, for eksempel kompetencer eller certifikatkrav, understøttes ikke endnu.

Funktionen understøtter også de operationelle egenskaber **Opstillingstid** og **Kørselstid**. Når du angiver disse egenskaber i en ruteoperation, opretter planlægningsprocessen de relevante opstillings- og procesjob.

Kort sagt understøtter planlægning for planlægningsoptimering de scenarier, der anvendes oftest. Du kan oprette ruten, tilføje primære og sekundære operationer, definere næste operationer, tilføje ressourcekrav og tilføje opstillingstid og kørselstid. Der tages derefter højde for disse oplysninger under planlægningen.

## <a name="limitations"></a>Begrænsninger

Der gælder følgende begrænsninger, når du bruger planlægning til planlægningsoptimering:

- Funktionen understøtter kun finplanlægning. Der tages ikke højde for indstillinger, der er relateret til grovplanlægning, under planlægningen, uanset planlægningsmetoden i behovsplanerne.
- Funktionen understøtter kun uendelig kapacitet.
- Funktionen understøtter ikke funktioner til ressourcebelastning.
- Funktionen tager ikke højde for rutespild.
- Funktionen understøtter kun *Varighed* som det primære ressourcevalg.

Bemærk, at funktionen *Planlægning med uendelig kapacitet for planlægningsoptimering* forbedres løbende. Microsoft forventer at introducere understøttelse af flere planlægningsindstillinger i fremtidige versioner.
