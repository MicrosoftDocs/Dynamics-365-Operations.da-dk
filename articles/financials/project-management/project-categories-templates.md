---
title: Synkronisere projektudgiftskategorier mellem Finance and Operations og Project Service Automation
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektudgiftskategorier mellem Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: c4d09fde2cf4335553243c136590f9f3135db97a
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "347830"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synkronisere projektudgiftskategorier mellem Finance and Operations og Project Service Automation

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektudgiftskategorier mellem Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation.

> [!NOTE]
> - Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.
> - Integration af faktiske oplysninger er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.1 eller nyere.
> - Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet. Hvis du skal nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a>Dataflow for Project Service Automation og Finance and Operations

Løsningen til integration af Project Service Automation og Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations. Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om transaktionskategorier for projektudgifter mellem Finance and Operations og Project Service Automation.

Hvis projektudgiftskategorier administreres i Finance and Operations, er integrationsflowet først fra Finance and Operations til Project Service Automation. Integrations-id'er for projektudgiftskategorier opdateres gennem synkronisering fra Project Service Automation til Finance and Operations.

Hvis projektudgiftskategorier administreres i Project Service Automation, er integrationsflowet først fra Project Service Automation til Finance and Operations. Projektkategorier skal allerede være konfigureret i Finance and Operations før synkroniseringen fra Project Service Automation. Derefter synkroniseres fra Finance and Operations til Project Service Automation og derefter fra Project Service Automation til Finance and Operations igen. På denne måde kan du hjælpe med til at sikre, at kategorierne sammenkædes, og at der ikke oprettes dubletter.

> [!NOTE]
> Projektudgiftskategorierne håndteres typisk i Finance and Operations. Men hvis de ikke styres i Finance and Operations, eller hvis udgiftskategorierne allerede er oprettet i Project Service Automation, skal du først synkronisere ved hjælp af skabelonen Transaktionskategorier for projektudgifter (PSA til Fin and Ops) Derefter skal du synkronisere ved hjælp af skabelonen Transaktionskategorier for projektudgifter (Fin and Ops til PSA). Du skal derefter køre synkroniseringen fra Project Service Automation til Finance and Operations igen.
>
> Hvis du synkroniserer først fra Project Service Automation, skal følgende krav opfyldes i Finance and Operations, før synkroniseringen udføres:
>
> - Den delte kategori, der svarer til den projektkategori, der er oprettet i Project Service Automation skal findes, og den skal være aktiveret for både **Projekt** og **Udgift**.
> - For hver juridisk enhed i Finance and Operations, der skal integreres med, skal der være følgende projektkategorier:
>
>     - **Projektkategori** findes. 
>     - **Brug i udgift** er aktiveret.
>     - **Aktiv i kladde** er aktiveret.
>     - **Transaktionstype** er angivet til **Udgift**.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.

[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a>Synkronisering af projektudgiftskategorier fra Finance and Operations til Project Service Automation

### <a name="template-and-task"></a>Skabelon og opgaver

Du kan få adgang skabelonen ved i Microsoft PowerApps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Finance and Operations til Project Service Automation:

- **Navn på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (Fin and Ops til PSA)
- **Navnet på opgaven i projektet:** Synkroniseringskategorier til PSA

### <a name="entity-set"></a>Enhedssæt

| Finance and Operations            | Project Service Automation |
|-----------------------------------|----------------------------|
| Integrationsenhed for kategorier | Transaktionskategorier     |

### <a name="entity-flow"></a>Enhedsflow

Projektudgiftskategorier administreres i Finance and Operations, og de synkroniseres med Project Service Automation som transaktionskategorier.

### <a name="power-query"></a>Power-forespørgsel

Når du synkroniserer til Project Service Automation, skal du skal bruge Microsoft Power-forespørgsel til Excel til at angive faktureringstypen i transaktionskategorien. Skabelonen Transaktionskategorier for projektudgifter (Fin and Ops til PSA) har en standardkolonne og tilknytning. Hvis du opretter din egen skabelon, skal du tilføje en betinget kolonne i Power-forespørgsel. Følg disse trin.

1. Klik på pilen for at åbne tilknytningen af projektudgiftskategorier i skabelonen Transaktionskategorier for projektudgifter (Fin and Ops til PSA).
2. Klik på linket **Avanceret forespørgsel og filtrering** for at åbne Power-forespørgslen.
2. Vælg **Tilføj betinget kolonne**.
3. Angiv et navn til den nye kolonne, f.eks. **BillingType**.
4. Angiv følgende betingelse: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Klik på **OK** i kolonnen.
6. Sørg for at tilknytte den nye kolonne på tilknytningssiden.

Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Finance and Operations til Project Service Automation.

[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a>Synkronisering af projektudgiftskategorier fra Project Service Automation til Finance and Operations

### <a name="template-and-task"></a>Skabelon og opgaver

Følgende skabelon og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Project Service Automation til Finance and Operations:

- **Navn på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (PSA til Fin and Ops)
- **Navnet på opgaven i projektet:** Synkroniseringskategorier til Fin Ops

### <a name="entity-set"></a>Enhedssæt

| Project Service Automation | Finance and Operations            |
|----------------------------|-----------------------------------|
| Transaktionskategorier     | Integrationsenhed for kategorier |

### <a name="entity-flow"></a>Enhedsflow

Projektudgiftskategorier administreres i Finance and Operations, og de synkroniseres med Project Service Automation som transaktionskategorier. Synkroniseringen tilbage til Finance and Operations opdaterer projektkategorien i Finance and Operations med integrations-id'et fra Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.

> [!NOTE]
> Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.

[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
