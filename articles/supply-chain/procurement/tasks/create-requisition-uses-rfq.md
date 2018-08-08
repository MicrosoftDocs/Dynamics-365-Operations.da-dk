--- 
title: Oprette en rekvisition, der bruger en tilbudsanmodning
description: "Denne vejledning viser, hvordan du føjer pris- og leverandøroplysninger til en indkøbsrekvisition fra en tilbudsanmodningsproces."
author: mkirknel
manager: AnnBe
ms.date: 08/25/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: 8cb67b3406a9574343a88e31d69359f3c463ee14
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---
# <a name="create-a-requisition-that-uses-an-rfq"></a><span data-ttu-id="c5f85-103">Oprette en rekvisition, der bruger en tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="c5f85-103">Create a requisition that uses an RFQ</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="c5f85-104">Denne vejledning viser, hvordan du føjer pris- og leverandøroplysninger til en indkøbsrekvisition fra en tilbudsanmodningsproces.</span><span class="sxs-lookup"><span data-stu-id="c5f85-104">This guide shows how to add price and vendor information to a purchase requisition from an RFQ process.</span></span> <span data-ttu-id="c5f85-105">Eksemplet i denne vejledning kan bruges i USMF-demodatafirmaet, og du skal være logget på som administrator for at fuldføre alle trin.</span><span class="sxs-lookup"><span data-stu-id="c5f85-105">The example shown in this guide can be used in the USMF demo data company, and you must be logged in as an Admin to complete all the steps.</span></span> <span data-ttu-id="c5f85-106">Opgaverne i denne vejledning udføres normalt af indkøbsmedarbejderne.</span><span class="sxs-lookup"><span data-stu-id="c5f85-106">The tasks in this guide would typically be done by procurement professionals.</span></span>


## <a name="create-a-requisition"></a><span data-ttu-id="c5f85-107">Opret en rekvisition</span><span class="sxs-lookup"><span data-stu-id="c5f85-107">Create a requisition</span></span>
1. <span data-ttu-id="c5f85-108">Gå til Indkøb og Forsyning > Indkøbsrekvisitioner > Indkøbsrekvisitioner, der er udarbejdet af mig.</span><span class="sxs-lookup"><span data-stu-id="c5f85-108">Go to Procurement and sourcing > Purchase requisitions > Purchase requisitions prepared by me.</span></span>
2. <span data-ttu-id="c5f85-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="c5f85-109">Click New.</span></span>
3. <span data-ttu-id="c5f85-110">Skriv en værdi i feltet Navn.</span><span class="sxs-lookup"><span data-stu-id="c5f85-110">In the Name field, type a value.</span></span>
4. <span data-ttu-id="c5f85-111">Angiv en dato i feltet Ønsket dato.</span><span class="sxs-lookup"><span data-stu-id="c5f85-111">In the Requested date field, enter a date.</span></span>
5. <span data-ttu-id="c5f85-112">Angiv en dato i datofeltet Regnskab.</span><span class="sxs-lookup"><span data-stu-id="c5f85-112">In the Accounting date field, enter a date.</span></span>
6. <span data-ttu-id="c5f85-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5f85-113">Click OK.</span></span>
7. <span data-ttu-id="c5f85-114">Indtast eller vælg en værdi i feltet Årsag.</span><span class="sxs-lookup"><span data-stu-id="c5f85-114">In the Reason field, enter or select a value.</span></span>
8. <span data-ttu-id="c5f85-115">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="c5f85-115">Click Add line.</span></span>
9. <span data-ttu-id="c5f85-116">Vælg en kategori i træet i feltet Indkøbskategori, og klik derefter på OK.</span><span class="sxs-lookup"><span data-stu-id="c5f85-116">In the Procurement category field, select a category in the tree, and then click OK.</span></span>
10. <span data-ttu-id="c5f85-117">Skriv en værdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="c5f85-117">In the Product name field, type a value.</span></span>
11. <span data-ttu-id="c5f85-118">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="c5f85-118">In the Quantity field, enter a number.</span></span>
12. <span data-ttu-id="c5f85-119">Indtast eller vælg en værdi i feltet Enhed.</span><span class="sxs-lookup"><span data-stu-id="c5f85-119">In the Unit field, enter or select a value.</span></span>
13. <span data-ttu-id="c5f85-120">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="c5f85-120">Click Save.</span></span>
14. <span data-ttu-id="c5f85-121">Klik på Arbejdsgang for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-121">Click Workflow to open the drop dialog.</span></span>
15. <span data-ttu-id="c5f85-122">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="c5f85-122">Click Submit.</span></span>
16. <span data-ttu-id="c5f85-123">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5f85-123">Close the page.</span></span>
17. <span data-ttu-id="c5f85-124">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="c5f85-124">Click Submit.</span></span>

## <a name="reassign-a-workflow-task"></a><span data-ttu-id="c5f85-125">Tildel en opgave i en arbejdsgang til en anden</span><span class="sxs-lookup"><span data-stu-id="c5f85-125">Reassign a workflow task</span></span>
    * <span data-ttu-id="c5f85-126">Den næste opgave er at oprette en tilbudsanmodning for at få tilbud på produktet fra leverandører.</span><span class="sxs-lookup"><span data-stu-id="c5f85-126">The next task is to create an RFQ to get bids from vendors for the product.</span></span> <span data-ttu-id="c5f85-127">I demodataene for USMF er arbejdsgangen for indkøbsrekvisitionen konfigureret med en regel, at hvis en leverandør ikke er markeret, eller hvis prisen er 0 for en linje, tildeles der en opgave til en bestemt arbejder om at oprette en tilbudsanmodning.</span><span class="sxs-lookup"><span data-stu-id="c5f85-127">In USMF demo data, the requisition workflow is set up with a rule so that if a vendor is not selected, or the unit price is 0 for a line, a task is assigned to a specific worker to create an RFQ.</span></span> <span data-ttu-id="c5f85-128">For at fortsætte med denne vejledning skal du gentildele opgaven til en anden bruger (dig selv).</span><span class="sxs-lookup"><span data-stu-id="c5f85-128">To continue with this guide, you need to re-assign that task to another user (yourself).</span></span> <span data-ttu-id="c5f85-129">Det kan du kun gøre, hvis du er logget på som administrator.</span><span class="sxs-lookup"><span data-stu-id="c5f85-129">You can only do this if you are logged in as an Admin.</span></span>  
1. <span data-ttu-id="c5f85-130">Klik på Arbejdsgang for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-130">Click Workflow to open the drop dialog.</span></span>
2. <span data-ttu-id="c5f85-131">Klik på Vis historik.</span><span class="sxs-lookup"><span data-stu-id="c5f85-131">Click View history.</span></span>
3. <span data-ttu-id="c5f85-132">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="c5f85-132">Refresh the page.</span></span>
4. <span data-ttu-id="c5f85-133">Udvid sektionen Sporingsdetaljer.</span><span class="sxs-lookup"><span data-stu-id="c5f85-133">Expand the Tracking details section.</span></span>
5. <span data-ttu-id="c5f85-134">Vælg 'den linje, der starter med "Arbejdsgang for linjeelement aktiveret den"' i træet.</span><span class="sxs-lookup"><span data-stu-id="c5f85-134">In the tree, select 'the line that starts with “Line workflow activated on”'.</span></span>
6. <span data-ttu-id="c5f85-135">Klik på Vis detaljer for arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="c5f85-135">Click View workflow details.</span></span>
7. <span data-ttu-id="c5f85-136">Udvid sektionen Workflowopgaver.</span><span class="sxs-lookup"><span data-stu-id="c5f85-136">Expand the Work items section.</span></span>
8. <span data-ttu-id="c5f85-137">Klik på Tildel igen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-137">Click Reassign.</span></span>
9. <span data-ttu-id="c5f85-138">Vælg Administrator i feltet Bruger.</span><span class="sxs-lookup"><span data-stu-id="c5f85-138">In the User field, select Admin.</span></span>
10. <span data-ttu-id="c5f85-139">Klik på Tildel igen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-139">Click Reassign.</span></span>
11. <span data-ttu-id="c5f85-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5f85-140">Close the page.</span></span>
12. <span data-ttu-id="c5f85-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5f85-141">Close the page.</span></span>

## <a name="create-an-rfq"></a><span data-ttu-id="c5f85-142">Opret en tilbudsanmodning</span><span class="sxs-lookup"><span data-stu-id="c5f85-142">Create an RFQ</span></span>
1. <span data-ttu-id="c5f85-143">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="c5f85-143">Refresh the page.</span></span>
2. <span data-ttu-id="c5f85-144">Klik på Tilbudsanmodning.</span><span class="sxs-lookup"><span data-stu-id="c5f85-144">Click Request for quotation.</span></span>
3. <span data-ttu-id="c5f85-145">Derefter skal du vælge USMF i feltet Juridisk indkøbsenhed.</span><span class="sxs-lookup"><span data-stu-id="c5f85-145">In the Buying legal entity field, select USMF.</span></span>
    * <span data-ttu-id="c5f85-146">Du skal vælge den samme juridiske enhed som den, der er på rekvisitionslinjen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-146">You must select the same legal entity that’s on the requisition line.</span></span>  
4. <span data-ttu-id="c5f85-147">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-147">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="c5f85-148">Hvis du havde flere linjer på indkøbsrekvisitionen, kan du vælge alle de linjer, du vil føje til tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-148">If you had multiple lines on your purchase requisition, select all the lines that you want to add to the RFQ.</span></span>  
5. <span data-ttu-id="c5f85-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5f85-149">Click OK.</span></span>
6. <span data-ttu-id="c5f85-150">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="c5f85-150">Refresh the page.</span></span>
7. <span data-ttu-id="c5f85-151">Åbn faktaboksen, og udvid derefter sektionen Relaterede dokumenter.</span><span class="sxs-lookup"><span data-stu-id="c5f85-151">Open the FactBox and then expand the Related documents section.</span></span>
    * <span data-ttu-id="c5f85-152">Du har måske allerede åbnet faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-152">You may already have the FactBox open.</span></span> <span data-ttu-id="c5f85-153">Se efter ikonet med en pil, til højre for til/fra-knapperne Linjer/Sidehoved.</span><span class="sxs-lookup"><span data-stu-id="c5f85-153">Look for the icon with an arrow on it, to the right of the Lines/Header toggle buttons.</span></span> <span data-ttu-id="c5f85-154">Hvis pilen peger mod højre, er faktaboksen allerede åben.</span><span class="sxs-lookup"><span data-stu-id="c5f85-154">If the arrow is pointing to the right, the FactBox is already open.</span></span> <span data-ttu-id="c5f85-155">Hvis pilen peger mod venstre, skal du klikke på den for at åbne faktaboksen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-155">If the arrow points to the left, click it to open the FactBox.</span></span>  
8. <span data-ttu-id="c5f85-156">Klik på linket i feltet Tilbudsanmodning for at åbne den tilbudsanmodning, der netop er blevet oprettet.</span><span class="sxs-lookup"><span data-stu-id="c5f85-156">Click the link in the Request for quotation field to open the RFQ that was just created.</span></span>
9. <span data-ttu-id="c5f85-157">Klik på Overskrift.</span><span class="sxs-lookup"><span data-stu-id="c5f85-157">Click Header.</span></span>
10. <span data-ttu-id="c5f85-158">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="c5f85-158">Click Add.</span></span>
11. <span data-ttu-id="c5f85-159">Indtast eller vælg en værdi i feltet Kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="c5f85-159">In the Vendor account field, enter or select a value.</span></span>
12. <span data-ttu-id="c5f85-160">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="c5f85-160">Click Add.</span></span>
13. <span data-ttu-id="c5f85-161">Indtast eller vælg en værdi i feltet Kreditorkonto.</span><span class="sxs-lookup"><span data-stu-id="c5f85-161">In the Vendor account field, enter or select a value.</span></span>
14. <span data-ttu-id="c5f85-162">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="c5f85-162">Click Send.</span></span>
15. <span data-ttu-id="c5f85-163">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5f85-163">Click OK.</span></span>
16. <span data-ttu-id="c5f85-164">Klik på Indtast svar.</span><span class="sxs-lookup"><span data-stu-id="c5f85-164">Click Enter reply.</span></span>
17. <span data-ttu-id="c5f85-165">Klik på Svar i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c5f85-165">On the Action Pane, click Reply.</span></span>
18. <span data-ttu-id="c5f85-166">Klik på Kopiér data til svar.</span><span class="sxs-lookup"><span data-stu-id="c5f85-166">Click Copy data to reply.</span></span>
    * <span data-ttu-id="c5f85-167">Derved kopieres data, f.eks. antal og datoer, fra tilbudsanmodningen til svaret.</span><span class="sxs-lookup"><span data-stu-id="c5f85-167">This copies data, such as the quantity and dates, from the RFQ to the reply .</span></span>  
19. <span data-ttu-id="c5f85-168">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="c5f85-168">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="c5f85-169">Det er den pris, du har modtaget fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="c5f85-169">This is the price that you’ve received from the vendor.</span></span> <span data-ttu-id="c5f85-170">Du kan også angive yderligere oplysninger fra leverandøren.</span><span class="sxs-lookup"><span data-stu-id="c5f85-170">You might also want to enter additional information from the vendor.</span></span>  
20. <span data-ttu-id="c5f85-171">Klik på Acceptér.</span><span class="sxs-lookup"><span data-stu-id="c5f85-171">Click Accept.</span></span>
21. <span data-ttu-id="c5f85-172">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="c5f85-172">Click OK.</span></span>

## <a name="verify-that-vendor-and-price-have-been-transferred-to-the-requisition"></a><span data-ttu-id="c5f85-173">Kontrollér, at leverandøren og prisen er blevet overført til rekvisitionen</span><span class="sxs-lookup"><span data-stu-id="c5f85-173">Verify that vendor and price have been transferred to the requisition</span></span>
1. <span data-ttu-id="c5f85-174">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5f85-174">Close the page.</span></span>
2. <span data-ttu-id="c5f85-175">Klik på Linjer.</span><span class="sxs-lookup"><span data-stu-id="c5f85-175">Click Lines.</span></span>
3. <span data-ttu-id="c5f85-176">Klik på Relaterede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="c5f85-176">Click Related information.</span></span>
4. <span data-ttu-id="c5f85-177">Klik på Indkøbsrekvisitionslinjer.</span><span class="sxs-lookup"><span data-stu-id="c5f85-177">Click Purchase requisition.</span></span>
5. <span data-ttu-id="c5f85-178">Vælg den linje, der blev overført til tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-178">Select the line that was transferred to the RFQ.</span></span>
    * <span data-ttu-id="c5f85-179">Kontrollér, at prisen og leverandøren er blevet kopieret til rekvisitionen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-179">Verify that the price and vendor have been copied to the requisition.</span></span>  
6. <span data-ttu-id="c5f85-180">Klik på Arbejdsgang for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="c5f85-180">Click Workflow to open the drop dialog.</span></span>
7. <span data-ttu-id="c5f85-181">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="c5f85-181">Click Complete.</span></span>
8. <span data-ttu-id="c5f85-182">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="c5f85-182">Close the page.</span></span>
9. <span data-ttu-id="c5f85-183">Klik på Fuldført.</span><span class="sxs-lookup"><span data-stu-id="c5f85-183">Click Complete.</span></span>


