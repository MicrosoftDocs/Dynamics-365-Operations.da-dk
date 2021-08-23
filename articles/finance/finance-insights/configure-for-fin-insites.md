---
title: Konfiguration til Finance Insights - versioner før 10.0.19
description: I dette emne beskrives de konfigurationstrin, der sætter systemet i gang med at bruge de egenskaber, der er tilgængelige i Finance Insights for versioner før 10.0.19.
author: ShivamPandey-msft
ms.date: 07/21/2021
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
ms.openlocfilehash: 77d51302ee38c843a1988d9a65537015edb9b5159ed1e9f657a04b5e0fe72cea
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6764328"
---
# <a name="configuration-for-finance-insights-for-private-preview-preview---before-version-10019"></a>Konfiguration til Finance Insights til privat forhåndsversion (forhåndsversion) - før version 10.0.19

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> Følgende procedurer til opsætning af Finance Insights gælder for Microsoft Dynamics 365 Finance før version 10.0.19. Hvis du vil konfigurere Finance Insights på version 10.0.20 og senere, skal du se [Konfiguration for Finance Insights (forhåndsversion) - version 10.0.20 og senere](configure-for-fin-insites-PubPrvw.md).

Finance Insights kombinerer funktionalitet fra Microsoft Dynamics 365 Finance sammen med Microsoft Dataverse, Azure og AI Builder for at levere effektive prognoseværktøjer til din organisation. I dette emne beskrives de konfigurationstrin, der sætter systemet i gang med at bruge de egenskaber, der er tilgængelige i Finance Insights.

## <a name="deploy-dynamics-365-finance"></a>Installér Dynamics 365 Finance

Følg disse trin for at installere miljøerne.

1. I Microsoft Dynamics Lifecycle Services (LCS) skal du oprette eller opdatere et Dynamics 365 Finance-miljø. Miljøet kræver programversion 10.0.11/Platformopdatering 35 eller nyere.
2. Miljøet skal være et miljø med høj tilgængelighed (HA) i sandkassesystemet. (Denne type miljø kaldes også et Niveau-2-miljø). Du kan finde flere oplysninger i [Miljøplanlægning](../../fin-ops-core/fin-ops/imp-lifecycle/environment-planning.md).
3. Hvis du konfigurerer Finance Insights i et sandkassemiljø, skal du muligvis kopiere produktionsdata til dette miljø, så du kan få forudsigelser, der virker. En forudsigelsesmodel bruger flere års data til at opbygge forudsigelser. Contoso-demodataene indeholder ikke nok historikdata til at træne forudsigelsesmodellen korrekt. 

## <a name="configure-dataverse"></a>Konfigurer Dataverse

Benyt følgende fremgangsmåde til at konfigurere Dataverse for Finance Insights.

1. Åbn miljøsiden i LCS, og kontroller, at sektionen **Intregration af Power Platform** allerede er konfigureret.
    1. Hvis den allerede er konfigureret, skal det Dataverse-miljønavn, der er knyttet Dynamics 365 Finance-miljøet, være anført. Kopier Dataverse-miljønavnet.
    2. Hvis den ikke er konfigureret, skal du benytte følgende fremgangsmåde:
        1. Klik på knappen **Opsætning** i sektionen Integration af Power Platform. Det kan tage op til en time, før miljøet er konfigureret.
        2. Hvis Dataverse-miløjet er konfigureret korrekt, skal det Dataverse-miljønavn, der er tilknyttet Dynamics 365 Finance-miljøet, være anført. Kopier Dataverse-miljønavnet.
> [!NOTE]
> Når du har fuldført miljøkonfigurationen, skal du **IKKE** vælge knappen **Link til CDS for Apps**. Dette er ikke nødvendigt for Finance Insights og vil deaktivere muligheden for at fuldføre de nødvendige tilføjelsesprogrammer for miljø i LCS.

2. Åbn [Power Platform Administration](https://admin.powerplatform.microsoft.com/), og udfør følgende trin for at oprette et nyt Dataverse-miljø i samme Active Directory-lejer:

    1. Åbn siden **Miljøer**.

        Siden [![Miljøer.](./media/power-pltfrm-admin-center.png)](./media/power-pltfrm-admin-center.png)

    2. Vælg Dataverse-miljøet, der er oprettet ovenfor, og vælg derefter **Indstillinger**.
    3. Vælg **Ressourcer \> Alle tidligere indstillinger**.
    4. Vælg indstillinger på den øverste navigationslinje **Indstillinger**, og vælg derefter **Tilpasninger**.
    5. Vælg **Udviklerressourcer**.
    6. Kopiér værdien af **Dataverse-organisations-id**.
    7. I adresselinjen i browseren skal du notere URL-adressen for Dataverse-organisationen. URL-adressen kan f. eks være `https://org42b2b3d3.crm.dynamics.com`.

3. Hvis du planlægger at bruge funktionen Likviditetsflowbudgetter eller budgetprognoser, skal du følge disse trin for at opdatere din organisations anmærkningsgrænse til mindst 50 MB:

    1. Åbn [Power Apps-portalen](https://make.powerapps.com).
    2. Vælg det miljø, du netop har oprettet, og vælg derefter **Avancerede indstillinger**.
    3. Vælg **Indstillinger \> E-mailkonfiguration**.
    4. Ret værdien i feltet **Maksimal filstørrelse** til **51.200**. (Værdien er udtrykt i kilobyte \[KB\].)
    5. Vælg **OK** for at gemme ændringerne.

## <a name="configure-the-azure-setup"></a>Konfigurere Azure-opsætning

### <a name="enter-the-dataverse-directory-id-and-the-users-azure-ad-object-id"></a>Angiv Dataverse-mappe-id og brugerens Azure AD-objekt-id

1. Angiv Dataverse-mappe-id:

    1. Åbn [Azure-portalen](https://portal.azure.com).
    2. Log på ved hjælp af det bruger-id, der blev brugt til at oprette Dataverse-miljøet.
    3. Gå til **Azure Active Directory**.
    4. Kopier værdien **Lejer-id**.

2. Angiv brugerens Azure Active Directory (Azure AD)-objekt-id:

    1. Gå til **Brugere** i [Azure-portal](https://portal.azure.com), og søg efter brugere efter e-mailadresse.
    2. Brugerens brugerens navn.
    3. Kopier værdien i **Objekt-id**.

### <a name="use-azure-cloud-shell-to-set-up-finance-insights-data-lake-resources"></a>Brug Azure Cloud Shell til at konfigurere Finance Insights Data Lake-ressourcer

# <a name="use-a-windows-powershell-script"></a>[Brug et Windows PowerShell-script](#tab/use-a-powershell-script)

Der er angivet et Windows PowerShell-script, så du nemt kan konfigurere de Azure-ressourcer, der er beskrevet under [Konfigurere eksport til Azure Data Lake](../../fin-ops-core/dev-itpro/data-entities/configure-export-data-lake.md). Hvis du foretrækker at foretage manuel opsætning, kan du springe denne procedure over og fortsætte med proceduren i afsnittet [Manuel opsætning](#manual-setup).

> [!NOTE]
> Følg nedenstående trin for at køre PowerShell-scriptet. Indstillingen Azure CLI "Try it" eller kørsel af scriptet på din PC fungerer muligvis ikke.

Udfør følgende trin for at konfigurere Azure ved hjælp af Windows PowerShell-scriptet. Du skal have rettigheder til at oprette en Azure-ressourcegruppe, Azure-ressourcer og et Azure AD-program. Yderligere oplysninger om de påkrævede tilladelser finder du i [Kontrollér Azure AD-tilladelser](/azure/active-directory/develop/howto-create-service-principal-portal#permissions-required-for-registering-an-app).

1. Gå til dit Azure-abonnement på [Azure-portalen](https://portal.azure.com). Vælg knappen **Cloud Shell** til højre for feltet **Søg**.
2. Vælg **PowerShell**.
3. Opret lager, hvis du bliver bedt om det.
4. Gå til fanen **Azure CLI**, og vælg **Kopiér**.  
5. Åbn Notesblok, og indsæt PowerShell-scriptet. Gem filen som ConfigureDataLake.ps1.
6. Overfør Windows PowerShell-scriptet til sessionen ved hjælp af menuindstillingen til overførsel i Cloud Shell.
7. Kør scriptet .\ConfigureDataLake.ps1.
8. Følg vejledningen for at køre scriptet.
9. Brug oplysningerne fra scriptoutputtet til at installere tilføjelsesprogrammet **Eksportér til Data Lake** i LCS.
10. Brug oplysningerne fra scriptoutputtet til at aktivere enhedslageret på siden **Dataforbindelser** i Finance (**Systemadministration \> Systemparametre \> Dataforbindelser**).

### <a name="manual-setup"></a>Manuel opsætning

#### <a name="add-applications-to-the-azure-ad-tenant"></a>Tilføj ansøgninger til Azure AD-lejeren

1. Gå til **Azure Active Directory** i [Azure-portalen](https://portal.azure.com).
2. Vælg **Administrer \> Virksomhedsprogrammer**.
3. Søg efter følgende ansøgninger efter app-id.

    | Applikation                              | App-id                               |
    |------------------------------------------|--------------------------------------|
    | Microsoft Dynamics ERP Microservices     | 0cdb527f-a8d1-4bf8-9436-b352c68682b2 |
    | Microsoft Dynamics ERP Microservices CDS | 703e2651-d3fc-48f5-942c-74274233dba8 |
    | Godkendelsestjeneste til AI Builder         | ad40333e-9910-4b61-b281-e3aeeb8c3ef3 |

Hvis du ikke kan finde de foregående programmer, kan du prøve følgende trin.

1. Vælg menuen **Start** på den lokale computer, og søg efter **PowerShell**.
2. Vælg og hold (eller højreklik) **Windows PowerShell**, og vælg derefter **Kør som administrator**.
3. Kør følgende kommando for at installere modulet **AzureAD**.

    `Install-Module -Name AzureAD`

4. Hvis der kræves en NuGet-udbyder for at fortsætte, skal du vælge **J** for at installere den.
5. Hvis meddelelsen "Ikke-betroet lager" vises, skal vælge **J** for at fortsætte.
6. For hvert program, der skal tilføjes, skal du køre følgende kommandoer for at føje programmet til Azure AD. Når du bliver bedt om det, skal du logge på som Azure AD-administrator.

    `Connect-AzureAD`

    `New-AzureADServicePrincipal –AppId <AppId>`

#### <a name="create-azure-resources"></a>Oprette Azure-ressourcer

> [!NOTE]
> Sørg for at oprette følgende ressourcer i samme Azure AD-forekomst som Dataverse-miljøet. Du kan ikke bruge ressourcer fra en anden Azure AD-forekomst.

1. Oprette en ny lagerkonto:

    1. Opret en Lagerkonto i [Azure-portalen](https://portal.azure.com).
    2. Angiv følgende felter i dialogboksen **Opret lagerkonto**:

        - **Placering** - Vælg det datacenter, hvor dit miljø er placeret.
        - **Ydeevne** - Vi anbefaler, at du vælger **Standard**.
        - **Kontotype** - Du skal vælge **Lager V2**.

    3. I dialogboksen **Avancerede indstillinger** til indstillingen **Data Lake-lager Gen2** skal du vælge **Aktiver** under funktionen **Hierarkiske navneområder**. Hvis du deaktiverer denne funktion, kan du ikke forbruge data, som Finance and Operations-apps skriver ved hjælp af tjenester som f.eks. Power BI-dataflow.
    4. Vælg **Gennemse og opret**. Når installationen er fuldført, vises den nye ressource på Azure-portalen.
    5. Gå til den lagerkonto, du har oprettet.
    6. Vælg **Adgangsnøgler** i menuen til venstre.
    7. Kopiér og gem forbindelsesstrengen for enten **Nøgle 1** eller **Nøgle 2**.
    8. Kopiér og gem navnet på lagerkontoen.

2. Oprette en ny Key Vault:

    1. Opret en Key Vault i [Azure-portalen](https://portal.azure.com).
    2. Vælg det datacenter, hvor dit miljø er placeret, i feltet **Placering** i dialogboksen **Opret Key Vault**.
    3. Når du har oprettet en Key Vault, skal du vælge den på listen og derefter vælge **Hemmeligheder**.
    4. Vælg **Generer/importer**.
    5. I dialogboksen **Opret en hemmelighed** i feltet **Uploadindstillinger** skal du vælge **Manuel**.
    6. Angiv et navn på hemmeligheden. Noter navnet, hvis du skal angive det senere.
    7. I feltet **Værdi** skal du angive den forbindelsesstreng, du har fået fra lagerkontoen i den foregående procedure.
    8. Vælg **Aktiverfet**, og vælg derefter **Opret**. Hemmeligheden oprettes og føjes til Key Vault.
    9. Gå til **Oversigt over Key Vault**, og noter DNS-navnet.

3. Oprette og registrere en Azure AD-ansøgning:

    1. I [Azure-portalen](https://portal.azure.com) skal du gå til **Azure Active Directory**, og derefter vælge **App-registreringer**.
    2. Vælg **Ny programregistrering**, og angiv følgende felter:

        - **Navn** - Angiv navnet på appen.
        - **Programtype** - Vælg **Web API**.
        - **Omdirigering af URI-konfiguration** - Angiv URL-adressen til Dynamics 365-forekomsten, f.eks. `https://yourdynamicsinstance.dynamics.com/auth`.

    3. Gå til den app, du lige har oprettet, og kopiér og gem værdien **Program-id (klient)**. Du skal angive denne værdi senere, når du konfigurerer Key Vault.
    4. Gå til **API-tilladelser**, og udfør følgende trin:

        1. Vælg **Tilføj en tilladelse**.
        2. Vælg **Azure Key Vault**.
        3. Når du har valgt delegerede rettigheder, skal du vælge **bruger\_repræsentation**.
        4. Vælg **Tilføj tilladelser**.

    5. Vælg **Certifikater \& hemmeligheder** i menuen for appen, og udfør derefter følgende trin for at oprette hemmeligheder for Key Vault:

        1. Vælg **Ny klient-hemmelighed**.
        2. Indtast et navn i feltet **Nøglebeskrivelse**.
        3. Vælg en varighed, og vælg derefter **Tilføj**. Der genereres en hemmelighed i feltet **Værdi**.
        4. Kopier og gem den hemmelige værdi.

4. Oprette Key Vault-hemmeligheder:

    1. Gå til den Key Vault, du har oprettet tidligere, og vælg **Hemmeligheder**.
    2. Udfør følgende trin for hvert hemmelige navn i følgende tabel:

        1. Vælg **Generer/importer**.
        2. I dialogboksen **Opret en hemmelighed** i feltet **Uploadindstillinger** skal du vælge **Manuel**.
        3. Opret det hemmelige navn og værdien ud fra følgende tabel.
        4. Vælg **Aktiverfet**, og vælg derefter **Opret**. Hemmeligheden oprettes og føjes til Key Vault.

        | Hemmeligt navn                       | Hemmelig værdi                                                                                |
        |-----------------------------------|---------------------------------------------------------------------------------------------|
        | app-id                            | App-id for det program, du har oprettet tidligere                                      |
        | app-hemmelighed                        | Den klienthemmelighed, du tidligere har gemt                                                    |
        | lagerkontonavn              | Navnet på den lagerkonto, du har oprettet tidligere, f. eks. **lagerkonto1**       |
        | lagerkontoforbindelsesstreng | Den forbindelsesstreng, du har kopieret fra siden **Adgangstaster** til lagerkontoen |

5. Godkende programmet for at få adgang til Key Vault:

    1. I [Azure-portalen](https://portal.azure.com) skal du åbne den Key Vault, du har oprettet tidligere.
    2. Vælg adgangspolitikker.
    3. Udfør følgende trin for hvert program i følgende tabel:

        1. Vælg **Tilføj adgangspolitik** for at oprette en adgangspolitik.
        2. I feltet **Hemmelige tilladelser** skal du vælge tilladelser fra følgende tabel.
        3. I feltet **Vælg overordnet** skal du søge efter programmets visningsnavn i følgende tabel.
        4. Vælg **Vælg**.
        5. Vælg **Tilføj**.
        6. Vælg **Gem**.

        | Applikation                                              | Rettigheder |
        |----------------------------------------------------------|-------------|
        | Visningsnavnet for den nye program, du har oprettet | Hent, Sæt på liste   |
        | **Microsoft Dynamics ERP Microservices**                 | Hent, Sæt på liste   |

6. Tildele roller for at få adgang til lagerkontoen:

    1. I [Azure-portalen](https://portal.azure.com) skal du åbne den lagerkonto, du har oprettet tidligere.
    2. Vælg **Adgangskontrol (IAM)**, og vælg derefter **Rolletildelinger**.
    3. Vælg **Tilføj, Tilføj rolletildeling**.
    4. Udfør følgende trin for hvert program i følgende tabel:

        1. Vælg rollen fra følgende tabel.
        2. Forlad feltet **Tildel adgangsrettigheder til**, der er angivet til **Azure AD-bruger, -gruppe eller -tjenesteprincipal**.
        3. I feltet **Vælg** skal du angive programmet fra følgende tabel.
        4. Vælg **Gem**.

        | Applikation                                              | Rolle                        |
        |----------------------------------------------------------|-----------------------------|
        | Visningsnavnet for den nye program, du har oprettet | Ejer                       |
        | Visningsnavnet for den nye program, du har oprettet | Bidragyder                 |
        | Visningsnavnet for den nye program, du har oprettet | Bidragyder til lagerkonto |
        | Visningsnavnet for den nye program, du har oprettet | Ejer af Blob Data-lager     |
        | **Godkendelsestjeneste til AI Builder**                     | Læser af Blob Data-lager    |

# <a name="azure-cli"></a>[Azure CLI](#tab/azure-azure-cli)

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



## <a name="configure-the-data-lake"></a>Konfigurer Data Lake

Udfør følgende trin for at bruge LCS til at tilføje tilføjelsesprogrammet Azure Data Lake til miljøet.

1. Log på LCS, og vælg derefter detaljerede oplysninger under miljønavnet på højre side af siden, vælg **Alle detaljer**.
2. Vælg **Installér et nyt tilføjelsesprogram** i afsnittet **Tilføjelsesprogrammer for miljø**.
3. Vælg **Eksporter til Data Lake**-tilføjelsesprogrammet.
4. Angiv følgende værdier.

    | Værdi                                                              | Betegnelse |
    |--------------------------------------------------------------------|-------------|
    | Lejer-id på det Azure-abonnement, hvor Key Vault er placeret | Det lejer-id, hvor lagerkontoen, apps og Key Vault er placeret. Hvis du vil finde denne værdi, skal åbne [Azure-portalen](https://portal.azure.com), gå til **Azure Active Directory** og kopiere værdien **Lejer-id**. |
    | Angiv DNS-navn for Key Vault                             | DNS-navnet på Key Vault, som f.eks. `https://customkeyvault.vault.azure.net/`. (Denne værdi svarer til det DNS-navn, der bruges i enhedslageret). |
    | Angiv den hemmelighed, der indeholder navnet på lagerkontoen   | **lagerkontonavn** |
    | Hemmeligt navn på app-id, der skal bruges til at få adgang til Data Lake          | **app-id** |
    | Hemmeligt navn, der skal bruges sammen med app-id                                 | **app-hemmelighed** |

5. Accepter betingelserne, og vælg **Installer**.

Tilføjelsesprogrammet vil blive installeret inden for et par minutter.

## <a name="configure-ai-builder"></a>Konfigurer AI Builder

1. Log på LCS, og åbn siden **Miljøoplysninger**.
2. Rul til sektionen **Tilføjelsesprogrammer for miljø**. Du bør kunne se de tilføjelsesprogrammer, der allerede er installeret i dette miljø. Hvis tilføjelsesprogrammet **Eksporter til Data Lake** ikke er angivet, skal du konfigurere dette tilføjelsesprogram.
3. Vælg tilføjelsesprogrammet **Hent Insights**.
4. Angiv følgende værdier på siden med tilføjelsesprogrammet **Hent Insights**.

    | Værdi                                                    | Betegnelse |
    |----------------------------------------------------------|-------------|
    | CDS URL-adresse til organisation                                     | Dataverse-organisationens URL-adresse, der blev kopieret ovenfor. |
    | CDS Org-id                                               | Dataverse-organisationens id, der blev kopieret ovenfor. |
5. Aktivér **Er dette standardmiljøet for din lejer**.

Tilføjelsesprogrammet kan være flere minutter om at blive installeret.
    
## <a name="configure-the-entity-store"></a>Konfigurer enhedslager

Udfør følgende trin for at konfigurere enhedslageret i Finance-miljøet.

1. Gå til **Systemadministration \> Opsætning \> Systemparametre \> Dataforbindelser**.
2. Indstil følgende Key Vault-felter:

    - **Program-id (klient)** - Angiv det programklient-id, du har oprettet tidligere.
    - **Programhemmelighed** - Angiv den hemmelighed, du har gemt for det program, du har oprettet tidligere.
    - **DNS-navn** - Find DNS-navnet (Domain Name System) på siden Programdetaljer for det program, du har oprettet tidligere.
    - **Hemmeligt navn** - Angiv **lager-konto-forbindelsesstreng**.
3. Aktivér **Aktivér Data Lake-integration**.
4. Vælg **Test Azure Key Vault**, og kontrollér, at der ikke er nogen fejl.
5. Vælg **Test Azure-lager**, og kontrollér, at der ikke er nogen fejl.

## <a name="feedback-and-support"></a>Feedback og support

Send en e-mail til [Indsigt i debitorbetaling (prøveversion)](mailto:fiap@microsoft.com), hvis du er interesseret i at give feedback eller har brug for support.

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger

Forhåndsvisning (1) kan anvende mindre beskyttelse af personlige oplysninger og sikkerhedsforanstaltninger end Dynamics 365 Finance and Operations-tjeneste, (2) de er ikke inkluderet i serviceniveauaftalen (SLA) for denne tjeneste, (3) de må ikke bruges til at behandle personaleoplysninger eller andre data, der er underlagt lovgivning eller overholdelse af lovmæssige krav, og (4) de har begrænset support.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
