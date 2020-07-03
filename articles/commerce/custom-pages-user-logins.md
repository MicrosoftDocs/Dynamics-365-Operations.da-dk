---
title: Konfigurere brugerdefinerede sider til brugerlogon
description: Dette emne beskriver, hvordan du bygger tilpassede sider i Microsoft Dynamics 365 Commerce, der håndterer tilpasset logon for brugere af Azure Active Directory (Azure AD) Business-to-Consumer-lejere (B2C).
author: brianshook
manager: annbe
ms.date: 06/16/2020
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
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 71c0f0b6969985b04262b522dd2165eb1475878d
ms.sourcegitcommit: 9a2e9f7dfec47c42178bb67a3e099e610515baf3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/16/2020
ms.locfileid: "3456966"
---
# <a name="set-up-custom-pages-for-user-sign-ins"></a><span data-ttu-id="c2dd3-103">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="c2dd3-103">Set up custom pages for user sign-ins</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="c2dd3-104">Dette emne beskriver, hvordan du bygger tilpassede sider i Microsoft Dynamics 365 Commerce, der håndterer tilpasset logon for brugere af Azure Active Directory (Azure AD) Business-to-Consumer-lejere (B2C).</span><span class="sxs-lookup"><span data-stu-id="c2dd3-104">This topic describes how to build custom pages in Microsoft Dynamics 365 Commerce that handle customized sign-ins for users of Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants.</span></span>

## <a name="overview"></a><span data-ttu-id="c2dd3-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="c2dd3-105">Overview</span></span>

<span data-ttu-id="c2dd3-106">Hvis du vil bruge brugerdefinerede sider, der er oprettet i Dynamics 365 Commerce, til at håndtere brugerlogon, skal du konfigurere de Azure AD-politikker, der skal refereres til i Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-106">To use custom pages that are authored in Dynamics 365 Commerce to handle user sign-in flows, you must set up the Azure AD policies that will be referenced in the Commerce environment.</span></span> <span data-ttu-id="c2dd3-107">Du kan konfigurere Azure AD B2C-politikkerne "Tilmelding og logon", "Profilredigering" og "Nulstilling af adgangskode" ved hjælp af Azure AD B2C-programmet.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-107">You can configure the "Sign up and sign in," "Profile editing," and "Password reset" Azure AD B2C policies by using the Azure AD B2C application.</span></span> <span data-ttu-id="c2dd3-108">Der kan derefter refereres til Azure AD B2C-lejeren og politiknavne under den klargørings proces, der udføres for Commerce-miljøet ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c2dd3-108">The Azure AD B2C tenant and policy names can then be referenced during the provisioning process that is done for the Commerce environment by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="c2dd3-109">De brugerdefinerede Commerce-sider kan opbygges ved hjælp af modulet til logon, tilmelding, kontoprofilredigering eller genstart af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-109">The custom Commerce pages can be built by using the sign in, sign up, account profile edit, or password reset module.</span></span> <span data-ttu-id="c2dd3-110">De URL-adresser til sider, der udgives for disse brugerdefinerede sider, skal derefter refereres i Azure AD B2C-politikkonfigurationerne i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-110">The page URLs that are published for these custom pages should then be referenced in Azure AD B2C policy configurations in the Azure portal.</span></span>

## <a name="set-up-b2c-policies"></a><span data-ttu-id="c2dd3-111">Konfigurere B2C-politikker</span><span class="sxs-lookup"><span data-stu-id="c2dd3-111">Set up B2C policies</span></span>

<span data-ttu-id="c2dd3-112">Når du har konfigureret din Azure AD B2C-lejer og har knyttet den til Commerce-miljøet, skal du gå siden **Azure AD B2C** i Azure-portalen og derefter vælge **Brugerstrømme (politikker)** i menuen under **Politikker**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-112">After you set up your Azure AD B2C tenant and associate it with your Commerce environment, go to the **Azure AD B2C** page in the Azure portal, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

![Kommandoen Brugerstrømme (politikker) i menuen](./media/B2C_CustomPage_PoliciesMenu.png)

<span data-ttu-id="c2dd3-114">Du kan nu konfigurere brugerlogonstrømmene "Tilmelding og logon", "Profilredigering" og "Nulstilling af adgangskode".</span><span class="sxs-lookup"><span data-stu-id="c2dd3-114">You can now configure the "Sign up and sign in," "Profile editing," and "Password reset" user sign-in flows.</span></span>

### <a name="configure-the-sign-up-and-sign-in-policy"></a><span data-ttu-id="c2dd3-115">Konfigurere politikken "Tilmelding og logon"</span><span class="sxs-lookup"><span data-stu-id="c2dd3-115">Configure the "Sign up and sign in" policy</span></span>

<span data-ttu-id="c2dd3-116">For at konfigurere politikken "Tilmelding og logon" skal du udføre følgende trin.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-116">To configure the "Sign up and sign in" policy, follow these steps.</span></span>

1. <span data-ttu-id="c2dd3-117">Vælg **Ny brugerstrøm**, og vælg derefter politikken **Tilmelding og logon** under fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-117">Select **New user flow**, and then, on the **Recommended** tab, select the **Sign up and sign in** policy.</span></span>
1. <span data-ttu-id="c2dd3-118">Angiv et navn til politikken (f.eks. **B2C\_1\_TilmeldingLogon**).</span><span class="sxs-lookup"><span data-stu-id="c2dd3-118">Enter a name for the policy (for example, **B2C\_1\_SignInSignUp**).</span></span>
1. <span data-ttu-id="c2dd3-119">Vælg de id-udbydere, der skal bruges til politikken, i sektionen **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-119">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="c2dd3-120">Du skal som minimum vælge **E-mailtilmelding**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-120">At a minimum, **Email signup** must be selected.</span></span>
1. <span data-ttu-id="c2dd3-121">I kolonnen **Indsaml attribut** skal du markere afkrydsningsfelterne for **E-mailadresse**, **Tildelt navn** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-121">In the **Collect attribute** column, select the check boxes for **Email Address**, **Given Name**, and **Surname**.</span></span>
1. <span data-ttu-id="c2dd3-122">I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Identitetsudbyder**, **Efternavn** og **Brugerens objekt-id**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-122">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>

    ![Valgte attributter og krav](./media/B2C_SignInSignUp_Attributes.png)

1. <span data-ttu-id="c2dd3-124">Vælg **OK** for at oprette politikken.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-124">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="c2dd3-125">Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-125">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="c2dd3-126">Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-126">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

    ![Siden Egenskaber for den nye politik](./media/B2C_SignInSignUp_EnableJavascript.png)

> [!NOTE]
> <span data-ttu-id="c2dd3-128">Der bliver refereret til hele politiknavnet i Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-128">The policy name will be fully referenced in the Commerce environment.</span></span> <span data-ttu-id="c2dd3-129">(**B2C\_1\_**-præfikset bliver medtaget i referencen). Politikker kan ikke omdøbes, når de først er oprettet.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-129">(The **B2C\_1\_** prefix will be included in the reference.) Policies can't be renamed after they are created.</span></span> <span data-ttu-id="c2dd3-130">Hvis du erstatter en eksisterende politik for Commerce-miljøet, kan du slette den oprindelige politik og oprette en ny politik med samme navn.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-130">If you're replacing an existing policy for your Commerce environment, you can delete the original policy and build a new policy that has the same name.</span></span> <span data-ttu-id="c2dd3-131">Hvis miljøet allerede er blevet klargjort, kan du også sende det nye politiknavn via en serviceanmodning.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-131">Alternatively, if the environment has already been provisioned, you can submit the new policy name through a service request.</span></span>

<span data-ttu-id="c2dd3-132">Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-132">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="c2dd3-133">Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-133">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-profile-editing-policy"></a><span data-ttu-id="c2dd3-134">Konfigurere politikken "Profilredigering"</span><span class="sxs-lookup"><span data-stu-id="c2dd3-134">Configure the "Profile editing" policy</span></span>

<span data-ttu-id="c2dd3-135">Du kan konfigurere politikken "Profilredigering" ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-135">To configure the "Profile editing" policy, follow these steps.</span></span>

1. <span data-ttu-id="c2dd3-136">Vælg **Ny brugerstrøm**, og vælg derefter politikken **Profilredigering** under fanen **Anbefalet**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-136">Select **New user flow**, and then, on the **Recommended** tab, select the **Profile editing** policy.</span></span>
1. <span data-ttu-id="c2dd3-137">Angiv et navn til politikken (f.eks. **B2C\_1\_RedigerProfil**).</span><span class="sxs-lookup"><span data-stu-id="c2dd3-137">Enter a name for the policy (for example, **B2C\_1\_EditProfile**).</span></span>
1. <span data-ttu-id="c2dd3-138">Vælg de id-udbydere, der skal bruges til politikken, i sektionen **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-138">In the **Identity Providers** section, select the identity providers to use for the policy.</span></span> <span data-ttu-id="c2dd3-139">Der skal som minimum være valgt **Log på lokal konto**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-139">At a minimum, **Local Account SignIn** must be selected.</span></span>
1. <span data-ttu-id="c2dd3-140">I kolonnen **Indsaml attribut** skal du markere afkrydsningsfelterne for **E-mailadresse** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-140">In the **Collect attribute** column, select the check boxes for **Email Addresses** and **Surname**.</span></span>
1. <span data-ttu-id="c2dd3-141">I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Identitetsudbyder**, **Efternavn** og **Brugerens objekt-id**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-141">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Identity Provider**, **Surname**, and **User's Object ID**.</span></span>
1. <span data-ttu-id="c2dd3-142">Vælg **OK** for at oprette politikken.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-142">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="c2dd3-143">Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-143">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="c2dd3-144">Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-144">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="c2dd3-145">Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-145">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="c2dd3-146">Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-146">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

### <a name="configure-the-password-reset-policy"></a><span data-ttu-id="c2dd3-147">Konfigurere politikken "Nulstilling af adgangskode"</span><span class="sxs-lookup"><span data-stu-id="c2dd3-147">Configure the "Password reset" policy</span></span>

<span data-ttu-id="c2dd3-148">Du kan konfigurere politikken "Nulstilling af adgangskode" ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-148">To configure the "Password reset" policy, follow these steps.</span></span>

1. <span data-ttu-id="c2dd3-149">Vælg **Ny brugerstrøm**, og vælg derefter politikken **Nulstilling af adgangskode v1.1** under fanen **Eksempel**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-149">Select **New user flow**, and then, on the **Preview** tab, select the **Password reset v1.1** policy.</span></span>

    ![Politikken for Nulstilling af adgangskode v.1.1 valgt under fanen Eksempel](./media/B2C_ForgetPassword_Menu.png)

1. <span data-ttu-id="c2dd3-151">Angiv et navn til politikken (f.eks. **B2C\_1\_GlemtAdgangskode**).</span><span class="sxs-lookup"><span data-stu-id="c2dd3-151">Enter a name for the policy (for example, **B2C\_1\_ForgetPassword**).</span></span>
1. <span data-ttu-id="c2dd3-152">Vælg **Nulstil adgangskode ved hjælp af e-mailadresse** i sektionen **Identitetsudbydere**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-152">In the **Identity Providers** section, select **Reset password using email address**.</span></span>
1. <span data-ttu-id="c2dd3-153">I kolonnen **Returkrav** skal du markere afkrydsningsfelterne **E-mailadresser**, **Tildelt navn**, **Efternavn** og **Brugerens objekt-id**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-153">In the **Return claim** column, select the check boxes for **Email Addresses**, **Given Name**, **Surname**, and **User's Object ID**.</span></span>

    ![Valgte krav](./media/B2C_ForgetPassword_Attributes.png)

1. <span data-ttu-id="c2dd3-155">Vælg **OK** for at oprette politikken.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-155">Select **OK** to create the policy.</span></span>
1. <span data-ttu-id="c2dd3-156">Dobbeltklik på navnet på den nye politik, og vælg derefter **Egenskaber** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-156">Double-click the new policy name, and then, in the navigation pane, select **Properties**.</span></span>
1. <span data-ttu-id="c2dd3-157">Vælg **Til** i indstillingen **Aktivér JavaScript-valg af sidelayout (eksempel)**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-157">Set the **Enable JavaScript enforcing page layout (preview)** option to **On**.</span></span>

<span data-ttu-id="c2dd3-158">Du skal vende tilbage til denne politik for at afslutte installationen, når du har opbygget de brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-158">You will return to this policy to finish the setup after you've built the custom pages.</span></span> <span data-ttu-id="c2dd3-159">Du skal nu lukke politikken for at vende tilbage til siden **Brugerstrømme (politikker)** i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-159">For now, close the policy to return to the **User flows (policies)** page in the Azure portal.</span></span>

## <a name="build-the-custom-pages"></a><span data-ttu-id="c2dd3-160">Oprette brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="c2dd3-160">Build the custom pages</span></span>

<span data-ttu-id="c2dd3-161">Udfør følgende trin for at opbygge de brugerdefinerede sider til håndtering af brugerlogon.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-161">To build the custom pages to handle user sign-ins, follow these steps.</span></span>

1. <span data-ttu-id="c2dd3-162">Gå til dit websted i Commerce-oprettelsesværktøjerne.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-162">In the Commerce authoring tools, go to your site.</span></span>
1. <span data-ttu-id="c2dd3-163">Opbyg følgende fem skabeloner og fem sider:</span><span class="sxs-lookup"><span data-stu-id="c2dd3-163">Build the following five templates and five pages:</span></span>

    - <span data-ttu-id="c2dd3-164">En **Logon**-skabelon og -side, der bruger logonmodulet.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-164">A **Sign In** template and page that use the sign in module.</span></span>
    - <span data-ttu-id="c2dd3-165">En **Logon**-skabelon og -side, der bruger logonmodulet.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-165">A **Sign Up** template and page that use the sign up module.</span></span>
    - <span data-ttu-id="c2dd3-166">En skabelon og side til **Nulstilling af adgangskod**, der bruger modulet til nulstilling af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-166">A **Password Reset** template and page that use the password reset module.</span></span>
    - <span data-ttu-id="c2dd3-167">En skabelon og side til **Bekræftelse af nulstilling af adgangskod**, der bruger modulet til bekræftelse af nulstilling af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-167">A **Password Reset verification** template and page that use the password reset verification module.</span></span>
    - <span data-ttu-id="c2dd3-168">En skabelon og side til **Profilredigering**, der bruger modulet til redigering af kontoprofilen</span><span class="sxs-lookup"><span data-stu-id="c2dd3-168">A **Profile Edit** template and page that use the account profile edit module</span></span>

<span data-ttu-id="c2dd3-169">Når du opbygger siderne, skal du følge disse retningslinjer:</span><span class="sxs-lookup"><span data-stu-id="c2dd3-169">When you build the pages, follow these guidelines:</span></span>

- <span data-ttu-id="c2dd3-170">For hver side eller hvert modul skal du bruge det layout og den typografi, der passer bedst til dine forretningsbehov.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-170">For each page or module, use the layout and style that best suit your business requirements.</span></span>
- <span data-ttu-id="c2dd3-171">Udgiv alle sider og URL-adresser, der skal bruges i Azure AD B2C-opsætningen.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-171">Publish all pages and URLs that must be used in the Azure AD B2C setup.</span></span>
- <span data-ttu-id="c2dd3-172">Når siderne og URL-adresserne er publiceret, skal du indsamle de URL-adresser, der skal bruges til konfigurationer af Azure AD B2C-politikken.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-172">After the pages and URLs are published, collect the URLs that must be used for the Azure AD B2C policy configurations.</span></span> <span data-ttu-id="c2dd3-173">Der føjes et **?preloadscripts=true**-suffiks til hver URL-adresse, når den bruges.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-173">A **?preloadscripts=true** suffix will be added to every URL when it's used.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="c2dd3-174">Du må ikke genbruge universelle sidehoveder og sidefødder, der har relative hyperlinks.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-174">Don't reuse universal headers and footers that have relative links.</span></span> <span data-ttu-id="c2dd3-175">Da disse sider findes på Azure AD B2C-domænet, når de bruges, bør der kun bruges absolutte URL-adresser til alle links.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-175">Because these pages will be hosted in the Azure AD B2C domain when they are used, only absolute URLs should be used for all links.</span></span>

## <a name="configure-azure-ad-b2c-policies-with-custom-page-information"></a><span data-ttu-id="c2dd3-176">Konfigurere Azure AD B2C-politikker med oplysninger om brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="c2dd3-176">Configure Azure AD B2C policies with custom page information</span></span> 

<span data-ttu-id="c2dd3-177">Gå tilbage til siden **Azure AD B2C** i Azure-portalen, og vælg derefter **Brugerstrømme (politikker)** i menuen under **Politikker**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-177">In the Azure portal, return to the **Azure AD B2C** page, and then, on the menu, under **Policies**, select **User flows (policies)**.</span></span>

### <a name="update-the-sign-up-and-sign-in-policy-with-custom-page-information"></a><span data-ttu-id="c2dd3-178">Opdatere politikken "Tilmelding og logon" med oplysninger om brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="c2dd3-178">Update the "Sign up and sign in" policy with custom page information</span></span>

<span data-ttu-id="c2dd3-179">Følg disse trin for at opdatere politikken "Tilmelding og logon" med oplysninger om brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-179">To update the "Sign up and sign in" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="c2dd3-180">Vælg **Sidelayout** i den **Tilmelding og logon**-politik, du har konfigureret tidligere, i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-180">In the **Sign in and sign up** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="c2dd3-181">Vælg layoutet **Side for samlet tilmelding eller logon**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-181">Select the **Unified sign up or sign in page** layout.</span></span>
1. <span data-ttu-id="c2dd3-182">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-182">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="c2dd3-183">Angiv hele URL-adressen til logon i feltet **Brugerdefineret side-URI**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-183">In the **Custom page URI** field, enter the full sign-in URL.</span></span> <span data-ttu-id="c2dd3-184">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-184">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="c2dd3-185">Angiv for eksempel ``www.<my domain>.com/sign-in?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-185">For example, enter ``www.<my domain>.com/sign-in?preloadscripts=true``.</span></span>
1. <span data-ttu-id="c2dd3-186">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-186">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="c2dd3-187">Vælg layoutet **Lokal kontotilmelding**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-187">Select the **Local account sign up page** layout.</span></span>
1. <span data-ttu-id="c2dd3-188">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-188">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="c2dd3-189">Angiv hele URL-adressen til tilmelding i feltet **URL-adresse til brugerdefineret side**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-189">In the **Custom page URI** field, enter the full sign-up URL.</span></span> <span data-ttu-id="c2dd3-190">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-190">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="c2dd3-191">Angiv for eksempel ``www.<my domain>.com/sign-up?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-191">For example, enter ``www.<my domain>.com/sign-up?preloadscripts=true``.</span></span>
1. <span data-ttu-id="c2dd3-192">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-192">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="c2dd3-193">Benyt følgende fremgangsmåde i sektionen **Brugerattributter**:</span><span class="sxs-lookup"><span data-stu-id="c2dd3-193">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="c2dd3-194">Vælg **Nej** i feltet **Kræver bekræftelse** for attributterne **E-mailadresse**, **Tildelt navn** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-194">For the **Email Address**, **Given Name**, and **Surname** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="c2dd3-195">Vælg **Nej** i feltet **Valgfrit** for attributterne **Tildelt navn** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-195">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

    ![Konfiguration af politikken for tilmelding til en lokal konto](./media/B2C_SignUp_PageURLConfig.png)

### <a name="update-the-profile-editing-policy-with-custom-page-information"></a><span data-ttu-id="c2dd3-197">Opdatere politikken "Profilredigering" med oplysninger om brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="c2dd3-197">Update the "Profile editing" policy with custom page information</span></span>

<span data-ttu-id="c2dd3-198">Følg disse trin for at opdatere politikken "Profilredigering" med oplysninger om brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-198">To update the "Profile editing" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="c2dd3-199">Vælg **Sidelayout** i den **Profilredigering**-politik, du har konfigureret tidligere, i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-199">In the **Profile Editing** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="c2dd3-200">Vælg layoutet til **Profilredigeringsside**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-200">Select the **Profile edit page** layout.</span></span>
1. <span data-ttu-id="c2dd3-201">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-201">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="c2dd3-202">Angiv hele URL-adressen til profilredigering i feltet **URL-adresse til brugerdefineret side**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-202">In the **Custom page URI** field, enter the full profile edit URL.</span></span> <span data-ttu-id="c2dd3-203">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-203">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="c2dd3-204">Angiv for eksempel ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-204">For example, enter ``www.<my domain>.com/profile-edit?preloadscripts=true``.</span></span>
1. <span data-ttu-id="c2dd3-205">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-205">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="c2dd3-206">Benyt følgende fremgangsmåde i sektionen **Brugerattributter**:</span><span class="sxs-lookup"><span data-stu-id="c2dd3-206">In the **User attributes** section, follow these steps:</span></span>

    1. <span data-ttu-id="c2dd3-207">Vælg **Nej** i feltet **Kræver bekræftelse** for attributterne **E-mailadresse**, **Tildelt navn**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-207">For the **Email Address**, **Given Name** attributes, select **No** in the **Requires Verification** field.</span></span>
    1. <span data-ttu-id="c2dd3-208">Vælg **Nej** i feltet **Valgfrit** for attributterne **Tildelt navn** og **Efternavn**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-208">For the **Given Name** and **Surname** attributes, select **No** in the **Optional** field.</span></span>

### <a name="update-the-password-reset-policy-with-custom-page-information"></a><span data-ttu-id="c2dd3-209">Opdatere politikken "Nulstilling af adgangskode" med oplysninger om brugerdefinerede sider</span><span class="sxs-lookup"><span data-stu-id="c2dd3-209">Update the "Password reset" policy with custom page information</span></span>

<span data-ttu-id="c2dd3-210">Følg disse trin for at opdatere politikken "Nulstilling af adgangskode" med oplysninger om brugerdefinerede sider.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-210">To update the "Password reset" policy with custom page information, follow these steps.</span></span>

1. <span data-ttu-id="c2dd3-211">Vælg **Sidelayout** i den **Nulstilling af adgangskode**-politik, du har konfigureret tidligere, i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-211">In the **Password Reset** policy that you configured earlier, in the navigation pane, select **Page layouts**.</span></span>
1. <span data-ttu-id="c2dd3-212">Vælg layoutet **Side for ny adgangskode**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-212">Select the **New password page** layout.</span></span>
1. <span data-ttu-id="c2dd3-213">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-213">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="c2dd3-214">Angiv hele URL-adressen til nulstilling af kodeord i feltet **URL-adresse til brugerdefineret side**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-214">In the **Custom page URI** field, enter the full password reset URL.</span></span> <span data-ttu-id="c2dd3-215">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-215">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="c2dd3-216">Angiv for eksempel ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-216">For example, enter ``www.<my domain>.com/passwordreset?preloadscripts=true``.</span></span>
1. <span data-ttu-id="c2dd3-217">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-217">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>
1. <span data-ttu-id="c2dd3-218">Vælg layoutet for **Side til kontogodkendelse**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-218">Select the **Account verification page** layout.</span></span>
1. <span data-ttu-id="c2dd3-219">Vælg **Ja** i indstillingen **Anvend brugerdefineret sideindhold**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-219">Set the **Use custom page content** option to **Yes**.</span></span>
1. <span data-ttu-id="c2dd3-220">Angiv hele URL-adressen til verificering af nulstilling af kodeord i feltet **URL-adresse til brugerdefineret side**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-220">In the **Custom page URI** field, enter the full password reset verification URL.</span></span> <span data-ttu-id="c2dd3-221">Medtag suffikset **?preloadscripts=true**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-221">Include the **?preloadscripts=true** suffix.</span></span> <span data-ttu-id="c2dd3-222">Angiv for eksempel ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-222">For example, enter ``www.<my domain>.com/passwordreset-verification?preloadscripts=true``.</span></span>
1. <span data-ttu-id="c2dd3-223">I feltet **Sidelayoutversion (Eksempel)** skal du vælge **1.2.0**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-223">In the **Page Layout Version (Preview)** field, select **1.2.0**.</span></span>



## <a name="customize-default-text-strings-for-labels-and-descriptions"></a><span data-ttu-id="c2dd3-224">Tilpasse standardtekststrenge for etiketter og beskrivelser</span><span class="sxs-lookup"><span data-stu-id="c2dd3-224">Customize default text strings for labels and descriptions</span></span>

<span data-ttu-id="c2dd3-225">I startpakken er logonmoduler udfyldt på forhånd med standardtekststrenge for etiketter og beskrivelser.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-225">In the starter kit, sign in modules are prefilled with default text strings for the labels and descriptions.</span></span> <span data-ttu-id="c2dd3-226">Du kan tilpasse disse strenge i SDK (Software Development Kit) ved at opdatere værdierne i filen global.json for logonmodulet.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-226">You can customize these strings in the software development kit (SDK) by updating the values in the global.json file for the sign in module.</span></span>

<span data-ttu-id="c2dd3-227">Standardteksten for linket til den glemte adgangskode er f.eks. **Har du glemt adgangskoden?**.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-227">For example, the default text for the forgotten password link is **Forgotten password?**.</span></span> <span data-ttu-id="c2dd3-228">I det følgende vises denne standardtekst på logonsiden.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-228">The following shows this default text on the sign-in page.</span></span>

![Standardtekst for linket til glemt adgangskode på logonsiden](./media/B2C_SignUp_ModuleFace.png)

<span data-ttu-id="c2dd3-230">Du kan dog redigere teksten i **Har du glemt adgangskoden?** i filen global.json til startpakkens logonmodul, som vist i følgende illustration.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-230">However, in the global.json file for the starter kit sign in module, you can edit the text to **Forgot Password?**, as shown in the following illustration.</span></span>

![Linkteksten opdateret i logonmodulets global.json-fil](./media/B2C_CustomizingStringsForModule.png)

<span data-ttu-id="c2dd3-232">Når du har opdateret global.json-filen og publiceret dine ændringer, vises den nye linktekst i logonmodulet i både Commerce-siden og på siden til direkte logon.</span><span class="sxs-lookup"><span data-stu-id="c2dd3-232">After you update the global.json file and publish your changes, the new link text appears in the sign in module in both Commerce and on the live sign-in page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="c2dd3-233">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="c2dd3-233">Additional resources</span></span>

[<span data-ttu-id="c2dd3-234">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="c2dd3-234">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="c2dd3-235">Implementere et nyt websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="c2dd3-235">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="c2dd3-236">Konfigurere en onlinebutikskanal</span><span class="sxs-lookup"><span data-stu-id="c2dd3-236">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="c2dd3-237">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="c2dd3-237">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="c2dd3-238">Tilknytte et onlinewebsted til en kanal</span><span class="sxs-lookup"><span data-stu-id="c2dd3-238">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="c2dd3-239">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="c2dd3-239">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="c2dd3-240">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="c2dd3-240">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="c2dd3-241">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="c2dd3-241">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="c2dd3-242">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="c2dd3-242">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="c2dd3-243">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="c2dd3-243">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="c2dd3-244">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="c2dd3-244">Enable location-based store detection</span></span>](enable-store-detection.md)
