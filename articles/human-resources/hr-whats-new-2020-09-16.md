---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (16. september 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 16. september 2020.
author: jcart1106
ms.date: 09/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2020-09-16
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b1386cca9fd39c2cf021e87fcc33da2bbda89630
ms.sourcegitcommit: c08a9d19eed1df03f32442ddb65a2adf1473d3b6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/06/2021
ms.locfileid: "6353584"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-september-16-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (16. september 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3557. Tallene i parenteser ved siden af visse funktioner henviser til Lifecycle Services (LCS)-supportnumre til reference.

## <a name="included-in-this-release"></a>Inkluderet i denne version

-  [Gemte visninger – generel tilgængelighed](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability)<br>- Du kan finde flere oplysninger i [Gemte visninger](../fin-ops-core/fin-ops/get-started/saved-views.md). 

- I formularen **Stillingshandlinger** findes et opdateret dimensionsgitter og en ny dialog (469495).

- Hvis du angiver **Begrænset adgang til arbejderoplysninger** til Ja i **Avanceret adgang** i **Delte Human Resources-parametre**, viser formen Frynsegoder nu kun de relevante arbejdere (393384).

- Indstillinger for ny kalenderoprettelse i **WorkCalendar**-enheden (477055):<br>- Standardsluttidspunkt<br>- Standardstarttidspunkt<br>- Fredag er arbejdsdag<br>- Mandag er arbejdsdag<br>- Lørdag er arbejdsdag<br>- Søndag er arbejdsdag<br>- Torsdag er arbejdsdag<br>- Tirsdag er arbejdsdag<br>- Onsdag er arbejdsdag<br>- Arbejdskalenderfridags-id

- **LeaveBankTransactionV1**-enheden indeholder nu årsagskoden (477823).

- Du kan nu gemme opgaveregistreringer (492923).

- Data publiceres nu korrekt fra **HCMWorkerContactEntity** (427620).

- Oversigtsfanen **Kompensation** vises nu for arbejdertypen kontrahent i formularen **Arbejderhandlinger** (482494).

- Felterne **Niveau** og **Plan** er nu obligatoriske, hvis der angives **Fast kompensation**. Der vises en fejlmeddelelse, hvis du ikke udfylder disse felter (482497).

- Feltet **Plantype** i **Frynsegoder** er nu en rulleliste (488768).

- Systemadministratorer modtager nu en besked, hvis et brugerdefineret felt slettes fra Human Resources (481408).

- Under processen til opsigelse af medarbejder fungerer Human Resources som forventet og ændrer ikke den valgte virksomhed efter at være blevet låst (479877). 

- Ledere kan ikke længere tilføje en talkolonne ved hjælp af brugertilpasning (485317).

- Ledere kan ikke længere fjerne dataområdefilteret fra de identifikationsnumre, der udløber (485321).

- Når feltet **Rapporterer til** er tomt, vises der stadig stillingsdetaljer, når markøren hviler på stillingen (433328).

- Medarbejdere kan nu se oplysninger om frynsegodeplanen i Medarbejderselvbetjening (481676).

- Medarbejdere kan nu se alle tilmeldte kurser (429048).

- Du kan nu begrænse visningsindstillingerne for siden **Professionelle certifikater**. Du kan begrænse visningsindstillinger til den aktuelle juridiske enhed efter arbejderstatus og arbejdertype (451501). 


## <a name="in-preview"></a>Som prøveversion

### <a name="human-resources-app-in-teams"></a>Human Resources-app i Teams

Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams. De kan interagere med en bot for at oprette orlovsanmodninger. Du kan finde flere oplysninger i:

- [Løsning til medarbejderes orlov og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 1
- [Appen Human Resources i Teams](./hr-admin-teams-leave-app.md) i dokumentation til Human Resources

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources-app i Teams-prøveversionsfunktioner
 
-  **Beskeder**: Afsendere og godkendere af anmodninger om fritid får besked i appen Human Resources i Teams. Godkendere kan godkende eller afvise anmodninger om fravær. Afsendere får besked, hvis anmodningen godkendes eller afvises. Du kan finde flere oplysninger i:
   - [Løsning til medarbejderes orlov og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 2
   - [Aktivere beskeder for appen Human Resources i Teams](./hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) i dokumentation til Human Resources
   - [Slå Teams-beskeder til eller fra for de enkelte brugere](./hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users) i dokumentationen til Human Resources
   - [Teams-beskeder](./hr-teams-leave-app.md#respond-to-teams-notifications) i dokumentationen til Human Resources
   - [Se dit teams orlovskalender](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i dokumentationen til Human Resources
 
- **Fraværskalender for leder**: Ledere kan se godkendte og afventende fravær for deres direkte underordnede i en kalendervisning. Denne visning giver en nem forståelse af, hvornår teammedlemmer ikke er på arbejde. Du kan finde flere oplysninger i:
   - [Løsning til medarbejderes orlov og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 2
   - [Se dit teams orlovskalender](./hr-teams-leave-app.md#view-your-teams-leave-calendar) i dokumentationen til Human Resources

### <a name="configuration-option-to-position-work-items-assigned-to-me-list-477004"></a>Konfigurationsindstilling til placering af listen Workflowopgaver, der er tildelt til mig (477004)

En ny indstilling er nu tilgængelig til at placere listen **Workflowopgaver, der er tildelt til mig**, i kolonnen til højre på dashboardet. Med denne ændring vises alle arbejdsopgaver og opgavelister i samme område. Aktivér denne funktion ved at aktivere **Prøveversion – forbedringer af arbejdsgangsoplevelsen** i Funktionsstyring. Du kan få flere oplysninger om aktivering af prøveversionsfunktioner under [Administrere funktioner](hr-admin-manage-features.md).

Denne funktion fremhæver også de arbejdsprocesindstillinger, der vises i formularen til personalehandlinger. Der vises også indstillinger for arbejdsgangen over fanen til hurtig handling med nem adgang til. Du kan finde flere oplysninger i: 

- [Forbedringer af arbejdsprocesser for organisation og personalestyring](/dynamics365-release-plan/2020wave2/human-resources/dynamics365-human-resources/organization-personnel-management-workflow-experience-enhancements) i Dynamics 365: 2020-frigivelsesplan bølge 2

![Workflowopgaver, der er tildelt til mig.](./media/hr-workflow-work-items-assigned-to-me.png)

![Hurtig adgang til arbejdsgangselementer.](./media/hr-workflow-quick-access.png)

### <a name="leave-and-absence-calendar"></a>Kalender for orlov og fravær

Denne frigivelse indeholder yderligere kalenderindstillinger for orlovs- og fraværskalendere. Du kan finde flere oplysninger i [Vise team- og firmakalendere](./hr-employee-self-service-calendar.md).

## <a name="coming-soon"></a>Kommer snart

### <a name="checklist-entities-included-in-dataverse"></a>Kontrollisteenheder inkluderet i Dataverse

Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.

### <a name="benefits-management-reason-codes"></a>Årsagskoder for administration af frynsegoder

Årsagskoder for administration af frynsegoder vil snart blive kombineret med eksisterende årsagskoder i Human Resources. Hvis du har oprettet årsagskoder i Frynsegodeadministration på mere end 15 tegn, skal du ændre navnet på årsagskoden i formen **Årsagskoder** for Frynsegodeadministration til højst 15 tegn. Når du har opdateret navnet, vises årsagskoden under den eksisterende formular til årsagskode i Personalestyring. Denne ændring vil være tilgængelig i fremtiden og vil ikke påvirke den eksisterende funktion.

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
