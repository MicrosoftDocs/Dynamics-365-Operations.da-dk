---
title: Pakningsstrategier for containere
description: I dette emne beskrives forskellene mellem pakningsstrategier for containere, og det indeholder eksempler.
author: GalynaFedorova
ms.date: 06/11/2021
ms.topic: article
ms.search.form: WHSWaveTemplateTable, InventLocationIdLookup, WHSContainerType, WHSContainerGroup, WHSContainerizationTable, WHSContainerizationBreak, WHSCreateContainerBreak, WHSContainerStructure, WHSContainerTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: v-gfedorova
ms.search.validFrom: 2021-06-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: f481f6ca047ee0285fe0e81d8fa96665e9d27cee
ms.sourcegitcommit: 8e846b52763f90d2232ec7d427839f4722570bce
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/22/2021
ms.locfileid: "6292755"
---
# <a name="container-packing-strategies"></a><span data-ttu-id="e3898-103">Pakningsstrategier for containere</span><span class="sxs-lookup"><span data-stu-id="e3898-103">Container packing strategies</span></span>

<span data-ttu-id="e3898-104">En *pakningsstrategi for containere* er en strategi, som du kan bruge til at definere varefordelinger på tværs af containere.</span><span class="sxs-lookup"><span data-stu-id="e3898-104">A *container packing strategy* is a strategy that you can use to define item allocations across containers.</span></span> <span data-ttu-id="e3898-105">I dette emne forklares forskellene mellem strategierne *Pak i alle åbne containere* og *Pak kun i aktuel container*.</span><span class="sxs-lookup"><span data-stu-id="e3898-105">This topic explains the differences between the *Pack into all open containers* and *Pack into current container only* strategies.</span></span>

- <span data-ttu-id="e3898-106">**Pak i alle åbne containere** – Systemet skal kontrollere alle åbne containere, der allerede er oprettet under containeriseringscyklussen, for at sikre, at varen kan være i en af dem.</span><span class="sxs-lookup"><span data-stu-id="e3898-106">**Pack into all open containers** – The system must check all open containers that have already been created during the containerization cycle, to make sure that the item will fit into one of them.</span></span> <span data-ttu-id="e3898-107">Under pakning kontrollerer systemet hver vare for at finde ud af, om den kan være i en af de tidligere oprettede containere.</span><span class="sxs-lookup"><span data-stu-id="e3898-107">During packing, the system checks each item to determine whether it will fit into any of the previously created containers.</span></span> <span data-ttu-id="e3898-108">Hvis varen ikke kan være i en eksisterende container, opretter systemet en ny container og fortsætter, indtil det er færdig med at pakke hele ordren.</span><span class="sxs-lookup"><span data-stu-id="e3898-108">If the item won't fit into an existing container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="e3898-109">*N* bestilte varer kræver for eksempel containerisering.</span><span class="sxs-lookup"><span data-stu-id="e3898-109">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="e3898-110">Hver gang systemet behandler en vare, der ikke kan være i en eksisterende container, vil den i det tilfælde foretage i alt (\[(*n* - 1) × (*n* + 1)\] ÷ 2) kontroller for at vurdere, om varen kan være i de eksisterende containere.</span><span class="sxs-lookup"><span data-stu-id="e3898-110">In the worst case, every time that the system processes an item that doesn't fit into any existing container, it will do a total of (\[(*n* – 1) × (*n* + 1)\] ÷ 2) checks to evaluate whether the item fits into the existing containers.</span></span>

- <span data-ttu-id="e3898-111">**Pak kun i aktuel container** – Systemet skal kun kontrollere den senest oprettede container for at sikre, at varen kan være i den.</span><span class="sxs-lookup"><span data-stu-id="e3898-111">**Pack into current container only** – The system must check only the most recently created container to make sure that the item will fit into it.</span></span> <span data-ttu-id="e3898-112">Under pakning kontrollerer systemet hver vare for at finde ud af, om den kan være i den senest oprettede container.</span><span class="sxs-lookup"><span data-stu-id="e3898-112">During packing, the system checks each item to determine whether it will fit into the most recently created container.</span></span> <span data-ttu-id="e3898-113">Hvis varen ikke kan være i den pågældende container, opretter systemet en ny container og fortsætter, indtil det er færdig med at pakke hele ordren.</span><span class="sxs-lookup"><span data-stu-id="e3898-113">If the item won't fit into that container, the system creates a new container and continues until it has finished packing the whole order.</span></span>

    <span data-ttu-id="e3898-114">*N* bestilte varer kræver for eksempel containerisering.</span><span class="sxs-lookup"><span data-stu-id="e3898-114">For example, *n* ordered items require containerization.</span></span> <span data-ttu-id="e3898-115">I værste tilfælde vil systemet foretage i alt (*n* - 1) kontroller for at evaluere, om varen kan være i containerne.</span><span class="sxs-lookup"><span data-stu-id="e3898-115">In the worst case, the system will do a total of (*n* – 1) checks to evaluate whether the item fits into the containers.</span></span>

## <a name="example-of-the-flow-for-container-packing-strategies"></a><span data-ttu-id="e3898-116">Eksempel på flowet for pakningsstrategier for containere</span><span class="sxs-lookup"><span data-stu-id="e3898-116">Example of the flow for container packing strategies</span></span>

<span data-ttu-id="e3898-117">Du skal konfigurere følgende varer for containerisering.</span><span class="sxs-lookup"><span data-stu-id="e3898-117">You set up the following items for containerization.</span></span>

| <span data-ttu-id="e3898-118">Post</span><span class="sxs-lookup"><span data-stu-id="e3898-118">Item</span></span> | <span data-ttu-id="e3898-119">Fysiske dimensioner (bredde × dybde × højde)</span><span class="sxs-lookup"><span data-stu-id="e3898-119">Physical dimensions (width × depth × height)</span></span> | <span data-ttu-id="e3898-120">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="e3898-120">Weight</span></span> |
|---|---|---|
| <span data-ttu-id="e3898-121">HDMI-kabel 6'</span><span class="sxs-lookup"><span data-stu-id="e3898-121">HDMI Cable 6'</span></span> | <span data-ttu-id="e3898-122">1 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="e3898-122">1 × 1 × 1</span></span> | <span data-ttu-id="e3898-123">1</span><span class="sxs-lookup"><span data-stu-id="e3898-123">1</span></span> |
| <span data-ttu-id="e3898-124">HDMI-kabel 12'</span><span class="sxs-lookup"><span data-stu-id="e3898-124">HDMI Cable 12'</span></span> | <span data-ttu-id="e3898-125">2 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="e3898-125">2 × 1 × 1</span></span> | <span data-ttu-id="e3898-126">1</span><span class="sxs-lookup"><span data-stu-id="e3898-126">1</span></span> |
| <span data-ttu-id="e3898-127">HDMI-kabel 18'</span><span class="sxs-lookup"><span data-stu-id="e3898-127">HDMI Cable 18'</span></span> | <span data-ttu-id="e3898-128">3 × 1 × 1</span><span class="sxs-lookup"><span data-stu-id="e3898-128">3 × 1 × 1</span></span> | <span data-ttu-id="e3898-129">2</span><span class="sxs-lookup"><span data-stu-id="e3898-129">2</span></span> |

<span data-ttu-id="e3898-130">Du skal også konfigurere følgende kasse, som skal bruges til pakning.</span><span class="sxs-lookup"><span data-stu-id="e3898-130">You also set up the following box that will be used for packaging.</span></span>

| <span data-ttu-id="e3898-131">Container</span><span class="sxs-lookup"><span data-stu-id="e3898-131">Container</span></span> | <span data-ttu-id="e3898-132">Fysiske dimensioner (længde × bredde × højde)</span><span class="sxs-lookup"><span data-stu-id="e3898-132">Physical dimensions (length × width × height)</span></span> | <span data-ttu-id="e3898-133">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="e3898-133">Weight</span></span> | <span data-ttu-id="e3898-134">Mængde</span><span class="sxs-lookup"><span data-stu-id="e3898-134">Volume</span></span> |
|---|---|---|---|
| <span data-ttu-id="e3898-135">Mellemstor kasse</span><span class="sxs-lookup"><span data-stu-id="e3898-135">Medium Box</span></span> | <span data-ttu-id="e3898-136">6 × 3 × 2</span><span class="sxs-lookup"><span data-stu-id="e3898-136">6 × 3 × 2</span></span> | <span data-ttu-id="e3898-137">10</span><span class="sxs-lookup"><span data-stu-id="e3898-137">10</span></span> | <span data-ttu-id="e3898-138">100</span><span class="sxs-lookup"><span data-stu-id="e3898-138">100</span></span> |

<span data-ttu-id="e3898-139">Endelig skal du konfigurere en ordre med følgende produkter og antal.</span><span class="sxs-lookup"><span data-stu-id="e3898-139">Finally, you set up an order that has the following products and quantities.</span></span>

| <span data-ttu-id="e3898-140">Salgsordrelinje</span><span class="sxs-lookup"><span data-stu-id="e3898-140">Sales order line</span></span> | <span data-ttu-id="e3898-141">Mængde</span><span class="sxs-lookup"><span data-stu-id="e3898-141">Quantity</span></span> |
|---|---|
| <span data-ttu-id="e3898-142">HDMI-kabel 12'</span><span class="sxs-lookup"><span data-stu-id="e3898-142">HDMI Cable 12'</span></span> | <span data-ttu-id="e3898-143">9</span><span class="sxs-lookup"><span data-stu-id="e3898-143">9</span></span> |
| <span data-ttu-id="e3898-144">HDMI-kabel 18'</span><span class="sxs-lookup"><span data-stu-id="e3898-144">HDMI Cable 18'</span></span> | <span data-ttu-id="e3898-145">8</span><span class="sxs-lookup"><span data-stu-id="e3898-145">8</span></span> |
| <span data-ttu-id="e3898-146">HDMI-kabel 6'</span><span class="sxs-lookup"><span data-stu-id="e3898-146">HDMI Cable 6'</span></span> | <span data-ttu-id="e3898-147">13</span><span class="sxs-lookup"><span data-stu-id="e3898-147">13</span></span> |

<span data-ttu-id="e3898-148">I følgende tabel opsummeres, hvordan containerisering fungerer, når du bruger strategien *Pak i alle åbne containere*, og når du kun bruger strategien *Pak kun i aktuel container*.</span><span class="sxs-lookup"><span data-stu-id="e3898-148">The following table summarizes how containerization works when you use the *Pack into all open containers* strategy and when you use the *Pack into current container only* strategy.</span></span>

| <span data-ttu-id="e3898-149">Pak i alle åbne containere</span><span class="sxs-lookup"><span data-stu-id="e3898-149">Pack into all open containers</span></span> | <span data-ttu-id="e3898-150">Pak i aktuel container</span><span class="sxs-lookup"><span data-stu-id="e3898-150">Pack into current container</span></span> |
|---|---|
| <p><span data-ttu-id="e3898-151">HDMI-kabel 12':</span><span class="sxs-lookup"><span data-stu-id="e3898-151">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="e3898-152">Opret en ny container, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="e3898-152">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="e3898-153">Anbring 9 ea i container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="e3898-153">Put 9 ea into container CONT0001.</span></span></li></ol> | <p><span data-ttu-id="e3898-154">HDMI-kabel 12':</span><span class="sxs-lookup"><span data-stu-id="e3898-154">HDMI Cable 12':</span></span></p><ol><li><span data-ttu-id="e3898-155">Opret en ny container, CONT0001.</span><span class="sxs-lookup"><span data-stu-id="e3898-155">Create a new container, CONT0001.</span></span></li><li><span data-ttu-id="e3898-156">Anbring 9 ea i container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="e3898-156">Put 9 ea into container CONT0001.</span></span></li></ol> |
| <p><span data-ttu-id="e3898-157">HDMI-kabel 18':</span><span class="sxs-lookup"><span data-stu-id="e3898-157">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="e3898-158">Kontrollér, om varen kan være i container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="e3898-158">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="e3898-159">Opret en ny container, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="e3898-159">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="e3898-160">Anbring 5 ea i container CONT0002.</span><span class="sxs-lookup"><span data-stu-id="e3898-160">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="e3898-161">Opret en ny container, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="e3898-161">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="e3898-162">Anbring 3 ea i container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="e3898-162">Put 3 ea into container CONT0003.</span></span></li></ol> | <p><span data-ttu-id="e3898-163">HDMI-kabel 18':</span><span class="sxs-lookup"><span data-stu-id="e3898-163">HDMI Cable 18':</span></span></p><ol><li><span data-ttu-id="e3898-164">Kontrollér, om varen kan være i container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="e3898-164">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="e3898-165">Opret en ny container, CONT0002.</span><span class="sxs-lookup"><span data-stu-id="e3898-165">Create a new container, CONT0002.</span></span></li><li><span data-ttu-id="e3898-166">Anbring 5 ea i container CONT0002.</span><span class="sxs-lookup"><span data-stu-id="e3898-166">Put 5 ea into container CONT0002.</span></span></li><li><span data-ttu-id="e3898-167">Opret en ny container, CONT0003.</span><span class="sxs-lookup"><span data-stu-id="e3898-167">Create a new container, CONT0003.</span></span></li><li><span data-ttu-id="e3898-168">Anbring 3 ea i container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="e3898-168">Put 3 ea into container CONT0003.</span></span></li></ol> |
| <p><span data-ttu-id="e3898-169">HDMI-kabel 6':</span><span class="sxs-lookup"><span data-stu-id="e3898-169">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="e3898-170">Kontrollér, om varen kan være i container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="e3898-170">Check whether the item can fit into container CONT0001.</span></span></li><li><span data-ttu-id="e3898-171">Anbring 1 ea i container CONT0001.</span><span class="sxs-lookup"><span data-stu-id="e3898-171">Put 1 ea into container CONT0001.</span></span></li><li><span data-ttu-id="e3898-172">Kontrollér, om varen kan være i container CONT0002.</span><span class="sxs-lookup"><span data-stu-id="e3898-172">Check whether the item can fit into container CONT0002.</span></span></li><li><span data-ttu-id="e3898-173">Kontrollér, om varen kan være i container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="e3898-173">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="e3898-174">Anbring 4 ea i container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="e3898-174">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="e3898-175">Opret en ny container, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="e3898-175">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="e3898-176">Anbring 8 ea i container CONT0004.</span><span class="sxs-lookup"><span data-stu-id="e3898-176">Put 8 ea into container CONT0004.</span></span></li></ol> | <p><span data-ttu-id="e3898-177">HDMI-kabel 6':</span><span class="sxs-lookup"><span data-stu-id="e3898-177">HDMI Cable 6':</span></span></p><ol><li><span data-ttu-id="e3898-178">Kontrollér, om varen kan være i container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="e3898-178">Check whether the item can fit into container CONT0003.</span></span></li><li><span data-ttu-id="e3898-179">Anbring 4 ea i container CONT0003.</span><span class="sxs-lookup"><span data-stu-id="e3898-179">Put 4 ea into container CONT0003.</span></span></li><li><span data-ttu-id="e3898-180">Opret en ny container, CONT0004.</span><span class="sxs-lookup"><span data-stu-id="e3898-180">Create a new container, CONT0004.</span></span></li><li><span data-ttu-id="e3898-181">Anbring 9 ea i container CONT0004.</span><span class="sxs-lookup"><span data-stu-id="e3898-181">Put 9 ea into container CONT0004.</span></span></li></ol> |

## <a name="example-scenario-pack-single-orders-per-container"></a><span data-ttu-id="e3898-182">Eksempelscenario: Pak enkelte ordrer pr. container</span><span class="sxs-lookup"><span data-stu-id="e3898-182">Example scenario: Pack single orders per container</span></span>

<span data-ttu-id="e3898-183">I dette afsnit kan du se et scenarie, hvor systemet er konfigureret til at samle flere ordrer i én forsendelse.</span><span class="sxs-lookup"><span data-stu-id="e3898-183">This section presents a scenario where the system is set up to consolidate multiple orders into one shipment.</span></span> <span data-ttu-id="e3898-184">Der udføres derfor containerisering fra salgsordren for at sikre, at alle ordrer, der indeholder flere produkter, pakkes i sin egen container.</span><span class="sxs-lookup"><span data-stu-id="e3898-184">Therefore, containerization will be done from the sales order to ensure that every order that contains multiple products is packed into its own container.</span></span>

<span data-ttu-id="e3898-185">Denne funktionalitet giver dig mulighed for at håndtere scenarier, hvor du kun skal pakke én salgsordre i hver container, så distributionscenteret kan udføre cross-docking af fulde containere mellem detailforretninger.</span><span class="sxs-lookup"><span data-stu-id="e3898-185">This functionality lets you handle scenarios where you must pack only one sales order into each container, so that the distribution center can cross-dock full containers between retail stores.</span></span> <span data-ttu-id="e3898-186">Ud over detailscenarierne (ordre pr. detailbutik og forsendelse til et distributionscenter til cross-docking) bruges denne teknik også ofte i lean forsyningskæder (salgsordre pr. just-in-time-produktionslinje).</span><span class="sxs-lookup"><span data-stu-id="e3898-186">In addition to the retail scenarios (order per retail store and shipping to a distribution center for cross-docking) this technique is also commonly used in lean supply chains (sales order per just-in-time production line).</span></span>

<span data-ttu-id="e3898-187">Dette scenario viser, hvordan du kan reducere antallet af containere, der evalueres under pakning, ved hjælp af strategien *Pak kun i aktuel container* for containerisering.</span><span class="sxs-lookup"><span data-stu-id="e3898-187">This scenario shows how you can decrease the number of containers that are evaluated during packing by using the *Pack into current container only* strategy for containerization.</span></span>

### <a name="prerequisites"></a><span data-ttu-id="e3898-188">Forudsætninger</span><span class="sxs-lookup"><span data-stu-id="e3898-188">Prerequisites</span></span>

#### <a name="turn-on-the-consolidate-shipments-feature-in-your-system"></a><span data-ttu-id="e3898-189">Aktivere funktionen Konsolider forsendelser i systemet</span><span class="sxs-lookup"><span data-stu-id="e3898-189">Turn on the Consolidate shipments feature in your system</span></span>

<span data-ttu-id="e3898-190">I dette scenario bruges funktionen *Konsolider forsendelser*.</span><span class="sxs-lookup"><span data-stu-id="e3898-190">This scenario uses the *Consolidate shipments* feature.</span></span> <span data-ttu-id="e3898-191">Hvis funktionen ikke allerede er tilgængelig i systemet, skal du aktivere den ved hjælp af [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span><span class="sxs-lookup"><span data-stu-id="e3898-191">If that feature isn't already available in your system, you must turn it on by using [Feature management](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md).</span></span>

#### <a name="make-demo-data-available"></a><span data-ttu-id="e3898-192">Gøre demodata tilgængelige</span><span class="sxs-lookup"><span data-stu-id="e3898-192">Make demo data available</span></span>

<span data-ttu-id="e3898-193">Dette scenarie indeholder referencer til værdier og poster, der er inkluderet i de standarddemodata, der er angivet for Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e3898-193">This scenario references values and records that are included in the standard demo data that is provided for Microsoft Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="e3898-194">Hvis du vil bruge de værdier, der er angivet her, når du udfører øvelserne, skal du arbejde i et miljø, hvor demodataene er installeret, og angive den juridiske enhed til **USMF**, før du går i gang.</span><span class="sxs-lookup"><span data-stu-id="e3898-194">If you want to use the values that are provided here as you do the exercises, be sure to work in an environment where the demo data is installed, and set the legal entity to **USMF** before you begin.</span></span>

### <a name="inspect-or-create-container-types"></a><span data-ttu-id="e3898-195">Undersøge eller oprette containertyper</span><span class="sxs-lookup"><span data-stu-id="e3898-195">Inspect or create container types</span></span>

<span data-ttu-id="e3898-196">Benyt følgende fremgangsmåde for at undersøge containertyper eller oprette nye containertyper, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="e3898-196">To inspect your container types, or to create new container types if they are required, follow these steps.</span></span>

1. <span data-ttu-id="e3898-197">Gå til **Lagerstedsstyring** \> **Konfiguration** \> **Containere** \> **Containertyper**.</span><span class="sxs-lookup"><span data-stu-id="e3898-197">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container types**.</span></span>
1. <span data-ttu-id="e3898-198">Kontrollér, at hver af følgende containertyper er tilgængelig i dine demodata.</span><span class="sxs-lookup"><span data-stu-id="e3898-198">Make sure that each of the following container types is available in your demo data.</span></span> <span data-ttu-id="e3898-199">Rediger eller opret containertyper efter behov.</span><span class="sxs-lookup"><span data-stu-id="e3898-199">Edit or create container types as required.</span></span>

    - <span data-ttu-id="e3898-200">Containertype 1:</span><span class="sxs-lookup"><span data-stu-id="e3898-200">Container type 1:</span></span>

        - <span data-ttu-id="e3898-201">**Containertypekode:** *Kasse-Stor*</span><span class="sxs-lookup"><span data-stu-id="e3898-201">**Container type code:** *Box-Large*</span></span>
        - <span data-ttu-id="e3898-202">**Beskrivelse:** *Stor kasse*</span><span class="sxs-lookup"><span data-stu-id="e3898-202">**Description:** *Large Box*</span></span>
        - <span data-ttu-id="e3898-203">**Maksimal nettovægt:** *100*</span><span class="sxs-lookup"><span data-stu-id="e3898-203">**Maximum net weight:** *100*</span></span>
        - <span data-ttu-id="e3898-204">**Mængde:** *400*</span><span class="sxs-lookup"><span data-stu-id="e3898-204">**Volume:** *400*</span></span>
        - <span data-ttu-id="e3898-205">**Længde:** *4*</span><span class="sxs-lookup"><span data-stu-id="e3898-205">**Length:** *4*</span></span>
        - <span data-ttu-id="e3898-206">**Bredde:** *10*</span><span class="sxs-lookup"><span data-stu-id="e3898-206">**Width:** *10*</span></span>
        - <span data-ttu-id="e3898-207">**Højde:** *10*</span><span class="sxs-lookup"><span data-stu-id="e3898-207">**Height:** *10*</span></span>

    - <span data-ttu-id="e3898-208">Containertype 2:</span><span class="sxs-lookup"><span data-stu-id="e3898-208">Container type 2:</span></span>

        - <span data-ttu-id="e3898-209">**Containertypekode:** *Kasse-Mellem*</span><span class="sxs-lookup"><span data-stu-id="e3898-209">**Container type code:** *Box-Medium*</span></span>
        - <span data-ttu-id="e3898-210">**Beskrivelse:** *Mellemstor kasse*</span><span class="sxs-lookup"><span data-stu-id="e3898-210">**Description:** *Medium Box*</span></span>
        - <span data-ttu-id="e3898-211">**Maksimal nettovægt:** *50*</span><span class="sxs-lookup"><span data-stu-id="e3898-211">**Maximum net weight:** *50*</span></span>
        - <span data-ttu-id="e3898-212">**Mængde:** *200*</span><span class="sxs-lookup"><span data-stu-id="e3898-212">**Volume:** *200*</span></span>
        - <span data-ttu-id="e3898-213">**Længde:** *2*</span><span class="sxs-lookup"><span data-stu-id="e3898-213">**Length:** *2*</span></span>
        - <span data-ttu-id="e3898-214">**Bredde:** *10*</span><span class="sxs-lookup"><span data-stu-id="e3898-214">**Width:** *10*</span></span>
        - <span data-ttu-id="e3898-215">**Højde:** *10*</span><span class="sxs-lookup"><span data-stu-id="e3898-215">**Height:** *10*</span></span>

    - <span data-ttu-id="e3898-216">Containertype 3:</span><span class="sxs-lookup"><span data-stu-id="e3898-216">Container type 3:</span></span>

        - <span data-ttu-id="e3898-217">**Containertypekode:** *Kasse-Lille*</span><span class="sxs-lookup"><span data-stu-id="e3898-217">**Container type code:** *Box-Small*</span></span>
        - <span data-ttu-id="e3898-218">**Beskrivelse:** *Lille kasse*</span><span class="sxs-lookup"><span data-stu-id="e3898-218">**Description:** *Small Box*</span></span>
        - <span data-ttu-id="e3898-219">**Maksimal nettovægt:** *20*</span><span class="sxs-lookup"><span data-stu-id="e3898-219">**Maximum net weight:** *20*</span></span>
        - <span data-ttu-id="e3898-220">**Mængde:** *100*</span><span class="sxs-lookup"><span data-stu-id="e3898-220">**Volume:** *100*</span></span>
        - <span data-ttu-id="e3898-221">**Længde:** *1*</span><span class="sxs-lookup"><span data-stu-id="e3898-221">**Length:** *1*</span></span>
        - <span data-ttu-id="e3898-222">**Bredde:** *10*</span><span class="sxs-lookup"><span data-stu-id="e3898-222">**Width:** *10*</span></span>
        - <span data-ttu-id="e3898-223">**Højde:** *10*</span><span class="sxs-lookup"><span data-stu-id="e3898-223">**Height:** *10*</span></span>

### <a name="inspect-or-create-container-groups"></a><span data-ttu-id="e3898-224">Undersøge eller oprette containergrupper</span><span class="sxs-lookup"><span data-stu-id="e3898-224">Inspect or create container groups</span></span>

<span data-ttu-id="e3898-225">Benyt følgende fremgangsmåde for at undersøge containergrupper eller oprette nye containergrupper, hvis det er nødvendigt.</span><span class="sxs-lookup"><span data-stu-id="e3898-225">To inspect your container groups, or to create new container groups if they are required, follow these steps.</span></span>

1. <span data-ttu-id="e3898-226">Gå til **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Containergrupper**.</span><span class="sxs-lookup"><span data-stu-id="e3898-226">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container groups**.</span></span>
1. <span data-ttu-id="e3898-227">Kontrollér, at følgende containergrupper er tilgængelige i dine demodata.</span><span class="sxs-lookup"><span data-stu-id="e3898-227">Make sure that the following container group is available in your demo data.</span></span> <span data-ttu-id="e3898-228">Hvis den ikke er tilgængelig, skal du vælge **Ny** for at oprette den.</span><span class="sxs-lookup"><span data-stu-id="e3898-228">If it isn't available, select **New** to create it.</span></span>

    - <span data-ttu-id="e3898-229">**Containergruppe-id:** *Kasser*</span><span class="sxs-lookup"><span data-stu-id="e3898-229">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="e3898-230">**Beskrivelse:** *Kassestørrelser*</span><span class="sxs-lookup"><span data-stu-id="e3898-230">**Description:** *Box sizes*</span></span>

1. <span data-ttu-id="e3898-231">Kontroller, at følgende linjer findes, i oversigtspanelet **Detaljer** for containergruppen *Kasser*.</span><span class="sxs-lookup"><span data-stu-id="e3898-231">On the **Details** FastTab for the *Boxes* container group, make sure that the following lines exist.</span></span> <span data-ttu-id="e3898-232">Hvis ikke, skal du vælge **Ny** for at tilføje dem.</span><span class="sxs-lookup"><span data-stu-id="e3898-232">If they don't, select **New** to add them.</span></span>

    - <span data-ttu-id="e3898-233">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="e3898-233">Line 1:</span></span>

        - <span data-ttu-id="e3898-234">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="e3898-234">**Sequence number:** *1*</span></span>
        - <span data-ttu-id="e3898-235">**Containertype:** *Kasse-Stor*</span><span class="sxs-lookup"><span data-stu-id="e3898-235">**Container type:** *Box-Large*</span></span>
        - <span data-ttu-id="e3898-236">**Containerudnyttelse i procent:** *100*</span><span class="sxs-lookup"><span data-stu-id="e3898-236">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="e3898-237">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="e3898-237">Line 2:</span></span>

        - <span data-ttu-id="e3898-238">**Løbenummer:** *2*</span><span class="sxs-lookup"><span data-stu-id="e3898-238">**Sequence number:** *2*</span></span>
        - <span data-ttu-id="e3898-239">**Containertype:** *Kasse-Mellem*</span><span class="sxs-lookup"><span data-stu-id="e3898-239">**Container type:** *Box-Medium*</span></span>
        - <span data-ttu-id="e3898-240">**Containerudnyttelse i procent:** *100*</span><span class="sxs-lookup"><span data-stu-id="e3898-240">**Container utilization percentage:** *100*</span></span>

    - <span data-ttu-id="e3898-241">Linje 3:</span><span class="sxs-lookup"><span data-stu-id="e3898-241">Line 3:</span></span>

        - <span data-ttu-id="e3898-242">**Løbenummer:** *3*</span><span class="sxs-lookup"><span data-stu-id="e3898-242">**Sequence number:** *3*</span></span>
        - <span data-ttu-id="e3898-243">**Containertype:** *Kasse-Lille*</span><span class="sxs-lookup"><span data-stu-id="e3898-243">**Container type:** *Box-Small*</span></span>
        - <span data-ttu-id="e3898-244">**Containerudnyttelse i procent:** *100*</span><span class="sxs-lookup"><span data-stu-id="e3898-244">**Container utilization percentage:** *100*</span></span>

### <a name="create-a-new-container-build-template"></a><span data-ttu-id="e3898-245">Oprette en ny containerbuildskabelon</span><span class="sxs-lookup"><span data-stu-id="e3898-245">Create a new container build template</span></span>

<span data-ttu-id="e3898-246">Følg disse trin for at oprette en ny containerbuildskabelon:</span><span class="sxs-lookup"><span data-stu-id="e3898-246">To create a new container build template, follow these steps.</span></span>

1. <span data-ttu-id="e3898-247">Gå til **Lokationsstyring** \> **Konfiguration** \> **Containere** \> **Skabelon til container-build**.</span><span class="sxs-lookup"><span data-stu-id="e3898-247">Go to **Warehouse management** \> **Setup** \> **Containers** \> **Container build template**.</span></span>
1. <span data-ttu-id="e3898-248">Vælg **Ny** for at oprette en skabelon til containerbuild, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="e3898-248">Select **New** to create a container build template that has the following settings:</span></span>

    - <span data-ttu-id="e3898-249">**Løbenummer:** *1*</span><span class="sxs-lookup"><span data-stu-id="e3898-249">**Sequence number:** *1*</span></span>
    - <span data-ttu-id="e3898-250">**Containerskabelon-id:** *Kasse*</span><span class="sxs-lookup"><span data-stu-id="e3898-250">**Container template ID:** *Box*</span></span>
    - <span data-ttu-id="e3898-251">**Containergruppe-id:** *Kasser*</span><span class="sxs-lookup"><span data-stu-id="e3898-251">**Container group ID:** *Boxes*</span></span>
    - <span data-ttu-id="e3898-252">**Grundlæggende forespørgselstyper:** *Salgsfordelingslinje*</span><span class="sxs-lookup"><span data-stu-id="e3898-252">**Base query types:** *Sales allocation line*</span></span>
    - <span data-ttu-id="e3898-253">**Kode for bølgetrin:** *234*</span><span class="sxs-lookup"><span data-stu-id="e3898-253">**Wave step code:** *234*</span></span>
    - <span data-ttu-id="e3898-254">**Tillad opdeling af plukninger:** *Ja*</span><span class="sxs-lookup"><span data-stu-id="e3898-254">**Allow split picks:** *Yes*</span></span>
    - <span data-ttu-id="e3898-255">**Pakningsstrategi for containere:** *Pak kun i aktuel container*</span><span class="sxs-lookup"><span data-stu-id="e3898-255">**Container packing strategy:** *Pack into current container only*</span></span>
    - <span data-ttu-id="e3898-256">**Pakning efter vejledningsenhed:** *Nej*</span><span class="sxs-lookup"><span data-stu-id="e3898-256">**Pack by directive unit:** *No*</span></span>

1. <span data-ttu-id="e3898-257">Mens rækken for den nye skabelon stadig er markeret, skal du vælge **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e3898-257">While the row for the new template is still selected, select **Edit query** on the Action Pane.</span></span>
1. <span data-ttu-id="e3898-258">Der vises en standarddialogboks med forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="e3898-258">A standard query editor dialog box appears.</span></span> <span data-ttu-id="e3898-259">Vælg **Tilføj** under fanen **Sortering** for at tilføje en række, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="e3898-259">On the **Sorting** tab, select **Add** to add a row that has the following settings:</span></span>

    - <span data-ttu-id="e3898-260">**Tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="e3898-260">**Table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="e3898-261">**Afledt tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="e3898-261">**Derived table:** *Temporary work transactions*</span></span>
    - <span data-ttu-id="e3898-262">**Felt:** *Ordrenummer*</span><span class="sxs-lookup"><span data-stu-id="e3898-262">**Field:** *Order number*</span></span>
    - <span data-ttu-id="e3898-263">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="e3898-263">**Search direction:** *Ascending*</span></span>

    > [!IMPORTANT]
    > <span data-ttu-id="e3898-264">For at undgå at skulle tjekke alle de andre åbne containere og for at gøre processen hurtigere ved at kontrollere én container ad gangen, skal du bruge strategien *Pak kun i aktuel container* ud over sortering efter ordrenummer.</span><span class="sxs-lookup"><span data-stu-id="e3898-264">To avoid cycling over all the other open containers, and to speed up the process by checking one container at a time, use the *Pack into current container only* strategy in addition to sorting by order number.</span></span> <span data-ttu-id="e3898-265">Denne kombination vil fungere som en arbejdspause i en arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="e3898-265">This combination will work like a work break on a work template.</span></span>

1. <span data-ttu-id="e3898-266">Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="e3898-266">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="e3898-267">Mens rækken for den nye skabelon stadig er markeret, skal du vælge **Begrænsninger i containerblanding** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e3898-267">While the row for the new template is still selected, select **Container mixing constraints** on the Action Pane.</span></span>

    <span data-ttu-id="e3898-268">Du vil nu tilføje en begrænsning, der anbringer varer fra en enkelt ordre i en enkelt container.</span><span class="sxs-lookup"><span data-stu-id="e3898-268">You will now add a constraint that puts items from a single order into a single container.</span></span> <span data-ttu-id="e3898-269">Varer fra en anden ordre anbringes i en separat container.</span><span class="sxs-lookup"><span data-stu-id="e3898-269">Items from any other order will be put into a separate container.</span></span>

1. <span data-ttu-id="e3898-270">Vælg **Ny** for at oprette en blandingsbegrænsning, der har følgende indstillinger:</span><span class="sxs-lookup"><span data-stu-id="e3898-270">Select **New** to create a mixing constraint that has the following settings:</span></span>

    - <span data-ttu-id="e3898-271">**Tabel:** *Salgsordrer*</span><span class="sxs-lookup"><span data-stu-id="e3898-271">**Table:** *Sales orders*</span></span>
    - <span data-ttu-id="e3898-272">**Vælg felt:** *SalesId* (Feltet vises som *Salgsordre* i gitteret).</span><span class="sxs-lookup"><span data-stu-id="e3898-272">**Field select:** *SalesId* (The field will appear as *Sales order* in the grid.)</span></span>

1. <span data-ttu-id="e3898-273">Vælg **OK** for at tilføje begrænsningen.</span><span class="sxs-lookup"><span data-stu-id="e3898-273">Select **OK** to add the constraint.</span></span>
1. <span data-ttu-id="e3898-274">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3898-274">Close the page.</span></span>

### <a name="set-up-a-wave-template-for-containerization"></a><span data-ttu-id="e3898-275">Konfigurere en bølgeskabelon til containerisering</span><span class="sxs-lookup"><span data-stu-id="e3898-275">Set up a wave template for containerization</span></span>

<span data-ttu-id="e3898-276">Følg disse trin for at konfigurere en bølgeskabelon.</span><span class="sxs-lookup"><span data-stu-id="e3898-276">To set up a wave template, follow these steps.</span></span>

1. <span data-ttu-id="e3898-277">Gå til **Lokationsstyring \> Konfiguration \> Bølger \> Bølgeskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="e3898-277">Go to **Warehouse management \> Setup \> Waves \> Wave templates**.</span></span>
1. <span data-ttu-id="e3898-278">I listeruden skal du angive feltet **Bølgeskabelontype** til *Forsendelse*.</span><span class="sxs-lookup"><span data-stu-id="e3898-278">In the list pane, set the **Wave template type** field to *Shipping*.</span></span>
1. <span data-ttu-id="e3898-279">Vælg skabelonen **63 Containerisering** på listen.</span><span class="sxs-lookup"><span data-stu-id="e3898-279">Select the **63 Containerization** template in the list.</span></span>
1. <span data-ttu-id="e3898-280">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e3898-280">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e3898-281">Find følgende linje i kolonnen **Valgte metoder** i oversigtspanelet **Metoder**:</span><span class="sxs-lookup"><span data-stu-id="e3898-281">On the **Methods** FastTab, in the **Selected methods** column, find the following line:</span></span>

    - <span data-ttu-id="e3898-282">**Metodenavn:** *containerisering*</span><span class="sxs-lookup"><span data-stu-id="e3898-282">**Method name:** *containerization*</span></span>
    - <span data-ttu-id="e3898-283">**Navn:** *Containerisering*</span><span class="sxs-lookup"><span data-stu-id="e3898-283">**Name:** *Containerization*</span></span>

1. <span data-ttu-id="e3898-284">Indstil feltet **Kode for bølgetrin** for linjen til *234*.</span><span class="sxs-lookup"><span data-stu-id="e3898-284">Set the **Wave step code** field for the line to *234*.</span></span>

### <a name="set-up-a-work-template"></a><span data-ttu-id="e3898-285">Opsætning af en arbejdsskabelon</span><span class="sxs-lookup"><span data-stu-id="e3898-285">Set up a work template</span></span>

<span data-ttu-id="e3898-286">Følg disse trin for at konfigurere en arbejdsskabelon.</span><span class="sxs-lookup"><span data-stu-id="e3898-286">To set up a work template, follow these steps.</span></span>

1. <span data-ttu-id="e3898-287">Gå til **Lagerstedsstyring \> Opsætning \> Arbejde \> Arbejdsskabeloner**.</span><span class="sxs-lookup"><span data-stu-id="e3898-287">Go to **Warehouse management \> Setup \> Work \> Work templates**.</span></span>
1. <span data-ttu-id="e3898-288">Angiv feltet **Arbejdsordretype** til *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="e3898-288">Set the **Work order type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="e3898-289">Find og vælg den arbejdsskabelon, der skal bruges til pakning af enkelte ordrer pr. container, i gitteret **Oversigt**.</span><span class="sxs-lookup"><span data-stu-id="e3898-289">In the **Overview** grid, find and select the work template that should be used for packing single orders per container.</span></span> <span data-ttu-id="e3898-290">I dette scenario skal du vælge skabelonen **63 Pluk til container**.</span><span class="sxs-lookup"><span data-stu-id="e3898-290">For this scenario, select the **63 Pick to container** template.</span></span>
1. <span data-ttu-id="e3898-291">Vælg **Rediger forespørgsel** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e3898-291">On the Action Pane, select **Edit query**.</span></span>
1. <span data-ttu-id="e3898-292">Der vises en standarddialogboks med forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="e3898-292">A standard query editor dialog box appears.</span></span> <span data-ttu-id="e3898-293">Tilføj følgende linjer under fanen **Sortering**:</span><span class="sxs-lookup"><span data-stu-id="e3898-293">On the **Sorting** tab, add the following lines:</span></span>

    - <span data-ttu-id="e3898-294">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="e3898-294">Line 1:</span></span>

        - <span data-ttu-id="e3898-295">**Tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="e3898-295">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="e3898-296">**Afledt tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="e3898-296">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="e3898-297">**Felt:** *Forsendelses-id*</span><span class="sxs-lookup"><span data-stu-id="e3898-297">**Field:** *Shipment ID*</span></span>
        - <span data-ttu-id="e3898-298">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="e3898-298">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="e3898-299">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="e3898-299">Line 2:</span></span>

        - <span data-ttu-id="e3898-300">**Tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="e3898-300">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="e3898-301">**Afledt tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="e3898-301">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="e3898-302">**Felt:** *Ordrenummer*</span><span class="sxs-lookup"><span data-stu-id="e3898-302">**Field:** *Order number*</span></span>
        - <span data-ttu-id="e3898-303">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="e3898-303">**Search direction:** *Ascending*</span></span>

    - <span data-ttu-id="e3898-304">Linje 3:</span><span class="sxs-lookup"><span data-stu-id="e3898-304">Line 3:</span></span>

        - <span data-ttu-id="e3898-305">**Tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="e3898-305">**Table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="e3898-306">**Afledt tabel:** *Midlertidige arbejdstransaktioner*</span><span class="sxs-lookup"><span data-stu-id="e3898-306">**Derived table:** *Temporary work transactions*</span></span>
        - <span data-ttu-id="e3898-307">**Felt:** *Container-id*</span><span class="sxs-lookup"><span data-stu-id="e3898-307">**Field:** *Container ID*</span></span>
        - <span data-ttu-id="e3898-308">**Søgeretning:** *Stigende*</span><span class="sxs-lookup"><span data-stu-id="e3898-308">**Search direction:** *Ascending*</span></span>

1. <span data-ttu-id="e3898-309">Vælg **OK** for at lukke dialogboksen for forespørgselseditoren.</span><span class="sxs-lookup"><span data-stu-id="e3898-309">Select **OK** to close the query editor dialog box.</span></span>
1. <span data-ttu-id="e3898-310">Du får vist følgende meddelelse: "Gruppering vil blive nulstillet, vil du fortsætte?"</span><span class="sxs-lookup"><span data-stu-id="e3898-310">You receive the following message: "Grouping will be reset, continue?"</span></span> <span data-ttu-id="e3898-311">Vælg **Ja** for at fortsætte.</span><span class="sxs-lookup"><span data-stu-id="e3898-311">Select **Yes** to continue.</span></span>
1. <span data-ttu-id="e3898-312">Mens skabelonen **63 Pluk til container** stadig er valgt, skal du vælge **Opgaveoverskriften skifter** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e3898-312">While the **63 Pick to container** template is still selected, select **Work header breaks** on the Action Pane.</span></span>

    <span data-ttu-id="e3898-313">Du kan nu anvende indstillinger for at afbryde arbejdet, så hver container i ordren knyttes til én arbejdsordre.</span><span class="sxs-lookup"><span data-stu-id="e3898-313">You will now apply settings to break the work so that each container in the order is linked to one work order.</span></span>

1. <span data-ttu-id="e3898-314">Markér afkrydsningsfeltet **Gruppe efter dette felt** for hver række på siden **Opgaveoverskriften skifter** (**Forsendelses-id**, **Ordrenummer** og **Container-id**).</span><span class="sxs-lookup"><span data-stu-id="e3898-314">Select the **Group by this field** checkbox for each row on the **Work header breaks** page (**Shipment ID**, **Order number**, and **Container ID**).</span></span>
1. <span data-ttu-id="e3898-315">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3898-315">Close the page.</span></span>

### <a name="set-up-shipment-consolidation-policies"></a><span data-ttu-id="e3898-316">Konfigurere politikker for forsendelseskonsolidering</span><span class="sxs-lookup"><span data-stu-id="e3898-316">Set up shipment consolidation policies</span></span>

<span data-ttu-id="e3898-317">Følg disse trin for at konfigurere en politik for forsendelseskonsolidering:</span><span class="sxs-lookup"><span data-stu-id="e3898-317">To set up a shipment consolidation policy, follow these steps.</span></span>

1. <span data-ttu-id="e3898-318">Gå til **Lagerstyringssted \> Opsætning \> Frigiv til lagersted \> Politikker for forsendelseskonsolidering**.</span><span class="sxs-lookup"><span data-stu-id="e3898-318">Go to **Warehouse management \> Setup \> Release to warehouse \> Shipment consolidation policies**.</span></span>
1. <span data-ttu-id="e3898-319">Indstil feltet **Politiktype** i listeruden til *Salgsordrer*.</span><span class="sxs-lookup"><span data-stu-id="e3898-319">In the list pane, set the **Policy type** field to *Sales orders*.</span></span>
1. <span data-ttu-id="e3898-320">Vælg politikken **Standard** på listen.</span><span class="sxs-lookup"><span data-stu-id="e3898-320">Select the **Default** policy in the list.</span></span>
1. <span data-ttu-id="e3898-321">Vælg **Rediger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e3898-321">On the Action Pane, select **Edit**.</span></span>
1. <span data-ttu-id="e3898-322">Gå til oversigtspanelet **Konsolideringsfelter** på listen **Valgte felter**, vælg den række, hvor feltet **Feltnavn** er indstillet til *Ordrenummer*.</span><span class="sxs-lookup"><span data-stu-id="e3898-322">On the **Consolidation fields** FastTab, in the **Selected fields** list, select the row where the **Field name** field is set to *Order number*.</span></span>
1. <span data-ttu-id="e3898-323">Vælg knappen **Fjern** ![Venstre pil](media/backward-button.png) for at flytte feltet til listen **Resterende felter**.</span><span class="sxs-lookup"><span data-stu-id="e3898-323">Select the **Remove** button ![Left arrow](media/backward-button.png) to move the field to the **Remaining fields** list.</span></span>
1. <span data-ttu-id="e3898-324">Vælg **Gem** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="e3898-324">On the Action Pane, select **Save**.</span></span>

### <a name="set-up-physical-dimensions-for-the-product"></a><span data-ttu-id="e3898-325">Konfigurere fysiske dimensioner for produktet</span><span class="sxs-lookup"><span data-stu-id="e3898-325">Set up physical dimensions for the product</span></span>

<span data-ttu-id="e3898-326">Hvis du vil konfigurere fysiske dimensioner for de produkter, der skal bruges i dette scenario, skal du følge disse trin.</span><span class="sxs-lookup"><span data-stu-id="e3898-326">To set up physical dimensions for the products that will be used in this scenario, follow these steps.</span></span>

1. <span data-ttu-id="e3898-327">Gå til **Administration af produktoplysninger \> Produkter \> Frigivne produkter**.</span><span class="sxs-lookup"><span data-stu-id="e3898-327">Go to **Product information management \> Products \> Released products**.</span></span>
1. <span data-ttu-id="e3898-328">Vælg det produkt, hvor feltet **Varenummer** er angivet til *A0001*.</span><span class="sxs-lookup"><span data-stu-id="e3898-328">Select the product where the **Item number** field is set to *A0001*.</span></span>
1. <span data-ttu-id="e3898-329">I handlingsruden skal du under fanen **Styr lager** i gruppen **Lager** vælge **Fysiske dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="e3898-329">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="e3898-330">På siden **Fysiske dimensioner** kan du se følgende linje i gitteret:</span><span class="sxs-lookup"><span data-stu-id="e3898-330">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="e3898-331">**Enhed:** *stk.*</span><span class="sxs-lookup"><span data-stu-id="e3898-331">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="e3898-332">**Bruttovægt:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-332">**Gross weight:** *3.00*</span></span>
    - <span data-ttu-id="e3898-333">**Bredde:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-333">**Width:** *2.00*</span></span>
    - <span data-ttu-id="e3898-334">**Dybde:** *2,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-334">**Depth:** *2.00*</span></span>
    - <span data-ttu-id="e3898-335">**Højde:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-335">**Height:** *4.00*</span></span>
    - <span data-ttu-id="e3898-336">**Mængde:** *16,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-336">**Volume:** *16.00*</span></span>

1. <span data-ttu-id="e3898-337">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3898-337">Close the page.</span></span>
1. <span data-ttu-id="e3898-338">Vælg det produkt, hvor feltet **Varenummer** er angivet til *A0002*.</span><span class="sxs-lookup"><span data-stu-id="e3898-338">Select the product where the **Item number** field is set to *A0002*.</span></span>
1. <span data-ttu-id="e3898-339">I handlingsruden skal du under fanen **Styr lager** i gruppen **Lager** vælge **Fysiske dimensioner**.</span><span class="sxs-lookup"><span data-stu-id="e3898-339">On the Action Pane, on the **Manage inventory** tab, in the **Warehouse** group, select **Physical dimensions**.</span></span>
1. <span data-ttu-id="e3898-340">På siden **Fysiske dimensioner** kan du se følgende linje i gitteret:</span><span class="sxs-lookup"><span data-stu-id="e3898-340">On the **Physical dimensions** page, you should see the following line in the grid:</span></span>

    - <span data-ttu-id="e3898-341">**Enhed:** *stk.*</span><span class="sxs-lookup"><span data-stu-id="e3898-341">**Unit:** *pcs*</span></span>
    - <span data-ttu-id="e3898-342">**Bruttovægt:** *4,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-342">**Gross weight:** *4.00*</span></span>
    - <span data-ttu-id="e3898-343">**Bredde:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-343">**Width:** *3.00*</span></span>
    - <span data-ttu-id="e3898-344">**Dybde:** *1,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-344">**Depth:** *1.00*</span></span>
    - <span data-ttu-id="e3898-345">**Højde:** *3,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-345">**Height:** *3.00*</span></span>
    - <span data-ttu-id="e3898-346">**Mængde:** *9,00*</span><span class="sxs-lookup"><span data-stu-id="e3898-346">**Volume:** *9.00*</span></span>

### <a name="create-sales-order-1"></a><span data-ttu-id="e3898-347">Opret salgsordre 1</span><span class="sxs-lookup"><span data-stu-id="e3898-347">Create sales order 1</span></span>

<span data-ttu-id="e3898-348">Følg disse trin for at oprette en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="e3898-348">To create a sales order, follow these steps.</span></span>

1. <span data-ttu-id="e3898-349">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="e3898-349">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e3898-350">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e3898-350">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e3898-351">Der vises en dialogboks til oprettelse af en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="e3898-351">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="e3898-352">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="e3898-352">Set the following values:</span></span>

    - <span data-ttu-id="e3898-353">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e3898-353">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e3898-354">**Lagersted:** *63*</span><span class="sxs-lookup"><span data-stu-id="e3898-354">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="e3898-355">Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e3898-355">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="e3898-356">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="e3898-356">The new sales order is opened.</span></span> <span data-ttu-id="e3898-357">Tilføj følgende salgslinjer i oversigtspanelet **Salgsordrelinjer**:</span><span class="sxs-lookup"><span data-stu-id="e3898-357">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="e3898-358">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="e3898-358">Line 1:</span></span>

        - <span data-ttu-id="e3898-359">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e3898-359">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="e3898-360">**Antal:** *2*</span><span class="sxs-lookup"><span data-stu-id="e3898-360">**Quantity:** *2*</span></span>

    - <span data-ttu-id="e3898-361">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="e3898-361">Line 2:</span></span>

        - <span data-ttu-id="e3898-362">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e3898-362">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="e3898-363">**Antal:** *2*</span><span class="sxs-lookup"><span data-stu-id="e3898-363">**Quantity:** *2*</span></span>

1. <span data-ttu-id="e3898-364">Vælg den første linje, og vælg derefter **Lager \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="e3898-364">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="e3898-365">På siden **Reservation** skal du vælge **Reservér parti**.</span><span class="sxs-lookup"><span data-stu-id="e3898-365">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="e3898-366">Luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="e3898-366">Then close the page.</span></span>
1. <span data-ttu-id="e3898-367">Gentag de to foregående trin for den anden linje.</span><span class="sxs-lookup"><span data-stu-id="e3898-367">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="e3898-368">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3898-368">Close the page.</span></span>

### <a name="create-sales-order-2"></a><span data-ttu-id="e3898-369">Opret salgsordre 2</span><span class="sxs-lookup"><span data-stu-id="e3898-369">Create sales order 2</span></span>

<span data-ttu-id="e3898-370">Følg disse trin for at oprette endnu en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="e3898-370">To create a second sales order, follow these steps.</span></span>

1. <span data-ttu-id="e3898-371">Gå til **Salg og marketing \> Salgsordrer \> Alle salgsordrer**.</span><span class="sxs-lookup"><span data-stu-id="e3898-371">Go to **Sales and marketing \> Sales orders \> All sales orders**.</span></span>
1. <span data-ttu-id="e3898-372">Gå til handlingsruden, og vælg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="e3898-372">On the Action Pane, select **New**.</span></span>
1. <span data-ttu-id="e3898-373">Der vises en dialogboks til oprettelse af en ny salgsordre.</span><span class="sxs-lookup"><span data-stu-id="e3898-373">A dialog box for creating a new sales order appears.</span></span> <span data-ttu-id="e3898-374">Angiv følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="e3898-374">Set the following values:</span></span>

    - <span data-ttu-id="e3898-375">**Debitorkonto:** *US-001*</span><span class="sxs-lookup"><span data-stu-id="e3898-375">**Customer account:** *US-001*</span></span>
    - <span data-ttu-id="e3898-376">**Lagersted:** *63*</span><span class="sxs-lookup"><span data-stu-id="e3898-376">**Warehouse:** *63*</span></span>

1. <span data-ttu-id="e3898-377">Vælg **OK** for at oprette salgsordrerne og lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e3898-377">Select **OK** to create the sales order and close the dialog box.</span></span>
1. <span data-ttu-id="e3898-378">Den nye indkøbsordre åbnes.</span><span class="sxs-lookup"><span data-stu-id="e3898-378">The new sales order is opened.</span></span> <span data-ttu-id="e3898-379">Tilføj følgende salgslinjer i oversigtspanelet **Salgsordrelinjer**:</span><span class="sxs-lookup"><span data-stu-id="e3898-379">On the **Sales order lines** FastTab, add the following sales lines:</span></span>

    - <span data-ttu-id="e3898-380">Linje 1:</span><span class="sxs-lookup"><span data-stu-id="e3898-380">Line 1:</span></span>

        - <span data-ttu-id="e3898-381">**Varenummer:** *A0001*</span><span class="sxs-lookup"><span data-stu-id="e3898-381">**Item number:** *A0001*</span></span>
        - <span data-ttu-id="e3898-382">**Antal:** *4*</span><span class="sxs-lookup"><span data-stu-id="e3898-382">**Quantity:** *4*</span></span>

    - <span data-ttu-id="e3898-383">Linje 2:</span><span class="sxs-lookup"><span data-stu-id="e3898-383">Line 2:</span></span>

        - <span data-ttu-id="e3898-384">**Varenummer:** *A0002*</span><span class="sxs-lookup"><span data-stu-id="e3898-384">**Item number:** *A0002*</span></span>
        - <span data-ttu-id="e3898-385">**Antal:** *4*</span><span class="sxs-lookup"><span data-stu-id="e3898-385">**Quantity:** *4*</span></span>

1. <span data-ttu-id="e3898-386">Vælg den første linje, og vælg derefter **Lager \> Reservation**.</span><span class="sxs-lookup"><span data-stu-id="e3898-386">Select the first line, and then select **Inventory \> Reservation**.</span></span>
1. <span data-ttu-id="e3898-387">På siden **Reservation** skal du vælge **Reservér parti**.</span><span class="sxs-lookup"><span data-stu-id="e3898-387">On the **Reservation** page, select **Reserve lot**.</span></span> <span data-ttu-id="e3898-388">Luk derefter siden.</span><span class="sxs-lookup"><span data-stu-id="e3898-388">Then close the page.</span></span>
1. <span data-ttu-id="e3898-389">Gentag de to foregående trin for den anden linje.</span><span class="sxs-lookup"><span data-stu-id="e3898-389">Repeat the previous two steps for the second line.</span></span>
1. <span data-ttu-id="e3898-390">Luk siden.</span><span class="sxs-lookup"><span data-stu-id="e3898-390">Close the page.</span></span>

### <a name="create-the-load"></a><span data-ttu-id="e3898-391">Oprette lasten</span><span class="sxs-lookup"><span data-stu-id="e3898-391">Create the load</span></span>

<span data-ttu-id="e3898-392">Udfør følgende trin for at oprette en last for hvert ordre, du har oprettet i dette scenarie, og frigiv den derefter til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="e3898-392">To create a load for each order that you created for this scenario and then release it to the warehouse, follow these steps.</span></span>

1. <span data-ttu-id="e3898-393">Gå til **Lagerstedsstyring \> Laster \> Panelet Lastplanlægning**.</span><span class="sxs-lookup"><span data-stu-id="e3898-393">Go to **Warehouse management \> Loads \> Load planning workbench**.</span></span>
1. <span data-ttu-id="e3898-394">Under fanen **Salgslinjer** kan du finde og vælge alle salgsordrelinjer fra de salgsordrer, du har oprettet for dette scenario.</span><span class="sxs-lookup"><span data-stu-id="e3898-394">On the **Sales lines** tab, find and select all the sales order lines from the sales orders that you created for this scenario.</span></span>
1. <span data-ttu-id="e3898-395">I handlingsruden skal du under fanen **Udbud og efterspørgsel** i gruppen **Tilføj** vælge **Til ny last**.</span><span class="sxs-lookup"><span data-stu-id="e3898-395">On the Action Pane, on the **Supply and demand** tab, in the **Add** group, select **To new load**.</span></span> <span data-ttu-id="e3898-396">De valgte ordrelinjer føjes til en ny last.</span><span class="sxs-lookup"><span data-stu-id="e3898-396">The selected order lines are added to a new load.</span></span>
1. <span data-ttu-id="e3898-397">I dialogboksen **Tildeling af lastskabelon** skal du gå til feltet **Lastskabelon-id** og vælge en lastskabelon, f.eks. *40' Container*.</span><span class="sxs-lookup"><span data-stu-id="e3898-397">In the **Load template assignment** dialog box, in the **Load template ID** field, select a load template, such as *40' Container*.</span></span>
1. <span data-ttu-id="e3898-398">Vælg **OK** for at lukke dialogboksen.</span><span class="sxs-lookup"><span data-stu-id="e3898-398">Select **OK** to close the dialog box.</span></span>
1. <span data-ttu-id="e3898-399">I sektionen **Laster** skal du vælge og finde den last, du lige har oprettet.</span><span class="sxs-lookup"><span data-stu-id="e3898-399">In the **Loads** section, find and select the load that you just created.</span></span>
1. <span data-ttu-id="e3898-400">Vælg **Frigiv \> Frigiv til lagersted**.</span><span class="sxs-lookup"><span data-stu-id="e3898-400">Select **Release \> Release to warehouse**.</span></span>
1. <span data-ttu-id="e3898-401">I dialogboksen **Frigiv til lagersted** skal du vælge **OK** for at frigive den valgte last til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="e3898-401">In the **Release to warehouse** dialog box, select **OK** to release the selected load to the warehouse.</span></span>

### <a name="verify-the-shipments-and-containers"></a><span data-ttu-id="e3898-402">Kontrollere forsendelser og containere</span><span class="sxs-lookup"><span data-stu-id="e3898-402">Verify the shipments and containers</span></span>

<span data-ttu-id="e3898-403">I følgende procedure kan du kontrollere de forsendelser, der er oprettet.</span><span class="sxs-lookup"><span data-stu-id="e3898-403">The following procedure lets you verify the shipments that have been created.</span></span> <span data-ttu-id="e3898-404">Du kan bruge den til at gennemse den ordre, du har oprettet til dette scenario, for at sikre dig, at du har opnået de forventede resultater.</span><span class="sxs-lookup"><span data-stu-id="e3898-404">Use it to review the order that you created for this scenario, to make sure that you've obtained the expected results.</span></span>

1. <span data-ttu-id="e3898-405">Gå til **Lagerstyringssted \> Forsendelser \> Alle forsendelser**.</span><span class="sxs-lookup"><span data-stu-id="e3898-405">Go to **Warehouse management \> Shipments \> All shipments**.</span></span>
1. <span data-ttu-id="e3898-406">Find og vælg den forsendelse, der er oprettet for den last, du netop har frigivet.</span><span class="sxs-lookup"><span data-stu-id="e3898-406">Find and select the shipment that was created for the load that you just released.</span></span>
1. <span data-ttu-id="e3898-407">Åbn fanen **Transport** i handlingsruden, og vælg **Vis containere**.</span><span class="sxs-lookup"><span data-stu-id="e3898-407">On the Action Pane, on the **Transportation** tab, select **View containers**.</span></span>
1. <span data-ttu-id="e3898-408">Bekræft, at varerne fra salgsordrerne er pakket i to forskellige containere.</span><span class="sxs-lookup"><span data-stu-id="e3898-408">Confirm that the items from the sales orders were containerized into two different containers.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="e3898-409">Yderligere ressourcer</span><span class="sxs-lookup"><span data-stu-id="e3898-409">Additional resources</span></span>

- [<span data-ttu-id="e3898-410">Containerisering</span><span class="sxs-lookup"><span data-stu-id="e3898-410">Containerization</span></span>](wave-containerization.md)
