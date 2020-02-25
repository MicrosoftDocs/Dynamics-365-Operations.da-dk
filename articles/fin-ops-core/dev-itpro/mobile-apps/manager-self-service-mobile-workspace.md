---
title: Arbejdsområdet Mit team til mobilenheder
description: Dette emne indeholder oplysninger om arbejdsområdet Mit team til mobilenheder, hvor ledere kan se deres direkte underordnede og udvidede personale. Brugerne kan også sende ros til enkeltpersoner i deres rapporteringskæde.
author: ShielaSogge
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.scope: Operations, Human Resources
ms.search.region: Global
ms.author: shielas
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: c2ad5f30ed0e69df1769eb0379b5da2865d4ce4f
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3005603"
---
# <a name="my-team-mobile-workspace"></a><span data-ttu-id="d9497-104">Arbejdsområdet Mit team til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="d9497-104">My team mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="d9497-105">Dette emne indeholder oplysninger om arbejdsområdet **Mit team** til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="d9497-105">This topic provides information about the **My team** mobile workspace.</span></span> <span data-ttu-id="d9497-106">I dette arbejdsområde kan ledere se deres direkte underordnede og udvidede personale.</span><span class="sxs-lookup"><span data-stu-id="d9497-106">This workspace lets managers view their direct reports and extended staff.</span></span> <span data-ttu-id="d9497-107">De kan også sende ros til enkeltpersoner i deres rapporteringskæde.</span><span class="sxs-lookup"><span data-stu-id="d9497-107">They can also send praise to individuals in their reporting chain.</span></span>

<span data-ttu-id="d9497-108">Dette mobile arbejdsområde er beregnet til brug sammen med Finance and Operations-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="d9497-108">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="d9497-109">Oversigt</span><span class="sxs-lookup"><span data-stu-id="d9497-109">Overview</span></span> 
<span data-ttu-id="d9497-110">I arbejdsområdet **Mit team** til mobilenheder kan ledere udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="d9497-110">The **My team** mobile workspace lets managers perform these tasks:</span></span>

- <span data-ttu-id="d9497-111">Vis en oversigt over lederens direkte underordnede.</span><span class="sxs-lookup"><span data-stu-id="d9497-111">View a list of the manager’s direct reports.</span></span>
- <span data-ttu-id="d9497-112">Vis en oversigt over lederens underordnede rapporteringsteam.</span><span class="sxs-lookup"><span data-stu-id="d9497-112">View a list of the manager’s extended reporting team.</span></span>
- <span data-ttu-id="d9497-113">Få vist detaljerede oplysninger for hvert teammedlem, f.eks. fødselsdato, anciennitetsdato, år i tjeneste og oplysninger om kompensation og performance.</span><span class="sxs-lookup"><span data-stu-id="d9497-113">View detailed information for each team member, such as birth date, seniority date, years of service, and compensation and performance information.</span></span>
- <span data-ttu-id="d9497-114">Send ros til en person i lederens udvidede rapporteringsteam.</span><span class="sxs-lookup"><span data-stu-id="d9497-114">Send praise to any individual in the manager’s extended reporting team.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="d9497-115">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="d9497-115">Prerequisites</span></span>
<span data-ttu-id="d9497-116">Før du kan bruge dette mobilarbejdsområde, skal følgende forudsætninger være opfyldt.</span><span class="sxs-lookup"><span data-stu-id="d9497-116">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="d9497-117">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="d9497-117">Prerequisite</span></span></th>
<th><span data-ttu-id="d9497-118">Rolle</span><span class="sxs-lookup"><span data-stu-id="d9497-118">Role</span></span></th>
<th><span data-ttu-id="d9497-119">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="d9497-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="d9497-120">Et af følgende produkter skal være installeret i organisationen:</span><span class="sxs-lookup"><span data-stu-id="d9497-120">One of the following products must be deployed in your organization:</span></span>
<ul><li><span data-ttu-id="d9497-121">En Finance and Operations-app</span><span class="sxs-lookup"><span data-stu-id="d9497-121">A Finance and Operations app</span></span></li>
<li><span data-ttu-id="d9497-122">Microsoft Dynamics 365 Human Resources</span><span class="sxs-lookup"><span data-stu-id="d9497-122">Microsoft Dynamics 365 Human Resources</span></span></li>
</ul>
</td>
<td><span data-ttu-id="d9497-123">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="d9497-123">System administrator</span></span></td>
<td><span data-ttu-id="d9497-124">Hvis en Finance and Operations-app ikke allerede er udrullet i organisationen, kan du se <a href="../deployment/deploy-demo-environment.md">Installere er demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="d9497-124">If you don&#39;t already have a Finance and Operations app deployed in your organization, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span> <span data-ttu-id="d9497-125">Hvis du ikke allerede har installeret Personale i organisationen, kan systemadministratoren få adgang til en prøveversion fra <a href="https://dynamics.microsoft.com/human-resources/overview/">Personale-websiden</a>.</span><span class="sxs-lookup"><span data-stu-id="d9497-125">If you don&#39;t already have Human Resources deployed in your organization, the system administrator can access a trial version from the <a href="https://dynamics.microsoft.com/human-resources/overview/">Human Resources webpage</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="d9497-126">Mobilarbejdsområdet <strong>Mit team</strong> skal være publiceret.</span><span class="sxs-lookup"><span data-stu-id="d9497-126">The <strong>My team</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="d9497-127">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="d9497-127">System administrator</span></span></td>
<td><span data-ttu-id="d9497-128">Se <a href="publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</span><span class="sxs-lookup"><span data-stu-id="d9497-128">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="d9497-129">Downloade og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="d9497-129">Download and install the mobile app</span></span>

<span data-ttu-id="d9497-130">Sådan downloades og installeres Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="d9497-130">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="d9497-131">Til Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="d9497-131">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="d9497-132">Til iPhones</span><span class="sxs-lookup"><span data-stu-id="d9497-132">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="d9497-133">Log på mobilappen</span><span class="sxs-lookup"><span data-stu-id="d9497-133">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="d9497-134">Start appen på din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="d9497-134">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="d9497-135">Angiv din Microsoft Dynamics 365 URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="d9497-135">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="d9497-136">Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="d9497-136">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="d9497-137">Angiv dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d9497-137">Enter your credentials.</span></span>
4.  <span data-ttu-id="d9497-138">Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="d9497-138">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="d9497-139">Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="d9497-139">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="d9497-140">[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="d9497-140">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="view-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="d9497-141">Få vist teammedlemmer ved hjælp af arbejdsområdet Mit team til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="d9497-141">View team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="d9497-142">I mobilappen skal du vælge mobilarbejdsområdet **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="d9497-142">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="d9497-143">Der vises en oversigt over teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="d9497-143">A list of team members is shown.</span></span> <span data-ttu-id="d9497-144">Oversigten viser også hvert teammedlems titel og eventuelle direkte underordnede, som han eller hun har.</span><span class="sxs-lookup"><span data-stu-id="d9497-144">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
2.  <span data-ttu-id="d9497-145">Vælg et teammedlem.</span><span class="sxs-lookup"><span data-stu-id="d9497-145">Select a team member.</span></span> <span data-ttu-id="d9497-146">Siden **Oversigt over teammedlem** vises.</span><span class="sxs-lookup"><span data-stu-id="d9497-146">The **Team member summary** page appears.</span></span> <span data-ttu-id="d9497-147">Oplysningerne på denne side indeholder teammedlemmets fødselsdato, anciennitetsdato, antal år i tjeneste, år i den aktuelle stilling og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d9497-147">The information on this page includes the team member's birth date, seniority date, years of service, years in his or her current position, and compensation information.</span></span>

## <a name="view-extended-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="d9497-148">Få vist udvidede teammedlemmer ved hjælp af arbejdsområdet Mit team til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="d9497-148">View extended team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="d9497-149">I mobilappen skal du vælge mobilarbejdsområdet **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="d9497-149">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="d9497-150">Der vises en oversigt over teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="d9497-150">A list of team members is shown.</span></span> <span data-ttu-id="d9497-151">Oversigten viser også hvert teammedlems titel og eventuelle direkte underordnede, som han eller hun har.</span><span class="sxs-lookup"><span data-stu-id="d9497-151">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
1.  <span data-ttu-id="d9497-152">Vælg linket **Direkte rapporter**.</span><span class="sxs-lookup"><span data-stu-id="d9497-152">Select the **Direct reports** link.</span></span> <span data-ttu-id="d9497-153">Der vises en oversigt over dit udvidede team.</span><span class="sxs-lookup"><span data-stu-id="d9497-153">A list of your extended team is shown.</span></span>
1.  <span data-ttu-id="d9497-154">Vælg et teammedlem.</span><span class="sxs-lookup"><span data-stu-id="d9497-154">Select a team member.</span></span> <span data-ttu-id="d9497-155">Siden **Oversigt over teammedlem** vises.</span><span class="sxs-lookup"><span data-stu-id="d9497-155">The **Team member summary** page appears.</span></span> <span data-ttu-id="d9497-156">Oplysningerne på denne side indeholder teammedlemmets fødselsdato, anciennitetsdato, antal år i tjeneste, år i den aktuelle stilling og kompensationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="d9497-156">The information on this page includes the team member's birth date, seniority date, years of service, years in his or her current position, and compensation information.</span></span>

## <a name="send-praise-about-team-members-by-using-the-my-team-mobile-workspace"></a><span data-ttu-id="d9497-157">Sende ros om teammedlemmer ved hjælp af arbejdsområdet Mit team til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="d9497-157">Send praise about team members by using the My team mobile workspace</span></span>
1.  <span data-ttu-id="d9497-158">I mobilappen skal du vælge mobilarbejdsområdet **Mit team**.</span><span class="sxs-lookup"><span data-stu-id="d9497-158">In the mobile app, select the **My team** workspace.</span></span> <span data-ttu-id="d9497-159">Der vises en oversigt over teammedlemmer.</span><span class="sxs-lookup"><span data-stu-id="d9497-159">A list of team members is shown.</span></span> <span data-ttu-id="d9497-160">Oversigten viser også hvert teammedlems titel og eventuelle direkte underordnede, som han eller hun har.</span><span class="sxs-lookup"><span data-stu-id="d9497-160">The list also shows each team member's title, and any direct reports that he or she has.</span></span>
1.  <span data-ttu-id="d9497-161">Vælg et teammedlem.</span><span class="sxs-lookup"><span data-stu-id="d9497-161">Select a team member.</span></span> <span data-ttu-id="d9497-162">Siden **Oversigt over teammedlem** vises.</span><span class="sxs-lookup"><span data-stu-id="d9497-162">The **Team member summary** page appears.</span></span>
1.  <span data-ttu-id="d9497-163">Vælg **Send ros**.</span><span class="sxs-lookup"><span data-stu-id="d9497-163">Select **Send praise**.</span></span> 
1. <span data-ttu-id="d9497-164">Angiv teksten til den ros, du vil sende.</span><span class="sxs-lookup"><span data-stu-id="d9497-164">Enter the text of the praise that you want to send.</span></span> 
1. <span data-ttu-id="d9497-165">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="d9497-165">Select **Done**.</span></span>
