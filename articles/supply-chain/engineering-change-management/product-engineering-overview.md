---
title: Oversigt over teknisk ændringsstyring
description: Dette emne giver en oversigt over teknisk ændringsstyring, som hjælper dig med at planlægge og administrere produktversioner og administrere produktlivscyklusser og tekniske ændringer.
author: t-benebo
ms.date: 11/11/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: benebotg
ms.search.validFrom: 2020-09-28
ms.dyn365.ops.version: Release 10.0.15
ms.openlocfilehash: d7c0839ffbea80904ca12d1cba7ba9880f721cdd
ms.sourcegitcommit: 57668404d61359b33e0c0280f2f7c4eb829b1ed2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/27/2021
ms.locfileid: "5947514"
---
# <a name="engineering-change-management-overview"></a><span data-ttu-id="b87ab-103">Oversigt over teknisk ændringsstyring</span><span class="sxs-lookup"><span data-stu-id="b87ab-103">Engineering change management overview</span></span>

[!include [banner](../includes/banner.md)]

## <a name="feature-summary"></a><span data-ttu-id="b87ab-104">Oversigt over funktioner</span><span class="sxs-lookup"><span data-stu-id="b87ab-104">Feature summary</span></span>

<span data-ttu-id="b87ab-105">Moderne producenter kræver omfattende administration af produktdata, versionsstyring og styring af teknisk ændring for at opnå succes i en verden med konstant kortere produktlivscyklusser, højere kvalitets- og pålidelighedskrav og større fokus på produktsikkerhed.</span><span class="sxs-lookup"><span data-stu-id="b87ab-105">Today's manufacturers require strong product data management, version control, and engineering change management to succeed in a world of constantly shrinking product lifecycles, increased quality and reliability requirements, and an increased focus on product safety.</span></span>

<span data-ttu-id="b87ab-106">Styring af tekniske ændringer bringer strukturen og disciplinen til administrationsprocessen for produktdata og gør det muligt at definere, frigive og revidere produkter på en kontrolleret måde, der understøttes af arbejdsprocesser.</span><span class="sxs-lookup"><span data-stu-id="b87ab-106">Engineering change management brings structure and discipline to the product data management process, and enables products to be defined, released, and revised in a controlled manner that is supported by workflows.</span></span><span data-ttu-id="b87ab-107"> Ved hjælp af produktversioner og styring af tekniske ændringer kan du dokumentere, vurdere virkningen af og anvende tekniske ændringer under hele et produkts livscyklus.</span><span class="sxs-lookup"><span data-stu-id="b87ab-107"> Through product versions and engineering change management, you can document, assess the impact of, and apply engineering changes throughout the whole lifecycle of a product.</span></span>

<span data-ttu-id="b87ab-108">Teknisk ændringsstyring hjælper dig med at planlægge og administrere produktversioner og administrere produktlivscyklusser og tekniske ændringer.</span><span class="sxs-lookup"><span data-stu-id="b87ab-108">Engineering change management helps you plan and manage product versioning, and manage product lifecycles and engineering changes.</span></span> <span data-ttu-id="b87ab-109">Her er en oversigt over dens hovedfunktioner:</span><span class="sxs-lookup"><span data-stu-id="b87ab-109">Here is a list of its main features:</span></span>

- <span data-ttu-id="b87ab-110">Produktversioner</span><span class="sxs-lookup"><span data-stu-id="b87ab-110">Product versioning</span></span>
- <span data-ttu-id="b87ab-111">Forbedrede produktudgivelsesfunktioner, der giver dig mulighed for at vedligeholde produktmasterdata i én juridisk enhed (den tekniske virksomhed) og publicere det fuldt konfigurerede, frigivne produkt til andre juridiske enheder</span><span class="sxs-lookup"><span data-stu-id="b87ab-111">Enhanced product release functionality that lets you maintain product master data in one legal entity (the engineering company) and publish the fully configured released product to other legal entities</span></span>
- <span data-ttu-id="b87ab-112">Regler for validering af, at nødvendige oplysninger angives, før en produktversion aktiveres (parathedskontrol)</span><span class="sxs-lookup"><span data-stu-id="b87ab-112">Rules for validating that required information is entered before a product version is activated (readiness checks)</span></span>
- <span data-ttu-id="b87ab-113">Forbedret administration af produktets levetid med detaljeret styring af, hvornår et frigivet produkt kan bruges i bestemte forretningsprocesser</span><span class="sxs-lookup"><span data-stu-id="b87ab-113">Improved product lifecycle management through fine-grained control over when a released product can be used in specific business processes</span></span>
- <span data-ttu-id="b87ab-114">Tekniske ændringsanmodninger, der understøttes af arbejdsprocesser</span><span class="sxs-lookup"><span data-stu-id="b87ab-114">Engineering change requests that are supported by workflows</span></span>
- <span data-ttu-id="b87ab-115">Tekniske ændringsordrer, der understøttes af arbejdsprocesser</span><span class="sxs-lookup"><span data-stu-id="b87ab-115">Engineering change orders that are supported by workflows</span></span>

> [!VIDEO https://www.microsoft.com/en-us/videoplayer/embed/RE4HE6B]

<span data-ttu-id="b87ab-116">Den foregående video ([Styring af ændringer i Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) er inkluderet i den [Finance and Operations-afspilningsliste](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW), der er tilgængelig på YouTube.</span><span class="sxs-lookup"><span data-stu-id="b87ab-116">The preceding video ([Change management capabilities in Dynamics 365 Supply Chain Management](https://youtu.be/N313FqvRuBc)) is included in the [Finance and Operations playlist](https://www.youtube.com/playlist?list=PLcakwueIHoT_SYfIaPGoOhloFoCXiUSyW) available on YouTube.</span></span>

## <a name="turn-on-the-engineering-change-management-and-version-dimension-features-for-your-system"></a><span data-ttu-id="b87ab-117">Aktivere funktionerne til styring af tekniske ændringer og versionsdimension for systemet</span><span class="sxs-lookup"><span data-stu-id="b87ab-117">Turn on the engineering change management and version dimension features for your system</span></span>

<span data-ttu-id="b87ab-118">Før du kan bruge styring af tekniske ændringer, skal du aktivere både funktionen *Styring af tekniske ændringer* og dens konfigurationsnøgle.</span><span class="sxs-lookup"><span data-stu-id="b87ab-118">Before you can use engineering change management, you must enable both the *Engineering Change Management* feature and its configuration key.</span></span> <span data-ttu-id="b87ab-119">Hvis du også vil spore versionsdimensionen for produkter i transaktioner (valgfrit), skal du også aktivere funktionen *Produktversionsdimension* og dens konfigurationsnøgle.</span><span class="sxs-lookup"><span data-stu-id="b87ab-119">If you also want to track the version dimension of products in transactions (optional), then you must also enable the *Product version dimension* feature and its configuration key.</span></span>

<span data-ttu-id="b87ab-120">Du skal først aktivere disse funktioner ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="b87ab-120">First, turn on the features by following these steps.</span></span>

1. <span data-ttu-id="b87ab-121">Gå til arbejdsområdet [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="b87ab-121">Go to the [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) workspace.</span></span>
1. <span data-ttu-id="b87ab-122">Søg efter opdateringer.</span><span class="sxs-lookup"><span data-stu-id="b87ab-122">Check for updates.</span></span>
1. <span data-ttu-id="b87ab-123">Aktivér den funktion, der hedder **Teknisk ændringsstyring**.</span><span class="sxs-lookup"><span data-stu-id="b87ab-123">Turn on the feature that is named **Engineering Change Management**.</span></span>
1. <span data-ttu-id="b87ab-124">Hvis du vil bruge den, skal du også aktivere funktionen med navnet **Produktdimensionsversion**.</span><span class="sxs-lookup"><span data-stu-id="b87ab-124">If you want to use it, then also turn on the feature that is named **Product dimension version**.</span></span>

<span data-ttu-id="b87ab-125">Du skal derefter aktivere konfigurationsnøglerne ved at følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="b87ab-125">Next, turn on the configuration keys by following these steps.</span></span>

1. <span data-ttu-id="b87ab-126">Sæt systemet i vedligeholdelsestilstand som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="b87ab-126">Put your system into maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>
1. <span data-ttu-id="b87ab-127">Gå til **Systemadministration \> Opsætning \> Licenskonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="b87ab-127">Go to **System administration \> Setup \> License configuration**.</span></span>
1. <span data-ttu-id="b87ab-128">Udvid noden **Handel**.</span><span class="sxs-lookup"><span data-stu-id="b87ab-128">Expand the **Trade** node.</span></span>
1. <span data-ttu-id="b87ab-129">Aktiver konfigurationsnøglen for hovedfunktionen ved at markere afkrydsningsfeltet **Styring af tekniske ændringer**.</span><span class="sxs-lookup"><span data-stu-id="b87ab-129">Enable the configuration key for the main feature by selecting the **Engineering Change Management** check box.</span></span> <span data-ttu-id="b87ab-130">(Det er ikke nødvendigt at udvide noden, medmindre du også vil deaktivere en eller begge af dens underfunktioner.)</span><span class="sxs-lookup"><span data-stu-id="b87ab-130">(It isn't necessary to expand the node unless you also want to disable one or both of its sub-features.)</span></span>
1. <span data-ttu-id="b87ab-131">Hvis du også vil bruge versionsdimensionen, skal du markere afkrydsningsfeltet **Produktdimension - Version**.</span><span class="sxs-lookup"><span data-stu-id="b87ab-131">If you also want to use the version dimension, then select the **Product dimension - Version** check box.</span></span> <span data-ttu-id="b87ab-132">(Dette afkrydsningsfelt er placeret længere nede på listen og er ikke indlejret under noden **Styring af tekniske ændringer**.)</span><span class="sxs-lookup"><span data-stu-id="b87ab-132">(This check box is further down the list, not nested under the **Engineering Change Management** node.)</span></span>
1. <span data-ttu-id="b87ab-133">Slå vedligeholdelsestilstand fra som beskrevet under [Vedligeholdelsestilstand](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span><span class="sxs-lookup"><span data-stu-id="b87ab-133">Turn off maintenance mode, as described in [Maintenance mode](../../fin-ops-core/dev-itpro/sysadmin/maintenance-mode.md).</span></span>

> [!IMPORTANT]
> <span data-ttu-id="b87ab-134">Fra april 2022 vil licensnøglerne til både **Styring af tekniske ændringer** og **Produktdimension – Version** som standard være aktiveret for alle nye installationer, men du vil stadig kunne deaktivere dem, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="b87ab-134">Starting in April 2022, the license keys for both **Engineering Change Management** and **Product dimension - Version** will be enabled by default for all new installations, but you will still be able to disable them if needed.</span></span>

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
