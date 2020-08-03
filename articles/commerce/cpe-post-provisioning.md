---
title: Konfigurere et Dynamics 365 Commerce-evalueringsmiljø
description: I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at det er blevet klargjort.
author: psimolin
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6a1ae960f0f530104af7bdea9a8fcb78b01571f5
ms.sourcegitcommit: 5175e3fae432016246244cf70fe05465f43de88c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 07/17/2020
ms.locfileid: "3599718"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="03731-103">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="03731-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="03731-104">I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at det er blevet klargjort.</span><span class="sxs-lookup"><span data-stu-id="03731-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="03731-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="03731-105">Overview</span></span>

<span data-ttu-id="03731-106">Fuldfør kun procedurerne i dette emne, efter dit Commerce-evalueringsmiljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="03731-106">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="03731-107">For yderligere oplysninger om, hvordan du klargør dit Commerce-evalueringsmiljø se [Klargøre et Commerce-evalueringsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="03731-107">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="03731-108">Når dit Commerce-evalueringsmiljø er blevet klargjort fra ende til anden, skal yderligere konfigurationstrin efter klargøring fuldføres, før du kan begynde at evaluere miljøet.</span><span class="sxs-lookup"><span data-stu-id="03731-108">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="03731-109">Hvis du vil fuldføre disse trin, skal du bruge Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="03731-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="03731-110">Før du begynder</span><span class="sxs-lookup"><span data-stu-id="03731-110">Before you start</span></span>

1. <span data-ttu-id="03731-111">Log på [LCS-portalen](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="03731-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="03731-112">Gå til dit projekt.</span><span class="sxs-lookup"><span data-stu-id="03731-112">Go to your project.</span></span>
1. <span data-ttu-id="03731-113">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="03731-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="03731-114">Vælg dit miljø fra listen.</span><span class="sxs-lookup"><span data-stu-id="03731-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="03731-115">Vælg **Log på miljø** i miljøoplysningerne til højre.</span><span class="sxs-lookup"><span data-stu-id="03731-115">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="03731-116">Du bliver sendt til Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="03731-116">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="03731-117">Kontrollér, at den juridiske enhed **USRT** er valgt i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="03731-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="03731-118">Under klargøring af aktiviteter i Commerce-hovedkontoret skal du kontrollere, at den juridiske enhed **USRT** altid er markeret.</span><span class="sxs-lookup"><span data-stu-id="03731-118">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="03731-119">Konfigurer POS </span><span class="sxs-lookup"><span data-stu-id="03731-119">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="03731-120">Tilknyt en arbejder til din identitet</span><span class="sxs-lookup"><span data-stu-id="03731-120">Associate a worker with your identity</span></span>

<span data-ttu-id="03731-121">Hvis du vil knytte en arbejder til din identitet, skal du følge disse trin i Commerce-hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="03731-121">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="03731-122">Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Medarbejdere \> Arbejdere**.</span><span class="sxs-lookup"><span data-stu-id="03731-122">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="03731-123">Find og vælg følgende post i listen: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="03731-123">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="03731-124">Klik på **Commerce** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="03731-124">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="03731-125">Vælg **Tilknyt eksisterende identitet**.</span><span class="sxs-lookup"><span data-stu-id="03731-125">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="03731-126">Skriv din mailadresse i feltet **E-mail** til højre for **Søg ved hjælp af e-mail**.</span><span class="sxs-lookup"><span data-stu-id="03731-126">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="03731-127">Vælg **Søg**.</span><span class="sxs-lookup"><span data-stu-id="03731-127">Select **Search**.</span></span>
1. <span data-ttu-id="03731-128">Vælg posten med dit navn.</span><span class="sxs-lookup"><span data-stu-id="03731-128">Select the record that has your name.</span></span>
1. <span data-ttu-id="03731-129">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="03731-129">Select **OK**.</span></span>
1. <span data-ttu-id="03731-130">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="03731-130">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="03731-131">Aktiverere sky POS</span><span class="sxs-lookup"><span data-stu-id="03731-131">Activate Cloud POS</span></span>

<span data-ttu-id="03731-132">Følg disse trin for at aktivere skybaseret POS.</span><span class="sxs-lookup"><span data-stu-id="03731-132">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="03731-133">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="03731-133">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="03731-134">Vælg dit miljø fra listen.</span><span class="sxs-lookup"><span data-stu-id="03731-134">Select your environment in the list.</span></span>
1. <span data-ttu-id="03731-135">Vælg **Log på skybaseret POS** i miljøoplysningerne til højre.</span><span class="sxs-lookup"><span data-stu-id="03731-135">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="03731-136">Vælg **Næste** for at åbne dialogboksen **Før du begynder**.</span><span class="sxs-lookup"><span data-stu-id="03731-136">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="03731-137">Lad feltet **Server-URL-adresse** være, som det er.</span><span class="sxs-lookup"><span data-stu-id="03731-137">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="03731-138">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="03731-138">Select **Next**.</span></span>
1. <span data-ttu-id="03731-139">Log på ved hjælp af din Microsoft Azure Active Directory (Azure AD)-konto.</span><span class="sxs-lookup"><span data-stu-id="03731-139">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="03731-140">Under **Butiksnavn** skal du vælge **San Francisco** og derefter vælge **Næste**.</span><span class="sxs-lookup"><span data-stu-id="03731-140">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="03731-141">Under **Kasseapparat og enhed** skal du vælge **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="03731-141">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="03731-142">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="03731-142">Select **Activate**.</span></span> <span data-ttu-id="03731-143">Du er logget ud og dirigeret til POS-login-siden.</span><span class="sxs-lookup"><span data-stu-id="03731-143">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="03731-144">Du kan nu logge på den skybaserede POS-oplevelse ved hjælp af operatør-ID **000713** og adgangskoden **123**.</span><span class="sxs-lookup"><span data-stu-id="03731-144">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="03731-145">Konfigurer dit websted i Commerce</span><span class="sxs-lookup"><span data-stu-id="03731-145">Set up your site in Commerce</span></span>

<span data-ttu-id="03731-146">Følg disse trin for at begynde at konfigurere dit evalueringswebsted i Commerce.</span><span class="sxs-lookup"><span data-stu-id="03731-146">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="03731-147">Log på Site Builder ved hjælp af den URL-adresse, som du noterede ned, da du initialiserede e-Commerce i forbindelse med klargøring (jf. [Initialiser e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="03731-147">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="03731-148">Vælg webstedet **Fabrikam** for at åbne dialogboksen webstedsopsætning.</span><span class="sxs-lookup"><span data-stu-id="03731-148">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="03731-149">Vælg det domæne, du angav, da du initialiserede e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="03731-149">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="03731-150">Som standardkanal skal du vælge **Udvidet Fabrikam-onlinebutik**.</span><span class="sxs-lookup"><span data-stu-id="03731-150">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="03731-151">(Sørg for at vælge den **udvidede** onlinebutik.)</span><span class="sxs-lookup"><span data-stu-id="03731-151">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="03731-152">Vælg **da-dk** som standardsprog.</span><span class="sxs-lookup"><span data-stu-id="03731-152">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="03731-153">Lad værdien i feltet **Sti** være, som den er.</span><span class="sxs-lookup"><span data-stu-id="03731-153">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="03731-154">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="03731-154">Select **OK**.</span></span> <span data-ttu-id="03731-155">Listen over sider på webstedet vises.</span><span class="sxs-lookup"><span data-stu-id="03731-155">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="03731-156">Aktivere job</span><span class="sxs-lookup"><span data-stu-id="03731-156">Enable jobs</span></span>

<span data-ttu-id="03731-157">Følg disse trin for at aktivere job i Commerce.</span><span class="sxs-lookup"><span data-stu-id="03731-157">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="03731-158">Log på miljøet (hovedkontor).</span><span class="sxs-lookup"><span data-stu-id="03731-158">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="03731-159">Brug menuen til venstre for at gå til **Retail og Commerce \> Forespørgsler og rapporter \> Batchjobs**.</span><span class="sxs-lookup"><span data-stu-id="03731-159">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="03731-160">De resterende trin i denne procedure skal fuldføres for hvert af følgende job:</span><span class="sxs-lookup"><span data-stu-id="03731-160">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="03731-161">Behandling af e-mail-besked om detailordre</span><span class="sxs-lookup"><span data-stu-id="03731-161">Process retail order email notification</span></span>
    * <span data-ttu-id="03731-162">Produkttilgængelighed</span><span class="sxs-lookup"><span data-stu-id="03731-162">Product availability</span></span>
    * <span data-ttu-id="03731-163">P-0001</span><span class="sxs-lookup"><span data-stu-id="03731-163">P-0001</span></span>
    * <span data-ttu-id="03731-164">Synkroniser ordrejob</span><span class="sxs-lookup"><span data-stu-id="03731-164">Synchronize orders job</span></span>

1. <span data-ttu-id="03731-165">Brug Quick Filter til at søge efter jobbet ved hjælp af dets navn.</span><span class="sxs-lookup"><span data-stu-id="03731-165">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="03731-166">Hvis status for jobbet er **Udfører**, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="03731-166">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="03731-167">Vælg posten.</span><span class="sxs-lookup"><span data-stu-id="03731-167">Select the record.</span></span>
    1. <span data-ttu-id="03731-168">Klik på **Batchjob** i handlingsruden, og vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="03731-168">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="03731-169">Vælg **Annullering**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="03731-169">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="03731-170">Du kan også vælge at angive gentagelsesintervallet til et (1) minut for følgende job:</span><span class="sxs-lookup"><span data-stu-id="03731-170">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="03731-171">Behandling af job med e-mailbesked om detailordre</span><span class="sxs-lookup"><span data-stu-id="03731-171">Process retail order email notification job</span></span>
* <span data-ttu-id="03731-172">P-0001-job</span><span class="sxs-lookup"><span data-stu-id="03731-172">P-0001 job</span></span>
* <span data-ttu-id="03731-173">Synkroniser ordrejob</span><span class="sxs-lookup"><span data-stu-id="03731-173">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="03731-174">Kør fuld datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="03731-174">Run full data synchronization</span></span>

<span data-ttu-id="03731-175">Følg disse trin for at køre fuld datasynkronisering i Commerce-hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="03731-175">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="03731-176">Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Handelsplanlægger \> Kanaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="03731-176">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="03731-177">Vælg den kanal, der hedder **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="03731-177">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="03731-178">Vælg **Fuld datasynkronisering** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="03731-178">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="03731-179">Angiv **9999** som distributionsplanen.</span><span class="sxs-lookup"><span data-stu-id="03731-179">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="03731-180">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="03731-180">Select **OK**.</span></span>
1. <span data-ttu-id="03731-181">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="03731-181">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="03731-182">Test kreditkortoplysninger for at udføre testindkøb</span><span class="sxs-lookup"><span data-stu-id="03731-182">Test credit card information to do test purchases</span></span>

<span data-ttu-id="03731-183">Du kan bruge følgende disse testkreditkortoplysninger til at udføre testtransaktioner på webstedet:</span><span class="sxs-lookup"><span data-stu-id="03731-183">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="03731-184">**Kortnummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="03731-184">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="03731-185">**Udløbsdato** 10/20</span><span class="sxs-lookup"><span data-stu-id="03731-185">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="03731-186">**Kontrolcifrene på kreditkortet (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="03731-186">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="03731-187">Forsøg aldrig under nogen omstændigheder at bruge faktiske kreditkortoplysninger på testwebstedet.</span><span class="sxs-lookup"><span data-stu-id="03731-187">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="03731-188">Næste trin</span><span class="sxs-lookup"><span data-stu-id="03731-188">Next steps</span></span>

<span data-ttu-id="03731-189">Når klargørings- og konfigurationstrinnene er fuldførte, kan du begynde at bruge dit evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="03731-189">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="03731-190">Brug Site Builder-URL-adressen for Commerce-webstedet til at gå til oprettelsesoplevelsen.</span><span class="sxs-lookup"><span data-stu-id="03731-190">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="03731-191">Brug URL-adressen for Commerce-webstedet for at gå til detailkundewebstedet.</span><span class="sxs-lookup"><span data-stu-id="03731-191">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="03731-192">Hvis du vil konfigurere valgfrie funktioner til dit Commerce-evalueringsmiljø, se [Konfigurere valgfrie funktioner til et Commerce-evalueringsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="03731-192">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="03731-193">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="03731-193">Additional resources</span></span>

[<span data-ttu-id="03731-194">Oversigt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="03731-194">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="03731-195">Klargøre et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="03731-195">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="03731-196">Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="03731-196">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="03731-197">Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="03731-197">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="03731-198">Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="03731-198">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="03731-199">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="03731-199">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="03731-200">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="03731-200">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="03731-201">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="03731-201">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="03731-202">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="03731-202">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
