---
title: "Systemkrav til installationer i det lokale miljø"
description: "Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til installationer i det lokale miljø."
author: kfend
manager: AnnBe
ms.date: 08/02/2017
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
ms.author: kfend
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 25a6f326c57e84d6a7c356ac5407be7ed3095f83
ms.openlocfilehash: 5edc6f0b2240e9dd2d3b72a13f35e96f016aa013
ms.contentlocale: da-dk
ms.lasthandoff: 10/04/2017

---

# <a name="system-requirements-for-on-premises-deployments"></a>Systemkrav til installationer i det lokale miljø

[!include[banner](../includes/banner.md)]

Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til installationer i det lokale miljø. Før du installerer Finance and Operations, skal du evt. kontrollere, at det system, du bruger, opfylder eller overstiger minimumkrav til netværk, hardware og software.

## <a name="network-requirements"></a>Netværkskrav
Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (on-premises) kan bruges på netværk, der bruger Internet Protocol Version 4 (IPv4) eller Internet Protocol Version 6 (IPv6). Overvej netværksmiljøet, når du planlægger systemet, og brug følgende retningslinjer.

### <a name="network-response-time"></a>Svartider på netværket
I følgende tabel vises netværkets minimumkrav til forbindelsen mellem webbrowser og AOS (Applikationsobjektserver) og til forbindelsen mellem AOS og databasen i et lokalt system.

| Værdi     | Webbrowser til AOS                      | AOS til database |
|-----------|-----------------------------------------|------------------------------------------------------------------------------------------|
| Båndbredde | 50 kilobyte pr. sekund (KBps) pr. bruger | 100 MB (megabyte) pr. sekund (MBps) |
| Ventetid   | Mindre end 250-300 millisekunder (ms)     | Mindre end 1 ms (kun LAN [local area network ]). AOS og databasen skal placeres samme sted. |

- Finance and Operations (on-premises) er designet til netværk, der har en ventetid på 250-300 millisekunder (ms) eller mindre. Denne ventetid er fra en browserklient til datacenteret, der er vært for Finance and Operations.
- Kravene til båndbredde for Finance and Operations (on-premises) afhænger af scenariet. Typiske situationer kræver en båndbredde på mere end 50 KBps mellem browseren og Finance and Operations-serveren. Men vi anbefaler mere båndbredde til scenarier, der har store datakrav, f.eks. arbejdsområder eller omfattende tilpasning. Den specifikke mængde båndbredde afhænger af brug.

Installationer, hvor AOS og Microsoft SQL Server-databasen er i forskellige datacentre, understøttes ikke. AOS og SQL Server-databasen skal være placeret samme sted. 

Generelt er Finance and Operations optimeret til at reducere trafikken mellem browser og server. Antallet af rundture fra en browserklient til datacenteret er enten nul eller én for hver brugerinteraktion, og dataene komprimeres.

> [!WARNING]
> Du må ikke beregne kravene til båndbredde fra en klientlokalitet ved at multiplicere antallet af brugere med minimumkravene til båndbredde. Den samtidig brug af en given lokalitet er meget vanskeligt at beregne. Vi anbefaler, at du bruger en reel simulering mod en forekomst af Finance and Operations i et ikke-produktionsmiljø som den bedste målestok for ydeevnen i dit tilfælde. 

### <a name="lan-environments"></a>LAN-miljøer
I LAN-miljøer (local area network), kræves Microsoft Fjernskrivebord i Microsoft Windows Server ikke for at oprette forbindelse til Finance and Operations. Dog kan Fjernskrivebord være påkrævet til vedligeholdelsesoperationer på de virtuelle maskiner (VM'er), der udgør serverinstallationerne.

### <a name="wan-environments"></a>WAN-miljøer
I WAN-miljøer (wide area network) kræves Fjernskrivebord i Windows Server ikke for at oprette forbindelse til Finance and Operations.

### <a name="internet-connectivity-requirements"></a>Krav til internetforbindelse
Finance and Operations (on-premises) kræver ikke forbindelse til internettet fra brugerarbejdsstationer. Dog vil nogle funktioner ikke være tilgængelige, hvis der ikke er forbindelse til internettet.

|                    |   |
|--------------------|---|
| **Browserklient** | Et intranetmiljø uden internetforbindelse er et designpunkt for den lokale installation. Nogle funktioner, der kræver skytjenester, vil ikke være tilgængelige, det kan f.eks. være Hjælp- og opgaveguidebiblioteker i Microsoft Dynamics Lifecycle Services (LCS). |
| **Server**         | AOS- eller Microsoft Azure Service Fabric-niveauer skal kunne kommunikere med LCS. Den lokale browserbaserede klient kræver ikke adgang til internettet. |
| **Telemetri**      | Telemetridata kan gå tabt, hvis der er lange afbrydelser i forbindelsen. Afbrydelse af forbindelsen til LCS påvirker ikke funktionen af det lokale program. |
| **LCS**            | Der kræves forbindelsen til LCS til installation, implementering af kode og vedligeholdelse. |

## <a name="telemetry-data-transfer-to-the-cloud"></a>Overførsel af telemetridata til skyen
De fleste telemetridata gemmes lokalt og kan ses ved hjælp af Logbog i Microsoft Windows. En lille del af telemetrihændelserne overføres til Microsofts telemetripipeline i skyen til diagnosticeringsformål. Kundedata og identificerbare brugerdata indgår ikke i de telemetridata, der sendes til Microsoft. VM-navne sendes til Microsoft som hjælp til styring af miljøer og diagnosticering fra LCS-portalen.

## <a name="domain-requirements"></a>Domænekrav
Når du installerer Finance and Operations (on-premises), skal du overveje følgende domænekrav:

- VM'er, der er vært for Finance and Operations (on-premises)-komponenter, skal være medlem af et Active Directory-domæne. Active Directory-domænetjenester (AD DS) skal konfigureres i oprindelig tilstand.
- VM'er, der kører Finance and Operations (on-premises)-komponenter, der skal have adgang til hinanden. Denne adgang er konfigureret i Active Directory-domænetjenester. 
- Domænecontrolleren skal være Microsoft Windows Server 2012 R2 eller nyere, og domænefunktionsniveauet skal være 2012 R2 eller derover.

## <a name="hardware-requirements"></a>Hardwarekrav
I dette afsnit beskrives den hardware, der kræves for at køre Finance and Operations (on-premises).

De faktiske hardwarekrav varierer baseret på systemkonfigurationen, datakompositionen og de programmer og funktioner, du vil bruge. Her er nogle af de faktorer, der kan påvirke valget af relevant hardware for Finance and Operations (on-premises):

- Antal enheder pr. time
- Antal samtidige brugere

## <a name="minimum-infrastructure-requirements"></a>Minimumkrav til infrastruktur
Finance and Operations (on-premises) bruger Service Fabric som vært for AOS, Batch, datastyring, Management Reporter og Orchestrator-miljøtjenester. 

SQL Server skal have en HADRON-konfiguration med høj tilgængelighed, der har mindst to noder til produktionsbrug.

I følgende illustration vises det mindste antal noder, der anbefales til Service Fabric-klyngen.

[![Anbefalet antal noder til Service Fabric-klynge](./media/system-reqs-on-premises-01.png)](./media/system-reqs-on-premises-01.png) 

## <a name="processor-and-ram-requirements"></a>Krav til processor og RAM
I følgende tabeller vises antallet af processorer og den RAM (random-access memory), der er brug for til hver rolle, der kræves for at køre denne installation. Du kan finde flere oplysninger i de anbefalede minimumkrav til en enkeltstående Service Fabric-klynge i [Planlægge og forberede Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

> [!NOTE]
> Hvis der er installeret anden Microsoft-software på samme computer, skal systemet også opfylde kravene til hardware for de pågældende programmer. Hvis andre serverprogrammer er installeret på den samme computer som AOS, anbefaler vi, at du begrænser disse serverprogrammer til 1 GB (gigabyte) RAM.

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

**Estimater af minimumstørrelse for produktions- og sandkasseinstallationer\***

| Topologi                                        | Rolle                          | Antal forekomster |
|-------------------------------------------------|-------------------------------|---------------------|
| Produktion                                      | AOS (datastyring, batch)  | 3                   |
|                                                 | Management Reporter           | 2                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator\*\*              | 3                   |
| Sandkasse                                         | AOS, datastyring, batch   | 2                   |
|                                                 | Management Reporter           | 1                   |
|                                                 | SQL Server Reporting Services | 1                   |
|                                                 | Orchestrator                  | 3                   |
| *Oversigt over produktions- og sandkassetopologier* |                               | *16*                |

\* Tallene i denne tabel vurderes af kunder, der bruger eksempelvisningsversionen, og kan blive tilpasset baseret på feedback fra disse kunder.

\*\* Orchestrator er angivet som den primære nodetype og bruges også til at køre Service Fabric-tjenesterne.

**Indledende estimater af Back-end SQL Server og AD DS**

<table>
<thead>
<tr>
<th></th>
<th>Rolle</th>
<th>VM'er/forekomster</th>
<th>Kerner</th>
<th>Kerner i alt</th>
<th>Hukommelse (GB) pr. forekomst</th>
<th>Samlet hukommelse (GB)</th>
</tr>
</thead>
<tbody>
<tr>
<td rowspan="3"><strong>Delt infrastruktur</strong></td>
<td>SQL Server*</td>
<td>2</td>
<td>8</td>
<td>16</td>
<td>32</td>
<td>64</td>
</tr>
<tr>
<td>Filserver/SAN (storage area network)/lager med høj tilgængelighed</td>
<td colspan="5"><p>Backend-lagring skal baseres på SSD-drev (solid-state drive) på et kørsels-SAN (storage area network).</p>
<p>Størrelse og input/output-handlinger pr. antal gennemløb pr. sekund (IOPS) er baseret på størrelsen af arbejdsbyrden.</p></td>
</tr>
<tr>
<td>Active Directory</td>
<td>3</td>
<td>4</td>
<td>12</td>
<td>16</td>
<td>48</td>
</tr>
<tr>
<td><em>Oversigt over delt infrastruktur</em></td>
<td></td>
<td><em>5</em></td>
<td></td>
<td><em>28</em></td>
<td></td>
<td><em>112</em></td>
</tr>
</tbody>
</table>

\* SQL Server-størrelser afhænger meget af arbejdsbelastningen. Du kan finde flere oplysninger under [Tilpasning af hardware til lokale miljøer](hardware-sizing-on-premises-environments.md).

## <a name="storage"></a>Lagring

- **AOS** – Finance and Operations (on-premises) bruger et SMB-share 3.0 (Server Message Block) til at gemme ustrukturerede data. Du kan finde flere oplysninger i [Storage Spaces Direct i Windows Server 2016](/windows-server/storage/storage-spaces/storage-spaces-direct-overview).
- **SQL** – Følgende valgmuligheder er relevante:

    - En SSD-opsætning med høj tilgængelighed
    - Et SAN, som er optimeret til OLTP-gennemløb (online transaction processing)
    - Højtydende DAS (direct-attached storage) 

- **SQL Server- og datastyrings-IOPS** – Lagringen for både datastyring og SQL Server skal have mindst 2.000 IOPS. Produktions-IOPS afhænger af mange faktorer. Du kan finde flere oplysninger under [Tilpasning af hardware til lokale miljøer](hardware-sizing-on-premises-environments.md).
- **VM IOPS** – hver VM skal have mindst 100 skrive-IOP'er.

## <a name="virtual-host-requirements"></a>Krav til virtuel vært
Når du opretter de virtuelle er værter for et Finance and Operations (on-premises)-miljø, kan du se retningslinjerne i [Planlægge og forberede Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation) og [Beskrivelse af en Service Fabric-klynge](/azure/service-fabric/service-fabric-cluster-resource-manager-cluster-description). Hver virtuelle vært skal have tilstrækkeligt mange kerner til den infrastruktur, der tilpasses. Der er mulighed for flere avancerede konfigurationer, hvor SQL Server placeres på fysisk hardware, mens alt andet er virtualiseret. Hvis SQL Server er virtualiseret, skal diskundersystemet være et hurtigt SAN eller tilsvarende. Sørg under alle omstændigheder for, at den grundlæggende opsætning af den virtuelle vært, har høj tilgængelighed og er redundant. I alle tilfælde, når virtualisering bruges, skal der ikke tages nogen VM-øjebliksbilleder.

## <a name="software-requirements-for-all-server-computers"></a>Krav til software for alle servere
Følgende software skal findes på en computer, før Finance and Operations (on-premises)-komponenter kan installeres:

- The Microsoft .NET Framework version 4.5.1 eller nyere
- Service Fabric

Du kan finde flere oplysninger i [Planlægge og forberede Service Fabric-klyngen](/azure/service-fabric/service-fabric-cluster-standalone-deployment-preparation).

## <a name="supported-server-operating-systems"></a>Understøttede serveroperativsystemer
I følgende tabel vises de serveroperativsystemer, der understøttes for Finance and Operations-komponenter.

| Operativsystem                                     | Notater |
|------------------------------------------------------|-------|
| Microsoft Windows Server 2016 Datacenter eller Standard | Disse krav gælder for databasen og den Service Fabric-klynge, der er vært for AOS. |

## <a name="software-requirements-for-database-servers"></a>Krav til software for databaseservere

- Kun 64-bit versioner af SQL Server 2016 understøttes.
- I et produktionsmiljø anbefales det, at du installerer den seneste kumulative opdatering (CU) for den version af SQL Server, du bruger.
- Finance and Operations (on-premises) understøtter Unicode-sorteringer, hvor der skelnes mellem små og store bogstaver, accenter, kana, og hvor der skal tages forbehold for bredden. Sorteringen skal stemme overens med indstillingerne for landestandarder i Windows på de computere, der kører forekomster af AOS. Hvis du konfigurerer en ny installation, anbefales det, at du vælger en Windows-sortering frem for en SQL Server-sortering. Yderligere oplysninger om, hvordan du vælger en sortering til en SQL Server-database, finder du i [dokumentationen til SQL Server](/sql/sql-server/sql-server-technical-documentation).

I følgende tabel vises de SQL Server versioner, der understøttes til Finance and Operations-databaser. Du kan finde flere oplysninger i minimumhardwarekravene til [SQL Server](https://www.microsoft.com/en-us/sql-server/sql-server-2016).

| Krav                                                      | Notater |
|------------------------------------------------------------------|-------|
| Microsoft SQL Server 2016 Standard Edition eller Enterprise Edition | Krav til hardware for SQL Server 2016 finder du i [Hardware og softwarekrav til installation af SQL Server 2016](/sql/sql-server/install/hardware-and-software-requirements-for-installing-sql-server). |

## <a name="software-requirements-for-application-object-server-aos"></a>Krav til software til AOS (Applikationsobjektserver) 
- SQL Server Integration Services (SSIS)

## <a name="software-requirements-for-reporting-server-bi"></a>Krav til software til Reporting Server (BI)
- SQL Server Reporting Services (SSRS)

## <a name="software-requirements-for-client-computers"></a>Krav til software for klientservere
Finance and Operations-webprogrammet kan køre på alle enheder, der har en HTML 5.0-kompatibel webbrowser. Her er nogle specifikke kombinationer af enhed/browser, som Microsoft har bekræftet:

- Microsoft Edge (nyeste offentligt tilgængelige version) på Windows-10
- Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
- Google Chrome (nyeste offentligt tilgængelige version) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tablet
- Apple Safari (nyeste offentligt tilgængelige version) på Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eller Apple iPad

## <a name="software-requirements-for-active-directory-federation-services"></a>Softwarekrav til Active Directory Federation Services 
Active Directory Federation Services (AD FS) på Windows Server 2016 er påkrævet.

Domænecontrolleren skal være Windows Server 2012 R2 eller nyere, og domænefunktionsniveauet skal være 2012 R2 eller derover. Du kan finde flere oplysninger om domænefunktionsniveauer på følgende sider:

- [Hvad er Active Directory-funktionsniveauer?](https://technet.microsoft.com/en-us/library/cc787290(v=ws.10).aspx)
- [Om funktionsniveauer i Active Directory-domænetjenester](https://technet.microsoft.com/en-us/library/understanding-active-directory-functional-levels(v=ws.10).aspx)

## <a name="supported-microsoft-office-applications"></a>Understøttede Microsoft Office-programmer
Følgende Microsoft Office-programmer understøttes i installationerne af Finance and Operations i skyen og det lokale miljø:

-   Hvis du vil køre tilføjelsesprogrammer til Microsoft Excel og Microsoft Word, skal du have Microsoft Office 2016 til Windows eller Mac installeret. Du kan finde yderligere oplysninger om versionskrav i [Fejlfinding af Office-integration](../../dev-itpro/office-integration/office-integration-troubleshooting.md).
-   Hvis du vil have vist dokumenter, der er genereret med funktionerne Eksport til Excel eller Eksport til Word, skal have Microsoft Office 2007 eller nyere installeret.
 
## <a name="hardware-and-software-requirements-for-retail-components"></a>Krav til hardware og software for Retail-komponenter
Finance and Operations (on-premises) omfatter ikke Retail-komponenter på nuværende tidspunkt.

