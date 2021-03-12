---
title: Opret leveranceplan
description: Denne procedure viser, hvordan du opretter en leveranceplan til en salgsordre.
author: omulvad
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, SalesDeliverySchedule, SalesEditLines,  SrsReportViewerForm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: aa9539ce92297a3b4f22ac18af79fdea98759e49
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991834"
---
# <a name="create-delivery-schedule"></a><span data-ttu-id="0df4c-103">Opret leveranceplan</span><span class="sxs-lookup"><span data-stu-id="0df4c-103">Create delivery schedule</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="0df4c-104">Denne procedure viser, hvordan du opretter en leveranceplan til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="0df4c-104">This procedure demonstrates how to create a delivery schedule for a sales order.</span></span> <span data-ttu-id="0df4c-105">En leveranceplan bruges, når der anmodes om et antal i en ordre eller et tilbud, som skal leveres i flere leverancer.</span><span class="sxs-lookup"><span data-stu-id="0df4c-105">A delivery schedule is used when a quantity on an order or a quotation is requested to be delivered in multiple shipments.</span></span> <span data-ttu-id="0df4c-106">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="0df4c-106">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-delivery-schedule"></a><span data-ttu-id="0df4c-107">Opret leveranceplan</span><span class="sxs-lookup"><span data-stu-id="0df4c-107">Create delivery schedule</span></span>
1. <span data-ttu-id="0df4c-108">Gå til Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="0df4c-108">Go to All sales orders.</span></span>
2. <span data-ttu-id="0df4c-109">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0df4c-109">Click New.</span></span>
3. <span data-ttu-id="0df4c-110">Indtast eller vælg en værdi i feltet Kundekonto.</span><span class="sxs-lookup"><span data-stu-id="0df4c-110">In the Customer account field, enter or select a value.</span></span>
4. <span data-ttu-id="0df4c-111">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0df4c-111">Click OK.</span></span>
5. <span data-ttu-id="0df4c-112">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="0df4c-112">In the Item number field, enter or select a value.</span></span>
6. <span data-ttu-id="0df4c-113">Skriv et tal, der er større end 1, i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="0df4c-113">In the Quantity field, enter a number that is bigger than 1.</span></span>
7. <span data-ttu-id="0df4c-114">Klik på Salgsordrelinje.</span><span class="sxs-lookup"><span data-stu-id="0df4c-114">Click Sales order line.</span></span>
8. <span data-ttu-id="0df4c-115">Klik på Leveranceplan.</span><span class="sxs-lookup"><span data-stu-id="0df4c-115">Click Delivery schedule.</span></span>
    * <span data-ttu-id="0df4c-116">Siden Leveranceplan er det sted, hvor du kan angive antallet af leverancer, hvor det samlede antal på ordrelinjen leveres til kunden.</span><span class="sxs-lookup"><span data-stu-id="0df4c-116">The Delivery schedule page is the place where you can specify the number of shipments in which the total quantity of the order line will be delivered to the customer.</span></span>    
    * <span data-ttu-id="0df4c-117">Som standard kopieres det samlede antal og andre leveringsoplysninger for den oprindelige salgslinje til den første linje i leveranceplanen.</span><span class="sxs-lookup"><span data-stu-id="0df4c-117">By default, the system copies the total quantity and other delivery details of the original sales line into the first delivery schedule line.</span></span> <span data-ttu-id="0df4c-118">I dette eksempel skal vi oprette en tidsplan for to forsendelser, hvor datoen for den anden forsendelse er forskudt en uge i forhold til den første.</span><span class="sxs-lookup"><span data-stu-id="0df4c-118">In this example, we'll create a schedule for two shipments, with the second shipment's date offset by a week from the first one.</span></span>  
9. <span data-ttu-id="0df4c-119">Angiv et tal, der er en del af det samlede antal, i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="0df4c-119">In the Quantity field, enter a number that is part of the total quantity.</span></span>
10. <span data-ttu-id="0df4c-120">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="0df4c-120">Click New.</span></span>
11. <span data-ttu-id="0df4c-121">Angiv det resterende antal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="0df4c-121">In the Quantity field, enter the remaining quantity.</span></span>
12. <span data-ttu-id="0df4c-122">Angiv en dato, der ligger en uge før datoen for den første leverancelinje, i feltet Ønsket afsendelsesdato.</span><span class="sxs-lookup"><span data-stu-id="0df4c-122">In the Requested ship date field, enter a date a date that is one week ahead from the date of the first delivery line.</span></span>
    * <span data-ttu-id="0df4c-123">De to indstillinger på oversigtspanelet Gebyrkonvertering styrer, hvordan gebyrerne skal fordeles på linjerne i leveranceplanen, når de er blevet tildelt til den oprindelige ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="0df4c-123">The two options on the Charges conversion FastTab control how you want the charges to be distributed across the delivery schedule lines, once they've been assigned to the original order line.</span></span> <span data-ttu-id="0df4c-124">Hvis du vælger Kopier bruttobeløb, kopieres samme gebyrbeløb til hver linje.</span><span class="sxs-lookup"><span data-stu-id="0df4c-124">If you select Copy gross amounts, the same charge amount is copied to each line.</span></span> <span data-ttu-id="0df4c-125">Indstillingen Fordel på leveringslinjer opdeler gebyrer ligeligt på leverancelinjerne.</span><span class="sxs-lookup"><span data-stu-id="0df4c-125">The Allocate to delivery lines option divides the charge equally across the delivery lines.</span></span>  
    * <span data-ttu-id="0df4c-126">Det er kun faste gebyrer, der kan opdeles, mens variable gebyrer stadig skal kopieres til linjerne.</span><span class="sxs-lookup"><span data-stu-id="0df4c-126">Only fixed charges can be divided, whereas variable charges will still be copied to the lines.</span></span>  
13. <span data-ttu-id="0df4c-127">Flyt markøren væk fra den anden leverancelinje for at opdatere siden.</span><span class="sxs-lookup"><span data-stu-id="0df4c-127">Move the cursor away from the second delivery line to update the page.</span></span>
    * <span data-ttu-id="0df4c-128">Du kan holde styr på det samlede antal, der er allokeret til linjerne i leveranceplanen, ved at se felterne Total og Resterende.</span><span class="sxs-lookup"><span data-stu-id="0df4c-128">You can keep track of the total quantity that's allocated to the delivery schedule lines by looking at the Total and Remaining fields.</span></span> <span data-ttu-id="0df4c-129">Når det resterende antal er nul, er det fulde antal fra den oprindelige linje blevet allokeret til tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="0df4c-129">When the remaining quantity is zero, the full quantity from the original line has been allocated to the schedule.</span></span>   
14. <span data-ttu-id="0df4c-130">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0df4c-130">Click OK.</span></span>
    * <span data-ttu-id="0df4c-131">Leveranceplanen er nu kopieret til ordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="0df4c-131">The delivery schedule has now been copied to the order lines.</span></span>   
    * <span data-ttu-id="0df4c-132">Den oprindelige ordrelinje, kaldet en kommerciel linje, er konverteret til en ordrelinje med flere leverancer.</span><span class="sxs-lookup"><span data-stu-id="0df4c-132">The original order line, referred to as a Commercial line, has been converted to an Order line with multiple deliveries.</span></span> <span data-ttu-id="0df4c-133">Den er markeret med et tydeligt ikon og fungerer som overskrift for leveringslinjerne.</span><span class="sxs-lookup"><span data-stu-id="0df4c-133">It is marked with a distinct icon and acts as a header for the delivery lines.</span></span>  
    * <span data-ttu-id="0df4c-134">De to nye linjer, kaldet leverancelinjer, udgør én leveranceplan.</span><span class="sxs-lookup"><span data-stu-id="0df4c-134">The two new lines, referred to as delivery lines, make up one delivery schedule.</span></span> <span data-ttu-id="0df4c-135">Ordren behandles mod disse linjer og ikke mod den oprindelige linje.</span><span class="sxs-lookup"><span data-stu-id="0df4c-135">The order will be processed against these lines and not the original line.</span></span> <span data-ttu-id="0df4c-136">Hvis dokumenter som bekræftelse af sedler, pluklister, følgesedler eller fakturaer udskrives, vises kun leverancelinjerne.</span><span class="sxs-lookup"><span data-stu-id="0df4c-136">If documents such as confirmation slips, picking lists, packing slips, or invoices are printed, only the delivery lines are shown.</span></span>   
    * <span data-ttu-id="0df4c-137">Leverancelinjerne kan have forskellige leveringsdatoer, antal, leveringsmåder og lagringsdimensioner, som f.eks. sted og lagersted.</span><span class="sxs-lookup"><span data-stu-id="0df4c-137">The delivery lines can have different delivery dates, quantities, modes of delivery, and storage dimensions, such as site and warehouse.</span></span> <span data-ttu-id="0df4c-138">Dog skal altid svarer til dem på linjen kommercielle produktdimensionerne, og kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="0df4c-138">However, the product dimensions must always match the ones on the commercial line and can't be changed.</span></span>  
15. <span data-ttu-id="0df4c-139">Skriv et tal, der er større end det aktuelle tal, i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="0df4c-139">In the Quantity field, enter a number that's bigger than the current one.</span></span>
16. <span data-ttu-id="0df4c-140">Vælg den kommercielle linje for at se effekten af genberegningen af antallet.</span><span class="sxs-lookup"><span data-stu-id="0df4c-140">Select the commercial line to see the effect of the quantity recalculation.</span></span>
17. <span data-ttu-id="0df4c-141">Klik på fanen Pluk og pak i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="0df4c-141">On the Action Pane, click Pick and pack.</span></span>
18. <span data-ttu-id="0df4c-142">Klik på Bogfør følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="0df4c-142">Click Post packing slip.</span></span>
19. <span data-ttu-id="0df4c-143">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="0df4c-143">Expand the Parameters section.</span></span>
20. <span data-ttu-id="0df4c-144">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="0df4c-144">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="0df4c-145">Bemærk, at følgesedlen oprettes for de to linjer i leveranceplanen og ikke den oprindelige ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="0df4c-145">Note that the packing slip will be created for the two delivery schedule lines and not the original order line.</span></span>  
21. <span data-ttu-id="0df4c-146">Vælg Ja i feltet Udskriv følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="0df4c-146">Select Yes in the Print packing slip field.</span></span>
22. <span data-ttu-id="0df4c-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="0df4c-147">Click OK.</span></span>
23. <span data-ttu-id="0df4c-148">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="0df4c-148">Click Yes.</span></span>
24. <span data-ttu-id="0df4c-149">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="0df4c-149">Close the page.</span></span>
