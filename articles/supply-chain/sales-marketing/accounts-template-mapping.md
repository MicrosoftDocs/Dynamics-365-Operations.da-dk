---
title: Synkronisere konti fra Sales med kunder i Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere konti fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 Finance and Operations, Enterprise edition.
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 1fdbeaaba53cd439d9872be78b1cf67cbc5a57b9
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-accounts-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="19c8d-103">Synkronisere konti fra Sales med kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="19c8d-103">Synchronize accounts from Sales to customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="19c8d-104">Før du kan bruge kundeemnet til kontantløsning, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="19c8d-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="19c8d-105">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere konti fra Microsoft Dynamics 365 for Sales (Sales) med Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="19c8d-105">The topic discusses the templates and underlying tasks that are used to synchronize accounts from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="template-and-task"></a><span data-ttu-id="19c8d-106">Skabelon og opgaver</span><span class="sxs-lookup"><span data-stu-id="19c8d-106">Template and task</span></span>

<span data-ttu-id="19c8d-107">Følgende skabeloner og underliggende opgaver bruges til at synkronisere konti fra Sales med Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="19c8d-107">The following templates and underlying tasks are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="19c8d-108">**Navnet på skabelonen:** Konti (Sales til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="19c8d-108">**Name of the template:** Accounts (Sales to Fin and Ops)</span></span>
- <span data-ttu-id="19c8d-109">**Navnet på opgaven i projektet:** Konti - Konto - Kunder</span><span class="sxs-lookup"><span data-stu-id="19c8d-109">**Name of the task in the project:** Accounts - Account - Customers</span></span>

<span data-ttu-id="19c8d-110">Synkroniseringsopgaver, der kræves før synkronisering af Konto/Kunde: Ingen</span><span class="sxs-lookup"><span data-stu-id="19c8d-110">Sync tasks required prior to Account / Customer sync: None</span></span>

## <a name="entity-set"></a><span data-ttu-id="19c8d-111">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="19c8d-111">Entity set</span></span>

| <span data-ttu-id="19c8d-112">Salg</span><span class="sxs-lookup"><span data-stu-id="19c8d-112">Sales</span></span>    | <span data-ttu-id="19c8d-113">CDS</span><span class="sxs-lookup"><span data-stu-id="19c8d-113">CDS</span></span>     | <span data-ttu-id="19c8d-114">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="19c8d-114">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="19c8d-115">Konti</span><span class="sxs-lookup"><span data-stu-id="19c8d-115">Accounts</span></span> | <span data-ttu-id="19c8d-116">Konto</span><span class="sxs-lookup"><span data-stu-id="19c8d-116">Account</span></span> | <span data-ttu-id="19c8d-117">Kunder</span><span class="sxs-lookup"><span data-stu-id="19c8d-117">Customers</span></span>              |

## <a name="entity-flow"></a><span data-ttu-id="19c8d-118">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="19c8d-118">Entity flow</span></span>

<span data-ttu-id="19c8d-119">Konti administreres i Sales og synkroniseres med Finance and Operations som kunder.</span><span class="sxs-lookup"><span data-stu-id="19c8d-119">Accounts are managed in Sales and synchronized to Finance and Operations as Customers.</span></span> <span data-ttu-id="19c8d-120">Egenskaben **Vedligeholdes eksternt** for disse kunder er indstillet til **Ja** for at spore kunder, der stammer fra Sales.</span><span class="sxs-lookup"><span data-stu-id="19c8d-120">The **Is Externally Maintained** property on these Customers is set to **Yes** to track Customers that originate from Sales.</span></span> <span data-ttu-id="19c8d-121">Under fakturering bruges disse oplysninger til at filtrere fakturaer, der synkroniseres med Sales.</span><span class="sxs-lookup"><span data-stu-id="19c8d-121">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="19c8d-122">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="19c8d-122">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="19c8d-123">Feltet **Kontonummer** er tilgængeligt på siden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-123">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="19c8d-124">Det er blevet gjort til en naturlig og entydig nøgle, som kan understøtte integrationen.</span><span class="sxs-lookup"><span data-stu-id="19c8d-124">It has been made a natural and unique key to support the integration.</span></span> <span data-ttu-id="19c8d-125">Funktionen Naturlig nøgle i CRM-løsningen (Customer Relationship Management) kan påvirke kunder, der allerede anvender feltet **Kontonummer**, men som ikke bruger en entydige **Kontonummer**-værdier for hver konto.</span><span class="sxs-lookup"><span data-stu-id="19c8d-125">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="19c8d-126">Integrationsløsningen understøtter i øjeblikket ikke denne sag.</span><span class="sxs-lookup"><span data-stu-id="19c8d-126">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="19c8d-127">Når en ny konto oprettes, og der ikke allerede findes en værdi for **Kontonummer**, oprettes den automatisk ved hjælp af en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="19c8d-127">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="19c8d-128">Værdien består af **ACC** efterfulgt af en stigende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="19c8d-128">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="19c8d-129">Her er et eksempel: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="19c8d-129">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="19c8d-130">Når integrationsløsningen for Sales anvendes, indstiller et opgraderingsscript feltet **Kontonummer** for eksisterende konti i Sales.</span><span class="sxs-lookup"><span data-stu-id="19c8d-130">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="19c8d-131">Hvis der ikke er nogen **Kontonummer**-værdier, bruges den nummerserie, der blev beskrevet tidligere.</span><span class="sxs-lookup"><span data-stu-id="19c8d-131">If there are no **Account Number** values, the number sequence that was described earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="19c8d-132">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="19c8d-132">Preconditions and mapping setup</span></span>

- <span data-ttu-id="19c8d-133">**CustomerGroupId**-tilknytningen fra **CDS &gt; Destination** skal opdateres til en gyldig værdi i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="19c8d-133">**CustomerGroupId** mapping from **CDS &gt; Destination** must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="19c8d-134">Du kan angive en standardværdi, eller du kan angive værdien ved hjælp af en værditilknytning.</span><span class="sxs-lookup"><span data-stu-id="19c8d-134">You can specify a default value, or you can set the value by using a value map.</span></span> <span data-ttu-id="19c8d-135">Standardskabelonværdien er **10**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-135">The default template value is **10**.</span></span>
- <span data-ttu-id="19c8d-136">**Adresse, lande-/områdekode** er påkrævet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="19c8d-136">**Address country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="19c8d-137">For at undgå synkroniseringsfejl kan du angive en standardværdi i tilknytningen fra **CDS &gt; Destination**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-137">To avoid synchronization errors, you can specify a default value in the mapping from **CDS &gt; Destination**.</span></span> <span data-ttu-id="19c8d-138">Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales.</span><span class="sxs-lookup"><span data-stu-id="19c8d-138">That default value is then used if the field is left blank in Sales.</span></span>

    - <span data-ttu-id="19c8d-139">Standardskabelonværdien for **AddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-139">The default template value for **AddressCountryRegionISOCode** is **USA**.</span></span>
    - <span data-ttu-id="19c8d-140">Standardskabelonværdien for **DeliveryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-140">The default template value for **DeliveryAddressCountryRegionISOCode** is **USA**.</span></span>

- <span data-ttu-id="19c8d-141">Ved at tilføje følgende tilknytninger fra **CDS &gt; Destination** kan du hjælpe med at reducere antallet af manuelle påkrævede opdateringer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="19c8d-141">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="19c8d-142">Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="19c8d-143">**SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="19c8d-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="19c8d-144">Et standardsted kan hentes fra produktet eller fra kunden fra ordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="19c8d-144">A default site can be taken either from the product, or from the customer from the order header.</span></span> <span data-ttu-id="19c8d-145">Standardskabelonværdien for **SiteId** er **1**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-145">The default template value for **SiteId** is **1**.</span></span>
    - <span data-ttu-id="19c8d-146">**WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="19c8d-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="19c8d-147">Et standardlagersted kan hentes fra produktet eller fra kunden fra ordrehovedet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="19c8d-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span> <span data-ttu-id="19c8d-148">Standardskabelonværdien for **WarehouseId** er **13**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-148">The default template value for **WarehouseId** is **13**.</span></span>
    - <span data-ttu-id="19c8d-149">**LanguageId** – Et sprog er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="19c8d-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="19c8d-150">Som standard bruges sproget fra ordrehovedet fra kunden.</span><span class="sxs-lookup"><span data-stu-id="19c8d-150">By default, the language from the order header from the customer is used.</span></span> <span data-ttu-id="19c8d-151">Standardskabelonværdien for **LanguageId** er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-151">The default template value for **LanguageId** is **en-us**.</span></span>

- <span data-ttu-id="19c8d-152">Opdater CDS-organisations-id'et (**Organization_OrganizationId**) i **Kilde &gt; CDS**-tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="19c8d-152">Update the CDS organization ID (**Organization_OrganizationId**) in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="19c8d-153">Standardskabelonværdien er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="19c8d-153">The default template value is **ORG001**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="19c8d-154">Tilknytning af skabelon i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="19c8d-154">Template mapping in data integrator</span></span>

> [!NOTE]
> <span data-ttu-id="19c8d-155">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** indgår ikke i standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="19c8d-155">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="19c8d-156">Hvis du vil tilknytte disse felter, skal du konfigurere en værditilknytning.</span><span class="sxs-lookup"><span data-stu-id="19c8d-156">To map these fields, you must set up a value mapping.</span></span> <span data-ttu-id="19c8d-157">Værditilknytninger er specifikke for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="19c8d-157">Value mappings are specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="19c8d-158">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="19c8d-158">The following illustrations show an example of a template mapping in data integrator.</span></span>

![Tilknytning af skabelon i dataintegrator](./media/accounts-template-mapping-data-integrator-1.png)

![Skabelontilknytning for konti i dataintegrator](./media/accounts-template-mapping-data-integrator-2.png)

## <a name="related-topics"></a><span data-ttu-id="19c8d-161">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="19c8d-161">Related topics</span></span>

[<span data-ttu-id="19c8d-162">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="19c8d-162">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="19c8d-163">Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="19c8d-163">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping.md)

[<span data-ttu-id="19c8d-164">Synkronisere titler og linjer i salgstilbud fra Sales med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="19c8d-164">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="19c8d-165">Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="19c8d-165">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="19c8d-166">Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="19c8d-166">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)




