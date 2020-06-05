---
title: Appen Personale i Teams
description: I dette emne introduceres Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams.
author: andreabichsel
manager: AnnBe
ms.date: 05/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-05-18
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 423ec36a73e8af9d915c5cfe16bd4d552448e2b6
ms.sourcegitcommit: d1541831d556b722a71aed442043ffb4a4576d87
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/20/2020
ms.locfileid: "3388110"
---
# <a name="human-resources-app-in-teams"></a><span data-ttu-id="8fd54-103">Appen Personale i Teams</span><span class="sxs-lookup"><span data-stu-id="8fd54-103">Human Resources app in Teams</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="8fd54-104">Med Microsoft Dynamics 365 Human Resources-appen i Microsoft Teams kan medarbejdere hurtigt anmode om at få fri og se deres flekskontooplysninger i Microsoft Teams.</span><span class="sxs-lookup"><span data-stu-id="8fd54-104">The Microsoft Dynamics 365 Human Resources app in Microsoft Teams lets employees quickly request time off and view their time-off balance information in Microsoft Teams.</span></span> <span data-ttu-id="8fd54-105">Medarbejderne kan interagere med en bot for at anmode om oplysninger.</span><span class="sxs-lookup"><span data-stu-id="8fd54-105">Employees can interact with a bot to request information.</span></span> <span data-ttu-id="8fd54-106">Fanen **Fridage** giver mere detaljerede oplysninger.</span><span class="sxs-lookup"><span data-stu-id="8fd54-106">The **Time off** tab provides more detailed information.</span></span>

![Orlov via appbot i Personale i Teams](./media/hr-admin-teams-leave-app-bot.png)

![Fanen Fri i orlovsappen i Personale i Teams](./media/hr-teams-leave-app-timeoff-tab.png)

## <a name="install-and-setup"></a><span data-ttu-id="8fd54-109">Installere og konfigurere</span><span class="sxs-lookup"><span data-stu-id="8fd54-109">Install and setup</span></span>

<span data-ttu-id="8fd54-110">Du kan finde Personale-appen i storen til Teams.</span><span class="sxs-lookup"><span data-stu-id="8fd54-110">You can find the Human Resources app in the Teams store.</span></span> <span data-ttu-id="8fd54-111">Få flere oplysninger om installation af appen Teams i [Styre anmodninger i Teams](hr-teams-leave-app.md).</span><span class="sxs-lookup"><span data-stu-id="8fd54-111">For information about installing the Teams app, see [Manage leave requests in Teams](hr-teams-leave-app.md).</span></span>

<span data-ttu-id="8fd54-112">Få flere oplysninger om styring af app-tilladelser i Teams i [Styre app-tilladelsespolitikker i Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span><span class="sxs-lookup"><span data-stu-id="8fd54-112">For information about managing app permissions in Teams, see [Manage app permission policies in Microsoft Teams](https://docs.microsoft.com/MicrosoftTeams/teams-app-permission-policies).</span></span>

## <a name="known-issues"></a><span data-ttu-id="8fd54-113">Kendte problemer</span><span class="sxs-lookup"><span data-stu-id="8fd54-113">Known issues</span></span>

| <span data-ttu-id="8fd54-114">Udsted</span><span class="sxs-lookup"><span data-stu-id="8fd54-114">Issue</span></span> | <span data-ttu-id="8fd54-115">Status</span><span class="sxs-lookup"><span data-stu-id="8fd54-115">Status</span></span> |
| --- | --- |
| <span data-ttu-id="8fd54-116">Saldoen er forkert, når der angives fri for en fremtidig dato.</span><span class="sxs-lookup"><span data-stu-id="8fd54-116">The balance is incorrect when submitting time off for a future date.</span></span> | <span data-ttu-id="8fd54-117">Prognosefunktion er ikke tilgængelig endnu.</span><span class="sxs-lookup"><span data-stu-id="8fd54-117">Forecasting isn't yet available.</span></span> <span data-ttu-id="8fd54-118">Saldoen viser den aktuelle dato.</span><span class="sxs-lookup"><span data-stu-id="8fd54-118">The balance displays for the current date.</span></span> |
| <span data-ttu-id="8fd54-119">Når du reducerer antallet af timer, der er taget i en eksisterende anmodning, går **Den resterende saldo** ned i stedet for.</span><span class="sxs-lookup"><span data-stu-id="8fd54-119">When reducing the number of hours taken in an existing request, the **Remaining balance** goes down instead of up.</span></span> | <span data-ttu-id="8fd54-120">Vi løser dette kendte problem på et senere tidspunkt.</span><span class="sxs-lookup"><span data-stu-id="8fd54-120">We'll address this known issue in the future.</span></span> <span data-ttu-id="8fd54-121">Visningen er ikke korrekt, men de korrekte beløb reguleres ved afsendelsen.</span><span class="sxs-lookup"><span data-stu-id="8fd54-121">The display is incorrect, but the correct amounts are adjusted upon submission.</span></span> |
| <span data-ttu-id="8fd54-122">To kort for **Kommende fridage** vises for de samme datoer.</span><span class="sxs-lookup"><span data-stu-id="8fd54-122">Two **Upcoming time off** cards display for the same dates.</span></span> | <span data-ttu-id="8fd54-123">Kortene repræsenterer de enkelte indsendelser.</span><span class="sxs-lookup"><span data-stu-id="8fd54-123">The cards represent individual submissions.</span></span> <span data-ttu-id="8fd54-124">Vi fortsætter med at få feedback og foretage justeringer.</span><span class="sxs-lookup"><span data-stu-id="8fd54-124">We'll continue to take feedback and make adjustments.</span></span> |
| <span data-ttu-id="8fd54-125">Kan ikke annullere en anmodning **Til gennemsyn**.</span><span class="sxs-lookup"><span data-stu-id="8fd54-125">Unable to cancel an **In review** request.</span></span> | <span data-ttu-id="8fd54-126">Denne funktionalitet understøttes ikke i øjeblikket, og den føjes til en fremtidig version.</span><span class="sxs-lookup"><span data-stu-id="8fd54-126">This functionality isn't currently supported and will be added in a future release.</span></span> |
| <span data-ttu-id="8fd54-127">Saldooplysninger beregnes pr. dags dato.</span><span class="sxs-lookup"><span data-stu-id="8fd54-127">Balance information is calculated as of today.</span></span> | <span data-ttu-id="8fd54-128">Systemet viser i øjeblikket ikke saldi pr. periodiseringsperioden, også selvom det er konfigureret i orlovs- og fraværsparametre.</span><span class="sxs-lookup"><span data-stu-id="8fd54-128">The system currently doesn't display balances as of the accrual period, even if it's configured in Leave and absence parameters.</span></span> |

## <a name="privacy-notice"></a><span data-ttu-id="8fd54-129">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="8fd54-129">Privacy notice</span></span>

<span data-ttu-id="8fd54-130">Med Dynamics 365 Human Resources-botten i Microsoft Teams analyseres brugerens tekstinput for at forstå den underliggende forespørgsel/det pågældende formål.</span><span class="sxs-lookup"><span data-stu-id="8fd54-130">With the Dynamics 365 Human Resources bot in Microsoft Teams, the user’s text inputs are analyzed for understanding the underlying query/intent.</span></span> <span data-ttu-id="8fd54-131">Brugerens input, f.eks. "Søg efter konto Contoso", sendes til en af Microsofts Cognitive Services kaldet LUIS (Language Understanding Intelligent Service.</span><span class="sxs-lookup"><span data-stu-id="8fd54-131">The user’s input such as “Search account Contoso” is routed to one of Microsoft’s Cognitive Service called Language Understanding Intelligent Service (LUIS).</span></span> <span data-ttu-id="8fd54-132">Læs mere om LUIS [her](https://www.luis.ai/).</span><span class="sxs-lookup"><span data-stu-id="8fd54-132">Read more about LUIS [here](https://www.luis.ai/).</span></span> <span data-ttu-id="8fd54-133">LUIS-tjenesten gør formålet utvetydeligt eller forstår formålet med brugerinputtet (i dette tilfælde er formålet at finde oplysninger) og destinationsenheden (i dette tilfælde er den ønskede enhed en konto med navnet Contoso).</span><span class="sxs-lookup"><span data-stu-id="8fd54-133">The LUIS service disambiguates or understands the intent of user input (in this case, the intent is to find information) and the target entity (in this case, the intended entity is an account named Contoso).</span></span> <span data-ttu-id="8fd54-134">Disse oplysninger sendes derefter til Microsofts [Azure-botstruktur](https://azure.microsoft.com/services/bot-service/) , som interagerer med data fra Dynamics 365 Human Resources og henter de ønskede oplysninger til brugerforespørgslen.</span><span class="sxs-lookup"><span data-stu-id="8fd54-134">This information is then passed on to Microsoft’s [Azure bot framework](https://azure.microsoft.com/services/bot-service/) which interacts with data from Dynamics 365 Human Resources and retrieves the desired information for the user query.</span></span> 

<span data-ttu-id="8fd54-135">Hvis du installerer og giver adgang til brugen af botten, accepterer du, at LUIS-tjenesten og Azure-botstrukturen kan behandle formålet bag inputtet, hvilket giver en forbedret brugeroplevelse.</span><span class="sxs-lookup"><span data-stu-id="8fd54-135">By installing and allowing access to use of the bot, you agree to allow the LUIS service and Azure bot framework to process the intent behind the input,  which results in an enhanced conversational user experience.</span></span> <span data-ttu-id="8fd54-136">LUIS-tjenesten og Azure-botstrukturen kan have forskellige overensstemmelsesniveauer sammenlignet med Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8fd54-136">The LUIS service and Azure bot framework may have varying levels of compliance compared to Dynamics 365 Human Resources.</span></span> <span data-ttu-id="8fd54-137">Mens LUIS-tjenesten kun har adgang til brugerforespørgslerne og ikke er beregnet til at blive forbundet med brugerens Dynamics 365 Human Resources-data eller -konto, kan en bruger af Dynamics 365 Human Resources-bot frivilligt angive en forespørgsel, der indeholder kundedata, personlige oplysninger eller andre data, og sådan forespørgselsindhold kan sendes til Luis-tjenesten og Azure-botstrukturen.</span><span class="sxs-lookup"><span data-stu-id="8fd54-137">While the LUIS service has access to only the user queries and is not designed to be connected to the user’s Dynamics 365 Human Resources data or account, a user of the Dynamics 365 Human Resources bot could voluntarily enter a query containing Customer Data, Personal Data, or other data and such query content could get sent to the LUIS service and the Azure bot framework.</span></span> 

<span data-ttu-id="8fd54-138">Indholdet af brugerforespørgsler og-meddelelser bevares i LUIS-systemet i maksimalt 30 dage, er krypteret i resten og bruges ikke til oplæring eller forbedring af tjenesten.</span><span class="sxs-lookup"><span data-stu-id="8fd54-138">The content of user’s queries and messages is retained in LUIS system for a maximum of 30 days, is encrypted at rest, and is not used for training or service improvement.</span></span> <span data-ttu-id="8fd54-139">Læs mere om Cognitive Services [her](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span><span class="sxs-lookup"><span data-stu-id="8fd54-139">Read more about Cognitive Services [here](https://azure.microsoft.com/services/cognitive-services/language-understanding-intelligent-service/).</span></span> 

<span data-ttu-id="8fd54-140">Hvis du vil styre administratorindstillinger for apps i Microsoft Teams, skal du gå til [Microsoft Teams Administration](https://admin.teams.microsoft.com/).</span><span class="sxs-lookup"><span data-stu-id="8fd54-140">To manage admin settings for apps in Microsoft Teams, go to the [Microsoft Teams admin center](https://admin.teams.microsoft.com/).</span></span> 

## <a name="see-also"></a><span data-ttu-id="8fd54-141">Se også</span><span class="sxs-lookup"><span data-stu-id="8fd54-141">See also</span></span> 

[<span data-ttu-id="8fd54-142">Downloade og installere Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="8fd54-142">Download and install Microsoft Teams</span></span>](https://support.office.com/article/download-and-install-microsoft-teams-422bf3aa-9ae8-46f1-83a2-e65720e1a34d)</br>
[<span data-ttu-id="8fd54-143">Microsoft Teams Hjælp-center</span><span class="sxs-lookup"><span data-stu-id="8fd54-143">Microsoft Teams help center</span></span>](https://support.office.com/teams)</br>
[<span data-ttu-id="8fd54-144">Administrere anmodninger i Teams</span><span class="sxs-lookup"><span data-stu-id="8fd54-144">Manage leave requests in Teams</span></span>](hr-teams-leave-app.md)

