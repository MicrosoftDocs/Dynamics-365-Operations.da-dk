---
title: Konfigurere et Dynamics 365 Commerce-prøveversionsmiljø
description: I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-prøveversionsmiljø, efter at det er blevet klargjort.
author: psimolin
manager: annbe
ms.date: 12/10/2019
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
ms.openlocfilehash: d72caee25c03e8167b94dd387c7861f98bd0f4cb
ms.sourcegitcommit: 12b9d6f2dd24e52e46487748c848864909af6967
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/14/2020
ms.locfileid: "3057711"
---
# <a name="configure-a-dynamics-365-commerce-preview-environment"></a><span data-ttu-id="b45e1-103">Konfigurere et Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="b45e1-103">Configure a Dynamics 365 Commerce preview environment</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b45e1-104">I dette emne beskrives det, hvordan du konfigurerer et Microsoft Dynamics 365 Commerce-prøveversionsmiljø, efter at det er blevet klargjort.</span><span class="sxs-lookup"><span data-stu-id="b45e1-104">This topic explains how to configure a Microsoft Dynamics 365 Commerce preview environment after it's provisioned.</span></span>

## <a name="overview"></a><span data-ttu-id="b45e1-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="b45e1-105">Overview</span></span>

<span data-ttu-id="b45e1-106">Fuldfør kun procedurerne i dette emne, efter dit Commerce-prøveversionsmiljø er klargjort.</span><span class="sxs-lookup"><span data-stu-id="b45e1-106">Complete the procedures in this topic only after your Commerce preview environment has been provisioned.</span></span> <span data-ttu-id="b45e1-107">For yderligere oplysninger om, hvordan du klargør dit Commerce-prøveversionsmiljø se [Klargøring af et Commerce-prøveversionsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="b45e1-107">For information about how to provision your Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

<span data-ttu-id="b45e1-108">Når dit Commerce-prøveversionsmiljø er blevet klargjort fra ende til anden, skal yderligere konfigurationstrin efter klargøring fuldføres, før du kan begynde at evaluere miljøet.</span><span class="sxs-lookup"><span data-stu-id="b45e1-108">After your Commerce preview environment has been provisioned end to end, additional post-provisioning configuration steps must be completed before you can start to evaluate the environment.</span></span> <span data-ttu-id="b45e1-109">Hvis du vil fuldføre disse trin, skal du bruge Microsoft Dynamics Lifecycle Services (LCS) og Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="b45e1-109">To complete these steps, you must use Microsoft Dynamics Lifecycle Services (LCS) and Dynamics 365 Commerce.</span></span>

## <a name="before-you-start"></a><span data-ttu-id="b45e1-110">Før du begynder</span><span class="sxs-lookup"><span data-stu-id="b45e1-110">Before you start</span></span>

1. <span data-ttu-id="b45e1-111">Log på [LCS-portalen](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="b45e1-111">Sign in to the [LCS portal](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="b45e1-112">Gå til dit projekt.</span><span class="sxs-lookup"><span data-stu-id="b45e1-112">Go to your project.</span></span>
1. <span data-ttu-id="b45e1-113">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="b45e1-113">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="b45e1-114">Vælg dit miljø fra listen.</span><span class="sxs-lookup"><span data-stu-id="b45e1-114">Select your environment in the list.</span></span>
1. <span data-ttu-id="b45e1-115">Vælg **Alle detaljer** i miljøoplysningerne til højre.</span><span class="sxs-lookup"><span data-stu-id="b45e1-115">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="b45e1-116">Vælg **Log på** for at åbne en menu, og vælg dernæst **Log på miljøet**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-116">Select **Login** to open a menu, and then select **Log on to environment**.</span></span>
1. <span data-ttu-id="b45e1-117">Kontrollér, at den juridiske enhed **USRT** er valgt i øverste højre hjørne.</span><span class="sxs-lookup"><span data-stu-id="b45e1-117">Make sure that the **USRT** legal entity is selected in the upper-right corner.</span></span>

## <a name="configure-the-point-of-sale-in-lcs"></a><span data-ttu-id="b45e1-118">Konfigurer POS i LCS</span><span class="sxs-lookup"><span data-stu-id="b45e1-118">Configure the point of sale in LCS</span></span>

### <a name="associate-a-worker-with-your-identity"></a><span data-ttu-id="b45e1-119">Tilknyt en arbejder til din identitet</span><span class="sxs-lookup"><span data-stu-id="b45e1-119">Associate a worker with your identity</span></span>

<span data-ttu-id="b45e1-120">Hvis du vil knytte en arbejder til din identitet i LCS, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="b45e1-120">To associate a worker with your identity in LCS, follow these steps.</span></span>

1. <span data-ttu-id="b45e1-121">Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Medarbejdere \> Arbejdere**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-121">Use the menu on the left to go to **Modules \> Retail and commerce \> Employees \> Workers**.</span></span>
1. <span data-ttu-id="b45e1-122">Find og vælg følgende post i listen: **000713 - Andrew Collette**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-122">In the list, find and select the following record: **000713 - Andrew Collette**.</span></span>
1. <span data-ttu-id="b45e1-123">Vælg **Retail** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b45e1-123">On the Action Pane, select **Retail**.</span></span>
1. <span data-ttu-id="b45e1-124">Vælg **Tilknyt eksisterende identitet**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-124">Select **Associate existing identity**.</span></span>
1. <span data-ttu-id="b45e1-125">Skriv din mailadresse i feltet **E-mail** til højre for **Søg ved hjælp af e-mail**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-125">In the **Email** field to the right of **Search using email**, enter your email address.</span></span>
1. <span data-ttu-id="b45e1-126">Vælg **Søg**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-126">Select **Search**.</span></span>
1. <span data-ttu-id="b45e1-127">Vælg posten med dit navn.</span><span class="sxs-lookup"><span data-stu-id="b45e1-127">Select the record that has your name.</span></span>
1. <span data-ttu-id="b45e1-128">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-128">Select **OK**.</span></span>
1. <span data-ttu-id="b45e1-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-129">Select **Save**.</span></span>

### <a name="activate-cloud-pos"></a><span data-ttu-id="b45e1-130">Aktiverere sky POS</span><span class="sxs-lookup"><span data-stu-id="b45e1-130">Activate Cloud POS</span></span>

<span data-ttu-id="b45e1-131">Følg disse trin for at aktivere skybaseret POS i LCS.</span><span class="sxs-lookup"><span data-stu-id="b45e1-131">To activate Cloud POS in LCS, follow these steps.</span></span>

1. <span data-ttu-id="b45e1-132">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="b45e1-132">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="b45e1-133">Vælg dit miljø fra listen.</span><span class="sxs-lookup"><span data-stu-id="b45e1-133">Select your environment in the list.</span></span>
1. <span data-ttu-id="b45e1-134">Vælg **Alle detaljer** i miljøoplysningerne til højre.</span><span class="sxs-lookup"><span data-stu-id="b45e1-134">In the environment information on the right, select **Full details**.</span></span>
1. <span data-ttu-id="b45e1-135">Vælg **Log på** for at åbne en menu, og vælg derefter **Log på skybaseret POS** for at åbne POS.</span><span class="sxs-lookup"><span data-stu-id="b45e1-135">Select **Login** to open a menu, and then select **Log on to Cloud Point of Sale** to open the point of sale (POS).</span></span>
1. <span data-ttu-id="b45e1-136">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-136">Select **Next**.</span></span>
1. <span data-ttu-id="b45e1-137">Log på ved hjælp af din Microsoft Azure Active Directory (Azure AD)-konto.</span><span class="sxs-lookup"><span data-stu-id="b45e1-137">Sign in by using your Microsoft Azure Active Directory (Azure AD) account.</span></span>
1. <span data-ttu-id="b45e1-138">Under **Butiksnavn** skal du vælge **San Francisco**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-138">Under **Store name**, select **San Francisco**.</span></span>
1. <span data-ttu-id="b45e1-139">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-139">Select **Next**.</span></span>
1. <span data-ttu-id="b45e1-140">Under **Kasseapparat og enhed** skal du vælge **SANFRAN-1**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-140">Under **Register and device**, select **SANFRAN-1**.</span></span>
1. <span data-ttu-id="b45e1-141">Vælg **Aktivér**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-141">Select **Activate**.</span></span> <span data-ttu-id="b45e1-142">Du er logget ud og dirigeret til POS-login-siden.</span><span class="sxs-lookup"><span data-stu-id="b45e1-142">You're signed out and taken to the POS sign-in page.</span></span>
1. <span data-ttu-id="b45e1-143">Du kan nu logge på den skybaserede POS-oplevelse ved hjælp af operatør-ID **000713** og adgangskoden **123**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-143">You can now sign in to the Cloud POS experience by using operator ID **000713** and password **123**.</span></span>

## <a name="set-up-your-site-in-commerce"></a><span data-ttu-id="b45e1-144">Konfigurer dit websted i Commerce</span><span class="sxs-lookup"><span data-stu-id="b45e1-144">Set up your site in Commerce</span></span>

<span data-ttu-id="b45e1-145">Følg disse trin for at begynde at konfigurere dit prøveversionswebsted i Commerce.</span><span class="sxs-lookup"><span data-stu-id="b45e1-145">To start to set up your preview site in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b45e1-146">Log på værktøjet til administration af webstedet ved hjælp af den URL-adresse, som du noterede ned, da du initialiserede e-Commerce i forbindelse med klargøring (jf. [Initialiser e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span><span class="sxs-lookup"><span data-stu-id="b45e1-146">Sign in to the site management tool by using the URL that you made a note of when you initialized e-Commerce during provisioning (see [Initialize e-Commerce](provisioning-guide.md#initialize-e-commerce)).</span></span>
1. <span data-ttu-id="b45e1-147">Vælg webstedet **Fabrikam** for at åbne dialogboksen webstedsopsætning.</span><span class="sxs-lookup"><span data-stu-id="b45e1-147">Select the **Fabrikam** site to open the site setup dialog box.</span></span>
1. <span data-ttu-id="b45e1-148">Vælg det domæne, du angav, da du initialiserede e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="b45e1-148">Select the domain that you entered when you initialized e-Commerce.</span></span>
1. <span data-ttu-id="b45e1-149">Som standardkanal skal du vælge **Udvidet Fabrikam-onlinebutik**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-149">Select **Fabrikam extended online store** as the default channel.</span></span> <span data-ttu-id="b45e1-150">(Sørg for at vælge den **udvidede** onlinebutik.)</span><span class="sxs-lookup"><span data-stu-id="b45e1-150">(Make sure that you select the **extended** online store.)</span></span>
1. <span data-ttu-id="b45e1-151">Vælg **da-dk** som standardsprog.</span><span class="sxs-lookup"><span data-stu-id="b45e1-151">Select **en-us** as the default language.</span></span>
1. <span data-ttu-id="b45e1-152">Lad værdien i feltet **Sti** være, som den er.</span><span class="sxs-lookup"><span data-stu-id="b45e1-152">Leave the value of the **Path** field as it is.</span></span>
1. <span data-ttu-id="b45e1-153">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-153">Select **OK**.</span></span> <span data-ttu-id="b45e1-154">Listen over sider på webstedet vises.</span><span class="sxs-lookup"><span data-stu-id="b45e1-154">The list of pages on the site appears.</span></span>

## <a name="enable-jobs"></a><span data-ttu-id="b45e1-155">Aktivere job</span><span class="sxs-lookup"><span data-stu-id="b45e1-155">Enable jobs</span></span>

<span data-ttu-id="b45e1-156">Følg disse trin for at aktivere job i Commerce.</span><span class="sxs-lookup"><span data-stu-id="b45e1-156">To enable jobs in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b45e1-157">Log på miljøet (hovedkontor).</span><span class="sxs-lookup"><span data-stu-id="b45e1-157">Sign in to the environment (HQ).</span></span>
1. <span data-ttu-id="b45e1-158">Brug menuen til venstre for at gå til **Retail og Commerce \> Forespørgsler og rapporter \> Batchjobs**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-158">Use the menu on the left to go to **Retail and commerce \> Inquiries and reports \> Batch jobs**.</span></span>

    <span data-ttu-id="b45e1-159">De resterende trin i denne procedure skal fuldføres for hvert af følgende job:</span><span class="sxs-lookup"><span data-stu-id="b45e1-159">The remaining steps of this procedure must be completed for each of the following jobs:</span></span>

    * <span data-ttu-id="b45e1-160">Behandling af e-mail-besked om detailordre</span><span class="sxs-lookup"><span data-stu-id="b45e1-160">Process retail order email notification</span></span>
    * <span data-ttu-id="b45e1-161">Produkttilgængelighed</span><span class="sxs-lookup"><span data-stu-id="b45e1-161">Product availability</span></span>
    * <span data-ttu-id="b45e1-162">P-0001</span><span class="sxs-lookup"><span data-stu-id="b45e1-162">P-0001</span></span>
    * <span data-ttu-id="b45e1-163">Synkroniser ordrejob</span><span class="sxs-lookup"><span data-stu-id="b45e1-163">Synchronize orders job</span></span>

1. <span data-ttu-id="b45e1-164">Brug Quick Filter til at søge efter jobbet ved hjælp af dets navn.</span><span class="sxs-lookup"><span data-stu-id="b45e1-164">Use the Quick Filter to search for the job by name.</span></span>
1. <span data-ttu-id="b45e1-165">Hvis status for jobbet er **Tilbagehold**, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="b45e1-165">If the status of the job is **Withhold**, follow these steps:</span></span>

    1. <span data-ttu-id="b45e1-166">Vælg posten.</span><span class="sxs-lookup"><span data-stu-id="b45e1-166">Select the record.</span></span>
    1. <span data-ttu-id="b45e1-167">Klik på **Batchjob** i handlingsruden, og vælg **Skift status**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-167">On the Action Pane, on **Batch job** tab, select **Change status**.</span></span>
    1. <span data-ttu-id="b45e1-168">Vælg **Afventer**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-168">Select **Waiting**, and then select **OK**.</span></span>

### <a name="run-full-data-synchronization"></a><span data-ttu-id="b45e1-169">Kør fuld datasynkronisering</span><span class="sxs-lookup"><span data-stu-id="b45e1-169">Run full data synchronization</span></span>

<span data-ttu-id="b45e1-170">Følg disse trin for at køre fuld datasynkronisering i Commerce.</span><span class="sxs-lookup"><span data-stu-id="b45e1-170">To run full data synchronization in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="b45e1-171">Brug menuen til venstre for at gå til **Moduler \> Retail og Commerce \> Konfiguration af hovedkontor \> Retail planlægger \> Kanaldatabase**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-171">Use the menu on the left to go to **Modules \> Retail and commerce \> Headquarters setup \> Retail scheduler \> Channel database**.</span></span>
1. <span data-ttu-id="b45e1-172">På listen til venstre er kanalen **Standard** valgt.</span><span class="sxs-lookup"><span data-stu-id="b45e1-172">In the list on the left, the **Default** channel is selected.</span></span> <span data-ttu-id="b45e1-173">Vælg den anden tilgængelige kanal.</span><span class="sxs-lookup"><span data-stu-id="b45e1-173">Select the other available channel.</span></span> <span data-ttu-id="b45e1-174">Denne kanal hedder **scXXXXXXXXX**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-174">This channel is named **scXXXXXXXXX**.</span></span>
1. <span data-ttu-id="b45e1-175">Vælg **Fuld datasynkronisering** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="b45e1-175">On the Action Pane, select **Full data sync**.</span></span>
1. <span data-ttu-id="b45e1-176">Angiv **9999** som distributionsplanen.</span><span class="sxs-lookup"><span data-stu-id="b45e1-176">Enter **9999** as the distribution schedule.</span></span>
1. <span data-ttu-id="b45e1-177">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-177">Select **OK**.</span></span>
1. <span data-ttu-id="b45e1-178">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="b45e1-178">Select **OK**.</span></span>

### <a name="test-credit-card-information-to-do-test-purchases"></a><span data-ttu-id="b45e1-179">Test kreditkortoplysninger for at udføre testindkøb</span><span class="sxs-lookup"><span data-stu-id="b45e1-179">Test credit card information to do test purchases</span></span>

<span data-ttu-id="b45e1-180">Du kan bruge følgende disse testkreditkortoplysninger til at udføre testtransaktioner på webstedet:</span><span class="sxs-lookup"><span data-stu-id="b45e1-180">To perform test transactions on the site, you can use the following test credit card information:</span></span>

- <span data-ttu-id="b45e1-181">**Kortnummer:** 4111-1111-1111-1111</span><span class="sxs-lookup"><span data-stu-id="b45e1-181">**Card number:** 4111-1111-1111-1111</span></span>
- <span data-ttu-id="b45e1-182">**Udløbsdato** 10/20</span><span class="sxs-lookup"><span data-stu-id="b45e1-182">**Expiration date:** 10/20</span></span>
- <span data-ttu-id="b45e1-183">**Kontrolcifrene på kreditkortet (CVV):** 737</span><span class="sxs-lookup"><span data-stu-id="b45e1-183">**Card verification value (CVV) code:** 737</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b45e1-184">Forsøg aldrig under nogen omstændigheder at bruge faktiske kreditkortoplysninger på testwebstedet.</span><span class="sxs-lookup"><span data-stu-id="b45e1-184">Never, under any circumstances, try to use actual credit card information on the test site.</span></span>

## <a name="next-steps"></a><span data-ttu-id="b45e1-185">Næste trin</span><span class="sxs-lookup"><span data-stu-id="b45e1-185">Next steps</span></span>

<span data-ttu-id="b45e1-186">Når klargørings- og konfigurationstrinnene er fuldførte, er du klar til at evaluere dit prøveversionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="b45e1-186">After the provisioning and configuration steps are completed, you're ready to evaluate your preview environment.</span></span> <span data-ttu-id="b45e1-187">Brug URL-adressen til administrationsværktøjet for Commerce-webstedet til at gå til oprettelsesoplevelsen.</span><span class="sxs-lookup"><span data-stu-id="b45e1-187">Use the URL of the Commerce site management tool to go to the authoring experience.</span></span> <span data-ttu-id="b45e1-188">Brug URL-adressen for Commerce-webstedet for at gå til oplevelsen detailkundewebstedet.</span><span class="sxs-lookup"><span data-stu-id="b45e1-188">Use the URL of the Commerce site to go to the retail customer site experience.</span></span>

<span data-ttu-id="b45e1-189">Hvis du vil konfigurere valgfrie funktioner til dit Commerce-prøveversionsmiljø, se [Konfiguration af valgfrie funktioner til et Commerce-prøveversionsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="b45e1-189">To configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b45e1-190">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b45e1-190">Additional resources</span></span>

[<span data-ttu-id="b45e1-191">Oversigt over Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="b45e1-191">Dynamics 365 Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="b45e1-192">Klargøre et Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="b45e1-192">Provision a Dynamics 365 Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="b45e1-193">Konfigurere valgfrie funktioner for et Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="b45e1-193">Configure optional features for a Dynamics 365 Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="b45e1-194">Ofte stillede spørgsmål om Dynamics 365 Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="b45e1-194">Dynamics 365 Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="b45e1-195">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="b45e1-195">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="b45e1-196">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="b45e1-196">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="b45e1-197">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="b45e1-197">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="b45e1-198">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="b45e1-198">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
