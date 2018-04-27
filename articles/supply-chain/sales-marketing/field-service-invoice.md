---
title: Synkronisere aftalefakturaer i Field Service med fritekstfakturaer i Finance and Operations
description: Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere aftalefakturaer i Microsoft Dynamics 365 for Field Service til fritekstfakturaer i Microsoft Dynamics 365 for Finance and Operations.
author: ChristianRytt
manager: AnnBe
ms.date: 04/10/2018
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
ms.sourcegitcommit: 08cfd2cfa24bef0f0c92126f5d1052a12ceba37a
ms.openlocfilehash: 1863814d6dd645da8602495858d024fbad2e7149
ms.contentlocale: da-dk
ms.lasthandoff: 04/11/2018

---

# <a name="synchronize-agreement-invoices-in-field-service-to-free-text-invoices-in-finance-and-operations"></a><span data-ttu-id="9dd52-103">Synkronisere aftalefakturaer i Field Service med fritekstfakturaer i Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9dd52-103">Synchronize agreement invoices in Field Service to free text invoices in Finance and Operations</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="9dd52-104">Dette emne omhandler skabeloner og underliggende opgaver, der bruges til at synkronisere aftalefakturaer i Microsoft Dynamics 365 for Field Service til fritekstfakturaer i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dd52-104">This topic discusses the templates and underlying tasks that are used to synchronize agreement invoices in Microsoft Dynamics 365 for Field Service to free text invoices in Microsoft Dynamics 365 for Finance and Operations.</span></span>

## <a name="templates-and-tasks"></a><span data-ttu-id="9dd52-105">Skabeloner og opgaver</span><span class="sxs-lookup"><span data-stu-id="9dd52-105">Templates and tasks</span></span>

<span data-ttu-id="9dd52-106">De følgende skabelon og underliggende opgaver bruges til at køre synkronisering af aftalefakturaer fra Field Service til fritekstfakturaer i Finans and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dd52-106">The following template and underlying tasks are used to run synchronization of agreement invoices from Field Service to free text invoices in Finance and Operations.</span></span>

<span data-ttu-id="9dd52-107">**Navnet på skabelonen i dataintegration:**</span><span class="sxs-lookup"><span data-stu-id="9dd52-107">**Name of the template in Data integration:**</span></span>

- <span data-ttu-id="9dd52-108">Aftalefakturaer (Field Service til Finance and Operations)</span><span class="sxs-lookup"><span data-stu-id="9dd52-108">Agreement invoices (Field Service to Fin and Ops)</span></span>

<span data-ttu-id="9dd52-109">**Navne på opgaverne i dataintegrationsprojektet:**</span><span class="sxs-lookup"><span data-stu-id="9dd52-109">**Names of the tasks in the Data integration project:**</span></span>

- <span data-ttu-id="9dd52-110">Fakturahoveder</span><span class="sxs-lookup"><span data-stu-id="9dd52-110">Invoice headers</span></span>
- <span data-ttu-id="9dd52-111">Fakturalinjer</span><span class="sxs-lookup"><span data-stu-id="9dd52-111">Invoice lines</span></span>

<span data-ttu-id="9dd52-112">Følgende synkroniseringsopgaver kræves, før aftalefakturaer kan synkroniseres:</span><span class="sxs-lookup"><span data-stu-id="9dd52-112">The following synchronization is required before synchronization of agreement invoices can occur:</span></span>

- <span data-ttu-id="9dd52-113">Konti (Sales til Finance and Operations) – Direkte</span><span class="sxs-lookup"><span data-stu-id="9dd52-113">Accounts (Sales to Fin and Ops) – Direct</span></span>

## <a name="entity-set"></a><span data-ttu-id="9dd52-114">Enhedssæt</span><span class="sxs-lookup"><span data-stu-id="9dd52-114">Entity set</span></span>

| <span data-ttu-id="9dd52-115">Field Service</span><span class="sxs-lookup"><span data-stu-id="9dd52-115">Field Service</span></span>  | <span data-ttu-id="9dd52-116">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9dd52-116">Finance and Operations</span></span>                 |
|----------------|----------------------------------------|
| <span data-ttu-id="9dd52-117">fakturaer</span><span class="sxs-lookup"><span data-stu-id="9dd52-117">invoices</span></span>       | <span data-ttu-id="9dd52-118">CDS-debitorfakturahoveder i fri tekst</span><span class="sxs-lookup"><span data-stu-id="9dd52-118">CDS customer free text invoice headers</span></span> |
| <span data-ttu-id="9dd52-119">invoicedetails</span><span class="sxs-lookup"><span data-stu-id="9dd52-119">invoicedetails</span></span> | <span data-ttu-id="9dd52-120">CDS-debitorfakturalinjer i fri tekst</span><span class="sxs-lookup"><span data-stu-id="9dd52-120">CDS customer free text invoice lines</span></span>   |

## <a name="entity-flow"></a><span data-ttu-id="9dd52-121">Enhedsflow</span><span class="sxs-lookup"><span data-stu-id="9dd52-121">Entity flow</span></span>

<span data-ttu-id="9dd52-122">Fakturaer, der er oprettet ud fra en aftale i Field Service, kan synkroniseres til Finance and Operations via et CDS-dataintegrationsprojekt (CDS – Common Data Service).</span><span class="sxs-lookup"><span data-stu-id="9dd52-122">Invoices that are created from an agreement in Field Service can be synchronized to Finance and Operations via a Common Data Service (CDS) Data integration project.</span></span> <span data-ttu-id="9dd52-123">Opdateringer til disse fakturaer synkroniseres til fritekstfakturaer i Finance and Operations, hvis fritekstfakturaers regnskabsstatus er **Igangværende**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-123">Updates to these invoices will be synchronized to the free text invoices in Finance and Operations if the accounting status of the free text invoices is **In process**.</span></span> <span data-ttu-id="9dd52-124">Når fritekstfakturaerne er bogført i Finance and Operations, og regnskabsstatussen er opdateret til **Fuldført**, kan du ikke længere synkronisere opdateringer fra Field Service.</span><span class="sxs-lookup"><span data-stu-id="9dd52-124">After the free text invoices are posted in Finance and Operations, and the accounting status is updated to **Completed**, you can no longer synchronize updates from Field Service.</span></span>

## <a name="field-service-crm-solution"></a><span data-ttu-id="9dd52-125">CRM-løsning til Field Service</span><span class="sxs-lookup"><span data-stu-id="9dd52-125">Field Service CRM solution</span></span>

<span data-ttu-id="9dd52-126">Feltet **Har linjer, der stammer fra aftale** er blevet føjet til enheden **Faktura**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-126">The **Has Lines With Agreement Origin** field has been added to the **Invoice** entity.</span></span> <span data-ttu-id="9dd52-127">Dette felt er med til at sikre, at kun fakturaer, der er oprettet ud fra en aftale, bliver synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="9dd52-127">This field helps guarantee that only invoices that are created from an agreement are synchronized.</span></span> <span data-ttu-id="9dd52-128">Værdien er **sand**, hvis fakturaen indeholder mindst en fakturalinje, der stammer fra en aftale.</span><span class="sxs-lookup"><span data-stu-id="9dd52-128">The value is **true** if the invoice contains at least one invoice line that originates from an agreement.</span></span>

<span data-ttu-id="9dd52-129">Feltet **Stammer fra aftale** er blevet føjet til enheden **Fakturalinje**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-129">The **Has Agreement Origin** field has been added to the **Invoice Line** entity.</span></span> <span data-ttu-id="9dd52-130">Dette felt er med til at sikre, at kun fakturalinjer, der er oprettet ud fra en aftale, bliver synkroniseret.</span><span class="sxs-lookup"><span data-stu-id="9dd52-130">This field helps guarantee that only invoice lines that are created from an agreement are synchronized.</span></span> <span data-ttu-id="9dd52-131">Værdien er **sand**, hvis fakturalinjen stammer fra en aftale.</span><span class="sxs-lookup"><span data-stu-id="9dd52-131">The value is **true** if the invoice line originates from an agreement.</span></span>

<span data-ttu-id="9dd52-132">**Fakturadato** er et obligatorisk felt i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9dd52-132">**Invoice date** is a mandatory field in Finance and Operations.</span></span> <span data-ttu-id="9dd52-133">Derfor skal feltet have en værdi i Field Service, før synkroniseringen udføres.</span><span class="sxs-lookup"><span data-stu-id="9dd52-133">Therefore, the field must have a value in Field Service before synchronization occurs.</span></span> <span data-ttu-id="9dd52-134">For at opfylde disse krav, tilføjes følgende logik:</span><span class="sxs-lookup"><span data-stu-id="9dd52-134">To meet this requirement, the following logic is added:</span></span>

- <span data-ttu-id="9dd52-135">Hvis feltet **Fakturadato** er tomt i enheden **Faktura** (hvis det ingen værdi rummer), angives det til dags dato, når der tilføjes en fakturalinje, der stammer fra en aftale.</span><span class="sxs-lookup"><span data-stu-id="9dd52-135">If the **Invoice Date** field is blank on the **Invoice** entity (that is, if it has no value), it's set to the current date when an invoice line that originates from an agreement is added.</span></span>
- <span data-ttu-id="9dd52-136">Brugeren kan ændre feltet **Fakturadato**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-136">The user can change the **Invoice Date** field.</span></span> <span data-ttu-id="9dd52-137">Når brugeren forsøger at gemme en faktura, der stammer fra en aftale, modtager vedkommende imidlertid en fejl i forretningsprocessen, hvis feltet **Fakturadato** er tomt på fakturaen.</span><span class="sxs-lookup"><span data-stu-id="9dd52-137">However, when the user tries to save an invoice that originates from an agreement, he or she receives a business process error if the **Invoice Date** field is blank on the invoice.</span></span>

## <a name="prerequisites-and-mapping-setup"></a><span data-ttu-id="9dd52-138">Forudsætninger og tilknytningsopsætning</span><span class="sxs-lookup"><span data-stu-id="9dd52-138">Prerequisites and mapping setup</span></span>

### <a name="in-finance-and-operations"></a><span data-ttu-id="9dd52-139">I Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="9dd52-139">In Finance and Operations</span></span>

<span data-ttu-id="9dd52-140">Fakturaens oprindelse skal konfigureres af hensyn til integration for at kunne skelne fritekstfakturaer i Finance and Operations, der er oprettet ud fra aftalefakturaer i Field Service.</span><span class="sxs-lookup"><span data-stu-id="9dd52-140">An invoice origin must be set up for the integration, to distinguish the free text invoices in Finance and Operations that are created from agreement invoices in Field Service.</span></span> <span data-ttu-id="9dd52-141">Når en faktura har en fakturaoprindelse af typen **Integration af aftalefaktura**, vises feltet **Eksternt fakturanummer** på hovedet **Salgsfaktura**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-141">When an invoice has an invoice origin of the **Agreement invoice integration** type, the **External invoice number** field is shown on the **Sales invoice** header.</span></span>

<span data-ttu-id="9dd52-142">Udover at blive vist i fakturahovedet kan oplysninger for **Eksternt fakturanummer** bruges til at sikre, at fakturaer, der er oprettet ud fra Field Service-aftalefakturaer, filtreres fra under fakturasynkroniseringen fra Finance and Operations til Field Service.</span><span class="sxs-lookup"><span data-stu-id="9dd52-142">Besides appearing on the invoice header, the **External invoice number** information can be used to help guarantee that invoices that are created from Field Service agreement invoices are filtered out during invoice synchronization from Finance and Operations to Field Service.</span></span>

1. <span data-ttu-id="9dd52-143">Gå til **Debitor** \> **Opsætning** \> **Oprindelseskoder for faktura**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-143">Go to **Accounts receivable** \> **Setup** \> **Invoice origin codes**.</span></span>
2. <span data-ttu-id="9dd52-144">Vælg **Ny** til at oprette en ny fakturaoprindelse.</span><span class="sxs-lookup"><span data-stu-id="9dd52-144">Select **New** to create a new invoice origin.</span></span>
3. <span data-ttu-id="9dd52-145">I feltet **Fakturaoprindelse** skal du angive et navn for fakturaoprindelsen, f.eks. **FS**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-145">In the **Invoice origin** field, enter a name for the invoice origin, such as **FS**.</span></span>
4. <span data-ttu-id="9dd52-146">Angiv en beskrivelse i feltet **Beskrivelse** som f.eks. **Aftalefaktura i Field Service**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-146">In the **Description** field, enter a description, such as **Field Service Agreement Invoice**.</span></span>
5. <span data-ttu-id="9dd52-147">Markér afkrydsningsfeltet **Tildeling af oprindelsestype**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-147">Select the **Origin type assignment** check box.</span></span>
6. <span data-ttu-id="9dd52-148">Angiv feltet **Fakturaoprindelsestype** til **Integration af aftalefaktura**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-148">Set the **Invoice origin type** field to **Agreement invoice integration**.</span></span>
7. <span data-ttu-id="9dd52-149">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-149">Select **Save**.</span></span>

### <a name="in-the-data-integration-project"></a><span data-ttu-id="9dd52-150">I dataintegrationsprojektet</span><span class="sxs-lookup"><span data-stu-id="9dd52-150">In the Data Integration project</span></span>

<span data-ttu-id="9dd52-151">Opgave: **Fakturalinjer**</span><span class="sxs-lookup"><span data-stu-id="9dd52-151">Task: **Invoice lines**</span></span>  

<span data-ttu-id="9dd52-152">Sørg for, at standardværdien for feltet **Visningsværdi for hovedkonto** i Finance and Operations opdateres, så det svarer til den ønskede værdi.</span><span class="sxs-lookup"><span data-stu-id="9dd52-152">Make sure that the default value for the Finance and Operations field **Main Account Display Value** is updated to match the desired value.</span></span>

<span data-ttu-id="9dd52-153">Standardskabelonværdien er **401100**.</span><span class="sxs-lookup"><span data-stu-id="9dd52-153">The default template value is **401100**.</span></span>

