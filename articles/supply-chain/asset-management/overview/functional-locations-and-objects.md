---
title: Arbejdssteder og aktiver
description: I dette emne beskrives arbejdssteder og aktiver i Styring af aktiver. Styring af aktiver er et avanceret modul til administration af aktiver og vedligeholdsopgaver i Dynamics 365 Supply Chain Management.
author: josaw1
manager: tfehr
ms.date: 06/24/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: CatProcureCatalogEdit, CatProcureCatalogListPage
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 2214
ms.assetid: 2f3e0441-414d-402b-b28b-7ab0d650d658
ms.search.region: Global
ms.author: mkirknel
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: fe3e82f425421acdae81a02032ac6252765e1c05
ms.sourcegitcommit: 199848e78df5cb7c439b001bdbe1ece963593cdb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/13/2020
ms.locfileid: "4424915"
---
# <a name="functional-locations-and-assets"></a><span data-ttu-id="93f17-104">Arbejdssteder og aktiver</span><span class="sxs-lookup"><span data-stu-id="93f17-104">Functional locations and assets</span></span>

[!include [banner](../../includes/banner.md)]

 

<span data-ttu-id="93f17-105">I dette emne beskrives arbejdssteder og aktiver i Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="93f17-105">This topic describes functional locations and assets in Asset Management.</span></span> <span data-ttu-id="93f17-106">Styring af aktiver er et avanceret modul til administration af aktiver og vedligeholdsopgaver i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="93f17-106">Asset Management is an advanced module for managing assets and maintenance jobs in Dynamics 365 Supply Chain Management.</span></span>

## <a name="overview"></a><span data-ttu-id="93f17-107">Overblik</span><span class="sxs-lookup"><span data-stu-id="93f17-107">Overview</span></span>

<span data-ttu-id="93f17-108">Aktivadministration kan problemfrit integreres med flere moduler i andre Finance and Operations-apps.</span><span class="sxs-lookup"><span data-stu-id="93f17-108">Asset Management is integrated seamlessly with several modules with other Finance and Operations apps.</span></span> <span data-ttu-id="93f17-109">I følgende illustration vises grænsefladerne med andre moduler.</span><span class="sxs-lookup"><span data-stu-id="93f17-109">The following illustration shows the interfaces with other modules.</span></span>

![Diagram, der viser, hvordan aktivstyring integreres med andre moduler](media/01-overview-image.png)

<span data-ttu-id="93f17-111">Styring af aktiver giver dig mulighed for effektivt at administrere og udføre alle opgaver, der er relateret til administration og servicering af mange typer udstyr i din virksomhed.</span><span class="sxs-lookup"><span data-stu-id="93f17-111">Asset Management lets you efficiently manage and perform all tasks that are related to managing and servicing many types of equipment in your company.</span></span> <span data-ttu-id="93f17-112">Dette udstyr omfatter maskiner, produktionsudstyr og køretøjer.</span><span class="sxs-lookup"><span data-stu-id="93f17-112">This equipment includes machines, production equipment, and vehicles.</span></span> <span data-ttu-id="93f17-113">Styring af aktiver understøtter også løsninger på tværs af adskillige brancher.</span><span class="sxs-lookup"><span data-stu-id="93f17-113">Asset Management also supports solutions across numerous industries.</span></span>

<span data-ttu-id="93f17-114">I følgende illustration vises en oversigt over de vigtigste funktioner, der dækkes af Styring af aktiver.</span><span class="sxs-lookup"><span data-stu-id="93f17-114">The following illustration shows an overview of the main functionality that is covered by Asset Management.</span></span>

![Diagram, der viser de vigtigste funktioner i aktivstyring](media/02-overview-image.png)

## <a name="functional-locations-and-assets"></a><span data-ttu-id="93f17-116">Funktionelle placeringer og aktiver</span><span class="sxs-lookup"><span data-stu-id="93f17-116">Functional locations and assets</span></span>

<span data-ttu-id="93f17-117">Arbejdssteder bruges til at administrere aktiver på lokationer.</span><span class="sxs-lookup"><span data-stu-id="93f17-117">Functional locations are used to manage assets on locations.</span></span> <span data-ttu-id="93f17-118">Denne styring omfatter sporing af aktivomkostninger på arbejdssteder.</span><span class="sxs-lookup"><span data-stu-id="93f17-118">This management includes tracking of asset costs on functional locations.</span></span> <span data-ttu-id="93f17-119">Arbejdssteder er struktureret hierarkisk, og lokationer kan have underlokationer.</span><span class="sxs-lookup"><span data-stu-id="93f17-119">Functional locations are structured hierarchically, and locations can have sub-locations.</span></span> <span data-ttu-id="93f17-120">Strukturen af arbejdssteder er statisk.</span><span class="sxs-lookup"><span data-stu-id="93f17-120">The structure of functional locations is static.</span></span> <span data-ttu-id="93f17-121">Med andre ord kan lokationer ikke skifte sted.</span><span class="sxs-lookup"><span data-stu-id="93f17-121">In other words, locations can't change place.</span></span> <span data-ttu-id="93f17-122">Aktiver kan installeres på arbejdssteder og kan efter behov installeres på andre arbejdssteder senere.</span><span class="sxs-lookup"><span data-stu-id="93f17-122">Assets can be installed on functional locations and, as required, can be installed on other functional locations later.</span></span>

<span data-ttu-id="93f17-123">Aktivomkostninger følger altid aktivets lokation.</span><span class="sxs-lookup"><span data-stu-id="93f17-123">Asset costs always follow the location of the asset.</span></span> <span data-ttu-id="93f17-124">Hvis du med andre ord installerer et aktiv på et nyt arbejdssted, bruger aktivet automatisk de økonomiske dimensioner, der er relateret til det nye arbejdssted.</span><span class="sxs-lookup"><span data-stu-id="93f17-124">In other words, if you install an asset on a new functional location, the asset automatically uses the financial dimensions that are related to the new functional location.</span></span> <span data-ttu-id="93f17-125">Derfor er aktivets omkostninger altid relateret til det arbejdssted, som aktivet aktuelt er installeret på.</span><span class="sxs-lookup"><span data-stu-id="93f17-125">Therefore, asset costs are always related to the functional location that the asset is  currently installed on.</span></span> <span data-ttu-id="93f17-126">Denne automatiske håndtering af økonomiske dimensioner hjælper med at sikre en fuldstændig sporing af omkostninger, når din virksomhed kontrollerer og rapporterer om arbejdssteder for projekter.</span><span class="sxs-lookup"><span data-stu-id="93f17-126">This automatic handling of financial dimensions helps guarantee complete tracking of costs when your company does project controlling and reporting on functional locations.</span></span>

<span data-ttu-id="93f17-127">Den måde, du opbygger hierarkiet af arbejdssteder på, afhænger af virksomhedens krav til vedligeholdelse af internt udstyr eller servicering af kundeudstyr.</span><span class="sxs-lookup"><span data-stu-id="93f17-127">The way that you build your hierarchy of functional locations depends on your company's requirements for maintaining internal equipment or servicing customer equipment.</span></span> <span data-ttu-id="93f17-128">I følgende figur vises et eksempel på arbejdssteder, der er baseret på geografiske placeringer.</span><span class="sxs-lookup"><span data-stu-id="93f17-128">The following figure shows an example of functional locations that are based on geographical locations.</span></span>

![Diagram, der viser arbejdssteder baseret på geografiske placeringer](media/03-overview-image.png)

<span data-ttu-id="93f17-130">I følgende figur vises et eksempel på arbejdssteder, der er baseret på kunder.</span><span class="sxs-lookup"><span data-stu-id="93f17-130">The following figure shows an example of functional locations that are based on customers.</span></span>

![Diagram, der viser arbejdssteder baseret på kunder](media/04-overview-image.png)
