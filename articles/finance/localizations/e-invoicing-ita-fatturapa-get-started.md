---
title: Konfigurere direkte integration af italiensk FatturaPA med SDI
description: Denne artikel indeholder oplysninger, der kan hjælpe dig med at komme i gang med elektronisk fakturering for Italien og oprette direkte integration af italiensk FatturaPA med udvekslingssystemet (SDI).
author: abaryshnikov
ms.date: 07/27/2022
ms.topic: article
audience: Application User, Developer
ms.reviewer: kfend
ms.search.region: Global
ms.author: abaryshnikov
ms.search.validFrom: 2021-10-18
ms.dyn365.ops.version: AX 10.0.20
ms.openlocfilehash: 363b7b5e3d5abbb990fea8f8ad4d0c1bebf80102
ms.sourcegitcommit: 6d9fcb52d723ac5022a3002e0ced8e7b56e9bc2a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/27/2022
ms.locfileid: "9203163"
---
# <a name="set-up-direct-integration-of-italian-fatturapa-with-sdi"></a>Konfigurere direkte integration af italiensk FatturaPA med SDI

[!include [banner](../includes/banner.md)]

> [!IMPORTANT]
> Elektronisk fakturering for Italien understøtter i øjeblikket muligvis ikke alle de funktioner, der er tilgængelige for elektroniske fakturaer i Microsoft Dynamics 365 Finance og Dynamics 365 Supply Chain Management.

Denne artikel indeholder oplysninger, der hjælper dig med at komme i gang med elektronisk fakturering for Italien i Finance og Supply Chain Management. Det fører dig gennem de konfigurationstrin, der er lande-/områdeafhængige i Regulatory Configuration Services (RCS). Disse trin supplerer de trin, der er beskrevet i [Kom i gang med elektronisk fakturering](e-invoicing-get-started.md).

## <a name="prerequisites"></a>Forudsætninger

Følgende forudsætninger skal være opfyldt, før du kan fuldføre trinnene i denne artikel:

- Udfør trinnene i [Start her med elektronisk fakturering](e-invoicing-get-started.md).
- Importer den elektroniske faktureringsfunktion **Italiensk FatturaPA (IT)** til RCS fra det globale lager. Yderligere oplysninger finder du i afsnittet [Importere en elektronisk faktureringsfunktion fra Microsoft-konfigurationsudbyder](e-invoicing-get-started.md#import-an-electronic-invoicing-feature-from-the-microsoft-configuration-provider) i den tidligere nævnte artikel "Kom i gang med elektronisk fakturering".
- Tilføj links fra de påkrævede certifikater til servicemiljøet. De påkrævede certifikater omfatter certifikatet Digital signatur, nøglecenter og klientens certifikat. Der er flere oplysninger i [Oprette en digital certifikathemmelighed](e-invoicing-get-started-service-administration.md#create-a-digital-certificate-secret) i artiklen "Start her med serviceadministration i elektronisk fakturering".

## <a name="country-specific-configuration-for-the-italian-fatturapa-it-electronic-invoicing-feature"></a>Den landespecifikke konfiguration til den elektroniske fakturafunktion Italiensk FatturaPA (IT)

Udfør følgende trin, før du installerer programopsætningen på din tilknyttede app Finance eller Supply Chain Management.

Dette afsnit supplerer afsnittet [Landespecifik konfiguration af programopsætning](e-invoicing-get-started.md#country-specific-configuration-of-application-setup) i artiklen "Start her med elektronisk fakturering".

### <a name="create-a-new-feature"></a>Opret en ny funktion

1. Log på RCS.
2. I afsnittet **Konfigurationsudbydere** i arbejdsområdet **Elektronisk rapportering** skal du markere dit firmas konfigurationsudbyder som aktiv.
3. I arbejdsområdet **Globaliseringsfunktioner** i sektionen **Funktioner** skal du vælge feltet **Elektronisk fakturering**.
4. På siden **Funktioner for elektronisk fakturering** skal du vælge **Tilføj** \> **Baseret på eksisterende funktion**.
5. Vælg **Italiensk FatturaPA (IT**) som en basisfunktion under **Microsoft-konfigurationsudbyder**, angiv et navn, og vælg derefter **Opret funktion**.

### <a name="set-up-application-specific-parameters"></a>Oprette ansøgningsspecifikke parametre

1. På siden **Funktioner for elektronisk fakturering** skal du vælge den funktion, du skal redigere.
2. Kontroller, at **Kladde**-versionen er valgt under fanen **Versioner**.
3. Vælg en konfiguration under fanen **Konfigurationer**, og vælg derefter **Programspecifikke parametre**.
4. I **Opslags**-sektionen skal du kontrollere, at opslaget **Liste over Natura-underkategorier med modtagerbetaling** er valgt.
5. Vælg **Tilføj** under **Betingelser**.
6. Tilføj bestemte betingelser for hver underkategori, der er defineret i systemet, og gem derefter ændringerne.

    > [!NOTE]
    > I kolonnen **Navn** kan du vælge pladsholderværdien **\*Tom\*** eller **\*Ikke tom\*** i stedet for en bestemt værdi.

### <a name="configure-a-processing-pipeline-for-export"></a>Konfigurere en behandlingspipeline til eksport

1. På siden **Funktioner for elektronisk fakturering** skal du vælge den funktion, du skal redigere.
2. Under fanen **Opsætninger** skal du vælge **Salgsfakturaer** og derefter vælge **Rediger**.
3. Gennemgå handlingerne i sektionen **Behandling af pipeline**, og angiv alle nødvendige felter:

    - I feltet **Certifikatnavn** for handlingen **Underskriv dokument** skal du angive certifikatet for digital signatur.
    - Angiv felterne **URL-adresse** og **Certifikater** for handlingen **Send**. Værdien i feltet **Certifikater** er en kæde af certifikater, hvoraf det første er rod-CA-certifikatet (caentrate.cer), mens det andet er certifikatet Klienter.

4. I afsnittet **Anvendelighedsregler** skal du gennemgå afsnittene og gennemse eller angive de påkrævede felter:
    - Gennemse **LegalEntityID**-sætningen, og opdater den med den korrekte værdi fra den juridiske enhed.

5. Vælg **Valider** for at sikre, at alle påkrævede felter er indstillet.
6. Gem ændringerne, og luk siden.
7. Under fanen **Opsætninger** skal du vælge **Projektfakturaer** og derefter vælge **Rediger**.
8. Gentag trin 3 til 6 for projektfakturaer.

### <a name="configure-the-processing-pipeline-for-import"></a>Konfigurere en behandlingspipeline til import

1. På siden **Funktioner for elektronisk fakturering** skal du vælge den funktion, du skal redigere.
2. Under fanen **Opsætninger** skal du vælge **Importfakturaer** og derefter vælge **Rediger**.
3. Angiv en strengværdi i feltet **Datakanel** i sektionen **Datakanel** under fanen **Parametre**.
4. Angiv felterne for opsætningen under fanen **Anvendelsesregler**. Du kan bruge standardsætningen **Kanal** ved at overføre den værdi, du har angivet for feltet **Datakanal** i det foregående trin, til feltet **Værdi**.

    ![Konfigurer anvendelighedsregler.](media/e-invoicing-ita-fatturapa-get-started-apprules-setup.png)

5. Vælg **Valider** for at sikre, at alle påkrævede felter er indstillet.

### <a name="deploy-the-feature"></a>Udrulle funktionen

1. Fuldfør, publicer og udrul funktionen til servicemiljøet. Yderligere oplysninger finder du i afsnittet [Implementere funktionen Elektronisk fakturering i servicemiljøet](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-service-environment) i artiklen "Kom i gang med elektronisk fakturering".
2. Udrul funktionen til det tilknyttede program. Yderligere oplysninger finder du i afsnittet [Implementere funktionen Elektronisk fakturering i tilknyttet program](e-invoicing-get-started.md#deploy-the-electronic-invoicing-feature-to-connected-application) i artiklen "Kom i gang med elektronisk fakturering".

### <a name="set-up-finance"></a>Konfigurere Finance

1. Log på dit Finance-miljø.
2. Gå til arbejdsområdet **Elektronisk rapportering**, og vælg feltet **Microsoft** i sektionen **Konfigurationsudbydere**.
3. Vælg **Lagre** \> **Global** \> **Åbn**.
4. Vælg og importér konfigurationerne **Kontekstmodel for debitorfaktura** og **Kontekstmodel for kreditorfaktura (IT)**.
5. Gå til **Organisationsadministration** \> **Konfiguration** \> **Elektroniske dokumentparametre**.
6. Find og vælg funktionen **Italiensk elektronisk faktura** under fanen **Funktioner**, og markér derefter afkrydsningsfeltet **Aktivér**.
7. Under fanen **Elektronisk dokument** skal du kontrollere, at felterne for **Debitorfakturajournal** og **Projektfaktura** er indstillet i overensstemmelse med oplysningerne i [Konfigurere opsætning af applikationen](e-invoicing-get-started.md#configure-the-application-setup).

### <a name="set-up-vendor-invoice-import"></a>Konfigurere import af kreditorfaktura 

1. I afsnittet **Konfigurationsudbydere** i arbejdsområdet **Elektronisk rapportering** i Finance skal du markere dit firmas konfigurationsudbyder som aktiv.
2. Vælg **Rapporteringskonfigurationer**.
3. Vælg **Kontekstmodel til debitorfaktura**, og vælge derefter **Opret konfiguration**.
4. Vælg **Afledt fra navn: Kundefakturakontekst, Microsoft** for at oprette en afledt konfiguration.
5. Vælg **Designer** i **Kladde**-versionen.
6. Vælg **Datamodel for datakilde** i træet **Datamodel**.
7. Vælg **DataChannel** i træet **Definitioner**, og vælg derefter **Designer**.
8. I træet **Datakilder** skal du udvide containeren **\$Kontekst\_Kanal**.
9. Vælg **Rediger** i feltet **Værdi**. 
10. Angiv navnet på datakanalen. Navnet må højst være på 10 tegn. Den skal svare til værdien af **Datakanal**-parameteren for datakanalen til funktionen Elektronisk fakturering i RCS.
11. Gem ændringerne, og gå derefter til **Rapporteringskonfigurationer** \> **Fuldført konfigurationsversion**.
12. Under fanen **Eksterne kanaler** skal du i sektionen **Kanaler** vælge **Tilføj**.
13. I feltet **Kanal** skal du angive værdien **\$Kontekstkanal**.
14. Angiv værdier i felterne **Firma** og **Beskrivelse**.
15. Vælg den nye afledte konfiguration fra **Kontekstmodel for debitorfaktura** i feltet **Dokumentkontekst**. Tilknytningsbeskrivelsen skal være en **datakanalkontekst**.
16. Under fanen **Importkilder** skal du vælge **Tilføj** og derefter angive følgende værdier:

    - **Navn:** OutputFile
    - **Navn på dataenhed:** Kreditorfakturahoved (**Dataenhed:** VendorInvoiceHeaderEntity)
    - **Modeltilknytning:** Import af kreditorfaktura (IT)

> [!NOTE]
> Hvis du har importeret kreditorfakturaer fra forskellige kilder, kan du oprette flere eksterne kanaler og flere afledte konfigurationer, der har forskellige værdier af **\$Kontekstkanal**. Du kan f.eks. importere kreditorfakturaer til forskellige juridiske enheder.

## <a name="proxy-server-setup"></a>Opsætning af proxyserver

Dette afsnit indeholder oplysninger, der kan hjælpe dig med at oprette og konfigurere proxytjenesten til kommunikation mellem udvekslingssystemet (SDI) og den elektroniske faktureringstjeneste.

### <a name="create-an-app-registration"></a>Oprette en appregistrering

1. Brug følgende Windows PowerShell-script til at oprette et selvsigneret certifikat til S2S-godkendelse (service-til-service).

    ```powershell
    $certOutputLocation = "C:\certs\proxytest"
    $certName = "sdiProxyClientS2SCert"
    $certPassword = "123"

    $certCerFile = Join-Path $certOutputLocation "$certName.cer"
    $certPfxFile = Join-Path $certOutputLocation "$certName.pfx"

    $securePassword = ConvertTo-SecureString $certPassword -AsPlainText -Force

    $cert = New-SelfSignedCertificate -KeyLength 2048 -KeyExportPolicy Exportable -FriendlyName "CN=$certName" -CertStoreLocation Cert:\CurrentUser\My -Subject $certName -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider"

    Export-Certificate -Cert $cert -FilePath $certCerFile -type CERT | Out-Null
    Export-PfxCertificate -Cert $cert -FilePath $certPfxFile -Password $securePassword | Out-Null
    ```

2. Gem .pfx-certifikatfilen i Key Vault, og slet derefter den lokale kopi.
3. Log på [Azure-portalen](https://portal.azure.com) som administrator.
4. Opret en appregistrering for SDI-proxytjenesten.

    1. Gå til **Appregistreringer**, opret en registrering, og angiv derefter følgende værdier for den:

        - **Navn:** SDI-proxyklient
        - **Understøttede kontotyper:** Kun konti i dette organisationsbibliotek (enkelt lejer)

    2. Vælg **Registrer**, og vælg derefter den appregistrering, du netop har oprettet.
    3. Gå til **API-tilladelser**, og vælg **Tildel administratorsamtykke**.
    4. Gå til **Certifikater og hemmeligheder**, vælg **Upload certifikat**, og upload .cer-certifikatfilen til S2S-godkendelse.
    5. Gå til **Virksomhedsprogrammer**, og vælg den app, du har oprettet.
    6. Gem værdierne af **Applikations-id** (klient-id) og **Objekt-id** for appen.
    7. Serviceteamet for fakturering skal give appen adgang til tjenesten. Send værdierne af følgende parametre til <D365EInvoiceSupport@microsoft.com>:

        - AAD-lejer-id
        - LCS-miljø-id
        - Applikations-id
        - Objekt-id

5. I RCS skal du føje appen til programlisten for dit servicemiljø.

    1. Gå til **Globaliseringsfunktioner** \> **Miljøer** \> **Elektronisk fakturering** \> **Tjenestemiljøer**, og vælg dit miljø.
    2. Føj en række til gitteret i sektionen **Programmer**, og angiv navnet på og objekt-id'et for appen.

        ![Tilføjelse af applikationen i servicemiljøet.](media/e-invoicing-ita-fatturapa-get-started-add-app-to-env.png)

    3. Vælg **Gem**, og vælg derefter **Publicer**.

### <a name="create-an-azure-virtual-machine"></a>Oprette en Azure-virtuel maskine

1. I [Azure-portalen](https://portal.azure.com) skal du gå til **Virtuelle maskiner** og vælge **Opret ny**.
2. Vælg abonnementet og ressourcegruppen under fanen **Basis**. Værdierne skal være det abonnement og den ressourcegruppe, hvor dit Key Vault og Blob-lager er placeret.
3. Vælg området. Denne værdi skal være det område, hvor Finance-miljøet er udrullet.
4. Tilføj administratorens brugernavn og adgangskode, og gem dem i Key Vault.
5. Vælg **HTTPS (443)** og **RPD (3389)** i feltet **Vælg indgående porte**.

    > [!NOTE]
    > Det anbefales, at du deaktiverer porten **RDP (3389)**, når systemet går i produktion. Du kan aktivere den igen, hvis du skal oprette forbindelse til den virtuelle maskine (VM) i forbindelse med fejlfinding.

    ![Indstilling af felterne under fanen Basis for at oprette en Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-1.png)

6. Markér afkrydsningsfeltet **Brug administrerede diske** i oversigtspanelet **Avanceret** under fanen **Diske**. Lad markeringen af afkrydsningsfeltet **Ephmeral OS-disk** være fjernet.

    ![Indstilling af felterne under fanen Diske for at oprette en Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-2.png)

7. Under feltet **Offentlig IP** under fanen **Netværk** skal du vælge **Opret ny**.

    ![Indstilling af felterne under fanen Netværk for at oprette en Azure VM.](media/e-invoicing-ita-fatturapa-get-started-create-vm-3.png)

8. I dialogboksen i **Opret offentlig IP-adresse** skal du i feltgruppen **SKU** vælge indstillingen **Standard**. I feltgruppen **Tildeling** skal du vælge indstillingen **Statisk**.

    ![Oprettelse af en offentlig IP-adresse.](media/e-invoicing-ita-fatturapa-get-started-create-vm-4.png)

9. Fjern markeringen i afkrydsningsfeltet **Automatisk lukning** under fanen **Administration** for at deaktivere automatisk lukning.
10. Angiv feltet **Gæste-OS-opdateringer** til **Manuel**, og angiv derefter andre politikker.
11. Gennemse og opret VM'en.
12. I dent nye VM skal du gå til **Identitet** \> **Systemtildelt** og angive indstillingen af **Status** til **Til**.
13. Giv VM-adgang til Key Vault.

    1. Gå til **Adgangskontrol (IAM)** \> **Rolletildelinger** i Key Vault.
    2. Vælg **Tilføj rolletildeling**, og angiv derefter følgende felter:

        1. I feltet **Rolle** skal du angive **Bruger af Key Vault-hemmeligheder**.
        2. Angiv **Virtuel maskine** i feltet **Tildel adgang til**.
        3. Angiv dit abonnement i feltet **Abonnement**.
        4. Angiv din VM i feltet **Vælg**.

    3. Gå til **Adgangspolitikker**.
    4. Vælg **Tilføj adgangspolitik**, og angiv derefter følgende felter:

        1. Vælg din VM i feltet **Valgt sikkerhedskonto**.
        2. Vælg tilladelserne **Liste** og **Hent** i sektionen **Certifikat**.

14. På [Azure-portalen](https://portal.azure.com) skal du gå til **Offentlige IP-adresser** og vælge den IP-adresse, der blev oprettet i VM.
15. Gå til **Konfiguration**, og angiv DNS-navnet (Domain Name System).

### <a name="prepare-the-proxy-service-environment"></a>Forberede proxytjenestemiljøet

Følg disse trin på den maskine, som er vært for proxytjenesten.

1. Opret forbindelse til VM ved hjælp af forbindelse til fjernskrivebord.
2. Åbn snap-in Lokalt maskincertifikat. Du kan finde flere oplysninger i [Sådan gør du: Vis certifikater med MMC-snap-in](/dotnet/framework/wcf/feature-details/how-to-view-certificates-with-the-mmc-snap-in).
3. Importer certifikatet **caentrate.cer** for produktion og **CAEntratetest.cer** til test i [Nøglecentre, der er tillid til](/dotnet/framework/wcf/feature-details/working-with-certificates#certificate-stores). (**CAEntratetest.cer** er det rod-CA-certifikat, der er leveret af myndigheden).
4. Åbn **Slå Windows-funktioner til eller fra** i Kontrolpanel, eller gå til **Serverstyring** \> **Tilføj roller og funktioner** for serveroperativsystemet (OS), og aktivér IIS-funktioner (Internet Information Services):

    - Webstyringsværktøjer
        - IIS-styringskonsol
    - World Wide Web-tjenester
        - Funktioner til programudvikling
            - .NET Extensibility 4.7 (eller 4.8)
            - ASP
            - ASP.NET 4.7 (eller 4.8)
            - CGI
            - ISAPI-udvidelser
            - ISAPI-filtre
        - Almindelige HTTP-funktioner
            - Standarddokument
            - Gennemsyn af mapper
            - HTTP-fejl
            - Statisk indhold
        - Tilstand og diagnose
            - HTTP-logføring
            - Sporing
        - Ydeevnefunktioner
            - Komprimering af statisk indhold
        - Sikkerhed
            - Anmodningsfiltrering

    ![Aktivering af IIS-funktioner.](media/e-invoicing-ita-fatturapa-get-started-turnon-features.png)

### <a name="set-up-the-sdi-proxy-service-in-iis"></a>Konfigurere SDI-proxytjenesten i IIS

1. I Microsoft Dynamics Lifecycle Services (LCS) skal du åbne det delte aktivbibliotek og vælge **Datapakke** som aktivtype.
2. Find **SDI-proxy til elektronisk fakturering**, og download den til VM.
3. Konfigurer tjenesten.

    1. Udpak den **SDI-proxy til elektronisk fakturering**-arkivmappe, du har hentet.
    2. I mappen **src\\FattureService** skal du åbne filen **appsettings.json** og angive følgende parametre:

        - **KeyVaultUri** – Angiv adressen på den Key Vault, der gemmer klientcertifikatet for faktureringstjenesten.
        - **TenantId** – Angiv GUID (Globally Unique Identifier) for kundens lejer.
        - **EnvironmentId** – Angiv id'et for LCS-miljøet.
        - **ClientId** – Angiv app-id'et for registreringen af mellemtjenester i kundens lejer.
        - **ClientCertificateName** – Angiv navnet på S2S-certifikatet i Key Vault.
        - **SecurityServiceClientOptions.Endpoint** – Angiv URL-adressen til sikkerhedstjenesten.
        - **SecurityServiceClientOptions.Resource** – Angiv det område, der skal anskaffes token for.
        - **InvoicingServiceClientOptions.Endpoint** – Angiv slutpunktet for faktureringstjenesten. Denne værdi skal være det samme slutpunkt, der bruges til RCS og Finance.
        - **InvoicingServiceClientOptions.ServiceEnvironmentId** – Angiv navnet på servicemiljøet. Denne værdi skal være navnet på dit Finance-miljø.
        - **NotificationsFolder** – Angiv den mappe, hvor indgående beskedfiler skal gemmes.

    3. Find følgende linje i **web.config**-filen, og tilføj aftrykket af proxyservercertifikatet.

        `<serviceCertificate findValue="[certificate thumbprint]" storeLocation="LocalMachine" storeName="My" x509FindType="FindByThumbprint">`

        > [!TIP]
        > Når systemet går i produktion, kan du ændre visse værdier i web.config-filen for at reducere mængden af logoplysninger, der indsamles, og hjælpe med at spare diskplads. I noden **\<system.diagnostics\>\<source\>** skal du ændre værdien af **switchValue** til **Critical,Error**. Du kan finde flere oplysninger under [MS Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).

4. Åbn IIS Manager. I træet til venstre skal du forblive i rodnoden. Til højre skal du vælge **Servercertifikater**.

    ![Valg af servicecertifikater i IIS Manager.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-1.png)

5. Åbn menuen, og vælg **Import**.
6. I feltet **Certifikatfil (.pfx)** i dialogboksen **Importcertifikat** skal du angive stien til .pfx-filen for proxyservercertifikatet.

    ![Angivelse af filen med proxytjenestens certifikat.](media/e-invoicing-ita-fatturapa-get-started-proxy-cert-2.png)

7. Vælg og hold (eller højreklik på) **Steder**, og vælg derefter **Tilføj websted**.
8. Angiv et navn til webstedet i feltet **Navn på websted** i dialogboksen **Tilføj websted**.
9. Peg i feltet **Fysisk sti** på mappen **src\\FattureService**.
10. Vælg **https** i feltet **Bindingstype**.
11. Angiv værtsnavnet i feltet **Værtsnavn**.
12. Lad felterne **IP-adresse** og **Port** være angivet til standardværdierne.
13. Kontrollér, at afkrydsningsfeltet **Kræv Servernavnsindikation** ikke er markeret, da SDI ikke understøtter denne teknologi.
14. Vælg det proxyservercertifikat, du har importeret, i feltet **SSL-certifikat**.
15. Angiv en pulje til webstedet i feltet **Programpulje**, og notér navnet det (f.eks. **SdiAppPool**).

    ![Tilføjelse af et websted.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-1.png)

16. Når du er færdig med at oprette webstedet, skal du åbne menuen for **SSL-indstillinger**.

    ![Åbning af menuen for SSL-indstillinger.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-2.png)

17. Markér afkrydsningsfeltet **Kræv SSL**, og vælg derefter indstillingen **Kræv** i feltgruppen **Klientcertifikater**.

    ![Konfigurering af SSL-indstillinger.](media/e-invoicing-ita-fatturapa-get-started-proxy-iis-setup-3.png)

18. Åbn **Gennemsyn af mapper**, og vælg **Aktivér**.
19. I enhver webbrowser skal du gå til **serverDNS/TrasmissioneFatture.svc**. Der skal vises en standardside om tjenesten.

    ![Kontrol af tjenesten i en browser.](media/e-invoicing-ita-fatturapa-get-started-proxy-open-browser.png)

20. Opret følgende mapper for at gemme logge og filer:

    - **C:\\Logs\\** – Gem logfiler her. Disse filer kan vises af [MS Service Trace Viewer](/dotnet/framework/wcf/service-trace-viewer-tool-svctraceviewer-exe).
    - **C:\\Files\\** – Gem alle svarfilerne her.

21. I Stifinder skal du tildele **NETWORK SERVICE** og **IIS AppPool\\SdiAppPool** (eller **IIS AppPool\\DefaultAppPool**, hvis du bruger standardpuljen) adgang til mapperne **Logs** og **Files**.

    1. Vælg og hold (eller højreklik på) på en af mapperne, og vælg derefter **Egenskaber**.
    2. Vælg **Rediger** under fanen **Sikkerhed** i dialogboksen **Egenskaber**.
    3. Tilføj brugerne, hvis de ikke står på listen.
    4. Gentag trin 1 til 3 for den anden mappe.

    ![Tilføjelse af rettigheder til servicebrugeren.](media/e-invoicing-ita-fatturapa-get-started-proxy-add-user.png)

## <a name="privacy-notice"></a>Erklæring om beskyttelse af personlige oplysninger 

Aktivering af funktionen **Italiensk elektronisk faktura** kræver måske, at der sendes begrænsede data. Disse data omfatter organisationens momsregistrerings-id. En administrator kan aktivere og deaktivere funktionen Italiensk elektronisk faktura. Følg disse trin for at deaktivere funktionen.

1. Gå til **Organisationsadministration** \> **Konfiguration** \> **Elektroniske dokumentparametre**.
2. Vælg de rækker, der indeholder funktionen **Italiensk elektronisk faktura**, under fanen **Funktioner**, og vælg derefter **Deaktiver nu**.

Data, der importeres fra disse eksterne systemer til denne Dynamics 365-onlinetjeneste, er underlagt vores [erklæring om beskyttelse af personlige oplysninger](https://go.microsoft.com/fwlink/?LinkId=512132). Yderligere oplysninger finder du i sektionen "Erklæring om beskyttelse af personlige oplysninger" i dokumentationen til den lande- eller områdespecifikke funktion.

## <a name="additional-resources"></a>Yderligere ressourcer

- [Oversigt over elektronisk fakturering](e-invoicing-service-overview.md)
- [Start her med serviceadministration i elektronisk fakturering](e-invoicing-get-started-service-administration.md)
- [Start her med elektronisk fakturering](e-invoicing-get-started.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
