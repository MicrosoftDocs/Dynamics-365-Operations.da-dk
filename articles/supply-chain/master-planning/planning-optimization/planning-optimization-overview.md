---
title: Oversigt over Planlægningsoptimering
description: Dette emne giver et overblik over funktionen Planlægningsoptimering.
author: ChristianRytt
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: intro-internal
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 8fd73313b82319c35eb5fccbd68cd305403bfe3f635f6b267fb408943af3396c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6739053"
---
# <a name="planning-optimization-overview"></a>Oversigt over Planlægningsoptimering

[!include [banner](../../includes/banner.md)]

Tilføjelsesprogrammet Planlægningsoptimering til Microsoft Dynamics 365 Supply Chain Management giver dig mulighed for at beregne varedisponering udenfor Dynamics 365 Supply Chain Management og den relaterede SQL-database. De fordele, der er tilknyttet funktionen Planlægningsoptimering, omfatter forbedret ydeevne og minimal påvirkning af SQL-databasen under kørsel af varedisponeringen. Hurtige planlægningskørsler kan udføres selv i kontortiden, så planlæggerne kan reagere øjeblikkeligt på ændringer i behov eller parametre.

Hvis du vil bruge Planlægningsoptimering, skal du installere tilføjelsesprogrammet til Planlægningsoptimering fra dit projekt i Microsoft Dynamics Lifecycle Services (LCS) og aktivere funktionen Planlægningsoptimering i Supply Chain Management. Du kan finde flere oplysninger under [Kom i gang med Planlægningsoptimering](get-started.md).

I følgende illustration vises fordelen ved at køre Planlægningsoptimering inden for kontorets åbningstider.

![Fordelen ved at køre Planlægningsoptimering inden for kontorets åbningstider.](media/PlanningOptimization1.png)

## <a name="improved-performance"></a>Forbedret ydeevne

Planlægningsoptimering kan bruges i scenarier, der involverer langvarige behovsplaner. Den er særligt designet til meget hurtige beregninger, der omfatter meget store mængder data. Da den er bygget som en ultra skalerbar tjeneste til flere lejere, kan flere forekomster arbejde sammen samtidigt i beregningen af planen. Desuden fjerner planlægningstjenesten belastningen fra varedisponeringen fra systemet og arbejder sammen med en datastrøm, der minimerer serverbelastningen.

Planlægningsoptimering kan hjælpe dig med at opnå følgende mål:

- Forbedret ydeevne for planlægning via en kortere kørsel.
- Reducere indvirkningen på andre processer under kørslen af varedisponering.
- Kør hyppigere planlægningskørsler. (Du er ikke begrænset til de daglige kørsler.)
- Være sikker på, at den fremtidige virksomhedsvækst ikke overbelaster planlægningssystemet.

## <a name="architecture-and-data-flow"></a>Arkitektur og dataflow

Når tilføjelsesprogrammet Planlægningsoptimering er installeret fra LCS, oprettes der en sikker forbindelse til Planlægningsoptimeringstjenesten. Tjenesten er placeret i samme datacenterland eller -område som den relaterede Supply Chain Management-forekomst. Efter Planlægningsoptimering er konfigureret, sendes der, når der køres varedisponering, masterdata og transaktionsdata fra Supply Chain Management til Planlægningsoptimeringstjenesten.

Hvis tilføjelsesprogrammet Planlægningsoptimering afinstalleres, fjernes alle relaterede data i Planlægningsoptimeringstjenesten.

### <a name="high-level-data-flow-for-regeneration-runs"></a>Dataflowet på højt niveau for kørsler af regenerering

1. Klienten Supply Chain Management sender et signal for at anmode om en planlægningskørsel fra Planlægningsoptimering.
2. Planlægningsoptimering anmoder om de påkrævede data via den integrerede forbindelse.
3. SQL-databasen sender de anmodede oplysninger om opsætning, master- og transaktionsdata til Planlægningsoptimering via Connector. Connectoren oversætter oplysninger mellem Supply Chain Management og tjenesten Planlægningsoptimering.
4. Planlægningsoptimeringstjenesten gemmer planlægningsrelaterede data i hukommelsen og foretager de påkrævede beregninger.
5. Planlægningsresultatet sendes til Supply Chain Management-databasen via Connector. Resultaterne omfatter oplysninger, som f.eks. ordreforslag og oplysninger om udligning. Planlægningsoptimering sender et signal til Supply Chain Management for at indikere, at planlægningskørslen er fuldført. Den sender også alle relevante meddelelser og advarsler.

Følgende illustration viser dataflowet.

![Dataflowet for kørsler af regenerering.](media/PlanningOptimization2.png)

## <a name="related-resources"></a>Tilknyttede ressourcer

[Start her med planlægningsoptimering](get-started.md)

[Analyse af om Planlægningsoptimering passer til](planning-optimization-fit-analysis.md)

[Få vist planhistorik og planlægningslogs](plan-history-logs.md)

[Anvend filtre på en plan](plan-filters.md)

[Annullere et planlægningsjob](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]