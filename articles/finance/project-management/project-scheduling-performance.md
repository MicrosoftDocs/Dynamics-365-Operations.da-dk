---
title: Ydeevne af projektressourceplanlægning
description: Dette emne beskriver, hvordan du kan forbedre ydeevnen af ressourceplanlægningen for et større antal projekter.
author: Yowelle
manager: AnnBe
ms.date: 08/31/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Service industries
ms.author: v-radsh
ms.dyn365.ops.version: 10.0.14
ms.search.validFrom: 2020-09-01
ms.openlocfilehash: 988fc83230f08a6534caa7c37784757d73c1cc12
ms.sourcegitcommit: 241ada0945c72d769eaa70ae35aedbb6a3233fdf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/02/2020
ms.locfileid: "3760509"
---
# <a name="project-resource-scheduling-performance"></a>Ydeevne af projektressourceplanlægning

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]


Ydeevneproblemer relateret til ressourceplanlægning kan forekomme, når antallet af projekter når op på tusinder. For at forbedre ydeevnen i ressourceplanlægningen er der en tilgængelig funktion, der giver brugerne mulighed for at reducere den tid, det tager at starte formularen Ressourcetilgængelighed. Dette fjerner specifikt synkroniseringsprocessen til akkumuleringer af ressourcekapacitet og bruger tabellen **ResProjectResource** til at øge ressourceopslaget. Bemærk, at tabellen **ResRollup** ikke længere vil blive brugt.

> [!IMPORTANT]
> Hvis der er en afhængighed af enten synkroniseringsprocessen til akkumuleringer af ressourcekapacitet eller tabellen **ResProjectResource**, skal du ikke bruge denne funktion.

## <a name="enable-resource-scheduling-performance-enhancement"></a>Aktivere forbedring af ydeevne for ressourceplanlægning
Hvis du vil aktivere forbedringer af ydeevnen for ressourceplanlægning, skal du udføre følgende trin.

1. Gå til **Funktionsstyring** > **Alle**, og find **Aktivér funktionen til forbedring af ydeevnen for projekt ressourceplanlægning** på funktionslisten.
2. Vælg **Aktiver nu**.

> [!NOTE]
> Hvis du ikke kan finde funktionen på listen, skal du vælge **Søg efter opdateringer** for at opdatere listen.

3. Opdater browseren, og gå derefter til **Projektstyring og regnskab** > **Periodisk** > **Projektressourcer** > **Synkroniser ressourcekalenderkapacitet på tværs af alle firmaer**.
4. Angiv **Fjern eksisterende kapacitetsposter** til **Ja** for at fjerne tidligere data. Hvis du vil oprette trinvise data, skal du angive den til **Nej**.
5. Vælg den periode, hvor der skal genereres data, i feltet **Periodekode**. Hvis du vælger en periodekode, skal der ikke defineres en start- og slutdato.
6. Hvis du ikke udfylder feltet **Periodekode**, skal du vælge bestemte start- og slutdatoer for at oprette data.
7. Vælg **OK**.

 > [!NOTE]
 > Dette vil distribuere generelle data til tabellen **ResCalendarCapacity** på tværs af alle firmaer i dit miljø, så batchjobbet kun skal køres i én juridisk enhed. Dataene i dette batchjob skal bruges til at beregne ressourcekapaciteten via den tilknyttede kalender.

8. Gå til **Projektstyring og regnskab** > **Periodisk** > **Projektressourcer** > **Udfyld projektressourcer på tværs af alle firmaer**, og vælg derefter **OK**. Dette er scriptet til dataopgradering for generelle data i tabellerne **ResProjectResource**, **ResCalendarDateTimeRange** og **ResEffectiveDateTimeRange**. Værdierne for feltet **PSAPRojSchedRole.RootActivity** opdateres også. Hvis dette ikke køres, vises der en advarsel, når du forsøger at udføre ressourceplanlægningshandlinger.
 
## <a name="turn-off-resource-scheduling-performance-enhancement"></a>Deaktivere forbedring af ydeevne for ressourceplanlægning

1. Gå til **Funktionsstyring** > **Alle**, og søg efter **Aktivér funktionen til forbedring af ydeevnen for projekt ressourceplanlægning**.
2. Vælg funktionen, og vælg derefter knappen **Deaktiver**.
3. Opdater browseren.
4. Gå til **Projektstyring og regnskab** > **Periodisk** > **Kapacitetssynkronisering** > **Synkroniser ressourcekapacitet, opkøb**.
5. På siden **Kapacitetsopkøb, synkronisering** skal du angive **Fjern eksisterende kapacitetsposter** til **Ja** for at fjerne tidligere data. Hvis du vil oprette trinvise data, skal du angive den til **Nej**.
6. Vælg den periode, hvor der skal genereres data, i feltet **Periodekode**. Hvis du vælger en periodekode, skal der ikke defineres en start- og slutdato.
7. Hvis du ikke udfylder feltet **Periodekode**, skal du vælge bestemte start- og slutdatoer for at oprette data.
8. Vælg **OK**.

> [!NOTE]
> Dette vil distribuere generelle data til tabellen **ResRollup** på tværs af alle firmaer i dit miljø, så batchjobbet kun skal køres i én juridisk enhed. Dette batchjob er nødvendigt for alle visninger af **Ressourcetilgængelighed**. Hvis dette batchjob ikke køres, vil **ResRollup**-data blive genereret løbende, hvilket kan tage lang tid.
