---
title: Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Sales.
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 6cf267d85795f6a7c253782b826cc75abef89d9f
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="synchronize-sales-invoice-headers-and-lines-directly-from-finance-and-operations-to-sales"></a><span data-ttu-id="3dafa-103">Synkronisere salgsfakturahoveder og linjer fra Finance and Operations direkte med Sales</span><span class="sxs-lookup"><span data-stu-id="3dafa-103">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="3dafa-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer direkte fra Microsoft Dynamics 365 for Finance and Operations til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="3dafa-104">This topic discusses the templates and underlying tasks that are used to synchronize sales invoice headers and lines directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="3dafa-105">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="3dafa-105">Data flow in Prospect to cash</span></span>

<span data-ttu-id="3dafa-106">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="3dafa-106">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="3dafa-107">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="3dafa-107">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="3dafa-108">I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="3dafa-108">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="3dafa-109">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="3dafa-109">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="3dafa-110">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="3dafa-110">Templates and tasks</span></span>

<span data-ttu-id="3dafa-111">For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="3dafa-111">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="3dafa-112">Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="3dafa-112">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="3dafa-113">Følgende skabelon og underliggende opgaver bruges til at synkronisere salgsfakturahoveder og -linjer fra Finance and Operations til Sales:</span><span class="sxs-lookup"><span data-stu-id="3dafa-113">The following template and underlying tasks are used to synchronize sales invoice headers and lines from Finance and Operations to Sales:</span></span>

- <span data-ttu-id="3dafa-114">**Navnet på skabelonen i dataintegration:** Salgsfakturaer (Fin and Ops til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="3dafa-114">**Name of the template in Data integration:** Sales Invoices (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="3dafa-115">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="3dafa-115">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="3dafa-116">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="3dafa-116">SalesInvoiceHeader</span></span>
    - <span data-ttu-id="3dafa-117">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="3dafa-117">SalesInvoiceLine</span></span>

<span data-ttu-id="3dafa-118">Følgende synkroniseringsopgaver kræves, før salgsfakturahoveder og -linjer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="3dafa-118">The following synchronization tasks are required before synchronization of sales invoice headers and lines can occur:</span></span>

- <span data-ttu-id="3dafa-119">Produkter (Fin and Ops til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="3dafa-119">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="3dafa-120">Konti (Sales til Fin and Ops) - Direkte (hvis den bruges)</span><span class="sxs-lookup"><span data-stu-id="3dafa-120">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="3dafa-121">Kontakter (Sales til Fin and Ops) - Direkte (hvis den bruges)</span><span class="sxs-lookup"><span data-stu-id="3dafa-121">Contacts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="3dafa-122">Salgsordrehoved og -linjer (Fin and Ops til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="3dafa-122">Sales order header and lines (Fin and Ops to Sales) - Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="3dafa-123">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="3dafa-123">Entity set</span></span>

| <span data-ttu-id="3dafa-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dafa-124">Finance and Operations</span></span>                               | <span data-ttu-id="3dafa-125">Salg</span><span class="sxs-lookup"><span data-stu-id="3dafa-125">Sales</span></span>          |
|------------------------------------------------------|----------------|
| <span data-ttu-id="3dafa-126">Eksternt vedligeholdte kundesalgsfakturahoveder</span><span class="sxs-lookup"><span data-stu-id="3dafa-126">Externally maintained customer sales invoice headers</span></span> | <span data-ttu-id="3dafa-127">Fakturaer</span><span class="sxs-lookup"><span data-stu-id="3dafa-127">Invoices</span></span>       |
| <span data-ttu-id="3dafa-128">Eksternt vedligeholdte kundesalgsfakturalinjer</span><span class="sxs-lookup"><span data-stu-id="3dafa-128">Externally maintained customer sales invoice lines</span></span>   | <span data-ttu-id="3dafa-129">InvoiceDetails</span><span class="sxs-lookup"><span data-stu-id="3dafa-129">InvoiceDetails</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="3dafa-130">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="3dafa-130">Entity flow</span></span>

<span data-ttu-id="3dafa-131">Salgsfakturaer oprettes i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="3dafa-131">Sales invoices are created in Finance and Operations and synchronized to Sales.</span></span>

> [!NOTE]
> <span data-ttu-id="3dafa-132">Moms vedrørende gebyrer på salgsfakturahovedet indgår i øjeblikket ikke i synkroniseringen fra Finance and Operations til Sales.</span><span class="sxs-lookup"><span data-stu-id="3dafa-132">Currently, tax that is related to charges on the sales invoice header isn't included in the synchronization from Finance and Operations to Sales.</span></span> <span data-ttu-id="3dafa-133">Sales understøtter ikke momsoplysninger på hovedniveau.</span><span class="sxs-lookup"><span data-stu-id="3dafa-133">Sales doesn't support tax information at the header level.</span></span> <span data-ttu-id="3dafa-134">Men moms, som er relateret til gebyrer på linjeniveau, er imidlertid inkluderet i synkroniseringen.</span><span class="sxs-lookup"><span data-stu-id="3dafa-134">However, tax that is related to charges at the line level is included in the synchronization.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="3dafa-135">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="3dafa-135">Prospect to cash solution for Sales</span></span>

- <span data-ttu-id="3dafa-136">Feltet **Fakturanummer** er føjet til enheden **Faktura** og vises på siden.</span><span class="sxs-lookup"><span data-stu-id="3dafa-136">An **Invoice number** field has been added to the **Invoice** entity and appears on the page.</span></span>
- <span data-ttu-id="3dafa-137">Knappen **Opret faktura** på siden **Salgsordre** er skjult, da fakturaer oprettes i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="3dafa-137">The **Create invoice** button on the **Sales order** page is hidden, because invoices will be created in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="3dafa-138">Siden **Faktura** kan ikke redigeres, fordi fakturaer synkroniseres fra Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dafa-138">The **Invoice** page can't be edited, because invoices will be synchronized from Finance and Operations.</span></span>
- <span data-ttu-id="3dafa-139">Værdien **Salgsordrestatus** ændres automatisk til **Faktureret**, når den relaterede faktura fra Finance and Operations er blevet synkroniseret til Sales.</span><span class="sxs-lookup"><span data-stu-id="3dafa-139">The **Sales order status** value is automatically changed to **Invoiced** when the related invoice from Finance and Operations has been synchronized to Sales.</span></span> <span data-ttu-id="3dafa-140">Desuden tildeles ejeren af den salgsordre, hvorfra fakturaen blev oprettet, som ejer af fakturaen.</span><span class="sxs-lookup"><span data-stu-id="3dafa-140">Additionally, the owner of the sales order that the invoice was created from is assigned as the owner of the invoice.</span></span> <span data-ttu-id="3dafa-141">Ejeren af salgsordren kan derfor få vist fakturaen.</span><span class="sxs-lookup"><span data-stu-id="3dafa-141">Therefore, the owner of the sales order can view the invoice.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="3dafa-142">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="3dafa-142">Preconditions and mapping setup</span></span>

<span data-ttu-id="3dafa-143">Før du synkroniserer salgsfakturaer, er det vigtigt, at du opdaterer følgende indstillinger i systemerne.</span><span class="sxs-lookup"><span data-stu-id="3dafa-143">Before you synchronize sales invoices, it's important that you update the following settings in the systems.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="3dafa-144">Konfiguration i Sales</span><span class="sxs-lookup"><span data-stu-id="3dafa-144">Setup in Sales</span></span>

<span data-ttu-id="3dafa-145">Gå til **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales**, og sørg for, at der bruges til følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="3dafa-145">Go to **Settings** > **Administration** > **System settings** > **Sales**, and make sure that the following settings are used:</span></span>

- <span data-ttu-id="3dafa-146">Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="3dafa-146">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
- <span data-ttu-id="3dafa-147">Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="3dafa-147">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="3dafa-148">Opsætning af dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="3dafa-148">Setup in the Data integration project</span></span>

#### <a name="salesinvoiceheader-task"></a><span data-ttu-id="3dafa-149">Opgaven SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="3dafa-149">SalesInvoiceHeader task</span></span>

- <span data-ttu-id="3dafa-150">Du skal sikre, at den nødvendige tilknytning findes for **InvoiceCountryRegionId** til **BillingAddress\_Country**.</span><span class="sxs-lookup"><span data-stu-id="3dafa-150">Make sure that the required mapping exists for **InvoiceCountryRegionId** to **BillingAddress\_Country**.</span></span>

    <span data-ttu-id="3dafa-151">Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="3dafa-151">The template value is a value map where several countries or regions are mapped.</span></span>

- <span data-ttu-id="3dafa-152">Der kræves en prisliste for at kunne oprette fakturaer i Sales.</span><span class="sxs-lookup"><span data-stu-id="3dafa-152">A price list is required in order to create invoices in Sales.</span></span> <span data-ttu-id="3dafa-153">Opdater værditilknytningen **pricelevelid.name \[prislistenavnet\]** til den prisliste, der bruges i Sales efter valuta.</span><span class="sxs-lookup"><span data-stu-id="3dafa-153">Update the value map for **pricelevelid.name \[Price list name\]** to the price list that is used in Sales per currency.</span></span> <span data-ttu-id="3dafa-154">Du kan bruge standardprislisten til en enkelt valuta.</span><span class="sxs-lookup"><span data-stu-id="3dafa-154">You can use the default price list for a single currency.</span></span> <span data-ttu-id="3dafa-155">Hvis du har prislister i flere valutaer, kan du også bruge en værditilknytning.</span><span class="sxs-lookup"><span data-stu-id="3dafa-155">Alternatively, if you have price lists in multiple currencies, you can use a value map.</span></span>

    <span data-ttu-id="3dafa-156">Skabelonværdien for **pricelevelid.name \[prislistenavnet\]** er en værditilknytning, der er baseret på valuta med USD = CRM Service USA (eksempel).</span><span class="sxs-lookup"><span data-stu-id="3dafa-156">The template value for **pricelevelid.name \[Price list name\]** is a value map that is based on currency with USD = CRM Service USA (sample).</span></span>  
    
#### <a name="salesinvoiceline-task"></a><span data-ttu-id="3dafa-157">Opgaven SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="3dafa-157">SalesInvoiceLine task</span></span>

- <span data-ttu-id="3dafa-158">Du skal sikre, at den nødvendige tilknytning findes for **Måleenhed**.</span><span class="sxs-lookup"><span data-stu-id="3dafa-158">Make sure that the required mapping exists for **Unit of measure**.</span></span>
- <span data-ttu-id="3dafa-159">Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dafa-159">Make sure that the required value map for **SalesUnitSymbol** in Finance and Operations exists.</span></span>

    <span data-ttu-id="3dafa-160">En skabelonværdi, der har en værditilknytning, er defineret for **SalesUnitSymbol** til **Quantity\_UOM**</span><span class="sxs-lookup"><span data-stu-id="3dafa-160">A template value that has a value map is defined for **SalesUnitSymbol** to **Quantity\_UOM**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="3dafa-161">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="3dafa-161">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="3dafa-162">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** indgår ikke i standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="3dafa-162">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="3dafa-163">Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="3dafa-163">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="3dafa-164">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="3dafa-164">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="3dafa-165">Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="3dafa-165">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="salesinvoiceheader"></a><span data-ttu-id="3dafa-166">SalesInvoiceHeader</span><span class="sxs-lookup"><span data-stu-id="3dafa-166">SalesInvoiceHeader</span></span>

![Skabelontilknytning i dataintegration](./media/sales-invoice-direct-template-mapping-data-integrator-1.png)

### <a name="salesinvoiceline"></a><span data-ttu-id="3dafa-168">SalesInvoiceLine</span><span class="sxs-lookup"><span data-stu-id="3dafa-168">SalesInvoiceLine</span></span>

![Skabelontilknytning i dataintegration](./media/sales-invoice-direct-template-mapping-data-integrator-2.png)



## <a name="related-topics"></a><span data-ttu-id="3dafa-170">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="3dafa-170">Related topics</span></span>

[<span data-ttu-id="3dafa-171">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="3dafa-171">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="3dafa-172">Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dafa-172">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="3dafa-173">Synkronisere produkter fra Finance and Operations direkte med produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="3dafa-173">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="3dafa-174">Synkronisere kontakter fra Sales direkte med kontakter eller debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="3dafa-174">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="3dafa-175">Synkronisere salgsordrehoveder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="3dafa-175">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)







