---
title: Sende salgsordrer uden lagerstyring
description: I dette emne beskrives, hvordan du opdaterer en salgsordre, når varerne er afsendt til kunden.
author: omulvad
manager: tfehr
ms.date: 08/20/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesTable, SalesEditLines,  SrsReportViewerForm, SalesTableLineQuantity, CustPackingSlipJournal
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9a2079ae02c01d30eb648e9cc95ee9cf6599048b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5205875"
---
# <a name="ship-sales-orders-without-warehousing"></a><span data-ttu-id="3cda3-103">Sende salgsordrer uden lagerstyring</span><span class="sxs-lookup"><span data-stu-id="3cda3-103">Ship sales orders without warehousing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cda3-104">I dette emne beskrives, hvordan du opdaterer en salgsordre, når varerne er afsendt til kunden.</span><span class="sxs-lookup"><span data-stu-id="3cda3-104">This topic explains how to update a sales order when products are shipped to the customer.</span></span> <span data-ttu-id="3cda3-105">Vejledningen gælder for den opfyldelsesstrøm, der ikke er konfigureret for lagerstedsstyring (hverken grundlæggende eller avancerede lagerfunktioner) og derfor ikke kræver, at produktplukning registreres før afsendelse.</span><span class="sxs-lookup"><span data-stu-id="3cda3-105">The guide is applicable to the fulfillment flow that is not set up for warehouse management (neither basic or advanced warehousing), and therefore does not require product picking to be registered before shipment.</span></span> <span data-ttu-id="3cda3-106">Du kan køre procedure på dine egne data eller i demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="3cda3-106">You can run this procedure on your own data or in demo data company USMF.</span></span> <span data-ttu-id="3cda3-107">I begge tilfælde skal du, før du starter denne opgave, oprette en salgsordre for et lagerført produkt med et antal større end 1.</span><span class="sxs-lookup"><span data-stu-id="3cda3-107">In both cases, before you start this task, create a sales order for an inventoried product with a quantity of greater than 1.</span></span> <span data-ttu-id="3cda3-108">For at undgå en bogføringsfejl skal du kontrollere, at produktets disponible antal i lokationen og på lagerstedet, som du har valgt i ordren, dækker ordreantallet.</span><span class="sxs-lookup"><span data-stu-id="3cda3-108">To avoid a posting error, you need to check that the product's on-hand quantity in the site and warehouse that you've selected on the order covers the order quantity.</span></span>

## <a name="post-packing-slip-for-an-order"></a><span data-ttu-id="3cda3-109">Bogføre følgeseddel for en ordre</span><span class="sxs-lookup"><span data-stu-id="3cda3-109">Post packing slip for an order</span></span>
1. <span data-ttu-id="3cda3-110">Gå til **Moduler > Salg og marketing > Salgsordrer > Alle salgsordrer** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="3cda3-110">In the navigation pane, go to **Modules > Sales and marketing > Sales orders > All sales orders**.</span></span>
2. <span data-ttu-id="3cda3-111">Find og vælg den ordre på listen, du har oprettet til denne opgave.</span><span class="sxs-lookup"><span data-stu-id="3cda3-111">In the list, find and select the order you have created for this task.</span></span>
3. <span data-ttu-id="3cda3-112">Vælg **Pluk og pak** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3cda3-112">On the Action Pane, select **Pick and pack**.</span></span>
4. <span data-ttu-id="3cda3-113">Vælg **Bogfør følgeseddel**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-113">Select **Post packing slip**.</span></span>
5. <span data-ttu-id="3cda3-114">Udvid eller skjul sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-114">Expand or collapse the **Parameters** section.</span></span>
6. <span data-ttu-id="3cda3-115">Vælg **Alle**" i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-115">In the **Quantity** field, select **All**.</span></span>
    - <span data-ttu-id="3cda3-116">Andre muligheder omfatter **Levér nu** og **Plukket**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-116">Other options include **Deliver now** and **Picked**.</span></span> <span data-ttu-id="3cda3-117">Hvis ordrelinjen er delvist leveret og feltet **Levér nu** på ordrelinjen indeholder en mængde, skal du vælge **Levér nu**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-117">If the order line is to be shipped partially and the **Deliver now** field on the order line contains a quantity, you would select **Deliver now**.</span></span> <span data-ttu-id="3cda3-118">Hvis din organisations opfyldelsesstrøm indeholder pluk som en separat proces, der styres af og registreres i en plukliste, skal du vælge **Plukket**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-118">If your organization's fulfillment flow includes picking as a separate process that is managed by and registered with a picking list, you would select **Picked**.</span></span>  
    - <span data-ttu-id="3cda3-119">Kontroller, at indstillingen **Bogføring** er indstillet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-119">Check that the **Posting** option is set to **Yes**.</span></span>  
7. <span data-ttu-id="3cda3-120">Sæt indstillingen **Udskriv følgeseddel** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-120">Set the **Print packing slip** option to **Yes**.</span></span> <span data-ttu-id="3cda3-121">Fanen **Oversigt** indeholder en liste over følgesedler, der skal genereres i denne postering.</span><span class="sxs-lookup"><span data-stu-id="3cda3-121">The **Overview** tab contains a list of packing slips to be generated in this posting.</span></span> <span data-ttu-id="3cda3-122">Hvis du leverer en enkelt ordre, vil der typisk være én følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="3cda3-122">If you are shipping an individual order, there will typically be one packing slip.</span></span> <span data-ttu-id="3cda3-123">Men hvis denne ordres linjer skal leveres fra forskellige steder, opdeles bogføringen automatisk i det rette antal dokumenter.</span><span class="sxs-lookup"><span data-stu-id="3cda3-123">However, if that order's lines are to be shipped from different sites, posting will automatically be split into the appropriate number of documents.</span></span> <span data-ttu-id="3cda3-124">Dette er en obligatorisk betingelse, der ikke kan ændres.</span><span class="sxs-lookup"><span data-stu-id="3cda3-124">This is a mandatory condition that cannot be changed.</span></span> <span data-ttu-id="3cda3-125">På samme måde opdeles bogføringen også i flere dokumenter, hvis ordrelinjerne skal leveres til forskellige leveringsadresser, og politikken for levering er indstillet til at kræve en opdeling.</span><span class="sxs-lookup"><span data-stu-id="3cda3-125">Similarly, the posting will also be split into multiple documents if the order's lines are to be shipped to different delivery addresses, and the shipping policy is set up to require a split.</span></span>  
8. <span data-ttu-id="3cda3-126">Vælg rækken for ordrelinjen, der skal sendes, under fanen **Linjer**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-126">On the **Lines** tab, select the row for the order line to be shipped.</span></span>
9. <span data-ttu-id="3cda3-127">Skriv et tal, der er lavere end den oprindelige mængde, i feltet **Opdater**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-127">In the **Update** field, enter a number lower than the original quantity.</span></span>
10. <span data-ttu-id="3cda3-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-128">Select **OK**.</span></span>
11. <span data-ttu-id="3cda3-129">Vælg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-129">Select **Yes**.</span></span>
12. <span data-ttu-id="3cda3-130">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3cda3-130">Close the page.</span></span>
13. <span data-ttu-id="3cda3-131">Vælg **Indstillinger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3cda3-131">On the Action Pane, select **Options**.</span></span>
14. <span data-ttu-id="3cda3-132">Vælg **Skift visning**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-132">Select **Change view**.</span></span>
15. <span data-ttu-id="3cda3-133">Vælg **Overskriftsvisning**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-133">Select **Header view**.</span></span>
    - <span data-ttu-id="3cda3-134">Hvis alle linjer i ordren er fuldt leveret, ændres ordrestatus fra åben til leveret.</span><span class="sxs-lookup"><span data-stu-id="3cda3-134">If all of the lines on the order have been fully shipped, the order status changes from Open to Delivered.</span></span>  
    - <span data-ttu-id="3cda3-135">I dette eksempel er ordrelinjen leveret delvist.</span><span class="sxs-lookup"><span data-stu-id="3cda3-135">In this example, the order line has been shipped partially.</span></span> <span data-ttu-id="3cda3-136">Det er grunden til, at ordrestatus forbliver åben.</span><span class="sxs-lookup"><span data-stu-id="3cda3-136">This is why the the order status remains Open.</span></span>     
    - <span data-ttu-id="3cda3-137">Feltet **Dokumentstatus** er indstillet til Følgeseddel, fordi mindst én af ordrelinjerne er blevet leveret.</span><span class="sxs-lookup"><span data-stu-id="3cda3-137">The **Document status** field is set to Packing slip because at least one of the order lines have been shipped.</span></span>  
16. <span data-ttu-id="3cda3-138">Vælg **Generelt** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3cda3-138">On the Action Pane, select **General**.</span></span>
17. <span data-ttu-id="3cda3-139">Vælg **Linjeantal**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-139">Select **Line quantity**.</span></span>
18. <span data-ttu-id="3cda3-140">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="3cda3-140">Close the page.</span></span>
19. <span data-ttu-id="3cda3-141">Vælg **Pluk og pak** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="3cda3-141">On the Action Pane, select **Pick and pack**.</span></span>
20. <span data-ttu-id="3cda3-142">Vælg **Følgeseddel**.</span><span class="sxs-lookup"><span data-stu-id="3cda3-142">Select **Packing slip**.</span></span> <span data-ttu-id="3cda3-143">Siden **Følgeseddelkladde** indeholder alle følgeseddeldokumenter, der oprettes for din ordre.</span><span class="sxs-lookup"><span data-stu-id="3cda3-143">The **Packing slip journal** page contains all the packing slip documents that were generated for your order.</span></span> <span data-ttu-id="3cda3-144">Du kan gennemse detaljerne for hvert dokument og udskrive dem, hvis du ønsker.</span><span class="sxs-lookup"><span data-stu-id="3cda3-144">You can review details of each document and print them, if you wish.</span></span>  



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]