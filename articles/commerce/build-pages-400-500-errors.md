---
title: Bygge brugerdefinerede svarsider for 4xx/5xx statuskodefejl
description: I dette emne beskrives, hvordan du bygger tilpassede svarsider for 4xx- og 5xx-statuskodefejl ved hjælp af oprettelsesværktøjerne i Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: bcceeb1bc68c6432442c863ca06b7ba81d0abed8
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2697100"
---
# <a name="build-custom-response-pages-for-4xx5xx-status-code-errors"></a><span data-ttu-id="d178c-103">Bygge brugerdefinerede svarsider for 4xx/5xx statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="d178c-103">Build custom response pages for 4xx/5xx status code errors</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="d178c-104">I dette emne beskrives, hvordan du bygger tilpassede svarsider for 4xx- og 5xx-statuskodefejl ved hjælp af oprettelsesværktøjerne i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="d178c-104">This topic describes how to build custom response pages for 4xx and 5xx status code errors by using the authoring tools in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="d178c-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="d178c-105">Overview</span></span>

<span data-ttu-id="d178c-106">Hvis en anmodning ikke lykkes, udsteder serveren fejlsvar med HTTP-statuskode.</span><span class="sxs-lookup"><span data-stu-id="d178c-106">If a request isn't successful, the server issues HTTP status code error responses.</span></span> <span data-ttu-id="d178c-107">Statuskoden 404 registreres og returneres, hvis der ikke bliver fundet en side, og statuskoden 500 registreres og returneres, hvis der opstår en serverfejl.</span><span class="sxs-lookup"><span data-stu-id="d178c-107">The 404 status code is captured and returned if a page isn't found, and the 500 status code is captured and returned if a server error occurs.</span></span> <span data-ttu-id="d178c-108">I Dynamics 365 Commerce kan programbrugere opbygge brugerdefinerede fejlsvarsider med statuskode, der vises for brugere af disse statuskodefejlsvar.</span><span class="sxs-lookup"><span data-stu-id="d178c-108">In Dynamics 365 Commerce, application users can build custom status code error response pages that are shown to users for these status code error responses.</span></span>

## <a name="build-a-status-code-error-response-page"></a><span data-ttu-id="d178c-109">Oprette en svarside for statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="d178c-109">Build a status code error response page</span></span>

<span data-ttu-id="d178c-110">Udfør følgende trin for at begynde at opbygge en svarside for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="d178c-110">To start to build a status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d178c-111">Log på Dynamics 365 Commerce i din foretrukne webbrowser.</span><span class="sxs-lookup"><span data-stu-id="d178c-111">In your preferred web browser, sign in to Dynamics 365 Commerce.</span></span> 
1. <span data-ttu-id="d178c-112">Vælg det websted, du vil bygge en svarside for 4xx/5xx statuskodefejl for.</span><span class="sxs-lookup"><span data-stu-id="d178c-112">Select the site that you want to build a 4xx/5xx status code error response page for.</span></span>

### <a name="build-the-template"></a><span data-ttu-id="d178c-113">Opbygge skabelonen</span><span class="sxs-lookup"><span data-stu-id="d178c-113">Build the template</span></span>

<span data-ttu-id="d178c-114">Udfør følgende trin for at begynde at opbygge skabelonen for svarsiden for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="d178c-114">To build the template for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d178c-115">Gå til **Skabelon \> Ny skabelon**.</span><span class="sxs-lookup"><span data-stu-id="d178c-115">Go to **Templates \> New template**.</span></span>
1. <span data-ttu-id="d178c-116">Navngiv den nye skabelon.</span><span class="sxs-lookup"><span data-stu-id="d178c-116">Name the new template.</span></span>
1. <span data-ttu-id="d178c-117">Opret skabelonen på basis af den struktur, som du ønsker, at svarsiden for statuskodefejlen skal have.</span><span class="sxs-lookup"><span data-stu-id="d178c-117">Build the template, based on the structure that you want the status code error response page to have.</span></span>
1. <span data-ttu-id="d178c-118">Check skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="d178c-118">Check the template in, and publish it.</span></span>

### <a name="build-the-status-code-error-response-page"></a><span data-ttu-id="d178c-119">Oprette svarsiden for statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="d178c-119">Build the status code error response page</span></span>

<span data-ttu-id="d178c-120">Udfør følgende trin for at opbygge svarsiden for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="d178c-120">To build the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d178c-121">Gå til **Sider \> Ny side**.</span><span class="sxs-lookup"><span data-stu-id="d178c-121">Go to **Pages \> New Page**.</span></span>
1. <span data-ttu-id="d178c-122">Navngiv svarsiden for statuskodefejl, men angiv **ikke** **URL-adresse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="d178c-122">Name the status code error response page, but do **not** set the **URL** field.</span></span>
1. <span data-ttu-id="d178c-123">Opbyg siden.</span><span class="sxs-lookup"><span data-stu-id="d178c-123">Build the page.</span></span>
1. <span data-ttu-id="d178c-124">Check siden ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="d178c-124">Check the page in, and publish it.</span></span>

> [!NOTE]
> <span data-ttu-id="d178c-125">Du kan oprette separate svarsider for statuskodefejl 4xx og 5xx.</span><span class="sxs-lookup"><span data-stu-id="d178c-125">You can create separate status code error response pages for 4xx and 5xx status code errors.</span></span> <span data-ttu-id="d178c-126">Du kan også bruge den samme generelle svarside for statuskodefejl til begge fejlkategorier.</span><span class="sxs-lookup"><span data-stu-id="d178c-126">Alternatively, you can use the same general status code error response page for both error categories.</span></span>

### <a name="set-up-a-redirect-for-the-status-code-error-response-page"></a><span data-ttu-id="d178c-127">Konfigurere en omdirigering for svarside for statuskodefejl</span><span class="sxs-lookup"><span data-stu-id="d178c-127">Set up a redirect for the status code error response page</span></span>

<span data-ttu-id="d178c-128">Udfør følgende trin for at konfigurere en omdirigering for svarsiden for statuskodefejl.</span><span class="sxs-lookup"><span data-stu-id="d178c-128">To set up a redirect for the status code error response page, follow these steps.</span></span>

1. <span data-ttu-id="d178c-129">Gå til **URL-adresser \> Ny \> Nyt alias**, og vælg den svarside for statuskodefejl, du har opbygget tidligere.</span><span class="sxs-lookup"><span data-stu-id="d178c-129">Go to **URLs \> New \> New Alias**, and select the status code error response page that you built earlier.</span></span>
1. <span data-ttu-id="d178c-130">I feltet **Alias** skal du enten angive **standard-4xx** eller **standard-5xx**, afhængigt af svarsiden for statuskodefejl, som du vil konfigurere en omdirigering for.</span><span class="sxs-lookup"><span data-stu-id="d178c-130">In the **Alias** field, enter either **default-4xx** or **default-5xx**, depending on the status code error response page that you're setting up a redirect for.</span></span> <span data-ttu-id="d178c-131">Disse aliasser skal publiceres.</span><span class="sxs-lookup"><span data-stu-id="d178c-131">These aliases must be published.</span></span> <span data-ttu-id="d178c-132">Ellers vil omdirigeringen ikke fungere.</span><span class="sxs-lookup"><span data-stu-id="d178c-132">Otherwise, the redirect won't work.</span></span>
1. <span data-ttu-id="d178c-133">Vælg **OK** for at oprette tilknytningen.</span><span class="sxs-lookup"><span data-stu-id="d178c-133">Select **OK** to commit the linking.</span></span>

> [!NOTE]
> <span data-ttu-id="d178c-134">Hvis du bruger en enkelt svarside for statuskodefejl til begge fejlkategorier, skal du gentage denne procedure for at sammenkæde et alias for den anden fejlkategori med den samme side.</span><span class="sxs-lookup"><span data-stu-id="d178c-134">If you're using a single status code error response page for both error categories, repeat this procedure to link an alias for the other error category to the same page.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="d178c-135">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="d178c-135">Additional resources</span></span>

[<span data-ttu-id="d178c-136">Arbejde med skabeloner</span><span class="sxs-lookup"><span data-stu-id="d178c-136">Work with templates</span></span>](work-with-templates.md)

[<span data-ttu-id="d178c-137">Tilføje en ny webstedsside</span><span class="sxs-lookup"><span data-stu-id="d178c-137">Add a new site page</span></span>](add-new-page.md)

[<span data-ttu-id="d178c-138">Oprette en side-URL</span><span class="sxs-lookup"><span data-stu-id="d178c-138">Create a page URL</span></span>](create-page-url.md)
