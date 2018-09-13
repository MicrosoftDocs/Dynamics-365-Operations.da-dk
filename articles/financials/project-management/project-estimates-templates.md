---
title: Synkronisere projektestimater direkte fra Project Service Automation til Finance and Operations
description: I dette emne beskrives skabelonerne og de underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation med Microsoft Dynamics 365 for Finance and Operations.
author: KimANelson
manager: AnnBe
ms.date: 07/20/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.custom: 87983
ms.assetid: b454ad57-2fd6-46c9-a77e-646de4153067
ms.search.region: Global
ms.author: knelson
ms.search.validFrom: 2016-11-28
ms.dyn365.ops.version: AX 7.3.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 21338b889e0377dbfd5adfd461ea81b39a75baf8
ms.contentlocale: da-dk
ms.lasthandoff: 08/08/2018

---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="60180-103">Synkronisere projektestimater direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60180-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="60180-104">I dette emne beskrives skabelonerne og de underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Microsoft Dynamics 365 for Project Service Automation med Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="60180-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Microsoft Dynamics 365 for Project Service Automation to Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="60180-105">Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelige i Microsoft Dynamics 365 for Finance and Operations version 8.0.</span><span class="sxs-lookup"><span data-stu-id="60180-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="60180-106">Integration af faktiske oplysninger er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.01 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="60180-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="60180-107">Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="60180-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="60180-108">Hvis du skal nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="60180-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="60180-109">Dataflow for Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60180-109">Data flow for Project Service Automation to Finance and Operations</span></span>

<span data-ttu-id="60180-110">Løsningen til integration af Project Service Automation med Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="60180-110">The Project Service Automation to Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="60180-111">Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om projekttimeestimater og projektudgiftsestimater fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="60180-111">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="60180-112">I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="60180-112">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="60180-113">[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="60180-113">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="60180-114">Projekttimeestimater</span><span class="sxs-lookup"><span data-stu-id="60180-114">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="60180-115">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="60180-115">Template and tasks</span></span>

<span data-ttu-id="60180-116">Du kan få adgang til de tilgængelige skabeloner ved i Microsoft PowerApps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="60180-116">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="60180-117">Følgende skabeloner og underliggende opgaver bruges til at synkronisere projekttimeestimater fra Project Service Automation med Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="60180-117">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="60180-118">**Navn på skabelonen i dataintegration:** Projekttimeestimater (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="60180-118">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="60180-119">**Navnet på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="60180-119">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="60180-120">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="60180-120">Transaction relationships</span></span>
    - <span data-ttu-id="60180-121">Udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="60180-121">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="60180-122">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="60180-122">Entity set</span></span>

| <span data-ttu-id="60180-123">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="60180-123">Project Service Automation</span></span> | <span data-ttu-id="60180-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60180-124">Finance and Operations</span></span>                        |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="60180-125">Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="60180-125">Project tasks</span></span>              | <span data-ttu-id="60180-126">Integrationsenhed for projekttimeestimater</span><span class="sxs-lookup"><span data-stu-id="60180-126">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="60180-127">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="60180-127">Entity flow</span></span>

<span data-ttu-id="60180-128">Projekttimeestimater administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projekttimebudgetter.</span><span class="sxs-lookup"><span data-stu-id="60180-128">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="60180-129">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="60180-129">Prerequisites</span></span>

<span data-ttu-id="60180-130">Før der kan foretages synkronisering af projekttimeestimater, skal du synkronisere projekter, projektopgaver og posteringskategorier for projektudgifter.</span><span class="sxs-lookup"><span data-stu-id="60180-130">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="60180-131">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="60180-131">Power Query</span></span>

<span data-ttu-id="60180-132">I skabelonen til projekttimeestimater skal du bruge Microsoft Power-forespørgsel til Excel til at udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="60180-132">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="60180-133">Angiv det standardbudgetmodel-id, der skal bruges, når integrationen opretter nye timebudgetter.</span><span class="sxs-lookup"><span data-stu-id="60180-133">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="60180-134">Frafiltrer eventuelle ressourcespecifikke poster i opgaven, som vil få integrationen med timebudgetter til at mislykkes.</span><span class="sxs-lookup"><span data-stu-id="60180-134">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="60180-135">Frafiltrere tomme posteringskategorirækker.</span><span class="sxs-lookup"><span data-stu-id="60180-135">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="60180-136">Hvis denne opgave ikke kan fuldføres, kan det resultere i forkerte timebudgetter.</span><span class="sxs-lookup"><span data-stu-id="60180-136">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="60180-137">Angiv standardbudgetmodel-id'et.</span><span class="sxs-lookup"><span data-stu-id="60180-137">Set the default forecast model ID</span></span>

<span data-ttu-id="60180-138">Du kan opdatere standardbudgetmodel-id'et i skabelonen ved at klikke på **Tilknyt**-pilen for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="60180-138">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="60180-139">Vælg derefter linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="60180-139">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="60180-140">Hvis du bruger standardskabelonen Projekttimeestimater (PSA til Fin and Ops), skal du vælge **Indsat betingelse** på listen over **Anvendte trin**.</span><span class="sxs-lookup"><span data-stu-id="60180-140">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="60180-141">I posten **Funktion** skal du erstatte **O_\_forecast** med navnet på det budgetmodel-id, der skal bruges sammen med integrationen.</span><span class="sxs-lookup"><span data-stu-id="60180-141">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="60180-142">Standardskabelonen har et budgetmodel-id fra demodataene.</span><span class="sxs-lookup"><span data-stu-id="60180-142">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="60180-143">Hvis du opretter en ny skabelon, skal du tilføje denne kolonne.</span><span class="sxs-lookup"><span data-stu-id="60180-143">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="60180-144">I Power-forespørgslen skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="60180-144">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="60180-145">Angiv betingelsen for kolonne, hvor hvis Projektopgave ikke er null, så \<enter the forecast model ID\>; else null.</span><span class="sxs-lookup"><span data-stu-id="60180-145">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="60180-146">Frafiltrere ressourcespecifikke poster</span><span class="sxs-lookup"><span data-stu-id="60180-146">Filter out resource-specific records</span></span>

<span data-ttu-id="60180-147">Skabelonen Projekttimeestimater (PSA til Fin and Ops) indeholder et standardfilter, der fjerner eventuelle ressourcespecifikke poster.</span><span class="sxs-lookup"><span data-stu-id="60180-147">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="60180-148">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="60180-148">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="60180-149">Vælg linket **Avanceret forespørgsel og filtrering** for at filtrere på kolonnen **msdyn\_islinetask**, så kun **falske** poster medtages.</span><span class="sxs-lookup"><span data-stu-id="60180-149">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="60180-150">Frafiltrere tomme posteringskategorirækker</span><span class="sxs-lookup"><span data-stu-id="60180-150">Filter out empty transaction category rows</span></span>

<span data-ttu-id="60180-151">Du skal tilføje et filter for at fjerne rækker, der har tomme posteringskategorier.</span><span class="sxs-lookup"><span data-stu-id="60180-151">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="60180-152">Denne opgave er påkrævet, uanset om du bruger standardskabelonen eller opretter din egen skabelon.</span><span class="sxs-lookup"><span data-stu-id="60180-152">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="60180-153">Dette filter fjerner eventuelle oversigtsrækker fra Project Service Automation, der kan forårsage, at timebudgetterne i Finance and Operations bliver forkerte.</span><span class="sxs-lookup"><span data-stu-id="60180-153">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance and Operations to be incorrect.</span></span> <span data-ttu-id="60180-154">Vælg linket **Avanceret forespørgsel og filtrering** for at frafiltrere null-poster i kolonnen **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="60180-154">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="60180-155">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="60180-155">Template mapping in Data integration</span></span>

<span data-ttu-id="60180-156">Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="60180-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="60180-157">Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="60180-157">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="60180-158">[![Tilknytning af skabelon](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="60180-158">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="60180-159">Projektudgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="60180-159">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="60180-160">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="60180-160">Template and tasks</span></span>

<span data-ttu-id="60180-161">Følgende skabelon og underliggende opgaver bruges til at synkronisere projektudgiftsestimater fra Project Service Automation med Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="60180-161">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="60180-162">**Navn på skabelonen i dataintegration:** Projektudgiftsestimater (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="60180-162">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="60180-163">**Navnet på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="60180-163">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="60180-164">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="60180-164">Transaction relationships</span></span> 
    - <span data-ttu-id="60180-165">Udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="60180-165">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="60180-166">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="60180-166">Entity set</span></span>

| <span data-ttu-id="60180-167">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="60180-167">Project Service Automation</span></span> | <span data-ttu-id="60180-168">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="60180-168">Finance and Operations</span></span>                                   |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="60180-169">Transaktionsforbindelser</span><span class="sxs-lookup"><span data-stu-id="60180-169">Transaction Connections</span></span>    | <span data-ttu-id="60180-170">Integrationsenhed for relationer for projekttransaktion</span><span class="sxs-lookup"><span data-stu-id="60180-170">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="60180-171">Estimatlinjer</span><span class="sxs-lookup"><span data-stu-id="60180-171">Estimate Lines</span></span>             | <span data-ttu-id="60180-172">Integrationsenhed for projektudgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="60180-172">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="60180-173">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="60180-173">Entity flow</span></span>

<span data-ttu-id="60180-174">Projektudgiftsestimater administreres i Project Service Automation, og de synkroniseres med Finance and Operations som projektudgiftsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="60180-174">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance and Operations as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="60180-175">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="60180-175">Prerequisites</span></span>

<span data-ttu-id="60180-176">Før der kan foretages synkronisering af projektudgiftsestimater, skal du synkronisere projekter, projektopgaver og transaktionskategorier for projektudgifter.</span><span class="sxs-lookup"><span data-stu-id="60180-176">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="60180-177">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="60180-177">Power Query</span></span>

<span data-ttu-id="60180-178">I skabelonen til projektudgiftsestimater skal du skal bruge Power-forespørgsel til at udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="60180-178">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="60180-179">Filtrere for kun at medtage linjeposter med udgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="60180-179">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="60180-180">Angiv det standardbudgetmodel-id, der skal bruges, når integrationen opretter nye timebudgetter.</span><span class="sxs-lookup"><span data-stu-id="60180-180">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="60180-181">Transformere faktureringstyperne.</span><span class="sxs-lookup"><span data-stu-id="60180-181">Transform the billing types.</span></span>
- <span data-ttu-id="60180-182">Transformere transaktionstyperne.</span><span class="sxs-lookup"><span data-stu-id="60180-182">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="60180-183">Filtrere for kun at medtage udgiftsestimatlinjer</span><span class="sxs-lookup"><span data-stu-id="60180-183">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="60180-184">Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) har et standardfilter, der kun medtager udgiftslinjer i integrationen.</span><span class="sxs-lookup"><span data-stu-id="60180-184">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="60180-185">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="60180-185">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="60180-186">Vælg opgaven **Transaktionsrelationer**, og klik derefter på pilen **Tilknyt** for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="60180-186">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="60180-187">Vælg linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="60180-187">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="60180-188">Filtrer på kolonnen **msdyn\_transactiontype1** for kun at medtage **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="60180-188">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="60180-189">Angiv standardbudgetmodel-id'et.</span><span class="sxs-lookup"><span data-stu-id="60180-189">Set the default forecast model ID</span></span>

<span data-ttu-id="60180-190">Du kan opdatere standardbudgetmodel-id'et i skabelonen ved at vælge opgaven **Udgiftsestimater** og derefter klikke på pilen **Tilknyt** for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="60180-190">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="60180-191">Vælg linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="60180-191">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="60180-192">Hvis du bruger standardskabelonen Projektudgiftsestimater (PSA til Fin and Ops), skal du i Power-forespørgsel først vælge **Indsat betingelse** i sektionen **Anvendte trin**.</span><span class="sxs-lookup"><span data-stu-id="60180-192">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="60180-193">I posten **Funktion** skal du erstatte **O_\_forecast** med navnet på det budgetmodel-id, der skal bruges sammen med integrationen.</span><span class="sxs-lookup"><span data-stu-id="60180-193">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="60180-194">Standardskabelonen har et budgetmodel-id fra demodataene.</span><span class="sxs-lookup"><span data-stu-id="60180-194">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="60180-195">Hvis du opretter en ny skabelon, skal du tilføje denne kolonne.</span><span class="sxs-lookup"><span data-stu-id="60180-195">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="60180-196">I Power-forespørgslen skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="60180-196">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="60180-197">Angiv betingelsen for den kolonne, hvor hvis Estimatlinje-id ikke er null, så \<enter the forecast model ID\>; else null.</span><span class="sxs-lookup"><span data-stu-id="60180-197">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="60180-198">Transformere faktureringstyperne</span><span class="sxs-lookup"><span data-stu-id="60180-198">Transform the billing types</span></span>

<span data-ttu-id="60180-199">Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) indeholder en betinget kolonne, der bruges til at transformere de faktureringstyper, der modtages fra Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="60180-199">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="60180-200">Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne.</span><span class="sxs-lookup"><span data-stu-id="60180-200">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="60180-201">Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="60180-201">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="60180-202">Angiv et navn til den nye kolonne, f.eks. **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="60180-202">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="60180-203">Angiv derefter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="60180-203">Then enter the following condition:</span></span>

<span data-ttu-id="60180-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="60180-204">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="60180-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="60180-205">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="60180-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="60180-206">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="60180-207">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="60180-207">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="60180-208">Transformere transaktionstyperne</span><span class="sxs-lookup"><span data-stu-id="60180-208">Transform the transaction types</span></span>

<span data-ttu-id="60180-209">Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) indeholder en betinget kolonne, der bruges til at transformere de transaktionstyper, der modtages fra Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="60180-209">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="60180-210">Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne.</span><span class="sxs-lookup"><span data-stu-id="60180-210">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="60180-211">Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="60180-211">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="60180-212">Angiv et navn til den nye kolonne, f.eks. **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="60180-212">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="60180-213">Angiv derefter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="60180-213">Then enter the following condition:</span></span>

<span data-ttu-id="60180-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="60180-214">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="60180-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="60180-215">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="60180-216">else **null**</span><span class="sxs-lookup"><span data-stu-id="60180-216">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="60180-217">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="60180-217">Template mapping in Data integration</span></span>

<span data-ttu-id="60180-218">Følgende illustrationer viser eksempler på skabelonopgavetilknytningerne i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="60180-218">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="60180-219">Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="60180-219">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="60180-220">[![Tilknytning af skabelon](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="60180-220">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="60180-221">[![Tilknytning af skabelon](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="60180-221">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
