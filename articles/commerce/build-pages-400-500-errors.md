---
title: Bygge brugerdefinerede svarsider for 4xx/5xx statuskodefejl
description: I dette emne beskrives, hvordan du bygger tilpassede svarsider for 4xx- og 5xx-statuskodefejl ved hjælp af oprettelsesværktøjerne i Microsoft Dynamics 365 Commerce.
author: v-chgri
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 6b35b3c07b1edd41e6a3763c0001529e125e4636
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5799635"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="a719f-103">Bygge brugerdefinerede svarsider for 4xx/5xx statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="a719f-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a719f-104">I dette emne beskrives, hvordan du bygger tilpassede svarsider for 4xx- og 5xx-statuskodefejl ved hjælp af oprettelsesværktøjerne i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a719f-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a719f-105">Hvis en anmodning ikke lykkes, udsteder serveren fejlsvar med HTTP-statuskode.</span><span class="sxs-lookup"><span data-stu-id="a719f-105">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="a719f-106">Statuskoden 404 registreres og returneres, hvis der ikke bliver fundet en side, og statuskoden 500 registreres og returneres, hvis der opstår en serverfejl.</span><span class="sxs-lookup"><span data-stu-id="a719f-106">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="a719f-107">I Dynamics 365 Commerce kan programbrugere opbygge brugerdefinerede fejlsvarsider med statuskode, der vises for brugere af disse statuskodefejlsvar.</span><span class="sxs-lookup"><span data-stu-id="a719f-107">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="a719f-108">Oprette en svarside for statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="a719f-108">Build a status code error response page</span></span>

<span data-ttu-id="a719f-109">Udfør følgende trin for at begynde at opbygge en svarside for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="a719f-109">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="a719f-110">Log på Dynamics 365 Commerce i din foretrukne webbrowser.</span><span class="sxs-lookup"><span data-stu-id="a719f-110">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="a719f-111">Vælg det websted, du vil bygge en svarside for 4xx/5xx statuskodefejl for.</span><span class="sxs-lookup"><span data-stu-id="a719f-111">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="a719f-112">Opbygge skabelonen</span><span class="sxs-lookup"><span data-stu-id="a719f-112">Build the template</span></span>

<span data-ttu-id="a719f-113">Udfør følgende trin for at begynde at opbygge skabelonen for svarsiden for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="a719f-113">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="a719f-114">Gå til **Skabeloner**.</span><span class="sxs-lookup"><span data-stu-id="a719f-114">Go to **Templates**.</span></span>
1. <span data-ttu-id="a719f-115">Vælg **Ny** for at oprette en sideskabelon.</span><span class="sxs-lookup"><span data-stu-id="a719f-115">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="a719f-116">Angiv et navn til den nye skabelon under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="a719f-116">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="a719f-117">Opret skabelonen på basis af den struktur, som du ønsker, at svarsiden for statuskodefejlen skal have.</span><span class="sxs-lookup"><span data-stu-id="a719f-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="a719f-118">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="a719f-118">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="a719f-119">Oprette svarsiden for statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="a719f-119">Build the status code error response page</span></span>

<span data-ttu-id="a719f-120">Udfør følgende trin for at opbygge svarsiden for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="a719f-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="a719f-121">Gå til **Sider**.</span><span class="sxs-lookup"><span data-stu-id="a719f-121">Go to **Pages**.</span></span>
1. <span data-ttu-id="a719f-122">Vælg **Ny** for at oprette en side.</span><span class="sxs-lookup"><span data-stu-id="a719f-122">Select **New** to create a page.</span></span>
1. <span data-ttu-id="a719f-123">Vælg en skabelon i dialogboksen **Vælg en skabelon**, og angiv derefter navnet på svarsiden for statuskodefejl under **Sidenavn**.</span><span class="sxs-lookup"><span data-stu-id="a719f-123">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="a719f-124">Lad feltet **Sidens URL-adresse** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="a719f-124">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="a719f-125">Opbyg siden.</span><span class="sxs-lookup"><span data-stu-id="a719f-125">Build the page.</span></span>
1. <span data-ttu-id="a719f-126">Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="a719f-126">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="a719f-127">Du kan oprette separate svarsider for statuskodefejl 4xx og 5xx.</span><span class="sxs-lookup"><span data-stu-id="a719f-127">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="a719f-128">Du kan også bruge den samme generelle svarside for statuskodefejl til begge fejlkategorier.</span><span class="sxs-lookup"><span data-stu-id="a719f-128">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="a719f-129">Konfigurere en omdirigering for svarside for statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="a719f-129">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="a719f-130">Udfør følgende trin for at konfigurere en omdirigering for svarsiden for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="a719f-130">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="a719f-131">Gå til **URL-adresser \> Ny \> Nyt alias**, og vælg den svarside for statuskodefejl, du har opbygget tidligere.</span><span class="sxs-lookup"><span data-stu-id="a719f-131">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="a719f-132">I feltet **Alias** skal du enten angive **standard-4xx** eller **standard-5xx**, afhængigt af svarsiden for statuskodefejl, som du vil konfigurere en omdirigering for.</span><span class="sxs-lookup"><span data-stu-id="a719f-132">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="a719f-133">Disse aliasser skal publiceres.</span><span class="sxs-lookup"><span data-stu-id="a719f-133">These aliases must be published.</span></span> <span data-ttu-id="a719f-134">Ellers vil omdirigeringen ikke fungere.</span><span class="sxs-lookup"><span data-stu-id="a719f-134">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="a719f-135">Vælg **OK** for at oprette tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="a719f-135">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="a719f-136">Hvis du bruger en enkelt svarside for statuskodefejl til begge fejlkategorier, skal du gentage denne procedure for at sammenkæde et alias for den anden fejlkategori med den samme side.</span><span class="sxs-lookup"><span data-stu-id="a719f-136">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a719f-137">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a719f-137">Additional resources</span></span>

[<span data-ttu-id="a719f-138">Arbejde med skabeloner</span><span class="sxs-lookup"><span data-stu-id="a719f-138">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="a719f-139">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="a719f-139">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="a719f-140">Oprette en side-URL</span><span class="sxs-lookup"><span data-stu-id="a719f-140">Create a page URL</span></span>](create-page-url.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
