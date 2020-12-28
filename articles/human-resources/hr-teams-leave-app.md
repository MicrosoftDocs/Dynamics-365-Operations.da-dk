---
title: Administrere anmodninger i Teams
description: I dette emne kan du se, hvordan du anmoder om fri i Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 10/28/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: d24c257054578282f1a2eafa050094194a358aa0
ms.sourcegitcommit: 369639cd92e03fe792ed9d61a329d842aafa052f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/29/2020
ms.locfileid: "4417892"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="5449f-103">Administrere anmodninger i Teams</span><span class="sxs-lookup"><span data-stu-id="5449f-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="5449f-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan du hurtigt anmode om at få fri og se dine flekskontooplysninger direkte i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5449f-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="5449f-105">Du kan interagere med en robot for at anmode om oplysninger og starte en orlovsanmodning.</span><span class="sxs-lookup"><span data-stu-id="5449f-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="5449f-106">Fanen **Fridage** giver mere detaljerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="5449f-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="5449f-107">Du kan også sende personer oplysninger om dine kommende fridage i teams og chatte uden for Human Resource-appen.</span><span class="sxs-lookup"><span data-stu-id="5449f-107">You can also send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="5449f-108">Installere appen</span><span class="sxs-lookup"><span data-stu-id="5449f-108">Install the app</span></span>

<span data-ttu-id="5449f-109">Du kan finde Personale-appen i storen til Teams.</span><span class="sxs-lookup"><span data-stu-id="5449f-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="5449f-110">I Microsoft Teams skal du vælge ellipserne.</span><span class="sxs-lookup"><span data-stu-id="5449f-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Ellipser i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="5449f-112">Søg efter Dynamics 365 Human Resources, og vælg derefter feltet **Personale**.</span><span class="sxs-lookup"><span data-stu-id="5449f-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![HR-feltet i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="5449f-114">Klik på knappen **Tilføj** for at installere appen.</span><span class="sxs-lookup"><span data-stu-id="5449f-114">Select the **Add** button to install the app.</span></span>

   ![Installer orlovsappen i Personale i Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="5449f-116">Hvis appen ikke automatisk logger dig på, skal du vælge fanen **Indstillinger** for at logge på.</span><span class="sxs-lookup"><span data-stu-id="5449f-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Fanen Indstillinger i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="5449f-118">Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer.</span><span class="sxs-lookup"><span data-stu-id="5449f-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="5449f-119">Hvis du har adgang til mere end én forekomst af Personale, kan du vælge, hvilket miljø du vil oprette forbindelse til, under fanen **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="5449f-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="5449f-120">Appen understøtter nu sikkerhedsrollen Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="5449f-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="5449f-121">Brug botten</span><span class="sxs-lookup"><span data-stu-id="5449f-121">Use the bot</span></span>

<span data-ttu-id="5449f-122">Når appen er installeret, vises en velkomstmeddelelse, der giver dig besked om, hvilke typer handlinger botten kan udføre på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="5449f-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Botvelkomstmeddelelse i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="5449f-124">Når du interagerer med bot for første gang, skal du muligvis logge på.</span><span class="sxs-lookup"><span data-stu-id="5449f-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="5449f-125">Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer.</span><span class="sxs-lookup"><span data-stu-id="5449f-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="5449f-126">Du kan bede bot om at:</span><span class="sxs-lookup"><span data-stu-id="5449f-126">You can ask the bot to:</span></span>

- <span data-ttu-id="5449f-127">Vise oplysninger om flekskontoen for hver orlovstype, du er tilmeldt.</span><span class="sxs-lookup"><span data-stu-id="5449f-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Vise konti i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="5449f-129">Vise flere detaljer om en bestemt orlovstype.</span><span class="sxs-lookup"><span data-stu-id="5449f-129">Show additional details about a specific leave type.</span></span>

   ![Vise detaljer i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="5449f-131">Starte en anmodning om en orlov for dig.</span><span class="sxs-lookup"><span data-stu-id="5449f-131">Start a leave request for you.</span></span>

   ![Anmodning om orlov i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="5449f-133">Når du har startet en orlovsanmodning, kan du justere dagene direkte på kortet.</span><span class="sxs-lookup"><span data-stu-id="5449f-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Redigering af anmodning i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="5449f-135">Når du er færdig med at angive oplysninger, skal du vælge **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="5449f-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="5449f-136">Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="5449f-136">You can also select **Save as draft** to come back to it later.</span></span>

![Afsendelse af anmodning i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="5449f-138">Administrere din orlov i Teams</span><span class="sxs-lookup"><span data-stu-id="5449f-138">Manage your leave in Teams</span></span>

<span data-ttu-id="5449f-139">Fanen **Fri** gør det muligt at vise:</span><span class="sxs-lookup"><span data-stu-id="5449f-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="5449f-140">Kontooplysninger om hver orlovstype, du er tilmeldt</span><span class="sxs-lookup"><span data-stu-id="5449f-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="5449f-141">Kommende orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="5449f-141">Upcoming leave requests</span></span>

- <span data-ttu-id="5449f-142">Anmodninger om fri</span><span class="sxs-lookup"><span data-stu-id="5449f-142">Time-off requests</span></span>

- <span data-ttu-id="5449f-143">kladdeorlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="5449f-143">Draft leave requests</span></span>

![Fanen Fri i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="5449f-145">Oprette en ny anmodning</span><span class="sxs-lookup"><span data-stu-id="5449f-145">Create a new request</span></span>

1. <span data-ttu-id="5449f-146">Hvis du vil oprette en ny anmodning, skal du vælge **Ny anmodning**.</span><span class="sxs-lookup"><span data-stu-id="5449f-146">To create a new leave request, select **New request**.</span></span>

   ![Ny anmodning i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="5449f-148">Angiv den eller de dage, du vil have en fridag, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="5449f-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Tilføj fridag i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="5449f-150">Angiv en årsagskode, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="5449f-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="5449f-151">Skriv også eventuelle kommentarer, og tilføj evt. vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="5449f-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="5449f-152">Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="5449f-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="5449f-153">Du kan også indtaste **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="5449f-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="5449f-154">Administrere kladdeanmodninger</span><span class="sxs-lookup"><span data-stu-id="5449f-154">Manage draft requests</span></span>

1. <span data-ttu-id="5449f-155">Vælg fanen **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="5449f-155">Select the **Drafts** tab.</span></span>

   ![Fanen Kladder i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="5449f-157">Vælg blyanten for at redigere anmodningen, eller vælg papirkurven, som kan slette anmodningen.</span><span class="sxs-lookup"><span data-stu-id="5449f-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="5449f-158">Foretag eventuelle nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="5449f-158">Make any necessary changes.</span></span> <span data-ttu-id="5449f-159">Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="5449f-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="5449f-160">Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="5449f-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Redigering af kladde i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="5449f-162">Besvare Teams-beskeder</span><span class="sxs-lookup"><span data-stu-id="5449f-162">Respond to Teams notifications</span></span>

<span data-ttu-id="5449f-163">Når du eller en arbejder, du er godkender for, sender en anmodning om orlov, modtager du en besked i appen Personale i Teams.</span><span class="sxs-lookup"><span data-stu-id="5449f-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="5449f-164">Du kan vælge beskeden for at få den vist.</span><span class="sxs-lookup"><span data-stu-id="5449f-164">You can select the notification to view it.</span></span> <span data-ttu-id="5449f-165">Beskeder vises også i **Chat**-området.</span><span class="sxs-lookup"><span data-stu-id="5449f-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="5449f-166">Hvis du er godkender, kan du vælge **Godkend** eller **Afvis** i beskeden.</span><span class="sxs-lookup"><span data-stu-id="5449f-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="5449f-167">Du kan også angive en valgfri meddelelse.</span><span class="sxs-lookup"><span data-stu-id="5449f-167">You can also provide an optional message.</span></span>

![Besked om orlovsanmodning i Teams-appen Personale](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="5449f-169">Sende kommende oplysninger om fridage til dine kolleger</span><span class="sxs-lookup"><span data-stu-id="5449f-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="5449f-170">Når du har installeret Human Resources-appen for Teams, kan du nemt sende oplysninger om dine kommende fridage til dine kolleger i teams eller chatsamtaler.</span><span class="sxs-lookup"><span data-stu-id="5449f-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="5449f-171">I et team eller en chat i Teams skal du vælge knappen Human Resources under chatvinduet.</span><span class="sxs-lookup"><span data-stu-id="5449f-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Knappen Human Resources under chatvinduet](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="5449f-173">Vælg den orlovsanmodning, du vil dele.</span><span class="sxs-lookup"><span data-stu-id="5449f-173">Select the leave request you want to share.</span></span> <span data-ttu-id="5449f-174">Hvis du vil dele en kladde af orlovsanmodningen, skal du vælge **Kladder** først.</span><span class="sxs-lookup"><span data-stu-id="5449f-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Vælge en kommende orlovsanmodning til at dele](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="5449f-176">Din orlovsanmodning vises i chatten.</span><span class="sxs-lookup"><span data-stu-id="5449f-176">Your leave request will display in the chat.</span></span>

![Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="5449f-178">Hvis du har delt en kladdebaseret anmodning, vises den som en kladde:</span><span class="sxs-lookup"><span data-stu-id="5449f-178">If you shared a draft request, it will display as a draft:</span></span>

![Kladde af Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="5449f-180">Se dit teams orlovskalender</span><span class="sxs-lookup"><span data-stu-id="5449f-180">View your team's leave calendar</span></span>

<span data-ttu-id="5449f-181">Hvis du er chef med direkte underordnede, kan du få vist dit teams godkendte og afventende fravær.</span><span class="sxs-lookup"><span data-stu-id="5449f-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="5449f-182">I appen Personale i Teams skal du vælge **Fri**.</span><span class="sxs-lookup"><span data-stu-id="5449f-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="5449f-183">Vælg **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="5449f-183">Select **Team calendar**.</span></span>

   ![Se kalender i Teams-appen Personale](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="5449f-185">I kalenderen vises dine direkte underordnedes godkendte og afventende fravær.</span><span class="sxs-lookup"><span data-stu-id="5449f-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Fraværskalender i Teams-appen Personale](./media/hr-teams-leave-app-calendar.png)

## <a name="troubleshooting"></a><span data-ttu-id="5449f-187">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="5449f-187">Troubleshooting</span></span>

<span data-ttu-id="5449f-188">Hvis du har problemer med at logge på eller bruge appen Human Resources Teams, kan du prøve at følge disse fejlfindingsinstruktioner.</span><span class="sxs-lookup"><span data-stu-id="5449f-188">If you're having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="5449f-189">Hvis du stadig har problemer efter fejlfinding, skal du kontakte Support.</span><span class="sxs-lookup"><span data-stu-id="5449f-189">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="5449f-190">Du kan finde flere oplysninger under [Få support](hr-admin-troubleshooting-support.md).</span><span class="sxs-lookup"><span data-stu-id="5449f-190">For more information, see [Get support](hr-admin-troubleshooting-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="5449f-191">Der kan ikke logge på appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="5449f-191">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="5449f-192">Hvis du ikke kan logge på appen, er det muligt, at den konto, du bruger til at logge på Microsoft Teams, ikke er knyttet til en medarbejderpost i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5449f-192">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5449f-193">Kontakt systemadministratoren for at sikre, at din medarbejderpost er tilknyttet korrekt.</span><span class="sxs-lookup"><span data-stu-id="5449f-193">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="5449f-194">Der opstod en fejl under godkendelse af orlovsanmodninger i appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="5449f-194">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="5449f-195">Hvis du modtager en fejl under forsøg på at godkende orlovsanmodninger i appen Teams, skal du prøve følgende fejlfindingstrin:</span><span class="sxs-lookup"><span data-stu-id="5449f-195">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="5449f-196">Kontrollér, at den konto, du bruger til at logge på Microsoft Teams, er den samme, som du bruger til at få adgang til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5449f-196">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="5449f-197">Kontrollér, at du er en gyldig godkender af anmodningen, ved at kontrollere indstillingerne af arbejdsproces for orlovsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="5449f-197">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="5449f-198">Du kan finde flere oplysninger om orlovsarbejdsprocesser i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="5449f-198">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="5449f-199">Kendte problemer med tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="5449f-199">Known accessibility issues</span></span>

<span data-ttu-id="5449f-200">Human Resources-appen i Teams har følgende tilgængelighedsproblemer, som vi arbejder på at løse i fremtidige versioner.</span><span class="sxs-lookup"><span data-stu-id="5449f-200">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="5449f-201">Udsted</span><span class="sxs-lookup"><span data-stu-id="5449f-201">Issue</span></span> | <span data-ttu-id="5449f-202">Løsning eller forklaring</span><span class="sxs-lookup"><span data-stu-id="5449f-202">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="5449f-203">Hvis du zoomer til 400 % på skrivebordet, skjules nogle af handlingsknapperne i visningen.</span><span class="sxs-lookup"><span data-stu-id="5449f-203">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="5449f-204">Vi anbefaler, at du bruger et forstørrelsesglas i stedet, indtil vi kan understøtte dette zoomniveau.</span><span class="sxs-lookup"><span data-stu-id="5449f-204">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="5449f-205">Under fanen **Fridage** annoncerer VoiceOver en knaphandling under læsning af overskriften til gitteret for fridage.</span><span class="sxs-lookup"><span data-stu-id="5449f-205">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="5449f-206">Overskriften og elementerne i gitteret grupperes efter år, og de kan skjules.</span><span class="sxs-lookup"><span data-stu-id="5449f-206">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="5449f-207">VoiceOver fortolker dette som et element, der kræver en handling, men det er ikke.</span><span class="sxs-lookup"><span data-stu-id="5449f-207">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="5449f-208">Hvis du foretager en strygebevægelse, mens en pop op-menu er åben, ignorerer VoiceOver læsningen af pop op-menuen eller menuindholdet.</span><span class="sxs-lookup"><span data-stu-id="5449f-208">If you swipe while a popup or menu is open, voiceover skips reading the popup or menu contents.</span></span> | <span data-ttu-id="5449f-209">Udforsk indholdet ved hjælp af fingerscanning.</span><span class="sxs-lookup"><span data-stu-id="5449f-209">Explore the content using finger scanning.</span></span> |
| <span data-ttu-id="5449f-210">Under fanen **Fridage** er der en ekstra strygebevægelse, når du navigerer til **Årsagskode** i en ny anmodning.</span><span class="sxs-lookup"><span data-stu-id="5449f-210">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="5449f-211">Der er ikke noget skjult kontrolelement, som strygenavigationen forsøger at få adgang til.</span><span class="sxs-lookup"><span data-stu-id="5449f-211">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="5449f-212">Hvis du lave en strygebevægelser under fanen **Fridage**, mens kalenderen er åben, havner du uden for kontrolelementet i stedet for øverst i en ny anmodning, eller når du redigerer en anmodning.</span><span class="sxs-lookup"><span data-stu-id="5449f-212">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="5449f-213">Når du når **Gå til i dag**, skal du betragte det som slutningen af kontrolelementet og stryge i modsatte retning for at gå tilbage til toppen.</span><span class="sxs-lookup"><span data-stu-id="5449f-213">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="5449f-214">VoiceOver kan ikke læse datoetiketterne.</span><span class="sxs-lookup"><span data-stu-id="5449f-214">Voiceover doesn't read the labels for dates.</span></span> | <span data-ttu-id="5449f-215">De datoer, der optræder som par, er altid **Startdato** og **Slutdato**.</span><span class="sxs-lookup"><span data-stu-id="5449f-215">The dates encountered in pairs are always **Start date** and **End date**.</span></span> |
| <span data-ttu-id="5449f-216">Under fanen **Chat** springer fokus tilbage til toppen, når du angiver en dato, mens du bruger hjælpeværktøjet eller tastaturnavigation.</span><span class="sxs-lookup"><span data-stu-id="5449f-216">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="5449f-217">Tabulér, indtil du når til inputområdet igen.</span><span class="sxs-lookup"><span data-stu-id="5449f-217">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="5449f-218">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="5449f-218">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="5449f-219">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="5449f-219">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="5449f-220">Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål.</span><span class="sxs-lookup"><span data-stu-id="5449f-220">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="5449f-221">Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="5449f-221">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="5449f-222">Læs mere om LUIS [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="5449f-222">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="5449f-223">LUIS-tjenesten gør formålet utvetydeligt eller forstår formålet med brugerinputtet (i dette tilfælde er formålet at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso).</span><span class="sxs-lookup"><span data-stu-id="5449f-223">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="5449f-224">Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="5449f-224">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="5449f-225">Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse.</span><span class="sxs-lookup"><span data-stu-id="5449f-225">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="5449f-226">LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="5449f-226">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="5449f-227">Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen.</span><span class="sxs-lookup"><span data-stu-id="5449f-227">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="5449f-228">Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="5449f-228">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="5449f-229">Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="5449f-229">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="5449f-230">Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="5449f-230">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="5449f-231">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="5449f-231">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="5449f-232">Når du bruger Dynamics 365 Human Resources-appen i Microsoft Teams, kan visse kundedata flyde uden for det geografiske område, hvor din lejers personaleservice er installeret.</span><span class="sxs-lookup"><span data-stu-id="5449f-232">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="5449f-233">Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsgangsopgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5449f-233">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="5449f-234">Disse data kan gemmes i Microsoft Azure Event Grid i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester.</span><span class="sxs-lookup"><span data-stu-id="5449f-234">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="5449f-235">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="5449f-235">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="5449f-236">Indholdet i samtalen med chatrobotten i Human Resources-appen kan gemmes i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="5449f-236">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="5449f-237">Disse data kan gemmes i Azure Cosmos DB i op til 24 timer og kan behandles uden for det geografiske område, hvor din lejers Human Resources-tjeneste er udrullet. Data, der er undervejs, og inaktive data krypteres og bruges ikke af Microsoft eller underprocesser til træning eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="5449f-237">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="5449f-238">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="5449f-238">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="5449f-239">Hvis du vil begrænse adgangen til Human Resources-appen i Microsoft Teams for din organisation eller brugere i organisationen, skal du se [Styre apptilladelsespolitikker i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="5449f-239">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="5449f-240">Se også</span><span class="sxs-lookup"><span data-stu-id="5449f-240">See also</span></span>

[<span data-ttu-id="5449f-241">Downloade og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="5449f-241">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="5449f-242">Microsoft Teams Hjælp-center</span><span class="sxs-lookup"><span data-stu-id="5449f-242">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="5449f-243">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="5449f-243">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
