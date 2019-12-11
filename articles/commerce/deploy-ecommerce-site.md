---
title: Implementere en ny e-handelslejer
description: I dette emne beskrives, hvordan du installerer en ny e-handelslejer ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).
author: psimolin
manager: annbe
ms.date: 10/31/2019
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
ms.openlocfilehash: c2632632b9b21dd3a88e9a4df0e65cfd28e579d2
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697445"
---
# <a name="deploy-a-new-e-commerce-tenant"></a><span data-ttu-id="ca892-103">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="ca892-103">Deploy a new e-Commerce tenant</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="ca892-104">I dette emne beskrives, hvordan du implementerer et nyt e-handelswebsted ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="ca892-104">This topic describes how to deploy a new e-Commerce site by using Microsoft Dynamics Lifecycle Services (LCS).</span></span>

## <a name="overview"></a><span data-ttu-id="ca892-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="ca892-105">Overview</span></span>
    
<span data-ttu-id="ca892-106">Microsoft Dynamics Lifecycle Services (LCS) er et skybaseret arbejdsområde til samarbejde, som partnere og kunder kan bruge til at styre deres projekter og miljøer, få vist de seneste oplysninger om Microsoft Dynamics-produkter og -funktioner og oprette, spore og gennemse supporthændelser.</span><span class="sxs-lookup"><span data-stu-id="ca892-106">Microsoft Dynamics Lifecycle Services (LCS) is a cloud-based collaborative workspace that partners and customers can use to manage their projects and environments, view the latest information about Microsoft Dynamics products and features, and create, track, and browse support incidents.</span></span> <span data-ttu-id="ca892-107">Funktioner til styring e-handel er integreret i LCS.</span><span class="sxs-lookup"><span data-stu-id="ca892-107">E-Commerce management features are integrated into LCS.</span></span>

<span data-ttu-id="ca892-108">Du kan få mere at vide om LCS i [Brugervejledning til Lifecycle Services](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span><span class="sxs-lookup"><span data-stu-id="ca892-108">To learn more about LCS, see the [Lifecycle Services User Guide](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/lifecycle-services/lcs-user-guide).</span></span>
    
## <a name="get-started"></a><span data-ttu-id="ca892-109">Introduktion</span><span class="sxs-lookup"><span data-stu-id="ca892-109">Get started</span></span>

<span data-ttu-id="ca892-110">Før du kan initialisere e-handel, skal du initialisere et projekt, et miljø og en Retail Cloud Scale Unit (RCSU).</span><span class="sxs-lookup"><span data-stu-id="ca892-110">Before you can initialize e-Commerce, you must initialize a project, an environment, and a Retail Cloud Scale Unit (RCSU).</span></span> <span data-ttu-id="ca892-111">Når du vil udføre initialiseringen i LCS, skal du have rettigheder til enten Projektejer- eller Miljøadministrator-rollen.</span><span class="sxs-lookup"><span data-stu-id="ca892-111">To do the initialization in LCS, you must have permissions for either the Project Owner or Environment manager role.</span></span> <span data-ttu-id="ca892-112">Topologierne for produktions- og sandkassemiljøet understøttes.</span><span class="sxs-lookup"><span data-stu-id="ca892-112">The production and sandbox environment topologies are supported.</span></span>

<span data-ttu-id="ca892-113">Du kan finde flere oplysninger om miljøer under [Miljøplanlægning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span><span class="sxs-lookup"><span data-stu-id="ca892-113">For more information about environments, see [Environment planning](https://docs.microsoft.com/dynamics365/unified-operations/fin-and-ops/imp-lifecycle/environment-planning).</span></span> <span data-ttu-id="ca892-114">Du kan finde flere oplysninger om RCSU under [Initialisere Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span><span class="sxs-lookup"><span data-stu-id="ca892-114">For more information about RCSU, see [Initialize Retail Cloud Scale Unit](https://docs.microsoft.com/dynamics365/unified-operations/dev-itpro/deployment/initialize-retail-channels).</span></span>

## <a name="initialize-e-commerce"></a><span data-ttu-id="ca892-115">Initialisere e-handel</span><span class="sxs-lookup"><span data-stu-id="ca892-115">Initialize e-Commerce</span></span>

<span data-ttu-id="ca892-116">Du kan bruge denne procedure til at initialisere e-handelsfunktionen i et eksisterende miljø.</span><span class="sxs-lookup"><span data-stu-id="ca892-116">Use this procedure to initialize the e-Commerce feature in an existing environment.</span></span>

<span data-ttu-id="ca892-117">Før du går i gang, skal du sikre dig, at du har følgende påkrævede oplysninger:</span><span class="sxs-lookup"><span data-stu-id="ca892-117">Before you begin, make sure that you have the following required information:</span></span>

- <span data-ttu-id="ca892-118">Den RCSU, der skal bruges.</span><span class="sxs-lookup"><span data-stu-id="ca892-118">The RCSU that will be used.</span></span>
- <span data-ttu-id="ca892-119">Den Microsoft Azure Active Directory-sikkerhedsgruppe, der skal bruges til administratorer af e-handel-systemet.</span><span class="sxs-lookup"><span data-stu-id="ca892-119">The Microsoft Azure Active Directory security group that will be used for e-Commerce system admins.</span></span>
- <span data-ttu-id="ca892-120">Den Microsoft Azure Active Directory-sikkerhedsgruppe, der skal bruges til vurderings- og anmeldelsesredaktører.</span><span class="sxs-lookup"><span data-stu-id="ca892-120">The Microsoft Azure Active Directory security group that will be used for ratings and reviews moderators.</span></span>
- <span data-ttu-id="ca892-121">De domæner, der skal knyttes til miljøet.</span><span class="sxs-lookup"><span data-stu-id="ca892-121">The domains that will be associated with the environment.</span></span>

<span data-ttu-id="ca892-122">Derudover kan du indsamle følgende valgfrie oplysninger:</span><span class="sxs-lookup"><span data-stu-id="ca892-122">In addition, you can collect the following optional information:</span></span>

- <span data-ttu-id="ca892-123">Oplysninger om Azure AD business-to-consumer (B2C):</span><span class="sxs-lookup"><span data-stu-id="ca892-123">Azure AD business-to-consumer (B2C) information:</span></span>

    - <span data-ttu-id="ca892-124">Navn på lejer.</span><span class="sxs-lookup"><span data-stu-id="ca892-124">Tenant Name.</span></span>
    - <span data-ttu-id="ca892-125">Klient-id.</span><span class="sxs-lookup"><span data-stu-id="ca892-125">Client ID.</span></span>
    - <span data-ttu-id="ca892-126">Logon på brugerdefineret domæne.</span><span class="sxs-lookup"><span data-stu-id="ca892-126">Login Custom Domain.</span></span>
    - <span data-ttu-id="ca892-127">Svar-URL-adresse.</span><span class="sxs-lookup"><span data-stu-id="ca892-127">Reply URL.</span></span>
    - <span data-ttu-id="ca892-128">Politik-id for tilmelding og logon.</span><span class="sxs-lookup"><span data-stu-id="ca892-128">SignUp SignIn Policy ID.</span></span>
    - <span data-ttu-id="ca892-129">Politik-id for nulstilling af adgangskode.</span><span class="sxs-lookup"><span data-stu-id="ca892-129">Reset password Policy ID.</span></span>
    - <span data-ttu-id="ca892-130">Rediger profilpolitik-id.</span><span class="sxs-lookup"><span data-stu-id="ca892-130">Edit Profile Policy ID.</span></span>

[!NOTE]
<span data-ttu-id="ca892-131">Disse oplysninger kan tilføjes senere via en serviceanmodning.</span><span class="sxs-lookup"><span data-stu-id="ca892-131">This information can be added later, through a service request.</span></span>

<span data-ttu-id="ca892-132">Når du har indsamlet de nødvendige oplysninger, skal du udføre disse trin for at initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="ca892-132">After you've collected the required information, follow these steps to initialize e-Commerce.</span></span>

1. <span data-ttu-id="ca892-133">Log på [LCS](https://lcs.dynamics.com).</span><span class="sxs-lookup"><span data-stu-id="ca892-133">Sign in to [LCS](https://lcs.dynamics.com).</span></span>
1. <span data-ttu-id="ca892-134">Åbn det projekt, der indeholder det miljø, hvor du vil initialisere e-handel.</span><span class="sxs-lookup"><span data-stu-id="ca892-134">Open the project that contains the environment where you want to initialize e-Commerce.</span></span>
1. <span data-ttu-id="ca892-135">Vælg miljøet i sektionen **Miljøer**.</span><span class="sxs-lookup"><span data-stu-id="ca892-135">In the **Environments** section, select the environment.</span></span>
1. <span data-ttu-id="ca892-136">Vælg linket **Retail administration** under **Funktioner i miljøet**.</span><span class="sxs-lookup"><span data-stu-id="ca892-136">Under **Environment features**, select the **Retail manage** link.</span></span>
1. <span data-ttu-id="ca892-137">Under fanen **e-handel** skal du vælge **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="ca892-137">On the **e-Commerce** tab, select **Setup**.</span></span> <span data-ttu-id="ca892-138">Der vises en dialogboks, hvor du skal angive de oplysninger, der skal bruges til klargøring.</span><span class="sxs-lookup"><span data-stu-id="ca892-138">A dialog box appears, where you must enter the information that is required for provisioning.</span></span>
1. <span data-ttu-id="ca892-139">Udfyld de påkrævede oplysninger, og gå derefter til næste side.</span><span class="sxs-lookup"><span data-stu-id="ca892-139">Fill in the required information, and then go to the next page.</span></span>
1. <span data-ttu-id="ca892-140">På næste side skal du udfylde de påkrævede oplysninger og derefter sende formularen.</span><span class="sxs-lookup"><span data-stu-id="ca892-140">On the next page, fill in the required information, and then submit the form.</span></span> <span data-ttu-id="ca892-141">Du vender tilbage til fanen **e-handel**, hvor du kan se, at initialiseringen er startet.</span><span class="sxs-lookup"><span data-stu-id="ca892-141">You're returned to the **e-Commerce** tab, where you should see that initialization has been started.</span></span>
1. <span data-ttu-id="ca892-142">Hvis du vil have vist initialiseringsstatus, skal du enten vælge **Opdater** eller vende tilbage til fanen **e-handel** senere.</span><span class="sxs-lookup"><span data-stu-id="ca892-142">To view the initialization status, either **Refresh** or return to the **e-Commerce** tab later.</span></span>
    
<span data-ttu-id="ca892-143">Når e-handel initialiseres fra LCS, klargør systemet flere komponenter, der kræves til e-handel, og knytter dem til miljøet.</span><span class="sxs-lookup"><span data-stu-id="ca892-143">When e-Commerce is initialized from LCS, the system provisions several components that are required for e-Commerce and associates them with the environment.</span></span> <span data-ttu-id="ca892-144">Når klargøringen er fuldført, opdateres fanen **e-handel** på siden **Detailstyring** og afspejler klargøringen.</span><span class="sxs-lookup"><span data-stu-id="ca892-144">After provisioning is completed, the **e-Commerce** tab on the **Retail management** page is updated to reflect the provisioning.</span></span> <span data-ttu-id="ca892-145">På siden vises de seneste tilpasningsinstallationer og status for eventuelle andre igangværende installationer.</span><span class="sxs-lookup"><span data-stu-id="ca892-145">The page shows the latest customization deployments and the status of any other ongoing deployments.</span></span> <span data-ttu-id="ca892-146">Siden indeholder også links til e-handelswebstedet og værktøjet til administration af e-handelswebsteder (oprettelsesværktøj).</span><span class="sxs-lookup"><span data-stu-id="ca892-146">It also includes links to the e-Commerce site and the e-Commerce site management tool (the authoring tool).</span></span>

## <a name="access-the-authoring-environment"></a><span data-ttu-id="ca892-147">Adgang til oprettelsesmiljøet</span><span class="sxs-lookup"><span data-stu-id="ca892-147">Access the authoring environment</span></span>

<span data-ttu-id="ca892-148">For at få adgang til oprettelsesmiljøet skal du gå til fanen **e-handel** på siden **Detailstyring**.</span><span class="sxs-lookup"><span data-stu-id="ca892-148">To access the authoring environment, go to the **e-Commerce** tab on the **Retail management** page.</span></span> <span data-ttu-id="ca892-149">Her finder du links til e-handelswebstedet og webstedets administrationsværktøj.</span><span class="sxs-lookup"><span data-stu-id="ca892-149">There, you will find links to your e-Commerce site and the site management tool.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="ca892-150">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="ca892-150">Additional resources</span></span>

[<span data-ttu-id="ca892-151">Oversigt over onlinebutik</span><span class="sxs-lookup"><span data-stu-id="ca892-151">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="ca892-152">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="ca892-152">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="ca892-153">Tilknytte et onlinewebsted til en kanal</span><span class="sxs-lookup"><span data-stu-id="ca892-153">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="ca892-154">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="ca892-154">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="ca892-155">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="ca892-155">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="ca892-156">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="ca892-156">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="ca892-157">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="ca892-157">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)
