---
title: Oversigt over prøveversionsmiljøet til Commerce
description: Dette emne indeholder en oversigt over prøveversionsmiljøet til Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 12/10/2019
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
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: 901583afde4739be5313fa129ff0e52f11326881
ms.sourcegitcommit: 610d5c3efadbaf11752b46f24680af619bcd70a6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/10/2019
ms.locfileid: "2906064"
---
# <a name="commerce-preview-environment-overview"></a><span data-ttu-id="37052-103">Oversigt over prøveversionsmiljøet til Commerce</span><span class="sxs-lookup"><span data-stu-id="37052-103">Commerce preview environment overview</span></span>

[!include [banner](includes/preview-banner.md)]
[!include [banner](includes/banner.md)]

<span data-ttu-id="37052-104">Dette emne indeholder en oversigt over prøveversionsmiljøet til Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="37052-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce preview environment.</span></span>

## <a name="overview"></a><span data-ttu-id="37052-105">Oversigt</span><span class="sxs-lookup"><span data-stu-id="37052-105">Overview</span></span>

<span data-ttu-id="37052-106">Commerce-prøveversionsmiljøet er et valgfrit altomfattende prøveversionsmiljø til Dynamics 365 Commerce, som gør det muligt for potentielle kunder at afprøve Commerce-produktet før dets generelle offentlige udgivelse.</span><span class="sxs-lookup"><span data-stu-id="37052-106">The Commerce preview environment is an optional end-to-end preview environment of Dynamics 365 Commerce that lets potential customers try out the Commerce product before its general release to the public.</span></span>

<span data-ttu-id="37052-107">Bortset fra nogle mindre begrænsninger, der ikke påvirker funktioner eller funktionalitet, giver Commerce-prøveversionsmiljøet den komplette Commerce-oplevelse og kan bruges af kunder og implementeringspartnere til at evaluere produktet, give feedback og foretage fit-/GAP-analyse.</span><span class="sxs-lookup"><span data-stu-id="37052-107">Aside from some minor limitations that don't affect features or functionality, the Commerce preview environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-preview-environment"></a><span data-ttu-id="37052-108">Begrænsninger i Commerce-prøveversionsmiljøet</span><span class="sxs-lookup"><span data-stu-id="37052-108">Limitations of the Commerce preview environment</span></span>

<span data-ttu-id="37052-109">Selvom Commerce-prøveversionsmiljøet indeholder det komplette sæt af Commerce-funktioner og -funktionalitet, er der nogle mindre begrænsninger:</span><span class="sxs-lookup"><span data-stu-id="37052-109">Although the Commerce preview environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="37052-110">Selv om Commerce-prøveversionsmiljøet i sig selv ikke har nogen geografiske begrænsning, kan miljøets komponenter, såsom Retail Cloud Scale Unit (RCSU) og e-Commerce-programmer, kun klargøres i USA.</span><span class="sxs-lookup"><span data-stu-id="37052-110">Although the Commerce preview environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, can be provisioned only in the United States.</span></span>
- <span data-ttu-id="37052-111">Anvendelse af Commerce-prøveversionsmiljøet er begrænset til 30 dage fra datoen for klargøringen af e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="37052-111">Use of the Commerce preview environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="37052-112">Commerce-prøveversionsmiljøet kan kun implementeres og initialiseres i et miljø, der bruger demotopologien, hvor alle komponenter i et miljø installeres i en enkelt virtuel maskine (VM).</span><span class="sxs-lookup"><span data-stu-id="37052-112">The Commerce preview environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed in a single virtual machine (VM).</span></span> <span data-ttu-id="37052-113">Den væsentligste begrænsning for denne VM-topologi med én boks er antallet af brugere, som prøveversionsmiljøet kan understøtte samtidig.</span><span class="sxs-lookup"><span data-stu-id="37052-113">The main limitation of this OneBox VM topology is the number of concurrent users that the preview environment can support.</span></span>
- <span data-ttu-id="37052-114">Commerce-prøveversionsmiljøet kan kun evalueres indtil Commerce-produktet gøres generelt tilgængeligt (GA).</span><span class="sxs-lookup"><span data-stu-id="37052-114">The Commerce preview environment can be evaluated only until the general availability (GA) of the Commerce product.</span></span> <span data-ttu-id="37052-115">Nye demo-miljøer vil være tilgængelige efter GA.</span><span class="sxs-lookup"><span data-stu-id="37052-115">New demo environments will be available after GA.</span></span>

## <a name="get-started"></a><span data-ttu-id="37052-116">Introduktion</span><span class="sxs-lookup"><span data-stu-id="37052-116">Get started</span></span>

<span data-ttu-id="37052-117">Hvis du vil klargør Commerce-prøveversionsmiljøet se [Klargøring af et Commerce-prøveversionsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="37052-117">To provision the Commerce preview environment, see [Provision a Commerce preview environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="37052-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="37052-118">Additional resources</span></span>

[<span data-ttu-id="37052-119">Klargøring af et Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="37052-119">Provision a Commerce preview environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="37052-120">Konfigurering af et Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="37052-120">Configure a Commerce preview environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="37052-121">Konfigurer valgfrie funktioner for et Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="37052-121">Configure optional features for a Commerce preview environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="37052-122">Ofte stillede spørgsmål om Commerce-prøveversionsmiljø</span><span class="sxs-lookup"><span data-stu-id="37052-122">Commerce preview environment FAQ</span></span>](cpe-faq.md)
