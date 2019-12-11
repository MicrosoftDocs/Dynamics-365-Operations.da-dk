---
title: Oprette et websted for e-handel
description: I dette emne beskrives de opgaver, der er knyttet til oprettelsen af et nyt e-handelswebsted i Dynamics 365 Commerce.
author: bicyclingfool
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fd87a51b73deae64867b0420c00db9fce7c79336
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697123"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="74325-103">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="74325-103">Create an e-Commerce site</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="74325-104">I dette emne beskrives de opgaver, der er knyttet til oprettelsen af et nyt e-handelswebsted i Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="74325-104">This topic describes the tasks that are associated with the creation of a new e-Commerce site in Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="74325-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="74325-105">Overview</span></span>

<span data-ttu-id="74325-106">Før du kan udvikle dit e-handelswebsted, skal du først oprette et nyt websted i webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="74325-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="74325-107">Før du kan oprette en nyt websted, skal der oprettes mindst én onlinebutik i Dynamics 365 Retail.</span><span class="sxs-lookup"><span data-stu-id="74325-107">Before you can create a new site, at least one online store must be created in Dynamics 365 Retail.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="74325-108">Konfigurere dit websted</span><span class="sxs-lookup"><span data-stu-id="74325-108">Set up your site</span></span>

<span data-ttu-id="74325-109">Du kan konfigurere dit websted ved at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="74325-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="74325-110">I Microsoft Lifecycle Services (LCS) skal du vælge linket til webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="74325-110">In Microsoft Lifecycle Services (LCS), select the link for the site authoring environment.</span></span> 
1. <span data-ttu-id="74325-111">Vælg **Nyt websted** på startsiden for webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="74325-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="74325-112">I dialogboksen **Nyt websted** skal du angive følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="74325-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="74325-113">Felt</span><span class="sxs-lookup"><span data-stu-id="74325-113">Field</span></span>                               | <span data-ttu-id="74325-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="74325-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="74325-115">Navn på websted</span><span class="sxs-lookup"><span data-stu-id="74325-115">Site name</span></span>                           | <span data-ttu-id="74325-116">Angiv det visningsnavn, der skal bruges til dit websted i webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="74325-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="74325-117">Dette navn er kun synligt i oprettelsesmiljøet og vil ikke blive vist for kunderne.</span><span class="sxs-lookup"><span data-stu-id="74325-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="74325-118">Sikkerhedsgruppe for webstedsadministrator</span><span class="sxs-lookup"><span data-stu-id="74325-118">Site administrator's security group</span></span> | <span data-ttu-id="74325-119">Angiv den Microsoft Azure Active Directory-sikkerhedsgruppe (Azure AD), der administrerer de brugere, der har rollen som webstedsadministrator på dette websted.</span><span class="sxs-lookup"><span data-stu-id="74325-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="74325-120">Standardkanal (driftsenhedsnummer)</span><span class="sxs-lookup"><span data-stu-id="74325-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="74325-121">Vælg den onlinebutik, som dette websted skal fungere som webstorefront for.</span><span class="sxs-lookup"><span data-stu-id="74325-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="74325-122">Hvis du ønsker, at dit e-handelswebsted skal understøtte flere onlinebutikker, skal du knytte butikkerne til webstedet i **Indstillinger for websted**, efter at webstedet er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="74325-122">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="74325-123">Standardsprog</span><span class="sxs-lookup"><span data-stu-id="74325-123">Default language</span></span>                            | <span data-ttu-id="74325-124">Angiv standardsproget for denne onlinebutik og dette marked.</span><span class="sxs-lookup"><span data-stu-id="74325-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="74325-125">En onlinebutik kan understøtte flere sprog.</span><span class="sxs-lookup"><span data-stu-id="74325-125">An online store can support multiple languages.</span></span> <span data-ttu-id="74325-126">Hvis du vil understøtte flere sprog for denne onlinebutik eller en anden onlinebutik, kan du konfigurere denne understøttelse i **Indstillinger for websted**, når webstedet er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="74325-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="74325-127">Domæne</span><span class="sxs-lookup"><span data-stu-id="74325-127">Domain</span></span>                              | <span data-ttu-id="74325-128">Vælg et domænenavn, der kan fungere som domæne for denne onlinebutik.</span><span class="sxs-lookup"><span data-stu-id="74325-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="74325-129">Hvis du ikke har konfigureret nogen domæner i LCS, kan du lade dette felt være tomt.</span><span class="sxs-lookup"><span data-stu-id="74325-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="74325-130">Når domænet er konfigureret i LCS, skal du føje det til din onlinebutik i **Indstillinger for websted**.</span><span class="sxs-lookup"><span data-stu-id="74325-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="74325-131">Sti</span><span class="sxs-lookup"><span data-stu-id="74325-131">Path</span></span>                              | <span data-ttu-id="74325-132">Når webstedet understøtter mere end ét sprog for et bestemt domænenavn, skal du bruge stifeltet til at oprette en entydig URL-adresse til et websted for det pågældende domæne og sprogkombinationen.</span><span class="sxs-lookup"><span data-stu-id="74325-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="74325-133">Hvis det sprog, du har angivet i feltet **Standardsprog**, er det eneste sprog, du vil understøtte for dette domæne, eller som fortsat er standardsproget, når du har lokaliseret dit websted til flere sprog, anbefales det, at du lader dette felt stå tomt.</span><span class="sxs-lookup"><span data-stu-id="74325-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="74325-134">Når webstedet er oprettet, kan du kontrollere, om det er knyttet til din onlinebutik, ved at vælge fanen **Produkter**. Du bør kunne se det produktsortiment, der er tildelt til onlinebutikken.</span><span class="sxs-lookup"><span data-stu-id="74325-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="74325-135">Du kan også bruge rullemenuen øverst til venstre på siden til at få adgang til de allokerede produkter efter kategori.</span><span class="sxs-lookup"><span data-stu-id="74325-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="74325-136">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="74325-136">Additional resources</span></span>

[<span data-ttu-id="74325-137">Oversigt over onlinebutik</span><span class="sxs-lookup"><span data-stu-id="74325-137">Online store overview</span></span>](online-store-overview.md)

[<span data-ttu-id="74325-138">Implementere et nyt websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="74325-138">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="74325-139">Tilknytte et onlinewebsted til en kanal</span><span class="sxs-lookup"><span data-stu-id="74325-139">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="74325-140">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="74325-140">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="74325-141">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="74325-141">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="74325-142">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="74325-142">Enable location-based store detection</span></span>](enable-store-detection.md)

[<span data-ttu-id="74325-143">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="74325-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="74325-144">Oversigt over startside for oprettelse</span><span class="sxs-lookup"><span data-stu-id="74325-144">Authoring home page overview</span></span>](authoring-home-overview.md)

[<span data-ttu-id="74325-145">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="74325-145">Add a new site page</span></span>](add-new-page.md)
