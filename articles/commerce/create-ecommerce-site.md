---
title: Oprette et websted for e-handel
description: I dette emne beskrives de trin og oplysninger, der er nødvendige for at oprette et nyt e-handels-websted i Dynamics 365 Commerce-webstedsgeneratoren.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: stuharg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 465154ef7209547481c8598d5eaefb434359b1fd
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5207964"
---
# <a name="create-an-e-commerce-site"></a><span data-ttu-id="84191-103">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="84191-103">Create an e-commerce site</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="84191-104">I dette emne beskrives de trin og oplysninger, der er nødvendige for at oprette et nyt e-handels-websted i Dynamics 365 Commerce-webstedsgeneratoren.</span><span class="sxs-lookup"><span data-stu-id="84191-104">This topic describes the steps and information required to create a new e-commerce site in Dynamics 365 Commerce site builder.</span></span>

<span data-ttu-id="84191-105">Når du licenserer Dynamics 365 Commerce-funktionerne til e-handel, vil webstedsgeneratoren blive klargjort til et startsted, som du kan bruge som udgangspunkt for dit eget websted.</span><span class="sxs-lookup"><span data-stu-id="84191-105">When you license the Dynamics 365 Commerce capabilities, site builder will be provisioned with a starter site that you can use as a basis for your own site.</span></span> <span data-ttu-id="84191-106">Men hvis du vil starte fra bunden, eller hvis du vil oprette endnu et websted, skal du oprette et nyt websted i området til oprettelse af websted.</span><span class="sxs-lookup"><span data-stu-id="84191-106">However, if you want to start from scratch or if you want to establish a second site, you will need to establish a new site in the site authoring environment.</span></span> 

## <a name="set-up-your-site"></a><span data-ttu-id="84191-107">Konfigurere dit websted</span><span class="sxs-lookup"><span data-stu-id="84191-107">Set up your site</span></span>

<span data-ttu-id="84191-108">Du kan konfigurere dit websted ved at gøre følgende:</span><span class="sxs-lookup"><span data-stu-id="84191-108">To set up your site, do the following.</span></span>

1. <span data-ttu-id="84191-109">Åbn webstedsgeneratormiljøet.</span><span class="sxs-lookup"><span data-stu-id="84191-109">Open the site builder environment.</span></span> <span data-ttu-id="84191-110">Du kan finde et link til webstedsgeneratoren i Microsoft Lifecycle Services (LCS) på siden med miljøfunktioner til Commerce.</span><span class="sxs-lookup"><span data-stu-id="84191-110">You can find a link to site builder in Microsoft Lifecycle Services (LCS) in the environment features page for Commerce.</span></span>
1. <span data-ttu-id="84191-111">Vælg **Nyt websted** på startsiden for webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="84191-111">On the home page for the site authoring environment, select **New site**.</span></span>
1. <span data-ttu-id="84191-112">I dialogboksen **Nyt websted** skal du angive følgende oplysninger.</span><span class="sxs-lookup"><span data-stu-id="84191-112">In the **New site** dialog box, provide the following information.</span></span>

| <span data-ttu-id="84191-113">Felt</span><span class="sxs-lookup"><span data-stu-id="84191-113">Field</span></span>                               | <span data-ttu-id="84191-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="84191-114">Description</span></span> |
|-------------------------------------|-------------|
| <span data-ttu-id="84191-115">Navn på websted</span><span class="sxs-lookup"><span data-stu-id="84191-115">Site name</span></span>                           | <span data-ttu-id="84191-116">Angiv det visningsnavn, der skal bruges til dit websted i webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="84191-116">Enter the display name that should be used for your site in the site authoring environment.</span></span> <span data-ttu-id="84191-117">Dette navn er kun synligt i oprettelsesmiljøet og vil ikke blive vist for kunderne.</span><span class="sxs-lookup"><span data-stu-id="84191-117">This name is visible only in the authoring environment and will not be shown to customers.</span></span> |
| <span data-ttu-id="84191-118">Sikkerhedsgruppe for webstedsadministrator</span><span class="sxs-lookup"><span data-stu-id="84191-118">Site administrator's security group</span></span> | <span data-ttu-id="84191-119">Angiv den Microsoft Azure Active Directory-sikkerhedsgruppe (Azure AD), der administrerer de brugere, der har rollen som webstedsadministrator på dette websted.</span><span class="sxs-lookup"><span data-stu-id="84191-119">Specify the Microsoft Azure Active Directory (Azure AD) security group that manages users who have the site administrator role in this site.</span></span> |
| <span data-ttu-id="84191-120">Standardkanal (driftsenhedsnummer)</span><span class="sxs-lookup"><span data-stu-id="84191-120">Default channel (operating unit number)</span></span> | <span data-ttu-id="84191-121">Vælg den onlinebutik, som dette websted skal fungere som webstorefront for.</span><span class="sxs-lookup"><span data-stu-id="84191-121">Select the online store that this site will serve as the web storefront for.</span></span> <span data-ttu-id="84191-122">Hvis du ønsker, at dit e-handelswebsted skal understøtte flere onlinebutikker, skal du knytte butikkerne til webstedet i **Indstillinger for websted**, efter at webstedet er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="84191-122">If you want your e-commerce site to support multiple online stores, you must associate the stores with your site in **Site settings** after the site is set up.</span></span> |
| <span data-ttu-id="84191-123">Standardsprog</span><span class="sxs-lookup"><span data-stu-id="84191-123">Default language</span></span>                            | <span data-ttu-id="84191-124">Angiv standardsproget for denne onlinebutik og dette marked.</span><span class="sxs-lookup"><span data-stu-id="84191-124">Specify the default language for this online store and market.</span></span> <span data-ttu-id="84191-125">En onlinebutik kan understøtte flere sprog.</span><span class="sxs-lookup"><span data-stu-id="84191-125">An online store can support multiple languages.</span></span> <span data-ttu-id="84191-126">Hvis du vil understøtte flere sprog for denne onlinebutik eller en anden onlinebutik, kan du konfigurere denne understøttelse i **Indstillinger for websted**, når webstedet er konfigureret.</span><span class="sxs-lookup"><span data-stu-id="84191-126">If you want to support multiple languages for this online store or another online store, you can configure that support in **Site settings** after the site is set up.</span></span>  |
| <span data-ttu-id="84191-127">Domæne</span><span class="sxs-lookup"><span data-stu-id="84191-127">Domain</span></span>                              | <span data-ttu-id="84191-128">Vælg et domænenavn, der kan fungere som domæne for denne onlinebutik.</span><span class="sxs-lookup"><span data-stu-id="84191-128">Select a domain name that will serve as the domain for this online store.</span></span> <span data-ttu-id="84191-129">Hvis du ikke har konfigureret nogen domæner i LCS, kan du lade dette felt være tomt.</span><span class="sxs-lookup"><span data-stu-id="84191-129">If you haven't configured any domains in LCS, you can leave this field blank.</span></span> <span data-ttu-id="84191-130">Når domænet er konfigureret i LCS, skal du føje det til din onlinebutik i **Indstillinger for websted**.</span><span class="sxs-lookup"><span data-stu-id="84191-130">After your domain is configured in LCS, you must add it to your online store in **Site settings**.</span></span>  |
| <span data-ttu-id="84191-131">Sti</span><span class="sxs-lookup"><span data-stu-id="84191-131">Path</span></span>                              | <span data-ttu-id="84191-132">Når webstedet understøtter mere end ét sprog for et bestemt domænenavn, skal du bruge stifeltet til at oprette en entydig URL-adresse til et websted for det pågældende domæne og sprogkombinationen.</span><span class="sxs-lookup"><span data-stu-id="84191-132">When your site supports more than one language for a given domain name, use the path field to create a unique site URL for that domain and language combination.</span></span> <span data-ttu-id="84191-133">Hvis det sprog, du har angivet i feltet **Standardsprog**, er det eneste sprog, du vil understøtte for dette domæne, eller som fortsat er standardsproget, når du har lokaliseret dit websted til flere sprog, anbefales det, at du lader dette felt stå tomt.</span><span class="sxs-lookup"><span data-stu-id="84191-133">If the language you specified in the **Default language** field is the only language you will support for this domain, or will continue to be the default language after you have localized your site into additional languages, we recommend that you leave this field empty.</span></span> |


<span data-ttu-id="84191-134">Når webstedet er oprettet, kan du kontrollere, om det er knyttet til din onlinebutik, ved at vælge fanen **Produkter**. Du bør kunne se det produktsortiment, der er tildelt til onlinebutikken.</span><span class="sxs-lookup"><span data-stu-id="84191-134">After your site is created, you can verify that it is associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="84191-135">Du kan også bruge rullemenuen øverst til venstre på siden til at få adgang til de allokerede produkter efter kategori.</span><span class="sxs-lookup"><span data-stu-id="84191-135">You can also use the drop-down menu in the upper left of the page to access the allocated products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="84191-136">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="84191-136">Additional resources</span></span>

[<span data-ttu-id="84191-137">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="84191-137">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="84191-138">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="84191-138">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="84191-139">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="84191-139">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="84191-140">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="84191-140">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="84191-141">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="84191-141">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="84191-142">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="84191-142">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="84191-143">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="84191-143">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="84191-144">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="84191-144">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="84191-145">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="84191-145">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="84191-146">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="84191-146">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]