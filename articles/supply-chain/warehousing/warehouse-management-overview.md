---
title: Lokationsstyring
description: Brug af lagerstedsstyring til at overvåge og automatisere lagerstedsprocesser.
author: ShylaThompson
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 7c9613070e077bced4b272b136985de5f4ddbdd0
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2019
ms.locfileid: "1543393"
---
# <a name="warehouse-management"></a><span data-ttu-id="f8ae8-103">Lagerstedsstyring</span><span class="sxs-lookup"><span data-stu-id="f8ae8-103">Warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8ae8-104">Lagerstedsstyringsmodulet til Dynamics 365 for Finance and Operations gør det muligt at styre lagerstyringspocesser i produktions-, distributions- og detailhandelsvirksomheder.</span><span class="sxs-lookup"><span data-stu-id="f8ae8-104">The Warehouse management module for Dynamics 365 for Finance and Operations lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="f8ae8-105">Dette modul har en lang række funktioner, der understøtter lagerstedet på et optimal niveau, når som helst.</span><span class="sxs-lookup"><span data-stu-id="f8ae8-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="f8ae8-106">Lokationsstyring er fuldt integreret med andre forretningsprocesser i Finance and Operations, f.eks. transport, produktion, kvalitetskontrol, køb, overførsel, salg og returneringer.</span><span class="sxs-lookup"><span data-stu-id="f8ae8-106">Warehouse management is fully integrated with other business processes in Finance and Operations such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="f8ae8-107">Introduktion</span><span class="sxs-lookup"><span data-stu-id="f8ae8-107">Get started</span></span>
<span data-ttu-id="f8ae8-108">Hvis du vil begynde at arbejde med Lokationsstyring, skal du fuldføre opsætningen af de generelle lagerstedsparametre for at understøtte forretningsprocesserne i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="f8ae8-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of you company.</span></span>

- <span data-ttu-id="f8ae8-109">Gå til siden **Parametre til lokationsstyring** under **Lokationsstyring** > **Konfiguration** for at konfigurere generelle lagerstedsparametre.</span><span class="sxs-lookup"><span data-stu-id="f8ae8-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="f8ae8-110">Du skal konfigurere komponenter for indgående og udgående lagerstedsarbejdsprocesser i henhold til virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="f8ae8-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="f8ae8-111">De vigtigste komponenter, du skal konfigurere, er bølgeskabeloner, arbejdsskabeloner, arbejdspuljer og lokalitetsvejledninger.</span><span class="sxs-lookup"><span data-stu-id="f8ae8-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="f8ae8-112">Konfiguration af lokation</span><span class="sxs-lookup"><span data-stu-id="f8ae8-112">Warehouse configuration</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="f8ae8-113">Styre lagerarbejde ved at bruge arbejdsskabeloner og lokalitetsdirektiver</span><span class="sxs-lookup"><span data-stu-id="f8ae8-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="f8ae8-114">Konfigurere mobilenheder til lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="f8ae8-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="f8ae8-115">Konfigurere en lokationsvejledning til vareplacering for indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="f8ae8-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="f8ae8-116">Konfigurere en arbejdsskabelon for indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="f8ae8-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="f8ae8-117">Lokationsstyringsprocesser</span><span class="sxs-lookup"><span data-stu-id="f8ae8-117">Warehouse management processes</span></span>
- <span data-ttu-id="f8ae8-118">Integreret understøttelse af kildedokumenterne for salgsordrer, returvarer, flytteordrer, produktionsordrer og kanban</span><span class="sxs-lookup"><span data-stu-id="f8ae8-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="f8ae8-119">Understøttelse af fleksible, indgående og udgående materialearbejdsgange baseret på forespørgsler</span><span class="sxs-lookup"><span data-stu-id="f8ae8-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="f8ae8-120">Fuld integration med produktions- og transporttilbuddene</span><span class="sxs-lookup"><span data-stu-id="f8ae8-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="f8ae8-121">Fuld kontrol over grænser for lokationslagring og lokationsmængder</span><span class="sxs-lookup"><span data-stu-id="f8ae8-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="f8ae8-122">Lageregenskaber styres af lagerstatus</span><span class="sxs-lookup"><span data-stu-id="f8ae8-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="f8ae8-123">Fuld understøttelse af batch- og serievare</span><span class="sxs-lookup"><span data-stu-id="f8ae8-123">Full batch and serial item support</span></span>
- <span data-ttu-id="f8ae8-124">Forskellige varemodtagelsesmuligheder</span><span class="sxs-lookup"><span data-stu-id="f8ae8-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="f8ae8-125">Flere plukstrategier</span><span class="sxs-lookup"><span data-stu-id="f8ae8-125">Multiple picking strategies</span></span>
- <span data-ttu-id="f8ae8-126">Indbygget understøttelse af næste generation af stregkodescannere</span><span class="sxs-lookup"><span data-stu-id="f8ae8-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="f8ae8-127">Palle-/containertyper til lagerprocesser</span><span class="sxs-lookup"><span data-stu-id="f8ae8-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="f8ae8-128">Avancerede optællingsegenskaber</span><span class="sxs-lookup"><span data-stu-id="f8ae8-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="f8ae8-129">Etiketudskrivning og ruteplanlægning af etiketter med understøttelse af Zebra ZPL</span><span class="sxs-lookup"><span data-stu-id="f8ae8-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="f8ae8-130">Business intelligence-integration i Power BI</span><span class="sxs-lookup"><span data-stu-id="f8ae8-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="f8ae8-131">Manuelle og automatiske lagerbevægelser</span><span class="sxs-lookup"><span data-stu-id="f8ae8-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="f8ae8-132">Fuldt integreret kvalitetskontrol (QMS)</span><span class="sxs-lookup"><span data-stu-id="f8ae8-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="f8ae8-133">Fuld sporbarhed af arbejderes materialehåndtering</span><span class="sxs-lookup"><span data-stu-id="f8ae8-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="f8ae8-134">Udgående bølgebehandling</span><span class="sxs-lookup"><span data-stu-id="f8ae8-134">Outbound wave processing</span></span>
- <span data-ttu-id="f8ae8-135">Understøttelse af manuel pakning og automatisk containerpakning</span><span class="sxs-lookup"><span data-stu-id="f8ae8-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="f8ae8-136">Klyngepluk</span><span class="sxs-lookup"><span data-stu-id="f8ae8-136">Cluster picking</span></span>
- <span data-ttu-id="f8ae8-137">Enkel cross-docking</span><span class="sxs-lookup"><span data-stu-id="f8ae8-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="f8ae8-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="f8ae8-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="f8ae8-139">Nyheder og funktioner under udvikling</span><span class="sxs-lookup"><span data-stu-id="f8ae8-139">What's new and in development</span></span>
<span data-ttu-id="f8ae8-140">Gå til [Microsoft Dynamics 365-oversigten](https://roadmap.dynamics.com/) for at se, hvilke nye funktioner der er blevet frigivet, og hvilke nye funktioner der er under udvikling.</span><span class="sxs-lookup"><span data-stu-id="f8ae8-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="f8ae8-141">Blogs</span><span class="sxs-lookup"><span data-stu-id="f8ae8-141">Blogs</span></span>
<span data-ttu-id="f8ae8-142">Du kan finde meninger, nyheder og andre oplysninger om lagerstyring og andre løsninger i [Microsoft Dynamics 365-bloggen](https://community.dynamics.com/b/msftdynamicsblog).</span><span class="sxs-lookup"><span data-stu-id="f8ae8-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 

