--- 
title: "Angive og sammenligne bud på tilbudsanmodninger og tildeler kontrakter"
description: "Denne procedure viser, hvordan du indtaster svar på en tilbudsanmodning, angiver score og sammenligner bud og derefter tildeler buddet til en af kreditorerne."
author: mkirknel
manager: AnnBe
ms.date: 06/07/2016
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
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 140d9f7a48b6cb06f02d3c4e6440d0a99a9d8161
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="enter-and-compare-rfq-bids-and-award-contracts"></a><span data-ttu-id="22904-103">Angive og sammenligne bud på tilbudsanmodninger og tildeler kontrakter</span><span class="sxs-lookup"><span data-stu-id="22904-103">Enter and compare RFQ bids and award contracts</span></span>

[!INCLUDE [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="22904-104">Denne procedure viser, hvordan du indtaster svar på en tilbudsanmodning, angiver score og sammenligner bud og derefter tildeler buddet til en af kreditorerne.</span><span class="sxs-lookup"><span data-stu-id="22904-104">This procedure shows you how to enter replies to an RFQ, score and compare bids, and then award the bid to one of the vendors.</span></span> <span data-ttu-id="22904-105">Du kan bruge denne procedure i USMF-demodatafirmaet.</span><span class="sxs-lookup"><span data-stu-id="22904-105">You can use this procedure in demo data company USMF.</span></span> <span data-ttu-id="22904-106">Før du starter, skal du have en tilbudsanmodning med to linjer, der er blevet sendt til mindst to kreditorer.</span><span class="sxs-lookup"><span data-stu-id="22904-106">Before you start, you must have an RFQ with two lines that has been sent to at least two vendors.</span></span> <span data-ttu-id="22904-107">Du kan køre proceduren "Oprette en tilbudsanmodning" som en forudsætning for at oprette den.</span><span class="sxs-lookup"><span data-stu-id="22904-107">You can run the "Create a request for quotation" procedure as a prerequisite to create this.</span></span> <span data-ttu-id="22904-108">Du skal have oprettet en scorekriterier, før du kan køre denne procedure.</span><span class="sxs-lookup"><span data-stu-id="22904-108">You need to have set up scoring criteria before you can run this procedure.</span></span>


## <a name="enter-a-reply-from-a-vendor"></a><span data-ttu-id="22904-109">Angive et svar fra en kreditor</span><span class="sxs-lookup"><span data-stu-id="22904-109">Enter a reply from a vendor</span></span>
1. <span data-ttu-id="22904-110">Gå til Indkøb og forsyning > Tilbudsanmodninger > Alle tilbudsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="22904-110">Go to Procurement and sourcing > Requests for quotations > All requests for quotations.</span></span>
2. <span data-ttu-id="22904-111">Vælg en tilbudsanmodning, der har statussen Afsendt, og klik på linket for tiilbudsanmodningens sagsnummer.</span><span class="sxs-lookup"><span data-stu-id="22904-111">Select an RFQ that has a status of Sent and click the link on the Request for quotation case number.</span></span>
    * <span data-ttu-id="22904-112">Tilbudsanmodningen bør være sendt til mindst 2 kreditorer.</span><span class="sxs-lookup"><span data-stu-id="22904-112">The RFQ should have been sent to at least 2 vendors.</span></span>  
3. <span data-ttu-id="22904-113">Klik på Overskrift for at gå til listen over kreditorer.</span><span class="sxs-lookup"><span data-stu-id="22904-113">Click Header to go to the list of vendors.</span></span>
4. <span data-ttu-id="22904-114">Vælg den kreditor, du vil angive et svar til på tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="22904-114">Select the vendor for whom you want to enter a response on the RFQ.</span></span>
5. <span data-ttu-id="22904-115">Klik på Indtast svar.</span><span class="sxs-lookup"><span data-stu-id="22904-115">Click Enter reply.</span></span>
6. <span data-ttu-id="22904-116">Klik på Svar i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="22904-116">On the Action Pane, click Reply.</span></span>
7. <span data-ttu-id="22904-117">Klik på Kopiér data til svar.</span><span class="sxs-lookup"><span data-stu-id="22904-117">Click Copy data to reply.</span></span>
    * <span data-ttu-id="22904-118">Denne handling kopierer markerede data, f.eks. antallet fra tilbudsanmodningssagen til svaret på tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="22904-118">This action will copy selected data, for example, the quantity from the RFQ case to the RFQ reply.</span></span> <span data-ttu-id="22904-119">Alternativt kan du springe over denne handling og udfylde alle svarfelter manuelt, når du redigerer svaret.</span><span class="sxs-lookup"><span data-stu-id="22904-119">Alternatively you can skip this action and fill in all the response fields manually when you edit the reply.</span></span>  
8. <span data-ttu-id="22904-120">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="22904-120">Click Edit.</span></span>
9. <span data-ttu-id="22904-121">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="22904-121">In the Unit price field, enter a number.</span></span>
10. <span data-ttu-id="22904-122">Vælg den anden tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="22904-122">Choose the other quotation line.</span></span>
11. <span data-ttu-id="22904-123">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="22904-123">In the Unit price field, enter a number.</span></span>

## <a name="score-the-bid"></a><span data-ttu-id="22904-124">Give score til det andet bud</span><span class="sxs-lookup"><span data-stu-id="22904-124">Score the bid</span></span>
1. <span data-ttu-id="22904-125">Klik på Overskrift for at gå til scoren for buddet.</span><span class="sxs-lookup"><span data-stu-id="22904-125">Click Header to go to the scoring of the bid.</span></span>
2. <span data-ttu-id="22904-126">Udvid sektionen Budscore.</span><span class="sxs-lookup"><span data-stu-id="22904-126">Expand the Bid scoring section.</span></span>
3. <span data-ttu-id="22904-127">Skriv et tal i feltet Resultat for en af scorekriterierne.</span><span class="sxs-lookup"><span data-stu-id="22904-127">In the Score field, enter a number for one of the scoring criteria.</span></span>
    * <span data-ttu-id="22904-128">Hvis du placerer markøren over et af scorekriterierne, viser et værktøjstip intervallet for scoren.</span><span class="sxs-lookup"><span data-stu-id="22904-128">If you hover over one of the scoring criteria a tooltip shows the range that you have to score within.</span></span> <span data-ttu-id="22904-129">Du kan tilføje et tal mellem 1 og 5 til et af kriterierne i denne demo.</span><span class="sxs-lookup"><span data-stu-id="22904-129">In this demo you can add a number between 1 and 5 to any of the criteria.</span></span>  
4. <span data-ttu-id="22904-130">Vælg et andet scorekriterium.</span><span class="sxs-lookup"><span data-stu-id="22904-130">Select another scoring criterion.</span></span>
5. <span data-ttu-id="22904-131">Angiv et tal i feltet Resultat.</span><span class="sxs-lookup"><span data-stu-id="22904-131">In the Score field, enter a number.</span></span>
6. <span data-ttu-id="22904-132">Udvid sektionen Spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="22904-132">Expand the Questionnaires section.</span></span>
    * <span data-ttu-id="22904-133">Hvis tilbudsanmodningssagen har et spørgeskema, der blev sendt til kreditorerne, kan du angive deres svar i afsnittet for spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="22904-133">If the RFQ case has a questionnaire that was sent to the vendors, you can enter their responses in the questionnaire section.</span></span>  
7. <span data-ttu-id="22904-134">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="22904-134">Close the page.</span></span>

## <a name="enter-a-reply-for-another-vendor"></a><span data-ttu-id="22904-135">Angive et svar til en anden kreditor</span><span class="sxs-lookup"><span data-stu-id="22904-135">Enter a reply for another vendor</span></span>
1. <span data-ttu-id="22904-136">Vælg den næste kreditor ved at fjerne den kreditor, du lige har angivet svar til, og derefter vælge rækken for den næste kreditor.</span><span class="sxs-lookup"><span data-stu-id="22904-136">Select the next vendor by clearing the vendor you have just entered the reply for and then selecting the row for the next vendor.</span></span>
2. <span data-ttu-id="22904-137">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="22904-137">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="22904-138">Klik på Indtast svar.</span><span class="sxs-lookup"><span data-stu-id="22904-138">Click Enter reply.</span></span>
4. <span data-ttu-id="22904-139">Klik på Kopiér data til svar.</span><span class="sxs-lookup"><span data-stu-id="22904-139">Click Copy data to reply.</span></span>
5. <span data-ttu-id="22904-140">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="22904-140">Click Edit.</span></span>
6. <span data-ttu-id="22904-141">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="22904-141">In the Unit price field, enter a number.</span></span>
7. <span data-ttu-id="22904-142">Vælg den anden tilbudslinje.</span><span class="sxs-lookup"><span data-stu-id="22904-142">Choose the other quotation line.</span></span>
8. <span data-ttu-id="22904-143">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="22904-143">In the Unit price field, enter a number.</span></span>

## <a name="score-the-second-bid"></a><span data-ttu-id="22904-144">Give score til det andet bud</span><span class="sxs-lookup"><span data-stu-id="22904-144">Score the second bid</span></span>
1. <span data-ttu-id="22904-145">Klik på Overskrift for at gå til scoren for buddet.</span><span class="sxs-lookup"><span data-stu-id="22904-145">Click Header to go to scoring of the bid.</span></span>
2. <span data-ttu-id="22904-146">Angiv et tal i feltet Resultat.</span><span class="sxs-lookup"><span data-stu-id="22904-146">In the Score field, enter a number.</span></span>
3. <span data-ttu-id="22904-147">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="22904-147">In the list, find and select the desired record.</span></span>
4. <span data-ttu-id="22904-148">Angiv et tal i feltet Resultat.</span><span class="sxs-lookup"><span data-stu-id="22904-148">In the Score field, enter a number.</span></span>

## <a name="compare-the-replies"></a><span data-ttu-id="22904-149">Sammenligne svarene</span><span class="sxs-lookup"><span data-stu-id="22904-149">Compare the replies</span></span>
1. <span data-ttu-id="22904-150">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="22904-150">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="22904-151">Klik på Sammenlign svar.</span><span class="sxs-lookup"><span data-stu-id="22904-151">Click Compare replies.</span></span>
3. <span data-ttu-id="22904-152">Angiv et tal i feltet Rang.</span><span class="sxs-lookup"><span data-stu-id="22904-152">In the Rank field, enter a number.</span></span>
    * <span data-ttu-id="22904-153">Denne side viser bud med overskriften og linjerne samt den samlede score på overskriftsniveauet.</span><span class="sxs-lookup"><span data-stu-id="22904-153">This page shows the bids with the header and lines, and the total score on the header level.</span></span> <span data-ttu-id="22904-154">Du kan sammenligne linjerne ved at sortere i gitteret, så sammenlignelige linjer er placeret ved siden af hinanden.</span><span class="sxs-lookup"><span data-stu-id="22904-154">You can compare the lines by sorting in the grid so that comparable lines are next to each other.</span></span> <span data-ttu-id="22904-155">Oplysningerne inkluderer også: Antal: Antallet er anført af kreditoren.</span><span class="sxs-lookup"><span data-stu-id="22904-155">The information also includes:   Quantity: The quantity quoted by the vendor.</span></span> <span data-ttu-id="22904-156">Dette er muligvis ikke det samme som det antal, der er angivet i tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="22904-156">This might not equal the quantity specified in the RFQ.</span></span>   <span data-ttu-id="22904-157">Nettobeløb: Den pris, som en kreditor har tilbudt efter fradrag af eventuelle rabatter, for varerne på linjen.</span><span class="sxs-lookup"><span data-stu-id="22904-157">Net amount: The price quoted by a vendor, after subtracting any discounts, for the items on the line.</span></span>   <span data-ttu-id="22904-158">Afvigelse: Det antal dage, hvormed leveringsdatoen i tilbudshovedet eller -linjen afviger fra den ønskede leveringsdato i tilbudsanmodningshovedet eller -linjen.</span><span class="sxs-lookup"><span data-stu-id="22904-158">Deviation: The number of days that the delivery date in the bid header or line deviates from the requested delivery date in the RFQ header or RFQ line.</span></span>   <span data-ttu-id="22904-159">Du kan angive en rangering for hvert bud.</span><span class="sxs-lookup"><span data-stu-id="22904-159">You can enter a rank for each bid.</span></span>  
4. <span data-ttu-id="22904-160">Vælg overskriftslinjen for det andet bud, du vil rangere.</span><span class="sxs-lookup"><span data-stu-id="22904-160">Select the header line for the other bid that you want to rank.</span></span>
5. <span data-ttu-id="22904-161">Angiv et tal i feltet Rang.</span><span class="sxs-lookup"><span data-stu-id="22904-161">In the Rank field, enter a number.</span></span>
6. <span data-ttu-id="22904-162">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="22904-162">Click Save.</span></span>

## <a name="reject-a-bid"></a><span data-ttu-id="22904-163">Afvise et bud</span><span class="sxs-lookup"><span data-stu-id="22904-163">Reject a bid</span></span>
1. <span data-ttu-id="22904-164">Vælg overskriftslinjen for det bud, du vil afvise.</span><span class="sxs-lookup"><span data-stu-id="22904-164">Select the header line for the bid that you want to reject.</span></span>
    * <span data-ttu-id="22904-165">Du kan kun acceptere, afvise eller returnere et bud eller linjer i et bud ad gangen.</span><span class="sxs-lookup"><span data-stu-id="22904-165">You can only accept, reject, or return one bid or lines within one bid at a time.</span></span>  
2. <span data-ttu-id="22904-166">Marker afkrydsningsfeltet Marker.</span><span class="sxs-lookup"><span data-stu-id="22904-166">Select the Mark check box.</span></span>
    * <span data-ttu-id="22904-167">Hvis du markerer afkrydsningsfeltet Marker i overskriften på et bud, markeres alle linjer.</span><span class="sxs-lookup"><span data-stu-id="22904-167">If you select the Mark check box on the Header of the bid then all the lines will be marked as well.</span></span> <span data-ttu-id="22904-168">Du kan også vælge at markere et undersæt af linjer i buddet for at afvise eller acceptere dem.</span><span class="sxs-lookup"><span data-stu-id="22904-168">You could also choose to mark a subset of the lines within the bid to reject or accept those.</span></span> <span data-ttu-id="22904-169">Det er muligt at acceptere én kreditors bud for nogle af linjerne i en tilbudsanmodning og derefter tildele andre linjer i en tilbudsanmodning til en anden kreditor, men du skal gøre dette i trin 2, et bud ad gangen.</span><span class="sxs-lookup"><span data-stu-id="22904-169">It’s possible to accept one vendor’s bid for some lines of an RFQ, and then award other RFQ lines to a different vendor, however you need to do this in 2 steps, one bid at a time.</span></span> <span data-ttu-id="22904-170">Hvis der findes alternative linjer, kan du kun acceptere den oprindelige budlinje eller dens alternativ, men ikke begge.</span><span class="sxs-lookup"><span data-stu-id="22904-170">If alternate lines are present, you can only accept either the original bid line or its alternate, but not both.</span></span>  
3. <span data-ttu-id="22904-171">Klik på Afvis.</span><span class="sxs-lookup"><span data-stu-id="22904-171">Click Reject.</span></span>
4. <span data-ttu-id="22904-172">Klik på Parametre for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="22904-172">Click Parameters to open the drop dialog.</span></span>
5. <span data-ttu-id="22904-173">Indtast eller vælg en værdi i feltet Årsag.</span><span class="sxs-lookup"><span data-stu-id="22904-173">In the Reason reject field, enter or select a value.</span></span>
    * <span data-ttu-id="22904-174">Årsagen til afvisningen gemmes i svaret.</span><span class="sxs-lookup"><span data-stu-id="22904-174">The reason for rejection will be stored on the reply.</span></span>  
6. <span data-ttu-id="22904-175">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="22904-175">Click OK.</span></span>
7. <span data-ttu-id="22904-176">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="22904-176">Click OK.</span></span>
8. <span data-ttu-id="22904-177">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="22904-177">Close the page.</span></span>
9. <span data-ttu-id="22904-178">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="22904-178">Close the page.</span></span>
10. <span data-ttu-id="22904-179">Opdater siden.</span><span class="sxs-lookup"><span data-stu-id="22904-179">Refresh the page.</span></span>

## <a name="accept-a-bid"></a><span data-ttu-id="22904-180">Acceptere et bud</span><span class="sxs-lookup"><span data-stu-id="22904-180">Accept a bid</span></span>
1. <span data-ttu-id="22904-181">Vælg det bud, du vil acceptere, og klik derefter på linket i feltet Tilbudsanmodning.</span><span class="sxs-lookup"><span data-stu-id="22904-181">Select the bid that you want to accept and then click the link in the Request for quotation field.</span></span>
2. <span data-ttu-id="22904-182">Klik på Svar i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="22904-182">On the Action Pane, click Reply.</span></span>
3. <span data-ttu-id="22904-183">Klik på Acceptér.</span><span class="sxs-lookup"><span data-stu-id="22904-183">Click Accept.</span></span>
    * <span data-ttu-id="22904-184">Hvis du har markeret bestemte linjer og ikke andre, vil accepten kun omfatte de markerede linjer.</span><span class="sxs-lookup"><span data-stu-id="22904-184">If you have marked specific lines and not others then the accept action will only include the marked lines.</span></span> <span data-ttu-id="22904-185">Hvis du vil acceptere alle linjer i et bud, behøver du ikke at markere linjerne.</span><span class="sxs-lookup"><span data-stu-id="22904-185">If you want to accept all lines on the bid then you do not have to mark the lines.</span></span>  
4. <span data-ttu-id="22904-186">Klik på Parametre for at åbne dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="22904-186">Click Parameters to open the drop dialog.</span></span>
    * <span data-ttu-id="22904-187">Dette gør det muligt at registrere en årsag for accepten af buddet.</span><span class="sxs-lookup"><span data-stu-id="22904-187">This allows you to record a reason for accepting the bid.</span></span> <span data-ttu-id="22904-188">Årsagen gemmes i buddet.</span><span class="sxs-lookup"><span data-stu-id="22904-188">The reason will be stored on the bid.</span></span>  
5. <span data-ttu-id="22904-189">Indtast eller vælg en værdi i feltet Årsag til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="22904-189">In the Reason accept field, enter or select a value.</span></span>
6. <span data-ttu-id="22904-190">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="22904-190">Click OK.</span></span>
7. <span data-ttu-id="22904-191">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="22904-191">Click OK.</span></span>
    * <span data-ttu-id="22904-192">Når du klikker på OK, genereres en indkøbsordre ud fra de linjer, der er inkluderet i accepten af tilbudsanmodningen.</span><span class="sxs-lookup"><span data-stu-id="22904-192">When you click OK this generates a purchase order based on the lines that are included in the RFQ acceptance.</span></span> <span data-ttu-id="22904-193">Hvis der er andre bud, der ikke er blevet behandlet (accepteret, afvist eller returneret), bliver du bedt om at afvise de resterende bud.</span><span class="sxs-lookup"><span data-stu-id="22904-193">If there are other bids that have not been processed (accepted, rejected, or returned) then the system will prompt you to reject the remaining bids.</span></span>  

## <a name="view-the-purchase-order-thats-been-generated"></a><span data-ttu-id="22904-194">Få vist den indkøbsordre, der bliver genereret</span><span class="sxs-lookup"><span data-stu-id="22904-194">View the purchase order that's been generated</span></span>
1. <span data-ttu-id="22904-195">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="22904-195">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="22904-196">Klik på indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="22904-196">Click Purchase order.</span></span>
    * <span data-ttu-id="22904-197">Her kan du se den indkøbsordre, der blev genereret, da du accepterede buddet.</span><span class="sxs-lookup"><span data-stu-id="22904-197">Here you can see the purchase order that was generated when you accepted the bid.</span></span>  
3. <span data-ttu-id="22904-198">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="22904-198">Close the page.</span></span>
4. <span data-ttu-id="22904-199">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="22904-199">Close the page.</span></span>
5. <span data-ttu-id="22904-200">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="22904-200">Close the page.</span></span>
6. <span data-ttu-id="22904-201">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="22904-201">Close the page.</span></span>


