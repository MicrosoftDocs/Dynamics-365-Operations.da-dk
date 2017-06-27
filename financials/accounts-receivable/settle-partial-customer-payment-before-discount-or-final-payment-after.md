---
title: "Udlign en delvis debitorbetaling før rabatdatoen, med en endelig betaling efter rabatdatoen"
description: "I denne artikel beskrives virkningen af afregning af betalinger til fakturaer for debitorer. Scenariet fokuserer på effekterne på reskontroen, ikke på Finans."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14584
ms.assetid: e54936f5-053b-4ed3-b778-42c7e9aeb7cf
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 4399cf66e423d2e6436c664e6485a77d9ad75d69
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="settle-a-partial-customer-payment-before-the-discount-date-with-a-final-payment-after-the-discount-date"></a>Udlign en delvis debitorbetaling før rabatdatoen, med en endelig betaling efter rabatdatoen

[!include[banner](../includes/banner.md)]


I denne artikel beskrives virkningen af afregning af betalinger til fakturaer for debitorer. Scenariet fokuserer på effekterne på reskontroen, ikke på Finans.

Fabrikam sælger varer til debitor 4027. Fabrikam tilbyder en kasserabat på 1 procent, hvis fakturaen betales i løbet af 14 dage. Fakturaer skal betales inden 30 dage. Fabrikam tilbyder også kasserabatter på delvise indbetalinger. Udligningsparametrene er placeret på siden **Kreditorparametre**.

## <a name="invoice"></a>Faktura
Den 25. juni indtaster og bogfører Arnie en faktura på 1.000,00 for debitor 4027. Arne kan få vist denne faktura ved hjælp af knappen **Transaktioner** på siden **Debitorer**.

| Bilag   | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI 10020 | Faktura          | 25-6-2015 | 10020   | 1.000,00                             |                                       | 1.000,00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Delvis betaling før kasserabatdatoen
Den 2. juli gennemfører debitor 4027 en delbetaling på 297,00 for fakturaen. Betalingen er berettiget til en kasserabat, fordi Fabrikam tilbyder kasserabatter på delbetalinger, og delbetalingen foretages før datoen for kasserabat. Derfor får debitor 4027 3,00 i kasserabat. Arnie registrerer betalingen for debitor 4027 ved hjælp af betalingskladden. Arnie åbner derefter siden **Udlign posteringer**, så han kan markere fakturaen til udligning.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Markeret | Almindelig            | FTI 10020 | 4027    | 25-6-2015 | 25-7-2015 | 10020   | 1.000,00                             | USD      | 297,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**. Hvis du ikke ændrer værdien **Beløb, der skal udlignes** til 297,00, vil værdierne **Kasserabatbeløb**, der vises, variere. 3,00 vil dog blive medtaget som kasserabatten, når betalingen bogføres, fordi udligningen automatisk justerer værdien **Beløb, der skal udlignes** for dig.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 09-07-2015 |
| Kasserabatbeløb         | 10,00     |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | 3,00      |

Arnie bogfører betalingen. Fakturaen har nu en saldo på 700,00. Du kan se følgende transaktioner for kunden.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI 10020  | Faktura          | 25-6-2015 | 10020   | 1.000,00                             |                                       | 700,00  | USD      |
| ARP-10020  |  Betaling         | 01-07-2015  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |  Kasserabat   | 01-07-2015  |         |                                      | 3,00                                  | 0,00    | USD      |

## <a name="remaining-payment-after-the-cash-discount-date"></a>Resterende betaling efter kasserabatdatoen
Den 11. juli, som er efter rabatperioden, betaler debitor 4027 resten af fakturaen. På siden **Udlign transaktioner** vises der ikke et rabatbeløb i feltet **Forkalkuleret kasserabat**, og værdien i feltet **Kasserabatbeløb** er **0,00**. Når debitor 4027 betaler de resterende 700,00, ydes der ingen yderligere rabat.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|----------|------------------|
| Markeret | Almindelig            | FTI 10020 | 4027    | 25-6-2015 | 25-7-2015 | 10020   | 700,00                               | USD      | 700,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 09-07-2015 |
| Kasserabatbeløb         | 0,00      |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 3,00      |
| Kasserabatbeløb, der skal medtages | 0,00      |

Hvis Arnie ændrer værdien i feltet **Anvend kasserabat** til **Altid**, tilsidesættes indstillingen **Beregn kasserabatter for delvise betalinger**, og kasserabatten anvendes. Betalingsbeløbet ændres til 693,00, og kasserabatten er de resterende 7,00.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Markeret | Altid            | FTI 10020 | 4027    | 25-6-2015 | 25-7-2015 | 10020   | 700,00                               |                                       | USD      | 693,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 09-07-2015 |
| Kasserabatbeløb         | 7:00      |
| Anvend kasserabat            | Altid    |
| Medtaget kasserabat          | 3,00      |
| Kasserabatbeløb, der skal medtages | 7:00      |

Arnie ændrer værdien i feltet **Anvend kasserabat** tilbage til **Normal**, da han ikke vil lade denne kunde få den resterende kasserabat på 7,00. Derefter bogfører Arnie betalingen. Når Arnie åbner siden **Kundetransaktioner**, kan han se, at fakturaen har en saldo på 0,00. Han kan også se, at der er to betalinger. Én betaling på 297,00 med en kasserabat på 3,00, og en anden betaling på 700,00.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI 10020  | Faktura          | 25-6-2015 | 10020   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10020  |                  | 01-07-2015  |         |                                      | 297,00                                | 0,00    | USD      |
| DISC-10020 |                  | 01-07-2015  |         |                                      | 3,00                                  | 0,00    | USD      |
| ARP-10021  |                  | 11-07-2015 |         |                                      | 700,00                                | 0,00    | USD      |






