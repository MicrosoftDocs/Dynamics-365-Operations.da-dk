---
title: Oprette en debitorfaktura
description: En **debitorfaktura for en salgsordre** er en regning, som er relateret til et salg, og som en organisation giver til en kunde.
author: ShivamPandey-msft
manager: AnnBe
ms.date: 01/12/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustFreeInvoice
audience: Application User
ms.reviewer: roschlom
ms.custom: 77772
ms.assetid: 00b4b40c-1576-4098-9aed-ac376fdeb8c5
ms.search.region: Global
ms.author: shpandey
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d278bda917d829caaedc7682ef9bebeb151d2bb9
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4991223"
---
# <a name="create-a-customer-invoice"></a><span data-ttu-id="34658-103">Oprette en debitorfaktura</span><span class="sxs-lookup"><span data-stu-id="34658-103">Create a customer invoice</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="34658-104">En **debitorfaktura for en salgsordre** er en regning, som er relateret til et salg, og som en organisation giver til en kunde.</span><span class="sxs-lookup"><span data-stu-id="34658-104">A **customer invoice for a sales order** is a bill that is related to a sale, and that an organization gives to a customer.</span></span> <span data-ttu-id="34658-105">Denne type debitorfaktura oprettes på basis af en salgsordre, som omfatter ordrelinjer og varenumre.</span><span class="sxs-lookup"><span data-stu-id="34658-105">This type of customer invoice is created based on a sales order, which includes order lines and item numbers.</span></span> <span data-ttu-id="34658-106">Varenumre angives og bogføres i finansmodulet.</span><span class="sxs-lookup"><span data-stu-id="34658-106">Item numbers are specified and posted in the ledger.</span></span> <span data-ttu-id="34658-107">Reskontrokladdeposter er ikke tilgængelige for en debitorfaktura for en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="34658-107">Subledger journal entries aren't available for a customer invoice for a sales order.</span></span> <span data-ttu-id="34658-108">Du kan finde flere oplysninger i [Oprette salgsordrefakturaer](tasks/create-sales-order-invoices.md).</span><span class="sxs-lookup"><span data-stu-id="34658-108">For more information, see [Create sales order invoices](tasks/create-sales-order-invoices.md).</span></span>

<span data-ttu-id="34658-109">En **fritekstfaktura** er ikke knyttet til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="34658-109">A **free text invoice** isn't related to a sales order.</span></span> <span data-ttu-id="34658-110">Den indeholder ordrelinjer, der omfatter finanskonti, fritekstbeskrivelser og et salgsbeløb, som du selv angiver.</span><span class="sxs-lookup"><span data-stu-id="34658-110">It contains order lines that include ledger accounts, free-text descriptions, and a sales amount that you enter.</span></span> <span data-ttu-id="34658-111">Du kan ikke angive et varenummer på en faktura af denne type.</span><span class="sxs-lookup"><span data-stu-id="34658-111">You can't enter an item number on this kind of invoice.</span></span> <span data-ttu-id="34658-112">Du skal angive de relevante oplysninger om moms.</span><span class="sxs-lookup"><span data-stu-id="34658-112">You must enter the appropriate sales tax information.</span></span> <span data-ttu-id="34658-113">Der er angivet en hovedkonto for salget på hver fakturalinje, som du kan fordele på flere forskellige finanskonti ved at klikke på **Distribuer beløb** på siden **Fritekstfaktura**.</span><span class="sxs-lookup"><span data-stu-id="34658-113">A main account for the sale is indicated on each invoice line, which you can distribute to multiple ledger accounts by clicking **Distribute amounts** on the **Free text invoice** page.</span></span> <span data-ttu-id="34658-114">Derudover bogføres debitorsaldoen på samlekontoen fra den posteringsprofil, der bruges til fritekstfakturaen.</span><span class="sxs-lookup"><span data-stu-id="34658-114">Additionally, the customer balance is posted to the summary account from the posting profile that is used for the free text invoice.</span></span>

<span data-ttu-id="34658-115">Du kan få flere oplysninger på:</span><span class="sxs-lookup"><span data-stu-id="34658-115">For more information see:</span></span>

[<span data-ttu-id="34658-116">Opret fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="34658-116">Create free text invoices</span></span>](../accounts-receivable/create-free-text-invoice-new.md)

[<span data-ttu-id="34658-117">Oprette en skabelon til en fritekstfaktura</span><span class="sxs-lookup"><span data-stu-id="34658-117">Create a free text invoice template</span></span>](../accounts-receivable/create-free-text-invoice-template-new.md)

[<span data-ttu-id="34658-118">Tildel en fritekstfakturaskabelon til en debitor.</span><span class="sxs-lookup"><span data-stu-id="34658-118">Assign free text invoice template to a customer</span></span>](tasks/assign-free-text-invoice-template-customer.md)

[<span data-ttu-id="34658-119">Generere og bogføre tilbagevendende fritekstfakturaer</span><span class="sxs-lookup"><span data-stu-id="34658-119">Generate and post recurring free text invoices</span></span>](tasks/post-recurring-free-text-invoices.md)


<span data-ttu-id="34658-120">En **proformafaktura** er en faktura, der udarbejdes som et estimat over det faktiske fakturabeløb, før fakturaen bogføres.</span><span class="sxs-lookup"><span data-stu-id="34658-120">A **pro forma invoice** is an invoice that is prepared as an estimate of the actual invoice amounts before the invoice is posted.</span></span> <span data-ttu-id="34658-121">Du kan udskrive en proformafaktura for en debitorfaktura for en salgsordre eller for en fritekstfaktura.</span><span class="sxs-lookup"><span data-stu-id="34658-121">You can print a pro forma invoice either for a customer invoice for a sales order or for a free text invoice.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-sales-orders"></a><span data-ttu-id="34658-122">Bogføre og udskrive individuelle debitorfakturaer, der er baseret på salgsordrer</span><span class="sxs-lookup"><span data-stu-id="34658-122">Post and print individual customer invoices that are based on sales orders</span></span>
<span data-ttu-id="34658-123">Brug denne proces til at oprette en faktura, der er baseret på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="34658-123">Use this process to create an invoice that is based on a sales order.</span></span> <span data-ttu-id="34658-124">Det kan du f.eks. gøre, hvis du beslutter at fakturere debitoren, før du leverer varerne eller tjenesterne.</span><span class="sxs-lookup"><span data-stu-id="34658-124">You might do this if you decide to invoice the customer before you deliver the goods or services.</span></span> 

<span data-ttu-id="34658-125">Når du bogfører en faktura, opdateres antallet i **Fakturarestmængde** for de enkelte varer med det samlede fakturerede antal fra den valgte salgsordre.</span><span class="sxs-lookup"><span data-stu-id="34658-125">When you post an invoice, the **Invoice remainder** quantity for each item is updated with the total of the invoiced quantities from the selected sales order.</span></span> <span data-ttu-id="34658-126">Hvis både antallet **Fakturarestmængde** og antallet **Levér rest** for alle varer i salgsordren er 0 (nul), ændres salgsordrens status til **Faktureret**.</span><span class="sxs-lookup"><span data-stu-id="34658-126">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="34658-127">Hvis antallet for **Fakturarestmængde** ikke er 0 (nul), forbliver status for salgsordren uændret, og der kan bogføres ekstra fakturaer for den.</span><span class="sxs-lookup"><span data-stu-id="34658-127">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span>

<span data-ttu-id="34658-128">Du kan få vist salgsordrernes status på listesiden **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="34658-128">You can view the status of the sales orders on the **All sales orders** list page.</span></span> <span data-ttu-id="34658-129">Brug listesiden **Åbn debitorfakturaer** til at få vist de fakturaer, du har bogført.</span><span class="sxs-lookup"><span data-stu-id="34658-129">Use the **Open customer invoices** list page to view the invoices that you posted.</span></span>

## <a name="post-and-print-individual-customer-invoices-that-are-based-on-packing-slips-and-the-date"></a><span data-ttu-id="34658-130">Bogføre og udskrive individuelle debitorfakturaer, der er baseret på følgesedler og datoen</span><span class="sxs-lookup"><span data-stu-id="34658-130">Post and print individual customer invoices that are based on packing slips and the date</span></span>
<span data-ttu-id="34658-131">Brug denne proces, når der er bogført en eller flere følgesedler til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="34658-131">Use this process when one or more packing slips have been posted for the sales order.</span></span> <span data-ttu-id="34658-132">Debitorfakturaen er baseret på disse følgesedler og afspejler antallene i dem.</span><span class="sxs-lookup"><span data-stu-id="34658-132">The customer invoice is based on these packing slips and reflects the quantities from them.</span></span> <span data-ttu-id="34658-133">De økonomiske oplysninger til fakturaen er baseret på de oplysninger, der angives, når du bogfører fakturaen.</span><span class="sxs-lookup"><span data-stu-id="34658-133">The financial information for the invoice is based on the information that is entered when you post the invoice.</span></span> 

<span data-ttu-id="34658-134">Du kan oprette en debitorfaktura, der er baseret på de linjeelementer på følgesedlen, som er afsendt til dato, selvom alle varerne i en bestemt salgsordre endnu ikke er afsendt.</span><span class="sxs-lookup"><span data-stu-id="34658-134">You can create a customer invoice that is based on the packing slip line items that have been shipped to date, even if all the items for a particular sales order haven't yet been shipped.</span></span> <span data-ttu-id="34658-135">Det kan du f.eks. gøre, hvis din juridiske enhed udsteder én faktura pr. debitor pr. måned, som dækker alle de leverancer, du sender i den pågældende måned.</span><span class="sxs-lookup"><span data-stu-id="34658-135">You might do this if, for example, your legal entity issues one invoice per customer per month that covers all the deliveries that you ship during that month.</span></span> <span data-ttu-id="34658-136">Hver følgeseddel repræsenterer en dellevering eller en komplet levering af varerne i salgsordren.</span><span class="sxs-lookup"><span data-stu-id="34658-136">Each packing slip represents a partial or complete delivery of the items on the sales order.</span></span> 

<span data-ttu-id="34658-137">Når du bogfører fakturaen, opdateres antallet **Fakturarestmængde** for hver vare med det samlede beløb for de leverede antal fra de valgte følgesedler.</span><span class="sxs-lookup"><span data-stu-id="34658-137">When you post the invoice, the **Invoice remainder** quantity for each item is updated with the total of the delivered quantities from the selected packing slips.</span></span> <span data-ttu-id="34658-138">Hvis både antallet **Fakturarestmængde** og antallet **Levér rest** for alle varer i salgsordren er 0 (nul), ændres salgsordrens status til **Faktureret**.</span><span class="sxs-lookup"><span data-stu-id="34658-138">If both the **Invoice remainder** quantity and the **Deliver remainder** quantity for all items on the sales order are 0 (zero), the status of the sales order is changed to **Invoiced**.</span></span> <span data-ttu-id="34658-139">Hvis antallet for **Fakturarestmængde** ikke er 0 (nul), forbliver status for salgsordren uændret, og der kan bogføres ekstra fakturaer for den.</span><span class="sxs-lookup"><span data-stu-id="34658-139">If the **Invoice remainder** quantity isn't 0 (zero), the status of the sales order remains unchanged, and additional invoices can be entered for it.</span></span> 

<span data-ttu-id="34658-140">Lagerposteringer opdateres med fakturanummeret, og status i feltet **Linjestatus** i salgsordren ændres til **Faktureret**.</span><span class="sxs-lookup"><span data-stu-id="34658-140">Inventory transactions are updated with the invoice number, and the status in the **Line status** field on the sales order is changed to **Invoiced**.</span></span> 

<span data-ttu-id="34658-141">Se salgsordrernes status på listesiden **Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="34658-141">View the status of the sales orders in the **All sales orders** list page.</span></span>

## <a name="consolidate-sales-orders-or-packing-slips-for-posting"></a><span data-ttu-id="34658-142">Konsolidere salgsordrer eller følgesedler til bogføring</span><span class="sxs-lookup"><span data-stu-id="34658-142">Consolidate sales orders or packing slips for posting</span></span>
<span data-ttu-id="34658-143">Brug denne fremgangsmåde, når en eller flere salgsordrer, der er klar til at blive faktureret, og du vil konsolidere dem i én faktura.</span><span class="sxs-lookup"><span data-stu-id="34658-143">Use this process when one or more sales orders are ready to be invoiced, and you want to consolidate them into a single invoice.</span></span> 

<span data-ttu-id="34658-144">Du kan vælge flere fakturaer på listesiden **Salgsordre** og derefter bruge **Generer fakturaer** for at sammenflette dem.</span><span class="sxs-lookup"><span data-stu-id="34658-144">You can select multiple invoices on the **Sales order** list page and then use **Generate invoices** to consolidate them.</span></span> <span data-ttu-id="34658-145">På siden **Bogføring af faktura** kan du ændre indstillingen **Samleordre** til at opsummere ved ordrenummer (hvor der er flere følgesedler for en enkelt salgsordre) eller efter fakturakonto (hvor der er flere salgsordrer for en enkelt faktura).</span><span class="sxs-lookup"><span data-stu-id="34658-145">On the **Posting invoice** page, you can change the **Summary order** setting to summarize by order number (where there are multiple packing slips for a single sales order) or by invoice account (where there are multiple sales orders for a single invoice account).</span></span> <span data-ttu-id="34658-146">Brug knappen **Arranger** for at konsolidere salgsordrer til enkelte fakturaer, der er baseret på indstillingen **Samleordre**.</span><span class="sxs-lookup"><span data-stu-id="34658-146">Use the **Arrange** button to consolidate sales orders into single invoices, based on the **Summary order** settings.</span></span>

## <a name="additional-settings-that-change-the-posting-behavior"></a><span data-ttu-id="34658-147">Yderligere indstillinger, der ændrer funktionsmåden for bogføring</span><span class="sxs-lookup"><span data-stu-id="34658-147">Additional settings that change the posting behavior</span></span>
<span data-ttu-id="34658-148">Følgende felter ændrer funktionaliteten af bogføringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="34658-148">The following fields change the behavior of the posting process.</span></span>

<table>
<colgroup>
<col width="50%" />
<col width="50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34658-149">Felt</span><span class="sxs-lookup"><span data-stu-id="34658-149">Field</span></span></th>
<th><span data-ttu-id="34658-150">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="34658-150">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="34658-151">Antal</span><span class="sxs-lookup"><span data-stu-id="34658-151">Quantity</span></span></td>
<td><span data-ttu-id="34658-152">Vælg de antal, som bogføringen af dokumentet skal baseres på.</span><span class="sxs-lookup"><span data-stu-id="34658-152">Select the quantities to base the posting of the document on.</span></span> <span data-ttu-id="34658-153">Indstillingerne, der er tilgængelige, afhænger af den type dokument, du bogfører, f.eks. en følgeseddel eller en faktura.</span><span class="sxs-lookup"><span data-stu-id="34658-153">The options that are available vary, depending on the type of document that you are posting, such as a packing slip or an invoice.</span></span>
<ul>
<li><span data-ttu-id="34658-154"><strong>Levér nu</strong> – Vælg alle de mængder, der er angivet i feltet <strong>Levér nu</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-154"><strong>Deliver now</strong> – Select all quantities that are entered in the <strong>Deliver now</strong> field.</span></span> <span data-ttu-id="34658-155">Du kan bruge denne indstilling til at bekræfte eller levere en delordre.</span><span class="sxs-lookup"><span data-stu-id="34658-155">Use this option to confirm or deliver a partial order.</span></span></li>
<li><span data-ttu-id="34658-156"><strong>Plukket</strong> – Vælg alle de mængder, der er plukket.</span><span class="sxs-lookup"><span data-stu-id="34658-156"><strong>Picked</strong> – Select all quantities that have been picked.</span></span></li>
<li><span data-ttu-id="34658-157"><strong>Alle</strong> – Vælg alle antal i salgsordren, der endnu ikke er opdateret af den aktuelle dokumenttype.</span><span class="sxs-lookup"><span data-stu-id="34658-157"><strong>All</strong> – Select all quantities on the sales order that haven&#39;t yet been updated by the current document type.</span></span></li>
<li><span data-ttu-id="34658-158"><strong>Følgeseddel</strong> – Vælg alle de antal, der er opdateret af en følgeseddel,.</span><span class="sxs-lookup"><span data-stu-id="34658-158"><strong>Packing slip</strong> – Select all quantities that have been updated by a packing slip.</span></span></li>
<li><span data-ttu-id="34658-159"><strong>Plukket antal og ikke-lagerførte produkter</strong> – Vælg alle de mængder, der er plukket, og alle de produktmængder, der ikke er på lager.</span><span class="sxs-lookup"><span data-stu-id="34658-159"><strong>Picked quantity and not stocked products</strong> – Select all quantities that have been picked and all product quantities that aren&#39;t stocked.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34658-160">Postering</span><span class="sxs-lookup"><span data-stu-id="34658-160">Posting</span></span></td>
<td><ul>
<li><span data-ttu-id="34658-161">Vælg denne indstilling for at journalisere salgsordren.</span><span class="sxs-lookup"><span data-stu-id="34658-161">Select this option to journalize the sales order.</span></span></li>
<li><span data-ttu-id="34658-162">Fjern markeringen af denne indstilling for at udskrive en proformasalgsordre.</span><span class="sxs-lookup"><span data-stu-id="34658-162">Clear this option to print a pro forma sales order.</span></span> <span data-ttu-id="34658-163"><strong>Bemærk!</strong> Hvis du har indgået en aftale om en betalingsplan, vises betalingsplanen ikke på proformasalgsordren.</span><span class="sxs-lookup"><span data-stu-id="34658-163"><strong>Note:</strong> If you made an agreement for a payment schedule, the payment schedule isn&#39;t shown on the pro forma sales order.</span></span> <span data-ttu-id="34658-164">Betalingsplaner vises kun på de egentlige salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="34658-164">Payment schedules are shown only on actual sales orders.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34658-165">Vælg senere</span><span class="sxs-lookup"><span data-stu-id="34658-165">Late selection</span></span></td>
<td><span data-ttu-id="34658-166">Vælg denne indstilling for at anvende den valgte forespørgsel senere.</span><span class="sxs-lookup"><span data-stu-id="34658-166">Select this option to apply the selected query later.</span></span> <span data-ttu-id="34658-167">Denne indstilling anvendes til batchjob.</span><span class="sxs-lookup"><span data-stu-id="34658-167">This option is used for batch jobs.</span></span> <span data-ttu-id="34658-168">Forespørgslen køres, når batchjobbet køres.</span><span class="sxs-lookup"><span data-stu-id="34658-168">The query is run when the batch job is run.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34658-169">Reducer antal</span><span class="sxs-lookup"><span data-stu-id="34658-169">Reduce quantity</span></span></td>
<td><span data-ttu-id="34658-170">Vælg denne indstilling for automatisk at reducere det leverede antal, når dokumentet bogføres, så det leverede antal er lig med den disponible beholdning.</span><span class="sxs-lookup"><span data-stu-id="34658-170">Select this option to automatically reduce the delivered quantity when the document is posted, so that the delivered quantity equals the available inventory.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34658-171">Udskriv</span><span class="sxs-lookup"><span data-stu-id="34658-171">Print</span></span></td>
<td><span data-ttu-id="34658-172">Vælg, hvornår dokumenter skal udskrives:</span><span class="sxs-lookup"><span data-stu-id="34658-172">Select when to print documents:</span></span>
<ul>
<li><span data-ttu-id="34658-173"><strong>Løbende</strong> – Udskriv dokumenter, når de enkelte fakturaer er opdateret.</span><span class="sxs-lookup"><span data-stu-id="34658-173"><strong>Current</strong> – Print documents after each invoice has been updated.</span></span></li>
<li><span data-ttu-id="34658-174"><strong>Efter</strong> – Udskriv dokumenter, efter alle fakturaerne er blevet opdateret.</span><span class="sxs-lookup"><span data-stu-id="34658-174"><strong>After</strong> – Print documents after all the invoices have been updated.</span></span></li>
</ul><span data-ttu-id="34658-175">
<strong>Bemærk!</strong> Feltet <strong>Udskrivning</strong> er kun tilgængeligt, hvis du vælger indstillingen <strong>Udskrivning af faktura</strong>, <strong>Udskrivning af bekræftelse</strong>, <strong>Udskrivning af plukliste</strong> eller <strong>Udskrivning af følgeseddel</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-175">
<strong>Note:</strong> The <strong>Print</strong> field is available only if you select the <strong>Print invoice</strong>, <strong>Print confirmation</strong>, <strong>Print picking list</strong>, or <strong>Print packing slip</strong> option.</span></span> <span data-ttu-id="34658-176">På siden <strong>Formsortering</strong> har du f.eks. konfigureret systemet til at sortere efter fakturakonto.</span><span class="sxs-lookup"><span data-stu-id="34658-176">For example, on the <strong>Form sorting</strong> page, you have set up the system to sort the information by invoice account.</span></span> <span data-ttu-id="34658-177">Du kan da vælge <strong>Efter</strong> for at udskrive dokumenter i en batch, der er sorteret efter fakturakonto.</span><span class="sxs-lookup"><span data-stu-id="34658-177">You can then select <strong>After</strong> to print the documents in a batch that is sorted by invoice account.</span></span> <span data-ttu-id="34658-178">Ellers udskrives dokumenter, før behandlingen er fuldført, og dokumenterne sorteres ikke i den rækkefølge, der er angivet på siden <strong>Formsortering</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-178">Otherwise, the documents are printed before processing is completed, and the documents aren&#39;t sorted in the order that is specified on the <strong>Form sorting</strong> page.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34658-179">Udskrivning af faktura</span><span class="sxs-lookup"><span data-stu-id="34658-179">Print invoice</span></span></td>
<td><span data-ttu-id="34658-180">Vælg denne indstilling for at udskrive fakturaen.</span><span class="sxs-lookup"><span data-stu-id="34658-180">Select this option to print the invoice.</span></span> <span data-ttu-id="34658-181">Hvis denne indstilling er slået fra, kan du bogføre en faktura uden at udskrive den.</span><span class="sxs-lookup"><span data-stu-id="34658-181">If this option is turned off, you can post an invoice without printing it.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34658-182">Send e-mail</span><span class="sxs-lookup"><span data-stu-id="34658-182">Send e-mail</span></span></td>
<td><span data-ttu-id="34658-183">Vælg denne indstilling for at sende fakturaen for en salgsordre som en vedhæftet fil i en e-mail til en kunde, efter at fakturaen er blevet bogført.</span><span class="sxs-lookup"><span data-stu-id="34658-183">Select this option to send the invoice for a sales order to the customer as an email attachment after the invoice is posted.</span></span> <span data-ttu-id="34658-184">Vedhæftede filer sendes som PDF- og XML-filer.</span><span class="sxs-lookup"><span data-stu-id="34658-184">Attachments are sent as PDF and XML files.</span></span> <span data-ttu-id="34658-185">Denne indstilling er kun tilgængelig, hvis du vælger indstillingen <strong>Aktivér CFD (elektroniske fakturaer)</strong> på siden <strong>Parametre for elektronisk faktura</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-185">This option is available only if you select the <strong>Enable CFD (electronic invoices)</strong> option on the <strong>Electronic invoice parameters</strong> page.</span></span> <span data-ttu-id="34658-186"><strong>Bemærk!</strong> (MEX) Dette kontrolelement er kun tilgængeligt for juridiske enheder, hvis primære adresse er i Mexico.</span><span class="sxs-lookup"><span data-stu-id="34658-186"><strong>Note:</strong> (MEX) This control is available only to legal entities whose primary address is in Mexico.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34658-187">Brug destination for udskriftsstyring</span><span class="sxs-lookup"><span data-stu-id="34658-187">Use print management destination</span></span></td>
<td><span data-ttu-id="34658-188">Vælg denne indstilling for at bruge de udskriftsindstillinger, der er angivet for posteringen, dokumentet eller modulet på siden <strong>Opsætning af udskriftsstyring</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-188">Select this option to use the print settings that are specified for the transaction, document, or module on the <strong>Print management setup</strong> page.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34658-189">Kontrollér kreditmaks.</span><span class="sxs-lookup"><span data-stu-id="34658-189">Check credit limit</span></span></td>
<td><span data-ttu-id="34658-190">Vælg de oplysninger, der skal analyseres, når der udføres en kontrol af kreditmaksimum.</span><span class="sxs-lookup"><span data-stu-id="34658-190">Select the information that should be analyzed when a credit limit check is performed.</span></span>
<ul>
<li><span data-ttu-id="34658-191"><strong>Ingen</strong> – Der er ingen krav i forbindelse med kontrol af kreditmaksimum.</span><span class="sxs-lookup"><span data-stu-id="34658-191"><strong>None</strong> – There is no requirement for the credit limit check.</span></span></li>
<li><span data-ttu-id="34658-192"><strong>Saldo</strong> - Kreditmaksimum kontrolleres i forhold til debitorsaldoen.</span><span class="sxs-lookup"><span data-stu-id="34658-192"><strong>Balance</strong> – The credit limit is checked against the customer balance.</span></span></li>
<li><span data-ttu-id="34658-193"><strong>Saldo + følgeseddel eller produktkvittering</strong> – Kreditmaksimum kontrolleres i forhold til debitorsaldoen og leverancer.</span><span class="sxs-lookup"><span data-stu-id="34658-193"><strong>Balance + packing slip or product receipt</strong> – The credit limit is checked against the customer balance and deliveries.</span></span></li>
<li><span data-ttu-id="34658-194"><strong>Saldo+Alt</strong> – Kreditmaks. kontrolleres i forhold til debitorsaldoen, leverancer og åbne ordrer.</span><span class="sxs-lookup"><span data-stu-id="34658-194"><strong>Balance+All</strong> – The credit limit is checked against the customer balance, deliveries, and open orders.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34658-195">Kreditrettelse</span><span class="sxs-lookup"><span data-stu-id="34658-195">Credit correction</span></span></td>
<td><span data-ttu-id="34658-196">Vælg denne indstilling for at få vist kreditnotaen som debet i bilagsposteringerne.</span><span class="sxs-lookup"><span data-stu-id="34658-196">Select this option to display the credit note as a debit in the voucher transactions.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="34658-197">Kredit, restantal</span><span class="sxs-lookup"><span data-stu-id="34658-197">Credit remaining quantity</span></span></td>
<td><span data-ttu-id="34658-198">Hvis du bogfører en kreditnota, skal du vælge denne indstilling, hvis du vil beholde den resterende mængde i ordren.</span><span class="sxs-lookup"><span data-stu-id="34658-198">If you&#39;re posting a credit note, select this option to keep the remaining quantity on order.</span></span> <span data-ttu-id="34658-199">Hvis denne indstilling fravælges, angives den resterende mængde til 0 (nul).</span><span class="sxs-lookup"><span data-stu-id="34658-199">If this option is cleared, the remaining quantity is set to 0 (zero).</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="34658-200">Samleopdatering for</span><span class="sxs-lookup"><span data-stu-id="34658-200">Summary update for</span></span></td>
<td><span data-ttu-id="34658-201">Vælg, hvordan flere salgsordrer skal opsummeres:</span><span class="sxs-lookup"><span data-stu-id="34658-201">Select how multiple sales orders should be summarized:</span></span>
<ul>
<li><span data-ttu-id="34658-202"><strong>Ingen</strong> – Opsummer ikke salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="34658-202"><strong>None</strong> – Don&#39;t summarize sales orders.</span></span> <span data-ttu-id="34658-203">Der oprettes f.eks. en separat faktura for hver enkelt salgsordre.</span><span class="sxs-lookup"><span data-stu-id="34658-203">For example, a separate invoice will be created for each sales order.</span></span></li>
<li><span data-ttu-id="34658-204"><strong>Fakturakonto</strong> – Opsummer alle valgte ordrer, baseret på de kriterier, der er angivet på siden <strong>Samleopdateringsparametre</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-204"><strong>Invoice account</strong> – Summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span></li>
<li><span data-ttu-id="34658-205"><strong>Ordre</strong> – Opsummer en udvalgt række ordrer i én ordre, som du angiver.</span><span class="sxs-lookup"><span data-stu-id="34658-205"><strong>Order</strong> – Summarize a selected range of orders into one order that you specify.</span></span> <span data-ttu-id="34658-206">Ordrerne opsummeres baseret på de kriterier, der er angivet på siden <strong>Samleopdateringsparametre</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-206">The orders are summarized based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="34658-207">Hvis du vælger denne indstilling, skal du vælge en værdi i feltet <strong>Salgsordrer</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-207">If you select this option, you must select a value in the <strong>Sales order</strong> field.</span></span></li>
<li><span data-ttu-id="34658-208"><strong>Automatisk samling</strong> – Hvis der er angivet samleopdateringer på siden <strong>Samleopdatering</strong>, skal du samle alle de valgte ordrer baseret på de kriterier, der er angivet på siden <strong>Samleopdateringsparametre</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-208"><strong>Automatic summary</strong> – If summary updates have been specified on the <strong>Summary update</strong> page, summarize all selected orders, based on the criteria that are set up on the <strong>Summary update parameters</strong> page.</span></span> <span data-ttu-id="34658-209">Hvis du ikke har angivet samleopdateringer, bliver ordren bogført særskilt.</span><span class="sxs-lookup"><span data-stu-id="34658-209">If summary updates haven&#39;t been specified, the order is posted separately.</span></span></li>
<li><span data-ttu-id="34658-210"><strong>Følgeseddel</strong> – Opsummer en udvalgt række ordrer i én faktura for hver følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="34658-210"><strong>Packing slip</strong> – Summarize a selected range of orders into one invoice for each packing slip.</span></span> <span data-ttu-id="34658-211">Denne indstilling kan kun benyttes, hvis der er valgt <strong>Følgeseddel</strong> i feltet <strong>Antal</strong>.</span><span class="sxs-lookup"><span data-stu-id="34658-211">This option is available only if <strong>Packing slip</strong> is selected in the <strong>Quantity</strong> field.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>





