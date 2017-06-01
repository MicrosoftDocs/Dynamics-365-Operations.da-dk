---
title: "Fordeling af budgetplanlægningsdata"
description: "I denne artikel beskrives de forskellige fordelingsmetoder, der er tilgængelige i Microsoft Dynamics 365 for Operations, og hvordan de kan bruges."
author: twheeloc
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: d421b161216d700f7819f1da8c0ca8ad089b5670
ms.openlocfilehash: 753b5c18d9b062ca4f799fd5690b4df3f7b71993
ms.contentlocale: da-dk
ms.lasthandoff: 05/25/2017


---

# <a name="budget-planning-data-allocation"></a>Fordeling af budgetplanlægningsdata

[!include[banner](../includes/banner.md)]


I denne artikel beskrives de forskellige fordelingsmetoder, der er tilgængelige i Microsoft Dynamics 365 for Operations, og hvordan de kan bruges.  

Du kan distribuere data i en budgetplan på en række forskellige måder at give et præcist billede af de forventede beløb.

## <a name="allocation-methods"></a>Fordelingsmetoder
Tre fordelingsmetoder (Fordel hen over perioder, Fordel på dimensioner og Brug finansfordelingsregler) kan oprette budgetplanlinjer, der er baseret på linjer i den samme budgetplan. Tre andre metoder (Aggregat, Fordel og Kopier fra budgetplanen) kan oprette budgetplanlinjer i andre budgetplaner. Du kan angive destinationsscenariet for alle seks fordelingsmetoder. Destinationsscenariet kan enten være det samme som kildescenariet eller forskelligt fra kildescenariet. Desuden kan du angive, om nye linjer er føjet til budgetplanen eller erstatter de aktuelle linjer i budgetplanen.

[![AllocateAcrossPeriods](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Fordel hen over perioder** – en periodefordelingskategori bruges til at fordele budgetplanlinjerne fra Kildebudgetplanscenariet på tværs af perioder i destinationsscenariet. Beløbet i kildedokumentet er tildelt flere linjer i destinationsscenariet, baseret på den procentdel og dato, der er defineret i periodefordelingskategorien.         

[![AllocateToDimensions](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Fordel på dimensioner** – Budgetplanlinjerne fordeles fra kildebudgetplanlægningsscenariet til en eller flere linjer i destinationsscenariet, baseret på procentsatserne og de økonomiske dimensioner, der er defineret i den valgte budgetfordelingsbetingelse.           

![AggregateChart](./media/aggregatechart-300x230.png)
**Aggreger** – Budgetplanlinjerne aggregeres fra kildebudgetplanscenariet i de tilknyttede (underordnede) budgetplaner til destinationsscenariet i den overordnede budgetplan. Denne metode gør det muligt at konsolidere budgetbeløb, der er oprettet på et lavere niveau i organisationen, på et højere niveau.          

[![DistributeChart](./media/distributechart-300x230.png)](./media/distributechart.png)
**Fordel** – Budgetplanlinjerne fordeles fra kilden budgetplanlægningsscenariet i den overordnede budgetplan til destinationsscenariet i de tilknyttede (underordnede) budgetplaner, baseret på de økonomiske dimensioner for organisationsenheder i de tilknyttede planer. Denne metode gør det muligt at sprede budgetbeløb, der er oprettet på et højere niveau i organisationen, ud for en mere lokaliseret gennemgang.           

[![LedgerAllocationRules](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Brug finansfordelingsregler** – Budgetplanlinjerne fordeles fra kildebudgetplanlægningscenariet til destinationscenariet på basis af den valgte finansfordelingsregel. 

[![CopyFromBudgetPlan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopier fra budgetplanen** – Som i fordelingsmetoden oprettes budgetplanlinjer i destinationen på basis af linjerne i en relateret budgetplan. Men for denne metode behøver kildebudgetplanen ikke være overordnet men kan være på et højere niveau i hierarkiet for budgetplanen. Denne fordelingsmetode er nyttig, hvis konsoliderede beløb oprindeligt er budgetteret på et meget højere niveau og skal overføres til et lavere niveau i organisationen for detaljeret gennemgang og regulering, før de kan modtage godkendelse på øverste niveau.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Ved hjælp af fordelingsmetoder i en budgetplan
Hvis du vil udføre fordelinger, skal du vælge de linjer, der skal tildeles, og derefter klikke på **Fordel budget**.

[![AllocateBudgetButton](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Vælg derefter en fordelingsmetode. De resterende felter angives derefter baseret på den metode, du har valgt. Disse felter indeholder kilden og destinationen for budgetplansdataene og en indstilling, der gør det muligt at multiplicere kilden med en bestemt faktor, når destinationsbeløbene er oprettet, for at forenkle masseregulering. Du kan også angive indstillingen **Vedhæft til plan**. Vælg **Nej** for at erstatte de eksisterende budgetplanlinjer, eller Vælg **Ja** for at bevare de eksisterende budgetplanlinjer og tilføje nye linjer for de fordelte beløb.

## <a name="automating-allocations-during-a-workflow"></a>Automatisering af tildelinger under en arbejdsproces
En effektiv funktion gør det muligt at foretage tildelinger automatisk som et led i en arbejdsgang i budgetplanlægningen. I løbet af arbejdsgangen for en budgetplan kan automatiserede opgaver starte en tildeling på et bestemt stadie i budgetplanlægningen. 

Hvis du vil konfigurere automatisk tildeling, skal du først oprette en fordelingstidsplan på siden **Konfiguration af budgetplanlægning**. Fordelingstidsplanen definerer den fordelingsmetode, der skal bruges, når den automatiske tildeling køres, og værdierne af de forskellige fordelingsindstillinger (se beskrivelse i afsnittet ovenfor). 

Derefter skal du oprette en trinvis fordeling på siden **Konfiguration af budgetplanlægning**. Den trinvise fordeling tildeler en fordelingstidsplan til arbejdsgangen for budgetplanlægningen og budgetplanlægningstrinnet. 

Til sidst skal du tilføje en automatiseret opgave til fordeling på det ønskede arbejdsprocesstadium i budgetplanlægningen. I følgende eksempel er der indsat to fase budgetplanlægningsfordelinger (vises med rødt) i arbejdsprocessen.

[![BudgetPlanningStageAllocations](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)




