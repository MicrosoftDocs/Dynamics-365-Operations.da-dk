---
title: Synkroniser aftalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management
description: I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere aftalefakturaer i Dynamics 365 Field Service med fritekstfakturaer i Dynamics 365 Supply Chain Management.
author: ChristianRytt
ms.date: 04/10/2018
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 21a77a0289055285f47323803a484c012e662e3a
ms.sourcegitcommit: 0cc89dd42c1924ca0ec735c6566bc56b39cc5f7d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/26/2021
ms.locfileid: "6102728"
---
# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-supply-chain-management"></a><span data-ttu-id="359d3-103">Synkroniser aftalefakturaer i Field Service til fritekstfakturaer i Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="359d3-103">Synchronize agreement invoices in Field Service to free text invoices in Supply Chain Management</span></span>

[!include[banner](../includes/banner.md)]

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="359d3-104">I dette emne beskrives de skabeloner og underliggende opgaver, der bruges til at synkronisere aftalefakturaer i Dynamics 365 Field Service med fritekstfakturaer i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="359d3-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Dynamics 365 Field Service to free text invoices in Dynamics 365 Supply Chain Management.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="359d3-105">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="359d3-105">Templates and tasks</span></span>

<span data-ttu-id="359d3-106">Følgende skabelon og underliggende opgaver bruges til at køre synkronisering af aftalefakturaer fra Field Service til fritekstfakturaer i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="359d3-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Supply Chain Management.</span></span>

<span data-ttu-id="359d3-107">**Navnet på skabelonen i Dataintegration**</span><span class="sxs-lookup"><span data-stu-id="359d3-107">**Name of the template in Data integration**</span></span>

- <span data-ttu-id="359d3-108">Aftalefakturaer (Field Service til Supply Chain Management)</span><span class="sxs-lookup"><span data-stu-id="359d3-108">Agreement invoices (Field Service to Supply Chain Management)</span></span>

<span data-ttu-id="359d3-109">**Navnene på opgaverne i dataintegrationsprojekt**</span><span class="sxs-lookup"><span data-stu-id="359d3-109">**Names of the tasks in the Data integration project**</span></span>

- <span data-ttu-id="359d3-110">Fakturahoveder</span><span class="sxs-lookup"><span data-stu-id="359d3-110">Invoice headers</span></span>
- <span data-ttu-id="359d3-111">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="359d3-111">Invoice lines</span></span>

<span data-ttu-id="359d3-112">Følgende synkroniseringsopgaver kræves, før aftalefakturaer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="359d3-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="359d3-113">Konti (Sales til Supply Chain Management) - Direkte</span><span class="sxs-lookup"><span data-stu-id="359d3-113">Accounts (Sales to Supply Chain Management) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="359d3-114">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="359d3-114">Entity set</span></span>

| <span data-ttu-id="359d3-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="359d3-115">Field Service</span></span>  | <span data-ttu-id="359d3-116">Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="359d3-116">Supply Chain Management</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="359d3-117">fakturaer</span><span class="sxs-lookup"><span data-stu-id="359d3-117">invoices</span></span>       | <span data-ttu-id="359d3-118">Dataverse-debitorfakturahoveder i fri tekst</span><span class="sxs-lookup"><span data-stu-id="359d3-118">Dataverse customer free text invoice headers</span></span> |
| <span data-ttu-id="359d3-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="359d3-119">invoicedetails</span></span> | <span data-ttu-id="359d3-120">Dataverse-debitorfakturalinjer i fri tekst</span><span class="sxs-lookup"><span data-stu-id="359d3-120">Dataverse customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="359d3-121">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="359d3-121">Entity flow</span></span>

<span data-ttu-id="359d3-122">Fakturaer, der er oprettet ud fra en aftale i Field Service, kan synkroniseres til Supply Chain Management via et Microsoft Dataverse-dataintegrationsprojekt.</span><span class="sxs-lookup"><span data-stu-id="359d3-122">Invoices that are created from an agreement in Field Service can be synchronized to Supply Chain Management via a Microsoft Dataverse Data integration project.</span></span> <span data-ttu-id="359d3-123">Opdateringer til disse fakturaer synkroniseres til fritekstfakturaer i Supply Chain Management, hvis fritekstfakturaers regnskabsstatus er **Igangværende**.</span><span class="sxs-lookup"><span data-stu-id="359d3-123">Updates to these invoices will be synchronized to the free text invoices in Supply Chain Management if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="359d3-124">Når fritekstfakturaerne er bogført i Supply Chain Management, og regnskabsstatussen er opdateret til **Fuldført**, kan du ikke længere synkronisere opdateringer fra Field Service.</span><span class="sxs-lookup"><span data-stu-id="359d3-124">After the free text invoices are posted in Supply Chain Management, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="359d3-125">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="359d3-125">Field Service CRM solution</span></span>

<span data-ttu-id="359d3-126">Kolonnen **Har linjer, der stammer fra aftale** er blevet føjet til tabellen **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="359d3-126">The **Has Lines With Agreement Origin** column has been added to the **Invoice** table.</span></span> <span data-ttu-id="359d3-127">Denne kolonne er med til at sikre, at kun fakturaer, der er oprettet ud fra en aftale, bliver synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="359d3-127">This column helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="359d3-128">Værdien er **sand**, hvis fakturaen indeholder mindst en fakturalinje, der stammer fra en aftale.</span><span class="sxs-lookup"><span data-stu-id="359d3-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="359d3-129">Kolonnen **Har linjer, der stammer fra aftale** er blevet føjet til tabellen **Fakturalinje**.</span><span class="sxs-lookup"><span data-stu-id="359d3-129">The **Has Agreement Origin** column has been added to the **Invoice Line** table.</span></span> <span data-ttu-id="359d3-130">Denne kolonne er med til at sikre, at kun fakturalinjer, der er oprettet ud fra en aftale, bliver synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="359d3-130">This column helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="359d3-131">Værdien er **sand**, hvis fakturalinjen stammer fra en aftale.</span><span class="sxs-lookup"><span data-stu-id="359d3-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="359d3-132">**Fakturadato** er et obligatorisk felt i Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="359d3-132">**Invoice date** is a mandatory field in Supply Chain Management.</span></span> <span data-ttu-id="359d3-133">Derfor skal kolonnen have en værdi i Field Service, før synkroniseringen udføres.</span><span class="sxs-lookup"><span data-stu-id="359d3-133">Therefore, the column must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="359d3-134">For at opfylde disse krav, tilføjes følgende logik:</span><span class="sxs-lookup"><span data-stu-id="359d3-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="359d3-135">Hvis kolonnen **Fakturadato** er tom i tabellen **Faktura** (hvis det ingen værdi rummer), angives det til dags dato, når der tilføjes en fakturalinje, der stammer fra en aftale.</span><span class="sxs-lookup"><span data-stu-id="359d3-135">If the **Invoice Date** column is blank on the **Invoice** table (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="359d3-136">Brugeren kan ændre kolonnen **Fakturadato**.</span><span class="sxs-lookup"><span data-stu-id="359d3-136">The user can change the **Invoice Date** column.</span></span> <span data-ttu-id="359d3-137">Når brugeren forsøger at gemme en faktura, der stammer fra en aftale, modtager vedkommende imidlertid en fejl i forretningsprocessen, hvis kolonnen **Fakturadato** er tom på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="359d3-137">However, when the user tries to save an invoice that originates from an agreement, they receive a business process error if the **Invoice Date** column is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="359d3-138">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="359d3-138">Prerequisites and mapping setup</span></span>

### <a name="in-supply-chain-management"></a><span data-ttu-id="359d3-139">I Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="359d3-139">In Supply Chain Management</span></span>

<span data-ttu-id="359d3-140">Fakturaens oprindelse skal konfigureres af hensyn til integration for at kunne skelne fritekstfakturaer i Supply Chain Management, der er oprettet ud fra aftalefakturaer i Field Service.</span><span class="sxs-lookup"><span data-stu-id="359d3-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Supply Chain Management that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="359d3-141">Når en faktura har en fakturaoprindelse af typen **Integration af aftalefaktura**, vises feltet **Eksternt fakturanummer** på hovedet **Salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="359d3-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="359d3-142">Udover at blive vist i fakturahovedet kan oplysninger for **Eksternt fakturanummer** bruges til at sikre, at fakturaer, der er oprettet ud fra Field Service-aftalefakturaer, filtreres fra under fakturasynkroniseringen fra Supply Chain Management til Field Service.</span><span class="sxs-lookup"><span data-stu-id="359d3-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Supply Chain Management to Field Service.</span></span>

1. <span data-ttu-id="359d3-143">Gå til **Debitor** \> **Opsætning** \> **Oprindelseskoder for faktura**.</span><span class="sxs-lookup"><span data-stu-id="359d3-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="359d3-144">Vælg **Ny** til at oprette en ny fakturaoprindelse.</span><span class="sxs-lookup"><span data-stu-id="359d3-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="359d3-145">I feltet **Fakturaoprindelse** skal du angive et navn for fakturaoprindelsen, f.eks. **FS**.</span><span class="sxs-lookup"><span data-stu-id="359d3-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="359d3-146">Angiv en beskrivelse i feltet **Beskrivelse** som f.eks. **Aftalefaktura i Field Service**.</span><span class="sxs-lookup"><span data-stu-id="359d3-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="359d3-147">Markér afkrydsningsfeltet **Tildeling af oprindelsestype**.</span><span class="sxs-lookup"><span data-stu-id="359d3-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="359d3-148">Angiv feltet **Fakturaoprindelsestype** til **Integration af aftalefaktura**.</span><span class="sxs-lookup"><span data-stu-id="359d3-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="359d3-149">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="359d3-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="359d3-150">I dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="359d3-150">In the Data Integration project</span></span>

<span data-ttu-id="359d3-151">Opgave: **Fakturalinjer**</span><span class="sxs-lookup"><span data-stu-id="359d3-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="359d3-152">Sørg for, at standardværdien for feltet **Visningsværdi for hovedkonto** i Supply Chain Management opdateres, så det svarer til den ønskede værdi.</span><span class="sxs-lookup"><span data-stu-id="359d3-152">Make sure that the default value for the Supply Chain Management field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="359d3-153">Standardskabelonværdien er **401100**.</span><span class="sxs-lookup"><span data-stu-id="359d3-153">The default template value is **401100**.</span></span>

## <a name="template-mapping-in-data-integration"></a><span data-ttu-id="359d3-154">Skabelontilknytning i dataintegration</span><span class="sxs-lookup"><span data-stu-id="359d3-154">Template mapping in Data integration</span></span>

<span data-ttu-id="359d3-155">Følgende illustration viser skabelontilknytningen i Dataintegration.</span><span class="sxs-lookup"><span data-stu-id="359d3-155">The following illustrations show the template mapping in Data integration.</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-headers"></a><span data-ttu-id="359d3-156">Aftalefakturaer (Field Service til Supply Chain Management): Fakturaoverskrifter</span><span class="sxs-lookup"><span data-stu-id="359d3-156">Agreement invoices (Field Service to Supply Chain Management): Invoice headers</span></span>

<span data-ttu-id="359d3-157">[![Tilknytning af skabelon i Dataintegration for fakturahoveder](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span><span class="sxs-lookup"><span data-stu-id="359d3-157">[![Template mapping in Data integration for invoice headers](./media/FSFreeTextInvoice1.png)](./media/FSFreeTextInvoice1.png)</span></span>

### <a name="agreement-invoices-field-service-to-supply-chain-management-invoice-lines"></a><span data-ttu-id="359d3-158">Aftalefakturaer (Field Service til Supply Chain Management): Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="359d3-158">Agreement invoices (Field Service to Supply Chain Management): Invoice lines</span></span>

<span data-ttu-id="359d3-159">[![Tilknytning af skabelon i Dataintegration for fakturalinjer](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span><span class="sxs-lookup"><span data-stu-id="359d3-159">[![Template mapping in Data integration for invoice lines](./media/FSFreeTextInvoice2.png)](./media/FSFreeTextInvoice2.png)</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]