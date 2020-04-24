---
title: Konfigurere medarbejderselvbetjening
description: I Microsoft Dynamics 365 Human Resources kan du konfigurere felter til navigation på øverste niveau i medarbejderselvbetjening.
author: andreabichsel
manager: AnnBe
ms.date: 04/06/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: dbbcb10f1d14088435248c3354ac153b23e5f8d7
ms.sourcegitcommit: a9461650d11d6845e1942865ebf7e35f75f61ad3
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/06/2020
ms.locfileid: "3229803"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="f7ed5-103">Konfigurere medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="f7ed5-103">Configure employee self service</span></span>

<span data-ttu-id="f7ed5-104">I Microsoft Dynamics 365 Human Resources kan du konfigurere felter til navigation på øverste niveau i medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="f7ed5-105">Frynsegodeplansfelter sender brugere videre til frynsegodeplaner, som de er berettiget til.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-105">Benefit plan tiles direct users to benefit plans that they're eligible for.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="f7ed5-106">Konfigurere et felt til frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="f7ed5-106">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="f7ed5-107">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f7ed5-108">Vælg fanen **Konfigurer felt til frynsegodeplaner**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-108">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f7ed5-109">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="f7ed5-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f7ed5-110">Felt</span><span class="sxs-lookup"><span data-stu-id="f7ed5-110">Field</span></span> | <span data-ttu-id="f7ed5-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f7ed5-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f7ed5-112">**Felt-id**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-112">**Tile ID**</span></span> | <span data-ttu-id="f7ed5-113">Entydigt id for feltet.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f7ed5-114">**Feltlabeltekst**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-114">**Tile label text**</span></span> | <span data-ttu-id="f7ed5-115">Den tekst, der vises for feltet på selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="f7ed5-116">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-116">**Description**</span></span> | <span data-ttu-id="f7ed5-117">En beskrivelse af feltet.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-117">A description of the tile.</span></span> |
   | <span data-ttu-id="f7ed5-118">**Internetadresse**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-118">**Internet address**</span></span> | <span data-ttu-id="f7ed5-119">Angiv URL-adressen på siden med medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f7ed5-120">**Feltstørrelse**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-120">**Tile size**</span></span> | <span data-ttu-id="f7ed5-121">Feltets størrelse: lille, mellem eller stor.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f7ed5-122">**Destination**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-122">**Target**</span></span> | <span data-ttu-id="f7ed5-123">Angiver, om siden skal åbnes i et nyt vindue eller i det aktuelle vindue.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f7ed5-124">**Feltbaggrundsbillede**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-124">**Tile background image**</span></span> | <span data-ttu-id="f7ed5-125">URL-adressen for det billede, der skal bruges til feltet (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="f7ed5-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f7ed5-126">**Igangsætning**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-126">**Start**</span></span> | <span data-ttu-id="f7ed5-127">Startdato og -tidspunkt, hvor feltet vil blive tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f7ed5-128">**End**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-128">**End**</span></span> | <span data-ttu-id="f7ed5-129">Slutdato og -tidspunkt, hvor feltet vil være tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f7ed5-130">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-130">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="f7ed5-131">Konfigurere et felt for flekskreditplan</span><span class="sxs-lookup"><span data-stu-id="f7ed5-131">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="f7ed5-132">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="f7ed5-133">Vælg fanen **Konfigurer felt til flekskreditplan**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-133">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="f7ed5-134">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="f7ed5-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="f7ed5-135">Felt</span><span class="sxs-lookup"><span data-stu-id="f7ed5-135">Field</span></span> | <span data-ttu-id="f7ed5-136">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f7ed5-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="f7ed5-137">**Felt-id**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-137">**Tile ID**</span></span> | <span data-ttu-id="f7ed5-138">Entydigt id for feltet.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="f7ed5-139">**Feltlabeltekst**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-139">**Tile label text**</span></span> | <span data-ttu-id="f7ed5-140">Den tekst, der vises for feltet Selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-140">The text that will appear for the tile on Self service.</span></span> |
   | <span data-ttu-id="f7ed5-141">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-141">**Description**</span></span> | <span data-ttu-id="f7ed5-142">En beskrivelse af feltet.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-142">A description of the tile.</span></span> |
   | <span data-ttu-id="f7ed5-143">**Internetadresse**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-143">**Internet address**</span></span> | <span data-ttu-id="f7ed5-144">Angiv URL-adressen på siden med medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="f7ed5-145">**Feltstørrelse**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-145">**Tile size**</span></span> | <span data-ttu-id="f7ed5-146">Feltets størrelse: lille, mellem eller stor.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="f7ed5-147">**Destination**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-147">**Target**</span></span> | <span data-ttu-id="f7ed5-148">Angiver, om siden skal åbnes i et nyt vindue eller i det aktuelle vindue.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="f7ed5-149">**Feltbaggrundsbillede**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-149">**Tile background image**</span></span> | <span data-ttu-id="f7ed5-150">URL-adressen for det billede, der skal bruges til feltet (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="f7ed5-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="f7ed5-151">**Igangsætning**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-151">**Start**</span></span> | <span data-ttu-id="f7ed5-152">Startdato og -tidspunkt, hvor feltet vil blive tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="f7ed5-153">**End**</span><span class="sxs-lookup"><span data-stu-id="f7ed5-153">**End**</span></span> | <span data-ttu-id="f7ed5-154">Slutdato og -tidspunkt, hvor feltet vil være tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="f7ed5-155">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="f7ed5-155">Select **Save**.</span></span>
