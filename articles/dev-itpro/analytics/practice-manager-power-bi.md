---
title: Power BI-indhold for praksischef
description: "I dette emne beskrives, hvad der er medtaget i Power BI-indhold til praksischef. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdet, og indeholder oplysninger om den datamodel og de enheder, der bliver brugt til at oprette indholdet."
author: KimANelson
manager: AnnBe
ms.date: 12/18/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
ms.search.form: ProjManagementWorkspace
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: aac6439bb54b3b9cab066b06c01763e880efef8e
ms.openlocfilehash: 44f017fc3460b83b730f2f7c909c6b88480dd918
ms.contentlocale: da-dk
ms.lasthandoff: 12/18/2017

---

# <a name="practice-manager-power-bi-content"></a>Power BI-indhold for praksischef

[!include[banner](../includes/banner.md)]

I dette emne beskrives, hvad der er medtaget i Microsoft Power BI-indholdet til **praksischef**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **praksischef** blev oprettet til praksischefer og projektledere. Det indeholder vigtige nøgleværdier, der er relateret til de projekter, som organisationen arbejder på. Dashboardet giver et overblik over projekterne og de relaterede kunder. Et rapportniveaufilter kan bruges til at rapportere for bestemte juridiske enheder. Dette Power BI-indhold trækker data fra projektregnskabets samlede målinger.

Power BI-indholdet til **Praksischef** indeholder fem rapportsider: en oversigtsside og fire sider, der giver oplysninger om projektomkostninger, omsætning, administration af optjent værdi og timenøgletal, der er opdelt på tværs af forskellige dimensioner.

Alle beløb i indholdet vises i systemvalutaen. Du kan angive systemvalutaen på siden **Systemparametre**.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold

Power BI-indholdet **Praksischef** vises i arbejdsområdet **Projektstyring**.


## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet

Følgende tabel indeholder oplysninger om de nøgletal, der findes på de enkelte rapportsider i Power BI-indholdet til **praksischef**.

| Rapportside       | Metrik |
|-------------------|---------|
| Projektoversigt | <ul><li>Oprettede projekter</li><li>Estimerede projekter</li><li>Igangværende projekter</li><li>Faktisk omsætning efter kunde</li><li>Budgetteret bruttoavance efter projekt</li><li>Oversigt over administration af optjent værdi</li></ul> |
| Kost              | <ul><li>Faktiske vs. budgetterede omkostninger efter måned</li><li>Faktiske vs. budgetterede omkostninger efter år</li><li>Faktiske vs. budgetterede omkostninger efter kategori</li><li>Faktisk omkostninger efter posteringstype</li></ul> |
| Indtægter           | <ul><li>Faktisk omsætning efter måned</li><li>Faktisk omsætning efter postnummer</li><li>Faktisk vs. budgetteret omsætning efter kategori</li><li>Faktisk omsætning efter kundebranche</li></ul> |
| EVM               | Indeks for overholdelse af omkostninger og tidsplaner efter projekt |
| Timer             | <ul><li>Faktiske fakturerbare udnyttede timer vs faktiske fakturerbare byrdetimer vs budgetterede timer</li><li>Faktiske fakturerbare udnyttede timer vs faktiske fakturerbare byrdetimer efter projekt</li><li>Faktiske fakturerbare udnyttede timer vs faktiske fakturerbare byrdetimer efter ressource</li><li>Faktisk udnyttelsesgrad af fakturerbare timer efter projekt</li><li>Faktisk udnyttelsesgrad af fakturerbare timer efter ressource</li></ul> |

Diagrammer og felter i alle disse rapporter kan filtreres og fastgøres til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Du kan også bruge funktionen Eksporter underliggende data til at eksportere de underliggende data, der opsummeres i en visuel effekt.

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

Følgende data bruges til at udfylde rapportsiderne i Power BI-indholdet til **Praksischef**. Disse data repræsenteres som samlede målinger, der er klargjort i enhedslageret. Enhedslageret er en Microsoft SQL Server-database, der er optimeret til analyser. Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md).

I de følgende afsnit beskrives de samlede målinger, der bruges i de enkelte enheder.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Enhed: ProjectAccountingCube\_ActualHourUtilization
**Datakilde:** ProjEmplTrans

| Samlede nøglemålinger      | Felt                              | Betegnelse |
|--------------------------------|------------------------------------|-------------|
| Faktiske fakturerbare udnyttede timer | Sum(ActualUtilizationBillableRate) | Summen af faktiske fakturerbare udnyttede timer. |
| Faktiske fakturerbare byrdetimer   | Sum(ActualBurdenBillableRate)      | Summen af den faktiske byrdeudnyttelsesgrad. |

### <a name="entity-projectaccountingcubeactuals"></a>Enhed: ProjectAccountingCube\_Actuals
**Datakilde:** ProjTransPosting

| Samlede nøglemålinger | Felt              | Betegnelse |
|---------------------------|--------------------|-------------|
| Faktisk omsætning            | Sum(ActualRevenue) | Summen af bogført omsætning for alle posteringer. |
| Faktisk omkostning               | Sum(ActualCost)    | Summen af posterede omkostninger for alle posteringstyper. |

### <a name="entity-projectaccountingcubecustomer"></a>Enhed: ProjectAccountingCube\_Customer
**Datakilde:** CustTable

| Samlede nøglemålinger | Felt                                             | Betegnelse |
|---------------------------|---------------------------------------------------|-------------|
| Antal projekter        | COUNTA(ProjectAccountingCube\_Projects[PROJECTS]) | Antal tilgængelige projekter. |


### <a name="entity-projectaccountingcubeforecasts"></a>Enhed: ProjectAccountingCube\_Forecasts
**Datakilde:** ProjTransBudget

| Samlede nøglemålinger | Felt                  | Betegnelse |
|---------------------------|------------------------|-------------|
| Budgetterede omkostninger               | Sum(BudgetCost)        | Summen af budgetomkostninger for alle posteringstyper. |
| Budgetteret omsætning            | Sum(BudgetRevenue)     | Summen af budgetteret periodiseret/faktureret omsætning. |
| Budgetteret bruttomargen       | Sum(BudgetGrossMargin) | Forskellen mellem summen af den samlede budgetterede omsætning og summen af de samlede budgetterede omkostninger. |

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Enhed: ProjectAccountingCube\_ProjectPlanCostsView
**Datakilde:** Projekt

| Samlede nøglemålinger | Felt                    | Betegnelse |
|---------------------------|--------------------------|-------------|
| Planlagt omkostning              | Sum(SumOfTotalCostPrice) | Summen af kostpris i estimater for alle projektposteringstyper, der har planlagte opgaver. |

### <a name="entity-projectaccountingcubeprojects"></a>Enhed: ProjectAccountingCube\_Projects
**Datakilde:** Projekt

| Samlede nøglemålinger    | Felt | Betegnelse |
|------------------------------|-------|-------------|
| Omkostningsperformanceindeks       | ProjectAccountingCube\_Projects[Optjent værdi] ÷ ProjectAccountingCube\_Projects[Samlede faktiske omkostninger for fuldførte opgaver] | Beregningen af den samlede optjente værdi divideret med de samlede faktiske omkostninger. |
| Tidsplansperformanceindeks   | ProjectAccountingCube\_Projects[Optjent værdi] ÷ ProjectAccountingCube\_Projects[Samlede, planlagte omkostninger for fuldførte opgaver] | Beregningen af den samlede optjente værdi divideret med de samlede planlagte omkostninger. |
| Procentdel af fuldført arbejde | Procentdelen af udført arbejde = ProjectAccountingCube\_Projects[samlede faktiske kostbeløb for de fuldførte opgaver] ÷ (ProjectAccountingCube\_Projects[samlede faktiske omkostninger for fuldførte opgaver] + ProjectAccountingCube\_Projects[Samlede, planlagte omkostninger for projekt] – ProjectAccountingCube\_Projects[Samlede, planlagte omkostninger for fuldførte opgaver]) | Den totale procentdel af fuldført arbejde baseret på de samlede faktiske omkostninger for fuldførte opgaver og de planlagte omkostninger for projektet. |
| Faktisk udnyttelsesgrad af fakturerbare timer  | ProjectAccountingCube\_Projects[projektets samlede faktiske fakturerbare udnyttede timer] ÷ (ProjectAccountingCube\_Projects[projektets samlede faktiske fakturerbare udnyttede timer] + ProjectAccountingCube\_Projects[projektets samlede faktiske fakturerbare byrdetimer]) | Det samlede antal faktiske fakturerbare timer baseret på de udnyttede timer og byrdetimerne. |
| Optjent værdi                 | ProjectAccountingCube\_Projects[projektets totale planlagte omkostning] × ProjectAccountingCube\_Projects[procentdelen af fuldført arbejde] | De samlede planlagte omkostninger ganget med procentdelen af fuldført arbejde. |

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Enhed: ProjectAccountingCube\_TotalEstimatedCosts 
**Datakilde:** ProjTable

| Samlede nøglemålinger       | Felt               | Betegnelse |
|---------------------------------|---------------------|-------------|
| Planlagt omkostning for fuldført aktivitet | Sum(TotalCostPrice) | Summen af kostpris i estimater for alle projektposteringstyper, der har fuldførte opgaver. |

