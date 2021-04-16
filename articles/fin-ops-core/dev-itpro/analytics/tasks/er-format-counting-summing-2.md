---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 2: Konfigurer beregninger)'
description: Dette emne beskriver, hvordan du konfigurerer et format for elektronisk rapportering til optælling og opsummering baseret på data fra det allerede genererede tekstoutput. (Del 2)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, ERSolutionCreateDropDialog, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: a14fe079515b176cbcda74852ae2ad456dd6434a
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5749015"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="a0a90-104">ER Konfigurere format for at udføre optælling og sammenlægning (del 2: Konfigurer beregninger)</span><span class="sxs-lookup"><span data-stu-id="a0a90-104">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a0a90-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="a0a90-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="a0a90-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="a0a90-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 1: Oprettelsesformat)".</span><span class="sxs-lookup"><span data-stu-id="a0a90-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="a0a90-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="a0a90-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="a0a90-109">Opret en formatkonfiguration for at tilføje optællings- og sammenlægningsdetaljer</span><span class="sxs-lookup"><span data-stu-id="a0a90-109">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="a0a90-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="a0a90-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="a0a90-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="a0a90-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="a0a90-112">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="a0a90-113">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-113">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="a0a90-114">Antag, at du skal tilpasse det format, der leveres af Microsoft, ved at tilføje linjer med oversigtsdetaljerne i slutningen af Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="a0a90-114">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="a0a90-115">Det skal du gøre ved at aflede din egen forekomst af Intrastat-konfigurationen fra Microsofts forekomst for at foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="a0a90-115">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="a0a90-116">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a0a90-116">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="a0a90-117">Skriv 'Afled fra navn: Intrastat (DE), Microsoft' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="a0a90-117">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="a0a90-118">Skriv 'Intrastat (DE) med optælling og sammenlægning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a0a90-118">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="a0a90-119">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="a0a90-119">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="a0a90-120">Konfigurer denne rapport til at udføre optælling og sammenlægning baseret på oplysninger om output</span><span class="sxs-lookup"><span data-stu-id="a0a90-120">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="a0a90-121">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="a0a90-121">Click Designer.</span></span>
2. <span data-ttu-id="a0a90-122">Vælg Ja i feltet Detaljer om indsamlingsoutput.</span><span class="sxs-lookup"><span data-stu-id="a0a90-122">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="a0a90-123">Dette flag aktiverer på kørselstidspunktet processen til indsamling af outputdetaljer til generering af Intrastat-filen.</span><span class="sxs-lookup"><span data-stu-id="a0a90-123">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="a0a90-124">Du skal foretage optælling for forskellige Intrastat-retninger, så føj en dedikeret modeloptælling til datakildernes liste over denne formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="a0a90-124">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="a0a90-125">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="a0a90-125">Click the Mapping tab.</span></span>
4. <span data-ttu-id="a0a90-126">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a0a90-126">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="a0a90-127">Vælg 'Datamodel\Optælling' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-127">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="a0a90-128">Skriv 'Retning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a0a90-128">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="a0a90-129">Indtast eller vælg en værdi i feltet Modelfasttekst.</span><span class="sxs-lookup"><span data-stu-id="a0a90-129">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="a0a90-130">Vælg værdien Retning.</span><span class="sxs-lookup"><span data-stu-id="a0a90-130">Select the value Direction.</span></span>  
8. <span data-ttu-id="a0a90-131">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a0a90-131">Click OK.</span></span>
9. <span data-ttu-id="a0a90-132">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a0a90-132">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="a0a90-133">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-133">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="a0a90-134">Skriv '$BlockName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a0a90-134">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="a0a90-135">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-135">Click Edit formula.</span></span>
13. <span data-ttu-id="a0a90-136">Skriv "bloker" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-136">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="a0a90-137">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-137">Click Save.</span></span>
15. <span data-ttu-id="a0a90-138">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-138">Close the page.</span></span>
16. <span data-ttu-id="a0a90-139">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a0a90-139">Click OK.</span></span>
17. <span data-ttu-id="a0a90-140">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a0a90-140">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="a0a90-141">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-141">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="a0a90-142">Skriv '$RecName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a0a90-142">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="a0a90-143">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-143">Click Edit formula.</span></span>
21. <span data-ttu-id="a0a90-144">Skriv "post" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-144">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="a0a90-145">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-145">Click Save.</span></span>
23. <span data-ttu-id="a0a90-146">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-146">Close the page.</span></span>
24. <span data-ttu-id="a0a90-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a0a90-147">Click OK.</span></span>
25. <span data-ttu-id="a0a90-148">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="a0a90-148">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="a0a90-149">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-149">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="a0a90-150">Skriv '$InvName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="a0a90-150">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="a0a90-151">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-151">Click Edit formula.</span></span>
29. <span data-ttu-id="a0a90-152">Skriv '"InvoicedAmountEUR"' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-152">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="a0a90-153">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-153">Click Save.</span></span>
31. <span data-ttu-id="a0a90-154">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-154">Close the page.</span></span>
32. <span data-ttu-id="a0a90-155">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="a0a90-155">Click OK.</span></span>
33. <span data-ttu-id="a0a90-156">Vælg 'Intrastat\Data' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-156">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="a0a90-157">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="a0a90-157">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="a0a90-158">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="a0a90-158">Click Add data source.</span></span>
    * <span data-ttu-id="a0a90-159">$BlockName</span><span class="sxs-lookup"><span data-stu-id="a0a90-159">$BlockName</span></span>  
36. <span data-ttu-id="a0a90-160">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-160">Click Save.</span></span>
37. <span data-ttu-id="a0a90-161">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-161">Close the page.</span></span>
38. <span data-ttu-id="a0a90-162">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="a0a90-162">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="a0a90-163">Skriv 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-163">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="a0a90-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="a0a90-164">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="a0a90-165">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-165">Click Save.</span></span>
41. <span data-ttu-id="a0a90-166">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-166">Close the page.</span></span>
    * <span data-ttu-id="a0a90-167">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a0a90-167">Count the lines of this sequence.</span></span> <span data-ttu-id="a0a90-168">Resultaterne skal bruges sammen med navnet "bloker" separat for forskellige retninger.</span><span class="sxs-lookup"><span data-stu-id="a0a90-168">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="a0a90-169">"Import" vil blive brugt til enhver Intrastat-postering for indførsel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-169">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="a0a90-170">Værdien "Eksport" vil blive brugt til enhver Intrastat-postering for udførsel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-170">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="a0a90-171">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="a0a90-171">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="a0a90-172">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="a0a90-172">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="a0a90-173">Udvid 'Intrastat\Data: Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-173">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="a0a90-174">Vælg 'Intrastat\Data: Sequence\Arrivals?' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-174">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="a0a90-175">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="a0a90-175">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="a0a90-176">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a0a90-176">Count the lines of this sequence.</span></span> <span data-ttu-id="a0a90-177">Resultaterne huskes med navnet "post".</span><span class="sxs-lookup"><span data-stu-id="a0a90-177">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="a0a90-178">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-178">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="a0a90-179">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="a0a90-179">Click Add data source.</span></span>
47. <span data-ttu-id="a0a90-180">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-180">Click Save.</span></span>
48. <span data-ttu-id="a0a90-181">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-181">Close the page.</span></span>
49. <span data-ttu-id="a0a90-182">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="a0a90-182">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="a0a90-183">Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-183">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="a0a90-184">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-184">Click Save.</span></span>
52. <span data-ttu-id="a0a90-185">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-185">Close the page.</span></span>
    * <span data-ttu-id="a0a90-186">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a0a90-186">Count the lines of this sequence.</span></span> <span data-ttu-id="a0a90-187">Resultaterne skal bruges sammen med navnet "post" separat for forskellige varekoder.</span><span class="sxs-lookup"><span data-stu-id="a0a90-187">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="a0a90-188">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="a0a90-188">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="a0a90-189">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksporter" i overensstemmelse hermed, og den anden blok "post"udfyldes med varekodeværdien.</span><span class="sxs-lookup"><span data-stu-id="a0a90-189">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="a0a90-190">Vælg 'Intrastat\Data: Sequence\Dispatches?' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-190">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="a0a90-191">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="a0a90-191">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="a0a90-192">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-192">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="a0a90-193">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="a0a90-193">Click Add data source.</span></span>
57. <span data-ttu-id="a0a90-194">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-194">Click Save.</span></span>
58. <span data-ttu-id="a0a90-195">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-195">Close the page.</span></span>
59. <span data-ttu-id="a0a90-196">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="a0a90-196">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="a0a90-197">Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="a0a90-197">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="a0a90-198">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-198">Click Save.</span></span>
62. <span data-ttu-id="a0a90-199">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-199">Close the page.</span></span>
63. <span data-ttu-id="a0a90-200">Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="a0a90-201">Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-201">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="a0a90-202">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="a0a90-202">Click the Format tab.</span></span>
66. <span data-ttu-id="a0a90-203">Vælg 'Intrastat\Data\Dispatches\Record\Fakturabeløb EUR' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-203">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="a0a90-204">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="a0a90-204">Click the Mapping tab.</span></span>
68. <span data-ttu-id="a0a90-205">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="a0a90-205">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="a0a90-206">Vælg '$InvName' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-206">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="a0a90-207">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="a0a90-207">Click Add data source.</span></span>
71. <span data-ttu-id="a0a90-208">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-208">Click Save.</span></span>
72. <span data-ttu-id="a0a90-209">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-209">Close the page.</span></span>
    * <span data-ttu-id="a0a90-210">Sammenlæg de fakturerede beløbsværdier for linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="a0a90-210">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="a0a90-211">Resultaterne skal bruges sammen med navnet "InvoicedAmountEUR" separat for forskellige Intrastat-retninger og varekoder.</span><span class="sxs-lookup"><span data-stu-id="a0a90-211">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="a0a90-212">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="a0a90-212">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="a0a90-213">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="a0a90-213">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="a0a90-214">Den anden blok "post" udfyldes med varekodeværdien, og den tredje kolonne "InvoicedAmountEUR" udfyldes med en fakturabeløbsværdien.</span><span class="sxs-lookup"><span data-stu-id="a0a90-214">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="a0a90-215">Udvid 'Intrastat\Data\Arrivals?' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-215">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="a0a90-216">Udvid 'Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-216">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="a0a90-217">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="a0a90-217">Click the Format tab.</span></span>
76. <span data-ttu-id="a0a90-218">Vælg 'Intrastat\Data\Arrivals\Record\Fakturabeløb EUR' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-218">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="a0a90-219">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="a0a90-219">Click the Mapping tab.</span></span>
78. <span data-ttu-id="a0a90-220">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="a0a90-220">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="a0a90-221">Vælg '$InvName' i træet.</span><span class="sxs-lookup"><span data-stu-id="a0a90-221">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="a0a90-222">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="a0a90-222">Click Add data source.</span></span>
81. <span data-ttu-id="a0a90-223">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-223">Click Save.</span></span>
82. <span data-ttu-id="a0a90-224">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-224">Close the page.</span></span>
83. <span data-ttu-id="a0a90-225">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="a0a90-225">Click Save.</span></span>
84. <span data-ttu-id="a0a90-226">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="a0a90-226">Close the page.</span></span>



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]