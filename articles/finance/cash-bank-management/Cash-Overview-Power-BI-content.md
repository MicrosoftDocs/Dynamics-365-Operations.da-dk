---
title: Power BI-indhold til oversigt over kontanter
description: Denne artikel beskriver Power BI-indholdet til Oversigt over kontanter. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdet.
author: angelad116
ms.date: 07/16/2020
ms.topic: overview
ms.prod: ''
ms.technology: ''
ms.search.form: BankTreasurerWorkspace
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: angelading
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: a255afac3aa68f3a48b21e4d2fbfb046a9de603c
ms.sourcegitcommit: 0b7a034e644f4d93fe55c7baca5a3f89dbe56898
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/14/2022
ms.locfileid: "9151993"
---
# <a name="cash-overview-power-bi-content"></a>Power BI-indhold til oversigt over kontanter

[!include [banner](../includes/banner.md)]

Denne artikel beskriver Microsoft Power BI-indholdet til **Oversigt over kontanter**. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdet.

## <a name="overview"></a>Overblik

Power BI-indholdet for **Oversigt over kontanter** blev oprettet for personer, der er ansvarlige for kontanter i deres organisation. Power BI-indholdet til **Oversigt over kontanter** giver indsigt i din likviditet. Det indeholder også budgetter, der kan hjælpe dig med at træffe bedre beslutninger og derfor give en forbedret likviditetstilstand. Du kan analysere kontanter efter juridisk enhed, valuta og bankkonto for at få en bedre forståelse af overskud og mangler.

## <a name="setup-needed-to-view-power-bi-content"></a>Opsætning, der kræves for at se Power BI-indhold

Følgende opsætning skal være fuldført, før der kan vises data i de visuelle elementer **Oversigt over kontanter** og **Bankstyring** i Power BI.

1. Gå til **Systemadministration > Konfiguration > systemparametre** for at angive **Systemvaluta** og **Systemvalutakurs**.
2. Gå til **Finans > Kalendere > Regnskabskalendere** for at validere regnskabskalenderdatoer, der er tildelt den aktive tidsperiode.
3. Gå til **Finans > Opsætning > Finans** for at angive **Regnskabsvaluta** og **Valutakurstype**.
4. Definer valutakurser mellem transaktionsvalutaer og regnskabsvaluta, regnskabsvaluta og systemvaluta samt regnskabsvaluta og bankvalutaer. Det gør du ved at gå til **Finans > Valutaer > Valutakurser**.
5. Konfigurer og kør likviditetsbudgettering. Du kan finde flere oplysninger om, hvordan du konfigurerer likviditetsbudgettering, i [Likviditetsbudget](./cash-flow-forecasting.md). 
6. Gå til **Systemadministration > Konfiguration > Enhedslager** for at opdatere den samlede måling af **LedgerCovLiquidityMeasurement**.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indholdet

Rapporter fra Power BI-indholdet til **Oversigt over kontanter** vises i arbejdsområderne **Oversigt over kontanter** og **Bankstyring**.

For at få vist rapporter over likviditetsbudgettering med data skal du først køre budgetteringsberegningsprocessen ved hjælp af funktionen **Beregn likviditetsbudgetter** fra området Likviditets- og bankstyring. Dette skal udføres for hvert regnskab, der er medtaget i budgettet.  På siden **Enhedslager** skal du derefter opdatere den samlede LedgerCovLiquidityMeasurement-måling.  

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


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
