---
title: Synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og -linjer direkte fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.
author: ChristianRytt
manager: tfehr
ms.date: 10/25/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.openlocfilehash: a1cf4072cb873ebbf4e0e46f16771458e436bcac
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5243099"
---
# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-supply-chain-management"></a><span data-ttu-id="b8fde-103">Synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b8fde-103">Synchronize sales quotation headers and lines directly from Sales to Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="b8fde-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og -linjer direkte fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

> [!NOTE]
> <span data-ttu-id="b8fde-105">Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="b8fde-105">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="b8fde-106">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="b8fde-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="b8fde-107">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="b8fde-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="b8fde-108">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data til firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="b8fde-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data for accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="b8fde-109">I følgende illustration vises, hvordan data synkroniseres mellem Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="b8fde-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="b8fde-110">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="b8fde-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="b8fde-111">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="b8fde-111">Template and tasks</span></span>

<span data-ttu-id="b8fde-112">Følgende skabelon og underliggende opgaver bruges til at synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="b8fde-112">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="b8fde-113">**Navnet på skabelonen i dataintegration:** Salgstilbud (Sales til Supply Chain Management) - Direkte</span><span class="sxs-lookup"><span data-stu-id="b8fde-113">**Name of the template in Data integration:** Sales Quotes (Sales to Supply Chain Management) - Direct</span></span>
- <span data-ttu-id="b8fde-114">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="b8fde-114">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="b8fde-115">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="b8fde-115">QuoteHeader</span></span>
    - <span data-ttu-id="b8fde-116">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="b8fde-116">QuoteLine</span></span>

<span data-ttu-id="b8fde-117">Følgende synkroniseringsopgaver kræves, før salgstilbudshoveder og -linjer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="b8fde-117">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="b8fde-118">Produkter (Supply Chain Management til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="b8fde-118">Products (Supply Chain Management to Sales) - Direct</span></span>
- <span data-ttu-id="b8fde-119">Konti (Sales til Supply Chain Management) - Direkte (hvis det er anvendt)</span><span class="sxs-lookup"><span data-stu-id="b8fde-119">Accounts (Sales to Supply Chain Management) - Direct (if used)</span></span>
- <span data-ttu-id="b8fde-120">Kontakter til kunder (Sales til Supply Chain Management) - Direkte (hvis det er anvendt)</span><span class="sxs-lookup"><span data-stu-id="b8fde-120">Contacts to Customers (Sales to Supply Chain Management) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="b8fde-121">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="b8fde-121">Entity set</span></span>

| <span data-ttu-id="b8fde-122">Sales</span><span class="sxs-lookup"><span data-stu-id="b8fde-122">Sales</span></span>        | <span data-ttu-id="b8fde-123">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b8fde-123">Supply Chain Management</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="b8fde-124">Citater</span><span class="sxs-lookup"><span data-stu-id="b8fde-124">Quotes</span></span>       | <span data-ttu-id="b8fde-125">Dataverse-salgstilbudshoved</span><span class="sxs-lookup"><span data-stu-id="b8fde-125">Dataverse sales quotation header</span></span> |
| <span data-ttu-id="b8fde-126">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="b8fde-126">QuoteDetails</span></span> | <span data-ttu-id="b8fde-127">Dataverse-salgstilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="b8fde-127">Dataverse sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="b8fde-128">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="b8fde-128">Entity flow</span></span>

<span data-ttu-id="b8fde-129">Salgstilbud oprettes i Sales og synkroniseres til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-129">Sales quotations are created in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="b8fde-130">Salgstilbud fra Sales synkroniseres kun, hvis følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="b8fde-130">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="b8fde-131">Alle tilbudsprodukter på salgstilbuddet vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="b8fde-131">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="b8fde-132">Når du klikker på **Aktivér tilbud**, bliver salgstilbuddet aktivt.</span><span class="sxs-lookup"><span data-stu-id="b8fde-132">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b8fde-133">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="b8fde-133">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b8fde-134">Feltet **Har kun eksternt vedligeholdte produkter** er føjet til objektet **Tilbud** for konsekvent at spore, om salgstilbuddet består udelukkende af eksternt vedligeholdte produkter.</span><span class="sxs-lookup"><span data-stu-id="b8fde-134">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="b8fde-135">Hvis et salgstilbud kun har eksternt vedligeholdte produkter, vedligeholdes produkterne i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-135">If a sales quotation has only externally maintained products, the products are maintained in Supply Chain Management.</span></span> <span data-ttu-id="b8fde-136">Denne funktionsmåde er med til at sikre, at du ikke forsøger at synkronisere salgstilbudslinjer, der har produkter, som er ukendte i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-136">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Supply Chain Management.</span></span>

<span data-ttu-id="b8fde-137">Alle tilbudsprodukter på salgstilbuddet opdateres med **Har kun eksternt vedligeholdte produkter**-oplysningerne fra salgstilbudshovedet.</span><span class="sxs-lookup"><span data-stu-id="b8fde-137">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="b8fde-138">Disse oplysninger findes i feltet **Tilbuddet indeholder kun eksternt vedligeholdte produkter** i enheden **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="b8fde-138">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="b8fde-139">En rabat kan føjes til tilbudsproduktet og synkroniseres til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-139">A discount can be added to the quote product and will be synchronized to Supply Chain Management.</span></span> <span data-ttu-id="b8fde-140">Felterne **Rabat**, **Gebyrer** og **Moms** i hovedet styres af en opsætning i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-140">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Supply Chain Management.</span></span> <span data-ttu-id="b8fde-141">Denne opsætning understøtter ikke aktuelt integrationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="b8fde-141">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="b8fde-142">I det aktuelle design vedligeholdes og håndteres felterne **Pris**, **Rabat**, **Gebyr** og **Moms** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-142">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in FSupply Chain Management.</span></span>

<span data-ttu-id="b8fde-143">I Sales gør løsningen følgende felter skrivebeskyttet, fordi værdierne ikke synkroniseres til Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="b8fde-143">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Supply Chain Management:</span></span>

- <span data-ttu-id="b8fde-144">Skrivebeskyttede felter i salgstilbudshovedet: **Rabatprocent**, **Rabat** og **Fragtbeløb**</span><span class="sxs-lookup"><span data-stu-id="b8fde-144">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="b8fde-145">Skrivebeskyttede felter på tilbudsprodukter: **Moms**</span><span class="sxs-lookup"><span data-stu-id="b8fde-145">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b8fde-146">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="b8fde-146">Preconditions and mapping setup</span></span>

<span data-ttu-id="b8fde-147">Før salgstilbud synkroniseres, er det vigtigt, at du opdaterer følgende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="b8fde-147">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="b8fde-148">Konfiguration i Sales</span><span class="sxs-lookup"><span data-stu-id="b8fde-148">Setup in Sales</span></span>

- <span data-ttu-id="b8fde-149">Sørg for, at der er konfigureret tilladelser for det team, som brugeren fra din Sales-forbindelse er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="b8fde-149">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="b8fde-150">Hvis du bruger demodata, har brugeren normalt administratoradgang, men teamet har ikke administratoradgang.</span><span class="sxs-lookup"><span data-stu-id="b8fde-150">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="b8fde-151">Hvis teamet ikke også har administratoradgang, når du kører projektet fra dataintegration, får du vist en fejlmeddelelse om, at det primære team mangler.</span><span class="sxs-lookup"><span data-stu-id="b8fde-151">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="b8fde-152">Du kan angive tilladelser for teamet ved at gå til **Indstillinger** &gt; **Sikkerhed** &gt; **Team** og vælge det relevante team.</span><span class="sxs-lookup"><span data-stu-id="b8fde-152">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="b8fde-153">Vælg **Administrer roller**, og vælg derefter en rolle med de ønskede tilladelser, f.eks. **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="b8fde-153">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="b8fde-154">Gå til **Indstillinger** &gt; **Administration** &gt; **Systemindstillinger** &gt; **Sales**, og sørg for, at der bruges til følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="b8fde-154">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="b8fde-155">Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b8fde-155">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="b8fde-156">Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="b8fde-156">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="b8fde-157">Opsætning af dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="b8fde-157">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="b8fde-158">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="b8fde-158">QuoteHeader</span></span>

- <span data-ttu-id="b8fde-159">Du skal sikre, at den nødvendige tilknytning findes for **Shipto\_land** til **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="b8fde-159">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="b8fde-160">I værditilknytningen kan du definere en standardværdi, der bruges, hvis værdien er tom.</span><span class="sxs-lookup"><span data-stu-id="b8fde-160">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="b8fde-161">Du skal blot lade den venstre side være tom, og indstille den højre side til det ønskede land eller område.</span><span class="sxs-lookup"><span data-stu-id="b8fde-161">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="b8fde-162">På denne måde behøver du ikke at skrive landet eller området for nationale ordrer.</span><span class="sxs-lookup"><span data-stu-id="b8fde-162">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="b8fde-163">Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet, og hvor en tom værdi svarer til værdien **DK**.</span><span class="sxs-lookup"><span data-stu-id="b8fde-163">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="b8fde-164">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="b8fde-164">QuoteLine</span></span>

- <span data-ttu-id="b8fde-165">Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-165">Make sure that the required value map exists for **SalesUnitSymbol** in Supply Chain Management.</span></span>
- <span data-ttu-id="b8fde-166">Sørg for, at de krævede enheder er defineret i Sales.</span><span class="sxs-lookup"><span data-stu-id="b8fde-166">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="b8fde-167">En skabelonværdi, der har en værditilknytning, er defineret for **oumid.name** til **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="b8fde-167">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="b8fde-168">Valgfrit: Du kan tilføje følgende tilknytninger for at sikre, at salgstilbudslinjerne importeres til Supply Chain Management, hvis der ikke er nogen standardoplysninger fra debitoren eller produktet:</span><span class="sxs-lookup"><span data-stu-id="b8fde-168">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Supply Chain Management if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="b8fde-169">**SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-169">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="b8fde-170">Der er ingen standardskabelonværdi for **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="b8fde-170">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="b8fde-171">**WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-171">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="b8fde-172">Der er ingen standardskabelonværdi for **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="b8fde-172">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="b8fde-173">Tilknytning af skabelon i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="b8fde-173">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="b8fde-174">Felterne **Rabat**, **Gebyrer** og **Moms** styres af en kompleks opsætning i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-174">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Supply Chain Management.</span></span> <span data-ttu-id="b8fde-175">Denne opsætning understøtter ikke aktuelt integrationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="b8fde-175">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="b8fde-176">I det aktuelle design håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="b8fde-176">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Supply Chain Management.</span></span>
> - <span data-ttu-id="b8fde-177">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="b8fde-177">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="b8fde-178">Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="b8fde-178">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="b8fde-179">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="b8fde-179">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="b8fde-180">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="b8fde-180">QuoteHeader</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="b8fde-182">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="b8fde-182">QuoteLine</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="b8fde-184">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="b8fde-184">Related topics</span></span>

[<span data-ttu-id="b8fde-185">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="b8fde-185">Prospect to cash</span></span>](prospect-to-cash.md)



[!INCLUDE[footer-include](../../includes/footer-banner.md)]