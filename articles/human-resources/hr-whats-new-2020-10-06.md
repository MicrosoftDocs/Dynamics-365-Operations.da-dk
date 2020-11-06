---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (6. oktober 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 6. oktober 2020.
author: jcart1106
manager: tfehr
ms.date: 10/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-10-06
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 5ca2fbbf3ffbcc7c9c32490f3733b8a94731170e
ms.sourcegitcommit: 69075e001d1fb4ef69282667052cd8d082273094
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4022209"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-october-6-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (6. oktober 2020)

Dette emne indeholder beskrivelser af nye, ændrede eller kommende funktioner i Dynamics 365 Human Resources. Du kan finde flere oplysninger om vores opdateringsproces og tidsplan i [opdateringsprocessen](hr-admin-setup-update-process.md).

Yderligere oplysninger om nye funktioner og de forventede generelle tilgængelighedsdatoer finder du i [Oversigten over Dynamics 365 Human Resources 2020-udgivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/dynamics365-human-resources/).

## <a name="in-this-release"></a>I denne frigivelse

Denne udgivelse indeholder følgende nye funktioner og fejlrettelser. Ændringerne gælder for build nummer 8.1.3636.

### <a name="new-features"></a>Nye funktioner

Følgende funktion er generelt tilgængelig med denne udgivelse.

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Yderligere indsigt i orlovskalendere | [Give yderligere indsigt i orlovskalendervisninger](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/provide-additional-insight-leave-calendar-views) | [Vise team- og firmakalender](hr-employee-self-service-calendar.md) |

### <a name="bug-fixes"></a>Fejlrettelser

Følgende fejlrettelser er inkluderet i denne version.

>[!NOTE]
> Vores målsætning er at få disse oplysninger ud til brugerne så hurtigt som muligt. Der kan være opdateringer til dette emne, der omfatter fejlrettelser, som blev udført i buildet, efter at dette emne blev udgivet.

| Fejlnummer | Fejl | Beskrivelse |
| --- | --- | --- |
| 448806 | **Standardidentifikationstype** eksporteres som **RecID** i HCM-parametre | Denne ændring af enheden Human Resources-parametre tilføjer en ekstra kolonne, der viser **Standardidentifikationstype**. |
| 492923 | Opgaveregistreringer gemmes ikke i Lifecycle Services (LCS) | Opgaveregistreringer kan nu gemmes i LCS. |
| 429950 | Fast løn udløber ikke korrekt under ændring af stillingen | Når du ændrer en arbejders stilling på siden **Overfør arbejder** , er lønslutdatoen indstillet til én dag før afslutning af stillingen. Lønslutdatoen er nu den samme som slutdatoen for stillingen. |
| 467214 | **Analyse af funktionærløn** vises kun, hvis **Navn på lønsatskonverteringen** er angivet til **Årlig** | Lønsatser for funktionærløn med et andet navn end **Årlig** , blev ikke vist i kompensationsanalysen. Med denne opdatering bruger kompensationsanalysen nu alle lønsatskonverteringer. Når du kører rapporterne **Pr. time** eller **Løn** , medtages enhver lønsatskonvertering, der bruger en anden periode end Pr. time, i filteret **Løn**. Det er kun lønsatser med en periode **Pr. time** , der medtages i **Pr. time** -filteret. |
| 482464 | Når du får vist **Evalueringer** , ændres visningen **Detaljer** ikke til gittervisning, når du har anvendt et filter | Når du har anvendt et filter, vises evalueringsgitteret som forventet. |
| 483184 | Human Resources opretter ikke orlovsperiodiseringer, når du vælger **Niveaubasis** som den **Justerede startdato** i posten **Orlovstilmelding** |Den **justerede startdato** udfyldes og bruges ved generering af orlovsperiodiseringer.  |
| 509731 | Anmodning om fridage for fremtidigt fratrådt arbejder er årsag til fejl, hvis arbejderen anmoder om fridage efter fratrædelsesdatoen | Anmodninger om fridage kan nu sendes til medarbejdere med en fremtidig fratrædelsesdato, hvis anmodningen foreligger før fratrædelsesdatoen. |
| 510716 | Kompensationsanalysen omfatter medarbejdere af begge køn i **Gennemsnitlig timeløn for mænd** | I kompensationsanalysen indeholdt **Gennemsnitlig timeløn for mænd** i den **demografiske kompensationsanalyse** den gennemsnitlige løn for kvinder. Nu omfatter den kun mænd. |
| 511348 | Selvbetjening for frynsegoder skal kun vise frynsegodeplaner, der er gældende fra dags dato til slutningen af frynsegodeperioden | Der blev vist udløbne frynsegodeplaner for medarbejdere på siden for **tilmelding til frynsegoder**. Denne rettelse fjerner disse planer. |
| 512706 | Angiv følgende felter som skrivebeskyttede:<ul><li>BenefitPlanEmployeeEntity</li><li>EnrollmentConfirmed</li><li>EnrollmentConfirmedBy</li><li>EnrollmentConfirmedDateTime | Knapperne **Tilføj** og **Fjern** for dimensionsdetaljer blev aktiveret forkert, når handlingen var fuldført. Denne opdatering af siden med **oplysninger om stillingshandlinger** bevirker, at felterne ikke kan redigeres, når handlingen er fuldført. |

## <a name="in-preview"></a>Som eksempel

Følgende nye funktioner findes som prøveversion. Du kan få flere oplysninger om aktivering og deaktivering af funktioner under [Administrere funktioner](hr-admin-manage-features.md).

| Funktion | Frigivelsesplan | Dokument |
| --- | --- | --- |
| Human Resources-app i Microsoft Teams | [Medarbejderorlovs- og -fraværsoplevelse i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) | [Human Resources-app i Teams](https://go.microsoft.com/fwlink/?linkid=2127841)<br>[Administrere fraværsanmodninger i Teams](hr-teams-leave-app.md) |
| Udvidede anmodninger om og godkendelser af arbejdsprocesser | [Forbedringer af arbejdsprocesser for organisations- og personalestyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) | [Konfigurationsindstilling til placering af listen Workflowopgaver, der er tildelt til mig](https://docs.microsoft.com/dynamics365/human-resources/hr-whats-new-2020-09-03#configuration-option-to-position-work-items-assigned-to-me-list-477004) |
| Virtuelle enheder i Common Data Service for Human Resources | [Udvide Dynamics 365 Human Resources-kernedata i Common Data Service](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/expand-dynamics-365-human-resources-core-data-common-data-service) | [Konfigurere Common Data Service virtuelle enheder](hr-admin-integration-common-data-service-virtual-entities.md) |

## <a name="coming-soon"></a>Kommer snart

Følgende nye funktioner er planlagt til fremtidige udgivelser:

- **Kontrollisteenheder inkluderet i Common Data Service** : Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Common Data Service.

- **Årsagskoder for administration af frynsegoder** : Årsagskoder for administration af frynsegoder vil snart blive kombineret med eksisterende årsagskoder i Personale. Hvis du har oprettet årsagskoder i Frynsegodeadministration på mere end 15 tegn, skal du ændre navnet på årsagskoden i formen **Årsagskoder** for Frynsegodeadministration til højst 15 tegn. Når du har opdateret navnet, vises årsagskoden under den eksisterende formular til årsagskode i Personalestyring. Denne ændring vil være tilgængelig i fremtiden og vil ikke påvirke den eksisterende funktion.

- **Brugerdefinerede links i selvbetjeningstjenesten for ledere** : vi udvider mulighederne i selvbetjeningstjenesten for at understøtte ledere. Vi tilføjer muligheden for at tilføje brugerdefinerede links under fanen **Mit team**. Denne funktion svarer til funktionen med brugerdefinerede links under fanen **Mine oplysninger** i medarbejderselvbetjening. Yderligere oplysninger finder du i [Brugerdefinerede links i selvbetjening for ledere](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/custom-links-manager-self-service).

Du kan se en komplet liste over planlagte funktioner og deres planlagte udgivelser under [Oversigt over Dynamics 365 Human Resources 2019 udgivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/).

## <a name="additional-resources"></a>Yderligere ressourcer

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2020 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)
