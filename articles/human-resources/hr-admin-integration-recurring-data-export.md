---
title: Opret en app til tilbagevendende dataeksport
description: Denne artikel viser, hvordan du opretter en Microsoft Azure-logikapp, der eksporterer data fra Microsoft Dynamics 365 Human Resources i en tilbagevendende tidsplan.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: a4a963bcfe5932f5642b43751ccd96c472fec0d9
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054998"
---
# <a name="create-a-recurring-data-export-app"></a><span data-ttu-id="37847-103">Opret en app til tilbagevendende dataeksport</span><span class="sxs-lookup"><span data-stu-id="37847-103">Create a recurring data export app</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="37847-104">Denne artikel viser, hvordan du opretter en Microsoft Azure-logikapp, der eksporterer data fra Microsoft Dynamics 365 Human Resources i en tilbagevendende tidsplan.</span><span class="sxs-lookup"><span data-stu-id="37847-104">This article shows how to create a Microsoft Azure logic app that exports data from Microsoft Dynamics 365 Human Resources on a recurring schedule.</span></span> <span data-ttu-id="37847-105">Selvstudiet benytter REST API for DMF-pakke (programmeringsgrænseflade til program) i Human Resources til at eksportere dataene.</span><span class="sxs-lookup"><span data-stu-id="37847-105">The tutorial takes advantage of Human Resources' DMF package REST application programming interface (API) to export the data.</span></span> <span data-ttu-id="37847-106">Når dataene er eksporteret, gemmer logikappen den eksporterede datapakke i en Microsoft OneDrive for Business-mappe.</span><span class="sxs-lookup"><span data-stu-id="37847-106">After the data has been exported, the logic app saves the exported data package to a Microsoft OneDrive for Business folder.</span></span>

## <a name="business-scenario"></a><span data-ttu-id="37847-107">Forretningsscenarie</span><span class="sxs-lookup"><span data-stu-id="37847-107">Business scenario</span></span>

<span data-ttu-id="37847-108">I et typisk forretningsscenarie til Microsoft Dynamics 365-integration skal data eksporteres til et downstream-system i en tilbagevendende tidsplan.</span><span class="sxs-lookup"><span data-stu-id="37847-108">In one typical business scenario for Microsoft Dynamics 365 integrations, data must be exported to a downstream system on a recurring schedule.</span></span> <span data-ttu-id="37847-109">Dette selvstudium viser, hvordan du kan eksportere alle poster for arbejdere fra Microsoft Dynamics 365 Human Resources og gemme listen over arbejdere i en OneDrive for Business-mappe.</span><span class="sxs-lookup"><span data-stu-id="37847-109">This tutorial shows how to export all worker records from Microsoft Dynamics 365 Human Resources and save the list of workers in a OneDrive for Business folder.</span></span>

> [!TIP]
> <span data-ttu-id="37847-110">De specifikke data, der eksporteres i dette selvstudium, og destinationen for de eksporterede data, er kun eksempler.</span><span class="sxs-lookup"><span data-stu-id="37847-110">The specific data that is exported in this tutorial and the destination of the exported data are only examples.</span></span> <span data-ttu-id="37847-111">Du kan nemt ændre dem, så de opfylder dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="37847-111">You can easily change them to meet your business needs.</span></span>

## <a name="technologies-used"></a><span data-ttu-id="37847-112">Anvendte teknologier</span><span class="sxs-lookup"><span data-stu-id="37847-112">Technologies used</span></span>

<span data-ttu-id="37847-113">I dette selvstudium bruges følgende teknologier:</span><span class="sxs-lookup"><span data-stu-id="37847-113">This tutorial uses the following technologies:</span></span>

- <span data-ttu-id="37847-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – Masterdatakilden for arbejdere, der skal eksporteres.</span><span class="sxs-lookup"><span data-stu-id="37847-114">**[Dynamics 365 Human Resources](https://dynamics.microsoft.com/talent/overview/)** – The master data source for workers that will be exported.</span></span>
- <span data-ttu-id="37847-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – Den teknologi, der omfatter organisering og planlægning af den tilbagevendende eksport.</span><span class="sxs-lookup"><span data-stu-id="37847-115">**[Azure Logic Apps](https://azure.microsoft.com/services/logic-apps/)** – The technology that provides orchestration and scheduling of the recurring export.</span></span>

    - <span data-ttu-id="37847-116">**[Connectors](/azure/connectors/apis-list)** – Den teknologi, der bruges til at forbinde logikappen med de nødvendige slutpunkter.</span><span class="sxs-lookup"><span data-stu-id="37847-116">**[Connectors](/azure/connectors/apis-list)** – The technology that is used to connect the logic app to the required endpoints.</span></span>

        - <span data-ttu-id="37847-117">[HTTP med Azure AD](/connectors/webcontents/)-connector</span><span class="sxs-lookup"><span data-stu-id="37847-117">[HTTP with Azure AD](/connectors/webcontents/) connector</span></span>
        - <span data-ttu-id="37847-118">[OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness)-connector</span><span class="sxs-lookup"><span data-stu-id="37847-118">[OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector</span></span>

- <span data-ttu-id="37847-119">**[REST API for DMF-pakke](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – den teknologi, der bruges til at udløse eksporten og overvåge, hvordan den skrider frem.</span><span class="sxs-lookup"><span data-stu-id="37847-119">**[DMF package REST API](../fin-ops-core/dev-itpro/data-entities/data-management-api.md)** – The technology that is used to trigger the export and monitor its progress.</span></span>
- <span data-ttu-id="37847-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – Destinationen for de eksporterede arbejdere.</span><span class="sxs-lookup"><span data-stu-id="37847-120">**[OneDrive for Business](https://onedrive.live.com/about/business/)** – The destination for the exported workers.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="37847-121">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="37847-121">Prerequisites</span></span>

<span data-ttu-id="37847-122">Før du starter øvelsen i dette selvstudium, skal du have følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="37847-122">Before you begin the exercise in this tutorial, you must have the following items:</span></span>

- <span data-ttu-id="37847-123">Et Human Resources-miljø med administratorrettigheder i miljøet</span><span class="sxs-lookup"><span data-stu-id="37847-123">A Human Resources environment that has admin-level permissions in the environment</span></span>
- <span data-ttu-id="37847-124">Et [Azure-abonnement](https://azure.microsoft.com/free/) som vært for logikappen</span><span class="sxs-lookup"><span data-stu-id="37847-124">An [Azure subscription](https://azure.microsoft.com/free/) to host the logic app</span></span>

## <a name="the-exercise"></a><span data-ttu-id="37847-125">Øvelsen</span><span class="sxs-lookup"><span data-stu-id="37847-125">The exercise</span></span>

<span data-ttu-id="37847-126">I slutningen af denne øvelse har du en logikapp, der har forbindelse til dit Human Resources-miljø og din OneDrive for Business-konto.</span><span class="sxs-lookup"><span data-stu-id="37847-126">At the end of this exercise, you will have a logic app that is connected to your Human Resources environment and your OneDrive for Business account.</span></span> <span data-ttu-id="37847-127">Logikappen eksporterer en datapakke fra Human Resources; vent til eksporten er fuldført, hent den eksporterede datapakke, og gem datapakken i den OneDrive for Business-mappe, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="37847-127">The logic app will export a data package from Human Resources, wait for the export to be completed, download the exported data package, and save the data package in the OneDrive for Business folder that you specified.</span></span>

<span data-ttu-id="37847-128">Den fuldførte logikapp ligner den i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="37847-128">The completed logic app will resemble the following illustration.</span></span>

![Oversigt over logikapp](media/integration-logic-app-overview.png)

### <a name="step-1-create-a-data-export-project-in-human-resources"></a><span data-ttu-id="37847-130">Trin 1: Opret et dataeksportprojekt i Human Resources</span><span class="sxs-lookup"><span data-stu-id="37847-130">Step 1: Create a data export project in Human Resources</span></span>

<span data-ttu-id="37847-131">Opret i Human Resources et dataeksportprojekt, der eksporterer arbejdere.</span><span class="sxs-lookup"><span data-stu-id="37847-131">In Human Resources, create a data export project that exports workers.</span></span> <span data-ttu-id="37847-132">Navngiv projektet **Eksport af medarbejdere**, og sørg for, at indstillingen **Generér datapakke** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="37847-132">Name the project **Export Workers**, and make sure that the **Generate data package** option is set to **Yes**.</span></span> <span data-ttu-id="37847-133">Føj en enkelt enhed (**Arbejder**) til projektet, og vælg det format, der skal eksporteres i.</span><span class="sxs-lookup"><span data-stu-id="37847-133">Add a single entity (**Worker**) to the project, and select the format to export in.</span></span> <span data-ttu-id="37847-134">(Microsoft Excel-formatet bruges i dette selvstudium).</span><span class="sxs-lookup"><span data-stu-id="37847-134">(Microsoft Excel format is used in this tutorial.)</span></span>

![Dataprojektet Eksport af medarbejdere](media/integration-logic-app-export-workers-project.png)

> [!IMPORTANT]
> <span data-ttu-id="37847-136">Husk navnet på dataeksportprojektet.</span><span class="sxs-lookup"><span data-stu-id="37847-136">Remember the name of the data export project.</span></span> <span data-ttu-id="37847-137">Du skal bruge det, når du opretter logikappen i næste trin.</span><span class="sxs-lookup"><span data-stu-id="37847-137">You will need it when you create the logic app in the next step.</span></span>

### <a name="step-2-create-the-logic-app"></a><span data-ttu-id="37847-138">Trin 2: Opret logikappen</span><span class="sxs-lookup"><span data-stu-id="37847-138">Step 2: Create the logic app</span></span>

<span data-ttu-id="37847-139">Hovedparten af opgaven omfatter oprettelse af logikappen.</span><span class="sxs-lookup"><span data-stu-id="37847-139">The bulk of the exercise involves creating the logic app.</span></span>

1. <span data-ttu-id="37847-140">Opret en logikapp i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="37847-140">In the Azure portal, create a logic app.</span></span>

    ![Side til oprettelse af logikapp](media/integration-logic-app-creation-1.png)

2. <span data-ttu-id="37847-142">Start med en tom logikapp i Logic Apps Designer.</span><span class="sxs-lookup"><span data-stu-id="37847-142">In the Logic Apps Designer, start with a blank logic app.</span></span>
3. <span data-ttu-id="37847-143">Tilføj en [udløser for gentagelsesplan](/azure/connectors/connectors-native-recurrence) for at køre logikappen hver 24. time (eller i henhold til en tidsplan efter eget valg).</span><span class="sxs-lookup"><span data-stu-id="37847-143">Add a [Recurrence Schedule trigger](/azure/connectors/connectors-native-recurrence) to run the logic app every 24 hours (or according to a schedule of your choice).</span></span>

    ![Dialogboksen Gentagelse](media/integration-logic-app-recurrence-step.png)

4. <span data-ttu-id="37847-145">Kald [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST-API for at planlægge eksport af din datapakke.</span><span class="sxs-lookup"><span data-stu-id="37847-145">Call the [ExportToPackage](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#exporttopackage) DMF REST API to schedule the export of your data package.</span></span>

    1. <span data-ttu-id="37847-146">Brug handlingen **Kald en HTTP-anmodning** fra HTTP med Azure AD-connector.</span><span class="sxs-lookup"><span data-stu-id="37847-146">Use the **Invoke an HTTP request** action from the HTTP with Azure AD connector.</span></span>

        - <span data-ttu-id="37847-147">**URL-adresse til grundlæggende ressourcer:** URL-adressen til dit Human Resources-miljø (medtag ikke oplysninger om sti/navneområde).</span><span class="sxs-lookup"><span data-stu-id="37847-147">**Base Resource URL:** The URL of your Human Resources environment (Don't include path/namespace information.)</span></span>
        - <span data-ttu-id="37847-148">**Azure AD-ressource URI-adresse:** `http://hr.talent.dynamics.com`</span><span class="sxs-lookup"><span data-stu-id="37847-148">**Azure AD Resource URI:** `http://hr.talent.dynamics.com`</span></span>

        > [!NOTE]
        > <span data-ttu-id="37847-149">Human Resources-tjenesten har endnu ikke en connector, der viser alle de API'er, der udgør REST API for DMF-pakken, f.eks. **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="37847-149">The Human Resources service doesn't yet provide a connector that exposes all the APIs that make up the DMF package REST API, such as **ExportToPackage**.</span></span> <span data-ttu-id="37847-150">Du skal i stedet kalde API'erne ved at bruge rå HTTPS-anmodninger via HTTP med Azure AD-connector.</span><span class="sxs-lookup"><span data-stu-id="37847-150">Instead, you must call the APIs by using raw HTTPS requests through the HTTP with Azure AD connector.</span></span> <span data-ttu-id="37847-151">Denne connector bruger Azure Active Directory (Azure AD) til godkendelse og autorisation til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="37847-151">This connector uses Azure Active Directory (Azure AD) for authentication and authorization to Human Resources.</span></span>

        ![HTTP med Azure AD-connector](media/integration-logic-app-http-aad-connector-step.png)

    2. <span data-ttu-id="37847-153">Log på Human Resources-miljøet via HTTP med Azure AD-connector.</span><span class="sxs-lookup"><span data-stu-id="37847-153">Sign in to your Human Resources environment through the HTTP with Azure AD connector.</span></span>
    3. <span data-ttu-id="37847-154">Konfigurer en HTTP **POST**-anmodning for at kalde **ExportToPackage** DMF REST-API'en.</span><span class="sxs-lookup"><span data-stu-id="37847-154">Set up an HTTP **POST** request to call the **ExportToPackage** DMF REST API.</span></span>

        - <span data-ttu-id="37847-155">**Metode:** POST</span><span class="sxs-lookup"><span data-stu-id="37847-155">**Method:** POST</span></span>
        - <span data-ttu-id="37847-156">**URL-adresse for anmodning:** https://\<hostname\>/navneområder/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span><span class="sxs-lookup"><span data-stu-id="37847-156">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.ExportToPackage</span></span>
        - <span data-ttu-id="37847-157">**Indhold i anmodningen:**</span><span class="sxs-lookup"><span data-stu-id="37847-157">**Body of the request:**</span></span>

            ```JSON
            {
                "definitionGroupId":"Export Workers",
                "packageName":"talent_package.zip",
                "executionId":"",
                "reExecute":false,
                "legalEntityId":"USMF"
            }
            ```

        ![Aktivere en HTTP-anmodningshandling](media/integration-logic-app-export-to-package-step.png)

    > [!TIP]
    > <span data-ttu-id="37847-159">Det kan være en god ide at omdøbe hvert trin, så det er mere sigende end standardnavnet **Kald en HTTP-anmodning**.</span><span class="sxs-lookup"><span data-stu-id="37847-159">You might want to rename each step so that it's more meaningful than the default name, **Invoke an HTTP request**.</span></span> <span data-ttu-id="37847-160">Du kan f.eks. omdøbe dette trin **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="37847-160">For example, you can rename this step **ExportToPackage**.</span></span>

5. <span data-ttu-id="37847-161">[Initialiser en variabel](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) for at gemme udførelsesstatus for anmodningen **ExportToPackage**.</span><span class="sxs-lookup"><span data-stu-id="37847-161">[Initialize a variable](/azure/logic-apps/logic-apps-create-variables-store-values#initialize-variable) to store the execution status of the **ExportToPackage** request.</span></span>

    ![Handlingen Initialiser variabel](media/integration-logic-app-initialize-variable-step.png)

6. <span data-ttu-id="37847-163">Vent, indtil udførelsesstatus for dataeksport er **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="37847-163">Wait until the execution status of the data export is **Succeeded**.</span></span>

    1. <span data-ttu-id="37847-164">Tilføj en [Indtil loop](/azure/logic-apps/logic-apps-control-flow-loops#until-loop), der gentages, indtil værdien af variablen **ExecutionStatus** er **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="37847-164">Add an [Until loop](/azure/logic-apps/logic-apps-control-flow-loops#until-loop) that repeats until the value of the **ExecutionStatus** variable is **Succeeded**.</span></span>
    2. <span data-ttu-id="37847-165">Tilføj en **Forsinkelse**-handling, der venter fem sekunder, før der sendes en forespørgsel om den aktuelle udførelsesstatus for eksporten.</span><span class="sxs-lookup"><span data-stu-id="37847-165">Add a **Delay** action that waits five seconds before it polls for the current execution status of the export.</span></span>

        ![Indtil løkke-container](media/integration-logic-app-until-loop-step.png)

        > [!NOTE]
        > <span data-ttu-id="37847-167">Angiv grænseantallet til **15** for at vente maksimalt 75 sekunder (15 gentagelser × 5 sekunder), til eksporten er fuldført.</span><span class="sxs-lookup"><span data-stu-id="37847-167">Set the limit count to **15** to wait a maximum of 75 seconds (15 iterations × 5 seconds) for the export to be completed.</span></span> <span data-ttu-id="37847-168">Hvis eksporten tager længere tid, skal du justere grænsen for antal efter behov.</span><span class="sxs-lookup"><span data-stu-id="37847-168">If your export takes more time, adjust the limit count as appropriate.</span></span>        

    3. <span data-ttu-id="37847-169">Tilføj en **Kald en HTTP-anmodning**-handling for at kalde [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST-API, og angiv variablen **ExecutionStatus** til resultatet af **GetExecutionSummaryStatus**-svaret.</span><span class="sxs-lookup"><span data-stu-id="37847-169">Add an **Invoke HTTP request** action to call the [GetExecutionSummaryStatus](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus) DMF REST API, and set the **ExecutionStatus** variable to the result of the **GetExecutionSummaryStatus** response.</span></span>

        > <span data-ttu-id="37847-170">I dette eksempel udføres der ikke fejlkontrol.</span><span class="sxs-lookup"><span data-stu-id="37847-170">This sample doesn't do error checking.</span></span> <span data-ttu-id="37847-171">**GetExecutionSummaryStatus**-API'en kan returnere ikke-gennemførte terminaltilstande (dvs. tilstande, der ikke er angivet til **Fuldført**).</span><span class="sxs-lookup"><span data-stu-id="37847-171">The **GetExecutionSummaryStatus** API can return non-successful terminal states (that is, states other than **Succeeded**).</span></span> <span data-ttu-id="37847-172">Yderligere oplysninger finder du i [API-dokumentation](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span><span class="sxs-lookup"><span data-stu-id="37847-172">For more information, see the [API documentation](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexecutionsummarystatus).</span></span>

        - <span data-ttu-id="37847-173">**Metode:** POST</span><span class="sxs-lookup"><span data-stu-id="37847-173">**Method:** POST</span></span>
        - <span data-ttu-id="37847-174">**URL-adresse for anmodning:** https://\<hostname\>/navneområder/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span><span class="sxs-lookup"><span data-stu-id="37847-174">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExecutionSummaryStatus</span></span>
        - <span data-ttu-id="37847-175">**Indhold i anmodningen:** body('Invoke\_an\_HTTP\_request')?['value']</span><span class="sxs-lookup"><span data-stu-id="37847-175">**Body of the request:** body('Invoke\_an\_HTTP\_request')?['value']</span></span>

            > [!NOTE]
            > <span data-ttu-id="37847-176">Du skal muligvis angive værdien for **Indhold i anmodningen** i kodevisning eller i funktionseditoren i designeren.</span><span class="sxs-lookup"><span data-stu-id="37847-176">You might have to enter the **Body of the request** value either in code view or in the function editor in the designer.</span></span>

        ![Handlingen Aktiver en HTTP-anmodning 2](media/integration-logic-app-get-execution-status-step.png)

        ![Handlingen Angiv variabel](media/integration-logic-app-set-variable-step.png)

        > [!IMPORTANT]
        > <span data-ttu-id="37847-179">Værdien for handlingen **Angiv variabel** (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) adskiller sig fra værdien for **Aktiver en HTTP-anmodning 2**-indholdsværdi, også selv om designeren viser værdierne på samme måde.</span><span class="sxs-lookup"><span data-stu-id="37847-179">The value for the **Set variable** action (**body('Invoke\_an\_HTTP\_request\_2')?['value']**) will differ from the value for the **Invoke an HTTP request 2** body value, even though the designer will show the values in the same way.</span></span>

7. <span data-ttu-id="37847-180">Hent URL-adressen til hentning for den eksporterede pakke.</span><span class="sxs-lookup"><span data-stu-id="37847-180">Get the download URL of the exported package.</span></span>

    - <span data-ttu-id="37847-181">Tilføj en **Kald en HTTP-anmodning**-handling for at kalde [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST-API'en.</span><span class="sxs-lookup"><span data-stu-id="37847-181">Add an **Invoke HTTP request** action to call the [GetExportedPackageUrl](../fin-ops-core/dev-itpro/data-entities/data-management-api.md#getexportedpackageurl) DMF REST API.</span></span>

        - <span data-ttu-id="37847-182">**Metode:** POST</span><span class="sxs-lookup"><span data-stu-id="37847-182">**Method:** POST</span></span>
        - <span data-ttu-id="37847-183">**URL-adresse for anmodning:** https://\<hostname\>/navneområder/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span><span class="sxs-lookup"><span data-stu-id="37847-183">**Url of the request:** https://\<hostname\>/namespaces/\<namespace\_guid\>/data/DataManagementDefinitionGroups/Microsoft.Dynamics.DataEntities.GetExportedPackageUrl</span></span>
        - <span data-ttu-id="37847-184">**Indhold i anmodningen:** {"executionId": body('GetExportedPackageURL')?['value']}</span><span class="sxs-lookup"><span data-stu-id="37847-184">**Body of the request:** {"executionId": body('GetExportedPackageURL')?['value']}</span></span>

        ![GetExportedPackageURL-handling](media/integration-logic-app-get-exported-package-step.png)

8. <span data-ttu-id="37847-186">Hent den eksporterede pakke.</span><span class="sxs-lookup"><span data-stu-id="37847-186">Download the exported package.</span></span>

    - <span data-ttu-id="37847-187">Tilføj en HTTP **GET**-anmodning (en indbygget [HTTP-connectorhandling](/azure/connectors/connectors-native-http)) for at hente pakken fra den URL-adresse, der blev returneret i forrige trin.</span><span class="sxs-lookup"><span data-stu-id="37847-187">Add an HTTP **GET** request (a built-in [HTTP connector action](/azure/connectors/connectors-native-http)) to download the package from the URL that was returned in the previous step.</span></span>

        - <span data-ttu-id="37847-188">**Metode:** GET</span><span class="sxs-lookup"><span data-stu-id="37847-188">**Method:** GET</span></span>
        - <span data-ttu-id="37847-189">**URI-adresse:** body('Invoke\_an\_HTTP\_request\_3').value</span><span class="sxs-lookup"><span data-stu-id="37847-189">**URI:** body('Invoke\_an\_HTTP\_request\_3').value</span></span>

            > [!NOTE]
            > <span data-ttu-id="37847-190">Du skal muligvis angive værdien for **URI-adresse** i kodevisning eller i funktionseditoren i designeren.</span><span class="sxs-lookup"><span data-stu-id="37847-190">You might have to enter the **URI** value either in code view or in the function editor in the designer.</span></span>

        ![HTTP GET-handling](media/integration-logic-app-download-file-step.png)

        > [!NOTE]
        > <span data-ttu-id="37847-192">Denne anmodning kræver ingen yderligere godkendelse, fordi den URL-adresse, som **GetExportedPackageUrl**-API'en returnerer, inkluderer et token for signaturer til delt adgang, der giver adgang til at hente filen.</span><span class="sxs-lookup"><span data-stu-id="37847-192">This request doesn't require any additional authentication, because the URL that the **GetExportedPackageUrl** API returns includes a shared access signatures token that grants access to download the file.</span></span>

9. <span data-ttu-id="37847-193">Gem den hentede pakke ved hjælp af [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness)-connector.</span><span class="sxs-lookup"><span data-stu-id="37847-193">Save the downloaded package by using the [OneDrive for Business](/azure/connectors/connectors-create-api-onedriveforbusiness) connector.</span></span>

    - <span data-ttu-id="37847-194">Tilføj en OneDrive for Business [Opret fil](/connectors/onedriveforbusinessconnector/#create-file)-handling.</span><span class="sxs-lookup"><span data-stu-id="37847-194">Add a OneDrive for Business [Create File](/connectors/onedriveforbusinessconnector/#create-file) action.</span></span>
    - <span data-ttu-id="37847-195">Opret forbindelse til OneDrive for Business-kontoen efter behov.</span><span class="sxs-lookup"><span data-stu-id="37847-195">Connect to your OneDrive for Business account, as required.</span></span>

        - <span data-ttu-id="37847-196">**Mappesti:** En mappe efter eget valg</span><span class="sxs-lookup"><span data-stu-id="37847-196">**Folder Path:** A folder of your choice</span></span>
        - <span data-ttu-id="37847-197">**Filnavn:** worker\_package.zip</span><span class="sxs-lookup"><span data-stu-id="37847-197">**File Name:** worker\_package.zip</span></span>
        - <span data-ttu-id="37847-198">**Filindhold:** Indholdet fra det forrige trin (dynamisk indhold)</span><span class="sxs-lookup"><span data-stu-id="37847-198">**File Content:** The body from the previous step (dynamic content)</span></span>

        ![Oprette filhandling](media/integration-logic-app-create-file-step.png)

### <a name="step-3-test-the-logic-app"></a><span data-ttu-id="37847-200">Trin 3: Test logikappen</span><span class="sxs-lookup"><span data-stu-id="37847-200">Step 3: Test the logic app</span></span>

<span data-ttu-id="37847-201">Hvis du vil teste logikappen, skal du vælge knappen **Kør** i designeren.</span><span class="sxs-lookup"><span data-stu-id="37847-201">To test your logic app, select the **Run** button in the designer.</span></span> <span data-ttu-id="37847-202">Du kan se, at trinnene i logikappen begynder at blive afviklet.</span><span class="sxs-lookup"><span data-stu-id="37847-202">You will see that the steps of the logic app start to run.</span></span> <span data-ttu-id="37847-203">Efter 30 til 40 sekunder bør logikappen være færdig med at køre, og din OneDrive for Business-mappe bør indeholde en ny pakkefil, der indeholder de eksporterede arbejdere.</span><span class="sxs-lookup"><span data-stu-id="37847-203">After 30 to 40 seconds, the logic app should finish running, and your OneDrive for Business folder should include a new package file that contains the exported workers.</span></span>

<span data-ttu-id="37847-204">Hvis der rapporteres om en fejl for et af trinnene, skal du vælge det trin, der er fejl ved, i designerne og undersøge felterne **Input** og **Output** for det.</span><span class="sxs-lookup"><span data-stu-id="37847-204">If a failure is reported for any step, select the failed step in the designer, and examine the **Inputs** and **Outputs** fields for it.</span></span> <span data-ttu-id="37847-205">Foretag fejlfinding, og juster trinnet som nødvendigt for at rette fejlene.</span><span class="sxs-lookup"><span data-stu-id="37847-205">Debug and adjust the step as required to correct the errors.</span></span>

<span data-ttu-id="37847-206">I følgende illustration vises det, hvordan Logic Apps Designer ser ud, når alle trin i logikappen kører korrekt.</span><span class="sxs-lookup"><span data-stu-id="37847-206">The following illustration shows what the Logic Apps Designer looks like when all the steps of the logic app run successfully.</span></span>

![Gennemført kørsel af logikapp](media/integration-logic-app-successful-run.png)

## <a name="summary"></a><span data-ttu-id="37847-208">Resume</span><span class="sxs-lookup"><span data-stu-id="37847-208">Summary</span></span>

<span data-ttu-id="37847-209">I dette selvstudium lærte du, hvordan du kan bruge en logikapp til at eksportere data fra Human Resources og gemme de eksporterede i en OneDrive for Business-mappe.</span><span class="sxs-lookup"><span data-stu-id="37847-209">In this tutorial, you learned how to use a logic app to export data from Human Resources and save the exported data to a OneDrive for Business folder.</span></span> <span data-ttu-id="37847-210">Du kan ændre trinene i dette selvstudium efter behov, så det passer til dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="37847-210">You can modify the steps of this tutorial as required to suit your business needs.</span></span>




[!INCLUDE[footer-include](../includes/footer-banner.md)]