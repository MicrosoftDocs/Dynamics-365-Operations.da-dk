---
title: Oprette en fritekstfaktura
description: Dette emne forklarer, hvordan du opretter fritekstfakturaer.
author: mikefalkner
manager: AnnBe
ms.date: 08/24/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: roschlom
ms.search.validFrom: 2018-08-30
ms.dyn365.ops.version: 8.0.4
ms.openlocfilehash: 7ccc652a407e9ed09c2ffffd3c86ff5070d6399b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5217500"
---
# <a name="create-a-free-text-invoice"></a><span data-ttu-id="cd609-103">Oprette en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="cd609-103">Create a free text invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cd609-104">Dette emne forklarer, hvordan du opretter fritekstfakturaer.</span><span class="sxs-lookup"><span data-stu-id="cd609-104">This topic explains how to create free text invoices.</span></span> <span data-ttu-id="cd609-105">I proceduren skal du bruge **USMF**-demoregnskabet.</span><span class="sxs-lookup"><span data-stu-id="cd609-105">For the procedure, use the **USMF** demo company.</span></span>

## <a name="create-a-free-text-invoice"></a><span data-ttu-id="cd609-106">Opret en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="cd609-106">Create a free text invoice</span></span>

1. <span data-ttu-id="cd609-107">Gå til **Debitor (eller salgsfinanskonto) \> Fakturaer \> Alle fritekstfakturaer**.</span><span class="sxs-lookup"><span data-stu-id="cd609-107">Go to **Accounts receivable (or Sales Ledger) \> Invoices \> All free text invoices**.</span></span>
2. <span data-ttu-id="cd609-108">Vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="cd609-108">Select **New**.</span></span>
3. <span data-ttu-id="cd609-109">Vælg en værdi i feltet **Debitorkonto**.</span><span class="sxs-lookup"><span data-stu-id="cd609-109">In the **Customer account** field, select a value.</span></span>

    * <span data-ttu-id="cd609-110">Fakturakontoen er som standard konto, der er valgt som debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="cd609-110">By default, the account that is selected as the customer account is used as the invoice account.</span></span>
    * <span data-ttu-id="cd609-111">Regnskabsstatus begynder med **Igangværende**, hvis fakturaen ikke er bogført.</span><span class="sxs-lookup"><span data-stu-id="cd609-111">If the invoice isn't posted, the accounting status starts with **In process**.</span></span>
    * <span data-ttu-id="cd609-112">Fakturanummeret tildeles, når fakturaen bogføres.</span><span class="sxs-lookup"><span data-stu-id="cd609-112">The invoice number will be assigned when the invoice is posted.</span></span>
    * <span data-ttu-id="cd609-113">Hvis du bruger bemyndigelser af typen Fælles eurobetalingsområde (SEPA), angives bemyndigelsen til Direct Debit automatisk, når du vælger debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="cd609-113">If you're using Single Euro Payments Area (SEPA) mandates, the direct debit mandate is automatically entered when you select the customer account.</span></span>

4. <span data-ttu-id="cd609-114">Indtast en værdi i feltet **Beskrivelse**.</span><span class="sxs-lookup"><span data-stu-id="cd609-114">In the **Description** field, enter a value.</span></span>
5. <span data-ttu-id="cd609-115">Angiv et kontonummer, der ikke har dimensioner, i feltet **Hovedkonto**.</span><span class="sxs-lookup"><span data-stu-id="cd609-115">In the **Main account** field, specify an account number that doesn't have dimensions.</span></span> <span data-ttu-id="cd609-116">Du skal angive dimensioner senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="cd609-116">You will enter dimensions later in this topic.</span></span>

    <span data-ttu-id="cd609-117">Du kan også angive et eller flere tegn for hovedkontoen og bruge opslaget til at finde kontoen.</span><span class="sxs-lookup"><span data-stu-id="cd609-117">You can also enter one or more characters for the main account, and use the lookup to find the account.</span></span>

6. <span data-ttu-id="cd609-118">Vælg oversigtspanelet **Linjedetaljer** for at føje dimensioner til hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="cd609-118">Select the **Line details** FastTab to add dimensions to the main account.</span></span>
7. <span data-ttu-id="cd609-119">Vælg fanen **Økonomisk dimensionslinje**.</span><span class="sxs-lookup"><span data-stu-id="cd609-119">Select the **Financial dimensions line** tab.</span></span>

    * <span data-ttu-id="cd609-120">Dimensionerne er kun for den valgte linje.</span><span class="sxs-lookup"><span data-stu-id="cd609-120">The dimensions are for the selected line only.</span></span>
    * <span data-ttu-id="cd609-121">Momsgruppen udfyldes som standard fra debitoren.</span><span class="sxs-lookup"><span data-stu-id="cd609-121">The sales tax group is filled in from the customer.</span></span> <span data-ttu-id="cd609-122">Hvis debitoren ikke har en momsgruppe, bruges momsgruppen fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="cd609-122">If the customer doesn't have a sales tax group, the sales tax group from the main account is used.</span></span>
    * <span data-ttu-id="cd609-123">Varemomsgruppen udfyldes fra hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="cd609-123">The items sales tax group is filled in from the main account.</span></span> <span data-ttu-id="cd609-124">Hvis hovedkontoen ikke har en varemomsgruppe, bruges den varemomsgruppe, der er angivet i momsparametrene i Finans.</span><span class="sxs-lookup"><span data-stu-id="cd609-124">If the main account doesn't have an item sales tax group, the item sales tax group that is specified in the sales tax parameters in General ledger is used.</span></span>

8. <span data-ttu-id="cd609-125">Valgfrit: Angiv et tal i feltet **Antal**.</span><span class="sxs-lookup"><span data-stu-id="cd609-125">Optional: In the **Quantity** field, enter a number.</span></span>
9. <span data-ttu-id="cd609-126">Valgfrit: Angiv et nummer i feltet **Enhedspris**.</span><span class="sxs-lookup"><span data-stu-id="cd609-126">Optional: In the **Unit price** field, enter a number.</span></span>

    <span data-ttu-id="cd609-127">Beløbet beregnes som antallet ganget med enhedsprisen.</span><span class="sxs-lookup"><span data-stu-id="cd609-127">The amount is calculated as the quantity times the unit price.</span></span> <span data-ttu-id="cd609-128">Du kan dog tilsidesætte denne beregning ved at angive et beløb.</span><span class="sxs-lookup"><span data-stu-id="cd609-128">However, you can override that calculation by entering an amount.</span></span>

10. <span data-ttu-id="cd609-129">Vælg **Moms** for at få vist den moms, der er beregnet for fakturaen.</span><span class="sxs-lookup"><span data-stu-id="cd609-129">Select **Sales tax** to view the sales tax that is calculated for the invoice.</span></span>

    <span data-ttu-id="cd609-130">Du kan få vist momsbeløbene på denne side, eller du kan tilsidesætte beløbene under fanen **Regulering**.</span><span class="sxs-lookup"><span data-stu-id="cd609-130">You can view the sales tax amounts on this page, or you can override the amounts on the **Adjustment** tab.</span></span>

11. <span data-ttu-id="cd609-131">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd609-131">Select **OK**.</span></span>
12. <span data-ttu-id="cd609-132">Vælg **Gebyrer** for at føje et gebyr til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="cd609-132">Select **Charges** to add a charge to the invoice.</span></span>
13. <span data-ttu-id="cd609-133">Skriv en værdi i feltet **Gebyrkode**.</span><span class="sxs-lookup"><span data-stu-id="cd609-133">In the **Charges code** field, enter a value.</span></span>
14. <span data-ttu-id="cd609-134">Indtast et tal i feltet **Gebyrværdi**.</span><span class="sxs-lookup"><span data-stu-id="cd609-134">In the **Charges value** field, enter a number.</span></span>
15. <span data-ttu-id="cd609-135">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="cd609-135">Close the page.</span></span>
16. <span data-ttu-id="cd609-136">Vælg **Totaler** for at få vist en opsummering af fakturadetaljerne og totalerne.</span><span class="sxs-lookup"><span data-stu-id="cd609-136">Select **Totals** to view a summary of the invoice details and totals.</span></span>
17. <span data-ttu-id="cd609-137">Vælg **Luk**.</span><span class="sxs-lookup"><span data-stu-id="cd609-137">Select **Close**.</span></span>
18. <span data-ttu-id="cd609-138">Vælg **Bogfør** for at bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="cd609-138">Select **Post** to post the invoice.</span></span> <span data-ttu-id="cd609-139">Du har stadig mulighed for at annullere, før du bogfører.</span><span class="sxs-lookup"><span data-stu-id="cd609-139">You will still have an opportunity to cancel before you actually post.</span></span>

    * <span data-ttu-id="cd609-140">Du kan ændre tidspunktet for udskrivning af fakturaer.</span><span class="sxs-lookup"><span data-stu-id="cd609-140">You can change the timing of invoice printing.</span></span> <span data-ttu-id="cd609-141">Vælg **Aktuel** for at udskrive hver faktura, når den opdateres.</span><span class="sxs-lookup"><span data-stu-id="cd609-141">Select **Current** to print each invoice as it's updated.</span></span> <span data-ttu-id="cd609-142">Vælg **Efter** for at udskrive alle fakturaer, der er blevet opdateret.</span><span class="sxs-lookup"><span data-stu-id="cd609-142">Select **After** to print after all invoices have been updated.</span></span>
    * <span data-ttu-id="cd609-143">Hvis du vil ændre, hvordan debitors kreditmaksimum kontrolleres, før fakturaen bogføres, kan du ændre værdien i feltet **Kreditmaksimumtype**.</span><span class="sxs-lookup"><span data-stu-id="cd609-143">To change how the customer's credit limit is verified before the invoice is posted, change the value in the **Credit limit type** field.</span></span>
    * <span data-ttu-id="cd609-144">Vælg **Ja** i denne indstilling for at udskrive fakturaen.</span><span class="sxs-lookup"><span data-stu-id="cd609-144">To print the invoice, set the option to **Yes**.</span></span>
    * <span data-ttu-id="cd609-145">Vælg **Ja** i denne indstilling for at bogføre fakturaen.</span><span class="sxs-lookup"><span data-stu-id="cd609-145">To post the invoice, set the option to **Yes**.</span></span> <span data-ttu-id="cd609-146">Du kan udskrive fakturaen uden at bogføre den.</span><span class="sxs-lookup"><span data-stu-id="cd609-146">You can print the invoice without posting it.</span></span>

19. <span data-ttu-id="cd609-147">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd609-147">Select **OK**.</span></span>

## <a name="copy-lines"></a><span data-ttu-id="cd609-148">Kopiér linjer</span><span class="sxs-lookup"><span data-stu-id="cd609-148">Copy lines</span></span>
<span data-ttu-id="cd609-149">Hvis du vil kopiere linjer i en fritekstfaktura, skal du vælge en eller flere linjer og derefter vælge **Kopier valgte linjer**.</span><span class="sxs-lookup"><span data-stu-id="cd609-149">To copy lines on a free text invoice, select one or more lines, and then select **Copy selected lines**.</span></span> <span data-ttu-id="cd609-150">Du kan angive antallet kopier, der skal tages, og du kan også kopiere noter og vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="cd609-150">You can specify the number of copies to make, and you can also copy notes and attachments.</span></span> <span data-ttu-id="cd609-151">Du kan enten kopiere fordelingerne eller lade, at de oprettes igen, når du bogfører.</span><span class="sxs-lookup"><span data-stu-id="cd609-151">You can either copy the distributions or let them be re-created when you post.</span></span>

<span data-ttu-id="cd609-152">Når du har kopieret linjerne, kan du derefter redigere oplysningerne efter behov.</span><span class="sxs-lookup"><span data-stu-id="cd609-152">After you copy lines, you can edit the information as you require.</span></span>

## <a name="create-a-free-text-invoice-from-a-template"></a><span data-ttu-id="cd609-153">Oprette en fritekstfaktura fra en skabelon</span><span class="sxs-lookup"><span data-stu-id="cd609-153">Create a free text invoice from a template</span></span>
<span data-ttu-id="cd609-154">Du kan oprette en fritekstfaktura fra en skabelon.</span><span class="sxs-lookup"><span data-stu-id="cd609-154">You can create a free text invoice from a template.</span></span> <span data-ttu-id="cd609-155">Når du vælger **Ny ud fra skabelon** under fanen **Faktura**, kan du vælge et skabelonnavn og debitorkontoen for den nye fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="cd609-155">When you select **New from template** on the **Invoice** tab, you can select a template name and the customer account for the new free text invoice.</span></span> <span data-ttu-id="cd609-156">Standardværdier, f.eks. betalingsbetingelserne og betalingsmåden, kan udfyldes automatisk fra debitoren, eller du kan bruge de værdier, der blev gemt i skabelonen.</span><span class="sxs-lookup"><span data-stu-id="cd609-156">Default values, such as the terms of payment and method of payment, can be automatically filled in from the customer, or you can use the values that were saved in the template.</span></span>

<span data-ttu-id="cd609-157">Der oprettes en ny fritekstfaktura, og du kan redigere værdierne efter behov.</span><span class="sxs-lookup"><span data-stu-id="cd609-157">A new free text invoice is created, and you can edit the values as you require.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]