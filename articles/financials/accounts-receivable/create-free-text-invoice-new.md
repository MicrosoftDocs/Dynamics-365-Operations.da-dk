--- 
title: Opret en fritekstfaktura
description: I denne artikel vises, hvordan du opretter en fritekstfaktura.
author: mikefalkner
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
ms.author: mfalkner
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: f69505f0c6137121cae92d42d052b244326c8436
ms.openlocfilehash: 2a611bdd4dd97109709ed355eb80471e27413744
ms.contentlocale: da-dk
ms.lasthandoff: 06/28/2018

---

# <a name="create-a-free-text-invoice"></a><span data-ttu-id="e42f3-103">Opret en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="e42f3-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="e42f3-104">I denne artikel vises, hvordan du opretter en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="e42f3-104">This article demonstrates how to create a free text invoice.</span></span> <span data-ttu-id="e42f3-105">I denne procedure skal du bruge USMF-demoregnskabet.</span><span class="sxs-lookup"><span data-stu-id="e42f3-105">For this procedure, use the USMF demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="e42f3-106">Opret en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="e42f3-106">Create a free text invoice</span></span>

1. <span data-ttu-id="e42f3-107">Gå til Debitor > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="e42f3-107">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="e42f3-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="e42f3-108">Click New.</span></span>
3. <span data-ttu-id="e42f3-109">Vælg en værdi i feltet Debitorkonto.</span><span class="sxs-lookup"><span data-stu-id="e42f3-109">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="e42f3-110">Fakturakontoen er som standard den samme konto, der er brugt til debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="e42f3-110">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="e42f3-111">Regnskabsstatus begynder med Igangværende, hvis fakturaen ikke er bogført.</span><span class="sxs-lookup"><span data-stu-id="e42f3-111">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="e42f3-112">Fakturanummeret tildeles, når fakturaen bogføres.</span><span class="sxs-lookup"><span data-stu-id="e42f3-112">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="e42f3-113">Hvis du bruger SEPA-bemyndigelser, udfyldes bemyndigelsen til Direct Debit automatisk med en bemyndigelse, når du vælger debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="e42f3-113">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="e42f3-114">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="e42f3-114">In the Description field, type a value.</span></span>
5. <span data-ttu-id="e42f3-115">Angive et kontonummer uden dimensioner i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="e42f3-115">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="e42f3-116">Du kan også angive et eller flere tegn for hovedkontoen og bruge opslaget til at finde din konto.</span><span class="sxs-lookup"><span data-stu-id="e42f3-116">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="e42f3-117">Du skal angive dimensioner senere i denne vejledning.</span><span class="sxs-lookup"><span data-stu-id="e42f3-117">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="e42f3-118">Udvid oversigtspanelet Linjedetaljer, så du kan føje dimensioner til din hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="e42f3-118">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="e42f3-119">Klik på fanen Økonomisk dimensionslinje.</span><span class="sxs-lookup"><span data-stu-id="e42f3-119">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="e42f3-120">Dimensionerne er kun for den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="e42f3-120">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="e42f3-121">Momsgruppen udfyldes fra kunden.</span><span class="sxs-lookup"><span data-stu-id="e42f3-121">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="e42f3-122">Hvis kunden ikke har en momsgruppe, bruges momsgruppen fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="e42f3-122">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="e42f3-123">Varemomsgruppen hentes fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="e42f3-123">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="e42f3-124">Hvis hovedkontoen ikke har en varemomsgruppe, bruges varemomsgruppen fra momsparametrene i Finans.</span><span class="sxs-lookup"><span data-stu-id="e42f3-124">If the main account does not have an item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="e42f3-125">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="e42f3-125">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="e42f3-126">Antallet er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="e42f3-126">The quantity is optional.</span></span>  
9. <span data-ttu-id="e42f3-127">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="e42f3-127">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="e42f3-128">Enhedsprisen er valgfri.</span><span class="sxs-lookup"><span data-stu-id="e42f3-128">The unit price is optional.</span></span>  
    * <span data-ttu-id="e42f3-129">Beløbet beregnes som antallet ganget med enhedsprisen.</span><span class="sxs-lookup"><span data-stu-id="e42f3-129">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="e42f3-130">Du kan dog tilsidesætte denne beregning og angive et beløb.</span><span class="sxs-lookup"><span data-stu-id="e42f3-130">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="e42f3-131">Klik på Moms for at få vist den moms, der er beregnet for din faktura.</span><span class="sxs-lookup"><span data-stu-id="e42f3-131">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="e42f3-132">Du kan få vist momsbeløbene på denne side, eller du kan tilsidesætte beløbene på fanen Regulering.</span><span class="sxs-lookup"><span data-stu-id="e42f3-132">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="e42f3-133">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e42f3-133">Click OK.</span></span>
12. <span data-ttu-id="e42f3-134">Klik på Gebyrer for at føje et gebyr til din faktura.</span><span class="sxs-lookup"><span data-stu-id="e42f3-134">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="e42f3-135">Skriv en værdi i feltet Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="e42f3-135">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="e42f3-136">Indtast et tal i feltet Gebyrværdi.</span><span class="sxs-lookup"><span data-stu-id="e42f3-136">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="e42f3-137">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e42f3-137">Close the page.</span></span>
16. <span data-ttu-id="e42f3-138">Klik på Totaler for at få vist opsummerede fakturadetaljer og totaler.</span><span class="sxs-lookup"><span data-stu-id="e42f3-138">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="e42f3-139">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="e42f3-139">Click Close.</span></span>
18. <span data-ttu-id="e42f3-140">Klik på Bogfør for at bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="e42f3-140">Click Post to post the invoice.</span></span> <span data-ttu-id="e42f3-141">Du kan annullere, før du bogfører.</span><span class="sxs-lookup"><span data-stu-id="e42f3-141">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="e42f3-142">Sådan ændrer du tidspunktet for fakturaudskrivning: Vælg Aktuel for at udskrive hver faktura, når den opdateres, eller vælg Efter for at udskrive alle fakturaer, der er blevet opdateret.</span><span class="sxs-lookup"><span data-stu-id="e42f3-142">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="e42f3-143">Hvis du vil ændre, hvordan kundens kreditmaksimum kontrolleres før bogføring, skal du ændre kreditmaksimumtypen.</span><span class="sxs-lookup"><span data-stu-id="e42f3-143">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="e42f3-144">Hvis du vil udskrive fakturaen, skal du vælge Ja.</span><span class="sxs-lookup"><span data-stu-id="e42f3-144">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="e42f3-145">Hvis du vil bogføre fakturaen, skal du vælge Ja.</span><span class="sxs-lookup"><span data-stu-id="e42f3-145">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="e42f3-146">Du kan udskrive fakturaen uden bogføring.</span><span class="sxs-lookup"><span data-stu-id="e42f3-146">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="e42f3-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="e42f3-147">Click OK.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="e42f3-148">Kopiér linjer</span><span class="sxs-lookup"><span data-stu-id="e42f3-148">Copy lines</span></span>
<span data-ttu-id="e42f3-149">Hvis du vil kopiere linjer i fritekstfakturaen, skal du vælge en eller flere linjer og derefter klikke på Kopier valgte linjer.</span><span class="sxs-lookup"><span data-stu-id="e42f3-149">To copy lines on the free text invoice, select one or more lines and then click Copy selected lines.</span></span> <span data-ttu-id="e42f3-150">Du kan angive antallet kopier, du vil foretage, og du kan også kopiere noter og vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="e42f3-150">You can specify the number of copies that you want to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="e42f3-151">Du kan kopiere fordelingerne, eller tillade at de oprettes igen, når du bogfører.</span><span class="sxs-lookup"><span data-stu-id="e42f3-151">You can copy the distributions or allow them to be recreated when you post.</span></span> <span data-ttu-id="e42f3-152">Når du har kopieret linjerne, kan du derefter redigere oplysningerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="e42f3-152">Once you copy the lines, you can edit the information as needed.</span></span> 

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="e42f3-153">Oprette en fritekstfaktura fra en skabelon</span><span class="sxs-lookup"><span data-stu-id="e42f3-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="e42f3-154">Du kan oprette en fritekstfaktura fra en skabelon.</span><span class="sxs-lookup"><span data-stu-id="e42f3-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="e42f3-155">Når du vælger Ny ud fra skabelon under fanen Faktura, kan du vælge et skabelonnavn og debitorkontoen for den nye fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="e42f3-155">When you select New from template from the Invoice tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="e42f3-156">Du kan også vælge at bruge standardværdier, f.eks. betalingsbetingelserne og betalingsmåden fra debitoren, eller du kan bruge de værdier, der blev gemt sammen med skabelonen.</span><span class="sxs-lookup"><span data-stu-id="e42f3-156">You can also choose to default values such as the terms of payment and method of payment from the customer or use the values that were saved with the template.</span></span> <span data-ttu-id="e42f3-157">Der oprettes en ny fritekstfaktura, og du kan redigere værdierne i fakturaen.</span><span class="sxs-lookup"><span data-stu-id="e42f3-157">A new free text invoice will be created and you can edit the values in that invoice.</span></span> 


