---
title: Udsende og planlægge spørgeskemaer.
description: I dette emne beskrives, hvordan du distribuerer de spørgeskemaer, som du har designet, så de er tilgængelige for den person eller gruppe af personer, der skal udfylde dem.
author: kherr75
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: KMConnectionType, KMKnowledgeCollectorPlanningTabel, SysEmailParameters
audience: Application User
ms.reviewer: rschloma
ms.search.scope: Core, Operations, Talent
ms.custom: 17424
ms.assetid: fd8d867a-2446-400a-b91f-ad4085427470
ms.search.region: Global
ms.author: kherr
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: eafcb047117eab73fddbd93c4c1d0aafb0023ebd
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/29/2019
ms.locfileid: "303695"
---
# <a name="distribute-and-schedule-questionnaires"></a><span data-ttu-id="e25ab-103">Udsende og planlægge spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="e25ab-103">Distribute and schedule questionnaires</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e25ab-104">I dette emne beskrives, hvordan du distribuerer de spørgeskemaer, som du har designet, så de er tilgængelige for den person eller gruppe af personer, der skal udfylde dem.</span><span class="sxs-lookup"><span data-stu-id="e25ab-104">This topic explains how distribute the questionnaires that you design, so that they are available to the person or group of people who will complete them.</span></span> 

<span data-ttu-id="e25ab-105">Der er flere måder at distribuere et spørgeskema på:</span><span class="sxs-lookup"><span data-stu-id="e25ab-105">There are multiple ways to distribute a questionnaire:</span></span>

-   <span data-ttu-id="e25ab-106">Markér spørgeskemaet som aktivt.</span><span class="sxs-lookup"><span data-stu-id="e25ab-106">Mark the questionnaire as active.</span></span> <span data-ttu-id="e25ab-107">Spørgeskemaet er derefter tilgængeligt for alle medarbejdere, medmindre der er oprettet en spørgeskemagruppe for at begrænse adgangen til det.</span><span class="sxs-lookup"><span data-stu-id="e25ab-107">The questionnaire is then available to all employees, unless a questionnaire group is set up to restrict access to it.</span></span>
-   <span data-ttu-id="e25ab-108">Tildel rettigheder til en spørgeskemagruppe.</span><span class="sxs-lookup"><span data-stu-id="e25ab-108">Assign rights to a questionnaire group.</span></span> <span data-ttu-id="e25ab-109">Spørgeskemaet er derefter tilgængeligt for alle medlemmer af den valgte gruppe.</span><span class="sxs-lookup"><span data-stu-id="e25ab-109">The questionnaire is then available to all members of the selected group.</span></span>
-   <span data-ttu-id="e25ab-110">Opret planlagte besvarelser.</span><span class="sxs-lookup"><span data-stu-id="e25ab-110">Create planned answer sessions.</span></span> <span data-ttu-id="e25ab-111">Spørgeskemaet er derefter kun tilgængeligt for én bestemt person.</span><span class="sxs-lookup"><span data-stu-id="e25ab-111">The questionnaire is then available only to a particular person.</span></span>
-   <span data-ttu-id="e25ab-112">Opret tidsplan.</span><span class="sxs-lookup"><span data-stu-id="e25ab-112">Create a schedule.</span></span> <span data-ttu-id="e25ab-113">Spørgeskemaet kan derefter være tilgængeligt for flere personer.</span><span class="sxs-lookup"><span data-stu-id="e25ab-113">The questionnaire can then be available to multiple people.</span></span>

## <a name="marking-a-questionnaire-as-active"></a><span data-ttu-id="e25ab-114">Markering af et spørgeskema som aktivt</span><span class="sxs-lookup"><span data-stu-id="e25ab-114">Marking a questionnaire as active</span></span>
<span data-ttu-id="e25ab-115">Ved at indstille feltet **Aktiv** til **Ja** på siden **Spørgeskemaer** kan du gøre spørgeskemaet tilgængeligt, så alle medarbejdere kan udfylde det.</span><span class="sxs-lookup"><span data-stu-id="e25ab-115">By setting the **Active** field to **Yes** on the **Questionnaires** page, you make the questionnaire available for all employees to complete.</span></span> <span data-ttu-id="e25ab-116">Svarpersoner kan udfylde spørgeskemaet flere gange.</span><span class="sxs-lookup"><span data-stu-id="e25ab-116">Respondents can complete the questionnaire multiple times.</span></span> <span data-ttu-id="e25ab-117">Denne funktion er nyttig, hvis du vil indsamle løbende feedback hele året.</span><span class="sxs-lookup"><span data-stu-id="e25ab-117">This functionality is useful if you want to gather continual feedback throughout the year.</span></span> <span data-ttu-id="e25ab-118">Du kan for eksempel oprette et spørgeskema, som medarbejdere bruger til at give feedback om tjenesten frokost i cafeteriaet.</span><span class="sxs-lookup"><span data-stu-id="e25ab-118">For example, you can make a questionnaire that employees use to give feedback about the lunch service in the cafeteria.</span></span>

## <a name="questionnaire-groups"></a><span data-ttu-id="e25ab-119">Spørgeskemagrupper</span><span class="sxs-lookup"><span data-stu-id="e25ab-119">Questionnaire groups</span></span>
<span data-ttu-id="e25ab-120">Du kan oprette spørgeskemagrupper og derefter medtage de svarpersoner, som et spørgeskema skal distribueres til.</span><span class="sxs-lookup"><span data-stu-id="e25ab-120">You can set up questionnaire groups and then include the respondents that a questionnaire should be distributed to.</span></span> 

<span data-ttu-id="e25ab-121">Du kan oprette spørgeskemagrupper fra følgende sider:</span><span class="sxs-lookup"><span data-stu-id="e25ab-121">You can create questionnaire groups from the following pages:</span></span>

-   <span data-ttu-id="e25ab-122">**Spørgeskemagrupper**– Kun personer i en spørgeskemagruppe kan udfylde et valgt spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e25ab-122">**Questionnaire groups** – Only individuals in a questionnaire group can complete a selected questionnaire.</span></span> <span data-ttu-id="e25ab-123">Hvis din målgruppe f.eks. er underleverandører, kan du oprette en spørgeskemagruppe, der er specifik for disse svarpersoner.</span><span class="sxs-lookup"><span data-stu-id="e25ab-123">For example, your intended audience is contractors, so you create a questionnaire group that is specific to those respondents.</span></span>
-   <span data-ttu-id="e25ab-124">**Medlemmer af spørgeskemagruppe** – Du kan føje personer til spørgeskemagruppen.</span><span class="sxs-lookup"><span data-stu-id="e25ab-124">**Questionnaire group members** – You can add people to the questionnaire groups.</span></span>

<span data-ttu-id="e25ab-125">Hvis du vil tildele en spørgeskemagruppe til et spørgeskema skal du klikke på **Brugerrettigheder** på siden **Spørgeskemaer**.</span><span class="sxs-lookup"><span data-stu-id="e25ab-125">To assign a questionnaire group to a questionnaire, on the **Questionnaires** page, click **User rights**.</span></span> <span data-ttu-id="e25ab-126">Når spørgeskemaet er gemt som aktivt, kan medlemmerne af spørgeskemagruppen udfylde spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="e25ab-126">After the questionnaire is saved as active, the members of the questionnaire group can complete the questionnaire.</span></span> <span data-ttu-id="e25ab-127">Denne funktion er nyttig, hvis du vil teste et spørgeskema på en udvalgt gruppe personer, før du ruller det ud til en større gruppe, eller hvis du vil målrette et spørgeskema mod en meget specifik målgruppe.</span><span class="sxs-lookup"><span data-stu-id="e25ab-127">This functionality is helpful if you want to test a questionnaire on a select group of people before you roll it out to a larger group, or if you want to target a questionnaire to a very specific audience.</span></span>

## <a name="planned-answer-sessions-in-a-questionnaire"></a><span data-ttu-id="e25ab-128">Planlagte besvarelser i et spørgeskema</span><span class="sxs-lookup"><span data-stu-id="e25ab-128">Planned answer sessions in a questionnaire</span></span>
<span data-ttu-id="e25ab-129">Planlagte besvarelser er spørgeskemaer, som du har designet og valgt svarpersoner for.</span><span class="sxs-lookup"><span data-stu-id="e25ab-129">Planned answer sessions are questionnaires that you've designed and selected the respondents for.</span></span> 

> <span data-ttu-id="e25ab-130">**Bemærk!** Før du kan oprette planlagte besvarelser, skal du designe et spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e25ab-130">**Note** Before you can set up planned answer sessions, you must design a questionnaire.</span></span> 

<span data-ttu-id="e25ab-131">På siden **Planlagte besvarelser** kan du oprette en planlagt besvarelse for en bestemt medarbejder.</span><span class="sxs-lookup"><span data-stu-id="e25ab-131">On the **Planned answer session** page, you can create a planned answer session for an individual employee.</span></span> <span data-ttu-id="e25ab-132">Listen på siden viser alle planlagte spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="e25ab-132">The list on the page displays all planned questionnaires.</span></span> 

<span data-ttu-id="e25ab-133">Planlagte besvarelser bruges også i formen **Spørgeskemaplaner**, hvor du kan planlægge spørgeskemaer for flere personer:</span><span class="sxs-lookup"><span data-stu-id="e25ab-133">Planned answer sessions are also used on the **Questionnaire schedules** page, where you can plan questionnaires for multiple people:</span></span>

-   <span data-ttu-id="e25ab-134">Medarbejdere</span><span class="sxs-lookup"><span data-stu-id="e25ab-134">Employees</span></span>
-   <span data-ttu-id="e25ab-135">Kursusdeltagere</span><span class="sxs-lookup"><span data-stu-id="e25ab-135">Course participants</span></span>
-   <span data-ttu-id="e25ab-136">Organisationsenheder</span><span class="sxs-lookup"><span data-stu-id="e25ab-136">Organizational units</span></span>

<span data-ttu-id="e25ab-137">Hver person kan kun besvare spørgeskemaet én gang.</span><span class="sxs-lookup"><span data-stu-id="e25ab-137">Each person can answer the questionnaire only one time.</span></span>

## <a name="scheduling-a-questionnaire"></a><span data-ttu-id="e25ab-138">Planlægning af et spørgeskema</span><span class="sxs-lookup"><span data-stu-id="e25ab-138">Scheduling a questionnaire</span></span>
<span data-ttu-id="e25ab-139">Du kan vælge, om du vil planlægge et spørgeskema til flere svarpersoner.</span><span class="sxs-lookup"><span data-stu-id="e25ab-139">You can optionally schedule a questionnaire for multiple respondents.</span></span>

### <a name="planning-types"></a><span data-ttu-id="e25ab-140">Planlægningstyper</span><span class="sxs-lookup"><span data-stu-id="e25ab-140">Planning types</span></span>

<span data-ttu-id="e25ab-141">Planlægningstyper er nødvendige, hvis du vil arrangere planlagte besvarelser for flere svarpersoner.</span><span class="sxs-lookup"><span data-stu-id="e25ab-141">Planning types are required if you want to schedule planned answer sessions for multiple respondents.</span></span> <span data-ttu-id="e25ab-142">Planlægningstyper bruges klassificering af tidsplaner for spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="e25ab-142">Planning types are used to classify questionnaire schedules.</span></span> <span data-ttu-id="e25ab-143">Du kan f.eks. planlægge spørgeskemaer til følgende formål:</span><span class="sxs-lookup"><span data-stu-id="e25ab-143">For example, you can schedule questionnaires for the following purposes:</span></span>

-   <span data-ttu-id="e25ab-144">Evaluering</span><span class="sxs-lookup"><span data-stu-id="e25ab-144">Evaluation</span></span>
-   <span data-ttu-id="e25ab-145">Undersøgelse</span><span class="sxs-lookup"><span data-stu-id="e25ab-145">Survey</span></span>
-   <span data-ttu-id="e25ab-146">Test</span><span class="sxs-lookup"><span data-stu-id="e25ab-146">Testing</span></span>

<span data-ttu-id="e25ab-147">Du kan angive planlægningstyper for en spørgeskemaplan på siden **Spørgeskemaplaner**.</span><span class="sxs-lookup"><span data-stu-id="e25ab-147">You can specify planning types for a questionnaire schedule on the **Questionnaire schedules** page.</span></span>

### <a name="reference-types-for-questionnaire"></a><span data-ttu-id="e25ab-148">Referencetyper for spørgeskema</span><span class="sxs-lookup"><span data-stu-id="e25ab-148">Reference types for questionnaire</span></span>

<span data-ttu-id="e25ab-149">Du kan bruge referencetyper til at angive kriterier de svarpersoner, du eventuelt vælger, når du planlægger et spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e25ab-149">You can use reference types to enter criteria for the respondents that you might select when you schedule a questionnaire.</span></span> 

<span data-ttu-id="e25ab-150">Brug siden **Referencetyper** til at angive referencetyper for et spørgeskema.</span><span class="sxs-lookup"><span data-stu-id="e25ab-150">Use the **Reference types** page to set up reference types for a questionnaire.</span></span> <span data-ttu-id="e25ab-151">Hver referencetype svarer til en tabel i Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e25ab-151">Each reference type corresponds to a table in Microsoft Dynamics 365 for Finance and Operations.</span></span> <span data-ttu-id="e25ab-152">Når du opretter spørgeskemaplaner, kan du angive individuelle poster i tabellen eller et interval af poster, der skal være tilknyttet spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="e25ab-152">When you create questionnaire schedules, you can specify individual records in the table or a range of records that the questionnaire will be associated with.</span></span> 

<span data-ttu-id="e25ab-153">Hvis du f.eks. vælger tabellen Kurser, kan du bestemme, hvilket kursus spørgeskemaet er beregnet til.</span><span class="sxs-lookup"><span data-stu-id="e25ab-153">For example, if you select the Courses table, you can decide which specific course the questionnaire will be for.</span></span> <span data-ttu-id="e25ab-154">Når du opretter en referencetype til tabellen Kurser, bliver nogle felter og knapper på siden **Kurser** tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="e25ab-154">When you set up a reference for the Courses table, some fields and buttons on the **Courses** page become available.</span></span>

### <a name="questionnaire-schedules"></a><span data-ttu-id="e25ab-155">Spørgeskemaplaner</span><span class="sxs-lookup"><span data-stu-id="e25ab-155">Questionnaire schedules</span></span>

<span data-ttu-id="e25ab-156">Du kan bruge spørgeskemaplaner til at generere flere planlagte besvarelsessessioner for en gruppe af brugere, på baggrund af en referencetype.</span><span class="sxs-lookup"><span data-stu-id="e25ab-156">You can use questionnaire schedules to generate multiple planned answer sessions for a group of users, based on a reference type.</span></span> <span data-ttu-id="e25ab-157">Opret en tidsplan på siden **Spørgeskemaplaner**.</span><span class="sxs-lookup"><span data-stu-id="e25ab-157">Create a schedule on the **Questionnaire schedules** page.</span></span> <span data-ttu-id="e25ab-158">Vælg planlægningsgruppen for at kategorisere tidsplanen, og vælg også den referencetype, der skal bruges til at forespørge i systemet efter bestemte brugere.</span><span class="sxs-lookup"><span data-stu-id="e25ab-158">Select the planning type to categorize the schedule, and also select the reference type that should be used to query the system for specific users.</span></span> <span data-ttu-id="e25ab-159">For eksempel hvis du indstiller referencetypen til tabellen Kurser, kan du vælge et bestemt kursus i feltet **Reference**.</span><span class="sxs-lookup"><span data-stu-id="e25ab-159">For example, if you set the reference type to the Courses table, you can select a specific course in the **Reference** field.</span></span> 

<span data-ttu-id="e25ab-160">Klik på **Oplysninger om opsætning** for at vælge spørgeskemaet og andre kriterier.</span><span class="sxs-lookup"><span data-stu-id="e25ab-160">Click **Setup details** to select the questionnaire and other criteria.</span></span> <span data-ttu-id="e25ab-161">For eksempel angiv instruktørens navn som et kriterium, hvis spørgeskemaet er en vurdering af instruktøren.</span><span class="sxs-lookup"><span data-stu-id="e25ab-161">For example, specify the instructor's name as a criterion if the questionnaire is an evaluation of the instructor.</span></span> <span data-ttu-id="e25ab-162">Når du er færdig med at indtaste oplysninger om opsætningen, genererer systemet planlagte besvarelsessessioner for de brugere, der er medtaget i forespørgslen.</span><span class="sxs-lookup"><span data-stu-id="e25ab-162">After you've finished entering the setup details, the system generates planned answer sessions for the users that are included in the query.</span></span> 

<span data-ttu-id="e25ab-163">Klik på **Planlagte besvarelser** for at få vist besvarelser for planen.</span><span class="sxs-lookup"><span data-stu-id="e25ab-163">Click **Planned answer sessions** to view the answer sessions for the schedule.</span></span> <span data-ttu-id="e25ab-164">Du kan derefter manuelt oprette yderligere planlagte besvarelser eller slette planlagte besvarelser, der ikke er besvaret.</span><span class="sxs-lookup"><span data-stu-id="e25ab-164">You can then manually create additional planned answer sessions or delete planned answer sessions that haven't been answered.</span></span> 

<span data-ttu-id="e25ab-165">Klik på **Funktioner** &gt; **Start** for at gøre spørgeskemaet tilgængeligt for brugerne i relaterede planlagte besvarelsessessioner.</span><span class="sxs-lookup"><span data-stu-id="e25ab-165">Click **Functions** &gt; **Start** to make the questionnaire available to the users in related planned answer sessions.</span></span> <span data-ttu-id="e25ab-166">Klik på **Svar** for at få vist de fuldførte besvarelser af spørgeskemaerne.</span><span class="sxs-lookup"><span data-stu-id="e25ab-166">Click **Answers** to view the completed responses to the questionnaire.</span></span> <span data-ttu-id="e25ab-167">Du kan også kopiere indstillingerne for spørgeskemaplanen, planlagte besvarelser og svar på en ny spørgeskemaplan.</span><span class="sxs-lookup"><span data-stu-id="e25ab-167">You can optionally copy the questionnaire schedule settings, planned answer sessions, and answers to a new questionnaire schedule.</span></span>

## <a name="notifying-respondents-about-questionnaires-that-are-available-to-them"></a><span data-ttu-id="e25ab-168">Besked til svarpersoner om spørgeskemaer, der er tilgængelige for dem</span><span class="sxs-lookup"><span data-stu-id="e25ab-168">Notifying respondents about questionnaires that are available to them</span></span>
<span data-ttu-id="e25ab-169">Når du distribuerer et spørgeskema, skal du give svarpersonerne besked om, at spørgeskemaerne er tilgængelige for dem.</span><span class="sxs-lookup"><span data-stu-id="e25ab-169">When you distribute a questionnaire, you must notify respondents that questionnaires are available to them.</span></span> 

### <a name="notifying-respondents-about-a-planned-answer-session"></a><span data-ttu-id="e25ab-170">Besked til svarpersoner om en planlagt besvarelse</span><span class="sxs-lookup"><span data-stu-id="e25ab-170">Notifying respondents about a planned answer session</span></span>

<span data-ttu-id="e25ab-171">Hvis du bruger en planlagt besvarelse, skal du give personen besked direkte, f.eks. via telefon eller e-mail.</span><span class="sxs-lookup"><span data-stu-id="e25ab-171">If you use a planned answer session, you must notify the person directly, such as by telephone or email.</span></span>

### <a name="notifying-respondents-about-a-scheduling"></a><span data-ttu-id="e25ab-172">Besked til svarpersoner om en planlægning</span><span class="sxs-lookup"><span data-stu-id="e25ab-172">Notifying respondents about a scheduling</span></span>

<span data-ttu-id="e25ab-173">Brug siden **Spørgeskemaplaner** til at forberede og sende en e-mail til alle svarpersoner, der er tilknyttet spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="e25ab-173">Use the **Questionnaire schedules** page to prepare and send email to all respondents who are assigned to the questionnaire.</span></span> <span data-ttu-id="e25ab-174">Angiv mailteksten under fanen **Mail til medarbejderselvbetjening**. Når planen er startet, skal du klikke på **Funktioner** &gt; **Send mail** for at generere og sende mailen til svarpersonerne.</span><span class="sxs-lookup"><span data-stu-id="e25ab-174">Enter the email text on the **E-mail for employee self service** tab. After the schedule has been started, click **Functions** &gt; **Send e-mail** to generate and send the email to the respondents.</span></span> <span data-ttu-id="e25ab-175">Svarpersonerne kan derefter logge på webstedet og udfylde spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="e25ab-175">Respondents can then sign in to the website and complete the questionnaire.</span></span> 

> <span data-ttu-id="e25ab-176">**Bemærk!** Før du kan bruge e-mailfunktionen, skal din it-administrator angive e-mailindstillingerne på siden **E-mailparametre**.</span><span class="sxs-lookup"><span data-stu-id="e25ab-176">**Note** Before you can use the email functionality, your IT administrator must enter the email settings on the **E-mail parameters** page.</span></span>

## <a name="ending-a-scheduled-questionnaire"></a><span data-ttu-id="e25ab-177">Afslutning af et planlagt spørgeskema</span><span class="sxs-lookup"><span data-stu-id="e25ab-177">Ending a scheduled questionnaire</span></span>
<span data-ttu-id="e25ab-178">Du kan afslutte et planlagt spørgeskema, når alle svarpersoner har udfyldt deres tildelte besvarelser.</span><span class="sxs-lookup"><span data-stu-id="e25ab-178">You can end a scheduled questionnaire after all respondents have completed their assigned answer sessions.</span></span> <span data-ttu-id="e25ab-179">Når et planlagt spørgeskema er afsluttet, kan du ikke kopiere indstillingerne til en ny tidsplan.</span><span class="sxs-lookup"><span data-stu-id="e25ab-179">After a scheduled questionnaire is ended, you can't copy its settings to a new schedule.</span></span> 

> <span data-ttu-id="e25ab-180">**Bemærk!** Hvis en eller flere svarpersoner ikke har fuldført spørgeskemaet, men du stadig vil afslutte planlægningen, skal du først slette disse svarpersoner fra listen på siden **Planlagte besvarelser**.</span><span class="sxs-lookup"><span data-stu-id="e25ab-180">**Note** If one or more respondents haven't completed the questionnaire, but you still want to end the scheduling, you must first delete those respondents from the list on the **Planned answer session** page.</span></span> <span data-ttu-id="e25ab-181">Derefter kan du slette tidsplanen.</span><span class="sxs-lookup"><span data-stu-id="e25ab-181">You can then end the schedule.</span></span>

## <a name="completing-questionnaires"></a><span data-ttu-id="e25ab-182">Besvare spørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="e25ab-182">Completing questionnaires</span></span>
<span data-ttu-id="e25ab-183">Når du har designet og distribueret et spørgeskema, kan spørgeskemaet udfyldes af udvalgte svarpersoner.</span><span class="sxs-lookup"><span data-stu-id="e25ab-183">After you've designed and distributed a questionnaire, the questionnaire can be completed by selected respondents.</span></span> <span data-ttu-id="e25ab-184">Du kan udfylde de spørgeskemaer, der er tilgængelige for dig, fra to steder:</span><span class="sxs-lookup"><span data-stu-id="e25ab-184">You can complete the questionnaires that are available to you from two locations:</span></span>

-   <span data-ttu-id="e25ab-185">Klik i navigationsruden på **Spørgeskemaer** &gt; **Distribuer** &gt; **Besvar et spørgeskema**.</span><span class="sxs-lookup"><span data-stu-id="e25ab-185">In the navigation pane, click **Questionnaires** &gt; **Distribute** &gt; **Complete a questionnaire**.</span></span>
-   <span data-ttu-id="e25ab-186">Klik på **Spørgeskemaer, der skal udfyldes** i Medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="e25ab-186">In Employee self-service, click **Questionnaires to complete**.</span></span>

<span data-ttu-id="e25ab-187">Spørgeskemaer kan gøres tilgængelige for bestemte brugere eller brugergrupper eller for alle brugere på et netværk.</span><span class="sxs-lookup"><span data-stu-id="e25ab-187">Questionnaires can made be available to specific users or groups of users, or to all users in a network.</span></span>

<a name="additional-resources"></a><span data-ttu-id="e25ab-188">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e25ab-188">Additional resources</span></span>
--------

[<span data-ttu-id="e25ab-189">Udforme spørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="e25ab-189">Designing questionnaires</span></span>](design-questionnaires.md)

[<span data-ttu-id="e25ab-190">Brug af spørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="e25ab-190">Using questionnaires</span></span>](questionnaires.md)

[<span data-ttu-id="e25ab-191">Visning og evaluering af resultaterne af spørgeskemaer</span><span class="sxs-lookup"><span data-stu-id="e25ab-191">Viewing and evaluating the results of questionnaires</span></span>](evaluate-questionnaire-results.md)


