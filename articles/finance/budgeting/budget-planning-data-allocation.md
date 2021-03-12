---
title: Datafordeling til budgetplanlægning
description: I dette emne beskrives de forskellige fordelingsmetoder, der er tilgængelige i Microsoft Dynamics 365 Finance, og hvordan de kan bruges.
author: ShylaThompson
manager: AnnBe
ms.date: 03/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: BudgetPlanningConfiguration
audience: Application User
ms.reviewer: roschlom
ms.custom: 15191
ms.assetid: 89a918e8-59a4-4711-a2e9-b41989ddd0f1
ms.search.region: Global
ms.author: sigitac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b07a0f59dfba1cc38133f0cc8ea02e0515f43443
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4971247"
---
# <a name="budget-planning-data-allocation"></a>Datafordeling til budgetplanlægning

[!include [banner](../includes/banner.md)]

I dette emne beskrives de forskellige fordelingsmetoder, der er tilgængelige i Microsoft Dynamics 365 Finance, og hvordan de kan bruges.  

Du kan distribuere data i en budgetplan på en række forskellige måder at give et præcist billede af de forventede beløb.

## <a name="allocation-methods"></a>Fordelingsmetoder
Tre fordelingsmetoder (Fordel hen over perioder, Fordel på dimensioner og Brug finansfordelingsregler) kan oprette budgetplanlinjer, der er baseret på linjer i den samme budgetplan. Tre andre metoder (Aggregat, Fordel og Kopier fra budgetplanen) kan oprette budgetplanlinjer i andre budgetplaner. Du kan angive destinationsscenariet for alle seks fordelingsmetoder. Destinationsscenariet kan enten være det samme som kildescenariet eller forskelligt fra kildescenariet. Desuden kan du angive, om nye linjer er føjet til budgetplanen eller erstatter de aktuelle linjer i budgetplanen.

> [!NOTE] 
> Et entydigt scenarie skal bruges til sammenlægning, der adskiller sig fra det scenarie, som blev brugt til distribution, eller andre ændringer, som tidligere er udført i den overordnede plan.  

[![Fordel på tværs af metode for periodefordeling](./media/allocateacrossperiods-300x259.png)](./media/allocateacrossperiods.png)
**Fordel på tværs af perioder** – En periodefordelingskategori bruges til at fordele budgetplanlinjerne fra Kildebudgetplanscenariet på tværs af perioder i destinationsscenariet. Beløbet i kildedokumentet er tildelt flere linjer i destinationsscenariet, baseret på den procentdel og dato, der er defineret i periodefordelingskategorien.         

[![Fordel til metode for dimensionsfordeling](./media/allocatetodimensions.jpg)](./media/allocatetodimensions.jpg)
**Fordel på dimensioner** – Budgetplanlinjerne fordeles fra kildebudgetplanlægningsscenariet til en eller flere linjer i destinationsscenariet, baseret på procentsatserne og de økonomiske dimensioner, der er defineret i den valgte budgetfordelingsbetingelse.           

![Aggreger diagram](./media/aggregatechart-300x230.png)
**Aggreger** – Budgetplanlinjerne aggregeres fra kildebudgetplanscenariet i de tilknyttede (underordnede) budgetplaner til destinationsscenariet i den overordnede budgetplan. Denne metode gør det muligt at konsolidere budgetbeløb, der er oprettet på et lavere niveau i organisationen, på et højere niveau.          

[![Fordel diagram](./media/distributechart-300x230.png)](./media/distributechart.png)
**Fordel** – Budgetplanlinjerne fordeles fra kilden budgetplanlægningsscenariet i den overordnede budgetplan til destinationsscenariet i de tilknyttede (underordnede) budgetplaner, baseret på de økonomiske dimensioner for organisationsenheder i de tilknyttede planer. Denne metode gør det muligt at sprede budgetbeløb, der er oprettet på et højere niveau i organisationen, ud for en mere lokaliseret gennemgang.           

[![Regler for finansfordeling](./media/ledgerallocationrules-300x202.png)](./media/ledgerallocationrules.png)
**Brug finansfordelingsregler** – Budgetplanlinjerne fordeles fra kildebudgetplanlægningscenariet til destinationscenariet på basis af den valgte finansfordelingsregel. 

[![Kopier fra budgetplan](./media/copyfrombudgetplan-187x300.png)](./media/copyfrombudgetplan.png)
**Kopier fra budgetplanen** – Som i fordelingsmetoden oprettes budgetplanlinjer i destinationen på basis af linjerne i en relateret budgetplan. Men for denne metode behøver kildebudgetplanen ikke være overordnet men kan være på et højere niveau i hierarkiet for budgetplanen. Denne fordelingsmetode er nyttig, hvis konsoliderede beløb oprindeligt er budgetteret på et meget højere niveau og skal overføres til et lavere niveau i organisationen for detaljeret gennemgang og regulering, før de kan modtage godkendelse på øverste niveau.          

## <a name="using-allocation-methods-in-a-budget-plan"></a>Ved hjælp af fordelingsmetoder i en budgetplan
Hvis du vil udføre fordelinger, skal du vælge de linjer, der skal tildeles, og derefter klikke på **Fordel budget**.

[![Knappen Fordel budget](./media/allocatebudgetbutton-300x84.png)](./media/allocatebudgetbutton.png) 

Vælg derefter en fordelingsmetode. De resterende felter angives derefter baseret på den metode, du har valgt. Disse felter indeholder kilden og destinationen for budgetplansdataene og en indstilling, der gør det muligt at multiplicere kilden med en bestemt faktor, når destinationsbeløbene er oprettet, for at forenkle masseregulering. Du kan også angive indstillingen **Vedhæft til plan**. Vælg **Nej** for at erstatte de eksisterende budgetplanlinjer, eller Vælg **Ja** for at bevare de eksisterende budgetplanlinjer og tilføje nye linjer for de fordelte beløb.

## <a name="automating-allocations-during-a-workflow"></a>Automatisering af tildelinger under en arbejdsproces
En effektiv funktion gør det muligt at foretage tildelinger automatisk som et led i en arbejdsgang i budgetplanlægningen. I løbet af arbejdsgangen for en budgetplan kan automatiserede opgaver starte en tildeling på et bestemt stadie i budgetplanlægningen. 

Hvis du vil konfigurere automatisk tildeling, skal du først oprette en fordelingstidsplan på siden **Konfiguration af budgetplanlægning**. Fordelingstidsplanen definerer den fordelingsmetode, der skal bruges, når den automatiske tildeling køres, og værdierne af de forskellige fordelingsindstillinger (se beskrivelse i afsnittet ovenfor). 

Derefter skal du oprette en trinvis fordeling på siden **Konfiguration af budgetplanlægning**. Den trinvise fordeling tildeler en fordelingstidsplan til arbejdsgangen for budgetplanlægningen og budgetplanlægningstrinnet. 

Til sidst skal du tilføje en automatiseret opgave til fordeling på det ønskede arbejdsprocesstadium i budgetplanlægningen. I følgende eksempel er der indsat to fase budgetplanlægningsfordelinger (vises med rødt) i arbejdsprocessen.

[![Trinfordelinger for budgetplanlægning](./media/budgetplanningstageallocations-300x300.png)](./media/budgetplanningstageallocations.png)



