---
title: Overvåge kørsel af en varedisponering
description: Dette emne beskriver, hvordan produktionsplanlæggeren kan se, om en varedisponeringskørsel er i gang.
author: ChristianRytt
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4db1173b35cd196ab39fae3cac3754439fab84d0
ms.sourcegitcommit: fcb8a3419e3597fe855cae9eb21333698518c2c7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/09/2022
ms.locfileid: "8103157"
---
# <a name="monitor-a-master-planning-run"></a>Overvåge kørsel af en varedisponering

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a>Brug et Gantt-diagram til at visualisere status for varedisponering

På siden **Vis varedisponeringens status** kan du få vist detaljer om den historiske varedisponeringskørsel i form af et Gantt-diagram. Denne funktionalitet kan hjælpe dig med at forstå den tid, der bruges på de forskellige faser i varedisponeringen. For et aktuelt aktivt planlægningsjob kan siden **Vis varedisponeringens status** bruges til at spore statussen og få vist den estimerede resterende tid.

### <a name="turn-the-master-plan-progress-visualization-feature-on-or-off"></a>Aktivere eller deaktivere funktionen Visualisering af status for varedisponering

Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres. Hvis du kører en version, der er ældre end 10.0.25, kan administratorer slå denne funktion til eller fra ved at søge efter funktionen *Visualisering af status for varedisponering* i arbejdsområdet [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).

### <a name="use-the-master-plan-progress-visualization-feature"></a>Bruge funktionen Visualisering af status for varedisponering

Siden **Vis varedisponeringens status** kan vise både tidligere planlægningsjobs og aktive planlægningsjobs. 

Der er to valgmuligheder for at få vist historiske planlægningsjobs. 

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**, og i handlingsruden skal du dernæst vælge **Historik**. Marker **Forespørgsler**, mens det ønskede job er markeret, og vælg derefter **Vis status**
1. Gå til **Varedisponering \> Arbejdsområder \> Varedisponering**, klik derefter på **Historik** i feltet Varedisponering. Marker **Forespørgsler**, mens det ønskede job er markeret, og vælg derefter **Vis status**

Der er to valgmuligheder for at få vist aktive planlægningsjobs. 
1. Gå til **Varedisponering \> Arbejdsområder \> Varedisponering** i handlingsruden, og vælg der **Uafsluttede planlægningsprocess**. Marker **Forespørgsler**, mens det ønskede job er markeret, og vælg derefter **Vis status**.
1. Gå til **Varedisponering \> Arbejdsområder \> Varedisponering**, klik derefter på **Vis status** i feltet Varedisponering. Marker **Forespørgsler**, mens det ønskede job er markeret, og vælg derefter **Vis status**

Bemærk, at du kun kan få vist aktive job, når et planlægningsjob behandles.

### <a name="analyze-a-master-planning-job"></a>Analyser et varedisponeringsjob

I Gantt-diagrammet kan du udvide hver af følgende planlægningsprocesser for at få vist flere detaljer om den tid, der er brugt:

- Initialisering
- Sletter og indsætter data
- Disponering
- Forsinkelser
- Handlingsmeddelelser
- Færdiggørelse
- Automatisk autorisation

Gantt-diagrammet er et nyttigt værktøj, hvis du vil se indvirkningen af at bruge handlingsbeskeder.

#### <a name="navigation-in-the-gantt-chart"></a>Navigation i Gantt-diagrammet

- Hvis du vil udvide den valgte gruppe og vise detaljerne, skal du vælge plustegnet (**+**) trævisningen.
- Hvis du vil skjule den markerede gruppe, skal du vælge minustegnet (**–**) i trævisningen.
- Du kan bruge tastaturet til at navigere. Brug **Pil op** og **Pil ned** til at flytte mellem rækker. Brug **Højre pil** og **Venstre pile** til at udvide og skjule grupper.
- Hvis du vil åbne eller lukke alle niveauer i Gantt-diagrammet, skal du vælge **Udvid alle** eller **Skjul alle**.
- Hold markøren over en opgave for at få vist den relaterede behandlingstid. (Opgaver er det laveste niveau i Gantt-diagrammet).

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a>Få vist en ekstra varedisponeringskørsel for at sammenligne job

Hvis du vælger et varedisponeringsjob i feltet **Vis yderligere varedisponeringskørsel**, kan du få vist en ekstra varedisponeringskørsel i Gantt-diagrammet og sammenligne de to job.

#### <a name="bom-level-display"></a>Visning på styklisteniveau

Styklistelisteniveauer (BOM) vises forskelligt for disponering, forsinkelser, handlinger og autorisation.

- **Disponering** – Styklisteniveauer vises som forventet. De beregnes fra toppen og ned.

    **Eksempel:** Styklisteniveau 0, 1, 2

- **Forsinkelser** – Styklisteniveauer vises som styklisteniveauer for varedisponering multipliceret med –1. (Med andre ord har de et negativt tegn).

    **Eksempel:** Styklisteniveau –2, –1, 0

- **Handlingsbesked** – Styklisteniveauer vises som forventet. De beregnes fra toppen og ned.

    **Eksempel:** Styklisteniveau 0, 1, 2

- **Auto-autorisering** – Styklisteniveauer vises som 999 minus styklisteniveauet for disponeringsplanlægning.

    **Eksempel:** Styklisteniveau 999, 998, 997

I følgende tabel vises en oversigt over problemet.

| Det viste styklisteniveau | Slutvare | Underkomponent | Råvarer |
|---|---|---|---|
| Disponering | 0 | 1 | 2 |
| Forsinkelser | 0 | –1 | –2 |
| Handlingsmeddelelse | 0 | 1 | 2 |
| Automatisk autorisation | 999 | 998 | 997 |

#### <a name="visualize-progress"></a>Visualiser status

Hvis du får vist et varedisponeringsjob, der kører, vises status i Gantt-diagrammets farver. Der gælder følgende farver for det blå tema: I forbindelse med andre farvetemaer vil farverne være forskellige.

- **Mørkeblå** – Fuldførte planlægningsopgaver.
- **Orange** – Den opgave, der er i gang i øjeblikket.
- **Lyseblå** – Estimatet for de resterende opgaver.

Farven vises kun på det laveste niveau i Gantt-diagrammet. Vælg **Udvid alle** for at få vist alle opgaver i varedisponeringsjobbet. Estimatet for resterende opgaver er baseret på historiske varedisponeringsjob.

## <a name="run-master-planning-and-track-processing-time"></a>Kør varedisponering og registrer procestiden

1. Vælg **Varedisponering** på standarddashboardet.
1. I feltet **Plan** indtastes eller vælges en værdi.
1. Vælg **Kør**.
1. Angiv indstillingen i **Registrer procestiden** til **Ja**.
1. Indtast et antal i feltet **Antal tråde**.
1. I oversigtspanelet **Medtagne poster** skal du vælge **Filtrer**.
1. I gitteret skal du vælge den række, hvor feltet **Felt** er angivet til **Varenummer**.
1. Angiv en værdi i feltet **Kriterie**.
1. Vælg **OK**.


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]