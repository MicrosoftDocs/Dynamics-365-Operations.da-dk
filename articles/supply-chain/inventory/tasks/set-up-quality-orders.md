---
title: Konfigurere kvalitetsordrer
description: Denne fremgangsmåde viser, hvordan du aktiverer en proces til kvalitetsstyring, hvor indgående lager skal undersøges umiddelbart efter modtagelsesregistrering.
author: perlynne
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventParameters, InventTestReportSetup, InventTestTable, DefaultDashboard, InventTestVariable, InventTestVariableOutcome, InventItemSampling, InventTestQualityGroup, InventTestItemQualityGroupAdd, SysQueryForm, InventTestItemQualityGroup, InventTestGroup, InventTestAssociationTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.search.industry: Distribution
ms.author: perlynne
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5a073de7bdfd2ef597c09a8066ff2b6a7721ca62
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "356984"
---
# <a name="set-up-quality-orders"></a><span data-ttu-id="277dc-103">Konfigurere kvalitetsordrer</span><span class="sxs-lookup"><span data-stu-id="277dc-103">Set up quality orders</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="277dc-104">Denne fremgangsmåde viser, hvordan du aktiverer en proces til kvalitetsstyring, hvor indgående lager skal undersøges umiddelbart efter modtagelsesregistrering.</span><span class="sxs-lookup"><span data-stu-id="277dc-104">This procedure shows you how to enable a quality management process where incoming inventory must be inspected immediately after arrival registration.</span></span> <span data-ttu-id="277dc-105">Proceduren udføres normalt af en kvalitetschef.</span><span class="sxs-lookup"><span data-stu-id="277dc-105">The procedure will typically be carried out by a quality manager.</span></span> <span data-ttu-id="277dc-106">Processen omfatter oprettelse af en kvalitetsgruppe til at definere de varer, der skal udtages, og en testgruppe til at gruppere de test, der skal udføres på varer i kvalitetsgruppen.</span><span class="sxs-lookup"><span data-stu-id="277dc-106">The process includes the creation of a quality group, to define the items that are going to be sampled, and a test group to group the tests that are to be performed on items in the quality group.</span></span> <span data-ttu-id="277dc-107">Du kan køre denne guide i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="277dc-107">You can run this guide in the USMF demo data company.</span></span>


## <a name="enable-quality-management"></a><span data-ttu-id="277dc-108">Aktivere kvalitetsstyring</span><span class="sxs-lookup"><span data-stu-id="277dc-108">Enable quality management</span></span>
1. <span data-ttu-id="277dc-109">Gå til lagerstyring > Opsætning > Parametre til lager- og lagerstedsstyring.</span><span class="sxs-lookup"><span data-stu-id="277dc-109">Go to Inventory management > Setup > Inventory and warehouse management parameters.</span></span>
2. <span data-ttu-id="277dc-110">Klik på fanen Kvalitetsstyring.</span><span class="sxs-lookup"><span data-stu-id="277dc-110">Click the Quality management tab.</span></span>
3. <span data-ttu-id="277dc-111">Angiv indstillingen Brug kvalitetsstyring til Ja.</span><span class="sxs-lookup"><span data-stu-id="277dc-111">Set the Use quality management option to Yes.</span></span>
4. <span data-ttu-id="277dc-112">Klik på Rapportopsætning.</span><span class="sxs-lookup"><span data-stu-id="277dc-112">Click Report setup.</span></span>
    * <span data-ttu-id="277dc-113">Rapportopsætning til kvalitetsstyring er allerede defineret i USMF.</span><span class="sxs-lookup"><span data-stu-id="277dc-113">In USMF, the report setup for quality management is already defined.</span></span> <span data-ttu-id="277dc-114">Hvis dette ikke var gjort, skulle du tilføje nye linjer her for de forskellige rapporttyper og vælge typen af dokument, der skal bruges til hver rapport.</span><span class="sxs-lookup"><span data-stu-id="277dc-114">If this wasn’t done, you’d add new lines here for the different report types, and select the type of document to be used for each report.</span></span>  
5. <span data-ttu-id="277dc-115">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-115">Close the page.</span></span>
6. <span data-ttu-id="277dc-116">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-116">Close the page.</span></span>

## <a name="create-a-test"></a><span data-ttu-id="277dc-117">Oprette en test</span><span class="sxs-lookup"><span data-stu-id="277dc-117">Create a test</span></span>
1. <span data-ttu-id="277dc-118">Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Test.</span><span class="sxs-lookup"><span data-stu-id="277dc-118">Go to Inventory management > Setup > Quality control > Tests.</span></span>
2. <span data-ttu-id="277dc-119">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="277dc-119">Click New.</span></span>
3. <span data-ttu-id="277dc-120">Skriv en værdi i feltet Test.</span><span class="sxs-lookup"><span data-stu-id="277dc-120">In the Test field, type a value.</span></span>
4. <span data-ttu-id="277dc-121">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="277dc-121">In the Description field, type a value.</span></span>
5. <span data-ttu-id="277dc-122">Vælg "Indstilling" i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="277dc-122">In the Type field, select 'Option'.</span></span>
    * <span data-ttu-id="277dc-123">I dette eksempel vil vi vælge "Indstilling", som gør det muligt at tildele testresultaterne, der er baseret på foruddefinerede værdier.</span><span class="sxs-lookup"><span data-stu-id="277dc-123">In this example, we'll select "Option" which will make it possible to assign the test results based on pre-defined values.</span></span>  
6. <span data-ttu-id="277dc-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="277dc-124">Click Save.</span></span>
7. <span data-ttu-id="277dc-125">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-125">Close the page.</span></span>

## <a name="create-test-variables-to-define-the-way-test-results-are-recorded"></a><span data-ttu-id="277dc-126">Opret testvariabler for at definere, hvordan testresultaterne registreres</span><span class="sxs-lookup"><span data-stu-id="277dc-126">Create Test variables to define the way test results are recorded</span></span>
1. <span data-ttu-id="277dc-127">Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Testvariabler.</span><span class="sxs-lookup"><span data-stu-id="277dc-127">Go to Inventory management > Setup > Quality control > Test variables.</span></span>
2. <span data-ttu-id="277dc-128">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="277dc-128">Click New.</span></span>
3. <span data-ttu-id="277dc-129">Skriv en værdi i feltet Variabel.</span><span class="sxs-lookup"><span data-stu-id="277dc-129">In the Variable field, type a value.</span></span>
4. <span data-ttu-id="277dc-130">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="277dc-130">In the Description field, type a value.</span></span>
5. <span data-ttu-id="277dc-131">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="277dc-131">Click Save.</span></span>
6. <span data-ttu-id="277dc-132">Klik på Udfald.</span><span class="sxs-lookup"><span data-stu-id="277dc-132">Click Outcomes.</span></span>
7. <span data-ttu-id="277dc-133">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="277dc-133">Click New.</span></span>
8. <span data-ttu-id="277dc-134">Skriv en værdi i feltet Udfald.</span><span class="sxs-lookup"><span data-stu-id="277dc-134">In the Outcome field, type a value.</span></span>
9. <span data-ttu-id="277dc-135">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="277dc-135">In the Description field, type a value.</span></span>
10. <span data-ttu-id="277dc-136">Vælg "Bestået" i feltet Status for udfald.</span><span class="sxs-lookup"><span data-stu-id="277dc-136">In the Outcome status field, select 'Pass'.</span></span>
11. <span data-ttu-id="277dc-137">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="277dc-137">Click Save.</span></span>
12. <span data-ttu-id="277dc-138">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="277dc-138">Click New.</span></span>
13. <span data-ttu-id="277dc-139">Skriv en værdi i feltet Udfald.</span><span class="sxs-lookup"><span data-stu-id="277dc-139">In the Outcome field, type a value.</span></span>
14. <span data-ttu-id="277dc-140">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="277dc-140">In the Description field, type a value.</span></span>
15. <span data-ttu-id="277dc-141">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="277dc-141">Click Save.</span></span>
16. <span data-ttu-id="277dc-142">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-142">Close the page.</span></span>
17. <span data-ttu-id="277dc-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-143">Close the page.</span></span>

## <a name="set-up-item-sampling"></a><span data-ttu-id="277dc-144">Konfigurer vareprøve</span><span class="sxs-lookup"><span data-stu-id="277dc-144">Set up item sampling</span></span>
1. <span data-ttu-id="277dc-145">Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Vareprøve.</span><span class="sxs-lookup"><span data-stu-id="277dc-145">Go to Inventory management > Setup > Quality control > Item sampling.</span></span>
2. <span data-ttu-id="277dc-146">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="277dc-146">Click New.</span></span>
3. <span data-ttu-id="277dc-147">Indtast en værdi i feltet Vareprøve.</span><span class="sxs-lookup"><span data-stu-id="277dc-147">In the Item sampling field, type a value.</span></span>
4. <span data-ttu-id="277dc-148">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="277dc-148">In the Description field, type a value.</span></span>
5. <span data-ttu-id="277dc-149">Angiv et tal i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="277dc-149">In the Value field, enter a number.</span></span>
    * <span data-ttu-id="277dc-150">Denne værdi, der er relateret til den angivelse af antal, der er valgt i det tilstødende felt.</span><span class="sxs-lookup"><span data-stu-id="277dc-150">This value relates to the Quantity specification that’s selected in the adjacent field.</span></span>  
6. <span data-ttu-id="277dc-151">Udvid eller skjul sektionen Proces.</span><span class="sxs-lookup"><span data-stu-id="277dc-151">Expand or collapse the Process section.</span></span>
7. <span data-ttu-id="277dc-152">Marker eller fjern markeringen i afkrydsningsfeltet Fuld spærring.</span><span class="sxs-lookup"><span data-stu-id="277dc-152">Select or clear the Full blocking check box.</span></span>
    * <span data-ttu-id="277dc-153">Hvis du vælger denne indstilling, blokeres hele partiet eller ordrelinjeantallet, hvis en test mislykkes.</span><span class="sxs-lookup"><span data-stu-id="277dc-153">If you select this option, the whole lot or order line quantity is blocked if a test is failed.</span></span> <span data-ttu-id="277dc-154">Hvis du ikke vælger den, blokeres kun varerne i kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="277dc-154">If you don't select it, only the items in the quality order are blocked.</span></span>  
8. <span data-ttu-id="277dc-155">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="277dc-155">Click Save.</span></span>
9. <span data-ttu-id="277dc-156">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-156">Close the page.</span></span>

## <a name="create-a-quality-group"></a><span data-ttu-id="277dc-157">Oprette en kvalitetsgruppe</span><span class="sxs-lookup"><span data-stu-id="277dc-157">Create a quality group</span></span>
1. <span data-ttu-id="277dc-158">Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Kvalitetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="277dc-158">Go to Inventory management > Setup > Quality control > Quality groups.</span></span>
2. <span data-ttu-id="277dc-159">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="277dc-159">Click New.</span></span>
3. <span data-ttu-id="277dc-160">Indtast en værdi i feltet Kvalitetsgruppe.</span><span class="sxs-lookup"><span data-stu-id="277dc-160">In the Quality group field, type a value.</span></span>
    * <span data-ttu-id="277dc-161">Brug et beskrivende navn for at identificere, hvilken form for varer gruppen indeholder (prøvekriterier).</span><span class="sxs-lookup"><span data-stu-id="277dc-161">Use a descriptive name to help you identify which kind of items the group will contain (your sampling criteria).</span></span>  
4. <span data-ttu-id="277dc-162">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="277dc-162">In the Description field, type a value.</span></span>
5. <span data-ttu-id="277dc-163">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="277dc-163">Click Save.</span></span>
6. <span data-ttu-id="277dc-164">Klik på Tilføj varer.</span><span class="sxs-lookup"><span data-stu-id="277dc-164">Click Add items.</span></span>
7. <span data-ttu-id="277dc-165">Vælg varenummerrækken</span><span class="sxs-lookup"><span data-stu-id="277dc-165">Select the Item number row</span></span>
    * <span data-ttu-id="277dc-166">I dette eksempel vil filtrering blive kørt baseret på varenummeret.</span><span class="sxs-lookup"><span data-stu-id="277dc-166">In this example the filtering will be run based on  the item number.</span></span>  
8. <span data-ttu-id="277dc-167">Skriv en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="277dc-167">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="277dc-168">Skriv f.eks. T\* for at filtrere på de varenumre, der begynder med T.</span><span class="sxs-lookup"><span data-stu-id="277dc-168">For example, type T\* to filter on the item numbers that start with T.</span></span>  
9. <span data-ttu-id="277dc-169">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="277dc-169">Click OK.</span></span>
10. <span data-ttu-id="277dc-170">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="277dc-170">Click OK.</span></span>
11. <span data-ttu-id="277dc-171">Klik på Varekvalitetsgrupper.</span><span class="sxs-lookup"><span data-stu-id="277dc-171">Click Item quality groups.</span></span>
12. <span data-ttu-id="277dc-172">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-172">Close the page.</span></span>
13. <span data-ttu-id="277dc-173">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-173">Close the page.</span></span>

## <a name="create-a-test-group"></a><span data-ttu-id="277dc-174">Oprette en testgruppe</span><span class="sxs-lookup"><span data-stu-id="277dc-174">Create a test group</span></span>
1. <span data-ttu-id="277dc-175">Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Testgrupper.</span><span class="sxs-lookup"><span data-stu-id="277dc-175">Go to Inventory management > Setup > Quality control > Test groups.</span></span>
2. <span data-ttu-id="277dc-176">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="277dc-176">Click New.</span></span>
3. <span data-ttu-id="277dc-177">Indtast en værdi i feltet Testgruppe.</span><span class="sxs-lookup"><span data-stu-id="277dc-177">In the Test group field, type a value.</span></span>
    * <span data-ttu-id="277dc-178">Giv testgruppen et navn, der hjælper dig med at huske, hvilken slags test udføres, og hvilken kvalitetsgruppe den skal knyttes til.</span><span class="sxs-lookup"><span data-stu-id="277dc-178">Give the Test group a name that will help you remember what kind of tests are being run, and which quality group it should be associated with.</span></span> <span data-ttu-id="277dc-179">For eksempel hvis skal den bruges med en kvalitetsgruppe, der vælger elementer, der starter med "T", kan du kalde den "T-elementtest".</span><span class="sxs-lookup"><span data-stu-id="277dc-179">For example, it it’s to be used with a quality group that selects items starting with “T”, you could call it “T-item tests”.</span></span>  
4. <span data-ttu-id="277dc-180">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="277dc-180">In the Description field, type a value.</span></span>
5. <span data-ttu-id="277dc-181">Vælg den vareprøvelinje, du oprettede før, i feltet Vareprøve.</span><span class="sxs-lookup"><span data-stu-id="277dc-181">In the Item sampling field, select the item sampling line that you created before.</span></span>
6. <span data-ttu-id="277dc-182">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="277dc-182">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="277dc-183">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="277dc-183">Click Add.</span></span>
8. <span data-ttu-id="277dc-184">Indtast et tal i feltet Sekvensnummer.</span><span class="sxs-lookup"><span data-stu-id="277dc-184">In the Sequence number field, enter a number.</span></span>
9. <span data-ttu-id="277dc-185">Vælg den test, som du oprettede tidligere, i feltet Test.</span><span class="sxs-lookup"><span data-stu-id="277dc-185">In the Test field, select the test that you created earlier.</span></span>
10. <span data-ttu-id="277dc-186">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="277dc-186">In the list, find and select the desired record.</span></span>
11. <span data-ttu-id="277dc-187">Klik på fanen Test.</span><span class="sxs-lookup"><span data-stu-id="277dc-187">Click the Test tab.</span></span>
12. <span data-ttu-id="277dc-188">Vælg den testvariabel, som du oprettede før, i feltet Variabel</span><span class="sxs-lookup"><span data-stu-id="277dc-188">In the Variable field, select the test variable that you created before</span></span>
13. <span data-ttu-id="277dc-189">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="277dc-189">In the list, find and select the desired record.</span></span>
14. <span data-ttu-id="277dc-190">Klik på rullelisten i feltet Standardudfald for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="277dc-190">In the Default outcome field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="277dc-191">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="277dc-191">In the list, click the link in the selected row.</span></span>
16. <span data-ttu-id="277dc-192">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="277dc-192">Click Save.</span></span>
17. <span data-ttu-id="277dc-193">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-193">Close the page.</span></span>

## <a name="define-when-quality-orders-will-be-created"></a><span data-ttu-id="277dc-194">Definere, hvornår der oprettes kvalitetsordrer</span><span class="sxs-lookup"><span data-stu-id="277dc-194">Define when quality orders will be created</span></span>
1. <span data-ttu-id="277dc-195">Gå til Lagerstyring > Opsætning > Kvalitetskontrol > Kvalitetstilknytninger.</span><span class="sxs-lookup"><span data-stu-id="277dc-195">Go to Inventory management > Setup > Quality control > Quality associations.</span></span>
2. <span data-ttu-id="277dc-196">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="277dc-196">Click New.</span></span>
3. <span data-ttu-id="277dc-197">Vælg en indstilling i feltet Referencetype.</span><span class="sxs-lookup"><span data-stu-id="277dc-197">In the Reference type field, select an option.</span></span>
4. <span data-ttu-id="277dc-198">Vælg "Gruppe" i feltet Varekode:</span><span class="sxs-lookup"><span data-stu-id="277dc-198">In the Item code field, select 'Group'.</span></span>
    * <span data-ttu-id="277dc-199">I dette eksempel vælger vi "Gruppe" og bruger den kvalitetsgruppe, vi oprettede før.</span><span class="sxs-lookup"><span data-stu-id="277dc-199">In this example, we’ll select "Group" and use the quality group we created before.</span></span> <span data-ttu-id="277dc-200">Du kan også angive denne indstilling til "Tabel" for at angive varerne manuelt eller vælge "Alle" for at føje alle varer til kvalitetsordren.</span><span class="sxs-lookup"><span data-stu-id="277dc-200">You could also set this to "Table" to specify the items manually, or select "All" to add all items to the quality order.</span></span>  
5. <span data-ttu-id="277dc-201">Vælg den kvalitetsgruppe, du oprettede før, i feltet Vare.</span><span class="sxs-lookup"><span data-stu-id="277dc-201">In the Item field, select the quality group that you created before.</span></span>
    * <span data-ttu-id="277dc-202">De tilgængelige indstillinger i feltet Vare afhænger af, hvad du har angivet i feltet Varekode.</span><span class="sxs-lookup"><span data-stu-id="277dc-202">The options available in the Item field depend on what you set in the Item code field.</span></span>  
6. <span data-ttu-id="277dc-203">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="277dc-203">In the list, find and select the desired record.</span></span>
7. <span data-ttu-id="277dc-204">Udvid eller skjul sektionen Proces.</span><span class="sxs-lookup"><span data-stu-id="277dc-204">Expand or collapse the Process section.</span></span>
8. <span data-ttu-id="277dc-205">Vælg en indstilling i feltet Hændelsestype.</span><span class="sxs-lookup"><span data-stu-id="277dc-205">In the Event type field, select an option.</span></span>
    * <span data-ttu-id="277dc-206">Dette er den hændelse, der udløser testen.</span><span class="sxs-lookup"><span data-stu-id="277dc-206">This is the event that triggers the test.</span></span> <span data-ttu-id="277dc-207">De tilgængelige indstillinger her afhænger af, hvilken proces du har valgt i feltet Referencetype.</span><span class="sxs-lookup"><span data-stu-id="277dc-207">The options available here depend on which process you selected in the Reference type field.</span></span>  
9. <span data-ttu-id="277dc-208">Vælg en indstilling i feltet Udførelse.</span><span class="sxs-lookup"><span data-stu-id="277dc-208">In the Execution field, select an option.</span></span>
10. <span data-ttu-id="277dc-209">Udvid eller skjul sektionen Proces for kvalitetsordre.</span><span class="sxs-lookup"><span data-stu-id="277dc-209">Expand or collapse the Quality order process section.</span></span>
11. <span data-ttu-id="277dc-210">Klik på rullelisten i feltet Hændelsesspærring for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="277dc-210">In the Event blocking field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="277dc-211">Dette felt viser en liste over processer, som det er muligt at blokere, hvis kvalitetsordren stadig er åben.</span><span class="sxs-lookup"><span data-stu-id="277dc-211">This field shows the list of processes that it’s possible to block if the quality order is still open.</span></span> <span data-ttu-id="277dc-212">Indstillingerne afhænger af, hvad du har valgt i feltet Hændelsestype.</span><span class="sxs-lookup"><span data-stu-id="277dc-212">The options depend on what you selected in the Event type field.</span></span>  
12. <span data-ttu-id="277dc-213">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="277dc-213">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="277dc-214">Dette vil være afhængigt af de tidligere valgte værdier.</span><span class="sxs-lookup"><span data-stu-id="277dc-214">This will be depending on the previous selected values.</span></span> <span data-ttu-id="277dc-215">Markér, hvis følgende processer skal blokeres, mens du har åbne kvalitetsordrer, der er knyttet til en kildedokumentlinje.</span><span class="sxs-lookup"><span data-stu-id="277dc-215">Select if the following processes must be blocked while having open quality orders linked to a source document line.</span></span>  
13. <span data-ttu-id="277dc-216">Udvid eller skjul sektionen Specifikationer.</span><span class="sxs-lookup"><span data-stu-id="277dc-216">Expand or collapse the Specifications section.</span></span>
14. <span data-ttu-id="277dc-217">Vælg den testgruppe, som du oprettede før, i feltet Testgruppe.</span><span class="sxs-lookup"><span data-stu-id="277dc-217">In the Test group field, select the test group that you created before.</span></span>
15. <span data-ttu-id="277dc-218">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="277dc-218">In the list, find and select the desired record.</span></span>
16. <span data-ttu-id="277dc-219">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="277dc-219">Click Save.</span></span>
17. <span data-ttu-id="277dc-220">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="277dc-220">Close the page.</span></span>

