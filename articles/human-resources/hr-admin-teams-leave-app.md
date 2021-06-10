---
title: Appen Human Resources i Teams
description: I dette emne introduceres Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
ms.date: 02/23/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: FeatureManagementWorkspace
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c1cceb15d64215cb8d5c996df792e863d466f87d
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053557"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="757ec-103">Appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="757ec-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="757ec-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan medarbejdere hurtigt anmode om at få fri og se deres flekskontooplysninger i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="757ec-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="757ec-105">Medarbejderne kan interagere med en bot for at anmode om oplysninger.</span><span class="sxs-lookup"><span data-stu-id="757ec-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="757ec-106">Fanen **Fridage** giver mere detaljerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="757ec-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="757ec-107">De kan også sende oplysninger om kommende fridage i teams og chatte uden for Human Resource-appen.</span><span class="sxs-lookup"><span data-stu-id="757ec-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Orlov via appbot i Human Resources i Teams](./media/hr-teams-leave-app-bot.png)

![Fanen Fri i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="757ec-111">Installere og konfigurere</span><span class="sxs-lookup"><span data-stu-id="757ec-111">Install and setup</span></span>

<span data-ttu-id="757ec-112">Du kan finde appen Dynamics 365 Human Resources i lageret til Teams.</span><span class="sxs-lookup"><span data-stu-id="757ec-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="757ec-113">Få flere oplysninger om installation af appen Teams i [Styre anmodninger i Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="757ec-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="757ec-114">Få flere oplysninger om styring af app-tilladelser i Teams i [Styre app-tilladelsespolitikker i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="757ec-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="757ec-115">Hvis brugerne skal have vist orlovs- og fraværskalenderen i appen, skal du aktivere **Orlovs- og fraværskalenderen i Teams** i funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="757ec-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="757ec-116">Du kan finde flere oplysninger om aktivering af funktioner i [Administrere funktioner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="757ec-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="757ec-117">Aktivere beskeder for appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="757ec-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="757ec-118">Hvis du ønsker, at brugere skal kunne modtage beskeder om orlov i appen Teams, skal du aktivere beskeder i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="757ec-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="757ec-119">Kun brugere, der er logget på Teams og bruger Dynamics 365 Human Resources Teams-appen, modtager beskederne.</span><span class="sxs-lookup"><span data-stu-id="757ec-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="757ec-120">I Human Resources skal du vælge **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="757ec-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="757ec-121">Vælg **Links**.</span><span class="sxs-lookup"><span data-stu-id="757ec-121">Select **Links**.</span></span>

3. <span data-ttu-id="757ec-122">Vælg **Systemparametre** under **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="757ec-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="757ec-123">Under fanen **Generelt** skal du angive **Aktivér beskeder for Teams-app** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="757ec-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivere beskeder for appen Teams i systemparametre](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="757ec-125">Hvis du vil aktivere Teams-beskeder for alle brugere, skal du vælge **Ja** ved prompten.</span><span class="sxs-lookup"><span data-stu-id="757ec-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Aktivere Teams-beskeder for alle brugere](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="757ec-127">Slå Teams-beskeder til eller fra for de enkelte brugere</span><span class="sxs-lookup"><span data-stu-id="757ec-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="757ec-128">Når du har aktiveret beskeder for Teams-appen Dynamics 365 Human Resources, kan du slå beskeder til eller fra for de enkelte brugere.</span><span class="sxs-lookup"><span data-stu-id="757ec-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="757ec-129">I Human Resources skal du vælge **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="757ec-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="757ec-130">Vælg **Links**.</span><span class="sxs-lookup"><span data-stu-id="757ec-130">Select **Links**.</span></span>

3. <span data-ttu-id="757ec-131">Vælg **Brugerindstillinger** under **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="757ec-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="757ec-132">Vælg fanen **Arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="757ec-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="757ec-133">Indstil **Aktivér beskeder for Teams-app** til **Ja** for at aktivere beskeder for brugeren eller **Nej** for at deaktivere beskeder for brugeren.</span><span class="sxs-lookup"><span data-stu-id="757ec-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Aktivér beskeder for Teams-app i Brugerindstillinger under fanen Arbejdsgang](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="757ec-135">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="757ec-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="757ec-136">Understøttede sprog</span><span class="sxs-lookup"><span data-stu-id="757ec-136">Supported languages</span></span>

<span data-ttu-id="757ec-137">Appen Dynamics 365 Human Resources i Teams understøtter følgende sprog:</span><span class="sxs-lookup"><span data-stu-id="757ec-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="757ec-138">Landestandard-id</span><span class="sxs-lookup"><span data-stu-id="757ec-138">Locale ID</span></span> | <span data-ttu-id="757ec-139">Sprog</span><span class="sxs-lookup"><span data-stu-id="757ec-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="757ec-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="757ec-140">de-DE</span></span> | <span data-ttu-id="757ec-141">Tysk (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="757ec-141">German (Germany)</span></span> |
| <span data-ttu-id="757ec-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="757ec-142">es-ES</span></span> | <span data-ttu-id="757ec-143">Spansk (Spanien)</span><span class="sxs-lookup"><span data-stu-id="757ec-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="757ec-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="757ec-144">es-MX</span></span> | <span data-ttu-id="757ec-145">Spansk (Mexico)</span><span class="sxs-lookup"><span data-stu-id="757ec-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="757ec-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="757ec-146">fr-CA</span></span> | <span data-ttu-id="757ec-147">Fransk (Canada)</span><span class="sxs-lookup"><span data-stu-id="757ec-147">French (Canada)</span></span> |
| <span data-ttu-id="757ec-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="757ec-148">fr-FR</span></span> | <span data-ttu-id="757ec-149">Fransk (Frankrig)</span><span class="sxs-lookup"><span data-stu-id="757ec-149">French (France)</span></span> |
| <span data-ttu-id="757ec-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="757ec-150">it-IT</span></span> | <span data-ttu-id="757ec-151">Italiensk (Italien)</span><span class="sxs-lookup"><span data-stu-id="757ec-151">Italian (Italy)</span></span> |
| <span data-ttu-id="757ec-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="757ec-152">nl-NL</span></span> | <span data-ttu-id="757ec-153">Hollandsk (Nederlandene)</span><span class="sxs-lookup"><span data-stu-id="757ec-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="757ec-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="757ec-154">pt-BR</span></span> | <span data-ttu-id="757ec-155">Portugisisk (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="757ec-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="757ec-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="757ec-156">tr-TR</span></span> | <span data-ttu-id="757ec-157">Tyrkisk (Tyrkiet)</span><span class="sxs-lookup"><span data-stu-id="757ec-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="757ec-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="757ec-158">zh-CN</span></span> | <span data-ttu-id="757ec-159">Kinesisk (forenklet)</span><span class="sxs-lookup"><span data-stu-id="757ec-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="757ec-160">Notater</span><span class="sxs-lookup"><span data-stu-id="757ec-160">Notes</span></span>

<span data-ttu-id="757ec-161">Følgende arbejdselementer oversættes i fremtidige versioner:</span><span class="sxs-lookup"><span data-stu-id="757ec-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="757ec-162">Workflowopgave</span><span class="sxs-lookup"><span data-stu-id="757ec-162">Work item</span></span> | <span data-ttu-id="757ec-163">Status</span><span class="sxs-lookup"><span data-stu-id="757ec-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="757ec-164">Saldoen er forkert, når der angives fri for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="757ec-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="757ec-165">Prognosefunktion er ikke tilgængelig endnu.</span><span class="sxs-lookup"><span data-stu-id="757ec-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="757ec-166">Saldoen viser den aktuelle dato.</span><span class="sxs-lookup"><span data-stu-id="757ec-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="757ec-167">Kan ikke annullere en anmodning **Til gennemsyn**.</span><span class="sxs-lookup"><span data-stu-id="757ec-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="757ec-168">Denne funktionalitet understøttes ikke i øjeblikket, og den føjes til en fremtidig version.</span><span class="sxs-lookup"><span data-stu-id="757ec-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="757ec-169">Saldooplysninger beregnes pr. dags dato.</span><span class="sxs-lookup"><span data-stu-id="757ec-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="757ec-170">Systemet viser i øjeblikket ikke saldi pr. periodiseringsperioden, også selvom det er konfigureret i orlovs- og fraværsparametre.</span><span class="sxs-lookup"><span data-stu-id="757ec-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="757ec-171">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="757ec-171">Troubleshooting</span></span>

<span data-ttu-id="757ec-172">Hvis en bruger har problemer med at logge på eller bruge appen Human Resources Teams, kan brugeren prøve at følge disse fejlfindingsinstruktioner.</span><span class="sxs-lookup"><span data-stu-id="757ec-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="757ec-173">Hvis du stadig har problemer efter fejlfinding, skal du kontakte Support.</span><span class="sxs-lookup"><span data-stu-id="757ec-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="757ec-174">Du kan finde flere oplysninger under [Få support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="757ec-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="757ec-175">Der kan ikke logge på appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="757ec-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="757ec-176">Hvis en bruger kontakter dig, fordi vedkommende ikke kan logge på appen, skal du kontrollere, at brugeren har en tilknyttet medarbejderpost i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="757ec-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="757ec-177">Der opstod en fejl under godkendelse af orlovsanmodninger i appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="757ec-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="757ec-178">Hvis en bruger modtager en fejl under forsøg på at godkende orlovsanmodninger i appen Teams, skal du afprøve følgende fejlfindingstrin:</span><span class="sxs-lookup"><span data-stu-id="757ec-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="757ec-179">Kontrollér, at deres Teams-konto er den samme, som de bruger til at få adgang til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="757ec-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="757ec-180">Kontrollér, at de er en gyldig godkender af anmodningen, ved at kontrollere indstillingerne af arbejdsproces for orlovsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="757ec-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="757ec-181">Du kan finde flere oplysninger om orlovsarbejdsprocesser i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="757ec-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

### <a name="leave-approvers-dont-receive-teams-chat-messages-to-approve-leave-requests"></a><span data-ttu-id="757ec-182">Orlovsgodkendere modtager ikke Teams-chatmeddelelser til godkendelse af orlovsanmodninger</span><span class="sxs-lookup"><span data-stu-id="757ec-182">Leave approvers don't receive Teams chat messages to approve leave requests</span></span>

1. <span data-ttu-id="757ec-183">Sørg for, at beskeder er aktiveret for miljøet og brugeren.</span><span class="sxs-lookup"><span data-stu-id="757ec-183">Ensure notifications are enabled for the environment and the user.</span></span> <span data-ttu-id="757ec-184">Du kan finde flere oplysninger i [Aktivere beskeder for Human Resources-appen i Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) og [Slå Teams-beskeder til eller fra for individuelle brugere](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span><span class="sxs-lookup"><span data-stu-id="757ec-184">For more information, see [Enable notifications for the Human Resources app in Teams](hr-admin-teams-leave-app.md#enable-notifications-for-the-human-resources-app-in-teams) and [Turn Teams notifications on or off for individual users](hr-admin-teams-leave-app.md#turn-teams-notifications-on-or-off-for-individual-users).</span></span>

2. <span data-ttu-id="757ec-185">Sørg for, at brugere er logget under fanen **Chatbeskeder** med de samme legitimationsoplysninger, som de bruger til at godkende orlovsanmodninger.</span><span class="sxs-lookup"><span data-stu-id="757ec-185">Ensure users are signed into the **Chats** tab with the same credentials they use for approving leave requests.</span></span> <span data-ttu-id="757ec-186">Brug meddelelserne for "Log af" og derefter "Log på" for at logge på med de rette legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="757ec-186">Use the messages "sign out" and then "sign in" to sign in with the correct credentials.</span></span>

3. <span data-ttu-id="757ec-187">Hvis problemet fortsætter, skal du kontrollere statussen for systembatchjobbet Forretningshændelser som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="757ec-187">If the issue persists, check the status of the Business Events system batch job as a system administrator.</span></span> <span data-ttu-id="757ec-188">Hvis det er i vente- eller udførelsesfasen, skal du tjekke ind igen om et par minutter.</span><span class="sxs-lookup"><span data-stu-id="757ec-188">If it's in a waiting or executing stage, check back in a few minutes.</span></span> <span data-ttu-id="757ec-189">Hvis statussen forbliver uændret, skal du logge en supportbillet, så vores team kan hjælpe med at løse problemet.</span><span class="sxs-lookup"><span data-stu-id="757ec-189">If the status remains unchanged, log a support ticket so our team can help resolve the issue.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="757ec-190">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="757ec-190">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="757ec-191">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="757ec-191">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="757ec-192">Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål.</span><span class="sxs-lookup"><span data-stu-id="757ec-192">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="757ec-193">Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="757ec-193">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="757ec-194">Læs mere om LUIS [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="757ec-194">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="757ec-195">LUIS-tjenesten gør formålet utvetydeligt eller forstår hensigten med brugerinputtet (i dette tilfælde er hensigten at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso).</span><span class="sxs-lookup"><span data-stu-id="757ec-195">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="757ec-196">Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="757ec-196">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span>

<span data-ttu-id="757ec-197">Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse.</span><span class="sxs-lookup"><span data-stu-id="757ec-197">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="757ec-198">LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="757ec-198">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="757ec-199">Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen.</span><span class="sxs-lookup"><span data-stu-id="757ec-199">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="757ec-200">Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="757ec-200">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="757ec-201">Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="757ec-201">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="757ec-202">Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="757ec-202">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="757ec-203">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="757ec-203">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="757ec-204">Når du bruger Dynamics 365 Human Resources-appen i Microsoft Teams, kan visse kundedata flyde uden for det geografiske område, hvor din lejers personaleservice er installeret.</span><span class="sxs-lookup"><span data-stu-id="757ec-204">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="757ec-205">Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsgangsopgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="757ec-205">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="757ec-206">Disse data kan gemmes i Microsoft Azure Event Grid i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester.</span><span class="sxs-lookup"><span data-stu-id="757ec-206">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="757ec-207">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="757ec-207">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="757ec-208">Indholdet i samtalen med chatrobotten i Human Resources-appen kan gemmes i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="757ec-208">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="757ec-209">Disse data kan gemmes i Azure Cosmos DB i op til 24 timer og kan behandles uden for det geografiske område, hvor din lejers Human Resources-tjeneste er udrullet. Data, der er undervejs, og inaktive data krypteres og bruges ikke af Microsoft eller underprocesser til træning eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="757ec-209">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="757ec-210">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="757ec-210">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="757ec-211">Hvis du vil begrænse adgangen til Human Resources-appen i Microsoft Teams for din organisation eller brugere i organisationen, skal du se [Styre apptilladelsespolitikker i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="757ec-211">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="757ec-212">Se også</span><span class="sxs-lookup"><span data-stu-id="757ec-212">See also</span></span> 

[<span data-ttu-id="757ec-213">Downloade og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="757ec-213">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="757ec-214">Microsoft Teams Hjælp-center</span><span class="sxs-lookup"><span data-stu-id="757ec-214">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="757ec-215">Administrere fraværsanmodninger i Teams</span><span class="sxs-lookup"><span data-stu-id="757ec-215">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]