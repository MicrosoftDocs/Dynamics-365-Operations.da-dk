--- 
title: "Konfigurere beregninger for at foretage optælling og opsummering"
description: "Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet."
author: NickSelin
manager: AnnBe
ms.date: 10/28/2016
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
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: d41ce101c0b038627e2baf6b5eac2410095af7ce
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="configure-computations-to-do-counting-and-summing"></a><span data-ttu-id="18573-103">Konfigurere beregninger for at foretage optælling og opsummering</span><span class="sxs-lookup"><span data-stu-id="18573-103">Configure computations to do counting and summing</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="18573-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="18573-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="18573-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="18573-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="18573-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 1: Oprettelsesformat)".</span><span class="sxs-lookup"><span data-stu-id="18573-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 1: Create format)” procedure.</span></span>

<span data-ttu-id="18573-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="18573-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="18573-108">Opret en formatkonfiguration for at tilføje optællings- og sammenlægningsdetaljer</span><span class="sxs-lookup"><span data-stu-id="18573-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="18573-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="18573-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="18573-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="18573-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="18573-111">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="18573-112">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="18573-113">Antag, at du skal tilpasse det format, der leveres af Microsoft, ved at tilføje linjer med oversigtsdetaljerne i slutningen af Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="18573-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="18573-114">Det skal du gøre ved at aflede din egen forekomst af Intrastat-konfigurationen fra Microsofts forekomst for at foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="18573-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="18573-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="18573-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="18573-116">Skriv 'Afled fra navn: Intrastat (DE), Microsoft' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="18573-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="18573-117">Skriv 'Intrastat (DE) med optælling og sammenlægning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="18573-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="18573-118">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="18573-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="18573-119">Konfigurer denne rapport til at udføre optælling og sammenlægning baseret på oplysninger om output</span><span class="sxs-lookup"><span data-stu-id="18573-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="18573-120">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="18573-120">Click Designer.</span></span>
2. <span data-ttu-id="18573-121">Vælg Ja i feltet Detaljer om indsamlingsoutput.</span><span class="sxs-lookup"><span data-stu-id="18573-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="18573-122">Dette flag aktiverer på kørselstidspunktet processen til indsamling af outputdetaljer til generering af Intrastat-filen.</span><span class="sxs-lookup"><span data-stu-id="18573-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="18573-123">Du skal foretage optælling for forskellige Intrastat-retninger, så føj en dedikeret modeloptælling til datakildens liste over denne formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="18573-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources’ list of this format configuration.</span></span>  
3. <span data-ttu-id="18573-124">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="18573-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="18573-125">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="18573-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="18573-126">Vælg 'Datamodel\Optælling' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="18573-127">Skriv 'Retning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="18573-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="18573-128">Indtast eller vælg en værdi i feltet Modelfasttekst.</span><span class="sxs-lookup"><span data-stu-id="18573-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="18573-129">Vælg værdien Retning.</span><span class="sxs-lookup"><span data-stu-id="18573-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="18573-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="18573-130">Click OK.</span></span>
9. <span data-ttu-id="18573-131">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="18573-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="18573-132">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="18573-133">Skriv '$BlockName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="18573-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="18573-134">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="18573-134">Click Edit formula.</span></span>
13. <span data-ttu-id="18573-135">Skriv "bloker" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="18573-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="18573-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-136">Click Save.</span></span>
15. <span data-ttu-id="18573-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-137">Close the page.</span></span>
16. <span data-ttu-id="18573-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="18573-138">Click OK.</span></span>
17. <span data-ttu-id="18573-139">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="18573-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="18573-140">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="18573-141">Skriv '$RecName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="18573-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="18573-142">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="18573-142">Click Edit formula.</span></span>
21. <span data-ttu-id="18573-143">Skriv "post" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="18573-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="18573-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-144">Click Save.</span></span>
23. <span data-ttu-id="18573-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-145">Close the page.</span></span>
24. <span data-ttu-id="18573-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="18573-146">Click OK.</span></span>
25. <span data-ttu-id="18573-147">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="18573-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="18573-148">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="18573-149">Skriv '$InvName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="18573-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="18573-150">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="18573-150">Click Edit formula.</span></span>
29. <span data-ttu-id="18573-151">Skriv '"InvoicedAmountEUR"' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="18573-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="18573-152">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-152">Click Save.</span></span>
31. <span data-ttu-id="18573-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-153">Close the page.</span></span>
32. <span data-ttu-id="18573-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="18573-154">Click OK.</span></span>
33. <span data-ttu-id="18573-155">Vælg 'Intrastat\Data' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="18573-156">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="18573-156">Click Edit button for the ‘Collected data key name’ field</span></span>
35. <span data-ttu-id="18573-157">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="18573-157">Click Add data source.</span></span>
    * <span data-ttu-id="18573-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="18573-158">$BlockName</span></span>  
36. <span data-ttu-id="18573-159">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-159">Click Save.</span></span>
37. <span data-ttu-id="18573-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-160">Close the page.</span></span>
38. <span data-ttu-id="18573-161">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="18573-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="18573-162">Skriv 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="18573-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="18573-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="18573-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="18573-164">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-164">Click Save.</span></span>
41. <span data-ttu-id="18573-165">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-165">Close the page.</span></span>
    * <span data-ttu-id="18573-166">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="18573-166">Count the lines of this sequence.</span></span> <span data-ttu-id="18573-167">Resultaterne skal bruges sammen med navnet "bloker" separat for forskellige retninger.</span><span class="sxs-lookup"><span data-stu-id="18573-167">The results will be used with the name “block” separately for different directions.</span></span> <span data-ttu-id="18573-168">"Import" vil blive brugt til enhver Intrastat-postering for indførsel.</span><span class="sxs-lookup"><span data-stu-id="18573-168">Value “Import” will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="18573-169">Værdien "Eksport" vil blive brugt til enhver Intrastat-postering for udførsel.</span><span class="sxs-lookup"><span data-stu-id="18573-169">The value “Export” will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="18573-170">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="18573-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="18573-171">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="18573-171">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span>  
42. <span data-ttu-id="18573-172">Udvid 'Intrastat\Data: Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="18573-173">Vælg 'Intrastat\Data: Sequence\Arrivals?' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="18573-174">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="18573-174">Click Edit button for the ‘Collected data key name’ field.</span></span>
    * <span data-ttu-id="18573-175">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="18573-175">Count the lines of this sequence.</span></span> <span data-ttu-id="18573-176">Resultaterne huskes med navnet "post".</span><span class="sxs-lookup"><span data-stu-id="18573-176">The results will be memorized using the name “record”.</span></span>  
45. <span data-ttu-id="18573-177">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="18573-178">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="18573-178">Click Add data source.</span></span>
47. <span data-ttu-id="18573-179">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-179">Click Save.</span></span>
48. <span data-ttu-id="18573-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-180">Close the page.</span></span>
49. <span data-ttu-id="18573-181">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="18573-181">Click Edit button for the ‘Collected data key value’ field</span></span>
50. <span data-ttu-id="18573-182">Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="18573-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="18573-183">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-183">Click Save.</span></span>
52. <span data-ttu-id="18573-184">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-184">Close the page.</span></span>
    * <span data-ttu-id="18573-185">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="18573-185">Count the lines of this sequence.</span></span> <span data-ttu-id="18573-186">Resultaterne skal bruges sammen med navnet "post" separat for forskellige varekoder.</span><span class="sxs-lookup"><span data-stu-id="18573-186">The results will be used with the name “record” separately for different commodity codes.</span></span> <span data-ttu-id="18573-187">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="18573-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="18573-188">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksporter" i overensstemmelse hermed, og den anden blok "post"udfyldes med varekodeværdien.</span><span class="sxs-lookup"><span data-stu-id="18573-188">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly and the second block “record” is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="18573-189">Vælg 'Intrastat\Data: Sequence\Dispatches?' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="18573-190">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="18573-190">Click Edit button for the ‘Collected data key name’ field</span></span>
55. <span data-ttu-id="18573-191">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="18573-192">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="18573-192">Click Add data source.</span></span>
57. <span data-ttu-id="18573-193">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-193">Click Save.</span></span>
58. <span data-ttu-id="18573-194">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-194">Close the page.</span></span>
59. <span data-ttu-id="18573-195">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="18573-195">Click the Edit button for the ‘Collected data key value’ field.</span></span>
60. <span data-ttu-id="18573-196">Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="18573-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="18573-197">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-197">Click Save.</span></span>
62. <span data-ttu-id="18573-198">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-198">Close the page.</span></span>
63. <span data-ttu-id="18573-199">Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="18573-200">Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="18573-201">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="18573-201">Click the Format tab.</span></span>
66. <span data-ttu-id="18573-202">Vælg 'Intrastat\Data\Dispatches\Record\Fakturabeløb EUR' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="18573-203">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="18573-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="18573-204">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="18573-204">Click the Edit button for the ‘Collected data key name’ field.</span></span>
69. <span data-ttu-id="18573-205">Vælg '$InvName' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="18573-206">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="18573-206">Click Add data source.</span></span>
71. <span data-ttu-id="18573-207">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-207">Click Save.</span></span>
72. <span data-ttu-id="18573-208">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-208">Close the page.</span></span>
    * <span data-ttu-id="18573-209">Sammenlæg de fakturerede beløbsværdier for linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="18573-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="18573-210">Resultaterne skal bruges sammen med navnet "InvoicedAmountEUR" separat for forskellige Intrastat-retninger og varekoder.</span><span class="sxs-lookup"><span data-stu-id="18573-210">The results will be used with the name “InvoicedAmountEUR” separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="18573-211">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="18573-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="18573-212">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="18573-212">For each transaction a row where the first column “block” is filled with the values “Import” and “Export” accordingly.</span></span> <span data-ttu-id="18573-213">Den anden blok "post" udfyldes med varekodeværdien, og den tredje kolonne "InvoicedAmountEUR" udfyldes med en fakturabeløbsværdien.</span><span class="sxs-lookup"><span data-stu-id="18573-213">The second block “record” is filled with the commodity code value, and the third column “InvoicedAmountEUR” is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="18573-214">Udvid 'Intrastat\Data\Arrivals?' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="18573-215">Udvid 'Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="18573-216">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="18573-216">Click the Format tab.</span></span>
76. <span data-ttu-id="18573-217">Vælg 'Intrastat\Data\Arrivals\Record\Fakturabeløb EUR' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="18573-218">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="18573-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="18573-219">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="18573-219">Click the Edit button for the ‘Collected data key name’ field.</span></span>
79. <span data-ttu-id="18573-220">Vælg '$InvName' i træet.</span><span class="sxs-lookup"><span data-stu-id="18573-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="18573-221">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="18573-221">Click Add data source.</span></span>
81. <span data-ttu-id="18573-222">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-222">Click Save.</span></span>
82. <span data-ttu-id="18573-223">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-223">Close the page.</span></span>
83. <span data-ttu-id="18573-224">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="18573-224">Click Save.</span></span>
84. <span data-ttu-id="18573-225">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="18573-225">Close the page.</span></span>


