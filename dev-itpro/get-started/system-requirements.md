---
title: Systemkrav
description: Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for operationer.
author: sericks007
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User, Developer, IT Pro
ms.search.scope: Core
ms.custom: 55651
ms.assetid: e564d51d-42d3-47c5-b388-93b8219c692a
ms.search.region: Global
ms.author: sericks
ms.search.validFrom: 2016-08-30
ms.dyn365.ops.version: Platform update 2
translationtype: Human Translation
ms.sourcegitcommit: c8c96dc9705688308dd4a5c720700ddc17657d75
ms.openlocfilehash: 9220c093d3f6d6700127c93651db4083be300311
ms.lasthandoff: 03/31/2017


---

# <a name="system-requirements"></a>Systemkrav

Dette emne viser systemkravene til den aktuelle version af Microsoft Dynamics 365 for operationer.

<a name="supported-web-browsers"></a>Understøttede webbrowsere
----------------------

Microsoft Dynamics 365 for operationer webprogram kan køre i en af følgende browsere, der kører på de angivne operativsystemer:

-   Microsoft Edge (seneste offentligt tilgængelige version) på Windows-10
-   Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
-   Google Chrome (seneste offentligt tilgængelige version) på Windows 10, Windows 8.1, Windows 8, Windows 7 eller 10 af Google Nexus tablet
-   Apple Safari (seneste offentligt tilgængelige version) på Mac OS X 10,10 (Yosemite), 10.11 (El Capitan) eller 10.12 (Sierra) eller Apple iPad

Gå til producentens websted for at finde den nyeste version af hver webbrowser. **Bemærkninger:**

-   Hvis du vil hente billeder, der er genereret ud fra Arbejdsrutineoptager og inkludere dem i Microsoft Word-dokumenter, skal du have en Chrome-udvidelse, der er installeret. <!---For instructions about how to install the extension, see [Screenshot Extension setup](/dynamics365/operations/dev-itpro/user-interface/task-recorder).-->
-   Arbejdsgangseditoren er startet som en ClickOnce-program. Kun Microsoft Edge og Internet Explorer (på en understøttet version af Microsoft Windows) understøtter ClickOnce-programmer. Arbejdsgangseditoren ClickOnce-programmet kræver et kompatibelt 64-bit-operativsystem.
-   Report Designer til finansiel rapportering er startet som en ClickOnce-program. Det kræver et kompatibelt 64-bit-operativsystem. Hvis du bruger Chrome, skal du installere en ClickOnce-udvidelse for at hente report designer-klienten. Hvis du bruger Chrome i incognito-tilstand, skal du kontrollere ClickOnce-udvidelsen også er aktiveret til incognito-tilstand.

### <a name="supported-web-browsers-for-retail-cloud-pos"></a>Understøttede webbrowsere for Retail Cloud POS

Retail POS for sky for Dynamics 365 for operationer kan køre i en af følgende browsere, der kører på de angivne operativsystemer:

-   Microsoft Edge (seneste offentligt tilgængelige version) på Windows-10
-   Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
-   Chrome (seneste offentligt tilgængelige version) på Windows-10, Windows 8.1 eller Windows 7

## <a name="network-requirements"></a>Netværkskravene.
-   Dynamics 365 for operationer er designet til netværk med ventetid på mindre end 150 millisekunder (ms). Dette er ventetid fra en browser-klient til Microsoft Azure datacenter, der er vært Dynamics 365 for operationer. Vi anbefaler, at du tester netværksventetid på <http://www.azurespeed.com>.
-   Kravene til båndbredde for Dynamics 365 for operationer afhænger af din situation. Mest typiske situationer kræver en båndbredde på mere end 50 kilobyte pr. sekund (KBps). Scenarier, der har behov for høj payload, som arbejdsområder eller situationer, der involverer omfattende tilpasning, anbefales mere båndbredde, men.

Generelt er Dynamics 365 for operationer optimeret til internettet. Antallet af trafik fra en browser-klient til Azure datacenteret er meget små, og hele data komprimeres. **Advarsel:** ikke beregne kravene til båndbredde fra en placering for klienten ved at multiplicere antallet af brugere med minimal båndbredde kravene. Samtidig brug af en given lokation er meget vanskeligt at beregne. For kunder, der er bekymret over kravene til båndbredde, kan du bruge en prøveversion af Dynamics 365 for operationer.

## <a name="net-framework-requirements"></a>.NET Framework-krav
Dynamics 365 for operationer kræver.NET Framework version 4.6.2 for alle Klik-når programmer, som routing agenten dokument. Installationsvejledning, se [installation af.NET Framework-](https://msdn.microsoft.com/en-us/library/5a4x27ek(v=vs.110).aspx).

## <a name="supported-microsoft-office-applications"></a>Understøttede Microsoft Office-programmer
-   Hvis du vil køre Microsoft Excel og Word-tilføjelsesprogrammer, skal du have Microsoft Office 2016 til Windows eller Mac installeret. Se yderligere oplysninger om versionskrav til [fejlfinding af Office-integration](/dynamics365/operations/dev-itpro/office-integration/office-integration-troubleshooting).
-   For at få vist dokumenter, der genereres ved eksport til Excel eller eksporteres til Word-funktioner, du skal have Microsoft Office 2007 eller nyere installeret.

## <a name="retail-modern-pos-requirements"></a>Retail POS moderne krav
### <a name="supported-operating-systems"></a>Understøttede operativsystemer

-   Moderne detail-POS er et 32-bit program, men det kan køre på både x86 og x64-arkitekturer.
-   Moderne detail-POS understøttes kun på Windows 10 Pro, Enterprise og Enterprise lang sigt Servicing gren (LTSB)-udgaver.

### <a name="minimum-system-requirements"></a>Mindste systemkrav

-   Den mindste understøttede opløsning er 1280 × 1024.
-   Den computer, der kører moderne detail-POS skal opfylde følgende krav:
    -   Den skal have, skal som minimum en dual core-processor, der kører på ikke mindre end 2 gigahertz (GHz).
    -   Den skal have, minimum 3 gigabyte (GB) RAM.
    -   Den skal have adgang til internettet.

## <a name="retail-hardware-station-requirements"></a>Retail station hardwarekrav
### <a name="supported-operating-systems"></a>Understøttede operativsystemer

-   Retail hardware station er et 32-bit program, men det vil køre på både x86 og x64-arkitekturer.
-   Retail hardware station understøttes på følgende operativsystemer:
    -   Windows 7 Professional, Enterprise og Ultimate-udgaverne **Bemærk:** Windows 7 understøttes kun, hvis Internet Explorer 11 manuelt er installeret på systemet.
    -   Udgaver af Windows 8.1 Update 1 Professional, Enterprise og integreret
    -   Windows 10 Pro, Enterprise og LTSB Enterprise editions

### <a name="minimum-system-requirements"></a>Mindste systemkrav

Computeren skal opfylde alle krav til installation og brug af følgende elementer:

-   IIS (Internet Information Services)
-   Tredjepartshardware

## <a name="retail-store-scale-unit-requirements"></a>Retail Store skala enhed krav
### <a name="supported-operating-systems"></a>Understøttede operativsystemer

-   Detailbutik skala enhed er et 32-bit program, men det vil køre på både x86 og x64-arkitekturer.
-   Detailbutik skala enhed understøttes på følgende operativsystemer:
    -   Windows 7 Professional, Enterprise og Ultimate-udgaverne
    -   Udgaver af Windows 8.1 Update 1 Professional, Enterprise og integreret
    -   Windows 10 Pro, Enterprise og LTSB Enterprise editions

### <a name="minimum-system-requirements"></a>Mindste systemkrav

-   4 GB RAM
-   1,6 GHz spidsbelastning CPU-hastighed pr. processorkerne (to kerner er minimum).
-   Mindst 10 GB ledig plads (kanal databasen kan kræve en stor mængde plads.)

### <a name="recommended-system-requirements"></a>Anbefalede systemkrav

-   6 GB RAM
-   2.4 GHz i7 (eller tilsvarende) top CPU hastighed pr. processorkerne (fire kerner anbefales.)
-   Mindst 10 GB ledig plads (kanal databasen kan kræve en stor mængde plads.)

## <a name="requirements-for-development-on-local-vms"></a>Krav til udviklingen af lokale FOS
Finde oplysninger om kravene til udviklingen på det lokale virtuelle maskiner (VM'er), [VM kører på stedet](/dynamics365/operations/dev-itpro/dev-tools/access-instances#vm-that-is-running-in-premises).

<a name="see-also"></a>Se også
--------

[Få en vurderingsversion af Dynamics 365 til operationer](/dynamics365/operations/dev-itpro/dev-tools/get-evaluation-copy)


