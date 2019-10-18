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
ms.openlocfilehash: fbdff413edf942b99e11412902abb7589a754c2d
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182364"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-3-use-computations-to-make-the-output"></a><span data-ttu-id="cc08a-103">ER Konfigurere format for at udføre optælling og sammenlægning (del 3: Brug beregninger til at udføre outputtet)</span><span class="sxs-lookup"><span data-stu-id="cc08a-103">ER Configure format to do counting and summing (Part 3: Use computations to make the output)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="cc08a-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="cc08a-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="cc08a-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="cc08a-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 2: Konfigurer beregninger)".</span><span class="sxs-lookup"><span data-stu-id="cc08a-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="cc08a-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="cc08a-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="cc08a-108">Konfigurer denne rapport til at bruge optællings- og sammenlægningsinfo</span><span class="sxs-lookup"><span data-stu-id="cc08a-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="cc08a-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="cc08a-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="cc08a-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="cc08a-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="cc08a-111">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="cc08a-112">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="cc08a-113">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="cc08a-114">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="cc08a-114">Click Designer.</span></span>
7. <span data-ttu-id="cc08a-115">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="cc08a-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="cc08a-116">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="cc08a-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="cc08a-117">Tilføj en ny datakilde for at hente en liste over huskede blokke.</span><span class="sxs-lookup"><span data-stu-id="cc08a-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="cc08a-118">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="cc08a-119">Skriv '$BlocksList' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="cc08a-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="cc08a-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="cc08a-120">$BlocksList</span></span>  
11. <span data-ttu-id="cc08a-121">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-121">Click Edit formula.</span></span>
12. <span data-ttu-id="cc08a-122">Vælg 'Datasamlingsfunktioner\COLLECTEDLIST' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="cc08a-123">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="cc08a-123">Click Add function.</span></span>
14. <span data-ttu-id="cc08a-124">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="cc08a-124">Click Add data source.</span></span>
15. <span data-ttu-id="cc08a-125">Skriv 'COLLECTEDLIST('$BlockName', ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="cc08a-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="cc08a-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="cc08a-127">Skriv 'COLLECTEDLIST('$BlockName', "\*")' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="cc08a-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="cc08a-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="cc08a-129">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cc08a-129">Click Save.</span></span>
    * <span data-ttu-id="cc08a-130">Mønsteret "\*" betyder, at alle blokke medtages på listen til denne post.</span><span class="sxs-lookup"><span data-stu-id="cc08a-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="cc08a-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cc08a-131">Close the page.</span></span>
19. <span data-ttu-id="cc08a-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="cc08a-132">Click OK.</span></span>
20. <span data-ttu-id="cc08a-133">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="cc08a-133">Click the Format tab.</span></span>
21. <span data-ttu-id="cc08a-134">Vælg 'Intrastat\Data' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="cc08a-135">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="cc08a-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="cc08a-136">Vælg 'Text\Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="cc08a-137">Skriv 'Totaler efter blokke' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="cc08a-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="cc08a-138">Totaler efter blokke</span><span class="sxs-lookup"><span data-stu-id="cc08a-138">Totals by blocks</span></span>  
25. <span data-ttu-id="cc08a-139">Vælg 'Ny linje – Windows (CR LF)' i feltet Specialtegn.</span><span class="sxs-lookup"><span data-stu-id="cc08a-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="cc08a-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="cc08a-140">Click OK.</span></span>
27. <span data-ttu-id="cc08a-141">Vælg 'Intrastat\Data\Totaler efter blokke' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="cc08a-142">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="cc08a-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="cc08a-143">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="cc08a-144">Skriv 'Blokkode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="cc08a-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="cc08a-145">Bloker kode</span><span class="sxs-lookup"><span data-stu-id="cc08a-145">Block code</span></span>  
31. <span data-ttu-id="cc08a-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="cc08a-146">Click OK.</span></span>
32. <span data-ttu-id="cc08a-147">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="cc08a-147">Click Add String.</span></span>
33. <span data-ttu-id="cc08a-148">Skriv 'Linjeoptælling' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="cc08a-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="cc08a-149">Linjeoptælling</span><span class="sxs-lookup"><span data-stu-id="cc08a-149">Lines counting</span></span>  
34. <span data-ttu-id="cc08a-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="cc08a-150">Click OK.</span></span>
35. <span data-ttu-id="cc08a-151">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="cc08a-151">Click Add String.</span></span>
36. <span data-ttu-id="cc08a-152">Skriv "Samlet beløb" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="cc08a-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="cc08a-153">Totalbeløb</span><span class="sxs-lookup"><span data-stu-id="cc08a-153">Total amount</span></span>  
37. <span data-ttu-id="cc08a-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="cc08a-154">Click OK.</span></span>
38. <span data-ttu-id="cc08a-155">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="cc08a-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="cc08a-156">Vælg '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="cc08a-157">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="cc08a-157">Click Bind.</span></span>
    * <span data-ttu-id="cc08a-158">Opret en oversigtslinje for hver huskede blok.</span><span class="sxs-lookup"><span data-stu-id="cc08a-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="cc08a-159">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="cc08a-159">Click the Format tab.</span></span>
42. <span data-ttu-id="cc08a-160">Vælg 'Intrastat\Data\Totaler efter blokke\Blokkode' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="cc08a-161">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="cc08a-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="cc08a-162">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-162">Click Edit formula.</span></span>
45. <span data-ttu-id="cc08a-163">Skriv "Blok-id: " & ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="cc08a-164">"Blok-id: " &</span><span class="sxs-lookup"><span data-stu-id="cc08a-164">"Block id: " &</span></span>  
46. <span data-ttu-id="cc08a-165">Udvid '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="cc08a-166">Vælg '$BlocksList\Value' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="cc08a-167">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="cc08a-167">Click Add data source.</span></span>
49. <span data-ttu-id="cc08a-168">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cc08a-168">Click Save.</span></span>
50. <span data-ttu-id="cc08a-169">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cc08a-169">Close the page.</span></span>
51. <span data-ttu-id="cc08a-170">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="cc08a-170">Click the Format tab.</span></span>
52. <span data-ttu-id="cc08a-171">Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="cc08a-172">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="cc08a-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="cc08a-173">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-173">Click Edit formula.</span></span>
    * <span data-ttu-id="cc08a-174">Opret output for antallet af linjer for hver blok, der vises i denne rapport.</span><span class="sxs-lookup"><span data-stu-id="cc08a-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="cc08a-175">Skriv '"Antal linjer i denne blok: " & ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="cc08a-176">"Antal linjer i denne blok: " &</span><span class="sxs-lookup"><span data-stu-id="cc08a-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="cc08a-177">Skriv '"Antal linjer i denne blok: " & TEXT(' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="cc08a-178">"Antal linjer i denne blok: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="cc08a-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="cc08a-179">Vælg 'Datasamlingsfunktioner\COUNTIFS' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="cc08a-180">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="cc08a-180">Click Add function.</span></span>
59. <span data-ttu-id="cc08a-181">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="cc08a-181">Click Add data source.</span></span>
60. <span data-ttu-id="cc08a-182">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="cc08a-183">"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="cc08a-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="cc08a-184">Udvid '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="cc08a-185">Vælg '$BlocksList\Value' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="cc08a-186">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="cc08a-186">Click Add data source.</span></span>
64. <span data-ttu-id="cc08a-187">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="cc08a-188">"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="cc08a-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="cc08a-189">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="cc08a-190">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="cc08a-190">Click Add data source.</span></span>
67. <span data-ttu-id="cc08a-191">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="cc08a-192">"Antal linjer i denne blok:" & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="cc08a-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="cc08a-193">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cc08a-193">Click Save.</span></span>
69. <span data-ttu-id="cc08a-194">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cc08a-194">Close the page.</span></span>
70. <span data-ttu-id="cc08a-195">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="cc08a-195">Click the Format tab.</span></span>
71. <span data-ttu-id="cc08a-196">Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling\Samlet beløb' i træet.</span><span class="sxs-lookup"><span data-stu-id="cc08a-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="cc08a-197">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="cc08a-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="cc08a-198">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-198">Click Edit formula.</span></span>
    * <span data-ttu-id="cc08a-199">Opret output, der er summen af det fakturerede beløb for hver blok, der vises i denne rapport.</span><span class="sxs-lookup"><span data-stu-id="cc08a-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="cc08a-200">Skriv '"Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="cc08a-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="cc08a-201">"Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="cc08a-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="cc08a-202">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cc08a-202">Click Save.</span></span>
76. <span data-ttu-id="cc08a-203">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cc08a-203">Close the page.</span></span>
77. <span data-ttu-id="cc08a-204">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cc08a-204">Click Save.</span></span>
78. <span data-ttu-id="cc08a-205">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cc08a-205">Close the page.</span></span>

