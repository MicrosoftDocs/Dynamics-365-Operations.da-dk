---
title: Konsistenskontrol af detailtransaktion
description: Dette emne beskriver funktionen konsistenskontrol af detailtransaktion i Microsoft Dynamics 365 for Retail.
author: josaw1
manager: AnnBe
ms.date: 01/08/2019
ms.topic: index-page
ms.prod: ''
ms.service: dynamics-365-retail
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: db01a12b92574b41f1f4fe7281c23992e0d36027
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "302075"
---
# <a name="retail-transaction-consistency-checker"></a>Konsistenskontrol af detailtransaktion


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Dette emne beskriver funktionen konsistenskontrol af detailtransaktion, der blev introduceret i Microsoft Dynamics 365 for Finance and Operations, version 8.1.3. Konsistenskontrollen identificerer og isolerer inkonsistente posteringer, før de hentes af processen til bogføring af opgørelsen.

Når en opgørelse bogføres i Retail, kan bogføringen mislykkes på grund af inkonsistente data i detailtransaktionstabellerne. Dataproblemet kan skyldes uforudsete problemer med i POS-programmet, eller at transaktioner blev importeret forkert fra tredjeparts-POS-systemer. Eksempler på, hvordan denne inkonsistens kan vise sig, omfatter: 

  - Totalen for transaktionen i hovedtabellen stemmer ikke overens med transaktionstotalen på linjerne.
  - Linjeantallet i hovedtabellen stemmer ikke overens med antallet af linjer i transaktionstabellen.
  - Moms i hovedtabellen stemmer ikke overens med momsbeløb på linjerne. 
  
Når inkonsistente transaktioner hentes af processen til bogføring af opgørelsen, oprettes der inkonsekvente salgsfakturaer og betalingskladder, og hele bogføringsprocessen for opgørelsen mislykkes derfor. Gendannelsen af opgørelserne fra en sådan tilstand omfatter komplekse rettelser af data på tværs af flere transaktionstabeller. Konsistenskontrollen af detailtransaktioner forhindrer sådanne problemer.

I følgende diagram illustreres bogføringsprocessen med konsistenskontrollen af transaktioner.

![Processen til bogføring af opgørelse med konsistenskontrol af detailtransaktioner](./media/validchecker.png "Processen til bogføring af opgørelse med konsistenskontrol af detailtransaktioner")

Batchprocessen **Valider butikstransaktioner** kontrollerer konsistensen af detailtransaktionstabellerne i følgende scenarier.

- Debitorkonto - validerer, at debitorkontoen i detailtransaktionstabellerne findes i debitormasteren i hovedkontoret.
- Linjetæller - validerer, at antallet af linjer, som er angivet i transaktionshovedtabellen, svarer til antallet af linjer i salgstransaktionstabellerne.

## <a name="set-up-the-consistency-checker"></a>Konfigurere konsistenskontrollen
Konfigurer batchprocessen "Valider butiksposteringer" på **Detail \> Detail-it \> POS- bogføring** til periodiske kørsler. Batchjobbet kan planlægges ud fra butikkens organisationshierarki på samme måde som processerne "Beregn opgørelser i batch" og "Bogfør opgørelse i batch" er konfigureret. Det anbefales, at du konfigurerer denne batchproces til at køre flere gange i løbet af dagen og planlægger den, så den køres ved afslutningen af hver kørsel af P-job.

## <a name="results-of-validation-process"></a>Resultater af valideringsprocessen
Resultaterne af valideringskontrollen af batchprocessen markeres på den relevante detailtransaktion. Feltet **Valideringsstatus** på detailtransaktionsposten er enten angivet til **Fuldført** eller **Fejl**, og datoen for den seneste valideringskørsel vises i feltet **Sidste valideringstidspunkt**.

For at få vist mere beskrivende fejltekst, der vedrører en valideringsfejl, skal du vælge den relevante detailbutikstransaktionspost og klikke på knappen **Valideringsfejl**.

Transaktioner, der ikke består valideringskontrollen, og transaktioner, der endnu ikke blevet valideret, trækkes ikke ind i opgørelser. Under processen "Beregn opgørelse" får brugere besked, hvis der findes posteringer, der kunne have været medtaget i opgørelsen, men ikke blev det.

Hvis der findes en valideringsfejl, er den eneste måde at rette fejlen på, at kontakte Microsoft Support. I en senere version vil der blive tilføjet en funktion, så brugerne kan rette de poster, hvor der opstod fejl, via brugergrænsefladen. Logførings- og overvågningsfunktioner vil også blive tilgængelige, så historikken over ændringerne kan spores.

> [!NOTE]
> Der tilføjes yderligere valideringsregler for at understøtte flere scenarier i en senere version.
