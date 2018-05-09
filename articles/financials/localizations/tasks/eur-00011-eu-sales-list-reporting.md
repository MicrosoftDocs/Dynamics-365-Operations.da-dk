--- 
title: Konfigurere rapportering for EU-listesystemet
description: "Denne opgave gennemgår en oversigt over de forudsætninger, der er nødvendige for EU-listesystem-rapportering."
author: EvgenyPopovMBS
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Operations
ms.search.region: Austria, Belgium, Czech Republic, Denmark, Estonia, Finland, France, Germany, Hungary, Ireland, Italy, Latvia, Lithuania, Netherlands, Poland, Spain, Sweden, United Kingdom
ms.author: epopov
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 821b1403da1b4269c01e07c20e82f0de67104d84
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---
# <a name="set-up-eu-sales-list-reporting"></a><span data-ttu-id="7b4bc-103">Konfigurere rapportering for EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="7b4bc-103">Set up EU sales list reporting</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7b4bc-104">Denne opgave gennemgår en oversigt over de forudsætninger, der er nødvendige for EU-listesystem-rapportering.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-104">This task walks you through an overview of the prerequisites required for EU sales list reporting.</span></span> <span data-ttu-id="7b4bc-105">Du kan finde flere oplysninger om rapportering i EU-listesystemet, herunder de nødvendige forudsætninger, i Dynamics 365 for Finance and Operations Hjælp.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-105">For more information about EU Sales list reporting, including required prerequisites, refer to the Dynamics 365 for Finance and Operations Help.</span></span>

<span data-ttu-id="7b4bc-106">Denne opgave gælder for alle europæiske lande/områder.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-106">This task applies to all European countries/regions.</span></span> <span data-ttu-id="7b4bc-107">Guiden er oprettet ved hjælp af demodatafirmaet DEMF og bruger derfor Tyskland som et EU-land/områdeeksempel.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-107">The guide was created using the demo data company DEMF and consequently Germany as an exemplar domestic country/region.</span></span> <span data-ttu-id="7b4bc-108">Guiden bruger også Portugal som et EU-land/områdeeksempel.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-108">The guide also uses Portugal as an exemplar EU country/region.</span></span>

<span data-ttu-id="7b4bc-109">Disse opgaver er beregnet til systemadministratorer.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-109">These tasks are intended for system administrators.</span></span>


## <a name="import-electronic-reporting-configurations-for-eu-sales-list-reporting"></a><span data-ttu-id="7b4bc-110">Importer konfiguration for elektronisk rapportering for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="7b4bc-110">Import electronic reporting configurations for EU sales list reporting</span></span>
1. <span data-ttu-id="7b4bc-111">Gå til Virksomhedsadministration > Arbejdsområder > Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-111">Go to Organization administration > Workspaces > Electronic reporting.</span></span>
2. <span data-ttu-id="7b4bc-112">Klik på Angiv som aktiv.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-112">Click Set active.</span></span>
3. <span data-ttu-id="7b4bc-113">Klik på Lagre.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-113">Click Repositories.</span></span>
4. <span data-ttu-id="7b4bc-114">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-114">Click Open.</span></span>
5. <span data-ttu-id="7b4bc-115">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-115">On the Action Pane, click Options.</span></span>
6. <span data-ttu-id="7b4bc-116">Klik på Avanceret filtrering/sortering.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-116">Click Advanced Filter/Sort.</span></span>
7. <span data-ttu-id="7b4bc-117">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-117">Click Add.</span></span>
8. <span data-ttu-id="7b4bc-118">Vælg "Konfigurationsnavn" i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-118">In the Field field, select 'Configuration name'.</span></span>
9. <span data-ttu-id="7b4bc-119">Skriv '"EU-listesystem (DE)" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-119">In the Criteria field, type 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="7b4bc-120">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-120">Click OK.</span></span>
11. <span data-ttu-id="7b4bc-121">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-121">Click Import.</span></span>
12. <span data-ttu-id="7b4bc-122">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-122">Click Yes.</span></span>
13. <span data-ttu-id="7b4bc-123">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-123">On the Action Pane, click Options.</span></span>
14. <span data-ttu-id="7b4bc-124">Klik på Avanceret filtrering/sortering.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-124">Click Advanced Filter/Sort.</span></span>
15. <span data-ttu-id="7b4bc-125">Klik på Nulstil.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-125">Click Reset.</span></span>
16. <span data-ttu-id="7b4bc-126">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-126">Click Add.</span></span>
17. <span data-ttu-id="7b4bc-127">Vælg "Konfigurationsnavn" i feltet Felt.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-127">In the Field field, select 'Configuration name'.</span></span>
18. <span data-ttu-id="7b4bc-128">Skriv "EU-listesystemrapport efter rækker'" i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-128">In the Criteria field, type 'EU Sales list by rows report'.</span></span>
19. <span data-ttu-id="7b4bc-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-129">Click OK.</span></span>
20. <span data-ttu-id="7b4bc-130">Klik på Importer.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-130">Click Import.</span></span>
21. <span data-ttu-id="7b4bc-131">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-131">Click Yes.</span></span>

## <a name="set-up-sales-tax-codes-for-eu-sales-list-reporting"></a><span data-ttu-id="7b4bc-132">Opsætning af momskoder for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="7b4bc-132">Set up sales tax codes for EU sales list reporting</span></span>
1. <span data-ttu-id="7b4bc-133">Gå til Moms > Indirekte skatter > Moms > Momskoder.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-133">Go to Tax > Indirect taxes > Sales tax > Sales tax codes.</span></span>
2. <span data-ttu-id="7b4bc-134">Brug Quick Filter til at filtrere på feltet Momskode med værdien ''VAT19".</span><span class="sxs-lookup"><span data-stu-id="7b4bc-134">Use the Quick Filter to filter on the Sales tax code field with a value of 'VAT19'.</span></span>
3. <span data-ttu-id="7b4bc-135">Udvid sektionen Rapportopsætning.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-135">Expand the Report setup section.</span></span>
    * <span data-ttu-id="7b4bc-136">Kontroller, at sektionen Udelukket er angivet til Nej.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-136">Verify that the Excluded selection is set to No.</span></span>  
    * <span data-ttu-id="7b4bc-137">Du skal muligvis oplåse opgaveguiden for at ændre denne indstilling.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-137">You may need to unlock the task guide to change this setting.</span></span>  

## <a name="set-up-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="7b4bc-138">Opsætning af momsgrupper for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="7b4bc-138">Set up sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="7b4bc-139">Gå til Moms > Indirekte skatter > Moms > Momsgrupper.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-139">Go to Tax > Indirect taxes > Sales tax > Sales tax groups.</span></span>
2. <span data-ttu-id="7b4bc-140">Brug Quick Filter til at filtrere på feltet Momsgruppe med værdien ''AR-DOM".</span><span class="sxs-lookup"><span data-stu-id="7b4bc-140">Use the Quick Filter to filter on the Sales tax group field with a value of 'AR-DOM'.</span></span>
3. <span data-ttu-id="7b4bc-141">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-141">Click Edit.</span></span>
4. <span data-ttu-id="7b4bc-142">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-142">Expand the Setup section.</span></span>
5. <span data-ttu-id="7b4bc-143">Marker den første række på listen.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-143">In the list, select the first row.</span></span>
6. <span data-ttu-id="7b4bc-144">Marker afkrydsningsfeltet Momsfri.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-144">Select the Exempt check box.</span></span>
7. <span data-ttu-id="7b4bc-145">Marker den anden række på listen.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-145">In the list, select the second row.</span></span>
8. <span data-ttu-id="7b4bc-146">Marker afkrydsningsfeltet Momsfri.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-146">Select the Exempt check box.</span></span>
9. <span data-ttu-id="7b4bc-147">Marker den tredje række på listen.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-147">In the list, select the third row.</span></span>
10. <span data-ttu-id="7b4bc-148">Marker afkrydsningsfeltet Momsfri.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-148">Select the Exempt check box.</span></span>

## <a name="set-up-item-sales-tax-groups-for-eu-sales-list-reporting"></a><span data-ttu-id="7b4bc-149">Opsætning af varemomsgrupper for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="7b4bc-149">Set up item sales tax groups for EU sales list reporting</span></span>
1. <span data-ttu-id="7b4bc-150">Gå til Moms > Indirekte skatter > Moms > Momsgrupper.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-150">Go to Tax > Indirect taxes > Sales tax > Item sales tax groups.</span></span>
2. <span data-ttu-id="7b4bc-151">Brug Quick Filter til at filtrere på feltet Varemomsgruppe med værdien ''FULL".</span><span class="sxs-lookup"><span data-stu-id="7b4bc-151">Use the Quick Filter to filter on the Item sales tax group field with a value of 'FULL '.</span></span>
    * <span data-ttu-id="7b4bc-152">Kontroller, at Rapporteringstype er indstillet til "Vare".</span><span class="sxs-lookup"><span data-stu-id="7b4bc-152">Verify that the Reporting type selection is set to 'Item'.</span></span>  
    * <span data-ttu-id="7b4bc-153">Du skal muligvis oplåse opgaveguiden for at ændre værdien i dette felt.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-153">You may need to unlock the task guide to change the value in this field.</span></span>  
3. <span data-ttu-id="7b4bc-154">Brug Quick Filter til at filtrere på feltet Varemomsgruppe med værdien ''RED".</span><span class="sxs-lookup"><span data-stu-id="7b4bc-154">Use the Quick Filter to filter on the Item sales tax group field with a value of 'RED '.</span></span>
    * <span data-ttu-id="7b4bc-155">Kontroller, at Rapporteringstype er indstillet til "Service".</span><span class="sxs-lookup"><span data-stu-id="7b4bc-155">Verify that the Reporting type selection is set to 'Service'.</span></span>  
    * <span data-ttu-id="7b4bc-156">Du skal muligvis oplåse opgaveguiden for at ændre værdien i dette felt.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-156">You may need to unlock the task guide to change the value in this field.</span></span>  

## <a name="set-up-countryregion-parameters-for-eu-sales-list-reporting"></a><span data-ttu-id="7b4bc-157">Konfigurere parametre for land/område for rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="7b4bc-157">Set up country/region parameters for EU sales list reporting</span></span>
1. <span data-ttu-id="7b4bc-158">Gå til Skat > Opsætning > Moms > Land/områdeparametre.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-158">Go to Tax > Setup > Sales tax > Country/region parameters.</span></span>
2. <span data-ttu-id="7b4bc-159">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-159">Click New.</span></span>
3. <span data-ttu-id="7b4bc-160">Skriv "PRT" i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-160">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="7b4bc-161">Skriv 'PT' i feltet Moms.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-161">In the Sales tax field, type 'PT'.</span></span>

## <a name="create-tax-exempt-numbers"></a><span data-ttu-id="7b4bc-162">Oprette SE-numre</span><span class="sxs-lookup"><span data-stu-id="7b4bc-162">Create tax exempt numbers</span></span>
1. <span data-ttu-id="7b4bc-163">Gå til Skat > Opsætning > Moms > SE-numre.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-163">Go to Tax > Setup > Sales tax > Tax exempt numbers.</span></span>
2. <span data-ttu-id="7b4bc-164">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-164">Click New.</span></span>
3. <span data-ttu-id="7b4bc-165">Skriv "PRT" i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-165">In the Country/region field, type 'PRT'.</span></span>
4. <span data-ttu-id="7b4bc-166">Skriv "PT12345" i feltet SE-nummer.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-166">In the Tax exempt number field, type 'PT12345'.</span></span>

## <a name="set-up-eu-sales-list-reporting-parameters"></a><span data-ttu-id="7b4bc-167">Konfigurere parametre for rapportering for EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="7b4bc-167">Set up EU sales list reporting parameters</span></span>
1. <span data-ttu-id="7b4bc-168">Gå til Skat > Opsætning > Udenrigshandel > Udenrigshandelsparametre.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-168">Go to Tax > Setup > Foreign trade > Foreign trade parameters.</span></span>
2. <span data-ttu-id="7b4bc-169">Klik på fanen EU-listesystem.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-169">Click the EU sales list tab.</span></span>
3. <span data-ttu-id="7b4bc-170">Vælg Ja i feltet Overfør køb.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-170">Select Yes in the Transfer purchases field.</span></span>
4. <span data-ttu-id="7b4bc-171">Udvid sektionen Afrundingsregler.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-171">Expand the Rounding rules section.</span></span>
5. <span data-ttu-id="7b4bc-172">Indstil Afrundingsregel til "0.1".</span><span class="sxs-lookup"><span data-stu-id="7b4bc-172">Set Rounding rule to '0.1'.</span></span>
6. <span data-ttu-id="7b4bc-173">Vælg Ja i feltet Brug minimumværdi.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-173">Select Yes in the Use minimum value field.</span></span>
7. <span data-ttu-id="7b4bc-174">Skriv "2" i feltet Antal decimaler.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-174">In the Number of decimals field, enter '2'.</span></span>
8. <span data-ttu-id="7b4bc-175">Udvid sektionen Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-175">Expand the Electronic reporting section.</span></span>
9. <span data-ttu-id="7b4bc-176">Vælg "EU-listesystem (DE)" i feltet Filformattilknytning.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-176">In the File format mapping field, select 'EU Sales list (DE)'.</span></span>
10. <span data-ttu-id="7b4bc-177">Vælg "EU-listesystemrapport efter rækker" i feltet Filformattilknytning.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-177">In the Report format mapping field, select 'EU Sales list by rows report'.</span></span>
11. <span data-ttu-id="7b4bc-178">Klik på fanen Egenskaber for land/område.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-178">Click the Country/region properties tab.</span></span>
    * <span data-ttu-id="7b4bc-179">Kontroller, at feltet Lande-/områdetype er angivet til "Indland" for landet/området DEU.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-179">Verify that the Country/region type field is set to 'Domestic' for Country/region DEU.</span></span>  
    * <span data-ttu-id="7b4bc-180">Du skal muligvis oplåse opgaveguiden for at ændre værdien i dette felt.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-180">You may need to unlock the task guide to change the value in this field.</span></span>  
12. <span data-ttu-id="7b4bc-181">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-181">Click New.</span></span>
13. <span data-ttu-id="7b4bc-182">Skriv "PRT" i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-182">In the Country/region field, type 'PRT'.</span></span>
14. <span data-ttu-id="7b4bc-183">Skriv 'PT' i feltet Intrastat-kode.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-183">In the Intrastat code field, type 'PT'.</span></span>
15. <span data-ttu-id="7b4bc-184">Vælg "EU" i feltet Lande-/områdetype.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-184">In the Country/region type field, select 'EU'.</span></span>
16. <span data-ttu-id="7b4bc-185">Klik på fanen Nummerserier.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-185">Click the Number sequences tab.</span></span>
    * <span data-ttu-id="7b4bc-186">Kontroller, at der er angivet en nummerseriekode for referencen "EU-listesystem".</span><span class="sxs-lookup"><span data-stu-id="7b4bc-186">Verify that a Number sequence code is specified for the Reference 'EU sales list'.</span></span>  

## <a name="create-a-customer-for-eu-sales-list-reporting-demo-purposes"></a><span data-ttu-id="7b4bc-187">Oprette en kunde med henblik på demonstration af EU-rapportering til EU-listesystemet</span><span class="sxs-lookup"><span data-stu-id="7b4bc-187">Create a customer for EU sales list reporting demo purposes</span></span>
1. <span data-ttu-id="7b4bc-188">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-188">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="7b4bc-189">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-189">Click New.</span></span>
3. <span data-ttu-id="7b4bc-190">Skriv "PRT-001" i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-190">In the Customer account field, type 'PRT-001'.</span></span>
4. <span data-ttu-id="7b4bc-191">Skriv 'En kunde fra Portugal' i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-191">In the Name field, type 'A customer from Portugal'.</span></span>
5. <span data-ttu-id="7b4bc-192">Vælg "10" i feltet Kundegruppe.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-192">In the Customer group field, select '10'.</span></span>
6. <span data-ttu-id="7b4bc-193">Vælg "AR-DOM" i feltet Momsgruppe.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-193">In the Sales tax group field, select 'AR-DOM'.</span></span>
7. <span data-ttu-id="7b4bc-194">Vælg "PT12345" i feltet SE-nummer.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-194">In the Tax exempt number field, select 'PT12345'.</span></span>
8. <span data-ttu-id="7b4bc-195">Skriv "PRT" i feltet Land/område.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-195">In the Country/region field, type 'PRT'.</span></span>
9. <span data-ttu-id="7b4bc-196">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7b4bc-196">Click Save.</span></span>


