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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3926acd07a68f59682c18f4f7bc290dc1e21d0b6
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/13/2021
ms.locfileid: "5889734"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="73ffa-103">Appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="73ffa-103">Human Resources app in Teams</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="73ffa-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan medarbejdere hurtigt anmode om at få fri og se deres flekskontooplysninger i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="73ffa-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="73ffa-105">Medarbejderne kan interagere med en bot for at anmode om oplysninger.</span><span class="sxs-lookup"><span data-stu-id="73ffa-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="73ffa-106">Fanen **Fridage** giver mere detaljerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="73ffa-106">The **Time off** tab provides more detailed information.</span></span> <span data-ttu-id="73ffa-107">De kan også sende oplysninger om kommende fridage i teams og chatte uden for Human Resource-appen.</span><span class="sxs-lookup"><span data-stu-id="73ffa-107">In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Orlov via appbot i Human Resources i Teams](./media/hr-teams-leave-app-bot.png)

![Fanen Fri i orlovsappen i Human Resources i Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="73ffa-111">Installere og konfigurere</span><span class="sxs-lookup"><span data-stu-id="73ffa-111">Install and setup</span></span>

<span data-ttu-id="73ffa-112">Du kan finde appen Dynamics 365 Human Resources i lageret til Teams.</span><span class="sxs-lookup"><span data-stu-id="73ffa-112">You can find the Dynamics 365 Human Resources app in the Teams store.</span></span> <span data-ttu-id="73ffa-113">Få flere oplysninger om installation af appen Teams i [Styre anmodninger i Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="73ffa-113">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="73ffa-114">Få flere oplysninger om styring af app-tilladelser i Teams i [Styre app-tilladelsespolitikker i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="73ffa-114">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

<span data-ttu-id="73ffa-115">Hvis brugerne skal have vist orlovs- og fraværskalenderen i appen, skal du aktivere **Orlovs- og fraværskalenderen i Teams** i funktionsstyring.</span><span class="sxs-lookup"><span data-stu-id="73ffa-115">If you want your users to view the Leave and absence calendar in the app, you'll need to enable the **Leave and absence calendar in Teams** in Feature management.</span></span> <span data-ttu-id="73ffa-116">Du kan finde flere oplysninger om aktivering af funktioner i [Administrere funktioner](hr-admin-manage-features.md).</span><span class="sxs-lookup"><span data-stu-id="73ffa-116">For more information about enabling features, see [Manage features](hr-admin-manage-features.md).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="73ffa-117">Aktivere beskeder for appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="73ffa-117">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="73ffa-118">Hvis du ønsker, at brugere skal kunne modtage beskeder om orlov i appen Teams, skal du aktivere beskeder i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="73ffa-118">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Dynamics 365 Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="73ffa-119">Kun brugere, der er logget på Teams og bruger Dynamics 365 Human Resources Teams-appen, modtager beskederne.</span><span class="sxs-lookup"><span data-stu-id="73ffa-119">Only users who are signed into Teams and using the Dynamics 365 Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="73ffa-120">I Human Resources skal du vælge **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-120">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="73ffa-121">Vælg **Links**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-121">Select **Links**.</span></span>

3. <span data-ttu-id="73ffa-122">Vælg **Systemparametre** under **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-122">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="73ffa-123">Under fanen **Generelt** skal du angive **Aktivér beskeder for Teams-app** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-123">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivere beskeder for appen Teams i systemparametre](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="73ffa-125">Hvis du vil aktivere Teams-beskeder for alle brugere, skal du vælge **Ja** ved prompten.</span><span class="sxs-lookup"><span data-stu-id="73ffa-125">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Aktivere Teams-beskeder for alle brugere](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="73ffa-127">Slå Teams-beskeder til eller fra for de enkelte brugere</span><span class="sxs-lookup"><span data-stu-id="73ffa-127">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="73ffa-128">Når du har aktiveret beskeder for Teams-appen Dynamics 365 Human Resources, kan du slå beskeder til eller fra for de enkelte brugere.</span><span class="sxs-lookup"><span data-stu-id="73ffa-128">After you've enabled notifications for the Dynamics 365 Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="73ffa-129">I Human Resources skal du vælge **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-129">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="73ffa-130">Vælg **Links**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-130">Select **Links**.</span></span>

3. <span data-ttu-id="73ffa-131">Vælg **Brugerindstillinger** under **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-131">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="73ffa-132">Vælg fanen **Arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-132">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="73ffa-133">Indstil **Aktivér beskeder for Teams-app** til **Ja** for at aktivere beskeder for brugeren eller **Nej** for at deaktivere beskeder for brugeren.</span><span class="sxs-lookup"><span data-stu-id="73ffa-133">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Aktivér beskeder for Teams-app i Brugerindstillinger under fanen Arbejdsgang](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="73ffa-135">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-135">Select **Save**.</span></span>

## <a name="supported-languages"></a><span data-ttu-id="73ffa-136">Understøttede sprog</span><span class="sxs-lookup"><span data-stu-id="73ffa-136">Supported languages</span></span>

<span data-ttu-id="73ffa-137">Appen Dynamics 365 Human Resources i Teams understøtter følgende sprog:</span><span class="sxs-lookup"><span data-stu-id="73ffa-137">The Dynamics 365 Human Resources app in Teams supports the following languages:</span></span>

| <span data-ttu-id="73ffa-138">Landestandard-id</span><span class="sxs-lookup"><span data-stu-id="73ffa-138">Locale ID</span></span> | <span data-ttu-id="73ffa-139">Sprog</span><span class="sxs-lookup"><span data-stu-id="73ffa-139">Language</span></span> |
| --- | --- |
| <span data-ttu-id="73ffa-140">de-DE</span><span class="sxs-lookup"><span data-stu-id="73ffa-140">de-DE</span></span> | <span data-ttu-id="73ffa-141">Tysk (Tyskland)</span><span class="sxs-lookup"><span data-stu-id="73ffa-141">German (Germany)</span></span> |
| <span data-ttu-id="73ffa-142">es-ES</span><span class="sxs-lookup"><span data-stu-id="73ffa-142">es-ES</span></span> | <span data-ttu-id="73ffa-143">Spansk (Spanien)</span><span class="sxs-lookup"><span data-stu-id="73ffa-143">Spanish (Spain)</span></span> |
| <span data-ttu-id="73ffa-144">es-MX</span><span class="sxs-lookup"><span data-stu-id="73ffa-144">es-MX</span></span> | <span data-ttu-id="73ffa-145">Spansk (Mexico)</span><span class="sxs-lookup"><span data-stu-id="73ffa-145">Spanish (Mexico)</span></span> |
| <span data-ttu-id="73ffa-146">fr-CA</span><span class="sxs-lookup"><span data-stu-id="73ffa-146">fr-CA</span></span> | <span data-ttu-id="73ffa-147">Fransk (Canada)</span><span class="sxs-lookup"><span data-stu-id="73ffa-147">French (Canada)</span></span> |
| <span data-ttu-id="73ffa-148">fr-FR</span><span class="sxs-lookup"><span data-stu-id="73ffa-148">fr-FR</span></span> | <span data-ttu-id="73ffa-149">Fransk (Frankrig)</span><span class="sxs-lookup"><span data-stu-id="73ffa-149">French (France)</span></span> |
| <span data-ttu-id="73ffa-150">it-IT</span><span class="sxs-lookup"><span data-stu-id="73ffa-150">it-IT</span></span> | <span data-ttu-id="73ffa-151">Italiensk (Italien)</span><span class="sxs-lookup"><span data-stu-id="73ffa-151">Italian (Italy)</span></span> |
| <span data-ttu-id="73ffa-152">nl-NL</span><span class="sxs-lookup"><span data-stu-id="73ffa-152">nl-NL</span></span> | <span data-ttu-id="73ffa-153">Hollandsk (Nederlandene)</span><span class="sxs-lookup"><span data-stu-id="73ffa-153">Dutch (Netherlands)</span></span> |
| <span data-ttu-id="73ffa-154">pt-BR</span><span class="sxs-lookup"><span data-stu-id="73ffa-154">pt-BR</span></span> | <span data-ttu-id="73ffa-155">Portugisisk (Brasilien)</span><span class="sxs-lookup"><span data-stu-id="73ffa-155">Portuguese (Brazil)</span></span> |
| <span data-ttu-id="73ffa-156">tr-TR</span><span class="sxs-lookup"><span data-stu-id="73ffa-156">tr-TR</span></span> | <span data-ttu-id="73ffa-157">Tyrkisk (Tyrkiet)</span><span class="sxs-lookup"><span data-stu-id="73ffa-157">Turkish (Turkey)</span></span> |
| <span data-ttu-id="73ffa-158">zh-CN</span><span class="sxs-lookup"><span data-stu-id="73ffa-158">zh-CN</span></span> | <span data-ttu-id="73ffa-159">Kinesisk (forenklet)</span><span class="sxs-lookup"><span data-stu-id="73ffa-159">Chinese (Simplified)</span></span> |

## <a name="notes"></a><span data-ttu-id="73ffa-160">Notater</span><span class="sxs-lookup"><span data-stu-id="73ffa-160">Notes</span></span>

<span data-ttu-id="73ffa-161">Følgende arbejdselementer oversættes i fremtidige versioner:</span><span class="sxs-lookup"><span data-stu-id="73ffa-161">The following work items are slated for future releases:</span></span>

| <span data-ttu-id="73ffa-162">Workflowopgave</span><span class="sxs-lookup"><span data-stu-id="73ffa-162">Work item</span></span> | <span data-ttu-id="73ffa-163">Status</span><span class="sxs-lookup"><span data-stu-id="73ffa-163">Status</span></span> |
| --- | --- |
| <span data-ttu-id="73ffa-164">Saldoen er forkert, når der angives fri for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="73ffa-164">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="73ffa-165">Prognosefunktion er ikke tilgængelig endnu.</span><span class="sxs-lookup"><span data-stu-id="73ffa-165">Forecasting isn't yet available.</span></span> <span data-ttu-id="73ffa-166">Saldoen viser den aktuelle dato.</span><span class="sxs-lookup"><span data-stu-id="73ffa-166">The balance displays for the current date.</span></span> |
| <span data-ttu-id="73ffa-167">Kan ikke annullere en anmodning **Til gennemsyn**.</span><span class="sxs-lookup"><span data-stu-id="73ffa-167">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="73ffa-168">Denne funktionalitet understøttes ikke i øjeblikket, og den føjes til en fremtidig version.</span><span class="sxs-lookup"><span data-stu-id="73ffa-168">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="73ffa-169">Saldooplysninger beregnes pr. dags dato.</span><span class="sxs-lookup"><span data-stu-id="73ffa-169">Balance information is calculated as of today.</span></span> | <span data-ttu-id="73ffa-170">Systemet viser i øjeblikket ikke saldi pr. periodiseringsperioden, også selvom det er konfigureret i orlovs- og fraværsparametre.</span><span class="sxs-lookup"><span data-stu-id="73ffa-170">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="troubleshooting"></a><span data-ttu-id="73ffa-171">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="73ffa-171">Troubleshooting</span></span>

<span data-ttu-id="73ffa-172">Hvis en bruger har problemer med at logge på eller bruge appen Human Resources Teams, kan brugeren prøve at følge disse fejlfindingsinstruktioner.</span><span class="sxs-lookup"><span data-stu-id="73ffa-172">If a user is having trouble signing into or using the Human Resources Teams app, try following these troubleshooting instructions.</span></span> <span data-ttu-id="73ffa-173">Hvis du stadig har problemer efter fejlfinding, skal du kontakte Support.</span><span class="sxs-lookup"><span data-stu-id="73ffa-173">If you're still having problems after troubleshooting, contact Support.</span></span> <span data-ttu-id="73ffa-174">Du kan finde flere oplysninger under [Få support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span><span class="sxs-lookup"><span data-stu-id="73ffa-174">For more information, see [Get support](../fin-ops-core/dev-itpro/lifecycle-services/lcs-support.md).</span></span>

### <a name="cant-sign-into-the-human-resources-app-in-teams"></a><span data-ttu-id="73ffa-175">Der kan ikke logge på appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="73ffa-175">Can't sign into the Human Resources app in Teams</span></span>

<span data-ttu-id="73ffa-176">Hvis en bruger kontakter dig, fordi vedkommende ikke kan logge på appen, skal du kontrollere, at brugeren har en tilknyttet medarbejderpost i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="73ffa-176">If a user contacts you because they can't sign into the app, verify that they have an associated employee record in Human Resources.</span></span>

### <a name="error-when-approving-leave-requests-in-the-human-resources-app-in-teams"></a><span data-ttu-id="73ffa-177">Der opstod en fejl under godkendelse af orlovsanmodninger i appen Human Resources i Teams</span><span class="sxs-lookup"><span data-stu-id="73ffa-177">Error when approving leave requests in the Human Resources app in Teams</span></span>

<span data-ttu-id="73ffa-178">Hvis en bruger modtager en fejl under forsøg på at godkende orlovsanmodninger i appen Teams, skal du afprøve følgende fejlfindingstrin:</span><span class="sxs-lookup"><span data-stu-id="73ffa-178">If a user receives an error while trying to approve,  leave requests in the Teams app, try the following troubleshooting steps:</span></span>

1. <span data-ttu-id="73ffa-179">Kontrollér, at deres Teams-konto er den samme, som de bruger til at få adgang til Human Resources.</span><span class="sxs-lookup"><span data-stu-id="73ffa-179">Verify that their Teams account is the same one they use for accessing Human Resources.</span></span>

2. <span data-ttu-id="73ffa-180">Kontrollér, at de er en gyldig godkender af anmodningen, ved at kontrollere indstillingerne af arbejdsproces for orlovsgodkendelse.</span><span class="sxs-lookup"><span data-stu-id="73ffa-180">Verify that they're a valid approver for the request by checking the workflow settings for leave approval.</span></span> <span data-ttu-id="73ffa-181">Du kan finde flere oplysninger om orlovsarbejdsprocesser i [Oprette en arbejdsgang for orlovsanmodning](hr-leave-and-absence-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="73ffa-181">For more information about leave request workflows, see [Create a leave request workflow](hr-leave-and-absence-workflow.md).</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="73ffa-182">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="73ffa-182">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="73ffa-183">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="73ffa-183">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="73ffa-184">Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål.</span><span class="sxs-lookup"><span data-stu-id="73ffa-184">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="73ffa-185">Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="73ffa-185">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="73ffa-186">Læs mere om LUIS [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="73ffa-186">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="73ffa-187">LUIS-tjenesten gør formålet utvetydeligt eller forstår hensigten med brugerinputtet (i dette tilfælde er hensigten at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso).</span><span class="sxs-lookup"><span data-stu-id="73ffa-187">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="73ffa-188">Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="73ffa-188">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="73ffa-189">Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse.</span><span class="sxs-lookup"><span data-stu-id="73ffa-189">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="73ffa-190">LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="73ffa-190">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="73ffa-191">Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen.</span><span class="sxs-lookup"><span data-stu-id="73ffa-191">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="73ffa-192">Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="73ffa-192">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="73ffa-193">Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="73ffa-193">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="73ffa-194">Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="73ffa-194">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="73ffa-195">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="73ffa-195">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="73ffa-196">Når du bruger Dynamics 365 Human Resources-appen i Microsoft Teams, kan visse kundedata flyde uden for det geografiske område, hvor din lejers personaleservice er installeret.</span><span class="sxs-lookup"><span data-stu-id="73ffa-196">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="73ffa-197">Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsgangsopgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="73ffa-197">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="73ffa-198">Disse data kan gemmes i Microsoft Azure Event Grid i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester.</span><span class="sxs-lookup"><span data-stu-id="73ffa-198">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="73ffa-199">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="73ffa-199">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>

<span data-ttu-id="73ffa-200">Indholdet i samtalen med chatrobotten i Human Resources-appen kan gemmes i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="73ffa-200">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="73ffa-201">Disse data kan gemmes i Azure Cosmos DB i op til 24 timer og kan behandles uden for det geografiske område, hvor din lejers Human Resources-tjeneste er udrullet. Data, der er undervejs, og inaktive data krypteres og bruges ikke af Microsoft eller underprocesser til træning eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="73ffa-201">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="73ffa-202">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span><span class="sxs-lookup"><span data-stu-id="73ffa-202">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](/microsoftteams/location-of-data-in-teams?preserve-view=true&view=o365-worldwide).</span></span>
 
<span data-ttu-id="73ffa-203">Hvis du vil begrænse adgangen til Human Resources-appen i Microsoft Teams for din organisation eller brugere i organisationen, skal du se [Styre apptilladelsespolitikker i Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="73ffa-203">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="73ffa-204">Se også</span><span class="sxs-lookup"><span data-stu-id="73ffa-204">See also</span></span> 

[<span data-ttu-id="73ffa-205">Downloade og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="73ffa-205">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="73ffa-206">Microsoft Teams Hjælp-center</span><span class="sxs-lookup"><span data-stu-id="73ffa-206">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="73ffa-207">Administrere fraværsanmodninger i Teams</span><span class="sxs-lookup"><span data-stu-id="73ffa-207">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]