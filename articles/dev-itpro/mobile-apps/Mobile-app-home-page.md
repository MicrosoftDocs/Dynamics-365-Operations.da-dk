---
title: Mobilapp-startside
description: "I dette emne beskrives Microsoft Dynamics 365 for Unified Operations-mobilappen. Emnet indeholder links til ressourcer, der kan hjælpe dig med implementere appen i din organisation."
author: sericks007
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-platform
ms.technology: 
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.search.scope: Operations
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: sericks
ms.dyn365.ops.intro: Platform update 4
ms.search.validFrom: 2017-02-28
ms.translationtype: HT
ms.sourcegitcommit: 6e64337f19600b18320550d91c134949c33af7b0
ms.openlocfilehash: 233d91138b11905d971be90154da54e61bbe2919
ms.contentlocale: da-dk
ms.lasthandoff: 12/01/2017

---

# <a name="mobile-app-home-page"></a><span data-ttu-id="e167c-103">Mobilapp-startside</span><span class="sxs-lookup"><span data-stu-id="e167c-103">Mobile app home page</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="e167c-104">I dette emne beskrives Microsoft Dynamics 365 for Unified Operations-mobilappen. Emnet indeholder links til ressourcer, der kan hjælpe dig med implementere appen i din organisation.</span><span class="sxs-lookup"><span data-stu-id="e167c-104">This topic describes the Microsoft Dynamics 365 for Unified Operations mobile app and provides links to resources that can help you implement it in your organization.</span></span>

> [!NOTE]
> <span data-ttu-id="e167c-105">Mobilappen blev tidligere kaldt *Microsoft Dynamics 365 for Finance and Operations*.</span><span class="sxs-lookup"><span data-stu-id="e167c-105">The mobile app was previously named *Microsoft Dynamics 365 for Finance and Operations*.</span></span>

<a name="overview"></a><span data-ttu-id="e167c-106">Overblik</span><span class="sxs-lookup"><span data-stu-id="e167c-106">Overview</span></span>
--------

<span data-ttu-id="e167c-107">Med mobilappen kan organisationen gøre sine forretningsprocesser tilgængelige på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="e167c-107">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="e167c-108">Når din IT-administrator har aktiveret arbejdsområdet til mobilenheder for din organisation, kan brugerne logge på appen og straks begynde at køre forretningsprocesser fra deres mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="e167c-108">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="e167c-109">Mobilappen indeholder følgende funktioner, der kan hjælpe med at øge produktiviteten:</span><span class="sxs-lookup"><span data-stu-id="e167c-109">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="e167c-110">Brugerne kan få vist, redigere og bruge forretningsdata, selvom de har uregelmæssig netværksforbindelse, eller deres mobilenheder er helt offline.</span><span class="sxs-lookup"><span data-stu-id="e167c-110">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="e167c-111">Når en enhed genopretter en netværksforbindelse, synkroniseres offlinedata automatisk med Dynamics 365 for Finance and Operations, Enterprise edition eller Microsoft Dynamics 365 for Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="e167c-111">When a device reestablishes a network connection, offline data operations are automatically synchronized with Dynamics 365 for Finance and Operations, Enterprise edition, or Microsoft Dynamics 365 for Finance and Operations.</span></span>
- <span data-ttu-id="e167c-112">It-administratorer eller udviklere kan bygge og udgive arbejdsområder til mobilenheder, der er skræddersyet til deres organisation.</span><span class="sxs-lookup"><span data-stu-id="e167c-112">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="e167c-113">Appen bruger eksisterende kodeaktiver.</span><span class="sxs-lookup"><span data-stu-id="e167c-113">The app uses your existing code assets.</span></span> <span data-ttu-id="e167c-114">Derfor behøver du ikke igen at implementere dine valideringsprocedurer, forretningslogik eller sikkerhedskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="e167c-114">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="e167c-115">It-administratorer eller udviklere kan nemt designe arbejdsområder til mobilenheder ved hjælp af peg og klik-arbejdsområdedesigneren, der leveres med webklienten.</span><span class="sxs-lookup"><span data-stu-id="e167c-115">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="e167c-116">It-administratorer eller udviklere kan vælge at optimere offlinefunktionerne for arbejdsområder ved hjælp af udvidelsesstrukturen for forretningslogik.</span><span class="sxs-lookup"><span data-stu-id="e167c-116">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="e167c-117">Da data fortsat behandles, mens en enhed er offline, forbliver dine mobilscenarier omfattende og flydende, selvom enhederne ikke har konstant netværksforbindelse.</span><span class="sxs-lookup"><span data-stu-id="e167c-117">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="e167c-118">Elementer i mobilappen</span><span class="sxs-lookup"><span data-stu-id="e167c-118">Elements of the mobile app</span></span>
<span data-ttu-id="e167c-119">Navigation i mobilappen består af fire grundbegreber: dashboardet, arbejdsområder, sider og handlinger.</span><span class="sxs-lookup"><span data-stu-id="e167c-119">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="e167c-120">[![Begreber til navigation i mobilappen](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="e167c-120">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="e167c-121">Når du starter appen, kommer du til **dashboardet**.</span><span class="sxs-lookup"><span data-stu-id="e167c-121">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="e167c-122">I dashboardet kan du se en liste over de **arbejdsområder**, der er publiceret.</span><span class="sxs-lookup"><span data-stu-id="e167c-122">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="e167c-123">I hvert arbejdsområde kan du se en liste over **sider**, der er tilgængelige for det pågældende arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="e167c-123">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="e167c-124">Når du er på en side, kan du udføre flere handlinger.</span><span class="sxs-lookup"><span data-stu-id="e167c-124">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="e167c-125">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="e167c-125">Here are some examples:</span></span>

    - <span data-ttu-id="e167c-126">Se detaljerede data.</span><span class="sxs-lookup"><span data-stu-id="e167c-126">View detailed data.</span></span>
    - <span data-ttu-id="e167c-127">Navigere til andre sider for at se relaterede data, f.eks. oplysninger om enheder eller linjer.</span><span class="sxs-lookup"><span data-stu-id="e167c-127">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="e167c-128">Se en liste over **handlinger**, der er tilgængelige for den pågældende side.</span><span class="sxs-lookup"><span data-stu-id="e167c-128">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="e167c-129">Med handlinger kan du oprette eller redigere eksisterende data.</span><span class="sxs-lookup"><span data-stu-id="e167c-129">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="e167c-130">Implementeringsproces</span><span class="sxs-lookup"><span data-stu-id="e167c-130">Implementation process</span></span>
<span data-ttu-id="e167c-131">I følgende illustration vises processen til implementering af både arbejdsområder til mobilenheder, der leveres af Microsoft, og brugerdefinerede arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="e167c-131">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

![Implementeringsproces for mobilapps](./media/Mobile-implementation-process-5.png)

<span data-ttu-id="e167c-133">Tabellen nedenfor indeholder links til ressourcer, der kan hjælpe dig med at implementere både arbejdsområder til mobilenheder, der leveres af Microsoft, og brugerdefinerede arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="e167c-133">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="e167c-134">Tallene i den første kolonne svarer til de nummererede trin i ovenstående illustration.</span><span class="sxs-lookup"><span data-stu-id="e167c-134">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e167c-135">Trin</span><span class="sxs-lookup"><span data-stu-id="e167c-135">Step</span></span></th>
<th><span data-ttu-id="e167c-136">Rolle</span><span class="sxs-lookup"><span data-stu-id="e167c-136">Role</span></span></th>
<th><span data-ttu-id="e167c-137">Handling</span><span class="sxs-lookup"><span data-stu-id="e167c-137">Action</span></span></th>
<th><span data-ttu-id="e167c-138">Ressourcer, som du kan bruge til at fuldføre handlingen</span><span class="sxs-lookup"><span data-stu-id="e167c-138">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="e167c-139">1</span><span class="sxs-lookup"><span data-stu-id="e167c-139">1</span></span></td>
<td><span data-ttu-id="e167c-140">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="e167c-140">System administrator</span></span></td>
<td><span data-ttu-id="e167c-141">Implementer Finance and Operations i din organisation.</span><span class="sxs-lookup"><span data-stu-id="e167c-141">Implement Finance and Operations in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="e167c-142">Hvis du endnu ikke har installeret en version af Microsoft Dynamics 365, kan du se under <a href="../deployment/deploy-demo-environment.md">Installere et demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="e167c-142">If you haven't yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="e167c-143">Du kan se en liste over arbejdsområder til mobilenheder, der kan bruges, under <a href="mobile-workspaces-released.md">Arbejdsområde til mobilenheder, der er udgivet for nylig</a>.</span><span class="sxs-lookup"><span data-stu-id="e167c-143">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e167c-144">2</span><span class="sxs-lookup"><span data-stu-id="e167c-144">2</span></span></td>
<td><span data-ttu-id="e167c-145">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="e167c-145">System administrator</span></span></td>
<td><span data-ttu-id="e167c-146"><strong>Hvis du bruger Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Hent og installer KB'er, der gør det muligt at bruge de arbejdsområder til mobilenheder, der leveres af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e167c-146"><strong>If you're using Microsoft Dynamics 365 for Finance and Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="e167c-147">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="e167c-147">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="e167c-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Arbejdsområde til omkostningsstyring på mobilenheder</a></span><span class="sxs-lookup"><span data-stu-id="e167c-148"><a href="../../financials/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="e167c-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Disponibelt lager i mobilarbejdsområde</a></span><span class="sxs-lookup"><span data-stu-id="e167c-149"><a href="../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="e167c-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Arbejdsområder for salgsordrer på mobilenheder</a></span><span class="sxs-lookup"><span data-stu-id="e167c-150"><a href="../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="e167c-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobilarbejdsområde for kreditorsamarbejde</a></span><span class="sxs-lookup"><span data-stu-id="e167c-151"><a href="../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="e167c-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Projekttidsregistrering i arbejdsområde til mobile enheder</a></span><span class="sxs-lookup"><span data-stu-id="e167c-152"><a href="../../financials/project-management/project-time-entry-mobile-workspace.md">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="e167c-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Arbejdsområde til udgiftsstyring på mobilenhed</a></span><span class="sxs-lookup"><span data-stu-id="e167c-153"><a href="../../financials/expense-management/expense-management-mobile-workspace.md">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e167c-154">3</span><span class="sxs-lookup"><span data-stu-id="e167c-154">3</span></span></td>
<td><span data-ttu-id="e167c-155">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="e167c-155">System administrator</span></span></td>
<td><span data-ttu-id="e167c-156">Publicer de arbejdsområder til mobilenheder, der leveres af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="e167c-156">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="e167c-157"><a href="publish-mobile-workspace.md">Publicer et arbejdsområde til mobilenheder</a>
</span><span class="sxs-lookup"><span data-stu-id="e167c-157"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e167c-158">4</span><span class="sxs-lookup"><span data-stu-id="e167c-158">4</span></span></td>
<td><span data-ttu-id="e167c-159">Udvikler eller uafhængig softwareleverandører (ISV)</span><span class="sxs-lookup"><span data-stu-id="e167c-159">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="e167c-160">Du kan bruge mobilplatformen til at oprette brugerdefinerede arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="e167c-160">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="e167c-161"><a href="platform/mobile-platform-home-page.md">Mobilplatform</a></span><span class="sxs-lookup"><span data-stu-id="e167c-161"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e167c-162">5</span><span class="sxs-lookup"><span data-stu-id="e167c-162">5</span></span></td>
<td><span data-ttu-id="e167c-163">ISV (Independent Software Vendor)</span><span class="sxs-lookup"><span data-stu-id="e167c-163">ISV</span></span></td>
<td><span data-ttu-id="e167c-164">Opret en pakke, der kan installeres, og som indeholder brugerdefinerede arbejdsområder til mobilenheder, og overfør pakken til Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="e167c-164">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="e167c-165"><a href="../deployment/create-apply-deployable-package.md">Opret en installerbar pakke</a></span><span class="sxs-lookup"><span data-stu-id="e167c-165"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e167c-166">6</span><span class="sxs-lookup"><span data-stu-id="e167c-166">6</span></span></td>
<td><span data-ttu-id="e167c-167">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="e167c-167">System administrator</span></span></td>
<td><span data-ttu-id="e167c-168">Anvend den installerbare pakke, der indeholder de brugerdefinerede arbejdsområder, der er leveret af den uafhængige softwareleverandør.</span><span class="sxs-lookup"><span data-stu-id="e167c-168">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="e167c-169"><a href="../deployment/apply-deployable-package-system.md">Anvend en installerbar pakke</a></span><span class="sxs-lookup"><span data-stu-id="e167c-169"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e167c-170">7</span><span class="sxs-lookup"><span data-stu-id="e167c-170">7</span></span></td>
<td><span data-ttu-id="e167c-171">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="e167c-171">System administrator</span></span></td>
<td><span data-ttu-id="e167c-172">Publicer de brugerdefinerede arbejdsområder til mobilenheder, der er leveret af ISV'en.</span><span class="sxs-lookup"><span data-stu-id="e167c-172">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="e167c-173"><a href="publish-mobile-workspace.md">Publicer et arbejdsområde til mobile enheder</a></span><span class="sxs-lookup"><span data-stu-id="e167c-173"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="e167c-174">8</span><span class="sxs-lookup"><span data-stu-id="e167c-174">8</span></span></td>
<td><span data-ttu-id="e167c-175">Bruger</span><span class="sxs-lookup"><span data-stu-id="e167c-175">User</span></span></td>
<td><span data-ttu-id="e167c-176">Download og installer mobilappen.</span><span class="sxs-lookup"><span data-stu-id="e167c-176">Download and install the mobile app.</span></span></td>
<td><ul>
<li><span data-ttu-id="e167c-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">Til Android-telefoner</a></span><span class="sxs-lookup"><span data-stu-id="e167c-177"><a href="https://go.microsoft.com/fwlink/?linkid=850662">For Android phones</a></span></span></li>
<li><span data-ttu-id="e167c-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">Til iPhones</a></span><span class="sxs-lookup"><span data-stu-id="e167c-178"><a href="https://go.microsoft.com/fwlink/?linkid=850663">For iPhones</a></span></span></li></ul>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="e167c-179">9</span><span class="sxs-lookup"><span data-stu-id="e167c-179">9</span></span></td>
<td><span data-ttu-id="e167c-180">Bruger</span><span class="sxs-lookup"><span data-stu-id="e167c-180">User</span></span></td>
<td><span data-ttu-id="e167c-181">Log på og brug mobilappen.</span><span class="sxs-lookup"><span data-stu-id="e167c-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="e167c-182">Appen indeholder de arbejdsområder til mobilenheder, der er udgivet af systemadministratoren.</span><span class="sxs-lookup"><span data-stu-id="e167c-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="e167c-183">Du kan se en liste over arbejdsområder til mobilenheder, der leveres af Microsoft, under <a href="mobile-workspaces-released.md">Arbejdsområde til mobilenheder, der er udgivet for nylig</a>.</span><span class="sxs-lookup"><span data-stu-id="e167c-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

