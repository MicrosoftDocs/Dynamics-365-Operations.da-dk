---
title: Oprette en indkøbsordre fra en salgsordre
description: Denne procedure viser, hvordan du kan oprette en indkøbsordre, der er baseret på en salgsordre.
author: omulvad
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesCreateOrder, SalesTable, PurchCreateFromSalesOrder, VendAccountItemLookup, SalesTableReferences, PurchTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: omulvad
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 7991476b86ace92cda513ae8906c62ba7fbbe915
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "325750"
---
# <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="42d44-103">Oprette en indkøbsordre fra en salgsordre</span><span class="sxs-lookup"><span data-stu-id="42d44-103">Create a purchase order from a sales order</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="42d44-104">Denne procedure viser, hvordan du kan oprette en indkøbsordre, der er baseret på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="42d44-104">This procedure shows you how to create a purchase order that is based on a sales order.</span></span> <span data-ttu-id="42d44-105">Produktmængderne på indkøbsordren angives derefter for at imødekomme efterspørgslen i den oprindelige salgsordre.</span><span class="sxs-lookup"><span data-stu-id="42d44-105">The product's quantities on the purchase order are then designated to fulfill the demand of the originating sales order.</span></span> <span data-ttu-id="42d44-106">Opfyldelse af salgsbehovet på denne måde er et alternativ til en mere omfattende og optimeret metode til planlægning af distributionskrav.</span><span class="sxs-lookup"><span data-stu-id="42d44-106">Fulfilling sales demand this way is an alternative to a more comprehensive and optimized method of Distribution Requirements Planning.</span></span> <span data-ttu-id="42d44-107">Du kan køre denne procedure på dit eget demodatafirma USMF eller på dine egne data.</span><span class="sxs-lookup"><span data-stu-id="42d44-107">You can run this procedure in demo data company USMF or on your own data.</span></span>


## <a name="create-a-purchase-order-from-a-sales-order"></a><span data-ttu-id="42d44-108">Oprette en indkøbsordre fra en salgsordre</span><span class="sxs-lookup"><span data-stu-id="42d44-108">Create a purchase order from a sales order</span></span>
1. <span data-ttu-id="42d44-109">Gå til Salg og marketing > Salgsordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="42d44-109">Go to Sales and marketing > Sales orders > All sales orders.</span></span>
2. <span data-ttu-id="42d44-110">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="42d44-110">Click New.</span></span>
3. <span data-ttu-id="42d44-111">Klik på rullelisten i feltet Kundekonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42d44-111">In the Customer account field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="42d44-112">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42d44-112">In the list, find and select the desired record.</span></span>
5. <span data-ttu-id="42d44-113">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="42d44-113">Click OK.</span></span>
6. <span data-ttu-id="42d44-114">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42d44-114">In the Item number field, click the drop-down button to open the lookup.</span></span>
7. <span data-ttu-id="42d44-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42d44-115">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="42d44-116">Hvis du bruger USMF, kan du vælge D0001.</span><span class="sxs-lookup"><span data-stu-id="42d44-116">If you're using USMF, you could select D0001.</span></span>  
8. <span data-ttu-id="42d44-117">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="42d44-117">In the Quantity field, enter a number.</span></span>
9. <span data-ttu-id="42d44-118">Klik på Tilføj linje.</span><span class="sxs-lookup"><span data-stu-id="42d44-118">Click Add line.</span></span>
10. <span data-ttu-id="42d44-119">Klik på rullelisten i feltet Varenummer for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42d44-119">In the Item number field, click the drop-down button to open the lookup.</span></span>
11. <span data-ttu-id="42d44-120">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42d44-120">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="42d44-121">Hvis du bruger USMF, kan du vælge T0020.</span><span class="sxs-lookup"><span data-stu-id="42d44-121">If you're using USMF, you could select T0020.</span></span>  
12. <span data-ttu-id="42d44-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42d44-122">In the list, click the link in the selected row.</span></span>
13. <span data-ttu-id="42d44-123">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="42d44-123">In the Quantity field, enter a number.</span></span>
14. <span data-ttu-id="42d44-124">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="42d44-124">Click Save.</span></span>
15. <span data-ttu-id="42d44-125">Klik på Salgsordre i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="42d44-125">On the Action Pane, click Sales order.</span></span>
16. <span data-ttu-id="42d44-126">Klik på indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="42d44-126">Click Purchase order.</span></span>
    * <span data-ttu-id="42d44-127">Siden Opret indkøbsordre indeholder alle åbne salgsordrelinjer, som er kopieret fra salgsordren.</span><span class="sxs-lookup"><span data-stu-id="42d44-127">The Create purchase order page lists all the open sales order lines which have been copied from the sales order.</span></span> <span data-ttu-id="42d44-128">Du kan gennemse ordredetaljerne, og hvis det er nødvendigt, kan du ændre de valgte oplysninger som f.eks. købsmængde og prisvilkår, før du opretter indkøbene.</span><span class="sxs-lookup"><span data-stu-id="42d44-128">You can review the order details, and if required, you can modify selected details such purchase quantity and pricing terms, before you create the purchases.</span></span>  
17. <span data-ttu-id="42d44-129">Vælg indstillingen Medtag alle.</span><span class="sxs-lookup"><span data-stu-id="42d44-129">Select the Include all option.</span></span>
    * <span data-ttu-id="42d44-130">Hvis du vil generere en indkøbsordre for kun et undersæt af salgsordrelinjerne, skal du vælge disse individuelt.</span><span class="sxs-lookup"><span data-stu-id="42d44-130">If you want to generate purchase orders for only a subset of the sales order lines, select these individually.</span></span>  
    * <span data-ttu-id="42d44-131">Feltet Kreditorkonto er muligvis allerede udfyldt med et leverandørnummer.</span><span class="sxs-lookup"><span data-stu-id="42d44-131">The Vendor account field may or may not already be populated with a vendor number.</span></span> <span data-ttu-id="42d44-132">Hvis standardkreditoren er konfigureret for produktet (på den tilknyttede varedisponering), kopieres denne kreditor til linjen.</span><span class="sxs-lookup"><span data-stu-id="42d44-132">If the default vendor is set up for the product (on the associated Item coverage) then this vendor will be copied  to the line.</span></span> <span data-ttu-id="42d44-133">Ellers skal du angive en kreditor manuelt.</span><span class="sxs-lookup"><span data-stu-id="42d44-133">Otherwise, you must enter a vendor manually.</span></span>  <span data-ttu-id="42d44-134">I denne vejledning, uanset om feltet Kreditorkonto allerede indeholder en værdi, får du i følgende trin en vejledning i at vælge en ny kreditor, der er forskellig for hver linje.</span><span class="sxs-lookup"><span data-stu-id="42d44-134">In this guide, regardless of whether the Vendor account field already contains a value or not, the following steps instruct you to select a new vendor which is different for each line.</span></span>  
18. <span data-ttu-id="42d44-135">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42d44-135">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
19. <span data-ttu-id="42d44-136">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42d44-136">In the list, find and select the desired record.</span></span>
20. <span data-ttu-id="42d44-137">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42d44-137">In the list, click the link in the selected row.</span></span>
21. <span data-ttu-id="42d44-138">Vælg den anden ordrelinje.</span><span class="sxs-lookup"><span data-stu-id="42d44-138">Select the second order line.</span></span>
22. <span data-ttu-id="42d44-139">Klik på rullelisten i feltet Kreditorkonto for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="42d44-139">In the Vendor account field, click the drop-down button to open the lookup.</span></span>
23. <span data-ttu-id="42d44-140">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="42d44-140">In the list, find and select the desired record.</span></span>
24. <span data-ttu-id="42d44-141">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="42d44-141">In the list, click the link in the selected row.</span></span>
25. <span data-ttu-id="42d44-142">Klik på Valider.</span><span class="sxs-lookup"><span data-stu-id="42d44-142">Click Validate.</span></span>
26. <span data-ttu-id="42d44-143">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="42d44-143">Click OK.</span></span>
    * <span data-ttu-id="42d44-144">Meddelelsen fortæller dig, at der er oprettet en eller flere indkøbsordrer.</span><span class="sxs-lookup"><span data-stu-id="42d44-144">The message informs you that one or more purchase orders have been created.</span></span> <span data-ttu-id="42d44-145">Systemet genererer en separat indkøbsordre for hver kreditor, du har angivet for ordrelinjerne.</span><span class="sxs-lookup"><span data-stu-id="42d44-145">The system generates a separate purchase order for each vendor that you specified for the sales order lines.</span></span> <span data-ttu-id="42d44-146">Det betyder, at hvis flere salgsordrelinjer skal leveres af den samme leverandør, oprettes der en enkelt indkøbsordre med flere linjer.</span><span class="sxs-lookup"><span data-stu-id="42d44-146">This means that if several sales order lines are to be supplied by the same vendor, a single purchase order with multiple lines will be generated.</span></span>  

## <a name="review-purchase-orders-created-from-sales-orders"></a><span data-ttu-id="42d44-147">Gennemse indkøbsordrer, der er oprettet ud fra salgsordrer</span><span class="sxs-lookup"><span data-stu-id="42d44-147">Review purchase orders created from sales orders</span></span>
1. <span data-ttu-id="42d44-148">Klik på Generelt i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="42d44-148">On the Action Pane, click General.</span></span>
2. <span data-ttu-id="42d44-149">Klik på Relaterede ordrer.</span><span class="sxs-lookup"><span data-stu-id="42d44-149">Click Related orders.</span></span>
    * <span data-ttu-id="42d44-150">Siden Relaterede ordrer indeholder en liste over alle de ordrer, der er oprettet fra ordren.</span><span class="sxs-lookup"><span data-stu-id="42d44-150">The Related orders page lists all the orders that were created from the sales order.</span></span> <span data-ttu-id="42d44-151">I dette eksempel er der oprettet to indkøbsordrer for hver af to forskellige leverandører.</span><span class="sxs-lookup"><span data-stu-id="42d44-151">In this example, there are two purchase orders generated for two different vendors respectively.</span></span>  
3. <span data-ttu-id="42d44-152">Klik for at følge linket i feltet Indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="42d44-152">Click to follow the link in the Purchase order field.</span></span>
    * <span data-ttu-id="42d44-153">Hver indkøbsordrelinje er tilknyttet den salgsordrelinje, der har resulteret i købet.</span><span class="sxs-lookup"><span data-stu-id="42d44-153">Each purchase order line is associated with the sales order line that led to the purchase.</span></span> <span data-ttu-id="42d44-154">Relationen til salgsordren er angivet under fanen Produkt i linjedetaljerne i oversigtspanelet, i referencetypen, referencenummeret og i referencepartifelterne.</span><span class="sxs-lookup"><span data-stu-id="42d44-154">The relation to the sales order is indicated on the Product tab in the Line details FastTab, in the Reference type, Reference number, and Reference lot fields.</span></span>  
4. <span data-ttu-id="42d44-155">Udvis eller skjul sektionen Linedetaljer.</span><span class="sxs-lookup"><span data-stu-id="42d44-155">Expand or collapse the Line details section.</span></span>
5. <span data-ttu-id="42d44-156">Klik på fanen Produkt.</span><span class="sxs-lookup"><span data-stu-id="42d44-156">Click the Product tab.</span></span>
    * <span data-ttu-id="42d44-157">Referencepartiet sikrer, at omkostningerne i forbindelse med det aktuelle indkøb debiteres den tilknyttede ordre.</span><span class="sxs-lookup"><span data-stu-id="42d44-157">The Reference lot guarantees that the costs from the current purchase are charged on the attached sales order.</span></span>  
    * <span data-ttu-id="42d44-158">Du kan navigere til den oprindelige salgsordre ved at åbne linket i feltet Nummer på reference.</span><span class="sxs-lookup"><span data-stu-id="42d44-158">You can navigate to the originating sales order by opening the link in the Reference number field.</span></span>  

