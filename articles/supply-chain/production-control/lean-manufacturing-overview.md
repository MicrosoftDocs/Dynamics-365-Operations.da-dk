---
title: Oversigt over lean manufacturing
description: Denne artikel indeholder en oversigt over og en beskrivelse af lean manufacturing-funktioner i Dynamics 365 Supply Chain Management.
author: johanhoffmann
ms.date: 06/20/2017
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: KanbanBoardTransferJob, KanbanBoardWorkCell, KanbanJobSchedulingListPage, LeanProductionFlow, Kanban, KanbanQuantityOverview, KanbanAssignCard, KanbanCirculatingCards, KanbanRules, WHSKanbanWaveTableManagePickingListPool
audience: Application User
ms.reviewer: kamaybac
ms.custom:
- "19371"
- intro-internal
ms.assetid: 026c5605-6be7-4fdb-a6f2-8e37a806796c
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e0c8b5ec4d4a391773e32a61a321c28868678baa
ms.sourcegitcommit: 3754d916799595eb611ceabe45a52c6280a98992
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2022
ms.locfileid: "7985930"
---
# <a name="lean-manufacturing-overview"></a>Oversigt over lean manufacturing

[!include [banner](../includes/banner.md)]

Denne artikel indeholder en oversigt over og en beskrivelse af lean manufacturing-funktioner i Dynamics 365 Supply Chain Management.

Lean manufacturing tilbyder værktøjer, som du kan bruge til at oprette lean-operationer. Disse værktøjer understøtter og fremmer følgende begreber og aktiviteter:
-   Oprette et lean manufacturing-grundlag ved udformning af produktions- og logistikprocesser som produktionsflow.
-   Implementere lean pull-system ved hjælp af kanbans for at signalere efterspørgselskrav.
-   Overvåge og vedligeholde kanban-job.

Lean manufacturing-arkitekturen består af produktionsflow, aktiviteter og kanban-regler. Disse strukturer er fuldt integreret med Supply Chain Management-processer. Du kan bruge lean manufacturing i et produktionsmiljø med blandet tilstand, der kombinerer forskellige strategier for levering, produktion og forsyning. Disse strategier omfatter produktionsordrer, batch-ordrer til forarbejdningsindustrier, købsordrer og overflytningsordrer.

| **Vigtig**                                                                                                                                                                                                                                                                |
|------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Du kan bruge Supply Chain Management til at understøtte implementeringen af lean manufacturing med kanbans. En vellykket implementering af lean-principper afhænger imidlertid af de interne forretningsprocesser, du bruger, de faktiske produktionsbetingelser og miljøet. |

## <a name="modeling-manufacturing-and-logistics-processes-as-production-flows"></a>Udforme produktions- og logistikprocesser som produktionsflow
For at oprette et lean manufacturing-grundlag skal produktions- og logistikprocesser udformes som produktionsflow. Denne aktivitet består af følgende opgaver:
1.  Identificere de processer, du vil implementere en lean-genopfyldningsstrategi for og derefter udforme disse processer som produktionsflow. Derefter kan du analysere og strømline processerne. Et af målene med lean-implementering er at reducere spild ved at forbedre strømmen af materialer og oplysninger.
2.  Definere et produktionsflow som en sekvens af aktiviteter, der beskriver materialeflow. En overførselsaktivitet definerer flytningen af et produkt eller produkter fra én placering til en anden. En procesaktivitet definerer en værditilvækst, der anvendes til et produkt.
3.  Oprette en version af produktionsflowet, der definerer kravene til tiden i takt. Disse krav bruges til at beregne procestiderne for hver aktivitet i produktionsflowet. Du kan oprette flere versioner af produktionsflow og derefter bruge disse versioner til at forbedre processerne.

## <a name="using-kanbans-to-signal-demand-requirements"></a>Bruge kanbans til at signalere efterspørgselskrav
Et pull-system producerer kun varer, når der er behov for varerne. Denne praksis reducerer leveringstider og overskydende lager. Du kan bruge kanbans til at planlægge, registrere og behandle krav, der er baseret på produktionsflow. Hvis du vil oprette en ramme med kanban, skal du oprette kanban-regler, der definerer oprettelsen af kanbans, og hvordan kravene er opfyldt. Du kan oprette to typer af kanban-regler. Produktionsregler opretter kanban-procesjob, og udtrækning af kanban-regler opretter kanban-overførselsjob. Du kan indstille følgende genopfyldningsstrategier:
-   Regler for **fastmængde**-kanban er relateret til en fast mængde materialehåndteringsenheder, hvilket betyder, at mængden af aktive kanbans er konstant. Når alle produkter fra en kanban er forbrugt, og materialehåndteringsenhederne manuelt er blevet tømt, oprettes der en ny kanban af samme type. Når du opretter regler for fastmængde-kanban, kan du beregne de optimale kanban-mængder og de produktmængder, der anvendes. Beregningen tager højde for prognose, faktisk efterspørgsel fra åbne ordrer, leveringstid for genbestilte varer og historiske krav.
-   **Planlagte** kanban-regler opfylder de krav, der beregnes af varedisponeringen. Varedisponering genereres planlagte kanbans, der kan autoriseres til kanbans.
-   Regler for **hændelses**-kanbans genopfylder de krav, der stammer fra salgsordrelinjer, styklistelinjer, kanban-linjer eller indstillinger for minimumslager. Når hændelses-kanbans genereres, bliver de udlignet i forhold til kildeforudsætningerne.

Når der oprettes kanbans, genereres et eller flere kanban-job baseret på kanban-flowet af aktiviteter, der er defineret i kanban-reglerne.

## <a name="monitoring-and-maintaining-kanban-jobs"></a>Overvågning og vedligeholdelse af kanban-job
Lean manufacturing viser den aktuelle status for produktion og logistik, der er omfattet af kanban-reglerne. Derfor kan du planlægge og prioritere følgende opgaver:

-   Få et overblik over den aktuelle tidsplan for kanban-job.
-   Planlægge og ændre planlægning for kanban-job.
-   Spore og registrere status for kanban-job.

Følgende liste beskriver specielle kanban-kort:
-   Tidsplanlægning af kanban-job – indeholder en oversigt over kanban-job. Tavlen viser kanban-job og deres status for en eller flere arbejdsceller. Jobsene er angivet efter de planlægningsperioder (dage eller uger), der er defineret i produktionsflowmodellen. Tavlen viser også kapacitetsforbruget for hver planlægningsperioden, så du kan overvåge den planlagte belastning. Du kan ændre status for kanban-job, omlægge kanban-job til andre perioder og udføre andre opgaver.
-   Kanban-område for overførsel af sager – Denne tavle giver et overblik over de aktuelle overførselsjob. Du kan opdatere og registrere pluklister, starte og fuldføre overførselsjob og udføre andre opgaver.
-   Kanban-området til procesjob – denne tavle er udviklet til at understøtte det normale produktionsflow og giver et overblik over den aktuelle situation i en eller flere arbejdsceller. Fra denne tavle kan Kanbans prioriteres, plukkes eller fremstilles. Tavlen er også udviklet til at understøtte stregkodescanning for rapportering af kanbans.

## <a name="kanban-jobs-and-integration-with-supply-chain-management-processes"></a>Kanban-job og -integration med Supply Chain Management-processer
Kanban-job er fuldt integreret med de aktuelle processer for lagertransaktioner i Supply Chain Management.
-   Du kan udføre plukaktiviteter for at genbestille materiale, der bruges til at opfylde kravene i kanban-job.
-   Du kan udskrive kanban-kort, cirkulerende kanban-kort og pluklister til at understøtte brugen af kanbans. Disse dokumenter bruges til at repræsentere, spore og registrere kanban-job på lagerstedet og produktionsanlægget.
-   Du kan registrere pluk- og overførselsaktiviteter på lageret ved at scanne stregkoderne.

Desuden understøtter lean manufacturing indkøb og faktureringsprocesser for tjenester, der henvises til af underleverandørens aktiviteter.
-   Du kan tildele købslinjer for aftalen og tjenester til underleverandørens aktiviteter.
-   Du kan oprette periodiske indkøbsordrer og modtagelsesadvisering for at understøtte køb og fakturering af tjenester.







[!INCLUDE[footer-include](../../includes/footer-banner.md)]