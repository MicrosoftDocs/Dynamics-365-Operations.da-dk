---
title: Bruge modeltilknytningskonfiguration til samlede beregninger på databaseniveau
description: Denne procedure indeholder oplysninger om, hvordan du designer en ny modeltilknytningskonfiguration til elektronisk rapportering (ER) og bruger indbyggede ER-funktioner til effektive samlede beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3084882dd4b51f067793b3a7999ce89cda1257d9
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2184594"
---
# <a name="use-model-mapping-configurations-for-aggregate-calculations-at-the-database-level"></a><span data-ttu-id="a3fd0-103">Bruge modeltilknytningskonfiguration til samlede beregninger på databaseniveau</span><span class="sxs-lookup"><span data-stu-id="a3fd0-103">Use model mapping configurations for aggregate calculations at the database level</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="a3fd0-104">Denne procedure indeholder oplysninger om, hvordan du designer en ny modeltilknytningskonfiguration til elektronisk rapportering (ER) og bruger indbyggede ER-funktioner til effektive samlede beregninger.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="a3fd0-105">I denne procedure skal du oprette en konfiguration til eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="a3fd0-106">Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="a3fd0-107">Disse trin kan udføres ved hjælp af ethvert datasæt.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="a3fd0-108">For at fuldføre disse trin, skal du først fuldføre trinnene i proceduren "ER forbedrer effektiviteten ved samlede beregninger ved at udføre dem på databaseniveau (Del 1: Forbered konfigurationer)".</span><span class="sxs-lookup"><span data-stu-id="a3fd0-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="a3fd0-109">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="a3fd0-110">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="a3fd0-111">Vælg 'Intrastat-model\Intrastat-eksempeltilknytning' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="a3fd0-112">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-112">Click Designer.</span></span>
5. <span data-ttu-id="a3fd0-113">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-113">Click Designer.</span></span>
6. <span data-ttu-id="a3fd0-114">Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="a3fd0-115">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-115">Click Add root.</span></span>
    * <span data-ttu-id="a3fd0-116">Tilføj en ny datakilde, der repræsenterer poster, du vil gruppere.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="a3fd0-117">Skriv "Transaktioner" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="a3fd0-118">Poster</span><span class="sxs-lookup"><span data-stu-id="a3fd0-118">Transactions</span></span>  
9. <span data-ttu-id="a3fd0-119">Skriv "Intrastat" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="a3fd0-120">Intrastat</span><span class="sxs-lookup"><span data-stu-id="a3fd0-120">Intrastat</span></span>  
10. <span data-ttu-id="a3fd0-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-121">Click OK.</span></span>
11. <span data-ttu-id="a3fd0-122">Vælg 'Funktioner\Gruppér efter' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="a3fd0-123">Denne datakildetype bruges til at introducere en ny datakilde på kørselstidspunktet til at gruppere poster og beregne de krævede summeringer.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="a3fd0-124">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-124">Click Add root.</span></span>
13. <span data-ttu-id="a3fd0-125">Skriv 'TransactionsGroups' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="a3fd0-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="a3fd0-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="a3fd0-127">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-127">Click Edit group by.</span></span>
15. <span data-ttu-id="a3fd0-128">Vælg "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="a3fd0-129">Vælg den tilføjede datakilde af typen 'Liste over poster', der repræsenterer de poster, du vil gruppere.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="a3fd0-130">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-130">Click Add field to.</span></span>
17. <span data-ttu-id="a3fd0-131">Klik på Hvad skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-131">Click What to group.</span></span>
18. <span data-ttu-id="a3fd0-132">Udvid "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="a3fd0-133">Vælg "Transaktioner\Retning" i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="a3fd0-134">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-134">Click Add field to.</span></span>
21. <span data-ttu-id="a3fd0-135">Klik på Grupperede felter.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="a3fd0-136">Marker feltet for at angive grupperingsniveauet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="a3fd0-137">Ud fra dette valg returnerer datakilden på kørselstidspunktet så mange grupper af transaktioner, som der er retningskoder, der vil blive opfyldt i Intrastat-tabellen.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="a3fd0-138">Vælg 'Transaktioner\Fakturabeløb(AmountMST)' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="a3fd0-139">Marker feltet for at angive kilden til beregning af aggregering.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="a3fd0-140">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-140">Click Add field to.</span></span>
24. <span data-ttu-id="a3fd0-141">Klik på Aggregeringsfelter.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="a3fd0-142">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="a3fd0-143">Vælg 'Sum' i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="a3fd0-144">Vælg aggregeringstypen.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="a3fd0-145">Skriv 'SumOfAmountMST' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="a3fd0-146">Angiv navnet på denne aggregering i datakilden, der er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="a3fd0-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-147">Click Save.</span></span>
    * <span data-ttu-id="a3fd0-148">Bemærk, at feltet 'Udførelse' angiver, at denne gruppering udføres på kørselstidspunktet i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="a3fd0-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-149">Close the page.</span></span>
30. <span data-ttu-id="a3fd0-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-150">Click OK.</span></span>
31. <span data-ttu-id="a3fd0-151">Udvid "Totaler" i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="a3fd0-152">Udvid 'TransactionsGroups' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="a3fd0-153">Udvid "TransactionsGroups\aggregerede" i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="a3fd0-154">Vælg 'TransactionsGroups\aggregerede\SumOfAmountMST' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="a3fd0-155">Vælg 'Totaler\Fakturaværdi i alt(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="a3fd0-156">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-156">Click Bind.</span></span>
    * <span data-ttu-id="a3fd0-157">Baseret på denne indstilling vil denne datakilde beregne summen af værdierne i feltet 'AmountMST' for de enkelte grupper af transaktioner.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="a3fd0-158">Denne aggregeringsberegning vil være tilgængelig som elementet TransactionsGroups.aggregated.TotalAmount.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="a3fd0-159">Udvid 'TransactionsGroups' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="a3fd0-160">Vælg "TransactionsGroups" i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="a3fd0-161">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-161">Click Edit.</span></span>
40. <span data-ttu-id="a3fd0-162">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-162">Click Edit group by.</span></span>
41. <span data-ttu-id="a3fd0-163">Udvid "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="a3fd0-164">Vælg 'Transaktioner\Fakturabeløb(AmountMST)' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="a3fd0-165">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-165">Click Add field to.</span></span>
44. <span data-ttu-id="a3fd0-166">Klik på Aggregeringsfelter.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="a3fd0-167">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="a3fd0-168">Vælg 'Maks.' i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="a3fd0-169">Skriv 'MaxOfAmountMST' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="a3fd0-170">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-170">Click Save.</span></span>
    * <span data-ttu-id="a3fd0-171">Udførelse af GROUPBY-datakilder kan på nuværende tidspunkt oversættes til SQL-databaseniveauet med visse begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="a3fd0-172">Oversættelsen kan foretages for begge datakilder af typen 'Liste over poster' eller for datakilder, der er repræsenteret som et udtryk, der bruger funktionen FILTER.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="a3fd0-173">Den kan også udføres, når kun én sammenlægning er konfigureret til et enkelt felt i grupperingsposterne.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="a3fd0-174">Bemærk, at selvom der var konfigureret mere end én aggregering til feltet AmountMST, angiver feltet 'Udførelse' stadig, at denne gruppering udføres på kørselstidspunktet i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="a3fd0-175">Det skyldes, at kun én aggregering er bundet til datamodelelementet, og det bruges på kørselstidspunktet til at hente data fra denne datakilde.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="a3fd0-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-176">Close the page.</span></span>
50. <span data-ttu-id="a3fd0-177">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-177">Click OK.</span></span>
51. <span data-ttu-id="a3fd0-178">Udvid 'TransactionsGroups' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="a3fd0-179">Udvid "TransactionsGroups\aggregerede" i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="a3fd0-180">Vælg 'TransactionsGroups\aggregerede\MaxOfAmountMST' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="a3fd0-181">Vælg 'Totaler\Total statistisk værdi(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="a3fd0-182">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-182">Click Bind.</span></span>
56. <span data-ttu-id="a3fd0-183">Udvid 'TransactionsGroups' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="a3fd0-184">Vælg "TransactionsGroups" i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="a3fd0-185">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-185">Click Edit.</span></span>
59. <span data-ttu-id="a3fd0-186">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-186">Click Edit group by.</span></span>
    * <span data-ttu-id="a3fd0-187">Bemærk, at feltet 'Udførelse' angiver, at denne gruppering udføres på kørselstidspunktet i hukommelsen, fordi begge aggregeringer af det samme felt er bundet til datamodelelementerne.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="a3fd0-188">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="a3fd0-189">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-189">Click Delete.</span></span>
62. <span data-ttu-id="a3fd0-190">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-190">Click Yes.</span></span>
63. <span data-ttu-id="a3fd0-191">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-191">Click Delete.</span></span>
64. <span data-ttu-id="a3fd0-192">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-192">Click Yes.</span></span>
65. <span data-ttu-id="a3fd0-193">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-193">Click Add field to.</span></span>
66. <span data-ttu-id="a3fd0-194">Klik på Hvad skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-194">Click What to group.</span></span>
67. <span data-ttu-id="a3fd0-195">Udvid 'Varepost(Intrastat)' i træet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="a3fd0-196">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-196">Click Save.</span></span>
    * <span data-ttu-id="a3fd0-197">Bemærk, at feltet 'Udførelse' angiver, at denne gruppering udføres på kørselstidspunktet i hukommelsen, selv om der er ikke defineret nogen aggregeringer, og den valgte datakilde af typen 'Tabelposter' refererer til samme 'Intrastat'-tabel.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="a3fd0-198">Det skyldes, at datakilden indeholder nogle beregnede felter, som endnu ikke kan oversættes til SQL-databaseniveauet.</span><span class="sxs-lookup"><span data-stu-id="a3fd0-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  

