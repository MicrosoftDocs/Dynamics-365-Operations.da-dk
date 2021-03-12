---
title: Oprette salgsordrefakturaer
description: Denne opgaveguide beskriver fakturering af en salgsordre, herunder fletning af fakturaer og batchbehandling.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 06/25/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: SalesTableListPage, SalesEditLines,  SysQueryForm, SysRecurrence
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e0076e838ad4eac687dc7db1bc0a94891f0ee6d9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991011"
---
# <a name="create-sales-order-invoices"></a><span data-ttu-id="1e450-103">Oprette salgsordrefakturaer</span><span class="sxs-lookup"><span data-stu-id="1e450-103">Create sales order invoices</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="1e450-104">Denne opgaveguide beskriver fakturering af en salgsordre, herunder fletning af fakturaer og batchbehandling.</span><span class="sxs-lookup"><span data-stu-id="1e450-104">This task guide describes invoicing a sales order, including merging invoices and batch processing.</span></span> <span data-ttu-id="1e450-105">Denne procedure bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="1e450-105">This procedure uses the USMF demo company.</span></span>


## <a name="create-an-invoice-from-a-sales-order"></a><span data-ttu-id="1e450-106">Opret en faktura fra en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="1e450-106">Create an invoice from a sales order</span></span>
1. <span data-ttu-id="1e450-107">Gå til **Navigationsrude > Moduler > Debitor > Ordrer > Salgsordrer, der er afsendt men ikke faktureret**.</span><span class="sxs-lookup"><span data-stu-id="1e450-107">Go to **Navigation pane > Modules > Accounts receivable > Orders > Shipped but not invoiced sales orders**.</span></span>
2. <span data-ttu-id="1e450-108">Vælg en salgsordre på listen.</span><span class="sxs-lookup"><span data-stu-id="1e450-108">Select a sales order in the list.</span></span> 
3. <span data-ttu-id="1e450-109">Klik på **Faktura > Generér > Faktura** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="1e450-109">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span> <span data-ttu-id="1e450-110">Bemærk, at denne salgsordre har flere tilknyttede følgesedler.</span><span class="sxs-lookup"><span data-stu-id="1e450-110">Note that this sales order has multiple packing slips associated with it.</span></span> <span data-ttu-id="1e450-111">Den viser kun ordet <multiple> i stedet for nummeret på følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="1e450-111">It will only show the word <multiple> instead of the packing slip number.</span></span>  
4. <span data-ttu-id="1e450-112">Udvid sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="1e450-112">Expand the **Parameters** section.</span></span>
    - <span data-ttu-id="1e450-113">Bogføring skal være angivet til Ja for at bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1e450-113">Posting must be set to Yes to post the invoice.</span></span> <span data-ttu-id="1e450-114">Du kan også deaktivere bogføring og bare udskrive fakturaen.</span><span class="sxs-lookup"><span data-stu-id="1e450-114">You can also turn off posting and just print the invoice.</span></span> <span data-ttu-id="1e450-115">Du kan dog opnå det samme resultat ved at oprette en proformafaktura i stedet for en faktura.</span><span class="sxs-lookup"><span data-stu-id="1e450-115">However, you can accomplish the same result by creating a proforma invoice instead of an invoice.</span></span>  
    - <span data-ttu-id="1e450-116">Denne indstilling anvendes til batchjob.</span><span class="sxs-lookup"><span data-stu-id="1e450-116">This option is used for batch jobs.</span></span> <span data-ttu-id="1e450-117">Forespørgslen køres, når batchjobbet køres.</span><span class="sxs-lookup"><span data-stu-id="1e450-117">The query is run when the batch job is run.</span></span>
5. <span data-ttu-id="1e450-118">Vælg "Efter" i feltet **Udskriv**.</span><span class="sxs-lookup"><span data-stu-id="1e450-118">In the **Print** field, select 'After'.</span></span>
6. <span data-ttu-id="1e450-119">Vælg **Ja** for **Udskriv faktura**.</span><span class="sxs-lookup"><span data-stu-id="1e450-119">Select **Yes** for **Print invoice**.</span></span> <span data-ttu-id="1e450-120">Udskriftsstyring kan udskrive flere kopier af fakturaen og også sende fakturaen via mail som en PDF-fil.</span><span class="sxs-lookup"><span data-stu-id="1e450-120">Print management can print  multiple copies of the invoice and also send the invoice via email as a PDF file.</span></span>  
7. <span data-ttu-id="1e450-121">Vælg "Opsummer" i feltet **Udskriv gebyrer**.</span><span class="sxs-lookup"><span data-stu-id="1e450-121">In the **Print charges** field, select 'Summarize'.</span></span>
8. <span data-ttu-id="1e450-122">Vælg "Saldo" i feltet **Kontrollér kreditmaks**.</span><span class="sxs-lookup"><span data-stu-id="1e450-122">In the **Check credit limit** field, select 'Balance'.</span></span>
9. <span data-ttu-id="1e450-123">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="1e450-123">Click **Cancel**.</span></span>

## <a name="combine-orders-into-a-single-invoice"></a><span data-ttu-id="1e450-124">Kombinere ordrer i én enkelt faktura</span><span class="sxs-lookup"><span data-stu-id="1e450-124">Combine orders into a single invoice</span></span>
1. <span data-ttu-id="1e450-125">Gå til **Navigationsrude > Moduler > Debitor > Ordrer > Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="1e450-125">Go to **Navigation pane > Modules > Accounts receivable > Orders > All sales orders**.</span></span>
2. <span data-ttu-id="1e450-126">Find en debitor, der har flere fakturaer, der er åbne.</span><span class="sxs-lookup"><span data-stu-id="1e450-126">Locate a customer that has multiple invoices open.</span></span>
3. <span data-ttu-id="1e450-127">Vælg flere åbne salgsordrer fra samme kunde.</span><span class="sxs-lookup"><span data-stu-id="1e450-127">Select multiple open sales orders from the same customer.</span></span>
4. <span data-ttu-id="1e450-128">Klik på **Faktura > Generér > Faktura** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="1e450-128">On the **Action Pane**, click **Invoice > Generate > Invoice**.</span></span>
5. <span data-ttu-id="1e450-129">Udvid sektionen **Parametre**.</span><span class="sxs-lookup"><span data-stu-id="1e450-129">Expand the **Parameters** section.</span></span>
6. <span data-ttu-id="1e450-130">Vælg "Alle" i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="1e450-130">In the **Quantity** field, select 'All'.</span></span> <span data-ttu-id="1e450-131">Bemærk, at der er vist to fakturaer oversigtsafsnittet.</span><span class="sxs-lookup"><span data-stu-id="1e450-131">Note that there are two invoices listed in the overview section.</span></span> <span data-ttu-id="1e450-132">Nu vi flette dem til en enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="1e450-132">Now let's merge them into a single invoice.</span></span>  
7. <span data-ttu-id="1e450-133">Vælg "Fakturakonto" i feltet **Samleopdatering for**.</span><span class="sxs-lookup"><span data-stu-id="1e450-133">In the **Summary update for** field, select 'Invoice account'.</span></span>
8. <span data-ttu-id="1e450-134">Klik på **Arranger** for at flette salgsordrerne til en enkelt faktura.</span><span class="sxs-lookup"><span data-stu-id="1e450-134">Click **Arrange** to merge the sales orders into a single invoice.</span></span> <span data-ttu-id="1e450-135">De to salgsordrer er nu flettet i én faktura.</span><span class="sxs-lookup"><span data-stu-id="1e450-135">The two sales orders are now merged into a single invoice.</span></span>   
9. <span data-ttu-id="1e450-136">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="1e450-136">Click **Cancel**.</span></span>
10. <span data-ttu-id="1e450-137">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1e450-137">Click **Yes**.</span></span>

## <a name="post-invoices-in-a-batch"></a><span data-ttu-id="1e450-138">Bogføre fakturaer i et batch</span><span class="sxs-lookup"><span data-stu-id="1e450-138">Post invoices in a batch</span></span>
1. <span data-ttu-id="1e450-139">Gå til **Navigationsrude > Moduler > Debitor > Fakturaer > Batchfakturering > Faktura**.</span><span class="sxs-lookup"><span data-stu-id="1e450-139">Go to **Navigation pane > Modules > Accounts receivable > Invoices > Batch invoicing > Invoice**.</span></span>
2. <span data-ttu-id="1e450-140">Klik på **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="1e450-140">Click **Select**.</span></span>
3. <span data-ttu-id="1e450-141">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e450-141">Click **OK**.</span></span>
4. <span data-ttu-id="1e450-142">Klik på **Batch**.</span><span class="sxs-lookup"><span data-stu-id="1e450-142">Click **Batch**.</span></span>
5. <span data-ttu-id="1e450-143">Vælg **Ja** for **Batchbehandling**.</span><span class="sxs-lookup"><span data-stu-id="1e450-143">Select **Yes** in **Batch processing**.</span></span>
6. <span data-ttu-id="1e450-144">Klik på **Gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="1e450-144">Click **Recurrence**.</span></span>
7. <span data-ttu-id="1e450-145">Vælg **Dage**.</span><span class="sxs-lookup"><span data-stu-id="1e450-145">Select **Days**.</span></span>
8. <span data-ttu-id="1e450-146">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e450-146">Click **OK**.</span></span>
9. <span data-ttu-id="1e450-147">Klik på **OK**.</span><span class="sxs-lookup"><span data-stu-id="1e450-147">Click **OK**.</span></span>
10. <span data-ttu-id="1e450-148">Klik på **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="1e450-148">Click **Cancel**.</span></span>
11. <span data-ttu-id="1e450-149">Klik på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="1e450-149">Click **Yes**.</span></span>

