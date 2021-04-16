---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 4: Kørselsformat)'
description: Dette emne beskriver, hvordan du konfigurerer et format for elektronisk rapportering til optælling og opsummering baseret på data fra det allerede genererede tekstoutput. (Del 4)
author: NickSelin
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5792505de78aad458bd8745630915cf58f05f73f
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5748967"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4---run-format"></a><span data-ttu-id="71e65-104">ER Konfigurere format for at udføre optælling og sammenlægning (del 4: Kørselsformat)</span><span class="sxs-lookup"><span data-stu-id="71e65-104">ER Configure format to do counting and summing (Part 4 - Run format)</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="71e65-105">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="71e65-105">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="71e65-106">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="71e65-106">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="71e65-107">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 3: Brug beregninger til at oprette output)".</span><span class="sxs-lookup"><span data-stu-id="71e65-107">To complete these steps, you must first complete the steps in the "ER Configure format to do counting and summing (Part 3: Use computations to make the output)" procedure.</span></span>

<span data-ttu-id="71e65-108">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="71e65-108">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="71e65-109">Test denne konfiguration til oprettelse af Intrastat-rapporter</span><span class="sxs-lookup"><span data-stu-id="71e65-109">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="71e65-110">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="71e65-110">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="71e65-111">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="71e65-111">Click Reporting configurations.</span></span>
3. <span data-ttu-id="71e65-112">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="71e65-112">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="71e65-113">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="71e65-113">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="71e65-114">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="71e65-114">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="71e65-115">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="71e65-115">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="71e65-116">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="71e65-116">Click User parameters.</span></span>
8. <span data-ttu-id="71e65-117">Vælg Ja i feltet Indstillinger for kørsel.</span><span class="sxs-lookup"><span data-stu-id="71e65-117">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="71e65-118">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71e65-118">Click OK.</span></span>
10. <span data-ttu-id="71e65-119">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="71e65-119">Click Edit.</span></span>
11. <span data-ttu-id="71e65-120">Vælg Ja i feltet Udkast til kørsel.</span><span class="sxs-lookup"><span data-stu-id="71e65-120">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="71e65-121">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="71e65-121">Click Save.</span></span>
13. <span data-ttu-id="71e65-122">Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre.</span><span class="sxs-lookup"><span data-stu-id="71e65-122">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="71e65-123">Udvid sektionen Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="71e65-123">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="71e65-124">Vælg konfigurationen "Intrastat (DE) med optælling og sammenlægning".</span><span class="sxs-lookup"><span data-stu-id="71e65-124">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
16. <span data-ttu-id="71e65-125">Vælg konfigurationen "Intrastat (DE) med optælling og sammenlægning".</span><span class="sxs-lookup"><span data-stu-id="71e65-125">Select the "Intrastat (DE) with counting & summing" configuration.</span></span>
17. <span data-ttu-id="71e65-126">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="71e65-126">Click Save.</span></span>
18. <span data-ttu-id="71e65-127">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="71e65-127">Close the page.</span></span>
19. <span data-ttu-id="71e65-128">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="71e65-128">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="71e65-129">Klik på Output.</span><span class="sxs-lookup"><span data-stu-id="71e65-129">Click Output.</span></span>
21. <span data-ttu-id="71e65-130">Klik på Rapport.</span><span class="sxs-lookup"><span data-stu-id="71e65-130">Click Report.</span></span>
    * <span data-ttu-id="71e65-131">Kør processen til oprettelse af Intrastat-rapport.</span><span class="sxs-lookup"><span data-stu-id="71e65-131">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="71e65-132">I feltet Fra dato skal du angive datoen til "2000-01-01".</span><span class="sxs-lookup"><span data-stu-id="71e65-132">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="71e65-133">Definer start- og slutdatoer for af rapporteringsperioden, som omfatter de eksisterende posteringer i formen.</span><span class="sxs-lookup"><span data-stu-id="71e65-133">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="71e65-134">I feltet Til dato skal du angive datoen til "2022-12-31".</span><span class="sxs-lookup"><span data-stu-id="71e65-134">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="71e65-135">Definer start- og slutdatoer for af rapporteringsperioden, som omfatter de eksisterende posteringer i formen.</span><span class="sxs-lookup"><span data-stu-id="71e65-135">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="71e65-136">Vælg 'Indførsel' i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="71e65-136">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="71e65-137">Vælg Ja i feltet Generer fil.</span><span class="sxs-lookup"><span data-stu-id="71e65-137">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="71e65-138">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71e65-138">Click OK.</span></span>
    * <span data-ttu-id="71e65-139">Få vist oprettet output med oversigtslinjer i slutningen.</span><span class="sxs-lookup"><span data-stu-id="71e65-139">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="71e65-140">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="71e65-140">Click New.</span></span>
28. <span data-ttu-id="71e65-141">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="71e65-141">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="71e65-142">Vælg 'Udførsel' i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="71e65-142">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="71e65-143">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="71e65-143">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="71e65-144">Indtast eller vælg en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="71e65-144">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="71e65-145">Angiv Vægt til 10</span><span class="sxs-lookup"><span data-stu-id="71e65-145">Set Weight to '10'.</span></span>
33. <span data-ttu-id="71e65-146">Angiv Fakturabeløb til '10000'.</span><span class="sxs-lookup"><span data-stu-id="71e65-146">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="71e65-147">Angiv Statistisk beløb til '10000'.</span><span class="sxs-lookup"><span data-stu-id="71e65-147">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="71e65-148">Klik på Output.</span><span class="sxs-lookup"><span data-stu-id="71e65-148">Click Output.</span></span>
36. <span data-ttu-id="71e65-149">Klik på Rapport.</span><span class="sxs-lookup"><span data-stu-id="71e65-149">Click Report.</span></span>
37. <span data-ttu-id="71e65-150">Vælg 'Udførsel' i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="71e65-150">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="71e65-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71e65-151">Click OK.</span></span>
    * <span data-ttu-id="71e65-152">Få vist oprettet output med oversigtslinjer i slutningen.</span><span class="sxs-lookup"><span data-stu-id="71e65-152">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="71e65-153">Bemærk, at det er blevet ændret sammenlignet med den første kørsel.</span><span class="sxs-lookup"><span data-stu-id="71e65-153">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="71e65-154">Kør denne konfiguration i fejlfindingstilstand for at gennemse indsamlede optællings- og sammenlægningsdata</span><span class="sxs-lookup"><span data-stu-id="71e65-154">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="71e65-155">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="71e65-155">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="71e65-156">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="71e65-156">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="71e65-157">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="71e65-157">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="71e65-158">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="71e65-158">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="71e65-159">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="71e65-159">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="71e65-160">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="71e65-160">Click User parameters.</span></span>
7. <span data-ttu-id="71e65-161">Vælg Ja i feltet Kør i fejlfindingstilstand.</span><span class="sxs-lookup"><span data-stu-id="71e65-161">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="71e65-162">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71e65-162">Click OK.</span></span>
9. <span data-ttu-id="71e65-163">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="71e65-163">Close the page.</span></span>
10. <span data-ttu-id="71e65-164">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="71e65-164">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="71e65-165">Klik på Output.</span><span class="sxs-lookup"><span data-stu-id="71e65-165">Click Output.</span></span>
12. <span data-ttu-id="71e65-166">Klik på Rapport.</span><span class="sxs-lookup"><span data-stu-id="71e65-166">Click Report.</span></span>
13. <span data-ttu-id="71e65-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="71e65-167">Click OK.</span></span>
14. <span data-ttu-id="71e65-168">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="71e65-168">Close the page.</span></span>
15. <span data-ttu-id="71e65-169">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="71e65-169">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="71e65-170">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="71e65-170">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="71e65-171">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="71e65-171">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="71e65-172">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="71e65-172">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="71e65-173">Klik på Fejlfindingslogfiler.</span><span class="sxs-lookup"><span data-stu-id="71e65-173">Click Debug logs.</span></span>
    * <span data-ttu-id="71e65-174">Bemærk, at der er oprettet en fejlfindingslogpost for kørselsprocessen for den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="71e65-174">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="71e65-175">Klik på Vedhæft.</span><span class="sxs-lookup"><span data-stu-id="71e65-175">Click Attach.</span></span>
21. <span data-ttu-id="71e65-176">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="71e65-176">Click Open.</span></span>
    * <span data-ttu-id="71e65-177">Gennemse den XML-fil, der indeholder optællings- og sammenlægningsdetaljer, der er indsamlet under kørsel af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="71e65-177">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  



[!INCLUDE[footer-include](../../../../includes/footer-banner.md)]