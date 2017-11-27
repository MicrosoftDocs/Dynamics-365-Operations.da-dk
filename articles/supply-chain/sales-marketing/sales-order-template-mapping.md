---
title: Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsordrehoveder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2017
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
ms.openlocfilehash: c7b2ff6430e99661ee284f65089086df9fa5a1ad
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-sales-order-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="fc52b-103">Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="fc52b-103">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="fc52b-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsordrehoveder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="fc52b-104">The topic discusses the templates and underlying tasks that are used to synchronize sales order headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="fc52b-105">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="fc52b-105">Template and tasks</span></span>

<span data-ttu-id="fc52b-106">Følgende skabeloner og underliggende opgaver bruges til at synkronisere salgsordrehoveder og -linjer fra Finance and Operations til Sales:</span><span class="sxs-lookup"><span data-stu-id="fc52b-106">The following templates and underlying tasks are used to synchronize sales order headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="fc52b-107">**Navnet på skabelonen i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="fc52b-107">**Name of template in Data integration**</span></span> 

    - <span data-ttu-id="fc52b-108">Salgsordrer (Fin and Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="fc52b-108">Sales Orders (Fin and Ops to Sales)</span></span>
    
- <span data-ttu-id="fc52b-109">**Navnene på opgaverne i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="fc52b-109">**Names of tasks in Data integration project**</span></span>

    - <span data-ttu-id="fc52b-110">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="fc52b-110">OrderHeader</span></span>
    - <span data-ttu-id="fc52b-111">OrderLine</span><span class="sxs-lookup"><span data-stu-id="fc52b-111">OrderLine</span></span>

<span data-ttu-id="fc52b-112">Synkroniseringsopgaver, der kræves før synkronisering af salgsfakturahoved og -linjer:</span><span class="sxs-lookup"><span data-stu-id="fc52b-112">Sync tasks required prior to Sales invoice header and lines sync:</span></span>

- <span data-ttu-id="fc52b-113">Produkter (Fin og Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="fc52b-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="fc52b-114">Konti (Sales til Fin og Ops) (hvis det bruges)</span><span class="sxs-lookup"><span data-stu-id="fc52b-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="fc52b-115">Kontakter til Debitorer (Sales til Fin and Ops) (hvis det bruges)</span><span class="sxs-lookup"><span data-stu-id="fc52b-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="fc52b-116">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="fc52b-116">Entity set</span></span>

| <span data-ttu-id="fc52b-117">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fc52b-117">Finance and Operations</span></span> |    <span data-ttu-id="fc52b-118">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="fc52b-118">Common Data Service (CDS)</span></span>         |     <span data-ttu-id="fc52b-119">Salg</span><span class="sxs-lookup"><span data-stu-id="fc52b-119">Sales</span></span>      |
|------------------------|----------------|----------------|
| <span data-ttu-id="fc52b-120">CDS-salgsordrehoveder</span><span class="sxs-lookup"><span data-stu-id="fc52b-120">CDS sales order headers</span></span>| <span data-ttu-id="fc52b-121">SalesOrder</span><span class="sxs-lookup"><span data-stu-id="fc52b-121">SalesOrder</span></span>     | <span data-ttu-id="fc52b-122">SalesOrders</span><span class="sxs-lookup"><span data-stu-id="fc52b-122">SalesOrders</span></span> |
| <span data-ttu-id="fc52b-123">CDS-salgsordrelinjer</span><span class="sxs-lookup"><span data-stu-id="fc52b-123">CDS sales order lines</span></span>  | <span data-ttu-id="fc52b-124">SalesOrderLine</span><span class="sxs-lookup"><span data-stu-id="fc52b-124">SalesOrderLine</span></span> | <span data-ttu-id="fc52b-125">SalesOrderDetails</span><span class="sxs-lookup"><span data-stu-id="fc52b-125">SalesOrderDetails</span></span>|

## <a name="entity-flow"></a><span data-ttu-id="fc52b-126">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="fc52b-126">Entity flow</span></span>

<span data-ttu-id="fc52b-127">Salgsordrer oprettes i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="fc52b-127">Sales orders are created in Finance and Operations and synchronized to Sales.</span></span>

<span data-ttu-id="fc52b-128">Filtre i skabelonen sikrer, at kun relevante salgsordrer medtages i synkroniseringen:</span><span class="sxs-lookup"><span data-stu-id="fc52b-128">Filters in the template ensure that only relevant sales orders are included in the synchronization:</span></span>

- <span data-ttu-id="fc52b-129">Både bestillings- og faktureringskunden på salgsordren, der stammer fra Sales, medtages i synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="fc52b-129">Both ordering and invoicing customer on the sales order that originate from Sales will be included in the synchronization.</span></span> <span data-ttu-id="fc52b-130">I Finance and Operations bruges felterne **OrderingCustomerIsExternallyMaintained** og **InvoiceCustomerIsExternallyMaintained** til at spore synkroniseringen i dataenheder.</span><span class="sxs-lookup"><span data-stu-id="fc52b-130">In Finance and Operations, the fields **OrderingCustomerIsExternallyMaintained** and **InvoiceCustomerIsExternallyMaintained** are used to track the synchronization in the data entities.</span></span>

- <span data-ttu-id="fc52b-131">**Salgsordren** i Finance and Operations skal bekræftes.</span><span class="sxs-lookup"><span data-stu-id="fc52b-131">The **Sales order** in Finance and Operations must be confirmed.</span></span> <span data-ttu-id="fc52b-132">Det er kun de bekræftede salgsordrer eller salgsordrer med højere behandlingsstatus, f.eks. status som leveret eller faktureret, der synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="fc52b-132">Only the confirmed sales orders or sales orders with higher processing status, for example, Shipped or Invoiced status, are synchronized to Sales.</span></span>

- <span data-ttu-id="fc52b-133">Når du opretter eller redigerer en salgsordre, skal batchkørslen **Beregn salgstotaler** i Finance and Operations udføres.</span><span class="sxs-lookup"><span data-stu-id="fc52b-133">After creating or modifying a sales order, the batch job **Calculate sales totals** in Finance and Operations must be executed.</span></span> <span data-ttu-id="fc52b-134">Kun salgsordrerne med beregnede salgstotaler synkroniseres med CDS og Sales.</span><span class="sxs-lookup"><span data-stu-id="fc52b-134">Only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="fc52b-135">Moms vedrørende gebyrer på **salgsordrehovedet** indgår i øjeblikket ikke i synkroniseringen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="fc52b-135">Tax related to charges on the **Sales order header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="fc52b-136">Det skyldes, at Sales ikke understøtter momsoplysninger på hovedniveau.</span><span class="sxs-lookup"><span data-stu-id="fc52b-136">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="fc52b-137">Moms, der er relateret til gebyrer på linjeniveau er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="fc52b-137">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="fc52b-138">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="fc52b-138">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="fc52b-139">Nye felter er føjet til enheden **Ordre** og vises på siden:</span><span class="sxs-lookup"><span data-stu-id="fc52b-139">New fields are added to the **Order** entity and displayed on the page:</span></span>

- <span data-ttu-id="fc52b-140">**Vedligeholdes eksternt** - Angivet til **Ja** når ordren kommer fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fc52b-140">**Is Maintained Externally** - Set to **Yes** when the order is coming from Finance and Operations.</span></span>

- <span data-ttu-id="fc52b-141">**Behandlingsstatus** – Bruges til at vise behandlingsstatussen for ordren i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fc52b-141">**Processing status** - Used to show the processing status of the order in Finance and Operations.</span></span> <span data-ttu-id="fc52b-142">Værdierne er:</span><span class="sxs-lookup"><span data-stu-id="fc52b-142">Values are:</span></span>

    - <span data-ttu-id="fc52b-143">Aktive</span><span class="sxs-lookup"><span data-stu-id="fc52b-143">Active</span></span>
    - <span data-ttu-id="fc52b-144">Bekræftet</span><span class="sxs-lookup"><span data-stu-id="fc52b-144">Confirmed</span></span>
    - <span data-ttu-id="fc52b-145">Følgeseddel</span><span class="sxs-lookup"><span data-stu-id="fc52b-145">Packing Slip</span></span>
    - <span data-ttu-id="fc52b-146">Er faktureret</span><span class="sxs-lookup"><span data-stu-id="fc52b-146">Invoiced</span></span>
    - <span data-ttu-id="fc52b-147">Plukket</span><span class="sxs-lookup"><span data-stu-id="fc52b-147">Picked</span></span>
    - <span data-ttu-id="fc52b-148">Delvist plukket</span><span class="sxs-lookup"><span data-stu-id="fc52b-148">Partially Picked</span></span>
    - <span data-ttu-id="fc52b-149">Delvist pakket</span><span class="sxs-lookup"><span data-stu-id="fc52b-149">Partially Packed</span></span>
    - <span data-ttu-id="fc52b-150">Afsendt</span><span class="sxs-lookup"><span data-stu-id="fc52b-150">Shipped</span></span>
    - <span data-ttu-id="fc52b-151">Delvist afsendt</span><span class="sxs-lookup"><span data-stu-id="fc52b-151">Partially Shipped</span></span>
    - <span data-ttu-id="fc52b-152">Delvist faktureret</span><span class="sxs-lookup"><span data-stu-id="fc52b-152">Partially Invoiced</span></span>
    - <span data-ttu-id="fc52b-153">Annulleret</span><span class="sxs-lookup"><span data-stu-id="fc52b-153">Cancelled</span></span>

<span data-ttu-id="fc52b-154">Indstillingen **Har kun eksternt vedligeholdte produkter** bruges i andre salgsordrescenarier (ved synkronisering fra Sales to Finance and Operation) til konsekvent at holde styr på, om salgsordren består udelukkende af **eksternt vedligeholdte produkter**, hvorved produkter vedligeholdes i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fc52b-154">The **Has Externally Maintained Products Only** setting is used in other sales order scenarios (from Sales to Finance and Operation sync) to consistently keep track of whether the sales order is made up entirely of **Externally Maintained Products**, in which case products are maintained in Finance and Operations.</span></span> <span data-ttu-id="fc52b-155">Dette sikrer, at du ikke forsøger at synkronisere salgsordrer med produkter, der er ukendte i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fc52b-155">This ensures that you don't try to sync sales order lines with products that are unknown to Finance and Operations.</span></span>
 
<span data-ttu-id="fc52b-156">Knapperne **Opret faktura**, **Annuller ordre**, **Genberegn**, **Hent produkter** og **Slå adresse op** knapperne på siden **Salgsordre** er skjult for eksternt vedligeholdte ordrer, da fakturaer oprettes i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="fc52b-156">The **Create Invoice**, **Cancel Order**, **Recalculate**, **Get Products** and **Lookup Address** buttons on the **Sales order** page are hidden for externally maintained orders because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="fc52b-157">Siden Ordre kan ikke redigeres, da salgsordreoplysninger synkroniseres fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="fc52b-157">The order page is non-editable because sales order information will be synced from Finance and Operations.</span></span>
 
<span data-ttu-id="fc52b-158">Feltet **Salgsordrestatus** forbliver aktivt for at sikre, at ændringer fra Finance and Operations kan flyde fra **salgsordren** i Sales.</span><span class="sxs-lookup"><span data-stu-id="fc52b-158">The **Sales order status** will remain active to ensure that changes from Finance and Operations can flow to the **Sales order** in Sales.</span></span> <span data-ttu-id="fc52b-159">Dette styres ved at angive standarden for **Statecode [Status]** til **Aktiv** i dataintegrationsprojektet.</span><span class="sxs-lookup"><span data-stu-id="fc52b-159">This is controlled by setting the default **Statecode [Status]** to **Active** in the Data integration project.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="fc52b-160">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="fc52b-160">Preconditions and mapping setup</span></span> 

<span data-ttu-id="fc52b-161">Før du synkroniserer salgsordrer, er det vigtigt at opdatere systemerne med følgende indstilling:</span><span class="sxs-lookup"><span data-stu-id="fc52b-161">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="fc52b-162">Konfiguration i Sales</span><span class="sxs-lookup"><span data-stu-id="fc52b-162">Setup in Sales</span></span>

- <span data-ttu-id="fc52b-163">Sikre tilladelser for det team, som brugeren (fra **Forbindelsessæt** i Sales) er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="fc52b-163">Ensure permissions for the team that the user (from your Sales **Connection set**) is assigned to.</span></span> <span data-ttu-id="fc52b-164">Hvis du bruger demodata, har brugeren normalt administratoradgang, men ikke teamet.</span><span class="sxs-lookup"><span data-stu-id="fc52b-164">If you are using demo data, usually the user has admin access, but not the team.</span></span> <span data-ttu-id="fc52b-165">Uden dette får du en fejl, der angiver, at det primære team mangler, når du kører projektet fra dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="fc52b-165">Without this you will get an error that Principal team is missing when running the project from Data integrator.</span></span> 

    - <span data-ttu-id="fc52b-166">Under **Indstillinger** > **Sikkerhed** > **Team** skal du vælge det relevante team, klikke på **Administrer roller** og vælge en rolle med de ønskede tilladelser, f.eks. systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="fc52b-166">Under **Settings** > **Security** > **Teams**, select the relevant team, click **Manage Roles** and select a role with the desired permissions e.g. System Administrator.</span></span>

- <span data-ttu-id="fc52b-167">Under **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, skal du sikre, at **Brug systemets prisberegningssystem** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fc52b-167">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="fc52b-168">Under **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, skal du sikre, at **Rabatberegningsmetode** er angivet til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="fc52b-168">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="fc52b-169">Konfiguration i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fc52b-169">Setup in Finance and Operations</span></span>

<span data-ttu-id="fc52b-170">Angiv **Salg og marketing** > **Periodiske opgaver** > **Beregn salgstotaler** til at køre som et batchjob med **Beregn totaler for salgsordrer** angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="fc52b-170">Set **Sales and marketing** > **Periodic tasks** > **Calculate sales totals** to run as a batch job, with **Calculate totals for sales orders** set to **Yes**.</span></span> <span data-ttu-id="fc52b-171">Det er vigtigt, fordi kun salgsordrerne med beregnede salgstotaler synkroniseres med CDS og Sales.</span><span class="sxs-lookup"><span data-stu-id="fc52b-171">This is important because only the sales orders with sales totals calculated will be synced to CDS and Sales.</span></span> <span data-ttu-id="fc52b-172">Frekvensen for batchjobbet skal være afstemt med frekvensen for salgsordresynkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="fc52b-172">The frequency of the batch job should be alligned with the frequency of the sales order synchronization.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="fc52b-173">Opsætning af dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="fc52b-173">Setup in the Data integration project</span></span>

#### <a name="salesheader-task"></a><span data-ttu-id="fc52b-174">Opgaven SalesHeader</span><span class="sxs-lookup"><span data-stu-id="fc52b-174">SalesHeader task</span></span>

- <span data-ttu-id="fc52b-175">Opdater tilknytningen til **CDS-organisations-id i Kilde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="fc52b-175">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span>

    - <span data-ttu-id="fc52b-176">Standardskabelonværdien for **Account_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="fc52b-176">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="fc52b-177">Standardskabelonværdien for **InvoiceAccount_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="fc52b-177">Default template value for **InvoiceAccount_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="fc52b-178">Standardskabelonværdien for **Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="fc52b-178">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="fc52b-179">Kontrollér, at den nødvendige tilknytning findes i **Kilde** > **CDS til InvoiceCountryRegionId to BillingAddress_Country** og for **DeliveryCountryRegionId til DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="fc52b-179">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId to BillingAddress_Country** and for **DeliveryCountryRegionId to DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="fc52b-180">Skabelonværdien er **ValueMap** med et antal lande, der er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="fc52b-180">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="fc52b-181">**Prisliste** er nødvendig for at kunne oprette ordrer i Sales.</span><span class="sxs-lookup"><span data-stu-id="fc52b-181">**Price list** is required to create orders in Sales.</span></span> <span data-ttu-id="fc52b-182">Opdater **ValueMap** i **CDS** > **Destination** for **pricelevelid.name [prislistenavnet]** til den **prisliste**, der bruges i Sales pr. valuta.</span><span class="sxs-lookup"><span data-stu-id="fc52b-182">Update the **ValueMap** in **CDS** > **Destination** for **pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="fc52b-183">Du kan enten bruge **standardprislisten** til hver enkelt valuta eller bruge **ValueMap**, hvis du har **prislister** i flere valutaer.</span><span class="sxs-lookup"><span data-stu-id="fc52b-183">You can either used the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>
    
    - <span data-ttu-id="fc52b-184">Standardskabelonværdien for **pricelevelid.name [prislistenavnet]** er CRM Service USA (eksempel).</span><span class="sxs-lookup"><span data-stu-id="fc52b-184">Default template value for **pricelevelid.name [Price List Name]** is CRM Service USA (sample).</span></span> 

#### <a name="salesline-task"></a><span data-ttu-id="fc52b-185">Opgaven SalesLine</span><span class="sxs-lookup"><span data-stu-id="fc52b-185">SalesLine task</span></span>

- <span data-ttu-id="fc52b-186">Opdater tilknytningen til **CDS-organisations-id i Kilde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="fc52b-186">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 
    
    - <span data-ttu-id="fc52b-187">Standardskabelonværdien for **SalesOrder_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="fc52b-187">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    - <span data-ttu-id="fc52b-188">Standardskabelonværdien for **Product_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="fc52b-188">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="fc52b-189">Du skal sikre, at den nødvendige tilknytning findes i **Kilde** > **CDS** for **DeliveryCountryRegionId** til **DeliveryAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="fc52b-189">Ensure that the needed mapping exists in **Source** > **CDS** for **DeliveryCountryRegionId** to **DeliveryAddress_Country**.</span></span>

    - <span data-ttu-id="fc52b-190">Skabelonværdien er **ValueMap** med et antal lande, der er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="fc52b-190">Template value is **ValueMap** with a number of countries mapped.</span></span>
    
- <span data-ttu-id="fc52b-191">Du skal sikre, at den påkrævede **ValueMap** for **SalesUnitSymbol** i Finance and Operations findes i **Kilde** > **CDS-tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="fc52b-191">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span>

    - <span data-ttu-id="fc52b-192">Skabelonværdi med **ValueMap** er defineret for **SalesUnitSymbol til Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="fc52b-192">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="fc52b-193">Tilknytning af skabelon i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="fc52b-193">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="fc52b-194">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="fc52b-194">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="fc52b-195">Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="fc52b-195">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="fc52b-196">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="fc52b-196">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="orderheader"></a><span data-ttu-id="fc52b-197">OrderHeader</span><span class="sxs-lookup"><span data-stu-id="fc52b-197">OrderHeader</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-order-template-mapping-data-integrator-1.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-order-template-mapping-data-integrator-2.png)

### <a name="orderline"></a><span data-ttu-id="fc52b-200">OrderLine</span><span class="sxs-lookup"><span data-stu-id="fc52b-200">OrderLine</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-order-template-mapping-data-integrator-3.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-order-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="fc52b-203">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="fc52b-203">Related topics</span></span>

[<span data-ttu-id="fc52b-204">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="fc52b-204">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="fc52b-205">Synkronisere konti fra Sales med debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fc52b-205">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="fc52b-206">Synkronisere kontakter fra Sales med kontakter eller debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fc52b-206">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="fc52b-207">Synkronisere titler og linjer i salgstilbud fra Sales med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="fc52b-207">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="fc52b-208">Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="fc52b-208">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)


