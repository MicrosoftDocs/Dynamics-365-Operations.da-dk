---
title: Arbejdsområdet Godkendelse af indkøbsordre til mobilenheder
description: Dette emne indeholder oplysninger om arbejdsområdet Godkendelse af indkøbsordre til mobilenheder, hvor du får vist indkøbsordrer og reagere på dem med handlinger. Du kan f.eks. godkende eller afvise en indkøbsordre.
author: kamaybac
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PurchVendorPortalRequests
audience: Application User
ms.reviewer: kamaybac
ms.custom: 30211
ms.search.region: Global
ms.author: dabourq
ms.search.validFrom: 2016-11-30
ms.dyn365.ops.version: Version 1611
ms.openlocfilehash: 19ddd9eb34d5e5248f782aafc9ac9dee1b38dadb
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5825344"
---
# <a name="purchase-order-approval-mobile-workspace"></a><span data-ttu-id="b5585-104">Arbejdsområdet Godkendelse af indkøbsordre til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="b5585-104">Purchase order approval mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="b5585-105">Dette emne indeholder oplysninger om arbejdsområdet **Godkendelse af indkøbsordre** på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="b5585-105">This topic provides information about the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="b5585-106">I dette arbejdsområde kan du få vist indkøbsordrer og reagere på dem med handlinger.</span><span class="sxs-lookup"><span data-stu-id="b5585-106">This workspace lets you view purchase orders and respond to them through actions.</span></span> <span data-ttu-id="b5585-107">Du kan f.eks. godkende eller afvise en indkøbsordre.</span><span class="sxs-lookup"><span data-stu-id="b5585-107">For example, you can approve or reject a purchase order.</span></span>
 
## <a name="overview"></a><span data-ttu-id="b5585-108">Overblik</span><span class="sxs-lookup"><span data-stu-id="b5585-108">Overview</span></span> 
<span data-ttu-id="b5585-109">Indkøbsordrer, der kræver godkendelse, går gennem en godkendelsesarbejdsgang.</span><span class="sxs-lookup"><span data-stu-id="b5585-109">Purchase orders that requires approval go through an approval workflow.</span></span> <span data-ttu-id="b5585-110">Arbejdsgangen kan indeholde forskellige trin, der kræver handling af en eller flere personer.</span><span class="sxs-lookup"><span data-stu-id="b5585-110">The workflow can include various steps that require that one or more people take action.</span></span> <span data-ttu-id="b5585-111">Én person kan f.eks. skulle fuldføre en opgave eller godkende indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="b5585-111">For example, a person might have to complete a task or approve the purchase order.</span></span> 

<span data-ttu-id="b5585-112">I arbejdsområdet **Godkendelse af indkøbsordre** til mobilenheder kan du nemt få vist og reagere på indkøbsordrer fra din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="b5585-112">The **Purchase order approval** mobile workspace lets you easily view and respond to purchase orders from your mobile device.</span></span> <span data-ttu-id="b5585-113">I dette arbejdsområde kan du også udføre de samme arbejdsgangshandlinger, som du kan udføre fra webklienten.</span><span class="sxs-lookup"><span data-stu-id="b5585-113">This workspace also lets you take the same workflow actions that you can take from the web client.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="b5585-114">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="b5585-114">Prerequisites</span></span>
<span data-ttu-id="b5585-115">Forudsætningerne varierer alt efter, hvilken version af Supply Chain Management der er installeret i din organisation.</span><span class="sxs-lookup"><span data-stu-id="b5585-115">The prerequisites vary, depending on the version of Supply Chain Management that has been deployed for your organization.</span></span>

### <a name="prerequisites-if-you-use-supply-chain-management"></a><span data-ttu-id="b5585-116">Forudsætninger, hvis du bruger Supply Chain Management</span><span class="sxs-lookup"><span data-stu-id="b5585-116">Prerequisites if you use Supply Chain Management</span></span> 
<span data-ttu-id="b5585-117">Hvis Supply Chain Management er implementeret for din organisation, skal systemadministratoren publicere mobilarbejdsområdet **Godkendelse af indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="b5585-117">If Supply Chain Management has been deployed for your organization, the system administrator must publish the **Purchase order approval** mobile workspace.</span></span> <span data-ttu-id="b5585-118">Du kan finde flere oplysninger under [Publicere et arbejdsområde til mobilenheder](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span><span class="sxs-lookup"><span data-stu-id="b5585-118">For instructions, see [Publish a mobile workspace](../../dev-itpro/mobile-apps/publish-mobile-workspace.md).</span></span>

### <a name="prerequisites-if-you-use-microsoft-dynamics-365-for-operations-version-1611-with-platform-update-3-or-later"></a><span data-ttu-id="b5585-119">Forudsætninger, hvis du bruger Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere</span><span class="sxs-lookup"><span data-stu-id="b5585-119">Prerequisites if you use Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later</span></span>
<span data-ttu-id="b5585-120">Hvis Microsoft Dynamics 365 for Operations version 1611 med platformsopdatering 3 eller nyere er implementeret for organisationen, skal systemadministratoren opfylde følgende forudsætninger.</span><span class="sxs-lookup"><span data-stu-id="b5585-120">If Microsoft Dynamics 365 for Operations version 1611 with Platform update 3 or later has been deployed for your organization, the system administrator must complete the following prerequisites.</span></span> 

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="b5585-121">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="b5585-121">Prerequisite</span></span></th>
<th><span data-ttu-id="b5585-122">Rolle</span><span class="sxs-lookup"><span data-stu-id="b5585-122">Role</span></span></th>
<th><span data-ttu-id="b5585-123">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b5585-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="b5585-124">Implementer KB 4017918.</span><span class="sxs-lookup"><span data-stu-id="b5585-124">Implement KB 4017918.</span></span></td>
<td><span data-ttu-id="b5585-125">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="b5585-125">System administrator</span></span></td>
<td><span data-ttu-id="b5585-126">KB 4017918 er et X ++ opdatering eller metadatahotfix, der indeholder arbejdsområdet <strong>Godkendelse af indkøbsordre</strong> til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="b5585-126">KB 4017918 is an X++ update or metadata hotfix that contains the <strong>Purchase order approval</strong> mobile workspace.</span></span> <span data-ttu-id="b5585-127">For at implementere KB 4017918 skal systemadministratoren gøre følgende.</span><span class="sxs-lookup"><span data-stu-id="b5585-127">To implement KB 4017918, your system administrator must follow these steps.</span></span>
<ol>
<li><span data-ttu-id="b5585-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Hente metadata-hotfixet fra Microsoft Dynamics Lifecycle Services (LCS)</a>.</span><span class="sxs-lookup"><span data-stu-id="b5585-128"><a href="../../dev-itpro/migration-upgrade/download-hotfix-lcs.md">Download the metadata hotfix from Microsoft Dynamics Lifecycle Services (LCS)</a>.</span></span></li>
<li><span data-ttu-id="b5585-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Installere metadatahotfixet</a>.</span><span class="sxs-lookup"><span data-stu-id="b5585-129"><a href="../../dev-itpro/migration-upgrade/install-metadata-hotfix-package.md">Install the metadata hotfix</a>.</span></span></li>
<li><span data-ttu-id="b5585-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Opret en installerbar pakke</a>, der indeholder <strong>SCMMobile</strong>-modellen, og overfør derefter den installerbare pakke til LCS.</span><span class="sxs-lookup"><span data-stu-id="b5585-130"><a href="../../dev-itpro/deployment/create-apply-deployable-package.md">Create a deployable package</a> that contains the <strong>SCMMobile</strong> model, and then upload the deployable package to LCS.</span></span></li>
<li><span data-ttu-id="b5585-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Anvend den installerbare pakke</a></span><span class="sxs-lookup"><span data-stu-id="b5585-131"><a href="../../dev-itpro/deployment/apply-deployable-package-system.md">Apply the deployable package</a>.</span></span></li>
</ol></td>
</tr>
<tr class="even">
<td><span data-ttu-id="b5585-132">Publicer arbejdsområdet <strong>Godkendelse af indkøbsordre</strong> til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="b5585-132">Publish the <strong>Purchase order approval</strong> mobile workspace.</span></span></td>
<td><span data-ttu-id="b5585-133">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="b5585-133">System administrator</span></span></td>
<td><span data-ttu-id="b5585-134">Se <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</span><span class="sxs-lookup"><span data-stu-id="b5585-134">See <a href="../../dev-itpro/mobile-apps/publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="b5585-135">Downloade og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="b5585-135">Download and install the mobile app</span></span>
<span data-ttu-id="b5585-136">Sådan downloades og installeres Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="b5585-136">Download and install the Finance and Operations mobile app:</span></span>

- [<span data-ttu-id="b5585-137">Til Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="b5585-137">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
- [<span data-ttu-id="b5585-138">Til iPhones</span><span class="sxs-lookup"><span data-stu-id="b5585-138">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)


## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="b5585-139">Log på mobilappen</span><span class="sxs-lookup"><span data-stu-id="b5585-139">Sign in to the mobile app</span></span>

1. <span data-ttu-id="b5585-140">Start appen på din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="b5585-140">Start the app on your mobile device.</span></span>
2. <span data-ttu-id="b5585-141">Angiv din Microsoft Dynamics 365 URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="b5585-141">Enter your Microsoft Dynamics 365 URL.</span></span>
3. <span data-ttu-id="b5585-142">Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="b5585-142">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="b5585-143">Angiv dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="b5585-143">Enter your credentials.</span></span>
4. <span data-ttu-id="b5585-144">Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="b5585-144">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="b5585-145">Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="b5585-145">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

![Arbejdsområdet Godkendelse af indkøbsordre på listen over tilgængelige arbejdsområder](./media/po-workspaces.png)

## <a name="view-orders-that-are-assigned-to-you"></a><span data-ttu-id="b5585-147">Få vist ordrer, der er tildelt dig</span><span class="sxs-lookup"><span data-stu-id="b5585-147">View orders that are assigned to you</span></span>
1. <span data-ttu-id="b5585-148">På din mobilenhed skal du vælge arbejdsområdet **Godkendelse af indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="b5585-148">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="b5585-149">Vælg **Ordrer, der er tildelt til mig** for at få vist alle de indkøbsordrer, hvor du er blevet bedt om at udføre en handling i arbejdsgangen til godkendelse af indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="b5585-149">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="b5585-150">Vælg en ordre.</span><span class="sxs-lookup"><span data-stu-id="b5585-150">Select an order.</span></span> <span data-ttu-id="b5585-151">På siden **Ordredetaljer** kan du se ordrehovedets oplysninger og linjer.</span><span class="sxs-lookup"><span data-stu-id="b5585-151">On the **Order details** page, you will see the order header information and lines.</span></span> <span data-ttu-id="b5585-152">Du kan også finde retningslinjer fra til opgaven i arbejdsgangen.</span><span class="sxs-lookup"><span data-stu-id="b5585-152">You can also find guidelines from the workflow task.</span></span>
4. <span data-ttu-id="b5585-153">Vælg **Regnskabsfordelinger** for at åbne siden **Overskrift regnskabsfordeling**.</span><span class="sxs-lookup"><span data-stu-id="b5585-153">Select **Accounting distributions** to open the **Header accounting distributions** page.</span></span>
5. <span data-ttu-id="b5585-154">Gå tilbage til siden **Ordredetaljer**, og vælg en linje.</span><span class="sxs-lookup"><span data-stu-id="b5585-154">Return to the **Order details** page, and select a line.</span></span> <span data-ttu-id="b5585-155">Du kan også udforske linjespecifikke regnskabsfordelinger fra ordrelinjeoplysningerne.</span><span class="sxs-lookup"><span data-stu-id="b5585-155">From the order line details, you can also explore the line-specific accounting distributions.</span></span>

## <a name="complete-an-action-on-the-purchase-order"></a><span data-ttu-id="b5585-156">Udføre en handling i indkøbsordren</span><span class="sxs-lookup"><span data-stu-id="b5585-156">Complete an action on the purchase order</span></span>
<span data-ttu-id="b5585-157">Når du har set den indkøbsordre, der er tildelt til dig, og har læst instruktionerne for arbejdsgangen, er du klar til at udføre en handling.</span><span class="sxs-lookup"><span data-stu-id="b5585-157">After you've viewed the purchase order that is assigned to you and read the workflow instructions, you should be ready to take action.</span></span>

1. <span data-ttu-id="b5585-158">På din mobilenhed skal du vælge arbejdsområdet **Godkendelse af indkøbsordre**.</span><span class="sxs-lookup"><span data-stu-id="b5585-158">On your mobile device, select the **Purchase order approval** workspace.</span></span>
2. <span data-ttu-id="b5585-159">Vælg **Ordrer, der er tildelt til mig** for at få vist alle de indkøbsordrer, hvor du er blevet bedt om at udføre en handling i arbejdsgangen til godkendelse af indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="b5585-159">Select **Orders assigned to me** to view all the purchase orders for which you've been asked to take action in the purchase order approval workflow.</span></span>
3. <span data-ttu-id="b5585-160">Vælg en ordre, og se på detaljesiden.</span><span class="sxs-lookup"><span data-stu-id="b5585-160">Select an order, and view the details page.</span></span>
4. <span data-ttu-id="b5585-161">Vælg **Handlinger** for at få vist de tilgængelige handlinger.</span><span class="sxs-lookup"><span data-stu-id="b5585-161">Select **Actions** to show the available actions.</span></span> <span data-ttu-id="b5585-162">Hvilke handlinger der er tilgængelige afhænger af den opgave, der er tildelt til dig.</span><span class="sxs-lookup"><span data-stu-id="b5585-162">The actions that are available depend on the task that has been assigned to you.</span></span>

    | <span data-ttu-id="b5585-163">Opgavehandling</span><span class="sxs-lookup"><span data-stu-id="b5585-163">Task action</span></span>    | <span data-ttu-id="b5585-164">Godkendelseshandling</span><span class="sxs-lookup"><span data-stu-id="b5585-164">Approval action</span></span>  |
    |----------------|------------------|
    | <span data-ttu-id="b5585-165">Komplet</span><span class="sxs-lookup"><span data-stu-id="b5585-165">Complete</span></span>       | <span data-ttu-id="b5585-166">Godkend</span><span class="sxs-lookup"><span data-stu-id="b5585-166">Approve</span></span>          |
    | <span data-ttu-id="b5585-167">Returner</span><span class="sxs-lookup"><span data-stu-id="b5585-167">Return</span></span>         | <span data-ttu-id="b5585-168">Afvis</span><span class="sxs-lookup"><span data-stu-id="b5585-168">Reject</span></span>           |
    | <span data-ttu-id="b5585-169">Anmod om ændring</span><span class="sxs-lookup"><span data-stu-id="b5585-169">Request change</span></span> | <span data-ttu-id="b5585-170">Anmod om ændring</span><span class="sxs-lookup"><span data-stu-id="b5585-170">Request change</span></span>   |
    | <span data-ttu-id="b5585-171">Stedfortræder</span><span class="sxs-lookup"><span data-stu-id="b5585-171">Delegate</span></span>       | <span data-ttu-id="b5585-172">Stedfortræder</span><span class="sxs-lookup"><span data-stu-id="b5585-172">Delegate</span></span>         |

5. <span data-ttu-id="b5585-173">Vælg den relevante handling.</span><span class="sxs-lookup"><span data-stu-id="b5585-173">Select the appropriate action.</span></span>
6. <span data-ttu-id="b5585-174">På siden **Fuldfør opgave** skal du angive en kommentar.</span><span class="sxs-lookup"><span data-stu-id="b5585-174">On the **Complete task** page, enter a comment.</span></span> <span data-ttu-id="b5585-175">Bemærk, at hvis du vælger handlingen **Deleger**, skal du vælge en bruger, du vil delegere opgaven til.</span><span class="sxs-lookup"><span data-stu-id="b5585-175">Note that if you select the **Delegate** action, you must select a user to delegate the task to.</span></span>
7. <span data-ttu-id="b5585-176">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="b5585-176">Select **Done**.</span></span> <span data-ttu-id="b5585-177">Når du har opdateret arbejdsområdet, er indkøbsordren ikke længere på listen.</span><span class="sxs-lookup"><span data-stu-id="b5585-177">After you refresh your workspace, the purchase order will no longer be in your list.</span></span> 


[!INCLUDE[footer-include](../../includes/footer-banner.md)]