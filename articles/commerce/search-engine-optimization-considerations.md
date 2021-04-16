---
title: Overvejelser om optimering af søgeprogram (SEO) for webstedet
description: I dette emne beskrives SEO-overvejelserne (søgemaskineoptimering) for dit websted fra udvikling til produktion.
author: psimolin
ms.date: 10/01/2019
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
ms.openlocfilehash: 52a10c754315bfef2a01c593f5fa5366e9054982
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5791793"
---
# <a name="search-engine-optimization-seo-considerations-for-your-site"></a><span data-ttu-id="4a4d4-103">Overvejelser om optimering af søgeprogram (SEO) for webstedet</span><span class="sxs-lookup"><span data-stu-id="4a4d4-103">Search engine optimization (SEO) considerations for your site</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="4a4d4-104">I dette emne beskrives SEO-overvejelserne (søgemaskineoptimering) for dit websted fra udvikling til produktion.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-104">This topic covers earch engine optimization (SEO) considerations for your site from development to production.</span></span>

## <a name="a-site-that-is-under-development"></a><span data-ttu-id="4a4d4-105">Et websted, der er under udvikling</span><span class="sxs-lookup"><span data-stu-id="4a4d4-105">A site that is under development</span></span>

<span data-ttu-id="4a4d4-106">Mens et websted er under udvikling, skal alle websider have metakoderne **NOINDEX** og **NOFOLLOW**, så søgemaskinerne ikke indekserer siderne og gemmer udviklingsversionerne af webstedet i cachen.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-106">While a site is under development, all site pages should have the **NOINDEX** and **NOFOLLOW** meta tags, so that search engines don't index the pages and store development versions of your site in their cache.</span></span> <span data-ttu-id="4a4d4-107">For at kunne foretage denne konfiguration skal du føje standardmetakodemodulet til webstedets sideskabelon.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-107">To do this configuration, you must add the default meta tags module to the site page template.</span></span> <span data-ttu-id="4a4d4-108">Standardegenskaberne for metakoder vil derefter være tilgængelige i området for SEO-egenskaber i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-108">The default meta tags properties will then be available in the SEO properties section in the page editor.</span></span> <span data-ttu-id="4a4d4-109">Du kan bruge disse egenskaber til at administrere metakoderne.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-109">You can use these properties to manage the meta tags.</span></span>

## <a name="soft-launch-of-a-site"></a><span data-ttu-id="4a4d4-110">Blød start af et websted</span><span class="sxs-lookup"><span data-stu-id="4a4d4-110">Soft launch of a site</span></span>

<span data-ttu-id="4a4d4-111">Under en "blød start" stilles et websted til rådighed for et begrænset publikum eller marked, før hele lanceringen finder sted.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-111">During a "soft launch," a website is made available to a limited audience or market before the full launch occurs.</span></span> <span data-ttu-id="4a4d4-112">Hvis du udfører en blød start af dit websted, skal du overveje at lade metakoderne for **NOINDEX** være på plads.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-112">If you do a soft launch of your website, you should consider leaving the **NOINDEX** meta tags in place.</span></span> <span data-ttu-id="4a4d4-113">På denne måde er du med til at sikre, at blød lancering forbliver begrænset til den mindre målgruppe, du ønsker at nå.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-113">In this way, you help guarantee that the soft launch remains restricted to the limited audience that you want to reach.</span></span>

## <a name="a-site-that-is-in-production"></a><span data-ttu-id="4a4d4-114">Et websted, der er i produktion</span><span class="sxs-lookup"><span data-stu-id="4a4d4-114">A site that is in production</span></span>

<span data-ttu-id="4a4d4-115">Når et websted er i produktion, skal du sørge for, at alle webstedets sider er korrekt mærket.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-115">When a site is in production, you should make sure that all site pages are correctly tagged.</span></span> <span data-ttu-id="4a4d4-116">Microsoft Dynamics 365 Commerce bruger de oplysninger, der er angivet for en side, til at gengive alle SEO-oplysninger på den pågældende side.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-116">Microsoft Dynamics 365 Commerce uses the information that is entered for a page to render all the SEO information on that page.</span></span> <span data-ttu-id="4a4d4-117">Følgende moduler indeholder denne funktionalitet: kategorisideoversigt, listesideoversigt og produktsideoversigt.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-117">The following modules provide this functionality: category page summary, list page summary, and product page summary.</span></span>

<span data-ttu-id="4a4d4-118">For at optimere indekseringen af søgemaskiner bruger gengivelsesstrukturen begge oplysninger fra de SEO-egenskaber, der er konfigureret i Dynamics 365 Commerce, og modulspecifikke oplysninger.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-118">To optimize search engine indexing, the rendering framework uses both information from the SEO properties that are configured in Dynamics 365 Commerce and module-specific information.</span></span> <span data-ttu-id="4a4d4-119">For et websted, der er i produktion, skal du sørge for, at filen robots.txt giver mulighed for indeksering af hele webstedet, og at det indeholder links til det publicerede dokument til oversigten over webstedet.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-119">For a site that is in production, you should make sure that the robots.txt file allows for indexing of your whole site, and that it contains links to your published site map document.</span></span> <span data-ttu-id="4a4d4-120">Du bør aktivere funktionaliteten for generering af webstedsoversigt under **Indstillinger for websted \> Oversigter over websted er aktiveret**.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-120">You should turn on the site map generation functionality at **Site Settings \> Site maps enabled**.</span></span>

### <a name="page-seo-settings-for-internal-preview-limited-audiences-and-all-audiences"></a><span data-ttu-id="4a4d4-121">Indstillinger for side-SEO til interne prøveversioner, begrænset målgruppe og alle målgrupper</span><span class="sxs-lookup"><span data-stu-id="4a4d4-121">Page SEO settings for internal preview, limited audiences, and all audiences</span></span>

<span data-ttu-id="4a4d4-122">Da Dynamics 365 Commerce understøtter "what you see is what you get" (WYSIWYG) i godkendte eksempelvisninger i den visuelle sidegenerator, kan forfattere forberede deres sideindhold uden at være bange for, at oplysningerne bliver synlige for besøgende på webstedet.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-122">Because Dynamics 365 Commerce supports "what you see is what you get" (WYSIWYG) authenticated previews in visual page builder, authors can prepare their page content without having to worry that the information will become visible to site visitors.</span></span> <span data-ttu-id="4a4d4-123">Hvis en side skal udgives, men eksponeringen skal være begrænset, skal den have metakoden **NOINDEX**, så den ikke vil blive indekseret af søgemaskiner.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-123">If a page must be published, but its exposure must be limited, it should have the **NOINDEX** meta tag, so that it won't be indexed by search engines.</span></span> <span data-ttu-id="4a4d4-124">Når siden er klar til alle målgrupper, skal alle grundlæggende SEO-metadata være til stede for at maksimere effektiviteten af søgeprogrammers indeksering.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-124">Then, when the page is ready for all audiences, all the basic SEO metadata should be present, to maximize the efficiency of search engine indexing.</span></span> <span data-ttu-id="4a4d4-125">Derudover bør metakoden **NOLIMIT** være fjernet.</span><span class="sxs-lookup"><span data-stu-id="4a4d4-125">Additionally, the **NOLIMIT** meta tag should be removed.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="4a4d4-126">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="4a4d4-126">Additional resources</span></span>

[<span data-ttu-id="4a4d4-127">Administrere e-handelsbrugere og -roller</span><span class="sxs-lookup"><span data-stu-id="4a4d4-127">Manage e-Commerce users and roles</span></span>](manage-ecommerce-users-roles.md)

[<span data-ttu-id="4a4d4-128">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="4a4d4-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="4a4d4-129">Administrere sikkerhedspolitik for indhold (CSP)</span><span class="sxs-lookup"><span data-stu-id="4a4d4-129">Manage Content Security Policy (CSP)</span></span>](manage-csp.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]