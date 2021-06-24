---
title: Konfiguration til Finance Insights til offentlig forhåndsversion (forhåndsversion) - version 10.0.20 og senere
description: I dette emne beskrives de konfigurationstrin, der sætter systemet i gang med at bruge de egenskaber, der er tilgængelige i Finance Insights for offentlig forhåndsversion i version 10.0.20 og nyere.
author: ShivamPandey-msft
ms.date: 06/03/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2021-06-03
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 613bd4816e2f0c4fbb56cf79779a08c6a09592bd
ms.sourcegitcommit: 655b0e16c7aef6182cd58bc816b901470e1bb2ce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/10/2021
ms.locfileid: "6222606"
---
# <a name="configuration-for-finance-insights-for-public-preview-preview---version-10020-and-later"></a><span data-ttu-id="a3033-103">Konfiguration til Finance Insights til offentlig forhåndsversion (forhåndsversion) - version 10.0.20 og senere</span><span class="sxs-lookup"><span data-stu-id="a3033-103">Configuration for Finance insights for public preview (preview) - version 10.0.20 and later</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="a3033-104">Finance Insights kombinerer funktionalitet fra Microsoft Dynamics 365 Finance sammen med Dataverse, Azure og AI Builder for at levere effektive prognoseværktøjer til din organisation.</span><span class="sxs-lookup"><span data-stu-id="a3033-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="a3033-105">I dette emne beskrives konfiguration af Dynamics 365 Finance version 10.0.20, så dit system kan bruge de egenskaber, der er tilgængelige i Finance Insights for offentlig forhåndsversion.</span><span class="sxs-lookup"><span data-stu-id="a3033-105">This topic explains how to configure Dynamics 365 Finance version 10.0.20 so that your system can use the capabilities that are available in Finance insights public preview.</span></span>

> [!NOTE]
> <span data-ttu-id="a3033-106">De konfigurationstrin, der er beskrevet i dette emne, gælder kun for Finans version 10.0.20 og senere.</span><span class="sxs-lookup"><span data-stu-id="a3033-106">The configuration steps that are described in this topic apply only to Finance version 10.0.20 and later.</span></span> <span data-ttu-id="a3033-107">Hvis du vil konfigurere Finance Insights på version 10.0.19 og tidligere, skal du se [Konfiguration for Finance insights - versioner op til 10.0.18](configure-for-fin-insites.md).</span><span class="sxs-lookup"><span data-stu-id="a3033-107">'To set up Finance insights on version 10.0.19 and earlier, see [Configuration for Finance insights - versions up to 10.0.18](configure-for-fin-insites.md).</span></span>

## <a name="deploy-finance"></a><span data-ttu-id="a3033-108">Udrulle Finance</span><span class="sxs-lookup"><span data-stu-id="a3033-108">Deploy Finance</span></span>

<span data-ttu-id="a3033-109">Følg disse trin for at udrulle miljøerne.</span><span class="sxs-lookup"><span data-stu-id="a3033-109">Follow these steps to deploy the environments.</span></span>

1. <span data-ttu-id="a3033-110">I Microsoft Dynamics Lifecycle Services (LCS) skal du oprette eller opdatere et Finance-miljø.</span><span class="sxs-lookup"><span data-stu-id="a3033-110">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Finance environment.</span></span> <span data-ttu-id="a3033-111">Miljøet kræver appversion 10.0.20 eller nyere af Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="a3033-111">The environment requires app version 10.0.20 or later of Finance and Operations apps.</span></span>
2. <span data-ttu-id="a3033-112">Miljøet skal være et miljø med høj tilgængelighed (HA) i sandkassesystemet.</span><span class="sxs-lookup"><span data-stu-id="a3033-112">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="a3033-113">(Denne type miljø kaldes også et Niveau-2-miljø). Du kan finde flere oplysninger i [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="a3033-113">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="a3033-114">Hvis du konfigurerer Finance Insights i et sandkassemiljø, skal du muligvis kopiere produktionsdata til dette miljø, så du kan få forudsigelser, der virker.</span><span class="sxs-lookup"><span data-stu-id="a3033-114">If you are configuring Finance insights in a Sandbox environment, you might need to copy production data to that environment for predictions to work.</span></span> <span data-ttu-id="a3033-115">En forudsigelsesmodel bruger flere års data til at opbygge forudsigelser.</span><span class="sxs-lookup"><span data-stu-id="a3033-115">The prediction model uses multiple years of data to build predictions.</span></span> <span data-ttu-id="a3033-116">Contoso-demodataene indeholder ikke nok historikdata til at træne forudsigelsesmodellen korrekt.</span><span class="sxs-lookup"><span data-stu-id="a3033-116">The Contoso demo data doesn’t contain enough historical data to train the prediction model adequately.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="a3033-117">Konfigurer Dataverse</span><span class="sxs-lookup"><span data-stu-id="a3033-117">Configure Dataverse</span></span>

<span data-ttu-id="a3033-118">Benyt følgende fremgangsmåde til at konfigurere Dataverse til Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="a3033-118">Follow these steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="a3033-119">Åbn miljøsiden i LCS, og kontrollér, at sektionen **Intregration af Power Platform** allerede er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="a3033-119">In LCS, open the environment page, and verify that the **Power Platform Integration** section is already set up.</span></span>

    - <span data-ttu-id="a3033-120">Hvis det allerede er konfigureret, skal det Dataverse-miljønavn, der er knyttet til Finance-miljøet, være anført.</span><span class="sxs-lookup"><span data-stu-id="a3033-120">If it's already set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>
    - <span data-ttu-id="a3033-121">Hvis det ikke er konfigureret, skal du benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="a3033-121">If it isn't yet set up, follow these steps:</span></span>

        1. <span data-ttu-id="a3033-122">I sektionen **Integration af Power Platform** skal du vælge **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="a3033-122">In the **Power Platform Integration** section, select **Setup**.</span></span> <span data-ttu-id="a3033-123">Det kan tage op til en time at konfigurere miljøet.</span><span class="sxs-lookup"><span data-stu-id="a3033-123">Setup of the environment might take up to an hour.</span></span>
        2. <span data-ttu-id="a3033-124">Hvis Dataverse-miløjet er konfigureret korrekt, skal det Dataverse-miljønavn, der er tilknyttet Finance-miljøet, være anført.</span><span class="sxs-lookup"><span data-stu-id="a3033-124">If the Dataverse environment is successfully set up, the Dataverse environment name that is linked to the Finance environment should be listed.</span></span>

        > [!NOTE]
        > <span data-ttu-id="a3033-125">Når du har fuldført miljøopsætningen, skal du **ikke** vælge **Link til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="a3033-125">After you complete the environment setup, do **not** select **Link to CDS for Apps**.</span></span> <span data-ttu-id="a3033-126">Denne knap er ikke påkrævet for Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="a3033-126">This button isn't required for Finance insights.</span></span> <span data-ttu-id="a3033-127">Hvis du vælger den, kan du ikke konfigurere de påkrævede miljøtilføjelsesprogrammer i LCS.</span><span class="sxs-lookup"><span data-stu-id="a3033-127">If you select it, you won't be able to configure the required environment add-ins in LCS.</span></span>

## <a name="configure-azure"></a><span data-ttu-id="a3033-128">Konfigurere Azure</span><span class="sxs-lookup"><span data-stu-id="a3033-128">Configure Azure</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="a3033-129">Brug Azure Cloud Shell til at konfigurere Finance Insights Data Lake-ressourcer</span><span class="sxs-lookup"><span data-stu-id="a3033-129">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="a3033-130">Brug et Windows PowerShell-script</span><span class="sxs-lookup"><span data-stu-id="a3033-130">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="a3033-131">Der er angivet et Windows PowerShell-script, så du nemt kan konfigurere de Azure-ressourcer, der er beskrevet under [Konfigurere eksport til Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="a3033-131">A Windows PowerShell script has been provided so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="a3033-132">Hvis du foretrækker at foretage manuel opsætning, kan du springe denne procedure over og fuldføre proceduren i afsnittet [Manuel opsætning](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="a3033-132">If you prefer to do the setup manually, skip this procedure, and complete the procedure in the [Manual setup](#manual-setup) section instead.</span></span>

> [!NOTE]
> <span data-ttu-id="a3033-133">Brug følgende procedure til at køre Windows PowerShell-scriptet.</span><span class="sxs-lookup"><span data-stu-id="a3033-133">Use the following procedure to run the Windows PowerShell script.</span></span> <span data-ttu-id="a3033-134">Opsætningen virker muligvis ikke, hvis du bruger indstillingen **Prøv det** i Azure CLI, eller hvis du kører scriptet på din computer.</span><span class="sxs-lookup"><span data-stu-id="a3033-134">The setup might not work if you use the **Try it** option in Azure CLI or if you run the script on your computer.</span></span>

<span data-ttu-id="a3033-135">Udfør følgende trin for at konfigurere Azure ved hjælp af Windows PowerShell-scriptet.</span><span class="sxs-lookup"><span data-stu-id="a3033-135">Follow these steps to use the Windows PowerShell script to configure Azure.</span></span> <span data-ttu-id="a3033-136">Du skal have rettigheder til at oprette en Azure-ressourcegruppe, Azure-ressourcer og et Azure AD-program.</span><span class="sxs-lookup"><span data-stu-id="a3033-136">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="a3033-137">Yderligere oplysninger om de påkrævede tilladelser finder du i [Kontrollér Azure AD-tilladelser](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="a3033-137">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="a3033-138">Gå til dit Azure-abonnement på [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="a3033-138">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span>
2. <span data-ttu-id="a3033-139">Vælg **Cloud Shell** til højre for feltet **Søg**.</span><span class="sxs-lookup"><span data-stu-id="a3033-139">Select **Cloud Shell** to the right of the **Search** field.</span></span>
3. <span data-ttu-id="a3033-140">Vælg **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="a3033-140">Select **PowerShell**.</span></span>
4. <span data-ttu-id="a3033-141">Opret lager, hvis du bliver bedt om det.</span><span class="sxs-lookup"><span data-stu-id="a3033-141">Create storage if you're prompted to create it.</span></span>
5. <span data-ttu-id="a3033-142">Vælg fanen **Azure CLI**, og vælg **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="a3033-142">On the **Azure CLI** tab, select **Copy**.</span></span>
6. <span data-ttu-id="a3033-143">Åbn en ny fil i Notesblok, og indsæt den i Windows PowerShell-scriptet.</span><span class="sxs-lookup"><span data-stu-id="a3033-143">In Notepad, open a new file, and paste in the Windows PowerShell script.</span></span>
7. <span data-ttu-id="a3033-144">Gem filen som **ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="a3033-144">Save the file as **ConfigureDataLake.ps1**.</span></span>
8. <span data-ttu-id="a3033-145">Upload Windows PowerShell-scriptet til sessionen ved hjælp af menuindstillingen til upload i Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="a3033-145">Upload the Windows PowerShell script to the session by using the menu option for upload in Cloud Shell.</span></span>
9. <span data-ttu-id="a3033-146">Kør scriptet **.\ConfigureDataLake.ps1**.</span><span class="sxs-lookup"><span data-stu-id="a3033-146">Run the **.\ConfigureDataLake.ps1** script.</span></span>
10. <span data-ttu-id="a3033-147">Følg vejledningen for at køre scriptet.</span><span class="sxs-lookup"><span data-stu-id="a3033-147">Follow the prompts to run the script.</span></span>
11. <span data-ttu-id="a3033-148">Brug oplysningerne fra scriptoutputtet til at installere tilføjelsesprogrammet Eksportér til Data Lake i LCS.</span><span class="sxs-lookup"><span data-stu-id="a3033-148">Use the information from the script output to install the Export to Data Lake add-in in LCS.</span></span>

### <a name="manual-setup"></a><span data-ttu-id="a3033-149">Manuel opsætning</span><span class="sxs-lookup"><span data-stu-id="a3033-149">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="a3033-150">Tilføj ansøgninger til Azure AD-lejeren</span><span class="sxs-lookup"><span data-stu-id="a3033-150">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="a3033-151">Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="a3033-151">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="a3033-152">Vælg **Administrer \> Virksomhedsprogrammer**.</span><span class="sxs-lookup"><span data-stu-id="a3033-152">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="a3033-153">Søg efter følgende ansøgninger efter app-id.</span><span class="sxs-lookup"><span data-stu-id="a3033-153">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="a3033-154">Applikation</span><span class="sxs-lookup"><span data-stu-id="a3033-154">Application</span></span>                              | <span data-ttu-id="a3033-155">App-id</span><span class="sxs-lookup"><span data-stu-id="a3033-155">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="a3033-156">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="a3033-156">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="a3033-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="a3033-157">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="a3033-158">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="a3033-158">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="a3033-159">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="a3033-159">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="a3033-160">Godkendelsestjeneste til AI Builder</span><span class="sxs-lookup"><span data-stu-id="a3033-160">AI Builder Authorization Service</span></span>         | <span data-ttu-id="a3033-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="a3033-161">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="a3033-162">Hvis du ikke kan finde de foregående programmer, kan du prøve følgende trin.</span><span class="sxs-lookup"><span data-stu-id="a3033-162">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="a3033-163">Vælg menuen **Start** på din lokale computer, og søg efter **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="a3033-163">On your local computer, on the **Start** menu, search for **powershell**.</span></span>
2. <span data-ttu-id="a3033-164">Vælg og hold (eller højreklik) **Windows PowerShell**, og vælg derefter **Kør som administrator**.</span><span class="sxs-lookup"><span data-stu-id="a3033-164">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="a3033-165">Kør følgende kommando for at installere modulet **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="a3033-165">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="a3033-166">Hvis der kræves en NuGet-udbyder for at fortsætte, skal du vælge **J** for at installere den.</span><span class="sxs-lookup"><span data-stu-id="a3033-166">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="a3033-167">Hvis meddelelsen "Ikke-betroet lager" vises, skal vælge **J** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="a3033-167">If you receive an "Untrusted repository" message, select **Y** to continue.</span></span>
6. <span data-ttu-id="a3033-168">For hvert program, der skal tilføjes, skal du køre følgende kommandoer for at føje programmet til Azure AD.</span><span class="sxs-lookup"><span data-stu-id="a3033-168">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="a3033-169">Når du bliver bedt om det, skal du logge på som Azure AD-administrator.</span><span class="sxs-lookup"><span data-stu-id="a3033-169">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="a3033-170">Oprette Azure-ressourcer</span><span class="sxs-lookup"><span data-stu-id="a3033-170">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="a3033-171">Sørg for at oprette følgende ressourcer i samme Azure AD-forekomst som Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="a3033-171">Make sure that you create the following resources in the same Azure AD instance that the Dataverse environment is in.</span></span> <span data-ttu-id="a3033-172">Du kan ikke bruge ressourcer fra en anden Azure AD-forekomst.</span><span class="sxs-lookup"><span data-stu-id="a3033-172">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="a3033-173">Opret en lagerkonto:</span><span class="sxs-lookup"><span data-stu-id="a3033-173">Create a storage account:</span></span>

    1. <span data-ttu-id="a3033-174">Opret en Lagerkonto i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="a3033-174">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="a3033-175">Angiv følgende felter i dialogboksen **Opret lagerkonto**:</span><span class="sxs-lookup"><span data-stu-id="a3033-175">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="a3033-176">**Placering** - Vælg det datacenter, hvor dit miljø er placeret.</span><span class="sxs-lookup"><span data-stu-id="a3033-176">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="a3033-177">**Ydeevne** - Vi anbefaler, at du vælger **Standard**.</span><span class="sxs-lookup"><span data-stu-id="a3033-177">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="a3033-178">**Kontotype** - Du skal vælge **Lager V2**.</span><span class="sxs-lookup"><span data-stu-id="a3033-178">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="a3033-179">I dialogboksen **Avancerede indstillinger** til indstillingen **Data Lake-lager Gen2** skal du vælge **Aktiver** under funktionen **Hierarkiske navneområder**.</span><span class="sxs-lookup"><span data-stu-id="a3033-179">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="a3033-180">Hvis du ikke aktiverer denne funktion, kan du ikke forbruge data, som Finance and Operations-apps skriver ved hjælp af tjenester som f.eks. Power BI-dataflow.</span><span class="sxs-lookup"><span data-stu-id="a3033-180">If you don't enable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="a3033-181">Vælg **Gennemse og opret**.</span><span class="sxs-lookup"><span data-stu-id="a3033-181">Select **Review and create**.</span></span> <span data-ttu-id="a3033-182">Når installationen er fuldført, vises den nye ressource på Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="a3033-182">When the deployment is completed, the new resource is shown in the Azure portal.</span></span>
    5. <span data-ttu-id="a3033-183">Gå til den lagerkonto, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="a3033-183">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="a3033-184">Vælg **Adgangsnøgler** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="a3033-184">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="a3033-185">Kopiér og gem navnet på lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="a3033-185">Copy and save the name of the storage account.</span></span> <span data-ttu-id="a3033-186">Du skal angive denne værdi senere, når du konfigurerer Key Vault-hemmeligheder.</span><span class="sxs-lookup"><span data-stu-id="a3033-186">You will have to provide this value later, when you set up key vault secrets.</span></span>

2. <span data-ttu-id="a3033-187">Oprette en Key Vault:</span><span class="sxs-lookup"><span data-stu-id="a3033-187">Create a key vault:</span></span>

    1. <span data-ttu-id="a3033-188">Opret en Key Vault i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="a3033-188">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="a3033-189">Vælg det datacenter, hvor dit miljø er placeret, i feltet **Placering** i dialogboksen **Opret Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="a3033-189">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="a3033-190">Når Key Vault er oprettet, skal du gå til **Oversigt over Key Vault** og kopiere og gemme DNS-navnet.</span><span class="sxs-lookup"><span data-stu-id="a3033-190">After key vault is created, go to **Key Vault Overview**, and copy and save the DNS name.</span></span> <span data-ttu-id="a3033-191">Du skal angive denne værdi senere, når du konfigurerer tilføjelsesprogrammet Data Lake.</span><span class="sxs-lookup"><span data-stu-id="a3033-191">You will have to provide this value later, when you set up the Data Lake add-in.</span></span>

3. <span data-ttu-id="a3033-192">Oprette og registrere en Azure AD-ansøgning:</span><span class="sxs-lookup"><span data-stu-id="a3033-192">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="a3033-193">I [Azure-portalen](https://portal.azure.com) skal du gå til **Azure Active Directory**, og derefter vælge **App-registreringer**.</span><span class="sxs-lookup"><span data-stu-id="a3033-193">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="a3033-194">Vælg **Ny programregistrering**, og angiv følgende felter:</span><span class="sxs-lookup"><span data-stu-id="a3033-194">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="a3033-195">**Navn** - Angiv navnet på appen.</span><span class="sxs-lookup"><span data-stu-id="a3033-195">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="a3033-196">**Programtype** - Vælg **Web API**.</span><span class="sxs-lookup"><span data-stu-id="a3033-196">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="a3033-197">**Omdirigering af URI-konfiguration** - Angiv URL-adressen til Dynamics 365-forekomsten, f.eks. `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="a3033-197">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="a3033-198">Gå til den app, du lige har oprettet, og kopiér og gem værdien **Program-id (klient)**.</span><span class="sxs-lookup"><span data-stu-id="a3033-198">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="a3033-199">Du skal angive denne værdi senere, når du konfigurerer Key Vault-hemmeligheder.</span><span class="sxs-lookup"><span data-stu-id="a3033-199">You will have to provide this value later, when you set up key vault secrets.</span></span>
    4. <span data-ttu-id="a3033-200">Gå til **API-tilladelser**, og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="a3033-200">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="a3033-201">Vælg **Tilføj en tilladelse**.</span><span class="sxs-lookup"><span data-stu-id="a3033-201">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="a3033-202">Vælg **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="a3033-202">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="a3033-203">Når du har valgt delegerede rettigheder, skal du vælge **bruger\_repræsentation**.</span><span class="sxs-lookup"><span data-stu-id="a3033-203">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="a3033-204">Vælg **Tilføj tilladelser**.</span><span class="sxs-lookup"><span data-stu-id="a3033-204">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="a3033-205">Vælg **Certifikater \& hemmeligheder** i menuen for appen, og udfør derefter følgende trin for at oprette hemmeligheder for Key Vault:</span><span class="sxs-lookup"><span data-stu-id="a3033-205">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="a3033-206">Vælg **Ny klient-hemmelighed**.</span><span class="sxs-lookup"><span data-stu-id="a3033-206">Select **New client secret**.</span></span>
        2. <span data-ttu-id="a3033-207">Indtast et navn i feltet **Nøglebeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="a3033-207">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="a3033-208">Vælg en varighed, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="a3033-208">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="a3033-209">Der genereres en hemmelighed i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="a3033-209">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="a3033-210">Kopiér og gem den klienthemmelighedens værdi.</span><span class="sxs-lookup"><span data-stu-id="a3033-210">Copy and save the client secret value.</span></span> <span data-ttu-id="a3033-211">Du skal angive denne værdi senere, når du konfigurerer Key Vault-hemmeligheder.</span><span class="sxs-lookup"><span data-stu-id="a3033-211">You will have to provide this value later, when you set up key vault secrets.</span></span>

4. <span data-ttu-id="a3033-212">Oprette Key Vault-hemmeligheder:</span><span class="sxs-lookup"><span data-stu-id="a3033-212">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="a3033-213">Gå til den Key Vault, du har oprettet tidligere, og vælg **Hemmeligheder**.</span><span class="sxs-lookup"><span data-stu-id="a3033-213">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="a3033-214">Udfør følgende trin for hvert hemmelige navn i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="a3033-214">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="a3033-215">Vælg **Generer/importer**.</span><span class="sxs-lookup"><span data-stu-id="a3033-215">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="a3033-216">I dialogboksen **Opret en hemmelighed** i feltet **Uploadindstillinger** skal du vælge **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="a3033-216">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="a3033-217">Opret det hemmelige navn og værdien ud fra tabellen.</span><span class="sxs-lookup"><span data-stu-id="a3033-217">Create the secret name and value from the table.</span></span>
        4. <span data-ttu-id="a3033-218">Vælg **Aktiverfet**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a3033-218">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="a3033-219">Hemmeligheden oprettes og føjes til Key Vault.</span><span class="sxs-lookup"><span data-stu-id="a3033-219">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="a3033-220">Hemmeligt navn</span><span class="sxs-lookup"><span data-stu-id="a3033-220">Secret name</span></span>                       | <span data-ttu-id="a3033-221">Hemmelig værdi</span><span class="sxs-lookup"><span data-stu-id="a3033-221">Secret value</span></span>                                                                                 |
        |-----------------------------------|----------------------------------------------------------------------------------------------|
        | <span data-ttu-id="a3033-222">app-id</span><span class="sxs-lookup"><span data-stu-id="a3033-222">app-id</span></span>                            | <span data-ttu-id="a3033-223">App-id for det program, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="a3033-223">The app ID of the application that you created earlier.</span></span>                                      |
        | <span data-ttu-id="a3033-224">app-hemmelighed</span><span class="sxs-lookup"><span data-stu-id="a3033-224">app-secret</span></span>                        | <span data-ttu-id="a3033-225">Den klienthemmelighed, du tidligere har gemt.</span><span class="sxs-lookup"><span data-stu-id="a3033-225">The client secret that you saved earlier.</span></span>                                                    |
        | <span data-ttu-id="a3033-226">lagerkontonavn</span><span class="sxs-lookup"><span data-stu-id="a3033-226">storage-account-name</span></span>              | <span data-ttu-id="a3033-227">Navnet på den lagerkonto, du har oprettet tidligere, f.eks. **lagerkonto1**.</span><span class="sxs-lookup"><span data-stu-id="a3033-227">The name of the storage account that you created earlier, such as **storageaccount1**.</span></span>       |

5. <span data-ttu-id="a3033-228">Godkende programmet for at få adgang til Key Vault:</span><span class="sxs-lookup"><span data-stu-id="a3033-228">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="a3033-229">I [Azure-portalen](https://portal.azure.com) skal du åbne den Key Vault, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="a3033-229">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="a3033-230">Vælg adgangspolitikker.</span><span class="sxs-lookup"><span data-stu-id="a3033-230">Select the access policies.</span></span>
    3. <span data-ttu-id="a3033-231">Udfør følgende trin for hvert program i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="a3033-231">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="a3033-232">Vælg **Tilføj adgangspolitik** for at oprette en adgangspolitik.</span><span class="sxs-lookup"><span data-stu-id="a3033-232">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="a3033-233">I feltet **Hemmelige tilladelser** skal du vælge tilladelser fra tabellen.</span><span class="sxs-lookup"><span data-stu-id="a3033-233">In the **Secret permissions** field, select the permissions from the table.</span></span>
        3. <span data-ttu-id="a3033-234">I feltet **Vælg overordnet** skal du søge efter programmets viste navn i tabellen.</span><span class="sxs-lookup"><span data-stu-id="a3033-234">In the **Select principal** field, search for the application display name from the table.</span></span>
        4. <span data-ttu-id="a3033-235">Vælg **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="a3033-235">Select **Select**.</span></span>
        5. <span data-ttu-id="a3033-236">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="a3033-236">Select **Add**.</span></span>
        6. <span data-ttu-id="a3033-237">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a3033-237">Select **Save**.</span></span>

        | <span data-ttu-id="a3033-238">Applikation</span><span class="sxs-lookup"><span data-stu-id="a3033-238">Application</span></span>                                              | <span data-ttu-id="a3033-239">Rettigheder</span><span class="sxs-lookup"><span data-stu-id="a3033-239">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="a3033-240">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="a3033-240">The display name of the new application that you created</span></span> | <span data-ttu-id="a3033-241">Hent, Sæt på liste</span><span class="sxs-lookup"><span data-stu-id="a3033-241">Get, List</span></span>   |
        | <span data-ttu-id="a3033-242">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="a3033-242">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="a3033-243">Hent, Sæt på liste</span><span class="sxs-lookup"><span data-stu-id="a3033-243">Get, List</span></span>   |

6. <span data-ttu-id="a3033-244">Tildele roller for at få adgang til lagerkontoen:</span><span class="sxs-lookup"><span data-stu-id="a3033-244">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="a3033-245">I [Azure-portalen](https://portal.azure.com) skal du åbne den lagerkonto, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="a3033-245">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="a3033-246">Vælg **Adgangskontrol (IAM)**, og vælg derefter **Rolletildelinger**.</span><span class="sxs-lookup"><span data-stu-id="a3033-246">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="a3033-247">Vælg **Tilføj, Tilføj rolletildeling**.</span><span class="sxs-lookup"><span data-stu-id="a3033-247">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="a3033-248">Udfør følgende trin for hvert program i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="a3033-248">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="a3033-249">Vælg rollen i tabellen.</span><span class="sxs-lookup"><span data-stu-id="a3033-249">Select the role from the table.</span></span>
        2. <span data-ttu-id="a3033-250">Forlad feltet **Tildel adgangsrettigheder til**, der er angivet til **Azure AD-bruger, -gruppe eller -tjenesteprincipal**.</span><span class="sxs-lookup"><span data-stu-id="a3033-250">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="a3033-251">I feltet **Vælg** skal du angive programmet fra tabellen.</span><span class="sxs-lookup"><span data-stu-id="a3033-251">In the **Select** field, enter the application from the table.</span></span>
        4. <span data-ttu-id="a3033-252">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a3033-252">Select **Save**.</span></span>

        | <span data-ttu-id="a3033-253">Applikation</span><span class="sxs-lookup"><span data-stu-id="a3033-253">Application</span></span>                                              | <span data-ttu-id="a3033-254">Rolle</span><span class="sxs-lookup"><span data-stu-id="a3033-254">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="a3033-255">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="a3033-255">The display name of the new application that you created</span></span> | <span data-ttu-id="a3033-256">Ejer</span><span class="sxs-lookup"><span data-stu-id="a3033-256">Owner</span></span>                       |
        | <span data-ttu-id="a3033-257">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="a3033-257">The display name of the new application that you created</span></span> | <span data-ttu-id="a3033-258">Bidragyder</span><span class="sxs-lookup"><span data-stu-id="a3033-258">Contributor</span></span>                 |
        | <span data-ttu-id="a3033-259">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="a3033-259">The display name of the new application that you created</span></span> | <span data-ttu-id="a3033-260">Bidragyder til lagerkonto</span><span class="sxs-lookup"><span data-stu-id="a3033-260">Storage Account Contributor</span></span> |
        | <span data-ttu-id="a3033-261">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="a3033-261">The display name of the new application that you created</span></span> | <span data-ttu-id="a3033-262">Ejer af Blob Data-lager</span><span class="sxs-lookup"><span data-stu-id="a3033-262">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="a3033-263">**Godkendelsestjeneste til AI Builder**</span><span class="sxs-lookup"><span data-stu-id="a3033-263">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="a3033-264">Læser af Blob Data-lager</span><span class="sxs-lookup"><span data-stu-id="a3033-264">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="a3033-265">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="a3033-265">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    Assert-ScriptSetup

    $ClientAppName = 'Finance Data Lake Application'
    $DefaultSecretExpiryInYear = 1
    $MicrosoftDynamicsERPMicroservicesAppId = '0cdb527f-a8d1-4bf8-9436-b352c68682b2'
    $MicrosoftDynamicsERPMicroservicesCDSAppId = '703e2651-d3fc-48f5-942c-74274233dba8'
    $AIBuilderAuthorizationServiceAppId = 'ad40333e-9910-4b61-b281-e3aeeb8c3ef3'
    $KeyVaultServicePrincipalAppId = 'cfa8b339-82a2-471a-a3c9-0fc0be7a4093'
    $GraphServicePrincipalAppId = '00000003-0000-0000-c000-000000000000'

    Import-Module AzureAD.Standard.Preview
    $connectAzureADParameters = @{ 'Identity' = $true; 'TenantId' = $env:ACC_TID }
    $azContext = AzureAD.Standard.Preview\Connect-AzureAD @connectAzureADParameters
    $userContext = ConvertFrom-Json ((az ad signed-in-user show) -join '')
    $user = Get-AzureADUser -Filter ("UserPrincipalName eq '" + $userContext.UserPrincipalName + "'")

    Set-AzureSubscription
    
    $resourceGroup = $null
    $ResourceGroupName = 'D365FinanceInsightsDataLake'
    $ResourceGroupNameSuffix = ''
    $FullResourceGroupName = ''
    Write-Output ("The default Azure Resource Group name is '{0}'" -f $ResourceGroupName)
    while (-not ($resourceGroup)) {
        $ResourceGroupNameSuffix = (Read-Host -Prompt "Enter optional Azure Resource Group name suffix: (leave blank for no suffix)")
        if ([string]::IsNullOrWhitespace($ResourceGroupNameSuffix))
        {
            $FullResourceGroupName = $ResourceGroupName
        }
        else
        {
            if ($ResourceGroupNameSuffix -notmatch "^[A-Za-z0-9]+$") {
                Write-Warning "The Azure Resource Group name suffix can only include alphanumeric characters."
                continue
            }

            if ($ResourceGroupNameSuffix.Length -gt 60) {
                Write-Warning "The Azure Resource Group name suffix cannot be longer than 60 characters."
                continue
            }

            $FullResourceGroupName = $ResourceGroupName + $ResourceGroupNameSuffix
        }
        
        $resourceGroup = Get-AzResourceGroup -Name $FullResourceGroupName -ErrorAction SilentlyContinue

        if (-not ($resourceGroup)) {
            Write-Output ("Your new Azure Resource Group name is '{0}'" -f $FullResourceGroupName)
            $resourceLocation = ''
            $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
            while ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations))) {
                $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
                if ($resourceLocation -eq 'help') {
                    Write-Output ("List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
                elseif ([string]::IsNullOrWhitespace($resourceLocation) -or (-not ($resourceLocation -in $azResourceLocations)))
                {
                    Write-Warning ("The provided location is not available for resource group. List of available regions is '{0}'" -f ($azResourceLocations -join ','))
                }
            }
            $resourceGroup = New-AzResourceGroup -Name $FullResourceGroupName -Location $resourceLocation
            Write-Output ("Created Azure Resource Group '{0}'" -f $resourceGroup.ResourceGroupName)
        }
        else {
            Write-Output ("Found Azure Resource Group '{0}'" -f ($resourceGroup.ResourceGroupName))
        }
    }

    Write-Output '================================================================================='
    $MicrosoftDynamicsERPMicroservicesAppObjectId = Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId
    Create-ADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Out-Null
    $aibuilderAuthorizationServiceObjectId = Create-ADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId
    Write-Output ('=================================================================================')

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $ClientAppName + "'")
    if (-not ($clientAppSPN)) {
        $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        if (-not $keyVaultPrincipal)
        {
            New-AzureADServicePrincipal -AppId $KeyVaultServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Key Vault principal to AAD"
            $keyVaultPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $KeyVaultServicePrincipalAppId + "'")
        }
        $keyVaultAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $keyVaultAccess.ResourceAppId = $keyVaultPrincipal.AppId
        $keyVaultAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $keyVaultPrincipal.Oauth2Permissions.Id, "Scope")

        $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        if (-not $graphPrincipal)
        {
            New-AzureADServicePrincipal -AppId $GraphServicePrincipalAppId | Format-Table -AutoSize
            Write-Output "Added Graph principal to AAD"
            $graphPrincipal = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $GraphServicePrincipalAppId + "'")
        }
        $userRead = $graphPrincipal.Oauth2Permissions | Where-Object { $_.Type -eq "User" -and $_.Value -eq "User.Read" }
        $graphAccess = New-Object -TypeName "Microsoft.Open.AzureAD.Model.RequiredResourceAccess"
        $graphAccess.ResourceAppId = $graphPrincipal.AppId
        $graphAccess.ResourceAccess = (New-Object -TypeName "microsoft.open.azuread.model.resourceAccess" -ArgumentList $userRead.Id, "Scope")

        $clientApp = New-AzureADApplication -DisplayName $ClientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($ClientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $ClientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $ClientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($DefaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    try {
        $deployment = New-AzResourceGroupDeployment -ResourceGroupName $FullResourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId -Force -ErrorAction Stop
    }
    catch {
        $ErrorMessage = $_.Exception.Message
        if ($ErrorMessage.Contains("not allowed to be updated"))
        {
            Write-Error ($ErrorMessage)
            Write-Warning "Some items in the existing resource group $FullResourceGroupName could not be updated. To resolve the issue, remove the existing resource group $FullResourceGroupName and run the script again."
        }
        else {
            throw
        }

    }
    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
        
        $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
        $tenantId = (Get-AzContext).Tenant.Id

        Write-Output "Values for LCS Data Lake Add-In:"
        Write-Output ("  Tenant ID:                         " + $tenantId)
        Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
        Write-Output "  Storage account secret name:       storage-account-name"
        Write-Output "  Application ID secret name:        app-id"
        Write-Output "  Application Secret secret name:    app-secret"
        Write-Warning "Copy this information for the LCS Add-in for easy access. Azure Cloud Shell will eventually time out and close."

        Write-Output '================================================================================='
        Write-Output "Values for System parameters > Data connections:"
        Write-Output ("  Application ID:                    " + $clientAppId)
        Write-Output ("  Application Secret:                " + $ClientAppSecret)
        Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
        Write-Output "  Secret name:                       storage-account-connection-string"
        Write-Warning "Copy this information for the System parameters for easy access. Azure Cloud Shell will eventually time out and close."
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $FullResourceGroupName)
    }
}

function Assert-ScriptSetup {
    if ($PSVersionTable.PSEdition -ne 'Core' -or -not $env:ACC_TID) { 
        throw "This script needs to be uploaded and run from Azure Cloud Shell (PowerShell)." 
    }
    
    if ((Get-AzContext) -eq $null -and (Connect-AzAccount) -eq $null) {
        throw 'Unable to connect to Azure account.'
    }
}

function Set-AzureSubscription {
    $azSubscription = $null
    while (-not ($azSubscription)) {
        $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (leave blank for default)")
        if ([string]::IsNullOrWhitespace($subscriptionId)){
            break
        }
        elseif (-not [guid]::TryParse($subscriptionId, $([ref][guid]::Empty))) {
                Write-Warning "Azure Subscription ID must be a valid GUID."
                continue
        }

        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }
}

function Create-ADServicePrincipal {
    param (
        [string] $AppId
    )

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AppId | Out-Null
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AppId + "'")
        Write-Host ("Added AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }
    else {
        Write-Host ("Found AAD Enterprise Application {0} with Application ID {1}" -f $service.DisplayName,$AppId)
    }

    return $service.ObjectId
}

$azureTemplate = @"
{
    "contentVersion": "1.0.0.0",
    "parameters": {
      "aibuilderAppObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of the AI Builder application."
        }
      },
      "clientAppId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the application ID of client application."
        }
      },
      "clientAppSecret": {
        "type": "String",
        "metadata": {
          "description": "Specifies the Azure App ID client secret to in azure key vault."
        }
      },
      "clientAppSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of a client application service principal."
        }
      },
      "userSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of tenant admin service principal."
        }
      },
      "microserviceSpObjectId": {
        "type": "string",
        "metadata": {
          "description": "Specifies the object ID of Microsoft Dynamics ERP Microservices service principal."
        }
      },
      "storageAccountType": {
        "type": "string",
        "defaultValue": "Standard_LRS",
        "allowedValues": [
          "Standard_LRS",
          "Standard_GRS",
          "Standard_ZRS",
          "Premium_LRS"
        ],
        "metadata": {
          "description": "Storage Account type"
        }
      }
    },
    "variables": {
      "storageAccountApiVersion": "2019-06-01",
      "keyVaultApiVersion": "2018-02-14",
      "secretsPermissions": [
        "list",
        "get"
      ],
      "location": "[resourceGroup().location]",
      "storageAccountName": "[concat('store', uniquestring(resourceGroup().id))]",
      "keyVaultName": "[concat('keyvault', uniquestring(resourceGroup().id))]",
      "owner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '8e3af657-a8ff-443c-a75c-2fe8c4bcb635')]",
      "contributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b24988ac-6180-42a0-ab88-20f7382dd24c')]",
      "storageAccountContributor": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '17d1049b-9a84-46fb-8f53-869881c3d3ab')]",
      "storageBlobDataOwner": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', 'b7e6dc6d-f1e8-4753-8033-0f276bb0955b')]",
      "storageBlobDataReader": "[concat('/subscriptions/', subscription().subscriptionId, '/providers/Microsoft.Authorization/roleDefinitions/', '2a2b9908-6ea1-4ae2-8e65-a410df84e7d1')]"
    },
    "resources": [
      {
        "type": "Microsoft.Storage/storageAccounts",
        "apiVersion": "[variables('storageAccountApiVersion')]",
        "name": "[variables('storageAccountName')]",
        "location": "[variables('location')]",
        "sku": {
          "name": "[parameters('storageAccountType')]"
        },
        "kind": "StorageV2",
        "properties": {
          "accessTier": "Hot",
          "supportsHttpsTrafficOnly": true,
          "isHnsEnabled": true
        },
        "resources": [
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'1')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('owner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'2')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('contributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'3')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageAccountContributor')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'4')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataOwner')]",
              "principalId": "[parameters('clientAppSpObjectId')]"
            }
          },
          {
            "type": "Microsoft.Storage/storageAccounts/providers/roleAssignments",
            "apiVersion": "2018-09-01-preview",
            "name": "[concat(variables('storageAccountName'), '/Microsoft.Authorization/', guid(uniqueString(variables('storageAccountName'),'5')))]",
            "dependsOn": [
              "[variables('storageAccountName')]"
            ],
            "properties": {
              "roleDefinitionId": "[variables('storageBlobDataReader')]",
              "principalId": "[parameters('aibuilderAppObjectId')]"
            }
          }
        ]
      },
      {
        "type": "Microsoft.KeyVault/vaults",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "name": "[variables('keyVaultName')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName'))]"
        ],
        "tags": {
        },
        "properties": {
          "enabledForDeployment": false,
          "enabledForTemplateDeployment": false,
          "enabledForDiskEncryption": false,
          "enableRbacAuthorization": false,
          "accessPolicies": [
            {
              "objectId": "[parameters('clientAppSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('microserviceSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            },
            {
              "objectId": "[parameters('userSpObjectId')]",
              "tenantId": "[subscription().tenantId]",
              "permissions": {
                "secrets": "[variables('secretsPermissions')]"
              }
            }
          ],
          "tenantId": "[subscription().tenantId]",
          "sku": {
            "name": "Standard",
            "family": "A"
          },
          "enableSoftDelete": false,
          "networkAcls": {
            "defaultAction": "Allow",
            "bypass": "AzureServices"
          }
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-id')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppId')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'app-secret')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[parameters('clientAppSecret')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-name')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[variables('storageAccountName')]"
        }
      },
      {
        "type": "Microsoft.KeyVault/vaults/secrets",
        "name": "[concat(variables('keyVaultName'), '/', 'storage-account-connection-string')]",
        "apiVersion": "[variables('keyVaultApiVersion')]",
        "location": "[variables('location')]",
        "dependsOn": [
          "[resourceId('Microsoft.KeyVault/vaults', variables('keyVaultName'))]"
        ],
        "properties": {
          "value": "[concat('DefaultEndpointsProtocol=https;AccountName=', variables('storageAccountName'), ';AccountKey=', listKeys(resourceId('Microsoft.Storage/storageAccounts', variables('storageAccountName')), variables('storageAccountApiVersion')).keys[0].value, ';EndpointSuffix=core.windows.net')]"
        }
      }
    ],
    "outputs": {
      "storageAccountName": {
        "type": "string",
        "value": "[variables('storageAccountName')]"
      },
      "keyVaultName": {
        "type": "string",
        "value": "[variables('keyVaultName')]"
      }
    }
  }
"@

try {
  Start-Transcript -path (Join-Path $HOME Provision-FinInsights-Azure.log)
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message

  if ($PSItem.Exception.StackTrace -ne $null)
  {
      Write-Warning $_.Exception.StackTrace
  }

  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}
finally {
  Stop-Transcript
}
```
---

## <a name="configure-the-export-to-data-lake-add-in"></a><span data-ttu-id="a3033-266">Konfigurere tilføjelsesprogrammet Eksportér til Data Lake</span><span class="sxs-lookup"><span data-stu-id="a3033-266">Configure the Export to Data Lake add-in</span></span>

<span data-ttu-id="a3033-267">Udfør følgende trin for at bruge LCS til at tilføje tilføjelsesprogrammet Eksportér til Data Lake i miljøet.</span><span class="sxs-lookup"><span data-stu-id="a3033-267">Follow these steps to use LCS to add the Export to Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="a3033-268">Log på LCS, og vælg derefter detaljerede oplysninger under miljønavnet på højre side af siden, vælg **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="a3033-268">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="a3033-269">Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="a3033-269">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="a3033-270">Vælg **Eksporter til Data Lake**-tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="a3033-270">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="a3033-271">Angiv følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="a3033-271">Enter the following values.</span></span>

    | <span data-ttu-id="a3033-272">Værdi</span><span class="sxs-lookup"><span data-stu-id="a3033-272">Value</span></span>                                                              | <span data-ttu-id="a3033-273">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="a3033-273">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="a3033-274">Lejer-id på det Azure-abonnement, hvor Key Vault er placeret</span><span class="sxs-lookup"><span data-stu-id="a3033-274">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="a3033-275">Det lejer-id, hvor lagerkontoen, apps og Key Vault er placeret.</span><span class="sxs-lookup"><span data-stu-id="a3033-275">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="a3033-276">Hvis du vil finde denne værdi, skal åbne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere værdien **Lejer-id**.</span><span class="sxs-lookup"><span data-stu-id="a3033-276">To obtain this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="a3033-277">Angiv DNS-navn for Key Vault</span><span class="sxs-lookup"><span data-stu-id="a3033-277">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="a3033-278">DNS-navnet på Key Vault, som f.eks. `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="a3033-278">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> |
    | <span data-ttu-id="a3033-279">Angiv den hemmelighed, der indeholder navnet på lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="a3033-279">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="a3033-280">**lagerkontonavn**</span><span class="sxs-lookup"><span data-stu-id="a3033-280">**storage-account-name**</span></span> |
    | <span data-ttu-id="a3033-281">Hemmeligt navn på app-id, der skal bruges til at få adgang til Data Lake</span><span class="sxs-lookup"><span data-stu-id="a3033-281">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="a3033-282">**app-id**</span><span class="sxs-lookup"><span data-stu-id="a3033-282">**app-id**</span></span> |
    | <span data-ttu-id="a3033-283">Hemmeligt navn på appens klienthemmelighed</span><span class="sxs-lookup"><span data-stu-id="a3033-283">Secret name for App client secret</span></span>                                  | <span data-ttu-id="a3033-284">**app-hemmelighed**</span><span class="sxs-lookup"><span data-stu-id="a3033-284">**app-secret**</span></span> |

5. <span data-ttu-id="a3033-285">Acceptér betingelserne, og vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="a3033-285">Agree to the terms, and then select **Install**.</span></span>

<span data-ttu-id="a3033-286">Tilføjelsesprogrammet vil blive installeret inden for et par minutter.</span><span class="sxs-lookup"><span data-stu-id="a3033-286">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-the-finance-insights-add-in"></a><span data-ttu-id="a3033-287">Konfigurere tilføjelsesprogrammet Finance Insights</span><span class="sxs-lookup"><span data-stu-id="a3033-287">Configure the Finance insights add-in</span></span>

> [!NOTE]
> <span data-ttu-id="a3033-288">Hvis du tidligere har installeret Hent Insights-tilføjelsesprogrammet, skal du afinstallere det, før du fuldfører følgende procedure.</span><span class="sxs-lookup"><span data-stu-id="a3033-288">If you previously installed the Get insights add-in, uninstall it before you complete the following procedure.</span></span>

<span data-ttu-id="a3033-289">Følg disse trin for at installere tilføjelsesprogrammet Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="a3033-289">Follow these steps to install the Finance insights add-in.</span></span>

1. <span data-ttu-id="a3033-290">Log på LCS, og vælg derefter detaljerede oplysninger under miljønavnet på højre side af siden, vælg **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="a3033-290">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="a3033-291">Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="a3033-291">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="a3033-292">Vælg tilføjelsesprogrammet **Finance Insights**.</span><span class="sxs-lookup"><span data-stu-id="a3033-292">Select the **Finance insights** add-in.</span></span>
4. <span data-ttu-id="a3033-293">Acceptér betingelserne, og vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="a3033-293">Agree to the terms, and then select **Install**.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="a3033-294">Feedback og support</span><span class="sxs-lookup"><span data-stu-id="a3033-294">Feedback and support</span></span>

<span data-ttu-id="a3033-295">Send en e-mail til [Finance Insights (forhåndsversion)](mailto:fiap@microsoft.com), hvis du er interesseret i at give feedback eller har brug for support.</span><span class="sxs-lookup"><span data-stu-id="a3033-295">If you're interested in providing feedback, or if you require support, send an email to [Finance insights (Preview)](mailto:fiap@microsoft.com).</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
