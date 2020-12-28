---
title: Konfigurere elektronisk OIOUBL-fakturering
description: Denne procedure gennemgår, hvordan du konfigurerer elektronisk OIOUBL fakturering.
author: mrolecki
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CustParameters, OMLegalEntity, UnitOfMeasure, ExtCodeTable
audience: Application User
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.search.region: Denmark
ms.author: mrolecki
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6930b0edd41afa551611a5d1e96c904093cd9778
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4407687"
---
# <a name="set-up-oioubl-electronic-invoicing"></a><span data-ttu-id="cea23-103">Konfigurere elektronisk OIOUBL-fakturering</span><span class="sxs-lookup"><span data-stu-id="cea23-103">Set up OIOUBL electronic invoicing</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="cea23-104">Denne procedure gennemgår, hvordan du konfigurerer elektronisk OIOUBL fakturering.</span><span class="sxs-lookup"><span data-stu-id="cea23-104">This procedure walks you through setting up OIOUBL electronic invoicing.</span></span> 



<span data-ttu-id="cea23-105">Denne opgave blev oprettet ved hjælp af demodatafirmaet USMF med landet/området i den juridiske enheds primære adresse opdateret til Danmark.</span><span class="sxs-lookup"><span data-stu-id="cea23-105">This task was created using the demo data company USMF with the country/region of legal entity primary address updated to Denmark.</span></span>



<span data-ttu-id="cea23-106">Det er den anden af seks procedurer, der viser processen til oprettelse af e-fakturaer ved hjælp af elektroniske rapporteringskonfigurationer.</span><span class="sxs-lookup"><span data-stu-id="cea23-106">This is the second procedure, out of six, that demonstrates the process of generating e-invoices using electronic reporting configurations.</span></span> <span data-ttu-id="cea23-107">Denne opgave bruger eksemplet med OIOUBL-e-fakturaen, der er fælles for Danmark, Østrig og Norge.</span><span class="sxs-lookup"><span data-stu-id="cea23-107">This task uses the OIOUBL e-invoice example, which is common for Denmark, Austria, and Norway.</span></span>

<span data-ttu-id="cea23-108">Før du kan udføre denne opgave, skal du importere elektroniske rapporteringskonfigurationer for elektronisk OIOUBL-fakturering.</span><span class="sxs-lookup"><span data-stu-id="cea23-108">Before you can complete this task, you must import the OIOUBL electronic invoicing electronic reporting configurations.</span></span>


## <a name="set-up-electronic-invoice-formats"></a><span data-ttu-id="cea23-109">Angive formater for elektroniske fakturaer</span><span class="sxs-lookup"><span data-stu-id="cea23-109">Set up electronic invoice formats</span></span>
1. <span data-ttu-id="cea23-110">Gå til Debitor > Opsætning > Debitorparametre.</span><span class="sxs-lookup"><span data-stu-id="cea23-110">Go to Accounts receivable > Setup > Accounts receivable parameters.</span></span>
2. <span data-ttu-id="cea23-111">Klik på fanen Elektroniske dokumenter.</span><span class="sxs-lookup"><span data-stu-id="cea23-111">Click the Electronic documents tab.</span></span>
3. <span data-ttu-id="cea23-112">Udvid sektionen Elektronisk rapportering.</span><span class="sxs-lookup"><span data-stu-id="cea23-112">Expand the Electronic reporting section.</span></span>
4. <span data-ttu-id="cea23-113">I feltet Salgs- og fritekstfaktura skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="cea23-113">In the Sales and Free text invoice field, enter or select a value.</span></span>
    * <span data-ttu-id="cea23-114">Vælg det format for elektronisk rapportering, der repræsenterer det ønskede dokument.</span><span class="sxs-lookup"><span data-stu-id="cea23-114">Choose the electronic reporting format that represents the required document.</span></span> <span data-ttu-id="cea23-115">Du kan have forskellige formatkonfigurationer for de enkelte dokumenttyper eller én konfiguration for alle dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="cea23-115">You might have separate format configurations per document type or one configuration for all document types.</span></span>  
5. <span data-ttu-id="cea23-116">I feltet Salgs- og fritekstkreditnota skal du angive eller vælge en værdi.</span><span class="sxs-lookup"><span data-stu-id="cea23-116">In the Sales and Free text credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="cea23-117">Vælg det format for elektronisk rapportering, der repræsenterer det ønskede dokument.</span><span class="sxs-lookup"><span data-stu-id="cea23-117">Choose the electronic reporting format that represents the required document.</span></span> <span data-ttu-id="cea23-118">Du kan have forskellige formatkonfigurationer for de enkelte dokumenttyper eller én konfiguration for alle dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="cea23-118">You might have separate format configurations per document type or one configuration for all document types.</span></span>  
6. <span data-ttu-id="cea23-119">Indtast eller vælg en værdi i feltet Projektfaktura.</span><span class="sxs-lookup"><span data-stu-id="cea23-119">In the Project invoice field, enter or select a value.</span></span>
    * <span data-ttu-id="cea23-120">Vælg det format for elektronisk rapportering, der repræsenterer det ønskede dokument.</span><span class="sxs-lookup"><span data-stu-id="cea23-120">Choose the electronic reporting format that represents the required document.</span></span> <span data-ttu-id="cea23-121">Du kan have forskellige formatkonfigurationer for de enkelte dokumenttyper eller én konfiguration for alle dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="cea23-121">You might have separate format configurations per document type or one configuration for all document types.</span></span>  
7. <span data-ttu-id="cea23-122">Indtast eller vælg en værdi i feltet Projektkreditnota.</span><span class="sxs-lookup"><span data-stu-id="cea23-122">In the Project credit note field, enter or select a value.</span></span>
    * <span data-ttu-id="cea23-123">Vælg det format for elektronisk rapportering, der repræsenterer det ønskede dokument.</span><span class="sxs-lookup"><span data-stu-id="cea23-123">Choose the electronic reporting format that represents the required document.</span></span> <span data-ttu-id="cea23-124">Du kan have forskellige formatkonfigurationer for de enkelte dokumenttyper eller én konfiguration for alle dokumenttyper.</span><span class="sxs-lookup"><span data-stu-id="cea23-124">You might have separate format configurations per document type or one configuration for all document types.</span></span>  
8. <span data-ttu-id="cea23-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cea23-125">Click Save.</span></span>

## <a name="set-up-a-legal-entity"></a><span data-ttu-id="cea23-126">Konfigurer en juridisk enhed</span><span class="sxs-lookup"><span data-stu-id="cea23-126">Set up a legal entity</span></span>
1. <span data-ttu-id="cea23-127">Gå til Virksomhedsadministration > Organisationer > Juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="cea23-127">Go to Organization administration > Organizations > Legal entities.</span></span>
2. <span data-ttu-id="cea23-128">Klik på Rediger.</span><span class="sxs-lookup"><span data-stu-id="cea23-128">Click Edit.</span></span>
3. <span data-ttu-id="cea23-129">Udvid sektionen Bankkontooplysninger.</span><span class="sxs-lookup"><span data-stu-id="cea23-129">Expand the Bank account information section.</span></span>
4. <span data-ttu-id="cea23-130">Skriv en værdi i feltet Registreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="cea23-130">In the Routing number field, type a value.</span></span>
    * <span data-ttu-id="cea23-131">Indtast for eksempel 12070918.</span><span class="sxs-lookup"><span data-stu-id="cea23-131">For example, enter 12070918.</span></span>  
5. <span data-ttu-id="cea23-132">Udvid sektionen Momsregistrering.</span><span class="sxs-lookup"><span data-stu-id="cea23-132">Expand the Tax registration section.</span></span>
6. <span data-ttu-id="cea23-133">Skriv en værdi i feltet Momsregistreringsnummer.</span><span class="sxs-lookup"><span data-stu-id="cea23-133">In the Tax registration number field, type a value.</span></span>
    * <span data-ttu-id="cea23-134">Indtast for eksempel 55568510.</span><span class="sxs-lookup"><span data-stu-id="cea23-134">For example, enter 55568510.</span></span>  

## <a name="set-up-external-codes-for-units-of-measure"></a><span data-ttu-id="cea23-135">Definere eksterne koder for måleenheder</span><span class="sxs-lookup"><span data-stu-id="cea23-135">Set up external codes for units of measure</span></span>
1. <span data-ttu-id="cea23-136">Gå til Virksomhedsadministration > Konfiguration > Enheder > Enheder.</span><span class="sxs-lookup"><span data-stu-id="cea23-136">Go to Organization administration > Setup > Units > Units.</span></span>
2. <span data-ttu-id="cea23-137">Brug Quick Filter til at finde poster.</span><span class="sxs-lookup"><span data-stu-id="cea23-137">Use the Quick Filter to find records.</span></span> <span data-ttu-id="cea23-138">For eksempel kan du filtrere på feltet Enhed med værdien 'pcs'.</span><span class="sxs-lookup"><span data-stu-id="cea23-138">For example, filter on the Unit field with a value of 'pcs'.</span></span>
3. <span data-ttu-id="cea23-139">Klik på Eksterne koder.</span><span class="sxs-lookup"><span data-stu-id="cea23-139">Click External codes.</span></span>
4. <span data-ttu-id="cea23-140">Markér den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="cea23-140">In the list, mark the selected row.</span></span>
5. <span data-ttu-id="cea23-141">Skriv en værdi i feltet Kode.</span><span class="sxs-lookup"><span data-stu-id="cea23-141">In the Code field, type a value.</span></span>
    * <span data-ttu-id="cea23-142">Skriv f.eks. PCSEA.</span><span class="sxs-lookup"><span data-stu-id="cea23-142">For example, enter PCSEA.</span></span>  
6. <span data-ttu-id="cea23-143">Indtast en værdi i feltet Ekstern kodedefinition.</span><span class="sxs-lookup"><span data-stu-id="cea23-143">In the External code definition field, type a value.</span></span> <span data-ttu-id="cea23-144">For eksempel OIOUBL EA-kode.</span><span class="sxs-lookup"><span data-stu-id="cea23-144">For example, OIOUBL EA code..</span></span>
7. <span data-ttu-id="cea23-145">Marker afkrydsningsfeltet Standardkode.</span><span class="sxs-lookup"><span data-stu-id="cea23-145">Select the Standard code check box.</span></span>
8. <span data-ttu-id="cea23-146">Klik på Tilføj.</span><span class="sxs-lookup"><span data-stu-id="cea23-146">Click Add.</span></span>
9. <span data-ttu-id="cea23-147">Skriv en værdi i feltet Værdi.</span><span class="sxs-lookup"><span data-stu-id="cea23-147">In the Value field, type a value.</span></span>
    * <span data-ttu-id="cea23-148">Skriv f.eks. EA.</span><span class="sxs-lookup"><span data-stu-id="cea23-148">For example, enter EA.</span></span>  
10. <span data-ttu-id="cea23-149">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="cea23-149">Click Save.</span></span>

