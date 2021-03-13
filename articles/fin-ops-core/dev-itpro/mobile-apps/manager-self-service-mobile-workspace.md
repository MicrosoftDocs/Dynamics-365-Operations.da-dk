---
title: Arbejdsområdet Mit team til mobilenheder
description: Dette emne indeholder oplysninger om arbejdsområdet Mit team til mobilenheder, hvor ledere kan se deres direkte underordnede og udvidede personale.
author: ShielaSogge
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 79678c42545a07054af00cd408e04e9d1a42caed
ms.sourcegitcommit: f8bac7ca2803913fd236adbc3806259a17a110f4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/06/2021
ms.locfileid: "5127539"
---
# <a name="my-team-mobile-workspace"></a><span data-ttu-id="00cb9-103">Mobilarbejdsområdet Mit team</span><span class="sxs-lookup"><span data-stu-id="00cb9-103">My team mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="00cb9-104">Dette emne indeholder oplysninger om arbejdsområdet **Mit team** til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="00cb9-104">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="00cb9-105">I dette arbejdsområde kan ledere se deres direkte underordnede og udvidede personale.</span><span class="sxs-lookup"><span data-stu-id="00cb9-105">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="00cb9-106">De kan også sende ros til enkeltpersoner i deres rapporteringskæde.</span><span class="sxs-lookup"><span data-stu-id="00cb9-106">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="00cb9-107">Dette mobile arbejdsområde er beregnet til brug sammen med Finance and Operations-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="00cb9-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="00cb9-108">Oversigt</span><span class="sxs-lookup"><span data-stu-id="00cb9-108">Overview</span></span> 
<span data-ttu-id="00cb9-109">I arbejdsområdet **Mit team** til mobilenheder kan ledere udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="00cb9-109">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="00cb9-110">Vis en oversigt over lederens direkte underordnede.</span><span class="sxs-lookup"><span data-stu-id="00cb9-110">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="00cb9-111">Vis en oversigt over lederens underordnede rapporteringsteam.</span><span class="sxs-lookup"><span data-stu-id="00cb9-111">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="00cb9-112">Få vist detaljerede oplysninger for hvert teammedlem, f.eks. fødselsdato, anciennitetsdato, år i tjeneste og oplysninger om kompensation og performance.</span><span class="sxs-lookup"><span data-stu-id="00cb9-112">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="00cb9-113">Send ros til en person i lederens udvidede rapporteringsteam.</span><span class="sxs-lookup"><span data-stu-id="00cb9-113">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="00cb9-114">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="00cb9-114">Prerequisites</span></span>
<span data-ttu-id="00cb9-115">Før du kan bruge dette mobilarbejdsområde, skal følgende forudsætninger være opfyldt.</span><span class="sxs-lookup"><span data-stu-id="00cb9-115">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="00cb9-116">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="00cb9-116">Prerequisite</span></span></th>
<th><span data-ttu-id="00cb9-117">Rolle</span><span class="sxs-lookup"><span data-stu-id="00cb9-117">Role</span></span></th>
<th><span data-ttu-id="00cb9-118">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="00cb9-118">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="00cb9-119">Et af følgende produkter skal være installeret i organisationen:</span><span class="sxs-lookup"><span data-stu-id="00cb9-119">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="00cb9-120">En Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="00cb9-120">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="00cb9-121">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="00cb9-121">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="00cb9-122">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="00cb9-122">System administrator</span></span></td>
<td><span data-ttu-id="00cb9-123">Hvis en Finance and Operations-app ikke allerede er udrullet i organisationen, kan du se <a href="../deployment/deploy-demo-environment.md">Installere er demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="00cb9-123">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="00cb9-124">Hvis du ikke allerede har installeret Personale i organisationen, kan systemadministratoren få adgang til en prøveversion fra <a href="https://dynamics.microsoft.com/human-resources/overview/">Personale-websiden</a>.</span><span class="sxs-lookup"><span data-stu-id="00cb9-124">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="00cb9-125">Mobilarbejdsområdet <strong>Mit team</strong> skal være publiceret.</span><span class="sxs-lookup"><span data-stu-id="00cb9-125">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="00cb9-126">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="00cb9-126">System administrator</span></span></td>
<td><span data-ttu-id="00cb9-127">Se <a href="publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</span><span class="sxs-lookup"><span data-stu-id="00cb9-127">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="00cb9-128">Downloade og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="00cb9-128">Download and install the mobile app</span></span>

<span data-ttu-id="00cb9-129">Sådan downloades og installeres Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="00cb9-129">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="00cb9-130">Til Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="00cb9-130">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="00cb9-131">Til iPhones</span><span class="sxs-lookup"><span data-stu-id="00cb9-131">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="00cb9-132">Log på mobilappen</span><span class="sxs-lookup"><span data-stu-id="00cb9-132">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="00cb9-133">Start appen på din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="00cb9-133">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="00cb9-134">Angiv din Microsoft Dynamics 365 URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="00cb9-134">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="00cb9-135">Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="00cb9-135">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="00cb9-136">Angiv dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="00cb9-136">Enter your credentials.</span></span>
4.  <span data-ttu-id="00cb9-137">Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="00cb9-137">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="00cb9-138">Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="00cb9-138">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="00cb9-139">[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="00cb9-139">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="00cb9-140">Få vist teammedlemmer ved hjælp af arbejdsområdet Mit team til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="00cb9-140">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="00cb9-141">I mobilappen skal du vælge mobilarbejdsområdet **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="00cb9-141">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="00cb9-142">Der vises en oversigt over teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="00cb9-142">A list of team members is shown.</span></span> <span data-ttu-id="00cb9-143">Oversigten viser også hvert teammedlems titel og eventuelle direkte underordnede, som medlemmet har.</span><span class="sxs-lookup"><span data-stu-id="00cb9-143">The list also shows each team member's title, and any direct reports that the member has.</span></span>
2.  <span data-ttu-id="00cb9-144">Vælg et teammedlem.</span><span class="sxs-lookup"><span data-stu-id="00cb9-144">Select a team member.</span></span> <span data-ttu-id="00cb9-145">Siden **Oversigt over teammedlem** vises.</span><span class="sxs-lookup"><span data-stu-id="00cb9-145">The **Team member summary** page appears.</span></span> <span data-ttu-id="00cb9-146">Oplysningerne på denne side indeholder teammedlemmets fødselsdato, anciennitetsdato, antal år i tjeneste, år i den aktuelle stilling og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="00cb9-146">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="00cb9-147">Få vist udvidede teammedlemmer ved hjælp af arbejdsområdet Mit team til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="00cb9-147">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="00cb9-148">I mobilappen skal du vælge mobilarbejdsområdet **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="00cb9-148">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="00cb9-149">Der vises en oversigt over teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="00cb9-149">A list of team members is shown.</span></span> <span data-ttu-id="00cb9-150">Oversigten viser også hvert teammedlems titel og eventuelle direkte underordnede, som medlemmet har.</span><span class="sxs-lookup"><span data-stu-id="00cb9-150">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="00cb9-151">Vælg linket **Direkte rapporter**.</span><span class="sxs-lookup"><span data-stu-id="00cb9-151">Select the **Direct reports** link.</span></span> <span data-ttu-id="00cb9-152">Der vises en oversigt over dit udvidede team.</span><span class="sxs-lookup"><span data-stu-id="00cb9-152">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="00cb9-153">Vælg et teammedlem.</span><span class="sxs-lookup"><span data-stu-id="00cb9-153">Select a team member.</span></span> <span data-ttu-id="00cb9-154">Siden **Oversigt over teammedlem** vises.</span><span class="sxs-lookup"><span data-stu-id="00cb9-154">The **Team member summary** page appears.</span></span> <span data-ttu-id="00cb9-155">Oplysningerne på denne side indeholder teammedlemmets fødselsdato, anciennitetsdato, antal år i tjeneste, år i den aktuelle stilling og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="00cb9-155">The information on this page includes the team member's birth date, seniority date, years of service, years in the current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="00cb9-156">Sende ros om teammedlemmer ved hjælp af arbejdsområdet Mit team til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="00cb9-156">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="00cb9-157">I mobilappen skal du vælge mobilarbejdsområdet **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="00cb9-157">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="00cb9-158">Der vises en oversigt over teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="00cb9-158">A list of team members is shown.</span></span> <span data-ttu-id="00cb9-159">Oversigten viser også hvert teammedlems titel og eventuelle direkte underordnede, som medlemmet har.</span><span class="sxs-lookup"><span data-stu-id="00cb9-159">The list also shows each team member's title, and any direct reports that the member has.</span></span>
1.  <span data-ttu-id="00cb9-160">Vælg et teammedlem.</span><span class="sxs-lookup"><span data-stu-id="00cb9-160">Select a team member.</span></span> <span data-ttu-id="00cb9-161">Siden **Oversigt over teammedlem** vises.</span><span class="sxs-lookup"><span data-stu-id="00cb9-161">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="00cb9-162">Vælg **Send ros**.</span><span class="sxs-lookup"><span data-stu-id="00cb9-162">Select **Send praise**.</span></span> 
1. <span data-ttu-id="00cb9-163">Angiv teksten til den ros, du vil sende.</span><span class="sxs-lookup"><span data-stu-id="00cb9-163">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="00cb9-164">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="00cb9-164">Select **Done**.</span></span>
