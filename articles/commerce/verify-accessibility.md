---
title: Bekræft tilgængelighed af sideindhold
description: Dette emne beskriver, hvordan du kontrollerer tilgængeligheden af sideindhold i Microsoft Dynamics 365 Commerce.
author: arotkin
manager: annbe
ms.date: 01/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.search.region: Global
ms.search.industry: retail
ms.author: arotkin
ms.search.validFrom: 2019-12-19
ms.dyn365.ops.version: Release 10.0.8
ms.openlocfilehash: 8e35b0f71ff41bade266fb177e4500c7d124ed1f
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3002653"
---
# <a name="verify-page-content-accessibility"></a><span data-ttu-id="d213c-103">Bekræft tilgængelighed af sideindhold</span><span class="sxs-lookup"><span data-stu-id="d213c-103">Verify page content accessibility</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="d213c-104">Dette emne beskriver, hvordan du kontrollerer tilgængeligheden af sideindhold i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d213c-104">This topic describes how to verify the accessibility of page content in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d213c-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="d213c-105">Overview</span></span>

<span data-ttu-id="d213c-106">Når du er færdig med at ændre en side, skal du sørge for, at indholdet er tilgængeligt for alle på internettet.</span><span class="sxs-lookup"><span data-stu-id="d213c-106">When you've finished changing a page, you should make sure that the content is accessible to everyone on the web.</span></span> <span data-ttu-id="d213c-107">I Commerce-oprettelsesværktøjerne kan du nemt kontrollere tilgængeligheden af sideindhold ved hjælp af den integrerede [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-tjeneste.</span><span class="sxs-lookup"><span data-stu-id="d213c-107">In the Commerce authoring tools, you can easily verify the accessibility of page content by using the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service.</span></span> <span data-ttu-id="d213c-108">Denne tjeneste bekræfter dit sideindhold i forhold til de seneste retningslinjer for hjælp til handicappede [World Wide Web Consortium (W3C)](https://www.w3.org/standards/webdesign/accessibility).</span><span class="sxs-lookup"><span data-stu-id="d213c-108">This service verifies your page content against the latest [World Wide Web Consortium (W3C) accessibility](https://www.w3.org/standards/webdesign/accessibility) guidelines.</span></span>

<span data-ttu-id="d213c-109">Integrationen af [Microsoft Accessibility Insights](https://accessibilityinsights.io/) skal være aktiveret på lejer- eller webstedsniveau, før du kan bruge den.</span><span class="sxs-lookup"><span data-stu-id="d213c-109">The [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration must be turned on at the tenant or site level before you can use it.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-all-the-sites-in-your-tenant"></a><span data-ttu-id="d213c-110">Aktivér Microsoft Accessibility Insights for alle webstederne i din lejer</span><span class="sxs-lookup"><span data-stu-id="d213c-110">Turn on Microsoft Accessibility Insights for all the sites in your tenant</span></span>

<span data-ttu-id="d213c-111">Hvis du vil aktivere integrationen af [Microsoft Accessibility Insights](https://accessibilityinsights.io/) for alle Commerce-websteder i din lejer, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="d213c-111">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for all the Commerce sites in your tenant, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="d213c-112">For at tilgå lejerindstillinger skal du være logget på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="d213c-112">To access tenant settings, you must be signed in to Commerce as a system admin.</span></span>

1. <span data-ttu-id="d213c-113">Log ind på Commerce som systemadministrator.</span><span class="sxs-lookup"><span data-stu-id="d213c-113">Sign in to Commerce as a system admin.</span></span>
1. <span data-ttu-id="d213c-114">I venstre navigationsrude skal du vælge **Lejerindstillinger** (ud for tandhjulssymbolet) for at udvide det.</span><span class="sxs-lookup"><span data-stu-id="d213c-114">In the left navigation pane, select **Tenant Settings** (next to the gear symbol) to expand it.</span></span>
1. <span data-ttu-id="d213c-115">Under **Lejerindstillinger** skal du vælge **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="d213c-115">Under **Tenant Settings**, select **Features**.</span></span>
1. <span data-ttu-id="d213c-116">Angiv indstillingen **Tilgængelighedskontrol** til **Til**.</span><span class="sxs-lookup"><span data-stu-id="d213c-116">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="turn-on-microsoft-accessibility-insights-for-a-single-site"></a><span data-ttu-id="d213c-117">Aktivér Microsoft Accessibility Insights for et enkelt websted</span><span class="sxs-lookup"><span data-stu-id="d213c-117">Turn on Microsoft Accessibility Insights for a single site</span></span>

<span data-ttu-id="d213c-118">Hvis du vil aktivere integrationen af [Microsoft Accessibility Insights](https://accessibilityinsights.io/) for et enkelt Commerce-websted, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="d213c-118">To turn on the [Microsoft Accessibility Insights](https://accessibilityinsights.io/) integration for a single Commerce site, follow these steps.</span></span>

1. <span data-ttu-id="d213c-119">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="d213c-119">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d213c-120">Vælg **Indstillinger for websted** i venstre navigationsrude for at udvide den.</span><span class="sxs-lookup"><span data-stu-id="d213c-120">In the left navigation pane, select **Site Settings** to expand it.</span></span>
1. <span data-ttu-id="d213c-121">Under **Indstillinger for webstedet** skal du vælge **Funktioner**.</span><span class="sxs-lookup"><span data-stu-id="d213c-121">Under **Site Settings**, select **Features**.</span></span>
1. <span data-ttu-id="d213c-122">Angiv indstillingen **Tilgængelighedskontrol** til **Til**.</span><span class="sxs-lookup"><span data-stu-id="d213c-122">Set the **Accessibility Check** option to **On**.</span></span>

## <a name="verify-the-accessibility-of-the-content-on-the-home-page"></a><span data-ttu-id="d213c-123">Kontroller tilgængeligheden af indholdet på startsiden</span><span class="sxs-lookup"><span data-stu-id="d213c-123">Verify the accessibility of the content on the home page</span></span>

<span data-ttu-id="d213c-124">Hvis du vil bruge den integrerede [Microsoft Accessibility Insights](https://accessibilityinsights.io/)-tjeneste til at scanne og kontrollere indholdet på din startside i Commerce, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="d213c-124">To use the integrated [Microsoft Accessibility Insights](https://accessibilityinsights.io/) service to scan and verify the content of your home page in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="d213c-125">Vælg **Fabrikam** (eller navnet på dit websted) under **Websteder**.</span><span class="sxs-lookup"><span data-stu-id="d213c-125">Under **Sites**, select **Fabrikam** (or the name of your site).</span></span>
1. <span data-ttu-id="d213c-126">Vælg **Sider** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="d213c-126">In the left navigation pane, select **Pages**.</span></span>
1. <span data-ttu-id="d213c-127">Find og vælg startsiden for at åbne den i sideeditoren.</span><span class="sxs-lookup"><span data-stu-id="d213c-127">Find and select the home page to open it in the page editor.</span></span>
1. <span data-ttu-id="d213c-128">Vælg **Kontrollér tilgængelighed** på kommandolinjen.</span><span class="sxs-lookup"><span data-stu-id="d213c-128">On the command bar, select **Check accessibility**.</span></span> <span data-ttu-id="d213c-129">Siden **Kontroller tilgængelighed** vises.</span><span class="sxs-lookup"><span data-stu-id="d213c-129">The **Check Accessibility** page appears.</span></span>
1. <span data-ttu-id="d213c-130">Gennemse rapportens indhold, når scanningen er fuldført.</span><span class="sxs-lookup"><span data-stu-id="d213c-130">After the scan is completed, review the contents of the report.</span></span>
1. <span data-ttu-id="d213c-131">Hvis en kontrol mislykkedes, skal du markere hvert mislykket kontrolelement for at udvide det, så du kan få vist flere oplysninger.</span><span class="sxs-lookup"><span data-stu-id="d213c-131">If any checks failed, select each failed check item to expand it so that you can view more details.</span></span>
1. <span data-ttu-id="d213c-132">Hvis du vil lukke rapporten, når du er færdig med at gennemse den, skal du rulle ned til bunden af siden **Kontrollér tilgængelighed** og vælge **OK**.</span><span class="sxs-lookup"><span data-stu-id="d213c-132">To close the report after you've finished reviewing it, scroll to the bottom of the **Check Accessibility** page, and select **OK**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d213c-133">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d213c-133">Additional resources</span></span>

[<span data-ttu-id="d213c-134">Redigere en eksisterende webstedsside</span><span class="sxs-lookup"><span data-stu-id="d213c-134">Modify an existing site page</span></span>](modify-existing-page.md)

[<span data-ttu-id="d213c-135">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="d213c-135">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d213c-136">Vælge sidelayout</span><span class="sxs-lookup"><span data-stu-id="d213c-136">Select page layouts</span></span>](select-page-layouts.md)

[<span data-ttu-id="d213c-137">Administrere SEO-metadata</span><span class="sxs-lookup"><span data-stu-id="d213c-137">Manage SEO metadata</span></span>](manage-seo-metadata.md)

[<span data-ttu-id="d213c-138">Gemme, få vist og udgive en side</span><span class="sxs-lookup"><span data-stu-id="d213c-138">Save, preview, and publish a page</span></span>](save-preview-publish-page.md)

[<span data-ttu-id="d213c-139">Forbedre en produktside</span><span class="sxs-lookup"><span data-stu-id="d213c-139">Enrich a product page</span></span>](enrich-product-page.md)

[<span data-ttu-id="d213c-140">Forbedre en kategorilandingsside</span><span class="sxs-lookup"><span data-stu-id="d213c-140">Enrich a category landing page</span></span>](enrich-category-page.md)
