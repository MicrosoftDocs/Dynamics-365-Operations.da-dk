---
title: Konfigurere en B2C-lejer i Commerce
description: I dette emne beskrives, hvordan du konfigurerer dine Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) til godkendelse af brugerwebsteder i Dynamics 365 Commerce.
author: BrianShook
manager: annbe
ms.date: 06/22/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-13
ms.dyn365.ops.version: ''
ms.openlocfilehash: 4ee667bb49e70e0c881a2db1248b3f0c7fc017ce
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478134"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="6cbc7-103">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="6cbc7-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="6cbc7-104">I dette emne beskrives, hvordan du konfigurerer dine Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) til godkendelse af brugerwebsteder i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

<span data-ttu-id="6cbc7-105">Dynamics 365 Commerce bruger Azure AD B2C til at understøtte brugerlegitimationsoplysninger og -godkendelsesstrømme.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-105">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="6cbc7-106">En bruger kan tilmelde dig, logge på og nulstille deres adgangskode via disse strømme.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-106">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="6cbc7-107">Azure AD B2C gemmer følsomme brugergodkendelsesoplysninger, f.eks. brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-107">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="6cbc7-108">Brugerposten i B2C-lejeren vil gemme en B2C lokal kontopost eller en B2C social identitetsudbyderpost.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-108">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="6cbc7-109">Disse B2C-poster vil oprette et link tilbage til kundeposten i Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-109">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="6cbc7-110">Oprette eller sammenkæde med en eksisterende AAD B2C-lejer i Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="6cbc7-110">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="6cbc7-111">Log på [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="6cbc7-111">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="6cbc7-112">Vælg **Opret en ressource** i Azure-portalmenuen.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-112">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="6cbc7-113">Sørg for at bruge det abonnement og den mappe, der er forbundet med dit Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-113">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Oprette en ressource i Azure-portalen](./media/B2CImage_1.png)

1. <span data-ttu-id="6cbc7-115">Gå til **Identitet \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-115">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="6cbc7-116">Når du er på siden **Opret ny B2C lejer eller Opret et link til en eksisterende lejer**, skal du bruge en af de muligheder nedenfor, der bedst passer til firmaets behov:</span><span class="sxs-lookup"><span data-stu-id="6cbc7-116">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="6cbc7-117">**Opret en ny Azure AD B2C-lejer**: Brug denne indstilling til at oprette en ny AAD B2C-lejer.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-117">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="6cbc7-118">Vælg **Opret en ny Azure AD B2C-lejer**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-118">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="6cbc7-119">Angiv organisationsnavnet under **Organisationsnavn**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-119">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="6cbc7-120">Angiv det oprindelige domænenavn under **Oprindeligt domænenavn**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-120">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="6cbc7-121">Vælg land eller område for **Land eller område**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-121">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="6cbc7-122">Vælg **Opret** for at oprette lejeren.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-122">Select **Create** to create the tenant.</span></span>

     ![Opret en ny Azure AD-lejer](./media/B2CImage_2.png)

     - <span data-ttu-id="6cbc7-124">**Sammenkæd en eksisterende Azure AD B2C lejer med mit Azure-abonnement**: Brug denne indstilling, hvis du allerede har en Azure AD B2C lejer, du vil oprette et link til.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-124">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="6cbc7-125">Vælg **Sammenkæd en eksisterende Azure AD B2C lejer til mit Azure-abonnement**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-125">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="6cbc7-126">Vælg den relevante B2C-lejer for **Azure AD B2C-lejer**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-126">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="6cbc7-127">Hvis meddelelsen "Der ikke blev fundet nogen berettiget B2C-lejer" vises i valgfeltet, har du ikke en eksisterende berettiget B2C-lejer og skal oprette en ny.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-127">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="6cbc7-128">Vælg **Opret ny** for **Ressourcegruppe**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-128">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="6cbc7-129">Angiv et **Navn** på den ressourcegruppe, der skal indeholde lejeren, Vælg **Ressourcegruppens lokalitet**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-129">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Sammenkæd en eksisterende Azure AD B2C lejer til mit Azure-abonnement](./media/B2CImage_3.png)

1. <span data-ttu-id="6cbc7-131">Når den nye Azure AD B2C-mappe er oprettet (det kan tage et øjeblik), vises der et link til den nye mappe på dashboardet.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-131">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="6cbc7-132">Dette link vil føre dig til siden "Velkommen til Azure Active Directory B2C".</span><span class="sxs-lookup"><span data-stu-id="6cbc7-132">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Link til ny AAD-mappe](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="6cbc7-134">Hvis du har flere abonnementer til din Azure-konto eller har konfigureret B2C-lejeren uden at oprette forbindelse til et aktivt abonnement, kan du bruge banneret **Fejlfinding** til at knytte lejeren til et abonnement.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-134">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="6cbc7-135">Vælg fejlfindingsmeddelelsen, og følg instruktionerne for at løse abonnementsproblemet.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-135">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="6cbc7-136">I følgende billede vises et eksempel på et Azure AD B2C-banner til **Fejlfinding**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-136">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Advarsel viser, at mappen ikke har noget aktivt abonnement](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="6cbc7-138">Opret B2C-programmet</span><span class="sxs-lookup"><span data-stu-id="6cbc7-138">Create the B2C application</span></span>

<span data-ttu-id="6cbc7-139">Når B2C-lejeren er blevet oprettet, skal du oprette et B2C-program i lejeren for at kunne kommunikere med Commerce-handlingerne.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-139">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="6cbc7-140">Hvis du vil oprette B2C-programmet, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-140">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="6cbc7-141">Vælg **Applikationer(Ældre)** i Azure-portalen, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-141">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="6cbc7-142">Angiv på det ønskede AAD B2C-program under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-142">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="6cbc7-143">Vælg **Ja** for **Inkluder webapp/web-API** under **Webapp/Web-API**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-143">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="6cbc7-144">Vælg **Ja** (standardværdien) til **Tillad implicit flow**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-144">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="6cbc7-145">Angiv dine dedikerede svar-URL-adresser under **Svar-URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-145">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="6cbc7-146">Se [Svar-URL-adresser](#reply-urls) nedenfor for at få oplysninger om svar-URL-adresser, og hvordan du formaterer dem her.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-146">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="6cbc7-147">Vælg **Nej** (standardværdien) til **Medtag som oprindelig klient**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-147">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="6cbc7-148">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-148">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="6cbc7-149">Svar-URL-adresser</span><span class="sxs-lookup"><span data-stu-id="6cbc7-149">Reply URLs</span></span>

<span data-ttu-id="6cbc7-150">Svar-URL-adresser er vigtige, da de giver en liste over returdomænerne, når dit websted kalder Azure AD B2C for at godkende en bruger.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-150">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="6cbc7-151">Det gør det muligt at returnere den godkendte bruger tilbage til det domæne, hvor de logger på (domænet for dit websted).</span><span class="sxs-lookup"><span data-stu-id="6cbc7-151">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="6cbc7-152">I feltet **Svar-URL-adresse** på skærmen **Azure AD B2C-programmer \> Nyt program** skal du tilføje separate linjer til både dit websteds domæne og (når miljøet er klargjort) til den Commerce-genererede URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-152">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="6cbc7-153">Disse URL-adresser skal altid bruge et gyldigt URL-adresseformat og må kun være grundlæggende URL-adresser (ingen efterfølgende skråstreger eller stier).</span><span class="sxs-lookup"><span data-stu-id="6cbc7-153">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="6cbc7-154">Strengen ``/_msdyn365/authresp`` skal derefter føjes til de grundlæggende URL-adresser som i følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-154">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="6cbc7-155">``https://www.fabrikam.com/_msdyn365/authresp`` (Domænet skal svare helt til e-handelsdomænet.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-155">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="6cbc7-156">Hvis du har flere domæner, skal du tilføje denne URL-adresse for hvert domæne.)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-156">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="6cbc7-157">Oprette politikker for brugerstrøm</span><span class="sxs-lookup"><span data-stu-id="6cbc7-157">Create user flow policies</span></span>

<span data-ttu-id="6cbc7-158">Brugerstrømme er de politikker, som Azure AD B2C bruger til at give sikker log ind, registrere, redigere profil og glemme brugeroplevelser med adgangskoder.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-158">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="6cbc7-159">Dynamics 365 Commerce bruger disse strømme til at udføre politikhandlingerne for at kommunikere med Azure AD B2C-lejeren.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-159">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="6cbc7-160">Når en bruger kommunikerer med disse politikker, omdirigeres de til Azure AD B2C-lejeren for at udføre handlingerne.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-160">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="6cbc7-161">Azure AD B2C omfatter tre grundlæggende brugerstrømtyper:</span><span class="sxs-lookup"><span data-stu-id="6cbc7-161">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="6cbc7-162">Tilmelde og logge på</span><span class="sxs-lookup"><span data-stu-id="6cbc7-162">Sign up and sign in</span></span>
- <span data-ttu-id="6cbc7-163">Profilredigering</span><span class="sxs-lookup"><span data-stu-id="6cbc7-163">Profile editing</span></span>
- <span data-ttu-id="6cbc7-164">Adgangskoden er nulstillet</span><span class="sxs-lookup"><span data-stu-id="6cbc7-164">Password reset</span></span>

<span data-ttu-id="6cbc7-165">Du kan vælge at bruge de standardbrugerstrømme, der leveres af Azure AD, og som viser en side, der er placeret på Aad B2C.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-165">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="6cbc7-166">Du kan også oprette en HTML-side for at styre udseendet af disse brugerstrømoplevelser.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-166">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="6cbc7-167">Hvis du vil tilpasse brugerpolitiksiderne for Dynamics 365 Commerce, skal du se [Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="6cbc7-167">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="6cbc7-168">Du kan finde flere oplysninger under [Tilpasse grænsefladen af brugeroplevelser i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="6cbc7-168">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="6cbc7-169">Oprette en tilmeldings- og login-politik for brugerstrøm</span><span class="sxs-lookup"><span data-stu-id="6cbc7-169">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="6cbc7-170">Gør følgende for at konfigurere en tilmeldings- og login-politik.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-170">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="6cbc7-171">Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-171">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="6cbc7-172">Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-172">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="6cbc7-173">Vælg **Tilmelde og logge på** på fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-173">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="6cbc7-174">Angiv et politiknavn under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-174">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="6cbc7-175">Dette navn vises bagefter med et præfiks, som portalen tildeler (f.eks. "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="6cbc7-175">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="6cbc7-176">Marker det relevante afkrydsningsfelt under **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-176">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="6cbc7-177">Vælg det relevante valg for dit firma under **Godkendelse af flere oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-177">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="6cbc7-178">Vælg indstillinger til at indsamle attributter eller returnere krav efter behov under **Brugerattributter og -krav**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-178">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="6cbc7-179">Commerce kræver følgende standardindstillinger:</span><span class="sxs-lookup"><span data-stu-id="6cbc7-179">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="6cbc7-180">**Indsaml attribut**</span><span class="sxs-lookup"><span data-stu-id="6cbc7-180">**Collect  attribute**</span></span> | <span data-ttu-id="6cbc7-181">**Returkrav**</span><span class="sxs-lookup"><span data-stu-id="6cbc7-181">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="6cbc7-182">E-mailadresse</span><span class="sxs-lookup"><span data-stu-id="6cbc7-182">Email Address</span></span>          | <span data-ttu-id="6cbc7-183">Mailadresser</span><span class="sxs-lookup"><span data-stu-id="6cbc7-183">Email Addresses</span></span>   |
    | <span data-ttu-id="6cbc7-184">Givent navn</span><span class="sxs-lookup"><span data-stu-id="6cbc7-184">Given Name</span></span>             | <span data-ttu-id="6cbc7-185">Givent navn</span><span class="sxs-lookup"><span data-stu-id="6cbc7-185">Given Name</span></span>        |
    |                        | <span data-ttu-id="6cbc7-186">Identitetsudbyder</span><span class="sxs-lookup"><span data-stu-id="6cbc7-186">Identity Provider</span></span> |
    | <span data-ttu-id="6cbc7-187">Efternavn</span><span class="sxs-lookup"><span data-stu-id="6cbc7-187">Surname</span></span>                | <span data-ttu-id="6cbc7-188">Efternavn</span><span class="sxs-lookup"><span data-stu-id="6cbc7-188">Surname</span></span>           |
    |                        | <span data-ttu-id="6cbc7-189">Brugerens objekt-id</span><span class="sxs-lookup"><span data-stu-id="6cbc7-189">User’s Object ID</span></span>  |

1. <span data-ttu-id="6cbc7-190">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-190">Select **Create**.</span></span>

<span data-ttu-id="6cbc7-191">Følgende billede er et eksempel på brugerstrømmen i Azure AD B2C-tilmelding og -login.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-191">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Politikindstillinger for tilmelding og login](./media/B2CImage_11.png)

<span data-ttu-id="6cbc7-193">I følgende billede vises indstillingen **Kør brugerstrøm** i brugerstrømmen Azure AD B2C-tilmelding og -login.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-193">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Kør indstillingen brugerstrøm i politikstrøm](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="6cbc7-195">Oprette en brugerstrømpolitik til profilredigering</span><span class="sxs-lookup"><span data-stu-id="6cbc7-195">Create a profile editing user flow policy</span></span>

<span data-ttu-id="6cbc7-196">Gør følgende for at oprette en brugerstrømpolitik til profilredigering.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-196">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="6cbc7-197">Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-197">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="6cbc7-198">Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-198">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="6cbc7-199">Vælg **Profilredigering** på fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-199">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="6cbc7-200">Angiv brugerstrømmen til profilredigeringen under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-200">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="6cbc7-201">Dette navn vises bagefter med et præfiks, som portalen tildeler (f.eks. "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="6cbc7-201">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="6cbc7-202">Vælg **Lokal kontoregistrering** under **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-202">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="6cbc7-203">Vælg følgende afkrydsningsfelter under **Brugerattributter**:</span><span class="sxs-lookup"><span data-stu-id="6cbc7-203">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="6cbc7-204">**Mailadresser** (kun **Returkrav**)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-204">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="6cbc7-205">**Givent navn** (**Indsaml attribut** og **Returneringskrav**)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-205">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="6cbc7-206">**Identitetsudbyder** (kun **Returnkrav**)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-206">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="6cbc7-207">**Efternavn** (**Indsaml attribut** og **Returneringskrav**)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-207">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="6cbc7-208">**Brugerens objekt-id** (kun **Returkrav**)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-208">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="6cbc7-209">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-209">Select **Create**.</span></span>

<span data-ttu-id="6cbc7-210">I følgende billede vises et eksempel på brugerstrøm til Azure AD B2C profilredigering.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-210">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Opret brugerstrømpolitikken til profilredigering](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="6cbc7-212">Opret en brugerstrømpolitik til nulstilling af adgangskode</span><span class="sxs-lookup"><span data-stu-id="6cbc7-212">Create a password reset user flow policy</span></span>

<span data-ttu-id="6cbc7-213">Gør følgende for at oprette en brugerstrømpolitik til nulstilling af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-213">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="6cbc7-214">Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-214">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="6cbc7-215">Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-215">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="6cbc7-216">Vælg **Nulstilling af adgangskode** på fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-216">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="6cbc7-217">Angiv et navn til brugerstrømmen til nulstilling af adgangskode under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-217">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="6cbc7-218">Vælg **Nulstil adgangskode ved hjælp af mailadresse** under **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-218">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="6cbc7-219">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-219">Select **Create**.</span></span>
1. <span data-ttu-id="6cbc7-220">Vælg følgende afkrydsningsfelter under **Programkrav**:</span><span class="sxs-lookup"><span data-stu-id="6cbc7-220">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="6cbc7-221">**E-mail-adresser**</span><span class="sxs-lookup"><span data-stu-id="6cbc7-221">**Email addresses**</span></span>
    - <span data-ttu-id="6cbc7-222">**Givent navn**</span><span class="sxs-lookup"><span data-stu-id="6cbc7-222">**Given Name**</span></span>
    - <span data-ttu-id="6cbc7-223">**Efternavn**</span><span class="sxs-lookup"><span data-stu-id="6cbc7-223">**Surname**</span></span>
    - <span data-ttu-id="6cbc7-224">**Brugerens objekt-id**</span><span class="sxs-lookup"><span data-stu-id="6cbc7-224">**User's Object ID**</span></span>
1. <span data-ttu-id="6cbc7-225">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-225">Select **Create**.</span></span>

<span data-ttu-id="6cbc7-226">Følgende billede viser, hvor du kan indstille **Nulstil adgangskode ved hjælp af mailadresse** i en brugerstrøm til nulstilling af adgangskode i Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-226">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Indstil "Nulstil adgangskode ved hjælp af mailadresse" i politikken Nulstil adgangskode](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="6cbc7-228">Tilføj sociale identitetsudbydere (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-228">Add social identity providers (Optional)</span></span>

<span data-ttu-id="6cbc7-229">Sociale identitetsudbydere giver brugerne mulighed for at bruge deres sociale konti til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-229">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="6cbc7-230">Tilføjelse af godkendelse af sociale identitetsudbydere er valgfri i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-230">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="6cbc7-231">Hvis godkendelse af sociale identitetsudbydere ikke tilføjes, vil Azure AD B2C-standardprofilerne være hovedprofilerne til din brugerbase.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-231">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="6cbc7-232">Brugerne vælger deres eget brugernavn (deres foretrukne mailadresse) og angiver en adgangskode.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-232">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="6cbc7-233">Azure AD B2C vil godkende brugere direkte.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-233">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="6cbc7-234">Hvis godkendelse af sociale identitetsudbydere er tilføjet, og en bruger vælger en af de tilbudte sociale identitetsudbydere, oprettes der stadig en enhed i Azure AD B2C-lejeren.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-234">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="6cbc7-235">Azure AD B2C godkender derefter brugerens legitimationsoplysninger via den sociale identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-235">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="6cbc7-236">Identitetsudbyderens login opretter en post i B2C-lejeren, men i et andet format end lokale konti, da det kalder den eksterne sociale identitetsudbyders reference for godkendelse.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-236">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="6cbc7-237">Brugeren kan bruge den samme mailadresse på tværs af sociale identitetsudbydere, hvilket betyder, at det brugernavn, der bruges til godkendelse af mailadressen, ikke er entydigt for lejeren.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-237">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="6cbc7-238">Azure AD B2C vil kun gennemtvinge, at brugere har en entydig mailadresse på lokale B2C-konti.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-238">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="6cbc7-239">Før du kan tilføje en social identitetsudbyder til godkendelse, skal du gå til portalen for identitetsudbyderen og konfigurere et identitetsudbyderprogram som angivet i dokumentationen til Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-239">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="6cbc7-240">Der findes en liste over links til dokumentationen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-240">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="6cbc7-241">Amazon</span><span class="sxs-lookup"><span data-stu-id="6cbc7-241">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="6cbc7-242">Azure AD (Enkelt lejer)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-242">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="6cbc7-243">Microsoft-konto</span><span class="sxs-lookup"><span data-stu-id="6cbc7-243">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="6cbc7-244">Facebook</span><span class="sxs-lookup"><span data-stu-id="6cbc7-244">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="6cbc7-245">GitHub</span><span class="sxs-lookup"><span data-stu-id="6cbc7-245">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="6cbc7-246">Google</span><span class="sxs-lookup"><span data-stu-id="6cbc7-246">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="6cbc7-247">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="6cbc7-247">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="6cbc7-248">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="6cbc7-248">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="6cbc7-249">Twitter</span><span class="sxs-lookup"><span data-stu-id="6cbc7-249">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="6cbc7-250">Tilføje og konfigurere en sociale identitetsudbyder</span><span class="sxs-lookup"><span data-stu-id="6cbc7-250">Add and set up a social identity provider</span></span>

<span data-ttu-id="6cbc7-251">Udfør følgende trin for at tilføje og konfigurere en social identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-251">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="6cbc7-252">Naviger til **Identitetsudbydere** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-252">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="6cbc7-253">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-253">Select **Add**.</span></span> <span data-ttu-id="6cbc7-254">Skærmbilledet **Tilføj identitetsudbyder** vises.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-254">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="6cbc7-255">Angiv det navn, der skal vises for brugere på din login-skærm, under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-255">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="6cbc7-256">Vælg en identitetsudbyder på listen under **Type identitetsudbyder**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-256">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="6cbc7-257">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-257">Select **OK**.</span></span>
1. <span data-ttu-id="6cbc7-258">Vælg **Konfigurer denne identitetsudbyder** for at få adgang til skærmbilledet **Konfigurer den sociale identitetsudbyder** .</span><span class="sxs-lookup"><span data-stu-id="6cbc7-258">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="6cbc7-259">Angiv det klient-id, der er hentet fra installationsprogrammet til identitetsudbyderen, under **Klient-id**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-259">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="6cbc7-260">Angiv den klienthemmelighed, der er hentet fra installationsprogrammet til identitetsudbyderen, under **Klienthemmelighed**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-260">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="6cbc7-261">Knyt brugerstrøm til tilmeldings- og login-politikker:</span><span class="sxs-lookup"><span data-stu-id="6cbc7-261">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="6cbc7-262">Gå til **Azure AD B2C – Brugerstrømme (politikker) \> {din tilmeldings- og logon-politik} \> Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-262">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="6cbc7-263">Hvis du vil knytte brugerstrømmen til login/tilmeldingspolitikken, skal du vælge hver af de identitetsudbydere, du har konfigureret til din konto.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-263">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="6cbc7-264">Hvis du vil teste disse, skal du vælge **Kør brugerstrøm** for hver identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-264">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="6cbc7-265">Login-siden vises på en ny fane, og der vises et valgfelt til den nye identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-265">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="6cbc7-266">I følgende billede vises eksempler på skærmbillederne **Tilføj identitetsudbyder** og **Konfigurerer sociale identitetsudbydere** i Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-266">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Føje en social identitetsudbyder til dit program](./media/B2CImage_14.png)

<span data-ttu-id="6cbc7-268">I følgende billede vises et eksempel på, hvordan du kan vælge identitetsudbydere på siden Azure AD B2C **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-268">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Vælg alle de sociale identitetsudbydere, der skal aktiveres for din politik](./media/B2CImage_16.png)

<span data-ttu-id="6cbc7-270">I følgende billede vises et eksempel på en standardlogin-skærm, hvor der vises en knap til login på en social identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-270">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Eksempel på standardlogin-skærm med knap til login til social identitetsudbyder](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="6cbc7-272">Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger</span><span class="sxs-lookup"><span data-stu-id="6cbc7-272">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="6cbc7-273">Når du har udført overstående trin til Azure AD B2C-klargøring, skal Azure AD B2C-programmet registreres i dit Dynamics 365 Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-273">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="6cbc7-274">Udfør følgende trin for at opdatere Headquarters med de nye Azure AD B2C-oplysninger.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-274">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="6cbc7-275">Gå til **Delte Commerce-parametre** i Commerce, og vælg **Identitetsudbydere** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-275">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="6cbc7-276">Gør følgende under **Identitetsudbydere**:</span><span class="sxs-lookup"><span data-stu-id="6cbc7-276">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="6cbc7-277">Angiv URL-adressen til udbyderen af identitetsudbydere i feltet **Udbyder**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-277">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="6cbc7-278">Du kan finde URL-adressen til udstederen [Få udsteders URL-adresse](#obtain-issuer-url) nedenfor.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-278">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="6cbc7-279">Skriv et navn på din udbyderpost i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-279">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="6cbc7-280">Skriv **Azure AD B2C (id_token)** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-280">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="6cbc7-281">Gør følgende under **Betroede parter** med ovenstående B2C-identitetsudbyderelement valgt:</span><span class="sxs-lookup"><span data-stu-id="6cbc7-281">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="6cbc7-282">Angiv dit B2C-program-id i feltet **Klient-id**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-282">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="6cbc7-283">Du kan finde dette i feltet **Program-id** på siden med egenskaber for B2C-programmet.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-283">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="6cbc7-284">Skriv **Offentlig** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-284">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="6cbc7-285">Skriv **Kunde** i feltet **Brugertype**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-285">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="6cbc7-286">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-286">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="6cbc7-287">Søg efter **Distributionsplan** i feltet Commerce-søgning</span><span class="sxs-lookup"><span data-stu-id="6cbc7-287">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="6cbc7-288">Vælg job **1110 global konfiguration** i den venstre navigationsmenu på siden **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-288">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="6cbc7-289">Vælg **Kør nu** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-289">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="6cbc7-290">Hent URL-adresse til udsteder</span><span class="sxs-lookup"><span data-stu-id="6cbc7-290">Obtain issuer URL</span></span>

<span data-ttu-id="6cbc7-291">Følg disse trin for at få URL-adressen til identitetsudbyderens udsteder.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-291">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="6cbc7-292">Opret en URL-metadataadresse i følgende format med din B2C-lejer og -politik: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="6cbc7-292">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="6cbc7-293">Eksempel: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-293">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="6cbc7-294">Angiv URL-metadataadressen i en browsers adresselinje.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-294">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="6cbc7-295">Kopier URL-adressen til identitetsudbyderens udsteder (værdien for **"udsteder"**) i metadataene.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-295">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="6cbc7-296">Eksempel: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-296">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="6cbc7-297">Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren</span><span class="sxs-lookup"><span data-stu-id="6cbc7-297">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="6cbc7-298">Når konfigurationen af din Azure AD B2C-lejer er fuldført, skal du konfigurere B2C-lejeren i Commerce-webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-298">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="6cbc7-299">Konfigurationstrin omfatter indsamling af oplysninger om B2C-programmet fra Azure-portalen, indtastning af B2C-programoplysninger i webstedsgeneratoren og derefter tilknytning af B2C-programmet til dit webstedsted og din kanal.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-299">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="6cbc7-300">Indsaml de nødvendige programoplysninger</span><span class="sxs-lookup"><span data-stu-id="6cbc7-300">Collect the required application information</span></span>

<span data-ttu-id="6cbc7-301">Udfør følgende trin for at indsamle de nødvendige programoplysninger.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-301">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="6cbc7-302">Gå til **Start \> Azure AD B2C-programmer** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-302">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="6cbc7-303">Vælg dit program, og vælg derefter **Egenskaber** i venstre navigationsrude for at få oplysninger om programmet.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-303">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="6cbc7-304">I boksen **Program-id** skal du indsamle program-id'et for det B2C-program, der er oprettet i din B2C-lejer.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-304">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="6cbc7-305">Det vil senere blive angivet som **Klient-GUID** i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-305">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="6cbc7-306">Hent svar-URL-adressen under **Svar-URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-306">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="6cbc7-307">Gå til **Start \> Azure AD B2C – Brugerstrømme (politikker)**, og indsaml derefter navnene på hver enkelt brugerstrømpolitik.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-307">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="6cbc7-308">I følgende billede vises et eksempel på siden **Azure AD B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-308">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Naviger til B2C-programmet i din lejer](./media/B2CImage_19.png)

<span data-ttu-id="6cbc7-310">I følgende billede vises et eksempel på siden **Egenskaber** for et program i Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-310">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Kopiér program-id'et fra egenskaberne for B2C-programmet](./media/B2CImage_21.png)

<span data-ttu-id="6cbc7-312">I følgende billede vises et eksempel på brugerstrømpolitikker på siden **Azure AD B2C – Brugerstrømme (politikker)**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-312">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Indsaml navnene på de enkelte B2C-politikstrømme](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="6cbc7-314">Angiv programoplysninger om din AAD B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="6cbc7-314">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="6cbc7-315">Du skal angive oplysninger om Azure AD B2C-lejeren i Commerce-webstedsgenerator, før du knytter B2C-lejeren til dit eller dine websteder.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-315">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="6cbc7-316">Udfør følgende trin for at føje AAD B2C-lejerens programoplysninger til Commerce.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-316">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="6cbc7-317">Log på som administrator af Commerce-webstedsgenerator for dit miljø.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-317">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="6cbc7-318">Vælg **Lejerindstillinger** i venstre navigationsrude for at udvide den.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-318">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="6cbc7-319">Vælg **B2C-indstillinger** under **Lejerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-319">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="6cbc7-320">Vælg **Administrer** i hovedvinduet ved siden af **B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-320">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="6cbc7-321">(Hvis lejeren vises på B2C-programlisten, er den allerede blevet tilføjet af en administrator.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-321">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="6cbc7-322">Kontrollér, at punkterne i trin 6 nedenfor svarer til dit B2C-program.)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-322">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="6cbc7-323">Vælg **Tilføj B2C-program**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-323">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="6cbc7-324">Angiv følgende påkrævede punkter i formularen, der vises, ved at bruge værdier fra B2C-lejeren og -programmet.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-324">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="6cbc7-325">Felter, der ikke er obligatoriske (dvs. uden en stjerne), kan være tomme.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-325">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="6cbc7-326">**Programnavn**: Navnet på dit B2C-program, f.eks. "Fabrikam B2C".</span><span class="sxs-lookup"><span data-stu-id="6cbc7-326">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="6cbc7-327">**Navn på lejer**: Navnet på din B2C-lejer (f.eks. brug "fabrikam", hvis domænet vises som "fabrikam.onmicrosoft.com" for B2C-lejeren).</span><span class="sxs-lookup"><span data-stu-id="6cbc7-327">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="6cbc7-328">**Glem adgangskodepolitik-id**: Politik-id for brugerstrømmen for glemt adgangskode, f.eks. "B2C_1_PasswordReset".</span><span class="sxs-lookup"><span data-stu-id="6cbc7-328">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="6cbc7-329">**Politik-id for tilmelding og logon**: Politik-id for tilmelding og logon i brugerstrømmen, f.eks. "B2C_1_signup_signin".</span><span class="sxs-lookup"><span data-stu-id="6cbc7-329">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="6cbc7-330">**Klient-GUID**: B2C-program-id'et, f.eks. "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span><span class="sxs-lookup"><span data-stu-id="6cbc7-330">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="6cbc7-331">**Rediger profilpolitik-id**: Politik-id'et for brugerstrømmen til profilredigering, f.eks. "B2C_1A_ProfileEdit".</span><span class="sxs-lookup"><span data-stu-id="6cbc7-331">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="6cbc7-332">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-332">Select **OK**.</span></span> <span data-ttu-id="6cbc7-333">Navnet på dit B2C-program vises nu på listen.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-333">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="6cbc7-334">Vælg **Gem** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-334">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="6cbc7-335">Knyt B2C-programmet til dit websted og din kanal</span><span class="sxs-lookup"><span data-stu-id="6cbc7-335">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="6cbc7-336">Hvis dit websted allerede er knyttet til et B2C program, og du skifter til et andet B2C-program, fjernes de aktuelle referencer, der er oprettet for brugere, som allerede er tilmeldt i dette miljø.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-336">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="6cbc7-337">Hvis de ændres, vil alle legitimationsoplysninger, der er knyttet til det aktuelt tildelte B2C-program, ikke være tilgængelige for brugerne.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-337">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="6cbc7-338">Du skal kun opdatere kun B2C-programmet, hvis du konfigurerer kanalens B2C-program for første gang, eller hvis du vil have, at brugere skal tilmelde sig med nye legitimationsoplysninger til denne kanal med det nye B2C-program.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-338">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="6cbc7-339">Vær forsigtig, når du knytter kanaler til B2C-programmer, og navngiv programmer tydeligt.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-339">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="6cbc7-340">Hvis en kanal ikke er knyttet til et B2C-program i trinnene nedenfor, vil de brugere, der logger på den pågældende kanal til dit websted, blive angivet i B2C-programmet, der vises som **standard** på listen **Lejerindstillinger \> B2C-indstillinger** for B2C-programmer.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-340">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="6cbc7-341">Gør følgende for at knytte B2C-programmet til dit websted og din kanal.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-341">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="6cbc7-342">Naviger til dit websted i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-342">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="6cbc7-343">Vælg **Indstillinger for websted** i venstre navigationsrude for at udvide den.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-343">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="6cbc7-344">Vælg **Kanaler** nedenunder **Indstillinger for websted**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-344">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="6cbc7-345">Vælg kanalen i hovedvinduet under **Kanaler**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-345">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="6cbc7-346">I ruden Egenskaber for kanal til højre skal du vælge navnet på dit B2C-program i rullemenuen **Vælg B2C-program**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-346">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="6cbc7-347">Vælg **Luk**, og vælg derefter **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-347">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="6cbc7-348">Flere B2C-oplysninger</span><span class="sxs-lookup"><span data-stu-id="6cbc7-348">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="6cbc7-349">Kundeoverflytning</span><span class="sxs-lookup"><span data-stu-id="6cbc7-349">Customer migration</span></span>

<span data-ttu-id="6cbc7-350">Hvis du overvejer at overflytte kundeposter fra en tidligere identitetsudbyderplatform, skal du arbejde med Dynamics 365 Commerce-teamet for at gennemgå dine behov for kundeoverflytning.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-350">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="6cbc7-351">Du kan få yderligere Azure AD B2C-dokumentation om kundeoverflytning under [Overflytte brugere til Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="6cbc7-351">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="6cbc7-352">Brugerdefinerede politikker</span><span class="sxs-lookup"><span data-stu-id="6cbc7-352">Custom policies</span></span>

<span data-ttu-id="6cbc7-353">Du kan få yderligere oplysninger om tilpasning af Azure AD B2C-interaktioner og politikstrømme, der ligger ud over, hvad der tilbydes af B2C standardpolitikker, i [Tilpassede politikker i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="6cbc7-353">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="6cbc7-354">Sekundær administrator</span><span class="sxs-lookup"><span data-stu-id="6cbc7-354">Secondary admin</span></span>

<span data-ttu-id="6cbc7-355">Du kan tilføje en valgfri, sekundær administratorkonto under afsnittet **Bruger** i din B2C-lejer.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-355">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="6cbc7-356">Det kan være en direkte konto eller en generel konto.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-356">This can be a direct account or a general account.</span></span> <span data-ttu-id="6cbc7-357">Hvis du skal dele en konto på tværs af teamressourcer, kan du også oprette en fælles konto.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-357">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="6cbc7-358">På grund af følsomheden for de data der er lagret i Azure AD B2C, skal en fælles konto overvåges nøje i følge firmaets sikkerhedspraksis.</span><span class="sxs-lookup"><span data-stu-id="6cbc7-358">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="6cbc7-359">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="6cbc7-359">Additional resources</span></span>

[<span data-ttu-id="6cbc7-360">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="6cbc7-360">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="6cbc7-361">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="6cbc7-361">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="6cbc7-362">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="6cbc7-362">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="6cbc7-363">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="6cbc7-363">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="6cbc7-364">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="6cbc7-364">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

<span data-ttu-id="6cbc7-365">[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)Knyt et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="6cbc7-365">[Upload URL redirects in bulk](upload-bulk-redirects.md)Associate a Dynamics 365 Commerce site with an online channel</span></span>

[<span data-ttu-id="6cbc7-366">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="6cbc7-366">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="6cbc7-367">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="6cbc7-367">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="6cbc7-368">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="6cbc7-368">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="6cbc7-369">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="6cbc7-369">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
