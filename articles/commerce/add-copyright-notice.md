---
title: Tilføj en copyright-meddelelse
description: I dette emne beskrives det, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.
author: psimolin
manager: AnnBe
ms.date: 10/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 54d9ccbb56131333159cdf8858dfca23b75b61fd
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980450"
---
# <a name="add-a-copyright-notice"></a><span data-ttu-id="02788-103">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="02788-103">Add a copyright notice</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="02788-104">I dette emne beskrives det, hvordan du føjer en copyrightmeddelelse til e-handelswebstedet.</span><span class="sxs-lookup"><span data-stu-id="02788-104">This topic describes how to add a copyright notice to your e-Commerce website.</span></span>

## <a name="prerequisites"></a><span data-ttu-id="02788-105">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="02788-105">Prerequisites</span></span>

<span data-ttu-id="02788-106">Før du kan føje en meddelelse om ophavsret til webstedet, skal du have følgende elementer:</span><span class="sxs-lookup"><span data-stu-id="02788-106">Before you can add a copyright notice to your site, you must have the following items:</span></span>

- <span data-ttu-id="02788-107">En skabelon, der indeholder et delt sidefodsfragment.</span><span class="sxs-lookup"><span data-stu-id="02788-107">A template that includes a shared footer fragment.</span></span>
- <span data-ttu-id="02788-108">En side, hvor denne skabelon bruges.</span><span class="sxs-lookup"><span data-stu-id="02788-108">A page that uses that template.</span></span>

## <a name="add-a-copyright-notice"></a><span data-ttu-id="02788-109">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="02788-109">Add a copyright notice</span></span>

<span data-ttu-id="02788-110">Hvis du vil tilføje en meddelelse om ophavsret nederst på alle de sider, der bruger en bestemt skabelon, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="02788-110">To add a copyright notice to the bottom of every page that uses a specific template, follow these steps.</span></span>

1. <span data-ttu-id="02788-111">Gå til **Fragmenter**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="02788-111">Go to **Fragments**, and then select **New**.</span></span>
1. <span data-ttu-id="02788-112">Vælg modulet **Sidefod** i dialogboksen **Nyt fragment**, og navngiv fragmentet.</span><span class="sxs-lookup"><span data-stu-id="02788-112">In the **New fragment** dialog box, select the **Footer** module, and name the fragment.</span></span> <span data-ttu-id="02788-113">Du kan f.eks. skrive **Sidefod-ophavsret**.</span><span class="sxs-lookup"><span data-stu-id="02788-113">For example, enter **Footer-Copyright**.</span></span>
1. <span data-ttu-id="02788-114">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="02788-114">Select **OK**.</span></span>
1. <span data-ttu-id="02788-115">Vælg ellipseknappen (**...**) i navigationsruden ud for **Sidefod**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="02788-115">In the navigation pane, select the ellipsis button (**...**) next to **Footer**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="02788-116">Vælg **Sidefodskategori** i dialogboksen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="02788-116">In the dialog box, select **Footer category**, and then select **OK**.</span></span>
1. <span data-ttu-id="02788-117">Vælg ellipseknappen i navigationsruden ud for **Sidefodskategori**, og vælg derefter **Tilføj modul**.</span><span class="sxs-lookup"><span data-stu-id="02788-117">In the navigation pane, select the ellipsis button next to **Footer category**, and then select **Add Module**.</span></span>
1. <span data-ttu-id="02788-118">Vælg **Tekstblok** i dialogboksen, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="02788-118">In the dialog box, select **Text block**, and then select **OK**.</span></span>
1. <span data-ttu-id="02788-119">Vælg **Tekstblok** i navigationsruden.</span><span class="sxs-lookup"><span data-stu-id="02788-119">In the navigation pane, select **Text block**.</span></span>
1. <span data-ttu-id="02788-120">Tilføj meddelelsen om ophavsret i egenskabsruden til højre i feltet **Afsnit**.</span><span class="sxs-lookup"><span data-stu-id="02788-120">In the properties pane on the right, in the **Paragraph** field, add your copyright message.</span></span> <span data-ttu-id="02788-121">Angiv f.eks. **(C) Fabrikam 2019**.</span><span class="sxs-lookup"><span data-stu-id="02788-121">For example, enter **(C) Fabrikam 2019**.</span></span>
1. <span data-ttu-id="02788-122">Vælg **Gem**, vælg **Afslut redigering**, og vælg derefter **Publicer**.</span><span class="sxs-lookup"><span data-stu-id="02788-122">Select **Save**, select **Finish editing**, and then select **Publish**.</span></span>
1. <span data-ttu-id="02788-123">Gå til **Skabeloner**, vælg skabelonen, og vælg derefter **Rediger**.</span><span class="sxs-lookup"><span data-stu-id="02788-123">Go to **Templates**, select the template, and then select **Edit**.</span></span>
1. <span data-ttu-id="02788-124">Under **Sidedisposition** skal du udvide **Brødtekst** og derefter udvide **Standardside**.</span><span class="sxs-lookup"><span data-stu-id="02788-124">Under **Page Outline**, expand **Body**, and then expand **Default Page**.</span></span>
1. <span data-ttu-id="02788-125">Vælg ellipseknappen ud for **Sidefodsplads**, og vælg derefter **Tilføj fragment**.</span><span class="sxs-lookup"><span data-stu-id="02788-125">Select the ellipsis button next to **Footer Slot**, and then select **Add Fragment**.</span></span>
1. <span data-ttu-id="02788-126">Vælg det fragment, du oprettede tidligere, og vælg derefter **Vælg**.</span><span class="sxs-lookup"><span data-stu-id="02788-126">Select the fragment that you created earlier, and then select **Select**.</span></span>
1. <span data-ttu-id="02788-127">Vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="02788-127">Select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span>

<span data-ttu-id="02788-128">Den sidefod, der indeholder meddelelsen om ophavsret, vises automatisk nederst på alle de sider, der bruger den valgte skabelon.</span><span class="sxs-lookup"><span data-stu-id="02788-128">The footer that contains the copyright notice automatically appears at the bottom of all pages that use the selected template.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="02788-129">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="02788-129">Additional resources</span></span>

[<span data-ttu-id="02788-130">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="02788-130">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="02788-131">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="02788-131">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="02788-132">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="02788-132">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="02788-133">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="02788-133">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="02788-134">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="02788-134">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="02788-135">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="02788-135">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="02788-136">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="02788-136">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

