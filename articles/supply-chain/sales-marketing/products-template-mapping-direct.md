---
title: Synkronisere produkter direkte fra Finance and Operations med produkter i Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Sales.
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
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 821ba4f0957d8bb84fc188c86895700631b46fed
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-products-directly-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="5f1a1-103">Synkronisere produkter fra Finance and Operations direkte med produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="5f1a1-103">Synchronize products directly from Finance and Operations to products in Sales</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="5f1a1-104">Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="5f1a1-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="5f1a1-105">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter direkte fra Microsoft Dynamics 365 for Finance and Operations med Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-105">This topic discusses the templates and underlying tasks that are used to synchronize products directly from Microsoft Dynamics 365 for Finance and Operations, to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="5f1a1-106">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="5f1a1-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="5f1a1-107">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="5f1a1-108">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="5f1a1-109">I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="5f1a1-110">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="5f1a1-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="5f1a1-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="5f1a1-111">Templates and tasks</span></span>

<span data-ttu-id="5f1a1-112">For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="5f1a1-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="5f1a1-113">Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="5f1a1-114">Følgende skabeloner og underliggende opgaver bruges til at synkronisere produkter fra Finance and Operations til Sales:</span><span class="sxs-lookup"><span data-stu-id="5f1a1-114">The following template and underlying tasks are used to synchronize products from Finance and Operations to Sales.</span></span>

- <span data-ttu-id="5f1a1-115">**Navnet på skabelonen i dataintegration:** Produkter (Fin and Ops til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="5f1a1-115">**Name of the template in Data integration:** Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="5f1a1-116">**Navnet på opgaven i dataintegrationsprojektet:** Produkter</span><span class="sxs-lookup"><span data-stu-id="5f1a1-116">**Name of the task in the Data integration project:** Products</span></span>

<span data-ttu-id="5f1a1-117">Der kræves ingen synkroniseringsopgaver, før der kan forekomme synkronisering af produkt.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-117">No synchronization tasks are required before product synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="5f1a1-118">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="5f1a1-118">Entity set</span></span>

| <span data-ttu-id="5f1a1-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5f1a1-119">Finance and Operations</span></span>     | <span data-ttu-id="5f1a1-120">Salg</span><span class="sxs-lookup"><span data-stu-id="5f1a1-120">Sales</span></span>    |
|----------------------------|----------|
| <span data-ttu-id="5f1a1-121">Salgbare frigivne produkter</span><span class="sxs-lookup"><span data-stu-id="5f1a1-121">Sellable released products</span></span> | <span data-ttu-id="5f1a1-122">Produkter</span><span class="sxs-lookup"><span data-stu-id="5f1a1-122">Products</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5f1a1-123">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="5f1a1-123">Entity flow</span></span>

<span data-ttu-id="5f1a1-124">Produkter administreres i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-124">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="5f1a1-125">Dataenheden **Salgbare frigivne produkter** i Finance and Operations eksporterer kun produkter, der er *salgbare*.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-125">The **Sellable released products** data entity in Finance and Operations exports only products that are *sellable*.</span></span> <span data-ttu-id="5f1a1-126">Salgbare produkter er produkter med de oplysninger, de skal bruge for at kunne bruges på en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-126">Sellable products are products that have the information that they require in order to be used on a sales order.</span></span> <span data-ttu-id="5f1a1-127">De samme regler gælder, når et produkt valideres ved brug af funktionen **Valider** på siden **Frigivet produkt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-127">The same rules apply when a product is validated by using the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="5f1a1-128">Produktnummeret bruges som en nøgle.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-128">The product number is used as a key.</span></span> <span data-ttu-id="5f1a1-129">Når produktvarianter synkroniseres til Sales, har hver produktvariant derfor et individuelt produkt-id.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-129">Therefore, when product variants are synchronized to Sales, each product variant has an individual product ID.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5f1a1-130">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="5f1a1-130">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5f1a1-131">I Sales er tilføjet et nyt felt **Vedligeholdes eksternt** for produkterne, for at angive, at et bestemt produkt vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-131">In Sales, a new **Is Externally Maintained** field has been added on products to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="5f1a1-132">Som standard er værdien indstillet til **Ja** under import til Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-132">By default, the value is set to **Yes** during an import to Sales.</span></span> <span data-ttu-id="5f1a1-133">Følgende værdier er tilgængelige:</span><span class="sxs-lookup"><span data-stu-id="5f1a1-133">The following values are available:</span></span>

- <span data-ttu-id="5f1a1-134">**Ja** – Produktet stammer fra Finance and Operations, og kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-134">**Yes** – The product originated from Finance and Operations and won't be editable in Sales.</span></span>
- <span data-ttu-id="5f1a1-135">**Nej** – Produktet blev angivet direkte i Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-135">**No** – The product was entered directly in Sales.</span></span>
- <span data-ttu-id="5f1a1-136">**(Tom)** – Produktet fandtes i Sales, før kundeemne til kontanter-løsningen blev aktiveret.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-136">**(Blank)** – The product existed in Sales before the Prospect to cash solution was enabled.</span></span>

<span data-ttu-id="5f1a1-137">Feltet **Vedligeholdes eksternt** bruges til at sikre, at det kun er tilbud og salgsordrer med eksternt vedligeholdte produkter, der synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-137">The **Is Externally Maintained** field helps guarantee that only quotations and sales orders that have externally maintained products will be synchronized to Finance and Operations.</span></span>

<span data-ttu-id="5f1a1-138">Eksternt vedligeholdte produkter føjes automatisk til den første gyldige prisliste, der har den samme valuta.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-138">Externally maintained products are automatically added to the first valid price list that has the same currency.</span></span> <span data-ttu-id="5f1a1-139">Prislister organiseres alfabetisk efter navn.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-139">Price lists are organized alphabetically by name.</span></span> <span data-ttu-id="5f1a1-140">Produktets salgspris fra Finance and Operations bruges som prisen på prislisten.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-140">The product sales price from Finance and Operations is used as the price on the price list.</span></span> <span data-ttu-id="5f1a1-141">Derfor skal der være en prisliste i Sales for hver produktsalgsvaluta i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-141">Therefore, there must be a price list in Sales for every product sales currency in Finance and Operations.</span></span> <span data-ttu-id="5f1a1-142">Valutaen for de frigivne salgbare produkter indstilles til regnskabsvalutaen i den juridiske enhed, som produktet eksporteres fra.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-142">The currency on the released sellable products is set to the accounting currency in the legal entity that the product is exported from.</span></span>

> [!NOTE]
> <span data-ttu-id="5f1a1-143">Produktsynkronisering lykkes ikke, medmindre der er en prisliste, der har en tilsvarende valuta.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-143">Product synchronization won't succeed unless there is a price list that has a matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5f1a1-144">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="5f1a1-144">Preconditions and mapping setup</span></span>

- <span data-ttu-id="5f1a1-145">Inden du kører synkronisering for første gang, skal du udfylde tabellen Specifikt produkt for de eksisterende produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-145">Before you run the synchronization for the first time, you must fill the Distinct product table for existing products in Finance and Operations.</span></span> <span data-ttu-id="5f1a1-146">Eksisterende produkter bliver ikke synkroniseret, før dette job er fuldført.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-146">Existing products won't be synchronized until this job is completed.</span></span>

    1. <span data-ttu-id="5f1a1-147">I Finance and Operations skal du bruge funktionen Søg til at søge efter **Udfyld tabel for specifik produkt**.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-147">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>
    2. <span data-ttu-id="5f1a1-148">Vælg **Udfyld tabel for specifikt produkt** for at køre jobbet.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-148">Select **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="5f1a1-149">Dette job skal kun køres én gang.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-149">This job must be run only one time.</span></span>

- <span data-ttu-id="5f1a1-150">Sørg for, at den krævede værditilknytning for salgsmåleenheden (UOM) mellem Finance and Operations og Sales findes i tilknytningen for **SalesUnitSymbol** til **DefaultUnit (Name)**.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-150">Make sure that the required value map for the selling unit of measure (UOM) between Finance and Operations and Sales exists in the mapping of **SalesUnitSymbol** to **DefaultUnit (Name)**.</span></span>
- <span data-ttu-id="5f1a1-151">Opdater værditilknytningen for **Enhedsgruppe** (**defaultuomscheduleid.name**), så den svarer til **Enhedsgrupper** i Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-151">Update the value map for **Unit group** (**defaultuomscheduleid.name**) so that it matches **Unit groups** in Sales.</span></span>

    <span data-ttu-id="5f1a1-152">Standardskabelonværdien er **Standardenhed**.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-152">The default template value is **Default unit**.</span></span>

- <span data-ttu-id="5f1a1-153">Sørg for, at salgsmåleenhederne for alle produkter fra Finance and Operations findes i Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-153">Make sure that the selling UOMs for all products from Finance and Operations exist in Sales.</span></span>
- <span data-ttu-id="5f1a1-154">Sørg for, at der findes prislister i Sales for alle produktsalgsvalutaer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-154">Make sure that price lists exist in Sales for every product sales currency in Finance and Operations.</span></span>
- <span data-ttu-id="5f1a1-155">Når produkter oprettes i Sales, kan de have statussen **Kladde** eller **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-155">When products are created in Sales, they can have a status of **Draft** or **Active**.</span></span> <span data-ttu-id="5f1a1-156">Denne funktion styres i **Indstillinger** > **Administration** > **Systemindstillinger** > **Sales** i Sales.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-156">The behavior is controlled at **Settings** > **Administration** > **System settings** > **Sales** in Sales.</span></span>

    <span data-ttu-id="5f1a1-157">Produkter, der har status **Kladde**, når de oprettes, skal aktiveres, før de kan føjes til tilbud eller salgsordrer.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-157">Products that have **Draft** status when they are created must be activated before they can be added to quotations or sales orders.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="5f1a1-158">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="5f1a1-158">Template mapping in Data integration</span></span>

<span data-ttu-id="5f1a1-159">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-159">The following illustration shows an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="5f1a1-160">Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5f1a1-160">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Skabelontilknytning i dataintegrator](./media/products-direct-template-mapping-data-integrator-1.png)


## <a name="related-topics"></a><span data-ttu-id="5f1a1-162">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="5f1a1-162">Related topics</span></span>

[<span data-ttu-id="5f1a1-163">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="5f1a1-163">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="5f1a1-164">Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5f1a1-164">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="5f1a1-165">Synkronisere kontakter direkte fra Sales med kontakter eller debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5f1a1-165">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="5f1a1-166">Synkronisere salgsordrehoveder og linjer fra Finance and Operations direkte med Sales</span><span class="sxs-lookup"><span data-stu-id="5f1a1-166">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="5f1a1-167">Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="5f1a1-167">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)




