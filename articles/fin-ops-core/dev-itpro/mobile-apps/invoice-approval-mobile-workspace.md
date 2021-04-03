---
title: Arbejdsområde for fakturagodkendelser på mobilenheder
description: Dette emne indeholder oplysninger om arbejdsområdet til fakturagodkendelse på mobilenheder.
author: abruer
manager: AnnBe
ms.date: 12/01/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: sericks
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.openlocfilehash: 3d90b89900b35bce648841aa9e49737a25309ce2
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5570064"
---
# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="25b1f-103">Arbejdsområde for fakturagodkendelser på mobilenheder</span><span class="sxs-lookup"><span data-stu-id="25b1f-103">Invoice approvals mobile workspace</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="25b1f-104">Dette emne indeholder oplysninger om arbejdsområdet til **Fakturagodkendelse** på mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="25b1f-104">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="25b1f-105">Arbejdsområdet indeholder en liste over fakturaer, der er tildelt til dig via arbejdsgangen for kreditorfakturahovedet.</span><span class="sxs-lookup"><span data-stu-id="25b1f-105">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="25b1f-106">Dette mobile arbejdsområde er beregnet til brug sammen med Finance and Operations-mobilappen.</span><span class="sxs-lookup"><span data-stu-id="25b1f-106">This mobile workspace is intended to be used with the Finance and Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="25b1f-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="25b1f-107">Overview</span></span>

<span data-ttu-id="25b1f-108">I arbejdsområdet **Fakturagodkendelser** til mobilenheder kan kreditormedarbejdere og -chefer få vist fakturaer, der er tildelt til dem som en del af arbejdsgangen for kreditorfakturahovedet.</span><span class="sxs-lookup"><span data-stu-id="25b1f-108">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="25b1f-109">Du kan få vist fakturaoplysninger og også linje- og distributionsoplysninger, så du kan træffe kvalificerede godkendelsesbeslutninger.</span><span class="sxs-lookup"><span data-stu-id="25b1f-109">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="25b1f-110">Fra arbejdsområdet kan du tage skridt til at flytte fakturaen gennem arbejdsgangsprocessen.</span><span class="sxs-lookup"><span data-stu-id="25b1f-110">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="25b1f-111">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="25b1f-111">Prerequisites</span></span>

<span data-ttu-id="25b1f-112">Før du kan bruge dette mobilarbejdsområde, skal følgende forudsætninger være opfyldt.</span><span class="sxs-lookup"><span data-stu-id="25b1f-112">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="25b1f-113">Forudsætning</span><span class="sxs-lookup"><span data-stu-id="25b1f-113">Prerequisite</span></span></th>
<th><span data-ttu-id="25b1f-114">Rolle</span><span class="sxs-lookup"><span data-stu-id="25b1f-114">Role</span></span></th>
<th><span data-ttu-id="25b1f-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="25b1f-115">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="25b1f-116">Microsoft Dynamics 365 Finance skal være installeret i organisationen.</span><span class="sxs-lookup"><span data-stu-id="25b1f-116">Microsoft Dynamics 365 Finance must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="25b1f-117">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="25b1f-117">System administrator</span></span></td>
<td><span data-ttu-id="25b1f-118">Se <a href="../deployment/deploy-demo-environment.md">Installere et demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="25b1f-118">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="25b1f-119">Mobilarbejdsområdet <strong>Fakturagodkendelser</strong> skal være publiceret.</span><span class="sxs-lookup"><span data-stu-id="25b1f-119">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="25b1f-120">Systemadministrator</span><span class="sxs-lookup"><span data-stu-id="25b1f-120">System administrator</span></span></td>
<td><span data-ttu-id="25b1f-121">Se <a href="publish-mobile-workspace.md">Publicere et arbejdsområde til mobilenheder</a>.</span><span class="sxs-lookup"><span data-stu-id="25b1f-121">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="25b1f-122">Downloade og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="25b1f-122">Download and install the mobile app</span></span>

<span data-ttu-id="25b1f-123">Sådan downloades og installeres Finance and Operations-mobilappen:</span><span class="sxs-lookup"><span data-stu-id="25b1f-123">Download and install the Finance and Operations mobile app:</span></span>

-   [<span data-ttu-id="25b1f-124">Til Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="25b1f-124">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="25b1f-125">Til iPhones</span><span class="sxs-lookup"><span data-stu-id="25b1f-125">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="25b1f-126">Log på mobilappen</span><span class="sxs-lookup"><span data-stu-id="25b1f-126">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="25b1f-127">Start appen på din mobilenhed.</span><span class="sxs-lookup"><span data-stu-id="25b1f-127">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="25b1f-128">Angiv din Microsoft Dynamics 365 URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="25b1f-128">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="25b1f-129">Første gang du logger på, bliver du bedt om at angive brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="25b1f-129">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="25b1f-130">Angiv dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="25b1f-130">Enter your credentials.</span></span>
4.  <span data-ttu-id="25b1f-131">Når du har logget på, vises de arbejdsområder, der er tilgængelige for din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="25b1f-131">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="25b1f-132">Bemærk, at hvis systemadministratoren publicerer et nyt arbejdsområde senere, skal du opdatere listen over arbejdsområder til mobilenheder.</span><span class="sxs-lookup"><span data-stu-id="25b1f-132">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="25b1f-133">[![Træk for at opdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="25b1f-133">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="25b1f-134">Godkend fakturaer ved hjælp af arbejdsområdet Fakturagodkendelser til mobilenheder</span><span class="sxs-lookup"><span data-stu-id="25b1f-134">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="25b1f-135">På din mobilenhed skal du vælge arbejdsområdet **Fakturagodkendelser**.</span><span class="sxs-lookup"><span data-stu-id="25b1f-135">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="25b1f-136">Vælg den faktura, der er tildelt til dig af arbejdsgangen for kreditorfakturahovedet.</span><span class="sxs-lookup"><span data-stu-id="25b1f-136">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="25b1f-137">På siden **Fakturadetaljer** skal du gennemse oplysningerne i fakturahovedet, f.eks. oplysninger om leverandør og dato.</span><span class="sxs-lookup"><span data-stu-id="25b1f-137">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="25b1f-138">Vælg en linje på fakturaen for at få vist mere detaljerede oplysninger om den i visningen **Detaljer om fakturalinje**.</span><span class="sxs-lookup"><span data-stu-id="25b1f-138">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="25b1f-139">Vælg **Fordelinger** i visningen **Detaljer om fakturalinje** for at se linjefordelingerne.</span><span class="sxs-lookup"><span data-stu-id="25b1f-139">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="25b1f-140">Her kan du se regnskabet for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="25b1f-140">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="25b1f-141">De oplysninger, der vises, omfatter de økonomiske dimensioner og hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="25b1f-141">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="25b1f-142">Vælg **Fordelinger** på siden **Fakturadetaljer** for at se alle fordelinger.</span><span class="sxs-lookup"><span data-stu-id="25b1f-142">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="25b1f-143">Her kan du se regnskabet for hele fakturaen.</span><span class="sxs-lookup"><span data-stu-id="25b1f-143">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="25b1f-144">De oplysninger, der vises, omfatter de økonomiske dimensioner og hovedkontiene.</span><span class="sxs-lookup"><span data-stu-id="25b1f-144">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="25b1f-145">Vælg **Vedhæftede filer** for at få vist noter eller filer, der er tilknyttet fakturaen.</span><span class="sxs-lookup"><span data-stu-id="25b1f-145">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="25b1f-146">På siden **Fakturadetaljer** skal du vælge den relevante handling i arbejdsgangen for at fuldføre valideringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="25b1f-146">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="25b1f-147">Vælg **Udført**.</span><span class="sxs-lookup"><span data-stu-id="25b1f-147">Select **Done**.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]