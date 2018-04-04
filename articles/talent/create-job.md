---
title: Konfiguration af dele af et job
description: "I dette emne beskrives de grundlæggende elementer, som en sag kan indeholde, og der gives eksempler på, hvordan du kan bruge disse elementer i din organisation."
author: rschloma
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmJob, HcmJobFunction, HcmJobTask, HcmTitle
audience: Application User
ms.author: rschloma
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent, Retail
ms.custom: 269054
ms.assetid: 889a8fab-0eef-45c2-91fc-ff2f4d44d54f
ms.search.region: Global
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.translationtype: HT
ms.sourcegitcommit: 812db9f1d319e4d16f83700a7153a0a3b318963e
ms.openlocfilehash: aaa8bdedc31ee03e96a0f7a5e78f25f888913e71
ms.contentlocale: da-dk
ms.lasthandoff: 03/23/2018

---

# <a name="setting-up-the-components-of-a-job"></a><span data-ttu-id="ed09e-103">Konfiguration af dele af et job</span><span class="sxs-lookup"><span data-stu-id="ed09e-103">Setting up the components of a job</span></span>

[!include[banner](includes/banner.md)]

[!include[retail name](includes/retail-name.md)]


<span data-ttu-id="ed09e-104">I dette emne beskrives de grundlæggende elementer, som en sag kan indeholde, og der gives eksempler på, hvordan du kan bruge disse elementer i din organisation.</span><span class="sxs-lookup"><span data-stu-id="ed09e-104">This topic describes the conceptual elements that a job can include and provides examples of how you can use those elements in your organization.</span></span> 

<span data-ttu-id="ed09e-105">Når du vil oprette job, skal du først konfigurere visse referenceoplysninger.</span><span class="sxs-lookup"><span data-stu-id="ed09e-105">Before you can create jobs, you must set up some reference information.</span></span> <span data-ttu-id="ed09e-106">Du kan oprette et job, der kun har et navn.</span><span class="sxs-lookup"><span data-stu-id="ed09e-106">You can create a job that has only a name.</span></span> <span data-ttu-id="ed09e-107">Du kan dog også medtage yderligere oplysninger, som f.eks. en stillingsbetegnelse, og derved angive standardværdier for de stillinger, der er tilknyttet jobbet.</span><span class="sxs-lookup"><span data-stu-id="ed09e-107">However, by including additional information, such as a job title, you provide default values for the positions that are assigned to the job.</span></span> <span data-ttu-id="ed09e-108">Desuden kan nogle af de oplysninger, du angiver, bruges til at filtrere kompensationsstrukturer til specifikke job.</span><span class="sxs-lookup"><span data-stu-id="ed09e-108">Additionally, some of the information that you enter can be used to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="ed09e-109">Hvis du vil oprette berettigelse, som du kan bruge til at filtrere lønstrukturer til et bestemt job, skal du konfigurere jobfunktioner og jobtyper, før du konfigurerer job.</span><span class="sxs-lookup"><span data-stu-id="ed09e-109">If you want to set up eligibility that you can use to filter compensation plans to a specific job, you should set up job functions and job types before you set up jobs.</span></span> <span data-ttu-id="ed09e-110">Når disse standardværdier er tilgængelige, sparer du tid, når du tilføjer stillinger til jobbet.</span><span class="sxs-lookup"><span data-stu-id="ed09e-110">By having these default values available, you will save time when you add positions to the job.</span></span> 

<span data-ttu-id="ed09e-111">Nogle jobdetaljer som f.eks. stillingsbetegnelse, type og funktion er datorelaterede.</span><span class="sxs-lookup"><span data-stu-id="ed09e-111">Some job details, such as the job title, type, and function, are date-effective.</span></span> <span data-ttu-id="ed09e-112">Hvis du opretter et job i dag, men først tilføjer disse detaljer senere, og derefter ser på jobbet pr. oprettelsesdatoen, vises disse detaljer ikke.</span><span class="sxs-lookup"><span data-stu-id="ed09e-112">If you create a job today but don't add these details until later, and you then look at the job as of the creation date, these details won't appear.</span></span> <span data-ttu-id="ed09e-113">Derfor skal du oprette nogle af disse referenceoplysninger, før du får brug for dem.</span><span class="sxs-lookup"><span data-stu-id="ed09e-113">Therefore, you should create some of this reference information before you require it.</span></span> <span data-ttu-id="ed09e-114">På den måde kan du føje oplysningerne til nye job, når du opretter dem.</span><span class="sxs-lookup"><span data-stu-id="ed09e-114">That way, you can add the information to new jobs when you create them.</span></span>

## <a name="job-titles"></a><span data-ttu-id="ed09e-115">Stillingsbetegnelser</span><span class="sxs-lookup"><span data-stu-id="ed09e-115">Job titles</span></span>
<span data-ttu-id="ed09e-116">Før du opretter job, skal du konfigurere stillingsbetegnelser for jobbene.</span><span class="sxs-lookup"><span data-stu-id="ed09e-116">Before you create jobs, you must set up titles for those jobs.</span></span> <span data-ttu-id="ed09e-117">Stillinger arver stillingsbetegnelser fra de job, som stillingerne er tilknyttet.</span><span class="sxs-lookup"><span data-stu-id="ed09e-117">Positions inherit job titles from the jobs that the positions are associated with.</span></span> 

<span data-ttu-id="ed09e-118">Vedligehold stillingsbetegnelser ved hjælp af siden **Titler**, som du kan åbne ved hjælp af søgefunktionen.</span><span class="sxs-lookup"><span data-stu-id="ed09e-118">Maintain job titles using the **Titles** page, which you can open by using the Search function.</span></span> <span data-ttu-id="ed09e-119">På siden **Titler** skal du angive de stillingsbetegnelser, som du vil bruge til dine job.</span><span class="sxs-lookup"><span data-stu-id="ed09e-119">On the **Titles **page, enter the titles that you plan to use for your jobs.</span></span>

## <a name="job-types"></a><span data-ttu-id="ed09e-120">Jobtyper</span><span class="sxs-lookup"><span data-stu-id="ed09e-120">Job types</span></span>
<span data-ttu-id="ed09e-121">Du kan bruge jobtyper til at gruppere lignende job i kategorier.</span><span class="sxs-lookup"><span data-stu-id="ed09e-121">You use job types to group similar jobs into categories.</span></span> <span data-ttu-id="ed09e-122">Jobtyper er ikke nødvendige.</span><span class="sxs-lookup"><span data-stu-id="ed09e-122">Job types aren't required.</span></span> <span data-ttu-id="ed09e-123">Hvis du planlægger at bruge jobtyper, når du konfigurerer berettigelsesregler for kompensationsstyring, skal du dog konfigurere jobtyper, før du konfigurerer job.</span><span class="sxs-lookup"><span data-stu-id="ed09e-123">However, if you plan to use job types when you set up eligibility rules for compensation management, you should set up job types before you set up jobs.</span></span> <span data-ttu-id="ed09e-124">Nogle eksempler på jobtyper er fuldtids og deltids eller fastlønnede og timelønnede.</span><span class="sxs-lookup"><span data-stu-id="ed09e-124">Some examples of job types are full-time and part-time, or salary and hourly pay.</span></span> <span data-ttu-id="ed09e-125">Du kan vedligeholde jobtyper fra siden **Jobtyper**.</span><span class="sxs-lookup"><span data-stu-id="ed09e-125">You maintain job types by using the **Job types** page.</span></span> <span data-ttu-id="ed09e-126">Angiv et navn og en kort beskrivelse af stillingstypen på siden **Jobtyper**.</span><span class="sxs-lookup"><span data-stu-id="ed09e-126">On the **Job types** page, enter a name and a brief description for the job type.</span></span> <span data-ttu-id="ed09e-127">I feltet **Momsfri status** skal du vælge en af følgende indstillinger for at angive Fair Labor Standards Act (FLSA) fritagelsesstatus for job med denne jobtype:</span><span class="sxs-lookup"><span data-stu-id="ed09e-127">In the **Exempt status** field, select one of the following options to indicate the Fair Labor Standards Act (FLSA) exempt status of jobs that have this job type:</span></span>

-   <span data-ttu-id="ed09e-128">**Frit** – Job er fritaget for overtid i henhold til FLSA.</span><span class="sxs-lookup"><span data-stu-id="ed09e-128">**Exempt** – Jobs are exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="ed09e-129">**Ikke-momsfri** – Job er ikke fritaget for overtid i henhold til FLSA.</span><span class="sxs-lookup"><span data-stu-id="ed09e-129">**Non-exempt** – Jobs aren't exempt from overtime under the FLSA.</span></span>
-   <span data-ttu-id="ed09e-130">**Gælder ikke** – FLSA-dækning er ikke relevant.</span><span class="sxs-lookup"><span data-stu-id="ed09e-130">**Does not apply** – FLSA coverage isn't applicable.</span></span>

## <a name="job-functions"></a><span data-ttu-id="ed09e-131">Jobfunktioner</span><span class="sxs-lookup"><span data-stu-id="ed09e-131">Job functions</span></span>
<span data-ttu-id="ed09e-132">Jobfunktioner beskriver overordnede funktionelle kategorier og relaterede overordnede opgaver.</span><span class="sxs-lookup"><span data-stu-id="ed09e-132">Job junctions describe high-level functional categories and relate high-level duties.</span></span> <span data-ttu-id="ed09e-133">Jobfunktioner er ikke nødvendige.</span><span class="sxs-lookup"><span data-stu-id="ed09e-133">Job functions aren't required.</span></span> <span data-ttu-id="ed09e-134">Du kan bruge jobfunktioner sammen med jobtyper til at filtrere kompensationsstrukturer til specifikke job.</span><span class="sxs-lookup"><span data-stu-id="ed09e-134">You can use job functions, together with job types, to filter compensation plans to specific jobs.</span></span> <span data-ttu-id="ed09e-135">Du kan knytte jobfunktioner og jobtyper til kompensationsplaner ved at oprette berettigelsesregler på siden **Berettigelsesregler**.</span><span class="sxs-lookup"><span data-stu-id="ed09e-135">You associate job functions and job types with compensation plans by setting up eligibility rules on the **Eligibility rules** page.</span></span> <span data-ttu-id="ed09e-136">Du kan derefter knytte et sæt niveauer til en kompensationsplan, der gælder for den specifikke jobtype/jobfunktionskombination, som du har defineret ved hjælp af en berettigelsesregel.</span><span class="sxs-lookup"><span data-stu-id="ed09e-136">You can then attach a set of levels to a compensation plan that apply to the specific combination of a job type and job function that you've defined through an eligibility rule.</span></span> <span data-ttu-id="ed09e-137">(Disse funktioner gælder både for faste og variable kompensationsplaner). Men hvis du planlægger at bruge jobfunktioner, når du konfigurerer berettigelsesregler for kompensationsstyring, skal du dog konfigurere jobfunktioner, før du konfigurerer job.</span><span class="sxs-lookup"><span data-stu-id="ed09e-137">(These features apply to both fixed compensation plans and variable compensation plans.) However, if you plan to use job functions when you set up eligibility rules for compensation management, you should set up job functions before you set up jobs.</span></span> <span data-ttu-id="ed09e-138">Følgende tabel indeholder nogle eksempler på jobfunktioner.</span><span class="sxs-lookup"><span data-stu-id="ed09e-138">The following table shows some examples of job functions.</span></span>

| <span data-ttu-id="ed09e-139">Stilling</span><span class="sxs-lookup"><span data-stu-id="ed09e-139">Job</span></span>           | <span data-ttu-id="ed09e-140">Jobfunktion</span><span class="sxs-lookup"><span data-stu-id="ed09e-140">Job function</span></span>         |
|---------------|----------------------|
| <span data-ttu-id="ed09e-141">Salgsdirektør</span><span class="sxs-lookup"><span data-stu-id="ed09e-141">Sales manager</span></span> | <span data-ttu-id="ed09e-142">Chef på mellemlederniveau</span><span class="sxs-lookup"><span data-stu-id="ed09e-142">Mid-level Manager</span></span>    |
| <span data-ttu-id="ed09e-143">Bogholder</span><span class="sxs-lookup"><span data-stu-id="ed09e-143">Accountant</span></span>    | <span data-ttu-id="ed09e-144">Professionelle</span><span class="sxs-lookup"><span data-stu-id="ed09e-144">Professionals</span></span>        |

<span data-ttu-id="ed09e-145">Du kan vedligeholde jobfunktioner på siden **Jobfunktioner**.</span><span class="sxs-lookup"><span data-stu-id="ed09e-145">You maintain job functions by using the **Job functions** page.</span></span> <span data-ttu-id="ed09e-146">Angiv en identifikationskode og en kort beskrivelse af jobfunktionen på siden **Jobfunktioner**.</span><span class="sxs-lookup"><span data-stu-id="ed09e-146">On the **Job functions** page, enter an identification code and a brief description for the job function.</span></span>

## <a name="job-tasks"></a><span data-ttu-id="ed09e-147">Arbejdsopgaver</span><span class="sxs-lookup"><span data-stu-id="ed09e-147">Job tasks</span></span>
<span data-ttu-id="ed09e-148">Arbejdsopgaver beskriver de grundlæggende opgaver, der skal udføres af en arbejder, der er i position for et job.</span><span class="sxs-lookup"><span data-stu-id="ed09e-148">Job tasks describe the basic tasks that a worker who is in a position for a job must complete.</span></span> <span data-ttu-id="ed09e-149">Samme arbejdsopgave kan føjes til flere job og til stillinger for de job, der bruger disse arbejdsopgaver.</span><span class="sxs-lookup"><span data-stu-id="ed09e-149">The same job task can be added to multiple jobs, and to positions for the jobs that use those job tasks.</span></span> <span data-ttu-id="ed09e-150">Følgende tabel indeholder nogle eksempler på arbejdsopgaver.</span><span class="sxs-lookup"><span data-stu-id="ed09e-150">The following table shows some examples of job tasks.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="ed09e-151">Stilling</span><span class="sxs-lookup"><span data-stu-id="ed09e-151">Job</span></span></th>
<th><span data-ttu-id="ed09e-152">Arbejdsopgave</span><span class="sxs-lookup"><span data-stu-id="ed09e-152">Job task</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="ed09e-153">Salgsdirektør</span><span class="sxs-lookup"><span data-stu-id="ed09e-153">Sales manager</span></span></td>
<td><ul>
<li><span data-ttu-id="ed09e-154"><strong>Performance-gennemgang</strong> – Gennemgang af en sælgers jobperformance.</span><span class="sxs-lookup"><span data-stu-id="ed09e-154"><strong>Perf-review</strong> – Review each salesperson's job performance.</span></span></li>
<li><span data-ttu-id="ed09e-155"><strong>Fraværsgennemgang</strong> – Godkend eller afvis en sælgers fraværsanmodninger eller registreringer.</span><span class="sxs-lookup"><span data-stu-id="ed09e-155"><strong>Abs-review</strong> – Approve or reject each salesperson's absence requests or registrations.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="ed09e-156">Bogholder</span><span class="sxs-lookup"><span data-stu-id="ed09e-156">Accountant</span></span></td>
<td><span data-ttu-id="ed09e-157"><strong>Regnskabsrapport</strong> – Forelæg ugentlige regnskaber til regnskabsdirektøren.</span><span class="sxs-lookup"><span data-stu-id="ed09e-157"><strong>FIN-Report</strong> – Present weekly financial reports to the chief financial officer.</span></span></td>
</tr>
</tbody>
</table>

<span data-ttu-id="ed09e-158">Du kan vedligeholde arbejdsopgaver fra siden **Arbejdsopgaver**.</span><span class="sxs-lookup"><span data-stu-id="ed09e-158">You maintain job tasks by using the **Job tasks** page.</span></span> <span data-ttu-id="ed09e-159">Angiv et navn til og en beskrivelse af arbejdsopgaven på siden **Arbejdsopgaver**.</span><span class="sxs-lookup"><span data-stu-id="ed09e-159">On the **Job tasks** page, enter a name and description for the job task.</span></span> <span data-ttu-id="ed09e-160">I feltet **Notat** kan du også yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="ed09e-160">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="ed09e-161">Noterne kan blive opdateret for et bestemt job, uden at det ændrer de noter, du har angivet her.</span><span class="sxs-lookup"><span data-stu-id="ed09e-161">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="areas-of-responsibility"></a><span data-ttu-id="ed09e-162">Ansvarsområder</span><span class="sxs-lookup"><span data-stu-id="ed09e-162">Areas of responsibility</span></span>
<span data-ttu-id="ed09e-163">Du kan bruge ansvarsområder til at angive arbejdsroller, processer og produkter, som en arbejder, der er i stilling til et job, er ansvarlig for.</span><span class="sxs-lookup"><span data-stu-id="ed09e-163">You use areas of responsibility to indicate the work roles, processes, and products that a worker who is in a position for a job is responsible for.</span></span> <span data-ttu-id="ed09e-164">Et eksempel for et job med titlen "Bogholder" kunne et ansvarsområde være "Økonomirapportering for produkt A".</span><span class="sxs-lookup"><span data-stu-id="ed09e-164">For example, for a job that is named "Accountant," one area of responsibility might be "Financial reporting for product A."</span></span> <span data-ttu-id="ed09e-165">Du kan vedligeholde ansvarsområder ved hjælp af siden **Ansvarsområder**, som du kan finde ved hjælp af søgefunktionen.</span><span class="sxs-lookup"><span data-stu-id="ed09e-165">You maintain areas of responsibility by using the **Areas of responsibility** page, which you can find by using the Search function.</span></span> <span data-ttu-id="ed09e-166">Angiv et navn til og en beskrivelse af ansvarsområdet på siden **Ansvarsområder**.</span><span class="sxs-lookup"><span data-stu-id="ed09e-166">On the **Areas of responsibility** page, enter a name and description for the responsibility.</span></span> <span data-ttu-id="ed09e-167">I feltet **Notat** kan du også yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="ed09e-167">In the **Note** field, you can optionally enter additional information.</span></span> <span data-ttu-id="ed09e-168">Noterne kan blive opdateret for et bestemt job, uden at det ændrer de noter, du har angivet her.</span><span class="sxs-lookup"><span data-stu-id="ed09e-168">The notes can be updated for a specific job without changing the notes that you entered here.</span></span>

## <a name="steps-for-creating-a-job"></a><span data-ttu-id="ed09e-169">Trin til oprettelse af et job</span><span class="sxs-lookup"><span data-stu-id="ed09e-169">Steps for creating a job</span></span>
<span data-ttu-id="ed09e-170">Referer til emnet [Definere nye job](../fin-and-ops/hr/tasks/define-new-jobs.md) for den trinvise procedure til at oprette et nyt job.</span><span class="sxs-lookup"><span data-stu-id="ed09e-170">Refer to the [Define new jobs](../fin-and-ops/hr/tasks/define-new-jobs.md) topic for the step-by-step procedure for creating a new job.</span></span> 

