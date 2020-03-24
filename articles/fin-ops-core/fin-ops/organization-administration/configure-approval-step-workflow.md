---
title: Konfigurere godkendelsestrin i en arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer egenskaberne for et godkendelsestrin.
author: sericks007
manager: AnnBe
ms.date: 08/23/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192161
ms.assetid: 8b478e3d-d6b4-403b-aae0-f639a71ca36c
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: c5bd5300a061e12ccabdea83c20863c95e15fe19
ms.sourcegitcommit: 1d5a4f70a931e78b06811add97c1962e8d93689b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/13/2020
ms.locfileid: "3124675"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="38e1e-103">Konfigurere godkendelsestrin i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="38e1e-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="38e1e-104">I dette emne forklares det, hvordan du konfigurerer egenskaberne for et godkendelsestrin.</span><span class="sxs-lookup"><span data-stu-id="38e1e-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="38e1e-105">Hvis du vil konfigurere et godkendelsestrin i arbejdsgangseditoren, skal du højreklikke på godkendelsestrinnet og derefter klikke på **Egenskaber** for at åbne siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="38e1e-106">Brug derefter nedenstående procedurer til at konfigurere egenskaberne for godkendelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="38e1e-107">Angive et navn på trinnet</span><span class="sxs-lookup"><span data-stu-id="38e1e-107">Name the step</span></span>
<span data-ttu-id="38e1e-108">Udfør følgende trin for at angive et navn på godkendelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="38e1e-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="38e1e-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="38e1e-110">Angiv et entydigt navn til godkendelsestrinnet i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="38e1e-111">Angive en emnelinje og instruktioner</span><span class="sxs-lookup"><span data-stu-id="38e1e-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="38e1e-112">Du skal angive en emnelinje og instruktioner til brugere, som har fået godkendelsestrinnet tildelt.</span><span class="sxs-lookup"><span data-stu-id="38e1e-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="38e1e-113">Hvis du f.eks. konfigurerer et godkendelsestrin for indkøbsrekvisitioner, kan den bruger, der har fået trinnet tildelt, se emnelinjen og instruktionerne på siden **Indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="38e1e-114">Emnelinjen vises i en meddelelseslinje på siden.</span><span class="sxs-lookup"><span data-stu-id="38e1e-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="38e1e-115">Brugeren kan derefter klikke på ikonet på meddelelseslinjen for at få vist instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="38e1e-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="38e1e-116">Udfør følgende trin for at angive en emnelinje og instruktioner.</span><span class="sxs-lookup"><span data-stu-id="38e1e-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="38e1e-117">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="38e1e-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="38e1e-118">I feltet **Emne for workflowopgave** skal du indtaste emnelinjen.</span><span class="sxs-lookup"><span data-stu-id="38e1e-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="38e1e-119">Hvis du vil personalisere emnelinjen, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="38e1e-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="38e1e-120">Pladsholderne erstattes med de relevante data, når emnelinjen vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="38e1e-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="38e1e-121">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="38e1e-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="38e1e-122">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="38e1e-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="38e1e-123">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="38e1e-124">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="38e1e-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="38e1e-125">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-125">Click **Insert**.</span></span>

4. <span data-ttu-id="38e1e-126">Følg disse trin for at tilføje oversættelser af emnelinjen:</span><span class="sxs-lookup"><span data-stu-id="38e1e-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="38e1e-127">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="38e1e-128">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="38e1e-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="38e1e-129">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="38e1e-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="38e1e-130">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="38e1e-131">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 3.</span><span class="sxs-lookup"><span data-stu-id="38e1e-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="38e1e-132">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-132">Click **Close**.</span></span>

5. <span data-ttu-id="38e1e-133">I feltet **Emne for workflowopgave** skal du indtaste instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="38e1e-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="38e1e-134">Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="38e1e-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="38e1e-135">Pladsholderne erstattes med de relevante data, når instruktionerne vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="38e1e-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="38e1e-136">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="38e1e-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="38e1e-137">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="38e1e-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="38e1e-138">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="38e1e-139">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="38e1e-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="38e1e-140">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-140">Click **Insert**.</span></span>

7. <span data-ttu-id="38e1e-141">Følg disse trin for at tilføje oversættelser af instruktionerne:</span><span class="sxs-lookup"><span data-stu-id="38e1e-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="38e1e-142">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="38e1e-143">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="38e1e-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="38e1e-144">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="38e1e-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="38e1e-145">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="38e1e-146">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 6.</span><span class="sxs-lookup"><span data-stu-id="38e1e-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="38e1e-147">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="38e1e-148">Tildele godkendelsestrinnet</span><span class="sxs-lookup"><span data-stu-id="38e1e-148">Assign the approval step</span></span>

<span data-ttu-id="38e1e-149">Udfør følgende trin for at angive, hvem godkendelsestrinnet skal tildeles.</span><span class="sxs-lookup"><span data-stu-id="38e1e-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="38e1e-150">Klik på **Tildeling** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="38e1e-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="38e1e-151">Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 3.</span><span class="sxs-lookup"><span data-stu-id="38e1e-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="38e1e-152">Indstilling</span><span class="sxs-lookup"><span data-stu-id="38e1e-152">Option</span></span></th>
    <th><span data-ttu-id="38e1e-153">Brugere, som godkendelsestrinnet er tildelt til</span><span class="sxs-lookup"><span data-stu-id="38e1e-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="38e1e-154">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="38e1e-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="38e1e-155">Deltager</span><span class="sxs-lookup"><span data-stu-id="38e1e-155">Participant</span></span></td>
    <td><span data-ttu-id="38e1e-156">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="38e1e-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38e1e-157">Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil tildele trinnet til.</span><span class="sxs-lookup"><span data-stu-id="38e1e-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="38e1e-158">Vælg den gruppe eller rolle, som trinnet skal tildeles til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="38e1e-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38e1e-159">Hierarki</span><span class="sxs-lookup"><span data-stu-id="38e1e-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="38e1e-160">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="38e1e-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38e1e-161">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil tildele trinnet til.</span><span class="sxs-lookup"><span data-stu-id="38e1e-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="38e1e-162">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="38e1e-163">Disse navne repræsenterer de brugere, som trinnet kan tildeles til.</span><span class="sxs-lookup"><span data-stu-id="38e1e-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="38e1e-164">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="38e1e-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="38e1e-165">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="38e1e-166">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="38e1e-167">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="38e1e-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="38e1e-168">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet trinnet skal tildeles:</span><span class="sxs-lookup"><span data-stu-id="38e1e-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="38e1e-169"><strong>Tildel til alle hentede brugere</strong> – Trinnet tildeles alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="38e1e-170"><strong>Tildel kun til den sidst hentede bruger</strong> – Trinnet tildeles kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="38e1e-171"><strong>Udeluk brugere med følgende betingelse</strong> – Trinnet tildeles ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="38e1e-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="38e1e-172">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="38e1e-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38e1e-173">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="38e1e-173">Workflow user</span></span></td>
    <td><span data-ttu-id="38e1e-174">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="38e1e-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="38e1e-175">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="38e1e-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38e1e-176">Bruger</span><span class="sxs-lookup"><span data-stu-id="38e1e-176">User</span></span></td>
    <td><span data-ttu-id="38e1e-177">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="38e1e-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38e1e-178">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="38e1e-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="38e1e-179">Listen <strong>Tilgængelige brugere</strong> indeholder alle systembrugere.</span><span class="sxs-lookup"><span data-stu-id="38e1e-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="38e1e-180">Vælg de brugere, der skal tildeles trinnet, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="38e1e-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="38e1e-181">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at håndtere eller reagere på dokumenter, der når til godkendelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="38e1e-182">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="38e1e-182">Select one of the following options:</span></span>

    - <span data-ttu-id="38e1e-183">**Timer** – Angiv det antal timer, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="38e1e-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="38e1e-184">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="38e1e-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="38e1e-185">**Dage** – Angiv det antal dage, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="38e1e-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="38e1e-186">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="38e1e-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="38e1e-187">**Uger** – Angiv det antal uger, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="38e1e-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="38e1e-188">**Måneder** – Vælg den dag eller uge, hvor brugeren senest skal have reageret.</span><span class="sxs-lookup"><span data-stu-id="38e1e-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="38e1e-189">Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="38e1e-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="38e1e-190">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have reageret.</span><span class="sxs-lookup"><span data-stu-id="38e1e-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="38e1e-191">Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="38e1e-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="38e1e-192">Hvis brugeren ikke håndterer dokumentet inden for den tildelte tid, er dokumentet forsinket.</span><span class="sxs-lookup"><span data-stu-id="38e1e-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="38e1e-193">Et forsinket dokument eskaleres ud fra de indstillinger, du vælger i området **Eskalering** på siden.</span><span class="sxs-lookup"><span data-stu-id="38e1e-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="38e1e-194">Hvis du har tildelt godkendelsestrinnet til flere brugere eller en gruppe af brugere, skal du vælge følgende indstillinger på fanen **Afviklingspolitik**:</span><span class="sxs-lookup"><span data-stu-id="38e1e-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="38e1e-195">**Enkelt godkender** – den handling, der udføres på dokumentet, bestemmes af den første person, der reagerer.</span><span class="sxs-lookup"><span data-stu-id="38e1e-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="38e1e-196">Antag f.eks. at Søren har sendt en udgiftsrapport på kr. 15.000.</span><span class="sxs-lookup"><span data-stu-id="38e1e-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="38e1e-197">Dokumentet er aktuelt tildelt Mette, Karina og Bjarne.</span><span class="sxs-lookup"><span data-stu-id="38e1e-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="38e1e-198">Hvis Mette er den første person, der reagerer på dokumentet, vil den handling, hun udfører, blive anvendt på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="38e1e-199">Hvis Mette afviser dokumentet, afvises det og sendes tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="38e1e-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="38e1e-200">Hvis Mette godkender dokumentet, sendes det til Dorthe til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="38e1e-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Arbejdsgang, der har en godkendelsesproces](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="38e1e-202">**Flertal af godkendere** – den handling, der skal anvendes på dokumentet, bliver bestemt, når de fleste af godkenderne har reageret.</span><span class="sxs-lookup"><span data-stu-id="38e1e-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="38e1e-203">Antag f.eks. at Søren har sendt en udgiftsrapport på kr. 15.000.</span><span class="sxs-lookup"><span data-stu-id="38e1e-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="38e1e-204">Dokumentet er aktuelt tildelt Mette, Karina og Bjarne.</span><span class="sxs-lookup"><span data-stu-id="38e1e-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="38e1e-205">Hvis Mette og Karina er de første personer, der reagerer på dokumentet, vil den handling, de udfører, blive anvendt på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="38e1e-206">Hvis Mette godkender dokumentet, men Karina afviser det, vil dokumentet blive afvist og sendt tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="38e1e-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="38e1e-207">Hvis både Mette og Karina godkender dokumentet, vil det blive sendt til Dorthe til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="38e1e-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="38e1e-208">**Procent af godkendere** – den handling, der anvendes på dokumentet, bliver bestemt, når en bestemt procentdel af godkenderne svarer.</span><span class="sxs-lookup"><span data-stu-id="38e1e-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="38e1e-209">Antag f.eks. at Søren har sendt en udgiftsrapport på kr. 15.000.</span><span class="sxs-lookup"><span data-stu-id="38e1e-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="38e1e-210">Udgiftsrapporten er aktuelt tildelt Mette, Karina og Bjarne, og du har angivet procentdelen til **50**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="38e1e-211">Hvis Mette og Karina er de første to godkendere, der reagerer, vil den handling, de udfører, blive anvendt på dokumentet, fordi de opfylder kravet om at være 50 procent af godkendere.</span><span class="sxs-lookup"><span data-stu-id="38e1e-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="38e1e-212">Hvis Mette godkender dokumentet, men Karina afviser det, vil dokumentet blive afvist og sendt tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="38e1e-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="38e1e-213">Hvis både Mette og Karina godkender dokumentet, vil det blive sendt til Dorthe til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="38e1e-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="38e1e-214">**Alle godkendere** – alle godkendere skal godkende dokumentet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="38e1e-215">Ellers kan arbejdsgangen ikke fortsætte.</span><span class="sxs-lookup"><span data-stu-id="38e1e-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="38e1e-216">Antag f.eks. at Søren har sendt en udgiftsrapport på 15.000 kr.</span><span class="sxs-lookup"><span data-stu-id="38e1e-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="38e1e-217">Dokumentet er aktuelt tildelt Mette, Karina og Bjarne.</span><span class="sxs-lookup"><span data-stu-id="38e1e-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="38e1e-218">Hvis Mette og Karina godkender dokumentet, men Bjarne afviser det, vil dokumentet blive afvist og sendt tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="38e1e-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="38e1e-219">Hvis Mette, Karina og Bjarne godkender dokumentet, bliver det sendt til Dorthe til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="38e1e-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="38e1e-220">Angive, hvornår godkendelsestrinnet skal bruges</span><span class="sxs-lookup"><span data-stu-id="38e1e-220">Specify when the approval step is required</span></span>

<span data-ttu-id="38e1e-221">Du kan angive, hvornår godkendelsestrinnet er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="38e1e-222">Godkendelsestrinnet kan være påkrævet altid, eller det kan kun være påkrævet, hvis bestemte betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="38e1e-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="38e1e-223">Godkendelsestrinnet er altid påkrævet</span><span class="sxs-lookup"><span data-stu-id="38e1e-223">The approval step is always required</span></span>

<span data-ttu-id="38e1e-224">Udfør følgende trin, hvis godkendelsestrinnet altid er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="38e1e-225">Klik på **Betingelse** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="38e1e-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="38e1e-226">Vælg indstillingen **Udfør altid dette trin**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="38e1e-227">Godkendelsestrinnet er påkrævet under bestemte betingelser.</span><span class="sxs-lookup"><span data-stu-id="38e1e-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="38e1e-228">Det godkendelsestrin, du er ved at konfigurere, er måske kun påkrævet, hvis bestemte betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="38e1e-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="38e1e-229">Hvis du f.eks. er ved at konfigurere et godkendelsestrin til en arbejdsgang for en indkøbsrekvisition, vil du måske have, at godkendelsestrinnet kun skal bruges, hvis indkøbsrekvisitionsbeløbet er større end 10.000 kr.</span><span class="sxs-lookup"><span data-stu-id="38e1e-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="38e1e-230">Udfør følgende trin, når du skal angive, at godkendelsestrinnet er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="38e1e-231">Klik på **Betingelse** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="38e1e-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="38e1e-232">Vælg indstillingen **Kør kun dette trin, når følgende betingelse er opfyldt**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="38e1e-233">Angiv en betingelse.</span><span class="sxs-lookup"><span data-stu-id="38e1e-233">Enter a condition.</span></span>
4. <span data-ttu-id="38e1e-234">Angiv eventuelle supplerende betingelser, hvis det er påkrævede.</span><span class="sxs-lookup"><span data-stu-id="38e1e-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="38e1e-235">Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="38e1e-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="38e1e-236">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-236">Click **Test**.</span></span>
    2. <span data-ttu-id="38e1e-237">På siden **Test betingelse for arbejdsgang** i området **Valider betingelse**, og vælg en post.</span><span class="sxs-lookup"><span data-stu-id="38e1e-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="38e1e-238">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-238">Click **Test**.</span></span> <span data-ttu-id="38e1e-239">Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.</span><span class="sxs-lookup"><span data-stu-id="38e1e-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="38e1e-240">Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="38e1e-241">Angive, hvad der sker, når dokumentet er forfaldent</span><span class="sxs-lookup"><span data-stu-id="38e1e-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="38e1e-242">Hvis en bruger ikke håndterer et dokument inden for den tildelte tid, er dokumentet forfaldent.</span><span class="sxs-lookup"><span data-stu-id="38e1e-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="38e1e-243">Et forfaldent dokument kan eskaleres eller tildeles automatisk til en anden bruger til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="38e1e-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="38e1e-244">Følg disse trin for at eskalere dokumentet, hvis det er forfaldent.</span><span class="sxs-lookup"><span data-stu-id="38e1e-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="38e1e-245">Klik på **Eskalering** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="38e1e-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="38e1e-246">Markér afkrydsningsfeltet **Brug eskaleringssti** for at oprette en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="38e1e-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="38e1e-247">De brugere, der er angivet i eskaleringsstien, tildeles automatisk dokumentet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="38e1e-248">Følgende tabel repræsenterer f.eks. en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="38e1e-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="38e1e-249">Forløb</span><span class="sxs-lookup"><span data-stu-id="38e1e-249">Sequence</span></span> | <span data-ttu-id="38e1e-250">Eskaleringssti</span><span class="sxs-lookup"><span data-stu-id="38e1e-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="38e1e-251">1</span><span class="sxs-lookup"><span data-stu-id="38e1e-251">1</span></span>        | <span data-ttu-id="38e1e-252">Knyt til: Anna</span><span class="sxs-lookup"><span data-stu-id="38e1e-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="38e1e-253">2</span><span class="sxs-lookup"><span data-stu-id="38e1e-253">2</span></span>        | <span data-ttu-id="38e1e-254">Knyt til: Erik</span><span class="sxs-lookup"><span data-stu-id="38e1e-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="38e1e-255">3</span><span class="sxs-lookup"><span data-stu-id="38e1e-255">3</span></span>        | <span data-ttu-id="38e1e-256">Sluthandling: Afvis</span><span class="sxs-lookup"><span data-stu-id="38e1e-256">Final action: Reject</span></span> |

    <span data-ttu-id="38e1e-257">I dette eksempel tildeles det forfaldne dokument automatisk til Anna.</span><span class="sxs-lookup"><span data-stu-id="38e1e-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="38e1e-258">Hvis Anna ikke reagerer inden for den tildelte tid, tildeles dokumentet automatisk til Erik.</span><span class="sxs-lookup"><span data-stu-id="38e1e-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="38e1e-259">Hvis Erik ikke reagerer inden for den tildelte tid, afvises dokumentet automatisk.</span><span class="sxs-lookup"><span data-stu-id="38e1e-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="38e1e-260">Klik på **Tilføj eskalering** for at føje en bruger til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="38e1e-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="38e1e-261">Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og følg derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 4.</span><span class="sxs-lookup"><span data-stu-id="38e1e-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="38e1e-262">Indstilling</span><span class="sxs-lookup"><span data-stu-id="38e1e-262">Option</span></span></th>
    <th><span data-ttu-id="38e1e-263">Brugere, som dokumentet eskaleres til</span><span class="sxs-lookup"><span data-stu-id="38e1e-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="38e1e-264">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="38e1e-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="38e1e-265">Hierarki</span><span class="sxs-lookup"><span data-stu-id="38e1e-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="38e1e-266">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="38e1e-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38e1e-267">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil eskalere dokumentet til.</span><span class="sxs-lookup"><span data-stu-id="38e1e-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="38e1e-268">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="38e1e-269">Disse navne repræsenterer de brugere, som dokumentet kan eskaleres til.</span><span class="sxs-lookup"><span data-stu-id="38e1e-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="38e1e-270">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="38e1e-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="38e1e-271">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="38e1e-272">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="38e1e-273">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="38e1e-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="38e1e-274">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet dokumentet skal eskaleres til:</span><span class="sxs-lookup"><span data-stu-id="38e1e-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="38e1e-275"><strong>Tildel til alle hentede brugere</strong> – Dokumentet eskaleres til alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="38e1e-276"><strong>Tildel kun til den sidst hentede bruger</strong> – Dokumentet eskaleres kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="38e1e-277"><strong>Udeluk brugere med følgende betingelse</strong> – Dokumentet eskaleres ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="38e1e-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="38e1e-278">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="38e1e-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38e1e-279">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="38e1e-279">Workflow user</span></span></td>
    <td><span data-ttu-id="38e1e-280">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="38e1e-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="38e1e-281">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="38e1e-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="38e1e-282">Bruger</span><span class="sxs-lookup"><span data-stu-id="38e1e-282">User</span></span></td>
    <td><span data-ttu-id="38e1e-283">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="38e1e-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="38e1e-284">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="38e1e-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="38e1e-285">Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere.</span><span class="sxs-lookup"><span data-stu-id="38e1e-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="38e1e-286">Vælg de brugere, dokumentet skal eskaleres til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="38e1e-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="38e1e-287">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at håndtere eller reagere på dokumenter.</span><span class="sxs-lookup"><span data-stu-id="38e1e-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="38e1e-288">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="38e1e-288">Select one of the following options:</span></span>

    - <span data-ttu-id="38e1e-289">**Timer** – Angiv det antal timer, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="38e1e-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="38e1e-290">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="38e1e-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="38e1e-291">**Dage** – Angiv det antal dage, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="38e1e-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="38e1e-292">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="38e1e-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="38e1e-293">**Uger** – Angiv det antal uger, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="38e1e-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="38e1e-294">**Måneder** – Vælg den dag eller uge, hvor brugeren senest skal have reageret.</span><span class="sxs-lookup"><span data-stu-id="38e1e-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="38e1e-295">Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="38e1e-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="38e1e-296">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have reageret.</span><span class="sxs-lookup"><span data-stu-id="38e1e-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="38e1e-297">Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="38e1e-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="38e1e-298">Gentag trin 3 til 4 for hvert bruger, der skal føjes til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="38e1e-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="38e1e-299">Du kan ændre brugernes rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="38e1e-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="38e1e-300">Hvis brugerne i eskaleringsstien ikke reagerer inden for den tildelte tid, håndteres dokumentet automatisk af systemet.</span><span class="sxs-lookup"><span data-stu-id="38e1e-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="38e1e-301">Hvis du vil angive den handling, som systemet skal udføre, skal du vælge rækken **Handling** og derefter vælge en handling på fanen **Sluthandling**.</span><span class="sxs-lookup"><span data-stu-id="38e1e-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>
