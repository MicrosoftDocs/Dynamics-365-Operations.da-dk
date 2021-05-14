---
title: Konfigurere Azure Active Directory-godkendelse for POS-login
description: Dette emne forklarer, hvordan du kan konfigurere Azure Active Directory som godkendelsesmetode i POS i Microsoft Dynamics 365 Commerce.
author: boycezhu
manager: annbe
ms.date: 04/23/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.search.region: global
ms.author: boycez
ms.search.validFrom: ''
ms.dyn365.ops.version: 10.0.11
ms.openlocfilehash: 34a7946a56a58655bc9ae23e060fc50ab01f2c6e
ms.sourcegitcommit: 593438a145672c55ff6a910eabce2939300b40ad
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5937452"
---
# <a name="configure-azure-active-directory-authentication-for-pos-sign-in"></a><span data-ttu-id="74361-103">Konfigurere Azure Active Directory-godkendelse for POS-login</span><span class="sxs-lookup"><span data-stu-id="74361-103">Configure Azure Active Directory authentication for POS sign-in</span></span>

[!include [banner](includes/banner.md)]
[!include [banner](includes/preview-banner.md)]

<span data-ttu-id="74361-104">Dette emne forklarer, hvordan du kan konfigurere Azure Active Directory (Azure AD) som godkendelsesmetode i POS i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="74361-104">This topic explains how to configure Azure Active Directory (Azure AD) as the authentication method in Microsoft Dynamics 365 Commerce point of sale (POS).</span></span>

<span data-ttu-id="74361-105">Detailhandlere, der bruger Dynamics 365 Commerce sammen med andre Microsoft-skytjenester, f.eks. Microsoft Azure, Microsoft 365 og Microsoft Teams, vil typisk bruge Azure AD til centraliseret administration af brugerlegitimationsoplysningerne for at opnå en sikker og problemfri logonoplevelse på tværs af programmer.</span><span class="sxs-lookup"><span data-stu-id="74361-105">Retailers who use Dynamics 365 Commerce along with other Microsoft cloud services such as Microsoft Azure, Microsoft 365, and Microsoft Teams typically want to use Azure AD for centralized management of user credentials for a secure and seamless sign-in experience across applications.</span></span> <span data-ttu-id="74361-106">Hvis du vil bruge Azure AD-godkendelse til Commerce POS, skal du først konfigurere Azure AD som godkendelsesmetoden i Commerce-hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="74361-106">To use Azure AD authentication for Commerce POS, you must first configure Azure AD as the authentication method in Commerce headquarters.</span></span>

## <a name="configure-pos-authentication-method"></a><span data-ttu-id="74361-107">Konfigurere POS-godkendelsesmetode</span><span class="sxs-lookup"><span data-stu-id="74361-107">Configure POS authentication method</span></span>

<span data-ttu-id="74361-108">Benyt denne fremgangsmåde for at konfigurere POS-godkendelsesmetoden i Commerce-hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="74361-108">To configure the POS authentication method in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="74361-109">Gå til **Retail og Commerce \> Konfiguration af kanal \> POS-opsætning \> POS-profiler \> Funktionalitetsprofiler**, og vælg den funktionalitetsprofil, du vil ændre.</span><span class="sxs-lookup"><span data-stu-id="74361-109">Go to **Retail and Commerce \> Channel setup \> POS setup \> POS profiles \> Functionality profiles**, and select a functionality profile to change.</span></span>
1. <span data-ttu-id="74361-110">Vælg en ønsket godkendelsesmetode på rullelisten **Logongodkendelsesmetode** i sektionen **POS-marbejderlogon** i oversigtspanelet **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="74361-110">In the **POS staff logon** section of the **Functions** FastTab, select a desired authentication method option from the **Logon authentication method** drop-down list.</span></span>

    <span data-ttu-id="74361-111">Der er tre indstillinger for **Logon-godkendelsesmetode**:</span><span class="sxs-lookup"><span data-stu-id="74361-111">The **Logon authentication method** has three options:</span></span>
    
    - <span data-ttu-id="74361-112">**Personale-id og adgangskode** – Denne standardindstilling kræver, at POS-brugere angiver et personale-id og en adgangskode for at logge på POS og få adgang til funktionaliteten til ledertilsidesættelse.</span><span class="sxs-lookup"><span data-stu-id="74361-112">**Personnel ID and Password** - This default option requires POS users to enter a personnel ID and password to sign in to the POS and to access manager override functionality.</span></span>
    - <span data-ttu-id="74361-113">**Azure AD uden enkeltlogon** – Denne indstilling kræver, at POS-brugere bruger Azure AD-legitimationsoplysninger til at logge på POS og få adgang til funktionaliteten til ledertilsidesættelse.</span><span class="sxs-lookup"><span data-stu-id="74361-113">**Azure AD without single sign-on** - This option requires POS users to use Azure AD credentials to sign in to the POS and access manager override functionality.</span></span> <span data-ttu-id="74361-114">Når POS-klienten opdateres eller åbnes igen, skal POS-brugeren angive Azure AD-legitimationsoplysninger for at logge på igen.</span><span class="sxs-lookup"><span data-stu-id="74361-114">When the POS client is refreshed or reopened, the POS user must provide Azure AD credentials to sign in again.</span></span>
    - <span data-ttu-id="74361-115">**Azure AD med enkeltlogon** – Når denne indstilling er valgt, kan POS-brugere logge på Cloud POS (CPOS) ved hjælp af aktive Azure AD-legitimationsoplysninger, der bruges af andre webapplikationer i samme webbrowser, eller logge på Modern POS (MPOS) ved hjælp af Azure AD-legitimationsoplysninger, der er logget på Windows.</span><span class="sxs-lookup"><span data-stu-id="74361-115">**Azure AD with single sign-on** - When this option is selected, POS users are able to sign in to Cloud POS (CPOS) using active Azure AD credentials that are being used by other web applications in the same web browser, or sign in to Modern POS (MPOS) using Azure AD credentials signed in to Windows.</span></span> <span data-ttu-id="74361-116">Begge metoder gør det muligt at logge på uden at skulle angive Azure AD-legitimationsoplysninger på skærmen for POS-logon.</span><span class="sxs-lookup"><span data-stu-id="74361-116">Both methods allow sign-in without needing to enter Azure AD credentials on the POS sign-in screen.</span></span> <span data-ttu-id="74361-117">Adgangen til funktionaliteten for POS-ledertilsidesættelse kræver dog stadig logon med Azure AD-legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="74361-117">However, accessing the POS manager override functionality will still require sign-in using Azure AD credentials.</span></span>

1. <span data-ttu-id="74361-118">Gå til **Retail og Commerce > Retail og Commerce IT > Distributionsplan**, og kør jobbet **1070 (Kanalkonfiguration)** for at synkronisere funktionalitetens seneste profilindstillinger til POS-klienter.</span><span class="sxs-lookup"><span data-stu-id="74361-118">Go to **Retail and Commerce > Retail and Commerce IT > Distribution schedule** and run the **1070 (Channel configuration)** job to synchronize the latest functionality profile settings to POS clients.</span></span>

> [!NOTE]
> - <span data-ttu-id="74361-119">Indstillingen for godkendelsesmetoden **Azure AD uden enkeltlogon** erstatter indstillingen **Azure Active Directory** i Commerce version 10.0.18 og tidligere.</span><span class="sxs-lookup"><span data-stu-id="74361-119">The **Azure AD without single sign-on** authentication method option replaces the **Azure Active Directory** option in Commerce version 10.0.18 and earlier.</span></span>
> - <span data-ttu-id="74361-120">Azure AD-godkendelse kræver en aktiv internetforbindelse og vil ikke fungere, når POS er offline.</span><span class="sxs-lookup"><span data-stu-id="74361-120">Azure AD authentication requires an active internet connection, and won't function when the POS is offline.</span></span>

## <a name="associate-azure-ad-accounts-with-pos-users"></a><span data-ttu-id="74361-121">Knytte Azure AD-konti til POS-brugere</span><span class="sxs-lookup"><span data-stu-id="74361-121">Associate Azure AD accounts with POS users</span></span>

<span data-ttu-id="74361-122">Hvis du vil bruge Azure AD som POS-godkendelsesmetode, skal du knytte Azure AD-konti til POS-brugere i Commerce-hovedkvarteret.</span><span class="sxs-lookup"><span data-stu-id="74361-122">To use Azure AD as the POS authentication method, you must associate Azure AD accounts with POS users in Commerce headquarters.</span></span> 

<span data-ttu-id="74361-123">Hvis du vil knytte Azure AD-konti til POS-brugere i Commerce-hovedkvarteret, skal du benytte denne fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="74361-123">To associate Azure AD accounts with POS users in Commerce headquarters, follow these steps.</span></span>
    
1. <span data-ttu-id="74361-124">Gå til **Retail og Commerce > Medarbejdere > Arbejdere**, og åbn en arbejderpost.</span><span class="sxs-lookup"><span data-stu-id="74361-124">Go to **Retail and Commerce > Employees > Workers** and open a worker record.</span></span>
1. <span data-ttu-id="74361-125">Vælg fanen **Commerce** i handlingsruden, og vælg derefter **Tilknyt eksisterende identitet** under **Ekstern identitet**.</span><span class="sxs-lookup"><span data-stu-id="74361-125">On the Action Pane, select the **Commerce** tab, then under **External identity** select **Associate existing identity**.</span></span> 
1. <span data-ttu-id="74361-126">Vælg **Søg ved hjælp af mail** i dialogboksen **Brug eksisterende ekstern identitet**, indtast en Azure AD-mailadresse, og vælg derefter **Søg**.</span><span class="sxs-lookup"><span data-stu-id="74361-126">In the **Use existing external identity** dialog box, select **Search using email**, enter an Azure AD email address, and then select **Search**.</span></span>
1. <span data-ttu-id="74361-127">Vælg den Azure AD-konto, der returneres, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="74361-127">Select the Azure AD account that is returned, then select **OK**.</span></span>

<span data-ttu-id="74361-128">Efter konfigurationsmetoden ovenfor, skal du udfylde felterne **Alias**, **UPN** og **Eksternt under-id** under fanen **Commerce** på siden med detaljer om arbejderen.</span><span class="sxs-lookup"><span data-stu-id="74361-128">After the configuration steps above, the **Alias**, **UPN**, and **External sub identifier** fields on the **Commerce** tab of the worker's details page will be filled in.</span></span>

<span data-ttu-id="74361-129">Du skal køre jobbet **1060 (personale)** i **Retail og Commerce > Retail og Commerce IT > Distributionsplan** for at synkronisere den seneste POS-bruger og Azure AD-kontodata til kanalen.</span><span class="sxs-lookup"><span data-stu-id="74361-129">You must run the **1060 (Staff)** job in **Retail and Commerce > Retail and Commerce IT > Distribution schedule** to synchronize the latest POS user and Azure AD account data to the channel.</span></span>

> [!NOTE]
> <span data-ttu-id="74361-130">Efter du har opdateret arbejderoplysninger som f.eks. adgangskode, POS-tilladelse, tilknyttet Azure AD-konto eller medarbejderadressekartotek i Commerce-hovedkvarteret, anbefales det som bedste praksis at køre jobbet **1060 (personale)** for at synkronisere de seneste arbejderoplysninger med kanalen.</span><span class="sxs-lookup"><span data-stu-id="74361-130">As a best practice, after worker information such as password, POS permission, associated Azure AD account, or employee address book is updated in Commerce headquarters, it is highly recommended to run the **1060 (Staff)** job to synchronize the latest worker information to the channel.</span></span> <span data-ttu-id="74361-131">POS-klienten kan derefter hente de korrekte data til brugergodkendelse og godkendelseskontroller.</span><span class="sxs-lookup"><span data-stu-id="74361-131">The POS client can then fetch the correct data for user authentication and authorization checks.</span></span>

## <a name="pos-lock-register-and-sign-out-with-azure-ad-authentication"></a><span data-ttu-id="74361-132">Låse kasseapparat for POS og logge af med Azure AD-godkendelse</span><span class="sxs-lookup"><span data-stu-id="74361-132">POS lock register and sign-out with Azure AD authentication</span></span>

<span data-ttu-id="74361-133">Følgende sker, når POS er konfigureret til at bruge Azure AD-godkendelsesmetoden:</span><span class="sxs-lookup"><span data-stu-id="74361-133">The following occurs when POS is configured to use the Azure AD authentication method:</span></span>

- <span data-ttu-id="74361-134">Funktionen **Lås kasseapparat** er ikke tilgængelig i POS-applikationen.</span><span class="sxs-lookup"><span data-stu-id="74361-134">The **Lock register** function will not be available in the POS application.</span></span> 
- <span data-ttu-id="74361-135">Funktionen **Lås automatisk** fungerer på samme måde som funktionen **Log af automatisk**.</span><span class="sxs-lookup"><span data-stu-id="74361-135">The **Automatically lock** function will behave the same as the **Automatically logoff** function.</span></span>
- <span data-ttu-id="74361-136">Hvis POS-brugeren vælger **Log af**, vil brugeren blive bedt om at logge på med Azure AD-legitimationsoplysninger, næste gang POS starter, uanset om enkeltlogon er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="74361-136">If the POS user selects **Log off**, the user will be asked to sign in with Azure AD credentials the next time the POS launches, regardless of whether single sign-in is enabled.</span></span>

## <a name="manager-override-functionality-with-azure-ad-authentication"></a><span data-ttu-id="74361-137">Funktionaliteten til ledertilsidesættelse med Azure AD-godkendelse</span><span class="sxs-lookup"><span data-stu-id="74361-137">Manager override functionality with Azure AD authentication</span></span>

<span data-ttu-id="74361-138">Når POS er konfigureret til at bruge Azure AD-godkendelse, åbner funktionaliteten til ledertilsidesættelse en dialogboks, hvor brugeren bliver bedt om at angive lederens Azure AD-legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="74361-138">When the POS is configured to use Azure AD authentication, the manager override functionality will open a dialog box that prompts for the manager user's Azure AD credentials.</span></span> <span data-ttu-id="74361-139">Når lederens logon er godkendt, fjernes lederens Azure AD-legitimationsoplysninger, og den forrige brugers Azure AD-legitimationsoplysninger anvendes til efterfølgende POS-handlinger.</span><span class="sxs-lookup"><span data-stu-id="74361-139">After manager sign-in is approved, the manager's Azure AD credentials will be dropped and the previous user's Azure AD credentials will be used for subsequent POS operations.</span></span>

> [!NOTE]
> - <span data-ttu-id="74361-140">I Commerce-versionerne 10.0.18 og tidligere understøtter lederens tilsidesættelsesfunktion ikke Azure AD.</span><span class="sxs-lookup"><span data-stu-id="74361-140">In Commerce versions 10.0.18 and earlier, the manager override function does not support Azure AD.</span></span> <span data-ttu-id="74361-141">Der kræves en medarbejders id og adgangskode, selvom POS er konfigureret som Azure AD-godkendelsesmetode.</span><span class="sxs-lookup"><span data-stu-id="74361-141">A personnel ID and password are required even if the POS is configured to use the Azure AD authentication method.</span></span>
> - <span data-ttu-id="74361-142">Når du bruger CPOS med Safari-webbrowseren på en Apple iOS-enhed, skal du først deaktivere **Bloker popup-vinduer** i Safari-indstillingerne for funktionaliteten til ledertilsidesættelse, før du kan arbejde med Azure AD-godkendelse.</span><span class="sxs-lookup"><span data-stu-id="74361-142">When using CPOS with the Safari web browser on an Apple iOS device, you must first turn off **Block Pop-ups** in Safari settings for the manager override functionality to work with Azure AD authentication.</span></span> 

## <a name="security-best-practices-for-azure-ad-based-pos-authentication-on-shared-devices"></a><span data-ttu-id="74361-143">Bedste sikkerhedspraksis for Azure AD-baseret POS-godkendelse på delte enheder</span><span class="sxs-lookup"><span data-stu-id="74361-143">Security best practices for Azure AD-based POS authentication on shared devices</span></span>

<span data-ttu-id="74361-144">Mange detailhandlende konfigurerer deres detailbutiksmiljø på en måde, så flere brugere har brug for at få adgang til POS-applikationen fra en delt fysisk enhed.</span><span class="sxs-lookup"><span data-stu-id="74361-144">Many retailers set up their retail store environment in a way that multiple users need to access the POS application from a shared physical device.</span></span> <span data-ttu-id="74361-145">I denne sammenhæng giver enkeltlogon en praktisk og problemfri godkendelsesoplevelse, kan den også oprette et sikkerhedshul, hvor den aktuelle POS-bruger muligvis ikke kan se, at en anden brugers legitimationsoplysninger anvendes til at udføre transaktioner eller handlinger i POS.</span><span class="sxs-lookup"><span data-stu-id="74361-145">In that context, while single sign-in provides a convenient and seamless authentication experience, it may also create a security loophole where the current POS user may not realize that another user's credentials are being used to perform transactions or operations in the POS.</span></span> <span data-ttu-id="74361-146">Før du konfigurerer POS til at bruge Azure AD-godkendelsesmetoden, anbefales det at gennemse sikkerhedspolitikken og logonindstillingerne for den delte enhed for at bestemme, hvilken indstilling der er bedst egnet.</span><span class="sxs-lookup"><span data-stu-id="74361-146">Before you configure the POS to use the Azure AD authentication method, it is highly recommended to review your security policy and the shared device's sign-in settings to decide which option is the best fit.</span></span>

- <span data-ttu-id="74361-147">Hvis der bruges en delt konto i dit detailmiljø (f.eks. en lokal konto) til logon på en fysisk enhed, anbefales det, at du bruger indstillingen **Azure AD uden enkeltlogon**.</span><span class="sxs-lookup"><span data-stu-id="74361-147">If your retail environment uses a shared account (for example, a local account) for physical device sign-in, it's recommended to use the **Azure AD without single sign-on** option.</span></span> <span data-ttu-id="74361-148">Dette sikrer, at den enkelte POS-bruger udtrykkeligt angiver Azure AD-legitimationsoplysninger for at logge på POS.</span><span class="sxs-lookup"><span data-stu-id="74361-148">This ensures that each POS user explicitly provides Azure AD credentials to sign in to the POS.</span></span>
- <span data-ttu-id="74361-149">Hvis detailmiljøet kræver, at medarbejdere bruger deres egne Azure AD-konti til at logge på POS og dets fysiske hostingenhed, anbefales det, at du bruger indstillingen **Azure AD med med enkeltlogon**.</span><span class="sxs-lookup"><span data-stu-id="74361-149">If your retail environment requires employees to use their own Azure AD accounts to sign in to the POS and its hosting physical device, it's recommended to use the **Azure AD with single sign-on** option.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74361-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="74361-150">Additional resources</span></span>

[<span data-ttu-id="74361-151"> Konfigurere en arbejder</span><span class="sxs-lookup"><span data-stu-id="74361-151">Configure a worker</span></span>](tasks/worker.md)

[<span data-ttu-id="74361-152">Oprette en detailfunktionalitetsprofil</span><span class="sxs-lookup"><span data-stu-id="74361-152">Create a retail functionality profile</span></span>](retail-functionality-profile.md)


[<span data-ttu-id="74361-153">Konfigurere udvidet logonfunktionalitet for MPOS og Cloud POS</span><span class="sxs-lookup"><span data-stu-id="74361-153">Set up extended logon functionality for MPOS and Cloud POS</span></span>](extended-logon.md)

[<span data-ttu-id="74361-154">Bedste sikkerhedspraksis for Cloud POS i delte miljøer</span><span class="sxs-lookup"><span data-stu-id="74361-154">Security best practices for Cloud POS in shared environments</span></span>](dev-itpro/secure-retail-cloud-pos.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
