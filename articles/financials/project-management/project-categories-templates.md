---
title: Synkronisere projektudgiftskategorier fra Project Service Automation
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektudgiftskategorier mellem Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 04/02/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: da-dk
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synkronisere projektudgiftskategorier mellem Finance and Operations og Project Service Automation

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektudgiftskategorier mellem Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation.

> [!NOTE]
> Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelige i Dynamics 365 for Finance and Operations version 8.0.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Dataflow for Project Service Automation og Finance and Operations

Løsningen til integration af Project Service Automation og Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations. Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om transaktionskategorier for projektudgifter mellem Finance and Operations og Project Service Automation.

Hvis projektudgiftskategorier administreres i Finance and Operations, går integrationsflowet først fra Finance and Operations til Project Service Automation, og derefter opdateres projektudgiftskategoriers integrations-id'er ved at synkronisere fra Project Service Automation til Finance and Operations.

Hvis projektudgiftskategorier administreres i Project Service Automation, er integrationsflowet først fra Project Service Automation til Finance and Operations. Projektkategorier skal allerede være konfigureret i Finance and Operations inden synkronisering af Project Service Automation. Derefter synkroniseres fra Finance and Operations til Project Service Automation og derefter fra Project Service Automation til Finance and Operations igen. Dette sikrer, at kategorierne sammenkædes, og at der ikke oprettes dubletter.

> [!NOTE]
> Projektudgiftskategorierne håndteres typisk i Finance and Operations. Hvis det ikke er tilfældet, eller du allerede har udgiftskategorier, der er oprettet i Project Service Automation, skal du først synkronisere med transaktionskategorier for projektudgifter (PSA til Fin and Ops) og derefter synkronisere ved hjælp af transaktionskategorier for projektudgifter (Fin and Ops til PSA). Du skal derefter køre synkroniseringen fra PSA til Fin and Ops igen.

> Hvis synkroniseringen først udføres fra Project Service Automation, skal projektkategorierne allerede være oprettet i Finance and Operations, og projektkategorier, der skal synkroniseres med Project Service Automation-transaktionskategorier, skal være konfigurerede som **Aktiv i kladder**.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.

[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)


## <a name="templates-and-tasks"></a>Skabeloner og opgaver

Du kan få adgang til tilgængelige skabeloner ved i Microsoft PowerApps Admininstration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Finance and Operations til Project Service Automation:

-  **Navn på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (Fin and Ops til PSA)
-  **Navnet på opgaven i projektet:** Synkroniseringskategorier til PSA

## <a name="entity-set"></a>Enhedssæt

| Finance and Operations               | Project Service Automation    |
|--------------------------------------|-------------------------------|
| Integrationsenhed for kategorier    | Transaktionskategorier        |

## <a name="entity-flow"></a>Enhedsflow

Projektudgiftskategorier administreres i Finance and Operations, og de synkroniseres med Project Service Automation som transaktionskategorier.

## <a name="power-query"></a>Power-forespørgsel

Du skal bruge Microsoft Power-forespørgsel til at angive faktureringstypen i transaktionskategorien, når du synkroniserer med Project Service Automation. Skabelonen til transaktionskategorier for projektudgifter (Fin and Ops til PSA) har en standardkolonne og tilknytning, der er allerede angivet. Hvis du opretter din egen skabelon, skal du tilføje en betinget kolonne i Power-forespørgsel.
- Åbn formularen Avanceret forespørgsel og filtrering fra tilknytningen af opgaven projektudgiftskategorier.
- Vælg **Tilføj betinget kolonne**.
- Giv den nye kolonne et navn, f.eks. BillingType.
- Angiv følgende betingelse: if **CATEGORYID not equal to null then 19235001, Otherwise null**.
- Klik på **OK** i kolonnen.
- Sørg for at tilknytte den nye kolonne på tilknytningssiden.

Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Finance and Operations til Project Service Automation.

[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

Følgende skabeloner og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Project Service Automation til Finance and Operations:

-**Navnet på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (PSA til Fin and Ops) -**Navnet på opgaven i projektet:** Synkronisering af kategorier til Fin Ops

## <a name="entity-set"></a>Enhedssæt

| Project Service Automation      | Finance and Operations             |
|---------------------------------|------------------------------------|
| Transaktionskategorier          | Integrationsenhed for kategorier  | 

## <a name="entity-flow"></a>Enhedsflow

Projektudgiftskategorier administreres i Finance and Operations, og de synkroniseres med Project Service Automation som transaktionskategorier. Synkroniseringen tilbage til Finance and Operations opdaterer integrations-id'et fra Project Service Automation i Finance and Operations-projektkategorien.

Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.

> [!NOTE]
> Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.

[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)

