---
title: Projekttidsregistrering i arbejdsområde til mobile enheder
description: Dette emne indeholder oplysninger om arbejdsområdet til projekttidsregistrering på mobilenheder. I dette arbejdsområde kan brugerne angive og gemme tider for et projekt ved hjælp af deres mobilenhed.
author: KimANelson
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: 272101
ms.assetid: 4505f021-b9bb-4b87-be24-6bf0bd88ee60
ms.search.region: Global
ms.search.industry: Service industries
ms.author: knelson
ms.dyn365.ops.version: Version 1611
ms.search.validFrom: 2016-11-30
ms.openlocfilehash: ee11f7f392676adb59bd25f6549737482faf5fdb
ms.sourcegitcommit: 2460d0da812c45fce67a061386db52e0ae46b0f3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/30/2019
ms.locfileid: "2250363"
---
# <a name="project-time-entry-mobile-workspace"></a><span data-ttu-id="03479-104">Projekttidsregistrering i arbejdsområde til mobile enheder</span><span class="sxs-lookup"><span data-stu-id="03479-104">Project time entry mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="03479-105">Dette emne indeholder oplysninger om arbejdsområdet **Tidsregistrering for projekt** på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="03479-105">This topic provides information about the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="03479-106">I dette arbejdsområde kan brugerne angive og gemme tider for et projekt ved hjælp af deres mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="03479-106">This workspace lets users enter and save time against a project by using their mobile device.</span></span>

<span data-ttu-id="03479-107">Dette arbejdsområde til mobilenheder er beregnet til brug med Dynamics 365 for Unified Operations Mobile-appen.</span><span class="sxs-lookup"><span data-stu-id="03479-107">This mobile workspace is intended to be used with the Dynamics 365 Unified Ops mobile app.</span></span> 

## <a name="overview"></a><span data-ttu-id="03479-108">Overblik</span><span class="sxs-lookup"><span data-stu-id="03479-108">Overview</span></span>
<span data-ttu-id="03479-109">Som led i deres daglige arbejde er projektressourcer ofte ude på et sted eller på rejse.</span><span class="sxs-lookup"><span data-stu-id="03479-109">As part of their daily work, project resources are often on-site or traveling.</span></span> <span data-ttu-id="03479-110">I arbejdsområdet **Projekttidsregistrering** til mobilenheder kan brugerne angive deres fakturerbare eller ikke-fakturerbar tid på et projekt på en mobilenhed efter eget valg.</span><span class="sxs-lookup"><span data-stu-id="03479-110">The **Project time entry** mobile workspace lets users enter their billable or non-billable time against a project on the mobile device of their choice.</span></span> <span data-ttu-id="03479-111">Derfor kan projektressourcer foretage tidsregistreringer når som helst og hvor som helst.</span><span class="sxs-lookup"><span data-stu-id="03479-111">Therefore, project resources can record time entries anytime and anywhere.</span></span> <span data-ttu-id="03479-112">De kan også få vist tidsregistreringer, der allerede er registreret.</span><span class="sxs-lookup"><span data-stu-id="03479-112">They can also view time entries that have already been recorded.</span></span> 

<span data-ttu-id="03479-113">Specifikt i mobilarbejdsområdet **Tidsregistrering for projekt** kan brugerne kan udføre disse opgaver:</span><span class="sxs-lookup"><span data-stu-id="03479-113">Specifically, in the **Project time entry** mobile workspace, users can perform these tasks:</span></span>

-   <span data-ttu-id="03479-114">Angiv det antal timer, du har brugt på en bestemt opgave, for den valgte dato.</span><span class="sxs-lookup"><span data-stu-id="03479-114">For any selected date, enter the number of hours that you spent on a specific task.</span></span>
-   <span data-ttu-id="03479-115">Søg på projektnavn eller kunde for at finde det projekt, du vil registrere tiden for.</span><span class="sxs-lookup"><span data-stu-id="03479-115">Search by project name or customer to find the project to enter time for.</span></span>
-   <span data-ttu-id="03479-116">Angiv kategori og aktivitet for den tid, du har brugt.</span><span class="sxs-lookup"><span data-stu-id="03479-116">Specify the category and activity for the time that you spent.</span></span>
-   <span data-ttu-id="03479-117">Registrer tiden som fakturerbar eller ikke-fakturerbar for projektet.</span><span class="sxs-lookup"><span data-stu-id="03479-117">Record the time as billable or non-billable for the project.</span></span>
-   <span data-ttu-id="03479-118">Angiv eventuelt eksterne eller interne bemærkninger.</span><span class="sxs-lookup"><span data-stu-id="03479-118">Optionally enter any external or internal comments.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="03479-119">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="03479-119">Prerequisites</span></span>
<span data-ttu-id="03479-120">Forudsætningerne er forskellige, afhængigt af hvilken version af Microsoft Dynamics 365 der er installeret i organisationen.</span><span class="sxs-lookup"><span data-stu-id="03479-120">The prerequisites differ, based on the version of Microsoft Dynamics 365 that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-dynamics-365-finance"></a><span data-ttu-id="03479-121">Forudsætninger, hvis du bruger Dynamics 365 Finance</span><span class="sxs-lookup"><span data-stu-id="03479-121">Prerequisites if you use Dynamics 365 Finance</span></span>
<span data-ttu-id="03479-122">Hvis Finance er implementeret for organisationen, skal systemadministratoren publicere mobilarbejdsområdet **Tidsregistrering for projekt**.</span><span class="sxs-lookup"><span data-stu-id="03479-122">If Finance has been deployed for your organization, the system administrator must publish the **Project time entry** mobile workspace.</span></span> <span data-ttu-id="03479-123">Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="03479-123">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="03479-124">Forudsætninger, hvis du bruger version 1611 med Platform update 3 eller nyere</span><span class="sxs-lookup"><span data-stu-id="03479-124">Prerequisites if you use version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="03479-125">Hvis version 1611 med Platform update 3 eller nyere er implementeret for organisationen, skal systemadministratoren opfylde følgende forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="03479-125">If version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="03479-126">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="03479-126">Prerequisite</span></span></th>
<th><span data-ttu-id="03479-127">Rolle</span><span class="sxs-lookup"><span data-stu-id="03479-127">Role</span></span></th>
<th><span data-ttu-id="03479-128">Betegnelse</span><span class="sxs-lookup"><span data-stu-id="03479-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">

<td><span data-ttu-id="03479-129">Implementere KB 4018050.</span><span class="sxs-lookup"><span data-stu-id="03479-129">Implement KB 4018050.</span></span></td>
<td><span data-ttu-id="03479-130">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="03479-130">System administrator</span></span></td>
<td><span data-ttu-id="03479-131">KB 4018050 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Projekttidsregistrering</strong> til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="03479-131">KB 4018050 is an X++ update or metadata hotfix that contains the <strong>Project time entry</strong> mobile workspace.</span></span> <span data-ttu-id="03479-132">For at implementere KB 4018050 skal systemadministratoren gøre følgende.</span><span class="sxs-lookup"><span data-stu-id="03479-132">To implement KB 4018050, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="03479-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Hente metadata-hotfixet fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="03479-133"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="03479-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installere metadatahotfixet</a>.</span><span class="sxs-lookup"><span data-stu-id="03479-134"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="03479-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opret en installerbar pakke</a>, der indeholder <strong>ApplicationSuite</strong>- og <strong>ProjectMobile</strong>-modellerne, og overfør derefter den installerbare pakke til LCS.</span><span class="sxs-lookup"><span data-stu-id="03479-135"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>ApplicationSuite</strong> and <strong>ProjectMobile</strong> models, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="03479-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Anvend den installerbare pakke</a></span><span class="sxs-lookup"><span data-stu-id="03479-136"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>

</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="03479-137">Publicer arbejdsområdet <strong>Tidsregistrering for projekt</strong> til mobile enheder.</span><span class="sxs-lookup"><span data-stu-id="03479-137">Publish the <strong>Project time entry</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="03479-138">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="03479-138">System administrator</span></span></td>
<td><span data-ttu-id="03479-139">Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</span><span class="sxs-lookup"><span data-stu-id="03479-139">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="03479-140">Downloade og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="03479-140">Download and install the mobile app</span></span>

<span data-ttu-id="03479-141">Download og installer Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="03479-141">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="03479-142">Til Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="03479-142">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="03479-143">Til iPhones</span><span class="sxs-lookup"><span data-stu-id="03479-143">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="03479-144">Log på mobilappen</span><span class="sxs-lookup"><span data-stu-id="03479-144">Sign in to the mobile app</span></span>
1.  <span data-ttu-id="03479-145">Start appen på din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="03479-145">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="03479-146">Angiv URL-adressen til din Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="03479-146">Enter your Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="03479-147">Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="03479-147">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="03479-148">Angiv dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="03479-148">Enter your credentials.</span></span>
4.  <span data-ttu-id="03479-149">Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="03479-149">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="03479-150">Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="03479-150">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

<span data-ttu-id="03479-151">[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="03479-151">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="enter-time-by-using-the-project-time-entry-mobile-workspace"></a><span data-ttu-id="03479-152">Angiv tid ved hjælp af arbejdsområdet Projekttidsregistrering til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="03479-152">Enter time by using the Project time entry mobile workspace</span></span>
1.  <span data-ttu-id="03479-153">På din mobilenhed skal du vælge arbejdsområdet **Projekttidsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="03479-153">On your mobile device, select the **Project time entry** workspace.</span></span>
2.  <span data-ttu-id="03479-154">Vælg **Tidsregistrering**.</span><span class="sxs-lookup"><span data-stu-id="03479-154">Select **Time entry**.</span></span> <span data-ttu-id="03479-155">Kalenderdatoerne for den aktuelle uge vises.</span><span class="sxs-lookup"><span data-stu-id="03479-155">The calendar dates for the current week are shown.</span></span>
3.  <span data-ttu-id="03479-156">Vælg **Handlinger** &gt; **Ny registrering** for en valgt dato.</span><span class="sxs-lookup"><span data-stu-id="03479-156">For a selected date, select **Actions** &gt; **New entry**.</span></span>
4.  <span data-ttu-id="03479-157">Angiv antallet af timer, der skal registreres.</span><span class="sxs-lookup"><span data-stu-id="03479-157">Enter the number of hours to record.</span></span>
5.  <span data-ttu-id="03479-158">Vælg projektet for tidsregistreringen.</span><span class="sxs-lookup"><span data-stu-id="03479-158">Select the project for the time entry.</span></span> <span data-ttu-id="03479-159">Der vises en liste over de projekter, der er indlæst i din app til offlinebrug.</span><span class="sxs-lookup"><span data-stu-id="03479-159">A list shows the projects that are loaded into your app for offline use.</span></span> <span data-ttu-id="03479-160">50 varer er indlæst som standard, men en udvikler kan ændre dette tal.</span><span class="sxs-lookup"><span data-stu-id="03479-160">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="03479-161">Du kan finde flere oplysninger under [Mobilplatform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="03479-161">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
6.  <span data-ttu-id="03479-162">Vælg **Søg**, hvis projektet ikke er på listen.</span><span class="sxs-lookup"><span data-stu-id="03479-162">If your project isn't in the list, select **Search**.</span></span> <span data-ttu-id="03479-163">Søg på navn, eller skift for at søge på projektnavn eller kunde.</span><span class="sxs-lookup"><span data-stu-id="03479-163">Search by name, or switch to search by project name or customer.</span></span>
7.  <span data-ttu-id="03479-164">Vælg en kategori.</span><span class="sxs-lookup"><span data-stu-id="03479-164">Select a category.</span></span> <span data-ttu-id="03479-165">Der vises en liste over de kategorier, der er indlæst i din app til offlinebrug.</span><span class="sxs-lookup"><span data-stu-id="03479-165">A list shows the categories that are loaded into your app for offline use.</span></span> <span data-ttu-id="03479-166">50 varer er indlæst som standard, men en udvikler kan ændre dette tal.</span><span class="sxs-lookup"><span data-stu-id="03479-166">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="03479-167">Du kan finde flere oplysninger under [Mobilplatform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="03479-167">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
8.  <span data-ttu-id="03479-168">Vælg **Søg**, hvis kategorien ikke er på listen.</span><span class="sxs-lookup"><span data-stu-id="03479-168">If your category isn't in the list, select **Search**.</span></span> <span data-ttu-id="03479-169">Søg på kategori, eller skift for at søge på kategorinavn.</span><span class="sxs-lookup"><span data-stu-id="03479-169">Search by category, or switch to search by category name.</span></span>
9.  <span data-ttu-id="03479-170">Vælg en aktivitet.</span><span class="sxs-lookup"><span data-stu-id="03479-170">Select an activity.</span></span> <span data-ttu-id="03479-171">Der vises en liste over de aktiviteter, der er indlæst i din app til offlinebrug.</span><span class="sxs-lookup"><span data-stu-id="03479-171">A list shows the activities that are loaded into your app for offline use.</span></span> <span data-ttu-id="03479-172">50 varer er indlæst som standard, men en udvikler kan ændre dette tal.</span><span class="sxs-lookup"><span data-stu-id="03479-172">By default, 50 items are loaded, but a developer can change this number.</span></span> <span data-ttu-id="03479-173">Du kan finde flere oplysninger under [Mobilplatform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span><span class="sxs-lookup"><span data-stu-id="03479-173">For more information, see [Mobile platform](../../dev-itpro/mobile-apps/platform/mobile-platform-home-page.md).</span></span>
10. <span data-ttu-id="03479-174">Vælg **Søg**, hvis aktiviteten ikke er på listen.</span><span class="sxs-lookup"><span data-stu-id="03479-174">If your activity isn't in the list, select **Search**.</span></span> <span data-ttu-id="03479-175">Søg på aktivitetsnummer, eller skift for at søge på formål.</span><span class="sxs-lookup"><span data-stu-id="03479-175">Search by activity number, or switch to search by purpose.</span></span>

11. <span data-ttu-id="03479-176">Vælg linjeegenskaben.</span><span class="sxs-lookup"><span data-stu-id="03479-176">Select the line property.</span></span>
12. <span data-ttu-id="03479-177">Valgfrit: Angiv eventuelt eksterne og interne bemærkninger.</span><span class="sxs-lookup"><span data-stu-id="03479-177">Optional: Enter any external and internal comments.</span></span>
13. <span data-ttu-id="03479-178">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="03479-178">Select **Done**.</span></span>
