---
title: Fakturere for vedligeholdelse af aktiver, der ejes af kunder
description: Dette emne indeholder en forklaring på, hvordan du kan oprette, behandle og fakturere vedligeholdelsesarbejde, der udføres på aktiver, som dine kunder ejer.
author: johanhoffmann
manager: tfehr
ms.date: 01/28/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EntAssetWorkOrderProjCostInfoPart
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: johanho
ms.search.validFrom: 2021-01-28
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 643e59f082949ed51ab61d79648a98b83a7f0b03
ms.sourcegitcommit: 1e615288db245f83c5d5e0cd45315400f8946beb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/08/2021
ms.locfileid: "5131835"
---
# <a name="bill-for-maintenance-on-customer-owned-assets"></a><span data-ttu-id="70952-103">Fakturere for vedligeholdelse af aktiver, der ejes af kunder</span><span class="sxs-lookup"><span data-stu-id="70952-103">Bill for maintenance on customer-owned assets</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="70952-104">Med funktionen *Fakturering af arbejdsordre* kan du oprette, behandle og fakturere vedligeholdelsesarbejde på aktiver, som dine kunder ejer.</span><span class="sxs-lookup"><span data-stu-id="70952-104">The *Work order billing* feature lets you create, process, and bill maintenance work that is done on assets that your customers own.</span></span> <span data-ttu-id="70952-105">Du kan udføre følgende opgaver med denne funktion:</span><span class="sxs-lookup"><span data-stu-id="70952-105">This feature lets you perform the following tasks:</span></span>

- <span data-ttu-id="70952-106">Knytte kunder til de aktiver, de ejer.</span><span class="sxs-lookup"><span data-stu-id="70952-106">Connect customers to the assets that they own.</span></span>
- <span data-ttu-id="70952-107">Vælg en kunde, og se de aktiver, som kunden ejer, når du opretter en arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="70952-107">Select a customer and view the assets that customer owns when you create a work order.</span></span>
- <span data-ttu-id="70952-108">Konfigurer et overordnet projekt for hver kunde.</span><span class="sxs-lookup"><span data-stu-id="70952-108">Set up a parent project for each customer.</span></span>
- <span data-ttu-id="70952-109">Registrer timer, varer, udgifter og gebyrer på arbejdsordren, og opret derefter et fakturaforslag til kunden senere.</span><span class="sxs-lookup"><span data-stu-id="70952-109">Register hours, items, expenses, and fees against the work order, and then create an invoice proposal for the customer later.</span></span>

<span data-ttu-id="70952-110">Funktionen har desuden følgende egenskaber:</span><span class="sxs-lookup"><span data-stu-id="70952-110">In addition, the feature provides the following functionality:</span></span>

- <span data-ttu-id="70952-111">Projektkontrakten fra en kundes overordnede projekt kopieres automatisk til det relevante arbejdsordreprojekt.</span><span class="sxs-lookup"><span data-stu-id="70952-111">The project contract from a customer's parent project is automatically copied to the relevant work order project.</span></span>
- <span data-ttu-id="70952-112">Aktivstyring kan nu bruge projekttransaktionstypen *Gebyr* i både prognoser for arbejdsordrer og arbejdsordrekladder.</span><span class="sxs-lookup"><span data-stu-id="70952-112">Asset management can now use the *fee* project transaction type on both work order forecasts and work order journals.</span></span>

## <a name="turn-on-the-customer-billing-feature"></a><span data-ttu-id="70952-113">Slå funktionen for kundefakturering til</span><span class="sxs-lookup"><span data-stu-id="70952-113">Turn on the customer billing feature</span></span>

<span data-ttu-id="70952-114">Før du kan bruge denne funktion, skal den være slået til i dit system.</span><span class="sxs-lookup"><span data-stu-id="70952-114">Before you can use this feature, it must be turned on in your system.</span></span> <span data-ttu-id="70952-115">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til.</span><span class="sxs-lookup"><span data-stu-id="70952-115">Admins can use the [feature management](../../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the feature and turn it on.</span></span> <span data-ttu-id="70952-116">I arbejdsområdet **Funktionsstyring** vises funktionen på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="70952-116">In the **Feature management** workspace, the feature is listed in the following way:</span></span>

- <span data-ttu-id="70952-117">**Modul:** *Projektstyring og regnskab*</span><span class="sxs-lookup"><span data-stu-id="70952-117">**Module:** *Project management and accounting*</span></span>
- <span data-ttu-id="70952-118">**Funktionsnavn:** *Fakturering af arbejdsordre*</span><span class="sxs-lookup"><span data-stu-id="70952-118">**Feature name:** *Work order billing*</span></span>

## <a name="example-scenario"></a><span data-ttu-id="70952-119">Eksempelscenario</span><span class="sxs-lookup"><span data-stu-id="70952-119">Example scenario</span></span>

<span data-ttu-id="70952-120">Du kan få mere at vide om, hvordan funktionen fungerer, ved at følge nedenstående eksempelscenarie.</span><span class="sxs-lookup"><span data-stu-id="70952-120">To learn how this feature works, work through the following example scenario.</span></span>

<span data-ttu-id="70952-121">Hvis du vil arbejde gennem dette scenarie ved hjælp af de eksempelposter og -værdier, der er angivet her, skal du være på et system, hvor [standarddemodataene](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) er installeret.</span><span class="sxs-lookup"><span data-stu-id="70952-121">To work through this scenario by using the sample records and values that are specified here, you must be on a system where the standard [demo data](../../../fin-ops-core/dev-itpro/deployment/deploy-demo-environment.md) is installed.</span></span> <span data-ttu-id="70952-122">Du skal vælge den juridiske enhed **USMF**, før du starter.</span><span class="sxs-lookup"><span data-stu-id="70952-122">You must select the **USMF** legal entity before you begin.</span></span>

<span data-ttu-id="70952-123">Du kan også bruge dette scenarie som vejledning til brug af funktionen, når du arbejder i et produktionssystem.</span><span class="sxs-lookup"><span data-stu-id="70952-123">You can also use this scenario as guidance for using the feature when you work on a production system.</span></span> <span data-ttu-id="70952-124">Du skal dog i det tilfælde erstatte dine egne værdier, og du mangler muligvis nogle typer påkrævede poster, som standarddemodataene giver.</span><span class="sxs-lookup"><span data-stu-id="70952-124">However, in that case, you must substitute your own values, and you might be missing some types of required records that the standard demo data provides.</span></span>

### <a name="step-1-create-a-new-project-contract-for-the-customer"></a><span data-ttu-id="70952-125">Trin 1: Opret en ny projektkontrakt for kunden</span><span class="sxs-lookup"><span data-stu-id="70952-125">Step 1: Create a new project contract for the customer</span></span>

1. <span data-ttu-id="70952-126">Gå til **Projektstyring og regnskab \> Projekter \> Projektkontrakter**.</span><span class="sxs-lookup"><span data-stu-id="70952-126">Go to **Project management and accounting \> Projects \> Project contracts**.</span></span>
1. <span data-ttu-id="70952-127">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="70952-127">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70952-128">Angiv følgende værdier i dialogboksen **Ny projektkontrakt**:</span><span class="sxs-lookup"><span data-stu-id="70952-128">In the **New project contract** dialog box, set the following values:</span></span>

    - <span data-ttu-id="70952-129">**Navn:** *Pelican Wholesales*</span><span class="sxs-lookup"><span data-stu-id="70952-129">**Name:** *Pelican Wholesales*</span></span>
    - <span data-ttu-id="70952-130">**Finansieringstype:** *Kunde*</span><span class="sxs-lookup"><span data-stu-id="70952-130">**Funding type:** *Customer*</span></span>
    - <span data-ttu-id="70952-131">**Finansieringskilde:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="70952-131">**Funding source:** *US-013* (*Pelican Wholesales*)</span></span>

1. <span data-ttu-id="70952-132">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="70952-132">Select **OK**.</span></span>

### <a name="step-2-create-a-new-parent-project-for-the-customer"></a><span data-ttu-id="70952-133">Trin 2: Opret et nyt overordnet projekt for kunden</span><span class="sxs-lookup"><span data-stu-id="70952-133">Step 2: Create a new parent project for the customer</span></span>

<span data-ttu-id="70952-134">Det overordnede projekt, som du opretter her, bruges, når der oprettes arbejdsordrer for kunden.</span><span class="sxs-lookup"><span data-stu-id="70952-134">The parent project that you create here will be used when work orders for the customer are created.</span></span>

1. <span data-ttu-id="70952-135">Gå til **Projektstyring og regnskab \> Projekter \> Alle projekter**.</span><span class="sxs-lookup"><span data-stu-id="70952-135">Go to **Project management and accounting \> Projects \> All projects**.</span></span>
1. <span data-ttu-id="70952-136">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="70952-136">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70952-137">Angiv følgende værdier i dialogboksen **Nyt projekt**:</span><span class="sxs-lookup"><span data-stu-id="70952-137">In the **New project** dialog box, set the following values:</span></span>

    - <span data-ttu-id="70952-138">**Projekttype:** *Tid og materialer*</span><span class="sxs-lookup"><span data-stu-id="70952-138">**Project type:** *Time and material*</span></span>
    - <span data-ttu-id="70952-139">**Projektnavn:** *Pelican Wholesales-arbejdsordrer*</span><span class="sxs-lookup"><span data-stu-id="70952-139">**Project name:** *Pelican Wholesales work orders*</span></span>
    - <span data-ttu-id="70952-140">**Projektgruppe:** *TM*</span><span class="sxs-lookup"><span data-stu-id="70952-140">**Project group:** *TM*</span></span>
    - <span data-ttu-id="70952-141">**Projektkontrakt-id:** *Pelican Wholesales* (den kontrakt, du oprettede tidligere)</span><span class="sxs-lookup"><span data-stu-id="70952-141">**Project contract ID:** *Pelican Wholesales* (the contract that you created earlier)</span></span>
    - <span data-ttu-id="70952-142">**Startdato:** Vælg dags dato.</span><span class="sxs-lookup"><span data-stu-id="70952-142">**Start date:** Select today's date.</span></span>

1. <span data-ttu-id="70952-143">Vælg **Opret projekt**.</span><span class="sxs-lookup"><span data-stu-id="70952-143">Select **Create project**.</span></span>
1. <span data-ttu-id="70952-144">Det nye projekt åbnes.</span><span class="sxs-lookup"><span data-stu-id="70952-144">The new project is opened.</span></span> <span data-ttu-id="70952-145">Notér dig værdien af **Projekt-id**.</span><span class="sxs-lookup"><span data-stu-id="70952-145">Make a note of the **Project ID** value.</span></span> <span data-ttu-id="70952-146">Du skal angive det senere.</span><span class="sxs-lookup"><span data-stu-id="70952-146">You will have to enter it later.</span></span>

### <a name="step-3-create-a-new-work-order-type-in-asset-management"></a><span data-ttu-id="70952-147">Trin 3: Opret en ny arbejdsordretype i Aktivstyring</span><span class="sxs-lookup"><span data-stu-id="70952-147">Step 3: Create a new work order type in Asset management</span></span>

1. <span data-ttu-id="70952-148">Gå til **Styring af aktiver \> Opsætning \> Arbejdsordre \> Arbejdsordretyper**.</span><span class="sxs-lookup"><span data-stu-id="70952-148">Go to **Asset management \> Setup \> Work order \> Work order types**.</span></span>
1. <span data-ttu-id="70952-149">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="70952-149">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70952-150">Der føjes en ny post til listen.</span><span class="sxs-lookup"><span data-stu-id="70952-150">A new record is added to the list.</span></span> <span data-ttu-id="70952-151">Angiv følgende værdier for den:</span><span class="sxs-lookup"><span data-stu-id="70952-151">Set the following values for it:</span></span>

    - <span data-ttu-id="70952-152">**Arbejdsordretype:** *Service*</span><span class="sxs-lookup"><span data-stu-id="70952-152">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="70952-153">**Navn:** *Servicearbejdsordrer*</span><span class="sxs-lookup"><span data-stu-id="70952-153">**Name:** *Service work orders*</span></span>
    - <span data-ttu-id="70952-154">**Livscyklustilstand for arbejdsordre:** *Standard*</span><span class="sxs-lookup"><span data-stu-id="70952-154">**Work order lifecycle state:** *Standard*</span></span>

### <a name="step-4-link-the-customer-account-to-the-parent-project"></a><span data-ttu-id="70952-155">Trin 4: Knyt kundekontoen til det overordnede projekt</span><span class="sxs-lookup"><span data-stu-id="70952-155">Step 4: Link the customer account to the parent project</span></span>

<span data-ttu-id="70952-156">Du skal nu knytte kundekontoen til det overordnede projekt i projektopsætningen i Aktivstyring.</span><span class="sxs-lookup"><span data-stu-id="70952-156">You must now link the customer account to the parent project in the project setup in Asset management.</span></span>

1. <span data-ttu-id="70952-157">Gå til **Styring af aktiver \> Opsætning \> Arbejdsordrer \> Opsætning af projekt**.</span><span class="sxs-lookup"><span data-stu-id="70952-157">Go to **Asset management \> Setup \> Work orders \> Project setup**.</span></span>
1. <span data-ttu-id="70952-158">På fanen **Overordnet projekt** skal du vælge **Tilføj** for at tilføje en ny linje.</span><span class="sxs-lookup"><span data-stu-id="70952-158">On the **Parent project** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="70952-159">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="70952-159">On the new line, set the following values:</span></span>

    - <span data-ttu-id="70952-160">**Debitorkonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="70952-160">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="70952-161">**Projekt-id:** Angiv det projekt-id, du har noteret tidligere.</span><span class="sxs-lookup"><span data-stu-id="70952-161">**Project ID:** Enter the project ID that you made a note of earlier.</span></span>

### <a name="step-5-link-the-project-group-and-type-to-the-work-order-project"></a><span data-ttu-id="70952-162">Trin 5: Knyt projektgruppen og typen til arbejdsordreprojektet</span><span class="sxs-lookup"><span data-stu-id="70952-162">Step 5: Link the project group and type to the work order project</span></span>

<span data-ttu-id="70952-163">Du bør stadig være på siden **Opsætning af Projekt** (**Styring af aktiver \> Opsætning \> Arbejdsordrer \> Opsætning af Projekt**).</span><span class="sxs-lookup"><span data-stu-id="70952-163">You should still be on the **Project setup** page (**Asset management \> Setup \> Work orders \> Project setup**).</span></span>

1. <span data-ttu-id="70952-164">På fanen **Projektgruppe** skal du vælge **Tilføj** for at tilføje en ny linje.</span><span class="sxs-lookup"><span data-stu-id="70952-164">On the **Project group** tab, select **Add** to add a line.</span></span>
1. <span data-ttu-id="70952-165">Angiv følgende værdier på den nye linje:</span><span class="sxs-lookup"><span data-stu-id="70952-165">On the new line, set the following values:</span></span>

    - <span data-ttu-id="70952-166">**Arbejdsordretype:** *Service* (den arbejdsordretype, du oprettede tidligere)</span><span class="sxs-lookup"><span data-stu-id="70952-166">**Work order type:** *Service* (the work order type that you created earlier)</span></span>
    - <span data-ttu-id="70952-167">**Projektgruppe:** *TM*</span><span class="sxs-lookup"><span data-stu-id="70952-167">**Project group:** *TM*</span></span>

> [!NOTE]
> <span data-ttu-id="70952-168">Projektkontrakten på arbejdsordreprojektet nedarves altid fra det overordnede projekt.</span><span class="sxs-lookup"><span data-stu-id="70952-168">The project contract on the work order project is always inherited from the parent project.</span></span>

### <a name="step-6-link-an-asset-to-the-customer-id"></a><span data-ttu-id="70952-169">Trin 6: Knyt et aktiv til kunde-id'et</span><span class="sxs-lookup"><span data-stu-id="70952-169">Step 6: Link an asset to the customer ID</span></span>

1. <span data-ttu-id="70952-170">Gå til **Styring af aktiver \> Aktiver \> Alle aktiver**.</span><span class="sxs-lookup"><span data-stu-id="70952-170">Go to **Asset management \> Assets \> Active assets**.</span></span>
1. <span data-ttu-id="70952-171">Angiv **VE-102** i feltet *Filter*, og vælg at filtrere efter **Aktiv**.</span><span class="sxs-lookup"><span data-stu-id="70952-171">In the **Filter** field, enter *VE-102*, and select to filter by **Asset**.</span></span>
1. <span data-ttu-id="70952-172">Vælg aktivet for at åbne dets indstillinger.</span><span class="sxs-lookup"><span data-stu-id="70952-172">Select the asset to open its settings.</span></span>
1. <span data-ttu-id="70952-173">Gå til oversigtspanelet **Kunde**, og angiv feltet **Debitorkonto** til *US-013* (*Pelican Wholesales*).</span><span class="sxs-lookup"><span data-stu-id="70952-173">On the **Customer** FastTab, set the **Customer account** field to *US-013* (*Pelican Wholesales*).</span></span>

    <span data-ttu-id="70952-174">Feltet **Navn** opdateres automatisk til *Pelican Wholesales*.</span><span class="sxs-lookup"><span data-stu-id="70952-174">The **Name** field is automatically updated to *Pelican Wholesales*.</span></span>

### <a name="step-7-create-a-new-work-order-on-the-asset"></a><span data-ttu-id="70952-175">Trin 7: Opret en ny arbejdsordre på aktivet</span><span class="sxs-lookup"><span data-stu-id="70952-175">Step 7: Create a new work order on the asset</span></span>

1. <span data-ttu-id="70952-176">Gå til **Styring af aktiver \> Arbejdsordrer \> Aktive arbejdsordrer**.</span><span class="sxs-lookup"><span data-stu-id="70952-176">Go to **Asset management \> Work orders \> Active work orders**.</span></span>
1. <span data-ttu-id="70952-177">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="70952-177">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="70952-178">Angiv følgende værdier i dialogboksen **Opret arbejdsordre**:</span><span class="sxs-lookup"><span data-stu-id="70952-178">In the **Create work order** dialog box, set the following values:</span></span>

    - <span data-ttu-id="70952-179">**Arbejdsordretype:** *Service*</span><span class="sxs-lookup"><span data-stu-id="70952-179">**Work order type:** *Service*</span></span>
    - <span data-ttu-id="70952-180">**Beskrivelse:** *Reparer lastvogn*</span><span class="sxs-lookup"><span data-stu-id="70952-180">**Description:** *Repair Truck*</span></span>
    - <span data-ttu-id="70952-181">**Debitorkonto:** *US-013* (*Pelican Wholesales*)</span><span class="sxs-lookup"><span data-stu-id="70952-181">**Customer account:** *US-013* (*Pelican Wholesales*)</span></span>
    - <span data-ttu-id="70952-182">**Aktiv:** *VE-102*</span><span class="sxs-lookup"><span data-stu-id="70952-182">**Asset:** *VE-102*</span></span>

        > [!NOTE]
        > <span data-ttu-id="70952-183">Opslaget viser kun aktiver, der er knyttet til den valgte kundekonto.</span><span class="sxs-lookup"><span data-stu-id="70952-183">The lookup shows only assets that are linked to the selected customer account.</span></span>

    - <span data-ttu-id="70952-184">**Vedligeholdelsesjobtype:** *Reparation*</span><span class="sxs-lookup"><span data-stu-id="70952-184">**Maintenance job type:** *Repair*</span></span>
    - <span data-ttu-id="70952-185">**Branche:** *Mekanik*</span><span class="sxs-lookup"><span data-stu-id="70952-185">**Trade:** *Mechanic*</span></span>
    - <span data-ttu-id="70952-186">**Serviceniveau:** *4*</span><span class="sxs-lookup"><span data-stu-id="70952-186">**Service level:** *4*</span></span>

1. <span data-ttu-id="70952-187">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="70952-187">Select **OK**.</span></span>

### <a name="step-8-review-the-work-order-and-start-to-work-on-it"></a><span data-ttu-id="70952-188">Trin 8: Gennemse arbejdsordren, og begynd at arbejde på den</span><span class="sxs-lookup"><span data-stu-id="70952-188">Step 8: Review the work order and start to work on it</span></span>

<span data-ttu-id="70952-189">I dette afsnit arbejder du med den arbejdsordre, du oprettede i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="70952-189">In this section, you will work on the work order that you created in the previous section.</span></span>

1. <span data-ttu-id="70952-190">Benyt følgende fremgangsmåde for at kontrollere, at det overordnede projekt er *Pelican Wholesales-arbejdsordrer*:</span><span class="sxs-lookup"><span data-stu-id="70952-190">Follow these steps to verify that the parent project is the *Pelican wholesales Work order* project:</span></span>

    1. <span data-ttu-id="70952-191">Vælg en linje i sektionen **Vedligeholdelsesjob for arbejdsordre**.</span><span class="sxs-lookup"><span data-stu-id="70952-191">In the **Work order maintenance jobs** section, select a line.</span></span>
    1. <span data-ttu-id="70952-192">Kontrollér værdien af **Projekt-id** i oversigtspanelet **Linjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="70952-192">On the **Line details** FastTab, inspect the **Project ID** value.</span></span> <span data-ttu-id="70952-193">Det skal være et nummer med bindestreg i formatet *\<Parent-Project-ID\>-\<Project-ID\>*.</span><span class="sxs-lookup"><span data-stu-id="70952-193">It should be a hyphenated number in the form *\<Parent-Project-ID\>-\<Project-ID\>*.</span></span> <span data-ttu-id="70952-194">Denne værdi er et link.</span><span class="sxs-lookup"><span data-stu-id="70952-194">This value is a link.</span></span>
    1. <span data-ttu-id="70952-195">Vælg linket til projekt-id'et for at åbne en side, hvor du kan se det overordnede projekt og projektnavnene.</span><span class="sxs-lookup"><span data-stu-id="70952-195">Select the project ID link to open a page where you can view the parent project and project names.</span></span>

1. <span data-ttu-id="70952-196">Vælg **Opdatere tilstand for arbejdsordre** i gruppen **Livscyklustilstand** under fanen **Arbejdsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="70952-196">On the Action Pane, on the **Work order** tab, in the **Lifecycle state** group, select **Update work order state**.</span></span>
1. <span data-ttu-id="70952-197">I dialogboksen **Opdatere tilstand for arbejdsordre** skal du i kolonnen **Vælg** markere afkrydsningsfeltet for den række, hvor feltet **Livscyklustilstand** er angivet til *I gang*.</span><span class="sxs-lookup"><span data-stu-id="70952-197">In the **Update work order state** dialog box, in the **Select** column, select the check box for the row where the **Lifecycle state** field is set to *In progress*.</span></span>
1. <span data-ttu-id="70952-198">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="70952-198">Select **OK**.</span></span>
1. <span data-ttu-id="70952-199">I dialogboksen **Livscyklustilstand: I gang** skal du vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="70952-199">In the **Lifecycle state: InProgress** dialog box, select **OK**.</span></span>

### <a name="step-9-post-the-hours-that-were-spent-on-the-work-order-and-create-a-new-invoice-proposal"></a><span data-ttu-id="70952-200">Trin 9: Bogfør de timer, der er brugt på arbejdsordren, og opret et nyt fakturaforslag</span><span class="sxs-lookup"><span data-stu-id="70952-200">Step 9: Post the hours that were spent on the work order and create a new invoice proposal</span></span>

<span data-ttu-id="70952-201">I dette afsnit arbejder du fortsat med den arbejdsordre, du arbejdede på i forrige afsnit.</span><span class="sxs-lookup"><span data-stu-id="70952-201">In this section, you will continue to work on the work order that you worked on in the previous section.</span></span>

1. <span data-ttu-id="70952-202">Vælg **Kladder** i gruppen **Projekt** under fanen **Arbejdsordre** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="70952-202">On the Action Pane, on the **Work order** tab, in the **Project** group, select **Journals**.</span></span>

    <span data-ttu-id="70952-203">Siden **Arbejdsordrekladder** vises.</span><span class="sxs-lookup"><span data-stu-id="70952-203">The **Work order journals** page appears.</span></span> <span data-ttu-id="70952-204">Her kan du registrere den tid, du har brugt på arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="70952-204">Here, you can register the time that you spent on the work order.</span></span>

1. <span data-ttu-id="70952-205">Vælg **Tilføj linje** i oversigtspanelet **Timer**.</span><span class="sxs-lookup"><span data-stu-id="70952-205">On the **Hours** FastTab, select **Add line**.</span></span>
1. <span data-ttu-id="70952-206">Angiv feltet **Timer** til *4* på den nye linje.</span><span class="sxs-lookup"><span data-stu-id="70952-206">On the new, line, set the **Hours** field to *4*.</span></span>
1. <span data-ttu-id="70952-207">Vælg **Bogfør kladder** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="70952-207">On the Action Pane, select **Post journals**.</span></span>
1. <span data-ttu-id="70952-208">Luk siden **Arbejdsordrekladder** for at vende tilbage til arbejdsordren.</span><span class="sxs-lookup"><span data-stu-id="70952-208">Close the **Work order journals** page to return to the work order.</span></span>
1. <span data-ttu-id="70952-209">I handlingsruden skal du under fanen **Fakturering** vælge **Nyt fakturaforslag**.</span><span class="sxs-lookup"><span data-stu-id="70952-209">On the Action Pane, on the **Invoicing** tab, select **New invoice proposal**.</span></span>
1. <span data-ttu-id="70952-210">Markér afkrydsningsfeltet **Vælg** ud for hver linje, du vil fakturere, i sektionen **Projekttransaktioner** i dialogboksen **Opret fakturaforslag**.</span><span class="sxs-lookup"><span data-stu-id="70952-210">In the **Create invoice proposal** dialog box, in the **Project transactions** section, select the **Select** check box for every line  that you want to invoice.</span></span>
1. <span data-ttu-id="70952-211">Vælg **OK** for at lukke dialogboksen og se fakturaforslaget.</span><span class="sxs-lookup"><span data-stu-id="70952-211">Select **OK** to close the dialog box and view the new invoice proposal.</span></span>
