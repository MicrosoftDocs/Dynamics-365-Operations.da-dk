---
title: Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 08/28/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: 
audience: Application User, IT Pro
ms.reviewer: yuyus
ms.search.scope: Core, Operations, UnifiedOperations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: fb5ba099911deda5308daf92d82cd6b3489995bf
ms.contentlocale: da-dk
ms.lasthandoff: 09/29/2017

---

# <a name="synchronize-sales-invoice-headers-and-lines-from-finance-and-operations-to-sales"></a><span data-ttu-id="c8054-103">Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="c8054-103">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="c8054-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer fra Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="c8054-104">The topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span> 

## <a name="templates-and-tasks"></a><span data-ttu-id="c8054-105">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="c8054-105">Templates and tasks</span></span>

<span data-ttu-id="c8054-106">Følgende skabeloner og underliggende opgaver bruges til at synkronisere salgsfakturahoveder og -linjer fra Finance and Operations til Sales:</span><span class="sxs-lookup"><span data-stu-id="c8054-106">The following templates and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="c8054-107">**Navnet på skabelonen i dataintegration**</span><span class="sxs-lookup"><span data-stu-id="c8054-107">**Name of the template in Data integration**</span></span> 

     - <span data-ttu-id="c8054-108">Salgsfakturaer (Fin og Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="c8054-108">Sales Invoices (Fin and Ops to Sales)</span></span>

- <span data-ttu-id="c8054-109">**Navnene på opgaverne i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="c8054-109">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="c8054-110">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="c8054-110">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="c8054-111">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="c8054-111">SalesInvoiceLine</span></span>

<span data-ttu-id="c8054-112">Synkroniseringsopgaver, der kræves før synkronisering af salgsfakturahoved og -linjer:</span><span class="sxs-lookup"><span data-stu-id="c8054-112">Sync tasks required prior to Sales invoice header and lines synchronization:</span></span>
-   <span data-ttu-id="c8054-113">Produkter (Fin og Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="c8054-113">Products (Fin and Ops to Sales)</span></span>
-   <span data-ttu-id="c8054-114">Konti (Sales til Fin og Ops) (hvis det bruges)</span><span class="sxs-lookup"><span data-stu-id="c8054-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="c8054-115">Kontakter (Sales til Fin og Ops) (hvis det bruges)</span><span class="sxs-lookup"><span data-stu-id="c8054-115">Contacts (Sales to Fin and Ops) (if used)</span></span>
-   <span data-ttu-id="c8054-116">Salgsordrehoved og -linjer (Fin og Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="c8054-116">Sales order header and lines (Fin and Ops to Sales)</span></span>

## <a name="entity-set"></a><span data-ttu-id="c8054-117">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="c8054-117">Entity set</span></span>

| <span data-ttu-id="c8054-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8054-118">Finance and Operations</span></span>                               | <span data-ttu-id="c8054-119">Common Data Service</span><span class="sxs-lookup"><span data-stu-id="c8054-119">Common Data Service (CDS)</span></span>              | <span data-ttu-id="c8054-120">Salg</span><span class="sxs-lookup"><span data-stu-id="c8054-120">Sales</span></span>          |
|------------------------------------------------------|------------------|----------------|
| <span data-ttu-id="c8054-121">Eksternt vedligeholdte kundesalgsfakturahoveder</span><span class="sxs-lookup"><span data-stu-id="c8054-121">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="c8054-122">SalesInvoice</span><span class="sxs-lookup"><span data-stu-id="c8054-122">SalesInvoice</span></span>     | <span data-ttu-id="c8054-123">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="c8054-123">Invoices</span></span>       |
| <span data-ttu-id="c8054-124">Eksternt vedligeholdte kundesalgsfakturalinjer</span><span class="sxs-lookup"><span data-stu-id="c8054-124">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="c8054-125">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="c8054-125">SalesInvoiceLine</span></span> | <span data-ttu-id="c8054-126">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="c8054-126">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="c8054-127">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="c8054-127">Entity flow</span></span>

<span data-ttu-id="c8054-128">Salgsfakturaer oprettes i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="c8054-128">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="c8054-129">Moms vedrørende gebyrer på **salgsfakturahovedet** indgår i øjeblikket ikke i synkroniseringen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="c8054-129">Tax related to charges on the **Sales invoice header** is currently not included in synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="c8054-130">Det skyldes, at Sales ikke understøtter momsoplysninger på hovedniveau.</span><span class="sxs-lookup"><span data-stu-id="c8054-130">This is because Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="c8054-131">Moms, der er relateret til gebyrer på linjeniveau er inkluderet.</span><span class="sxs-lookup"><span data-stu-id="c8054-131">Tax related to charges at the line level is included.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="c8054-132">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="c8054-132">Prospect to cash solution for Sales</span></span>

-  <span data-ttu-id="c8054-133">Et **Fakturanummerfelt** er føjet til enheden **Faktura** og vises på siden.</span><span class="sxs-lookup"><span data-stu-id="c8054-133">An **Invoice number field** is added to the **Invoice** entity and displayed on the page.</span></span>
 
-  <span data-ttu-id="c8054-134">Knappen **Opret faktura** på siden **Salgsordre** er skjult, da fakturaer oprettes i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="c8054-134">The **Create invoice** button on the **Sales order** page is hidden because invoices will be created in Finance and Operations and synced to Sales.</span></span> <span data-ttu-id="c8054-135">Siden **Faktura** kan ikke redigeres, fordi fakturaer synkroniseres fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="c8054-135">The **Invoice** page is non-editable because invoices will be synced from Finance and Operations.</span></span>
 
-  <span data-ttu-id="c8054-136">Feltet **Salgsordrestatus** ændres automatisk til **Faktureret**, når den relaterede faktura fra Finance and Operations er blevet synkroniseret til Sales.</span><span class="sxs-lookup"><span data-stu-id="c8054-136">The **Sales order status** changes automatically to **Invoiced** when the related invoice from Finance and Operations has been  synchronized to Sales.</span></span> <span data-ttu-id="c8054-137">Desuden tildeles ejeren af den salgsordre, hvorfra fakturaen blev oprettet, som ejer af fakturaen.</span><span class="sxs-lookup"><span data-stu-id="c8054-137">Also, the owner of the sales order from which the invoice was created is assigned as the owner of the invoice.</span></span> <span data-ttu-id="c8054-138">Det giver ejeren af salgsordren mulighed for at få vist fakturaen.</span><span class="sxs-lookup"><span data-stu-id="c8054-138">This gives the owner of the sales order the ability to view the invoice.</span></span>
 
## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="c8054-139">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="c8054-139">Preconditions and mapping setup</span></span>

<span data-ttu-id="c8054-140">Før du synkroniserer salgsfakturaer, er det vigtigt at opdatere systemerne med følgende indstilling:</span><span class="sxs-lookup"><span data-stu-id="c8054-140">Before synchronizing sales invoices, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="c8054-141">Konfiguration i Sales</span><span class="sxs-lookup"><span data-stu-id="c8054-141">Setup in Sales</span></span>

- <span data-ttu-id="c8054-142">Under **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, skal du sikre, at **Brug systemets prisberegningssystem** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="c8054-142">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Use system prizing calculation system** is set to **Yes**.</span></span> 

- <span data-ttu-id="c8054-143">Under **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, skal du sikre, at **Rabatberegningsmetode** er angivet til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="c8054-143">Under **Settings** > **Administration** > **System settings** > **Sales**, ensure that **Discount calculation method** is set to **Line item**.</span></span> 

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="c8054-144">Opsætning af dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="c8054-144">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="c8054-145">Opgaven SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="c8054-145">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="c8054-146">Opdater tilknytningen til **CDS-organisations-id** i **Kilde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="c8054-146">Update the mapping for **CDS Organization ID** in **Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="c8054-147">Standardskabelonværdien for **SalesOrder_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="c8054-147">Default template value for **SalesOrder_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="c8054-148">Standardskabelonværdien for **Account_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="c8054-148">Default template value for **Account_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="c8054-149">Standardskabelonværdien for **Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="c8054-149">Default template value for **Organization_OrganizationId** is ORG001.</span></span>

- <span data-ttu-id="c8054-150">Du skal sikre, at den nødvendige tilknytning findes i **Kilde** > **CDS til InvoiceCountryRegionId** til **BillingAddress_Country**.</span><span class="sxs-lookup"><span data-stu-id="c8054-150">Ensure that the needed mapping exists in **Source** > **CDS for InvoiceCountryRegionId** to **BillingAddress_Country**.</span></span>

    -  <span data-ttu-id="c8054-151">Skabelonværdien er **ValueMap** med et antal lande, der er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="c8054-151">Template value is **ValueMap** with a number of countries mapped.</span></span>

- <span data-ttu-id="c8054-152">**Prisliste** er nødvendig for at kunne oprette fakturaer i Sales.</span><span class="sxs-lookup"><span data-stu-id="c8054-152">**Price list** is required to create invoices in Sales.</span></span> <span data-ttu-id="c8054-153">Opdater **ValueMap** i **CDS** > **Destination for pricelevelid.name [prislistenavnet]** til den **Prisliste**, der bruges i Sales pr. valuta.</span><span class="sxs-lookup"><span data-stu-id="c8054-153">Update the **ValueMap** in **CDS** > **Destination for pricelevelid.name [Price List Name]** to the **Price list** used in Sales per currency.</span></span> <span data-ttu-id="c8054-154">Du kan enten bruge **standardprislisten** til hver enkelt valuta eller bruge **ValueMap**, hvis du har **prislister** i flere valutaer.</span><span class="sxs-lookup"><span data-stu-id="c8054-154">You can either use the default **Price list** for single currency or use **ValueMap** if you have **Price lists** in multiple currencies.</span></span>

    -  <span data-ttu-id="c8054-155">Skabelonværdi for **pricelevelid.name [prislistenavnet]** er **ValueMap** baseret på **valuta**.</span><span class="sxs-lookup"><span data-stu-id="c8054-155">Template value for **pricelevelid.name [Price List Name]** is **ValueMap** based on **Currency**.</span></span>
    -  <span data-ttu-id="c8054-156">USD: CRM-tjenesten USA (eksempel).</span><span class="sxs-lookup"><span data-stu-id="c8054-156">usd: CRM Service USA (sample).</span></span> 

#### <a name="salesinvoiceline-task"></a><span data-ttu-id="c8054-157">Opgaven SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="c8054-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="c8054-158">Du skal sikre, at den nødvendige tilknytning findes i **Kilde** > **CDS til måleenhed**.</span><span class="sxs-lookup"><span data-stu-id="c8054-158">Ensure that the needed mapping exists in **Source** > **CDS for Unit of measure**.</span></span>

- <span data-ttu-id="c8054-159">Du skal sikre, at den påkrævede **ValueMap** for **SalesUnitSymbol** i Finance and Operations findes i **Kilde** > **CDS-tilknytning**.</span><span class="sxs-lookup"><span data-stu-id="c8054-159">Ensure that the needed **ValueMap** for **SalesUnitSymbol** in Finance and Operations exists in the **Source** > **CDS mapping**.</span></span> 
    
    - <span data-ttu-id="c8054-160">Skabelonværdi med **ValueMap** er defineret for **SalesUnitSymbol til Quantity_UOM**.</span><span class="sxs-lookup"><span data-stu-id="c8054-160">Template value with **ValueMap** is defined for **SalesUnitSymbol to Quantity_UOM**.</span></span>
    
-  <span data-ttu-id="c8054-161">Opdater tilknytningen til **CDS-organisations-id i Kilde** > **CDS**.</span><span class="sxs-lookup"><span data-stu-id="c8054-161">Update the mapping for **CDS Organization ID in Source** > **CDS**.</span></span> 

    -  <span data-ttu-id="c8054-162">Standardskabelonværdien for **SalesInvoicer_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="c8054-162">Default template value for **SalesInvoicer_Organization_OrganizationId** is ORG001.</span></span>
    -  <span data-ttu-id="c8054-163">Standardskabelonværdien for **Product_Organization_OrganizationId** er ORG001.</span><span class="sxs-lookup"><span data-stu-id="c8054-163">Default template value for **Product_Organization_OrganizationId** is ORG001.</span></span>
 
## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="c8054-164">Skabelontilknytning i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="c8054-164">Template mapping in Data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="c8054-165">**Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="c8054-165">**Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** are not part of the default mappings.</span></span> <span data-ttu-id="c8054-166">Tilknytning af disse felter kræver angivelse af en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="c8054-166">Mapping of these fields requires value mapping to be set up, which is specific to the data in the organizations between which the entity is synchronized.</span></span>

<span data-ttu-id="c8054-167">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="c8054-167">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-1.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-2.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-3.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-invoice-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="c8054-172">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="c8054-172">Related topics</span></span>

[<span data-ttu-id="c8054-173">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="c8054-173">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="c8054-174">Synkronisere konti fra Sales med debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8054-174">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="c8054-175">Synkronisere kontakter fra Sales med kontakter eller debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8054-175">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="c8054-176">Synkronisere titler og linjer i salgstilbud fra Sales med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="c8054-176">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="c8054-177">Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="c8054-177">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)


