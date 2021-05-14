---
title: Konfiguration til Finance Insights (prøveversion)
description: I dette emne beskrives de konfigurationstrin, der sætter systemet i gang med at bruge de egenskaber, der er tilgængelige i Finance Insights.
author: ShivamPandey-msft
ms.date: 11/25/2020
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
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 60e4d69157d7b73bd9e47310adae320687230080
ms.sourcegitcommit: a202bf67c3c2c054e2a47cb7b3145cb7c0ee635e
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/25/2021
ms.locfileid: "5941220"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="9d53f-103">Konfiguration til Finance Insights (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="9d53f-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview banner](../includes/preview-banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="9d53f-104">Finance Insights kombinerer funktionalitet fra Microsoft Dynamics 365 Finance sammen med Microsoft Dataverse, Azure og AI Builder for at levere effektive prognoseværktøjer til din organisation.</span><span class="sxs-lookup"><span data-stu-id="9d53f-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Microsoft Dataverse, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="9d53f-105">I dette emne beskrives de konfigurationstrin, der sætter systemet i gang med at bruge de egenskaber, der er tilgængelige i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="9d53f-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="9d53f-106">Installér Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="9d53f-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="9d53f-107">Følg disse trin for at installere miljøerne.</span><span class="sxs-lookup"><span data-stu-id="9d53f-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="9d53f-108">I Microsoft Dynamics Lifecycle Services (LCS) skal du oprette eller opdatere et Dynamics 365 Finance-miljø.</span><span class="sxs-lookup"><span data-stu-id="9d53f-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="9d53f-109">Miljøet kræver programversion 10.0.11/Platformopdatering 35 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="9d53f-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="9d53f-110">Miljøet skal være et miljø med høj tilgængelighed (HA) i sandkassesystemet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="9d53f-111">(Denne type miljø kaldes også et Niveau-2-miljø). Du kan finde flere oplysninger i [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="9d53f-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="9d53f-112">Hvis du bruger Contoso-demodata, skal du bruge yderligere eksempeldata for at kunne bruge debitorbetalingsforudsigelser, likviditetsbudgetter og budgetprognosefunktioner.</span><span class="sxs-lookup"><span data-stu-id="9d53f-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-dataverse"></a><span data-ttu-id="9d53f-113">Konfigurer Dataverse</span><span class="sxs-lookup"><span data-stu-id="9d53f-113">Configure Dataverse</span></span>

<span data-ttu-id="9d53f-114">Benyt følgende fremgangsmåde til at konfigurere Dataverse for Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="9d53f-114">Use the following steps to configure Dataverse for Finance insights.</span></span>

1. <span data-ttu-id="9d53f-115">Åbn miljøsiden i LCS, og kontroller, at sektionen **Intregration af Power Platform** allerede er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="9d53f-115">Open the environment page in LCS and verify that the **Power Platform Integration** section is already setup.</span></span>
    1. <span data-ttu-id="9d53f-116">Hvis den allerede er konfigureret, skal det Dataverse-miljønavn, der er knyttet Dynamics 365 Finance-miljøet, være anført.</span><span class="sxs-lookup"><span data-stu-id="9d53f-116">If it is already set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="9d53f-117">Kopier Dataverse-miljønavnet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-117">Copy the Dataverse environment name.</span></span>
    2. <span data-ttu-id="9d53f-118">Hvis den ikke er konfigureret, skal du benytte følgende fremgangsmåde:</span><span class="sxs-lookup"><span data-stu-id="9d53f-118">If it is not set up, follow these steps:</span></span>
        1. <span data-ttu-id="9d53f-119">Klik på knappen **Opsætning** i sektionen Integration af Power Platform.</span><span class="sxs-lookup"><span data-stu-id="9d53f-119">Select the **Setup** button in the Power Platform Integration section.</span></span> <span data-ttu-id="9d53f-120">Det kan tage op til en time, før miljøet er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="9d53f-120">It may take up to an hour for the environment to be set up.</span></span>
        2. <span data-ttu-id="9d53f-121">Hvis Dataverse-miløjet er konfigureret korrekt, skal det Dataverse-miljønavn, der er tilknyttet Dynamics 365 Finance-miljøet, være anført.</span><span class="sxs-lookup"><span data-stu-id="9d53f-121">If the Dataverse environment is successfully set up, the Dataverse environment name linked to the Dynamics 365 Finance Environment should be listed.</span></span> <span data-ttu-id="9d53f-122">Kopier Dataverse-miljønavnet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-122">Copy the Dataverse environment name.</span></span>
> [!NOTE]
> <span data-ttu-id="9d53f-123">Når du har fuldført miljøkonfigurationen, skal du **IKKE** vælge knappen **Link til CDS for Apps**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-123">After completing the environment set up, **DO NOT** select the **Link to CDS for Apps** button.</span></span> <span data-ttu-id="9d53f-124">Dette er ikke nødvendigt for Finance Insights og vil deaktivere muligheden for at fuldføre de nødvendige tilføjelsesprogrammer for miljø i LCS.</span><span class="sxs-lookup"><span data-stu-id="9d53f-124">This is not needed for Finance Insights and will disable the ability to complete the required Environment Add-ins in LCS.</span></span>

2. <span data-ttu-id="9d53f-125">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com/), og udfør følgende trin for at oprette et nyt Dataverse-miljø i samme Active Directory-lejer:</span><span class="sxs-lookup"><span data-stu-id="9d53f-125">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Dataverse environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="9d53f-126">Åbn siden **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-126">Open the **Environments** page.</span></span>

        <span data-ttu-id="9d53f-127">Siden [![Miljøer](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="9d53f-127">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="9d53f-128">Vælg Dataverse-miljøet, der er oprettet ovenfor, og vælg derefter **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-128">Select the Dataverse environment created above and then select **Settings**.</span></span>
    3. <span data-ttu-id="9d53f-129">Vælg **Ressourcer \> Alle tidligere indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-129">Select **Resources \> All Legacy Settings**.</span></span>
    4. <span data-ttu-id="9d53f-130">Vælg indstillinger på den øverste navigationslinje **Indstillinger**, og vælg derefter **Tilpasninger**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-130">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    5. <span data-ttu-id="9d53f-131">Vælg **Udviklerressourcer**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-131">Select **Developer Resources**.</span></span>
    6. <span data-ttu-id="9d53f-132">Kopiér værdien af **Dataverse-organisations-id**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-132">Copy the **Dataverse organization ID** value.</span></span>
    7. <span data-ttu-id="9d53f-133">I adresselinjen i browseren skal du notere URL-adressen for Dataverse-organisationen.</span><span class="sxs-lookup"><span data-stu-id="9d53f-133">In the browser's address bar, make a note of the URL for the Dataverse organization.</span></span> <span data-ttu-id="9d53f-134">URL-adressen kan f. eks være `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="9d53f-134">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

3. <span data-ttu-id="9d53f-135">Hvis du planlægger at bruge funktionen Likviditetsflowbudgetter eller budgetprognoser, skal du følge disse trin for at opdatere din organisations anmærkningsgrænse til mindst 50 MB:</span><span class="sxs-lookup"><span data-stu-id="9d53f-135">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="9d53f-136">Åbn [Power Apps-portalen](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="9d53f-136">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="9d53f-137">Vælg det miljø, du netop har oprettet, og vælg derefter **Avancerede indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-137">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="9d53f-138">Vælg **Indstillinger \> E-mailkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-138">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="9d53f-139">Ret værdien i feltet **Maksimal filstørrelse** til **51.200**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-139">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="9d53f-140">(Værdien er udtrykt i kilobyte \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="9d53f-140">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="9d53f-141">Vælg **OK** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="9d53f-141">Select **OK** to save your changes.</span></span>

## <a name="configure-the-azure-setup"></a><span data-ttu-id="9d53f-142">Konfigurere Azure-opsætning</span><span class="sxs-lookup"><span data-stu-id="9d53f-142">Configure the Azure setup</span></span>

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="9d53f-143">Angiv Dataverse-mappe-id og brugerens Azure AD-objekt-id</span><span class="sxs-lookup"><span data-stu-id="9d53f-143">Enter the Dataverse directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="9d53f-144">Angiv Dataverse-mappe-id:</span><span class="sxs-lookup"><span data-stu-id="9d53f-144">Enter the Dataverse directory ID:</span></span>

    1. <span data-ttu-id="9d53f-145">Åbn [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="9d53f-145">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="9d53f-146">Log på ved hjælp af det bruger-id, der blev brugt til at oprette Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-146">Sign in by using the user ID that was used to create the Dataverse environment.</span></span>
    3. <span data-ttu-id="9d53f-147">Gå til **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-147">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="9d53f-148">Kopier værdien **Lejer-id**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-148">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="9d53f-149">Angiv brugerens Azure Active Directory (Azure AD)-objekt-id:</span><span class="sxs-lookup"><span data-stu-id="9d53f-149">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="9d53f-150">Gå til **Brugere** i [Azure-portal](https://portal.azure.com), og søg efter brugere efter e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="9d53f-150">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="9d53f-151">Brugerens brugerens navn.</span><span class="sxs-lookup"><span data-stu-id="9d53f-151">Select the user's name.</span></span>
    3. <span data-ttu-id="9d53f-152">Kopier værdien i **Objekt-id**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-152">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="9d53f-153">Brug Azure Cloud Shell til at konfigurere Finance Insights Data Lake-ressourcer</span><span class="sxs-lookup"><span data-stu-id="9d53f-153">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="9d53f-154">Brug et Windows PowerShell-script</span><span class="sxs-lookup"><span data-stu-id="9d53f-154">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="9d53f-155">Der er angivet et Windows PowerShell-script, så du nemt kan konfigurere de Azure-ressourcer, der er beskrevet under [Konfigurere eksport til Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span><span class="sxs-lookup"><span data-stu-id="9d53f-155">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md).</span></span> <span data-ttu-id="9d53f-156">Hvis du foretrækker at foretage manuel opsætning, kan du springe denne procedure over og fortsætte med proceduren i afsnittet [Manuel opsætning](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="9d53f-156">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="9d53f-157">Følg nedenstående trin for at køre PowerShell-scriptet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-157">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="9d53f-158">Indstillingen Azure CLI "Try it" eller kørsel af scriptet på din PC fungerer muligvis ikke.</span><span class="sxs-lookup"><span data-stu-id="9d53f-158">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="9d53f-159">Udfør følgende trin for at konfigurere Azure ved hjælp af Windows PowerShell-scriptet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-159">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="9d53f-160">Du skal have rettigheder til at oprette en Azure-ressourcegruppe, Azure-ressourcer og et Azure AD-program.</span><span class="sxs-lookup"><span data-stu-id="9d53f-160">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="9d53f-161">Yderligere oplysninger om de påkrævede tilladelser finder du i [Kontrollér Azure AD-tilladelser](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="9d53f-161">For information about the required permissions, see [Check Azure AD permissions](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="9d53f-162">Gå til dit Azure-abonnement på [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="9d53f-162">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="9d53f-163">Vælg knappen **Cloud Shell** til højre for feltet **Søg**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-163">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="9d53f-164">Vælg **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-164">Select **PowerShell**.</span></span>
3. <span data-ttu-id="9d53f-165">Opret lager, hvis du bliver bedt om det.</span><span class="sxs-lookup"><span data-stu-id="9d53f-165">Create storage if you're prompted to do so.</span></span>
4. <span data-ttu-id="9d53f-166">Gå til fanen **Azure CLI**, og vælg **Kopiér**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-166">Go to the **Azure CLI** tab and select **Copy**.</span></span>  
5. <span data-ttu-id="9d53f-167">Åbn Notesblok, og indsæt PowerShell-scriptet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-167">Open Notepad and paste the PowerShell script.</span></span> <span data-ttu-id="9d53f-168">Gem filen som ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="9d53f-168">Save the file as ConfigureDataLake.ps1.</span></span>
6. <span data-ttu-id="9d53f-169">Overfør Windows PowerShell-scriptet til sessionen ved hjælp af menuindstillingen til overførsel i Cloud Shell.</span><span class="sxs-lookup"><span data-stu-id="9d53f-169">Upload the Windows PowerShell script to the session using the menu option for upload in Cloud Shell.</span></span>
7. <span data-ttu-id="9d53f-170">Kør scriptet .\ConfigureDataLake.ps1.</span><span class="sxs-lookup"><span data-stu-id="9d53f-170">Run the script .\ConfigureDataLake.ps1.</span></span>
8. <span data-ttu-id="9d53f-171">Følg vejledningen for at køre scriptet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-171">Follow the prompts to run the script.</span></span>
9. <span data-ttu-id="9d53f-172">Brug oplysningerne fra scriptoutputtet til at installere tilføjelsesprogrammet **Eksportér til Data Lake** i LCS.</span><span class="sxs-lookup"><span data-stu-id="9d53f-172">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
10. <span data-ttu-id="9d53f-173">Brug oplysningerne fra scriptoutputtet til at aktivere enhedslageret på siden **Dataforbindelser** i Finance (**Systemadministration \> Systemparametre \> Dataforbindelser**).</span><span class="sxs-lookup"><span data-stu-id="9d53f-173">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="9d53f-174">Manuel opsætning</span><span class="sxs-lookup"><span data-stu-id="9d53f-174">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="9d53f-175">Tilføj ansøgninger til Azure AD-lejeren</span><span class="sxs-lookup"><span data-stu-id="9d53f-175">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="9d53f-176">Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="9d53f-176">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="9d53f-177">Vælg **Administrer \> Virksomhedsprogrammer**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-177">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="9d53f-178">Søg efter følgende ansøgninger efter app-id.</span><span class="sxs-lookup"><span data-stu-id="9d53f-178">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="9d53f-179">Applikation</span><span class="sxs-lookup"><span data-stu-id="9d53f-179">Application</span></span>                              | <span data-ttu-id="9d53f-180">App-id</span><span class="sxs-lookup"><span data-stu-id="9d53f-180">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="9d53f-181">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="9d53f-181">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="9d53f-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="9d53f-182">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="9d53f-183">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="9d53f-183">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="9d53f-184">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="9d53f-184">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="9d53f-185">Godkendelsestjeneste til AI Builder</span><span class="sxs-lookup"><span data-stu-id="9d53f-185">AI Builder Authorization Service</span></span>         | <span data-ttu-id="9d53f-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="9d53f-186">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="9d53f-187">Hvis du ikke kan finde de foregående programmer, kan du prøve følgende trin.</span><span class="sxs-lookup"><span data-stu-id="9d53f-187">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="9d53f-188">Vælg menuen **Start** på den lokale computer, og søg efter **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-188">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="9d53f-189">Vælg og hold (eller højreklik) **Windows PowerShell**, og vælg derefter **Kør som administrator**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-189">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="9d53f-190">Kør følgende kommando for at installere modulet **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-190">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="9d53f-191">Hvis der kræves en NuGet-udbyder for at fortsætte, skal du vælge **J** for at installere den.</span><span class="sxs-lookup"><span data-stu-id="9d53f-191">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="9d53f-192">Hvis meddelelsen "Ikke-betroet lager" vises, skal vælge **J** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="9d53f-192">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="9d53f-193">For hvert program, der skal tilføjes, skal du køre følgende kommandoer for at føje programmet til Azure AD.</span><span class="sxs-lookup"><span data-stu-id="9d53f-193">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="9d53f-194">Når du bliver bedt om det, skal du logge på som Azure AD-administrator.</span><span class="sxs-lookup"><span data-stu-id="9d53f-194">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="9d53f-195">Oprette Azure-ressourcer</span><span class="sxs-lookup"><span data-stu-id="9d53f-195">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="9d53f-196">Sørg for at oprette følgende ressourcer i samme Azure AD-forekomst som Dataverse-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-196">Make sure that you create the following resources in the same Azure AD instance as the Dataverse environment.</span></span> <span data-ttu-id="9d53f-197">Du kan ikke bruge ressourcer fra en anden Azure AD-forekomst.</span><span class="sxs-lookup"><span data-stu-id="9d53f-197">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="9d53f-198">Oprette en ny lagerkonto:</span><span class="sxs-lookup"><span data-stu-id="9d53f-198">Create a new storage account:</span></span>

    1. <span data-ttu-id="9d53f-199">Opret en Lagerkonto i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="9d53f-199">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="9d53f-200">Angiv følgende felter i dialogboksen **Opret lagerkonto**:</span><span class="sxs-lookup"><span data-stu-id="9d53f-200">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="9d53f-201">**Placering** - Vælg det datacenter, hvor dit miljø er placeret.</span><span class="sxs-lookup"><span data-stu-id="9d53f-201">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="9d53f-202">**Ydeevne** - Vi anbefaler, at du vælger **Standard**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-202">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="9d53f-203">**Kontotype** - Du skal vælge **Lager V2**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-203">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="9d53f-204">I dialogboksen **Avancerede indstillinger** til indstillingen **Data Lake-lager Gen2** skal du vælge **Aktiver** under funktionen **Hierarkiske navneområder**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-204">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="9d53f-205">Hvis du deaktiverer denne funktion, kan du ikke forbruge data, som Finance and Operations-apps skriver ved hjælp af tjenester som f.eks. Power BI-dataflow.</span><span class="sxs-lookup"><span data-stu-id="9d53f-205">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="9d53f-206">Vælg **Gennemse og opret**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-206">Select **Review and create**.</span></span> <span data-ttu-id="9d53f-207">Når installationen er fuldført, vises den nye ressource på Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="9d53f-207">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="9d53f-208">Gå til den lagerkonto, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-208">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="9d53f-209">Vælg **Adgangsnøgler** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="9d53f-209">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="9d53f-210">Kopiér og gem forbindelsesstrengen for enten **Nøgle 1** eller **Nøgle 2**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-210">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="9d53f-211">Kopiér og gem navnet på lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="9d53f-211">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="9d53f-212">Oprette en ny Key Vault:</span><span class="sxs-lookup"><span data-stu-id="9d53f-212">Create a new key vault:</span></span>

    1. <span data-ttu-id="9d53f-213">Opret en Key Vault i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="9d53f-213">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="9d53f-214">Vælg det datacenter, hvor dit miljø er placeret, i feltet **Placering** i dialogboksen **Opret Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-214">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="9d53f-215">Når du har oprettet en Key Vault, skal du vælge den på listen og derefter vælge **Hemmeligheder**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-215">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="9d53f-216">Vælg **Generer/importer**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-216">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="9d53f-217">I dialogboksen **Opret en hemmelighed** i feltet **Uploadindstillinger** skal du vælge **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-217">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="9d53f-218">Angiv et navn på hemmeligheden.</span><span class="sxs-lookup"><span data-stu-id="9d53f-218">Enter a name for the secret.</span></span> <span data-ttu-id="9d53f-219">Noter navnet, hvis du skal angive det senere.</span><span class="sxs-lookup"><span data-stu-id="9d53f-219">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="9d53f-220">I feltet **Værdi** skal du angive den forbindelsesstreng, du har fået fra lagerkontoen i den foregående procedure.</span><span class="sxs-lookup"><span data-stu-id="9d53f-220">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="9d53f-221">Vælg **Aktiverfet**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-221">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="9d53f-222">Hemmeligheden oprettes og føjes til Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9d53f-222">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="9d53f-223">Gå til **Oversigt over Key Vault**, og noter DNS-navnet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-223">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="9d53f-224">Oprette og registrere en Azure AD-ansøgning:</span><span class="sxs-lookup"><span data-stu-id="9d53f-224">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="9d53f-225">I [Azure-portalen](https://portal.azure.com) skal du gå til **Azure Active Directory**, og derefter vælge **App-registreringer**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-225">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="9d53f-226">Vælg **Ny programregistrering**, og angiv følgende felter:</span><span class="sxs-lookup"><span data-stu-id="9d53f-226">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="9d53f-227">**Navn** - Angiv navnet på appen.</span><span class="sxs-lookup"><span data-stu-id="9d53f-227">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="9d53f-228">**Programtype** - Vælg **Web API**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-228">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="9d53f-229">**Omdirigering af URI-konfiguration** - Angiv URL-adressen til Dynamics 365-forekomsten, f.eks. `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="9d53f-229">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="9d53f-230">Gå til den app, du lige har oprettet, og kopiér og gem værdien **Program-id (klient)**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-230">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="9d53f-231">Du skal angive denne værdi senere, når du konfigurerer Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9d53f-231">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="9d53f-232">Gå til **API-tilladelser**, og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="9d53f-232">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="9d53f-233">Vælg **Tilføj en tilladelse**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-233">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="9d53f-234">Vælg **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-234">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="9d53f-235">Når du har valgt delegerede rettigheder, skal du vælge **bruger\_repræsentation**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-235">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="9d53f-236">Vælg **Tilføj tilladelser**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-236">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="9d53f-237">Vælg **Certifikater \& hemmeligheder** i menuen for appen, og udfør derefter følgende trin for at oprette hemmeligheder for Key Vault:</span><span class="sxs-lookup"><span data-stu-id="9d53f-237">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="9d53f-238">Vælg **Ny klient-hemmelighed**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-238">Select **New client secret**.</span></span>
        2. <span data-ttu-id="9d53f-239">Indtast et navn i feltet **Nøglebeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-239">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="9d53f-240">Vælg en varighed, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-240">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="9d53f-241">Der genereres en hemmelighed i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-241">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="9d53f-242">Kopier og gem den hemmelige værdi.</span><span class="sxs-lookup"><span data-stu-id="9d53f-242">Copy and save the secret value.</span></span>

4. <span data-ttu-id="9d53f-243">Oprette Key Vault-hemmeligheder:</span><span class="sxs-lookup"><span data-stu-id="9d53f-243">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="9d53f-244">Gå til den Key Vault, du har oprettet tidligere, og vælg **Hemmeligheder**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-244">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="9d53f-245">Udfør følgende trin for hvert hemmelige navn i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="9d53f-245">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="9d53f-246">Vælg **Generer/importer**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-246">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="9d53f-247">I dialogboksen **Opret en hemmelighed** i feltet **Uploadindstillinger** skal du vælge **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-247">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="9d53f-248">Opret det hemmelige navn og værdien ud fra følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="9d53f-248">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="9d53f-249">Vælg **Aktiverfet**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-249">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="9d53f-250">Hemmeligheden oprettes og føjes til Key Vault.</span><span class="sxs-lookup"><span data-stu-id="9d53f-250">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="9d53f-251">Hemmeligt navn</span><span class="sxs-lookup"><span data-stu-id="9d53f-251">Secret name</span></span>                       | <span data-ttu-id="9d53f-252">Hemmelig værdi</span><span class="sxs-lookup"><span data-stu-id="9d53f-252">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="9d53f-253">app-id</span><span class="sxs-lookup"><span data-stu-id="9d53f-253">app-id</span></span>                            | <span data-ttu-id="9d53f-254">App-id for det program, du har oprettet tidligere</span><span class="sxs-lookup"><span data-stu-id="9d53f-254">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="9d53f-255">app-hemmelighed</span><span class="sxs-lookup"><span data-stu-id="9d53f-255">app-secret</span></span>                        | <span data-ttu-id="9d53f-256">Den klienthemmelighed, du tidligere har gemt</span><span class="sxs-lookup"><span data-stu-id="9d53f-256">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="9d53f-257">lagerkontonavn</span><span class="sxs-lookup"><span data-stu-id="9d53f-257">storage-account-name</span></span>              | <span data-ttu-id="9d53f-258">Navnet på den lagerkonto, du har oprettet tidligere, f. eks. **lagerkonto1**</span><span class="sxs-lookup"><span data-stu-id="9d53f-258">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="9d53f-259">lagerkontoforbindelsesstreng</span><span class="sxs-lookup"><span data-stu-id="9d53f-259">storage-account-connection-string</span></span> | <span data-ttu-id="9d53f-260">Den forbindelsesstreng, du har kopieret fra siden **Adgangstaster** til lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="9d53f-260">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="9d53f-261">Godkende programmet for at få adgang til Key Vault:</span><span class="sxs-lookup"><span data-stu-id="9d53f-261">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="9d53f-262">I [Azure-portalen](https://portal.azure.com) skal du åbne den Key Vault, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="9d53f-262">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="9d53f-263">Vælg adgangspolitikker.</span><span class="sxs-lookup"><span data-stu-id="9d53f-263">Select the access policies.</span></span>
    3. <span data-ttu-id="9d53f-264">Udfør følgende trin for hvert program i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="9d53f-264">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="9d53f-265">Vælg **Tilføj adgangspolitik** for at oprette en adgangspolitik.</span><span class="sxs-lookup"><span data-stu-id="9d53f-265">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="9d53f-266">I feltet **Hemmelige tilladelser** skal du vælge tilladelser fra følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="9d53f-266">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="9d53f-267">I feltet **Vælg overordnet** skal du søge efter programmets visningsnavn i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="9d53f-267">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="9d53f-268">Vælg **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-268">Select **Select**.</span></span>
        5. <span data-ttu-id="9d53f-269">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-269">Select **Add**.</span></span>
        6. <span data-ttu-id="9d53f-270">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-270">Select **Save**.</span></span>

        | <span data-ttu-id="9d53f-271">Applikation</span><span class="sxs-lookup"><span data-stu-id="9d53f-271">Application</span></span>                                              | <span data-ttu-id="9d53f-272">Rettigheder</span><span class="sxs-lookup"><span data-stu-id="9d53f-272">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="9d53f-273">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="9d53f-273">The display name of the new application that you created</span></span> | <span data-ttu-id="9d53f-274">Hent, Sæt på liste</span><span class="sxs-lookup"><span data-stu-id="9d53f-274">Get, List</span></span>   |
        | <span data-ttu-id="9d53f-275">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="9d53f-275">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="9d53f-276">Hent, Sæt på liste</span><span class="sxs-lookup"><span data-stu-id="9d53f-276">Get, List</span></span>   |

6. <span data-ttu-id="9d53f-277">Tildele roller for at få adgang til lagerkontoen:</span><span class="sxs-lookup"><span data-stu-id="9d53f-277">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="9d53f-278">I [Azure-portalen](https://portal.azure.com) skal du åbne den lagerkonto, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="9d53f-278">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="9d53f-279">Vælg **Adgangskontrol (IAM)**, og vælg derefter **Rolletildelinger**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-279">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="9d53f-280">Vælg **Tilføj, Tilføj rolletildeling**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-280">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="9d53f-281">Udfør følgende trin for hvert program i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="9d53f-281">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="9d53f-282">Vælg rollen fra følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="9d53f-282">Select the role from the following table.</span></span>
        2. <span data-ttu-id="9d53f-283">Forlad feltet **Tildel adgangsrettigheder til**, der er angivet til **Azure AD-bruger, -gruppe eller -tjenesteprincipal**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-283">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="9d53f-284">I feltet **Vælg** skal du angive programmet fra følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="9d53f-284">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="9d53f-285">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-285">Select **Save**.</span></span>

        | <span data-ttu-id="9d53f-286">Applikation</span><span class="sxs-lookup"><span data-stu-id="9d53f-286">Application</span></span>                                              | <span data-ttu-id="9d53f-287">Rolle</span><span class="sxs-lookup"><span data-stu-id="9d53f-287">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="9d53f-288">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="9d53f-288">The display name of the new application that you created</span></span> | <span data-ttu-id="9d53f-289">Ejer</span><span class="sxs-lookup"><span data-stu-id="9d53f-289">Owner</span></span>                       |
        | <span data-ttu-id="9d53f-290">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="9d53f-290">The display name of the new application that you created</span></span> | <span data-ttu-id="9d53f-291">Bidragyder</span><span class="sxs-lookup"><span data-stu-id="9d53f-291">Contributor</span></span>                 |
        | <span data-ttu-id="9d53f-292">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="9d53f-292">The display name of the new application that you created</span></span> | <span data-ttu-id="9d53f-293">Bidragyder til lagerkonto</span><span class="sxs-lookup"><span data-stu-id="9d53f-293">Storage Account Contributor</span></span> |
        | <span data-ttu-id="9d53f-294">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="9d53f-294">The display name of the new application that you created</span></span> | <span data-ttu-id="9d53f-295">Ejer af Blob Data-lager</span><span class="sxs-lookup"><span data-stu-id="9d53f-295">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="9d53f-296">**Godkendelsestjeneste til AI Builder**</span><span class="sxs-lookup"><span data-stu-id="9d53f-296">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="9d53f-297">Læser af Blob Data-lager</span><span class="sxs-lookup"><span data-stu-id="9d53f-297">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="9d53f-298">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="9d53f-298">Azure CLI</span></span>](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a><span data-ttu-id="9d53f-299">Konfigurer Data Lake</span><span class="sxs-lookup"><span data-stu-id="9d53f-299">Configure the data lake</span></span>

<span data-ttu-id="9d53f-300">Udfør følgende trin for at bruge LCS til at tilføje tilføjelsesprogrammet Azure Data Lake til miljøet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-300">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="9d53f-301">Log på LCS, og vælg derefter detaljerede oplysninger under miljønavnet på højre side af siden, vælg **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-301">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="9d53f-302">Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-302">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="9d53f-303">Vælg **Eksporter til Data Lake**-tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-303">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="9d53f-304">Angiv følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="9d53f-304">Enter the following values.</span></span>

    | <span data-ttu-id="9d53f-305">Værdi</span><span class="sxs-lookup"><span data-stu-id="9d53f-305">Value</span></span>                                                              | <span data-ttu-id="9d53f-306">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9d53f-306">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="9d53f-307">Lejer-id på det Azure-abonnement, hvor Key Vault er placeret</span><span class="sxs-lookup"><span data-stu-id="9d53f-307">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="9d53f-308">Det lejer-id, hvor lagerkontoen, apps og Key Vault er placeret.</span><span class="sxs-lookup"><span data-stu-id="9d53f-308">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="9d53f-309">Hvis du vil finde denne værdi, skal åbne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere værdien **Lejer-id**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-309">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="9d53f-310">Angiv DNS-navn for Key Vault</span><span class="sxs-lookup"><span data-stu-id="9d53f-310">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="9d53f-311">DNS-navnet på Key Vault, som f.eks. `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="9d53f-311">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="9d53f-312">(Denne værdi svarer til det DNS-navn, der bruges i enhedslageret).</span><span class="sxs-lookup"><span data-stu-id="9d53f-312">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="9d53f-313">Angiv den hemmelighed, der indeholder navnet på lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="9d53f-313">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="9d53f-314">**lagerkontonavn**</span><span class="sxs-lookup"><span data-stu-id="9d53f-314">**storage-account-name**</span></span> |
    | <span data-ttu-id="9d53f-315">Hemmeligt navn på app-id, der skal bruges til at få adgang til Data Lake</span><span class="sxs-lookup"><span data-stu-id="9d53f-315">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="9d53f-316">**app-id**</span><span class="sxs-lookup"><span data-stu-id="9d53f-316">**app-id**</span></span> |
    | <span data-ttu-id="9d53f-317">Hemmeligt navn, der skal bruges sammen med app-id</span><span class="sxs-lookup"><span data-stu-id="9d53f-317">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="9d53f-318">**app-hemmelighed**</span><span class="sxs-lookup"><span data-stu-id="9d53f-318">**app-secret**</span></span> |

5. <span data-ttu-id="9d53f-319">Accepter betingelserne, og vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-319">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="9d53f-320">Tilføjelsesprogrammet vil blive installeret inden for et par minutter.</span><span class="sxs-lookup"><span data-stu-id="9d53f-320">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="9d53f-321">Konfigurer AI Builder</span><span class="sxs-lookup"><span data-stu-id="9d53f-321">Configure AI Builder</span></span>

1. <span data-ttu-id="9d53f-322">Log på LCS, og åbn siden **Miljøoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-322">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="9d53f-323">Rul til sektionen **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-323">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="9d53f-324">Du bør kunne se de tilføjelsesprogrammer, der allerede er installeret i dette miljø.</span><span class="sxs-lookup"><span data-stu-id="9d53f-324">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="9d53f-325">Hvis tilføjelsesprogrammet **Eksporter til Data Lake** ikke er angivet, skal du konfigurere dette tilføjelsesprogram.</span><span class="sxs-lookup"><span data-stu-id="9d53f-325">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="9d53f-326">Vælg tilføjelsesprogrammet **Hent Insights**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-326">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="9d53f-327">Angiv følgende værdier på siden med tilføjelsesprogrammet **Hent Insights**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-327">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="9d53f-328">Værdi</span><span class="sxs-lookup"><span data-stu-id="9d53f-328">Value</span></span>                                                    | <span data-ttu-id="9d53f-329">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="9d53f-329">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="9d53f-330">CDS URL-adresse til organisation</span><span class="sxs-lookup"><span data-stu-id="9d53f-330">CDS Organization URL</span></span>                                     | <span data-ttu-id="9d53f-331">Dataverse-organisationens URL-adresse, der blev kopieret ovenfor.</span><span class="sxs-lookup"><span data-stu-id="9d53f-331">The Dataverse organization URL copied from above.</span></span> |
    | <span data-ttu-id="9d53f-332">CDS Org-id</span><span class="sxs-lookup"><span data-stu-id="9d53f-332">CDS Org ID</span></span>                                               | <span data-ttu-id="9d53f-333">Dataverse-organisationens id, der blev kopieret ovenfor.</span><span class="sxs-lookup"><span data-stu-id="9d53f-333">The Dataverse organization ID copied from above.</span></span> |
5. <span data-ttu-id="9d53f-334">Aktivér **Er dette standardmiljøet for din lejer**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-334">Enable **Is this the default environment for you Tenant**.</span></span>
    
## <a name="configure-the-entity-store"></a><span data-ttu-id="9d53f-335">Konfigurer enhedslager</span><span class="sxs-lookup"><span data-stu-id="9d53f-335">Configure the entity store</span></span>

<span data-ttu-id="9d53f-336">Udfør følgende trin for at konfigurere enhedslageret i Finance-miljøet.</span><span class="sxs-lookup"><span data-stu-id="9d53f-336">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="9d53f-337">Gå til **Systemadministration \> Opsætning \> Systemparametre \> Dataforbindelser**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-337">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="9d53f-338">Indstil følgende Key Vault-felter:</span><span class="sxs-lookup"><span data-stu-id="9d53f-338">Set the following key vault fields:</span></span>

    - <span data-ttu-id="9d53f-339">**Program-id (klient)** - Angiv det programklient-id, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="9d53f-339">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="9d53f-340">**Programhemmelighed** - Angiv den hemmelighed, du har gemt for det program, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="9d53f-340">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="9d53f-341">**DNS-navn** - Find DNS-navnet (Domain Name System) på siden Programdetaljer for det program, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="9d53f-341">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="9d53f-342">**Hemmeligt navn** - Angiv **lager-konto-forbindelsesstreng**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-342">**Secret name** – Enter **storage-account-connection-string**.</span></span>
3. <span data-ttu-id="9d53f-343">Aktivér **Aktivér Data Lake-integration**.</span><span class="sxs-lookup"><span data-stu-id="9d53f-343">Enable **Enable Data Lake integration**.</span></span>
4. <span data-ttu-id="9d53f-344">Vælg **Test Azure Key Vault**, og kontrollér, at der ikke er nogen fejl.</span><span class="sxs-lookup"><span data-stu-id="9d53f-344">Select **Test Azure Key Vault** and verify there are no errors.</span></span>
5. <span data-ttu-id="9d53f-345">Vælg **Test Azure-lager**, og kontrollér, at der ikke er nogen fejl.</span><span class="sxs-lookup"><span data-stu-id="9d53f-345">Select **Test Azure storage** and verify there are no errors.</span></span>

## <a name="feedback-and-support"></a><span data-ttu-id="9d53f-346">Feedback og support</span><span class="sxs-lookup"><span data-stu-id="9d53f-346">Feedback and support</span></span>

<span data-ttu-id="9d53f-347">Send en e-mail til [Indsigt i debitorbetaling (prøveversion)](mailto:fiap@microsoft.com), hvis du er interesseret i at give feedback eller har brug for support.</span><span class="sxs-lookup"><span data-stu-id="9d53f-347">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="9d53f-348">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="9d53f-348">Privacy notice</span></span>

<span data-ttu-id="9d53f-349">Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="9d53f-349">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
