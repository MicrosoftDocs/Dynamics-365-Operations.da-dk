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
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2020-03-16
ms.openlocfilehash: d45b19c1e88e6a27bde4335d4a356f2173bdfcd3
ms.sourcegitcommit: e06da171b9cba8163893e30244c52a9ce0901146
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2020
ms.locfileid: "3275411"
---
# <a name="troubleshoot-live-synchronization-issues"></a><span data-ttu-id="dd850-103">Fejlfinding i forbindelse med problemer med direkte synkronisering</span><span class="sxs-lookup"><span data-stu-id="dd850-103">Troubleshoot live synchronization issues</span></span>

[!include [banner](../../includes/banner.md)]



<span data-ttu-id="dd850-104">Dette emne indeholder fejlfindingsoplysninger for integration med dobbeltskrivning mellem Finance and Operations-apps og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="dd850-104">This topic provides troubleshooting information for dual-write integration between Finance and Operations apps and Common Data Service.</span></span> <span data-ttu-id="dd850-105">Specifikt indeholder emnet oplysninger, der kan hjælpe dig med at løse problemer med direkte synkronisering.</span><span class="sxs-lookup"><span data-stu-id="dd850-105">Specifically, it provides information that can help you fix issues with live synchronization.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="dd850-106">Nogle af de problemer, som dette emne vedrører, kræver muligvis enten rollen systemadministrator eller legitimationsoplysninger fra Microsoft Azure Active Directory (Azure AD)-lejeradministratoren.</span><span class="sxs-lookup"><span data-stu-id="dd850-106">Some of the issues that this topic addresses might require either the system admin role or Microsoft Azure Active Directory (Azure AD) tenant admin credentials.</span></span> <span data-ttu-id="dd850-107">I afsnittet for hvert spørgsmål forklarer, om der kræves en bestemt rolle eller legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="dd850-107">The section for each issue explains whether a specific role or credentials are required.</span></span>

## <a name="live-synchronization-throws-a-403-forbidden-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="dd850-108">Direkte synkronisering medfører en fejl af typen 403 Forbudt, når du opretter en post i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="dd850-108">Live synchronization throws a 403 Forbidden error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="dd850-109">Du kan få vist følgende fejlmeddelelse, når du opretter en post i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="dd850-109">You might receive the following error message when you create a record in a Finance and Operations app:</span></span>

<span data-ttu-id="dd850-110">*\[{\\"fejl\\":{\\"kode\\":\\"0x 80072560\\",\\"meddelelse\\":\\"Brugeren er ikke medlem af organisationen.\\"}}\], Fjernserveren returnerede en fejl: (403) forbudt."}}".*</span><span class="sxs-lookup"><span data-stu-id="dd850-110">*\[{\\"error\\":{\\"code\\":\\"0x80072560\\",\\"message\\":\\"The user is not a member of the organization.\\"}}\], The remote server returned an error: (403) Forbidden."}}".*</span></span>

<span data-ttu-id="dd850-111">Du kan løse problemet ved at følge trinnene i [Systemkrav og forudsætninger](requirements-and-prerequisites.md).</span><span class="sxs-lookup"><span data-stu-id="dd850-111">To fix the issue, follow the steps in [System requirements and prerequisites](requirements-and-prerequisites.md).</span></span> <span data-ttu-id="dd850-112">Hvis du vil udføre disse trin, skal de brugere af dobbeltskrivningsprogrammet, der er oprettet i Common Data Service, have rollen som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="dd850-112">To complete those steps, the dual-write application users who are created in Common Data Service must have the system admin role.</span></span> <span data-ttu-id="dd850-113">Standard-ejerteamet skal også have rollen som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="dd850-113">The default owning team must also have the system admin role.</span></span>

## <a name="live-synchronization-for-any-entity-consistently-throws-a-similar-error-when-you-create-a-record-in-a-finance-and-operations-app"></a><span data-ttu-id="dd850-114">Direkte synkronisering for alle enheder medfører konsekvent samme fejl, når du opretter en post i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="dd850-114">Live synchronization for any entity consistently throws a similar error when you create a record in a Finance and Operations app</span></span>

<span data-ttu-id="dd850-115">**Påkrævet rolle for at rette fejlen:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="dd850-115">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="dd850-116">Du kan få vist en fejlmeddelelse som den følgende, hver gang du forsøger at gemme enhedsdata i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="dd850-116">You might receive an error message like the following every time that you try to save entity data in a Finance and Operations app:</span></span>

<span data-ttu-id="dd850-117">*Ændringerne kan ikke gemmes i databasen. Arbejdsenheden kan ikke allokere transaktionen. Der kunne ikke skrives data til enhedsmåleenheder (uoms). Skrivning til UnitOfMeasureEntity mislykkedes, og fejlmeddelelsen "Kan ikke synkronisere med enhedsmåleenheder" vises.*</span><span class="sxs-lookup"><span data-stu-id="dd850-117">*Cannot save the changes to the database. Unit of Work can not commit transaction. Unable to write data to entity uoms. Writes to UnitOfMeasureEntity failed with error message Unable to sync with entity uoms.*</span></span>

<span data-ttu-id="dd850-118">Hvis du vil løse dette problem, skal du sørge for, at de nødvendige referencedata findes i både Finance and Operations-appen og Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="dd850-118">To fix the issue, you must make sure that the prerequisite reference data exists in both the Finance and Operations app and Common Data Service.</span></span> <span data-ttu-id="dd850-119">Hvis den kunde, som du arbejder med i Finance and Operations-appen, f.eks. tilhører en bestemt kundegruppe, skal du kontrollere, at kundegruppen findes i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="dd850-119">For example, if the customer that you're in the Finance and Operations app belongs to a specific customer group, make sure that the customer group exists in Common Data Service.</span></span>

<span data-ttu-id="dd850-120">Hvis der findes data på begge sider, og du har bekræftet, at problemet ikke er datarelateret, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="dd850-120">If data exists on both sides, and you've confirmed that the issue isn't data-related, follow these steps.</span></span>

1. <span data-ttu-id="dd850-121">Stop den relaterede enhed.</span><span class="sxs-lookup"><span data-stu-id="dd850-121">Stop the related entity.</span></span>
2. <span data-ttu-id="dd850-122">Log på Finance and Operations-appen, og kontroller, at der findes poster for den fejlbehæftede enhed i tabellerne DualWriteProjectConfiguration og DualWriteProjectFieldConfiguration.</span><span class="sxs-lookup"><span data-stu-id="dd850-122">Sign in to the Finance and Operations app, and make sure that records for the failing entity exist in the DualWriteProjectConfiguration and DualWriteProjectFieldConfiguration tables.</span></span> <span data-ttu-id="dd850-123">Forespørgslen ser sådan ud, hvis f.eks. enheden **Kunder** er fejlbehæftet.</span><span class="sxs-lookup"><span data-stu-id="dd850-123">For example, here is what the query looks like if the **Customers** entity is failing.</span></span>

    ```sql
    Select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and
        EXTERNALENTITYNAME = 'accounts' 
    ```

3. <span data-ttu-id="dd850-124">Hvis der findes poster for den fejlbehæftede enhed, selv efter at du har stoppet tilknytningen af enheden, skal du slette de poster, der er relateret til enheden med fejlen.</span><span class="sxs-lookup"><span data-stu-id="dd850-124">If there are records for the failing entity even after you stop the entity mapping, delete the records that are related to the failing entity.</span></span> <span data-ttu-id="dd850-125">Noter kolonnen **projectname** i tabellen DualWriteProjectConfiguration, og hent posten i tabellen DualWriteProjectFieldConfiguration ved hjælp af projektnavnet for at slette posten.</span><span class="sxs-lookup"><span data-stu-id="dd850-125">Make a note of the **projectname** column in the DualWriteProjectConfiguration table, and fetch the record in the DualWriteProjectFieldConfiguration table by using the project name to delete the record.</span></span>
4. <span data-ttu-id="dd850-126">Start tilknytningen af enheden.</span><span class="sxs-lookup"><span data-stu-id="dd850-126">Start the entity mapping.</span></span> <span data-ttu-id="dd850-127">Valider, om dataene synkroniseres uden problemer.</span><span class="sxs-lookup"><span data-stu-id="dd850-127">Validate whether the data is synced without any issues.</span></span>

## <a name="handle-read-or-write-privilege-errors-when-you-create-data-in-a-finance-and-operations-app"></a><span data-ttu-id="dd850-128">Håndtere fejl i forbindelse med læse- eller skriverettigheder, når du opretter data i en Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="dd850-128">Handle read or write privilege errors when you create data in a Finance and Operations app</span></span>

<span data-ttu-id="dd850-129">Du kan få vist en fejlmeddelelse om en "Ugyldig anmodning", der svarer mere eller mindre til den i følgende eksempel, når du opretter data i en Finance and Operations-app.</span><span class="sxs-lookup"><span data-stu-id="dd850-129">You might receive a "Bad Request" error message that resembles the following example when you create data in a Finance and Operations app.</span></span>

![Eksempel på fejlmeddelelsen Ugyldig anmodning](media/error_record_id_source.png)

<span data-ttu-id="dd850-131">For at løse problemet skal du tildele den korrekte sikkerhedsrolle til teamet for den tilknyttede Dynamics 365 Sales- eller Dynamics 365 Customer Service-virksomhedsenhed for at aktivere de manglende rettigheder.</span><span class="sxs-lookup"><span data-stu-id="dd850-131">To fix the issue, you must assign the correct security role to the team of the mapped Dynamics 365 Sales or Dynamics 365 Customer Service business unit to enable the missing privilege.</span></span>

1. <span data-ttu-id="dd850-132">Find den virksomhedsenhed i Finance and Operations-appen, der er tilknyttet i Dataintegration-forbindelsessættet.</span><span class="sxs-lookup"><span data-stu-id="dd850-132">In the Finance and Operations app, find the business unit that is mapped in the Data Integration connection set.</span></span>

    ![Organisationstilknytning](media/mapped_business_unit.png)

2. <span data-ttu-id="dd850-134">Log på miljøet i den modelbaserede app i Dynamics 365, naviger til **Indstilling \> Sikkerhed**, og find teamet for den tilknyttede virksomhedsenhed.</span><span class="sxs-lookup"><span data-stu-id="dd850-134">Sign in to the environment in the model-driven app in Dynamics 365, navigate to **Setting \> Security**, and find the team of the mapped business unit.</span></span>

    ![Team for den tilknyttede virksomhedsenhed](media/setting_security_page.png)

3. <span data-ttu-id="dd850-136">Åbn siden, som teamet skal redigere, og vælg derefter **Administrer roller** for at åbne dialogboksen **Administrer teamroller**.</span><span class="sxs-lookup"><span data-stu-id="dd850-136">Open the page for the team for editing, and then select **Manage roles** to open the **Manage Team Roles** dialog box.</span></span>

    ![Knappen Administrer roller](media/manage_team_roles.png)

4. <span data-ttu-id="dd850-138">Tildel den rolle, der har læse-/skriverettigheden til de relevante enheder, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="dd850-138">Assign the role that has the read/write privilege for the relevant entities, and then select **OK**.</span></span>

## <a name="fix-synchronization-issues-in-an-environment-that-has-a-recently-changed-common-data-service-environment"></a><span data-ttu-id="dd850-139">Rette synkroniseringsproblemer i et miljø, der har et Common Data Service-miljø, som er blevet ændret for nylig</span><span class="sxs-lookup"><span data-stu-id="dd850-139">Fix synchronization issues in an environment that has a recently changed Common Data Service environment</span></span>

<span data-ttu-id="dd850-140">**Påkrævet rolle for at rette fejlen:** Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="dd850-140">**Required role to fix the issue:** System admin</span></span>

<span data-ttu-id="dd850-141">Du kan få vist følgende fejlmeddelelse, når du opretter data i en Finance and Operations-app:</span><span class="sxs-lookup"><span data-stu-id="dd850-141">You might receive the following error message when you create data in a Finance and Operations app:</span></span>

<span data-ttu-id="dd850-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Der kunne ikke oprettes nyttedata for enheden CustCustomerV3Entity**", "logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Der opstod en fejl under oprettelse af nyttedata med følgende fejlmeddelelse om ugyldig URI: URI'en er tom".}\],"isErrorCountUpdated":true}*</span><span class="sxs-lookup"><span data-stu-id="dd850-142">*{"entityName":"CustCustomerV3Entity","executionStatus":2,"fieldResponses":\[\],"recordResponses":\[{"errorMessage":"**Unable to generate payload for entity CustCustomerV3Entity**","logDateTime":"2019-08-27T18:51:52.5843124Z","verboseError":"Payload creation failed with error Invalid URI: The URI is empty."}\],"isErrorCountUpdated":true}*</span></span>

<span data-ttu-id="dd850-143">Sådan ser fejlen ud i den modelbaserede app i Dynamics 365:</span><span class="sxs-lookup"><span data-stu-id="dd850-143">Here is what the error looks like in the model-driven app in Dynamics 365:</span></span>

<span data-ttu-id="dd850-144">*Der opstod en uventet fejl i ISV-koden. (ErrorType = ClientError) Uventet undtagelse fra plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: enhedskontoen kunne ikke behandles - (et forbindelsesforsøg mislykkedes, fordi den tilsluttede part ikke svarede korrekt efter en tidsperiode, eller den oprettede forbindelse mislykkedes, fordi den vært, der er oprettet forbindelse til, ikke svarede*</span><span class="sxs-lookup"><span data-stu-id="dd850-144">*An unexpected error occurred from ISV code. (ErrorType = ClientError) Unexpected exception from plug-in (Execute): Microsoft.Dynamics.Integrator.DualWriteRuntime.Plugins.PostCommitPlugin: System.Exception: failed to process entity account - (A connection attempt failed because the connected party did not properly respond after a period of time, or established connection failed because connected host has failed to respond*</span></span>

<span data-ttu-id="dd850-145">Denne fejl opstår, når Common Data Service-miljøet nulstilles forkert, samtidig med at du forsøger at oprette data i Finance and Operations-appen.</span><span class="sxs-lookup"><span data-stu-id="dd850-145">This error occurs when the Common Data Service environment is incorrectly reset at the same time that you try to create data in the Finance and Operations app.</span></span>

<span data-ttu-id="dd850-146">Følg disse trin for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="dd850-146">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="dd850-147">Log på den virtuelle Finance and Operations-maskine (VM), åbn SQL Server Management Studio (SSMS), og søg efter poster i tabellen DUALWRITEPROJECTCONFIGURATIONENTITY, hvor **internalentityname** er lig med **Debitorer V3** og **externalentityname** er lig med **konti**.</span><span class="sxs-lookup"><span data-stu-id="dd850-147">Sign in to the Finance and Operations virtual machine (VM), open SQL Server Management Studio (SSMS), and look for records in the DUALWRITEPROJECTCONFIGURATIONENTITY table where **internalentityname** equals **Customers V3** and **externalentityname** equals **accounts**.</span></span> <span data-ttu-id="dd850-148">Forespørgslen ser sådan ud.</span><span class="sxs-lookup"><span data-stu-id="dd850-148">Here is what the query looks like.</span></span>

    ```sql
    select projectname, externalenvironmentURL ,\* 
    from DUALWRITEPROJECTCONFIGURATION 
    where INTERNALENTITYNAME = 'Customers V3' and EXTERNALENTITYNAME = 'accounts'
    ```

2. <span data-ttu-id="dd850-149">Brug projektnavnet fra resultaterne af den forrige forespørgsel til at køre følgende forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="dd850-149">Use the project name from the results of the previous query to run the following query.</span></span>

    ```sql
    select \* 
    from DUALWRITEPROJECTFIELDCONFIGURATION 
    where projectname = <project name from previous query>
    ```

3. <span data-ttu-id="dd850-150">Kontroller, at kolonnen **externalenvironmentURL** har den korrekte Common Data Service eller URL-adresse til appen.</span><span class="sxs-lookup"><span data-stu-id="dd850-150">Make sure that the **externalenvironmentURL** column has the correct Common Data Service or app URL.</span></span> <span data-ttu-id="dd850-151">Slet eventuelle identiske poster, der peger på den forkerte Common Data Service-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="dd850-151">Delete any duplicate records that point to the wrong Common Data Service URL.</span></span> <span data-ttu-id="dd850-152">Slet de tilsvarende poster i tabellerne DUALWRITEPROJECTFIELDCONFIGURATION og DUALWRITEPROJECTCONFIGURATION.</span><span class="sxs-lookup"><span data-stu-id="dd850-152">Delete the corresponding records in the DUALWRITEPROJECTFIELDCONFIGURATION and DUALWRITEPROJECTCONFIGURATION tables.</span></span>
4. <span data-ttu-id="dd850-153">Stop enhedstilknytningen, og start den derefter igen</span><span class="sxs-lookup"><span data-stu-id="dd850-153">Stop the entity mapping, and then restart it</span></span>
