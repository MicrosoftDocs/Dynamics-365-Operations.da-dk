---
title: Systemkrav for Talent
description: I dette emne beskrives kravene til Dynamics 365 Talent.
author: andreabichsel
manager: AnnBe
ms.date: 10/21/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: anbichse
ms.search.scope: Core, Operations, Talent
ms.custom: 63213
ms.assetid: 5dbc62fc-0184-4c0e-9856-e735fc68799e
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 509827d5736887f56e7754a0760af7dea76277f7
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460670"
---
# <a name="talent-system-requirements"></a>Systemkrav for Talent

[!include [banner](includes/banner.md)]

Dette emne indeholder beskrivelser af kravene til Microsoft Dynamics 365 Talent, herunder Attract og Onboard. Den beskriver også de lande og områder, hvor Talent er tilgængelig, samt oplysninger om sprog og lokalisering for Talent-data. I tilføjelser indeholder dette emne opdateringspolitikken for Talent.

## <a name="supported-web-browsers"></a>Understøttede webbrowsere

Microsoft Dynamics 365 Talent kan køre i en af følgende webbrowsere, der kører på de angivne operativsystemer: 

*   Microsoft Edge (nyeste offentligt tilgængelige version) på Windows 10
*   Internet Explorer 11 på Windows 10, Windows 8.1 eller Windows 7
*   Google Chrome (nyeste offentligt tilgængelige version)
*   Apple Safari (nyeste offentligt tilgængelige version)

Gå til producentens websted for at finde den nyeste version af hver webbrowser. 

> [!NOTE]
> * Hvis du vil hente billeder, der er genereret ud fra Arbejdsrutineoptager og inkludere dem i Microsoft Word-dokumenter, skal du have en Chrome-udvidelse installeret. 
> * Arbejdsgangseditoren startes som et ClickOnce-program. Kun Microsoft Edge og Internet Explorer (på en understøttet version af Microsoft Windows) understøtter ClickOnce-programmer. ClickOnce-programmet til arbejdsgangseditoren kræver et kompatibelt 64-bit-operativsystem.
> * Hvis du vil se PDF-filer, anbefaler vi, at du bruger moderne browsere, som Microsoft Edge (seneste offentligt tilgængelige version) i Windows 10 eller Google Chrome (seneste offentligt tilgængelige version) i Windows 10, Windows 8.1, Windows 8, Windows 7 eller Google Nexus 10-tabletten.
>   Netværkskrav
> * Dynamics 365 Talent er designet til netværk med ventetid på 250-300 millisekunder (ms) eller mindre. Dette er ventetiden fra en browserklient til Microsoft Azure-datacenteret, der er vært for Talent. Vi anbefaler, at du tester netværksventetiden på [www.azurespeed.com](https://www.azurespeed.com "Test af ventetid i Azure").
> * Kravene til båndbredde for Talent afhænger af dit scenarie. De fleste typiske scenarier kræver en båndbredde på mere end 50 kilobyte pr. sekund (KBps).
> 
> [!WARNING]
> Du må ikke beregne kravene til båndbredde fra en klientlokalitet ved at multiplicere antallet af brugere med minimumkravene til båndbredde. Den samtidig brug af en given lokalitet er meget vanskeligt at beregne. Til kunder, der er bekymret over kravene til båndbredde, kan du bruge en prøveversion af Talent.

## <a name="supported-microsoft-office-applications"></a>Understøttede Microsoft Office-applikationer

* Hvis du vil køre tilføjelsesprogrammer til Microsoft Excel og Word, skal du have Microsoft Office 2016 til Windows eller Mac installeret. Du kan finde yderligere oplysninger om versionskrav i [Fejlfinding af Office-integration](../dev-itpro/office-integration/office-integration-troubleshooting.md "Fejlfinding af Office-integration").
* Hvis du vil have vist dokumenter, der er genereret med funktionerne Eksport til Excel eller Eksport til Word, skal have Microsoft Office 2007 eller nyere installeret.

## <a name="regional-availability-languages-and-localization"></a>Regional tilgængelighed, sprog og lokalisering

Du kan hente en PDF-fil over de lande, områder og sprog, som Talent understøtter i [International tilgængelighed af Microsoft Dynamics 365](https://docs.microsoft.com/dynamics365/get-started/availability). 

> [!NOTE]
> Mens brugergrænsefladen er lokaliseret til andre sprog, gemmes alle brugerdata på det sprog, de blev indtastet på. Du kan oprette mails og skabeloner på andre sprog, men data som f.eks. planlægningsoplysninger, er kun tilgængelige på engelsk på nuværende tidspunkt.

Hvis du er udvikler, der er interesseret i at oprette lande- eller områdespecifikke tilpasninger, eller i at oprette en løsning for et land eller en region, der ikke understøttes af Microsoft, skal du se [Globalisering](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lcs-solutions/country-region).



[!INCLUDE[footer-include](../includes/footer-banner.md)]