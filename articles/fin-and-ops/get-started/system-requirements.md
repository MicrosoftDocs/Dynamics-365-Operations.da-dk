---
title: Systemkrav til skyinstallationer
description: Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til skyinstallationer.
author: sericks007
manager: AnnBe
ms.date: 08/02/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 8
ms.translationtype: HT
ms.sourcegitcommit: 5230911e1febc66b294f1331846373a472789adf
ms.openlocfilehash: 46eacb2a01c3bfcc7144c7d8c39ee0189fd72e16
ms.contentlocale: da-dk
ms.lasthandoff: 08/04/2017

---

# <a name="system-requirements-for-cloud-deployments"></a>Systemkrav til skyinstallationer

[!include[banner](../includes/banner.md)]

Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for Finance and Operations, Enterprise edition til skyinstallationer. Før du installerer Finance and Operations, skal du evt. kontrollere, at det system, du bruger, opfylder eller overstiger minimumkrav til netværk, hardware og software.

## <a name="supported-web-browsers"></a>Understøttede webbrowsere
Webprogrammet kan køre i en af følgende webbrowsere, der kører på de angivne operativsystemer:

-   Microsoft Edge (nyeste offentligt tilgængelige version) på Windows-10
-   Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
-   Google Chrome (nyeste offentligt tilgængelige version) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tablet
-   Apple Safari (nyeste offentligt tilgængelige version) på Mac OS X 10.10 (Yosemite), 10.11 (El Capitan) 10.12 (Sierra) eller Apple iPad

Gå til producentens websted for at finde den nyeste version af hver webbrowser. 

> [!NOTE]
> -   Du skal installere en foreløbig version af Chrome-udvidelsen, for at Arbejdsrutineoptager kan tage skærmbilleder og medtage dem i de Microsoft Word-dokumenter, der genereres. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/unified-operations/dev-itpro/user-interface/task-recorder).-->
> -   Arbejdsgangseditoren startes som et ClickOnce-program. Kun Microsoft Edge og Internet Explorer (på en understøttet version af Microsoft Windows) understøtter ClickOnce-programmer. ClickOnce-programmet til arbejdsgangseditoren kræver et kompatibelt 64-bit-operativsystem.
> -   Report Designer til finansiel rapportering startes som et ClickOnce-program. Det kræver et kompatibelt 64-bit-operativsystem. Hvis du bruger Chrome, skal du installere en ClickOnce-udvidelse for at kunne hente Report Designer-klienten. Hvis du bruger Chrome i Incognito-tilstand, skal du kontrollere, at ClickOnce-udvidelsen også er aktiveret til Incognito-tilstand.
> -   Hvis du vil se PDF-filer, anbefaler vi, at du bruger browsere som f.eks. Microsoft Edge (seneste offentligt tilgængelige version) i Windows 10 eller Google Chrome (seneste offentligt tilgængelige version) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tabletten.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Understøttede webbrowsere for Retail Cloud POS

Retail Cloud POS kan køre i en af følgende webbrowsere, der kører på de angivne operativsystemer:

-   Microsoft Edge (nyeste offentligt tilgængelige version) på Windows-10
-   Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
-   Chrome (seneste offentligt tilgængelige version) på Windows 10, Windows 8.1 eller Windows 7

## <a name="network-requirements"></a>Netværkskrav
-   Finance and Operations er designet til netværk, der har en ventetid på 250-300 millisekunder (ms) eller mindre. Denne ventetid fra en browserklient til Microsoft Azure-datacenteret, der er vært for Finance and Operations. Vi anbefaler, at du tester netværksventetiden på <http://www.azurespeed.com>.
-   Kravene til båndbredde for Finance and Operations afhænger af scenariet. De fleste typiske scenarier kræver en båndbredde på mere end 50 kilobyte pr. sekund (KBps). Men vi anbefaler mere båndbredde til scenarier, der har store datakrav, f.eks. arbejdsområder eller omfattende tilpasning.

Generelt er Finance and Operations optimeret til internettet. Antallet af rundture fra en browserklient til Azure-datacenteret er meget lille, og alle data komprimeres. 

> [!WARNING]
> Du må ikke beregne kravene til båndbredde fra en klientlokalitet ved at multiplicere antallet af brugere med minimumkravene til båndbredde. Den samtidig brug af en given lokalitet er meget vanskeligt at beregne. Kunder, der er bekymret over kravene til båndbredde, kan bruge en prøveversion af Finance and Operations.

## <a name="net-framework-requirements"></a>.NET Framework-krav
Finance and Operations kræver Microsoft .NET Framework version 4.6.2 til alle ClickOnce-programmer, f.eks. ruteplanlægningsagenten for dokumenter. Se installationsvejledning i [Installation af. NET Framework-](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Understøttede Microsoft Office-programmer
Følgende Microsoft Office-programmer understøttes i installationerne af Finance and Operations i skyen og det lokale miljø:

-   Hvis du vil køre tilføjelsesprogrammer til Microsoft Excel og Word, skal du have Microsoft Office 2016 til Windows eller Mac installeret. Du kan finde yderligere oplysninger om versionskrav i [Fejlfinding af Office-integration](/dynamics365/unified-operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   Hvis du vil have vist dokumenter, der er genereret med funktionerne Eksport til Excel eller Eksport til Word, skal have Microsoft Office 2007 eller nyere installeret.

## <a name="retail-modern-pos-requirements"></a>Retail Modern POS-krav

> [!NOTE]
> Hvis Retail Modern POS vil bruge en offlinedatabase, skal computeren opfylde alle systemkrav til Microsoft SQL Server. En Retail Modern POS-database fungerer på Microsoft SQL Server 2012 med Service Pack 3 eller nyere, Microsoft SQL Server 2014 med Service Pack 2 eller nyere og Microsoft SQL Server 2016. Det anbefales, at du altid bruger den nyeste version, der er tilgængelig, og at du installerer alle de nyeste service packs.

### <a name="supported-operating-systems"></a>Understøttede operativsystemer

-   Retail Modern POS er et 32-bit-program, men det kan køre på både x86- og x64-arkitekturer.
-   Retail Modern POS understøttes kun på udgaverne Windows 10 Pro, Enterprise og Enterprise Long Term Servicing Branch (LTSB).

### <a name="minimum-system-requirements"></a>Minimumssystemkrav

-   Den mindste understøttede opløsning er 1280 × 1024.
-   Den computer, der kører Retail Modern POS, skal opfylde følgende krav:

    -   Den skal som minimum have en dual core-processor, der ikke kører mindre end 2 gigahertz (GHz).
    -   Den skal minimum have 3 GB (gigabyte) RAM (random-access memory).
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

-   Connector til Microsoft Dynamics AX har to separate installationsprogrammer, et til Async Server Connector-tjenesten og et til Real-time service for Dynamics AX 2012 R3.
-   Begge komponenter er et 32-bit-program, men de kan køre på både x86- og x64-arkitekturer.
-   Begge komponenter understøttes på følgende operativsystemer:

    -   Windows 7 Professional-, Enterprise- og Ultimate-udgaverne
    -   Windows 8.1 Update 1 Professional-, Enterprise- og Embedded-udgaverne
    -   Windows 10 Pro-, Enterprise- og Enterprise LTSB-udgaverne
    -   Microsoft Windows Server 2012 R2 og Microsoft Windows Server 2016

### <a name="minimum-system-requirements"></a>Minimumssystemkrav
-   2 GB RAM (4 GB RAM anbefales).
-   1,6 GHz spidsbelastnings CPU-hastighed pr. processorkerne (to kerner er minimum).
-   Mindst 10 GB ledig plads (kanaldatabasen kan kræve en stor mængde plads.)

## <a name="requirements-for-development-on-local-vms"></a>Krav til udvikling på lokale virtuelle maskiner
Du kan finde oplysninger om kravene til udvikling på lokale virtuelle maskiner (VM'er), [VM, der kører i det lokale miljø](../dev-tools/access-instances.md).


## <a name="see-also"></a>Se også

[Få en evalueringskopi af Dynamics 365 for Finance and Operations, Enterprise edition](/dynamics365/unified-operations/dev-itpro/dev-tools/get-evaluation-copy)
