---
title: Konfigurere brugerdefinerede sider til brugerlogon
description: Dette emne beskriver, hvordan du bygger tilpassede sider i Microsoft Dynamics 365 Commerce, der håndterer tilpasset logon for brugere af Azure Active Directory (Azure AD) Business-to-Consumer-lejere (B2C).
author: brianshook
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 3328fad5328ae1954a6749f9a5eebcb71c723698
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5477942"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="ab2ef-103">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="ab2ef-103">Set up custom pages for user sign-ins</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="ab2ef-104">Dette emne beskriver, hvordan du bygger tilpassede sider i Microsoft Dynamics 365 Commerce, der håndterer tilpasset logon for brugere af Azure Active Directory (Azure AD) Business-to-Consumer-lejere (B2C).</span><span class="sxs-lookup"><span data-stu-id="ab2ef-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

<span data-ttu-id="ab2ef-105">Hvis du vil bruge brugerdefinerede sider, der er oprettet i Dynamics 365 Commerce, til at håndtere brugerlogon, skal du konfigurere de Azure AD-politikker, der skal refereres til i Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-105">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="ab2ef-106">Du kan konfigurere Azure AD B2C-politikkerne "Tilmelding og logon", "Profilredigering" og "Nulstilling af adgangskode" ved hjælp af Azure AD B2C-programmet.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-106">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="ab2ef-107">Der kan derefter refereres til Azure AD B2C-lejeren og politiknavne under den klargørings proces, der udføres for Commerce-miljøet ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ab2ef-107">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="ab2ef-108">De brugerdefinerede Commerce-sider kan opbygges ved hjælp af modulet til logon, tilmelding, kontoprofilredigering eller genstart af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-108">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="ab2ef-109">De URL-adresser til sider, der udgives for disse brugerdefinerede sider, skal derefter refereres i Azure AD B2C-politikkonfigurationerne i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-109">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="ab2ef-110">Konfigurere B2C-politikker</span><span class="sxs-lookup"><span data-stu-id="ab2ef-110">Set up B2C policies</span></span>

<span data-ttu-id="ab2ef-111">Når du har konfigureret din Azure AD B2C-lejer og har knyttet den til Commerce-miljøet, skal du gå siden **Azure AD B2C** i Azure-portalen og derefter vælge **Brugerstrømme (politikker)** i menuen under **Politikker**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-111">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Kommandoen Brugerstrømme (politikker) i menuen](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="ab2ef-113">Du kan nu konfigurere brugerlogonstrømmene "Tilmelding og logon", "Profilredigering" og "Nulstilling af adgangskode".</span><span class="sxs-lookup"><span data-stu-id="ab2ef-113">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="ab2ef-114">Konfigurere politikken "Tilmelding og logon"</span><span class="sxs-lookup"><span data-stu-id="ab2ef-114">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="ab2ef-115">For at konfigurere politikken "Tilmelding og logon" skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-115">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="ab2ef-116">Vælg **Ny brugerstrøm**, og vælg derefter politikken **Tilmelding og logon** under fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-116">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="ab2ef-117">Angiv et navn til politikken (f.eks. **B2C\_1\_TilmeldingLogon**).</span><span class="sxs-lookup"><span data-stu-id="ab2ef-117">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="ab2ef-118">Vælg de id-udbydere, der skal bruges til politikken, i sektionen **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-118">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="ab2ef-119">Du skal som minimum vælge **E-mailtilmelding**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-119">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="ab2ef-120">I kolonnen **Indsaml attribut** skal du markere afkrydsningsfelterne for **E-mailadresse**, **Tildelt navn** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-120">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="ab2ef-121">I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Identitetsudbyder**, **Efternavn** og **Brugerens objekt-id**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-121">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Valgte attributter og krav](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="ab2ef-123">Vælg **OK** for at oprette politikken.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-123">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="ab2ef-124">Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-124">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="ab2ef-125">Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-125">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Siden Egenskaber for den nye politik](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="ab2ef-127">Der bliver refereret til hele politiknavnet i Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-127">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="ab2ef-128">(**B2C\_1\_**-præfikset bliver medtaget i referencen). Politikker kan ikke omdøbes, når de først er oprettet.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-128">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="ab2ef-129">Hvis du erstatter en eksisterende politik for Commerce-miljøet, kan du slette den oprindelige politik og oprette en ny politik med samme navn.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-129">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="ab2ef-130">Hvis miljøet allerede er blevet klargjort, kan du også sende det nye politiknavn via en serviceanmodning.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-130">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="ab2ef-131">Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-131">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="ab2ef-132">Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-132">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="ab2ef-133">Konfigurere politikken "Profilredigering"</span><span class="sxs-lookup"><span data-stu-id="ab2ef-133">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="ab2ef-134">Du kan konfigurere politikken "Profilredigering" ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-134">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="ab2ef-135">Vælg **Ny brugerstrøm**, og vælg derefter politikken **Profilredigering** under fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-135">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="ab2ef-136">Angiv et navn til politikken (f.eks. **B2C\_1\_RedigerProfil**).</span><span class="sxs-lookup"><span data-stu-id="ab2ef-136">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="ab2ef-137">Vælg de id-udbydere, der skal bruges til politikken, i sektionen **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-137">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="ab2ef-138">Der skal som minimum være valgt **Log på lokal konto**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-138">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="ab2ef-139">I kolonnen **Indsaml attribut** skal du markere afkrydsningsfelterne for **E-mailadresse** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-139">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="ab2ef-140">I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Identitetsudbyder**, **Efternavn** og **Brugerens objekt-id**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-140">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="ab2ef-141">Vælg **OK** for at oprette politikken.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-141">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="ab2ef-142">Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-142">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="ab2ef-143">Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-143">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="ab2ef-144">Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-144">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="ab2ef-145">Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-145">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="ab2ef-146">Konfigurere politikken "Nulstilling af adgangskode"</span><span class="sxs-lookup"><span data-stu-id="ab2ef-146">Configure the "Password reset" policy</span></span>

<span data-ttu-id="ab2ef-147">Du kan konfigurere politikken "Nulstilling af adgangskode" ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-147">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="ab2ef-148">Vælg **Ny brugerstrøm**, og vælg derefter politikken **Nulstilling af adgangskode v1.1** under fanen **Eksempel**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-148">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Politikken for Nulstilling af adgangskode v.1.1 valgt under fanen Eksempel](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="ab2ef-150">Angiv et navn til politikken (f.eks. **B2C\_1\_GlemtAdgangskode**).</span><span class="sxs-lookup"><span data-stu-id="ab2ef-150">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="ab2ef-151">Vælg **Nulstil adgangskode ved hjælp af e-mailadresse** i sektionen **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-151">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="ab2ef-152">I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Efternavn** og **Brugerens objekt-id**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-152">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Valgte krav](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="ab2ef-154">Vælg **OK** for at oprette politikken.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-154">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="ab2ef-155">Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-155">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="ab2ef-156">Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-156">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="ab2ef-157">Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-157">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="ab2ef-158">Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-158">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="ab2ef-159">Oprette brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="ab2ef-159">Build the custom pages</span></span>

<span data-ttu-id="ab2ef-160">Udfør følgende trin for at opbygge de brugerdefinerede sider til håndtering af brugerlogon.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-160">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="ab2ef-161">Gå til dit websted i Commerce-oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-161">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="ab2ef-162">Opbyg følgende fem skabeloner og fem sider:</span><span class="sxs-lookup"><span data-stu-id="ab2ef-162">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="ab2ef-163">En **Logon**-skabelon og -side, der bruger logonmodulet.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-163">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="ab2ef-164">En **Logon**-skabelon og -side, der bruger logonmodulet.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-164">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="ab2ef-165">En skabelon og side til **Nulstilling af adgangskod**, der bruger modulet til nulstilling af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-165">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="ab2ef-166">En skabelon og side til **Bekræftelse af nulstilling af adgangskod**, der bruger modulet til bekræftelse af nulstilling af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-166">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="ab2ef-167">En skabelon og side til **Profilredigering**, der bruger modulet til redigering af kontoprofilen</span><span class="sxs-lookup"><span data-stu-id="ab2ef-167">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="ab2ef-168">Når du opbygger siderne, skal du følge disse retningslinjer:</span><span class="sxs-lookup"><span data-stu-id="ab2ef-168">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="ab2ef-169">For hver side eller hvert modul skal du bruge det layout og den typografi, der passer bedst til dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-169">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="ab2ef-170">Udgiv alle sider og URL-adresser, der skal bruges i Azure AD B2C-opsætningen.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-170">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="ab2ef-171">Når siderne og URL-adresserne er publiceret, skal du indsamle de URL-adresser, der skal bruges til konfigurationer af Azure AD B2C-politikken.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-171">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="ab2ef-172">Der føjes et **?preloadscripts=true**-suffiks til hver URL-adresse, når den bruges.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-172">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="ab2ef-173">Du må ikke genbruge universelle sidehoveder og sidefødder, der har relative hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-173">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="ab2ef-174">Da disse sider findes på Azure AD B2C-domænet, når de bruges, bør der kun bruges absolutte URL-adresser til alle links.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-174">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="ab2ef-175">Konfigurere Azure AD B2C-politikker med oplysninger om brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="ab2ef-175">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="ab2ef-176">Gå tilbage til siden **Azure AD B2C** i Azure-portalen, og vælg derefter **Brugerstrømme (politikker)** i menuen under **Politikker**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-176">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="ab2ef-177">Opdatere politikken "Tilmelding og logon" med oplysninger om brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="ab2ef-177">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="ab2ef-178">Følg disse trin for at opdatere politikken "Tilmelding og logon" med oplysninger om brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-178">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="ab2ef-179">Vælg **Sidelayout** i den **Tilmelding og logon**-politik, du har konfigureret tidligere, i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-179">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="ab2ef-180">Vælg layoutet **Side for samlet tilmelding eller logon**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-180">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="ab2ef-181">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-181">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="ab2ef-182">Angiv hele URL-adressen til logon i feltet **Brugerdefineret side-URI**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-182">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="ab2ef-183">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-183">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="ab2ef-184">Angiv for eksempel ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-184">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="ab2ef-185">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-185">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="ab2ef-186">Vælg layoutet **Lokal kontotilmelding**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-186">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="ab2ef-187">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-187">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="ab2ef-188">Angiv hele URL-adressen til tilmelding i feltet **URL-adresse til brugerdefineret side**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-188">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="ab2ef-189">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-189">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="ab2ef-190">Angiv for eksempel ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-190">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="ab2ef-191">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-191">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="ab2ef-192">Benyt følgende fremgangsmåde i sektionen **Brugerattributter**:</span><span class="sxs-lookup"><span data-stu-id="ab2ef-192">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="ab2ef-193">Vælg **Nej** i feltet **Kræver bekræftelse** for attributterne **E-mailadresse**, **Tildelt navn** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-193">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="ab2ef-194">Vælg **Nej** i feltet **Valgfrit** for attributterne **Tildelt navn** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-194">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Konfiguration af politikken for tilmelding til en lokal konto](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="ab2ef-196">Opdatere politikken "Profilredigering" med oplysninger om brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="ab2ef-196">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="ab2ef-197">Følg disse trin for at opdatere politikken "Profilredigering" med oplysninger om brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-197">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="ab2ef-198">Vælg **Sidelayout** i den **Profilredigering**-politik, du har konfigureret tidligere, i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-198">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="ab2ef-199">Vælg layoutet til **Profilredigeringsside**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-199">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="ab2ef-200">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-200">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="ab2ef-201">Angiv hele URL-adressen til profilredigering i feltet **URL-adresse til brugerdefineret side**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-201">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="ab2ef-202">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-202">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="ab2ef-203">Angiv for eksempel ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-203">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="ab2ef-204">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-204">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="ab2ef-205">Benyt følgende fremgangsmåde i sektionen **Brugerattributter**:</span><span class="sxs-lookup"><span data-stu-id="ab2ef-205">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="ab2ef-206">Vælg **Nej** i feltet **Kræver bekræftelse** for attributterne **E-mailadresse**, **Tildelt navn**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-206">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="ab2ef-207">Vælg **Nej** i feltet **Valgfrit** for attributterne **Tildelt navn** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-207">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="ab2ef-208">Opdatere politikken "Nulstilling af adgangskode" med oplysninger om brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="ab2ef-208">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="ab2ef-209">Følg disse trin for at opdatere politikken "Nulstilling af adgangskode" med oplysninger om brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-209">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="ab2ef-210">Vælg **Sidelayout** i den **Nulstilling af adgangskode**-politik, du har konfigureret tidligere, i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-210">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="ab2ef-211">Vælg layoutet **Side for ny adgangskode**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-211">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="ab2ef-212">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-212">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="ab2ef-213">Angiv hele URL-adressen til nulstilling af kodeord i feltet **URL-adresse til brugerdefineret side**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-213">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="ab2ef-214">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-214">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="ab2ef-215">Angiv for eksempel ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-215">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="ab2ef-216">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-216">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="ab2ef-217">Vælg layoutet for **Side til kontogodkendelse**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-217">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="ab2ef-218">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-218">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="ab2ef-219">Angiv hele URL-adressen til verificering af nulstilling af kodeord i feltet **URL-adresse til brugerdefineret side**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-219">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="ab2ef-220">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-220">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="ab2ef-221">Angiv for eksempel ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-221">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="ab2ef-222">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-222">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="ab2ef-223">Tilpasse standardtekststrenge for etiketter og beskrivelser</span><span class="sxs-lookup"><span data-stu-id="ab2ef-223">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="ab2ef-224">I modulbiblioteket er logonmoduler udfyldt på forhånd med standardtekststrenge til etiketter og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-224">In the module library, sign-in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="ab2ef-225">Du kan tilpasse disse strenge i SDK (Software Development Kit) ved at opdatere værdierne i filen global.json for logonmodulet.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-225">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="ab2ef-226">Standardteksten for linket til den glemte adgangskode er f.eks. **Har du glemt adgangskoden?**.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-226">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="ab2ef-227">I det følgende vises denne standardtekst på logonsiden.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-227">The following shows this default text on the sign-in page.</span></span>

![Standardtekst for linket til glemt adgangskode på logonsiden](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="ab2ef-229">Du kan dog redigere teksten til **Har du glemt adgangskoden?** i filen global.json til modulbibliotekets logonmodul, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-229">However, in the global.json file for the module library sign-in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Linkteksten opdateret i logonmodulets global.json-fil](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="ab2ef-231">Når du har opdateret global.json-filen og publiceret dine ændringer, vises den nye linktekst i logonmodulet i både Commerce og på den direkte logonside.</span><span class="sxs-lookup"><span data-stu-id="ab2ef-231">After you update the global.json file and publish your changes, the new link text appears in the sign-in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ab2ef-232">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ab2ef-232">Additional resources</span></span>

[<span data-ttu-id="ab2ef-233">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="ab2ef-233">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ab2ef-234">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="ab2ef-234">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="ab2ef-235">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="ab2ef-235">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="ab2ef-236">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="ab2ef-236">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ab2ef-237">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="ab2ef-237">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="ab2ef-238">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="ab2ef-238">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="ab2ef-239">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="ab2ef-239">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="ab2ef-240">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="ab2ef-240">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="ab2ef-241">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="ab2ef-241">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ab2ef-242">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="ab2ef-242">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
