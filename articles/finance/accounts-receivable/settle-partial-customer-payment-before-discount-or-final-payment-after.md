---
title: Udligne en delvis betaling før rabatdatoen med en endelig betaling efter rabatdatoen
description: I denne artikel beskrives virkningen af afregning af betalinger til fakturaer for debitorer. Scenariet fokuserer på effekterne på reskontroen, ikke på Finans.
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 4f6b4527a9f176857e0cc6ba4665688dc8721ac1
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9780452"
---
# <a name="settle-partial-payment-before-discount-date-with-final-payment-after-discount-date"></a>Udligne en delvis betaling før rabatdatoen med en endelig betaling efter rabatdatoen

[!include [banner](../includes/banner.md)]

I denne artikel beskrives virkningen af afregning af betalinger til fakturaer for debitorer. Scenariet fokuserer på effekterne på reskontroen, ikke på Finans.

Fabrikam sælger varer til debitor 4027. Fabrikam tilbyder en kasserabat på 1 procent, hvis fakturaen betales i løbet af 14 dage. Fakturaer skal betales inden 30 dage. Fabrikam tilbyder også kasserabatter på delvise indbetalinger. Udligningsparametrene er placeret på siden **Kreditorparametre**.

## <a name="invoice"></a>Faktura
Den 25. juni indtaster og bogfører Arnie en faktura på 1.000,00 for debitor 4027. Arne kan få vist denne faktura ved hjælp af knappen **Transaktioner** på siden **Debitorer**.

| Bilag   | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI 10020 | Faktura          | 25/6/2020 | 10020   | 1,000.00                             |                                       | 1,000.00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Delvis betaling før kasserabatdatoen
Den 2. juli gennemfører debitor 4027 en delbetaling på 297,00 for fakturaen. Betalingen er berettiget til en kasserabat, fordi Fabrikam tilbyder kasserabatter på delbetalinger, og delbetalingen foretages før datoen for kasserabat. Derfor får debitor 4027 3,00 i kasserabat. Arnie registrerer betalingen for debitor 4027 ved hjælp af betalingskladden. Arnie åbner derefter siden **Udlign posteringer**, så han kan markere fakturaen til udligning.

| Marker     | Anvende kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valgt | Normal            | FTI 10020 | 4027    | 25/6/2020 | 25/7/2020 | 10020   | 1,000.00                             | USD      | 297,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**. Hvis du ikke ændrer værdien **Beløb, der skal udlignes** til 297,00, vil værdierne **Kasserabatbeløb**, der vises, variere. 3,00 vil dog blive medtaget som kasserabatten, når betalingen bogføres, fordi udligningen automatisk justerer værdien **Beløb, der skal udlignes** for dig.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 09/7/2020 |
| Kasserabatbeløb         | 10.00     |
| Anvende kasserabat            | Normal    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | 3,00      |

Arnie bogfører betalingen. Fakturaen har nu en saldo på 700,00. Du kan se følgende transaktioner for kunden.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI 10020  | Faktura          | 25/6/2020 | 10020   | 1,000.00                             |                                       | 700.00  | USD      |
| ARP-10020  |  Betaling         | 1.7.2020  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |  Kasserabat   | 1.7.2020  |         |                                      | 3.00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Resterende betaling efter kasserabatdatoen
Den 11. juli, som er efter rabatperioden, betaler debitor 4027 resten af fakturaen. På siden **Udlign transaktioner** vises der ikke et rabatbeløb i feltet **Forkalkuleret kasserabat**, og værdien i feltet **Kasserabatbeløb** er **0,00**. Når debitor 4027 betaler de resterende 700,00, ydes der ingen yderligere rabat.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Valgt | Normal            | FTI 10020 | 4027    | 25/6/2020 | 25/7/2020 | 10020   | 700.00                               | USD      | 700.00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 09/7/2020 |
| Kasserabatbeløb         | 0,00      |
| Anvende kasserabat            | Normal    |
| Medtaget kasserabat          | 3,00      |
| Kasserabatbeløb, der skal medtages | 0,00      |

Hvis Arnie ændrer værdien i feltet **Anvend kasserabat** til **Altid**, tilsidesættes indstillingen **Beregn kasserabatter for delvise betalinger**, og kasserabatten anvendes. Betalingsbeløbet ændres til 693,00, og kasserabatten er de resterende 7,00.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|---------------|---------------------|----------|------------------|
| Valgt | Altid            | FTI 10020 | 4027    | 25/6/2020 | 25/7/2020 | 10020   | 700.00        |                        | USD      | 693,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 09/7/2020 |
| Kasserabatbeløb         | 7.00      |
| Anvende kasserabat            | Altid    |
| Medtaget kasserabat          | 3,00      |
| Kasserabatbeløb, der skal medtages | 7:00      |

Arnie ændrer værdien i feltet **Anvend kasserabat** tilbage til **Normal**, da han ikke vil lade denne kunde få den resterende kasserabat på 7,00. Derefter bogfører Arnie betalingen. Når Arnie åbner siden **Kundetransaktioner**, har fakturaen en saldo på 0,00. Der er to betalinger. Én betaling på 297,00 med en kasserabat på 3,00, og en anden betaling på 700,00.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI 10020  | Faktura          | 25/6/2020 | 10020   | 1,000.00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 1.7.2020  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |                  | 1.7.2020  |         |                                      | 3.00                                  | 0,00    | USD      |
| ARP-10021  |                  | 11/7/2020 |         |                                      | 700.00                                | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
