---
title: Tilvælge brug af vurderinger og anmeldelser
description: I dette emne beskrives, hvordan du kan tilvælge at bruge vurderinger og anmeldelser på dit Microsoft Dynamics 365 Commerce-websted.
author: gvrmohanreddy
manager: annbe
ms.date: 10/01/2019
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
ms.author: gmohanv
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 10e3c33af232fa46df09a103b2e73eae09a909eb
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697974"
---
# <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="dd755-103">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="dd755-103">Opt in to use ratings and reviews</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="dd755-104">I dette emne beskrives, hvordan du kan tilvælge at bruge vurderinger og anmeldelser på dit Microsoft Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="dd755-104">This topic explains how to opt in to use ratings and reviews on your Microsoft Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="dd755-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="dd755-105">Overview</span></span>

<span data-ttu-id="dd755-106">Vurderings- og anmeldelsesløsningen er en omnikanalløsning, du kan stille til rådighed i Dynamics 365 Commerce ved hjælp af Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="dd755-106">The ratings and reviews solution is an omnichannel solution that you can make available in Dynamics 365 Commerce by using Microsoft Dynamics Lifecycle Services (LCS).</span></span> <span data-ttu-id="dd755-107">LCS er en administrationsportal, som detailhandlere kan bruger til at styre deres miljøer fra klargøring til nedlukning.</span><span class="sxs-lookup"><span data-stu-id="dd755-107">LCS is an administration portal that retailers use to manage their environments from provisioning to decommissioning.</span></span>

<span data-ttu-id="dd755-108">Hvis du vil bruge vurderings- og anmeldelsesløsningerne på Commerce-webstedet, skal du først tilvælge det.</span><span class="sxs-lookup"><span data-stu-id="dd755-108">If you want to use the ratings and reviews solution on your Commerce website, you must first opt in.</span></span>

## <a name="opt-in-to-use-ratings-and-reviews"></a><span data-ttu-id="dd755-109">Tilvælge brug af vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="dd755-109">Opt in to use ratings and reviews</span></span>

<span data-ttu-id="dd755-110">Du kan tilvælge at bruge vurderinger og anmeldelser på dit websted ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="dd755-110">To opt in to use ratings and reviews on your site, follow these steps.</span></span>

1. <span data-ttu-id="dd755-111">Følg trinnene i [Implementere et nyt websted for e-handel](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="dd755-111">Follow the steps in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span>
1. <span data-ttu-id="dd755-112">Mens du stadig er i LCS, skal du gå til **Konfiguration af Retail-installation \> Andre indstillinger**.</span><span class="sxs-lookup"><span data-stu-id="dd755-112">While you're still in LCS, go to **Retail deployment setup \> Other settings**.</span></span>
1. <span data-ttu-id="dd755-113">Vælg **Ja** i indstillingen **Aktivér vurderinger og anmeldelser**.</span><span class="sxs-lookup"><span data-stu-id="dd755-113">Set the **Enable ratings and reviews service** option to **Yes**.</span></span>
1. <span data-ttu-id="dd755-114">I den **AAD-sikkerhedsgruppen for redaktør af vurderinger og anmeldelser (sikkerhedsgruppens objekt-id)** skal du angive id'et for den Microsoft Azure Active Directory-sikkerhedsgruppe (Azure AD), der omfatter vurderings- og anmeldelsesredaktørerne.</span><span class="sxs-lookup"><span data-stu-id="dd755-114">In the **AAD security group for ratings and review moderator (security group object id)** field, enter the ID of the Microsoft Azure Active Directory (Azure AD) security group that includes the ratings and reviews moderators.</span></span>

    ![Tilvælge brug af vurderinger og anmeldelser](media/LCS_RnR_Preference.png)

1. <span data-ttu-id="dd755-116">Fuldfør processen til e-handelsinitialisering.</span><span class="sxs-lookup"><span data-stu-id="dd755-116">Complete the e-Commerce initialization process.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="dd755-117">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="dd755-117">Additional resources</span></span>

[<span data-ttu-id="dd755-118">Oversigt over vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="dd755-118">Ratings and reviews overview</span></span>](ratings-reviews-overview.md)

[<span data-ttu-id="dd755-119">Administrere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="dd755-119">Manage ratings and reviews</span></span>](manage-reviews.md)

[<span data-ttu-id="dd755-120">Konfigurere vurderinger og anmeldelser</span><span class="sxs-lookup"><span data-stu-id="dd755-120">Configure ratings and reviews</span></span>](configure-ratings-reviews.md)

[<span data-ttu-id="dd755-121">Synkronisere produktvurderinger i Dynamics 365 Retail</span><span class="sxs-lookup"><span data-stu-id="dd755-121">Sync product ratings in Dynamics 365 Retail</span></span>](sync-product-ratings.md)
