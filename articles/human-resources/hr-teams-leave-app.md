---
title: Administrere anmodninger i Teams
description: I dette emne kan du se, hvordan du anmoder om fri i Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 48bf6f7997d6159077419bcd05d27fd711c8fb4b
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5891024"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="2cdf7-103">Administrere fraværsanmodninger i Teams</span><span class="sxs-lookup"><span data-stu-id="2cdf7-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="2cdf7-104">Med Dynamics 365 Human Resources-appen i Microsoft Teams kan du hurtigt anmode om at få fri og se dine flekskontooplysninger direkte i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="2cdf7-105">Du kan interagere med en robot for at anmode om oplysninger og starte en orlovsanmodning.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="2cdf7-106">Fanen **Fridage** giver mere detaljerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="2cdf7-107">Du kan også sende personer oplysninger om dine kommende fridage i Teams og chatte uden for Human Resource-appen.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="2cdf7-108">Installere appen</span><span class="sxs-lookup"><span data-stu-id="2cdf7-108">Install the app</span></span>

<span data-ttu-id="2cdf7-109">Du kan finde appen Dynamics 365 Human Resources i lageret til Teams.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="2cdf7-110">I Microsoft Teams skal du vælge ellipserne.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Ellipser i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="2cdf7-112">Søg efter Dynamics 365 Human Resources, og vælg derefter feltet **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![HR-feltet i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="2cdf7-114">Klik på knappen **Tilføj** for at installere appen.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-114">Select the **Add** button to install the app.</span></span>

   ![Installer orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="2cdf7-116">Hvis appen ikke automatisk logger dig på, skal du vælge fanen **Indstillinger** for at logge på.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Fanen Indstillinger i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="2cdf7-118">Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="2cdf7-119">Hvis du har adgang til mere end én forekomst af Human Resources, kan du vælge, hvilket miljø du vil oprette forbindelse til, under fanen **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="2cdf7-120">Appen understøtter nu sikkerhedsrollen Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="2cdf7-121">Brug botten</span><span class="sxs-lookup"><span data-stu-id="2cdf7-121">Use the bot</span></span>

<span data-ttu-id="2cdf7-122">Når appen er installeret, vises en velkomstmeddelelse, der giver dig besked om, hvilke typer handlinger botten kan udføre på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Botvelkomstmeddelelse i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="2cdf7-124">Når du interagerer med bot for første gang, skal du muligvis logge på.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="2cdf7-125">Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="2cdf7-126">Du kan bede bot om at:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-126">You can ask the bot to:</span></span>

- <span data-ttu-id="2cdf7-127">Starte en anmodning om en orlov for dig.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-127">Start a leave request for you.</span></span>

  ![Starte en anmodning om orlov i Teams-chat](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="2cdf7-129">Chatrobotten udfylder en orlovsanmodning for dig.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-129">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="2cdf7-130">Vælg **Anmod om fri**, og rediger detaljerne om anmodningen.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-130">Select **Request time off** and edit the details for your request.</span></span>

  ![Redigere detaljer om orlovsanmodning](./media/hr-teams-leave-app-details.png)

- <span data-ttu-id="2cdf7-132">Når du er færdig med at redigere oplysningerne om din anmodning om orlov, skal du vælge **Send** for at sende den til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Sende orlovsanmodning](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="2cdf7-134">Administrere din orlov i Teams</span><span class="sxs-lookup"><span data-stu-id="2cdf7-134">Manage your leave in Teams</span></span>

<span data-ttu-id="2cdf7-135">Fanen **Fri** gør det muligt at vise:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="2cdf7-136">Kontooplysninger om hver orlovstype, du er tilmeldt</span><span class="sxs-lookup"><span data-stu-id="2cdf7-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="2cdf7-137">Kommende orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="2cdf7-137">Upcoming leave requests</span></span>

- <span data-ttu-id="2cdf7-138">Anmodninger om fri</span><span class="sxs-lookup"><span data-stu-id="2cdf7-138">Time-off requests</span></span>

- <span data-ttu-id="2cdf7-139">kladdeorlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="2cdf7-139">Draft leave requests</span></span>

![Fanen Fri i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="2cdf7-141">Oprette en ny anmodning</span><span class="sxs-lookup"><span data-stu-id="2cdf7-141">Create a new request</span></span>

1. <span data-ttu-id="2cdf7-142">Hvis du vil oprette en ny anmodning, skal du vælge **Ny anmodning**.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-142">To create a new leave request, select **New request**.</span></span>

   ![Ny anmodning i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="2cdf7-144">Angiv den eller de dage, du vil have en fridag, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-144">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Tilføj fridag i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="2cdf7-146">Angiv en årsagskode, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-146">If applicable, enter a reason code.</span></span> <span data-ttu-id="2cdf7-147">Skriv også eventuelle kommentarer, og tilføj evt. vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-147">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="2cdf7-148">Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-148">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2cdf7-149">Du kan også indtaste **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-149">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="2cdf7-150">Administrere kladdeanmodninger</span><span class="sxs-lookup"><span data-stu-id="2cdf7-150">Manage draft requests</span></span>

1. <span data-ttu-id="2cdf7-151">Vælg fanen **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-151">Select the **Drafts** tab.</span></span>

   ![Fanen Kladder i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="2cdf7-153">Vælg blyanten for at redigere anmodningen, eller vælg papirkurven, som kan slette anmodningen.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="2cdf7-154">Foretag eventuelle nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-154">Make any necessary changes.</span></span> <span data-ttu-id="2cdf7-155">Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="2cdf7-156">Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-156">You can also select **Save as draft** to come back to it later.</span></span>

   ![Redigering af kladde i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="2cdf7-158">Besvare Teams-beskeder</span><span class="sxs-lookup"><span data-stu-id="2cdf7-158">Respond to Teams notifications</span></span>

<span data-ttu-id="2cdf7-159">Når du eller en arbejder, du er godkender for, sender en anmodning om orlov, modtager du en besked i appen Human Resources i Teams.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-159">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="2cdf7-160">Du kan vælge beskeden for at få den vist.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-160">You can select the notification to view it.</span></span> <span data-ttu-id="2cdf7-161">Beskeder vises også i **Chat**-området.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-161">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="2cdf7-162">Hvis du er godkender, kan du vælge **Godkend** eller **Afvis** i beskeden.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-162">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="2cdf7-163">Du kan også angive en valgfri meddelelse.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-163">You can also provide an optional message.</span></span>

![Besked om orlovsanmodning i Teams-appen Human Resources](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="2cdf7-165">Sende kommende oplysninger om fridage til dine kolleger</span><span class="sxs-lookup"><span data-stu-id="2cdf7-165">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="2cdf7-166">Når du har installeret Human Resources-appen for Teams, kan du nemt sende oplysninger om dine kommende fridage til dine kolleger i teams eller chatsamtaler.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-166">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="2cdf7-167">I et team eller en chat i Teams skal du vælge knappen Human Resources under chatvinduet.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-167">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Knappen Human Resources under chatvinduet](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="2cdf7-169">Vælg den orlovsanmodning, du vil dele.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-169">Select the leave request you want to share.</span></span> <span data-ttu-id="2cdf7-170">Hvis du vil dele en kladde af orlovsanmodningen, skal du vælge **Kladder** først.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-170">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Vælge en kommende orlovsanmodning til at dele](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="2cdf7-172">Din orlovsanmodning vises i chatten.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-172">Your leave request will display in the chat.</span></span>

![Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="2cdf7-174">Hvis du har delt en kladdebaseret anmodning, vises den som en kladde:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-174">If you shared a draft request, it will display as a draft:</span></span>

![Kladde af Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="2cdf7-176">Se dit teams orlovskalender</span><span class="sxs-lookup"><span data-stu-id="2cdf7-176">View your team's leave calendar</span></span>

<span data-ttu-id="2cdf7-177">Hvis du er chef med direkte underordnede, kan du få vist dit teams godkendte og afventende fravær.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-177">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="2cdf7-178">I appen Human Resources i Teams skal du vælge **Fri**.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-178">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="2cdf7-179">Vælg **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-179">Select **Team calendar**.</span></span> <span data-ttu-id="2cdf7-180">I kalenderen vises dine direkte underordnedes godkendte og afventende fravær.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-180">The calendar displays your direct reports' approved and pending time off.</span></span>

   ![Se kalender i Teams-appen Human Resources](./media/hr-teams-leave-app-view-calendar.png)

   > [!NOTE]
   > <span data-ttu-id="2cdf7-182">Hvis du ikke kan se teamkalenderen, kan du bede din administrator om at aktivere den.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-182">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="2cdf7-183">Du kan finde flere oplysninger i [Installere og konfigurere](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-183">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="2cdf7-184">Understøttede sprog</span><span class="sxs-lookup"><span data-stu-id="2cdf7-184">Supported languages</span></span>

<span data-ttu-id="2cdf7-185">Appen Dynamics 365 Human Resources i Teams understøtter følgende sprog:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-185">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="2cdf7-186">Landestandard-id</span><span class="sxs-lookup"><span data-stu-id="2cdf7-186">Locale ID</span></span> | <span data-ttu-id="2cdf7-187">Sprog</span><span class="sxs-lookup"><span data-stu-id="2cdf7-187">Language</span></span> |
| --- | --- |
| <span data-ttu-id="2cdf7-188">de-DE</span><span class="sxs-lookup"><span data-stu-id="2cdf7-188">de-DE</span></span> | <span data-ttu-id="2cdf7-189">Tysk (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-189">German (Germany)</span></span> |
| <span data-ttu-id="2cdf7-190">es-ES</span><span class="sxs-lookup"><span data-stu-id="2cdf7-190">es-ES</span></span> | <span data-ttu-id="2cdf7-191">Spansk (Spanien)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-191">Spanish (Spain)</span></span> |
| <span data-ttu-id="2cdf7-192">es-MX</span><span class="sxs-lookup"><span data-stu-id="2cdf7-192">es-MX</span></span> | <span data-ttu-id="2cdf7-193">Spansk (Mexico)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-193">Spanish (Mexico)</span></span> |
| <span data-ttu-id="2cdf7-194">fr-CA</span><span class="sxs-lookup"><span data-stu-id="2cdf7-194">fr-CA</span></span> | <span data-ttu-id="2cdf7-195">Fransk (Canada)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-195">French (Canada)</span></span> |
| <span data-ttu-id="2cdf7-196">fr-FR</span><span class="sxs-lookup"><span data-stu-id="2cdf7-196">fr-FR</span></span> | <span data-ttu-id="2cdf7-197">Fransk (Frankrig)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-197">French (France)</span></span> |
| <span data-ttu-id="2cdf7-198">it-IT</span><span class="sxs-lookup"><span data-stu-id="2cdf7-198">it-IT</span></span> | <span data-ttu-id="2cdf7-199">Italiensk (Italien)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-199">Italian (Italy)</span></span> |
| <span data-ttu-id="2cdf7-200">nl-NL</span><span class="sxs-lookup"><span data-stu-id="2cdf7-200">nl-NL</span></span> | <span data-ttu-id="2cdf7-201">Hollandsk (Nederlandene)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-201">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="2cdf7-202">pt-BR</span><span class="sxs-lookup"><span data-stu-id="2cdf7-202">pt-BR</span></span> | <span data-ttu-id="2cdf7-203">Portugisisk (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-203">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="2cdf7-204">tr-TR</span><span class="sxs-lookup"><span data-stu-id="2cdf7-204">tr-TR</span></span> | <span data-ttu-id="2cdf7-205">Tyrkisk (Tyrkiet)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-205">Turkish (Turkey)</span></span> |
| <span data-ttu-id="2cdf7-206">zh-CN</span><span class="sxs-lookup"><span data-stu-id="2cdf7-206">zh-CN</span></span> | <span data-ttu-id="2cdf7-207">Kinesisk (forenklet)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-207">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="2cdf7-208">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="2cdf7-208">Troubleshooting</span></span>

<span data-ttu-id="2cdf7-209">Hvis du har problemer med at logge på eller bruge Dynamics 365 Human Resources-appen Teams, kan du prøve at følge disse fejlfindingsinstruktioner.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-209">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="2cdf7-210">Hvis du stadig har problemer efter fejlfinding, skal du kontakte Support.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-210">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="2cdf7-211">Du kan finde flere oplysninger under [Få support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-211">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="2cdf7-212">Der kan ikke logge på appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="2cdf7-212">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="2cdf7-213">Hvis du ikke kan logge på appen, er det muligt, at den konto, du bruger til at logge på Microsoft Teams, ikke er knyttet til en medarbejderpost i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-213">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2cdf7-214">Kontakt systemadministratoren for at sikre, at din medarbejderpost er tilknyttet korrekt.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-214">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="2cdf7-215">Oversættelser vises ikke korrekt</span><span class="sxs-lookup"><span data-stu-id="2cdf7-215">Translations don't display correctly</span></span>

<span data-ttu-id="2cdf7-216">Hvis oversættelser ikke vises som forventet, skal du sørge for, at det sprog, du vælger i Teams, svarer til det sprog, der er valgt i **Brugerindstillinger** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-216">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="2cdf7-217">I Teams skal du se på **App-sprog** i **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-217">In Teams, look at **App language** in **Settings**.</span></span>

![Teams-indstillinger](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="2cdf7-219">Vælg **Indstillinger** i Human Resources, og vælg derefter **Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-219">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="2cdf7-220">Kontrollér, at feltet **Sprog** svarer til feltet **App-sprog** i Teams.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-220">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Brugerindstillinger i Human Resources](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="2cdf7-222">Hvis du stadig oplever oversættelsesproblemer, kan du give os besked.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-222">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="2cdf7-223">Du kan finde oplysninger i [Få support til Finance and Operations-apps eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-223">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="2cdf7-224">Der opstod en fejl under godkendelse af orlovsanmodninger i appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="2cdf7-224">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="2cdf7-225">Hvis du modtager en fejl under forsøg på at godkende orlovsanmodninger i appen Teams, skal du prøve følgende fejlfindingstrin:</span><span class="sxs-lookup"><span data-stu-id="2cdf7-225">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="2cdf7-226">Kontrollér, at den konto, du bruger til at logge på Microsoft Teams, er den samme, som du bruger til at få adgang til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-226">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="2cdf7-227">Kontrollér, at du er en gyldig godkender af anmodningen, ved at kontrollere indstillingerne af arbejdsproces for orlovsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-227">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="2cdf7-228">Du kan finde flere oplysninger om orlovsarbejdsprocesser i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-228">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="2cdf7-229">Kendte problemer med tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="2cdf7-229">Known accessibility issues</span></span>

<span data-ttu-id="2cdf7-230">Human Resources-appen i Teams har følgende tilgængelighedsproblemer, som vi arbejder på at løse i fremtidige versioner.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-230">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="2cdf7-231">Udsted</span><span class="sxs-lookup"><span data-stu-id="2cdf7-231">Issue</span></span> | <span data-ttu-id="2cdf7-232">Løsning eller forklaring</span><span class="sxs-lookup"><span data-stu-id="2cdf7-232">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="2cdf7-233">Hvis du zoomer til 400 % på skrivebordet, skjules nogle af handlingsknapperne i visningen.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-233">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="2cdf7-234">Vi anbefaler, at du bruger et forstørrelsesglas i stedet, indtil vi kan understøtte dette zoomniveau.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-234">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="2cdf7-235">Under fanen **Fridage** annoncerer VoiceOver en knaphandling under læsning af overskriften til gitteret for fridage.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-235">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="2cdf7-236">Overskriften og elementerne i gitteret grupperes efter år, og de kan skjules.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-236">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="2cdf7-237">VoiceOver fortolker dette som et element, der kræver en handling, men det er ikke.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-237">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="2cdf7-238">Under fanen **Fridage** er der en ekstra strygebevægelse, når du navigerer til **Årsagskode** i en ny anmodning.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-238">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="2cdf7-239">Der er ikke noget skjult kontrolelement, som strygenavigationen forsøger at få adgang til.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-239">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="2cdf7-240">Hvis du lave en strygebevægelser under fanen **Fridage**, mens kalenderen er åben, havner du uden for kontrolelementet i stedet for øverst i en ny anmodning, eller når du redigerer en anmodning.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-240">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="2cdf7-241">Når du når **Gå til i dag**, skal du betragte det som slutningen af kontrolelementet og stryge i modsatte retning for at gå tilbage til toppen.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-241">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="2cdf7-242">Under fanen **Chat** springer fokus tilbage til toppen, når du angiver en dato, mens du bruger hjælpeværktøjet eller tastaturnavigation.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-242">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="2cdf7-243">Tabulér, indtil du når til inputområdet igen.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-243">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="2cdf7-244">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="2cdf7-244">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="2cdf7-245">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="2cdf7-245">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="2cdf7-246">Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-246">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="2cdf7-247">Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-247">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="2cdf7-248">Læs mere om LUIS [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-248">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="2cdf7-249">LUIS-tjenesten gør formålet utvetydeligt eller forstår hensigten med brugerinputtet (i dette tilfælde er hensigten at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-249">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="2cdf7-250">Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-250">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="2cdf7-251">Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-251">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="2cdf7-252">LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-252">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="2cdf7-253">Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-253">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="2cdf7-254">Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-254">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="2cdf7-255">Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-255">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="2cdf7-256">Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-256">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="2cdf7-257">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="2cdf7-257">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="2cdf7-258">Når du bruger Dynamics 365 Human Resources-appen i Microsoft Teams, kan visse kundedata flyde uden for det geografiske område, hvor din lejers personaleservice er installeret.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-258">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="2cdf7-259">Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsgangsopgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-259">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="2cdf7-260">Disse data kan gemmes i Microsoft Azure Event Grid i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-260">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2cdf7-261">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-261">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="2cdf7-262">Indholdet i samtalen med chatrobotten i Human Resources-appen kan gemmes i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-262">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="2cdf7-263">Disse data kan gemmes i Azure Cosmos DB i op til 24 timer og kan behandles uden for det geografiske område, hvor din lejers Human Resources-tjeneste er udrullet. Data, der er undervejs, og inaktive data krypteres og bruges ikke af Microsoft eller underprocesser til træning eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="2cdf7-263">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="2cdf7-264">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-264">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="2cdf7-265">Hvis du vil begrænse adgangen til Human Resources-appen i Microsoft Teams for din organisation eller brugere i organisationen, skal du se [Styre apptilladelsespolitikker i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="2cdf7-265">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="2cdf7-266">Se også</span><span class="sxs-lookup"><span data-stu-id="2cdf7-266">See also</span></span>

[<span data-ttu-id="2cdf7-267">Downloade og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="2cdf7-267">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="2cdf7-268">Microsoft Teams Hjælp-center</span><span class="sxs-lookup"><span data-stu-id="2cdf7-268">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="2cdf7-269">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="2cdf7-269">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]