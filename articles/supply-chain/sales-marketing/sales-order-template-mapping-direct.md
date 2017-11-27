---
title: Synkronisere salgsordrehoveder og -linjer direkte fra Finance and Operations til Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsordrehoveder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: cc0be50552ae680ba5291e72b7c482ee67e1e70e
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="3cede-103">Synkronisere salgsordrehoveder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="3cede-103">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="3cede-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsordrehoveder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-104">This topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="3cede-105">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="3cede-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="3cede-106">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="3cede-107">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="3cede-108">I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="3cede-109">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="3cede-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3cede-110">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="3cede-110">Templates and tasks</span></span>

<span data-ttu-id="3cede-111">For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="3cede-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="3cede-112">Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="3cede-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3cede-113">Følgende skabelon og underliggende opgaver bruges til at synkronisere salgsordrehoveder og -linjer fra Finance and Operations til Sales:</span><span class="sxs-lookup"><span data-stu-id="3cede-113">The following template and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="3cede-114">**Navnet på skabelonen i dataintegration:** Salgsordrer Orders (Fin and Ops til Sales) – Direkte</span><span class="sxs-lookup"><span data-stu-id="3cede-114">**Name of the template in Data integration:** Sales Orders (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="3cede-115">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="3cede-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="3cede-116">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="3cede-116">OrderHeader</span></span>
    - <span data-ttu-id="3cede-117">OrderLine</span><span class="sxs-lookup"><span data-stu-id="3cede-117">OrderLine</span></span>

<span data-ttu-id="3cede-118">Følgende synkroniseringsopgaver kræves, før salgsfakturahoveder og -linjer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="3cede-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="3cede-119">Produkter (Fin and Ops til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="3cede-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="3cede-120">Konti (Sales til Fin and Ops) - Direkte (hvis den bruges)</span><span class="sxs-lookup"><span data-stu-id="3cede-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="3cede-121">Kontakter til Debitorer (Sales til Fin and Ops) – Direkte (hvis det bruges)</span><span class="sxs-lookup"><span data-stu-id="3cede-121">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="3cede-122">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="3cede-122">Entity set</span></span>

| <span data-ttu-id="3cede-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3cede-123">Finance and Operations</span></span>  | <span data-ttu-id="3cede-124">Salg</span><span class="sxs-lookup"><span data-stu-id="3cede-124">Sales</span></span>             |
|-------------------------|-------------------|
| <span data-ttu-id="3cede-125">CDS-salgsordrehoveder</span><span class="sxs-lookup"><span data-stu-id="3cede-125">CDS sales order headers</span></span> | <span data-ttu-id="3cede-126">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="3cede-126">SalesOrders</span></span>       |
| <span data-ttu-id="3cede-127">CDS-salgsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="3cede-127">CDS sales order lines</span></span>   | <span data-ttu-id="3cede-128">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="3cede-128">SalesOrderDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3cede-129">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="3cede-129">Entity flow</span></span>

<span data-ttu-id="3cede-130">Salgsordrer oprettes i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-130">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="3cede-131">Filtre i skabelonen hjælper med til at sikre, at kun relevante salgsordrer medtages i synkroniseringen:</span><span class="sxs-lookup"><span data-stu-id="3cede-131">Filters in the template help guarantee that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="3cede-132">På salgsordren medtages både bestillings- og faktureringskunden, der stammer fra Sales, i synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="3cede-132">On the sales order, both the ordering customer and the invoicing customer that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="3cede-133">I Finance and Operations bruges felterne **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til at spore synkroniseringen i dataenheder.</span><span class="sxs-lookup"><span data-stu-id="3cede-133">In Finance and Operations, the **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** fields are used to track the synchronization in the data entities.</span></span>
- <span data-ttu-id="3cede-134">Salgsordren i Finance and Operations skal bekræftes.</span><span class="sxs-lookup"><span data-stu-id="3cede-134">The sales order in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="3cede-135">Det er kun de bekræftede salgsordrer eller salgsordrer, der har en højere behandlingsstatus, f.eks. status som **Leveret** eller **Faktureret**, der synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-135">Only confirmed sales orders or sales orders that have a higher processing status, such as **Shipped** or **Invoiced**, are synchronized to Sales.</span></span>
- <span data-ttu-id="3cede-136">Når en salgsordre oprettes eller redigeres, skal batchkørslen **Beregn salgstotaler** i Finance and Operations udføres.</span><span class="sxs-lookup"><span data-stu-id="3cede-136">After a sales order is created or modified, the **Calculate sales totals** batch job in Finance and Operations must be run.</span></span> <span data-ttu-id="3cede-137">Kun salgsordrer, hvor salgstotaler er beregnet, synkroniseres med Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-137">Only sales orders where sales totals are calculated will be synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="3cede-138">Moms vedrørende gebyrer på salgsordrehovedet indgår i øjeblikket ikke i synkroniseringen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-138">Currently, tax that is related to charges on the sales order header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="3cede-139">Sales understøtter ikke momsoplysninger på hovedniveau.</span><span class="sxs-lookup"><span data-stu-id="3cede-139">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="3cede-140">Men moms, som er relateret til gebyrer på linjeniveau, er imidlertid inkluderet i synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="3cede-140">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="3cede-141">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="3cede-141">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="3cede-142">Nye felter er føjet til enheden **Ordre** og vises på siden:</span><span class="sxs-lookup"><span data-stu-id="3cede-142">New fields have been added to the **Order** entity and appear on the page:</span></span>

- <span data-ttu-id="3cede-143">**Vedligeholdes eksternt** - Angiv denne indstilling til **Ja**, når ordren kommer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3cede-143">**Is Maintained Externally** – Set this option to **Yes** when the order is coming from Finance and Operations.</span></span>
- <span data-ttu-id="3cede-144">**Behandlingsstatus** – Dette felt viser behandlingsstatussen for ordren i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3cede-144">**Processing status** – This field shows the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="3cede-145">Følgende værdier er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="3cede-145">The following values are available:</span></span>

    - <span data-ttu-id="3cede-146">Aktive</span><span class="sxs-lookup"><span data-stu-id="3cede-146">Active</span></span>
    - <span data-ttu-id="3cede-147">Bekræftet</span><span class="sxs-lookup"><span data-stu-id="3cede-147">Confirmed</span></span>
    - <span data-ttu-id="3cede-148">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="3cede-148">Packing Slip</span></span>
    - <span data-ttu-id="3cede-149">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="3cede-149">Invoiced</span></span>
    - <span data-ttu-id="3cede-150">Plukket</span><span class="sxs-lookup"><span data-stu-id="3cede-150">Picked</span></span>
    - <span data-ttu-id="3cede-151">Delvist plukket</span><span class="sxs-lookup"><span data-stu-id="3cede-151">Partially Picked</span></span>
    - <span data-ttu-id="3cede-152">Delvist pakket</span><span class="sxs-lookup"><span data-stu-id="3cede-152">Partially Packed</span></span>
    - <span data-ttu-id="3cede-153">Afsendt</span><span class="sxs-lookup"><span data-stu-id="3cede-153">Shipped</span></span>
    - <span data-ttu-id="3cede-154">Delvist afsendt</span><span class="sxs-lookup"><span data-stu-id="3cede-154">Partially Shipped</span></span>
    - <span data-ttu-id="3cede-155">Delvist faktureret</span><span class="sxs-lookup"><span data-stu-id="3cede-155">Partially Invoiced</span></span>
    - <span data-ttu-id="3cede-156">Annulleret</span><span class="sxs-lookup"><span data-stu-id="3cede-156">Cancelled</span></span>

<span data-ttu-id="3cede-157">Indstillingen **Har kun eksternt vedligeholdte produkter** bruges i andre salgsordrescenarier (f.eks. ved synkronisering fra Sales til Finance and Operations) til konsekvent at holde styr på, om salgsordren består udelukkende af eksternt vedligeholdte produkter.</span><span class="sxs-lookup"><span data-stu-id="3cede-157">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (for example, synchronization from Sales to Finance and Operation) to consistently track whether a sales order consists entirely of externally maintained products.</span></span> <span data-ttu-id="3cede-158">Hvis en salgsordre kun består af eksternt vedligeholdte produkter, vedligeholdes produkterne i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3cede-158">If a sales order consists entirely of externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="3cede-159">Denne indstilling er med til at sikre, at du ikke forsøger at synkronisere salgsordrelinjer, der har produkter, som er ukendte i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3cede-159">This setting helps guarantee that you don't try to synchronize sales order lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="3cede-160">Knapperne **Opret faktura**, **Annuller ordre**, **Genberegn**, **Hent produkter** og **Slå adresse op** på siden **Salgsordre** er skjult for eksternt vedligeholdte ordrer, da fakturaer oprettes i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-160">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products**, and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="3cede-161">Ordresiden kan ikke redigeres, fordi salgsordreoplysninger synkroniseres fra Finance and Operations efter aktiveringen.</span><span class="sxs-lookup"><span data-stu-id="3cede-161">The order page can't be edited, because sales order information will be synchronized from Finance and Operations.</span></span>

<span data-ttu-id="3cede-162">Status for en salgsordre forbliver **Aktiv** for at sikre, at ændringer fra Finance and Operations kan flyde til salgsordren i Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-162">The status of a sales order will remain **Active** to help guarantee that changes from Finance and Operations can flow to the sales order in Sales.</span></span> <span data-ttu-id="3cede-163">For at styre denne funktion, skal standardværdien for **Statecode \[[Status]\]** angives til **Aktiv** i dataintegrationsprojektet.</span><span class="sxs-lookup"><span data-stu-id="3cede-163">To control this behavior, set the default **Statecode \[Status\]** value to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="3cede-164">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="3cede-164">Preconditions and mapping setup</span></span>

<span data-ttu-id="3cede-165">Før du synkroniserer salgsordrer, er det vigtigt, at du opdaterer følgende indstillinger i systemerne.</span><span class="sxs-lookup"><span data-stu-id="3cede-165">Before you synchronize sales orders, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="3cede-166">Konfiguration i Sales</span><span class="sxs-lookup"><span data-stu-id="3cede-166">Setup in Sales</span></span>

- <span data-ttu-id="3cede-167">Sørg for, at der er konfigureret tilladelser for det team, som brugeren fra din Sales-forbindelse er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="3cede-167">Make sure that permissions are set up for the team that the user from your Sales connection set is assigned to.</span></span> <span data-ttu-id="3cede-168">Hvis du bruger demodata, har brugeren normalt administratoradgang, men teamet har ikke administratoradgang.</span><span class="sxs-lookup"><span data-stu-id="3cede-168">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="3cede-169">Hvis teamet ikke også har administratoradgang, når du kører projektet fra dataintegration, får du vist en fejlmeddelelse om, at det primære team mangler.</span><span class="sxs-lookup"><span data-stu-id="3cede-169">If the team doesn't also have admin access, when you run the project from Data integration, you will receive an error message that states that Principal team is missing.</span></span>

    <span data-ttu-id="3cede-170">Gå til **Indstillinger** > **Sikkerhed** > **Teams**, vælg det relevante team, vælg **Administrer roller**, og vælg en rolle med de ønskede tilladelser, f.eks. **systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="3cede-170">Go to **Settings** > **Security** > **Teams**, select the relevant team, select **Manage Roles**, and select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="3cede-171">Gå til **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, og sørg for, at der bruges til følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="3cede-171">Go to **Settings** > **Administration** > **System settings** > **Sales**, and makes sure that the following settings are used:</span></span>

    - <span data-ttu-id="3cede-172">Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cede-172">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="3cede-173">Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="3cede-173">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="3cede-174">Konfiguration i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3cede-174">Setup in Finance and Operations</span></span>

<span data-ttu-id="3cede-175">Gå til **Salg og marketing** > **Periodiske opgaver** > **Beregne Salgstotaler**, og Indstil jobbet til at køre som et batchjob.</span><span class="sxs-lookup"><span data-stu-id="3cede-175">Go to **Sales and marketing** > **Periodic tasks** > **Calculate sales totals**, and set the job to run as a batch job.</span></span> <span data-ttu-id="3cede-176">Angiv indstillingen **Beregn totaler for salgsordrer** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3cede-176">Set the **Calculate totals for sales orders** option to **Yes**.</span></span> <span data-ttu-id="3cede-177">Dette trin er vigtigt, fordi kun salgsordrer, hvor salgstotaler er beregnet, synkroniseres med Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-177">This step is important, because only sales orders where sales totals are calculated will be synchronized to Sales.</span></span> <span data-ttu-id="3cede-178">Frekvensen for batchjobbet skal være afstemt med frekvensen for salgsordresynkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="3cede-178">The frequency of the batch job should be aligned with the frequency of sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="3cede-179">Opsætning af dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="3cede-179">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="3cede-180">Opgaven SalesHeader</span><span class="sxs-lookup"><span data-stu-id="3cede-180">SalesHeader task</span></span>

- <span data-ttu-id="3cede-181">Kontrollér, at den nødvendige tilknytning findes for **InvoiceCountryRegionId** til **BillingAddress\_Country** og for **DeliveryCountryRegionId** til **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="3cede-181">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country** and for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="3cede-182">Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="3cede-182">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="3cede-183">Der kræves en prisliste for at kunne oprette ordrer i Sales.</span><span class="sxs-lookup"><span data-stu-id="3cede-183">A price list is required in order to create orders in Sales.</span></span> <span data-ttu-id="3cede-184">Opdater værditilknytningen **pricelevelid.name \[prislistenavnet\]** til den prisliste, der bruges i Sales efter valuta.</span><span class="sxs-lookup"><span data-stu-id="3cede-184">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="3cede-185">Du kan bruge standardprislisten til en enkelt valuta.</span><span class="sxs-lookup"><span data-stu-id="3cede-185">You can use the default price list for a single currency.</span></span> <span data-ttu-id="3cede-186">Hvis du har prislister i flere valutaer, kan du også bruge en værditilknytning.</span><span class="sxs-lookup"><span data-stu-id="3cede-186">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="3cede-187">Standardskabelonværdien for **pricelevelid.name \[prislistenavnet\]** er **CRM Service USA (eksempel)**.</span><span class="sxs-lookup"><span data-stu-id="3cede-187">The default template value for **pricelevelid.name \[Price list name\]** is **CRM Service USA (sample)**.</span></span>

#### <a name="salesline-task"></a><span data-ttu-id="3cede-188">Opgaven SalesLine</span><span class="sxs-lookup"><span data-stu-id="3cede-188">SalesLine task</span></span>

- <span data-ttu-id="3cede-189">Du skal sikre, at den nødvendige tilknytning findes for **DeliveryCountryRegionId** til **DeliveryAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="3cede-189">Make sure that the required mapping exists for **DeliveryCountryRegionId** to **DeliveryAddress\_Country**.</span></span>

    <span data-ttu-id="3cede-190">Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="3cede-190">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="3cede-191">Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3cede-191">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="3cede-192">En skabelonværdi, der har en værditilknytning, er defineret for **SalesUnitSymbol** til **Quantity\_UOM**</span><span class="sxs-lookup"><span data-stu-id="3cede-192">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3cede-193">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="3cede-193">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="3cede-194">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** indgår ikke i standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="3cede-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="3cede-195">Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="3cede-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="3cede-196">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="3cede-196">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="3cede-197">Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3cede-197">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="orderheader"></a><span data-ttu-id="3cede-198">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="3cede-198">OrderHeader</span></span>

![Skabelontilknytning i dataintegrator](./media/sales-order-direct-template-mapping-data-integrator-1.png)

### <a name="orderline"></a><span data-ttu-id="3cede-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="3cede-200">OrderLine</span></span>

![Skabelontilknytning i dataintegrator](./media/sales-order-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="3cede-202">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="3cede-202">Related topics</span></span>

[<span data-ttu-id="3cede-203">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="3cede-203">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="3cede-204">Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3cede-204">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="3cede-205">Synkronisere produkter direkte fra Finance and Operations med produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="3cede-205">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="3cede-206">Synkronisere kontakter direkte fra Sales med kontakter eller debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3cede-206">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="3cede-207">Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="3cede-207">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




