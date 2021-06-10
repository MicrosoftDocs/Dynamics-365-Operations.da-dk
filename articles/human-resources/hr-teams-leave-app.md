---
title: Administrere anmodninger i Teams
description: I dette emne kan du se, hvordan du anmoder om fri i Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
ms.date: 05/25/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeaveAbsenceWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 661bb8369fe4dbe6cdf6ee0fb05d16f4350ecf5a
ms.sourcegitcommit: c5c8f19a696ad4a3d68dffd63bfe7b484b999d2b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/25/2021
ms.locfileid: "6097253"
---
# <a name="manage-leave-requests-in-teams"></a><span data-ttu-id="88aaf-103">Administrere fraværsanmodninger i Teams</span><span class="sxs-lookup"><span data-stu-id="88aaf-103">Manage leave requests in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="88aaf-104">Med Dynamics 365 Human Resources-appen i Microsoft Teams kan du hurtigt anmode om at få fri og se dine flekskontooplysninger direkte i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="88aaf-104">The Dynamics 365 Human Resources app in Microsoft Teams lets you quickly request time off and view your time-off balance information right in Microsoft Teams.</span></span> <span data-ttu-id="88aaf-105">Du kan interagere med en robot for at anmode om oplysninger og starte en orlovsanmodning.</span><span class="sxs-lookup"><span data-stu-id="88aaf-105">You can interact with a bot to request information and start a leave request.</span></span> <span data-ttu-id="88aaf-106">Fanen **Fridage** giver mere detaljerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="88aaf-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="88aaf-107">Du kan også sende personer oplysninger om dine kommende fridage i Teams og chatte uden for Human Resource-appen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-107">You can also send people information about your upcoming time off in Teams and chats outside the Human Resources app.</span></span>

## <a name="install-the-app"></a><span data-ttu-id="88aaf-108">Installere appen</span><span class="sxs-lookup"><span data-stu-id="88aaf-108">Install the app</span></span>

<span data-ttu-id="88aaf-109">Du kan finde appen Dynamics 365 Human Resources i lageret til Teams.</span><span class="sxs-lookup"><span data-stu-id="88aaf-109">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span>

1. <span data-ttu-id="88aaf-110">Gå til listen over apps i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="88aaf-110">In Microsoft Teams, navigate to the list of apps.</span></span>
 
2. <span data-ttu-id="88aaf-111">Søg efter Dynamics 365 Human Resources, og vælg derefter feltet **Human Resources**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-111">Search for Dynamics 365 Human Resources, and then select the **Human Resources** tile.</span></span>

3. <span data-ttu-id="88aaf-112">Klik på knappen **Tilføj** for at installere appen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-112">Select the **Add** button to install the app.</span></span>

<span data-ttu-id="88aaf-113">Hvis appen ikke automatisk logger dig på, skal du vælge fanen **Indstillinger** for at logge på.</span><span class="sxs-lookup"><span data-stu-id="88aaf-113">If the app doesn't automatically sign you in, select the **Settings** tab to sign in.</span></span>

> [!NOTE]
> <span data-ttu-id="88aaf-114">Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer.</span><span class="sxs-lookup"><span data-stu-id="88aaf-114">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span> 

<span data-ttu-id="88aaf-115">Hvis du har adgang til mere end én forekomst af Human Resources, kan du vælge, hvilket miljø du vil oprette forbindelse til, under fanen **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-115">If you have access to more than one instance of Human Resources, you can select which environment you want to connect to in the **Settings** tab.</span></span>

> [!NOTE]
> <span data-ttu-id="88aaf-116">Appen understøtter nu sikkerhedsrollen Systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="88aaf-116">The app now supports the System Administrator security role.</span></span>
 
## <a name="use-the-bot"></a><span data-ttu-id="88aaf-117">Brug botten</span><span class="sxs-lookup"><span data-stu-id="88aaf-117">Use the bot</span></span>

<span data-ttu-id="88aaf-118">Når appen er installeret, vises en velkomstmeddelelse, der giver dig besked om, hvilke typer handlinger botten kan udføre på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="88aaf-118">After the app installs, a welcome message appears, letting you know the types of actions the bot can take on your behalf.</span></span>

> [!NOTE]
> <span data-ttu-id="88aaf-119">Når du interagerer med bot for første gang, skal du muligvis logge på.</span><span class="sxs-lookup"><span data-stu-id="88aaf-119">When first interacting with the bot, you might need to sign in.</span></span> <span data-ttu-id="88aaf-120">Hvis du ikke kan se logondialogboksen, skal du kontrollere browserindstillingerne for at tillade pop op-vinduer.</span><span class="sxs-lookup"><span data-stu-id="88aaf-120">If you don’t see a sign-in dialog box, check your browser settings to allow pop-ups.</span></span>

<span data-ttu-id="88aaf-121">Du kan bede bot om at:</span><span class="sxs-lookup"><span data-stu-id="88aaf-121">You can ask the bot to:</span></span>

- <span data-ttu-id="88aaf-122">Få vist dine aktuelle orlovssaldi.</span><span class="sxs-lookup"><span data-stu-id="88aaf-122">View your current leave balances.</span></span> <span data-ttu-id="88aaf-123">Send f.eks. meddelelsen "Vis orlovssaldi".</span><span class="sxs-lookup"><span data-stu-id="88aaf-123">For example, send a message that says, "View leave balances."</span></span>

- <span data-ttu-id="88aaf-124">Starte en anmodning om en orlov for dig.</span><span class="sxs-lookup"><span data-stu-id="88aaf-124">Start a leave request for you.</span></span> <span data-ttu-id="88aaf-125">Send f.eks. en meddelelse med teksten "Tag fri" eller "Jeg ønsker holde ferie næste torsdag og fredag" for at være mere specifik, når du anmoder om orlov for ferietypen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-125">For example, send a message that says, “Take time off” or “I want to take vacation time off next Thursday and Friday” to be more specific for requesting leave for the vacation leave type.</span></span> 

  ![Starte en anmodning om orlov i Teams-chat](./media/hr-teams-leave-app-initiate.png)

- <span data-ttu-id="88aaf-127">Chatrobotten udfylder en orlovsanmodning for dig.</span><span class="sxs-lookup"><span data-stu-id="88aaf-127">The chat bot will populate a leave request for you.</span></span> <span data-ttu-id="88aaf-128">Vælg **Anmod om fri**, og rediger detaljerne om anmodningen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-128">Select **Request time off** and edit the details for your request.</span></span>

   <span data-ttu-id="88aaf-129">Hvis du vil sende orlovsanmodninger for flere orlovstyper for den samme dato, skal du vælge indstillingen **Opdel dag med** fra menuen **Flere indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-129">If you want to submit leave requests for multiple leave types for the same date, select the **Split day with** option from the **More options** menu.</span></span> 

   <span data-ttu-id="88aaf-130">Hvis du vælger en halv dags orlov, og orlovsanmodningsenheden er i dage, kan du angive, om du vil anmode om fri første halvdel af dagen eller anden halvdel af dagen, ved at vælge indstillingen **Halvdagsdefinition** i menuen **Flere indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-130">If you select a half day leave when the leave request unit is in days, you can specify whether you want to request time off the first half day or the second half day by selecting the **Half day definition** option from the **More options** menu.</span></span>
   
   ![Halvdagsdefintioner](./media/HalfDayDefinitions.png)

- <span data-ttu-id="88aaf-132">Når du er færdig med at redigere oplysningerne om din anmodning om orlov, skal du vælge **Send** for at sende den til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="88aaf-132">When you're done editing your leave request details, select **Submit** to submit it for approval.</span></span>

  ![Sende orlovsanmodning](./media/hr-teams-leave-app-submit.png)

## <a name="manage-your-leave-in-teams"></a><span data-ttu-id="88aaf-134">Administrere din orlov i Teams</span><span class="sxs-lookup"><span data-stu-id="88aaf-134">Manage your leave in Teams</span></span>

<span data-ttu-id="88aaf-135">Fanen **Fri** gør det muligt at vise:</span><span class="sxs-lookup"><span data-stu-id="88aaf-135">The **Time off** tab allows you to view:</span></span> 

- <span data-ttu-id="88aaf-136">Kontooplysninger om hver orlovstype, du er tilmeldt</span><span class="sxs-lookup"><span data-stu-id="88aaf-136">Balance information for each leave type you're enrolled in</span></span>

- <span data-ttu-id="88aaf-137">Kommende orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="88aaf-137">Upcoming leave requests</span></span>

- <span data-ttu-id="88aaf-138">Anmodninger om fri</span><span class="sxs-lookup"><span data-stu-id="88aaf-138">Time-off requests</span></span>

- <span data-ttu-id="88aaf-139">kladdeorlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="88aaf-139">Draft leave requests</span></span>
 
### <a name="create-a-new-request"></a><span data-ttu-id="88aaf-140">Oprette en ny anmodning</span><span class="sxs-lookup"><span data-stu-id="88aaf-140">Create a new request</span></span>

1. <span data-ttu-id="88aaf-141">Hvis du vil oprette en ny anmodning, skal du vælge **Ny anmodning**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-141">To create a new leave request, select **New request**.</span></span>

2. <span data-ttu-id="88aaf-142">Angiv den eller de dage, du vil have en fridag, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-142">Enter the day or days you want to take off, and then select **Add**.</span></span>

   ![Tilføj fridag i orlovsappen i Human Resources i Teams](./media/TimeOffHours.png)

3. <span data-ttu-id="88aaf-144">Angiv en årsagskode, hvis det er relevant.</span><span class="sxs-lookup"><span data-stu-id="88aaf-144">If applicable, enter a reason code.</span></span> <span data-ttu-id="88aaf-145">Skriv også eventuelle kommentarer, og tilføj evt. vedhæftede filer.</span><span class="sxs-lookup"><span data-stu-id="88aaf-145">Also enter any comments and add any attachments.</span></span>

4. <span data-ttu-id="88aaf-146">Vælg indstillingen **Opdel dag med** i menuen **Flere indstillinger**, hvis du vil sende flere orlovsanmodninger for den samme dato for forskellige orlovstyper.</span><span class="sxs-lookup"><span data-stu-id="88aaf-146">Select the **Split day with** option from the **More options** menu if you want to submit multiple leave request entries for the same date for different leave types.</span></span>

5. <span data-ttu-id="88aaf-147">Vælg indstillingen **Halvdagsdefinition** for at angive, om du vil anmode om fri den første halvdel af dagen eller den anden halvdel af dagen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-147">Select the **Half day definition** option to specify if you want to request the first half day off or the second half day off.</span></span> <span data-ttu-id="88aaf-148">Denne indstilling er tilgængelig, når orlovsanmodningsenheden er i dage, og det ønskede antal dage er 0,5 dage.</span><span class="sxs-lookup"><span data-stu-id="88aaf-148">This option is available when the leave request unit is in days and the amount requested is 0.5 days.</span></span>

6. <span data-ttu-id="88aaf-149">Når du er færdig med at angive oplysninger, skal du vælge **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="88aaf-149">When you're done entering information, enter **Submit** to submit it for approval.</span></span> <span data-ttu-id="88aaf-150">Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="88aaf-150">You can also enter **Save as draft** to come back to it later.</span></span>

### <a name="manage-draft-requests"></a><span data-ttu-id="88aaf-151">Administrere kladdeanmodninger</span><span class="sxs-lookup"><span data-stu-id="88aaf-151">Manage draft requests</span></span>

1. <span data-ttu-id="88aaf-152">Vælg fanen **Kladder**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-152">Select the **Drafts** tab.</span></span>

2. <span data-ttu-id="88aaf-153">Vælg blyanten for at redigere anmodningen, eller vælg papirkurven, som kan slette anmodningen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-153">Select the pencil to edit the request, or select the trash can to delete the request.</span></span>

3. <span data-ttu-id="88aaf-154">Foretag eventuelle nødvendige ændringer.</span><span class="sxs-lookup"><span data-stu-id="88aaf-154">Make any necessary changes.</span></span> <span data-ttu-id="88aaf-155">Når du er færdig med at angive oplysninger, skal du skrive **Send** for at sende dem til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="88aaf-155">When you're done entering information, type **Submit** to submit it for approval.</span></span> <span data-ttu-id="88aaf-156">Du kan også vælge **Gem som kladde** for at vende tilbage til den senere.</span><span class="sxs-lookup"><span data-stu-id="88aaf-156">You can also select **Save as draft** to come back to it later.</span></span>
   
### <a name="respond-to-teams-notifications"></a><span data-ttu-id="88aaf-157">Besvare Teams-beskeder</span><span class="sxs-lookup"><span data-stu-id="88aaf-157">Respond to Teams notifications</span></span>

<span data-ttu-id="88aaf-158">Når du eller en arbejder, du er godkender for, sender en anmodning om orlov, modtager du en besked i appen Human Resources i Teams.</span><span class="sxs-lookup"><span data-stu-id="88aaf-158">When you or a worker you're an approver for submits a leave request, you'll receive a notification in the Human Resources app in Teams.</span></span> <span data-ttu-id="88aaf-159">Du kan vælge beskeden for at få den vist.</span><span class="sxs-lookup"><span data-stu-id="88aaf-159">You can select the notification to view it.</span></span> <span data-ttu-id="88aaf-160">Beskeder vises også i **Chat**-området.</span><span class="sxs-lookup"><span data-stu-id="88aaf-160">Notifications also appear in the **Chat** area.</span></span>

<span data-ttu-id="88aaf-161">Hvis du er godkender, kan du vælge **Godkend** eller **Afvis** i beskeden.</span><span class="sxs-lookup"><span data-stu-id="88aaf-161">If you're an approver, you can select **Approve** or **Deny** in the notification.</span></span> <span data-ttu-id="88aaf-162">Du kan også angive en valgfri meddelelse.</span><span class="sxs-lookup"><span data-stu-id="88aaf-162">You can also provide an optional message.</span></span>

## <a name="send-upcoming-time-off-information-to-your-coworkers"></a><span data-ttu-id="88aaf-163">Sende kommende oplysninger om fridage til dine kolleger</span><span class="sxs-lookup"><span data-stu-id="88aaf-163">Send upcoming time-off information to your coworkers</span></span>

<span data-ttu-id="88aaf-164">Når du har installeret Human Resources-appen for Teams, kan du nemt sende oplysninger om dine kommende fridage til dine kolleger i teams eller chatsamtaler.</span><span class="sxs-lookup"><span data-stu-id="88aaf-164">After you install the Human Resources app for Teams, you can easily send information about your upcoming time off to your coworkers in teams or chats.</span></span>

1. <span data-ttu-id="88aaf-165">I et team eller en chat i Teams skal du vælge knappen Human Resources under chatvinduet.</span><span class="sxs-lookup"><span data-stu-id="88aaf-165">In a team or chat in Teams, select the Human Resources button below the chat window.</span></span>

   ![Knappen Human Resources under chatvinduet](./media/hr-teams-leave-app-chat-button.png)

2. <span data-ttu-id="88aaf-167">Vælg den orlovsanmodning, du vil dele.</span><span class="sxs-lookup"><span data-stu-id="88aaf-167">Select the leave request you want to share.</span></span> <span data-ttu-id="88aaf-168">Hvis du vil dele en kladde af orlovsanmodningen, skal du vælge **Kladder** først.</span><span class="sxs-lookup"><span data-stu-id="88aaf-168">If you want to share a draft leave request, select **Drafts** first.</span></span>

<span data-ttu-id="88aaf-169">Din orlovsanmodning vises i chatten.</span><span class="sxs-lookup"><span data-stu-id="88aaf-169">Your leave request will display in the chat.</span></span>

<span data-ttu-id="88aaf-170">Hvis du har delt en kladdebaseret anmodning, vises den som en kladde.</span><span class="sxs-lookup"><span data-stu-id="88aaf-170">If you shared a draft request, it will display as a draft.</span></span>

## <a name="view-your-teams-leave-calendar"></a><span data-ttu-id="88aaf-171">Se dit teams orlovskalender</span><span class="sxs-lookup"><span data-stu-id="88aaf-171">View your team's leave calendar</span></span>

<span data-ttu-id="88aaf-172">Hvis du er chef med direkte underordnede, kan du få vist dit teams godkendte og afventende fravær.</span><span class="sxs-lookup"><span data-stu-id="88aaf-172">If you're a manager with direct reports, you can view your team's approved and pending time off.</span></span>

1. <span data-ttu-id="88aaf-173">I appen Human Resources i Teams skal du vælge **Fri**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-173">In the Human Resources app in Teams, select **Time off**.</span></span>

2. <span data-ttu-id="88aaf-174">Vælg **Teamkalender**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-174">Select **Team calendar**.</span></span> <span data-ttu-id="88aaf-175">I kalenderen vises dine direkte underordnedes godkendte og afventende fravær.</span><span class="sxs-lookup"><span data-stu-id="88aaf-175">The calendar displays your direct reports' approved and pending time off.</span></span>

   > [!NOTE]
   > <span data-ttu-id="88aaf-176">Hvis du ikke kan se teamkalenderen, kan du bede din administrator om at aktivere den.</span><span class="sxs-lookup"><span data-stu-id="88aaf-176">If you can't see the team calendar, ask your admin to enable it.</span></span> <span data-ttu-id="88aaf-177">Du kan finde flere oplysninger i [Installere og konfigurere](hr-admin-teams-leave-app.md#install-and-setup).</span><span class="sxs-lookup"><span data-stu-id="88aaf-177">For more information, see [Install and setup](hr-admin-teams-leave-app.md#install-and-setup).</span></span>

## <a name="supported-languages"></a><span data-ttu-id="88aaf-178">Understøttede sprog</span><span class="sxs-lookup"><span data-stu-id="88aaf-178">Supported languages</span></span>

<span data-ttu-id="88aaf-179">Appen Dynamics 365 Human Resources i Teams understøtter følgende sprog:</span><span class="sxs-lookup"><span data-stu-id="88aaf-179">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="88aaf-180">Landestandard-id</span><span class="sxs-lookup"><span data-stu-id="88aaf-180">Locale ID</span></span> | <span data-ttu-id="88aaf-181">Sprog</span><span class="sxs-lookup"><span data-stu-id="88aaf-181">Language</span></span> |
| --- | --- |
| <span data-ttu-id="88aaf-182">de-DE</span><span class="sxs-lookup"><span data-stu-id="88aaf-182">de-DE</span></span> | <span data-ttu-id="88aaf-183">Tysk (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="88aaf-183">German (Germany)</span></span> |
| <span data-ttu-id="88aaf-184">es-ES</span><span class="sxs-lookup"><span data-stu-id="88aaf-184">es-ES</span></span> | <span data-ttu-id="88aaf-185">Spansk (Spanien)</span><span class="sxs-lookup"><span data-stu-id="88aaf-185">Spanish (Spain)</span></span> |
| <span data-ttu-id="88aaf-186">es-MX</span><span class="sxs-lookup"><span data-stu-id="88aaf-186">es-MX</span></span> | <span data-ttu-id="88aaf-187">Spansk (Mexico)</span><span class="sxs-lookup"><span data-stu-id="88aaf-187">Spanish (Mexico)</span></span> |
| <span data-ttu-id="88aaf-188">fr-CA</span><span class="sxs-lookup"><span data-stu-id="88aaf-188">fr-CA</span></span> | <span data-ttu-id="88aaf-189">Fransk (Canada)</span><span class="sxs-lookup"><span data-stu-id="88aaf-189">French (Canada)</span></span> |
| <span data-ttu-id="88aaf-190">fr-FR</span><span class="sxs-lookup"><span data-stu-id="88aaf-190">fr-FR</span></span> | <span data-ttu-id="88aaf-191">Fransk (Frankrig)</span><span class="sxs-lookup"><span data-stu-id="88aaf-191">French (France)</span></span> |
| <span data-ttu-id="88aaf-192">it-IT</span><span class="sxs-lookup"><span data-stu-id="88aaf-192">it-IT</span></span> | <span data-ttu-id="88aaf-193">Italiensk (Italien)</span><span class="sxs-lookup"><span data-stu-id="88aaf-193">Italian (Italy)</span></span> |
| <span data-ttu-id="88aaf-194">nl-NL</span><span class="sxs-lookup"><span data-stu-id="88aaf-194">nl-NL</span></span> | <span data-ttu-id="88aaf-195">Hollandsk (Nederlandene)</span><span class="sxs-lookup"><span data-stu-id="88aaf-195">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="88aaf-196">pt-BR</span><span class="sxs-lookup"><span data-stu-id="88aaf-196">pt-BR</span></span> | <span data-ttu-id="88aaf-197">Portugisisk (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="88aaf-197">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="88aaf-198">tr-TR</span><span class="sxs-lookup"><span data-stu-id="88aaf-198">tr-TR</span></span> | <span data-ttu-id="88aaf-199">Tyrkisk (Tyrkiet)</span><span class="sxs-lookup"><span data-stu-id="88aaf-199">Turkish (Turkey)</span></span> |
| <span data-ttu-id="88aaf-200">zh-CN</span><span class="sxs-lookup"><span data-stu-id="88aaf-200">zh-CN</span></span> | <span data-ttu-id="88aaf-201">Kinesisk (forenklet)</span><span class="sxs-lookup"><span data-stu-id="88aaf-201">Chinese (Simplified)</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="88aaf-202">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="88aaf-202">Troubleshooting</span></span>

<span data-ttu-id="88aaf-203">Hvis du har problemer med at logge på eller bruge Dynamics 365 Human Resources-appen Teams, kan du prøve at følge disse fejlfindingsinstruktioner.</span><span class="sxs-lookup"><span data-stu-id="88aaf-203">If you're having trouble signing into or using the Dynamics 365 Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="88aaf-204">Hvis du stadig har problemer efter fejlfinding, skal du kontakte Support.</span><span class="sxs-lookup"><span data-stu-id="88aaf-204">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="88aaf-205">Du kan finde flere oplysninger under [Få support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="88aaf-205">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="88aaf-206">Der kan ikke logge på appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="88aaf-206">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="88aaf-207">Hvis du ikke kan logge på appen, er det muligt, at den konto, du bruger til at logge på Microsoft Teams, ikke er knyttet til en medarbejderpost i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="88aaf-207">If you can't sign into the app, it's possible that the account you're using to sign into Microsoft Teams isn't associated with an employee record in Dynamics 365 Human Resources.</span></span> <span data-ttu-id="88aaf-208">Kontakt systemadministratoren for at sikre, at din medarbejderpost er tilknyttet korrekt.</span><span class="sxs-lookup"><span data-stu-id="88aaf-208">Contact your system administrator to ensure your employee record is correctly associated.</span></span>

### <a name="translations-dont-display-correctly"></a><span data-ttu-id="88aaf-209">Oversættelser vises ikke korrekt</span><span class="sxs-lookup"><span data-stu-id="88aaf-209">Translations don't display correctly</span></span>

<span data-ttu-id="88aaf-210">Hvis oversættelser ikke vises som forventet, skal du sørge for, at det sprog, du vælger i Teams, svarer til det sprog, der er valgt i **Brugerindstillinger** i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="88aaf-210">If translations don't display as expected, make sure the language you select in Teams matches the language selected in Human Resources **User options**.</span></span>

<span data-ttu-id="88aaf-211">I Teams skal du se på **App-sprog** i **Indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-211">In Teams, look at **App language** in **Settings**.</span></span>

![Teams-indstillinger](./media/hr-teams-leave-app-settings.png)

<span data-ttu-id="88aaf-213">Vælg **Indstillinger** i Human Resources, og vælg derefter **Brugerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="88aaf-213">In Human Resources, select **Settings** and then select **User options**.</span></span> <span data-ttu-id="88aaf-214">Kontrollér, at feltet **Sprog** svarer til feltet **App-sprog** i Teams.</span><span class="sxs-lookup"><span data-stu-id="88aaf-214">Verify that the **Language** field matches the **App language** field in Teams.</span></span>

![Brugerindstillinger i Human Resources](./media/hr-teams-leave-app-user-options.png)

<span data-ttu-id="88aaf-216">Hvis du stadig oplever oversættelsesproblemer, kan du give os besked.</span><span class="sxs-lookup"><span data-stu-id="88aaf-216">If you still experience translation issues, let us know.</span></span> <span data-ttu-id="88aaf-217">Du kan finde oplysninger i [Få support til Finance and Operations-apps eller Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span><span class="sxs-lookup"><span data-stu-id="88aaf-217">For information, see [Get support for Finance and Operations apps or Lifecycle Services (LCS)](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md?toc=%2fdynamics365%2fhuman-resources%2ftoc.json).</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="88aaf-218">Der opstod en fejl under godkendelse af orlovsanmodninger i appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="88aaf-218">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="88aaf-219">Hvis du modtager en fejl under forsøg på at godkende orlovsanmodninger i appen Teams, skal du prøve følgende fejlfindingstrin:</span><span class="sxs-lookup"><span data-stu-id="88aaf-219">If you receive an error when you're trying to approve leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="88aaf-220">Kontrollér, at den konto, du bruger til at logge på Microsoft Teams, er den samme, som du bruger til at få adgang til Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="88aaf-220">Verify that the account you're using to sign into Microsoft Teams is the same one you use for accessing Dynamics 365 Human Resources.</span></span>

2. <span data-ttu-id="88aaf-221">Kontrollér, at du er en gyldig godkender af anmodningen, ved at kontrollere indstillingerne af arbejdsproces for orlovsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="88aaf-221">Verify that you're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="88aaf-222">Du kan finde flere oplysninger om orlovsarbejdsprocesser i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="88aaf-222">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="88aaf-223">Orlovsgodkendere modtager ikke Teams-chatmeddelelser til godkendelse af orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="88aaf-223">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="88aaf-224">Sørg for, at beskeder er aktiveret for miljøet og brugeren.</span><span class="sxs-lookup"><span data-stu-id="88aaf-224">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="88aaf-225">Du kan finde flere oplysninger i [Aktivere beskeder for Human Resources-appen i Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Slå Teams-beskeder til eller fra for individuelle brugere](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="88aaf-225">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="88aaf-226">Sørg for, at brugere er logget under fanen **Chatbeskeder** med de samme legitimationsoplysninger, som de bruger til at godkende orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="88aaf-226">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="88aaf-227">Brug meddelelserne for "Log af" og derefter "Log på" for at logge på med de rette legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="88aaf-227">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="88aaf-228">Hvis problemet fortsætter, skal du kontrollere statussen for systembatchjobbet Forretningshændelser som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="88aaf-228">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="88aaf-229">Hvis det er i vente- eller udførelsesfasen, skal du tjekke ind igen om et par minutter.</span><span class="sxs-lookup"><span data-stu-id="88aaf-229">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="88aaf-230">Hvis statussen forbliver uændret, skal du logge en supportbillet, så vores team kan hjælpe med at løse problemet.</span><span class="sxs-lookup"><span data-stu-id="88aaf-230">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="known-accessibility-issues"></a><span data-ttu-id="88aaf-231">Kendte problemer med tilgængelighed</span><span class="sxs-lookup"><span data-stu-id="88aaf-231">Known accessibility issues</span></span>

<span data-ttu-id="88aaf-232">Human Resources-appen i Teams har følgende tilgængelighedsproblemer, som vi arbejder på at løse i fremtidige versioner.</span><span class="sxs-lookup"><span data-stu-id="88aaf-232">The Human Resources app in Teams has the following accessibility issues that we're working on fixing in future releases.</span></span>

| <span data-ttu-id="88aaf-233">Udsted</span><span class="sxs-lookup"><span data-stu-id="88aaf-233">Issue</span></span> | <span data-ttu-id="88aaf-234">Løsning eller forklaring</span><span class="sxs-lookup"><span data-stu-id="88aaf-234">Workaround or explanation</span></span> |
| --- | --- |
| <span data-ttu-id="88aaf-235">Hvis du zoomer til 400 % på skrivebordet, skjules nogle af handlingsknapperne i visningen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-235">Zooming to 400% on desktop hides some of the action buttons from view.</span></span> | <span data-ttu-id="88aaf-236">Vi anbefaler, at du bruger et forstørrelsesglas i stedet, indtil vi kan understøtte dette zoomniveau.</span><span class="sxs-lookup"><span data-stu-id="88aaf-236">We recommend using a magnifier instead until we can support this zoom level.</span></span> |
| <span data-ttu-id="88aaf-237">Under fanen **Fridage** annoncerer VoiceOver en knaphandling under læsning af overskriften til gitteret for fridage.</span><span class="sxs-lookup"><span data-stu-id="88aaf-237">On the **Time off** tab, voiceover announces a button action while reading the header for the time-off grid.</span></span> | <span data-ttu-id="88aaf-238">Overskriften og elementerne i gitteret grupperes efter år, og de kan skjules.</span><span class="sxs-lookup"><span data-stu-id="88aaf-238">The header and elements within the grid are grouped by year, and they're collapsible.</span></span> <span data-ttu-id="88aaf-239">VoiceOver fortolker dette som et element, der kræver en handling, men det er ikke.</span><span class="sxs-lookup"><span data-stu-id="88aaf-239">Voiceover interprets this as an actionable item, but it isn't.</span></span> |
| <span data-ttu-id="88aaf-240">Under fanen **Fridage** er der en ekstra strygebevægelse, når du navigerer til **Årsagskode** i en ny anmodning.</span><span class="sxs-lookup"><span data-stu-id="88aaf-240">On the **Time off** tab, there's an extra swipe gesture when navigating to **Reason code** in a new request.</span></span> | <span data-ttu-id="88aaf-241">Der er ikke noget skjult kontrolelement, som strygenavigationen forsøger at få adgang til.</span><span class="sxs-lookup"><span data-stu-id="88aaf-241">There is no hidden control that the swipe navigation is trying to get to.</span></span> |
| <span data-ttu-id="88aaf-242">Hvis du lave en strygebevægelser under fanen **Fridage**, mens kalenderen er åben, havner du uden for kontrolelementet i stedet for øverst i en ny anmodning, eller når du redigerer en anmodning.</span><span class="sxs-lookup"><span data-stu-id="88aaf-242">On the **Time off** tab, if you swipe while the calendar is open, you end up outside the control instead of at the top in a new request or while editing a request.</span></span> | <span data-ttu-id="88aaf-243">Når du når **Gå til i dag**, skal du betragte det som slutningen af kontrolelementet og stryge i modsatte retning for at gå tilbage til toppen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-243">When you reach **Go to today**, consider that to be the end of the control and swipe in the reverse direction to get back to the top.</span></span> |
| <span data-ttu-id="88aaf-244">Under fanen **Chat** springer fokus tilbage til toppen, når du angiver en dato, mens du bruger hjælpeværktøjet eller tastaturnavigation.</span><span class="sxs-lookup"><span data-stu-id="88aaf-244">On the **Chat** tab, the focus jumps back to the top when you enter a date while using the assistive tool or keyboard navigation.</span></span> | <span data-ttu-id="88aaf-245">Tabulér, indtil du når til inputområdet igen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-245">Tab until you reach your input area again.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="88aaf-246">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="88aaf-246">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="88aaf-247">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="88aaf-247">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="88aaf-248">Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål.</span><span class="sxs-lookup"><span data-stu-id="88aaf-248">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="88aaf-249">Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="88aaf-249">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="88aaf-250">Læs mere om LUIS [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="88aaf-250">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="88aaf-251">LUIS-tjenesten gør formålet utvetydeligt eller forstår hensigten med brugerinputtet (i dette tilfælde er hensigten at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso).</span><span class="sxs-lookup"><span data-stu-id="88aaf-251">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="88aaf-252">Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-252">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="88aaf-253">Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse.</span><span class="sxs-lookup"><span data-stu-id="88aaf-253">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="88aaf-254">LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="88aaf-254">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="88aaf-255">Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen.</span><span class="sxs-lookup"><span data-stu-id="88aaf-255">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="88aaf-256">Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="88aaf-256">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="88aaf-257">Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="88aaf-257">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="88aaf-258">Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="88aaf-258">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="88aaf-259">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="88aaf-259">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="88aaf-260">Når du bruger Dynamics 365 Human Resources-appen i Microsoft Teams, kan visse kundedata flyde uden for det geografiske område, hvor din lejers personaleservice er installeret.</span><span class="sxs-lookup"><span data-stu-id="88aaf-260">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="88aaf-261">Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsgangsopgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="88aaf-261">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="88aaf-262">Disse data kan gemmes i Microsoft Azure Event Grid i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester.</span><span class="sxs-lookup"><span data-stu-id="88aaf-262">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="88aaf-263">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="88aaf-263">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="88aaf-264">Indholdet i samtalen med chatrobotten i Human Resources-appen kan gemmes i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="88aaf-264">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="88aaf-265">Disse data kan gemmes i Azure Cosmos DB i op til 24 timer og kan behandles uden for det geografiske område, hvor din lejers Human Resources-tjeneste er udrullet. Data, der er undervejs, og inaktive data krypteres og bruges ikke af Microsoft eller underprocesser til træning eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="88aaf-265">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="88aaf-266">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="88aaf-266">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="88aaf-267">Hvis du vil begrænse adgangen til Human Resources-appen i Microsoft Teams for din organisation eller brugere i organisationen, skal du se [Styre apptilladelsespolitikker i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="88aaf-267">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="88aaf-268">Se også</span><span class="sxs-lookup"><span data-stu-id="88aaf-268">See also</span></span>

[<span data-ttu-id="88aaf-269">Downloade og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="88aaf-269">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="88aaf-270">Microsoft Teams Hjælp-center</span><span class="sxs-lookup"><span data-stu-id="88aaf-270">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="88aaf-271">Human Resources-app i Teams</span><span class="sxs-lookup"><span data-stu-id="88aaf-271">Human Resources app in Teams</span></span>](hr-admin-teams-leave-app.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
