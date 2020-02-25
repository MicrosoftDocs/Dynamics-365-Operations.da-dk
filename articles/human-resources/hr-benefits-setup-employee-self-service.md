---
title: Konfigurere medarbejderselvbetjening
description: ''
author: andreabichsel
manager: AnnBe
ms.date: 02/03/2020
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
ms.openlocfilehash: e44a35071b8d0987e6c949fb11312204317b44a1
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/03/2020
ms.locfileid: "3008497"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="c1ea5-102">Konfigurere medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="c1ea5-102">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="c1ea5-103">I Microsoft Dynamics 365 Human Resources kan du konfigurere felter til navigation på øverste niveau i medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-103">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="c1ea5-104">Frynsegodeplansfelter sender brugere videre til frynsegodeplaner som de er berettiget til at tilmelde sig.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-104">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="c1ea5-105">Oprette et felt i et rollebaseret område</span><span class="sxs-lookup"><span data-stu-id="c1ea5-105">Set up a role center tile</span></span>

1. <span data-ttu-id="c1ea5-106">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-106">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="c1ea5-107">Vælg fanen **Opsætning af rollebaseret område**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-107">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="c1ea5-108">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="c1ea5-108">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c1ea5-109">Felt</span><span class="sxs-lookup"><span data-stu-id="c1ea5-109">Field</span></span> | <span data-ttu-id="c1ea5-110">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-110">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c1ea5-111">Felt-id</span><span class="sxs-lookup"><span data-stu-id="c1ea5-111">Tile ID</span></span> | <span data-ttu-id="c1ea5-112">Entydigt id for feltet.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-112">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="c1ea5-113">Feltlabeltekst</span><span class="sxs-lookup"><span data-stu-id="c1ea5-113">Tile label text</span></span> | <span data-ttu-id="c1ea5-114">Den tekst, der vises for feltet på selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-114">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="c1ea5-115">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-115">Description</span></span> | <span data-ttu-id="c1ea5-116">En beskrivelse af feltet.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-116">A description of the tile.</span></span> |
   | <span data-ttu-id="c1ea5-117">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-117">Internet address</span></span> | <span data-ttu-id="c1ea5-118">Angiv URL-adressen på siden med medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-118">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="c1ea5-119">Feltstørrelse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-119">Tile size</span></span> | <span data-ttu-id="c1ea5-120">Feltets størrelse: lille, mellem eller stor.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-120">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="c1ea5-121">Destination</span><span class="sxs-lookup"><span data-stu-id="c1ea5-121">Target</span></span> | <span data-ttu-id="c1ea5-122">Angiver, om siden skal åbnes i et nyt vindue eller i det aktuelle vindue.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-122">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="c1ea5-123">Feltbaggrundsbillede</span><span class="sxs-lookup"><span data-stu-id="c1ea5-123">Tile background image</span></span> | <span data-ttu-id="c1ea5-124">URL-adressen for det billede, der skal bruges til feltet (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="c1ea5-124">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="c1ea5-125">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="c1ea5-125">Start</span></span> | <span data-ttu-id="c1ea5-126">Startdato og -tidspunkt, hvor feltet vil blive tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-126">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="c1ea5-127">End</span><span class="sxs-lookup"><span data-stu-id="c1ea5-127">End</span></span> | <span data-ttu-id="c1ea5-128">Slutdato og -tidspunkt, hvor feltet vil være tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-128">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="c1ea5-129">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-129">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="c1ea5-130">Konfigurere et felt til frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="c1ea5-130">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="c1ea5-131">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-131">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="c1ea5-132">Vælg fanen **Konfigurer felt til frynsegodeplaner**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-132">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="c1ea5-133">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="c1ea5-133">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c1ea5-134">Felt</span><span class="sxs-lookup"><span data-stu-id="c1ea5-134">Field</span></span> | <span data-ttu-id="c1ea5-135">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-135">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c1ea5-136">Felt-id</span><span class="sxs-lookup"><span data-stu-id="c1ea5-136">Tile ID</span></span> | <span data-ttu-id="c1ea5-137">Entydigt id for feltet.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-137">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="c1ea5-138">Feltlabeltekst</span><span class="sxs-lookup"><span data-stu-id="c1ea5-138">Tile label text</span></span> | <span data-ttu-id="c1ea5-139">Den tekst, der vises for feltet på selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-139">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="c1ea5-140">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-140">Description</span></span> | <span data-ttu-id="c1ea5-141">En beskrivelse af feltet.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-141">A description of the tile.</span></span> |
   | <span data-ttu-id="c1ea5-142">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-142">Internet address</span></span> | <span data-ttu-id="c1ea5-143">Angiv URL-adressen på siden med medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-143">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="c1ea5-144">Feltstørrelse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-144">Tile size</span></span> | <span data-ttu-id="c1ea5-145">Feltets størrelse: lille, mellem eller stor.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-145">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="c1ea5-146">Destination</span><span class="sxs-lookup"><span data-stu-id="c1ea5-146">Target</span></span> | <span data-ttu-id="c1ea5-147">Angiver, om siden skal åbnes i et nyt vindue eller i det aktuelle vindue.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-147">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="c1ea5-148">Feltbaggrundsbillede</span><span class="sxs-lookup"><span data-stu-id="c1ea5-148">Tile background image</span></span> | <span data-ttu-id="c1ea5-149">URL-adressen for det billede, der skal bruges til feltet (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="c1ea5-149">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="c1ea5-150">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="c1ea5-150">Start</span></span> | <span data-ttu-id="c1ea5-151">Startdato og -tidspunkt, hvor feltet vil blive tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-151">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="c1ea5-152">End</span><span class="sxs-lookup"><span data-stu-id="c1ea5-152">End</span></span> | <span data-ttu-id="c1ea5-153">Slutdato og -tidspunkt, hvor feltet vil være tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-153">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="c1ea5-154">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-154">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="c1ea5-155">Konfigurere et felt for flekskreditplan</span><span class="sxs-lookup"><span data-stu-id="c1ea5-155">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="c1ea5-156">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-156">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="c1ea5-157">Vælg fanen **Konfigurer felt til flekskreditplan**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-157">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="c1ea5-158">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="c1ea5-158">Specify values for the following fields:</span></span>

   | <span data-ttu-id="c1ea5-159">Felt</span><span class="sxs-lookup"><span data-stu-id="c1ea5-159">Field</span></span> | <span data-ttu-id="c1ea5-160">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-160">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="c1ea5-161">Felt-id</span><span class="sxs-lookup"><span data-stu-id="c1ea5-161">Tile ID</span></span> | <span data-ttu-id="c1ea5-162">Entydigt id for feltet.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-162">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="c1ea5-163">Feltlabeltekst</span><span class="sxs-lookup"><span data-stu-id="c1ea5-163">Tile label text</span></span> | <span data-ttu-id="c1ea5-164">Den tekst, der vises for feltet på selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-164">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="c1ea5-165">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-165">Description</span></span> | <span data-ttu-id="c1ea5-166">En beskrivelse af feltet.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-166">A description of the tile.</span></span> |
   | <span data-ttu-id="c1ea5-167">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-167">Internet address</span></span> | <span data-ttu-id="c1ea5-168">Angiv URL-adressen på siden med medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-168">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="c1ea5-169">Feltstørrelse</span><span class="sxs-lookup"><span data-stu-id="c1ea5-169">Tile size</span></span> | <span data-ttu-id="c1ea5-170">Feltets størrelse: lille, mellem eller stor.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-170">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="c1ea5-171">Destination</span><span class="sxs-lookup"><span data-stu-id="c1ea5-171">Target</span></span> | <span data-ttu-id="c1ea5-172">Angiver, om siden skal åbnes i et nyt vindue eller i det aktuelle vindue.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-172">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="c1ea5-173">Feltbaggrundsbillede</span><span class="sxs-lookup"><span data-stu-id="c1ea5-173">Tile background image</span></span> | <span data-ttu-id="c1ea5-174">URL-adressen for det billede, der skal bruges til feltet (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="c1ea5-174">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="c1ea5-175">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="c1ea5-175">Start</span></span> | <span data-ttu-id="c1ea5-176">Startdato og -tidspunkt, hvor feltet vil blive tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-176">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="c1ea5-177">End</span><span class="sxs-lookup"><span data-stu-id="c1ea5-177">End</span></span> | <span data-ttu-id="c1ea5-178">Slutdato og -tidspunkt, hvor feltet vil være tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-178">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="c1ea5-179">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="c1ea5-179">Select **Save**.</span></span>
