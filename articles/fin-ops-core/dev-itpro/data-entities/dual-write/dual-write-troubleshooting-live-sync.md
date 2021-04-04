---
title: Fejlfinding i forbindelse med problemer med direkte synkronisering
description: Dette emne indeholder fejlfindingsoplysninger, der kan hjælpe dig med at løse problemer med direkte synkronisering.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 03/16/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: b40b71eb45ae5a95a732c9554356afcddecb750e
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5566807"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="80b36-103">Fejlfinding i forbindelse med problemer med direkte synkronisering</span><span class="sxs-lookup"><span data-stu-id="80b36-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]



<span data-ttu-id="80b36-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="80b36-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Dataverse.</span></span> <span data-ttu-id="80b36-105">Specifikt indeholder emnet oplysninger, der kan hjælpe dig med at løse problemer med direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="80b36-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="80b36-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="80b36-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="80b36-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="80b36-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="80b36-108">Direkte synkronisering medfører en fejl af typen 403 Forbudt, når du opretter en række i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="80b36-108">Live synchronization throws a 403 Forbidden error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="80b36-109">Du kan få vist følgende fejlmeddelelse, når du opretter en række i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="80b36-109">You might receive the following error message when you create a row in a Finance and Operations app:</span></span>

<span data-ttu-id="80b36-110">*\[{\\"fejl\\":{\\"kode\\":\\"0x 80072560\\",\\"meddelelse\\":\\"Brugeren er ikke medlem af organisationen.\\"}}\], Fjernserveren returnerede en fejl: (403) forbudt."}}".*</span><span class="sxs-lookup"><span data-stu-id="80b36-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="80b36-111">Du kan løse problemet ved at følge trinnene i [Systemkrav og forudsætninger](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="80b36-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="80b36-112">Hvis du vil udføre disse trin, skal de brugere af dobbeltskrivningsprogrammet, der er oprettet i Dataverse, have rollen som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="80b36-112">To complete those steps, the dual-write application users who are created in Dataverse must have the system admin role.</span></span> <span data-ttu-id="80b36-113">Standard-ejerteamet skal også have rollen som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="80b36-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-table-consistently-throws-a-similar-error-when-you-create-a-row-in-a-finance-and-operations-app"></a><span data-ttu-id="80b36-114">Direkte synkronisering for alle tabeller medfører konsekvent samme fejl, når du opretter en række i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="80b36-114">Live synchronization for any table consistently throws a similar error when you create a row in a Finance and Operations app</span></span>

<span data-ttu-id="80b36-115">**Påkrævet rolle for at rette fejlen:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="80b36-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="80b36-116">Du kan få vist en fejlmeddelelse som den følgende, hver gang du forsøger at gemme tabeldata i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="80b36-116">You might receive an error message like the following every time that you try to save table data in a Finance and Operations app:</span></span>

<span data-ttu-id="80b36-117">*Ændringerne kan ikke gemmes i databasen. Arbejdsenheden kan ikke allokere transaktionen. Der kunne ikke skrives data til enhedsmåleenheder (uoms). Skrivning til UnitOfMeasureEntity mislykkedes, og fejlmeddelelsen "Kan ikke synkronisere med enhedsmåleenheder" vises.*</span><span class="sxs-lookup"><span data-stu-id="80b36-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="80b36-118">Hvis du vil løse dette problem, skal du sørge for, at de nødvendige referencedata findes i både Finance and Operations-appen og Dataverse.</span><span class="sxs-lookup"><span data-stu-id="80b36-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Dataverse.</span></span> <span data-ttu-id="80b36-119">Hvis den kunde, som du arbejder med i Finance and Operations-appen, f.eks. tilhører en bestemt kundegruppe, skal du kontrollere, at kundegruppen findes i Dataverse.</span><span class="sxs-lookup"><span data-stu-id="80b36-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Dataverse.</span></span>

<span data-ttu-id="80b36-120">Hvis der findes data på begge sider, og du har bekræftet, at problemet ikke er datarelateret, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="80b36-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="80b36-121">Stop den relaterede tabel.</span><span class="sxs-lookup"><span data-stu-id="80b36-121">Stop the related table.</span></span>
2. <span data-ttu-id="80b36-122">Log på Finance and Operations-appen, og kontrollér, at der findes rækker for den fejlbehæftede tabel i tabellerne DualWriteProjectConfiguration og DualWriteProjectFieldConfiguration.</span><span class="sxs-lookup"><span data-stu-id="80b36-122">Sign in to the Finance and Operations app, and make sure that rows for the failing table exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="80b36-123">Forespørgslen ser sådan ud, hvis f.eks. tabellen **Kunder** er fejlbehæftet.</span><span class="sxs-lookup"><span data-stu-id="80b36-123">For example, here is what the query looks like if the **Customers** table is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="80b36-124">Hvis der findes rækker for den fejlbehæftede tabel, selv efter at du har stoppet tabeltilknytningen, skal du slette de rækker, der er relateret til tabellen med fejlen.</span><span class="sxs-lookup"><span data-stu-id="80b36-124">If there are rows for the failing table even after you stop the table mapping, delete the rows that are related to the failing table.</span></span> <span data-ttu-id="80b36-125">Notér dig kolonnen **projectname** i tabellen DualWriteProjectConfiguration, og hent rækken i tabellen DualWriteProjectFieldConfiguration ved hjælp af projektnavnet for at slette rækken.</span><span class="sxs-lookup"><span data-stu-id="80b36-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the row in the DualWriteProjectFieldConfiguration table by using the project name to delete the row.</span></span>
4. <span data-ttu-id="80b36-126">Start tabeltilknytningen.</span><span class="sxs-lookup"><span data-stu-id="80b36-126">Start the table mapping.</span></span> <span data-ttu-id="80b36-127">Valider, om dataene synkroniseres uden problemer.</span><span class="sxs-lookup"><span data-stu-id="80b36-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="80b36-128">Håndtere fejl i forbindelse med læse- eller skriverettigheder, når du opretter data i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="80b36-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="80b36-129">Du kan få vist en fejlmeddelelse om en "Ugyldig anmodning", der svarer mere eller mindre til den i følgende eksempel, når du opretter data i en Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="80b36-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Eksempel på fejlmeddelelsen Ugyldig anmodning](media/error_record_id_source.png)

<span data-ttu-id="80b36-131">For at løse problemet skal du tildele den korrekte sikkerhedsrolle til teamet for den tilknyttede Dynamics 365 Sales- eller Dynamics 365 Customer Service-virksomhedsenhed for at aktivere de manglende rettigheder.</span><span class="sxs-lookup"><span data-stu-id="80b36-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="80b36-132">Find den virksomhedsenhed i Finance and Operations-appen, der er tilknyttet i Dataintegration-forbindelsessættet.</span><span class="sxs-lookup"><span data-stu-id="80b36-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisationstilknytning](media/mapped_business_unit.png)

2. <span data-ttu-id="80b36-134">Log på miljøet i den modelbaserede app i Dynamics 365, naviger til **Indstilling \> Sikkerhed**, og find teamet for den tilknyttede virksomhedsenhed.</span><span class="sxs-lookup"><span data-stu-id="80b36-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Team for den tilknyttede virksomhedsenhed](media/setting_security_page.png)

3. <span data-ttu-id="80b36-136">Åbn siden, som teamet skal redigere, og vælg derefter **Administrer roller** for at åbne dialogboksen **Administrer teamroller**.</span><span class="sxs-lookup"><span data-stu-id="80b36-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Knappen Administrer roller](media/manage_team_roles.png)

4. <span data-ttu-id="80b36-138">Tildel den rolle, der har læse-/skriverettigheden til de relevante tabeller, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="80b36-138">Assign the role that has the read/write privilege for the relevant tables, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-dataverse-environment"></a><span data-ttu-id="80b36-139">Rette synkroniseringsproblemer i et miljø, der har et Dataverse-miljø, som er blevet ændret for nylig</span><span class="sxs-lookup"><span data-stu-id="80b36-139">Fix synchronization issues in an environment that has a recently changed Dataverse environment</span></span>

<span data-ttu-id="80b36-140">**Påkrævet rolle for at rette fejlen:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="80b36-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="80b36-141">Du kan få vist følgende fejlmeddelelse, når du opretter data i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="80b36-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="80b36-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Der kunne ikke oprettes nyttedata for enheden CustCustomerV3Entity**", "logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Der opstod en fejl under oprettelse af nyttedata med følgende fejlmeddelelse om ugyldig URI: URI'en er tom".}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="80b36-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="80b36-143">Sådan ser fejlen ud i den modelbaserede app i Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="80b36-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="80b36-144">*Der opstod en uventet fejl i ISV-koden. (ErrorType = ClientError) Uventet undtagelse fra plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: enhedskontoen kunne ikke behandles - (et forbindelsesforsøg mislykkedes, fordi den tilsluttede part ikke svarede korrekt efter en tidsperiode, eller den oprettede forbindelse mislykkedes, fordi den vært, der er oprettet forbindelse til, ikke svarede*</span><span class="sxs-lookup"><span data-stu-id="80b36-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="80b36-145">Denne fejl opstår, når Dataverse-miljøet nulstilles forkert, samtidig med at du forsøger at oprette data i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="80b36-145">This error occurs when the Dataverse environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="80b36-146">Følg disse trin for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="80b36-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="80b36-147">Log på den virtuelle Finance and Operations-maskine (VM), åbn SQL Server Management Studio (SSMS), og søg efter rækker i tabellen DUALWRITEPROJECTCONFIGURATIONENTITY, hvor **internalentityname** er lig med **Debitorer V3** og **externalentityname** er lig med **konti**.</span><span class="sxs-lookup"><span data-stu-id="80b36-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for rows in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="80b36-148">Forespørgslen ser sådan ud.</span><span class="sxs-lookup"><span data-stu-id="80b36-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="80b36-149">Brug projektnavnet fra resultaterne af den forrige forespørgsel til at køre følgende forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="80b36-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="80b36-150">Kontroller, at kolonnen **externalenvironmentURL** har den korrekte Dataverse eller URL-adresse til appen.</span><span class="sxs-lookup"><span data-stu-id="80b36-150">Make sure that the **externalenvironmentURL** column has the correct Dataverse or app URL.</span></span> <span data-ttu-id="80b36-151">Slet eventuelle identiske rækker, der peger på den forkerte Dataverse-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="80b36-151">Delete any duplicate rows that point to the wrong Dataverse URL.</span></span> <span data-ttu-id="80b36-152">Slet de tilsvarende rækker i tabellerne DUALWRITEPROJECTFIELDCONFIGURATION og DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="80b36-152">Delete the corresponding rows in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="80b36-153">Stop tabeltilknytningen, og start den derefter igen</span><span class="sxs-lookup"><span data-stu-id="80b36-153">Stop the table mapping, and then restart it</span></span>


[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]