--- 
title: "Bruge en modeltilknytningskonfiguration til samlede beregninger på databaseniveau (ER)"
description: Denne procedure indeholder oplysninger om, hvordan du designer en ny modeltilknytningskonfiguration til elektronisk rapportering (ER) og bruger indbyggede ER-funktioner til effektive samlede beregninger.
author: NickSelin
manager: AnnBe
ms.date: 12/12/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 1dfb0d62f87f4bfdf4916fe2348bee5019841e93
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="use-a-model-mapping-configuration-for-aggregate-calculations-at-the-database-leveler"></a><span data-ttu-id="932ee-103">Bruge en modeltilknytningskonfiguration til samlede beregninger på databaseniveau (ER)</span><span class="sxs-lookup"><span data-stu-id="932ee-103">Use a model mapping configuration for aggregate calculations at the database level(ER)</span></span> 

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="932ee-104">Denne procedure indeholder oplysninger om, hvordan du designer en ny modeltilknytningskonfiguration til elektronisk rapportering (ER) og bruger indbyggede ER-funktioner til effektive samlede beregninger.</span><span class="sxs-lookup"><span data-stu-id="932ee-104">This procedure provides information about how to design a new Electronic reporting (ER) model mapping configuration and use built-in ER functions for efficient aggregate calculations.</span></span> <span data-ttu-id="932ee-105">I denne procedure skal du oprette en konfiguration til eksempelfirmaet Litware, Inc.</span><span class="sxs-lookup"><span data-stu-id="932ee-105">In this procedure you will create a configuration for the sample company, Litware, Inc.</span></span> 

<span data-ttu-id="932ee-106">Denne procedure er til brugere, der er tildelt rollen som Systemadministrator eller Elektronisk rapporteringsudvikler.</span><span class="sxs-lookup"><span data-stu-id="932ee-106">This procedure is created for users with the assigned role of System administrator or Electronic reporting developer.</span></span> <span data-ttu-id="932ee-107">Disse trin kan udføres ved hjælp af ethvert datasæt.</span><span class="sxs-lookup"><span data-stu-id="932ee-107">These steps can be completed using any dataset.</span></span>

 <span data-ttu-id="932ee-108">For at fuldføre disse trin, skal du først fuldføre trinnene i proceduren "ER forbedrer effektiviteten ved samlede beregninger ved at udføre dem på databaseniveau (Del 1: Forbered konfigurationer)".</span><span class="sxs-lookup"><span data-stu-id="932ee-108">To complete these steps, you must first complete the steps in the procedure, “ER improves the efficiency of aggregate calculations by performing them on database level (Part 1: Prepare configurations).”</span></span>

1. <span data-ttu-id="932ee-109">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="932ee-109">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="932ee-110">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-110">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="932ee-111">Vælg 'Intrastat-model\Intrastat-eksempeltilknytning' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-111">In the tree, select 'Intrastat model\Intrastat sample mapping'.</span></span>
4. <span data-ttu-id="932ee-112">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="932ee-112">Click Designer.</span></span>
5. <span data-ttu-id="932ee-113">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="932ee-113">Click Designer.</span></span>
6. <span data-ttu-id="932ee-114">Vælg 'Dynamics 365 for Operations\Tabelposter' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-114">In the tree, select 'Dynamics 365 for Operations\Table records'.</span></span>
7. <span data-ttu-id="932ee-115">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="932ee-115">Click Add root.</span></span>
    * <span data-ttu-id="932ee-116">Tilføj en ny datakilde, der repræsenterer poster, du vil gruppere.</span><span class="sxs-lookup"><span data-stu-id="932ee-116">Add a new data source representing records you want to group.</span></span>  
8. <span data-ttu-id="932ee-117">Skriv "Transaktioner" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="932ee-117">In the Name field, type 'Transactions'.</span></span>
    * <span data-ttu-id="932ee-118">Poster</span><span class="sxs-lookup"><span data-stu-id="932ee-118">Transactions</span></span>  
9. <span data-ttu-id="932ee-119">Skriv "Intrastat" i feltet Tabel.</span><span class="sxs-lookup"><span data-stu-id="932ee-119">In the Table field, type 'Intrastat'.</span></span>
    * <span data-ttu-id="932ee-120">Intrastat</span><span class="sxs-lookup"><span data-stu-id="932ee-120">Intrastat</span></span>  
10. <span data-ttu-id="932ee-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="932ee-121">Click OK.</span></span>
11. <span data-ttu-id="932ee-122">Vælg 'Funktioner\Gruppér efter' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-122">In the tree, select 'Functions\Group by'.</span></span>
    * <span data-ttu-id="932ee-123">Denne datakildetype bruges til at introducere en ny datakilde på kørselstidspunktet til at gruppere poster og beregne de krævede summeringer.</span><span class="sxs-lookup"><span data-stu-id="932ee-123">This data source type is used to introduce a new data source at run-time to group records and to calculate required aggregations.</span></span>  
12. <span data-ttu-id="932ee-124">Klik på Tilføj rod.</span><span class="sxs-lookup"><span data-stu-id="932ee-124">Click Add root.</span></span>
13. <span data-ttu-id="932ee-125">Skriv 'TransactionsGroups' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="932ee-125">In the Name field, type 'TransactionsGroups'.</span></span>
    * <span data-ttu-id="932ee-126">TransactionsGroups</span><span class="sxs-lookup"><span data-stu-id="932ee-126">TransactionsGroups</span></span>  
14. <span data-ttu-id="932ee-127">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="932ee-127">Click Edit group by.</span></span>
15. <span data-ttu-id="932ee-128">Vælg "Transaktioner}" i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-128">In the tree, select 'Transactions'.</span></span>
    * <span data-ttu-id="932ee-129">Vælg den tilføjede datakilde af typen 'Liste over poster', der repræsenterer de poster, du vil gruppere.</span><span class="sxs-lookup"><span data-stu-id="932ee-129">Select the added data source of the ‘Record list’ type that represents the records that you want to group.</span></span>  
16. <span data-ttu-id="932ee-130">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="932ee-130">Click Add field to.</span></span>
17. <span data-ttu-id="932ee-131">Klik på Hvad skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="932ee-131">Click What to group.</span></span>
18. <span data-ttu-id="932ee-132">Udvid "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-132">In the tree, expand 'Transactions'.</span></span>
19. <span data-ttu-id="932ee-133">Vælg "Transaktioner\Retning" i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-133">In the tree, select 'Transactions\Direction'.</span></span>
20. <span data-ttu-id="932ee-134">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="932ee-134">Click Add field to.</span></span>
21. <span data-ttu-id="932ee-135">Klik på Grupperede felter.</span><span class="sxs-lookup"><span data-stu-id="932ee-135">Click Grouped fields.</span></span>
    * <span data-ttu-id="932ee-136">Marker feltet for at angive grupperingsniveauet.</span><span class="sxs-lookup"><span data-stu-id="932ee-136">Select the field to specify the grouping level.</span></span> <span data-ttu-id="932ee-137">Ud fra dette valg returnerer datakilden på kørselstidspunktet så mange grupper af transaktioner, som der er retningskoder, der vil blive opfyldt i Intrastat-tabellen.</span><span class="sxs-lookup"><span data-stu-id="932ee-137">Based on this selection, the data source will return at run-time as many groups of transactions as there are direction codes that will be met in the Intrastat table.</span></span>  
22. <span data-ttu-id="932ee-138">Vælg 'Transaktioner\Fakturabeløb(AmountMST)' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-138">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
    * <span data-ttu-id="932ee-139">Marker feltet for at angive kilden til beregning af aggregering.</span><span class="sxs-lookup"><span data-stu-id="932ee-139">Select the field to specify the source for aggregation calculation.</span></span>  
23. <span data-ttu-id="932ee-140">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="932ee-140">Click Add field to.</span></span>
24. <span data-ttu-id="932ee-141">Klik på Aggregeringsfelter.</span><span class="sxs-lookup"><span data-stu-id="932ee-141">Click Aggregation fields.</span></span>
25. <span data-ttu-id="932ee-142">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="932ee-142">In the list, mark the selected row.</span></span>
26. <span data-ttu-id="932ee-143">Vælg 'Sum' i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="932ee-143">In the Method field, select 'Sum'.</span></span>
    * <span data-ttu-id="932ee-144">Vælg aggregeringstypen.</span><span class="sxs-lookup"><span data-stu-id="932ee-144">Select the aggregation type.</span></span>  
27. <span data-ttu-id="932ee-145">Skriv 'SumOfAmountMST' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="932ee-145">In the Name field, type 'SumOfAmountMST'.</span></span>
    * <span data-ttu-id="932ee-146">Angiv navnet på denne aggregering i datakilden, der er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="932ee-146">Specify the name of this aggregation in the configured data source.</span></span>  
28. <span data-ttu-id="932ee-147">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="932ee-147">Click Save.</span></span>
    * <span data-ttu-id="932ee-148">Bemærk, at feltet 'Udførelse' angiver, at denne gruppering udføres på kørselstidspunktet i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="932ee-148">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in the SQL database.</span></span>  
29. <span data-ttu-id="932ee-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="932ee-149">Close the page.</span></span>
30. <span data-ttu-id="932ee-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="932ee-150">Click OK.</span></span>
31. <span data-ttu-id="932ee-151">Udvid "Totaler" i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-151">In the tree, expand 'Totals'.</span></span>
32. <span data-ttu-id="932ee-152">Udvid 'TransactionsGroups' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-152">In the tree, expand 'TransactionsGroups'.</span></span>
33. <span data-ttu-id="932ee-153">Udvid "TransactionsGroups\aggregerede" i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-153">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
34. <span data-ttu-id="932ee-154">Vælg 'TransactionsGroups\aggregerede\SumOfAmountMST' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-154">In the tree, select 'TransactionsGroups\aggregated\SumOfAmountMST'.</span></span>
35. <span data-ttu-id="932ee-155">Vælg 'Totaler\Fakturaværdi i alt(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span><span class="sxs-lookup"><span data-stu-id="932ee-155">In the tree, select 'Totals\Total invoice value(TotalInvoiceValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded')'.</span></span>
36. <span data-ttu-id="932ee-156">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="932ee-156">Click Bind.</span></span>
    * <span data-ttu-id="932ee-157">Baseret på denne indstilling vil denne datakilde beregne summen af værdierne i feltet 'AmountMST' for de enkelte grupper af transaktioner.</span><span class="sxs-lookup"><span data-stu-id="932ee-157">Based on this setting, this data source will calculate the sum of values of the ‘AmountMST’ field for each groups of transactions.</span></span> <span data-ttu-id="932ee-158">Denne aggregeringsberegning vil være tilgængelig som elementet TransactionsGroups.aggregated.TotalAmount.</span><span class="sxs-lookup"><span data-stu-id="932ee-158">This aggregation calculation will be available as TransactionsGroups.aggregated.TotalAmount item.</span></span>  
37. <span data-ttu-id="932ee-159">Udvid 'TransactionsGroups' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-159">In the tree, expand 'TransactionsGroups'.</span></span>
38. <span data-ttu-id="932ee-160">Vælg "TransactionsGroups" i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-160">In the tree, select 'TransactionsGroups'.</span></span>
39. <span data-ttu-id="932ee-161">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="932ee-161">Click Edit.</span></span>
40. <span data-ttu-id="932ee-162">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="932ee-162">Click Edit group by.</span></span>
41. <span data-ttu-id="932ee-163">Udvid "Transaktioner" i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-163">In the tree, expand 'Transactions'.</span></span>
42. <span data-ttu-id="932ee-164">Vælg 'Transaktioner\Fakturabeløb(AmountMST)' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-164">In the tree, select 'Transactions\Invoice amount(AmountMST)'.</span></span>
43. <span data-ttu-id="932ee-165">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="932ee-165">Click Add field to.</span></span>
44. <span data-ttu-id="932ee-166">Klik på Aggregeringsfelter.</span><span class="sxs-lookup"><span data-stu-id="932ee-166">Click Aggregation fields.</span></span>
45. <span data-ttu-id="932ee-167">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="932ee-167">In the list, mark the selected row.</span></span>
46. <span data-ttu-id="932ee-168">Vælg 'Maks.' i feltet Metode.</span><span class="sxs-lookup"><span data-stu-id="932ee-168">In the Method field, select 'Max'.</span></span>
47. <span data-ttu-id="932ee-169">Skriv 'MaxOfAmountMST' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="932ee-169">In the Name field, type 'MaxOfAmountMST'.</span></span>
48. <span data-ttu-id="932ee-170">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="932ee-170">Click Save.</span></span>
    * <span data-ttu-id="932ee-171">Udførelse af GROUPBY-datakilder kan på nuværende tidspunkt oversættes til SQL-databaseniveauet med visse begrænsninger.</span><span class="sxs-lookup"><span data-stu-id="932ee-171">Currently, the execution of GROUPBY data sources can be translated to the SQL database level with some limitations.</span></span> <span data-ttu-id="932ee-172">Oversættelsen kan foretages for begge datakilder af typen 'Liste over poster' eller for datakilder, der er repræsenteret som et udtryk, der bruger funktionen FILTER.</span><span class="sxs-lookup"><span data-stu-id="932ee-172">Translation can be done for either data sources of the ‘Record list’ type or data sources represented as an expression using the FILTER function.</span></span> <span data-ttu-id="932ee-173">Den kan også udføres, når kun én sammenlægning er konfigureret til et enkelt felt i grupperingsposterne.</span><span class="sxs-lookup"><span data-stu-id="932ee-173">It can also be done when the only one aggregation is configured for a single field of the grouping records.</span></span>  
    * <span data-ttu-id="932ee-174">Bemærk, at selvom der var konfigureret mere end én aggregering til feltet AmountMST, angiver feltet 'Udførelse' stadig, at denne gruppering udføres på kørselstidspunktet i SQL-databasen.</span><span class="sxs-lookup"><span data-stu-id="932ee-174">Note that even though more than one aggregation was configured for the AmountMST field, the ‘Execution at’ field still indicates that this grouping will be performed at run-time in the SQL database.</span></span> <span data-ttu-id="932ee-175">Det skyldes, at kun én aggregering er bundet til datamodelelementet, og det bruges på kørselstidspunktet til at hente data fra denne datakilde.</span><span class="sxs-lookup"><span data-stu-id="932ee-175">This is because only one aggregation is bound to the data model item and will be used at run-time to pull data from this data source.</span></span>  
49. <span data-ttu-id="932ee-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="932ee-176">Close the page.</span></span>
50. <span data-ttu-id="932ee-177">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="932ee-177">Click OK.</span></span>
51. <span data-ttu-id="932ee-178">Udvid 'TransactionsGroups' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-178">In the tree, expand 'TransactionsGroups'.</span></span>
52. <span data-ttu-id="932ee-179">Udvid "TransactionsGroups\aggregerede" i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-179">In the tree, expand 'TransactionsGroups\aggregated'.</span></span>
53. <span data-ttu-id="932ee-180">Vælg 'TransactionsGroups\aggregerede\MaxOfAmountMST' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-180">In the tree, select 'TransactionsGroups\aggregated\MaxOfAmountMST'.</span></span>
54. <span data-ttu-id="932ee-181">Vælg 'Totaler\Total statistisk værdi(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0,0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span><span class="sxs-lookup"><span data-stu-id="932ee-181">In the tree, select 'Totals\Total statistical value(TotalStatisticalValue) = IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$StatisticalValueRounded')'.</span></span>
55. <span data-ttu-id="932ee-182">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="932ee-182">Click Bind.</span></span>
56. <span data-ttu-id="932ee-183">Udvid 'TransactionsGroups' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-183">In the tree, expand 'TransactionsGroups'.</span></span>
57. <span data-ttu-id="932ee-184">Vælg "TransactionsGroups" i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-184">In the tree, select 'TransactionsGroups'.</span></span>
58. <span data-ttu-id="932ee-185">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="932ee-185">Click Edit.</span></span>
59. <span data-ttu-id="932ee-186">Klik på Rediger gruppe efter.</span><span class="sxs-lookup"><span data-stu-id="932ee-186">Click Edit group by.</span></span>
    * <span data-ttu-id="932ee-187">Bemærk, at feltet 'Udførelse' angiver, at denne gruppering udføres på kørselstidspunktet i hukommelsen, fordi begge aggregeringer af det samme felt er bundet til datamodelelementerne.</span><span class="sxs-lookup"><span data-stu-id="932ee-187">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory because both aggregations of the same field are bound to the data model items.</span></span>   
60. <span data-ttu-id="932ee-188">Markér eller fjern markeringen af alle rækker på listen.</span><span class="sxs-lookup"><span data-stu-id="932ee-188">In the list, mark or unmark all rows.</span></span>
61. <span data-ttu-id="932ee-189">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="932ee-189">Click Delete.</span></span>
62. <span data-ttu-id="932ee-190">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="932ee-190">Click Yes.</span></span>
63. <span data-ttu-id="932ee-191">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="932ee-191">Click Delete.</span></span>
64. <span data-ttu-id="932ee-192">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="932ee-192">Click Yes.</span></span>
65. <span data-ttu-id="932ee-193">Klik på Tilføj et felt til.</span><span class="sxs-lookup"><span data-stu-id="932ee-193">Click Add field to.</span></span>
66. <span data-ttu-id="932ee-194">Klik på Hvad skal grupperes.</span><span class="sxs-lookup"><span data-stu-id="932ee-194">Click What to group.</span></span>
67. <span data-ttu-id="932ee-195">Udvid 'Varepost(Intrastat)' i træet.</span><span class="sxs-lookup"><span data-stu-id="932ee-195">In the tree, expand 'Commodity record(Intrastat)'.</span></span>
68. <span data-ttu-id="932ee-196">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="932ee-196">Click Save.</span></span>
    * <span data-ttu-id="932ee-197">Bemærk, at feltet 'Udførelse' angiver, at denne gruppering udføres på kørselstidspunktet i hukommelsen, selv om der er ikke defineret nogen aggregeringer, og den valgte datakilde af typen 'Tabelposter' refererer til samme 'Intrastat'-tabel.</span><span class="sxs-lookup"><span data-stu-id="932ee-197">Note that the ‘Execution at’ field indicates that this grouping will be performed at run-time in memory even though there are no aggregations defined and the selected data source of ‘Table records’ type refers to the same ‘Intrastat’ table.</span></span> <span data-ttu-id="932ee-198">Det skyldes, at datakilden indeholder nogle beregnede felter, som endnu ikke kan oversættes til SQL-databaseniveauet.</span><span class="sxs-lookup"><span data-stu-id="932ee-198">This is because the data source contains some calculated fields which can’t yet be translated to the SQL database level.</span></span>  

