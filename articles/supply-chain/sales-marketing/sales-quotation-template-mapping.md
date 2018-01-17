---
title: Synkronisere salgstilbudshoveder og -linjer fra Sales til Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og -linjer fra Microsoft Dynamics 365 for Sales til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
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
ms.search.scope: Core, Operations
ms.custom: 
ms.assetid: 
ms.search.region: global
ms.search.industry: 
ms.author: crytt
ms.dyn365.ops.version: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 029511634e56aec7fdd91bad9441cd12951fbd8d
ms.openlocfilehash: d34c808bce5b61b528f50224e3a72590476d8e55
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-sales-quotation-headers-and-lines-from-sales-to-finance-and-operations"></a><span data-ttu-id="5596b-103">Synkronisere salgstilbudshoveder og -linjer fra Sales til Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5596b-103">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="5596b-104">Før du kan bruge kundeemnet til kontantløsning, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="5596b-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="5596b-105">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere salgstilbudshoveder og -linjer fra Microsoft Dynamics 365 for Sales (Sales) til Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="5596b-105">The topic discusses the templates and underlying tasks that are used to synchronize sales quotation headers and lines from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span> 

## <a name="template-and-tasks"></a><span data-ttu-id="5596b-106">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="5596b-106">Template and tasks</span></span>

<span data-ttu-id="5596b-107">Følgende skabeloner og underliggende opgaver bruges til at synkronisere salgstilbudshoveder og -linjer fra Sales til Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="5596b-107">The following templates and underlying tasks are used to synchronize sales quotation headers and lines from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="5596b-108">**Navnet på skabelonen:** Salgstilbud (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="5596b-108">**Name of the template:** Sales Quotes (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="5596b-109">**Navnene på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="5596b-109">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="5596b-110">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="5596b-110">QuoteHeader</span></span>
    - <span data-ttu-id="5596b-111">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="5596b-111">QuoteLine</span></span>

<span data-ttu-id="5596b-112">Følgende synkroniseringsopgaver kræves, før salgstilbudshoveder og -linjer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="5596b-112">The following synchronization tasks are required before synchronization of sales quotation headers and lines can occur:</span></span>

- <span data-ttu-id="5596b-113">Produkter (Fin og Ops til Sales)</span><span class="sxs-lookup"><span data-stu-id="5596b-113">Products (Fin and Ops to Sales)</span></span>
- <span data-ttu-id="5596b-114">Konti (Sales til Fin og Ops) (hvis det bruges)</span><span class="sxs-lookup"><span data-stu-id="5596b-114">Accounts (Sales to Fin and Ops) (if used)</span></span>
- <span data-ttu-id="5596b-115">Kontakter til Debitorer (Sales til Fin and Ops) (hvis det bruges)</span><span class="sxs-lookup"><span data-stu-id="5596b-115">Contacts to Customers (Sales to Fin and Ops) (if used)</span></span>

## <a name="entity-set"></a><span data-ttu-id="5596b-116">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="5596b-116">Entity set</span></span>

| <span data-ttu-id="5596b-117">Salg</span><span class="sxs-lookup"><span data-stu-id="5596b-117">Sales</span></span>        | <span data-ttu-id="5596b-118">CDS</span><span class="sxs-lookup"><span data-stu-id="5596b-118">CDS</span></span>           | <span data-ttu-id="5596b-119">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5596b-119">Finance and Operations</span></span>    |
|--------------|---------------|---------------------------|
| <span data-ttu-id="5596b-120">Citater</span><span class="sxs-lookup"><span data-stu-id="5596b-120">Quotes</span></span>       | <span data-ttu-id="5596b-121">Tilbud</span><span class="sxs-lookup"><span data-stu-id="5596b-121">Quotation</span></span>     | <span data-ttu-id="5596b-122">Salgstilbudshoveder</span><span class="sxs-lookup"><span data-stu-id="5596b-122">Sales quotation headers</span></span>   |
| <span data-ttu-id="5596b-123">QuoteDetails</span><span class="sxs-lookup"><span data-stu-id="5596b-123">QuoteDetails</span></span> | <span data-ttu-id="5596b-124">QuotationLine</span><span class="sxs-lookup"><span data-stu-id="5596b-124">QuotationLine</span></span> | <span data-ttu-id="5596b-125">CDS-salgstilbudslinjer</span><span class="sxs-lookup"><span data-stu-id="5596b-125">CDS sales quotation lines</span></span> |

## <a name="entity-flow"></a><span data-ttu-id="5596b-126">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="5596b-126">Entity flow</span></span>

<span data-ttu-id="5596b-127">Salgstilbud oprettes i Sales og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-127">Sales quotations are created in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="5596b-128">Salgstilbud fra Sales synkroniseres kun, hvis følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="5596b-128">Sales quotations from Sales are synchronized only if the following conditions are met:</span></span>

- <span data-ttu-id="5596b-129">Alle produkter på linjerne i salgstilbuddet vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="5596b-129">All products on the sales quotation lines are externally maintained.</span></span>
- <span data-ttu-id="5596b-130">Salgstilbuddet er aktivt eller aktiveret.</span><span class="sxs-lookup"><span data-stu-id="5596b-130">The sales quotation is active or activated.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="5596b-131">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="5596b-131">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="5596b-132">Feltet **Har kun eksternt vedligeholdte produkter** er føjet til objektet Tilbud for konsekvent at spore, om salgstilbuddet består af udelukkende eksternt vedligeholdte produkter.</span><span class="sxs-lookup"><span data-stu-id="5596b-132">The **Has Externally Maintained Products Only** field has been added to the Quote entity to consistently track whether the sales quotation consists entirely of externally maintained products.</span></span> <span data-ttu-id="5596b-133">Hvis et salgstilbud kun har eksternt vedligeholdte produkter, vedligeholdes produkterne i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-133">If a sales quotation has only externally maintained products, the products are maintained in Finance and Operations.</span></span> <span data-ttu-id="5596b-134">Denne funktionsmåde er med til at sikre, at du ikke forsøger at synkronisere salgstilbudslinjer med produkter, der er ukendte i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-134">This behavior helps guarantee that you don't try to synchronize sales quotation lines with products that are unknown to Finance and Operations.</span></span>

<span data-ttu-id="5596b-135">Alle produkter og linjer i tilbuddet opdateres med **Har kun eksternt vedligeholdte produkter**-oplysningerne fra tilbudshovedet.</span><span class="sxs-lookup"><span data-stu-id="5596b-135">All products and lines on the quotation are updated with the **Has Externally Maintained Products Only** information from the quotation header.</span></span> <span data-ttu-id="5596b-136">Disse oplysninger findes i feltet **Tilbuddet indeholder kun eksternt vedligeholdte produkter** i enheden for tilbudslinjen.</span><span class="sxs-lookup"><span data-stu-id="5596b-136">This information can be found in the **Quote Has Externally Maintained Products Only** field on the Quote line entity.</span></span>

<span data-ttu-id="5596b-137">Felterne **Rabat**, **Tillæg** og **Moms** styres af en kompleks opsætning i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-137">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="5596b-138">Denne opsætning understøtter ikke aktuelt integrationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="5596b-138">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="5596b-139">I det aktuelle design styres og håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-139">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are mastered and handled by Finance and Operations.</span></span>

<span data-ttu-id="5596b-140">I Sales gør løsningen følgende felter skrivebeskyttet, fordi værdierne ikke synkroniseres for Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="5596b-140">In Sales, the solution makes the following fields read-only, because the values aren't synchronized to Finance and Operations:</span></span>

- <span data-ttu-id="5596b-141">**Skrivebeskyttede felter i salgstilbudshovedet:** Rabatprocent, Rabat, Fragtbeløb</span><span class="sxs-lookup"><span data-stu-id="5596b-141">**Read-only fields on the sales quotation header:** Discount %, Discount, Freight Amount</span></span>
- <span data-ttu-id="5596b-142">**Skrivebeskyttede felter på linjer i salgstilbuddet:** Moms</span><span class="sxs-lookup"><span data-stu-id="5596b-142">**Read-only fields on sales quotation lines:** Tax</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="5596b-143">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="5596b-143">Preconditions and mapping setup</span></span>

<span data-ttu-id="5596b-144">Før du synkroniserer salgsordrer, er det vigtigt at opdatere systemerne med følgende indstilling:</span><span class="sxs-lookup"><span data-stu-id="5596b-144">Before synchronizing sales orders, it is important to update the systems with the following setting:</span></span>

### <a name="setup-in-sales"></a><span data-ttu-id="5596b-145">Konfiguration i Sales</span><span class="sxs-lookup"><span data-stu-id="5596b-145">Setup in Sales</span></span>

- <span data-ttu-id="5596b-146">Gå til **Indstillinger** &gt; **Administration** &gt; **Systemindstillinger** &gt; **Sales** og kontrollér, at feltet **Rabatberegningsmetode** er indstillet til **Pr. enhed**.</span><span class="sxs-lookup"><span data-stu-id="5596b-146">Go to **Settings** &gt; **Administration** &gt; **System settings** &gt; **Sales**, and make sure that the **Discount calculation method** field is set to **Per unit**.</span></span> <span data-ttu-id="5596b-147">Med denne indstilling kan du sikre, at rabatten for linjeelementet fra Sales svarer til indstillingen i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-147">This setting helps guarantee that the line item discount from Sales matches the setting in Finance and Operations.</span></span> <span data-ttu-id="5596b-148">I modsat fald er rabatten ikke korrekt i Finance and Operations, fordi Finance and Operations læser rabatten som en rabat på pr. enhed, selvom det var en rabat pr. linje i Sales.</span><span class="sxs-lookup"><span data-stu-id="5596b-148">Otherwise, the discount won't be correct in Finance and Operations, because Finance and Operations will read the discount as a per-unit discount even if it was a per-line discount in Sales.</span></span>

### <a name="setup-in-finance-and-operations"></a><span data-ttu-id="5596b-149">Konfiguration i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5596b-149">Setup in Finance and Operations</span></span>

- <span data-ttu-id="5596b-150">Gå til **Debitor** &gt; **Konfiguration** &gt; **Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="5596b-150">Go to **Accounts receivable** &gt; **Setup** &gt; **Account receivable parameters**.</span></span> <span data-ttu-id="5596b-151">Under fanen **Nummerserie** skal du vælge nummerserien for salgstilbud og derefter klikke på **Vis detaljer**.</span><span class="sxs-lookup"><span data-stu-id="5596b-151">On the **Number sequence** tab, select the number sequence for sales quotations, and then click **View details**.</span></span> <span data-ttu-id="5596b-152">Derefter skal du under **Generel opsætning** indstille feltet **Manuel** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="5596b-152">Then, under **General Setup**, set the **Manual** field to **Yes**.</span></span>
- <span data-ttu-id="5596b-153">Gå til **Debitor** &gt; **Konfiguration** &gt; **Debitorparametre**.</span><span class="sxs-lookup"><span data-stu-id="5596b-153">Go to **Accounts receivable** &gt; **Setup** &gt; **Accounts receivable parameters**.</span></span> <span data-ttu-id="5596b-154">Under fanen **Forsendelser** skal du derefter indstille feltet **Leveringsdatokontrol** til **Ingen**.</span><span class="sxs-lookup"><span data-stu-id="5596b-154">Then, on the **Shipments** tab, set the **Delivery date control** field to **None**.</span></span> <span data-ttu-id="5596b-155">Denne indstilling hjælper med at forhindre, at synkronisering mislykkes for salgstilbud.</span><span class="sxs-lookup"><span data-stu-id="5596b-155">This setting helps prevent synchronization from failing for sales quotations.</span></span>

### <a name="setup-in-the-data-integration-project"></a><span data-ttu-id="5596b-156">Opsætning af dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="5596b-156">Setup in the Data integration project</span></span>

#### <a name="quoteheader"></a><span data-ttu-id="5596b-157">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="5596b-157">QuoteHeader</span></span>

- <span data-ttu-id="5596b-158">Feltet **Ønsket leveringsdato** er påkrævet i Finance and Operations, og synkroniseringen mislykkes, hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="5596b-158">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="5596b-159">For at undgå dette problem, hvis feltet er tomt, hentes en standarddato fra **Kilde &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="5596b-159">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="5596b-160">Datoen skal opdateres til en foretrukken værdi.</span><span class="sxs-lookup"><span data-stu-id="5596b-160">The date should be updated to a preferred value.</span></span> <span data-ttu-id="5596b-161">I øjeblikket kan du ikke angive en værdi som **I dag** som dags dato.</span><span class="sxs-lookup"><span data-stu-id="5596b-161">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="5596b-162">Du skal angive en konkret dato.</span><span class="sxs-lookup"><span data-stu-id="5596b-162">You must enter a specific date.</span></span> <span data-ttu-id="5596b-163">Standardværdien i skabelonen for **Ønsket leveringsdato** er **01-01-2020**.</span><span class="sxs-lookup"><span data-stu-id="5596b-163">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="5596b-164">Feltet **Adresse, lande-/områdekode** er påkrævet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-164">The **Address Country region code** field is required in Finance and Operations.</span></span> <span data-ttu-id="5596b-165">For at forhindre synkroniseringsfejl kan du angive en standardværdi, der bruges, hvis feltet er tomt i Sales.</span><span class="sxs-lookup"><span data-stu-id="5596b-165">To help prevent synchronization errors, you can specify a default value that is used if the field is left blank in Sales.</span></span> <span data-ttu-id="5596b-166">Denne standardværdi er også nyttig, fordi du ikke manuelt skal indtaste en værdi i feltet **Land/område** for lokale adresser.</span><span class="sxs-lookup"><span data-stu-id="5596b-166">This default value is also useful, because you don't have to manually enter a value in the **Country region** field for local addresses.</span></span> <span data-ttu-id="5596b-167">Der er ingen standardskabelonværdi for **DeliveryAddressCountryRegionISOCode**.</span><span class="sxs-lookup"><span data-stu-id="5596b-167">There is no default template value for **DeliveryAddressCountryRegionISOCode**.</span></span>
- <span data-ttu-id="5596b-168">Opdater tilknytningen for **CDS-organisations-id** i **Kilde &gt; CDS**, så den passer til **CDS-organisation** i organisationsenheden:</span><span class="sxs-lookup"><span data-stu-id="5596b-168">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="5596b-169">Standardskabelonværdien for **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="5596b-169">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="5596b-170">Standardskabelonværdien for **Account_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="5596b-170">The default template value for **Account_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="5596b-171">Standardskabelonværdien for **InvoiceAccount_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="5596b-171">The default template value for **InvoiceAccount_OrganizationId** is **ORG001**.</span></span>

#### <a name="quoteline"></a><span data-ttu-id="5596b-172">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="5596b-172">QuoteLine</span></span>

- <span data-ttu-id="5596b-173">Opdater tilknytningen for **CDS-organisations-id** i **Kilde &gt; CDS**, så den passer til **CDS-organisation** i organisationsenheden:</span><span class="sxs-lookup"><span data-stu-id="5596b-173">Update the mapping for **CDS Organization ID** in **Source &gt; CDS** so that it matches **CDS organization** in the Organization entity:</span></span>

    - <span data-ttu-id="5596b-174">Standardskabelonværdien for **Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="5596b-174">The default template value for **Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="5596b-175">Standardskabelonværdien for **Product_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="5596b-175">The default template value for **Product_Organization_Organization_OrganizationId** is **ORG001**.</span></span>
    - <span data-ttu-id="5596b-176">Standardskabelonværdien for **Quotation_Organization_Organization_OrganizationId** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="5596b-176">The default template value for **Quotation_Organization_Organization_OrganizationId** is **ORG001**.</span></span>

- <span data-ttu-id="5596b-177">Feltet **Ønsket leveringsdato** er påkrævet i Finance and Operations, og synkroniseringen mislykkes, hvis feltet er tomt.</span><span class="sxs-lookup"><span data-stu-id="5596b-177">The **Requested delivery date** field is required in Finance and Operations, and synchronization will fail if the field is left blank.</span></span> <span data-ttu-id="5596b-178">For at undgå dette problem, hvis feltet er tomt, hentes en standarddato fra **Kilde &gt; CDS**.</span><span class="sxs-lookup"><span data-stu-id="5596b-178">To prevent this issue, if the field is blank, a default date is taken from **Source &gt; CDS**.</span></span> <span data-ttu-id="5596b-179">Datoen skal opdateres til en foretrukken værdi.</span><span class="sxs-lookup"><span data-stu-id="5596b-179">The date should be updated to a preferred value.</span></span> <span data-ttu-id="5596b-180">I øjeblikket kan du ikke angive en værdi som **I dag** som dags dato.</span><span class="sxs-lookup"><span data-stu-id="5596b-180">Currently, you can't enter a value such as **Today** to represent today's date.</span></span> <span data-ttu-id="5596b-181">Du skal angive en konkret dato.</span><span class="sxs-lookup"><span data-stu-id="5596b-181">You must enter a specific date.</span></span> <span data-ttu-id="5596b-182">Standardværdien i skabelonen for **Ønsket leveringsdato** er **01-01-2020**.</span><span class="sxs-lookup"><span data-stu-id="5596b-182">The default template value for **Requested delivery date** is **1/1/2020**.</span></span>
- <span data-ttu-id="5596b-183">Du kan tilføje følgende tilknytninger fra **CDS &gt; Destination** for at sikre, at tilbudslinjerne importeres til Finance and Operations, hvis der ikke er nogen standardoplysninger fra debitoren eller produktet:</span><span class="sxs-lookup"><span data-stu-id="5596b-183">You can add the following mappings from **CDS &gt; Destination** to help guarantee that quotation lines are imported into Finance and Operations if there is no default information from either the customer or the product:</span></span>

    - <span data-ttu-id="5596b-184">**SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-184">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="5596b-185">Der er ingen standardskabelonværdi for **SiteId**.</span><span class="sxs-lookup"><span data-stu-id="5596b-185">There is no default template value for **SiteId**.</span></span>
    - <span data-ttu-id="5596b-186">**WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-186">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="5596b-187">Der er ingen standardskabelonværdi for **WarehouseId**.</span><span class="sxs-lookup"><span data-stu-id="5596b-187">There is no default template value for **WarehouseId**.</span></span>

- <span data-ttu-id="5596b-188">Sørg for, at den krævede værditilknytning for salgsmåleenheden (UOM) i Finance and Operations findes i **CDS &gt; Destination**-tilknytningen for **Quantity_UOM** til **SALESUNITSYMBOL**.</span><span class="sxs-lookup"><span data-stu-id="5596b-188">Make sure that the required value map for the selling unit of measure (UOM) in Finance and Operations exists in the **CDS &gt; Destination** mapping for **Quantity_UOM** to **SALESUNITSYMBOL**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="5596b-189">Tilknytning af skabelon i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="5596b-189">Template mapping in data integrator</span></span>

> [!NOTE]
> - <span data-ttu-id="5596b-190">Felterne **Rabat**, **Tillæg** og **Moms** styres af en kompleks opsætning i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-190">The **Discount**, **Charges**, and **Tax** fields are controlled by a complex setup in Finance and Operations.</span></span> <span data-ttu-id="5596b-191">Denne opsætning understøtter ikke aktuelt integrationstilknytning.</span><span class="sxs-lookup"><span data-stu-id="5596b-191">This setup doesn't currently support integration mapping.</span></span> <span data-ttu-id="5596b-192">I det aktuelle design håndteres felterne **Pris**, **Rabat**, **Tillæg** og **Moms** af Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="5596b-192">In the current design, the **Price**, **Discount**, **Charge**, and **Tax** fields are handled by Finance and Operations.</span></span>
> - <span data-ttu-id="5596b-193">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** er ikke en del af standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="5596b-193">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't part of the default mappings.</span></span> <span data-ttu-id="5596b-194">Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="5596b-194">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="5596b-195">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="5596b-195">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="quoteheader"></a><span data-ttu-id="5596b-196">QuoteHeader</span><span class="sxs-lookup"><span data-stu-id="5596b-196">QuoteHeader</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-1.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-2.png)

### <a name="quoteline"></a><span data-ttu-id="5596b-199">QuoteLine</span><span class="sxs-lookup"><span data-stu-id="5596b-199">QuoteLine</span></span>

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-3.png)

![Tilknytning af skabelon i dataintegrator](./media/sales-quotation-template-mapping-data-integrator-4.png)

## <a name="related-topics"></a><span data-ttu-id="5596b-202">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="5596b-202">Related topics</span></span>

[<span data-ttu-id="5596b-203">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="5596b-203">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="5596b-204">Synkronisere konti fra Sales med debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5596b-204">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="5596b-205">Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="5596b-205">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)



