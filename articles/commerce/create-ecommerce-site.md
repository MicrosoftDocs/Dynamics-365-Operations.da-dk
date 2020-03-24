---
title: Oprette et websted for e-handel
description: I dette emne beskrives de trin og oplysninger, der er nødvendige for at oprette et nyt e-handels-websted i Dynamics 365 Commerce-webstedsgeneratoren.
author: bicyclingfool
manager: AnnBe
ms.date: 03/02/2020
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
ms.openlocfilehash: 7177bae911dfa91a645b40581bf23b3ed76562a3
ms.sourcegitcommit: 567132f4e4f7a1d76dccf762068209a42c788b52
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/03/2020
ms.locfileid: "3096768"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="36f13-103">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="36f13-103">Create an e-Commerce site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="36f13-104">I dette emne beskrives de trin og oplysninger, der er nødvendige for at oprette et nyt e-handels-websted i Dynamics 365 Commerce-webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="36f13-104">This topic describes the steps and information required to create a new e-Commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="36f13-105">Før du kan gå i gang med at udvikle dit e-handelswebsted, skal du først oprette et nyt websted i webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="36f13-105">Before you can start developing your e-Commerce site, you must first establish a new site in site builder.</span></span> 


<span data-ttu-id="36f13-106">Før du kan udvikle dit e-handelswebsted, skal du først oprette et nyt websted i webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="36f13-106">To start to develop your e-Commerce site, you must first establish a new site in the site authoring environment.</span></span> <span data-ttu-id="36f13-107">Før du kan oprette et nyt websted, skal der oprettes mindst én onlinebutik i Commerce.</span><span class="sxs-lookup"><span data-stu-id="36f13-107">Before you can create a new site, at least one online store must be created in Commerce.</span></span> 


## <a name="set-up-your-site"></a><span data-ttu-id="36f13-108">Konfigurere dit websted</span><span class="sxs-lookup"><span data-stu-id="36f13-108">Set up your site</span></span>

<span data-ttu-id="36f13-109">Du kan konfigurere dit websted ved at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="36f13-109">To set up your site, do the following.</span></span>

1. <span data-ttu-id="36f13-110">Åbn webstedsgeneratormiljøet.</span><span class="sxs-lookup"><span data-stu-id="36f13-110">Open the site builder environment.</span></span> <span data-ttu-id="36f13-111">Du kan finde et link til webstedsgeneratoren i Microsoft Lifecycle Services (LCS) på siden med miljøfunktioner til Commerce.</span><span class="sxs-lookup"><span data-stu-id="36f13-111">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="36f13-112">Vælg **Nyt websted** på startsiden for webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="36f13-112">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="36f13-113">I dialogboksen **Nyt websted** skal du angive følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="36f13-113">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="36f13-114">Felt</span><span class="sxs-lookup"><span data-stu-id="36f13-114">Field</span></span>                               | <span data-ttu-id="36f13-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="36f13-115">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="36f13-116">Navn på websted</span><span class="sxs-lookup"><span data-stu-id="36f13-116">Site name</span></span>                           | <span data-ttu-id="36f13-117">Angiv det visningsnavn, der skal bruges til dit websted i webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="36f13-117">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="36f13-118">Dette navn er kun synligt i oprettelsesmiljøet og vil ikke blive vist for kunderne.</span><span class="sxs-lookup"><span data-stu-id="36f13-118">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="36f13-119">Sikkerhedsgruppe for webstedsadministrator</span><span class="sxs-lookup"><span data-stu-id="36f13-119">Site administrator's security group</span></span> | <span data-ttu-id="36f13-120">Angiv den Microsoft Azure Active Directory-sikkerhedsgruppe (Azure AD), der administrerer de brugere, der har rollen som webstedsadministrator på dette websted.</span><span class="sxs-lookup"><span data-stu-id="36f13-120">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="36f13-121">Standardkanal (driftsenhedsnummer)</span><span class="sxs-lookup"><span data-stu-id="36f13-121">Default channel (operating unit number)</span></span> | <span data-ttu-id="36f13-122">Vælg den onlinebutik, som dette websted skal fungere som webstorefront for.</span><span class="sxs-lookup"><span data-stu-id="36f13-122">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="36f13-123">Hvis du ønsker, at dit e-handelswebsted skal understøtte flere onlinebutikker, skal du knytte butikkerne til webstedet i **Indstillinger for websted**, efter at webstedet er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="36f13-123">If you want your e-Commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="36f13-124">Standardsprog</span><span class="sxs-lookup"><span data-stu-id="36f13-124">Default language</span></span>                            | <span data-ttu-id="36f13-125">Angiv standardsproget for denne onlinebutik og dette marked.</span><span class="sxs-lookup"><span data-stu-id="36f13-125">Specify the default language for this online store and market.</span></span> <span data-ttu-id="36f13-126">En onlinebutik kan understøtte flere sprog.</span><span class="sxs-lookup"><span data-stu-id="36f13-126">An online store can support multiple languages.</span></span> <span data-ttu-id="36f13-127">Hvis du vil understøtte flere sprog for denne onlinebutik eller en anden onlinebutik, kan du konfigurere denne understøttelse i **Indstillinger for websted**, når webstedet er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="36f13-127">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="36f13-128">Domæne</span><span class="sxs-lookup"><span data-stu-id="36f13-128">Domain</span></span>                              | <span data-ttu-id="36f13-129">Vælg et domænenavn, der kan fungere som domæne for denne onlinebutik.</span><span class="sxs-lookup"><span data-stu-id="36f13-129">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="36f13-130">Hvis du ikke har konfigureret nogen domæner i LCS, kan du lade dette felt være tomt.</span><span class="sxs-lookup"><span data-stu-id="36f13-130">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="36f13-131">Når domænet er konfigureret i LCS, skal du føje det til din onlinebutik i **Indstillinger for websted**.</span><span class="sxs-lookup"><span data-stu-id="36f13-131">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="36f13-132">Sti</span><span class="sxs-lookup"><span data-stu-id="36f13-132">Path</span></span>                              | <span data-ttu-id="36f13-133">Når webstedet understøtter mere end ét sprog for et bestemt domænenavn, skal du bruge stifeltet til at oprette en entydig URL-adresse til et websted for det pågældende domæne og sprogkombinationen.</span><span class="sxs-lookup"><span data-stu-id="36f13-133">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="36f13-134">Hvis det sprog, du har angivet i feltet **Standardsprog**, er det eneste sprog, du vil understøtte for dette domæne, eller som fortsat er standardsproget, når du har lokaliseret dit websted til flere sprog, anbefales det, at du lader dette felt stå tomt.</span><span class="sxs-lookup"><span data-stu-id="36f13-134">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="36f13-135">Når webstedet er oprettet, kan du kontrollere, om det er knyttet til din onlinebutik, ved at vælge fanen **Produkter**. Du bør kunne se det produktsortiment, der er tildelt til onlinebutikken.</span><span class="sxs-lookup"><span data-stu-id="36f13-135">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="36f13-136">Du kan også bruge rullemenuen øverst til venstre på siden til at få adgang til de allokerede produkter efter kategori.</span><span class="sxs-lookup"><span data-stu-id="36f13-136">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="36f13-137">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="36f13-137">Additional resources</span></span>

[<span data-ttu-id="36f13-138">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="36f13-138">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="36f13-139">Implementere et nyt websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="36f13-139">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="36f13-140">Konfigurere en onlinebutikskanal</span><span class="sxs-lookup"><span data-stu-id="36f13-140">Set up an online store channel</span></span>](online-stores.md)

[<span data-ttu-id="36f13-141">Tilknytte et onlinewebsted til en kanal</span><span class="sxs-lookup"><span data-stu-id="36f13-141">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="36f13-142">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="36f13-142">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="36f13-143">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="36f13-143">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="36f13-144">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="36f13-144">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="36f13-145">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="36f13-145">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="36f13-146">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="36f13-146">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="36f13-147">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="36f13-147">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="36f13-148">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="36f13-148">Enable location-based store detection</span></span>](enable-store-detection.md)
