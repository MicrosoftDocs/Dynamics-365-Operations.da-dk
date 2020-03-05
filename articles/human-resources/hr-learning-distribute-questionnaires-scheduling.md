---
title: Udsende spørgeskemaer ved hjælp af planlægning
description: Planlægning af spørgeskemaet kan du planlægge og fordele spørgeskemaer til flere svarpersoner.
author: andreabichsel
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: KMKnowledgeCollectorPlanningTable, KMKnowledgeCollectorPlanningMulti, SysQueryForm, HcmPersonLookup, KMKnowledgeCollectorPlanning
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 0448a7ebe802a961c8c1296ef57d12ea22e4ec27
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008511"
---
# <a name="distribute-questionnaires-using-scheduling"></a><span data-ttu-id="7deee-103">Udsende spørgeskemaer ved hjælp af planlægning</span><span class="sxs-lookup"><span data-stu-id="7deee-103">Distribute questionnaires using scheduling</span></span>

<span data-ttu-id="7deee-104">Planlægning af spørgeskemaet kan du planlægge og fordele spørgeskemaer til flere svarpersoner.</span><span class="sxs-lookup"><span data-stu-id="7deee-104">Questionnaire scheduling allows you to plan and distribute questionnaires to multiple respondents.</span></span> <span data-ttu-id="7deee-105">Det demodatafirma, der bruges til at oprette denne procedure, er USMF.</span><span class="sxs-lookup"><span data-stu-id="7deee-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="create-a-questionnaire-schedule"></a><span data-ttu-id="7deee-106">Opret en tidsplan for et spørgeskema</span><span class="sxs-lookup"><span data-stu-id="7deee-106">Create a questionnaire schedule</span></span>

1. <span data-ttu-id="7deee-107">Gå til spørgeskemaet > fordel > tidsplaner for spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="7deee-107">Go to Questionnaire > Distribute > Questionnaire schedules.</span></span>

2. <span data-ttu-id="7deee-108">Klik på Ny.</span><span class="sxs-lookup"><span data-stu-id="7deee-108">Click New.</span></span>

3. <span data-ttu-id="7deee-109">Skriv en værdi i feltet Planlægning.</span><span class="sxs-lookup"><span data-stu-id="7deee-109">In the Scheduling field, type a value.</span></span>

4. <span data-ttu-id="7deee-110">Skriv en værdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="7deee-110">In the Description field, type a value.</span></span>
    * <span data-ttu-id="7deee-111">Angiv tidsplanen til anonym, hvis svarene skal registreres uden navne, der er knyttet til svaret.</span><span class="sxs-lookup"><span data-stu-id="7deee-111">Set the schedule to Anonymous if the responses should be recorded without names associated to the response.</span></span>  
    * <span data-ttu-id="7deee-112">Tilladelse af anonyme resultater skal først oprettes i HR-parametrene.</span><span class="sxs-lookup"><span data-stu-id="7deee-112">Allowing anonymous results must be set up in the HR parameters first.</span></span>  

5. <span data-ttu-id="7deee-113">Vælg planlægningstypen i feltet Type.</span><span class="sxs-lookup"><span data-stu-id="7deee-113">In the Type field, select the planning type.</span></span>  <span data-ttu-id="7deee-114">I dette eksempel bruger vi typen Tilfredshed.</span><span class="sxs-lookup"><span data-stu-id="7deee-114">In this example we will use the Satisfaction type.</span></span>

6. <span data-ttu-id="7deee-115">Find og vælg den ønskede post på listen.</span><span class="sxs-lookup"><span data-stu-id="7deee-115">In the list, find and select the desired record.</span></span>

7. <span data-ttu-id="7deee-116">Klik op linket i den valgte række på listen.</span><span class="sxs-lookup"><span data-stu-id="7deee-116">In the list, click the link in the selected row.</span></span>

8. <span data-ttu-id="7deee-117">Indtast en dato i feltet Dato.</span><span class="sxs-lookup"><span data-stu-id="7deee-117">In the Date field, enter a date.</span></span>

9. <span data-ttu-id="7deee-118">Udvid sektionen E-mail for medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="7deee-118">Expand the Email for employee self service section.</span></span>

10. <span data-ttu-id="7deee-119">Skriv en værdi i feltet Emne.</span><span class="sxs-lookup"><span data-stu-id="7deee-119">In the Subject field, type a value.</span></span>

    * <span data-ttu-id="7deee-120">Eksempel: Tilgængeligt spørgeskema</span><span class="sxs-lookup"><span data-stu-id="7deee-120">Example: Questionnaire available</span></span>  

11. <span data-ttu-id="7deee-121">I feltet Tekst skal du skrive mailens brødtekst.</span><span class="sxs-lookup"><span data-stu-id="7deee-121">In the Text field, type the body of your email message.</span></span> <span data-ttu-id="7deee-122">Bemærk, at variablen kan bruges til at erstatte værdier i systemet.</span><span class="sxs-lookup"><span data-stu-id="7deee-122">Note, the variable can be used to substitue values in the system.</span></span>

    * <span data-ttu-id="7deee-123">Eksempel: Kære %P% Log på medarbejderselvbetjening for at udfylde spørgeskemaet om medarbejdernes sundhed.</span><span class="sxs-lookup"><span data-stu-id="7deee-123">Example: Dear %P%, Please log in to Employee Self Service to complete the Workforce Health questionnaire.</span></span>  <span data-ttu-id="7deee-124">Contoso</span><span class="sxs-lookup"><span data-stu-id="7deee-124">Contoso</span></span>  

12. <span data-ttu-id="7deee-125">Klik på Gem.</span><span class="sxs-lookup"><span data-stu-id="7deee-125">Click Save.</span></span>

## <a name="use-the-setup-details-to-select-the-questionnaires-to-be-answered-as-well-as-any-queries-to-use-to-select-respondents"></a><span data-ttu-id="7deee-126">Brug opsætningsoplysningerne til at vælge eller spørgeskemaer, som skal besvares, samt eventuelle forespørgsler, der skal bruges til valg af svarpersoner.</span><span class="sxs-lookup"><span data-stu-id="7deee-126">Use the Setup details to select the questionnaire(s) to be answered as well as any queries to use to select respondents.</span></span>

1. <span data-ttu-id="7deee-127">Klik på Oplysninger om opsætning.</span><span class="sxs-lookup"><span data-stu-id="7deee-127">Click Setup details.</span></span>

2. <span data-ttu-id="7deee-128">På listen skal du vælge en forespørgsel, som du bruge til at søge i systemet efter svarpersoner til spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="7deee-128">In the list, select a query to use to search the system for respondents for the questionnaire.</span></span>

    * <span data-ttu-id="7deee-129">Eksempel: Arbejdere</span><span class="sxs-lookup"><span data-stu-id="7deee-129">Example: Workers</span></span>  

3. <span data-ttu-id="7deee-130">Klik på Vis eller Rediger forespørgsel for at vælge bestemte personer eller justere forespørgslen for at søge efter personer, der opfylder bestemte søgekriterier.</span><span class="sxs-lookup"><span data-stu-id="7deee-130">Click View or modify query to select specific people or adjust the query to find people who match specific criteria.</span></span>

    * <span data-ttu-id="7deee-131">Bemærk, at alle svarpersoner skal også brugere i systemet.</span><span class="sxs-lookup"><span data-stu-id="7deee-131">Note that all respondents must also be users in the system.</span></span>  

4. <span data-ttu-id="7deee-132">Markér den valgte række for Person.</span><span class="sxs-lookup"><span data-stu-id="7deee-132">In the list, mark the row for Person</span></span>

5. <span data-ttu-id="7deee-133">Indtast eller vælg en værdi i feltet Kriterier.</span><span class="sxs-lookup"><span data-stu-id="7deee-133">In the Criteria field, enter or select a value.</span></span>

    * <span data-ttu-id="7deee-134">Vælg Julia Funderburk</span><span class="sxs-lookup"><span data-stu-id="7deee-134">Select Julia Funderburk</span></span>  

6. <span data-ttu-id="7deee-135">Vælg Julia Funderburk på listen</span><span class="sxs-lookup"><span data-stu-id="7deee-135">In the list, select Julia Funderburk</span></span>

7. <span data-ttu-id="7deee-136">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7deee-136">Click OK.</span></span>

8. <span data-ttu-id="7deee-137">Klik på fanen Spørgeskemaer.</span><span class="sxs-lookup"><span data-stu-id="7deee-137">Click the Questionnaires tab.</span></span>

9. <span data-ttu-id="7deee-138">I træet skal du vælge indstillingen for at få vist noden for spørgeskemaet af typen Tilfredshedsundersøgelse i træet.</span><span class="sxs-lookup"><span data-stu-id="7deee-138">In the tree, expand 'the node for the questionnaire type Satisfaction Survey'.</span></span>

10. <span data-ttu-id="7deee-139">Markér 'Arbejdsstyrken helbredskontrol' i træet.</span><span class="sxs-lookup"><span data-stu-id="7deee-139">In the tree, check 'Workforce Health Assessment'.</span></span>

11. <span data-ttu-id="7deee-140">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7deee-140">Click OK.</span></span>

12. <span data-ttu-id="7deee-141">Klik på Planlagt besvarelse.</span><span class="sxs-lookup"><span data-stu-id="7deee-141">Click Planned answer session.</span></span>

    * <span data-ttu-id="7deee-142">Bemærk, at det planlagte besvarelser, der er oprettet for hver bruger, der er markeret/forespørges.</span><span class="sxs-lookup"><span data-stu-id="7deee-142">Note that Planned answer sessions have been created for each selected/queried user.</span></span>  

13. <span data-ttu-id="7deee-143">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7deee-143">Close the page.</span></span>

## <a name="start-the-questionnaire-schedule-in-order-to-make-the-questionnaire-available-for-respondents-to-complete"></a><span data-ttu-id="7deee-144">Start spørgeskema tidsplanen for at stille til rådighed for svarpersonerne at udfylde spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="7deee-144">Start the questionnaire schedule in order to make the questionnaire available for respondents to complete.</span></span>

1. <span data-ttu-id="7deee-145">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="7deee-145">Click Functions.</span></span>

2. <span data-ttu-id="7deee-146">Klik på Start.</span><span class="sxs-lookup"><span data-stu-id="7deee-146">Click Start.</span></span>

3. <span data-ttu-id="7deee-147">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7deee-147">Click OK.</span></span>

## <a name="send-the-email-to-inform-respondents-of-the-available-questionnaire"></a><span data-ttu-id="7deee-148">Send e-mail til at underrette svarpersoner for det spørgeskema, der er tilgængelige.</span><span class="sxs-lookup"><span data-stu-id="7deee-148">Send the email to inform respondents of the available questionnaire.</span></span>

1. <span data-ttu-id="7deee-149">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="7deee-149">Click Functions.</span></span>

2. <span data-ttu-id="7deee-150">Klik på Send e-mail.</span><span class="sxs-lookup"><span data-stu-id="7deee-150">Click Send email.</span></span>

3. <span data-ttu-id="7deee-151">Klik på Annuller.</span><span class="sxs-lookup"><span data-stu-id="7deee-151">Click Cancel.</span></span>

## <a name="use-planned-answer-sessions-to-monitor-who-needs-to-complete-the-questionnaire"></a><span data-ttu-id="7deee-152">Brug planlagte besvarelser til skærm, der skal udfylde spørgeskemaet.</span><span class="sxs-lookup"><span data-stu-id="7deee-152">Use Planned answer sessions to monitor who needs to complete the questionnaire.</span></span>

1. <span data-ttu-id="7deee-153">Klik på Planlagt besvarelse.</span><span class="sxs-lookup"><span data-stu-id="7deee-153">Click Planned answer session.</span></span>

    * <span data-ttu-id="7deee-154">Slette eventuelle resterende planlagte besvarelser når du er klar til at afslutte den planlagte session.</span><span class="sxs-lookup"><span data-stu-id="7deee-154">Delete any remaining planned answer session when you're ready to end the scheduled session.</span></span>  

2. <span data-ttu-id="7deee-155">Klik på Slet.</span><span class="sxs-lookup"><span data-stu-id="7deee-155">Click Delete.</span></span>

3. <span data-ttu-id="7deee-156">Klik på Ja.</span><span class="sxs-lookup"><span data-stu-id="7deee-156">Click Yes.</span></span>

4. <span data-ttu-id="7deee-157">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="7deee-157">Close the page.</span></span>

## <a name="end-the-schedule-when-all-respondents-have-completed-the-questionnaire-andor-all-remaining-planned-answer-sessions-have-been-deleted"></a><span data-ttu-id="7deee-158">Afslut tidsplanen, når alle svarpersoner har udfyldt spørgeskemaet og/eller alle resterende Planlagte besvarelser-sessioner er slettet.</span><span class="sxs-lookup"><span data-stu-id="7deee-158">End the schedule when all respondents have completed the questionnaire and/or all remaining Planned answer sessions have been deleted.</span></span>

1. <span data-ttu-id="7deee-159">Klik på Funktioner.</span><span class="sxs-lookup"><span data-stu-id="7deee-159">Click Functions.</span></span>
2. <span data-ttu-id="7deee-160">Klik på Afslut.</span><span class="sxs-lookup"><span data-stu-id="7deee-160">Click End.</span></span>
3. <span data-ttu-id="7deee-161">Klik på OK.</span><span class="sxs-lookup"><span data-stu-id="7deee-161">Click OK.</span></span>
