---
title: Konfigurere og installere selvstudium til Regression Suite Automation Tool
description: Dette emne er et selvstudium, der viser, hvordan du kan konfigurere og installere Regression Suite Automation Tool (RSAT).
author: robinarh
manager: AnnBe
ms.date: 09/20/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ROBOTS: NOINDEX, NOFOLLOW
audience: Application User, Developer, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: 21761, NotInToc
ms.search.region: Global
ms.author: rhaertle
ms.search.validFrom: 2019-05-30
ms.dyn365.ops.version: AX 7.0.0, Operations
ms.openlocfilehash: f5670f6a580249491ad16ae46470160545bb8f91
ms.sourcegitcommit: 4fdee254649a751d46632fb4d0d48698e112fa72
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/08/2020
ms.locfileid: "3248707"
---
# <a name="set-up-and-install-regression-suite-automation-tool-tutorial"></a>Konfigurere og installere selvstudium til Regression Suite Automation Tool
Dette emne er et selvstudium, der hjælper dig med konfigurere og komme i gang med RSAT og de værktøjer, der er knyttet til brugen af RSAT. 

[!include [banner](../includes/banner.md)]

> [!NOTE]
> Brug dine internetbrowserværktøjer til at downloade og gemme denne side i PDF-format. 

## <a name="key-concepts"></a>Nøglebegreber

- Forstå den opsætning af installation og forudsætning , der kræves til de forskellige programmer, som understøtter Regression Suite Automation Tool (RSAT).
- Forstå, hvordan du kan bruge funktionen Arbejdsrutineoptager sammen med Microsoft Dynamics Lifecycle Services (LCS) og Microsoft Azure DevOps til at oprette, konfigurere, køre, undersøge og rapportere om testsager.
- Giv funktionelle brugere mulighed for at registrere forretningsopgaver ved hjælp af Arbejdsrutineoptager og derefter konvertere opgaveregistreringerne til en pakke af automatiske test uden at skulle skrive kildekode.

## <a name="before-you-begin"></a>Før du begynder

### <a name="prerequisites"></a>Forudsætninger

- Der kræves et miljø, der kører Microsoft Dynamics 365 for Finance and Operations version 10.0 (april 2019) eller nyere, til dette selvstudium. For kunder, der bruger Microsoft Dynamics 365 for Finance and Operations Enterprise Edition 7.3, er Platform update 20 (PU20) eller nyere også understøttet.
- Brugeren skal have administratorrettigheder til miljøet.
- Du skal have adgang til kundens lejer-LCS og Azure DevOps (tidligere kaldet Microsoft Visual Studio Team Services \[VSTS\]).
- Den bruger, der opretter og administrerer testpakker, skal have licens til Azure DevOps Test Plans eller Test Manager. Følgende licenser giver dig også adgang til Test Plans:
    - Visual Studio Enterprise-licens
    - Visual Studio Test Professional-licens
    - Abonnementslicens til MSDN-platforme
- RSAT skal have adgang til testmiljøet via en webbrowser.
- Hvis du vil generere og redigere testparametre, skal du have Microsoft Excel installeret.

## <a name="configure-azure-devops"></a>Konfigurer Azure DevOps

### <a name="user-eligibility"></a>Brugerberettigelse

Sørg for, at brugeren er oprettet i Azure DevOps og har et abonnementsniveau, der giver adgang til Azure Test Plans. Der kræves kun en licens til Azure DevOps Test Plans, hvis brugeren opretter og administrerer testsager (så ikke alle RSAT-brugere kræver denne licens). Oplysninger om licenskravene finder du under [Licenskrav](https://docs.microsoft.com/azure/devops/test/manual-test-permissions#license-requirements).

### <a name="create-a-new-azure-devops-project"></a>Opret et nyt Azure DevOps-projekt
RSAT bruger Azure Devops til styring af testsager og testpakker, rapportering og undersøgelse af testkørselsresultater. 

> [!NOTE]
> Du kan bruge et eksisterende Azure DevOps-projekt. Men hvis det eksisterende Azure DevOps-projekt er konfigureret, så det har en brugerdefineret skabelon, får du vist en "VSTS-synkroniseringsfejl", når du synkroniserer testsager fra Forretningsmodeldesigner (BPM) til Azure DevOps (se afsnittet [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops)). Hvis følgende bedste fremgangsmåder er blevet fulgt for den brugerdefinerede skabelon, kan du synkronisere testsagerne til Azure DevOps. (Disse bedste fremgangsmåder vises i fejlmeddelelsen).

- Slet ikke nogen arbejdselementtyper eller indbyggede felter.
- Slet ikke nogen tilstand af en arbejdselementtype.
- Føj ikke nogen påkrævede felter til en arbejdselementtype.

![Fejlmeddelelse med en liste over bedste fremgangsmåder](./media/setup_rsa_tool_02.png)

For dette selvstudium anbefales det ellers, at du opretter et nyt Azure DevOps-projekt. Yderligere oplysninger finder du under [Problemer under synkronisering af BPM ved at bruge en brugerdefineret Azure DevOps-processkabelon (VSTS)](https://blogs.msdn.microsoft.com/lcs/2018/11/28/issues-when-syncing-to-bpm-using-a-custom-azure-devops-vsts-process-template/).

1. Åbn Azure DevOps-URL-adressen (`https://dev.azure.com/<Azure DevOps Name>`).
2. Vælg **Opret projekt** i øverste højre hjørne af Azure DevOps-siden.

    ![Knappen Opret projekt](./media/setup_rsa_tool_03.png)

3. Udfyld følgende felter, og vælg derefter **Opret**:

    - **Projektnavn**
    - **Versionskontrol** – Vælg **Team Foundation Version Control**. Bemærk, at standardindstillingen, **Git**, ikke understøttes.
    - **Arbejdselementproces**

    ![Dialogboksen Opret nyt projekt](./media/setup_rsa_tool_04.png)

### <a name="create-a-personal-access-token"></a>Oprette et token for personlig adgang

I dette selvstudium skal du bruge LCS som Forretningsmodeldesigner (BPM) til at oprette et testsagsbibliotek og synkronisere testsagerne med Azure DevOps. Du skal bruge et personligt adgangstoken for at synkronisere BPM med Azure DevOps.

1. Vælg profilikonet i øverste højre hjørne af siden til Azure DevOps-projektet, og vælg derefter **Sikkerhed**.

    ![Kommandoen Sikkerhed](./media/setup_rsa_tool_05.png)

2. Vælg **Tokens for personlig adgang** under **Sikkerhed** i ruden til venstre. Vælg derefter **Nyt token**.

    ![Knappen Nyt token under fanen Tokens for personlig adgang i Brugerindstillinger](./media/setup_rsa_tool_06.png)

3. Udfyld følgende felter, og vælg derefter **Opret**:

    - **Navn**
    - **Udløb (UTC)** – Vælg **Brugerdefineret**, og brug derefter datovælgeren til at vælge den seneste tilgængelige dato.
    - **Områder** – Vælg indstillingen **Fuld adgang**.

    ![Dialogboksen Opret et nyt personligt adgangstoken](./media/setup_rsa_tool_07.png)

    > [!NOTE]
    > Noter det personlige adgangstoken, der oprettes. Du skal bruge det senere, når du opretter RSAT-konfigurationen.

    ![Token for personlig adgang](./media/setup_rsa_tool_08.png)

## <a name="configure-the-lcs-project"></a>Konfigurere LCS-projektet

Du skal bruge et LCS-projekt (Lifecycle Services) til mastertestbiblioteket. LCS Forretningsmodeldesigner (BPM) bruges som masterbibliotek for testsagerne. BPM bruges til at administrere og distribuere testbiblioteker på tværs af LCS-projekter. En Microsoft-partner eller en uafhængig softwareleverandør (ISV), der f.eks. bygger testsager, skal frigive testsagerne i form af BPM-biblioteker. I BPM er testsager organiseret efter forretningsproces. BPM definerer ikke udførelsesrækkefølgen eller hyppigheden af testforløb. Disse detaljer styres i Azure DevOps, som beskrevet senere i dette emne.  

Til dit LCS-projekt kan du bruge et eksisterende kundeimplementerings- eller partnerprojekt.

### <a name="update-the-lcs-language"></a>Opdatere LCS-sproget

> [!NOTE]
> For at få brugergrænsefladen (UI) til at vise forretningsprocesser korrekt skal det foretrukne LCS-sprog indstilles til **Engelsk (USA)**.

1. Gå til LCS-implementeringsprojektet.
2. Vælg knappen **Indstillinger** (tandhjulssymbolet) i øverste højre hjørne af siden, og vælg dernæst **Foretrukket sprog**.

    ![Kommandoer i menuen Indstillinger](./media/setup_rsa_tool_09.png)

3. Vælg **Engelsk (USA)** i feltet **Foretrukket sprog**, og vælg derefter **Gem**.

    ![Fanen Foretrukket sprog i Brugerindstillinger](./media/setup_rsa_tool_10.png)

### <a name="configure-lcs-to-connect-to-the-azure-devops-project"></a>Konfigurere LCS til at oprette forbindelse til Azure DevOps-projektet

Hvis du tidligere har oprettet et nyt Azure DevOps-projekt, skal du konfigurere LCS-projektet til at oprette forbindelse til det. Ellers kan du fortsætte til næste afsnit, hvis dit LCS-projekt allerede er forbundet med Azure DevOps-projektet.

1. Gå til LCS-implementeringsprojektet.
2. Vælg knappen **Menu**, og vælg derefter **Projektindstillinger**.

    ![Kommandoen Projektindstillinger](./media/setup_rsa_tool_11.png)

3. Vælg **Visual Studio Team Services** i ruden til venstre, og vælg derefter **Konfigurer Visual Studio Team Services**.

    ![Fanen Visual Studio Team Services i Projektindstillinger](./media/setup_rsa_tool_12.png)

4. Brug feltet **URL-adresse til Azure DevOps-websted** til at angive URL-adressen til Azure DevOps-webstedet. Angiv det personlige adgangstoken, der blev oprettet tidligere, i feltet **Token for personlig adgang**.

    > [!NOTE]
    > Selvom VSTS nu kaldes Azure DevOps skal du bruge den gamle URL-adresse til at knytte LCS til dit Azure DevOps-projekt. Den Azure DevOps-URL-adresse, der bruges i dette selvstudium, er f.eks `https://dev.azure.com/D365FOFastTrack/`. Men på følgende illustration angives den som `https://D365FOFastTrack.visualstudio.com/`.

    ![Trin 1 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_13.png)

5. Vælg **Fortsæt**.
6. Vælg VSTS-projektet på det valgte websted, som skal knyttes til LCS-projektet, i feltet **Visual Studio Team Services-projekt**. Feltet **Processkabelon** er som standard indstillet til **Agile**. Du kan se en brugerdefineret skabelon i vejledningen til Best Practice i afsnittet [Oprette et nyt Azure DevOps-projekt](#create-a-new-azure-devops-project). Vælg derefter **Fortsæt**.

    ![Trin 2 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_14.png)

7. Gennemse indstillingerne, og vælg derefter **Gem**.

    ![Trin 3 i Konfigurer Visual Studio Team Services](./media/setup_rsa_tool_15.png)

8. Vælg **Godkend** for at godkende LCS-adgang til det konfigurerede Azure DevOps-websted på dine vegne og for at aktivere funktioner, der kan integreres med VSTS.

    ![Knappen Godkend](./media/setup_rsa_tool_16.png)

9. Der vises en meddelelsesboks med teksten "Du er ved at blive omdirigeret til et eksternt websted for at give LCS tilladelse til at oprette forbindelse til Visual Studio Team Services på dine vegne. Vil du fortsætte?" Vælg **Ja**.

    ![Meddelelsesboks](./media/setup_rsa_tool_17.png)

10. Vælg **Accepter**.

    ![Godkende adgang](./media/setup_rsa_tool_18.png)

11. Hvis du er godkendt som bruger, skal brugergrænsefladen vende tilbage til siden med projektindstillinger til LCS.

    ![Godkendt bruger](./media/setup_rsa_tool_19.png)

### <a name="create-a-new-bpm-library"></a>Oprette et nyt BPM-bibliotek

1. Gå til LCS-implementeringsprojektet.
2. Vælg knappen **Menu**, og vælg derefter **Forretningsmodeldesigner**.

    ![Kommandoen Forretningsmodeldesigner](./media/setup_rsa_tool_20.png)

3. Vælg **Nyt bibliotek**.

    ![Knappen Nyt bibliotek](./media/setup_rsa_tool_21.png)

4. Angiv et navn i feltet **Biblioteksnavn**, og vælg derefter **Opret**. Til dette selvstudium skal du navngive BPM-biblioteket **RSAT**.

    ![Dialogboksen Opret nyt bibliotek](./media/setup_rsa_tool_22.png)

5. Åbn det nye **RSAT** BPM-bibliotek.
6. Vælg eksempelprocessen **Kerneforretningsprocesser**, og vælg derefter **Redigeringstilstand** i højre side.

    ![Knappen Redigeringstilstand](./media/setup_rsa_tool_23.png)

7. Rediger værdien i både feltet **Navn** og feltet **Beskrivelse** til **Opret et produkt**. Vælg derefter **Gem**.

    ![Felterne Navn og Beskrivelse](./media/setup_rsa_tool_24.png)

## <a name="environment"></a>Miljø

### <a name="version-requirement"></a>Versionskrav

Der kræves et test- eller sandkassemiljø, som kører version 10. For kunder, der bruger version 7.3, er Platform update 20 eller nyere også understøttet.

> [!NOTE]
> RSAT skal have adgang til testmiljøet via en webbrowser.

### <a name="user-criteria"></a>Brugerkriterier

Brugeren skal have administratorrettigheder til dette miljø.

### <a name="set-up-help-settings-to-connect-with-lcs"></a>Konfigurere indstillinger for hjælp til at oprette forbindelse til LCS

Dette trin er nødvendigt for at oprette forbindelse til LCS, så opgaveregistreringer kan gemmes i det relevante BPM-bibliotek i LCS via klienten.

1. Åbn klienten.
2. Gå til **Systemadministration \> Opsætning \> Systemparametre**.
3. Vælg det relevante LCS projekt (**RSAT** til dette selvstudium) i feltet **Konfiguration af hjælp til Lifecycle Services** under fanen **Hjælp**.

    ![Feltet Konfiguration af hjælp til Lifecycle Services under fanen Hjælp](./media/setup_rsa_tool_25.png)

    BPM-biblioteker udfyldes under det relevante LCS-projekt.

4. Vælg **Gem**.
5. Du skal muligvis opdatere browseren for at få vist det opdaterede Hjælp-indhold.

    ![Besked om opdatering af browseren](./media/setup_rsa_tool_26.png)

## <a name="task-recordings"></a>Opgaveregistreringer

> [!NOTE]
> Sørg for, at alle opgaveregistreringer starter på det primære dashboard. Sørg for, at de enkelte poster er korte, og fokusér på én forretningsopgave, f.eks. oprettelse af en salgsordre.

### <a name="create-a-task-recording-and-save-it-to-the-bpm-library"></a>Oprette en opgaveregistrering og gemme den i BPM-biblioteket

Opret en tilsvarende opgaveregistrering, som du kan knytte til den simple forretningsproces, der blev oprettet i det nye BPM-bibliotek.

1. Åbn klienten.
2. I hoveddashboardet skal du vælge knappen **Indstillinger** (tandhjulsymbolet) og derefter vælge **Arbejdsrutineoptager**.

    ![Kommandoer i menuen Indstillinger](./media/setup_rsa_tool_27.png)

3. Vælg **Opret registrering**.

    ![Knappen Opret registrering](./media/setup_rsa_tool_28.png)

4. Udfyld felterne **Registreringsnavn** og **Beskrivelse af registrering**, og vælg derefter **Start**.

    ![Felterne Registreringsnavn og Beskrivelse af registrering](./media/setup_rsa_tool_29.png)

5. Registrer trinnene til oprettelse af et produkt. Når du er færdig, skal du vælge **Stop** for at stoppe registreringen.

    ![Trin til oprettelse af et produkt](./media/setup_rsa_tool_30.png)

6. Vælg **Gem i Lifecycle Services**.

    ![Indstillinger for Gem](./media/setup_rsa_tool_31.png)

    Biblioteksoplysninger indlæses fra LCS.

    ![Statusindikator](./media/setup_rsa_tool_32.png)

7. Vælg det BPM-bibliotek, der skal knyttes til opgaveregistreringen. I dette selvstudium skal du vælge det BPM-bibliotek **RSAT**, der blev oprettet tidligere, og **Opret et produkt** som forretningsproces under det. Vælg derefter **OK**.

    ![Tilknytning af opgaveregistrering med et BPM-bibliotek og en forretningsproces](./media/setup_rsa_tool_33.png)

    Meddelelsen "Blev gemt i Lifecycle Services" vises.

    ![Meddelelse om en vellykket lagring i LCS](./media/setup_rsa_tool_34.png)

8. Hvis du vil gemme opgaveregistreringen lokalt og derefter overføre den til BPM via LCS, skal du følge disse trin:

    1. Vælg **Gem på denne pc**, når registreringen er fuldført.

        ![Indstillinger for Gem](./media/setup_rsa_tool_35.png)

    2. På meddelelseslinjen i browseren skal du vælge **Gem** eller **Gem som** for at gemme filen på din lokale computer.

        ![Meddelelseslinje](./media/setup_rsa_tool_36.png)

    3. Gå til BPM-biblioteket **RSAT**, og vælg den forretningsproces, hvor opgaveregistreringen skal gemmes.
    4. Vælg **Overfør** under fanen **Oversigt**.

        ![Knappen Overfør](./media/setup_rsa_tool_37.png)

    5. Vælg **Gennemse**, og vælg den. axtr-fil, du gemte tidligere. Vælg derefter **Overfør**.

        ![Vælg den. axtr-fil, der skal overføres](./media/setup_rsa_tool_38.png)

### <a name="test-the-synchronization-from-bpm-to-azure-devops"></a>Teste synkroniseringen fra BPM til Azure DevOps

Nu, hvor en opgaveregistrering er knyttet til forretningsprocessen, skal du validere, at forretningsprocessen og den tilknyttede opgaveregistrering kan synkroniseres til Azure DevOps som en funktion og en testsag (henholdsvist) ved hjælp af synkroniseringsfunktionen VSTS i LCS.

> [!NOTE]
> Den tilsvarende arbejdselementtype, der oprettes i Azure DevOps, varierer, afhængigt af den processkabelon du valgte, da du konfigurerede LCS-projektet med Azure DevOps, som beskrevet i afsnittet [Oprette et nyt Azure DevOps-projekt](#create-a-new-azure-devops-project).

1. Gå til BPM-biblioteket, og åbn det **RSAT**-bibliotek, du har oprettet tidligere.
2. Vælg ellipseknappen (**...**), og vælg **VSTS-synkronisering**.

    ![VSTS-synkroniseringskommando i ellipsemenuen](./media/setup_rsa_tool_39.png)

    Når VSTS-synkronisering er fuldført, vises fanen **Krav** i venstre side og omfatter det tilsvarende Azure DevOps-arbejdselement.

    > [!NOTE]
    > Der arbejdselement, der oprettes i Azure DevOps, vil have BPM-biblioteksnavnet som titelpræfiks.

    ![Fanen Krav](./media/setup_rsa_tool_40.png)

3. Opdater siden.
4. Vælg ellipseknappen (**...**). Du vil se en ekstra indstilling, **Synkroniser testsager**. Vælg denne indstilling.

    ![Kommandoen Synkroniser testsager i ellipsemenuen](./media/setup_rsa_tool_41.png)

    > [!NOTE]
    > Hvis indstillingen **Synkroniser testsager** ikke er tilgængelig, efter at du har opdateret siden, skal du gå til hovedsiden for BPM og vælge **Synkroniser testsager** for hele biblioteket. På denne måde gennemtvinger du effektivt en synkronisering af hele biblioteket.
    > 
    > ![Vælge synkronisering af testsager for hele biblioteket](./media/setup_rsa_tool_42.png)

    Når synkroniseringen af testsager er fuldført, oprettes der en ny testsag under fanen **Krav**.

    ![Ny testsag under fanen Krav](./media/setup_rsa_tool_43.png)

5. Gå til dit Azure DevOps-projekt, og vælg **Tavler \> Workflowopgaver**.

    ![Kommandoen Workflowopgaver under Tavler](./media/setup_rsa_tool_44.png)

6. Valider, at den workflowopgave og den testsag, du har oprettet via BPM-synkronisering, findes.

    ![Workflowopgave og testsag](./media/setup_rsa_tool_45.png)

## <a name="install-and-configure-rsat"></a>Installere og konfigurere RSAT

RSAT kan installeres på en hvilken som helst computer, der kører Windows 10, og som kan oprette forbindelse til miljøet via en webbrowser (Internet Explorer eller Google Chrome).

> [!NOTE]
> Før du installerer en ny version af værktøjet, anbefales du at fjerne den tidligere version.

### <a name="install-an-authentication-certificate"></a>Installere et godkendelsescertifikat

Hvis du vil aktivere godkendelse, skal du generere og installere et certifikat på den computer, som RSAT kører på.

#### <a name="generate-a-certificate"></a>Generere et nyt certifikat

1. Hvis du vil oprette en certifikatfil, skal du åbne et Microsoft Windows PowerShell-vindue som administrator og derefter køre følgende kommando.

    ```
    $certificate = New-SelfSignedCertificate -dnsname 127.0.0.1 -CertStoreLocation cert:\LocalMachine\My -FriendlyName "D365 Automated testing certificate" -Provider "Microsoft Strong Cryptographic Provider"
    ```

2. Åbn certifikatstyring ved at indtaste **certlm.msc** i dialogboksen **Kør**, og bekræft, at **Certifikat til automatisk afprøvning af D365** er oprettet under **Personlige \> certifikater**.

    > [!NOTE]
    > Sørg for at angive **certlm.msc**, ikke **certmgr.msc**, da certifikaterne er gemt på den lokale computer.

    ![Certifikat for D365-automatiseret testcertifikat](./media/setup_rsa_tool_46.png)

3. Højreklik på certifikatet, og vælg derefter **Kopier**.
4. Gå til **Rodnøglecentre, der er tillid til \> Certifikater**.

    ![Mappen Certifikater under mappen Rodnøglecentre, der er tillid til](./media/setup_rsa_tool_47.png)

5. Vælg **Sæt ind** i menuen **Handling** for at kopiere certifikatet til placeringen af **Rodnøglecentre, der er tillid til**.

    ![Kommandoen Sæt ind i menuen Handling](./media/setup_rsa_tool_48.png)

6. Hvis du vil hente et aftryk af det installerede certifikat uden mellemrum eller specialtegn, skal du åbne et Windows PowerShell-vindue som administrator og køre følgende kommandoer.

    ```
    cd Cert:\LocalMachine\My

    Get-ChildItem | Where-Object { $_.Subject -like "CN=127.0.0.1" }
    ```

    > [!NOTE]
    > Gem aftrykket, da du senere skal bruge det, når du opdaterer .wif-filerne til Applikationsobjektserver (AOS) og opretter konfigurationen af RSAT.

#### <a name="configure-the-aos-computer-to-trust-the-connection"></a>Konfigurere AOS-computeren til at vise tillid til forbindelsen

> [!NOTE]
> Hvis miljøet er et niveau 2+-miljø, skal certifikataftrykket opdateres i filen wif.config for **alle** AOS-computere for miljøet.

1. Opret en RDP-forbindelse (Remote Desktop Protocol) til AOS-computeren. Logonoplysninger er tilgængelige på siden med miljødetaljer i LCS.
2. Åbn Microsoft IIS (Internet Information Services), og find **AOSService** på listen over websteder.

    ![AOSService på listen over websteder](./media/setup_rsa_tool_49.png)

3. Højreklik på **Stifinder** for at åbne mappen **\<Drev\>: \\AosService\\WebRoot**. Find filen **wif.config**.

    ![Filen wif.config i mappen WebRoot](./media/setup_rsa_tool_50.png)

4. Opdater filen **wif.config** ved at tilføje en ny myndighedspost for certifikatet og navnet på myndigheden, som vist i følgende eksempel.

    ```
    <issuerNameRegistry type="Microsoft.Dynamics.AX.Security.SharedUtility.AxIssuerNameRegistry,Microsoft.Dynamics.AX.Security.SharedUtility">
        <authority name="CN=127.0.0.1">
            <keys>
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
                <add thumbprint="xxxxxxxxxxxxxxxxxxxx" />
            </keys>
            <validIssuers>
                <add name="CN=127.0.0.1" />
            </validIssuers>
        </authority>
    ```

    > [!NOTE]
    > Hvis flere brugere benytter samme program, skal hver bruger oprette separate aftryk, og hvert af disse aftryk skal tilføjes i sektionen **\<nøgler\>**.

5. Hvis der er mere end én AOS-computer, skal du gentage trin 3 til 4 for hver ekstra computer.

    > [!NOTE]
    > I modsætning til ældre niveau 2-miljøer installeres nye niveau 2-miljøer med to forekomster af AOS.

6. Kør **iisreset** på alle AOS-computere.

    > [!NOTE]
    > Hvis du ikke har administratorrettigheder til at køre **iisreset** på en computer med niveau 1, skal du vælge Vedligehold > Genstart tjenester på siden med miljødetaljer i LCS.

#### <a name="tier-2-environment"></a>Miljø på niveau 2

Hvis der bruges et niveau 2+-miljø (Sandkasse: Standardgodkendelsestest eller højere), skal du kontrollere eller angive følgende indstilling i registreringsdatabasen på den computer, hvor RSAT er installeret. Dette trin er påkrævet, fordi det hjælper dig med at undgå godkendelses- eller RSAT-forbindelsesfejl.

```
if ((Test-Path HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319))
{
    Set-ItemProperty HKLM:\SOFTWARE\Wow6432Node\Microsoft\.NETFramework\v4.0.30319 -Name SchUseStrongCrypto -Value 1 -Type dword -Force -Confirm:$false
}
```

### <a name="install-rsat"></a>Installere RSAT

1. Gå til <https://www.microsoft.com/download/details.aspx?id=57357>, og vælg **Download**.
2. Vælg alle filerne, og vælg derefter **Næste**.

    ![Vælge alle filer](./media/setup_rsa_tool_51.png)

3. Dobbeltklik på .msi-pakken for at køre installationsprogrammet. Vælg **Udfør**, når installationen er fuldført.

    ![RSAT-installationsprogramfil](./media/setup_rsa_tool_52.png)

### <a name="install-selenium-and-browser-drivers"></a>Installere Selenium- og browserdrivere

I ældre versioner af RSAT skulle du installere Selenium- og browserdrivere. Du behøver ikke længere at installere disse drivere, fordi de installeres automatisk.

1. Første gang du åbner RSAT, bliver du bedt om automatisk at downloade og installere Selenium. Du kan finde flere oplysninger i afsnittet [Konfigurere RSAT](#configure-rsat).
2. Før du kan køre en testsag, bliver du bedt om automatisk at hente og installere den browserdriver, der svarer til den standardbrowser, der er valgt i RSAT-konfigurationen. Du kan finde flere oplysninger i afsnittet [Indlæse og køre testsager](#load-and-run-test-cases).

## <a name="get-started-with-rsat"></a>Kom i gang med RSAT

### <a name="create-a-test-plan-and-test-suites"></a>Oprette en testplan og testpakker

1. Gå til Azure DevOps-projektet, og vælg **Testplaner**.

    ![Kommandoen Testplaner](./media/setup_rsa_tool_53.png)

2. Vælg **Ny testplan**.

    ![Knappen Ny testplan](./media/setup_rsa_tool_54.png)

3. Udfyld feltet **Navn**, og vælg derefter **Opret**. Til dette selvstudium skal du navngive testplanen **RSAT-testplan**.

    ![Dialogboksen Ny testplan](./media/setup_rsa_tool_55.png)

4. Vælg plustegnet (**+**), og vælg derefter **Statisk pakke** for at oprette en statisk pakke under den nye testplan. Navngiv den nye testpakke **T01 – Fremstilling til lager**.

    > [!NOTE]
    > Du kan også oprette en forespørgselsbaseret pakke, hvis de nye testsager fra BPM ikke automatisk skal trækkes ind i RSAT-testpakken.

    ![Oprettelse af en statisk pakke](./media/setup_rsa_tool_56.png)

### <a name="attach-test-cases-to-test-suites"></a>Knytte testsager til testpakker

1. Vælg **Tilføj eksisterende** i højre side for at føje eksisterende testsager til testpakken.

    ![Knappen Tilføj eksisterende](./media/setup_rsa_tool_57.png)

2. På siden **Føj testsager til pakke** skal du vælge **Kør forespørgsel**og derefter vælge den testsag, der skal føjes til testpakken. I dette selvstudium skal du vælge **Opret et nyt produkt** som testsag. Vælg derefter **Tilføj testsager** i nederste højre hjørne af siden (denne knap vises ikke i følgende illustration).

    ![Knappen Kør forespørgsel](./media/setup_rsa_tool_58.png)

    Testsagen føjes til testpakken **T01-Fremstilling til lager**.

    ![Testsag, der er føjet til testpakken](./media/setup_rsa_tool_59.png)

### <a name="configure-rsat"></a>Konfigurer RSAT

1. Åbn RSAT.

    ![RSAT-ikon](./media/setup_rsa_tool_60.png)

2. Du får vist advarselsmeddelelsen "Regression Suite Automation Tool kræver Selenium. Vil du automatisk hente og installere det nu?" Vælg **Ja**.

    ![Advarselsmeddelelse](./media/setup_rsa_tool_61.png)

3. Klik på knappen **Indstillinger** (tandhjulsymbolet) i øverste højre hjørne, og udfyld derefter følgende felter i den dialogboks, der vises:

    - **URL-adresse til Azure DevOps** – Angiv URL-adressen til dit Azure DevOps-projekt, f.eks `https://yourAzureDevOpsUrlHere.visualStudio.com`.
    - **Adgangstoken** – Angiv det adgangstoken, der giver værktøjet mulighed for at oprette forbindelse til Azure DevOps. Brug det personlige adgangstoken, som du oprettede tidligere i dette selvstudium. Yderligere oplysninger finder du under [Godkende adgang med personlige adgangstokens](https://www.visualstudio.com/docs/setup-admin/team-services/use-personal-access-tokens-to-authenticate).
    - **Projektnavn** – Vælg navnet på dit Azure DevOps-projekt.
    - **Testplan** – Vælg den Azure DevOps-testplan, der indeholder dine testsager. Du kan finde flere oplysninger under [Oprette testplaner og testpakker](https://www.visualstudio.com/docs/test/manual-exploratory-testing/getting-started/create-a-test-plan). Når du har valgt en testplan, skal du vælge **Test forbindelse** for at teste forbindelsen til Azure DevOps.
    - **Værtsnavn** – Angiv værtsnavnet på testmiljøet, f.eks. **\<myaos\>.cloudax.dynamics.com**. Du skal ikke medtage præfikset **https://** eller **http://**.
    - **SOAP-værtsnavn** – Angiv SOAP-værtsnavnet for testmiljøet. SOAP-værtsnavnet er typisk det samme som værtsnavnet, men har et **soap**-suffiks. Her er et eksempel: **\<myaos\>soap.cloudax.dynamics.com**. Du skal ikke medtage præfikset **https://** eller **http://**.

        > [!NOTE]
        > Hvis du vil finde værtsnavnet og SOAP-værtsnavnet, skal du åbne IIS Manager, højreklikke på **Websteder \> AOSService** og derefter vælge **Rediger bindinger**. Værdierne i kolonnen **Værtsnavn** giver dig værtsnavnet og SOAP-værtsnavnet (SOAP-værtsnavnet har suffikset **soap** i URL-adressen).

        ![Værtsnavn og SOAP-værtsnavn i kolonnen Værtsnavn](./media/setup_rsa_tool_63.png)

    - **Administratorbrugernavn** – Angiv mailadressen på en administratorbruger i testmiljøet.
    - **Aftryk** – Angiv aftrykket på godkendelsescertifikatet som beskrevet tidligere i dette selvstudium.
    - **Arbejdsmappe** – Angiv mappeplaceringen til lagring af automatiserede testfiler, f.eks. Excel-testdatafiler. Angiv eller vælg f.eks. **C:\\Temp\\RegressionTool**.

        > [!NOTE]
        > Hvis navnet på mappen har mellemrum, mislykkes udførelsen, fordi mappen ikke blev fundet. Dette problem er et kendt problem, som skulle være rettet i den seneste version af værktøjet.

    - **Standardbrowser** – Vælg enten **Internet Explorer** eller **Google Chrome**. Sørg for, at de relevante browserdrivere er installeret.
    - **Timeout for testkørsel** – Angiv timeoutperioden i minutter for testkørsler. Når timeoutperioden udløber, lukkes alle aktive vinduer, og ventende testsager mislykkes.
    - **Timeout for testhandling** – Dette felt kontrollerer timeoutperioden i minutter for Finance and Operations-miljøets serveranmodninger. Normalt skal standardværdien (2 minutter) være tilstrækkelig. Men i langsomme miljøer kan det være en god idé at øge værdien, hvis der opstår fejl, der er relateret til timeout.
    - **Firmanavn** – Angiv det firmanavn, der skal bruges som standardfirma, når Excel-parameterfiler oprettes. Du kan ændre firmaet senere ved at redigere Excel-parameterfilen.

    ![Dialogboksen Indstillinger](./media/setup_rsa_tool_62.png)

4. Vælg **Anvend** for at anvende og gemme dine indstillinger.

    Hvis du vil gemme de aktuelle indstillinger i en konfigurationsfil på din computer, skal du vælge **Gem som**. Hvis du vil gendanne dine indstillinger fra en konfigurationsfil på din computer, skal du vælge **Åbn**.

5. Vælg **Luk** for at lukke dialogboksen.

### <a name="load-and-run-test-cases"></a>Indlæse og køre testsager

1. Vælg **Indlæs** for at indlæse testplanen **RSAT-testplan** fra Azure DevOps-projektet.

    ![Knappen Indlæs](./media/setup_rsa_tool_64.png)

2. Vælg testsagen **Opret et nyt produkt** fra testpakken, og vælg derefter **Ny \> Generér testkørsels- og parameterfiler**.

    ![Kommandoen Generér testkørsels- og parameterfiler i menuen Ny](./media/setup_rsa_tool_65.png)

    Excel-parameterfilen oprettes i den lokale mappe, som du har angivet i RSAT-konfigurationen (f.eks. **C:\\Temp\\RegressionTool**).

    ![Excel-parameterfil er oprettet](./media/setup_rsa_tool_66.png)

3. Hvis du vil gemme parameterfilerne, skal du vælge **Overfør**. Test automatiseringsfiler for alle valgte testsager, der overføres til Azure DevOps til fremtidig brug. (Disse filer omfatter Excel-testparameterfiler).

    På denne måde kan du vælge **Indlæs** for at indlæse parameterfilerne (og automatiseringsfiler) fra testsagen direkte fra Azure DevOps. Du behøver ikke at generere parameterfilerne igen. Denne fremgangsmåde vil blive vigtig senere, når du vil beholde ændringerne i parameterfilen, så de ikke bliver overskrevet.

4. Hvis du vil kontrollere, at automatiseringsfilerne og parameterfilerne gemmes i Azure DevOps, skal du gå til Azure DevOps-projektet, vælge **Tavler \> Workflowopgaver** og vælge testsagen **Opret et nyt produkt**. Under fanen **Vedhæftede filer** skulle du få vist fire filer:

    - **.cs** – C\# automatiseringsfil
    - **.dll** – Kompileret automatiseringsfil som en assembly
    - **.xlsx** – Excel-parameterfil
    - **.xml** – Registreringsfil

    ![Filer under fanen Vedhæftede filer](./media/setup_rsa_tool_67.png)

5. Vælg den testsag, der skal køres, og vælg derefter **Kør**.

    > [!NOTE]
    > Før du kører testsager, og hvis du bruger Internet Explorer som browser, skal du sørge for, at din skrivebordsopløsning er angivet til **100 %** i **Windows-skærmindstillingerne \> Skalering og layout**. Hvis du ikke kan ændre denne indstilling på en virtuel maskine (VM), skal du ændre den på den klient (bærbar), hvor du forsøger at få adgang til den virtuelle maskine. Opløsningsindstillingerne nedarves derefter med skærmindstillingerne for den virtuelle maskine.

    ![Skrivebordsopløsning angivet til 100 %](./media/setup_rsa_tool_68.png)

6. Hvis browserdriverne ikke er installeret i systemet, får du vist en advarselsmeddelelse om, at "Denne handling kræver driveren \<browsernavn\>. Vil du downloade og installere den automatisk nu?" Vælg **Ja**.

    ![Advarselsmeddelelse for Internet Explorer](./media/setup_rsa_tool_69.png)

    ![Advarselsmeddelelse for Chrome](./media/setup_rsa_tool_70.png)

    > [!NOTE]
    > Hvis du bruger Chrome som browser og modtager en fejlmeddelelse om, at sessionen ikke blev oprettet, fordi Chrome-versionen ikke er korrekt, skal du downloade den seneste Chrome-driver fra <http://chromedriver.chromium.org/downloads> til mappen **C:\\Programmer (x86)\\Regression Suite Automation Tool\\Common\\External\\Selenium**.

    ![Fejlmeddelelse for Chrome](./media/setup_rsa_tool_71.png)

    Testsagen er kørt, og feltet **Resultat** er opdateret.

    ![Statusindikator](./media/setup_rsa_tool_72.png)

    Hvis du har fulgt dette selvstudium slavisk, vil testsagen **Opret et nyt produkt** mislykkes, fordi opgaveregistreringen til oprettelse af et produkt har gemt produktnavnet som en fast kodet værdi. Hvis du kører den samme testsag igen, skulle du modtage en fejlmeddelelse, da produktet allerede findes.

    ![Resultatfelt er angivet til Ikke bestået](./media/setup_rsa_tool_72.png)

### <a name="view-the-test-results"></a>Vise testresultaterne

1. Dobbeltklik på den mislykkede testsag.

    Du får en fejlmeddelelse.

    ![Fejlmeddelelse](./media/setup_rsa_tool_73.png)

2. Vælg **Detaljer** for at få vist hele fejlmeddelelsen.

    ![Hel fejlmeddelelse](./media/setup_rsa_tool_74.png)

3. Hvis du vil have vist en detaljeret version af fejlmeddelelsen i Azure DevOps, skal du vælge **Åbn i Azure DevOps**. I Azure DevOps kan du få vist status for testsagen og den detaljerede fejlmeddelelse.

    ![Detaljeret fejlmeddelelse i Azure DevOps](./media/setup_rsa_tool_75.png)

4. Hvis du vil have vist testresultaterne direkte i Azure DevOps-projektet, skal du gå til **Testplaner \> Testplaner \> Kørsler**. Dobbeltklik på den testkørsel, du vil have vist flere oplysninger om.

    ![Liste over testkørsler i Azure DevOps](./media/setup_rsa_tool_76.png)

5. Fanen **Kørselsoversigt** viser, at testsagen ikke lykkedes, men den viser ikke den faktiske fejlmeddelelse. Hvis du vil have vist den detaljerede fejlmeddelelse, skal du vælge fanen **Testresultater**.

    ![Fanen Kørselsoversigt](./media/setup_rsa_tool_77.png)

    Fanen **Testresultater** indeholder oplysninger om testsagen sammen med resultatet og fejlmeddelelsen.

    ![Fanen Testresultater](./media/setup_rsa_tool_78.png)

6. Dobbeltklik på den relevante post for at få vist den detaljerede fejlmeddelelse.

    ![Detaljeret fejlmeddelelse](./media/setup_rsa_tool_79.png)

    > [!NOTE]
    > Alle fejlmeddelelser er også tilgængelige lokalt i **C:\\Brugere\\\$DitBrugernavn\\AppData\\Roaming\\regressionTool\\errormsg-.txt**.

7. Du kan også eksportere testkørselsresultaterne fra testplanniveauet ved at vælge **Eksportér**.

    ![Eksportere en testplan](./media/setup_rsa_tool_80.png)

### <a name="modify-the-excel-parameter-file"></a>Redigere Excel-parameterfilen

1. Åbn RSAT.
2. Vælg testsagen, og vælg derefter **Rediger** for at åbne Excel-parameterfilen.

    Bemærk, at værdien i feltet **Produktnummer** i **EcoResProductCreate**-arket er hard-coded. Du skal opdatere dette felt til et nyt produktnummer, før du kører testsagen igen.

3. Hvis du vil generere et entydigt produktnummer for hver kørsel uden at skulle genåbne Excel-parameterfilen og manuelt opdatere produktnummeret hver gang, skal du bruge følgende Excel-formel.

    ```
    ="RSAT_"&TEXT(NOW(),"yyymmddhhmm")
    ```

    > [!NOTE]
    > Udover fanen **Generelt** indeholder Excel-parameterfilen en datafane for hver formularside, som testsagen besøger.

    ![Feltet Produktnummer](./media/setup_rsa_tool_81.png)

4. Vælg **Gem**, og luk derefter Excel-projektmappen.
5. Vælg **Overfør** for at gemme Excel-parameterfilen i Azure DevOps.

    ![Meddelelse om vellykket overførsel](./media/setup_rsa_tool_82.png)

    > [!NOTE]
    > Hvis du vil køre testsager i en bestemt brugerkontekst, skal du angive brugerens e mail-id i feltet **Testbruger** under fanen **Generelt** i Excel-parameterfilen. I den seneste version af RSAT er layoutet i felterne i Excel-parameterfilen blevet opdateret, men konceptet forbliver uændret.
    >
    > ![Feltet Testbruger](./media/setup_rsa_tool_83.png)

### <a name="validate-the-results"></a>Validere resultaterne

- Vælg **Kør** for at køre testsagen igen, og kontrollér, at testsagen er bestået. Du kan få vist testresultaterne som beskrevet i afsnittet [Vise testresultaterne](#view-the-test-results).

    ![Resultatfelt er angivet til Bestået](./media/setup_rsa_tool_84.png)

### <a name="chaining-of-test-cases"></a>Sammenkædning af testsager

En nøglefunktion i RSAT er sammenkædning af testsager (dvs. en test kan overføre værdier til andre test). Testsager køres efter deres definerede rækkefølge i Azure DevOps-testplanen. (Denne rækkefølge kan også opdateres i selve testværktøjet). Hvis du derfor vil overføre variabler fra én testsag til en anden, er det vigtigt, at testene befinder sig i den rigtige rækkefølge.

I dette afsnit skal du oprette en gemt variabel i den første testsag, oprette endnu en testsag og overføre den gemte variabel fra den første testsag til den anden testsag. Derefter skal du køre testsagerne som en sammenkædet testsag i RSAT.

#### <a name="modify-an-existing-task-recording-to-create-a-saved-variable"></a>Redigere en eksisterende opgaveregistrering for at oprette en gemt variabel

1. Åbn klienten.
2. Vælg knappen **Indstillinger** (tandhjulsymbolet), og vælg derefter **Arbejdsrutineoptager**.
3. Vælg **Rediger registrering**.

    ![Knappen Rediger registrering](./media/setup_rsa_tool_85.png)

4. Vælg **Åbn fra Lifecycle Services**.

    ![Knappen Åbn fra Lifecycle Services](./media/setup_rsa_tool_86.png)

5. Vælg **Vælg biblioteket Lifecycle Services**.

    ![Knappen Vælg biblioteket Lifecycle Services](./media/setup_rsa_tool_87.png)

    BPM-biblioteker indlæses fra LCS.

    ![Statusindikator](./media/setup_rsa_tool_88.png)

6. Når BPM-bibliotekerne er indlæst fra LCS, skal du vælge BPM-biblioteket **RSAT** og derefter den **Opret et nyt produkt**-forretningsproces, som opgaveregistrering blev knyttet til. Vælg derefter **OK**.

    ![Valg af et BPM-bibliotek og en forretningsproces](./media/setup_rsa_tool_89.png)

7. Navnet på den rette opgaveregistrering angives i feltet **Registreringsnavn**. Vælg **Start**.

    ![Navn på opgaveregistrering i feltet Registreringsnavn](./media/setup_rsa_tool_90.png)

8. Gå til **Administration af produktoplysninger \> Produkter**, og vælg **Nyt** for at åbne den side, hvor den oprindelige opgaveregistrering, **Opret et produkt**, blev registreret.
9. Vælg **Indsæt trin**.

    > [!NOTE]
    > Det nye trin indsættes **efter** det trin, du har valgt i ruden.

    ![Knappen Indsæt trin](./media/setup_rsa_tool_91.png)

10. Højreklik på feltet **Produktnummer**, og vælg derefter **Arbejdsrutineoptager \> Kopiér**.

    ![Kommandoen Kopiér](./media/setup_rsa_tool_92.png)

11. Der tilføjes et nyt trin i ruden. Notér værdien i feltet **Produktnummer**, da du skal bruge nummeret senere.

    ![Nyt tilføjet trin](./media/setup_rsa_tool_93.png)

12. Vælg **Redigeringen blev afsluttet**.
13. Vælg **Gem i Lifecycle Services**, og knyt den nye opgaveregistrering til det samme BPM-bibliotek og den samme forretningsproces, som den oprindelige opgaveregistrering blev knyttet til. Du kan finde flere oplysninger i afsnittet [Oprette en opgaveregistrering og gemme den i BPM-biblioteket](#create-a-task-recording-and-save-it-to-the-bpm-library).
14. Gå til BPM-biblioteket, og vælg **Synkroniser testsager** for at overskrive den opgaveregistrering, der er knyttet til testsagen i Azure DevOps, som beskrevet i afsnittet [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).
15. Åbn RSAT, og vælg **Indlæs** for at genindlæse alle testsagerne i testpakken. Du skal generere automatiserings- og parameterfilerne for den relevante testsag ved at vælge testsagen og derefter vælge **Ny \> Generér testkørsels- og parameterfiler** som beskrevet i afsnittet [Indlæse og køre testsager](#load-and-run-test-cases).

    > [!NOTE]
    > Hvis Excel-parameterfilen er åben, mislykkes regenering. Derfor skal du kontrollere, at Excel-parameterfilen til testsagen er lukket, før du genererer den nye Excel-parameterfil.

16. Vælg **Rediger** for at åbne den nye Excel-parameterfil. Du får vist en ny **Gemt variabel**-post i linje 9. Denne variabel, **{{EcoResProductCreate\_identifikation\_ProductNumber\_Copy}}**, gemmes i opgaveregistreringens XML-fil og kan bruges i efterfølgende test.

    ![Gemt variabelpost](./media/setup_rsa_tool_94.png)

#### <a name="create-a-new-test-case"></a>Oprette en ny testsag

1. Gå til BPM-biblioteket **RSAT**.
2. Vælg eksempelprocessen **Supportforretningsprocesser**, og vælg derefter **Redigeringstilstand** i højre side.
3. Rediger værdien i både feltet **Navn** og feltet **Beskrivelse** til **Frigiv et produkt**. Vælg derefter **Gem**.

    ![Navn og beskrivelse er ændret til Frigiv et produkt](./media/setup_rsa_tool_95.png)

#### <a name="create-a-new-task-recording-that-has-a-validate-function"></a>Oprette en ny opgaveregistrering, der har en valideringsfunktion

- Opret en opgaveregistrering for at frigive det produkt, der er oprettet tidligere, til den juridiske enhed USRT. Du kan finde flere oplysninger i afsnittet [Oprette en opgaveregistrering og gemme den i BPM-biblioteket](#create-a-task-recording-and-save-it-to-the-bpm-library).

    > [!NOTE]
    > Ved sammenkædede testsager anbefaler vi altid, at du finder eller filtrerer efter den post, du har brug for, ved at *skrive værdien i feltet manuelt*. På denne måde kan værktøjet bestemme den post, som handlingen skal udføres på, i den efterfølgende testsag.

    ![Ny opgaveregistrering, der har en valideringsfunktion](./media/setup_rsa_tool_96.png)

    Som den foregående illustration viser, når produktet blev fundet ved hjælp af Quick filter, men før du vælger **Frigiv produkter**, skal du validere værdien i feltet **Produktnummer** for at sikre, at produkt-id'et er det produkt-id, der blev oprettet tidligere. Hvis du vil validere værdien, skal du højreklikke på feltet **Produktnummer** og derefter vælge **Arbejdsrutineoptager \> Valider \> Aktuel værdi**.

    ![Validering af den aktuelle værdi](./media/setup_rsa_tool_97.png)

#### <a name="save-the-task-recording-to-bpm"></a>Gemme opgaveregistreringen i BPM

1. Vælg **Gem i Lifecycle Services**, når opgaveregistreringen er fuldført.

    ![Indstillinger for Gem](./media/setup_rsa_tool_98.png)

2. Biblioteksoplysninger indlæses fra LCS.

    ![Statusindikator](./media/setup_rsa_tool_99.png)

3. Vælg det BPM-bibliotek, der skal knyttes til opgaveregistreringen. I dette selvstudium skal du vælge det BPM-bibliotek **RSAT**, der blev oprettet tidligere, og **Frigiv et produkt** som forretningsproces under det. Vælg derefter **OK**.

#### <a name="sync-bpm-to-azure-devops"></a>Synkronisere BPM til Azure DevOps

1. Gå til BPM-biblioteket, og åbn biblioteket **RSAT**.
2. Vælg **VSTS-synkronisering** og derefter **Synkroniser testsager**. Du kan finde flere oplysninger i afsnittet [Teste synkroniseringen fra BPM til Azure DevOps](#test-the-synchronization-from-bpm-to-azure-devops).

    Når synkroniseringen er fuldført, vises den nye workflowopgave og den tilsvarende testsag for forretningsprocessen **Frigiv et produkt** i Azure DevOps ved **Tavler \> Workflowopgaver**.

#### <a name="add-the-new-test-case-to-the-existing-test-suite"></a>Føje den nye testsag til den eksisterende testpakke

1. Gå til **Testplaner \> Testplaner**, og vælg planen **RSAT-testplan**.
2. Vælg **Tilføj eksisterende**.
3. Vælg **Kør forespørgsel** på siden **Føj testsager til pakke**.
4. Vælg den nye testsag, der blev oprettet til **Frigiv et produkt**, og vælg derefter **Tilføj testsager** i nederste højre hjørne af siden (denne knap vises ikke i følgende illustration).

    ![Siden Føj testsager til pakke](./media/setup_rsa_tool_100.png)

    Testpakken har nu to testsager.

    ![To testsager i testpakken](./media/setup_rsa_tool_101.png)

#### <a name="load-test-cases-into-rsat"></a>Indlæse testsager i RSAT

1. Åbn RSAT, og vælg **Indlæs**.
2. Testsagerne indlæses, og du får vist en advarsel om, at "Handlingen vil overskrive Excel-testdatafiler, og lokale ændringer vil gå tabt. Vil du fortsætte?" Vælg **Ja** for at opdatere Excel-parameterfilerne i det lokale system, men ikke de Excel-parameterfiler, der er overført til Azure DevOps.

    ![Advarselsmeddelelse](./media/setup_rsa_tool_102.png)

    Begge testsager indlæses sammen med Excel-parameterfilen til den første testsag. Da du valgte **Overførsel** i sidste kørsel, hentes parameterfilerne fra Azure DevOps.

    ![Testsager er indlæst](./media/setup_rsa_tool_103.png)

3. Vælg kun den anden testsag, og vælg derefter **Ny \> Generér testkørsels- og parameterfiler**.

#### <a name="edit-the-excel-parameter-file"></a>Redigere Excel-parameterfilen

1. Vælg kun den anden testsag, og vælg derefter **Rediger** for at åbne den tilsvarende Excel-parameterfil.
2. Kopiér den gemte variabel **{{EcoResProductCreate\_Identification\_ProductNumber\_Copy}}** (se afsnittet [Redigere en eksisterende opgaveregistrering for at oprette en gemt variabel](#modify-an-existing-task-recording-to-create-a-saved-variable)) fra den første testsag til alle de felter, hvor produktnummeret bruges. I dette tilfælde skal du kopiere variablen til felterne **Produktnummer** og **Valider produktnummer** på arket **EcoResProductListPage**.

    ![Felterne Produktnummer og Valider produktnummer](./media/setup_rsa_tool_104.png)

    > [!NOTE]
    > Der kan kun overføres variabler mellem testene under den samme testkørsel. Navnene på variablerne skal være helt ens.

3. Vælg **Gem**, og luk derefter Excel-projektmappen.
4. Vælg **Overfør** for at gemme de ændringer, du har foretaget, i Excel-parameterfilen.

#### <a name="run-the-chained-test-cases"></a>Køre de sammenkædede testsager

1. Vælg begge testsager, og vælg derefter **Kør**.
2. Kontrollér, at begge testsager er bestået.

    ![Resultatfelt er angivet til bestået for begge testsager](./media/setup_rsa_tool_105.png)
