---
title: Synkronisere konti direkte fra Sales med kunder i Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere konti fra Dynamics 365 Sales med Supply Chain Management.
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
ms.openlocfilehash: ebca416e94f44d0448a4f4d0be08f13e30e749e9
ms.sourcegitcommit: 57bc7e17682e2edb5e1766496b7a22f4621819dd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/18/2019
ms.locfileid: "2813218"
---
# <a name="synchronize-accounts-directly-from-sales-to-customers-in-supply-chain-management"></a><span data-ttu-id="25dde-103">Synkronisere konti direkte fra Sales med kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="25dde-103">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="25dde-104">Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="25dde-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Common Data Service for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="25dde-105">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere konti direkte fra Dynamics 365 Sales med Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25dde-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="25dde-106">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="25dde-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="25dde-107">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="25dde-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span>  <span data-ttu-id="25dde-108">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om konti, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="25dde-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="25dde-109">I følgende illustration vises, hvordan data synkroniseres mellem Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="25dde-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="25dde-110">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="25dde-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="25dde-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="25dde-111">Templates and tasks</span></span>

<span data-ttu-id="25dde-112">For at få adgang til de tilgængelige skabeloner skal du åbne [Power Apps Administration](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="25dde-112">To access the available templates, open [Power Apps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="25dde-113">Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="25dde-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="25dde-114">Følgende skabelon og underliggende opgave bruges til at synkronisere konti fra Sales med Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="25dde-114">The following template and underlying task are used to synchronize accounts from Sales to Supply Chain Management:</span></span>

- <span data-ttu-id="25dde-115">**Navnet på skabelonen i dataintegration:** Accounts (Sales to Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="25dde-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="25dde-116">**Navnet på opgaven i projektet:** Konti - Kunder</span><span class="sxs-lookup"><span data-stu-id="25dde-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="25dde-117">Der kræves ingen synkroniseringsopgaver, før der kan forekomme synkronisering af konto/kunde.</span><span class="sxs-lookup"><span data-stu-id="25dde-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="25dde-118">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="25dde-118">Entity set</span></span>

| <span data-ttu-id="25dde-119">Salg</span><span class="sxs-lookup"><span data-stu-id="25dde-119">Sales</span></span>    | <span data-ttu-id="25dde-120">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="25dde-120">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="25dde-121">Konti</span><span class="sxs-lookup"><span data-stu-id="25dde-121">Accounts</span></span> | <span data-ttu-id="25dde-122">Debitorer V2</span><span class="sxs-lookup"><span data-stu-id="25dde-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="25dde-123">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="25dde-123">Entity flow</span></span>

<span data-ttu-id="25dde-124">Konti administreres i Sales og synkroniseres med Supply Chain Management som kunder.</span><span class="sxs-lookup"><span data-stu-id="25dde-124">Accounts are managed in Sales and synchronized to Supply Chain Management as customers.</span></span> <span data-ttu-id="25dde-125">Egenskaben **Vedligeholdes eksternt** for disse kunder er indstillet til **Ja** for at spore kunder, der stammer fra Sales.</span><span class="sxs-lookup"><span data-stu-id="25dde-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="25dde-126">Under fakturering bruges disse oplysninger til at filtrere fakturaer, der synkroniseres med Sales.</span><span class="sxs-lookup"><span data-stu-id="25dde-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="25dde-127">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="25dde-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="25dde-128">Feltet **Kontonummer** er tilgængeligt på siden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="25dde-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="25dde-129">Det er blevet gjort til en naturlig og entydig nøgle for at understøtte integrationen.</span><span class="sxs-lookup"><span data-stu-id="25dde-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="25dde-130">Funktionen Naturlig nøgle i CRM-løsningen (Customer Relationship Management) kan påvirke kunder, der allerede anvender feltet **Kontonummer**, men som ikke bruger en entydige **Kontonummer**-værdier for hver konto.</span><span class="sxs-lookup"><span data-stu-id="25dde-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="25dde-131">Integrationsløsningen understøtter i øjeblikket ikke denne sag.</span><span class="sxs-lookup"><span data-stu-id="25dde-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="25dde-132">Når en ny konto oprettes, og der ikke allerede findes en værdi for **Kontonummer**, oprettes den automatisk ved hjælp af en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="25dde-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="25dde-133">Værdien består af **ACC** efterfulgt af en stigende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="25dde-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="25dde-134">Her er et eksempel: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="25dde-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="25dde-135">Når integrationsløsningen for Sales anvendes, indstiller et opgraderingsscript feltet **Kontonummer** for eksisterende konti i Sales.</span><span class="sxs-lookup"><span data-stu-id="25dde-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="25dde-136">Hvis der ikke er nogen **Kontonummer**-værdier, bruges den nummerserie, der blev nævnt tidligere.</span><span class="sxs-lookup"><span data-stu-id="25dde-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="25dde-137">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="25dde-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="25dde-138">Tilknytningen **CustomerGroupId** skal opdateres til en gyldig værdi i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25dde-138">The **CustomerGroupId** mapping must be updated to a valid value in Supply Chain Management.</span></span> <span data-ttu-id="25dde-139">Du kan angive en standardværdi, eller du kan angive værdien ved hjælp af en værditilknytning.</span><span class="sxs-lookup"><span data-stu-id="25dde-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="25dde-140">Standardskabelonværdien er **10**.</span><span class="sxs-lookup"><span data-stu-id="25dde-140">The default template value is **10**.</span></span>

- <span data-ttu-id="25dde-141">Ved at tilføje følgende tilknytninger kan du hjælpe med at reducere antallet af manuelle påkrævede opdateringer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25dde-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="25dde-142">Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="25dde-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="25dde-143">**SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25dde-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="25dde-144">Et standardsted kan hentes fra produktet eller fra kunden fra ordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="25dde-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="25dde-145">Standardskabelonværdien er **1**.</span><span class="sxs-lookup"><span data-stu-id="25dde-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="25dde-146">**WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25dde-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Supply Chain Management.</span></span> <span data-ttu-id="25dde-147">Et standardlagersted kan hentes fra produktet eller fra kunden fra ordrehovedet i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25dde-147">A default warehouse can be taken either from the product, or from the customer from the order header in Supply Chain Management.</span></span>

        <span data-ttu-id="25dde-148">Standardskabelonværdien er **13**.</span><span class="sxs-lookup"><span data-stu-id="25dde-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="25dde-149">**LanguageId** - Et sprog er påkrævet for at generere tilbud og salgsordrer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25dde-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span> <span data-ttu-id="25dde-150">Som standard bruges sproget fra ordrehovedet fra kunden.</span><span class="sxs-lookup"><span data-stu-id="25dde-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="25dde-151">Standardskabelonværdien er **da**.</span><span class="sxs-lookup"><span data-stu-id="25dde-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="25dde-152">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="25dde-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="25dde-153">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** indgår ikke i standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="25dde-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="25dde-154">Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="25dde-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="25dde-155">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="25dde-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="25dde-156">Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="25dde-156">The mapping shows which field information will be synchronized from Sales to Supply Chain Management.</span></span>

![Skabelontilknytning i dataintegration](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="25dde-158">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="25dde-158">Related topics</span></span>


[<span data-ttu-id="25dde-159">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="25dde-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="25dde-160">Synkronisere konti direkte fra Sales med kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="25dde-160">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="25dde-161">Synkronisere kontakter direkte fra Sales med kontakter eller kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="25dde-161">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="25dde-162">Synkronisering af salgsordrer direkte mellem Sales og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="25dde-162">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="25dde-163">Synkronisere salgsfakturahoveder og -linjer direkte fra Supply Chain Management til Sales</span><span class="sxs-lookup"><span data-stu-id="25dde-163">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)

