---
title: Synkronisere produkter fra Finance and Operations til produkter i Sales
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations Enterprise edition til Microsoft Dynamics 365 for Sales.
author: ChristianRytt
manager: AnnBe
ms.date: 07/03/2017
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
ms.author: ChristianRytt
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 08c38aada355583c5a6872f75b57db95d9b81786
ms.openlocfilehash: 2f14b06b57930256f9211f2085512aa589df083e
ms.contentlocale: da-dk
ms.lasthandoff: 07/27/2017

---

# <a name="synchronize-products-from-finance-and-operations-to-products-in-sales"></a><span data-ttu-id="0f95d-103">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="0f95d-103">Synchronize products from Finance and Operations to products in Sales</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="0f95d-104">Før du kan bruge kundeemnet til kontantløsning, skal du have kendskab til [Dynamics 365-dataintegration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="0f95d-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](https://docs.microsoft.com/en-us/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="0f95d-105">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations Enterprise edition til Microsoft Dynamics 365 for Sales.</span><span class="sxs-lookup"><span data-stu-id="0f95d-105">This topic discusses the templates and underlying tasks that are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition to Microsoft Dynamics 365 for Sales.</span></span>

## <a name="template-and-task"></a><span data-ttu-id="0f95d-106">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="0f95d-106">Template and task</span></span>

<span data-ttu-id="0f95d-107">Følgende skabeloner og underliggende opgaver bruges til at synkronisere produkter fra Microsoft Dynamics 365 for Finance and Operations Enterprise edition (Finance and Operations) til Microsoft Dynamics 365 for Sales (Sales).</span><span class="sxs-lookup"><span data-stu-id="0f95d-107">The following templates and underlying tasks are used to synchronize products from Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations) to Microsoft Dynamics 365 for Sales (Sales).</span></span>

-   <span data-ttu-id="0f95d-108">Navnet på skabelonen: Produkter (Finance and Operations til Sales)</span><span class="sxs-lookup"><span data-stu-id="0f95d-108">Name of template: Products (Fin and Ops to Sales)</span></span>

-   <span data-ttu-id="0f95d-109">Navnet på opgaven i projektet: Produkter</span><span class="sxs-lookup"><span data-stu-id="0f95d-109">Name of task in project: Products</span></span>

<span data-ttu-id="0f95d-110">Synkroniseringsopgaver, der kræves før produktsynkronisering: Ingen</span><span class="sxs-lookup"><span data-stu-id="0f95d-110">Sync tasks required prior to Product sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="0f95d-111">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="0f95d-111">Entity set</span></span>

| <span data-ttu-id="0f95d-112">**Finance and Operations**</span><span class="sxs-lookup"><span data-stu-id="0f95d-112">**Finance and Operations**</span></span> | <span data-ttu-id="0f95d-113">**CDS**</span><span class="sxs-lookup"><span data-stu-id="0f95d-113">**CDS**</span></span> | <span data-ttu-id="0f95d-114">**Sales**</span><span class="sxs-lookup"><span data-stu-id="0f95d-114">**Sales**</span></span>  |
|----------------------------|---------|------------|
| <span data-ttu-id="0f95d-115">Salgbare frigivne produkter</span><span class="sxs-lookup"><span data-stu-id="0f95d-115">Sellable released products</span></span> | <span data-ttu-id="0f95d-116">Produkt</span><span class="sxs-lookup"><span data-stu-id="0f95d-116">Product</span></span> | <span data-ttu-id="0f95d-117">Produkter</span><span class="sxs-lookup"><span data-stu-id="0f95d-117">Products</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="0f95d-118">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="0f95d-118">Entity flow</span></span>

<span data-ttu-id="0f95d-119">Produkter administreres i Finance and Operations og synkroniseres til Sales.</span><span class="sxs-lookup"><span data-stu-id="0f95d-119">Products are managed in Finance and Operations and synchronized to Sales.</span></span> <span data-ttu-id="0f95d-120">Dataenheden **Salgbare frigivne produkter** i Finance and Operations eksporterer kun produkter, der er salgbare, hvilket betyder, at produkter de oplysninger, der skal bruges i en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="0f95d-120">The data entity **Sellable released products** in Finance and Operations only exports products that are sellable, which means that products have the information required to be used on a sales order.</span></span> <span data-ttu-id="0f95d-121">De samme regler gælder, når et produkt valideres med funktionen **Valider** på siden **Frigivet produkt**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-121">The same rules apply when a product is validated with the **Validate** function on the **Released product** page.</span></span>

<span data-ttu-id="0f95d-122">**Produktnummer** bruges som nøgle, hvilket betyder, at produktvarianter synkroniseres til CDS og Sales med individuelle **Produkt-id'er** pr. **Produktvariant**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-122">The **Product number** is used as key, meaning that product variants are synchronized to CDS and Sales with individual **Product IDs** per **Product variant**.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="0f95d-123">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="0f95d-123">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="0f95d-124">I Sales tilføjes et nyt felt for produkterne, **Vedligeholdes eksternt**, for at angive, at et bestemt produkt vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="0f95d-124">In Sales, a new field on the products **Is Externally Maintained** is added to indicate that a given product is maintained externally.</span></span> <span data-ttu-id="0f95d-125">Værdien er indstillet til **Ja** som standard under import til Sales.</span><span class="sxs-lookup"><span data-stu-id="0f95d-125">The value is set to **Yes** by default during import to Sales.</span></span>

-   <span data-ttu-id="0f95d-126">**Vedligeholdes eksternt = Ja**: Produktet stammer fra Finance and Operations og kan ikke redigeres i Sales.</span><span class="sxs-lookup"><span data-stu-id="0f95d-126">**Is Externally Maintained = Yes**: Product originates from Finance and Operations and will not be editable in Sales.</span></span>

-   <span data-ttu-id="0f95d-127">**Vedligeholdes eksternt = Nej**: Produkt angives direkte i Sales.</span><span class="sxs-lookup"><span data-stu-id="0f95d-127">**Is Externally Maintained = No**: Product is entered directly in Sales.</span></span>

-   <span data-ttu-id="0f95d-128">**Vedligeholdes eksternt = Tom**: Produktet findes i Sales før aktivering af løsningen Kundeemne-til-kontant.</span><span class="sxs-lookup"><span data-stu-id="0f95d-128">**Is Externally Maintained = Blank**: Product exists in Sales prior to enabling the Prospect to cash solution.</span></span>

<span data-ttu-id="0f95d-129">Oplysningerne i **Vedligeholdes eksternt** bruges til at sikre, at det kun er **Tilbud** og **Salgsordrer** med **eksternt vedligeholdte produkter** der synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f95d-129">The **Is Externally Maintained** information is used to ensure that only **Quotes** and **Sales orders** with **Externally maintained products** will sync to Finance and Operations.</span></span>

<span data-ttu-id="0f95d-130">**Eksternt vedligeholdte produkter** føjes automatisk til den første gyldige **Prisliste** med den samme valuta.</span><span class="sxs-lookup"><span data-stu-id="0f95d-130">**Externally maintained products** are automatically added to the first valid **Price list** with the same currency.</span></span> <span data-ttu-id="0f95d-131">Bemærk, at listen er organiseret alfabetisk efter **Navn**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-131">Note that the list is organized alphabetically by **Name**.</span></span> <span data-ttu-id="0f95d-132">Produktets salgspris fra Finance and Operations bruges som pris på **Prisliste**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-132">The product sales price from Finance and Operations is used as price on the **Price list**.</span></span> <span data-ttu-id="0f95d-133">Det betyder, at det er nødvendigt at have en **prisliste** i Sales for hver **Produktsalgsvaluta** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f95d-133">This means that it is required to have a **Price list** in Sales for each **Product sales currency** in Finance and Operations.</span></span> <span data-ttu-id="0f95d-134">Valutaen for de endelige salgbare produkter indstilles til regnskabsvalutaen i den juridiske enhed, som produktet eksporteres fra.</span><span class="sxs-lookup"><span data-stu-id="0f95d-134">Currency on the released sellable products is set to the accounting currency in the legal entity, from which the product is exported.</span></span>

> [!NOTE]
> <span data-ttu-id="0f95d-135">Produktsynkroniseringen mislykkes uden en **prisliste** med den tilsvarende valuta.</span><span class="sxs-lookup"><span data-stu-id="0f95d-135">Product sync will not succeed without a **Price list** with the matching currency.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="0f95d-136">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="0f95d-136">Preconditions and mapping setup</span></span>

-   <span data-ttu-id="0f95d-137">Inden du kører den allerførste synkronisering, skal du udfylde de **Tabel for specifik produkt** for eksisterende produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f95d-137">Before you run the very first sync, you must populate the **Distinct product table** for existing products in Finance and Operations.</span></span> <span data-ttu-id="0f95d-138">Eksisterende produkter bliver ikke synkroniseret, før dette job er fuldført.</span><span class="sxs-lookup"><span data-stu-id="0f95d-138">Existing products will not be synchronized until this job is completed.</span></span>

    -   <span data-ttu-id="0f95d-139">I Finance and Operations skal du bruge funktionen Søg til at søge efter **Udfyld tabel for specifik produkt**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-139">In Finance and Operations, use Search to search for **Populate distinct product table**.</span></span>

    -   <span data-ttu-id="0f95d-140">Klik på **Udfyld tabel for specifik produkt** for at køre jobbet.</span><span class="sxs-lookup"><span data-stu-id="0f95d-140">Click the **Populate distinct product table** to run the job.</span></span> <span data-ttu-id="0f95d-141">Dette job skal kun køres én gang.</span><span class="sxs-lookup"><span data-stu-id="0f95d-141">This job only needs to be run once.</span></span>

-   <span data-ttu-id="0f95d-142">Kontroller, at den påkrævede **ValueMap** for salg af **Måleenhed** (UOM) i Finance and Operations findes i **Kilde -\> CDS-tilknytning af SalesUnitSymbol/DefaultSellingUnitOfMeasure**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-142">Ensure that the needed **ValueMap** for selling **Unit of measure** (UOM) in Finance and Operations exists in the **Source -\> CDS mapping SalesUnitSymbol / DefaultSellingUnitOfMeasure**.</span></span>

-   <span data-ttu-id="0f95d-143">Kontroller, at **Understøttede decimaler** for måleenheden opfylder dit behov i **CDS -\> Destination**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-143">Ensure that **Decimals supported** for UOM match your requirements in **CDS -\> Destination**.</span></span> <span data-ttu-id="0f95d-144">Hvis du har brug for forskellige værdier pr. måleenhed, kan dette gøres med **ValueMap** fra Enhed, f.eks. [Hver: 0] & [Pund: 2].</span><span class="sxs-lookup"><span data-stu-id="0f95d-144">If you require different values per UOM, this can be done with **ValueMap** from Unit, for example, [Each : 0] & [Pound : 2].</span></span>

    -   <span data-ttu-id="0f95d-145">Standardskabelonværdien 0 anvendes.</span><span class="sxs-lookup"><span data-stu-id="0f95d-145">Template value is defaulted to 0.</span></span>

-   <span data-ttu-id="0f95d-146">Opdater **CDS-organisations-id Organization_OrganizationId** i **Kilde -\> CDS**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-146">Update the **CDS Organization ID Organization_OrganizationId** in **Source -\> CDS**.</span></span>

    -   <span data-ttu-id="0f95d-147">Standardskabelonværdien ORG001 anvendes.</span><span class="sxs-lookup"><span data-stu-id="0f95d-147">Template value is defaulted to ORG001.</span></span>

-   <span data-ttu-id="0f95d-148">Opdater **ValueMap** for **Enhedsgruppe** (**defaultuomscheduleid.name**) i **CDS -\> Destination**, s den stemmer overens med **Enhedsgrupper** i Sales.</span><span class="sxs-lookup"><span data-stu-id="0f95d-148">Update **ValueMap** for **Unit group** (**defaultuomscheduleid.name**) in **CDS -\> Destination** to match the **Unit groups** in Sales.</span></span>

    -   <span data-ttu-id="0f95d-149">Standardskabelonværdien for **Standardenhed** anvendes.</span><span class="sxs-lookup"><span data-stu-id="0f95d-149">Template value is defaulted to **Default unit**.</span></span>

-   <span data-ttu-id="0f95d-150">Kontroller, at alle produkter, der sælger måleenheder fra Finance and Operations, findes i Sales med værdien **CDS-pluklister**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-150">Ensure that all products selling UOMs from Finance and Operations exist in Sales with the **CDS picklists** value.</span></span>

-   <span data-ttu-id="0f95d-151">Kontroller, at **Prislister** findes i Sales for hvert produktsalgsvaluta i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="0f95d-151">Ensure that **Price lists** exist in Sales for each product sales currency in Finance and Operations.</span></span>

-   <span data-ttu-id="0f95d-152">Du kan oprette produkter i Sales med status **Kladde** eller **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-152">Products can be created in Sales with status **Draft** or **Active**.</span></span> <span data-ttu-id="0f95d-153">Dette styres i **Systemindstillinger** under **Salg** i Sales.</span><span class="sxs-lookup"><span data-stu-id="0f95d-153">This is controlled in **System settings** under **Sales** in Sales.</span></span>

    -   <span data-ttu-id="0f95d-154">Produkter, der er oprettet med kladdestatus, skal aktiveres, før de kan føjes til **Tilbud** eller **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="0f95d-154">Products created with draft status need to be activated before they can be added to **Quote** or **Sales order**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="0f95d-155">Tilknytning af skabelon i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="0f95d-155">Template mapping in data integrator</span></span>

<span data-ttu-id="0f95d-156">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="0f95d-156">The following illustrations show an example of a template mapping in data integrator.</span></span>

![tilknytning af skabelon i dataintegrator](./media/products-template-mapping-data-integrator-1.png)

![tilknytning af skabelon for produkter i dataintegrator](./media/products-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="0f95d-159">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="0f95d-159">Related topics</span></span>

[<span data-ttu-id="0f95d-160">Synkronisere konti fra Sales med kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f95d-160">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="0f95d-161">Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f95d-161">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="0f95d-162">Synkronisere salgstilbudshoveder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="0f95d-162">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)


