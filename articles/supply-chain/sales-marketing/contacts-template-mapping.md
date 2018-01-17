---
title: Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere kontaktpersoner (Kontaktpersoner) og kontaktpersoner (Kunder) fra Microsoft Dynamics 365 for Sales med Microsoft Dynamics 365 for Finance and Operations, Enterprise edition.
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
ms.openlocfilehash: 2982c0d6f04f9f7b639a73ed5f68a082f05b17be
ms.contentlocale: da-dk
ms.lasthandoff: 01/17/2018

---

# <a name="synchronize-contacts-from-sales-to-contacts-or-customers-in-finance-and-operations"></a><span data-ttu-id="e9a55-103">Synkronisere kontaktpersoner fra Sales med kontaktpersoner eller kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9a55-103">Synchronize contacts from Sales to contacts or customers in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

> [!NOTE]
> <span data-ttu-id="e9a55-104">Før du kan bruge kundeemnet til kontantløsning, skal du have kendskab til [Dynamics 365-dataintegration](/common-data-service/entity-reference/dynamics-365-integration).</span><span class="sxs-lookup"><span data-stu-id="e9a55-104">Before you can use the Prospect to cash solution, be familiar with [Dynamics 365 Data Integration](/common-data-service/entity-reference/dynamics-365-integration).</span></span> 

<span data-ttu-id="e9a55-105">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere kontaktpersonenheder (Kontaktpersoner) og kontaktpersoner (Kunder) fra Microsoft Dynamics 365 for Sales (Sales) med Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span><span class="sxs-lookup"><span data-stu-id="e9a55-105">This topic discusses the templates and underlying tasks that are used to synchronize Contact (Contacts) entities and Contact (Customers) from Microsoft Dynamics 365 for Sales (Sales) to Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (Finance and Operations).</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="e9a55-106">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="e9a55-106">Templates and tasks</span></span>

<span data-ttu-id="e9a55-107">Følgende skabeloner og underliggende opgaver bruges til at synkronisere kontaktpersoner (Kontaktpersoner) i Sales med kontaktpersoner (Kunder) i Finance and Operations:</span><span class="sxs-lookup"><span data-stu-id="e9a55-107">The following templates and underlying tasks are used to synchronize Contact (Contacts) in Sales to Contact (Customers) in Finance and Operations:</span></span>

- <span data-ttu-id="e9a55-108">**Skabelonernes navne:**</span><span class="sxs-lookup"><span data-stu-id="e9a55-108">**Names of the templates:**</span></span>

    - <span data-ttu-id="e9a55-109">Kontaktpersoner (Sales til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="e9a55-109">Contacts (Sales to Fin and Ops)</span></span>
    - <span data-ttu-id="e9a55-110">Kontaktpersoner til Kunder (Sales til Fin og Ops)</span><span class="sxs-lookup"><span data-stu-id="e9a55-110">Contacts to Customer (Sales to Fin and Ops)</span></span>

- <span data-ttu-id="e9a55-111">**Navnene på opgaverne i projektet:**</span><span class="sxs-lookup"><span data-stu-id="e9a55-111">**Names of the tasks in the project:**</span></span>

    - <span data-ttu-id="e9a55-112">Kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="e9a55-112">Contacts</span></span>
    - <span data-ttu-id="e9a55-113">ContactToCustomer</span><span class="sxs-lookup"><span data-stu-id="e9a55-113">ContactToCustomer</span></span>

<span data-ttu-id="e9a55-114">Følgende synkroniseringsopgave skal udføres før synkronisering af kontaktpersoner: Konti (Sales til Fin and Ops)</span><span class="sxs-lookup"><span data-stu-id="e9a55-114">The following synchronization task is required before Contact synchronization: Accounts (Sales to Fin and Ops)</span></span>

## <a name="entity-sets"></a><span data-ttu-id="e9a55-115">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="e9a55-115">Entity sets</span></span>

| <span data-ttu-id="e9a55-116">Sales</span><span class="sxs-lookup"><span data-stu-id="e9a55-116">Sales</span></span>    | <span data-ttu-id="e9a55-117">CDS</span><span class="sxs-lookup"><span data-stu-id="e9a55-117">CDS</span></span>     | <span data-ttu-id="e9a55-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9a55-118">Finance and Operations</span></span> |
|----------|---------|------------------------|
| <span data-ttu-id="e9a55-119">Kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="e9a55-119">Contacts</span></span> | <span data-ttu-id="e9a55-120">Kontakt</span><span class="sxs-lookup"><span data-stu-id="e9a55-120">Contact</span></span> | <span data-ttu-id="e9a55-121">CDS kontakter</span><span class="sxs-lookup"><span data-stu-id="e9a55-121">CDS Contacts</span></span>           |
| <span data-ttu-id="e9a55-122">Kontaktpersoner</span><span class="sxs-lookup"><span data-stu-id="e9a55-122">Contacts</span></span> | <span data-ttu-id="e9a55-123">Konto</span><span class="sxs-lookup"><span data-stu-id="e9a55-123">Account</span></span> | <span data-ttu-id="e9a55-124">Debitorer V2</span><span class="sxs-lookup"><span data-stu-id="e9a55-124">Customers V2</span></span>           |

## <a name="entity-flow"></a><span data-ttu-id="e9a55-125">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="e9a55-125">Entity flow</span></span>

<span data-ttu-id="e9a55-126">Kontaktpersoner administreres i Sales og synkroniseres med CDS (Common Data Service) og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-126">Contacts are managed in Sales, and are synchronized to Common Data Service (CDS) and Finance and Operations.</span></span>

<span data-ttu-id="e9a55-127">En kontaktperson i Sales kan blive en kontaktperson i CDS og Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-127">A Contact in Sales can become a Contact in CDS and Finance and Operations.</span></span> <span data-ttu-id="e9a55-128">Kontaktpersonen kan også blive en konto i CDS og en kunde i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-128">Alternatively, it can become an Account in CDS and a Customer in Finance and Operations.</span></span> <span data-ttu-id="e9a55-129">For at bestemme, om en kontaktperson skal hentes i Sales for at blive synkroniseret med CDS og Finance and Operations (f.eks. Kontaktpersoner i Sales &gt; Kontaktperson i CDS &gt; Kontaktpersoner i Finance and Operations), ser systemet på følgende egenskaber for Kontaktperson i Sales:</span><span class="sxs-lookup"><span data-stu-id="e9a55-129">To determine whether a contact should be picked up in Sales for synchronization to CDS and Finance and Operations (for example, Contacts in Sales &gt; Contact in CDS &gt; Contacts in Finance and Operations), the system looks at the following properties on Contact in Sales:</span></span>

- <span data-ttu-id="e9a55-130">**Synkroniser til Konto i CDS og Kunde i Finance and Operations:** Kontaktpersoner, hvor **Er aktiv kunde** er indstillet til **Ja**</span><span class="sxs-lookup"><span data-stu-id="e9a55-130">**Sync to Account in CDS and Customer in Finance and Operations:** Contacts where **Is Active Customer** is set to **Yes**</span></span>
- <span data-ttu-id="e9a55-131">**Synkroniser til Kontaktperson i CDS og Kontaktperson i Finance and Operations:** Kontaktpersoner, hvor **Er aktiv kunde** er indstillet til **Nej** og **Firma** (overordnet konto/kontaktperson) peger på en konto (og ikke en kontaktperson)</span><span class="sxs-lookup"><span data-stu-id="e9a55-131">**Sync to Contact in CDS and Contact in Finance and Operations:** Contacts where **Is Active Customer** is set to **No** and **Company** (Parent Account/Contact) points to an Account (not a Contact)</span></span>

## <a name="prospect-to-cash-solution-for-sales"></a><span data-ttu-id="e9a55-132">Kundeemne til kontantløsning for Sales</span><span class="sxs-lookup"><span data-stu-id="e9a55-132">Prospect to cash solution for Sales</span></span> 

<span data-ttu-id="e9a55-133">Et nyt felt **Er aktiv kunde** er føjet til Kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="e9a55-133">A new **Is Active Customer** field has been added to the Contact.</span></span> <span data-ttu-id="e9a55-134">Dette felt bruges til at skelne mellem kontaktpersoner, der har salgsaktivitet, og kontaktpersoner, der ikke har en salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="e9a55-134">This field is used to differentiate Contacts that have sales activity and Contacts that don't have sales activity.</span></span> <span data-ttu-id="e9a55-135">**Er aktiv kunde** er kun indstillet til **Ja** for kontaktpersoner, der har relaterede tilbud, ordrer eller fakturaer.</span><span class="sxs-lookup"><span data-stu-id="e9a55-135">**Is Active Customer** is set to **Yes** only for Contacts that have related quotations, orders, or invoices.</span></span> <span data-ttu-id="e9a55-136">Kun disse kontaktpersoner synkroniseres med Finance and Operations som kunder.</span><span class="sxs-lookup"><span data-stu-id="e9a55-136">Only those Contacts are synchronized to Finance and Operations as Customers.</span></span>

<span data-ttu-id="e9a55-137">Et nyt felt **IsCompanyAnAccount** er tilføjet i Kontaktperson.</span><span class="sxs-lookup"><span data-stu-id="e9a55-137">A new **IsCompanyAnAccount** field has been added to the Contact.</span></span> <span data-ttu-id="e9a55-138">Dette felt bruges til at angive, om en kontaktperson er tilknyttet et firma (overordnet konto/kontaktperson) af typen **Konto**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-138">This field is used to indicate whether a Contact is linked to a Company (Parent Account/Contact) of the **Account** type.</span></span> <span data-ttu-id="e9a55-139">Disse oplysninger bruges til at identificere kontaktpersoner, der skal synkroniseres med Finance and Operations som kontaktpersoner.</span><span class="sxs-lookup"><span data-stu-id="e9a55-139">This information is used to identify Contacts that should be synchronized to Finance and Operations as Contacts.</span></span>

<span data-ttu-id="e9a55-140">Et nyt felt, **Kontaktpersons nummer**, er føjet til kontaktpersonen for at sikre en naturlig og entydig nøgle til integrationen.</span><span class="sxs-lookup"><span data-stu-id="e9a55-140">A new **Contact Number** field has been added to the Contact to help guarantee a natural and unique key for the integration.</span></span> <span data-ttu-id="e9a55-141">Når der oprettes en ny kontaktperson, genereres der automatisk en værdi for **Kontaktpersons nummer** ved hjælp af en nummerserie.</span><span class="sxs-lookup"><span data-stu-id="e9a55-141">When a new Contact is created, a **Contact Number** value is automatically generated by using a number sequence.</span></span> <span data-ttu-id="e9a55-142">Værdien består af **CON** efterfulgt af en stigende nummerserie og et suffiks på seks tegn.</span><span class="sxs-lookup"><span data-stu-id="e9a55-142">The value consists of **CON**, followed by an increasing number sequence and then a suffix of six characters.</span></span> <span data-ttu-id="e9a55-143">Her er et eksempel: **CON-01000-BVRCPS**</span><span class="sxs-lookup"><span data-stu-id="e9a55-143">Here is an example: **CON-01000-BVRCPS**</span></span>

<span data-ttu-id="e9a55-144">Når integrationsløsningen for Sales føjes til Sales, indstiller et opgraderingsscript feltet **Kontaktpersons nummer** for eksisterende kontaktpersoner ved hjælp af den nummerserie, der blev beskrevet tidligere.</span><span class="sxs-lookup"><span data-stu-id="e9a55-144">When the integration solution for Sales is added to Sales, an upgrade script sets the **Contact Number** field for existing Contacts by using the number sequence that was discussed earlier.</span></span> <span data-ttu-id="e9a55-145">Opgraderingsscriptet indstiller også feltet **Er aktiv kunde** til **Ja** for de kontaktpersoner, der har salgsaktivitet.</span><span class="sxs-lookup"><span data-stu-id="e9a55-145">The upgrade script also sets the **Is Active Customer** field to **Yes** for any Contacts that have sales activity.</span></span>

## <a name="in-finance-and-operations"></a><span data-ttu-id="e9a55-146">I Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9a55-146">In Finance and Operations</span></span> 

<span data-ttu-id="e9a55-147">Kontaktpersoner mærkes ved hjælp af egenskaben **IsContactPersonExternallyMaintained**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-147">Contacts are tagged by using the **IsContactPersonExternallyMaintained** property.</span></span> <span data-ttu-id="e9a55-148">Denne egenskab angiver, at en given kontaktperson vedligeholdes eksternt.</span><span class="sxs-lookup"><span data-stu-id="e9a55-148">This property indicates that a given Contact is maintained externally.</span></span> <span data-ttu-id="e9a55-149">I dette tilfælde vedligeholdes eksternt vedligeholdte kontaktpersoner i Sales.</span><span class="sxs-lookup"><span data-stu-id="e9a55-149">In this case, externally maintained Contacts are maintained in Sales.</span></span>

## <a name="preconditions-and-mapping-setup"></a><span data-ttu-id="e9a55-150">Betingelserne og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="e9a55-150">Preconditions and mapping setup</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="e9a55-151">Kontaktperson til kontaktperson</span><span class="sxs-lookup"><span data-stu-id="e9a55-151">Contact to Contact</span></span>

- <span data-ttu-id="e9a55-152">Opdater **CDS-organisations-id** i **Kilde &gt; CDS**-tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="e9a55-152">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span>

    - <span data-ttu-id="e9a55-153">Standardskabelonværdien for **Organization_OrganizationId [Organisations-ID]** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-153">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
    - <span data-ttu-id="e9a55-154">Standardskabelonværdien for **PrimaryAccount_Organization_OrganizationId [Organisations-ID]** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-154">The default template value for **PrimaryAccount_Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>

- <span data-ttu-id="e9a55-155">**Adresse, lande-/områdekode** er påkrævet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-155">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="e9a55-156">For at undgå synkroniseringsfejl kan du angive en standardværdi i **CDS &gt; Operations**-tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="e9a55-156">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Operations** mapping.</span></span> <span data-ttu-id="e9a55-157">Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales.</span><span class="sxs-lookup"><span data-stu-id="e9a55-157">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="e9a55-158">Standardskabelonværdien for **PrimaryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-158">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="e9a55-159">Sørg for, at der findes en værdi for følgende felt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-159">Make sure that a value for the following field exists in Finance and Operations.</span></span> <span data-ttu-id="e9a55-160">Hvis oplysningerne ikke er nødvendige i Finance and Operations, kan du fjerne tilknytningen fra **CDS &gt; Destination**-tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="e9a55-160">If the information isn't required in Finance and Operations, you can remove the mapping from the **CDS &gt; Destination** mapping.</span></span>

    - <span data-ttu-id="e9a55-161">**Feltnavn i Finance and Operations:** Beslutning</span><span class="sxs-lookup"><span data-stu-id="e9a55-161">**Field name in Finance and Operations:** Decision</span></span>
    - <span data-ttu-id="e9a55-162">**Tilknytning:** PrimaryAccountRole = DecisionMakingRole</span><span class="sxs-lookup"><span data-stu-id="e9a55-162">**Mapping:** PrimaryAccountRole = DecisionMakingRole</span></span>

### <a name="contact-to-customer"></a><span data-ttu-id="e9a55-163">Kontaktperson til kunde</span><span class="sxs-lookup"><span data-stu-id="e9a55-163">Contact to Customer</span></span>

- <span data-ttu-id="e9a55-164">Opdater **CDS-organisations-id** i **Kilde &gt; CDS**-tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="e9a55-164">Update **CDS Organization ID** in the **Source &gt; CDS** mapping.</span></span> <span data-ttu-id="e9a55-165">Standardskabelonværdien for **Organization_OrganizationId [Organisations-ID]** er **ORG001**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-165">The default template value for **Organization_OrganizationId [Organization ID]** is **ORG001**.</span></span>
- <span data-ttu-id="e9a55-166">**Adresse, lande-/områdekode** er påkrævet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-166">**Address Country region code** is required in Finance and Operations.</span></span> <span data-ttu-id="e9a55-167">For at undgå synkroniseringsfejl kan du angive en standardværdi i **CDS &gt; Destination**-tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="e9a55-167">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="e9a55-168">Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales.</span><span class="sxs-lookup"><span data-stu-id="e9a55-168">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="e9a55-169">Standardskabelonværdien for **PrimaryAddressCountryRegionISOCode** er **USA**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-169">The default template value for **PrimaryAddressCountryRegionISOCode** is **USA**.</span></span>
- <span data-ttu-id="e9a55-170">**CustomerGroup** er påkrævet i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-170">**CustomerGroup** is required in Finance and Operations.</span></span> <span data-ttu-id="e9a55-171">For at undgå synkroniseringsfejl kan du angive en standardværdi i **CDS &gt; Destination**-tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="e9a55-171">To avoid synchronization errors, you can specify a default value in the **CDS &gt; Destination** mapping.</span></span> <span data-ttu-id="e9a55-172">Denne standardværdi bruges derefter, hvis feltet er tomt, i Sales.</span><span class="sxs-lookup"><span data-stu-id="e9a55-172">That default value is then used if the field is left blank in Sales.</span></span> <span data-ttu-id="e9a55-173">Standardskabelonværdien for **CustomerGroupId** er **10**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-173">The default template value for **CustomerGroupId** is **10**.</span></span>
- <span data-ttu-id="e9a55-174">Ved at tilføje følgende tilknytninger fra **CDS &gt; Destination** kan du hjælpe med at reducere antallet af manuelle opdateringer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-174">By adding the following mappings from **CDS &gt; Destination**, you can help reduce the number of manual updates that are in Finance and Operations.</span></span> <span data-ttu-id="e9a55-175">Du kan bruge en standardværdi eller en værditilknytning fra f.eks. **Land/område** eller **By**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-175">You can use a default value or a value map from, for example, **Country/Region** or **City**.</span></span>

    - <span data-ttu-id="e9a55-176">**SiteId** - Der kan også defineres et standardsted for produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-176">**SiteId** - A default site can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="e9a55-177">Et sted er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-177">A site is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="e9a55-178">En skabelonværdi for **SiteId** er ikke defineret.</span><span class="sxs-lookup"><span data-stu-id="e9a55-178">A template value for **SiteId** isn't defined.</span></span>
    - <span data-ttu-id="e9a55-179">**WarehouseId** - Der kan også defineres et standardlagersted for produkter i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-179">**WarehouseId** - A default warehouse can also be defined on products in Finance and Operations.</span></span> <span data-ttu-id="e9a55-180">Et lagersted er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-180">A warehouse is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="e9a55-181">En skabelonværdi for **WarehouseId** er ikke defineret.</span><span class="sxs-lookup"><span data-stu-id="e9a55-181">A template value for **WarehouseId** isn't defined.</span></span>
    - <span data-ttu-id="e9a55-182">**LanguageId** - Et sprog er påkrævet for at generere tilbud og salgsordrer i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e9a55-182">**LanguageId** - A language is required in order to generate quotations and sales orders in Finance and Operations.</span></span> <span data-ttu-id="e9a55-183">Standardskabelonværdien for **LanguageId** er **en-us**.</span><span class="sxs-lookup"><span data-stu-id="e9a55-183">The default template value for **LanguageId** is **en-us**.</span></span>

## <a name="template-mapping-in-data-integrator"></a><span data-ttu-id="e9a55-184">Tilknytning af skabelon i dataintegrator</span><span class="sxs-lookup"><span data-stu-id="e9a55-184">Template mapping in data integrator</span></span>

<span data-ttu-id="e9a55-185">Følgende illustration viser et eksempel på en skabelontilknytning i dataintegrator.</span><span class="sxs-lookup"><span data-stu-id="e9a55-185">The following illustrations show an example of a template mapping in data integrator.</span></span>

### <a name="contact-to-contact"></a><span data-ttu-id="e9a55-186">Kontaktperson til kontaktperson</span><span class="sxs-lookup"><span data-stu-id="e9a55-186">Contact to Contact</span></span>

![Tilknytning af skabelon i dataintegrator](./media/contacts-template-mapping-data-integrator-1.png)

![Skabelontilknytning for kontaktpersoner i dataintegrator](./media/contacts-template-mapping-data-integrator-2.png)

### <a name="contact-to-customer"></a><span data-ttu-id="e9a55-189">Kontaktperson til kunde</span><span class="sxs-lookup"><span data-stu-id="e9a55-189">Contact to Customer</span></span>

![Tilknytning af skabelon i dataintegrator](./media/contacts-template-mapping-data-integrator-3.png)

![Skabelontilknytning for kontaktpersoner i dataintegrator](./media/contacts-template-mapping-data-integrator-4.png)


## <a name="related-topics"></a><span data-ttu-id="e9a55-192">Relaterede emner</span><span class="sxs-lookup"><span data-stu-id="e9a55-192">Related topics</span></span>

[<span data-ttu-id="e9a55-193">Synkronisere produkter fra Finance and Operations til produkter i Sales</span><span class="sxs-lookup"><span data-stu-id="e9a55-193">Synchronize products from Finance and Operations to products in Sales</span></span>](products-template-mapping.md)

[<span data-ttu-id="e9a55-194">Synkronisere konti fra Sales med kunder i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9a55-194">Synchronize accounts from Sales to customers in Finance and Operations</span></span>](accounts-template-mapping.md)

[<span data-ttu-id="e9a55-195">Synkronisere titler og linjer i salgstilbud fra Sales med Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="e9a55-195">Synchronize sales quotation headers and lines from Sales to Finance and Operations</span></span>](sales-quotation-template-mapping.md)

[<span data-ttu-id="e9a55-196">Synkronisere salgsordrehoveder og linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="e9a55-196">Synchronize sales order headers and lines from Finance and Operations to Sales</span></span>](sales-order-template-mapping.md)

[<span data-ttu-id="e9a55-197">Synkronisere salgsfakturahoveder og linjer fra Finance and Operations til Sales</span><span class="sxs-lookup"><span data-stu-id="e9a55-197">Synchronize sales invoice headers and lines from Finance and Operations to Sales</span></span>](sales-invoice-template-mapping.md)

