---
title: Vælg et tema for webstedet
description: Dette emne indeholder en beskrivelse af, hvordan du kan angive eller ændre webstedets tema i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
manager: annbe
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 66fcff9fa18d3c98e022ef91d15903fbba8b6b61
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4982390"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="343f6-103">Vælg et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="343f6-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="343f6-104">Dette emne indeholder en beskrivelse af, hvordan du kan angive eller ændre webstedets tema i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="343f6-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="343f6-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="343f6-105">Overview</span></span>

<span data-ttu-id="343f6-106">Layout og typografi til et websted (f.eks. skrifttyper, størrelser og farver) defineres af det tema, du vælger, og gælder for webstedet.</span><span class="sxs-lookup"><span data-stu-id="343f6-106">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="343f6-107">Et tema oprettes og implementeres af en udvikler i firmaet.</span><span class="sxs-lookup"><span data-stu-id="343f6-107">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="343f6-108">Du kan finde en oversigt over temaer under [Oversigt over temaer](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="343f6-108">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="343f6-109">Du kan finde flere oplysninger om, hvordan du opretter og anvender temaer, under [Oprette et nyt tema](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="343f6-109">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="343f6-110">Når du første gang opretter et websted, bruger det som standard et tema med navnet **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="343f6-110">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="343f6-111">Dette standardtema findes som en del af Commerce-modulbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="343f6-111">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="343f6-112">Når du har implementeret yderligere temaer for dit websted, kan du konfigurere webstedet, så det bruger et af dem i stedet.</span><span class="sxs-lookup"><span data-stu-id="343f6-112">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="343f6-113">Vælge temaet for webstedet</span><span class="sxs-lookup"><span data-stu-id="343f6-113">Select the site theme</span></span>

<span data-ttu-id="343f6-114">Udfør følgende trin for at vælge det tema, der anvendes på webstedet.</span><span class="sxs-lookup"><span data-stu-id="343f6-114">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="343f6-115">Gå til dit websted i webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="343f6-115">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="343f6-116">Gå til **Administration af websted** \> **Udvidelsesmuligheder**.</span><span class="sxs-lookup"><span data-stu-id="343f6-116">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="343f6-117">Vælg et tema i rullemenuen under **Tema**.</span><span class="sxs-lookup"><span data-stu-id="343f6-117">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="343f6-118">Vælg **Gem og udgiv** for at anvende det valgte tema på webstedet.</span><span class="sxs-lookup"><span data-stu-id="343f6-118">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="343f6-119">Det tema, du vælger, udgives på webstedet, så snart du vælger **Gem og udgiv** på siden **Udvidelsesmuligheder**.</span><span class="sxs-lookup"><span data-stu-id="343f6-119">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="343f6-120">Hvis du vil se et tema på webstedet, før du anvender det, kan du bruge dit udviklings- eller sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="343f6-120">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="343f6-121">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="343f6-121">Additional resources</span></span>

[<span data-ttu-id="343f6-122">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="343f6-122">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="343f6-123">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="343f6-123">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="343f6-124">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="343f6-124">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="343f6-125">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="343f6-125">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="343f6-126">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="343f6-126">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="343f6-127">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="343f6-127">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="343f6-128">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="343f6-128">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="343f6-129">Oversigt over temaer</span><span class="sxs-lookup"><span data-stu-id="343f6-129">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="343f6-130">Opret et nyt tema</span><span class="sxs-lookup"><span data-stu-id="343f6-130">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)

