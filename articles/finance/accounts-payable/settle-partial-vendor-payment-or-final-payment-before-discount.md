---
title: Udlign en delvis kreditorbetaling, og udlign den endelige betaling fuldt ud før rabatdatoen
description: Denne artikel gennemgår et scenario, hvor der foretages delbetalinger for en kreditorfaktura og der gives en kasserabat.
author: abruer
manager: AnnBe
ms.date: 08/22/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14431
ms.assetid: 6b8e3420-b4c9-4e02-9588-598fe6d3df0d
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 34d941c3806ccc9d2b8baa29eef45fbd4216686e
ms.sourcegitcommit: 165e082e59ab783995c16fd70943584bc3ba3455
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/06/2020
ms.locfileid: "3967304"
---
# <a name="settle-a-partial-vendor-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Udlign en delvis kreditorbetaling, og udlign den endelige betaling fuldt ud før rabatdatoen

[!include [banner](../includes/banner.md)]

Denne artikel gennemgår et scenario, hvor der foretages delbetalinger for en kreditorfaktura og der gives en kasserabat.

Fabrikam køber varer fra leverandør 3064. Leverandøren giver Fabrikam en kasserabat på 1 procent, hvis fakturaen betales i løbet af 14 dage. Fakturaer skal betales inden 30 dage. Leverandøren giver desuden Fabrikam kasserabatter på delbetalinger. Udligningsparametrene er placeret på siden **Kreditorparametre**. Den 25. juni skriver April en faktura på 1.000,00 til kreditor 3064.

## <a name="vendor-invoice-on-june-25"></a>Kreditorfaktura den 25. juni
Den 25. juni angiver og bogfører April en faktura på 1.000,00 til kreditor 3064. April kan se denne transaktion på siden **Kreditorposteringer**.

| Bilag   | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo   | Valuta |
|-----------|-----------|---------|--------------------------------------|---------------------------------------|-----------|----------|
| Fak-10010 | 25-6-2015 | 10010   |                                      | 1.000,00                              | -1.000,00 | USD      |

Fra siden **Leverandører** åbner April siden **Udlign transaktioner**. Hun kan bruge formen **Udlign posteringer** til at få vist datoerne og beløbene for kasserabatter. Forfaldsdatoen er den 25. juli, og en kasserabat på -10,00 er tilgængelig, hvis fakturaen betales inden den 9. juli.

| Foretag afmærkning | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
|      | Almindelig            | Fak-10010 | 3064    | 25-6-2015 | 25-7-2015 | 10010   | 1.000,00                       | USD      | 990,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 7/09/2015 |
| Kasserabatbeløb         | -10,00    |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | -10,00    |

April klikker på fanen **Kasserabat** for at få vist rabatbeløbet.

| Kasserabatdato | Kasserabatbeløb | Beløb i transaktionsvaluta |
|--------------------|----------------------|--------------------------------|
| 9-7-2015           | 10,00                | 990,00                         |
| 25-7-2015          | 0,00                 | 1.000,00                       |

## <a name="partial-payment-on-july-1-by-using-the-settle-transactions-page"></a>Delvis betaling den 1. juli ved hjælp af siden Udlign posteringer
April kan oprette en betalingskladde for denne betaling ved at åbne siden **Betalingskladde** under Kreditor. Hun opretter en ny kladde og indtaster en linje for kreditor 3064. Hun åbner derefter siden **Udlign posteringer**, så hun kan markere fakturaen til udligning. April markerer fakturaen og ændrer værdien i feltet **Beløb, der skal udlignes** til **-500,00**. Hun ser, at værdien i feltet **Kasserabatbeløb** er **-10,00** for hele fakturaen, og at værdien i feltet **Kasserabatbeløb, der skal medtages** er **-5,05**. April udligner derfor -505,05 af denne faktura.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | FTI 10010 | 4028    | 25-6-2015 | 25-7-2015 | 10010   | 1.000,00                       | USD      | -500,00          |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 7/09/2015 |
| Kasserabatbeløb         | -10,00    |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | -5,05     |

April vil udligne præcist halvdelen af fakturaen. Hun ændrer derfor værdien i feltet **Beløb, der skal udlignes** til **-495,00**. Det samlede beløb, der er afregnet, er nu 500,00. Dette beløb omfatter en kasserabat på -5,00.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | FTI 10010 | 4028    | 25-6-2015 | 25-7-2015 | 10010   | 1.000,00                       | USD      | -495,00          |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 7/09/2015 |
| Kasserabatbeløb         | -10,00    |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | -5,00     |

April lukker siden **Udlign posteringer**. Der oprettes en betalingslinje for 495,00 i kladden, og April bogfører derefter kladden. April kan gennemse kreditorposteringerne på siden **Kreditorposteringer**. Hun ser, at fakturaen har en saldo på -500,00. Hun ser også en betaling på 495,00 og en kasserabat på 5,00.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fak-10010  | Faktura          | 25-6-2015 | 10010   |                                      | 1.000,00                              | -500,00 | USD      |
| APP-10010  | Betaling          | 7/1/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Kasserabat    | 7/1/2015  |         | 5,00                                 |                                       | 0,00    | USD      |

## <a name="remaining-amount-paid-on-july-8"></a>Restbeløbet betalt den 8. juli
April betaler resten af fakturaen til kreditor 3064 den 8. juli, som er i perioden for kasserabatten. April opretter betalingskladden den 8. juli og markerer posteringen til udligning. Hun ser, at det beløb, der skal udlignes, er 495,00. Værdien i feltet **Forkalkuleret kasserabat** er **-5,00**, fordi rabatten på 5,00 rabat blev trukket tidligere.

|                         |        |
|-------------------------|--------|
| Afmærket i alt            | 495,00 |
| Forkalkuleret kasserabat | -5,00  |

Oplysninger om den markerede postering vises i gitteret på siden **Udlign åbne posteringer**.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | FTI 10010 | 4028    | 25-6-2015 | 25-7-2015 | 10010   | 1.000,00                       | USD      | 495,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 7/09/2015 |
| Kasserabatbeløb         | 10,00     |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 5,00      |
| Kasserabatbeløb, der skal medtages | 5,00      |

April bogfører betalingskladden og gennemgår kreditorposteringerne på siden **Kreditorposteringer**. Saldoen for fakturaen er nu 0,00, og April ser to betalinger og to kasserabatter.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fak-10010  | Faktura          | 25-6-2015 | 10010   |                                      | 1.000,00                              | 0,00    | USD      |
| APP-10010  |  Betaling         | 7/1/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10010 | Kasserabat    | 7/1/2015  |         | 5,00                                 |                                       | 0,00    | USD      |
| APP-10011  | Betaling          | 7/8/2015  |         | 495,00                               |                                       | 0,00    | USD      |
| DISC-10011 | Kasserabat    | 7/8/2015  |         | 5,00                                 |                                       | 0,00    | USD      |





