---
title: Lokationsstyring
description: "Brug af lagerstedsstyring til at overvåge og automatisere lagerstedsprocesser."
author: BibiSp
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: WHSParameters
audience: Application User
ms.reviewer: bis
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: ba426692e2e404ab75e5730b8205115fc59e402f
ms.openlocfilehash: 43167cc36398d3f7f8d639187f67fad1bae8082f
ms.contentlocale: da-dk
ms.lasthandoff: 02/08/2018

---
# <a name="warehouse-management"></a><span data-ttu-id="0f8bd-103">Lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="0f8bd-103">Warehouse management</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="0f8bd-104">Modulet Lokationsstyring til Dynamics 365 for Finance and Operations, Enterprise Edition giver dig mulighed for at administrere lagerstedsprocesser i produktions-, distributions- og detailvirksomheder.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-104">The Warehouse management module for Dynamics 365 for Finance and Operations, Enterprise edition lets you manage warehouse processes in manufacturing, distribution, and retail companies.</span></span> <span data-ttu-id="0f8bd-105">Dette modul har en lang række funktioner, der understøtter lagerstedet på et optimal niveau, når som helst.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-105">This module has a wide range of features to support the warehouse facility at an optimal level, at any time.</span></span> <span data-ttu-id="0f8bd-106">Lokationsstyring er fuldt integreret med andre forretningsprocesser i Finance and Operations, f.eks. transport, produktion, kvalitetskontrol, køb, overførsel, salg og returneringer.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-106">Warehouse management is fully integrated with other business processes in Finance and Operations such as transportation, manufacturing, quality control, purchase, transfer, sales, and returns.</span></span>

## <a name="get-started"></a><span data-ttu-id="0f8bd-107">Introduktion</span><span class="sxs-lookup"><span data-stu-id="0f8bd-107">Get started</span></span>
<span data-ttu-id="0f8bd-108">Hvis du vil begynde at arbejde med Lokationsstyring, skal du fuldføre opsætningen af de generelle lagerstedsparametre for at understøtte forretningsprocesserne i virksomheden.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-108">To start working with Warehouse management, you need to complete the setup of the general warehouse parameters to support the business processes of you company.</span></span>

- <span data-ttu-id="0f8bd-109">Gå til siden **Parametre til lokationsstyring** under **Lokationsstyring** > **Konfiguration** for at konfigurere generelle lagerstedsparametre.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-109">Go to the **Warehouse management parameters** page under **Warehouse management** > **Setup** to set up general warehouse parameters.</span></span>

<span data-ttu-id="0f8bd-110">Du skal konfigurere komponenter for indgående og udgående lagerstedsarbejdsprocesser i henhold til virksomhedens behov.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-110">You must configure components for inbound and outbound warehouse process workflows according to business requirements.</span></span> <span data-ttu-id="0f8bd-111">De vigtigste komponenter, du skal konfigurere, er bølgeskabeloner, arbejdsskabeloner, arbejdspuljer og lokalitetsvejledninger.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-111">The most important components that you must configure are wave templates, work templates, work pools, and location directives.</span></span>

- [<span data-ttu-id="0f8bd-112">Konfiguration af lokation</span><span class="sxs-lookup"><span data-stu-id="0f8bd-112">Warehouse configuration</span></span>](warehouse-configuration.md)
- [<span data-ttu-id="0f8bd-113">Styre lagerarbejde ved at bruge arbejdsskabeloner og lokalitetsdirektiver</span><span class="sxs-lookup"><span data-stu-id="0f8bd-113">Control warehouse work by using work templates and location directives</span></span>](control-warehouse-location-directives.md)
- [<span data-ttu-id="0f8bd-114">Konfigurere mobilenheder til lagerstedsarbejde</span><span class="sxs-lookup"><span data-stu-id="0f8bd-114">Set up mobile devices for warehouse work</span></span>](configure-mobile-devices-warehouse.md)
- [<span data-ttu-id="0f8bd-115">Konfigurere en lokationsvejledning til vareplacering for indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="0f8bd-115">Set up a location directive for purchase order put-away</span></span>](../transportation/tasks/set-up-location-directive-purchase-order-put-away.md)
- [<span data-ttu-id="0f8bd-116">Konfigurere en arbejdsskabelon for indkøbsordrer</span><span class="sxs-lookup"><span data-stu-id="0f8bd-116">Set up a work template for purchase orders</span></span>](./tasks/set-up-work-template-purchase-orders.md)

## <a name="warehouse-management-processes"></a><span data-ttu-id="0f8bd-117">Lokationsstyringsprocesser</span><span class="sxs-lookup"><span data-stu-id="0f8bd-117">Warehouse management processes</span></span>
- <span data-ttu-id="0f8bd-118">Integreret understøttelse af kildedokumenterne for salgsordrer, returvarer, flytteordrer, produktionsordrer og kanban</span><span class="sxs-lookup"><span data-stu-id="0f8bd-118">Integrated support for source documents for sales orders, returns, transfer orders, production orders, and kanban</span></span>  
- <span data-ttu-id="0f8bd-119">Understøttelse af fleksible, indgående og udgående materialearbejdsgange baseret på forespørgsler</span><span class="sxs-lookup"><span data-stu-id="0f8bd-119">Flexible, inbound and outbound material workflow support based on queries</span></span>
- <span data-ttu-id="0f8bd-120">Fuld integration med produktions- og transporttilbuddene</span><span class="sxs-lookup"><span data-stu-id="0f8bd-120">Full integration with the Manufacturing and Transportation offerings</span></span>
- <span data-ttu-id="0f8bd-121">Fuld kontrol over grænser for lokationslagring og lokationsmængder</span><span class="sxs-lookup"><span data-stu-id="0f8bd-121">Full control of location stocking limits and location volumetrics</span></span>
- <span data-ttu-id="0f8bd-122">Lageregenskaber styres af lagerstatus</span><span class="sxs-lookup"><span data-stu-id="0f8bd-122">Inventory properties controlled by inventory status</span></span>
- <span data-ttu-id="0f8bd-123">Fuld understøttelse af batch- og serievare</span><span class="sxs-lookup"><span data-stu-id="0f8bd-123">Full batch and serial item support</span></span>
- <span data-ttu-id="0f8bd-124">Forskellige varemodtagelsesmuligheder</span><span class="sxs-lookup"><span data-stu-id="0f8bd-124">Various item receiving capabilities</span></span>
- <span data-ttu-id="0f8bd-125">Flere plukstrategier</span><span class="sxs-lookup"><span data-stu-id="0f8bd-125">Multiple picking strategies</span></span>
- <span data-ttu-id="0f8bd-126">Indbygget understøttelse af næste generation af stregkodescannere</span><span class="sxs-lookup"><span data-stu-id="0f8bd-126">Out-of-the-box support for the next generation of barcode scanners</span></span>
- <span data-ttu-id="0f8bd-127">Palle-/containertyper til lagerprocesser</span><span class="sxs-lookup"><span data-stu-id="0f8bd-127">Pallet/container types for warehouse processes</span></span>
- <span data-ttu-id="0f8bd-128">Avancerede optællingsegenskaber</span><span class="sxs-lookup"><span data-stu-id="0f8bd-128">Advanced counting capabilities</span></span>
- <span data-ttu-id="0f8bd-129">Etiketudskrivning og ruteplanlægning af etiketter med understøttelse af Zebra ZPL</span><span class="sxs-lookup"><span data-stu-id="0f8bd-129">Label printing and label routing with Zebra ZPL support</span></span>
- <span data-ttu-id="0f8bd-130">Business intelligence-integration i Power BI</span><span class="sxs-lookup"><span data-stu-id="0f8bd-130">Business intelligence integration into Power BI</span></span>
- <span data-ttu-id="0f8bd-131">Manuelle og automatiske lagerbevægelser</span><span class="sxs-lookup"><span data-stu-id="0f8bd-131">Manual and automatic movement of inventory</span></span>
- <span data-ttu-id="0f8bd-132">Fuldt integreret kvalitetskontrol (QMS)</span><span class="sxs-lookup"><span data-stu-id="0f8bd-132">Fully-integrated quality control (QMS)</span></span>
- <span data-ttu-id="0f8bd-133">Fuld sporbarhed af arbejderes materialehåndtering</span><span class="sxs-lookup"><span data-stu-id="0f8bd-133">Full traceability of workers' material handling</span></span>
- <span data-ttu-id="0f8bd-134">Udgående bølgebehandling</span><span class="sxs-lookup"><span data-stu-id="0f8bd-134">Outbound wave processing</span></span>
- <span data-ttu-id="0f8bd-135">Understøttelse af manuel pakning og automatisk containerpakning</span><span class="sxs-lookup"><span data-stu-id="0f8bd-135">Manual packing and automatic containerization support</span></span>
- <span data-ttu-id="0f8bd-136">Klyngepluk</span><span class="sxs-lookup"><span data-stu-id="0f8bd-136">Cluster picking</span></span>
- <span data-ttu-id="0f8bd-137">Enkel cross-docking</span><span class="sxs-lookup"><span data-stu-id="0f8bd-137">Simple cross docking</span></span>

## <a name="additional-resources"></a><span data-ttu-id="0f8bd-138">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="0f8bd-138">Additional resources</span></span>
### <a name="whats-new-and-in-development"></a><span data-ttu-id="0f8bd-139">Nyheder og under udvikling</span><span class="sxs-lookup"><span data-stu-id="0f8bd-139">What's new and in development</span></span>
<span data-ttu-id="0f8bd-140">Gå til [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) for at se, hvilke nye funktioner der er blevet frigivet, og hvilke nye funktioner der er under udvikling.</span><span class="sxs-lookup"><span data-stu-id="0f8bd-140">Go to the [Microsoft Dynamics 365 Roadmap](https://roadmap.dynamics.com/) to see what new features have been released and what new features are in development.</span></span>

### <a name="blogs"></a><span data-ttu-id="0f8bd-141">Blogs</span><span class="sxs-lookup"><span data-stu-id="0f8bd-141">Blogs</span></span>
<span data-ttu-id="0f8bd-142">Du kan finde meninger, nyheder og andre oplysninger om Lokationsstyring og andre løsninger i [Microsoft Dynamics 365-bloggen](https://community.dynamics.com/b/msftdynamicsblog).</span><span class="sxs-lookup"><span data-stu-id="0f8bd-142">You can find opinions, news, and other information about Warehouse management and other solutions on the [Microsoft Dynamics 365 blog](https://community.dynamics.com/b/msftdynamicsblog).</span></span>


 


