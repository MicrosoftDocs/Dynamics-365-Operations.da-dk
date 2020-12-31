---
title: Arbejdsområde for fakturagodkendelser på mobilenheder
description: Dette emne indeholder oplysninger om arbejdsområdet til fakturagodkendelse på mobilenheder. Arbejdsområdet indeholder en liste over fakturaer, der er tildelt til dig via arbejdsgangen for kreditorfakturahovedet.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 8d4b40c7ce8939248e85b6b6f3d359bd16e35b0d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4683402"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="cf052-104">Arbejdsområde for fakturagodkendelser på mobilenheder</span><span class="sxs-lookup"><span data-stu-id="cf052-104">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="cf052-105">Dette emne indeholder oplysninger om arbejdsområdet til **Fakturagodkendelse** på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="cf052-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="cf052-106">Arbejdsområdet indeholder en liste over fakturaer, der er tildelt til dig via arbejdsgangen for kreditorfakturahovedet.</span><span class="sxs-lookup"><span data-stu-id="cf052-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="cf052-107">Dette mobile arbejdsområde er beregnet til brug sammen med Finance and Operations-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="cf052-107">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="cf052-108">Overblik</span><span class="sxs-lookup"><span data-stu-id="cf052-108">Overview</span></span>

<span data-ttu-id="cf052-109">I arbejdsområdet **Fakturagodkendelser** til mobilenheder kan kreditormedarbejdere og -chefer få vist fakturaer, der er tildelt til dem som en del af arbejdsgangen for kreditorfakturahovedet.</span><span class="sxs-lookup"><span data-stu-id="cf052-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="cf052-110">Du kan få vist fakturaoplysninger og også linje- og distributionsoplysninger, så du kan træffe kvalificerede godkendelsesbeslutninger.</span><span class="sxs-lookup"><span data-stu-id="cf052-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="cf052-111">Fra arbejdsområdet kan du tage skridt til at flytte fakturaen gennem arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="cf052-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="cf052-112">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="cf052-112">Prerequisites</span></span>

<span data-ttu-id="cf052-113">Før du kan bruge dette mobilarbejdsområde, skal følgende forudsætninger være opfyldt.</span><span class="sxs-lookup"><span data-stu-id="cf052-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="cf052-114">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="cf052-114">Prerequisite</span></span></th>
<th><span data-ttu-id="cf052-115">Rolle</span><span class="sxs-lookup"><span data-stu-id="cf052-115">Role</span></span></th>
<th><span data-ttu-id="cf052-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cf052-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="cf052-117">Microsoft Dynamics 365 Finance skal være installeret i organisationen.</span><span class="sxs-lookup"><span data-stu-id="cf052-117">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="cf052-118">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="cf052-118">System administrator</span></span></td>
<td><span data-ttu-id="cf052-119">Se <a href="../deployment/deploy-demo-environment.md">Installere et demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="cf052-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="cf052-120">Mobilarbejdsområdet <strong>Fakturagodkendelser</strong> skal være publiceret.</span><span class="sxs-lookup"><span data-stu-id="cf052-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="cf052-121">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="cf052-121">System administrator</span></span></td>
<td><span data-ttu-id="cf052-122">Se <a href="publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</span><span class="sxs-lookup"><span data-stu-id="cf052-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="cf052-123">Downloade og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="cf052-123">Download and install the mobile app</span></span>

<span data-ttu-id="cf052-124">Sådan downloades og installeres Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="cf052-124">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="cf052-125">Til Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="cf052-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="cf052-126">Til iPhones</span><span class="sxs-lookup"><span data-stu-id="cf052-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="cf052-127">Log på mobilappen</span><span class="sxs-lookup"><span data-stu-id="cf052-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="cf052-128">Start appen på din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="cf052-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="cf052-129">Angiv din Microsoft Dynamics 365 URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="cf052-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="cf052-130">Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="cf052-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="cf052-131">Angiv dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="cf052-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="cf052-132">Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="cf052-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="cf052-133">Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="cf052-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="cf052-134">[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="cf052-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="cf052-135">Godkend fakturaer ved hjælp af arbejdsområdet Fakturagodkendelser til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="cf052-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="cf052-136">På din mobilenhed skal du vælge arbejdsområdet **Fakturagodkendelser**.</span><span class="sxs-lookup"><span data-stu-id="cf052-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="cf052-137">Vælg den faktura, der er tildelt til dig af arbejdsgangen for kreditorfakturahovedet.</span><span class="sxs-lookup"><span data-stu-id="cf052-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="cf052-138">På siden **Fakturadetaljer** skal du gennemse oplysningerne i fakturahovedet, f.eks. oplysninger om leverandør og dato.</span><span class="sxs-lookup"><span data-stu-id="cf052-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="cf052-139">Vælg en linje på fakturaen for at få vist mere detaljerede oplysninger om den i visningen **Detaljer om fakturalinje**.</span><span class="sxs-lookup"><span data-stu-id="cf052-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="cf052-140">Vælg **Fordelinger** i visningen **Detaljer om fakturalinje** for at se linjefordelingerne.</span><span class="sxs-lookup"><span data-stu-id="cf052-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="cf052-141">Her kan du se regnskabet for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="cf052-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="cf052-142">De oplysninger, der vises, omfatter de økonomiske dimensioner og hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="cf052-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="cf052-143">Vælg **Fordelinger** på siden **Fakturadetaljer** for at se alle fordelinger.</span><span class="sxs-lookup"><span data-stu-id="cf052-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="cf052-144">Her kan du se regnskabet for hele fakturaen.</span><span class="sxs-lookup"><span data-stu-id="cf052-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="cf052-145">De oplysninger, der vises, omfatter de økonomiske dimensioner og hovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="cf052-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="cf052-146">Vælg **Vedhæftede filer** for at få vist noter eller filer, der er tilknyttet fakturaen.</span><span class="sxs-lookup"><span data-stu-id="cf052-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="cf052-147">På siden **Fakturadetaljer** skal du vælge den relevante handling i arbejdsgangen for at fuldføre valideringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="cf052-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="cf052-148">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="cf052-148">Select **Done**.</span></span>
