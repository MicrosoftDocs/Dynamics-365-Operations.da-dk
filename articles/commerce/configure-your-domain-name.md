---
title: Konfigurere dit domænenavn
description: I dette emne beskrives, hvordan du kan konfigurere et domænenavn for et Microsoft Dynamics 365 e-handelswebsted.
author: psimolin
manager: AnnBe
ms.date: 10/01/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Core, Operations, Retail
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 8f73c034563fb1cc6b05091b4c47e2a788d1a8b6
ms.sourcegitcommit: ef3a1d7527311d00b69a1072ae5eb021ce68034c
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/09/2020
ms.locfileid: "2945530"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="585f7-103">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="585f7-103">Configure your domain name</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="585f7-104">I dette emne beskrives, hvordan du kan konfigurere et domænenavn for et Microsoft Dynamics 365 e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="585f7-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="585f7-105">Tilføje domæner under initialisering af e-handel</span><span class="sxs-lookup"><span data-stu-id="585f7-105">Add domains during e-Commerce initialization</span></span>

<span data-ttu-id="585f7-106">Hvis du vil knytte domæner til e-handelsmiljøet, skal du initialisere e-handel som beskrevet i [Implementere et nyt e-handelswebsted](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="585f7-106">To associate domains with your e-commerce environment, initialize e-Commerce as described in [Deploy a new e-Commerce site](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="585f7-107">Under initialiseringen bliver du bedt om at angive oplysninger, der skal bruges til at klargøre e-handelsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="585f7-107">During initialization, you're asked to provide information that will be used to provision your e-Commerce environment.</span></span> <span data-ttu-id="585f7-108">Tilføj alle de domæner, du planlægger at bruge til dette miljø, i feltet **Understøttede værtsnavne**.</span><span class="sxs-lookup"><span data-stu-id="585f7-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="585f7-109">Flere domæner skal adskilles med semikolon.</span><span class="sxs-lookup"><span data-stu-id="585f7-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="585f7-110">På denne måde konfigureres domænerne i alle de påkrævede e-handelskomponenter, og de er klar til at blive brugt, når du skifter trafik fra CDN (Content Delivery Network) eller webserveren og peger på dem i e-handelsbutikkerne.</span><span class="sxs-lookup"><span data-stu-id="585f7-110">In this way, the domains are configured in all the required e-Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-Commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="585f7-111">Tilføje domæner efter initialisering af e-handel</span><span class="sxs-lookup"><span data-stu-id="585f7-111">Add domains after e-Commerce initialization</span></span>

<span data-ttu-id="585f7-112">Hvis du vil knytte nye domæner til e-handelsmiljøet efter e-handelsinitialiseringen, skal du sende en serviceanmodning.</span><span class="sxs-lookup"><span data-stu-id="585f7-112">To associate new domains with your e-Commerce environment after e-Commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="585f7-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="585f7-113">Additional resources</span></span>

[<span data-ttu-id="585f7-114">Implementere et nyt websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="585f7-114">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="585f7-115">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="585f7-115">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="585f7-116">Tilknytte et onlinewebsted til en kanal</span><span class="sxs-lookup"><span data-stu-id="585f7-116">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="585f7-117">Administrer robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="585f7-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="585f7-118">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="585f7-118">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="585f7-119">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="585f7-119">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="585f7-120">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="585f7-120">Enable location-based store detection</span></span>](enable-store-detection.md)
