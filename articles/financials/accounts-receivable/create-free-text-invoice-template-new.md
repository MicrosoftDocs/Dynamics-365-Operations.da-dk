--- 
title: Oprette en skabelon til en fritekstfaktura
description: Denne procedure viser, hvordan du opretter en skabelon til en fritekstfaktura.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 05/29/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d617302e020c21a7a7fb077e4ce9481b6c80b796
ms.openlocfilehash: 80eb886c70e3bfde3a9eff87be48498aa48d7234
ms.contentlocale: da-dk
ms.lasthandoff: 08/06/2018

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="d3ae2-103">Oprette en skabelon til en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="d3ae2-103">Create a free text invoice template</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d3ae2-104">I denne gennemgang skal du bruge USMF-demoregnskabet.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-104">For this walkthrough, use the USMF demo company.</span></span> <span data-ttu-id="d3ae2-105">Denne procedure er beregnet til den bruger, der er ansvarlig for håndtering og behandling af debitorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-105">This procedure is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

## <a name="create-a-template"></a><span data-ttu-id="d3ae2-106">Opret en skabelon</span><span class="sxs-lookup"><span data-stu-id="d3ae2-106">Create a template</span></span>

1. <span data-ttu-id="d3ae2-107">Gå til Debitor > Fakturaer > Tilbagevendende fakturaer > Skabeloner til fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-107">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="d3ae2-108">Du kan bruge denne form til at oprette skabeloner til fritekstfakturaer, som kan indeholde fakturalinjer, gebyrer, en regnskabsfordelingsskabelon og oplysninger om finanskonti.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-108">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="d3ae2-109">Klik på "Ny" for at oprette en ny skabelon til en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-109">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="d3ae2-110">Skriv en værdi i feltet Skabelonnavn.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-110">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="d3ae2-111">"Skabelonnavn" identificerer entydigt en skabelon til fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-111">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="d3ae2-112">To skabeloner kan ikke have samme "Skabelonnavn".</span><span class="sxs-lookup"><span data-stu-id="d3ae2-112">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="d3ae2-113">Indtast en beskrivelse af skabelonen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-113">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="d3ae2-114">Udvid fanen Fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-114">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="d3ae2-115">Angiv en beskrivelse af fakturalinjen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-115">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="d3ae2-116">Vælg en omsætningskonto i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-116">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="d3ae2-117">Du kan vælge en modkonto for en debitorkreditering for det samlede fakturabeløb på siden Debitorposteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-117">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="d3ae2-118">Klik på rullelisten i feltet Momsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-118">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d3ae2-119">Momsgruppen for den aktuelle fakturalinje er standardmomsgruppen for debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-119">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="d3ae2-120">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-120">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="d3ae2-121">Vælg varemomsgruppen for den aktuelle fakturalinje i feltet Varemomsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-121">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="d3ae2-122">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-122">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="d3ae2-123">Angiv eller få vist prisen pr. enhed for fakturalinjen i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-123">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="d3ae2-124">Dette beløb ganges automatisk med feltet Antal for at bestemme beløbet på fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-124">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="d3ae2-125">Føj en ny linje til skabelon til fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-125">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="d3ae2-126">Angiv en beskrivelse af fakturalinjen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-126">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="d3ae2-127">Vælg en omsætningskonto i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-127">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="d3ae2-128">Du kan vælge en modkonto for en debitorkreditering for det samlede fakturabeløb på siden Debitorposteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-128">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="d3ae2-129">Klik på rullelisten i feltet Momsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-129">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d3ae2-130">Momsgruppen for den aktuelle fakturalinje er standardmomsgruppen for debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-130">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="d3ae2-131">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-131">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="d3ae2-132">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-132">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="d3ae2-133">Varemomsgruppen for den aktuelle fakturalinje.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-133">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="d3ae2-134">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-134">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="d3ae2-135">Angiv eller få vist antallet af enheder for fakturalinjen</span><span class="sxs-lookup"><span data-stu-id="d3ae2-135">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="d3ae2-136">Dette tal ganges med værdien i feltet Enhedspris for at bestemme beløbet på fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-136">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="d3ae2-137">Angiv eller få vist prisen pr. enhed for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-137">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="d3ae2-138">Dette beløb ganges med værdien i feltet Antal for at bestemme beløbet på fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-138">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="d3ae2-139">Få vist og rediger regnskabsfordelinger for en enkelt linje og eventuelle underordnede linjer.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-139">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="d3ae2-140">Regnskabsfordelinger bruges til at definere, hvordan et beløb skal håndteres regnskabsmæssigt, f.eks. hvordan indtægt, skat eller afgifter håndteres på en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-140">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="d3ae2-141">Opdater regnskabsfordelingerne for den valgte fakturalinje.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-141">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="d3ae2-142">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-142">Click Close.</span></span>

## <a name="save-a-free-text-invoice-as-a-template"></a><span data-ttu-id="d3ae2-143">Gemme en fritekstfaktura som en skabelon</span><span class="sxs-lookup"><span data-stu-id="d3ae2-143">Save a free text invoice as a template</span></span>
<span data-ttu-id="d3ae2-144">Du kan også gemme en eksisterende fritekstfaktura som en skabelon.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-144">You can also save an existing free text invoice as a template.</span></span> <span data-ttu-id="d3ae2-145">Når du vælger Gem i skabelon under fanen faktura, kan du angive et navn og en beskrivelse af skabelonen.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-145">When you select Save to template from the Invoice tab, provide a name and a description for the template.</span></span> <span data-ttu-id="d3ae2-146">Hvis der findes allerede en skabelon med dette navn, vises en meddelelse om, at der allerede findes en skabelon med dette navn.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-146">If a template with the name already exists, you will see a notification that a template with that name already exists.</span></span> <span data-ttu-id="d3ae2-147">Du kan stadig klikke på OK for at erstatte den.</span><span class="sxs-lookup"><span data-stu-id="d3ae2-147">You can still click on Ok to replace it.</span></span> 

