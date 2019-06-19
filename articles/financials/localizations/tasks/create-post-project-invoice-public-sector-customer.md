---
title: Oprette og bogføre en projektfaktura for en debitor i den offentlige sektor
description: Denne opgave hjælper dig med at oprette og bogføre en projektfaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ProjProjectContractsListPage, ProjInvoiceTable, ProjFundingSourceDetail, ContactPersonLookup, ProjSalesItemReq, ProjTableLookup, InventItemIdLookupSimple, SalesEditLines,  ProjInvoiceProposalListPage, ProjInvoiceProposalCreateLines, ProjInvoiceProposalDetail, ProjInvoiceEditLines, ProjInvoiceListPage, ERFormatMappingRunJobTable
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f894c3bc94ddeac1a92f72949b841bacfbe67c2d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568777"
---
# <a name="create-and-post-a-project-invoice-for-a-public-sector-customer"></a><span data-ttu-id="6e6fa-103">Oprette og bogføre en projektfaktura for en debitor i den offentlige sektor</span><span class="sxs-lookup"><span data-stu-id="6e6fa-103">Create and post a project invoice for a public sector customer</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="6e6fa-104">Denne opgave hjælper dig med at oprette og bogføre en projektfaktura for en debitor ved hjælp af elektronisk OIOUBL-fakturering.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-104">This task walks you through creating and posting a project invoice for a customer using OIOUBL electronic invoicing.</span></span> 



<span data-ttu-id="6e6fa-105">Denne opgave blev oprettet ved hjælp af demodatafirmaet USMF med landet/området i den juridiske enheds primære adresse opdateret til Danmark.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-105">This task was created using the demo data company USMF with the country/region of legal entity primary address updated to Denmark.</span></span>



<span data-ttu-id="6e6fa-106">Det er den sjette af seks procedurer, der viser den afsluttende proces til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-106">This is the sixth procedure out of six illustrating end to end process of generating e-invoices using electronic reporting configurations.</span></span> <span data-ttu-id="6e6fa-107">Den er baseret på OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-107">It is based on OIOUBL e-invoice example which is common for Denmark, Austria and Norway.</span></span> <span data-ttu-id="6e6fa-108">Du kan finde mindre forskelle for andre landespecifikke e-fakturaimplementeringer, som spansk eller italiensk, i tilgængelige WIKI-artikler.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-108">In order to find minor differences for other country specific e-Invoice implementations, like Spanish or Italian, please refer to available WIKI articles.</span></span>



<span data-ttu-id="6e6fa-109">Før du kan udføre denne procedure, skal du udføre følgende procedurer: 'Importere elektroniske rapporteringskonfigurationer for elektronisk OIOUBL-fakturering', 'Konfigurere elektronisk OIOUBL-fakturering' og 'Konfigurere en debitorkonto til elektronisk OIOUBL-fakturering'.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-109">Before you can complete this procedure, you must complete the following procedures: ‘Import OIOUBL electronic invoicing electronic reporting configurations’, ‘Set up OIOUBL electronic invoicing’ and ‘Set up a customer account for OIOUBL electronic invoicing’.</span></span>


## <a name="update-a-project-contract"></a><span data-ttu-id="6e6fa-110">Opdater en projektkontrakt</span><span class="sxs-lookup"><span data-stu-id="6e6fa-110">Update a project contract</span></span>
1. <span data-ttu-id="6e6fa-111">Gå til Projektstyring og regnskab > Projekter > Projektkontrakter.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-111">Go to Project management and accounting > Projects > Project contracts.</span></span>
2. <span data-ttu-id="6e6fa-112">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-112">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6e6fa-113">Filtrer f.eks. efter feltet Projektkontrakt-id med værdien "000057".</span><span class="sxs-lookup"><span data-stu-id="6e6fa-113">For example, filter on the Project contract ID field with a value of '000057'.</span></span>
    * <span data-ttu-id="6e6fa-114">Vælg en projektkontrakt, der har en debitorfinansieringskilde, der er aktiveret til elektronisk fakturering.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-114">Select a project contract that has a customer funding source that is enabled for electronic invoicing.</span></span>  
3. <span data-ttu-id="6e6fa-115">Åbn detaljer for en projektkontrakt.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-115">Open details for a project contract.</span></span>
4. <span data-ttu-id="6e6fa-116">Udvid sektionen Finansieringskilder.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-116">Expand the Funding sources section.</span></span>
5. <span data-ttu-id="6e6fa-117">Klik på Detaljer.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-117">Click Details.</span></span>
6. <span data-ttu-id="6e6fa-118">Udvid afsnittet Andet.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-118">Expand the Other section.</span></span>
7. <span data-ttu-id="6e6fa-119">Skriv en værdi i feltet Debitorrekvisition.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-119">In the Customer requisition field, type a value.</span></span>
8. <span data-ttu-id="6e6fa-120">Skriv en værdi i feltet Kundereference.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-120">In the Customer reference field, type a value.</span></span>
9. <span data-ttu-id="6e6fa-121">Indtast eller vælg en værdi i feltet Kontakt-id.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-121">In the Contact ID field, enter or select a value.</span></span>
10. <span data-ttu-id="6e6fa-122">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-122">Click Save.</span></span>

## <a name="create-a-project-transaction"></a><span data-ttu-id="6e6fa-123">Opret en projekttransaktion</span><span class="sxs-lookup"><span data-stu-id="6e6fa-123">Create a project transaction</span></span>
1. <span data-ttu-id="6e6fa-124">Gå til Projektstyring og regnskab > Vareopgaver > Varebehov.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-124">Go to Project management and accounting > Item tasks > Item requirements.</span></span>
2. <span data-ttu-id="6e6fa-125">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-125">Click New.</span></span>
3. <span data-ttu-id="6e6fa-126">Indtast eller vælg en værdi i feltet Projekt-id.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-126">In the Project ID field, enter or select a value.</span></span>
    * <span data-ttu-id="6e6fa-127">Som et eksempel kan du bruge projekt-id '000057'.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-127">As an example, you may use '000057' project ID.</span></span>  
4. <span data-ttu-id="6e6fa-128">Indtast eller vælg en værdi i feltet Varenummer.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-128">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="6e6fa-129">Som et eksempel kan du bruge varenummer 'D0001'.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-129">As an example, you may use 'D0001' item number.</span></span>  
5. <span data-ttu-id="6e6fa-130">Klik på Administrer i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-130">On the Action Pane, click Manage.</span></span>
6. <span data-ttu-id="6e6fa-131">Klik på Bogføring.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-131">Click Posting.</span></span>
7. <span data-ttu-id="6e6fa-132">Klik på følgeseddel.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-132">Click Packing slip.</span></span>
8. <span data-ttu-id="6e6fa-133">Udvid sektionen Parametre.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-133">Expand the Parameters section.</span></span>
9. <span data-ttu-id="6e6fa-134">Vælg "Alle" i feltet Antal.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-134">In the Quantity field, select 'All'.</span></span>
10. <span data-ttu-id="6e6fa-135">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-135">Click OK.</span></span>
11. <span data-ttu-id="6e6fa-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-136">Click OK.</span></span>

## <a name="create-a-proposal-and-post-an-invoice"></a><span data-ttu-id="6e6fa-137">Oprette et forslag og bogføre en faktura</span><span class="sxs-lookup"><span data-stu-id="6e6fa-137">Create a proposal and post an invoice</span></span> 
1. <span data-ttu-id="6e6fa-138">Gå til Projektstyring og regnskab > Projektfakturaer > Projektfakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-138">Go to Project management and accounting > Project invoices > Project invoice proposals.</span></span>
2. <span data-ttu-id="6e6fa-139">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-139">Click New.</span></span>
3. <span data-ttu-id="6e6fa-140">Klik på Fakturaforslag.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-140">Click Invoice proposal.</span></span>
4. <span data-ttu-id="6e6fa-141">Indtast eller vælg en værdi i feltet Projekt.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-141">In the Project field, enter or select a value.</span></span>
5. <span data-ttu-id="6e6fa-142">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-142">Click OK.</span></span>
6. <span data-ttu-id="6e6fa-143">Klik på Bogfør.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-143">Click Post.</span></span>
7. <span data-ttu-id="6e6fa-144">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-144">Click OK.</span></span>
8. <span data-ttu-id="6e6fa-145">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-145">Click OK.</span></span>

## <a name="generate-an-oioubl-project-invoice"></a><span data-ttu-id="6e6fa-146">Oprette en OIOUBL projektfaktura</span><span class="sxs-lookup"><span data-stu-id="6e6fa-146">Generate an OIOUBL project invoice</span></span>
1. <span data-ttu-id="6e6fa-147">Gå til Projektstyring og regnskab > Projektfakturaer > Projektfakturaer.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-147">Go to Project management and accounting > Project invoices > Project invoices.</span></span>
2. <span data-ttu-id="6e6fa-148">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-148">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6e6fa-149">Filtrer f.eks. efter feltet Projektkontrakt-id med værdien "000057".</span><span class="sxs-lookup"><span data-stu-id="6e6fa-149">For example, filter on the Project contract ID field with a value of '000057'.</span></span>
3. <span data-ttu-id="6e6fa-150">Klik på Projektfaktura i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-150">On the Action Pane, click Project invoice.</span></span>
4. <span data-ttu-id="6e6fa-151">Klik på Send.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-151">Click Send.</span></span>
5. <span data-ttu-id="6e6fa-152">Klik på Oprindelig.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-152">Click Original.</span></span>

## <a name="view-an-oioubl-electronic-invoice"></a><span data-ttu-id="6e6fa-153">Se en elektronisk OIOUBL faktura</span><span class="sxs-lookup"><span data-stu-id="6e6fa-153">View an OIOUBL electronic invoice</span></span>
1. <span data-ttu-id="6e6fa-154">Gå til Virksomhedsadministration > Elektronisk rapportering > Elektroniske rapporteringsjob.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-154">Go to Organization administration > Electronic reporting > Electronic reporting jobs.</span></span>
2. <span data-ttu-id="6e6fa-155">Klik på Vis filer.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-155">Click Show files.</span></span>
3. <span data-ttu-id="6e6fa-156">Klik på Åbn.</span><span class="sxs-lookup"><span data-stu-id="6e6fa-156">Click Open.</span></span>

