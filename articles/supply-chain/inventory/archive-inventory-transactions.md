---
title: Arkivere lagertransaktioner
description: Dette emne beskriver, hvordan du arkiverer lagertransaktionsdata for at forbedre systemets ydeevne.
author: sherry-zheng
ms.date: 03/01/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: InventTransArchiveProcessForm
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2021-03-01
ms.dyn365.ops.version: Release 10.0.18
ms.openlocfilehash: bacc27c1a9066892c51110d28ba9a2ad26bebe77
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5839289"
---
# <a name="archive-inventory-transactions"></a><span data-ttu-id="cd05d-103">Arkivere lagertransaktioner</span><span class="sxs-lookup"><span data-stu-id="cd05d-103">Archive inventory transactions</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="cd05d-104">Med tiden fortsætter tabellen med lagertransaktioner (`InventTrans`) med at stige og forbruge mere databaseplads.</span><span class="sxs-lookup"><span data-stu-id="cd05d-104">Over time, the inventory transactions table (`InventTrans`) will continue to grow and consume more database space.</span></span> <span data-ttu-id="cd05d-105">Derfor bliver de forespørgsler, der foretages mod tabellen, efterhånden langsommere.</span><span class="sxs-lookup"><span data-stu-id="cd05d-105">Therefore, queries that are made against the table will gradually become slower.</span></span> <span data-ttu-id="cd05d-106">Dette emne beskriver, hvordan du kan bruge funktionen *Arkivér lagertransaktioner* til at arkivere data om lagertransaktioner for at forbedre systemets ydeevne.</span><span class="sxs-lookup"><span data-stu-id="cd05d-106">This topic describes how you can use the *Inventory transactions archive* feature to archive data about inventory transactions to help improve system performance.</span></span>

> [!NOTE]
> <span data-ttu-id="cd05d-107">Det er kun økonomisk opdaterede lagertransaktioner, der kan arkiveres i en valgt lukket finansperiode.</span><span class="sxs-lookup"><span data-stu-id="cd05d-107">Only financially updated inventory transactions can be archived in a selected closed ledger period.</span></span> <span data-ttu-id="cd05d-108">Hvis du vil arkivere, skal økonomisk opdaterede udgående lagertransaktioner have afgangsstatussen *Solgt*, og indgående lagertransaktioner skal have tilgangsstatussen *Købt*.</span><span class="sxs-lookup"><span data-stu-id="cd05d-108">To be archived, financially updated outbound inventory transactions must have an issue status of *Sold*, and inbound inventory transactions must have a receipt status of *Purchased*.</span></span>

<span data-ttu-id="cd05d-109">Når du arkiverer lagertransaktioner, flyttes alle relaterede transaktioner til tabellen `InventTransArchive`.</span><span class="sxs-lookup"><span data-stu-id="cd05d-109">When you archive inventory transactions, all related transactions are moved to the `InventTransArchive` table.</span></span> <span data-ttu-id="cd05d-110">Lagerafgangstransaktioner og lagertilgangstransaktioner arkiveres separat baseret på kombinationen af vare-id (`itemId`) og lagerdimensions-id (`inventDimId`), og de indgår i de opsummerede afgangs- og opsummerede tilgangstransaktioner.</span><span class="sxs-lookup"><span data-stu-id="cd05d-110">Inventory issue transactions and inventory receipt transactions are archived separately, based on the combination of the item ID (`itemId`) and inventory dimension ID (`inventDimId`), and they are put into the summarized issue and summarized receipt transactions.</span></span>

<span data-ttu-id="cd05d-111">Hvis en kombination af `itemId` og `inventDimId` kun indeholder én tilgangs- eller afgangstransaktion, arkiveres transaktionen ikke.</span><span class="sxs-lookup"><span data-stu-id="cd05d-111">If an `itemId` and `inventDimId` combination contains only one receipt or issue transaction, the transaction won't be archived.</span></span>

## <a name="turn-on-the-feature-in-your-system"></a><span data-ttu-id="cd05d-112">Aktivere funktionen i systemet</span><span class="sxs-lookup"><span data-stu-id="cd05d-112">Turn on the feature in your system</span></span>

<span data-ttu-id="cd05d-113">Hvis systemet ikke allerede indeholder de funktioner, der er beskrevet i dette emne, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Arkivér lagertransaktioner*.</span><span class="sxs-lookup"><span data-stu-id="cd05d-113">If your system doesn't already include the features that is described in this topic, go to [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md), and turn on the *Inventory transactions archive* feature.</span></span>

## <a name="things-to-consider-before-you-archive-inventory-transactions"></a><span data-ttu-id="cd05d-114">Ting, der skal overvejes, før du arkiverer lagertransaktioner</span><span class="sxs-lookup"><span data-stu-id="cd05d-114">Things to consider before you archive inventory transactions</span></span>

<span data-ttu-id="cd05d-115">Før du arkiverer lagertransaktioner, skal du overveje følgende forretningsscenarier, da de påvirkes af operationen:</span><span class="sxs-lookup"><span data-stu-id="cd05d-115">Before you archive inventory transactions, you should consider the following business scenarios, because they will be affected by the operation:</span></span>

- <span data-ttu-id="cd05d-116">Når du overvåger lagertransaktioner fra relaterede dokumenter som f.eks. indkøbsordrelinjer, vises de som arkiverede.</span><span class="sxs-lookup"><span data-stu-id="cd05d-116">When you audit inventory transactions from related documents, such as purchase order lines, they will be shown as archived.</span></span> <span data-ttu-id="cd05d-117">Du kan gennemse de arkiverede transaktioner ved at gå til **Lagerstyring \> Periodiske opgaver \> Oprydning \> Arkivér lagertransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="cd05d-117">To review the archived transactions, you must go to **Inventory management \> Periodic tasks \> Clean up \> Inventory transactions archive**.</span></span>
- <span data-ttu-id="cd05d-118">Lagerlukning kan ikke annulleres i arkiverede perioder.</span><span class="sxs-lookup"><span data-stu-id="cd05d-118">Inventory closing can't be canceled for archived periods.</span></span> <span data-ttu-id="cd05d-119">Før du kan annullere en lagerlukning, skal du tilbageføre lagertransaktionsarkivet for den relevante periode.</span><span class="sxs-lookup"><span data-stu-id="cd05d-119">Before you can cancel an inventory closing, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="cd05d-120">Standardomkostningskonvertering kan ikke udføres for arkiverede perioder.</span><span class="sxs-lookup"><span data-stu-id="cd05d-120">Standard cost conversion can't be done for archived periods.</span></span> <span data-ttu-id="cd05d-121">Før du kan udføre standardomkostningskonvertering, skal du tilbageføre lagertransaktionsarkivet for den relevante periode.</span><span class="sxs-lookup"><span data-stu-id="cd05d-121">Before you can do standard cost conversion, you must reverse the inventory transaction archive for the relevant period.</span></span>
- <span data-ttu-id="cd05d-122">Lagerrapporter, der er hentet fra lagertransaktioner, påvirkes, når du arkiverer lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="cd05d-122">Inventory reports that are sourced from inventory transactions will be affected when you archive inventory transactions.</span></span> <span data-ttu-id="cd05d-123">Disse rapporter omfatter rapport over aldersfordelt lager og rapport over lagerværdier.</span><span class="sxs-lookup"><span data-stu-id="cd05d-123">These reports include the inventory aging report and inventory value reports.</span></span>
- <span data-ttu-id="cd05d-124">Lagerbudgetter kan påvirkes, hvis de køres i tidshorisonten for arkiverede perioder.</span><span class="sxs-lookup"><span data-stu-id="cd05d-124">Inventory forecasts might be affected if they are run during the time horizon of archived periods.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="cd05d-125">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="cd05d-125">Prerequisites</span></span>

<span data-ttu-id="cd05d-126">Lagertransaktioner kan kun arkiveres i perioder, hvor følgende betingelser er opfyldt:</span><span class="sxs-lookup"><span data-stu-id="cd05d-126">Inventory transactions can be archived only during periods where the following conditions are met:</span></span>

- <span data-ttu-id="cd05d-127">Finansperioden skal være lukket.</span><span class="sxs-lookup"><span data-stu-id="cd05d-127">The ledger period must be closed.</span></span>
- <span data-ttu-id="cd05d-128">Lagerlukning skal køres på eller efter til-periodedatoen for arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-128">Inventory closing must be run on or after the to-period date of the archive.</span></span>
- <span data-ttu-id="cd05d-129">Perioden skal være mindst ét år før fra-periodedatoen for arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-129">The period must be at least one year before the from-period date of the archive.</span></span>
- <span data-ttu-id="cd05d-130">Der må ikke være eksisterende genberegninger af lager.</span><span class="sxs-lookup"><span data-stu-id="cd05d-130">There must not be any existing inventory recalculations.</span></span>

## <a name="archive-inventory-transactions"></a><span data-ttu-id="cd05d-131">Arkivere lagertransaktioner</span><span class="sxs-lookup"><span data-stu-id="cd05d-131">Archive inventory transactions</span></span>

<span data-ttu-id="cd05d-132">Benyt følgende trin for at arkivere lagertransaktioner.</span><span class="sxs-lookup"><span data-stu-id="cd05d-132">To archive inventory transactions, follow these steps.</span></span>

1. <span data-ttu-id="cd05d-133">Gå til **Lagerstyring** \> **Periodiske opgaver** \> **Oprydning** \> **Arkivér lagertransaktioner**.</span><span class="sxs-lookup"><span data-stu-id="cd05d-133">Go to **Inventory management** \> **Periodic tasks** \> **Clean up** \> **Inventory transaction archive**.</span></span>

    <span data-ttu-id="cd05d-134">Siden **Arkivér lagertransaktioner** vises med en liste over arkiverede procesposter.</span><span class="sxs-lookup"><span data-stu-id="cd05d-134">The **Inventory transactions archive** page appears and shows a list of archived process records.</span></span>

    <span data-ttu-id="cd05d-135">![Siden Arkivér lagertransaktioner](media/archive-inventory-empty.png "Siden Arkivér lagertransaktioner")</span><span class="sxs-lookup"><span data-stu-id="cd05d-135">![Inventory transactions archive page](media/archive-inventory-empty.png "Inventory transactions archive page")</span></span>

1. <span data-ttu-id="cd05d-136">Vælg **Arkivér lagertransaktioner** i handlingsruden for at oprette et lagerposteringsarkiv.</span><span class="sxs-lookup"><span data-stu-id="cd05d-136">On the Action Pane, select **Inventory transactions archive** to create an inventory transaction archive.</span></span>
1. <span data-ttu-id="cd05d-137">Angiv følgende felter i oversigtspanelet **Parametre** i dialogboksen **Arkivér lagertransaktioner**:</span><span class="sxs-lookup"><span data-stu-id="cd05d-137">In the **Inventory transactions archive** dialog box, on the **Parameters** FastTab, set the following fields:</span></span>

    - <span data-ttu-id="cd05d-138">**Fra dato i lukket finansperiode** – Vælg den tidligste transaktionsdato, der skal medtages i arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-138">**From date in closed ledger period** – Select the earliest transaction date to include in the archive.</span></span>
    - <span data-ttu-id="cd05d-139">**Til dato i lukket finansperiode** – Vælg den seneste transaktionsdato, der skal medtages i arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-139">**To date in closed ledger period** – Select the latest transaction date to include in the archive.</span></span>

    <span data-ttu-id="cd05d-140">![Dialogboksen Arkivér lagertransaktioner](media/archive-inventory-dates.png "Dialogboksen Arkivér lagertransaktioner")</span><span class="sxs-lookup"><span data-stu-id="cd05d-140">![Inventory transactions archive dialog box](media/archive-inventory-dates.png "Inventory transactions archive dialog box")</span></span>

    > [!NOTE]
    > <span data-ttu-id="cd05d-141">Det er kun perioder, der opfylder [forudsætningerne](#prerequisites), som kan vælges.</span><span class="sxs-lookup"><span data-stu-id="cd05d-141">Only periods that meet the [prerequisites](#prerequisites) will be available for selection.</span></span>

1. <span data-ttu-id="cd05d-142">Konfigurer batchafviklingsdetaljer efter behov i oversigtspanelet **Kør i baggrunden**.</span><span class="sxs-lookup"><span data-stu-id="cd05d-142">On the **Run in the background** FastTab, set up batch processing details as you require.</span></span> <span data-ttu-id="cd05d-143">Følg de normale trin for batchjob i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="cd05d-143">Follow the usual steps for batch jobs in Microsoft Dynamics 365 Supply Chain Management.</span></span>
1. <span data-ttu-id="cd05d-144">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd05d-144">Select **OK**.</span></span>
1. <span data-ttu-id="cd05d-145">Du modtager en meddelelse, hvor du bliver bedt om at bekræfte, at du vil fortsætte.</span><span class="sxs-lookup"><span data-stu-id="cd05d-145">You receive a message that prompts you to confirm that you want to continue.</span></span> <span data-ttu-id="cd05d-146">Læs meddelelsen omhyggeligt, og vælg derefter **Ja**, hvis du vil fortsætte.</span><span class="sxs-lookup"><span data-stu-id="cd05d-146">Read the message carefully, and then select **Yes** if you want to continue.</span></span>

    <span data-ttu-id="cd05d-147">Du modtager en meddelelse om, at lagertransaktionernes arkivjob er føjet til batchkøen.</span><span class="sxs-lookup"><span data-stu-id="cd05d-147">You receive a message that states that your inventory transactions archive job has been added to the batch queue.</span></span> <span data-ttu-id="cd05d-148">Jobbet vil nu begynde at arkivere lagertransaktioner fra den valgte periode.</span><span class="sxs-lookup"><span data-stu-id="cd05d-148">The job will now start to archive inventory transactions from the selected period.</span></span>

## <a name="view-archived-inventory-transactions"></a><span data-ttu-id="cd05d-149">Vis arkiverede lagertransaktioner</span><span class="sxs-lookup"><span data-stu-id="cd05d-149">View archived inventory transactions</span></span>

<span data-ttu-id="cd05d-150">Siden **Arkivér lagertransaktioner** viser hele din arkiveringshistorik.</span><span class="sxs-lookup"><span data-stu-id="cd05d-150">The **Inventory transactions archive** page shows your full archiving history.</span></span> <span data-ttu-id="cd05d-151">Hver række i gitteret indeholder oplysninger som f.eks. den dato, hvor arkivet blev oprettet, den bruger, der oprettede det, og statussen.</span><span class="sxs-lookup"><span data-stu-id="cd05d-151">Each row in the grid shows information such as the date when the archive was created, the user who created it, and its status.</span></span>

<span data-ttu-id="cd05d-152">![Arkiveringshistorik på siden Arkivér lagertransaktioner](media/archive-inventory-full.png "Arkiveringshistorik på siden Arkivér lagertransaktioner")</span><span class="sxs-lookup"><span data-stu-id="cd05d-152">![Archiving history on the Inventory transactions archive page](media/archive-inventory-full.png "Archiving history on the Inventory transactions archive page")</span></span>

<span data-ttu-id="cd05d-153">Vælg en af følgende værdier på rullelisten øverst på siden for at filtrere de arkiver, der vises i gitteret:</span><span class="sxs-lookup"><span data-stu-id="cd05d-153">In the drop-down list at the top of the page select one of the following values to filter the archives that are shown in the grid:</span></span>

- <span data-ttu-id="cd05d-154">**Aktiv** – Vis kun aktive arkiver, ikke tilbageførte arkiver.</span><span class="sxs-lookup"><span data-stu-id="cd05d-154">**Active** – Show only active archives, not reversed archives.</span></span>
- <span data-ttu-id="cd05d-155">**Alle** – Vis alle arkiver, både aktive og tilbageførte.</span><span class="sxs-lookup"><span data-stu-id="cd05d-155">**All** – Show all archives, both active and reversed.</span></span>

<span data-ttu-id="cd05d-156">For hvert arkiv i gitteret gives følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="cd05d-156">For each archive in the grid, the following information is provided:</span></span>

- <span data-ttu-id="cd05d-157">**Aktiv** – En markering angiver, at arkivet er aktivt.</span><span class="sxs-lookup"><span data-stu-id="cd05d-157">**Active** – A check mark indicates that the archive is active.</span></span>
- <span data-ttu-id="cd05d-158">**Fra dato** – Datoen på den ældste transaktion, der kan medtages i arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-158">**From date** – The date of the oldest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="cd05d-159">**Til dato** – Datoen på den seneste transaktion, der kan medtages i arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-159">**To date** – The date of the latest transaction that can be included in the archive.</span></span>
- <span data-ttu-id="cd05d-160">**Planlagt af** – Den brugerkonto, der oprettede arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-160">**Scheduled by** – The user account that created the archive.</span></span>
- <span data-ttu-id="cd05d-161">**Udført** – Datoen for oprettelsen af arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-161">**Executed** – The date when the archive was created.</span></span>
- <span data-ttu-id="cd05d-162">**Tilbageført** – En markering angiver, at arkivet er tilbageført.</span><span class="sxs-lookup"><span data-stu-id="cd05d-162">**Reverse** – A check mark indicates that the archive has been reversed.</span></span>
- <span data-ttu-id="cd05d-163">**Stop aktuel opdatering** – En markering angiver, at arkivering er i gang, men det er blevet sat på pause.</span><span class="sxs-lookup"><span data-stu-id="cd05d-163">**Stop current update** – A check mark indicates that the archive is in progress, but it has been paused.</span></span>
- <span data-ttu-id="cd05d-164">**Tilstand** – Behandlingsstatus for arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-164">**State** – The processing status of the archive.</span></span> <span data-ttu-id="cd05d-165">De mulige værdier er *Venter*, *I gang* og *Udført*.</span><span class="sxs-lookup"><span data-stu-id="cd05d-165">The possible values are *Waiting*, *In progress*, and *Finished*.</span></span>

<span data-ttu-id="cd05d-166">Værktøjslinjen over gitteret indeholder følgende knapper, du kan bruge til at arbejde med et valgt arkiv:</span><span class="sxs-lookup"><span data-stu-id="cd05d-166">The toolbar above the grid provides the following buttons that you can use to work with a selected archive:</span></span>

- <span data-ttu-id="cd05d-167">**Arkiverede transaktioner** – Få vist alle detaljer i det valgte arkiv.</span><span class="sxs-lookup"><span data-stu-id="cd05d-167">**Archived transactions** – View the full details of the selected archive.</span></span> <span data-ttu-id="cd05d-168">Siden **Arkiverede transaktioner** viser alle transaktionerne i arkivet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-168">The **Archived transactions** page that appears shows all the transactions in the archive.</span></span>

    <span data-ttu-id="cd05d-169">![Siden Arkiverede transaktioner](media/archive-inventory-transactions.png "Siden Arkiverede transaktioner")</span><span class="sxs-lookup"><span data-stu-id="cd05d-169">![Archived transactions page](media/archive-inventory-transactions.png "Archived transactions page")</span></span>

    <span data-ttu-id="cd05d-170">Hvis du vil have vist flere oplysninger om en bestemt transaktion på siden **Arkiverede transaktioner**, skal du vælge den i gitteret og derefter vælge **Arkiverede transaktionsdetaljer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="cd05d-170">To view more information about a specific transaction on the **Archived transactions** page, select it in the grid, and then, on the Action Pane, select **Archived transaction details**.</span></span> <span data-ttu-id="cd05d-171">Siden **Arkiverede transaktionsdetaljer** viser oplysninger som f.eks. finanspostering, referencer til relateret reskontro og økonomiske dimensioner.</span><span class="sxs-lookup"><span data-stu-id="cd05d-171">The **Archived transaction details** page that appears shows information such as the ledger posting, related subledger references, and financial dimensions.</span></span>

- <span data-ttu-id="cd05d-172">**Afbryd arkivering midlertidigt** – Afbryd et valgt arkiv midlertidigt, som er ved at blive behandlet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-172">**Pause archiving** – Pause a selected archive that is currently being processed.</span></span> <span data-ttu-id="cd05d-173">Denne pause træder først i kraft, når arkiveringsopgaven er oprettet.</span><span class="sxs-lookup"><span data-stu-id="cd05d-173">The pause takes effect only after the archiving task has been generated.</span></span> <span data-ttu-id="cd05d-174">Derfor kan der være en kort forsinkelse, før pausen træder i kraft.</span><span class="sxs-lookup"><span data-stu-id="cd05d-174">Therefore, there might be a short delay before the pause takes effect.</span></span> <span data-ttu-id="cd05d-175">Hvis et arkiv er blevet afbrudt midlertidigt, vises der en markering i feltet **Stop aktuel opdatering**.</span><span class="sxs-lookup"><span data-stu-id="cd05d-175">If an archive has been paused, a check mark appears in its **Stop current update** field.</span></span>
- <span data-ttu-id="cd05d-176">**Fortsæt arkivering** – Fortsæt behandlingen af et valgt arkiv, som er afbrudt midlertidigt.</span><span class="sxs-lookup"><span data-stu-id="cd05d-176">**Resume archiving** – Resume processing for a selected archive that is currently paused.</span></span>
- <span data-ttu-id="cd05d-177">**Tilbagefør** – Tilbagefør det valgte arkiv.</span><span class="sxs-lookup"><span data-stu-id="cd05d-177">**Reverse** – Reverse the selected archive.</span></span> <span data-ttu-id="cd05d-178">Du kan kun tilbageføre et arkiv, hvis feltet **Tilstand** er angivet til *Udført*.</span><span class="sxs-lookup"><span data-stu-id="cd05d-178">You can reverse an archive only if its **State** field is set to *Finished*.</span></span> <span data-ttu-id="cd05d-179">Hvis et arkiv er blevet tilbageført, vises der en markering i feltet **Tilbageført**.</span><span class="sxs-lookup"><span data-stu-id="cd05d-179">If an archive has been reversed, a check mark appears in its **Reverse** field.</span></span>
