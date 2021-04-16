---
title: Konfigurere uddannelseskurser
description: Human Resourcesadministratorer og -chefer kan bruge kursusfunktionerne til at vedligeholde oplysninger om de kurser, der tilbydes til arbejdere.
author: andreabichsel
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: HcmCourseType, HcmCourseTypeGroup, HRMCourseTable, HcmLearningWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7532
ms.assetid: a6950c29-8b3e-45b2-9084-ddfb1317ffaa
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Human Resources
ms.openlocfilehash: 0718987583d02a76acc2420e5a371c418757e384
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5793531"
---
# <a name="set-up-training-courses"></a><span data-ttu-id="b3956-103">Konfigurere uddannelseskurser</span><span class="sxs-lookup"><span data-stu-id="b3956-103">Set up training courses</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b3956-104">Human Resourcesadministratorer og -chefer kan bruge kursusfunktionerne til at vedligeholde oplysninger om de kurser, der tilbydes til arbejdere.</span><span class="sxs-lookup"><span data-stu-id="b3956-104">Human resources administrators and managers can use the courses features to maintain information about the training that's offered to workers.</span></span>

 <a name="set-up-prerequisites"></a><span data-ttu-id="b3956-105"> Angiv forudsætninger</span><span class="sxs-lookup"><span data-stu-id="b3956-105">Set up prerequisites</span></span>
---------------------

<span data-ttu-id="b3956-106">Følgende oplysninger er påkrævet og skal konfigureres, før du opretter kurser.</span><span class="sxs-lookup"><span data-stu-id="b3956-106">The following information is required and must be set up before you create courses.</span></span>
-   <span data-ttu-id="b3956-107">**Kursustyper**</span><span class="sxs-lookup"><span data-stu-id="b3956-107">**Course types**</span></span>

<span data-ttu-id="b3956-108">Følgende oplysninger er valgfrie oplysninger, du kan angive for kurser.</span><span class="sxs-lookup"><span data-stu-id="b3956-108">The following information is optional information that you can specify for courses.</span></span> <span data-ttu-id="b3956-109">Hvis du ved, at du kommer til at angive disse oplysninger for kurser, skal du konfigurere oplysningerne, før du opretter kursusposter.</span><span class="sxs-lookup"><span data-stu-id="b3956-109">If you know that you will be entering this information for courses, you should set up this information before you create course records.</span></span>
-   <span data-ttu-id="b3956-110">**Kursuslokalegrupper**</span><span class="sxs-lookup"><span data-stu-id="b3956-110">**Classroom groups**</span></span>
-   <span data-ttu-id="b3956-111">**Kursusgrupper**</span><span class="sxs-lookup"><span data-stu-id="b3956-111">**Course groups**</span></span>
-   <span data-ttu-id="b3956-112">**Kursussteder**</span><span class="sxs-lookup"><span data-stu-id="b3956-112">**Course locations**</span></span>
-   <span data-ttu-id="b3956-113">**Kursuslokaler**</span><span class="sxs-lookup"><span data-stu-id="b3956-113">**Classrooms**</span></span>
-   <span data-ttu-id="b3956-114">**Instruktører**</span><span class="sxs-lookup"><span data-stu-id="b3956-114">**Instructors**</span></span>

## <a name="course-types"></a><span data-ttu-id="b3956-115">Kursustyper</span><span class="sxs-lookup"><span data-stu-id="b3956-115">Course types</span></span>
<span data-ttu-id="b3956-116">Du kan bruge kursustyper til at kategorisere kurser efter kursets struktur eller indhold.</span><span class="sxs-lookup"><span data-stu-id="b3956-116">You can use course types to categorize courses according to the structure or content of the course.</span></span> <span data-ttu-id="b3956-117">Du kan oprette kursustyper på siden **Kursustyper**.</span><span class="sxs-lookup"><span data-stu-id="b3956-117">You can create course types on the **Course types** page.</span></span> <span data-ttu-id="b3956-118">Du skal vælge en kursustype, når du opretter en kursuspost.</span><span class="sxs-lookup"><span data-stu-id="b3956-118">You must select a course type when you create a course record.</span></span>

## <a name="course-setup-type"></a><span data-ttu-id="b3956-119">Opsætningstype for kursus</span><span class="sxs-lookup"><span data-stu-id="b3956-119">Course setup type</span></span>
<span data-ttu-id="b3956-120">Følgende tabel viser de tre opsætningstyper for kurser.</span><span class="sxs-lookup"><span data-stu-id="b3956-120">The following table lists the three setup types for courses.</span></span> <span data-ttu-id="b3956-121">Opsætningstyper bestemmer kursets struktur.</span><span class="sxs-lookup"><span data-stu-id="b3956-121">Setup types determine the structure of the course.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3956-122">Opsætningstype</span><span class="sxs-lookup"><span data-stu-id="b3956-122">Setup type</span></span></th>
<th><span data-ttu-id="b3956-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b3956-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3956-124"><strong>Standard</strong></span><span class="sxs-lookup"><span data-stu-id="b3956-124"><strong>Standard</strong></span></span></td>
<td><span data-ttu-id="b3956-125">Vælg denne type for kurser, der ikke har en daglig agenda.</span><span class="sxs-lookup"><span data-stu-id="b3956-125">Select this type for courses that will not have a daily agenda.</span></span> <span data-ttu-id="b3956-126">Dette er standardopsætningstypen, når du opretter et nyt kursus.</span><span class="sxs-lookup"><span data-stu-id="b3956-126">This is the default setup type when you create a new course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3956-127"><strong>Agenda</strong></span><span class="sxs-lookup"><span data-stu-id="b3956-127"><strong>Agenda</strong></span></span></td>
<td><span data-ttu-id="b3956-128">Vælg denne type for at planlægge detaljerne for hver dag i et kursus, der finder sted over flere dage.</span><span class="sxs-lookup"><span data-stu-id="b3956-128">Select this type to plan the details of each day of a course that takes place over multiple days.</span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3956-129"><strong>Agenda + session</strong></span><span class="sxs-lookup"><span data-stu-id="b3956-129"><strong>Agenda + session</strong></span></span></td>
<td><span data-ttu-id="b3956-130">Vælg denne type for mere komplekse kurser.</span><span class="sxs-lookup"><span data-stu-id="b3956-130">Select this type for the more complex courses.</span></span> <span data-ttu-id="b3956-131">For eksempel kan du opdele agendaen for kurset i spor og sessioner.</span><span class="sxs-lookup"><span data-stu-id="b3956-131">For example, you can divide the agenda for the course into tracks and sessions.</span></span>
<ul>
<li><span data-ttu-id="b3956-132"><strong>Spor</strong> – Spor er specifikke emneområder for et kursus.</span><span class="sxs-lookup"><span data-stu-id="b3956-132"><strong>Track</strong> – Tracks are specific subject areas for a course.</span></span></li>
<li><span data-ttu-id="b3956-133"><strong>Sessioner</strong> – Sessioner underopdeler spor og hjælper med at identificere specifikke processer eller teknikker, der er relevante for sporet.</span><span class="sxs-lookup"><span data-stu-id="b3956-133"><strong>Sessions</strong> – Sessions divide up tracks and help identify specific processes or techniques that are relevant to the track.</span></span></li>
</ul></td>
</tr>
</tbody>
</table>

## <a name="course-tasks"></a><span data-ttu-id="b3956-134">Kursusopgaver</span><span class="sxs-lookup"><span data-stu-id="b3956-134">Course tasks</span></span>
<span data-ttu-id="b3956-135">For hvert kursus kan udføre følgende opgaver.</span><span class="sxs-lookup"><span data-stu-id="b3956-135">For each course, you can complete the following tasks.</span></span>
- <span data-ttu-id="b3956-136">Registrere deltagere</span><span class="sxs-lookup"><span data-stu-id="b3956-136">Register participants</span></span>
- <span data-ttu-id="b3956-137">Angive en tilmeldingsfrist</span><span class="sxs-lookup"><span data-stu-id="b3956-137">Specify a registration deadline</span></span>
- <span data-ttu-id="b3956-138">Angive det mindste og største antal deltagere</span><span class="sxs-lookup"><span data-stu-id="b3956-138">Define the minimum and maximum number of participants</span></span>
- <span data-ttu-id="b3956-139">Tildel et kursussted og et lokale</span><span class="sxs-lookup"><span data-stu-id="b3956-139">Assign a course location and classroom</span></span>
- <span data-ttu-id="b3956-140">Anbefal hoteller til kursusdeltagere</span><span class="sxs-lookup"><span data-stu-id="b3956-140">Recommend hotels to course participants</span></span>
- <span data-ttu-id="b3956-141">Oprette en kursusbeskrivelse, som derefter kan offentliggøres på Medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="b3956-141">Create a course description, which you can then advertise on Employee self service</span></span>

  ><span data-ttu-id="b3956-142">**Bemærk!** Du kan kun slette et kursus, hvis ingen har tilmeldt sig kurset.</span><span class="sxs-lookup"><span data-stu-id="b3956-142">**Note** You can delete a course only if no one has registered for it.</span></span> 

## <a name="course-statuses"></a><span data-ttu-id="b3956-143">Kursusstatusser</span><span class="sxs-lookup"><span data-stu-id="b3956-143">Course statuses</span></span>
<span data-ttu-id="b3956-144">I følgende tabel vises de mulige statusser for kurser og de handlinger, du kan udføre, når kurset har en bestemt status.</span><span class="sxs-lookup"><span data-stu-id="b3956-144">The following table lists the possible course statuses and the actions that you can complete when the course has a specific status.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b3956-145">Status</span><span class="sxs-lookup"><span data-stu-id="b3956-145">Status</span></span></th>
<th><span data-ttu-id="b3956-146">Aktioner</span><span class="sxs-lookup"><span data-stu-id="b3956-146">Actions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b3956-147"><strong>Oprettet</strong></span><span class="sxs-lookup"><span data-stu-id="b3956-147"><strong>Created</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="b3956-148">Angiv og rediger kursusoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b3956-148">Enter and modify course information.</span></span></li>
<li><span data-ttu-id="b3956-149">Rediger status for kurset til <strong>Åbn</strong>, så medarbejderne kan tilmelde sig kurset.</span><span class="sxs-lookup"><span data-stu-id="b3956-149">Change the course status to <strong>Open</strong> so that workers can register for the course.</span></span></li>
</ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3956-150"><strong>Åben</strong></span><span class="sxs-lookup"><span data-stu-id="b3956-150"><strong>Open</strong></span></span></td>
<td><ul>
<li><span data-ttu-id="b3956-151">Meld deltagerne til kurset.</span><span class="sxs-lookup"><span data-stu-id="b3956-151">Register participants for the course.</span></span></li>
<li><span data-ttu-id="b3956-152">Fjern deltagere fra kurset.</span><span class="sxs-lookup"><span data-stu-id="b3956-152">Remove participants from the course.</span></span></li>
<li><span data-ttu-id="b3956-153">Bekræfte deltageres tilmelding til kurset.</span><span class="sxs-lookup"><span data-stu-id="b3956-153">Confirm participants for the course.</span></span></li>
<li><span data-ttu-id="b3956-154">Rediger status for kurset til<strong> Lukket</strong> eller <strong>Annulleret</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3956-154">Change the course status to <strong>Closed</strong> or <strong>Canceled</strong>.</span></span></li>
<li><span data-ttu-id="b3956-155">Planlæg spørgeskemaer for deltagere, som har status <strong>Bekræftet</strong>.</span><span class="sxs-lookup"><span data-stu-id="b3956-155">Plan questionnaires for participants whose status is <strong>Confirmed</strong>.</span></span></li>
</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="b3956-156"><strong>Lukket</strong></span><span class="sxs-lookup"><span data-stu-id="b3956-156"><strong>Closed</strong></span></span></td>
<td><span data-ttu-id="b3956-157">Du kan genåbne kurset.</span><span class="sxs-lookup"><span data-stu-id="b3956-157">You can reopen the course.</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b3956-158"><strong>Annulleret</strong></span><span class="sxs-lookup"><span data-stu-id="b3956-158"><strong>Canceled</strong></span></span></td>
<td><span data-ttu-id="b3956-159">Du kan genåbne kurset.</span><span class="sxs-lookup"><span data-stu-id="b3956-159">You can reopen the course.</span></span></td>
</tr>
</tbody>
</table>

## <a name="course-participants"></a><span data-ttu-id="b3956-160">Kursusdeltagere</span><span class="sxs-lookup"><span data-stu-id="b3956-160">Course participants</span></span>
<span data-ttu-id="b3956-161">Kursusdeltagere er arbejdere, der deltager i et kursus eller anden undervisning.</span><span class="sxs-lookup"><span data-stu-id="b3956-161">Course participants are workers who participate in a training course or event.</span></span> <span data-ttu-id="b3956-162">Du kan kun melde deltagere til åbne kurser.</span><span class="sxs-lookup"><span data-stu-id="b3956-162">You can only register participants for open courses.</span></span> <span data-ttu-id="b3956-163">Det laveste og højeste antal deltagere, du kan tilmelde et kursus, er angivet i oversigtspanelet **Generelt** på siden **Kurser**.</span><span class="sxs-lookup"><span data-stu-id="b3956-163">The minimum and maximum number of participants that you can register for a course is defined on the **General** FastTab on the **Courses** page.</span></span>

<a name="workflow"></a><span data-ttu-id="b3956-164">Arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="b3956-164">Workflow</span></span>
--------

<span data-ttu-id="b3956-165">Medarbejdere, der tilmelder sig et kursus på siden **Medarbejderselvbetjening**, kan få deres tilmelding dirigeret gennem godkendelsesarbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="b3956-165">Employees who register for a course through the **Employee self service** page can have their registration routed through workflow for approval.</span></span> <span data-ttu-id="b3956-166">Du kan tildele en arbejdsgang et kursus i oversigtspanelet **Generelt** på siden **Kurser**.</span><span class="sxs-lookup"><span data-stu-id="b3956-166">You can assign a workflow to a course on the **General** FastTab on the **Courses** page.</span></span>







[!INCLUDE[footer-include](../includes/footer-banner.md)]