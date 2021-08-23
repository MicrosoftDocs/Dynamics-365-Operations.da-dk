---
title: Nyheder eller ændringer i Dynamics 365 Human Resources (20. august 2020)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 Human Resources for 20. august 2020.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 32535c1f93990306ffaa0a5d97b48d3e6fdda7d014ceeeb2552960cd08b4be6c
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6775837"
---
# <a name="whats-new-or-changed-in-dynamics-365-human-resources-august-20-2020"></a>Nyheder eller ændringer i Dynamics 365 Human Resources (20. august 2020)

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 Human Resources. Ændringerne gælder for build nummer 8.1.3478. Tallene i parenteser i nogle overskrifter henviser til Lifecycle Services (LCS)-supportnumre til reference.

## <a name="show-upcoming-and-pending-leave-of-absence-information-to-cards-in-people-workspace"></a>Vise forestående og ventende orlovsoplysninger til kort i arbejdsområdet Personer

Indstillinger for ventende og kommende orlovsanmodninger er nu tilgængelige på kortene Orlov og fravær i arbejdsområdet **Personer**.

## <a name="private-field-isnt-yes-by-default-for-employee-role-in-employee-self-service-477106"></a>Feltet Privat er ikke Ja som standard for medarbejderrollen i Medarbejderselvbetjening (477106)

Feltet **Privat** er nu som standard angivet til **Ja**, når medarbejderne tilføjer nye adresseposter via siden **Personlige oplysninger** i Medarbejderselvbetjening. 

## <a name="candidates-to-hire-fasttab-in-personnel-management-shows-an-incorrect-count-of-candidates-470110"></a>Oversigtspanelet Kandidater, der skal ansættes i Personalestyring viser et forkert antal kandidater (470110)

Siden **Personalestyring** viser nu antallet af kandidater, der skal ansættes. 

## <a name="cant-enter-sickness-for-terminated-employee-when-accrual-is-set-to-zero-446195"></a>Kan ikke angive sygdom for fratrådt medarbejder, når periodisering er indstillet til nul (446195)

Orlovstransaktioner er nu tilladt for medarbejdere, der er fratrådt i fremtiden, og periodiseringen angives til nul. Orlovstransaktioner kan angives til medarbejderens fratrædelsesdato. 

## <a name="adding-custom-fields-to-the-new-worker-form-disables-the-fields-in-the-action-pane-for-manage-leave-473314"></a>Når du føjer brugerdefinerede felter til den nye arbejderformular, deaktiveres felterne i handlingsruden for Administrer orlov (473314)

Indstillingerne i handlingsruden for den nye **Arbejder**-formular i **Administrer orlov** vil ikke længere være deaktiveret, hvis der er føjet brugerdefinerede felter til den nye **Arbejder**-formular.

## <a name="making-the-leave-comment-field-mandatory-allows-a-leave-request-to-be-submitted-when-no-comment-is-entered-473543"></a>Hvis du gør feltet Efterlad kommentar obligatorisk, kan en orlovsanmodning afsendes, når der ikke er angivet en kommentar (473543)

Kommentarfelter kan nu være obligatoriske, og orlovsanmodninger accepterer denne indstilling. Obligatoriske felter er en prøveversionsfunktion.

### <a name="dmf-entity-available-for-accrual-suspensions"></a>DMF-enhed er tilgængelig for periodiseringssuspenderinger

En DMF-enhed er nu tilgængelig for periodiseringssuspenderinger.

## <a name="in-preview"></a>Som eksempel

### <a name="mandatory-fields"></a>Obligatoriske felter

Du kan nu gøre felter obligatoriske ved hjælp af tilpasningsfunktionerne for personale. Denne funktion kræver **Gemte visninger**. Du kan finde flere oplysninger om gemte visninger i:

- [Gemte visninger – generel tilgængelighed](/dynamics365-release-plan/2020wave2/finance-operations/finance-operations-crossapp-capabilities/saved-views--general-availability) i Dynamics 365 2020-frigivelsesplan bølge 2
- [Opbygge formularer, der fuldt ud anvender gemte visninger](../fin-ops-core/dev-itpro/user-interface/understanding-saved-views.md)

### <a name="human-resources-application-in-teams"></a>Human Resources-app i Teams

Medarbejderne kan få vist og anmode om fri fra arbejde i Microsoft Teams. De kan interagere med en bot for at oprette orlovsanmodninger. Du kan finde flere oplysninger i:

- [Løsning til medarbejderes orlov og fravær i Microsoft Teams](/dynamics365-release-plan/2020wave1/dynamics365-human-resources/employee-leave-absence-experience-teams) Dynamics 365 2020-frigivelsesplan bølge 1
- [Human Resources-app i Teams](./hr-admin-teams-leave-app.md)

## <a name="coming-soon"></a>Kommer snart

### <a name="human-resources-app-in-teams-preview-features"></a>Human Resources-app i Teams-prøveversionsfunktioner
 
-  **Beskeder**: Afsendere og godkendere af anmodninger om fritid får besked i appen Human Resources i Teams. Godkendere kan godkende eller afvise anmodninger om fritid, og afsendere får besked, hvis anmodningen godkendes eller afvises.
 
- **Fraværskalender for leder**: Ledere kan se godkendte og afventende fravær for deres direkte underordnede i en kalendervisning. Denne visning giver en nem forståelse af, hvornår teammedlemmer ikke er på arbejde.

### <a name="checklist-entities-included-in-dataverse"></a>Kontrollisteenheder inkluderet i Dataverse

Der vil snart være tilgængelige kontrollisteenheder til processer til onboarding, offboarding, overførsler og forretning i Dataverse.

## <a name="known-issues"></a>Kendte problemer

Arbejdsområdet **Funktionsstyring** viser muligvis funktioner, der er deaktiveret som visningsfunktioner, når de generelt er tilgængelige. Nedenfor vises en liste over de mest almindeligt tilgængelige funktioner, der viser en forkert status. 

- Frynsegodeadministration
- Sagsstyring
- Databaselogføring (overvågning)
- Orlovsperiodisering for et enkelt firma eller en enkelt plan
- Afbrydelse af periodisering af orlov og fravær
- Årsagskode og kommentar for saldoregulering
- Købe og sælge orlov
- Kalender for orlov og fravær
- Regler for orlovsoverførsel
- Revision af orlovsperiodisering
- Sletning af orlovsperiodisering
- Afrunding af orlovsperiodisering
- Konfigurer flere orlovstyper på en enkelt orlovsplan
- Forbedringer af opdatering af fravær
- Bruge en medarbejders FTE-analyse til periodiseringer
- Visning af kompensation på tværs af firmaer
- Udskiv performancegennemgange
- Korrektioner for feriedage ved orlovsperiodisering

### <a name="benefit-plan-employee-entity"></a>Frynsegodeplan for medarbejderenhed 

Vi har for nylig fundet to problemer vedrørende **BenefitsPlanEmployee**-enheden. Når du importerer arbejdertilmeldinger, angives **Disponeringskode** og **Plantypekode** forkert. Dette problem får medarbejderes frynsegodeplaner til at blive vist forkert i formularen **Frynsegodeplan for arbejder** og i formularen **Åbn tilmelding** i Medarbejderselvbetjening. Dette problem kan også påvirke medarbejderens mulighed for at vælge planer i Medarbejderselvbetjening. Der er i øjeblikket ikke en løsning på problemet. Vi behandler dette som en rettelse med høj prioritet og udruller rettelsen med vores næste frigivelse.

## <a name="see-also"></a>Se også

[Nyheder eller ændringer i Human Resources](hr-admin-whats-new.md)</br>
[Oversigt over Dynamics 365 Human Resources 2019 frigivelsesbølge 2](/dynamics365-release-plan/2019wave2/dynamics365-human-resources/)</br>
[Opdater proces](hr-admin-setup-update-process.md)</br>
[Administrere funktioner](hr-admin-manage-features.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]