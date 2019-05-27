---
title: Visuel planlægning af lean manufacturing
description: Dette emne indeholder oplysninger om kanban-planlægningsområdet, som produktionsplanlæggeren kan bruge til at styre og optimere produktionsplanen for kanban-job.
author: johanhoffmann
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoard, KanbanJobSchedulingListPage, LeanProductionFlowVisualization
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Manufacturing
ms.author: johanho
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6fdfa78ba0ace5481305d2ab505ed5fc7538e29e
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1545024"
---
# <a name="visual-scheduling-for-lean-manufacturing"></a>Visuel planlægning af lean manufacturing

[!include [banner](../includes/banner.md)]

Dette emne indeholder oplysninger om kanban-planlægningsområdet, som produktionsplanlæggeren kan bruge til at styre og optimere produktionsplanen for kanban-job.

Dette emne indeholder oplysninger om kanban-planlægningsområdet, som produktionsplanlæggeren kan bruge til at styre og optimere produktionsplanen for kanban-job.

I kanban-planlægningsområdet kan produktionsplanlæggere styre og optimere produktionsplanen for kanban-job. Det gør det nemt at overskue strømmen af kanban-job og giver produktionsplanlæggeren et værktøj, der optimerer og justerer produktionsplanen efter lean manufacturing-arbejdscellen.

## <a name="visual-scheduling-of-kanban-jobs"></a>Visuel planlægning af kanban-job
Et kanban-job kan bestå af et eller flere kanban-job. Der findes to typer af kanban-job:

-   Proces
-   Ompostering

Du kan kun planlægge job af typen **Proces**. Kanban-jobbet og dets egenskaber, f.eks. som aktivitetstiden, er defineret i kanban-produktionsflow. Kanban-jobbet er også tildelt en arbejdscelle i kanban-produktionsflow. Daglig kapacitet for arbejdscellen er beregnet ud fra den arbejdscellekapacitet, der er angivet for ressourcegruppen. Den justeres med den daglige arbejdstid i den relaterede kalender. Når et kanban-job er planlagt, belaster jobbet kapaciteten for arbejdscellen. Kanban-planlægningsområdet indeholder følgende primære funktioner:

-   En grafisk oversigt over produktionsplanen i en lean arbejdscelle. Denne oversigt viser planlagte kanban-procesjob i definerede perioder.
-   Et værktøj, du kan bruge til at planlægge ikke-planlagte kanban-job og omplanlægge tidligere planlagte job.

## <a name="kanban-schedule-board"></a>Kanban-planlægningsområde
Siden **Kanban-planlægningsområde** indeholder syv hovedelementer, som er vist i følgende illustration. 

![Kanban-planlægningsområde](./media/kanban-schedule-board-1024x554.png)
1.  Handlingsrude
2.  Filtreringsfelter
3.  Knap til ikke-planlagte job
4.  Periodenode
5.  Kanban-job
6.  Kapacitetslinje
7.  Tidsskala

### <a name="view-the-time-scale"></a>Se tidsskalaen

Området er opdelt i perioder, der hver især er repræsenteret som en node (4). Nodeperioderne er angivet på den lodrette akse, og den vandrette akse repræsenterer en tidsskala (7), der viser periodens længde. En periode har en længde på enten en dag eller en uge. Periodens længde bestemmes af konfigurationen af den arbejdscelle, der er valgt for Kanban planlægningsområdet (2). For hver periodenode angiver i kanban-planlægningsområdet, hvor meget de planlagte kanban-job belaster perioden. Der findes også en angivelse af det maksimale gennemløb for perioden. Hvis det planlagte gennemløb overstiger det maksimale gennemløb, betragtes perioden som overbelastet og vises med et rødt advarselssymbol. Et planlagt kanban-job vises i en periode med planlagte start- og sluttider (5). Længden af jobbet er lig med aktivitetstiden. Kanban-job vises som overlappende i en periode, hvis deres aktivitetstider overstiger arbejdscellens takttid.

### <a name="view-job-status"></a>Se jobstatus

Yderligere oplysninger om et kanban-job er tilgængelige i det værktøjstip, der vises, når du holder markøren over jobbet. Et symbol viser oplysninger om status for jobbet. Eksempelvis angiver et ursymbol, at kanban-jobbet er forfaldent.

### <a name="use-colors-to-view-the-kanban-schedule-board"></a>Bruge farver til at få vist kanban-planlægningsområdet

Du kan bruge farver til at skelne kanban-job ad for at forbedre den oversigt, der indeholder kanban-planlægningsområdet. Farven på et kanban-job er konfigureret i lean planlægningsgruppen, hvor du kan sammenlægge de produkter, der skal produceres i samme sekvens. Brug knappen **Brug temafarver** under fanen **Område** i handlingsruden til at skifte mellem temafarverne i programmet og de farver, der er konfigureret i lean planlægningsgruppen. For hver periode angiver en kapacitetslinje (6), hvor mange af de tilgængelige timer i perioden der er belastet med kanban-job. Hvis perioden er overbelastet, er kapacitetslinjen tykkere og rød. Disse funktioner er tilgængelige under fanen **Område** i handlingsruden (1) øverst på siden **kanban-planlægningsområde**.

## <a name="plan-unplanned-jobs"></a>Planlæg ikke-planlagte job
Du kan planlægge ikke-planlagte kanban-job i dialogboksen **Planlæg ikke-planlagte job**. Du kan åbne denne dialogboks ved at klikke på knappen **Ikke-planlagte job**, der viser det aktuelle antal ikke-planlagte job. Du kan også klikke på **Planlæg ikke-planlagte job** på fanen **Område** i handlingsruden. Dialogboksen viser en liste over ikke-planlagte kanban-job for arbejdscellen. Du kan bruge feltet **Filter** til at filtrere efter alle felter i gitteret. For eksempel kan du filtrere efter kanban-job for et bestemt produkt. Når du har en filtreret listen over de job, du vil planlægge, kan du vælge dem på listen og derefter klikke på **OK**. Hvis du vil bruge automatisk planlægning til at planlægge job, skal du angive den **Automatisk planlægning** til **Ja**. I så fald planlægges jobbene i en periode i henhold til deres forfaldsdato. Du kan også planlægge job pr. periode. Vælg en periode i feltet **Periode**. I følgende illustration vises et eksempel på dialogboksen **Planlæg ikke-planlagte job**. 

![Dialogboksen Planlæg ikke-planlagte job](./media/plan-unplanned-jobs-1024x564.png)

## <a name="sequence-kanban-jobs-within-the-same-period"></a>Rækkefølgen af kanban-job inden for samme periode
Du kan ændre rækkefølgen af et eller flere valgte job i en periode. Denne funktion kan være nyttig, hvis du vil prioritere nogle job i perioden. Alternativt kan du få angive rækkefølgen af job, der har samme produktattributter, for at optimere kørslen af jobbet. Du kan ændre rækkefølgen via træk og slip eller ved at bruge menupunkterne **Bagud** og **Fremad** under fanen **Område** i handlingsruden.

## <a name="reassign-kanban-jobs-across-periods"></a>Tildele kanban-job igen på tværs af perioder
Job kan omfordeles fra én periode til en anden. Denne funktion kan være nyttig, hvis en periode er overbelastet, og du vil fordele belastningen på perioder, der har ekstra kapacitet. Du omfordele job via træk og slip eller ved at bruge menupunkterne **Næste periode** og **Forrige periode** under fanen **Område** i handlingsruden.

## <a name="open-the-kanban-schedule-board"></a>Åbne kanban-planlægningsområdet
Du kan åbne kanban-planlægningsområdet ved hjælp af menupunktet på følgende sider:

-   Siden **Området Produktion**
-   Siden **Planlægning af kanban-job**
-   Siden **Visualisering af produktionsflow**


<a name="additional-resources"></a>Yderligere ressourcer
--------

[Lean manufacturing – tidsplanlægning af kanban-job](lean-manufacturing-kanban-job-scheduling.md)

