---
title: "Opdatere standardomkostninger i et produktionsmiljø"
description: "Denne artikel indeholder vejledning i at opdatere standardomkostninger i et produktionsmiljø."
author: YuyuScheller
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: fd3392eba3a394bd4b92112093c1f1f9b894426d
ms.openlocfilehash: 564251038b9bdd836857f177e996ab17433e8000
ms.contentlocale: da-dk
ms.lasthandoff: 04/25/2017


---

# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Opdatere standardomkostninger i et produktionsmiljø

[!include[banner](../includes/banner.md)]


Denne artikel indeholder vejledning i at opdatere standardomkostninger i et produktionsmiljø. 

Opdateringer kan afspejle nye varer, omkostningskategorier eller formler til beregning af indirekte omkostninger. De kan også afspejle korrektioner og ændrede omkostninger. Typen af opdatering påvirker, hvilke trin der skal udføres for at opdatere standardomkostninger som vist i følgende tilfælde:

-   Angiv de forventede ændringer af standardomkostninger for købte varer, og ret derefter status for varens omkostningsposter til **Aktiv** på den relevante dato. Du skal dog ikke efterkalkulere omkostningerne for producerede varer, der bruger de købte varer.
-   Angiv standardomkostninger for en ny købt vare, men du skal ikke efterkalkulere omkostningerne for producerede varer med en styklisteversion, der indeholder nye købte varer som en komponent.
-   Korriger eller rediger omkostningerne for en købt vare, eller rediger den omkostningsgruppe, der er tildelt en købt vare, og beregn derefter omkostningen for alle producerede varer med en styklisteversion, der indeholder den købte vare som en komponent.
-   Rediger omkostningerne for en omkostningsart, og beregn omkostningerne for alle producerede varer med en ruteversion, der indeholder ruteoperationer, som bruger omkostningsarten.
-   Ret de omkostningskategorier, der er knyttet til ruteoperationer, eller den omkostningsgruppe, der er tildelt omkostningskategorierne. Beregn derefter omkostningerne for alle producerede varer med en ruteversion, der indeholder ruteoperationer, som bruger omkostningsarten.
-   Rediger en beregningsformel for indirekte omkostninger, og beregn omkostningerne for alle producerede varer, der påvirkes af ændringen.
-   Rediger eller tilføj en produktionslokation for en produceret vare, og beregn varens produktionsomkostninger for lokationen.
-   Beregn eller genberegn omkostningerne for en produceret vare, og genberegn omkostningerne for alle producerede varer med en styklisteversion, der indeholder den producerede vare som en komponent.
-   Beregn omkostninger for en ny produceret vare baseret på den definerede, godkendte og aktive stykliste samt ruteoplysninger.

De kræver alle nøje overvejelser om, hvordan standardomkostningerne skal opdateres.




