--- 
title: Oprette salgsordrefakturaer
description: Denne opgaveguide beskriver fakturering af en salgsordre, herunder fletning af fakturaer og batchbehandling.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 8/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 32d71167fdad65cb1dec37671999a497759ca484
ms.openlocfilehash: 6f687816fc6393de2a587273a5350858b3503945
ms.contentlocale: da-dk
ms.lasthandoff: 09/11/2018

---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="67cd3-103">Oprette salgsordrefakturaer</span><span class="sxs-lookup"><span data-stu-id="67cd3-103">Create sales order invoices</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="67cd3-104">Denne opgaveguide beskriver fakturering af en salgsordre, herunder fletning af fakturaer og batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="67cd3-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="67cd3-105">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="67cd3-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="67cd3-106">Opret en faktura fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="67cd3-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="67cd3-107">Gå til Debitor > Ordrer > Salgsordrer, der er afsendt men ikke faktureret.</span><span class="sxs-lookup"><span data-stu-id="67cd3-107">Go to Accounts receivable > Orders > Shipped but not invoiced sales orders.</span></span>
2. <span data-ttu-id="67cd3-108">Vælg en salgsordre på listen.</span><span class="sxs-lookup"><span data-stu-id="67cd3-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="67cd3-109">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="67cd3-109">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="67cd3-110">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="67cd3-110">Click Invoice.</span></span>
    * <span data-ttu-id="67cd3-111">Bemærk, at denne salgsordre har flere tilknyttede følgesedler.</span><span class="sxs-lookup"><span data-stu-id="67cd3-111">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="67cd3-112">Den viser kun ordet <multiple> i stedet for nummeret på følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="67cd3-112">It will only show the word <multiple> instead of the packing slip number.</span></span>  
5. <span data-ttu-id="67cd3-113">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="67cd3-113">Expand the Parameters section.</span></span>
    * <span data-ttu-id="67cd3-114">Bogføring skal være angivet til Ja for at bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="67cd3-114">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="67cd3-115">Du kan også deaktivere bogføring og bare udskrive fakturaen.</span><span class="sxs-lookup"><span data-stu-id="67cd3-115">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="67cd3-116">Du kan dog opnå det samme resultat ved at oprette en proformafaktura i stedet for en faktura.</span><span class="sxs-lookup"><span data-stu-id="67cd3-116">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    * <span data-ttu-id="67cd3-117">Denne indstilling anvendes til batchjob.</span><span class="sxs-lookup"><span data-stu-id="67cd3-117">This option is used for batch jobs.</span></span> <span data-ttu-id="67cd3-118">Forespørgslen køres, når batchjobbet køres.</span><span class="sxs-lookup"><span data-stu-id="67cd3-118">The query is run when the batch job is run.</span></span>    
6. <span data-ttu-id="67cd3-119">Vælg "Efter" i feltet Udskriv.</span><span class="sxs-lookup"><span data-stu-id="67cd3-119">In the Print field, select 'After'.</span></span>
7. <span data-ttu-id="67cd3-120">Vælg Ja for Udskriv faktura.</span><span class="sxs-lookup"><span data-stu-id="67cd3-120">Select Yes for Print invoice.</span></span>
    * <span data-ttu-id="67cd3-121">Udskriftsstyring kan udskrive flere kopier af fakturaen og også sende fakturaen via mail som en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="67cd3-121">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
8. <span data-ttu-id="67cd3-122">Vælg "Opsummer" i feltet Udskriv gebyrer.</span><span class="sxs-lookup"><span data-stu-id="67cd3-122">In the Print charges field, select 'Summarize'.</span></span>
9. <span data-ttu-id="67cd3-123">Vælg "Saldo" i feltet Kontrollér kreditmaks.</span><span class="sxs-lookup"><span data-stu-id="67cd3-123">In the Check credit limit field, select 'Balance'.</span></span>
10. <span data-ttu-id="67cd3-124">Klik på Annuller.</span><span class="sxs-lookup"><span data-stu-id="67cd3-124">Click Cancel.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="67cd3-125">Kombinere ordrer i én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="67cd3-125">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="67cd3-126">Gå til Debitor > Ordrer > Alle salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="67cd3-126">Go to Accounts receivable > Orders > All sales orders.</span></span>
2. <span data-ttu-id="67cd3-127">Find en debitor, der har flere fakturaer, der er åbne.</span><span class="sxs-lookup"><span data-stu-id="67cd3-127">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="67cd3-128">Vælg en åben salgsordre.</span><span class="sxs-lookup"><span data-stu-id="67cd3-128">Select an open sales order.</span></span>
4. <span data-ttu-id="67cd3-129">Vælg en anden salgsordre for den samme kunde.</span><span class="sxs-lookup"><span data-stu-id="67cd3-129">Select another open sales order for the same customer.</span></span>
5. <span data-ttu-id="67cd3-130">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="67cd3-130">On the Action Pane, click Invoice.</span></span>
6. <span data-ttu-id="67cd3-131">Klik på Faktura.</span><span class="sxs-lookup"><span data-stu-id="67cd3-131">Click Invoice.</span></span>
7. <span data-ttu-id="67cd3-132">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="67cd3-132">Expand the Parameters section.</span></span>
8. <span data-ttu-id="67cd3-133">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="67cd3-133">In the Quantity field, select 'All'.</span></span>
    * <span data-ttu-id="67cd3-134">Bemærk, at der er vist to fakturaer oversigtsafsnittet.</span><span class="sxs-lookup"><span data-stu-id="67cd3-134">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="67cd3-135">Nu vi flette dem til en enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="67cd3-135">Now let's merge them into a single invoice.</span></span>  
9. <span data-ttu-id="67cd3-136">Vælg "Fakturakonto"i samleopdateringen for feltet.</span><span class="sxs-lookup"><span data-stu-id="67cd3-136">In the Summary update for field, select 'Invoice account'.</span></span>
10. <span data-ttu-id="67cd3-137">Klik på Arranger for at flette salgsordrerne til en enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="67cd3-137">Click Arrange to merge the sales orders into a single invoice.</span></span>
    * <span data-ttu-id="67cd3-138">De to salgsordrer er nu flettet i én faktura.</span><span class="sxs-lookup"><span data-stu-id="67cd3-138">The two sales orders are now merged into a single invoice.</span></span>   
11. <span data-ttu-id="67cd3-139">Klik på Annuller.</span><span class="sxs-lookup"><span data-stu-id="67cd3-139">Click Cancel.</span></span>
12. <span data-ttu-id="67cd3-140">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="67cd3-140">Click Yes.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="67cd3-141">Bogføre fakturaer i et batch</span><span class="sxs-lookup"><span data-stu-id="67cd3-141">Post invoices in a batch</span></span>
1. <span data-ttu-id="67cd3-142">Gå til Debitor > Fakturaer > Batchfakturering > Faktura.</span><span class="sxs-lookup"><span data-stu-id="67cd3-142">Go to Accounts receivable > Invoices > Batch invoicing > Invoice.</span></span>
2. <span data-ttu-id="67cd3-143">Klik på Vælg.</span><span class="sxs-lookup"><span data-stu-id="67cd3-143">Click Select.</span></span>
3. <span data-ttu-id="67cd3-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="67cd3-144">Click OK.</span></span>
4. <span data-ttu-id="67cd3-145">Klik på Batch.</span><span class="sxs-lookup"><span data-stu-id="67cd3-145">Click Batch.</span></span>
5. <span data-ttu-id="67cd3-146">Klik på Ja for at aktivere batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="67cd3-146">Click on Yes to turn on batch processing.</span></span>
6. <span data-ttu-id="67cd3-147">Klik på Gentagelse.</span><span class="sxs-lookup"><span data-stu-id="67cd3-147">Click Recurrence.</span></span>
7. <span data-ttu-id="67cd3-148">Vælg Dage</span><span class="sxs-lookup"><span data-stu-id="67cd3-148">Select Days</span></span>
8. <span data-ttu-id="67cd3-149">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="67cd3-149">Click OK.</span></span>
9. <span data-ttu-id="67cd3-150">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="67cd3-150">Click OK.</span></span>
10. <span data-ttu-id="67cd3-151">Klik på Annuller.</span><span class="sxs-lookup"><span data-stu-id="67cd3-151">Click Cancel.</span></span>
11. <span data-ttu-id="67cd3-152">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="67cd3-152">Click Yes.</span></span>


