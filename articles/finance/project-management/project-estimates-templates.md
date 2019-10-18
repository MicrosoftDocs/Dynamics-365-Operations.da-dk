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
ms.openlocfilehash: 3b885610ac9ca8645358ba8ab6d46ab82143a534
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250478"
---
# <a name="synchronize-project-estimates-directly-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="7f808-103">Synkronisere projektestimater direkte fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7f808-103">Synchronize project estimates directly from Project Service Automation to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="7f808-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projekttimeestimater og projektudgiftsestimater direkte fra Dynamics 365 Project Service Automation til Dynamics 365 Finance.</span><span class="sxs-lookup"><span data-stu-id="7f808-104">This topic describes the templates and underlying tasks that are used to synchronize project hour estimates and project expense estimates directly from Dynamics 365 Project Service Automation to Dynamics 365 Finance.</span></span>

> [!NOTE]
> - <span data-ttu-id="7f808-105">Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i version 8.0.</span><span class="sxs-lookup"><span data-stu-id="7f808-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in version 8.0.</span></span>
> - <span data-ttu-id="7f808-106">Integration af faktiske oplysninger er tilgængelig i version 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="7f808-106">Actuals integration is available in version 8.0.1 or later.</span></span>

## <a name="data-flow-for-project-service-automation-to-finance"></a><span data-ttu-id="7f808-107">Dataflow for Project Service Automation til Finance</span><span class="sxs-lookup"><span data-stu-id="7f808-107">Data flow for Project Service Automation to Finance</span></span>

<span data-ttu-id="7f808-108">Løsningen til integration af Project Service Automation og Finance bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="7f808-108">The Project Service Automation to Finance integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance.</span></span> <span data-ttu-id="7f808-109">Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om projekttimeestimater og projektudgiftsestimater fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="7f808-109">The integration templates that are available with the Data integration feature enable the flow of data about project hour estimates and project expense estimates from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7f808-110">I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance.</span><span class="sxs-lookup"><span data-stu-id="7f808-110">The following illustration shows how the data is synchronized between Project Service Automation and Finance.</span></span>

<span data-ttu-id="7f808-111">[![Dataflow for Project Service Automation-integration med Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="7f808-111">[![Data flow for Project Service Automation integration with Finance](./media/ProjectEstimatesFlow.png)](./media/ProjectEstimatesFlow.png)</span></span>

## <a name="project-hour-estimates"></a><span data-ttu-id="7f808-112">Projekttimeestimater</span><span class="sxs-lookup"><span data-stu-id="7f808-112">Project hour estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7f808-113">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="7f808-113">Template and tasks</span></span>

<span data-ttu-id="7f808-114">Du kan få adgang til de tilgængelige skabeloner ved i Microsoft PowerApps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="7f808-114">To access the available templates, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7f808-115">Følgende skabeloner og underliggende opgaver bruges til at synkronisere projekttimeestimater fra Project Service Automation med Finance:</span><span class="sxs-lookup"><span data-stu-id="7f808-115">The following template and underlying tasks are used to synchronize project hour estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7f808-116">**Navn på skabelonen i dataintegration:** Projekttimeestimater (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="7f808-116">**Name of the template in Data integration:** Project hour estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7f808-117">**Navnet på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="7f808-117">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7f808-118">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="7f808-118">Transaction relationships</span></span>
    - <span data-ttu-id="7f808-119">Udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="7f808-119">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7f808-120">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="7f808-120">Entity set</span></span>

| <span data-ttu-id="7f808-121">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7f808-121">Project Service Automation</span></span> | <span data-ttu-id="7f808-122">Finans</span><span class="sxs-lookup"><span data-stu-id="7f808-122">Finance</span></span>                                       |
|----------------------------|-----------------------------------------------|
| <span data-ttu-id="7f808-123">Projektopgaver</span><span class="sxs-lookup"><span data-stu-id="7f808-123">Project tasks</span></span>              | <span data-ttu-id="7f808-124">Integrationsenhed for projekttimeestimater</span><span class="sxs-lookup"><span data-stu-id="7f808-124">Integration entity for project hour estimates</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="7f808-125">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="7f808-125">Entity flow</span></span>

<span data-ttu-id="7f808-126">Projekttimeestimater administreres i Project Service Automation, og de synkroniseres med Finance som projekttimebudgetter.</span><span class="sxs-lookup"><span data-stu-id="7f808-126">Project hour estimates are managed in Project Service Automation, and they are synchronized to Finance as project hour forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7f808-127">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="7f808-127">Prerequisites</span></span>

<span data-ttu-id="7f808-128">Før der kan foretages synkronisering af projekttimeestimater, skal du synkronisere projekter, projektopgaver og posteringskategorier for projektudgifter.</span><span class="sxs-lookup"><span data-stu-id="7f808-128">Before synchronization of project hour estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7f808-129">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="7f808-129">Power Query</span></span>

<span data-ttu-id="7f808-130">I skabelonen til projekttimeestimater skal du bruge Microsoft Power-forespørgsel til Excel til at udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="7f808-130">In the project hour estimates template, you must use Microsoft Power Query for Excel to complete these tasks:</span></span>

- <span data-ttu-id="7f808-131">Angiv det standardbudgetmodel-id, der skal bruges, når integrationen opretter nye timebudgetter.</span><span class="sxs-lookup"><span data-stu-id="7f808-131">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7f808-132">Frafiltrer eventuelle ressourcespecifikke poster i opgaven, som vil få integrationen med timebudgetter til at mislykkes.</span><span class="sxs-lookup"><span data-stu-id="7f808-132">Filter out any resource-specific records in the task that will fail the integration into hour forecasts.</span></span>
- <span data-ttu-id="7f808-133">Frafiltrere tomme posteringskategorirækker.</span><span class="sxs-lookup"><span data-stu-id="7f808-133">Filter out any empty transaction category rows.</span></span> <span data-ttu-id="7f808-134">Hvis denne opgave ikke kan fuldføres, kan det resultere i forkerte timebudgetter.</span><span class="sxs-lookup"><span data-stu-id="7f808-134">Failure to complete this task might result in incorrect hour forecasts.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7f808-135">Angiv standardbudgetmodel-id'et.</span><span class="sxs-lookup"><span data-stu-id="7f808-135">Set the default forecast model ID</span></span>

<span data-ttu-id="7f808-136">Du kan opdatere standardbudgetmodel-id'et i skabelonen ved at klikke på **Tilknyt**-pilen for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="7f808-136">To update the default forecast model ID in the template, click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7f808-137">Vælg derefter linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="7f808-137">Then select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7f808-138">Hvis du bruger standardskabelonen Projekttimeestimater (PSA til Fin and Ops), skal du vælge **Indsat betingelse** på listen over **Anvendte trin**.</span><span class="sxs-lookup"><span data-stu-id="7f808-138">If you're using the default Project hour estimates (PSA to Fin and Ops) template, select the **Inserted Condition** in the list of **Applied Steps**.</span></span> <span data-ttu-id="7f808-139">I posten **Funktion** skal du erstatte **O_\_forecast** med navnet på det budgetmodel-id, der skal bruges sammen med integrationen.</span><span class="sxs-lookup"><span data-stu-id="7f808-139">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7f808-140">Standardskabelonen har et budgetmodel-id fra demodataene.</span><span class="sxs-lookup"><span data-stu-id="7f808-140">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7f808-141">Hvis du opretter en ny skabelon, skal du tilføje denne kolonne.</span><span class="sxs-lookup"><span data-stu-id="7f808-141">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7f808-142">I Power-forespørgslen skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="7f808-142">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7f808-143">Angiv betingelsen for kolonne, hvor hvis Projektopgave ikke er null, så \<enter the forecast model ID\>; else null.</span><span class="sxs-lookup"><span data-stu-id="7f808-143">Enter the condition for the column, where, if Project task is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="filter-out-resource-specific-records"></a><span data-ttu-id="7f808-144">Frafiltrere ressourcespecifikke poster</span><span class="sxs-lookup"><span data-stu-id="7f808-144">Filter out resource-specific records</span></span>

<span data-ttu-id="7f808-145">Skabelonen Projekttimeestimater (PSA til Fin and Ops) indeholder et standardfilter, der fjerner eventuelle ressourcespecifikke poster.</span><span class="sxs-lookup"><span data-stu-id="7f808-145">The Project hour estimates (PSA to Fin and Ops) template has a default filter that removes any resource-specific records.</span></span> <span data-ttu-id="7f808-146">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="7f808-146">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7f808-147">Vælg linket **Avanceret forespørgsel og filtrering** for at filtrere på kolonnen **msdyn\_islinetask**, så kun **falske** poster medtages.</span><span class="sxs-lookup"><span data-stu-id="7f808-147">Select the **Advanced Query and Filtering** link to filter on the **msdyn\_islinetask** column so that only **False** records are included.</span></span>

#### <a name="filter-out-empty-transaction-category-rows"></a><span data-ttu-id="7f808-148">Frafiltrere tomme posteringskategorirækker</span><span class="sxs-lookup"><span data-stu-id="7f808-148">Filter out empty transaction category rows</span></span>

<span data-ttu-id="7f808-149">Du skal tilføje et filter for at fjerne rækker, der har tomme posteringskategorier.</span><span class="sxs-lookup"><span data-stu-id="7f808-149">You must add a filter to remove any rows that have empty transaction categories.</span></span> <span data-ttu-id="7f808-150">Denne opgave er påkrævet, uanset om du bruger standardskabelonen eller opretter din egen skabelon.</span><span class="sxs-lookup"><span data-stu-id="7f808-150">This task is required, regardless of whether you're using the default template or creating your own template.</span></span> <span data-ttu-id="7f808-151">Dette filter fjerner eventuelle oversigtsrækker fra Project Service Automation, der kan forårsage, at timebudgetterne i Finance bliver forkerte.</span><span class="sxs-lookup"><span data-stu-id="7f808-151">This filter removes any summary rows from Project Service Automation that might cause the hour forecasts in Finance to be incorrect.</span></span> <span data-ttu-id="7f808-152">Vælg linket **Avanceret forespørgsel og filtrering** for at frafiltrere null-poster i kolonnen **msdyn\_transactioncategory\_value**.</span><span class="sxs-lookup"><span data-stu-id="7f808-152">Select **Advanced Query and Filtering** link to filter out null records in the **msdyn\_transactioncategory\_value** column.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7f808-153">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="7f808-153">Template mapping in Data integration</span></span>

<span data-ttu-id="7f808-154">Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="7f808-154">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="7f808-155">Tilknytningen viser de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="7f808-155">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7f808-156">[![Tilknytning af skabelon](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7f808-156">[![Template mapping](./media/ProjectHourEstimatesMapping.jpg)](./media/ProjectHourEstimatesMapping.jpg)</span></span>

## <a name="project-expense-estimates"></a><span data-ttu-id="7f808-157">Projektudgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="7f808-157">Project expense estimates</span></span>

### <a name="template-and-tasks"></a><span data-ttu-id="7f808-158">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="7f808-158">Template and tasks</span></span>

<span data-ttu-id="7f808-159">Følgende skabeloner og underliggende opgaver bruges til at synkronisere projektudgiftsestimater fra Project Service Automation med Finance:</span><span class="sxs-lookup"><span data-stu-id="7f808-159">The following template and underlying tasks are used to synchronize project expense estimates from Project Service Automation to Finance:</span></span>

- <span data-ttu-id="7f808-160">**Navn på skabelonen i dataintegration:** Projektudgiftsestimater (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="7f808-160">**Name of the template in Data integration:** Project expense estimates (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="7f808-161">**Navnet på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="7f808-161">**Name of the tasks in the project:**</span></span>

    - <span data-ttu-id="7f808-162">Transaktionsrelationer</span><span class="sxs-lookup"><span data-stu-id="7f808-162">Transaction relationships</span></span> 
    - <span data-ttu-id="7f808-163">Udgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="7f808-163">Expense estimates</span></span>

### <a name="entity-set"></a><span data-ttu-id="7f808-164">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="7f808-164">Entity set</span></span>

| <span data-ttu-id="7f808-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="7f808-165">Project Service Automation</span></span> | <span data-ttu-id="7f808-166">Finans</span><span class="sxs-lookup"><span data-stu-id="7f808-166">Finance</span></span>                                                  |
|----------------------------|----------------------------------------------------------|
| <span data-ttu-id="7f808-167">Transaktionsforbindelser</span><span class="sxs-lookup"><span data-stu-id="7f808-167">Transaction Connections</span></span>    | <span data-ttu-id="7f808-168">Integrationsenhed for relationer for projekttransaktion</span><span class="sxs-lookup"><span data-stu-id="7f808-168">Integration entity for project transaction relationships</span></span> |
| <span data-ttu-id="7f808-169">Estimatlinjer</span><span class="sxs-lookup"><span data-stu-id="7f808-169">Estimate Lines</span></span>             | <span data-ttu-id="7f808-170">Integrationsenhed for projektudgiftsestimater</span><span class="sxs-lookup"><span data-stu-id="7f808-170">Integration entity for project expense estimates</span></span>         |

### <a name="entity-flow"></a><span data-ttu-id="7f808-171">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="7f808-171">Entity flow</span></span>

<span data-ttu-id="7f808-172">Projektudgiftsestimater administreres i Project Service Automation, og de synkroniseres med Finance som projektudgiftsbudgetter.</span><span class="sxs-lookup"><span data-stu-id="7f808-172">Project expense estimates are managed in Project Service Automation, and they are synchronized to Finance as project expense forecasts.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="7f808-173">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="7f808-173">Prerequisites</span></span>

<span data-ttu-id="7f808-174">Før der kan foretages synkronisering af projektudgiftsestimater, skal du synkronisere projekter, projektopgaver og transaktionskategorier for projektudgifter.</span><span class="sxs-lookup"><span data-stu-id="7f808-174">Before synchronization of project expense estimates can occur, you must synchronize projects, project tasks, and project expense transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="7f808-175">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="7f808-175">Power Query</span></span>

<span data-ttu-id="7f808-176">I skabelonen til projektudgiftsestimater skal du skal bruge Power-forespørgsel til at udføre følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="7f808-176">In the project expense estimates template, you must use Power Query to complete the following tasks:</span></span>

- <span data-ttu-id="7f808-177">Filtrere for kun at medtage linjeposter med udgiftsestimater.</span><span class="sxs-lookup"><span data-stu-id="7f808-177">Filter to include only expense estimate line records.</span></span>
- <span data-ttu-id="7f808-178">Angiv det standardbudgetmodel-id, der skal bruges, når integrationen opretter nye timebudgetter.</span><span class="sxs-lookup"><span data-stu-id="7f808-178">Set the default forecast model ID that will be used when the integration creates new hour forecasts.</span></span>
- <span data-ttu-id="7f808-179">Transformere faktureringstyperne.</span><span class="sxs-lookup"><span data-stu-id="7f808-179">Transform the billing types.</span></span>
- <span data-ttu-id="7f808-180">Transformere transaktionstyperne.</span><span class="sxs-lookup"><span data-stu-id="7f808-180">Transform the transaction types.</span></span>

#### <a name="filter-to-include-only-expense-estimate-lines"></a><span data-ttu-id="7f808-181">Filtrere for kun at medtage udgiftsestimatlinjer</span><span class="sxs-lookup"><span data-stu-id="7f808-181">Filter to include only expense estimate lines</span></span>

<span data-ttu-id="7f808-182">Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) har et standardfilter, der kun medtager udgiftslinjer i integrationen.</span><span class="sxs-lookup"><span data-stu-id="7f808-182">The Project expense estimates (PSA to Fin and Ops) template has a default filter that includes only expense lines in the integration.</span></span> <span data-ttu-id="7f808-183">Hvis du opretter din egen skabelon, skal du tilføje dette filter.</span><span class="sxs-lookup"><span data-stu-id="7f808-183">If you create your own template, you must add this filter.</span></span> <span data-ttu-id="7f808-184">Vælg opgaven **Transaktionsrelationer**, og klik derefter på pilen **Tilknyt** for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="7f808-184">Select the **Transaction relationships** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7f808-185">Vælg linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="7f808-185">Select the **Advanced Query and Filtering** link.</span></span> <span data-ttu-id="7f808-186">Filtrer på kolonnen **msdyn\_transactiontype1** for kun at medtage **msdyn\_estimateline**.</span><span class="sxs-lookup"><span data-stu-id="7f808-186">Filter the **msdyn\_transactiontype1** column so that it includes only **msdyn\_estimateline**.</span></span>

#### <a name="set-the-default-forecast-model-id"></a><span data-ttu-id="7f808-187">Angiv standardbudgetmodel-id'et.</span><span class="sxs-lookup"><span data-stu-id="7f808-187">Set the default forecast model ID</span></span>

<span data-ttu-id="7f808-188">Du kan opdatere standardbudgetmodel-id'et i skabelonen ved at vælge opgaven **Udgiftsestimater** og derefter klikke på pilen **Tilknyt** for at åbne tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="7f808-188">To update the default forecast model ID in the template, select the **Expense estimates** task, and then click the **Map** arrow to open the mapping.</span></span> <span data-ttu-id="7f808-189">Vælg linket **Avanceret forespørgsel og filtrering**.</span><span class="sxs-lookup"><span data-stu-id="7f808-189">Select the **Advanced Query and Filtering** link.</span></span>

- <span data-ttu-id="7f808-190">Hvis du bruger standardskabelonen Projektudgiftsestimater (PSA til Fin and Ops), skal du i Power-forespørgsel først vælge **Indsat betingelse** i sektionen **Anvendte trin**.</span><span class="sxs-lookup"><span data-stu-id="7f808-190">If you're using the default Project expense estimates (PSA to Fin and Ops) template, in Power Query, select the first **Inserted Condition** from the **Applied Steps** section.</span></span> <span data-ttu-id="7f808-191">I posten **Funktion** skal du erstatte **O_\_forecast** med navnet på det budgetmodel-id, der skal bruges sammen med integrationen.</span><span class="sxs-lookup"><span data-stu-id="7f808-191">In the **Function** entry, replace **O\_forecast** with the name of the forecast model ID that should be used with the integration.</span></span> <span data-ttu-id="7f808-192">Standardskabelonen har et budgetmodel-id fra demodataene.</span><span class="sxs-lookup"><span data-stu-id="7f808-192">The default template has a forecast model ID from the demo data.</span></span>
- <span data-ttu-id="7f808-193">Hvis du opretter en ny skabelon, skal du tilføje denne kolonne.</span><span class="sxs-lookup"><span data-stu-id="7f808-193">If you're creating a new template, you must add this column.</span></span> <span data-ttu-id="7f808-194">I Power-forespørgslen skal du vælge **Tilføj betinget kolonne** og angiv et navn til den nye kolonne, f.eks. **ModelID**.</span><span class="sxs-lookup"><span data-stu-id="7f808-194">In Power Query, select **Add Conditional Column**, and enter a name for the new column, such as **ModelID**.</span></span> <span data-ttu-id="7f808-195">Angiv betingelsen for den kolonne, hvor hvis Estimatlinje-id ikke er null, så \<enter the forecast model ID\>; else null.</span><span class="sxs-lookup"><span data-stu-id="7f808-195">Enter the condition for the column, where, if Estimate line ID is not null, then \<enter the forecast model ID\>; else null.</span></span>

#### <a name="transform-the-billing-types"></a><span data-ttu-id="7f808-196">Transformere faktureringstyperne</span><span class="sxs-lookup"><span data-stu-id="7f808-196">Transform the billing types</span></span>

<span data-ttu-id="7f808-197">Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) indeholder en betinget kolonne, der bruges til at transformere de faktureringstyper, der modtages fra Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="7f808-197">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the billing types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7f808-198">Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne.</span><span class="sxs-lookup"><span data-stu-id="7f808-198">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7f808-199">Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="7f808-199">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7f808-200">Angiv et navn til den nye kolonne, f.eks. **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="7f808-200">Enter a name for the new column, such as **BillingType**.</span></span> <span data-ttu-id="7f808-201">Angiv derefter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="7f808-201">Then enter the following condition:</span></span>

<span data-ttu-id="7f808-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span><span class="sxs-lookup"><span data-stu-id="7f808-202">If **msdyn\_billingtype** = 192350000, then **NonChargeable**</span></span>  
<span data-ttu-id="7f808-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span><span class="sxs-lookup"><span data-stu-id="7f808-203">else if **msdyn\_billingtype** = 192350001, then **Chargeable**</span></span>  
<span data-ttu-id="7f808-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span><span class="sxs-lookup"><span data-stu-id="7f808-204">else if **msdyn\_billingtype** = 192350002, then **Complimentary**</span></span>  
<span data-ttu-id="7f808-205">else **NotAvailable**</span><span class="sxs-lookup"><span data-stu-id="7f808-205">else **NotAvailable**</span></span>

#### <a name="transform-the-transaction-types"></a><span data-ttu-id="7f808-206">Transformere transaktionstyperne</span><span class="sxs-lookup"><span data-stu-id="7f808-206">Transform the transaction types</span></span>

<span data-ttu-id="7f808-207">Skabelonen Projektudgiftsestimater (PSA til Fin and Ops) indeholder en betinget kolonne, der bruges til at transformere de transaktionstyper, der modtages fra Project Service Automation under integrationen.</span><span class="sxs-lookup"><span data-stu-id="7f808-207">The Project expense estimates (PSA to Fin and Ops) template includes a conditional column that is used to transform the transaction types that are received from Project Service Automation during the integration.</span></span> <span data-ttu-id="7f808-208">Hvis du opretter din egen skabelon, skal du tilføje denne betingede kolonne.</span><span class="sxs-lookup"><span data-stu-id="7f808-208">If you create your own template, you must add this conditional column.</span></span> <span data-ttu-id="7f808-209">Vælg linket **Avanceret forespørgsel og filtrering**, og vælg derefter **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="7f808-209">Select the **Advanced Query and Filtering** link and then select **Add Conditional Column**.</span></span> <span data-ttu-id="7f808-210">Angiv et navn til den nye kolonne, f.eks. **TransactionType**.</span><span class="sxs-lookup"><span data-stu-id="7f808-210">Enter a name for the new column, such as **TransactionType**.</span></span> <span data-ttu-id="7f808-211">Angiv derefter følgende betingelse:</span><span class="sxs-lookup"><span data-stu-id="7f808-211">Then enter the following condition:</span></span>

<span data-ttu-id="7f808-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span><span class="sxs-lookup"><span data-stu-id="7f808-212">If **msdyn\_transactiontypecode** = 192350000, then **Cost**</span></span>  
<span data-ttu-id="7f808-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span><span class="sxs-lookup"><span data-stu-id="7f808-213">else if **msdyn\_transactiontypecode** = 192350005, then **Sales**</span></span>  
<span data-ttu-id="7f808-214">else **null**</span><span class="sxs-lookup"><span data-stu-id="7f808-214">else **null**</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7f808-215">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="7f808-215">Template mapping in Data integration</span></span>

<span data-ttu-id="7f808-216">Følgende illustrationer viser eksempler på skabelonopgavetilknytningerne i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="7f808-216">The following illustrations show examples of the template task mappings in Data integration.</span></span> <span data-ttu-id="7f808-217">Tilknytningen viser de feltoplysninger, der synkroniseres fra Project Service Automation til Finance.</span><span class="sxs-lookup"><span data-stu-id="7f808-217">The mapping shows the field information that will be synchronized from Project Service Automation to Finance.</span></span>

<span data-ttu-id="7f808-218">[![Tilknytning af skabelon](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7f808-218">[![Template mapping](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)](./media/ExpenseEstimateTransactionRelationshipsMapping.jpg)</span></span>

<span data-ttu-id="7f808-219">[![Tilknytning af skabelon](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="7f808-219">[![Template mapping](./media/ExpenseEstimatesMapping.jpg)](./media/ExpenseEstimatesMapping.jpg)</span></span>
