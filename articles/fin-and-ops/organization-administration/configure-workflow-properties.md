---
title: Konfigurere egenskaber for arbejdsgang
description: I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en arbejdsgang.
author: sericks007
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User, IT Pro
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.custom: 196083
ms.assetid: 192b7a98-7d04-4c7a-a986-29d797a8a837
ms.search.region: Global
ms.author: donaldc
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 19cc8f92b5bb6d9ddfdc77785e48de17ed005703
ms.openlocfilehash: 7ea35d851613a19889392400e31cf8492d5dc799
ms.contentlocale: da-dk
ms.lasthandoff: 03/23/2018

---

# <a name="configure-workflow-properties"></a><span data-ttu-id="1be54-103">Konfigurere egenskaber for arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="1be54-103">Configure workflow properties</span></span>

[!include[banner](../includes/banner.md)]


<span data-ttu-id="1be54-104">I dette emne forklares det, hvordan du konfigurerer de forskellige egenskaber for en arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="1be54-104">This topic explains how to configure the various properties of a workflow.</span></span>

<span data-ttu-id="1be54-105">Du kan konfigurere egenskaberne for en arbejdsgang ved at åbne arbejdsgangen i arbejdsgangseditoren.</span><span class="sxs-lookup"><span data-stu-id="1be54-105">To configure the properties of a workflow, open the workflow in the workflow editor.</span></span> <span data-ttu-id="1be54-106">Klik på lærredet i arbejdsgangseditoren, og klik derefter på **Egenskaber** for at åbne siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="1be54-106">Click the canvas of the workflow editor, and then click **Properties** to open the **Properties** page.</span></span> <span data-ttu-id="1be54-107">Du kan derefter bruge følgende procedurer til at konfigurere forskellige egenskaber for arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="1be54-107">You can then use the following procedures to configure the various properties of the workflow.</span></span>

## <a name="name-the-workflow"></a><span data-ttu-id="1be54-108">Navngive arbejdsgangen</span><span class="sxs-lookup"><span data-stu-id="1be54-108">Name the workflow</span></span>
<span data-ttu-id="1be54-109">Udfør følgende trin for at angive et navn på arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="1be54-109">Follow these steps to enter a name for the workflow.</span></span>

1.  <span data-ttu-id="1be54-110">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1be54-110">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="1be54-111">Angiv et entydigt navn til arbejdsgangen i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="1be54-111">In the **Name** field, enter a unique name for the workflow.</span></span> <span data-ttu-id="1be54-112">Hvis du f.eks. opretter en arbejdsgang for indkøbsrekvisitioner for hvert land eller område, du opererer i, kan du navngive arbejdsgangen for indkøbsrekvisitioner **Indkøbsrekvisitioner Danmark** eller **Indkøbsrekvisitioner Spanien**.</span><span class="sxs-lookup"><span data-stu-id="1be54-112">For example, if you create a purchase requisition workflow for each country/region that you operate in, you can name the purchase requisition workflow **Purchase Requisitions Denmark** or **Purchase Requisitions Spain**.</span></span>

## <a name="specify-the-workflow-owner"></a><span data-ttu-id="1be54-113">Angive ejer af arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="1be54-113">Specify the workflow owner</span></span>
<span data-ttu-id="1be54-114">Ejeren af arbejdsgangen er den person, der administrerer og vedligeholder arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="1be54-114">The workflow owner is the person who manages and maintains the workflow.</span></span> <span data-ttu-id="1be54-115">Udfør følgende trin for at angive ejeren af arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="1be54-115">Follow these steps to specify the workflow owner.</span></span>

1.  <span data-ttu-id="1be54-116">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1be54-116">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="1be54-117">Vælg navnet på den person, der skal administrere arbejdsgangen, på listen **Ejer**.</span><span class="sxs-lookup"><span data-stu-id="1be54-117">In the **Owner** list, select the name of the person who will manage the workflow.</span></span>

## <a name="select-an-email-template"></a><span data-ttu-id="1be54-118">Vælge en e-mail-skabelon</span><span class="sxs-lookup"><span data-stu-id="1be54-118">Select an email template</span></span>
<span data-ttu-id="1be54-119">Udfør følgende trin for at vælge den mailskabelon, der skal bruges til at generere beskeder om arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="1be54-119">Follow these steps to select the email template that is used to generate notification messages about the workflow.</span></span>

1.  <span data-ttu-id="1be54-120">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1be54-120">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="1be54-121">På listen **E-mail-skabelon til arbejdsgangsbeskeder** skal du vælge skabelonen.</span><span class="sxs-lookup"><span data-stu-id="1be54-121">In the **Email template for workflow notifications** list, select the template.</span></span>

## <a name="enter-instructions-for-users"></a><span data-ttu-id="1be54-122">Angive instruktioner til brugere</span><span class="sxs-lookup"><span data-stu-id="1be54-122">Enter instructions for users</span></span>
<span data-ttu-id="1be54-123">Du kan angive instruktioner til brugere, der sender dokumenter til behandling og godkendelse.</span><span class="sxs-lookup"><span data-stu-id="1be54-123">You can provide instructions to users who submit documents for processing and approval.</span></span> <span data-ttu-id="1be54-124">Disse brugere kaldes også *igangsættere*.</span><span class="sxs-lookup"><span data-stu-id="1be54-124">These users are also referred to as *originators*.</span></span> <span data-ttu-id="1be54-125">Antag f.eks., at du opretter en arbejdsgang for indkøbsrekvisitioner, og du angiver instruktioner.</span><span class="sxs-lookup"><span data-stu-id="1be54-125">For example, you're creating a purchase requisition workflow, and you enter instructions.</span></span> <span data-ttu-id="1be54-126">Disse instruktioner kan derefter ses af brugere, der angiver indkøbsrekvisitioner på siden **Indkøbsrekvisitioner**.</span><span class="sxs-lookup"><span data-stu-id="1be54-126">Those instructions can then be viewed by users who enter purchase requisitions on the **Purchase requisitions** page.</span></span> <span data-ttu-id="1be54-127">Igangsætteren klikker på ikonet på arbejdsgangens meddelelseslinje for at få vist instruktioner.</span><span class="sxs-lookup"><span data-stu-id="1be54-127">To view instructions, the originator clicks the icon in the workflow message bar.</span></span> <span data-ttu-id="1be54-128">Udfør følgende trin for at angive instruktioner til brugerne.</span><span class="sxs-lookup"><span data-stu-id="1be54-128">Follow these steps to enter instructions for users.</span></span>

1.  <span data-ttu-id="1be54-129">Klik på **Grundlæggende indstillinger** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1be54-129">In the left pane, click **Basic Settings**.</span></span>
2.  <span data-ttu-id="1be54-130">I feltet **Afsendelsesinstruktioner** skal du indtaste instruktionerne.</span><span class="sxs-lookup"><span data-stu-id="1be54-130">In the **Submission instructions** field, enter the instructions.</span></span>
3.  <span data-ttu-id="1be54-131">Hvis du vil personalisere instruktionerne, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="1be54-131">To personalize the instructions, you can insert placeholders.</span></span> <span data-ttu-id="1be54-132">Pladsholdere erstattes med de relevante data, når instruktionerne vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="1be54-132">Placeholders are replaced with the appropriate data when the instructions are shown to users.</span></span> <span data-ttu-id="1be54-133">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="1be54-133">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="1be54-134">Klik et sted i feltet **Afsendelsesinstruktioner** for at angive, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="1be54-134">Click in the **Submission instructions** field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="1be54-135">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="1be54-135">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="1be54-136">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="1be54-136">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="1be54-137">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="1be54-137">Click **Insert**.</span></span>

4.  <span data-ttu-id="1be54-138">Følg disse trin for at tilføje oversættelser af instruktionerne:</span><span class="sxs-lookup"><span data-stu-id="1be54-138">To add translations of the instructions, follow these steps:</span></span>
    1.  <span data-ttu-id="1be54-139">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="1be54-139">Click **Translations**.</span></span>
    2.  <span data-ttu-id="1be54-140">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="1be54-140">On the page that appears, click **Add**.</span></span>
    3.  <span data-ttu-id="1be54-141">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="1be54-141">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="1be54-142">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="1be54-142">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="1be54-143">Hvis du vil personalisere teksten, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="1be54-143">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="1be54-144">I trin 3 kan du se anvisninger i, hvordan du angiver en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="1be54-144">For instructions about how to enter a placeholder, see step 3.</span></span>
    6.  <span data-ttu-id="1be54-145">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="1be54-145">Click **Close**.</span></span>

## <a name="specify-when-this-workflow-is-used"></a><span data-ttu-id="1be54-146">Angive, hvornår denne arbejdsgang bruges</span><span class="sxs-lookup"><span data-stu-id="1be54-146">Specify when this workflow is used</span></span>
<span data-ttu-id="1be54-147">Du kan oprette flere arbejdsgange, der er baseret på samme type.</span><span class="sxs-lookup"><span data-stu-id="1be54-147">You can create multiple workflows that are based on the same type.</span></span> <span data-ttu-id="1be54-148">Du kan f.eks. oprette en arbejdsgang for indkøbsrekvisitioner for hvert land eller område, som du opererer i, f.eks. Indkøbsrekvisitioner Danmark eller Indkøbsrekvisitioner Spanien.</span><span class="sxs-lookup"><span data-stu-id="1be54-148">For example, you can create a purchase requisition workflow for each country/region that you operate in, such as Purchase Requisitions Denmark and Purchase Requisitions Spain.</span></span> <span data-ttu-id="1be54-149">Når der findes flere arbejdsgange, der er baseret på samme type, skal du angive, hvornår den enkelte arbejdsgang bruges.</span><span class="sxs-lookup"><span data-stu-id="1be54-149">When you have multiple workflows that are based on the same type, you must specify when each workflow is used.</span></span> <span data-ttu-id="1be54-150">I det foregående eksempel skal du angive følgende betingelser:</span><span class="sxs-lookup"><span data-stu-id="1be54-150">For the preceding example, you specify the following conditions:</span></span>

-   <span data-ttu-id="1be54-151">Indkøbsrekvisitioner Danmark bruges når: land/område = DK</span><span class="sxs-lookup"><span data-stu-id="1be54-151">Purchase Requisitions Denmark is used when: country/region = DK</span></span>
-   <span data-ttu-id="1be54-152">Indkøbsrekvisitioner Spanien bruges når: land/område = ES</span><span class="sxs-lookup"><span data-stu-id="1be54-152">Purchase Requisitions Spain is used when: country/region = ES</span></span>

<span data-ttu-id="1be54-153">Udfør følgende trin for at angive, hvornår den arbejdsgang, du konfigurerer, skal bruges.</span><span class="sxs-lookup"><span data-stu-id="1be54-153">Follow these steps to specify when the workflow that you're configuring is used.</span></span>

1.  <span data-ttu-id="1be54-154">Klik på **Aktivering** i venstre rude.</span><span class="sxs-lookup"><span data-stu-id="1be54-154">In the left pane, click **Activation**.</span></span>
2.  <span data-ttu-id="1be54-155">Markér afkrydsningsfeltet **Angiv betingelserne for at køre denne arbejdsgang**</span><span class="sxs-lookup"><span data-stu-id="1be54-155">Select the **Set the conditions for running this workflow** check box.</span></span>
3.  <span data-ttu-id="1be54-156">Klik på **Tilføj betingelse**.</span><span class="sxs-lookup"><span data-stu-id="1be54-156">Click **Add condition**.</span></span>
4.  <span data-ttu-id="1be54-157">Angiv en betingelse.</span><span class="sxs-lookup"><span data-stu-id="1be54-157">Enter a condition.</span></span>
5.  <span data-ttu-id="1be54-158">Angiv eventuelle supplerende betingelser, hvis det er påkrævede.</span><span class="sxs-lookup"><span data-stu-id="1be54-158">Enter any additional conditions that are required.</span></span>
6.  <span data-ttu-id="1be54-159">Hvis du vil kontrollere, at de angivne betingelser er konfigureret korrekt, skal du følge disse trin:</span><span class="sxs-lookup"><span data-stu-id="1be54-159">To verify that the conditions that you entered are set correctly, follow these steps:</span></span>
    1.  <span data-ttu-id="1be54-160">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="1be54-160">Click **Test**.</span></span>
    2.  <span data-ttu-id="1be54-161">På siden **Test betingelse for arbejdsgang** i området **Valider betingelse**, og vælg en post.</span><span class="sxs-lookup"><span data-stu-id="1be54-161">On the **Test workflow condition** page, in the **Validate condition** area, select a record.</span></span>
    3.  <span data-ttu-id="1be54-162">Klik på **Test**.</span><span class="sxs-lookup"><span data-stu-id="1be54-162">Click **Test**.</span></span> <span data-ttu-id="1be54-163">Systemet evaluerer den valgte post for at afgøre, om den opfylder de betingelser, du har angivet.</span><span class="sxs-lookup"><span data-stu-id="1be54-163">The system evaluates the record to determine whether it meets the conditions that you specified.</span></span> <span data-ttu-id="1be54-164">Hvis du f.eks. opretter en arbejdsgang for indkøbsrekvisitioner til Spanien, vises en liste over indkøbsrekvisitioner i området **Valider betingelse** på siden.</span><span class="sxs-lookup"><span data-stu-id="1be54-164">For example, if you're creating a purchase requisition workflow for Spain, the **Validate condition** area of the page shows a list of purchase requisitions.</span></span> <span data-ttu-id="1be54-165">Når du klikker på **Test**, evaluerer systemet den markerede indkøbsrekvisition for at finde ud af, om land/område er ES.</span><span class="sxs-lookup"><span data-stu-id="1be54-165">When you click **Test**, the system evaluates the selected purchase requisition to determine whether the country/region is ES.</span></span>
    4.  <span data-ttu-id="1be54-166">Klik på **OK** eller **Annuller** for at vende tilbage til siden **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="1be54-166">Click **OK** or **Cancel** to return to the **Properties** page.</span></span>

## <a name="specify-when-notifications-are-sent"></a><span data-ttu-id="1be54-167">Angive, hvornår beskeder sendes</span><span class="sxs-lookup"><span data-stu-id="1be54-167">Specify when notifications are sent</span></span>
<span data-ttu-id="1be54-168">Når et dokument sendes til behandling, oprettes en arbejdsgangsforekomst.</span><span class="sxs-lookup"><span data-stu-id="1be54-168">When a document is submitted for processing, a workflow instance is created.</span></span> <span data-ttu-id="1be54-169">Du kan sende beskeder til brugerne, når forekomster, som er baseret på arbejdsgangen, startes, fuldføres, afsluttes eller stoppes på grund af en fejl.</span><span class="sxs-lookup"><span data-stu-id="1be54-169">You can send notifications to users when workflow instances that are based on the workflow are started, completed, terminated, or stopped because of an error.</span></span> <span data-ttu-id="1be54-170">Udfør følgende trin til at angive, hvornår der sendes beskeder.</span><span class="sxs-lookup"><span data-stu-id="1be54-170">Follow these steps to specify when notifications are sent.</span></span>

1.  <span data-ttu-id="1be54-171">Klik på **Beskeder** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="1be54-171">In the left pane, click **Notifications**.</span></span>
2.  <span data-ttu-id="1be54-172">Markér afkrydsningsfeltet for hver hændelse, som skal udløse beskeder:</span><span class="sxs-lookup"><span data-stu-id="1be54-172">Select the check box for each event that should trigger notifications:</span></span>
    -   <span data-ttu-id="1be54-173">**Startet** – Send beskeder, når en arbejdsgangsforekomst er startet.</span><span class="sxs-lookup"><span data-stu-id="1be54-173">**Started** – Send notifications when a workflow instance is started.</span></span>
    -   <span data-ttu-id="1be54-174">**Stoppet** – Send beskeder, når en arbejdsgangsforekomst er stoppet på grund af en fejl.</span><span class="sxs-lookup"><span data-stu-id="1be54-174">**Stopped** – Send notifications when a workflow instance is stopped because of an error.</span></span>
    -   <span data-ttu-id="1be54-175">**Fuldført** – Send beskeder, når en arbejdsgangsforekomst er fuldført.</span><span class="sxs-lookup"><span data-stu-id="1be54-175">**Completed** – Send notifications when a workflow instance is completed.</span></span>
    -   <span data-ttu-id="1be54-176">**Uoprettelig** – Send beskeder, når en arbejdsgangsforekomst er stoppet på grund af en uoprettelig fejl.</span><span class="sxs-lookup"><span data-stu-id="1be54-176">**Unrecoverable** – Send notifications when a workflow instance is stopped because of an unrecoverable error.</span></span>
    -   <span data-ttu-id="1be54-177">**Afsluttet** – Send beskeder, når en arbejdsgangsforekomst er afsluttet.</span><span class="sxs-lookup"><span data-stu-id="1be54-177">**Terminated** – Send notifications when a workflow instance is terminated.</span></span>

3.  <span data-ttu-id="1be54-178">Vælg rækken for den hændelse, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="1be54-178">Select the row for an event that you selected in step 2.</span></span>
4.  <span data-ttu-id="1be54-179">Indtast teksten til beskeden på fanen **Beskedtekst**.</span><span class="sxs-lookup"><span data-stu-id="1be54-179">On the **Notification text** tab, enter the text of the notification.</span></span>
5.  <span data-ttu-id="1be54-180">Hvis du vil personalisere teksten, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="1be54-180">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="1be54-181">Pladsholderne erstattes med de relevante data, når teksten vises for brugerne.</span><span class="sxs-lookup"><span data-stu-id="1be54-181">Placeholders are replaced with the appropriate data when the text is shown to users.</span></span> <span data-ttu-id="1be54-182">Udfør følgende trin for at indsætte en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="1be54-182">To insert a placeholder, follow these steps:</span></span>
    1.  <span data-ttu-id="1be54-183">Klik i feltet for at angive, hvor pladsholderen skal vises.</span><span class="sxs-lookup"><span data-stu-id="1be54-183">Click in the field to specify where the placeholder should appear.</span></span>
    2.  <span data-ttu-id="1be54-184">Klik på **Indsæt pladsholder**.</span><span class="sxs-lookup"><span data-stu-id="1be54-184">Click **Insert placeholder**.</span></span>
    3.  <span data-ttu-id="1be54-185">Vælg den pladsholder, du vil indsætte, på den viste liste.</span><span class="sxs-lookup"><span data-stu-id="1be54-185">In the list that appears, select the placeholder to insert.</span></span>
    4.  <span data-ttu-id="1be54-186">Klik på **Indsæt**.</span><span class="sxs-lookup"><span data-stu-id="1be54-186">Click **Insert**.</span></span>

6.  <span data-ttu-id="1be54-187">Følg disse trin for at tilføje oversættelser af teksten:</span><span class="sxs-lookup"><span data-stu-id="1be54-187">To add translations of the text, follow these steps:</span></span>
    1.  <span data-ttu-id="1be54-188">Klik på **Oversættelser**.</span><span class="sxs-lookup"><span data-stu-id="1be54-188">Click **Translations**.</span></span>
    2.  <span data-ttu-id="1be54-189">Klik på **Tilføj** på den viste side.</span><span class="sxs-lookup"><span data-stu-id="1be54-189">On the page that appears, Click **Add**.</span></span>
    3.  <span data-ttu-id="1be54-190">På den viste liste skal du vælge det sprog, du vil bruge, når du indtaster teksten.</span><span class="sxs-lookup"><span data-stu-id="1be54-190">In the list that appears, select the language that you will enter the text in.</span></span>
    4.  <span data-ttu-id="1be54-191">Indtast teksten i feltet **Oversat tekst**.</span><span class="sxs-lookup"><span data-stu-id="1be54-191">In the **Translated text** field, enter the text.</span></span>
    5.  <span data-ttu-id="1be54-192">Hvis du vil personalisere teksten, kan du indsætte pladsholdere.</span><span class="sxs-lookup"><span data-stu-id="1be54-192">To personalize the text, you can insert placeholders.</span></span> <span data-ttu-id="1be54-193">I trin 5 kan du se anvisninger i, hvordan du angiver en pladsholder.</span><span class="sxs-lookup"><span data-stu-id="1be54-193">For instructions about how to enter a placeholder, see step 5.</span></span>
    6.  <span data-ttu-id="1be54-194">Klik på **Luk**.</span><span class="sxs-lookup"><span data-stu-id="1be54-194">Click **Close**.</span></span>

7.  <span data-ttu-id="1be54-195">På fanen **Modtager** skal du bruge følgende indstillinger til at angive, hvem der skal modtage beskeder.</span><span class="sxs-lookup"><span data-stu-id="1be54-195">On the **Recipient** tab, use the following options to specify who should receive the notifications.</span></span>
    <table>
    <colgroup>
    <col width="33%" />
    <col width="33%" />
    <col width="33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="1be54-196">Indstilling</span><span class="sxs-lookup"><span data-stu-id="1be54-196">Option</span></span></th>
    <th><span data-ttu-id="1be54-197">Beskederne sendes til disse brugere.</span><span class="sxs-lookup"><span data-stu-id="1be54-197">Notifications are sent to these users</span></span></th>
    <th><span data-ttu-id="1be54-198">Hvis du vil sende beskeder, skal du følge disse trin</span><span class="sxs-lookup"><span data-stu-id="1be54-198">To send notifications, follow these steps</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><span data-ttu-id="1be54-199">Deltager</span><span class="sxs-lookup"><span data-stu-id="1be54-199">Participant</span></span></td>
    <td><span data-ttu-id="1be54-200">Brugere, som er tildelt til en bestemt gruppe eller rolle</span><span class="sxs-lookup"><span data-stu-id="1be54-200">Users who are assigned to a specific group or role</span></span></td>
    <td><ol>
    <li><span data-ttu-id="1be54-201">På fanen <strong>Modtager</strong> skal du klikke på <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="1be54-201">On the <strong>Recipient</strong> tab, click <strong>Participant</strong>.</span></span></li>
    <li><span data-ttu-id="1be54-202">På fanen <strong>Rollebaseret</strong> på listen <strong>Deltagertype</strong> skal du vælge den type gruppe eller rolle, du vil sende beskeder til.</span><span class="sxs-lookup"><span data-stu-id="1be54-202">On the <strong>Role based</strong> tab, in the <strong>Type of participant</strong> list, select the type of group or role to send notifications to.</span></span></li>
    <li><span data-ttu-id="1be54-203">Vælg den gruppe eller rolle, der skal sendes beskeder til, på listen <strong>Deltager</strong>.</span><span class="sxs-lookup"><span data-stu-id="1be54-203">In the <strong>Participant</strong> list, select the group or role to send notifications to.</span></span></li>
    </ol></td>
    </tr>
    <tr class="even">
    <td><span data-ttu-id="1be54-204">Arbejdsgangsbruger</span><span class="sxs-lookup"><span data-stu-id="1be54-204">Workflow user</span></span></td>
    <td><span data-ttu-id="1be54-205">Brugere, som deltager i denne arbejdsgang</span><span class="sxs-lookup"><span data-stu-id="1be54-205">Users who are participants in this workflow</span></span></td>
    <td><ol>
    <li><span data-ttu-id="1be54-206">På fanen <strong>Modtager</strong> skal du klikke på <strong>Arbejdsgangsbruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="1be54-206">On the <strong>Recipient</strong> tab, click <strong>Workflow user</strong>.</span></span></li>
    <li><span data-ttu-id="1be54-207">På fanen <strong>Arbejdsgangsbruger</strong> på listen <strong>Arbejdsgangsbruger</strong> skal du vælge en deltager i denne arbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="1be54-207">On the <strong>Workflow user</strong> tab, in the <strong>Workflow user</strong> list, select a participant in this workflow.</span></span></li>
    </ol></td>
    </tr>
    <tr class="odd">
    <td><span data-ttu-id="1be54-208">Bruger</span><span class="sxs-lookup"><span data-stu-id="1be54-208">User</span></span></td>
    <td><span data-ttu-id="1be54-209">Bestemte Finance and Operations-brugere</span><span class="sxs-lookup"><span data-stu-id="1be54-209">Specific Finance and Operations users</span></span></td>
    <td><ol>
    <li><span data-ttu-id="1be54-210">På fanen <strong>Modtager</strong> skal du klikke på <strong>Bruger</strong>.</span><span class="sxs-lookup"><span data-stu-id="1be54-210">On the <strong>Recipient</strong> tab, click <strong>User</strong>.</span></span></li>
    <li><span data-ttu-id="1be54-211">Under fanen <strong>Bruger</strong> på listen <strong>Tilgængelige brugere</strong> vises alle Finance and Operations-brugere.</span><span class="sxs-lookup"><span data-stu-id="1be54-211">On the <strong>User</strong> tab, the <strong>Available users</strong> list includes all Finance and Operations users.</span></span> <span data-ttu-id="1be54-212">Vælg de brugere, der skal sendes beskeder til, og flyt derefter disse brugere til listen <strong>Valgte brugere</strong>.</span><span class="sxs-lookup"><span data-stu-id="1be54-212">Select the users to send notifications to, and move those users into the <strong>Selected users</strong> list.</span></span></li>
    </ol></td>
    </tr>
    </tbody>
    </table>

8.  <span data-ttu-id="1be54-213">Gentag trin 3 til 7 for hver af de hændelser, du har valgt i trin 2.</span><span class="sxs-lookup"><span data-stu-id="1be54-213">Repeat steps 3 through 7 for each event that you selected in step 2.</span></span>

## <a name="enter-comments-about-the-changes-that-you-made-to-the-workflow"></a><span data-ttu-id="1be54-214">Angiv kommentarer om de ændringer, du har foretaget i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="1be54-214">Enter comments about the changes that you made to the workflow</span></span>
<span data-ttu-id="1be54-215">Hvis du vil angive kommentarer om de ændringer, du har foretaget i arbejdsgangen, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="1be54-215">To enter comments about the changes that you made to the workflow, follow these steps.</span></span>

1.  <span data-ttu-id="1be54-216">Klik på **Noter** i ruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="1be54-216">In the left pane, click **Notes**.</span></span>
2.  <span data-ttu-id="1be54-217">I feltet **Angiv kommentarer om arbejdsgangen** skal du angive dine kommentarer.</span><span class="sxs-lookup"><span data-stu-id="1be54-217">In the **Enter comments about the workflow** field, enter your comments.</span></span>
3.  <span data-ttu-id="1be54-218">Gennemse kommentarer.</span><span class="sxs-lookup"><span data-stu-id="1be54-218">Review your comments.</span></span> <span data-ttu-id="1be54-219">Når du har tilføjet kommentarer, kan du ikke ændre dem.</span><span class="sxs-lookup"><span data-stu-id="1be54-219">After you add comments, you can't modify them.</span></span>
4.  <span data-ttu-id="1be54-220">Klik på **Tilføj** til at tilføje dine kommentarer til området **Kommentarhistorik**.</span><span class="sxs-lookup"><span data-stu-id="1be54-220">Click **Add** to add your comments to the **Comment history** area.</span></span>





