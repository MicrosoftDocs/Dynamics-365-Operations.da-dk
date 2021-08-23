---
title: Oversigt over udligning for centraliserede betalinger
description: I dette emne beskrives udligning af centraliserede betalinger for Microsoft Dynamics 365 Finance.
author: abruer
ms.date: 08/02/2018
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.custom:
- "222414"
- intro-internal
ms.assetid: 610f6858-0f37-4d0f-8c68-bab5a971ef4a
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 30e8baea4bb7d6aabad36613a49f2d01ad58d1bbaff817efced5bb85f9835687
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6777114"
---
# <a name="settlement-overview-for-centralized-payments"></a>Oversigt over udligning for centraliserede betalinger

[!include [banner](../includes/banner.md)]

Organisationer, der omfatter flere juridiske enheder, kan oprette og administrere betalinger via en juridisk enhed, der håndterer alle betalinger. Derved fjernes behovet for at angive den samme postering i flere juridiske enheder, og der spares tid, idet processen til betalingsforslag, udligningsprocessen, redigering af åbne posteringer og redigering af lukkede posteringer strømlines for centraliserede betalinger. 

Når en debitor- eller kreditorbetaling angives i en juridisk enhed og udlignes med en faktura, der blev angivet i en andet juridisk enhed, genereres de relevante udligningsposteringer, forfalden til og forfalden fra, automatisk for hver juridisk enhed. Der oprettes en udligningspost for hver kombination af faktura og betaling i posteringen. Her enkelt udligningspost tildeles et nyt bilagsnummer, som er baseret på løbenummerserien, der angives på siden **Debitorparametre** for debitorer og siden **Kreditorparametre** for kreditorer. 

Hvis der genereres yderligere udligningsposter for kasserabatter, værdireguleringer af udenlandsk valuta, øredifferencer, overbetalinger eller underbetalinger, tildeles de den senere dato for betalings- eller fakturaposteringen. Hvis udligningen sker, efter at betalingen er bogført, bruger udligningsposterne den bogføringsdato for udligningen, der er angivet på siden **Udlign åbne posteringer**.

## <a name="posting-types-transaction-types-and-default-descriptions"></a>Bogføringstyper, posteringstyper og standardbeskrivelser

Bilagsposteringer for intern udligning bruges til den interne udlignings posteringstype, interne kundeudligning og interne kreditorudlignings posteringstyper. Du kan konfigurere oplysninger for posteringstypen på siden **Standardbeskrivelser**. 

Følgende posteringstyper kan bruges i udligninger i enkelte firmaer og i udligninger på tværs af firmaer.

-   Udligning
-   Kasserabat
-   Værdireguleringer af udenlandsk valuta (omfatter realiserede og ikke-realiserede værdireguleringer af udenlandsk valuta).
-   Øredifference
-   Overbetaling/underbetaling

Du kan også definere standardbeskrivelser af interne udligningsbilag.

## <a name="currency-exchange-gains-or-losses"></a>Valutakursvinding eller -tab

Den valutakurs, der bruges til debitor- og kreditorposteringer, lagres sammen med posteringen. Realiseret gevinst eller tab på valutakurser bogføres enten til den juridiske enhed for fakturaen eller til den juridiske enhed for betalingen, afhængig af hvilken indstilling der er valgt til feltet **Bogfør valutakurstab eller -vinding** på siden **Mellemregning** til den juridiske enhed for betalingen. Disse valutaer bruges i følgende eksempler:
-   Regnskabsvaluta for betaling: EUR
-   Regnskabsvaluta for faktura: USD
-   Transaktionsvaluta for betaling: DKK
-   Transaktionsvaluta for faktura: CAD

### <a name="currency-calculations"></a>Valutaberegninger

Når du udligner en faktura, der er angivet i én juridisk enhed, med en betaling, der er angivet i en anden juridisk enhed, omregnes transaktionsvalutaen for betalingen (DKK) i tre trin:
1.  Omregnes til regnskabsvalutaen for betalingen (EUR) ved brug af valutakurserne fra den juridiske enhed for betalingen.
2.  Omregnes til regnskabsvalutaen for fakturaen (USD).
3.  Omregnes til fakturaens transaktionsvaluta (CAD) ved brug af valutakurser fra den juridiske enhed for fakturaen.

I omregningsprocessen bruges valutakurserne på betalingsdatoen. Hvis den betalingsbeløbet i fakturaens transaktionsvaluta (CAD) er lig med fakturabeløbet (CAD), betragtes fakturaen som fuldt ud betalt. 

Når siden **Udlign åbne posteringer** åbnes i en betalingskladde, hvor betalingsbeløbet ikke er angivet, beregnes udligningsbeløbet på basis af de fakturaer, der er markeret til udligning på siden **Udlign åbne posteringer**. Udligningsbeløbet omregnes i tre trin:
1.  Omregnes til fakturaens regnskabsvaluta (USD) ved brug af valutakurserne fra den juridiske enhed for fakturaen pr. betalingsdatoen.
2.  Omregnes til regnskabsvalutaen for betalingen (EUR) ved brug af valutakurserne fra den juridiske enhed for fakturaen pr. betalingsdatoen.
3.  Omregnes til transaktionsvalutaen for betalingen (DKK).

Det beregnede betalingsbeløb overføres til betalingskladdelinjen, når du lukker siden **Udlign åbne posteringer**.

### <a name="posting-for-gain-or-loss-because-of-different-accounting-currencies"></a>Bogføring af vinding eller tab på grund af forskellige regnskabsvalutaer

Hvis der er valutakursvinding eller -tab, bogføres vindingen eller tabet til den juridiske enhed, der er angivet for feltet **Bogfør valutakurstab eller -vinding** på siden **Mellemregning** for den juridiske enhed for betalingen. Beløbet for vinding eller tab omregnes til regnskabsvalutaen for den juridiske enhed, hvor beløbet for vinding eller tab er bogført, ved hjælp af den valutakurs, der er angivet for den pågældende juridiske enhed.

## <a name="cash-discounts"></a>Kasserabatter

Kasserabatter, som genereres i forbindelse med udligninger på tværs af firmaer, bogføres enten til den juridiske enhed for fakturaen eller den juridiske enhed for betalingen afhængigt af, hvilken indstilling der er valgt for feltet **Bogfør kasserabat** på siden **Mellemregning** for den juridiske enhed for betalingen. Der genereres en tilsvarende udligningspostering i den juridiske enhed for fakturaen.

## <a name="overpayments-and-underpayments"></a>Overbetalinger og underbetalinger

Tolerancer for overbetalinger, underbetalinger og øredifferencer bestemmes på basis af den juridiske enhed for overbetalinger og på basis af den juridiske enhed for fakturaen for underbetalinger. Bogføringskontoen, der bruges, afhænger af indstillingen i feltet **Håndtering af kasserabat** på siden **Debitorparametre** for debitorer og feltet **Håndtering af kasserabat** på siden **Kreditorparametre** for kreditorer.

-   Hvis indstillingen for håndtering af kasserabat er Præcis, eller hvis indstillingen er Løs, og den relevante kasserabat bogføres i en anden juridisk enhed fra overbetalingen, anvendes den automatiske konto for Debitor, kasserabat, Kreditor kasserabat eller Øredifference i regnskabsvaluta. Du kan angive disse konti på siden **Konti til automatiske posteringer**.
-   Hvis indstillingen for håndtering af kasserabat er Løs, og kasserabatten bogføres i den samme juridiske enhed som overbetalingen (hvis den juridiske enhed for betalingen og den juridiske enhed for fakturaen er den samme), justeres kasserabatkontoen. Hvis en faktura på 100,00 med en mulig kasserabat på 3,00 f.eks. udlignes med en betaling på 98,00, justeres kasserabatkontoen for 1,00. Nettorabatbeløbet er 2,00.
-   Hvis indstillingen for håndtering af kasserabat er Løs, bogføres kasserabatten i den samme juridiske enhed som overbetalingen, og overbetalingen eller underbetalingen udlignes med flere fakturaer med kasserabatter, og kontoen for kasserabatten for den sidste faktura justeres.

Hvis indstillingen for håndtering af kasserabat er Løs, gælder de løse udligningsregler kun i følgende situationer:
-   Der findes en overbetaling.
-   Overbetalingen udlignes med en eller flere fakturaer, der indeholder en kasserabat.
-   Kasserabatten bogføres i samme juridiske enhed som overbetalingen.

I alle andre situationer bogføres overbetalinger eller underbetalinger på den automatiske konto for Debitor, kasserabat, Kreditor kasserabat eller Øredifference i regnskabsvalutaen.

## <a name="sales-tax"></a>Moms
Momsposteringer bliver i den juridiske enhed, hvor de oprindeligt blev bogført. 

Hvis der er blevet bogført moms for en forudbetaling, tilbageføres momsen for forudbetalingen i den juridiske enhed for forudbetalingen ved udligning på tværs af firmaer. Momsen i den juridiske enhed for fakturaen forbliver i den juridiske enhed for fakturaen.

## <a name="financial-dimensions"></a>Økonomiske dimensioner
For debitorbetalinger bruger posteringerne for forfalden til og forfalden fra i den juridiske enhed for betalingen de økonomiske dimensioner, der er angivet for samlekontoen for debitorer, fra den betaling, der udlignes. I den juridiske enhed for fakturaen bruger posteringerne for forfalden til og forfalden fra de økonomiske dimensioner, der er angivet for samlekontoen for debitorer, fra den faktura, der udlignes. 

For kreditorbetalinger bruger posteringerne for forfalden til og forfalden fra i den juridiske enhed for betalingen de økonomiske dimensioner, der er angivet for samlekontoen for kreditorer, fra den betaling, der udlignes. I den juridiske enhed for fakturaen bruger posteringerne for forfalden til og forfalden fra de økonomiske dimensioner, der er angivet for samlekontoen for kreditorer, fra den faktura, der udlignes.

## <a name="withholding-tax"></a>A-skat
Den kreditorkonto, der er tilknyttet fakturaen, bruges til at bestemme, om der skal beregnes A-skat. Hvis der beregnes A-skat, beregnes den i den juridiske enhed, der er tilknyttet fakturaen. Hvis der anvendes forskellige valutaer i de juridiske enheder, bruges valutakursen fra den juridiske enhed, der er tilknyttet fakturaen.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]