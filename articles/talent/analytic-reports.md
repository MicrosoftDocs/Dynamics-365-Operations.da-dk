---
title: Bruge analytiske rapporter i Microsoft Dynamics 365 Talent - Attract
description: Dette emne beskriver de analytiske rapporter til indsigt i ansættelsesprocessen i Microsoft Dynamics 365 Talent - Attract
author: fewatson
manager: AnnBe
ms.date: 04/30/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: fewatson
ms.search.validFrom: 2019-04-30
ms.dyn365.ops.version: Talent April 2019 update
ms.openlocfilehash: be62fe9a5021cfa83a465d316b182c0a154c0c50
ms.sourcegitcommit: 434dd21450bddcd891aba0555b9853d9ba0afb6f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/23/2019
ms.locfileid: "2010000"
---
# <a name="use-analytic-reports"></a><span data-ttu-id="e1ba7-103">Bruge analyserapporter</span><span class="sxs-lookup"><span data-stu-id="e1ba7-103">Use analytic reports</span></span>

<span data-ttu-id="e1ba7-104">Analytiske rapporter i Microsoft Dynamics 365 Talent: Attract indeholder en out-of-the-box (OOTB)-løsning, der giver indsigt i ansættelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-104">Analytic reports in Microsoft Dynamics 365 Talent: Attract provide an out-of-the-box (OOTB) solution for hiring process insights.</span></span> <span data-ttu-id="e1ba7-105">Tilgængelige funktioner omfatter:</span><span class="sxs-lookup"><span data-stu-id="e1ba7-105">Availabe features include:</span></span>

- <span data-ttu-id="e1ba7-106">**Jobanalyser:** Klik på fanen **Analyser** i det job for at se målværdier for jobansøgere.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-106">**Job analytics:** Click the **Analytics** tab within a job for metrics on the job's applicants.</span></span>
- <span data-ttu-id="e1ba7-107">**Analysehub:** Klik på **Analyser** i venstre navigationslinje for at se samlet metrik på tværs af job.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-107">**Analytics hub:** Click **Analytics** on the left navigation for aggregated metrics across jobs.</span></span>
- <span data-ttu-id="e1ba7-108">**Brugerspecifik sikkerhed:** Adgang til rapporter styres af Attract-[rolle](security-attract.md) og jobdeltagerrolle.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-108">**User-specific security:** Access to reports is controlled by Attract [role](security-attract.md) and job participant role.</span></span>
- <span data-ttu-id="e1ba7-109">**Tværgående filtrering:** Klik på visuelle elementer i en rapport for at få vist andre målepunkter, der er filtreret efter udvalgte data.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-109">**Cross-filtering:** Click visuals within a report to view other metrics filtered by selected data.</span></span>

>[!NOTE] 
>- <span data-ttu-id="e1ba7-110">Denne funktion findes på nuværende tidspunkt i [prøveversionen](access-preview-feature.md).</span><span class="sxs-lookup"><span data-stu-id="e1ba7-110">This feature is currently in [preview](access-preview-feature.md).</span></span> <span data-ttu-id="e1ba7-111">Hvis du vil prøve den, skal du have [**Tilføjelsesprogrammet Omfattende ansættelser**](attract-comprehensive-hiring.md).</span><span class="sxs-lookup"><span data-stu-id="e1ba7-111">To try it, you must have the [**Comprehensive Hiring Add-On**](attract-comprehensive-hiring.md).</span></span>
>- <span data-ttu-id="e1ba7-112">Alle rapporter for offentlig visning vises på engelsk.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-112">All public preview reports are displayed in English.</span></span>
>- <span data-ttu-id="e1ba7-113">Rapporter opdateres hver 3. time.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-113">Reports refresh every 3 hours.</span></span> <span data-ttu-id="e1ba7-114">Den seneste opdateringstidspunkt (i den lokale tidszone) findes øverst i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-114">The last refresh time (in the local timezone) is located at the top of the report.</span></span> <span data-ttu-id="e1ba7-115">Opdateringstiderne er en tilnærmelse og varierer afhængigt af datamængde og ressourcebelastning i dit område.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-115">Refresh times are an approximation and vary based on data volume and resource load in your region.</span></span>

## <a name="job-analytics"></a><span data-ttu-id="e1ba7-116">Jobanalyser</span><span class="sxs-lookup"><span data-stu-id="e1ba7-116">Job Analytics</span></span>

<span data-ttu-id="e1ba7-117">Jobanalyse-rapporter er et øjebliksbillede af ansættelsesprocessen for et job.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-117">Job Analytics reports are a snapshot of the hiring process for a job.</span></span>  <span data-ttu-id="e1ba7-118">Nøgleværdier omfatter:</span><span class="sxs-lookup"><span data-stu-id="e1ba7-118">Key metrics include:</span></span>

- <span data-ttu-id="e1ba7-119">Aktive ansøgere efter stadie</span><span class="sxs-lookup"><span data-stu-id="e1ba7-119">Active applicants by stage</span></span>
- <span data-ttu-id="e1ba7-120">Ansøgningskilde</span><span class="sxs-lookup"><span data-stu-id="e1ba7-120">Applicant source</span></span>
- <span data-ttu-id="e1ba7-121">Ansøgertype (intern eller ekstern)</span><span class="sxs-lookup"><span data-stu-id="e1ba7-121">Applicant type (internal or external)</span></span>

## <a name="analytics-hub"></a><span data-ttu-id="e1ba7-122">Analysehub</span><span class="sxs-lookup"><span data-stu-id="e1ba7-122">Analytics Hub</span></span>

<span data-ttu-id="e1ba7-123">Analysehub-rapporter samler jobdata på tværs af job for at vise tendenser i ansættelsesprocessen.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-123">Analytics Hub reports aggregate data across jobs to surface trends in the hiring process.</span></span> <span data-ttu-id="e1ba7-124">Attract omfatter to OOTB-rapporter: Oversigt over pipeline og Tragtanalyse.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-124">Attract includes two OOTB reports: Pipeline Summary and Funnel Analysis.</span></span>

### <a name="pipeline-summary"></a><span data-ttu-id="e1ba7-125">Oversigt over pipeline</span><span class="sxs-lookup"><span data-stu-id="e1ba7-125">Pipeline Summary</span></span>

<span data-ttu-id="e1ba7-126">Rapporten Oversigt over pipeline samler data til åbne job.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-126">The Pipeline Summary report aggregates data for open jobs.</span></span> <span data-ttu-id="e1ba7-127">Nøgleværdier omfatter:</span><span class="sxs-lookup"><span data-stu-id="e1ba7-127">Key metrics include:</span></span>

- <span data-ttu-id="e1ba7-128">Ansøgere på tværs af alle job efter stadie</span><span class="sxs-lookup"><span data-stu-id="e1ba7-128">Applicants across all jobs by stage</span></span>
- <span data-ttu-id="e1ba7-129">Ansøgningskilde</span><span class="sxs-lookup"><span data-stu-id="e1ba7-129">Applicant source</span></span>
- <span data-ttu-id="e1ba7-130">Åbne job efter anciennitetsniveau</span><span class="sxs-lookup"><span data-stu-id="e1ba7-130">Open jobs by seniority level</span></span>

### <a name="funnel-analysis"></a><span data-ttu-id="e1ba7-131">Tragtanalyse</span><span class="sxs-lookup"><span data-stu-id="e1ba7-131">Funnel Analysis</span></span>

<span data-ttu-id="e1ba7-132">Tragtanalyserapporten samler data for job, der er lukket som udfyldte.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-132">The Funnel Analysis report aggregates data for jobs that have been closed as filled.</span></span> <span data-ttu-id="e1ba7-133">Nøgleværdier omfatter:</span><span class="sxs-lookup"><span data-stu-id="e1ba7-133">Key metrics include:</span></span>

- <span data-ttu-id="e1ba7-134">Tidsforløb for ansættelse</span><span class="sxs-lookup"><span data-stu-id="e1ba7-134">Time to hire</span></span>
- <span data-ttu-id="e1ba7-135">Omregningsmetrik (ved pegning)</span><span class="sxs-lookup"><span data-stu-id="e1ba7-135">Conversion metrics (on hover)</span></span>
- <span data-ttu-id="e1ba7-136">Hyppighed af tilbudsaccept</span><span class="sxs-lookup"><span data-stu-id="e1ba7-136">Offer acceptance rate</span></span>

<span data-ttu-id="e1ba7-137">Bemærk! For at få det mest nøjagtige billede af, hvor lang tid en ansættelse tager, anbefales det, at du bruger [Tilbudsstyring](offer-setup.md), en funktionen, der er tilgængelig som en del af tilføjelsesprogrammet Omfattende ansættelser.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-137">Note: For the most accurate time to hire reporting, it is recommended that you use [Offer management](offer-setup.md), a feature available as part of the Comprehensive Hiring Add-On.</span></span>

>[!TIP] 
><span data-ttu-id="e1ba7-138">Prøv at pege på visuelle elementer for at få flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-138">Try hovering over visuals for additional information.</span></span> <span data-ttu-id="e1ba7-139">Hvis du f.eks. peger på **Aktive ansøgere**, viser visuelle elementer de gennemsnitlige dage i fasen.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-139">For example, hovering over **Active applicants** visuals will display the average days in stage.</span></span> <span data-ttu-id="e1ba7-140">Analyse af disse oplysninger kan give indsigt, der er vigtig for at reducere den tid, ansættelsen tager, og give rekrutteringspersoner mulighed for at fokusere på, hvordan de kan reducere den tid, der bruges på de enkelte stadier.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-140">Analyzing this information can provide insights critical to reducing time to hire and enable recruiters to focus on ways to reduce the time spent in each stage.</span></span>

## <a name="user-specific-security"></a><span data-ttu-id="e1ba7-141">Brugerspecifik sikkerhed</span><span class="sxs-lookup"><span data-stu-id="e1ba7-141">User-specific security</span></span>

<span data-ttu-id="e1ba7-142">Attract-rapporter er tilgængelige for administrator-, læs alle-, rekrutterings- og ansættelseschef [roller](security-attract.md).</span><span class="sxs-lookup"><span data-stu-id="e1ba7-142">Attract reports are accessible for Admin, Read All, Recruiter, and Hiring Manager [roles](security-attract.md).</span></span> <span data-ttu-id="e1ba7-143">Ikke-tildelte brugere har ikke adgang til nogen af de analytiske rapportsider (Jobanalyser og Analysehub).</span><span class="sxs-lookup"><span data-stu-id="e1ba7-143">Unassigned users do not have access to either of the analytic report pages (Job Analytics or Analytics Hub).</span></span>

<span data-ttu-id="e1ba7-144">Jobanalyser-rapporter viser data for det valgte job.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-144">Job Analytics reports display data for the selected job.</span></span> <span data-ttu-id="e1ba7-145">Analysehub-rapporter samler data på tværs af alle job, som en bruger kan få vist.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-145">Analytics Hub reports aggregate data across all jobs a user can view.</span></span> <span data-ttu-id="e1ba7-146">Brugere, der kan få vist både Mine job og Alle job på siden Job, har de samme tilgængelige visninger i analysehubben.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-146">Users that can view both My jobs and All jobs on the Jobs page have the same views available in the Analytics Hub.</span></span>

## <a name="cross-filter"></a><span data-ttu-id="e1ba7-147">Tværgående filtrer</span><span class="sxs-lookup"><span data-stu-id="e1ba7-147">Cross-filter</span></span>

<span data-ttu-id="e1ba7-148">En af de fantastiske funktioner i Power BI er den måde, som alle visuelle elementer på en rapportside er forbundet på.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-148">One of the great features of Power BI is the way all visuals on a report page are interconnected.</span></span> <span data-ttu-id="e1ba7-149">Hvis du markerer et datapunkt i et af de visuelle elementer, bliver alle andre visuelle elementer på siden, der indeholder denne dataændring, baseret på det markerede.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-149">If you select a data point on one of the visuals, all the other visuals on the page that contain that data change, based on that selection.</span></span> <span data-ttu-id="e1ba7-150">Få mere at vide, og få vist et eksempel i [Hvordan visuelle elementer filtreres på tværs af hinanden i en Power BI-rapport](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span><span class="sxs-lookup"><span data-stu-id="e1ba7-150">Find out more and see an example in [How visuals cross-filter each other in a Power BI report](https://docs.microsoft.com/power-bi/consumer/end-user-interactions).</span></span>

## <a name="export-to-excel"></a><span data-ttu-id="e1ba7-151">Eksportér til Excel</span><span class="sxs-lookup"><span data-stu-id="e1ba7-151">Export to Excel</span></span>

<span data-ttu-id="e1ba7-152">Hvis du vil have vist rapportdata i Excel, kan du klikke på menuen Indstillinger (tre prikker) i et visuelt element og vælge **Eksporter underliggende data**.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-152">To view report data in Excel, you can click the options menu (three dots) on a visual and select **Export underlying data**.</span></span> <span data-ttu-id="e1ba7-153">Eksporterede data eksporteres som filtrerede i overensstemmelse med brugertilladelser i Attract.</span><span class="sxs-lookup"><span data-stu-id="e1ba7-153">Exported data will export as filtered, respecting user permissions in Attract.</span></span> <span data-ttu-id="e1ba7-154">Du kan finde flere oplysninger under [Eksportere data fra visualiseringer](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span><span class="sxs-lookup"><span data-stu-id="e1ba7-154">For more information, see [Export data from visualizations](https://docs.microsoft.com/power-bi/visuals/power-bi-visualization-export-data).</span></span>
