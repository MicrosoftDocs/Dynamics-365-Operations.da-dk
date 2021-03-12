---
title: Arbejdsopdeling
description: Dette emne indeholder oplysninger om arbejdsopdelingsfunktionen. Med denne funktionalitet kan du opdele store arbejdsordrer i flere mindre arbejdsordrer, som du derefter kan tildele til flere lagermedarbejdere. På denne måde kan det samme arbejde plukkes samtidig af flere lagermedarbejdere.
author: mirzaab
manager: tfehr
ms.date: 10/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.search.industry: WHSWorkTableListPage
ms.author: mirzaab
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8a530f3887c3c66295177d480a8c486dd0984153
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4965521"
---
# <a name="work-split"></a><span data-ttu-id="c67bd-105">Arbejdsopdeling</span><span class="sxs-lookup"><span data-stu-id="c67bd-105">Work split</span></span>

<span data-ttu-id="c67bd-106">Med arbejdsopdelingsfunktionen kan du opdele store arbejds-id'er (dvs. arbejdsordrer med flere linjer) i flere mindre arbejds-id'er, som du derefter kan tildele til flere lagermedarbejdere.</span><span class="sxs-lookup"><span data-stu-id="c67bd-106">Work split functionality lets you split large work IDs (that is, work orders that have several lines) into several smaller work IDs that you can then assign to multiple warehouse workers.</span></span> <span data-ttu-id="c67bd-107">På denne måde kan det samme arbejdsnummer plukkes samtidig af flere lagermedarbejdere.</span><span class="sxs-lookup"><span data-stu-id="c67bd-107">In this way, the same work creation number can be picked simultaneously by several warehouse workers.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c67bd-108">Du kan kun opdele arbejdsordrer, der har statussen *Åben* eller *Igangværende*.</span><span class="sxs-lookup"><span data-stu-id="c67bd-108">You can split only work orders that have a status of *Open* or *In-progress*.</span></span>

## <a name="turn-on-the-work-split-functionality"></a><span data-ttu-id="c67bd-109">Aktivere funktionen til opdeling af arbejde</span><span class="sxs-lookup"><span data-stu-id="c67bd-109">Turn on the work split functionality</span></span>

<span data-ttu-id="c67bd-110">Før du kan bruge funktionen til opdeling af arbejde, skal du aktivere funktionen og dens forudsætning i systemet.</span><span class="sxs-lookup"><span data-stu-id="c67bd-110">Before you can use the work split functionality, you must turn on the feature and its prerequisite feature in your system.</span></span> <span data-ttu-id="c67bd-111">Administratorer kan bruge indstillingerne i [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) til at kontrollere funktionens status og slå den til efter behov.</span><span class="sxs-lookup"><span data-stu-id="c67bd-111">Administrators can use the [feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) settings to check the status of the features and turn them on as required.</span></span>

<span data-ttu-id="c67bd-112">Først skal du aktivere den forudsætningsfunktionen *Blokering af arbejde i hele organisationen*, hvis den ikke allerede er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="c67bd-112">First, turn on the prerequisite *Organization-wide work blocking* feature if it isn't already turned on.</span></span> <span data-ttu-id="c67bd-113">I arbejdsområdet **Funktionsstyring** vises denne funktion på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="c67bd-113">In the **Feature management** workspace, this feature is listed in the following way:</span></span>

- <span data-ttu-id="c67bd-114">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="c67bd-114">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c67bd-115">**Funktionsnavn:** *Blokering af arbejde i hele organisationen*</span><span class="sxs-lookup"><span data-stu-id="c67bd-115">**Feature name:** *Organization-wide work blocking*</span></span>

> [!NOTE]
> <span data-ttu-id="c67bd-116">Når denne funktion er aktiveret, anvendes der automatisk en dataopgradering, når funktionen er aktiveret på tværs af alle juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="c67bd-116">When this feature is activated, a data upgrade is automatically applied after the feature is turned on across all legal entities.</span></span>

<span data-ttu-id="c67bd-117">Derefter skal du aktivere funktionen *Arbejdsopdeling*, som findes på følgende måde:</span><span class="sxs-lookup"><span data-stu-id="c67bd-117">Next, turn on the *Work split* feature, which is listed in the following way:</span></span>

- <span data-ttu-id="c67bd-118">**Modul:** *Lokationsstyring*</span><span class="sxs-lookup"><span data-stu-id="c67bd-118">**Module:** *Warehouse management*</span></span>
- <span data-ttu-id="c67bd-119">**Funktionsnavn:** *Arbejdsopdeling*</span><span class="sxs-lookup"><span data-stu-id="c67bd-119">**Feature name:** *Work split*</span></span>

## <a name="enhancements-to-the-work-details-and-all-work-pages"></a><span data-ttu-id="c67bd-120">Forbedringer af arbejdsdetaljerne og alle arbejdssider</span><span class="sxs-lookup"><span data-stu-id="c67bd-120">Enhancements to the Work details and All work pages</span></span>

<span data-ttu-id="c67bd-121">Funktionen *Arbejdsopdeling* føjer følgende to knapper til fanen **Arbejde** i handlingsruden på siderne **Arbejdsdetaljer** og **Alt arbejde**:</span><span class="sxs-lookup"><span data-stu-id="c67bd-121">The *Work split* feature adds the following two buttons to the **Work** tab on the Action Pane of the **Work details** and **All work** pages:</span></span>

- <span data-ttu-id="c67bd-122">**Opdel arbejde** – Opdel det aktuelle arbejds-id i flere mindre arbejds-id'er, der kan behandles af særskilte arbejdere.</span><span class="sxs-lookup"><span data-stu-id="c67bd-122">**Split work** – Split the current work ID into multiple smaller work IDs that can be processed by separate workers.</span></span>
- <span data-ttu-id="c67bd-123">**Annuller arbejdsopdelt session** – Annuller den arbejdsopdelte session, og gør arbejdet tilgængeligt for behandling.</span><span class="sxs-lookup"><span data-stu-id="c67bd-123">**Cancel work split session** – Cancel the work split session, and make the work available for processing.</span></span>

<span data-ttu-id="c67bd-124">![Knapperne Opdel arbejde og Annuller arbejdsopdelt session](media/Work_split_buttons.png "Knapperne Opdel arbejde og Annuller arbejdsopdelt session")</span><span class="sxs-lookup"><span data-stu-id="c67bd-124">![Split work and Cancel work split session buttons](media/Work_split_buttons.png "Split work and Cancel work split session buttons")</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c67bd-125">Knappen **Opdel arbejde** er ikke tilgængelig, hvis en eller flere af følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="c67bd-125">The **Split work** button won't be available if any of the following conditions are met:</span></span>
>
> - <span data-ttu-id="c67bd-126">Arbejdsstatussen er noget andet end *Åben* eller *Igangværende*.</span><span class="sxs-lookup"><span data-stu-id="c67bd-126">The work status is something other than *Open* or *In progress*.</span></span>
> - <span data-ttu-id="c67bd-127">Et container-id er knyttet til arbejds-id'et.</span><span class="sxs-lookup"><span data-stu-id="c67bd-127">A container ID is associated with the work ID.</span></span> <span data-ttu-id="c67bd-128">(En container kan ikke opdeles systematisk, fordi den kræver fysiske handlinger).</span><span class="sxs-lookup"><span data-stu-id="c67bd-128">(A container can't be systematically split, because it requires physical actions.)</span></span>
> - <span data-ttu-id="c67bd-129">Arbejdet er knyttet til en klynge.</span><span class="sxs-lookup"><span data-stu-id="c67bd-129">The work is associated with a cluster.</span></span>
> - <span data-ttu-id="c67bd-130">Arbejdsordretypen er noget andet end en af følgende typer:</span><span class="sxs-lookup"><span data-stu-id="c67bd-130">The work order type is something other than one of the following types:</span></span>
>
>    - <span data-ttu-id="c67bd-131">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="c67bd-131">Sales orders</span></span>
>    - <span data-ttu-id="c67bd-132">Råvarepluk</span><span class="sxs-lookup"><span data-stu-id="c67bd-132">Raw material picking</span></span>
>    - <span data-ttu-id="c67bd-133">Flytteafgang</span><span class="sxs-lookup"><span data-stu-id="c67bd-133">Transfer issue</span></span>
>
> - <span data-ttu-id="c67bd-134">Arbejdet opdeles i øjeblikket af en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="c67bd-134">The work is currently being split by another user.</span></span> <span data-ttu-id="c67bd-135">Hvis du forsøger at åbne opdelingssiden for arbejde, der allerede er ved at blive opdelt af en anden bruger, får du vist følgende fejlmeddelelse: "Arbejdet med id \#\#\#\# er ved at blive opdelt.</span><span class="sxs-lookup"><span data-stu-id="c67bd-135">If you try to open the splitting page for work that is already being split by another user, you receive the following error message: "The work with ID \#\#\#\# is currently being split.</span></span> <span data-ttu-id="c67bd-136">Prøv igen om et par minutter.</span><span class="sxs-lookup"><span data-stu-id="c67bd-136">Retry in a few minutes.</span></span> <span data-ttu-id="c67bd-137">Hvis du fortsætter med at modtage denne meddelelse, skal du kontakte en tilsynsførende".</span><span class="sxs-lookup"><span data-stu-id="c67bd-137">If you continue to receive this message, contact a supervisor."</span></span>

<span data-ttu-id="c67bd-138">En ny årsag til arbejdsblokering, *Opdelt arbejde*, angiver, hvornår arbejds-id'et er ved at blive opdelt.</span><span class="sxs-lookup"><span data-stu-id="c67bd-138">A new work blocking reason, *Split work*, indicates when the work ID is in the process of being split.</span></span> <span data-ttu-id="c67bd-139">Det vises både på siden **Opdel arbejde** og i lagerstedsappen, hvis en bruger forsøger at køre arbejdet.</span><span class="sxs-lookup"><span data-stu-id="c67bd-139">It's shown both on the **Split work** page and in the warehouse app if a user tries to run the work.</span></span> <span data-ttu-id="c67bd-140">Når der bruges blokeringsårsager, ændres navnet på feltet **Blokeret bølge** fra arbejds-id'et til **Blokeret**.</span><span class="sxs-lookup"><span data-stu-id="c67bd-140">When blocking reasons are used, the name of the **Blocked wave** field from the work ID is changed to **Blocked**.</span></span>

## <a name="initiate-a-work-split"></a><span data-ttu-id="c67bd-141">Starte en opdeling af arbejde</span><span class="sxs-lookup"><span data-stu-id="c67bd-141">Initiate a work split</span></span>

<span data-ttu-id="c67bd-142">Funktionen tilføjer en ny **Opdel arbejde**-side, der giver brugerne mulighed for at opdele arbejdslinjer fra arbejds-id'et.</span><span class="sxs-lookup"><span data-stu-id="c67bd-142">The feature adds a new **Split work** page that lets users split work lines from the work ID.</span></span> <span data-ttu-id="c67bd-143">Når siden åbnes første gang, vises linjer, der har statussen *Åben*, og som er tilgængelige for opdeling.</span><span class="sxs-lookup"><span data-stu-id="c67bd-143">When the page is first opened, it shows lines that have a work status of *Open* and that are available to be split.</span></span> <span data-ttu-id="c67bd-144">Vælg **Opdel arbejde** i handlingsruden at behandle det valgte arbejde.</span><span class="sxs-lookup"><span data-stu-id="c67bd-144">On the Action Pane, select **Split work** to process the selected work.</span></span>

<span data-ttu-id="c67bd-145">Hvis du vil opdele arbejdet, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c67bd-145">To split work, follow these steps.</span></span>

1. <span data-ttu-id="c67bd-146">Åbn en af følgende arbejdssider:</span><span class="sxs-lookup"><span data-stu-id="c67bd-146">Open one of the following work pages:</span></span>

    - <span data-ttu-id="c67bd-147">**Arbejdsdetaljer** (**Lokationsstyring \> Arbejde \> Arbejdsdetaljer**)</span><span class="sxs-lookup"><span data-stu-id="c67bd-147">**Work details** (**Warehouse management \> Work \> Work details**)</span></span>
    - <span data-ttu-id="c67bd-148">**Alt arbejde** (**Lokationsstyring \> Arbejde \> Alt arbejde**)</span><span class="sxs-lookup"><span data-stu-id="c67bd-148">**All work** (**Warehouse management \> Work \> All work**)</span></span>

1. <span data-ttu-id="c67bd-149">Vælg et arbejds-id, der skal opdeles, i gitteret.</span><span class="sxs-lookup"><span data-stu-id="c67bd-149">In the grid, select a work ID to split.</span></span> <span data-ttu-id="c67bd-150">Feltet **Arbejdsordretype** skal angives til en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="c67bd-150">The **Work order type** field must be set to one of the following values:</span></span>

    - <span data-ttu-id="c67bd-151">Salgsordre</span><span class="sxs-lookup"><span data-stu-id="c67bd-151">Sales orders</span></span>
    - <span data-ttu-id="c67bd-152">Råvarepluk</span><span class="sxs-lookup"><span data-stu-id="c67bd-152">Raw material picking</span></span>
    - <span data-ttu-id="c67bd-153">Flytteafgang</span><span class="sxs-lookup"><span data-stu-id="c67bd-153">Transfer issue</span></span>

1. <span data-ttu-id="c67bd-154">Gå til handlingsrunde og vælg **Opdel arbejde** i gruppen **Arbejde** under fanen **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="c67bd-154">On the Action Pane, on the **Work** tab, in the **Work** group, select **Split work**.</span></span>

    <span data-ttu-id="c67bd-155">Siden **Opdel arbejde** vises med de åbne arbejdslinjer, som er åbne og kan opdeles.</span><span class="sxs-lookup"><span data-stu-id="c67bd-155">The **Split work** page appears and shows the work lines that are open and available to be split.</span></span> <span data-ttu-id="c67bd-156">Der vises som standard kun tilgængelige arbejdslinjer.</span><span class="sxs-lookup"><span data-stu-id="c67bd-156">By default, only available work lines are shown.</span></span> <span data-ttu-id="c67bd-157">Hvis du vil have vist alle linjer for arbejds-id'et (f.eks. linjer med arbejdstypen *Læg på lager*), skal du markere afkrydsningsfeltet **Vis alle linjer** over gitteret.</span><span class="sxs-lookup"><span data-stu-id="c67bd-157">To view all lines for the work ID (for example, lines that have a work type of *Put*), select the **Show all lines** check box above the grid.</span></span>

    <span data-ttu-id="c67bd-158">Følgende meddelelse vises: "Brugere kan ikke behandle linjer i arbejdet, før du er færdig med at opdele og lukke denne side".</span><span class="sxs-lookup"><span data-stu-id="c67bd-158">The following message is shown: "Users can't process lines of the work until you finish splitting and close this page."</span></span>

    <span data-ttu-id="c67bd-159">Feltet **Årsag til blokering af arbejde** for det aktuelle arbejde vil blive indstillet til *Opdelt arbejde*, og arbejdet vil blive blokeret.</span><span class="sxs-lookup"><span data-stu-id="c67bd-159">The **Work blocking reason** field for the current work will be set to *Split work*, and the work will be blocked.</span></span>

    <span data-ttu-id="c67bd-160">![Blokeringsårsag](media/Blocking_reason.png "Blokeringsårsag")</span><span class="sxs-lookup"><span data-stu-id="c67bd-160">![Blocking reason](media/Blocking_reason.png "Blocking reason")</span></span>

1. <span data-ttu-id="c67bd-161">Vælg de linjer, der skal fjernes fra det aktuelle arbejds-id, og føj dem til et nyt arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="c67bd-161">Select the lines to remove from the current work ID and add to a new work ID.</span></span> <span data-ttu-id="c67bd-162">Følgende hændelser forekommer:</span><span class="sxs-lookup"><span data-stu-id="c67bd-162">The following events occur:</span></span>

    - <span data-ttu-id="c67bd-163">Når du opdeler arbejdet, annulleres den eller de valgte linjer fra det oprindelige arbejds-id og kopieres derefter til et nyt arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="c67bd-163">When you split the work, the selected line or lines from the original work ID are canceled and then copied to a new work ID.</span></span>
    - <span data-ttu-id="c67bd-164">Strukturen for den eksisterende arbejdsskabelon og lokationen for læg på lager (og også fremtidige pluk/læg på lager-par) bevares.</span><span class="sxs-lookup"><span data-stu-id="c67bd-164">The existing work template structure and the location of the put (and also future pick/put pairs) are preserved.</span></span> <span data-ttu-id="c67bd-165">Værdierne for følgende arbejds-id-felter kopieres fra det oprindelige arbejde til det nye arbejde:</span><span class="sxs-lookup"><span data-stu-id="c67bd-165">Values for the following work ID fields are copied from the original work to the new work:</span></span>

        - <span data-ttu-id="c67bd-166">Last-id</span><span class="sxs-lookup"><span data-stu-id="c67bd-166">Load ID</span></span>
        - <span data-ttu-id="c67bd-167">Forsendelses-id</span><span class="sxs-lookup"><span data-stu-id="c67bd-167">Shipment ID</span></span>
        - <span data-ttu-id="c67bd-168">Arbejdsordretype</span><span class="sxs-lookup"><span data-stu-id="c67bd-168">Work order type</span></span>
        - <span data-ttu-id="c67bd-169">Ordrenummer</span><span class="sxs-lookup"><span data-stu-id="c67bd-169">Order number</span></span>
        - <span data-ttu-id="c67bd-170">Lokation</span><span class="sxs-lookup"><span data-stu-id="c67bd-170">Site</span></span>
        - <span data-ttu-id="c67bd-171">Lagersted</span><span class="sxs-lookup"><span data-stu-id="c67bd-171">Warehouse</span></span>
        - <span data-ttu-id="c67bd-172">Arbejdsprioritet</span><span class="sxs-lookup"><span data-stu-id="c67bd-172">Work priority</span></span>
        - <span data-ttu-id="c67bd-173">Arbejdspulje-id</span><span class="sxs-lookup"><span data-stu-id="c67bd-173">Work pool ID</span></span>
        - <span data-ttu-id="c67bd-174">Bølge-id</span><span class="sxs-lookup"><span data-stu-id="c67bd-174">Wave ID</span></span>
        - <span data-ttu-id="c67bd-175">Nummer på arbejdsoprettelse</span><span class="sxs-lookup"><span data-stu-id="c67bd-175">Work creation number</span></span>

    - <span data-ttu-id="c67bd-176">Følgende felter kopieres ikke til det nye arbejds-id:</span><span class="sxs-lookup"><span data-stu-id="c67bd-176">The following fields aren't copied to the new work ID:</span></span>

        - <span data-ttu-id="c67bd-177">**Arbejds-id** – Der genereres et nyt arbejds-id fra den relevante nummerserie.</span><span class="sxs-lookup"><span data-stu-id="c67bd-177">**Work ID** – A new work ID is generated from the appropriate number sequence.</span></span>
        - <span data-ttu-id="c67bd-178">**Arbejdsstatus** – Dette felt er angivet til *Åben*.</span><span class="sxs-lookup"><span data-stu-id="c67bd-178">**Work status** – This field is set to *Open*.</span></span>
        - <span data-ttu-id="c67bd-179">**Låst af** – Dette felt angives er udgangspunkt tomt.</span><span class="sxs-lookup"><span data-stu-id="c67bd-179">**Locked by** – This field is initially set to blank.</span></span>
        - <span data-ttu-id="c67bd-180">**Målnummerplade-id** – Dette felt er tomt.</span><span class="sxs-lookup"><span data-stu-id="c67bd-180">**Target license plate ID** – This field is left blank.</span></span>
        - <span data-ttu-id="c67bd-181">**Dato og klokkeslæt for oprettelse** – Dette felt er angivet til dags dato og det aktuelle klokkeslæt.</span><span class="sxs-lookup"><span data-stu-id="c67bd-181">**Created date and time** – This field is set to the current date and time.</span></span>
        - <span data-ttu-id="c67bd-182">**Blokeret bølge/fastfrossen** – Dette felt er genberegnet for det oprindelige arbejds-id og det nye arbejds-id.</span><span class="sxs-lookup"><span data-stu-id="c67bd-182">**Blocked wave/frozen** – This field is recomputed for the original work ID and the new work ID.</span></span>

1. <span data-ttu-id="c67bd-183">Vælg **Opdel arbejde** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c67bd-183">On the Action Pane, select **Split work**.</span></span>

<span data-ttu-id="c67bd-184">Mens arbejdet opdeles, vises følgende meddelelse: "Behandlingsoperation – Opdel arbejde".</span><span class="sxs-lookup"><span data-stu-id="c67bd-184">While the work is being split, the following message is shown: "Processing operation - Split work".</span></span> <span data-ttu-id="c67bd-185">Når denne meddelelse er synlig, kan du annullere handlingen ved at vælge **Annuller** i meddelelsesboksen.</span><span class="sxs-lookup"><span data-stu-id="c67bd-185">While this message is visible, you can cancel the operation by selecting **Cancel** in the message box.</span></span>

<span data-ttu-id="c67bd-186">Hvis afkrydsningsfeltet **Vis alle linjer** ikke er markeret, vises den linje, der er opdelt og annulleret, ikke længere i gitteret.</span><span class="sxs-lookup"><span data-stu-id="c67bd-186">If the **Show all lines** check box is cleared, the line that was split off and canceled will no longer appear in the grid.</span></span> <span data-ttu-id="c67bd-187">Hvis afkrydsningsfeltet er markeret, bør du kunne se, at værdien i feltet **Arbejdsstatus** for linjen er ændret til *Annulleret*.</span><span class="sxs-lookup"><span data-stu-id="c67bd-187">If the check box is selected, you should see that the value of the **Work status** field for that line has changed to *Canceled*.</span></span>

<span data-ttu-id="c67bd-188">Følgende meddelelse vises for at angive, at det nye arbejds-id er oprettet: "Arbejde \#\#\#\# er oprettet ved at opdele fra det oprindelige arbejde \#\#\#\#".</span><span class="sxs-lookup"><span data-stu-id="c67bd-188">The following notification is shown to indicate that the new work ID has been created: "Work \#\#\#\# has been created by splitting off from original work \#\#\#\#."</span></span>

<span data-ttu-id="c67bd-189">Andre arbejdslinjer fra det oprindelige arbejds-id (f.eks. *Læg på lager*-linjer) vil blive justeret efter behov, så de afspejler de linjer i arbejdet, der er blevet annulleret.</span><span class="sxs-lookup"><span data-stu-id="c67bd-189">Other work lines from the original work ID (such as *Put* lines) will be adjusted as required to reflect the lines of work that have been canceled.</span></span> <span data-ttu-id="c67bd-190">Hvis det oprindelige arbejds-id f.eks. havde en *Læg på lager*-linje for et antal på 15, og *Pluk*-linjer, der har et samlet antal på 10 blev annulleret, vil det nye *Læg på lager*-antal på det oprindelige arbejds-id nu være 5.</span><span class="sxs-lookup"><span data-stu-id="c67bd-190">For example, if the original work ID had a *Put* line for a quantity of 15, and *Pick* lines that have a total quantity of 10 were canceled, the new *Put* quantity on the original work ID will now be 5.</span></span>

<span data-ttu-id="c67bd-191">Det nye arbejde tildeles ikke straks til en bruger.</span><span class="sxs-lookup"><span data-stu-id="c67bd-191">The new work won't immediately be assigned to any user.</span></span> <span data-ttu-id="c67bd-192">Du kan dog tildele det til en bruger nu, hvis det er nødvendigt, ved hjælp af standardfunktionerne på siden **Arbejdsdetaljer**.</span><span class="sxs-lookup"><span data-stu-id="c67bd-192">However, you can assign it to a user now, as required, by using the standard functionality of the **Work details** page.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c67bd-193">Du kan kun opdele arbejds-id'er, der indeholder to eller flere tilgængelige arbejdslinjer.</span><span class="sxs-lookup"><span data-stu-id="c67bd-193">You can split only work IDs that contain two or more available work lines.</span></span> <span data-ttu-id="c67bd-194">Hvis du vælger **Opdel arbejde**, når der kun er én arbejdslinje, får du vist følgende fejlmeddelelse: "Mindst én arbejdslinje skal forblive i det indledende arbejde".</span><span class="sxs-lookup"><span data-stu-id="c67bd-194">If you select **Split work** when there is only one work line, you will receive the following error message: "At least one work line must remain on initial work."</span></span> <span data-ttu-id="c67bd-195">Hvis dette er tilfældet, sker der ingen opdeling.</span><span class="sxs-lookup"><span data-stu-id="c67bd-195">In this case, no splitting will occur.</span></span>

## <a name="finish-a-work-split"></a><span data-ttu-id="c67bd-196">Afslutte en opdeling af arbejde</span><span class="sxs-lookup"><span data-stu-id="c67bd-196">Finish a work split</span></span>

<span data-ttu-id="c67bd-197">Hvis du vil afslutte opdeling af arbejde, skal blokeringsårsagen *Opdel arbejde* være fjernet.</span><span class="sxs-lookup"><span data-stu-id="c67bd-197">To finish splitting work, the *Split work* blocking reason must be removed.</span></span> <span data-ttu-id="c67bd-198">Der er to måder at gøre dette på:</span><span class="sxs-lookup"><span data-stu-id="c67bd-198">There are two ways to complete this step:</span></span>

- <span data-ttu-id="c67bd-199">Den bruger, der opdeler arbejdet, lukker siden **Opdel arbejde** ved at vælge knappen **Luk** (**X**) i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="c67bd-199">The user who is splitting the work closes the **Split work** page by selecting the **Close** button (**X**) in the upper-right corner.</span></span> <span data-ttu-id="c67bd-200">Når siden lukkes, fjernes blokeringsårsagen *Opdel arbejde*.</span><span class="sxs-lookup"><span data-stu-id="c67bd-200">When the page is closed, the *Split Work* blocking reason will be removed.</span></span> <span data-ttu-id="c67bd-201">Den *Blokerede* tilstand for dette arbejde vil blive genberegnet, og hvis der ikke er nogen resterende blokeringsårsager for dette arbejde, vil arbejdet blive fjernet.</span><span class="sxs-lookup"><span data-stu-id="c67bd-201">The *Blocked* state of this work will be recomputed and, if there are no remaining blocking reasons for this work, the work will be unblocked.</span></span>
- <span data-ttu-id="c67bd-202">Alle brugere åbner arbejds-id'et og vælger knappen **Annuller opdeling af arbejdssession** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="c67bd-202">Any user opens the work ID and selects the **Cancel work split session** button on the Action Pane.</span></span> <span data-ttu-id="c67bd-203">Årsagen til blokeringen af *Opdel arbejde* vil blive fjernet, og *Blokeret*-tilstand for dette arbejde vil blive genberegnet, ligesom når siden **Opdel arbejde** lukkes.</span><span class="sxs-lookup"><span data-stu-id="c67bd-203">The *Split work* blocking reason will be removed, and the *Blocked* state of this work will be recomputed, just as when the **Split work** page is closed.</span></span>

<span data-ttu-id="c67bd-204">Når blokeringsårsagen *Opdel arbejde* er fjernet, kan arbejdet køres på mobilenheden, hvis den **blokerede** tilstand er angivet til *Nej* på arbejds-id'et.</span><span class="sxs-lookup"><span data-stu-id="c67bd-204">After the *Split work* blocking reason is removed, the work can be run on the mobile device, provided that the **Blocked** state is set to *No* on the work ID.</span></span>

## <a name="user-blocking-on-the-warehouse-app"></a><span data-ttu-id="c67bd-205">Brugerblokering på lagerstedsappen</span><span class="sxs-lookup"><span data-stu-id="c67bd-205">User blocking on the warehouse app</span></span>

<span data-ttu-id="c67bd-206">Hvis du forsøger at bruge lagerstedsappen til at køre plukarbejde på et arbejds-id, der er ved at blive opdelt, får du vist følgende fejlmeddelelse: "Arbejdet med id \#\#\#\# er ved at blive opdelt".</span><span class="sxs-lookup"><span data-stu-id="c67bd-206">If you try to use the warehouse app to run picking work against a work ID that is being split, you will receive the following error message: "The work with ID \#\#\#\# is currently being split."</span></span> <span data-ttu-id="c67bd-207">Hvis du modtager denne meddelelse, skal du vælge **Annuller**.</span><span class="sxs-lookup"><span data-stu-id="c67bd-207">If you receive this message, select **Cancel**.</span></span> <span data-ttu-id="c67bd-208">Du kan derefter fortsætte med at behandle andet arbejde.</span><span class="sxs-lookup"><span data-stu-id="c67bd-208">You can then continue to process other work.</span></span>

## <a name="other-blocked-operations"></a><span data-ttu-id="c67bd-209">Andre blokerede handlinger</span><span class="sxs-lookup"><span data-stu-id="c67bd-209">Other blocked operations</span></span>

<span data-ttu-id="c67bd-210">Handlinger, der redigerer arbejdslinjer, arbejdslagertransaktioner eller genopfyldningslinks, der er relateret til det arbejde, der opdeles, mislykkes, og følgende fejlmeddelelse vises: "Arbejdet med id \#\#\#\# er ved at blive opdelt".</span><span class="sxs-lookup"><span data-stu-id="c67bd-210">Any operations that modify work lines, work inventory transactions, or replenishment links that are related to work that is being split will fail, and the following error message will be shown: "The work with ID \#\#\#\# is currently being split."</span></span>
