---
title: Formalisere forretningsprocesser
description: "Funktionen til forretningsprocesser giver dig mulighed for at oprette en skabelon til forretningsproces til processer, der skal fuldføres inden for organisationen."
author: ShielaSogge
manager: AnnBe
ms.date: 01/09/2018
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: PersonnelBusinessProcessGenericWorkspace, BusinessProcessGenericTemplateListpage, BusinessProcessGenericMyTemplates, BusinessProcessGroupAssignment
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Talent, Core
ms.custom: 7521
ms.assetid: 3b953d5f-6325-4c9e-8b9b-6ab0458a73f8
ms.search.region: Global
ms.author: ShielaS
ms.search.validFrom: 2018-01-09
ms.dyn365.ops.version: AX 7.1.0, Talent October 2017 update
ms.translationtype: HT
ms.sourcegitcommit: a8b5a5af5108744406a3d2fb84d7151baea2481b
ms.openlocfilehash: 1b50a97f5e2fc94255ff71702faf91ab36e68eb4
ms.contentlocale: da-dk
ms.lasthandoff: 04/13/2018

---
# <a name="formalize-business-processes"></a><span data-ttu-id="d4f7e-103">Formalisere forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="d4f7e-103">Formalize business processes</span></span>
<span data-ttu-id="d4f7e-104">Funktionen til forretningsprocesser giver dig mulighed for at oprette en skabelon til forretningsproces til processer, der skal fuldføres inden for organisationen.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-104">The Business process feature allows you to create a business process template for processes that need to be completed within your organization.</span></span> <span data-ttu-id="d4f7e-105">Dit firma udfører f.eks. en HR revision hvert år.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-105">For example, your company may complete an HR audit each year.</span></span> <span data-ttu-id="d4f7e-106">Der kan oprettes en skabelon til at spore alle de opgaver, som revisionen består af, for at sikre at alle opgaver er udført, hver gang processen er fuldført, og om nødvendigt for at sikre, at opgaver udføres i den rigtige rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-106">A template can be created to track all the tasks that the audit comprises to help ensure that all the tasks are done each time the process is completed, and if necessary, to help ensure that tasks are performed in the correct order.</span></span> <span data-ttu-id="d4f7e-107">Skabeloner kan bruges igen til gentagne processer eller kopieres for at blive brugt som udgangspunkt ved oprettelsen af nye.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-107">Templates can be re-used for recurring processes or copied to use as a starting point creating new ones.</span></span>

<span data-ttu-id="d4f7e-108">Når der oprettes en skabelon, kan en proces startes og spores i arbejdsområdet Forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-108">After a template is created, a process can be started and tracked in the Business process workspace.</span></span>  <span data-ttu-id="d4f7e-109">Når der startes en forretningsproces, tildeles der opgaver til de relevante personer opgaverne, og der angives en forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-109">When a business process is started, the tasks will be assigned to the appropriate people and will include a due date.</span></span> <span data-ttu-id="d4f7e-110">Vi dækker disse komponenter detaljeret nedenfor.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-110">We will cover these components in detail below.</span></span>

## <a name="business-process-template"></a><span data-ttu-id="d4f7e-111">Forretningsprocesskabelon</span><span class="sxs-lookup"><span data-stu-id="d4f7e-111">Business process template</span></span>
<span data-ttu-id="d4f7e-112">En forretningsprocesskabelon indeholder en gruppe opgaver, der udgør en forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-112">A Business process template lists a group of tasks that make up a business process.</span></span> <span data-ttu-id="d4f7e-113">Personalechefer og -assistenter kan som standard oprette forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-113">Human resource managers and assistants can create business processes by default.</span></span>  <span data-ttu-id="d4f7e-114">Dette kan dog ændres i sikkerhedskonfigurationen ved at redigere pligten Vedligehold generiske forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-114">However, this can be changed in the security configuration by editing the Maintain generic business processes duty.</span></span>

<span data-ttu-id="d4f7e-115">Der kan defineres en procesejer for hver proces.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-115">A Process owner can be defined for each process.</span></span> <span data-ttu-id="d4f7e-116">Procesejeren har overblik over alle opgaver for processen og kan tildele opgaver igen eller ændre forfaldsdatoer.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-116">The process owner will have visibility into all the tasks for the process, and can re-assign tasks or change due dates.</span></span>  <span data-ttu-id="d4f7e-117">Personaledirektøren kan f.eks. oprette en forretningsprocesskabelon for en gennemgang af frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-117">For example, the HR director could create a Business process template for a benefits review.</span></span>  <span data-ttu-id="d4f7e-118">Chef for kompensation og frynsegoder kan angives som ejeren af processen, så vedkommende kan få indsigt i de opgaver, der skal fuldføres som en del af gennemgangen.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-118">The Comp and benefits manager can be set as the Process owner, so that he or she can have insight into the tasks that need to be completed as part of the review.</span></span>  <span data-ttu-id="d4f7e-119">En procesejer kan ikke oprette eller slette aktive forretningsprocesser eller forretningsprocesskabeloner.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-119">A Process owner cannot create or delete active Business processes or Business process templates.</span></span>

## <a name="task"></a><span data-ttu-id="d4f7e-120">Opgave</span><span class="sxs-lookup"><span data-stu-id="d4f7e-120">Task</span></span>
<span data-ttu-id="d4f7e-121">En forretningsproces består ofte af flere opgaver.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-121">A business process often comprises multiple tasks.</span></span> <span data-ttu-id="d4f7e-122">Nogle opgaver kan udføres inden for Dynamics 365 for Talent, f.eks. gennemgang af interne kursustilbud.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-122">Some tasks can be completed within Dynamics 365 for Talent, such as reviewing internal course offerings.</span></span> <span data-ttu-id="d4f7e-123">I dette tilfælde vælges der et menupunkt i feltet Opgavelink.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-123">In this instance, a Menu item is selected in the Task link field.</span></span> <span data-ttu-id="d4f7e-124">Andre opgaver kan omfatte gennemgang eller udfyldelse af formularer på et websted.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-124">Other tasks might involve reviewing or completing forms on a web site.</span></span> <span data-ttu-id="d4f7e-125">Hvis du vælger URL-adresse i feltet Opgavelink kan webadressen angives.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-125">Selecting URL in the Task link field enables the web address to be entered.</span></span> <span data-ttu-id="d4f7e-126">Du kan angive URL-adresser for både eksterne og interne websteder i dette felt.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-126">You can enter URLs for both external and internal sites in this field.</span></span> <span data-ttu-id="d4f7e-127">Du kan også oprette opgaver for aktiviteter, der udføres manuelt, f.eks. gennemsyn af adgangen til alle strukturer.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-127">You can also create tasks for activities that you complete manually, such as reviewing the accessibility of all structures.</span></span> <span data-ttu-id="d4f7e-128">I dette tilfælde er en opgavekæde ikke påkrævet.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-128">In this instance a task link is not required.</span></span> <span data-ttu-id="d4f7e-129">Denne fleksibilitet gør det muligt at spore flere typer opgaver i en omfattende proces.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-129">This flexibility lets you track multiple kinds of tasks in a comprehensive process.</span></span>

<span data-ttu-id="d4f7e-130">Opgaver kan tildeles til en bestemt arbejder eller til en stilling.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-130">Tasks can be assigned to a specific worker or to a position.</span></span> <span data-ttu-id="d4f7e-131">For eksempel vil chefen for kompensation og frynsegoder altid være den person, der udfører en gennemgang af forsikringspræmier.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-131">For example, the Comp and benefits manager will always be the person that conducts a review of insurance premiums.</span></span>   <span data-ttu-id="d4f7e-132">Når du opretter denne opgave, skal du vælge Stilling som Tildelingstypen og derefter vælge chefen for kompensation og frynsegoder på listen Stilling.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-132">When creating this task, select Position for the Assignment type, and then select Comp and benefit manager from the Position list.</span></span> <span data-ttu-id="d4f7e-133">Når processen begynder, tildeles opgaven til den medarbejder, der har stillingen chef for kompensation og frynsegoder.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-133">When the process starts, the task will be assigned to the worker who is in the Comp and benefits manager position.</span></span> <span data-ttu-id="d4f7e-134">Du kan også tildele en opgave til en bestemt arbejder ved at vælge arbejderen i feltet Tildelingstype og derefter vælge den relevante person.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-134">You can also assign a task to a specific worker by selecting Worker in the Assignment type field, and then selecting the appropriate person.</span></span>

<span data-ttu-id="d4f7e-135">Forfaldsdatoer for opgaven er afhængig af den måldato, der er angivet i starten af processen.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-135">Task due dates depend on the Target date entered at the start of the process.</span></span> <span data-ttu-id="d4f7e-136">Nogle opgaver skal fuldføres før måldatoen, og nogle kan muligvis udføres efter måldatoen.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-136">Some tasks must be completed before the target date, and some might be completed after the target date.</span></span>  <span data-ttu-id="d4f7e-137">Når du definerer en opgave, angiver du en relativ forfaldsdato i forhold til måldatoen i feltet Forskydning af forfaldsdato fra måldato.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-137">When defining a task, you will enter a due date that is relative to the target date in the Due date offset from target date field.</span></span> <span data-ttu-id="d4f7e-138">Antag for eksempel, at chefen for kompensation og frynsegoder skal foretage en gennemgang af forsikringspræmier, 10 dage før HR-revisionen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-138">For example, assume that the Comp and benefits manager must perform a review of the insurance premiums 10 days before the HR audit is complete.</span></span> <span data-ttu-id="d4f7e-139">Den oprettede opgave har en forfaldsdato i forhold til måldatoen på -10.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-139">The task created will have a due date relative to target date of -10.</span></span> <span data-ttu-id="d4f7e-140">Hvis processen derfor er startet den 13. maj, er opgaven forfalden den 3. maj.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-140">Therefore, if the process is started on May 13th, the task will be due on May 3rd.</span></span> <span data-ttu-id="d4f7e-141">Bemærk: Forfaldsdatoer kan også justeres, når processen er startet.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-141">Note: Due dates can also be adjusted after the process is started.</span></span>

<span data-ttu-id="d4f7e-142">Komplekse opgaver kan kræve flere trin, eller der er behov for, at den person, der udfører opgaver, skal angive yderligere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-142">Complex tasks might require multiple steps, or need the individual performing the tasks to provide additional information.</span></span> <span data-ttu-id="d4f7e-143">Du kan føje instruktioner til opgaven og desuden foretage RTF-formatering af instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-143">You can add Instructions to the task, and include rich text formatting for the instructions, as well.</span></span> <span data-ttu-id="d4f7e-144">Instruktionerne kan give yderligere oplysninger om, hvordan opgaven skal fuldføres, til den person, der er tildelt til at gennemføre den.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-144">The instructions can provide additional information on how to complete the task to the person who is assigned to complete it.</span></span>

## <a name="starting-a-process"></a><span data-ttu-id="d4f7e-145">Starte en proces</span><span class="sxs-lookup"><span data-stu-id="d4f7e-145">Starting a process</span></span>
<span data-ttu-id="d4f7e-146">En proces kan startes fra en forretningsprocesskabelon ved at vælge Start proces.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-146">A process can be started within a Business process template by selecting Start process.</span></span>  <span data-ttu-id="d4f7e-147">Når en proces er startet, oprettes opgaver for de valgte arbejdere og/eller stillinger, der er defineret i de opgaver, der er inkluderet i forretningsprocesskabelonen.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-147">When a process is started, tasks will be created for the selected workers and/or positions defined in the tasks that are included in the Business process template.</span></span> <span data-ttu-id="d4f7e-148">En forfaldsdato tildeles også til hver opgave ved at tilføje eller fratrække forskydningsdagene fra måldatoen (se oplysningerne om forskydningsdage i afsnittet Opgave).</span><span class="sxs-lookup"><span data-stu-id="d4f7e-148">A due date will also be assigned to each task by adding or subtracting the offset days from the target date (see the information regarding offset days in the task section).</span></span> <span data-ttu-id="d4f7e-149">De aktive forretningsprocesser kan ses i arbejdsområdet Forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-149">The active Business processes can be viewed in the Business processes workspace.</span></span> 

## <a name="employee-self-service"></a><span data-ttu-id="d4f7e-150">Medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="d4f7e-150">Employee self-service</span></span>
<span data-ttu-id="d4f7e-151">Når en opgave er tildelt til en medarbejder, kan vedkommendes tildelte opgaver ses på siden Medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-151">When a task is assigned to an employee, their assigned tasks can be viewed on the Employee self service page.</span></span> <span data-ttu-id="d4f7e-152">Medarbejdere, der har en forretningsprocesopgave knyttet til sig, kan se opgaven, dens beskrivelse, instruktioner til at fuldførelse og navnet på en kontaktperson, og de kan åbne den tilknyttede Dynamics365-side eller -webside fra deres side Medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-152">Employees who have a business process task assigned to them can see the task, its description, instructions for completing it, and the name of a contact person, and they can open the associated Dynamics365 page or web page, from their Employee self-service page.</span></span> <span data-ttu-id="d4f7e-153">Opgaver kan markeres som igangværende, annullerede eller fuldførte.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-153">Tasks can be marked as in-progress, canceled or completed.</span></span>

## <a name="business-process-workspace"></a><span data-ttu-id="d4f7e-154">Arbejdsområdet Forretningsproces</span><span class="sxs-lookup"><span data-stu-id="d4f7e-154">Business Process Workspace</span></span>
<span data-ttu-id="d4f7e-155">Personalemedarbejdere kan se de aktive forretningsprocesser i arbejdsområdet Forretningsproces.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-155">HR professionals can view the active business processes from the Business process workspace.</span></span> <span data-ttu-id="d4f7e-156">Arbejdsområdet viser alle aktive processer og de opgaver, der er tilknyttet hver enkelt.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-156">The workspace lists all active processes and the tasks that are associated with each one.</span></span> <span data-ttu-id="d4f7e-157">Den omfattende opgaveliste kan filtreres efter forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-157">The comprehensive task list can be filtered by due date.</span></span> <span data-ttu-id="d4f7e-158">Siden viser også forfaldne opgaver og opgaver, der specifikt er tildelt til personalemedarbejderen.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-158">The page also lists overdue tasks, and tasks specifically assigned to the HR professional.</span></span> <span data-ttu-id="d4f7e-159">De kan også opdatere status for alle opgaver og kan om nødvendigt tildele opgaver til andre for at sørge for at den overordnede forretningsproces bevæger sig fremad.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-159">They can also update the status of all tasks and if necessary, reassign tasks to help keep the overall business process moving forward.</span></span>

## <a name="my-business-processes-workspace"></a><span data-ttu-id="d4f7e-160">Arbejdsområdet Mine forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="d4f7e-160">My Business Processes Workspace</span></span>
<span data-ttu-id="d4f7e-161">Procesejere kan få vist de aktive forretningsprocesser, der er tildelt dem, fra arbejdsområdet Mine forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-161">Process owners can view the active business processes that are assigned to them from the My Business Process workspace.</span></span> <span data-ttu-id="d4f7e-162">Arbejdsområdet viser alle aktive processer og de tilknyttede opgaver, som den pågældende bruger ejer.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-162">The workspace lists all active processes and associated tasks that that user owns.</span></span>  <span data-ttu-id="d4f7e-163">Den omfattende opgaveliste kan filtreres efter forfaldsdato.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-163">The comprehensive task list can be filtered by due date.</span></span> <span data-ttu-id="d4f7e-164">Siden viser også de opgaver, der specifikt er tildelt procesejer.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-164">The page also lists tasks specifically assigned to process owner.</span></span> <span data-ttu-id="d4f7e-165">Procesejeren kan også opdatere status for alle opgaver, samt omfordele alle opgaver.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-165">The process owner can also update the status of all tasks, as well as reassign any tasks.</span></span>

## <a name="navigating-business-processes"></a><span data-ttu-id="d4f7e-166">Navigere i forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="d4f7e-166">Navigating Business Processes</span></span>
1. <span data-ttu-id="d4f7e-167">Hvis du vil tilføje en forretningsprocesskabelon, skal du gå til Forretningsprocesser – Links – Administration af forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-167">To add a Business process template, navigate to Business processes- links – Business processes administration.</span></span>
   - <span data-ttu-id="d4f7e-168">a.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-168">a.</span></span>   <span data-ttu-id="d4f7e-169">Ny opretter en ny skabelon.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-169">New will create a new template.</span></span>
   - <span data-ttu-id="d4f7e-170">b.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-170">b.</span></span>   <span data-ttu-id="d4f7e-171">Kopier fra skabelon kopierer den valgte skabelon til en ny.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-171">Copy from template will copy the selected template to a new one.</span></span>
   - <span data-ttu-id="d4f7e-172">c.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-172">c.</span></span>   <span data-ttu-id="d4f7e-173">Start proces starter den valgte forretningsproces, tildelet opgaver og beregner forfaldsdatoer.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-173">Start process will start the selected business process, assign tasks, and calculate due dates.</span></span>  
2. <span data-ttu-id="d4f7e-174">For at få vist aktive processer og tilknyttede opgaver skal du gå til arbejdsområdet Forretningsprocesser.</span><span class="sxs-lookup"><span data-stu-id="d4f7e-174">To view active processes and associated tasks navigate to the Business processes workspace.</span></span>
