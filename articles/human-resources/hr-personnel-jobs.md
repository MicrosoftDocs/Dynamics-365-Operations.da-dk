---
title: Konfigurere komponenterne i et job
description: I denne artikel beskrives de grundlæggende elementer, som en sag kan indeholde, og der gives eksempler på, hvordan du kan bruge disse elementer i din organisation.
author: twheeloc
ms.date: 10/28/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle, HcmPersonnelManagementWorkspace, HCMJobFamily
audience: Application User
ms.author: twheeloc
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: afe100879a4f83e4ef16048bc4b1acace19b679b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877708"
---
# <a name="set-up-the-components-of-a-job"></a>Konfigurere komponenterne i et job


[!INCLUDE [PEAP](../includes/peap-1.md)]

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives de grundlæggende elementer, som en sag kan indeholde, og der gives eksempler på, hvordan du kan bruge disse elementer i din organisation. 

Når du vil oprette job, skal du først konfigurere visse referenceoplysninger. Du kan oprette et job, der kun har et navn. Du kan dog også medtage yderligere oplysninger, som f.eks. en stillingsbetegnelse, og derved angive standardværdier for de stillinger, der er tilknyttet jobbet. Desuden kan nogle af de oplysninger, du angiver, bruges til at filtrere kompensationsstrukturer til specifikke job. Hvis du vil oprette berettigelse, som du kan bruge til at filtrere lønstrukturer til et bestemt job, skal du konfigurere jobfunktioner og jobtyper, før du konfigurerer job. Når disse standardværdier er tilgængelige, sparer du tid, når du tilføjer stillinger til jobbet. 

Nogle jobdetaljer som f.eks. stillingsbetegnelse, type og funktion er datorelaterede. Hvis du opretter et job i dag, men først tilføjer disse detaljer senere, og derefter ser på jobbet pr. oprettelsesdatoen, vises disse detaljer ikke. Derfor skal du oprette nogle af disse referenceoplysninger, før du får brug for dem. På den måde kan du føje oplysningerne til nye job, når du opretter dem.

## <a name="job-titles"></a>Stillingsbetegnelser
Før du opretter job, skal du konfigurere stillingsbetegnelser for jobbene. Stillinger arver stillingsbetegnelser fra de job, som stillingerne er tilknyttet. 

Vedligehold stillingsbetegnelser ved hjælp af siden **Titler**, som du kan åbne ved hjælp af søgefunktionen. På siden **Titler** skal du angive de stillingsbetegnelser, som du vil bruge til dine job.

## <a name="job-types"></a>Jobtyper
Du kan bruge jobtyper til at gruppere lignende job i kategorier. Jobtyper er ikke nødvendige. Hvis du planlægger at bruge jobtyper, når du konfigurerer berettigelsesregler for kompensationsstyring, skal du dog konfigurere jobtyper, før du konfigurerer job. Nogle eksempler på jobtyper er fuldtids og deltids eller fastlønnede og timelønnede. Du kan vedligeholde jobtyper fra siden **Jobtyper**. Angiv et navn og en kort beskrivelse af stillingstypen på siden **Jobtyper**. I feltet **Momsfri status** skal du vælge en af følgende indstillinger for at angive Fair Labor Standards Act (FLSA) fritagelsesstatus for job med denne jobtype:

-   **Frit** – Job er fritaget for overtid i henhold til FLSA.
-   **Ikke-momsfri** – Job er ikke fritaget for overtid i henhold til FLSA.
-   **Gælder ikke** – FLSA-dækning er ikke relevant.

## <a name="job-family"></a>Jobserie
En jobfamilie er en gruppe job, der involverer lignende arbejde, og som kræver lignende uddannelse, færdigheder, viden og ekspertise. En jobfamilie kan knyttes til et job i oversigtspanelet **Jobklassifikation** på siden **Job** og i oversigtspanelet **Generelt** på siden **Alle stillinger**. Jobfamilier kan være brede eller specifikke, afhængigt af virksomheden og rapporteringskravene. Eksempler på brede jobfamilier kan være **Faglærtarbejdskraft** og **Ufaglært arbejdskraft**. Eksempler på bestemte jobfamilier kan være **Regnskab**, **Produktion** og **Salg**.

Vedligehold jobfamilier ved hjælp af siden **Jobfamilie**, som du kan åbne ved hjælp af søgefunktionen. På siden **Jobfamilie** skal du angive et entydigt navn til familien og angive en detaljeret beskrivelse, som du vil bruge til dine job.

## <a name="job-functions"></a>Jobfunktioner
Jobfunktioner beskriver overordnede funktionelle kategorier og relaterede overordnede opgaver. Jobfunktioner er ikke nødvendige. Du kan bruge jobfunktioner sammen med jobtyper til at filtrere kompensationsstrukturer til specifikke job. Du kan knytte jobfunktioner og jobtyper til kompensationsplaner ved at oprette berettigelsesregler på siden **Berettigelsesregler**. Du kan derefter knytte et sæt niveauer til en kompensationsplan, der gælder for den specifikke jobtype/jobfunktionskombination, som du har defineret ved hjælp af en berettigelsesregel. (Disse funktioner gælder både for faste og variable kompensationsplaner). Men hvis du planlægger at bruge jobfunktioner, når du konfigurerer berettigelsesregler for kompensationsstyring, skal du dog konfigurere jobfunktioner, før du konfigurerer job. Følgende tabel indeholder nogle eksempler på jobfunktioner.

| Stilling           | Jobfunktion         |
|---------------|----------------------|
| Salgsdirektør | Chef på mellemlederniveau    |
| Bogholder    | Professionelle        |

Du kan vedligeholde jobfunktioner på siden **Jobfunktioner**. Angiv en identifikationskode og en kort beskrivelse af jobfunktionen på siden **Jobfunktioner**.

## <a name="compensation"></a>Kompensation
Hvis du vil tildele en plan for fast løn til en medarbejder, der har en stilling i et job, skal du angive kompensationsniveauer for jobbet. **Kompensationsniveau** bruges, når minimum-, mellem- og maksimumbeløb angives i en kompensationsstruktur (kompensationsgitter). Når der oprettes plan for fast løn, vælges kompensationsstrukturen. Kompensationsstrukturen inkluderer også kompensationsniveauet. Når du vælger en plan for fast løn for en medarbejder, afhænger de kompensationsniveauer, der kan vælges, af det job, som medarbejderens stilling er tilknyttet. Du kan finde flere oplysninger om, hvordan du konfigurerer kompensation, under [Kompensationsplaner](hr-compensation-overview.md).

## <a name="job-skills"></a>Jobkompetencer
Jobkompetencer beskriver de kompetencer, der kræves for at udføre et job. Der skal knyttes et kompetenceniveau til hver jobkompetence. Kompetenceniveauerne er brugerdefinerede. De angiver det videns- eller færdighedsniveau, der kræves til kompetencen. Firmaer kan for eksempel oprette numeriske niveauer, for eksempel 1-5, hvor **1** betyder nybegynder, og **5** betyder ekspert. Alternativt kan firmaer oprette niveauer med navnet **Nybegynder**, **Mellem** eller **Ekspert**. Når kompetenceniveauet er angivet, kan vigtigheden af kompetencen også angives. Hvis en bogholder for eksempel skal have stor viden om Microsoft Excel, kan der oprettes en færdighed ved navn **Excel-viden**. Kompetenceniveauet kan derefter angives til **Mellem**, og vigtigheden kan angives til **Mest**.

De kompetencer, der findes for et job, kan bruges til kompetencetilknytning. Kompetencetilknytning kan sammenligne de kompetencer, der kræves for et job, og de kompetencer, der er knyttet til en arbejder. Derefter kan den bestemme et procentvist match på basis af overlappende kompetencer. Du kan få mere at vide om kompetencetilknytning under [Konfigurere kompetencer](hr-develop-skills.md). 

## <a name="job-tasks"></a>Arbejdsopgaver
Arbejdsopgaver beskriver de grundlæggende opgaver, der skal udføres af en arbejder, der er i position for et job. Samme arbejdsopgave kan føjes til flere job og til stillinger for de job, der bruger disse arbejdsopgaver. Følgende tabel indeholder nogle eksempler på arbejdsopgaver.

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
<li><strong>Performance-gennemgang</strong> – Gennemgang af en sælgers jobperformance.</li>
<li><strong>Fraværsgennemgang</strong> – Godkend eller afvis en sælgers fraværsanmodninger eller registreringer.</li>
</ul></td>
</tr>
<tr class="even">
<td>Bogholder</td>
<td><strong>Regnskabsrapport</strong> – Forelæg ugentlige regnskaber til regnskabsdirektøren.</td>
</tr>
</tbody>
</table>

Du kan vedligeholde arbejdsopgaver fra siden **Arbejdsopgaver**. Angiv et navn til og en beskrivelse af arbejdsopgaven på siden **Arbejdsopgaver**. I feltet **Notat** kan du også yderligere oplysninger. Noterne kan blive opdateret for et bestemt job, uden at det ændrer de noter, du har angivet her.

## <a name="areas-of-responsibility"></a>Ansvarsområder
Du kan bruge ansvarsområder til at angive arbejdsroller, processer og produkter, som en arbejder, der er i stilling til et job, er ansvarlig for. Et eksempel for et job med titlen "Bogholder" kunne et ansvarsområde være "Økonomirapportering for produkt A". Du kan vedligeholde ansvarsområder ved hjælp af siden **Ansvarsområder**, som du kan finde ved hjælp af søgefunktionen. Angiv et navn til og en beskrivelse af ansvarsområdet på siden **Ansvarsområder**. I feltet **Notat** kan du også yderligere oplysninger. Noterne kan blive opdateret for et bestemt job, uden at det ændrer de noter, du har angivet her.

## <a name="steps-for-creating-a-job"></a>Trin til oprettelse af et job
Se artiklen emnet [Definere nye job](./hr-personnel-define-jobs.md) for den trinvise procedure til at oprette et nyt job. 


[!INCLUDE[footer-include](../includes/footer-banner.md)]
