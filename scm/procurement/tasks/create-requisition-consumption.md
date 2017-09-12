--- 
title: Oprette en forbrugsrekvisition
description: "Denne fremgangsmåde fører dig gennem processen med at oprette en rekvisition."
author: mkirknel
manager: AnnBe
ms.date: 11/14/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 07fe007005fcbbac1beecadb14dbd752376a0bd4
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-requisition-for-consumption"></a><span data-ttu-id="ac2aa-103">Oprette en forbrugsrekvisition</span><span class="sxs-lookup"><span data-stu-id="ac2aa-103">Create a requisition for consumption</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="ac2aa-104">Denne fremgangsmåde fører dig gennem processen med at oprette en rekvisition.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-104">This procedure walks you through the process of creating a requisition.</span></span> <span data-ttu-id="ac2aa-105">Den viser forskellige måder at søge efter produkter i indkøbskataloget, og hvordan du tilføjer et produkt, der ikke findes i kataloget.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-105">It shows you different ways to search for products in your procurement catalogue and how to add a product that isn’t in your catalogue.</span></span> <span data-ttu-id="ac2aa-106">Inden du begynder denne procedure, skal du have en indkøbspolitik, der er konfigureret med Forbrug som standardtypen for rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-106">Before you start this procedure, you must have a purchasing policy set up with Consumption as the default type of requisition.</span></span> <span data-ttu-id="ac2aa-107">Du kan gennemgå denne procedure i demodatafirmaet USMF eller bruge dine egne data.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-107">You can walk through this procedure in demo data company USMF, or using your own data.</span></span> <span data-ttu-id="ac2aa-108">Proceduren kan kun udføres af en brugerprofil, der er angivet som arbejder.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-108">The procedure can only be carried out by a user profile that is set up as worker.</span></span>  <span data-ttu-id="ac2aa-109">Denne opgave vil normalt udføres af en medarbejder.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-109">This task would normally be carried out by an employee.</span></span> <span data-ttu-id="ac2aa-110">Medarbejders sikkerhedsrolle tillader, at du kan udføre opgaverne, eller hvis du bruger USMF, kan du logge på som Alicia.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-110">The Employee employ security role will allow you to carry out the tasks, or if you’re using USMF, you can log in as Alicia.</span></span>


## <a name="create-a-new-requisition"></a><span data-ttu-id="ac2aa-111">Opret en ny rekvisition</span><span class="sxs-lookup"><span data-stu-id="ac2aa-111">Create a new requisition</span></span>
1. <span data-ttu-id="ac2aa-112">Gå til Indkøb og Forsyning > Indkøbsrekvisitioner > Indkøbsrekvisitioner, der er udarbejdet af mig.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-112">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="ac2aa-113">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-113">Click New.</span></span>
3. <span data-ttu-id="ac2aa-114">Angiv et navn for rekvisitionen i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-114">In the Name field, give the requisition a name.</span></span>
4. <span data-ttu-id="ac2aa-115">Angiv en dato i feltet Ønsket dato.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-115">In the Requested date field, enter a date.</span></span>
    * <span data-ttu-id="ac2aa-116">Som standard kopieres den ønskede dato og regnskabsdatoen til indkøbsrekvisitionslinjerne.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-116">By default, the requested date and accounting date are copied to the purchase requisition lines.</span></span> <span data-ttu-id="ac2aa-117">De kan ændres på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-117">They can be changed at the line level.</span></span> <span data-ttu-id="ac2aa-118">Den ønskede dato er den leveringsdato, der er anmodet om.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-118">The requested date is the requested delivery date.</span></span>  
5. <span data-ttu-id="ac2aa-119">Angiv en dato i datofeltet Regnskab.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-119">In the Accounting date field, enter a date.</span></span>
    * <span data-ttu-id="ac2aa-120">Regnskabsdatoen bruges til registrering af regnskabsposten i finans og til at kontrollere, om budgetmidlerne er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-120">The accounting date is used to record the accounting entry in the general ledger, and to validate whether budget funds are available.</span></span>  
6. <span data-ttu-id="ac2aa-121">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-121">Click OK.</span></span>
7. <span data-ttu-id="ac2aa-122">Klik på rullelisten i feltet Årsag for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-122">In the Reason field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ac2aa-123">Den forretningsberettigelsesårsag, som du vælger, vises som standard for indkøbsrekvisitionslinjerne, men du kan ændre den på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-123">By default, the business justification reason that you select appears for the purchase requisition lines, but you can change it at the line level.</span></span>    
8. <span data-ttu-id="ac2aa-124">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-124">In the list, find and select the desired record.</span></span>
9. <span data-ttu-id="ac2aa-125">Vælg årsagen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-125">Select the reason</span></span>
10. <span data-ttu-id="ac2aa-126">Angiv en mere beskrivende begrundelse for rekvisitionen i oplysningsfeltet</span><span class="sxs-lookup"><span data-stu-id="ac2aa-126">In the details field enter a more descriptive justification for the requisition</span></span>

## <a name="add-a-line-to-the-requisition"></a><span data-ttu-id="ac2aa-127">Føj en ny linje til rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-127">Add a line to the requisition</span></span>
1. <span data-ttu-id="ac2aa-128">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-128">Click Add line.</span></span>
    * <span data-ttu-id="ac2aa-129">Der er to måder at føje linjer til indkøbsrekvisitionen på.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-129">There are two ways of adding lines to the purchase requisition.</span></span> <span data-ttu-id="ac2aa-130">Hvis du allerede kender produktnummeret, eller du allerede ved, at du anmoder om et produkt, der ikke findes i produktkataloget, kan du tilføje linjen direkte med "Tilføj linje".</span><span class="sxs-lookup"><span data-stu-id="ac2aa-130">If you already know the product number or you already  know that you are requesting a product that is not in the product catalogueue, then you can add the line directly with "Add line".</span></span> <span data-ttu-id="ac2aa-131">Den anden måde er at bruge "Tilføj produkter", hvor du kan bruge søgning og filtrering til at finde varer i produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-131">The other way is to use "Add products" where you can use searching and filtering to find items in the product catalogueue.</span></span>    
2. <span data-ttu-id="ac2aa-132">Klik på den række, du netop har oprettet.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-132">Click on the row you just created.</span></span>
    * <span data-ttu-id="ac2aa-133">Anmoderen er den arbejder, der har anmodet om rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-133">The requester is the worker that has requested the requisition.</span></span>   
    * <span data-ttu-id="ac2aa-134">Den person, der forbereder rekvisitionen, er som standard den arbejder, der har anmodet om den.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-134">By default the person preparing the requisition is the worker who has requested it.</span></span> <span data-ttu-id="ac2aa-135">Der skal gives tilladelse til at forberede en rekvisitionslinje på vegne af en anden arbejder.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-135">You have to be given permission to prepare a requisition line on behalf of another worker.</span></span> <span data-ttu-id="ac2aa-136">Hvis du har sådanne tilladelser, vises de andre arbejdere i dette opslag.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-136">If you have such permissions then the other workers will show up in this lookup.</span></span>  
3. <span data-ttu-id="ac2aa-137">Indtast en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-137">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="ac2aa-138">De varer, du kan vælge, er begrænset af kategoriadgangspolitik og indkøbskataloget for den juridiske indkøbsenhed.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-138">The items that are available for you to choose are limited by the category access policy and the procurement catalogue for the buying legal entity.</span></span>   
4. <span data-ttu-id="ac2aa-139">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-139">In the Quantity field, enter a number.</span></span>

## <a name="add-more-products-to-the-requisition"></a><span data-ttu-id="ac2aa-140">Føj flere produkter til rekvisitionen</span><span class="sxs-lookup"><span data-stu-id="ac2aa-140">Add more products to the requisition</span></span>
1. <span data-ttu-id="ac2aa-141">Klik på Tilføj produkter.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-141">Click Add products.</span></span>
    * <span data-ttu-id="ac2aa-142">Dette er indstillingen, hvor du kan søge efter produkter i produktkataloget.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-142">This is the option where you can search for products in the product catalogueue.</span></span>    
2. <span data-ttu-id="ac2aa-143">Skriv den første del af navnet på den kategori, du søger efter, i feltet Find indkøb, og klik derefter på Enter.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-143">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="ac2aa-144">Skriv f.eks. comput.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-144">For example, type comput.</span></span>  
3. <span data-ttu-id="ac2aa-145">Bruge InvokeDefaultButton-genvejen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-145">Use the InvokeDefaultButton shortcut.</span></span>
4. <span data-ttu-id="ac2aa-146">I den valgte kategori skal du bruge Filter til filtrering af listen over produkter.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-146">Use the Filter to filter the list of products in the selected category.</span></span>
5. <span data-ttu-id="ac2aa-147">Vælg det produktkort, der skal føjes til rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-147">Select the product card that you want to add to the requisition.</span></span>
6. <span data-ttu-id="ac2aa-148">Klik på Føj til linjer</span><span class="sxs-lookup"><span data-stu-id="ac2aa-148">Click Add to lines.</span></span>
7. <span data-ttu-id="ac2aa-149">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-149">In the Quantity field, enter a number.</span></span>
8. <span data-ttu-id="ac2aa-150">Skriv den første del af navnet på den kategori, du søger efter, i feltet Find indkøb, og klik derefter på Enter.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-150">In the Find procurement category node field, type the first part of the name of the category that you are looking for, and then click Enter.</span></span>
    * <span data-ttu-id="ac2aa-151">Skriv f.eks. over (overstregningstuscher).</span><span class="sxs-lookup"><span data-stu-id="ac2aa-151">For example, type High (highlighters).</span></span>  
9. <span data-ttu-id="ac2aa-152">Bruge InvokeDefaultButton-genvejen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-152">Use the InvokeDefaultButton shortcut.</span></span>
10. <span data-ttu-id="ac2aa-153">Klik på Tilføj ikke-angivet produkt til linjer for at tilføje et produkt, der ikke findes i indkøbskataloget.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-153">Click Add unlisted product to lines to add a product that’s not listed in the procurement catalogue.</span></span>
11. <span data-ttu-id="ac2aa-154">Angiv en værdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-154">In the Product name field, type a value.</span></span>
12. <span data-ttu-id="ac2aa-155">Skriv en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-155">In the Unit field, type a value.</span></span>
13. <span data-ttu-id="ac2aa-156">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-156">Click OK.</span></span>
14. <span data-ttu-id="ac2aa-157">Angiv en beskrivelse af produktet i feltet Varebeskrivelse.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-157">In the Item description field, add a description of the product.</span></span>
15. <span data-ttu-id="ac2aa-158">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-158">In the Quantity field, enter a number.</span></span>
16. <span data-ttu-id="ac2aa-159">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-159">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="ac2aa-160">Hvis du kender prisen for en bestemt kreditor (som du vælger i feltet kreditorkonto), kan denne pris indtastes</span><span class="sxs-lookup"><span data-stu-id="ac2aa-160">If you know the price for a particular vendor (that you select in the vendor account field) then that price can be entered</span></span>   
17. <span data-ttu-id="ac2aa-161">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-161">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="ac2aa-162">De kreditorer, der findes i dette felt, afhænger af de indkøbspolitikker og den status, som kreditoren har for den aktuelle indkøbskategori.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-162">The vendors that are available in this field depend on the purchasing policies and the status that the vendor has for the current procurement category.</span></span> <span data-ttu-id="ac2aa-163">Som et alternativ til valg af kreditor her kan du klikke på knappen Foreslå kreditor.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-163">As an alternative to selecting a vendor here, you can click the Suggest vendor button.</span></span>    
18. <span data-ttu-id="ac2aa-164">Vælg den kreditor, du vil bruge, på listen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-164">In the list, select the vendor you want to use.</span></span>
19. <span data-ttu-id="ac2aa-165">Skriv en værdi i talfeltet Ekstern vare.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-165">In the External item number field, type a value.</span></span>
    * <span data-ttu-id="ac2aa-166">Dette er et referencenummer til det produkt, der er kendt af kreditoren.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-166">This is a reference number for the product that is known by the vendor.</span></span> <span data-ttu-id="ac2aa-167">Dette kan eksempelvis være varenummeret for produktet i kreditorens eget katalog.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-167">For example, this could be the item number of the product in the vendor's own catalogue.</span></span>  
20. <span data-ttu-id="ac2aa-168">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-168">Click OK.</span></span>

## <a name="distribute-amounts"></a><span data-ttu-id="ac2aa-169">Fordel beløb</span><span class="sxs-lookup"><span data-stu-id="ac2aa-169">Distribute amounts</span></span>
1. <span data-ttu-id="ac2aa-170">Klik på Finans.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-170">Click Financials.</span></span>
2. <span data-ttu-id="ac2aa-171">Klik på Fordel beløb.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-171">Click Distribute amounts.</span></span>
    * <span data-ttu-id="ac2aa-172">Denne fremgangsmåde viser, hvordan du fordeler omkostningerne for den første linje mellem 2 konti.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-172">This process shows you how to distribute the cost for the first line between 2 accounts.</span></span> <span data-ttu-id="ac2aa-173">Dette kan også foretages senere, når rekvisitionen er til gennemsyn.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-173">This can also be done later when the requisition is in review.</span></span>  
3. <span data-ttu-id="ac2aa-174">Klik på Opdel for at oprette en ny fordelingslinje.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-174">Click Split to create a new distribution line.</span></span>
4. <span data-ttu-id="ac2aa-175">Vælg den første bærer, som skal være en del af omkostningen, i feltet Finanskonto.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-175">In the Ledger account field select the first cost centre that should take part of the cost.</span></span>
5. <span data-ttu-id="ac2aa-176">Vælg den anden fordelingslinje.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-176">Select the other distribution line.</span></span>
6. <span data-ttu-id="ac2aa-177">Angiv den anden bærer i feltet Finanskonto.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-177">In the Ledger account field specify the other cost centre.</span></span>
7. <span data-ttu-id="ac2aa-178">Klik på Fordel ligeligt.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-178">Click Distribute equally.</span></span>
8. <span data-ttu-id="ac2aa-179">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-179">Close the page.</span></span>

## <a name="view-line-details"></a><span data-ttu-id="ac2aa-180">Vis linjedetaljer</span><span class="sxs-lookup"><span data-stu-id="ac2aa-180">View line details</span></span>
1. <span data-ttu-id="ac2aa-181">Slå udvidelsen af sektionen Linjedetaljer til/fra.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-181">Toggle the expansion of the Line details section.</span></span>

## <a name="submit-the-requisition"></a><span data-ttu-id="ac2aa-182">Send rekvisitionen</span><span class="sxs-lookup"><span data-stu-id="ac2aa-182">Submit the requisition</span></span>
1. <span data-ttu-id="ac2aa-183">Klik på Arbejdsgang for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-183">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="ac2aa-184">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-184">Click Submit.</span></span>
3. <span data-ttu-id="ac2aa-185">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-185">Close the page.</span></span>
4. <span data-ttu-id="ac2aa-186">Skriv en bemærkning til godkenderen af rekvisitionen i feltet Bemærkning.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-186">In the Comment field, type a note for the approver of the requisition.</span></span>
5. <span data-ttu-id="ac2aa-187">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-187">Click Submit.</span></span>
6. <span data-ttu-id="ac2aa-188">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-188">Close the page.</span></span>
7. <span data-ttu-id="ac2aa-189">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="ac2aa-189">Refresh the page.</span></span>


