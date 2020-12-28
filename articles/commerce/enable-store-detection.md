---
title: Aktivere registrering af lokationsbaserede butikker
description: I dette emne beskrives, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.
author: brianshook
manager: annbe
ms.date: 07/02/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.search.scope: Operations, Retail, Core
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: brshoo
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: f87d29a8cffb70e4dea211cea7538e5e4c85295c
ms.sourcegitcommit: 4bf5ae2f2f144a28e431ed574c7e8438dc5935de
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/13/2020
ms.locfileid: "4517300"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="155de-103">Aktivere registrering af lokationsbaserede butikker</span><span class="sxs-lookup"><span data-stu-id="155de-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="155de-104">I dette emne beskrives, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="155de-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="155de-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="155de-105">Overview</span></span>

<span data-ttu-id="155de-106">Med registrering af lokationsbaserede butikker i Commerce kan du levere relevant webstedsindhold til kunderne på baggrund af deres placering.</span><span class="sxs-lookup"><span data-stu-id="155de-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="155de-107">Hvis registrering af lokationsbaserede butikker er slået til, bruger Commerce-gengivelsestjenesten land/område-oplysningerne fra IP-adressen på kundens webbrowser til at dirigere kunden til den bedst mulige geografiske lokationskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="155de-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="155de-108">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="155de-108">Privacy notice</span></span>

<span data-ttu-id="155de-109">Hvis du slår funktionen til registrering af lokationsbaserede butikker til, sendes oplysninger fra kundens browser til en Microsoft-lokationstjeneste.</span><span class="sxs-lookup"><span data-stu-id="155de-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="155de-110">Disse oplysninger bruges derefter til at angive det kundeindhold, der er relevant for det sted, hvor vedkommende befinder sig.</span><span class="sxs-lookup"><span data-stu-id="155de-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="155de-111">Både de oplysninger, der sendes fra kundens browser, og de lokationsbaserede oplysninger, der returneres til kunden, kræver overholdelse af politikker om beskyttelse af personlige oplysninger og politikker om cookies.</span><span class="sxs-lookup"><span data-stu-id="155de-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="155de-112">Aktivere registrering af lokationsbaserede butikker</span><span class="sxs-lookup"><span data-stu-id="155de-112">Turn on location-based store detection</span></span>

<span data-ttu-id="155de-113">Udfør følgende trin for at aktivere registrering af lokationsbaserede butikker i Commerce.</span><span class="sxs-lookup"><span data-stu-id="155de-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="155de-114">Gå til dit websted i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="155de-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="155de-115">Vælg **Administration af websted** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="155de-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="155de-116">Vælg **Indstillinger for websted**.</span><span class="sxs-lookup"><span data-stu-id="155de-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="155de-117">Vælg **Til** i indstillingen **Aktivere registrering af lokationsbaseret lager**.</span><span class="sxs-lookup"><span data-stu-id="155de-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="155de-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="155de-118">Additional resources</span></span>

[<span data-ttu-id="155de-119">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="155de-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="155de-120">Implementere en ny e-handelslejer</span><span class="sxs-lookup"><span data-stu-id="155de-120">Deploy a new e-commerce tenant</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="155de-121">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="155de-121">Create an e-commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="155de-122">Tilknytte et Dynamics 365 Commerce-websted til en onlinekanal</span><span class="sxs-lookup"><span data-stu-id="155de-122">Associate a Dynamics 365 Commerce site with an online channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="155de-123">Administrere robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="155de-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="155de-124">Masseoverføre omdirigeringer af URL-adresser</span><span class="sxs-lookup"><span data-stu-id="155de-124">Upload URL redirects in bulk</span></span>](upload-bulk-redirects.md)

[<span data-ttu-id="155de-125">Konfigurere en B2C-lejer i Commerce</span><span class="sxs-lookup"><span data-stu-id="155de-125">Set up a B2C tenant in Commerce</span></span>](set-up-B2C-tenant.md)

[<span data-ttu-id="155de-126">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="155de-126">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="155de-127">Konfigurere flere B2C-lejere i et Commerce-miljø</span><span class="sxs-lookup"><span data-stu-id="155de-127">Configure multiple B2C tenants in a Commerce environment</span></span>](configure-multi-B2C-tenants.md)

[<span data-ttu-id="155de-128">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="155de-128">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
