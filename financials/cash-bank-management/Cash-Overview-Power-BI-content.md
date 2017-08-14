---
title: Power BI-indhold for oversigt over kontanter
description: "Dette emne beskriver Power BI-indhold for oversigt over kontanter. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdet."
author: saraschi2
manager: AnnBe
ms.date: 06/22/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, UnifiedOperations
ms.search.region: Global
ms.author: saraschi
ms.search.validFrom: 2017-06-30T00:00:00.000Z
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 367fe61492648ee3ee629a8121e664dfaa0c6c99
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="cash-overview-power-bi-content"></a>Power BI-indhold for oversigt over kontanter

[!include[banner](../includes/banner.md)]

Dette emne beskriver Microsoft Power BI-indhold for **Oversigt over kontanter**. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der blev brugt til at oprette indholdet.

## <a name="overview"></a>Overblik

Power BI-indholdet for **Oversigt over kontanter** blev oprettet for personer, der er ansvarlige for kontanter i deres organisation. **Oversigt over kontanter** Power BI-indholdet giver indsigt i din likviditet. Det indeholder også budgetter, der kan hjælpe dig med at træffe bedre beslutninger og derfor give en forbedret likviditetstilstand. Du kan analysere kontanter efter juridisk enhed, valuta og bankkonto for at få en bedre forståelse af overskud og mangler.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold

Hvis du bruger Opdateringen til Dynamics 365 for Finance and Operations, Enterprise edition fra juli 2017, vises rapporterer fra Power BI-indholdet **Oversigt over kontanter** i arbejdsområderne **Oversigt over kontanter** og **Bankstyring**.

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

## <a name="extending-the-power-bi-content"></a>Udvidelse af Power BI-indhold
Du kan levere fremragende analyser til dem, der ikke logger på Dynamics 365, ved hjælp af de indholdspakker, der er tilgængelige i Lifecycle Services (LCS). Disse indholdspakker kan redigeres, så de omfatter andre rapporter eller grafik, som derefter kan udgives på din Power BI.com-lejer til analyse. 

Du kan finde Power BI-indhold for **Oversigt over kontanter** i biblioteket med delte aktiver i LCS. Du kan finde flere oplysninger om, hvordan du downloader indhold og implementerer det i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](/dynamics365/unified-operations/dev-itpro/analytics/power-bi-content-microsoft-partners). Hvis du vil se en demo, der viser, hvordan du implementerer Power BI-indholdet, kan du se dette Office Mix [Power BI-indhold fra Microsoft og dine partnere i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

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

Disse enheder blev brugt til at oprette beregnede målinger i datamodellen. Disse beregnede mål bruges derefter til at beregne diagrammer og rapporter, der bruges i Power BI-indholdet for **Oversigt over kontanter**. Hvis du vil medtage yderligere beregninger i rapporter og dashboard, kan du hente og redigere Power BI-filen fra LCS. Denne fil er den standarddatamodel, der blev brugt til at oprette indholdet. Når du har foretaget ændringerne, kan du oprette indhold for organisationen og dashboards, som indeholder de oplysninger, du har tilføjet.


