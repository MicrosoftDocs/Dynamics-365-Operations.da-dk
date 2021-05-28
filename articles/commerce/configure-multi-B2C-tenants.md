---
title: Konfigurere flere B2C-lejere i et Commerce-miljø
description: I dette emne beskrives, hvornår og hvordan du konfigurerer flere Microsoft Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) pr. kanal til brugergodkendelse i et dedikeret Dynamics 365 Commerce-miljø.
author: BrianShook
ms.date: 03/17/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.region: Global
ms.search.industry: retail
ms.author: brshoo
ms.search.validFrom: 2020-02-12
ms.dyn365.ops.version: ''
ms.openlocfilehash: c813adb79ae1b78a052332e077393f125830633f
ms.sourcegitcommit: cabd991fda2bfcabb55db84c225b24a7bb061631
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6027716"
---
# <a name="configure-multiple-b2c-tenants-in-a-commerce-environment"></a><span data-ttu-id="1e4e3-103">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="1e4e3-103">Configure multiple B2C tenants in a Commerce environment</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="1e4e3-104">I dette emne beskrives, hvornår og hvordan du konfigurerer flere Microsoft Azure Active Directory (Azure AD) B2C-lejere (Business-to-Consumer) pr. kanal til brugergodkendelse i et dedikeret Dynamics 365 Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-104">This topic describes when and how to set up multiple Microsoft Azure Active Directory (Azure AD) business-to-consumer (B2C) tenants per channel for user authentication in a dedicated Dynamics 365 Commerce environment.</span></span>

<span data-ttu-id="1e4e3-105">Dynamics 365 Commerce bruger Azure AD B2C cloud-identitetstjeneste til at understøtte brugerlegitimationsoplysninger og godkendelsesstrømme.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-105">Dynamics 365 Commerce uses the Azure AD B2C cloud identity service to support user credentials and authentication flows.</span></span> <span data-ttu-id="1e4e3-106">Brugerne kan bruge godkendelsesstrømmene til at tilmelde sig, logge på og nulstille deres adgangskode.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-106">Users can use the authentication flows to sign up, sign in, and reset their password.</span></span> <span data-ttu-id="1e4e3-107">Azure AD B2C gemmer en brugers følsomme godkendelsesoplysninger, f.eks. brugernavn og adgangskode.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-107">Azure AD B2C stores a user's sensitive authentication information, such as the user name and password.</span></span> <span data-ttu-id="1e4e3-108">Brugerposten er entydig for hver B2C-lejer, og den bruger brugernavnets legitimationsoplysninger (mailadressen) eller sociale identitetsudbyderes legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-108">The user record is unique to each B2C tenant, and it uses either user name (email address) credentials or social identity provider credentials.</span></span>

<span data-ttu-id="1e4e3-109">I de fleste tilfælde bruges en enkelt Azure AD B2C-lejer i et Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-109">In most cases, a single Azure AD B2C tenant is used in a Commerce environment.</span></span> <span data-ttu-id="1e4e3-110">Commerce-kunder kan derefter oprette og udgive flere websteder i samme Commerce-miljø, og de samme kundelegitimationsoplysninger vil blive anvendt på tværs af disse steder.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-110">Commerce customers can then create and publish multiple sites in the same Commerce environment, and the same customer credentials will be used across these sites.</span></span> <span data-ttu-id="1e4e3-111">Hvis webstederne i miljøet imidlertid skal behandles som forskellige brands og vises for brugere som separate firmaer, kan en B2C-lejer konfigureres til den kanal, der bruges til adskillelse af lokation/brand.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-111">However, if the sites in the environment should be treated as different brands and appear to users as separate businesses, a B2C tenant can be configured for the channel that is used for the site/brand separation.</span></span>

## <a name="considerations-when-multiple-b2c-tenants-are-set-up-per-channel"></a><span data-ttu-id="1e4e3-112">Overvejelser ved konfiguration af flere B2C-lejere pr. kanal</span><span class="sxs-lookup"><span data-stu-id="1e4e3-112">Considerations when multiple B2C tenants are set up per channel</span></span>

<span data-ttu-id="1e4e3-113">Når hver kanal eller et websted behandles som en separat virksomhed, er den bedste mulighed ofte, hvad angår brugergodkendelsesprocesser i Commerce, at bruge separate juridiske enheder.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-113">Often, when each channel or site is being treated as a separate business, the best option with respect to user authentication flows in Commerce is to use separate legal entities.</span></span> <span data-ttu-id="1e4e3-114">Hvis du imidlertid vil have hver kanal/lokation i samme miljø og juridiske enhed, men gerne vil have adskilt brugergodkendelse for hver enkelt websted, er det vigtigt, at du overvejer følgende punkter, før du fortsætter:</span><span class="sxs-lookup"><span data-stu-id="1e4e3-114">However, if you want to keep each channel/site in the same environment and legal entity, but want to have separate user authentication for each site, it's important that you consider the following points before you proceed:</span></span>

- <span data-ttu-id="1e4e3-115">Brugerne vil have deres egne særskilte legitimationsoplysninger for hver kanal/hvert websted.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-115">Users will have their own distinct credentials for each channel/site.</span></span>

    <span data-ttu-id="1e4e3-116">Den samme person kan have to separate konti pr. kanal/lokation, da hver konto vil være en entydig post i en separat B2C-lejer.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-116">The same person can have two separate accounts per channel/site, because each account will be a unique entry into a separate B2C tenant.</span></span>

- <span data-ttu-id="1e4e3-117">I Microsoft Dynamics-miljøet returneres der separate kundeposter med søgninger med globale poster.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-117">In the Microsoft Dynamics environment, separate customer records will be returned for global record searches.</span></span>

    <span data-ttu-id="1e4e3-118">Hvis en bruger anvender den samme mailadresse på tværs af kanaler/websteder, returnerer globale kundesøgninger resultater for hver kanal/hvert enkelt websted.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-118">If a user uses the same email address across channels/sites, global customer searches will return results for each channel/site.</span></span> <span data-ttu-id="1e4e3-119">(Der vises en kanalindikator.)</span><span class="sxs-lookup"><span data-stu-id="1e4e3-119">(A channel indicator will be shown.)</span></span>

- <span data-ttu-id="1e4e3-120">Du kan bruge adressekartoteket som hjælp til at gruppere brugere, så de kan spores pr. kanal.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-120">The address book can be used to help group users, so that they can be tracked per channel.</span></span>
- <span data-ttu-id="1e4e3-121">Antallet af kundeposter pr. kanal kan stige, og denne forøgelse kan påvirke udførelsen af globale kundesøgninger.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-121">The number of customer records per channel might increase, and this increase might affect the performance of global customer searches.</span></span>
- <span data-ttu-id="1e4e3-122">B2C-lejere skal være omhyggeligt knyttet til en kanal for at undgå situationer, hvor kunder tilmelder sig en forkert lejer.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-122">B2C tenants must be carefully mapped to a channel, to help prevent situations where customers sign up for an incorrect tenant.</span></span> <span data-ttu-id="1e4e3-123">Ellers kan der opstå forvirring eller sporingsproblemer.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-123">Otherwise, confusion or tracking issues can occur.</span></span>

<span data-ttu-id="1e4e3-124">I følgende illustration vises flere B2C-lejere i et Commerce-miljø.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-124">The following illustration shows multiple B2C tenants in a Commerce environment.</span></span>

![Flere B2C-lejere i et Commerce-miljø](media/MultiB2C_In_Environment.png)

<span data-ttu-id="1e4e3-126">Hvis du beslutter, at din virksomhed kræver særskilte B2C-lejere pr. kanal i det samme Commerce-miljø, skal du fuldføre procedurerne i følgende afsnit for at anmode om denne funktion.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-126">If you decide that your business requires distinct B2C tenants per channel in the same Commerce environment, complete the procedures in the following sections to request this feature.</span></span>

## <a name="configure-b2c-tenants-in-your-environment"></a><span data-ttu-id="1e4e3-127">Konfigurere B2C-lejere i dit miljø</span><span class="sxs-lookup"><span data-stu-id="1e4e3-127">Configure B2C tenants in your environment</span></span>

<span data-ttu-id="1e4e3-128">Hvis du vil konfigurere B2C-lejere i dit miljø, skal du gennemføre de relevante procedurer i dette afsnit.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-128">To configure B2C tenants in your environment, complete the relevant procedures in this section.</span></span>

### <a name="add-an-azure-ad-b2c-tenant"></a><span data-ttu-id="1e4e3-129">Tilføje en Azure AD B2C-lejer</span><span class="sxs-lookup"><span data-stu-id="1e4e3-129">Add an Azure AD B2C tenant</span></span>

<span data-ttu-id="1e4e3-130">Følg disse trin for at føje en Azure AD B2C-lejer til dit miljø.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-130">To add an Azure AD B2C tenant to your environment, follow these steps.</span></span>

1. <span data-ttu-id="1e4e3-131">Log på Commerce-webstedsgeneratoren for dit miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-lejere, skal du være systemadministrator for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-131">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="1e4e3-132">Vælg **Lejerindstillinger** i venstre navigationsrude for at udvide den.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-132">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="1e4e3-133">Vælg **B2C-indstillinger**, og vælg derefter **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-133">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="1e4e3-134">Vælg **Tilføj B2C-program**, og angiv følgende oplysninger:</span><span class="sxs-lookup"><span data-stu-id="1e4e3-134">Select **Add B2C Application**, and then enter the following information:</span></span>

    - <span data-ttu-id="1e4e3-135">**Programnavn**: Angiv det navn, der skal bruges i programmet i forbindelse med administration af det i Commerce.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-135">**Application Name**: Enter the name that should be used for the application in the context of managing it in Commerce.</span></span> <span data-ttu-id="1e4e3-136">Vi anbefaler, at du bruger det programnavn, du valgte, da du konfigurerede Azure AD B2C-programmet i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-136">We recommend that you use the application name that you chose when you set up the Azure AD B2C application in the Azure portal.</span></span> <span data-ttu-id="1e4e3-137">På denne måde kan du hjælpe med at reducere forvirring, når du håndterer B2C-lejere i Commerce.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-137">In this way, you can help reduce confusion when you manage B2C tenants in Commerce.</span></span>
    - <span data-ttu-id="1e4e3-138">**Navn på lejer**: Angiv navnet på B2C-lejeren, som det vises i Azure-portalen.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-138">**Tenant Name**: Enter the B2C tenant name as it appears in the Azure portal.</span></span>
    - <span data-ttu-id="1e4e3-139">**Glem adgangskodepolitik-id**: Angiv politik-id'et (navnet på politikken på Azure-portalen).</span><span class="sxs-lookup"><span data-stu-id="1e4e3-139">**Forget Password Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="1e4e3-140">**Politik-id for tilmelding og logon**: Angiv politik-id'et (navnet på politikken på Azure-portalen).</span><span class="sxs-lookup"><span data-stu-id="1e4e3-140">**Signup Signin Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>
    - <span data-ttu-id="1e4e3-141">**Klient-GUID**: Angiv det Azure AD B2C-lejer-id, som det vises i Azure-portalen (ikke program-id'et for B2C-lejeren).</span><span class="sxs-lookup"><span data-stu-id="1e4e3-141">**Client GUID**: Enter the Azure AD B2C tenant ID as it appears in the Azure portal (not the application ID for the B2C tenant).</span></span>
    - <span data-ttu-id="1e4e3-142">**Rediger profilpolitik-id**: Angiv politik-id'et (navnet på politikken på Azure-portalen).</span><span class="sxs-lookup"><span data-stu-id="1e4e3-142">**Edit Profile Policy ID**: Enter the policy ID (the name of the policy in the Azure portal).</span></span>

1. <span data-ttu-id="1e4e3-143">Vælg **OK**, når du er færdig med at angive disse oplysninger, for at gemme ændringerne.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-143">When you've finished entering this information, select **OK** to save your changes.</span></span> <span data-ttu-id="1e4e3-144">Den nye Azure AD B2C-lejer vises nu på listen under **Administrer B2C-programmer**.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-144">Your new Azure AD B2C tenant should now appear in the list under **Manage B2C Applications**.</span></span>

> [!NOTE]
> <span data-ttu-id="1e4e3-145">Du bør lade felter som **Område**, **Ikke-interaktivt politik-id**, **Ikke-interaktivt klient-id**, **Logon på brugerdefineret domæne** og **Politik-id for tilmelding** være tomme, medmindre Dynamics 365 Commerce-teamet beder dig om at angive dem.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-145">You should leave fields such as **Scope**, **Non Interactive Policy ID**, **Non Interactive Client ID**, **Login Custom Domain**, and **Sign Up Policy ID** blank unless the Dynamics 365 Commerce team instructs you to set them.</span></span>


### <a name="manage-or-delete-an-azure-ad-b2c-tenant"></a><span data-ttu-id="1e4e3-146">Administrere eller slette en Azure AD B2C-lejer</span><span class="sxs-lookup"><span data-stu-id="1e4e3-146">Manage or delete an Azure AD B2C tenant</span></span>

1. <span data-ttu-id="1e4e3-147">Log på Commerce-webstedsgeneratoren for dit miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-lejere, skal du være systemadministrator for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-147">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="1e4e3-148">Vælg **Lejerindstillinger** i venstre navigationsrude for at udvide den.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-148">In the left navigation pane, select **Tenant Settings** to expand it.</span></span>
1. <span data-ttu-id="1e4e3-149">Vælg **B2C-indstillinger**, og vælg derefter **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-149">Select **B2C Settings**, and then select **Manage**.</span></span>
1. <span data-ttu-id="1e4e3-150">Hvis du vil redigere en B2C lejer, skal du vælge blyantsymbolet ud for den.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-150">To edit a B2C tenant, select the pencil symbol next to it.</span></span> <span data-ttu-id="1e4e3-151">Hvis du vil slette en B2C-lejer, skal du vælge papirkurvssymbolet ud for den.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-151">To delete a B2C tenant, select the trash can symbol next to it.</span></span>
1. <span data-ttu-id="1e4e3-152">Vælg **Gem**, og vælg derefter **Udgiv** for at aktivere ændringerne.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-152">Select **Save**, and then select **Publish** to activate your changes.</span></span>

> [!WARNING]
> <span data-ttu-id="1e4e3-153">Når en B2C-lejer er konfigureret til et live/publiceret websted, har brugerne muligvis tilmeldt sig ved hjælp af konti, der findes i lejeren.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-153">When a B2C tenant is configured for a live/published site, users might have signed up by using accounts that are present on the tenant.</span></span> <span data-ttu-id="1e4e3-154">Hvis du sletter en konfigureret lejer i menuen **Lejerindstillinger \> B2C-lejer**, fjerner du den pågældende B2C-lejers tilknytning fra steder, der er knyttet til kanaler i lejeren.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-154">If you delete a configured tenant on the **Tenant Settings \> B2C Tenant** menu, you remove the association of that B2C tenant from sites that are associated with any channels of the tenant.</span></span> <span data-ttu-id="1e4e3-155">I dette tilfælde vil brugerne muligvis ikke længere kunne logge på deres konti.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-155">In this case, your users might no longer be able to sign in to their accounts.</span></span> <span data-ttu-id="1e4e3-156">Derfor skal du være meget forsigtig, når du sletter en konfigureret lejer.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-156">Therefore, use extreme caution when you delete a configured tenant.</span></span>
>
> <span data-ttu-id="1e4e3-157">Når en konfigureret lejer slettes, vil B2C-lejeren og -posterne fortsat være bevaret, men konfigurationen af Commerce-systemlejeren vil blive ændret eller fjernet.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-157">When a configured tenant is deleted, the B2C tenant and records will continue to be maintained, but the Commerce system configuration of that tenant will be changed or removed.</span></span> <span data-ttu-id="1e4e3-158">Brugere, der forsøger at tilmelde sig eller logge på webstedet, opretter en ny kontopost i standard- eller den netop tilknyttede B2C-lejer, der er konfigureret til kanalen på webstedet.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-158">Users who try to sign up or sign in to the site will create a new account record in the default or newly associated B2C tenant that is configured for the channel of the site.</span></span>

## <a name="configure-your-channel-with-a-b2c-tenant"></a><span data-ttu-id="1e4e3-159">Konfigurere din kanal med en B2C-lejer</span><span class="sxs-lookup"><span data-stu-id="1e4e3-159">Configure your channel with a B2C tenant</span></span>

1. <span data-ttu-id="1e4e3-160">Log på Commerce-webstedsgeneratoren for dit miljø som systemadministrator. Hvis du vil konfigurere Azure AD B2C-lejere, skal du være systemadministrator for Commerce-miljøet.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-160">Sign in to Commerce site builder for your environment as a system admin. To configure Azure AD B2C tenants, you must be a system admin for the Commerce environment.</span></span>
1. <span data-ttu-id="1e4e3-161">Vælg **Indstillinger for websted** i venstre navigationsrude for at udvide den.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-161">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="1e4e3-162">Vælg **Kanaler**, og vælg derefter den kanal, der skal konfigureres.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-162">Select **Channels**, and then select the channel to configure.</span></span>
1. <span data-ttu-id="1e4e3-163">Vælg den konfigurerede Azure AD B2C-lejer, der skal bruges til denne kanal, i feltet **Vælg B2C-program** i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-163">In the properties pane on the right, in the **Select B2C Application** field, select the configured Azure AD B2C tenant to use for this channel.</span></span>
1. <span data-ttu-id="1e4e3-164">Vælg **Gem og udgiv** på kommandolinjen for at bekræfte den nye eller opdaterede konfiguration.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-164">On the command bar, select **Save and Publish** to commit the new or updated configuration.</span></span>

> [!WARNING]
> <span data-ttu-id="1e4e3-165">Hvis du ændrer det B2C-program, der er tildelt kanalen, fjerner du de aktuelle referencer, der er oprettet for brugere, som allerede er tilmeldt i miljøet.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-165">If you change the B2C application that is assigned to the channel, you remove the current references that have been established for any users who have already signed up in the environment.</span></span> <span data-ttu-id="1e4e3-166">I dette tilfælde vil alle legitimationsoplysninger, der er knyttet til det aktuelt tildelte B2C-program, ikke være tilgængelige for brugerne.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-166">In this case, any credentials that are associated with the currently assigned B2C application won't be available to users.</span></span> <span data-ttu-id="1e4e3-167">Du skal derfor kun ændre en Azure AD B2C-kanalkonfiguration, hvis du konfigurerer kanalen første gang, og ingen brugere har haft mulighed for at tilmelde sig.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-167">Therefore, change a channel Azure AD B2C configuration only if you're setting up the channel for the first time, and no users have been able to sign up.</span></span> <span data-ttu-id="1e4e3-168">Ellers skal brugerne måske tilmelde sig igen for at oprette en post i den nye Azure AD B2C-lejer.</span><span class="sxs-lookup"><span data-stu-id="1e4e3-168">Otherwise, users might have to sign up again to establish a record in the new Azure AD B2C tenant.</span></span>
## <a name="additional-resources"></a><span data-ttu-id="1e4e3-169">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="1e4e3-169">Additional resources</span></span>

[<span data-ttu-id="1e4e3-170">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="1e4e3-170">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="1e4e3-171">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="1e4e3-171">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="1e4e3-172">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="1e4e3-172">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="1e4e3-173">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="1e4e3-173">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="1e4e3-174">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="1e4e3-174">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="1e4e3-175">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="1e4e3-175">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="1e4e3-176">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="1e4e3-176">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="1e4e3-177">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="1e4e3-177">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="1e4e3-178">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="1e4e3-178">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="1e4e3-179">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="1e4e3-179">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
