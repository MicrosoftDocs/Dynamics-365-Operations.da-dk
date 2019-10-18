---
title: EUR-00011 Konfigurere rapportering for EU-listesystemet
description: Denne opgave gennemgår en oversigt over de forudsætninger, der er nødvendige for EU-listesystem-rapportering.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ERWorkspace, ERSolutionRepositoryTable, ERSolutionImport, SysQueryForm, SysQueryFieldLookUp,  TaxTable, TaxGroup, TaxItemGroup, TaxCountryRegionParameters, TaxVATNumTable, IntrastatParameters, CustTable, DirPartyQuickCreateForm
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b44d439bf1e991380fb7273a70e1f69f807c8b25
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2175093"
---
# <a name="eur-00011-set-up-eu-sales-list-reporting"></a><span data-ttu-id="5ae86-103">EUR-00011 Konfigurere rapportering for EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="5ae86-103">EUR-00011 Set up EU sales list reporting</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5ae86-104">Denne opgave gennemgår en oversigt over de forudsætninger, der er nødvendige for EU-listesystem-rapportering.</span><span class="sxs-lookup"><span data-stu-id="5ae86-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="5ae86-105">Du kan finde flere oplysninger om rapportering i EU-listesystemet, herunder de nødvendige forudsætninger, i Hjælp.</span><span class="sxs-lookup"><span data-stu-id="5ae86-105">For more information about EU Sales list reporting, including required prerequisites, refer to Help.</span></span>

<span data-ttu-id="5ae86-106">Denne opgave gælder for alle europæiske lande/områder.</span><span class="sxs-lookup"><span data-stu-id="5ae86-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="5ae86-107">Guiden er oprettet ved hjælp af demodatafirmaet DEMF og bruger derfor Tyskland som et EU-land/områdeeksempel.</span><span class="sxs-lookup"><span data-stu-id="5ae86-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="5ae86-108">Guiden bruger også Portugal som et EU-land/områdeeksempel.</span><span class="sxs-lookup"><span data-stu-id="5ae86-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="5ae86-109">Disse opgaver er beregnet til systemadministratorer.</span><span class="sxs-lookup"><span data-stu-id="5ae86-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="5ae86-110">Importer konfiguration for elektronisk rapportering for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="5ae86-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="5ae86-111">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="5ae86-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="5ae86-112">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="5ae86-112">Click Set active.</span></span>
3. <span data-ttu-id="5ae86-113">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="5ae86-113">Click Repositories.</span></span>
4. <span data-ttu-id="5ae86-114">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="5ae86-114">Click Open.</span></span>
5. <span data-ttu-id="5ae86-115">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5ae86-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="5ae86-116">Klik på Avanceret filtrering/sortering.</span><span class="sxs-lookup"><span data-stu-id="5ae86-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="5ae86-117">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="5ae86-117">Click Add.</span></span>
8. <span data-ttu-id="5ae86-118">Vælg "Konfigurationsnavn" i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="5ae86-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="5ae86-119">Skriv '"EU-listesystem (DE)" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="5ae86-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="5ae86-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5ae86-120">Click OK.</span></span>
11. <span data-ttu-id="5ae86-121">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="5ae86-121">Click Import.</span></span>
12. <span data-ttu-id="5ae86-122">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="5ae86-122">Click Yes.</span></span>
13. <span data-ttu-id="5ae86-123">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="5ae86-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="5ae86-124">Klik på Avanceret filtrering/sortering.</span><span class="sxs-lookup"><span data-stu-id="5ae86-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="5ae86-125">Klik på Nulstil.</span><span class="sxs-lookup"><span data-stu-id="5ae86-125">Click Reset.</span></span>
16. <span data-ttu-id="5ae86-126">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="5ae86-126">Click Add.</span></span>
17. <span data-ttu-id="5ae86-127">Vælg "Konfigurationsnavn" i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="5ae86-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="5ae86-128">Skriv "EU-listesystemrapport efter rækker'" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="5ae86-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="5ae86-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5ae86-129">Click OK.</span></span>
20. <span data-ttu-id="5ae86-130">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="5ae86-130">Click Import.</span></span>
21. <span data-ttu-id="5ae86-131">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="5ae86-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="5ae86-132">Opsætning af momskoder for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="5ae86-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="5ae86-133">Gå til Moms > Indirekte skatter > Moms > Momskoder.</span><span class="sxs-lookup"><span data-stu-id="5ae86-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="5ae86-134">Brug Quick Filter til at filtrere på feltet Momskode med værdien ''VAT19".</span><span class="sxs-lookup"><span data-stu-id="5ae86-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="5ae86-135">Udvid sektionen Rapportopsætning.</span><span class="sxs-lookup"><span data-stu-id="5ae86-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="5ae86-136">Kontroller, at sektionen Udelukket er angivet til Nej.</span><span class="sxs-lookup"><span data-stu-id="5ae86-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="5ae86-137">Du skal muligvis oplåse opgaveguiden for at ændre denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="5ae86-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="5ae86-138">Opsætning af momsgrupper for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="5ae86-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="5ae86-139">Gå til Moms > Indirekte skatter > Moms > Momsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5ae86-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="5ae86-140">Brug Quick Filter til at filtrere på feltet Momsgruppe med værdien ''AR-DOM".</span><span class="sxs-lookup"><span data-stu-id="5ae86-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="5ae86-141">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="5ae86-141">Click Edit.</span></span>
4. <span data-ttu-id="5ae86-142">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="5ae86-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="5ae86-143">Marker den første række på listen.</span><span class="sxs-lookup"><span data-stu-id="5ae86-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="5ae86-144">Marker afkrydsningsfeltet Momsfri.</span><span class="sxs-lookup"><span data-stu-id="5ae86-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="5ae86-145">Marker den anden række på listen.</span><span class="sxs-lookup"><span data-stu-id="5ae86-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="5ae86-146">Marker afkrydsningsfeltet Momsfri.</span><span class="sxs-lookup"><span data-stu-id="5ae86-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="5ae86-147">Marker den tredje række på listen.</span><span class="sxs-lookup"><span data-stu-id="5ae86-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="5ae86-148">Marker afkrydsningsfeltet Momsfri.</span><span class="sxs-lookup"><span data-stu-id="5ae86-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="5ae86-149">Opsætning af varemomsgrupper for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="5ae86-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="5ae86-150">Gå til Moms > Indirekte skatter > Moms > Momsgrupper.</span><span class="sxs-lookup"><span data-stu-id="5ae86-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="5ae86-151">Brug Quick Filter til at filtrere på feltet Varemomsgruppe med værdien ''FULL".</span><span class="sxs-lookup"><span data-stu-id="5ae86-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="5ae86-152">Kontroller, at Rapporteringstype er indstillet til "Vare".</span><span class="sxs-lookup"><span data-stu-id="5ae86-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="5ae86-153">Du skal muligvis oplåse opgaveguiden for at ændre værdien i dette felt.</span><span class="sxs-lookup"><span data-stu-id="5ae86-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="5ae86-154">Brug Quick Filter til at filtrere på feltet Varemomsgruppe med værdien ''RED".</span><span class="sxs-lookup"><span data-stu-id="5ae86-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="5ae86-155">Kontroller, at Rapporteringstype er indstillet til "Service".</span><span class="sxs-lookup"><span data-stu-id="5ae86-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="5ae86-156">Du skal muligvis oplåse opgaveguiden for at ændre værdien i dette felt.</span><span class="sxs-lookup"><span data-stu-id="5ae86-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="5ae86-157">Konfigurere parametre for land/område for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="5ae86-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="5ae86-158">Gå til Skat > Opsætning > Moms > Land/områdeparametre.</span><span class="sxs-lookup"><span data-stu-id="5ae86-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="5ae86-159">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5ae86-159">Click New.</span></span>
3. <span data-ttu-id="5ae86-160">Skriv "PRT" i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="5ae86-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="5ae86-161">Skriv 'PT' i feltet Moms.</span><span class="sxs-lookup"><span data-stu-id="5ae86-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="5ae86-162">Oprette SE-numre</span><span class="sxs-lookup"><span data-stu-id="5ae86-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="5ae86-163">Gå til Skat > Opsætning > Moms > SE-numre.</span><span class="sxs-lookup"><span data-stu-id="5ae86-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="5ae86-164">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5ae86-164">Click New.</span></span>
3. <span data-ttu-id="5ae86-165">Skriv "PRT" i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="5ae86-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="5ae86-166">Skriv "PT12345" i feltet SE-nummer.</span><span class="sxs-lookup"><span data-stu-id="5ae86-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="5ae86-167">Konfigurere parametre for rapportering for EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="5ae86-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="5ae86-168">Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre.</span><span class="sxs-lookup"><span data-stu-id="5ae86-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="5ae86-169">Klik på fanen EU-listesystem.</span><span class="sxs-lookup"><span data-stu-id="5ae86-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="5ae86-170">Vælg Ja i feltet Overfør køb.</span><span class="sxs-lookup"><span data-stu-id="5ae86-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="5ae86-171">Udvid sektionen Afrundingsregler.</span><span class="sxs-lookup"><span data-stu-id="5ae86-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="5ae86-172">Indstil Afrundingsregel til "0.1".</span><span class="sxs-lookup"><span data-stu-id="5ae86-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="5ae86-173">Vælg Ja i feltet Brug minimumværdi.</span><span class="sxs-lookup"><span data-stu-id="5ae86-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="5ae86-174">Skriv "2" i feltet Antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="5ae86-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="5ae86-175">Udvid sektionen Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="5ae86-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="5ae86-176">Vælg "EU-listesystem (DE)" i feltet Filformattilknytning.</span><span class="sxs-lookup"><span data-stu-id="5ae86-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="5ae86-177">Vælg "EU-listesystemrapport efter rækker" i feltet Filformattilknytning.</span><span class="sxs-lookup"><span data-stu-id="5ae86-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="5ae86-178">Klik på fanen Egenskaber for land/område.</span><span class="sxs-lookup"><span data-stu-id="5ae86-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="5ae86-179">Kontroller, at feltet Lande-/områdetype er angivet til "Indland" for landet/området DEU.</span><span class="sxs-lookup"><span data-stu-id="5ae86-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="5ae86-180">Du skal muligvis oplåse opgaveguiden for at ændre værdien i dette felt.</span><span class="sxs-lookup"><span data-stu-id="5ae86-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="5ae86-181">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5ae86-181">Click New.</span></span>
13. <span data-ttu-id="5ae86-182">Skriv "PRT" i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="5ae86-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="5ae86-183">Skriv 'PT' i feltet Intrastat-kode.</span><span class="sxs-lookup"><span data-stu-id="5ae86-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="5ae86-184">Vælg "EU" i feltet Lande-/områdetype.</span><span class="sxs-lookup"><span data-stu-id="5ae86-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="5ae86-185">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="5ae86-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="5ae86-186">Kontroller, at der er angivet en nummerseriekode for referencen "EU-listesystem".</span><span class="sxs-lookup"><span data-stu-id="5ae86-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="5ae86-187">Oprette en kunde med henblik på demonstration af EU-rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="5ae86-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="5ae86-188">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="5ae86-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="5ae86-189">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5ae86-189">Click New.</span></span>
3. <span data-ttu-id="5ae86-190">Skriv "PRT-001" i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="5ae86-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="5ae86-191">Skriv 'En kunde fra Portugal' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="5ae86-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="5ae86-192">Vælg "10" i feltet Kundegruppe.</span><span class="sxs-lookup"><span data-stu-id="5ae86-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="5ae86-193">Vælg "AR-DOM" i feltet Momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="5ae86-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="5ae86-194">Vælg "PT12345" i feltet SE-nummer.</span><span class="sxs-lookup"><span data-stu-id="5ae86-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="5ae86-195">Skriv "PRT" i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="5ae86-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="5ae86-196">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="5ae86-196">Click Save.</span></span>

