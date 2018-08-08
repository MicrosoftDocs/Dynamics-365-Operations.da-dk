---
title: "Kanban-området for overførsel understøtter stregkodescannere"
description: "Kanban-områdetet understøtter scannerinput fra en widget stregkodescanner til at vælge, starte, udfylde og tømme et kanban-job."
author: ChristianRytt
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: KanbanBoardTransferJob
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 19391
ms.assetid: a426f645-d59b-4c98-8d78-eba8d64a562e
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: d9747ba144d56c9410846769e5465372c89ea111
ms.openlocfilehash: e63a33af63144b78d0c375022b9802e11c255598
ms.contentlocale: da-dk
ms.lasthandoff: 08/07/2018

---

# <a name="kanban-transfer-board-support-for-barcode-scanners"></a><span data-ttu-id="075f4-103">Kanban-området for overførsel understøtter stregkodescannere</span><span class="sxs-lookup"><span data-stu-id="075f4-103">Kanban transfer board support for barcode scanners</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="075f4-104">Kanban-områdetet understøtter scannerinput fra en widget stregkodescanner til at vælge, starte, udfylde og tømme et kanban-job.</span><span class="sxs-lookup"><span data-stu-id="075f4-104">The Kanban transfer board supports scanner input from a widget barcode scanner to Select, Start, Complete, and Empty a kanban job.</span></span>

<a name="registration-modes"></a><span data-ttu-id="075f4-105">Registreringstilstande</span><span class="sxs-lookup"><span data-stu-id="075f4-105">Registration modes</span></span>
------------------

<span data-ttu-id="075f4-106">På oversigtspanelet **Scanner registrering** kan du vælge den registreringstilstand, der styrer handlingen, når du scanner et kanban-kortnummer eller manuelt skriver tallet i feltet med kanban-kortet.</span><span class="sxs-lookup"><span data-stu-id="075f4-106">On the **Scanner registration** FastTab you can select the registration mode, which controls the action when you scan a kanban card number or manually type the number in the Kanban card number field.</span></span>

| <span data-ttu-id="075f4-107">Angiv registreringstilstand</span><span class="sxs-lookup"><span data-stu-id="075f4-107">Set registration mode</span></span> | <span data-ttu-id="075f4-108">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="075f4-108">Description</span></span>                                                                                     |
|-----------------------|-------------------------------------------------------------------------------------------------|
| <span data-ttu-id="075f4-109">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="075f4-109">Start</span></span>                 | <span data-ttu-id="075f4-110">Registrerer et kanban-overførselsjob som igangværende.</span><span class="sxs-lookup"><span data-stu-id="075f4-110">Registers a Kanban transfer job as in progress.</span></span>                                                 |
| <span data-ttu-id="075f4-111">Fuldført</span><span class="sxs-lookup"><span data-stu-id="075f4-111">Complete</span></span>              | <span data-ttu-id="075f4-112">Registrerer et kanban-overførselsjob som fuldført.</span><span class="sxs-lookup"><span data-stu-id="075f4-112">Registers a Kanban transfer job as completed.</span></span>                                                   |
| <span data-ttu-id="075f4-113">Tom</span><span class="sxs-lookup"><span data-stu-id="075f4-113">Empty</span></span>                 | <span data-ttu-id="075f4-114">Registrerer den materialehåndteringsenhed, der refereres til på kanban-kortet, som tom.</span><span class="sxs-lookup"><span data-stu-id="075f4-114">Registers the material handling unit that is referenced by a Kanban card as empty.</span></span>              |
| <span data-ttu-id="075f4-115">Vælg</span><span class="sxs-lookup"><span data-stu-id="075f4-115">Select</span></span>                | <span data-ttu-id="075f4-116">Registrerer et kanban-kortnummer og vælger automatisk det job, der refereres til på kanban-listen.</span><span class="sxs-lookup"><span data-stu-id="075f4-116">Registers a Kanban card number and automatically selects the referenced job in the Kanban list.</span></span> |

 
<a name="registration-mode-select"></a><span data-ttu-id="075f4-117">Valg af registreringstilstand</span><span class="sxs-lookup"><span data-stu-id="075f4-117">Registration mode Select</span></span>
------------------------

<span data-ttu-id="075f4-118">Når du bruger en stregkodelæser til at vælge et job, ændres visningstilstanden for kanban-området.</span><span class="sxs-lookup"><span data-stu-id="075f4-118">When you use a bar code reader to select a job, the display mode of the kanban board changes.</span></span> <span data-ttu-id="075f4-119">I denne tilstand gælder følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="075f4-119">In this mode, the following conditions apply:</span></span>

-   <span data-ttu-id="075f4-120">Der vises kun det scannede kanban-job.</span><span class="sxs-lookup"><span data-stu-id="075f4-120">Only the scanned kanban job is displayed.</span></span>
-   <span data-ttu-id="075f4-121">Detaljerne om det valgte job vises i oversigtspanelet **Detaljer**.</span><span class="sxs-lookup"><span data-stu-id="075f4-121">The details of the selected job are displayed in the **Details** FastTab.</span></span>
-   <span data-ttu-id="075f4-122">I oversigtspanelet **Meddelelser** vises der kun meddelelser for det valgte job.</span><span class="sxs-lookup"><span data-stu-id="075f4-122">The **Messages** FastTab displays messages only for the selected job.</span></span>
-   <span data-ttu-id="075f4-123">Du kan ændre status for jobbet ved hjælp af funktioner, der er tilgængelige i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="075f4-123">You can change the status of the job by using the functions that are available on the Action Pane.</span></span> <span data-ttu-id="075f4-124">I kanban-overførselsområdet vises der fortsat kun et enkelt job i denne periode.</span><span class="sxs-lookup"><span data-stu-id="075f4-124">The Kanban transfer board continues to display only a single job during this time.</span></span>
-   <span data-ttu-id="075f4-125">Du kan opdatere oplysningerne på listen over job manuelt ved at klikke på **Opdater** (Skift+F5) i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="075f4-125">You can update the information in the list of jobs manually by clicking **Refresh** (Shift+F5) on the Action Pane.</span></span> <span data-ttu-id="075f4-126">Når du har opdateret oplysningerne, vises de komplette resultater for jobfilteret igen.</span><span class="sxs-lookup"><span data-stu-id="075f4-126">After you refresh the information, the full results for the job filter are displayed again.</span></span>

## <a name="job-status-and-possible-actions"></a><span data-ttu-id="075f4-127">Jobstatus og mulige handlinger</span><span class="sxs-lookup"><span data-stu-id="075f4-127">Job status and possible actions</span></span>
<span data-ttu-id="075f4-128">Status for det valgte job og status for udlignede job for hændelseskanbans bestemmer, om du kan behandle jobbet yderligere.</span><span class="sxs-lookup"><span data-stu-id="075f4-128">The status of the selected job and the status of any pegged jobs for event kanbans, determine whether you can process the job further.</span></span> <span data-ttu-id="075f4-129">I følgende tabel vises oplysninger om disse statusser og opgaver:</span><span class="sxs-lookup"><span data-stu-id="075f4-129">The following table displays information about these statuses and tasks:</span></span>
-   <span data-ttu-id="075f4-130">De statusser, der er tilgængelige for job eller for materialehåndteringsenheder, der henvises til af jobbene.</span><span class="sxs-lookup"><span data-stu-id="075f4-130">The statuses that are available for jobs, or for the handling units that are referenced by the jobs.</span></span>
-   <span data-ttu-id="075f4-131">Hver opgave, du kan udføre for jobbet.</span><span class="sxs-lookup"><span data-stu-id="075f4-131">Each task that you can perform for the job.</span></span>

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
<th><span data-ttu-id="075f4-132">Jobtype</span><span class="sxs-lookup"><span data-stu-id="075f4-132">Job type</span></span></th>
<th><span data-ttu-id="075f4-133">Status for job eller status for materialehåndteringsenhed</span><span class="sxs-lookup"><span data-stu-id="075f4-133">Job status or handling unit status</span></span></th>
<th><span data-ttu-id="075f4-134">Opdater plukliste</span><span class="sxs-lookup"><span data-stu-id="075f4-134">Update picking list</span></span></th>
<th><span data-ttu-id="075f4-135">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="075f4-135">Start</span></span></th>
<th><span data-ttu-id="075f4-136">Opdater registrering</span><span class="sxs-lookup"><span data-stu-id="075f4-136">Update registration</span></span></th>
<th><span data-ttu-id="075f4-137">Fuldført</span><span class="sxs-lookup"><span data-stu-id="075f4-137">Complete</span></span></th>
<th><span data-ttu-id="075f4-138">Tom</span><span class="sxs-lookup"><span data-stu-id="075f4-138">Empty</span></span></th>
<th><span data-ttu-id="075f4-139">Opret hændelseskanbans</span><span class="sxs-lookup"><span data-stu-id="075f4-139">Create event kanbans</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="075f4-140">Flytning</span><span class="sxs-lookup"><span data-stu-id="075f4-140">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="075f4-141">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="075f4-141">Not planned</span></span></li>
<li><span data-ttu-id="075f4-142">Der er ingen udlignede job, eller udlignede job er fuldførte</span><span class="sxs-lookup"><span data-stu-id="075f4-142">No pegged jobs, or pegged jobs are Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="075f4-143">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-143">Yes</span></span></td>
<td><span data-ttu-id="075f4-144">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-144">Yes</span></span></td>
<td><span data-ttu-id="075f4-145">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-145">Yes</span></span></td>
<td><span data-ttu-id="075f4-146">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-146">Yes</span></span></td>
<td><span data-ttu-id="075f4-147">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-147">No</span></span></td>
<td><span data-ttu-id="075f4-148">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-148">Yes</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="075f4-149">Flytning</span><span class="sxs-lookup"><span data-stu-id="075f4-149">Transfer</span></span></td>
<td><ul>
<li><span data-ttu-id="075f4-150">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="075f4-150">Not planned</span></span></li>
<li><span data-ttu-id="075f4-151">Det udlignede job er ikke fuldført</span><span class="sxs-lookup"><span data-stu-id="075f4-151">The pegged job is not Completed</span></span></li>
</ul></td>
<td><span data-ttu-id="075f4-152">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-152">Yes</span></span></td>
<td><span data-ttu-id="075f4-153">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-153">No</span></span></td>
<td><span data-ttu-id="075f4-154">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-154">Yes</span></span></td>
<td><span data-ttu-id="075f4-155">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-155">No</span></span></td>
<td><span data-ttu-id="075f4-156">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-156">No</span></span></td>
<td><span data-ttu-id="075f4-157">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-157">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="075f4-158">Flytning</span><span class="sxs-lookup"><span data-stu-id="075f4-158">Transfer</span></span></td>
<td><span data-ttu-id="075f4-159">I gang</span><span class="sxs-lookup"><span data-stu-id="075f4-159">In progress</span></span></td>
<td><span data-ttu-id="075f4-160">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-160">Yes</span></span></td>
<td><span data-ttu-id="075f4-161">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-161">No</span></span></td>
<td><span data-ttu-id="075f4-162">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-162">Yes</span></span></td>
<td><span data-ttu-id="075f4-163">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-163">Yes</span></span></td>
<td><span data-ttu-id="075f4-164">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-164">No</span></span></td>
<td><span data-ttu-id="075f4-165">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-165">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="075f4-166">Flytning</span><span class="sxs-lookup"><span data-stu-id="075f4-166">Transfer</span></span></td>
<td><span data-ttu-id="075f4-167">Gennemført</span><span class="sxs-lookup"><span data-stu-id="075f4-167">Completed</span></span></td>
<td><span data-ttu-id="075f4-168">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-168">No</span></span></td>
<td><span data-ttu-id="075f4-169">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-169">No</span></span></td>
<td><span data-ttu-id="075f4-170">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-170">No</span></span></td>
<td><span data-ttu-id="075f4-171">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-171">No</span></span></td>
<td><span data-ttu-id="075f4-172">Ja</span><span class="sxs-lookup"><span data-stu-id="075f4-172">Yes</span></span></td>
<td><span data-ttu-id="075f4-173">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-173">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="075f4-174">Overførsel eller proces</span><span class="sxs-lookup"><span data-stu-id="075f4-174">Transfer or process</span></span></td>
<td><span data-ttu-id="075f4-175">Tom</span><span class="sxs-lookup"><span data-stu-id="075f4-175">Empty</span></span></td>
<td><span data-ttu-id="075f4-176">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-176">No</span></span></td>
<td><span data-ttu-id="075f4-177">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-177">No</span></span></td>
<td><span data-ttu-id="075f4-178">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-178">No</span></span></td>
<td><span data-ttu-id="075f4-179">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-179">No</span></span></td>
<td><span data-ttu-id="075f4-180">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-180">No</span></span></td>
<td><span data-ttu-id="075f4-181">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-181">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="075f4-182">Overførsel eller proces</span><span class="sxs-lookup"><span data-stu-id="075f4-182">Transfer or process</span></span></td>
<td><span data-ttu-id="075f4-183">Der blev ikke fundet et kanban-kort</span><span class="sxs-lookup"><span data-stu-id="075f4-183">A kanban card is not found</span></span></td>
<td><span data-ttu-id="075f4-184">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-184">No</span></span></td>
<td><span data-ttu-id="075f4-185">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-185">No</span></span></td>
<td><span data-ttu-id="075f4-186">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-186">No</span></span></td>
<td><span data-ttu-id="075f4-187">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-187">No</span></span></td>
<td><span data-ttu-id="075f4-188">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-188">No</span></span></td>
<td><span data-ttu-id="075f4-189">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-189">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="075f4-190">Overførsel eller proces</span><span class="sxs-lookup"><span data-stu-id="075f4-190">Transfer or process</span></span></td>
<td><span data-ttu-id="075f4-191">Der blev fundet et kanban-kort, men det er ikke tildelt til en kanban</span><span class="sxs-lookup"><span data-stu-id="075f4-191">A kanban card is found, but it is not assigned to a kanban</span></span></td>
<td><span data-ttu-id="075f4-192">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-192">No</span></span></td>
<td><span data-ttu-id="075f4-193">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-193">No</span></span></td>
<td><span data-ttu-id="075f4-194">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-194">No</span></span></td>
<td><span data-ttu-id="075f4-195">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-195">No</span></span></td>
<td><span data-ttu-id="075f4-196">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-196">No</span></span></td>
<td><span data-ttu-id="075f4-197">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-197">No</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="075f4-198">Behandl</span><span class="sxs-lookup"><span data-stu-id="075f4-198">Process</span></span></td>
<td><ul>
<li><span data-ttu-id="075f4-199">Ikke planlagt</span><span class="sxs-lookup"><span data-stu-id="075f4-199">Not planned</span></span></li>
<li><span data-ttu-id="075f4-200">Forberedt</span><span class="sxs-lookup"><span data-stu-id="075f4-200">Prepared</span></span></li>
<li><span data-ttu-id="075f4-201">I gang</span><span class="sxs-lookup"><span data-stu-id="075f4-201">In progress</span></span></li>
</ul></td>
<td><span data-ttu-id="075f4-202">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-202">No</span></span></td>
<td><span data-ttu-id="075f4-203">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-203">No</span></span></td>
<td><span data-ttu-id="075f4-204">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-204">No</span></span></td>
<td><span data-ttu-id="075f4-205">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-205">No</span></span></td>
<td><span data-ttu-id="075f4-206">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-206">No</span></span></td>
<td><span data-ttu-id="075f4-207">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-207">No</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="075f4-208">Behandl</span><span class="sxs-lookup"><span data-stu-id="075f4-208">Process</span></span></td>
<td><span data-ttu-id="075f4-209">Gennemført</span><span class="sxs-lookup"><span data-stu-id="075f4-209">Completed</span></span></td>
<td><span data-ttu-id="075f4-210">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-210">No</span></span></td>
<td><span data-ttu-id="075f4-211">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-211">No</span></span></td>
<td><span data-ttu-id="075f4-212">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-212">No</span></span></td>
<td><span data-ttu-id="075f4-213">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-213">No</span></span></td>
<td><span data-ttu-id="075f4-214">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-214">No</span></span></td>
<td><span data-ttu-id="075f4-215">Nej</span><span class="sxs-lookup"><span data-stu-id="075f4-215">No</span></span></td>
</tr>
</tbody>
</table>






