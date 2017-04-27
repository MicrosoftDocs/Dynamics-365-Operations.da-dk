---
title: Foretag fordelinger
description: "Denne artikel indeholder oplysninger om allokeringer, indstillinger for behandling af dem i Microsoft Dynamics 365 for Operations, og hvordan de kan bruges i budgetplanlægning. Tildelinger bruges til at distribuere beløb på tværs af flere finanskontokombinationer. De hjælper med at sikre, at udgifter eller indtægter debiteres for det rigtige objekt i regnskabet."
author: twheeloc
manager: AnnBe
ms.date: 2017-04-04
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: annbe
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: 37f4df5d0b79208a8c565bc9101ddde193a6ef5b
ms.lasthandoff: 03/31/2017


---

# <a name="process-allocations"></a>Foretag fordelinger

Denne artikel indeholder oplysninger om allokeringer, indstillinger for behandling af dem i Microsoft Dynamics 365 for Operations, og hvordan de kan bruges i budgetplanlægning. Tildelinger bruges til at distribuere beløb på tværs af flere finanskontokombinationer. De hjælper med at sikre, at udgifter eller indtægter debiteres for det rigtige objekt i regnskabet.

Microsoft Dynamics 365 for Operations indeholder følgende funktioner, der understøtter denne proces:

-   Tildel transaktionsbeløb manuelt, ved hjælp af handlingen Opdel i regnskabsfordelinger eller ved at anvende standardskabeloner til økonomiske dimensioner for et dokument. Yderligere oplysninger finder du i afsnittet [Regnskabsfordelinger.](\accounts-payable\accounting-distributions.md)
-   Fordel automatisk posteringsbeløb baseret på fordelingsbetingelserne, der er defineret for enkelte hovedkonto. Poster på fordelingskonti vil blive genereret for hver kladde, der er baseret på finanskontoen procentdel og destination, hver gang en regnskabspost opfylder de kriterier, der er defineret som kilde for finanskontoen.
-   Tildel automatisk finanssaldi eller faste beløb, der er baseret på fordelingsregler for Finans. Fordelingsreglerne for finans behandles med jævne mellemrum ved hjælp af fordelingskladder. 

###  <a name="allocations-in-budget-planning"></a>Fordelinger i budgetplanlægning

Finansfordelingsregler kan bruges til budgetplaner. Når du bruger finansfordelingsregler i budgetplanlægningen, fungerer allokeringsreglerne på samme måde, som de ville i Finans, men kildedata og destinationsdata kommer fra budgetplanen. Du kan manuelt vælge finansfordelingsregler, som skal bruges til budgetplaner. Du kan også bruge en fordelingstidsplan, der kører som en del af en arbejdsgangproces.

> [!NOTE]
> Du kan ikke bruge interne finansfordelingsregler til budgetplanlæsning.




