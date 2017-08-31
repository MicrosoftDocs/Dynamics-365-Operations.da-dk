---
title: Power BI-indhold for praksischef
description: "I dette emne beskrives, hvad der er medtaget i Power BI-indhold til praksischef. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der bliver brugt til at oprette indholdet."
author: KimANelson
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations, UnifiedOperations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: Human Translation
ms.sourcegitcommit: 993e88703f19dbeec435d07a4599cbbfcda563bc
ms.openlocfilehash: b63e31f3e4993c1fda229a54b4e5ef2fed824355
ms.contentlocale: da-dk
ms.lasthandoff: 06/20/2017

---

# <a name="practice-manager-power-bi-content"></a>Power BI-indhold for praksischef

[!include[banner](../includes/banner.md)]

I dette emne beskrives, hvad der er medtaget i Microsoft Power BI-indholdet til **praksischef**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **praksischef** blev oprettet til praksischefer og projektledere. Det indeholder vigtige nøgleværdier, der er relateret til de projekter, som organisationen arbejder på. Dashboardet giver et overblik over projekterne og de relaterede kunder. Et rapportniveaufilter kan bruges til at rapportere for bestemte juridiske enheder. Dette Power BI-indhold trækker data fra projektregnskabets samlede målinger.

Power BI-indholdet til **Praksischef** indeholder fem rapportsider: en oversigtsside og fire sider, der giver oplysninger om projektomkostninger, omsætning, administration af optjent værdi og timenøgletal, der er opdelt på tværs af forskellige dimensioner.

Alle beløb i indholdet vises i systemvalutaen. Du kan angive systemvalutaen på siden **Systemparametre**.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold
Hvis du bruger opdateringen til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition fra juli 2017, vises Power BI-indholdet til **Praksischef** i arbejdsområdet **Projektstyring**.

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet

Følgende tabel indeholder oplysninger om de nøgletal, der findes på de enkelte rapportsider i Power BI-indholdet til **praksischef**.

| Rapportside       | Metrik |
|-------------------|---------|
| Projektoversigt | <ul><li>Oprettede projekter</li><li>Estimerede projekter</li><li>Igangværende projekter</li><li>Antal projekter efter stadie</li><li>Antal projekter efter by</li><li>Faktisk omsætning efter kunde</li><li>Budgetteret bruttoavance efter projekt</li><li>Oversigt over administration af optjent værdi</li></ul> |
| Kost              | <ul><li>Faktiske vs. budgetterede omkostninger efter måned</li><li>Faktiske vs. budgetterede omkostninger efter år</li><li>Faktiske vs. budgetterede omkostninger efter kategori</li><li>Faktisk omkostninger efter posteringstype</li></ul> |
| Indtægter           | <ul><li>Faktisk omsætning efter måned</li><li>Faktisk omsætning efter postnummer</li><li>Faktisk vs. budgetteret omsætning efter kategori</li><li>Faktisk omsætning efter kundebranche</li></ul> |
| EVM               | Indeks for overholdelse af omkostninger og tidsplaner efter projekt |
| Timer             | <ul><li>Faktiske fakturerbare udnyttede timer vs faktiske fakturerbare byrdetimer vs budgetterede timer</li><li>Faktiske fakturerbare udnyttede timer vs faktiske fakturerbare byrdetimer efter projekt</li><li>Faktiske fakturerbare udnyttede timer vs faktiske fakturerbare byrdetimer efter ressource</li><li>Faktisk udnyttelsesgrad af fakturerbare timer efter projekt</li><li>Faktisk udnyttelsesgrad af fakturerbare timer efter ressource</li></ul> |

Diagrammer og felter i alle disse rapporter kan filtreres og fastgøres til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Du kan også bruge funktionen Eksporter underliggende data til at eksportere de underliggende data, der opsummeres i en visuel effekt.

## <a name="extending-the-power-bi-content"></a>Udvidelse af Power BI-indhold
Når du bruger de indholdspakker, der er tilgængelige i Microsoft Dynamics Lifecycle Services (LCS), kan du levere fremragende analyser til personer, der ikke logger på Microsoft Dynamics 365. Du kan redigere disse indholdspakker, så de omfatter andre rapporter eller grafik, og derefter udgive dem på din Power BI.com-lejer med henblik på analyse. 

Du kan finde Power BI-indhold til **Praksischef** i biblioteket med delte aktiver i LCS. Du kan finde flere oplysninger om, hvordan du downloader indhold og implementerer det i din organisation, under [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md). Hvis du vil se en demo, der viser, hvordan du implementerer Power BI-indholdet, kan du se dette Office Mix [Power BI-indhold fra Microsoft og dine partnere i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

Sørg for at downloade **Praksischef**-indhold, der gælder for den version af Dynamics 365, du bruger.

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

Følgende data bruges til at udfylde rapportsiderne i Power BI-indholdet til **Praksischef**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md).

I de følgende afsnit beskrives de samlede målinger, der bruges i de enkelte enheder.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Enhed: ProjectAccountingCube_ActualHourUtilization
**Datakilde:** ProjEmplTrans

| Samlede nøglemålinger      | Felt                              | Betegnelse | 
|--------------------------------|------------------------------------|-------------|
| Faktiske fakturerbare udnyttede timer | Sum(ActualUtilizationBillableRate) | Summen af faktiske fakturerbare udnyttede timer. |
| Faktiske fakturerbare byrdetimer   | Sum(ActualBurdenBillableRate)      | Summen af den faktiske byrdeudnyttelsesgrad. |

### <a name="entity-projectaccountingcubeactuals"></a>Enhed: ProjectAccountingCube_Actuals
**Datakilde:** ProjTransPosting

| Samlede nøglemålinger | Felt              | Betegnelse | 
|---------------------------|--------------------|-------------|
| Faktisk omsætning            | Sum(ActualRevenue) | Summen af bogført omsætning for alle posteringer. |   
| Faktisk omkostning               | Sum(ActualCost)    | Summen af posterede omkostninger for alle posteringstyper. |

### <a name="entity-projectaccountingcubecustomer"></a>Enhed: ProjectAccountingCube_Customer
**Datakilde:** CustTable

| Samlede nøglemålinger | Felt                                            | Betegnelse | 
|---------------------------|--------------------------------------------------|-------------|
| Antal projekter        | COUNTA(ProjectAccountingCube_Projects[PROJECTS]) | Antal tilgængelige projekter. |


### <a name="entity-projectaccountingcubeforecasts"></a>Enhed: ProjectAccountingCube_Forecasts
**Datakilde:** ProjTransBudget

| Samlede nøglemålinger | Felt                  | Betegnelse | 
|---------------------------|------------------------|-------------|
| Budgetterede omkostninger               | Sum(BudgetCost)        | Summen af budgetomkostninger for alle posteringstyper. |
| Budgetteret omsætning            | Sum(BudgetRevenue)     | Summen af budgetteret periodiseret/faktureret omsætning.  |
| Budgetteret bruttomargen       | Sum(BudgetGrossMargin) | Forskellen mellem summen af den samlede budgetterede omsætning og summen af de samlede budgetterede omkostninger. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Enhed: ProjectAccountingCube_ProjectPlanCostsView
**Datakilde:** Projekt

| Samlede nøglemålinger | Felt                    | Betegnelse | 
|---------------------------|--------------------------|-------------|
| Planlagt omkostning              | Sum(SumOfTotalCostPrice) | Summen af kostpris i estimater for alle projektposteringstyper, der har planlagte opgaver. |

### <a name="entity-projectaccountingcubeprojects"></a>Enhed: ProjectAccountingCube_Projects
**Datakilde:** Projekt

| Samlede nøglemålinger    | Felt | Betegnelse | 
|------------------------------|-------|-------------|
| Omkostningsperformanceindeks       | ProjectAccountingCube_Projects[optjent værdi] / ProjectAccountingCube_Projects [faktiske omkostninger i alt for fuldførte opgaver] | Beregningen af den samlede optjente værdi divideret med de samlede faktiske omkostninger. |
| Tidsplansperformanceindeks   | ProjectAccountingCube_Projects[optjent værdi] / ProjectAccountingCube_Projects [planlagte omkostninger i alt for fuldførte opgaver] | Beregningen af den samlede optjente værdi divideret med de samlede planlagte omkostninger. |
| Procentdel af fuldført arbejde | Procentdelen af udført arbejde = ProjectAccountingCube_Projects[samlede faktiske kostbeløb for de fuldførte opgaver] / (ProjectAccountingCube_Projects[samlede faktiske kostbeløb for de fuldførte opgaver] + ProjectAccountingCube_Projects[samlede, planlagte omkostninger for projekt] - ProjectAccountingCube_Projects[samlede, planlagte omkostninger for de fuldførte opgaver]) | Den totale procentdel af fuldført arbejde baseret på de samlede faktiske omkostninger for fuldførte opgaver og de planlagte omkostninger for projektet. |
| Faktisk udnyttelsesgrad af fakturerbare timer  | ProjectAccountingCube_Projects[projektets samlede faktiske fakturerbare udnyttede timer] / (ProjectAccountingCube_Projects[projektets samlede faktiske fakturerbare udnyttede timer] + ProjectAccountingCube_Projects[projektets samlede faktiske fakturerbare byrdetimer]) | Det samlede antal faktiske fakturerbare timer baseret på de udnyttede timer og byrdetimerne. |
| Optjent værdi                 | ProjectAccountingCube_Projects[projektets totale planlagte omkostning] * ProjectAccountingCube_Projects [procentdelen af fuldført arbejde] | De samlede planlagte omkostninger ganget med procentdelen af fuldført arbejde. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Enhed: ProjectAccountingCube_TotalEstimatedCosts 
**Datakilde:** ProjTable

| Samlede nøglemålinger       | Felt               | Betegnelse | 
|---------------------------------|---------------------|-------------|
| Planlagt omkostning for fuldført aktivitet | Sum(TotalCostPrice) | Summen af kostpris i estimater for alle projektposteringstyper, der har fuldførte opgaver. |

