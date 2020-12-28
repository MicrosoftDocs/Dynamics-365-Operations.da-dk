---
title: Kanban-området for overførsel understøtter stregkodescannere
description: Kanban-områdetet understøtter scannerinput fra en widget stregkodescanner til at vælge, starte, udfylde og tømme et kanban-job.
author: ChristianRytt
manager: tfehr
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 1bd6f1bdd847f74cee7d3594d19b72454063c0cb
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424855"
---
# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="89a5b-103">Kanban-området for overførsel understøtter stregkodescannere</span><span class="sxs-lookup"><span data-stu-id="89a5b-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="89a5b-104">Kanban-områdetet understøtter scannerinput fra en widget stregkodescanner til at vælge, starte, udfylde og tømme et kanban-job.</span><span class="sxs-lookup"><span data-stu-id="89a5b-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="89a5b-105">Registreringstilstande</span><span class="sxs-lookup"><span data-stu-id="89a5b-105">Registration modes</span></span>
------------------

<span data-ttu-id="89a5b-106">På oversigtspanelet **Scanner registrering** kan du vælge den registreringstilstand, der styrer handlingen, når du scanner et kanban-kortnummer eller manuelt skriver tallet i feltet med kanban-kortet.</span><span class="sxs-lookup"><span data-stu-id="89a5b-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="89a5b-107">Angiv registreringstilstand</span><span class="sxs-lookup"><span data-stu-id="89a5b-107">Set registration mode</span></span> | <span data-ttu-id="89a5b-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="89a5b-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="89a5b-109">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="89a5b-109">Start</span></span>                 | <span data-ttu-id="89a5b-110">Registrerer et kanban-overførselsjob som igangværende.</span><span class="sxs-lookup"><span data-stu-id="89a5b-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="89a5b-111">Fuldført</span><span class="sxs-lookup"><span data-stu-id="89a5b-111">Complete</span></span>              | <span data-ttu-id="89a5b-112">Registrerer et kanban-overførselsjob som fuldført.</span><span class="sxs-lookup"><span data-stu-id="89a5b-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="89a5b-113">Tom</span><span class="sxs-lookup"><span data-stu-id="89a5b-113">Empty</span></span>                 | <span data-ttu-id="89a5b-114">Registrerer den materialehåndteringsenhed, der refereres til på kanban-kortet, som tom.</span><span class="sxs-lookup"><span data-stu-id="89a5b-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="89a5b-115">Vælg</span><span class="sxs-lookup"><span data-stu-id="89a5b-115">Select</span></span>                | <span data-ttu-id="89a5b-116">Registrerer et kanban-kortnummer og vælger automatisk det job, der refereres til på kanban-listen.</span><span class="sxs-lookup"><span data-stu-id="89a5b-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<span data-ttu-id="89a5b-117">Valg af registreringstilstand</span><span class="sxs-lookup"><span data-stu-id="89a5b-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="89a5b-118">Når du bruger en stregkodelæser til at vælge et job, ændres visningstilstanden for kanban-området.</span><span class="sxs-lookup"><span data-stu-id="89a5b-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span><span data-ttu-id="89a5b-119">I denne tilstand gælder følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="89a5b-119"> In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="89a5b-120">Der vises kun det scannede kanban-job.</span><span class="sxs-lookup"><span data-stu-id="89a5b-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="89a5b-121">Detaljerne om det valgte job vises i oversigtspanelet **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="89a5b-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="89a5b-122">I oversigtspanelet **Meddelelser** vises der kun meddelelser for det valgte job.</span><span class="sxs-lookup"><span data-stu-id="89a5b-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="89a5b-123">Du kan ændre status for jobbet ved hjælp af funktioner, der er tilgængelige i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="89a5b-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="89a5b-124">I kanban-overførselsområdet vises der fortsat kun et enkelt job i denne periode.</span><span class="sxs-lookup"><span data-stu-id="89a5b-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="89a5b-125">Du kan opdatere oplysningerne på listen over job manuelt ved at klikke på **Opdater** (Skift+F5) i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="89a5b-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="89a5b-126">Når du har opdateret oplysningerne, vises de komplette resultater for jobfilteret igen.</span><span class="sxs-lookup"><span data-stu-id="89a5b-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="89a5b-127">Jobstatus og mulige handlinger</span><span class="sxs-lookup"><span data-stu-id="89a5b-127">Job status and possible actions</span></span>
<span data-ttu-id="89a5b-128">Status for det valgte job og status for udlignede job for hændelseskanbans bestemmer, om du kan behandle jobbet yderligere.</span><span class="sxs-lookup"><span data-stu-id="89a5b-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="89a5b-129">I følgende tabel vises oplysninger om disse statusser og opgaver:</span><span class="sxs-lookup"><span data-stu-id="89a5b-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="89a5b-130">De statusser, der er tilgængelige for job eller for materialehåndteringsenheder, der henvises til af jobbene.</span><span class="sxs-lookup"><span data-stu-id="89a5b-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="89a5b-131">Hver opgave, du kan udføre for jobbet.</span><span class="sxs-lookup"><span data-stu-id="89a5b-131">Each task that you can perform for the job.</span></span>

<table>
<colgroup>
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
<col width="12%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="89a5b-132">Jobtype</span><span class="sxs-lookup"><span data-stu-id="89a5b-132">Job type</span></span></th>
<th><span data-ttu-id="89a5b-133">Status for job eller status for materialehåndteringsenhed</span><span class="sxs-lookup"><span data-stu-id="89a5b-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="89a5b-134">Opdater plukliste</span><span class="sxs-lookup"><span data-stu-id="89a5b-134">Update picking list</span></span></th>
<th><span data-ttu-id="89a5b-135">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="89a5b-135">Start</span></span></th>
<th><span data-ttu-id="89a5b-136">Opdater registrering</span><span class="sxs-lookup"><span data-stu-id="89a5b-136">Update registration</span></span></th>
<th><span data-ttu-id="89a5b-137">Fuldført</span><span class="sxs-lookup"><span data-stu-id="89a5b-137">Complete</span></span></th>
<th><span data-ttu-id="89a5b-138">Tom</span><span class="sxs-lookup"><span data-stu-id="89a5b-138">Empty</span></span></th>
<th><span data-ttu-id="89a5b-139">Opret hændelseskanbans</span><span class="sxs-lookup"><span data-stu-id="89a5b-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="89a5b-140">Flytning</span><span class="sxs-lookup"><span data-stu-id="89a5b-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="89a5b-141">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="89a5b-141">Not planned</span></span></li>
<li><span data-ttu-id="89a5b-142">Der er ingen udlignede job, eller udlignede job er fuldførte</span><span class="sxs-lookup"><span data-stu-id="89a5b-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="89a5b-143">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-143">Yes</span></span></td>
<td><span data-ttu-id="89a5b-144">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-144">Yes</span></span></td>
<td><span data-ttu-id="89a5b-145">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-145">Yes</span></span></td>
<td><span data-ttu-id="89a5b-146">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-146">Yes</span></span></td>
<td><span data-ttu-id="89a5b-147">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-147">No</span></span></td>
<td><span data-ttu-id="89a5b-148">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89a5b-149">Flytning</span><span class="sxs-lookup"><span data-stu-id="89a5b-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="89a5b-150">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="89a5b-150">Not planned</span></span></li>
<li><span data-ttu-id="89a5b-151">Det udlignede job er ikke fuldført</span><span class="sxs-lookup"><span data-stu-id="89a5b-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="89a5b-152">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-152">Yes</span></span></td>
<td><span data-ttu-id="89a5b-153">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-153">No</span></span></td>
<td><span data-ttu-id="89a5b-154">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-154">Yes</span></span></td>
<td><span data-ttu-id="89a5b-155">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-155">No</span></span></td>
<td><span data-ttu-id="89a5b-156">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-156">No</span></span></td>
<td><span data-ttu-id="89a5b-157">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89a5b-158">Flytning</span><span class="sxs-lookup"><span data-stu-id="89a5b-158">Transfer</span></span></td>
<td><span data-ttu-id="89a5b-159">I gang</span><span class="sxs-lookup"><span data-stu-id="89a5b-159">In progress</span></span></td>
<td><span data-ttu-id="89a5b-160">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-160">Yes</span></span></td>
<td><span data-ttu-id="89a5b-161">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-161">No</span></span></td>
<td><span data-ttu-id="89a5b-162">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-162">Yes</span></span></td>
<td><span data-ttu-id="89a5b-163">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-163">Yes</span></span></td>
<td><span data-ttu-id="89a5b-164">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-164">No</span></span></td>
<td><span data-ttu-id="89a5b-165">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89a5b-166">Flytning</span><span class="sxs-lookup"><span data-stu-id="89a5b-166">Transfer</span></span></td>
<td><span data-ttu-id="89a5b-167">Gennemført</span><span class="sxs-lookup"><span data-stu-id="89a5b-167">Completed</span></span></td>
<td><span data-ttu-id="89a5b-168">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-168">No</span></span></td>
<td><span data-ttu-id="89a5b-169">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-169">No</span></span></td>
<td><span data-ttu-id="89a5b-170">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-170">No</span></span></td>
<td><span data-ttu-id="89a5b-171">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-171">No</span></span></td>
<td><span data-ttu-id="89a5b-172">Ja</span><span class="sxs-lookup"><span data-stu-id="89a5b-172">Yes</span></span></td>
<td><span data-ttu-id="89a5b-173">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89a5b-174">Overførsel eller proces</span><span class="sxs-lookup"><span data-stu-id="89a5b-174">Transfer or process</span></span></td>
<td><span data-ttu-id="89a5b-175">Tom</span><span class="sxs-lookup"><span data-stu-id="89a5b-175">Empty</span></span></td>
<td><span data-ttu-id="89a5b-176">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-176">No</span></span></td>
<td><span data-ttu-id="89a5b-177">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-177">No</span></span></td>
<td><span data-ttu-id="89a5b-178">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-178">No</span></span></td>
<td><span data-ttu-id="89a5b-179">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-179">No</span></span></td>
<td><span data-ttu-id="89a5b-180">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-180">No</span></span></td>
<td><span data-ttu-id="89a5b-181">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89a5b-182">Overførsel eller proces</span><span class="sxs-lookup"><span data-stu-id="89a5b-182">Transfer or process</span></span></td>
<td><span data-ttu-id="89a5b-183">Der blev ikke fundet et kanban-kort</span><span class="sxs-lookup"><span data-stu-id="89a5b-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="89a5b-184">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-184">No</span></span></td>
<td><span data-ttu-id="89a5b-185">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-185">No</span></span></td>
<td><span data-ttu-id="89a5b-186">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-186">No</span></span></td>
<td><span data-ttu-id="89a5b-187">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-187">No</span></span></td>
<td><span data-ttu-id="89a5b-188">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-188">No</span></span></td>
<td><span data-ttu-id="89a5b-189">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89a5b-190">Overførsel eller proces</span><span class="sxs-lookup"><span data-stu-id="89a5b-190">Transfer or process</span></span></td>
<td><span data-ttu-id="89a5b-191">Der blev fundet et kanban-kort, men det er ikke tildelt til en kanban</span><span class="sxs-lookup"><span data-stu-id="89a5b-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="89a5b-192">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-192">No</span></span></td>
<td><span data-ttu-id="89a5b-193">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-193">No</span></span></td>
<td><span data-ttu-id="89a5b-194">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-194">No</span></span></td>
<td><span data-ttu-id="89a5b-195">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-195">No</span></span></td>
<td><span data-ttu-id="89a5b-196">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-196">No</span></span></td>
<td><span data-ttu-id="89a5b-197">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="89a5b-198">Behandl</span><span class="sxs-lookup"><span data-stu-id="89a5b-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="89a5b-199">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="89a5b-199">Not planned</span></span></li>
<li><span data-ttu-id="89a5b-200">Forberedt</span><span class="sxs-lookup"><span data-stu-id="89a5b-200">Prepared</span></span></li>
<li><span data-ttu-id="89a5b-201">I gang</span><span class="sxs-lookup"><span data-stu-id="89a5b-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="89a5b-202">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-202">No</span></span></td>
<td><span data-ttu-id="89a5b-203">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-203">No</span></span></td>
<td><span data-ttu-id="89a5b-204">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-204">No</span></span></td>
<td><span data-ttu-id="89a5b-205">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-205">No</span></span></td>
<td><span data-ttu-id="89a5b-206">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-206">No</span></span></td>
<td><span data-ttu-id="89a5b-207">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="89a5b-208">Behandl</span><span class="sxs-lookup"><span data-stu-id="89a5b-208">Process</span></span></td>
<td><span data-ttu-id="89a5b-209">Gennemført</span><span class="sxs-lookup"><span data-stu-id="89a5b-209">Completed</span></span></td>
<td><span data-ttu-id="89a5b-210">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-210">No</span></span></td>
<td><span data-ttu-id="89a5b-211">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-211">No</span></span></td>
<td><span data-ttu-id="89a5b-212">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-212">No</span></span></td>
<td><span data-ttu-id="89a5b-213">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-213">No</span></span></td>
<td><span data-ttu-id="89a5b-214">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-214">No</span></span></td>
<td><span data-ttu-id="89a5b-215">Nej</span><span class="sxs-lookup"><span data-stu-id="89a5b-215">No</span></span></td>
</tr>
</tbody>
</table>





