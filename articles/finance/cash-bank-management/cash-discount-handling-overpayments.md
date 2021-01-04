---
title: Kasserabatter i forbindelse med overbetalinger
description: Denne artikel indeholder scenarier, der viser, hvordan en betaling skal håndteres, når kunden skal have en kasserabat, men har betalt for meget.
author: panolte
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym, LedgerJournalTransVendPaym, VendOpenTrans, VendParameters
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14171
ms.assetid: a94d0fd0-57ba-4054-93c8-519d01d50e19
ms.search.region: Global
ms.author: panolte
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 3f0714eab80f43695b2b93f77a70f31c360277f9
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441703"
---
# <a name="cash-discounts-for-overpayments"></a>Kasserabatter i forbindelse med overbetalinger

[!include [banner](../includes/banner.md)]

Denne artikel indeholder scenarier, der viser, hvordan en betaling skal håndteres, når kunden skal have en kasserabat, men har betalt for meget. 

En faktura anses for overbetalt, når betalingsbeløbet er større end fakturabeløbet minus kasserabatten. For at angive, hvordan en mulig kasserabatdifference håndteres, når en faktura er overbetalt skal du bruge felterne **Håndtering af kasserabat** og **Maksimal over- eller underbetaling** på siden **Debitorparametre**. I følgende eksempel har kunden betalt 0,50 for meget for fakturaen.

| Fakturatotal | Tilgængelig kasserabat | Det beløb, der skal betales, indeholder kasserabatten | Beløb, som kunden faktisk betaler |
|---------------|-------------------------|-----------------------------------------------------|-----------------------------------|
| 105,00        | 10,50                   | 94,50                                               | 95,00                             |

## <a name="cash-discount-administration--specific"></a>Håndtering af kasserabat = Specifik
Når **Specifik** er valgt i feltet **Håndtering af kasserabat** på siden **Konti til automatisk posteringer**, medtages den fulde kasserabat. Det overbetalte beløb bogføres enten til en finanskonto til kasserabatdifference eller forbliver en saldo på debitorens konto. Funktionen afhænger af, om det overbetalte beløb er mellem 0,00 og det beløb, der er angivet i feltet **Maksimal over- eller underbetaling**, eller om det overbetalte beløb er mere end beløbet for **Maksimal over- eller underbetaling**.

### <a name="scenario-1"></a>Scenarie 1

I dette scenarie er det for meget betalte beløb mellem 0,00 og den maksimale over- eller underbetaling. Der angives en faktura for 105,00, og en kasserabat er tilgængelig, hvis fakturaen betales inden for syv dage.

| Fakturatotal | Tilgængelig kasserabat | Det beløb, der skal betales, indeholder kasserabatten |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Kunden indsender en betaling på 95,00 inden for kasserabatperioden. Betalingen udlignes i forhold til fakturaen på 105,00. Når fakturaen og betalingen er udlignet, oprettes følgende posteringer i Debitor.

| Transaktion   | Beløb | Saldo |
|---------------|--------|---------|
| Faktura       | 105,00 | 0,00    |
| Betaling       | -95,00 | 0,00    |
| Kasserabat | -10,50 | 0,00    |

Følgende regnskabsposter genereres for betalingen og udligningen. **Betaling**

| Konto             | Debetbeløb | Kreditbeløb |
|---------------------|--------------|---------------|
| Kontant                | 95,00        |               |
| Debitor |              | 95,00         |

**Udligning**

| Konto                                                                                                          | Debetbeløb | Kreditbeløb |
|------------------------------------------------------------------------------------------------------------------|--------------|---------------|
| Kasserabatten (feltet **Hovedkonto til debitorrabatter** på siden **Kasserabatter**)                 | 10,50        |               |
| Debitor                                                                                              |              | 10,50         |
| Debitorkasserabat (feltet **Debitor, kasserabat** på siden **Konti til automatisk posteringer**) |              | 0,50          |
| Debitor                                                                                              | 0,50         |               |

### <a name="scenario-2"></a>Scenarie 2

I dette scenarie overstiger det for meget betalte beløb det maksimale overbetalings eller underbetalingsbeløb. Der angives en faktura for 105,00, og en kasserabat er tilgængelig, hvis fakturaen betales inden for syv dage.

| Fakturatotal | Tilgængelig kasserabat | Det beløb, der skal betales, indeholder kasserabatten |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Kunden indsender en betaling på 95,00 inden for kasserabatperioden. Betalingen udlignes i forhold til fakturaen på 105,00. Når fakturaen og betalingen er udlignet, oprettes følgende posteringer i Debitor.

| Transaktion   | Beløb | Saldo |
|---------------|--------|---------|
| Faktura       | 105,00 | 0,00    |
| Betaling       | -95,00 | -0,50   |
| Kasserabat | -10,50 | 0,00    |

Det for meget betalte beløb på 0,50 forbliver som en åben saldo for betalingen og kan udlignes mod en anden faktura. Følgende regnskabsposter genereres for betalingen og udligningen. **Betaling**

| Konto             | Debetbeløb | Kreditbeløb |
|---------------------|--------------|---------------|
| Kontant                | 95,00        |               |
| Debitor |              | 95,00         |

**Udligning**

| Konto                                                                                          | Debetbeløb | Kreditbeløb |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Kasserabatten (feltet **Hovedkonto til debitorrabatter** på siden **Kasserabatter**) | 10,50        |               |
| Debitor                                                                              |              | 10,50         |

## <a name="cash-discount-administration--unspecific"></a>Håndtering af kasserabat = Uspecifik
Når **Uspecifik** er valgt i feltet **Håndtering af kasserabat** på siden **Konti til automatisk posteringer**, reduceres kasserabatbeløbet af overbetalingsbeløbet. Denne funktion gælder altid, uanset om overbetaling beløbet er over eller under det beløb, der er angivet i feltet **Maksimal over- eller underbetaling**.

### <a name="scenario-3"></a>Scenarie 3

I dette scenarie angives en faktura for 105,00, og en kasserabat er tilgængelig, hvis fakturaen betales inden for syv dage.

| Fakturatotal | Tilgængelig kasserabat | Det beløb, der skal betales, indeholder kasserabatten |
|---------------|-------------------------|-----------------------------------------------------|
| 105,00        | 10,50                   | 94,50                                               |

Kunden indsender en betaling på 95,00 inden for kasserabatdatoen. Betalingen udlignes i forhold til fakturaen på 105,00. Når fakturaen og betalingen er udlignet, oprettes følgende posteringer i Debitor.

| Transaktion   | Beløb | Saldo |
|---------------|--------|---------|
| Faktura       | 105,00 | 0,00    |
| Betaling       | -95,00 | -0,00   |
| Kasserabat | -10,00 | 0,00    |

Kasserabatbeløbet reduceres fra 10,50 til 10,00. Betalingen og fakturaen anses for udlignet. **Betaling**

| Konto             | Debetbeløb | Kreditbeløb |
|---------------------|--------------|---------------|
| Kontant                | 95,00        |               |
| Debitor |              | 95,00         |

**Udligning**

| Konto                                                                                          | Debetbeløb | Kreditbeløb |
|--------------------------------------------------------------------------------------------------|--------------|---------------|
| Kasserabatten (feltet **Hovedkonto til debitorrabatter** på siden **Kasserabatter**) | 10,50        |               |
| Debitor                                                                              |              | 10,50         |





