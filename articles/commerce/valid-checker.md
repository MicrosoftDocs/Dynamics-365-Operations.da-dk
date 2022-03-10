---
title: Validere butikstransaktioner til beregning af opgørelse
description: I dette emne beskrives funktionerne til validering af butikstransaktioner i Microsoft Dynamics 365 Commerce.
author: analpert
ms.date: 01/31/2022
ms.topic: index-page
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgriffin
ms.custom: ''
ms.assetid: ed0f77f7-3609-4330-bebd-ca3134575216
ms.search.region: global
ms.search.industry: Retail
ms.author: analpert
ms.search.validFrom: 2019-01-15
ms.dyn365.ops.version: 10
ms.openlocfilehash: f51b1f39aa212fe8587761721194db7791bec5bc
ms.sourcegitcommit: 7893ffb081c36838f110fadf29a183f9bdb72dd3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/02/2022
ms.locfileid: "8087443"
---
# <a name="validate-store-transactions-for-statement-calculation"></a>Validere butikstransaktioner til beregning af opgørelse

[!include [banner](includes/banner.md)]

I dette emne beskrives funktionerne til validering af butikstransaktioner i Microsoft Dynamics 365 Commerce. Valideringsprocessen identificerer og markerer transaktioner, der kan medføre bogføringsfejl, inden de hentes af bogføringsprocessen for opgørelsen.

Når du forsøger at bogføre en opgørelse, kan valideringsprocessen mislykkes på grund af uoverensstemmende data i tabellerne til handelstransaktioner. Her er nogle eksempler på faktorer, der kan forårsage disse uoverensstemmelser:

- Totalen for transaktionen i hovedtabellen stemmer ikke overens med transaktionstotalen på linjerne.
- Antallet af varer, der er angivet i hovedtabellen, svarer ikke til antallet af varer i transaktionstabellen.
- Momsen i hovedtabellen stemmer ikke overens med momsbeløb på linjerne. 

Hvis processen til bogføring af opgørelsen henter inkonsistente transaktioner, kan de salgsfakturaer og betalingskladder, der oprettes, medføre, at bogføring af opgørelsen mislykkes. Processen **Valider butikstransaktioner** forhindrer disse problemer ved at sikre, at kun de transaktioner, der overholder valideringsreglerne for transaktioner, overføres til beregningsprocessen for transaktionsopgørelsen.

I følgende illustration vises de gentagne processer i dagtimerne til overførsel af transaktioner, validering af transaktioner, beregning og bogføring af transaktionsopgørelser og processerne for afslutning af dagen i forhold til beregning og bogføring af regnskaber.

![Illustration vise de gentagne processer i dagtimerne til overførsel af transaktioner, validering af transaktioner, beregning og bogføring af transaktionsopgørelser og processerne for afslutning af dagen for beregning og bogføring af regnskaber.](./media/valid-checker-statement-posting-flow.png)

## <a name="store-transaction-validation-rules"></a>Valideringsregler for butikstransaktioner

Batchprocessen **Valider butiksposteringer** kontrollerer konsistensen af handelstransaktionstabellerne baseret på følgende valideringsregler.

> [!NOTE]
> Der vil fortsat blive tilføjet valideringsregler i de efterfølgende versioner.

### <a name="transaction-header-validation-rules"></a>Valideringsregler for transaktionshoveder

Følgende tabel indeholder de valideringsregler for transaktionshoveder, der kontrolleres i forhold til detailtransaktionshovedet, før disse transaktioner overføres til bogføring af opgørelser.

| Regel | Beskrivelse |
|-------|-------------|
| Forretningsdato | Denne regel validerer, at forretningsdagen for transaktionen er knyttet til en åben regnskabsperiode i Finans. |
| Valutaafrunding | Denne regel validerer, at transaktionsbeløbene afrundes i henhold til valutaafrundingsreglen. |
| Debitorkonto | Denne regel validerer, at den debitor, der bruges i transaktionen, findes i databasen. |
| Rabatbeløb | Denne regel validerer, at rabatbeløbet i hovedet er lig med summen af rabatbeløbene på linjerne. |
| Bogføringsstatus for regnskabsdokument (Brasilien) | Denne regel validerer, at regnskabsdokumentet kan bogføres korrekt. |
| Bruttobeløb | Denne regel validerer, at bruttobeløbet i transaktionshovedet matcher nettobeløbet, inklusive moms, af transaktionslinjerne plus gebyrer. |
| Netto | Denne regel validerer, at nettobeløbet i transaktionshovedet matcher nettobeløbet, eksklusive moms, af transaktionslinjerne plus gebyrer. |
| Netto + moms | Denne regel validerer, at bruttobeløbet i transaktionshovedet matcher nettobeløbet, eksklusive moms, af transaktionslinjerne plus alle momsangivelser og gebyrer. |
| Antal varer | Denne regel validerer, at antallet af varer, der er angivet i transaktionshovedet, svarer til summen af antal på transaktionslinjerne. |
| Betalingsbeløb | Denne regel validerer, at betalingsbeløbet i transaktionshovedet svarer til summen af alle betalingstransaktioner. |
| Beregning af momsfritagelse | Denne regel kontrollerer, at summen af det beregnede beløb og det fritagne momsbeløb for gebyrlinjer er lig med det oprindelige beregnede beløb. |
| Priser inklusive moms | Denne regel validerer, at flaget **Moms er inkluderet i priserne** er konsistent på tværs af transaktionshovedet og momstransaktionerne. |
| Transaktion ikke tom | Denne regel kontrollerer, at transaktionen indeholder linjer, og at mindst én linje ikke er erklæret ugyldig. |
| Under-/overbetaling | Denne regel validerer, at differencen mellem bruttobeløbet og betalingsbeløbet ikke er mere end konfigurationen af den maksimalt tilladte underbetaling/overbetaling. |

### <a name="transaction-line-validation-rules"></a>Valideringsregler for transaktionslinjer

Følgende tabel indeholder de valideringsregler for transaktionslinjer, der kontrolleres i forhold til linjedetaljerne for detailtransaktioner, før disse transaktioner overføres til bogføring af opgørelser.

| Regel | Beskrivelse |
|-------|-------------|
| Stregkode | Denne regel validerer, at alle varens stregkoder, der bruges på transaktionslinjerne, findes i databasen. |
| Gebyrlinjer | Denne regel kontrollerer, at summen af det beregnede beløb og det fritagne momsbeløb for gebyrlinjer er lig med det oprindelige beregnede beløb. |
| Returnering af gavekort | Denne regel validerer, at der ikke er nogen returneringer af gavekort i transaktionen. |
| Varevariant | Denne regel validerer, at alle varer og alle varianter, der bruges på transaktionslinjerne, findes i databasen. |
| Linjerabat | Denne regel validerer, at rabatbeløbet på linjen er lig med summen af rabattransaktionerne. |
| Linjemoms | Denne regel validerer, at momsbeløbet på linjen er lig med summen af momstransaktionerne. |
| Negativ pris | Denne regel validerer, at der ikke bruges nogen negative priser på transaktionslinjerne. |
| Styret af serienummer | Denne regel validerer, at serienummeret findes i transaktionslinjen for varer, der styres af serienummer. |
| Serienummerdimension | Denne regel kontrollerer, at der ikke er angivet et serienummer, hvis varens serienummerdimension er inaktiv. |
| Modstridende fortegn | Denne regel validerer, at antal og nettobeløb har samme fortegn i alle transaktionslinjerne. |
| Momsfritagelse | Denne regel kontrollerer, at summen af linjevareprisen og det fritagne momsbeløb er lig med den oprindelige pris. |
| Tildeling af momsgruppe | Denne regel validerer, at en kombination af momsgruppen og varemomsgruppen resulterer i et gyldigt momsskæringspunkt. |
| Konverteringer af måleenhed | Denne regel validerer, at måleenheden for alle linjer har en gyldig konvertering til lagermåleenheden. |

## <a name="enable-the-store-transaction-validation-process"></a>Aktivér valideringsprocessen for butikstransaktioner

Konfigurer jobbet **Valider butikstransaktioner** for periodiske kørsler i Commerce-hovedkontoret (**Retail og Commerce \> Retail og Commerce IT \> POS-bogføring**). Batchjobbet planlægges ud fra butikkens organisationshierarki. Det anbefales, at du konfigurerer denne batchproces til at køre med samme frekvens som batchjobbene **P-job** og **Beregn transaktionsopgørelser.**

## <a name="results-of-the-validation-process"></a>Resultater af valideringsprocessen

Resultaterne af batchprocessen **Valider butikstransaktioner** kan ses på hver enkelt detailbutikstransaktion. Feltet **Valideringsstatus** i transaktionsposten er angivet til **Fuldført**, **Fejl** eller **Ingen**. Feltet **Sidste valideringstidspunkt** viser datoen for den sidste valideringskørsel.

Følgende tabel beskriver de enkelte valideringsstatusser.

| Valideringsstatus | Beskrivelse |
|-------------------|-------------|
| Fuldført | Alle aktiverede valideringsregler blev overholdt. |
| Fejl | En aktiveret valideringsregel har identificeret en fejl. Du kan få vist flere detaljer om fejlen ved at vælge **Valideringsfejl** i handlingsruden. |
| Ingen | Transaktionstypen kræver ikke, at der anvendes valideringsregler. |

![Siden Butikstransaktioner, der viser feltet Valideringsstatus og knappen Valideringsfejl.](./media/valid-checker-validation-status-errors.png)

Det er kun transaktioner, der har valideringsstatussen **Fuldført**, der hentes ind i transaktionsopgørelserne. Hvis du vil have vist transaktioner med statussen **Fejl**, skal du gennemgå feltet **Cash and carry-valideringsfejl** i arbejdsområdet **Butiksregnskab**.

![Felter i arbejdsområdet Butiksregnskab.](./media/valid-checker-cash-carry-validation-failures.png)

Du kan finde flere oplysninger om, hvordan du løser cash and carry-valideringsfejl, under [Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner](edit-cash-trans.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Redigere og overvåge cash and carry-transaktioner og kassestyringstransaktioner](edit-cash-trans.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]
