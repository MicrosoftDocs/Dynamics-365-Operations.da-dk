---
title: "Opsætning af dele af et job"
description: "I dette emne beskrives de grundlæggende elementer, at en sag kan indeholde, og giver eksempler på, hvordan du kan bruge disse elementer i din organisation."
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: d96b1f01a5cb4370436888deae8fd4835a0dbb80
ms.openlocfilehash: b8143db5b133337603a7f2f46028d91bb81cd947
ms.lasthandoff: 03/31/2017


---

# <a name="setting-up-the-components-of-a-job"></a>Opsætning af dele af et job

I dette emne beskrives de grundlæggende elementer, at en sag kan indeholde, og giver eksempler på, hvordan du kan bruge disse elementer i din organisation. 

Før du kan oprette job, skal du konfigurere nogle referenceoplysninger. Du kan oprette et job, der er kun et navn. Ved at medtage yderligere oplysninger, såsom en stilling, skal du dog angive standardværdier for de stillinger, der er tilknyttet jobbet. Nogle af de oplysninger, du indtaster kan desuden bruges til at filtrere kompensationsstrukturer til specifikke job. Hvis du vil konfigurere berettigelse, som du kan bruge til at filtrere kompensationsstrukturer til specifikke job, skal du angive jobfunktioner og jobtyper, før du konfigurerer job. Under disse standardværdier, der er tilgængelig, sparer du tid, når du tilføjer stillinger til jobbet. 

Nogle Jobdetaljer som titel, type og funktion, er datorelaterede. Disse detaljer vises ikke, hvis du opretter en sag i dag, men ikke tilføje disse oplysninger til senere, og du derefter se på jobbet til oprettelse af dato. Derfor skal du oprette nogle af denne oplysninger før du har brug for den. På den måde, du kan føje oplysninger til nye job, når du opretter dem..

## <a name="job-titles"></a>Stillingsbetegnelser
Før du opretter job, skal du konfigurere stillingsbetegnelser for jobbene. Stillinger arver stillingsbetegnelser fra de job, som stillingerne er tilknyttet. 

Vedligehold stillinger ved hjælp af den **titler** side, som du kan åbne ved hjælp af søgefunktionen. På den ** titler ** skal du angive de overskrifter, som du vil bruge til dit job.

## <a name="job-types"></a>Jobtyper
Du kan bruge jobtyper til at gruppere lignende job i kategorier. Jobtyper er ikke påkrævet. Hvis du planlægger at bruge jobtyper, når du konfigurerer berettigelsesregler for kompensationsstyring, skal du dog konfigurere jobtyper, før du konfigurerer job. Nogle eksempler på jobtyper er på fuld tid og deltid eller løn- og time løn. Du kan vedligeholde jobtyper ved hjælp af den **jobtyper** side. På den **jobtyper** skal du angive et navn og en kort beskrivelse til jobtypen. I den **fritage status** skal du vælge en af følgende indstillinger for at angive Fair Labor standarder Act (FLSA) undtaget status for job med denne jobtype:

-   **Se** – job er fritaget for overtid i henhold til FLSA.
-   **Ikke-fritaget** – job er ikke fritaget for overtid i henhold til FLSA.
-   **Gælder ikke** – FLSA-dækning er ikke relevant.

## <a name="job-functions"></a>Jobfunktioner
Job kryds beskriver overordnede funktionelle kategorier og relatere overordnede opgaver. Jobfunktioner er ikke påkrævede. Du kan bruge jobfunktioner sammen med jobtyper til at filtrere kompensationsstrukturer til specifikke job. Du knytte jobfunktioner og jobtyper til kompensationsplaner ved at oprette berettigelsesregler i den **berettigelsesregler** side. Derefter kan du knytte et sæt niveauer til en lønstruktur, der gælder for den specifikke kombination af en jobtype og jobfunktion, du har defineret gennem en berettigelsesregel. (Disse funktioner kan bruges til både fast løn-strukturer og variable lønstrukturer.) Hvis du planlægger at bruge jobfunktioner, når du konfigurerer berettigelsesregler for kompensationsstyring, skal du dog konfigurere jobfunktioner, før du konfigurerer job. I følgende tabel vises nogle eksempler på jobfunktioner.

| Stilling           | Jobfunktion      |
|---------------|-------------------|
| Salgsdirektør | Mellemstore Manager |
| Bogholder    | Fagfolk     |

Du kan vedligeholde jobfunktioner ved hjælp af den **jobfunktioner,** side. På den **jobfunktioner,** skal du angive et id og en kort beskrivelse af jobfunktionen.

## <a name="job-tasks"></a>Arbejdsopgaver
Sagsopgaver beskriver de grundlæggende opgaver, der skal udføre en arbejder, der er i stand til en sag. Samme arbejdsopgave kan føjes til flere job og stillinger for de job, der bruger disse opgaver. I følgende tabel vises nogle eksempler på opgaver.

<table>
<thead>
<tr class="header">
<th>Stilling</th>
<th>Arbejdsopgave</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td>Salgsdirektør</td>
<td><ul>
<li><strong>Performance-gennemgang</strong> – gennemse hver sælgers job ydeevne.</li>
<li><strong>Fraværsgennemgang</strong> – Godkend eller afvis anmodninger om fravær eller registreringer for hver sælger.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bogholder</td>
<td><strong>FINSK-rapport</strong> – forelægge den Økonomichef ugentlige finansielle rapporter.</td>
</tr>
</tbody>
</table>

Du kan vedligeholde opgaver ved hjælp af den **sagsopgaver** side. På den **sagsopgaver** skal du angive et navn og en beskrivelse af sagsopgaven. I den **Note** du kan eventuelt angive yderligere oplysninger. Noterne kan blive opdateret for et bestemt job, uden at ændre de noter, du har angivet her.

## <a name="areas-of-responsibility"></a>Ansvarsområder
Du kan bruge ansvarsområder til at angive de arbejdsroller, processer og produkter, der er ansvarlig for en arbejder, der er i stand til en sag. For eksempel for en sag, der hedder "Bogholder", kan et ansvarsområde være "Finansiel rapportering for vare A." Du kan vedligeholde ansvarsområder ved hjælp af den **ansvarsområder** side, som du kan finde ved hjælp af søgefunktionen. På den **ansvarsområder** skal du angive et navn og en beskrivelse af ansvarsområdet. I den **Note** du kan eventuelt angive yderligere oplysninger. Noterne kan blive opdateret for et bestemt job, uden at ændre de noter, du har angivet her.


