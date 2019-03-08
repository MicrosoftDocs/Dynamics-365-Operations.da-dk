---
title: Konfigurere stillinger
description: Stillinger er et vigtigt element i et organisationshierarkis lavere niveau.
author: DarinKramer
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, HcmWorkforceWorkspace, HcmWorkerActivityChart, HcmAllWorkersListPart, HcmPosition, HcmPositionNewPosition, HcmJobLookup, HcmPositionReportsToDialog, HcmPositionLookup, FinancialDimensionDefaultTemplatesLookup, DimensionLookup
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5d69e6b926a047888a162dae1cdc870718d8f945
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "337871"
---
# <a name="set-up-positions"></a><span data-ttu-id="1341f-103">Konfigurere stillinger</span><span class="sxs-lookup"><span data-stu-id="1341f-103">Set up positions</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1341f-104">Stillinger er et vigtigt element i et organisationshierarkis lavere niveau.</span><span class="sxs-lookup"><span data-stu-id="1341f-104">Positions are an important element of the lower level of an organization hierarchy.</span></span> <span data-ttu-id="1341f-105">En stilling er en individuel forekomst af et job.</span><span class="sxs-lookup"><span data-stu-id="1341f-105">A position is an individual instance of a job.</span></span> <span data-ttu-id="1341f-106">For eksempel er stillingen "Salgschef (øst)" én af de stillinger, der er tilknyttet jobbet "Salgschef".</span><span class="sxs-lookup"><span data-stu-id="1341f-106">For example, the position, “Sales manager (East),” is one of the positions that is associated with the job, “Sales manager.”</span></span> <span data-ttu-id="1341f-107">En stilling findes i en afdeling og har muligvis kun én tilknyttet arbejder.</span><span class="sxs-lookup"><span data-stu-id="1341f-107">A position exists in a department and may have only one worker associated with it.</span></span> <span data-ttu-id="1341f-108">I denne opgave vil vi gennemgå de trin, der kræves for at oprette en stilling.</span><span class="sxs-lookup"><span data-stu-id="1341f-108">In this task we will walk through the steps required to create a position.</span></span> <span data-ttu-id="1341f-109">Denne procedure er beregnet til personalespecialister.</span><span class="sxs-lookup"><span data-stu-id="1341f-109">This procedure is intended for Human Resources Specialists.</span></span>

1. <span data-ttu-id="1341f-110">Klik på Styring af arbejdskraft.</span><span class="sxs-lookup"><span data-stu-id="1341f-110">Click Workforce management.</span></span>
2. <span data-ttu-id="1341f-111">Klik på Ledige stillinger.</span><span class="sxs-lookup"><span data-stu-id="1341f-111">Click Open positions.</span></span>
3. <span data-ttu-id="1341f-112">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="1341f-112">Click New to open the drop dialog.</span></span>
4. <span data-ttu-id="1341f-113">Indtast eller vælg en værdi i feltet Job.</span><span class="sxs-lookup"><span data-stu-id="1341f-113">In the Job field, enter or select a value.</span></span>
    * <span data-ttu-id="1341f-114">Denne jobbeskrivelse, titel og ansættelsesfaktor svarende til fuld tid bliver automatisk kopieret fra det valgte job til stillingen.</span><span class="sxs-lookup"><span data-stu-id="1341f-114">The Job description, title, and full-time equivalent employment factor are automatically copied from the selected job into the position.</span></span>  
5. <span data-ttu-id="1341f-115">ResolveChanges-jobbet.</span><span class="sxs-lookup"><span data-stu-id="1341f-115">ResolveChanges the Job.</span></span>
6. <span data-ttu-id="1341f-116">Klik på Opret stilling.</span><span class="sxs-lookup"><span data-stu-id="1341f-116">Click Create position.</span></span>
7. <span data-ttu-id="1341f-117">Indtast eller vælg en værdi i feltet Afdeling.</span><span class="sxs-lookup"><span data-stu-id="1341f-117">In the Department field, enter or select a value.</span></span>
8. <span data-ttu-id="1341f-118">Indtast eller vælg en værdi i feltet Stilling.</span><span class="sxs-lookup"><span data-stu-id="1341f-118">In the Position type field, enter or select a value.</span></span>
9. <span data-ttu-id="1341f-119">Indtast eller vælg en værdi i feltet Kompensationsområde.</span><span class="sxs-lookup"><span data-stu-id="1341f-119">In the Compensation region field, enter or select a value.</span></span>
    * <span data-ttu-id="1341f-120">Feltet Kompensationsområde bestemmer reglerne for kompensationsberettigelse og budgetter med fast stigning, der gælder for en medarbejder i den pågældende stilling.</span><span class="sxs-lookup"><span data-stu-id="1341f-120">The Compensation region field determines the compensation eligibility rules and fixed increase budgets that apply to an employee in that position.</span></span>  
10. <span data-ttu-id="1341f-121">Indtast en dato og et klokkeslæt i feltet Tilgængelig for tildeling.</span><span class="sxs-lookup"><span data-stu-id="1341f-121">In the Available for assignment field, enter a date and time.</span></span>
11. <span data-ttu-id="1341f-122">Udvid sektionen Stillings varighed.</span><span class="sxs-lookup"><span data-stu-id="1341f-122">Expand the Position duration section.</span></span>
    * <span data-ttu-id="1341f-123">Stillingens varighed angives som standard ud fra de aktiverings- og pensioneringsdatoer, der er angivet tidligere</span><span class="sxs-lookup"><span data-stu-id="1341f-123">Position duration is entered by default based on activation and retirement dates entered earlier</span></span>  
12. <span data-ttu-id="1341f-124">Udvid sektionen Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="1341f-124">Expand the Reports to position section.</span></span>
    * <span data-ttu-id="1341f-125">Når du tildeler en medarbejder til en stilling, der refererer til en anden stilling, opretter du en direkte rapporteringsrelation mellem de arbejdere, der er tildelt til to stillinger.</span><span class="sxs-lookup"><span data-stu-id="1341f-125">When you assign a worker to a position that reports to another position, you create a direct reporting relationship between the workers who are assigned to the two positions.</span></span>  
13. <span data-ttu-id="1341f-126">Klik på Ny for at åbne dialogboksen Fjern.</span><span class="sxs-lookup"><span data-stu-id="1341f-126">Click New to open the drop dialog.</span></span>
14. <span data-ttu-id="1341f-127">Indtast eller vælg en værdi i feltet Rapportér til.</span><span class="sxs-lookup"><span data-stu-id="1341f-127">In the Reports to field, enter or select a value.</span></span>
15. <span data-ttu-id="1341f-128">Klik på Opret.</span><span class="sxs-lookup"><span data-stu-id="1341f-128">Click Create.</span></span>
16. <span data-ttu-id="1341f-129">Udvid sektionen Medarbejdertildeling.</span><span class="sxs-lookup"><span data-stu-id="1341f-129">Expand the Worker assignment section.</span></span>
17. <span data-ttu-id="1341f-130">Udvid eller skjul sektionen Relationer.</span><span class="sxs-lookup"><span data-stu-id="1341f-130">Expand the Relationships section.</span></span>
    * <span data-ttu-id="1341f-131">Hvis organisationen bruger et matrixhierarki eller et andet brugerdefineret hierarki, kan du konfigurere stillingshierarkityper og derefter tilføje rapporteringsforhold for hver enkelt hierarki, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="1341f-131">If your organization uses a matrix hierarchy or another custom hierarchy, you can set up position hierarchy types and then add reporting relationships to positions for each hierarchy type that you set up.</span></span>  
18. <span data-ttu-id="1341f-132">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="1341f-132">Click Add.</span></span>
19. <span data-ttu-id="1341f-133">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="1341f-133">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="1341f-134">Indtast eller vælg en værdi i feltet Hierarkinavn.</span><span class="sxs-lookup"><span data-stu-id="1341f-134">In the Hierarchy name field, enter or select a value.</span></span>
21. <span data-ttu-id="1341f-135">Indtast eller vælg en værdi i feltet Rapporterer til stilling.</span><span class="sxs-lookup"><span data-stu-id="1341f-135">In the Reports to position field, enter or select a value.</span></span>
22. <span data-ttu-id="1341f-136">Udvid sektionen Lønningsliste.</span><span class="sxs-lookup"><span data-stu-id="1341f-136">Expand the Payroll section.</span></span>
23. <span data-ttu-id="1341f-137">Indtast eller vælg en værdi i feltet Betalingscyklus.</span><span class="sxs-lookup"><span data-stu-id="1341f-137">In the Pay cycle field, enter or select a value.</span></span>
24. <span data-ttu-id="1341f-138">Indtast eller vælg en værdi i feltet Betalt af.</span><span class="sxs-lookup"><span data-stu-id="1341f-138">In the Paid by field, enter or select a value.</span></span>
25. <span data-ttu-id="1341f-139">Indtast et tal i feltet Normaltimer på årsbasis.</span><span class="sxs-lookup"><span data-stu-id="1341f-139">In the Annual regular hours field, enter a number.</span></span>
    * <span data-ttu-id="1341f-140">Dette det faste antal betalte timer, som arbejderen i denne stilling forventes at arbejde hvert år.</span><span class="sxs-lookup"><span data-stu-id="1341f-140">This is the number of regularly paid hours that the worker in this position is expected to work each year.</span></span>  
26. <span data-ttu-id="1341f-141">Udvid sektionen Fagforening.</span><span class="sxs-lookup"><span data-stu-id="1341f-141">Expand the Labor union section.</span></span>
27. <span data-ttu-id="1341f-142">Skjul sektionen Fagforening.</span><span class="sxs-lookup"><span data-stu-id="1341f-142">Collapse the Labor union section.</span></span>
28. <span data-ttu-id="1341f-143">Udvid sektionen Økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="1341f-143">Expand the Financial dimensions section.</span></span>
29. <span data-ttu-id="1341f-144">Indtast eller vælg en værdi i feltet Distributionsskabelon.</span><span class="sxs-lookup"><span data-stu-id="1341f-144">In the Distribution template field, enter or select a value.</span></span>
30. <span data-ttu-id="1341f-145">Indtast eller vælg en værdi i feltet Afdeling.</span><span class="sxs-lookup"><span data-stu-id="1341f-145">In the Department field, enter or select a value.</span></span>
31. <span data-ttu-id="1341f-146">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="1341f-146">Click Save.</span></span>

