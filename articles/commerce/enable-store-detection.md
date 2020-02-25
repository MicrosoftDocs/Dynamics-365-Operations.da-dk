---
title: Aktivere registrering af lokationsbaserede butikker
description: I dette emne beskrives, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.
author: brianshook
manager: annbe
ms.date: 10/01/2019
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
ms.openlocfilehash: 304d8d2f05916295b9c6320561d6a25ff40df955
ms.sourcegitcommit: 81a647904dd305c4be2e4b683689f128548a872d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/01/2020
ms.locfileid: "3003088"
---
# <a name="enable-location-based-store-detection"></a><span data-ttu-id="5439c-103">Aktivere registrering af lokationsbaserede butikker</span><span class="sxs-lookup"><span data-stu-id="5439c-103">Enable location-based store detection</span></span>


[!include [banner](includes/banner.md)]

<span data-ttu-id="5439c-104">I dette emne beskrives, hvordan du aktiverer registrering af lokationsbaserede butikker for dit Dynamics 365 Commerce-websted.</span><span class="sxs-lookup"><span data-stu-id="5439c-104">This topic describes how to turn on location-based store detection for your Dynamics 365 Commerce site.</span></span>

## <a name="overview"></a><span data-ttu-id="5439c-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="5439c-105">Overview</span></span>

<span data-ttu-id="5439c-106">Med registrering af lokationsbaserede butikker i Commerce kan du levere relevant webstedsindhold til kunderne på baggrund af deres placering.</span><span class="sxs-lookup"><span data-stu-id="5439c-106">Location-based store detection in Commerce lets you provide relevant site content to customers, based on their location.</span></span> <span data-ttu-id="5439c-107">Hvis registrering af lokationsbaserede butikker er slået til, bruger Commerce-gengivelsestjenesten lande-/områdeoplysningerne fra IP-adressen på kundens webbrowser til at dirigere kunden til den bedst mulige geografiske lokationskonfiguration.</span><span class="sxs-lookup"><span data-stu-id="5439c-107">When location-based store detection is turned on, the Commerce rendering service uses the country/region information from the IP address of the customer's web browser to direct the customer to the best geographical site configuration that is available.</span></span>

## <a name="privacy-notice"></a><span data-ttu-id="5439c-108">Erklæring om beskyttelse af personlige oplysninger</span><span class="sxs-lookup"><span data-stu-id="5439c-108">Privacy notice</span></span>

<span data-ttu-id="5439c-109">Hvis du slår funktionen til registrering af lokationsbaserede butikker til, sendes oplysninger fra kundens browser til en Microsoft-lokationstjeneste.</span><span class="sxs-lookup"><span data-stu-id="5439c-109">If you turn on the location-based store detection feature, information from the customer's browser is sent to a Microsoft location service.</span></span> <span data-ttu-id="5439c-110">Disse oplysninger bruges derefter til at angive det kundeindhold, der er relevant for det sted, hvor vedkommende befinder sig.</span><span class="sxs-lookup"><span data-stu-id="5439c-110">This information is then used to provide the customer content that is relevant to his or her location.</span></span> <span data-ttu-id="5439c-111">Både de oplysninger, der sendes fra kundens browser, og de lokationsbaserede oplysninger, der returneres til kunden, kræver overholdelse af politikker om beskyttelse af personlige oplysninger og politikker om cookies.</span><span class="sxs-lookup"><span data-stu-id="5439c-111">Both the information that is sent from the customer's browser and the location-based information that is returned to the customer are subject to privacy and cookie compliance policies.</span></span>

## <a name="turn-on-location-based-store-detection"></a><span data-ttu-id="5439c-112">Aktivere registrering af lokationsbaserede butikker</span><span class="sxs-lookup"><span data-stu-id="5439c-112">Turn on location-based store detection</span></span>

<span data-ttu-id="5439c-113">Udfør følgende trin for at aktivere registrering af lokationsbaserede butikker i Commerce.</span><span class="sxs-lookup"><span data-stu-id="5439c-113">To turn on location-based store detection in Commerce, follow these steps.</span></span>

1. <span data-ttu-id="5439c-114">Gå til dit websted i oprettelsesværktøjet.</span><span class="sxs-lookup"><span data-stu-id="5439c-114">In the authoring tool, go to your site.</span></span>
1. <span data-ttu-id="5439c-115">Vælg **Administration af websted** i navigationsruden til venstre.</span><span class="sxs-lookup"><span data-stu-id="5439c-115">In the navigation pane on the left, select **Site Management**.</span></span>
1. <span data-ttu-id="5439c-116">Vælg **Indstillinger for websted**.</span><span class="sxs-lookup"><span data-stu-id="5439c-116">Select **Site Settings**.</span></span>
1. <span data-ttu-id="5439c-117">Vælg **Til** i indstillingen **Aktivere registrering af lokationsbaseret lager**.</span><span class="sxs-lookup"><span data-stu-id="5439c-117">Set the **Enable location based store detection** option to **On**.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="5439c-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="5439c-118">Additional resources</span></span>

[<span data-ttu-id="5439c-119">Konfigurere dit domænenavn</span><span class="sxs-lookup"><span data-stu-id="5439c-119">Configure your domain name</span></span>](configure-your-domain-name.md)

[<span data-ttu-id="5439c-120">Implementere et nyt websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="5439c-120">Deploy a new e-Commerce site</span></span>](deploy-ecommerce-site.md)

[<span data-ttu-id="5439c-121">Oprette et websted for e-handel</span><span class="sxs-lookup"><span data-stu-id="5439c-121">Create an e-Commerce site</span></span>](create-ecommerce-site.md)

[<span data-ttu-id="5439c-122">Tilknytte et onlinewebsted til en kanal</span><span class="sxs-lookup"><span data-stu-id="5439c-122">Associate an online site with a channel</span></span>](associate-site-online-store.md)

[<span data-ttu-id="5439c-123">Administrer robots.txt-filer</span><span class="sxs-lookup"><span data-stu-id="5439c-123">Manage robots.txt files</span></span>](manage-robots-txt-files.md)

[<span data-ttu-id="5439c-124">Konfigurere brugerdefinerede sider til brugerlogon</span><span class="sxs-lookup"><span data-stu-id="5439c-124">Set up custom pages for user logins</span></span>](custom-pages-user-logins.md)

[<span data-ttu-id="5439c-125">Tilføje understøttelse af et netværk, der leverer indhold (CDN)</span><span class="sxs-lookup"><span data-stu-id="5439c-125">Add support for a content delivery network (CDN)</span></span>](add-cdn-support.md)
