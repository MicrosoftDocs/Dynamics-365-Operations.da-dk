---
title: Frigivelsesproces og frigivelseshistorik for Planlægningsoptimering
description: Dette emne indeholder oplysninger om frigivelsesprocessen og frigivelseshistorikken for Planlægningsoptimering.
author: crytt
ms.date: 09/02/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: d0f7a9f59d1034451c5c2dec1150c017bda27ad4
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7474694"
---
# <a name="planning-optimization-release-process-and-release-history"></a>Frigivelsesproces og frigivelseshistorik for Planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Microsoft opdaterer Planlægningsoptimering på månedsbasis. Men på baggrund af forretningsbehov frigiver vi fra tid til anden flere opdateringer mellem de planlagte frigivelser.

Hver frigivelse udgives i de individuelle områder, hvor Planlægningsoptimering er tilgængelig. Det tager typisk tre dage at behandle processen.

Mens Planlægningsoptimering opdateres, kan varedisponering køre en smule langsommere end normalt.

Miljøer, der bruger Planlægningsoptimering, modtager automatisk den seneste version. Der kræves ingen brugerhandling: Tjenesten opdateres automatisk. Men ingen større funktionsændring overføres automatisk til miljøer. Ændringer, der betragtes som større, er som standard deaktiverede, og de skal aktiveres direkte ved hjælp af [funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md). Derfor vil ændringerne ikke blive vist i miljøet, før du har aktiveret dem.

Da der ikke vises beskeder, når Planlægningsoptimering opdateres i dit miljø, kan du gennemse produktbemærkningerne i følgende tabel for at finde ud af, hvornår ændringerne blev frigivet, og hvilke funktioner de introducerede. Denne tabel viser de ændringer, der er frigivet til Planlægningsoptimering, om disse ændringer er knyttet til en funktion fra funktionsstyring og datoen for frigivelsen.

| Ændringer | Detaljer om funktionsstyring | Udstedelsesdatoer |
|---|---|---|
| Generelle forbedringer af ydeevne, kvalitet og stabilitet. | Der kræves ingen funktionsstyring. | 25 - 30 august 2021 |
| <p>Har tilføjet feltet **Leveringstid** til ordreforslag.</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet.</p> | Der kræves ingen funktionsstyring. | 12 - 17 august 2021 |
| <p>Tilføjet ressourcetypekrav for planlægning med ubegrænset kapacitet.</p><p>Forbedret ressourceeffektivitet og kalendereffektivitet for planlægning med ubegrænset kapacitet.</p><p>Yderligere oplysninger finder du under [Planlægning med ubegrænset kapacitet](infinite-capacity-planning.md). | <p>Tilgængelig i funktionsstyring fra og med version 10.0.20.</p><p>Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering*</p> | 6 - 12 juli 2021 |
| Generelle forbedringer af kvalitet. | Der kræves ingen funktionsstyring. | 6 - 12 juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
