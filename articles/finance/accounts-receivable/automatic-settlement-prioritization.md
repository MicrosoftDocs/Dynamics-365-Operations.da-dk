---
title: Automatisk udligning og prioritering
description: I dette emne beskrives det, hvordan posteringerne udlignes, hvis du vælger automatisk udligning på siden Debitorparametre. Det forklarer også, hvordan automatisk udligning kan bruges sammen med betalingsprioriteten.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustOpenTrans, CustParameters, LedgerJournalTransCustPaym
audience: Application User
ms.reviewer: roschlom
ms.search.scope: Core, Operations
ms.custom: 14531
ms.assetid: e7837cf6-ec69-44b4-8d47-eba38d5c7b1f
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b596557e80035e8d62d01f156a6678c75e4ae573
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4441532"
---
# <a name="automatic-settlement-and-prioritization"></a>Automatisk udligning og prioritering

[!include [banner](../includes/banner.md)]

I dette emne beskrives det, hvordan posteringerne udlignes, hvis du vælger automatisk udligning på siden Debitorparametre. Det forklarer også, hvordan automatisk udligning kan bruges sammen med betalingsprioriteten.

Du har to muligheder, når du udligner betalinger med fakturaer og andre transaktioner. Du kan manuelt vælge posteringerne, der skal udlignes, eller systemet kan vælge posteringerne automatisk ved hjælp af funktionen til automatisk udligning. Du kan også tilpasse, hvordan automatiske udligninger skal behandles, ved hjælp af indstillingen **Prioriter udligning**. Disse indstillinger er en del af de udligningsparametre, der er defineret på siden **Debitorparametre**. Den måde, posteringer automatisk udlignes på, kan variere, afhængigt af den metode, der bruges til automatisk udligning. Følgende metoder er tilgængelige:

-   Brugerdefineret udligningsprioritet
-   Automatisk standardudligning

I følgende afsnit beskrives, hvordan posteringerne udlignes for hver metode.

## <a name="example-transactions"></a>Eksempeltransaktioner
Eksemplerne på udligninger senere i denne artikel er baseret på følgende transaktioner. Alle transaktioner er for debitor 2050.

| Postering   | Dato        | Beløb | Kasserabatbetingelser. | Kasserabatdato | Bemærkninger                                                                                                                                                                                      |
|---------------|-------------|--------|---------------------|--------------------|-----------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|
| Faktura 1     | 15. august   | 100,00 | 2%14, Netto 30        | 29. august          |                                                                                                                                                                                               |
| Faktura 2     | 1. september | 250,00 | 2%14, Netto 30        | 15. september       |                                                                                                                                                                                               |
| Faktura 3     | Oktober 15  | 500,00 | 2% 14/Net 30        | 29. oktober         |                                                                                                                                                                                               |
| Rentenota | 15. oktober  | 7:00   |                     |                    | Denne rentenota er for faktura 1 og 2. Beløbet beregnes som 2 procent renter på beløb, der er forfaldet for mindst 30 dage siden. F.eks. 0,02 × (100,00 + 250,00) = 7,00. |

## <a name="user-defined-settlement-priority"></a>Brugerdefineret udligningsprioritet
Hvis du angiver **Brug prioritet til automatiske udligninger** til **Ja** på siden **Debitorparametre**, bruges den udligningsprioritet, du definerer på siden **Udligningsprioritet**, når posteringer er markeret til automatisk udligning. Følgende udligningsprioritet er defineret i dette eksempel:

1.  Transaktionstype
    -   Betalingsgebyrer
    -   Rykkere
    -   Rentenotaer
    -   Fakturaer

2.  Posteringsdato, Stigende
3.  Bilag

Hvis du bogfører en betaling på 700,00 den 25. oktober, udlignes betalingen med transaktionerne i følgende rækkefølge.

| Bilag       | Dato       | Faktura | Beløb i transaktionsvaluta | Beløb, der skal udlignes | Saldo | Valuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Rentenota | 15-10-2015 |         | 7:00                           | 7:00             | 0,00    | USD      |
| Faktura 1     | 15-08-2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Faktura 2     | 01-09-2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Faktura 3     | 15-10-2015 |         | 500,00                         | 343,00           | 157,00  | USD      |

## <a name="default-automatic-settlement"></a>Automatisk standardudligning
Hvis der ikke er en brugerdefineret udligningsprioritet, markeres posteringer automatisk til udligning på baggrund af forfaldsdatoen. Udlignede transaktioner skal have samme valuta som den transaktion, som de er udlignet med. Hvis du bogfører en betaling på 700,00 den 25. oktober, markeres følgende transaktioner til udligning.

| Bilag       | Dato       | Faktura | Beløb i transaktionsvaluta | Beløb, der skal udlignes | Saldo | Valuta |
|---------------|------------|---------|--------------------------------|------------------|---------|----------|
| Faktura 1     | 15-08-2015  | 10001   | 100,00                         | 100,00           | 0,00    | USD      |
| Faktura 2     | 01-09-2015   | 10002   | 250,00                         | 250,00           | 0,00    | USD      |
| Faktura 3     | 15-10-2015 |         | 500.00                         | 350.00           | 150.00  | USD      |
| Rentenota | 15-10-2015 |         | 7.00                           | 0,00             | 7.00    | USD      |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]