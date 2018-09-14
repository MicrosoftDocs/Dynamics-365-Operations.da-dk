--- 
title: Sende salgsordrer uden lagerstyring
description: "Denne vejledning viser, hvordan du opdaterer en salgsordre, når varerne er afsendt til kunden."
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: ae70e09dbc4da90b7d1802d076384eae2d00da0e
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="3de24-103">Sende salgsordrer uden lagerstyring</span><span class="sxs-lookup"><span data-stu-id="3de24-103">Ship sales orders without warehousing</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3de24-104">Denne vejledning viser, hvordan du opdaterer en salgsordre, når varerne er afsendt til kunden.</span><span class="sxs-lookup"><span data-stu-id="3de24-104">This guide demonstrates how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="3de24-105">Vejledningen gælder for den opfyldelsesstrøm, der ikke er konfigureret for lagerstedsstyring (hverken grundlæggende eller avancerede lagerfunktioner) og derfor ikke kræver, at produktplukning registreres før afsendelse.</span><span class="sxs-lookup"><span data-stu-id="3de24-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="3de24-106">Du kan køre procedure på dine egne data eller i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="3de24-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="3de24-107">I begge tilfælde skal du, før du starter denne opgave, oprette en salgsordre for et lagerført produkt med et antal større end 1.</span><span class="sxs-lookup"><span data-stu-id="3de24-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="3de24-108">For at undgå en bogføringsfejl skal du kontrollere, at produktets disponible antal i lokationen og på lagerstedet, som du har valgt i ordren, dækker ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="3de24-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you’ve selected on the order covers the order quantity.</span></span>


## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="3de24-109">Bogføre følgeseddel for en ordre</span><span class="sxs-lookup"><span data-stu-id="3de24-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="3de24-110">Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="3de24-110">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="3de24-111">Find og vælg den ordre på listen, du har oprettet til denne opgave.</span><span class="sxs-lookup"><span data-stu-id="3de24-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="3de24-112">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3de24-112">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3de24-113">Klik på fanen Pluk og pak i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3de24-113">On the Action Pane, click Pick and pack.</span></span>
5. <span data-ttu-id="3de24-114">Klik på Bogfør følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="3de24-114">Click Post packing slip.</span></span>
6. <span data-ttu-id="3de24-115">Udvid eller skjul sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="3de24-115">Expand or collapse the Parameters section.</span></span>
7. <span data-ttu-id="3de24-116">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="3de24-116">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="3de24-117">Andre muligheder omfatter Levér nu og Plukket.</span><span class="sxs-lookup"><span data-stu-id="3de24-117">Other options include Deliver now and Picked.</span></span> <span data-ttu-id="3de24-118">Hvis ordrelinjen er delvist leveret og feltet Levér nu på ordrelinjen indeholder en mængde, skal du vælge Levér nu.</span><span class="sxs-lookup"><span data-stu-id="3de24-118">If the order line is to be shipped partially and the Deliver now field on the order line contains a quantity, you would select Deliver now.</span></span> <span data-ttu-id="3de24-119">Hvis din organisations opfyldelsesstrøm indeholder pluk som en separat proces, der styres af og registreres i en plukliste, skal du vælge Plukket.</span><span class="sxs-lookup"><span data-stu-id="3de24-119">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select Picked.</span></span>  
    * <span data-ttu-id="3de24-120">Kontroller, at indstillingen Bogføring er indstillet til Ja.</span><span class="sxs-lookup"><span data-stu-id="3de24-120">Check that the Posting option is set to Yes.</span></span>  
8. <span data-ttu-id="3de24-121">Sæt indstillingen Udskriv følgeseddel til Ja.</span><span class="sxs-lookup"><span data-stu-id="3de24-121">Set the Print packing slip option to Yes.</span></span>
    * <span data-ttu-id="3de24-122">Fanen Oversigt indeholder en liste over følgesedler, der skal genereres i denne postering.</span><span class="sxs-lookup"><span data-stu-id="3de24-122">The Overview tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="3de24-123">Hvis du leverer en enkelt ordre, vil der typisk være én følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="3de24-123">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="3de24-124">Men hvis denne ordres linjer skal leveres fra forskellige steder, opdeles bogføringen automatisk i det rette antal dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3de24-124">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="3de24-125">Dette er en obligatorisk betingelse, der ikke kan ændres.</span><span class="sxs-lookup"><span data-stu-id="3de24-125">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="3de24-126">På samme måde opdeles bogføringen også i flere dokumenter, hvis ordrelinjerne skal leveres til forskellige leveringsadresser, og politikken for levering er indstillet til at kræve en opdeling.</span><span class="sxs-lookup"><span data-stu-id="3de24-126">Similarly, the posting will also be split into multiple documents if the order’s lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
9. <span data-ttu-id="3de24-127">Vælg rækken for ordrelinjen, der skal sendes, under fanen Linjer.</span><span class="sxs-lookup"><span data-stu-id="3de24-127">On the Lines tab, select the row for the order line to be shipped.</span></span>
10. <span data-ttu-id="3de24-128">Skriv et tal, der er lavere end den oprindelige mængde, i feltet Opdater.</span><span class="sxs-lookup"><span data-stu-id="3de24-128">In the Update field, enter a number lower than the original quantity.</span></span>
11. <span data-ttu-id="3de24-129">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="3de24-129">Click OK.</span></span>
12. <span data-ttu-id="3de24-130">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="3de24-130">Click Yes.</span></span>
13. <span data-ttu-id="3de24-131">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3de24-131">Close the page.</span></span>
14. <span data-ttu-id="3de24-132">Klik på Indstillinger i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3de24-132">On the Action Pane, click Options.</span></span>
15. <span data-ttu-id="3de24-133">Klik på Skift visning.</span><span class="sxs-lookup"><span data-stu-id="3de24-133">Click Change view.</span></span>
16. <span data-ttu-id="3de24-134">Klik på Overskriftsvisning.</span><span class="sxs-lookup"><span data-stu-id="3de24-134">Click Header view.</span></span>
    * <span data-ttu-id="3de24-135">Hvis alle linjer i ordren er fuldt leveret, ændres ordrestatus fra åben til leveret.</span><span class="sxs-lookup"><span data-stu-id="3de24-135">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    * <span data-ttu-id="3de24-136">I dette eksempel er ordrelinjen leveret delvist.</span><span class="sxs-lookup"><span data-stu-id="3de24-136">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="3de24-137">Det er grunden til, at ordrestatus forbliver åben.</span><span class="sxs-lookup"><span data-stu-id="3de24-137">This is why the the order status remains Open.</span></span>     
    * <span data-ttu-id="3de24-138">Feltet Dokumentstatus er indstillet til Følgeseddel, fordi mindst én af ordrelinjerne er blevet leveret.</span><span class="sxs-lookup"><span data-stu-id="3de24-138">The Document status field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
17. <span data-ttu-id="3de24-139">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3de24-139">On the Action Pane, click General.</span></span>
18. <span data-ttu-id="3de24-140">Klik på Linjeantal.</span><span class="sxs-lookup"><span data-stu-id="3de24-140">Click Line quantity.</span></span>
19. <span data-ttu-id="3de24-141">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3de24-141">Close the page.</span></span>
20. <span data-ttu-id="3de24-142">Klik på fanen Pluk og pak i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3de24-142">On the Action Pane, click Pick and pack.</span></span>
21. <span data-ttu-id="3de24-143">Klik på følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="3de24-143">Click Packing slip.</span></span>
    * <span data-ttu-id="3de24-144">Siden Følgeseddelkladde indeholder alle følgeseddeldokumenter, der oprettes for din ordre.</span><span class="sxs-lookup"><span data-stu-id="3de24-144">The Packing slip journal page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="3de24-145">Du kan gennemse detaljerne for hvert dokument og udskrive dem, hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="3de24-145">You can review details of each document and print them, if you wish.</span></span>  


