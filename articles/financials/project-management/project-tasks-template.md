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

# <a name="synchronize-project-tasks-from-project-service-automation-directly-to-project-activities-in-finance-and-operations"></a><span data-ttu-id="16907-103">Synkronisere projektopgaver fra Project Service Automation direkte med projektaktiviteter i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="16907-103">Synchronize project tasks from Project Service Automation directly to project activities in Finance and Operations</span></span>

<span data-ttu-id="16907-104">I dette emne beskrives den skabelon og underliggende opgave, der bruges til at synkronisere projektopgaver direkte fra Microsoft Dynamics 365 for Project Service Automation med Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="16907-104">This topic describes the template and underlying task that is used to synchronize project tasks directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="16907-105">Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelige i Dynamics 365 for Finance and Operations version 8.0.</span><span class="sxs-lookup"><span data-stu-id="16907-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="16907-106">Dataflow for Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="16907-106">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="16907-107">Løsningen til integration af Project Service Automation med Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="16907-107">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="16907-108">Integrationsskabelonen, der er tilgængelig i dataintegrationsfunktionen, muliggør strømmen af data vedrørende faktiske projektopgaver fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="16907-108">The integration template that is available with the Data integration feature enables the flow of data about project tasks from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="16907-109">I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="16907-109">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="16907-110">[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span><span class="sxs-lookup"><span data-stu-id="16907-110">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectTasksFlow.png)](./media/ProjectTasksFlow.png)</span></span>

## <a name="template-and-task"></a><span data-ttu-id="16907-111">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="16907-111">Template and task</span></span>

<span data-ttu-id="16907-112">Du kan få adgang skabelonen ved i Microsoft PowerApps Admininstration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="16907-112">To access the template, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="16907-113">Følgende skabelon og underliggende opgave bruges til at synkronisere projektopgaver fra Project Service Automation til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="16907-113">The following template and underlying task is used to synchronize project tasks from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="16907-114">-**Navnet på skabelonen i dataintegration:** Projektopgaver (PSA til Fin and Ops) -**Navnet på opgaven i projektet:** Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="16907-114">-**Name of the template in Data integration:** Project tasks (PSA to Fin and Ops) -**Name of the task in the project:** Project tasks</span></span>

<span data-ttu-id="16907-115">Før der kan foretages synkronisering af projektopgaver, skal du synkronisere projektkontrakter og projekter.</span><span class="sxs-lookup"><span data-stu-id="16907-115">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="entity-set"></a><span data-ttu-id="16907-116">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="16907-116">Entity set</span></span>

|<span data-ttu-id="16907-117">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="16907-117">Project Service Automation</span></span>               | <span data-ttu-id="16907-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="16907-118">Finance and Operations</span></span>                |
|-----------------------------------------|---------------------------------------|
| <span data-ttu-id="16907-119">Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="16907-119">Project Tasks</span></span>                           | <span data-ttu-id="16907-120">Integrationsenhed for projektopgave.</span><span class="sxs-lookup"><span data-stu-id="16907-120">Integration entity for project task.</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="16907-121">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="16907-121">Entity flow</span></span>

<span data-ttu-id="16907-122">Projektopgaver administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projektaktiviteter.</span><span class="sxs-lookup"><span data-stu-id="16907-122">Project tasks are managed in Project Service Automation, and they are synchronized to Finance and Operations as project activities.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="16907-123">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="16907-123">Prerequisites and mapping setup</span></span>

<span data-ttu-id="16907-124">Før der kan foretages synkronisering af projektopgaver, skal du synkronisere projektkontrakter og projekter.</span><span class="sxs-lookup"><span data-stu-id="16907-124">Before synchronization of project tasks can occur, you must synchronize project contracts and projects.</span></span>

## <a name="power-query"></a><span data-ttu-id="16907-125">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="16907-125">Power Query</span></span>

<span data-ttu-id="16907-126">Du skal bruge Microsoft Power-forespørgsel til at filtrere data, hvis disse betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="16907-126">You must use Microsoft Power Query to filter data if these conditions are met:</span></span>

- <span data-ttu-id="16907-127">Du har ressourcespecifikke poster i en projektopgave.</span><span class="sxs-lookup"><span data-stu-id="16907-127">You have resource specific records within a project task.</span></span>

<span data-ttu-id="16907-128">Hvis du skal bruge Power-forespørgsel, skal du følge disse retningslinjer:</span><span class="sxs-lookup"><span data-stu-id="16907-128">If you must use Power Query, follow these guidelines:</span></span>

- <span data-ttu-id="16907-129">Skabelonen Projektopgaver (PSA til Fin and Ops) har et standardfilter, hvis du vil udelade ressourcespecifikke poster fra en projektopgave ved at indstille filteret for **IsLineTask** til **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="16907-129">The Project tasks (PSA to Fin and Ops) template has a default filter to exclude resource specific records from within a project task by setting the filter on the **IsLineTask** to **False**.</span></span> <span data-ttu-id="16907-130">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="16907-130">If you create your own template, you must add this filter.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="16907-131">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="16907-131">Template mapping in Data integration</span></span>

<span data-ttu-id="16907-132">Følgende illustration viser et eksempel på skabelonopgavetilknytningerne i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="16907-132">The following illustration shows an example of the template task mappings in Data integration.</span></span> <span data-ttu-id="16907-133">Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="16907-133">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="16907-134">[![Tilknytning af skabelon](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span><span class="sxs-lookup"><span data-stu-id="16907-134">[![Template mapping](./media/ProjectTasksMapping.png)](./media/ProjectTasksMapping.png)</span></span>


