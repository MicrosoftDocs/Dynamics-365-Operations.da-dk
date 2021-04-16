---
title: Klargøre et Dynamics 365 Commerce-evalueringsmiljø
description: I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-evalueringsmiljø.
author: psimolin
ms.date: 12/17/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 19cedf01d1b916de785454d55448f41d1f5db1df
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5792285"
---
# <a name="provision-a-dynamics-365-commerce-evaluation-environment"></a><span data-ttu-id="c3056-103">Klargøre et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="c3056-103">Provision a Dynamics 365 Commerce evaluation environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="c3056-104">I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="c3056-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

<span data-ttu-id="c3056-105">Før du går i gang, anbefales det, at du hurtigt gennemgår dette emne for at få et indtryk af, hvad processen kræver.</span><span class="sxs-lookup"><span data-stu-id="c3056-105">Before you begin, we recommend that you take a quick scan through this topic to get an idea of what the process requires.</span></span>

> [!NOTE]
> <span data-ttu-id="c3056-106">Miljøer til Commerce-evaluering er ikke generelt tilgængelige og tildeles til partnere og kunder efter anmodning.</span><span class="sxs-lookup"><span data-stu-id="c3056-106">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="c3056-107">Du kan få flere oplysninger ved at rette henvendelse til din kontakt hos din Microsoft-partner.</span><span class="sxs-lookup"><span data-stu-id="c3056-107">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="c3056-108">Hvis du vil kunne klargør et Commerce-evalueringsmiljø, skal du oprette et projekt, der har et bestemt produktnavn og er en bestemt type.</span><span class="sxs-lookup"><span data-stu-id="c3056-108">To successfully provision a Commerce evaluation environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="c3056-109">Miljøet og Commerce Scale Unit (CSU) har nogle specifikke parametre, du skal bruge, når du forventer at klargøre dit e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="c3056-109">The environment and Commerce Scale Unit (CSU) also have some specific parameters that you must use when you expect to provision e-Commerce later.</span></span> <span data-ttu-id="c3056-110">Instruktionerne i dette emne beskriver alle de påkrævede trin for klargøring og de parametre, du skal bruge.</span><span class="sxs-lookup"><span data-stu-id="c3056-110">The instructions in this topic describe all the steps that are required to complete provisioning and the parameters that you must use.</span></span>

<span data-ttu-id="c3056-111">Nå du har klargjort dit Commerce-evalueringsmiljø, skal du fuldføre nogle få efter-klargørings-trin, for at gøre dit evalueringsmiljø klar til brug.</span><span class="sxs-lookup"><span data-stu-id="c3056-111">After you successfully provision your Commerce evaluation environment, you must complete a few post-provisioning steps to prepare it for use.</span></span> <span data-ttu-id="c3056-112">Nogle trin er valgfrie, afhængigt af de aspekter af systemet, du vil evaluere.</span><span class="sxs-lookup"><span data-stu-id="c3056-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="c3056-113">Du kan altid udføre de valgfrie trin senere.</span><span class="sxs-lookup"><span data-stu-id="c3056-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="c3056-114">For yderligere oplysninger om, hvordan du konfigurerer dit Commerce-evalueringsmiljø, efter du har klargjort det, se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="c3056-114">For information about how to configure your Commerce evaluation environment after you provision it, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="c3056-115">For yderligere oplysninger om, hvordan du konfigurerer valgfrie funktioner til dit Commerce-evalueringsmiljø, se [Konfigurere valgfrie funktioner til et Commerce-evalueringsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="c3056-115">For information about how to configure optional features for your Commerce evaluation environment, see [Configure optional features for a Commerce evaluation environment](cpe-optional-features.md).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="c3056-116">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="c3056-116">Prerequisites</span></span>

<span data-ttu-id="c3056-117">Følgende forudsætninger skal være på plads, før du kan klargør dit Commerce-evalueringsmiljø:</span><span class="sxs-lookup"><span data-stu-id="c3056-117">The following prerequisites must be in place before you can provision your Commerce evaluation environment:</span></span>

- <span data-ttu-id="c3056-118">Du er registreret i evalueringsprogrammet og har fået tildelt kapacitet til et evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="c3056-118">You have been onboarded into the evaluation program and granted capacity for an evaluation environment.</span></span>
- <span data-ttu-id="c3056-119">Du har adgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).</span><span class="sxs-lookup"><span data-stu-id="c3056-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="c3056-120">Du er en eksisterende Microsoft Dynamics 365-partner eller -kunde og kan oprette et Dynamics 365 Commerce-projekt.</span><span class="sxs-lookup"><span data-stu-id="c3056-120">You are an existing Microsoft Dynamics 365 partner or customer and are able to create a Dynamics 365 Commerce project.</span></span>
- <span data-ttu-id="c3056-121">Du har administratoradgang til dit Microsoft Azure-abonnement, eller du er i kontakt med en abonnementsadministrator, der kan hjælpe dig, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="c3056-121">You have administrator access to your Microsoft Azure subscription, or you're in contact with a subscription administrator who can assist you if required.</span></span>
- <span data-ttu-id="c3056-122">Du har dit Azure Active Directory-lejer-ID (Azure AD) ved hånden.</span><span class="sxs-lookup"><span data-stu-id="c3056-122">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="c3056-123">Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en systemadministratorgruppe til e-Commerce, og du har gruppens ID ved hånden.</span><span class="sxs-lookup"><span data-stu-id="c3056-123">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="c3056-124">Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en gruppe for redaktører af vurderinger og anmeldelser, og du har gruppens ID ved hånden.</span><span class="sxs-lookup"><span data-stu-id="c3056-124">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="c3056-125">(Denne sikkerhedsgruppe kan være den samme som e-Commerce-systemadministratorgruppen.)</span><span class="sxs-lookup"><span data-stu-id="c3056-125">(This security group can be the same as the e-Commerce system admin group.)</span></span>

<span data-ttu-id="c3056-126">Bemærk, at denne liste ikke er udtømmende.</span><span class="sxs-lookup"><span data-stu-id="c3056-126">Note that this list isn't exhaustive.</span></span> <span data-ttu-id="c3056-127">Hvis du oplever nogen problemer, skal du rette henvendelse til din kontakt hos din Microsoft-partner for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="c3056-127">If you experience any issues, reach out to your Microsoft partner contact for assistance.</span></span>

## <a name="provision-your-commerce-evaluation-environment"></a><span data-ttu-id="c3056-128">Klargøre dit Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="c3056-128">Provision your Commerce evaluation environment</span></span>

<span data-ttu-id="c3056-129">Disse procedurer forklarer, hvordan du klargør et Commerce-evalueringsmiljø.</span><span class="sxs-lookup"><span data-stu-id="c3056-129">These procedures explain how to provision a Commerce evaluation environment.</span></span> <span data-ttu-id="c3056-130">Når du har fuldført dem, vil Commerce-evalueringsmiljøet være klar til konfiguration.</span><span class="sxs-lookup"><span data-stu-id="c3056-130">After you successfully complete them, the Commerce evaluation environment will be ready for configuration.</span></span> <span data-ttu-id="c3056-131">Alle de aktiviteter, der er beskrevet her, finder sted på LCS-portalen.</span><span class="sxs-lookup"><span data-stu-id="c3056-131">All the activities that are described here occur in the LCS portal.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="c3056-132">Opret et nyt projekt</span><span class="sxs-lookup"><span data-stu-id="c3056-132">Create a new project</span></span>

<span data-ttu-id="c3056-133">Hvis du vil oprette et nyt projekt i LCS, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c3056-133">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="c3056-134">På LCS-startsiden skal du vælge plustegnet (**+**) for at oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="c3056-134">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="c3056-135">Benyt en af følgende fremgangsmåder i højre rude:</span><span class="sxs-lookup"><span data-stu-id="c3056-135">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="c3056-136">Hvis du er en partner, skal du vælge **Overflyt, opret løsninger, og lær at bruge**.</span><span class="sxs-lookup"><span data-stu-id="c3056-136">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="c3056-137">Hvis du er en kunde, skal du vælge **Mulige førsalg**.</span><span class="sxs-lookup"><span data-stu-id="c3056-137">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="c3056-138">Angiv et navn, beskrivelse og branche.</span><span class="sxs-lookup"><span data-stu-id="c3056-138">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="c3056-139">I feltet **Produktnavn** skal du vælge **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="c3056-139">In the **Product name** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="c3056-140">I feltet **Produktversion** skal du vælge **Dynamics 365 Commerce**.</span><span class="sxs-lookup"><span data-stu-id="c3056-140">In the **Product version** field, select **Dynamics 365 Commerce**.</span></span>
1. <span data-ttu-id="c3056-141">I feltet **Metode** skal du vælge **Dynamics Retail-implementeringsmetode**.</span><span class="sxs-lookup"><span data-stu-id="c3056-141">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="c3056-142">Valgfrit: Du kan importere roller og brugere fra et eksisterende projekt.</span><span class="sxs-lookup"><span data-stu-id="c3056-142">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="c3056-143">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="c3056-143">Select **Create**.</span></span> <span data-ttu-id="c3056-144">Projektoversigten vises.</span><span class="sxs-lookup"><span data-stu-id="c3056-144">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="c3056-145">Tilføj Azure Connector</span><span class="sxs-lookup"><span data-stu-id="c3056-145">Add the Azure Connector</span></span>

<span data-ttu-id="c3056-146">Hvis du vil føje Azure Connector til dit LCS-projekt, skal du følge trinnene i [Fuldføre processen til onboarding af Azure Resource Manager (ARM)](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span><span class="sxs-lookup"><span data-stu-id="c3056-146">To add the Azure Connector to your LCS project, follow the steps in [Complete the Azure Resource Manager (ARM) onboarding process](https://docs.microsoft.com/dynamics365/fin-ops-core/dev-itpro/deployment/arm-onboarding).</span></span>

### <a name="deploy-the-environment"></a><span data-ttu-id="c3056-147">Installer miljøet</span><span class="sxs-lookup"><span data-stu-id="c3056-147">Deploy the environment</span></span>

<span data-ttu-id="c3056-148">Følg disse trin for at installere miljøet.</span><span class="sxs-lookup"><span data-stu-id="c3056-148">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="c3056-149">Du behøver måske ikke at fuldføre trin 6, 7 og/eller 8, fordi sider, der har en enkelt indstilling, springes over.</span><span class="sxs-lookup"><span data-stu-id="c3056-149">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="c3056-150">Når du er i visningen **Miljøparametre**, skal du bekræfte, at teksten **Dynamics 365 Commerce - Demo (10.0.* x* med platformsopdatering *xx*)\*\* vises direkte over feltet **Miljønavn**.</span><span class="sxs-lookup"><span data-stu-id="c3056-150">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce - Demo (10.0.* x* with Platform update *xx*)\*\* appears directly above the **Environment name** field.</span></span> <span data-ttu-id="c3056-151">Se detaljer på den illustration, der vises efter trin 8.</span><span class="sxs-lookup"><span data-stu-id="c3056-151">For details, see the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="c3056-152">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="c3056-152">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="c3056-153">Vælg **Tilføj** for at tilføje et miljø.</span><span class="sxs-lookup"><span data-stu-id="c3056-153">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="c3056-154">Vælg den seneste version i feltet **Programversion**.</span><span class="sxs-lookup"><span data-stu-id="c3056-154">In the **Application version** field, select the most current version.</span></span> <span data-ttu-id="c3056-155">Hvis du har et specifikt behov for at vælge en anden programversion end den seneste version, skal du ikke vælge en version før **10.0.14**.</span><span class="sxs-lookup"><span data-stu-id="c3056-155">If you have a specific need to select an application version other than the most current version, do not select a version prior to **10.0.14**.</span></span>
1. <span data-ttu-id="c3056-156">I feltet **Platformsversion** skal du bruge den platformsversion, der automatisk vælges for den programversion, du har valgt.</span><span class="sxs-lookup"><span data-stu-id="c3056-156">In the **Platform version** field, use the platform version that is automatically chosen for the application version you selected.</span></span> 

    ![Valg af program- og platformsversioner](./media/project1.png)

1. <span data-ttu-id="c3056-158">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="c3056-158">Select **Next**.</span></span>
1. <span data-ttu-id="c3056-159">Vælg **Demo** miljøtopologi.</span><span class="sxs-lookup"><span data-stu-id="c3056-159">Select **Demo** as the environment topology.</span></span>

    ![Valg af miljøtopologi 1](./media/project2.png)

1. <span data-ttu-id="c3056-161">Angiv et miljønavn på side **Installer miljø**.</span><span class="sxs-lookup"><span data-stu-id="c3056-161">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="c3056-162">Lad de avancerede indstillinger være, som de er.</span><span class="sxs-lookup"><span data-stu-id="c3056-162">Leave the advanced settings as they are.</span></span>

    ![Siden Installer miljø](./media/project4.png)

1. <span data-ttu-id="c3056-164">Juster VM-størrelsen efter behov.</span><span class="sxs-lookup"><span data-stu-id="c3056-164">Adjust the VM size as required.</span></span> <span data-ttu-id="c3056-165">(Vi anbefaler, at VM-lagerenheden \[SKU\] **D13 V2**.)</span><span class="sxs-lookup"><span data-stu-id="c3056-165">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="c3056-166">Gennemgå prissætnings- og licensvilkårene, og markér derefter afkrydsningsfeltet for at angive, at du accepterer dem.</span><span class="sxs-lookup"><span data-stu-id="c3056-166">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="c3056-167">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="c3056-167">Select **Next**.</span></span>
1. <span data-ttu-id="c3056-168">Klik på **Installer** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.</span><span class="sxs-lookup"><span data-stu-id="c3056-168">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="c3056-169">Du bliver sendt tilbage til visningen **Skybaserede miljøer**, og dit miljø skulle stå på listen.</span><span class="sxs-lookup"><span data-stu-id="c3056-169">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="c3056-170">Det miljø, du har anmodet om, vil blive vist i køen og derefter som under installation.</span><span class="sxs-lookup"><span data-stu-id="c3056-170">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="c3056-171">Det vil tage nogen tid at fuldføre miljø arbejdsgangene.</span><span class="sxs-lookup"><span data-stu-id="c3056-171">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="c3056-172">Kom derfor tilbage efter ca. seks til ni timer.</span><span class="sxs-lookup"><span data-stu-id="c3056-172">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="c3056-173">Før du fortsætter, skal du kontrollere, at din statussen for dit miljø er **Installeret**.</span><span class="sxs-lookup"><span data-stu-id="c3056-173">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-the-commerce-scale-unit-cloud"></a><span data-ttu-id="c3056-174">Initialisere Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="c3056-174">Initialize the Commerce Scale Unit (cloud)</span></span>

<span data-ttu-id="c3056-175">Følg disse trin for at påbegynde CSU'en.</span><span class="sxs-lookup"><span data-stu-id="c3056-175">To initialize the CSU, follow these steps.</span></span>

1. <span data-ttu-id="c3056-176">Vælg dit miljø på listen i visningen **Skybaserede miljøer**.</span><span class="sxs-lookup"><span data-stu-id="c3056-176">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="c3056-177">Vælg **Alle detaljer** i miljøvisningen til højre.</span><span class="sxs-lookup"><span data-stu-id="c3056-177">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="c3056-178">Visningen med miljødetaljer vises.</span><span class="sxs-lookup"><span data-stu-id="c3056-178">The environment details view appears.</span></span>
1. <span data-ttu-id="c3056-179">Under **Miljøfunktioner** skal du vælge **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="c3056-179">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="c3056-180">På fanen **Commerce** skal du vælge **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="c3056-180">On the **Commerce** tab, select **Initialize**.</span></span> <span data-ttu-id="c3056-181">CSU-initialiseringsparametrene bliver vist.</span><span class="sxs-lookup"><span data-stu-id="c3056-181">The CSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="c3056-182">I feltet **Område** skal du vælge det område, der er det samme eller tæt på det område, du har implementeret miljøet i.</span><span class="sxs-lookup"><span data-stu-id="c3056-182">In the **Region** field, select the region that is the same or close to the region that you deployed the environment to.</span></span>
1. <span data-ttu-id="c3056-183">Lad feltet **Version** være, som det er.</span><span class="sxs-lookup"><span data-stu-id="c3056-183">Leave the **Version** field as it is.</span></span>
1. <span data-ttu-id="c3056-184">Vælg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="c3056-184">Select **Initialize**.</span></span>
1. <span data-ttu-id="c3056-185">Klik på **Ja** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.</span><span class="sxs-lookup"><span data-stu-id="c3056-185">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="c3056-186">Visningen **Commerce-administration** vises igen, hvor fanen **Commerce** er valgt.</span><span class="sxs-lookup"><span data-stu-id="c3056-186">The **Commerce management** view displays again, where the **Commerce** tab is selected.</span></span> <span data-ttu-id="c3056-187">Din CSU er sat i kø til klargøring.</span><span class="sxs-lookup"><span data-stu-id="c3056-187">Your CSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="c3056-188">Før du fortsætter, skal du kontrollere, at din statussen for dit CSU er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="c3056-188">Before you continue, make sure that the status of your CSU is **Success**.</span></span> <span data-ttu-id="c3056-189">Initialiseringen tager ca. to til fem timer.</span><span class="sxs-lookup"><span data-stu-id="c3056-189">Initialization takes approximately two to five hours.</span></span>

<span data-ttu-id="c3056-190">Hvis du ikke kan finde linket **Administrer** i miljødetaljevisningen, skal du kontakte din Microsoft-kontaktperson for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="c3056-190">If you can't find the **Manage** link in the environment details view, reach out to your Microsoft contact for assistance.</span></span>

<span data-ttu-id="c3056-191">Du kan få vist følgende fejlmeddelelse under første implementeringsprocessen:</span><span class="sxs-lookup"><span data-stu-id="c3056-191">During the deployment process, you might receive the following error message:</span></span>

> <span data-ttu-id="c3056-192">Evalueringsmiljøer (demo/test)-miljøer skal registrere programmet skalaenheds-connector \<application ID\> i headquarters.</span><span class="sxs-lookup"><span data-stu-id="c3056-192">Evaluation (demo/test) environments need to register the scale unit connector application \<application ID\> in headquarters.</span></span>

<span data-ttu-id="c3056-193">Hvis CSU-initialiseringen mislykkes, og du modtager denne fejlmeddelelse, skal du notere program-id, da det er et globalt entydigt id (GUID), og derefter følge trinnene i næste afsnit for at registrere CSU-implementeringsapplikationen i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="c3056-193">If the CSU initialization fails and you receive this error message, make a note of the application ID, which is a globally unique identifier (GUID), and then follow the steps in the next section to register the CSU deployment application in Commerce headquarters.</span></span>

### <a name="register-the-csu-deployment-application-in-commerce-headquarters-if-required"></a><span data-ttu-id="c3056-194">Registrer CSU-implementeringsapplikationen i Commerce Headquarters (hvis det er nødvendigt)</span><span class="sxs-lookup"><span data-stu-id="c3056-194">Register the CSU deployment application in Commerce headquarters (if required)</span></span>

<span data-ttu-id="c3056-195">Følg disse trin for at registrere CSU-implementeringsapplikationen i Commerce Headquarters.</span><span class="sxs-lookup"><span data-stu-id="c3056-195">To register the CSU deployment application in Commerce headquarters, follow these steps.</span></span>

1. <span data-ttu-id="c3056-196">I Commerce Headquarters skal du gå til **Systemadministration \> Opsætning \> Azure Active Directory-applikationer**.</span><span class="sxs-lookup"><span data-stu-id="c3056-196">In Commerce headquarters, go to **System administration \> Setup \> Azure Active Directory applications**.</span></span>
1. <span data-ttu-id="c3056-197">I kolonnen **Klient-id** skal du angive applikations-id fra den fejlmeddelelse for CSU-initialisering, du har modtaget.</span><span class="sxs-lookup"><span data-stu-id="c3056-197">In the **Client Id** column, enter the application ID from the CSU initialization error message that you received.</span></span>
1. <span data-ttu-id="c3056-198">Angiv en beskrivende tekst i kolonnen **Navn** (f.eks. **CSU Eval**).</span><span class="sxs-lookup"><span data-stu-id="c3056-198">In the **Name** column, enter any descriptive text (for example, **CSU Eval**).</span></span>
1. <span data-ttu-id="c3056-199">Angiv **RetailServiceAccount** i kolonnen **Bruger-id**.</span><span class="sxs-lookup"><span data-stu-id="c3056-199">In the **User ID** column, enter **RetailServiceAccount**.</span></span>
1. <span data-ttu-id="c3056-200">Ny forsøg på at initialisere CSU og installere fra LCS.</span><span class="sxs-lookup"><span data-stu-id="c3056-200">Retry the CSU initialization and deployment from LCS.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="c3056-201">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="c3056-201">Initialize e-Commerce</span></span>

<span data-ttu-id="c3056-202">Følg disse trin for at påbegynde e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="c3056-202">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="c3056-203">Under fanen **e-Commerce** skal du gennemgå samtykket for evalueringen og derefter vælge **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c3056-203">On the **e-Commerce** tab, review the evaluation consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="c3056-204">Angiv et navn for **e-Commerce-miljønavn** i feltet.</span><span class="sxs-lookup"><span data-stu-id="c3056-204">In the **e-Commerce environment name** field, enter a name.</span></span> <span data-ttu-id="c3056-205">Vær opmærksom på, at navnet vil være synligt i nogle af URL-adresserne, der peger på din e-Commerce-forekomst.</span><span class="sxs-lookup"><span data-stu-id="c3056-205">Be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="c3056-206">I feltet **Commerce Scale Unit-navn** skal du vælge din CSU på listen.</span><span class="sxs-lookup"><span data-stu-id="c3056-206">In the **Commerce Scale Unit name** field, select your CSU in the list.</span></span> <span data-ttu-id="c3056-207">(Listen bør kun have én indstilling.)</span><span class="sxs-lookup"><span data-stu-id="c3056-207">(The list should have only one option.)</span></span>

    <span data-ttu-id="c3056-208">Feltet **e-Commerce-geografi** indstilles automatisk.</span><span class="sxs-lookup"><span data-stu-id="c3056-208">The **e-Commerce geography** field is set automatically.</span></span>

1. <span data-ttu-id="c3056-209">Vælg **Næste** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="c3056-209">Select **Next** to continue.</span></span>
1. <span data-ttu-id="c3056-210">I feltet **Understøttede værtsnavne** skal du angive et vilkårligt gyldigt domæne som f.eks. `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="c3056-210">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1. <span data-ttu-id="c3056-211">I feltet **ADD-sikkerhedsgruppe for systemadministratorer** skal du angive de første par bogstaver i navnet på den sikkerhedsgruppe, du vil bruge, og derefter vælge symbolet for forstørrelsesglas for at få vist søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="c3056-211">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="c3056-212">Vælg den korrekte sikkerhedsgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="c3056-212">Select the correct security group in the list.</span></span>
1.  <span data-ttu-id="c3056-213">I feltet **ADD-sikkerhedsgruppe for vurderings- og anmeldelsesadministratorer** skal du angive de første par bogstaver i navnet på den sikkerhedsgruppe, du vil bruge, og derefter vælge symbolet for forstørrelsesglas for at få vist søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="c3056-213">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use, and then select the magnifying glass symbol to view the search results.</span></span> <span data-ttu-id="c3056-214">Vælg den korrekte sikkerhedsgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="c3056-214">Select the correct security group in the list.</span></span>
1. <span data-ttu-id="c3056-215">Vælg **Ja** i indstillingen **Aktivér vurderinger og anmeldelser**.</span><span class="sxs-lookup"><span data-stu-id="c3056-215">Leave the **Enable ratings and review service** option set to **Yes**.</span></span>
1. <span data-ttu-id="c3056-216">Vælg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="c3056-216">Select **Initialize**.</span></span> <span data-ttu-id="c3056-217">Visningen **Commerce-administration** vises igen, hvor fanen **e-Commerce** er valgt.</span><span class="sxs-lookup"><span data-stu-id="c3056-217">The **Commerce management** view displays again, where the **e-Commerce** tab is selected.</span></span> <span data-ttu-id="c3056-218">Din initialisering af e-Commerce er påbegyndt.</span><span class="sxs-lookup"><span data-stu-id="c3056-218">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="c3056-219">Før du fortsætter, skal du vente, indtil initialiseringsstatus for din e-Commerce er **Initialisering blev gennemført**.</span><span class="sxs-lookup"><span data-stu-id="c3056-219">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="c3056-220">Under **Links** nederst til højre skal du notere URL-adresserne for følgende links:</span><span class="sxs-lookup"><span data-stu-id="c3056-220">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="c3056-221">**e-Commerce-websted** – linket til roden af dit e-Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="c3056-221">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="c3056-222">**Commerce-webstedsgenerator** – linket til administrationsværktøjet for webstedet.</span><span class="sxs-lookup"><span data-stu-id="c3056-222">**Commerce site builder** – The link to the site management tool.</span></span>

## <a name="next-steps"></a><span data-ttu-id="c3056-223">Næste trin</span><span class="sxs-lookup"><span data-stu-id="c3056-223">Next steps</span></span>

<span data-ttu-id="c3056-224">For at fortsætte processen med klargøring og konfigurering af dit Commerce-evalueringsmiljø se [Konfigurere et Commerce-evalueringsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="c3056-224">To continue the process of provisioning and configuring your Commerce evaluation environment, see [Configure a Commerce evaluation environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c3056-225">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c3056-225">Additional resources</span></span>

[<span data-ttu-id="c3056-226">Oversigt over Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="c3056-226">Dynamics 365 Commerce evaluation environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="c3056-227">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="c3056-227">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="c3056-228">Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="c3056-228">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="c3056-229">Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="c3056-229">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="c3056-230">Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="c3056-230">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="c3056-231">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="c3056-231">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="c3056-232">Commerce Scale Unit (sky)</span><span class="sxs-lookup"><span data-stu-id="c3056-232">Commerce Scale Unit (cloud)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="c3056-233">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="c3056-233">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="c3056-234">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="c3056-234">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
