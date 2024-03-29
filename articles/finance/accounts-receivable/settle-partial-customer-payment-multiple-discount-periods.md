---
title: Udlign en delvis debitorbetaling, der omfatter flere rabatperioder
description: Denne artikel viser, hvordan delvise debitorbetalinger udlignes, når der er flere rabatperioder.
author: ShivamPandey-msft
ms.date: 11/15/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.custom: 14471
ms.assetid: b633a7c4-c18d-42e7-91cc-adcdc8a3ba98
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 62defda8831d2915050fc6822f60a905f067fe88
ms.sourcegitcommit: 9c4638c4bb5b5f8adc7508542a0a2c3e1de5190c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/15/2022
ms.locfileid: "9778433"
---
# <a name="settle-a-partial-customer-payment-that-has-multiple-discount-periods"></a>Udlign en delvis debitorbetaling, der omfatter flere rabatperioder

[!include [banner](../includes/banner.md)]

Denne artikel viser, hvordan delvise debitorbetalinger udlignes, når der er flere rabatperioder.

Fabrikam tilbyder kunden 4031 to kasserabatperioder. Kunden modtager en kasserabat på 2 %, hvis fakturaen er betalt inden fem dage og en kasserabat på 1 %, hvis fakturaen betales inden 14 dage. Fabrikam tilbyder også kasserabatter på delvise indbetalinger. Udligningsparametrene er placeret på siden **Kreditorparametre**.

## <a name="invoice"></a>Faktura
Den 25. juni indtaster og bogfører Arnie en faktura på 1.000,00 for debitor 4031. Da Arnie gennemgår kasserabatterne for denne faktura, ser han, at debitor 4031 får en rabat på 20,00, hvis fakturaen betales inden den 30. juni. Hvis fakturaen er betalt den 9. juli, modtager kunden en rabat på 10,00.

| Kasserabatdato | Kasserabatbeløb | Beløb i transaktionsvaluta |
|--------------------|----------------------|--------------------------------|
| 6/30/2020          | 20.00                | 980.00                         |
| 9/7/2020           | 10.00                | 990.00                         |
| 25/7/2020          | 0,00                 | 1,000.00                       |

Arnie kan se denne postering på siden **Debitorposteringer**.

| Bilag   | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI 10030 | Faktura          | 25/6/2020 | 10030   | 1,000.00                             |                                       | 1,000.00 | USD      |

## <a name="partial-payment-before-the-cash-discount-date"></a>Delvis betaling før kasserabatdatoen
Kunde 4031 foretager en delvis betaling på 294,00 d. 28. juni. Da d. 28 juni er inden for den første kasserabatperiode, får kunden en rabat på 6,00. På siden **Udlign posteringer** er værdien **Kasserabatbeløb** 20,00, og værdien **Kasserabatbeløb, der skal medtages** er 6,00.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Valgt | Normal            | FTI 10030 | 4031    | 25/6/2020 | 25/7/2020 | 10030   | 1,000.00                       | USD      | 294,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**. Hvis du ikke ændrer værdien **Beløb, der skal udlignes** til **294,00**, vil værdierne **Kasserabatbeløb**, der vises, variere. 6,00 vil dog blive medtaget som kasserabatten, når betalingen bogføres, fordi udligning automatisk justerer værdien **Beløb, der skal udlignes** for dig.

| &nbsp;                       | &nbsp;    |
|------------------------------|-----------|
| Kasserabatdato           | 6/30/2020 |
| Kasserabatbeløb         | 20.00     |
| Anvende kasserabat            | Normal    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | 6,00      |

Efter at Arnie har bogført betalingen, er fakturasaldoen 700,00.

## <a name="partial-payment-before-the-second-cash-discount-date"></a>Delvis betaling før den anden kasserabatdato
Den 8. juli betaler debitoren resten af fakturabeløbet. En rabat på 7,00 (1 %) medtages, da betalingen blev foretaget inden for den anden kasserabatperiode.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------|-----------------------|----------|------------------|
| Valgt | Normal            | FTI 10030 | 4031    | 25/6/2020 | 25/7/2020 | 10030   | 700.00       |            | USD      | 693,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

| &nbsp;                       | &nbsp;    |
|------------------------------|-----------|
| Kasserabatdato           | 09/7/2020 |
| Kasserabatbeløb         | 30.00     |
| Anvende kasserabat            | Normal    |
| Medtaget kasserabat          | 6,00      |
| Kasserabatbeløb, der skal medtages | 7:00      |

Fakturasaldoen er nu 0,00. Arnie kan se oplysningerne på siden **Debitorposteringer**.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI 10030  | Faktura          | 25/6/2020 | 10030   | 1,000.00                             |                                       | 0,00    | USD      |
| ARP-10030  |  Betaling         | 28/6/2020 |         |                                      | 294,00                                | 0,00    | USD      |
| DISC-10030 |  Kasserabat   | 28/6/2020 |         |                                      | 6,00                                  | 0,00    | USD      |
| ARP-10031  |  Betaling         | 8/7/2020  |         |                                      | 693,00                                | 0,00    | USD      |
| DISC-1031  |  Kasserabat   | 8/7/2020  |         |                                      | 7.00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
