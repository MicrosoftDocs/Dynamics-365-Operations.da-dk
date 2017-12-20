---
title: Synkronisere kontakter direkte fra Sales med kontakter eller debitorer i Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere enhederne kontakt (kontakter) og kontakt (kunder) fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.
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
ms.dyn365.ops.intro: July 2017 update
ms.search.validFrom: 2017-07-8
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: 8de9a920f384b69c9b3764a0431208bbdcb395bf
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="synchronize-contacts-directly-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="a484a-103">Synkronisere kontakter direkte fra Sales med kontakter eller debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a484a-103">Synchronize contacts directly from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="a484a-104">Før du kan bruge kundeemne til kontant-løsningen, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="a484a-104">Before you can use the Prospect to cash solution, you should be familiar with [Dynamics 365 Data integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span>

<span data-ttu-id="a484a-105">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere enhederne kontakt (kontakter) og kontakt (kunder) direkte fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="a484a-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) and Contact (Customers) entities directly from Microsoft Dynamics 365 for Sales to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.</span></span>

## <a name="data-flow-in-prospect-to-cash"></a><span data-ttu-id="a484a-106">Dataflow i kundeemne til kontant</span><span class="sxs-lookup"><span data-stu-id="a484a-106">Data flow in Prospect to cash</span></span>

<span data-ttu-id="a484a-107">Kundeemnet til kontant-løsningen bruger funktionen Dataintegration til at synkronisere data på tværs af forekomster af Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="a484a-107">The Prospect to cash solution uses the Data integration feature to synchronize data across instances of Finance and Operations and Sales.</span></span> <span data-ttu-id="a484a-108">Kundeemne til kontanter-skabelonerne, der er tilgængelige i funktionen Dataintegration, muliggør strømme af data om firmaer, kontakter, produkter, salgstilbud, salgsordrer og salgsfakturaer mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="a484a-108">The Prospect to cash templates that are available with the Data integration feature enable the flow of data about accounts, contacts, products, sales quotations, sales orders, and sales invoices between Finance and Operations and Sales.</span></span> <span data-ttu-id="a484a-109">I følgende illustration vises, hvordan data synkroniseres mellem Finance and Operations og Sales.</span><span class="sxs-lookup"><span data-stu-id="a484a-109">The following illustration shows how the data is synchronized between Finance and Operations and Sales.</span></span>

<span data-ttu-id="a484a-110">[![Dataflow i kundeemne til kontant](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span><span class="sxs-lookup"><span data-stu-id="a484a-110">[![Data flow in Prospect to cash](./media/prospect-to-cash-data-flow.png)](./media/prospect-to-cash-data-flow.png)</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="a484a-111">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="a484a-111">Templates and tasks</span></span>

<span data-ttu-id="a484a-112">For at få adgang til de tilgængelige skabeloner, skal du åbne [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span><span class="sxs-lookup"><span data-stu-id="a484a-112">To access the available templates, open [PowerApps Admin Center](https://preview.admin.powerapps.com/dataintegration).</span></span> <span data-ttu-id="a484a-113">Vælg **Projekter**, og vælg derefter i øverste højre hjørne **Nyt projekt** for at vælge offentlige skabeloner.</span><span class="sxs-lookup"><span data-stu-id="a484a-113">Select **Projects**, and then, in the upper-right corner, select **New project** to select public templates.</span></span>

<span data-ttu-id="a484a-114">Følgende skabeloner og underliggende opgaver bruges til at synkronisere enhederne kontakter (kontakter) i Sales med enhederne kontakter (kunder) i Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="a484a-114">The following templates and underlying tasks are used to synchronize Contact (Contacts) entities in Sales to Contact (Customers) entities in Finance and Operations:</span></span>

- <span data-ttu-id="a484a-115">**Navne på skabeloner i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="a484a-115">**Names of the templates in Data integration:**</span></span>

    - <span data-ttu-id="a484a-116">Kontakter (Fin and Ops til Sales) - Direkte</span><span class="sxs-lookup"><span data-stu-id="a484a-116">Contacts (Sales to Fin and Ops) - Direct</span></span>
    - <span data-ttu-id="a484a-117">Kontakter til kunder (Sales til Fin and Ops) - Direkte</span><span class="sxs-lookup"><span data-stu-id="a484a-117">Contacts to Customer (Sales to Fin and Ops) - Direct</span></span>

- <span data-ttu-id="a484a-118">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="a484a-118">**Names of the tasks in the Data integration project:**</span></span>

    - <span data-ttu-id="a484a-119">Kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="a484a-119">Contacts</span></span>
    - <span data-ttu-id="a484a-120">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="a484a-120">ContactToCustomer</span></span>

<span data-ttu-id="a484a-121">Følgende synkroniseringsopgave skal udføres før synkronisering af kontakter kan finde sted: Konti (Sales til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="a484a-121">The following synchronization task is required before contact synchronization can occur: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="a484a-122">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="a484a-122">Entity sets</span></span>

| <span data-ttu-id="a484a-123">Salg</span><span class="sxs-lookup"><span data-stu-id="a484a-123">Sales</span></span>    | <span data-ttu-id="a484a-124">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a484a-124">Finance and Operations</span></span> |
|----------|------------------------|
| <span data-ttu-id="a484a-125">Kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="a484a-125">Contacts</span></span> | <span data-ttu-id="a484a-126">CDS kontakter</span><span class="sxs-lookup"><span data-stu-id="a484a-126">CDS Contacts</span></span>           |
| <span data-ttu-id="a484a-127">Kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="a484a-127">Contacts</span></span> | <span data-ttu-id="a484a-128">Debitorer V2</span><span class="sxs-lookup"><span data-stu-id="a484a-128">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="a484a-129">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="a484a-129">Entity flow</span></span>

<span data-ttu-id="a484a-130">Kontakter administreres i Sales og synkroniseres til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-130">Contacts are managed in Sales and synchronized to Finance and Operations.</span></span>

<span data-ttu-id="a484a-131">En kontakt i Sales kan enten blive en kontakt eller en kunde i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-131">A contact in Sales can become either a contact or a customer in Finance and Operations.</span></span> <span data-ttu-id="a484a-132">For at bestemme om en kontakt i Sales skal synkroniseres til Finance and Operations som en kontakt eller en kunde, ser systemet på følgende egenskaber på kontakten i Sales:</span><span class="sxs-lookup"><span data-stu-id="a484a-132">To determine whether a contact in Sales should be synchronized to Finance and Operations as a contact or a customer, the system looks at the following properties on the contact in Sales:</span></span>

- <span data-ttu-id="a484a-133">**Synkronisering til en kunde i Finance and Operations:** Kontakter hvor **Er aktiv kunde** er angivet til **Ja**</span><span class="sxs-lookup"><span data-stu-id="a484a-133">**Synchronization to a customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="a484a-134">**Synkronisering til en kontakt i Finance and Operations:** Kontakter hvor **Er aktiv kunde** er angivet til **Nej** og **Firma** (overordnet konto/kontakt) peger på en konto (ikke en kontakt)</span><span class="sxs-lookup"><span data-stu-id="a484a-134">**Synchronization to a contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (parent account/contact) points to an account (not a contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="a484a-135">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="a484a-135">Prospect to cash solution for Sales</span></span>

<span data-ttu-id="a484a-136">Et nyt felt **Er aktiv kunde** er føjet til kontakten.</span><span class="sxs-lookup"><span data-stu-id="a484a-136">A new **Is Active Customer** field has been added to the contact.</span></span> <span data-ttu-id="a484a-137">Dette felt bruges til at skelne mellem kontakter, der har salgsaktivitet, og kontakter, der ikke har en salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="a484a-137">This field is used to differentiate contacts that have sales activity and contacts that don't have sales activity.</span></span> <span data-ttu-id="a484a-138">**Er aktiv kunde** er kun indstillet til **Ja** for kontakter, der har relaterede tilbud, ordrer eller fakturaer.</span><span class="sxs-lookup"><span data-stu-id="a484a-138">**Is Active Customer** is set to **Yes** only for contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="a484a-139">Kun disse kontakter synkroniseres med Finance and Operations som kunder.</span><span class="sxs-lookup"><span data-stu-id="a484a-139">Only those contacts are synchronized to Finance and Operations as customers.</span></span>

<span data-ttu-id="a484a-140">Et nyt felt **IsCompanyAnAccount** er føjet til kontakten.</span><span class="sxs-lookup"><span data-stu-id="a484a-140">A new **IsCompanyAnAccount** field has been added to the contact.</span></span> <span data-ttu-id="a484a-141">Dette felt angiver, om en kontakt er tilknyttet et firma (overordnet konto/kontakt) af typen **Konto**.</span><span class="sxs-lookup"><span data-stu-id="a484a-141">This field indicates whether a contact is linked to a company (parent account/contact) of the **Account** type.</span></span> <span data-ttu-id="a484a-142">Disse oplysninger bruges til at identificere kontakter, der skal synkroniseres med Finance and Operations som kontakter.</span><span class="sxs-lookup"><span data-stu-id="a484a-142">This information is used to identify contacts that should be synchronized to Finance and Operations as contacts.</span></span>

<span data-ttu-id="a484a-143">Et nyt felt, **Kontaktnummer**, er føjet til kontakten for at sikre en naturlig og entydig nøgle til integrationen.</span><span class="sxs-lookup"><span data-stu-id="a484a-143">A new **Contact Number** field has been added to the contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="a484a-144">Når der oprettes en ny kontakt, genereres der automatisk en værdi for **Kontaktnummer** ved hjælp af en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="a484a-144">When a new contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="a484a-145">Værdien består af **CON** efterfulgt af en stigende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="a484a-145">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="a484a-146">Her er et eksempel: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="a484a-146">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="a484a-147">Når integrationsløsningen for Sales anvendes, indstiller et opgraderingsscript feltet **Kontaktnummer** for eksisterende kontakter ved hjælp af den nummerserie, der blev omtalt tidligere.</span><span class="sxs-lookup"><span data-stu-id="a484a-147">When the integration solution for Sales is applied, an upgrade script sets the **Contact Number** field for existing contacts by using the number sequence that was mentioned earlier.</span></span> <span data-ttu-id="a484a-148">Opgraderingsscriptet indstiller også feltet **Er aktiv kunde** til **Ja** for alle kontakter, der har salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="a484a-148">The upgrade script also sets the **Is Active Customer** field to **Yes** for any contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="a484a-149">I Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a484a-149">In Finance and Operations</span></span>

<span data-ttu-id="a484a-150">Kontaktpersoner mærkes ved hjælp af egenskaben **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="a484a-150">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="a484a-151">Denne egenskab angiver, at en given kontakt vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="a484a-151">This property indicates that a given contact is maintained externally.</span></span> <span data-ttu-id="a484a-152">I dette tilfælde vedligeholdes eksternt vedligeholdte kontakter i Sales.</span><span class="sxs-lookup"><span data-stu-id="a484a-152">In this case, externally maintained contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="a484a-153">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="a484a-153">Preconditions and mapping setup</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="a484a-154">Kontakt til kunde</span><span class="sxs-lookup"><span data-stu-id="a484a-154">Contact to customer</span></span>

- <span data-ttu-id="a484a-155">**CustomerGroup** er påkrævet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-155">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="a484a-156">For at hjælpe med til at undgå synkroniseringsfejl kan du angive en standardværdi i tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="a484a-156">To help prevent synchronization errors, you can specify a default value in the mapping.</span></span> <span data-ttu-id="a484a-157">Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales.</span><span class="sxs-lookup"><span data-stu-id="a484a-157">That default value is then used if the field is left blank in Sales.</span></span>

    <span data-ttu-id="a484a-158">Standardskabelonværdien er **10**.</span><span class="sxs-lookup"><span data-stu-id="a484a-158">The default template value is **10**.</span></span>

- <span data-ttu-id="a484a-159">Ved at tilføje følgende tilknytninger kan du hjælpe med at reducere antallet af manuelle påkrævede opdateringer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-159">By adding the following mappings, you can help reduce the number of manual updates that are required in Finance and Operations.</span></span> <span data-ttu-id="a484a-160">Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="a484a-160">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="a484a-161">**SiteId** - Der kan også defineres et standardwebsted for produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-161">**SiteId** – A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="a484a-162">Et sted er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-162">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="a484a-163">En skabelonværdi for **SiteId** er ikke defineret.</span><span class="sxs-lookup"><span data-stu-id="a484a-163">A template value for **SiteId** isn't defined.</span></span>

    - <span data-ttu-id="a484a-164">**WarehouseId** - Der kan også defineres et standardlagersted for produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-164">**WarehouseId** – A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="a484a-165">Et lagersted er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-165">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span>

        <span data-ttu-id="a484a-166">En skabelonværdi for **WarehouseId** er ikke defineret.</span><span class="sxs-lookup"><span data-stu-id="a484a-166">A template value for **WarehouseId** isn't defined.</span></span>

    - <span data-ttu-id="a484a-167">**LanguageId** – Et sprog er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-167">**LanguageId** – A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span>
    
        <span data-ttu-id="a484a-168">Standardskabelonværdien er **da**.</span><span class="sxs-lookup"><span data-stu-id="a484a-168">The default template value for is **en-us**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="a484a-169">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="a484a-169">Template mapping in Data integration</span></span>

<span data-ttu-id="a484a-170">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegration.</span><span class="sxs-lookup"><span data-stu-id="a484a-170">The following illustrations show an example of a template mapping in Data integration.</span></span> 

> [!NOTE]
> <span data-ttu-id="a484a-171">Tilknytningen viser, hvilke oplysninger der synkroniseres fra Sales til Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="a484a-171">The mapping shows which field information will be synchronized from Sales to Finance and Operations.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="a484a-172">Kontakt til kontakt</span><span class="sxs-lookup"><span data-stu-id="a484a-172">Contact to contact</span></span>

![Skabelontilknytning i dataintegrator](./media/contacts-direct-template-mapping-data-integrator-1.png)

### <a name="contact-to-customer"></a><span data-ttu-id="a484a-174">Kontakt til kunde</span><span class="sxs-lookup"><span data-stu-id="a484a-174">Contact to customer</span></span>

![Skabelontilknytning i dataintegrator](./media/contacts-direct-template-mapping-data-integrator-2.png)


## <a name="related-topics"></a><span data-ttu-id="a484a-176">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="a484a-176">Related topics</span></span>

[<span data-ttu-id="a484a-177">Kundeemne til kontanter</span><span class="sxs-lookup"><span data-stu-id="a484a-177">Prospect to cash</span></span>](prospect-to-cash.md)

[<span data-ttu-id="a484a-178">Synkronisere konti fra direkte fra Sales med debitorer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="a484a-178">Synchronize accounts directly from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping-direct.md)

[<span data-ttu-id="a484a-179">Synkronisere produkter direkte fra Finance and Operations med produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="a484a-179">Synchronize products directly from Finance and Operations to products in Sales</span></span>](products-template-mapping-direct.md)

[<span data-ttu-id="a484a-180">Synkronisere salgsordrehoveder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="a484a-180">Synchronize sales order headers and lines directly from Finance and Operations to Sales</span></span>](sales-order-template-mapping-direct.md)

[<span data-ttu-id="a484a-181">Synkronisere salgsfakturahoveder og -linjer direkte fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="a484a-181">Synchronize sales invoice headers and lines directly from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping-direct.md)


