---
title: Foretage fejlfinding af konfiguration af lagersted
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du konfigurerer Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 09b5770190fea9591f422b61ce6deedb2b9fa790
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993997"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="bcd67-103">Foretage fejlfinding af konfiguration af lagersted</span><span class="sxs-lookup"><span data-stu-id="bcd67-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="bcd67-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du konfigurerer Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="bcd67-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="bcd67-105">Jeg får vist følgende fejlmeddelelse: "Id'et eller lokationen er ikke gyldig".</span><span class="sxs-lookup"><span data-stu-id="bcd67-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bcd67-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bcd67-106">Issue description</span></span>

<span data-ttu-id="bcd67-107">Du får vist denne fejlmeddelelse, når du scanner et nummerplade-id eller en lokation.</span><span class="sxs-lookup"><span data-stu-id="bcd67-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bcd67-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="bcd67-108">Issue resolution</span></span>

<span data-ttu-id="bcd67-109">Kontrollér, at nummerplade-id'et ikke er reserveret af noget andet.</span><span class="sxs-lookup"><span data-stu-id="bcd67-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="bcd67-110">Dette problem opstod, når den værdi, som en bruger scannede i lagerstedsappen, både var en gyldig lokation og et gyldigt nummerplade-id.</span><span class="sxs-lookup"><span data-stu-id="bcd67-110">This issue used to occur when the value that a user scanned in the warehouse app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="bcd67-111">Dette problem blev dog løst i version 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="bcd67-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="bcd67-112">Jeg får vist følgende fejlmeddelelse: "Id skal være angivet for denne lokation".</span><span class="sxs-lookup"><span data-stu-id="bcd67-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bcd67-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bcd67-113">Issue description</span></span>

<span data-ttu-id="bcd67-114">Du får vist denne fejlmeddelelse, hvis du opretter en flytteordre ved hjælp af et lagersted, der er aktiveret til avanceret lokationsstyring (WMS), og du derefter forsøger at bekræfte forsendelsen, efter at arbejdet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="bcd67-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bcd67-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="bcd67-115">Issue resolution</span></span>

<span data-ttu-id="bcd67-116">Feltet **Standardtilgangslokation** er tomt for et transitlagersted i "fra"-lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="bcd67-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="bcd67-117">Du kan løse dette problem ved at angive en standardtilgangslokation på transitlagerstedet.</span><span class="sxs-lookup"><span data-stu-id="bcd67-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="bcd67-118">Kontrollér, at denne lokation er id-styret.</span><span class="sxs-lookup"><span data-stu-id="bcd67-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="bcd67-119">Jeg får vist følgende fejlmeddelelse: "Du kan ikke oprette en arbejdsskabelonlinje til ændring af lagerstatus, fordi arbejdstypen ikke er gyldig.</span><span class="sxs-lookup"><span data-stu-id="bcd67-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="bcd67-120">Vælg en anden arbejdstype".</span><span class="sxs-lookup"><span data-stu-id="bcd67-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bcd67-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bcd67-121">Issue description</span></span>

<span data-ttu-id="bcd67-122">I forbindelse med en arbejdsskabelon kan du ikke vælge *Ændring af lagerstatus* i kolonnen **Arbejdstype** i sektionen **Detaljer for arbejdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="bcd67-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bcd67-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="bcd67-123">Issue resolution</span></span>

<span data-ttu-id="bcd67-124">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="bcd67-124">This behavior is by design.</span></span> <span data-ttu-id="bcd67-125">Arbejdstypen *Ændring af lagerstatus* bruges kun i forbindelse med systemprocesser.</span><span class="sxs-lookup"><span data-stu-id="bcd67-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="bcd67-126">Den kan ikke konfigureres.</span><span class="sxs-lookup"><span data-stu-id="bcd67-126">It can't be configured.</span></span> <span data-ttu-id="bcd67-127">Da listen over arbejdstyper er fastlagt som en fasttekst, kan de ekstra poster ikke filtreres fra rullemenuen **Arbejdstype**.</span><span class="sxs-lookup"><span data-stu-id="bcd67-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="bcd67-128">Jeg får vist følgende fejlmeddelelse: "Antallet er ikke gyldigt for enheden 1%".</span><span class="sxs-lookup"><span data-stu-id="bcd67-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="bcd67-129">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bcd67-129">Issue description</span></span>

<span data-ttu-id="bcd67-130">Antallet er ikke gyldigt for *hver*-enheden, når der er plukarbejde, der har flere id'er på én lokation.</span><span class="sxs-lookup"><span data-stu-id="bcd67-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bcd67-131">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="bcd67-131">Issue resolution</span></span>

<span data-ttu-id="bcd67-132">Kontrollér, at felterne **Enhedsseriegruppe-id** og **Enhedsomregninger** på det frigivne produkt eller den frigivne produktvariant er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="bcd67-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="bcd67-133">Bemærk, at fejlmeddelelsen er blevet forbedret i version 10.0.15 (se [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="bcd67-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="bcd67-134">Den nye fejlmeddelelse er "Antallet er ikke gyldigt.</span><span class="sxs-lookup"><span data-stu-id="bcd67-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="bcd67-135">Forventede %1 %2".</span><span class="sxs-lookup"><span data-stu-id="bcd67-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="bcd67-136">I lokationsvejledninger for salgsordres læg på lager-arbejde, evaluerer indstillingen for flere SKU'er ikke flere handlinger for lokationsvejledninger.</span><span class="sxs-lookup"><span data-stu-id="bcd67-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bcd67-137">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bcd67-137">Issue description</span></span>

<span data-ttu-id="bcd67-138">Lokationsvejledninger for arbejdsordretypen *Salgsordrer* og arbejdstypen *Læg på lager* evaluerer ikke flere handlinger for lokationsvejledninger, når indstillingen **Flere SKU'er** er valgt.</span><span class="sxs-lookup"><span data-stu-id="bcd67-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="bcd67-139">Det er kun den første handling i lokationsvejledningen, der evalueres.</span><span class="sxs-lookup"><span data-stu-id="bcd67-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bcd67-140">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="bcd67-140">Issue resolution</span></span>

<span data-ttu-id="bcd67-141">En ny funktion, *Evaluer alle handlinger for lokationsvejledninger med flere SKU'er*, er blevet tilføjet i version 10.0.15 (se [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="bcd67-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="bcd67-142">Denne funktion evaluerer alle handlinger for lokationsvejledninger med flere SKU'er.</span><span class="sxs-lookup"><span data-stu-id="bcd67-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="bcd67-143">Hvis du har brug for denne funktion, skal du bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere den.</span><span class="sxs-lookup"><span data-stu-id="bcd67-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-app-to-do-partial-picking"></a><span data-ttu-id="bcd67-144">Jeg kan ikke bruge lagerstedsappen til at foretage en delvis plukning.</span><span class="sxs-lookup"><span data-stu-id="bcd67-144">I can't use the warehouse app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="bcd67-145">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bcd67-145">Issue description</span></span>

<span data-ttu-id="bcd67-146">I forbindelse med salgs- og flytteordrer kan du ikke springe varer over og foretage delvis plukning.</span><span class="sxs-lookup"><span data-stu-id="bcd67-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bcd67-147">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="bcd67-147">Issue resolution</span></span>

<span data-ttu-id="bcd67-148">På siden **Menupunkter i mobilenhed** skal du for hvert menupunkt, der er konfigureret til at behandle salgsordrer eller flytteordrer, angive **Ja** for indstillingen **Tillad opdeling af arbejde** i oversigtspanelet *Generelt*.</span><span class="sxs-lookup"><span data-stu-id="bcd67-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="bcd67-149">Hvordan kan jeg foretage en ændring af lagerstatus for delmængdearbejde?</span><span class="sxs-lookup"><span data-stu-id="bcd67-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="bcd67-150">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="bcd67-150">Issue description</span></span>

<span data-ttu-id="bcd67-151">Du vil foretage en ændring af lagerstatus for et delvist antal af en batch.</span><span class="sxs-lookup"><span data-stu-id="bcd67-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="bcd67-152">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="bcd67-152">Issue resolution</span></span>

<span data-ttu-id="bcd67-153">Hvis du vil give arbejdere mulighed for at foretage denne ændring, kan du oprette et menupunkt til lagerstedsappen.</span><span class="sxs-lookup"><span data-stu-id="bcd67-153">To enable workers to make this change, you can create a menu item for the warehouse app.</span></span> <span data-ttu-id="bcd67-154">Opret (eller rediger) et menupunkt med følgende indstillinger på siden **Menupunkter i mobilenhed**:</span><span class="sxs-lookup"><span data-stu-id="bcd67-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="bcd67-155">**Tilstand:** *Arbejde*</span><span class="sxs-lookup"><span data-stu-id="bcd67-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="bcd67-156">**Brug eksisterende arbejde:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="bcd67-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="bcd67-157">**Arbejdsoprettelsesproces:** *Bevægelse*</span><span class="sxs-lookup"><span data-stu-id="bcd67-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="bcd67-158">**Vis lagerstatus:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="bcd67-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="bcd67-159">Angiv de resterende felter på siden efter behov.</span><span class="sxs-lookup"><span data-stu-id="bcd67-159">You can set other fields on the page as you require.</span></span>
