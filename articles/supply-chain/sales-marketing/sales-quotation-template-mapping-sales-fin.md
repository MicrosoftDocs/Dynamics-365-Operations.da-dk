---
title: Synkroniser hoveder og linjer i salgstilbud direkte fra Sales med Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 11/14/2017
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
ms.openlocfilehash: d61e85a80cda06570e17276b9aa35255540626d0
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-directly-from-sales-to-finance-and-operations"></a><span data-ttu-id="b89ab-103">Synkroniser hoveder og linjer i salgstilbud direkte fra Sales med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b89ab-103">Synchronize sales quotation headers and lines directly from Sales to Finance and Operations</span></span>

[!INCLUDE [banner](../includes/banner.md)]

<span data-ttu-id="b89ab-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgsfakturahoveder og -linjer direkte fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-104">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

> [!NOTE]
> <span data-ttu-id="b89ab-105">Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="b89ab-105">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

## <a name="template-and-tasks"></a><span data-ttu-id="b89ab-106">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="b89ab-106">Template and tasks</span></span>

<span data-ttu-id="b89ab-107">Følgende skabelon og underliggende opgaver bruges til at synkronisere salgstilbudshoveder og -linjer direkte fra Sales til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b89ab-107">The following template and underlying tasks are used to synchronize sales quotation headers and lines directly from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="b89ab-108">**Navnet på skabelonen i dataintegration:** Sales Quotes (Sales to Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="b89ab-108">**Name of the template in Data integration:** Sales Quotes (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="b89ab-109">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="b89ab-109">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="b89ab-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="b89ab-110">QuoteHeader</span></span>
    - <span data-ttu-id="b89ab-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="b89ab-111">QuoteLine</span></span>

<span data-ttu-id="b89ab-112">Følgende synkroniseringsopgaver kræves, før salgstilbudshoveder og -linjer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="b89ab-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="b89ab-113">Produkter (Fin and Ops til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="b89ab-113">Products (Fin and Ops to Sales) - Direct</span></span>
- <span data-ttu-id="b89ab-114">Konti (Sales til Fin and Ops) - Direkte (hvis den bruges)</span><span class="sxs-lookup"><span data-stu-id="b89ab-114">Accounts (Sales to Fin and Ops) - Direct (if used)</span></span>
- <span data-ttu-id="b89ab-115">Kontakter til Debitorer (Sales til Fin and Ops) – Direkte (hvis det bruges)</span><span class="sxs-lookup"><span data-stu-id="b89ab-115">Contacts to Customers (Sales to Fin and Ops) - Direct (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="b89ab-116">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="b89ab-116">Entity set</span></span>

| <span data-ttu-id="b89ab-117">Salg</span><span class="sxs-lookup"><span data-stu-id="b89ab-117">Sales</span></span>        | <span data-ttu-id="b89ab-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="b89ab-118">Finance and Operations</span></span>     |
|--------------|----------------------------|
| <span data-ttu-id="b89ab-119">Citater</span><span class="sxs-lookup"><span data-stu-id="b89ab-119">Quotes</span></span>       | <span data-ttu-id="b89ab-120">CDS-salgstilbudshoved</span><span class="sxs-lookup"><span data-stu-id="b89ab-120">CDS sales quotation header</span></span> |
| <span data-ttu-id="b89ab-121">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="b89ab-121">QuoteDetails</span></span> | <span data-ttu-id="b89ab-122">CDS-salgstilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="b89ab-122">CDS sales quotation lines</span></span>  |

## <a name="entity-flow"></a><span data-ttu-id="b89ab-123">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="b89ab-123">Entity flow</span></span>

<span data-ttu-id="b89ab-124">Salgstilbud oprettes i Sales og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-124">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="b89ab-125">Salgstilbud fra Sales synkroniseres kun, hvis følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="b89ab-125">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="b89ab-126">Alle tilbudsprodukter på salgstilbuddet vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="b89ab-126">All quote products on the sales quotation are externally maintained.</span></span>
- <span data-ttu-id="b89ab-127">Når du klikker på **Aktivér tilbud**, bliver salgstilbuddet aktivt.</span><span class="sxs-lookup"><span data-stu-id="b89ab-127">After you click **Activate quote**, the sales quotation is active.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="b89ab-128">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="b89ab-128">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="b89ab-129">Feltet **Har kun eksternt vedligeholdte produkter** er føjet til objektet **Tilbud** for konsekvent at spore, om salgstilbuddet består udelukkende af eksternt vedligeholdte produkter.</span><span class="sxs-lookup"><span data-stu-id="b89ab-129">The **Has Externally Maintained Products Only** field has been added to the **Quote** entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="b89ab-130">Hvis et salgstilbud kun har eksternt vedligeholdte produkter, vedligeholdes produkterne i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-130">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="b89ab-131">Denne funktionsmåde er med til at sikre, at du ikke forsøger at synkronisere salgstilbudslinjer, der har produkter, som er ukendte i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-131">This behavior helps guarantee that you don't try to synchronize sales quotation lines that have products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="b89ab-132">Alle tilbudsprodukter på salgstilbuddet opdateres med **Har kun eksternt vedligeholdte produkter**-oplysningerne fra salgstilbudshovedet.</span><span class="sxs-lookup"><span data-stu-id="b89ab-132">All quote products on the sales quotation are updated with the **Has Externally Maintained Products Only** information from the sales quotation header.</span></span> <span data-ttu-id="b89ab-133">Disse oplysninger findes i feltet **Tilbuddet indeholder kun eksternt vedligeholdte produkter** i enheden **QuoteDetails**.</span><span class="sxs-lookup"><span data-stu-id="b89ab-133">This information is found in the **Quote Has Externally Maintained Products Only** field on the **QuoteDetails** entity.</span></span>

<span data-ttu-id="b89ab-134">En rabat kan føjes til tilbudsproduktet og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-134">A discount can be added to the quote product and will be synchronized to Finance and Operations.</span></span> <span data-ttu-id="b89ab-135">Felterne **Rabat**, **Gebyrer** og **Moms** i hovedet styres af en opsætning i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-135">The **Discount**, **Charges**, and **Tax** fields on the header are controlled by a setup in Finance and Operations.</span></span> <span data-ttu-id="b89ab-136">Denne opsætning understøtter ikke aktuelt integrationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="b89ab-136">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="b89ab-137">I det aktuelle design vedligeholdes og håndteres felterne **Pris**, **Rabat**, **Gebyr** og **Moms** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-137">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are maintained and handled in Finance and Operations.</span></span>

<span data-ttu-id="b89ab-138">I Sales gør løsningen følgende felter skrivebeskyttet, fordi værdierne ikke synkroniseres for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="b89ab-138">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="b89ab-139">Skrivebeskyttede felter i salgstilbudshovedet: **Rabatprocent**, **Rabat** og **Fragtbeløb**</span><span class="sxs-lookup"><span data-stu-id="b89ab-139">Read-only fields on the sales quotation header: **Discount %**, **Discount**, and **Freight Amount**</span></span>
- <span data-ttu-id="b89ab-140">Skrivebeskyttede felter på tilbudsprodukter: **Moms**</span><span class="sxs-lookup"><span data-stu-id="b89ab-140">Read-only fields on quote products: **Tax**</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="b89ab-141">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="b89ab-141">Preconditions and mapping setup</span></span>

<span data-ttu-id="b89ab-142">Før salgstilbud synkroniseres, er det vigtigt, at du opdaterer følgende indstillinger.</span><span class="sxs-lookup"><span data-stu-id="b89ab-142">Before sales quotations are synchronized, it's important that you update the following settings.</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="b89ab-143">Konfiguration i Sales</span><span class="sxs-lookup"><span data-stu-id="b89ab-143">Setup in Sales</span></span>

- <span data-ttu-id="b89ab-144">Sørg for, at der er konfigureret tilladelser for det team, som brugeren fra din Sales-forbindelse er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="b89ab-144">Make sure that permissions are set up for the team that the user from your connection set in Sales is assigned to.</span></span> <span data-ttu-id="b89ab-145">Hvis du bruger demodata, har brugeren normalt administratoradgang, men teamet har ikke administratoradgang.</span><span class="sxs-lookup"><span data-stu-id="b89ab-145">If you're using demo data, the user usually has admin access, but the team doesn't have admin access.</span></span> <span data-ttu-id="b89ab-146">Hvis teamet ikke også har administratoradgang, når du kører projektet fra dataintegration, får du vist en fejlmeddelelse om, at det primære team mangler.</span><span class="sxs-lookup"><span data-stu-id="b89ab-146">If the team doesn't have admin access when you run the project from Data integration, you will receive an error message that states that the Principal team is missing.</span></span>

    <span data-ttu-id="b89ab-147">Du kan angive tilladelser for teamet ved at gå til **Indstillinger** &gt; **Sikkerhed** &gt; **Team** og vælge det relevante team.</span><span class="sxs-lookup"><span data-stu-id="b89ab-147">To set up permissions for the team, go to **Settings** &gt; **Security** &gt; **Teams**, and select the relevant team.</span></span> <span data-ttu-id="b89ab-148">Vælg **Administrer roller**, og vælg derefter en rolle med de ønskede tilladelser, f.eks. **Systemadministrator**.</span><span class="sxs-lookup"><span data-stu-id="b89ab-148">Select **Manage Roles**, and then select a role that has the desired permissions, such as **System Administrator**.</span></span>

- <span data-ttu-id="b89ab-149">Gå til **Indstillinger** &gt; **Administration** &gt; **Systemindstillinger** &gt; **Sales**, og sørg for, at der bruges til følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="b89ab-149">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the following settings are used:</span></span>

    - <span data-ttu-id="b89ab-150">Indstillingen **Brug systemets prisberegningssystem** er angivet til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="b89ab-150">The **Use system prizing calculation system** option is set to **Yes**.</span></span>
    - <span data-ttu-id="b89ab-151">Feltet **Rabatberegningsmetode** er angivet til **Linjeelement**.</span><span class="sxs-lookup"><span data-stu-id="b89ab-151">The **Discount calculation method** field is set to **Line item**.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="b89ab-152">Opsætning af dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="b89ab-152">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="b89ab-153">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="b89ab-153">QuoteHeader</span></span>

- <span data-ttu-id="b89ab-154">Du skal sikre, at den nødvendige tilknytning findes for **Shipto\_land** til **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="b89ab-154">Make sure that the required mapping exists for **Shipto\_country** to **DeliveryAddressCountryRegionISOCode**.</span></span> <span data-ttu-id="b89ab-155">I værditilknytningen kan du definere en standardværdi, der bruges, hvis værdien er tom.</span><span class="sxs-lookup"><span data-stu-id="b89ab-155">In the value map, you can define a default value that is used if the value is left blank.</span></span> <span data-ttu-id="b89ab-156">Du skal blot lade den venstre side være tom, og indstille den højre side til det ønskede land eller område.</span><span class="sxs-lookup"><span data-stu-id="b89ab-156">Just leave the left side blank, and set the right side to the desired country or region.</span></span> <span data-ttu-id="b89ab-157">På denne måde behøver du ikke at skrive landet eller området for nationale ordrer.</span><span class="sxs-lookup"><span data-stu-id="b89ab-157">In this way, you don't have to type the country or region for national orders.</span></span>

    <span data-ttu-id="b89ab-158">Skabelonværdien er en værditilknytning, hvor flere lande eller områder er tilknyttet, og hvor en tom værdi svarer til værdien **DK**.</span><span class="sxs-lookup"><span data-stu-id="b89ab-158">The template value is a value map where several countries or regions are mapped, and where a blank value equals a value of **US**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="b89ab-159">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="b89ab-159">QuoteLine</span></span>

- <span data-ttu-id="b89ab-160">Sørg for, at den påkrævede værditilknytning findes for **SalesUnitSymbol** i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-160">Make sure that the required value map exists for **SalesUnitSymbol** in Finance and Operations.</span></span>
- <span data-ttu-id="b89ab-161">Sørg for, at de krævede enheder er defineret i Sales.</span><span class="sxs-lookup"><span data-stu-id="b89ab-161">Make sure that the required units are defined in Sales.</span></span>

    <span data-ttu-id="b89ab-162">En skabelonværdi, der har en værditilknytning, er defineret for **oumid.name** til **SalesUnitSymbol**.</span><span class="sxs-lookup"><span data-stu-id="b89ab-162">A template value that has a value map is defined for **oumid.name** to **SalesUnitSymbol**.</span></span>

- <span data-ttu-id="b89ab-163">Valgfrit: Du kan tilføje følgende tilknytninger for at sikre, at salgstilbudslinjerne importeres til Finance and Operations, hvis der ikke er nogen standardoplysninger fra debitoren eller produktet:</span><span class="sxs-lookup"><span data-stu-id="b89ab-163">Optional: You can add the following mappings to help guarantee that sales quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="b89ab-164">**SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-164">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="b89ab-165">Der er ingen standardskabelonværdi for **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="b89ab-165">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="b89ab-166">**WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-166">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="b89ab-167">Der er ingen standardskabelonværdi for **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="b89ab-167">There is no default template value for **WarehouseId**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="b89ab-168">Tilknytning af skabelon i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="b89ab-168">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="b89ab-169">Felterne **Rabat**, **Tillæg** og **Moms** styres af en kompleks opsætning i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-169">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="b89ab-170">Denne opsætning understøtter ikke aktuelt integrationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="b89ab-170">Currently, this setup doesn't support integration mapping.</span></span> <span data-ttu-id="b89ab-171">I det aktuelle design håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="b89ab-171">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="b89ab-172">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="b89ab-172">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="b89ab-173">Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="b89ab-173">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="b89ab-174">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="b89ab-174">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="b89ab-175">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="b89ab-175">QuoteHeader</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-1.png)

### <a name="quoteline"></a><span data-ttu-id="b89ab-177">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="b89ab-177">QuoteLine</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-direct-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="b89ab-179">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="b89ab-179">Related topics</span></span>

[<span data-ttu-id="b89ab-180">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="b89ab-180">Prospect to cash</span></span>](prospect-to-cash.md)


