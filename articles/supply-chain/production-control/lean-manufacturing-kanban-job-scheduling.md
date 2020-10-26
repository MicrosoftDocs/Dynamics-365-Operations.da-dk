---
title: Kanban-job til lean manufacturing
description: Denne artikel indeholder oplysninger om visuel kontrol med kanban-jobplanlægning og forskellige metoder til at planlægge kanban-job.
author: cvocph
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardScheduleJobForward, KanbanBoardShowJobs, KanbanJobSchedulingListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 52961
ms.assetid: fe3b4822-6140-4b02-bebb-1fc17be2bce8
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 77ba67de5585022ab7d506c8cd2acb380a4e3a54
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/10/2020
ms.locfileid: "3979445"
---
# <a name="kanban-job-scheduling-for-lean-manufacturing"></a>Kanban-job til lean manufacturing

[!include [banner](../includes/banner.md)]

Denne artikel indeholder oplysninger om visuel kontrol med kanban-jobplanlægning og forskellige metoder til at planlægge kanban-job.  

Siden **Tidsplanlæg af kanban-job** giver visuel kontrol over tidsplaner for lean manufacturing-arbejdsceller. Den giver et overblik over alle kanban-job og indeholder flere funktioner til filtrering. Fra denne side kan du flytte til andre sider, der er relateret til kanban-konfiguration og kørsel.

## <a name="automatic-scheduling-of-kanban-jobs"></a>Automatisk tidsplanlægning af kanban-job
Planlægning kan udløses automatisk, hvis du indstiller parameteren **Automatisk planlægningsantal** i kanban-reglen. Hvis du indstiller **Automatisk planlægningsantal** til **1**, planlægges hvert kanban-job straks, når det oprettes. Resultatet er en serie af first pull, first serve-operationer. Hvis du indstiller **Automatisk planlægningsantal** til en værdi, der er mere end 1, grupperes kanban-job, før de er planlagt. 

Dette koncept gør det muligt for kanban-størrelser at blive reduceret til under de faktiske økonomiske batchstørrelser. F.eks. er den økonomiske batchstørrelse for en bestemt vare (eller varefamilie) 30. I stedet for at oprette kanbans, der bruger produktantallet 30, kan du konfigurere kanban-reglen, så der er et antal på 10 og en værdi for **Automatisk planlægningsantal** på **3**. Selvom automatisk planlægning tidsplanlægger kanban-job for arbejdscellen, når der kun er ikke-planlagte job, er det helt gennemsigtigt for planlæggeren og den tilsynsførende, at to ikke-planlagte job måske afventer udførelse. Planlæggeren eller den tilsynsførende kan derefter tage disse to job i produktion ved manuelt at planlægge dem eller oprette yderligere kanbans.

## <a name="manual-scheduling"></a>Manuel tidsplanlægning
For manuel tidsplanlægning introducererede Microsoft Dynamics AX 2012 kanban-planlægningsområdet. Manuel tidsplanlægning kan kombineres med automatisk tidsplanlægning. Med kanban-planlægningsområdet kan du planlægge og fjerne planlægningen af job, flytte dem i rækkefølge eller flytte dem fra periode til periode. Job, der er baseret på en kanban-regel, hvor værdien **Automatisk planlægning** er højere end **0**, kan planlægningen være manuelt fjernet. Disse job kan dog planlægges igen, når den næste automatiske planlægningshændelse indtræffer (når der oprettes en ny kanban). Følgende indstillinger er tilgængelige for manuel tidsplanlægning:

-   **Tidsplan** planlægger de valgte job efter deres forfaldsdato. (Denne indstilling ligner automatisk planlægning).
-   **Planlæg fremad fra dato** forsøger at planlægge de valgte job efter forfaldsdatoen, men begrænser resultatet ved hjælp af den angivne tidligste startdato.
-   **Bagud** flytter de valgte planlagte job tilbage i rækkefølgen inden for perioden.
-   **Fremad** flytter de valgte planlagte job fremad i rækkefølgen inden for perioden.
-   **Forrige periode** flytter de valgte planlagte job til starten eller slutningen af den foregående periode.
-   **Næste periode** flytter de valgte planlagte job til starten eller slutningen af den næste periode.
-   **Planlæg** &gt; **Gendan jobstatus** giver dig mulighed for at fjerne planlægningen for et planlagt job.

## <a name="lean-scheduling-groups"></a>Lean planlægningsgrupper
Hver farve repræsenterer en lean planlægningsgruppe. Lean planlægningsgrupper kan defineres frit, som generiske grupper eller grupper, der tilhører en enkelt arbejdscelle. Varer og dimensioner kan frit tildeles til planlægningsgrupper: For eksempel kan en planlægningsgruppe i malecellen repræsentere en farve for produktet. I arbejde, der drives af specifikke værktøjskrav, kan varerne være grupperede efter krav til værktøj og en arbejdscelle for emballage kan gruppere varer ud fra emballageskabelonen. Brugen af farver til lean planlægningsgrupper er valgfri, men anbefales. Det forbedrer indsigt i status for planen. For eksempel er det meget nemt at se, hvilke farver der produceres på hvilken dag, og du kan se en oversigt over, hvordan dette arbejde kan optimeres.

## <a name="work-cell-capacity-and-period-capacity"></a>Arbejdscellekapacitet og periodekapacitet
Kapaciteten for en lean arbejdscelle er altid samtidig kapacitet. Med andre ord: flere job kan være aktive i en arbejdscelle på samme tid. Kapaciteten kan spores i to tilstande: gennemløb og timer.

### <a name="throughput"></a>Gennemløb

Kapaciteten for en arbejdscelle er defineret af det gennemsnitlige gennemløbsantal for en referenceperiode (standardarbejdsdag, uge eller måned). Den faktiske kapacitet pr. dag eller uge beregnes derefter baseret på arbejdstider for den kalender, der er tildelt arbejdscellen. Den kapacitet, der er indlæst af job er antallet af job, der er reguleret af gennemløbsforholdet for varen i arbejdscellen.

### <a name="hours"></a>Timer

Den tilgængelige kapacitet pr. dag eller uge er defineret af den kalender, der er tildelt arbejdscellen. Den kapacitet, der er indlæst af job, er procestid eller aktiviteten, der er reguleret af antallet (standardantallet for aktiviteten versus den faktiske jobmængde) og gennemkøbsforholdet for varen i arbejdscellen.

#### <a name="period-capacity-factbox"></a>Faktaboksen Periodekapacitet

Listesiden **Tidsplanlægning af kanban-job** indeholder en faktaboks, der viser den tilgængelige og reserverede periodekapacitet for den valgte arbejdscelle. Afhængigt af de valgte planlagte perioder i produktionsflowmodellen viser perioderne dage eller uger.

<a name="additional-resources"></a>Yderligere ressourcer
--------



