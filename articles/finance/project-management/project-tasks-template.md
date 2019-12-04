---
title: Synkronisere projektopgaver direkte fra Project Service Automation til Finance and Operations
description: I dette emne beskrives den skabelon og underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
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
ms.dyn365.ops.version: AX 7.3.0
ms.openlocfilehash: ba475721b69e7c75dfd2197597b54050a3598d37
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770260"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a>Synkronisere projektopgaver direkte fra Project Service Automation til Finance and Operations

[!include[banner](../includes/banner.md)]

I dette emne beskrives den skabelon og underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.

> [!NOTE]
> - Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.
> - Hvis du bruger Enterprise edition 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet. Hvis du skal nulstille regnskabsfordelingerne, anbefalede vi, at du også installerer KB 4131710.
> - Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.

## <a name="data-flow-for-project-service-automation-to-finance"></a>Dataflow for Project Service Automation til Finance

Løsningen til integration af Project Service Automation og Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance. Integrationsskabelonen, der er tilgængelig i dataintegrationsfunktionen, muliggør strømmen af data vedrørende faktiske projektopgaver fra Project Service Automation til Finance.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance.

[![Dataflow for Project Service Automation-integration med Finance](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Skabelon og opgaver

Du kan få adgang skabelonen ved i Microsoft Power Apps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabelon og underliggende opgave bruges til at synkronisere projektopgaver fra Project Service Automation til Finance:

- **Navnet på skabelonen i dataintegration:** Projektopgaver (PSA til Fin and Ops)
- **Navnet på opgaven i projektet:** Projektopgaver

Før der kan foretages synkronisering af projektopgaver, skal du synkronisere projektkontrakter og projekter.

## <a name="entity-set"></a>Enhedssæt

| Project Service Automation | Finans                             |
|----------------------------|-------------------------------------|
| Projektopgaver              | Integrationsenhed for projektopgave |

## <a name="entity-flow"></a>Enhedsflow

Projektopgaver administreres i Project Service Automation, og de synkroniseres med Finance som projektaktiviteter.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

Før der kan foretages synkronisering af projektopgaver, skal du synkronisere projektkontrakter og projekter.

## <a name="power-query"></a>Power-forespørgsel

Du skal bruge Microsoft Power-forespørgsel til Excel til at filtrere data, hvis denne betingelser er opfyldt:

- Du har ressourcespecifikke poster i en projektopgave.

Hvis du skal bruge Power-forespørgsel, skal du følge disse retningslinjer:

- Skabelonen Projektopgaver (PSA til Fin and Ops) har et standardfilter, der udelader ressourcespecifikke poster fra en projektopgave ved at indstille filteret for **IsLineTask** til **Falsk**. Hvis du opretter din egen skabelon, skal du tilføje dette filter.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på skabelonopgavetilknytningerne i dataintegration. Tilknytningen viser de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.

[![Tilknytning af skabelon](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)
