---
title: Nyheder eller ændringer i Warehouse Management-mobilappen
description: Dette emne viser de nye og ændrede funktioner for hver frigivet version af Warehouse Management-mobilappen til Microsoft Dynamics 365 Supply Chain Management.
author: ivanv-microsoft
ms.date: 07/30/2021
ms.topic: article
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ivanv
ms.search.validFrom: 2021-06-07
ms.dyn365.ops.version: 10.0.21
ms.openlocfilehash: 6d98cea29f4c25319caed6680966f61c660778f0
ms.sourcegitcommit: 3d05bb2a423fe130700686ff73daa355d15b0e09
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/16/2021
ms.locfileid: "7386093"
---
# <a name="whats-new-or-changed-in-the-warehouse-management-mobile-app"></a>Nyheder eller ændringer i Warehouse Management-mobilappen

[!include [banner](../includes/banner.md)]

Dette emne viser de nye funktioner, rettelser, forbedringer og kendte problemer for hver frigivet version af Warehouse Management-mobilappen til Microsoft Dynamics 365 Supply Chain Management.

## <a name="version-2090"></a>Version 2.0.9.0

Denne version løser en fejl, hvor appen ikke længere kan reagere, hvis brugere går opad fra toppen af en liste.

## <a name="version-2080"></a>Version 2.0.8.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Tilføjet understøttelse af [funktionen med trininstruktioner](mobile-app-titles-instructions.md), der blev introduceret i Supply Chain Management version 10.0.21.
- Tilføjet tipanimation for at vise brugere, at de kan lukke overlejringer ved at swipe nedad.
- Tilføjet understøttelse af funktionstaster på handlingslister og menuer. Brugerne kan holde enhver funktionstast nede i tre sekunder for at få vist en oversigt over tilgængelige kommandoer.
- Løst en fejl, der medførte, at følgende fejlmeddelelse blev vist på visse enheder: "Der kan ikke findes en egnet visning til den angivne størrelse".
- Løst en fejl, hvor fuld skærm-tilstand ikke altid fungerer, når skærmtastaturet bruges.
- Løst en fejl, hvor sideswiping ikke fungerer på Windows-enheder.
- Har løst forskellige problemer, der forårsagede, at systemet ikke længere svarede.

## <a name="version-2070"></a>Version 2.0.7.0

### <a name="new-features-fixes-and-improvements-in-version-2070"></a>Nye funktioner, rettelser og forbedringer i version 2.0.7.0

- Har føjet et afsnit til siden **Om**, hvor den seneste version af appen er kontrolleret.
- Har gjort det nemmere svippe og stryge gennem sider.
- Har ændret ikonet for knappen stigende/faldende på opgavelisten.
- Har reduceret margenerne på **Detalje**-kortet, så der er plads til flere oplysninger.
- Har anvendt forskellige forbedringer af ydeevnen for at reducere problemer med, at appen bliver langsommere med tiden.
- Hvis der er flere kontrolelementer, end de kan være på skærmen, hvilket medfører sideskift, ruller drejekontrolelementet ikke længere samme vej som siden.
- Har prioriteret at vise den senest scannede værdi frem for visning af opgavens titel, så hvis de overlapper, afkortes opgavens titel.
- Har løst forskellige problemer, der forårsagede, at systemet ikke længere svarede.
- Tekst forskellige steder afskæres ikke længere på visse sprog.
- Appen kører nu som standard i fuld skærm.
- Har løst et problem, der fra tid til anden ville medføre, at scanninger blev ignoreret på hovedsiden med bestemte enheder.

### <a name="known-issues-in-version-2070"></a>Kendte problemer i version 2.0.7.0

- På visse enheder vises følgende fejlmeddelelse, når du starter appen eller påbegynder en opgave: "Der kan ikke findes en passende visning til den angivne størrelse". Hvis du får vist denne fejlmeddelelse på nogen af dine enheder, skal du nedgradere mobilappen Warehouse Management til version 2.0.6.0 på den pågældende enhed og vente med at opgradere, indtil næste version af appen frigives.

## <a name="version-2060"></a>Version 2.0.6.0

### <a name="new-features-fixes-and-improvements-in-version-2060"></a>Nye funktioner, rettelser og forbedringer i version 2.0.6.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- I demotilstand vises nu alle etiketter på enhedssproget.
- Det er mindre sandsynligt, at du får følgende fejlmeddelelse: "Der kan ikke findes en passende visning til den angivne størrelse".
- Minimumshøjden for arbejdskort er øget (i tilfælde hvor tre eller færre felter konfigureres til at blive vist på opgavelisten).
- Margener (udtoning) nederst i detaljekort er blevet forbedret.
- Ugyldige symboler i XML-filer, der udveksles med serveren, håndteres nu korrekt. (Tegn, der ikke kan udskrives, håndteres for eksempel nu igen korrekt og medfører ikke længere, at appen holder op med at svare).
- HTTP-fejl (for eksempel "fejl 503"), når der sendes en serveranmodning, håndteres nu korrekt.
- Mens der vises en fejl, vises indstillingslisten ikke længere automatisk for kontrolelementer af typen kombinationsboks.
- Appen holder ikke længere op med at svare på grund af den visningsretning, der er valgt i brugerindstillingerne.
- Produktbilleder vises nu i selvbetjeningsmiljøer. (Denne ændring gælder kun for versioner med lav opløsning. Filstyringstjenesten understøtter ikke billeder i fuld størrelse i selvbetjeningsmiljøer).
- En fejl, der involverede korte pluk med nul antal, er blevet løst.
- Appen holder ikke længere op med at svare, når et detaljekort viser flere identiske felter.

### <a name="known-issues-in-version-2060"></a>Kendte problemer i version 2.0.6.0

Der findes følgende kendte problemer i denne version:

- Appen (især opgavelisten) bliver langsommere over tid.
- **Windows-version:** Når en USB-drev bruges til scanning i Windows, medfører uoverensstemmende resultater, at scannede symboler blandes sammen.

## <a name="version-2050"></a>Version 2.0.5.0

I denne version introduceres følgende nye funktioner, rettelser og forbedringer.

- Klienthemmeligheden skjules ikke længere i opsætningen af forbindelsesindstillinger.
- Du kan nu trykke længe på enhver tekst for at se den i fuld længde.
- Fejlmeddelelsen, når der mangler lagertilladelser, er blevet forbedret.
- Der er tilføjet nye kontrolsekvenser for nogle flow.
- Knappen Send bliver ikke længere tilgængelig på grund af størrelsesvinduet.
- Skydere kan nu fortsætte på mindre skærme, når der bruges store knapstørrelser.
- Overlejringen med fire knapper kan ikke længere afskæres.
- Nu understøttes knappen Delete på tastaturet.
- Et problem med lysstyrke, der kan forekomme, når der trykkes på tastaturet, er løst.
- Der er løst forskellige problemer med demodata.
- Et problem, der havde indflydelse på numeriske felter på detaljesiden, er blevet løst.
- Skærmtastaturet forsvinder ikke længere fra tid til anden på nogle enheder.
- Flere forskellige problemer med brugergrænsefladen, for eksempel fejl, der havde indflydelse på baggrundsfarven og positionen, er løst.
- Den russiske brugergrænseflade er blevet forbedret.
- Forskellige problemer, der forårsagede, at systemet ikke længere svarede, er blevet løst.
- Et problem, der var relateret til genåbningen af regnemaskinen, er blevet løst.
- **Android-version:** Der er løst et problem, hvor Android 4.4 holdt op med at svare ved start.
- **Android-version:** Minimumskalering er reduceret til 50 procent.

## <a name="version-2040"></a>Version 2.0.4.0

Version 2.0.4.0 var den første generelt tilgængelige version af Warehouse Management-mobilappen.

### <a name="new-features-fixes-and-improvements-in-version-2040"></a>Nye funktioner, rettelser og forbedringer i version 2.0.4.0

Denne version indeholder følgende nye funktioner, rettelser og forbedringer, som ikke var tilgængelige i forhåndsversionen:

- Hvis et detaljekort indeholder to etiketter, der har identiske data, skjules den ene af etiketterne.
- Specialtegn vises nu som standard, og muligheden for at skjule dem er blevet fjernet fra brugerindstillingerne.
- Deaktiverede send-knapper vises nu som ikke-tilgængelige i håndholdt visning.
- En ændring i sekvenslogikken for kontroller sikrer en mere problemfri skalering på tværs af enheder. Der er derfor mindre behov for at justere skaleringen af skrifttyper eller knapper.
- Standardfarvetemaet er ændret til *Mørk*.
- Det manglende ikon for den deaktiverede send-knap er blevet tilføjet på båndet.
- Timeoutundtagelser åbner nu forbindelsessiden i stedet for at vise en linjefejl.
- Hvis der ikke er en tilgængelig send-handling (for eksempel **OK**, **Ja**, **Accepter**, **Udført** eller **Udført**), deaktiveres knappen Send.
- Appens stabilitet er blevet forbedret.
- Der findes en rettelse til sikkerhedsrisikoen [CVE-2021-26701](https://msrc.microsoft.com/update-guide/vulnerability/CVE-2021-26701).
- **Windows-version:** Et problem i Windows, hvor menuerne ikke reagerede, efter at størrelsen på vinduet var blevet ændret, er blevet løst.

### <a name="known-issue-in-version-2040"></a>Kendt problem i version 2.0.4.0

Der findes følgende kendte problem i denne version:

- Denne version har et problem med enheder, der bruger Android 4.4. Du kan opleve problemer, når du bruger appen på denne version af Android.
