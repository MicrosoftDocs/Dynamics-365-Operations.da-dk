---
title: Foretage fejlfinding af konfiguration af lagersted
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du konfigurerer Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 1dbd947f0740d22e0f79e6d5c272beb64715c8a5
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5814386"
---
# <a name="troubleshoot-warehouse-configuration"></a><span data-ttu-id="8ea0b-103">Foretage fejlfinding af konfiguration af lagersted</span><span class="sxs-lookup"><span data-stu-id="8ea0b-103">Troubleshoot warehouse configuration</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8ea0b-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du konfigurerer Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-104">This topic describes how to fix common issues that you might encounter while you configure Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-the-license-plate-or-location-is-not-valid"></a><span data-ttu-id="8ea0b-105">Jeg får vist følgende fejlmeddelelse: "Id'et eller lokationen er ikke gyldig".</span><span class="sxs-lookup"><span data-stu-id="8ea0b-105">I receive the following error message: "The license plate or location is not valid."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ea0b-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ea0b-106">Issue description</span></span>

<span data-ttu-id="8ea0b-107">Du får vist denne fejlmeddelelse, når du scanner et nummerplade-id eller en lokation.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-107">You receive this error message when you scan a license plate ID or location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ea0b-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8ea0b-108">Issue resolution</span></span>

<span data-ttu-id="8ea0b-109">Kontrollér, at nummerplade-id'et ikke er reserveret af noget andet.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-109">Make sure that the license plate ID isn't reserved by something else.</span></span> <span data-ttu-id="8ea0b-110">Dette problem opstod, når den værdi, som en bruger scannede i mobilappen Lokationsstyring, både var en gyldig lokation og et gyldigt nummerplade-id.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-110">This issue used to occur when the value that a user scanned in the Warehouse Management mobile app was both a valid location and a valid license plate ID.</span></span> <span data-ttu-id="8ea0b-111">Dette problem blev dog løst i version 10.0.11.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-111">However, this issue was resolved in version 10.0.11.</span></span>

## <a name="i-receive-the-following-error-message-license-plate-must-be-specified-for-this-location"></a><span data-ttu-id="8ea0b-112">Jeg får vist følgende fejlmeddelelse: "Id skal være angivet for denne lokation".</span><span class="sxs-lookup"><span data-stu-id="8ea0b-112">I receive the following error message: "License plate must be specified for this location."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ea0b-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ea0b-113">Issue description</span></span>

<span data-ttu-id="8ea0b-114">Du får vist denne fejlmeddelelse, hvis du opretter en flytteordre ved hjælp af et lagersted, der er aktiveret til avanceret lokationsstyring (WMS), og du derefter forsøger at bekræfte forsendelsen, efter at arbejdet er fuldført.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-114">You receive this error message if you create a transfer order by using a warehouse that is enabled for advanced warehouse management (WMS), and then, after the work is completed, you try to confirm the shipment.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ea0b-115">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8ea0b-115">Issue resolution</span></span>

<span data-ttu-id="8ea0b-116">Feltet **Standardtilgangslokation** er tomt for et transitlagersted i "fra"-lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-116">The **Default receipt location** field is blank for a transit warehouse of the "from" warehouse.</span></span> <span data-ttu-id="8ea0b-117">Du kan løse dette problem ved at angive en standardtilgangslokation på transitlagerstedet.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-117">To fix this issue, specify a default receipt location in the transit warehouse.</span></span> <span data-ttu-id="8ea0b-118">Kontrollér, at denne lokation er id-styret.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-118">Make sure that this location is license plate–controlled.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-work-template-line-for-inventory-status-change-because-the-work-type-is-not-valid-select-a-different-work-type"></a><span data-ttu-id="8ea0b-119">Jeg får vist følgende fejlmeddelelse: "Du kan ikke oprette en arbejdsskabelonlinje til ændring af lagerstatus, fordi arbejdstypen ikke er gyldig.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-119">I receive the following error message: "You can't create a work template line for Inventory status change because the work type is not valid.</span></span> <span data-ttu-id="8ea0b-120">Vælg en anden arbejdstype".</span><span class="sxs-lookup"><span data-stu-id="8ea0b-120">Select a different work type."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ea0b-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ea0b-121">Issue description</span></span>

<span data-ttu-id="8ea0b-122">I forbindelse med en arbejdsskabelon kan du ikke vælge *Ændring af lagerstatus* i kolonnen **Arbejdstype** i sektionen **Detaljer for arbejdsskabelon**.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-122">For a work template, you can't select *Inventory status change* in the **Work type** column of the **Work template details** section.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ea0b-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8ea0b-123">Issue resolution</span></span>

<span data-ttu-id="8ea0b-124">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-124">This behavior is by design.</span></span> <span data-ttu-id="8ea0b-125">Arbejdstypen *Ændring af lagerstatus* bruges kun i forbindelse med systemprocesser.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-125">The *Inventory status change* work type is used only by system processes.</span></span> <span data-ttu-id="8ea0b-126">Den kan ikke konfigureres.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-126">It can't be configured.</span></span> <span data-ttu-id="8ea0b-127">Da listen over arbejdstyper er fastlagt som en fasttekst, kan de ekstra poster ikke filtreres fra rullemenuen **Arbejdstype**.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-127">Because the list of work types is fixed as an enumeration, the extra entries can't be filtered out of the **Work type** drop-down menu.</span></span>

## <a name="i-receive-the-following-error-message-the-quantity-is-not-valid-for-unit-1"></a><span data-ttu-id="8ea0b-128">Jeg får vist følgende fejlmeddelelse: "Antallet er ikke gyldigt for enheden 1%".</span><span class="sxs-lookup"><span data-stu-id="8ea0b-128">I receive the following error message: "The Quantity is not valid for unit 1%."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ea0b-129">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ea0b-129">Issue description</span></span>

<span data-ttu-id="8ea0b-130">Antallet er ikke gyldigt for *hver*-enheden, når der er plukarbejde, der har flere id'er på én lokation.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-130">The quantity isn't valid for the *ea* unit when there is picking work that has multiple license plates in one location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ea0b-131">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8ea0b-131">Issue resolution</span></span>

<span data-ttu-id="8ea0b-132">Kontrollér, at felterne **Enhedsseriegruppe-id** og **Enhedsomregninger** på det frigivne produkt eller den frigivne produktvariant er angivet korrekt.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-132">Verify that the **Unit sequence group ID** and **Unit conversions** fields on the released product or product variant are set correctly.</span></span>

<span data-ttu-id="8ea0b-133">Bemærk, at fejlmeddelelsen er blevet forbedret i version 10.0.15 (se [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span><span class="sxs-lookup"><span data-stu-id="8ea0b-133">Note that the error message has been improved in version 10.0.15 (see [KB 4581627](https://fix.lcs.dynamics.com/Issue/Details/?bugId=486531)).</span></span> <span data-ttu-id="8ea0b-134">Den nye fejlmeddelelse er "Antallet er ikke gyldigt.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-134">The new error message is, "The quantity is not valid.</span></span> <span data-ttu-id="8ea0b-135">Forventede %1 %2".</span><span class="sxs-lookup"><span data-stu-id="8ea0b-135">Expected %1 %2."</span></span>

## <a name="in-location-directives-for-sales-order-put-work-the-multiple-sku-option-doesnt-evaluate-multiple-location-directive-actions"></a><span data-ttu-id="8ea0b-136">I lokationsvejledninger for salgsordres læg på lager-arbejde, evaluerer indstillingen for flere SKU'er ikke flere handlinger for lokationsvejledninger.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-136">In location directives for sales order put work, the multiple SKU option doesn't evaluate multiple location directive actions.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ea0b-137">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ea0b-137">Issue description</span></span>

<span data-ttu-id="8ea0b-138">Lokationsvejledninger for arbejdsordretypen *Salgsordrer* og arbejdstypen *Læg på lager* evaluerer ikke flere handlinger for lokationsvejledninger, når indstillingen **Flere SKU'er** er valgt.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-138">Location directives of the *Sales orders* work order type and the *Put* work type don't evaluate multiple location directive actions when the **Multiple SKU** option is selected.</span></span> <span data-ttu-id="8ea0b-139">Det er kun den første handling i lokationsvejledningen, der evalueres.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-139">Only the first location directive action is evaluated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ea0b-140">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8ea0b-140">Issue resolution</span></span>

<span data-ttu-id="8ea0b-141">En ny funktion, *Evaluer alle handlinger for lokationsvejledninger med flere SKU'er*, er blevet tilføjet i version 10.0.15 (se [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span><span class="sxs-lookup"><span data-stu-id="8ea0b-141">A new feature, *Evaluate all actions for Multi SKU location directives*, has been added in version 10.0.15 (see [KB 4579866](https://fix.lcs.dynamics.com/Issue/Details?kb=4579866&bugId=475946&dbType=3&qc=1bc41a56de7a3ee419fa76397a6bf282fce5be9b93e427c08a6d916d1dfa3091)).</span></span> <span data-ttu-id="8ea0b-142">Denne funktion evaluerer alle handlinger for lokationsvejledninger med flere SKU'er.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-142">This feature evaluates all actions for multi-SKU location directives.</span></span> <span data-ttu-id="8ea0b-143">Hvis du har brug for denne funktion, skal du bruge [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at aktivere den.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-143">If you require this feature, use [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) to turn it on.</span></span>

## <a name="i-cant-use-the-warehouse-management-mobile-app-to-do-partial-picking"></a><span data-ttu-id="8ea0b-144">Jeg kan ikke bruge mobilappen Lokationsstyring til at foretage en delvis plukning.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-144">I can't use the Warehouse Management mobile app to do partial picking.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ea0b-145">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ea0b-145">Issue description</span></span>

<span data-ttu-id="8ea0b-146">I forbindelse med salgs- og flytteordrer kan du ikke springe varer over og foretage delvis plukning.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-146">For sales and transfer orders, you can't skip items and do partial picking.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ea0b-147">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8ea0b-147">Issue resolution</span></span>

<span data-ttu-id="8ea0b-148">På siden **Menupunkter i mobilenhed** skal du for hvert menupunkt, der er konfigureret til at behandle salgsordrer eller flytteordrer, angive **Ja** for indstillingen **Tillad opdeling af arbejde** i oversigtspanelet *Generelt*.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-148">On the **Mobile device menu items** page, for each menu item that is set up to process sales orders or transfer orders, set the **Allow splitting of work** option on the **General** FastTab to *Yes*.</span></span>

## <a name="how-can-i-do-an-inventory-status-change-for-partial-quantity-work"></a><span data-ttu-id="8ea0b-149">Hvordan kan jeg foretage en ændring af lagerstatus for delmængdearbejde?</span><span class="sxs-lookup"><span data-stu-id="8ea0b-149">How can I do an inventory status change for partial quantity work?</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ea0b-150">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ea0b-150">Issue description</span></span>

<span data-ttu-id="8ea0b-151">Du vil foretage en ændring af lagerstatus for et delvist antal af en batch.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-151">You want to do an inventory status change for a partial quantity of a batch.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ea0b-152">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8ea0b-152">Issue resolution</span></span>

<span data-ttu-id="8ea0b-153">Hvis du vil give arbejdere mulighed for at foretage denne ændring, kan du oprette et menupunkt til mobilappen Lokationsstyring.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-153">To enable workers to make this change, you can create a menu item for the Warehouse Management mobile app.</span></span> <span data-ttu-id="8ea0b-154">Opret (eller rediger) et menupunkt med følgende indstillinger på siden **Menupunkter i mobilenhed**:</span><span class="sxs-lookup"><span data-stu-id="8ea0b-154">On the **Mobile device menu items** page, create (or edit) a menu item that has the following settings:</span></span>

- <span data-ttu-id="8ea0b-155">**Tilstand:** *Arbejde*</span><span class="sxs-lookup"><span data-stu-id="8ea0b-155">**Mode:** *Work*</span></span>
- <span data-ttu-id="8ea0b-156">**Brug eksisterende arbejde:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="8ea0b-156">**Use existing work:** *No*</span></span>
- <span data-ttu-id="8ea0b-157">**Arbejdsoprettelsesproces:** *Bevægelse*</span><span class="sxs-lookup"><span data-stu-id="8ea0b-157">**Work creation process:** *Movement*</span></span>
- <span data-ttu-id="8ea0b-158">**Vis lagerstatus:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="8ea0b-158">**Display inventory status:** *Yes*</span></span>

<span data-ttu-id="8ea0b-159">Angiv de resterende felter på siden efter behov.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-159">You can set other fields on the page as you require.</span></span>

## <a name="the-dock-management-profile-of-a-location-profile-is-not-preventing-inventory-types-from-being-mixed"></a><span data-ttu-id="8ea0b-160">En lokationsprofils dokstyringsprofil forhindrer ikke, at lagertyper blandes.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-160">The dock management profile of a location profile is not preventing inventory types from being mixed.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8ea0b-161">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ea0b-161">Issue description</span></span>

<span data-ttu-id="8ea0b-162">Du bruger *forsendelseskonsolideringspolitikker*.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-162">You are using *shipment consolidation policies*.</span></span> <span data-ttu-id="8ea0b-163">Du har konfigureret en *dokstyringsprofil* for en *lokationsprofil*, men når der oprettes arbejde, blandes lagertyperne på den endelige lokation.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-163">You have set up a *dock management profile* for a *location profile*, but when work is created, the inventory types are mixed at the final location.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8ea0b-164">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8ea0b-164">Issue resolution</span></span>

<span data-ttu-id="8ea0b-165">Profiler for dokstyring kræver, at arbejdet opdeles i forvejen.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-165">Dock management profiles require work to be split up front.</span></span> <span data-ttu-id="8ea0b-166">Med andre ord forventer dokstyringsprofilen, at der ikke vil være flere læg-lokationer i et arbejdshoved.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-166">In other words, the dock management profile expects that a work header won't have multiple put locations.</span></span>

<span data-ttu-id="8ea0b-167">For at dokstyringsprofilen kan håndtere blanding af lager effektivt, skal der konfigureres en pause i arbejdshovedet.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-167">For the dock management profile to effectively manage the mixing of inventory, a work header break must be set up.</span></span>

<span data-ttu-id="8ea0b-168">I dette eksempel er vores dokstyringsprofil konfigureret sådan, at **Lagertyper, der ikke skal blandes**, er angivet til *Forsendelses-id*, og vi konfigurerer en arbejdshovedpause for den:</span><span class="sxs-lookup"><span data-stu-id="8ea0b-168">In this example our dock management profile is configured such that **Inventory types that should not be mixed** is set to *Shipment ID*, and we'll set up a work header break for it:</span></span>

1. <span data-ttu-id="8ea0b-169">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-169">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="8ea0b-170">Vælg den **Arbejdsordretype**, der skal redigeres (f.eks. *Indkøbsordrer*).</span><span class="sxs-lookup"><span data-stu-id="8ea0b-170">Select the **Work order type** to edit (for example, *Purchase orders*).</span></span>
1. <span data-ttu-id="8ea0b-171">Vælg den arbejdsskabelon, du vil redigere.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-171">Select the work template to edit.</span></span>
1. <span data-ttu-id="8ea0b-172">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-172">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="8ea0b-173">Åbn fanen **Sortering**, og tilføj en række med følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="8ea0b-173">Open the **Sorting** tab and add a row with the following settings:</span></span>
    - <span data-ttu-id="8ea0b-174">**Tabel** - *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="8ea0b-174">**Table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="8ea0b-175">**Afledt tabel** - *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="8ea0b-175">**Derived table** - *Temporary work transactions*</span></span>
    - <span data-ttu-id="8ea0b-176">**Felt** - *Forsendelses-id*</span><span class="sxs-lookup"><span data-stu-id="8ea0b-176">**Field** - *Shipment ID*</span></span>
1. <span data-ttu-id="8ea0b-177">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-177">Select **OK**.</span></span>
1. <span data-ttu-id="8ea0b-178">Du vender tilbage til siden **Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-178">You return to the **Work templates** page.</span></span> <span data-ttu-id="8ea0b-179">Vælg **Opgaveoverskriften skifter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-179">On the Action Pane, select **Work header breaks**.</span></span>
1. <span data-ttu-id="8ea0b-180">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-180">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="8ea0b-181">Markér det afkrydsningsfelt, der er tilknyttet **Feltnavnet** *Forsendelses-id*.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-181">Select the check box associated with the **Field name** *Shipment ID*.</span></span>
1. <span data-ttu-id="8ea0b-182">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="8ea0b-182">On the Action Pane, select **Save**.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
