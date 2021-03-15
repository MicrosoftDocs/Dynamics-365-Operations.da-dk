---
title: Planlægge oprettelse af arbejde under bølge
description: I dette emne beskrives, hvordan du kan konfigurere og bruge behandlingsmetoden til planlægning af arbejdsoprettelse i bølge.
author: perlynne
manager: mirzaab
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: ''
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: ed8f43c7db139b7b16ac6901d5db56ba2f021690
ms.sourcegitcommit: b7a7a14f8650913f6797ae1c4a82ad8adfe415fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/28/2021
ms.locfileid: "5078244"
---
# <a name="schedule-work-creation-during-wave"></a>Planlægge oprettelse af arbejde under bølge

[!include [banner](../includes/banner.md)]

Brug funktionen *Planlæg oprettelse af arbejde* som en del af din bølgeproces for at øge gennemløbet af bølgearbejde ved at lade systemet oprette arbejde via parallel behandling.

Når funktionaliteten er aktiveret, oprettes der automatisk planlagt arbejde, som systemet i den sidste ende behandler for at oprette faktisk arbejde. Hvis antallet af bølgelastlinjer når en foruddefineret grænseværdi, opretter systemet det faktiske arbejde hurtigere ved at anvende parallel asynkron behandling.

## <a name="enable-the-schedule-work-creation-feature"></a>Aktivere funktionen Planlæg oprettelse af arbejde

### <a name="enable-the-feature-in-feature-management"></a>Aktivere funktionen i funktionsstyring

Før du kan bruge funktionen *Planlæg oprettelse af arbejde*, skal den være aktiveret i dit system. Administratorer kan bruge området [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov. Dér vises funktionen på følgende måde:

- **Modul:** *Lokationsstyring*
- **Funktionsnavn:** *Planlæg oprettelse af arbejde*

> [!NOTE]
> Funktionen *Blokering af arbejde i hele organisationen* skal være aktiveret, før du kan aktivere *Planlæg oprettelse af arbejde*.

### <a name="manually-enable-batch-processing-of-waves"></a>Aktivere batchafvikling af bølger manuelt

Hvis du vil have fordel af en parallel asynkron metode til oprettelse af lagerstedsarbejde, skal din bølgeproces køres i batch. Sådan konfigurerer du dette:

1. Gå til **Lokationsstyring \> Opsætning \> Parametre til lokationsstyring**.

1. Angiv **Udfør behandling af bølger i batch** til **Ja** under fanen *Generelt*. Du kan også vælge en dedikeret **Batchgruppe til behandling af bølger** for at forhindre, at batchkøbehandlingen køres på samme tid som andre processer.

1. Indstil **Vent på lås (ms.)**, som gælder, når systemet behandler flere bølger samtidig. Ved de fleste større bølgeprocesser anbefales en værdi af *60000*.

### <a name="manually-enable-the-new-wave-step-method-for-existing-wave-templates"></a>Aktivere den nye metode til bølgetrin manuelt for eksisterende bølgeskabeloner

Start med at oprette den nye metode til bølgetrin, og aktivér den til parallel asynkron opgavebehandling.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**.

1. Vælg  **Genopret metoder**, og bemærk, at *WSScheduleWorkCreationUroStepMethod* er føjet til listen over metoder til behandling af bølger, du kan bruge i dine forsendelsesbølgeskabeloner.

1. Vælg posten med **Metodenavn** *WSScheduleWorkCreationHodStepMethod*, og vælg **Opgavekonfiguration**.

1. Gå til handlingsruden, og vælg **Ny** for at føje en ny række til gitteret med følgende indstillinger:

    - **Lagersted** – Vælg det lagersted, som du vil bruge til at planlægge behandling af oprettelse af arbejde.

    - **Maksimalt antal batchopgaver** – Angiv et maksimalt antal batchopgaver. I de fleste tilfælde skal denne værdi være i intervallet fra 8-16, men du anbefales at eksperimentere med den optimale indstilling baseret på dine scenarier.

    - **Batchgruppe til bølgebehandling** – Vælg en dedikeret batchgruppe til behandling af bølger for at optimere batchkøbehandlingen.

Nu er du klar til at opdatere en eksisterende bølgeskabelon (eller oprette en ny) til at bruge metoden *Planlæg oprettelse af arbejde* til bølgebehandling.

1. Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.

1. Vælg **Rediger** i handlingsruden.

1. I listeruden skal du vælge den bølgeskabelon, som du vil opdatere (hvis du tester med demodata, kan du bruge *24 Standard for forsendelse*).

1. Udvid oversigtspanelet **Metoder**, og vælg rækken med **Navn** *Planlæg oprettelse af arbejde* i gitteret **Resterende metoder**.

1. Vælg pilen, der peger på kolonnen **Valgte metoder**, så den valgte række flyttes til den pågældende kolonne. (Du kan kun have én valgt metode ad gangen, der bruger enten *WSScheduleWorkCreationHodStepMethod* eller *createWork*, så den eksisterende række med **Metodenavn** *createWork* automatisk flyttes til gitteret **Resterende metoder**).

## <a name="set-wave-task-processing-threshold-data"></a>Angive tærskeldata for behandling af bølgeopgave

Systemet opretter standardtærskeldata for behandling af bølgeopgaver, første gang en bølgeproces køres ved hjælp af opgavebaseret behandling. Dataene bruges til at styre, hvornår behandling af bølger vil køre asynkront og være opgavebaseret, hvilket gør det muligt at behandle og oprette arbejde parallelt.

Standarddataene vil først bruge en grænseværdi på 15 for minimumantallet af belastningslinjer (MINIMUMWAVELOADLINES). Det betyder, at når systemet behandler en bølge med mere end 15 belastningslinjer, vil systemet bruge asynkron opgavebehandling. Du kan manuelt indsætte/opdatere disse data i tabellen **WHSWaveTaskProcessingThresholdParameters** i testmiljøet, men hvis du har brug for at ændre denne indstilling i et produktionsmiljø, skal du kontakte Microsoft Support for at anmode om opdateringen.

## <a name="work-with-the-feature"></a>Arbejde med funktionen

Når funktionen *Planlæg oprettelse af arbejde* er aktiveret, opretter bølgebehandling det planlagte arbejde, som senere vil blive brugt af den nye arbejdsoprettelsesproces. Under oprettelse af arbejde blokeres arbejdet ved hjælp af funktionen *Blokering af arbejde i hele organisationen*.

Følgende rutediagram viser, hvordan planlagt arbejde oprettes under bølgebehandling.

![Planlæg arbejdsoprettelse](media/schedule-work-creation-process.png)

### <a name="planned-work"></a>Planlagt arbejde

På siden **Detaljer om planlagt arbejde** (**Lokationsstyring \> Arbejde \> Detaljer om planlagt arbejde**) vises oplysninger om det planlagte arbejde, der oprindeligt blev oprettet under behandling af bølger. Følgende værdier af **Processtatus** er tilgængelige:

- **Sat i kø** – Det planlagte arbejde venter på at blive brugt til at oprette arbejde.
- **Fuldført** – Det planlagte arbejde er brugt til at oprette arbejde.
- **Mislykkedes** – Bølgebehandlingen er mislykket. Bemærk, at det planlagte arbejde kan være i tilstanden **Mislykkedes** med eller uden relateret faktisk arbejde. Når den faktiske arbejdsoprettelsesproces mislykkes, forbliver det faktiske arbejde med status *Annulleret*.

### <a name="batch-job-for-the-work-creation-process"></a>Batchjob for processen til oprettelse af arbejde

Hvis du vil have vist batchjobbene til behandling af bølger, skal du vælge **Batchjob** i handlingsruden på siden **Alle bølger**.

Herfra kan du få vist alle oplysninger om batchopgaven for hvert enkelt batchjob-id.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]