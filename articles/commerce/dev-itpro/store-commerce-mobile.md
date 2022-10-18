---
title: Store Commerce-app til mobilplatformer
description: I denne artikel beskrives, hvordan du kommer i gang med at bruge Microsoft Dynamics 365 Commerce Store Commerce-app til Android og iOS.
author: stuharg
ms.date: 10/07/2022
ms.topic: article
audience: Application User, Developer, IT Pro
ms.reviewer: v-chgriffin
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2018-10-29
ms.openlocfilehash: 1f07a130629863ebd9d036378436cf360e90ac26
ms.sourcegitcommit: 98231ff810f41f9fcdc6b536d87e453028aa6db8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/07/2022
ms.locfileid: "9642335"
---
# <a name="store-commerce-app-for-mobile-platforms"></a>Store Commerce-app til mobilplatformer

[!include [banner](../includes/banner.md)]

I denne artikel beskrives, hvordan du kommer i gang med at bruge Microsoft Dynamics 365 Commerce Store Commerce-apps til Android og iOS.

Mobilapps Dynamics 365 Commerce til Android og iOS gør processen til implementering af POS-enheder (full-fremhævede pos-enheder) til dit detailmiljø ligetil og simpel. Med Store Commerce-mobilapps kan du få alle funktionerne og fordelene ved [Store Commerce-appen til Windows](store-commerce.md) på formfaktorerne Telefon og tablet. Store Commerce-mobilapps kan installeres direkte fra butikkerne i Apple og Google Play app stores, og det er ikke nødvendigt, at en udvikler opretter en ny programpakke for at installere eller opdatere dem. 

Med Store Commerce Mobile-apps kan du bevare den fulde funktionalitet og de aktuelle Retail hybrid-apps. Store Commerce til iOS omfatter desuden understøttelse af en dedikeret hardwarestation, så iOS-enheder kan kommunikere med netværksbetalingsterminaler, kvitteringsprintere og pengeskuffer uden at kræve implementering af en delt hardwarestation. 

> [!IMPORTANT]
> Store Commerce-apps til Windows, Android og iOS er den næste generation af POS-programmer til Dynamics 365 Commerce. Det aktuelle MPOS-program (Modern POS) og [retail hybrid-apps](hybridapp.md) til mobil udfases i oktober 2023. Microsoft anbefaler, at du bruger Store Commerce eller Cloud POS (CPOS) til alle nye POS-installationer. Eksisterende kunder skal planlægge at overflytte fra Retail hybrid-appen til Store Commerce. Du kan finde flere oplysninger om afskrivningsplanen for MPOS og Retail hybrid-appsene i [Tilpasning af Dynamics 365 Commerce-teknologistakke i butikken](https://www.microsoft.com/download/details.aspx?id=103896). 

## <a name="app-architecture"></a>App-arkitektur

Store Commerce Mobile-apps bruger samme topologi som Store Commerce-appen til Windows, når den implementeres i hybridtilstand. Store Commerce Mobile-apps er shell-applikationer, der viser CPOS direkte fra Commerce Scale Unit (CSU), og som opretter forbindelse til konsolløst Commerce og Commerce Headquarters via CSU. Shell-applikationsmodellen gør det muligt for Store Commerce-apps at understøtte en dedikeret hardwarestation til direkte integration med en betalingsterminal, printer, pengeskuffe og andre eksterne enheder. Du behøver ikke at konfigurere en delt hardwarestation for at kunne bruge hardwareenheder. 

Hvis du vil opdatere en Store Commerce-mobilapp, skal du blot opdatere CSU. Alle nye kassefunktioner og -funktioner hentes automatisk af appen. Du kan finde flere oplysninger om, hvordan du opdaterer CSU, i [Anvend opdateringer og udvidelser til Commerce Scale Unit (cloud)](../../fin-ops-core/dev-itpro/deployment/update-retail-channel.md).

Shell-appsene er servicerede via opdateringer af app-butikken. Når en mindre version når den generelle tilgængelighed (GA), udgiver Microsoft den til appbutikkerne. Microsoft kan også udgive rettelser mellem mindre versionsopdateringer for at frigive rettelser med høj prioritet.

## <a name="prerequisites"></a>Forudsætninger

Store Commerce-mobilapps kræver Dynamics 365 Commerce, specifikt Commerce Headquarters og CSU-komponenter. Følgende tabel indeholder de minimum-os-versioner (operativsystem) og CSU-versioner, der kræves af Android og iOS-mobilapps. 

| Forudsætning | Android      | iOS  |
| ------------ | ------------ | ---- |
| OS-version   | 7.0          | 15.0 |
| CSU-version  | 9.38.22266.8 | Endnu ikke fastlagt  |

## <a name="install-the-app"></a>Installere appen

Du kan installere Store Commerce-mobilapps direkte fra Google Play-butikken eller Apple App Store. 

- [Store Commerce-app for Android](https://aka.ms/storecommerceandroid)
- Store Commerce-app til iOS (tilgængelig snart)

App-pakkerne Android (.apk) og Apple-app (.ipa) kan også hentes fra biblioteket Delte aktiver i Microsoft Dynamics Lifecycle Services. 

## <a name="device-and-register-setup"></a>Konfiguration af enhed og registrering

Før et kasseapparat kan aktiveres i Store Commerce-mobilapps, skal du konfigurere en enhed og et kasseapparat i Commerce Headquarters. Du kan finde flere oplysninger under [Enheder og registre](../implementation-considerations-devices.md). 

### <a name="device-setup"></a>Opsætning af enhed

Følg følgende fremgangsmåde for at oprette og konfigurere en ny enhed.

1. Gå i Commerce Headquarters til **Retail og Commerce \> Kanalkonfiguration \> POS-Konfiguration \> Enheder**. 
1. Opret en ny enhed, og vælg enten **Modern POS - Android** eller **Modern POS - iOS** som programtype, afhængigt af hvilken mobilapp du implementerer. 

    > [!NOTE] 
    > Programtyperne **Modern POS - Android** og **Modern POS - iOS** bruges også til at implementere de aktuelle hybridapps til Android og iOS. Når MPOS er blevet udfaset, vil labels for disse applikationstyper blive opdateret til **Store Commerce – Android** og **Modern POS - iOS**. 

### <a name="register-setup"></a>Opsætning af kasseapparatet

Du kan oprette et nyt kasseapparat og knytte det til den enhed, du har oprettet, eller du kan knytte et eksisterende kasseapparat til den nye enhed. Yderligere oplysninger om kasseapparater finder du i [Oprette og tilknytte kasseapparater](../tasks/create-associate-registers.md).

### <a name="screen-layout-setup"></a>Konfiguration af skærmlayout

Hvis du genbruger et skærmlayout, der indgår i de demodata, der følger med din Dynamics 365 Commerce-licens, vælger Store Commerce-appen automatisk det inkluderede layout, hvis din enheds skærmløsning er mindre end 480 &times; 853 pixel i stående retning. Men hvis du opretter et skærmlayout fra bunden, eller hvis din mobile enhed bruger en større opløsning end det tastaturlayout, der understøttes, skal du sikre dig, at du opretter en løsning og tilknyttede knapgitre, som er passende til den telefon eller tablet, du planlægger at implementere på. Yderligere oplysninger om konfigurationer af skærmlayout finder du i [visuelle konfigurationer til POS-brugergrænsefladen](../pos-screen-layouts.md). 

Når enheder og kasseapparater er konfigureret i Commerce headquarters, skal du gå til **Detail og handel \> Detail og handel-id \> Distributionsplaner** og køre kasseapparatjobbet.

## <a name="activate-a-device"></a>Aktivér en enhed

Hvis du vil aktivere en enhed på en Store Commerce-mobilapp, skal du følge disse trin.

1. Åbn appen på din mobilenhed.
1. Angiv URL-adressen til CPOS, som du kan finde på siden med miljøoplysninger i Lifecycle Services eller på siden **Kanalprofiler** i Commerce Headquarters (**Detail og handel \> Kanalopsætning \> Kanalprofiler**).
1. Log på ved hjælp af legitimationsoplysningerne for en arbejder, der har tilladelse til at administrere enheder.
1. Vælg den butik, der er tilknyttet det kasseapparat, du har oprettet eller genbruget i Commerce Headquarters.
1. Vælg det register, der er tilknyttet den enhed, du har oprettet i Commerce Headquarters.
1. Enheden bør nu være aktiveret. Du kan logge på registeret ved at bruge bruger-id og adgangskode for den arbejder, der er tilknyttet den valgte butik. 

Yderligere oplysninger om enhedsaktivering finder du i [POS-enhedsaktivering](retail-device-activation.md#activate-a-modern-pos-or-cloud-pos-device-by-using-guided-activation).

## <a name="feature-parity-with-store-commerce-for-windows"></a>Funktionsparitet med Store Commerce til Windows

I nedenstående tabel sammenlignes funktionerne i Store Commerce-appen på tværs af Windows-, Android og iOS-platforme.

| Funktion                                                                               | Windows | Android | iOS |
| ------------------------------------------------------------------------------------- | ------- | ------- | --- |
| Dedikeret hardwarestation                                                            | Ja     | Ja     | Ja |
| Delt hardwarestation                                                               | Ja     | Ja     | Ja |
| Kommunikation med netværkstilsluttede eksterne enheder (betalingsterminal, printer og pengeskuffe) | Ja     | Ja     | Ja |
| OLE for POS-eksterne enheder (OPOS) via en lokal hardwarestation             | Ja     | Nej      | Nej  |
| Offlinetilstand                                                                          | Ja     | Nej      | Nej  |

## <a name="additional-resources"></a>Yderligere ressourcer

[Store Commerce-app](store-commerce.md)

[Vælge mellem Store Commerce og Cloud POS](../mpos-or-cpos.md)

[Foretage fejlfinding af problemer ved opsætning og installation af Store Commerce](../troubleshoot/store-commerce-setup-installation.md)
