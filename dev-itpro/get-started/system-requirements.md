---
title: Systemkrav
description: "Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til installationer i skyen og i det lokale miljø."
author: sericks007
manager: AnnBe
ms.date: 07/14/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: robinr
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30T00:00:00.000Z
ms.dyn365.ops.version: Platform update 2
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 871ba89973f6af341c536f67db056bebb54600b3
ms.contentlocale: da-dk
ms.lasthandoff: 07/25/2017

---

# <a name="system-requirements"></a>Systemkrav

[!include[banner](../includes/banner.md)]


Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til installationer i skyen og i det lokale miljø. Før du installerer Finance and Operations, skal du kontrollere, at det system, du bruger, opfylder eller overstiger minimumkrav til netværk, hardware og software.


## <a name="supported-microsoft-office-applications"></a>Understøttede Microsoft Office-programmer
Følgende Office-programmer understøttes i installationerne af Finance and Operations i skyen og det lokale miljø.
-   Hvis du vil køre tilføjelsesprogrammer til Microsoft Excel og Word, skal du have Microsoft Office 2016 til Windows eller Mac installeret. Du kan finde yderligere oplysninger om versionskrav i [Fejlfinding af Office-integration](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Hvis du vil have vist dokumenter, der er genereret med funktionerne Eksport til Excel eller Eksport til Word, skal have Microsoft Office 2007 eller nyere installeret.

# <a name="system-requirements-specific-to-cloud-deployments"></a>Systemkrav, der er specifikke for installationer i skyen
## <a name="network-requirements"></a>Netværkskrav
-   Finance and Operations er designet til netværk med ventetid på 250-300 millisekunder (ms) eller mindre. Dette er ventetiden fra en browserklient til Microsoft Azure-datacenteret, der er vært for Finance and Operations. Vi anbefaler, at du tester netværksventetiden på <http://www.azurespeed.com>.
-   Kravene til båndbredde for Finance and Operations afhænger af scenariet. De fleste typiske scenarier kræver en båndbredde på mere end 50 kilobyte pr. sekund (KBps). Men til scenarier, der har store datakrav, f.eks. arbejdsområder eller scenarier, der involverer omfattende tilpasning, anbefales mere båndbredde.

Generelt er Finance and Operations optimeret til internettet. Antallet af rundture fra en browserklient til Azure-datacenteret er meget lille, og alle data komprimeres. 

> [!WARNING]
> Du må ikke beregne kravene til båndbredde fra en klientlokalitet ved at multiplicere antallet af brugere med minimumkravene til båndbredde. Den samtidig brug af en given lokalitet er meget vanskeligt at beregne. Til kunder, der er bekymret over kravene til båndbredde, kan de bruge en prøveversion af Finance and Operations.

## <a name="net-framework-requirements"></a>.NET Framework-krav
Finance and Operations kræver .NET Framework version 4.6.2 til alle ClickOnce-programmer, f.eks. ruteplanlægningsagenten for dokumenter. Se installationsvejledning i [Installation af. NET Framework-](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-web-browsers"></a>Understøttede webbrowsere
Webprogrammet kan køre i en af følgende webbrowsere, der kører på de angivne operativsystemer:


-   Microsoft Edge (nyeste offentligt tilgængelige version) på Windows-10
-   Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
-   Google Chrome (nyeste offentligt tilgængelige version) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tablet
-   Apple Safari (nyeste offentligt tilgængelige version) på Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eller Apple iPad

Gå til producentens websted for at finde den nyeste version af hver webbrowser. 

> [!NOTE]
> -   En foreløbig version af Chrome-udvidelsen skal være installeret, før skærmbilleder kan tages af Arbejdsrutineoptager og medtages i de genererede Microsoft Word-dokumenter. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Arbejdsgangseditoren startes som et ClickOnce-program. Kun Microsoft Edge og Internet Explorer (på en understøttet version af Microsoft Windows) understøtter ClickOnce-programmer. ClickOnce-programmet til arbejdsgangseditoren kræver et kompatibelt 64-bit-operativsystem.
> -   Report Designer til finansiel rapportering startes som et ClickOnce-program. Det kræver et kompatibelt 64-bit-operativsystem. Hvis du bruger Chrome, skal du installere en ClickOnce-udvidelse for at kunne hente Report Designer-klienten. Hvis du bruger Chrome i incognito-tilstand, skal du kontrollere, at ClickOnce-udvidelsen også er aktiveret til incognito-tilstand.
> -   Hvis du vil se PDF-filer, anbefaler vi, at du bruger browsere som f.eks. Microsoft Edge (seneste offentligt tilgængelige version) i Windows 10 eller Google Chrome (seneste offentligt tilgængelige version) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tabletten.


### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Understøttede webbrowsere for Retail Cloud POS

Retail Cloud POS kan køre i en af følgende webbrowsere, der kører på de angivne operativsystemer:

-   Microsoft Edge (nyeste offentligt tilgængelige version) på Windows-10
-   Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
-   Chrome (seneste offentligt tilgængelige version) på Windows 10, Windows 8.1 eller Windows 7

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS-krav
### <a name="supported-operating-systems"></a>Understøttede operativsystemer

-   Retail Modern POS er et 32-bit-program, men det kan køre på både x86- og x64-arkitekturer.
-   Retail Modern POS understøttes kun på udgaverne Windows 10 Pro, Enterprise og Enterprise Long Term Servicing Branch (LTSB).

### <a name="minimum-system-requirements"></a>Minimumssystemkrav

-   Den mindste understøttede opløsning er 1280 × 1024.
-   Den computer, der kører Retail Modern POS, skal opfylde følgende krav:
    -   Den skal som minimum have en dual core-processor, der ikke kører mindre end 2 gigahertz (GHz).
    -   Den skal minimum have 3 gigabyte (GB) RAM.
    -   Den skal have adgang til internettet.

## <a name="retail-hardware-station-requirements"></a>Krav til Retail hardware station
### <a name="supported-operating-systems"></a>Understøttede operativsystemer

-   Retail hardware station er et 32-bit-program, men det kan køre på både x86- og x64-arkitekturer.
-   Retail hardware station understøttes på følgende operativsystemer:
    -   Windows 7 Professional-, Enterprise- og Ultimate-udgaverne 
    
    > [!NOTE]
    > Windows 7 understøttes kun, hvis Internet Explorer 11 installeres manuelt på systemet.

    -   Windows 8.1 Update 1 Professional-, Enterprise- og Embedded-udgaverne
    -   Windows 10 Pro-, Enterprise- og Enterprise LTSB-udgaverne

### <a name="minimum-system-requirements"></a>Minimumssystemkrav

Computeren skal opfylde alle systemkrav til installation og brug af følgende elementer:

-   IIS (Internet Information Services)
-   Tredjepartshardware

## <a name="retail-store-scale-unit-requirements"></a>Krav til vægtenhed til detailbutikker
### <a name="supported-operating-systems"></a>Understøttede operativsystemer

-   Vægtenhed til detailbutikker er et 32-bit-program, men det kan køre på både x86- og x64-arkitekturer.
-   Vægtenhed til detailbutikker understøttes på følgende operativsystemer:
    -   Windows 7 Professional-, Enterprise- og Ultimate-udgaverne
    -   Windows 8.1 Update 1 Professional-, Enterprise- og Embedded-udgaverne
    -   Windows 10 Pro-, Enterprise- og Enterprise LTSB-udgaverne

### <a name="minimum-system-requirements"></a>Minimumssystemkrav

-   4 GB RAM
-   1,6 GHz spidsbelastnings CPU-hastighed pr. processorkerne (to kerner er minimum).
-   Mindst 10 GB ledig plads (kanaldatabasen kan kræve en stor mængde plads.)

### <a name="recommended-system-requirements"></a>Anbefalede systemkrav

-   6 GB RAM
-   2,4 GHz i7 (eller tilsvarende) top CPU-hastighed pr. processorkerne (fire kerner anbefales.)
-   Mindst 10 GB ledig plads (kanaldatabasen kan kræve en stor mængde plads.)

## <a name="connector-requirements"></a>Krav til Connector
### <a name="supported-operating-systems"></a>Understøttede operativsystemer

-   Connector til Microsoft Dynamics AX har to separate installationsprogrammer, den **Async Server Connector-tjenesten** og **Real-time service for Dynamics AX 2012 R3**.
-   Begge komponenter er et 32-bit-program, men de kan køre på både x86- og x64-arkitekturer.
-   Begge komponenter understøttes på følgende operativsystemer:
    -   Windows 7 Professional-, Enterprise- og Ultimate-udgaverne
    -   Windows 8.1 Update 1 Professional-, Enterprise- og Embedded-udgaverne
    -   Windows 10 Pro-, Enterprise- og Enterprise LTSB-udgaverne
    -   Windows Server 2012 R2, Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimumssystemkrav

-   2 GB RAM, 4 GB RAM anbefales
-   1,6 GHz spidsbelastnings CPU-hastighed pr. processorkerne (to kerner er minimum).
-   Mindst 10 GB ledig plads (kanaldatabasen kan kræve en stor mængde plads.)

## <a name="requirements-for-development-on-local-vms"></a>Krav til udvikling på lokale virtuelle maskiner
Du kan finde oplysninger om kravene til udvikling på lokale virtuelle maskiner (VM'er), [VM, der kører i det lokale miljø](../dev-tools/access-instances.md).

# <a name="system-requirements-for-on-premises-deployments"></a>Systemkrav til installationer i det lokale miljø

## <a name="network-requirements"></a>Netværkskrav
Finance and Operations (on-premises) kan fungere på netværk, der bruger Internet Protocol version 4 (IPv4) eller Internet Protocol version 6 (IPv6). Overvej netværksmiljøet, når du planlægger systemet, og brug følgende retningslinjer.

### <a name="network-response-time"></a>Svartider på netværket
I følgende tabel vises netværkets minimumkrav til forbindelsen mellem webbrowser og AOS (Applikationsobjektserver) og til forbindelsen mellem AOS og databasen i et lokalt system.

| Værdi     | Webbrowser til AOS | AOS til database                                            |
|-----------|--------------------|------------------------------------------------------------|
| Båndbredde | 50 KBps pr. bruger   | 100 MBps                                                   |
| Ventetid   | < 250-300 ms       | < 1 ms (kun LAN). AOS og databasen skal placeres samme sted. |

- Finance and Operations (on-premises) er designet til netværk, der har en ventetid på 250-300 millisekunder (ms) eller mindre. Denne ventetid er fra en browserklient til datacenteret, der er vært for Finance and Operations.
- Kravene til båndbredde for Finance and Operations (on-premises) afhænger af scenariet. Typiske situationer kræver en båndbredde på mere end 50 kilobyte pr. sekund (KBps) mellem browseren og Finance and Operations-serveren. Men til scenarier, der har store datakrav, f.eks. arbejdsområder eller scenarier, der involverer omfattende tilpasning, anbefales en større båndbredde afhængigt af anvendelsen.
Installationer, hvor AOS og SQL Server-databasen er i forskellige datacentre, understøttes ikke. AOS og SQL Server-databasen skal være placeret samme sted. Generelt er Finance and Operations optimeret til at reducere trafikken mellem browser og server. Antallet af rundture fra en browserklient til datacenteret er enten nul eller én for hver brugerinteraktion, og dataene komprimeres.

> [!WARNING]
> Du må ikke beregne kravene til båndbredde fra en klientlokalitet ved at multiplicere antallet af brugere med minimumkravene til båndbredde. Den samtidig brug af en given lokalitet er meget vanskeligt at beregne. Det anbefales, at du bruger en reel simulering mod en forekomst af Finance and Operations i et ikke-produktionsmiljø som den bedste målestok for ydeevnen i dit tilfælde. 

### <a name="lan-environments"></a>LAN-miljøer
I LAN-miljøer (local area network), kræves Microsoft Fjernskrivebord i Microsoft Windows Server ikke for at oprette forbindelse til Finance and Operations. Dog kan det være påkrævet til vedligeholdelsesoperationer på de VM'er, der udgør serverinstallationerne.

### <a name="wan-environments"></a>WAN-miljøer
I WAN-miljøer (wide area network), kræves Fjernskrivebord i Windows Server ikke for at oprette forbindelse til Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Krav til internetforbindelse
Finance and Operations (on-premises) kræver ikke forbindelse til internettet fra slutbrugerarbejdsstationer. Dog vil nogle funktioner ikke være tilgængelige uden forbindelse til internettet.

| Browserklient | Et intranetmiljø uden internetforbindelse er et designpunkt for den lokale installation. Nogle funktioner, der kræver skytjenester, vil ikke være tilgængelige, det kan f.eks. være Hjælp- og opgaveguidebiblioteker i LCS. |
|----------------|----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Server         | AOS- eller Service Fabric-niveauer skal kunne kommunikere med LCS. Den lokale browserbaserede klient kræver ikke adgang til internettet.                                                                                |
| Telemetri      | Telemetridata kan gå tabt, hvis der er lange afbrydelser i forbindelsen. Afbrydelse af forbindelsen til LCS påvirker ikke funktionen af det lokale program.                                                |
| LCS            | Der kræves forbindelsen til LCS til installation, implementering af kode og vedligeholdelse.                                                                                                                                 |
## <a name="telemetry-data-transfer-to-the-cloud"></a>Overførsel af telemetridata til skyen
Det meste telemetri gemmes lokalt og kan ses ved hjælp af Logbog i Microsoft Windows. En lille del af telemetrihændelserne overføres til Microsofts telemetripipeline i skyen til diagnosticeringsformål. Kundedata og identificerbare slutbrugerdata indgår ikke i de telemetridata, der sendes til Microsoft. VM-navne sendes til Microsoft som hjælp til styring af miljøer og diagnosticering fra LCS-portalen.

## <a name="domain-requirements"></a>Domænekrav
Når du installerer Finance and Operations (on-premises), skal du overveje følgende domænekrav:

- Virtuelle maskiner, der er vært for Finance and Operations (on-premises)-komponenter, skal være medlem af et Active Directory-domæne. Active Directory-domænetjenester (AD DS) skal konfigureres i oprindelig tilstand.
- Virtuelle maskiner, der kører Finance and Operations (on-premises)-komponenter, der skal have adgang til hinanden, der er konfigureret i Active Directory-domænetjenester. 
- Domænecontrolleren skal køre på Microsoft Windows Server 2016.

## <a name="hardware-requirements"></a>Hardwarekrav
I dette afsnit beskrives den hardware, der kræves for at køre Finance and Operations (on-premises).
Baseret på systemkonfigurationen, datakompositionen og de programmer og funktioner, du vil bruge, varierer de faktiske hardwarekrav. Her er nogle af de faktorer, der kan påvirke valget af relevant hardware for Finance and Operations (on-premises):

- Antal enheder pr. time.
- Antal samtidige brugere.

## <a name="minimum-infrastructure-requirements"></a>Minimumkrav til infrastruktur
Finance and Operations (on-premises) bruger Microsoft Azure Service Fabric som vært for AOS, Batch, datastyring, Management Reporter og Orchestrator-miljøtjenester. Service Fabric-klyngen er ikke vært for Microsoft SQL Server Reporting Services (SSRS).
SQL Server skal konfigureres i en HADRON-konfiguration med høj tilgængelighed, der har mindst to noder til produktionsbrug.
I følgende illustration vises det mindste antal noder, der anbefales i Service Fabric-klyngen.

[![det anbefalede antal noder til service fabric-klynge](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Krav til processor og RAM
I følgende tabel vises antallet af processorer og den RAM (random-access memory), der er brug for til hver af de roller, der kræves for at køre denne installation. Du kan finde flere oplysninger ved at læse om de anbefalede minimumkrav til den enkeltstående Service Fabric-klynge, i [Planlægge og forberede Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Hvis der er installeret anden Microsoft-software på samme computer, skal systemet også opfylde kravene til hardware for de pågældende programmer. Vi anbefaler, at du begrænser andre serverprogrammer på den samme computer som AOS til 1 GB (gigabyte) RAM.

**Tilpasning efter rolle og topologitype**

| Topologi   | Rolle (nodetype)              | Anbefalede processorkerner | Anbefalet hukommelse (GB) |
|------------|-------------------------------|-----------------------------|-------------------------|
| Produktion | AOS, datastyring, batch   | 8                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |
| Sandkasse    | AOS, datastyring, batch   | 4                           | 24                      |
|            | Management Reporter           | 4                           | 16                      |
|            | SQL Server Reporting Services | 4                           | 16                      |
|            | Orchestrator                  | 4                           | 16                      |

**Estimater af minimumstørrelse for produktions- og sandkasseinstallationer**\*

| Topologi                                  | Rolle                          | Antal forekomster |
|-------------------------------------------|-------------------------------|---------------------|
| Produktion                                | AOS (datastyring, batch)  | 3                   |
|                                           | Management Reporter           | 2                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator\*\*                | 3                   |
| Sandkasse                                   | AOS, datastyring, batch   | 2                   |
|                                           | Management Reporter           | 1                   |
|                                           | SQL Server Reporting Services | 1                   |
|                                           | Orchestrator                  | 3                   |
| *Oversigt over produktions- og sandkassetopologier* |                               | 16                  |

\*Disse tal valideres af vores kunder, der bruger eksempelvisningen, og kan blive reguleret efter behov baseret på deres feedback.

\*\*Orchestrator er angivet som den primære nodetype og bruges også til at køre Service Fabric-tjenesterne.

**Indledende estimater af Back-end SQL Server og AD**

[![Indledende estimater af SQL Server og AD](./media/system-reqs-on-premises-02.PNG)](./media/system-reqs-on-premises-02.PNG) 

\*SQL Server-størrelser afhænger meget af arbejdsbelastningen. Du kan finde flere oplysninger i afsnittet [Tilpasning af hardware til lokale miljøer](#Hardware-sizing-for-on-premises-environments).

## <a name="storage"></a>Lagring

- **AOS** - Finance and Operations (on-premises) vil bruge et SMB-share 3.0 (Server Message Block) til at gemme ustrukturerede data. Du kan finde flere oplysninger i [Storage Spaces Direct i Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Relevante indstillinger:
    - Opsætning af et SSD-drev (solid-state drive) med høj tilgængelighed.
    - Et SAN (storage area network) optimeret til OLTP-gennemløb.
    - Højtydende DAS (Direct-attached Storage) 
- **SQL- og datastyrings-IOPS** – Lagringen for både datastyring og SQL Server skal have mindst 2.000 input/output-operationer pr. sekund (IOPS). Produktions-IOPS afhænger af mange faktorer. Du kan finde flere oplysninger i afsnittet "Tilpasning af hardware til lokale miljøer". 
- **IOPS for virtuelle maskiner** – Hver virtuel maskine skal have mindst 100 skrive-IOPS.

## <a name="virtual-host-requirements"></a>Krav til virtuel vært
Når du opretter de virtuelle er værter for et Finance and Operations (on-premises)-miljø, kan du se i følgende retningslinjer: [Planlægge og forberede Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) og [Beskrivelse af en Service Fabric-klynge](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Hver virtuelle vært skal have tilstrækkeligt mange kerner til den infrastruktur, der tilpasses. Der er mulighed for flere avancerede konfigurationer, hvor SQL Server placeres på fysisk hardware, mens alt andet er virtualiseret. Hvis SQL Server er virtualiseret, skal diskundersystemet være et hurtigt SAN eller tilsvarende. Sørg under alle omstændigheder for, at den grundlæggende opsætning af den virtuelle vært, har høj tilgængelighed og er redundant. I alle tilfælde, når virtualisering bruges, skal der ikke tages nogen VM-øjebliksbilleder.

## <a name="software-requirements-for-all-server-computers"></a>Krav til software for alle servere
Følgende software skal findes på en computer, før Finance and Operations (on-premises)-komponenter kan installeres:

- Microsoft .NET Framework 4.5.1 eller nyere
- Service Fabric. Du kan finde flere oplysninger i [Planlægge og forberede Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Understøttede serveroperativsystemer
I følgende tabel vises de serveroperativsystemer, der understøttes for Finance and Operations-komponenter.

| Operativsystem                                     | Notater                                                                                  |
|------------------------------------------------------|----------------------------------------------------------------------------------------|
| Microsoft Windows Server 2016 Datacenter eller Standard | Disse krav gælder for databasen og den Service Fabric-klynge, der er vært for AOS. |

## <a name="software-requirements-for-database-servers"></a>Krav til software for databaseservere

- Kun 64-bit versioner af SQL Server 2016 understøttes.
- I et produktionsmiljø anbefales det, at du installerer den seneste kumulative opdatering (CU) for den version af SQL Server, du bruger.
- Finance and Operations (on-premises) understøtter Unicode-sorteringer, hvor der skelnes mellem små og store bogstaver, accenter, kana, og hvor der skal tages forbehold for bredden. Sorteringen skal stemme overens med indstillingerne for landestandarder i Windows på de computere, der kører forekomster af AOS. Hvis du konfigurerer en ny installation, anbefales det, at du vælger en Windows-sortering frem for en SQL Server-sortering. Yderligere oplysninger om, hvordan du vælger en sortering til en SQL Server-database, finder du i [dokumentationen til SQL Server](/sql/sql-server/sql-server-technical-documentation).
I følgende tabel vises de SQL Server versioner, der understøttes til Finance and Operations-databaser. Du kan finde flere oplysninger i minimumhardwarekravene til [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Krav                                                      | Notater                                                                                                                     |
|------------------------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------|
| Microsoft SQL Server 2016 Standard Edition eller Enterprise Edition | Krav til hardware for SQL Server 2016 finder du i [Hardware og softwarekrav til installation af SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-client-computers"></a>Krav til software for klientservere
Finance and Operations-webprogrammet kan køre på alle enheder med en HTML5.0-kompatibel webbrowser. Specifikke kombinationer af enhed/browser, som Microsoft har bekræftet, omfatter:

- Microsoft Edge (nyeste offentligt tilgængelige version) på Windows-10
- Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
- Google Chrome (nyeste offentligt tilgængelige version) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tablet
- Apple Safari (nyeste offentligt tilgængelige version) på Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eller Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Softwarekrav til Active Directory Federation Services 
Active Directory Federation Services (AD FS) på Windows Server 2016

Domænecontrolleren skal være Windows Server 2012 R2 eller nyere med et domænefunktionsniveau for 2012 R2 eller derover

Du kan finde flere oplysninger om domænefunktionsniveauer i afsnittet: 
- [Hvad er Active Directory-funktionsniveauer?](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Om funktionsniveauer i Active Directory-domænetjenester](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Krav til hardware og software for Retail-komponenter
Finance and Operations (on-premises) omfatter ikke Retail-komponenter på nuværende tidspunkt.

<a name="see-also"></a>Se også
--------

[Få en evalueringskopi af Dynamics 365 for Finance and Operations, Enterprise edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)

