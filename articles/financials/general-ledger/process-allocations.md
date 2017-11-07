---
title: Foretag fordelinger
description: "Denne artikel indeholder oplysninger om allokeringer, indstillinger for behandling af dem i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, og hvordan de kan bruges i budgetplanlægning. Tildelinger bruges til at distribuere beløb på tværs af flere finanskontokombinationer. De hjælper med at sikre, at udgifter eller indtægter debiteres for det rigtige objekt i regnskabet."
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: AccountingDistribution, LedgerAllocationRule, MainAccount
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 17361
ms.assetid: 04c8548a-0af9-492b-954b-946b4f8ca023
ms.search.region: Global
ms.author: peakerbl
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 8859359f70132e9116e6a2d534a0f5f1d0bfeb80
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="process-allocations"></a>Foretag fordelinger

[!include[banner](../includes/banner.md)]


Denne artikel indeholder oplysninger om allokeringer, indstillinger for behandling af dem i Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, og hvordan de kan bruges i budgetplanlægning. Tildelinger bruges til at distribuere beløb på tværs af flere finanskontokombinationer. De hjælper med at sikre, at udgifter eller indtægter debiteres for det rigtige objekt i regnskabet.

Microsoft Dynamics 365 for Finance and Operations indeholder følgende funktioner, der understøtter denne proces:

-   Tildel transaktionsbeløb manuelt, ved hjælp af handlingen Opdel i regnskabsfordelinger eller ved at anvende standardskabeloner til økonomiske dimensioner for et dokument. Yderligere oplysninger finder du i afsnittet [Regnskabsfordelinger.](../accounts-payable/accounting-distributions.md)
-   Fordel automatisk posteringsbeløb baseret på fordelingsbetingelserne, der er defineret for enkelte hovedkonto. Poster på fordelingskonti vil blive genereret for hver kladde, der er baseret på finanskontoen procentdel og destination, hver gang en regnskabspost opfylder de kriterier, der er defineret som kilde for finanskontoen.
-   Tildel automatisk finanssaldi eller faste beløb, der er baseret på fordelingsregler for Finans. Fordelingsreglerne for finans behandles med jævne mellemrum ved hjælp af fordelingskladder. 

###  <a name="allocations-in-budget-planning"></a>Fordelinger i budgetplanlægning

Finansfordelingsregler kan bruges til budgetplaner. Når du bruger finansfordelingsregler i budgetplanlægningen, fungerer allokeringsreglerne på samme måde, som de ville i Finans, men kildedata og destinationsdata kommer fra budgetplanen. Du kan manuelt vælge finansfordelingsregler, som skal bruges til budgetplaner. Du kan også bruge en fordelingstidsplan, der kører som en del af en arbejdsgangproces.

> [!NOTE]
> Du kan ikke bruge interne finansfordelingsregler til budgetplanlæsning.






