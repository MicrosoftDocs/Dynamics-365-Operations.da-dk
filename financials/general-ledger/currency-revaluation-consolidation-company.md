---
title: "Værdiregulering af valuta i et konsolideret regnskab"
description: 
author: rschloma
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 62183
ms.assetid: 2762baaf-0c10-4ff7-8713-c506d6c29b98
ms.search.region: Global
ms.author: hminzner
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 0c6a7bdc4ba82dd57ab3e395e6dfb0ae4de31fc4
ms.openlocfilehash: b8ad4aa1653d090b46a7e35e9e710324df2edfe5
ms.lasthandoff: 03/31/2017


---

# <a name="currency-revaluation-in-a-consolidation-company"></a>Værdiregulering af valuta i et konsolideret regnskab



Når du konsoliderer data fra én regnskabsvalutaen til en anden, skal du stadig køre værdiregulering af valuta, hvis der sker en ændring i valutakursen, så dine kontosaldi værdireguleres korrekt. Når du oprindeligt konsoliderer dataene, skal du bruge fanen **Valutaomregning** for at markere de første valutakurser til oversættelse under konsolideringsprocessen. Når en ny valutakurs er angivet (f.eks. i den næste måned), skal du værdiregulere kontosaldiene. Urealiserede gevinster eller tab opdateres derefter baseret på den nye valutakurs og dato. Følgende eksempel illustrerer regnskabsposterne, der er oprettet under processen.

## <a name="company-setup"></a>Virksomhedsopsætning
-   **Kilde/driftsregnskab (USMF)** – USD bruges som regnskabs- og rapporteringsvaluta.
-   **Konsolideret regnskab (CON)** – EUR bruges som regnskabs- og rapporteringsvaluta.
    -   ** Realiseret gevinst ** – finanskontoen 801500
    -   **Realiseret tab** – Finanskonto 801600
    -   **Urealiseret gevinst** – Finanskonto 801600
    -   **Urealiseret tab** – Finanskonto 801400

## <a name="original-transactions"></a>Oprindelige posteringer
### <a name="cash-receipt-transactions-in-usmf"></a>Indbetalingsposteringer i USMF

| Dato       | Finanskonto               | Valuta | Beløb |
|------------|------------------------------|----------|--------|
| 10/11/2015 | 110110 – Kontant                | USD      | 500    |
| 10/11/2015 | 130100 – Debitorer | USD      | -500   |

## <a name="exchange-rates"></a>Valutakurser
| Fra valuta | Til valuta | Startdato | Valutakurs |
|---------------|-------------|------------|---------------|
| EUR           | USD         | 10/1/2015  | 200           |
| EUR           | USD         | 11/1/2015  | 150           |
| EUR           | USD         | 12/1/2012  | 1000           |

## <a name="perform-the-consolidation-for-october-2015"></a>Udføre konsolidering for oktober 2015
### <a name="balances-in-the-consolidation-company"></a>Saldiene i det konsoliderede regnskab

| Finanskonto | Valuta | Beløb | Kalkulation    |
|----------------|----------|--------|----------------|
| 110110         | EUR      | 250    | 500 USD × 50 %  |
| 130100         | EUR      | -250   | -500 USD × 50 % |

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-november-30-2015"></a>Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 30. november 2015
### <a name="balances-in-the-consolidation-company"></a>Saldiene i det konsoliderede regnskab

| Finanskonto | Valuta | Beløb  | Kalkulation                        |
|----------------|----------|---------|------------------------------------|
| 110110         | EUR      | 333,33  | Oprindeligt beløb på 500 × 66,6667 %  |
| 130100         | EUR      | -333,33 | Oprindeligt beløb på -500 × 66,6667 % |
| 801400         | EUR      | 83,33   | 333,33-250                       |
| 801600         | EUR      | -83,33  | -333,33 – (-250)                   |

Du vil se flere posteringer for rapporteringsvalutabeløbene.

## <a name="perform-currency-revaluation-for-the-accounts-from-october-1-2015-through-december-31-2015"></a>Udfør værdiregulering af valuta for konti fra 1. oktober 2015 til 31. december 2015
### <a name="balances-in-the-consolidation-company"></a>Saldiene i det konsoliderede regnskab

| Finanskonto | Valuta | Beløb  | Kalkulation                                          |
|----------------|----------|---------|------------------------------------------------------|
| 110110         | EUR      | 500,00  | Oprindeligt beløb på 500 × 1 %                           |
| 130100         | EUR      | -500,00 | Oprindeligt beløb på -500 × 1                          |
| 801400         | EUR      | 250     | 500-333,33 = 166,67 166,67 + 83,33 = 250           |
| 801600         | EUR      | -250    | -500 – (-333,33) = -166,67-166,67 + (-83,33) = -250 |



