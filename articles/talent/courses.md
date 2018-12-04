---
title: Konfigurere uddannelseskurser
description: Personaleadministratorer og -chefer kan bruge kursusfunktionerne til at vedligeholde oplysninger om de kurser, der tilbydes til arbejdere.
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: rschloma
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 95d5bf26c22238753586cf4a7aaf5c26f061a705
ms.openlocfilehash: 27fbc54afca384b804f2b0468206242ff89d4031
ms.contentlocale: da-dk
ms.lasthandoff: 02/23/2018

---

# <a name="set-up-training-courses"></a>Konfigurere uddannelseskurser

[!include [banner](includes/banner.md)]

Personaleadministratorer og -chefer kan bruge kursusfunktionerne til at vedligeholde oplysninger om de kurser, der tilbydes til arbejdere.

 <a name="set-up-prerequisites"></a> Angiv forudsætninger
---------------------

Følgende oplysninger er påkrævet og skal konfigureres, før du opretter kurser.
-   **Kursustyper**

Følgende oplysninger er valgfrie oplysninger, du kan angive for kurser. Hvis du ved, at du kommer til at angive disse oplysninger for kurser, skal du konfigurere oplysningerne, før du opretter kursusposter.
-   **Kursuslokalegrupper**
-   **Kursusgrupper**
-   **Kursussteder**
-   **Kursuslokaler**
-   **Instruktører**

## <a name="course-types"></a>Kursustyper
Du kan bruge kursustyper til at kategorisere kurser efter kursets struktur eller indhold. Du kan oprette kursustyper på siden **Kursustyper**. Du skal vælge en kursustype, når du opretter en kursuspost.

## <a name="course-setup-type"></a>Opsætningstype for kursus
Følgende tabel viser de tre opsætningstyper for kurser. Opsætningstyper bestemmer kursets struktur.

<table>
<thead>
<tr class="header">
<th>Opsætningstype</th>
<th>Beskrivelse</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Standard</strong></td>
<td>Vælg denne type for kurser, der ikke har en daglig agenda. Dette er standardopsætningstypen, når du opretter et nyt kursus.</td>
</tr>
<tr class="even">
<td><strong>Agenda</strong></td>
<td>Vælg denne type for at planlægge detaljerne for hver dag i et kursus, der finder sted over flere dage.</td>
</tr>
<tr class="odd">
<td><strong>Agenda + session</strong></td>
<td>Vælg denne type for mere komplekse kurser. For eksempel kan du opdele agendaen for kurset i spor og sessioner.
<ul>
<li><strong>Spor</strong> – Spor er specifikke emneområder for et kursus.</li>
<li><strong>Sessioner</strong> – Sessioner underopdeler spor og hjælper med at identificere specifikke processer eller teknikker, der er relevante for sporet.</li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a>Kursusopgaver
For hvert kursus kan udføre følgende opgaver.
- Registrere deltagere
- Angive en tilmeldingsfrist
- Angive det mindste og største antal deltagere
- Tildel et kursussted og et lokale
- Anbefal hoteller til kursusdeltagere
- Oprette en kursusbeskrivelse, som derefter kan offentliggøres på Medarbejderselvbetjening

  >**Bemærk!** Du kan kun slette et kursus, hvis ingen har tilmeldt sig kurset. 

## <a name="course-statuses"></a>Kursusstatusser
I følgende tabel vises de mulige statusser for kurser og de handlinger, du kan udføre, når kurset har en bestemt status.

<table>
<thead>
<tr class="header">
<th>Status</th>
<th>Aktioner</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><strong>Oprettet</strong></td>
<td><ul>
<li>Angiv og rediger kursusoplysninger.</li>
<li>Rediger status for kurset til <strong>Åbn</strong>, så medarbejderne kan tilmelde sig kurset.</li>
</ul></td>
</tr>
<tr class="even">
<td><strong>Åben</strong></td>
<td><ul>
<li>Meld deltagerne til kurset.</li>
<li>Fjern deltagere fra kurset.</li>
<li>Bekræfte deltageres tilmelding til kurset.</li>
<li>Rediger status for kurset til<strong> Lukket</strong> eller <strong>Annulleret</strong>.</li>
<li>Planlæg spørgeskemaer for deltagere, som har status <strong>Bekræftet</strong>.</li>
</ul></td>
</tr>
<tr class="odd">
<td><strong>Lukket</strong></td>
<td>Du kan genåbne kurset.</td>
</tr>
<tr class="even">
<td><strong>Annulleret</strong></td>
<td>Du kan genåbne kurset.</td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a>Kursusdeltagere
Kursusdeltagere er arbejdere, jobansøgere eller kontaktpersoner, der deltager i et kursus eller anden undervisning. Du kan kun melde deltagere til åbne kurser. Det laveste og højeste antal deltagere, du kan tilmelde et kursus, er angivet i oversigtspanelet **Generelt** på siden **Kurser**.

<a name="workflow"></a>Arbejdsgang
--------

Medarbejdere, der tilmelder sig et kursus på siden **Medarbejderselvbetjening**, kan få deres tilmelding dirigeret gennem godkendelsesarbejdsgangen.  En arbejdsgang kan tildeles til et kursus i oversigtspanelet **Generelt** på siden **Kurser**.






