---
title: Konfigurere manuelle opgave i en arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer egenskaberne for en manuel opgave.
author: ChrisGarty
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192191
ms.assetid: 27f1afde-ff26-4b6f-8c11-27ec49130bbb
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: b4be7f0ee5e487185033b7ccb9a2b0a91eb4a36c
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5747849"
---
# <a name="configure-manual-tasks-in-a-workflow"></a><span data-ttu-id="3a3f6-103">Konfigurere manuelle opgave i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="3a3f6-103">Configure manual tasks in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="3a3f6-104">I dette emne forklares det, hvordan du konfigurerer egenskaberne for en manuel opgave.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-104">This topic explains how to configure the properties for a manual task.</span></span>

<span data-ttu-id="3a3f6-105">Hvis du vil konfigurere en manuel opgave i arbejdsgangseditoren, skal du højreklikke på opgaven og derefter klikke på **Egenskaber** for at åbne siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-105">To configure a manual task in the workflow editor, right-click the task, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="3a3f6-106">Brug derefter følgende procedurer for at konfigurere egenskaberne for den manuelle opgave.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-106">Then use the following procedures to configure the properties for the manual task.</span></span>

## <a name="name-the-task"></a><span data-ttu-id="3a3f6-107">Navngive opgaven</span><span class="sxs-lookup"><span data-stu-id="3a3f6-107">Name the task</span></span>

<span data-ttu-id="3a3f6-108">Udfør følgende trin for at angive et navn på den manuelle opgave.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-108">Follow these steps to enter a name for the manual task.</span></span>

1. <span data-ttu-id="3a3f6-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3a3f6-110">Angiv et entydigt navn til opgaven i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-110">In the **Name** field, enter a unique name for the task.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="3a3f6-111">Angive en emnelinje og instruktioner</span><span class="sxs-lookup"><span data-stu-id="3a3f6-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="3a3f6-112">Du skal angive en emnelinje og instruktioner til brugere, som har fået opgaven tildelt.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-112">You must provide a subject line and instructions to users who are assigned to the task.</span></span> <span data-ttu-id="3a3f6-113">Hvis du f.eks. konfigurerer en opgave for indkøbsrekvisitioner, ser den bruger, der har fået opgaven tildelt, emnelinjen og instruktionerne på siden **Indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-113">For example, if you're configuring a task for purchase requisitions, the user who is assigned to the task sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="3a3f6-114">Emnelinjen vises i en meddelelseslinje på siden.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="3a3f6-115">Brugeren kan derefter klikke på ikonet på meddelelseslinjen for at få vist detaljerede instruktioner.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="3a3f6-116">Udfør følgende trin for at angive en emnelinje og instruktioner.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="3a3f6-117">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="3a3f6-118">I feltet **Emne for workflowopgave** skal du indtaste emnelinjen.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="3a3f6-119">Hvis du vil personalisere emnelinjen, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="3a3f6-120">Pladsholderne erstattes med de relevante data, når emnelinjen vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="3a3f6-121">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="3a3f6-122">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3a3f6-123">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3a3f6-124">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3a3f6-125">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-125">Click **Insert**.</span></span>

4. <span data-ttu-id="3a3f6-126">Følg disse trin for at tilføje oversættelser af emnelinjen:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="3a3f6-127">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="3a3f6-128">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3a3f6-129">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3a3f6-130">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3a3f6-131">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 3.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="3a3f6-132">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-132">Click **Close**.</span></span>

5. <span data-ttu-id="3a3f6-133">I feltet **Emne for workflowopgave** skal du indtaste instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="3a3f6-134">Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="3a3f6-135">Pladsholderne erstattes med de relevante data, når instruktionerne vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="3a3f6-136">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="3a3f6-137">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3a3f6-138">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3a3f6-139">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3a3f6-140">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-140">Click **Insert**.</span></span>

7. <span data-ttu-id="3a3f6-141">Følg disse trin for at tilføje oversættelser af instruktionerne:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="3a3f6-142">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="3a3f6-143">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3a3f6-144">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3a3f6-145">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3a3f6-146">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 6.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="3a3f6-147">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-147">Click **Close**.</span></span>

## <a name="assign-the-task"></a><span data-ttu-id="3a3f6-148">Tildele opgaven</span><span class="sxs-lookup"><span data-stu-id="3a3f6-148">Assign the task</span></span>

<span data-ttu-id="3a3f6-149">Udfør følgende trin for at angive, hvem den manuelle opgave skal tildeles til.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-149">Follow these steps to specify who the manual task should be assigned to.</span></span>

1. <span data-ttu-id="3a3f6-150">Klik på **Tildeling** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="3a3f6-151">Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 3.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3a3f6-152">Indstilling</span><span class="sxs-lookup"><span data-stu-id="3a3f6-152">Option</span></span></th>
    <th><span data-ttu-id="3a3f6-153">Brugere, som opgaven er tildelt til</span><span class="sxs-lookup"><span data-stu-id="3a3f6-153">Users that the task is assigned to</span></span></th>
    <th><span data-ttu-id="3a3f6-154">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="3a3f6-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3a3f6-155">Deltager</span><span class="sxs-lookup"><span data-stu-id="3a3f6-155">Participant</span></span></td>
    <td><span data-ttu-id="3a3f6-156">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="3a3f6-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a3f6-157">Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil tildele opgaven til.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the task to.</span></span></li>
    <li><span data-ttu-id="3a3f6-158">Vælg den gruppe eller rolle, som opgaven skal tildeles, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-158">In the <strong>Participant</strong> list, select the group or role to assign the task to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a3f6-159">Hierarki</span><span class="sxs-lookup"><span data-stu-id="3a3f6-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="3a3f6-160">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="3a3f6-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a3f6-161">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil tildele opgaven til.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the task to.</span></span></li>
    <li><span data-ttu-id="3a3f6-162">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="3a3f6-163">Disse navne repræsenterer de brugere, som opgaven kan tildeles.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-163">These names represent users that the task can be assigned to.</span></span> <span data-ttu-id="3a3f6-164">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="3a3f6-165">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="3a3f6-166">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="3a3f6-167">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="3a3f6-168">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet opgaven skal tildeles:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="3a3f6-169"><strong>Tildel til alle hentede brugere</strong> – Opgaven tildeles alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-169"><strong>Assign to all users retrieved</strong> – The task is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="3a3f6-170"><strong>Tildel kun til den sidst hentede bruger</strong> – Opgaven tildeles kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-170"><strong>Assign only to last user retrieved</strong> – The task is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="3a3f6-171"><strong>Udeluk brugere med følgende betingelse</strong> – Opgaven tildeles ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-171"><strong>Exclude users with the following condition</strong> – The task isn't assigned to users in the range who meet a specific condition.</span></span> <span data-ttu-id="3a3f6-172">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a3f6-173">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="3a3f6-173">Workflow user</span></span></td>
    <td><span data-ttu-id="3a3f6-174">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="3a3f6-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="3a3f6-175">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a3f6-176">Bruger</span><span class="sxs-lookup"><span data-stu-id="3a3f6-176">User</span></span></td>
    <td><span data-ttu-id="3a3f6-177">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="3a3f6-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a3f6-178">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="3a3f6-179">Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-179">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="3a3f6-180">Vælg de brugere, der skal tildeles opgaven, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-180">Select the users to assign the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a3f6-181">Kø</span><span class="sxs-lookup"><span data-stu-id="3a3f6-181">Queue</span></span></td>
    <td><span data-ttu-id="3a3f6-182">En workflowopgavekø</span><span class="sxs-lookup"><span data-stu-id="3a3f6-182">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a3f6-183">Når du har valgt <strong>Kø</strong>, skal du klikke på fanen <strong>Købaseret</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-183">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="3a3f6-184">Udfør følgende trin for at tildele opgaven til en bestemt kø:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-184">To assign the task to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="3a3f6-185">På listen <strong>Køtype</strong> skal du vælge <strong>Workflowopgavekøer</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-185">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="3a3f6-186">Vælg køen på listen <strong>Kønavn</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-186">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="3a3f6-187">Hvis en bestemt betingelse skal være afgørende for, hvilken kø opgaven tildeles, skal du udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-187">If a specific condition should determine which queue the task is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="3a3f6-188">På listen <strong>Køtype</strong> skal du vælge <strong>Betingede workflowopgavekøer</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-188">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="3a3f6-189">På listen <strong>Kønavn</strong> skal du vælge <strong>Betinget kø</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-189">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="3a3f6-190">Denne indstilling bruges kun til nogle få arbejdsgange som f.eks. Sagsstyring.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-190">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="3a3f6-191">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at færdiggøre opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-191">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="3a3f6-192">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-192">Select one of the following options:</span></span>

    - <span data-ttu-id="3a3f6-193">**Timer** – Angiv det antal timer, brugeren har til at færdiggøre opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-193">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="3a3f6-194">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-194">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3a3f6-195">**Dage** – Angiv det antal dage, som brugeren har til at færdiggøre opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-195">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="3a3f6-196">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-196">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3a3f6-197">**Uger** – Angiv det antal uger, som brugeren har til at færdiggøre opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-197">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="3a3f6-198">**Måneder** – Vælg den dag og uge, hvor brugeren senest skal have færdiggjort opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-198">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="3a3f6-199">Det kan f.eks. være, at brugeren skal have færdiggjort opgaven senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-199">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="3a3f6-200">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have færdiggjort opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-200">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="3a3f6-201">Det kan f.eks. være, at brugeren skal have færdiggjort opgaven senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-201">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

    <span data-ttu-id="3a3f6-202">Hvis brugeren ikke færdiggør opgaven inden for den tildelte tid, er opgaven forsinket.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-202">If the user doesn't complete the task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="3a3f6-203">En opgave, der er forsinket, kan eskaleres ud fra de indstillinger, du vælger i området **Eskalering** på siden.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-203">A task that is overdue can be escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-the-task-is-overdue"></a><span data-ttu-id="3a3f6-204">Angive, hvad der sker, når opgaven er forfalden</span><span class="sxs-lookup"><span data-stu-id="3a3f6-204">Specify what happens when the task is overdue</span></span>

<span data-ttu-id="3a3f6-205">Hvis en bruger ikke færdiggør den manuelle opgave inden for den tildelte tid, er opgaven forsinket.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-205">If a user doesn't complete the manual task in the allotted time, the task is overdue.</span></span> <span data-ttu-id="3a3f6-206">En opgave, der er forfalden, kan eskaleres eller tildeles automatisk til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-206">A task that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="3a3f6-207">Udfør følgende trin for at eskalere opgaven, hvis den er forfalden.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-207">Follow these steps to escalate the task if it's overdue.</span></span>

1. <span data-ttu-id="3a3f6-208">Klik på **Eskalering** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-208">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="3a3f6-209">Markér afkrydsningsfeltet **Brug eskaleringssti** for at oprette en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-209">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="3a3f6-210">De brugere, der er angivet i eskaleringsstien, tildeles automatisk opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-210">The system automatically assigns the task to the users who are listed in the escalation path.</span></span> <span data-ttu-id="3a3f6-211">Følgende tabel repræsenterer f.eks. en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-211">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="3a3f6-212">Forløb</span><span class="sxs-lookup"><span data-stu-id="3a3f6-212">Sequence</span></span> | <span data-ttu-id="3a3f6-213">Eskaleringssti</span><span class="sxs-lookup"><span data-stu-id="3a3f6-213">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="3a3f6-214">1</span><span class="sxs-lookup"><span data-stu-id="3a3f6-214">1</span></span>        | <span data-ttu-id="3a3f6-215">Knyt til: Anna</span><span class="sxs-lookup"><span data-stu-id="3a3f6-215">Assign to: Donna</span></span>     |
    | <span data-ttu-id="3a3f6-216">2</span><span class="sxs-lookup"><span data-stu-id="3a3f6-216">2</span></span>        | <span data-ttu-id="3a3f6-217">Knyt til: Erik</span><span class="sxs-lookup"><span data-stu-id="3a3f6-217">Assign to: Erin</span></span>      |
    | <span data-ttu-id="3a3f6-218">3</span><span class="sxs-lookup"><span data-stu-id="3a3f6-218">3</span></span>        | <span data-ttu-id="3a3f6-219">Sluthandling: Afvis</span><span class="sxs-lookup"><span data-stu-id="3a3f6-219">Final action: Reject</span></span> |

    <span data-ttu-id="3a3f6-220">I dette eksempel tildeles den forfaldne opgave automatisk til Anna.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-220">In this example, the system assigns the overdue task to Donna.</span></span> <span data-ttu-id="3a3f6-221">Hvis Anna ikke færdiggør opgaven inden for den tildelte tid, tildeles opgaven automatisk til Erik.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-221">If Donna doesn't complete the task in the allotted time, the system assigns the task to Erin.</span></span> <span data-ttu-id="3a3f6-222">Hvis Erik ikke færdiggør opgaven inden for den tildelte tid, afvises det dokument, der blev sendt til behandling, af systemet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-222">If Erin doesn't complete the task in the allotted time, the system rejects the document that was submitted for processing.</span></span>

3. <span data-ttu-id="3a3f6-223">Klik på **Tilføj eskalering** for at føje en bruger til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-223">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="3a3f6-224">Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og følg derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 4.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-224">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3a3f6-225">Indstilling</span><span class="sxs-lookup"><span data-stu-id="3a3f6-225">Option</span></span></th>
    <th><span data-ttu-id="3a3f6-226">Brugere, som opgaven eskaleres til</span><span class="sxs-lookup"><span data-stu-id="3a3f6-226">Users that the task is escalated to</span></span></th>
    <th><span data-ttu-id="3a3f6-227">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="3a3f6-227">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3a3f6-228">Hierarki</span><span class="sxs-lookup"><span data-stu-id="3a3f6-228">Hierarchy</span></span></td>
    <td><span data-ttu-id="3a3f6-229">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="3a3f6-229">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a3f6-230">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil eskalere opgaven til.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-230">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the task to.</span></span></li>
    <li><span data-ttu-id="3a3f6-231">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-231">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="3a3f6-232">Disse navne repræsenterer de brugere, som opgaven kan eskaleres til.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-232">These names represent users that the task can be escalated to.</span></span> <span data-ttu-id="3a3f6-233">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-233">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="3a3f6-234">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-234">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="3a3f6-235">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-235">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="3a3f6-236">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-236">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="3a3f6-237">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet opgaven skal eskaleres til:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-237">On the <strong>Hierarchy options</strong> tab, specify which users in the range the task should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="3a3f6-238"><strong>Tildel til alle hentede brugere</strong> – Opgaven eskaleres til alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-238"><strong>Assign to all users retrieved</strong> – The task is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="3a3f6-239"><strong>Tildel kun til den sidst hentede bruger</strong> – Opgaven eskaleres kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-239"><strong>Assign only to last user retrieved</strong> – The task is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="3a3f6-240"><strong>Udeluk brugere med følgende betingelse</strong> – Opgaven eskaleres ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-240"><strong>Exclude users with the following condition</strong> – This task isn't escalated to users in the range who meet a specific condition.</span></span> <span data-ttu-id="3a3f6-241">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-241">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a3f6-242">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="3a3f6-242">Workflow user</span></span></td>
    <td><span data-ttu-id="3a3f6-243">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="3a3f6-243">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="3a3f6-244">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-244">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a3f6-245">Bruger</span><span class="sxs-lookup"><span data-stu-id="3a3f6-245">User</span></span></td>
    <td><span data-ttu-id="3a3f6-246">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="3a3f6-246">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a3f6-247">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-247">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="3a3f6-248">Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-248">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="3a3f6-249">Vælg de brugere, som opgaven skal eskaleres til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-249">Select the users to escalate the task to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="3a3f6-250">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at færdiggøre opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-250">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to complete the task.</span></span> <span data-ttu-id="3a3f6-251">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-251">Select one of the following options:</span></span>

    - <span data-ttu-id="3a3f6-252">**Timer** – Angiv det antal timer, brugeren har til at færdiggøre opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-252">**Hours** – Enter the number of hours that the user has to complete the task.</span></span> <span data-ttu-id="3a3f6-253">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-253">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3a3f6-254">**Dage** – Angiv det antal dage, som brugeren har til at færdiggøre opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-254">**Days** – Enter the number of days that the user has to complete the task.</span></span> <span data-ttu-id="3a3f6-255">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-255">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3a3f6-256">**Uger** – Angiv det antal uger, som brugeren har til at færdiggøre opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-256">**Weeks** – Enter the number of weeks that the user has to complete the task.</span></span>
    - <span data-ttu-id="3a3f6-257">**Måneder** – Vælg den dag og uge, hvor brugeren senest skal have færdiggjort opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-257">**Months** – Select the day and week that the user must complete the task by.</span></span> <span data-ttu-id="3a3f6-258">Det kan f.eks. være, at brugeren skal have færdiggjort opgaven senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-258">For example, you might want the user to complete the task by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="3a3f6-259">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have færdiggjort opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-259">**Years** – Select the day, week, and month that the user must complete the task by.</span></span> <span data-ttu-id="3a3f6-260">Det kan f.eks. være, at brugeren skal have færdiggjort opgaven senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-260">For example, you might want the user to complete the task by Friday of the third week of December.</span></span>

5. <span data-ttu-id="3a3f6-261">Gentag trin 3 til 4 for hvert bruger, der skal føjes til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-261">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="3a3f6-262">Du kan ændre brugernes rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-262">You can change the order of the users.</span></span>
6. <span data-ttu-id="3a3f6-263">Hvis brugerne i eskaleringsstien ikke færdiggør opgaven inden for den tildelte tid, håndteres opgaven af systemet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-263">If the users in the escalation path don't complete the task in the allotted time, the system takes action on the task.</span></span> <span data-ttu-id="3a3f6-264">Hvis du vil angive den handling, som systemet skal udføre, skal du vælge rækken **Handling** og derefter vælge en handling på fanen **Sluthandling**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-264">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>

## <a name="specify-when-the-system-automatically-acts-on-the-task"></a><span data-ttu-id="3a3f6-265">Angive, hvornår systemet automatisk skal behandle opgaven</span><span class="sxs-lookup"><span data-stu-id="3a3f6-265">Specify when the system automatically acts on the task</span></span>

<span data-ttu-id="3a3f6-266">Du kan konfigurere systemet, så en manuel opgave håndteres, hvis bestemte betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-266">You can configure the system to take action on the manual task if specific conditions are met.</span></span> <span data-ttu-id="3a3f6-267">En opgave kræver f.eks., at et medlem af udgiftsrapportafdelingen gennemgår de kvitteringer, der fremlægges sammen med en udgiftsrapport.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-267">For example, a task requires that a member of the Expense reports department review the receipts that are submitted together with an expense report.</span></span> <span data-ttu-id="3a3f6-268">Ifølge firmaets politik skal denne opgave udføres, hvis det samlede beløb i udgiftsrapporten overstiger USD 100.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-268">According to company policy, this task must be performed if the total amount of the expense report is more than USD 100.</span></span> <span data-ttu-id="3a3f6-269">I dette scenarie kan du konfigurere systemet, så opgaven automatisk markeres som **Fuldført**, når det samlede beløb er mindre end 100.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-269">In this scenario, you can configure the system to automatically mark the task as **Complete** when the total amount is less than 100.</span></span> <span data-ttu-id="3a3f6-270">Udfør disse trin for at angive, hvornår systemet skal håndtere den manuelle opgave.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-270">Follow these steps to specify when the system takes action on the manual task.</span></span>

1. <span data-ttu-id="3a3f6-271">Klik på **Automatiske handlinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-271">In the left pane, click **Automatic actions**.</span></span>
2. <span data-ttu-id="3a3f6-272">Marker afkrydsningsfeltet **Aktivér automatiske handlinger**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-272">Select the **Enable automatic actions** check box.</span></span>
3. <span data-ttu-id="3a3f6-273">Klik på **Tilføj betingelse**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-273">Click **Add condition**.</span></span>
4. <span data-ttu-id="3a3f6-274">Angiv en betingelse.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-274">Enter a condition.</span></span>
5. <span data-ttu-id="3a3f6-275">Angiv eventuelle supplerende betingelser, hvis det er påkrævede.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-275">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="3a3f6-276">Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-276">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="3a3f6-277">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-277">Click **Test**.</span></span>
    2. <span data-ttu-id="3a3f6-278">På siden **Test betingelse for arbejdsgang** i området **Valider betingelse**, og vælg en post.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-278">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="3a3f6-279">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-279">Click **Test**.</span></span> <span data-ttu-id="3a3f6-280">Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-280">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="3a3f6-281">Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-281">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

7. <span data-ttu-id="3a3f6-282">Vælg den handling, som systemet skal udføre på opgaven, på listen **Handling til automatisk udførelse**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-282">In the **Auto complete action** list, select the action that the system should take on the task.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="3a3f6-283">Angive, hvornår beskeder sendes</span><span class="sxs-lookup"><span data-stu-id="3a3f6-283">Specify when notifications are sent</span></span>

<span data-ttu-id="3a3f6-284">Du kan sende beskeder til personer, når en manuel opgave er delegeret videre, eskaleret, fuldført eller afvist, eller når der er anmodet om en ændring.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-284">You can send notifications to people when a manual task has been delegated, escalated, completed, or rejected, or when a change has been requested.</span></span> <span data-ttu-id="3a3f6-285">Udfør følgende trin for at angive, hvornår der sendes beskeder, og hvem beskederne sendes til.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-285">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="3a3f6-286">Klik på **Beskeder** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-286">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="3a3f6-287">Markér afkrydsningsfeltet ud for de hændelser, som beskederne udsendes i forbindelse med.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-287">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="3a3f6-288">**Deleger** – Opgaven er tildelt en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-288">**Delegate** – The task has been assigned to another user.</span></span>
    - <span data-ttu-id="3a3f6-289">**Eskaler** – Den bruger, der har fået opgaven tildelt, har ikke fuldført den inden for den tildelte tid.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-289">**Escalate** – The assigned user hasn't completed the task in the allotted time.</span></span>
    - <span data-ttu-id="3a3f6-290">**Fuldført** – Den bruger, der har fået opgaven tildelt, har fuldført den.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-290">**Complete** – The assigned user has completed the task.</span></span>
    - <span data-ttu-id="3a3f6-291">**Afvis** – Den bruger, der har fået opgaven tildelt, har afvist det fremsendte dokument.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-291">**Reject** – The assigned user has rejected the document that was submitted.</span></span>
    - <span data-ttu-id="3a3f6-292">**Anmod om ændring** – Den bruger, der har fået opgaven tildelt, har anmodet om en ændring i det fremsendte dokument.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-292">**Request change** – The assigned user has requested a change to the document that was submitted.</span></span>

3. <span data-ttu-id="3a3f6-293">Vælg rækken for den hændelse, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-293">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="3a3f6-294">Indtast teksten til beskeden i tekstfeltet på fanen **Beskedtekst**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-294">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="3a3f6-295">Hvis du vil personalisere beskeden, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-295">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="3a3f6-296">Pladsholderne erstattes med de relevante oplysninger, når beskeden vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-296">Placeholders are replaced with appropriate information when the notification is shown to users.</span></span> <span data-ttu-id="3a3f6-297">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-297">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="3a3f6-298">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-298">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="3a3f6-299">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-299">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="3a3f6-300">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-300">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="3a3f6-301">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-301">Click **Insert**.</span></span>

6. <span data-ttu-id="3a3f6-302">Følg disse trin for at tilføje oversættelser af beskeden:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-302">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="3a3f6-303">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-303">Click **Translations**.</span></span>
    2. <span data-ttu-id="3a3f6-304">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-304">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="3a3f6-305">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-305">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="3a3f6-306">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-306">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="3a3f6-307">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 5.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-307">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="3a3f6-308">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-308">Click **Close**.</span></span>

7. <span data-ttu-id="3a3f6-309">På fanen **Modtager** skal du angive, hvem beskederne skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-309">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="3a3f6-310">Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 8.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-310">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="3a3f6-311">Indstilling</span><span class="sxs-lookup"><span data-stu-id="3a3f6-311">Option</span></span></th>
    <th><span data-ttu-id="3a3f6-312">Modtagere af besked</span><span class="sxs-lookup"><span data-stu-id="3a3f6-312">Notification recipients</span></span></th>
    <th><span data-ttu-id="3a3f6-313">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="3a3f6-313">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="3a3f6-314">Deltager</span><span class="sxs-lookup"><span data-stu-id="3a3f6-314">Participant</span></span></td>
    <td><span data-ttu-id="3a3f6-315">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="3a3f6-315">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a3f6-316">Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-316">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="3a3f6-317">Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-317">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a3f6-318">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="3a3f6-318">Workflow user</span></span></td>
    <td><span data-ttu-id="3a3f6-319">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="3a3f6-319">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="3a3f6-320">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-320">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="3a3f6-321">Bruger</span><span class="sxs-lookup"><span data-stu-id="3a3f6-321">User</span></span></td>
    <td><span data-ttu-id="3a3f6-322">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="3a3f6-322">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="3a3f6-323">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-323">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="3a3f6-324">Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-324">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="3a3f6-325">Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-325">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="3a3f6-326">Gentag trin 3 til 7 for hver af de hændelser, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-326">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="3a3f6-327">Angive en tidsgrænse</span><span class="sxs-lookup"><span data-stu-id="3a3f6-327">Set a time limit</span></span>

<span data-ttu-id="3a3f6-328">Udfør følgende trin, hvis den manuelle opgave skal fuldføres inden en bestemt tidsgrænse.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-328">Follow these steps if the manual task must be completed in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="3a3f6-329">De indstillinger, du vælger i denne procedure, overskriver de indstillinger, du har valgt i områderne **Tildeling** og **Eskalering** på siden.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="3a3f6-330">Klik på **Avancerede indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="3a3f6-331">Markér afkrydsningsfeltet **Angiv en tidsgrænse for arbejdsgangselementet**</span><span class="sxs-lookup"><span data-stu-id="3a3f6-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="3a3f6-332">Angiv, hvornår opgaven skal være fuldført, i feltet **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-332">In the **Duration** field, specify when the task must be completed.</span></span> <span data-ttu-id="3a3f6-333">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="3a3f6-333">Select one of the following options:</span></span>

    - <span data-ttu-id="3a3f6-334">**Timer** – Angiv det antal timer, som opgaven skal fuldføres på.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-334">**Hours** – Enter the number of hours that the task must be completed in.</span></span> <span data-ttu-id="3a3f6-335">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3a3f6-336">**Dage** – Angiv det antal dage, som opgaven skal fuldføres på.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-336">**Days** – Enter the number of days that the task must be completed in.</span></span> <span data-ttu-id="3a3f6-337">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="3a3f6-338">**Uger** – Angiv det antal uger, inden for hvilke opgaven skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-338">**Weeks** – Enter the number of weeks that the task must be completed in.</span></span>
    - <span data-ttu-id="3a3f6-339">**Måneder** – Vælg den dag og uge, hvor opgaven senest skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-339">**Months** – Select the day and week that the task must be completed by.</span></span> <span data-ttu-id="3a3f6-340">Det kan f.eks. være, at opgaven skal være fuldført f.eks. senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-340">For example, you might want the task to be completed by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="3a3f6-341">**År** – Vælg den dag, uge og måned, hvor opgaven senest skal være fuldført.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-341">**Years** – Select the day, week, and month that the task must be completed by.</span></span> <span data-ttu-id="3a3f6-342">Det kan f.eks. være, at opgaven skal være fuldført senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-342">For example, you might want the task to be completed by Friday of the third week of December.</span></span>

4. <span data-ttu-id="3a3f6-343">Hvis tidsfristen overskrides, håndteres opgaven af systemet.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-343">If the time limit is exceeded, the system takes action on the task.</span></span> <span data-ttu-id="3a3f6-344">Vælg den handling, der skal udføres, på listen **Handling**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-344">In the **Action** list, select the action that the system should take.</span></span>

## <a name="specify-which-actions-are-available-to-the-user"></a><span data-ttu-id="3a3f6-345">Angiv, hvilke handlinger der er tilgængelige for brugeren</span><span class="sxs-lookup"><span data-stu-id="3a3f6-345">Specify which actions are available to the user</span></span>

<span data-ttu-id="3a3f6-346">Når den manuelle opgave tildeles en bruger, skal vedkommende håndtere opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-346">When the manual task is assigned to a user, the user must take action on the task.</span></span> <span data-ttu-id="3a3f6-347">Udfør disse trin for at angive, hvilke handlinger brugeren kan udføre på opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-347">Follow these steps to specify which actions the user can take on the task.</span></span>

> [!NOTE]
> <span data-ttu-id="3a3f6-348">Det vil variere, hvilke handlinger der er tilgængelige, afhængigt af opgavens design.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-348">The actions that are available vary, depending on the design of the task.</span></span>

1. <span data-ttu-id="3a3f6-349">Klik på **Avancerede indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-349">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="3a3f6-350">Markér afkrydsningsfeltet **Fuldført**, hvis brugeren skal kunne markere opgaven som **Fuldført**.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-350">Select the **Complete** check box if the user should be able to mark the task as **Complete**.</span></span>
3. <span data-ttu-id="3a3f6-351">Markér afkrydsningsfeltet **Afvis**, hvis brugeren skal kunne afvise det dokument, der blev fremsendt.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-351">Select the **Reject** check box if the user should be able to reject the document that was submitted.</span></span>
4. <span data-ttu-id="3a3f6-352">Markér afkrydsningsfeltet **Anmod om ændring**, hvis brugeren skal kunne anmode om ændringer i det fremsendte dokument.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-352">Select the **Request change** check box if the user should be able to request changes to the document that was submitted.</span></span>
5. <span data-ttu-id="3a3f6-353">Markér afkrydsningsfeltet **Deleger**, hvis brugeren skal kunne tildele denne opgave til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-353">Select the **Delegate** check box if the user should be able to assign the task to another user.</span></span>
6. <span data-ttu-id="3a3f6-354">Markér afkrydsningsfeltet **Tildel igen**, hvis brugeren skal kunne tildele denne opgave til en anden bruger i workflowopgavekøen.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-354">Select the **Reassign** check box if the user should be able to reassign the task to another user in the work item queue.</span></span>
7. <span data-ttu-id="3a3f6-355">Markér afkrydsningsfeltet **Frigiv**, hvis brugeren skal kunne tildele denne opgave til workflowopgavekøen.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-355">Select the **Release** check box if the user should be able to reassign the task to the work item queue.</span></span> <span data-ttu-id="3a3f6-356">Derefter kan en anden bruger fuldføre opgaven.</span><span class="sxs-lookup"><span data-stu-id="3a3f6-356">Another user can then complete the task.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]