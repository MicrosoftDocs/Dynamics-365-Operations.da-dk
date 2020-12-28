---
title: Nyheder eller ændringer i Dynamics 365 for Talent (10. september 2019)
description: I dette emne beskrives funktioner, der enten er nye eller ændrede i Microsoft Dynamics 365 for Talent.
author: Darinkramer
manager: AnnBe
ms.date: 9/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-09-10
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 0aadecd5b37759492f7895ccfda1a777793a08b3
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460679"
---
# <a name="whats-new-or-changed-in-dynamics-365-for-talent-september-10-2019"></a>Nyheder eller ændringer i Dynamics 365 for Talent (10. september 2019)

I dette emne beskrives funktioner, der enten er nye eller ændrede i Dynamics 365 for Talent.

## <a name="changes-in-attract"></a>Ændringer i Attract

### <a name="candidate-e-mail-login"></a>Kandidatmail-logon

Kandidater kan nu bruge enhver mailadresse til at oprette en konto og logge på et Talent-karrierewebsted for at ansøge om job og slå ansøgningsstatus op. Dette er en tilføjelse til allerede at kunne logge på Talent-karrierestedet ved hjælp af sociale konti eller organisationens legitimationsoplysninger.

### <a name="job-activation-and-posting"></a>Jobaktivering og jobopslag

Vi har foretaget nogle få ændringer af jobaktivering og jobopslag. Du skal aktivere job, før du sender dem til Talent-karrierewebstedet eller til andre eksterne jobportaler, herunder LinkedIn og Broadbean.

## <a name="changes-in-onboard"></a>Ændringer i Onboard

Denne version indeholder rettelser af mindre fejl i Dynamics 365 Talent: Onboard.

## <a name="changes-in-core-hr"></a>Ændringer i Core HR

Ændringer, der er beskrevet i dette afsnit, gælder for build-nummer 8.1.2482. Tallene i parenteser i nogle overskrifter henviser til supportnumre i Microsoft Dynamics Lifecycle Services (LCS).

### <a name="you-can-enable-preview-features-in-sandbox-and-trial-environments"></a>Du kan aktivere funktioner i prøveversioner i sandkasse- og testmiljøer

Når du klargør en ny forekomst af Talent, kan du angive, om forekomsttypen er Produktion eller Sandkasse. Forekomster af typen Sandkasse giver mulighed for tidlig test af nye funktioner. Hvis en af de eksisterende forekomster skal opdateres til Sandkasse-forekomsttypen, skal du kontakte Support for at starte ændringsanmodningen.

Du kan finde flere oplysninger om, hvordan ændringer udgives, ved at se [Klargøre Talent](./provisioning-talent.md).

### <a name="platform-update-29"></a>Platform update 29

Du kan finde yderligere oplysninger om Platform update 29 under [Funktioner i prøveversionen af Dynamics 365 for Finance and Operations platform update 29 (oktober 2019)](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/get-started/whats-new-platform-update-29).

### <a name="new-job-base-entity-available-in-data-management-framework-347202"></a>Ny jobbasisenhed er tilgængelig i Data Management Framework (347202)

I denne version er der en ny tilgængelig jobbasisenhed for import/eksport af data. 

### <a name="worker-advanced-security-policy-incorrectly-displays-positions-in-position-hierarchy-354868"></a>Avanceret sikkerhedspolitik for arbejder viser ukorrekte stillinger i stillingshierarki (354868)

Med denne udgivelse vises stillinger ikke længere som åbne med en "tom" arbejder, når brugere har begrænset adgang.

### <a name="job-form-close-box-wont-close-form-in-certain-situations-342467"></a>Lukkefelt til jobform kan ikke lukke i visse situationer (342467)

Denne version indeholder en ændring, der giver mulighed for at lukke formen i alle scenarier.

### <a name="new-case-on-employee-record-is-locked-for-human-resources-manager-role-337111"></a>Ny sag på medarbejderpost er låst for rollen Personalechef (337111)

Når denne ændring er formen til sagsstyring ikke længere låst, når du åbner den fra formen Medarbejder.

### <a name="employment-end-date-always-defaults-to-235959-351492"></a>Slutdato for ansættelse er som standard altid 23:59:59 (351492)

Med denne ændring kan du ændre ansættelsesdatoen til en anden tid end 23:59:59, når en ansættelse afsluttes manuelt.

### <a name="unable-to-set-up-expiration-date-on-an-earning-code-through-data-management-336604"></a>Der kan ikke defineres udløbsdato for en lønkode via datastyring (336604)

I denne version kan du oprette lønkoder, der udløber via **PayrollWorkerPositionEarningCodeEntity**-enheden.

### <a name="employee-development-analytic-report-doesnt-display-data-348737"></a>Den analytiske rapport for medarbejderudvikling viser ikke data (348737)

I denne uges udgivelse er analysen af medarbejderfærdigheder blevet opdateret, så den giver en nøjagtig rapportering.

### <a name="terms-of-employment-datetime-dont-default-to-beginning-of-day-349101"></a>Ansættelsesdato/-tidspunkt er ikke som standard starten af dagen (349101)

Med denne ændring er startdatoen og -klokkeslættet nu som standard starten af dagen, og slutdatoen/-tidspunktet er som standard slutning på dagen.

### <a name="changing-the-employment-end-date-on-worker-action-form-displays-an-error-354092"></a>Hvis du ændrer ansættelsens slutdato på formen Arbejderhandling, vises en fejl (354092) 

Denne ændring retter et problem, når slutdatoen for ansættelsen ændres som en del af arbejderhandlingen.

### <a name="applying-onboarding-checklists-across-companies-338433"></a>Anvende onboarding-checklister på tværs af firmaer (338433)

Denne version giver nu mulighed for at anvende kontrollister for medarbejdere, der er ansat i andre juridiske enheder end den juridiske enhed, der er logget på.

## <a name="in-preview"></a>Som eksempel

### <a name="streamlined-employee-entry-and-navigation"></a>Strømlinet medarbejderangivelse og navigation

Denne funktionalitet er nu tilgængelig i sandkassemiljøer. Hvis du vil aktivere funktionen, skal du gå til **Systemadministration > Links > Opsætning > Systemparametre > Funktioner i prøveversion**. Vælg **Udvidet arbejderform og navigation**. Dette aktiverer disse ændringer for alle brugere. Du kan deaktivere denne indstilling på et hvilket som helst tidspunkt.

Du kan finde oplysninger under [Strømlinet medarbejderangivelse og navigation](./streamlined-employee-entry.md).
