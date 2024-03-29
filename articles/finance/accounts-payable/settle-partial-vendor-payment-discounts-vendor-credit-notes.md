---
title: Udligne en delvis kreditorbetaling med rabatter på kreditnotaer
description: Denne artikel fører dig gennem et scenario, hvor en kreditnota udlignes med en faktura.
author: angelad116
ms.date: 10/24/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 14222
ms.assetid: 2b19f7fd-9ff9-4ee4-bddf-f582946d008e
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
ms.openlocfilehash: b926d94059fb12b143b9c9b4b5c04cb7f39f8e99
ms.sourcegitcommit: 0d5c07ba91a9ceb2eeb11db032fd28037216789d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/25/2022
ms.locfileid: "9715931"
---
# <a name="settle-a-partial-vendor-payment-that-has-discounts-on-credit-notes"></a>Udligne en delvis kreditorbetaling med rabatter på kreditnotaer

[!include [banner](../includes/banner.md)]

Denne artikel fører dig gennem et scenario, hvor en kreditnota udlignes med en faktura.

Fabrikams kreditorer giver kasserabatter på kreditnotaer. Kreditor 3050 giver Fabrikam en kasserabat på 1 procent, hvis en faktura betales i løbet af 14 dage.

## <a name="invoice-and-credit-memo"></a>Faktura og kreditnota
Den 29. juni opretter April en faktura på 1.000,00 til kreditor 3050. Den 2. juli opretter hun en kreditnota på 200,00. Fra siden **Leverandører** åbner April siden **Udlign transaktioner**. Hun kan bruge siden **Udlign transaktioner** til at markere både kreditnotaen og den faktura, der skal udlignes. Der beregnes en rabat på 2,00 på kreditnotaen. Derfor er den samlede værdi af kreditnotaen reduceret til 198,00.

| Foretag afmærkning                     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret                 | Almindelig            | Fak-10070 | 3050    | 29-6-2015 | 29-7-2015 | 10070   | -1.000,00                      | USD      | -990,00          |
| Markeret og fremhævet | Almindelig            | CR-10070  | 3050    | 2-7-2015  | 29-7-2015 |         | 200,00                         | USD      | 198,00           |

Rabatoplysninger for kreditnotaen vises nederst på siden **Udlign åbne posteringer**.

| Felt                        | Værdi     |
|------------------------------|-----------|
| Kasserabatdato           | 13/07/2015 |
| Kasserabatbeløb         | 2.00      |
| Anvende kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | 2,00      |

April klikker på **Bogfør**. Dereefter gennemgår hun den gennemførte udligning. April kan se, at 198,00 fra kreditnotaen blev anvendt, og at der blev givet en rabat på 2,00. Derfor er totalen 200,00.

| Foretag afmærkning                     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura  | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|----------|--------------------------------|----------|------------------|
| Markeret og fremhævet | Almindelig            | Fak-10070 | 3050    | 29-6-2015 | 29-7-2015 | 10070    | -1.000,00                      | USD      | -200,00          |
| Valgt                 | Almindelig            | CR-10070  | 3050    | 2-7-2015  | 29-7-2015 | CR-10070 | 200,00                         | USD      | 198,00           |

April kan gennemgå kreditorposteringer på siden **Kreditorposteringer** ved at vælge en kreditor på siden **Alle kreditorer** og derefter klikke på **Transaktioner** i handlingsruden. På denne side kan April se, at fakturaen har en saldo på -800,00. Hun kan også se en kreditnota på 198,00 og en rabat på 2,00.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| Fak-10070  | Faktura          | 29-6-2015 | 10070   |                                      | 1.000,00                              | -800,00 | USD      |
| Fak-10071  |                  | 2-7-2015  | CR10071 | 200,00                               |                                       | 0,00    | USD      |
| DISC-10071 |  Kasserabat   | 2-7-2015  |         | 2,00                                 |                                       | 0,00    | USD      |
| DISC-10071 |  Kasserabat   | 2-7-2015  |         |                                      | 2,00                                  | 0,00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
