---
title: Tildele en skabelon til fritekstfakturaer til en debitor
description: Denne opgaver viser, hvordan du tildeler en fritekstfakturaskabelon til en debitor.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 08/12/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustTable, CustRecurrenceInvoice
audience: Application User
ms.reviewer: roschlom
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d1f87c731a603dbb3def0ebc2d2ebe54f9706053
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5254101"
---
# <a name="assign-a-free-text-invoice-template-to-a-customer"></a><span data-ttu-id="3cdda-103">Tildele en skabelon til fritekstfakturaer til en debitor</span><span class="sxs-lookup"><span data-stu-id="3cdda-103">Assign a free text invoice template to a customer</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3cdda-104">Denne opgaver viser, hvordan du tildeler en fritekstfakturaskabelon til en debitor.</span><span class="sxs-lookup"><span data-stu-id="3cdda-104">This task demonstrates how to assign a free text invoice template to a customer.</span></span> <span data-ttu-id="3cdda-105">Denne opgave bruger USMF-demofirmaet og er beregnet til den bruger, der er ansvarlig for håndtering af og behandling af debitorfakturaer.</span><span class="sxs-lookup"><span data-stu-id="3cdda-105">This task uses the USMF demo company and is intended for the user who is responsible for managing and processing A/R invoices.</span></span>

1. <span data-ttu-id="3cdda-106">I **navigationsruden** skal du gå til **Moduler > Debitor > Debitorer > Alle kunder**.</span><span class="sxs-lookup"><span data-stu-id="3cdda-106">In the **Navigation pane**, go to **Modules > Accounts receivable > Customers > All customers**.</span></span>
2. <span data-ttu-id="3cdda-107">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3cdda-107">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3cdda-108">Klik på **Faktura** i **handlingsruden**.</span><span class="sxs-lookup"><span data-stu-id="3cdda-108">On the **Action Pane**, click **Invoice**.</span></span>
4. <span data-ttu-id="3cdda-109">Klik på **Tilbagevendende fakturaer**.</span><span class="sxs-lookup"><span data-stu-id="3cdda-109">Click **Recurring invoices**.</span></span> <span data-ttu-id="3cdda-110">Du kan bruge denne side til at knytte fritekstfakturaskabeloner til debitorer og angive, hvor ofte fakturaer sendes til debitoren.</span><span class="sxs-lookup"><span data-stu-id="3cdda-110">Use this page to assign free text invoice templates to customers and specify how frequently invoices will be sent to the customer.</span></span>  
5. <span data-ttu-id="3cdda-111">Klik på **Ny** for at tildele debitoren en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="3cdda-111">Click **New** to assign a new template to the customer.</span></span>
6. <span data-ttu-id="3cdda-112">Vælg den fritekstfakturaskabelon, du vil tildele debitoren, i feltet **Skabelon**.</span><span class="sxs-lookup"><span data-stu-id="3cdda-112">In the **Template** field, select the free text invoice template you want to assign to the customer.</span></span>
7. <span data-ttu-id="3cdda-113">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="3cdda-113">In the list, find and select the desired record.</span></span>
8. <span data-ttu-id="3cdda-114">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="3cdda-114">In the list, click the link in the selected row.</span></span>
9. <span data-ttu-id="3cdda-115">Angiv den dato, hvor den første faktura skal genereres, i feltet **Faktureringsstartdato**.</span><span class="sxs-lookup"><span data-stu-id="3cdda-115">In the **Billing start date** field, enter the date when the first invoice will be generated.</span></span>
10. <span data-ttu-id="3cdda-116">Angiv en slutdato for gentagelse i sektionen **Slut på gentagelse**.</span><span class="sxs-lookup"><span data-stu-id="3cdda-116">In the **Recurrence end** section, enter a recurring end date.</span></span>  
    * <span data-ttu-id="3cdda-117">Vælg en af følgende: Slutdato mangler – Fakturaer genereres i det uendelige, indtil skabelonen fjernes fra debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="3cdda-117">Select one of the following: No end date – Invoices will be generated indefinitely until the template is removed from the customer account.</span></span>
    * <span data-ttu-id="3cdda-118">Faktureringsslutdato – Vælg denne indstilling, og angiv den sidste dato, hvor fakturaen kan genereres.</span><span class="sxs-lookup"><span data-stu-id="3cdda-118">Billing end date – Select this option and enter the last date that the invoice can be generated.</span></span>  
11. <span data-ttu-id="3cdda-119">Angiv det maksimale akkumulerede beløb, efter hvilket fakturagenerering skal stoppe, i feltet **Maksimalt akkumuleret beløb**.</span><span class="sxs-lookup"><span data-stu-id="3cdda-119">In the **Maximum cumulative amount** field, enter the maximum cumulative amount after which invoice generation will stop.</span></span> <span data-ttu-id="3cdda-120">Indtast det maksimale akkumulerede beløb, der kan nås med den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="3cdda-120">Enter the maximum cumulative amount that can be reached using the selected template.</span></span> <span data-ttu-id="3cdda-121">Hvis du f.eks. indtaster 1.000,00 og genererer månedlige fakturaer for hver 100,00, stopper genereringen af fakturaer, når den 10. faktura er genereret.</span><span class="sxs-lookup"><span data-stu-id="3cdda-121">For example, if you enter 1,000.00 and generate monthly invoices for 100.00 each, invoices will stop generating after the tenth invoice is generated.</span></span>  
12. <span data-ttu-id="3cdda-122">I sektionen **Generer tilbagevendende fakturaer ved hjælp af standardværdierne fra** skal du enten vælge fritekstfakturaskabelonen eller debitorkontoen.</span><span class="sxs-lookup"><span data-stu-id="3cdda-122">In the **Generate recurring invoices by using the default values from** section, select either free text invoice template or the customer account.</span></span> <span data-ttu-id="3cdda-123">Vælg, om du vil bruge skabelonen til fritekstfakturaer eller debitorkontoen til at bestemme standardværdierne for sprog, posteringsprofil, momsgruppe, varemomsgruppe, listekode, land/region til levering, valuta, betalingsbetingelser, betalingsmetode, betalingsspecifikation, betalingsplan, kasserabat, økonomiske dimensioner og giroindbetalingskort, når fakturaer oprettes.</span><span class="sxs-lookup"><span data-stu-id="3cdda-123">Select whether to use the free text invoice template or the customer account to determine the default values for the language, posting profile, sales tax group, item sales tax group, list code, country/region for delivery, currency, terms of payment, method of payment, payment specification, payment schedule, cash discount, financial dimensions, and giro money transfer slip when invoices are created.</span></span>  
13. <span data-ttu-id="3cdda-124">Vælg gentagelsesmønsteret i feltet **Gentagelsesmønster**.</span><span class="sxs-lookup"><span data-stu-id="3cdda-124">In the **Recurrence pattern** field, select the recurrence pattern.</span></span>
    + <span data-ttu-id="3cdda-125">Dagligt – Vælg denne indstilling, og indtast antallet af dage i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="3cdda-125">Daily – Select this option and enter the number of days in the Per field.</span></span> <span data-ttu-id="3cdda-126">Hvis du f.eks. indtaster 15, genereres der en faktura til debitoren hver 15. dag.</span><span class="sxs-lookup"><span data-stu-id="3cdda-126">For example, if you enter 15, an invoice will be generated every 15 days for this customer.</span></span>
    + <span data-ttu-id="3cdda-127">Ugentligt – Vælg denne indstilling, og indtast antallet af uger i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="3cdda-127">Weekly - Select this option and enter the number of weeks in the Per field.</span></span> <span data-ttu-id="3cdda-128">Hvis du f.eks. indtaster 2, genereres der en faktura til debitoren hver anden uge.</span><span class="sxs-lookup"><span data-stu-id="3cdda-128">For example, if you enter 2, an invoice will be generated every two weeks for this customer.</span></span>
    + <span data-ttu-id="3cdda-129">Månedligt – Vælg denne indstilling, og indtast antallet af måneder i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="3cdda-129">Monthly - Select this option and enter the number of months in the Per field.</span></span> <span data-ttu-id="3cdda-130">Hvis du f.eks. indtaster 6, genereres der en faktura til denne debitor hver sjette måned.</span><span class="sxs-lookup"><span data-stu-id="3cdda-130">For example, if you enter 6, an invoice will be generated every six months for this customer.</span></span>
    + <span data-ttu-id="3cdda-131">Årligt – Vælg denne indstilling, og indtast antallet af år i feltet Pr.</span><span class="sxs-lookup"><span data-stu-id="3cdda-131">Yearly – Select this option and enter the number of years in the Per field.</span></span> <span data-ttu-id="3cdda-132">Hvis du f.eks. indtaster 2, genereres der en faktura til debitoren hvert andet år.</span><span class="sxs-lookup"><span data-stu-id="3cdda-132">For example, if you enter 2, an invoice will be generated every two years for this customer.</span></span>  
14. <span data-ttu-id="3cdda-133">Brug feltet **Pr.** til at angive et antal.</span><span class="sxs-lookup"><span data-stu-id="3cdda-133">In the **Per** field, enter a number.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]