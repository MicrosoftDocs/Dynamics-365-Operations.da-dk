---
title: Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal
description: I dette emne forklares det, hvordan du kan binde dit Microsoft Dynamics 365 Commerce-websted til en eller flere onlinebutikker.
author: bicyclingfool
manager: AnnBe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ROBOTS: ''
audience: Application user
ms.reviewer: josaw
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.author: stuharg
ms.search.validFrom: 2019-09-30
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: fc93441bd09deccdb8c7ecf955c0ec5177c0b31e
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4980017"
---
# <a name="associate-a-dynamics-365-commerce-site-with-an-online-channel"></a><span data-ttu-id="e4dc5-103">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="e4dc5-103">Associate a Dynamics 365 Commerce site with an online channel</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="e4dc5-104">I dette emne forklares det, hvordan du kan binde dit Microsoft Dynamics 365 Commerce-websted til en eller flere onlinebutikker.</span><span class="sxs-lookup"><span data-stu-id="e4dc5-104">This topic explains how to bind your Microsoft Dynamics 365 Commerce site to one or more online stores.</span></span> 

<span data-ttu-id="e4dc5-105">Når du har klargjort dit Dynamics 365 Commerce-e-handelsmiljø ved hjælp af Microsoft Dynamics Lifecycle Services-portalen (LCS), er du klar til at oprette dit første e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="e4dc5-105">After you've provisioned your Dynamics 365 Commerce e-commerce environment by using the Microsoft Dynamics Lifecycle Services (LCS) portal, you're ready to establish your first e-commerce website.</span></span> <span data-ttu-id="e4dc5-106">Når du begynder at oprette et websted, kan du knytte webstedet til en onlinebutik, der er oprettet tidligere.</span><span class="sxs-lookup"><span data-stu-id="e4dc5-106">As part of the initial site creation, you associate the site with an online store that was previously created.</span></span> <span data-ttu-id="e4dc5-107">Dette trin binder webstedet til en onlinekanal og lader webstedet vise navigationshierarkiet, produkter, kategorier, priser, forsendelsesindstillinger og alt andet, du har defineret i onlinebutikken.</span><span class="sxs-lookup"><span data-stu-id="e4dc5-107">This step binds the site to an online channel and lets the site show the navigation hierarchy, products, categories, prices, shipping options, and everything else that you defined in the online store.</span></span>

<span data-ttu-id="e4dc5-108">Hvis du vil oprette et nyt websted og knytte en onlinebutik til det, skal du i LCS vælge linket til webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="e4dc5-108">To establish a new site and associate an online store with it, in LCS, select the link for the site authoring environment.</span></span> <span data-ttu-id="e4dc5-109">Vælg derefter **Nyt websted** på siden for webstedets oprettelsesmiljø.</span><span class="sxs-lookup"><span data-stu-id="e4dc5-109">Then, on the page for the site authoring environment, select **New site**.</span></span> <span data-ttu-id="e4dc5-110">I dialogboksen **Nyt websted** skal du angive nogle grundlæggende oplysninger om dit websted.</span><span class="sxs-lookup"><span data-stu-id="e4dc5-110">In the **New site** dialog box, you must provide some basic information about your site.</span></span> <span data-ttu-id="e4dc5-111">Du kan få en fuldstændig forklaring på de oplysninger, du skal angive, under [Oprette et nyt e-handelswebsted](create-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="e4dc5-111">For a complete explanation of the information that you must provide, see [Create a new e-commerce site](create-ecommerce-site.md).</span></span>

<span data-ttu-id="e4dc5-112">Når webstedet er oprettet, kan du kontrollere, om det er knyttet til din onlinebutik, ved at vælge fanen **Produkter**. Du bør kunne se det produktsortiment, der er tildelt til onlinebutikken.</span><span class="sxs-lookup"><span data-stu-id="e4dc5-112">After your site is created, you can verify that it's associated with your online store by selecting the **Products** tab. You should see the assortment of products that has been allocated to the online store.</span></span> <span data-ttu-id="e4dc5-113">Du kan også bruge rullefeltet øverst til venstre på siden til at få adgang til produkterne efter kategori.</span><span class="sxs-lookup"><span data-stu-id="e4dc5-113">You can also use the drop-down field in the upper left of the page to access the products by category.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e4dc5-114">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e4dc5-114">Additional resources</span></span>

[<span data-ttu-id="e4dc5-115">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="e4dc5-115">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="e4dc5-116">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="e4dc5-116">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="e4dc5-117">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="e4dc5-117">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="e4dc5-118">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="e4dc5-118">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="e4dc5-119">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="e4dc5-119">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="e4dc5-120">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="e4dc5-120">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="e4dc5-121">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="e4dc5-121">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="e4dc5-122">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="e4dc5-122">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="e4dc5-123">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="e4dc5-123">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="e4dc5-124">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="e4dc5-124">Enable location-based store detection</span></span>](enable-store-detection.md)
