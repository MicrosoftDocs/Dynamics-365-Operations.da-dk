---
title: Budgetanalyse i den offentlige sektor
description: Denne artikel beskriver, hvordan du bruger siden Budgetanalyse til at få vist indtægter og udgifter efter økonomisk dimension, og det besvarer ofte stillede spørgsmål, herunder forskellene på siden Budgetanalyse og statistiksiden Budgetstyring.
author: v-kiarnd
ms.date: 01/28/2022
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 19641
ms.assetid: a1055712-0a20-425d-939d-de8564c358b8
ms.search.industry: Public sector
ms.search.form: BudgetAnalysisInquiry_PSN, BudgetControlStatistics, DimensionDetails, LedgerPeriodCode, LedgerTrialBalanceListPage
ms.openlocfilehash: e02e592b29c77a8c5c78377ec126993b0002da3d
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273713"
---
# <a name="budget-analysis-in-the-public-sector"></a>Budgetanalyse i den offentlige sektor

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du bruger siden Budgetanalyse til at få vist bogførte indtægter og udgifter efter økonomisk dimension, og det besvarer ofte stillede spørgsmål, herunder forskellene på siden Budgetanalyse og statistiksiden Budgetstyring. 

Denne artikel beskriver de budgetanalysefunktioner, som er tilgængelige for den offentlige sektor. 

Før du læser denne artikel, bør du også læse [Overblik over budgettering i den offentlige sektor](budgeting-public-sector.md). 

Du skal evt. angive følgende budgetteringsfunktioner for den offentlige sektor. Brug siden **Budgetanalyse** til at få vist bogførte indtægter og udgifter efter økonomisk dimension ved hjælp af en kombination af finanskonto og budgetstyringsdata. Du kan få vist opsummerede beløb og transaktionsdetaljer for reviderede budgetter, faktiske udgifter, behæftelser og forudgående behæftelser. 

Indtægter og udgifter kan opsummeres ved hjælp af de forskellige niveauer af økonomiske dimensioner. Hvis f.eks. budgetdimensioner er middel, organisation og hovedkonto, kan du vælge **Middel**, **Organisation** eller **Hovedkonto** for at se den økonomiske aktivitet opsummeret på det pågældende niveau. 

Du kan også bruge siden **Budgetanalyse** til at vælge en økonomisk dimensionsopsætning og et kolonnesæt. Vælg eller angiv følgende, og klik derefter på **Opdater totaler:**

-   Parametre
-   Datooplysninger
-   Økonomiske dimensioner

> [!NOTE] 
> På siden **Økonomiske dimensioner** kan du oprette de økonomiske dimensioner. Du kan angive datointervallet for transaktioner, der er medtaget, på siden **Datointervaller** i Finans.

## <a name="what-transaction-details-are-available-on-the-budget-analysis-page"></a>Hvilke transaktionsdetaljer er tilgængelige på siden Budgetanalyse?
Du kan vælge et element i gitteret og rulle ned for at se detaljer om følgende transaktioner:

-   **Revideret budgetbeløb** (summen af oprindeligt budget, revision, overførsel og overførte beløb)
-   **Faktiske udgifter** (summen af de debiteringer og krediteringer, der blev bogført i forhold til de økonomiske dimensionsværdier)
-   **Behæftelser** og **Budgetreservationer** (herunder oprindelige og eftergivelse af posteringer)

### <a name="tips"></a>Tip!

-   Du kan få vist de reviderede budgetregisterposter for budgetanalyseforespørgslen ved at klikke på **Opdateret budget** i handlingsruden. Budgettyperne for de reviderede budgetregisterposter omfatter det oprindelige budget, overførsel, flytning og revision. Disse beløb kommer fra tabellerne med budgetregisterposterne.
-   Du kan få vist de faktiske udgifter for budgetanalyseforespørgslen ved at klikke på **Faktisk**. Siden har indflydelse på den oprindelige dokumentside, f.eks. en avanceret finanspost. Disse beløb kommer fra tabellerne med finanskontoposterne, undtagen når indstillingen **Udgiftsbudget med overførsler** er valgt. Når denne indstilling er markeret, bruges budgetkildetabellerne.
-   Du kan få vist behæftelser og refererede transaktioner for budgetanalyseforespørgslen ved at klikke på **Behæftelse**. Siden påvirker den generelle budgetreservation (hvis den er implementeret) eller indkøbsordre for den valgte postering. Disse beløb kommer fra tabellerne til budgetkildesporing.
-   Du kan få vist budgetreservationer og refererede transaktioner for budgetanalyseforespørgslen ved at klikke på **Budgetreservation**. Siden har indflydelse på indkøbsrekvisitionen for den valgte postering. Disse beløb kommer fra tabellerne til budgetkildesporing.

## <a name="should-i-use-the-budget-control-statistics-page-or-the-budget-analysis-page"></a>Skal jeg bruge siden Statistik for budgetstyring eller siden Budgetanalyse?
Siden **Budgetstyringsdimension** er værktøjet, der skal bruges, når du vil analysere en enkelt budgetkonto, eller en kombination eller gruppe af konti efter periode og budgetstyringsdimension. Siden **Budgetanalyse** er mere fleksibel. Du kan bruge den til at forespørge i enhver dimensionsrækkefølge på tværs af kontoplaner eller til at forespørge på en underopsætning af en konto. Du kunne f.eks. få vist en liste over totalerne for midlerne for år til dato, analysere frem til et bestemt middel for at få vist afdelingsværktøjer og derefter analysere frem til en bestemt afdeling for at få vist kontototalerne.

Følgende tabel beskriver forskellene mellem disse sider.

| Siden Statistik for budgetstyring | Budgetanalyse                        |
|---|---|
| Viser budgetsaldiene for en budgetcyklus og en budgetmodel for én enkelt økonomisk dimensionsværdi eller budgetgruppe. | Viser de samlede budgetbeløb for flere økonomiske dimensionsværdier på samme tid. |
| Medtager data fra både bekræftede og ubekræftede behæftelser.                                                         | Medtager kun data fra bekræftede behæftelser.                                             |
| Medtager kun data fra udgiftskonti.                                                                               | Medtager data fra både indtægts- og udgiftskonti.                                       |

> [!NOTE] 
> Hvis du ønsker, at de tilgængelige eller resterende budgetbeløb skal medtage kladdeposteringer, skal du bruge siden **Statistik for budgetstyring**. Siden **Budgetanalyse** viser kun bogførte posteringer.

## <a name="can-i-export-the-budget-analysis-results-to-microsoft-excel"></a>Kan jeg eksportere budgetanalyseresultaterne til Microsoft Excel?
Ja, du kan eksportere resultaterne af budgetanalysen. På siden **Budgetanalyse** skal du trykke på Ctrl + Skift + E.

## <a name="how-do-i-display-information-for-a-specific-closing-period"></a>Hvordan får jeg vist oplysninger for en bestemt ultimoperiode?
Hvis du vil se saldi og oplysninger for en bestemt ultimoperiode, skal du bruge siden **Råbalance**. På siden **Råbalance** skelnes ikke mellem driftsperioder og ultimoperioder.

## <a name="can-i-analyze-the-budget-in-a-dimension-order-thats-different-from-the-expense-account-structure"></a>Kan jeg analysere budgettet i en dimensionsordre, der er forskellig fra udgiftskontostrukturen?
Ja. F.eks. ønsker du måske at få vist bestemte hovedkonti på tværs af programmer eller andre dimensioner? Du kan oprette økonomiske dimensionssæt, der afspejler den måde, du vil analysere dine data på. Du kan bruge siden **Økonomiske dimensionsopsætninger** i Finans. For at få vist hovedkonti på tværs af programmer kan du f.eks. oprette et programdimensionssæt og derefter tilføje dimensioner ved hjælp af **Hovedkonto**. Når du vender tilbage til siden **Budgetanalyse** og vælger det dimensionssæt, vises budgettet som en liste over hovedkonti. Du kan derefter analysere ned i en hovedkonto for at medtage programniveauet for dimensionssættet, som inddeler alle totaler efter program inden for denne hovedkonto.

## <a name="what-if-the-financial-dimension-set-that-i-want-to-use-isnt-included-on-the-page"></a>Hvad nu hvis det økonomiske dimensionssæt, jeg vil bruge, ikke er medtaget på siden?
Alle eksisterende økonomiske dimensionssæt vises på siden **Budgetanalyse**. Hvis du ikke kan se den, du ønsker, kan du oprette den i modulet Finans.

## <a name="what-is-the-carry-forwards-column-set-used-for"></a>Hvad bruges kolonnesættet Overførsler til?
Brug kolonnesættet **Udgiftsbudget med overførsler**, hvis du overfører budgettet for indkøbsordrer, der er åbne ved årsafslutningen. Dette kolonnesæt viser separate totaler både for posteringer, der bruger et aktivt budget for det forudgående år, og for posteringer, der bruger budgettet for det nye år. Dette gør det nemt for dig at overvåge de budgetterede, behæftede og forbrugte beløb, der er relateret til posteringer fra det foregående år.

## <a name="what-should-i-do-if-the-grids-are-empty-even-when-ive-selected-all-the-values"></a>Hvad skal jeg gøre, hvis gitrene er tomme, selvom jeg har valgt alle værdierne?
Hvis gitrene er tomme på siden **Budgetanalyse**, kan du prøve følgende handlinger for at løse problemet:

-   Klik på **Opdater totaler**, når du har indstillet værdierne øverst på siden.
-   Kontrollér, at den valgte dimensionsopsætning medtager den dimensionsværdi, du leder efter.
-   Kontrollér, at posteringslaget og datoerne er korrekte for de værdier, du søger efter.
-   Kontrollér, at posteringsdokumenter, som du leder efter, er bogført eller bekræftet. Siden **Budgetanalyse** viser kun bogførte posteringer.

## <a name="how-do-i-see-updated-numbers-in-the-columns-when-i-change-the-dimension-set-dates-posting-layers-and-other-settings"></a>Hvordan kan jeg se opdaterede tal i kolonnerne, når jeg ændrer dimensionssæt, datoer, posteringslag og andre indstillinger?
Når du har ændret indstillingerne øverst på siden, skal du klikke på **Opdater totaler** for at se resultaterne af din forespørgsel.

## <a name="feature-budget-control-statistics-date-range-enhancements"></a>Funktion: Udvidelser af datointerval for statistik for budgetstyring
Denne funktion giver en ny visning, så der kun vises faktiske beløb i det datointerval, der vises i forespørgslerne til **Statistik for budgetstyring**. Denne funktion er som standard slået til i 2022 udgivelsesbølge 2. 



[!INCLUDE[footer-include](../../includes/footer-banner.md)]
