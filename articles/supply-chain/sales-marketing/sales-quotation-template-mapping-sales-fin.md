---
title: Synkroniser hoveder og linjer i salgstilbud direkte fra Sales med Finance and Operations
description: I emnet beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 10/25/2018
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
ms.openlocfilehash: 0894f4728d3f1df21db130cd9e87d9881726e7fa
ms.sourcegitcommit: 45f8cea6ac75bd2f4187380546a201c056072c59
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/12/2019
ms.locfileid: "1743365"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="9777a-103">Synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9777a-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9777a-104">I emnet beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="9777a-105">Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="9777a-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="9777a-106">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="9777a-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="9777a-107">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="9777a-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="9777a-108">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data til firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="9777a-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="9777a-109">I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="9777a-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="9777a-110">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="9777a-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="9777a-111">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="9777a-111">Template and tasks</span></span>

<span data-ttu-id="9777a-112">Følgende skabelon og underliggende opgaver bruges til at synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="9777a-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="9777a-113">**Navnet på skabelonen i dataintegration:** Sales Quotes (Sales to Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="9777a-113">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="9777a-114">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="9777a-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="9777a-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9777a-115">QuoteHeader</span></span>
    - <span data-ttu-id="9777a-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9777a-116">QuoteLine</span></span>

<span data-ttu-id="9777a-117">Følgende synkroniseringsopgaver kræves, før salgstilbudshoveder og -linjer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="9777a-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="9777a-118">Produkter (Fin and Ops til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="9777a-118">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="9777a-119">Konti (Sales til Fin and Ops) - Direkte (hvis den bruges)</span><span class="sxs-lookup"><span data-stu-id="9777a-119">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="9777a-120">Kontakter til Debitorer (Sales til Fin and Ops) – Direkte (hvis det bruges)</span><span class="sxs-lookup"><span data-stu-id="9777a-120">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="9777a-121">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="9777a-121">Entity set</span></span>

| <span data-ttu-id="9777a-122">Salg</span><span class="sxs-lookup"><span data-stu-id="9777a-122">Sales</span></span>        | <span data-ttu-id="9777a-123">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9777a-123">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="9777a-124">Citater</span><span class="sxs-lookup"><span data-stu-id="9777a-124">Quotes</span></span>       | <span data-ttu-id="9777a-125">CDS-salgstilbudshoved</span><span class="sxs-lookup"><span data-stu-id="9777a-125">CDS sales quotation header</span></span> |
| <span data-ttu-id="9777a-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="9777a-126">QuoteDetails</span></span> | <span data-ttu-id="9777a-127">CDS-salgstilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="9777a-127">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="9777a-128">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="9777a-128">Entity flow</span></span>

<span data-ttu-id="9777a-129">Salgstilbud oprettes i Sales og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-129">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="9777a-130">Salgstilbud fra Sales synkroniseres kun, hvis følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="9777a-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="9777a-131">Alle tilbudsprodukter på salgstilbuddet vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="9777a-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="9777a-132">Når du klikker på **Aktivér tilbud**, bliver salgstilbuddet aktivt.</span><span class="sxs-lookup"><span data-stu-id="9777a-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="9777a-133">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="9777a-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="9777a-134">Feltet **Har kun eksternt vedligeholdte produkter** er føjet til objektet **Tilbud** for konsekvent at spore, om salgstilbuddet består udelukkende af eksternt vedligeholdte produkter.</span><span class="sxs-lookup"><span data-stu-id="9777a-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="9777a-135">Hvis et salgstilbud kun har eksternt vedligeholdte produkter, vedligeholdes produkterne i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-135">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="9777a-136">Denne funktionsmåde er med til at sikre, at du ikke forsøger at synkronisere salgstilbudslinjer, der har produkter, som er ukendte i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="9777a-137">Alle tilbudsprodukter på salgstilbuddet opdateres med **Har kun eksternt vedligeholdte produkter**-oplysningerne fra salgstilbudshovedet.</span><span class="sxs-lookup"><span data-stu-id="9777a-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="9777a-138">Disse oplysninger findes i feltet **Tilbuddet indeholder kun eksternt vedligeholdte produkter** i enheden **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="9777a-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="9777a-139">En rabat kan føjes til tilbudsproduktet og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-139">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="9777a-140">Felterne **Rabat**, **Gebyrer** og **Moms** i hovedet styres af en opsætning i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="9777a-141">Denne opsætning understøtter ikke aktuelt integrationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="9777a-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="9777a-142">I det aktuelle design vedligeholdes og håndteres felterne **Pris**, **Rabat**, **Gebyr** og **Moms** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="9777a-143">I Sales gør løsningen følgende felter skrivebeskyttet, fordi værdierne ikke synkroniseres for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="9777a-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="9777a-144">Skrivebeskyttede felter i salgstilbudshovedet: **Rabatprocent**, **Rabat** og **Fragtbeløb**</span><span class="sxs-lookup"><span data-stu-id="9777a-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="9777a-145">Skrivebeskyttede felter på tilbudsprodukter: **Moms**</span><span class="sxs-lookup"><span data-stu-id="9777a-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="9777a-146">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="9777a-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="9777a-147">Før salgstilbud synkroniseres, er det vigtigt, at du opdaterer følgende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="9777a-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="9777a-148">Konfiguration i Sales</span><span class="sxs-lookup"><span data-stu-id="9777a-148">Setup in Sales</span></span>

- <span data-ttu-id="9777a-149">Sørg for, at der er konfigureret tilladelser for det team, som brugeren fra din Sales-forbindelse er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="9777a-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="9777a-150">Hvis du bruger demodata, har brugeren normalt administratoradgang, men teamet har ikke administratoradgang.</span><span class="sxs-lookup"><span data-stu-id="9777a-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="9777a-151">Hvis teamet ikke også har administratoradgang, når du kører projektet fra dataintegration, får du vist en fejlmeddelelse om, at det primære team mangler.</span><span class="sxs-lookup"><span data-stu-id="9777a-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="9777a-152">Du kan angive tilladelser for teamet ved at gå til **Indstillinger** &gt; **Sikkerhed** &gt; **Team** og vælge det relevante team.</span><span class="sxs-lookup"><span data-stu-id="9777a-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="9777a-153">Vælg **Administrer roller**, og vælg derefter en rolle med de ønskede tilladelser, f.eks. **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="9777a-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="9777a-154">Gå til **Indstillinger** &gt; **Administration** &gt; **Systemindstillinger** &gt; **Sales**, og sørg for, at der bruges til følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="9777a-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="9777a-155">Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9777a-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="9777a-156">Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="9777a-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="9777a-157">Opsætning af dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="9777a-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="9777a-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9777a-158">QuoteHeader</span></span>

- <span data-ttu-id="9777a-159">Du skal sikre, at den nødvendige tilknytning findes for **Shipto\_land** til **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="9777a-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="9777a-160">I værditilknytningen kan du definere en standardværdi, der bruges, hvis værdien er tom.</span><span class="sxs-lookup"><span data-stu-id="9777a-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="9777a-161">Du skal blot lade den venstre side være tom, og indstille den højre side til det ønskede land eller område.</span><span class="sxs-lookup"><span data-stu-id="9777a-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="9777a-162">På denne måde behøver du ikke at skrive landet eller området for nationale ordrer.</span><span class="sxs-lookup"><span data-stu-id="9777a-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="9777a-163">Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet, og hvor en tom værdi svarer til værdien **DK**.</span><span class="sxs-lookup"><span data-stu-id="9777a-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="9777a-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9777a-164">QuoteLine</span></span>

- <span data-ttu-id="9777a-165">Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-165">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="9777a-166">Sørg for, at de krævede enheder er defineret i Sales.</span><span class="sxs-lookup"><span data-stu-id="9777a-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="9777a-167">En skabelonværdi, der har en værditilknytning, er defineret for **oumid.name** til **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="9777a-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="9777a-168">Valgfrit: Du kan tilføje følgende tilknytninger for at sikre, at salgstilbudslinjerne importeres til Finance and Operations, hvis der ikke er nogen standardoplysninger fra debitoren eller produktet:</span><span class="sxs-lookup"><span data-stu-id="9777a-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="9777a-169">**SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="9777a-170">Der er ingen standardskabelonværdi for **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="9777a-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="9777a-171">**WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="9777a-172">Der er ingen standardskabelonværdi for **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="9777a-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="9777a-173">Tilknytning af skabelon i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="9777a-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="9777a-174">Felterne **Rabat**, **Tillæg** og **Moms** styres af en kompleks opsætning i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="9777a-175">Denne opsætning understøtter ikke aktuelt integrationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="9777a-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="9777a-176">I det aktuelle design håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9777a-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="9777a-177">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="9777a-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="9777a-178">Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="9777a-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="9777a-179">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="9777a-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="9777a-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="9777a-180">QuoteHeader</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="9777a-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="9777a-182">QuoteLine</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="9777a-184">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="9777a-184">Related topics</span></span>

[<span data-ttu-id="9777a-185">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="9777a-185">Prospect to cash</span></span>](prospect-to-cash.md)

