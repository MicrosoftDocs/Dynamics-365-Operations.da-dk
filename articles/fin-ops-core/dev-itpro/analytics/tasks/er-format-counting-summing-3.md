---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 3: Brug beregninger til at oprette outputtet)'
description: Dette emne beskriver, hvordan du konfigurerer et format for elektronisk rapportering til optælling og opsummering baseret på data fra det allerede genererede tekstoutput. (Del 3)
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, EROperationDesigner, ERDataSourceAddDropDialog, ERExpressionDesignerFormula, ERComponentTypeDropDialog
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 4a69dd28051d8e98643eb95c663525075bed8dec
ms.sourcegitcommit: 5192cfaedfd861faea63d8954d7bcc500608a225
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/30/2021
ms.locfileid: "5092966"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="ec567-104">ER Konfigurere format for at udføre optælling og sammenlægning (del 3: Brug beregninger til at oprette outputtet)</span><span class="sxs-lookup"><span data-stu-id="ec567-104">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ec567-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="ec567-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="ec567-106">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="ec567-106">These steps can be performed in any company.</span></span>

<span data-ttu-id="ec567-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 2: Konfigurer beregninger)".</span><span class="sxs-lookup"><span data-stu-id="ec567-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 2: Configure computations)" procedure.</span></span>

<span data-ttu-id="ec567-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="ec567-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="ec567-109">Konfigurer denne rapport til at bruge optællings- og sammenlægningsinfo</span><span class="sxs-lookup"><span data-stu-id="ec567-109">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="ec567-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="ec567-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="ec567-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="ec567-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="ec567-112">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="ec567-113">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="ec567-114">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="ec567-115">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="ec567-115">Click Designer.</span></span>
7. <span data-ttu-id="ec567-116">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="ec567-116">Click the Mapping tab.</span></span>
8. <span data-ttu-id="ec567-117">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ec567-117">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="ec567-118">Tilføj en ny datakilde for at hente en liste over huskede blokke.</span><span class="sxs-lookup"><span data-stu-id="ec567-118">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="ec567-119">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-119">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="ec567-120">Skriv '$BlocksList' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ec567-120">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="ec567-121">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="ec567-121">$BlocksList</span></span>  
11. <span data-ttu-id="ec567-122">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-122">Click Edit formula.</span></span>
12. <span data-ttu-id="ec567-123">Vælg 'Datasamlingsfunktioner\COLLECTEDLIST' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-123">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="ec567-124">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="ec567-124">Click Add function.</span></span>
14. <span data-ttu-id="ec567-125">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="ec567-125">Click Add data source.</span></span>
15. <span data-ttu-id="ec567-126">Skriv 'COLLECTEDLIST('$BlockName', ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-126">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="ec567-127">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="ec567-127">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="ec567-128">Skriv 'COLLECTEDLIST('$BlockName', "\*")' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-128">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="ec567-129">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="ec567-129">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="ec567-130">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ec567-130">Click Save.</span></span>
    * <span data-ttu-id="ec567-131">Mønsteret "\*" betyder, at alle blokke medtages på listen til denne post.</span><span class="sxs-lookup"><span data-stu-id="ec567-131">The pattern "\*" means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="ec567-132">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec567-132">Close the page.</span></span>
19. <span data-ttu-id="ec567-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ec567-133">Click OK.</span></span>
20. <span data-ttu-id="ec567-134">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="ec567-134">Click the Format tab.</span></span>
21. <span data-ttu-id="ec567-135">Vælg 'Intrastat\Data' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-135">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="ec567-136">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ec567-136">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="ec567-137">Vælg 'Text\Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-137">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="ec567-138">Skriv 'Totaler efter blokke' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ec567-138">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="ec567-139">Totaler efter blokke</span><span class="sxs-lookup"><span data-stu-id="ec567-139">Totals by blocks</span></span>  
25. <span data-ttu-id="ec567-140">Vælg 'Ny linje – Windows (CR LF)' i feltet Specialtegn.</span><span class="sxs-lookup"><span data-stu-id="ec567-140">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="ec567-141">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ec567-141">Click OK.</span></span>
27. <span data-ttu-id="ec567-142">Vælg 'Intrastat\Data\Totaler efter blokke' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-142">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="ec567-143">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ec567-143">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="ec567-144">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-144">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="ec567-145">Skriv 'Blokkode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ec567-145">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="ec567-146">Bloker kode</span><span class="sxs-lookup"><span data-stu-id="ec567-146">Block code</span></span>  
31. <span data-ttu-id="ec567-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ec567-147">Click OK.</span></span>
32. <span data-ttu-id="ec567-148">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="ec567-148">Click Add String.</span></span>
33. <span data-ttu-id="ec567-149">Skriv 'Linjeoptælling' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ec567-149">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="ec567-150">Linjeoptælling</span><span class="sxs-lookup"><span data-stu-id="ec567-150">Lines counting</span></span>  
34. <span data-ttu-id="ec567-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ec567-151">Click OK.</span></span>
35. <span data-ttu-id="ec567-152">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="ec567-152">Click Add String.</span></span>
36. <span data-ttu-id="ec567-153">Skriv "Samlet beløb" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ec567-153">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="ec567-154">Totalbeløb</span><span class="sxs-lookup"><span data-stu-id="ec567-154">Total amount</span></span>  
37. <span data-ttu-id="ec567-155">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ec567-155">Click OK.</span></span>
38. <span data-ttu-id="ec567-156">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="ec567-156">Click the Mapping tab.</span></span>
39. <span data-ttu-id="ec567-157">Vælg '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-157">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="ec567-158">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="ec567-158">Click Bind.</span></span>
    * <span data-ttu-id="ec567-159">Opret en oversigtslinje for hver huskede blok.</span><span class="sxs-lookup"><span data-stu-id="ec567-159">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="ec567-160">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="ec567-160">Click the Format tab.</span></span>
42. <span data-ttu-id="ec567-161">Vælg 'Intrastat\Data\Totaler efter blokke\Blokkode' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-161">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="ec567-162">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="ec567-162">Click the Mapping tab.</span></span>
44. <span data-ttu-id="ec567-163">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-163">Click Edit formula.</span></span>
45. <span data-ttu-id="ec567-164">Skriv "Blok-id: " & ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-164">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="ec567-165">"Blok-id: " &</span><span class="sxs-lookup"><span data-stu-id="ec567-165">"Block id: " &</span></span>  
46. <span data-ttu-id="ec567-166">Udvid '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-166">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="ec567-167">Vælg '$BlocksList\Value' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-167">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="ec567-168">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="ec567-168">Click Add data source.</span></span>
49. <span data-ttu-id="ec567-169">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ec567-169">Click Save.</span></span>
50. <span data-ttu-id="ec567-170">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec567-170">Close the page.</span></span>
51. <span data-ttu-id="ec567-171">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="ec567-171">Click the Format tab.</span></span>
52. <span data-ttu-id="ec567-172">Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-172">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="ec567-173">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="ec567-173">Click the Mapping tab.</span></span>
54. <span data-ttu-id="ec567-174">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-174">Click Edit formula.</span></span>
    * <span data-ttu-id="ec567-175">Opret output for antallet af linjer for hver blok, der vises i denne rapport.</span><span class="sxs-lookup"><span data-stu-id="ec567-175">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="ec567-176">Skriv '"Antal linjer i denne blok: " & ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-176">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="ec567-177">"Antal linjer i denne blok: " &</span><span class="sxs-lookup"><span data-stu-id="ec567-177">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="ec567-178">Skriv '"Antal linjer i denne blok: " & TEXT(' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-178">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="ec567-179">"Antal linjer i denne blok: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="ec567-179">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="ec567-180">Vælg 'Datasamlingsfunktioner\COUNTIFS' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-180">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="ec567-181">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="ec567-181">Click Add function.</span></span>
59. <span data-ttu-id="ec567-182">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="ec567-182">Click Add data source.</span></span>
60. <span data-ttu-id="ec567-183">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-183">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="ec567-184">"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="ec567-184">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="ec567-185">Udvid '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-185">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="ec567-186">Vælg '$BlocksList\Value' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-186">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="ec567-187">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="ec567-187">Click Add data source.</span></span>
64. <span data-ttu-id="ec567-188">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-188">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="ec567-189">"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="ec567-189">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="ec567-190">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-190">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="ec567-191">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="ec567-191">Click Add data source.</span></span>
67. <span data-ttu-id="ec567-192">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-192">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="ec567-193">"Antal linjer i denne blok:" & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="ec567-193">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="ec567-194">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ec567-194">Click Save.</span></span>
69. <span data-ttu-id="ec567-195">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec567-195">Close the page.</span></span>
70. <span data-ttu-id="ec567-196">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="ec567-196">Click the Format tab.</span></span>
71. <span data-ttu-id="ec567-197">Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling\Samlet beløb' i træet.</span><span class="sxs-lookup"><span data-stu-id="ec567-197">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="ec567-198">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="ec567-198">Click the Mapping tab.</span></span>
73. <span data-ttu-id="ec567-199">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-199">Click Edit formula.</span></span>
    * <span data-ttu-id="ec567-200">Opret output, der er summen af det fakturerede beløb for hver blok, der vises i denne rapport.</span><span class="sxs-lookup"><span data-stu-id="ec567-200">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="ec567-201">Skriv '"Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="ec567-201">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="ec567-202">"Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="ec567-202">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="ec567-203">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ec567-203">Click Save.</span></span>
76. <span data-ttu-id="ec567-204">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec567-204">Close the page.</span></span>
77. <span data-ttu-id="ec567-205">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="ec567-205">Click Save.</span></span>
78. <span data-ttu-id="ec567-206">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ec567-206">Close the page.</span></span>

