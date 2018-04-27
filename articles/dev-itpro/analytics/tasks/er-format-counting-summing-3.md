--- 
title: "Bruge beregninger til fremstille output til optælling og opsummering"
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
ms.openlocfilehash: 5b7f0cc5b94ab7be11a013ef3e5909d84847e885
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="use-computations-to-make-the-output-for-counting-and-summing"></a><span data-ttu-id="43b2e-103">Bruge beregninger til fremstille output til optælling og opsummering</span><span class="sxs-lookup"><span data-stu-id="43b2e-103">Use computations to make the output for counting and summing</span></span> 

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="43b2e-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="43b2e-105">Disse trin kan udføres i en hvilken som helst virksomhed.</span><span class="sxs-lookup"><span data-stu-id="43b2e-105">These steps can be performed in any company.</span></span>

<span data-ttu-id="43b2e-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 2: Konfigurer beregninger)".</span><span class="sxs-lookup"><span data-stu-id="43b2e-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 2: Configure computations)” procedure.</span></span>

<span data-ttu-id="43b2e-107">Denne fremgangsmåde er til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="43b2e-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="configure-this-report-to-use-counting-and-summing-info"></a><span data-ttu-id="43b2e-108">Konfigurer denne rapport til at bruge optællings- og sammenlægningsinfo</span><span class="sxs-lookup"><span data-stu-id="43b2e-108">Configure this report to use counting and summing info</span></span>
1. <span data-ttu-id="43b2e-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="43b2e-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="43b2e-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="43b2e-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="43b2e-111">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="43b2e-112">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="43b2e-113">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="43b2e-114">Klik på Designer.</span><span class="sxs-lookup"><span data-stu-id="43b2e-114">Click Designer.</span></span>
7. <span data-ttu-id="43b2e-115">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="43b2e-115">Click the Mapping tab.</span></span>
8. <span data-ttu-id="43b2e-116">Klik på Tilføj rod for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="43b2e-116">Click Add root to open the drop dialog.</span></span>
    * <span data-ttu-id="43b2e-117">Tilføj en ny datakilde for at hente en liste over huskede blokke.</span><span class="sxs-lookup"><span data-stu-id="43b2e-117">Add a new data source to get the list of memorized blocks.</span></span>  
9. <span data-ttu-id="43b2e-118">Vælg "Funktioner\Beregnet felt" i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-118">In the tree, select 'Functions\Calculated field'.</span></span>
10. <span data-ttu-id="43b2e-119">Skriv '$BlocksList' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="43b2e-119">In the Name field, type '$BlocksList'.</span></span>
    * <span data-ttu-id="43b2e-120">$BlocksList</span><span class="sxs-lookup"><span data-stu-id="43b2e-120">$BlocksList</span></span>  
11. <span data-ttu-id="43b2e-121">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-121">Click Edit formula.</span></span>
12. <span data-ttu-id="43b2e-122">Vælg 'Datasamlingsfunktioner\COLLECTEDLIST' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-122">In the tree, select 'Data collection functions\COLLECTEDLIST'.</span></span>
13. <span data-ttu-id="43b2e-123">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="43b2e-123">Click Add function.</span></span>
14. <span data-ttu-id="43b2e-124">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="43b2e-124">Click Add data source.</span></span>
15. <span data-ttu-id="43b2e-125">Skriv 'COLLECTEDLIST('$BlockName', ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-125">In the Formula field, enter 'COLLECTEDLIST('$BlockName', '.</span></span>
    * <span data-ttu-id="43b2e-126">COLLECTEDLIST('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="43b2e-126">COLLECTEDLIST('$BlockName',</span></span>  
16. <span data-ttu-id="43b2e-127">Skriv 'COLLECTEDLIST('$BlockName', "\*")' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-127">In the Formula field, enter 'COLLECTEDLIST('$BlockName', "\*")'.</span></span>
    * <span data-ttu-id="43b2e-128">COLLECTEDLIST('$BlockName', "\*")</span><span class="sxs-lookup"><span data-stu-id="43b2e-128">COLLECTEDLIST('$BlockName', "\*")</span></span>  
17. <span data-ttu-id="43b2e-129">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="43b2e-129">Click Save.</span></span>
    * <span data-ttu-id="43b2e-130">Mønsteret "\*" betyder, at alle blokke medtages på listen til denne post.</span><span class="sxs-lookup"><span data-stu-id="43b2e-130">The pattern “\*” means that all blocks will be included to the list for this record.</span></span>  
18. <span data-ttu-id="43b2e-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="43b2e-131">Close the page.</span></span>
19. <span data-ttu-id="43b2e-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="43b2e-132">Click OK.</span></span>
20. <span data-ttu-id="43b2e-133">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="43b2e-133">Click the Format tab.</span></span>
21. <span data-ttu-id="43b2e-134">Vælg 'Intrastat\Data' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-134">In the tree, select 'Intrastat\Data'.</span></span>
22. <span data-ttu-id="43b2e-135">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="43b2e-135">Click Add to open the drop dialog.</span></span>
23. <span data-ttu-id="43b2e-136">Vælg 'Text\Sequence' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-136">In the tree, select 'Text\Sequence'.</span></span>
24. <span data-ttu-id="43b2e-137">Skriv 'Totaler efter blokke' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="43b2e-137">In the Name field, type 'Totals by blocks'.</span></span>
    * <span data-ttu-id="43b2e-138">Totaler efter blokke</span><span class="sxs-lookup"><span data-stu-id="43b2e-138">Totals by blocks</span></span>  
25. <span data-ttu-id="43b2e-139">Vælg 'Ny linje – Windows (CR LF)' i feltet Specialtegn.</span><span class="sxs-lookup"><span data-stu-id="43b2e-139">In the Special characters field, select 'New line - Windows (CR LF)'.</span></span>
26. <span data-ttu-id="43b2e-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="43b2e-140">Click OK.</span></span>
27. <span data-ttu-id="43b2e-141">Vælg 'Intrastat\Data\Totaler efter blokke' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-141">In the tree, select 'Intrastat\Data\Totals by blocks'.</span></span>
28. <span data-ttu-id="43b2e-142">Klik på Tilføj for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="43b2e-142">Click Add to open the drop dialog.</span></span>
29. <span data-ttu-id="43b2e-143">Vælg "Tekst\Streng" i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-143">In the tree, select 'Text\String'.</span></span>
30. <span data-ttu-id="43b2e-144">Skriv 'Blokkode' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="43b2e-144">In the Name field, type 'Block code'.</span></span>
    * <span data-ttu-id="43b2e-145">Bloker kode</span><span class="sxs-lookup"><span data-stu-id="43b2e-145">Block code</span></span>  
31. <span data-ttu-id="43b2e-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="43b2e-146">Click OK.</span></span>
32. <span data-ttu-id="43b2e-147">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="43b2e-147">Click Add String.</span></span>
33. <span data-ttu-id="43b2e-148">Skriv 'Linjeoptælling' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="43b2e-148">In the Name field, type 'Lines counting'.</span></span>
    * <span data-ttu-id="43b2e-149">Linjeoptælling</span><span class="sxs-lookup"><span data-stu-id="43b2e-149">Lines counting</span></span>  
34. <span data-ttu-id="43b2e-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="43b2e-150">Click OK.</span></span>
35. <span data-ttu-id="43b2e-151">Klik på Tilføj streng.</span><span class="sxs-lookup"><span data-stu-id="43b2e-151">Click Add String.</span></span>
36. <span data-ttu-id="43b2e-152">Skriv "Samlet beløb" i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="43b2e-152">In the Name field, type 'Total amount'.</span></span>
    * <span data-ttu-id="43b2e-153">Totalbeløb</span><span class="sxs-lookup"><span data-stu-id="43b2e-153">Total amount</span></span>  
37. <span data-ttu-id="43b2e-154">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="43b2e-154">Click OK.</span></span>
38. <span data-ttu-id="43b2e-155">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="43b2e-155">Click the Mapping tab.</span></span>
39. <span data-ttu-id="43b2e-156">Vælg '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-156">In the tree, select '$BlocksList'.</span></span>
40. <span data-ttu-id="43b2e-157">Klik på Bind.</span><span class="sxs-lookup"><span data-stu-id="43b2e-157">Click Bind.</span></span>
    * <span data-ttu-id="43b2e-158">Opret en oversigtslinje for hver huskede blok.</span><span class="sxs-lookup"><span data-stu-id="43b2e-158">Create a summary line for each memorized block.</span></span>  
41. <span data-ttu-id="43b2e-159">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="43b2e-159">Click the Format tab.</span></span>
42. <span data-ttu-id="43b2e-160">Vælg 'Intrastat\Data\Totaler efter blokke\Blokkode' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-160">In the tree, select 'Intrastat\Data\Totals by blocks\Block code'.</span></span>
43. <span data-ttu-id="43b2e-161">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="43b2e-161">Click the Mapping tab.</span></span>
44. <span data-ttu-id="43b2e-162">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-162">Click Edit formula.</span></span>
45. <span data-ttu-id="43b2e-163">Skriv "Blok-id: " & ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-163">In the Formula field, enter '"Block id: " & '.</span></span>
    * <span data-ttu-id="43b2e-164">"Blok-id: " &</span><span class="sxs-lookup"><span data-stu-id="43b2e-164">"Block id: " &</span></span>  
46. <span data-ttu-id="43b2e-165">Udvid '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-165">In the tree, expand '$BlocksList'.</span></span>
47. <span data-ttu-id="43b2e-166">Vælg '$BlocksList\Value' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-166">In the tree, select '$BlocksList\Value'.</span></span>
48. <span data-ttu-id="43b2e-167">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="43b2e-167">Click Add data source.</span></span>
49. <span data-ttu-id="43b2e-168">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="43b2e-168">Click Save.</span></span>
50. <span data-ttu-id="43b2e-169">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="43b2e-169">Close the page.</span></span>
51. <span data-ttu-id="43b2e-170">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="43b2e-170">Click the Format tab.</span></span>
52. <span data-ttu-id="43b2e-171">Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-171">In the tree, select 'Intrastat\Data\Totals by blocks\Lines counting'.</span></span>
53. <span data-ttu-id="43b2e-172">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="43b2e-172">Click the Mapping tab.</span></span>
54. <span data-ttu-id="43b2e-173">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-173">Click Edit formula.</span></span>
    * <span data-ttu-id="43b2e-174">Opret output for antallet af linjer for hver blok, der vises i denne rapport.</span><span class="sxs-lookup"><span data-stu-id="43b2e-174">Create output for the number of lines for each block presented in this report.</span></span>  
55. <span data-ttu-id="43b2e-175">Skriv '"Antal linjer i denne blok: " & ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-175">In the Formula field, enter '"Number of lines in this block: " & '.</span></span>
    * <span data-ttu-id="43b2e-176">"Antal linjer i denne blok: " &</span><span class="sxs-lookup"><span data-stu-id="43b2e-176">"Number of lines in this block: " &</span></span>  
56. <span data-ttu-id="43b2e-177">Skriv '"Antal linjer i denne blok: " & TEXT(' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-177">In the Formula field, enter '"Number of lines in this block: " & TEXT('.</span></span>
    * <span data-ttu-id="43b2e-178">"Antal linjer i denne blok: " & TEXT(</span><span class="sxs-lookup"><span data-stu-id="43b2e-178">"Number of lines in this block: " & TEXT(</span></span>  
57. <span data-ttu-id="43b2e-179">Vælg 'Datasamlingsfunktioner\COUNTIFS' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-179">In the tree, select 'Data collection functions\COUNTIFS'.</span></span>
58. <span data-ttu-id="43b2e-180">Klik på Tilføj funktion.</span><span class="sxs-lookup"><span data-stu-id="43b2e-180">Click Add function.</span></span>
59. <span data-ttu-id="43b2e-181">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="43b2e-181">Click Add data source.</span></span>
60. <span data-ttu-id="43b2e-182">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-182">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '.</span></span>
    * <span data-ttu-id="43b2e-183">"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName',</span><span class="sxs-lookup"><span data-stu-id="43b2e-183">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName',</span></span>  
61. <span data-ttu-id="43b2e-184">Udvid '$BlocksList' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-184">In the tree, expand '$BlocksList'.</span></span>
62. <span data-ttu-id="43b2e-185">Vælg '$BlocksList\Value' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-185">In the tree, select '$BlocksList\Value'.</span></span>
63. <span data-ttu-id="43b2e-186">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="43b2e-186">Click Add data source.</span></span>
64. <span data-ttu-id="43b2e-187">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, ' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-187">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '.</span></span>
    * <span data-ttu-id="43b2e-188">"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span><span class="sxs-lookup"><span data-stu-id="43b2e-188">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value,</span></span>  
65. <span data-ttu-id="43b2e-189">Vælg '$RecName' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-189">In the tree, select '$RecName'.</span></span>
66. <span data-ttu-id="43b2e-190">Klik på Tilføj datakilde.</span><span class="sxs-lookup"><span data-stu-id="43b2e-190">Click Add data source.</span></span>
67. <span data-ttu-id="43b2e-191">Skriv '"Antal linjer i denne blok: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-191">In the Formula field, enter '"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="43b2e-192">"Antal linjer i denne blok:" & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="43b2e-192">"Number of lines in this block: " & TEXT(COUNTIFS('$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
68. <span data-ttu-id="43b2e-193">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="43b2e-193">Click Save.</span></span>
69. <span data-ttu-id="43b2e-194">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="43b2e-194">Close the page.</span></span>
70. <span data-ttu-id="43b2e-195">Klik på fanen Format.</span><span class="sxs-lookup"><span data-stu-id="43b2e-195">Click the Format tab.</span></span>
71. <span data-ttu-id="43b2e-196">Vælg 'Intrastat\Data\Totaler efter blokke\Linjeoptælling\Samlet beløb' i træet.</span><span class="sxs-lookup"><span data-stu-id="43b2e-196">In the tree, select 'Intrastat\Data\Totals by blocks\Total amount'.</span></span>
72. <span data-ttu-id="43b2e-197">Klik på fanen Tilknytning.</span><span class="sxs-lookup"><span data-stu-id="43b2e-197">Click the Mapping tab.</span></span>
73. <span data-ttu-id="43b2e-198">Klik på Rediger formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-198">Click Edit formula.</span></span>
    * <span data-ttu-id="43b2e-199">Opret output, der er summen af det fakturerede beløb for hver blok, der vises i denne rapport.</span><span class="sxs-lookup"><span data-stu-id="43b2e-199">Create output that will be the total of the invoiced amount for each block presented in this report.</span></span>  
74. <span data-ttu-id="43b2e-200">Skriv '"Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))' i feltet Formel.</span><span class="sxs-lookup"><span data-stu-id="43b2e-200">In the Formula field, enter '"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))'.</span></span>
    * <span data-ttu-id="43b2e-201">"Sum af faktureret beløb: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span><span class="sxs-lookup"><span data-stu-id="43b2e-201">"Sum of invoiced amount: " & TEXT(SUMIFS('$InvName', '$BlockName', '$BlocksList'.Value, '$RecName', "\*"))</span></span>  
75. <span data-ttu-id="43b2e-202">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="43b2e-202">Click Save.</span></span>
76. <span data-ttu-id="43b2e-203">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="43b2e-203">Close the page.</span></span>
77. <span data-ttu-id="43b2e-204">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="43b2e-204">Click Save.</span></span>
78. <span data-ttu-id="43b2e-205">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="43b2e-205">Close the page.</span></span>


