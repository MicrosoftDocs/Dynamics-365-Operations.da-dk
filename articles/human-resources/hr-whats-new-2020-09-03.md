---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (03. september 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 3. september 2020.
author: andreabichsel
ms.date: 09/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-09-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 965f3ca859c601d26470038a889b0f21d2bdff5f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800111"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-3-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (3. september 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3504. Tallene i parenteser i nogle overskrifter henviser til Lifecycle Services (LCS)-supportnumre til reference.

Yderligere oplysninger om kommende funktioner i Human Resources finder du i [Oversigt over Dynamics 365 Human Resources-frigivelsesbølge 2 i 2019](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/). Du kan finde flere oplysninger om opdateringsprocessen for Human Resources i [opdateringsprocessen](hr-admin-setup-update-process.md).

## <a name="in-this-release"></a>I denne frigivelse

### <a name="new-default-financial-dimensions-grid-and-dialog-pattern-throughout-human-resources-469495"></a>Nyt standardmønster for økonomiske dimensioners gitter og dialogboks i hele Human Resources (469495)

Det nye mønster for økonomiske dimensioner er nu tilgængeligt i følgende områder:

- Stillingshandlinger (formular: **HcmPositionActionDetail**)
- Lønkoder (formular: **PayrollEarningCode**)

### <a name="entries-dont-appear-in-company-leave-calendar-if-leave-and-absence-calendar-enhancements-arent-enabled-484406"></a>Poster vises ikke i firmaets orlovskalender, hvis forbedringerne for orlov og fravær ikke er aktiveret (484406)

Denne frigivelse løser et problem, hvor orlovsposter ikke vises i firmaets orlovskalender. Dette problem opstår kun, når indstillingen **Forbedringer af orlovs- og fraværskalender** ikke er aktiveret i funktionsstyring.

### <a name="benefitplanemployeeentity-issue-467597"></a>BenefitPlanEmployeeEntity-fejl (467597)

Denne version retter et problem med **BenefitsPlanEmployee**-enheden. Når du importerer arbejdertilmeldinger, angives **Disponeringskode** og **Plantypekode** nu korrekt. Dette problem får medarbejderes frynsegodeplaner til at blive vist forkert i formularen **Frynsegodeplan for arbejder** og **Åbn tilmelding** i Medarbejderselvbetjening.

### <a name="electronic-file-1094-c-output-missing-letter-in-xml-435190"></a>Elektronisk filoutput 1094-C mangler bogstav i XML (435190)

Denne ændring retter et problem med 1094-C-outputfilen, der mangler et tegn, der skal bruges, når der sendes til det amerikanske skattevæsen (IRS).

### <a name="employee-variable-compensation-table-mapped-to-fixed-compensation-form-476117"></a>Tabellen Medarbejdervariabelkompensation er tilknyttet formularen for fast løn (476117)

Denne ændring justerer de faste lønfelter med formularen ti fast løn. Felter til variabel kompensation er nu kun tilgængelige i formularen til variabel kompensation.

### <a name="leave-requests-allowed-before-enrollment-if-that-leave-type-has-a-negative-minimum-balance-469917"></a>Orlovsanmodninger er tilladt før tilmelding, hvis den pågældende orlovstype har en negativ minimumsaldo (469917)

Denne ændring forhindrer, at der indtastes orlovsanmodninger, før de tilmeldes i planen, også selvom tilmeldingen har en negativ minimumsaldo. Du kan kun angive eller sende anmodninger, når planen er aktiv.

### <a name="document-templates-dont-download-457279"></a>Dokumentskabeloner downloades ikke (457279)

Med denne ændring kan du nu downloade alle dokumentskabeloner. 

### <a name="data-displays-as-column-headers-instead-of-rows-for-the-pay-rate-field-in-the-compensation-plan-report-476077"></a>Data vises som kolonneoverskrifter i stedet for rækker til feltet Lønsats i rapporten over kompensationsplan (476077)

I analyserapporten vises nu de korrekte oplysninger om **Lønsats**.

## <a name="in-preview"></a>Som eksempel

### <a name="human-resources-application-in-teams"></a>Human Resources-app i Teams

Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams. De kan interagere med en bot for at oprette orlovsanmodninger. Du kan finde flere oplysninger i:

- [Løsning til medarbejderes orlov og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 1
- [Appen Human Resources i Teams](https://go.microsoft.com/fwlink/?linkid=2127841) i dokumentation til Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources-app i Teams-prøveversionsfunktioner
 
-  **Beskeder**: Afsendere og godkendere af anmodninger om fritid får besked i appen Human Resources i Teams. Godkendere kan godkende eller afvise anmodninger om fritid. Afsendere får besked, hvis anmodningen godkendes eller afvises. Du kan finde flere oplysninger i:
   - [Løsning til medarbejderes orlov og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 2
   - [Aktivere beskeder for appen Human Resources i Teams](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#enable-notifications-for-the-human-resources-app-in-teams) i dokumentation til Human Resources
   - [Slå Teams-beskeder til eller fra for de enkelte brugere](https://docs.microsoft.com/dynamics365/human-resources/hr-admin-teams-leave-app#turn-teams-notifications-on-or-off-for-individual-users) i dokumentationen til Human Resources
   - [Teams-beskeder](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#teams-notifications) i dokumentationen til Human Resources
   - [Se dit teams orlovskalender](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) i dokumentationen til Human Resources
 
- **Fraværskalender for leder**: Ledere kan se godkendte og afventende fravær for deres direkte underordnede i en kalendervisning. Denne visning giver en nem forståelse af, hvornår teammedlemmer ikke er på arbejde. Du kan finde flere oplysninger i:
   - [Løsning til medarbejderes orlov og fravær i Microsoft Teams](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 2
   - [Se dit teams orlovskalender](https://docs.microsoft.com/dynamics365/human-resources/hr-teams-leave-app#view-your-teams-leave-calendar) i dokumentationen til Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigurationsindstilling til placering af listen Workflowopgaver, der er tildelt til mig (477004)

En ny indstilling er nu tilgængelig til at placere listen **Workflowopgaver, der er tildelt til mig**, i kolonnen til højre på dashboardet. Med denne ændring vises alle arbejdsopgaver og opgavelister i samme område. Aktivér denne funktion ved at aktivere **Prøveversion – forbedringer af arbejdsgangsoplevelsen** i Funktionsstyring. Du kan få flere oplysninger om aktivering af prøveversionsfunktioner under [Administrere funktioner](hr-admin-manage-features.md).

Denne funktion fremhæver også de arbejdsprocesindstillinger, der vises i formularen til personalehandlinger. Der vises også indstillinger for arbejdsgangen over fanen til hurtig handling med nem adgang til. Du kan finde flere oplysninger i: 

- [Forbedringer af arbejdsprocesser for organisation og personalestyring](https://docs.microsoft.com/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) i Dynamics 365: 2020-frigivelsesplan bølge 2

![Workflowopgaver, der er tildelt til mig](./media/hr-workflow-work-items-assigned-to-me.png)

![Hurtig adgang til arbejdsgangselementer](./media/hr-workflow-quick-access.png)

## <a name="coming-soon"></a>Kommer snart

### <a name="checklist-entities-included-in-dataverse"></a>Kontrollisteenheder inkluderet i Dataverse

Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.

### <a name="benefits-management-reason-codes"></a>Årsagskoder for administration af frynsegoder

Årsagskoder for administration af frynsegoder vil snart blive kombineret med eksisterende årsagskoder i Human Resources. Hvis du har oprettet årsagskoder i Frynsegodeadministration på mere end 15 tegn, skal du ændre navnet på årsagskoden i formen **Årsagskoder** for Frynsegodeadministration til højst 15 tegn. Når du har opdateret navnet, vises årsagskoden under den eksisterende formular til årsagskode i Personalestyring. Denne ændring vil være tilgængelig i fremtiden og vil ikke påvirke den eksisterende funktion.

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]