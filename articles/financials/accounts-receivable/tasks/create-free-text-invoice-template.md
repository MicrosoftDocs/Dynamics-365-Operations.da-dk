--- 
title: Oprette en skabelon til en fritekstfaktura
description: Denne registrering anvender demofirmaet USMF.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 11/11/2016
ms.topic: business-process
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: e9c9811b348d81cd735c5b75ca48e0a56a8d52be
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice-template"></a><span data-ttu-id="12c94-103">Oprette en skabelon til en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="12c94-103">Create a free text invoice template</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="12c94-104">Denne registrering anvender demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="12c94-104">This recording uses the USMF demo company.</span></span> <span data-ttu-id="12c94-105">Registreringen er beregnet til den bruger, der er ansvarlig for håndtering og behandling af debitorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="12c94-105">The recording is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="12c94-106">Gå til Debitor > Fakturaer > Tilbagevendende fakturaer > Skabeloner til fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="12c94-106">Go to Accounts receivable > Invoices > Recurring invoices > Free text invoice templates.</span></span>
    * <span data-ttu-id="12c94-107">Du kan bruge denne form til at oprette skabeloner til fritekstfakturaer, som kan indeholde fakturalinjer, gebyrer, en regnskabsfordelingsskabelon og oplysninger om finanskonti.</span><span class="sxs-lookup"><span data-stu-id="12c94-107">Use this form to create free text invoice templates that can include invoice lines, charges, an accounting distribution template, and ledger account information.</span></span>  
2. <span data-ttu-id="12c94-108">Klik på "Ny" for at oprette en ny skabelon til en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="12c94-108">Click 'New' to create a new free text invoice template.</span></span>
3. <span data-ttu-id="12c94-109">Skriv en værdi i feltet Skabelonnavn.</span><span class="sxs-lookup"><span data-stu-id="12c94-109">In the Template name field, type a value.</span></span>
    * <span data-ttu-id="12c94-110">"Skabelonnavn" identificerer entydigt en skabelon til fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="12c94-110">‘Template name’ uniquely identifies a free text invoice template.</span></span> <span data-ttu-id="12c94-111">To skabeloner kan ikke have samme "Skabelonnavn".</span><span class="sxs-lookup"><span data-stu-id="12c94-111">No two templates can have the same ‘Template name’.</span></span>  
4. <span data-ttu-id="12c94-112">Indtast en beskrivelse af skabelonen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="12c94-112">In the Description field, enter a description of the template.</span></span>
5. <span data-ttu-id="12c94-113">Udvid fanen Fakturalinjer.</span><span class="sxs-lookup"><span data-stu-id="12c94-113">Expand the Invoice lines tab.</span></span>
6. <span data-ttu-id="12c94-114">Angiv en beskrivelse af fakturalinjen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="12c94-114">In the Description field, enter a description of the invoice line.</span></span>
7. <span data-ttu-id="12c94-115">Vælg en omsætningskonto i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="12c94-115">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="12c94-116">Du kan vælge en modkonto for en debitorkreditering for det samlede fakturabeløb på siden Debitorposteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="12c94-116">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
8. <span data-ttu-id="12c94-117">Klik på rullelisten i feltet Momsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="12c94-117">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="12c94-118">Momsgruppen for den aktuelle fakturalinje er standardmomsgruppen for debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="12c94-118">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
9. <span data-ttu-id="12c94-119">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12c94-119">In the list, click the link in the selected row.</span></span>
10. <span data-ttu-id="12c94-120">Vælg varemomsgruppen for den aktuelle fakturalinje i feltet Varemomsgruppe.</span><span class="sxs-lookup"><span data-stu-id="12c94-120">In the Item tax group field, select the item sales tax group for the current invoice line.</span></span>
11. <span data-ttu-id="12c94-121">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12c94-121">In the list, click the link in the selected row.</span></span>
12. <span data-ttu-id="12c94-122">Angiv eller få vist prisen pr. enhed for fakturalinjen i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="12c94-122">In the Unit price field, enter or view the price per unit for the invoice line</span></span>
    * <span data-ttu-id="12c94-123">Dette beløb ganges automatisk med feltet Antal for at bestemme beløbet på fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="12c94-123">This amount is multiplied by the Quantity field to determine the invoice line amount.</span></span>  
13. <span data-ttu-id="12c94-124">Føj en ny linje til skabelon til fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="12c94-124">Add a new line to free text invoice template.</span></span>
14. <span data-ttu-id="12c94-125">Angiv en beskrivelse af fakturalinjen i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="12c94-125">In the Description field, enter a description of the invoice line.</span></span>
15. <span data-ttu-id="12c94-126">Vælg en omsætningskonto i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="12c94-126">In the Main account field, select a revenue account.</span></span>
    * <span data-ttu-id="12c94-127">Du kan vælge en modkonto for en debitorkreditering for det samlede fakturabeløb på siden Debitorposteringsprofiler.</span><span class="sxs-lookup"><span data-stu-id="12c94-127">You can select the offset transaction account of a customer credit for the total invoice amount in the Customer posting profiles page.</span></span>  
16. <span data-ttu-id="12c94-128">Klik på rullelisten i feltet Momsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="12c94-128">In the Sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="12c94-129">Momsgruppen for den aktuelle fakturalinje er standardmomsgruppen for debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="12c94-129">The sales tax group for the current invoice line is the default sales tax group for the customer account.</span></span>  
17. <span data-ttu-id="12c94-130">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12c94-130">In the list, click the link in the selected row.</span></span>
18. <span data-ttu-id="12c94-131">Klik på rullelisten i feltet Varemomsgruppe for at åbne opslaget.</span><span class="sxs-lookup"><span data-stu-id="12c94-131">In the Item sales tax group field, click the drop-down button to open the lookup.</span></span>
    * <span data-ttu-id="12c94-132">Varemomsgruppen for den aktuelle fakturalinje.</span><span class="sxs-lookup"><span data-stu-id="12c94-132">The item sales tax group for the current invoice line.</span></span>  
19. <span data-ttu-id="12c94-133">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="12c94-133">In the list, click the link in the selected row.</span></span>
20. <span data-ttu-id="12c94-134">Angiv eller få vist antallet af enheder for fakturalinjen</span><span class="sxs-lookup"><span data-stu-id="12c94-134">Enter or view the number of units for the invoice line</span></span>
    * <span data-ttu-id="12c94-135">Dette tal ganges med værdien i feltet Enhedspris for at bestemme beløbet på fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="12c94-135">This number is multiplied by the value in the Unit price field to determine the invoice line amount.</span></span>  
21. <span data-ttu-id="12c94-136">Angiv eller få vist prisen pr. enhed for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="12c94-136">Enter or view the price per unit for the invoice line.</span></span> 
    * <span data-ttu-id="12c94-137">Dette beløb ganges med værdien i feltet Antal for at bestemme beløbet på fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="12c94-137">This amount is multiplied by the value in the Quantity field to determine the invoice line amount.</span></span>  
22. <span data-ttu-id="12c94-138">Få vist og rediger regnskabsfordelinger for en enkelt linje og eventuelle underordnede linjer.</span><span class="sxs-lookup"><span data-stu-id="12c94-138">View and modify the accounting distributions for an individual line and any child lines.</span></span>
    * <span data-ttu-id="12c94-139">Regnskabsfordelinger bruges til at definere, hvordan et beløb skal håndteres regnskabsmæssigt, f.eks. hvordan indtægt, skat eller afgifter håndteres på en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="12c94-139">Accounting distributions define how an amount will be accounted for, such as how the revenue, tax, or charges will be accounted for on a free text invoice.</span></span>  
23. <span data-ttu-id="12c94-140">Opdater regnskabsfordelingerne for den valgte fakturalinje.</span><span class="sxs-lookup"><span data-stu-id="12c94-140">Update the accounting distributions for the selected invoice line.</span></span>
24. <span data-ttu-id="12c94-141">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="12c94-141">Click Close.</span></span>


