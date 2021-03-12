---
title: EUR-00002 Generere en EU Intrastat-opgørelse
description: Denne procedure fører dig gennem de trin, der kræves for at eksportere Intrastat-opgørelsen i det elektroniske filformat og gennemse opgørelsens data i et Excel-format.
author: Anasyash
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, IntrastatParameters, IntrastatCommodityLookup, IntrastatCompressParameters, Intrastat, SysQueryForm
audience: Application User
ms.reviewer: kfend
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: anasyash
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 581a837049f239cb9b9fa41eb978304751cb3b54
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4989975"
---
# <a name="eur-00002-generate-an-eu-intrastat-declaration"></a><span data-ttu-id="d531d-103">EUR-00002 Generere en EU Intrastat-opgørelse</span><span class="sxs-lookup"><span data-stu-id="d531d-103">EUR-00002 Generate an EU Intrastat declaration</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="d531d-104">Denne procedure fører dig gennem de trin, der kræves for at eksportere Intrastat-opgørelsen i det elektroniske filformat og gennemse opgørelsens data i et Excel-format.</span><span class="sxs-lookup"><span data-stu-id="d531d-104">This procedure walks you through the steps required to export the Intrastat declaration in the electronic file format and preview the declaration data in an Excel format.</span></span> 

<span data-ttu-id="d531d-105">Før du kan udføre denne procedure, skal du overføre transaktioner til Intrastat.</span><span class="sxs-lookup"><span data-stu-id="d531d-105">Before you can complete this procedure, you must transfer transactions to the Intrastat.</span></span> 

<span data-ttu-id="d531d-106">Denne procedure blev oprettet ved hjælp af demodatafirmaet DEMF.</span><span class="sxs-lookup"><span data-stu-id="d531d-106">This procedure was created using the demo data company DEMF.</span></span>


## <a name="import-configurations-with-settings"></a><span data-ttu-id="d531d-107">Importere konfigurationer med indstillinger</span><span class="sxs-lookup"><span data-stu-id="d531d-107">Import configurations with settings</span></span>
1. <span data-ttu-id="d531d-108">Gå til Arbejdsområder > Elektronisk rapportering</span><span class="sxs-lookup"><span data-stu-id="d531d-108">Go to Workspaces > Electronic reporting</span></span>
2. <span data-ttu-id="d531d-109">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="d531d-109">Click Set active.</span></span>
3. <span data-ttu-id="d531d-110">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="d531d-110">Click Repositories.</span></span>
4. <span data-ttu-id="d531d-111">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="d531d-111">Click Open.</span></span>
5. <span data-ttu-id="d531d-112">Åbn kolonnefilteret Konfigurationsnavn.</span><span class="sxs-lookup"><span data-stu-id="d531d-112">Open Configuration name column filter.</span></span>
6. <span data-ttu-id="d531d-113">Anvend et filter til feltet "Konfigurationsnavn" med værdien "Intrastat (DE)" ved hjælp af filteroperatøren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="d531d-113">Apply a filter on the "Configuration name" field, with a value of "Intrastat (DE)", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="d531d-114">Du bør vælge det konfigurationsnavn, der gælder for landets/områdets juridiske enhed.</span><span class="sxs-lookup"><span data-stu-id="d531d-114">You should select the configuration name applicable for the country of your legal entity.</span></span> <span data-ttu-id="d531d-115">Denne procedure bruger den tyske juridiske enhed (DEMF) som et eksempel, og derfor bør "Intrastat (DE)" vælges.</span><span class="sxs-lookup"><span data-stu-id="d531d-115">This procedure uses the German legal entity (DEMF) as an example, therefore "Intrastat (DE)" should be chosen.</span></span>  
    * <span data-ttu-id="d531d-116">Klik på Importér, og klik derefter på Ja.</span><span class="sxs-lookup"><span data-stu-id="d531d-116">Click Import and then click Yes.</span></span>  
7. <span data-ttu-id="d531d-117">Åbn kolonnefilteret Konfigurationsnavn.</span><span class="sxs-lookup"><span data-stu-id="d531d-117">Open Configuration name column filter.</span></span>
8. <span data-ttu-id="d531d-118">Anvend et filter til feltet "Konfigurationsnavn" med værdien "Intrastat-rapport" ved hjælp af filteroperatøren "begynder med".</span><span class="sxs-lookup"><span data-stu-id="d531d-118">Apply a filter on the "Configuration name" field, with a value of "intrastat report", using the "begins with" filter operator.</span></span>
    * <span data-ttu-id="d531d-119">Klik på Importér, og klik derefter på Ja.</span><span class="sxs-lookup"><span data-stu-id="d531d-119">Click Import and then click Yes.</span></span>  

## <a name="set-up-foreign-trade-parameters"></a><span data-ttu-id="d531d-120">Konfigurere udenrigshandelsparametre</span><span class="sxs-lookup"><span data-stu-id="d531d-120">Set up Foreign trade parameters</span></span>
1. <span data-ttu-id="d531d-121">Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre</span><span class="sxs-lookup"><span data-stu-id="d531d-121">Go to Tax > Setup > Foreign trade > Foreign trade parameters</span></span>
2. <span data-ttu-id="d531d-122">Udvid sektionen Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="d531d-122">Expand the Electronic reporting section.</span></span>
3. <span data-ttu-id="d531d-123">Indtast eller vælg værdien Intrastat (DE) i feltet Filformattilknytning.</span><span class="sxs-lookup"><span data-stu-id="d531d-123">In the File format mapping field, enter or select a value Intrastat (DE)</span></span>
4. <span data-ttu-id="d531d-124">Indtast eller vælg værdien Intrastat-rapport i feltet Rapportformattilknytning.</span><span class="sxs-lookup"><span data-stu-id="d531d-124">In the Report format mapping field, enter or select a value Intrastat report</span></span>
5. <span data-ttu-id="d531d-125">Udvid sektionen Afrundingsregler.</span><span class="sxs-lookup"><span data-stu-id="d531d-125">Expand the Rounding rules section.</span></span>
    * <span data-ttu-id="d531d-126">Du skal oprette afrundingsregler, der anvendes i dit land/område til Intrastat-rapportering.</span><span class="sxs-lookup"><span data-stu-id="d531d-126">You should set up rounding rules that are applicable in your country/region for Intrastat reporting.</span></span>  
6. <span data-ttu-id="d531d-127">Indtast et tal i feltet Afrundingsregel.</span><span class="sxs-lookup"><span data-stu-id="d531d-127">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="d531d-128">Indtast for eksempel afrundingspræcisionen '0,01'.</span><span class="sxs-lookup"><span data-stu-id="d531d-128">Enter rounding precision, for example, enter '0.01'.</span></span>  
7. <span data-ttu-id="d531d-129">Indtast et tal i feltet Antal decimaler for beløb.</span><span class="sxs-lookup"><span data-stu-id="d531d-129">In the Number of decimals for amount field, enter a number.</span></span>
    * <span data-ttu-id="d531d-130">Indtast for eksempel '2'.</span><span class="sxs-lookup"><span data-stu-id="d531d-130">For example, enter '2'.</span></span>  
8. <span data-ttu-id="d531d-131">Vælg en indstilling i feltet Afrunding under 1 kg.</span><span class="sxs-lookup"><span data-stu-id="d531d-131">In the Rounding below 1 kg field, select an option.</span></span>
    * <span data-ttu-id="d531d-132">Vælg for eksempel 'Afrunding op til 1 kg'.</span><span class="sxs-lookup"><span data-stu-id="d531d-132">For example, select 'Rounding up to 1 kg'.</span></span>  
9. <span data-ttu-id="d531d-133">Indtast et tal i feltet Afrundingsregel.</span><span class="sxs-lookup"><span data-stu-id="d531d-133">In the Rounding rule field, enter a number.</span></span>
    * <span data-ttu-id="d531d-134">Indtast for eksempel '1' for at afrunde vægten til heltallet.</span><span class="sxs-lookup"><span data-stu-id="d531d-134">For example, enter '1' for rounding weight to the integer.</span></span>  
10. <span data-ttu-id="d531d-135">Udvid sektionen Minimumsgrænse.</span><span class="sxs-lookup"><span data-stu-id="d531d-135">Expand the Minimum limit section.</span></span>
11. <span data-ttu-id="d531d-136">Angiv et tal i feltet Vægt.</span><span class="sxs-lookup"><span data-stu-id="d531d-136">In the Weight field, enter a number.</span></span>
    * <span data-ttu-id="d531d-137">Indtast for eksempel '10' som minimal vægt.</span><span class="sxs-lookup"><span data-stu-id="d531d-137">For example, enter '10' as the minimum weight.</span></span>  
12. <span data-ttu-id="d531d-138">Angiv et tal i feltet Beløb.</span><span class="sxs-lookup"><span data-stu-id="d531d-138">In the Amount field, enter a number.</span></span>
    * <span data-ttu-id="d531d-139">Indtast for eksempel '200' som minimalt beløb.</span><span class="sxs-lookup"><span data-stu-id="d531d-139">For example, enter '200' as the minimum amount.</span></span>  
13. <span data-ttu-id="d531d-140">Indtast eller vælg en værdi i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="d531d-140">In the Commodity field, enter or select a value.</span></span>

## <a name="set-up-compression-of-intrastat"></a><span data-ttu-id="d531d-141">Konfigurere komprimering af Intrastat</span><span class="sxs-lookup"><span data-stu-id="d531d-141">Set up Compression of Intrastat</span></span>
1. <span data-ttu-id="d531d-142">Gå til Skat > Konfiguration > Udenrigshandel > Komprimering af Intrastat.</span><span class="sxs-lookup"><span data-stu-id="d531d-142">Go to Tax > Setup > Foreign trade > Compression of Intrastat.</span></span>
2. <span data-ttu-id="d531d-143">Klik på Fjern.</span><span class="sxs-lookup"><span data-stu-id="d531d-143">Click Remove.</span></span>
3. <span data-ttu-id="d531d-144">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="d531d-144">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d531d-145">Vælg for eksempel Vare i sektionen Tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="d531d-145">For example, select Commodity in the Available section.</span></span>  
4. <span data-ttu-id="d531d-146">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="d531d-146">Click Add.</span></span>

## <a name="generate-intrastat-declaration"></a><span data-ttu-id="d531d-147">Generere Intrastat-opgørelse</span><span class="sxs-lookup"><span data-stu-id="d531d-147">Generate Intrastat declaration</span></span>
1. <span data-ttu-id="d531d-148">Gå til Skat > Erklæringer > Udenrigshandel > Intrastat</span><span class="sxs-lookup"><span data-stu-id="d531d-148">Go to Tax > Declarations > Foreign trade > Intrastat</span></span>
2. <span data-ttu-id="d531d-149">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="d531d-149">Click Validate.</span></span>
    * <span data-ttu-id="d531d-150">Valideringen udføres i henhold til feltet Checkkonfiguration på siden Udenrigshandelsparametre.</span><span class="sxs-lookup"><span data-stu-id="d531d-150">The validation is done according to the Check setup field on the Foreign trade parameters page.</span></span>  
3. <span data-ttu-id="d531d-151">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d531d-151">Click OK.</span></span>
4. <span data-ttu-id="d531d-152">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="d531d-152">Click Update.</span></span>
5. <span data-ttu-id="d531d-153">Klik på Minimumsgrænse</span><span class="sxs-lookup"><span data-stu-id="d531d-153">Click Minimum limit.</span></span>
6. <span data-ttu-id="d531d-154">Angiv en dato i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="d531d-154">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="d531d-155">Indtast for eksempel '1. januar 2015'.</span><span class="sxs-lookup"><span data-stu-id="d531d-155">For example, enter January 1, 2015.</span></span>  
7. <span data-ttu-id="d531d-156">Vælg Ja i feltet Komprimer.</span><span class="sxs-lookup"><span data-stu-id="d531d-156">Select Yes in the Compress field.</span></span>
8. <span data-ttu-id="d531d-157">Indtast en dato i feltet Slutdato.</span><span class="sxs-lookup"><span data-stu-id="d531d-157">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="d531d-158">Indtast for eksempel '31. januar 2015'.</span><span class="sxs-lookup"><span data-stu-id="d531d-158">For example, enter January 31, 2015.</span></span>  
9. <span data-ttu-id="d531d-159">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d531d-159">Click OK.</span></span>
10. <span data-ttu-id="d531d-160">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="d531d-160">Click Update.</span></span>
11. <span data-ttu-id="d531d-161">Klik på Komprimer.</span><span class="sxs-lookup"><span data-stu-id="d531d-161">Click Compress.</span></span>
    * <span data-ttu-id="d531d-162">Denne komprimering sker i overensstemmelse med konfigurationen af Komprimering af Intrastat.</span><span class="sxs-lookup"><span data-stu-id="d531d-162">This compression happens according to how you set the Compression of intrastate settings.</span></span>  
12. <span data-ttu-id="d531d-163">Angiv en dato i feltet Startdato.</span><span class="sxs-lookup"><span data-stu-id="d531d-163">In the Start date field, enter a date.</span></span>
    * <span data-ttu-id="d531d-164">Indtast for eksempel '1. januar 2015'.</span><span class="sxs-lookup"><span data-stu-id="d531d-164">For example, enter January 1, 2015.</span></span>  
13. <span data-ttu-id="d531d-165">Indtast en dato i feltet Slutdato.</span><span class="sxs-lookup"><span data-stu-id="d531d-165">In the End date field, enter a date.</span></span>
    * <span data-ttu-id="d531d-166">Indtast for eksempel '31. januar 2015'.</span><span class="sxs-lookup"><span data-stu-id="d531d-166">For example, enter 31st January 2015.</span></span>  
14. <span data-ttu-id="d531d-167">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d531d-167">Click OK.</span></span>
15. <span data-ttu-id="d531d-168">Klik på Opdater.</span><span class="sxs-lookup"><span data-stu-id="d531d-168">Click Update.</span></span>
16. <span data-ttu-id="d531d-169">Klik på Regenerer sekvensnumre.</span><span class="sxs-lookup"><span data-stu-id="d531d-169">Click Regenerate sequence numbers.</span></span>
17. <span data-ttu-id="d531d-170">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d531d-170">Click OK.</span></span>
18. <span data-ttu-id="d531d-171">Klik på Output.</span><span class="sxs-lookup"><span data-stu-id="d531d-171">Click Output.</span></span>
19. <span data-ttu-id="d531d-172">Klik på Rapport.</span><span class="sxs-lookup"><span data-stu-id="d531d-172">Click Report.</span></span>
20. <span data-ttu-id="d531d-173">Indtast den første dato i rapporteringsperioden i feltet Fra dato.</span><span class="sxs-lookup"><span data-stu-id="d531d-173">In the From date field, enter the first date of the reporting period.</span></span>
    * <span data-ttu-id="d531d-174">Indstil for eksempel datoen til 1. januar 2015.</span><span class="sxs-lookup"><span data-stu-id="d531d-174">For example, set the date to January 1, 2015.</span></span>  
21. <span data-ttu-id="d531d-175">Indtast en dato i feltet Til dato.</span><span class="sxs-lookup"><span data-stu-id="d531d-175">In the To date field, enter a date.</span></span>
    * <span data-ttu-id="d531d-176">Indtast for eksempel '31. januar 2015'.</span><span class="sxs-lookup"><span data-stu-id="d531d-176">For example, enter January 31, 2015.</span></span>  
22. <span data-ttu-id="d531d-177">Vælg Ja i feltet Generer fil.</span><span class="sxs-lookup"><span data-stu-id="d531d-177">Select Yes in the Generate file field.</span></span>
23. <span data-ttu-id="d531d-178">Skriv en værdi i feltet Filnavn.</span><span class="sxs-lookup"><span data-stu-id="d531d-178">In the File name field, type a value.</span></span>
24. <span data-ttu-id="d531d-179">Vælg Ja i feltet Generer rapport.</span><span class="sxs-lookup"><span data-stu-id="d531d-179">Select Yes in the Generate report field.</span></span>
25. <span data-ttu-id="d531d-180">Skriv en værdi i feltet Raportfilnavn.</span><span class="sxs-lookup"><span data-stu-id="d531d-180">In the Report file name field, type a value.</span></span>
26. <span data-ttu-id="d531d-181">Vælg en indstilling i feltet Retning.</span><span class="sxs-lookup"><span data-stu-id="d531d-181">In the Direction field, select an option.</span></span>
    * <span data-ttu-id="d531d-182">Vælg for eksempel 'Udførsel'.</span><span class="sxs-lookup"><span data-stu-id="d531d-182">For example, select 'Dispatches'.</span></span>  
27. <span data-ttu-id="d531d-183">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="d531d-183">Click OK.</span></span>

