---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 19. april 2021
description: I denne artikel beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 19. april 2021.
author: marcelbf
ms.date: 04/19/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: marcelbf
ms.search.validFrom: 2021-04-19
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fffe9c042c71dc220179bb6d1ba7fd59d5e53cc0
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9069527"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-april-19-2021"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 19. april 2021

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I denne artikel beskrives funktioner, der enten er nye, ændrede eller kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2021-udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.4113.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Platform update 10.0.17 (41) | -- | [Platformsopdateringer til version 10.0.17 af programmer til finans og drift (april 2021)](../fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-17.md) |
| Understøttelse af brugerdefinerede felter i formularer for Administration af frynsegoder | [Understøttelse af brugerdefineret felt i administration af frynsegoder](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-benefits-management)| [Oversigt over administration af frynsegoder](hr-benefits-management-overview.md)|

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis denne artikel til at omfatte fejlrettelser, som blev udført i buildet, efter at denne artikel blev udgivet.

| Fejlnummer | Problem |  Beskrivende tekst |
| --- | --- | --- |
| 552164 | **Gemt visning** for **Medarbejderselvbetjening > Åbne kurser** fungerer ikke for kurser, der indeholder en agenda | Hvis der bruges en gemt visning for åbne kurser (ESS), og et af kurserne har en tilknyttet agenda, vises der ikke flere linjer for dette kursus i visningen. |
| 560614 | **Frynsegoder > Indstillinger for livshændelser** viser uoverensstemmelser i dokumentationen for værktøjstip og kodefunktionsmåden. | Opdaterede værktøjstip i **Indstillinger for livshændelser** for at vise en korrekt funktionsmåde. |
| 560616 | **Frynsegoder > Indstillinger for livshændelser** kan redigeres i medarbejderens frynsegkodeplan, men ændringerne påvirkes ikke. | Opdateret funktionsmåde for Indstillinger af livshændelser skifter for at aktivere eller deaktivere ud fra afhængige indstillinger ifølge dokumentationen for værktøjstip. |
| 565054 | Det er ikke muligt at få vist indholdet af listen **Arbejdere uden ansættelse**, når **Avanceret adgang** er aktiveret. | Denne version løser problemet, når **Avanceret adgang** er aktiveret, og kun systemadministratorer kan se indholdet af listen **Arbejderne uden ansættelse**. Da denne rettelse er en sikkerhedsændring, skal du vælge den til i Funktionsstyring. Når funktionen er aktiveret, vil de roller, der har adgang til formularen, kunne se indholdet, selvom den avancerede adgang er slået til. Du kan finde flere oplysninger i [Arbejdere uden ansættelse](hr-personnel-workers-without-employment.md). |
| 570586 | Godkendelse af anmodning om orlov mislykkes, når ansættelsen slutter før den seneste transaktion for den pågældende arbejder på tværs af alle orlovsplaner. | Efter ophøret af en ansættelse mislykkes valideringen af orlovsanmodningen ikke ud fra medarbejderens orlovstransaktioner.|
| 570783 | Aktivering og deaktivering af orlov på tværs af virksomheder i de delte parametre for Human Resources ændrer, hvad medarbejdere, der er ansat i en enkelt virksomhed, kan se i orlovsanmodninger. | Medarbejdere, der er ansat i en enkelt virksomhed, kan ikke se ændringer i anmodningen om fridage, hvis parameteren er aktiveret eller deaktiveret. |
| 572343 | Den krævede årsagskode vises ikke, når funktionen for orlov på tværs af virksomheder er aktiveret. | Når funktionen for orlov på tværs af virksomheder er aktiveret, vises årsagskoden nu som forventet. |
| 573676 | Du kan ikke føje **Periode** til **Administration af frynsegoder > Links > Frynsegodeplaner**. | Løste fejl, hvor **Periode** ikke kunne tilføjes eller opdateres på den eksisterende formular for **Frynsegodeplan**. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Arbejdsområde for personalegodeadministration | [Arbejdsområdet Administration af frynsegoder (forhåndsversion)](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/benefits-management-workspace) | [Arbejdsområde for frynsegodeadministration](hr-benefits-management-workspace.md) |
| Forbedringer af arbejdsgang for orlov og fravær | [Forbedringer af arbejdsgang for orlov og fravær](https://go.microsoft.com/fwlink/?linkid=2147528) | [Anmod om fravær](hr-employee-self-service-request-time-off.md)|
| Aktivere forenklet lønintegration (API'er for lønintegration) | [Aktivere forenklet integration med lønudbydere](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/enable-simplified-integration-payroll-providers) | [Lønintegration API](hr-admin-integration-payroll-api-introduction.md)|

## <a name="coming-soon"></a>Kommer snart

| Funktion | Detaljer |
| --- | --- |
| Færdigheder, der angives af en leder for deres medarbejdere, kan godkendes automatisk af et arbejdsflow | Kommer snart. |
| Platform update 10.0.18 (42) | Platformsopdatering 10.0.18 er planlagt til at starte udrulning med servicefrigivelse den 17. maj 2021. Du kan få mere at vide i [Platformsopdateringer til version 10.0.18 af programmer til finans og drift (maj 2021)](/dynamics365/fin-ops-core/dev-itpro/get-started/whats-new-platform-updates-10-0-18). |
| Understøttelse af brugerdefineret felt i berettigelsesregler for administration af frynsegoder  | [Understøttelse af brugerdefineret felt for behandling af berettigelse](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/custom-field-support-eligibility-processing) |

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2021 udgivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2021 frigivelsesbølge 1](/dynamics365-release-plan/2021wave1/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]

