---
title: Konfigurere manuelle beslutninger i en arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en manuel beslutning.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 192101
ms.assetid: 0bccad77-1a44-4f08-967b-12c62c02afc7
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d09e99a5bf99593a8fa7682f9d4f29eaa4e7c836
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1569353"
---
# <a name="configure-manual-decisions-in-a-workflow"></a><span data-ttu-id="ce55d-103">Konfigurere manuelle beslutninger i en arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ce55d-103">Configure manual decisions in a workflow</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="ce55d-104">I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en manuel beslutning.</span><span class="sxs-lookup"><span data-stu-id="ce55d-104">This topic explains how to configure the properties of a manual decision.</span></span>

<span data-ttu-id="ce55d-105">Hvis du vil konfigurere en manuel beslutning i arbejdsgangseditoren, skal du højreklikke på den manuelle beslutning og derefter klikke på **Egenskaber** for at åbne formularen **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-105">To configure a manual decision in the workflow editor, right-click the manual decision, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="ce55d-106">Brug derefter nedenstående procedure for at konfigurere egenskaberne for den manuelle beslutning.</span><span class="sxs-lookup"><span data-stu-id="ce55d-106">Then use the following procedures to configure the properties of the manual decision.</span></span>

## <a name="name-the-decision"></a><span data-ttu-id="ce55d-107">Navngive beslutningen</span><span class="sxs-lookup"><span data-stu-id="ce55d-107">Name the decision</span></span>

<span data-ttu-id="ce55d-108">Udfør følgende trin for at angive et navn på den manuelle beslutning.</span><span class="sxs-lookup"><span data-stu-id="ce55d-108">Follow these steps to enter a name for the manual decision.</span></span>

1. <span data-ttu-id="ce55d-109">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="ce55d-109">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ce55d-110">Angiv et entydigt navn på den manuelle beslutning i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-110">In the **Name** field, enter a unique name for the manual decision.</span></span>

## <a name="enter-a-subject-line-and-instructions"></a><span data-ttu-id="ce55d-111">Angive en emnelinje og instruktioner</span><span class="sxs-lookup"><span data-stu-id="ce55d-111">Enter a subject line and instructions</span></span>

<span data-ttu-id="ce55d-112">Du skal angive en emnelinje og instruktioner til brugere, som har fået den manuelle beslutning tildelt.</span><span class="sxs-lookup"><span data-stu-id="ce55d-112">You must provide a subject line and instructions to users who are assigned to the manual decision.</span></span> <span data-ttu-id="ce55d-113">Hvis du f.eks. konfigurerer en beslutning for indkøbsrekvisitioner, ser den bruger, der har fået beslutningen tildelt, emnelinjen og instruktionerne på siden **Indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-113">For example, if you're configuring a decision for purchase requisitions, the user who is assigned to the decision sees the subject line and instructions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="ce55d-114">Emnelinjen vises i en meddelelseslinje på siden.</span><span class="sxs-lookup"><span data-stu-id="ce55d-114">The subject line appears in a message bar on the page.</span></span> <span data-ttu-id="ce55d-115">Brugeren kan derefter klikke på ikonet på meddelelseslinjen for at få vist detaljerede instruktioner.</span><span class="sxs-lookup"><span data-stu-id="ce55d-115">The user can then click the icon in the message bar to view the instructions.</span></span> <span data-ttu-id="ce55d-116">Udfør følgende trin for at angive en emnelinje og instruktioner.</span><span class="sxs-lookup"><span data-stu-id="ce55d-116">Follow these steps to enter a subject line and instructions.</span></span>

1. <span data-ttu-id="ce55d-117">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="ce55d-117">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ce55d-118">På fanen **Instruktioner** i feltet **Emne for workflowopgave** skal du indtaste emnelinjen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-118">On the **Instructions** tab, in the **Work item subject** field, enter the subject line.</span></span>
3. <span data-ttu-id="ce55d-119">Hvis du vil personalisere emnelinjen, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="ce55d-119">To personalize the subject line, you can insert placeholders.</span></span> <span data-ttu-id="ce55d-120">Pladsholderne erstattes med de relevante data, når emnelinjen vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="ce55d-120">Placeholders are replaced with appropriate data when the subject line is shown to users.</span></span> <span data-ttu-id="ce55d-121">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="ce55d-121">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ce55d-122">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="ce55d-122">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ce55d-123">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-123">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ce55d-124">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="ce55d-124">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ce55d-125">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-125">Click **Insert**.</span></span>

4. <span data-ttu-id="ce55d-126">Følg disse trin for at tilføje oversættelser af emnelinjen:</span><span class="sxs-lookup"><span data-stu-id="ce55d-126">To add translations of the subject line, follow these steps:</span></span>

    1. <span data-ttu-id="ce55d-127">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-127">Click **Translations**.</span></span>
    2. <span data-ttu-id="ce55d-128">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="ce55d-128">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ce55d-129">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="ce55d-129">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ce55d-130">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-130">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ce55d-131">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 3.</span><span class="sxs-lookup"><span data-stu-id="ce55d-131">To personalize the text, you can insert placeholders as described in step 3.</span></span>
    6. <span data-ttu-id="ce55d-132">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-132">Click **Close**.</span></span>

5. <span data-ttu-id="ce55d-133">I feltet **Emne for workflowopgave** skal du indtaste instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="ce55d-133">In the **Work item instructions** field, enter the instructions.</span></span>
6. <span data-ttu-id="ce55d-134">Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="ce55d-134">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="ce55d-135">Pladsholderne erstattes med de relevante data, når instruktionerne vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="ce55d-135">Placeholders are replaced with appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="ce55d-136">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="ce55d-136">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ce55d-137">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="ce55d-137">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ce55d-138">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-138">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ce55d-139">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="ce55d-139">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ce55d-140">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-140">Click **Insert**.</span></span>

7. <span data-ttu-id="ce55d-141">Følg disse trin for at tilføje oversættelser af instruktionerne:</span><span class="sxs-lookup"><span data-stu-id="ce55d-141">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="ce55d-142">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-142">Click **Translations**.</span></span>
    2. <span data-ttu-id="ce55d-143">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="ce55d-143">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ce55d-144">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="ce55d-144">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ce55d-145">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-145">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ce55d-146">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 6.</span><span class="sxs-lookup"><span data-stu-id="ce55d-146">To personalize the text, you can insert placeholders as described in step 6.</span></span>
    6. <span data-ttu-id="ce55d-147">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-147">Click **Close**.</span></span>

## <a name="specify-the-possible-outcomes-of-a-decision"></a><span data-ttu-id="ce55d-148">Angive mulige udfald af en beslutning</span><span class="sxs-lookup"><span data-stu-id="ce55d-148">Specify the possible outcomes of a decision</span></span>

<span data-ttu-id="ce55d-149">Når et dokument tildeles en beslutningstager, får beslutningstageren typisk stillet et spørgsmål.</span><span class="sxs-lookup"><span data-stu-id="ce55d-149">Typically, when a document is assigned to a decision maker, the decision maker is asked a question.</span></span> <span data-ttu-id="ce55d-150">Svaret på spørgsmålet er normalt **Ja** eller **Nej**, **Sand** eller **Falsk**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-150">The answer to this question is usually **Yes** or **No**, or **True** or **False**.</span></span> <span data-ttu-id="ce55d-151">Udfør følgende trin for at angive det mulige udfald af den manuelle beslutning.</span><span class="sxs-lookup"><span data-stu-id="ce55d-151">Follow these steps to specify the possible outcomes of the manual decision.</span></span>

1. <span data-ttu-id="ce55d-152">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="ce55d-152">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="ce55d-153">Indtast navnet på udfaldet eller indstillingen på fanen **Udfald** i feltet **Udfald 1**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-153">On the **Outcomes** tab, in the **Outcome 1** field, enter the name of the outcome, or the option.</span></span>
3. <span data-ttu-id="ce55d-154">Følg disse trin for at tilføje oversættelser af udfaldet:</span><span class="sxs-lookup"><span data-stu-id="ce55d-154">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="ce55d-155">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-155">Click **Translations**.</span></span>
    2. <span data-ttu-id="ce55d-156">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="ce55d-156">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ce55d-157">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="ce55d-157">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ce55d-158">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-158">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ce55d-159">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-159">Click **Close**.</span></span>

4. <span data-ttu-id="ce55d-160">Indtast navnet på udfaldet eller indstillingen i feltet **Udfald 2**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-160">In the **Outcome 2** field, enter the name of the outcome, or the option.</span></span>
5. <span data-ttu-id="ce55d-161">Følg disse trin for at tilføje oversættelser af udfaldet:</span><span class="sxs-lookup"><span data-stu-id="ce55d-161">To add translations of the outcome, follow these steps:</span></span>

    1. <span data-ttu-id="ce55d-162">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-162">Click **Translations**.</span></span>
    2. <span data-ttu-id="ce55d-163">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="ce55d-163">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ce55d-164">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="ce55d-164">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ce55d-165">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-165">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ce55d-166">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-166">Click **Close**.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="ce55d-167">Angive, hvornår beskeder sendes</span><span class="sxs-lookup"><span data-stu-id="ce55d-167">Specify when notifications are sent</span></span>

<span data-ttu-id="ce55d-168">Du kan sende beskeder til personer, når en beslutning er truffet, delegeret videre eller eskaleret.</span><span class="sxs-lookup"><span data-stu-id="ce55d-168">You can send notifications to people when a decision has been made, delegated, or escalated.</span></span> <span data-ttu-id="ce55d-169">Udfør følgende trin for at angive, hvornår der sendes beskeder, og hvem beskederne sendes til.</span><span class="sxs-lookup"><span data-stu-id="ce55d-169">Follow these steps to specify when notifications are sent, and who the notifications are sent to.</span></span>

1. <span data-ttu-id="ce55d-170">Klik på **Beskeder** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="ce55d-170">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="ce55d-171">Markér afkrydsningsfeltet ud for de hændelser, som beskederne udsendes i forbindelse med.</span><span class="sxs-lookup"><span data-stu-id="ce55d-171">Select the check box next to the events that notifications should be sent for:</span></span>

    - <span data-ttu-id="ce55d-172">**\[Valg 1\]** – Den bruger, der er tildelt beskeden, har valgt **\[Valg 1\]**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-172">**\[Choice 1\]** – The assigned user has selected **\[Choice 1\]**.</span></span>
    - <span data-ttu-id="ce55d-173">**\[Valg 2\]** – Den bruger, der er tildelt beskeden, har valgt **\[Valg 2\]**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-173">**\[Choice 2\]** – The assigned user has selected **\[Choice 2\]**.</span></span>
    - <span data-ttu-id="ce55d-174">**Deleger** – Den bruger, der er tildelt beslutningen, har tildelt den til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="ce55d-174">**Delegate** – The assigned user has assigned the decision to another user.</span></span>
    - <span data-ttu-id="ce55d-175">**Eskaler** – Den bruger, der har fået tildelt beslutningen, har ikke truffet beslutningen inden for den tildelte tid.</span><span class="sxs-lookup"><span data-stu-id="ce55d-175">**Escalate** – The assigned user hasn't made the decision in the allotted time.</span></span>

3. <span data-ttu-id="ce55d-176">Vælg rækken for den hændelse, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="ce55d-176">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="ce55d-177">Indtast teksten til beskeden i tekstfeltet på fanen **Beskedtekst**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-177">On the **Notification text** tab, in the text box, enter the text of the notification.</span></span>
5. <span data-ttu-id="ce55d-178">Hvis du vil personalisere beskeden, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="ce55d-178">To personalize the notification, you can insert placeholders.</span></span> <span data-ttu-id="ce55d-179">Pladsholderne erstattes med de relevante data, når beskeden vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="ce55d-179">Placeholders are replaced with appropriate data when the notification is show to users.</span></span> <span data-ttu-id="ce55d-180">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="ce55d-180">Follow these steps to insert a placeholder:</span></span>

    1. <span data-ttu-id="ce55d-181">I tekstboksen skal du klikke på det sted, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="ce55d-181">In the text box, click where the placeholder should appear.</span></span>
    2. <span data-ttu-id="ce55d-182">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-182">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="ce55d-183">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="ce55d-183">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="ce55d-184">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-184">Click **Insert**.</span></span>

6. <span data-ttu-id="ce55d-185">Følg disse trin for at tilføje oversættelser af beskeden:</span><span class="sxs-lookup"><span data-stu-id="ce55d-185">To add translations of the notification, follow these steps:</span></span>

    1. <span data-ttu-id="ce55d-186">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-186">Click **Translations**.</span></span>
    2. <span data-ttu-id="ce55d-187">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="ce55d-187">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="ce55d-188">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="ce55d-188">In the list that appears, select the language that you're entering the text in.</span></span>
    4. <span data-ttu-id="ce55d-189">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-189">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="ce55d-190">Hvis du vil tilpasse teksten, kan du indsætte pladsholdere som beskrevet i trin 5.</span><span class="sxs-lookup"><span data-stu-id="ce55d-190">To personalize the text, you can insert placeholders as described in step 5.</span></span>
    6. <span data-ttu-id="ce55d-191">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-191">Click **Close**.</span></span>

7. <span data-ttu-id="ce55d-192">På fanen **Modtager** skal du angive, hvem beskederne skal sendes til.</span><span class="sxs-lookup"><span data-stu-id="ce55d-192">On the **Recipient** tab, specify who the notifications are sent to.</span></span> <span data-ttu-id="ce55d-193">Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 8.</span><span class="sxs-lookup"><span data-stu-id="ce55d-193">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 8.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ce55d-194">Indstilling</span><span class="sxs-lookup"><span data-stu-id="ce55d-194">Option</span></span></th>
    <th><span data-ttu-id="ce55d-195">Modtagere af besked</span><span class="sxs-lookup"><span data-stu-id="ce55d-195">Notification recipients</span></span></th>
    <th><span data-ttu-id="ce55d-196">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="ce55d-196">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ce55d-197">Deltager</span><span class="sxs-lookup"><span data-stu-id="ce55d-197">Participant</span></span></td>
    <td><span data-ttu-id="ce55d-198">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="ce55d-198">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ce55d-199">Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</span><span class="sxs-lookup"><span data-stu-id="ce55d-199">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="ce55d-200">Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-200">In the <strong>Participant</strong> list, select the group or to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ce55d-201">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="ce55d-201">Workflow user</span></span></td>
    <td><span data-ttu-id="ce55d-202">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ce55d-202">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ce55d-203">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-203">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ce55d-204">Bruger</span><span class="sxs-lookup"><span data-stu-id="ce55d-204">User</span></span></td>
    <td><span data-ttu-id="ce55d-205">Specifikke Microsoft Dynamics 365 for Finance and Operations-brugere</span><span class="sxs-lookup"><span data-stu-id="ce55d-205">Specific Microsoft Dynamics 365 for Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ce55d-206">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-206">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ce55d-207">Listen <strong>Tilgængelige brugere</strong> vises alle Finance and Operations-brugere.</span><span class="sxs-lookup"><span data-stu-id="ce55d-207">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="ce55d-208">Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-208">Select the users to send notifications to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="ce55d-209">Gentag trin 3 til 7 for hver af de hændelser, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="ce55d-209">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="assign-a-decision"></a><span data-ttu-id="ce55d-210">Tildele en beslutning</span><span class="sxs-lookup"><span data-stu-id="ce55d-210">Assign a decision</span></span>

<span data-ttu-id="ce55d-211">Udfør følgende trin for at angive, hvem en manuel beslutning skal tildeles til.</span><span class="sxs-lookup"><span data-stu-id="ce55d-211">Follow these steps to specify who a manual decision should be assigned to.</span></span>

1. <span data-ttu-id="ce55d-212">Klik på **Tildeling** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="ce55d-212">In the left pane, click **Assignment**.</span></span>
2. <span data-ttu-id="ce55d-213">Vælg en af indstillingerne i følgende tabel under fanen **Tildelingstype**, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 3.</span><span class="sxs-lookup"><span data-stu-id="ce55d-213">On the **Assignment type** tab, select one of the options in the following table, and then follow the additional steps for that option before you go to step 3.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ce55d-214">Indstilling</span><span class="sxs-lookup"><span data-stu-id="ce55d-214">Option</span></span></th>
    <th><span data-ttu-id="ce55d-215">Brugere, som beslutningen tildeles</span><span class="sxs-lookup"><span data-stu-id="ce55d-215">Users that the decision is assigned to</span></span></th>
    <th><span data-ttu-id="ce55d-216">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="ce55d-216">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ce55d-217">Deltager</span><span class="sxs-lookup"><span data-stu-id="ce55d-217">Participant</span></span></td>
    <td><span data-ttu-id="ce55d-218">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="ce55d-218">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ce55d-219">Når du har valgt <strong>Deltager</strong> under fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong>, skal du vælge den type gruppe eller rolle, du vil tildele beslutningen til.</span><span class="sxs-lookup"><span data-stu-id="ce55d-219">After you select <strong>Participant</strong>, on the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to assign the decision to.</span></span></li>
    <li><span data-ttu-id="ce55d-220">Vælg den type gruppe eller rolle, som beslutningen skal tildeles til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-220">In the <strong>Participant</strong> list, select the group or role to assign the decision to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ce55d-221">Hierarki</span><span class="sxs-lookup"><span data-stu-id="ce55d-221">Hierarchy</span></span></td>
    <td><span data-ttu-id="ce55d-222">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="ce55d-222">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ce55d-223">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil tildele beslutningen til.</span><span class="sxs-lookup"><span data-stu-id="ce55d-223">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to assign the decision to.</span></span></li>
    <li><span data-ttu-id="ce55d-224">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-224">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="ce55d-225">Disse navne repræsenterer de brugere, som beslutningen kan tildeles til.</span><span class="sxs-lookup"><span data-stu-id="ce55d-225">These names represent users that the decision can be assigned to.</span></span> <span data-ttu-id="ce55d-226">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="ce55d-226">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="ce55d-227">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-227">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="ce55d-228">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-228">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="ce55d-229">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="ce55d-229">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="ce55d-230">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet beslutningen skal tildeles:</span><span class="sxs-lookup"><span data-stu-id="ce55d-230">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be assigned to:</span></span> <ul>
    <li><span data-ttu-id="ce55d-231"><strong>Tildel til alle hentede brugere</strong> – Beslutningen tildeles alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-231"><strong>Assign to all users retrieved</strong> – The decision is assigned to all users in the range.</span></span></li>
    <li><span data-ttu-id="ce55d-232"><strong>Tildel kun til den sidst hentede bruger</strong> – Beslutningen tildeles kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-232"><strong>Assign only to last user retrieved</strong> – The decision is assigned to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="ce55d-233"><strong>Udeluk brugere med følgende betingelse</strong> – Beslutningen tildeles ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="ce55d-233"><strong>Exclude users with the following condition</strong> – The decision isn't assigned to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="ce55d-234">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-234">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ce55d-235">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="ce55d-235">Workflow user</span></span></td>
    <td><span data-ttu-id="ce55d-236">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ce55d-236">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ce55d-237">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-237">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ce55d-238">Bruger</span><span class="sxs-lookup"><span data-stu-id="ce55d-238">User</span></span></td>
    <td><span data-ttu-id="ce55d-239">Bestemte Finance and Operations-brugere</span><span class="sxs-lookup"><span data-stu-id="ce55d-239">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ce55d-240">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-240">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ce55d-241">Listen <strong>Tilgængelige brugere</strong> vises alle Finance and Operations-brugere.</span><span class="sxs-lookup"><span data-stu-id="ce55d-241">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="ce55d-242">Vælg de brugere, der skal tildeles beslutningen, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-242">Select the users to assign the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ce55d-243">Kø</span><span class="sxs-lookup"><span data-stu-id="ce55d-243">Queue</span></span></td>
    <td><span data-ttu-id="ce55d-244">En workflowopgavekø</span><span class="sxs-lookup"><span data-stu-id="ce55d-244">A work item queue</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ce55d-245">Når du har valgt <strong>Kø</strong>, skal du klikke på fanen <strong>Købaseret</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-245">After you select <strong>Queue</strong>, click the <strong>Queue based</strong> tab.</span></span></li>
    <li><span data-ttu-id="ce55d-246">Udfør følgende trin for at tildele beslutningen til en bestemt kø:</span><span class="sxs-lookup"><span data-stu-id="ce55d-246">To assign the decision to a specific queue, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="ce55d-247">På listen <strong>Køtype</strong> skal du vælge <strong>Workflowopgavekøer</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-247">In the <strong>Queue type</strong> list, select <strong>Work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="ce55d-248">Vælg køen på listen <strong>Kønavn</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-248">In the <strong>Queue name</strong> list, select the queue.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="ce55d-249">Hvis en bestemt betingelse skal være afgørende for, hvilken kø beslutningen tildeles til, skal du udføre følgende trin:</span><span class="sxs-lookup"><span data-stu-id="ce55d-249">If a specific condition should determine which queue the decision is assigned to, follow these steps:</span></span> <ol>
    <li><span data-ttu-id="ce55d-250">På listen <strong>Køtype</strong> skal du vælge <strong>Betingede workflowopgavekøer</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-250">In the <strong>Queue type</strong> list, select <strong>Conditional work item queues</strong>.</span></span></li>
    <li><span data-ttu-id="ce55d-251">På listen <strong>Kønavn</strong> skal du vælge <strong>Betinget kø</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-251">In the <strong>Queue name</strong> list, select <strong>Conditional queue</strong>.</span></span></li>
    </ol>
    </li>
    </ol>
    <blockquote>[!NOTE] <span data-ttu-id="ce55d-252">Denne indstilling bruges kun til nogle få arbejdsgange som f.eks. Sagsstyring.</span><span class="sxs-lookup"><span data-stu-id="ce55d-252">This option is used for only a few workflows, such as Case management.</span></span></blockquote>
    </td>
    </tr>
    </tbody>
    </table>

3. <span data-ttu-id="ce55d-253">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-253">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="ce55d-254">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="ce55d-254">Select one of the following options:</span></span>

    - <span data-ttu-id="ce55d-255">**Timer** – Angiv det antal timer, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-255">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="ce55d-256">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="ce55d-256">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ce55d-257">**Dage** – Angiv det antal dage, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-257">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="ce55d-258">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="ce55d-258">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ce55d-259">**Uger** – Angiv det antal uger, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-259">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="ce55d-260">**Måneder** – Vælg den dag og uge, hvor brugeren senest skal have truffet beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-260">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="ce55d-261">Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="ce55d-261">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ce55d-262">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have truffet beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-262">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="ce55d-263">Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="ce55d-263">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

    <span data-ttu-id="ce55d-264">Hvis brugeren ikke træffer beslutningen inden for den tildelte tid, er beslutningen forsinket.</span><span class="sxs-lookup"><span data-stu-id="ce55d-264">If the user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="ce55d-265">En forsinket beslutning eskaleres ud fra de indstillinger, du vælger i området **Eskalering** på siden.</span><span class="sxs-lookup"><span data-stu-id="ce55d-265">A decision that is overdue is escalated, based on the options that you select in the **Escalation** area of the page.</span></span>

## <a name="specify-what-happens-when-a-decision-is-overdue"></a><span data-ttu-id="ce55d-266">Angive, hvad der sker, når en beslutning er forsinket.</span><span class="sxs-lookup"><span data-stu-id="ce55d-266">Specify what happens when a decision is overdue</span></span>

<span data-ttu-id="ce55d-267">Hvis en bruger ikke træffer beslutningen inden for den tildelte tid, er beslutningen forsinket.</span><span class="sxs-lookup"><span data-stu-id="ce55d-267">If a user doesn't make the decision in the allotted time, the decision is overdue.</span></span> <span data-ttu-id="ce55d-268">En beslutning, der er forfalden, kan eskaleres eller tildeles automatisk til en anden bruger.</span><span class="sxs-lookup"><span data-stu-id="ce55d-268">A decision that is overdue can be escalated, or automatically assigned to another user.</span></span> <span data-ttu-id="ce55d-269">Udfør følgende trin for at eskalere beslutningen, hvis den er forsinket.</span><span class="sxs-lookup"><span data-stu-id="ce55d-269">Follow these steps to escalate the decision if it's overdue.</span></span>

1. <span data-ttu-id="ce55d-270">Klik på **Eskalering** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="ce55d-270">In the left pane, click **Escalation**.</span></span>
2. <span data-ttu-id="ce55d-271">Markér afkrydsningsfeltet **Brug eskaleringssti** for at oprette en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="ce55d-271">Select the **Use escalation path** check box to create an escalation path.</span></span> <span data-ttu-id="ce55d-272">De brugere, der er angivet i eskaleringsstien, tildeles automatisk beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-272">The system automatically assigns the decision to the users who are listed in the escalation path.</span></span> <span data-ttu-id="ce55d-273">Følgende tabel repræsenterer f.eks. en eskaleringssti.</span><span class="sxs-lookup"><span data-stu-id="ce55d-273">For example, the following table represents an escalation path.</span></span>

    | <span data-ttu-id="ce55d-274">Forløb</span><span class="sxs-lookup"><span data-stu-id="ce55d-274">Sequence</span></span> | <span data-ttu-id="ce55d-275">Eskaleringssti</span><span class="sxs-lookup"><span data-stu-id="ce55d-275">Escalation path</span></span>            |
    |----------|----------------------------|
    | <span data-ttu-id="ce55d-276">1</span><span class="sxs-lookup"><span data-stu-id="ce55d-276">1</span></span>        | <span data-ttu-id="ce55d-277">Knyt til: Anna</span><span class="sxs-lookup"><span data-stu-id="ce55d-277">Assign to: Donna</span></span>           |
    | <span data-ttu-id="ce55d-278">2</span><span class="sxs-lookup"><span data-stu-id="ce55d-278">2</span></span>        | <span data-ttu-id="ce55d-279">Knyt til: Erik</span><span class="sxs-lookup"><span data-stu-id="ce55d-279">Assign to: Erin</span></span>            |
    | <span data-ttu-id="ce55d-280">3</span><span class="sxs-lookup"><span data-stu-id="ce55d-280">3</span></span>        | <span data-ttu-id="ce55d-281">Sluthandling: \[Valg 1\]</span><span class="sxs-lookup"><span data-stu-id="ce55d-281">Final action: \[Choice 1\]</span></span> |

    <span data-ttu-id="ce55d-282">I dette eksempel tildeles den forsinkede beslutning automatisk til Anna.</span><span class="sxs-lookup"><span data-stu-id="ce55d-282">In this example, the system assigns the overdue decision to Donna.</span></span> <span data-ttu-id="ce55d-283">Hvis Anna ikke træffer beslutningen inden for den tildelte tid, tildeles beslutningen automatisk til Erik.</span><span class="sxs-lookup"><span data-stu-id="ce55d-283">If Donna doesn't make the decision in the allotted time, the system assigns the decision to Erin.</span></span> <span data-ttu-id="ce55d-284">Hvis Erik ikke træffer beslutningen inden for den tildelte tid, vælges **\[[Valg 1\]** automatisk som beslutning.</span><span class="sxs-lookup"><span data-stu-id="ce55d-284">If Erin doesn't make the decision in the allotted time, the system selects **\[Choice 1\]** as the decision.</span></span>

3. <span data-ttu-id="ce55d-285">Klik på **Tilføj eskalering** for at føje en bruger til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="ce55d-285">To add a user to the escalation path, click **Add escalation**.</span></span> <span data-ttu-id="ce55d-286">Vælg en af indstillingerne i følgende tabel, og udfør derefter de ekstra trin for den pågældende indstilling, før du går videre til trin 4.</span><span class="sxs-lookup"><span data-stu-id="ce55d-286">Select one of the options in the following table, and then follow the additional steps for that option before you go to step 4.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="ce55d-287">Indstilling</span><span class="sxs-lookup"><span data-stu-id="ce55d-287">Option</span></span></th>
    <th><span data-ttu-id="ce55d-288">Brugere, som beslutningen eskaleres til</span><span class="sxs-lookup"><span data-stu-id="ce55d-288">Users that the decision is escalated to</span></span></th>
    <th><span data-ttu-id="ce55d-289">Ekstra trin</span><span class="sxs-lookup"><span data-stu-id="ce55d-289">Additional steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="ce55d-290">Hierarki</span><span class="sxs-lookup"><span data-stu-id="ce55d-290">Hierarchy</span></span></td>
    <td><span data-ttu-id="ce55d-291">Brugere i et bestemt organisationshierarki</span><span class="sxs-lookup"><span data-stu-id="ce55d-291">Users in a specific organizational hierarchy</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ce55d-292">Når du har valgt <strong>Hierarki</strong> under fanen <strong>Hierarkivalg</strong> på listen <strong>Hierarkitype</strong>, skal du vælge den type hierarki, du vil eskalere beslutningen til.</span><span class="sxs-lookup"><span data-stu-id="ce55d-292">After you select <strong>Hierarchy</strong>, on the <strong>Hierarchy selection</strong> tab, in the <strong>Hierarchy type</strong> list, select the type of hierarchy to escalate the decision to.</span></span></li>
    <li><span data-ttu-id="ce55d-293">Systemet skal hente et interval af brugernavne fra hierarkiet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-293">The system must retrieve a range of user names from the hierarchy.</span></span> <span data-ttu-id="ce55d-294">Disse navne repræsenterer de brugere, som beslutningen kan eskaleres til.</span><span class="sxs-lookup"><span data-stu-id="ce55d-294">These names represent users that the decision can be escalated to.</span></span> <span data-ttu-id="ce55d-295">Udfør følgende trin for at angive startpunktet og slutpunktet for intervallet af de brugernavne, som systemet henter:</span><span class="sxs-lookup"><span data-stu-id="ce55d-295">Follow these steps to specify the starting point and ending point of the range of user names that the system retrieves:</span></span> <ol>
    <li><span data-ttu-id="ce55d-296">Vælg en person på listen <strong>Start fra</strong> for at angive startpunktet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-296">To specify the starting point, select a person in the <strong>Start from</strong> list.</span></span></li>
    <li><span data-ttu-id="ce55d-297">Klik på <strong>Tilføj betingelse</strong> for at angive slutpunktet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-297">To specify the ending point, click <strong>Add condition</strong>.</span></span> <span data-ttu-id="ce55d-298">Angiv derefter en betingelse for at bestemme, hvor i hierarkiet systemet skal stoppe med at hente navne.</span><span class="sxs-lookup"><span data-stu-id="ce55d-298">Then enter a condition that determines where in the hierarchy the system stops retrieving names.</span></span></li>
    </ol>
    </li>
    <li><span data-ttu-id="ce55d-299">På fanen <strong>Hierarkiindstillinger</strong> skal du angive, hvilke brugere i intervallet beslutningen skal eskaleres til:</span><span class="sxs-lookup"><span data-stu-id="ce55d-299">On the <strong>Hierarchy options</strong> tab, specify which users in the range the decision should be escalated to:</span></span> <ul>
    <li><span data-ttu-id="ce55d-300"><strong>Tildel til alle hentede brugere</strong> – Beslutningen eskaleres til alle brugere i intervallet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-300"><strong>Assign to all users retrieved</strong> – The decision is escalated to all users in the range.</span></span></li>
    <li><span data-ttu-id="ce55d-301"><strong>Tildel kun til den sidst hentede bruger</strong> – Beslutningen eskaleres kun til den sidste bruger i intervallet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-301"><strong>Assign only to last user retrieved</strong> – The decision is escalated to only the last user in the range.</span></span></li>
    <li><span data-ttu-id="ce55d-302"><strong>Udeluk brugere med følgende betingelse</strong> – Beslutningen eskaleres ikke til brugere i intervallet, som opfylder en bestemt betingelse.</span><span class="sxs-lookup"><span data-stu-id="ce55d-302"><strong>Exclude users with the following condition:</strong> – The decision isn't escalated to any users in the range who meet a specific condition.</span></span> <span data-ttu-id="ce55d-303">Klik på <strong>Tilføj betingelse</strong> for at angive betingelsen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-303">Click <strong>Add condition</strong> to specify the condition.</span></span></li>
    </ul>
    </li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ce55d-304">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="ce55d-304">Workflow user</span></span></td>
    <td><span data-ttu-id="ce55d-305">Brugere i den aktuelle arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="ce55d-305">Users in the current workflow</span></span></td>
    <td>
    <ul>
    <li><span data-ttu-id="ce55d-306">Når du har valgt <strong>Arbejdsgangbruger</strong> på fanen <strong>Arbejdsgangbruger</strong> på listen <strong>Arbejdsgangbruger</strong>, skal du vælge en bruger, der deltager i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-306">After you select <strong>Workflow user</strong>, on the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a user who participates in the workflow.</span></span></li>
    </ul>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="ce55d-307">Bruger</span><span class="sxs-lookup"><span data-stu-id="ce55d-307">User</span></span></td>
    <td><span data-ttu-id="ce55d-308">Bestemte Finance and Operations-brugere</span><span class="sxs-lookup"><span data-stu-id="ce55d-308">Specific Finance and Operations users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="ce55d-309">Når du har valgt <strong>Bruger</strong>, skal du klikke på fanen <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-309">After you select <strong>User</strong>, click the <strong>User</strong> tab.</span></span></li>
    <li><span data-ttu-id="ce55d-310">Listen <strong>Tilgængelige brugere</strong> vises alle Finance and Operations-brugere.</span><span class="sxs-lookup"><span data-stu-id="ce55d-310">The <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="ce55d-311">Vælg de brugere, beslutningen skal eskaleres til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="ce55d-311">Select the users to escalate the decision to, and then move those users to the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

4. <span data-ttu-id="ce55d-312">På fanen **Tidsgrænse** i feltet **Varighed** skal du angive, hvor lang tid brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-312">On the **Time limit** tab, in the **Duration** field, specify how much time the user has to make the decision.</span></span> <span data-ttu-id="ce55d-313">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="ce55d-313">Select one of the following options:</span></span>

    - <span data-ttu-id="ce55d-314">**Timer** – Angiv det antal timer, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-314">**Hours** – Enter the number of hours that the user has to make the decision.</span></span> <span data-ttu-id="ce55d-315">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="ce55d-315">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ce55d-316">**Dage** – Angiv det antal dage, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-316">**Days** – Enter the number of days that the user has to make the decision.</span></span> <span data-ttu-id="ce55d-317">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="ce55d-317">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ce55d-318">**Uger** – Angiv det antal uger, som brugeren har til at træffe beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-318">**Weeks** – Enter the number of weeks that the user has to make the decision.</span></span>
    - <span data-ttu-id="ce55d-319">**Måneder** – Vælg den dag og uge, hvor brugeren senest skal have truffet beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-319">**Months** – Select the day and week that the user must make the decision by.</span></span> <span data-ttu-id="ce55d-320">Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="ce55d-320">For example, you might want the user to make the decision by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ce55d-321">**År** – Vælg den dag, uge og måned, hvor brugeren senest skal have truffet beslutningen.</span><span class="sxs-lookup"><span data-stu-id="ce55d-321">**Years** – Select the day, week, and month that the user must make the decision by.</span></span> <span data-ttu-id="ce55d-322">Det kan være, at brugeren f.eks. skal træffe beslutningen senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="ce55d-322">For example, you might want the user to make the decision by Friday of the third week of December.</span></span>

5. <span data-ttu-id="ce55d-323">Gentag trin 3 til 4 for hvert bruger, der skal føjes til eskaleringsstien.</span><span class="sxs-lookup"><span data-stu-id="ce55d-323">Repeat steps 3 through 4 for each user that should be added to the escalation path.</span></span> <span data-ttu-id="ce55d-324">Du kan ændre brugernes rækkefølge.</span><span class="sxs-lookup"><span data-stu-id="ce55d-324">You can change the order of the users.</span></span>
6. <span data-ttu-id="ce55d-325">Hvis brugerne i eskaleringsstien ikke træffer beslutningen inden for den tildelte tid, træffes beslutningen automatisk af systemet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-325">If the users in the escalation path don't make the decision in the allotted time, the system makes the decision.</span></span> <span data-ttu-id="ce55d-326">Hvis du vil angive den indstilling, som systemet vælger, skal du vælge rækken **Handling** og derefter vælge en indstilling på fanen **Sluthandling**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-326">To specify the option that the system selects, select the **Action** row, and then, on the **End action** tab, select an option.</span></span>

## <a name="set-a-time-limit"></a><span data-ttu-id="ce55d-327">Angive en tidsgrænse</span><span class="sxs-lookup"><span data-stu-id="ce55d-327">Set a time limit</span></span>

<span data-ttu-id="ce55d-328">Udfør følgende trin, hvis beslutningen skal træffes inden en bestemt tidsgrænse.</span><span class="sxs-lookup"><span data-stu-id="ce55d-328">Follow these steps if the decision must be made in a specific time.</span></span>

> [!NOTE]
> <span data-ttu-id="ce55d-329">De indstillinger, du vælger i denne procedure, overskriver de indstillinger, du har valgt i områderne **Tildeling** og **Eskalering** på siden.</span><span class="sxs-lookup"><span data-stu-id="ce55d-329">The options that you select in this procedure override the options that you selected in the **Assignment** and **Escalation** areas of the page.</span></span>

1. <span data-ttu-id="ce55d-330">Klik på **Avancerede indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="ce55d-330">In the left pane, click **Advanced settings**.</span></span>
2. <span data-ttu-id="ce55d-331">Markér afkrydsningsfeltet **Angiv en tidsgrænse for arbejdsgangselementet**</span><span class="sxs-lookup"><span data-stu-id="ce55d-331">Select the **Set a time limit for the workflow element** check box.</span></span>
3. <span data-ttu-id="ce55d-332">Angiv, hvornår beslutningen skal være truffet, i feltet **Varighed**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-332">In the **Duration** field, specify when the decision must be made.</span></span> <span data-ttu-id="ce55d-333">Vælg en af følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="ce55d-333">Select one of the following options:</span></span>

    - <span data-ttu-id="ce55d-334">**Timer** – Angiv antallet af timer.</span><span class="sxs-lookup"><span data-stu-id="ce55d-334">**Hours** – Enter the number of hours.</span></span> <span data-ttu-id="ce55d-335">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="ce55d-335">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ce55d-336">**Dage** – Angiv antallet af dage.</span><span class="sxs-lookup"><span data-stu-id="ce55d-336">**Days** – Enter the number of days.</span></span> <span data-ttu-id="ce55d-337">Vælg derefter den kalender, din organisation bruger, og angiv oplysninger om organisationens arbejdsuge.</span><span class="sxs-lookup"><span data-stu-id="ce55d-337">Then select the calendar that your organization uses, and enter information about your organization's work week.</span></span>
    - <span data-ttu-id="ce55d-338">**Uger** – Angiv antallet af uger.</span><span class="sxs-lookup"><span data-stu-id="ce55d-338">**Weeks** – Enter the number of weeks.</span></span>
    - <span data-ttu-id="ce55d-339">**Måneder** – Vælg den dag og uge, hvor beslutningen senest skal være truffet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-339">**Months** – Select the day and week that the decision must be made by.</span></span> <span data-ttu-id="ce55d-340">Det kan være, at beslutningen f.eks. skal være truffet senest fredag i den tredje uge i måneden.</span><span class="sxs-lookup"><span data-stu-id="ce55d-340">For example, you might want the decision to be made by Friday of the third week of the month.</span></span>
    - <span data-ttu-id="ce55d-341">**År** – Vælg den dag, uge og måned, hvor beslutningen senest skal være truffet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-341">**Years** – Select the day, week, and month that the decision must be made by.</span></span> <span data-ttu-id="ce55d-342">Det kan være, at beslutningen f.eks. skal være truffet senest fredag i den tredje uge i december.</span><span class="sxs-lookup"><span data-stu-id="ce55d-342">For example, you might want the decision to be made by Friday of the third week of December.</span></span>

4. <span data-ttu-id="ce55d-343">Hvis tidsfristen overskrides, træffes beslutningen automatisk af systemet.</span><span class="sxs-lookup"><span data-stu-id="ce55d-343">If the time limit is exceeded, the system makes the decision.</span></span> <span data-ttu-id="ce55d-344">Vælg den indstilling, som systemet skal vælge, på listen **Handling**.</span><span class="sxs-lookup"><span data-stu-id="ce55d-344">In the **Action** list, select the option that the system should select.</span></span>
