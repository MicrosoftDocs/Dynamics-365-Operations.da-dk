---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 2: Konfigurer beregninger)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2d785b321037645837dbcbaf28c8ede9b8e97b79
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550596"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="e3a11-103">ER Konfigurere format for at udføre optælling og sammenlægning (del 2: Konfigurer beregninger)</span><span class="sxs-lookup"><span data-stu-id="e3a11-103">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e3a11-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="e3a11-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="e3a11-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="e3a11-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 1: Oprettelsesformat)".</span><span class="sxs-lookup"><span data-stu-id="e3a11-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="e3a11-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="e3a11-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="e3a11-108">Opret en formatkonfiguration for at tilføje optællings- og sammenlægningsdetaljer</span><span class="sxs-lookup"><span data-stu-id="e3a11-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="e3a11-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="e3a11-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="e3a11-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="e3a11-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="e3a11-111">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="e3a11-112">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="e3a11-113">Antag, at du skal tilpasse det format, der leveres af Microsoft, ved at tilføje linjer med oversigtsdetaljerne i slutningen af Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="e3a11-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="e3a11-114">Det skal du gøre ved at aflede din egen forekomst af Intrastat-konfigurationen fra Microsofts forekomst for at foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="e3a11-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="e3a11-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e3a11-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="e3a11-116">Skriv 'Afled fra navn: Intrastat (DE), Microsoft' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="e3a11-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="e3a11-117">Skriv 'Intrastat (DE) med optælling og sammenlægning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e3a11-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="e3a11-118">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="e3a11-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="e3a11-119">Konfigurer denne rapport til at udføre optælling og sammenlægning baseret på oplysninger om output</span><span class="sxs-lookup"><span data-stu-id="e3a11-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="e3a11-120">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="e3a11-120">Click Designer.</span></span>
2. <span data-ttu-id="e3a11-121">Vælg Ja i feltet Detaljer om indsamlingsoutput.</span><span class="sxs-lookup"><span data-stu-id="e3a11-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="e3a11-122">Dette flag aktiverer på kørselstidspunktet processen til indsamling af outputdetaljer til generering af Intrastat-filen.</span><span class="sxs-lookup"><span data-stu-id="e3a11-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="e3a11-123">Du skal foretage optælling for forskellige Intrastat-retninger, så føj en dedikeret modeloptælling til datakildens liste over denne formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e3a11-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="e3a11-124">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="e3a11-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="e3a11-125">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e3a11-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="e3a11-126">Vælg 'Datamodel\Optælling' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="e3a11-127">Skriv 'Retning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e3a11-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="e3a11-128">Indtast eller vælg en værdi i feltet Modelfasttekst.</span><span class="sxs-lookup"><span data-stu-id="e3a11-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="e3a11-129">Vælg værdien Retning.</span><span class="sxs-lookup"><span data-stu-id="e3a11-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="e3a11-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e3a11-130">Click OK.</span></span>
9. <span data-ttu-id="e3a11-131">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e3a11-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="e3a11-132">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="e3a11-133">Skriv '$BlockName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e3a11-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="e3a11-134">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-134">Click Edit formula.</span></span>
13. <span data-ttu-id="e3a11-135">Skriv "bloker" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="e3a11-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-136">Click Save.</span></span>
15. <span data-ttu-id="e3a11-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-137">Close the page.</span></span>
16. <span data-ttu-id="e3a11-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e3a11-138">Click OK.</span></span>
17. <span data-ttu-id="e3a11-139">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e3a11-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="e3a11-140">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="e3a11-141">Skriv '$RecName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e3a11-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="e3a11-142">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-142">Click Edit formula.</span></span>
21. <span data-ttu-id="e3a11-143">Skriv "post" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="e3a11-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-144">Click Save.</span></span>
23. <span data-ttu-id="e3a11-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-145">Close the page.</span></span>
24. <span data-ttu-id="e3a11-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e3a11-146">Click OK.</span></span>
25. <span data-ttu-id="e3a11-147">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e3a11-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="e3a11-148">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="e3a11-149">Skriv '$InvName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="e3a11-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="e3a11-150">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-150">Click Edit formula.</span></span>
29. <span data-ttu-id="e3a11-151">Skriv '"InvoicedAmountEUR"' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="e3a11-152">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-152">Click Save.</span></span>
31. <span data-ttu-id="e3a11-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-153">Close the page.</span></span>
32. <span data-ttu-id="e3a11-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e3a11-154">Click OK.</span></span>
33. <span data-ttu-id="e3a11-155">Vælg 'Intrastat\Data' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="e3a11-156">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="e3a11-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="e3a11-157">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="e3a11-157">Click Add data source.</span></span>
    * <span data-ttu-id="e3a11-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="e3a11-158">$BlockName</span></span>  
36. <span data-ttu-id="e3a11-159">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-159">Click Save.</span></span>
37. <span data-ttu-id="e3a11-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-160">Close the page.</span></span>
38. <span data-ttu-id="e3a11-161">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="e3a11-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="e3a11-162">Skriv 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="e3a11-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="e3a11-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="e3a11-164">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-164">Click Save.</span></span>
41. <span data-ttu-id="e3a11-165">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-165">Close the page.</span></span>
    * <span data-ttu-id="e3a11-166">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e3a11-166">Count the lines of this sequence.</span></span> <span data-ttu-id="e3a11-167">Resultaterne skal bruges sammen med navnet "bloker" separat for forskellige retninger.</span><span class="sxs-lookup"><span data-stu-id="e3a11-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="e3a11-168">"Import" vil blive brugt til enhver Intrastat-postering for indførsel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="e3a11-169">Værdien "Eksport" vil blive brugt til enhver Intrastat-postering for udførsel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="e3a11-170">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="e3a11-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="e3a11-171">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="e3a11-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="e3a11-172">Udvid 'Intrastat\Data: Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="e3a11-173">Vælg 'Intrastat\Data: Sequence\Arrivals?' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="e3a11-174">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="e3a11-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="e3a11-175">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e3a11-175">Count the lines of this sequence.</span></span> <span data-ttu-id="e3a11-176">Resultaterne huskes med navnet "post".</span><span class="sxs-lookup"><span data-stu-id="e3a11-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="e3a11-177">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="e3a11-178">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="e3a11-178">Click Add data source.</span></span>
47. <span data-ttu-id="e3a11-179">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-179">Click Save.</span></span>
48. <span data-ttu-id="e3a11-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-180">Close the page.</span></span>
49. <span data-ttu-id="e3a11-181">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="e3a11-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="e3a11-182">Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="e3a11-183">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-183">Click Save.</span></span>
52. <span data-ttu-id="e3a11-184">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-184">Close the page.</span></span>
    * <span data-ttu-id="e3a11-185">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e3a11-185">Count the lines of this sequence.</span></span> <span data-ttu-id="e3a11-186">Resultaterne skal bruges sammen med navnet "post" separat for forskellige varekoder.</span><span class="sxs-lookup"><span data-stu-id="e3a11-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="e3a11-187">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="e3a11-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="e3a11-188">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksporter" i overensstemmelse hermed, og den anden blok "post"udfyldes med varekodeværdien.</span><span class="sxs-lookup"><span data-stu-id="e3a11-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="e3a11-189">Vælg 'Intrastat\Data: Sequence\Dispatches?' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="e3a11-190">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="e3a11-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="e3a11-191">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="e3a11-192">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="e3a11-192">Click Add data source.</span></span>
57. <span data-ttu-id="e3a11-193">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-193">Click Save.</span></span>
58. <span data-ttu-id="e3a11-194">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-194">Close the page.</span></span>
59. <span data-ttu-id="e3a11-195">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="e3a11-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="e3a11-196">Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="e3a11-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="e3a11-197">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-197">Click Save.</span></span>
62. <span data-ttu-id="e3a11-198">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-198">Close the page.</span></span>
63. <span data-ttu-id="e3a11-199">Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="e3a11-200">Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="e3a11-201">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="e3a11-201">Click the Format tab.</span></span>
66. <span data-ttu-id="e3a11-202">Vælg 'Intrastat\Data\Dispatches\Record\Fakturabeløb EUR' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="e3a11-203">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="e3a11-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="e3a11-204">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="e3a11-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="e3a11-205">Vælg '$InvName' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="e3a11-206">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="e3a11-206">Click Add data source.</span></span>
71. <span data-ttu-id="e3a11-207">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-207">Click Save.</span></span>
72. <span data-ttu-id="e3a11-208">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-208">Close the page.</span></span>
    * <span data-ttu-id="e3a11-209">Sammenlæg de fakturerede beløbsværdier for linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="e3a11-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="e3a11-210">Resultaterne skal bruges sammen med navnet "InvoicedAmountEUR" separat for forskellige Intrastat-retninger og varekoder.</span><span class="sxs-lookup"><span data-stu-id="e3a11-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="e3a11-211">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="e3a11-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="e3a11-212">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="e3a11-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="e3a11-213">Den anden blok "post" udfyldes med varekodeværdien, og den tredje kolonne "InvoicedAmountEUR" udfyldes med en fakturabeløbsværdien.</span><span class="sxs-lookup"><span data-stu-id="e3a11-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="e3a11-214">Udvid 'Intrastat\Data\Arrivals?' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="e3a11-215">Udvid 'Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="e3a11-216">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="e3a11-216">Click the Format tab.</span></span>
76. <span data-ttu-id="e3a11-217">Vælg 'Intrastat\Data\Arrivals\Record\Fakturabeløb EUR' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="e3a11-218">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="e3a11-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="e3a11-219">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="e3a11-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="e3a11-220">Vælg '$InvName' i træet.</span><span class="sxs-lookup"><span data-stu-id="e3a11-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="e3a11-221">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="e3a11-221">Click Add data source.</span></span>
81. <span data-ttu-id="e3a11-222">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-222">Click Save.</span></span>
82. <span data-ttu-id="e3a11-223">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-223">Close the page.</span></span>
83. <span data-ttu-id="e3a11-224">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="e3a11-224">Click Save.</span></span>
84. <span data-ttu-id="e3a11-225">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3a11-225">Close the page.</span></span>

