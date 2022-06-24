---
title: Implementere edge-skaleringsenheder på brugerdefineret hardware ved hjælp af LBD
description: Denne artikel indeholder en forklaring på, hvordan der klargøres edge-skaleringsenheder i det lokale miljø ved hjælp af tilpasset hardware og installation, der er baseret på lokale forretningsdata (LBD).
author: Mirzaab
ms.date: 01/24/2022
ms.topic: article
ms.prod: dynamics-365
ms.service: ''
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: mirzaab
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 794de8c0d77949789e4046418ac2b55dba1bee02
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8882744"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd"></a>Implementere edge-skaleringsenheder på brugerdefineret hardware ved hjælp af LBD

[!include [banner](../includes/banner.md)]

Edge-skaleringsenheder spiller en vigtig rolle i den distribuerede hybridtopologi for Supply Chain Management. I hybridtopologien kan du fordele arbejdsbyrder mellem din Supply Chain Management-sky-hub og yderligere skaleringsenheder i skyen eller på Edge.

Edge-skaleringsenheder implementeres ved at oprette lokale forretningsdata (LBD) [det lokale miljø](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) og derefter konfigurere dem, så de fungerer som en skaleringsenhed i den distribuerede hybridtopologi for Supply Chain Management. Dette kan du opnå ved at knytte det lokale LBD-miljø til et Supply Chain Management-miljø i skyen, der er konfigureret til at fungere som hub.  

Denne artikel beskriver, hvordan du kan konfigurere et lokalt LBD-miljø som en edge-skaleringsenhed og derefter knytte det til en hub.

## <a name="infrastructure-considerations"></a>Overvejelser ved infrastrukturen

Edge-skaleringsenheder kører i lokale miljøer, så infrastrukturkravene er meget ens. Der er dog visse forskelle, der skal bemærkes:

- Edge-skaleringsenheder bruger ikke Financial Reporting, så de kræver ikke Financial Reporting-noder.
- Arbejdsbyrderne ved produktion og lager er ikke beregningstunge, og derfor bør du overveje at tilpasse beregningskraften til AOS-noder tilsvarende.

## <a name="deployment-overview"></a>Oversigt over installation

Her er en oversigt over installationstrinnene.

1. **Aktivér en LBD-plads i dit LBD-projekt i Microsoft Dynamics Lifecycle Services (LCS).**

1. **Konfigurer og implementer et LBD-miljø med en *tom* database.**

    Brug LCS til at installere LBD-miljøet med den seneste topologi og en tom database. Du kan finde flere oplysninger i afsnittet [Konfigurere og implementere et LBD-miljø med tom database](#set-up-deploy) senere i denne artikel. Du skal bruge Supply Chain Management version 10.0.21 eller højere på tværs af hub- og skaleringsenhedsmiljøer.

1. **Upload målpakker til LBD-projektaktiver i LCS.**

    Forbered program-, platform- og tilpasningspakker, som du bruger på tværs af hubben og edge-skaleringsenheden. Du kan finde flere oplysninger i afsnittet [Uploade målpakker til LBD-projektaktiver i LCS](#upload-packages) senere i denne artikel.

1. **Servicér LBD-miljøet med målpakkerne.**

    Dette trin sikrer, at samme opbygning og tilpasninger implementeres på hubben og den nævnte skaleringsenhed. Du kan finde flere oplysninger i afsnittet [Servicere LBD-miljøet med målpakkerne](#service-target-packages) senere i denne artikel.

1. **Fuldfør konfigurationen af skaleringsenheden og tildelingen af arbejdsbyrde.**

    Du kan finde flere oplysninger i afsnittet [Tildele din LBD-edge-skaleringsenhed til en hub](#assign-edge-to-hub) senere i denne artikel.

De resterende afsnit i denne artikel indeholder flere oplysninger om, hvordan du fuldfører hvert trin.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Konfigurere og implementere et LBD-miljø med en tom database

Dette trin opretter et funktionelt LBD-miljø. Men miljøet har ikke nødvendigvis samme program- og platformsversioner som hub-miljøet. Desuden mangler den stadig tilpasninger, og den er endnu ikke aktiveret til at fungere som skaleringsenhed.

1. Følg vejledningen i [Konfigurere og installere miljøer i det lokale miljø (Platform update 41 og senere)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Du skal bruge Supply Chain Management version 10.0.21 eller højere på tværs af hub- og skaleringsenhedsmiljøer. Derudover skal du bruge version 2.12.0 eller en senere version af infrastrukturens scripts. 

    > [!IMPORTANT]
    > Læs resten af dette afsnit, **før** du fuldfører trinnene i det pågældende artikel.

1. Før du beskriver din konfiguration i infrastrukturens\\ConfigTemplate.xml-fil, skal du køre følgende script:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Dette script fjerner alle konfigurationer, der ikke er nødvendige ved implementering af edge-skaleringsenheder.

1. Konfigurer en database, der indeholder tomme data, som det er beskrevet i [Konfigurere databaser](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Brug den tomme data.bak-fil til dette trin.
1. Når du har fuldført trinnet [Konfigurer databaser](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb), skal du køre følgende script for at konfigurere Scale Unit Alm Orchestrator-databasen.

    > [!NOTE]
    > Konfigurer ikke Financial Reporting-databasen i trinnet [Konfigurer databaser](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb).

    ```powershell
    .\Initialize-Database.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -ComponentName EdgeScaleUnit
    ```

    Scriptet Initialize-Database.ps1 udfører følgende handlinger:

    1. Opret en tom database med navnet **ScaleUnitAlmDb**.
    2. Knyt brugerne til databaseroller baseret på følgende tabel.

        | Bruger            | Type | Databaserolle |
        |-----------------|------|---------------|
        | svc-LocalAgent$ | gMSA | db\_ejer     |

1. Følg vejledningen i [Konfigurere og installere miljøer i det lokale miljø (Platform update 41 og senere)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md).
1. Når du har fuldført trinnet [Konfigurer AD FS](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb), skal du følge disse trin:

    1. Opret et nyt AD FS-program (Active Directory Federation Services), som gør det muligt for Alm Orchestration-tjenesten at kommunikere med din AOS (Application Object Server).

        ```powershell
        # Host URL is your DNS record\host name for accessing the AOS
        .\Create-ADFSServerApplicationForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml -HostUrl 'https://ax.d365ffo.onprem.contoso.com'
        ```

    1. Opret et nyt Azure Active Directory-program (Azure AD), der giver Alm Orchestration-tjenesten mulighed for at kommunikere med tjenesten Administration af skaleringsenhed.

        ```powershell
        # Example .\Create-SumAADApplication.ps1 -ConfigurationFilePath ..\ConfigTemplate.xml -TenantId '6240a19e-86f1-41af-91ab-dbe29dbcfb95' -ApplicationDisplayName 'EdgeAgent-SUMCommunication-EN01'
        .\Create-SumAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                       -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                       -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
        ```

1. Følg vejledningen i [Konfigurere og installere miljøer i det lokale miljø (Platform update 41 og senere)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Når du skal angive konfigurationen for den lokale agent, skal du sørge for at aktivere funktionerne i Edge Scale Unit og angive alle påkrævede parametre.

    ![Aktivering af Edge Scale Unit-funktioner.](media/EnableEdgeScaleUnitFeatures.png "Aktivering af Edge Scale Unit-funktioner.")

1. Før du implementerer miljøet fra LCS, skal du konfigurere scriptet før installation. Du kan finde flere oplysninger under [Scripts til præ-installation og efterinstallation af lokale agenter](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopier scriptet Configure-CloudAndEdge.ps1 fra mappen **ScaleUnit** i **Infrastrukturscripts** til mappen **Scripts** i det share for agentfillagring, der blev konfigureret i miljøet. En typisk sti er \\\\lbdiscsi01\\agent\\Scripts.
    2. Opret scriptet **PreDeployment.ps1**, som vil kalde scriptene ved hjælp af de påkrævede parametre. Scriptet til før installation skal være lagt i **Scripts**-mappen i agentfillagerets share. Ellers kan det ikke køres. En typisk sti er \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Indholdet af scriptet PreDeployment.ps1 vil ligne følgende eksempel.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        . $PSScriptRoot\Configure-CloudAndEdge.ps1 -AgentShare $agentShare -InstanceId '@A'
        ```

        > [!NOTE]
        > Parameteren InstanceId må kun være to tegn. Det første tegn er @, og det andet kan være et hvilket som helst stort bogstav i det engelske alfabet.
        >
        > - Gyldige værdier:
        >   - @D
        >   - @X
        > - Ikke gyldige værdier:
        >   - @a
        >   - @4
        >   - @#

1. Implementer miljøet ved hjælp af den seneste basistopologi, der findes.
1. Følg disse trin, når dit miljø er installeret.

    1. Kør følgende SQL-kommandoer i din virksomhedsdatabase (AXDB).

        ```sql
        ALTER TABLE dbo.NUMBERSEQUENCETABLE ENABLE CHANGE_TRACKING WITH (TRACK_COLUMNS_UPDATED = ON)
        delete from NumberSequenceTable
        delete from NumberSequenceReference
        delete from NumberSequenceScope
        delete from FeatureManagementMetadata
        delete from FeatureManagementState
        delete from SysFeatureStateV0
        ```

    1. Forøg den maksimale batchsession til en værdi, der er mere end 4.

        ```sql
        Update batchserverconfig set maxbatchsessions = '<Replace with number of concurrent batch tasks you want>'
        ```

    1. Kontrollér, at sporing af ændringer er aktiveret i din virksomhedsdatabase (AXDB).

        1. Åbn SQL Server Management Studio (SSMS).
        1. Vælg og hold (eller højreklik på) din virksomhedsdatabase (AXDB), og vælg derefter **Egenskaber**.
        1. Vælg **Ændringssporing** i det vindue, der åbnes, og angiv følgende værdier:

            - **Ændringssporing:** *Sand*
            - **Opbevaringsperiode:** *7*
            - **Opbevaringsenheder:** *Dage*
            - **Automatisk oprydning:** *Sand*

    1. Tilføj det AD FS-program-id, du oprettede tidligere (ved hjælp af scriptet Create-ADFSServerApplicationForEdgeScaleUnits.ps1) til Azure AD-programtabellen i din skaleringsenhed. Dette trin kan fuldføres manuelt via brugergrænsefladen. Du kan også fuldføre det via databasen ved hjælp af følgende script.

        ```sql
        DECLARE @ALMOrchestratorId NVARCHAR(76) = '<Replace with the ADFS Application ID created in a previous step>';

        IF NOT EXISTS (SELECT TOP 1 1 FROM SysAADClientTable WHERE AADClientId = @ALMOrchestratorId)
        BEGIN
            INSERT INTO SysAADClientTable (AADClientId, UserId, Name, ModifiedBy, CreatedBy)
            VALUES (@ALMOrchestratorId, 'ScaleUnitManagement', 'Scale Unit Management', 'Admin', 'Admin');
        END
        ```

## <a name="set-up-an-azure-key-vault-and-an-azure-ad-application-to-enable-communication-between-scale-units"></a><a name="set-up-keyvault"></a>Oprette en Azure Key Vault og et Azure AD-program, der skal aktivere kommunikation mellem skalaenheder

1. Når miljøet er implementeret, skal du oprette et andet Azure AD-program for at aktivere betroet kommunikation mellem din hub og skaleringsenhed.

    ```powershell
    .\Create-SpokeToHubAADApplication.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                          -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                          -ApplicationDisplayName '<Whichever name you want the Azure AD app to have>'
    ```

1. Når du har oprettet programmet, skal du oprette en klienthemmelighed og gemme oplysningerne i en Azure Key Vault. Du skal desuden give adgang til det Azure AD-program, der er oprettet, så det kan hente de hemmeligheder, der er gemt i Key Vault. Følgende script vil automatisk udføre alle de påkrævede handlinger for dig.

    ```powershell
    .\Create-SpokeToHubAADAppSecrets.ps1 -ConfigurationFilePath '<Path of the ConfigTemplate.xml file>' `
                                         -TenantId '<ID of the tenant where your cloud hub is deployed>' `
                                         -SubscriptionName '<Any subscription within your tenant>' `
                                         -ResourceGroupName '<Any resource group within your subscription>' `
                                         -KeyVaultName '<Any key vault within your resource group>' `
                                         -Location '<Any Azure location where Azure Key Vault is available>' `
                                         -LCSEnvironmentId '<The LCS environment ID of your deployed scale unit>' `
    ```

    > [!NOTE]
    > Hvis der ikke findes en Key Vault, der har den angivne værdi for **KeyVaultName**, opretter scriptet automatisk en.

1. Tilføj det Azure AD-program-id, du netop har oprettet (ved hjælp af scriptet Create-SpokeToHubAADApplication.ps1) i Azure AD-programtabellen i din hub. Dette trin kan fuldføres manuelt via brugergrænsefladen.

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Uploade målpakker til LBD-projektaktiver i LCS

Dette trin forbereder programversionen, platformsversionen og tilpasninger, der vil blive oveført til dit LBD-skaleringsenhedsmiljø.

1. Upload den samme pakke med kombineret program/platform, der blev anvendt på hub-miljøet, til aktivbiblioteket i det lokale LCS-projekt.
1. Få en kopi af den tilpassede installerbare pakke, der blev anvendt på hub-miljøet, og upload den til aktivbiblioteket i det lokale LCS-projekt.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Servicere LBD-miljøet med målpakkerne

Dette trin indretter programversionen, platformsversionen og tilpasninger i dit LBD-skaleringsenhedsmiljø med huppen.

1. Servicér LBD-miljøet med den kombinerede pakke med program/platform, som du uploadede i det foregående trin.
1. Servicér LBD-miljøet med den tilpassede installerbare pakke, som du uploadede i det foregående trin.

    ![Anvende opdateringer i LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Anvende opdateringer i LCS")

    ![Valg af tilpasningspakken.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Valg af tilpasningspakken")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Tildele din LBD-edge-skaleringsenhed til en hub

Du kan konfigurere og administrere din edge-skaleringsenhed via portalen Administration af skaleringsenhed. Du kan få flere oplysninger i [Administrere skalaenheder og arbejdsbyrder ved hjælp af portalen til styring af skalaenhed](./cloud-edge-landing-page.md#scale-unit-manager-portal).

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
