---
title: "Konfigurere og installere lokale miljøer"
description: "Dette emne indeholder oplysninger om, hvordan du planlægger, konfigurerer og implementerer et lokalt miljø."
author: kfend
manager: AnnBe
ms.date: 06/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: kfend
ms.search.scope: Core
ms.custom: 55651
ms.assetid: 
ms.search.region: Global
ms.author: sarvanisathish
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 3e9a2e33d9579769f6808b598f865d75f072c450
ms.openlocfilehash: 7caf033ab2de5afd6a2d88fa2d41631df4542cbe
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="set-up-and-deploy-on-premises-environments"></a>Konfigurere og installere lokale miljøer

I dette dokument beskrives, hvordan du kan planlægge din installation, konfigurere infrastrukturen og implementere Microsoft Dynamics 365 for Finance og Operations, Enterprise edition (on-premises).

## <a name="finance-and-operations-components"></a>Finance and Operations-komponenter

Programmet Finance and Operations består af tre hovedkomponenter:

- Applikationsobjektserver (AOS)
- Business Intelligence (BI)
- Økonomirapportering/Management Reporter

Disse komponenter afhænger af følgende systemsoftware:

- Microsoft Windows Server 2016
- Microsoft SQL Server 2016 SP1, som indeholder følgende:

    - Fuldtekstindekssøgning er aktiveret.
    - SQL Server Reporting Services (SSRS).
    - SQL Server Integration Services (SSIS).
    
     > [!NOTE]
     > Programmet kører ikke, hvis Fuldtekstsøgning ikke er aktiveret.

- SQL Server Management Studio
- Enkeltstående Microsoft Azure Service stof
- Windows PowerShell 5.0 eller nyere
- Active Directory Federation Services (AD FS) på Windows Server 2016

  Domænecontrolleren skal være Windows Server 2012 R2 eller nyere med et domænefunktionsniveau for 2012 R2 eller derover

  Du kan finde flere oplysninger om domænefunktionsniveauer i afsnittet: 
  - [Hvad er Active Directory-funktionsniveauer?](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
  - [Om funktionsniveauer i Active Directory-domænetjenester](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)


## <a name="lifecycle-services"></a>Lifecycle Services

Finance and Operations-bit distribueres via Microsoft Dynamics Lifecycle Services (LCS). Før du kan installere, skal du købe licensnøgler via [Enterprise-aftale](https://www.microsoft.com/en-us/Licensing/licensing-programs/enterprise.aspx)-kanalen og konfigurere et lokalt projekt i LCS. Installationer kan kun startes gennem LCS. Du kan finde flere oplysninger om opsætning af lokale projekter i LCS i [Oprette et lokalt projekt i Lifecycle Services](../lifecycle-services/lbd-create-lcs-on-prem-project.md).

## <a name="authentication"></a>Godkendelse

Det lokale program fungerer sammen med AD FS. Hvis du vil arbejde med LCS, skal du også konfigurere Azure Active Directory (Azure AD).

## <a name="standalone-service-fabric"></a>Enkeltstående Service Fabric

Finance and Operations bruger enkeltstående Service Fabric. Du kan finde flere oplysninger i [dokumentationen til Service Fabric](/azure/service-fabric/).

## <a name="infrastructure"></a>Infrastruktur

Finance and Operations er beregnet til brug på en hyperkonvergeret arkitektur. Hardwarekonfigurationen inkluderer følgende komponenter:

- Enkeltstående Service Fabric-klynge, der er baseret på Windows Server 2016 virtuelle maskiner (VM'er)
- SQL Server (både grupperet SQL og Always-On understøttes)
- AD FS til godkendelse
- Server Message Block (SMB) version 3 filshare til lagring
- Valgfrit: Microsoft Office Server 2017

Du kan finde flere oplysninger i [Systemkrav](../get-started/system-requirements.md) og retningslinjer for tilpasning.

### <a name="hardware-layout"></a>Hardwarelayout

Planlæg din infrastruktur og Service Fabric-klynge baseret på den anbefalede dimensionering i [Tilpasning af hardware til lokale miljøer](../get-started/hardware-sizing-on-premises-environments.md). Du kan finde flere oplysninger om, hvordan du planlægger Service Fabric-klyngen, i [Planlægge og forberede enkeltstående Service Fabric-klyngeinstallation](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

I følgende tabel vises et eksempel på hardwarelayoutet. I dette eksempel bruges i resten af dette emne til at illustrere opsætningen.

> [!NOTE]
> Den primære node i Service Fabric-klyngen skal have mindst tre noder. I dette eksempel er **OrchestratorType** angivet som den primære nodetype.

| Maskinformål                                 | Maskinnavn    | IP-adresse    |
|-------------------------------------------------|-----------------|---------------|
| Domænecontroller                               | DAX7SQLAODC1    | 10.179.108.2  |
| AD FS                                           | DAX7SQLAOADFS1  | 10.179.108.3  |
| Filserver                                     | DAX7SQLAOFILE1  | 10.179.108.4  |
| SQL Always-On-klynge                           | DAX7SQLAOSQLA01 | 10.179.108.5  |
|                                                 | DAX7SQLAOSQLA02 | 10.179.108.6  |
|                                                 | DAX7SQLAOSQLA   | 10.179.108.9  |
| Klient                                          | SQLAOCLIENT1    | 10.179.108.11 |
| Service Fabric-klynge/AOS 1                    | SQLAOSF1AOS1    | 10.179.108.12 |
| Service Fabric-klynge/AOS 2                    | SQLAOSF1AOS2    | 10.179.108.13 |
| Service Fabric-klynge/AOS 3                    | SQLAOSF1AOS3    | 10.179.108.14 |
| Service Fabric-klynge/Orchestrator 1           | SQLAOSF1ORCH1   | 10.179.108.15 |
| Service Fabric-klynge/Orchestrator 2           | SQLAOSF1ORCH2   | 10.179.108.16 |
| Service Fabric-klynge/Orchestrator 3           | SQLAOSF1ORCH3   | 10.179.108.17 |
| Service Fabric-klynge/Management Reporter-node | SQLAOSMR1       | 10.179.108.18 |
| Service Fabric-klynge/SSRS-node                | SQLAOSFBIN1     | 10.179.108.10 |

## <a name="setup"></a>Konfiguration

### <a name="prerequisites"></a>Forudsætninger

Før du begynder på opsætningen, skal følgende forudsætninger være opfyldt. Opsætningen af disse forudsætninger behandles ikke i dette dokument.

- Active Directory-domænetjenester (AD DS) er installeret og konfigureret på netværket.
- AD FS er installeret.
- SQL Server, SSRS og Management Studio er installeret.

### <a name="overview"></a>Overblik

Følgende trin skal udføres for at konfigurere infrastrukturen for Finance and Operations.

1. Planlæg dit domænenavn og DNS-zoner
2. Planlæg og hent certifikaterne
3. Planlæg dine bruger- og tjenestekonti
4. Opret DNS-zoner og tilføj A-poster
5. Føj VM'er til domænet
6. Føj nødvendig software til VM'er
7. Hent installationsscripts fra LCS
8. Beskriv konfigurationen
9. Installer certifikater
10. Konfigurer en enkeltstående Service Fabric-klynge
11. Konfigurer LCS-forbindelse til lejeren
12. Konfigurer fillager
13. Konfigurer SQL Server
14. Konfigurer databaserne
15. Krypter legitimationsoplysninger
16. Konfiguration af SSRS
17. Konfigurer AD FS

### <a name="plan-your-domain-name-and-dns-zones"></a>Planlæg dit domænenavn og DNS-zoner

Det anbefales, at du bruger et offentligt registreret domænenavn til din produktionsinstallation af AOS. På denne måde kan man få adgang til den uden for netværket, hvis der er behov for det.

Hvis din virksomheds domæne er eksempelvis contoso.com, kan din zone for Finans and Operations (on-premises) f.eks. være d365ffo.onprem.contoso.com, og værtsnavnene kan være følgende:

- ax.d365ffo.onprem.contoso.com for AOS-computere
- sf.d365ffo.onprem.contoso.com for Service Fabric-klyngen

### <a name="plan-and-acquire-your-certificates"></a>Planlæg og hent certifikaterne

SSL-certifikater (Secure Sockets Layer ) er påkrævet for at sikre en Service Fabric-klynge og alle de programmer, der installeres. For produktions- og sandkassearbejdsbelastninger anbefales det, at du får certifikater fra et nøglecenter (CA) f.eks. [DigiCert](https://www.digicert.com/ssl-certificate/), [Comodo](https://ssl.comodo.com/), [Symantec](https://www.websecurity.symantec.com/ssl-certificate), [GoDaddy](https://www.godaddy.com/web-security/ssl-certificate) eller [GlobalSign](https://www.globalsign.com/en/ssl/). Hvis dit domæne er konfigureret med [Active Directory-certifikattjenester](https://technet.microsoft.com/en-us/library/cc772393(v=ws.10).aspx) (AD CS), kan du oprette certifikaterne via AD CS. Hvert certifikat skal indeholde en privat nøgle, der er oprettet til nøgleudveksling, og det skal kunne eksporteres til en .pfx-fil (Personal Information Exchange).

Selvsignerede certifikater kan kun bruges til testformål. Af praktiske årsager omfatter installationsscripts scripts, der kan generere og eksportere selvsignerede certifikater. Som allerede nævnt skal disse certifikater kun bruges til testformål.

| Formål                                      | Forklaring | Yderligere krav |
|----------------------------------------------|-------------|-------------------------|
| SQL Server SSL-certifikat                   | Dette certifikat bruges til at kryptere data, der overføres via et netværk mellem en forekomst af SQL Server og et klientprogram. | <p>Domænenavnet for certifikatet skal stemme overens med det fuldt kvalificerede domænenavn (FQDN) på SQL Server-forekomsten eller Listener.</p><p>Hvis SQL Listener f.eks. er placeret på computeren DAX7SQLAOSQLA, er certifikatets DNS-navn DAX7SQLAOSQLA.onprem.contoso.com.</p> |
| Service Fabric-servercertifikat            | Certifikatet bruges til at hjælpe med at sikre kommunikationen mellem Service Fabric-noderne. Certifikatet bruges også som det servercertifikat, der præsenteres for den klient, der opretter forbindelse til klyngen. | <p>Certifikatets domænenavn skal svare til den DNS-zone, der er host for AOS og Service Fabric.</p><p>For eksempel kan domænenavnet for certifikatet være \*.onprem.contoso.com eller \*.contoso.com.</p><p>Hvis du bruger et certifikat med jokertegn, gælder jokertegnet kun ét niveau. Et underdomæne, et alternativt emnenavn (SAN), skal anvendes på certifikatet, hvis det er på mere end ét niveau, f.eks. \*.contoso.com i det foregående eksempel.</p> |
| Service Fabric-klientcertifikat            | Certifikatet bruges af klienter til at få vist og administrere Service Fabric-klyngen. | |
| Certifikat for kodeomsætning af nøgle                     | Certifikatet bruges til at kryptere følsomme oplysninger, f.eks. adgangskode til SQL Server og adgangskoder til brugerkonti. | <p>Certifikatnøglen skal indeholde Kodeomsætning af data (10), og må ikke indeholde servergodkendelse eller klientgodkendelse.</p><p>Du kan finde flere oplysninger i [Administration af hemmeligheder i Service Fabric-programmer](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-application-secret-management).</p> |
| AOS SSL-certifikat                          | <p>Certifikatet bruges som det servercertifikat, der præsenteres for klienten for AOS-webstedet. Det bruges også til at aktivere Windows Communication Foundation (WCF)/Simple Object Access Protocol (SOAP)-certifikater.</p><p>Service Fabric-servercertifikatet kan bruges her, hvis det er et certifikat med jokertegn.</p> | <p>Certifikatets domænenavn skal svare til den DNS-zone, der er host for AOS og Service Fabric.</p><p>For eksempel kan domænenavnet for certifikatet være \*d365ffo.onprem.contoso.com, \*onprem.contoso.com eller \*.contoso.com.</p><p>Hvis du bruger et certifikat med jokertegn, gælder jokertegnet kun ét niveau. Et underdomæne, SAN, skal anvendes på certifikatet, hvis det er på mere end ét niveau, f.eks. \*.contoso.com i det foregående eksempel.</p> |
| Sessionsgodkendelsescertifikat           | Certifikatet bruges af AOS til at hjælpe med at sikre en brugers sessionsoplysninger. | Det er også det **Filshare**-certifikat, der bruges under installation fra LCS. |
| Datakrypterings- og datasigneringscertifikat | Disse certifikater bruges af AOS til at kryptere følsomme oplysninger. | |
| Klientcertifikat til Økonomirapportering       | Certifikatet bruges til at hjælpe med at sikre kommunikationen mellem Økonomirapporterings-tjenester og AOS. | |
| Rapporteringscertifikat                        | Certifikatet bruges til at hjælpe med at sikre kommunikationen mellem SSRS og AOS. | |
| Lokalt agentcertifikat           | <p>Certifikatet bruges til at hjælpe med at sikre kommunikationen mellem en lokal agent med en lokal vært og LCS.</p><p>Med dette certifikat kan den lokale agent handle på vegne af din Azure AD-lejer og kommunikere med LCS om at arrangere og overvåge installationer.</p> | |

### <a name="plan-your-users-and-service-accounts"></a>Planlæg dine bruger- og tjenestekonti

Du skal oprette flere bruger- eller tjenestekonti for at kunne bruge Finance and Operations (on-premises). Du skal oprette en kombination af gruppeadministrerede tjenestekonti (gMSAs), domænekonti og SQL-konti. I følgende tabel vises brugerkontiene, formålet med dem og eksempelnavne, der skal bruges i dette emne.

| Brugerkonti                                            | Type           | Formål | Brugernavn |
|---------------------------------------------------------|----------------|---------|-----------|
| Økonomirapportering-programtjenestekonto         | gMSA           |         | Contoso\\svc-FRAS$ |
| Tjenestekonto til Økonomirapportering-processer             | gMSA           |         | Contoso\\svc-FRPS$ |
| Tjenestekontoen Click Once Designer til Økonomirapportering | gMSA           |         | Contoso\\svc-FRCO$ |
| AOS-tjenestekonto                                     | gMSA           | Denne bruger skal oprettes til korrektur af fremtidige scenarier. Vi planlægger at sætte AOS i stand til at fungere sammen med gMSA i kommende versioner. Ved at oprette denne bruger på tidspunktet for installationen, kan du sikre en problemfri overgang til gMSA. | Contoso\\svc-AXSF$ |
| AOS-tjenestekonto                                     | Domænekonto | AOS bruger denne bruger i GA-udgivelsen. | Contoso\\AXServiceUser |
| AOS SQL DB-administrationsbruger                                   | SQL-bruger       | Finance and Operations bruger denne bruger til at godkende i SQL\*. Denne bruger erstattes også af gMSA-brugeren i kommende versioner. | AXDBAdmin |
| Tjenestekonto for lokal installationsagent                  | gMSA           | Denne konto bruges af den lokale agent til at arrangere installationen på forskellige noder. | Contoso\\Svc-LocalAgent$ |

\* SQL-brugernavnet og adgangskoden til SQL-godkendelse er sikret, fordi de er krypteret og gemt i det pågældende filshare.

### <a name="create-dns-zones-and-add-a-records"></a>Opret DNS-zoner og tilføj A-poster

DNS er integreret med AD DS, så du kan du organisere, administrere og finde ressourcer i et netværk. Opret en normal DNS-opslagszone og A-poster for AOS-værtsnavnet og Service Fabric-klyngen. I følgende eksempelinstallation er navnet på DNS-zonen d365ffo.onprem.contoso.com og A-poster eller værtsnavne er følgende:

- **ax**.d365ffo.onprem.contoso.com for AOS-computere
- **sf**.d365ffo.onprem.contoso.com for Service Fabric-klyngen

#### <a name="add-a-dns-zone"></a>Tilføj en DNS-zone

Du skal følge nedenstående procedure for at tilføje en DSN-zone.

1. Log på domænecontrollercomputeren, klikke på **Start**, og start DNS Manager ved at skrive **dnsmgmt.msc**.
2. Højreklik på domænecontrollernavnet, og klik derefter på **Ny zone** \> **Næste**.
3. Vælg en **Primær zone**.
4. Lad afkrydsningsfeltet **Gem zonen i Active Directory (kun tilgængelig, hvis DNS-serveren er en domænecontroller, der kan skrives til)** være markeret, og klik derefter på **Næste**.
5. Vælg **Til alle DNS-servere, der kører på domænecontrollere på dette domæne: Contoso.com**, og klik derefter på **Næste**.
6. Vælg **Normal opslagszone**, og klik derefter på **Næste**.
7. Angiv zonenavnet til brug for din konfiguration, og klik derefter på **Næste**. Skriv f.eks. **d365ffo.onprem.contoso.com**.
8. Vælg **Tillad ikke dynamiske opdateringer**, og klik derefter på **Næste**.

#### <a name="set-up-an-a-record-for-aos"></a>Definer en A-post til AOS

I den nye DNS-zone skal du oprette en A-post, der hedder **ax.d365ffo.onprem.contoso.com** for **hver** Service Fabric-klyngenode af typen **AOSNodeType**. Opret ikke A-poster til de andre nodetyper.

1. Højreklik på den nye zone, og klik derefter på **Ny vært**.
2. Angiv navn og IP-adresse for Service Fabric-noden (f.eks. 10.179.108.12), og klik derefter på **Tilføj vært**.

#### <a name="set-up-an-a-record-for-the-orchestrator"></a>Definer en A-post til Orchestrator'en

I den nye DNS-zone skal du oprette en A-post, der hedder **sf.d365ffo.onprem.contoso.com** for **hver** Service Fabric-klyngenode af typen **OrchestratorType**. Opret ikke A-poster til de andre nodetyper.

1. Højreklik på den nye zone, og klik derefter på **Ny vært**.
2. Angiv navn og IP-adresse for Service Fabric-noden (f.eks. 10.179.108.15), og klik derefter på **Tilføj vært**.

#### <a name="join-vms-to-the-domain"></a>Føj VM'er til domænet

Føj hver af VM'erne til domænet ved at udføre trinnene i [Sådan føjer du Windows Server 2016 til et Active Directory-domæne](http://www.tomsitpro.com/articles/join-windows-server-2016-to-ad-domain,2-1063.html). Du kan også bruge Windows PowerShell-scriptet.

```
$domainName = Read-Host -Prompt 'Specify domain name (ex: contoso.com)'
Add-Computer -DomainName $domainName -Credential (Get-Credential -Message 'Enter domain credential')
Restart-Computer
```
Når VM'erne er knyttet til domænet, kan du føje AOS-tjenestekonti (Contoso\svc AXSF$, Contoso\svc AXSF$) til den lokale administratorgruppe. Du kan se i artiklen [Føje et medlem til en lokal gruppe](https://technet.microsoft.com/en-us/library/cc772524(v=ws.11).aspx), hvordan du gør dette.

#### <a name="disable-user-access-control"></a>Deaktivere brugeradgangskontrol 

Kør følgende script for at deaktivere brugeradgangskontrol på **hver** Service Fabric-node.
```
$RegPath = "HKLM:\SOFTWARE\Microsoft\Windows\CurrentVersion\Policies\System"
New-ItemProperty -Path $RegPath -Name "EnableLUA" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "ConsentPromptBehaviorAdmin" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "EnableUIADesktopToggle" -Value 0 -PropertyType "DWORD" -Force
New-ItemProperty -Path $RegPath -Name "LocalAccountTokenFilterPolicy" -Value 1 -PropertyType "DWORD" -Force
```
> [!IMPORTANT]
> Du skal genstarte noden, når scriptet er fuldført.

#### <a name="add-prerequisite-software-to-vms"></a>Føj nødvendig software til VM'er

Følgende tabel indeholder den nødvendige software, der skal anvendes på computerne af hver nodetype.

> [!NOTE]
> Du skal genstarte computeren, når du har installeret komponenterne.

| Node-type | Komponent | Kommando |
|-----------|-----------|---------|
| AOS       | SNAC – ODBC-driver | Se [Microsoft ODBC-driver 13.1 til SQL Server - Windows + Linux](https://www.microsoft.com/en-us/download/details.aspx?id=53339). |
| AOS       | Microsoft .NET Framework version 2.0-3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| AOS       | Microsoft .NET Framework version 4.0-4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| AOS       | IIS (Internet Information Services) | `Add-WindowsFeature WAS, WAS-Process-Model, WAS-NET-Environment, WAS-Config-APIs`<br>`# Windows Process Activation Service`<br>`Add-WindowsFeature Web-Server, Web-WebServer, Web-Security, Web-Filtering, Web-App-Dev, Web-Net-Ext, Web-Mgmt-Tools, Web-Mgmt-Console` |
| AOS       | Microsoft SQL Server Management Studio 2016 | |
| AOS       | Microsoft Visual C++ Redistributable-pakker til Microsoft Visual Studio 2013 | Se [Microsoft Visual C++ Redistributable-pakker til Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |
| AOS       | Microsoft Access Database Engine 2010 Redistributable | Se [Microsoft Access Database Engine 2010 Redistributable](https://www.microsoft.com/en-us/download/details.aspx?id=13255) |
| BI        | .NET Framework version 2.0-3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| BI        | .NET Framework version 4.0-4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| BI        | Microsoft SQL Server 2016 SP1 | |
| BI        | Management Studio 2016 | |
| BI        | SQL Server Reporting Services 2016 i **Oprindelig** tilstand | |
| MR        | .NET Framework version 2.0-3.5 (CLR 2.0) | `Add-WindowsFeature -Name NET-Framework-Features, NET-Framework-Core, NET-HTTP-Activation, NET-Non-HTTP-Activ` |
| MR        | .NET Framework version 4.0-4.6 (CLR 4.0) | `Add-WindowsFeature -Name NET-Framework-45-Features, NET-Framework-45-Core, NET-Framework-45-ASPNET, NET-WCF-Services45, NET-WCF-TCP-PortSharing45` |
| MR        | Visual C++ Redistributable-pakker til Visual Studio 2013 | Se [Microsoft Visual C++ Redistributable-pakker til Visual Studio 2013](https://support.microsoft.com/en-us/help/3179560). |

#### <a name="download-setup-scripts-from-lcs"></a>Hent installationsscripts fra LCS

Vi har medtaget flere scripts for at forbedre installationsoplevelsen. Følg disse trin for at hente installationsscriptene fra LCS.

1. Log på LCS (<https://lcs.dynamics.com/v2>).
2. Klik på dashboardet, og klik på feltet **Delt aktivbibliotek**.
3. Klik på fanen **Model**.
4. I gitteret skal du vælge rækken **Dynamics 365 for Operations - lokale installationsscripts**.
5. Klik på **Versioner**, og hent den nyeste version af disse scripts.

### <a name="describe-your-configuration"></a>Beskriv konfigurationen

Dette afsnit indeholder oplysninger om de scripts, skal du køre. Scriptene beskrives i den rækkefølge, du skal køre dem i. For at køre scriptene skal du udfylde skabelonfilen på $(downloadPath)\\ConfigTemplate.xml. Filen ConfigTemplate.xml beskriver Service Fabric-klyngerne, de certifikater, der bruges til at konfigurere dem, og de konti, der skal have adgang til de relevante certifikater. I det eksempel, der er angivet, udfyldes værdierne for den eksempelinfrastruktur, der er beskrevet i dette emne. Skabelonfilen skal bruges i næste afsnit.

#### <a name="create-the-domain-account-for-a-service-user"></a>Oprette domænekontoen for en tjenestebruger

Kør følgende kommando for at oprette domænebrugerkontoen contoso\\AXServiceUser.

```
New-ADUser -Name 'AXServiceUser' `
    -AccountPassword (Read-Host -Prompt 'Specify User Password' -AsSecureString) `
    -PasswordNeverExpires $true -ChangePasswordAtLogon $false `
    -Enabled $true -UserPrincipalName 'AXServiceUser@contoso.com'
```

#### <a name="create-gmsas"></a>Oprette gMSAs

1. Skift til mappen **$(DownloadPath)**, og kør følgende Windows PowerShell-kommando.

    > [!NOTE]
    > Dette script opretter ikke brugeren. I stedet udskrives de kommandoer, der skal køres manuelt på domænecontrollercomputeren.

    ```
    # Generate gMSA account creation script (shows in console):
    .\Get-NewGMSAInDomainScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

2. Kopier outputtet fra kommandoen til et Windows PowerShell-vindue. Sørg for, at linjeskiftene er fjernet, og kør linjerne på Active Directory-domænecontrollercomputeren ved hjælp af administratorrettigheder (højreklik, og klik derefter på **Kør som Administrator**).
3. Kør følgende script på Active Directory-domænecontrollercomputeren for at validere, at kontiene er blevet oprettet. Du skal sørge for at køre scriptet, efter at du har erstattet det mønster, der svarer til navngivningskonventionen for tjenestekontiene.

    ```
    #Use this command to validate the gMSA accounts are added to AD.
    #Ensure to replace the Filter parameter with the pattern used to create your accounts.
    Get-ADServiceAccount -Filter { samAccountName -like "svc-*" }
    ```

4. Kør scriptet Export-AddGMSAsONVMScript.ps1 på klientcomputeren. Dette script genererer scripts, der køres på hver Service Fabric-VM, og føjer dem til en mappe, der svarer til hvert VM-navn.

    ```
    # Exports a script for installing gMSA on VM nodes into a directory VMs\<VMName>, again feed from XML
    .\Export-AddGMSAsOnVMScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

#### <a name="stop-iis"></a>Stop IIS

Brug RDP (Fjernskrivebordsprotokol) til at oprette forbindelse til hver Service Fabric-VM, og udfør de manuelle trin i [Starte eller stoppe webserveren (IIS 7)](https://technet.microsoft.com/en-us/library/cc732317(v=ws.10).aspx). Alternativt kan du bruge følgende Windows PowerShell script ved at bruge RDP til at oprette forbindelse til hver Service Fabric-VM.

```
$ServiceName = "WAS"
$wasService = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($wasService)
{
    $wasService.DependentServices | Stop-Service -Force -ErrorAction Continue
    $wasService | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}

$ServiceName = 'W3SVC'
$w3svc = Get-Service $ServiceName -ErrorAction SilentlyContinue
if($w3svc)
{
    $w3svc.DependentServices | Stop-Service -Force -ErrorAction Continue
    $w3svc | Stop-Service -ErrorAction Continue
    Set-Service $ServiceName -StartupType Disabled
}
```
_IIS-funktionen skal være installeret, men deaktiveret, da der er nogle afhængigheder af IIS-DLL-filer i produktet._

### <a name="install-certificates"></a>Installer certifikater

1. Hvis du har hentet de certifikater, der er angivet tidligere i dette emne, fra et gyldigt nøglecenter, skal du angive .pfx-filnavnet og aftrykket for certifikaterne i filen ConfigTemplate.xml. Indstil attributten **generateSelfSignedCert** til **False** og **exportable**-attributten til **False**. Kopier .pfx-filerne til $(DownloadPath)\\InfrastructureScripts\\Certs-mappen.
2. Hvis du bruger selvsignerede certifikater (kun til testformål), kan du køre følgende script. For at oprette selvsignerede certifikater skal du i filen ConfigTemplate.xml sikre dig, at **generateSelfSignedCert** er indstillet til **True** og **exportable** er indstillet til **True**. Scriptet opdaterer XML-filen med aftrykket for certifikaterne.

    ```
    # Create self-signed certs (optionally, use -Display if you only want to see commands):
    # Note: this script is completely driven off ConfigTemplate.xml
    .\New-SelfSignedCertificates.ps1 -InputXml .\ConfigTemplate.xml
    ```

3. Du kan eksportere de nye certifikater med den private nøgle (.pfx-filen). Brug følgende script til at oprette og køre eksportkommandoerne i Windows PowerShell. .pfx-filerne bliver placeret i Cert-mappen.

    ```
    # Exports Pfx files into a directory VMs\<VMName>, all the certs will reside in a folder named Certs\
    # Feeds from XML, if certs don't have passwords then you are prompted to enter one
    .\Export-PfxFiles.ps1 -InputXml .\ConfigTemplate.xml
    ```

    > [!NOTE]
    > Certifikaterne skal være installeret og skal være placeret i cert:\\CurrentUser\\Mit. Certifikaterne skal også kunne eksporteres.

    Hvis du bruger selvsignerede certifikater, gå til næste afsnit. Du behøver ikke at udføre denne procedure.

4. Når du har eksporteret eller kopieret .pfx-filerne til $(DownloadPath)\\InfrastructureScripts\\Certs-mappen, skal du køre følgende kommandoer for at oprette scripts, der skal anbringes i de mapper, der svarer til VM'erne.

    ```
    # Exports script for adding ACLs to certs into a directory VMs\<VMName>
    .\Export-CertificateAclsForVMs.ps1 -InputXml .\ConfigTemplate.xml
    
    # Exports Import-PfxFiles.ps1 script for importing PFXs on VM nodes into a directory VMS\<VMname>:
    .\Export-ImportPfxFilesScript.ps1 -InputXml .\ConfigTemplate.xml
    
    .\Export-UnblockStrongNameScript.ps1 -InputXml .\ConfigTemplate.xml
    ```

5. Kopier scriptene i hver mappe til de VM'er, der svarer til mappenavnet.
6. På hver VM skal du køre følgende scripts i den rækkefølge, de vises i.

    ```
    #Run this script only if it exists
    .\Add-GMSAOnVM.ps1
    
    .\Import-PfxFiles.ps1
    
    .\Set-CertificateAcls.ps1
    
    #Run this script only if it exists
    .\Unblock-StrongName.ps1
    ```

### <a name="set-up-a-standalone-service-fabric-cluster"></a>Konfigurer en enkeltstående Service Fabric-klynge

1. Kør følgende kommando for at oprette filen ClusterConfig.json.

    ```
    .\New-SFClusterConfig.ps1 -InputXml .\ConfigTemplate.xml
    ```

    Du kan finde flere oplysninger i [Trin 1B: Oprette en klynge til flere maskiner](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster), [Sikre en enkeltstående klynge på Windows ved hjælp af x.509-certifikater](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-windows-cluster-x509-security) og [Oprette en separat klynge, der kører på Windows Server](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#create-the-cluster).

2. Hent [Den enkeltstående Service Fabric-installationspakke](https://docs.microsoft.com/en-us/azure/service-fabric/service-fabric-cluster-creation-for-windows-server#download-the-service-fabric-standalone-package) til en af din Service Fabric-noder. Når zip-filen er hentet, kan du genåbne den ved at højreklikke på zip-filen og derefter klikke på **Egenskaber**. I dialogboksen skal du markere afkrydsningsfeltet **Ophæv blokering** nederst til højre.
3. Kopier zip-filen til en af noderne i Service Fabric-klyngen, og pak den ud.
4. Kør følgende kommandoer for at oprette en indgående firewallregel på port 443 og 445 i alle noder.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "SFInbound443445" -LocalPort 135, 137, 138, 139, 445, 443 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "SFInbound443445"
    ```

5. Kør følgende kommandoer for at oprette en indgående firewallregel på port 80 for SSRS-noden alene.

    ```
    #Create inbound Rule
    New-NetFirewallRule -DisplayName "Reporting80" -LocalPort 80 -Direction Inbound -Enabled True -Protocol TCP
    
    #Test inbound Rule
    Get-NetFirewallRule -DisplayName "Reporting80"
    ```

6. Kopier din ClusterConfig.json-fil til mappen med den udpakkede installationsfil til den enkeltstående Service Fabric.
7. Gå til den udpakkede installationsmappen i Windows PowerShell ved hjælp af administratorrettigheder, og kør følgende kommando for at teste ClusterConfig.

    ```
    .\TestConfiguration.ps1 -ClusterConfigFilePath .\clusterConfig.json
    ```

8. Hvis testen fuldføres korrekt, skal du køre følgende kommando for at installere klyngen.

    ```
    .\CreateServiceFabricCluster.ps1 -ClusterConfigFilePath .\ClusterConfig.json
    ```

9. Når klyngen er oprettet, kan du åbne Service Fabric Explorer på enhver klientcomputer for at validere installationen:

    1. Installer Service Fabric-klientcertifikatet i CurrentUser\\Mit, hvis det ikke allerede er installeret.
    2. Gå til **Indstillinger for Internet Explorer** \> **Kompatibilitetstilstand**, og fjern markeringen i afkrydsningsfeltet **Vis intranetsteder i kompatibilitetstilstand**.
    3. Gå til `https://sf.d365ffo.onprem.contoso.com:19080`, hvor sf.d365ffo.onprem.contoso.com er værtsnavnet for den Service Fabric-klynge, der er angivet i denne zone. Hvis DNS-navnefortolkning ikke er konfigureret, kan du bruge IP-adressen på computeren.
    4. Vælg klientcertifikatet. Siden **Service Fabric Explorer** vises.

### <a name="configure-lcs-connectivity-for-the-tenant"></a>Konfigurer LCS-forbindelse til lejeren

Implementering og vedligeholdelse af Finance and Operations planlægges via LCS ved hjælp af en lokal agent. Hvis du vil oprette forbindelse fra LCS til Finance and Operations-lejeren, skal du konfigurere et certifikat, der gør det muligt for den lokale agent til at handle på vegne af din Azure AD-lejer (f.eks. Contoso.Onmicrosoft.com).

Brug det lokale agentcertifikat, du har fået fra et nøglecenter eller det selvsignerede certifikat, som du genererede ved hjælp af scripts.

Kun brugerkonti, der har mapperollen Global administrator kan tilføje certifikater for at godkende LCS. Som standard bliver den person, der tilmelder sig Microsoft Office 365 for din organisation, global administrator for mappen.

> [!NOTE]
> Du skal konfigurere certifikatet nøjagtigt én gang pr. lejer. Alle lokale miljøer kan bruge det samme certifikat til at oprette forbindelse med LCS.

1. Hent og installer den nyeste version af Azure PowerShell på en klientcomputer. Du kan finde flere oplysninger i [Installere og konfigurere Azure PowerShell](https://docs.microsoft.com/en-us/powershell/azure/install-azurerm-ps?view=azurermps-4.1.0&viewFallbackFrom=azurermps-4.0.0).
2. Log på [Kundens Azure-portal](https://portal.azure.com) for at kontrollere, at du har mapperollen Global administrator.
3. Kør følgende script fra $(DownloadPath)\\InfrastructureScripts.

   ```
   .\AddCertToServicePrincipal.ps1 -CertificateThumbprint <OnPremLocalAgent Certificate Thumbprint>
   ```

### <a name="set-up-file-storage"></a>Konfigurer fillager

Du skal konfigurere to meget tilgængelige SMB-3.0-filshares. Du kan finde oplysninger om, hvordan du aktiverer SMB 3.0, i [SMB-sikkerhedsforbedringer](https://technet.microsoft.com/en-us/library/dn551363(v=ws.11).aspx#BKMK_disablesmb1).
Sikre, at dialektforhandling ikke kan registrere eller forhindre nedgradering fra SMB 2.0 eller 3.0 til SMB 1.0. Af denne grund og for at udnytte alle mulighederne i SMB-kryptering, anbefales det, at du deaktiverer SMB-1.0 serveren

> [!NOTE]
> For at sikre, at dataene er beskyttede, mens de er gemt i dit miljø, skal BitLocker-drevkryptering være aktiveret på hver enkelt computer. Du kan finde oplysninger om, hvordan du aktiverer BitLocker, i [BitLocker: Sådan installerer du på Windows Server 2012 og nyere](https://docs.microsoft.com/en-us/windows/device-security/bitlocker/bitlocker-how-to-deploy-on-windows-server).

- Et filshare, der gemmer brugerdokumenter, der er overført til AOS (f.eks. \\\\DAX7SQLAOFILE1\\aos-lager).
- Et filshare, der indeholder de seneste build- og konfigurationsfiler for at arrangere installationen (f.eks. \\\\DAX7SQLAOFILE1\\agent))

    > [!NOTE]
    > Hold denne filsharesti så kort som muligt for at undgå at overskride den maksimale stilængde af de filer, der vil blive lagt i sharet.

1. Kør følgende kommando på filsharemaskinen.

    ```
    Install-WindowsFeature -Name FS-FileServer -IncludeAllSubFeature -IncludeManagementTools
    ```
#### <a name="set-up-the-dax7sqlaofile1aos-storage-file-share"></a>Konfigurere filsharet \\\\DAX7SQLAOFILE1\\aos-lager

2. I Serverstyring skal du vælge **Fil- og lagringstjenester** \> **Shares**.
3. Klik på **Opgaver** \> **Nyt share** for at oprette et nyt share med navnet **aos-lager**.
4. Giv **Rediger**-rettigheder til hver computer i Service Fabric-klyngen undtagen **OrchestratorNodeType**.
5. Giv **Rediger**-rettigheder til brugerens AOS-domænebruger (contoso\\AXServiceUser) og gMSA brugeren (contoso\\AXSF-svc).

#### <a name="set-up-the-dax7sqlaofile1agent-file-share"></a>Konfigurere filsharet \\\\DAX7SQLAOFILE1\\agent

6. Gå tilbage til Serverstyring og vælg **Fil- og lagringstjenester** \> **Shares**.
7. Klik på **Opgaver** \> **Nyt share** for at oprette et nyt share med navnet **agent**.
8. Giv gMSA-brugeren **Fuld kontrol**-rettigheder til den lokale installationsagent (contoso\\LocalAgent-svc$).

### <a name="set-up-sql-server"></a>Konfigurer SQL Server

1. Installer SQL Server 2016 SP1 med høj tilgængelighed, enten som SQL-klynger, der omfatter et SAN (Storage Area Network) eller i en Always-On-konfiguration.  Kontroller, at **Databaseprogram, Reporting Services, Fuldtekstsøgning** og **Administrationsværktøjer** allerede er installeret.
> [!NOTE]
> Kontroller, at SQL Always On er konfigureret i henhold til [Siden Vælg synkronisering af startdata (Guiderne Always On-tilgængelighedsgruppe)](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards), og følg [Sådan forberedes sekundære databaser manuelt](https://docs.microsoft.com/en-us/sql/database-engine/availability-groups/windows/select-initial-data-synchronization-page-always-on-availability-group-wizards#PrepareSecondaryDbs)
2. Kør SQL-tjenesten som domænebruger.
3. Få et SSL-certifikat fra et nøglecenter, så du kan konfigurere Finance and Operations. Til testformål kan du oprette og bruge et selvsigneret certifikat.

**Selvsigneret certifikat til grupperet SQL-forekomst**
   ```
   New-SelfSignedCertificate -CertStoreLocation "cert:\CurrentUser\My" -DnsName "DAX7SQLAOSQLA.contososqlao.com" -Provider "Microsoft Enhanced RSA and AES Cryptographic Provider" -Subject "DAX7SQLAOSQLA.contososqlao.com"
   ```
**Selvsigneret certifikat til Always-On SQL-forekomst**
```
#https://www.derekseaman.com/2014/11/sql-2014-alwayson-ag-pt-13-ssl.html

# Create certificate for each SQL Node (i.e. 2 nodes = 2 certificates)
# Run script on each node
$computerName = $env:COMPUTERNAME.ToLower() 
$domain = $env:USERDNSDOMAIN.ToLower()
$listenerName = 'dax7sqlaosqla' 
$cert = New-SelfSignedCertificate -Subject "$computerName.$domain" -DnsName "$listenerName.$domain", $listenerName, $computerName -Provider 'Microsoft Enhanced RSA and AES Cryptographic Provider'

```
4. Brug certifikatet, og udfør trinnene i [Sådan aktiveres SSL-kryptering for en forekomst af SQL Server ved hjælp af Microsoft Management Console](https://support.microsoft.com/en-us/help/316898/how-to-enable-ssl-encryption-for-an-instance-of-sql-server-by-using-microsoft-management-console) for at konfigurere SSL på SQL Server.
5. Følg disse trin for hver node i klyngen. Sørg for at foretage ændringerne på den ikke-aktive node og foretage failover til den, når ændringerne er foretaget.

    1. Importer certifikatet til LocalMachine\\Mit.
    2. Giv certifikatrettigheder til den tjenestekonto, som bruges til at køre SQL-tjenesten. I Microsoft Management Console (MMC) skal du højreklikke på certifikatet (certlm.msc) og derefter klikke på **Opgaver** \> **Administrer private nøgler**.
    3. Føj certifikataftrykket til HKEY\_LOCAL\_MACHINE\\SOFTWARE\\Microsoft\\Microsoft SQL Server\\*MSSQL.x*\\MSSQLServer\\SuperSocketNetLib\\Certificate.
    4. I Microsoft SQL Server Configuration Manager skal du indstille **ForceEncryption** til **Ja**.

6. Eksporter den offentlige nøgle for certifikatet (.cer-filen), og installer den i roden, der er tillid til, i hver Service Fabric-node.

### <a name="configure-the-orchestratordata-database"></a>Konfigurere OrchestratorData-databasen

1.  Opret en tom database, og giv den navnet **OrchestratorData**. Denne database bruges af den lokale agent til at arrangere installationer.
2.  Giv den lokale agent gMSA (svc LocalAgent$) **db\_ejer**-rettigheder til databasen:

    1. Udvid navnet på serveren i træet, udvid **Sikkerhed** \> **Logon**, højreklik derefter, og klik på **Nyt logon**.

        ![Kommandoen Nyt logon](./media/OPSetup_01_NewLogin.png)


    2. Slå **svc LocalAgent$**-tjenestekontoen op. Klik på **Placeringer**, og vælg **Hele kataloget**, og klik derefter på **Objekttyper**, og vælg **Tjenestekonto**.

        ![Dialogboksen Vælg bruger, tjenestekonto eller gruppe](./media/OPSetup_02_SelectUserServiceAccountOrGroupDialogBox.png)

    3. Indstil **Tildel ServerRole** til **Offentlig**.
    4. Tildel **db\_ejer**-databaserollerettigheden til OrchestratorData-databasen.

### <a name="configure-the-finance-and-operations-database"></a>Konfigurere Finance and Operations-databasen

1. Log på LCS (<https://lcs.dynamics.com/v2>).
2. Klik på dashboardet, og klik på feltet **Delt aktivbibliotek**.
3. Klik på fanen **Model**. 
4. I gitteret skal du klikke på rækken **Dynamics 365 for Operations on-premises, Enterprise edition - Demodata** for at hente zip-filen.
5. Zip-filen indeholder tomme filer og .bak-filer med demodata. Vælg den relevante .bak-fil efter behov. Hvis du f.eks. har brug for demodata, skal du gendanne filen AxBootstrapDB_Demodata.bak. 
6. Gendan databasen AxBootstrapDB_DemoData.bak.
7. Omdøb databasen **AXDBRAIN**.
8. Kør følgende forespørgsler på den gendannede database.

    ```
    ALTER DATABASE AXDBRAIN
    SET READ_COMMITTED_SNAPSHOT ON
    GO
    
    ALTER DATABASE AXDBRAIN
    SET ALLOW_SNAPSHOT_ISOLATION ON
    GO
    ```

4. Opdater databasefilerne:

    1. Højreklik på databasen, og klik derefter på **Egenskaber**.
    2. Klik på **Filer** for at ændre databasefilens egenskaber.
    3. I feltet **Oprindelig størrelse (MB)** skal du angive en værdi på mere end 5.120.

        ![Dialogboksen Databaseegenskaber](./media/OPSetup_03_DatabasePropertiesDialogBox.png)

    4. For **AXDBBuild\_Data** skal du indstille feltet **Automatisk vækst/Maksimer** til **200** MB (megabyte).
    5. For **AXDBBuild\_Log** skal du indstille feltet **Automatisk vækst/Maksimer** til **500** MB.

        ![Dialogboksen Rediger automatisk vækst](./media/OPSetup_04_ChangeAutogrowthDialogBox.png)

5. Opret en ny bruger, som SQL-godkendelse er aktiveret for (axdbadmin).
6. Du kan bruge oplysningerne i tabellen nedenfor til at tilknytte brugere og databaseroller.

    | Bruger             | Type    | Databaserolle |
    |------------------|---------|---------------|
    | svc-AXSF$        | gMSA    | db\_ejer     |
    | svc-LocalAgent$  | gMSA    | db\_ejer     |
    | svc-FRPS$        | gMSA    | db\_ejer     |
    | svc-FRAS$        | gMSA    | db\_ejer     |
    | axdbadmin        | SqlUser | db\_ejer     |

7. Giv svc AXSF$-brugeren og axdbadmin SQL-brugeradgang til følgende roller i tempdb-databasen:

    - db\_datareader
    - db\_datawriter
    - db\_ddladmin

8. I Management Studio skal du køre følgende Transact SQL-kommandoer (T-SQL):

    ```
    GRANT VIEW SERVER STATE TO axdbadmin
    GRANT VIEW SERVER STATE TO [contososqlao\svc-AXSF$]
    ```
9. Kør følgende kommando:
```
.\Reset-DatabaseUsers.ps1 -DatabaseServer ‘<FQDN of the SQL server>’ -DatabaseName '<AX database name>'
```

### <a name="configure-the-financial-reporting-database"></a>Konfigurere databasen Økonomirapportering

1.  Opret en tom database, og giv den navnet **FinancialReporting**.
2.  Du kan bruge oplysningerne i tabellen nedenfor til at tilknytte brugere og databaseroller.

    | Bruger             | Type | Databaserolle |
    |------------------|------|---------------|
    | svc-LocalAgent$  | gMSA | db\_ejer     |
    | svc-FRPS$        | gMSA | db\_ejer     |
    | svc-FRAS$        | gMSA | db\_ejer     |

### <a name="encrypt-credentials"></a>Krypter legitimationsoplysninger

1. På en klientcomputer skal du installere Certifikat for kodeomsætning af nøgle i LocalMachine\\Mit certifikatlager.
2. Tildel den aktuelle bruger læseadgang til den private nøgle for dette certifikat.
3. Opret filen Credentials.json, som vist her.

    ```
    {
        "AosPrincipal": {
            "AccountPassword": "<encryptedDomainUserPassword>"
        },
        "AosSqlAuth": {
            "SqlUser": "<encryptedSqlUser>",
            "SqlPwd": "<encryptedSqlPassword>"
        }
    }
    ```

    - **AccountPassword** er den krypterede domænebrugeradgangskode for AOS-domænebrugeren (contoso\\axserviceuser).
    - **SqlUser** er den krypterede SQL-bruger (axdbadmin), der har adgang til Finance and Operations-databasen (AXDBRAIN), og **SqlPassword** er den krypterede SQL-adgangskode.

4. Kopier .json-filen til SMB-filsharet \\\\AX7SQLAOFILE1\\agent\\Credentials\\Credentials.json.
5. Opdater Credentials.json-filen med krypterede værdier.

    ```
    # Service fabric API to encrypt text and copy it to the clipboard.
    Invoke-ServiceFabricEncryptText -Text '<textToEncrypt>' -CertThumbprint '<DataEncipherment Thumbprint>' -CertStore -StoreLocation LocalMachine -StoreName My | clip
    ```

    1. I Credentials.json skal du erstatte **\<encryptedDomainUserPassword\>** med adgangskoden til det krypterede domæne.
    2. Erstat **\<encryptedSqlUser\>** med den krypterede Finance and Operations SQL-bruger.
    3. Erstat **\<encryptedSqlPassword\>** med Finance and Operations SQL-adgangskoden.
    
### <a name="set-up-ssrs"></a>Konfiguration af SSRS

1.  Før du begynder, skal du kontrollere, at de forudsætninger, der er angivet i begyndelsen af dette emne, er installeret.
2.  Følg trinene for at [Konfigurere SQL Server Reporting Services for en lokal installation](../analytics/configure-ssrs-on-premises.md)

### <a name="configure-ad-fs"></a>Konfigurer AD FS

Før du kan udføre denne procedure, skal AD FS være installeret på Windows Server 2016. Du kan finde oplysninger om implementering af AD FS i [Deployment Guide Windows Server 2016 og 2012 R2 AD FS Deployment Guide](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/deployment/windows-server-2012-r2-ad-fs-deployment-guide).

Finance and Operations kræver yderligere konfiguration end standardkonfigurationen af AD FS. I de følgende trin kører Windows PowerShell på en computer, hvor rolletjenesten AD FS er installeret. Brugerkontoen skal have tilstrækkelige rettigheder til at administrere AD FS. F.eks. skal brugeren have en domæneadministratorkonto.

1. Konfigurer AD FS-identifikatoren, så den svarer til AD FS-tokenudstederen.

    ```
    $adfsProperties = Get-AdfsProperties
    Set-AdfsProperties -Identifier $adfsProperties.IdTokenIssuer
    ```

2. Du skal deaktivere Windows-integreret godkendelse (WIA) for intranet-godkendelsesforbindelser, medmindre du har konfigureret AD FS til blandede miljøer. Du kan finde flere oplysninger om, hvordan du konfigurerer WIA, så det kan bruges sammen med AD FS, i [Konfigurere browsere til at bruge Windows-integreret godkendelse (WIA) i AD FS](https://docs.microsoft.com/en-us/windows-server/identity/ad-fs/operations/configure-ad-fs-browser-wia).

   ```
   Set-AdfsGlobalAuthenticationPolicy -PrimaryIntranetAuthenticationProvider FormsAuthentication, MicrosoftPassportAuthentication
   ```

3. E-mailadressen for den bruger, der logger på, skal kunne bruges som godkendelsesinput.

   ```
   Add-Type -AssemblyName System.Net
   $fdqn = ([System.Net.Dns]::GetHostEntry('localhost').HostName).ToLower()
   $domainName = $fdqn.Substring($fdqn.IndexOf('.')+1)
   Set-AdfsClaimsProviderTrust -TargetIdentifier 'AD AUTHORITY' -AlternateLoginID mail -LookupForests $domainName
   ```

For at AD FS kan have tillid til Finance and Operations i forbindelse med udveksling af godkendelse skal forskellige programposter registreres i AD FS under en AD FS-programgruppe. For at gøre installationen hurtigere og reducere antallet af fejl kan du bruge følgende script til registrering. Kopier scriptet Publish-ADFSApplicationGroup.ps1 og D365FO-OP-mappen til en maskine, hvor rolletjenesten AD FS er installeret. Kør derefter scriptet ved hjælp af en brugerkonto, f.eks. en administratorkonto, der har tilstrækkelige rettigheder til at administrere AD FS. Yderligere oplysninger om, hvordan du bruger scriptet, finder du i dokumentationen, der er angivet i scriptet. Notér de klient-id'er, der er angivet i outputtet, da du bliver bedt om disse oplysninger i LCS på et senere tidspunkt.

```
# Host URL is your DNS record\host name for accessing the AOS
.\Publish-ADFSApplicationGroup.ps1 -HostUrl 'ax.d365ffo.onprem.contoso.com'
```

AD FS-administrationskonsollen skal ligne følgende illustration. Du kan åbne Serverstyring ved at klikke på **Værktøjer** \> **AD FS-administration** og derefter klikke nederst i træstrukturen i venstre side på **Programgrupper**. Dobbeltklik på programgruppen for at få vist flere detaljer.

![Egenskaber for programgruppe](./media/OPSetup_05_ApplicatioGroupProperties.png)

Til sidst skal du med tanke på logisk kontrol sikre, at du kan få adgang til AD FS OpenID konfigurations-URL'en på en Service Fabric-node af typen **AOSNodeType** ved at gå til `https://<adfs-dns-name>/adfs/.well-known/openid-configuration` i en webbrowser. Hvis du modtager en meddelelse om, at webstedet ikke er sikkert, har du ikke har tilføjet dit AD FS SSL-certifikat til det nøglecenter, der er tillid til. Dette trin er beskrevet i installationsvejledningen til AD FS. Hvis du kan få adgang til URL-adressen, returneres en JSON-fil (JavaScript Object Notation), der indeholder konfigurationen af AD FS, og du kan se, er der er tillid til din AD FS URL-adresse.

Hermed er opsætningen af infrastrukturen afsluttet. I følgende afsnit beskrives, hvordan du navigerer til [LCS](https://lcs.dynamics.com) for at konfigurere connectoren og implementere dit Dynamics 365 for Finance and Operations-miljø.

## <a name="configure-connector-and-install-on-premises-local-agent"></a>Konfigurere connector og installere lokal agent

1. Log på [LCS](https://lcs.dynamics.com/), og åbn det lokale implementeringsprojekt.
2. Klik i hamburger-menuen på **Projektindstillinger**.

    ![Kommandoen Projektindstillinger](./media/OPSetup_06_ProjectSettings.png)

3. Klik på **On-premises-connectors**.
4. Klik på **Tilføj** for at oprette en ny connector.
5. Under fanen **Opsæt værtsinfrastruktur** skal du hente agentinstallationsprogram.

    ![Knappen Hent agentinstallationsprogram under fanen Opsæt værtsinfrastruktur](./media/OPSetup_07_DownloadAgentInstaller.png)

6. Kontroller, at zip-filen ikke er blokeret. Højreklik på filen, klik på **Egenskaber**, og vælg derefter **Ophæv blokering**.
7. Pak agentinstallationsprogrammet ud på en af Service Fabric-noderne af typen **OrchestratorType**.
8. Under fanen **Konfigurer agent** skal du angive konfigurationsindstillingerne.
9. Gem konfigurationen, og klik derefter på **Hent konfigurationer** for at hente konfigurationsfilen localagent-config.json.

    ![Knappen Hent konfigurationer under fanen Konfigurer agent](./media/OPSetup_08_DownloadConfigurations.png)

10. Kopier filen localagent-config.json til den computer, hvor agentinstallationspakken er placeret.
11. Åbn et kommandopromptvindue, og kør følgende kommando ved at gå til mappen med agentinstallationsprogrammet.

    ```
    LocalAgentCLI.exe Install <path to config.json>
    ```

    > [!NOTE]
    > Den bruger, der kører denne kommando, skal have **db\_ejer**-rettigheder til OrchestratorData-databasen.
    
12. Gå tilbage til den lokale connector i LCS, når den lokale agent er installeret.
13. Under fanen **Valider opsætning** skal du klikke på knappen **Meddelelsesagent**. Dette vil teste LCS-forbindelsen til din lokale agent. Når forbindelsen er blevet oprettet, vil siden se ud som på symbolet nedenfor.

     ![Validere agent](./media/ValidateAgent.PNG)

## <a name="deploy-your-dynamics-365-for-finance-and-operations-on-premises-environment"></a>Installere Dynamics 365 for Finance and Operations (on-premises)-miljøet

1. Naviger til dit lokale projekt i LCS, gå til **Miljø**, **Sandkasse**, og klik på **Konfigurer**.
2. Vælg din **Miljøtopologi**, og gennemgå guiden for at starte installationen.
3. Den lokale agent modtager installationsanmodningen, starter installationen og giver LCS besked, når den er klar.

