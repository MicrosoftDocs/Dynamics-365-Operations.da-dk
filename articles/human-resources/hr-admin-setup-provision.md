---
title: Klargøring af Personale
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f3a7987a9b385fb6ba0294dc46b0d66be8228f06
ms.sourcegitcommit: 829329220475ed8cff5a5db92a59dd90c22b04fa
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/05/2020
ms.locfileid: "3026261"
---
# <a name="provision-human-resources"></a><span data-ttu-id="715a0-102">Klargøring af Personale</span><span class="sxs-lookup"><span data-stu-id="715a0-102">Provision Human Resources</span></span>

<span data-ttu-id="715a0-103">Denne artikel fører dig gennem processen med at klargøre et nyt produktionsmiljø til Microsoft Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="715a0-103">This article walks you through the process of provisioning a new production environment for Microsoft Dynamics 365 Human Resources.</span></span> <span data-ttu-id="715a0-104">Det antages i artiklen, at du har købt Personale via en Cloud Solution Provider (CSP) eller en EA-aftale (Enterprise Architecture).</span><span class="sxs-lookup"><span data-stu-id="715a0-104">This article assumes that you've purchased Human Resources through a Cloud Solution Provider (CSP) or enterprise architecture (EA) agreement.</span></span> <span data-ttu-id="715a0-105">Hvis du har en eksisterende Microsoft Dynamics 365-licens, der allerede indeholder Personale-serviceplanen, og du ikke kan udføre trinnene i denne artikel, kan du kontakte Support.</span><span class="sxs-lookup"><span data-stu-id="715a0-105">If you have an existing Microsoft Dynamics 365 license that already includes the Human Resources service plan, and you can't complete the steps in this article, contact Support.</span></span>

<span data-ttu-id="715a0-106">For at komme i gang skal den globale administrator logge på [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) og oprette et nyt Personale-projekt.</span><span class="sxs-lookup"><span data-stu-id="715a0-106">To begin, the global administrator should sign in to [Microsoft Dynamics Lifecycle Services](https://lcs.dynamics.com) (LCS) and create a new Human Resources project.</span></span> <span data-ttu-id="715a0-107">Medmindre et problem med licensering forhindrer klargøring af Personale, skulle der ikke være brug for hjælp fra Support- eller DSE-medarbejdere (Dynamics Service Engineering).</span><span class="sxs-lookup"><span data-stu-id="715a0-107">Unless a licensing issue prevents you from provisioning Human Resource, assistance from Support or Dynamics Service Engineering (DSE) representatives isn't required.</span></span>

## <a name="create-an-lcs-project"></a><span data-ttu-id="715a0-108">Oprette et LCS-projekt</span><span class="sxs-lookup"><span data-stu-id="715a0-108">Create an LCS project</span></span>

<span data-ttu-id="715a0-109">Når du vil bruge LCS til at administrere dine Personale-miljøer, skal du først oprette et LCS-projekt.</span><span class="sxs-lookup"><span data-stu-id="715a0-109">To use LCS to manage your Human Resources environments, you must first create an LCS project.</span></span>

1. <span data-ttu-id="715a0-110">Log på [LCS](https://lcs.dynamics.com/Logon/Index) ved hjælp af den konto, som du brugte til dit abonnement på Personale.</span><span class="sxs-lookup"><span data-stu-id="715a0-110">Sign in to [LCS](https://lcs.dynamics.com/Logon/Index) by using the account that you used to subscribe to Human Resources.</span></span>

2. <span data-ttu-id="715a0-111">Markér plustegnet (**+**) for at oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="715a0-111">Select the plus sign (**+**) to create a project.</span></span>

3. <span data-ttu-id="715a0-112">Vælg **Microsoft Dynamics 365 Human Resources** som produktnavn og -version.</span><span class="sxs-lookup"><span data-stu-id="715a0-112">Select **Microsoft Dynamics 365 Human Resources** as the product name and product version.</span></span>

4. <span data-ttu-id="715a0-113">Vælg **Dynamics 365 Human Resources**-metoden.</span><span class="sxs-lookup"><span data-stu-id="715a0-113">Select the **Dynamics 365 Human Resources** methodology.</span></span>

5. <span data-ttu-id="715a0-114">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="715a0-114">Select **Create**.</span></span>

<span data-ttu-id="715a0-115">Du kan finde oplysninger om, hvordan du kommer i gang med Personale, i den **Personale**-metode, du oprettede i det nye projekt.</span><span class="sxs-lookup"><span data-stu-id="715a0-115">For information about how to get started with Human Resources, see the **Human Resources** methodology that you created in your new project.</span></span> <span data-ttu-id="715a0-116">Når du er færdig med at oprette projektet, skal du udføre følgende procedure for at klargøre Personale-miljøet.</span><span class="sxs-lookup"><span data-stu-id="715a0-116">After you've finished creating the project, complete the following procedure to provision your Human Resources environment.</span></span>

## <a name="provision-a-human-resources-project"></a><span data-ttu-id="715a0-117">Klargøring af et Personale-projekt</span><span class="sxs-lookup"><span data-stu-id="715a0-117">Provision a Human Resources project</span></span>

<span data-ttu-id="715a0-118">Når du har oprettet et LCS-projekt, kan du klargøre Personale i et miljø.</span><span class="sxs-lookup"><span data-stu-id="715a0-118">After you've created an LCS project, you can provision Human Resources into an environment.</span></span>

1. <span data-ttu-id="715a0-119">I LCS-projektet skal du vælge feltet **Administration af Personale-app**.</span><span class="sxs-lookup"><span data-stu-id="715a0-119">In your LCS project, select the **Human Resources App Management** tile.</span></span>

2. <span data-ttu-id="715a0-120">Angiv, om dette er en sandkasse- eller produktionsforekomst af Personale.</span><span class="sxs-lookup"><span data-stu-id="715a0-120">Indicate whether this is a Sandbox or Production instance of Human Resource.</span></span> <span data-ttu-id="715a0-121">De tidlige visningsfunktioner kan være tilgængelige i sandkasseforekomster med henblik på hurtig feedback og test.</span><span class="sxs-lookup"><span data-stu-id="715a0-121">Early preview features may be available in Sandbox instances to allow for early feedback and testing.</span></span>
   
    > [!NOTE]
    > <span data-ttu-id="715a0-122">Talent-forekomsttypen kan ikke ændres, når den først er angivet.</span><span class="sxs-lookup"><span data-stu-id="715a0-122">The Talent instance type cannot be changed once set.</span></span> <span data-ttu-id="715a0-123">Kontrollér, at den korrekte forekomsttype er valgt, før du fortsætter.</span><span class="sxs-lookup"><span data-stu-id="715a0-123">Verify the correct instance type is selected before continuing.</span></span></br></br>
    > <span data-ttu-id="715a0-124">Personale-forekomsttypen er adskilt fra den forekomsttype for Microsoft Power Apps-miljøet, som du angiver i Power Apps Administration.</span><span class="sxs-lookup"><span data-stu-id="715a0-124">The Human Resources instance type is separate from the instance type of the Microsoft Power Apps environment, which you set in the Power Apps Admin center.</span></span>
    
3. <span data-ttu-id="715a0-125">Vælg indstillingen **Inkluder demodata**, hvis du ønsker, at dit miljø skal medtage det demodatasæt, der bruges af Testdrev til Personale-oplevelsen.</span><span class="sxs-lookup"><span data-stu-id="715a0-125">Select the **Include Demo Data** option if you want your environment to include the same demo data set used in the Human Resources Test Drive experience.</span></span> <span data-ttu-id="715a0-126">Dette er en fordel for langsigtede demo- eller uddannelsesmiljøer og skal aldrig bruges til produktionsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="715a0-126">This is beneficial for long-term demo or training environments, and should never be used for production environments.</span></span>  <span data-ttu-id="715a0-127">Bemærk, at du skal vælge denne indstilling ved første installation.</span><span class="sxs-lookup"><span data-stu-id="715a0-127">Note that you must choose this option upon initial deployment.</span></span> <span data-ttu-id="715a0-128">Du kan ikke efterfølgende opdatere en eksisterende installation.</span><span class="sxs-lookup"><span data-stu-id="715a0-128">You cannot update an existing deployment later.</span></span>

4. <span data-ttu-id="715a0-129">Personale klargøres altid i et Microsoft Power Apps-miljø for at aktivere Power Apps-integration og -udvidelse.</span><span class="sxs-lookup"><span data-stu-id="715a0-129">Human Resources is always provisioned into a Microsoft Power Apps environment to enable Power Apps integration and extensibility.</span></span> <span data-ttu-id="715a0-130">Læs afsnittet "Valg af et Power Apps-miljø" i denne artikel, før du fortsætter.</span><span class="sxs-lookup"><span data-stu-id="715a0-130">Read the “Selecting a Power Apps environment” section of this article before you continue.</span></span> <span data-ttu-id="715a0-131">Hvis du ikke allerede har et Power Apps-miljø, skal du vælge "Administrer miljøer i LCS" eller navigere til Power Apps Administration.</span><span class="sxs-lookup"><span data-stu-id="715a0-131">If you don't already have a Power Apps environment, select Manage environments in LCS or navigate to the Power Apps Admin center.</span></span> <span data-ttu-id="715a0-132">Følg derefter trinnene for at [Oprette et Power Apps-miljø](https://docs.microsoft.com/powerapps/administrator/create-environment).</span><span class="sxs-lookup"><span data-stu-id="715a0-132">Then follow the steps to [Create a Power Apps environment](https://docs.microsoft.com/powerapps/administrator/create-environment).</span></span>

    > [!NOTE]
    > <span data-ttu-id="715a0-133">For at få vist eksisterende miljøer eller oprette nye miljøer skal den lejeradministrator, der klargør Personale, være tildelt Power Apps P2-licensen.</span><span class="sxs-lookup"><span data-stu-id="715a0-133">To view existing environments or create new environments, the tenant admin who provisions Human Resources must be assigned to the Power Apps P2 license.</span></span> <span data-ttu-id="715a0-134">Hvis organisationen ikke har en Power Apps P2-licens, kan du få en fra din Cloud Solution Provider eller fra [Power Apps-prissætningssiden](https://powerapps.microsoft.com/pricing/).</span><span class="sxs-lookup"><span data-stu-id="715a0-134">If your organization doesn't have a Power Apps P2 license, you can get one from your CSP or from the [Power Apps pricing page](https://powerapps.microsoft.com/pricing/).</span></span>

5. <span data-ttu-id="715a0-135">Vælg det miljø, du vil klargøre Personale til.</span><span class="sxs-lookup"><span data-stu-id="715a0-135">Select the environment to provision Human Resources into.</span></span>

6. <span data-ttu-id="715a0-136">Vælg **Ja** for at acceptere vilkårene og begynde installationen.</span><span class="sxs-lookup"><span data-stu-id="715a0-136">Select **Yes** to agree to the terms and begin deployment.</span></span>

   <span data-ttu-id="715a0-137">Det nye miljø vises på listen over miljøer i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="715a0-137">Your new environment appears in the list of environments in the navigation pane on the left.</span></span> <span data-ttu-id="715a0-138">Men du kan ikke begynde at bruge miljøet, før installationsstatus er opdateret til **Installeret**.</span><span class="sxs-lookup"><span data-stu-id="715a0-138">However, you can't start to use the environment until the deployment status is updated to **Deployed**.</span></span> <span data-ttu-id="715a0-139">Denne proces tager typisk få minutter.</span><span class="sxs-lookup"><span data-stu-id="715a0-139">This process typically takes a few minutes.</span></span> <span data-ttu-id="715a0-140">Hvis klargøringsprocessen mislykkes, skal du kontakte Support.</span><span class="sxs-lookup"><span data-stu-id="715a0-140">If the provisioning process is unsuccessful, you must contact Support.</span></span>

7. <span data-ttu-id="715a0-141">Vælg **Log på Personale** for at bruge det nye miljø.</span><span class="sxs-lookup"><span data-stu-id="715a0-141">Select **Log on to Human Resource** to use your new environment.</span></span>

    > [!NOTE]
    > <span data-ttu-id="715a0-142">Hvis du endnu ikke har godkendt de endelige krav, kan du installere en testforekomst af Personale i projektet.</span><span class="sxs-lookup"><span data-stu-id="715a0-142">If you haven't yet signed off on the final requirements, you can deploy a test instance of Human Resources in the project.</span></span> <span data-ttu-id="715a0-143">Du kan derefter bruge denne forekomst til at teste din løsning, indtil du kan godkende den.</span><span class="sxs-lookup"><span data-stu-id="715a0-143">You can then use this instance to test your solution until you sign off.</span></span> <span data-ttu-id="715a0-144">Hvis du bruger det nye miljø til test, skal du gentage denne procedure for at oprette et produktionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="715a0-144">If you use your new environment for testing, you must repeat this procedure to create a production environment.</span></span>

    > <span data-ttu-id="715a0-145">Da kun to LCS-miljøer er tilladt som en del af Personale-abonnementet, kan du også overveje at benytte dig af et gratis 60-dages [Personale-forsøgsmiljø](https://dynamics.microsoft.com/talent/overview/).</span><span class="sxs-lookup"><span data-stu-id="715a0-145">Because only two LCS environments are allowed as part of the Human Resources subscription, you might consider leveraging a free 60-day [Human Resources trial environment](https://dynamics.microsoft.com/talent/overview/).</span></span> <span data-ttu-id="715a0-146">Selvom et forsøgsmiljø ejes af den bruger, der har anmodet om det, kan andre brugere inviteres gennem systemadministrationsoplevelsen i Personale.</span><span class="sxs-lookup"><span data-stu-id="715a0-146">Although a trial environment is owned by the user who requested it, other users can be invited through the system administration experience for Human Resources.</span></span> <span data-ttu-id="715a0-147">Forsøgsmiljøer indeholder fiktive data, der kan bruges til at udforske programmet på en sikker måde.</span><span class="sxs-lookup"><span data-stu-id="715a0-147">Trial environments contain fictitious data that can be used to explore the program in a safe manner.</span></span> <span data-ttu-id="715a0-148">De ikke er beregnet til brug som produktionsmiljøer.</span><span class="sxs-lookup"><span data-stu-id="715a0-148">They aren't intended to be used as production environments.</span></span> <span data-ttu-id="715a0-149">Bemærk, at når et forsøgsmiljø udløber efter 60 dage, slettes alle data i det, og de kan ikke gendannes.</span><span class="sxs-lookup"><span data-stu-id="715a0-149">Note that when a trial environment expires after 60 days, all the data that's in it is deleted and can't be recovered.</span></span> <span data-ttu-id="715a0-150">Du kan tilmelde dig til et nyt forsøgsmiljø, når det eksisterende miljø udløber.</span><span class="sxs-lookup"><span data-stu-id="715a0-150">You can sign up for a new trial environment after the existing environment expires.</span></span>

## <a name="select-a-power-apps-environment"></a><span data-ttu-id="715a0-151">Vælg et Power Apps-miljø</span><span class="sxs-lookup"><span data-stu-id="715a0-151">Select a Power Apps environment</span></span>

<span data-ttu-id="715a0-152">Integrationen mellem Personale- og Power Apps-miljøerne gør det muligt for dig at integrere og udvide brugen af Personale-data ved hjælp af Power Apps-værktøjer.</span><span class="sxs-lookup"><span data-stu-id="715a0-152">The integration between Human Resources and the Power Apps environments lets you integrate and extend the use of Human Resources data using Power Apps tools.</span></span> <span data-ttu-id="715a0-153">Forståelse af formålet med Power Apps-miljøer vil ikke blot hjælpe dig med at udvikle apps med henblik på at udvide Personale, men vil også hjælpe dig med at vælge det korrekte miljø i forbindelse med klargøringen af Personale.</span><span class="sxs-lookup"><span data-stu-id="715a0-153">Understanding the purpose of Power Apps environments will not only help you build apps to extend Human Resource, but will also help you select the correct environment when provisioning Human Resource.</span></span> <span data-ttu-id="715a0-154">Du kan finde oplysninger om Power Apps-miljøer, herunder omfanget af miljøet, adgang til miljøet og oprettelse og valg af et miljø, under [Annoncering af Power Apps-miljøer](https://powerapps.microsoft.com/blog/powerapps-environments/).</span><span class="sxs-lookup"><span data-stu-id="715a0-154">For information about Power Apps environments, including environment scope, environment access, and creating and choosing an environment, see [Announcing Power Apps environments](https://powerapps.microsoft.com/blog/powerapps-environments/).</span></span> 

<span data-ttu-id="715a0-155">Brug følgende retningslinjer til fastsættelse af, hvilket Power Apps-miljø som Personale skal installeres i:</span><span class="sxs-lookup"><span data-stu-id="715a0-155">Use the following guidance when determining which Power Apps environment to deploy Human Resources into:</span></span> 

1. <span data-ttu-id="715a0-156">I LCS skal du vælge **Administrer miljøer** eller gå direkte til Power Apps Administration, hvor du kan få vist eksisterende miljøer og oprette nye miljøer.</span><span class="sxs-lookup"><span data-stu-id="715a0-156">In LCS, select **Manage environments**, or go directly to the Power Apps Admin center where you can view existing environments and create new environments.</span></span>

2. <span data-ttu-id="715a0-157">Der er knyttet et enkelt Personale-miljø til et enkelt Power Apps-miljø.</span><span class="sxs-lookup"><span data-stu-id="715a0-157">A single Human Resources environment is mapped to a single Power Apps environment.</span></span>

3. <span data-ttu-id="715a0-158">Et Power Apps-miljø indeholder Personale sammen med de tilsvarende Power Apps-, Power Automate- og Common Data Service-programmer.</span><span class="sxs-lookup"><span data-stu-id="715a0-158">A Power Apps environment contains Human Resources, along with the corresponding Power Apps, Power Automate, and Common Data Service applications.</span></span> <span data-ttu-id="715a0-159">Hvis Power Apps-miljøet slettes, så slettes apps i det samtidig.</span><span class="sxs-lookup"><span data-stu-id="715a0-159">If the Power Apps environment is deleted, so are the apps within it.</span></span> <span data-ttu-id="715a0-160">Under klargøring af et Personale-miljø kan enten et **Prøveversion**- eller **Produktion**-miljø klargøres.</span><span class="sxs-lookup"><span data-stu-id="715a0-160">When provisioning a Human Resources environment, you can provision either a **Trial** or **Production** environment.</span></span> <span data-ttu-id="715a0-161">Vælg den ønskede type miljø baseret på, hvordan miljøet skal bruges.</span><span class="sxs-lookup"><span data-stu-id="715a0-161">Choose the type of environment based on how the environment will be used.</span></span> 

4. <span data-ttu-id="715a0-162">Dataintegration og teststrategier, såsom Sandkasse, UAT eller Produktion, bør tages i betragtning.</span><span class="sxs-lookup"><span data-stu-id="715a0-162">Data integration and testing strategies should be considered, such as Sandbox, UAT, or Production.</span></span> <span data-ttu-id="715a0-163">Vi anbefaler, at du overvejer de forskellige konsekvenser af din installation, da det ikke er let at ændre tilknytningen af Personale-miljøer til et Power Apps-miljø senere.</span><span class="sxs-lookup"><span data-stu-id="715a0-163">We recommend that you consider the various implications for your deployment, because it isn't easy to later change which Human Resources environment is mapped to a Power Apps environment.</span></span>

5. <span data-ttu-id="715a0-164">Følgende Power Apps-miljøer kan ikke bruges til Personale og filtreres fra valglisten i LCS:</span><span class="sxs-lookup"><span data-stu-id="715a0-164">The following Power Apps environments cannot be used for Human Resources and will be filtered from the selection list within LCS:</span></span>
 
    - <span data-ttu-id="715a0-165">**Power Apps-standardmiljøer** ‑ Selvom hver lejer automatisk klargøres med et Power Apps-standardmiljø, anbefales det ikke at bruge dem sammen med Personale, da alle lejerbrugere har adgang til Power Apps-miljøet og derfor utilsigtet kan beskadige produktionsdata i forbindelse med test og gennemsyn af Power Apps- eller Power Automate-integrationer.</span><span class="sxs-lookup"><span data-stu-id="715a0-165">**Default Power Apps environments** - Although each tenant is automatically provisioned with a default Power Apps environment, we don't recommend using them with Human Resources because all tenant users have access to the Power Apps environment and could unintentionally corrupt production data when testing and exploring with Power Apps or Power Automate integrations.</span></span>
   
    - <span data-ttu-id="715a0-166">**Testmiljøer** ‑ Disse miljøer oprettes med en udløbsdato og udløber efter dette tidspunkt, hvilket resulterer i, at dit miljø og enhver Personale-forekomst, der er indeholdt heri, automatisk bliver fjernet.</span><span class="sxs-lookup"><span data-stu-id="715a0-166">**Trial environments** - These environments are created with an expiration date and will expire after that time, causing your environment and any Human Resources instances contained within to be removed automatically.</span></span>
   
    - <span data-ttu-id="715a0-167">**Ikke-understøttede områder** - I øjeblikket understøttes Personale kun i følgende områder: USA, Europa, Storbritannien, Australien, Canada og Asien.</span><span class="sxs-lookup"><span data-stu-id="715a0-167">**Unsupported regions** - Currently Human Resources is only supported in the following regions: United States, Europe, United Kingdom, Australia, Canada and Asia.</span></span>
  
6. <span data-ttu-id="715a0-168">Når du har besluttet, hvilket miljø der er bedst at anvende, kan du fortsætte klargøringsprocessen.</span><span class="sxs-lookup"><span data-stu-id="715a0-168">After you have determined the correct environment to use, you can continue with the provisioning process.</span></span> 
 
## <a name="grant-access-to-the-environment"></a><span data-ttu-id="715a0-169">Give adgang til miljøet</span><span class="sxs-lookup"><span data-stu-id="715a0-169">Grant access to the environment</span></span>

<span data-ttu-id="715a0-170">Som standard har den globale administrator, der oprettede miljøet, adgang til det.</span><span class="sxs-lookup"><span data-stu-id="715a0-170">By default, the global administrator who created the environment has access to it.</span></span> <span data-ttu-id="715a0-171">Men andre programbrugere skal eksplicit tildeles adgang.</span><span class="sxs-lookup"><span data-stu-id="715a0-171">However, additional application users must be explicitly granted access.</span></span> <span data-ttu-id="715a0-172">For at give adgang skal du tilføje brugere og tildele dem de relevante roller i Personale-miljøet.</span><span class="sxs-lookup"><span data-stu-id="715a0-172">To grant access, you need to add users and assign the appropriate roles to them in the Human Resources environment.</span></span> <span data-ttu-id="715a0-173">Den globale administrator, der installerede Personale, skal også starte både Attract og Onboard for at fuldføre initialiseringen og aktivere adgang for andre lejerbrugere.</span><span class="sxs-lookup"><span data-stu-id="715a0-173">The global administrator that deployed Human Resources must also launch both Attract and Onboard to complete the initialization and enable access for other tenant users.</span></span>  <span data-ttu-id="715a0-174">Før dette er gjort, kan andre brugere ikke få adgang til Attract og Onboard, men får adgangsfejl.</span><span class="sxs-lookup"><span data-stu-id="715a0-174">Until this happens, other users will not be able to access Attract and Onboard and will get access violation errors.</span></span> <span data-ttu-id="715a0-175">Du kan finde flere oplysninger under [Opret nye brugere](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) og [Tildel sikkerhedsroller til brugere](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).</span><span class="sxs-lookup"><span data-stu-id="715a0-175">For more information, see [Create new users](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/create-new-users) and [Assign users to security roles](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/sysadmin/tasks/assign-users-security-roles).</span></span> 