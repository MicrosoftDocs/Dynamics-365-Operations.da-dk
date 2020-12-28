---
title: Bygge brugerdefinerede svarsider for 4xx/5xx statuskodefejl
description: I dette emne beskrives, hvordan du bygger tilpassede svarsider for 4xx- og 5xx-statuskodefejl ved hjælp af oprettelsesværktøjerne i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 04/14/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: josaw
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 060f5e5616624279711f61f582e6a898c7eb7785
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4411049"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="34016-103">Bygge brugerdefinerede svarsider for 4xx/5xx statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="34016-103">Build custom response pages for 4xx/5xx status code errors</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="34016-104">I dette emne beskrives, hvordan du bygger tilpassede svarsider for 4xx- og 5xx-statuskodefejl ved hjælp af oprettelsesværktøjerne i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="34016-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="34016-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="34016-105">Overview</span></span>

<span data-ttu-id="34016-106">Hvis en anmodning ikke lykkes, udsteder serveren fejlsvar med HTTP-statuskode.</span><span class="sxs-lookup"><span data-stu-id="34016-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="34016-107">Statuskoden 404 registreres og returneres, hvis der ikke bliver fundet en side, og statuskoden 500 registreres og returneres, hvis der opstår en serverfejl.</span><span class="sxs-lookup"><span data-stu-id="34016-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="34016-108">I Dynamics 365 Commerce kan programbrugere opbygge brugerdefinerede fejlsvarsider med statuskode, der vises for brugere af disse statuskodefejlsvar.</span><span class="sxs-lookup"><span data-stu-id="34016-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="34016-109">Oprette en svarside for statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="34016-109">Build a status code error response page</span></span>

<span data-ttu-id="34016-110">Udfør følgende trin for at begynde at opbygge en svarside for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="34016-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="34016-111">Log på Dynamics 365 Commerce i din foretrukne webbrowser.</span><span class="sxs-lookup"><span data-stu-id="34016-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="34016-112">Vælg det websted, du vil bygge en svarside for 4xx/5xx statuskodefejl for.</span><span class="sxs-lookup"><span data-stu-id="34016-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="34016-113">Opbygge skabelonen</span><span class="sxs-lookup"><span data-stu-id="34016-113">Build the template</span></span>

<span data-ttu-id="34016-114">Udfør følgende trin for at begynde at opbygge skabelonen for svarsiden for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="34016-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="34016-115">Gå til **Skabeloner**.</span><span class="sxs-lookup"><span data-stu-id="34016-115">Go to **Templates**.</span></span>
1. <span data-ttu-id="34016-116">Vælg **Ny** for at oprette en sideskabelon.</span><span class="sxs-lookup"><span data-stu-id="34016-116">Select **New** to create a page template.</span></span>
1. <span data-ttu-id="34016-117">Angiv et navn til den nye skabelon under **Skabelonnavn** i dialogboksen **Ny skabelon**, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="34016-117">In the **New Template** dialog box, under **Template Name**, enter a name for the new template, and then select **OK**.</span></span>
1. <span data-ttu-id="34016-118">Opret skabelonen på basis af den struktur, som du ønsker, at svarsiden for statuskodefejlen skal have.</span><span class="sxs-lookup"><span data-stu-id="34016-118">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="34016-119">Vælg **Gem**, vælg **Afslut redigering** for at tjekke skabelonen ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="34016-119">Select **Save**, select **Finish editing** to check in the template, and then select **Publish** to publish it.</span></span> 

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="34016-120">Oprette svarsiden for statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="34016-120">Build the status code error response page</span></span>

<span data-ttu-id="34016-121">Udfør følgende trin for at opbygge svarsiden for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="34016-121">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="34016-122">Gå til **Sider**.</span><span class="sxs-lookup"><span data-stu-id="34016-122">Go to **Pages**.</span></span>
1. <span data-ttu-id="34016-123">Vælg **Ny** for at oprette en side.</span><span class="sxs-lookup"><span data-stu-id="34016-123">Select **New** to create a page.</span></span>
1. <span data-ttu-id="34016-124">Vælg en skabelon i dialogboksen **Vælg en skabelon**, og angiv derefter navnet på svarsiden for statuskodefejl under **Sidenavn**.</span><span class="sxs-lookup"><span data-stu-id="34016-124">In the **Choose a template** dialog box, select a template, and then, under **Page name**, enter a name for the status code error response page.</span></span> <span data-ttu-id="34016-125">Lad feltet **Sidens URL-adresse** stå tomt.</span><span class="sxs-lookup"><span data-stu-id="34016-125">Leave the **Page URL** field blank.</span></span>
1. <span data-ttu-id="34016-126">Opbyg siden.</span><span class="sxs-lookup"><span data-stu-id="34016-126">Build the page.</span></span>
1. <span data-ttu-id="34016-127">Vælg **Gem**, vælg **Afslut redigering** for at tjekke siden ind, og vælg derefter **Publicer** for at publicere den.</span><span class="sxs-lookup"><span data-stu-id="34016-127">Select **Save**, select **Finish editing** to check in the page, and then select **Publish** to publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="34016-128">Du kan oprette separate svarsider for statuskodefejl 4xx og 5xx.</span><span class="sxs-lookup"><span data-stu-id="34016-128">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="34016-129">Du kan også bruge den samme generelle svarside for statuskodefejl til begge fejlkategorier.</span><span class="sxs-lookup"><span data-stu-id="34016-129">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="34016-130">Konfigurere en omdirigering for svarside for statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="34016-130">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="34016-131">Udfør følgende trin for at konfigurere en omdirigering for svarsiden for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="34016-131">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="34016-132">Gå til **URL-adresser \> Ny \> Nyt alias**, og vælg den svarside for statuskodefejl, du har opbygget tidligere.</span><span class="sxs-lookup"><span data-stu-id="34016-132">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="34016-133">I feltet **Alias** skal du enten angive **standard-4xx** eller **standard-5xx**, afhængigt af svarsiden for statuskodefejl, som du vil konfigurere en omdirigering for.</span><span class="sxs-lookup"><span data-stu-id="34016-133">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="34016-134">Disse aliasser skal publiceres.</span><span class="sxs-lookup"><span data-stu-id="34016-134">These aliases must be published.</span></span> <span data-ttu-id="34016-135">Ellers vil omdirigeringen ikke fungere.</span><span class="sxs-lookup"><span data-stu-id="34016-135">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="34016-136">Vælg **OK** for at oprette tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="34016-136">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="34016-137">Hvis du bruger en enkelt svarside for statuskodefejl til begge fejlkategorier, skal du gentage denne procedure for at sammenkæde et alias for den anden fejlkategori med den samme side.</span><span class="sxs-lookup"><span data-stu-id="34016-137">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="34016-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="34016-138">Additional resources</span></span>

[<span data-ttu-id="34016-139">Arbejde med skabeloner</span><span class="sxs-lookup"><span data-stu-id="34016-139">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="34016-140">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="34016-140">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="34016-141">Oprette en side-URL</span><span class="sxs-lookup"><span data-stu-id="34016-141">Create a page URL</span></span>](create-page-url.md)
