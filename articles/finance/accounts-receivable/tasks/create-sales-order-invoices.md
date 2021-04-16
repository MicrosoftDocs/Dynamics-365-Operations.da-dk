---
title: Oprette salgsordrefakturaer
description: Denne opgaveguide beskriver fakturering af en salgsordre, herunder fletning af fakturaer og batchbehandling.
author: ShivamPandey-msft
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 984bb482f357e35dcfa4c08597a6be9e39817b98
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5837099"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="58b9c-103">Oprette salgsordrefakturaer</span><span class="sxs-lookup"><span data-stu-id="58b9c-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="58b9c-104">Denne opgaveguide beskriver fakturering af en salgsordre, herunder fletning af fakturaer og batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="58b9c-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="58b9c-105">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="58b9c-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="58b9c-106">Opret en faktura fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="58b9c-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="58b9c-107">Gå til **Navigationsrude > Moduler > Debitor > Ordrer > Salgsordrer, der er afsendt men ikke faktureret**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="58b9c-108">Vælg en salgsordre på listen.</span><span class="sxs-lookup"><span data-stu-id="58b9c-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="58b9c-109">Klik på **Faktura > Generér > Faktura** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="58b9c-110">Bemærk, at denne salgsordre har flere tilknyttede følgesedler.</span><span class="sxs-lookup"><span data-stu-id="58b9c-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="58b9c-111">Den viser kun ordet <multiple> i stedet for nummeret på følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="58b9c-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="58b9c-112">Udvid sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="58b9c-113">Bogføring skal være angivet til Ja for at bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="58b9c-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="58b9c-114">Du kan også deaktivere bogføring og bare udskrive fakturaen.</span><span class="sxs-lookup"><span data-stu-id="58b9c-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="58b9c-115">Du kan dog opnå det samme resultat ved at oprette en proformafaktura i stedet for en faktura.</span><span class="sxs-lookup"><span data-stu-id="58b9c-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="58b9c-116">Denne indstilling anvendes til batchjob.</span><span class="sxs-lookup"><span data-stu-id="58b9c-116">This option is used for batch jobs.</span></span> <span data-ttu-id="58b9c-117">Forespørgslen køres, når batchjobbet køres.</span><span class="sxs-lookup"><span data-stu-id="58b9c-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="58b9c-118">Vælg "Efter" i feltet **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="58b9c-119">Vælg **Ja** for **Udskriv faktura**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="58b9c-120">Udskriftsstyring kan udskrive flere kopier af fakturaen og også sende fakturaen via mail som en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="58b9c-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="58b9c-121">Vælg "Opsummer" i feltet **Udskriv gebyrer**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="58b9c-122">Vælg "Saldo" i feltet **Kontrollér kreditmaks**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="58b9c-123">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="58b9c-124">Kombinere ordrer i én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="58b9c-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="58b9c-125">Gå til **Navigationsrude > Moduler > Debitor > Ordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="58b9c-126">Find en debitor, der har flere fakturaer, der er åbne.</span><span class="sxs-lookup"><span data-stu-id="58b9c-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="58b9c-127">Vælg flere åbne salgsordrer fra samme kunde.</span><span class="sxs-lookup"><span data-stu-id="58b9c-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="58b9c-128">Klik på **Faktura > Generér > Faktura** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="58b9c-129">Udvid sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="58b9c-130">Vælg "Alle" i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="58b9c-131">Bemærk, at der er vist to fakturaer oversigtsafsnittet.</span><span class="sxs-lookup"><span data-stu-id="58b9c-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="58b9c-132">Nu vi flette dem til en enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="58b9c-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="58b9c-133">Vælg "Fakturakonto" i feltet **Samleopdatering for**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="58b9c-134">Klik på **Arranger** for at flette salgsordrerne til en enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="58b9c-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="58b9c-135">De to salgsordrer er nu flettet i én faktura.</span><span class="sxs-lookup"><span data-stu-id="58b9c-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="58b9c-136">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="58b9c-137">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="58b9c-138">Bogføre fakturaer i et batch</span><span class="sxs-lookup"><span data-stu-id="58b9c-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="58b9c-139">Gå til **Navigationsrude > Moduler > Debitor > Fakturaer > Batchfakturering > Faktura**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="58b9c-140">Klik på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-140">Click **Select**.</span></span>
3. <span data-ttu-id="58b9c-141">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-141">Click **OK**.</span></span>
4. <span data-ttu-id="58b9c-142">Klik på **Batch**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-142">Click **Batch**.</span></span>
5. <span data-ttu-id="58b9c-143">Vælg **Ja** for **Batchbehandling**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="58b9c-144">Klik på **Gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="58b9c-145">Vælg **Dage**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-145">Select **Days**.</span></span>
8. <span data-ttu-id="58b9c-146">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-146">Click **OK**.</span></span>
9. <span data-ttu-id="58b9c-147">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-147">Click **OK**.</span></span>
10. <span data-ttu-id="58b9c-148">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="58b9c-149">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="58b9c-149">Click **Yes**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]