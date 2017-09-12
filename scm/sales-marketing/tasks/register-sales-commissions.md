--- 
title: Registrere salgskommissioner
description: Denne procedure viser, hvordan salgsprovisioner beregnes og registreres.
author: omulvad
manager: AnnBe
ms.date: 11/10/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: kfend
ms.search.scope: Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: f195f9e466eab3cf87afea2b5d430d0ea25c5a83
ms.contentlocale: da-dk
ms.lasthandoff: 08/29/2017

---
# <a name="register-sales-commissions"></a><span data-ttu-id="4a9c5-103">Registrere salgskommissioner</span><span class="sxs-lookup"><span data-stu-id="4a9c5-103">Register sales commissions</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4a9c5-104">Denne procedure viser, hvordan salgsprovisioner beregnes og registreres.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-104">This procedure shows you how sales commissions are calculated and registered.</span></span> <span data-ttu-id="4a9c5-105">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-105">You can run this procedure in demo data company USMF or on your own data.</span></span> <span data-ttu-id="4a9c5-106">Før du starter denne vejledning, skal du køre vejledningen "Konfigurer regler for salgsprovision" for at sikre, at du har den nødvendige provisionsberegningsopsætning.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-106">Before starting this guide, run the guide called "Set up sales commission rules" to make sure that you have all the necessary commission calculation setup.</span></span>

<span data-ttu-id="4a9c5-107">Notér de kunde- og varenumre, du har valgt til provisionsprocessen, og brug dem, når du bliver bedt om at oprette en salgsordre i denne vejledning.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-107">Take note of the customer and item numbers that you have chosen for the commission process and use them when asked to create a sales order in this guide.</span></span>


## <a name="invoice-a-sales-order-that-qualifies-a-salesperson-for-a-commission"></a><span data-ttu-id="4a9c5-108">Fakturere en salgsordre, der kvalificerer en sælger til en provision</span><span class="sxs-lookup"><span data-stu-id="4a9c5-108">Invoice a sales order that qualifies a salesperson for a commission</span></span>
1. <span data-ttu-id="4a9c5-109">Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="4a9c5-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-110">Click New.</span></span>
3. <span data-ttu-id="4a9c5-111">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="4a9c5-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="4a9c5-113">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-113">In the list, click the link in the selected row.</span></span>
6. <span data-ttu-id="4a9c5-114">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-114">Click OK.</span></span>
7. <span data-ttu-id="4a9c5-115">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-115">On the Action Pane, click Options.</span></span>
8. <span data-ttu-id="4a9c5-116">Klik på Skift visning.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-116">Click Change view.</span></span>
9. <span data-ttu-id="4a9c5-117">Klik på Overskriftsvisning.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-117">Click Header view.</span></span>
10. <span data-ttu-id="4a9c5-118">Udvid sektionen Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-118">Expand the Setup section.</span></span>
    * <span data-ttu-id="4a9c5-119">Værdien i feltet Salg repræsenterer en gruppe med en eller flere sælgere, der knyttet til den.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-119">The value in the Sales group field represents a group with one or more sales representatives assigned to it.</span></span> <span data-ttu-id="4a9c5-120">Personerne i gruppen er dem, der modtager provision, når ordren faktureres i henhold til foruddefinerede satser og fordeling.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-120">The people in the group are the ones who will receive commissions when the order is invoiced, as per predefined rates and distribution.</span></span>   <span data-ttu-id="4a9c5-121">Værdien kopieres fra kundekortet, men du kan ændre den, hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-121">The value is copied from the Customer card, but you can change it if you wish.</span></span>  <span data-ttu-id="4a9c5-122">Gruppen Salg kopieres også til salgsordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-122">The Sales group is also copied to the sales order line.</span></span> <span data-ttu-id="4a9c5-123">Du kan ændre den, så den er anderledes end den i hovedet og/eller mellem linjerne.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-123">You can change it so that it can differ from the one in the header and/or between lines.</span></span>  
    * <span data-ttu-id="4a9c5-124">Værdien i feltet Provisionsgruppe repræsenterer en gruppe, du har oprettet for en eller flere kunder med det formål at spore provisioner.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-124">The value in the Commission group field represents a group that you have created for one or more customers with the purpose of tracking commissions.</span></span>   <span data-ttu-id="4a9c5-125">Værdien kopieres fra kundekortet, men du kan ændre den, hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-125">The value is copied from the Customer card, but you can change it if you wish.</span></span>   
11. <span data-ttu-id="4a9c5-126">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-126">On the Action Pane, click Options.</span></span>
12. <span data-ttu-id="4a9c5-127">Klik på Skift visning.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-127">Click Change view.</span></span>
13. <span data-ttu-id="4a9c5-128">Klik på Linjevisning.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-128">Click Line view.</span></span>
14. <span data-ttu-id="4a9c5-129">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-129">In the Item number field, click the drop-down button to open the lookup.</span></span>
15. <span data-ttu-id="4a9c5-130">Vælg den vare, du har angivet for provisioner, på listen.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-130">In the list, select the item you have set up for commissions.</span></span> 
16. <span data-ttu-id="4a9c5-131">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-131">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="4a9c5-132">Bemærk linjens nettobeløb.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-132">Take note of the line's Net amount.</span></span> <span data-ttu-id="4a9c5-133">Det repræsenterer salgsindtægter, som i dette eksempel danner grundlag for provisionsberegningen.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-133">It represents the sales revenue, which in this example is the basis for commission calculation.</span></span>  
17. <span data-ttu-id="4a9c5-134">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-134">Click Save.</span></span>
18. <span data-ttu-id="4a9c5-135">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-135">On the Action Pane, click Invoice.</span></span>
19. <span data-ttu-id="4a9c5-136">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-136">Click Invoice.</span></span>
20. <span data-ttu-id="4a9c5-137">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-137">Expand the Parameters section.</span></span>
21. <span data-ttu-id="4a9c5-138">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-138">In the Quantity field, select 'All'.</span></span>
22. <span data-ttu-id="4a9c5-139">Vælg Ja i feltet Bogføring.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-139">Select Yes in the Posting field.</span></span>
23. <span data-ttu-id="4a9c5-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-140">Click OK.</span></span>
24. <span data-ttu-id="4a9c5-141">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-141">Click OK.</span></span>
    * <span data-ttu-id="4a9c5-142">Det kan tage omkring et minut at bogføre transaktionen.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-142">It may take a minute or so to post the transaction.</span></span> <span data-ttu-id="4a9c5-143">Vent på, at behandlingen fuldføres, og luk ikke siden.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-143">Allow the processing to complete and don’t close the page.</span></span>  

## <a name="review-the-registered-sales-commissions"></a><span data-ttu-id="4a9c5-144">Gennemse de registrerede salgsprovisioner</span><span class="sxs-lookup"><span data-stu-id="4a9c5-144">Review the registered sales commissions</span></span>
1. <span data-ttu-id="4a9c5-145">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-145">On the Action Pane, click Invoice.</span></span>
2. <span data-ttu-id="4a9c5-146">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-146">Click Invoice.</span></span>
3. <span data-ttu-id="4a9c5-147">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-147">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="4a9c5-148">Klik på Provisionsposter.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-148">Click Commission transactions.</span></span>
    * <span data-ttu-id="4a9c5-149">Fanen Oversigt viser linjer, der repræsenterer provisionsbeløb, der skal betales til sælgere, der er knyttet til fakturerede salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-149">The Overview tab displays lines representing the commission amounts payable to sales representatives who are associated with the invoiced sales order.</span></span> <span data-ttu-id="4a9c5-150">Lad os se nærmere på det.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-150">Let's review the details.</span></span>     
    * <span data-ttu-id="4a9c5-151">Hvis du har brugt guiden "Konfigurer regler for salgsprovision" til at konfigurere provisionssalgsgruppen, er der to sælgere, som skal modtage en salgsprovision, og provisionen deles ligeligt mellem dem.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-151">If you used the "Set up sales commission rules" guide to set up the Commission sales group, there are two sales people to receive a sales commissions, and the commission is split equally between them.</span></span>  
    * <span data-ttu-id="4a9c5-152">I dette eksempel beregnes det samlede provisionsbeløb som en procentdel af salgsindtægterne (nettobeløbet på ordrelinjen).</span><span class="sxs-lookup"><span data-stu-id="4a9c5-152">In this example, the total amount of the commission is calculated as a percentage of the sales revenue (the net amount of order line).</span></span>   
5. <span data-ttu-id="4a9c5-153">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-153">Close the page.</span></span>
6. <span data-ttu-id="4a9c5-154">Klik på Bilag.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-154">Click Voucher.</span></span>
    * <span data-ttu-id="4a9c5-155">Du kan gennemgå bilagsposteringer for provisionsbeløb, der er bogført til de foruddefinerede provisionsudgifts- og -kreditorkonti.</span><span class="sxs-lookup"><span data-stu-id="4a9c5-155">You can review the voucher transactions for the commission amounts that have been posted to the predefined commission expense and commission payable accounts.</span></span>  


