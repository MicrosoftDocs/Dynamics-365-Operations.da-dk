---
title: Power BI-indhold til Oversigt over kontanter
description: Dette emne beskriver Power BI-indholdet til Oversigt over kontanter. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdet.
author: saraschi2
manager: AnnBe
ms.date: 12/19/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 5dccb5c5c6c336607603dfc7a935c039e5ac4aa5
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "318643"
---
# <a name="cash-overview-power-bi-content"></a>Power BI-indhold til Oversigt over kontanter

[!include [banner](../includes/banner.md)]

Dette emne beskriver Power BI-indhold til **Oversigt over kontanter**. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdet.

## <a name="overview"></a>Overblik

Power BI-indholdet for **Oversigt over kontanter** blev oprettet for personer, der er ansvarlige for kontanter i deres organisation. Power BI-indholdet til **Oversigt over kontanter** giver indsigt i din likviditet. Det indeholder også budgetter, der kan hjælpe dig med at træffe bedre beslutninger og derfor give en forbedret likviditetstilstand. Du kan analysere kontanter efter juridisk enhed, valuta og bankkonto for at få en bedre forståelse af overskud og mangler.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet

Rapporter fra Power BI-indholdet til **Oversigt over kontanter** vises i arbejdsområderne **Oversigt over kontanter** og **Bankstyring**.

For at få vist rapporter over likviditetsbudgettering med data skal du først køre budgetteringsberegningsprocessen ved hjælp af funktionen **Beregn likviditetsbudgetter** fra området Likviditets- og bankstyring.  Dette skal udføres for hvert regnskab, der er medtaget i budgettet.  På siden **Enhedslager** skal du derefter opdatere den samlede LedgerCovLiquidityMeasurement-måling.  

Til demonstrationsformål kan du tilføje demodata for likviditetsbudgettering ved hjælp af siden **Generér data** fra modulet Demodata.  Dette script indsætter data i likviditetsbudgetteringstabeller for hurtig angivelse af oplysninger, der er nødvendige i rapporter.  Dette modul er kun tilgængeligt, hvis demodatapakkemodellen er installeret i miljøet. 

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet
Følgende tabel indeholder oplysninger om de nøgletal, der findes på de enkelte rapportsider i Power BI-indholdet til **Oversigt over kontanter**.

| Rapport                                | Indhold |
|---------------------------------------|----------|
| Oversigt over kontanter – alle firmaer         | <ul><li>Indgående og udgående pengestrømme i systemvalutaen</li><li>Saldi for budgetteret valuta</li><li>Den samlede banksaldo i systemvalutaen</li><li>Saldo pr. juridisk enhed</li><li>Dagens faktisk vs. budgetteret saldo i bankkontoens valuta</li></ul> |
| Oversigt over kontanter – aktuelt firma       | <ul><li>Indgående og udgående pengestrømme i regnskabsvalutaen</li><li>Saldi for budgetteret valuta</li><li>Den samlede banksaldo i regnskabsvalutaen</li><li>Dagens faktisk vs. budgetteret saldo i bankkontoens valuta</li></ul> |
| Likviditetsbudget – alle firmaer    | <ul><li>Indgående og udgående pengestrømme i systemvalutaen</li><li>Daglig budgetoversigt</li><li>Budgetdetaljer</li></ul> |
| Likviditetsbudget – firmavaluta | <ul><li>Indgående og udgående pengestrømme i regnskabsvalutaen</li><li>Daglig budgetoversigt</li><li>Budgetdetaljer</li></ul> |
| Valutabudget                     | <ul><li>Saldi for budgetteret valuta</li><li>Daglig valutaoversigt</li><li>Budgetdetaljer</li></ul> |
| Banksaldi                         | <ul><li>Den samlede banksaldo i systemvalutaen</li><li>Saldo pr. juridisk enhed</li><li>Dagens faktisk vs. budgetteret saldo i bankkontoens valuta</li><li>Saldo pr. bankkonto</li><li>Saldo pr. valuta</li></ul> |


## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

Følgende tabel viser de enheder, som Power BI-indholdet for **Oversigt over kontanter** er baseret på.

| Enhed                                                                          | Indhold |
|---------------------------------------------------------------------------------|----------|
| LedgerCovLiquidityMeasurement\_Company                                          | Virksomheder, som rapporter kan filtreres efter |
| LedgerCovLiquidityMeasurement\_Date                                             | Datoer, som rapporter kan filtreres efter |
| LedgerCovLiquidityMeasurement\_LedgerCovForecastActual                          | Faktisk banksaldo i forhold til sidste budgetterede banksaldo |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidity                               | Budgetterede posteringsdetaljer |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceCompany    | Opsummeret indgående pengestrømme, udgående pengestrømme og saldo ved hjælp af regnskabsvalutaen for hvert regnskab |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityInflowOutflowBalanceEnterprise | Opsummeret indgående pengestrømme, udgående pengestrømme og saldo ved hjælp af systemvalutaen for alle regnskaber |
| LedgerCovLiquidityMeasurement\_LedgerCovLiquidityTransactionCurrency            | Opsummeret nettoposteringsbeløb og saldo for valutaer ved hjælp af transaktionsvalutaen |


