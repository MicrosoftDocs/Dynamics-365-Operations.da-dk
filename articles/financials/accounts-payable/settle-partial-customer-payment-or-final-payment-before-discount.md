---
title: "Udlign en delvis debitorbetaling, og udlign den endelige betaling fuldt ud før rabatdatoen"
description: Denne artikel indeholder scenarier, der viser, hvordan du registrerer delbetalinger for en kunde og anvender kasserabatter i kasserabatperioden.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustOpenTrans, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, AX 7.0.0, Operations, UnifiedOperations
ms.custom: 14491
ms.assetid: 0f07d3ce-a439-43ed-a22e-957ccd36a37b
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 1d48a10f413ce4e2830bfba062615980a6de70a4
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="settle-a-partial-customer-payment-and-the-final-payment-in-full-before-the-discount-date"></a>Udlign en delvis debitorbetaling, og udlign den endelige betaling fuldt ud før rabatdatoen

[!include[banner](../includes/banner.md)]


Denne artikel indeholder scenarier, der viser, hvordan du registrerer delbetalinger for en kunde og anvender kasserabatter i kasserabatperioden.

Fabrikam sælger varer til debitor 4028. Fabrikam tilbyder en kasserabat på 1 procent, hvis fakturaen betales i løbet af 14 dage. Fakturaer skal betales inden 30 dage. Fabrikam tilbyder også kasserabatter på delvise indbetalinger. Udligningsparametrene er placeret på siden **Kreditorparametre**.

## <a name="customer-invoice"></a>Debitorfaktura
Den 25. juni indtaster og bogfører Arnie en faktura på 1.000,00 for debitor 4028. Arnie kan se denne postering på siden **Debitorposteringer**.

| Bilag   | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo  | Valuta |
|-----------|------------------|-----------|---------|--------------------------------------|---------------------------------------|----------|----------|
| FTI 10010 | Faktura          | 25-6-2015 | 10010   | 1.000,00                             |                                       | 1.000,00 | USD      |

Fra siden **Debitor** eller **Debitorposteringer** Arne kan åbne siden **Udlign posteringer** for at få vist datoerne og beløbene for kasserabatter, der er tilgængelige for fakturaen. Forfaldsdatoen er den 25. juli, og en kasserabat på 10,00 er tilgængelig, hvis fakturaen betales inden den 9. juli.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | FTI 10010 | 4028    | 25-6-2015 | 25-7-2015 | 10010   | 1.000,00                       | USD      | 990,00           |

Rabatoplysninger for den markerede faktura vises nederst på siden **Udlign posteringer**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 7/09/2015 |
| Kasserabatbeløb         | 10,00     |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | 10,00     |

Arnie klikker på fanen **Kasserabat** for at få vist rabatbeløbet.

| Kasserabatdato | Kasserabatbeløb | Beløb i transaktionsvaluta |
|--------------------|----------------------|--------------------------------|
| 9-7-2015           | 10,00                | 990,00                         |
| 25-7-2015          | 0,00                 | 1.000,00                       |

## <a name="partial-payment-by-using-the-enter-customer-payments-page"></a>Delvis betaling ved hjælp af siden Angiv debitorbetalinger
Debitor 4028 sender en betaling på 500,00 den 1. juli. For at angive denne betaling klikker Arnie ikke på **Linjer**. I stedet registrerer han betalingen ved at oprette en ny betalingskladde og derefter åbne siden **Angiv debitorbetalinger**. Han indtaster oplysningerne om betaling og markerer den faktura, som han har angivet. Når Arnie skriver **500,00** som beløbet, skriver han også **500,00** i feltet **Beløb til betaling** i gitteret. Da Fabrikam giver mulighed for en kasserabat på delbetalinger, kan han se, at en delvis kasserabat på 5,05 også bliver medtaget. Beregningen af denne rabat er 500,00 ÷ 0,99 × 0,01 = 5,05. (I denne beregning divideres 500,00 med 0,99, fordi der er en rabat på 1 %. Derfor betaler debitoren 99 % af fakturaen. Resultatet multipliceres derefter med rabatprocenten, som er 1 % eller 0,01. Hvis kunden tager den fulde rabat på 10,00, bliver det beløb, der skal afregnes 990,00). Rabatoplysninger vises i gitteret i bunden af siden **Angiv debitorbetalinger**.

| Kasserabatbeløb, der skal medtages | Medtaget kasserabat | Beløb til betaling |
|------------------------------|---------------------|---------------|
| 5,05                         | 0,00                | 500,00        |

## <a name="partial-payment-by-using-the-journal-lines"></a>Delvis betaling ved hjælp af kladdelinjer
I stedet for at åbne siden **Angiv debitorbetalinger** i betalingskladden, kan Arnie klikke på **Linjer** for at angive en betaling. Udbetalingskladden vises, og Arnie kan angive en linje for debitor 4028. Arnie åbner derefter siden **Udlign posteringer**, så han kan markere fakturaen til udligning. Arnie markerer fakturaen og ændrer værdien i feltet **Beløb, der skal udlignes** til **500,00**. Han ser igen, at værdien i feltet **Kasserabatbeløb** er **10,00** for hele fakturaen, og at værdien i feltet **Kasserabatbeløb, der skal medtages** er **5,05**. Arnie udligner derfor 505,05 af denne faktura.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | FTI 10010 | 4028    | 25-6-2015 | 25-7-2015 | 10010   | 1.000,00                       | USD      | 500,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 7/09/2015 |
| Kasserabatbeløb         | 10,00     |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | 5,05      |

Hvis debitoren ønsker at udligne præcist halvdelen af fakturaen, indsender debitoren en betaling på 495,00. I så fald skriver Arnie **495,00** i feltet **Beløb, der skal udlignes**. Kasserabatten for 5,00 vil desuden blive medtaget, så det samlede udlignede beløb er 500,00.

| Foretag afmærkning     | Anvend kasserabat | Bilag   | Konto | Dato      | Forfaldsdato  | Faktura | Beløb i transaktionsvaluta | Valuta | Beløb, der skal udlignes |
|----------|-------------------|-----------|---------|-----------|-----------|---------|--------------------------------|----------|------------------|
| Markeret | Almindelig            | FTI 10010 | 4028    | 25-6-2015 | 25-7-2015 | 10010   | 1.000,00                       | USD      | 495,00           |

Rabatoplysninger vises nederst på siden **Udlign åbne posteringer**.

|                              |           |
|------------------------------|-----------|
| Kasserabatdato           | 7/09/2015 |
| Kasserabatbeløb         | 10,00     |
| Anvend kasserabat            | Almindelig    |
| Medtaget kasserabat          | 0,00      |
| Kasserabatbeløb, der skal medtages | 5,00      |

Arnie lukker siden **Udlign posteringer**. Der oprettes en betalingslinje for 495,00 i kladden, og Arnie bogfører derefter kladden. Han kan gennem debitorposteringerne på siden **Debitorposteringer**. På denne side kan Arnie se, at fakturaen har en saldo på 500,00. Han ser også en betaling på 495,00 og en rabat på 5,00.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI 10010  | Faktura          | 25-6-2015 | 10010   | 1.000,00                             |                                       | 500,00  | USD      |
| ARP-10010  |  Betaling         | 7/1/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 |  Kasserabat   | 7/1/2015  |         |                                      | 5,00                                  | 0,00    | USD      |

## <a name="payment-for-the-remaining-amount"></a>Betaling af det resterende beløb
Debitor 4028 betaler resten af beløbet på 495,00 den 8. juli, som er inden for kasserabatperioden. Arnie opretter betalingskladden den 8. juli og markerer posteringen til udligning. Han ser, at det beløb, der skal udlignes, er 495,00. Værdien i feltet **Forkalkuleret kasserabat** er **5,00**, fordi rabatten på 5,00 blev medtaget tidligere.

|                         |        |
|-------------------------|--------|
| Afmærket i alt            | 495,00 |
| Forkalkuleret kasserabat | 5,00   |

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

Arnie bogfører denne betalingskladde og gennemgår debitorposteringerne på siden **Debitorposteringer**. Saldoen for fakturaen er nu 0,00, og Arnie ser to betalinger og to kasserabatter.

| Bilag    | Transaktionstype | Dato      | Faktura | Beløb i transaktionsvalutadebet | Beløb i transaktionsvalutakredit | Saldo | Valuta |
|------------|------------------|-----------|---------|--------------------------------------|---------------------------------------|---------|----------|
| FTI 10010  | Faktura          | 25-6-2015 | 10010   | 1.000,00                             |                                       | 0,00    | USD      |
| ARP-10010  | Betaling          | 7/1/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10010 | Kasserabat    | 7/1/2015  |         |                                      | 5,00                                  | 0,00    | USD      |
| ARP-10011  | Betaling          | 7/8/2015  |         |                                      | 495,00                                | 0,00    | USD      |
| DISC-10011 | Kasserabat    | 7/8/2015  |         |                                      | 5,00                                  | 0,00    | USD      |






