---
title: Konfiguration til Finance Insights (prøveversion)
description: I dette emne beskrives de konfigurationstrin, der sætter systemet i gang med at bruge de egenskaber, der er tilgængelige i Finance Insights.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/25/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14151
ms.assetid: 3d43ba40-780c-459a-a66f-9a01d556e674
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2020-07-20
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 38cdeb9110691e594b4b90fc5bc79e369c9f4707
ms.sourcegitcommit: 1cfd6e0c808341b0f5bafbde7d04b0255b27352f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/02/2020
ms.locfileid: "4664084"
---
# <a name="configuration-for-finance-insights-preview"></a><span data-ttu-id="f277e-103">Konfiguration til Finance Insights (prøveversion)</span><span class="sxs-lookup"><span data-stu-id="f277e-103">Configuration for Finance insights (preview)</span></span>

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="f277e-104">Finance Insights kombinerer funktionalitet fra Microsoft Dynamics 365 Finance sammen med Common Data Service, Azure og AI Builder for at levere effektive prognoseværktøjer til din organisation.</span><span class="sxs-lookup"><span data-stu-id="f277e-104">Finance insights combines functionality from Microsoft Dynamics 365 Finance with Common Data Service, Azure, and AI Builder to provide powerful forecasting tools for your organization.</span></span> <span data-ttu-id="f277e-105">I dette emne beskrives de konfigurationstrin, der sætter systemet i gang med at bruge de egenskaber, der er tilgængelige i Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="f277e-105">This topic explains the configuration steps that will enable your system to use the capabilities that are available in Finance insights.</span></span>

## <a name="deploy-dynamics-365-finance"></a><span data-ttu-id="f277e-106">Installér Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="f277e-106">Deploy Dynamics 365 Finance</span></span>

<span data-ttu-id="f277e-107">Følg disse trin for at installere miljøerne.</span><span class="sxs-lookup"><span data-stu-id="f277e-107">Deploy the environments by following these steps.</span></span>

1. <span data-ttu-id="f277e-108">I Microsoft Dynamics Lifecycle Services (LCS) skal du oprette eller opdatere et Dynamics 365 Finance-miljø.</span><span class="sxs-lookup"><span data-stu-id="f277e-108">In Microsoft Dynamics Lifecycle Services (LCS), create or update a Dynamics 365 Finance environment.</span></span> <span data-ttu-id="f277e-109">Miljøet kræver programversion 10.0.11/Platformopdatering 35 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="f277e-109">The environment requires app version 10.0.11/Platform update 35 or later.</span></span>
2. <span data-ttu-id="f277e-110">Miljøet skal være et miljø med høj tilgængelighed (HA) i sandkassesystemet.</span><span class="sxs-lookup"><span data-stu-id="f277e-110">The environment must be a high-availability (HA) environment in Sandbox.</span></span> <span data-ttu-id="f277e-111">(Denne type miljø kaldes også et Niveau-2-miljø). Du kan finde flere oplysninger i [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span><span class="sxs-lookup"><span data-stu-id="f277e-111">(This type of environment is also known as a Tier-2 environment.) For more information, see [Environment planning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).</span></span>
3. <span data-ttu-id="f277e-112">Hvis du bruger Contoso-demodata, skal du bruge yderligere eksempeldata for at kunne bruge debitorbetalingsforudsigelser, likviditetsbudgetter og budgetprognosefunktioner.</span><span class="sxs-lookup"><span data-stu-id="f277e-112">If you're using Contoso demo data, you will require additional sample data to use the Customer payment predictions, Cash flow forecasts, and Budget forecasts features.</span></span> 

## <a name="configure-common-data-service"></a><span data-ttu-id="f277e-113">Konfigurer Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f277e-113">Configure Common Data Service</span></span>

<span data-ttu-id="f277e-114">Du kan fuldføre de manuelle konfigurationstrin, der følger, eller du kan gøre konfigurationsprocessen hurtigere ved at bruge det Windows PowerShell-script, der angives.</span><span class="sxs-lookup"><span data-stu-id="f277e-114">You can complete the manual configuration steps that follow, or you can speed up the configuration process by using the Windows PowerShell script that is provided.</span></span> <span data-ttu-id="f277e-115">Når PowerShell-scriptet er afsluttet, får du vist værdier, der skal bruges til at konfigurere Finance Insights.</span><span class="sxs-lookup"><span data-stu-id="f277e-115">When the PowerShell script has finished running, it will give you values to use to configure Finance insights.</span></span> 

> [!NOTE]
> <span data-ttu-id="f277e-116">Åbn PowerShell på din PC for at køre scriptet.</span><span class="sxs-lookup"><span data-stu-id="f277e-116">Open PowerShell on your PC to run the script.</span></span> <span data-ttu-id="f277e-117">Du skal muligvis bruge PowerShell version 5.</span><span class="sxs-lookup"><span data-stu-id="f277e-117">You may need PowerShell version 5.</span></span> <span data-ttu-id="f277e-118">Microsoft Azure CLI "Try it" virker muligvis ikke.</span><span class="sxs-lookup"><span data-stu-id="f277e-118">The Microsoft Azure CLI "Try it" option may not work.</span></span>

# <a name="manual-configuration-steps"></a>[<span data-ttu-id="f277e-119">Manuelle konfigurationstrin</span><span class="sxs-lookup"><span data-stu-id="f277e-119">Manual configuration steps</span></span>](#tab/configuration-steps)

1. <span data-ttu-id="f277e-120">Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com/), og udfør følgende trin for at oprette et nyt Common Data Service-miljø i samme Active Directory-lejer:</span><span class="sxs-lookup"><span data-stu-id="f277e-120">Open the [Power Platform admin center](https://admin.powerplatform.microsoft.com/), and follow these steps to create a new Common Data Service environment in the same Active Directory tenant:</span></span>

    1. <span data-ttu-id="f277e-121">Åbn siden **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="f277e-121">Open the **Environments** page.</span></span>

        <span data-ttu-id="f277e-122">Siden [![Miljøer](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span><span class="sxs-lookup"><span data-stu-id="f277e-122">[![Environments page](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)</span></span>

    2. <span data-ttu-id="f277e-123">Vælg **Nyt miljø**.</span><span class="sxs-lookup"><span data-stu-id="f277e-123">Select **New environment**.</span></span>
    3. <span data-ttu-id="f277e-124">I feltet **Type** skal du vælge **Sandkasse**.</span><span class="sxs-lookup"><span data-stu-id="f277e-124">In the **Type** field, select **Sandbox**.</span></span>
    4. <span data-ttu-id="f277e-125">Angiv indstillingen **Opret database** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f277e-125">Set the **Create Database** option to **Yes**.</span></span>
    5. <span data-ttu-id="f277e-126">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="f277e-126">Select **Next**.</span></span>
    6. <span data-ttu-id="f277e-127">Vælg sprog og valuta for organisationen.</span><span class="sxs-lookup"><span data-stu-id="f277e-127">Select the language and currency for your organization.</span></span>
    7. <span data-ttu-id="f277e-128">Accepter standardværdierne for de andre felter.</span><span class="sxs-lookup"><span data-stu-id="f277e-128">Accept the default values for the other fields.</span></span>
    8. <span data-ttu-id="f277e-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f277e-129">Select **Save**.</span></span>
    9. <span data-ttu-id="f277e-130">Opdatér siden **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="f277e-130">Refresh the **Environments** page.</span></span>
    10. <span data-ttu-id="f277e-131">Vent, indtil værdien i **Status** opdateres til **Klar**.</span><span class="sxs-lookup"><span data-stu-id="f277e-131">Wait until the value of the **State** field is updated to **Ready**.</span></span>
    11. <span data-ttu-id="f277e-132">Notér dig Common Data Service-organisations-id.</span><span class="sxs-lookup"><span data-stu-id="f277e-132">Make a note of the Common Data Service organization ID.</span></span>
    12. <span data-ttu-id="f277e-133">Vælg miljøet, og vælg derefter **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f277e-133">Select the environment, and then select **Settings**.</span></span>
    13. <span data-ttu-id="f277e-134">Vælg **Ressourcer \> Alle tidligere indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f277e-134">Select **Resources \> All Legacy Settings**.</span></span>
    14. <span data-ttu-id="f277e-135">Vælg indstillinger på den øverste navigationslinje **Indstillinger**, og vælg derefter **Tilpasninger**.</span><span class="sxs-lookup"><span data-stu-id="f277e-135">On the top navigation bar, select **Settings**, and then select **Customizations**.</span></span>
    15. <span data-ttu-id="f277e-136">Vælg **Udviklerressourcer**.</span><span class="sxs-lookup"><span data-stu-id="f277e-136">Select **Developer Resources**.</span></span>
    16. <span data-ttu-id="f277e-137">Indstil feltet **Forekomstreferenceoplysninger-id** til den Common Data Service-organisations-id, som du noterede tidligere.</span><span class="sxs-lookup"><span data-stu-id="f277e-137">Set the **Instance Reference Information ID** field to the Common Data Service organization ID value that you made a note of earlier.</span></span>
    17. <span data-ttu-id="f277e-138">I adresselinjen i browseren skal du notere URL-adressen for Common Data Service-organisationen.</span><span class="sxs-lookup"><span data-stu-id="f277e-138">In the browser's address bar, make a note of the URL for the Common Data Service organization.</span></span> <span data-ttu-id="f277e-139">URL-adressen kan f. eks være `https://org42b2b3d3.crm.dynamics.com`.</span><span class="sxs-lookup"><span data-stu-id="f277e-139">For example, the URL might be `https://org42b2b3d3.crm.dynamics.com`.</span></span>

2. <span data-ttu-id="f277e-140">Hvis du planlægger at bruge funktionen Likviditetsflowbudgetter eller budgetprognoser, skal du følge disse trin for at opdatere din organisations anmærkningsgrænse til mindst 50 MB:</span><span class="sxs-lookup"><span data-stu-id="f277e-140">If you plan to use the Cash flow forecasts or Budget forecasts feature, follow these steps to update the annotation limit for your organization to at least 50 megabytes (MB):</span></span>

    1. <span data-ttu-id="f277e-141">Åbn [Power Apps-portalen](https://make.powerapps.com).</span><span class="sxs-lookup"><span data-stu-id="f277e-141">Open the [Power Apps portal](https://make.powerapps.com).</span></span>
    2. <span data-ttu-id="f277e-142">Vælg det miljø, du netop har oprettet, og vælg derefter **Avancerede indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="f277e-142">Select the environment that you just created, and then select **Advanced settings**.</span></span>
    3. <span data-ttu-id="f277e-143">Vælg **Indstillinger \> E-mailkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f277e-143">Select **Settings \> Email Configuration**.</span></span>
    4. <span data-ttu-id="f277e-144">Ret værdien i feltet **Maksimal filstørrelse** til **51.200**.</span><span class="sxs-lookup"><span data-stu-id="f277e-144">Change the value of the **Maximum file size** field to **51,200**.</span></span> <span data-ttu-id="f277e-145">(Værdien er udtrykt i kilobyte \[KB\].)</span><span class="sxs-lookup"><span data-stu-id="f277e-145">(The value is expressed in kilobytes \[KB\].)</span></span>
    5. <span data-ttu-id="f277e-146">Vælg **OK** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="f277e-146">Select **OK** to save your changes.</span></span>

# <a name="windows-powershell-configuration-script"></a>[<span data-ttu-id="f277e-147">Windows PowerShell-konfigurationsscript</span><span class="sxs-lookup"><span data-stu-id="f277e-147">Windows PowerShell configuration script</span></span>](#tab/powershell-configuration-script)

```azurecli-interactive
Write-Output 'The following modules need to be present for execution of this script:'
Write-Output '  Microsoft.PowerApps.Administration.PowerShell'
Write-Output '  Microsoft.PowerApps.PowerShell'
Write-Output '  Microsoft.Xrm.Tooling.CrmConnector.PowerShell'

try {
    $moduleConsent = Read-Host 'Is it ok to install or update these modules as needed? (yes/no)'
    if ($moduleConsent -ne 'yes' -and $moduleConsent -ne 'y') {
        Write-Warning 'User declined to install required modules.'
        return
    }

    $module = 'Microsoft.PowerApps.Administration.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '2.0.61' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '2.0.61' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.PowerApps.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '1.0.9' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '1.0.9' -AllowClobber -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    $module = 'Microsoft.Xrm.Tooling.CrmConnector.PowerShell'
    if (-not (Get-InstalledModule -Name $module -MinimumVersion '3.3.0.892' -ErrorAction SilentlyContinue)) {
        Install-Module -Name $module -MinimumVersion '3.3.0.892' -Force
        Write-Output ('Installed {0} module.' -f $module)
    }
    else {
        Write-Output ('{0} module found.' -f $module)
    }

    Write-Output '================================================================================='

    $useMfa = $false
    $useMfaPrompt = Read-Host "Does your organization require the use of multi-factor authentication? (yes/no)"
    if ($useMfaPrompt -eq 'yes' -or $useMfaPrompt -eq 'y') {
        $useMfa = $true
    }
    if(-not $useMfa) {
        $credential = Get-Credential -Message 'Power Apps Credential'
    }

    $orgFriendlyName = Read-Host "Enter the name of the CDS Organization to use or create: (blank for 'FinanceInsightsOrg')"
    if ($orgFriendlyName.Trim() -eq '') {
        $orgFriendlyName = 'FinanceInsightsOrg'
    }

    $isDefaultOrgPrompt = Read-Host ("Is '" + $orgFriendlyName + "' the default organization for your tenant? (yes/no)")
    if ($isDefaultOrgPrompt -eq 'yes' -or $isDefaultOrgPrompt -eq 'y') {
        $isDefaultOrg = $true
    }

    if ($credential) {
        Add-PowerAppsAccount -Username $credential.UserName -Password $credential.Password
    }
    else {
        Add-PowerAppsAccount
    }

    if ($isDefaultOrg) {
        $orgMatch = ('(default)')
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { $_.IsDefault -eq $true })
    }
    else {
        $orgMatch = ('{0} (*)' -f $orgFriendlyName)
        $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.IsDefault -eq $false -and ($_.DisplayName -eq $orgFriendlyName -or $_.DisplayName -like $orgMatch)) })
    }

    $getCrmOrgParams = @{ 'OnlineType' = 'Office365' }
    if ($credential) {
        $getCrmOrgParams.Credential = $credential
    }

    if ($null -eq $environment) {
        Write-Output '================================================================================='
        Write-Output 'PowerApps environment not found. A new one will be provisioned.'

        $invalid = 'invalid'

        $location = $invalid
        $cdsLocations = (Get-AdminPowerAppEnvironmentLocations | Select-Object LocationName).LocationName
        while (-not ($location -in $cdsLocations)) {
            $location = (Read-Host -Prompt "Enter the location in which to create the new PowerApps environment: ('help' to see values)")
            if ($location -eq 'help') {
                $cdsLocations
            }
        }

        $currency = $invalid
        $cdsCurrencies = (Get-AdminPowerAppCdsDatabaseCurrencies -Location $location | Select-Object CurrencyName).CurrencyName
        while ($currency -ne '' -and -not ($currency -in $cdsCurrencies)) {
            $currency = (Read-Host -Prompt "Enter the currency to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($currency -eq 'help') {
                $cdsCurrencies
            }
        }

        $language = $invalid
        $cdsLanguages = (Get-AdminPowerAppCdsDatabaseLanguages -Location $location | Select-Object LanguageName, LanguageDisplayName)
        while ($language -ne '' -and -not ($language -in $cdsLanguages.LanguageName)) {
            $language = (Read-Host -Prompt "Enter the language name to use for the new PowerApps environment: ('help' to see values, blank for default)")
            if ($language -eq 'help') {
                $cdsLanguages | Format-Table -Property LanguageName, LanguageDisplayName
            }
        }

        Write-Output 'Provisioning PowerApps environment. This may take several minutes.'

        $sleep = 15

        $envParams = @{ 'DisplayName' = $orgFriendlyName; 'EnvironmentSku' = 'Sandbox'; 'ProvisionDatabase' = $true; 'Location' = $location; 'WaitUntilFinished' = $true }
        if ($language.Trim() -ne '') {
            $envParams.LanguageName = $language
        }
        if ($currency.Trim() -ne '') {
            $envParams.CurrencyName = $currency
        }
        $newEnvResult = New-AdminPowerAppEnvironment @envParams
        if (($null -eq $newEnvResult) -or ($newEnvResult.CommonDataServiceDatabaseProvisioningState -ne 'Succeeded')) {
            Write-Warning 'Failed to create to PowerApps environment'
            if ($null -ne $newEnvResult) {
                $newEnvResult
            }
        }
        else {
            $environment = $null
            $retryCount = 0
            while (($null -eq $environment) -and ($retryCount -lt 5)) {
                Start-Sleep -Seconds $sleep
                $environment = (Get-AdminPowerAppEnvironment | Where-Object { ($_.DisplayName -like $orgMatch) })
            }
            Write-Output ("Provisioned PowerApps environment with name: '" + $environment.DisplayName + "'")
        }

        Write-Output 'Waiting for CDS organization provisioning. This may take several minutes.'
        if (-not $credential) {
            $sleep = 120
            Write-Output 'You may be prompted for credentials multiple times while checking the status of the provisioning.'
        }

        while ($null -eq $crmOrg) {
            Start-Sleep -Seconds $sleep
            $crmOrg = (Get-CrmOrganizations @getCrmOrgParams) | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }
    else {
        $crmOrgs = Get-CrmOrganizations @getCrmOrgParams
        if ($UseDefaultOrganization -eq $true) {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -match $orgMatch }
        }
        else {
            $crmOrg = $crmOrgs | Where-Object { $_.FriendlyName -eq $orgFriendlyName }
        }
    }

    Write-Output '================================================================================='
    Write-Output 'Values for PowerAI LCS Add-In:'
    Write-Output ("  CDS organization url:             " + $crmOrg.WebApplicationUrl)
    Write-Output ("  CDS organization ID:              " + $crmOrg.OrganizationId)
}
catch {
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $_.Exception.InnerException
    while ($null -ne $inner) {
        Write-Output 'Inner Exception:'
        Write-Error $_.Exception.Message
        Write-Warning $_.Exception.StackTrace
        $inner = $inner.InnerException
    }
}
```
---

## <a name="configure-the-azure-setup"></a><span data-ttu-id="f277e-148">Konfigurere Azure-opsætning</span><span class="sxs-lookup"><span data-stu-id="f277e-148">Configure the Azure setup</span></span>

### <a name="enter-the-common-data-service-directory-id-and-the-users-azure-ad-object-id"></a><span data-ttu-id="f277e-149">Angiv Common Data Service-mappe-id og brugerens Azure AD-objekt-id</span><span class="sxs-lookup"><span data-stu-id="f277e-149">Enter the Common Data Service directory ID and the user's Azure AD object ID</span></span>

1. <span data-ttu-id="f277e-150">Angiv Common Data Service-mappe-id:</span><span class="sxs-lookup"><span data-stu-id="f277e-150">Enter the Common Data Service directory ID:</span></span>

    1. <span data-ttu-id="f277e-151">Åbn [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f277e-151">Open the [Azure portal](https://portal.azure.com).</span></span>
    2. <span data-ttu-id="f277e-152">Log på ved hjælp af det bruger-id, der blev brugt til at oprette Common Data Service-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f277e-152">Sign in by using the user ID that was used to create the Common Data Service environment.</span></span>
    3. <span data-ttu-id="f277e-153">Gå til **Azure Active Directory**.</span><span class="sxs-lookup"><span data-stu-id="f277e-153">Go to **Azure Active Directory**.</span></span>
    4. <span data-ttu-id="f277e-154">Kopier værdien **Lejer-id**.</span><span class="sxs-lookup"><span data-stu-id="f277e-154">Copy the **Tenant ID** value.</span></span>

2. <span data-ttu-id="f277e-155">Angiv brugerens Azure Active Directory (Azure AD)-objekt-id:</span><span class="sxs-lookup"><span data-stu-id="f277e-155">Enter the user's Azure Active Directory (Azure AD) object ID:</span></span>

    1. <span data-ttu-id="f277e-156">Gå til **Brugere** i [Azure-portal](https://portal.azure.com), og søg efter brugere efter e-mailadresse.</span><span class="sxs-lookup"><span data-stu-id="f277e-156">In the [Azure portal](https://portal.azure.com), go to **Users**, and search for the user by email address.</span></span>
    2. <span data-ttu-id="f277e-157">Brugerens brugerens navn.</span><span class="sxs-lookup"><span data-stu-id="f277e-157">Select the user's name.</span></span>
    3. <span data-ttu-id="f277e-158">Kopier værdien i **Objekt-id**.</span><span class="sxs-lookup"><span data-stu-id="f277e-158">Copy the **Object ID** value.</span></span>

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a><span data-ttu-id="f277e-159">Brug Azure Cloud Shell til at konfigurere Finance Insights Data Lake-ressourcer</span><span class="sxs-lookup"><span data-stu-id="f277e-159">Use Azure Cloud Shell to set up Finance insights Data Lake resources</span></span>

# <a name="use-a-windows-powershell-script"></a>[<span data-ttu-id="f277e-160">Brug et Windows PowerShell-script</span><span class="sxs-lookup"><span data-stu-id="f277e-160">Use a Windows PowerShell script</span></span>](#tab/use-a-powershell-script)

<span data-ttu-id="f277e-161">Der er angivet et Windows PowerShell-script, så du nemt kan konfigurere de Azure-ressourcer, der er beskrevet under [Konfigurere eksport til Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span><span class="sxs-lookup"><span data-stu-id="f277e-161">A Windows PowerShell script has been provided, so that you can easily set up the Azure resources that are described in [Configure export to Azure Data Lake](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/data-entities/configure-export-data-lake).</span></span> <span data-ttu-id="f277e-162">Hvis du foretrækker at foretage manuel opsætning, kan du springe denne procedure over og fortsætte med proceduren i afsnittet [Manuel opsætning](#manual-setup).</span><span class="sxs-lookup"><span data-stu-id="f277e-162">If you prefer to do manual setup, skip this procedure, and continue with the procedure in the [Manual setup](#manual-setup) section.</span></span>

> [!NOTE]
> <span data-ttu-id="f277e-163">Følg nedenstående trin for at køre PowerShell-scriptet.</span><span class="sxs-lookup"><span data-stu-id="f277e-163">Follow the steps below to run the PowerShell script.</span></span> <span data-ttu-id="f277e-164">Indstillingen Azure CLI "Try it" eller kørsel af scriptet på din PC fungerer muligvis ikke.</span><span class="sxs-lookup"><span data-stu-id="f277e-164">The Azure CLI "Try it" option, or running the script on your PC may not work.</span></span>

<span data-ttu-id="f277e-165">Udfør følgende trin for at konfigurere Azure ved hjælp af Windows PowerShell-scriptet.</span><span class="sxs-lookup"><span data-stu-id="f277e-165">Follow these steps to configure Azure by using the Windows PowerShell script.</span></span> <span data-ttu-id="f277e-166">Du skal have rettigheder til at oprette en Azure-ressourcegruppe, Azure-ressourcer og et Azure AD-program.</span><span class="sxs-lookup"><span data-stu-id="f277e-166">You must have rights to create an Azure resource group, Azure resources, and an Azure AD application.</span></span> <span data-ttu-id="f277e-167">Yderligere oplysninger om de påkrævede tilladelser finder du i [Kontrollér Azure AD-tilladelser](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span><span class="sxs-lookup"><span data-stu-id="f277e-167">For information about the required permissions, see [Check Azure AD permissions](https://docs.microsoft.com/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).</span></span>

1. <span data-ttu-id="f277e-168">Gå til dit Azure-abonnement på [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f277e-168">In the [Azure portal](https://portal.azure.com), go to your target Azure subscription.</span></span> <span data-ttu-id="f277e-169">Vælg knappen **Cloud Shell** til højre for feltet **Søg**.</span><span class="sxs-lookup"><span data-stu-id="f277e-169">Select the **Cloud Shell** button to the right of the **Search** field.</span></span>
2. <span data-ttu-id="f277e-170">Vælg **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="f277e-170">Select **PowerShell**.</span></span>
3. <span data-ttu-id="f277e-171">Opret lager, hvis du bliver bedt om det.</span><span class="sxs-lookup"><span data-stu-id="f277e-171">Create storage, if you're prompted to do so.</span></span> <span data-ttu-id="f277e-172">Overfør derefter Windows PowerShell-scriptet til sessionen.</span><span class="sxs-lookup"><span data-stu-id="f277e-172">Then upload the Windows PowerShell script to the session.</span></span>
4. <span data-ttu-id="f277e-173">Køre scriptet.</span><span class="sxs-lookup"><span data-stu-id="f277e-173">Run the script.</span></span>
5. <span data-ttu-id="f277e-174">Følg vejledningen for at køre scriptet.</span><span class="sxs-lookup"><span data-stu-id="f277e-174">Follow the prompts to run the script.</span></span>
6. <span data-ttu-id="f277e-175">Brug oplysningerne fra scriptoutputtet til at installere tilføjelsesprogrammet **Eksportér til Data Lake** i LCS.</span><span class="sxs-lookup"><span data-stu-id="f277e-175">Use the information from the script output to install the **Export to Data Lake** add-in in LCS.</span></span>
7. <span data-ttu-id="f277e-176">Brug oplysningerne fra scriptoutputtet til at aktivere enhedslageret på siden **Dataforbindelser** i Finance (**Systemadministration \> Systemparametre \> Dataforbindelser**).</span><span class="sxs-lookup"><span data-stu-id="f277e-176">Use the information from the script output to enable the entity store on the **Data connections** page in Finance (**System administration \> System parameters \> Data connections**).</span></span>

### <a name="manual-setup"></a><span data-ttu-id="f277e-177">Manuel opsætning</span><span class="sxs-lookup"><span data-stu-id="f277e-177">Manual setup</span></span>

#### <a name="add-applications-to-the-azure-ad-tenant"></a><span data-ttu-id="f277e-178">Tilføj ansøgninger til Azure AD-lejeren</span><span class="sxs-lookup"><span data-stu-id="f277e-178">Add applications to the Azure AD tenant</span></span>

1. <span data-ttu-id="f277e-179">Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f277e-179">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**.</span></span>
2. <span data-ttu-id="f277e-180">Vælg **Administrer \> Virksomhedsprogrammer**.</span><span class="sxs-lookup"><span data-stu-id="f277e-180">Select **Manage \> Enterprise applications**.</span></span>
3. <span data-ttu-id="f277e-181">Søg efter følgende ansøgninger efter app-id.</span><span class="sxs-lookup"><span data-stu-id="f277e-181">Search for the following applications by app ID.</span></span>

    | <span data-ttu-id="f277e-182">Applikation</span><span class="sxs-lookup"><span data-stu-id="f277e-182">Application</span></span>                              | <span data-ttu-id="f277e-183">App-id</span><span class="sxs-lookup"><span data-stu-id="f277e-183">App ID</span></span>                               |
    |------------------------------------------|--------------------------------------|
    | <span data-ttu-id="f277e-184">Microsoft Dynamics ERP Microservices</span><span class="sxs-lookup"><span data-stu-id="f277e-184">Microsoft Dynamics ERP Microservices</span></span>     | <span data-ttu-id="f277e-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span><span class="sxs-lookup"><span data-stu-id="f277e-185">0cdb527f-a8d1-4bf8-9436-b352c68682b2</span></span> |
    | <span data-ttu-id="f277e-186">Microsoft Dynamics ERP Microservices CDS</span><span class="sxs-lookup"><span data-stu-id="f277e-186">Microsoft Dynamics ERP Microservices CDS</span></span> | <span data-ttu-id="f277e-187">703e2651-d3fc-48f5-942c-74274233dba8</span><span class="sxs-lookup"><span data-stu-id="f277e-187">703e2651-d3fc-48f5-942c-74274233dba8</span></span> |
    | <span data-ttu-id="f277e-188">Godkendelsestjeneste til AI Builder</span><span class="sxs-lookup"><span data-stu-id="f277e-188">AI Builder Authorization Service</span></span>         | <span data-ttu-id="f277e-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span><span class="sxs-lookup"><span data-stu-id="f277e-189">ad40333e-9910-4b61-b281-e3aeeb8c3ef3</span></span> |

<span data-ttu-id="f277e-190">Hvis du ikke kan finde de foregående programmer, kan du prøve følgende trin.</span><span class="sxs-lookup"><span data-stu-id="f277e-190">If you can't find any of the preceding applications, try the following steps.</span></span>

1. <span data-ttu-id="f277e-191">Vælg menuen **Start** på den lokale computer, og søg efter **PowerShell**.</span><span class="sxs-lookup"><span data-stu-id="f277e-191">On your local machine, select the **Start** menu, and search for **powershell**.</span></span>
2. <span data-ttu-id="f277e-192">Vælg og hold (eller højreklik) **Windows PowerShell**, og vælg derefter **Kør som administrator**.</span><span class="sxs-lookup"><span data-stu-id="f277e-192">Select and hold (or right-click) **Windows PowerShell**, and then select **Run as administrator**.</span></span>
3. <span data-ttu-id="f277e-193">Kør følgende kommando for at installere modulet **AzureAD**.</span><span class="sxs-lookup"><span data-stu-id="f277e-193">Run the following command to install the **AzureAD** module.</span></span>

    `Install-Module -Name AzureAD`

4. <span data-ttu-id="f277e-194">Hvis der kræves en NuGet-udbyder for at fortsætte, skal du vælge **J** for at installere den.</span><span class="sxs-lookup"><span data-stu-id="f277e-194">If a NuGet provider is required to continue, select **Y** to install it.</span></span>
5. <span data-ttu-id="f277e-195">Hvis meddelelsen "Ikke-betroet lager" vises, skal vælge **J** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="f277e-195">If an "Untrusted repository" message appears, select **Y** to continue.</span></span>
6. <span data-ttu-id="f277e-196">For hvert program, der skal tilføjes, skal du køre følgende kommandoer for at føje programmet til Azure AD.</span><span class="sxs-lookup"><span data-stu-id="f277e-196">For each application that must be added, run the following commands to add the application to Azure AD.</span></span> <span data-ttu-id="f277e-197">Når du bliver bedt om det, skal du logge på som Azure AD-administrator.</span><span class="sxs-lookup"><span data-stu-id="f277e-197">When you're prompted, sign in as the Azure AD administrator.</span></span>

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a><span data-ttu-id="f277e-198">Oprette Azure-ressourcer</span><span class="sxs-lookup"><span data-stu-id="f277e-198">Create Azure resources</span></span>

> [!NOTE]
> <span data-ttu-id="f277e-199">Sørg for at oprette følgende ressourcer i samme Azure AD-forekomst som Common Data Service-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f277e-199">Make sure that you create the following resources in the same Azure AD instance as the Common Data Service environment.</span></span> <span data-ttu-id="f277e-200">Du kan ikke bruge ressourcer fra en anden Azure AD-forekomst.</span><span class="sxs-lookup"><span data-stu-id="f277e-200">You can't use resources from a different Azure AD instance.</span></span>

1. <span data-ttu-id="f277e-201">Oprette en ny lagerkonto:</span><span class="sxs-lookup"><span data-stu-id="f277e-201">Create a new storage account:</span></span>

    1. <span data-ttu-id="f277e-202">Opret en Lagerkonto i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f277e-202">In the [Azure portal](https://portal.azure.com), create a storage account.</span></span>
    2. <span data-ttu-id="f277e-203">Angiv følgende felter i dialogboksen **Opret lagerkonto**:</span><span class="sxs-lookup"><span data-stu-id="f277e-203">In the **Create storage account** dialog box, set the following fields:</span></span>

        - <span data-ttu-id="f277e-204">**Placering** - Vælg det datacenter, hvor dit miljø er placeret.</span><span class="sxs-lookup"><span data-stu-id="f277e-204">**Location** – Select the data center where your environment is located.</span></span>
        - <span data-ttu-id="f277e-205">**Ydeevne** - Vi anbefaler, at du vælger **Standard**.</span><span class="sxs-lookup"><span data-stu-id="f277e-205">**Performance** – We recommend that you select **Standard**.</span></span>
        - <span data-ttu-id="f277e-206">**Kontotype** - Du skal vælge **Lager V2**.</span><span class="sxs-lookup"><span data-stu-id="f277e-206">**Account kind** – You must select **StorageV2**.</span></span>

    3. <span data-ttu-id="f277e-207">I dialogboksen **Avancerede indstillinger** til indstillingen **Data Lake-lager Gen2** skal du vælge **Aktiver** under funktionen **Hierarkiske navneområder**.</span><span class="sxs-lookup"><span data-stu-id="f277e-207">In the **Advanced options** dialog box, for the **Data Lake storage Gen2** option, select **Enable** under the **Hierarchical namespaces** feature.</span></span> <span data-ttu-id="f277e-208">Hvis du deaktiverer denne funktion, kan du ikke forbruge data, som Finance and Operations-apps skriver ved hjælp af tjenester som f.eks. Power BI-dataflow.</span><span class="sxs-lookup"><span data-stu-id="f277e-208">If you disable this feature, you can't consume data that Finance and Operations apps write by using services such as Power BI data flows.</span></span>
    4. <span data-ttu-id="f277e-209">Vælg **Gennemse og opret**.</span><span class="sxs-lookup"><span data-stu-id="f277e-209">Select **Review and create**.</span></span> <span data-ttu-id="f277e-210">Når installationen er fuldført, vises den nye ressource på Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="f277e-210">When the deployment is completed, the new resource will be shown in the Azure portal.</span></span>
    5. <span data-ttu-id="f277e-211">Gå til den lagerkonto, du har oprettet.</span><span class="sxs-lookup"><span data-stu-id="f277e-211">Go to the storage account that you created.</span></span>
    6. <span data-ttu-id="f277e-212">Vælg **Adgangsnøgler** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="f277e-212">On the left menu, select **Access keys**.</span></span>
    7. <span data-ttu-id="f277e-213">Kopiér og gem forbindelsesstrengen for enten **Nøgle 1** eller **Nøgle 2**.</span><span class="sxs-lookup"><span data-stu-id="f277e-213">Copy and save the connection string for either **Key1** or **Key2**.</span></span>
    8. <span data-ttu-id="f277e-214">Kopiér og gem navnet på lagerkontoen.</span><span class="sxs-lookup"><span data-stu-id="f277e-214">Copy and save the storage account name.</span></span>

2. <span data-ttu-id="f277e-215">Oprette en ny Key Vault:</span><span class="sxs-lookup"><span data-stu-id="f277e-215">Create a new key vault:</span></span>

    1. <span data-ttu-id="f277e-216">Opret en Key Vault i [Azure-portalen](https://portal.azure.com).</span><span class="sxs-lookup"><span data-stu-id="f277e-216">In the [Azure portal](https://portal.azure.com), create a key vault.</span></span>
    2. <span data-ttu-id="f277e-217">Vælg det datacenter, hvor dit miljø er placeret, i feltet **Placering** i dialogboksen **Opret Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="f277e-217">In the **Create key vault** dialog box, in the **Location** field, select the data center where your environment is located.</span></span>
    3. <span data-ttu-id="f277e-218">Når du har oprettet en Key Vault, skal du vælge den på listen og derefter vælge **Hemmeligheder**.</span><span class="sxs-lookup"><span data-stu-id="f277e-218">After key vault is created, select it in the list, and then select **Secrets**.</span></span>
    4. <span data-ttu-id="f277e-219">Vælg **Generer/importer**.</span><span class="sxs-lookup"><span data-stu-id="f277e-219">Select **Generate/Import**.</span></span>
    5. <span data-ttu-id="f277e-220">I dialogboksen **Opret en hemmelighed** i feltet **Uploadindstillinger** skal du vælge **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="f277e-220">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
    6. <span data-ttu-id="f277e-221">Angiv et navn på hemmeligheden.</span><span class="sxs-lookup"><span data-stu-id="f277e-221">Enter a name for the secret.</span></span> <span data-ttu-id="f277e-222">Noter navnet, hvis du skal angive det senere.</span><span class="sxs-lookup"><span data-stu-id="f277e-222">Make a note of the name, because you will have to provide it later.</span></span>
    7. <span data-ttu-id="f277e-223">I feltet **Værdi** skal du angive den forbindelsesstreng, du har fået fra lagerkontoen i den foregående procedure.</span><span class="sxs-lookup"><span data-stu-id="f277e-223">In the **Value** field, enter the connection string that you obtained from the storage account in the previous procedure.</span></span>
    8. <span data-ttu-id="f277e-224">Vælg **Aktiverfet**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="f277e-224">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="f277e-225">Hemmeligheden oprettes og føjes til Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f277e-225">The secret is created and added to Key Vault.</span></span>
    9. <span data-ttu-id="f277e-226">Gå til **Oversigt over Key Vault**, og noter DNS-navnet.</span><span class="sxs-lookup"><span data-stu-id="f277e-226">Go to the **Key Vault Overview**, and make a note of the DNS name.</span></span>

3. <span data-ttu-id="f277e-227">Oprette og registrere en Azure AD-ansøgning:</span><span class="sxs-lookup"><span data-stu-id="f277e-227">Create and register an Azure AD application:</span></span>

    1. <span data-ttu-id="f277e-228">I [Azure-portalen](https://portal.azure.com) skal du gå til **Azure Active Directory**, og derefter vælge **App-registreringer**.</span><span class="sxs-lookup"><span data-stu-id="f277e-228">In the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and then select **App registrations**.</span></span>
    2. <span data-ttu-id="f277e-229">Vælg **Ny programregistrering**, og angiv følgende felter:</span><span class="sxs-lookup"><span data-stu-id="f277e-229">Select **New application registration**, and set the following fields:</span></span>

        - <span data-ttu-id="f277e-230">**Navn** - Angiv navnet på appen.</span><span class="sxs-lookup"><span data-stu-id="f277e-230">**Name** – Enter the name of the app.</span></span>
        - <span data-ttu-id="f277e-231">**Programtype** - Vælg **Web API**.</span><span class="sxs-lookup"><span data-stu-id="f277e-231">**Application type** – Select **Web API**.</span></span>
        - <span data-ttu-id="f277e-232">**Omdirigering af URI-konfiguration** - Angiv URL-adressen til Dynamics 365-forekomsten, f.eks. `https://yourdynamicsinstance.dynamics.com/auth`.</span><span class="sxs-lookup"><span data-stu-id="f277e-232">**Redirect URI setup** – Enter the URL for your Dynamics 365 instance, such as, `https://yourdynamicsinstance.dynamics.com/auth`.</span></span>

    3. <span data-ttu-id="f277e-233">Gå til den app, du lige har oprettet, og kopiér og gem værdien **Program-id (klient)**.</span><span class="sxs-lookup"><span data-stu-id="f277e-233">Go to the app that you just created, and copy and save its **Application (client) ID** value.</span></span> <span data-ttu-id="f277e-234">Du skal angive denne værdi senere, når du konfigurerer Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f277e-234">You will have to provide this value later, when you set up the key vault.</span></span>
    4. <span data-ttu-id="f277e-235">Gå til **API-tilladelser**, og udfør følgende trin:</span><span class="sxs-lookup"><span data-stu-id="f277e-235">Go to **API permissions**, and follow these steps:</span></span>

        1. <span data-ttu-id="f277e-236">Vælg **Tilføj en tilladelse**.</span><span class="sxs-lookup"><span data-stu-id="f277e-236">Select **Add a permission**.</span></span>
        2. <span data-ttu-id="f277e-237">Vælg **Azure Key Vault**.</span><span class="sxs-lookup"><span data-stu-id="f277e-237">Select **Azure Key vault**.</span></span>
        3. <span data-ttu-id="f277e-238">Når du har valgt delegerede rettigheder, skal du vælge **bruger\_repræsentation**.</span><span class="sxs-lookup"><span data-stu-id="f277e-238">After you select delegated permissions, select **user\_impersonation**.</span></span>
        4. <span data-ttu-id="f277e-239">Vælg **Tilføj tilladelser**.</span><span class="sxs-lookup"><span data-stu-id="f277e-239">Select **Add permissions**.</span></span>

    5. <span data-ttu-id="f277e-240">Vælg **Certifikater \& hemmeligheder** i menuen for appen, og udfør derefter følgende trin for at oprette hemmeligheder for Key Vault:</span><span class="sxs-lookup"><span data-stu-id="f277e-240">On the menu for the app, select **Certificates \& secrets**, and then follow these steps to create Key Vault secrets:</span></span>

        1. <span data-ttu-id="f277e-241">Vælg **Ny klient-hemmelighed**.</span><span class="sxs-lookup"><span data-stu-id="f277e-241">Select **New client secret**.</span></span>
        2. <span data-ttu-id="f277e-242">Indtast et navn i feltet **Nøglebeskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="f277e-242">In the **Key Description** field, enter a name.</span></span>
        3. <span data-ttu-id="f277e-243">Vælg en varighed, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="f277e-243">Select a duration, and then select **Add**.</span></span> <span data-ttu-id="f277e-244">Der genereres en hemmelighed i feltet **Værdi**.</span><span class="sxs-lookup"><span data-stu-id="f277e-244">A secret is generated in the **Value** field.</span></span>
        4. <span data-ttu-id="f277e-245">Kopier og gem den hemmelige værdi.</span><span class="sxs-lookup"><span data-stu-id="f277e-245">Copy and save the secret value.</span></span>

4. <span data-ttu-id="f277e-246">Oprette Key Vault-hemmeligheder:</span><span class="sxs-lookup"><span data-stu-id="f277e-246">Create Key Vault secrets:</span></span>

    1. <span data-ttu-id="f277e-247">Gå til den Key Vault, du har oprettet tidligere, og vælg **Hemmeligheder**.</span><span class="sxs-lookup"><span data-stu-id="f277e-247">Go to the key vault that you created earlier, and select **Secrets**.</span></span>
    2. <span data-ttu-id="f277e-248">Udfør følgende trin for hvert hemmelige navn i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="f277e-248">For each secret name in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f277e-249">Vælg **Generer/importer**.</span><span class="sxs-lookup"><span data-stu-id="f277e-249">Select **Generate/Import**.</span></span>
        2. <span data-ttu-id="f277e-250">I dialogboksen **Opret en hemmelighed** i feltet **Uploadindstillinger** skal du vælge **Manuel**.</span><span class="sxs-lookup"><span data-stu-id="f277e-250">In the **Create a secret** dialog box, in the **Upload options** field, select **Manual**.</span></span>
        3. <span data-ttu-id="f277e-251">Opret det hemmelige navn og værdien ud fra følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f277e-251">Create the secret name and value from the following table.</span></span>
        4. <span data-ttu-id="f277e-252">Vælg **Aktiverfet**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="f277e-252">Select **Enabled**, and then select **Create**.</span></span> <span data-ttu-id="f277e-253">Hemmeligheden oprettes og føjes til Key Vault.</span><span class="sxs-lookup"><span data-stu-id="f277e-253">The secret is created and added to Key Vault.</span></span>

        | <span data-ttu-id="f277e-254">Hemmeligt navn</span><span class="sxs-lookup"><span data-stu-id="f277e-254">Secret name</span></span>                       | <span data-ttu-id="f277e-255">Hemmelig værdi</span><span class="sxs-lookup"><span data-stu-id="f277e-255">Secret value</span></span>                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | <span data-ttu-id="f277e-256">app-id</span><span class="sxs-lookup"><span data-stu-id="f277e-256">app-id</span></span>                            | <span data-ttu-id="f277e-257">App-id for det program, du har oprettet tidligere</span><span class="sxs-lookup"><span data-stu-id="f277e-257">The app ID of the application that you created earlier</span></span>                                      |
        | <span data-ttu-id="f277e-258">app-hemmelighed</span><span class="sxs-lookup"><span data-stu-id="f277e-258">app-secret</span></span>                        | <span data-ttu-id="f277e-259">Den klienthemmelighed, du tidligere har gemt</span><span class="sxs-lookup"><span data-stu-id="f277e-259">The client secret that you saved earlier</span></span>                                                    |
        | <span data-ttu-id="f277e-260">lagerkontonavn</span><span class="sxs-lookup"><span data-stu-id="f277e-260">storage-account-name</span></span>              | <span data-ttu-id="f277e-261">Navnet på den lagerkonto, du har oprettet tidligere, f. eks. **lagerkonto1**</span><span class="sxs-lookup"><span data-stu-id="f277e-261">The name of the storage account that you created earlier, such as **storageaccount1**</span></span>       |
        | <span data-ttu-id="f277e-262">lagerkontoforbindelsesstreng</span><span class="sxs-lookup"><span data-stu-id="f277e-262">storage-account-connection-string</span></span> | <span data-ttu-id="f277e-263">Den forbindelsesstreng, du har kopieret fra siden **Adgangstaster** til lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="f277e-263">The connection string that you copied from the **Access keys** page for the storage account</span></span> |

5. <span data-ttu-id="f277e-264">Godkende programmet for at få adgang til Key Vault:</span><span class="sxs-lookup"><span data-stu-id="f277e-264">Authorize the application to access the key vault:</span></span>

    1. <span data-ttu-id="f277e-265">I [Azure-portalen](https://portal.azure.com) skal du åbne den Key Vault, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="f277e-265">In the [Azure portal](https://portal.azure.com), open the key vault that you created earlier.</span></span>
    2. <span data-ttu-id="f277e-266">Vælg adgangspolitikker.</span><span class="sxs-lookup"><span data-stu-id="f277e-266">Select the access policies.</span></span>
    3. <span data-ttu-id="f277e-267">Udfør følgende trin for hvert program i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="f277e-267">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f277e-268">Vælg **Tilføj adgangspolitik** for at oprette en adgangspolitik.</span><span class="sxs-lookup"><span data-stu-id="f277e-268">Select **Add Access Policy** to create an access policy.</span></span>
        2. <span data-ttu-id="f277e-269">I feltet **Hemmelige tilladelser** skal du vælge tilladelser fra følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f277e-269">In the **Secret permissions** field, select the permissions from the following table.</span></span>
        3. <span data-ttu-id="f277e-270">I feltet **Vælg overordnet** skal du søge efter programmets visningsnavn i følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f277e-270">In the **Select principal** field, search for the application display name from the following table.</span></span>
        4. <span data-ttu-id="f277e-271">Vælg **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="f277e-271">Select **Select**.</span></span>
        5. <span data-ttu-id="f277e-272">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="f277e-272">Select **Add**.</span></span>
        6. <span data-ttu-id="f277e-273">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f277e-273">Select **Save**.</span></span>

        | <span data-ttu-id="f277e-274">Applikation</span><span class="sxs-lookup"><span data-stu-id="f277e-274">Application</span></span>                                              | <span data-ttu-id="f277e-275">Rettigheder</span><span class="sxs-lookup"><span data-stu-id="f277e-275">Permissions</span></span> |
        |----------------------------------------------------------|-------------|
        | <span data-ttu-id="f277e-276">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="f277e-276">The display name of the new application that you created</span></span> | <span data-ttu-id="f277e-277">Hent, Sæt på liste</span><span class="sxs-lookup"><span data-stu-id="f277e-277">Get, List</span></span>   |
        | <span data-ttu-id="f277e-278">**Microsoft Dynamics ERP Microservices**</span><span class="sxs-lookup"><span data-stu-id="f277e-278">**Microsoft Dynamics ERP Microservices**</span></span>                 | <span data-ttu-id="f277e-279">Hent, Sæt på liste</span><span class="sxs-lookup"><span data-stu-id="f277e-279">Get, List</span></span>   |

6. <span data-ttu-id="f277e-280">Tildele roller for at få adgang til lagerkontoen:</span><span class="sxs-lookup"><span data-stu-id="f277e-280">Assign roles to access the storage account:</span></span>

    1. <span data-ttu-id="f277e-281">I [Azure-portalen](https://portal.azure.com) skal du åbne den lagerkonto, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="f277e-281">In the [Azure portal](https://portal.azure.com), open the storage account that you created earlier.</span></span>
    2. <span data-ttu-id="f277e-282">Vælg **Adgangskontrol (IAM)**, og vælg derefter **Rolletildelinger**.</span><span class="sxs-lookup"><span data-stu-id="f277e-282">Select **Access Control (IAM)**, and then select **Role Assignments**.</span></span>
    3. <span data-ttu-id="f277e-283">Vælg **Tilføj, Tilføj rolletildeling**.</span><span class="sxs-lookup"><span data-stu-id="f277e-283">Select **Add, Add Role Assignment**.</span></span>
    4. <span data-ttu-id="f277e-284">Udfør følgende trin for hvert program i følgende tabel:</span><span class="sxs-lookup"><span data-stu-id="f277e-284">For each application in the following table, follow these steps:</span></span>

        1. <span data-ttu-id="f277e-285">Vælg rollen fra følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f277e-285">Select the role from the following table.</span></span>
        2. <span data-ttu-id="f277e-286">Forlad feltet **Tildel adgangsrettigheder til**, der er angivet til **Azure AD-bruger, -gruppe eller -tjenesteprincipal**.</span><span class="sxs-lookup"><span data-stu-id="f277e-286">Leave the **Assign access to** field set to **Azure AD user, group, or service principal**.</span></span>
        3. <span data-ttu-id="f277e-287">I feltet **Vælg** skal du angive programmet fra følgende tabel.</span><span class="sxs-lookup"><span data-stu-id="f277e-287">In the **Select** field, enter the application from the following table.</span></span>
        4. <span data-ttu-id="f277e-288">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f277e-288">Select **Save**.</span></span>

        | <span data-ttu-id="f277e-289">Applikation</span><span class="sxs-lookup"><span data-stu-id="f277e-289">Application</span></span>                                              | <span data-ttu-id="f277e-290">Rolle</span><span class="sxs-lookup"><span data-stu-id="f277e-290">Role</span></span>                        |
        |----------------------------------------------------------|-----------------------------|
        | <span data-ttu-id="f277e-291">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="f277e-291">The display name of the new application that you created</span></span> | <span data-ttu-id="f277e-292">Ejer</span><span class="sxs-lookup"><span data-stu-id="f277e-292">Owner</span></span>                       |
        | <span data-ttu-id="f277e-293">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="f277e-293">The display name of the new application that you created</span></span> | <span data-ttu-id="f277e-294">Bidragyder</span><span class="sxs-lookup"><span data-stu-id="f277e-294">Contributor</span></span>                 |
        | <span data-ttu-id="f277e-295">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="f277e-295">The display name of the new application that you created</span></span> | <span data-ttu-id="f277e-296">Bidragyder til lagerkonto</span><span class="sxs-lookup"><span data-stu-id="f277e-296">Storage Account Contributor</span></span> |
        | <span data-ttu-id="f277e-297">Visningsnavnet for den nye program, du har oprettet</span><span class="sxs-lookup"><span data-stu-id="f277e-297">The display name of the new application that you created</span></span> | <span data-ttu-id="f277e-298">Ejer af Blob Data-lager</span><span class="sxs-lookup"><span data-stu-id="f277e-298">Storage Blob Data Owner</span></span>     |
        | <span data-ttu-id="f277e-299">**Godkendelsestjeneste til AI Builder**</span><span class="sxs-lookup"><span data-stu-id="f277e-299">**AI Builder Authorization Service**</span></span>                     | <span data-ttu-id="f277e-300">Læser af Blob Data-lager</span><span class="sxs-lookup"><span data-stu-id="f277e-300">Storage Blob Data Reader</span></span>    |

# <a name="azure-cli"></a>[<span data-ttu-id="f277e-301">Azure CLI</span><span class="sxs-lookup"><span data-stu-id="f277e-301">Azure CLI</span></span>](#tab/azure-azure-cli)

```
function New-FinanceDataLakeAzureResources {
    $defaultSecretExpiryInYear = 1

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

    $subscriptionId = (Read-Host -Prompt "Enter the Azure Subscription ID: (blank for default)")
    if ($subscriptionId.Trim() -ne '') {
        $azSubscription = Select-AzSubscription -SubscriptionId $subscriptionId
    }

    $resourceGroupName = (Read-Host -Prompt "Enter the Azure Resource Group name: (blank for 'FinanceDataLake')")
    if ($null -eq $resourceGroupName -or $resourceGroupName.Trim() -eq '') {
        $resourceGroupName = 'FinanceDataLake'
    }
    $resourceGroup = Get-AzResourceGroup -Name $resourceGroupName -ErrorAction SilentlyContinue

    if (-not ($resourceGroup)) {
        $resourceLocation = ''
        $azResourceLocations = (Get-AzLocation | Select-Object Location).Location
        while ($resourceLocation.Trim() -eq '' -or (-not ($resourceLocation -in $azResourceLocations))) {
            $resourceLocation = (Read-Host -Prompt "Enter the location in which to create the Azure Resource Group: ('help' to see values)")
            if ($resourceLocation -eq 'help') {
                $azResourceLocations
                $resourceLocation = ''
            }
        }
        $resourceGroup = New-AzResourceGroup -Name $resourceGroupName -Location $resourceLocation
    }
    else {
        $resourceLocation = $resourceGroup.Location
    }

    $clientAppName = (Read-Host -Prompt "Enter the name of the application registration: (blank for 'Finance Data Lake Application')")
    if ($clientAppName.Trim() -eq '') {
        $clientAppName = 'Finance Data Lake Application'
    }

    Write-Output '================================================================================='

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesAppId)
    }
    $MicrosoftDynamicsERPMicroservicesAppObjectId = $service.ObjectId

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $MicrosoftDynamicsERPMicroservicesCDSAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $MicrosoftDynamicsERPMicroservicesCDSAppId | Format-Table -AutoSize
        Write-Output ("Added AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'Microsoft Dynamics ERP Microservices CDS' with Application ID {0}" -f $MicrosoftDynamicsERPMicroservicesCDSAppId)
    }

    $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
    if (-not $service) {
        New-AzureADServicePrincipal -AppId $AIBuilderAuthorizationServiceAppId | Format-Table -AutoSize
        $service = Get-AzureADServicePrincipal -Filter ("AppId eq '" + $AIBuilderAuthorizationServiceAppId + "'")
        Write-Output ("Added AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    else {
        Write-Output ("Found AAD Enterprise Application 'AI Builder Authorization Service' with Application ID {0}" -f $AIBuilderAuthorizationServiceAppId)
    }
    $aibuilderAuthorizationServiceObjectId = $service.ObjectId

    Write-Output '================================================================================='

    $clientAppSPN = Get-AzureADServicePrincipal -Filter ("DisplayName eq '" + $clientAppName + "'")
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

        $clientApp = New-AzureADApplication -DisplayName $clientAppName -RequiredResourceAccess @($keyVaultAccess, $graphAccess)
        $clientAppSPN = New-AzureADServicePrincipal -AppId $clientApp.AppId -Tags @($clientAppName)
        $clientAppId = $clientApp.AppId
        Write-Output ('Created App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
    else {
        $clientApp = Get-AzureADApplication -Filter ("DisplayName eq '" + $clientAppName + "'")
        $clientAppId = $clientApp.AppId
        Write-Output ('Found App Registration "' + $clientAppName + '" with Application Id: ' + $clientAppId)
    }
            
    $clientAppSecretCredential = New-AzureADApplicationPasswordCredential -ObjectId $clientApp.ObjectId -CustomKeyIdentifier "ClientAppAccessKey" -EndDate (get-date).AddYears($defaultSecretExpiryInYear)
    $ClientAppSecret = $clientAppSecretCredential.Value
    $clientAppSpId = $clientAppSPN.ObjectId

    Write-Output ('Generated application secret: ' + $ClientAppSecret)
    Write-Output '================================================================================='

    $templateObject = ConvertFrom-Json $azureTemplate -AsHashtable
    $templateObject.{$schema} = "https://schema.management.azure.com/schemas/2019-04-01/deploymentTemplate.json#"
    Write-Output 'Provisioning Azure resources. This may take a few minutes.'
    $deployment = New-AzResourceGroupDeployment -ResourceGroupName $resourceGroupName -TemplateObject $templateObject -aibuilderAppObjectId $aibuilderAuthorizationServiceObjectId -clientAppId $clientAppId -clientAppSecret $ClientAppSecret -clientAppSpObjectId  $clientAppSpId -microserviceSpObjectId $MicrosoftDynamicsERPMicroservicesAppObjectId -userSpObjectId $user.ObjectId

    if ($deployment.ProvisioningState -eq 'Succeeded') {
        Write-Output "Successfully deployed the following resources to Azure:"
        Write-Output ("  Key Vault:                         " + $deployment.Outputs.keyVaultName.Value)
        Write-Output ("  Storage Account:                   " + $deployment.Outputs.storageAccountName.Value)
    }
    else {
        Write-Output ("Provisioning Azure resources failed with the following state: " + $deployment.ProvisioningState)
        Write-Output ("Some of the resources may have been created in resource group: " + $resourceGroupName)
    }

    Write-Output '================================================================================='

    $keyVault = Get-AzKeyVault -VaultName $deployment.Outputs.keyVaultName.Value
    Write-Output "Values for LCS Data Lake Add-In:"
    Write-Output ("  Tenant ID:                         " + $subscriptionContext.Context.Subscription.TenantId)
    Write-Output ("  DNS Name:                          " + $keyVault.VaultUri)
    Write-Output "  Storage account secret name:       storage-account-name"
    Write-Output "  Application ID secret name:        app-id"
    Write-Output "  Application Secret secret name:    app-secret"
    Write-Warning "Copy this information for the LCS Add-in as it is not saved. Azure Cloud Shell will eventually time out and close."

    Write-Output '================================================================================='
    Write-Output "Values for System parameters > Data connections:"
    Write-Output ("  Application ID:                    " + $clientAppId)
    Write-Output ("  Application Secret:                " + $ClientAppSecret)
    Write-Output ("  DNS name:                          " + $keyVault.VaultUri)
    Write-Output "  Secret name:                       storage-account-connection-string"
    Write-Warning "Copy this information for the System parameters as it is not saved. Azure Cloud Shell will eventually time out and close."
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
  New-FinanceDataLakeAzureResources
}
catch {
  Write-Error $_.Exception.Message
  Write-Warning $_.Exception.StackTrace
  $inner = $_.Exception.InnerException
  while ($null -ne $inner) {
    Write-Output 'Inner Exception:'
    Write-Error $_.Exception.Message
    Write-Warning $_.Exception.StackTrace
    $inner = $inner.InnerException
  }
}

```
---

## <a name="configure-the-entity-store"></a><span data-ttu-id="f277e-302">Konfigurer enhedslager</span><span class="sxs-lookup"><span data-stu-id="f277e-302">Configure the entity store</span></span>

<span data-ttu-id="f277e-303">Udfør følgende trin for at konfigurere enhedslageret i Finance-miljøet.</span><span class="sxs-lookup"><span data-stu-id="f277e-303">Follow these steps to set up the entity store in your Finance environment.</span></span>

1. <span data-ttu-id="f277e-304">Gå til **Systemadministration \> Opsætning \> Systemparametre \> Dataforbindelser**.</span><span class="sxs-lookup"><span data-stu-id="f277e-304">Go to **System administration \> Setup \> System parameters \> Data connections**.</span></span>
2. <span data-ttu-id="f277e-305">Indstil **Aktivér Data Lake-integration** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="f277e-305">Set the **Enable Data Lake integration** option to **Yes**.</span></span>
3. <span data-ttu-id="f277e-306">Indstille følgende Key Vault-felter:</span><span class="sxs-lookup"><span data-stu-id="f277e-306">Set the following Key Vault fields:</span></span>

    - <span data-ttu-id="f277e-307">**Program-id (klient)** - Angiv det programklient-id, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="f277e-307">**Application (client) ID** – Enter the application client ID that you created earlier.</span></span>
    - <span data-ttu-id="f277e-308">**Programhemmelighed** - Angiv den hemmelighed, du har gemt for det program, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="f277e-308">**Application Secret** – Enter the secret that you saved for the application that you created earlier.</span></span>
    - <span data-ttu-id="f277e-309">**DNS-navn** - Find DNS-navnet (Domain Name System) på siden Programdetaljer for det program, du har oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="f277e-309">**DNS name** – You can find the Domain Name System (DNS) name on the application details page for the application that you created earlier.</span></span>
    - <span data-ttu-id="f277e-310">**Hemmeligt navn** - Angiv **lager-konto-forbindelsesstreng**.</span><span class="sxs-lookup"><span data-stu-id="f277e-310">**Secret name** – Enter **storage-account-connection-string**.</span></span>

## <a name="configure-the-data-lake"></a><span data-ttu-id="f277e-311">Konfigurer Data Lake</span><span class="sxs-lookup"><span data-stu-id="f277e-311">Configure the data lake</span></span>

<span data-ttu-id="f277e-312">Udfør følgende trin for at bruge LCS til at tilføje tilføjelsesprogrammet Azure Data Lake til miljøet.</span><span class="sxs-lookup"><span data-stu-id="f277e-312">Follow these steps to use LCS to add the Azure Data Lake add-in to the environment.</span></span>

1. <span data-ttu-id="f277e-313">Log på LCS, og vælg derefter detaljerede oplysninger under miljønavnet på højre side af siden, vælg **Alle detaljer**.</span><span class="sxs-lookup"><span data-stu-id="f277e-313">Sign in to LCS, and then, under the environment name on the right side of the page, select **Full Details**.</span></span>
2. <span data-ttu-id="f277e-314">Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="f277e-314">In the **Environment add-ins** section, select **Install a new add-in**.</span></span>
3. <span data-ttu-id="f277e-315">Vælg **Eksporter til Data Lake**-tilføjelsesprogrammet.</span><span class="sxs-lookup"><span data-stu-id="f277e-315">Select the **Export to Data Lake** add-in.</span></span>
4. <span data-ttu-id="f277e-316">Angiv følgende værdier.</span><span class="sxs-lookup"><span data-stu-id="f277e-316">Enter the following values.</span></span>

    | <span data-ttu-id="f277e-317">Værdi</span><span class="sxs-lookup"><span data-stu-id="f277e-317">Value</span></span>                                                              | <span data-ttu-id="f277e-318">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="f277e-318">Description</span></span> |
    |--------------------------------------------------------------------|-------------|
    | <span data-ttu-id="f277e-319">Lejer-id på det Azure-abonnement, hvor Key Vault er placeret</span><span class="sxs-lookup"><span data-stu-id="f277e-319">Tenant ID of the Azure Subscription where the Key Vault is located</span></span> | <span data-ttu-id="f277e-320">Det lejer-id, hvor lagerkontoen, apps og Key Vault er placeret.</span><span class="sxs-lookup"><span data-stu-id="f277e-320">The tenant ID where the storage account, apps, and key vaults are located.</span></span> <span data-ttu-id="f277e-321">Hvis du vil finde denne værdi, skal åbne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere værdien **Lejer-id**.</span><span class="sxs-lookup"><span data-stu-id="f277e-321">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="f277e-322">Angiv DNS-navn for Key Vault</span><span class="sxs-lookup"><span data-stu-id="f277e-322">Provide the DNS name of your Key Vault</span></span>                             | <span data-ttu-id="f277e-323">DNS-navnet på Key Vault, som f.eks. `https://customkeyvault.vault.azure.net/`.</span><span class="sxs-lookup"><span data-stu-id="f277e-323">The DNS name of the key vault, such as `https://customkeyvault.vault.azure.net/`.</span></span> <span data-ttu-id="f277e-324">(Denne værdi svarer til det DNS-navn, der bruges i enhedslageret).</span><span class="sxs-lookup"><span data-stu-id="f277e-324">(This value matches the DNS name that is used in the entity store.)</span></span> |
    | <span data-ttu-id="f277e-325">Angiv den hemmelighed, der indeholder navnet på lagerkontoen</span><span class="sxs-lookup"><span data-stu-id="f277e-325">Provide the secret that contains the name of the storage account</span></span>   | <span data-ttu-id="f277e-326">**lagerkontonavn**</span><span class="sxs-lookup"><span data-stu-id="f277e-326">**storage-account-name**</span></span> |
    | <span data-ttu-id="f277e-327">Hemmeligt navn på app-id, der skal bruges til at få adgang til Data Lake</span><span class="sxs-lookup"><span data-stu-id="f277e-327">Secret Name for App ID to be used for accessing Data Lake</span></span>          | <span data-ttu-id="f277e-328">**app-id**</span><span class="sxs-lookup"><span data-stu-id="f277e-328">**app-id**</span></span> |
    | <span data-ttu-id="f277e-329">Hemmeligt navn, der skal bruges sammen med app-id</span><span class="sxs-lookup"><span data-stu-id="f277e-329">Secret name to be used with App ID</span></span>                                 | <span data-ttu-id="f277e-330">**app-hemmelighed**</span><span class="sxs-lookup"><span data-stu-id="f277e-330">**app-secret**</span></span> |

5. <span data-ttu-id="f277e-331">Accepter betingelserne, og vælg **Installer**.</span><span class="sxs-lookup"><span data-stu-id="f277e-331">Agree to the terms, and select **Install**.</span></span>

<span data-ttu-id="f277e-332">Tilføjelsesprogrammet vil blive installeret inden for et par minutter.</span><span class="sxs-lookup"><span data-stu-id="f277e-332">The add-in will be installed within a few minutes.</span></span>

## <a name="configure-ai-builder"></a><span data-ttu-id="f277e-333">Konfigurer AI Builder</span><span class="sxs-lookup"><span data-stu-id="f277e-333">Configure AI Builder</span></span>

1. <span data-ttu-id="f277e-334">Log på LCS, og åbn siden **Miljøoplysninger**.</span><span class="sxs-lookup"><span data-stu-id="f277e-334">Sign in to LCS, and open the **Environment details** page.</span></span>
2. <span data-ttu-id="f277e-335">Rul til sektionen **Tilføjelsesprogrammer for miljø**.</span><span class="sxs-lookup"><span data-stu-id="f277e-335">Scroll to the **Environment add-ins** section.</span></span> <span data-ttu-id="f277e-336">Du bør kunne se de tilføjelsesprogrammer, der allerede er installeret i dette miljø.</span><span class="sxs-lookup"><span data-stu-id="f277e-336">You should see the add-ins that are already installed in this environment.</span></span> <span data-ttu-id="f277e-337">Hvis tilføjelsesprogrammet **Eksporter til Data Lake** ikke er angivet, skal du konfigurere dette tilføjelsesprogram.</span><span class="sxs-lookup"><span data-stu-id="f277e-337">If the **Export to Data Lake** add-in isn't among them, configure this add-in.</span></span>
3. <span data-ttu-id="f277e-338">Vælg tilføjelsesprogrammet **Hent Insights**.</span><span class="sxs-lookup"><span data-stu-id="f277e-338">Select the **Get insights** add-in.</span></span>
4. <span data-ttu-id="f277e-339">Angiv følgende værdier på siden med tilføjelsesprogrammet **Hent Insights**.</span><span class="sxs-lookup"><span data-stu-id="f277e-339">On the **Get insights** add-in details page, enter the following values.</span></span>

    | <span data-ttu-id="f277e-340">Værdi</span><span class="sxs-lookup"><span data-stu-id="f277e-340">Value</span></span>                                                    | <span data-ttu-id="f277e-341">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="f277e-341">Description</span></span> |
    |----------------------------------------------------------|-------------|
    | <span data-ttu-id="f277e-342">CDS URL-adresse til organisation</span><span class="sxs-lookup"><span data-stu-id="f277e-342">CDS Organization URL</span></span>                                     | <span data-ttu-id="f277e-343">URL-adressen til Common Data Service-organisationen for Common Data Service-forekomst.</span><span class="sxs-lookup"><span data-stu-id="f277e-343">The Common Data Service organization URL of the Common Data Service instance.</span></span> <span data-ttu-id="f277e-344">Hvis du vil finde denne værdi, skal du åbne [Power Apps-portalen](https://make.powerapps.com), vælge knappen **Indstillinger** (tandhjulssymbolet) i øverste højre hjørne, vælge **Avancerede indstillinger** og kopiere URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="f277e-344">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Advanced settings**, and copy the URL.</span></span> <span data-ttu-id="f277e-345">(URL-adressen slutter med "dynamics.com.")</span><span class="sxs-lookup"><span data-stu-id="f277e-345">(The URL ends with "dynamics.com.")</span></span> |
    | <span data-ttu-id="f277e-346">CDS Org-id</span><span class="sxs-lookup"><span data-stu-id="f277e-346">CDS Org ID</span></span>                                               | <span data-ttu-id="f277e-347">Miljø-id for Common Data Service-forekomst.</span><span class="sxs-lookup"><span data-stu-id="f277e-347">The environment ID of the Common Data Service instance.</span></span> <span data-ttu-id="f277e-348">Hvis du vil finde denne værdi, skal du åbne [Power Apps-portalen](https://make.powerapps.com), vælge knappen **Indstillinger** (tandhjulssymbolet) i øverste højre hjørne, vælge **Tilpasning \> Developer-ressourcer \> Forekomstreferenceoplysninger** og kopiere værdien **id**.</span><span class="sxs-lookup"><span data-stu-id="f277e-348">To find this value, open the [Power Apps portal](https://make.powerapps.com), select the **Settings** button (gear symbol) in the upper-right upper corner, select **Customizations \> Developer resources \> Instance Reference Information**, and copy the **ID** value.</span></span> |
    | <span data-ttu-id="f277e-349">CDS-lejer-id (mappe-id fra AAD)</span><span class="sxs-lookup"><span data-stu-id="f277e-349">CDS Tenant ID (Directory ID from AAD)</span></span>               | <span data-ttu-id="f277e-350">Lejer-id for Common Data Service-forekomst.</span><span class="sxs-lookup"><span data-stu-id="f277e-350">The tenant ID of the Common Data Service instance.</span></span> <span data-ttu-id="f277e-351">Hvis du vil finde denne værdi, skal åbne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere værdien **Lejer-id**.</span><span class="sxs-lookup"><span data-stu-id="f277e-351">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory**, and copy the **Tenant ID** value.</span></span> |
    | <span data-ttu-id="f277e-352">Angiv det brugerobjekt-id, der har rollen som systemadministrator</span><span class="sxs-lookup"><span data-stu-id="f277e-352">Provide user object ID who has system administrator role</span></span> | <span data-ttu-id="f277e-353">Azure AD-brugerobjekt-id for brugeren i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f277e-353">The Azure AD user object ID of the user in Common Data Service.</span></span> <span data-ttu-id="f277e-354">Denne bruger skal være systemadministrator for Common Data Service-forekomsten.</span><span class="sxs-lookup"><span data-stu-id="f277e-354">This user must be a system administrator of the Common Data Service instance.</span></span> <span data-ttu-id="f277e-355">Hvis du vil finde denne værdi, skal du åbne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory\> Brugere**, vælge brugeren og derefter kopiere **Objekt-id**-værdien i afsnittet **Identitet**.</span><span class="sxs-lookup"><span data-stu-id="f277e-355">To find this value, open the [Azure portal](https://portal.azure.com), go to **Azure Active Directory \> Users**, select the user, and then, in the **Identity** section, copy the **Object ID** value.</span></span> |
    | <span data-ttu-id="f277e-356">Er dette standard-CDS-miljø for lejeren?</span><span class="sxs-lookup"><span data-stu-id="f277e-356">Is this the default CDS environment for the tenant?</span></span>      | <span data-ttu-id="f277e-357">Hvis Common Data Service-forekomsten var den første produktionsforekomst, der blev oprettet, skal du markere dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="f277e-357">If the Common Data Service instance was the first production instance that was created, select this check box.</span></span> <span data-ttu-id="f277e-358">Hvis Common Data Service-forekomsten er oprettet manuelt, skal du fjerne markeringen i dette afkrydsningsfelt.</span><span class="sxs-lookup"><span data-stu-id="f277e-358">If the Common Data Service instance was manually created, clear this check box.</span></span> |

## <a name="feedback-and-support"></a><span data-ttu-id="f277e-359">Feedback og support</span><span class="sxs-lookup"><span data-stu-id="f277e-359">Feedback and support</span></span>

<span data-ttu-id="f277e-360">Send en e-mail til [Indsigt i debitorbetaling (prøveversion)](mailto:fiap@microsoft.com), hvis du er interesseret i at give feedback eller har brug for support.</span><span class="sxs-lookup"><span data-stu-id="f277e-360">Please send an email to [Customer payment insights (Preview)](mailto:fiap@microsoft.com) if you are interested in providing feedback or need support.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="f277e-361">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="f277e-361">Privacy notice</span></span>

<span data-ttu-id="f277e-362">Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.</span><span class="sxs-lookup"><span data-stu-id="f277e-362">Previews (1) might use less privacy and fewer security measures than the Dynamics 365 Finance and Operations service, (2) aren't included in the service level agreement (SLA) for this service, (3) should not be used to process personal data or other data that is subject to legal or regulatory compliance requirements, and (4) have limited support.</span></span>
