---
title: Påmindelsesmodul
description: Dette emne omhandler påmindelsesmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.
author: anupamar-ms
manager: annbe
ms.date: 10/31/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application User
ms.reviewer: v-chgri
ms.search.scope: Retail, Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: anupamar
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: ''
ms.openlocfilehash: 82138dd7f0934f732215f67a3726638eb87075d4
ms.sourcegitcommit: 3a4e137ef3a96ba0a58c5352f4a3b57467ace9ae
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/11/2019
ms.locfileid: "2785346"
---
# <a name="alert-module"></a><span data-ttu-id="a74b5-103">Påmindelsesmodul</span><span class="sxs-lookup"><span data-stu-id="a74b5-103">Alert module</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="a74b5-104">Dette emne omhandler påmindelsesmoduler og beskriver, hvordan du kan føje dem til sider på websteder i Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="a74b5-104">This topic covers alert modules and describes how to add them to site pages in Microsoft Dynamics 365 Commerce.</span></span>

## <a name="overview"></a><span data-ttu-id="a74b5-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="a74b5-105">Overview</span></span>

<span data-ttu-id="a74b5-106">Et påmindelsesmodul bruges til at vise indbyggede informationsmeddelelser på en side.</span><span class="sxs-lookup"><span data-stu-id="a74b5-106">An alert module is used to show inline informational messages on a page.</span></span> <span data-ttu-id="a74b5-107">Påmindelsesmoduler understøtter en sms-besked og et link.</span><span class="sxs-lookup"><span data-stu-id="a74b5-107">Alert modules support a text message and a link.</span></span> <span data-ttu-id="a74b5-108">De kan bruges til at vise kampagner for hele webstedet, som vises på alle sider på et websted for e-handel.</span><span class="sxs-lookup"><span data-stu-id="a74b5-108">They can be used to show site-wide promotions that appear on all pages of an e-Commerce site.</span></span> 

<span data-ttu-id="a74b5-109">Påmindelsesmoduler styres af data fra CMS-indholdsstyringssystemet (Content Management System) og kan placeres på en hvilken som helst side.</span><span class="sxs-lookup"><span data-stu-id="a74b5-109">Alert modules are driven by data from the content management system (CMS) and can be put on any page.</span></span>

## <a name="examples-of-alert-modules-in-e-commerce"></a><span data-ttu-id="a74b5-110">Eksempler på påmindelsesmoduler i e-handel</span><span class="sxs-lookup"><span data-stu-id="a74b5-110">Examples of alert modules in e-Commerce</span></span>

<span data-ttu-id="a74b5-111">Påmindelsesmoduler kan bruges i webstedets sidehoved til at angive kampagner eller meddelelser for hele webstedet.</span><span class="sxs-lookup"><span data-stu-id="a74b5-111">Alert modules can be used in the site header to indicate site-wide promotions or messages.</span></span> <span data-ttu-id="a74b5-112">Her er nogle eksempler:</span><span class="sxs-lookup"><span data-stu-id="a74b5-112">Here are some examples:</span></span>

<span data-ttu-id="a74b5-113">"Det årlige udsalg slutter om 10 dage"</span><span class="sxs-lookup"><span data-stu-id="a74b5-113">"Annual sale ends in 10 days"</span></span>

<span data-ttu-id="a74b5-114">"Store besparelser på skolestartudsalg.</span><span class="sxs-lookup"><span data-stu-id="a74b5-114">"Save big with back to school sale.</span></span> <span data-ttu-id="a74b5-115">Køb nu".</span><span class="sxs-lookup"><span data-stu-id="a74b5-115">Shop Now."</span></span>

## <a name="alert-module-properties"></a><span data-ttu-id="a74b5-116">Egenskaber for påmindelsesmodul</span><span class="sxs-lookup"><span data-stu-id="a74b5-116">Alert module properties</span></span>

| <span data-ttu-id="a74b5-117">Egenskabsbetegnelse</span><span class="sxs-lookup"><span data-stu-id="a74b5-117">Property name</span></span>  | <span data-ttu-id="a74b5-118">Værdi</span><span class="sxs-lookup"><span data-stu-id="a74b5-118">Value</span></span>                              | <span data-ttu-id="a74b5-119">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a74b5-119">Description</span></span> |
|----------------|------------------------------------|-------------|
| <span data-ttu-id="a74b5-120">Tekst</span><span class="sxs-lookup"><span data-stu-id="a74b5-120">Text</span></span>           | <span data-ttu-id="a74b5-121">Tekst</span><span class="sxs-lookup"><span data-stu-id="a74b5-121">Text</span></span>                               | <span data-ttu-id="a74b5-122">Den tekstmeddelelse, der vises i påmindelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="a74b5-122">The text message that appears in the alert module.</span></span> |
| <span data-ttu-id="a74b5-123">Tekstjustering</span><span class="sxs-lookup"><span data-stu-id="a74b5-123">Text alignment</span></span> | <span data-ttu-id="a74b5-124">**Højre**, **Venstre** eller **Centreret**</span><span class="sxs-lookup"><span data-stu-id="a74b5-124">**Right**, **Left**, or **Center**</span></span> | <span data-ttu-id="a74b5-125">En værdi, der definerer, hvordan tekst justeres i påmindelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="a74b5-125">A value that defines how text is aligned in the alert module.</span></span> |
| <span data-ttu-id="a74b5-126">Påmindelse for afvisning</span><span class="sxs-lookup"><span data-stu-id="a74b5-126">Dismiss alert</span></span>  | <span data-ttu-id="a74b5-127">**Sand** eller **Falsk**</span><span class="sxs-lookup"><span data-stu-id="a74b5-127">**True** or **False**</span></span>              | <span data-ttu-id="a74b5-128">Hvis værdien er angivet til **Sand**, kan kunden afvise påmindelsen.</span><span class="sxs-lookup"><span data-stu-id="a74b5-128">If the value is set to **True**, the customer can dismiss the alert.</span></span> |
| <span data-ttu-id="a74b5-129">Binding</span><span class="sxs-lookup"><span data-stu-id="a74b5-129">Link</span></span>           | <span data-ttu-id="a74b5-130">URL-adresse</span><span class="sxs-lookup"><span data-stu-id="a74b5-130">URL</span></span>                                | <span data-ttu-id="a74b5-131">URL-adressen for et valgfrit link.</span><span class="sxs-lookup"><span data-stu-id="a74b5-131">The URL for an optional link.</span></span> |

## <a name="add-an-alert-module-to-a-page"></a><span data-ttu-id="a74b5-132">Føj et påmindelsesmodul til en side</span><span class="sxs-lookup"><span data-stu-id="a74b5-132">Add an alert module to a page</span></span> 

<span data-ttu-id="a74b5-133">Hvis du vil føje et påmindelsesmodul til en side og angive de påkrævede egenskaber, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="a74b5-133">To add an alert module to a page and set the required properties, follow these steps.</span></span>

1. <span data-ttu-id="a74b5-134">Opret en sideskabelon med navnet **påmindelsesskabelon**.</span><span class="sxs-lookup"><span data-stu-id="a74b5-134">Create a page template that is named **alert template**.</span></span>
1. <span data-ttu-id="a74b5-135">Tilføj et påmindelsesmodul på pladsen **Hoved** på standardsiden.</span><span class="sxs-lookup"><span data-stu-id="a74b5-135">In the **Main** slot of the default page, add an alert module.</span></span>
1. <span data-ttu-id="a74b5-136">Tjek skabelonen ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="a74b5-136">Check in the template, and publish it.</span></span> 
1. <span data-ttu-id="a74b5-137">Brug den påmindelsesskabelon, som du netop har oprettet, til at oprette en side med navnet **påmindelsesside**.</span><span class="sxs-lookup"><span data-stu-id="a74b5-137">Use the alert template that you just created to create a page that is named **alert page**.</span></span> 
1. <span data-ttu-id="a74b5-138">Tilføj et påmindelsesmodul på pladsen **Hoved** på den nye side.</span><span class="sxs-lookup"><span data-stu-id="a74b5-138">In the **Main** slot of the new page, add an alert module.</span></span>
1. <span data-ttu-id="a74b5-139">Angiv påmindelsesteksten i indstillingerne for påmindelsesmodulet.</span><span class="sxs-lookup"><span data-stu-id="a74b5-139">In the settings for the alert module, enter the alert text.</span></span> <span data-ttu-id="a74b5-140">Du kan redigere de andre egenskaber, hvis du vil tilpasse påmindelsesmodulet yderligere.</span><span class="sxs-lookup"><span data-stu-id="a74b5-140">You can edit the other properties if you want to customize the alert module further.</span></span>
1. <span data-ttu-id="a74b5-141">Gem siden, og se en forhåndsvisning af den.</span><span class="sxs-lookup"><span data-stu-id="a74b5-141">Save and preview the page.</span></span> <span data-ttu-id="a74b5-142">Øverst på siden kan du se en påmindelse med den tekst, du har tilføjet.</span><span class="sxs-lookup"><span data-stu-id="a74b5-142">At the top of the page, you should see an alert that has the text that you added.</span></span>
1. <span data-ttu-id="a74b5-143">Tjek siden ind, og publicer den.</span><span class="sxs-lookup"><span data-stu-id="a74b5-143">Check in the page, and publish it.</span></span> 

## <a name="additional-resources"></a><span data-ttu-id="a74b5-144">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="a74b5-144">Additional resources</span></span>

[<span data-ttu-id="a74b5-145">Oversigt over startsæt</span><span class="sxs-lookup"><span data-stu-id="a74b5-145">Starter kit overview</span></span>](starter-kit-overview.md)

[<span data-ttu-id="a74b5-146">Karruselmodul</span><span class="sxs-lookup"><span data-stu-id="a74b5-146">Carousel module</span></span>](add-carousel.md)

[<span data-ttu-id="a74b5-147">Indholdsrig blok-modul</span><span class="sxs-lookup"><span data-stu-id="a74b5-147">Content rich block module</span></span>](add-content-rich-block.md)

[<span data-ttu-id="a74b5-148">Indholdsplaceringsmodul</span><span class="sxs-lookup"><span data-stu-id="a74b5-148">Content placement module</span></span>](add-content-placement-modules.md)

[<span data-ttu-id="a74b5-149">Funktionsmodul</span><span class="sxs-lookup"><span data-stu-id="a74b5-149">Feature module</span></span>](add-feature-module.md)

[<span data-ttu-id="a74b5-150">Hero-modul</span><span class="sxs-lookup"><span data-stu-id="a74b5-150">Hero module</span></span>](add-hero-module.md)

[<span data-ttu-id="a74b5-151">Videoafspillermodul</span><span class="sxs-lookup"><span data-stu-id="a74b5-151">Video player module</span></span>](add-video-player.md)
