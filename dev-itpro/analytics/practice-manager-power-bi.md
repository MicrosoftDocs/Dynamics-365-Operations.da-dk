---
title: Power BI-indhold for praksischef
description: "I dette emne beskrives, hvad der er medtaget i Power BI-indhold til praksischef. Det beskrives, hvordan du får adgang til rapporter, der er inkluderet i indholdspakken, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken."
author: knelson
manager: AnnBe
ms.date: 04/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Developer/IT Pro
ms.assetid: 
ms.search.region: Global
ms.author: knelson
ms.dyn365.intro: 2017/04/27
ms.dyn365.version: 
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 0f2a1a9df8e5036c60b74b8a710e606b0b1e312a
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="practice-manager-power-bi-content"></a>Power BI-indhold for praksischef

[!include[banner](../includes/banner.md)]


I dette emne beskrives, hvad der er medtaget i Microsoft Power BI-indholdet til **praksischef**. Det beskrives, hvordan du får adgang til Power BI-rapporter, og der er oplysninger om den datamodel og de enheder, der er brugt til at oprette indholdspakken.

## <a name="overview"></a>Overblik

Power BI-indholdet til **praksischef** blev oprettet til praksischefer og projektledere. Det indeholder vigtige nøgleværdier, der er relateret til de projekter, som organisationen arbejder på. Dashboardet giver et overblik over projekterne og de relaterede kunder. Et rapportniveaufilter kan bruges til at rapportere for bestemte juridiske enheder. Power BI-indholdet trækker data fra projektregnskabets samlede målinger til Microsoft Dynamics 365 for Operations.

Power BI-indholdet til **praksischef** indeholder fem rapportsider: en oversigtsside og fire sider, der giver oplysninger om projektomkostninger, omsætning, administration af optjent værdi og timenøgletal, der er opdelt på tværs af forskellige dimensioner.

Alle beløb i indholdet vises i systemvalutaen. Du kan angive systemvalutaen på siden **Systemparametre**.

## <a name="accessing-the-power-bi-content"></a>Adgang til Power BI-indhold

Du kan finde Power Bi-indholdet til **Praksischef** i biblioteket Delte aktiver i Microsoft Dynamics Lifecycle Services (LCS). Du kan finde flere oplysninger om, hvordan du henter indholdspakken og forbinder den med dine Microsoft Dynamics-365 for Operations-data, under [Power BI-indhold i LCS fra Microsoft og dine partnere](power-bi-content-microsoft-partners.md).

Hvis du vil se en demo, der viser, hvordan du implementerer Power BI-indholdet, kan du se dette Office Mix [Power BI-indhold fra Microsoft og dine partnere i Dynamics Lifecycle Services](https://mix.office.com/watch/9puyb1b2xs1w).

## <a name="reports-that-are-included-in-the-power-bi-content"></a>Rapporter, der er inkluderet i Power BI-indholdet

Følgende tabel indeholder oplysninger om de nøgletal, der findes på de enkelte rapportsider i Power BI-indholdet til **praksischef**.

| Rapportside                                          | Metrik               |
|------------------------------------------------------|-----------------------------------------------|
| Dashboard  | Oprettede projekter<br>Estimerede projekter<br>Igangværende projekter<br>Antal projekter efter stadie<br>Antal projekter efter by<br>Faktisk omsætning efter kunde<br>Budgetteret bruttoavance efter projekt<br>Oversigt over administration af optjent værdi |
| Kost                                                 | Faktiske vs. budgetterede omkostninger efter måned<br>Faktiske vs. budgetterede omkostninger efter år<br>Faktiske vs. budgetterede omkostninger efter kategori<br>Faktisk omkostninger efter posteringstype       |
| Indtægter                                              | Faktisk omsætning efter måned<br>Faktisk omsætning efter postnummer<br>Faktisk vs. budgetteret omsætning efter kategori<br>Faktisk omsætning efter kundebranche        |
| EVM                                                  | Indeks for overholdelse af omkostninger og tidsplaner efter projekt                 |
| Timer                                                | Faktiske fakturerbare udnyttede timer vs faktiske fakturerbare byrdetimer vs budgetterede timer<br>Faktiske fakturerbare udnyttede timer vs faktiske fakturerbare byrdetimer efter projekt<br>Faktiske fakturerbare udnyttede timer vs faktiske fakturerbare byrdetimer efter ressource<br>Faktisk udnyttelsesgrad af fakturerbare timer efter projekt<br>Faktisk udnyttelsesgrad af fakturerbare timer efter ressource |

Diagrammer og felter i alle disse rapporter kan filtreres og fastgøres til dashboardet. Du kan finde flere oplysninger om filtrering og fastgørelse i Power BI under [Oprette og konfigurere et dashboard](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-4-2-create-configure-dashboards/). Du kan også bruge funktionen Eksporter underliggende data til at eksportere de underliggende data, der opsummeres i en visuel effekt.

## <a name="understanding-the-data-model-and-entities"></a>Forståelse af datamodellen og enheder

Dynamics 365 for Operations-data bruges til at udfylde rapportsiderne i Power BI-indholdet til **praksischef**. Disse data repræsenteres som samlede målinger, der gemmes midlertidigt i enhedslageret, som er en Microsoft SQL-database, der er optimeret til analyse. Du kan finde flere oplysninger under [Oversigt over Power BI-integration med enhedslager](power-bi-integration-entity-store.md).

I de følgende afsnit beskrives de samlede målinger, der bruges i de enkelte enheder.

### <a name="entity-projectaccountingcubeactualhourutilization"></a>Enhed: ProjectAccountingCube_ActualHourUtilization
**Datakilde**: ProjEmplTrans

| Samlede nøglemålinger                | Felt                                | Betegnelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualBillableUtilizedHours              | Sum(ActualUtilizationBillableRate)   | Summen af faktiske fakturerbare udnyttede timer |
| ActualBillableBurdenHours                | Sum(ActualBurdenBillableRate)        | Summen af faktisk byrdeudnyttelsesgrad             |

### <a name="entity-projectaccountingcubeactuals"></a>Enhed: ProjectAccountingCube_Actuals
**Datakilde**: ProjTransPosting

| Samlede nøglemålinger                | Felt                                | Betegnelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| ActualRevenue                            |     Sum(ActualRevenue)               |  Summen af bogført omsætning for alle posteringer |   
| ActualCost   |                             Sum(ActualCost)           |    Summen af posterede omkostninger for alle posteringstyper    |

### <a name="entity-projectaccountingcubecustomer"></a>Enhed: ProjectAccountingCube_Customer
**Datakilde**: CustTable

| Samlede nøglemålinger                | Felt                                | Betegnelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    Antal projekter        |   COUNTA(ProjectAccountingCube_Projects[PROJECTS])       |         Antal tilgængelige projekter    |


### <a name="entity-projectaccountingcubeforecasts"></a>Enhed: ProjectAccountingCube_Forecasts
**Datakilde**: ProjTransBudget

| Samlede nøglemålinger                | Felt                                | Betegnelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|    BudgetCost    |       Sum(BudgetCost)  |       Summen af budgetterede omkostninger for alle posteringstyper     |
|     BudgetRevenue    |         Sum(BudgetRevenue)    |    Summen af budgetteret periodiseret/faktureret omsætning         |
|BudgetGrossMargin | Sum(BudgetGrossMargin) |Forskellen mellem summen af den samlede budgetterede omsætning og summen af de samlede budgetterede omkostninger

### <a name="entity-projectaccountingcubeprojectplancostsview"></a>Enhed: ProjectAccountingCube_ProjectPlanCostsView
**Datakilde**: Projekt

| Samlede nøglemålinger                | Felt                                | Betegnelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|      PlannedCost      |        Sum(SumOfTotalCostPrice)   | Total kostpris i estimater for alle projektposteringstyper med planlagte opgaver |

### <a name="entity-projectaccountingcubeprojects"></a>Enhed: ProjectAccountingCube_Projects
**Datakilde**: Projekt

| Samlede nøglemålinger                | Felt                                | Betegnelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
|   Omkostningsperformanceindeks  |ProjectAccountingCube_Projects[optjent værdi] / ProjectAccountingCube_Projects [faktiske omkostninger i alt for fuldførte opgaver] |     Beregningen af den samlede optjente værdi divideret med de samlede faktiske omkostninger|
|  Tidsplansperformanceindeks |ProjectAccountingCube_Projects[optjent værdi] / ProjectAccountingCube_Projects [planlagte omkostninger i alt for fuldførte opgaver]|Beregningen af den samlede optjente værdi divideret med de samlede planlagte omkostninger |
|Procentdel af fuldført arbejde |Procentdelen af udført arbejde = ProjectAccountingCube_Projects[samlede faktiske kostbeløb for de fuldførte opgaver] / (ProjectAccountingCube_Projects[samlede faktiske kostbeløb for de fuldførte opgaver] + ProjectAccountingCube_Projects[samlede, planlagte omkostninger for projekt] - ProjectAccountingCube_Projects[samlede, planlagte omkostninger for de fuldførte opgaver])|Den totale procentdel af fuldført arbejde baseret på de samlede faktiske omkostninger for fuldført opgave og de planlagte omkostninger for projektet|
|Projektets faktiske udnyttelsesgrad af fakturerbare timer|ProjectAccountingCube_Projects[projektets samlede faktiske fakturerbare udnyttede timer] / (ProjectAccountingCube_Projects[projektets samlede faktiske fakturerbare udnyttede timer] + ProjectAccountingCube_Projects[projektets samlede faktiske fakturerbare byrdetimer])|Samlede faktiske fakturerbare timer baseret på udnyttet + byrde|
|Optjent værdi|ProjectAccountingCube_Projects[projektets totale planlagte omkostning] * ProjectAccountingCube_Projects [procentdelen af fuldført arbejde]|Samlede planlagte omkostninger ganget med procentdelen af fuldført arbejde|

### <a name="entity-projectaccountingcubetotalestimatedcosts"></a>Enhed: ProjectAccountingCube_TotalEstimatedCosts 
**Datakilde**: ProjTable

| Samlede nøglemålinger                | Felt                                | Betegnelse                            | 
|------------------------------------------|--------------------------------------|----------------------------------------|
| CompletedActivityPlannedCost  |  Sum(TotalCostPrice)  |   Total kostpris i estimater for alle projektposteringstyper med fuldførte opgaver|

## <a name="additional-resources"></a>Yderligere ressourcer

Her er nogle nyttige links, der er knyttet til enheder og oprettelse af Power BI-indhold:

- [Dataenheder](/dynamics365/operations/dev-itpro/data-entities/data-entities)
- [Oprettelse af organisatoriske indholdspakker](https://powerbi.microsoft.com/en-us/documentation/powerbi-service-organizational-content-packs-introduction/)
- [Datamodellering i Power BI](https://powerbi.microsoft.com/en-us/guided-learning/powerbi-learning-2-1-intro-modeling-data)
- [Konfigurer Power BI-integration til arbejdsområder](configure-power-bi-integration.md)

