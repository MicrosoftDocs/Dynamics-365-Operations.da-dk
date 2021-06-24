---
title: Mobilapp-startside
description: I dette emne beskrives Finance and Operations-mobilappen (Dynamics 365). Emnet indeholder links til ressourcer, der kan hjælpe dig med implementere appen i din organisation.
author: ChrisGarty
ms.date: 01/22/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User, Developer, IT Pro
ms.reviewer: sericks
ms.custom: 272853
ms.assetid: c99f818f-27b3-4e45-92b4-74272dad0e17
ms.search.region: Global
ms.author: cgarty
ms.dyn365.ops.version: Platform update 4
ms.search.validFrom: 2017-02-28
ms.openlocfilehash: 469b03151f3113f44d932a2d6f4bf3fcfa059133
ms.sourcegitcommit: ff09736563d3cd2bc74c7664edd1767b218401cb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/04/2021
ms.locfileid: "6188404"
---
# <a name="mobile-app-home-page"></a><span data-ttu-id="33de3-103">Mobilapp-startside</span><span class="sxs-lookup"><span data-stu-id="33de3-103">Mobile app home page</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="33de3-104">I dette emne beskrives **Finance and Operations-mobilappen (Dynamics 365)**. Emnet indeholder links til ressourcer, der kan hjælpe dig med implementere appen i din organisation.</span><span class="sxs-lookup"><span data-stu-id="33de3-104">This topic describes the **Finance and Operations (Dynamics 365)** mobile app and provides links to resources that can help you implement it in your organization.</span></span>

## <a name="overview"></a><span data-ttu-id="33de3-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="33de3-105">Overview</span></span>

<span data-ttu-id="33de3-106">Med mobilappen kan organisationen gøre sine forretningsprocesser tilgængelige på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="33de3-106">The mobile app enables your organization to make its business processes available on mobile devices.</span></span> <span data-ttu-id="33de3-107">Når din IT-administrator har aktiveret arbejdsområdet til mobilenheder for din organisation, kan brugerne logge på appen og straks begynde at køre forretningsprocesser fra deres mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="33de3-107">After your IT admin enables the mobile workspaces for your organization, users can sign in to the app and immediately begin to run business processes from their mobile devices.</span></span> <span data-ttu-id="33de3-108">Mobilappen indeholder følgende funktioner, der kan hjælpe med at øge produktiviteten:</span><span class="sxs-lookup"><span data-stu-id="33de3-108">The mobile app includes the following features that can help increase productivity:</span></span>

- <span data-ttu-id="33de3-109">Brugerne kan få vist, redigere og bruge forretningsdata, selvom de har uregelmæssig netværksforbindelse, eller deres mobilenheder er helt offline.</span><span class="sxs-lookup"><span data-stu-id="33de3-109">Users can view, edit, and act on business data, even if they have intermittent network connectivity or their mobile devices are completely offline.</span></span> <span data-ttu-id="33de3-110">Når en enhed genopretter en netværksforbindelse, synkroniseres offlinedatahandlinger automatisk.</span><span class="sxs-lookup"><span data-stu-id="33de3-110">When a device reestablishes a network connection, offline data operations are automatically synchronized.</span></span>
- <span data-ttu-id="33de3-111">It-administratorer eller udviklere kan bygge og udgive arbejdsområder til mobilenheder, der er skræddersyet til deres organisation.</span><span class="sxs-lookup"><span data-stu-id="33de3-111">IT admins or developers can build and publish mobile workspaces that have been tailored to their organization.</span></span> <span data-ttu-id="33de3-112">Appen bruger eksisterende kodeaktiver.</span><span class="sxs-lookup"><span data-stu-id="33de3-112">The app uses your existing code assets.</span></span> <span data-ttu-id="33de3-113">Derfor behøver du ikke igen at implementere dine valideringsprocedurer, forretningslogik eller sikkerhedskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="33de3-113">Therefore, you don't have to re-implement your validation procedures, business logic, or security configuration.</span></span>
- <span data-ttu-id="33de3-114">It-administratorer eller udviklere kan nemt designe arbejdsområder til mobilenheder ved hjælp af peg og klik-arbejdsområdedesigneren, der leveres med webklienten.</span><span class="sxs-lookup"><span data-stu-id="33de3-114">IT admins or developers can easily design mobile workspaces by using the point-and-click workspace designer that is included with the web client.</span></span>
- <span data-ttu-id="33de3-115">It-administratorer eller udviklere kan vælge at optimere offlinefunktionerne for arbejdsområder ved hjælp af udvidelsesstrukturen for forretningslogik.</span><span class="sxs-lookup"><span data-stu-id="33de3-115">IT admins or developers can optionally optimize the offline capabilities of workspaces by using the Business logic extensibility framework.</span></span> <span data-ttu-id="33de3-116">Da data fortsat behandles, mens en enhed er offline, forbliver dine mobilscenarier omfattende og flydende, selvom enhederne ikke har konstant netværksforbindelse.</span><span class="sxs-lookup"><span data-stu-id="33de3-116">Because data continues to be processed while a device is offline, your mobile scenarios remain rich and fluid, even if devices don't have constant network connectivity.</span></span>

## <a name="elements-of-the-mobile-app"></a><span data-ttu-id="33de3-117">Elementer i mobilappen</span><span class="sxs-lookup"><span data-stu-id="33de3-117">Elements of the mobile app</span></span>
<span data-ttu-id="33de3-118">Navigation i mobilappen består af fire grundbegreber: dashboardet, arbejdsområder, sider og handlinger.</span><span class="sxs-lookup"><span data-stu-id="33de3-118">Navigation in the mobile app consists of four basic concepts: the dashboard, workspaces, pages, and actions.</span></span> 

<span data-ttu-id="33de3-119">[![Begreber til navigation i mobilappen](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span><span class="sxs-lookup"><span data-stu-id="33de3-119">[![Navigation concepts in the mobile app](./media/mobilephoneapp1-1024x536.png)](./media/mobilephoneapp1.png)</span></span>

1. <span data-ttu-id="33de3-120">Når du starter appen, kommer du til **dashboardet**.</span><span class="sxs-lookup"><span data-stu-id="33de3-120">When you start the app, you go to the **dashboard**.</span></span>
2. <span data-ttu-id="33de3-121">I dashboardet kan du se en liste over de **arbejdsområder**, der er publiceret.</span><span class="sxs-lookup"><span data-stu-id="33de3-121">On the dashboard, you can see a list of **workspaces** that have been published.</span></span>
3. <span data-ttu-id="33de3-122">I hvert arbejdsområde kan du se en liste over **sider**, der er tilgængelige for det pågældende arbejdsområde.</span><span class="sxs-lookup"><span data-stu-id="33de3-122">In each workspace, you can see a list of **pages** that are available for that workspace.</span></span>
4. <span data-ttu-id="33de3-123">Når du er på en side, kan du udføre flere handlinger.</span><span class="sxs-lookup"><span data-stu-id="33de3-123">After you're on a page, you can perform several actions.</span></span> <span data-ttu-id="33de3-124">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="33de3-124">Here are some examples:</span></span>

    - <span data-ttu-id="33de3-125">Se detaljerede data.</span><span class="sxs-lookup"><span data-stu-id="33de3-125">View detailed data.</span></span>
    - <span data-ttu-id="33de3-126">Navigere til andre sider for at se relaterede data, f.eks. oplysninger om enheder eller linjer.</span><span class="sxs-lookup"><span data-stu-id="33de3-126">Navigate to other pages for related data, such as entity details or lines.</span></span>
    - <span data-ttu-id="33de3-127">Se en liste over **handlinger**, der er tilgængelige for den pågældende side.</span><span class="sxs-lookup"><span data-stu-id="33de3-127">See a list of **actions** that are available for that page.</span></span> <span data-ttu-id="33de3-128">Med handlinger kan du oprette eller redigere eksisterende data.</span><span class="sxs-lookup"><span data-stu-id="33de3-128">Actions let you create or edit existing data.</span></span>

## <a name="implementation-process"></a><span data-ttu-id="33de3-129">Implementeringsproces</span><span class="sxs-lookup"><span data-stu-id="33de3-129">Implementation process</span></span>
<span data-ttu-id="33de3-130">I følgende illustration vises processen til implementering af både arbejdsområder til mobilenheder, der leveres af Microsoft, og brugerdefinerede arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="33de3-130">The following illustration shows the process for implementing both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> 

<span data-ttu-id="33de3-131">[![Implementeringsproces for mobilapps](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span><span class="sxs-lookup"><span data-stu-id="33de3-131">[![Mobile apps implementation process](./media/Mobile-implementation-process-5.png)](./media/Mobile-implementation-process-5.png)</span></span>

<span data-ttu-id="33de3-132">Tabellen nedenfor indeholder links til ressourcer, der kan hjælpe dig med at implementere både arbejdsområder til mobilenheder, der leveres af Microsoft, og brugerdefinerede arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="33de3-132">The following table includes links to resources that can help you implement both mobile workspaces that are provided by Microsoft and custom mobile workspaces.</span></span> <span data-ttu-id="33de3-133">Tallene i den første kolonne svarer til de nummererede trin i ovenstående illustration.</span><span class="sxs-lookup"><span data-stu-id="33de3-133">The numbers in the first column correspond to the numbered steps in the previous illustration.</span></span>

<table>
<colgroup>
<col width="25%" />
<col width="25%" />
<col width="25%" />
<col width="25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="33de3-134">Trin</span><span class="sxs-lookup"><span data-stu-id="33de3-134">Step</span></span></th>
<th><span data-ttu-id="33de3-135">Rolle</span><span class="sxs-lookup"><span data-stu-id="33de3-135">Role</span></span></th>
<th><span data-ttu-id="33de3-136">Handling</span><span class="sxs-lookup"><span data-stu-id="33de3-136">Action</span></span></th>
<th><span data-ttu-id="33de3-137">Ressourcer, som du kan bruge til at fuldføre handlingen</span><span class="sxs-lookup"><span data-stu-id="33de3-137">Resources to help you complete the action</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="33de3-138">1</span><span class="sxs-lookup"><span data-stu-id="33de3-138">1</span></span></td>
<td><span data-ttu-id="33de3-139">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="33de3-139">System administrator</span></span></td>
<td><span data-ttu-id="33de3-140">Implementer Finance and Operations-appen i organisationen.</span><span class="sxs-lookup"><span data-stu-id="33de3-140">Implement the Finance and Operations app in your organization.</span></span></td>
<td><ul><li><span data-ttu-id="33de3-141">Hvis du endnu ikke har installeret en version af Microsoft Dynamics 365, kan du se under <a href="../deployment/deploy-demo-environment.md">Installere et demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="33de3-141">If you haven&#39;t yet deployed a version of Microsoft Dynamics 365, see <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span></li><li><span data-ttu-id="33de3-142">Du kan se en liste over arbejdsområder til mobilenheder, der kan bruges, under <a href="mobile-workspaces-released.md">Arbejdsområde til mobilenheder, der er udgivet for nylig</a>.</span><span class="sxs-lookup"><span data-stu-id="33de3-142">To see a list of mobile workspaces that can be used, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span></li></ul></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33de3-143">2</span><span class="sxs-lookup"><span data-stu-id="33de3-143">2</span></span></td>
<td><span data-ttu-id="33de3-144">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="33de3-144">System administrator</span></span></td>
<td><span data-ttu-id="33de3-145"><strong>Hvis du bruger Microsoft Dynamics 365 for Operations version 1611:</strong> Hent og installer KB'er om de arbejdsområder til mobilenheder, der leveres af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="33de3-145"><strong>If you&#39;re using Microsoft Dynamics 365 for Operations version 1611:</strong> Download and install KBs that enable the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="33de3-146">Du kan finde flere oplysninger under følgende emner:</span><span class="sxs-lookup"><span data-stu-id="33de3-146">See the following topics for more information:</span></span>
<ul>

<li><span data-ttu-id="33de3-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Arbejdsområde til omkostningsstyring på mobilenheder</a></span><span class="sxs-lookup"><span data-stu-id="33de3-147"><a href="../../../finance/cost-accounting/cost-controlling-mobile-workspace.md">Cost controlling mobile workspaces</a></span></span></li>
<li><span data-ttu-id="33de3-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Disponibelt lager i mobilarbejdsområde</a></span><span class="sxs-lookup"><span data-stu-id="33de3-148"><a href="../../../supply-chain/inventory/inventory-on-hand-mobile-workspace.md">Inventory on-hand mobile workspace</a></span></span></li>
<li><span data-ttu-id="33de3-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Arbejdsområder for salgsordrer på mobilenheder</a></span><span class="sxs-lookup"><span data-stu-id="33de3-149"><a href="../../../supply-chain/sales-marketing/sales-orders-mobile-workspace.md">Sales orders mobile workspaces</a></span></span></li>
<li><span data-ttu-id="33de3-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Mobilarbejdsområde for kreditorsamarbejde</a></span><span class="sxs-lookup"><span data-stu-id="33de3-150"><a href="../../../supply-chain/procurement/vendor-collaboration-mobile-workspace.md">Vendor collaboration mobile workspace</a></span></span></li>
<li><span data-ttu-id="33de3-151"><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Projekttidsregistrering i arbejdsområde til mobile enheder</a></span><span class="sxs-lookup"><span data-stu-id="33de3-151"><a href="/dynamics365/project-operations/prod-pma/project-time-entry-mobile-workspace">Project time entry mobile workspace</a></span></span></li>
<li><span data-ttu-id="33de3-152"><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Arbejdsområde til udgiftsstyring på mobilenhed</a></span><span class="sxs-lookup"><span data-stu-id="33de3-152"><a href="/dynamics365/project-operations/prod-exp/expense-management-mobile-workspace">Expense management mobile workspace</a></span></span></li>

</ul></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33de3-153">3</span><span class="sxs-lookup"><span data-stu-id="33de3-153">3</span></span></td>
<td><span data-ttu-id="33de3-154">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="33de3-154">System administrator</span></span></td>
<td><span data-ttu-id="33de3-155">Publicer de arbejdsområder til mobilenheder, der leveres af Microsoft.</span><span class="sxs-lookup"><span data-stu-id="33de3-155">Publish the mobile workspaces that are provided by Microsoft.</span></span></td>
<td><span data-ttu-id="33de3-156"><a href="publish-mobile-workspace.md">Publicer et arbejdsområde til mobilenheder</a>
</span><span class="sxs-lookup"><span data-stu-id="33de3-156"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a>
</span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33de3-157">4</span><span class="sxs-lookup"><span data-stu-id="33de3-157">4</span></span></td>
<td><span data-ttu-id="33de3-158">Udvikler eller uafhængig softwareleverandører (ISV)</span><span class="sxs-lookup"><span data-stu-id="33de3-158">Developer or independent software vendor (ISV)</span></span></td>
<td><span data-ttu-id="33de3-159">Du kan bruge mobilplatformen til at oprette brugerdefinerede arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="33de3-159">Use the mobile platform to create custom mobile workspaces.</span></span></td>
<td><span data-ttu-id="33de3-160"><a href="platform/mobile-platform-home-page.md">Mobilplatform</a></span><span class="sxs-lookup"><span data-stu-id="33de3-160"><a href="platform/mobile-platform-home-page.md">Mobile platform</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33de3-161">5</span><span class="sxs-lookup"><span data-stu-id="33de3-161">5</span></span></td>
<td><span data-ttu-id="33de3-162">ISV (Independent Software Vendor)</span><span class="sxs-lookup"><span data-stu-id="33de3-162">ISV</span></span></td>
<td><span data-ttu-id="33de3-163">Opret en pakke, der kan installeres, og som indeholder brugerdefinerede arbejdsområder til mobilenheder, og overfør pakken til Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="33de3-163">Create a deployable package that contains custom mobile workspaces, and upload the package to Microsoft Dynamics Lifecycle Services (LCS).</span></span></td>
<td><span data-ttu-id="33de3-164"><a href="../deployment/create-apply-deployable-package.md">Oprette en installerbar pakke</a></span><span class="sxs-lookup"><span data-stu-id="33de3-164"><a href="../deployment/create-apply-deployable-package.md">Create a deployable package</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33de3-165">6</span><span class="sxs-lookup"><span data-stu-id="33de3-165">6</span></span></td>
<td><span data-ttu-id="33de3-166">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="33de3-166">System administrator</span></span></td>
<td><span data-ttu-id="33de3-167">Anvend den installerbare pakke, der indeholder de brugerdefinerede arbejdsområder, der er leveret af den uafhængige softwareleverandør.</span><span class="sxs-lookup"><span data-stu-id="33de3-167">Apply the deployable package that contains the custom workspaces that are provided by the independent software vendor (ISV).</span></span></td>
<td><span data-ttu-id="33de3-168"><a href="../deployment/apply-deployable-package-system.md">Anvend en installerbar pakke</a></span><span class="sxs-lookup"><span data-stu-id="33de3-168"><a href="../deployment/apply-deployable-package-system.md">Apply a deployable package</a></span></span></td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33de3-169">7</span><span class="sxs-lookup"><span data-stu-id="33de3-169">7</span></span></td>
<td><span data-ttu-id="33de3-170">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="33de3-170">System administrator</span></span></td>
<td><span data-ttu-id="33de3-171">Publicer de brugerdefinerede arbejdsområder til mobilenheder, der er leveret af ISV'en.</span><span class="sxs-lookup"><span data-stu-id="33de3-171">Publish the custom mobile workspaces that are provided by the ISV.</span></span></td>
<td><span data-ttu-id="33de3-172"><a href="publish-mobile-workspace.md">Publicere et arbejdsområde til mobile enheder</a></span><span class="sxs-lookup"><span data-stu-id="33de3-172"><a href="publish-mobile-workspace.md">Publish a mobile workspace</a></span></span></td>
</tr>
<tr class="even">
<td><span data-ttu-id="33de3-173">8</span><span class="sxs-lookup"><span data-stu-id="33de3-173">8</span></span></td>
<td><span data-ttu-id="33de3-174">Bruger</span><span class="sxs-lookup"><span data-stu-id="33de3-174">User</span></span></td>
<td><span data-ttu-id="33de3-175">Download og installer mobilappen.</span><span class="sxs-lookup"><span data-stu-id="33de3-175">Download and install the mobile app.</span></span></td>
<td><span data-ttu-id="33de3-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations-app til Android</a></span><span class="sxs-lookup"><span data-stu-id="33de3-176">
<a href="https://go.microsoft.com/fwlink/?linkid=850662">Finance and Operations app for Android</a></span></span><BR/><span data-ttu-id="33de3-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations-app til iOS</a></span><span class="sxs-lookup"><span data-stu-id="33de3-177">
<a href="https://go.microsoft.com/fwlink/?linkid=850663">Finance and Operations app for iOS</a></span></span><BR/>
<span data-ttu-id="33de3-178">(Windows Phone understøttes ikke)</span><span class="sxs-lookup"><span data-stu-id="33de3-178">(Windows Phone unsupported)</span></span>
</td>
</tr>
<tr class="odd">
<td><span data-ttu-id="33de3-179">9</span><span class="sxs-lookup"><span data-stu-id="33de3-179">9</span></span></td>
<td><span data-ttu-id="33de3-180">Bruger</span><span class="sxs-lookup"><span data-stu-id="33de3-180">User</span></span></td>
<td><span data-ttu-id="33de3-181">Log på og brug mobilappen.</span><span class="sxs-lookup"><span data-stu-id="33de3-181">Sign in, and use the mobile app.</span></span> <span data-ttu-id="33de3-182">Appen indeholder de arbejdsområder til mobilenheder, der er udgivet af systemadministratoren.</span><span class="sxs-lookup"><span data-stu-id="33de3-182">The app includes the mobile workspaces that have been published by the system administrator.</span></span></td>
<td><span data-ttu-id="33de3-183">Du kan se en liste over arbejdsområder til mobilenheder, der leveres af Microsoft, under <a href="mobile-workspaces-released.md">Arbejdsområde til mobilenheder, der er udgivet for nylig</a>.</span><span class="sxs-lookup"><span data-stu-id="33de3-183">To see a list of mobile workspaces that are provided by Microsoft, see <a href="mobile-workspaces-released.md">Mobile workspaces recently released</a>.</span></span>
</td>
</tr>
</tbody>
</table>

## <a name="troubleshooting"></a><span data-ttu-id="33de3-184">Fejlfinding</span><span class="sxs-lookup"><span data-stu-id="33de3-184">Troubleshooting</span></span>
[<span data-ttu-id="33de3-185">Ressourcer til mobilplatform</span><span class="sxs-lookup"><span data-stu-id="33de3-185">Mobile platform resources</span></span>](platform/mobile-platform-home-page.md#troubleshooting-the-app)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]