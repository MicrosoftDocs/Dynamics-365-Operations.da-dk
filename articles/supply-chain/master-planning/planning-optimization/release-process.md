---
title: Frigivelsesproces og frigivelseshistorik for Planlægningsoptimering
description: Dette emne indeholder oplysninger om frigivelsesprocessen og frigivelseshistorikken for Planlægningsoptimering.
author: ChristianRytt
ms.date: 09/21/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-07-28
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: b2e0145c28b40f4fbfb54ad7e7ed32fbc130c569
ms.sourcegitcommit: 8afd0cdb39ec443fb7631c39401967cce0fac34e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2021
ms.locfileid: "7727426"
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
| <p>Ekstra understøttelse af beregningsformler til procestid, produktionsrute med overlap og produktionsoperationsnummer på behovsposteringer.</p><p>Bedre fejlmeddelelser for produktionsplanlægning, der er knyttet til timeout, kapacitet blev ikke fundet og cyklisk rute.</p><p>Forbedret konsistens ved beregning af tilgangsdatoer og afgangsdatoer på både ordreforslag og autoriserede ordrer.</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet. | Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering* | 22.- 27. oktober 2021 |
| <p>Ekstra understøttelse af overvejelser om spildprocent ved beregning af procestid.</p><p>Ekstra understøttelse af operationsnummer og materialeforbrug under planlægning. | Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering* | 5.- 7. oktober 2021 |
| <p>Ekstra understøttelse af jobtyper til produktionsrute: **Kø før**, **Kø efter** og **Transporttid**.</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet. | Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering* | 25. - 30. september 2021 |
| <p>Tilføjet understøttelse af behovsplaner, hvor **Planlægningsmetode** er indstillet til *Grovplanlægning*.</p><p>På siden **Rutegrupper** skal du markere indstillingerne af afkrydsningsfelterne **Aktivering**, **Arbejdstid** og **Kapacitet** for rækker med **Rute-/jobtype** som *Opsætning* eller *Proces*. </p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet. | <p>Grovplanlægning er tilgængelig i funktionsstyring fra og med version 10.0.20.</p><p>Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering*</p>  | 9. - 17. september 2021 |
| Generelle forbedringer af ydeevne, kvalitet og stabilitet. | Der kræves ingen funktionsstyring. | 25 - 30 august 2021 |
| <p>Har tilføjet feltet **Leveringstid** til ordreforslag.</p><p>Generelle forbedringer af ydeevne, kvalitet og stabilitet.</p> | Der kræves ingen funktionsstyring. | 12 - 17 august 2021 |
| <p>Tilføjet ressourcetypekrav for planlægning med ubegrænset kapacitet.</p><p>Forbedret ressourceeffektivitet og kalendereffektivitet for planlægning med ubegrænset kapacitet.</p><p>Yderligere oplysninger finder du under [Planlægning med ubegrænset kapacitet](infinite-capacity-planning.md). | <p>Tilgængelig i funktionsstyring fra og med version 10.0.20.</p><p>Funktionsnavn: *Uendelig kapacitetsplanlægning til Planlægningsoptimering*</p> | 6 - 12 juli 2021 |
| Generelle forbedringer af kvalitet. | Der kræves ingen funktionsstyring. | 6 - 12 juli 2021 |

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
