---
title: "Budgetplanlægningsskabeloner til Excel"
description: Dette emne beskriver, hvordan du opretter en Microsoft Excel-skabeloner, der kan bruges sammen med budgetplaner.
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 261794
ms.assetid: 1d8e99c1-b70d-41ba-991e-ab50b16797e0
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: eb32cf1b96dfef75131b8c7541e20a93615a87f7
ms.openlocfilehash: 0e2eb6e7c130f03edbf60a185d397d94b5d61d7d
ms.lasthandoff: 03/31/2017


---

# <a name="budget-planning-templates-for-excel"></a>Budgetplanlægningsskabeloner til Excel

Dette emne beskriver, hvordan du opretter en Microsoft Excel-skabeloner, der kan bruges sammen med budgetplaner.

Dette emne viser, hvordan du opretter Excel-skabeloner, der skal bruges med budgetplaner ved hjælp af standard demo-datasæt og Admin bruger-login. Finde flere oplysninger om budgetplanlægning, [oversigt i budgetplanlægningen.](budget-planning-overview-configuration.md) Du kan også følge den [budgetplanlægning 101](budget-plan.md) selvstudium for at lære grundlæggende modul konfiguration og brug principper.

## <a name="generate-a-worksheet-using-budget-plan-document-layout"></a>Opret et regneark med budget plan dokumentlayout
Budget plan dokumenter kan ses og redigeres ved hjælp af et eller flere layout. Hvert layout kan have en tilknyttet budget plan dokumentskabelon for at få vist og rediger budget plandata i et Excel-regneark. I dette emne vil blive genereret en dokumentskabelon for budget plan, ved hjælp af en eksisterende konfiguration layout. Åbn den **budgetplaner liste** (**budgettering**&gt;**budgetplaner**). Klik på **ny** til at oprette et nyt budget plan dokument. [![bpt1](./media/bpt11-1024x552.png)](./media/bpt11.png) 

Brug af **Tilføj** linje mulighed for at tilføje linjer. Klik på **layout** til at få vist konfigurationen af budget plan dokument layout. 
[![bpt2](./media/bpt2-1024x274.png)](./media/bpt2.png) 

Du kan gennemgå konfigurationen af layout og juster den efter behov. Gå til **skabelon**&gt;**Generer** til at oprette en Excel-fil for dette layout. Når skabelonen er oprettet, kan du gå til **skabelon**&gt;**se** til at åbne og gennemse skabelonen budget plan. Du kan gemme Excel-filen til den lokale harddisk. [![bpt3](./media/bpt3-1024x545.png)](./media/bpt3.png) 

> [!NOTE] 
> Budget plan dokumentets layout kan ikke redigeres, når en Excel-skabelon, der er knyttet til den. Hvis du vil ændre layoutet, slette den tilknyttede Excel skabelonfil og genoprette den. Dette er påkrævet for at holde felterne i layoutet, og regnearket er synkroniseret. 

Excel-skabelon indeholder alle elementerne fra budget plan dokumentets layout, hvor den **findes i regnearket** kolonne er indstillet til True. Overlappende elementer er ikke tilladt i Excel-skabelonen. For eksempel hvis layout indeholder anmodning Q1, anmodning Q2, anmodning Q3 og Q4 anmodning kolonner og en kolonne med samlede anmodning, der repræsenterer summen af alle 4 kvartalsvise kolonner, er den kvartalsvise kolonner eller samlede kolonne tilgængelig og kan bruges i Excel-skabelonen. Excel-filen kan ikke opdatere overlappende kolonner under opdateringen, fordi dataene i tabellen bliver forældet og upræcis.

[![bpt4](./media/bpt4-1024x615.png)](./media/bpt4.png)

> [!NOTE] 
> For at undgå potentielle problemer med visning og redigering af budgetplandata ved hjælp af Excel, skal den samme bruger logføres i begge Dynamics 365 for operationer og datatilslutning tilføjelsesprogrammet Microsoft Dynamics-kontor.

## <a name="add-a-header-to-budget-plan-document-template"></a>Tilføje et sidehoved til budget plan dokumentskabelon
Hvis du vil tilføje sidehovedoplysninger, Vælg den øverste række i Excel-filen og indsætte tomme rækker. Klik på **Design** i den **datatilslutning** til at tilføje felter i sidehovedet til Excel-filen.

[![bpt5](./media/bpt5-1024x615.png)](./media/bpt5.png) 

I den **Design** under fanen ** ** Klik **Tilføj** felter, og vælg derefter **BudgetPlanHeader** som datakilde enhed.

[![bpt6](./media/bpt6-1024x615.png)](./media/bpt6.png)

Punkt markøren til den ønskede placering i Excel-filen. Klik på **Tilføj etiket** at tilføje feltetiketten til den valgte placering. Vælg **Tilføj værdi** til at føje værdifeltet til det valgte sted. Klik på **gjort** at lukke designeren.

## <a name="bpt7mediabpt7pngmediabpt7png"></a>[![bpt7](./media/bpt7.png)](./media/bpt7.png)

<a name="add-a-calculated-column-to-budget-plan-document-template-table"></a>Føje en beregnet kolonne til budget plan skabelon dokumenttabellen
--------------------------------------------------------------

Næste, beregnede kolonner føjes til genererede budget plan dokumentskabelon. A **samlede anmodning** kolonne, som opsummerer anmodningen Q1: anmodning K4 kolonner, og en **regulering** kolonne, der beregner den **samlede anmodning** kolonne med en foruddefineret faktor.

Klik på **Design** i den **datatilslutning** til at føje kolonner til tabellen. Klik på **Rediger** ud for **BudgetPlanWorksheet** datakilde for at begynde at tilføje kolonner.

[![bpt8](./media/bpt8-1024x301.png)](./media/bpt8.png) 

Markeret feltgruppe viser de kolonner, der er tilgængelige i skabelonen. Klik på **formel** til at tilføje en ny kolonne. Navngive den nye kolonne og derefter indsætte formlen i den **formel** felt. Klik på **opdatering** til at indsætte kolonnen.

[![bpt12](./media/bpt12-1024x565.png)](./media/bpt12.png)

> [!NOTE] 
> For at definere formlen skal oprette formlen i regnearket og derefter kopiere det til den **Design** vindue. En Dynamics 365 for operationer bundet-tabel, typisk navngives "AXTable1". For at opsummere anmode om Q1: anmode om Q4 kolonner i regnearket, formlen = AxTable1\[anmodning Q1\]+ AxTable1\[anmodning Q2\]+ AxTable1\[anmode om Q3\]+ AxTable1\[anmode om Q4\].

Gentag disse trin for at indsætte de **justering af** kolonne. Brug formlen = AxTable1\[samlede anmodning\]\*$I$ 1 for denne kolonne. Dette vil tage værdien i celle I1 og multiplicere værdierne i de **samlede anmodning** kolonne til beregning af reguleringsbeløb.

Gem og luk Excel-filen. Gå tilbage til Dynamics 365 for operationer og i **layout**, skal du klikke på **skabelon &gt;overføre** til at overføre den gemte Excel-skabelon, der skal bruges til budgetplanen. 

[![bpt10](./media/bpt10-1024x352.png)](./media/bpt10.png) 

Luk den **layout** skyderen. I **budgetplan** dokument, skal du klikke på **regneark** til at få vist og Rediger dokument i Microsoft Excel. Bemærk, at den justerede Excel-skabelon, der blev brugt til at oprette denne Budgetplansregnearket og beregnede kolonner er opdateret ved hjælp af formler, der er defineret i de forrige trin. 

[![bpt11](./media/bpt111-1024x431.png)](./media/bpt111.png)

## <a name="tips--tricks-for-creating-budget-plan-templates"></a>Tips og tricks til at oprette skabeloner for budgetplan
### <a name="can-i-add-and-use-additional-data-sources-to-a-budget-plan-template"></a>Kan jeg tilføje og bruge flere datakilder til en budgetplansskabelon?

Ja, du kan bruge den **Design** menuen for at tilføje yderligere enheder til den samme eller andre regneark i Excel-skabelonen. For eksempel kan du tilføje de **BudgetPlanProposedProject** -datakilde til at oprette og vedligeholde en liste over foreslåede projekter på samme tid, når arbejdet med budgettet planlægger data i Excel. Bemærk, at herunder store datakilder kan påvirke ydeevnen af Excel-projektmappen. 

Du kan bruge den **Filter** indstilling i den **datatilslutning** at føje ønskede filtre til flere datakilder.

### <a name="can-i-hide-the-design-option-in-the-data-connector-for-other-users"></a>Kan jeg skjule designindstillinger i datatilslutning for andre brugere?

Ja, åbne den **datatilslutning** indstillinger for at skjule den **Design** indstilling fra andre brugere.

[![bpt13](./media/bpt13-1024x565.png)](./media/bpt13.png)

Udvid **dataindstillinger** og fjerne markeringen i de **aktivere design** afkrydsningsfelt. Derved skjules det **Design** indstilling fra den **datatilslutning**.

[![bpt14](./media/bpt14-1024x592.png)](./media/bpt14.png)

### <a name="can-i-prevent-users-from-accidently-closing-the-data-connector-while-working-with-data"></a>Er det muligt at forhindre brugere i ved et uheld lukker forbindelsen Data mens du arbejder med data?

Vi anbefaler, at låse skabelonen for at forhindre brugere i at lukke den. Hvis du vil aktivere låsen, skal du klikke på den **datatilslutning**, vises med en pil i øverste højre hjørne. 

[![bpt15](./media/bpt15-1024x285.png)](./media/bpt15.png) 

Klik på pilen for at få en ekstra menu. Vælg **Lås**.

### <a name="bpt16mediabpt16-1024x614pngmediabpt16png"></a>[![bpt16](./media/bpt16-1024x614.png)](./media/bpt16.png)

### <a name="can-i-use-other-excel-features-like-cell-formatting-colors-conditional-formatting-and-charts-with-my-budget-plan-templates"></a>Er det muligt at bruge andre Microsoft Excel-funktioner, som celleformatering, farver, betinget formatering og diagrammer med Mine skabeloner for budgetplan?

Ja, fungerer de fleste af de almindelige Excel-funktioner i skabeloner for budgetplan. Det anbefales, at bruge farvekodning for brugere for at skelne mellem kolonnerne skrivebeskyttet og kan redigeres. Betinget formatering kan bruges til at fremhæve problematiske områder af budgettet. Kolonnetotaler kan let vises ved hjælp af standard Excel-formler oven over tabellen.

Du kan også oprette og bruge pivottabeller og -diagrammer til supplerende grupperinger og visualiseringer af budgetdata. På den **Data** under fanen den **forbindelser** skal du klikke på **Opdater alle**, og klik derefter på **egenskaber for forbindelse**. Klik på den **Brug** tab. Under **Opdater**, skal du vælge den **Opdater data, når du åbner filen** afkrydsningsfelt. 

[![bpt17](./media/bpt17-1024x614.png)](./media/bpt17.png)


