---
title: Synkronisere projektopgaver fra Project Service Automation
description: I dette emne beskrives den skabelon og underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Microsoft Dynamics 365 for Project Service Automation med Dynamics 365 for Finance and Operations.
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
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: 399b519ab0da4de405aeb06f3e7f4bf29a6c5cc3
ms.openlocfilehash: 89df0d99d780441ad08cd6bff3e1fd203694eb8e
ms.contentlocale: da-dk
ms.lasthandoff: 05/30/2018

---

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a>Synkronisere projektopgaver fra Project Service Automation direkte med projektaktiviteter i Finance and Operations

I dette emne beskrives den skabelon og underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Microsoft Dynamics 365 for Project Service Automation med Dynamics 365 for Finance and Operations.

> [!NOTE]
> Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelige i Dynamics 365 for Finance and Operations version 8.0.

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a>Dataflow for Project Service Automation til Finance and Operations

Løsningen til integration af Project Service Automation med Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations. Integrationsskabelonen, der er tilgængelig i dataintegrationsfunktionen, muliggør strømmen af data vedrørende faktiske projektopgaver fra Project Service Automation til Finance and Operations.

I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.

[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)

## <a name="template-and-task"></a>Skabelon og opgaver

Du kan få adgang skabelonen ved i Microsoft PowerApps Admininstration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.

Følgende skabelon og underliggende opgave bruges til at synkronisere projektopgaver fra Project Service Automation til Finance and Operations:

-**Navnet på skabelonen i dataintegration:** Projektopgaver (PSA til Fin and Ops) -**Navnet på opgaven i projektet:** Projektopgaver

Før der kan foretages synkronisering af projektopgaver, skal du synkronisere projektkontrakter og projekter.

## <a name="entity-set"></a>Enhedssæt

|Project Service Automation               | Finance and Operations                |
|-----------------------------------------|---------------------------------------|
| Projektopgaver                           | Integrationsenhed for projektopgave.   |

## <a name="entity-flow"></a>Enhedsflow

Projektopgaver administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projektaktiviteter.

## <a name="prerequisites-and-mapping-setup"></a>Forudsætninger og tilknytningsopsætning

Før der kan foretages synkronisering af projektopgaver, skal du synkronisere projektkontrakter og projekter.

## <a name="power-query"></a>Power-forespørgsel

Du skal bruge Microsoft Power-forespørgsel til at filtrere data, hvis disse betingelser er opfyldt:

- Du har ressourcespecifikke poster i en projektopgave.

Hvis du skal bruge Power-forespørgsel, skal du følge disse retningslinjer:

- Skabelonen Projektopgaver (PSA til Fin and Ops) har et standardfilter, hvis du vil udelade ressourcespecifikke poster fra en projektopgave ved at indstille filteret for **IsLineTask** til **Falsk**. Hvis du opretter din egen skabelon, skal du tilføje dette filter.

## <a name="template-mapping-in-data-integration"></a>Skabelontilknytning i dataintegration

Følgende illustration viser et eksempel på skabelonopgavetilknytningerne i dataintegration. Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.

[![Tilknytning af skabelon](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)


