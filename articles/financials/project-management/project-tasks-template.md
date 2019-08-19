---
title: Synkronisere projektopgaver direkte fra Project Service Automation til Finance and Operations
description: I dette emne beskrives den skabelon og underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.
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
ms.openlocfilehash: f7ea5036682ad5b61fe56acd20a591cccc01f2cb
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/01/2019
ms.locfileid: "1838313"
---
# <a name="synchronize-project-tasks-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="3d4b3-103">Synkronisere projektopgaver direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3d4b3-103">Synchronize project tasks directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3d4b3-104">I dette emne beskrives den skabelon og underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Microsoft Dynamics 365 for Project Service Automation til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-104">This topic describes the template and underlying task that are used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="3d4b3-105">Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="3d4b3-106">Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-106">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="3d4b3-107">Hvis du skal nulstille regnskabsfordelingerne, anbefalede vi, at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-107">If you must reset the accounting distributions, we recommended that you also install KB 4131710.</span></span>
> - <span data-ttu-id="3d4b3-108">Integration af faktiske oplysninger er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-108">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="3d4b3-109">Dataflow for Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3d4b3-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="3d4b3-110">Løsningen til integration af Project Service Automation med Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="3d4b3-111">Integrationsskabelonen, der er tilgængelig i dataintegrationsfunktionen, muliggør strømmen af data vedrørende faktiske projektopgaver fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-111">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="3d4b3-112">I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="3d4b3-113">[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="3d4b3-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="3d4b3-114">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="3d4b3-114">Template and task</span></span>

<span data-ttu-id="3d4b3-115">Du kan få adgang skabelonen ved i Microsoft PowerApps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-115">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3d4b3-116">Følgende skabelon og underliggende opgave bruges til at synkronisere projektopgaver fra Project Service Automation til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="3d4b3-116">The following template and underlying task are used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="3d4b3-117">**Navnet på skabelonen i dataintegration:** Projektopgaver (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="3d4b3-117">**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="3d4b3-118">**Navnet på opgaven i projektet:** Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="3d4b3-118">**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="3d4b3-119">Før der kan foretages synkronisering af projektopgaver, skal du synkronisere projektkontrakter og projekter.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-119">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="3d4b3-120">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="3d4b3-120">Entity set</span></span>

| <span data-ttu-id="3d4b3-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="3d4b3-121">Project Service Automation</span></span> | <span data-ttu-id="3d4b3-122">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3d4b3-122">Finance and Operations</span></span>              |
|----------------------------|-------------------------------------|
| <span data-ttu-id="3d4b3-123">Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="3d4b3-123">Project Tasks</span></span>              | <span data-ttu-id="3d4b3-124">Integrationsenhed for projektopgave</span><span class="sxs-lookup"><span data-stu-id="3d4b3-124">Integration entity for project task</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3d4b3-125">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="3d4b3-125">Entity flow</span></span>

<span data-ttu-id="3d4b3-126">Projektopgaver administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-126">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="3d4b3-127">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="3d4b3-127">Prerequisites and mapping setup</span></span>

<span data-ttu-id="3d4b3-128">Før der kan foretages synkronisering af projektopgaver, skal du synkronisere projektkontrakter og projekter.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-128">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="3d4b3-129">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="3d4b3-129">Power Query</span></span>

<span data-ttu-id="3d4b3-130">Du skal bruge Microsoft Power-forespørgsel til Excel til at filtrere data, hvis denne betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="3d4b3-130">You must use Microsoft Power Query for Excel to filter data if this condition is met:</span></span>

- <span data-ttu-id="3d4b3-131">Du har ressourcespecifikke poster i en projektopgave.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-131">You have resource-specific records in a project task.</span></span>

<span data-ttu-id="3d4b3-132">Hvis du skal bruge Power-forespørgsel, skal du følge disse retningslinjer:</span><span class="sxs-lookup"><span data-stu-id="3d4b3-132">If you must use Power Query, follow this guideline:</span></span>

- <span data-ttu-id="3d4b3-133">Skabelonen Projektopgaver (PSA til Fin and Ops) har et standardfilter, der udelader ressourcespecifikke poster fra en projektopgave ved at indstille filteret for **IsLineTask** til **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-133">The Project tasks (PSA to Fin and Ops) template has a default filter that excludes resource-specific records from a project task by setting the filter on **IsLineTask** to **False**.</span></span> <span data-ttu-id="3d4b3-134">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-134">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3d4b3-135">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="3d4b3-135">Template mapping in Data integration</span></span>

<span data-ttu-id="3d4b3-136">Følgende illustration viser et eksempel på skabelonopgavetilknytningerne i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-136">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="3d4b3-137">Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3d4b3-137">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="3d4b3-138">[![Tilknytning af skabelon](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="3d4b3-138">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>
