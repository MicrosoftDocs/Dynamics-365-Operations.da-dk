---
title: Fejlfinde lagerhandlinger
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med lagerhandlinger.
author: sherry-zheng
ms.date: 12/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-03
ms.dyn365.ops.version: Release 10.0.16
ms.openlocfilehash: 24e41e35b3e810c509a16b91fffd1e796ab9d134
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5832052"
---
# <a name="troubleshoot-inventory-operations"></a><span data-ttu-id="c6019-103">Fejlfinde lagerhandlinger</span><span class="sxs-lookup"><span data-stu-id="c6019-103">Troubleshoot inventory operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6019-104">Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med lagerhandlinger.</span><span class="sxs-lookup"><span data-stu-id="c6019-104">This topic describes how to fix issues that you might encounter while you work with inventory operations.</span></span>

## <a name="i-cant-find-the-workflow-drop-down-dialog-box-for-inventory-journals"></a><span data-ttu-id="c6019-105">Jeg kan ikke finde dialogboksen til rullelisten "Arbejdsgang" for lagerkladder.</span><span class="sxs-lookup"><span data-stu-id="c6019-105">I can't find the "Workflow" drop-down dialog box for inventory journals.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6019-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c6019-106">Issue description</span></span>

<span data-ttu-id="c6019-107">Du kan ikke finde dialogboksen til rullelisten **Arbejdsgang** på kladdesiden, eller relaterede arbejdsgangshandlinger er ikke tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="c6019-107">You can't find the **Workflow** drop-down dialog box on the journal page, or related workflow operations aren't available.</span></span>

<span data-ttu-id="c6019-108">Dette problem kan forekomme af tre årsager som beskrevet i følgende underafsnit.</span><span class="sxs-lookup"><span data-stu-id="c6019-108">This issue can occur for three reasons, as described in the following subsections.</span></span>

### <a name="issue-resolution-1"></a><span data-ttu-id="c6019-109">Problemløsning 1</span><span class="sxs-lookup"><span data-stu-id="c6019-109">Issue resolution 1</span></span>

<span data-ttu-id="c6019-110">Hvis problemet gælder for alle brugere, kan det være på grund af, at godkendelsesarbejdsgangen ikke er tildelt kladdenavnet.</span><span class="sxs-lookup"><span data-stu-id="c6019-110">If the issue applies to all users, it might be occurring because the approval workflow hasn't been assigned to the journal name.</span></span> <span data-ttu-id="c6019-111">Følg disse trin for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="c6019-111">To fix the issue, follow these steps.</span></span>

1. <span data-ttu-id="c6019-112">Gå til **Lagerstyring &gt; Konfiguration &gt; Kladdenavne &gt; Lager**.</span><span class="sxs-lookup"><span data-stu-id="c6019-112">Go to **Inventory Management &gt; Setup &gt; Journal names &gt; Inventory**.</span></span>
1. <span data-ttu-id="c6019-113">Vælg et kladdenavn i listeruden for at åbne indstillingerne.</span><span class="sxs-lookup"><span data-stu-id="c6019-113">In the list pane, select a journal name to open its settings.</span></span>
1. <span data-ttu-id="c6019-114">I oversigtspanelet **Generelt** skal du angive indstillingen **Godkendelsesarbejdsgang** til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="c6019-114">On the **General** FastTab, set the **Approval workflow** option to *Yes*.</span></span> <span data-ttu-id="c6019-115">Klik på **Ja**, hvis du bliver bedt om at bekræfte ændringen.</span><span class="sxs-lookup"><span data-stu-id="c6019-115">If you're prompted to confirm the change, select **Yes**.</span></span>
1. <span data-ttu-id="c6019-116">I feltet **Arbejdsgang** skal du vælge den arbejdsgang, du vil bruge til det valgte kladdenavn.</span><span class="sxs-lookup"><span data-stu-id="c6019-116">In the **Workflow** field, select the workflow that you want to use for the selected journal name.</span></span>

### <a name="issue-resolution-2"></a><span data-ttu-id="c6019-117">Problemløsning 2</span><span class="sxs-lookup"><span data-stu-id="c6019-117">Issue resolution 2</span></span>

<span data-ttu-id="c6019-118">Hvis arbejdsgangen bruger tilpasset kode, kan der opstå problemer, efter du har opgraderet systemet.</span><span class="sxs-lookup"><span data-stu-id="c6019-118">If your workflow uses customized code, issues might occur after you upgrade the system.</span></span> <span data-ttu-id="c6019-119">I kladdearbejdsgangen kan knappen **Send** f.eks. være nedtonet, så du ikke kan vælge den for at godkende en afsendelse.</span><span class="sxs-lookup"><span data-stu-id="c6019-119">For example, in the journal workflow, the **Submit** button might be grayed out so you can't select it to approve a submission.</span></span>

<span data-ttu-id="c6019-120">Hvis knappen **Send** er nedtonet, er arbejdsgangen måske blevet tilpasset, hvilket betyder, at metoden for arbejdsgangen `canSubmitToWorkflow()` i `FormDataUtil` er blevet udvidet.</span><span class="sxs-lookup"><span data-stu-id="c6019-120">If the **Submit** button is grayed out, your workflow might have been customized, which means the method of the workflow, `canSubmitToWorkflow()` in `FormDataUtil`, has been extended.</span></span> <span data-ttu-id="c6019-121">Du kan løse dette problem ved at ændre den måde, hvorpå du udvider metoden for `canSubmitToWorkflow()` til at bruge strukturen, i følgende eksempel.</span><span class="sxs-lookup"><span data-stu-id="c6019-121">To fix this issue, change the way that you extend the method of the `canSubmitToWorkflow()` to use the structure in the following example.</span></span>

```xpp
[ExtensionOf(formStr(InventJournalMovement))]
public final class InventJournalMovement_extension
{
    public boolean canSubmitToWorkflow()
    {
        boolean ret = YourLogicOfCanSubmitToWorkflow();

        return ret;
    }
}
```

### <a name="issue-resolution-3"></a><span data-ttu-id="c6019-122">Problemløsning 3</span><span class="sxs-lookup"><span data-stu-id="c6019-122">Issue resolution 3</span></span>

<span data-ttu-id="c6019-123">Hvis problemet kun gælder for nogle få bestemte brugere, har disse brugere muligvis ikke de sikkerhedsrettigheder, der er nødvendige for at køre arbejdsgangshandlinger i lagerkladder.</span><span class="sxs-lookup"><span data-stu-id="c6019-123">If the issue applies only to a few specific users, those users might not have the security privileges that are required to run workflow operations on inventory journals.</span></span> <span data-ttu-id="c6019-124">Kontrollér, at hver påvirket bruger har sikkerhedsrettigheden *Vedligehold arbejdsgang for lagerkladder*.</span><span class="sxs-lookup"><span data-stu-id="c6019-124">Verify that each affected user has the *Maintain inventory journal workflow* security privilege.</span></span> <span data-ttu-id="c6019-125">Denne rettighed er som standard tildelt en opgave med samme navn, og denne opgave anvendes til rollerne *Lagerarbejder* og *Lagerchef*.</span><span class="sxs-lookup"><span data-stu-id="c6019-125">By default, this privilege is assigned to a duty that has same name, and that duty is applied to the *Warehouse worker* and *Warehouse manager* roles.</span></span>

## <a name="my-inventory-journal-remains-in-system-locked-status-and-the-workflow-batch-job-doesnt-work"></a><span data-ttu-id="c6019-126">Min lagerkladde forbliver i statussen systemlåst, og arbejdsgangsbatchjobbet virker ikke.</span><span class="sxs-lookup"><span data-stu-id="c6019-126">My inventory journal remains in system-locked status, and the workflow batch job doesn't work.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6019-127">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c6019-127">Issue description</span></span>

<span data-ttu-id="c6019-128">En af lagerkladderne er låst af en eller anden handling, og den frigives ikke.</span><span class="sxs-lookup"><span data-stu-id="c6019-128">One of your inventory journals is locked by some operation and isn't being released.</span></span> <span data-ttu-id="c6019-129">Hvis der f.eks. opstår en ukendt fejl under bogføring (som er en systemlåshandling), kan kladden stadig have statussen systemlåst.</span><span class="sxs-lookup"><span data-stu-id="c6019-129">For example, if an unknown error occurs during posting (which is a system lock operation), the journal might remain in system-locked status.</span></span> <span data-ttu-id="c6019-130">I dette tilfælde viser arbejdsgangsopgavehandleren en fejl under låsevalidering.</span><span class="sxs-lookup"><span data-stu-id="c6019-130">In this case, the workflow work item handler will throw an error while it does lock validation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c6019-131">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c6019-131">Issue resolution</span></span>

<span data-ttu-id="c6019-132">Log på SQL Server-forekomsten for Supply Chain Management, og kontrollér, om **InventJournalTable.SystemBlocked** er angivet til *1*.</span><span class="sxs-lookup"><span data-stu-id="c6019-132">Sign in to the SQL Server instance for Supply Chain Management, and check whether **InventJournalTable.SystemBlocked** is set to *1*.</span></span> <span data-ttu-id="c6019-133">Hvis det er tilfældet, skal du sørge for, at kladden ikke er i låst status og derefter nulstille **InventJournalTable.SystemBlocked** til *0*.</span><span class="sxs-lookup"><span data-stu-id="c6019-133">If it is, make sure that the journal should not be in locked status, and then reset **InventJournalTable.SystemBlocked** to *0*.</span></span>

## <a name="my-inventory-journal-workflow-is-never-completed-and-the-journal-cant-be-edited-or-posted"></a><span data-ttu-id="c6019-134">Min arbejdsgang for lagerkladder fuldføres aldrig, og kladden kan ikke redigeres eller bogføres.</span><span class="sxs-lookup"><span data-stu-id="c6019-134">My inventory journal workflow is never completed, and the journal can't be edited or posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6019-135">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c6019-135">Issue description</span></span>

<span data-ttu-id="c6019-136">Når du har sendt en arbejdsgang for lagerkladdegodkendelse, stopper arbejdsgangsbehandlingen med at svare, og du kan ikke redigere eller behandle kladderne.</span><span class="sxs-lookup"><span data-stu-id="c6019-136">After you submit a journal approval workflow, workflow processing stops responding, and you can't edit or process your journals.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c6019-137">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c6019-137">Issue resolution</span></span>

<span data-ttu-id="c6019-138">Der er flere årsager til, at arbejdsgangsbehandlingen muligvis ikke fuldføres.</span><span class="sxs-lookup"><span data-stu-id="c6019-138">There are several reasons why workflow processing might not be completed.</span></span> <span data-ttu-id="c6019-139">Kontrollér, om der er følgende problemer:</span><span class="sxs-lookup"><span data-stu-id="c6019-139">Check for the following issues:</span></span>

- <span data-ttu-id="c6019-140">Gå til **Lagerstyring &gt; Konfiguration &gt; Arbejdsgange for lagerstyring**, og gennemse konfigurationen af den berørte arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="c6019-140">Go to **Inventory management &gt; Setup &gt; Inventory management workflows**, and review the configuration of the affected workflow.</span></span> <span data-ttu-id="c6019-141">Du kan finde flere oplysninger i [Arbejdsgange for godkendelse af lagerkladde](inventory-journal-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="c6019-141">For more information, see [Inventory journal approval workflows](inventory-journal-workflow.md).</span></span>
- <span data-ttu-id="c6019-142">Der kan opstå en undtagelse eller fejl i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="c6019-142">The workflow might be encountering an exception or error.</span></span> <span data-ttu-id="c6019-143">Gennemse historikken for arbejdselementet for den berørte arbejdsgang for at se, om den omfatter en applikationsfejl, der afslutter arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="c6019-143">Review the work item history of the affected workflow to see whether it includes an application error that terminates the workflow.</span></span>
- <span data-ttu-id="c6019-144">Lagerkladden kan kun opdateres eller redigeres, hvis den er godkendt.</span><span class="sxs-lookup"><span data-stu-id="c6019-144">The inventory journal can be updated or edited only if it's approved.</span></span> <span data-ttu-id="c6019-145">Hvis tilbagekaldelse er aktiv, kan du prøve at tilbagekalde kladden.</span><span class="sxs-lookup"><span data-stu-id="c6019-145">If recall is active, you can try to recall the journal.</span></span> <span data-ttu-id="c6019-146">Afviklingen af arbejdsgangsbatchjobbet kan være suspenderet af flere årsager.</span><span class="sxs-lookup"><span data-stu-id="c6019-146">Execution of the workflow batch job might be suspended for multiple reasons.</span></span> <span data-ttu-id="c6019-147">Nogle af disse årsager kan være forårsaget af problemer i arbejdsgangsstrukturen.</span><span class="sxs-lookup"><span data-stu-id="c6019-147">Some of these reasons might be caused by the workflow framework issue.</span></span>

## <a name="inventory-journal-workflow-conditions-apply-only-at-the-journal-level-not-at-the-line-level"></a><span data-ttu-id="c6019-148">Betingelserne for arbejdsgange for lagerkladder gælder kun på kladdeniveau, ikke på linjeniveau</span><span class="sxs-lookup"><span data-stu-id="c6019-148">Inventory journal workflow conditions apply only at the journal level, not at the line level</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6019-149">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c6019-149">Issue description</span></span>

<span data-ttu-id="c6019-150">Du kan opleve denne fejl, hvis du f.eks. prøver at konfigurere en betingelse for arbejdsgange for lagerkladder for kostbeløbet.</span><span class="sxs-lookup"><span data-stu-id="c6019-150">You might experience this issue if, for example, you try to set up an inventory journal workflow condition on the cost amount.</span></span> <span data-ttu-id="c6019-151">Du konfigurerer betingelsen, så trin 1 kun køres, når kostbeløbet er mindre end 100.</span><span class="sxs-lookup"><span data-stu-id="c6019-151">You set up the condition so that step 1 is run only when the cost amount is less than 100.</span></span> <span data-ttu-id="c6019-152">Du konfigurerer derefter en anden betingelse, så trin 2 kun køres, når kostbeløbet er mere end eller lig med 100.</span><span class="sxs-lookup"><span data-stu-id="c6019-152">You then set up another condition so that step 2 is run only when the cost amount is more than or equal to 100.</span></span> <span data-ttu-id="c6019-153">Når arbejdsgangen derefter køres, vises der kun én linje i arbejdsgangshistorikken, og den første betingelse evalueres altid som *sand*, uanset hvilken værdi der sendes.</span><span class="sxs-lookup"><span data-stu-id="c6019-153">Then, when the workflow is run, the workflow history shows only one line, and the first condition is always evaluated as *true*, regardless of the value that is submitted.</span></span>

### <a name="issue-workaround"></a><span data-ttu-id="c6019-154">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c6019-154">Issue workaround</span></span>

<span data-ttu-id="c6019-155">I den aktuelle version gælder betingelserne for arbejdsgange for lagerkladder kun på kladdeniveau, ikke på linjeniveau.</span><span class="sxs-lookup"><span data-stu-id="c6019-155">In the current release, inventory workflow conditions apply only at the journal level, not at the line level.</span></span> <span data-ttu-id="c6019-156">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="c6019-156">This behavior is by design.</span></span> <span data-ttu-id="c6019-157">Det anbefales, at du kun angiver betingelseskriterierne for attributter på kladdeniveau.</span><span class="sxs-lookup"><span data-stu-id="c6019-157">We recommend that you set your condition criteria only on journal-level attributes.</span></span>

## <a name="the-filter-pane-on-the-on-hand-list-page-doesnt-filter-results-as-i-expect"></a><span data-ttu-id="c6019-158">Filterruden på listesiden Beholdningsliste filtrerer ikke resultater som forventet.</span><span class="sxs-lookup"><span data-stu-id="c6019-158">The filter pane on the On-hand list page doesn't filter results as I expect.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6019-159">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c6019-159">Issue description</span></span>

<span data-ttu-id="c6019-160">Filtrene i filteruden på siden **Beholdningsliste** filtrerer ikke resultater som forventet.</span><span class="sxs-lookup"><span data-stu-id="c6019-160">The filters in the filter pane on the **On-hand list** page don't filter results as you expect.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c6019-161">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c6019-161">Issue resolution</span></span>

<span data-ttu-id="c6019-162">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="c6019-162">This behavior is by design.</span></span>

<span data-ttu-id="c6019-163">Siden  **Beholdningsliste** samles fra en detaljeret disponibel lagerbeholdningstabel, der omfatter alle tilgængelige dimensioner.</span><span class="sxs-lookup"><span data-stu-id="c6019-163">The **On-hand list** page is assembled from a detailed on-hand inventory table that includes all available dimensions.</span></span> <span data-ttu-id="c6019-164">Listen på denne side er dog en oversigt.</span><span class="sxs-lookup"><span data-stu-id="c6019-164">However, the list on this page is a summary.</span></span> <span data-ttu-id="c6019-165">Derfor kan den kombinere rækker fra kildetabellen ved at aggregere værdier i henhold til de viste dimensioner.</span><span class="sxs-lookup"><span data-stu-id="c6019-165">Therefore, it might combine rows from the source table by aggregating values according to the dimensions that are shown.</span></span>

<span data-ttu-id="c6019-166">Filtre, der er konfigureret i filterruden, gælder for kildetabellen, ikke den samlede liste.</span><span class="sxs-lookup"><span data-stu-id="c6019-166">Filters that are set up in the filter pane apply to the source table, not to the aggregated list.</span></span> <span data-ttu-id="c6019-167">Denne adfærd kan nogle gange give uventede resultater, som det fremgår af [disse eksempler](inventory-on-hand-list.md#examples).</span><span class="sxs-lookup"><span data-stu-id="c6019-167">This behavior can sometimes produce unexpected results, as shown in [these examples](inventory-on-hand-list.md#examples).</span></span>

<span data-ttu-id="c6019-168">De  [filtre, der findes i gitteret](inventory-on-hand-list.md#grid-filters),  *bliver* anvendt på den samlede liste.</span><span class="sxs-lookup"><span data-stu-id="c6019-168">However, the [filters that are provided in the grid](inventory-on-hand-list.md#grid-filters) *do* apply to the aggregated list.</span></span> <span data-ttu-id="c6019-169">Disse filtre omfatter både QuickFilter øverst i gitteret og filteret for hver kolonneoverskrift.</span><span class="sxs-lookup"><span data-stu-id="c6019-169">These filters include both the QuickFilter at the top of the grid and the filter for each column heading.</span></span>

## <a name="the-unit-and-unit-quantity-arent-working-correctly-in-the-inventory-journal"></a><span data-ttu-id="c6019-170">Enheden og enhedsantallet fungerer ikke korrekt i lagerkladden.</span><span class="sxs-lookup"><span data-stu-id="c6019-170">The unit and unit quantity aren't working correctly in the inventory journal.</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6019-171">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c6019-171">Issue description</span></span>

<span data-ttu-id="c6019-172">Der kan opstå en eller begge af følgende fejl, når du arbejder med enheder og antal i en lagerkladde:</span><span class="sxs-lookup"><span data-stu-id="c6019-172">You might encounter one or both of the following issues when you work with units and quantities in an inventory journal:</span></span>

- <span data-ttu-id="c6019-173">Du kan ikke se enheder eller enhedsantal i lagerkladden, når der er konfigureret en enhedskonvertering for det frigivne produkt, og du kan ikke ændre enheden i lagerkladden.</span><span class="sxs-lookup"><span data-stu-id="c6019-173">You don't see units or unit quantities in the inventory journal while a unit of conversion is set up for the released product, and you can't change the unit in the inventory journal.</span></span>
- <span data-ttu-id="c6019-174">Du kan se felterne **Antal** og **Enhed** i lagerkladden, men du kan ikke se feltet **Enhedsantal**.</span><span class="sxs-lookup"><span data-stu-id="c6019-174">You see the **Quantity** and **Unit** fields in the inventory journal, but you don't see the **Unit quantity** field.</span></span> <span data-ttu-id="c6019-175">Hvis du ændrer enheden, angiver et antal og bogfører kladden, vises den oprindelige måleenhed for dette antal stadig i kladden.</span><span class="sxs-lookup"><span data-stu-id="c6019-175">If you change the unit, enter a quantity, and post the journal, the journal still shows the original unit of measurement for that quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c6019-176">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c6019-176">Issue resolution</span></span>

<span data-ttu-id="c6019-177">Følg disse trin for at løse dette problem.</span><span class="sxs-lookup"><span data-stu-id="c6019-177">To fix this issue, follow these steps.</span></span>

1. <span data-ttu-id="c6019-178">I arbejdsområdet **Funktionsstyring** skal du sørge for, at funktionen *Brug af måleenhed og enhedsantal i lagerkladder* er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="c6019-178">In the **Feature management** workspace, make sure that the *Using unit of measure and unit quantity in inventory journals* feature is turned on.</span></span> <span data-ttu-id="c6019-179">Denne funktion føjer felterne **Enhed** og **Enhedsantal** til kladden.</span><span class="sxs-lookup"><span data-stu-id="c6019-179">This feature adds the **Unit** and **Unit quantity** fields to the journal.</span></span>
1. <span data-ttu-id="c6019-180">Når funktionen er aktiveret, skal du benytte felterne **Antal**, **Enhedsantal** og **Enhed** på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="c6019-180">After the feature is turned on, use the **Quantity**, **Unit quantity**, and **Unit** fields in the following way:</span></span>

    - <span data-ttu-id="c6019-181">**Antal** – Angiv antallet ved hjælp af den standardenhed, der er defineret for det frigivne produkt.</span><span class="sxs-lookup"><span data-stu-id="c6019-181">**Quantity** – Specify the quantity by using the default unit that is defined for the released product.</span></span> <span data-ttu-id="c6019-182">Selve standardenheden vises dog ikke her.</span><span class="sxs-lookup"><span data-stu-id="c6019-182">However, the default unit itself isn't shown here.</span></span> <span data-ttu-id="c6019-183">Hvis der er konfigureret en konvertering mellem standardenheden og den valgte enhed i feltet **Enhed**, opdateres feltet **Antal** automatisk baseret på valgene i felterne **Enhedantal** og **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="c6019-183">If a conversion is set up between the default unit and the unit that is selected in the **Unit** field, the **Quantity** field is automatically updated, based on the selections in the **Unit quantity** and **Unit** fields.</span></span>
    - <span data-ttu-id="c6019-184">**Enhedsantal** – Angiv antallet ved at bruge den enhed, der er valgt i feltet **Enhed**.</span><span class="sxs-lookup"><span data-stu-id="c6019-184">**Unit quantity** – Specify the quantity by using the unit that is selected in the **Unit** field.</span></span>
    - <span data-ttu-id="c6019-185">**Enhed** – Vælg den enhed, der skal anvendes på værdien i feltet **Enhedsantal**.</span><span class="sxs-lookup"><span data-stu-id="c6019-185">**Unit** – Select the unit to apply to the value in the **Unit quantity** field.</span></span>

## <a name="i-receive-the-following-error-message-maximum-number-of-decimals-for-the-stock-keeping-unit-is-0"></a><span data-ttu-id="c6019-186">Jeg får følgende fejlmeddelelse: "Maks. antal decimaler for lagerenheden er 0".</span><span class="sxs-lookup"><span data-stu-id="c6019-186">I receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

### <a name="issue-description"></a><span data-ttu-id="c6019-187">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="c6019-187">Issue description</span></span>

<span data-ttu-id="c6019-188">Når du forsøger at bogføre en lagertransaktion eller en lagerreservation, får du vist følgende fejlmeddelelse: "Maks. antal decimaler for lagerenheden er 0".</span><span class="sxs-lookup"><span data-stu-id="c6019-188">When you try to post an inventory transaction or an inventory reservation, you receive the following error message: "Maximum number of decimals for the stock keeping unit is 0."</span></span>

<span data-ttu-id="c6019-189">Denne fejl opstår, når lagertransaktionsantallet angives som en decimalværdi, der er under det præcisionsniveau, som feltet understøtter.</span><span class="sxs-lookup"><span data-stu-id="c6019-189">This issue occurs when the inventory transaction quantity is specified as a decimal value that is below the level of precision that the field supports.</span></span> <span data-ttu-id="c6019-190">Der er f.eks. angivet et antal på *0,5* for en lagertransaktion, men antal understøttes kun i heltal.</span><span class="sxs-lookup"><span data-stu-id="c6019-190">For example, a quantity of *0.5* has been specified for an inventory transaction, but only integer quantities are supported.</span></span> <span data-ttu-id="c6019-191">Derfor skal værdien være *1* i stedet for *0,5*.</span><span class="sxs-lookup"><span data-stu-id="c6019-191">Therefore, the value should be *1* instead of *0.5*.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="c6019-192">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="c6019-192">Issue resolution</span></span>

1. <span data-ttu-id="c6019-193">Kør følgende script på SQL Server-forekomsten for at afrunde antallet i lagertransaktionerne.</span><span class="sxs-lookup"><span data-stu-id="c6019-193">Run the following script on your SQL Server instance to round quantities in the inventory transactions.</span></span> <span data-ttu-id="c6019-194">Dette script retter værdier i tabellen **InventTrans**.</span><span class="sxs-lookup"><span data-stu-id="c6019-194">This script will correct values in the **inventTrans** table.</span></span>

    ```sql
    update it set it.QTY = round(it.qty, decimalPrecisionValue) from inventtrans it where it.DATAAREAID='XXXX' and it.PARTITION=XXXXXX and it.qty <> round(it.qty, decimalPrecisionValue) and exists (select 'x' from INVENTTABLEMODULE a, unitofmeasure b where  a.unitid =b.SYMBOL and a.partition=it.partition and a.PARTITION=b.PARTITION and  MODULETYPE =0 and  b.DECIMALPRECISION=decimalPrecisionValue and a.DATAAREAID='XXXX' and a.ITEMID =it.ITEMID and it.DATAAREAID=a.DATAAREAID)
    ```

1. <span data-ttu-id="c6019-195">Kør en konsistenskontrol beholdningen, hvor indstillingen **ret fejl** er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="c6019-195">Run an on-hand consistency check where the **fix error** option is turned on.</span></span> <span data-ttu-id="c6019-196">Denne kontrol retter værdier i tabellen **InventSum**.</span><span class="sxs-lookup"><span data-stu-id="c6019-196">This check will correct values in the **inventSum** table.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c6019-197">Det anbefales på det kraftigste, at du nøje redigerer scriptet i dit miljø, tester det i et testmiljø og derefter kontrollerer de resulterende data, før du kører scriptet i et produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="c6019-197">We strongly recommend that you carefully edit the script as required for your environment, test it in a test environment, and then check the resulting data before you run the script in a production environment.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]