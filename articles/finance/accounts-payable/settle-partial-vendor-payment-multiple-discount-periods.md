---
title: Udlign en delvis kreditorbetaling, der omfatter flere rabatperioder
description: Denne artikel gennemgår et scenarie, hvor der foretages flere delbetalinger for en kreditor, der tilbyder flere kasserabatter.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14262
ms.assetid: af95c48a-afd1-476c-978d-e34995100be4
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: da69d61c657ddc168a27a97fe16909d5f60eb4fd
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778031"
---
# <a name="settle-a-partial-vendor-payment-that-has-multiple-discount-periods"></a>Udlign en delvis kreditorbetaling, der omfatter flere rabatperioder

[!include [banner](../includes/banner.md)]

Denne artikel gennemgår et scenarie, hvor der foretages flere delbetalinger for en kreditor, der tilbyder flere kasserabatter. 

Kreditor 3054 tilbyder Fabrikam en kasserabat på 2 %, hvis en faktura betales inden for fem dage, og en kasserabat på 1 %, hvis fakturaen betales inden for 14 dage.

## <a name="invoice"></a>Faktura
Den 28. juni opretter April en faktura på 1.000,00 til kreditor 3054. April kan se denne transaktion på siden **Kreditorposteringer**.

| Bilag   | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo   | Valuta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Fak-10060 | 28/6/2020 | 10060   |                                      | 1,000.00                              | -1.000,00 | USD      |

Følgende datoer og beløb for kasserabatten er tilgængelige for denne faktura.

| Kasserabatdato | Kasserabatbeløb | Beløb i transaktionsvaluta |
|--------------------|----------------------|--------------------------------|
| 3/7/2020           | 20.00                | 980.00                         |
| 12/7/2020          | 10.00                | 990.00                         |
| 25/7/2020          | 0,00                 | 1,000.00                       |

## <a name="payment-on-july-2"></a>Betaling d. 2. juli
D. 2. juli vil April betale 300,00 af denne faktura. Hun opretter en engangsbetaling ved hjælp af siden **Betalingskladde** i Kreditor. Hun tilføjer en linje for Kreditor 3054 og indtaster et beløb til betaling på **300,00**. April åbner derefter siden **Udlign posteringer**, så hun kan markere den faktura, der skal udlignes. Hun opdaterer værdien i feltet **Beløb, der skal udlignes** til **300,00** og bemærker, at værdien i feltet **Kasserabatbeløb, der skal medtages** er ændret til **6,12**. Da denne betaling sker i første rabatperiode, anvendes der en rabat på 2 procent.

| Foretag afmærkning | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Fak-10060 | 3054    | 28/6/2020 | 28/7/2020 | 10060   | 1,000.00                       | USD      | 300,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 02/7/2020 |
| Kasserabatbeløb         | -20,00    |
| Anvende kasserabat            | Normal    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | -6,12     |

Da der er en tilgængelig kasserabat, vil April ændre det betalingsbeløbet, så det samlede udlignede beløb er 300,00 for betalingen, og kasserabatten. Hun ænder værdien i feltet **Beløb, der skal udlignes** til **294,00** og bemærker, at værdien i feltet **Kasserabatbeløb, der skal medtages** er ændret til **6,00**.

| Foretag afmærkning | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Fak-10060 | 3054    | 28/6/2020 | 28/7/2020 | 10060   | 1,000.00                       | USD      | 294,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 02/7/2020 |
| Kasserabatbeløb         | -20,00    |
| Anvende kasserabat            | Normal    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | -6,00     |

April bogfører denne betaling. Hun kan se posteringerne på siden **Kreditorposteringer**. Hun ser, at 300,00 er anvendt på fakturaen. Dette beløb omfatter en rabat på 6,00. Derfor er den resterende saldo 700,00.

| Bilag    | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fak-10060  | 28/6/2020 | 10060   |                                      | 1,000.00                              | -700.00 | USD      |
| APP-10060  | 2/7/2020  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 2/7/2020  |         | 6,00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-8"></a>Betaling d. 8. juli
April foretager en ekstra betaling mod fakturaen d. 8. juli. For at angive beløbet åbner hun siden **Udlign transaktioner** og klikker derefter på fanen **Kasserabat**. Hun ser datoerne og beløbene for de to kasserabatter, der er tilgængelige. Da denne betaling er foretaget i den anden rabatperiode, er en rabat på 1 % eller 5,00 tilgængelig. Dette beløb beregnes som halvdelen af rabatten på 1 % på 1.000,00 eller halvdelen af 10,00.

| Kasserabatdato | Kasserabatbeløb | Beløb i transaktionsvaluta |
|--------------------|----------------------|--------------------------------|
| 3/7/2020           | 20.00                | 680,00                         |
| 12/7/2020          | 10.00                | 690,00                         |
| 25/7/2020          | 0,00                 | 700.00                         |

April beslutter at betale 495,00 og medtagetage kasserabatten på 5,00. Det samlede beløb, der er udlignet, er derfor 500,00.

| Foretag afmærkning | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Normal            | Fak-10060 | 3054    | 28/6/2020 | 28/7/2020 | 10060   | 1,000.00                       | USD      | 495,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 12/7/2020 |
| Kasserabatbeløb         | -10,00    |
| Anvende kasserabat            | Normal    |
| Medtaget kasserabat          | -6,00     |
| Kasserabatbeløb, der skal medtages | -5,00     |

På siden **Kreditorposteringer** ser April, at den nye saldo er 200,00.

| Bilag    | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fak-10060  | 28/6/2020 | 10060   |                                      | 1,000.00                              | -200,00 | USD      |
| APP-10060  | 2/7/2020  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 2/7/2020  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 12/7/2020 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 12/7/2020 |         | 5.00                                 |                                       | 0,00    | USD      |

## <a name="payment-on-july-20"></a>Betaling d. 20. juli
Den 20. juli opretter April en endelig betaling på 200,00. Der medtages ingen kasserabat, da betalingen sker efter begge rabatperioder. Fakturaens saldo er 0,00.

| Bilag    | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fak-10060  | 28/6/2020 | 10060   |                                      | 1,000.00                              | -200,00 | USD      |
| APP-10060  | 2/7/2020  |         | 294,00                               |                                       | 0,00    | USD      |
| DISC-10060 | 2/7/2020  |         | 6,00                                 |                                       | 0,00    | USD      |
| APP-10061  | 12/7/2020 |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10061 | 12/7/2020 |         | 5.00                                 |                                       | 0,00    | USD      |
| APP-10062  | 20/7/2020 |         | 200.00                               |                                       | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
