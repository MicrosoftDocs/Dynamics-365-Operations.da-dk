---
title: Konfigurere egenskaber for arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en arbejdsgang.
author: sericks007
manager: AnnBe
ms.date: 07/17/2018
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 76d44c472989a73d71c2edd19f1187ecd09827ae
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/27/2019
ms.locfileid: "2190114"
---
# <a name="configure-workflow-properties"></a><span data-ttu-id="c6a02-103">Konfigurere egenskaber for arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c6a02-103">Configure workflow properties</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="c6a02-104">I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="c6a02-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="c6a02-105">Du kan konfigurere egenskaberne for en arbejdsgang ved at åbne arbejdsgangen i arbejdsgangseditoren.</span><span class="sxs-lookup"><span data-stu-id="c6a02-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="c6a02-106">Klik på lærredet i arbejdsgangseditoren, og klik derefter på **Egenskaber** for at åbne siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="c6a02-107">Du kan derefter bruge følgende procedurer til at konfigurere forskellige egenskaber for arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="c6a02-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="c6a02-108">Navngive arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="c6a02-108">Name the workflow</span></span>

<span data-ttu-id="c6a02-109">Udfør følgende trin for at angive et navn på arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="c6a02-109">Follow these steps to enter a name for the workflow.</span></span>

1. <span data-ttu-id="c6a02-110">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="c6a02-110">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c6a02-111">Angiv et entydigt navn til arbejdsgangen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="c6a02-112">Hvis du f.eks. opretter en arbejdsgang for indkøbsrekvisitioner for hvert land eller område, du opererer i, kan du navngive arbejdsgangen for indkøbsrekvisitioner **Indkøbsrekvisitioner Danmark** eller **Indkøbsrekvisitioner Spanien**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="c6a02-113">Angive ejer af arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c6a02-113">Specify the workflow owner</span></span>

<span data-ttu-id="c6a02-114">Ejeren af arbejdsgangen er den person, der administrerer og vedligeholder arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="c6a02-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="c6a02-115">Udfør følgende trin for at angive ejeren af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="c6a02-115">Follow these steps to specify the workflow owner.</span></span>

1. <span data-ttu-id="c6a02-116">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="c6a02-116">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c6a02-117">Vælg navnet på den person, der skal administrere arbejdsgangen, på listen **Ejer**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="c6a02-118">Vælge en e-mail-skabelon</span><span class="sxs-lookup"><span data-stu-id="c6a02-118">Select an email template</span></span>

<span data-ttu-id="c6a02-119">Udfør følgende trin for at vælge den mailskabelon, der skal bruges til at generere beskeder om arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="c6a02-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1. <span data-ttu-id="c6a02-120">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="c6a02-120">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c6a02-121">På listen **E-mail-skabelon til arbejdsgangsbeskeder** skal du vælge skabelonen.</span><span class="sxs-lookup"><span data-stu-id="c6a02-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="c6a02-122">Angive instruktioner til brugere</span><span class="sxs-lookup"><span data-stu-id="c6a02-122">Enter instructions for users</span></span>

<span data-ttu-id="c6a02-123">Du kan angive instruktioner til brugere, der sender dokumenter til behandling og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="c6a02-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="c6a02-124">Disse brugere kaldes også *igangsættere*.</span><span class="sxs-lookup"><span data-stu-id="c6a02-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="c6a02-125">Antag f.eks., at du opretter en arbejdsgang for indkøbsrekvisitioner, og du angiver instruktioner.</span><span class="sxs-lookup"><span data-stu-id="c6a02-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="c6a02-126">Disse instruktioner kan derefter ses af brugere, der angiver indkøbsrekvisitioner på siden **Indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="c6a02-127">Igangsætteren klikker på ikonet på arbejdsgangens meddelelseslinje for at få vist instruktioner.</span><span class="sxs-lookup"><span data-stu-id="c6a02-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="c6a02-128">Udfør følgende trin for at angive instruktioner til brugerne.</span><span class="sxs-lookup"><span data-stu-id="c6a02-128">Follow these steps to enter instructions for users.</span></span>

1. <span data-ttu-id="c6a02-129">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="c6a02-129">In the left pane, click **Basic Settings**.</span></span>
2. <span data-ttu-id="c6a02-130">I feltet **Afsendelsesinstruktioner** skal du indtaste instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="c6a02-130">In the **Submission instructions** field, enter the instructions.</span></span>
3. <span data-ttu-id="c6a02-131">Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="c6a02-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="c6a02-132">Pladsholdere erstattes med de relevante data, når instruktionerne vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="c6a02-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="c6a02-133">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="c6a02-133">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="c6a02-134">Klik et sted i feltet **Afsendelsesinstruktioner** for at angive, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="c6a02-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c6a02-135">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-135">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c6a02-136">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="c6a02-136">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c6a02-137">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-137">Click **Insert**.</span></span>

4. <span data-ttu-id="c6a02-138">Følg disse trin for at tilføje oversættelser af instruktionerne:</span><span class="sxs-lookup"><span data-stu-id="c6a02-138">To add translations of the instructions, follow these steps:</span></span>

    1. <span data-ttu-id="c6a02-139">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-139">Click **Translations**.</span></span>
    2. <span data-ttu-id="c6a02-140">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="c6a02-140">On the page that appears, click **Add**.</span></span>
    3. <span data-ttu-id="c6a02-141">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="c6a02-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="c6a02-142">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-142">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="c6a02-143">Hvis du vil personalisere teksten, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="c6a02-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c6a02-144">I trin 3 kan du se anvisninger i, hvordan du angiver en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="c6a02-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6. <span data-ttu-id="c6a02-145">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="c6a02-146">Angive, hvornår denne arbejdsgang bruges</span><span class="sxs-lookup"><span data-stu-id="c6a02-146">Specify when this workflow is used</span></span>

<span data-ttu-id="c6a02-147">Du kan oprette flere arbejdsgange, der er baseret på samme type.</span><span class="sxs-lookup"><span data-stu-id="c6a02-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="c6a02-148">Du kan f.eks. oprette en arbejdsgang for indkøbsrekvisitioner for hvert land eller område, som du opererer i, f.eks. Indkøbsrekvisitioner Danmark eller Indkøbsrekvisitioner Spanien.</span><span class="sxs-lookup"><span data-stu-id="c6a02-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="c6a02-149">Når der findes flere arbejdsgange, der er baseret på samme type, skal du angive, hvornår den enkelte arbejdsgang bruges.</span><span class="sxs-lookup"><span data-stu-id="c6a02-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="c6a02-150">I det foregående eksempel skal du angive følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="c6a02-150">For the preceding example, you specify the following conditions:</span></span>

- <span data-ttu-id="c6a02-151">Indkøbsrekvisitioner Danmark bruges når: land/område = DK</span><span class="sxs-lookup"><span data-stu-id="c6a02-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
- <span data-ttu-id="c6a02-152">Indkøbsrekvisitioner Spanien bruges når: land/område = ES</span><span class="sxs-lookup"><span data-stu-id="c6a02-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="c6a02-153">Udfør følgende trin for at angive, hvornår den arbejdsgang, du konfigurerer, skal bruges.</span><span class="sxs-lookup"><span data-stu-id="c6a02-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1. <span data-ttu-id="c6a02-154">Klik på **Aktivering** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="c6a02-154">In the left pane, click **Activation**.</span></span>
2. <span data-ttu-id="c6a02-155">Markér afkrydsningsfeltet **Angiv betingelserne for at køre denne arbejdsgang**</span><span class="sxs-lookup"><span data-stu-id="c6a02-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3. <span data-ttu-id="c6a02-156">Klik på **Tilføj betingelse**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-156">Click **Add condition**.</span></span>
4. <span data-ttu-id="c6a02-157">Angiv en betingelse.</span><span class="sxs-lookup"><span data-stu-id="c6a02-157">Enter a condition.</span></span>
5. <span data-ttu-id="c6a02-158">Angiv eventuelle supplerende betingelser, hvis det er påkrævede.</span><span class="sxs-lookup"><span data-stu-id="c6a02-158">Enter any additional conditions that are required.</span></span>
6. <span data-ttu-id="c6a02-159">Hvis du vil kontrollere, at de angivne betingelser er konfigureret korrekt, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="c6a02-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>

    1. <span data-ttu-id="c6a02-160">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-160">Click **Test**.</span></span>
    2. <span data-ttu-id="c6a02-161">På siden **Test betingelse for arbejdsgang** i området **Valider betingelse**, og vælg en post.</span><span class="sxs-lookup"><span data-stu-id="c6a02-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3. <span data-ttu-id="c6a02-162">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-162">Click **Test**.</span></span> <span data-ttu-id="c6a02-163">Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="c6a02-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="c6a02-164">Hvis du f.eks. opretter en arbejdsgang for indkøbsrekvisitioner til Spanien, vises en liste over indkøbsrekvisitioner i området **Valider betingelse** på siden.</span><span class="sxs-lookup"><span data-stu-id="c6a02-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="c6a02-165">Når du klikker på **Test**, evaluerer systemet den markerede indkøbsrekvisition for at finde ud af, om land/område er ES.</span><span class="sxs-lookup"><span data-stu-id="c6a02-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4. <span data-ttu-id="c6a02-166">Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="c6a02-167">Angive, hvornår beskeder sendes</span><span class="sxs-lookup"><span data-stu-id="c6a02-167">Specify when notifications are sent</span></span>

<span data-ttu-id="c6a02-168">Når et dokument sendes til behandling, oprettes en arbejdsgangsforekomst.</span><span class="sxs-lookup"><span data-stu-id="c6a02-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="c6a02-169">Du kan sende beskeder til brugerne, når forekomster, som er baseret på arbejdsgangen, startes, fuldføres, afsluttes eller stoppes på grund af en fejl.</span><span class="sxs-lookup"><span data-stu-id="c6a02-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="c6a02-170">Udfør følgende trin til at angive, hvornår der sendes beskeder.</span><span class="sxs-lookup"><span data-stu-id="c6a02-170">Follow these steps to specify when notifications are sent.</span></span>

1. <span data-ttu-id="c6a02-171">Klik på **Beskeder** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="c6a02-171">In the left pane, click **Notifications**.</span></span>
2. <span data-ttu-id="c6a02-172">Markér afkrydsningsfeltet for hver hændelse, som skal udløse beskeder:</span><span class="sxs-lookup"><span data-stu-id="c6a02-172">Select the check box for each event that should trigger notifications:</span></span>

    - <span data-ttu-id="c6a02-173">**Startet** – Send beskeder, når en arbejdsgangsforekomst er startet.</span><span class="sxs-lookup"><span data-stu-id="c6a02-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    - <span data-ttu-id="c6a02-174">**Stoppet** – Send beskeder, når en arbejdsgangsforekomst er stoppet på grund af en fejl.</span><span class="sxs-lookup"><span data-stu-id="c6a02-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    - <span data-ttu-id="c6a02-175">**Fuldført** – Send beskeder, når en arbejdsgangsforekomst er fuldført.</span><span class="sxs-lookup"><span data-stu-id="c6a02-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    - <span data-ttu-id="c6a02-176">**Uoprettelig** – Send beskeder, når en arbejdsgangsforekomst er stoppet på grund af en uoprettelig fejl.</span><span class="sxs-lookup"><span data-stu-id="c6a02-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    - <span data-ttu-id="c6a02-177">**Afsluttet** – Send beskeder, når en arbejdsgangsforekomst er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="c6a02-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3. <span data-ttu-id="c6a02-178">Vælg rækken for den hændelse, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="c6a02-178">Select the row for an event that you selected in step 2.</span></span>
4. <span data-ttu-id="c6a02-179">Indtast teksten til beskeden på fanen **Beskedtekst**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5. <span data-ttu-id="c6a02-180">Hvis du vil personalisere teksten, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="c6a02-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c6a02-181">Pladsholderne erstattes med de relevante data, når teksten vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="c6a02-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="c6a02-182">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="c6a02-182">To insert a placeholder, follow these steps:</span></span>

    1. <span data-ttu-id="c6a02-183">Klik i feltet for at angive, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="c6a02-183">Click in the field to specify where the placeholder should appear.</span></span>
    2. <span data-ttu-id="c6a02-184">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-184">Click **Insert placeholder**.</span></span>
    3. <span data-ttu-id="c6a02-185">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="c6a02-185">In the list that appears, select the placeholder to insert.</span></span>
    4. <span data-ttu-id="c6a02-186">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-186">Click **Insert**.</span></span>
    5. <span data-ttu-id="c6a02-187">En fælles pladsholder for **Beskedtekst**, der skal medtages, er "Seneste noter: %Workflow.Last note%", som viser alle kommentarer fra det forrige trin.</span><span class="sxs-lookup"><span data-stu-id="c6a02-187">A common **Notification text** placeholder to include is "Last Notes: %Workflow.Last note%", which displays any comments from the previous step.</span></span>

6. <span data-ttu-id="c6a02-188">Følg disse trin for at tilføje oversættelser af teksten:</span><span class="sxs-lookup"><span data-stu-id="c6a02-188">To add translations of the text, follow these steps:</span></span>

    1. <span data-ttu-id="c6a02-189">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-189">Click **Translations**.</span></span>
    2. <span data-ttu-id="c6a02-190">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="c6a02-190">On the page that appears, Click **Add**.</span></span>
    3. <span data-ttu-id="c6a02-191">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="c6a02-191">In the list that appears, select the language that you will enter the text in.</span></span>
    4. <span data-ttu-id="c6a02-192">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-192">In the **Translated text** field, enter the text.</span></span>
    5. <span data-ttu-id="c6a02-193">Hvis du vil personalisere teksten, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="c6a02-193">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="c6a02-194">I trin 5 kan du se anvisninger i, hvordan du angiver en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="c6a02-194">For instructions about how to enter a placeholder, see step 5.</span></span>
    6. <span data-ttu-id="c6a02-195">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-195">Click **Close**.</span></span>

7. <span data-ttu-id="c6a02-196">På fanen **Modtager** skal du bruge følgende indstillinger til at angive, hvem der skal modtage beskeder.</span><span class="sxs-lookup"><span data-stu-id="c6a02-196">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>

    <table>
    <thead>
    <tr>
    <th><span data-ttu-id="c6a02-197">Indstilling</span><span class="sxs-lookup"><span data-stu-id="c6a02-197">Option</span></span></th>
    <th><span data-ttu-id="c6a02-198">Beskederne sendes til disse brugere.</span><span class="sxs-lookup"><span data-stu-id="c6a02-198">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="c6a02-199">Hvis du vil sende beskeder, skal du følge disse trin</span><span class="sxs-lookup"><span data-stu-id="c6a02-199">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td><span data-ttu-id="c6a02-200">Deltager</span><span class="sxs-lookup"><span data-stu-id="c6a02-200">Participant</span></span></td>
    <td><span data-ttu-id="c6a02-201">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="c6a02-201">Users who are assigned to a specific group or role</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c6a02-202">På fanen <strong>Modtager</strong> skal du klikke på <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6a02-202">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="c6a02-203">På fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong> skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</span><span class="sxs-lookup"><span data-stu-id="c6a02-203">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="c6a02-204">Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6a02-204">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c6a02-205">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="c6a02-205">Workflow user</span></span></td>
    <td><span data-ttu-id="c6a02-206">Brugere, som deltager i denne arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="c6a02-206">Users who are participants in this workflow</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c6a02-207">På fanen <strong>Modtager</strong> skal du klikke på <strong>Arbejdsgangsbruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6a02-207">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="c6a02-208">På fanen <strong>Arbejdsgangsbruger</strong> på listen <strong>Arbejdsgangsbruger</strong> skal du vælge en deltager i denne arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="c6a02-208">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol>
    </td>
    </tr>
    <tr>
    <td><span data-ttu-id="c6a02-209">Bruger</span><span class="sxs-lookup"><span data-stu-id="c6a02-209">User</span></span></td>
    <td><span data-ttu-id="c6a02-210">Specifikke brugere</span><span class="sxs-lookup"><span data-stu-id="c6a02-210">Specific users</span></span></td>
    <td>
    <ol>
    <li><span data-ttu-id="c6a02-211">På fanen <strong>Modtager</strong> skal du klikke på <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6a02-211">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="c6a02-212">På fanen <strong>Bruger</strong> indeholder listen <strong>Tilgængelige brugere</strong> alle brugere.</span><span class="sxs-lookup"><span data-stu-id="c6a02-212">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all users.</span></span> <span data-ttu-id="c6a02-213">Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="c6a02-213">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol>
    </td>
    </tr>
    </tbody>
    </table>

8. <span data-ttu-id="c6a02-214">Gentag trin 3 til 7 for hver af de hændelser, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="c6a02-214">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="c6a02-215">Angiv kommentarer om de ændringer, du har foretaget i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="c6a02-215">Enter comments about the changes that you made to the workflow</span></span>

<span data-ttu-id="c6a02-216">Hvis du vil angive kommentarer om de ændringer, du har foretaget i arbejdsgangen, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="c6a02-216">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1. <span data-ttu-id="c6a02-217">Klik på **Noter** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="c6a02-217">In the left pane, click **Notes**.</span></span>
2. <span data-ttu-id="c6a02-218">I feltet **Angiv kommentarer om arbejdsgangen** skal du angive dine kommentarer.</span><span class="sxs-lookup"><span data-stu-id="c6a02-218">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3. <span data-ttu-id="c6a02-219">Gennemse kommentarer.</span><span class="sxs-lookup"><span data-stu-id="c6a02-219">Review your comments.</span></span> <span data-ttu-id="c6a02-220">Når du har tilføjet kommentarer, kan du ikke ændre dem.</span><span class="sxs-lookup"><span data-stu-id="c6a02-220">After you add comments, you can't modify them.</span></span>
4. <span data-ttu-id="c6a02-221">Klik på **Tilføj** til at tilføje dine kommentarer til området **Kommentarhistorik**.</span><span class="sxs-lookup"><span data-stu-id="c6a02-221">Click **Add** to add your comments to the **Comment history** area.</span></span>
