---
title: Planlægge oprettelse af arbejde under bølge
description: I dette emne beskrives, hvordan du kan konfigurere og bruge behandlingsmetoden til planlægning af arbejdsoprettelse i bølge.
author: perlynne
ms.date: 01/14/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSPostMethod, WHSWavePostMethodTaskConfig, WHSWaveTemplateTable, WHSParameters, WHSWaveTableListPage, WHSWorkTableListPage, WHSWorkTable, BatchJobEnhanced, WHSPlannedWorkOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-01-14
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 5e9dc9b7cf33f9393f408d8f8a458e9b0ea47639
ms.sourcegitcommit: 8cb031501a2b2505443599aabffcfece50e01263
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/09/2021
ms.locfileid: "7778371"
---
# <a name="schedule-work-creation-during-wave"></a>Planlægge oprettelse af arbejde under bølge

[!include [banner](../../includes/banner.md)]

Brug funktionen *Planlæg oprettelse af arbejde* som en del af din bølgeproces for at øge gennemløbet af bølgearbejde ved at lade systemet oprette arbejde via parallel behandling.

Når funktionaliteten er aktiveret, oprettes der automatisk planlagt arbejde, som systemet i den sidste ende behandler for at oprette faktisk arbejde. Hvis antallet af bølgelastlinjer når en foruddefineret grænseværdi, opretter systemet det faktiske arbejde hurtigere ved at anvende parallel asynkron behandling.

## <a name="turn-on-the-scheduled-work-creation-features-in-feature-management"></a>Aktivere funktioner til planlagt oprettelse af arbejde i funktionsstyring

Hvis du vil bruge de funktioner, der er beskrevet i dette emne, skal de være aktiverede for systemet. I arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) skal du aktivere følgende funktioner i følgende rækkefølge:

1. **Arbejdsblokering for hele organisationen** – Kræves til både manuel og automatisk konfiguration af planlagt oprettelse af arbejde. (Fra og med Supply Chain Management version 10.0.21 er denne funktion obligatorisk, så den er som standard aktiveret og kan ikke deaktiveres igen).
1. **Planlæg oprettelse af arbejde** – Kræves til både manuel og automatisk konfiguration af planlagt oprettelse af arbejde.
1. **Bølgemetoden "Planlæg oprettelse af arbejde" for hele organisationen** – Kræves til automatisk konfiguration af planlagt oprettelse af arbejde. Du har ikke brug for denne funktion, hvis du kun vil bruge manuel konfiguration.

<a name="Auto-enable-schedule-work-creation"></a>

## <a name="automatically-configure-scheduled-work-creation"></a>Konfigurere planlagt oprettelse af arbejde automatisk

Hvis du aktiverer funktionen *Bølgemetoden "Planlæg oprettelse af arbejde" for hele organisationen*, sker følgende automatisk på systemet:

- Bølgemetoden *Planlæg arbejdsoprettelse* (`WHSScheduleWorkCreationWaveStepMethod`) tilføjes og konfigureres til at køre parallelt på tværs af alle juridiske enheder.
- Bølgeskabeloner fra alle juridiske enheder, hvor **Bølgeskabelontype** er angivet til *Forsendelse*, og **Skabelonstatus** er angivet til *Gyldig*, vil have metoden *Opret arbejde* erstattet af metoden *Planlæg arbejdsoprettelse*. Bølgeskabeloner fra juridiske enheder, hvor metoden *Opret arbejdse* kan gentages, ændres dog ikke.
- Opgavekonfigurationer for metoden *Planlæg arbejdsoprettelse* oprettes for alle lagersteder fra alle juridiske enheder, hvor **Brug processer til lokationsstyring** er aktiveret. Det betyder, at metoden *Planlæg arbejdsoprettelse* nu som standard køres parallelt. Eksisterende lagersteder, hvor du ændrer **Brug processer for lokationsstyring** fra *Nej* til *Ja*, kører også denne metode parallelt som standard.
- Alle juridiske enheder behandler bølger i batches, og **Vent på lås (ms)** angives til en standardværdi på *60.000* ms, hvis den tidligere var angivet til *0* ms.
- Alle de nye bølgeskabeloner, du opretter, har metoden *Planlæg arbejdsoprettelse* i stedet for metoden *Opret arbejde*.

De eksisterende konfigurationer til behandling af opgaver og bølger bevares også for alle juridiske enheder, der allerede er konfigureret til at behandle bølger i batches, og for alle lagersteder, der allerede er konfigureret til at bruge metoden *Planlæg arbejdsoprettelse* parallelt.

Hvis det er nødvendigt, kan du manuelt tilbagestille nogle af eller alle de indstillinger, der blev foretaget automatisk, da du aktiverede funktionen *Bølgemetoden Planlæg oprettelse af arbejde for hele organisationen*, ved at gøre følgende:

- For bølgeskabeloner skal du gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**. Erstat metoden *Planlæg oprettelse af arbejde* med *Opret arbejde*.
- For lagerstedsparametre skal du gå til **Lokationsstyring \> Konfiguration \> Parametre til lokationsstyring**. Anvend dine foretrukne værdier for **Udfør behandling af bølger i batch** og **Vent på lås (ms)** under fanen **Bølgebehandling**.
- For bølgemetoder skal du gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeprocesmetoder**. Vælg `WHSScheduleWorkCreationWaveStepMethod` i handlingsruden, og vælg **Opgavekonfiguration**. Rediger eller slet antallet af batchopgaver og den tildelte bølgegruppe for hvert af de viste lagersteder efter behov.

## <a name="manually-configure-scheduled-work-creation"></a>Konfigurere planlagt oprettelse af arbejde manuelt

Hvis du ikke aktiverede funktionen [*Bølgemetoden "Planlæg oprettelse af arbejde" for hele organisationen*](#Auto-enable-schedule-work-creation), kan du bruge de procedurer, der er angivet i dette afsnit, til manuelt at konfigurere planlagt arbejdsoprettelse efter behov.

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
1. Vælg pilen, der peger på kolonnen **Valgte metoder**, så den valgte række flyttes til den pågældende kolonne. (Du kan kun have én valgt metode ad gangen, der bruger enten `WHSScheduleWorkCreationWaveStepMethod` eller `createWork`, så den eksisterende række med **Metodenavn** `createWork` automatisk flyttes til gitteret **Resterende metoder**).

## <a name="set-wave-task-processing-threshold-data"></a>Angive tærskeldata for behandling af bølgeopgave

Systemet opretter standardtærskeldata for behandling af bølgeopgaver, første gang en bølgeproces køres ved hjælp af opgavebaseret behandling. Dataene bruges til at styre, hvornår behandling af bølger vil køre asynkront og være opgavebaseret, hvilket gør det muligt at behandle og oprette arbejde parallelt.

Standarddataene vil først bruge en grænseværdi på 15 for minimumantallet af belastningslinjer (`MINIMUMWAVELOADLINES`). Det betyder, at når systemet behandler en bølge med mere end 15 belastningslinjer, vil systemet bruge asynkron opgavebehandling. Du kan manuelt indsætte/opdatere disse data i `WHSWaveTaskProcessingThresholdParameters`-tabellen i testmiljøet. Hvis du vil ændre denne indstilling i et produktionsmiljø, skal du kontakte Microsoft Support for at anmode om opdateringen.

## <a name="work-with-the-scheduled-work-creation"></a>Arbejde med den planlagte oprettelse af arbejde

Du kan finde flere oplysninger om, hvordan du arbejder med planlagt oprettelse af arbejde, i [Bølgeoprettelse og -behandling](wave-processing.md). 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
