---
title: Synkronisere projektudgiftskategorier fra Project Service Automation
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektudgiftskategorier mellem Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation.
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
ms.dyn365.ops.version: AX 8.0.0
ms.translationtype: HT
ms.sourcegitcommit: bd8feff598cf80ca675c7d2b5dda636799b19e29
ms.openlocfilehash: dcdb9b6ec296073d511c069cdceb1c61080b6d97
ms.contentlocale: da-dk
ms.lasthandoff: 05/29/2018

---

# <a name="synchronize-project-expense-categories-between-finance-and-operations-and-project-service-automation"></a><span data-ttu-id="61c15-103">Synkronisere projektudgiftskategorier mellem Finance and Operations og Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="61c15-103">Synchronize project expense categories between Finance and Operations and Project Service Automation</span></span>

<span data-ttu-id="61c15-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere projektudgiftskategorier mellem Microsoft Dynamics 365 for Finance and Operations og Dynamics 365 for Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="61c15-104">This topic describes the templates and underlying tasks that are used to synchronize project expense categories between Microsoft Dynamics 365 for Finance and Operations and Dynamics 365 for Project Service Automation.</span></span>

> [!NOTE]
> <span data-ttu-id="61c15-105">Projektopgaveintegration, udgiftstransaktionskategorier, timeestimater, udgiftsestimater og låsning af funktioner er tilgængelige i Dynamics 365 for Finance and Operations version 8.0.</span><span class="sxs-lookup"><span data-stu-id="61c15-105">Project tasks integration, expense transaction categories, hour estimates, expense estimates, and functionality locking is available in Dynamics 365 for Finance and Operations version 8.0.</span></span>

## <a name="data-flow-for-project-service-automation-and-finance-and-operations"></a><span data-ttu-id="61c15-106">Dataflow for Project Service Automation og Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="61c15-106">Data flow for Project Service Automation and Finance and Operations</span></span>

<span data-ttu-id="61c15-107">Løsningen til integration af Project Service Automation og Finance and Operations bruger dataintegrationsfunktionen til at synkronisere data på tværs af forekomster af Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61c15-107">The Project Service Automation and Finance and Operations integration solution uses the Data integration feature to synchronize data across instances of Project Service Automation and Finance and Operations.</span></span> <span data-ttu-id="61c15-108">Integrationsskabelonerne, der er tilgængelige i dataintegrationsfunktionen, muliggør strømmen af data om transaktionskategorier for projektudgifter mellem Finance and Operations og Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="61c15-108">The integration templates that are available with the Data integration feature enables the flow of data about project expense transaction categories between Finance and Operations and Project Service Automation.</span></span>

<span data-ttu-id="61c15-109">Hvis projektudgiftskategorier administreres i Finance and Operations, går integrationsflowet først fra Finance and Operations til Project Service Automation, og derefter opdateres projektudgiftskategoriers integrations-id'er ved at synkronisere fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61c15-109">If the project expense categories are mastered in Finance and Operations, the integration flow is first from Finance and Operations to Project Service Automation, and then updating the project expense categories integration IDs by synchronizing from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="61c15-110">Hvis projektudgiftskategorier administreres i Project Service Automation, er integrationsflowet først fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61c15-110">If the project expense categories are mastered in Project Service Automation, the integration flow is first from Project Service Automation to Finance and Operations.</span></span> <span data-ttu-id="61c15-111">Projektkategorier skal allerede være konfigureret i Finance and Operations inden synkronisering af Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="61c15-111">The project categories must already be configured in Finance and Operations prior to the synchronization from Project Service Automation.</span></span> <span data-ttu-id="61c15-112">Derefter synkroniseres fra Finance and Operations til Project Service Automation og derefter fra Project Service Automation til Finance and Operations igen.</span><span class="sxs-lookup"><span data-stu-id="61c15-112">Then synchronize from Finance and Operations back to Project Service Automation and then from Project Service Automation to Finance and Operations again.</span></span> <span data-ttu-id="61c15-113">Dette sikrer, at kategorierne sammenkædes, og at der ikke oprettes dubletter.</span><span class="sxs-lookup"><span data-stu-id="61c15-113">This ensures the categories are linked and duplicates are not created.</span></span>

> [!NOTE]
> <span data-ttu-id="61c15-114">Projektudgiftskategorierne håndteres typisk i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61c15-114">Typically, the project expense categories will be mastered in Finance and Operations.</span></span> <span data-ttu-id="61c15-115">Hvis det ikke er tilfældet, eller du allerede har udgiftskategorier, der er oprettet i Project Service Automation, skal du først synkronisere med transaktionskategorier for projektudgifter (PSA til Fin and Ops) og derefter synkronisere ved hjælp af transaktionskategorier for projektudgifter (Fin and Ops til PSA).</span><span class="sxs-lookup"><span data-stu-id="61c15-115">If that is not your situation, or you already have expense categories created in Project Service Automation, you must first sync using the Project expense transaction categories (PSA to Fin and Ops) and then sync using Project expense transaction categories (Fin and Ops to PSA).</span></span> <span data-ttu-id="61c15-116">Du skal derefter køre synkroniseringen fra PSA til Fin and Ops igen.</span><span class="sxs-lookup"><span data-stu-id="61c15-116">You should then run the sync from PSA to Fin and Ops one more time.</span></span>

> <span data-ttu-id="61c15-117">Hvis synkroniseringen først udføres fra Project Service Automation, skal projektkategorierne allerede være oprettet i Finance and Operations, og projektkategorier, der skal synkroniseres med Project Service Automation-transaktionskategorier, skal være konfigurerede som **Aktiv i kladder**.</span><span class="sxs-lookup"><span data-stu-id="61c15-117">If synchronizing first from Project Service Automation, the project categories must already be set up in Finance and Operations and any project categories that need to be synched with the Project Service Automation transaction categories must be set up to be **Active in journals**.</span></span>

<span data-ttu-id="61c15-118">I følgende illustration vises, hvordan data synkroniseres mellem Project Service Automation og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61c15-118">The following illustration shows how the data is synchronized between Project Service Automation and Finance and Operations.</span></span>

<span data-ttu-id="61c15-119">[![Dataflow for Project Service Automation-integration med Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span><span class="sxs-lookup"><span data-stu-id="61c15-119">[![Data flow for Project Service Automation integration with Finance and Operations](./media/ProjectExpenseCategoriesFlow.png)](./media/ProjectExpenseCategoriesFlow.png)</span></span>


## <a name="templates-and-tasks"></a><span data-ttu-id="61c15-120">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="61c15-120">Templates and tasks</span></span>

<span data-ttu-id="61c15-121">Du kan få adgang til tilgængelige skabeloner ved i Microsoft PowerApps Admininstration at vælge **Projekter** og derefter i øverste højre hjørne vælge **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="61c15-121">To access available templates, in the Microsoft PowerApps Admin Center, select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="61c15-122">Følgende skabeloner og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Finance and Operations til Project Service Automation:</span><span class="sxs-lookup"><span data-stu-id="61c15-122">The following template and underlying task is used to synchronize project expense categories from Finance and Operations to Project Service Automation:</span></span>

-  <span data-ttu-id="61c15-123">**Navn på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (Fin and Ops til PSA)</span><span class="sxs-lookup"><span data-stu-id="61c15-123">**Name of the template in Data integration:** Project expense transaction categories (Fin and Ops to PSA)</span></span>
-  <span data-ttu-id="61c15-124">**Navnet på opgaven i projektet:** Synkroniseringskategorier til PSA</span><span class="sxs-lookup"><span data-stu-id="61c15-124">**Name of the task in the project:** Sync categories to PSA</span></span>

## <a name="entity-set"></a><span data-ttu-id="61c15-125">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="61c15-125">Entity set</span></span>

| <span data-ttu-id="61c15-126">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="61c15-126">Finance and Operations</span></span>               | <span data-ttu-id="61c15-127">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="61c15-127">Project Service Automation</span></span>    |
|--------------------------------------|-------------------------------|
| <span data-ttu-id="61c15-128">Integrationsenhed for kategorier</span><span class="sxs-lookup"><span data-stu-id="61c15-128">Integration entity for categories</span></span>    | <span data-ttu-id="61c15-129">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="61c15-129">Transaction categories</span></span>        |

## <a name="entity-flow"></a><span data-ttu-id="61c15-130">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="61c15-130">Entity flow</span></span>

<span data-ttu-id="61c15-131">Projektudgiftskategorier administreres i Finance and Operations, og de synkroniseres med Project Service Automation som transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="61c15-131">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span>

## <a name="power-query"></a><span data-ttu-id="61c15-132">Power-forespørgsel</span><span class="sxs-lookup"><span data-stu-id="61c15-132">Power Query</span></span>

<span data-ttu-id="61c15-133">Du skal bruge Microsoft Power-forespørgsel til at angive faktureringstypen i transaktionskategorien, når du synkroniserer med Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="61c15-133">You must use Microsoft Power Query to set the billing type on the transaction category when synchronizing to Project Service Automation.</span></span> <span data-ttu-id="61c15-134">Skabelonen til transaktionskategorier for projektudgifter (Fin and Ops til PSA) har en standardkolonne og tilknytning, der er allerede angivet.</span><span class="sxs-lookup"><span data-stu-id="61c15-134">The Project expense transaction categories (Fin and Ops to PSA) template has a default column and mapping already provided.</span></span> <span data-ttu-id="61c15-135">Hvis du opretter din egen skabelon, skal du tilføje en betinget kolonne i Power-forespørgsel.</span><span class="sxs-lookup"><span data-stu-id="61c15-135">If you create your own template, you must add a conditional column in Power Query.</span></span>
- <span data-ttu-id="61c15-136">Åbn formularen Avanceret forespørgsel og filtrering fra tilknytningen af opgaven projektudgiftskategorier.</span><span class="sxs-lookup"><span data-stu-id="61c15-136">Open the Advance Query and Filtering form from within the mapping of project expense categories task.</span></span>
- <span data-ttu-id="61c15-137">Vælg **Tilføj betinget kolonne**.</span><span class="sxs-lookup"><span data-stu-id="61c15-137">Select **Add Conditional Column**.</span></span>
- <span data-ttu-id="61c15-138">Giv den nye kolonne et navn, f.eks. BillingType.</span><span class="sxs-lookup"><span data-stu-id="61c15-138">Give the new column a name, such as BillingType.</span></span>
- <span data-ttu-id="61c15-139">Angiv følgende betingelse: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span><span class="sxs-lookup"><span data-stu-id="61c15-139">Enter the following condition: if **CATEGORYID not equal to null then 19235001, Otherwise null**.</span></span>
- <span data-ttu-id="61c15-140">Klik på **OK** i kolonnen.</span><span class="sxs-lookup"><span data-stu-id="61c15-140">Click **OK** on the column.</span></span>
- <span data-ttu-id="61c15-141">Sørg for at tilknytte den nye kolonne på tilknytningssiden.</span><span class="sxs-lookup"><span data-stu-id="61c15-141">Be sure to map this new column in the mapping page.</span></span>

<span data-ttu-id="61c15-142">Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="61c15-142">The following illustration shows an example of the template task mapping in Data integration.</span></span> <span data-ttu-id="61c15-143">Tilknytningen viser, de oplysninger der synkroniseres fra Finance and Operations til Project Service Automation.</span><span class="sxs-lookup"><span data-stu-id="61c15-143">The mapping shows the field information that will be synchronized from Finance and Operations to Project Service Automation.</span></span>

<span data-ttu-id="61c15-144">[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="61c15-144">[![Template mapping](./media/ProjectExpenseCategoriesToPSAMapping.jpg)](./media/ProjectExpenseCategoriesToPSAMapping.jpg)</span></span>

<span data-ttu-id="61c15-145">Følgende skabeloner og underliggende opgave bruges til at synkronisere projektudgiftskategorier fra Project Service Automation til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="61c15-145">The following template and underlying task is used to synchronize project expense categories from Project Service Automation to Finance and Operations:</span></span>

<span data-ttu-id="61c15-146">-**Navnet på skabelonen i dataintegration:** Transaktionskategorier for projektudgifter (PSA til Fin and Ops) -**Navnet på opgaven i projektet:** Synkronisering af kategorier til Fin Ops</span><span class="sxs-lookup"><span data-stu-id="61c15-146">-**Name of the template in Data integration:** Project expense transaction categories (PSA to Fin and Ops) -**Name of the task in the project:** Sync categories to Fin Ops</span></span>

## <a name="entity-set"></a><span data-ttu-id="61c15-147">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="61c15-147">Entity set</span></span>

| <span data-ttu-id="61c15-148">Project Service Automation</span><span class="sxs-lookup"><span data-stu-id="61c15-148">Project Service Automation</span></span>      | <span data-ttu-id="61c15-149">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="61c15-149">Finance and Operations</span></span>             |
|---------------------------------|------------------------------------|
| <span data-ttu-id="61c15-150">Transaktionskategorier</span><span class="sxs-lookup"><span data-stu-id="61c15-150">Transaction categories</span></span>          | <span data-ttu-id="61c15-151">Integrationsenhed for kategorier</span><span class="sxs-lookup"><span data-stu-id="61c15-151">Integration entity for categories</span></span>  | 

## <a name="entity-flow"></a><span data-ttu-id="61c15-152">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="61c15-152">Entity flow</span></span>

<span data-ttu-id="61c15-153">Projektudgiftskategorier administreres i Finance and Operations, og de synkroniseres med Project Service Automation som transaktionskategorier.</span><span class="sxs-lookup"><span data-stu-id="61c15-153">Project expense categories are managed in Finance and Operations, and they are synchronized to Project Service Automation as transaction categories.</span></span> <span data-ttu-id="61c15-154">Synkroniseringen tilbage til Finance and Operations opdaterer integrations-id'et fra Project Service Automation i Finance and Operations-projektkategorien.</span><span class="sxs-lookup"><span data-stu-id="61c15-154">The synchronization back to Finance and Operations updates the integration ID from Project Service Automation on the Finance and Operations project category.</span></span>

<span data-ttu-id="61c15-155">Følgende illustration viser et eksempel på skabelonopgavetilknytningen i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="61c15-155">The following illustration shows an example of the template task mapping in Data integration.</span></span>

> [!NOTE]
> <span data-ttu-id="61c15-156">Tilknytningen viser, de oplysninger der synkroniseres fra Project Service Automation til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="61c15-156">The mapping shows the field information that will be synchronized from Project Service Automation to Finance and Operations.</span></span>

<span data-ttu-id="61c15-157">[![Tilknytning af skabelon](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span><span class="sxs-lookup"><span data-stu-id="61c15-157">[![Template mapping](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)](./media/ProjectExpenseCategoriesToFinOpsMapping.jpg)</span></span>

