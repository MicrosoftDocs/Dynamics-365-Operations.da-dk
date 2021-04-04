---
title: Konfigurere en Dynamics 365 Commerce-oversigt
description: Dette emne indeholder en oversigt over evalueringsmiljøet til Microsoft Dynamics 365 Commerce.
author: v-chgri
manager: annbe
ms.date: 07/16/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-commerce
ms.technology: ''
audience: Application user
ms.reviewer: v-chgri
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: v-chgri
ms.search.validFrom: 2019-12-10
ms.dyn365.ops.version: Release 10.0.5
ms.openlocfilehash: cc6bffba6ee402c6b48d6a3c8f8356eb32b5423b
ms.sourcegitcommit: c88b54ba13a4dfe39b844ffaced4dc435560c47d
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/19/2021
ms.locfileid: "5478014"
---
# <a name="dynamics-365-commerce-evaluation-environment-overview"></a><span data-ttu-id="76afc-103">Konfigurere en Dynamics 365 Commerce-oversigt</span><span class="sxs-lookup"><span data-stu-id="76afc-103">Dynamics 365 Commerce evaluation environment overview</span></span>

[!include [banner](includes/banner.md)]

<span data-ttu-id="76afc-104">Dette emne indeholder en oversigt over evalueringsmiljøet til Microsoft Dynamics 365 Commerce.</span><span class="sxs-lookup"><span data-stu-id="76afc-104">This topic gives an overview of the Microsoft Dynamics 365 Commerce evaluation environment.</span></span>

> [!NOTE]
> <span data-ttu-id="76afc-105">Miljøer til Commerce-evaluering er ikke generelt tilgængelige og tildeles til partnere og kunder efter anmodning.</span><span class="sxs-lookup"><span data-stu-id="76afc-105">Commerce evaluation environments aren't generally available, and are granted to partners and customers on a per-request basis.</span></span> <span data-ttu-id="76afc-106">Du kan få flere oplysninger ved at rette henvendelse til din kontakt hos din Microsoft-partner.</span><span class="sxs-lookup"><span data-stu-id="76afc-106">For more information, reach out to your Microsoft partner contact.</span></span>

<span data-ttu-id="76afc-107">Commerce-evalueringsmiljøet er et valgfrit altomfattende miljø til Dynamics 365 Commerce, som gør det muligt for partnere og potentielle kunder at afprøve Commerce-produktet.</span><span class="sxs-lookup"><span data-stu-id="76afc-107">The Commerce evaluation environment is an optional end-to-end environment of Dynamics 365 Commerce that lets partners and potential customers try out the Commerce product.</span></span>

<span data-ttu-id="76afc-108">Evalueringsmiljøer er delvist forudkonfigureret for at reducere de krævede trin efter klargøring.</span><span class="sxs-lookup"><span data-stu-id="76afc-108">Evaluation environments are partially preconfigured to reduce the required post-provisioning steps.</span></span>

<span data-ttu-id="76afc-109">Bortset fra nogle mindre begrænsninger, der ikke påvirker funktioner eller funktionalitet, giver Commerce-evalueringsmiljøet den komplette Commerce-oplevelse og kan bruges af kunder og implementeringspartnere til at evaluere produktet, give feedback og foretage fit-/GAP-analyse.</span><span class="sxs-lookup"><span data-stu-id="76afc-109">Aside from some minor limitations that don't affect features or functionality, the Commerce evaluation environment provides the complete Commerce experience, and can be used by customers and implementation partners to evaluate the product, provide feedback, and do fit/gap analysis.</span></span>

## <a name="limitations-of-the-commerce-evaluation-environment"></a><span data-ttu-id="76afc-110">Begrænsninger i Commerce-evalueringsmiljøet</span><span class="sxs-lookup"><span data-stu-id="76afc-110">Limitations of the Commerce evaluation environment</span></span>

<span data-ttu-id="76afc-111">Selvom Commerce-evalueringsmiljøet indeholder det komplette sæt af Commerce-funktioner og -funktionalitet, er der nogle mindre begrænsninger:</span><span class="sxs-lookup"><span data-stu-id="76afc-111">Although the Commerce evaluation environment provides the full set of Commerce features and functionality, there are some minor limitations:</span></span>

- <span data-ttu-id="76afc-112">Selv om Commerce-evalueringsmiljøet i sig selv ikke har nogen geografiske begrænsninger, skal miljøets komponenter, såsom Retail Cloud Scale Unit (RCSU) og e-Commerce-programmer, klargøres i USA.</span><span class="sxs-lookup"><span data-stu-id="76afc-112">Although the Commerce evaluation environment itself has no geographical limitations, components of the environment, such as the Retail Cloud Scale Unit (RCSU) and e-Commerce applications, should be provisioned only in the United States.</span></span>
- <span data-ttu-id="76afc-113">Anvendelse af Commerce-evalueringsmiljøet er begrænset til 30 dage fra datoen for klargøringen af e-Commerce.</span><span class="sxs-lookup"><span data-stu-id="76afc-113">Use of the Commerce evaluation environment is limited to 30 days from the date when e-Commerce is provisioned.</span></span>
- <span data-ttu-id="76afc-114">Commerce-evalueringsmiljøet kan kun implementeres og initialiseres i et miljø, der bruger demotopologien, hvor alle komponenter i et miljø installeres i en enkelt skybaseret virtuel maskine (VM).</span><span class="sxs-lookup"><span data-stu-id="76afc-114">The Commerce evaluation environment can be successfully deployed and initialized only in an environment that uses the demo topology, where all components of an environment are deployed on a single cloud-hosted virtual machine (VM).</span></span> <span data-ttu-id="76afc-115">Den væsentligste begrænsning for denne topologi er antallet af brugere, som miljøet kan understøtte samtidig.</span><span class="sxs-lookup"><span data-stu-id="76afc-115">The main limitation of this topology is the number of concurrent users that the environment can support.</span></span>

## <a name="get-started"></a><span data-ttu-id="76afc-116">Introduktion</span><span class="sxs-lookup"><span data-stu-id="76afc-116">Get started</span></span>

<span data-ttu-id="76afc-117">Sådan klargør du Commerce-evalueringsmiljøet se [Klargøre et Commerce-evalueringsmiljø](provisioning-guide.md).</span><span class="sxs-lookup"><span data-stu-id="76afc-117">To provision the Commerce evaluation environment, see [Provision a Commerce evaluation environment](provisioning-guide.md).</span></span>

## <a name="additional-resources"></a><span data-ttu-id="76afc-118">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="76afc-118">Additional resources</span></span>

[<span data-ttu-id="76afc-119">Klargøre et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="76afc-119">Provision a Dynamics 365 Commerce evaluation environment</span></span>](provisioning-guide.md)

[<span data-ttu-id="76afc-120">Konfigurere et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="76afc-120">Configure a Dynamics 365 Commerce evaluation environment</span></span>](cpe-post-provisioning.md)

[<span data-ttu-id="76afc-121">Konfigurere BOPIS i et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="76afc-121">Configure BOPIS in a Dynamics 365 Commerce evaluation environment</span></span>](cpe-bopis.md)

[<span data-ttu-id="76afc-122">Konfigurere valgfrie funktioner til et Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="76afc-122">Configure optional features for a Dynamics 365 Commerce evaluation environment</span></span>](cpe-optional-features.md)

[<span data-ttu-id="76afc-123">Ofte stillede spørgsmål om Dynamics 365 Commerce-evalueringsmiljø</span><span class="sxs-lookup"><span data-stu-id="76afc-123">Dynamics 365 Commerce evaluation environment FAQ</span></span>](cpe-faq.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]
