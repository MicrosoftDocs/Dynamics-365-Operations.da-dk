---
title: Konsistenskontrol af detailtransaktion
description: Dette emne beskriver funktionen konsistenskontrol af transaktion i Dynamics 365 Commerce.
author: josaw1
manager: AnnBe
ms.date: 10/14/2019
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
ms.openlocfilehash: 3da8bdf6feb932e074680b6cb80e1b7b71f9a82b
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3004245"
---
# <a name="retail-transaction-consistency-checker"></a>Konsistenskontrol af detailtransaktion


[!include [banner](includes/banner.md)]
[!include [preview banner](includes/preview-banner.md)]

Dette emne beskriver funktionen konsistenskontrol af transaktion i Microsoft Dynamics 365 Commerce. Konsistenskontrollen identificerer og isolerer inkonsistente transaktioner, før de hentes af processen til bogføring af opgørelsen.

Når en opgørelse er bogført, kan bogføringen mislykkes på grund af inkonsistente data i Commerce-transaktionstabellerne. Dataproblemet kan skyldes uforudsete problemer i POS-programmet, eller at transaktioner blev importeret forkert fra tredjeparts-POS-systemer. Eksempler på, hvordan denne inkonsistens kan vise sig, omfatter: 

- Totalen for transaktionen i hovedtabellen stemmer ikke overens med transaktionstotalen på linjerne.
- Linjeantallet i hovedtabellen stemmer ikke overens med antallet af linjer i transaktionstabellen.
- Moms i hovedtabellen stemmer ikke overens med momsbeløb på linjerne. 

Når inkonsistente transaktioner hentes af processen til bogføring af opgørelsen, oprettes der inkonsekvente salgsfakturaer og betalingskladder, og hele bogføringsprocessen for opgørelsen mislykkes derfor. Gendannelsen af opgørelserne fra en sådan tilstand omfatter komplekse rettelser af data på tværs af flere transaktionstabeller. Konsistenskontrollen af transaktioner forhindrer sådanne problemer.

I følgende diagram illustreres bogføringsprocessen med konsistenskontrollen af transaktioner.

![Processen til bogføring af opgørelse med konsistenskontrol af transaktioner](./media/validchecker.png "Processen til bogføring af opgørelse med konsistenskontrol af detailtransaktioner")

Batchprocessen **Valider butiksposteringer** kontrollerer konsistensen af Commerce-transaktionstabellerne i følgende scenarier.

- **Debitorkonto** – validerer, at debitorkontoen i transaktionstabellerne findes i debitormasteren i hovedkontoret.
- **Linjetæller** – validerer, at antallet af linjer, som er angivet i transaktionshovedtabellen, svarer til antallet af linjer i salgstransaktionstabellerne.
- **Pris inkl. moms** – validerer, at parameteren **Pris inkl. moms** er konsistent på tværs af transaktionslinjer.
- **Betalingsbeløb** - validerer, at betalingsposterne svarer til betalingsbeløbet i hovedet.
- **Bruttobeløb** – validerer, at bruttobeløbet i hovedet er summen af nettobeløbene på linjerne plus momsbeløbet.
- **Nettobeløb** – validerer, at nettobeløbet i hovedet er summen af nettobeløbene på linjerne.
- **Under-/overbetaling** – validerer, at differencen mellem bruttobeløbet i hovedet og betalingsbeløbet ikke overskrider konfigurationen af den maksimalt tilladte underbetaling/overbetaling.
- **Rabatbeløb** – validerer, at rabatbeløbet på rabattabellerne og rabatbeløbet i tabellerne for transaktionslinjer er konsistente, og at rabatbeløbet i hovedet er summen af rabatbeløbene på linjerne.
- **Linjerabat** – validerer, at linjerabatten på transaktionslinjen er summen af alle linjer i rabattabellen, der svarer til transaktionslinjen.
- **Gavekortvare** – Commerce understøtter ikke returnering af gavekortvarer. Saldoen på et gavekort kan dog udbetales kontant. Alle gavekortvarer, der behandles som en returlinje i stedet for en udbetalingslinje, mislykkes i bogføringsprocessen for opgørelsen. Valideringsprocessen for gavekortvarer er garanti for, at de eneste returneringslinjer for gavekortvarer i transaktionstabellerne er udbetalingslinjer for gavekort.
- **Negativ pris** – validerer, at der ikke er nogen negative pristransaktionslinjer.
- **Vare og variant** – validerer, at varer og varianter på transaktionslinjerne findes i masterfilen for vare og variant.
- **Momsbeløb** - validerer, at momsposter svarer til momsbeløbene på linjerne.
- **Serienummer** - validerer, at serienummeret findes i posteringslinjerne for varer, der styres af serienummer.
- **Fortegn** - validerer, at fortegnet på antallet og nettobeløbet er det samme i alle posteringslinjerne.
- **Forretningsdato** - validerer, at de økonomiske perioder for alle forretningsdatoerne for transaktionerne er åbne.

## <a name="set-up-the-consistency-checker"></a>Konfigurere konsistenskontrollen

Konfigurere batchprocessen "Valider butiksposteringer" på **Retail og Commerce \> Retail og Commerce IT \> POS-bogføring** til periodiske kørsler. Batchjobbet kan planlægges ud fra butikkens organisationshierarki på samme måde som processerne "Beregn opgørelser i batch" og "Bogfør opgørelse i batch" er konfigureret. Det anbefales, at du konfigurerer denne batchproces til at køre flere gange i løbet af dagen og planlægger den, så den køres ved afslutningen af hver kørsel af P-job.

## <a name="results-of-validation-process"></a>Resultater af valideringsprocessen

Resultaterne af valideringskontrollen af batchprocessen markeres på den relevante transaktion. Feltet **Valideringsstatus** på transaktionsposten er enten angivet til **Fuldført** eller **Fejl**, og datoen for den seneste valideringskørsel vises i feltet **Sidste valideringstidspunkt**.

For at få vist mere beskrivende fejltekst, der vedrører en valideringsfejl, skal du vælge den relevante butikstransaktionspost og klikke på knappen **Valideringsfejl**.

Transaktioner, der ikke består valideringskontrollen, og transaktioner, der endnu ikke blevet valideret, trækkes ikke ind i opgørelser. Under processen "Beregn opgørelse" får brugere besked, hvis der findes posteringer, der kunne have været medtaget i opgørelsen, men ikke blev det.

Hvis der findes en valideringsfejl, er den eneste måde at rette fejlen på, at kontakte Microsoft Support. I en senere version vil der blive tilføjet en funktion, så brugerne kan rette de poster, hvor der opstod fejl, via brugergrænsefladen. Logførings- og overvågningsfunktioner vil også blive tilgængelige, så historikken over ændringerne kan spores.

> [!NOTE]
> Der tilføjes yderligere valideringsregler for at understøtte flere scenarier i en senere version.