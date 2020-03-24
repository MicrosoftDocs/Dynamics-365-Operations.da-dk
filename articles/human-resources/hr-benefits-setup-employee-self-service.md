---
title: Konfigurere medarbejderselvbetjening
description: I Microsoft Dynamics 365 Human Resources kan du konfigurere felter til navigation på øverste niveau i medarbejderselvbetjening.
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
ms.openlocfilehash: 17918fc7b894929c92c54b59b7440ab8aef980bd
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092654"
---
# <a name="configure-employee-self-service"></a><span data-ttu-id="647be-103">Konfigurere medarbejderselvbetjening</span><span class="sxs-lookup"><span data-stu-id="647be-103">Configure employee self service</span></span>

[!include [banner](includes/preview-feature.md)]

<span data-ttu-id="647be-104">I Microsoft Dynamics 365 Human Resources kan du konfigurere felter til navigation på øverste niveau i medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="647be-104">In Microsoft Dynamics 365 Human Resources, you can configure tiles for top-level navigation in Employee self service.</span></span> <span data-ttu-id="647be-105">Frynsegodeplansfelter sender brugere videre til frynsegodeplaner som de er berettiget til at tilmelde sig.</span><span class="sxs-lookup"><span data-stu-id="647be-105">Benefit plan tiles direct users to benefit plans that they are eligible to enroll in.</span></span>

## <a name="set-up-a-role-center-tile"></a><span data-ttu-id="647be-106">Oprette et felt i et rollebaseret område</span><span class="sxs-lookup"><span data-stu-id="647be-106">Set up a role center tile</span></span>

1. <span data-ttu-id="647be-107">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="647be-107">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="647be-108">Vælg fanen **Opsætning af rollebaseret område**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="647be-108">Select the **Role center tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="647be-109">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="647be-109">Specify values for the following fields:</span></span>

   | <span data-ttu-id="647be-110">Felt</span><span class="sxs-lookup"><span data-stu-id="647be-110">Field</span></span> | <span data-ttu-id="647be-111">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="647be-111">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="647be-112">Felt-id</span><span class="sxs-lookup"><span data-stu-id="647be-112">Tile ID</span></span> | <span data-ttu-id="647be-113">Entydigt id for feltet.</span><span class="sxs-lookup"><span data-stu-id="647be-113">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="647be-114">Feltlabeltekst</span><span class="sxs-lookup"><span data-stu-id="647be-114">Tile label text</span></span> | <span data-ttu-id="647be-115">Den tekst, der vises for feltet på selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="647be-115">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="647be-116">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="647be-116">Description</span></span> | <span data-ttu-id="647be-117">En beskrivelse af feltet.</span><span class="sxs-lookup"><span data-stu-id="647be-117">A description of the tile.</span></span> |
   | <span data-ttu-id="647be-118">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="647be-118">Internet address</span></span> | <span data-ttu-id="647be-119">Angiv URL-adressen på siden med medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="647be-119">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="647be-120">Feltstørrelse</span><span class="sxs-lookup"><span data-stu-id="647be-120">Tile size</span></span> | <span data-ttu-id="647be-121">Feltets størrelse: lille, mellem eller stor.</span><span class="sxs-lookup"><span data-stu-id="647be-121">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="647be-122">Destination</span><span class="sxs-lookup"><span data-stu-id="647be-122">Target</span></span> | <span data-ttu-id="647be-123">Angiver, om siden skal åbnes i et nyt vindue eller i det aktuelle vindue.</span><span class="sxs-lookup"><span data-stu-id="647be-123">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="647be-124">Feltbaggrundsbillede</span><span class="sxs-lookup"><span data-stu-id="647be-124">Tile background image</span></span> | <span data-ttu-id="647be-125">URL-adressen for det billede, der skal bruges til feltet (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="647be-125">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="647be-126">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="647be-126">Start</span></span> | <span data-ttu-id="647be-127">Startdato og -tidspunkt, hvor feltet vil blive tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="647be-127">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="647be-128">End</span><span class="sxs-lookup"><span data-stu-id="647be-128">End</span></span> | <span data-ttu-id="647be-129">Slutdato og -tidspunkt, hvor feltet vil være tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="647be-129">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="647be-130">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="647be-130">Select **Save**.</span></span>

## <a name="set-up-a-benefit-plans-tile"></a><span data-ttu-id="647be-131">Konfigurere et felt til frynsegodeplaner</span><span class="sxs-lookup"><span data-stu-id="647be-131">Set up a benefit plans tile</span></span>

1. <span data-ttu-id="647be-132">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="647be-132">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="647be-133">Vælg fanen **Konfigurer felt til frynsegodeplaner**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="647be-133">Select the **Benefit plans tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="647be-134">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="647be-134">Specify values for the following fields:</span></span>

   | <span data-ttu-id="647be-135">Felt</span><span class="sxs-lookup"><span data-stu-id="647be-135">Field</span></span> | <span data-ttu-id="647be-136">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="647be-136">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="647be-137">Felt-id</span><span class="sxs-lookup"><span data-stu-id="647be-137">Tile ID</span></span> | <span data-ttu-id="647be-138">Entydigt id for feltet.</span><span class="sxs-lookup"><span data-stu-id="647be-138">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="647be-139">Feltlabeltekst</span><span class="sxs-lookup"><span data-stu-id="647be-139">Tile label text</span></span> | <span data-ttu-id="647be-140">Den tekst, der vises for feltet på selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="647be-140">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="647be-141">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="647be-141">Description</span></span> | <span data-ttu-id="647be-142">En beskrivelse af feltet.</span><span class="sxs-lookup"><span data-stu-id="647be-142">A description of the tile.</span></span> |
   | <span data-ttu-id="647be-143">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="647be-143">Internet address</span></span> | <span data-ttu-id="647be-144">Angiv URL-adressen på siden med medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="647be-144">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="647be-145">Feltstørrelse</span><span class="sxs-lookup"><span data-stu-id="647be-145">Tile size</span></span> | <span data-ttu-id="647be-146">Feltets størrelse: lille, mellem eller stor.</span><span class="sxs-lookup"><span data-stu-id="647be-146">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="647be-147">Destination</span><span class="sxs-lookup"><span data-stu-id="647be-147">Target</span></span> | <span data-ttu-id="647be-148">Angiver, om siden skal åbnes i et nyt vindue eller i det aktuelle vindue.</span><span class="sxs-lookup"><span data-stu-id="647be-148">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="647be-149">Feltbaggrundsbillede</span><span class="sxs-lookup"><span data-stu-id="647be-149">Tile background image</span></span> | <span data-ttu-id="647be-150">URL-adressen for det billede, der skal bruges til feltet (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="647be-150">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="647be-151">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="647be-151">Start</span></span> | <span data-ttu-id="647be-152">Startdato og -tidspunkt, hvor feltet vil blive tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="647be-152">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="647be-153">End</span><span class="sxs-lookup"><span data-stu-id="647be-153">End</span></span> | <span data-ttu-id="647be-154">Slutdato og -tidspunkt, hvor feltet vil være tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="647be-154">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="647be-155">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="647be-155">Select **Save**.</span></span>

## <a name="set-up-a-flex-credit-plan-tile"></a><span data-ttu-id="647be-156">Konfigurere et felt for flekskreditplan</span><span class="sxs-lookup"><span data-stu-id="647be-156">Set up a flex credit plan tile</span></span>

1. <span data-ttu-id="647be-157">I arbejdsområdet **Frynsegodeadministration** skal du vælge **Parametre for medarbejdsselvbetjening** under **Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="647be-157">In the **Benefits management** workspace, under **Setup**, select **Employee self service parameters**.</span></span>

2. <span data-ttu-id="647be-158">Vælg fanen **Konfigurer felt til flekskreditplan**, og vælg derefter **Ny**.</span><span class="sxs-lookup"><span data-stu-id="647be-158">Select the **Flex credit plan tile setup** tab, and then select **New**.</span></span>

3. <span data-ttu-id="647be-159">Angiv værdier for følgende felter:</span><span class="sxs-lookup"><span data-stu-id="647be-159">Specify values for the following fields:</span></span>

   | <span data-ttu-id="647be-160">Felt</span><span class="sxs-lookup"><span data-stu-id="647be-160">Field</span></span> | <span data-ttu-id="647be-161">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="647be-161">Description</span></span> |
   | --- | --- |
   | <span data-ttu-id="647be-162">Felt-id</span><span class="sxs-lookup"><span data-stu-id="647be-162">Tile ID</span></span> | <span data-ttu-id="647be-163">Entydigt id for feltet.</span><span class="sxs-lookup"><span data-stu-id="647be-163">The unique identifier for the tile.</span></span> |
   | <span data-ttu-id="647be-164">Feltlabeltekst</span><span class="sxs-lookup"><span data-stu-id="647be-164">Tile label text</span></span> | <span data-ttu-id="647be-165">Den tekst, der vises for feltet på selvbetjening.</span><span class="sxs-lookup"><span data-stu-id="647be-165">The text that will appear for the tile on Self-service.</span></span> |
   | <span data-ttu-id="647be-166">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="647be-166">Description</span></span> | <span data-ttu-id="647be-167">En beskrivelse af feltet.</span><span class="sxs-lookup"><span data-stu-id="647be-167">A description of the tile.</span></span> |
   | <span data-ttu-id="647be-168">Internetadresse</span><span class="sxs-lookup"><span data-stu-id="647be-168">Internet address</span></span> | <span data-ttu-id="647be-169">Angiv URL-adressen på siden med medarbejderselvbetjening.</span><span class="sxs-lookup"><span data-stu-id="647be-169">Enter the URL to the employee self service page.</span></span> |
   | <span data-ttu-id="647be-170">Feltstørrelse</span><span class="sxs-lookup"><span data-stu-id="647be-170">Tile size</span></span> | <span data-ttu-id="647be-171">Feltets størrelse: lille, mellem eller stor.</span><span class="sxs-lookup"><span data-stu-id="647be-171">The size of the tile: Small, Medium, or Large.</span></span> |
   | <span data-ttu-id="647be-172">Destination</span><span class="sxs-lookup"><span data-stu-id="647be-172">Target</span></span> | <span data-ttu-id="647be-173">Angiver, om siden skal åbnes i et nyt vindue eller i det aktuelle vindue.</span><span class="sxs-lookup"><span data-stu-id="647be-173">Specifies whether the page should open in a new window or the current window.</span></span> |
   | <span data-ttu-id="647be-174">Feltbaggrundsbillede</span><span class="sxs-lookup"><span data-stu-id="647be-174">Tile background image</span></span> | <span data-ttu-id="647be-175">URL-adressen for det billede, der skal bruges til feltet (valgfrit).</span><span class="sxs-lookup"><span data-stu-id="647be-175">The URL of the image to use for the tile (optional).</span></span> |
   | <span data-ttu-id="647be-176">Igangsætning</span><span class="sxs-lookup"><span data-stu-id="647be-176">Start</span></span> | <span data-ttu-id="647be-177">Startdato og -tidspunkt, hvor feltet vil blive tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="647be-177">The beginning date and time the tile should be available.</span></span> |
   | <span data-ttu-id="647be-178">End</span><span class="sxs-lookup"><span data-stu-id="647be-178">End</span></span> | <span data-ttu-id="647be-179">Slutdato og -tidspunkt, hvor feltet vil være tilgængeligt.</span><span class="sxs-lookup"><span data-stu-id="647be-179">The end date and time the tile should be available.</span></span> |

4. <span data-ttu-id="647be-180">Vælg **Gem**.</span><span class="sxs-lookup"><span data-stu-id="647be-180">Select **Save**.</span></span>
