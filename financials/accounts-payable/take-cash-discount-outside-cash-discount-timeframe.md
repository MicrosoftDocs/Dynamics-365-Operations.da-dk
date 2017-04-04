---
title: En kasserabat uden for perioden kasserabat
description: Denne artikel indeholder to scenarier, der viser, hvordan en kasserabat kan anvendes, selvom betalingen sker uden for kasserabatperioden.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: LedgerJournalTransVendPaym, VendOpenTrans
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 14301
ms.assetid: bad10b7f-e550-4742-9261-8a094c9c624d
ms.search.region: Global
ms.author: kweekley
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 2cb439e871d57f74c296697cfc42705fb0121bb7
ms.openlocfilehash: bea9565f488c01e5e6aede8cabe73ac13b75dacb
ms.lasthandoff: 03/31/2017


---

# <a name="take-a-cash-discount-outside-the-cash-discount-period"></a>En kasserabat uden for perioden kasserabat

Denne artikel indeholder to scenarier, der viser, hvordan en kasserabat kan anvendes, selvom betalingen sker uden for kasserabatperioden.

April opretter en faktura på 2.000,00 til kreditor 3052 d. 28. Fakturaen har en kasserabat på 1 procent, hvis fakturaen betales inden 14 dage.

## <a name="use-cash-discount-option--always"></a>Brug kasserabatindstilling = Altid
April opretter en betaling den 1. juli, som er efter rabatdatoen. April åbner siden **Udlign posteringer** for at få vist de posteringer, der kan udlignes. 

April markerer fakturaen til betaling. Der anvendes ingen kasserabat, da betalingen sker efter rabatdatoen. Leverandøren har dog givet April godkendelse til at tage kasserabatten alligevel. Derfor April ændrer værdien i den **bruge kasserabatten** til **altid**.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Kasserabatdato | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Altid            | Fak-10030 | 3052    | 28-6-2015          | 12-7-2015 | 10030   | -2.000,00                      | USD      | -1.980,00        |

Rabatoplysninger vises nederst på siden **Udlign transaktioner**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 12-7-2015 |
| Kasserabatbeløb         | -20,00    |
| Anvend kasserabat            | Altid    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | -20,00    |

## <a name="date-to-use-for-calculating-discounts--selected-date"></a>Dato, der skal bruges til beregning af rabatter = Valgt dato
Hvis både fakturaen og betalingen er blevet bogført, kan kasserabatten stadig medtages, når posteringerne er udlignet på siden **Udlign posteringer**. April ændre værdien i feltet **Dato, der skal bruges til beregning af rabatter** til **Valgt dato**. Hun skriver derefter datoen 28. juli, som er i kasserabatperioden for fakturaen. Denne dato bruges til at beregne en kasserabat for posteringen. På siden **Udlign åbne posteringer** ser April ser, at den fulde rabat på 20,00 vises som standard. Fakturalinjen viser, at det beløb, der skal udlignes, er 1.980,00.

| Foretag afmærkning                     | Anvend kasserabat | Bilag   | Konto | Kasserabatdato | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|--------------------------|-------------------|-----------|---------|--------------------|-----------|---------|--------------------------------|----------|------------------|
| Markeret og fremhævet | Almindelig            | Fak-10030 | 3052    | 28-6-2015          | 12-7-2015 | 10030   | -2.000,00                      | USD      | -1.980,00        |
| Valgt                 | Almindelig            | APP-10030 | 3052    | 15-7-2015          | 15-7-2015 |         | 500,00                         | USD      | 500,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**. Det rabatbeløb, der skal medtages, er 20,00, da det beløb, der skal udlignes for fakturaen, er standardbeløbet 1.980,00.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 12-7-2015 |
| Kasserabatbeløb         | -20,00    |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | -20,00    |

April opdaterer værdien i feltet **Beløb, der skal udlignes** til **500,00**. Værdien i feltet **Kasserabatbeløb, der skal medtages** beregnes som **5,05**.

| Foretag afmærkning                     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|--------------------------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret og fremhævet | Almindelig            | Fak-10030 | 3052    | 28-6-2015 | 12-7-2015 | 10030   | 2.000,00                       | USD      | -500,00          |
| Valgt                 | Almindelig            | APP-10030 | 3052    | 15-7-2015 | 15-7-2015 |         | 500,00                         | USD      | 500,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**. Værdien i feltet **Kasserabatbeløb, der skal medtages** er **5,05**, da det beløb, der skal udlignes for fakturaen, er ændret til betalingsbeløbet 500,00.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 12-7-2015 |
| Kasserabatbeløb         | -20,00    |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | -5,05     |




