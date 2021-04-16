---
title: Tilvælge brug af vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du kan tilvælge at bruge vurderinger og anmeldelser på dit Microsoft Dynamics 365 Commerce-websted.
author: gvrmohanreddy
ms.date: 01/30/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 9e3f2a17e182c0e3efc8b90380eff74f350c3278
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5804643"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="bd8c4-103">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="bd8c4-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="bd8c4-104">I dette emne beskrives, hvordan du kan tilvælge at bruge vurderinger og anmeldelser på dit Microsoft Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="bd8c4-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="bd8c4-105">Overblik</span><span class="sxs-lookup"><span data-stu-id="bd8c4-105">Overview</span></span>

<span data-ttu-id="bd8c4-106">Vurderings- og anmeldelsesløsningen er en omnikanalløsning, du kan stille til rådighed i Dynamics 365 Commerce ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="bd8c4-106">The ratings and reviews solution is an omni-channel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="bd8c4-107">LCS er en administrationsportal, som detailhandlere kan bruger til at styre deres miljøer fra klargøring til nedlukning.</span><span class="sxs-lookup"><span data-stu-id="bd8c4-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="bd8c4-108">Hvis du vil bruge vurderings- og anmeldelsesløsningen på Commerce-webstedet, skal du tilmelde dig vurderinger og anmeldelser under installationen af dit e-handels-websted på Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="bd8c4-108">If you want to use the ratings and reviews solution on your Commerce website, you must opt in for ratings and reviews during deployment of your e-Commerce site on Dynamics 365 Commerce.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="bd8c4-109">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="bd8c4-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="bd8c4-110">Du kan tilvælge at bruge vurderinger og anmeldelser på dit websted ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="bd8c4-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="bd8c4-111">Følg trinnene i [Implementere et nyt websted for e-handel](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="bd8c4-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="bd8c4-112">Mens du stadig er i LCS, skal du gå til **Konfiguration af Retail-installation \> Andre indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="bd8c4-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="bd8c4-113">Vælg **Ja** i indstillingen **Aktivér vurderinger og anmeldelser**.</span><span class="sxs-lookup"><span data-stu-id="bd8c4-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="bd8c4-114">I den **AAD-sikkerhedsgruppen for redaktør af vurderinger og anmeldelser (sikkerhedsgruppens objekt-id)** skal du angive id'et for den Microsoft Azure Active Directory-sikkerhedsgruppe (Azure AD), der omfatter vurderings- og anmeldelsesredaktørerne.</span><span class="sxs-lookup"><span data-stu-id="bd8c4-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Tilvælge brug af vurderinger og anmeldelser](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="bd8c4-116">Fuldfør processen til e-handelsinitialisering.</span><span class="sxs-lookup"><span data-stu-id="bd8c4-116">Complete the e-Commerce initialization process.</span></span>

> [!NOTE] 
> <span data-ttu-id="bd8c4-117">Hvis du er eksisterende Dynamics 365 Commerce-kunde, der allerede har implementeret et e-handels-websted uden at have tilmeldt dig vurderinger og anmeldelser og nu vil bruge vurderinger og anmeldelser fra Dynamics 365 Commerce-pakken, skal du sende en serviceanmodning.</span><span class="sxs-lookup"><span data-stu-id="bd8c4-117">If you are an existing Dynamics 365 Commerce customer who has already deployed an e-Commerce site without having opted in for ratings and reviews and now want to use ratings and reviews from the Dynamics 365 Commerce package, please submit a service request.</span></span> <span data-ttu-id="bd8c4-118">Oplysninger om, hvordan du sender en serviceanmodning, finder du under [Proces for afsendelse af serviceanmodninger](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span><span class="sxs-lookup"><span data-stu-id="bd8c4-118">For information about how to submit a service request, see [Submit service requests process](../fin-ops-core/dev-itpro/lifecycle-services/submit-request-dynamics-service-engineering-team.md?toc=/dynamics365/commerce/toc.json).</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="bd8c4-119">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="bd8c4-119">Additional resources</span></span>

[<span data-ttu-id="bd8c4-120">Oversigt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="bd8c4-120">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="bd8c4-121">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="bd8c4-121">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="bd8c4-122">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="bd8c4-122">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="bd8c4-123">Synkronisere produktvurderinger i Dynamics 365 Commerce</span><span class="sxs-lookup"><span data-stu-id="bd8c4-123">Sync product ratings in Dynamics 365 Commerce</span></span>](sync-product-ratings.md)




[!INCLUDE[footer-include](../includes/footer-banner.md)]