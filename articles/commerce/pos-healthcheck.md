---
title: Sundhedstjek af eksterne POS-enheder og tjenester
description: Dette emne indeholder en oversigt over sundhedstjekhandlinger i POS.
author: rubendel
manager: AnnBe
ms.date: 03/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations, Retail
ms.custom: 141393
ms.assetid: e23e944c-15de-459d-bcc5-ea03615ebf4c
ms.search.region: Global
ms.search.industry: Retail
ms.author: rubendel
ms.search.validFrom: 2019-03-31
ms.dyn365.ops.version: AX 7.0.1
ms.openlocfilehash: 86f0964b6d929d0434a8bf04aaefc173bee21c6f
ms.sourcegitcommit: d77e902b1ab436e5ff3e78c496f5a70ef38e737c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/15/2020
ms.locfileid: "4411204"
---
# <a name="health-check-for-pos-peripherals-and-services"></a>Sundhedstjek af eksterne POS-enheder og tjenester

[!include [banner](includes/banner.md)]

I dette emne beskrives sundhedstjekhandlingen i POS.

## <a name="overview"></a>Overblik

Detailbutikker kan være komplekse miljøer, hvor der bruges mange programmer og enheder. I takt med at driften vokser, kan det blive vanskeligt at sikre sig, at handlinger altid kører problemfrit, på grund af afhængigheder af f.eks. eksterne enheder, der kan gå i stykker eller utilsigtet bliver koblet fra i løbet af en dag. Fejlfinding af problemer, der vedrører enheder og tjenester, kan være kostbar for større handlende og lige frustrerende i forbindelse med mindre handlinger.

Microsoft Dynamics 365 Commerce versioner 10.0.10 og nyere omfatter en sundhedstjek, der kan være med til at forhindre nogle af disse omkostninger og frustrationer. Denne handling angiver en metode til test af enheder direkte fra POS uden for normal drift. Derfor kan den hjælpe forhandlere med at finde problemer, før de opstår.

## <a name="key-terms"></a>Vigtige termer

| Periode | Beskrivende tekst |
|---|---|
| Eksterne enheder | Enhver enhed, som POS-programmet bruger til at lette transaktioner og andre handlinger i butikken. Eksemplerne omfatter pengeskuffer, stregkodescannere og betalingsterminaler. |
| Ydelse | I dette emne er en tjeneste et hjælpeprogram, som POS-programmet afhænger af for at udføre transaktioner og daglige handlinger. Eksempler kan være apps, der hjælper med beregning af skat eller forsendelse. |

## <a name="health-check-operation"></a>Handling af sundhedstjek

Handlingen Sundhedstjek er handling 717 på siden **POS-handlinger** i Commerce Headquarters. Den kan bruges, mens POS er i en tilstand uden en kasseskuffe. En hardwarestation skal dog være aktiv.

Som standard tester sundhedstilstand kun enheder, der er konfigureret i hardwareprofilen for den hardwarestation, der aktuelt er aktiv for et kasseapparat. Hvis et kasseapparat bruger flere hardwarestationer i løbet af en dag, skal du foretage sundhedstjek af alle dem, og der skal være forbindelse til én hardwarestation ad gangen. Der er ingen sundhedstjek på butiksniveau. Det er dog muligt, at denne type kontrol kan udføres via Commerce Server-udvidelsesmuligheder.

### <a name="out-of-box-health-checks"></a>Køreklar sundhedstjek

| Type | Forbindelse | Oplysninger |
|---|---|---|
| Printer | OPOS | Denne kontrol tester grundlæggende funktioner til objektsammenkædning og -integrering for POS-funktioner (OPOS). Her er nogle eksempler:<ul><li>Åbn: **Åbn** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Luk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Luk**</li></ul> |
| Linjevisning | OPOS | Denne kontrol tester grundlæggende OPOS-funktioner. Her er nogle eksempler:<ul><li>Åbn: **Åbn** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Luk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Luk**</li></ul> |
| Dobbeltvisning | Windows | Denne kontrol sikrer, at operativsystemet registrerer en ekstra Windows-visning. | 
| Magnetstribelæser | OPOS | Denne kontrol tester grundlæggende OPOS-funktioner. Her er nogle eksempler:<ul><li>Åbn: **Åbn** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Luk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Luk**</li></ul> |
| Kasseskuffe | OPOS | Denne kontrol tester grundlæggende OPOS-funktioner. Her er nogle eksempler:<ul><li>Åbn: **Åbn** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Luk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Luk**</li></ul> | 
| Scanner | OPOS | Denne kontrol tester grundlæggende OPOS-funktioner. Her er nogle eksempler:<ul><li>Åbn: **Åbn** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Luk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Luk**</li></ul> | 
| Målestok | OPOS | Denne kontrol tester grundlæggende OPOS-funktioner. Her er nogle eksempler:<ul><li>Åbn: **Åbn** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Luk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Luk**</li></ul> |
| Pinkodetastatur | OPOS | Denne kontrol tester grundlæggende OPOS-funktioner. Her er nogle eksempler:<ul><li>Åbn: **Åbn** &gt; **ClaimDevice** &gt; **DeviceEnabled=True**</li><li>Luk: **DeviceEnabled=False** &gt; **ReleaseDevice** &gt; **Luk**</li></ul> |
| Betalingsterminal | SDK-betalinger | Denne kontrol tester de grundlæggende terminalfunktioner til betalinger, der ydes af betalings-SDK'et. <ul><li>Lås</li><li>BeginTransaction</li><li>EndTransaction</li><li>ReleaseDevice</li><li>Afslutning</li></ul> |

### <a name="using-the-health-check-operation-in-the-pos"></a>Bruge handlingen Sundhedstjek i POS

Når Sundhedstjek aktiveres i POS, viser en rude til højre de konfigurerede enheder, og status for hver enkelt enhed vises. Hvis du vil foretage en sundhedstjek af en enkelt enhed, skal du markere enheden og derefter vælge **Test valgt**. Hvis du vil udføre sundhedstjek af alle enheder, skal du vælge **Test alle**. Funktionen **Test alle** tester alle enheder én ad gangen og opdaterer status for hver enkelt enhed i kolonnen **Status**.

Kolonnen **Sidste kontrol** viser, hvornår der sidst blev udført sundhedstjek for hver enhed.

Hvis sundhedstjekket for en enhed lykkes (dvs., hvis der ikke opstår fejl), vil enhedens status være **OK**. Hvis sundhedstjekket mislykkes, vil status angive, at der er opstået en fejl. I det tilfælde indeholder ruden til højre detaljer vedrørende fejlen, eller den giver brugeren besked om at kontakte systemadministratoren.

Nogle enheder, som f.eks. OPOS-låsen, har ikke et køreklart sundhedstjek. Hvis et sundhedstjek ikke registreres for en hvilken som helst enhed, der bruges, er status **Understøttes ikke**.

### <a name="extending-health-checks"></a>Udvidelse af sundhedstjek

De køreklare sundhedstjek er konfigureret til at give brugervenlige meddelelser til typiske fejl. Ikke alle scenarier er imidlertid dækket. Ved hjælp af udvidelsesmuligheder kan handlende knytte brugervenlige meddelelser til fejl, der kan være specifikke for deres miljø.

Der kan også oprettes brugerdefinerede sundhedstjek til at teste enheder, der ikke understøttes som køreklare, eller til at teste tjenester, som POS afhænger af.

## <a name="related-articles"></a>Relaterede artikler

[Modern POS-udløsere (MPOS) og udskrivning](dev-itpro/pos-trigger-printing.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]