---
title: Fejlfinding i forbindelse med problemer med direkte synkronisering
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med direkte synkronisering.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: ca12759096bd1bafda0a5eee18287a694083db69
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685557"
---
# <a name="troubleshoot-live-synchronization-issues"></a>Fejlfinding i forbindelse med problemer med direkte synkronisering

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse. Specifikt indeholder emnet oplysninger, der kan hjælpe dig med at løse problemer med direkte synkronisering.

> [!IMPORTANT]
> Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren. I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Direkte synkronisering medfører en fejl af typen 403 Forbudt, når du opretter en række i en Finance and Operations-app

Du kan få vist følgende fejlmeddelelse, når du opretter en række i en Finance and Operations-app:

*\[{\\"fejl\\":{\\"kode\\":\\"0x 80072560\\",\\"meddelelse\\":\\"Brugeren er ikke medlem af organisationen.\\"}}\], Fjernserveren returnerede en fejl: (403) forbudt."}}".*

Du kan løse problemet ved at følge trinnene i [Systemkrav og forudsætninger](requirements-and-prerequisites.md). Hvis du vil udføre disse trin, skal de brugere af dobbeltskrivningsprogrammet, der er oprettet i Dataverse, have rollen som systemadministrator. Standard-ejerteamet skal også have rollen som systemadministrator.

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a>Direkte synkronisering for alle enheder medfører konsekvent samme fejl, når du opretter en række i en Finance and Operations-app

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist en fejlmeddelelse som den følgende, hver gang du forsøger at gemme enhedsdata i en Finance and Operations-app:

*Ændringerne kan ikke gemmes i databasen. Arbejdsenheden kan ikke allokere transaktionen. Der kunne ikke skrives data til enhedsmåleenheder (uoms). Skrivning til UnitOfMeasureEntity mislykkedes, og fejlmeddelelsen "Kan ikke synkronisere med enhedsmåleenheder" vises.*

Hvis du vil løse dette problem, skal du sørge for, at de nødvendige referencedata findes i både Finance and Operations-appen og Dataverse. Hvis den kunde, som du arbejder med i Finance and Operations-appen, f.eks. tilhører en bestemt kundegruppe, skal du kontrollere, at kundegruppen findes i Dataverse.

Hvis der findes data på begge sider, og du har bekræftet, at problemet ikke er datarelateret, skal du følge disse trin.

1. Stop den relaterede enhed.
2. Log på Finance and Operations-appen, og kontrollér, at der findes rækker for den fejlbehæftede enhed i tabellerne DualWriteProjectConfiguration og DualWriteProjectFieldConfiguration. Forespørgslen ser sådan ud, hvis f.eks. enheden **Kunder** er fejlbehæftet.

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. Hvis der findes rækker for den fejlbehæftede enhed, selv efter at du har stoppet tabeltilknytningen, skal du slette de rækker, der er relateret til enheden med fejlen. Notér kolonnen **projectname** i tabellen DualWriteProjectConfiguration, og hent posten i tabellen DualWriteProjectFieldConfiguration ved hjælp af projektnavnet for at slette rækken.
4. Start tabeltilknytningen. Valider, om dataene synkroniseres uden problemer.

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a>Håndtere fejl i forbindelse med læse- eller skriverettigheder, når du opretter data i en Finance and Operations-app

Du kan få vist en fejlmeddelelse om en "Ugyldig anmodning", der svarer mere eller mindre til den i følgende eksempel, når du opretter data i en Finance and Operations-app.

![Eksempel på fejlmeddelelsen Ugyldig anmodning](media/error_record_id_source.png)

For at løse problemet skal du tildele den korrekte sikkerhedsrolle til teamet for den tilknyttede Dynamics 365 Sales- eller Dynamics 365 Customer Service-virksomhedsenhed for at aktivere de manglende rettigheder.

1. Find den virksomhedsenhed i Finance and Operations-appen, der er tilknyttet i Dataintegration-forbindelsessættet.

    ![Organisationstilknytning](media/mapped_business_unit.png)

2. Log på miljøet i den modelbaserede app i Dynamics 365, naviger til **Indstilling \> Sikkerhed**, og find teamet for den tilknyttede virksomhedsenhed.

    ![Team for den tilknyttede virksomhedsenhed](media/setting_security_page.png)

3. Åbn siden, som teamet skal redigere, og vælg derefter **Administrer roller** for at åbne dialogboksen **Administrer teamroller**.

    ![Knappen Administrer roller](media/manage_team_roles.png)

4. Tildel den rolle, der har læse-/skriverettigheden til de relevante tabeller, og vælg derefter **OK**.

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a>Rette synkroniseringsproblemer i et miljø, der har et Dataverse-miljø, som er blevet ændret for nylig

**Påkrævet rolle for at rette fejlen:** Systemadministrator

Du kan få vist følgende fejlmeddelelse, når du opretter data i en Finance and Operations-app:

*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Der kunne ikke oprettes nyttedata for enheden CustCustomerV3Entity**", "logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Der opstod en fejl under oprettelse af nyttedata med følgende fejlmeddelelse om ugyldig URI: URI'en er tom".}\],"isErrorCountUpdated":true}*

Sådan ser fejlen ud i den modelbaserede app i Dynamics 365:

*Der opstod en uventet fejl i ISV-koden. (ErrorType = ClientError) Uventet undtagelse fra plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: enhedskontoen kunne ikke behandles - (et forbindelsesforsøg mislykkedes, fordi den tilsluttede part ikke svarede korrekt efter en tidsperiode, eller den oprettede forbindelse mislykkedes, fordi den vært, der er oprettet forbindelse til, ikke svarede*

Denne fejl opstår, når Dataverse-miljøet nulstilles forkert, samtidig med at du forsøger at oprette data i Finance and Operations-appen.

Følg disse trin for at løse dette problem.

1. Log på den virtuelle Finance and Operations-maskine (VM), åbn SQL Server Management Studio (SSMS), og søg efter rækker i tabellen DUALWRITEPROJECTCONFIGURATIONENTITY, hvor **internalentityname** er lig med **Debitorer V3** og **externalentityname** er lig med **konti**. Forespørgslen ser sådan ud.

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. Brug projektnavnet fra resultaterne af den forrige forespørgsel til at køre følgende forespørgsel.

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. Kontroller, at kolonnen **externalenvironmentURL** har den korrekte Dataverse eller URL-adresse til appen. Slet eventuelle identiske rækker, der peger på den forkerte Dataverse-URL-adresse. Slet de tilsvarende rækker i tabellerne DUALWRITEPROJECTFIELDCONFIGURATION og DUALWRITEPROJECTCONFIGURATION.
4. Stop tabeltilknytningen, og start den derefter igen
