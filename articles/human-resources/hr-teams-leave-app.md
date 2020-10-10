---
title: Administrere anmodninger i Teams
description: I dette emne kan du se, hvordan du anmoder om fri i Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/03/2020
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
ms.openlocfilehash: c7b74983cbddf661456b0a65939e272078d59f6d
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828938"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="47347-103">Administrere anmodninger i Teams</span><span class="sxs-lookup"><span data-stu-id="47347-103">Manage leave requests in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="47347-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan du hurtigt anmode om at få fri og se dine flekskontooplysninger direkte i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="47347-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="47347-105">Du kan interagere med en robot for at anmode om oplysninger og starte en orlovsanmodning.</span><span class="sxs-lookup"><span data-stu-id="47347-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="47347-106">Fanen **Fridage** giver mere detaljerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="47347-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="47347-107">Du kan også sende personoplysninger om dine kommende fridage i teams og chatte uden for Human Resource-appen.</span><span class="sxs-lookup"><span data-stu-id="47347-107">In addition, you can send people information about your upcoming time off in teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="47347-108">Installere appen</span><span class="sxs-lookup"><span data-stu-id="47347-108">Install the app</span></span>

<span data-ttu-id="47347-109">Du kan finde Personale-appen i storen til Teams.</span><span class="sxs-lookup"><span data-stu-id="47347-109">You can find the Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="47347-110">I Microsoft Teams skal du vælge ellipserne.</span><span class="sxs-lookup"><span data-stu-id="47347-110">In Microsoft Teams, select the ellipses.</span></span>

   ![Ellipser i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-ellipses.png)
 
2. <span data-ttu-id="47347-112">Søg efter Dynamics 365 Human Resources, og vælg derefter feltet **Personale**.</span><span class="sxs-lookup"><span data-stu-id="47347-112">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

   ![HR-feltet i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-human-resources-tile.png)

3. <span data-ttu-id="47347-114">Klik på knappen **Tilføj** for at installere appen.</span><span class="sxs-lookup"><span data-stu-id="47347-114">Select the **Add** button to install the app.</span></span>

   ![Installer orlovsappen i Personale i Teams](./media/hr-teams-leave-app-in-store.png)

<span data-ttu-id="47347-116">Hvis appen ikke automatisk logger dig på, skal du vælge fanen **Indstillinger** for at logge på.</span><span class="sxs-lookup"><span data-stu-id="47347-116">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

![Fanen Indstillinger i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-settings-tab.png)

> [!NOTE]
> <span data-ttu-id="47347-118">Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer.</span><span class="sxs-lookup"><span data-stu-id="47347-118">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="47347-119">Hvis du har adgang til mere end én forekomst af Personale, kan du vælge, hvilket miljø du vil oprette forbindelse til, under fanen **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="47347-119">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="47347-120">Appen understøtter nu sikkerhedsrollen Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="47347-120">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="47347-121">Brug botten</span><span class="sxs-lookup"><span data-stu-id="47347-121">Use the bot</span></span>

<span data-ttu-id="47347-122">Når appen er installeret, vises en velkomstmeddelelse, der giver dig besked om, hvilke typer handlinger botten kan udføre på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="47347-122">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

![Botvelkomstmeddelelse i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot.png)
 
> [!NOTE]
> <span data-ttu-id="47347-124">Når du interagerer med bot for første gang, skal du muligvis logge på.</span><span class="sxs-lookup"><span data-stu-id="47347-124">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="47347-125">Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer.</span><span class="sxs-lookup"><span data-stu-id="47347-125">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="47347-126">Du kan bede bot om at:</span><span class="sxs-lookup"><span data-stu-id="47347-126">You can ask the bot to:</span></span>

- <span data-ttu-id="47347-127">Vise oplysninger om flekskontoen for hver orlovstype, du er tilmeldt.</span><span class="sxs-lookup"><span data-stu-id="47347-127">Show time-off balance information for each leave type you're enrolled in.</span></span>

   ![Vise konti i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-balances.png)
 
- <span data-ttu-id="47347-129">Vise flere detaljer om en bestemt orlovstype.</span><span class="sxs-lookup"><span data-stu-id="47347-129">Show additional details about a specific leave type.</span></span>

   ![Vise detaljer i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-details.png)

- <span data-ttu-id="47347-131">Starte en anmodning om en orlov for dig.</span><span class="sxs-lookup"><span data-stu-id="47347-131">Start a leave request for you.</span></span>

   ![Anmodning om orlov i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-request.png)
 
<span data-ttu-id="47347-133">Når du har startet en orlovsanmodning, kan du justere dagene direkte på kortet.</span><span class="sxs-lookup"><span data-stu-id="47347-133">After you start a leave request, you can adjust the days right within the card.</span></span>

![Redigering af anmodning i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-edit.png)
 
<span data-ttu-id="47347-135">Når du er færdig med at angive oplysninger, skal du vælge **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="47347-135">When you're done entering information, select **Submit** to submit it for approval.</span></span> <span data-ttu-id="47347-136">Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="47347-136">You can also select **Save as draft** to come back to it later.</span></span>

![Afsendelse af anmodning i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-bot-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="47347-138">Administrere din orlov i Teams</span><span class="sxs-lookup"><span data-stu-id="47347-138">Manage your leave in Teams</span></span>

<span data-ttu-id="47347-139">Fanen **Fri** gør det muligt at vise:</span><span class="sxs-lookup"><span data-stu-id="47347-139">The **Time off** tab allows you to view:</span></span>

- <span data-ttu-id="47347-140">Kontooplysninger om hver orlovstype, du er tilmeldt</span><span class="sxs-lookup"><span data-stu-id="47347-140">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="47347-141">Kommende orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="47347-141">Upcoming leave requests</span></span>

- <span data-ttu-id="47347-142">Anmodninger om fri</span><span class="sxs-lookup"><span data-stu-id="47347-142">Time-off requests</span></span>

- <span data-ttu-id="47347-143">kladdeorlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="47347-143">Draft leave requests</span></span>

![Fanen Fri i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab.png)
 
### <a name="create-a-new-request"></a><span data-ttu-id="47347-145">Oprette en ny anmodning</span><span class="sxs-lookup"><span data-stu-id="47347-145">Create a new request</span></span>

1. <span data-ttu-id="47347-146">Hvis du vil oprette en ny anmodning, skal du vælge **Ny anmodning**.</span><span class="sxs-lookup"><span data-stu-id="47347-146">To create a new leave request, select **New request**.</span></span>

   ![Ny anmodning i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab-new.png)

2. <span data-ttu-id="47347-148">Angiv den eller de dage, du vil have en fridag, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="47347-148">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Tilføj fridag i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab-add.png)

3. <span data-ttu-id="47347-150">Angiv en årsagskode, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="47347-150">If applicable, enter a reason code.</span></span> <span data-ttu-id="47347-151">Skriv også eventuelle kommentarer, og tilføj evt. vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="47347-151">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="47347-152">Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="47347-152">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="47347-153">Du kan også indtaste **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="47347-153">You can also type **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="47347-154">Administrere kladdeanmodninger</span><span class="sxs-lookup"><span data-stu-id="47347-154">Manage draft requests</span></span>

1. <span data-ttu-id="47347-155">Vælg fanen **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="47347-155">Select the **Drafts** tab.</span></span>

   ![Fanen Kladder i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-drafts-tab.png)

2. <span data-ttu-id="47347-157">Vælg blyanten for at redigere anmodningen, eller vælg papirkurven, som kan slette anmodningen.</span><span class="sxs-lookup"><span data-stu-id="47347-157">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="47347-158">Foretag eventuelle nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="47347-158">Make any necessary changes.</span></span> <span data-ttu-id="47347-159">Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="47347-159">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="47347-160">Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="47347-160">You can also select **Save as draft** to come back to it later.</span></span>

   ![Redigering af kladde i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-drafts-edit.png)
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="47347-162">Besvare Teams-beskeder</span><span class="sxs-lookup"><span data-stu-id="47347-162">Respond to Teams notifications</span></span>

<span data-ttu-id="47347-163">Når du eller en arbejder, du er godkender for, sender en anmodning om orlov, modtager du en besked i appen Personale i Teams.</span><span class="sxs-lookup"><span data-stu-id="47347-163">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="47347-164">Du kan vælge beskeden for at få den vist.</span><span class="sxs-lookup"><span data-stu-id="47347-164">You can select the notification to view it.</span></span> <span data-ttu-id="47347-165">Beskeder vises også i **Chat**-området.</span><span class="sxs-lookup"><span data-stu-id="47347-165">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="47347-166">Hvis du er godkender, kan du vælge **Godkend** eller **Afvis** i beskeden.</span><span class="sxs-lookup"><span data-stu-id="47347-166">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="47347-167">Du kan også angive en valgfri meddelelse.</span><span class="sxs-lookup"><span data-stu-id="47347-167">You can also provide an optional message.</span></span>

![Besked om orlovsanmodning i Teams-appen Personale](./media/hr-teams-leave-app-notification.png)

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="47347-169">Sende kommende oplysninger om fridage til dine kolleger</span><span class="sxs-lookup"><span data-stu-id="47347-169">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="47347-170">Når du har installeret Human Resources-appen for Teams, kan du nemt sende oplysninger om dine kommende fridage til dine kolleger i teams eller chatsamtaler.</span><span class="sxs-lookup"><span data-stu-id="47347-170">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="47347-171">I et team eller en chat i Teams skal du vælge knappen Human Resources under chatvinduet.</span><span class="sxs-lookup"><span data-stu-id="47347-171">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Knappen Human Resources under chatvinduet](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="47347-173">Vælg den orlovsanmodning, du vil dele.</span><span class="sxs-lookup"><span data-stu-id="47347-173">Select the leave request you want to share.</span></span> <span data-ttu-id="47347-174">Hvis du vil dele en kladde af orlovsanmodningen, skal du vælge **Kladder** først.</span><span class="sxs-lookup"><span data-stu-id="47347-174">If you want to share a draft leave request, select **Drafts** first.</span></span>

   ![Vælge en kommende orlovsanmodning til at dele](./media/hr-teams-leave-app-chat-search.png)

<span data-ttu-id="47347-176">Din orlovsanmodning vises i chatten.</span><span class="sxs-lookup"><span data-stu-id="47347-176">Your leave request will display in the chat.</span></span>

![Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-card.png)

<span data-ttu-id="47347-178">Hvis du har delt en kladdebaseret anmodning, vises den som en kladde:</span><span class="sxs-lookup"><span data-stu-id="47347-178">If you shared a draft request, it will display as a draft:</span></span>

![Kladde af Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-draft-card.png)

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="47347-180">Se dit teams orlovskalender</span><span class="sxs-lookup"><span data-stu-id="47347-180">View your team's leave calendar</span></span>

<span data-ttu-id="47347-181">Hvis du er chef med direkte underordnede, kan du få vist dit teams godkendte og afventende fravær.</span><span class="sxs-lookup"><span data-stu-id="47347-181">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="47347-182">I appen Personale i Teams skal du vælge **Fri**.</span><span class="sxs-lookup"><span data-stu-id="47347-182">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="47347-183">Vælg **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="47347-183">Select **Team calendar**.</span></span>

   ![Se kalender i Teams-appen Personale](./media/hr-teams-leave-app-view-calendar.png)

<span data-ttu-id="47347-185">I kalenderen vises dine direkte underordnedes godkendte og afventende fravær.</span><span class="sxs-lookup"><span data-stu-id="47347-185">The calendar displays your direct reports' approved and pending time off.</span></span>

![Fraværskalender i Teams-appen Personale](./media/hr-teams-leave-app-calendar.png)

## <a name="privacy-notice"></a><span data-ttu-id="47347-187">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="47347-187">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="47347-188">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="47347-188">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="47347-189">Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål.</span><span class="sxs-lookup"><span data-stu-id="47347-189">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="47347-190">Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="47347-190">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="47347-191">Læs mere om LUIS [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="47347-191">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="47347-192">LUIS-tjenesten gør formålet utvetydeligt eller forstår formålet med brugerinputtet (i dette tilfælde er formålet at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso).</span><span class="sxs-lookup"><span data-stu-id="47347-192">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="47347-193">Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="47347-193">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="47347-194">Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse.</span><span class="sxs-lookup"><span data-stu-id="47347-194">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="47347-195">LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="47347-195">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="47347-196">Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen.</span><span class="sxs-lookup"><span data-stu-id="47347-196">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="47347-197">Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="47347-197">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="47347-198">Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="47347-198">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="47347-199">Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="47347-199">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="47347-200">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="47347-200">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="47347-201">Når du bruger Dynamics 365 Human Resources-appen i Microsoft Teams, kan visse kundedata flyde uden for det geografiske område, hvor din lejers personaleservice er installeret.</span><span class="sxs-lookup"><span data-stu-id="47347-201">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="47347-202">Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsgangsopgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="47347-202">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="47347-203">Disse data kan gemmes i Microsoft Azure Event Grid i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester.</span><span class="sxs-lookup"><span data-stu-id="47347-203">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="47347-204">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="47347-204">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="47347-205">Indholdet i samtalen med chatrobotten i Human Resources-appen kan gemmes i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="47347-205">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="47347-206">Disse data kan gemmes i Azure Cosmos DB i op til 24 timer og kan behandles uden for det geografiske område, hvor din lejers Human Resources-tjeneste er udrullet. Data, der er undervejs, og inaktive data krypteres og bruges ikke af Microsoft eller underprocesser til træning eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="47347-206">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="47347-207">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="47347-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="47347-208">Hvis du vil begrænse adgangen til Human Resources-appen i Microsoft Teams for din organisation eller brugere i organisationen, skal du se [Styre apptilladelsespolitikker i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="47347-208">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="47347-209">Se også</span><span class="sxs-lookup"><span data-stu-id="47347-209">See also</span></span>

[<span data-ttu-id="47347-210">Downloade og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="47347-210">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="47347-211">Microsoft Teams Hjælp-center</span><span class="sxs-lookup"><span data-stu-id="47347-211">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="47347-212">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="47347-212">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)
