---
title: Implementere en ny e-handelslejer
description: I dette emne beskrives, hvordan du implementerer et nyt Dynamics 365 Commerce-e-handelswebsted ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 0fff5d47d6eb3e08288d17853fcd94f9eab843c3
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5801943"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="eb41c-103">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="eb41c-103">Deploy a new e-commerce tenant</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="eb41c-104">I dette emne beskrives, hvordan du implementerer et nyt Dynamics 365 Commerce-e-handelswebsted ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="eb41c-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

<span data-ttu-id="eb41c-105">Microsoft Dynamics Lifecycle Services (LCS) er et skybaseret arbejdsområde til samarbejde, som partnere og kunder kan bruge til at styre deres projekter og miljøer, få vist de seneste oplysninger om Microsoft Dynamics-produkter og -funktioner og oprette, spore og gennemse supporthændelser.</span><span class="sxs-lookup"><span data-stu-id="eb41c-105">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="eb41c-106">Funktioner til styring e-handel er integreret i LCS.</span><span class="sxs-lookup"><span data-stu-id="eb41c-106">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="eb41c-107">Du kan få mere at vide om LCS i [Brugervejledning til Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="eb41c-107">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="eb41c-108">Introduktion</span><span class="sxs-lookup"><span data-stu-id="eb41c-108">Get started</span></span>

<span data-ttu-id="eb41c-109">Før du kan initialisere e-handel, skal du initialisere et projekt, et miljø og en Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="eb41c-109">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="eb41c-110">Når du vil udføre initialiseringen i LCS, skal du have rettigheder til enten Projektejer- eller Miljøadministrator-rollen.</span><span class="sxs-lookup"><span data-stu-id="eb41c-110">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="eb41c-111">Topologierne for produktions- og sandkassemiljøet understøttes.</span><span class="sxs-lookup"><span data-stu-id="eb41c-111">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="eb41c-112">Du kan finde flere oplysninger om miljøer under [Miljøplanlægning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="eb41c-112">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="eb41c-113">Du kan finde flere oplysninger om RCSU under [Initialisere Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="eb41c-113">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="eb41c-114">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="eb41c-114">Initialize e-commerce</span></span>

<span data-ttu-id="eb41c-115">Du kan bruge denne procedure til at initialisere e-handelsfunktionen i et eksisterende miljø.</span><span class="sxs-lookup"><span data-stu-id="eb41c-115">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="eb41c-116">Før du går i gang, skal du sikre dig, at du har følgende påkrævede oplysninger:</span><span class="sxs-lookup"><span data-stu-id="eb41c-116">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="eb41c-117">Den RCSU, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="eb41c-117">The RCSU that will be used.</span></span>
- <span data-ttu-id="eb41c-118">Den Microsoft Azure Active Directory-sikkerhedsgruppe, der skal bruges til administratorer af e-handelssystemet.</span><span class="sxs-lookup"><span data-stu-id="eb41c-118">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="eb41c-119">Den Microsoft Azure Active Directory-sikkerhedsgruppe, der skal bruges til vurderings- og anmeldelsesredaktører.</span><span class="sxs-lookup"><span data-stu-id="eb41c-119">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="eb41c-120">De domæner, der skal knyttes til miljøet.</span><span class="sxs-lookup"><span data-stu-id="eb41c-120">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="eb41c-121">Derudover kan du indsamle følgende valgfrie oplysninger:</span><span class="sxs-lookup"><span data-stu-id="eb41c-121">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="eb41c-122">Oplysninger om Azure AD business-to-consumer (B2C):</span><span class="sxs-lookup"><span data-stu-id="eb41c-122">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="eb41c-123">Navn på lejer.</span><span class="sxs-lookup"><span data-stu-id="eb41c-123">Tenant Name.</span></span>
    - <span data-ttu-id="eb41c-124">Klient-id.</span><span class="sxs-lookup"><span data-stu-id="eb41c-124">Client ID.</span></span>
    - <span data-ttu-id="eb41c-125">Logon på brugerdefineret domæne.</span><span class="sxs-lookup"><span data-stu-id="eb41c-125">Login Custom Domain.</span></span>
    - <span data-ttu-id="eb41c-126">Svar-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="eb41c-126">Reply URL.</span></span>
    - <span data-ttu-id="eb41c-127">Politik-id for tilmelding og logon.</span><span class="sxs-lookup"><span data-stu-id="eb41c-127">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="eb41c-128">Politik-id for nulstilling af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="eb41c-128">Reset password Policy ID.</span></span>
    - <span data-ttu-id="eb41c-129">Rediger profilpolitik-id.</span><span class="sxs-lookup"><span data-stu-id="eb41c-129">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="eb41c-130">Disse oplysninger kan tilføjes senere via en serviceanmodning.</span><span class="sxs-lookup"><span data-stu-id="eb41c-130">This information can be added later, through a service request.</span></span>

<span data-ttu-id="eb41c-131">Når du har indsamlet de nødvendige oplysninger, skal du udføre disse trin for at initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="eb41c-131">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="eb41c-132">Log på [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="eb41c-132">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="eb41c-133">Åbn det projekt, der indeholder det miljø, hvor du vil initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="eb41c-133">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="eb41c-134">Vælg miljøet i sektionen **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="eb41c-134">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="eb41c-135">Vælg linket **Retail administration** under **Funktioner i miljøet**.</span><span class="sxs-lookup"><span data-stu-id="eb41c-135">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="eb41c-136">Under fanen **e-handel** skal du vælge **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="eb41c-136">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="eb41c-137">Der vises en dialogboks, hvor du skal angive de oplysninger, der skal bruges til klargøring.</span><span class="sxs-lookup"><span data-stu-id="eb41c-137">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="eb41c-138">Udfyld de påkrævede oplysninger, og gå derefter til næste side.</span><span class="sxs-lookup"><span data-stu-id="eb41c-138">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="eb41c-139">På næste side skal du udfylde de påkrævede oplysninger og derefter sende formularen.</span><span class="sxs-lookup"><span data-stu-id="eb41c-139">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="eb41c-140">Du vender tilbage til fanen **e-handel**, hvor du kan se, at initialiseringen er startet.</span><span class="sxs-lookup"><span data-stu-id="eb41c-140">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="eb41c-141">Hvis du vil have vist initialiseringsstatus, skal du enten vælge **Opdater** eller vende tilbage til fanen **e-handel** senere.</span><span class="sxs-lookup"><span data-stu-id="eb41c-141">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="eb41c-142">Når e-handel initialiseres fra LCS, klargør systemet flere komponenter, der kræves til e-handel, og knytter dem til miljøet.</span><span class="sxs-lookup"><span data-stu-id="eb41c-142">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="eb41c-143">Når klargøringen er fuldført, opdateres fanen **e-handel** på siden **Detailstyring**, så den afspejler klargøringen.</span><span class="sxs-lookup"><span data-stu-id="eb41c-143">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="eb41c-144">På siden vises de seneste tilpasningsinstallationer og status for eventuelle andre igangværende installationer.</span><span class="sxs-lookup"><span data-stu-id="eb41c-144">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="eb41c-145">Siden indeholder også links til e-handelswebstedet og generatoren til e-handelswebsteder, hvor websteder oprettes.</span><span class="sxs-lookup"><span data-stu-id="eb41c-145">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="eb41c-146">Få adgang til Commerce-webstedsgenerator</span><span class="sxs-lookup"><span data-stu-id="eb41c-146">Access Commerce site builder</span></span>

<span data-ttu-id="eb41c-147">Hvis du vil have adgang til Commerce-webstedsgeneratoren, skal du gå til fanen **e-handel** på siden **Detailstyring** i LCS og vælge linket **Administrationsværktøj til websted for e-handel**.</span><span class="sxs-lookup"><span data-stu-id="eb41c-147">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="eb41c-148">Landingssiden for webstedsgeneratoren viser en visning på lejerniveau.</span><span class="sxs-lookup"><span data-stu-id="eb41c-148">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="eb41c-149">Fra denne side kan du:</span><span class="sxs-lookup"><span data-stu-id="eb41c-149">From this page, you can:</span></span>

- <span data-ttu-id="eb41c-150">Redigere indstillinger på lejerniveau.</span><span class="sxs-lookup"><span data-stu-id="eb41c-150">Modify tenant-level settings.</span></span>
- <span data-ttu-id="eb41c-151">Navigere til et websted, du har oprettet og har tilladelse til at få vist.</span><span class="sxs-lookup"><span data-stu-id="eb41c-151">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="eb41c-152">Få adgang til funktioner til gennemsyn, f.eks. redigering og rapportering.</span><span class="sxs-lookup"><span data-stu-id="eb41c-152">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="eb41c-153">Oprette et nyt websted.</span><span class="sxs-lookup"><span data-stu-id="eb41c-153">Create a new site.</span></span> <span data-ttu-id="eb41c-154">Du kan finde flere oplysninger om, hvordan du opretter et nyt websted [Oprette et websted for e-handel](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="eb41c-154">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="eb41c-155">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="eb41c-155">Additional resources</span></span>

[<span data-ttu-id="eb41c-156">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="eb41c-156">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="eb41c-157">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="eb41c-157">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="eb41c-158">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="eb41c-158">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="eb41c-159">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="eb41c-159">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="eb41c-160">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="eb41c-160">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="eb41c-161">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="eb41c-161">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="eb41c-162">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="eb41c-162">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="eb41c-163">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="eb41c-163">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="eb41c-164">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="eb41c-164">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="eb41c-165">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="eb41c-165">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
