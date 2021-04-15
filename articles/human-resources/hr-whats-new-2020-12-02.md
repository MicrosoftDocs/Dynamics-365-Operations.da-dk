---
title: Nyheder eller ændringer i Dynamics 365 Human Resources 2. december 2020
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 2. december 2020.
author: marcelbf
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b7d9ecea08f5095e7fa8501d690bbabbd54e6501
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5802233"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-december-2-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources 2. december 2020

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

I dette emne beskrives funktioner, som er nye eller ændrede, eller som kommer snart i Dynamics 365 Human Resources.

Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [Opdateringsproces](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2020-udgivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.3788.

### <a name="new-features"></a>Nye funktioner

Følgende funktioner er generelt tilgængelige med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Ledere, der kan sende rekrutteringsanmodninger om stillinger | [Ledere, der kan sende en rekrutteringsanmodning om åbne stillinger](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Tilføje en rekrutteringsanmodning](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Udvidet kandidatprofil i Personalestyring | [Udvidet kandidatprofil i Personalestyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Tilføje eller redigere en kandidatprofil](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Muliggøre forenklet integration med rekrutteringsudbydere | [Muliggøre forenklet integration med rekrutteringsudbydere](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Rekruttere jobkandidater](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |
| Brugerdefinerede links i selvbetjening for leder | [Brugerdefinerede links i selvbetjening for leder](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service) | [Brugerdefinerede links i selvbetjening for leder](https://aka.ms/MSSCustomLinks) |


### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

> [!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Vi opdaterer muligvis dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Udsted | Beskrivelse |
| --- | --- | --- |
| 514087 | BenefitEligibilityProcessResult skal omfatte datetime, der blev brugt til behandlingen. | Resultatet af BenefitEligibity-behandlingen omfatter nu datetimestamp for seneste behandling, som manglede tidligere. |
| 526903 | Der kan ikke tilmeldes frynsegoder for planer med afhængige, når **Vælg automatisk udpegede modtagere** er aktiveret i **Delte parametre for personale**. | Problemet, når der ikke kunne registreres frynsegoder for de afhængige, når indstillingen **Vælg automatisk udpegede modtagere** var slået til for standard udpegede modtagere, er løst. |
| 521922 | Parameteren **Vis fravær uden detaljer** viser detaljer om anmodning om fritid i teams fraværskalender. | Orlovstype, farve på orlovstype og oplysninger om dagen vises i teamets fraværskalender, når **Vis fravær uden detaljer** er indstillet til **Ja** i **Parametre for orlov og fravær**. Dette er blevet løst, og nu vises orlovstypen ikke, og standardfarven på orlovstypen (mørkeblå) bruges til alle orlovstyper i teams fraværskalender. |
| 527316 | Ændringer i titlen for beskeder om job, stilling og arbejder synkroniseres ikke. | En titelrelation blev tidligere føjet til enhederne job, stilling og arbejder. Synkroniseringen for denne relation fungerer som synkronisering fra Human Resources til Dataverse, men har ikke virket for beskeder fra Dataverse. Dette er blevet løst. |
| 512275 | Fjern farveindstillingerne fra **Parametre for orlov og fravær**. | Nu, hvor der er defineret farver for orlovstypen, er farveindstillingerne ikke længere nødvendige i **Parametre for orlov og fravær**, så de er blevet fjernet. |
| 437112 | Misvisende fejlmeddelelsestekst under tildeling af medarbejderstilling. | Fejlmeddelelsen om ansættelse af en arbejder og forsøg på at tildele arbejderen til en stilling, der ikke er aktiv, er blevet opdateret. Opdateret meddelelse: **Den angivne stilling er ikke aktiv pr. ansættelsens startdato. Kontroller varigheden af denne stilling.** |
| 527816 | Problemer med ydeevnen med siden sluttid **Fridage**. | Ydeevnen er blevet forbedret på siden **Fridage**. |
| 523158 | BenefitPeriodMigrationUpgrade og BenefitPlanMigrationUpgrade udføres ikke. | Problemer med frynsegodeoverførselsjob relateret til **Periode** og **Plan**, der ikke kører korrekt, er løst. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Medarbejderorlovs- og -fraværsoplevelse i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Administrere fraværsanmodninger i Teams](hr-teams-leave-app.md) |
| Udvidede anmodninger om og godkendelser af arbejdsprocesser | [Forbedringer af arbejdsprocesser for organisations- og personalestyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsindstilling til placering af listen Workflowopgaver, der er tildelt til mig](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Integration med LinkedIn Talent Hub | [Integration med LinkedIn Talent Hub](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/integration-linkedin-talent-hub) | [Integrere med LinkedIn talent-hub](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-integration-linkedin) |
|Visning af orlov for ledere på tværs af firmaet | [Visning af orlov for medarbejdere på tværs af firmaet](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/cross-company-view-employee-leave-managers) | [Konfigurere parametre for orlov og fravær](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-parameters) |
|Give yderligere indsigt i orlovssaldi| [Give yderligere indsigt i orlovssaldi](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-into-leave-balances) | [Administrere medarbejderorlov](https://docs.microsoft.com/dynamics365/human-resources/hr-leave-and-absence-manage-employee-leave) |
| Ledere, der kan sende rekrutteringsanmodninger om stillinger | [Ledere, der kan sende en rekrutteringsanmodning om åbne stillinger](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/manager-submit-request-recruit-open-positions) | [Tilføje en rekrutteringsanmodning](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-a-recruiting-request) |
| Udvidet kandidatprofil i Personalestyring | [Udvidet kandidatprofil i Personalestyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enhanced-candidate-profile-personnel-management) | [Tilføje eller redigere en kandidatprofil](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit#add-or-edit-a-candidate-profile) |
| Muliggøre forenklet integration med rekrutteringsudbydere | [Muliggøre forenklet integration med rekrutteringsudbydere](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/enable-simplified-integration-recruiting-providers) | [Rekruttere jobkandidater](https://docs.microsoft.com/dynamics365/human-resources/hr-personnel-recruit) |

## <a name="coming-soon"></a>Kommer snart

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2020 udgivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/).

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2020 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]