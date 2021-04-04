---
title: Forsendelsescontainere
description: Dette emne beskriver, hvordan du konfigurerer forsendelsescontainere for modulet Landingsomkostninger.
author: sherry-zheng
manager: tfehr
ms.date: 12/09/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ITMContainerTypeTable, ITMContainerTable, ITMContainerUnitTypeTable, ITMRefrigerationTypeTable, ITMContainersListPage, ITMContainers
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: chuzheng
ms.search.validFrom: 2020-12-09
ms.dyn365.ops.version: Release 10.0.17
ms.openlocfilehash: ca712aa7f07792861d5ba36afd8d7b63cc9ce8fb
ms.sourcegitcommit: 2b4809e60974e72df9476ffd62706b1bfc8da4a7
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/04/2021
ms.locfileid: "5500952"
---
# <a name="shipping-container-setup"></a><span data-ttu-id="706a9-103">Opsætning af forsendelsescontainere</span><span class="sxs-lookup"><span data-stu-id="706a9-103">Shipping container setup</span></span>

[!include [banner](../../includes/banner.md)]
[!include [preview banner](../includes/preview-banner.md)]

<span data-ttu-id="706a9-104">Dette emne beskriver, hvordan du konfigurerer forsendelsescontainere for modulet **Landingsomkostninger**.</span><span class="sxs-lookup"><span data-stu-id="706a9-104">This topic describes how to set up shipping containers for the **Landed cost** module.</span></span>

## <a name="set-up-shipping-container-types"></a><a id="shipping-container-types"></a><span data-ttu-id="706a9-105">Konfigurere forsendelsescontainertyper</span><span class="sxs-lookup"><span data-stu-id="706a9-105">Set up shipping container types</span></span>

<span data-ttu-id="706a9-106">Forsendelsescontainertyper definerer de typer forsendelsescontainere, der er tilgængelige for brug under forsendelse og fragt.</span><span class="sxs-lookup"><span data-stu-id="706a9-106">Shipping container types define the types of shipping containers that are available for use during shipping and voyages.</span></span>

<span data-ttu-id="706a9-107">Du kan arbejde med forsendelsescontainertyper ved at gå til **Landingsomkostninger \> Opsætning af containere \> Forsendelsescontainertyper**.</span><span class="sxs-lookup"><span data-stu-id="706a9-107">To work with the shipping container types, go to **Landed cost \> Containers setup \> Shipping container types**.</span></span> <span data-ttu-id="706a9-108">Her kan du se, tilføje og fjerne poster for dine containertyper.</span><span class="sxs-lookup"><span data-stu-id="706a9-108">There, you can view, add, and remove records for your container types.</span></span> <span data-ttu-id="706a9-109">I følgende tabel forklares de felter, der er tilgængelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="706a9-109">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="706a9-110">Felt</span><span class="sxs-lookup"><span data-stu-id="706a9-110">Field</span></span> | <span data-ttu-id="706a9-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="706a9-111">Description</span></span> |
|---|---|
| <span data-ttu-id="706a9-112">Forsendelsescontainertype</span><span class="sxs-lookup"><span data-stu-id="706a9-112">Shipping container type</span></span> | <span data-ttu-id="706a9-113">Angiv et entydigt id-navn/-nummer for forsendelsescontainertypen.</span><span class="sxs-lookup"><span data-stu-id="706a9-113">Enter a unique identification name/number for the shipping container type.</span></span> |
| <span data-ttu-id="706a9-114">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="706a9-114">Description</span></span> | <span data-ttu-id="706a9-115">Angiv en beskrivelse af forsendelsescontainertypen.</span><span class="sxs-lookup"><span data-stu-id="706a9-115">Enter a description of the shipping container type.</span></span> |
| <span data-ttu-id="706a9-116">Mængde</span><span class="sxs-lookup"><span data-stu-id="706a9-116">Volume</span></span> | <span data-ttu-id="706a9-117">Angiv den maksimale mængde, der er tilladt i denne forsendelsescontainertype.</span><span class="sxs-lookup"><span data-stu-id="706a9-117">Enter the maximum volume that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="706a9-118">Tykkelse</span><span class="sxs-lookup"><span data-stu-id="706a9-118">Weight</span></span> | <span data-ttu-id="706a9-119">Angiv den maksimale vægt, der er tilladt i denne forsendelsescontainertype.</span><span class="sxs-lookup"><span data-stu-id="706a9-119">Enter the maximum weight that is allowed in shipping containers of this type.</span></span> |
| <span data-ttu-id="706a9-120">Kan returneres</span><span class="sxs-lookup"><span data-stu-id="706a9-120">Returnable</span></span> | <span data-ttu-id="706a9-121">Angiv, om denne forsendelsescontainertype kan returneres til leverandøren, når den er brugt under en fragt.</span><span class="sxs-lookup"><span data-stu-id="706a9-121">Specify whether shipping containers of this type can be returned to the vendor after they are used during a voyage.</span></span> <span data-ttu-id="706a9-122">Hvis denne indstilling er angivet til *Ja*, kan der gælde yderligere omkostninger for returnering af denne forsendelsescontainertype til oprindelseshavnen.</span><span class="sxs-lookup"><span data-stu-id="706a9-122">If this option is set to *Yes*, additional costs might apply for the return of shipping containers of this type to the port of origin.</span></span> |

## <a name="set-up-shipping-containers"></a><span data-ttu-id="706a9-123">Konfigurere forsendelsescontainere</span><span class="sxs-lookup"><span data-stu-id="706a9-123">Set up shipping containers</span></span>

<span data-ttu-id="706a9-124">Du bruger forsendelsescontainerposter til at identificere hver container, du bruger under fragt.</span><span class="sxs-lookup"><span data-stu-id="706a9-124">You use shipping container records to identify each container that you use during voyages.</span></span> <span data-ttu-id="706a9-125">Når du opretter en fragt, kan du vælge en bestemt container til den på listen over alle de forsendelsescontainerposter, du her har defineret.</span><span class="sxs-lookup"><span data-stu-id="706a9-125">When you create a voyage, you can select a specific container for it in the list of all the shipping container records that you've defined here.</span></span> <span data-ttu-id="706a9-126">Denne funktion er især nyttig, hvis dit firma ejer egne forsendelsescontainere.</span><span class="sxs-lookup"><span data-stu-id="706a9-126">This feature is especially useful if your company owns its own shipping containers.</span></span>

<span data-ttu-id="706a9-127">Du behøver ikke at angive forsendelsescontainernumre for forsendelsescontainere, der kun bruges én gang.</span><span class="sxs-lookup"><span data-stu-id="706a9-127">You don't have to enter shipping container numbers for shipping containers that will be used only one time.</span></span> <span data-ttu-id="706a9-128">Du kan i stedet tilføje forsendelsescontainernummeret, når du opretter en fragt.</span><span class="sxs-lookup"><span data-stu-id="706a9-128">Instead, you can add the shipping container number when you create a voyage.</span></span>

<span data-ttu-id="706a9-129">Forsendelsescontainerposter bruges kun i Landingsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="706a9-129">Shipping container records are used only in Landed cost.</span></span> <span data-ttu-id="706a9-130">De er ikke tilgængelige i standardmodulet **Transportstyring** (TMS).</span><span class="sxs-lookup"><span data-stu-id="706a9-130">They aren't available in the standard **Transportation management** module (TMS).</span></span>

<span data-ttu-id="706a9-131">Du kan arbejde med forsendelsescontainere ved at gå til **Landingsomkostninger \> Opsætning af containere \> Forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="706a9-131">To work with shipping containers, go to **Landed cost \> Containers setup \> Shipping containers**.</span></span> <span data-ttu-id="706a9-132">Her kan du se, tilføje og fjerne poster for dine forsendelsescontainere.</span><span class="sxs-lookup"><span data-stu-id="706a9-132">There, you can view, add, and remove records your shipping containers.</span></span> <span data-ttu-id="706a9-133">I følgende tabel forklares de felter, der er tilgængelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="706a9-133">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="706a9-134">Felt</span><span class="sxs-lookup"><span data-stu-id="706a9-134">Field</span></span> | <span data-ttu-id="706a9-135">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="706a9-135">Description</span></span> |
|---|---|
| <span data-ttu-id="706a9-136">Forsendelsescontainer</span><span class="sxs-lookup"><span data-stu-id="706a9-136">Shipping container</span></span> | <span data-ttu-id="706a9-137">Angiv et entydigt id-navn/-nummer for forsendelsescontaineren.</span><span class="sxs-lookup"><span data-stu-id="706a9-137">Enter a unique identification name/number for the shipping container.</span></span> |
| <span data-ttu-id="706a9-138">Forsendelsescontainertype</span><span class="sxs-lookup"><span data-stu-id="706a9-138">Shipping container type</span></span> | <span data-ttu-id="706a9-139">Vælg typen af forsendelsescontainer.</span><span class="sxs-lookup"><span data-stu-id="706a9-139">Select the type of shipping container.</span></span> <span data-ttu-id="706a9-140">Yderligere oplysninger kan du se i afsnittet [Konfigurere forsendelsescontainertyper](#shipping-container-types) tidligere i dette emne.</span><span class="sxs-lookup"><span data-stu-id="706a9-140">For more information, see the [Set up shipping container types](#shipping-container-types) section earlier in this topic.</span></span> |

> [!NOTE]
> - <span data-ttu-id="706a9-141">Opsætningen af forsendelsescontaineren er valgfri.</span><span class="sxs-lookup"><span data-stu-id="706a9-141">The shipping container setup is optional.</span></span> <span data-ttu-id="706a9-142">Du vil typisk kun bruge den, hvis dit firma ejer sine egne forsendelsescontainere eller ofte genbruger de samme forsendelsescontainere.</span><span class="sxs-lookup"><span data-stu-id="706a9-142">Typically, you will use it only if your company owns its own shipping containers or often reuses the same shipping containers.</span></span>
> - <span data-ttu-id="706a9-143">Der beregnes ingen kontrolcifre for forsendelsescontainernumre.</span><span class="sxs-lookup"><span data-stu-id="706a9-143">No check digits are calculated for shipping container numbers.</span></span>

## <a name="set-up-unit-types"></a><a name="unit-types"></a><span data-ttu-id="706a9-144">Konfigurere enhedstyper</span><span class="sxs-lookup"><span data-stu-id="706a9-144">Set up unit types</span></span>

<span data-ttu-id="706a9-145">Enhedstyper opretter yderligere grupperinger og identifikationsmetoder for forsendelsescontainere.</span><span class="sxs-lookup"><span data-stu-id="706a9-145">Unit types establish additional groupings and identification methods for shipping containers.</span></span> <span data-ttu-id="706a9-146">Enhedstypen bruges typisk til at identificere den type container, som varer pakkes i, f.eks. paller eller tønder.</span><span class="sxs-lookup"><span data-stu-id="706a9-146">The unit type is typically used to identify the type of container that goods are packaged in, such as pallets or drums.</span></span> <span data-ttu-id="706a9-147">Du kan vælge en enhedstype, når du konfigurerer en container på siden **Alle forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="706a9-147">You can select a unit type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="706a9-148">Enhedstyper bruges kun i Landingsomkostninger.</span><span class="sxs-lookup"><span data-stu-id="706a9-148">Unit types are used only in Landed cost.</span></span> <span data-ttu-id="706a9-149">De er ikke tilgængelige i TMS.</span><span class="sxs-lookup"><span data-stu-id="706a9-149">They aren't available in TMS.</span></span>

<span data-ttu-id="706a9-150">Du kan arbejde med enhedstyper ved at gå til **Landingsomkostninger \> Opsætning af containere \> Enhedstyper**.</span><span class="sxs-lookup"><span data-stu-id="706a9-150">To work with unit types, go to **Landed cost \> Containers setup \> Unit types**.</span></span> <span data-ttu-id="706a9-151">Her kan du se, tilføje og fjerne poster for dine enhedstyper.</span><span class="sxs-lookup"><span data-stu-id="706a9-151">There, you can view, add, and remove records for your unit types.</span></span> <span data-ttu-id="706a9-152">I følgende tabel forklares de felter, der er tilgængelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="706a9-152">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="706a9-153">Felt</span><span class="sxs-lookup"><span data-stu-id="706a9-153">Field</span></span> | <span data-ttu-id="706a9-154">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="706a9-154">Description</span></span> |
|---|---|
| <span data-ttu-id="706a9-155">Enhedstype</span><span class="sxs-lookup"><span data-stu-id="706a9-155">Unit type</span></span> | <span data-ttu-id="706a9-156">Angiv et entydigt id-navn/-nummer for enhedstypen.</span><span class="sxs-lookup"><span data-stu-id="706a9-156">Enter a unique identification name/number for the unit type.</span></span> |
| <span data-ttu-id="706a9-157">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="706a9-157">Description</span></span> | <span data-ttu-id="706a9-158">Angiv en beskrivelse af enhedstypen.</span><span class="sxs-lookup"><span data-stu-id="706a9-158">Enter a description of the unit type.</span></span> |

## <a name="set-up-refrigeration-types"></a><a name="refrigeration-types"></a><span data-ttu-id="706a9-159">Definere afkølingstyper</span><span class="sxs-lookup"><span data-stu-id="706a9-159">Set up refrigeration types</span></span>

<span data-ttu-id="706a9-160">Afkølingstyper opretter yderligere grupperinger og identifikationsmetoder for forsendelsescontainere (normalt afkølede containere).</span><span class="sxs-lookup"><span data-stu-id="706a9-160">Refrigeration types establish additional groupings and identification methods for shipping containers (usually refrigerated containers).</span></span> <span data-ttu-id="706a9-161">Du kan vælge en afkølingstype, når du konfigurerer en container på siden **Alle forsendelsescontainere**.</span><span class="sxs-lookup"><span data-stu-id="706a9-161">You can select a refrigeration type when you set up a container on the **All shipping containers** page.</span></span>

<span data-ttu-id="706a9-162">Du kan arbejde med afkølingstyper ved at gå til **Landingsomkostninger \> Opsætning af containere \> Afkølingstyper**.</span><span class="sxs-lookup"><span data-stu-id="706a9-162">To work with refrigeration types, go to **Landed cost \> Containers setup \> Refrigeration types**.</span></span> <span data-ttu-id="706a9-163">Her kan du se, tilføje og fjerne poster for dine afkølingstyper.</span><span class="sxs-lookup"><span data-stu-id="706a9-163">There, you can view, add, and remove records for your refrigeration types.</span></span> <span data-ttu-id="706a9-164">I følgende tabel forklares de felter, der er tilgængelige for hver post.</span><span class="sxs-lookup"><span data-stu-id="706a9-164">The following table describes the fields that are available for each record.</span></span>

| <span data-ttu-id="706a9-165">Felt</span><span class="sxs-lookup"><span data-stu-id="706a9-165">Field</span></span> | <span data-ttu-id="706a9-166">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="706a9-166">Description</span></span> |
|---|---|
| <span data-ttu-id="706a9-167">Afkølingstype</span><span class="sxs-lookup"><span data-stu-id="706a9-167">Refrigeration type</span></span> | <span data-ttu-id="706a9-168">Angiv et entydigt id-navn/-nummer for afkølingstypen.</span><span class="sxs-lookup"><span data-stu-id="706a9-168">Enter a unique identification name/number for the refrigeration type.</span></span> |
| <span data-ttu-id="706a9-169">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="706a9-169">Description</span></span> | <span data-ttu-id="706a9-170">Angiv en beskrivelse af afkølingstypen.</span><span class="sxs-lookup"><span data-stu-id="706a9-170">Enter a description of the refrigeration type.</span></span> |
