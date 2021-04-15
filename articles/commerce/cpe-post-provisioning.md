---
title: Konfigurere et Dynamics 365 Commerce-evalueringsmiljø
description: I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at det er blevet klargjort.
author: psimolin
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e80830a1cb0864c7eef19857b91e36ad27cdef
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5795853"
---
# <a name="configure-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="ffa4a-103">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="ffa4a-103">Configure a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ffa4a-104">I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-evalueringsmiljø, efter at det er blevet klargjort.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce evaluation environment after it's provisioned.</span></span>

<span data-ttu-id="ffa4a-105">Fuldfør kun procedurerne i dette emne, efter dit Commerce-evalueringsmiljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-105">Complete the procedures in this topic only after your Commerce evaluation environment has been provisioned.</span></span> <span data-ttu-id="ffa4a-106">For yderligere oplysninger om, hvordan du klargør dit Commerce-evalueringsmiljø se [Klargøre et Commerce-evalueringsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="ffa4a-106">For information about how to provision your Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

<span data-ttu-id="ffa4a-107">Når dit Commerce-evalueringsmiljø er blevet klargjort fra ende til anden, skal yderligere konfigurationstrin efter klargøring fuldføres, før du kan begynde at evaluere miljøet.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-107">After your Commerce evaluation environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="ffa4a-108">Hvis du vil fuldføre disse trin, skal du bruge Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-108">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="ffa4a-109">Før du begynder</span><span class="sxs-lookup"><span data-stu-id="ffa4a-109">Before you start</span></span>

1. <span data-ttu-id="ffa4a-110">Log på [LCS-portalen](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="ffa4a-110">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="ffa4a-111">Gå til dit projekt.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-111">Go to your project.</span></span>
1. <span data-ttu-id="ffa4a-112">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-112">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="ffa4a-113">Vælg dit miljø fra listen.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-113">Select your environment in the list.</span></span>
1. <span data-ttu-id="ffa4a-114">Vælg **Log på miljø** i miljøoplysningerne til højre.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-114">In the environment information on the right, select **Log on to environment**.</span></span> <span data-ttu-id="ffa4a-115">Du bliver sendt til Commerce-hovedkontoret.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-115">You will be sent to Commerce headquarters.</span></span>
1. <span data-ttu-id="ffa4a-116">Kontrollér, at den juridiske enhed **USRT** er valgt i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-116">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

<span data-ttu-id="ffa4a-117">Under klargøring af aktiviteter i Commerce-hovedkontoret skal du kontrollere, at den juridiske enhed **USRT** altid er markeret.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-117">During post-provisioning activities in Commerce headquarters, make sure that the **USRT** legal entity is always selected.</span></span>

## <a name="configure-the-point-of-sale"></a><span data-ttu-id="ffa4a-118">Konfigurer POS </span><span class="sxs-lookup"><span data-stu-id="ffa4a-118">Configure the point of sale</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="ffa4a-119">Tilknyt en arbejder til din identitet</span><span class="sxs-lookup"><span data-stu-id="ffa4a-119">Associate a worker with your identity</span></span>

<span data-ttu-id="ffa4a-120">Hvis du vil knytte en arbejder til din identitet, skal du følge disse trin i Commerce-hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-120">To associate a worker with your identity, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="ffa4a-121">Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Medarbejdere \> Arbejdere**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="ffa4a-122">Find og vælg følgende post i listen: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="ffa4a-123">Klik på **Commerce** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-123">On the Action Pane, select **Commerce**.</span></span>
1. <span data-ttu-id="ffa4a-124">Vælg **Tilknyt eksisterende identitet**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="ffa4a-125">Skriv din mailadresse i feltet **E-mail** til højre for **Søg ved hjælp af e-mail**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="ffa4a-126">Vælg **Søg**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-126">Select **Search**.</span></span>
1. <span data-ttu-id="ffa4a-127">Vælg posten med dit navn.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="ffa4a-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-128">Select **OK**.</span></span>
1. <span data-ttu-id="ffa4a-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="ffa4a-130">Aktiverere sky POS</span><span class="sxs-lookup"><span data-stu-id="ffa4a-130">Activate Cloud POS</span></span>

<span data-ttu-id="ffa4a-131">Følg disse trin for at aktivere skybaseret POS.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-131">To activate Cloud POS, follow these steps in LCS.</span></span>

1. <span data-ttu-id="ffa4a-132">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="ffa4a-133">Vælg dit miljø fra listen.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="ffa4a-134">Vælg **Log på skybaseret POS** i miljøoplysningerne til højre.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-134">In the environment information on the right, select **Log on to Cloud Point of Sale**.</span></span>
1. <span data-ttu-id="ffa4a-135">Vælg **Næste** for at åbne dialogboksen **Før du begynder**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-135">Select **Next** to open the **Before you start** dialog box.</span></span>
1. <span data-ttu-id="ffa4a-136">Lad feltet **Server-URL-adresse** være, som det er.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-136">Leave the **Server URL** field as it is.</span></span> <span data-ttu-id="ffa4a-137">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-137">Select **Next**.</span></span>
1. <span data-ttu-id="ffa4a-138">Log på ved hjælp af din Microsoft Azure Active Directory (Azure AD)-konto.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-138">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="ffa4a-139">Under **Butiksnavn** skal du vælge **San Francisco** og derefter vælge **Næste**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-139">Under **Store name**, select **San Francisco**, and then select **Next**.</span></span>
1. <span data-ttu-id="ffa4a-140">Under **Kasseapparat og enhed** skal du vælge **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="ffa4a-141">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-141">Select **Activate**.</span></span> <span data-ttu-id="ffa4a-142">Du er logget ud og dirigeret til POS-login-siden.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="ffa4a-143">Du kan nu logge på den skybaserede POS-oplevelse ved hjælp af operatør-ID **000713** og adgangskoden **123**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="ffa4a-144">Konfigurer dit websted i Commerce</span><span class="sxs-lookup"><span data-stu-id="ffa4a-144">Set up your site in Commerce</span></span>

<span data-ttu-id="ffa4a-145">Følg disse trin for at begynde at konfigurere dit evalueringswebsted i Commerce.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-145">To start to set up your evaluation site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ffa4a-146">Log på Site Builder ved hjælp af den URL-adresse, som du noterede ned, da du initialiserede e-Commerce i forbindelse med klargøring (jf. [Initialiser e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="ffa4a-146">Sign in to site builder by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="ffa4a-147">Vælg webstedet **Fabrikam** for at åbne dialogboksen webstedsopsætning.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="ffa4a-148">Vælg det domæne, du angav, da du initialiserede e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="ffa4a-149">Som standardkanal skal du vælge **Udvidet Fabrikam-onlinebutik**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="ffa4a-150">(Sørg for at vælge den **udvidede** onlinebutik.)</span><span class="sxs-lookup"><span data-stu-id="ffa4a-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="ffa4a-151">Vælg **da-dk** som standardsprog.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="ffa4a-152">Lad værdien i feltet **Sti** være, som den er.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="ffa4a-153">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-153">Select **OK**.</span></span> <span data-ttu-id="ffa4a-154">Listen over sider på webstedet vises.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="ffa4a-155">Aktivere job</span><span class="sxs-lookup"><span data-stu-id="ffa4a-155">Enable jobs</span></span>

<span data-ttu-id="ffa4a-156">Følg disse trin for at aktivere job i Commerce.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="ffa4a-157">Log på miljøet (hovedkontor).</span><span class="sxs-lookup"><span data-stu-id="ffa4a-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="ffa4a-158">Brug menuen til venstre for at gå til **Retail og Commerce \> Forespørgsler og rapporter \> Batchjobs**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="ffa4a-159">De resterende trin i denne procedure skal fuldføres for hvert af følgende job:</span><span class="sxs-lookup"><span data-stu-id="ffa4a-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="ffa4a-160">Behandling af e-mail-besked om detailordre</span><span class="sxs-lookup"><span data-stu-id="ffa4a-160">Process retail order email notification</span></span>
    * <span data-ttu-id="ffa4a-161">Produkttilgængelighed</span><span class="sxs-lookup"><span data-stu-id="ffa4a-161">Product availability</span></span>
    * <span data-ttu-id="ffa4a-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="ffa4a-162">P-0001</span></span>
    * <span data-ttu-id="ffa4a-163">Synkroniser ordrejob</span><span class="sxs-lookup"><span data-stu-id="ffa4a-163">Synchronize orders job</span></span>

1. <span data-ttu-id="ffa4a-164">Brug Quick Filter til at søge efter jobbet ved hjælp af dets navn.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="ffa4a-165">Hvis status for jobbet er **Udfører**, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="ffa4a-165">If the status of the job is **Executing**, follow these steps:</span></span>

    1. <span data-ttu-id="ffa4a-166">Vælg posten.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-166">Select the record.</span></span>
    1. <span data-ttu-id="ffa4a-167">Klik på **Batchjob** i handlingsruden, og vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="ffa4a-168">Vælg **Annullering**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-168">Select **Canceling**, and then select **OK**.</span></span>

<span data-ttu-id="ffa4a-169">Du kan også vælge at angive gentagelsesintervallet til et (1) minut for følgende job:</span><span class="sxs-lookup"><span data-stu-id="ffa4a-169">Optionally, you can also set the recurrence interval to one (1) minute for the following jobs:</span></span>

* <span data-ttu-id="ffa4a-170">Behandling af job med e-mailbesked om detailordre</span><span class="sxs-lookup"><span data-stu-id="ffa4a-170">Process retail order email notification job</span></span>
* <span data-ttu-id="ffa4a-171">P-0001-job</span><span class="sxs-lookup"><span data-stu-id="ffa4a-171">P-0001 job</span></span>
* <span data-ttu-id="ffa4a-172">Synkroniser ordrejob</span><span class="sxs-lookup"><span data-stu-id="ffa4a-172">Synchronize orders job</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="ffa4a-173">Kør fuld datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="ffa4a-173">Run full data synchronization</span></span>

<span data-ttu-id="ffa4a-174">Følg disse trin for at køre fuld datasynkronisering i Commerce-hovedkontor.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-174">To run full data synchronization in Commerce, follow these steps in Commerce headquarters.</span></span>

1. <span data-ttu-id="ffa4a-175">Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Handelsplanlægger \> Kanaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-175">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Commerce scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="ffa4a-176">Vælg den kanal, der hedder **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-176">Select the channel that is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="ffa4a-177">Vælg **Fuld datasynkronisering** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-177">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="ffa4a-178">Angiv **9999** som distributionsplanen.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-178">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="ffa4a-179">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-179">Select **OK**.</span></span>
1. <span data-ttu-id="ffa4a-180">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-180">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="ffa4a-181">Test kreditkortoplysninger for at udføre testindkøb</span><span class="sxs-lookup"><span data-stu-id="ffa4a-181">Test credit card information to do test purchases</span></span>

<span data-ttu-id="ffa4a-182">Du kan bruge følgende disse testkreditkortoplysninger til at udføre testtransaktioner på webstedet:</span><span class="sxs-lookup"><span data-stu-id="ffa4a-182">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="ffa4a-183">**Kortnummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="ffa4a-183">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="ffa4a-184">**Udløbsdato** 10/20</span><span class="sxs-lookup"><span data-stu-id="ffa4a-184">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="ffa4a-185">**Kontrolcifrene på kreditkortet (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="ffa4a-185">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ffa4a-186">Forsøg aldrig under nogen omstændigheder at bruge faktiske kreditkortoplysninger på testwebstedet.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-186">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="ffa4a-187">Næste trin</span><span class="sxs-lookup"><span data-stu-id="ffa4a-187">Next steps</span></span>

<span data-ttu-id="ffa4a-188">Når klargørings- og konfigurationstrinnene er fuldførte, kan du begynde at bruge dit evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-188">After the provisioning and configuration steps are completed, you can start to use your evaluation environment.</span></span> <span data-ttu-id="ffa4a-189">Brug Site Builder-URL-adressen for Commerce-webstedet til at gå til oprettelsesoplevelsen.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-189">Use the Commerce site builder URL to go to the authoring experience.</span></span> <span data-ttu-id="ffa4a-190">Brug URL-adressen for Commerce-webstedet for at gå til detailkundewebstedet.</span><span class="sxs-lookup"><span data-stu-id="ffa4a-190">Use the Commerce site URL to go to the retail customer site experience.</span></span>

<span data-ttu-id="ffa4a-191">Hvis du vil konfigurere valgfrie funktioner til dit Commerce-evalueringsmiljø, se [Konfigurere valgfrie funktioner til et Commerce-evalueringsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="ffa4a-191">To configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ffa4a-192">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ffa4a-192">Additional resources</span></span>

[<span data-ttu-id="ffa4a-193">Oversigt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="ffa4a-193">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="ffa4a-194">Klargøre et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="ffa4a-194">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="ffa4a-195">Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="ffa4a-195">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="ffa4a-196">Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="ffa4a-196">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="ffa4a-197">Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="ffa4a-197">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="ffa4a-198">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="ffa4a-198">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="ffa4a-199">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="ffa4a-199">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="ffa4a-200">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="ffa4a-200">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="ffa4a-201">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="ffa4a-201">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
