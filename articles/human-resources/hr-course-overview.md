---
title: Oversigt over kurser
description: Denne artikel forklarer, hvordan Human Resources-administratorer og -chefer kan bruge kursusfunktionerne til at vedligeholde oplysninger om de kurser, der tilbydes til arbejdere.
author: twheeloc
ms.date: 08/26/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: a1fd00fb9feea9ab426f67095770389696452215
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2022
ms.locfileid: "9716332"
---
# <a name="courses-overview"></a>Oversigt over kurser

Microsoft Dynamics 365 Human Resources leverer en løsning, der opfylder organisationens uddannelsesbehov. Denne løsning indeholder to kursusstier: *virtuel* og *instruktørledet*.

*Virtuel læring* er en undervisningsoplevelse, der er forbedret via onlineressourcer. I *instruktørledet undervisning* står en instruktør i spidsen for en træningssession for en gruppe arbejdere eller kursister.

I vores undervisningsmodul kan Human Resources-medarbejdere, administratorer, træningsledere og chefer oprette og tildele arbejdere begge kursusstier.

> [!NOTE]
> Hvis du vil bruge virtuelle kurser, skal du aktivere funktionen **Kursusforbedringer** i Funktionsstyring.

## <a name="set-up-virtual-courses"></a>Konfigurere virtuelle kurser

Hvis du vil konfigurere virtuelle kurser, skal du aktivere funktionen **Kursusforbedringer** i Funktionsstyring. Gå til **Kurser \> Nye**, og angiv indstillingen **Virtuel** til **Ja**. Når funktionen er aktiveret, skal der bruges et kursuslink. Feltet **Kursusstatus** angives til **Åben**. Indstillingen **Tillad medarbejderselvregistrering** er angivet til **Ja**, men kan angives til **Nej**.

Når funktionen **Kursusforbedringer** er aktiveret i Funktionsstyring, sker følgende ændringer:

- Der skal angives en forfaldsdato for kursustildelingen.
- Der skal være et kursuslink.
- **Medarbejderselvbetjening** viser en medarbejderoversigt i **Kurser**. Brugeren kan se kurser, der er forsinkede, forfalder snart og tildelte.
- Arbejdere kan gennemføre virtuelle kurser og selv attestere dem.

## <a name="set-up-instructor-led-courses"></a>Definere instruktørledede kurser

Det er ikke nødvendigt at konfigurere instruktørledede kurser, før de kan bruges.

Følgende oplysninger er valgfrie oplysninger, du kan angive dem for kurser. Hvis disse oplysninger skal angives for kurser, skal de konfigureres, før kursusposterne oprettes:

- Kursustype
- Kursuslokalegrupper
- Kursusgrupper
- Kursussteder
- Kursuslokaler
- Instruktører
- Kursustyper

Du kan bruge *kursustyper* til at kategorisere kurser efter deres struktur eller indhold. Du kan oprette kursustyper på siden  **Kursustyper** .

Det laveste og højeste antal deltagere, du kan tilmelde et kursus, er angivet i oversigtspanelet  **Generelt**  på siden  **Kurser** .

### <a name="course-setup-type"></a>Opsætningstype for kursus 

*Opsætningstyper* bestemmer kursets struktur. Der er tre opsætningstyper for kurser.

| Konfigurationstype | Beskrivende tekst |
|------|--------|
| Standard | Kurser af denne opsætningstype har ikke en daglig agenda. Det er standardopsætningstypen, når du opretter et nyt kursus. |
| Agenda | Vælg denne opsætningstype for at planlægge detaljerne for hver dag i et kursus, der finder sted over flere dage. |
| Agenda + session | <p>Vælg denne opsætningstype for mere komplekse kurser. For eksempel kan du opdele agendaen for kurset i *spor* og *sessioner*.</p><ul><li>*Spor* er specifikke emneområder for et kursus.</li><li>*Sessioner* underopdeler spor og hjælper med at identificere specifikke processer eller teknikker, der er relevante for sporet.</li></ul> |

### <a name="course-tasks"></a>Kursusopgaver

For hvert kursus skal følgende opgaver fuldføres:

- Registrer deltagere.
- Angive en tilmeldingsfrist.
- Angive det mindste og største antal deltagere.
- Tildel et kursussted og et lokale.
- Anbefal hoteller til kursusdeltagere.
- Opret en kursusbeskrivelse, som kan offentliggøres på  **Medarbejderselvbetjening**.

> [!NOTE]
> Du kan kun slette et kursus, hvis ingen har tilmeldt sig kurset.

### <a name="course-statuses"></a>Kursusstatusser

Følgende tabel indeholder statusser for kurset og de handlinger, der er fuldført for hvert af dem.

| Status | Handlinger |
|------|--------|
| Oprettet den | <ul><li>Angiv og rediger kursusoplysninger.</li><li>Ret status for kurset til  **Åben**, så medarbejderne kan tilmelde sig kurset.</li></ul> | 
| Åbent | <ul><li>Meld deltagerne til kurset.</li><li>Fjern deltagere fra kurset.</li><li>Bekræfte deltageres tilmelding til kurset.</li><li>Skift status for kurset til  **Lukket**  eller  **Annulleret** for deltagere, hvis status er  **Bekræftet**.</li></ul>|
| Lukket | Du kan genåbne kurset. |
| Annulleret | Du kan genåbne kurset. |

### <a name="course-participants"></a>Kursusdeltagere

*Kursusdeltagere* er arbejdere, der deltager i et kursus eller anden undervisning. Du kan kun melde deltagere til åbne kurser.

### <a name="workflow"></a>Arbejdsgang

Medarbejdere, der tilmelder sig et kursus på siden  **Medarbejderselvbetjening** , kan få deres tilmelding dirigeret gennem godkendelsesarbejdsgangen. Du kan tildele en arbejdsgang et kursus i oversigtspanelet  **Generelt**  på siden  **Kurser** .
