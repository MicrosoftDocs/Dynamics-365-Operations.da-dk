---
title: Koncernkontogrupper og yderligere af konsolideringskonti
description: Dette emne indeholder oplysninger om koncernkontogrupper og yderligere af konsolideringskonti, og forklarer, hvordan de bruges i Microsoft Dynamics 365 for operationer.
author: RobinARH
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: Operations, Core
ms.custom: 265544
ms.assetid: 71c31df7-b655-46a8-8844-4f92a8bd71b0
ms.search.region: Global
ms.author: aolson
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
translationtype: Human Translation
ms.sourcegitcommit: 9f4d7fdd8cfa7a540fce219f6ae4792e57dfbe44
ms.openlocfilehash: f9c5aaa389c9c2f85d1ab91cbf3d2222cbebef55
ms.lasthandoff: 03/31/2017


---

# <a name="consolidation-account-groups-and-additional-consolidation-accounts"></a>Koncernkontogrupper og yderligere af konsolideringskonti

Dette emne indeholder oplysninger om koncernkontogrupper og yderligere af konsolideringskonti, og forklarer, hvordan de bruges i Microsoft Dynamics 365 for operationer.

<a name="consolidation-account-groups"></a>Koncernkontogrupper
----------------------------

Koncernkontogrupper kan du oprette grupper af firmaer, du vil bruge til at konsolidere data. Oftest en koncernkontogruppe repræsenterer en lovpligtig kontoplan eller knytter konti til en gruppe, der er defineret af virksomhedens hovedkvarter. Du kan finde konsolidering kontogrupper i den **Setup** område af den **konsolideringer** modul. Når du tilføjer en ny gruppe, kan du angive en entydig identifier for kontogruppen og et navn.

## <a name="additional-consolidation-accounts"></a>Flere koncernkonti
Af flere konsolideringskonti, kan du tildele en konto fra en eksisterende kontoplan til en koncernkontogruppe. Du kan derefter angive en konsolidering kontoværdi og et navn. 

Du kan finde yderligere konsolideringskonti i den **Setup** område i den **konsolideringer** modul. Når du opretter en ny konto til konsolidering, skal du angive følgende oplysninger:

-   **Hovedkonto** – dette felt er et opslag, der viser alle de hovedkonti, der er baseret på kontoplanen, som du valgte på siden. Når du vælger en konto, angives navnet automatisk i den **Main kontonavn** felt.
-   **Koncernkontogruppen** – Brug dette felt til at angive for at tildele kontoen til gruppen. Hvis du samler på to forskellige måder, skal du føje den samme konto til alle fire koncernkontogrupper.
-   **Koncernkonto** – Angiv værdien af koncernkontoen. Denne værdi behøver ikke være en konto fra en kontoplan. Det kan være enhver værdi, som du har brug for.
-   **Konsolidering kontonavn** – Angiv navnet på den konto, som du vil have det vist i forespørgsler og rapporter.
-   **SAT niveau** – dette felt bruges til at rapportere kontoudtog til de mexicanske myndigheder. 

Når du er færdig med at oprette dine koncernkontogrupper og yderligere af konsolideringskonti, kan du markere gruppen i processen konsolideres online.



