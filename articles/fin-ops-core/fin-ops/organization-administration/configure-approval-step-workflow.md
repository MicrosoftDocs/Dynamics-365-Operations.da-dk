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
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2177069"
---
# <a name="configure-approval-steps-in-a-workflow"></a><span data-ttu-id="7079a-103">Konfigurere godkendelsestrin i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="7079a-103">Configure approval steps in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="7079a-104">I dette emne forklares det, hvordan du konfigurerer egenskaberne for et godkendelsestrin.</span><span class="sxs-lookup"><span data-stu-id="7079a-104">This topic explains how to configure the properties of an approval step.</span></span>

<span data-ttu-id="7079a-105">Hvis du vil konfigurere et godkendelsestrin i arbejdsgangseditoren, skal du højreklikke på godkendelsestrinnet og derefter klikke på **Egenskaber** for at åbne siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="7079a-105">To configure an approval step in the workflow editor, right-click the approval step, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="7079a-106">Brug derefter nedenstående procedurer til at konfigurere egenskaberne for godkendelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="7079a-106">Then use the following procedures to configure the properties of the approval step.</span></span>

## <a name="name-the-step"></a><span data-ttu-id="7079a-107">Angive et navn på trinnet</span><span class="sxs-lookup"><span data-stu-id="7079a-107">Name the step</span></span>
<span data-ttu-id="7079a-108">Udfør følgende trin for at angive et navn på godkendelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="7079a-108">Follow these steps to enter a name for the approval step.</span></span>

1. <span data-ttu-id="7079a-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="7079a-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="7079a-110">Angiv et entydigt navn til godkendelsestrinnet i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="7079a-110">In the **Name** field, enter a unique name for the approval step.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="7079a-111">Angive en emnelinje og instruktioner</span><span class="sxs-lookup"><span data-stu-id="7079a-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="7079a-112">Du skal angive en emnelinje og instruktioner til brugere, som har fået godkendelsestrinnet tildelt.</span><span class="sxs-lookup"><span data-stu-id="7079a-112">You must provide a subject line and instructions to users who are assigned to the approval step.</span></span> <span data-ttu-id="7079a-113">Hvis du f.eks. konfigurerer et godkendelsestrin for indkøbsrekvisitioner, kan den bruger, der har fået trinnet tildelt, se emnelinjen og instruktionerne på siden **Indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="7079a-113">For example, if you're configuring an approval step for purchase requisitions, the user who is assigned to the step sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="7079a-114">Emnelinjen vises i en meddelelseslinje på siden.</span><span class="sxs-lookup"><span data-stu-id="7079a-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="7079a-115">Brugeren kan derefter klikke på ikonet på meddelelseslinjen for at få vist instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="7079a-115">The user can then click the icon in the message bar to see the instructions.</span></span> <span data-ttu-id="7079a-116">Udfør følgende trin for at angive en emnelinje og instruktioner.</span><span class="sxs-lookup"><span data-stu-id="7079a-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="7079a-117">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="7079a-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="7079a-118">I feltet **Emne for workflowopgave** skal du indtaste emnelinjen.</span><span class="sxs-lookup"><span data-stu-id="7079a-118">In the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="7079a-119">Hvis du vil personalisere emnelinjen, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="7079a-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="7079a-120">Pladsholderne erstattes med de relevante data, når emnelinjen vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="7079a-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="7079a-121">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="7079a-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="7079a-122">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="7079a-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="7079a-123">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="7079a-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="7079a-124">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="7079a-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="7079a-125">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="7079a-125">Click **Insert**.</span></span>

4. <span data-ttu-id="7079a-126">Følg disse trin for at tilføje oversættelser af emnelinjen:</span><span class="sxs-lookup"><span data-stu-id="7079a-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="7079a-127">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="7079a-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="7079a-128">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="7079a-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="7079a-129">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="7079a-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="7079a-130">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="7079a-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="7079a-131">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 3.</span><span class="sxs-lookup"><span data-stu-id="7079a-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="7079a-132">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="7079a-132">Click **Close**.</span></span>

5. <span data-ttu-id="7079a-133">I feltet **Emne for workflowopgave** skal du indtaste instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="7079a-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="7079a-134">Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="7079a-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="7079a-135">Pladsholderne erstattes med de relevante data, når instruktionerne vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="7079a-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="7079a-136">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="7079a-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="7079a-137">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="7079a-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="7079a-138">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="7079a-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="7079a-139">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="7079a-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="7079a-140">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="7079a-140">Click **Insert**.</span></span>

7. <span data-ttu-id="7079a-141">Følg disse trin for at tilføje oversættelser af instruktionerne:</span><span class="sxs-lookup"><span data-stu-id="7079a-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="7079a-142">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="7079a-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="7079a-143">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="7079a-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="7079a-144">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="7079a-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="7079a-145">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="7079a-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="7079a-146">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 6.</span><span class="sxs-lookup"><span data-stu-id="7079a-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="7079a-147">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="7079a-147">Click **Close**.</span></span>

## <a name="assign-the-approval-step"></a><span data-ttu-id="7079a-148">Tildele godkendelsestrinnet</span><span class="sxs-lookup"><span data-stu-id="7079a-148">Assign the approval step</span></span>

<span data-ttu-id="7079a-149">Udfør følgende trin for at angive, hvem godkendelsestrinnet skal tildeles.</span><span class="sxs-lookup"><span data-stu-id="7079a-149">Follow these steps to specify who the approval step should be assigned to.</span></span>

1. <span data-ttu-id="7079a-150">Klik på **Tildeling** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="7079a-150">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="7079a-151">Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 3.</span><span class="sxs-lookup"><span data-stu-id="7079a-151">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="7079a-152">Indstilling</span><span class="sxs-lookup"><span data-stu-id="7079a-152">Option</span></span></th>
    <th><span data-ttu-id="7079a-153">Brugere, som godkendelsestrinnet er tildelt til</span><span class="sxs-lookup"><span data-stu-id="7079a-153">Users that the approval step is assigned to</span></span></th>
    <th><span data-ttu-id="7079a-154">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="7079a-154">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="7079a-155">Deltager</span><span class="sxs-lookup"><span data-stu-id="7079a-155">Participant</span></span></td>
    <td><span data-ttu-id="7079a-156">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="7079a-156">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7079a-157">Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil tildele trinnet til.</span><span class="sxs-lookup"><span data-stu-id="7079a-157">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the step to.</span></span></li>
    <li><span data-ttu-id="7079a-158">Vælg den gruppe eller rolle, som trinnet skal tildeles til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="7079a-158">In the <strong>Participant</strong> list, select the group or role to assign the step to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7079a-159">Hierarki</span><span class="sxs-lookup"><span data-stu-id="7079a-159">Hierarchy</span></span></td>
    <td><span data-ttu-id="7079a-160">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="7079a-160">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7079a-161">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil tildele trinnet til.</span><span class="sxs-lookup"><span data-stu-id="7079a-161">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the step to.</span></span></li>
    <li><span data-ttu-id="7079a-162">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="7079a-162">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="7079a-163">Disse navne repræsenterer de brugere, som trinnet kan tildeles til.</span><span class="sxs-lookup"><span data-stu-id="7079a-163">These names represent users that the step can be assigned to.</span></span> <span data-ttu-id="7079a-164">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="7079a-164">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="7079a-165">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="7079a-165">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="7079a-166">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="7079a-166">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="7079a-167">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="7079a-167">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="7079a-168">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet trinnet skal tildeles:</span><span class="sxs-lookup"><span data-stu-id="7079a-168">On the <strong>Hierarchy options</strong> tab, specify which users in the range the step should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="7079a-169"><strong>Tildel til alle hentede brugere</strong> – Trinnet tildeles alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="7079a-169"><strong>Assign to all users retrieved</strong> – The step is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="7079a-170"><strong>Tildel kun til den sidst hentede bruger</strong> – Trinnet tildeles kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="7079a-170"><strong>Assign only to last user retrieved</strong> – The step is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="7079a-171"><strong>Udeluk brugere med følgende betingelse</strong> – Trinnet tildeles ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="7079a-171"><strong>Exclude users with the following condition</strong> – The step isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="7079a-172">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="7079a-172">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7079a-173">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="7079a-173">Workflow user</span></span></td>
    <td><span data-ttu-id="7079a-174">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="7079a-174">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="7079a-175">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="7079a-175">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7079a-176">Bruger</span><span class="sxs-lookup"><span data-stu-id="7079a-176">User</span></span></td>
    <td><span data-ttu-id="7079a-177">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="7079a-177">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7079a-178">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="7079a-178">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="7079a-179">Listen <strong>Tilgængelige brugere</strong> indeholder alle systembrugere.</span><span class="sxs-lookup"><span data-stu-id="7079a-179">The <strong>Available users</strong> list includes all system users.</span></span> <span data-ttu-id="7079a-180">Vælg de brugere, der skal tildeles trinnet, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="7079a-180">Select the users to assign the step to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="7079a-181">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at håndtere eller reagere på dokumenter, der når til godkendelsestrinnet.</span><span class="sxs-lookup"><span data-stu-id="7079a-181">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents that reach the approval step.</span></span> <span data-ttu-id="7079a-182">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="7079a-182">Select one of the following options:</span></span>

    - <span data-ttu-id="7079a-183">**Timer** – Angiv det antal timer, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="7079a-183">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="7079a-184">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="7079a-184">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7079a-185">**Dage** – Angiv det antal dage, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="7079a-185">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="7079a-186">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="7079a-186">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7079a-187">**Uger** – Angiv det antal uger, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="7079a-187">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="7079a-188">**Måneder** – Vælg den dag eller uge, hvor brugeren senest skal have reageret.</span><span class="sxs-lookup"><span data-stu-id="7079a-188">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="7079a-189">Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="7079a-189">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="7079a-190">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have reageret.</span><span class="sxs-lookup"><span data-stu-id="7079a-190">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="7079a-191">Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="7079a-191">For example, you might want the user to respond by Friday of the third week of December.</span></span>

    <span data-ttu-id="7079a-192">Hvis brugeren ikke håndterer dokumentet inden for den tildelte tid, er dokumentet forsinket.</span><span class="sxs-lookup"><span data-stu-id="7079a-192">If the user doesn't take action on the document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="7079a-193">Et forsinket dokument eskaleres ud fra de indstillinger, du vælger i området **Eskalering** på siden.</span><span class="sxs-lookup"><span data-stu-id="7079a-193">A document that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

4. <span data-ttu-id="7079a-194">Hvis du har tildelt godkendelsestrinnet til flere brugere eller en gruppe af brugere, skal du vælge følgende indstillinger på fanen **Afviklingspolitik**:</span><span class="sxs-lookup"><span data-stu-id="7079a-194">If you assigned the approval step to multiple users or a group of users, on the **Completion policy** tab, select one of the following options:</span></span>

    - <span data-ttu-id="7079a-195">**Enkelt godkender** – den handling, der udføres på dokumentet, bestemmes af den første person, der reagerer.</span><span class="sxs-lookup"><span data-stu-id="7079a-195">**Single approver** – The action that is applied to the document is determined by the first person who responds.</span></span> <span data-ttu-id="7079a-196">Antag f.eks. at Søren har sendt en udgiftsrapport på kr. 15.000.</span><span class="sxs-lookup"><span data-stu-id="7079a-196">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="7079a-197">Dokumentet er aktuelt tildelt Mette, Karina og Bjarne.</span><span class="sxs-lookup"><span data-stu-id="7079a-197">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="7079a-198">Hvis Mette er den første person, der reagerer på dokumentet, vil den handling, hun udfører, blive anvendt på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="7079a-198">If Sue is the first person who responds to the document, the action that she takes is applied to the document.</span></span> <span data-ttu-id="7079a-199">Hvis Mette afviser dokumentet, afvises det og sendes tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="7079a-199">If Sue rejects the document, it's rejected and sent back to Sam.</span></span> <span data-ttu-id="7079a-200">Hvis Mette godkender dokumentet, sendes det til Dorthe til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="7079a-200">If Sue approves the document, it's sent to Ann for approval.</span></span>

        ![Arbejdsgang, der har en godkendelsesproces](./media/workflow_multipleusersinstep.gif)

    - <span data-ttu-id="7079a-202">**Flertal af godkendere** – den handling, der skal anvendes på dokumentet, bliver bestemt, når de fleste af godkenderne har reageret.</span><span class="sxs-lookup"><span data-stu-id="7079a-202">**Majority of approvers** – The action that is applied to the document is determined when most of the approvers respond.</span></span> <span data-ttu-id="7079a-203">Antag f.eks. at Søren har sendt en udgiftsrapport på kr. 15.000.</span><span class="sxs-lookup"><span data-stu-id="7079a-203">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="7079a-204">Dokumentet er aktuelt tildelt Mette, Karina og Bjarne.</span><span class="sxs-lookup"><span data-stu-id="7079a-204">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="7079a-205">Hvis Mette og Karina er de første personer, der reagerer på dokumentet, vil den handling, de udfører, blive anvendt på dokumentet.</span><span class="sxs-lookup"><span data-stu-id="7079a-205">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document.</span></span>

        - <span data-ttu-id="7079a-206">Hvis Mette godkender dokumentet, men Karina afviser det, vil dokumentet blive afvist og sendt tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="7079a-206">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="7079a-207">Hvis både Mette og Karina godkender dokumentet, vil det blive sendt til Dorthe til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="7079a-207">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="7079a-208">**Procent af godkendere** – den handling, der anvendes på dokumentet, bliver bestemt, når en bestemt procentdel af godkenderne svarer.</span><span class="sxs-lookup"><span data-stu-id="7079a-208">**Percentage of approvers** – The action that is applied to the document is determined when a specific percentage of the approvers respond.</span></span> <span data-ttu-id="7079a-209">Antag f.eks. at Søren har sendt en udgiftsrapport på kr. 15.000.</span><span class="sxs-lookup"><span data-stu-id="7079a-209">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="7079a-210">Udgiftsrapporten er aktuelt tildelt Mette, Karina og Bjarne, og du har angivet procentdelen til **50**.</span><span class="sxs-lookup"><span data-stu-id="7079a-210">The expense report is currently assigned to Sue, Jo, and Bill, and you entered **50** as the percentage.</span></span> <span data-ttu-id="7079a-211">Hvis Mette og Karina er de første to godkendere, der reagerer, vil den handling, de udfører, blive anvendt på dokumentet, fordi de opfylder kravet om at være 50 procent af godkendere.</span><span class="sxs-lookup"><span data-stu-id="7079a-211">If Sue and Jo are the first two approvers who respond, the action that they take is applied to the document, because they meet the requirement for 50 percent of approvers.</span></span>

        - <span data-ttu-id="7079a-212">Hvis Mette godkender dokumentet, men Karina afviser det, vil dokumentet blive afvist og sendt tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="7079a-212">If Sue approves the document, but Jo rejects it, the document is rejected and sent back to Sam.</span></span>
        - <span data-ttu-id="7079a-213">Hvis både Mette og Karina godkender dokumentet, vil det blive sendt til Dorthe til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="7079a-213">If both Sue and Jo approve the document, it's sent to Ann for approval.</span></span>

    - <span data-ttu-id="7079a-214">**Alle godkendere** – alle godkendere skal godkende dokumentet.</span><span class="sxs-lookup"><span data-stu-id="7079a-214">**All approvers** – All the approvers must approve the document.</span></span> <span data-ttu-id="7079a-215">Ellers kan arbejdsgangen ikke fortsætte.</span><span class="sxs-lookup"><span data-stu-id="7079a-215">Otherwise, the workflow can't continue.</span></span> <span data-ttu-id="7079a-216">Antag f.eks. at Søren har sendt en udgiftsrapport på 15.000 kr.</span><span class="sxs-lookup"><span data-stu-id="7079a-216">For example, Sam has submitted an expense report for USD 15,000.</span></span> <span data-ttu-id="7079a-217">Dokumentet er aktuelt tildelt Mette, Karina og Bjarne.</span><span class="sxs-lookup"><span data-stu-id="7079a-217">The expense report is currently assigned to Sue, Jo, and Bill.</span></span> <span data-ttu-id="7079a-218">Hvis Mette og Karina godkender dokumentet, men Bjarne afviser det, vil dokumentet blive afvist og sendt tilbage til Søren.</span><span class="sxs-lookup"><span data-stu-id="7079a-218">If Sue and Joe approve the document, but Bill rejects it, the document is rejected and sent back to Sam.</span></span> <span data-ttu-id="7079a-219">Hvis Mette, Karina og Bjarne godkender dokumentet, bliver det sendt til Dorthe til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="7079a-219">If Sue, Jo, and Bill all approve the document, it's sent to Ann for approval.</span></span>

## <a name="specify-when-the-approval-step-is-required"></a><span data-ttu-id="7079a-220">Angive, hvornår godkendelsestrinnet skal bruges</span><span class="sxs-lookup"><span data-stu-id="7079a-220">Specify when the approval step is required</span></span>

<span data-ttu-id="7079a-221">Du kan angive, hvornår godkendelsestrinnet er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="7079a-221">You can specify when the approval step is required.</span></span> <span data-ttu-id="7079a-222">Godkendelsestrinnet kan være påkrævet altid, eller det kan kun være påkrævet, hvis bestemte betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="7079a-222">The approval step can always be required, or it can be required only if specific conditions are met.</span></span>

### <a name="the-approval-step-is-always-required"></a><span data-ttu-id="7079a-223">Godkendelsestrinnet er altid påkrævet</span><span class="sxs-lookup"><span data-stu-id="7079a-223">The approval step is always required</span></span>

<span data-ttu-id="7079a-224">Udfør følgende trin, hvis godkendelsestrinnet altid er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="7079a-224">Follow these steps if the approval step is always required.</span></span>

1. <span data-ttu-id="7079a-225">Klik på **Betingelse** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="7079a-225">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="7079a-226">Vælg indstillingen **Udfør altid dette trin**.</span><span class="sxs-lookup"><span data-stu-id="7079a-226">Select the **Always run this step** option.</span></span>

### <a name="the-approval-step-is-required-in-specific-conditions"></a><span data-ttu-id="7079a-227">Godkendelsestrinnet er påkrævet under bestemte betingelser.</span><span class="sxs-lookup"><span data-stu-id="7079a-227">The approval step is required in specific conditions</span></span>

<span data-ttu-id="7079a-228">Det godkendelsestrin, du er ved at konfigurere, er måske kun påkrævet, hvis bestemte betingelser er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="7079a-228">The approval step that you're configuring might be required only if specific conditions are met.</span></span> <span data-ttu-id="7079a-229">Hvis du f.eks. er ved at konfigurere et godkendelsestrin til en arbejdsgang for en indkøbsrekvisition, vil du måske have, at godkendelsestrinnet kun skal bruges, hvis indkøbsrekvisitionsbeløbet er større end 10.000 kr.</span><span class="sxs-lookup"><span data-stu-id="7079a-229">For example, if you're configuring an approval step for a purchase requisition workflow, you might want the approval step to occur only if the amount of the purchase requisition is more than USD 10,000.</span></span> <span data-ttu-id="7079a-230">Udfør følgende trin, når du skal angive, at godkendelsestrinnet er påkrævet.</span><span class="sxs-lookup"><span data-stu-id="7079a-230">Follow these steps to specify when the approval step is required.</span></span>

1. <span data-ttu-id="7079a-231">Klik på **Betingelse** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="7079a-231">In the left pane, click **Condition**.</span></span>
2. <span data-ttu-id="7079a-232">Vælg indstillingen **Kør kun dette trin, når følgende betingelse er opfyldt**.</span><span class="sxs-lookup"><span data-stu-id="7079a-232">Select the **Run this step only when the following condition is met** option.</span></span>
3. <span data-ttu-id="7079a-233">Angiv en betingelse.</span><span class="sxs-lookup"><span data-stu-id="7079a-233">Enter a condition.</span></span>
4. <span data-ttu-id="7079a-234">Angiv eventuelle supplerende betingelser, hvis det er påkrævede.</span><span class="sxs-lookup"><span data-stu-id="7079a-234">Enter any additional conditions that are required.</span></span>
5. <span data-ttu-id="7079a-235">Hvis du vil kontrollere, at de betingelser, du har angivet, er konfigureret korrekt, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="7079a-235">To verify that the conditions that you entered are configured correctly, follow these steps:</span></span>

    1. <span data-ttu-id="7079a-236">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="7079a-236">Click **Test**.</span></span>
    2. <span data-ttu-id="7079a-237">På siden **Test betingelse for arbejdsgang** i området **Valider betingelse**, og vælg en post.</span><span class="sxs-lookup"><span data-stu-id="7079a-237">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="7079a-238">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="7079a-238">Click **Test**.</span></span> <span data-ttu-id="7079a-239">Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har defineret.</span><span class="sxs-lookup"><span data-stu-id="7079a-239">The system evaluates the record to determine whether it meets the conditions that you defined.</span></span>
    4. <span data-ttu-id="7079a-240">Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="7079a-240">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-what-happens-when-the-document-is-overdue"></a><span data-ttu-id="7079a-241">Angive, hvad der sker, når dokumentet er forfaldent</span><span class="sxs-lookup"><span data-stu-id="7079a-241">Specify what happens when the document is overdue</span></span>

<span data-ttu-id="7079a-242">Hvis en bruger ikke håndterer et dokument inden for den tildelte tid, er dokumentet forfaldent.</span><span class="sxs-lookup"><span data-stu-id="7079a-242">If a user doesn't take action on a document in the allotted time, the document is overdue.</span></span> <span data-ttu-id="7079a-243">Et forfaldent dokument kan eskaleres eller tildeles automatisk til en anden bruger til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="7079a-243">A document that is overdue can be escalated, or automatically assigned to another user for approval.</span></span> <span data-ttu-id="7079a-244">Følg disse trin for at eskalere dokumentet, hvis det er forfaldent.</span><span class="sxs-lookup"><span data-stu-id="7079a-244">Follow these steps to escalate the document if it's overdue.</span></span>

1. <span data-ttu-id="7079a-245">Klik på **Eskalering** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="7079a-245">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="7079a-246">Markér afkrydsningsfeltet **Brug eskaleringssti** for at oprette en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="7079a-246">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="7079a-247">De brugere, der er angivet i eskaleringsstien, tildeles automatisk dokumentet.</span><span class="sxs-lookup"><span data-stu-id="7079a-247">The system automatically assigns the document to the users who are listed in the escalation path.</span></span> <span data-ttu-id="7079a-248">Følgende tabel repræsenterer f.eks. en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="7079a-248">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="7079a-249">Forløb</span><span class="sxs-lookup"><span data-stu-id="7079a-249">Sequence</span></span> | <span data-ttu-id="7079a-250">Eskaleringssti</span><span class="sxs-lookup"><span data-stu-id="7079a-250">Escalation path</span></span>      |
    |----------|----------------------|
    | <span data-ttu-id="7079a-251">1</span><span class="sxs-lookup"><span data-stu-id="7079a-251">1</span></span>        | <span data-ttu-id="7079a-252">Knyt til: Anna</span><span class="sxs-lookup"><span data-stu-id="7079a-252">Assign to: Donna</span></span>     |
    | <span data-ttu-id="7079a-253">2</span><span class="sxs-lookup"><span data-stu-id="7079a-253">2</span></span>        | <span data-ttu-id="7079a-254">Knyt til: Erik</span><span class="sxs-lookup"><span data-stu-id="7079a-254">Assign to: Erin</span></span>      |
    | <span data-ttu-id="7079a-255">3</span><span class="sxs-lookup"><span data-stu-id="7079a-255">3</span></span>        | <span data-ttu-id="7079a-256">Sluthandling: Afvis</span><span class="sxs-lookup"><span data-stu-id="7079a-256">Final action: Reject</span></span> |

    <span data-ttu-id="7079a-257">I dette eksempel tildeles det forfaldne dokument automatisk til Anna.</span><span class="sxs-lookup"><span data-stu-id="7079a-257">In this example, the system assigns the overdue document to Donna.</span></span> <span data-ttu-id="7079a-258">Hvis Anna ikke reagerer inden for den tildelte tid, tildeles dokumentet automatisk til Erik.</span><span class="sxs-lookup"><span data-stu-id="7079a-258">If Donna doesn't respond in the allotted time, the system assigns the document to Erin.</span></span> <span data-ttu-id="7079a-259">Hvis Erik ikke reagerer inden for den tildelte tid, afvises dokumentet automatisk.</span><span class="sxs-lookup"><span data-stu-id="7079a-259">If Erin doesn't respond in the allotted time, the system rejects the document.</span></span>

3. <span data-ttu-id="7079a-260">Klik på **Tilføj eskalering** for at føje en bruger til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="7079a-260">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="7079a-261">Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og følg derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 4.</span><span class="sxs-lookup"><span data-stu-id="7079a-261">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="7079a-262">Indstilling</span><span class="sxs-lookup"><span data-stu-id="7079a-262">Option</span></span></th>
    <th><span data-ttu-id="7079a-263">Brugere, som dokumentet eskaleres til</span><span class="sxs-lookup"><span data-stu-id="7079a-263">Users that the document is escalated to</span></span></th>
    <th><span data-ttu-id="7079a-264">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="7079a-264">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="7079a-265">Hierarki</span><span class="sxs-lookup"><span data-stu-id="7079a-265">Hierarchy</span></span></td>
    <td><span data-ttu-id="7079a-266">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="7079a-266">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7079a-267">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil eskalere dokumentet til.</span><span class="sxs-lookup"><span data-stu-id="7079a-267">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the document to.</span></span></li>
    <li><span data-ttu-id="7079a-268">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="7079a-268">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="7079a-269">Disse navne repræsenterer de brugere, som dokumentet kan eskaleres til.</span><span class="sxs-lookup"><span data-stu-id="7079a-269">These names represent users that the document can be escalated to.</span></span> <span data-ttu-id="7079a-270">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="7079a-270">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="7079a-271">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="7079a-271">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="7079a-272">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="7079a-272">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="7079a-273">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="7079a-273">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="7079a-274">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet dokumentet skal eskaleres til:</span><span class="sxs-lookup"><span data-stu-id="7079a-274">On the <strong>Hierarchy options</strong> tab, specify which users in the range the document should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="7079a-275"><strong>Tildel til alle hentede brugere</strong> – Dokumentet eskaleres til alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="7079a-275"><strong>Assign to all users retrieved</strong> – The document is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="7079a-276"><strong>Tildel kun til den sidst hentede bruger</strong> – Dokumentet eskaleres kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="7079a-276"><strong>Assign only to last user retrieved</strong> – The document is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="7079a-277"><strong>Udeluk brugere med følgende betingelse</strong> – Dokumentet eskaleres ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="7079a-277"><strong>Exclude users with the following condition</strong> – The document isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="7079a-278">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="7079a-278">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7079a-279">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="7079a-279">Workflow user</span></span></td>
    <td><span data-ttu-id="7079a-280">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="7079a-280">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="7079a-281">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="7079a-281">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="7079a-282">Bruger</span><span class="sxs-lookup"><span data-stu-id="7079a-282">User</span></span></td>
    <td><span data-ttu-id="7079a-283">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="7079a-283">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="7079a-284">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="7079a-284">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="7079a-285">Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere.</span><span class="sxs-lookup"><span data-stu-id="7079a-285">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="7079a-286">Vælg de brugere, dokumentet skal eskaleres til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="7079a-286">Select the users to escalate the document to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="7079a-287">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at håndtere eller reagere på dokumenter.</span><span class="sxs-lookup"><span data-stu-id="7079a-287">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to take action on, or respond to, documents.</span></span> <span data-ttu-id="7079a-288">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="7079a-288">Select one of the following options:</span></span>

    - <span data-ttu-id="7079a-289">**Timer** – Angiv det antal timer, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="7079a-289">**Hours** – Enter the number of hours that the user has to respond.</span></span> <span data-ttu-id="7079a-290">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="7079a-290">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7079a-291">**Dage** – Angiv det antal dage, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="7079a-291">**Days** – Enter the number of days that the user has to respond.</span></span> <span data-ttu-id="7079a-292">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="7079a-292">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="7079a-293">**Uger** – Angiv det antal uger, som brugeren har til at reagere i.</span><span class="sxs-lookup"><span data-stu-id="7079a-293">**Weeks** – Enter the number of weeks that the user has to respond.</span></span>
    - <span data-ttu-id="7079a-294">**Måneder** – Vælg den dag eller uge, hvor brugeren senest skal have reageret.</span><span class="sxs-lookup"><span data-stu-id="7079a-294">**Months** – Select the day and week that the user must respond by.</span></span> <span data-ttu-id="7079a-295">Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="7079a-295">For example, you might want the user to respond by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="7079a-296">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have reageret.</span><span class="sxs-lookup"><span data-stu-id="7079a-296">**Years** – Select the day, week, and month that the user must respond by.</span></span> <span data-ttu-id="7079a-297">Det kan f.eks. være, at brugeren skal have reageret senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="7079a-297">For example, you might want the user to respond by Friday of the third week of December.</span></span>

5. <span data-ttu-id="7079a-298">Gentag trin 3 til 4 for hvert bruger, der skal føjes til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="7079a-298">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="7079a-299">Du kan ændre brugernes rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="7079a-299">You can change the order of the users.</span></span>
6. <span data-ttu-id="7079a-300">Hvis brugerne i eskaleringsstien ikke reagerer inden for den tildelte tid, håndteres dokumentet automatisk af systemet.</span><span class="sxs-lookup"><span data-stu-id="7079a-300">If the users in the escalation path don't respond in the allotted time, the system automatically take action on the document.</span></span> <span data-ttu-id="7079a-301">Hvis du vil angive den handling, som systemet skal udføre, skal du vælge rækken **Handling** og derefter vælge en handling på fanen **Sluthandling**.</span><span class="sxs-lookup"><span data-stu-id="7079a-301">To specify the action that the system takes, select the **Action** row, and then, on the **End action** tab, select an action.</span></span>
