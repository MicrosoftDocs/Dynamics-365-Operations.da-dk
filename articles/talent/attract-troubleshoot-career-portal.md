---
title: Attract-brugere kan ikke anvende job fra karriereportal
description: Dette emne forklarer, hvordan du lokaliserer fejl, når Attract-brugere ikke kan ansøge om job fra karriereportalen.
author: andreabichsel
manager: AnnBe
ms.date: 09/23/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Core, Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-09-23
ms.dyn365.ops.version: Platform update 24
ms.openlocfilehash: e1d72bef6d8bbe15e27326f66341915ba44a09b4
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4460652"
---
# <a name="attract-users-cant-apply-for-jobs-from-career-portal"></a><span data-ttu-id="7109b-103">Attract-brugere kan ikke anvende job fra karriereportal</span><span class="sxs-lookup"><span data-stu-id="7109b-103">Attract users can't apply for jobs from career portal</span></span>

[!include [banner](includes/banner.md)]

## <a name="issue"></a><span data-ttu-id="7109b-104">Udsted</span><span class="sxs-lookup"><span data-stu-id="7109b-104">Issue</span></span>

<span data-ttu-id="7109b-105">Attract-brugere kan ikke anvende job fra karriereportalen.</span><span class="sxs-lookup"><span data-stu-id="7109b-105">Attract users can't apply for jobs from the career portal.</span></span> <span data-ttu-id="7109b-106">Når de forsøger at ansøge om et job, der er oprettet i Dynamics 365 Talent: Attract, indlæser browseren hele siden og fuldfører ikke handlingen.</span><span class="sxs-lookup"><span data-stu-id="7109b-106">When they try to apply for a job that was created in Dynamics 365 Talent: Attract, the browser loads the page continuously and doesn't complete the action.</span></span>

## <a name="cause"></a><span data-ttu-id="7109b-107">Årsag</span><span class="sxs-lookup"><span data-stu-id="7109b-107">Cause</span></span>

<span data-ttu-id="7109b-108">Dette problem opstår, når talentrelationsteamet ikke har brugerrollen Talent.</span><span class="sxs-lookup"><span data-stu-id="7109b-108">This problem occurs when the Talent Relationship Team doesn't have the Talent user role.</span></span>

## <a name="resolution"></a><span data-ttu-id="7109b-109">Løsning</span><span class="sxs-lookup"><span data-stu-id="7109b-109">Resolution</span></span>

<span data-ttu-id="7109b-110">Tildel Talent-brugerrollen til talentrelationsteamet.</span><span class="sxs-lookup"><span data-stu-id="7109b-110">Assign the Talent user role to the Talent Relationship Team.</span></span>

1. <span data-ttu-id="7109b-111">Log på [Power Platform Administration](https://admin.powerplatform.microsoft.com) med en af følgende administratorlegitimationsoplysninger:</span><span class="sxs-lookup"><span data-stu-id="7109b-111">Sign in to the [Power Platform admin center](https://admin.powerplatform.microsoft.com) with any of the following admin credentials:</span></span>

   - <span data-ttu-id="7109b-112">Dynamics 365 Administration</span><span class="sxs-lookup"><span data-stu-id="7109b-112">Dynamics 365 admin</span></span>
   - <span data-ttu-id="7109b-113">Global administrator</span><span class="sxs-lookup"><span data-stu-id="7109b-113">Global admin</span></span>
   - <span data-ttu-id="7109b-114">Power Platform Administration</span><span class="sxs-lookup"><span data-stu-id="7109b-114">Power Platform admin</span></span>

2. <span data-ttu-id="7109b-115">Vælg **Miljøer** i navigationsruden, og vælg derefter det miljø, som brugerrollen Talent skal tildeles til talentrelationsteamet i.</span><span class="sxs-lookup"><span data-stu-id="7109b-115">In the navigation pane, select **Environments**, and then select the environment in which to assign the Talent user role to the Talent Relationship Team.</span></span>

   ![Vælg miljø](./media/attract-troubleshoot-career-portal-select-environment.png)

3. <span data-ttu-id="7109b-117">I ruden **Miljøer** skal du vælge **URL-adressen til miljøet** og logge på miljøets administrationsportal (f.eks. https:<orgname>.crm.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="7109b-117">In the **Environments** pane, select the **Environment URL** and sign in to the environment's admin portal (for example, https:<orgname>.crm.dynamics.com).</span></span>

4. <span data-ttu-id="7109b-118">Vælg **Indstillinger**, vælg **System**, og vælg derefter **Sikkerhed**.</span><span class="sxs-lookup"><span data-stu-id="7109b-118">Select **Settings**, select **System**, and then select **Security**.</span></span>

   ![Naviger til Sikkerhed](./media/attract-troubleshoot-career-portal-security.png)

5. <span data-ttu-id="7109b-120">Vælg **Teams**.</span><span class="sxs-lookup"><span data-stu-id="7109b-120">Select **Teams**.</span></span>

   ![Vælg Teams.](./media/attract-troubleshoot-career-portal-security-teams.png)

6. <span data-ttu-id="7109b-122">Søg efter **Talentrelationsteam** i søgefeltet, og vælg derefter teamet i søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="7109b-122">Search for **Talent Relationship Team** in the search box, and then select the team from the search results.</span></span>

7. <span data-ttu-id="7109b-123">Vælg **Administrer roller** på båndet.</span><span class="sxs-lookup"><span data-stu-id="7109b-123">Select **MANAGE ROLES** from the ribbon.</span></span>

8. <span data-ttu-id="7109b-124">Vælg **Talent-bruger** på listen over tilgængelige roller i dialogboksen **Administrer teamroller**, og vælg derefter **OK** for at anvende rollen.</span><span class="sxs-lookup"><span data-stu-id="7109b-124">In the **Manage Team Roles** dialog, select **Talent user** from the list of available roles, and then select **OK** to apply the role.</span></span>

   ![Anvend rolle](./media/attract-troubleshoot-career-portal-apply-role.png)

9. <span data-ttu-id="7109b-126">Test dine ændringer:</span><span class="sxs-lookup"><span data-stu-id="7109b-126">Test your changes:</span></span>

   1. <span data-ttu-id="7109b-127">Log på karriereportalen fra et nyt browservindue.</span><span class="sxs-lookup"><span data-stu-id="7109b-127">Sign in to the career portal from a new browser window.</span></span>
   2. <span data-ttu-id="7109b-128">Ansøg om jobbet fra karriereportalen.</span><span class="sxs-lookup"><span data-stu-id="7109b-128">Apply for the job from the career portal.</span></span> 