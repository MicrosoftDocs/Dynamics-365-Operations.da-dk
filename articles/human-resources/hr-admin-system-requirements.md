---
title: Systemkrav
description: Denne artikel angiver systemkravene for Microsoft Dynamics 365 Human Resources.
author: twheeloc
ms.date: 08/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: SystemAdministrationWorkspaceForm
audience: Application User
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: b07d14dfe0e6b53c9489c284520a24b97d9887fa
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8879331"
---
# <a name="system-requirements"></a>Systemkrav

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

Denne artikel angiver systemkravene for Microsoft Dynamics 365 Human Resources. Den beskriver også de lande og områder, hvor Human Resources er tilgængelig, og oplysninger om sprog og lokalisering for Human Resources-data.

## <a name="supported-web-browsers"></a>Understøttede webbrowsere

Brugere kan åbne Microsoft Dynamics 365 Human Resources fra en af følgende webbrowsere, som kører på de angivne operativsystemer: 

*   Microsoft Edge (nyeste offentligt tilgængelige version) på Windows 10
*   Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
*   Google Chrome (nyeste offentligt tilgængelige version)
*   Apple Safari (nyeste offentligt tilgængelige version)

Gå til producentens websted for at finde den nyeste version af hver webbrowser. 

## <a name="special-considerations"></a>Særlige overvejelser

* Hvis du vil aktivere Arbejdsrutineoptager for at tage skærmbilleder og medtage dem i de Microsoft Word-dokumenter, der genereres, skal du installere en foreløbig version af Chrome-udvidelsen.
* Arbejdsgangseditoren startes som et ClickOnce-program. Kun Microsoft Edge og Internet Explorer (på en understøttet version af Microsoft Windows) understøtter ClickOnce-programmer. ClickOnce-programmet til arbejdsgangseditoren kræver et kompatibelt 64-bit-operativsystem.
* Hvis du vil se PDF-filer, anbefaler vi, at du bruger moderne browsere, som Microsoft Edge (seneste offentligt tilgængelige version) i Windows 10 eller Google Chrome (seneste offentligt tilgængelige version) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tabletten.

## <a name="network-requirements"></a>Netværkskrav

* Human Resources er designet til netværk med ventetid på 250-300 millisekunder (ms) eller mindre. Dette er ventetiden fra en browserklient til Microsoft Azure-datacenteret, der er vært for Human Resources. Vi anbefaler, at du tester netværksventetiden på [www.azurespeed.com](https://www.azurespeed.com "Test af ventetid i Azure").
* Kravene til båndbredde for Human Resources afhænger af dit scenarie. Typiske scenarier kræver en båndbredde på mere end 50 kilobyte pr. sekund (KBps).
 
> [!WARNING]
> Du må ikke beregne kravene til båndbredde fra en klientlokalitet ved at multiplicere antallet af brugere med minimumkravene til båndbredde. Den samtidig brug af en given lokalitet er meget vanskeligt at beregne. Til kunder, der er bekymret over kravene til båndbredde, kan du bruge en prøveversion af Human Resources.

## <a name="supported-microsoft-office-applications"></a>Understøttede Microsoft Office-applikationer

* Hvis du vil køre tilføjelsesprogrammer til Microsoft Excel og Word, skal du have Microsoft Office 2016 til Windows eller Mac installeret. Du kan finde yderligere oplysninger om versionskrav i [Fejlfinding af Office-integration](../fin-ops-core/dev-itpro/office-integration/office-integration-troubleshooting.md "Fejlfinding af Office-integration").
* Hvis du vil have vist dokumenter, der er genereret med funktionerne Eksport til Excel eller Eksport til Word, skal have Microsoft Office 2007 eller nyere installeret.

## <a name="regional-availability-languages-and-localization"></a>Regional tilgængelighed, sprog og lokalisering

Du kan hente en PDF-fil over de lande, områder og sprog, som Human Resources understøtter i [International tilgængelighed af Microsoft Dynamics 365](/dynamics365/get-started/availability). 

> [!NOTE]
> Mens brugergrænsefladen er lokaliseret til andre sprog, gemmes alle brugerdata på det sprog, de blev indtastet på. Du kan oprette emails og skabeloner på andre sprog, men data som f.eks. planlægningsoplysninger, er kun tilgængelige på engelsk på nuværende tidspunkt.

Hvis du er udvikler, der er interesseret i at oprette lande- eller områdespecifikke tilpasninger, eller i at oprette en løsning for et land eller en region, der ikke understøttes af Microsoft, skal du se [Globalisering](/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).

[!INCLUDE[footer-include](../includes/footer-banner.md)]
