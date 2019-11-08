---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 3: Brug beregninger til at oprette outputtet)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.
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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7bbef7048488056f50ec8967a9af53d468666856
ms.sourcegitcommit: 75db3b75d35d27034f9b56e7119c9d0cb7666830
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/03/2019
ms.locfileid: "2550757"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3---use-computations-to-make-the-output"></a><span data-ttu-id="96eec-103">ER Konfigurere format for at udføre optælling og sammenlægning (del 3: Brug beregninger til at oprette outputtet)</span><span class="sxs-lookup"><span data-stu-id="96eec-103">ER Configure format to do counting and summing (Part 3 - Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="96eec-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="96eec-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="96eec-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="96eec-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="96eec-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 2: Konfigurer beregninger)".</span><span class="sxs-lookup"><span data-stu-id="96eec-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="96eec-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="96eec-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="96eec-108">Konfigurer denne rapport til at bruge optællings- og sammenlægningsinfo</span><span class="sxs-lookup"><span data-stu-id="96eec-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="96eec-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="96eec-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="96eec-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="96eec-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="96eec-111">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="96eec-112">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="96eec-113">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="96eec-114">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="96eec-114">Click Designer.</span></span>
7. <span data-ttu-id="96eec-115">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="96eec-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="96eec-116">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="96eec-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="96eec-117">Tilføj en ny datakilde for at hente en liste over huskede blokke.</span><span class="sxs-lookup"><span data-stu-id="96eec-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="96eec-118">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="96eec-119">Skriv '$BlocksList' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="96eec-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="96eec-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="96eec-120">$BlocksList</span></span>  
11. <span data-ttu-id="96eec-121">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-121">Click Edit formula.</span></span>
12. <span data-ttu-id="96eec-122">Vælg 'Datasamlingsfunktioner\COLLECTEDLIST' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="96eec-123">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="96eec-123">Click Add function.</span></span>
14. <span data-ttu-id="96eec-124">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="96eec-124">Click Add data source.</span></span>
15. <span data-ttu-id="96eec-125">Skriv 'COLLECTEDLIST('$BlockName', ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="96eec-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="96eec-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="96eec-127">Skriv 'COLLECTEDLIST('$BlockName', "\*")' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="96eec-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="96eec-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="96eec-129">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="96eec-129">Click Save.</span></span>
    * <span data-ttu-id="96eec-130">Mønsteret "\*" betyder, at alle blokke medtages på listen til denne post.</span><span class="sxs-lookup"><span data-stu-id="96eec-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="96eec-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="96eec-131">Close the page.</span></span>
19. <span data-ttu-id="96eec-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="96eec-132">Click OK.</span></span>
20. <span data-ttu-id="96eec-133">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="96eec-133">Click the Format tab.</span></span>
21. <span data-ttu-id="96eec-134">Vælg 'Intrastat\Data' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="96eec-135">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="96eec-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="96eec-136">Vælg 'Text\Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="96eec-137">Skriv 'Totaler efter blokke' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="96eec-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="96eec-138">Totaler efter blokke</span><span class="sxs-lookup"><span data-stu-id="96eec-138">Totals by blocks</span></span>  
25. <span data-ttu-id="96eec-139">Vælg 'Ny linje – Windows (CR LF)' i feltet Specialtegn.</span><span class="sxs-lookup"><span data-stu-id="96eec-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="96eec-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="96eec-140">Click OK.</span></span>
27. <span data-ttu-id="96eec-141">Vælg 'Intrastat\Data\Totaler efter blokke' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="96eec-142">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="96eec-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="96eec-143">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="96eec-144">Skriv 'Blokkode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="96eec-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="96eec-145">Bloker kode</span><span class="sxs-lookup"><span data-stu-id="96eec-145">Block code</span></span>  
31. <span data-ttu-id="96eec-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="96eec-146">Click OK.</span></span>
32. <span data-ttu-id="96eec-147">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="96eec-147">Click Add String.</span></span>
33. <span data-ttu-id="96eec-148">Skriv 'Linjeoptælling' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="96eec-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="96eec-149">Linjeoptælling</span><span class="sxs-lookup"><span data-stu-id="96eec-149">Lines counting</span></span>  
34. <span data-ttu-id="96eec-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="96eec-150">Click OK.</span></span>
35. <span data-ttu-id="96eec-151">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="96eec-151">Click Add String.</span></span>
36. <span data-ttu-id="96eec-152">Skriv "Samlet beløb" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="96eec-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="96eec-153">Totalbeløb</span><span class="sxs-lookup"><span data-stu-id="96eec-153">Total amount</span></span>  
37. <span data-ttu-id="96eec-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="96eec-154">Click OK.</span></span>
38. <span data-ttu-id="96eec-155">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="96eec-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="96eec-156">Vælg '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="96eec-157">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="96eec-157">Click Bind.</span></span>
    * <span data-ttu-id="96eec-158">Opret en oversigtslinje for hver huskede blok.</span><span class="sxs-lookup"><span data-stu-id="96eec-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="96eec-159">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="96eec-159">Click the Format tab.</span></span>
42. <span data-ttu-id="96eec-160">Vælg 'Intrastat\Data\Totaler efter blokke\Blokkode' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="96eec-161">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="96eec-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="96eec-162">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-162">Click Edit formula.</span></span>
45. <span data-ttu-id="96eec-163">Skriv "Blok-id: " & ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="96eec-164">"Blok-id: " &</span><span class="sxs-lookup"><span data-stu-id="96eec-164">"Block id: " &</span></span>  
46. <span data-ttu-id="96eec-165">Udvid '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="96eec-166">Vælg '$BlocksList\Value' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="96eec-167">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="96eec-167">Click Add data source.</span></span>
49. <span data-ttu-id="96eec-168">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="96eec-168">Click Save.</span></span>
50. <span data-ttu-id="96eec-169">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="96eec-169">Close the page.</span></span>
51. <span data-ttu-id="96eec-170">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="96eec-170">Click the Format tab.</span></span>
52. <span data-ttu-id="96eec-171">Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="96eec-172">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="96eec-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="96eec-173">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-173">Click Edit formula.</span></span>
    * <span data-ttu-id="96eec-174">Opret output for antallet af linjer for hver blok, der vises i denne rapport.</span><span class="sxs-lookup"><span data-stu-id="96eec-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="96eec-175">Skriv '"Antal linjer i denne blok: " & ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="96eec-176">"Antal linjer i denne blok: " &</span><span class="sxs-lookup"><span data-stu-id="96eec-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="96eec-177">Skriv '"Antal linjer i denne blok: " & TEXT(' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="96eec-178">"Antal linjer i denne blok: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="96eec-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="96eec-179">Vælg 'Datasamlingsfunktioner\COUNTIFS' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="96eec-180">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="96eec-180">Click Add function.</span></span>
59. <span data-ttu-id="96eec-181">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="96eec-181">Click Add data source.</span></span>
60. <span data-ttu-id="96eec-182">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="96eec-183">"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="96eec-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="96eec-184">Udvid '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="96eec-185">Vælg '$BlocksList\Value' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="96eec-186">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="96eec-186">Click Add data source.</span></span>
64. <span data-ttu-id="96eec-187">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="96eec-188">"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="96eec-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="96eec-189">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="96eec-190">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="96eec-190">Click Add data source.</span></span>
67. <span data-ttu-id="96eec-191">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="96eec-192">"Antal linjer i denne blok:" & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="96eec-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="96eec-193">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="96eec-193">Click Save.</span></span>
69. <span data-ttu-id="96eec-194">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="96eec-194">Close the page.</span></span>
70. <span data-ttu-id="96eec-195">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="96eec-195">Click the Format tab.</span></span>
71. <span data-ttu-id="96eec-196">Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling\Samlet beløb' i træet.</span><span class="sxs-lookup"><span data-stu-id="96eec-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="96eec-197">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="96eec-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="96eec-198">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-198">Click Edit formula.</span></span>
    * <span data-ttu-id="96eec-199">Opret output, der er summen af det fakturerede beløb for hver blok, der vises i denne rapport.</span><span class="sxs-lookup"><span data-stu-id="96eec-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="96eec-200">Skriv '"Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="96eec-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="96eec-201">"Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="96eec-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="96eec-202">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="96eec-202">Click Save.</span></span>
76. <span data-ttu-id="96eec-203">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="96eec-203">Close the page.</span></span>
77. <span data-ttu-id="96eec-204">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="96eec-204">Click Save.</span></span>
78. <span data-ttu-id="96eec-205">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="96eec-205">Close the page.</span></span>

