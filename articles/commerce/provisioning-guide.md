---
title: Klargøre et Dynamics 365 Commerce-evalueringsmiljø
description: I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-evalueringsmiljø.
author: psimolin
manager: annbe
ms.date: 11/05/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: b54216a565c264dfcfe821581fee9df7b5e22323
ms.sourcegitcommit: 715508547f9a71a89a138190e8540686556c753d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/05/2020
ms.locfileid: "4411235"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="3546f-103">Klargøre et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="3546f-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="3546f-104">I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="3546f-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="3546f-105">Før du går i gang, anbefales det, at du hurtigt gennemgår dette emne for at få et indtryk af, hvad processen kræver.</span><span class="sxs-lookup"><span data-stu-id="3546f-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="3546f-106">Miljøer til Commerce-evaluering er ikke generelt tilgængelige og tildeles til partnere og kunder efter anmodning.</span><span class="sxs-lookup"><span data-stu-id="3546f-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="3546f-107">Du kan få flere oplysninger ved at rette henvendelse til din kontakt hos din Microsoft-partner.</span><span class="sxs-lookup"><span data-stu-id="3546f-107">For more information, reach out to your Microsoft partner contact.</span></span>

## <a name="overview"></a><span data-ttu-id="3546f-108">Overblik</span><span class="sxs-lookup"><span data-stu-id="3546f-108">Overview</span></span>

<span data-ttu-id="3546f-109">Hvis du vil kunne klargør et Commerce-evalueringsmiljø, skal du oprette et projekt, der har et bestemt produktnavn og er en bestemt type.</span><span class="sxs-lookup"><span data-stu-id="3546f-109">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="3546f-110">Miljøet og Commerce Scale Unit (CSU) har nogle specifikke parametre, du skal bruge, når du forventer at klargøre dit e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="3546f-110">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="3546f-111">Instruktionerne i dette emne beskriver alle de påkrævede trin for klargøring og de parametre, du skal bruge.</span><span class="sxs-lookup"><span data-stu-id="3546f-111">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="3546f-112">Nå du har klargjort dit Commerce-evalueringsmiljø, skal du fuldføre nogle få efter-klargørings-trin, for at gøre dit evalueringsmiljø klar til brug.</span><span class="sxs-lookup"><span data-stu-id="3546f-112">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="3546f-113">Nogle trin er valgfrie, afhængigt af de aspekter af systemet, du vil evaluere.</span><span class="sxs-lookup"><span data-stu-id="3546f-113">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="3546f-114">Du kan altid udføre de valgfrie trin senere.</span><span class="sxs-lookup"><span data-stu-id="3546f-114">You can always complete the optional steps later.</span></span>

<span data-ttu-id="3546f-115">For yderligere oplysninger om, hvordan du konfigurerer dit Commerce-evalueringsmiljø, efter du har klargjort det, se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="3546f-115">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="3546f-116">For yderligere oplysninger om, hvordan du konfigurerer valgfrie funktioner til dit Commerce-evalueringsmiljø, se [Konfigurere valgfrie funktioner til et Commerce-evalueringsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="3546f-116">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="3546f-117">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="3546f-117">Prerequisites</span></span>

<span data-ttu-id="3546f-118">Følgende forudsætninger skal være på plads, før du kan klargør dit Commerce-evalueringsmiljø:</span><span class="sxs-lookup"><span data-stu-id="3546f-118">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="3546f-119">Du er registreret i evalueringsprogrammet og har fået tildelt kapacitet til et evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="3546f-119">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="3546f-120">Du har adgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).</span><span class="sxs-lookup"><span data-stu-id="3546f-120">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="3546f-121">Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan oprette et Dynamics 365 Commerce-projekt.</span><span class="sxs-lookup"><span data-stu-id="3546f-121">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="3546f-122">Du har administratoradgang til dit Microsoft Azure-abonnement, eller du er i kontakt med en abonnementsadministrator, der kan hjælpe dig, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="3546f-122">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="3546f-123">Du har dit Azure Active Directory-lejer-ID (Azure AD) ved hånden.</span><span class="sxs-lookup"><span data-stu-id="3546f-123">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="3546f-124">Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en systemadministratorgruppe til e-Commerce, og du har gruppens ID ved hånden.</span><span class="sxs-lookup"><span data-stu-id="3546f-124">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="3546f-125">Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en gruppe for redaktører af vurderinger og anmeldelser, og du har gruppens ID ved hånden.</span><span class="sxs-lookup"><span data-stu-id="3546f-125">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="3546f-126">(Denne sikkerhedsgruppe kan være den samme som e-Commerce-systemadministratorgruppen.)</span><span class="sxs-lookup"><span data-stu-id="3546f-126">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="3546f-127">Bemærk, at denne liste ikke er udtømmende.</span><span class="sxs-lookup"><span data-stu-id="3546f-127">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="3546f-128">Hvis du oplever nogen problemer, skal du rette henvendelse til din kontakt hos din Microsoft-partner for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="3546f-128">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="3546f-129">Klargøre dit Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="3546f-129">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="3546f-130">Disse procedurer forklarer, hvordan du klargør et Commerce-evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="3546f-130">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="3546f-131">Når du har fuldført dem, vil Commerce-evalueringsmiljøet være klar til konfiguration.</span><span class="sxs-lookup"><span data-stu-id="3546f-131">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="3546f-132">Alle de aktiviteter, der er beskrevet her, finder sted på LCS-portalen.</span><span class="sxs-lookup"><span data-stu-id="3546f-132">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="3546f-133">Opret et nyt projekt</span><span class="sxs-lookup"><span data-stu-id="3546f-133">Create a new project</span></span>

<span data-ttu-id="3546f-134">Hvis du vil oprette et nyt projekt i LCS, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="3546f-134">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="3546f-135">På LCS-startsiden skal du vælge plustegnet (**+**) for at oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="3546f-135">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="3546f-136">Benyt en af følgende fremgangsmåder i højre rude:</span><span class="sxs-lookup"><span data-stu-id="3546f-136">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="3546f-137">Hvis du er en partner, skal du vælge **Overflyt, opret løsninger, og lær at bruge**.</span><span class="sxs-lookup"><span data-stu-id="3546f-137">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="3546f-138">Hvis du er en kunde, skal du vælge **Mulige førsalg**.</span><span class="sxs-lookup"><span data-stu-id="3546f-138">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="3546f-139">Angiv et navn, beskrivelse og branche.</span><span class="sxs-lookup"><span data-stu-id="3546f-139">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="3546f-140">I feltet **Produktnavn** skal du vælge **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="3546f-140">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="3546f-141">I feltet **Produktversion** skal du vælge **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="3546f-141">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="3546f-142">I feltet **Metode** skal du vælge **Dynamics Retail-implementeringsmetode**.</span><span class="sxs-lookup"><span data-stu-id="3546f-142">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="3546f-143">Valgfrit: Du kan importere roller og brugere fra et eksisterende projekt.</span><span class="sxs-lookup"><span data-stu-id="3546f-143">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="3546f-144">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="3546f-144">Select **Create**.</span></span> <span data-ttu-id="3546f-145">Projektoversigten vises.</span><span class="sxs-lookup"><span data-stu-id="3546f-145">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="3546f-146">Tilføj Azure Connector</span><span class="sxs-lookup"><span data-stu-id="3546f-146">Add the Azure Connector</span></span>

<span data-ttu-id="3546f-147">Hvis du vil føje Azure Connector til dit LCS-projekt, skal du følge trinnene i [Fuldføre processen til onboarding af Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="3546f-147">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="3546f-148">Installer miljøet</span><span class="sxs-lookup"><span data-stu-id="3546f-148">Deploy the environment</span></span>

<span data-ttu-id="3546f-149">Følg disse trin for at installere miljøet.</span><span class="sxs-lookup"><span data-stu-id="3546f-149">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="3546f-150">Du behøver måske ikke at fuldføre trin 6, 7 og/eller 8, fordi sider, der har en enkelt indstilling, springes over.</span><span class="sxs-lookup"><span data-stu-id="3546f-150">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="3546f-151">Når du er i visningen **Miljøparametre**, skal du bekræfte, at teksten **Dynamics 365 Commerce - Demo (10.0.* x* med platformsopdatering *xx*)\*\* vises direkte over feltet **Miljønavn**.</span><span class="sxs-lookup"><span data-stu-id="3546f-151">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="3546f-152">Se detaljer på den illustration, der vises efter trin 8.</span><span class="sxs-lookup"><span data-stu-id="3546f-152">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="3546f-153">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="3546f-153">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="3546f-154">Vælg **Tilføj** for at tilføje et miljø.</span><span class="sxs-lookup"><span data-stu-id="3546f-154">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="3546f-155">Vælg den seneste version i feltet **Programversion**.</span><span class="sxs-lookup"><span data-stu-id="3546f-155">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="3546f-156">Hvis du har et specifikt behov for at vælge en anden programversion end den seneste version, skal du ikke vælge en version før **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="3546f-156">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="3546f-157">I feltet **Platformsversion** skal du bruge den platformsversion, der automatisk vælges for den programversion, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="3546f-157">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Valg af program- og platformsversioner](./media/project1.png)

1. <span data-ttu-id="3546f-159">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="3546f-159">Select **Next**.</span></span>
1. <span data-ttu-id="3546f-160">Vælg **Demo** miljøtopologi.</span><span class="sxs-lookup"><span data-stu-id="3546f-160">Select **Demo** as the environment topology.</span></span>

    ![Valg af miljøtopologi 1](./media/project2.png)

1. <span data-ttu-id="3546f-162">Angiv et miljønavn på side **Installer miljø**.</span><span class="sxs-lookup"><span data-stu-id="3546f-162">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="3546f-163">Lad de avancerede indstillinger være, som de er.</span><span class="sxs-lookup"><span data-stu-id="3546f-163">Leave the advanced settings as they are.</span></span>

    ![Siden Installer miljø](./media/project4.png)

1. <span data-ttu-id="3546f-165">Juster VM-størrelsen efter behov.</span><span class="sxs-lookup"><span data-stu-id="3546f-165">Adjust the VM size as required.</span></span> <span data-ttu-id="3546f-166">(Vi anbefaler, at VM-lagerenheden \[SKU\] **D13 V2**.)</span><span class="sxs-lookup"><span data-stu-id="3546f-166">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="3546f-167">Gennemgå prissætnings- og licensvilkårene, og markér derefter afkrydsningsfeltet for at angive, at du accepterer dem.</span><span class="sxs-lookup"><span data-stu-id="3546f-167">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="3546f-168">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="3546f-168">Select **Next**.</span></span>
1. <span data-ttu-id="3546f-169">Klik på **Installer** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.</span><span class="sxs-lookup"><span data-stu-id="3546f-169">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="3546f-170">Du bliver sendt tilbage til visningen **Skybaserede miljøer**, og dit miljø skulle stå på listen.</span><span class="sxs-lookup"><span data-stu-id="3546f-170">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="3546f-171">Det miljø, du har anmodet om, vil blive vist i køen og derefter som under installation.</span><span class="sxs-lookup"><span data-stu-id="3546f-171">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="3546f-172">Det vil tage nogen tid at fuldføre miljø arbejdsgangene.</span><span class="sxs-lookup"><span data-stu-id="3546f-172">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="3546f-173">Kom derfor tilbage efter ca. seks til ni timer.</span><span class="sxs-lookup"><span data-stu-id="3546f-173">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="3546f-174">Før du fortsætter, skal du kontrollere, at din statussen for dit miljø er **Installeret**.</span><span class="sxs-lookup"><span data-stu-id="3546f-174">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="3546f-175">Initialisere Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="3546f-175">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="3546f-176">Følg disse trin for at påbegynde CSU.</span><span class="sxs-lookup"><span data-stu-id="3546f-176">To initialize CSU, follow these steps.</span></span>

1. <span data-ttu-id="3546f-177">Vælg dit miljø på listen i visningen **Skybaserede miljøer**.</span><span class="sxs-lookup"><span data-stu-id="3546f-177">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="3546f-178">Vælg **Alle detaljer** i miljøvisningen til højre.</span><span class="sxs-lookup"><span data-stu-id="3546f-178">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="3546f-179">Visningen med miljødetaljer vises.</span><span class="sxs-lookup"><span data-stu-id="3546f-179">The environment details view appears.</span></span>
1. <span data-ttu-id="3546f-180">Under **Miljøfunktioner** skal du vælge **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="3546f-180">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="3546f-181">På fanen **Commerce** skal du vælge **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="3546f-181">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="3546f-182">CSU-initialiseringsparametrene bliver vist.</span><span class="sxs-lookup"><span data-stu-id="3546f-182">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="3546f-183">I feltet **Område** skal du vælge det område, der er det samme eller tæt på det område, du har implementeret miljøet i.</span><span class="sxs-lookup"><span data-stu-id="3546f-183">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="3546f-184">Lad feltet **Version** være, som det er.</span><span class="sxs-lookup"><span data-stu-id="3546f-184">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="3546f-185">Vælg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="3546f-185">Select **Initialize**.</span></span>
1. <span data-ttu-id="3546f-186">Klik på **Ja** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.</span><span class="sxs-lookup"><span data-stu-id="3546f-186">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="3546f-187">Visningen **Commerce-administration** vises igen, hvor fanen **Commerce** er valgt.</span><span class="sxs-lookup"><span data-stu-id="3546f-187">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="3546f-188">Din CSU er sat i kø til klargøring.</span><span class="sxs-lookup"><span data-stu-id="3546f-188">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="3546f-189">Før du fortsætter, skal du kontrollere, at din statussen for dit CSU er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="3546f-189">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="3546f-190">Initialiseringen tager ca. to til fem timer.</span><span class="sxs-lookup"><span data-stu-id="3546f-190">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="3546f-191">Hvis du ikke kan finde linket **Administrer** i miljødetaljevisningen, skal du kontakte din Microsoft-kontaktperson for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="3546f-191">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="3546f-192">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="3546f-192">Initialize e-Commerce</span></span>

<span data-ttu-id="3546f-193">Følg disse trin for at påbegynde e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="3546f-193">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="3546f-194">Under fanen **e-Commerce** skal du gennemgå samtykket for evalueringen og derefter vælge **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="3546f-194">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="3546f-195">Angiv et navn for **e-Commerce-miljønavn** i feltet.</span><span class="sxs-lookup"><span data-stu-id="3546f-195">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="3546f-196">Vær opmærksom på, at navnet vil være synligt i nogle af URL-adresserne, der peger på din e-Commerce-forekomst.</span><span class="sxs-lookup"><span data-stu-id="3546f-196">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="3546f-197">I feltet **Commerce Scale Unit-navn** skal du vælge din CSU på listen.</span><span class="sxs-lookup"><span data-stu-id="3546f-197">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="3546f-198">(Listen bør kun have én indstilling.)</span><span class="sxs-lookup"><span data-stu-id="3546f-198">(The list should have only one option.)</span></span>

    <span data-ttu-id="3546f-199">Feltet **e-Commerce-geografi** indstilles automatisk.</span><span class="sxs-lookup"><span data-stu-id="3546f-199">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="3546f-200">Vælg **Næste** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="3546f-200">Select **Next** to continue.</span></span>
1. <span data-ttu-id="3546f-201">I feltet **Understøttede værtsnavne** skal du angive et vilkårligt gyldigt domæne som f.eks. `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="3546f-201">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="3546f-202">I feltet **ADD-sikkerhedsgruppe for systemadministratorer** skal du angive de første par bogstaver i navnet på den sikkerhedsgruppe, du vil bruge, og derefter vælge symbolet for forstørrelsesglas for at få vist søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="3546f-202">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="3546f-203">Vælg den korrekte sikkerhedsgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="3546f-203">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="3546f-204">I feltet **ADD-sikkerhedsgruppe for vurderings- og anmeldelsesadministratorer** skal du angive de første par bogstaver i navnet på den sikkerhedsgruppe, du vil bruge, og derefter vælge symbolet for forstørrelsesglas for at få vist søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="3546f-204">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="3546f-205">Vælg den korrekte sikkerhedsgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="3546f-205">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="3546f-206">Vælg **Ja** i indstillingen **Aktivér vurderinger og anmeldelser**.</span><span class="sxs-lookup"><span data-stu-id="3546f-206">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="3546f-207">Vælg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="3546f-207">Select **Initialize**.</span></span> <span data-ttu-id="3546f-208">Visningen **Commerce-administration** vises igen, hvor fanen **e-Commerce** er valgt.</span><span class="sxs-lookup"><span data-stu-id="3546f-208">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="3546f-209">Din initialisering af e-Commerce er påbegyndt.</span><span class="sxs-lookup"><span data-stu-id="3546f-209">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="3546f-210">Før du fortsætter, skal du vente, indtil initialiseringsstatus for din e-Commerce er **Initialisering blev gennemført**.</span><span class="sxs-lookup"><span data-stu-id="3546f-210">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="3546f-211">Under **Links** nederst til højre skal du notere URL-adresserne for følgende links:</span><span class="sxs-lookup"><span data-stu-id="3546f-211">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="3546f-212">**e-Commerce-websted** – linket til roden af dit e-Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="3546f-212">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="3546f-213">**Commerce-webstedsgenerator** – linket til administrationsværktøjet for webstedet.</span><span class="sxs-lookup"><span data-stu-id="3546f-213">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="3546f-214">Næste trin</span><span class="sxs-lookup"><span data-stu-id="3546f-214">Next steps</span></span>

<span data-ttu-id="3546f-215">For at fortsætte processen med klargøring og konfigurering af dit Commerce-evalueringsmiljø se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="3546f-215">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="3546f-216">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="3546f-216">Additional resources</span></span>

[<span data-ttu-id="3546f-217">Oversigt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="3546f-217">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="3546f-218">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="3546f-218">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="3546f-219">Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="3546f-219">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="3546f-220">Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="3546f-220">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="3546f-221">Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="3546f-221">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="3546f-222">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="3546f-222">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="3546f-223">Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="3546f-223">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="3546f-224">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="3546f-224">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="3546f-225">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="3546f-225">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)
