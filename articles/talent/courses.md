---
title: Konfigurere uddannelseskurser
description: Personaleadministratorer og -chefer kan bruge kursusfunktionerne til at vedligeholde oplysninger om de kurser, der tilbydes til arbejdere.
author: twheeloc
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-talent
ms.technology: 
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable
audience: Application User
ms.reviewer: twheeloc
ms.search.scope: Core, Operations
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: twheeloc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Talent July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: e0b28c62fe586102a3fb98d77edbea2c06bcf852
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-training-courses"></a><span data-ttu-id="a5084-103">Konfigurere uddannelseskurser</span><span class="sxs-lookup"><span data-stu-id="a5084-103">Set up training courses</span></span>

[!include[banner](includes/banner.md)]


<span data-ttu-id="a5084-104">Personaleadministratorer og -chefer kan bruge kursusfunktionerne til at vedligeholde oplysninger om de kurser, der tilbydes til arbejdere.</span><span class="sxs-lookup"><span data-stu-id="a5084-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="a5084-105"> Angiv forudsætninger</span><span class="sxs-lookup"><span data-stu-id="a5084-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="a5084-106">Følgende oplysninger er påkrævet og skal konfigureres, før du opretter kurser.</span><span class="sxs-lookup"><span data-stu-id="a5084-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="a5084-107">**Kursustyper**</span><span class="sxs-lookup"><span data-stu-id="a5084-107">**Course types**</span></span>

<span data-ttu-id="a5084-108">Følgende oplysninger er valgfrie oplysninger, du kan angive for kurser.</span><span class="sxs-lookup"><span data-stu-id="a5084-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="a5084-109">Hvis du ved, at du kommer til at angive disse oplysninger for kurser, skal du konfigurere oplysningerne, før du opretter kursusposter.</span><span class="sxs-lookup"><span data-stu-id="a5084-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="a5084-110">**Kursuslokalegrupper**</span><span class="sxs-lookup"><span data-stu-id="a5084-110">**Classroom groups**</span></span>
-   <span data-ttu-id="a5084-111">**Kursusgrupper**</span><span class="sxs-lookup"><span data-stu-id="a5084-111">**Course groups**</span></span>
-   <span data-ttu-id="a5084-112">**Kursussteder**</span><span class="sxs-lookup"><span data-stu-id="a5084-112">**Course locations**</span></span>
-   <span data-ttu-id="a5084-113">**Kursuslokaler**</span><span class="sxs-lookup"><span data-stu-id="a5084-113">**Classrooms**</span></span>
-   <span data-ttu-id="a5084-114">**Instruktører**</span><span class="sxs-lookup"><span data-stu-id="a5084-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="a5084-115">Kursustyper</span><span class="sxs-lookup"><span data-stu-id="a5084-115">Course types</span></span>
<span data-ttu-id="a5084-116">Du kan bruge kursustyper til at kategorisere kurser efter kursets struktur eller indhold.</span><span class="sxs-lookup"><span data-stu-id="a5084-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="a5084-117">Du kan oprette kursustyper på siden **Kursustyper**.</span><span class="sxs-lookup"><span data-stu-id="a5084-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="a5084-118">Du skal vælge en kursustype, når du opretter en kursuspost.</span><span class="sxs-lookup"><span data-stu-id="a5084-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="a5084-119">Opsætningstype for kursus</span><span class="sxs-lookup"><span data-stu-id="a5084-119">Course setup type</span></span>
<span data-ttu-id="a5084-120">Følgende tabel viser de tre opsætningstyper for kurser.</span><span class="sxs-lookup"><span data-stu-id="a5084-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="a5084-121">Opsætningstyper bestemmer kursets struktur.</span><span class="sxs-lookup"><span data-stu-id="a5084-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a5084-122">Opsætningstype</span><span class="sxs-lookup"><span data-stu-id="a5084-122">Setup type</span></span></th>
<th><span data-ttu-id="a5084-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a5084-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5084-124"><strong>Standard</strong></span><span class="sxs-lookup"><span data-stu-id="a5084-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="a5084-125">Vælg denne type for kurser, der ikke har en daglig agenda.</span><span class="sxs-lookup"><span data-stu-id="a5084-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="a5084-126">Dette er standardopsætningstypen, når du opretter et nyt kursus.</span><span class="sxs-lookup"><span data-stu-id="a5084-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5084-127"><strong>Agenda</strong></span><span class="sxs-lookup"><span data-stu-id="a5084-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="a5084-128">Vælg denne type for at planlægge detaljerne for hver dag i et kursus, der finder sted over flere dage.</span><span class="sxs-lookup"><span data-stu-id="a5084-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5084-129"><strong>Agenda + session</strong></span><span class="sxs-lookup"><span data-stu-id="a5084-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="a5084-130">Vælg denne type for mere komplekse kurser.</span><span class="sxs-lookup"><span data-stu-id="a5084-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="a5084-131">For eksempel kan du opdele agendaen for kurset i spor og sessioner.</span><span class="sxs-lookup"><span data-stu-id="a5084-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="a5084-132"><strong>Spor</strong> – Spor er specifikke emneområder for et kursus.</span><span class="sxs-lookup"><span data-stu-id="a5084-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="a5084-133"><strong>Sessioner</strong> – Sessioner underopdeler spor og hjælper med at identificere specifikke processer eller teknikker, der er relevante for sporet.</span><span class="sxs-lookup"><span data-stu-id="a5084-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="a5084-134">Kursusopgaver</span><span class="sxs-lookup"><span data-stu-id="a5084-134">Course tasks</span></span>
<span data-ttu-id="a5084-135">For hvert kursus kan udføre følgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="a5084-135">For each course, you can complete the following tasks.</span></span>
-   <span data-ttu-id="a5084-136">Registrere deltagere</span><span class="sxs-lookup"><span data-stu-id="a5084-136">Register participants</span></span>
-   <span data-ttu-id="a5084-137">Angive en tilmeldingsfrist</span><span class="sxs-lookup"><span data-stu-id="a5084-137">Specify a registration deadline</span></span>
-   <span data-ttu-id="a5084-138">Angive det mindste og største antal deltagere</span><span class="sxs-lookup"><span data-stu-id="a5084-138">Define the minimum and maximum number of participants</span></span>
-   <span data-ttu-id="a5084-139">Tildel et kursussted og et lokale</span><span class="sxs-lookup"><span data-stu-id="a5084-139">Assign a course location and classroom</span></span>
-   <span data-ttu-id="a5084-140">Anbefal hoteller til kursusdeltagere</span><span class="sxs-lookup"><span data-stu-id="a5084-140">Recommend hotels to course participants</span></span>
-   <span data-ttu-id="a5084-141">Oprette en kursusbeskrivelse, som derefter kan offentliggøres på Medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="a5084-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="a5084-142">**Bemærk!** Du kan kun slette et kursus, hvis ingen har tilmeldt sig kurset.</span><span class="sxs-lookup"><span data-stu-id="a5084-142">**Note** You can delete a course only if no one has registered for it.</span></span> 
    
## <a name="course-statuses"></a><span data-ttu-id="a5084-143">Kursusstatusser</span><span class="sxs-lookup"><span data-stu-id="a5084-143">Course statuses</span></span>
<span data-ttu-id="a5084-144">I følgende tabel vises de mulige statusser for kurser og de handlinger, du kan udføre, når kurset har en bestemt status.</span><span class="sxs-lookup"><span data-stu-id="a5084-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="a5084-145">Status</span><span class="sxs-lookup"><span data-stu-id="a5084-145">Status</span></span></th>
<th><span data-ttu-id="a5084-146">Aktioner</span><span class="sxs-lookup"><span data-stu-id="a5084-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="a5084-147"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="a5084-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="a5084-148">Angiv og rediger kursusoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a5084-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="a5084-149">Rediger status for kurset til <strong>Åbn</strong>, så medarbejderne kan tilmelde sig kurset.</span><span class="sxs-lookup"><span data-stu-id="a5084-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5084-150"><strong>Åben</strong></span><span class="sxs-lookup"><span data-stu-id="a5084-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="a5084-151">Meld deltagerne til kurset.</span><span class="sxs-lookup"><span data-stu-id="a5084-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="a5084-152">Fjern deltagere fra kurset.</span><span class="sxs-lookup"><span data-stu-id="a5084-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="a5084-153">Bekræfte deltageres tilmelding til kurset.</span><span class="sxs-lookup"><span data-stu-id="a5084-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="a5084-154">Rediger status for kurset til<strong> Lukket</strong> eller <strong>Annulleret</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5084-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="a5084-155">Planlæg spørgeskemaer for deltagere, som har status <strong>Bekræftet</strong>.</span><span class="sxs-lookup"><span data-stu-id="a5084-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="a5084-156"><strong>Lukket</strong></span><span class="sxs-lookup"><span data-stu-id="a5084-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="a5084-157">Du kan genåbne kurset.</span><span class="sxs-lookup"><span data-stu-id="a5084-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="a5084-158"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="a5084-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="a5084-159">Du kan genåbne kurset.</span><span class="sxs-lookup"><span data-stu-id="a5084-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="a5084-160">Kursusdeltagere</span><span class="sxs-lookup"><span data-stu-id="a5084-160">Course participants</span></span>
<span data-ttu-id="a5084-161">Kursusdeltagere er arbejdere, jobansøgere eller kontaktpersoner, der deltager i et kursus eller anden undervisning.</span><span class="sxs-lookup"><span data-stu-id="a5084-161">Course participants are workers, applicants, or contact persons who participate in a training course or event.</span></span> <span data-ttu-id="a5084-162">Du kan kun melde deltagere til åbne kurser.</span><span class="sxs-lookup"><span data-stu-id="a5084-162">You can only register participants for open courses.</span></span> <span data-ttu-id="a5084-163">Det laveste og højeste antal deltagere, du kan tilmelde et kursus, er angivet i oversigtspanelet **Generelt** på siden **Kurser**.</span><span class="sxs-lookup"><span data-stu-id="a5084-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="a5084-164">Arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="a5084-164">Workflow</span></span>
--------

<span data-ttu-id="a5084-165">Medarbejdere, der tilmelder sig et kursus på siden **Medarbejderselvbetjening**, kan få deres tilmelding dirigeret gennem godkendelsesarbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="a5084-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span>  <span data-ttu-id="a5084-166">En arbejdsgang kan tildeles til et kursus i oversigtspanelet **Generelt** på siden **Kurser**.</span><span class="sxs-lookup"><span data-stu-id="a5084-166">A workflow can be assigned to a course on the **General** FastTab on the **Courses** page.</span></span>






