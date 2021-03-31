---
title: Overvåge kørsel af en varedisponering
description: Dette emne beskriver, hvordan produktionsplanlæggeren kan se, om en varedisponeringskørsel er i gang.
author: josaw1
manager: tfehr
ms.date: 11/04/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2dea87ac106e79339b8cb6bb2c28e36e35de4a1a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5226093"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="85c0c-103">Overvåge kørsel af en varedisponering</span><span class="sxs-lookup"><span data-stu-id="85c0c-103">Monitor a master planning run</span></span>

[!include [banner](../../includes/banner.md)]

## <a name="use-a-gantt-chart-to-visualize-master-planning-progress"></a><span data-ttu-id="85c0c-104">Brug et Gantt-diagram til at visualisere status for varedisponering</span><span class="sxs-lookup"><span data-stu-id="85c0c-104">Use a Gantt chart to visualize master planning progress</span></span>

<span data-ttu-id="85c0c-105">På siden **Vis varedisponeringens status** kan du få vist detaljer om den historiske varedisponeringskørsel i form af et Gantt-diagram.</span><span class="sxs-lookup"><span data-stu-id="85c0c-105">From the **View master planning progress** page, you can view details of historical master planning runs as a Gantt chart.</span></span> <span data-ttu-id="85c0c-106">Denne funktionalitet kan hjælpe dig med at forstå den tid, der bruges på de forskellige faser i varedisponeringen.</span><span class="sxs-lookup"><span data-stu-id="85c0c-106">This functionality can help you understand the time that is spent on the various phases of master planning.</span></span> <span data-ttu-id="85c0c-107">For et aktuelt aktivt planlægningsjob kan siden **Vis varedisponeringens status** bruges til at spore statussen og få vist den estimerede resterende tid.</span><span class="sxs-lookup"><span data-stu-id="85c0c-107">For a current active planning job, the **View master planning progress** page can be used to track progress and view the estimated remaining time.</span></span>

### <a name="turn-on-and-use-the-master-plan-progress-visualization-feature"></a><span data-ttu-id="85c0c-108">Aktiver og anvend funktionen Visualisering af varedisponeringens status</span><span class="sxs-lookup"><span data-stu-id="85c0c-108">Turn on and use the Master plan progress visualization feature</span></span>

<span data-ttu-id="85c0c-109">For at anvende denne funktionalitet skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="85c0c-109">To use this functionality, follow these steps.</span></span>

1. <span data-ttu-id="85c0c-110">I arbejdsområdet **Funktionsstyring** på fanen **Ny** skal du vælge **Visualisering af varedisponeringens status** fra listen.</span><span class="sxs-lookup"><span data-stu-id="85c0c-110">In the **Feature management** workspace, on the **New** tab, select **Master planning progress visualization** in the list.</span></span> <span data-ttu-id="85c0c-111">Hvis funktionen ikke vises under den fanen **Ny**, skal du se på fanerne **Ikke aktiverede** og **Alle**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-111">If the feature doesn't appear on the **New** tab, look on the **Not enabled** and **All** tabs.</span></span>
1. <span data-ttu-id="85c0c-112">Vælg **Aktiver nu**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-112">Select **Enable now**.</span></span> <span data-ttu-id="85c0c-113">Du kan også vælge **Planlæg** og derefter vælge det tidspunkt, hvor funktionen skal aktiveres.</span><span class="sxs-lookup"><span data-stu-id="85c0c-113">Alternatively, select **Schedule**, and then select the time when you want the feature to be turned on.</span></span>

<span data-ttu-id="85c0c-114">Siden **Vis varedisponeringens status** kan vise både tidligere planlægningsjobs og aktive planlægningsjobs.</span><span class="sxs-lookup"><span data-stu-id="85c0c-114">The **View master planning progress** page can display both historical planning jobs and active planning jobs.</span></span> 

<span data-ttu-id="85c0c-115">Der er to valgmuligheder for at få vist historiske planlægningsjobs.</span><span class="sxs-lookup"><span data-stu-id="85c0c-115">To view historical planning jobs, there are two options.</span></span> 

1. <span data-ttu-id="85c0c-116">Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**, og i handlingsruden skal du dernæst vælge **Historik**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-116">Go to **Master planning \> Setup \> Plans \> Master plans**, and then, on the Action Pane, select **History**.</span></span> <span data-ttu-id="85c0c-117">Marker **Forespørgsler**, mens det ønskede job er markeret, og vælg derefter **Vis status**</span><span class="sxs-lookup"><span data-stu-id="85c0c-117">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>
1. <span data-ttu-id="85c0c-118">Gå til **Varedisponering \> Arbejdsområder \> Varedisponering**, klik derefter på **Historik** i feltet Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="85c0c-118">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **History**.</span></span> <span data-ttu-id="85c0c-119">Marker **Forespørgsler**, mens det ønskede job er markeret, og vælg derefter **Vis status**</span><span class="sxs-lookup"><span data-stu-id="85c0c-119">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="85c0c-120">Der er to valgmuligheder for at få vist aktive planlægningsjobs.</span><span class="sxs-lookup"><span data-stu-id="85c0c-120">To view active planning jobs, there are two options.</span></span> 
1. <span data-ttu-id="85c0c-121">Gå til **Varedisponering \> Arbejdsområder \> Varedisponering** i handlingsruden, og vælg der **Uafsluttede planlægningsprocess**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-121">Go to **Master planning \> Workspaces \> Master planning**, on the Action Pane, select **Unfinished planning process**.</span></span> <span data-ttu-id="85c0c-122">Marker **Forespørgsler**, mens det ønskede job er markeret, og vælg derefter **Vis status**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-122">With the desired job selected, select **Inquiries**,  and then select **View progress**.</span></span>
1. <span data-ttu-id="85c0c-123">Gå til **Varedisponering \> Arbejdsområder \> Varedisponering**, klik derefter på **Vis status** i feltet Varedisponering.</span><span class="sxs-lookup"><span data-stu-id="85c0c-123">Go to **Master planning \> Workspaces \> Master planning**, on the Master planning tile click **View progress**.</span></span> <span data-ttu-id="85c0c-124">Marker **Forespørgsler**, mens det ønskede job er markeret, og vælg derefter **Vis status**</span><span class="sxs-lookup"><span data-stu-id="85c0c-124">With the desired job selected, select **Inquiries**,  and then select **View progress**</span></span>

<span data-ttu-id="85c0c-125">Bemærk, at du kun kan få vist aktive job, når et planlægningsjob behandles.</span><span class="sxs-lookup"><span data-stu-id="85c0c-125">Note you can view active jobs only when a planning job is processing.</span></span>

### <a name="analyze-a-master-planning-job"></a><span data-ttu-id="85c0c-126">Analyser et varedisponeringsjob</span><span class="sxs-lookup"><span data-stu-id="85c0c-126">Analyze a master planning job</span></span>

<span data-ttu-id="85c0c-127">I Gantt-diagrammet kan du udvide hver af følgende planlægningsprocesser for at få vist flere detaljer om den tid, der er brugt:</span><span class="sxs-lookup"><span data-stu-id="85c0c-127">In the Gantt chart, you can expand each of the following planning processes to view additional details about the time that is spent:</span></span>

- <span data-ttu-id="85c0c-128">Initialisering</span><span class="sxs-lookup"><span data-stu-id="85c0c-128">Initializing</span></span>
- <span data-ttu-id="85c0c-129">Sletter og indsætter data</span><span class="sxs-lookup"><span data-stu-id="85c0c-129">Deleting and inserting data</span></span>
- <span data-ttu-id="85c0c-130">Disponering</span><span class="sxs-lookup"><span data-stu-id="85c0c-130">Coverage planning</span></span>
- <span data-ttu-id="85c0c-131">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="85c0c-131">Delays</span></span>
- <span data-ttu-id="85c0c-132">Handlingsmeddelelser</span><span class="sxs-lookup"><span data-stu-id="85c0c-132">Action messages</span></span>
- <span data-ttu-id="85c0c-133">Færdiggørelse</span><span class="sxs-lookup"><span data-stu-id="85c0c-133">Finalization</span></span>
- <span data-ttu-id="85c0c-134">Automatisk autorisation</span><span class="sxs-lookup"><span data-stu-id="85c0c-134">Auto-firming</span></span>

<span data-ttu-id="85c0c-135">Gantt-diagrammet er et nyttigt værktøj, hvis du vil se indvirkningen af at bruge handlingsbeskeder.</span><span class="sxs-lookup"><span data-stu-id="85c0c-135">The Gantt chart is a useful tool if you want to view the impact of using action messages.</span></span>

#### <a name="navigation-in-the-gantt-chart"></a><span data-ttu-id="85c0c-136">Navigation i Gantt-diagrammet</span><span class="sxs-lookup"><span data-stu-id="85c0c-136">Navigation in the Gantt chart</span></span>

- <span data-ttu-id="85c0c-137">Hvis du vil udvide den valgte gruppe og vise detaljerne, skal du vælge plustegnet (**+**) trævisningen.</span><span class="sxs-lookup"><span data-stu-id="85c0c-137">To expand the selected group and show the details, select the plus sign (**+**) in the tree view.</span></span>
- <span data-ttu-id="85c0c-138">Hvis du vil skjule den markerede gruppe, skal du vælge minustegnet (**–**) i trævisningen.</span><span class="sxs-lookup"><span data-stu-id="85c0c-138">To collapse the selected group, select the minus sign (**–**) in the tree view.</span></span>
- <span data-ttu-id="85c0c-139">Du kan bruge tastaturet til at navigere.</span><span class="sxs-lookup"><span data-stu-id="85c0c-139">You can use your keyboard for navigation.</span></span> <span data-ttu-id="85c0c-140">Brug **Pil op** og **Pil ned** til at flytte mellem rækker.</span><span class="sxs-lookup"><span data-stu-id="85c0c-140">Use the **Up arrow** and **Down arrow** keys to move between rows.</span></span> <span data-ttu-id="85c0c-141">Brug **Højre pil** og **Venstre pile** til at udvide og skjule grupper.</span><span class="sxs-lookup"><span data-stu-id="85c0c-141">Use the **Right arrow** and **Left arrow** keys to expand and collapse groups.</span></span>
- <span data-ttu-id="85c0c-142">Hvis du vil åbne eller lukke alle niveauer i Gantt-diagrammet, skal du vælge **Udvid alle** eller **Skjul alle**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-142">To open or close all levels in the Gantt chart, select **Expand all** or **Collapse all**.</span></span>
- <span data-ttu-id="85c0c-143">Hold markøren over en opgave for at få vist den relaterede behandlingstid.</span><span class="sxs-lookup"><span data-stu-id="85c0c-143">To view the related processing time, hover over a task.</span></span> <span data-ttu-id="85c0c-144">(Opgaver er det laveste niveau i Gantt-diagrammet).</span><span class="sxs-lookup"><span data-stu-id="85c0c-144">(Tasks are the lowest level in the Gantt chart.)</span></span>

#### <a name="view-an-additional-master-planning-run-to-compare-jobs"></a><span data-ttu-id="85c0c-145">Få vist en ekstra varedisponeringskørsel for at sammenligne job</span><span class="sxs-lookup"><span data-stu-id="85c0c-145">View an additional master planning run to compare jobs</span></span>

<span data-ttu-id="85c0c-146">Hvis du vælger et varedisponeringsjob i feltet **Vis yderligere varedisponeringskørsel**, kan du få vist en ekstra varedisponeringskørsel i Gantt-diagrammet og sammenligne de to job.</span><span class="sxs-lookup"><span data-stu-id="85c0c-146">By selecting a master planning job on field **Show additional master planning run**, you can view an additional master planning run in the Gantt chart and compare the two jobs.</span></span>

#### <a name="bom-level-display"></a><span data-ttu-id="85c0c-147">Visning på styklisteniveau</span><span class="sxs-lookup"><span data-stu-id="85c0c-147">BOM-level display</span></span>

<span data-ttu-id="85c0c-148">Styklistelisteniveauer (BOM) vises forskelligt for disponering, forsinkelser, handlinger og autorisation.</span><span class="sxs-lookup"><span data-stu-id="85c0c-148">Bill of materials (BOM) levels are shown differently for coverage planning, delays, actions, and firming.</span></span>

- <span data-ttu-id="85c0c-149">**Disponering** – Styklisteniveauer vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="85c0c-149">**Coverage planning** – BOM levels are shown as expected.</span></span> <span data-ttu-id="85c0c-150">De beregnes fra toppen og ned.</span><span class="sxs-lookup"><span data-stu-id="85c0c-150">They are calculated from the top down.</span></span>

    <span data-ttu-id="85c0c-151">**Eksempel:** Styklisteniveau 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="85c0c-151">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="85c0c-152">**Forsinkelser** – Styklisteniveauer vises som styklisteniveauer for varedisponering multipliceret med –1.</span><span class="sxs-lookup"><span data-stu-id="85c0c-152">**Delays** – BOM levels are shown as the coverage planning BOM levels multiplied by –1.</span></span> <span data-ttu-id="85c0c-153">(Med andre ord har de et negativt tegn).</span><span class="sxs-lookup"><span data-stu-id="85c0c-153">(In other words, they have a negative sign.)</span></span>

    <span data-ttu-id="85c0c-154">**Eksempel:** Styklisteniveau –2, –1, 0</span><span class="sxs-lookup"><span data-stu-id="85c0c-154">**Example:** BOM level –2, –1, 0</span></span>

- <span data-ttu-id="85c0c-155">**Handlingsbesked** – Styklisteniveauer vises som forventet.</span><span class="sxs-lookup"><span data-stu-id="85c0c-155">**Action message** – BOM levels are shown as expected.</span></span> <span data-ttu-id="85c0c-156">De beregnes fra toppen og ned.</span><span class="sxs-lookup"><span data-stu-id="85c0c-156">They are calculated from the top down.</span></span>

    <span data-ttu-id="85c0c-157">**Eksempel:** Styklisteniveau 0, 1, 2</span><span class="sxs-lookup"><span data-stu-id="85c0c-157">**Example:** BOM level 0, 1, 2</span></span>

- <span data-ttu-id="85c0c-158">**Auto-autorisering** – Styklisteniveauer vises som 999 minus styklisteniveauet for disponeringsplanlægning.</span><span class="sxs-lookup"><span data-stu-id="85c0c-158">**Auto-firming** – BOM levels are shown as 999 minus the coverage planning BOM level.</span></span>

    <span data-ttu-id="85c0c-159">**Eksempel:** Styklisteniveau 999, 998, 997</span><span class="sxs-lookup"><span data-stu-id="85c0c-159">**Example:** BOM level 999, 998, 997</span></span>

<span data-ttu-id="85c0c-160">I følgende tabel vises en oversigt over problemet.</span><span class="sxs-lookup"><span data-stu-id="85c0c-160">The following table summarizes the behavior.</span></span>

| <span data-ttu-id="85c0c-161">Det viste styklisteniveau</span><span class="sxs-lookup"><span data-stu-id="85c0c-161">BOM level that is shown</span></span> | <span data-ttu-id="85c0c-162">Slutvare</span><span class="sxs-lookup"><span data-stu-id="85c0c-162">End item</span></span> | <span data-ttu-id="85c0c-163">Underkomponent</span><span class="sxs-lookup"><span data-stu-id="85c0c-163">Subcomponent</span></span> | <span data-ttu-id="85c0c-164">Råvarer</span><span class="sxs-lookup"><span data-stu-id="85c0c-164">Raw material</span></span> |
|---|---|---|---|
| <span data-ttu-id="85c0c-165">Disponering</span><span class="sxs-lookup"><span data-stu-id="85c0c-165">Coverage planning</span></span> | <span data-ttu-id="85c0c-166">0</span><span class="sxs-lookup"><span data-stu-id="85c0c-166">0</span></span> | <span data-ttu-id="85c0c-167">1</span><span class="sxs-lookup"><span data-stu-id="85c0c-167">1</span></span> | <span data-ttu-id="85c0c-168">2</span><span class="sxs-lookup"><span data-stu-id="85c0c-168">2</span></span> |
| <span data-ttu-id="85c0c-169">Forsinkelser</span><span class="sxs-lookup"><span data-stu-id="85c0c-169">Delays</span></span> | <span data-ttu-id="85c0c-170">0</span><span class="sxs-lookup"><span data-stu-id="85c0c-170">0</span></span> | <span data-ttu-id="85c0c-171">–1</span><span class="sxs-lookup"><span data-stu-id="85c0c-171">–1</span></span> | <span data-ttu-id="85c0c-172">–2</span><span class="sxs-lookup"><span data-stu-id="85c0c-172">–2</span></span> |
| <span data-ttu-id="85c0c-173">Handlingsmeddelelse</span><span class="sxs-lookup"><span data-stu-id="85c0c-173">Action message</span></span> | <span data-ttu-id="85c0c-174">0</span><span class="sxs-lookup"><span data-stu-id="85c0c-174">0</span></span> | <span data-ttu-id="85c0c-175">1</span><span class="sxs-lookup"><span data-stu-id="85c0c-175">1</span></span> | <span data-ttu-id="85c0c-176">2</span><span class="sxs-lookup"><span data-stu-id="85c0c-176">2</span></span> |
| <span data-ttu-id="85c0c-177">Automatisk autorisation</span><span class="sxs-lookup"><span data-stu-id="85c0c-177">Auto-firming</span></span> | <span data-ttu-id="85c0c-178">999</span><span class="sxs-lookup"><span data-stu-id="85c0c-178">999</span></span> | <span data-ttu-id="85c0c-179">998</span><span class="sxs-lookup"><span data-stu-id="85c0c-179">998</span></span> | <span data-ttu-id="85c0c-180">997</span><span class="sxs-lookup"><span data-stu-id="85c0c-180">997</span></span> |

#### <a name="visualize-progress"></a><span data-ttu-id="85c0c-181">Visualiser status</span><span class="sxs-lookup"><span data-stu-id="85c0c-181">Visualize progress</span></span>

<span data-ttu-id="85c0c-182">Hvis du får vist et varedisponeringsjob, der kører, vises status i Gantt-diagrammets farver.</span><span class="sxs-lookup"><span data-stu-id="85c0c-182">If you view a master planning job that is currently running, progress is shown through colors in the Gantt chart.</span></span> <span data-ttu-id="85c0c-183">Der gælder følgende farver for det blå tema:</span><span class="sxs-lookup"><span data-stu-id="85c0c-183">The following colors apply to the blue theme.</span></span> <span data-ttu-id="85c0c-184">I forbindelse med andre farvetemaer vil farverne være forskellige.</span><span class="sxs-lookup"><span data-stu-id="85c0c-184">For other color themes, the colors will differ.</span></span>

- <span data-ttu-id="85c0c-185">**Mørkeblå** – Fuldførte planlægningsopgaver.</span><span class="sxs-lookup"><span data-stu-id="85c0c-185">**Dark blue** – Completed planning tasks.</span></span>
- <span data-ttu-id="85c0c-186">**Orange** – Den opgave, der er i gang i øjeblikket.</span><span class="sxs-lookup"><span data-stu-id="85c0c-186">**Orange** – The task that is currently in progress.</span></span>
- <span data-ttu-id="85c0c-187">**Lyseblå** – Estimatet for de resterende opgaver.</span><span class="sxs-lookup"><span data-stu-id="85c0c-187">**Light blue** – The estimate for remaining tasks.</span></span>

<span data-ttu-id="85c0c-188">Farven vises kun på det laveste niveau i Gantt-diagrammet.</span><span class="sxs-lookup"><span data-stu-id="85c0c-188">The color is shown only on the lowest level in the Gantt chart.</span></span> <span data-ttu-id="85c0c-189">Vælg **Udvid alle** for at få vist alle opgaver i varedisponeringsjobbet.</span><span class="sxs-lookup"><span data-stu-id="85c0c-189">Select **Expand all** to view all tasks in the master planning job.</span></span> <span data-ttu-id="85c0c-190">Estimatet for resterende opgaver er baseret på historiske varedisponeringsjob.</span><span class="sxs-lookup"><span data-stu-id="85c0c-190">The estimate of remaining tasks is based on historical master planning jobs.</span></span>

## <a name="run-master-planning-and-track-processing-time"></a><span data-ttu-id="85c0c-191">Kør varedisponering og registrer procestiden</span><span class="sxs-lookup"><span data-stu-id="85c0c-191">Run master planning and track processing time</span></span>

1. <span data-ttu-id="85c0c-192">Vælg **Varedisponering** på standarddashboardet.</span><span class="sxs-lookup"><span data-stu-id="85c0c-192">On the default dashboard, select **Master planning**.</span></span>
1. <span data-ttu-id="85c0c-193">I feltet **Plan** indtastes eller vælges en værdi.</span><span class="sxs-lookup"><span data-stu-id="85c0c-193">In the **Plan** field, enter or select a value.</span></span>
1. <span data-ttu-id="85c0c-194">Vælg **Kør**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-194">Select **Run**.</span></span>
1. <span data-ttu-id="85c0c-195">Angiv indstillingen i **Registrer procestiden** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-195">Set the **Track processing time** option to **Yes**.</span></span>
1. <span data-ttu-id="85c0c-196">Indtast et antal i feltet **Antal tråde**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-196">In the **Number of threads** field, enter a number.</span></span>
1. <span data-ttu-id="85c0c-197">I oversigtspanelet **Medtagne poster** skal du vælge **Filtrer**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-197">On the **Records to include** FastTab, select **Filter**.</span></span>
1. <span data-ttu-id="85c0c-198">I gitteret skal du vælge den række, hvor feltet **Felt** er angivet til **Varenummer**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-198">In the grid, select the row where the **Field** field is set to **Item number**.</span></span>
1. <span data-ttu-id="85c0c-199">Angiv en værdi i feltet **Kriterie**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-199">In the **Criteria** field, enter a value.</span></span>
1. <span data-ttu-id="85c0c-200">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="85c0c-200">Select **OK**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]