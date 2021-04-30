---
title: Klargøre Microsoft Teams fra Dynamics 365 Commerce
description: I dette emne beskrives, hvordan Microsoft Teams kan klargøres ved hjælp af organisationsdata fra Dynamics 365 Commerce.
author: gvrmohanreddy
manager: annbe
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: ba7c74942735b723d1015dc4da0068fbb631bc6b
ms.sourcegitcommit: 34b478f175348d99df4f2f0c2f6c0c21b6b2660a
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/16/2021
ms.locfileid: "5908898"
---
# <a name="provision-microsoft-teams-from-dynamics-365-commerce"></a><span data-ttu-id="1a3ba-103">Klargøre Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="1a3ba-103">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1a3ba-104">I dette emne beskrives, hvordan Microsoft Teams kan klargøres ved hjælp af organisationsdata fra Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-104">This topic describes how to provision Microsoft Teams by using organizational data from Dynamics 365 Commerce.</span></span>

<span data-ttu-id="1a3ba-105">Dynamics 365 Commerce er en nem måde at klargøre Teams på, hvis du endnu ikke har konfigureret teams til dine detailforretninger der.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-105">Dynamics 365 Commerce offers an easy way to provision Teams if you haven't yet set up teams for your retail stores there.</span></span> <span data-ttu-id="1a3ba-106">Ved at udnytte veldefinerede oplysninger fra Commerce, som du vil bruge i Teams, kan du hjælpe butiksmedarbejderne med at komme i gang i Teams.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-106">By taking advantage of well-defined information from Commerce that you want to use in Teams, you can help your store employees get started in Teams.</span></span> <span data-ttu-id="1a3ba-107">Disse oplysninger omfatter organisationshierarki, butiksnavne, medarbejderoplysninger og Azure Active Directory-konti (Azure AD).</span><span class="sxs-lookup"><span data-stu-id="1a3ba-107">This information includes the organizational hierarchy, store names, employee information, and Azure Active Directory (Azure AD) accounts.</span></span> 

<span data-ttu-id="1a3ba-108">Klargøringsprocessen for Teams har to hovedtrin:</span><span class="sxs-lookup"><span data-stu-id="1a3ba-108">The process of provisioning Teams has two main steps:</span></span>

1. <span data-ttu-id="1a3ba-109">I Teams skal du oprette et team for hver detailbutik og tilføje butiksmedarbejdere som medlemmer af det relevante team.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-109">In Teams, create a team for each retail store, and add store workers as members of the appropriate team.</span></span> <span data-ttu-id="1a3ba-110">Hvis en medarbejder er tilknyttet mere end én detailbutik, afspejler teammedlemskab dette.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-110">If an employee is associated with more than one retail store, team membership will reflect that fact.</span></span> <span data-ttu-id="1a3ba-111">Der oprettes et kommunikationsteam, der omfatter lokale ledere som medlemmer, som kan hjælpe med at publicere opgaver fra Teams.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-111">A communications team that includes regional managers as members will be created to help publish tasks from Teams.</span></span>
1. <span data-ttu-id="1a3ba-112">Upload dit organisationshierarki fra Commerce til Teams.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-112">Upload your organizational hierarchy from Commerce to Teams.</span></span>

## <a name="provision-teams-in-commerce-headquarters"></a><span data-ttu-id="1a3ba-113">Klargøre Teams i Commerce-hovedkontor</span><span class="sxs-lookup"><span data-stu-id="1a3ba-113">Provision Teams in Commerce headquarters</span></span>

<span data-ttu-id="1a3ba-114">Udfør følgende opgaver, før du klargør Microsoft Teams:</span><span class="sxs-lookup"><span data-stu-id="1a3ba-114">Before you provision Microsoft Teams, complete these tasks:</span></span>

- <span data-ttu-id="1a3ba-115">Bekræft, at alle regionchefer er blevet gjort til kommunikationschefer.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-115">Confirm that all regional managers have been made communications managers.</span></span>
- <span data-ttu-id="1a3ba-116">Bekræft, at Azure-kontoen for hver butikschef og medarbejder er blevet knyttet til den pågældende chefs eller medarbejders arbejderpost i Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-116">Confirm that the Azure account of every store manager and worker has been associated with that manager's or worker's worker record in Commerce headquarters.</span></span>

<span data-ttu-id="1a3ba-117">Du kan klargøre Teams i Commerce-hovedkontoret ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-117">To provision Teams in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="1a3ba-118">Gå til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af Microsoft Teams-integration**.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-118">Go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="1a3ba-119">Vælg **Klargør Teams** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-119">On the Action Pane, select **Provision teams**.</span></span> <span data-ttu-id="1a3ba-120">Der oprettes et batchjob med navnet **Teams-klargøring**.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-120">A batch job that is named **Teams provision** is created.</span></span>
1. <span data-ttu-id="1a3ba-121">Gå til **Systemadministration \> Forespørgsler \> Batchjob**, og find det seneste job, der indeholder beskrivelsen **Teams-klargøring**.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-121">Go to **System administration \> Inquiries \> Batch jobs**, and find the most recent job that has the description **Teams provision**.</span></span> <span data-ttu-id="1a3ba-122">Vent, indtil jobbet er kørt færdig.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-122">Wait until this job has finished running.</span></span>

> [!TIP]
> <span data-ttu-id="1a3ba-123">Hvis ingen af dine lokale ledere, butikschefer og butiksmedarbejdere er blevet tilknyttet en Teams-licens, kan du få vist følgende fejlmeddelelse: "Det lykkedes ikke at hente brugbare SKU-kategorier for brugeren".</span><span class="sxs-lookup"><span data-stu-id="1a3ba-123">If none of your regional managers, store managers, and store workers have been associated with a Teams license, you might receive the following error message: "Failed to retrieve appliable Sku categories for the user."</span></span> <span data-ttu-id="1a3ba-124">Hvis du vil løse problemet, skal du vælge **Synkroniser teams og medlemmer** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-124">To correct the issue, select **Sync teams and members** on the Action Pane.</span></span>

<!-- ![Dynamics 365 Commerce - Teams integration configuration](media/D365-Commerce-Microsoft-Teams-Configuration_with_disclaimer.png)-->

## <a name="validate-teams-provisioning-in-the-teams-admin-center"></a><span data-ttu-id="1a3ba-125">Validere klargøring af Teams i Teams Administration</span><span class="sxs-lookup"><span data-stu-id="1a3ba-125">Validate Teams provisioning in the Teams admin center</span></span>

<span data-ttu-id="1a3ba-126">Hvis du vil validere Microsoft Teams-klargøring i Microsoft Teams Administrationen, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-126">To validate Microsoft Teams provisioning in the Microsoft Teams admin center, follow these steps.</span></span>
    
1. <span data-ttu-id="1a3ba-127">Gå til [Teams Administration](https://admin.teams.microsoft.com/), og log på som administrator af din e-handelslejer.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-127">Go to the [Teams admin center](https://admin.teams.microsoft.com/), and sign in as the administrator of your e-commerce tenant.</span></span>
1. <span data-ttu-id="1a3ba-128">Vælg **Teams** i venstre navigationsrude for at udvide den, og vælg derefter **Administrer teams**.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-128">In the left navigation pane, select **Teams** to expand it, and then select **Manage teams**.</span></span>
1. <span data-ttu-id="1a3ba-129">Bekræft, at der er oprettet ét team for hver Commerce-detailbutik.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-129">Confirm that one team has been created for each Commerce retail store.</span></span>
1. <span data-ttu-id="1a3ba-130">Vælg et team, og bekræft, at butiksmedarbejdere er føjet til det som medlemmer.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-130">Select a team, and confirm that store workers have been added to it as members.</span></span>
1. <span data-ttu-id="1a3ba-131">Vælg **Brugere** i venstre navigationsrude, og bekræft, at alle butiksmedarbejdere i alle butikker er blevet tilføjet som brugere.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-131">In the left navigation pane, select **Users**, and confirm that all store employees in all stores have been added as users.</span></span>

<span data-ttu-id="1a3ba-132">I følgende illustration vises et eksempel på siden **Administrer teams** i Teams Administration.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-132">The following illustration shows an example of the **Manage teams** page in the Teams admin center.</span></span>

![Eksempel på siden Administrer teams i Teams Administration](media/Teams-FLW-Admin-Teams.png)

## <a name="upload-a-commerce-organizational-hierarchy-to-teams"></a><span data-ttu-id="1a3ba-134">Uploade et Commerce-organisationshierarki til Teams</span><span class="sxs-lookup"><span data-stu-id="1a3ba-134">Upload a Commerce organizational hierarchy to Teams</span></span>
    
<span data-ttu-id="1a3ba-135">Commerce-organisationshierarkiet kan bruges i Microsoft Teams til at publicere opgaver til alle eller udvalgte butikker, der bruger samme hierarkistruktur.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-135">The Commerce organizational hierarchy can be used in Microsoft Teams to publish tasks to all or selected stores that use the same hierarchy structure.</span></span>

<span data-ttu-id="1a3ba-136">Følg disse trin for at uploade et Commerce-organisationshierarki til Teams.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-136">To upload a Commerce organizational hierarchy to Teams, follow these steps.</span></span>
    
1. <span data-ttu-id="1a3ba-137">Gå i Commerce-hovedkontoret til **Retail og Commerce \> Konfiguration af kanal \> Konfiguration af Microsoft Teams-integration**.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-137">In Commerce headquarters, go to **Retail and Commerce \> Channel setup \> Microsoft Teams Integration Configuration**.</span></span>
1. <span data-ttu-id="1a3ba-138">Vælg **Download målretningshierarki**, og vælg derefter **Detailbutikker efter område** for at downloade en kommasepareret fil (CSV) med organisationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-138">Select **Download targeting hierarchy**, and then select **Retail Stores by Region** to download a comma-separated values (CSV) file of the organizational hierarchy.</span></span>
1. <span data-ttu-id="1a3ba-139">Installer Microsoft Teams PowerShell-modulet ved at følge trinnene i [Installere Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span><span class="sxs-lookup"><span data-stu-id="1a3ba-139">Install the Microsoft Teams PowerShell module by following the steps in [Install Microsoft Teams PowerShell](https://docs.microsoft.com/microsoftteams/teams-powershell-install).</span></span>
1. <span data-ttu-id="1a3ba-140">Når du bliver bedt om det i Teams PowerShell-vinduet, skal du logge på med administratorkontoen for din Azure AD-lejer.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-140">When you're prompted in the Teams PowerShell window, sign in by using the administrator account for your Azure AD tenant.</span></span>
1. <span data-ttu-id="1a3ba-141">Følg trinnene i [Konfigurere dit teammålretningshierarki](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) for at uploade CSV-filen til målretningshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-141">Follow the steps in [Set up your team targeting hierarchy](https://docs.microsoft.com/microsoftteams/set-up-your-team-hierarchy) to upload the CSV file for the targeting hierarchy.</span></span>

## <a name="verify-that-the-organizational-hierarchy-was-uploaded-to-teams"></a><span data-ttu-id="1a3ba-142">Kontrollere, at organisationshierarkiet er blevet uploadet til Teams</span><span class="sxs-lookup"><span data-stu-id="1a3ba-142">Verify that the organizational hierarchy was uploaded to Teams</span></span>

<span data-ttu-id="1a3ba-143">Du kan kontrollere, at organisationshierarkiet er blevet uploadet til Microsoft Teams, ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-143">To verify that the organizational hierarchy was uploaded to Microsoft Teams, follow these steps.</span></span>

1. <span data-ttu-id="1a3ba-144">Log på Teams som kommunikationschef.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-144">Sign in to Teams as a communications manager.</span></span>
1. <span data-ttu-id="1a3ba-145">Vælg **Opgaver efter planlægning** i den venstre navigationsrude.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-145">In the left navigation pane, select **Tasks by Planner**.</span></span>
1. <span data-ttu-id="1a3ba-146">Opret en ny liste med en dummy-opgave under fanen **Publicerede lister**.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-146">On the **Published lists** tab, create a new list that has a dummy task.</span></span>
1. <span data-ttu-id="1a3ba-147">Vælg **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-147">Select **Publish**.</span></span> <span data-ttu-id="1a3ba-148">Organisationshierarkiet skal vises i dialogboksen **Vælg, hvem der skal publiceres til**, som vist i eksemplet på følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="1a3ba-148">The organizational hierarchy should appear in the **Select who to publish to** dialog box, as shown in the example in the following illustration.</span></span>

![Eksempel på et organisationshierarki i dialogboksen Vælg, hvem der skal publiceres til](media/Microsoft-teams-verify-org-hierarchy.png)

## <a name="additional-resources"></a><span data-ttu-id="1a3ba-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1a3ba-150">Additional resources</span></span>

[<span data-ttu-id="1a3ba-151">Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="1a3ba-151">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="1a3ba-152">Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="1a3ba-152">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="1a3ba-153">Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="1a3ba-153">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="1a3ba-154">Administrere brugerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1a3ba-154">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="1a3ba-155">Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="1a3ba-155">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)

[<span data-ttu-id="1a3ba-156">Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="1a3ba-156">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>](teams-integration-faq.md)
