---
title: Appen Personale i Teams
description: I dette emne introduceres Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 09/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
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
ms.openlocfilehash: 33322b9b553076125695f257b201463e9d8275c6
ms.sourcegitcommit: e27510ba52623c801353eed4853f8c0aeea3bb2d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/22/2020
ms.locfileid: "3828908"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="be049-103">Appen Personale i Teams</span><span class="sxs-lookup"><span data-stu-id="be049-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="be049-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan medarbejdere hurtigt anmode om at få fri og se deres flekskontooplysninger i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="be049-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="be049-105">Medarbejderne kan interagere med en bot for at anmode om oplysninger.</span><span class="sxs-lookup"><span data-stu-id="be049-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="be049-106">Fanen **Fridage** giver mere detaljerede oplysninger. Derudover kan de sende personer oplysninger om kommende fridage i Teams og chatsamtaler uden for Human Resources-app.</span><span class="sxs-lookup"><span data-stu-id="be049-106">The **Time off** tab provides more detailed information.In addition, they can send people information about upcoming time off in teams and chats outside the Human Resources app.</span></span>

![Orlov via appbot i Personale i Teams](./media/hr-admin-teams-leave-app-bot.png)

![Fanen Fri i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab.png)

![Human Resources-orlovsanmodningskort](./media/hr-teams-leave-app-chat-card.png)

## <a name="install-and-setup"></a><span data-ttu-id="be049-110">Installere og konfigurere</span><span class="sxs-lookup"><span data-stu-id="be049-110">Install and setup</span></span>

<span data-ttu-id="be049-111">Du kan finde Personale-appen i storen til Teams.</span><span class="sxs-lookup"><span data-stu-id="be049-111">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="be049-112">Få flere oplysninger om installation af appen Teams i [Styre anmodninger i Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="be049-112">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="be049-113">Få flere oplysninger om styring af app-tilladelser i Teams i [Styre app-tilladelsespolitikker i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="be049-113">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="enable-notifications-for-the-human-resources-app-in-teams"></a><span data-ttu-id="be049-114">Aktivere beskeder for appen Personale i Teams</span><span class="sxs-lookup"><span data-stu-id="be049-114">Enable notifications for the Human Resources app in Teams</span></span>

<span data-ttu-id="be049-115">Hvis du ønsker, at brugere skal kunne modtage beskeder om orlov i appen Teams, skal du aktivere beskeder i Personale.</span><span class="sxs-lookup"><span data-stu-id="be049-115">If you want users to receive leave request notifications in the Teams app, you must enable notifications in Human Resources.</span></span>

>[!NOTE]
><span data-ttu-id="be049-116">Kun brugere, der er logget på Teams og bruger Teams-appen Personale, modtager beskederne.</span><span class="sxs-lookup"><span data-stu-id="be049-116">Only users who are signed into Teams and using the Human Resources Teams app will receive notifications.</span></span>

1. <span data-ttu-id="be049-117">I Personale skal du vælge **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="be049-117">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="be049-118">Vælg **Links**.</span><span class="sxs-lookup"><span data-stu-id="be049-118">Select **Links**.</span></span>

3. <span data-ttu-id="be049-119">Vælg **Systemparametre** under **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="be049-119">Under **Setup**, select **System parameters**.</span></span>

4. <span data-ttu-id="be049-120">Under fanen **Generelt** skal du angive **Aktivér beskeder for Teams-app** til **Ja**.</span><span class="sxs-lookup"><span data-stu-id="be049-120">On the **General** tab, set **Enable notifications for Teams app** to **Yes**.</span></span>

   ![Aktivere beskeder for appen Teams i systemparametre](./media/hr-admin-teams-leave-app-enable-notifications.png)

5. <span data-ttu-id="be049-122">Hvis du vil aktivere Teams-beskeder for alle brugere, skal du vælge **Ja** ved prompten.</span><span class="sxs-lookup"><span data-stu-id="be049-122">To turn on Teams notifications for all users, select **Yes** at the prompt.</span></span>

   ![Aktivere Teams-beskeder for alle brugere](./media/hr-admin-teams-leave-app-notifications-all-users.png)

### <a name="turn-teams-notifications-on-or-off-for-individual-users"></a><span data-ttu-id="be049-124">Slå Teams-beskeder til eller fra for de enkelte brugere</span><span class="sxs-lookup"><span data-stu-id="be049-124">Turn Teams notifications on or off for individual users</span></span>

<span data-ttu-id="be049-125">Når du har aktiveret beskeder for Teams-appen Personale, kan du slå beskeder til eller fra for de enkelte brugere.</span><span class="sxs-lookup"><span data-stu-id="be049-125">After you've enabled notifications for the Human Resources Teams app, you can turn notifications on or off for individual users.</span></span>

1. <span data-ttu-id="be049-126">I Personale skal du vælge **Systemadministration**.</span><span class="sxs-lookup"><span data-stu-id="be049-126">In Human Resources, select **System administration**.</span></span>

2. <span data-ttu-id="be049-127">Vælg **Links**.</span><span class="sxs-lookup"><span data-stu-id="be049-127">Select **Links**.</span></span>

3. <span data-ttu-id="be049-128">Vælg **Brugerindstillinger** under **Brugere**.</span><span class="sxs-lookup"><span data-stu-id="be049-128">Under **Users**, select **User options**.</span></span>

4. <span data-ttu-id="be049-129">Vælg fanen **Arbejdsgang**.</span><span class="sxs-lookup"><span data-stu-id="be049-129">Select the **Workflow** tab.</span></span>

5. <span data-ttu-id="be049-130">Indstil **Aktivér beskeder for Teams-app** til **Ja** for at aktivere beskeder for brugeren eller **Nej** for at deaktivere beskeder for brugeren.</span><span class="sxs-lookup"><span data-stu-id="be049-130">Set **Enable notifications for Teams app** to **Yes** to enable notifications for the user or **No** to disable notifications for the user.</span></span>

   ![Aktivér beskeder for Teams-app i Brugerindstillinger under fanen Arbejdsgang](./media/hr-admin-teams-leave-app-notifications.png)

6. <span data-ttu-id="be049-132">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="be049-132">Select **Save**.</span></span>

## <a name="known-issues"></a><span data-ttu-id="be049-133">Kendte problemer</span><span class="sxs-lookup"><span data-stu-id="be049-133">Known issues</span></span>

| <span data-ttu-id="be049-134">Udsted</span><span class="sxs-lookup"><span data-stu-id="be049-134">Issue</span></span> | <span data-ttu-id="be049-135">Status</span><span class="sxs-lookup"><span data-stu-id="be049-135">Status</span></span> |
| --- | --- |
| <span data-ttu-id="be049-136">Vandret rulning fungerer ikke på Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="be049-136">Horizontal scrolling doesn't work on Android phones</span></span> | <span data-ttu-id="be049-137">Vandret rulning er ikke et problem på iOS-enheder eller stationære computere.</span><span class="sxs-lookup"><span data-stu-id="be049-137">Horizontal scrolling isn't an issue on iOS or desktop devices.</span></span> <span data-ttu-id="be049-138">Vi arbejder på at løse problemet for Android.</span><span class="sxs-lookup"><span data-stu-id="be049-138">We're working on a fix for Android.</span></span> |
| <span data-ttu-id="be049-139">Saldoen er forkert, når der angives fri for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="be049-139">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="be049-140">Prognosefunktion er ikke tilgængelig endnu.</span><span class="sxs-lookup"><span data-stu-id="be049-140">Forecasting isn't yet available.</span></span> <span data-ttu-id="be049-141">Saldoen viser den aktuelle dato.</span><span class="sxs-lookup"><span data-stu-id="be049-141">The balance displays for the current date.</span></span> |
| <span data-ttu-id="be049-142">Kan ikke annullere en anmodning **Til gennemsyn**.</span><span class="sxs-lookup"><span data-stu-id="be049-142">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="be049-143">Denne funktionalitet understøttes ikke i øjeblikket, og den føjes til en fremtidig version.</span><span class="sxs-lookup"><span data-stu-id="be049-143">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="be049-144">Saldooplysninger beregnes pr. dags dato.</span><span class="sxs-lookup"><span data-stu-id="be049-144">Balance information is calculated as of today.</span></span> | <span data-ttu-id="be049-145">Systemet viser i øjeblikket ikke saldi pr. periodiseringsperioden, også selvom det er konfigureret i orlovs- og fraværsparametre.</span><span class="sxs-lookup"><span data-stu-id="be049-145">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="be049-146">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="be049-146">Privacy notice</span></span>

### <a name="microsoft-language-understanding-intelligent-service-luis"></a><span data-ttu-id="be049-147">Microsoft Language Understanding Intelligent Service (LUIS)</span><span class="sxs-lookup"><span data-stu-id="be049-147">Microsoft Language Understanding Intelligent Service (LUIS)</span></span>

<span data-ttu-id="be049-148">Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål.</span><span class="sxs-lookup"><span data-stu-id="be049-148">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="be049-149">Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service).</span><span class="sxs-lookup"><span data-stu-id="be049-149">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="be049-150">Læs mere om LUIS [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="be049-150">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="be049-151">LUIS-tjenesten gør formålet utvetydeligt eller forstår formålet med brugerinputtet (i dette tilfælde er formålet at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso).</span><span class="sxs-lookup"><span data-stu-id="be049-151">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="be049-152">Disse oplysninger sendes derefter til Microsofts  [Azure Bot Framework](https://azure.microsoft.com/services/bot-service/), som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="be049-152">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/), which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="be049-153">Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse.</span><span class="sxs-lookup"><span data-stu-id="be049-153">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="be049-154">LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="be049-154">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="be049-155">Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen.</span><span class="sxs-lookup"><span data-stu-id="be049-155">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="be049-156">Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="be049-156">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="be049-157">Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="be049-157">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="be049-158">Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="be049-158">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span>

### <a name="microsoft-teams-azure-event-grid-and-azure-cosmos-db"></a><span data-ttu-id="be049-159">Microsoft Teams, Azure Event Grid og Azure Cosmos DB</span><span class="sxs-lookup"><span data-stu-id="be049-159">Microsoft Teams, Azure Event Grid, and Azure Cosmos DB</span></span>

<span data-ttu-id="be049-160">Når du bruger Dynamics 365 Human Resources-appen i Microsoft Teams, kan visse kundedata flyde uden for det geografiske område, hvor din lejers personaleservice er installeret.</span><span class="sxs-lookup"><span data-stu-id="be049-160">When using the Dynamics 365 Human Resources app in Microsoft Teams, certain customer data may flow outside of the geographic region where your tenant’s Human Resources service is deployed.</span></span>

<span data-ttu-id="be049-161">Dynamics 365 Human Resources overfører oplysninger om medarbejderens orlovsanmodning og arbejdsgangsopgave til Microsoft Azure Event Grid og Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="be049-161">Dynamics 365 Human Resources transmits the employee’s leave request and workflow task details to Microsoft Azure Event Grid and Microsoft Teams.</span></span> <span data-ttu-id="be049-162">Disse data kan gemmes i Microsoft Azure Event Grid i op til 24 timer og behandles i USA, krypteres under overførslen og i lageret og bruges ikke af Microsoft eller underprocesser til træning eller forbedring af tjenester.</span><span class="sxs-lookup"><span data-stu-id="be049-162">This data may be stored in Microsoft Azure Event Grid for up to 24 hours and will be processed in the United States, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="be049-163">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="be049-163">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>

<span data-ttu-id="be049-164">Indholdet i samtalen med chatrobotten i Human Resources-appen kan gemmes i Azure Cosmos DB og overføres til Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="be049-164">While conversing with the chat bot in the Human Resources app, the conversation content may be stored in Azure Cosmos DB and transmitted to Microsoft Teams.</span></span> <span data-ttu-id="be049-165">Disse data kan gemmes i Azure Cosmos DB i op til 24 timer og kan behandles uden for det geografiske område, hvor din lejers Human Resources-tjeneste er udrullet. Data, der er undervejs, og inaktive data krypteres og bruges ikke af Microsoft eller underprocesser til træning eller tjenesteforbedringer.</span><span class="sxs-lookup"><span data-stu-id="be049-165">This data may be stored in Azure Cosmos DB for up to 24 hours and may be processed outside of the geographic region where your tenant's Human Resources service is deployed, is encrypted in transit and at rest, and is not used by Microsoft or its subprocessors for training or service improvements.</span></span> <span data-ttu-id="be049-166">Få indsigt i, hvor dine data opbevares i Teams, ved at se: [Placering af data i Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span><span class="sxs-lookup"><span data-stu-id="be049-166">To understand where your data is stored in Teams, please see: [Location of data in Microsoft Teams](https://docs.microsoft.com/microsoftteams/location-of-data-in-teams?view=o365-worldwide&preserve-view=true).</span></span>
 
<span data-ttu-id="be049-167">Hvis du vil begrænse adgangen til Human Resources-appen i Microsoft Teams for din organisation eller brugere i organisationen, skal du se [Styre apptilladelsespolitikker i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="be049-167">To restrict access to the Human Resources app in Microsoft Teams for your organization or users within your organization, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="see-also"></a><span data-ttu-id="be049-168">Se også</span><span class="sxs-lookup"><span data-stu-id="be049-168">See also</span></span> 

[<span data-ttu-id="be049-169">Downloade og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="be049-169">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="be049-170">Microsoft Teams Hjælp-center</span><span class="sxs-lookup"><span data-stu-id="be049-170">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="be049-171">Administrere fraværsanmodninger i Teams</span><span class="sxs-lookup"><span data-stu-id="be049-171">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

