---
title: Udligne en delvis betaling før rabatdatoen og en endelig betaling efter rabatdatoen
description: Denne artikel fører dig gennem et scenario, hvor der foretages flere delvise betalinger, hvor nogle ligger inden for kasserabatperioden og andre uden for kasserabatperioden.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14411
ms.assetid: 302ad6ae-28ee-4899-9f6b-f74424a5f50c
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 59ad9b9e7e75027fc46658c901da7a70520a1332
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715747"
---
# <a name="settle-partial-payment-before-discount-date-and-final-payment-after-discount-date"></a>Udligne en delvis betaling før rabatdatoen og en endelig betaling efter rabatdatoen

[!include [banner](../includes/banner.md)]

Denne artikel fører dig gennem et scenario, hvor der foretages flere delvise betalinger, hvor nogle ligger inden for kasserabatperioden og andre uden for kasserabatperioden.

Fabrikam køber varer fra leverandør 3057. Fabrikam modtager en kasserabat på 1 procent, hvis fakturaen betales i løbet af 14 dage. Fakturaer skal betales inden 30 dage. Leverandøren giver desuden Fabrikam kasserabatter på delbetalinger. Udligningsparametrene er placeret på siden **Kreditorparametre**.

## <a name="invoice-on-june-25"></a>Fakturer d. 25. juni
Den 25. juni angiver og bogfører April en faktura på 1.000,00 til kreditor 3057. April kan se denne transaktion på siden **Kreditorposteringer**.

| Bilag   | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo   | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Fak-10020 | Faktura          | 25-6-2015 | 10020   |                                      | 1.000,00                              | -1.000,00 | USD      |

## <a name="partial-payment-on-july-2"></a>Delvis betaling d. 2. juli
D. 2. juli vil April udligne 300,00 af denne faktura. Betalingen er rabatberettiget, fordi Fabrikam får rabatter på delbetalinger. Derfor betaler April 297,00 og 3,00 i rabat. Hun opretter en betalingskladde og indtaster en linje for kreditor 3057. Hun åbner derefter siden **Udlign posteringer**, så hun kan markere fakturaen til udligning.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | Fak-10020 | 3057    | 25-6-2015 | 25-7-2015 | 10020   | -1.000,00                      | USD      | -297,00          |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 09-07-2015 |
| Kasserabatbeløb         | -10,00    |
| Anvende kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | -3,00     |

Derefter bogfører April fakturaen. Fakturaen har nu en saldo på 700,00. April kan se denne transaktion på siden **Kreditorposteringer**.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fak-10020  | Faktura          | 25-6-2015 | 10020   |                                      | 1.000,00                              | -700.00 | USD      |
| APP-10020  | Betaling          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Kasserabat    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--normal"></a>Resterende betaling d. 15. juli, brug kasserabat = Normal
April betaler resten af fakturaen den 15. juli, som er efter rabatperioden. På siden **Udlign åbne posteringer** vises ingen rabatbeløb i feltet **Forkalkuleret kasserabat**, og værdien i feltet **Kasserabatbeløb** er **0,00**. Når April betaler de resterende 700,00, ydes der ingen yderligere rabat.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | Fak-10020 | 3057    | 25-6-2015 | 25-7-2015 | 10020   | -700.00                        | USD      | -700.00          |

Rabatoplysninger vises nederst på siden **Udlign transaktioner**. April kan se, at hun allerede har fået 3,00 i rabat.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 09-07-2015 |
| Kasserabatbeløb         | 0,00      |
| Anvende kasserabat            | Almindelig    |
| Medtaget kasserabat          | -3,00     |
| Kasserabatbeløb, der skal medtages | 0,00      |

Derefter bogfører April fakturaen. Når hun åbner siden **Kreditorposteringer**, ser hun, at fakturaen har en saldo på 0,00. Hun kan også se, at der er to betalinger. Én betaling på 297,00 med en rabat på 3,00, og en anden betaling på 700,00.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fak-10020  | Faktura          | 25-6-2015 | 10020   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10020  | Betaling          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Kasserabat    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Betaling          | 15-7-2015 |         | 700,00                               |                                       | 0,00    | USD      |

## <a name="remaining-payment-on-july-15-use-cash-discount--always"></a>Resterende betaling d. 15. juli, brug kasserabat = Altid
Hvis kreditoren giver April rabat, selvom hun betaler efter rabatdatoen, kan hun ændre værdien i feltet **Anvend kasserabat** til **Altid**. Indstillingen **Beregn kasserabatter for delvise betalinger** tilsidesættes, og rabatten fradrages. Betalingsbeløbet er 693,00, og rabatten er de resterende 7,00.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------------|---------------------------------------|----------|------------------|
| Markeret | Altid            | Fak-10020 | 3057    | 25-6-2015 | 25-7-2015 | 10020   | 700,00                               |                                       | USD      | -693,00          |

Rabatoplysninger vises nederst på siden **Udlign transaktioner**.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 09-07-2015 |
| Kasserabatbeløb         | 7.00      |
| Anvende kasserabat            | Altid    |
| Medtaget kasserabat          | -3,00     |
| Kasserabatbeløb, der skal medtages | -7,00     |

Derefter bogfører April fakturaen. Når hun åbner siden **Kreditorposteringer**, ser hun, at fakturaen har en saldo på 0,00. Hun kan også se, at der er to betalinger. Én betaling er for 297,00 med en rabat på 3,00, og den anden betaling er på 693,00 med en rabat på 7,00.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fak-10020  | Faktura          | 25-6-2015 | 10020   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10020  | Betaling          | 7/1/2015  |         | 297,00                               |                                       | 0,00    | USD      |
| DISC-10020 | Kasserabat    | 7/1/2015  |         | 3,00                                 |                                       | 0,00    | USD      |
| APP-10021  | Betaling          | 15-7-2015 |         | 693,00                               |                                       | 0,00    | USD      |
| DISC-10021 | Kasserabat    | 15-7-2015 |         | 7:00                                 |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
