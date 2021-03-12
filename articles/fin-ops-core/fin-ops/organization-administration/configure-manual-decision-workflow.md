---
title: Konfigurere manuelle beslutninger i en arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en manuel beslutning.
author: ChrisGarty
manager: AnnBe
ms.date: 06/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: cgarty
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d351facbce02355ddb4bdf91d43d9df561e4f3b5
ms.sourcegitcommit: b112925c389a460a98c3401cc2c67df7091b066f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/19/2020
ms.locfileid: "4798846"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="380fa-103">Konfigurere manuelle beslutninger i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="380fa-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="380fa-104">I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en manuel beslutning.</span><span class="sxs-lookup"><span data-stu-id="380fa-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="380fa-105">Hvis du vil konfigurere en manuel beslutning i arbejdsgangseditoren, skal du højreklikke på den manuelle beslutning og derefter klikke på **Egenskaber** for at åbne formularen **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="380fa-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="380fa-106">Brug derefter nedenstående procedure for at konfigurere egenskaberne for den manuelle beslutning.</span><span class="sxs-lookup"><span data-stu-id="380fa-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="380fa-107">Navngive beslutningen</span><span class="sxs-lookup"><span data-stu-id="380fa-107">Name the decision</span></span>

<span data-ttu-id="380fa-108">Udfør følgende trin for at angive et navn på den manuelle beslutning.</span><span class="sxs-lookup"><span data-stu-id="380fa-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="380fa-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="380fa-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="380fa-110">Angiv et entydigt navn på den manuelle beslutning i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="380fa-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="380fa-111">Angive en emnelinje og instruktioner</span><span class="sxs-lookup"><span data-stu-id="380fa-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="380fa-112">Du skal angive en emnelinje og instruktioner til brugere, som har fået den manuelle beslutning tildelt.</span><span class="sxs-lookup"><span data-stu-id="380fa-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="380fa-113">Hvis du f.eks. konfigurerer en beslutning for indkøbsrekvisitioner, ser den bruger, der har fået beslutningen tildelt, emnelinjen og instruktionerne på siden **Indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="380fa-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="380fa-114">Emnelinjen vises i en meddelelseslinje på siden.</span><span class="sxs-lookup"><span data-stu-id="380fa-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="380fa-115">Brugeren kan derefter klikke på ikonet på meddelelseslinjen for at få vist detaljerede instruktioner.</span><span class="sxs-lookup"><span data-stu-id="380fa-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="380fa-116">Udfør følgende trin for at angive en emnelinje og instruktioner.</span><span class="sxs-lookup"><span data-stu-id="380fa-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="380fa-117">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="380fa-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="380fa-118">På fanen **Instruktioner** i feltet **Emne for workflowopgave** skal du indtaste emnelinjen.</span><span class="sxs-lookup"><span data-stu-id="380fa-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="380fa-119">Hvis du vil personalisere emnelinjen, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="380fa-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="380fa-120">Pladsholderne erstattes med de relevante data, når emnelinjen vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="380fa-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="380fa-121">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="380fa-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="380fa-122">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="380fa-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="380fa-123">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="380fa-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="380fa-124">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="380fa-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="380fa-125">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="380fa-125">Click **Insert**.</span></span>

4. <span data-ttu-id="380fa-126">Følg disse trin for at tilføje oversættelser af emnelinjen:</span><span class="sxs-lookup"><span data-stu-id="380fa-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="380fa-127">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="380fa-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="380fa-128">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="380fa-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="380fa-129">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="380fa-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="380fa-130">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="380fa-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="380fa-131">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 3.</span><span class="sxs-lookup"><span data-stu-id="380fa-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="380fa-132">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="380fa-132">Click **Close**.</span></span>

5. <span data-ttu-id="380fa-133">I feltet **Emne for workflowopgave** skal du indtaste instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="380fa-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="380fa-134">Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="380fa-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="380fa-135">Pladsholderne erstattes med de relevante data, når instruktionerne vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="380fa-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="380fa-136">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="380fa-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="380fa-137">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="380fa-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="380fa-138">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="380fa-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="380fa-139">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="380fa-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="380fa-140">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="380fa-140">Click **Insert**.</span></span>

7. <span data-ttu-id="380fa-141">Følg disse trin for at tilføje oversættelser af instruktionerne:</span><span class="sxs-lookup"><span data-stu-id="380fa-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="380fa-142">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="380fa-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="380fa-143">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="380fa-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="380fa-144">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="380fa-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="380fa-145">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="380fa-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="380fa-146">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 6.</span><span class="sxs-lookup"><span data-stu-id="380fa-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="380fa-147">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="380fa-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="380fa-148">Angive mulige udfald af en beslutning</span><span class="sxs-lookup"><span data-stu-id="380fa-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="380fa-149">Når et dokument tildeles en beslutningstager, får beslutningstageren typisk stillet et spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="380fa-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="380fa-150">Svaret på spørgsmålet er normalt **Ja** eller **Nej**, **Sand** eller **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="380fa-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="380fa-151">Udfør følgende trin for at angive det mulige udfald af den manuelle beslutning.</span><span class="sxs-lookup"><span data-stu-id="380fa-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="380fa-152">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="380fa-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="380fa-153">Indtast navnet på udfaldet eller indstillingen på fanen **Udfald** i feltet **Udfald 1**.</span><span class="sxs-lookup"><span data-stu-id="380fa-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="380fa-154">Følg disse trin for at tilføje oversættelser af udfaldet:</span><span class="sxs-lookup"><span data-stu-id="380fa-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="380fa-155">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="380fa-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="380fa-156">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="380fa-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="380fa-157">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="380fa-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="380fa-158">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="380fa-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="380fa-159">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="380fa-159">Click **Close**.</span></span>

4. <span data-ttu-id="380fa-160">Indtast navnet på udfaldet eller indstillingen i feltet **Udfald 2**.</span><span class="sxs-lookup"><span data-stu-id="380fa-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="380fa-161">Følg disse trin for at tilføje oversættelser af udfaldet:</span><span class="sxs-lookup"><span data-stu-id="380fa-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="380fa-162">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="380fa-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="380fa-163">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="380fa-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="380fa-164">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="380fa-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="380fa-165">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="380fa-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="380fa-166">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="380fa-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="380fa-167">Angive, hvornår beskeder sendes</span><span class="sxs-lookup"><span data-stu-id="380fa-167">Specify when notifications are sent</span></span>

<span data-ttu-id="380fa-168">Du kan sende beskeder til personer, når en beslutning er truffet, delegeret videre eller eskaleret.</span><span class="sxs-lookup"><span data-stu-id="380fa-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="380fa-169">Udfør følgende trin for at angive, hvornår der sendes beskeder, og hvem beskederne sendes til.</span><span class="sxs-lookup"><span data-stu-id="380fa-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="380fa-170">Klik på **Beskeder** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="380fa-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="380fa-171">Markér afkrydsningsfeltet ud for de hændelser, som beskederne udsendes i forbindelse med.</span><span class="sxs-lookup"><span data-stu-id="380fa-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="380fa-172">**\[Valg 1\]** – Den bruger, der er tildelt beskeden, har valgt **\[Valg 1\]**.</span><span class="sxs-lookup"><span data-stu-id="380fa-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="380fa-173">**\[Valg 2\]** – Den bruger, der er tildelt beskeden, har valgt **\[Valg 2\]**.</span><span class="sxs-lookup"><span data-stu-id="380fa-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="380fa-174">**Deleger** – Den bruger, der er tildelt beslutningen, har tildelt den til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="380fa-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="380fa-175">**Eskaler** – Den bruger, der har fået tildelt beslutningen, har ikke truffet beslutningen inden for den tildelte tid.</span><span class="sxs-lookup"><span data-stu-id="380fa-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="380fa-176">Vælg rækken for den hændelse, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="380fa-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="380fa-177">Indtast teksten til beskeden i tekstfeltet på fanen **Beskedtekst**.</span><span class="sxs-lookup"><span data-stu-id="380fa-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="380fa-178">Hvis du vil personalisere beskeden, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="380fa-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="380fa-179">Pladsholderne erstattes med de relevante data, når beskeden vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="380fa-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="380fa-180">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="380fa-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="380fa-181">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="380fa-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="380fa-182">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="380fa-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="380fa-183">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="380fa-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="380fa-184">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="380fa-184">Click **Insert**.</span></span>

6. <span data-ttu-id="380fa-185">Følg disse trin for at tilføje oversættelser af beskeden:</span><span class="sxs-lookup"><span data-stu-id="380fa-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="380fa-186">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="380fa-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="380fa-187">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="380fa-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="380fa-188">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="380fa-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="380fa-189">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="380fa-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="380fa-190">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 5.</span><span class="sxs-lookup"><span data-stu-id="380fa-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="380fa-191">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="380fa-191">Click **Close**.</span></span>

7. <span data-ttu-id="380fa-192">På fanen **Modtager** skal du angive, hvem beskederne skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="380fa-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="380fa-193">Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 8.</span><span class="sxs-lookup"><span data-stu-id="380fa-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="380fa-194">Indstilling</span><span class="sxs-lookup"><span data-stu-id="380fa-194">Option</span></span></th>
    <th><span data-ttu-id="380fa-195">Modtagere af besked</span><span class="sxs-lookup"><span data-stu-id="380fa-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="380fa-196">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="380fa-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="380fa-197">Deltager</span><span class="sxs-lookup"><span data-stu-id="380fa-197">Participant</span></span></td>
    <td><span data-ttu-id="380fa-198">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="380fa-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="380fa-199">Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</span><span class="sxs-lookup"><span data-stu-id="380fa-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="380fa-200">Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="380fa-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="380fa-201">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="380fa-201">Workflow user</span></span></td>
    <td><span data-ttu-id="380fa-202">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="380fa-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="380fa-203">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="380fa-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="380fa-204">Bruger</span><span class="sxs-lookup"><span data-stu-id="380fa-204">User</span></span></td>
    <td><span data-ttu-id="380fa-205">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="380fa-205">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="380fa-206">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="380fa-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="380fa-207">Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere.</span><span class="sxs-lookup"><span data-stu-id="380fa-207">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="380fa-208">Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="380fa-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="380fa-209">Gentag trin 3 til 7 for hver af de hændelser, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="380fa-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="380fa-210">Tildele en beslutning</span><span class="sxs-lookup"><span data-stu-id="380fa-210">Assign a decision</span></span>

<span data-ttu-id="380fa-211">Udfør følgende trin for at angive, hvem en manuel beslutning skal tildeles til.</span><span class="sxs-lookup"><span data-stu-id="380fa-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="380fa-212">Klik på **Tildeling** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="380fa-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="380fa-213">Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 3.</span><span class="sxs-lookup"><span data-stu-id="380fa-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="380fa-214">Indstilling</span><span class="sxs-lookup"><span data-stu-id="380fa-214">Option</span></span></th>
    <th><span data-ttu-id="380fa-215">Brugere, som beslutningen tildeles</span><span class="sxs-lookup"><span data-stu-id="380fa-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="380fa-216">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="380fa-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="380fa-217">Deltager</span><span class="sxs-lookup"><span data-stu-id="380fa-217">Participant</span></span></td>
    <td><span data-ttu-id="380fa-218">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="380fa-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="380fa-219">Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil tildele beslutningen til.</span><span class="sxs-lookup"><span data-stu-id="380fa-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="380fa-220">Vælg den type gruppe eller rolle, som beslutningen skal tildeles til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="380fa-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="380fa-221">Hierarki</span><span class="sxs-lookup"><span data-stu-id="380fa-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="380fa-222">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="380fa-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="380fa-223">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil tildele beslutningen til.</span><span class="sxs-lookup"><span data-stu-id="380fa-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="380fa-224">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="380fa-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="380fa-225">Disse navne repræsenterer de brugere, som beslutningen kan tildeles til.</span><span class="sxs-lookup"><span data-stu-id="380fa-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="380fa-226">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="380fa-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="380fa-227">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="380fa-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="380fa-228">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="380fa-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="380fa-229">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="380fa-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="380fa-230">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet beslutningen skal tildeles:</span><span class="sxs-lookup"><span data-stu-id="380fa-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="380fa-231"><strong>Tildel til alle hentede brugere</strong> – Beslutningen tildeles alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="380fa-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="380fa-232"><strong>Tildel kun til den sidst hentede bruger</strong> – Beslutningen tildeles kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="380fa-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="380fa-233"><strong>Udeluk brugere med følgende betingelse</strong> – Beslutningen tildeles ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="380fa-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="380fa-234">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="380fa-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="380fa-235">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="380fa-235">Workflow user</span></span></td>
    <td><span data-ttu-id="380fa-236">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="380fa-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="380fa-237">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="380fa-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="380fa-238">Bruger</span><span class="sxs-lookup"><span data-stu-id="380fa-238">User</span></span></td>
    <td><span data-ttu-id="380fa-239">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="380fa-239">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="380fa-240">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="380fa-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="380fa-241">Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere.</span><span class="sxs-lookup"><span data-stu-id="380fa-241">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="380fa-242">Vælg de brugere, der skal tildeles beslutningen, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="380fa-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="380fa-243">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-243">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="380fa-244">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="380fa-244">Select one of the following options:</span></span>

    - <span data-ttu-id="380fa-245">**Timer** – Angiv det antal timer, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-245">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="380fa-246">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="380fa-246">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="380fa-247">**Dage** – Angiv det antal dage, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-247">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="380fa-248">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="380fa-248">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="380fa-249">**Uger** – Angiv det antal uger, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-249">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="380fa-250">**Måneder** – Vælg den dag og uge, hvor brugeren senest skal have truffet beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-250">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="380fa-251">Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="380fa-251">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="380fa-252">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have truffet beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-252">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="380fa-253">Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="380fa-253">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="380fa-254">Hvis brugeren ikke træffer beslutningen inden for den tildelte tid, er beslutningen forsinket.</span><span class="sxs-lookup"><span data-stu-id="380fa-254">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="380fa-255">En forsinket beslutning eskaleres ud fra de indstillinger, du vælger i området **Eskalering** på siden.</span><span class="sxs-lookup"><span data-stu-id="380fa-255">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="380fa-256">Angive, hvad der sker, når en beslutning er forsinket.</span><span class="sxs-lookup"><span data-stu-id="380fa-256">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="380fa-257">Hvis en bruger ikke træffer beslutningen inden for den tildelte tid, er beslutningen forsinket.</span><span class="sxs-lookup"><span data-stu-id="380fa-257">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="380fa-258">En beslutning, der er forfalden, kan eskaleres eller tildeles automatisk til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="380fa-258">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="380fa-259">Udfør følgende trin for at eskalere beslutningen, hvis den er forsinket.</span><span class="sxs-lookup"><span data-stu-id="380fa-259">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="380fa-260">Klik på **Eskalering** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="380fa-260">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="380fa-261">Markér afkrydsningsfeltet **Brug eskaleringssti** for at oprette en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="380fa-261">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="380fa-262">De brugere, der er angivet i eskaleringsstien, tildeles automatisk beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-262">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="380fa-263">Følgende tabel repræsenterer f.eks. en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="380fa-263">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="380fa-264">Forløb</span><span class="sxs-lookup"><span data-stu-id="380fa-264">Sequence</span></span> | <span data-ttu-id="380fa-265">Eskaleringssti</span><span class="sxs-lookup"><span data-stu-id="380fa-265">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="380fa-266">1</span><span class="sxs-lookup"><span data-stu-id="380fa-266">1</span></span>        | <span data-ttu-id="380fa-267">Knyt til: Anna</span><span class="sxs-lookup"><span data-stu-id="380fa-267">Assign to: Donna</span></span>           |
    | <span data-ttu-id="380fa-268">2</span><span class="sxs-lookup"><span data-stu-id="380fa-268">2</span></span>        | <span data-ttu-id="380fa-269">Knyt til: Erik</span><span class="sxs-lookup"><span data-stu-id="380fa-269">Assign to: Erin</span></span>            |
    | <span data-ttu-id="380fa-270">3</span><span class="sxs-lookup"><span data-stu-id="380fa-270">3</span></span>        | <span data-ttu-id="380fa-271">Sluthandling: \[Valg 1\]</span><span class="sxs-lookup"><span data-stu-id="380fa-271">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="380fa-272">I dette eksempel tildeles den forsinkede beslutning automatisk til Anna.</span><span class="sxs-lookup"><span data-stu-id="380fa-272">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="380fa-273">Hvis Anna ikke træffer beslutningen inden for den tildelte tid, tildeles beslutningen automatisk til Erik.</span><span class="sxs-lookup"><span data-stu-id="380fa-273">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="380fa-274">Hvis Erik ikke træffer beslutningen inden for den tildelte tid, vælges **\[Valg 1\]** automatisk som beslutning.</span><span class="sxs-lookup"><span data-stu-id="380fa-274">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="380fa-275">Klik på **Tilføj eskalering** for at føje en bruger til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="380fa-275">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="380fa-276">Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 4.</span><span class="sxs-lookup"><span data-stu-id="380fa-276">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="380fa-277">Indstilling</span><span class="sxs-lookup"><span data-stu-id="380fa-277">Option</span></span></th>
    <th><span data-ttu-id="380fa-278">Brugere, som beslutningen eskaleres til</span><span class="sxs-lookup"><span data-stu-id="380fa-278">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="380fa-279">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="380fa-279">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="380fa-280">Hierarki</span><span class="sxs-lookup"><span data-stu-id="380fa-280">Hierarchy</span></span></td>
    <td><span data-ttu-id="380fa-281">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="380fa-281">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="380fa-282">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil eskalere beslutningen til.</span><span class="sxs-lookup"><span data-stu-id="380fa-282">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="380fa-283">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="380fa-283">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="380fa-284">Disse navne repræsenterer de brugere, som beslutningen kan eskaleres til.</span><span class="sxs-lookup"><span data-stu-id="380fa-284">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="380fa-285">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="380fa-285">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="380fa-286">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="380fa-286">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="380fa-287">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="380fa-287">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="380fa-288">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="380fa-288">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="380fa-289">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet beslutningen skal eskaleres til:</span><span class="sxs-lookup"><span data-stu-id="380fa-289">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="380fa-290"><strong>Tildel til alle hentede brugere</strong> – Beslutningen eskaleres til alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="380fa-290"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="380fa-291"><strong>Tildel kun til den sidst hentede bruger</strong> – Beslutningen eskaleres kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="380fa-291"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="380fa-292"><strong>Udeluk brugere med følgende betingelse</strong> – Beslutningen eskaleres ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="380fa-292"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="380fa-293">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="380fa-293">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="380fa-294">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="380fa-294">Workflow user</span></span></td>
    <td><span data-ttu-id="380fa-295">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="380fa-295">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="380fa-296">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="380fa-296">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="380fa-297">Bruger</span><span class="sxs-lookup"><span data-stu-id="380fa-297">User</span></span></td>
    <td><span data-ttu-id="380fa-298">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="380fa-298">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="380fa-299">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="380fa-299">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="380fa-300">Listen <strong>Tilgængelige brugere</strong> indeholder alle brugere.</span><span class="sxs-lookup"><span data-stu-id="380fa-300">The <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="380fa-301">Vælg de brugere, beslutningen skal eskaleres til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="380fa-301">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="380fa-302">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-302">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="380fa-303">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="380fa-303">Select one of the following options:</span></span>

    - <span data-ttu-id="380fa-304">**Timer** – Angiv det antal timer, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-304">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="380fa-305">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="380fa-305">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="380fa-306">**Dage** – Angiv det antal dage, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-306">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="380fa-307">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="380fa-307">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="380fa-308">**Uger** – Angiv det antal uger, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-308">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="380fa-309">**Måneder** – Vælg den dag og uge, hvor brugeren senest skal have truffet beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-309">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="380fa-310">Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="380fa-310">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="380fa-311">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have truffet beslutningen.</span><span class="sxs-lookup"><span data-stu-id="380fa-311">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="380fa-312">Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="380fa-312">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="380fa-313">Gentag trin 3 til 4 for hvert bruger, der skal føjes til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="380fa-313">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="380fa-314">Du kan ændre brugernes rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="380fa-314">You can change the order of the users.</span></span>
6. <span data-ttu-id="380fa-315">Hvis brugerne i eskaleringsstien ikke træffer beslutningen inden for den tildelte tid, træffes beslutningen automatisk af systemet.</span><span class="sxs-lookup"><span data-stu-id="380fa-315">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="380fa-316">Hvis du vil angive den indstilling, som systemet vælger, skal du vælge rækken **Handling** og derefter vælge en indstilling på fanen **Sluthandling**.</span><span class="sxs-lookup"><span data-stu-id="380fa-316">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="380fa-317">Angive en tidsgrænse</span><span class="sxs-lookup"><span data-stu-id="380fa-317">Set a time limit</span></span>

<span data-ttu-id="380fa-318">Udfør følgende trin, hvis beslutningen skal træffes inden en bestemt tidsgrænse.</span><span class="sxs-lookup"><span data-stu-id="380fa-318">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="380fa-319">De indstillinger, du vælger i denne procedure, overskriver de indstillinger, du har valgt i områderne **Tildeling** og **Eskalering** på siden.</span><span class="sxs-lookup"><span data-stu-id="380fa-319">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="380fa-320">Klik på **Avancerede indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="380fa-320">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="380fa-321">Markér afkrydsningsfeltet **Angiv en tidsgrænse for arbejdsgangselementet**</span><span class="sxs-lookup"><span data-stu-id="380fa-321">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="380fa-322">Angiv, hvornår beslutningen skal være truffet, i feltet **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="380fa-322">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="380fa-323">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="380fa-323">Select one of the following options:</span></span>

    - <span data-ttu-id="380fa-324">**Timer** – Angiv antallet af timer.</span><span class="sxs-lookup"><span data-stu-id="380fa-324">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="380fa-325">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="380fa-325">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="380fa-326">**Dage** – Angiv antallet af dage.</span><span class="sxs-lookup"><span data-stu-id="380fa-326">**Days** – Enter the number of days.</span></span> <span data-ttu-id="380fa-327">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="380fa-327">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="380fa-328">**Uger** – Angiv antallet af uger.</span><span class="sxs-lookup"><span data-stu-id="380fa-328">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="380fa-329">**Måneder** – Vælg den dag og uge, hvor beslutningen senest skal være truffet.</span><span class="sxs-lookup"><span data-stu-id="380fa-329">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="380fa-330">Det kan være, at beslutningen f.eks. skal være truffet senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="380fa-330">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="380fa-331">**År** – Vælg den dag, uge og måned, hvor beslutningen senest skal være truffet.</span><span class="sxs-lookup"><span data-stu-id="380fa-331">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="380fa-332">Det kan være, at beslutningen f.eks. skal være truffet senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="380fa-332">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="380fa-333">Hvis tidsfristen overskrides, træffes beslutningen automatisk af systemet.</span><span class="sxs-lookup"><span data-stu-id="380fa-333">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="380fa-334">Vælg den indstilling, som systemet skal vælge, på listen **Handling**.</span><span class="sxs-lookup"><span data-stu-id="380fa-334">In the **Action** list, select the option that the system should select.</span></span>
