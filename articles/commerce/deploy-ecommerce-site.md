---
title: Implementere en ny e-handelslejer
description: I dette emne beskrives, hvordan du implementerer et nyt Dynamics 365 Commerce-e-handelswebsted ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 157dc8225e5bbf9338a1b5a79a2880e8a8c4bf10
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517276"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="92c1a-103">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="92c1a-103">Deploy a new e-commerce tenant</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="92c1a-104">I dette emne beskrives, hvordan du implementerer et nyt Dynamics 365 Commerce-e-handelswebsted ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="92c1a-104">This topic describes how to deploy a new Dynamics 365 Commerce e-commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="92c1a-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="92c1a-105">Overview</span></span>

<span data-ttu-id="92c1a-106">Microsoft Dynamics Lifecycle Services (LCS) er et skybaseret arbejdsområde til samarbejde, som partnere og kunder kan bruge til at styre deres projekter og miljøer, få vist de seneste oplysninger om Microsoft Dynamics-produkter og -funktioner og oprette, spore og gennemse supporthændelser.</span><span class="sxs-lookup"><span data-stu-id="92c1a-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="92c1a-107">Funktioner til styring e-handel er integreret i LCS.</span><span class="sxs-lookup"><span data-stu-id="92c1a-107">E-commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="92c1a-108">Du kan få mere at vide om LCS i [Brugervejledning til Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="92c1a-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="92c1a-109">Introduktion</span><span class="sxs-lookup"><span data-stu-id="92c1a-109">Get started</span></span>

<span data-ttu-id="92c1a-110">Før du kan initialisere e-handel, skal du initialisere et projekt, et miljø og en Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="92c1a-110">Before you can initialize e-commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="92c1a-111">Når du vil udføre initialiseringen i LCS, skal du have rettigheder til enten Projektejer- eller Miljøadministrator-rollen.</span><span class="sxs-lookup"><span data-stu-id="92c1a-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="92c1a-112">Topologierne for produktions- og sandkassemiljøet understøttes.</span><span class="sxs-lookup"><span data-stu-id="92c1a-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="92c1a-113">Du kan finde flere oplysninger om miljøer under [Miljøplanlægning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="92c1a-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="92c1a-114">Du kan finde flere oplysninger om RCSU under [Initialisere Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="92c1a-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="92c1a-115">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="92c1a-115">Initialize e-commerce</span></span>

<span data-ttu-id="92c1a-116">Du kan bruge denne procedure til at initialisere e-handelsfunktionen i et eksisterende miljø.</span><span class="sxs-lookup"><span data-stu-id="92c1a-116">Use this procedure to initialize the e-commerce feature in an existing environment.</span></span>

<span data-ttu-id="92c1a-117">Før du går i gang, skal du sikre dig, at du har følgende påkrævede oplysninger:</span><span class="sxs-lookup"><span data-stu-id="92c1a-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="92c1a-118">Den RCSU, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="92c1a-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="92c1a-119">Den Microsoft Azure Active Directory-sikkerhedsgruppe, der skal bruges til administratorer af e-handelssystemet.</span><span class="sxs-lookup"><span data-stu-id="92c1a-119">The Microsoft Azure Active Directory security group that will be used for e-commerce system admins.</span></span>
- <span data-ttu-id="92c1a-120">Den Microsoft Azure Active Directory-sikkerhedsgruppe, der skal bruges til vurderings- og anmeldelsesredaktører.</span><span class="sxs-lookup"><span data-stu-id="92c1a-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="92c1a-121">De domæner, der skal knyttes til miljøet.</span><span class="sxs-lookup"><span data-stu-id="92c1a-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="92c1a-122">Derudover kan du indsamle følgende valgfrie oplysninger:</span><span class="sxs-lookup"><span data-stu-id="92c1a-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="92c1a-123">Oplysninger om Azure AD business-to-consumer (B2C):</span><span class="sxs-lookup"><span data-stu-id="92c1a-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="92c1a-124">Navn på lejer.</span><span class="sxs-lookup"><span data-stu-id="92c1a-124">Tenant Name.</span></span>
    - <span data-ttu-id="92c1a-125">Klient-id.</span><span class="sxs-lookup"><span data-stu-id="92c1a-125">Client ID.</span></span>
    - <span data-ttu-id="92c1a-126">Logon på brugerdefineret domæne.</span><span class="sxs-lookup"><span data-stu-id="92c1a-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="92c1a-127">Svar-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="92c1a-127">Reply URL.</span></span>
    - <span data-ttu-id="92c1a-128">Politik-id for tilmelding og logon.</span><span class="sxs-lookup"><span data-stu-id="92c1a-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="92c1a-129">Politik-id for nulstilling af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="92c1a-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="92c1a-130">Rediger profilpolitik-id.</span><span class="sxs-lookup"><span data-stu-id="92c1a-130">Edit Profile Policy ID.</span></span>

> [!NOTE]
> <span data-ttu-id="92c1a-131">Disse oplysninger kan tilføjes senere via en serviceanmodning.</span><span class="sxs-lookup"><span data-stu-id="92c1a-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="92c1a-132">Når du har indsamlet de nødvendige oplysninger, skal du udføre disse trin for at initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="92c1a-132">After you've collected the required information, follow these steps to initialize e-commerce.</span></span>

1. <span data-ttu-id="92c1a-133">Log på [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="92c1a-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="92c1a-134">Åbn det projekt, der indeholder det miljø, hvor du vil initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="92c1a-134">Open the project that contains the environment where you want to initialize e-commerce.</span></span>
1. <span data-ttu-id="92c1a-135">Vælg miljøet i sektionen **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="92c1a-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="92c1a-136">Vælg linket **Retail administration** under **Funktioner i miljøet**.</span><span class="sxs-lookup"><span data-stu-id="92c1a-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="92c1a-137">Under fanen **e-handel** skal du vælge **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="92c1a-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="92c1a-138">Der vises en dialogboks, hvor du skal angive de oplysninger, der skal bruges til klargøring.</span><span class="sxs-lookup"><span data-stu-id="92c1a-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="92c1a-139">Udfyld de påkrævede oplysninger, og gå derefter til næste side.</span><span class="sxs-lookup"><span data-stu-id="92c1a-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="92c1a-140">På næste side skal du udfylde de påkrævede oplysninger og derefter sende formularen.</span><span class="sxs-lookup"><span data-stu-id="92c1a-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="92c1a-141">Du vender tilbage til fanen **e-handel**, hvor du kan se, at initialiseringen er startet.</span><span class="sxs-lookup"><span data-stu-id="92c1a-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="92c1a-142">Hvis du vil have vist initialiseringsstatus, skal du enten vælge **Opdater** eller vende tilbage til fanen **e-handel** senere.</span><span class="sxs-lookup"><span data-stu-id="92c1a-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="92c1a-143">Når e-handel initialiseres fra LCS, klargør systemet flere komponenter, der kræves til e-handel, og knytter dem til miljøet.</span><span class="sxs-lookup"><span data-stu-id="92c1a-143">When e-commerce is initialized from LCS, the system provisions several components that are required for e-commerce and associates them with the environment.</span></span> <span data-ttu-id="92c1a-144">Når klargøringen er fuldført, opdateres fanen **e-handel** på siden **Detailstyring**, så den afspejler klargøringen.</span><span class="sxs-lookup"><span data-stu-id="92c1a-144">After provisioning is complete, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="92c1a-145">På siden vises de seneste tilpasningsinstallationer og status for eventuelle andre igangværende installationer.</span><span class="sxs-lookup"><span data-stu-id="92c1a-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="92c1a-146">Siden indeholder også links til e-handelswebstedet og generatoren til e-handelswebsteder, hvor websteder oprettes.</span><span class="sxs-lookup"><span data-stu-id="92c1a-146">It also includes links to the e-commerce site and the Commerce site builder where sites are authored.</span></span>

## <a name="access-commerce-site-builder"></a><span data-ttu-id="92c1a-147">Få adgang til Commerce-webstedsgenerator</span><span class="sxs-lookup"><span data-stu-id="92c1a-147">Access Commerce site builder</span></span>

<span data-ttu-id="92c1a-148">Hvis du vil have adgang til Commerce-webstedsgeneratoren, skal du gå til fanen **e-handel** på siden **Detailstyring** i LCS og vælge linket **Administrationsværktøj til websted for e-handel**.</span><span class="sxs-lookup"><span data-stu-id="92c1a-148">To access Commerce site builder, go to the **e-Commerce** tab on the **Retail management** page in LCS and select the **e-Commerce site management tool** link.</span></span> <span data-ttu-id="92c1a-149">Landingssiden for webstedsgeneratoren viser en visning på lejerniveau.</span><span class="sxs-lookup"><span data-stu-id="92c1a-149">The site builder landing page displays a tenant-level view.</span></span> <span data-ttu-id="92c1a-150">Fra denne side kan du:</span><span class="sxs-lookup"><span data-stu-id="92c1a-150">From this page, you can:</span></span>

- <span data-ttu-id="92c1a-151">Redigere indstillinger på lejerniveau.</span><span class="sxs-lookup"><span data-stu-id="92c1a-151">Modify tenant-level settings.</span></span>
- <span data-ttu-id="92c1a-152">Navigere til et websted, du har oprettet og har tilladelse til at få vist.</span><span class="sxs-lookup"><span data-stu-id="92c1a-152">Navigate to any site you have created, and have permission to view.</span></span> 
- <span data-ttu-id="92c1a-153">Få adgang til funktioner til gennemsyn, f.eks. redigering og rapportering.</span><span class="sxs-lookup"><span data-stu-id="92c1a-153">Access Reviews features such as moderation and reporting.</span></span>
- <span data-ttu-id="92c1a-154">Oprette et nyt websted.</span><span class="sxs-lookup"><span data-stu-id="92c1a-154">Create a new site.</span></span> <span data-ttu-id="92c1a-155">Du kan finde flere oplysninger om, hvordan du opretter et nyt websted [Oprette et websted for e-handel](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="92c1a-155">For more information about how to create a new site, see [Create an e-commerce site](create-ecommerce-site.md) .</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="92c1a-156">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="92c1a-156">Additional resources</span></span>

[<span data-ttu-id="92c1a-157">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="92c1a-157">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="92c1a-158">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="92c1a-158">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="92c1a-159">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="92c1a-159">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="92c1a-160">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="92c1a-160">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="92c1a-161">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="92c1a-161">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="92c1a-162">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="92c1a-162">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="92c1a-163">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="92c1a-163">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="92c1a-164">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="92c1a-164">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="92c1a-165">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="92c1a-165">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="92c1a-166">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="92c1a-166">Enable location-based store detection</span></span>](enable-store-detection.md)
