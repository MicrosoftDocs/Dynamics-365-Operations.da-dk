---
title: "Konfigurere forudsætninger for administration"
description: Brug denne procedure til at aktivere processer for styring af uoverensstemmelser.
author: perlynne
manager: AnnBe
ms.date: 11/02/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: 5f8499f53c785170fa1ec13b0a34a306ac6c45b5
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---
# <a name="set-up-prerequisites-for-management"></a><span data-ttu-id="819c2-103">Konfigurere forudsætninger for administration</span><span class="sxs-lookup"><span data-stu-id="819c2-103">Set up prerequisites for management</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="819c2-104">Brug denne procedure til at aktivere processer for styring af uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="819c2-104">Use this procedure to enable nonconformance management processes.</span></span> <span data-ttu-id="819c2-105">En uoverensstemmelse er en procedure eller vare, der har et kvalitetsproblem, hvor de beskrivende oplysninger omfatter årsagen til og typen af problemet.</span><span class="sxs-lookup"><span data-stu-id="819c2-105">A nonconformance describes a procedure or item that has a quality problem, where the descriptive information includes the source and type of problem.</span></span> <span data-ttu-id="819c2-106">Proceduren bruger USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="819c2-106">This procedure uses the USMF demo data company.</span></span> <span data-ttu-id="819c2-107">Denne procedure udføres typisk af en kvalitetschef.</span><span class="sxs-lookup"><span data-stu-id="819c2-107">This procedure is typically performed by a quality manager.</span></span>


## <a name="enable-quality-management-processes-within-the-company"></a><span data-ttu-id="819c2-108">Aktivere kvalitetsstyringsprocesser i virksomheden</span><span class="sxs-lookup"><span data-stu-id="819c2-108">Enable quality management processes within the company</span></span>
1. <span data-ttu-id="819c2-109">Gå til lagerstyring > Opsætning > Parametre til lager- og lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="819c2-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="819c2-110">Klik på fanen Kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="819c2-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="819c2-111">Vælg Ja i feltet Brug kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="819c2-111">Select Yes in the Use quality management field.</span></span>
    * <span data-ttu-id="819c2-112">Vælg denne parameter for at aktivere kvalitetsstyringsprocesser for virksomheden.</span><span class="sxs-lookup"><span data-stu-id="819c2-112">Select this parameter to enable quality management processes for the company.</span></span>  
4. <span data-ttu-id="819c2-113">Angiv et tal i feltet Timepris.</span><span class="sxs-lookup"><span data-stu-id="819c2-113">In the Hourly rate field, enter a number.</span></span>
    * <span data-ttu-id="819c2-114">Brug feltet Timepris til at angive en timepris for arbejdet i den lokale valuta.</span><span class="sxs-lookup"><span data-stu-id="819c2-114">Use the Hourly rate field to enter an hourly labor rate in the local currency.</span></span> <span data-ttu-id="819c2-115">Timeprisen bruges til beregning af omkostningerne for operationer, der vedrører en uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="819c2-115">The hourly rate is used for calculating costs for operations that are related to a nonconformance.</span></span> <span data-ttu-id="819c2-116">Timeprisen og de beregnede omkostninger er referenceoplysninger for en uoverensstemmelse, og de påvirker ikke andre funktioner.</span><span class="sxs-lookup"><span data-stu-id="819c2-116">The hourly rate and calculated costs provide reference information for a nonconformance, and they do not interact with other functionality.</span></span>  
5. <span data-ttu-id="819c2-117">Klik på Rapportopsætning.</span><span class="sxs-lookup"><span data-stu-id="819c2-117">Click Report setup.</span></span>
    * <span data-ttu-id="819c2-118">På denne siden kan du definere notetyper for kvalitetsrapporter, der skal bruges til forskellige typer rapporter over kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="819c2-118">This page allows you to define the quality report note types that will be used on different kinds of quality management reports.</span></span>  
6. <span data-ttu-id="819c2-119">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-119">Close the page.</span></span>
7. <span data-ttu-id="819c2-120">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-120">Close the page.</span></span>

## <a name="enable-user-for-nonconformance-processing"></a><span data-ttu-id="819c2-121">Aktivere bruger til håndtering af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="819c2-121">Enable user for nonconformance processing</span></span>
1. <span data-ttu-id="819c2-122">Gå til Systemadministration > Brugere > Brugere.</span><span class="sxs-lookup"><span data-stu-id="819c2-122">Go to System administration > Users > Users.</span></span>
    * <span data-ttu-id="819c2-123">For at behandle godkendelsen af en uoverensstemmelse skal den bruger, der godkender eller afviser uoverensstemmelser, have en "Navn"-værdi tildelt på siden Brugere.</span><span class="sxs-lookup"><span data-stu-id="819c2-123">To process the approval of a nonconformance the user who  approves or rejects nonconformances must have a “Name” value assigned on the Users page.</span></span> <span data-ttu-id="819c2-124">For at kunne bruge dokumentnoter skal brugeren også have Dokumenthåndtering aktiveret i brugerindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="819c2-124">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
2. <span data-ttu-id="819c2-125">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="819c2-125">Use the Quick Filter to find records.</span></span> <span data-ttu-id="819c2-126">For eksempel kan du filtrere på feltet Navn med værdien 'Ricardo'.</span><span class="sxs-lookup"><span data-stu-id="819c2-126">For example, filter on the Name field with a value of 'Ricardo'.</span></span>
    * <span data-ttu-id="819c2-127">Du kan bruge filteret til at finde den bruger, der skal godkende eller afvise uoverensstemmelsesposter.</span><span class="sxs-lookup"><span data-stu-id="819c2-127">Use the filter to find the user who will be approving or rejecting the nonconformance records.</span></span>  
3. <span data-ttu-id="819c2-128">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="819c2-128">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="819c2-129">For at behandle godkendelsen af en uoverensstemmelse skal du sørge for, at den bruger, der godkender eller afviser uoverensstemmelser, har en "Navn"-værdi tildelt på siden Brugere.</span><span class="sxs-lookup"><span data-stu-id="819c2-129">To process the approval of a nonconformance, make sure the user who approves or rejects nonconformances has a “Name” value assigned on the Users page.</span></span>  
4. <span data-ttu-id="819c2-130">Klik på Brugerindstillinger.</span><span class="sxs-lookup"><span data-stu-id="819c2-130">Click User options.</span></span>
5. <span data-ttu-id="819c2-131">Klik på fanen Præferencer.</span><span class="sxs-lookup"><span data-stu-id="819c2-131">Click the Preferences tab.</span></span>
6. <span data-ttu-id="819c2-132">Vælg Ja i feltet Aktivér dokumenthåndtering.</span><span class="sxs-lookup"><span data-stu-id="819c2-132">Select Yes in the Enable document handling field.</span></span>
    * <span data-ttu-id="819c2-133">For at kunne bruge dokumentnoter skal brugeren også have Dokumenthåndtering aktiveret i brugerindstillingerne.</span><span class="sxs-lookup"><span data-stu-id="819c2-133">To use the document notes, the user must also have Document handling activated in the user options.</span></span>  
7. <span data-ttu-id="819c2-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-134">Close the page.</span></span>
8. <span data-ttu-id="819c2-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-135">Close the page.</span></span>
9. <span data-ttu-id="819c2-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-136">Close the page.</span></span>

## <a name="define-diagnostic-types-for-nonconformance-processing"></a><span data-ttu-id="819c2-137">Definere diagnosticeringstyper for håndtering af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="819c2-137">Define diagnostic types for nonconformance processing</span></span>
1. <span data-ttu-id="819c2-138">Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Diagnosticeringstyper.</span><span class="sxs-lookup"><span data-stu-id="819c2-138">Go to Inventory management > Setup > Quality management > Diagnostic types.</span></span>
    * <span data-ttu-id="819c2-139">Brug siden Diagnosticeringstyper til definere en klassifikation af diagnosticeringshandlinger.</span><span class="sxs-lookup"><span data-stu-id="819c2-139">Use the Diagnostic types page to define a classification of diagnostic actions.</span></span> <span data-ttu-id="819c2-140">En rettelse angiver, hvilken type diagnosticeringshandling, der skal udføres for en godkendt uoverensstemmelse, hvem der skal udføre den og den ønskede og planlagte fuldførelsesdato.</span><span class="sxs-lookup"><span data-stu-id="819c2-140">A correction identifies what type of diagnostic action should be taken on an approved nonconformance, who should perform it, and the requested and planned completion date.</span></span>  
2. <span data-ttu-id="819c2-141">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="819c2-141">Click New.</span></span>
3. <span data-ttu-id="819c2-142">Skriv en værdi i feltet Diagnosticering.</span><span class="sxs-lookup"><span data-stu-id="819c2-142">In the Diagnostic field, type a value.</span></span>
4. <span data-ttu-id="819c2-143">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="819c2-143">In the Description field, type a value.</span></span>
5. <span data-ttu-id="819c2-144">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-144">Close the page.</span></span>

## <a name="define-quality-charges-for-nonconformance-processing"></a><span data-ttu-id="819c2-145">Definere kvalitetsgebyrer for håndtering af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="819c2-145">Define quality charges for nonconformance processing</span></span>
1. <span data-ttu-id="819c2-146">Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Kvalitetsgebyrer.</span><span class="sxs-lookup"><span data-stu-id="819c2-146">Go to Inventory management > Setup > Quality management > Quality charges.</span></span>
    * <span data-ttu-id="819c2-147">Brug siden Kvalitetsgebyrer til at definere en klassifikation af gebyrer, der skal bruges i handlinger, der vedrører uoverensstemmelser.</span><span class="sxs-lookup"><span data-stu-id="819c2-147">Use the Quality charges page to define a classification of charges that will used in operations related to nonconformances.</span></span>  
2. <span data-ttu-id="819c2-148">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="819c2-148">Click New.</span></span>
3. <span data-ttu-id="819c2-149">Skriv en værdi i feltet Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="819c2-149">In the Charges code field, type a value.</span></span>
4. <span data-ttu-id="819c2-150">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="819c2-150">In the Description field, type a value.</span></span>
5. <span data-ttu-id="819c2-151">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-151">Close the page.</span></span>

## <a name="define-the-operations-for-nonconformance-processing"></a><span data-ttu-id="819c2-152">Definere handlinger for håndtering af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="819c2-152">Define the operations for nonconformance processing</span></span>
1. <span data-ttu-id="819c2-153">Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Handlinger.</span><span class="sxs-lookup"><span data-stu-id="819c2-153">Go to Inventory management > Setup > Quality management > Operations.</span></span>
    * <span data-ttu-id="819c2-154">Brug siden Handlinger til at definere en klassifikation af det arbejde, der kan blive udført for en godkendt uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="819c2-154">Use the Operations page to define a classification of the work that may be performed for an approved nonconformance.</span></span> <span data-ttu-id="819c2-155">Når du relaterer en handling til en uoverensstemmelse, kan du også definere detaljerede oplysninger om det tilknyttede materiale, arbejdstimer og tillæg, der kræves for at udføre handlingen.</span><span class="sxs-lookup"><span data-stu-id="819c2-155">When you relate an operation to a nonconformance, you can define information about the associated material, labor hours, and miscellaneous charges that are required to perform the operation.</span></span> <span data-ttu-id="819c2-156">Disse oplysninger danner grundlaget for beregning af en forkalkuleret omkostning for udførelsen af handlingen.</span><span class="sxs-lookup"><span data-stu-id="819c2-156">This information provides the basis for calculating an estimated cost for performing the operation.</span></span>  
2. <span data-ttu-id="819c2-157">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="819c2-157">Click New.</span></span>
3. <span data-ttu-id="819c2-158">Skriv en værdi i feltet Handling.</span><span class="sxs-lookup"><span data-stu-id="819c2-158">In the Operation field, type a value.</span></span>
4. <span data-ttu-id="819c2-159">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="819c2-159">In the Description field, type a value.</span></span>
5. <span data-ttu-id="819c2-160">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-160">Close the page.</span></span>

## <a name="define-problem-types-for-nonconformance-processing"></a><span data-ttu-id="819c2-161">Definere problemtyper for håndtering af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="819c2-161">Define problem types for nonconformance processing</span></span>
1. <span data-ttu-id="819c2-162">Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Problemtyper.</span><span class="sxs-lookup"><span data-stu-id="819c2-162">Go to Inventory management > Setup > Quality management > Problem types.</span></span>
    * <span data-ttu-id="819c2-163">Brug siden Problemtyper til at definere en klassifikation for de kvalitetsproblemer, der kan forekomme for de forskellige uoverensstemmelsestyper.</span><span class="sxs-lookup"><span data-stu-id="819c2-163">Use the Problem types page to define a classification of quality problems that are encountered in the various nonconformance types.</span></span> <span data-ttu-id="819c2-164">Uoverensstemmelsestyperne omfatter Intern, Debitor, Kreditor, Serviceanmodning, Produktion og Produktion af samprodukter.</span><span class="sxs-lookup"><span data-stu-id="819c2-164">The nonconformance types include Internal, Customer, Vendor, Service request, Production, and Co-product production.</span></span> <span data-ttu-id="819c2-165">En enkelt problemtype kan tilknyttes flere uoverensstemmelsestyper.</span><span class="sxs-lookup"><span data-stu-id="819c2-165">A single problem type can be associated with multiple nonconformance types.</span></span>  
2. <span data-ttu-id="819c2-166">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="819c2-166">Click New.</span></span>
3. <span data-ttu-id="819c2-167">Skriv en værdi i feltet Problem.</span><span class="sxs-lookup"><span data-stu-id="819c2-167">In the Problem type field, type a value.</span></span>
4. <span data-ttu-id="819c2-168">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="819c2-168">In the Description field, type a value.</span></span>
5. <span data-ttu-id="819c2-169">Klik på Uoverensstemmelsestyper.</span><span class="sxs-lookup"><span data-stu-id="819c2-169">Click Non conformance types.</span></span>
    * <span data-ttu-id="819c2-170">Brug siden Uoverensstemmelsestyper til at autorisere brugen af en problemtype til en eller flere uoverensstemmelsestyper.</span><span class="sxs-lookup"><span data-stu-id="819c2-170">Use the Non conformance types page to authorize the use of a problem type for one or more of the nonconformance types.</span></span> <span data-ttu-id="819c2-171">En problemtype vedrørende en defektkode kunne f.eks. gælde for alle uoverensstemmelsestyper, mens en problemtype for kundeklager måske kun gælder for uoverensstemmelsestyperne Debitor eller Serviceanmodning.</span><span class="sxs-lookup"><span data-stu-id="819c2-171">For example, a problem type regarding a defect code could apply to all nonconformance types, whereas a problem type about customer complaints may only apply to the customer and service request nonconformance types.</span></span>  
6. <span data-ttu-id="819c2-172">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="819c2-172">Click New.</span></span>
7. <span data-ttu-id="819c2-173">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="819c2-173">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="819c2-174">Vælg en indstilling i feltet Uoverensstemmelse.</span><span class="sxs-lookup"><span data-stu-id="819c2-174">In the Non conformance type field, select an option.</span></span>
9. <span data-ttu-id="819c2-175">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-175">Close the page.</span></span>
10. <span data-ttu-id="819c2-176">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-176">Close the page.</span></span>

## <a name="define-quarantine-zones-for-nonconformance-processing"></a><span data-ttu-id="819c2-177">Definere karantænezoner for håndtering af uoverensstemmelser</span><span class="sxs-lookup"><span data-stu-id="819c2-177">Define quarantine zones for nonconformance processing</span></span>
1. <span data-ttu-id="819c2-178">Gå til Lagerstyring > Konfiguration > Kvalitetsstyring > Karantænezoner.</span><span class="sxs-lookup"><span data-stu-id="819c2-178">Go to Inventory management > Setup > Quality management > Quarantine zones.</span></span>
2. <span data-ttu-id="819c2-179">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="819c2-179">Click New.</span></span>
3. <span data-ttu-id="819c2-180">Skriv en værdi i feltet Karantænezone.</span><span class="sxs-lookup"><span data-stu-id="819c2-180">In the Quarantine zone field, type a value.</span></span>
4. <span data-ttu-id="819c2-181">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="819c2-181">In the Description field, type a value.</span></span>
5. <span data-ttu-id="819c2-182">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="819c2-182">Close the page.</span></span>

