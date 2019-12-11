---
title: Tilføj en copyright-meddelelse
description: I dette emne beskrives det, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.
author: psimolin
manager: AnnBe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 39135a2eca25336097ee9eddf06dc6709c102571
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696939"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="e72db-103">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="e72db-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="e72db-104">I dette emne beskrives det, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="e72db-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="e72db-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="e72db-105">Prerequisites</span></span>

<span data-ttu-id="e72db-106">Før du kan føje en meddelelse om ophavsret til webstedet, skal du have følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="e72db-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="e72db-107">En skabelon, der indeholder et delt sidefodsfragment.</span><span class="sxs-lookup"><span data-stu-id="e72db-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="e72db-108">En side, hvor denne skabelon bruges.</span><span class="sxs-lookup"><span data-stu-id="e72db-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="e72db-109">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="e72db-109">Add a copyright notice</span></span>

<span data-ttu-id="e72db-110">Hvis du vil tilføje en meddelelse om ophavsret nederst på alle de sider, der bruger en bestemt skabelon, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e72db-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="e72db-111">Gå til **Fragmenter**, og vælg derefter **Nyt side fragment**.</span><span class="sxs-lookup"><span data-stu-id="e72db-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="e72db-112">Vælg modulet **Sidefod** i dialogboksen, og navngiv fragmentet.</span><span class="sxs-lookup"><span data-stu-id="e72db-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="e72db-113">Du kan f.eks. skrive **Sidefod-ophavsret**.</span><span class="sxs-lookup"><span data-stu-id="e72db-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="e72db-114">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="e72db-114">Select **OK**.</span></span>
1. <span data-ttu-id="e72db-115">Vælg ellipseknappen (**...**) i navigationsruden ud for **Sidefod**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e72db-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="e72db-116">Vælg **Sidefodskategori** i dialogboksen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e72db-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="e72db-117">Vælg ellipseknappen i navigationsruden ud for **Sidefodskategori**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="e72db-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="e72db-118">Vælg **Element for indholdsrig blok** i dialogboksen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="e72db-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="e72db-119">Vælg **Element for indholdsrig blok** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="e72db-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="e72db-120">Tilføj meddelelsen om ophavsret i egenskabsruden til højre i feltet **Afsnit**.</span><span class="sxs-lookup"><span data-stu-id="e72db-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="e72db-121">Angiv f.eks. **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="e72db-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="e72db-122">Vælg **Gem**, vælg **Tjek ind**, og vælg derefter **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="e72db-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="e72db-123">Gå til **Skabeloner**, vælg skabelonen, og vælg derefter **Tjek ud**.</span><span class="sxs-lookup"><span data-stu-id="e72db-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="e72db-124">Under **Sidedisposition** skal du udvide **Brødtekst** og derefter udvide **Standardside**.</span><span class="sxs-lookup"><span data-stu-id="e72db-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="e72db-125">Vælg ellipseknappen ud for **Sidefodsplads**, og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="e72db-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="e72db-126">Vælg det fragment, du oprettede tidligere, og vælg derefter **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="e72db-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="e72db-127">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="e72db-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="e72db-128">Den sidefod, der indeholder meddelelsen om ophavsret, vises automatisk nederst på alle de sider, der bruger den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="e72db-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e72db-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e72db-129">Additional resources</span></span>

[<span data-ttu-id="e72db-130">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="e72db-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="e72db-131">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="e72db-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="e72db-132">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="e72db-132">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="e72db-133">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="e72db-133">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="e72db-134">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="e72db-134">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="e72db-135">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="e72db-135">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

