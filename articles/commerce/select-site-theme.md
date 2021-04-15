---
title: Vælg et tema for webstedet
description: Dette emne indeholder en beskrivelse af, hvordan du kan angive eller ændre webstedets tema i Microsoft Dynamics 365 Commerce.
author: bicyclingfool
ms.date: 09/15/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: StuHarg
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 1e11e2ffafa29dfe4ad7a4a8e4d14e9d7c74c31f
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5794061"
---
# <a name="select-a-site-theme"></a><span data-ttu-id="a0777-103">Vælge et tema for webstedet</span><span class="sxs-lookup"><span data-stu-id="a0777-103">Select a site theme</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="a0777-104">Dette emne indeholder en beskrivelse af, hvordan du kan angive eller ændre webstedets tema i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a0777-104">This topic describes how to set or change your site's theme in Microsoft Dynamics 365 Commerce.</span></span>

<span data-ttu-id="a0777-105">Layout og typografi til et websted (f.eks. skrifttyper, størrelser og farver) defineres af det tema, du vælger, og gælder for webstedet.</span><span class="sxs-lookup"><span data-stu-id="a0777-105">A site's layout and style (for example, fonts, sizes, and colors) are defined by the theme that you select and apply to the site.</span></span> <span data-ttu-id="a0777-106">Et tema oprettes og implementeres af en udvikler i firmaet.</span><span class="sxs-lookup"><span data-stu-id="a0777-106">A theme is created and deployed by a developer at your company.</span></span> <span data-ttu-id="a0777-107">Du kan finde en oversigt over temaer under [Oversigt over temaer](e-commerce-extensibility/theming.md).</span><span class="sxs-lookup"><span data-stu-id="a0777-107">For an overview of themes, see [Theming overview](e-commerce-extensibility/theming.md).</span></span> <span data-ttu-id="a0777-108">Du kan finde flere oplysninger om, hvordan du opretter og anvender temaer, under [Oprette et nyt tema](e-commerce-extensibility/create-theme.md).</span><span class="sxs-lookup"><span data-stu-id="a0777-108">For more information about how to create and deploy themes, see [Create a new theme](e-commerce-extensibility/create-theme.md).</span></span>

<span data-ttu-id="a0777-109">Når du første gang opretter et websted, bruger det som standard et tema med navnet **Fabrikam**.</span><span class="sxs-lookup"><span data-stu-id="a0777-109">By default, when you first create a site, it uses a theme that is named **Fabrikam**.</span></span> <span data-ttu-id="a0777-110">Dette standardtema findes som en del af Commerce-modulbiblioteket.</span><span class="sxs-lookup"><span data-stu-id="a0777-110">This default theme is provided as part of the Commerce module library.</span></span> <span data-ttu-id="a0777-111">Når du har implementeret yderligere temaer for dit websted, kan du konfigurere webstedet, så det bruger et af dem i stedet.</span><span class="sxs-lookup"><span data-stu-id="a0777-111">After you've deployed additional themes for your site, you can configure the site so that it uses one of them instead.</span></span>

## <a name="select-the-site-theme"></a><span data-ttu-id="a0777-112">Vælge temaet for webstedet</span><span class="sxs-lookup"><span data-stu-id="a0777-112">Select the site theme</span></span>

<span data-ttu-id="a0777-113">Udfør følgende trin for at vælge det tema, der anvendes på webstedet.</span><span class="sxs-lookup"><span data-stu-id="a0777-113">To select the theme that is applied to your site, follow these steps.</span></span>

1. <span data-ttu-id="a0777-114">Gå til dit websted i webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="a0777-114">In the site authoring environment, go to your site.</span></span>
1. <span data-ttu-id="a0777-115">Gå til **Administration af websted** \> **Udvidelsesmuligheder**.</span><span class="sxs-lookup"><span data-stu-id="a0777-115">Go to **Site Management** \> **Extensibility**.</span></span>
1. <span data-ttu-id="a0777-116">Vælg et tema i rullemenuen under **Tema**.</span><span class="sxs-lookup"><span data-stu-id="a0777-116">Under **Theme**, select a theme on the drop-down menu.</span></span>
1. <span data-ttu-id="a0777-117">Vælg **Gem og udgiv** for at anvende det valgte tema på webstedet.</span><span class="sxs-lookup"><span data-stu-id="a0777-117">To apply the selected theme to your site, select **Save and publish**.</span></span>

> [!NOTE]
> <span data-ttu-id="a0777-118">Det tema, du vælger, udgives på webstedet, så snart du vælger **Gem og udgiv** på siden **Udvidelsesmuligheder**.</span><span class="sxs-lookup"><span data-stu-id="a0777-118">The theme that you select is published to your site as soon as you select **Save and publish** on the **Extensibility** page.</span></span> <span data-ttu-id="a0777-119">Hvis du vil se et tema på webstedet, før du anvender det, kan du bruge dit udviklings- eller sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="a0777-119">To preview a theme on your site before you apply it, you can use your development or sandbox environment.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="a0777-120">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a0777-120">Additional resources</span></span>

[<span data-ttu-id="a0777-121">Tilføj et logo</span><span class="sxs-lookup"><span data-stu-id="a0777-121">Add a logo</span></span>](add-logo.md)

[<span data-ttu-id="a0777-122">Arbejd med CSS-tilsidesættelsesfiler</span><span class="sxs-lookup"><span data-stu-id="a0777-122">Work with CSS override files</span></span>](css-override-files.md)

[<span data-ttu-id="a0777-123">Tilføj en favicon</span><span class="sxs-lookup"><span data-stu-id="a0777-123">Add a favicon</span></span>](add-favicon.md)

[<span data-ttu-id="a0777-124">Tilføj en velkomstmeddelelse</span><span class="sxs-lookup"><span data-stu-id="a0777-124">Add a welcome message</span></span>](add-welcome-message.md)

[<span data-ttu-id="a0777-125">Tilføj en copyright-meddelelse</span><span class="sxs-lookup"><span data-stu-id="a0777-125">Add a copyright notice</span></span>](add-copyright-notice.md)

[<span data-ttu-id="a0777-126">Føje sprog til webstedet</span><span class="sxs-lookup"><span data-stu-id="a0777-126">Add languages to your site</span></span>](add-languages-to-site.md)

[<span data-ttu-id="a0777-127">Tilføje scriptkode til sider på websteder for at understøtte telemetri</span><span class="sxs-lookup"><span data-stu-id="a0777-127">Add script code to site pages to support telemetry</span></span>](add-telemetry.md)

[<span data-ttu-id="a0777-128">Oversigt over temaer</span><span class="sxs-lookup"><span data-stu-id="a0777-128">Theming overview</span></span>](e-commerce-extensibility/theming.md)

[<span data-ttu-id="a0777-129">Opret et nyt tema</span><span class="sxs-lookup"><span data-stu-id="a0777-129">Create a new theme</span></span>](e-commerce-extensibility/create-theme.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]
