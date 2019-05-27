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
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1558236"
---
# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="b16e7-103">Synkronisere projektudgiftskategorier mellem Finance and Operations og Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b16e7-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="b16e7-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektudgiftskategorier mellem Microsoft Dynamics 365 for Finance and Operations og Microsoft Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b16e7-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Microsoft Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> - <span data-ttu-id="b16e7-105">Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.</span><span class="sxs-lookup"><span data-stu-id="b16e7-105">Project task integration, expense transaction categories, hour estimates, expense estimates, and functionality locking are available in Microsoft Dynamics 365 for Finance and Operations version 8.0.</span></span>
> - <span data-ttu-id="b16e7-106">Integration af faktiske oplysninger er tilgængelig i Microsoft Dynamics 365 for Finance and Operations version 8.0.1 eller nyere.</span><span class="sxs-lookup"><span data-stu-id="b16e7-106">Actuals integration is available in Microsoft Dynamics 365 for Finance and Operations version 8.0.1 or later.</span></span>
> - <span data-ttu-id="b16e7-107">Hvis du bruger Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, 7.3.0, når du har installeret KB 4132657 og KB 4132660, kan du bruge skabelonerne til at integrere projektopgaver, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og faktiske oplysninger og konfigurere låsning af funktionalitet.</span><span class="sxs-lookup"><span data-stu-id="b16e7-107">If you're using Microsoft Dynamics 365 for Finance and Operations, Enterprise edition 7.3.0, after you install KB 4132657 and KB 4132660, you will be able to use the templates to integrate project tasks, expense transaction categories, hour estimates, expense estimates, and actuals, and to configure functionality locking.</span></span> <span data-ttu-id="b16e7-108">Hvis du skal nulstille regnskabsfordelingerne, anbefaler vi, at du også installerer KB 4131710.</span><span class="sxs-lookup"><span data-stu-id="b16e7-108">If you must reset the accounting distributions, we recommend that you also install KB 4131710.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="b16e7-109">Dataflow for Project Service Automation og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b16e7-109">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="b16e7-110">Løsningen til integration af Project Service Automation og Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b16e7-110">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="b16e7-111">Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om transaktionskategorier for projektudgifter mellem Finance and Operations og Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b16e7-111">The integration templates that are available with the Data integration feature enable the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="b16e7-112">Hvis projektudgiftskategorier administreres i Finance and Operations, er integrationsflowet først fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b16e7-112">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation.</span></span> <span data-ttu-id="b16e7-113">Integrations-id'er for projektudgiftskategorier opdateres gennem synkronisering fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b16e7-113">The integration IDs of the project expense categories are then updated through synchronization from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="b16e7-114">Hvis projektudgiftskategorier administreres i Project Service Automation, er integrationsflowet først fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b16e7-114">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="b16e7-115">Projektkategorier skal allerede være konfigureret i Finance and Operations før synkroniseringen fra Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b16e7-115">The project categories must already be configured in Finance and Operations before the synchronization from Project Service Automation.</span></span> <span data-ttu-id="b16e7-116">Derefter synkroniseres fra Finance and Operations til Project Service Automation og derefter fra Project Service Automation til Finance and Operations igen.</span><span class="sxs-lookup"><span data-stu-id="b16e7-116">Then synchronize from Finance and Operations back to Project Service Automation, and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="b16e7-117">På denne måde kan du hjælpe med til at sikre, at kategorierne sammenkædes, og at der ikke oprettes dubletter.</span><span class="sxs-lookup"><span data-stu-id="b16e7-117">In this way, you help guarantee that the categories are linked, and that no duplicates are created.</span></span>

> [!NOTE]
> <span data-ttu-id="b16e7-118">Projektudgiftskategorierne håndteres typisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b16e7-118">Typically, the project expense categories are mastered in Finance and Operations.</span></span> <span data-ttu-id="b16e7-119">Men hvis de ikke styres i Finance and Operations, eller hvis udgiftskategorierne allerede er oprettet i Project Service Automation, skal du først synkronisere ved hjælp af skabelonen Transaktionskategorier for projektudgifter (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="b16e7-119">However, if they aren't mastered in Finance and Operations, or if expense categories have already been created in Project Service Automation, you must first synchronize by using the Project expense transaction categories (PSA to Fin and Ops) template.</span></span> <span data-ttu-id="b16e7-120">Derefter skal du synkronisere ved hjælp af skabelonen Transaktionskategorier for projektudgifter (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="b16e7-120">Then synchronize by using the Project expense transaction categories (Fin and Ops to PSA) template.</span></span> <span data-ttu-id="b16e7-121">Du skal derefter køre synkroniseringen fra Project Service Automation til Finance and Operations igen.</span><span class="sxs-lookup"><span data-stu-id="b16e7-121">You should then run the synchronization from Project Service Automation to Finance and Operations one more time.</span></span>
>
> <span data-ttu-id="b16e7-122">Hvis du synkroniserer først fra Project Service Automation, skal følgende krav opfyldes i Finance and Operations, før synkroniseringen udføres:</span><span class="sxs-lookup"><span data-stu-id="b16e7-122">If you synchronize first from Project Service Automation, the following requirements must be met in Finance and Operations before the synchronization is run:</span></span>
>
> - <span data-ttu-id="b16e7-123">Den delte kategori, der svarer til den projektkategori, der er oprettet i Project Service Automation skal findes, og den skal være aktiveret for både **Projekt** og **Udgift**.</span><span class="sxs-lookup"><span data-stu-id="b16e7-123">The shared category that matches the project category that is set up in Project Service Automation must exist, and it must be enabled for both **Project** and **Expense**.</span></span>
> - <span data-ttu-id="b16e7-124">For hver juridisk enhed i Finance and Operations, der skal integreres med, skal der være følgende projektkategorier:</span><span class="sxs-lookup"><span data-stu-id="b16e7-124">For each Finance and Operations legal entity that must be integrated with, the following project categories must exist:</span></span>
>
>     - <span data-ttu-id="b16e7-125">**Projektkategori** findes.</span><span class="sxs-lookup"><span data-stu-id="b16e7-125">**Project category** exists.</span></span> 
>     - <span data-ttu-id="b16e7-126">**Brug i udgift** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="b16e7-126">**Use in Expense** is enabled.</span></span>
>     - <span data-ttu-id="b16e7-127">**Aktiv i kladde** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="b16e7-127">**Active in journal** is enabled.</span></span>
>     - <span data-ttu-id="b16e7-128">**Transaktionstype** er angivet til **Udgift**.</span><span class="sxs-lookup"><span data-stu-id="b16e7-128">**Transaction type** is set to **Expense**.</span></span>

<span data-ttu-id="b16e7-129">I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b16e7-129">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="b16e7-130">[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="b16e7-130">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>

## <a name="project-expense-category-synchronization-from-finance-and-operations-to-project-service-automation"></a><span data-ttu-id="b16e7-131">Synkronisering af projektudgiftskategorier fra Finance and Operations til Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b16e7-131">Project expense category synchronization from Finance and Operations to Project Service Automation</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b16e7-132">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="b16e7-132">Template and task</span></span>

<span data-ttu-id="b16e7-133">Du kan få adgang skabelonen ved i Microsoft PowerApps Administration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="b16e7-133">To access the template, in the Microsoft PowerApps admin center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="b16e7-134">Følgende skabeloner og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Finance and Operations til Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="b16e7-134">The following template and underlying task are used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

- <span data-ttu-id="b16e7-135">**Navn på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (Fin and Ops til PSA)</span><span class="sxs-lookup"><span data-stu-id="b16e7-135">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
- <span data-ttu-id="b16e7-136">**Navnet på opgaven i projektet:** Synkroniseringskategorier til PSA</span><span class="sxs-lookup"><span data-stu-id="b16e7-136">**Name of the task in the project:** Sync categories to PSA</span></span>

### <a name="entity-set"></a><span data-ttu-id="b16e7-137">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="b16e7-137">Entity set</span></span>

| <span data-ttu-id="b16e7-138">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b16e7-138">Finance and Operations</span></span>            | <span data-ttu-id="b16e7-139">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b16e7-139">Project Service Automation</span></span> |
|-----------------------------------|----------------------------|
| <span data-ttu-id="b16e7-140">Integrationsenhed for kategorier</span><span class="sxs-lookup"><span data-stu-id="b16e7-140">Integration entity for categories</span></span> | <span data-ttu-id="b16e7-141">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="b16e7-141">Transaction categories</span></span>     |

### <a name="entity-flow"></a><span data-ttu-id="b16e7-142">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="b16e7-142">Entity flow</span></span>

<span data-ttu-id="b16e7-143">Projektudgiftskategorier administreres i Finance and Operations, og de synkroniseres med Project Service Automation som transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="b16e7-143">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

### <a name="power-query"></a><span data-ttu-id="b16e7-144">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="b16e7-144">Power Query</span></span>

<span data-ttu-id="b16e7-145">Når du synkroniserer til Project Service Automation, skal du skal bruge Microsoft Power-forespørgsel til Excel til at angive faktureringstypen i transaktionskategorien.</span><span class="sxs-lookup"><span data-stu-id="b16e7-145">When you're synchronizing to Project Service Automation, you must use Microsoft Power Query for Excel to set the billing type on the transaction category.</span></span> <span data-ttu-id="b16e7-146">Skabelonen Transaktionskategorier for projektudgifter (Fin and Ops til PSA) har en standardkolonne og tilknytning.</span><span class="sxs-lookup"><span data-stu-id="b16e7-146">The Project expense transaction categories (Fin and Ops to PSA) template provides a default column and mapping.</span></span> <span data-ttu-id="b16e7-147">Hvis du opretter din egen skabelon, skal du tilføje en betinget kolonne i Power-forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="b16e7-147">If you create your own template, you must add a conditional column in Power Query.</span></span> <span data-ttu-id="b16e7-148">Følg disse trin.</span><span class="sxs-lookup"><span data-stu-id="b16e7-148">Follow these steps.</span></span>

1. <span data-ttu-id="b16e7-149">Klik på pilen for at åbne tilknytningen af projektudgiftskategorier i skabelonen Transaktionskategorier for projektudgifter (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="b16e7-149">Click the arrow to open the mapping of the project expense categories task in the Project expense transaction categories (Fin and Ops to PSA) template.</span></span>
2. <span data-ttu-id="b16e7-150">Klik på linket **Avanceret forespørgsel og filtrering** for at åbne Power-forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="b16e7-150">Click the **Advance Query and Filtering** link to open Power Query.</span></span>
2. <span data-ttu-id="b16e7-151">Vælg **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="b16e7-151">Select **Add Conditional Column**.</span></span>
3. <span data-ttu-id="b16e7-152">Angiv et navn til den nye kolonne, f.eks. **BillingType**.</span><span class="sxs-lookup"><span data-stu-id="b16e7-152">Enter a name for the new column, such as **BillingType**.</span></span>
4. <span data-ttu-id="b16e7-153">Angiv følgende betingelse: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="b16e7-153">Enter the following condition: **if CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
5. <span data-ttu-id="b16e7-154">Klik på **OK** i kolonnen.</span><span class="sxs-lookup"><span data-stu-id="b16e7-154">Click **OK** on the column.</span></span>
6. <span data-ttu-id="b16e7-155">Sørg for at tilknytte den nye kolonne på tilknytningssiden.</span><span class="sxs-lookup"><span data-stu-id="b16e7-155">Be sure to map this new column on the mapping page.</span></span>

<span data-ttu-id="b16e7-156">Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="b16e7-156">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="b16e7-157">Tilknytningen viser, de oplysninger der synkroniseres fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b16e7-157">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="b16e7-158">[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b16e7-158">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

## <a name="project-expense-category-synchronization-from-project-service-automation-to-finance-and-operations"></a><span data-ttu-id="b16e7-159">Synkronisering af projektudgiftskategorier fra Project Service Automation til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b16e7-159">Project expense category synchronization from Project Service Automation to Finance and Operations</span></span>

### <a name="template-and-task"></a><span data-ttu-id="b16e7-160">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="b16e7-160">Template and task</span></span>

<span data-ttu-id="b16e7-161">Følgende skabelon og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Project Service Automation til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b16e7-161">The following template and underlying task are used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

- <span data-ttu-id="b16e7-162">**Navn på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (PSA til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="b16e7-162">**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops)</span></span>
- <span data-ttu-id="b16e7-163">**Navnet på opgaven i projektet:** Synkroniseringskategorier til Fin Ops</span><span class="sxs-lookup"><span data-stu-id="b16e7-163">**Name of the task in the project:** Sync categories to Fin Ops</span></span>

### <a name="entity-set"></a><span data-ttu-id="b16e7-164">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="b16e7-164">Entity set</span></span>

| <span data-ttu-id="b16e7-165">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="b16e7-165">Project Service Automation</span></span> | <span data-ttu-id="b16e7-166">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b16e7-166">Finance and Operations</span></span>            |
|----------------------------|-----------------------------------|
| <span data-ttu-id="b16e7-167">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="b16e7-167">Transaction categories</span></span>     | <span data-ttu-id="b16e7-168">Integrationsenhed for kategorier</span><span class="sxs-lookup"><span data-stu-id="b16e7-168">Integration entity for categories</span></span> |

### <a name="entity-flow"></a><span data-ttu-id="b16e7-169">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="b16e7-169">Entity flow</span></span>

<span data-ttu-id="b16e7-170">Projektudgiftskategorier administreres i Finance and Operations, og de synkroniseres med Project Service Automation som transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="b16e7-170">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="b16e7-171">Synkroniseringen tilbage til Finance and Operations opdaterer projektkategorien i Finance and Operations med integrations-id'et fra Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="b16e7-171">The synchronization back to Finance and Operations updates the project category in Finance and Operations with the integration ID from Project Service Automation.</span></span>

### <a name="template-mapping-in-data-integration"></a><span data-ttu-id="b16e7-172">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="b16e7-172">Template mapping in Data integration</span></span>

<span data-ttu-id="b16e7-173">Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="b16e7-173">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="b16e7-174">Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b16e7-174">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="b16e7-175">[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="b16e7-175">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>
