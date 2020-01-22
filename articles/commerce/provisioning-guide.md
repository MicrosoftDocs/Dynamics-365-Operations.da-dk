---
title: Klargøring af et Commerce-prøveversionsmiljø
description: I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-prøveversionsmiljø.
author: psimolin
manager: annbe
ms.date: 01/06/2020
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
ms.openlocfilehash: b77d2cbbc100aeae5dcd53ddbe69ff2e4435da13
ms.sourcegitcommit: 4d77d06a07ec9e7a3fcbd508afdffaa406fd3dd8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/06/2020
ms.locfileid: "2934742"
---
# <a name="provision-a-commerce-preview-environment"></a><span data-ttu-id="2ebc8-103">Klargøring af et Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="2ebc8-103">Provision a Commerce preview environment</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="2ebc8-104">I dette emne beskrives det, hvordan du klargør et Microsoft Dynamics 365 Commerce-prøveversionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-104">This topic explains how to provision a Microsoft Dynamics 365 Commerce preview environment.</span></span>

<span data-ttu-id="2ebc8-105">Før du går i gang, anbefales det, at du som minimum skimmer hele dette emne igennem for at få en ide om, hvad processen indebærer, og hvad dette emne indeholder.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-105">Before you begin, we recommend that you at least skim through this whole topic to get an idea of what the process entails and what this topic contains.</span></span>

> [!NOTE]
> <span data-ttu-id="2ebc8-106">Hvis du endnu ikke har fået adgang til Dynamics 365 Commerce-prøveversionen, kan du anmode om adgang fra [Commerce-webstedet](https://aka.ms/Dynamics365CommerceWebsite).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-106">If you haven't yet been granted access to the Dynamics 365 Commerce preview, you can request preview access from the [Commerce website](https://aka.ms/Dynamics365CommerceWebsite).</span></span>

## <a name="overview"></a><span data-ttu-id="2ebc8-107">Oversigt</span><span class="sxs-lookup"><span data-stu-id="2ebc8-107">Overview</span></span>

<span data-ttu-id="2ebc8-108">Hvis du vil kunne klargør dit Commerce-prøveversionsmiljø, skal du oprette et projekt, der har et bestemt produktnavn og er en bestemt type.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-108">To successfully provision your Commerce preview environment, you must create a project that has a specific product name and type.</span></span> <span data-ttu-id="2ebc8-109">Miljøet og Retail Cloud Scale Unit (RCSU) har nogle specifikke parametre, du skal bruge, når du senere klargør dit e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-109">The environment and Retail Cloud Scale Unit (RCSU) also have some specific parameters that you must use when you provision e-Commerce later.</span></span> <span data-ttu-id="2ebc8-110">Instruktionerne i dette emne beskriver alle de påkrævede trin, du skal fuldføre, og de parametre, du skal bruge.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-110">The instructions in this topic describe all the required steps that you must complete and the parameters that you must use.</span></span>

<span data-ttu-id="2ebc8-111">Nå du har klargjort dit Commerce-prøveversionsmiljø, skal du fuldføre nogle få efter-klargørings-trin, for at gøre dit prøveversionsmiljø klar.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-111">After you successfully provision your Commerce preview environment, you must complete a few post-provisioning steps to prepare it.</span></span> <span data-ttu-id="2ebc8-112">Nogle trin er valgfrie, afhængigt af de aspekter af systemet, du vil evaluere.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-112">Some steps are optional, depending on the aspects of the system that you want to evaluate.</span></span> <span data-ttu-id="2ebc8-113">Du kan altid udføre de valgfrie trin senere.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-113">You can always complete the optional steps later.</span></span>

<span data-ttu-id="2ebc8-114">For yderligere oplysninger om, hvordan du konfigurerer dit Commerce-prøveversionsmiljø, efter du har klargjort det, se [Konfigurering af et Commerce-prøveversionsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-114">For information about how to configure your Commerce preview environment after you provision it, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span> <span data-ttu-id="2ebc8-115">For yderligere oplysninger om, hvordan du konfigurerer valgfrie funktioner til dit Commerce-prøveversionsmiljø, se [Konfiguration af valgfrie funktioner til et Commerce-prøveversionsmiljø](cpe-optional-features.md).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-115">For information about how to configure optional features for your Commerce preview environment, see [Configure optional features for a Commerce preview environment](cpe-optional-features.md).</span></span>

<span data-ttu-id="2ebc8-116">Hvis du har spørgsmål til klargøringstrinnene, eller du oplever problemer, bedes du fortælle det til Microsoft i [Microsoft Dynamics 365 Commerce-prøveversionens-Yammer-gruppen](https://aka.ms/Dynamics365CommercePreviewYammer).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-116">If you have any questions about the provisioning steps, or if you encounter any issues, let Microsoft know in the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer).</span></span>

## <a name="prerequisites"></a><span data-ttu-id="2ebc8-117">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="2ebc8-117">Prerequisites</span></span>

<span data-ttu-id="2ebc8-118">Følgende forudsætninger skal være på plads, før du kan klargør dit Commerce-prøveversionsmiljø:</span><span class="sxs-lookup"><span data-stu-id="2ebc8-118">The following prerequisites must be in place before you can provision your Commerce preview environment:</span></span>

- <span data-ttu-id="2ebc8-119">Du har adgang til Microsoft Dynamics Lifecycle Services-portalen (LCS).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-119">You have access to the Microsoft Dynamics Lifecycle Services (LCS) portal.</span></span>
- <span data-ttu-id="2ebc8-120">Du er blevet godkendt til Dynamics 365 Commerce-prøveversionsprogrammet.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-120">You've been accepted into the Dynamics 365 Commerce Preview program.</span></span>
- <span data-ttu-id="2ebc8-121">Du har de nødvendige rettigheder til at oprette et projekt til **Mulige førsalg** eller **Overflyt, opret løsninger, og lær at bruge**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-121">You have the required permissions to create a project for **Prospective presales** or **Migrate, create solutions, and learn**.</span></span>
- <span data-ttu-id="2ebc8-122">Du er medlem af rollen **Miljøadministrator** eller **Projektejer** i det projekt, hvor du skal klargøre miljøet.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-122">You're a member of the **Environment manager** or **Project owner** role in the project where you will provision the environment.</span></span>
- <span data-ttu-id="2ebc8-123">Du har administratoradgang til dit Microsoft Azure-abonnement eller du er i kontakt med en abonnementsadministrator, der kan fuldføre de to trin, der kræver administratorrettigheder, på dine vegne.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-123">You have admin access to your Microsoft Azure subscription, or you're in contact with a subscription admin who can complete the two steps that require admin permissions on your behalf.</span></span>
- <span data-ttu-id="2ebc8-124">Du har dit Azure Active Directory-lejer-ID (Azure AD) ved hånden.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-124">You have your Azure Active Directory (Azure AD) tenant ID available.</span></span>
- <span data-ttu-id="2ebc8-125">Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en systemadministratorgruppe til e-Commerce, og du har gruppens ID ved hånden.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-125">You've created an Azure AD security group that can be used as an e-Commerce system admin group, and you have its ID available.</span></span>
- <span data-ttu-id="2ebc8-126">Du har oprettet en Azure AD-sikkerhedsgruppe, der kan bruges som en gruppe for redaktører af vurderinger og anmeldelser, og du har gruppens ID ved hånden.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-126">You've created an Azure AD security group that can be used as a Ratings and Reviews moderator group, and you have its ID available.</span></span> <span data-ttu-id="2ebc8-127">(Denne sikkerhedsgruppe kan være den samme som e-Commerce-systemadministratorgruppen.)</span><span class="sxs-lookup"><span data-stu-id="2ebc8-127">(This security group can be the same as the e-Commerce system admin group.)</span></span>

### <a name="find-your-azure-ad-tenant-id"></a><span data-ttu-id="2ebc8-128">Find dit Azure AD-lejer-ID</span><span class="sxs-lookup"><span data-stu-id="2ebc8-128">Find your Azure AD tenant ID</span></span>

<span data-ttu-id="2ebc8-129">Dit Azure AD-lejer-ID er en global entydig identifikator (GUID), der ligner dette eksempel: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-129">Your Azure AD tenant ID is a globally unique identifier (GUID) that resembles this example: **72f988bf-86f1-41af-91ab-2d7cd011db47**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-the-azure-portal"></a><span data-ttu-id="2ebc8-130">Find dit Azure AD-lejer-ID ved hjælp af Azure-portalen</span><span class="sxs-lookup"><span data-stu-id="2ebc8-130">Find your Azure AD tenant ID by using the Azure portal</span></span>

1. <span data-ttu-id="2ebc8-131">Log på [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-131">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
1. <span data-ttu-id="2ebc8-132">Sørg for, at det korrekte bibliotek er valgt.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-132">Make sure that the correct directory is selected.</span></span>
1. <span data-ttu-id="2ebc8-133">Vælg **Azure Active Directory** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-133">On the menu on the left, select **Azure Active Directory**.</span></span>
1. <span data-ttu-id="2ebc8-134">Under **Administrer** skal du vælge **Egenskaber**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-134">Under **Manage**, select **Properties**.</span></span> <span data-ttu-id="2ebc8-135">Dit Azure AD-lejer-ID vises under **Mappe-ID**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-135">Your Azure AD tenant ID appears under **Directory ID**.</span></span>

#### <a name="find-your-azure-ad-tenant-id-by-using-openid-connect-metadata"></a><span data-ttu-id="2ebc8-136">Find dit Azure AD-lejer-ID ved hjælp af OpenID Connect-metadata</span><span class="sxs-lookup"><span data-stu-id="2ebc8-136">Find your Azure AD tenant ID by using OpenID Connect metadata</span></span>

<span data-ttu-id="2ebc8-137">Opret en OpenID-URL-adresse ved at erstatte **\{DIT\_DOMÆNE\}** med dit domæne, som eksemeplvis `microsoft.com`.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-137">Create an OpenID URL by replacing **\{YOUR\_DOMAIN\}** with your domain, such as `microsoft.com`.</span></span> <span data-ttu-id="2ebc8-138">For eksempel `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` bliver til `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-138">For example, `https://login.microsoftonline.com/{YOUR_DOMAIN}/.well-known/openid-configuration` will become `https://login.microsoftonline.com/microsoft.com/.well-known/openid-configuration`.</span></span>

1. <span data-ttu-id="2ebc8-139">Gå til den OpenID-URL-adresse, der indeholder dit domæne.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-139">Go to the OpenID URL that contains your domain.</span></span>

    <span data-ttu-id="2ebc8-140">Du kan finde dit Azure AD-lejer-ID i flere egenskabsværdier.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-140">You can find you Azure AD tenant ID in multiple property values.</span></span>

1. <span data-ttu-id="2ebc8-141">Find **godkendelse\_slutpunkt**, og udpak det GUID, der vises umiddelbart efter `login.microsoftonline.com/`.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-141">Find **authorization\_endpoint**, and extract the GUID that appears immediately after `login.microsoftonline.com/`.</span></span>

### <a name="find-your-azure-ad-security-group-id"></a><span data-ttu-id="2ebc8-142">Find dit Azure AD-sikkerhedsgruppe-ID</span><span class="sxs-lookup"><span data-stu-id="2ebc8-142">Find your Azure AD security group ID</span></span>

<span data-ttu-id="2ebc8-143">ID'et for din Azure AD-sikkerhedsgruppe er et GUID, der ligner dette eksempel: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-143">The ID of your Azure AD security group is a GUID that resembles this example: **436ea7f5-ee6c-40c1-9f08-825c5811066a**.</span></span>

<span data-ttu-id="2ebc8-144">I denne procedure antages det, at du er medlem af den gruppe, du forsøger at finde ID'et for.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-144">This procedure assumes that you're a member of the group that you're trying to find the ID for.</span></span>

1. <span data-ttu-id="2ebc8-145">Åbn [Graf-stifinder](https://developer.microsoft.com/graph/graph-explorer#).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-145">Open the [Graph Explorer](https://developer.microsoft.com/graph/graph-explorer#).</span></span>
1. <span data-ttu-id="2ebc8-146">Vælg **Log på med Microsoft**, og log på ved hjælp af dine legitimationsoplysninger.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-146">Select **Sign In with Microsoft**, and sign in by using your credentials.</span></span>
1. <span data-ttu-id="2ebc8-147">Vælg **vis flere eksempler** til venstre.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-147">On the left, select **show more samples**.</span></span>
1. <span data-ttu-id="2ebc8-148">Aktivér **Grupper** i højre rude.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-148">In the right pane, enable **Groups**.</span></span>
1. <span data-ttu-id="2ebc8-149">Luk den højre rude.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-149">Close the right pane.</span></span>
1. <span data-ttu-id="2ebc8-150">Vælg **alle grupper, som jeg tilhører**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-150">Select **all groups I belong to**.</span></span>
1. <span data-ttu-id="2ebc8-151">Find din gruppe i feltet **Forhåndsvisning af svar**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-151">In the **Response Preview** field, find your group.</span></span> <span data-ttu-id="2ebc8-152">Sikkerhedsgruppe-ID'et vises under **ID**-egenskaben.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-152">The security group ID appears under the **id** property.</span></span>

## <a name="provision-your-commerce-preview-environment"></a><span data-ttu-id="2ebc8-153">Klargøring af dit Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="2ebc8-153">Provision your Commerce preview environment</span></span>

<span data-ttu-id="2ebc8-154">Disse procedurer forklarer, hvordan du klargør et Commerce-prøveversionsmiljø.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-154">These procedures explain how to provision a Commerce preview environment.</span></span> <span data-ttu-id="2ebc8-155">Når du har fuldført dem, vil Commerce-prøveversionsmiljøet være klar til konfiguration.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-155">After you successfully complete them, the Commerce preview environment will be ready for configuration.</span></span> <span data-ttu-id="2ebc8-156">Alle de aktiviteter, der er beskrevet her, finder sted på LCS-portalen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-156">All the activities that are described here occur in the LCS portal.</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ebc8-157">Forhåndsadgang er knyttet til den LCS-konto og -organisation, som du angav i prøveversionsansøgning.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-157">Preview access is tied to the LCS account and organization that you specified in your preview application.</span></span> <span data-ttu-id="2ebc8-158">Du skal bruge den samme konto til at klargøre Commerce-prøveversionmiljøet.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-158">You must use the same account to provision the Commerce preview environment.</span></span> <span data-ttu-id="2ebc8-159">Hvis du skal bruge en anden LCS-konto eller -lejer til Commerce-prøveversionmiljøet, skal du oplyse Microsoft herom.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-159">If you must use a different LCS account or tenant for the Commerce preview environment, you must provide those details to Microsoft.</span></span> <span data-ttu-id="2ebc8-160">Du finder kontaktoplysninger i afsnittet [Support til Commerce-prøveversionmiljøet](#commerce-preview-environment-support) senere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-160">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section later in this topic.</span></span>

### <a name="grant-access-to-e-commerce-applications"></a><span data-ttu-id="2ebc8-161">Give adgang til e-handelsprogrammer</span><span class="sxs-lookup"><span data-stu-id="2ebc8-161">Grant access to e-Commerce applications</span></span>

> [!IMPORTANT]
> <span data-ttu-id="2ebc8-162">Den person, der logger på, skal være en Azure AD-lejeradministrator, som har Azure AD-lejer-ID'et.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-162">The person who signs in must be an Azure AD tenant admin who has the Azure AD tenant ID.</span></span> <span data-ttu-id="2ebc8-163">Hvis dette trin ikke er fuldført, vil de resterende klargøringstrin mislykkes.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-163">If this step isn't successfully completed, the remaining provisioning steps will fail.</span></span>

<span data-ttu-id="2ebc8-164">Følg disse trin for at autorisere e-Commerce-programmer til at få adgang til dit Azure-abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-164">To authorize e-Commerce applications to access your Azure subscription, follow these steps.</span></span>

1. <span data-ttu-id="2ebc8-165">Sammensæt en URL-adresse i følgende format:</span><span class="sxs-lookup"><span data-stu-id="2ebc8-165">Assemble a URL in the following format:</span></span>

    `https://login.windows.net/{AAD_TENANT_ID}/oauth2/authorize?client_id=fbcbf727-cd18-4422-a723-f8274075331a&response_type=code&redirect_uri=https://sb.manage.commerce.dynamics.com/_commerce/Consent&response_mode=query&prompt=admin_consent&state=12345`

1. <span data-ttu-id="2ebc8-166">Kopiér og Indsæt URL-adressen i din browser eller teksteditor, og erstat **\{AAD\_LEJER\_-ID\}** med dit Azure AD-lejer-ID.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-166">Copy and paste the URL into your browser or text editor, and replace **\{AAD\_TENANT\_ID\}** with your Azure AD tenant ID.</span></span> <span data-ttu-id="2ebc8-167">Åbn dernæst URL-adressen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-167">Then open the URL.</span></span>
1. <span data-ttu-id="2ebc8-168">Log på Azure AD i dialogboksen for logon, og bekræft, at du vil give **Dynamics 365 Commerce (prøveversion)** adgang til dit abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-168">In the Azure AD sign-in dialog box, sign in, and confirm that you want to grant **Dynamics 365 Commerce (Preview)** access to your subscription.</span></span> <span data-ttu-id="2ebc8-169">Du bliver sendt videre til en side, der indikerer, om handlingen lykkedes.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-169">You're redirected to a page that indicates whether the operation was successful.</span></span>

### <a name="confirm-that-preview-features-are-available-and-turned-on-in-lcs"></a><span data-ttu-id="2ebc8-170">Bekræft, at prøveversionens funktioner er tilgængelige og aktiverede i LCS</span><span class="sxs-lookup"><span data-stu-id="2ebc8-170">Confirm that preview features are available and turned on in LCS</span></span>

<span data-ttu-id="2ebc8-171">For at bekræfte, at prøveversionens funktioner er tilgængelige og aktiverede i LCS, skal du gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="2ebc8-171">To confirm that preview features are available and turned on in LCS, follow these steps.</span></span>

1. <span data-ttu-id="2ebc8-172">Log på [LCS-portalen](https://lcs.dynamics.com) ved at bruge den samme LCS-konto, som du brugte til at anmode om adgang til prøveversionen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-172">Sign in to the [LCS portal](https://lcs.dynamics.com) by using the same LCS account that you used to request access to the preview.</span></span>
1. <span data-ttu-id="2ebc8-173">Rul helt til højre på LCS-startsiden, og vælg feltet **Styring af prøveversionsfunktion**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-173">On the LCS home page, scroll all the way to the right, and select the **Preview feature management** tile.</span></span>

    ![Feltet Styring af prøveversionsfunktion](./media/preview1.png)

1. <span data-ttu-id="2ebc8-175">Rul ned til **Funktioner i private prøveversioner**, bekræft, at følgende funktioner er tilgængelige og aktiverede:</span><span class="sxs-lookup"><span data-stu-id="2ebc8-175">Scroll down to **Private preview features**, and confirm that the following features are available and turned on:</span></span>

    - <span data-ttu-id="2ebc8-176">Evaluering af e-handel</span><span class="sxs-lookup"><span data-stu-id="2ebc8-176">e-Commerce Evaluation</span></span>
    - <span data-ttu-id="2ebc8-177">Programmiljøer til Commerce-prøveversion</span><span class="sxs-lookup"><span data-stu-id="2ebc8-177">Commerce Preview Program Environments</span></span>

    ![Funktioner i private prøveversioner](./media/preview2.png)

1. <span data-ttu-id="2ebc8-179">Hvis disse funktioner ikke vises på listen, skal du kontakte Microsoft og angive din arbejdsmailadresse, LCS-konto og lejeroplysninger.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-179">If those features don't appear in the list, contact Microsoft, and provide your work email address, LCS account, and tenant details.</span></span> <span data-ttu-id="2ebc8-180">Du finder kontaktoplysninger i afsnittet [Support til Commerce-prøveversionmiljøet](#commerce-preview-environment-support).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-180">For contact information, see the [Commerce preview environment support](#commerce-preview-environment-support) section.</span></span>

### <a name="create-a-new-project"></a><span data-ttu-id="2ebc8-181">Opret et nyt projekt</span><span class="sxs-lookup"><span data-stu-id="2ebc8-181">Create a new project</span></span>

<span data-ttu-id="2ebc8-182">Hvis du vil oprette et nyt projekt i LCS, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-182">To create a new project in LCS, follow these steps.</span></span>

1. <span data-ttu-id="2ebc8-183">På LCS-startsiden skal du vælge plustegnet (**+**) for at oprette et projekt.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-183">On the LCS home page, select the plus sign (**+**) to create a project.</span></span>
1. <span data-ttu-id="2ebc8-184">Benyt en af følgende fremgangsmåder i højre rude:</span><span class="sxs-lookup"><span data-stu-id="2ebc8-184">In the right pane, follow one of these steps:</span></span>

    - <span data-ttu-id="2ebc8-185">Hvis du er en partner, skal du vælge **Overflyt, opret løsninger, og lær at bruge**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-185">If you're a partner, select **Migrate, create solutions, and learn**.</span></span>
    - <span data-ttu-id="2ebc8-186">Hvis du er en kunde, skal du vælge **Mulige førsalg**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-186">If you're a customer, select **Prospective presales**.</span></span>

1. <span data-ttu-id="2ebc8-187">Angiv et navn, beskrivelse og branche.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-187">Enter a name, description, and industry.</span></span>
1. <span data-ttu-id="2ebc8-188">I feltet **Produktnavn** skal du vælge **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-188">In the **Product name** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="2ebc8-189">I feltet **Produktversion** skal du vælge **Dynamics 365 Retail**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-189">In the **Product version** field, select **Dynamics 365 Retail**.</span></span>
1. <span data-ttu-id="2ebc8-190">I feltet **Metode** skal du vælge **Dynamics Retail-implementeringsmetode**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-190">In the **Methodology** field, select **Dynamics Retail implementation methodology**.</span></span>
1. <span data-ttu-id="2ebc8-191">Valgfrit: Du kan importere roller og brugere fra et eksisterende projekt.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-191">Optional: You can import roles and users from an existing project.</span></span>
1. <span data-ttu-id="2ebc8-192">Vælg **Opret**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-192">Select **Create**.</span></span> <span data-ttu-id="2ebc8-193">Projektoversigten vises.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-193">The project view appears.</span></span>

### <a name="add-the-azure-connector"></a><span data-ttu-id="2ebc8-194">Tilføj Azure Connector</span><span class="sxs-lookup"><span data-stu-id="2ebc8-194">Add the Azure Connector</span></span>

<span data-ttu-id="2ebc8-195">Hvis du vil tilføje Azure Connector til dit LCS-projekt, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-195">To add the Azure Connector to your LCS project, follow these steps.</span></span>

1. <span data-ttu-id="2ebc8-196">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="2ebc8-196">Follow one of these steps:</span></span>

    - <span data-ttu-id="2ebc8-197">Hvis du er en partner, skal du vælge feltet **Projektindstillinger** længst til højre.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-197">If you're a partner, select the **Project settings** tile on the far right.</span></span>
    - <span data-ttu-id="2ebc8-198">Hvis du er en kunde, skal du vælge **Projektindstillinger** i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-198">If you're a customer, select **Project settings** on the top menu.</span></span>

1. <span data-ttu-id="2ebc8-199">Vælg **Azure-connectorer**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-199">Select **Azure connectors**.</span></span>
1. <span data-ttu-id="2ebc8-200">Vælg **Tilføj** for at tilføje Azure Connector'en.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-200">Select **Add** to add the Azure Connector.</span></span>
1. <span data-ttu-id="2ebc8-201">Skriv et navn.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-201">Enter a name.</span></span>
1. <span data-ttu-id="2ebc8-202">Angiv dit Azure-abonnements-ID.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-202">Enter your Azure subscription ID.</span></span>
1. <span data-ttu-id="2ebc8-203">Aktiver indstillingen **Konfigurer til at bruge Azure Resource Manager (ARM)**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-203">Turn on the **Configure to use Azure Resource Manager (ARM)** option.</span></span>
1. <span data-ttu-id="2ebc8-204">Kontrollér, at værdien **Azure-abonnement AAD-lejerdomæne (eller ID)** er korrekt.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-204">Verify that the **Azure subscription AAD Tenant Domain (or ID)** value is correct.</span></span> <span data-ttu-id="2ebc8-205">Kontakt om nødvendigt din Azure-abonnementsadministrator.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-205">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="2ebc8-206">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-206">Select **Next**.</span></span>
1. <span data-ttu-id="2ebc8-207">Følg instruktionerne på siden for at give det eller de nødvendige programmer adgang til dit abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-207">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="2ebc8-208">Kontakt om nødvendigt din Azure-abonnementsadministrator.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-208">Consult your Azure subscription admin as required.</span></span>

    1. <span data-ttu-id="2ebc8-209">Log på [Azure-portalen](https://portal.azure.com/).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-209">Sign in to the [Azure portal](https://portal.azure.com/).</span></span>
    1. <span data-ttu-id="2ebc8-210">Sørg for, at den korrekte mappe er valgt, og vælg derefter **Abonnementer** i menuen til venstre.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-210">Make sure that the correct directory is selected, and then, on the menu on the left, select **Subscriptions**.</span></span>
    1. <span data-ttu-id="2ebc8-211">Find det korrekte abonnement på listen, og vælg det.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-211">Find the correct subscription in the list, and select it.</span></span> <span data-ttu-id="2ebc8-212">Brug søgefunktionen efter behov.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-212">Use the search functionality as required.</span></span>
    1. <span data-ttu-id="2ebc8-213">Vælg **Adgangskontrol (IAM)** i menuen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-213">On the menu, select **Access control (IAM)**.</span></span>
    1. <span data-ttu-id="2ebc8-214">Til højre under **Tilføj en rolletildeling** skal du vælge **Tilføj**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-214">On the right, under **Add a role assignment**, select **Add**.</span></span> <span data-ttu-id="2ebc8-215">Ruden **Tilføj rolletildeling** vises.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-215">The **Add role assignment** pane appears.</span></span>
    1. <span data-ttu-id="2ebc8-216">I feltet **Rolle** skal du vælge **Bidragsyder**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-216">In the **Role** field, select **Contributor**.</span></span>
    1. <span data-ttu-id="2ebc8-217">I feltet **Tildel adgang** skal du lade standardværdien for **Azure AD-bruger, gruppe eller tjenesteprincipal** være.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-217">In the **Assign access to** field, leave the default value, **Azure AD user, group, or service principal**.</span></span>
    1. <span data-ttu-id="2ebc8-218">Under **Vælg** skal du angive **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-218">Under **Select**, enter **b96b7e94-b82e-4e71-99a0-cf7fb188acea**.</span></span>
    1. <span data-ttu-id="2ebc8-219">Vælg **Dynamics-installationstjenester \[wsfed-enabled\]** på listen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-219">Select **Dynamics Deployment Services \[wsfed-enabled\]** in the list.</span></span>
    1. <span data-ttu-id="2ebc8-220">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-220">Select **Save**.</span></span>

1. <span data-ttu-id="2ebc8-221">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-221">Select **Next**.</span></span>
1. <span data-ttu-id="2ebc8-222">Følg instruktionerne på siden for at give det eller de nødvendige programmer adgang til dit abonnement.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-222">Follow the instructions on the page to grant the required applications access to your subscription.</span></span> <span data-ttu-id="2ebc8-223">Kontakt om nødvendigt din Azure-abonnementsadministrator.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-223">Consult your Azure subscription admin as required.</span></span>
1. <span data-ttu-id="2ebc8-224">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-224">Select **Next**.</span></span>
1. <span data-ttu-id="2ebc8-225">I feltet **Azure-region** skal du vælge **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-225">In the **Azure region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="2ebc8-226">Vælg **Forbind**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-226">Select **Connect**.</span></span> <span data-ttu-id="2ebc8-227">Din Azure-connector bør blive vist på listen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-227">Your Azure Connector should appear in the list.</span></span>

### <a name="import-the-commerce-preview-demo-base-extension"></a><span data-ttu-id="2ebc8-228">Importer Demobasisudvidelse til Commerce-prøveversion</span><span class="sxs-lookup"><span data-stu-id="2ebc8-228">Import the Commerce Preview Demo Base Extension</span></span>

<span data-ttu-id="2ebc8-229">Følg disse trin for at importere Demobasisudvidelse til Commerce-prøveversion i projektet.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-229">To import the Commerce Preview Demo Base Extension into your project, follow these steps.</span></span>

1. <span data-ttu-id="2ebc8-230">Åbn startsiden for dit projekt ved at vælge projektets navn øverst.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-230">Open the home page for your project by selecting the project name at the top.</span></span>
1. <span data-ttu-id="2ebc8-231">Udfør ét af følgende trin:</span><span class="sxs-lookup"><span data-stu-id="2ebc8-231">Follow one of these steps:</span></span>

    - <span data-ttu-id="2ebc8-232">Hvis du er en partner, skal du vælge feltet **Aktivbibliotek** længst til højre.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-232">If you're a partner, select the **Asset library** tile on the far right.</span></span>
    - <span data-ttu-id="2ebc8-233">Hvis du er en kunde, skal du vælge **Aktivbibliotek** i den øverste menu.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-233">If you're a customer, select **Asset library** on the top menu.</span></span>

1. <span data-ttu-id="2ebc8-234">Vælg **Installerbar softwarepakke** fra listen til venstre.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-234">In the list on the left, select **Software deployable package**.</span></span>
1. <span data-ttu-id="2ebc8-235">Vælg **Importér**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-235">Select **Import**.</span></span>
1. <span data-ttu-id="2ebc8-236">Under **Delt aktivbibliotek** skal du vælge **Demobasisudvidelse til Commerce-prøveversion** fra aktivlisten.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-236">Under **Shared asset library**, select **Commerce Preview Demo Base Extension** in the list of assets.</span></span>
1. <span data-ttu-id="2ebc8-237">Vælg **Pluk**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-237">Select **Pick**.</span></span> <span data-ttu-id="2ebc8-238">Du kommer tilbage til aktivbiblioteket, og du bør kunne se udvidelsen på listen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-238">You're returned to the Asset library, and you should see the extension in the list.</span></span>

<span data-ttu-id="2ebc8-239">I følgende illustration vises de handlinger, der skal udføres på LCS-siden **Aktivbibliotek**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-239">The following illustration shows the actions that must be taken on the LCS **Asset library** page.</span></span>

![Import af Demobasisudvidelse til Commerce-prøveversion](./media/import.png)

### <a name="deploy-the-environment"></a><span data-ttu-id="2ebc8-241">Installer miljøet</span><span class="sxs-lookup"><span data-stu-id="2ebc8-241">Deploy the environment</span></span>

<span data-ttu-id="2ebc8-242">Følg disse trin for at installere miljøet.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-242">To deploy the environment, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="2ebc8-243">Du behøver måske ikke at fuldføre trin 6, 7 og/eller 8, fordi sider, der har en enkelt indstilling, springes over.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-243">You might not have to complete steps 6, 7, and/or 8, because pages that have a single option are skipped.</span></span> <span data-ttu-id="2ebc8-244">Når du er i visningen **Miljøparametre**, skal du bekræfte, at teksten **Dynamics 365 Commerce (prøveversion) - Demo (10.0.6 med platformsopdatering 30)** vises direkte over feltet **Miljønavn**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-244">When you're in the **Environment parameters** view, confirm that the text **Dynamics 365 Commerce (Preview) - Demo (10.0.6 with Platform update 30)** appears directly above the **Environment name** field.</span></span> <span data-ttu-id="2ebc8-245">Se den illustration, der vises efter trin 8.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-245">See the illustration that appears after step 8.</span></span>

1. <span data-ttu-id="2ebc8-246">Vælg **Skybaserede miljøer** øverst i menuen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-246">On the top menu, select **Cloud-hosted environments**.</span></span>
1. <span data-ttu-id="2ebc8-247">Vælg **Tilføj** for at tilføje et miljø.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-247">Select **Add** to add an environment.</span></span>
1. <span data-ttu-id="2ebc8-248">I feltet **Programversion** skal du vælge **10.0.6**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-248">In the **Application version** field, select **10.0.6**.</span></span>
1. <span data-ttu-id="2ebc8-249">I feltet **Platformsversion** skal du vælge **Platformsopdatering 30**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-249">In the **Platform version** field, select **Platform Update 30**.</span></span>

    ![Valg af program- og platformsversioner](./media/project1.png)

1. <span data-ttu-id="2ebc8-251">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-251">Select **Next**.</span></span>
1. <span data-ttu-id="2ebc8-252">Vælg **Demo** miljøtopologi.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-252">Select **Demo** as the environment topology.</span></span>

    ![Valg af miljøtopologi 1](./media/project2.png)

1. <span data-ttu-id="2ebc8-254">Vælg **Dynamics 365 Commerce (prøveversion) - Demo** som miljøtopologi.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-254">Select **Dynamics 365 Commerce (Preview) - Demo** as the environment topology.</span></span> <span data-ttu-id="2ebc8-255">Hvis du har konfigureret en enkelt Azure Connector tidligere, bruges denne til dette miljø.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-255">If you configured a single Azure Connector earlier, it will be used for this environment.</span></span> <span data-ttu-id="2ebc8-256">Hvis du har konfigureret flere Azure Connector'er, kan du vælge, hvilken connector der skal bruges: **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-256">If you configured multiple Azure Connectors, you can select which connector to use: **East US**, **East US 2**, **West US**, or **West US 2**.</span></span> <span data-ttu-id="2ebc8-257">(For at opnå den bedste altomfattende præstation anbefaler vi, at du vælger **Det vestlige USA 2**.)</span><span class="sxs-lookup"><span data-stu-id="2ebc8-257">(For the best end-to-end performance, we recommend that you select **West US 2**.)</span></span>

    ![Valg af miljøtopologi 2](./media/project3.png)

1. <span data-ttu-id="2ebc8-259">Angiv et miljønavn på side **Installer miljø**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-259">On the **Deploy environment** page, enter an environment name.</span></span> <span data-ttu-id="2ebc8-260">Lad de avancerede indstillinger være, som de er.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-260">Leave the advanced settings as they are.</span></span>

    ![Siden Installer miljø](./media/project4.png)

1. <span data-ttu-id="2ebc8-262">Juster VM-størrelsen efter behov.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-262">Adjust the VM size as required.</span></span> <span data-ttu-id="2ebc8-263">(Vi anbefaler, at VM-lagerenheden \[SKU\] **D13 V2**.)</span><span class="sxs-lookup"><span data-stu-id="2ebc8-263">(We recommend VM stock keeping unit \[SKU\] **D13 v2**.)</span></span>
1. <span data-ttu-id="2ebc8-264">Gennemgå prissætnings- og licensvilkårene, og markér derefter afkrydsningsfeltet for at angive, at du accepterer dem.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-264">Review the pricing and licensing terms, and then select the check box to indicate that you agree to them.</span></span>
1. <span data-ttu-id="2ebc8-265">Vælg **Næste**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-265">Select **Next**.</span></span>
1. <span data-ttu-id="2ebc8-266">Klik på **Installer** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-266">On the deployment confirmation page, verify that the details are correct, and then select **Deploy**.</span></span> <span data-ttu-id="2ebc8-267">Du bliver sendt tilbage til visningen **Skybaserede miljøer**, og dit miljø skulle stå på listen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-267">You're returned to the **Cloud-hosted environments** view, and your environment should appear in the list.</span></span>

    <span data-ttu-id="2ebc8-268">Det miljø, du har anmodet om, vil blive vist i køen og derefter som under installation.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-268">Your requested environment will appear as queued and then deploying.</span></span> <span data-ttu-id="2ebc8-269">Det vil tage nogen tid at fuldføre miljø arbejdsgangene.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-269">The environment workflows will take some time to be completed.</span></span> <span data-ttu-id="2ebc8-270">Kom derfor tilbage efter ca. seks til ni timer.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-270">Therefore, check back after approximately six to nine hours.</span></span>

1. <span data-ttu-id="2ebc8-271">Før du fortsætter, skal du kontrollere, at din statussen for dit miljø er **Installeret**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-271">Before you continue, make sure that the status of your environment is **Deployed**.</span></span>

### <a name="initialize-rcsu"></a><span data-ttu-id="2ebc8-272">Initialisere RCSU</span><span class="sxs-lookup"><span data-stu-id="2ebc8-272">Initialize RCSU</span></span>

<span data-ttu-id="2ebc8-273">Følg disse trin for at påbegynde RCSU.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-273">To initialize RCSU, follow these steps.</span></span>

1. <span data-ttu-id="2ebc8-274">Vælg dit miljø på listen i visningen **Skybaserede miljøer**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-274">In the **Cloud-hosted environments** view, select your environment in the list.</span></span>
1. <span data-ttu-id="2ebc8-275">Vælg **Alle detaljer** i miljøvisningen til højre.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-275">In the environment view on the right, select **Full details**.</span></span> <span data-ttu-id="2ebc8-276">Visningen med miljødetaljer vises.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-276">The environment details view appears.</span></span>
1. <span data-ttu-id="2ebc8-277">Under **Miljøfunktioner** skal du vælge **Administrer**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-277">Under **Environment features**, select **Manage**.</span></span>
1. <span data-ttu-id="2ebc8-278">På fanen **Retail** skal du vælge **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-278">On the **Retail** tab, select **Initialize**.</span></span> <span data-ttu-id="2ebc8-279">RCSU-initialiseringsparametrene bliver vist.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-279">The RCSU initialization parameters view appears.</span></span>
1. <span data-ttu-id="2ebc8-280">I feltet **Tegion** skal du vælge **Det østlige USA**, **Det østlige USA 2**, **Det vestlige USA** eller **Det vestlige USA 2**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-280">In the **Region** field, select **East US**, **East US 2**, **West US**, or **West US 2**.</span></span>
1. <span data-ttu-id="2ebc8-281">I feltet **Version** skal du vælge **Angiv en Version** på listen og derefter angive **9.16.19262.5** i det felt, der vises.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-281">In the **Version** field, select **Specify a version** in the list, and then specify **9.16.19262.5** in the field that appears.</span></span> <span data-ttu-id="2ebc8-282">Sørg for at angive den nøjagtige version, der er angivet her.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-282">Be sure to specify the exact version that is indicated here.</span></span> <span data-ttu-id="2ebc8-283">Ellers skal du opdatere RCSU til den korrekte version senere.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-283">Otherwise, you will have to update RCSU to the correct version later.</span></span>
1. <span data-ttu-id="2ebc8-284">Aktivér indstillingen **Anvend udvidelse**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-284">Turn on the **Apply extension** option.</span></span>
1. <span data-ttu-id="2ebc8-285">Vælg **Demobasisudvidelse til Commerce-prøveversion** på listen over udvidelser.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-285">In the list of extensions, select **Commerce Preview Demo Base Extension**.</span></span>
1. <span data-ttu-id="2ebc8-286">Vælg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-286">Select **Initialize**.</span></span>
1. <span data-ttu-id="2ebc8-287">Klik på **Ja** på siden til bekræftelse af installationen, når du har kontrolleret, at oplysningerne er korrekte.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-287">On the deployment confirmation page, verify that the details are correct, and then select **Yes**.</span></span> <span data-ttu-id="2ebc8-288">Du returneres til visningen **Retail management**, hvor fanen **Retail** er valgt.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-288">You're returned to the **Retail management** view, where the **Retail** tab is selected.</span></span> <span data-ttu-id="2ebc8-289">Din RCSU er sat i kø til klargøring.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-289">Your RCSU has been queued for provisioning.</span></span>
1. <span data-ttu-id="2ebc8-290">Før du fortsætter, skal du kontrollere, at din statussen for dit RCSU er **Vellykket**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-290">Before you continue, make sure that the status of your RCSU is **Success**.</span></span> <span data-ttu-id="2ebc8-291">Initialiseringen tager ca. to til fem timer.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-291">Initialization takes approximately two to five hours.</span></span>

### <a name="initialize-e-commerce"></a><span data-ttu-id="2ebc8-292">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="2ebc8-292">Initialize e-Commerce</span></span>

<span data-ttu-id="2ebc8-293">Følg disse trin for at påbegynde e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-293">To initialize e-Commerce, follow these steps.</span></span>

1. <span data-ttu-id="2ebc8-294">Under fanen **e-Commerce (prøveversion)** skal du gennemgå samtykket for prøveversionen og derefter vælge **Opsætning**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-294">On the **e-Commerce (Preview)** tab, review the preview consent, and then select **Setup**.</span></span>
1. <span data-ttu-id="2ebc8-295">Angiv et navn for **e-Commerce-lejernavn** i feltet.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-295">In the **e-Commerce tenant name** field, enter a name.</span></span> <span data-ttu-id="2ebc8-296">Bemærk dog, at navnet vil være synligt i nogle af URL-adresserne, der peger på din e-Commerce-forekomst.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-296">However, be aware that this name will appear in some of the URLs that point to your e-Commerce instance.</span></span>
1. <span data-ttu-id="2ebc8-297">I feltet **Retail cloud scale unit-navn** skal du vælge din RCSU fra listen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-297">In the **Retail cloud scale unit name** field, select your RCSU in the list.</span></span> <span data-ttu-id="2ebc8-298">(Listen bør kun have én indstilling.)</span><span class="sxs-lookup"><span data-stu-id="2ebc8-298">(The list should have only one option.)</span></span>

    <span data-ttu-id="2ebc8-299">Feltet **e-Commerce-geografi** angives automatisk, og værdien kan ikke ændres.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-299">The **e-Commerce geography** field is set automatically, and the value can't be changed.</span></span>

1. <span data-ttu-id="2ebc8-300">Vælg **Næste** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-300">Select **Next** to continue.</span></span>
1. <span data-ttu-id="2ebc8-301">I feltet **Understøttede værtsnavne** skal du angive et vilkårligt gyldigt domæne som f.eks. `www.fabrikam.com`.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-301">In the **Supported host names** field, enter any valid domain, such as `www.fabrikam.com`.</span></span>
1.  <span data-ttu-id="2ebc8-302">I feltet **AAD-sikkerhedsgruppe for systemadministrator** skal du angive de første få bogstaver i navnet på den sikkerhedsgruppe, som du ønsker at bruge.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-302">In the **AAD security group for system admin** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="2ebc8-303">Vælg ikonet for forstørrelsesglasset for at få vist søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-303">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="2ebc8-304">Vælg en sikkerhedsgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-304">Select a security group from the list.</span></span>
2.  <span data-ttu-id="2ebc8-305">I feltet **AAD-sikkerhedsgruppen for redaktører for vurderinger og anmeldelser** skal du angive de første få bogstaver i navnet på den sikkerhedsgruppe, som du ønsker at bruge.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-305">In the **AAD security group for ratings and review moderator** field, enter the first few letters of the name of the security group that you want to use.</span></span> <span data-ttu-id="2ebc8-306">Vælg ikonet for forstørrelsesglasset for at få vist søgeresultaterne.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-306">Select the magnifying class icon to display the search results.</span></span> <span data-ttu-id="2ebc8-307">Vælg en sikkerhedsgruppe på listen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-307">Select a security group from the list.</span></span>
1. <span data-ttu-id="2ebc8-308">Lad indstillingen **Aktivér tjenesten vurderinger og anmeldelser** være aktiveret.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-308">Leave the **Enable ratings and review service** option turned on.</span></span>
1. <span data-ttu-id="2ebc8-309">Hvis du allerede har fuldført samtykketrinnet for Microsoft Azure Active Directory (Azure AD) som beskrevet i afsnittet "Tildel adgang til e-Commerce-programmer", skal du markere afkrydsningsfeltet for at bekræfte dit samtykke.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-309">If you have already completed the Microsoft Azure Active Directory (Azure AD) consent step as described in the "Grant access to e-Commerce applications" section, select the check box to confirm your consent.</span></span> <span data-ttu-id="2ebc8-310">Hvis du endnu ikke har fuldført dette trin, skal du gøre det, før du fortsætter initialiseringen.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-310">If you have not yet completed this step, you need to do that before proceeding with the initialization.</span></span> <span data-ttu-id="2ebc8-311">Marker hyperlinket i teksten ved siden af afkrydsningsfeltet for at åbne dialogboksen til samtykke og fuldføre trinnet.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-311">Select the link within the text next to the check box to open the consent dialog box and complete the step.</span></span>
1. <span data-ttu-id="2ebc8-312">Vælg **Initialiser**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-312">Select **Initialize**.</span></span> <span data-ttu-id="2ebc8-313">Du bliver returneret til visningen **Detailstyring**, hvor fanen **e-Commerce (prøveversion)** er valgt.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-313">You're returned to the **Retail management** view, where the **e-Commerce (Preview)** tab is selected.</span></span> <span data-ttu-id="2ebc8-314">Din initialisering af e-Commerce er påbegyndt.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-314">E-Commerce initialization has started.</span></span>
1. <span data-ttu-id="2ebc8-315">Før du fortsætter, skal du vente, indtil initialiseringsstatus for din e-Commerce er **Initialisering blev gennemført**.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-315">Before you continue, wait until the status of e-Commerce initialization is **Initialization successful**.</span></span>
1. <span data-ttu-id="2ebc8-316">Under **Links** nederst til højre skal du notere URL-adresserne for følgende links:</span><span class="sxs-lookup"><span data-stu-id="2ebc8-316">Under **Links** in the lower right, make a note of the URLs for the following links:</span></span>

    * <span data-ttu-id="2ebc8-317">**e-Commerce-websted** – linket til roden af dit e-Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-317">**e-Commerce site** – The link to the root of your e-Commerce site.</span></span>
    * <span data-ttu-id="2ebc8-318">**Værktøj til administration af e-Commerce-websted** – linket til administrationsværktøjet for webstedet.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-318">**e-Commerce site management tool** – The link to the site management tool.</span></span>

## <a name="commerce-preview-environment-support"></a><span data-ttu-id="2ebc8-319">Support til Commerce-prøveversionsmiljøet</span><span class="sxs-lookup"><span data-stu-id="2ebc8-319">Commerce preview environment support</span></span>

<span data-ttu-id="2ebc8-320">Hvis der opstår problemer under din fuldførelse af klargøringstrinnene, kan du gå til [Microsoft Dynamics 365 Commerce-prøveversionens Yammer-gruppe](https://aka.ms/Dynamics365CommercePreviewYammer) for at få hjælp.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-320">If you experience issues while you're completing the provisioning steps, visit the [Microsoft Dynamics 365 Commerce Preview Yammer group](https://aka.ms/Dynamics365CommercePreviewYammer) for help.</span></span>

<span data-ttu-id="2ebc8-321">Hvis du oplever problemer, når du forsøger at få adgang til Yammer-gruppen, kan du kontakte Microsoft via e-mail på <Dynamics365Commerce@microsoft.com>.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-321">If you experience issues when you try to access the Yammer group, you can contact Microsoft by email at <Dynamics365Commerce@microsoft.com>.</span></span> <span data-ttu-id="2ebc8-322">Denne e-mailadresse overvåges ikke aktivt.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-322">This email address isn't actively monitored.</span></span> <span data-ttu-id="2ebc8-323">Du skal derfor regne med, at svaret vil blive forsinket.</span><span class="sxs-lookup"><span data-stu-id="2ebc8-323">Therefore, expect a delay in the response.</span></span>

## <a name="next-steps"></a><span data-ttu-id="2ebc8-324">Næste trin</span><span class="sxs-lookup"><span data-stu-id="2ebc8-324">Next steps</span></span>

<span data-ttu-id="2ebc8-325">For at fortsætte processen med klargøring og konfigurering af dit Commerce-prøveversionsmiljø se [Konfigurering af et Commerce-prøveversionsmiljø](cpe-post-provisioning.md).</span><span class="sxs-lookup"><span data-stu-id="2ebc8-325">To continue the process of provisioning and configuring your Commerce preview environment, see [Configure a Commerce preview environment](cpe-post-provisioning.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="2ebc8-326">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="2ebc8-326">Additional resources</span></span>

[<span data-ttu-id="2ebc8-327">Oversigt over miljø til prøveversion af Commerce</span><span class="sxs-lookup"><span data-stu-id="2ebc8-327">Commerce preview environment overview</span></span>](cpe-overview.md)

[<span data-ttu-id="2ebc8-328">Konfigurering af et Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="2ebc8-328">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="2ebc8-329">Konfigurer valgfrie funktioner for et Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="2ebc8-329">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="2ebc8-330">Ofte stillede spørgsmål om Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="2ebc8-330">Commerce preview environment FAQ</span></span>](cpe-faq.md)

[<span data-ttu-id="2ebc8-331">Microsoft Lifecycle Services (LCS)</span><span class="sxs-lookup"><span data-stu-id="2ebc8-331">Microsoft Lifecycle Services (LCS)</span></span>](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide)

[<span data-ttu-id="2ebc8-332">Retail Cloud Scale Unit (RCSU)</span><span class="sxs-lookup"><span data-stu-id="2ebc8-332">Retail Cloud Scale Unit (RCSU)</span></span>](https://docs.microsoft.com/business-applications-release-notes/october18/dynamics365-retail/retail-cloud-scale-unit)

[<span data-ttu-id="2ebc8-333">Microsoft Azure-portal</span><span class="sxs-lookup"><span data-stu-id="2ebc8-333">Microsoft Azure portal</span></span>](https://azure.microsoft.com/features/azure-portal)

[<span data-ttu-id="2ebc8-334">Dynamics 365 Commerce-websted</span><span class="sxs-lookup"><span data-stu-id="2ebc8-334">Dynamics 365 Commerce website</span></span>](https://aka.ms/Dynamics365CommerceWebsite)

[<span data-ttu-id="2ebc8-335">Hjælp-ressourcer til Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="2ebc8-335">Help resources for Dynamics 365 Retail</span></span>](../retail/index.md)
