---
title: Implementere edge-skaleringsenheder på brugerdefineret hardware ved hjælp af LBD (forhåndsversion)
description: Dette emne indeholder en forklaring på, hvordan der klargøres edge-skaleringsenheder i det lokale miljø ved hjælp af tilpasset hardware og installation, der er baseret på lokale forretningsdata (LBD).
author: cabeln
ms.date: 04/22/2021
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: cabeln
ms.search.validFrom: 2021-04-13
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 0ebbdaab9d6f040497d3158db2712e102b6e9aa8
ms.sourcegitcommit: 1e5a46271bf7fae2f958d2b1b666a8d2583e04a8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2021
ms.locfileid: "7678975"
---
# <a name="deploy-edge-scale-units-on-custom-hardware-using-lbd-preview"></a>Implementere edge-skaleringsenheder på brugerdefineret hardware ved hjælp af LBD (forhåndsversion)

[!include [banner](../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)] <!--KFM: Until 11/1/2021 -->

Edge-skaleringsenheder spiller en vigtig rolle i den distribuerede hybridtopologi for Supply Chain Management. I hybridtopologien kan du fordele arbejdsbyrder mellem din Supply Chain Management-sky-hub og yderligere skaleringsenheder i skyen eller på Edge.

Edge-skaleringsenheder implementeres ved at oprette lokale forretningsdata (LBD) [det lokale miljø](../../fin-ops-core/dev-itpro/deployment/on-premises-deployment-landing-page.md) og derefter konfigurere dem, så de fungerer som en skaleringsenhed i den distribuerede hybridtopologi for Supply Chain Management. Dette kan du opnå ved at knytte det lokale LBD-miljø til et Supply Chain Management-miljø i skyen, der er konfigureret til at fungere som hub.  

Edge-skaleringsenheder er i øjeblikket en forhåndsversion. Derfor må du kun bruge et miljø af denne type i overensstemmelse med [vilkår for forhåndsversion](https://aka.ms/scmcnepreviewterms).

I dette emne beskrives, hvordan du kan konfigurere et lokalt LBD-miljø som en edge-skaleringsenhed og derefter knytte det til en hub.

## <a name="deployment-overview"></a>Oversigt over installation

Her er en oversigt over installationstrinnene.

1. **Aktivér en LBD-plads i dit LBD-projekt i Microsoft Dynamics Lifecycle Services (LCS).**

    I forhåndsversionen er LBD-edge-skaleringsenheder rettet mod eksisterende LBD-kunder. Der vil kun være en ekstra 60-dages begrænset LBD-sandkasseplads i specifikke kundesituationer.

1. **Konfigurer og implementer et LBD-miljø med en *tom* database.**

    Brug LCS til at installere LBD-miljøet med den seneste topologi og en tom database. Du kan finde flere oplysninger i afsnittet [Konfigurere og implementere et LBD-miljø med tom database](#set-up-deploy) senere i dette emne. Du skal bruge Supply Chain Management version 10.0.19 med platform update 43 eller højere på tværs af hub- og skaleringsenhedsmiljøer.

1. **Upload målpakker til LBD-projektaktiver i LCS.**

    Forbered program-, platform- og tilpasningspakker, som du bruger på tværs af hubben og edge-skaleringsenheden. Du kan finde flere oplysninger i afsnittet [Uploade målpakker til LBD-projektaktiver i LCS](#upload-packages) senere i dette emne.

1. **Servicér LBD-miljøet med målpakkerne.**

    Dette trin sikrer, at samme opbygning og tilpasninger implementeres på hubben og den nævnte skaleringsenhed. Du kan finde flere oplysninger i afsnittet [Servicere LBD-miljøet med målpakkerne](#service-target-packages) senere i dette emne.

1. **Fuldfør konfigurationen af skaleringsenheden og tildelingen af arbejdsbyrde.**

    Du kan finde flere oplysninger i afsnittet [Tildele din LBD-edge-skaleringsenhed til en hub](#assign-edge-to-hub) senere i dette emne.

De resterende afsnit i dette emne indeholder flere oplysninger om, hvordan du fuldfører hvert trin.

## <a name="set-up-and-deploy-an-lbd-environment-with-an-empty-database"></a><a name="set-up-deploy"></a>Konfigurere og implementere et LBD-miljø med en tom database

Dette trin opretter et funktionelt LBD-miljø. Men miljøet har ikke nødvendigvis samme program- og platformsversioner som hub-miljøet. Desuden mangler den stadig tilpasninger, og den er endnu ikke aktiveret til at fungere som skaleringsenhed.

1. Følg vejledningen i [Konfigurere og installere miljøer i det lokale miljø (Platform update 41 og senere)](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md). Du skal bruge Supply Chain Management version 10.0.19 med platform update 43 eller højere på tværs af hub- og skaleringsenhedsmiljøer

    > [!IMPORTANT]
    > Læs resten af dette afsnit, **før** du fuldfører trinnene i det pågældende emne.

1. Før du beskriver din konfiguration i infrastrukturens\\ConfigTemplate.xml-fil, skal du køre følgende script:

    ```powershell
    .\Configure-ScriptsForEdgeScaleUnits.ps1 -ConfigurationFilePath .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Dette script fjerner alle konfigurationer, der ikke er nødvendige ved implementering af edge-skaleringsenheder.

1. Konfigurer en database, der indeholder tomme data, som det er beskrevet i [Konfigurere databaser](../../fin-ops-core/dev-itpro/deployment/setup-deploy-on-premises-pu41.md#configuredb). Brug den tomme data.bak-fil til dette trin.
1. Konfigurer scriptet før installation. Du kan finde flere oplysninger under [Scripts til præ-installation og efterinstallation af lokale agenter](../../fin-ops-core/dev-itpro/lifecycle-services/pre-post-scripts.md).

    1. Kopier indholdet fra mappen **ScaleUnit** i **Infrastrukturscripts** til mappen **Scripts** i det share for agentfillagring, der blev konfigureret i miljøet. En typisk sti er \\\\lbdiscsi01\\agent\\Scripts.
    2. Opret scriptet **PreDeployment.ps1**, som vil kalde scriptene ved hjælp af de påkrævede parametre. Scriptet til før installation skal være lagt i **Scripts**-mappen i agentfillagerets share. Ellers kan det ikke køres. En typisk sti er \\\\lbdiscsi01\\agent\\Scripts\\PreDeployment.ps1.

        Indholdet af scriptet PreDeployment.ps1 vil ligne følgende eksempel.

        ```powershell
        $agentShare = '\\lbdiscsi01\agent'
        
        Write-Output "AgentShare is set to $agentShare" 
        & $agentShare\Scripts\Configure-CloudandEdge.ps1 -AgentShare $agentShare -InstanceId '@A' -DatabaseServer 'lbdsqla01.contoso.com' -DatabaseName 'AXDB'
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

## <a name="upload-target-packages-into-lbd-project-assets-in-lcs"></a><a name="upload-packages"></a>Uploade målpakker til LBD-projektaktiver i LCS

Dette trin forbereder programversionen, platformsversionen og tilpasninger, der vil blive oveført til dit LBD-skaleringsenhedsmiljø.

1. Upload den samme pakke med kombineret program/platform, der blev anvendt på hub-miljøet, til aktivbiblioteket i det lokale LCS-projekt.
1. Få en kopi af den tilpassede installerbare pakke, der blev anvendt på hub-miljøet, og upload den til aktivbiblioteket i det lokale LCS-projekt.

## <a name="service-the-lbd-environment-with-target-packages"></a><a name="service-target-packages"></a>Servicere LBD-miljøet med målpakkerne

Dette trin indretter programversionen, platformsversionen og tilpasninger i dit LBD-skaleringsenhedsmiljø med huppen.

1. Servicér LBD-miljøet med den kombinerede pakke med program/platform, som du uploadede i det foregående trin.
1. Servicér LBD-miljøet med den tilpassede installerbare pakke, som du uploadede i det foregående trin.

    ![Vælg Vedligehold > Anvend opdateringer i LCS.](media/cloud_edge-LBD-LCS-ServiceLBDEnv1.png "Valg af Vedligehold > Anvend opdateringer i LCS")

    ![Valg af tilpasningspakken.](media/cloud_edge-LBD-LCS-ServiceLBDEnv2.png "Valg af tilpasningspakken")

## <a name="assign-your-lbd-edge-scale-unit-to-a-hub"></a><a name="assign-edge-to-hub"></a>Tildele din LBD-edge-skaleringsenhed til en hub

Mens edge-skaleringsenheder stadig er en forhåndsversion, skal du bruge de [skalaenhedsimplementerings- og konfigurationsværktøjer](https://github.com/microsoft/SCMScaleUnitDevTools), der er tilgængelige på GitHub, til at tildele din LBD-edge-skaleringsenhed til en hub. Processen giver mulighed for, at en LBD-konfiguration kan fungere som edge-skaleringsenhed og knytte den til hubben. Processen minder om konfiguration af et udviklingsmiljø med én kasse.

1. Download den seneste version af [SCMScaleUnitDevTools](https://github.com/microsoft/SCMScaleUnitDevTools/releases), og udpak indholdet af filen.
1. Opret en kopi af filen `UserConfig.sample.xml`, og navngiv den `UserConfig.xml`.
1. Opret et Microsoft Azure Active Directory-program (Azure AD) i din Azure AD-lejer, som det er nævnt i [installationsvejledningen til skaleringsenhed og arbejdsbyrder](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#aad-application-registrations).
    1. Når det er oprettet, skal du navigere til Azure AD-programformularen (SysAADClientTable) i din hub.
    1. Opret en ny post, og angiv **Klient-id** til id'et for det program, du har oprettet. Angiv **Navn** til *ScaleUnits* og **Bruger-id** til *Admin*.

1. Opret et AD FS-program (Active Directory Federation Service), som det er nævnt i [installationsvejledningen til skaleringsenhed og arbejdsbyrder](https://github.com/microsoft/SCMScaleUnitDevTools/wiki/Step-by-step-usage-guide#adfs-application-registrations).
    1. Når det er oprettet, skal du navigere til Azure AD-programformularen (SysAADClientTable) på din edge-skaleringsenhed.
    1. Opret en ny post, og angiv **Klient-id** til id'et for det program, du har oprettet. Angiv **Bruger-id** til *Admin*.

1. Rediger `UserConfig.xml`-filen.
    1. Angiv oplysningerne fra det Azure AD-program, du tidligere har oprettet, under afsnittet `InterAOSAADConfiguration`.
        - Angiv program-id'et for Azure-programmet i elementet `AppId`.
        - Angiv programhemmeligheden for Azure-programmet i elementet `AppSecret`.
        - Elementet `Authority` skal indeholde URL-adressen, der angiver sikkerhedsmyndigheden for din lejer.

        ```xml
        <InterAOSAADConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopty56TGUedDTVhtER-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </InterAOSAADConfiguration>
        ```

    1. Under afsnittet `ScaleUnitConfiguration` skal du for den første `ScaleUnitInstance` redigere afsnittet `AuthConfiguration`.
        - Angiv program-id'et for Azure-programmet i elementet `AppId`.
        - Angiv programhemmeligheden for Azure-programmet i elementet `AppSecret`.
        - Elementet `Authority` skal indeholde URL-adressen, der angiver sikkerhedsmyndigheden for din lejer.

        ```xml
        <AuthConfiguration>
            <AppId>8dab14f6-97b1-48e3-b51b-350b45f6ede5</AppId>
            <AppSecret>k6em-_7.lopdz.6d3DTVOtf9Lo-j_6anY1</AppSecret>
            <Authority>https://login.windows.net/contoso.onmicrosoft.com</Authority>
        </AuthConfiguration>
        ```

    1. Angiv også følgende værdier for den samme `ScaleUnitInstance`:
        - Angiv URL-adressen for din hub i elementet `Domain`. For eksempel: `https://cloudhub.sandbox.operations.dynamics.com/`
        - Kontrollér, at værdien `LCSHosted` er angivet i elementet `EnvironmentType`.

    1. Under afsnittet `ScaleUnitConfiguration` skal du for den anden `ScaleUnitInstance` redigere afsnittet `AuthConfiguration`.
        - Angiv program-id'et for AD FS-programmet i elementet `AppId`.
        - Angiv programhemmeligheden for ADFS-programmet i elementet `AppSecret`.
        - Elementet `Authority` skal indeholde URL-adressen til din AD FS-forekomst.

        ```xml
        <AuthConfiguration>
            <AppId>26b16f25-21d8-4d36-987b-62df292895aa</AppId>
            <AppSecret>iZFfObgI6lLtY9kEbBjEFV98NqI5_YZ0e5SBcWER</AppSecret>
            <Authority>https://adfs.contoso.com/adfs</Authority>
        </AuthConfiguration>
        ```

    1. Angiv også følgende værdier for den samme `ScaleUnitInstance`:
        - Angiv URL-adressen for din edge-skaleringsenhed i elementet `Domain`. For eksempel: https://ax.contoso.com/
        - Kontrollér, at værdien LDB er angivet i elementet `EnvironmentType`.
        - I elementet `ScaleUnitId` skal du angive den samme værdi, som du angav for `InstanceId`, da du konfigurerede `Configure-CloudandEdge.ps1`-scriptet før installationen.

        > [!NOTE]
        > Hvis du ikke bruger standard-id'et (@A), skal du opdatere ScaleUnitId for hver ConfiguredWorkload under sektionen Arbejdsbyrder.

1. Åbn PowerShell, og naviger til mappen, der indeholder filen `UserConfig.xml`.

1. Kør værktøjet med denne kommando.

    ```powershell
    .\CLI.exe
    ```

    > [!NOTE]
    > Efter hver handling skal du starte værktøjet igen.

1. Vælg **2. Forbered miljøer til installation af arbejdsbyrde** i værktøjet. Kør derefter følgende trin:
    1. Vælg **1. Forbered hubben**.
    1. Vælg **2. Forbered skaleringsenheden**.

    > [!NOTE]
    > Hvis du ikke kører denne kommando fra en ren installation, og den mislykkes, skal du udføre følgende handlinger:
    >
    > - Fjern alle mapper fra mappen `aos-storage` (undtagen for `GACAssemblies`).
    > - Kør følgende SQL-kommando i din virksomhedsdatabasen (AXDB):
    >
    > ```sql 
    > delete from storagefoler
    > ```

1. Kør følgende SQL-kommandoer i din virksomhedsdatabasen (AXDB):

    ```sql
    delete from FEATUREMANAGEMENTMETADATA
    delete from FEATUREMANAGEMENTSTATE
    delete from NUMBERSEQUENCESCOPE
    ```

1. Kontrollér, at sporing af ændringer er aktiveret i din virksomhedsdatabase (AXDB)
    1. Start SQL Server Management Studio (SSMS).
    1. Højreklik på din virksomhedsdatabase (AXDB), og vælg egenskaber.
    1. Vælg **Ændringssporing** i det vindue, der åbnes, og foretag følgende indstillinger:

        - **Ændringssporing:** *Sand*
        - **Opbevaringsperiode:** *7*
        - **Opbevaringsenheder:** *Dage*
        - **Automatisk oprydning:** *Sand*

1. Vælg **3. Installer arbejdsbyrder** i værktøjet. Kør derefter følgende trin:
    1. Vælg **1. Installer på hub**.
    1. Vælg **2. Installer på skaleringsenhed**.

[!INCLUDE [cloud-edge-privacy-notice](../../includes/cloud-edge-privacy-notice.md)]

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
