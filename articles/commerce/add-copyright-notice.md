---
title: Tilføj en copyright-meddelelse
description: I dette emne beskrives det, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.
author: psimolin
manager: AnnBe
ms.date: 12/12/2019
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
ms.openlocfilehash: 58c2949057ef777f706d12cee2dd3341d1a3b7e6
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2914559"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="105b0-103">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="105b0-103">Add a copyright notice</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="105b0-104">I dette emne beskrives det, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="105b0-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="105b0-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="105b0-105">Prerequisites</span></span>

<span data-ttu-id="105b0-106">Før du kan føje en meddelelse om ophavsret til webstedet, skal du have følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="105b0-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="105b0-107">En skabelon, der indeholder et delt sidefodsfragment.</span><span class="sxs-lookup"><span data-stu-id="105b0-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="105b0-108">En side, hvor denne skabelon bruges.</span><span class="sxs-lookup"><span data-stu-id="105b0-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="105b0-109">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="105b0-109">Add a copyright notice</span></span>

<span data-ttu-id="105b0-110">Hvis du vil tilføje en meddelelse om ophavsret nederst på alle de sider, der bruger en bestemt skabelon, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="105b0-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="105b0-111">Gå til **Fragmenter**, og vælg derefter **Nyt side fragment**.</span><span class="sxs-lookup"><span data-stu-id="105b0-111">Go to **Fragments**, and then select **New Page Fragment**.</span></span>
1. <span data-ttu-id="105b0-112">Vælg modulet **Sidefod** i dialogboksen, og navngiv fragmentet.</span><span class="sxs-lookup"><span data-stu-id="105b0-112">In the dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="105b0-113">Du kan f.eks. skrive **Sidefod-ophavsret**.</span><span class="sxs-lookup"><span data-stu-id="105b0-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="105b0-114">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="105b0-114">Select **OK**.</span></span>
1. <span data-ttu-id="105b0-115">Vælg ellipseknappen (**...**) i navigationsruden ud for **Sidefod**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="105b0-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="105b0-116">Vælg **Sidefodskategori** i dialogboksen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="105b0-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="105b0-117">Vælg ellipseknappen i navigationsruden ud for **Sidefodskategori**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="105b0-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="105b0-118">Vælg **Element for indholdsrig blok** i dialogboksen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="105b0-118">In the dialog box, select **Content rich block item**, and then select **OK**.</span></span>
1. <span data-ttu-id="105b0-119">Vælg **Element for indholdsrig blok** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="105b0-119">In the navigation pane, select **Content rich block item**.</span></span>
1. <span data-ttu-id="105b0-120">Tilføj meddelelsen om ophavsret i egenskabsruden til højre i feltet **Afsnit**.</span><span class="sxs-lookup"><span data-stu-id="105b0-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="105b0-121">Angiv f.eks. **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="105b0-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="105b0-122">Vælg **Gem**, vælg **Tjek ind**, og vælg derefter **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="105b0-122">Select **Save**, select **Check In**, and then select **Publish**.</span></span>
1. <span data-ttu-id="105b0-123">Gå til **Skabeloner**, vælg skabelonen, og vælg derefter **Tjek ud**.</span><span class="sxs-lookup"><span data-stu-id="105b0-123">Go to **Templates**, select the template, and then select **Check Out**.</span></span>
1. <span data-ttu-id="105b0-124">Under **Sidedisposition** skal du udvide **Brødtekst** og derefter udvide **Standardside**.</span><span class="sxs-lookup"><span data-stu-id="105b0-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="105b0-125">Vælg ellipseknappen ud for **Sidefodsplads**, og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="105b0-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="105b0-126">Vælg det fragment, du oprettede tidligere, og vælg derefter **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="105b0-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="105b0-127">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="105b0-127">Check in the template, and publish it.</span></span>

<span data-ttu-id="105b0-128">Den sidefod, der indeholder meddelelsen om ophavsret, vises automatisk nederst på alle de sider, der bruger den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="105b0-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="105b0-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="105b0-129">Additional resources</span></span>

[<span data-ttu-id="105b0-130">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="105b0-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="105b0-131">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="105b0-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="105b0-132">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="105b0-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="105b0-133">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="105b0-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="105b0-134">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="105b0-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="105b0-135">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="105b0-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="105b0-136">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="105b0-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

