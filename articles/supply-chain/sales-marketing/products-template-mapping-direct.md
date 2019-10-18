---
title: Synkronisere produkter direkte fra Supply Chain Management med produkter i Sales
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 06/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: 38f0db7db0cc4f65d46cd241f75a7274f19f62cf
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2251379"
---
# <a name="synchronize-products-directly-from-supply-chain-management-to-products-in-sales"></a><span data-ttu-id="fda95-103">Synkronisere produkter direkte fra Supply Chain Management med produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="fda95-103">Synchronize products directly from Supply Chain Management to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="fda95-104">Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="fda95-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="fda95-105">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere produkter direkte fra Dynamics 365 Supply Chain Management til Dynamics 365 Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Dynamics 365 Supply Chain Management to Dynamics 365 Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="fda95-106">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="fda95-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="fda95-107">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="fda95-108">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om konti, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="fda95-109">I følgende illustration vises, hvordan data synkroniseres mellem Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="fda95-110">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="fda95-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="fda95-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="fda95-111">Templates and tasks</span></span>

<span data-ttu-id="fda95-112">For at få adgang til de tilgængelige skabeloner skal du åbne [PowerApps Administration](https://admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="fda95-112">To access the available templates, open [PowerApps Admin Center](https://admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="fda95-113">Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="fda95-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="fda95-114">Følgende skabelon og underliggende opgaver bruges til at synkronisere produkter fra Supply Chain Management til Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-114">The following template and underlying tasks are used to synchronize products from Supply Chain Management to Sales.</span></span>

- <span data-ttu-id="fda95-115">**Navnet på skabelonen i dataintegration:** Produkter (Supply Chain Management til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="fda95-115">**Name of the template in Data integration:** Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="fda95-116">**Navnet på opgaven i dataintegrationsprojektet:** Produkter</span><span class="sxs-lookup"><span data-stu-id="fda95-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="fda95-117">Der kræves ingen synkroniseringsopgaver, før der kan forekomme synkronisering af produkt.</span><span class="sxs-lookup"><span data-stu-id="fda95-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="fda95-118">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="fda95-118">Entity set</span></span>

| <span data-ttu-id="fda95-119">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fda95-119">Supply Chain Management</span></span>    | <span data-ttu-id="fda95-120">Salg</span><span class="sxs-lookup"><span data-stu-id="fda95-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="fda95-121">Salgbare frigivne produkter</span><span class="sxs-lookup"><span data-stu-id="fda95-121">Sellable released products</span></span> | <span data-ttu-id="fda95-122">Produkter</span><span class="sxs-lookup"><span data-stu-id="fda95-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="fda95-123">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="fda95-123">Entity flow</span></span>

<span data-ttu-id="fda95-124">Produkter administreres i Supply Chain Management og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-124">Products are managed in Supply Chain Management and synchronized to Sales.</span></span> <span data-ttu-id="fda95-125">Dataenheden **Salgbare frigivne produkter** i Supply Chain Management eksporterer kun produkter, der er *salgbare*.</span><span class="sxs-lookup"><span data-stu-id="fda95-125">The **Sellable released products** data entity in Supply Chain Management exports only products that are *sellable*.</span></span> <span data-ttu-id="fda95-126">Salgbare produkter er produkter med de oplysninger, de skal bruge for at kunne bruges på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="fda95-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="fda95-127">De samme regler gælder, når et produkt valideres ved brug af funktionen **Valider** på siden **Frigivet produkt**.</span><span class="sxs-lookup"><span data-stu-id="fda95-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="fda95-128">Produktnummeret bruges som en nøgle.</span><span class="sxs-lookup"><span data-stu-id="fda95-128">The product number is used as a key.</span></span> <span data-ttu-id="fda95-129">Når produktvarianter synkroniseres til Sales, har hver produktvariant derfor et individuelt produkt-id.</span><span class="sxs-lookup"><span data-stu-id="fda95-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="fda95-130">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="fda95-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="fda95-131">I Sales er tilføjet et nyt felt **Vedligeholdes eksternt** for produkterne, for at angive, at et bestemt produkt vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="fda95-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="fda95-132">Som standard er værdien indstillet til **Ja** under import til Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="fda95-133">Følgende værdier er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="fda95-133">The following values are available:</span></span>

- <span data-ttu-id="fda95-134">**Ja** – Produktet stammer fra Supply Chain Management, og det kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-134">**Yes** – The product originated from Supply Chain Management and won't be editable in Sales.</span></span>
- <span data-ttu-id="fda95-135">**Nej** – Produktet blev angivet direkte i Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="fda95-136">**(Tom)** – Produktet fandtes i Sales, før kundeemne til kontanter-løsningen blev aktiveret.</span><span class="sxs-lookup"><span data-stu-id="fda95-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="fda95-137">Feltet **Vedligeholdes eksternt** bruges til at sikre, at det kun er tilbud og salgsordrer med eksternt vedligeholdte produkter, der synkroniseres til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fda95-137">The **Is Externally Maintained** field helps ensure that only quotations and sales orders that have externally maintained products will be synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="fda95-138">Eksternt vedligeholdte produkter føjes automatisk til den første gyldige prisliste, der har den samme valuta.</span><span class="sxs-lookup"><span data-stu-id="fda95-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="fda95-139">Prislister organiseres alfabetisk efter navn.</span><span class="sxs-lookup"><span data-stu-id="fda95-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="fda95-140">Produktets salgspris fra Supply Chain Management bruges som prisen på prislisten.</span><span class="sxs-lookup"><span data-stu-id="fda95-140">The product sales price from Supply Chain Management is used as the price on the price list.</span></span> <span data-ttu-id="fda95-141">Derfor skal der være en prisliste i Sales for hver produktsalgsvaluta i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fda95-141">Therefore, there must be a price list in Sales for every product sales currency in Supply Chain Management.</span></span> <span data-ttu-id="fda95-142">Valutaen for de frigivne salgbare produkter indstilles til regnskabsvalutaen i den juridiske enhed, som produktet eksporteres fra.</span><span class="sxs-lookup"><span data-stu-id="fda95-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> - <span data-ttu-id="fda95-143">Produktsynkronisering lykkes ikke, medmindre der er en prisliste, der har en tilsvarende valuta.</span><span class="sxs-lookup"><span data-stu-id="fda95-143">Product synchronization will not succeed unless there is a price list that has a matching currency.</span></span>
> - <span data-ttu-id="fda95-144">Du kan styre den anvendte prisliste til integrationen ved at tilknytte pricelevelid.name [standardprisliste (navn)] i dataintegrationsprojektet.</span><span class="sxs-lookup"><span data-stu-id="fda95-144">You can control the used price list with the integration by mapping the pricelevelid.name [Default Price List (Name)] in the Data Integration project.</span></span> <span data-ttu-id="fda95-145">Inputtet skal skrives med små bogstaver.</span><span class="sxs-lookup"><span data-stu-id="fda95-145">The input has to be in all lowercase letters.</span></span> <span data-ttu-id="fda95-146">For eksempel vil standarden for en prisliste i Sales, der hedder 'Standard', være: Destinationsfelt: pricelevelid.name [standardprisliste (navn)] og tilknytningstype: [ { "transformType": "Standard", "defaultValue": "standard" } ].</span><span class="sxs-lookup"><span data-stu-id="fda95-146">For example, the default for a price list in Sales named ‘Standard’ would be: Destination field: pricelevelid.name [Default Price List (Name)] and Map type: [ { "transformType": "Default", "defaultValue": "standard" } ].</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="fda95-147">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="fda95-147">Preconditions and mapping setup</span></span>

- <span data-ttu-id="fda95-148">Inden du kører synkronisering for første gang, skal du udfylde tabellen Specifikt produkt for de eksisterende produkter i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fda95-148">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Supply Chain Management.</span></span> <span data-ttu-id="fda95-149">Eksisterende produkter bliver ikke synkroniseret, før dette job er fuldført.</span><span class="sxs-lookup"><span data-stu-id="fda95-149">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="fda95-150">I Supply Chain Management skal du bruge funktionen Søg til at søge efter **Udfyld tabel for specifikt produkt**.</span><span class="sxs-lookup"><span data-stu-id="fda95-150">In Supply Chain Management, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="fda95-151">Vælg **Udfyld tabel for specifikt produkt** for at køre jobbet.</span><span class="sxs-lookup"><span data-stu-id="fda95-151">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="fda95-152">Dette job skal kun køres én gang.</span><span class="sxs-lookup"><span data-stu-id="fda95-152">This job must be run only one time.</span></span>

- <span data-ttu-id="fda95-153">Sørg for, at den krævede værditilknytning for salgsmåleenheden mellem Supply Chain Management og Sales findes i tilknytningen af **SalesUnitSymbol** til **DefaultUnit (Name)**.</span><span class="sxs-lookup"><span data-stu-id="fda95-153">Make sure that the required value map for the selling unit of measure (UOM) between Supply Chain Management and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="fda95-154">Opdater værditilknytningen for **Enhedsgruppe** (**defaultuomscheduleid.name**), så den svarer til **Enhedsgrupper** i Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-154">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="fda95-155">Standardskabelonværdien er **Standardenhed**.</span><span class="sxs-lookup"><span data-stu-id="fda95-155">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="fda95-156">Sørg for, at salgsmåleenhederne for alle produkter fra Supply Chain Management findes i Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-156">Make sure that the selling UOMs for all products from Supply Chain Management exist in Sales.</span></span>
- <span data-ttu-id="fda95-157">Sørg for, at der findes prislister i Sales for alle produktsalgsvalutaer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fda95-157">Make sure that price lists exist in Sales for every product sales currency in Supply Chain Management.</span></span>
- <span data-ttu-id="fda95-158">Når produkter oprettes i Sales, kan de have statussen **Kladde** eller **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="fda95-158">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="fda95-159">Denne funktion styres i **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales** i Sales.</span><span class="sxs-lookup"><span data-stu-id="fda95-159">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="fda95-160">Produkter, der har status **Kladde**, når de oprettes, skal aktiveres, før de kan føjes til tilbud eller salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="fda95-160">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="fda95-161">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="fda95-161">Template mapping in Data integration</span></span>

<span data-ttu-id="fda95-162">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="fda95-162">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="fda95-163">Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="fda95-163">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Skabelontilknytning i dataintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="fda95-165">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="fda95-165">Related topics</span></span>

[<span data-ttu-id="fda95-166">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="fda95-166">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="fda95-167">Synkronisere konti direkte fra Sales med kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fda95-167">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="fda95-168">Synkronisere kontakter direkte fra Sales med kontakter eller kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="fda95-168">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="fda95-169">Synkronisere salgshoveder og -linjer direkte fra Supply Chain Management til Sales</span><span class="sxs-lookup"><span data-stu-id="fda95-169">Synchronize sales order headers and lines directly from Supply Chain Management to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="fda95-170">Synkronisere salgsfakturahoveder og -linjer direkte fra Supply Chain Management til Sales</span><span class="sxs-lookup"><span data-stu-id="fda95-170">Synchronize sales invoice headers and lines directly from Supply Chain ManagementSupply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)



