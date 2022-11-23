---
title: Værdiregulering af valuta i et konsolideret regnskab
description: Denne artikel beskriver, hvordan du revaluerer valuta i et konsolideret regnskab.
author: aprilolson
ms.date: 10/02/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LedgerExchAdjHist
audience: Application User
ms.reviewer: twheeloc
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c05ef0d4d05d5113d3b858dafe49ee9c1c7211d9
ms.sourcegitcommit: cf6b764824bd1cf2c0dde6d37ddd0a7abab87ff0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/16/2022
ms.locfileid: "9779656"
---
# <a name="currency-revaluation-in-a-consolidation-company"></a>Værdiregulering af valuta i et konsolideret regnskab

[!include [banner](../includes/banner.md)]

Når du konsoliderer data fra én regnskabsvalutaen til en anden, skal du stadig køre værdiregulering af valuta, hvis der sker en ændring i valutakursen, så dine kontosaldi værdireguleres korrekt. Når du oprindeligt konsoliderer dataene, skal du bruge fanen **Valutaomregning** for at markere de første valutakurser til oversættelse under konsolideringsprocessen. Når en ny valutakurs er angivet (f.eks. i den næste måned), skal du værdiregulere kontosaldiene. Urealiserede gevinster eller tab opdateres derefter baseret på den nye valutakurs og dato. Følgende eksempel illustrerer regnskabsposterne, der er oprettet under processen.

## <a name="company-setup"></a>Virksomhedsopsætning
-   **Kilde/driftsregnskab (USMF)** – USD bruges som regnskabs- og rapporteringsvaluta.
-   **Konsolideret regnskab (CON)** – EUR bruges som regnskabs- og rapporteringsvaluta.
    -   **Realiseret gevinst** – Finanskonto 801500
    -   **Realiseret tab** – Finanskonto 801600
    -   **Urealiseret gevinst** – Finanskonto 801600
    -   **Urealiseret tab** – Finanskonto 801400

## <a name="original-transactions"></a>Oprindelige posteringer
### <a name="cash-receipt-transactions-in-usmf"></a>Indbetalingsposteringer i USMF

| Date       | Finanskonto               | Valuta | Antal |
|------------|------------------------------|----------|--------|
| 11/10/2020 | 110110 – Kontant                | USD      | 500    |
| 11/10/2020 | 130100 – Debitorer | USD      | -500   |

## <a name="exchange-rates"></a>Valutakurser

| Fra valuta | Til valuta | Igangsæt dato | Valutakurs |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 1/10/2020  | 200           |
| EUR           | USD         | 1/11/2020  | 150           |
| EUR           | USD         | 1/12/2017  | 100           |

## <a name="perform-the-consolidation-for-october-2020"></a>Udføre konsolidering for oktober 2020
### <a name="balances-in-the-consolidation-company"></a>Saldiene i det konsoliderede regnskab

| Finanskonto | Valuta | Beløb | Kalkulation    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50 %  |
| 130100         | EUR      | -250   | -500 USD × 50 % |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-november-30-2020"></a>Udfør værdiregulering af valuta for konti fra 1. oktober 2020 til 30. november 2020
### <a name="balances-in-the-consolidation-company"></a>Saldiene i det konsoliderede regnskab

| Finanskonto | Valuta | Beløb  | Kalkulation                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333,33  | Oprindeligt beløb på 500 × 66,6667 %  |
| 130100         | EUR      | -333,33 | Oprindeligt beløb på -500 × 66,6667 % |
| 801400         | EUR      | 83,33   | 333,33-250                       |
| 801600         | EUR      | -83,33  | -333,33 – (-250)                   |

Du vil se flere posteringer for rapporteringsvalutabeløbene.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2020-through-december-31-2020"></a>Udfør værdiregulering af valuta for konti fra 1. oktober 2020 til 31. december 2020
### <a name="balances-in-the-consolidation-company"></a>Saldiene i det konsoliderede regnskab

| Finanskonto | Valuta | Beløb  | Kalkulation                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Oprindeligt beløb på 500 × 1 %                           |
| 130100         | EUR      | -500,00 | Oprindeligt beløb på -500 × 1                          |
| 801400         | EUR      | 250     | 500-333,33 = 166,67 166,67 + 83,33 = 250           |
| 801600         | EUR      | -250    | -500 – (-333,33) = -166,67-166,67 + (-83,33) = -250 |







[!INCLUDE[footer-include](../../includes/footer-banner.md)]
