---
title: 'ER Konfigurere format for at udføre optælling og sammenlægning (del 4: Kørselsformat)'
description: Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.
author: NickSelin
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionTable, IntrastatParameters, Intrastat, InventItemIdLookupSimple, IntrastatCommodityLookup, ERFormatMappingRunLogTable, DocuView
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 17989b7fa2baf14472ec19a041cb5ce7e5c0380d
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "336192"
---
# <a name="er-configure-format-to-do-counting-and-summing-part-4-run-format"></a><span data-ttu-id="1f072-103">ER Konfigurere format for at udføre optælling og sammenlægning (del 4: Kørselsformat)</span><span class="sxs-lookup"><span data-stu-id="1f072-103">ER Configure format to do counting and summing (Part 4: Run format)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="1f072-104">Følgende trin beskriver, hvordan en bruger, der er tildelt til rollen som systemadministrator eller udvikler til elektronisk rapportering, kan konfigurere en model for elektronisk rapportering (ER) til at udføre optælling og sammenlægning baseret på data i det tekstoutput, der allerede er oprettet.</span><span class="sxs-lookup"><span data-stu-id="1f072-104">The following steps explain how a user assigned to the system administrator or electronic reporting developer role can configure an Electronic reporting (ER) format to do counting and summing based on data of the already generated text output.</span></span> <span data-ttu-id="1f072-105">Disse trin kan udføres i DEMF-virksomheden.</span><span class="sxs-lookup"><span data-stu-id="1f072-105">These steps can be performed in the DEMF company.</span></span>

<span data-ttu-id="1f072-106">For at fuldføre disse trin skal du først udføre trinnene i proceduren "Konfigurer ER-format til optælling og sammenlægning (del 3: Brug beregninger til at oprette output)".</span><span class="sxs-lookup"><span data-stu-id="1f072-106">To complete these steps, you must first complete the steps in the “ER Configure format to do counting and summing (Part 3: Use computations to make the output)” procedure.</span></span>

<span data-ttu-id="1f072-107">Denne procedure er beregnet til en funktion, der blev tilføjet i Dynamics 365 for Operations version 1611.</span><span class="sxs-lookup"><span data-stu-id="1f072-107">This procedure is for a feature that was added in Dynamics 365 for Operations version 1611.</span></span>


## <a name="test-this-configuration-for-generation-of-the-intrastat-reports"></a><span data-ttu-id="1f072-108">Test denne konfiguration til oprettelse af Intrastat-rapporter</span><span class="sxs-lookup"><span data-stu-id="1f072-108">Test this configuration for generation of the Intrastat reports</span></span>
1. <span data-ttu-id="1f072-109">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="1f072-109">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="1f072-110">Klik på Rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="1f072-110">Click Reporting configurations.</span></span>
3. <span data-ttu-id="1f072-111">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="1f072-111">In the tree, expand 'Intrastat model'.</span></span>
4. <span data-ttu-id="1f072-112">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="1f072-112">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
5. <span data-ttu-id="1f072-113">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="1f072-113">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
6. <span data-ttu-id="1f072-114">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1f072-114">On the Action Pane, click Configurations.</span></span>
7. <span data-ttu-id="1f072-115">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="1f072-115">Click User parameters.</span></span>
8. <span data-ttu-id="1f072-116">Vælg Ja i feltet Indstillinger for kørsel.</span><span class="sxs-lookup"><span data-stu-id="1f072-116">Select Yes in the Run settings field.</span></span>
9. <span data-ttu-id="1f072-117">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1f072-117">Click OK.</span></span>
10. <span data-ttu-id="1f072-118">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="1f072-118">Click Edit.</span></span>
11. <span data-ttu-id="1f072-119">Vælg Ja i feltet Udkast til kørsel.</span><span class="sxs-lookup"><span data-stu-id="1f072-119">Select Yes in the Run Draft field.</span></span>
12. <span data-ttu-id="1f072-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="1f072-120">Click Save.</span></span>
13. <span data-ttu-id="1f072-121">Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre.</span><span class="sxs-lookup"><span data-stu-id="1f072-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
14. <span data-ttu-id="1f072-122">Udvid sektionen Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="1f072-122">Expand the Electronic reporting section.</span></span>
15. <span data-ttu-id="1f072-123">Vælg konfigurationen "Intrastat (DE) med optælling og sammenlægning".</span><span class="sxs-lookup"><span data-stu-id="1f072-123">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
16. <span data-ttu-id="1f072-124">Vælg konfigurationen "Intrastat (DE) med optælling og sammenlægning".</span><span class="sxs-lookup"><span data-stu-id="1f072-124">Select the “Intrastat (DE) with counting & summing” configuration.</span></span>
17. <span data-ttu-id="1f072-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="1f072-125">Click Save.</span></span>
18. <span data-ttu-id="1f072-126">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1f072-126">Close the page.</span></span>
19. <span data-ttu-id="1f072-127">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="1f072-127">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
20. <span data-ttu-id="1f072-128">Klik på Output.</span><span class="sxs-lookup"><span data-stu-id="1f072-128">Click Output.</span></span>
21. <span data-ttu-id="1f072-129">Klik på Rapport.</span><span class="sxs-lookup"><span data-stu-id="1f072-129">Click Report.</span></span>
    * <span data-ttu-id="1f072-130">Kør processen til oprettelse af Intrastat-rapport.</span><span class="sxs-lookup"><span data-stu-id="1f072-130">Run the Intrastat report generation process.</span></span>  
22. <span data-ttu-id="1f072-131">I feltet Fra dato skal du angive datoen til "2000-01-01".</span><span class="sxs-lookup"><span data-stu-id="1f072-131">In the From date field, set the date to '2000-01-01'.</span></span>
    * <span data-ttu-id="1f072-132">Definer start- og slutdatoer for af rapporteringsperioden, som omfatter de eksisterende posteringer i formen.</span><span class="sxs-lookup"><span data-stu-id="1f072-132">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
23. <span data-ttu-id="1f072-133">I feltet Til dato skal du angive datoen til "2022-12-31".</span><span class="sxs-lookup"><span data-stu-id="1f072-133">In the To date field, set the date to '2022-12-31'.</span></span>
    * <span data-ttu-id="1f072-134">Definer start- og slutdatoer for af rapporteringsperioden, som omfatter de eksisterende posteringer i formen.</span><span class="sxs-lookup"><span data-stu-id="1f072-134">Define start and end dates for the reporting period that include the existing on the form transactions.</span></span>  
24. <span data-ttu-id="1f072-135">Vælg 'Indførsel' i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="1f072-135">In the Direction field, select 'Arrivals'.</span></span>
25. <span data-ttu-id="1f072-136">Vælg Ja i feltet Generer fil.</span><span class="sxs-lookup"><span data-stu-id="1f072-136">Select Yes in the Generate file field.</span></span>
26. <span data-ttu-id="1f072-137">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1f072-137">Click OK.</span></span>
    * <span data-ttu-id="1f072-138">Få vist oprettet output med oversigtslinjer i slutningen.</span><span class="sxs-lookup"><span data-stu-id="1f072-138">Review the created output with the summary lines in the end.</span></span>  
27. <span data-ttu-id="1f072-139">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="1f072-139">Click New.</span></span>
28. <span data-ttu-id="1f072-140">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="1f072-140">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="1f072-141">Vælg 'Udførsel' i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="1f072-141">In the Direction field, select 'Dispatches'.</span></span>
30. <span data-ttu-id="1f072-142">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="1f072-142">In the Item number field, enter or select a value.</span></span>
31. <span data-ttu-id="1f072-143">Indtast eller vælg en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="1f072-143">In the Commodity field, enter or select a value.</span></span>
32. <span data-ttu-id="1f072-144">Angiv Vægt til 10</span><span class="sxs-lookup"><span data-stu-id="1f072-144">Set Weight to '10'.</span></span>
33. <span data-ttu-id="1f072-145">Angiv Fakturabeløb til '10000'.</span><span class="sxs-lookup"><span data-stu-id="1f072-145">Set Invoice amount to '10000'.</span></span>
34. <span data-ttu-id="1f072-146">Angiv Statistisk beløb til '10000'.</span><span class="sxs-lookup"><span data-stu-id="1f072-146">Set Statistical amount to '10000'.</span></span>
35. <span data-ttu-id="1f072-147">Klik på Output.</span><span class="sxs-lookup"><span data-stu-id="1f072-147">Click Output.</span></span>
36. <span data-ttu-id="1f072-148">Klik på Rapport.</span><span class="sxs-lookup"><span data-stu-id="1f072-148">Click Report.</span></span>
37. <span data-ttu-id="1f072-149">Vælg 'Udførsel' i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="1f072-149">In the Direction field, select 'Dispatches'.</span></span>
38. <span data-ttu-id="1f072-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1f072-150">Click OK.</span></span>
    * <span data-ttu-id="1f072-151">Få vist oprettet output med oversigtslinjer i slutningen.</span><span class="sxs-lookup"><span data-stu-id="1f072-151">Review the created output with the summary lines in the end.</span></span> <span data-ttu-id="1f072-152">Bemærk, at det er blevet ændret sammenlignet med den første kørsel.</span><span class="sxs-lookup"><span data-stu-id="1f072-152">Note that it has been changed in comparison to the first run.</span></span>  

## <a name="run-this-configuration-in-debug-mode-to-review-the-collected-counting--summing-data"></a><span data-ttu-id="1f072-153">Kør denne konfiguration i fejlfindingstilstand for at gennemse indsamlede optællings- og sammenlægningsdata</span><span class="sxs-lookup"><span data-stu-id="1f072-153">Run this configuration in debug mode to review the collected counting & summing data</span></span>
1. <span data-ttu-id="1f072-154">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="1f072-154">Go to Organization administration > Electronic reporting > Configurations.</span></span>
2. <span data-ttu-id="1f072-155">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="1f072-155">In the tree, expand 'Intrastat model'.</span></span>
3. <span data-ttu-id="1f072-156">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="1f072-156">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
4. <span data-ttu-id="1f072-157">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="1f072-157">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
5. <span data-ttu-id="1f072-158">Klik på Konfigurationer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1f072-158">On the Action Pane, click Configurations.</span></span>
6. <span data-ttu-id="1f072-159">Klik på Brugerparametre.</span><span class="sxs-lookup"><span data-stu-id="1f072-159">Click User parameters.</span></span>
7. <span data-ttu-id="1f072-160">Vælg Ja i feltet Kør i fejlfindingstilstand.</span><span class="sxs-lookup"><span data-stu-id="1f072-160">Select Yes in the Run in debug mode field.</span></span>
8. <span data-ttu-id="1f072-161">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1f072-161">Click OK.</span></span>
9. <span data-ttu-id="1f072-162">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1f072-162">Close the page.</span></span>
10. <span data-ttu-id="1f072-163">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat.</span><span class="sxs-lookup"><span data-stu-id="1f072-163">Go to Tax > Declarations > Foreign trade > Intrastat.</span></span>
11. <span data-ttu-id="1f072-164">Klik på Output.</span><span class="sxs-lookup"><span data-stu-id="1f072-164">Click Output.</span></span>
12. <span data-ttu-id="1f072-165">Klik på Rapport.</span><span class="sxs-lookup"><span data-stu-id="1f072-165">Click Report.</span></span>
13. <span data-ttu-id="1f072-166">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="1f072-166">Click OK.</span></span>
14. <span data-ttu-id="1f072-167">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="1f072-167">Close the page.</span></span>
15. <span data-ttu-id="1f072-168">Gå til Virksomhedsadministration > Elektronisk rapportering > Konfigurationer.</span><span class="sxs-lookup"><span data-stu-id="1f072-168">Go to Organization administration > Electronic reporting > Configurations.</span></span>
16. <span data-ttu-id="1f072-169">Udvid 'Intrastat-model' i træet.</span><span class="sxs-lookup"><span data-stu-id="1f072-169">In the tree, expand 'Intrastat model'.</span></span>
17. <span data-ttu-id="1f072-170">Udvid 'Intrastat-model\Intrastat (DE)' i træet.</span><span class="sxs-lookup"><span data-stu-id="1f072-170">In the tree, expand 'Intrastat model\Intrastat (DE)'.</span></span>
18. <span data-ttu-id="1f072-171">Vælg 'Intrastat-model\Intrastat (DE)\Intrastat (DE) med optælling og sammenlægning' i træet.</span><span class="sxs-lookup"><span data-stu-id="1f072-171">In the tree, select 'Intrastat model\Intrastat (DE)\Intrastat (DE) with counting & summing'.</span></span>
19. <span data-ttu-id="1f072-172">Klik på Fejlfindingslogfiler.</span><span class="sxs-lookup"><span data-stu-id="1f072-172">Click Debug logs.</span></span>
    * <span data-ttu-id="1f072-173">Bemærk, at der er oprettet en fejlfindingslogpost for kørselsprocessen for den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1f072-173">Note that a debug log record has been created for the execution process of the selected configuration.</span></span>  
20. <span data-ttu-id="1f072-174">Klik på Vedhæft.</span><span class="sxs-lookup"><span data-stu-id="1f072-174">Click Attach.</span></span>
21. <span data-ttu-id="1f072-175">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="1f072-175">Click Open.</span></span>
    * <span data-ttu-id="1f072-176">Gennemse den XML-fil, der indeholder optællings- og sammenlægningsdetaljer, der er indsamlet under kørsel af den valgte konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1f072-176">Review the created XML file that contains counting and summing details that were collected during the execution of the selected configuration.</span></span>  

