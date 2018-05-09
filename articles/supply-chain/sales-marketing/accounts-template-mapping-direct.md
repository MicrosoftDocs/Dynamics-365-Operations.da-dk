---
title: Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere konti fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 for Finance and Operations.
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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: c7a4f54412808d2fd2fec6d213ce8a5a98d3e881
ms.contentlocale: da-dk
ms.lasthandoff: 05/08/2018

---

# <a name="synchronize-accounts-directly-from-sales-to-customers-in-finance-and-operations"></a><span data-ttu-id="7a2fc-103">Synkronisere konti fra Sales direkte med debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7a2fc-103">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>

[!include [banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="7a2fc-104">Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="7a2fc-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="7a2fc-105">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere konti direkte fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-105">This topic discusses the templates and underlying tasks that are used to synchronize accounts directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="7a2fc-106">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="7a2fc-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="7a2fc-107">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span>  <span data-ttu-id="7a2fc-108">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="7a2fc-109">I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="7a2fc-110">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="7a2fc-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="7a2fc-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="7a2fc-111">Templates and tasks</span></span>

<span data-ttu-id="7a2fc-112">For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="7a2fc-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="7a2fc-113">Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="7a2fc-114">Følgende skabelon og underliggende opgave bruges til at synkronisere konti fra Sales med Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="7a2fc-114">The following template and underlying task are used to synchronize accounts from Sales to Finance and Operations:</span></span>

- <span data-ttu-id="7a2fc-115">**Navnet på skabelonen i dataintegration:** Accounts (Sales to Fin and Ops) - Direct</span><span class="sxs-lookup"><span data-stu-id="7a2fc-115">**Name of the template in Data integration:** Accounts (Sales to Fin and Ops) - Direct</span></span>
- <span data-ttu-id="7a2fc-116">**Navnet på opgaven i projektet:** Konti - Kunder</span><span class="sxs-lookup"><span data-stu-id="7a2fc-116">**Name of the task in the project:** Accounts - Customers</span></span>

<span data-ttu-id="7a2fc-117">Der kræves ingen synkroniseringsopgaver, før der kan forekomme synkronisering af konto/kunde.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-117">No synchronization tasks are required before Account/Customer synchronization can occur.</span></span>

## <a name="entity-set"></a><span data-ttu-id="7a2fc-118">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="7a2fc-118">Entity set</span></span>

| <span data-ttu-id="7a2fc-119">Salg</span><span class="sxs-lookup"><span data-stu-id="7a2fc-119">Sales</span></span>    | <span data-ttu-id="7a2fc-120">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7a2fc-120">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="7a2fc-121">Konti</span><span class="sxs-lookup"><span data-stu-id="7a2fc-121">Accounts</span></span> | <span data-ttu-id="7a2fc-122">Debitorer V2</span><span class="sxs-lookup"><span data-stu-id="7a2fc-122">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="7a2fc-123">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="7a2fc-123">Entity flow</span></span>

<span data-ttu-id="7a2fc-124">Konti administreres i Sales og synkroniseres med Finance and Operations som kunder.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-124">Accounts are managed in Sales and synchronized to Finance and Operations as customers.</span></span> <span data-ttu-id="7a2fc-125">Egenskaben **Vedligeholdes eksternt** for disse kunder er indstillet til **Ja** for at spore kunder, der stammer fra Sales.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-125">The **Is Externally Maintained** property on these customers is set to **Yes** to track customers that originate from Sales.</span></span> <span data-ttu-id="7a2fc-126">Under fakturering bruges disse oplysninger til at filtrere fakturaer, der synkroniseres med Sales.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-126">During invoicing, this information is used to filter invoices that are synchronized to Sales.</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="7a2fc-127">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="7a2fc-127">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="7a2fc-128">Feltet **Kontonummer** er tilgængeligt på siden **Konto**.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-128">The **Account Number** field is available on the **Account** page.</span></span> <span data-ttu-id="7a2fc-129">Det er blevet gjort til en naturlig og entydig nøgle for at understøtte integrationen.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-129">It has been made a natural and unique key in order to support the integration.</span></span> <span data-ttu-id="7a2fc-130">Funktionen Naturlig nøgle i CRM-løsningen (Customer Relationship Management) kan påvirke kunder, der allerede anvender feltet **Kontonummer**, men som ikke bruger en entydige **Kontonummer**-værdier for hver konto.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-130">The natural key feature of the Customer Relationship Management (CRM) solution might affect customers who already use the **Account Number** field, but who don't use unique **Account Number** values per account.</span></span> <span data-ttu-id="7a2fc-131">Integrationsløsningen understøtter i øjeblikket ikke denne sag.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-131">Currently, the integration solution doesn't support this case.</span></span>

<span data-ttu-id="7a2fc-132">Når en ny konto oprettes, og der ikke allerede findes en værdi for **Kontonummer**, oprettes den automatisk ved hjælp af en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-132">When a new account is created, if an **Account Number** value doesn't already exist, it's automatically generated by using a number sequence.</span></span> <span data-ttu-id="7a2fc-133">Værdien består af **ACC** efterfulgt af en stigende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-133">The value consists of **ACC**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="7a2fc-134">Her er et eksempel: **ACC-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="7a2fc-134">Here is an example: **ACC-01000-BVRCPS**</span></span>

<span data-ttu-id="7a2fc-135">Når integrationsløsningen for Sales anvendes, indstiller et opgraderingsscript feltet **Kontonummer** for eksisterende konti i Sales.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-135">When the integration solution for Sales is applied, an upgrade script sets the **Account Number** field for existing accounts in Sales.</span></span> <span data-ttu-id="7a2fc-136">Hvis der ikke er nogen **Kontonummer**-værdier, bruges den nummerserie, der blev nævnt tidligere.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-136">If there are no **Account Number** values, the number sequence that was mentioned earlier is used.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="7a2fc-137">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="7a2fc-137">Preconditions and mapping setup</span></span>

- <span data-ttu-id="7a2fc-138">Tilknytningen **CustomerGroupId** skal opdateres til en gyldig værdi i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-138">The **CustomerGroupId** mapping must be updated to a valid value in Finance and Operations.</span></span> <span data-ttu-id="7a2fc-139">Du kan angive en standardværdi, eller du kan angive værdien ved hjælp af en værditilknytning.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-139">You can specify a default value, or you can set the value by using a value map.</span></span>

    <span data-ttu-id="7a2fc-140">Standardskabelonværdien er **10**.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-140">The default template value is **10**.</span></span>

- <span data-ttu-id="7a2fc-141">Ved at tilføje følgende tilknytninger kan du hjælpe med at reducere antallet af manuelle påkrævede opdateringer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-141">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="7a2fc-142">Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-142">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="7a2fc-143">**SiteId** - Et sted er påkrævet for at generere tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-143">**SiteId** – A site is required in order to generate quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="7a2fc-144">Et standardsted kan hentes fra produktet eller fra kunden fra ordrehovedet.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-144">A default site can be taken either from the product, or from the customer from the order header.</span></span>

        <span data-ttu-id="7a2fc-145">Standardskabelonværdien er **1**.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-145">The default template value is **1**.</span></span>

    - <span data-ttu-id="7a2fc-146">**WarehouseId** - Et lagersted er påkrævet for at behandle tilbud og salgsordrelinjer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-146">**WarehouseId** – A warehouse is required in order to process quotations and sales order lines in Finance and Operations.</span></span> <span data-ttu-id="7a2fc-147">Et standardlagersted kan hentes fra produktet eller fra kunden fra ordrehovedet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-147">A default warehouse can be taken either from the product, or from the customer from the order header in Finance and Operations.</span></span>

        <span data-ttu-id="7a2fc-148">Standardskabelonværdien er **13**.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-148">The default template value is **13**.</span></span>

    - <span data-ttu-id="7a2fc-149">**LanguageId** – Et sprog er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-149">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="7a2fc-150">Som standard bruges sproget fra ordrehovedet fra kunden.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-150">By default, the language from the order header from the customer is used.</span></span>

        <span data-ttu-id="7a2fc-151">Standardskabelonværdien er **da**.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-151">The default template value is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="7a2fc-152">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="7a2fc-152">Template mapping in Data integration</span></span>

> [!NOTE]
> <span data-ttu-id="7a2fc-153">Felterne **Betalingsbetingelser**, **Fragtbetingelser**, **Leveringsbetingelser**, **Leveringsmetode** og **Leveringstilstand** indgår ikke i standardtilknytningerne.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-153">The **Payment terms**, **Freight terms**, **Delivery terms**, **Shipping method**, and **Delivery mode** fields aren't included in the default mappings.</span></span> <span data-ttu-id="7a2fc-154">Hvis du vil tilknytte disse felter, skal du angive en værditilknytning, der er specifik for dataene i de organisationer, som enheden synkroniseres mellem.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-154">To map these fields, you must set up a value mapping that is specific to the data in the organizations that the entity is synchronized between.</span></span>

<span data-ttu-id="7a2fc-155">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-155">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="7a2fc-156">Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="7a2fc-156">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

![Skabelontilknytning i dataintegration](./media/accounts-direct-template-mapping-data-integrator-1.png)

## <a name="related-topics"></a><span data-ttu-id="7a2fc-158">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="7a2fc-158">Related topics</span></span>


[<span data-ttu-id="7a2fc-159">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="7a2fc-159">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="7a2fc-160">Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7a2fc-160">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="7a2fc-161">Synkronisere kontakter direkte fra Sales med kontakter eller debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="7a2fc-161">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>](contacts-template-mapping-direct.md)

[<span data-ttu-id="7a2fc-162">Synkronisere salgsordrehoveder og linjer fra Finance and Operations direkte med Sales</span><span class="sxs-lookup"><span data-stu-id="7a2fc-162">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="7a2fc-163">Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="7a2fc-163">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)


