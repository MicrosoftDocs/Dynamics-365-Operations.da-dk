---
title: Synkronisere projektestimater direkte fra Project Service Automation til Finance and Operations
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Microsoft Dynamics 365 Project Service Automation til Dynamics 365 Finance.
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
ms.openlocfilehash: ebf0fce60ad006e798aa4f404fbffcf10a0b31f9
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/06/2019
ms.locfileid: "2770283"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="63325-103">Synkronisere projektestimater direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="63325-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="63325-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="63325-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="63325-105">Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.</span><span class="sxs-lookup"><span data-stu-id="63325-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="63325-106">Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="63325-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="63325-107">Dataflow for Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="63325-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="63325-108">Løsningen til integration af Project Service Automation og Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="63325-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="63325-109">Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om projekttimeestimater og projektudgiftsestimater fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="63325-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="63325-110">I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="63325-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="63325-111">[![Dataflow for Project Service Automation-integration med Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="63325-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="63325-112">Projekttimeestimater</span><span class="sxs-lookup"><span data-stu-id="63325-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="63325-113">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="63325-113">Template and tasks</span></span>

<span data-ttu-id="63325-114">Du kan få adgang til de tilgængelige skabeloner ved i Microsoft Power Apps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="63325-114">To access the available templates, in the Microsoft Power Apps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="63325-115">Følgende skabeloner og underliggende opgaver bruges til at synkronisere projekttimeestimater fra Project Service Automation med Finance:</span><span class="sxs-lookup"><span data-stu-id="63325-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="63325-116">**Navn på skabelonen i dataintegration:** Projekttimeestimater (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="63325-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="63325-117">**Navnet på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="63325-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="63325-118">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="63325-118">Transaction relationships</span></span>
    - <span data-ttu-id="63325-119">Udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="63325-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="63325-120">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="63325-120">Entity set</span></span>

| <span data-ttu-id="63325-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="63325-121">Project Service Automation</span></span> | <span data-ttu-id="63325-122">Finans</span><span class="sxs-lookup"><span data-stu-id="63325-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="63325-123">Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="63325-123">Project tasks</span></span>              | <span data-ttu-id="63325-124">Integrationsenhed for projekttimeestimater</span><span class="sxs-lookup"><span data-stu-id="63325-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="63325-125">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="63325-125">Entity flow</span></span>

<span data-ttu-id="63325-126">Projekttimeestimater administreres i Project Service Automation, og de synkroniseres med Finance som projekttimebudgetter.</span><span class="sxs-lookup"><span data-stu-id="63325-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="63325-127">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="63325-127">Prerequisites</span></span>

<span data-ttu-id="63325-128">Før der kan foretages synkronisering af projekttimeestimater, skal du synkronisere projekter, projektopgaver og posteringskategorier for projektudgifter.</span><span class="sxs-lookup"><span data-stu-id="63325-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="63325-129">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="63325-129">Power Query</span></span>

<span data-ttu-id="63325-130">I skabelonen til projekttimeestimater skal du bruge Microsoft Power-forespørgsel til Excel til at udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="63325-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="63325-131">Angiv det standardbudgetmodel-id, der skal bruges, når integrationen opretter nye timebudgetter.</span><span class="sxs-lookup"><span data-stu-id="63325-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="63325-132">Frafiltrer eventuelle ressourcespecifikke poster i opgaven, som vil få integrationen med timebudgetter til at mislykkes.</span><span class="sxs-lookup"><span data-stu-id="63325-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="63325-133">Frafiltrere tomme posteringskategorirækker.</span><span class="sxs-lookup"><span data-stu-id="63325-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="63325-134">Hvis denne opgave ikke kan fuldføres, kan det resultere i forkerte timebudgetter.</span><span class="sxs-lookup"><span data-stu-id="63325-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="63325-135">Angiv standardbudgetmodel-id'et.</span><span class="sxs-lookup"><span data-stu-id="63325-135">Set the default forecast model ID</span></span>

<span data-ttu-id="63325-136">Du kan opdatere standardbudgetmodel-id'et i skabelonen ved at klikke på **Tilknyt**-pilen for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="63325-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="63325-137">Vælg derefter linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="63325-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="63325-138">Hvis du bruger standardskabelonen Projekttimeestimater (PSA til Fin and Ops), skal du vælge **Indsat betingelse** på listen over **Anvendte trin**.</span><span class="sxs-lookup"><span data-stu-id="63325-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="63325-139">I posten **Funktion** skal du erstatte **O_\_forecast** med navnet på det budgetmodel-id, der skal bruges sammen med integrationen.</span><span class="sxs-lookup"><span data-stu-id="63325-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="63325-140">Standardskabelonen har et budgetmodel-id fra demodataene.</span><span class="sxs-lookup"><span data-stu-id="63325-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="63325-141">Hvis du opretter en ny skabelon, skal du tilføje denne kolonne.</span><span class="sxs-lookup"><span data-stu-id="63325-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="63325-142">I Power-forespørgslen skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="63325-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="63325-143">Angiv betingelsen for kolonne, hvor hvis Projektopgave ikke er null, så \<enter the forecast model ID\>; else null.</span><span class="sxs-lookup"><span data-stu-id="63325-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="63325-144">Frafiltrere ressourcespecifikke poster</span><span class="sxs-lookup"><span data-stu-id="63325-144">Filter out resource-specific records</span></span>

<span data-ttu-id="63325-145">Skabelonen Projekttimeestimater (PSA til Fin and Ops) indeholder et standardfilter, der fjerner eventuelle ressourcespecifikke poster.</span><span class="sxs-lookup"><span data-stu-id="63325-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="63325-146">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="63325-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="63325-147">Vælg linket **Avanceret forespørgsel og filtrering** for at filtrere på kolonnen **msdyn\_islinetask**, så kun **falske** poster medtages.</span><span class="sxs-lookup"><span data-stu-id="63325-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="63325-148">Frafiltrere tomme posteringskategorirækker</span><span class="sxs-lookup"><span data-stu-id="63325-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="63325-149">Du skal tilføje et filter for at fjerne rækker, der har tomme posteringskategorier.</span><span class="sxs-lookup"><span data-stu-id="63325-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="63325-150">Denne opgave er påkrævet, uanset om du bruger standardskabelonen eller opretter din egen skabelon.</span><span class="sxs-lookup"><span data-stu-id="63325-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="63325-151">Dette filter fjerner eventuelle oversigtsrækker fra Project Service Automation, der kan forårsage, at timebudgetterne i Finance bliver forkerte.</span><span class="sxs-lookup"><span data-stu-id="63325-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="63325-152">Vælg linket **Avanceret forespørgsel og filtrering** for at frafiltrere null-poster i kolonnen **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="63325-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="63325-153">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="63325-153">Template mapping in Data integration</span></span>

<span data-ttu-id="63325-154">Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="63325-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="63325-155">Tilknytningen viser de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="63325-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="63325-156">[![Tilknytning af skabelon](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="63325-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="63325-157">Projektudgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="63325-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="63325-158">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="63325-158">Template and tasks</span></span>

<span data-ttu-id="63325-159">Følgende skabeloner og underliggende opgaver bruges til at synkronisere projektudgiftsestimater fra Project Service Automation med Finance:</span><span class="sxs-lookup"><span data-stu-id="63325-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="63325-160">**Navn på skabelonen i dataintegration:** Projektudgiftsestimater (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="63325-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="63325-161">**Navnet på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="63325-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="63325-162">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="63325-162">Transaction relationships</span></span> 
    - <span data-ttu-id="63325-163">Udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="63325-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="63325-164">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="63325-164">Entity set</span></span>

| <span data-ttu-id="63325-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="63325-165">Project Service Automation</span></span> | <span data-ttu-id="63325-166">Finans</span><span class="sxs-lookup"><span data-stu-id="63325-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="63325-167">Transaktionsforbindelser</span><span class="sxs-lookup"><span data-stu-id="63325-167">Transaction Connections</span></span>    | <span data-ttu-id="63325-168">Integrationsenhed for relationer for projekttransaktion</span><span class="sxs-lookup"><span data-stu-id="63325-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="63325-169">Estimatlinjer</span><span class="sxs-lookup"><span data-stu-id="63325-169">Estimate Lines</span></span>             | <span data-ttu-id="63325-170">Integrationsenhed for projektudgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="63325-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="63325-171">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="63325-171">Entity flow</span></span>

<span data-ttu-id="63325-172">Projektudgiftsestimater administreres i Project Service Automation, og de synkroniseres med Finance som projektudgiftsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="63325-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="63325-173">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="63325-173">Prerequisites</span></span>

<span data-ttu-id="63325-174">Før der kan foretages synkronisering af projektudgiftsestimater, skal du synkronisere projekter, projektopgaver og transaktionskategorier for projektudgifter.</span><span class="sxs-lookup"><span data-stu-id="63325-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="63325-175">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="63325-175">Power Query</span></span>

<span data-ttu-id="63325-176">I skabelonen til projektudgiftsestimater skal du skal bruge Power-forespørgsel til at udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="63325-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="63325-177">Filtrere for kun at medtage linjeposter med udgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="63325-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="63325-178">Angiv det standardbudgetmodel-id, der skal bruges, når integrationen opretter nye timebudgetter.</span><span class="sxs-lookup"><span data-stu-id="63325-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="63325-179">Transformere faktureringstyperne.</span><span class="sxs-lookup"><span data-stu-id="63325-179">Transform the billing types.</span></span>
- <span data-ttu-id="63325-180">Transformere transaktionstyperne.</span><span class="sxs-lookup"><span data-stu-id="63325-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="63325-181">Filtrere for kun at medtage udgiftsestimatlinjer</span><span class="sxs-lookup"><span data-stu-id="63325-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="63325-182">Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) har et standardfilter, der kun medtager udgiftslinjer i integrationen.</span><span class="sxs-lookup"><span data-stu-id="63325-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="63325-183">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="63325-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="63325-184">Vælg opgaven **Transaktionsrelationer**, og klik derefter på pilen **Tilknyt** for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="63325-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="63325-185">Vælg linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="63325-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="63325-186">Filtrer på kolonnen **msdyn\_transactiontype1** for kun at medtage **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="63325-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="63325-187">Angiv standardbudgetmodel-id'et.</span><span class="sxs-lookup"><span data-stu-id="63325-187">Set the default forecast model ID</span></span>

<span data-ttu-id="63325-188">Du kan opdatere standardbudgetmodel-id'et i skabelonen ved at vælge opgaven **Udgiftsestimater** og derefter klikke på pilen **Tilknyt** for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="63325-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="63325-189">Vælg linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="63325-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="63325-190">Hvis du bruger standardskabelonen Projektudgiftsestimater (PSA til Fin and Ops), skal du i Power-forespørgsel først vælge **Indsat betingelse** i sektionen **Anvendte trin**.</span><span class="sxs-lookup"><span data-stu-id="63325-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="63325-191">I posten **Funktion** skal du erstatte **O_\_forecast** med navnet på det budgetmodel-id, der skal bruges sammen med integrationen.</span><span class="sxs-lookup"><span data-stu-id="63325-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="63325-192">Standardskabelonen har et budgetmodel-id fra demodataene.</span><span class="sxs-lookup"><span data-stu-id="63325-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="63325-193">Hvis du opretter en ny skabelon, skal du tilføje denne kolonne.</span><span class="sxs-lookup"><span data-stu-id="63325-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="63325-194">I Power-forespørgslen skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="63325-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="63325-195">Angiv betingelsen for den kolonne, hvor hvis Estimatlinje-id ikke er null, så \<enter the forecast model ID\>; else null.</span><span class="sxs-lookup"><span data-stu-id="63325-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="63325-196">Transformere faktureringstyperne</span><span class="sxs-lookup"><span data-stu-id="63325-196">Transform the billing types</span></span>

<span data-ttu-id="63325-197">Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) indeholder en betinget kolonne, der bruges til at transformere de faktureringstyper, der modtages fra Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="63325-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="63325-198">Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne.</span><span class="sxs-lookup"><span data-stu-id="63325-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="63325-199">Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="63325-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="63325-200">Angiv et navn til den nye kolonne, f.eks. **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="63325-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="63325-201">Angiv derefter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="63325-201">Then enter the following condition:</span></span>

<span data-ttu-id="63325-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="63325-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="63325-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="63325-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="63325-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="63325-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="63325-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="63325-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="63325-206">Transformere transaktionstyperne</span><span class="sxs-lookup"><span data-stu-id="63325-206">Transform the transaction types</span></span>

<span data-ttu-id="63325-207">Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) indeholder en betinget kolonne, der bruges til at transformere de transaktionstyper, der modtages fra Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="63325-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="63325-208">Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne.</span><span class="sxs-lookup"><span data-stu-id="63325-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="63325-209">Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="63325-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="63325-210">Angiv et navn til den nye kolonne, f.eks. **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="63325-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="63325-211">Angiv derefter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="63325-211">Then enter the following condition:</span></span>

<span data-ttu-id="63325-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="63325-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="63325-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="63325-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="63325-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="63325-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="63325-215">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="63325-215">Template mapping in Data integration</span></span>

<span data-ttu-id="63325-216">Følgende illustrationer viser eksempler på skabelonopgavetilknytningerne i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="63325-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="63325-217">Tilknytningen viser de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="63325-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="63325-218">[![Tilknytning af skabelon](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="63325-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="63325-219">[![Tilknytning af skabelon](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="63325-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
