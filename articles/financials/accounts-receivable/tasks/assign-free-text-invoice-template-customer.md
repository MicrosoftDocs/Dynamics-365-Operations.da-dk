--- 
title: Tildel en fritekstfakturaskabelon til en debitor.
description: Denne opgaver viser, hvordan du tildeler en fritekstfakturaskabelon til en debitor.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 317b3bd4c1f395987ef3dbbd268c40be5c688320
ms.contentlocale: da-dk
ms.lasthandoff: 09/14/2018

---
# <a name="assign-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="58571-103">Tildel en fritekstfakturaskabelon til en debitor.</span><span class="sxs-lookup"><span data-stu-id="58571-103">Assign free text invoice template to a customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="58571-104">Denne opgaver viser, hvordan du tildeler en fritekstfakturaskabelon til en debitor.</span><span class="sxs-lookup"><span data-stu-id="58571-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="58571-105">Denne opgave bruger USMF-demofirmaet og er beregnet til den bruger, der er ansvarlig for håndtering af og behandling af debitorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="58571-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="58571-106">Gå til Debitor > Kunder > Alle kunder.</span><span class="sxs-lookup"><span data-stu-id="58571-106">Go to Accounts receivable > Customers > All customers.</span></span>
2. <span data-ttu-id="58571-107">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="58571-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="58571-108">Klik på Faktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="58571-108">On the Action Pane, click Invoice.</span></span>
4. <span data-ttu-id="58571-109">Klik på Tilbagevendende fakturaer.</span><span class="sxs-lookup"><span data-stu-id="58571-109">Click Recurring invoices.</span></span>
    * <span data-ttu-id="58571-110">Du kan bruge denne side til at knytte fritekstfakturaskabeloner til debitorer og angive, hvor ofte fakturaer sendes til debitoren.</span><span class="sxs-lookup"><span data-stu-id="58571-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="58571-111">Klik på Ny for at tildele en ny skabelon til debitoren.</span><span class="sxs-lookup"><span data-stu-id="58571-111">Click New to assign a new template to the customer.</span></span>
6. <span data-ttu-id="58571-112">Vælg den fritekstfakturaskabelon, du vil tildele debitoren.</span><span class="sxs-lookup"><span data-stu-id="58571-112">Select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="58571-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="58571-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="58571-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="58571-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="58571-115">Angiv den dato, hvor den første faktura vil blive genereret.</span><span class="sxs-lookup"><span data-stu-id="58571-115">Enter the date when the first invoice will be generated.</span></span>
    * <span data-ttu-id="58571-116">Angiv en tilbagevendende slutdato.</span><span class="sxs-lookup"><span data-stu-id="58571-116">Enter a recurring end date.</span></span>  
    * <span data-ttu-id="58571-117">Vælg en af følgende: Slutdato mangler – Fakturaer genereres i det uendelige, indtil skabelonen fjernes fra debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="58571-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>  <span data-ttu-id="58571-118">Faktureringsslutdato – Vælg denne indstilling, og angiv den sidste dato, hvor fakturaen kan genereres.</span><span class="sxs-lookup"><span data-stu-id="58571-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
    * <span data-ttu-id="58571-119">Maksimalt akkumuleret beløb, hvorefter genereringen af fakturaer stopper.</span><span class="sxs-lookup"><span data-stu-id="58571-119">Maximum cumulative amount after which invoice generation will stop.</span></span>  
    * <span data-ttu-id="58571-120">Indtast det maksimale akkumulerede beløb, der kan nås med den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="58571-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="58571-121">Hvis du f.eks. indtaster 1.000,00 og genererer månedlige fakturaer for hver 100,00, stopper genereringen af fakturaer, når den 10. faktura er genereret.</span><span class="sxs-lookup"><span data-stu-id="58571-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
    * <span data-ttu-id="58571-122">Generer tilbagevendende fakturaer ved hjælp af standardværdierne fra enten fritekstfakturaskabelonen eller debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="58571-122">Generate recurring invoices by using the default values from either free text invoice template or the customer account.</span></span>  
    * <span data-ttu-id="58571-123">Vælg, om du vil bruge skabelonen til fritekstfakturaer eller debitorkontoen til at bestemme standardværdierne for sprog, posteringsprofil, momsgruppe, varemomsgruppe, listekode, land/region til levering, valuta, betalingsbetingelser, betalingsmetode, betalingsspecifikation, betalingsplan, kasserabat, økonomiske dimensioner og giroindbetalingskort, når fakturaer oprettes.</span><span class="sxs-lookup"><span data-stu-id="58571-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
10. <span data-ttu-id="58571-124">Vælg gentagelsesmønsteret.</span><span class="sxs-lookup"><span data-stu-id="58571-124">Select the recurrence pattern.</span></span>
    * <span data-ttu-id="58571-125">Dagligt – Vælg denne indstilling, og indtast antallet af dage i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="58571-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="58571-126">Hvis du f.eks. indtaster 15, genereres der en faktura til debitoren hver 15. dag.</span><span class="sxs-lookup"><span data-stu-id="58571-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>  <span data-ttu-id="58571-127">Ugentligt – Vælg denne indstilling, og indtast antallet af uger i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="58571-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="58571-128">Hvis du f.eks. indtaster 2, genereres der en faktura til debitoren hver anden uge.</span><span class="sxs-lookup"><span data-stu-id="58571-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>  <span data-ttu-id="58571-129">Månedligt – Vælg denne indstilling, og indtast antallet af måneder i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="58571-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="58571-130">Hvis du f.eks. indtaster 6, genereres der en faktura til denne debitor hver sjette måned.</span><span class="sxs-lookup"><span data-stu-id="58571-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>  <span data-ttu-id="58571-131">Årligt – Vælg denne indstilling, og indtast antallet af år i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="58571-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="58571-132">Hvis du f.eks. indtaster 2, genereres der en faktura til debitoren hvert andet år.</span><span class="sxs-lookup"><span data-stu-id="58571-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
11. <span data-ttu-id="58571-133">Angiv et tal i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="58571-133">In the Per field, enter a number.</span></span>


