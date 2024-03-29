---
title: Bruge en betaling til at udligne fakturaer, der spænder over flere rabatperioder
description: Denne artikel viser, hvordan flere fakturaer betales, når hver enkelt faktura er berettiget til en kasserabat. Scenarierne i denne artikel fokuserer på, hvordan de kasserabatter, der anvendes, varierer, afhængigt af hvornår betalingen foretages.
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14511
ms.assetid: 3e42ccb5-b9d7-4a70-8db9-4206d10fd433
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 6bf321a5b0511295f2500f10cdffa9ff6f043bff
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780481"
---
# <a name="use-one-payment-to-settle-invoices-that-span-multiple-discount-periods"></a>Bruge en betaling til at udligne fakturaer, der spænder over flere rabatperioder

[!include [banner](../includes/banner.md)]

Denne artikel viser, hvordan flere fakturaer betales, når hver enkelt faktura er berettiget til en kasserabat. Scenarierne i denne artikel fokuserer på, hvordan de kasserabatter, der anvendes, varierer, afhængigt af hvornår betalingen foretages.

Fabrikam sælger varer til debitor 4032. Fabrikam tilbyder en kasserabat på 1 procent, hvis fakturaen betales i løbet af 14 dage. Fabrikam tilbyder også kasserabatter på delvise indbetalinger. Udligningsparametrene er placeret på siden **Kreditorparametre**.

## <a name="invoices"></a>Fakturaer
Debitor 4032 har tre fakturaer på i alt 3,000.00:

-   Faktura FTI-10040 på 1.000,00 blev bogført d. 15. maj. Denne faktura er berettiget til en kasserabat på 1 %, hvis den betales inden 14 dage.
-   Faktura FTI-10041 på 1.000,00 blev bogført d. 25. juni. Denne faktura er berettiget til en kasserabat på 1 %, hvis den betales inden 14 dage.
-   Faktura FTI-10042 på 1.000,00 blev bogført d. 25. juni. Denne faktura er berettiget til en kasserabat på 2 %, hvis den betales inden fem dage, og en rabat på 1 %, hvis den betales inden 14 dage.

## <a name="settle-all-invoices-on-june-29"></a>Udligne alle fakturaer d. 29 juni
Hvis Arnie opretter en betalingskladde for at udligne fakturaerne helt den 29. juni, er betalingen 2.970,00. Summen af alle rabatbeløb er 30,00. Arnie opretter en betaling for debitor 4032 og åbner derefter siden **Udlign posteringer**. På siden **Udlign posteringer** markerer Arnie alle tre fakturalinjer til udligning:

-   Betalingen for faktura FTI-10040 er 1.000,00. Der er ingen kasserabat.
-   Betalingen for faktura FTI-10041 er 990,00. En kasserabat på 1 %, eller 10,00, er medtaget.
-   Betalingen for faktura FTI-10042 er 980,00. En kasserabat på 2 %, eller 20,00, er medtaget.

| Foretag afmærkning | Anvend kasserabat | Bilag   | Konto | Dato   | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Valuta | Beløb, der skal udlignes |
|------|----------|-----------|---------|-----------|-----------|---------|---------------------|---------------------|----------|------------------|
| Valgt     | Normal      | FTI 10040 | 4032    | 15/5/2020 | 15/6/2020 | 10040   | 1,000.00  |                    | USD      | 1,000.00         |
| Valgt     | Normal      | FTI 10041 | 4032    | 25/6/2020 | 25/7/2020 | 10041   | 1,000.00  |                    | USD      | 990.00           |
| Markeret og fremhævet | Normal      | FTI 10042 | 4032    | 25/6/2020 | 25/7/2020 | 10042   | 1,000.00    |              | USD      | 980.00           |

Når betalingen er bogført, er debitorens saldo 0,00.

## <a name="settle-all-invoices-on-july-1"></a>Udligne alle fakturaer d. 1 juli
Hvis Arnie opretter en betalingskladde for at udligne fakturaerne helt den 1. juli, er betalingen 2.980,00. Arnie opretter en betaling for debitor 4032 og åbner derefter siden **Udlign posteringer**. På siden **Udlign posteringer** markerer Arnie alle tre fakturalinjer til udligning:

-   Betalingen for faktura FTI-10040 er 1.000,00. Der er ingen kasserabat.
-   Betalingen for faktura FTI-10041 er 990,00. En kasserabat på 1 %, eller 10,00, er medtaget.
-   Betalingen for faktura FTI-10042 er 990,00. En kasserabat på 1 %, eller 10,00, er medtaget. Selvom d. 1. juli er efter perioden, der giver en rabat på 2 %, er det stadig i perioden for rabatten på 1 %.

| Foretag afmærkning                     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Valuta | Beløb, der skal udlignes |
|----------|---------|-----------|---------|-----------|-----------|---------|--------------------|------------------|----------|------------------|
| Valgt         | Normal            | FTI 10040 | 4032    | 15/5/2020 | 15/6/2020 | 10040   | 1,000.00         |                | USD      | 1,000.00         |
| Valgt                 | Normal            | FTI 10041 | 4032    | 25/6/2020 | 25/7/2020 | 10041   | 1,000.00  |               | USD      | 990.00           |
| Markeret og fremhævet | Normal            | FTI 10042 | 4032    | 25/6/2020 | 25/7/2020 | 10042   | 1,000.00  |             | USD      | 990.00           |

## <a name="partial-settlement-on-june-29"></a>Delvis betaling 29. juni
Debitor 4032 kan betale et delbeløb, f.eks. halvdelen af hver faktura. Arnie opretter en betaling for debitor 4032 og åbner derefter siden **Udlign posteringer**. På siden **Udlign posteringer** markerer Arnie alle tre fakturalinjer til udligning. På hver linje angiver han udligningsbeløbet, baseret på de anvisninger, som debitoren gav. Når Arnie vælger en linje, ser han rabatbeløbet for den pågældende linje og det kasserabatbeløb, der er medtaget. Da debitoren betaler halvdelen af fakturaen, kan Arnie se, at værdien i feltet **Kasserabatbeløb** for FTI-10042 er **20,00**, men værdien i feltet **Medtaget kasserabat** er **10,00**. Betalingsbeløbet er 1.485,00.

| Foretag afmærkning   | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Valuta | Beløb, der skal udlignes |
|-------------|-------------------|-----------|---------|-----------|-----------|---------|-----------|------------------|----------|------------------|
| Valgt   | Normal       | FTI 10040 | 4032    | 15/5/2020 | 15/6/2020 | 10040   | 1,000.00        |               | USD      | 500.00           |
| Valgt                 | Normal            | FTI 10041 | 4032    | 25/6/2020 | 25/7/2020 | 10041   | 1,000.00     |     | USD      | 495,00           |
| Markeret og fremhævet | Normal            | FTI 10042 | 4032    | 25/6/2020 | 25/7/2020 | 10042   | 1,000.00     |         | USD      | 490,00           |

Arnie kan også manuelt angive betalingsbeløb på 1.485,00, før han åbner siden **Udlign posteringer**. Hvis han manuelt indtaster betalingsbeløbet og derefter markerer alle tre posteringer, men ikke justerer værdien i feltet **Beløb, der skal udlignes** for hver postering, modtager han følgende meddelelse, når han lukker siden:

> Totalbeløbet af markerede transaktioner er forskelligt fra kladdebeløbet. Vil du ændre kladdebeløbet?

Hvis Arnie ønsker, at betalingsbeløbet kun skal være 1.485,00, skal han klikke på **Nej** og derefter bogføre kladden. Posteringerne udlignes som følger:

1.  Faktura FTI-10040 udlignes helt for 1.000,00, da den blev indtastet d. 15. maj, og det er den ældste faktura. Der er ingen kasserabat. Det resterende beløb på betalingstransaktionen er 485,00.
2.  Faktura FTI-10041 udlignes ikke overhovedet. Fakturaer FTI-10041 og FTI 10042 blev indtastet på samme dato. Dog er der en rabat på 1 % for faktura FTI-10041, og rabat på 2 % for faktura FTI 10042. Da der ydes en større rabat på faktura FTI 10042, udlignes de resterende 485,00 med faktura FTI-10042.
3.  Faktura FTI-10042 udlignes med de resterende 485,00. Fabrikam tilbyder delrabatter. I så fald er rabatten 9,90 (= 485.00 ÷ 0,98 × 0,02). Beløbet (485,00) divideres med 0,98, fordi der er en rabat på 2 %, (så kunden betaler 98 % af fakturaen). Resultatet multipliceres derefter med rabatprocenten, eller 2 procent. Betalingen på 485,00 plus rabat på 9,90 er lig med 494,90. Beløbet på den oprindelige faktura var 1.000,00. Derfor har posteringen en balance på 505,10 (= 1.000,00-494,90).

Arnie kan se oplysningerne på siden **Debitorposteringer**.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo  | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI 10040  | Faktura          | 15/5/2020 | 10040   | 1,000.00                             |                                       | 0,00     | USD      |
| FTI 10041  | Faktura          | 25/6/2020 | 10041   | 1,000.00                             |                                       | 1,000.00 | USD      |
| FTI 10042  | Faktura          | 25/6/2020 | 10042   | 1,000.00                             |                                       | 505,10   | USD      |
| ARP-10040  | Betaling          | 29/6/2020 |         |                                      | 1.485,00                              | 0,00     | USD      |
| DISC-10040 | Kasserabat    | 29/6/2020 |         |                                      | 9,90                                  | 0,00     | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
