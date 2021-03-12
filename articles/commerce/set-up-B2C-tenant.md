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
ms.openlocfilehash: 68e72bc17005c11f28f572114357f906098cc045
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993338"
---
# <a name="set-up-a-b2c-tenant-in-commerce"></a><span data-ttu-id="a9478-103">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="a9478-103">Set up a B2C tenant in Commerce</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a9478-104">I dette emne beskrives, hvordan du konfigurerer dine Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) til godkendelse af brugerwebsteder i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a9478-104">This topic describes how to set up your Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants for user site authentication in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a9478-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="a9478-105">Overview</span></span>

<span data-ttu-id="a9478-106">Dynamics 365 Commerce bruger Azure AD B2C til at understøtte brugerlegitimationsoplysninger og -godkendelsesstrømme.</span><span class="sxs-lookup"><span data-stu-id="a9478-106">Dynamics 365 Commerce uses Azure AD B2C to support user credential and authentication flows.</span></span> <span data-ttu-id="a9478-107">En bruger kan tilmelde dig, logge på og nulstille deres adgangskode via disse strømme.</span><span class="sxs-lookup"><span data-stu-id="a9478-107">A user can sign up, sign in, and reset their password through these flows.</span></span> <span data-ttu-id="a9478-108">Azure AD B2C gemmer følsomme brugergodkendelsesoplysninger, f.eks. brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="a9478-108">Azure AD B2C stores sensitive user authentication information, such as username and password.</span></span> <span data-ttu-id="a9478-109">Brugerposten i B2C-lejeren vil gemme en B2C lokal kontopost eller en B2C social identitetsudbyderpost.</span><span class="sxs-lookup"><span data-stu-id="a9478-109">The user record in the B2C tenant will store either a B2C local account record or a B2C social identity provider record.</span></span> <span data-ttu-id="a9478-110">Disse B2C-poster vil oprette et link tilbage til kundeposten i Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="a9478-110">These B2C records will link back to the customer record in the Commerce environment.</span></span>

## <a name="create-or-link-to-an-existing-aad-b2c-tenant-in-the-azure-portal"></a><span data-ttu-id="a9478-111">Oprette eller sammenkæde med en eksisterende AAD B2C-lejer i Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="a9478-111">Create or link to an existing AAD B2C tenant in the Azure portal</span></span>

1. <span data-ttu-id="a9478-112">Log på [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="a9478-112">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="a9478-113">Vælg **Opret en ressource** i Azure-portalmenuen.</span><span class="sxs-lookup"><span data-stu-id="a9478-113">From the Azure portal menu, select **Create a resource**.</span></span> <span data-ttu-id="a9478-114">Sørg for at bruge det abonnement og den mappe, der er forbundet med dit Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="a9478-114">Be sure to use the subscription and directory that will be connected with your Commerce environment.</span></span>

    ![Oprette en ressource i Azure-portalen](./media/B2CImage_1.png)

1. <span data-ttu-id="a9478-116">Gå til **Identitet \> Azure Active Directory B2C**.</span><span class="sxs-lookup"><span data-stu-id="a9478-116">Go to **Identity \> Azure Active Directory B2C**.</span></span>
1. <span data-ttu-id="a9478-117">Når du er på siden **Opret ny B2C lejer eller Opret et link til en eksisterende lejer**, skal du bruge en af de muligheder nedenfor, der bedst passer til firmaets behov:</span><span class="sxs-lookup"><span data-stu-id="a9478-117">Once on the **Create New B2C Tenant or Link to existing Tenant** page, use one of the options below that best suits your company's needs:</span></span>

    - <span data-ttu-id="a9478-118">**Opret en ny Azure AD B2C-lejer**: Brug denne indstilling til at oprette en ny AAD B2C-lejer.</span><span class="sxs-lookup"><span data-stu-id="a9478-118">**Create a new Azure AD B2C Tenant**: Use this option to create a new AAD B2C tenant.</span></span>
        1. <span data-ttu-id="a9478-119">Vælg **Opret en ny Azure AD B2C-lejer**.</span><span class="sxs-lookup"><span data-stu-id="a9478-119">Select **Create a new Azure AD B2C Tenant**.</span></span>
        1. <span data-ttu-id="a9478-120">Angiv organisationsnavnet under **Organisationsnavn**.</span><span class="sxs-lookup"><span data-stu-id="a9478-120">Under **Organization name**, enter the organization name.</span></span>
        1. <span data-ttu-id="a9478-121">Angiv det oprindelige domænenavn under **Oprindeligt domænenavn**.</span><span class="sxs-lookup"><span data-stu-id="a9478-121">Under **Initial domain name**, enter the initial domain name.</span></span>
        1. <span data-ttu-id="a9478-122">Vælg land eller område for **Land eller område**.</span><span class="sxs-lookup"><span data-stu-id="a9478-122">For **Country or region**, select the country or region.</span></span>
        1. <span data-ttu-id="a9478-123">Vælg **Opret** for at oprette lejeren.</span><span class="sxs-lookup"><span data-stu-id="a9478-123">Select **Create** to create the tenant.</span></span>

     ![Opret en ny Azure AD-lejer](./media/B2CImage_2.png)

     - <span data-ttu-id="a9478-125">**Sammenkæd en eksisterende Azure AD B2C lejer med mit Azure-abonnement**: Brug denne indstilling, hvis du allerede har en Azure AD B2C lejer, du vil oprette et link til.</span><span class="sxs-lookup"><span data-stu-id="a9478-125">**Link an existing Azure AD B2C Tenant to my Azure subscription**: Use this option if you already have an Azure AD B2C tenant you want to link to.</span></span>
        1. <span data-ttu-id="a9478-126">Vælg **Sammenkæd en eksisterende Azure AD B2C lejer til mit Azure-abonnement**.</span><span class="sxs-lookup"><span data-stu-id="a9478-126">Select **Link an existing Azure AD B2C Tenant to my Azure subscription**.</span></span>
        1. <span data-ttu-id="a9478-127">Vælg den relevante B2C-lejer for **Azure AD B2C-lejer**.</span><span class="sxs-lookup"><span data-stu-id="a9478-127">For **Azure AD B2C Tenant**, select the appropriate B2C tenant.</span></span> <span data-ttu-id="a9478-128">Hvis meddelelsen "Der ikke blev fundet nogen berettiget B2C-lejer" vises i valgfeltet, har du ikke en eksisterende berettiget B2C-lejer og skal oprette en ny.</span><span class="sxs-lookup"><span data-stu-id="a9478-128">If the message "No eligible B2C Tenants found" appears in the selection box, you do not have an existing eligible B2C tenant and will need to create a new one.</span></span>
        1. <span data-ttu-id="a9478-129">Vælg **Opret ny** for **Ressourcegruppe**.</span><span class="sxs-lookup"><span data-stu-id="a9478-129">For **Resource group**, select **Create new**.</span></span> <span data-ttu-id="a9478-130">Angiv et **Navn** på den ressourcegruppe, der skal indeholde lejeren, Vælg **Ressourcegruppens lokalitet**, og vælg derefter **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a9478-130">Enter a **Name** for the resource group that will contain the tenant, select the **Resource group location**, and then select **Create**.</span></span>

    ![Sammenkæd en eksisterende Azure AD B2C lejer til mit Azure-abonnement](./media/B2CImage_3.png)

1. <span data-ttu-id="a9478-132">Når den nye Azure AD B2C-mappe er oprettet (det kan tage et øjeblik), vises der et link til den nye mappe på dashboardet.</span><span class="sxs-lookup"><span data-stu-id="a9478-132">Once the new Azure AD B2C directory is created (this may take a few moments), a link to the new directory will appear on the dashboard.</span></span> <span data-ttu-id="a9478-133">Dette link vil føre dig til siden "Velkommen til Azure Active Directory B2C".</span><span class="sxs-lookup"><span data-stu-id="a9478-133">This link will direct you to the "Welcome to Azure Active Directory B2C" page.</span></span>

    ![Link til ny AAD-mappe](./media/B2CImage_4.png)

> [!NOTE]
> <span data-ttu-id="a9478-135">Hvis du har flere abonnementer til din Azure-konto eller har konfigureret B2C-lejeren uden at oprette forbindelse til et aktivt abonnement, kan du bruge banneret **Fejlfinding** til at knytte lejeren til et abonnement.</span><span class="sxs-lookup"><span data-stu-id="a9478-135">If you have multiple subscriptions within your Azure account or have set up the B2C tenant without linking to an active subscription, a **Troubleshoot** banner will direct you to link the tenant to a subscription.</span></span> <span data-ttu-id="a9478-136">Vælg fejlfindingsmeddelelsen, og følg instruktionerne for at løse abonnementsproblemet.</span><span class="sxs-lookup"><span data-stu-id="a9478-136">Select the troubleshooting message and follow the instructions to resolve the subscription issue.</span></span>

<span data-ttu-id="a9478-137">I følgende billede vises et eksempel på et Azure AD B2C-banner til **Fejlfinding**.</span><span class="sxs-lookup"><span data-stu-id="a9478-137">The following image shows an example of an Azure AD B2C **Troubleshoot** banner.</span></span>

![Advarsel viser, at mappen ikke har noget aktivt abonnement](./media/B2CImage_5.png)

## <a name="create-the-b2c-application"></a><span data-ttu-id="a9478-139">Opret B2C-programmet</span><span class="sxs-lookup"><span data-stu-id="a9478-139">Create the B2C application</span></span>

<span data-ttu-id="a9478-140">Når B2C-lejeren er blevet oprettet, skal du oprette et B2C-program i lejeren for at kunne kommunikere med Commerce-handlingerne.</span><span class="sxs-lookup"><span data-stu-id="a9478-140">Once the B2C tenant has been created, you will create a B2C application within the tenant to interact with the Commerce actions.</span></span>

<span data-ttu-id="a9478-141">Hvis du vil oprette B2C-programmet, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="a9478-141">To create the B2C application, follow these steps.</span></span>

1. <span data-ttu-id="a9478-142">Vælg **Applikationer(Ældre)** i Azure-portalen, og vælg derefter **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="a9478-142">In the Azure portal, select **Applications(Legacy)** and then select **Add**.</span></span>
1. <span data-ttu-id="a9478-143">Angiv på det ønskede AAD B2C-program under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a9478-143">Under **Name**, enter the name of the desired AAD B2C application.</span></span>
1. <span data-ttu-id="a9478-144">Vælg **Ja** for **Inkluder webapp/web-API** under **Webapp/Web-API**.</span><span class="sxs-lookup"><span data-stu-id="a9478-144">Under **Web App/Web API**, for **Include web app / web API**, select **Yes**.</span></span>
1. <span data-ttu-id="a9478-145">Vælg **Ja** (standardværdien) til **Tillad implicit flow**.</span><span class="sxs-lookup"><span data-stu-id="a9478-145">For **Allow implicit flow**, select **Yes** (the default value).</span></span>
1. <span data-ttu-id="a9478-146">Angiv dine dedikerede svar-URL-adresser under **Svar-URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="a9478-146">Under **Reply URL**, enter your dedicated reply URLs.</span></span> <span data-ttu-id="a9478-147">Se [Svar-URL-adresser](#reply-urls) nedenfor for at få oplysninger om svar-URL-adresser, og hvordan du formaterer dem her.</span><span class="sxs-lookup"><span data-stu-id="a9478-147">See [Reply URLs](#reply-urls) below for information on reply URLs and how to format them here.</span></span>
1. <span data-ttu-id="a9478-148">Vælg **Nej** (standardværdien) til **Medtag som oprindelig klient**.</span><span class="sxs-lookup"><span data-stu-id="a9478-148">For **Include native client**, select **No** (the default value).</span></span>
1. <span data-ttu-id="a9478-149">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a9478-149">Select **Create**.</span></span>

### <a name="reply-urls"></a><span data-ttu-id="a9478-150">Svar-URL-adresser</span><span class="sxs-lookup"><span data-stu-id="a9478-150">Reply URLs</span></span>

<span data-ttu-id="a9478-151">Svar-URL-adresser er vigtige, da de giver en liste over returdomænerne, når dit websted kalder Azure AD B2C for at godkende en bruger.</span><span class="sxs-lookup"><span data-stu-id="a9478-151">Reply URLs are important as they provide an allow list of the return domains when your site calls Azure AD B2C to authenticate a user.</span></span> <span data-ttu-id="a9478-152">Det gør det muligt at returnere den godkendte bruger tilbage til det domæne, hvor de logger på (domænet for dit websted).</span><span class="sxs-lookup"><span data-stu-id="a9478-152">This permits the return of the authenticated user back to the domain from which they are signing into (your site domain).</span></span> 

<span data-ttu-id="a9478-153">I feltet **Svar-URL-adresse** på skærmen **Azure AD B2C-programmer \> Nyt program** skal du tilføje separate linjer til både dit websteds domæne og (når miljøet er klargjort) til den Commerce-genererede URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="a9478-153">In the **Reply URL** box on the **Azure AD B2c - Applications \> New application** screen, you need to add separate lines for both your site domain and (once your environment is provisioned) the Commerce-generated URL.</span></span> <span data-ttu-id="a9478-154">Disse URL-adresser skal altid bruge et gyldigt URL-adresseformat og må kun være grundlæggende URL-adresser (ingen efterfølgende skråstreger eller stier).</span><span class="sxs-lookup"><span data-stu-id="a9478-154">These URLs must always use a valid URL format and must be base URLs only (no trailing forward slashes or paths).</span></span> <span data-ttu-id="a9478-155">Strengen ``/_msdyn365/authresp`` skal derefter føjes til de grundlæggende URL-adresser som i følgende eksempler.</span><span class="sxs-lookup"><span data-stu-id="a9478-155">The string ``/_msdyn365/authresp`` then needs to be appended to the base URLs, as in the following examples.</span></span>

- <span data-ttu-id="a9478-156">``https://www.fabrikam.com/_msdyn365/authresp`` (Domænet skal svare helt til e-handelsdomænet.</span><span class="sxs-lookup"><span data-stu-id="a9478-156">``https://www.fabrikam.com/_msdyn365/authresp`` (The domain should match the e-commerce domain completely.</span></span> <span data-ttu-id="a9478-157">Hvis du har flere domæner, skal du tilføje denne URL-adresse for hvert domæne.)</span><span class="sxs-lookup"><span data-stu-id="a9478-157">If you have multiple domains, you need to add this URL for each domain.)</span></span>
- ``https://fabrikam-prod.commerce.dynamics.com/_msdyn365/authresp``

## <a name="create-user-flow-policies"></a><span data-ttu-id="a9478-158">Oprette politikker for brugerstrøm</span><span class="sxs-lookup"><span data-stu-id="a9478-158">Create user flow policies</span></span>

<span data-ttu-id="a9478-159">Brugerstrømme er de politikker, som Azure AD B2C bruger til at give sikker log ind, registrere, redigere profil og glemme brugeroplevelser med adgangskoder.</span><span class="sxs-lookup"><span data-stu-id="a9478-159">User flows are the policies Azure AD B2C uses to provide secure sign in, sign up, edit profile, and forget password user experiences.</span></span> <span data-ttu-id="a9478-160">Dynamics 365 Commerce bruger disse strømme til at udføre politikhandlingerne for at kommunikere med Azure AD B2C-lejeren.</span><span class="sxs-lookup"><span data-stu-id="a9478-160">Dynamics 365 Commerce uses these flows to perform the policy actions to interact with the Azure AD B2C tenant.</span></span> <span data-ttu-id="a9478-161">Når en bruger kommunikerer med disse politikker, omdirigeres de til Azure AD B2C-lejeren for at udføre handlingerne.</span><span class="sxs-lookup"><span data-stu-id="a9478-161">When a user interacts with these policies, they are redirected to the Azure AD B2C tenant to perform the actions.</span></span>

<span data-ttu-id="a9478-162">Azure AD B2C omfatter tre grundlæggende brugerstrømtyper:</span><span class="sxs-lookup"><span data-stu-id="a9478-162">Azure AD B2C provides three basic user flow types:</span></span>
- <span data-ttu-id="a9478-163">Tilmelde og logge på</span><span class="sxs-lookup"><span data-stu-id="a9478-163">Sign up and sign in</span></span>
- <span data-ttu-id="a9478-164">Profilredigering</span><span class="sxs-lookup"><span data-stu-id="a9478-164">Profile editing</span></span>
- <span data-ttu-id="a9478-165">Adgangskoden er nulstillet</span><span class="sxs-lookup"><span data-stu-id="a9478-165">Password reset</span></span>

<span data-ttu-id="a9478-166">Du kan vælge at bruge de standardbrugerstrømme, der leveres af Azure AD, og som viser en side, der er placeret på Aad B2C.</span><span class="sxs-lookup"><span data-stu-id="a9478-166">You can choose to use the default user flows provided by Azure AD, which will display a page hosted by AAD B2C.</span></span> <span data-ttu-id="a9478-167">Du kan også oprette en HTML-side for at styre udseendet af disse brugerstrømoplevelser.</span><span class="sxs-lookup"><span data-stu-id="a9478-167">Alternately, you can create an HTML page to control the look and feel of these user flow experiences.</span></span> 

<span data-ttu-id="a9478-168">Hvis du vil tilpasse brugerpolitiksiderne for Dynamics 365 Commerce, skal du se [Konfigurere brugerdefinerede sider til brugerlogon](custom-pages-user-logins.md).</span><span class="sxs-lookup"><span data-stu-id="a9478-168">To customize the user policy pages for Dynamics 365 Commerce, see [Set up custom pages for user logins](custom-pages-user-logins.md).</span></span> <span data-ttu-id="a9478-169">Du kan finde flere oplysninger under [Tilpasse grænsefladen af brugeroplevelser i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span><span class="sxs-lookup"><span data-stu-id="a9478-169">For additional information, see [Customize the interface of user experiences in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/tutorial-customize-ui).</span></span>

### <a name="create-a-sign-up-and-sign-in-user-flow-policy"></a><span data-ttu-id="a9478-170">Oprette en tilmeldings- og login-politik for brugerstrøm</span><span class="sxs-lookup"><span data-stu-id="a9478-170">Create a sign up and sign in user flow policy</span></span>

<span data-ttu-id="a9478-171">Gør følgende for at konfigurere en tilmeldings- og login-politik.</span><span class="sxs-lookup"><span data-stu-id="a9478-171">To create a sign up and sign in user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="a9478-172">Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="a9478-172">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="a9478-173">Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.</span><span class="sxs-lookup"><span data-stu-id="a9478-173">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="a9478-174">Vælg **Tilmelde og logge på** på fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="a9478-174">On the **Recommended** tab, select **Sign up and sign in**.</span></span>
1. <span data-ttu-id="a9478-175">Angiv et politiknavn under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a9478-175">Under **Name**, enter a policy name.</span></span> <span data-ttu-id="a9478-176">Dette navn vises bagefter med et præfiks, som portalen tildeler (f.eks. "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="a9478-176">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="a9478-177">Marker det relevante afkrydsningsfelt under **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="a9478-177">Under **Identity providers**, select the appropriate check box.</span></span>
1. <span data-ttu-id="a9478-178">Vælg det relevante valg for dit firma under **Godkendelse af flere oplysninger**.</span><span class="sxs-lookup"><span data-stu-id="a9478-178">Under **Multifactor Authentication**, select the appropriate choice for your company.</span></span> 
1. <span data-ttu-id="a9478-179">Vælg indstillinger til at indsamle attributter eller returnere krav efter behov under **Brugerattributter og -krav**.</span><span class="sxs-lookup"><span data-stu-id="a9478-179">Under **User attributes and claims**, select options to collect attributes or return claims as appropriate.</span></span> <span data-ttu-id="a9478-180">Commerce kræver følgende standardindstillinger:</span><span class="sxs-lookup"><span data-stu-id="a9478-180">Commerce requires the following default options:</span></span>

    | <span data-ttu-id="a9478-181">**Indsaml attribut**</span><span class="sxs-lookup"><span data-stu-id="a9478-181">**Collect  attribute**</span></span> | <span data-ttu-id="a9478-182">**Returkrav**</span><span class="sxs-lookup"><span data-stu-id="a9478-182">**Return  claim**</span></span> |
    | ---------------------- | ----------------- |
    | <span data-ttu-id="a9478-183">E-mailadresse</span><span class="sxs-lookup"><span data-stu-id="a9478-183">Email Address</span></span>          | <span data-ttu-id="a9478-184">Mailadresser</span><span class="sxs-lookup"><span data-stu-id="a9478-184">Email Addresses</span></span>   |
    | <span data-ttu-id="a9478-185">Givent navn</span><span class="sxs-lookup"><span data-stu-id="a9478-185">Given Name</span></span>             | <span data-ttu-id="a9478-186">Givent navn</span><span class="sxs-lookup"><span data-stu-id="a9478-186">Given Name</span></span>        |
    |                        | <span data-ttu-id="a9478-187">Identitetsudbyder</span><span class="sxs-lookup"><span data-stu-id="a9478-187">Identity Provider</span></span> |
    | <span data-ttu-id="a9478-188">Efternavn</span><span class="sxs-lookup"><span data-stu-id="a9478-188">Surname</span></span>                | <span data-ttu-id="a9478-189">Efternavn</span><span class="sxs-lookup"><span data-stu-id="a9478-189">Surname</span></span>           |
    |                        | <span data-ttu-id="a9478-190">Brugerens objekt-id</span><span class="sxs-lookup"><span data-stu-id="a9478-190">User’s Object ID</span></span>  |

1. <span data-ttu-id="a9478-191">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a9478-191">Select **Create**.</span></span>

<span data-ttu-id="a9478-192">Følgende billede er et eksempel på brugerstrømmen i Azure AD B2C-tilmelding og -login.</span><span class="sxs-lookup"><span data-stu-id="a9478-192">The following image is an example of the Azure AD B2C sign up and sign in user flow.</span></span>

![Politikindstillinger for tilmelding og login](./media/B2CImage_11.png)

<span data-ttu-id="a9478-194">I følgende billede vises indstillingen **Kør brugerstrøm** i brugerstrømmen Azure AD B2C-tilmelding og -login.</span><span class="sxs-lookup"><span data-stu-id="a9478-194">The following image shows the **Run user flow** option in the Azure AD B2C sign up and sign in user flow.</span></span>

![Kør indstillingen brugerstrøm i politikstrøm](./media/B2CImage_23.png)
   
### <a name="create-a-profile-editing-user-flow-policy"></a><span data-ttu-id="a9478-196">Oprette en brugerstrømpolitik til profilredigering</span><span class="sxs-lookup"><span data-stu-id="a9478-196">Create a profile editing user flow policy</span></span>

<span data-ttu-id="a9478-197">Gør følgende for at oprette en brugerstrømpolitik til profilredigering.</span><span class="sxs-lookup"><span data-stu-id="a9478-197">To create a profile editing user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="a9478-198">Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="a9478-198">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="a9478-199">Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.</span><span class="sxs-lookup"><span data-stu-id="a9478-199">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="a9478-200">Vælg **Profilredigering** på fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="a9478-200">On the **Recommended** tab, select **Profile editing**.</span></span>
1. <span data-ttu-id="a9478-201">Angiv brugerstrømmen til profilredigeringen under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a9478-201">Under **Name**, enter the profile editing user flow.</span></span> <span data-ttu-id="a9478-202">Dette navn vises bagefter med et præfiks, som portalen tildeler (f.eks. "B2C_1_").</span><span class="sxs-lookup"><span data-stu-id="a9478-202">This name will display afterwards with a prefix the portal assigns (for example, "B2C_1_").</span></span>
1. <span data-ttu-id="a9478-203">Vælg **Lokal kontoregistrering** under **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="a9478-203">Under **Identity providers**, select **Local Account SignIn**.</span></span>
1. <span data-ttu-id="a9478-204">Vælg følgende afkrydsningsfelter under **Brugerattributter**:</span><span class="sxs-lookup"><span data-stu-id="a9478-204">Under **User attributes**, select the following check boxes:</span></span>
    - <span data-ttu-id="a9478-205">**Mailadresser** (kun **Returkrav**)</span><span class="sxs-lookup"><span data-stu-id="a9478-205">**Email Addresses** (**Return claim** only)</span></span>
    - <span data-ttu-id="a9478-206">**Givent navn** (**Indsaml attribut** og **Returneringskrav**)</span><span class="sxs-lookup"><span data-stu-id="a9478-206">**Given Name** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="a9478-207">**Identitetsudbyder** (kun **Returnkrav**)</span><span class="sxs-lookup"><span data-stu-id="a9478-207">**Identity Provider** (**Return claim** only)</span></span>
    - <span data-ttu-id="a9478-208">**Efternavn** (**Indsaml attribut** og **Returneringskrav**)</span><span class="sxs-lookup"><span data-stu-id="a9478-208">**Surname** (**Collect attribute** and **Return claim**)</span></span>
    - <span data-ttu-id="a9478-209">**Brugerens objekt-id** (kun **Returkrav**)</span><span class="sxs-lookup"><span data-stu-id="a9478-209">**User's Object ID** (**Return claim** only)</span></span>
1. <span data-ttu-id="a9478-210">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a9478-210">Select **Create**.</span></span>

<span data-ttu-id="a9478-211">I følgende billede vises et eksempel på brugerstrøm til Azure AD B2C profilredigering.</span><span class="sxs-lookup"><span data-stu-id="a9478-211">The following image shows an example of the Azure AD B2C profile editing user flow.</span></span>

![Opret brugerstrømpolitikken til profilredigering](./media/B2CImage_12.png)

### <a name="create-a-password-reset-user-flow-policy"></a><span data-ttu-id="a9478-213">Opret en brugerstrømpolitik til nulstilling af adgangskode</span><span class="sxs-lookup"><span data-stu-id="a9478-213">Create a password reset user flow policy</span></span>

<span data-ttu-id="a9478-214">Gør følgende for at oprette en brugerstrømpolitik til nulstilling af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="a9478-214">To create a password reset user flow policy, follow these steps.</span></span>

1. <span data-ttu-id="a9478-215">Vælg **Brugerstrømme (politikker)** i navigationsruden til venstre i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="a9478-215">In the Azure portal, select **User flows (policies)** in the left navigation pane.</span></span>
1. <span data-ttu-id="a9478-216">Vælg **Ny brugerstrøm** på siden **Azure AD B2C – Brugerstrømme (politikker)**.</span><span class="sxs-lookup"><span data-stu-id="a9478-216">On the **Azure AD B2C – User flows (policies)** page, select **New User Flow**.</span></span>
1. <span data-ttu-id="a9478-217">Vælg **Nulstilling af adgangskode** på fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="a9478-217">On the **Recommended** tab, select **Password Reset**.</span></span>
1. <span data-ttu-id="a9478-218">Angiv et navn til brugerstrømmen til nulstilling af adgangskode under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a9478-218">Under **Name**, enter a name for the password reset user flow.</span></span>
1. <span data-ttu-id="a9478-219">Vælg **Nulstil adgangskode ved hjælp af mailadresse** under **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="a9478-219">Under **Identity providers**, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="a9478-220">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a9478-220">Select **Create**.</span></span>
1. <span data-ttu-id="a9478-221">Vælg følgende afkrydsningsfelter under **Programkrav**:</span><span class="sxs-lookup"><span data-stu-id="a9478-221">Under **Application claims**, select the following check boxes:</span></span>
    - <span data-ttu-id="a9478-222">**E-mail-adresser**</span><span class="sxs-lookup"><span data-stu-id="a9478-222">**Email addresses**</span></span>
    - <span data-ttu-id="a9478-223">**Givent navn**</span><span class="sxs-lookup"><span data-stu-id="a9478-223">**Given Name**</span></span>
    - <span data-ttu-id="a9478-224">**Efternavn**</span><span class="sxs-lookup"><span data-stu-id="a9478-224">**Surname**</span></span>
    - <span data-ttu-id="a9478-225">**Brugerens objekt-id**</span><span class="sxs-lookup"><span data-stu-id="a9478-225">**User's Object ID**</span></span>
1. <span data-ttu-id="a9478-226">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="a9478-226">Select **Create**.</span></span>

<span data-ttu-id="a9478-227">Følgende billede viser, hvor du kan indstille **Nulstil adgangskode ved hjælp af mailadresse** i en brugerstrøm til nulstilling af adgangskode i Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a9478-227">The following image shows where to set **Reset Password using mail address** in the Azure AD B2C password reset user flow.</span></span>

![Indstil "Nulstil adgangskode ved hjælp af mailadresse" i politikken Nulstil adgangskode](./media/B2CImage_13.png)

## <a name="add-social-identity-providers-optional"></a><span data-ttu-id="a9478-229">Tilføj sociale identitetsudbydere (valgfrit)</span><span class="sxs-lookup"><span data-stu-id="a9478-229">Add social identity providers (Optional)</span></span>

<span data-ttu-id="a9478-230">Sociale identitetsudbydere giver brugerne mulighed for at bruge deres sociale konti til godkendelse.</span><span class="sxs-lookup"><span data-stu-id="a9478-230">Social identity providers allow users to use their social accounts for authentication.</span></span> <span data-ttu-id="a9478-231">Tilføjelse af godkendelse af sociale identitetsudbydere er valgfri i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a9478-231">Adding social identity provider authentication is optional in Dynamics 365 Commerce.</span></span> 

<span data-ttu-id="a9478-232">Hvis godkendelse af sociale identitetsudbydere ikke tilføjes, vil Azure AD B2C-standardprofilerne være hovedprofilerne til din brugerbase.</span><span class="sxs-lookup"><span data-stu-id="a9478-232">If social identity provider authentication is not added, the default Azure AD B2C profiles will be the main profiles for your user base.</span></span> <span data-ttu-id="a9478-233">Brugerne vælger deres eget brugernavn (deres foretrukne mailadresse) og angiver en adgangskode.</span><span class="sxs-lookup"><span data-stu-id="a9478-233">Users will select their own username (their preferred email address) and set a password.</span></span> <span data-ttu-id="a9478-234">Azure AD B2C vil godkende brugere direkte.</span><span class="sxs-lookup"><span data-stu-id="a9478-234">Azure AD B2C will authenticate users directly.</span></span> 

<span data-ttu-id="a9478-235">Hvis godkendelse af sociale identitetsudbydere er tilføjet, og en bruger vælger en af de tilbudte sociale identitetsudbydere, oprettes der stadig en enhed i Azure AD B2C-lejeren.</span><span class="sxs-lookup"><span data-stu-id="a9478-235">If social identity provider authentication is added and a user chooses one of the social identity providers offered, an entity is still created in the Azure AD B2C tenant.</span></span> <span data-ttu-id="a9478-236">Azure AD B2C godkender derefter brugerens legitimationsoplysninger via den sociale identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="a9478-236">Azure AD B2C will then authenticate the user's credentials with the social identity provider.</span></span>

> [!NOTE]
> <span data-ttu-id="a9478-237">Identitetsudbyderens login opretter en post i B2C-lejeren, men i et andet format end lokale konti, da det kalder den eksterne sociale identitetsudbyders reference for godkendelse.</span><span class="sxs-lookup"><span data-stu-id="a9478-237">The identity provider sign in creates a record in the B2C tenant, but in a different format than local accounts since it will call the external social identity provider reference for authentication.</span></span> <span data-ttu-id="a9478-238">Brugeren kan bruge den samme mailadresse på tværs af sociale identitetsudbydere, hvilket betyder, at det brugernavn, der bruges til godkendelse af mailadressen, ikke er entydigt for lejeren.</span><span class="sxs-lookup"><span data-stu-id="a9478-238">The user can use the same email address across social identity providers, meaning that the email username used for authentication may not be unique to the tenant.</span></span> <span data-ttu-id="a9478-239">Azure AD B2C vil kun gennemtvinge, at brugere har en entydig mailadresse på lokale B2C-konti.</span><span class="sxs-lookup"><span data-stu-id="a9478-239">Azure AD B2C will only enforce that users have a unique email address on local B2C accounts.</span></span>

<span data-ttu-id="a9478-240">Før du kan tilføje en social identitetsudbyder til godkendelse, skal du gå til portalen for identitetsudbyderen og konfigurere et identitetsudbyderprogram som angivet i dokumentationen til Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a9478-240">Before you can add a social identity provider for authentication, you must go to the identity provider's portal and set up an identity provider application as instructed in the Azure AD B2C documentation.</span></span> <span data-ttu-id="a9478-241">Der findes en liste over links til dokumentationen nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a9478-241">A list of links to the documentation is provided below.</span></span>

- [<span data-ttu-id="a9478-242">Amazon</span><span class="sxs-lookup"><span data-stu-id="a9478-242">Amazon</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-amzn-app)
- [<span data-ttu-id="a9478-243">Azure AD (Enkelt lejer)</span><span class="sxs-lookup"><span data-stu-id="a9478-243">Azure AD (Single Tenant)</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-azure-active-directory)
- [<span data-ttu-id="a9478-244">Microsoft-konto</span><span class="sxs-lookup"><span data-stu-id="a9478-244">Microsoft Account</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-msa-app)
- [<span data-ttu-id="a9478-245">Facebook</span><span class="sxs-lookup"><span data-stu-id="a9478-245">Facebook</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-fb-app)
- [<span data-ttu-id="a9478-246">GitHub</span><span class="sxs-lookup"><span data-stu-id="a9478-246">GitHub</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-github-app)
- [<span data-ttu-id="a9478-247">Google</span><span class="sxs-lookup"><span data-stu-id="a9478-247">Google</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-goog-app)
- [<span data-ttu-id="a9478-248">LinkedIn</span><span class="sxs-lookup"><span data-stu-id="a9478-248">LinkedIn</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-li-app)
- [<span data-ttu-id="a9478-249">OpenID Connect</span><span class="sxs-lookup"><span data-stu-id="a9478-249">OpenID Connect</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-oidc-idp)
- [<span data-ttu-id="a9478-250">Twitter</span><span class="sxs-lookup"><span data-stu-id="a9478-250">Twitter</span></span>](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-setup-twitter-app)

### <a name="add-and-set-up-a-social-identity-provider"></a><span data-ttu-id="a9478-251">Tilføje og konfigurere en sociale identitetsudbyder</span><span class="sxs-lookup"><span data-stu-id="a9478-251">Add and set up a social identity provider</span></span>

<span data-ttu-id="a9478-252">Udfør følgende trin for at tilføje og konfigurere en social identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="a9478-252">To add and set up a social identity provider, follow these steps.</span></span>  

1. <span data-ttu-id="a9478-253">Naviger til **Identitetsudbydere** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="a9478-253">In the Azure portal, navigate to **Identity Providers**.</span></span>
1. <span data-ttu-id="a9478-254">Vælg **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="a9478-254">Select **Add**.</span></span> <span data-ttu-id="a9478-255">Skærmbilledet **Tilføj identitetsudbyder** vises.</span><span class="sxs-lookup"><span data-stu-id="a9478-255">The **Add identity provider** screen appears.</span></span>
1. <span data-ttu-id="a9478-256">Angiv det navn, der skal vises for brugere på din login-skærm, under **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a9478-256">Under **Name**, enter the name to be displayed to users on your sign in screen.</span></span>
1. <span data-ttu-id="a9478-257">Vælg en identitetsudbyder på listen under **Type identitetsudbyder**.</span><span class="sxs-lookup"><span data-stu-id="a9478-257">Under **Identity provider type**, select an identity provider from the list.</span></span>
1. <span data-ttu-id="a9478-258">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9478-258">Select **OK**.</span></span>
1. <span data-ttu-id="a9478-259">Vælg **Konfigurer denne identitetsudbyder** for at få adgang til skærmbilledet **Konfigurer den sociale identitetsudbyder** .</span><span class="sxs-lookup"><span data-stu-id="a9478-259">Select **Set up this identity provider** to access the **Set up the social identity provider** screen.</span></span>
1. <span data-ttu-id="a9478-260">Angiv det klient-id, der er hentet fra installationsprogrammet til identitetsudbyderen, under **Klient-id**.</span><span class="sxs-lookup"><span data-stu-id="a9478-260">Under **Client ID**, enter the client ID as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="a9478-261">Angiv den klienthemmelighed, der er hentet fra installationsprogrammet til identitetsudbyderen, under **Klienthemmelighed**.</span><span class="sxs-lookup"><span data-stu-id="a9478-261">Under **Client secret**, enter the client secret as obtained from the identity provider application setup.</span></span>
1. <span data-ttu-id="a9478-262">Knyt brugerstrøm til tilmeldings- og login-politikker:</span><span class="sxs-lookup"><span data-stu-id="a9478-262">Attach user flow for sign in sign up policies:</span></span>
1. <span data-ttu-id="a9478-263">Gå til **Azure AD B2C – Brugerstrømme (politikker) \> {din tilmeldings- og logon-politik} \> Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="a9478-263">Go to **Azure AD B2C – User flows (policies) \> {your sign-in sign-up policy} \> Identity providers**.</span></span>
1. <span data-ttu-id="a9478-264">Hvis du vil knytte brugerstrømmen til login/tilmeldingspolitikken, skal du vælge hver af de identitetsudbydere, du har konfigureret til din konto.</span><span class="sxs-lookup"><span data-stu-id="a9478-264">To attach the sign in/sign up user flow policy, select each identity provider you have set up for your account.</span></span> <span data-ttu-id="a9478-265">Hvis du vil teste disse, skal du vælge **Kør brugerstrøm** for hver identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="a9478-265">To test these, select **Run user flow** for each identity provider.</span></span> <span data-ttu-id="a9478-266">Login-siden vises på en ny fane, og der vises et valgfelt til den nye identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="a9478-266">A new tab will display the sign-in page displaying the new identity provider selection box.</span></span>

<span data-ttu-id="a9478-267">I følgende billede vises eksempler på skærmbillederne **Tilføj identitetsudbyder** og **Konfigurerer sociale identitetsudbydere** i Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a9478-267">The following image shows examples of the **Add identity provider** and **Set up the social identity provider** screens in Azure AD B2C.</span></span>

![Føje en social identitetsudbyder til dit program](./media/B2CImage_14.png)

<span data-ttu-id="a9478-269">I følgende billede vises et eksempel på, hvordan du kan vælge identitetsudbydere på siden Azure AD B2C **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="a9478-269">The following image shows an example of how to select identity providers on the Azure AD B2C **Identity Providers** page.</span></span>

![Vælg alle de sociale identitetsudbydere, der skal aktiveres for din politik](./media/B2CImage_16.png)

<span data-ttu-id="a9478-271">I følgende billede vises et eksempel på en standardlogin-skærm, hvor der vises en knap til login på en social identitetsudbyder.</span><span class="sxs-lookup"><span data-stu-id="a9478-271">The following image shows an example of a default sign-in screen with a social identity provider sign-in button displayed.</span></span>

![Eksempel på standardlogin-skærm med knap til login til social identitetsudbyder](./media/B2CImage_17.png)

## <a name="update-commerce-headquarters-with-the-new-azure-ad-b2c-information"></a><span data-ttu-id="a9478-273">Opdater Commerce Headquarters med de nye Azure AD B2C-oplysninger</span><span class="sxs-lookup"><span data-stu-id="a9478-273">Update Commerce headquarters with the new Azure AD B2C information</span></span>

<span data-ttu-id="a9478-274">Når du har udført overstående trin til Azure AD B2C-klargøring, skal Azure AD B2C-programmet registreres i dit Dynamics 365 Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="a9478-274">Once the Azure AD B2C provisioning steps above are completed, the Azure AD B2C application must be registered in your Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="a9478-275">Udfør følgende trin for at opdatere Headquarters med de nye Azure AD B2C-oplysninger.</span><span class="sxs-lookup"><span data-stu-id="a9478-275">To update headquarters with the new Azure AD B2C information, follow these steps.</span></span>

1. <span data-ttu-id="a9478-276">Gå til **Delte Commerce-parametre** i Commerce, og vælg **Identitetsudbydere** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="a9478-276">In Commerce, go to **Commerce Shared Parameters** and select **Identity Providers** in the left menu.</span></span>
1. <span data-ttu-id="a9478-277">Gør følgende under **Identitetsudbydere**:</span><span class="sxs-lookup"><span data-stu-id="a9478-277">Under **Identity Providers**, do the following:</span></span>
    1. <span data-ttu-id="a9478-278">Angiv URL-adressen til udbyderen af identitetsudbydere i feltet **Udbyder**.</span><span class="sxs-lookup"><span data-stu-id="a9478-278">In the **Issuer** box, enter the identity provider issuer URL.</span></span> <span data-ttu-id="a9478-279">Du kan finde URL-adressen til udstederen [Få udsteders URL-adresse](#obtain-issuer-url) nedenfor.</span><span class="sxs-lookup"><span data-stu-id="a9478-279">To find your issuer URL, see [Obtain issuer URL](#obtain-issuer-url) below.</span></span>
    1. <span data-ttu-id="a9478-280">Skriv et navn på din udbyderpost i feltet **Navn**.</span><span class="sxs-lookup"><span data-stu-id="a9478-280">In the **Name** box, enter a name for your issuer record.</span></span>
    1. <span data-ttu-id="a9478-281">Skriv **Azure AD B2C (id_token)** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="a9478-281">In the **Type** box, enter **Azure AD B2C (id_token)**.</span></span>
1. <span data-ttu-id="a9478-282">Gør følgende under **Betroede parter** med ovenstående B2C-identitetsudbyderelement valgt:</span><span class="sxs-lookup"><span data-stu-id="a9478-282">Under **Relying Parties**, with the above B2C identity provider item selected, do the following:</span></span>
    1. <span data-ttu-id="a9478-283">Angiv dit B2C-program-id i feltet **Klient-id**.</span><span class="sxs-lookup"><span data-stu-id="a9478-283">In the **ClientID** box, enter your B2C application ID.</span></span> <span data-ttu-id="a9478-284">Du kan finde dette i feltet **Program-id** på siden med egenskaber for B2C-programmet.</span><span class="sxs-lookup"><span data-stu-id="a9478-284">You can find this in the **Application ID** box of your B2C application's properties page.</span></span>
    1. <span data-ttu-id="a9478-285">Skriv **Offentlig** i feltet **Type**.</span><span class="sxs-lookup"><span data-stu-id="a9478-285">In the **Type** box, enter **Public**.</span></span>
    1. <span data-ttu-id="a9478-286">Skriv **Kunde** i feltet **Brugertype**.</span><span class="sxs-lookup"><span data-stu-id="a9478-286">In the **User Type** box, enter **Customer**.</span></span>
1. <span data-ttu-id="a9478-287">Gå til handlingsruden, og vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="a9478-287">On the action pane, select **Save**.</span></span>
1. <span data-ttu-id="a9478-288">Søg efter **Distributionsplan** i feltet Commerce-søgning</span><span class="sxs-lookup"><span data-stu-id="a9478-288">In the Commerce search box, search for **Distribution schedule**</span></span>
1. <span data-ttu-id="a9478-289">Vælg job **1110 global konfiguration** i den venstre navigationsmenu på siden **Distributionsplaner**.</span><span class="sxs-lookup"><span data-stu-id="a9478-289">In the left navigation menu of the **Distribution schedules** page, select job **1110 Global configuration**.</span></span>
1. <span data-ttu-id="a9478-290">Vælg **Kør nu** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="a9478-290">On the action pane, select **Run Now**.</span></span>

### <a name="obtain-issuer-url"></a><span data-ttu-id="a9478-291">Hent URL-adresse til udsteder</span><span class="sxs-lookup"><span data-stu-id="a9478-291">Obtain issuer URL</span></span>

<span data-ttu-id="a9478-292">Følg disse trin for at få URL-adressen til identitetsudbyderens udsteder.</span><span class="sxs-lookup"><span data-stu-id="a9478-292">To obtain your identity provider issuer URL, follow these steps.</span></span>

1. <span data-ttu-id="a9478-293">Opret en URL-metadataadresse i følgende format med din B2C-lejer og -politik: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span><span class="sxs-lookup"><span data-stu-id="a9478-293">Create a metadata address URL in the following format using your B2C tenant and policy: ``https://<B2CTENANTNAME>.b2clogin.com/<B2CTENANTNAME>.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=<B2CSIGN-INPOLICY>``</span></span>
    - <span data-ttu-id="a9478-294">Eksempel: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span><span class="sxs-lookup"><span data-stu-id="a9478-294">Example: ``https://d365plc.b2clogin.com/d365plc.onmicrosoft.com/v2.0/.well-known/openid-configuration?p=B2C_1_signinup``.</span></span>
1. <span data-ttu-id="a9478-295">Angiv URL-metadataadressen i en browsers adresselinje.</span><span class="sxs-lookup"><span data-stu-id="a9478-295">Enter the metadata address URL into a browser address bar.</span></span>
1. <span data-ttu-id="a9478-296">Kopier URL-adressen til identitetsudbyderens udsteder (værdien for **"udsteder"**) i metadataene.</span><span class="sxs-lookup"><span data-stu-id="a9478-296">In the metadata, copy the identity provider issuer URL (the value for **"issuer"**).</span></span>
    - <span data-ttu-id="a9478-297">Eksempel: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span><span class="sxs-lookup"><span data-stu-id="a9478-297">Example: ``https://login.fabrikam.com/073405c3-0113-4f43-b5e2-df01266e24ae/v2.0/``.</span></span>

## <a name="configure-your-b2c-tenant-in-commerce-site-builder"></a><span data-ttu-id="a9478-298">Konfigurere din B2C-lejer i Commerce-webstedsgeneratoren</span><span class="sxs-lookup"><span data-stu-id="a9478-298">Configure your B2C tenant in Commerce site builder</span></span>

<span data-ttu-id="a9478-299">Når konfigurationen af din Azure AD B2C-lejer er fuldført, skal du konfigurere B2C-lejeren i Commerce-webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="a9478-299">Once setup of your Azure AD B2C tenant is completed, you must configure the B2C tenant in Commerce site builder.</span></span> <span data-ttu-id="a9478-300">Konfigurationstrin omfatter indsamling af oplysninger om B2C-programmet fra Azure-portalen, indtastning af B2C-programoplysninger i webstedsgeneratoren og derefter tilknytning af B2C-programmet til dit webstedsted og din kanal.</span><span class="sxs-lookup"><span data-stu-id="a9478-300">Configuration steps include collecting B2C application information from the Azure portal, entering that B2C application information into site builder, and then associating the B2C application with your site and channel.</span></span>

### <a name="collect-the-required-application-information"></a><span data-ttu-id="a9478-301">Indsaml de nødvendige programoplysninger</span><span class="sxs-lookup"><span data-stu-id="a9478-301">Collect the required application information</span></span>

<span data-ttu-id="a9478-302">Udfør følgende trin for at indsamle de nødvendige programoplysninger.</span><span class="sxs-lookup"><span data-stu-id="a9478-302">To collect the required application information, follow these steps.</span></span>

1. <span data-ttu-id="a9478-303">Gå til **Start \> Azure AD B2C-programmer** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="a9478-303">In the Azure portal, go to **Home \> Azure AD B2C - Applications**.</span></span>
1. <span data-ttu-id="a9478-304">Vælg dit program, og vælg derefter **Egenskaber** i venstre navigationsrude for at få oplysninger om programmet.</span><span class="sxs-lookup"><span data-stu-id="a9478-304">Select your application, and then in the left navigation pane select **Properties** to obtain the application details.</span></span>
1. <span data-ttu-id="a9478-305">I boksen **Program-id** skal du indsamle program-id'et for det B2C-program, der er oprettet i din B2C-lejer.</span><span class="sxs-lookup"><span data-stu-id="a9478-305">From the **Application ID** box, collect the application ID of the B2C application created in your B2C tenant.</span></span> <span data-ttu-id="a9478-306">Det vil senere blive angivet som **Klient-GUID** i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="a9478-306">This will later be entered as the **Client GUID** in site builder.</span></span>
1. <span data-ttu-id="a9478-307">Hent svar-URL-adressen under **Svar-URL-adresse**.</span><span class="sxs-lookup"><span data-stu-id="a9478-307">Under **Reply URL**, collect the reply URL.</span></span>
1. <span data-ttu-id="a9478-308">Gå til **Start \> Azure AD B2C – Brugerstrømme (politikker)**, og indsaml derefter navnene på hver enkelt brugerstrømpolitik.</span><span class="sxs-lookup"><span data-stu-id="a9478-308">Go to **Home \> Azure AD B2C – User flows (policies)**, and then collect the names of each user flow policy.</span></span>

<span data-ttu-id="a9478-309">I følgende billede vises et eksempel på siden **Azure AD B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="a9478-309">The following image shows an example of the **Azure AD B2C - Applications** page.</span></span>

![Naviger til B2C-programmet i din lejer](./media/B2CImage_19.png)

<span data-ttu-id="a9478-311">I følgende billede vises et eksempel på siden **Egenskaber** for et program i Azure AD B2C.</span><span class="sxs-lookup"><span data-stu-id="a9478-311">The following image shows an example of an application **Properties** page in Azure AD B2C.</span></span> 

![Kopiér program-id'et fra egenskaberne for B2C-programmet](./media/B2CImage_21.png)

<span data-ttu-id="a9478-313">I følgende billede vises et eksempel på brugerstrømpolitikker på siden **Azure AD B2C – Brugerstrømme (politikker)**.</span><span class="sxs-lookup"><span data-stu-id="a9478-313">The following image shows an example of user flow policies on the **Azure AD B2C – User flows (policies)** page.</span></span>

![Indsaml navnene på de enkelte B2C-politikstrømme](./media/B2CImage_22.png)

### <a name="enter-your-aad-b2c-tenant-application-information-into-commerce"></a><span data-ttu-id="a9478-315">Angiv programoplysninger om din AAD B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="a9478-315">Enter your AAD B2C tenant application information into Commerce</span></span>

<span data-ttu-id="a9478-316">Du skal angive oplysninger om Azure AD B2C-lejeren i Commerce-webstedsgenerator, før du knytter B2C-lejeren til dit eller dine websteder.</span><span class="sxs-lookup"><span data-stu-id="a9478-316">You must enter details of the Azure AD B2C tenant into Commerce site builder before associating the B2C tenant with your site(s).</span></span>

<span data-ttu-id="a9478-317">Udfør følgende trin for at føje AAD B2C-lejerens programoplysninger til Commerce.</span><span class="sxs-lookup"><span data-stu-id="a9478-317">To add your AAD B2C tenant application information to Commerce, follow these steps.</span></span>

1. <span data-ttu-id="a9478-318">Log på som administrator af Commerce-webstedsgenerator for dit miljø.</span><span class="sxs-lookup"><span data-stu-id="a9478-318">Sign in as an administrator to Commerce site builder for your environment.</span></span>
1. <span data-ttu-id="a9478-319">Vælg **Lejerindstillinger** i venstre navigationsrude for at udvide den.</span><span class="sxs-lookup"><span data-stu-id="a9478-319">In the left navigation pane, select **Tenant Settings**  to expand it.</span></span>
1. <span data-ttu-id="a9478-320">Vælg **B2C-indstillinger** under **Lejerindstillinger**.</span><span class="sxs-lookup"><span data-stu-id="a9478-320">Under **Tenant Settings**, select **B2C Settings**.</span></span> 
1. <span data-ttu-id="a9478-321">Vælg **Administrer** i hovedvinduet ved siden af **B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="a9478-321">In the main window next **B2C Applications**, select **Manage**.</span></span> <span data-ttu-id="a9478-322">(Hvis lejeren vises på B2C-programlisten, er den allerede blevet tilføjet af en administrator.</span><span class="sxs-lookup"><span data-stu-id="a9478-322">(If your tenant appears in the B2C Applications list, then it was already added by an administrator.</span></span> <span data-ttu-id="a9478-323">Kontrollér, at punkterne i trin 6 nedenfor svarer til dit B2C-program.)</span><span class="sxs-lookup"><span data-stu-id="a9478-323">Verify that the items in step 6 below match your B2C Application.)</span></span>
1. <span data-ttu-id="a9478-324">Vælg **Tilføj B2C-program**.</span><span class="sxs-lookup"><span data-stu-id="a9478-324">Select **Add B2C Application**.</span></span>
1. <span data-ttu-id="a9478-325">Angiv følgende påkrævede punkter i formularen, der vises, ved at bruge værdier fra B2C-lejeren og -programmet.</span><span class="sxs-lookup"><span data-stu-id="a9478-325">Enter the following required items in the form displayed, using values from your B2C tenant and application.</span></span> <span data-ttu-id="a9478-326">Felter, der ikke er obligatoriske (dvs. uden en stjerne), kan være tomme.</span><span class="sxs-lookup"><span data-stu-id="a9478-326">Fields that are not required (those without an asterisk) may be left blank.</span></span>

    - <span data-ttu-id="a9478-327">**Programnavn**: Navnet på dit B2C-program, f.eks. "Fabrikam B2C".</span><span class="sxs-lookup"><span data-stu-id="a9478-327">**Application Name**: The name for your B2C Application, for example "Fabrikam B2C".</span></span>
    - <span data-ttu-id="a9478-328">**Navn på lejer**: Navnet på din B2C-lejer (f.eks. brug "fabrikam", hvis domænet vises som "fabrikam.onmicrosoft.com" for B2C-lejeren).</span><span class="sxs-lookup"><span data-stu-id="a9478-328">**Tenant Name**: The name of your B2C tenant (for example, use "fabrikam" if the domain appears as "fabrikam.onmicrosoft.com" for the B2C tenant).</span></span> 
    - <span data-ttu-id="a9478-329">**Glem adgangskodepolitik-id**: Politik-id for brugerstrømmen for glemt adgangskode, f.eks. "B2C_1_PasswordReset".</span><span class="sxs-lookup"><span data-stu-id="a9478-329">**Forget Password Policy ID**: The forget password user flow policy ID, for example "B2C_1_PasswordReset".</span></span>
    - <span data-ttu-id="a9478-330">**Politik-id for tilmelding og logon**: Politik-id for tilmelding og logon i brugerstrømmen, f.eks. "B2C_1_signup_signin".</span><span class="sxs-lookup"><span data-stu-id="a9478-330">**Signup Signin Policy ID**: The sign up and sign in user flow policy ID, for example "B2C_1_signup_signin".</span></span>
    - <span data-ttu-id="a9478-331">**Klient-GUID**: B2C-program-id'et, f.eks. "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span><span class="sxs-lookup"><span data-stu-id="a9478-331">**Client GUID**: The B2C application ID, for example "22290eb2-c52e-42e9-8b35-a2b0a3bcb9e6".</span></span>
    - <span data-ttu-id="a9478-332">**Rediger profilpolitik-id**: Politik-id'et for brugerstrømmen til profilredigering, f.eks. "B2C_1A_ProfileEdit".</span><span class="sxs-lookup"><span data-stu-id="a9478-332">**Edit Profile Policy ID**: The profile editing user flow policy ID, for example "B2C_1A_ProfileEdit".</span></span>

1. <span data-ttu-id="a9478-333">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="a9478-333">Select **OK**.</span></span> <span data-ttu-id="a9478-334">Navnet på dit B2C-program vises nu på listen.</span><span class="sxs-lookup"><span data-stu-id="a9478-334">You should now see the name of your B2C application appear in the list.</span></span>
1. <span data-ttu-id="a9478-335">Vælg **Gem** for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="a9478-335">Select **Save** to save your changes.</span></span>

### <a name="associate-the-b2c-application-to-your-site-and-channel"></a><span data-ttu-id="a9478-336">Knyt B2C-programmet til dit websted og din kanal</span><span class="sxs-lookup"><span data-stu-id="a9478-336">Associate the B2C application to your site and channel</span></span>

> [!WARNING]
> <span data-ttu-id="a9478-337">Hvis dit websted allerede er knyttet til et B2C program, og du skifter til et andet B2C-program, fjernes de aktuelle referencer, der er oprettet for brugere, som allerede er tilmeldt i dette miljø.</span><span class="sxs-lookup"><span data-stu-id="a9478-337">If your site is already associated with a B2C application, changing to a different B2C application will remove the current references established for users already signed up in this environment.</span></span> <span data-ttu-id="a9478-338">Hvis de ændres, vil alle legitimationsoplysninger, der er knyttet til det aktuelt tildelte B2C-program, ikke være tilgængelige for brugerne.</span><span class="sxs-lookup"><span data-stu-id="a9478-338">If changed, any credentials associated with the currently-assigned B2C application will not be available to users.</span></span> 
> 
> <span data-ttu-id="a9478-339">Du skal kun opdatere kun B2C-programmet, hvis du konfigurerer kanalens B2C-program for første gang, eller hvis du vil have, at brugere skal tilmelde sig med nye legitimationsoplysninger til denne kanal med det nye B2C-program.</span><span class="sxs-lookup"><span data-stu-id="a9478-339">Only update the B2C application if you are setting up the channel's B2C application for the first time or if you intend to have users re-sign up with new credentials to this channel with the new B2C application.</span></span> <span data-ttu-id="a9478-340">Vær forsigtig, når du knytter kanaler til B2C-programmer, og navngiv programmer tydeligt.</span><span class="sxs-lookup"><span data-stu-id="a9478-340">Take caution when associating channels to B2C applications, and name applications clearly.</span></span> <span data-ttu-id="a9478-341">Hvis en kanal ikke er knyttet til et B2C-program i trinnene nedenfor, vil de brugere, der logger på den pågældende kanal til dit websted, blive angivet i B2C-programmet, der vises som **standard** på listen **Lejerindstillinger \> B2C-indstillinger** for B2C-programmer.</span><span class="sxs-lookup"><span data-stu-id="a9478-341">If a channel is not associated to a B2C application in the steps below, users signing into that channel for your site will be entered into the B2C application showing as **default** in the **Tenant Settings \> B2C Settings** list of B2C applications.</span></span>

<span data-ttu-id="a9478-342">Gør følgende for at knytte B2C-programmet til dit websted og din kanal.</span><span class="sxs-lookup"><span data-stu-id="a9478-342">To associate the B2C application to your site and channel, follow these steps.</span></span>

1. <span data-ttu-id="a9478-343">Naviger til dit websted i Commerce-webstedsgenerator.</span><span class="sxs-lookup"><span data-stu-id="a9478-343">Navigate to your site in Commerce site builder.</span></span>
1. <span data-ttu-id="a9478-344">Vælg **Indstillinger for websted** i venstre navigationsrude for at udvide den.</span><span class="sxs-lookup"><span data-stu-id="a9478-344">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="a9478-345">Vælg **Kanaler** nedenunder **Indstillinger for websted**.</span><span class="sxs-lookup"><span data-stu-id="a9478-345">Below **Site Settings**, select **Channels**.</span></span>
1. <span data-ttu-id="a9478-346">Vælg kanalen i hovedvinduet under **Kanaler**.</span><span class="sxs-lookup"><span data-stu-id="a9478-346">In the main window under **Channels**, select your channel.</span></span>
1. <span data-ttu-id="a9478-347">I ruden Egenskaber for kanal til højre skal du vælge navnet på dit B2C-program i rullemenuen **Vælg B2C-program**.</span><span class="sxs-lookup"><span data-stu-id="a9478-347">In the channel properties pane on the right, select your B2C application name from the **Select B2C Application** drop down menu.</span></span>
1. <span data-ttu-id="a9478-348">Vælg **Luk**, og vælg derefter **Gem og udgiv**.</span><span class="sxs-lookup"><span data-stu-id="a9478-348">Select **Close**, and then select **Save and Publish**.</span></span>

## <a name="additional-b2c-information"></a><span data-ttu-id="a9478-349">Flere B2C-oplysninger</span><span class="sxs-lookup"><span data-stu-id="a9478-349">Additional B2C information</span></span>

### <a name="customer-migration"></a><span data-ttu-id="a9478-350">Kundeoverflytning</span><span class="sxs-lookup"><span data-stu-id="a9478-350">Customer migration</span></span>

<span data-ttu-id="a9478-351">Hvis du overvejer at overflytte kundeposter fra en tidligere identitetsudbyderplatform, skal du arbejde med Dynamics 365 Commerce-teamet for at gennemgå dine behov for kundeoverflytning.</span><span class="sxs-lookup"><span data-stu-id="a9478-351">If you are considering migrating customer records from a previous identity provider platform, please work with the Dynamics 365 Commerce team to review your customer migration needs.</span></span>

<span data-ttu-id="a9478-352">Du kan få yderligere Azure AD B2C-dokumentation om kundeoverflytning under [Overflytte brugere til Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span><span class="sxs-lookup"><span data-stu-id="a9478-352">For additional Azure AD B2C documentation on customer migration, see [Migrate users to Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-user-migration).</span></span>

### <a name="custom-policies"></a><span data-ttu-id="a9478-353">Brugerdefinerede politikker</span><span class="sxs-lookup"><span data-stu-id="a9478-353">Custom policies</span></span>

<span data-ttu-id="a9478-354">Du kan få yderligere oplysninger om tilpasning af Azure AD B2C-interaktioner og politikstrømme, der ligger ud over, hvad der tilbydes af B2C standardpolitikker, i [Tilpassede politikker i Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span><span class="sxs-lookup"><span data-stu-id="a9478-354">For additional information regarding customizing Azure AD B2C interactions and policy flows beyond what is offered by B2C standard policies, see [Custom policies in Azure Active Directory B2C](https://docs.microsoft.com/azure/active-directory-b2c/active-directory-b2c-overview-custom).</span></span> 

### <a name="secondary-admin"></a><span data-ttu-id="a9478-355">Sekundær administrator</span><span class="sxs-lookup"><span data-stu-id="a9478-355">Secondary admin</span></span>

<span data-ttu-id="a9478-356">Du kan tilføje en valgfri, sekundær administratorkonto under afsnittet **Bruger** i din B2C-lejer.</span><span class="sxs-lookup"><span data-stu-id="a9478-356">An optional, secondary administrator account can be added in the **Users** section of your B2C tenant.</span></span> <span data-ttu-id="a9478-357">Det kan være en direkte konto eller en generel konto.</span><span class="sxs-lookup"><span data-stu-id="a9478-357">This can be a direct account or a general account.</span></span> <span data-ttu-id="a9478-358">Hvis du skal dele en konto på tværs af teamressourcer, kan du også oprette en fælles konto.</span><span class="sxs-lookup"><span data-stu-id="a9478-358">If you need to share an account across team resources, a common account can also be created.</span></span> <span data-ttu-id="a9478-359">På grund af følsomheden for de data der er lagret i Azure AD B2C, skal en fælles konto overvåges nøje i følge firmaets sikkerhedspraksis.</span><span class="sxs-lookup"><span data-stu-id="a9478-359">Due to the sensitivity of the data stored in Azure AD B2C, a common account should be monitored closely per your company's security practices.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a9478-360">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a9478-360">Additional resources</span></span>

[<span data-ttu-id="a9478-361">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="a9478-361">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="a9478-362">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="a9478-362">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="a9478-363">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="a9478-363">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="a9478-364">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="a9478-364">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="a9478-365">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="a9478-365">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

<span data-ttu-id="a9478-366">[Masseoverføre omdirigeringer af URL-adresser](upload-bulk-redirects.md)Knyt et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="a9478-366">[Upload URL redirects in bulk](upload-bulk-redirects.md)Associate a Dynamics 365 Commerce site with an online channel</span></span>

[<span data-ttu-id="a9478-367">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="a9478-367">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="a9478-368">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="a9478-368">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="a9478-369">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="a9478-369">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="a9478-370">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="a9478-370">Enable location-based store detection</span></span>](enable-store-detection.md)
