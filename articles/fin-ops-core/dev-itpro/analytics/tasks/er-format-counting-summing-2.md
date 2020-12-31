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
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9314a8cd5838333a20dd59dfb52f80a43d89b8c6
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4684685"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-2---configure-computations"></a><span data-ttu-id="0d4ad-103">ER Konfigurere format for at udføre optælling og sammenlægning (del 2: Konfigurer beregninger)</span><span class="sxs-lookup"><span data-stu-id="0d4ad-103">ER Configure format to do counting and summing (Part 2 - Configure computations)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0d4ad-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="0d4ad-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="0d4ad-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 1: Oprettelsesformat)".</span><span class="sxs-lookup"><span data-stu-id="0d4ad-106">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 1: Create format)" procedure.</span></span>

<span data-ttu-id="0d4ad-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="create-a-format-configuration-to-add-counting-and-summing-details"></a><span data-ttu-id="0d4ad-108">Opret en formatkonfiguration for at tilføje optællings- og sammenlægningsdetaljer</span><span class="sxs-lookup"><span data-stu-id="0d4ad-108">Create a format configuration to add counting and summing details</span></span>
1. <span data-ttu-id="0d4ad-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="0d4ad-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="0d4ad-111">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="0d4ad-112">Vælg 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-112">In the tree, select 'Intrastat model\Intrastat (DE)'.</span></span>
    * <span data-ttu-id="0d4ad-113">Antag, at du skal tilpasse det format, der leveres af Microsoft, ved at tilføje linjer med oversigtsdetaljerne i slutningen af Intrastat-rapporten.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-113">Assume that you need to customize the format provided by Microsoft by adding lines with summary details at the end of the Intrastat report.</span></span> <span data-ttu-id="0d4ad-114">Det skal du gøre ved at aflede din egen forekomst af Intrastat-konfigurationen fra Microsofts forekomst for at foretage ændringer.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-114">You need to do that by deriving our own instance of the Intrastat configuration from the Microsoft instance to make modifications.</span></span>  
5. <span data-ttu-id="0d4ad-115">Klik på Opret konfiguration for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-115">Click Create configuration to open the drop dialog.</span></span>
6. <span data-ttu-id="0d4ad-116">Skriv 'Afled fra navn: Intrastat (DE), Microsoft' i feltet Ny.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-116">In the New field, enter 'Derive from Name: Intrastat (DE), Microsoft'.</span></span>
7. <span data-ttu-id="0d4ad-117">Skriv 'Intrastat (DE) med optælling og sammenlægning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-117">In the Name field, type 'Intrastat (DE) with counting & summing'.</span></span>
8. <span data-ttu-id="0d4ad-118">Klik på Opret konfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-118">Click Create configuration.</span></span>

## <a name="configure-this-report-to-do-counting-and-summation-based-on-output-details"></a><span data-ttu-id="0d4ad-119">Konfigurer denne rapport til at udføre optælling og sammenlægning baseret på oplysninger om output</span><span class="sxs-lookup"><span data-stu-id="0d4ad-119">Configure this report to do counting and summation based on output details</span></span>
1. <span data-ttu-id="0d4ad-120">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-120">Click Designer.</span></span>
2. <span data-ttu-id="0d4ad-121">Vælg Ja i feltet Detaljer om indsamlingsoutput.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-121">Select Yes in the Collect output details field.</span></span>
    * <span data-ttu-id="0d4ad-122">Dette flag aktiverer på kørselstidspunktet processen til indsamling af outputdetaljer til generering af Intrastat-filen.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-122">This flag will activate at run-time the process of collecting output details for generating the Intrastat file.</span></span>  
    * <span data-ttu-id="0d4ad-123">Du skal foretage optælling for forskellige Intrastat-retninger, så føj en dedikeret modeloptælling til datakildernes liste over denne formatkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-123">You need to do counting for different Intrastat directions, so add a dedicated model enumeration to the data sources' list of this format configuration.</span></span>  
3. <span data-ttu-id="0d4ad-124">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-124">Click the Mapping tab.</span></span>
4. <span data-ttu-id="0d4ad-125">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-125">Click Add root to open the drop dialog.</span></span>
5. <span data-ttu-id="0d4ad-126">Vælg 'Datamodel\Optælling' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-126">In the tree, select 'Data model\Enumeration '.</span></span>
6. <span data-ttu-id="0d4ad-127">Skriv 'Retning' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-127">In the Name field, type 'Direction'.</span></span>
7. <span data-ttu-id="0d4ad-128">Indtast eller vælg en værdi i feltet Modelfasttekst.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-128">In the Model enumeration field, enter or select a value.</span></span>
    * <span data-ttu-id="0d4ad-129">Vælg værdien Retning.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-129">Select the value Direction.</span></span>  
8. <span data-ttu-id="0d4ad-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-130">Click OK.</span></span>
9. <span data-ttu-id="0d4ad-131">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-131">Click Add root to open the drop dialog.</span></span>
10. <span data-ttu-id="0d4ad-132">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-132">In the tree, select 'Functions\Calculated field'.</span></span>
11. <span data-ttu-id="0d4ad-133">Skriv '$BlockName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-133">In the Name field, type '$BlockName'.</span></span>
12. <span data-ttu-id="0d4ad-134">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-134">Click Edit formula.</span></span>
13. <span data-ttu-id="0d4ad-135">Skriv "bloker" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-135">In the Formula field, enter '"block"'.</span></span>
14. <span data-ttu-id="0d4ad-136">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-136">Click Save.</span></span>
15. <span data-ttu-id="0d4ad-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-137">Close the page.</span></span>
16. <span data-ttu-id="0d4ad-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-138">Click OK.</span></span>
17. <span data-ttu-id="0d4ad-139">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-139">Click Add root to open the drop dialog.</span></span>
18. <span data-ttu-id="0d4ad-140">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-140">In the tree, select 'Functions\Calculated field'.</span></span>
19. <span data-ttu-id="0d4ad-141">Skriv '$RecName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-141">In the Name field, type '$RecName'.</span></span>
20. <span data-ttu-id="0d4ad-142">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-142">Click Edit formula.</span></span>
21. <span data-ttu-id="0d4ad-143">Skriv "post" i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-143">In the Formula field, enter '"record"'.</span></span>
22. <span data-ttu-id="0d4ad-144">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-144">Click Save.</span></span>
23. <span data-ttu-id="0d4ad-145">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-145">Close the page.</span></span>
24. <span data-ttu-id="0d4ad-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-146">Click OK.</span></span>
25. <span data-ttu-id="0d4ad-147">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-147">Click Add root to open the drop dialog.</span></span>
26. <span data-ttu-id="0d4ad-148">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-148">In the tree, select 'Functions\Calculated field'.</span></span>
27. <span data-ttu-id="0d4ad-149">Skriv '$InvName' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-149">In the Name field, type '$InvName'.</span></span>
28. <span data-ttu-id="0d4ad-150">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-150">Click Edit formula.</span></span>
29. <span data-ttu-id="0d4ad-151">Skriv '"InvoicedAmountEUR"' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-151">In the Formula field, enter '"InvoicedAmountEUR"'.</span></span>
30. <span data-ttu-id="0d4ad-152">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-152">Click Save.</span></span>
31. <span data-ttu-id="0d4ad-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-153">Close the page.</span></span>
32. <span data-ttu-id="0d4ad-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-154">Click OK.</span></span>
33. <span data-ttu-id="0d4ad-155">Vælg 'Intrastat\Data' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-155">In the tree, select 'Intrastat\Data'.</span></span>
34. <span data-ttu-id="0d4ad-156">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="0d4ad-156">Click Edit button for the 'Collected data key name' field</span></span>
35. <span data-ttu-id="0d4ad-157">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-157">Click Add data source.</span></span>
    * <span data-ttu-id="0d4ad-158">$BlockName</span><span class="sxs-lookup"><span data-stu-id="0d4ad-158">$BlockName</span></span>  
36. <span data-ttu-id="0d4ad-159">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-159">Click Save.</span></span>
37. <span data-ttu-id="0d4ad-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-160">Close the page.</span></span>
38. <span data-ttu-id="0d4ad-161">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-161">Click the Edit button for the Collected data key value field.</span></span>
39. <span data-ttu-id="0d4ad-162">Skriv 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-162">In the Formula field, enter 'IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")'.</span></span>
    * <span data-ttu-id="0d4ad-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span><span class="sxs-lookup"><span data-stu-id="0d4ad-163">IF(Intrastat.CommodityRecord.Direction=Direction.Import, "Import", "Export")</span></span>  
40. <span data-ttu-id="0d4ad-164">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-164">Click Save.</span></span>
41. <span data-ttu-id="0d4ad-165">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-165">Close the page.</span></span>
    * <span data-ttu-id="0d4ad-166">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-166">Count the lines of this sequence.</span></span> <span data-ttu-id="0d4ad-167">Resultaterne skal bruges sammen med navnet "bloker" separat for forskellige retninger.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-167">The results will be used with the name "block" separately for different directions.</span></span> <span data-ttu-id="0d4ad-168">"Import" vil blive brugt til enhver Intrastat-postering for indførsel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-168">Value "Import" will be used for any arrivals Intrastat transactions.</span></span> <span data-ttu-id="0d4ad-169">Værdien "Eksport" vil blive brugt til enhver Intrastat-postering for udførsel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-169">The value "Export" will be used for any Intrastat dispatches transactions.</span></span> <span data-ttu-id="0d4ad-170">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-170">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="0d4ad-171">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-171">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span>  
42. <span data-ttu-id="0d4ad-172">Udvid 'Intrastat\Data: Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-172">In the tree, expand 'Intrastat\Data: Sequence'.</span></span>
43. <span data-ttu-id="0d4ad-173">Vælg 'Intrastat\Data: Sequence\Arrivals?' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-173">In the tree, select 'Intrastat\Data: Sequence\Arrivals?'.</span></span>
44. <span data-ttu-id="0d4ad-174">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-174">Click Edit button for the 'Collected data key name' field.</span></span>
    * <span data-ttu-id="0d4ad-175">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-175">Count the lines of this sequence.</span></span> <span data-ttu-id="0d4ad-176">Resultaterne huskes med navnet "post".</span><span class="sxs-lookup"><span data-stu-id="0d4ad-176">The results will be memorized using the name "record".</span></span>  
45. <span data-ttu-id="0d4ad-177">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-177">In the tree, select '$RecName'.</span></span>
46. <span data-ttu-id="0d4ad-178">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-178">Click Add data source.</span></span>
47. <span data-ttu-id="0d4ad-179">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-179">Click Save.</span></span>
48. <span data-ttu-id="0d4ad-180">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-180">Close the page.</span></span>
49. <span data-ttu-id="0d4ad-181">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="0d4ad-181">Click Edit button for the 'Collected data key value' field</span></span>
50. <span data-ttu-id="0d4ad-182">Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-182">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
51. <span data-ttu-id="0d4ad-183">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-183">Click Save.</span></span>
52. <span data-ttu-id="0d4ad-184">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-184">Close the page.</span></span>
    * <span data-ttu-id="0d4ad-185">Tæl linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-185">Count the lines of this sequence.</span></span> <span data-ttu-id="0d4ad-186">Resultaterne skal bruges sammen med navnet "post" separat for forskellige varekoder.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-186">The results will be used with the name "record" separately for different commodity codes.</span></span> <span data-ttu-id="0d4ad-187">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-187">Consider this to be a virtual Excel spreadsheet.</span></span> <span data-ttu-id="0d4ad-188">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksporter" i overensstemmelse hermed, og den anden blok "post"udfyldes med varekodeværdien.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-188">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly and the second block "record" is filled with the commodity code value.</span></span>  
53. <span data-ttu-id="0d4ad-189">Vælg 'Intrastat\Data: Sequence\Dispatches?' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-189">In the tree, select 'Intrastat\Data: Sequence\Dispatches?'.</span></span>
54. <span data-ttu-id="0d4ad-190">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'</span><span class="sxs-lookup"><span data-stu-id="0d4ad-190">Click Edit button for the 'Collected data key name' field</span></span>
55. <span data-ttu-id="0d4ad-191">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-191">In the tree, select '$RecName'.</span></span>
56. <span data-ttu-id="0d4ad-192">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-192">Click Add data source.</span></span>
57. <span data-ttu-id="0d4ad-193">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-193">Click Save.</span></span>
58. <span data-ttu-id="0d4ad-194">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-194">Close the page.</span></span>
59. <span data-ttu-id="0d4ad-195">Klik på knappen Rediger for feltet 'Nøgleværdi for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-195">Click the Edit button for the 'Collected data key value' field.</span></span>
60. <span data-ttu-id="0d4ad-196">Skriv 'Intrastat.CommodityRecord.CommodityCode' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-196">In the Formula field, enter 'Intrastat.CommodityRecord.CommodityCode'.</span></span>
61. <span data-ttu-id="0d4ad-197">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-197">Click Save.</span></span>
62. <span data-ttu-id="0d4ad-198">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-198">Close the page.</span></span>
63. <span data-ttu-id="0d4ad-199">Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-199">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?'.</span></span>
64. <span data-ttu-id="0d4ad-200">Udvid 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record = Intrastat.CommodityRecord' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-200">In the tree, expand 'Intrastat\Data: Sequence\Dispatches: Sequence?\Record =  Intrastat.CommodityRecord'.</span></span>
65. <span data-ttu-id="0d4ad-201">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-201">Click the Format tab.</span></span>
66. <span data-ttu-id="0d4ad-202">Vælg 'Intrastat\Data\Dispatches\Record\Fakturabeløb EUR' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-202">In the tree, select 'Intrastat\Data\Dispatches\Record\Invoice amount EUR'.</span></span>
67. <span data-ttu-id="0d4ad-203">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-203">Click the Mapping tab.</span></span>
68. <span data-ttu-id="0d4ad-204">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-204">Click the Edit button for the 'Collected data key name' field.</span></span>
69. <span data-ttu-id="0d4ad-205">Vælg '$InvName' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-205">In the tree, select '$InvName'.</span></span>
70. <span data-ttu-id="0d4ad-206">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-206">Click Add data source.</span></span>
71. <span data-ttu-id="0d4ad-207">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-207">Click Save.</span></span>
72. <span data-ttu-id="0d4ad-208">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-208">Close the page.</span></span>
    * <span data-ttu-id="0d4ad-209">Sammenlæg de fakturerede beløbsværdier for linjerne i denne rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-209">Summarize the invoiced amount values for lines of this sequence.</span></span> <span data-ttu-id="0d4ad-210">Resultaterne skal bruges sammen med navnet "InvoicedAmountEUR" separat for forskellige Intrastat-retninger og varekoder.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-210">The results will be used with the name "InvoicedAmountEUR" separately for different Intrastat directions and commodity codes.</span></span> <span data-ttu-id="0d4ad-211">Overvej at bruge et virtuelt Excel-regneark.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-211">Consider this to be a virtual creation in Excel spreadsheet.</span></span> <span data-ttu-id="0d4ad-212">For hver transaktion udfyldes en række, hvor den første kolonne er "bloker", med værdierne "Import" og "Eksport" i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-212">For each transaction a row where the first column "block" is filled with the values "Import" and "Export" accordingly.</span></span> <span data-ttu-id="0d4ad-213">Den anden blok "post" udfyldes med varekodeværdien, og den tredje kolonne "InvoicedAmountEUR" udfyldes med en fakturabeløbsværdien.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-213">The second block "record" is filled with the commodity code value, and the third column "InvoicedAmountEUR" is filled with the invoice amount value.</span></span>  
73. <span data-ttu-id="0d4ad-214">Udvid 'Intrastat\Data\Arrivals?' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-214">In the tree, expand 'Intrastat\Data\Arrivals?'.</span></span>
74. <span data-ttu-id="0d4ad-215">Udvid 'Intrastat\Data\Arrivals?\Record = Intrastat.CommodityRecord' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-215">In the tree, expand 'Intrastat\Data\Arrivals?\Record =  Intrastat.CommodityRecord'.</span></span>
75. <span data-ttu-id="0d4ad-216">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-216">Click the Format tab.</span></span>
76. <span data-ttu-id="0d4ad-217">Vælg 'Intrastat\Data\Arrivals\Record\Fakturabeløb EUR' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-217">In the tree, select 'Intrastat\Data\Arrivals\Record\Invoice amount EUR'.</span></span>
77. <span data-ttu-id="0d4ad-218">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-218">Click the Mapping tab.</span></span>
78. <span data-ttu-id="0d4ad-219">Klik på knappen Rediger for feltet 'Nøglenavn for opsamlede data'.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-219">Click the Edit button for the 'Collected data key name' field.</span></span>
79. <span data-ttu-id="0d4ad-220">Vælg '$InvName' i træet.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-220">In the tree, select '$InvName'.</span></span>
80. <span data-ttu-id="0d4ad-221">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-221">Click Add data source.</span></span>
81. <span data-ttu-id="0d4ad-222">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-222">Click Save.</span></span>
82. <span data-ttu-id="0d4ad-223">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-223">Close the page.</span></span>
83. <span data-ttu-id="0d4ad-224">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-224">Click Save.</span></span>
84. <span data-ttu-id="0d4ad-225">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0d4ad-225">Close the page.</span></span>

