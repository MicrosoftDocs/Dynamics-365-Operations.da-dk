---
title: Tilføj en favicon
description: I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.
author: bicyclingfool
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 58cb6c592351a96876532ef53d5d477ff93fafa1
ms.sourcegitcommit: 295d940a345879b3dfc5991e387b91c7257019ea
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/01/2019
ms.locfileid: "2696985"
---
# <a name="add-a-favicon"></a><span data-ttu-id="cd3e2-103">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="cd3e2-103">Add a favicon</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="cd3e2-104">I dette emne forklares det, hvordan du føjer et favoritikon til webstedet.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-104">This topic explains how to add a favicon to your site.</span></span>

## <a name="overview"></a><span data-ttu-id="cd3e2-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="cd3e2-105">Overview</span></span>

<span data-ttu-id="cd3e2-106">Et favoritikon er en lille grafikfil, der bl.a. vises under en webbrowserfane, på adresselinjen, i browserhistorikken og i bogmærker eller favoritter.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-106">A favicon is a small graphics file that is shown on a web browser tab, in the Address bar, in the browsing history, and in bookmarks or favorites, among other places.</span></span> <span data-ttu-id="cd3e2-107">Det anbefales, at du føjer et favoritikon til dit websted, fordi det repræsenterer og forstærker dit varemærke og hjælper med at skelne dit websted fra andre websteder, som kunderne besøger.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-107">We recommend that you add a favicon to your site, because it represents and reinforces your brand, and helps distinguish your site from other sites that your customers visit.</span></span>

<span data-ttu-id="cd3e2-108">Du kan føje flere favoritikoner med forskellig størrelse og filtype til webstedet, men i dette emne vises det, hvordan du tilføjer et enkelt favoritikon.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-108">Although you can add multiple favicons of various sizes and file types to your site, this topic shows how to add a single favicon.</span></span> <span data-ttu-id="cd3e2-109">Du bruger imidlertid den samme proces og placering ved tilføjelse af flere favoritikoner.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-109">However, the same process and location are used to add more favicons.</span></span>

## <a name="upload-a-favicon-to-your-sites-asset-collection"></a><span data-ttu-id="cd3e2-110">Overføre et favoritikon til webstedets aktivsamling</span><span class="sxs-lookup"><span data-stu-id="cd3e2-110">Upload a favicon to your site's asset collection</span></span>

<span data-ttu-id="cd3e2-111">Benyt følgende fremgangsmåde for at overføre et favoritikon til webstedets aktivsamling.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-111">To upload a favicon to your site's asset collection, follow these steps.</span></span>

1. <span data-ttu-id="cd3e2-112">Gå til **Aktiver \> Overfør \> Overfør aktiver**.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-112">Go to **Assets \> Upload \> Upload assets**.</span></span>
1. <span data-ttu-id="cd3e2-113">Find og vælg favoritikonet i det lokale filsystem.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-113">Find and select the favicon on your local file system.</span></span>
1. <span data-ttu-id="cd3e2-114">Angiv en titel, og vælg derefter **OK**.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-114">Enter a title, and then select **OK**.</span></span> 
1. <span data-ttu-id="cd3e2-115">Kopiér favoritikonets offentlige URL-adresse i egenskabsruden til højre.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-115">In the property pane on the right, copy the public URL of the favicon.</span></span>

> [!NOTE]
> <span data-ttu-id="cd3e2-116">Hvis du ikke vælger indstillingen **Publicer aktiver efter overførsel**, skal du vende tilbage til siden **Aktiver** senere og publicere favoritikonet manuelt.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-116">If you don't select the **Publish assets after upload** option, you must return to **Assets** page and manually publish the favicon later.</span></span>

## <a name="create-the-html-for-the-favicon"></a><span data-ttu-id="cd3e2-117">Opret HTML-kode til favoritikonet</span><span class="sxs-lookup"><span data-stu-id="cd3e2-117">Create the HTML for the favicon</span></span>

<span data-ttu-id="cd3e2-118">Du opretter HTML-koden til favoritkonet ved hjælp af følgende HTML-kodestykke.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-118">To create the HTML for the favicon, use the following HTML snippet.</span></span> <span data-ttu-id="cd3e2-119">I attributten **href** skal du erstatte **"Public\_URL\_for\_your\_favicon"** med den offentlige URL-adresse, som du kopierede tidligere.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-119">For the **href** attribute, replace **"Public\_URL\_for\_your\_favicon"** with the public URL that you copied earlier.</span></span>

`<link rel="shortcut icon" href="Public_URL_for_your_favicon">`

## <a name="add-the-html-for-the-favicon-to-the-head-element-of-your-pages"></a><span data-ttu-id="cd3e2-120">Føj HTML-koden til favoritikonet til elementet \<head\> for dine sider</span><span class="sxs-lookup"><span data-stu-id="cd3e2-120">Add the HTML for the favicon to the \<head\> element of your pages</span></span>

<span data-ttu-id="cd3e2-121">Du føjer et favoritikon til dit websted ved at bruge samme fremgangsmåde, der bruges til at føje enhver HTML-type/ethvert HTML-script til elementet **\<head\>** for siderne på webstedet.</span><span class="sxs-lookup"><span data-stu-id="cd3e2-121">To add a favicon to your site, use the same procedure that is used to add any type of HTML or script to the **\<head\>** element of your site pages.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="cd3e2-122">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="cd3e2-122">Additional resources</span></span>

[<span data-ttu-id="cd3e2-123">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="cd3e2-123">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="cd3e2-124">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="cd3e2-124">Select a site theme</span></span>](select-site-theme.md)

[<span data-ttu-id="cd3e2-125">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="cd3e2-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="cd3e2-126">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="cd3e2-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="cd3e2-127">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="cd3e2-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="cd3e2-128">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="cd3e2-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

