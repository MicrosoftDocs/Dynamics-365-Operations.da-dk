--- 
title: Opret en fritekstfaktura
description: Denne opgaveguide viser, hvordan du opretter en fritekstfaktura.
author: mikefalkner
manager: AnnBe
ms.date: 10/23/2016
ms.topic: business-process
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
ms.sourcegitcommit: 7e0a5d044133b917a3eb9386773205218e5c1b40
ms.openlocfilehash: 33324a9b95026600bcc6facb9c22a04fd2e323c8
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="5179f-103">Opret en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="5179f-103">Create a free text invoice</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5179f-104">Denne opgaveguide viser, hvordan du opretter en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="5179f-104">This task guide demonstrates creating a free text invoice.</span></span> <span data-ttu-id="5179f-105">Denne opgave bruger demofirmaet USMF.</span><span class="sxs-lookup"><span data-stu-id="5179f-105">This task uses the USMF demo company.</span></span>

1. <span data-ttu-id="5179f-106">Gå til Debitor > Fakturaer > Alle fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="5179f-106">Go to Accounts receivable > Invoices > All free text invoices.</span></span>
2. <span data-ttu-id="5179f-107">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="5179f-107">Click New.</span></span>
3. <span data-ttu-id="5179f-108">Vælg en værdi i feltet Debitorkonto.</span><span class="sxs-lookup"><span data-stu-id="5179f-108">In the Customer account field, select a value.</span></span>
    * <span data-ttu-id="5179f-109">Fakturakontoen er som standard den samme konto, der er brugt til debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="5179f-109">The invoice account will default to the same account used for the customer account.</span></span>   
    * <span data-ttu-id="5179f-110">Regnskabsstatus begynder med Igangværende, hvis fakturaen ikke er bogført.</span><span class="sxs-lookup"><span data-stu-id="5179f-110">The accounting status starts with In process if the invoice is not posted.</span></span>   
    * <span data-ttu-id="5179f-111">Fakturanummeret tildeles, når fakturaen bogføres.</span><span class="sxs-lookup"><span data-stu-id="5179f-111">The invoice number will be assigned when the invoice is posted.</span></span>  
    * <span data-ttu-id="5179f-112">Hvis du bruger SEPA-bemyndigelser, udfyldes bemyndigelsen til Direct Debit automatisk med en bemyndigelse, når du vælger debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="5179f-112">If you are using SEPA mandates, the direct debit mandate will be automatically populated with a mandate when you select the customer account.</span></span>  
4. <span data-ttu-id="5179f-113">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="5179f-113">In the Description field, type a value.</span></span>
5. <span data-ttu-id="5179f-114">Angive et kontonummer uden dimensioner i feltet Hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="5179f-114">In the Main account field, specify an account number without dimensions.</span></span>
    * <span data-ttu-id="5179f-115">Du kan også angive et eller flere tegn for hovedkontoen og bruge opslaget til at finde din konto.</span><span class="sxs-lookup"><span data-stu-id="5179f-115">You can also enter one or more characters for the main account and use the lookup to find your account.</span></span> <span data-ttu-id="5179f-116">Du skal angive dimensioner senere i denne vejledning.</span><span class="sxs-lookup"><span data-stu-id="5179f-116">You will enter dimensions later on in this guide.</span></span>  
6. <span data-ttu-id="5179f-117">Udvid oversigtspanelet Linjedetaljer, så du kan føje dimensioner til din hovedkonto.</span><span class="sxs-lookup"><span data-stu-id="5179f-117">Expand the Line details fasttab so you can add dimensions to your main account.</span></span>
7. <span data-ttu-id="5179f-118">Klik på fanen Økonomisk dimensionslinje.</span><span class="sxs-lookup"><span data-stu-id="5179f-118">Click the Financial dimensions line tab.</span></span>
    * <span data-ttu-id="5179f-119">Dimensionerne er kun for den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="5179f-119">The dimensions are for the selected line only.</span></span>    
    * <span data-ttu-id="5179f-120">Momsgruppen udfyldes fra kunden.</span><span class="sxs-lookup"><span data-stu-id="5179f-120">The sales tax group is populated from the customer.</span></span> <span data-ttu-id="5179f-121">Hvis kunden ikke har en momsgruppe, bruges momsgruppen fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="5179f-121">If the customer does not have a sales tax group, the sales tax group from the main account is used.</span></span>  
    * <span data-ttu-id="5179f-122">Varemomsgruppen hentes fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="5179f-122">The items sales tax group is populated from the main account.</span></span> <span data-ttu-id="5179f-123">Hvis hovedkontoen ikke har en varemomsgruppe, bruges varemomsgruppen fra momsparametrene i Finans.</span><span class="sxs-lookup"><span data-stu-id="5179f-123">If the main account does not have a item sales tax group, then the item sales tax group in the General ledger sales tax parameters is used.</span></span>    
8. <span data-ttu-id="5179f-124">Angiv et tal i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="5179f-124">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="5179f-125">Antallet er valgfrit.</span><span class="sxs-lookup"><span data-stu-id="5179f-125">The quantity is optional.</span></span>  
9. <span data-ttu-id="5179f-126">Angiv et tal i feltet Enhedspris.</span><span class="sxs-lookup"><span data-stu-id="5179f-126">In the Unit price field, enter a number.</span></span>
    * <span data-ttu-id="5179f-127">Enhedsprisen er valgfri.</span><span class="sxs-lookup"><span data-stu-id="5179f-127">The unit price is optional.</span></span>  
    * <span data-ttu-id="5179f-128">Beløbet beregnes som antallet ganget med enhedsprisen.</span><span class="sxs-lookup"><span data-stu-id="5179f-128">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="5179f-129">Du kan dog tilsidesætte denne beregning og angive et beløb.</span><span class="sxs-lookup"><span data-stu-id="5179f-129">However, you can override that calculation and enter an amount.</span></span>  
10. <span data-ttu-id="5179f-130">Klik på Moms for at få vist den moms, der er beregnet for din faktura.</span><span class="sxs-lookup"><span data-stu-id="5179f-130">Click on Sales tax to view the sales tax calculated for your invoice.</span></span>
    * <span data-ttu-id="5179f-131">Du kan få vist momsbeløbene på denne side, eller du kan tilsidesætte beløbene på fanen Regulering.</span><span class="sxs-lookup"><span data-stu-id="5179f-131">View the sales tax amounts in this page or you can override the amounts on the Adjustment tab.</span></span>  
11. <span data-ttu-id="5179f-132">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5179f-132">Click OK.</span></span>
12. <span data-ttu-id="5179f-133">Klik på Gebyrer for at føje et gebyr til din faktura.</span><span class="sxs-lookup"><span data-stu-id="5179f-133">Click Charges to add a charge to your invoice.</span></span> 
13. <span data-ttu-id="5179f-134">Skriv en værdi i feltet Gebyrkode.</span><span class="sxs-lookup"><span data-stu-id="5179f-134">In the Charges code field, type a value.</span></span>
14. <span data-ttu-id="5179f-135">Indtast et tal i feltet Gebyrværdi.</span><span class="sxs-lookup"><span data-stu-id="5179f-135">In the Charges value field, enter a number.</span></span>
15. <span data-ttu-id="5179f-136">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="5179f-136">Close the page.</span></span>
16. <span data-ttu-id="5179f-137">Klik på Totaler for at få vist opsummerede fakturadetaljer og totaler.</span><span class="sxs-lookup"><span data-stu-id="5179f-137">Click Totals to view the summary invoice details and totals.</span></span>
17. <span data-ttu-id="5179f-138">Klik på Luk.</span><span class="sxs-lookup"><span data-stu-id="5179f-138">Click Close.</span></span>
18. <span data-ttu-id="5179f-139">Klik på Bogfør for at bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="5179f-139">Click Post to post the invoice.</span></span> <span data-ttu-id="5179f-140">Du kan annullere, før du bogfører.</span><span class="sxs-lookup"><span data-stu-id="5179f-140">You will be able to cancel before you post.</span></span>
    * <span data-ttu-id="5179f-141">Sådan ændrer du tidspunktet for fakturaudskrivning: Vælg Aktuel for at udskrive hver faktura, når den opdateres, eller vælg Efter for at udskrive alle fakturaer, der er blevet opdateret.</span><span class="sxs-lookup"><span data-stu-id="5179f-141">To change the timing of your invoice printing:  Select Current to print each invoice as it is updated   or  Select After to print after all invoices have been updated.</span></span>  
    * <span data-ttu-id="5179f-142">Hvis du vil ændre, hvordan kundens kreditmaksimum kontrolleres før bogføring, skal du ændre kreditmaksimumtypen.</span><span class="sxs-lookup"><span data-stu-id="5179f-142">If you want to change how the customer's credit limit is checked before posting, change the Credit limit type.</span></span>  
    * <span data-ttu-id="5179f-143">Hvis du vil udskrive fakturaen, skal du vælge Ja.</span><span class="sxs-lookup"><span data-stu-id="5179f-143">If you want to print the invoice, select Yes.</span></span>  
    * <span data-ttu-id="5179f-144">Hvis du vil bogføre fakturaen, skal du vælge Ja.</span><span class="sxs-lookup"><span data-stu-id="5179f-144">If you want to post the invoice, select Yes.</span></span> <span data-ttu-id="5179f-145">Du kan udskrive fakturaen uden bogføring.</span><span class="sxs-lookup"><span data-stu-id="5179f-145">You can print the invoice without posting.</span></span>  
19. <span data-ttu-id="5179f-146">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="5179f-146">Click OK.</span></span>


