---
title: Opdatere standardomkostninger i et produktionsmiljø
description: Denne artikel indeholder vejledning i at opdatere standardomkostninger i et produktionsmiljø.
author: AndersGirke
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CostingVersion, InventStdCostConv
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79663
ms.assetid: 3a7c3d13-8dbc-442d-a281-ac0ebe99ec83
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7bc203176967fbe6c20f4f687fe36fdcf3157b20
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4983819"
---
# <a name="update-standard-costs-in-a-manufacturing-environment"></a>Opdatere standardomkostninger i et produktionsmiljø

[!include [banner](../includes/banner.md)]

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



