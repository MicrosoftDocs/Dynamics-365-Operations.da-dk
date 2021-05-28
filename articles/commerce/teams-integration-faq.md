---
title: Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration
description: Dette emne indeholder svar på ofte stillede spørgsmål vedrørende Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.
author: gvrmohanreddy
ms.date: 03/31/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.author: gmohanv
ms.search.validFrom: 2021-01-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: 3fc7cff0a3f8d0fbfb196ec5951b138088afece7
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/11/2021
ms.locfileid: "6019464"
---
# <a name="dynamics-365-commerce-and-microsoft-teams-integration-faq"></a><span data-ttu-id="a07d1-103">Ofte stillede spørgsmål til Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="a07d1-103">Dynamics 365 Commerce and Microsoft Teams integration FAQ</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a07d1-104">Dette emne indeholder svar på ofte stillede spørgsmål vedrørende Microsoft Dynamics 365 Commerce- og Microsoft Teams-integration.</span><span class="sxs-lookup"><span data-stu-id="a07d1-104">This topic provides answers to frequently asked questions regarding Microsoft Dynamics 365 Commerce and Microsoft Teams integration.</span></span>

### <a name="who-in-the-store-becomes-an-owner-of-a-team-while-provisioning-teams-from-commerce"></a><span data-ttu-id="a07d1-105">Hvem i butikken bliver ejer af et team, når Teams klargøres fra Commerce?</span><span class="sxs-lookup"><span data-stu-id="a07d1-105">Who in the store becomes an owner of a team while provisioning Teams from Commerce?</span></span> 

<span data-ttu-id="a07d1-106">Alle butikschefer føjes automatisk til den tilsvarende teamgruppe som ejere, så de kan udføre handlinger, f.eks. tilføjelse af en privat kanal og tilføjelse eller sletning af medlemmer.</span><span class="sxs-lookup"><span data-stu-id="a07d1-106">All store managers are automatically added as owners to the corresponding team group so that they can perform operations such as adding a private channel and adding or deleting members.</span></span> 

### <a name="how-do-i-assign-the-communications-manager-role-to-an-employee-in-commerce-headquarters"></a><span data-ttu-id="a07d1-107">Hvordan tildeler jeg rollen "kommunikationschef" til en medarbejder i Commerce-hovedkontoret?</span><span class="sxs-lookup"><span data-stu-id="a07d1-107">How do I assign the "communications manager" role to an employee in Commerce headquarters?</span></span> 

<span data-ttu-id="a07d1-108">Kommunikationschefer har i Microsoft Teams mulighed for at oprette og publicere opgavelister.</span><span class="sxs-lookup"><span data-stu-id="a07d1-108">Communication managers in Microsoft Teams have the ability to create and publish task lists.</span></span> <span data-ttu-id="a07d1-109">Organisationsmedarbejdere, der har brug for at blive kommunikationschefer, skal have rollen "detailopgaveadministrator" tildelt i Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="a07d1-109">Organization employees who need to become communication managers must have the "retail task manager" role assigned to them in Commerce headquarters.</span></span>

<span data-ttu-id="a07d1-110">Hvis du vil tildele rollen detailopgaveadministrator til en medarbejder i Commerce-hovedkontoret, skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="a07d1-110">To assign the retail task manager role to an employee in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="a07d1-111">Gå til **Retail og Commerce \> Medarbejdere \> Brugere**.</span><span class="sxs-lookup"><span data-stu-id="a07d1-111">Go to **Retail and Commerce \> Employees \> Users**.</span></span>
1. <span data-ttu-id="a07d1-112">Vælg medarbejderen.</span><span class="sxs-lookup"><span data-stu-id="a07d1-112">Select an employee.</span></span>
1. <span data-ttu-id="a07d1-113">Klik på **Tildel roller** i oversigtspanelet **Brugers roller**.</span><span class="sxs-lookup"><span data-stu-id="a07d1-113">On the **User's roles** FastTab, select **Assign roles**.</span></span>
1. <span data-ttu-id="a07d1-114">Vælg rollen **Retail Jobliste** i dialogboksen **Tildel roller til bruger**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a07d1-114">In the **Assign roles to user** dialog box, select the **Retail task manager** role, and then select **OK**.</span></span>

### <a name="how-do-i-make-a-specific-organization-hierarchy-available-to-upload-into-microsoft-teams"></a><span data-ttu-id="a07d1-115">Hvordan gør jeg et bestemt organisationshierarki tilgængeligt for upload til Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="a07d1-115">How do I make a specific organization hierarchy available to upload into Microsoft Teams?</span></span>

<span data-ttu-id="a07d1-116">I Commerce-hovedkontoret er hver organisations hierarki tilknyttet et eller flere formål.</span><span class="sxs-lookup"><span data-stu-id="a07d1-116">In Commerce headquarters, every organization's hierarchy is associated with one or more purposes.</span></span> <span data-ttu-id="a07d1-117">Kontrollér, at det hierarki, du vil klargøre til Microsoft Teams, har formålet **Detailrapportering** tilknyttet, som vist i følgende billede af eksemplet nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a07d1-117">Make sure the hierarchy that you want to provision into Microsoft Teams has the **Retail reporting** purpose associated with it, as shown in the following example image.</span></span> 

![Eksempel på et formål med organisationshierarki i Commerce-hovedkontoret](media/d365-commerce-organization-hierarchies-purpose.png)

### <a name="how-do-i-enable-retail-store-workers-to-sign-in-to-commerce-point-of-sale-pos-using-azure-active-directory-azure-ad"></a><span data-ttu-id="a07d1-119">Hvordan sætter jeg detailbutiksmedarbejdere i stand til at logge på Commerce POS via Azure Active Directory (Azure AD)?</span><span class="sxs-lookup"><span data-stu-id="a07d1-119">How do I enable retail store workers to sign in to Commerce point of sale (POS) using Azure Active Directory (Azure AD)?</span></span>

<span data-ttu-id="a07d1-120">Du kan finde oplysninger om, hvordan du konfigurerer Commerce POS-logon til at bruge Azure AD-godkendelse, i [Aktivere Azure Active Directory-godkendelse for POS-logon](aad-pos-logon.md).</span><span class="sxs-lookup"><span data-stu-id="a07d1-120">For information about how to configure the Commerce POS sign-in experience to use Azure AD authentication, see [Enable Azure Active Directory authentication for POS sign-in](aad-pos-logon.md).</span></span>

### <a name="how-do-i-map-stores-and-corresponding-teams-in-commerce-headquarters-if-my-organization-has-already-created-teams-in-microsoft-teams"></a><span data-ttu-id="a07d1-121">Hvordan tilknytter jeg butikker og tilsvarende teams i Commerce-hovedkontoret, hvis min organisation allerede har oprettet teams i Microsoft Teams?</span><span class="sxs-lookup"><span data-stu-id="a07d1-121">How do I map stores and corresponding teams in Commerce headquarters if my organization has already created teams in Microsoft Teams?</span></span>

<span data-ttu-id="a07d1-122">Oplysninger om, hvordan du kan tilknytte butikker og teams, hvis der findes eksisterende teams, finder du i [Tilknytte butikker og tilsvarende teams, hvis organisationen har eksisterende teams i Microsoft Teams](map-stores-existing-teams.md).</span><span class="sxs-lookup"><span data-stu-id="a07d1-122">For information on how to map stores and teams if there are pre-existing teams, see [Map stores and corresponding teams if your organization has pre-existing teams in Microsoft Teams](map-stores-existing-teams.md).</span></span>

### <a name="how-do-i-clear-the-microsoft-graph-api-token-stored-in-the-session-storage"></a><span data-ttu-id="a07d1-123">Hvordan rydder jeg det Microsoft Graph API-token, der er gemt i sessionslageret?</span><span class="sxs-lookup"><span data-stu-id="a07d1-123">How do I clear the Microsoft Graph API token stored in the session storage?</span></span>

<span data-ttu-id="a07d1-124">En bruger, der har logget på POS POS med en Azure Active Directory-konto (Azure AD), skal logge af POS eller lukke programmet for at rydde sessionslageret.</span><span class="sxs-lookup"><span data-stu-id="a07d1-124">A user who has signed in to the point of sale (POS) with an Azure Active Directory (Azure AD) account should sign out from the POS or close the application to clear the session storage.</span></span> 

> [!TIP]
> <span data-ttu-id="a07d1-125">Det anbefales at anvende den bedste fremgangsmåde, hvis butiksmedarbejdere altid låser POS-terminalen eller logger af en session, når de ikke bruger terminalen.</span><span class="sxs-lookup"><span data-stu-id="a07d1-125">A recommended best practice is to always have store workers lock the POS terminal or sign out from a session when not using the terminal.</span></span> 

### <a name="what-happens-if-a-store-doesnt-have-store-managers"></a><span data-ttu-id="a07d1-126">Hvad sker der, hvis en butik ikke har butikschefer?</span><span class="sxs-lookup"><span data-stu-id="a07d1-126">What happens if a store doesn't have store managers?</span></span>

<span data-ttu-id="a07d1-127">Hvis en butik ikke har chefer, oprettes der ikke en teamgruppe for butikken eller i Teams.</span><span class="sxs-lookup"><span data-stu-id="a07d1-127">If a store doesn't have managers, a team group will not be created for the store or in Teams.</span></span> 

### <a name="what-happens-if-a-store-manager-leaves-the-company"></a><span data-ttu-id="a07d1-128">Hvad sker der, hvis en butikschef forlader firmaet?</span><span class="sxs-lookup"><span data-stu-id="a07d1-128">What happens if a store manager leaves the company?</span></span>

<span data-ttu-id="a07d1-129">Alle med ejerrollen kan tilføje en ny butikschef i Commerce-hovedkontoret og klargøre Teams igen, så den nye chef får de nødvendige rettigheder i Teams for gruppen.</span><span class="sxs-lookup"><span data-stu-id="a07d1-129">Anyone with the owner role can add a new store manager in Commerce headquarters and reprovision Teams so that the new manager will have the necessary privileges in Teams for the group.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="a07d1-130">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a07d1-130">Additional resources</span></span>

[<span data-ttu-id="a07d1-131">Oversigt over Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="a07d1-131">Dynamics 365 Commerce and Microsoft Teams integration overview</span></span>](commerce-teams-integration.md)

[<span data-ttu-id="a07d1-132">Aktivere Dynamics 365 Commerce- og Microsoft Teams-integration</span><span class="sxs-lookup"><span data-stu-id="a07d1-132">Enable Dynamics 365 Commerce and Microsoft Teams integration</span></span>](enable-teams-integration.md)

[<span data-ttu-id="a07d1-133">Klargøre Microsoft Teams fra Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="a07d1-133">Provision Microsoft Teams from Dynamics 365 Commerce</span></span>](provision-teams-from-commerce.md)

[<span data-ttu-id="a07d1-134">Synkronisere opgavestyring mellem Microsoft Teams og Dynamics 365 Commerce POS</span><span class="sxs-lookup"><span data-stu-id="a07d1-134">Synchronize task management between Microsoft Teams and Dynamics 365 Commerce POS</span></span>](synchronize-tasks-teams-pos.md)

[<span data-ttu-id="a07d1-135">Administrere brugerroller i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a07d1-135">Manage user roles in Microsoft Teams</span></span>](manage-user-roles-teams.md)

[<span data-ttu-id="a07d1-136">Tilknytte butikker og teams, hvis der er eksisterende teams i Microsoft Teams</span><span class="sxs-lookup"><span data-stu-id="a07d1-136">Map stores and teams if there are pre-existing teams in Microsoft Teams</span></span>](map-stores-existing-teams.md)
