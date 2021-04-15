---
title: Konfigurere dit domænenavn
description: I dette emne beskrives, hvordan du kan konfigurere et domænenavn for et Microsoft Dynamics 365 e-handelswebsted.
author: psimolin
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: Retail
ms.author: psimolin
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: 10.0.5
ms.openlocfilehash: 3d41168da44100a09c58b8c05367ab45bbd62a30
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5796045"
---
# <a name="configure-your-domain-name"></a><span data-ttu-id="b4238-103">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="b4238-103">Configure your domain name</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="b4238-104">I dette emne beskrives, hvordan du kan konfigurere et domænenavn for et Microsoft Dynamics 365 e-handelswebsted.</span><span class="sxs-lookup"><span data-stu-id="b4238-104">This topic explains how to configure a domain name for a Microsoft Dynamics 365 e-commerce site.</span></span> 

## <a name="add-domains-during-e-commerce-initialization"></a><span data-ttu-id="b4238-105">Tilføje domæner under initialisering af e-handel</span><span class="sxs-lookup"><span data-stu-id="b4238-105">Add domains during e-commerce initialization</span></span>

<span data-ttu-id="b4238-106">Hvis du vil knytte domæner til Dynamics 365 Commerce e-handelsmiljøet, skal du initialisere e-handel som beskrevet i [Implementere en ny e-handelslejer](deploy-ecommerce-site.md).</span><span class="sxs-lookup"><span data-stu-id="b4238-106">To associate domains with your Dynamics 365 Commerce e-commerce environment, initialize e-commerce as described in [Deploy a new e-commerce tenant](deploy-ecommerce-site.md).</span></span> <span data-ttu-id="b4238-107">Under initialiseringen bliver du bedt om at angive oplysninger, der skal bruges til at klargøre e-handelsmiljøet.</span><span class="sxs-lookup"><span data-stu-id="b4238-107">During initialization, you're asked to provide information that will be used to provision your e-commerce environment.</span></span> <span data-ttu-id="b4238-108">Tilføj alle de domæner, du planlægger at bruge til dette miljø, i feltet **Understøttede værtsnavne**.</span><span class="sxs-lookup"><span data-stu-id="b4238-108">In the **Supported host names** field, add all the domains that you plan to use with this environment.</span></span> <span data-ttu-id="b4238-109">Flere domæner skal adskilles med semikolon.</span><span class="sxs-lookup"><span data-stu-id="b4238-109">Multiple domains should be separated with semi-colon.</span></span> <span data-ttu-id="b4238-110">På denne måde konfigureres domænerne i alle de påkrævede e-handelskomponenter, og de er klar til at blive brugt, når du skifter trafik fra CDN (Content Delivery Network) eller webserveren og peger på dem i e-handelsbutikkerne.</span><span class="sxs-lookup"><span data-stu-id="b4238-110">In this way, the domains are configured in all the required Commerce components, and they are ready to be used when you switch traffic from your content delivery network (CDN) or web server and point it to the e-commerce front ends.</span></span>

## <a name="add-domains-after-e-commerce-initialization"></a><span data-ttu-id="b4238-111">Tilføje domæner efter initialisering af e-handel</span><span class="sxs-lookup"><span data-stu-id="b4238-111">Add domains after e-commerce initialization</span></span>

<span data-ttu-id="b4238-112">Hvis du vil knytte nye domæner til e-handelsmiljøet efter e-handelsinitialiseringen, skal du sende en serviceanmodning.</span><span class="sxs-lookup"><span data-stu-id="b4238-112">To associate new domains with your e-commerce environment after e-commerce initialization, you must submit a service request.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="b4238-113">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="b4238-113">Additional resources</span></span>

[<span data-ttu-id="b4238-114">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="b4238-114">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="b4238-115">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="b4238-115">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="b4238-116">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="b4238-116">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="b4238-117">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="b4238-117">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="b4238-118">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="b4238-118">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="b4238-119">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="b4238-119">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="b4238-120">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="b4238-120">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="b4238-121">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="b4238-121">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="b4238-122">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="b4238-122">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)

[<span data-ttu-id="b4238-123">Aktivere registrering af lokationsbaseret lager</span><span class="sxs-lookup"><span data-stu-id="b4238-123">Enable location-based store detection</span></span>](enable-store-detection.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]