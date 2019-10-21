---
title: Synkronisere projektudgiftskategorier mellem Finance and Operations og Project Service Automation
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektudgiftskategorier mellem Microsoft Dynamics 365 Finance og Dynamics 365 Project Service Automation.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 8.0.0
ms.openlocfilehash: 482febc91a04766216f9887ab59d30cc9aed5096
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250501"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a>Synkronisere projektudgiftskategorier mellem Finance and Operations og Project Service Automation

[!include[banner](../includes/banner.md)]

I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektudgiftskategorier mellem Dynamics 365 Finance og Dynamics 365 Project Service Automation.

> [!NOTE]
> - Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.
> - Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.
> - Hvis du bruger Enterprise edition 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet. Hvis du skal nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.

## <a name="data-flow-for-project-service-automation-and-finance"></a>Dataflow for Project Service Automation og Finance

Løsningen til integration af Project Service Automation og Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance. Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om transaktionskategorier for projektudgifter mellem Finance og Project Service Automation.

Hvis projektudgiftskategorier administreres i Finance, er integrationsflowet først fra Finance til Project Service Automation. Integrations-id'er for projektudgiftskategorier opdateres gennem synkronisering fra Project Service Automation til Finance.

Hvis projektudgiftskategorier administreres i Project Service Automation, er integrationsflowet først fra Project Service Automation til Finance. Projektkategorier skal allerede være konfigureret i Finance før synkroniseringen fra Project Service Automation. Derefter synkroniseres fra Finance til Project Service Automation og derefter fra Project Service Automation til Finance igen. På denne måde kan du hjælpe med til at sikre, at kategorierne sammenkædes, og at der ikke oprettes dubletter.

> [!NOTE]
> Projektudgiftskategorierne håndteres typisk i Finance. Men hvis de ikke gør det, eller hvis udgiftskategorierne allerede er oprettet i Project Service Automation, skal du først synkronisere ved hjælp af skabelonen Transaktionskategorier for projektudgifter (PSA til Fin and Ops) Derefter skal du synkronisere ved hjælp af skabelonen Transaktionskategorier for projektudgifter (Fin and Ops til PSA). Du skal derefter køre synkroniseringen fra Project Service Automation til Finance igen.
>
> Hvis du synkroniserer først fra Project Service Automation, skal følgende krav opfyldes i Finance, før synkroniseringen udføres:
>
> - Den delte kategori, der svarer til den projektkategori, der er oprettet i Project Service Automation skal findes, og den skal være aktiveret for både **Projekt** og **Udgift**.
> - For hver juridisk enhed i Finance, der skal integreres med, skal der være følgende projektkategorier:
>
>     - **Projektkategori** findes. 
>     - **Brug i udgift** er aktiveret.
>     - **Aktiv i kladde** er aktiveret.
>     - **Transaktionstype** er angivet til **Udgift**.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance.

[![Dataflow for Project Service Automation-integration med Finance](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)

## <a name="project-expense-category-synchronization-from-finance-to-project-service-automation"></a>Synkronisering af projektudgiftskategorier fra Finance til Project Service Automation

### <a name="template-and-task"></a>Skabelon og opgaver

Du kan få adgang skabelonen ved i Microsoft PowerApps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabeloner og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Finance til Project Service Automation:

- **Navn på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (Fin and Ops til PSA)
- **Navnet på opgaven i projektet:** Synkroniseringskategorier til PSA

### <a name="entity-set"></a>Enhedssæt

| Finans                           | Project Service Automation |
|-----------------------------------|----------------------------|
| Integrationsenhed for kategorier | Transaktionskategorier     |

### <a name="entity-flow"></a>Enhedsflow

Projektudgiftskategorier administreres i Finance, og de synkroniseres med Project Service Automation som transaktionskategorier.

### <a name="power-query"></a>Power-forespørgsel

Når du synkroniserer til Project Service Automation, skal du skal bruge Microsoft Power-forespørgsel til Excel til at angive faktureringstypen i transaktionskategorien. Skabelonen Transaktionskategorier for projektudgifter (Fin and Ops til PSA) har en standardkolonne og tilknytning. Hvis du opretter din egen skabelon, skal du tilføje en betinget kolonne i Power-forespørgsel. Følg disse trin.

1. Klik på pilen for at åbne tilknytningen af projektudgiftskategorier i skabelonen Transaktionskategorier for projektudgifter (Fin and Ops til PSA).
2. Klik på linket **Avanceret forespørgsel og filtrering** for at åbne Power-forespørgslen.
2. Vælg **Tilføj betinget kolonne**.
3. Angiv et navn til den nye kolonne, f.eks. **BillingType**.
4. Angiv følgende betingelse: **if CATEGORYID not equal to null then 19235001, Otherwise null**.
5. Klik på **OK** i kolonnen.
6. Sørg for at tilknytte den nye kolonne på tilknytningssiden.

Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration. Tilknytningen viser de feltoplysninger, der synkroniseres fra Finance til Project Service Automation.

[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance"></a>Synkronisering af projektudgiftskategorier fra Project Service Automation til Finance

### <a name="template-and-task"></a>Skabelon og opgaver

Følgende skabelon og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Project Service Automation til Finance:

- **Navn på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (PSA til Fin and Ops)
- **Navnet på opgaven i projektet:** Synkroniseringskategorier til Fin Ops

### <a name="entity-set"></a>Enhedssæt

| Project Service Automation | Finans                           |
|----------------------------|-----------------------------------|
| Transaktionskategorier     | Integrationsenhed for kategorier |

### <a name="entity-flow"></a>Enhedsflow

Projektudgiftskategorier administreres i Finance, og de synkroniseres med Project Service Automation som transaktionskategorier. Synkroniseringen tilbage til Finance opdaterer projektkategorien i Finance med integrations-id'et fra Project Service Automation.

### <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.

> [!NOTE]
> Tilknytningen viser de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)
