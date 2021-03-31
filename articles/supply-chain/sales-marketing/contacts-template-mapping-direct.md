---
title: Synkronisere kontakter direkte fra Sales med kontakter eller kunder i Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere enhederne Kontakt (kontakter) og Kontakt (kunder) fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: d0e3b8b2087547ea93a16cd3eb43b2126e0e787b
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5215787"
---
# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-supply-chain-management"></a><span data-ttu-id="6cdc3-103">Synkronisere kontakter direkte fra Sales med kontakter eller kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6cdc3-103">Synchronize contacts directly from Sales to contacts or customers in Supply Chain Management</span></span>

[!include [banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

> [!NOTE]
> <span data-ttu-id="6cdc3-104">Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Integrere data i Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span><span class="sxs-lookup"><span data-stu-id="6cdc3-104">Before you can use the Prospect to cash solution, you should be familiar with [Integrate data into Microsoft Dataverse for Apps](https://docs.microsoft.com/powerapps/administrator/data-integrator).</span></span>

<span data-ttu-id="6cdc3-105">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere tabellerne Kontakt (kontakter) og Kontakt (kunder) direkte fra Dynamics 365 Sales til Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) tables directly from Dynamics 365 Sales to Dynamics 365 Supply Chain Management.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="6cdc3-106">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="6cdc3-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="6cdc3-107">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Supply Chain Management and Sales.</span></span> <span data-ttu-id="6cdc3-108">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om konti, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Supply Chain Management and Sales.</span></span> <span data-ttu-id="6cdc3-109">I følgende illustration vises, hvordan data synkroniseres mellem Supply Chain Management og Sales.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-109">The following illustration shows how the data is synchronized between Supply Chain Management and Sales.</span></span>

<span data-ttu-id="6cdc3-110">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="6cdc3-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="6cdc3-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="6cdc3-111">Templates and tasks</span></span>

<span data-ttu-id="6cdc3-112">For at få adgang til de tilgængelige skabeloner skal du åbne [PowerApps Administration](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="6cdc3-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="6cdc3-113">Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="6cdc3-114">Følgende skabeloner og underliggende opgaver bruges til at synkronisere tabellerne Kontakt (kontakter) i Sales med tabellerne Kontakt (kunder) i Supply Chain Management:</span><span class="sxs-lookup"><span data-stu-id="6cdc3-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) tables in Sales to Contact (Customers) tables in Supply Chain Management.</span></span>

- <span data-ttu-id="6cdc3-115">**Navne på skabeloner i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="6cdc3-115">**Names of the templates in Data integration**</span></span>

    - <span data-ttu-id="6cdc3-116">Kontakter (Sales til Supply Chain Management) - Direkte</span><span class="sxs-lookup"><span data-stu-id="6cdc3-116">Contacts (Sales to Supply Chain Management) - Direct</span></span>
    - <span data-ttu-id="6cdc3-117">Kontakter til kunde (Sales til Supply Chain Management) - Direkte</span><span class="sxs-lookup"><span data-stu-id="6cdc3-117">Contacts to Customer (Sales to Supply Chain Management) - Direct</span></span>

- <span data-ttu-id="6cdc3-118">**Navnene på opgaverne i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="6cdc3-118">**Names of the tasks in the Data integration project**</span></span>

    - <span data-ttu-id="6cdc3-119">Kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="6cdc3-119">Contacts</span></span>
    - <span data-ttu-id="6cdc3-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="6cdc3-120">ContactToCustomer</span></span>

<span data-ttu-id="6cdc3-121">Følgende synkroniseringsopgave skal udføres før synkronisering af kontakter kan finde sted: Konti (Sales til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="6cdc3-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Supply Chain Management)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="6cdc3-122">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="6cdc3-122">Entity sets</span></span>

| <span data-ttu-id="6cdc3-123">Sales</span><span class="sxs-lookup"><span data-stu-id="6cdc3-123">Sales</span></span>    | <span data-ttu-id="6cdc3-124">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6cdc3-124">Supply Chain Management</span></span> |
|----------|------------------------|
| <span data-ttu-id="6cdc3-125">Kontakter</span><span class="sxs-lookup"><span data-stu-id="6cdc3-125">Contacts</span></span> | <span data-ttu-id="6cdc3-126">Dataverse-kontakter</span><span class="sxs-lookup"><span data-stu-id="6cdc3-126">Dataverse Contacts</span></span>           |
| <span data-ttu-id="6cdc3-127">Kontakter</span><span class="sxs-lookup"><span data-stu-id="6cdc3-127">Contacts</span></span> | <span data-ttu-id="6cdc3-128">Debitorer V2</span><span class="sxs-lookup"><span data-stu-id="6cdc3-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="6cdc3-129">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="6cdc3-129">Entity flow</span></span>

<span data-ttu-id="6cdc3-130">Kontakter administreres i Sales og synkroniseres tol Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-130">Contacts are managed in Sales and synchronized to Supply Chain Management.</span></span>

<span data-ttu-id="6cdc3-131">En kontakt i Sales kan enten blive en kontakt eller en kunde i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-131">A contact in Sales can become either a contact or a customer in Supply Chain Management.</span></span> <span data-ttu-id="6cdc3-132">For at bestemme om en kontakt i Sales skal synkroniseres til Supply Chain Management som en kontakt eller en kunde, ser systemet på følgende egenskaber på kontakten i Sales:</span><span class="sxs-lookup"><span data-stu-id="6cdc3-132">To determine whether a contact in Sales should be synchronized to Supply Chain Management as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="6cdc3-133">**Synkronisering til en kunde i Supply Chain Management:** Kontakter hvor **Er aktiv kunde** er angivet til **Ja**</span><span class="sxs-lookup"><span data-stu-id="6cdc3-133">**Synchronization to a customer in Supply Chain Management:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="6cdc3-134">**Synkronisering til en kontakt i Supply Chain Management:** Kontakter hvor **Er aktiv kunde** er angivet til **Nej** og **Firma** (overordnet konto/kontakt) peger på en konto (ikke en kontakt)</span><span class="sxs-lookup"><span data-stu-id="6cdc3-134">**Synchronization to a contact in Supply Chain Management:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="6cdc3-135">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="6cdc3-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="6cdc3-136">Den nye kolonne **Er aktiv kunde** er føjet til kontakten.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-136">A new **Is Active Customer** column has been added to the contact.</span></span> <span data-ttu-id="6cdc3-137">Denne kolonne bruges til at skelne mellem kontakter, der har salgsaktivitet, og kontakter, der ikke har en salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-137">This column is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="6cdc3-138">**Er aktiv kunde** er kun indstillet til **Ja** for kontakter, der har relaterede tilbud, ordrer eller fakturaer.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="6cdc3-139">Kun disse kontakter synkroniseres med Supply Chain Management som kunder.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-139">Only those contacts are synchronized to Supply Chain Management as customers.</span></span>

<span data-ttu-id="6cdc3-140">Den nye kolonne **IsCompanyAnAccount** er føjet til kontakten.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-140">A new **IsCompanyAnAccount** column has been added to the contact.</span></span> <span data-ttu-id="6cdc3-141">Denne kolonne angiver, om en kontakt er tilknyttet et firma (overordnet konto/kontakt) af typen **Konto**.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-141">This column indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="6cdc3-142">Disse oplysninger bruges til at identificere kontakter, der skal synkroniseres med Supply Chain Management som kontakter.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-142">This information is used to identify contacts that should be synchronized to Supply Chain Management as contacts.</span></span>

<span data-ttu-id="6cdc3-143">Den nye kolonne **Kontaktnummer** er føjet til kontakten for at sikre en naturlig og entydig nøgle til integrationen.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-143">A new **Contact Number** column has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="6cdc3-144">Når der oprettes en ny kontakt, genereres der automatisk en værdi for **Kontaktnummer** ved hjælp af en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="6cdc3-145">Værdien består af **CON** efterfulgt af en stigende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="6cdc3-146">Her er et eksempel: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="6cdc3-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="6cdc3-147">Når integrationsløsningen for Sales anvendes, indstiller et opgraderingsscript kolonnen **Kontaktnummer** for eksisterende kontakter ved hjælp af den nummerserie, der blev omtalt tidligere.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** column for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="6cdc3-148">Opgraderingsscriptet indstiller også kolonnen **Er aktiv kunde** til **Ja** for alle kontakter, der har salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-148">The upgrade script also sets the **Is Active Customer** column to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-supply-chain-management"></a><span data-ttu-id="6cdc3-149">I Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6cdc3-149">In Supply Chain Management</span></span>

<span data-ttu-id="6cdc3-150">Kontaktpersoner mærkes ved hjælp af egenskaben **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="6cdc3-151">Denne egenskab angiver, at en given kontakt vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="6cdc3-152">I dette tilfælde vedligeholdes eksternt vedligeholdte kontakter i Sales.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="6cdc3-153">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="6cdc3-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="6cdc3-154">Kontakt til kunde</span><span class="sxs-lookup"><span data-stu-id="6cdc3-154">Contact to customer</span></span>

- <span data-ttu-id="6cdc3-155">**CustomerGroup** er påkrævet i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-155">**CustomerGroup** is required in Supply Chain Management.</span></span> <span data-ttu-id="6cdc3-156">For at hjælpe med til at undgå synkroniseringsfejl kan du angive en standardværdi i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="6cdc3-157">Denne standardværdi bruges derefter, hvis kolonnen er tom i Sales.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-157">That default value is then used if the column is left blank in Sales.</span></span>

    <span data-ttu-id="6cdc3-158">Standardskabelonværdien er **10**.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-158">The default template value is **10**.</span></span>

- <span data-ttu-id="6cdc3-159">Ved at tilføje følgende tilknytninger kan du hjælpe med at reducere antallet af manuelle påkrævede opdateringer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Supply Chain Management.</span></span> <span data-ttu-id="6cdc3-160">Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="6cdc3-161">**SiteId** - Der kan også defineres et standardwebsted for produkter i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-161">**SiteId** – A default site can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="6cdc3-162">Et sted er påkrævet for at generere tilbud og salgsordrer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-162">A site is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="6cdc3-163">En skabelonværdi for **SiteId** er ikke defineret.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="6cdc3-164">**WarehouseId** - Der kan også defineres et lagersted for produkter i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-164">**WarehouseId** – A default warehouse can also be defined on products in Supply Chain Management.</span></span> <span data-ttu-id="6cdc3-165">Et lagersted er påkrævet for at generere tilbud og salgsordrer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-165">A warehouse is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>

        <span data-ttu-id="6cdc3-166">En skabelonværdi for **WarehouseId** er ikke defineret.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="6cdc3-167">**LanguageId** - Et sprog er påkrævet for at generere tilbud og salgsordrer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Supply Chain Management.</span></span>
    
        <span data-ttu-id="6cdc3-168">Standardskabelonværdien er **da**.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="6cdc3-169">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="6cdc3-169">Template mapping in Data integration</span></span>

<span data-ttu-id="6cdc3-170">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="6cdc3-171">Tilknytningen viser, hvilke kolonneoplysninger der synkroniseres fra Sales til Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="6cdc3-171">The mapping shows which column information will be synchronized from Sales to Supply Chain Management.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="6cdc3-172">Kontakt til kontakt</span><span class="sxs-lookup"><span data-stu-id="6cdc3-172">Contact to contact</span></span>

![Skabelontilknytning i dataintegrator](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="6cdc3-174">Kontakt til kunde</span><span class="sxs-lookup"><span data-stu-id="6cdc3-174">Contact to customer</span></span>

![Skabelontilknytning i dataintegrator](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="6cdc3-176">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="6cdc3-176">Related topics</span></span>

[<span data-ttu-id="6cdc3-177">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="6cdc3-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="6cdc3-178">Synkronisere konti direkte fra Sales med kunder i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6cdc3-178">Synchronize accounts directly from Sales to customers in Supply Chain Management</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="6cdc3-179">Synkronisere produkter direkte fra Supply Chain Management med produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="6cdc3-179">Synchronize products directly from Supply Chain Management to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="6cdc3-180">Synkronisering af salgsordrer direkte mellem Sales og Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="6cdc3-180">Synchronization of sales orders directly between Sales and Supply Chain Management</span></span>](sales-order-template-mapping-direct-two-ways.md)

[<span data-ttu-id="6cdc3-181">Synkronisere salgsfakturahoveder og -linjer direkte fra Supply Chain Management til Sales</span><span class="sxs-lookup"><span data-stu-id="6cdc3-181">Synchronize sales invoice headers and lines directly from Supply Chain Management to Sales</span></span>](sales-invoice-template-mapping-direct.md)




[!INCLUDE[footer-include](../../includes/footer-banner.md)]