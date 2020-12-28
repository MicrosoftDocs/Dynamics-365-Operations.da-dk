---
title: Foretage fejlfinding af lastopbygning og forsendelser
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lastopbygning og forsendelser i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
manager: tfehr
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 2933bcfd2cc526e39a4e1343cd472334a5b95607
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645326"
---
# <a name="troubleshoot-load-building-and-shipments"></a><span data-ttu-id="8f77c-103">Foretage fejlfinding af lastopbygning og forsendelser</span><span class="sxs-lookup"><span data-stu-id="8f77c-103">Troubleshoot load building and shipments</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="8f77c-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lastopbygning og forsendelser i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="8f77c-104">This topic describes how to fix common issues that you might encounter while you work with load building and shipments in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-you-cant-create-a-load-line-for-this-order-line-because-it-contains-inventory-dimensions-that-are-invalid"></a><span data-ttu-id="8f77c-105">Jeg får vist følgende fejlmeddelelse: "Du kan ikke oprette en lastlinje for denne ordrelinje, fordi den indeholder lagerdimensioner, der er ugyldige..."</span><span class="sxs-lookup"><span data-stu-id="8f77c-105">I receive the following error message: "You can't create a load line for this order line because it contains inventory dimensions that are invalid..."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8f77c-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8f77c-106">Issue description</span></span>

<span data-ttu-id="8f77c-107">Du får vist følgende fejlmeddelelse, når du forsøger at frigive en retursalgsordre til lagerstedet:</span><span class="sxs-lookup"><span data-stu-id="8f77c-107">You receive the following error message when you try to release a return sales order to the warehouse:</span></span>

> <span data-ttu-id="8f77c-108">Du kan ikke oprette en lastlinje for denne ordrelinje, fordi den indeholder lagerdimensioner, der er ugyldige.</span><span class="sxs-lookup"><span data-stu-id="8f77c-108">You can't create a load line for this order line because it contains inventory dimensions that are invalid.</span></span> <span data-ttu-id="8f77c-109">Du kan ikke referere til lagerdimensioner, der findes under lokationsdimensionen i reservationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="8f77c-109">You can't reference inventory dimensions that are located below the location dimension in the reservation hierarchy.</span></span> <span data-ttu-id="8f77c-110">Fjern de ugyldige dimensioner fra ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8f77c-110">Remove the invalid dimensions from the order line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8f77c-111">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8f77c-111">Issue resolution</span></span>

<span data-ttu-id="8f77c-112">Desværre understøtter produktet ikke lastbehandling af en salgsreturproces.</span><span class="sxs-lookup"><span data-stu-id="8f77c-112">Unfortunately, the product doesn't support load processing for a sales return process.</span></span> <span data-ttu-id="8f77c-113">Derfor kan du ikke frigive retursalgsordren til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="8f77c-113">Therefore, you can't release the return sales order to the warehouse.</span></span>

<span data-ttu-id="8f77c-114">På salgsordretransaktioner kan du ikke referere til lagerdimensioner, der findes under dimensionen **Lokation** i reservationshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="8f77c-114">On sales order transactions, you can't reference inventory dimensions that are located below the **Location** dimension in the reservation hierarchy.</span></span> <span data-ttu-id="8f77c-115">Løsningen er at fjerne de ugyldige dimensioner fra ordrelinjen.</span><span class="sxs-lookup"><span data-stu-id="8f77c-115">The resolution is to remove the invalid dimensions from the order line.</span></span>

## <a name="i-receive-the-following-error-message-one-of-the-lines-is-already-on-a-load-unable-to-release-to-warehouse"></a><span data-ttu-id="8f77c-116">Jeg får vist følgende fejlmeddelelse: "En af linjerne er allerede på en last.</span><span class="sxs-lookup"><span data-stu-id="8f77c-116">I receive the following error message: "One of the lines is already on a load.</span></span> <span data-ttu-id="8f77c-117">Kan ikke frigive til lagersted".</span><span class="sxs-lookup"><span data-stu-id="8f77c-117">Unable to release to warehouse."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8f77c-118">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8f77c-118">Issue description</span></span>

<span data-ttu-id="8f77c-119">Hvis du opretter laster manuelt, eller hvis du konfigurerer processen, så der allerede er oprettet laster før indtastning af salgsordrelinjer, forudsættes det, at den efterfølgende frigivelse udføres manuelt, og at ruten og vurderingen fra lasten vil blive anvendt.</span><span class="sxs-lookup"><span data-stu-id="8f77c-119">If you manually create loads, or if you set up the process so that loads are already created before sales order line entry occurs, the assumption is that the subsequent release will be done manually, and that the route and rating from the load will be used.</span></span>

<span data-ttu-id="8f77c-120">I et andet muligt scenario forsøger du at foretage automatisk frigivelse til lagerstedet, men bølgeprocessen kunne ikke oprette arbejde.</span><span class="sxs-lookup"><span data-stu-id="8f77c-120">In another possible scenario, you're trying to do an automatic release to the warehouse, but the wave process failed to create work.</span></span> <span data-ttu-id="8f77c-121">Derfor oprettes der stadig en åben forsendelse eller last.</span><span class="sxs-lookup"><span data-stu-id="8f77c-121">Therefore, an open shipment or load is still created.</span></span> <span data-ttu-id="8f77c-122">Denne åbne forsendelse eller last blokerer derefter efterfølgende forsøg på automatisk at frigive ordren, indtil du enten sletter den åbne forsendelse eller last eller manuelt genbehandler bølgen.</span><span class="sxs-lookup"><span data-stu-id="8f77c-122">This open shipment or load then blocks subsequent attempts to automatically release the order until you either delete the open shipment or load, or manually reprocess the wave.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8f77c-123">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8f77c-123">Issue resolution</span></span>

<span data-ttu-id="8f77c-124">Du kan frigive fra salgsordresiden, eller automatisk frigivelse kan udføres fra siden Frigiv salgsordre, hvis der ikke findes en last før frigivelsen til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="8f77c-124">You can release from the sales order page, or automatic release can be done from the release sales order page, only if no load exists before the release to the warehouse.</span></span> <span data-ttu-id="8f77c-125">Lasten oprettes automatisk, når bølgen er behandlet.</span><span class="sxs-lookup"><span data-stu-id="8f77c-125">The load will automatically be created after the wave is processed.</span></span>

## <a name="i-receive-the-following-error-message-the-delivery-note-correction-cant-be-processed-the-delivery-note-only-contains-items-that-are-subject-to-warehouse-management-processes-as-these-are-not-supported-by-delivery-note-correction"></a><span data-ttu-id="8f77c-126">Jeg får vist følgende fejlmeddelelse: "Ændringen af følgeseddel kan ikke behandles.</span><span class="sxs-lookup"><span data-stu-id="8f77c-126">I receive the following error message: "The delivery note correction can't be processed.</span></span> <span data-ttu-id="8f77c-127">Følgeseddel indeholder kun varer, der er underlagt lokationsstyringsprocesser, da disse ikke understøttes af korrektion af følgeseddel".</span><span class="sxs-lookup"><span data-stu-id="8f77c-127">The delivery note only contains items that are subject to warehouse management processes, as these are not supported by Delivery Note correction."</span></span>

### <a name="issue-description"></a><span data-ttu-id="8f77c-128">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8f77c-128">Issue description</span></span>

<span data-ttu-id="8f77c-129">Når du har bogført en følgeseddel, kan du ikke annullere den, fordi knappen **Annuller** ikke er tilgængelig.</span><span class="sxs-lookup"><span data-stu-id="8f77c-129">After you post a delivery note, you can't cancel it, because the **Cancel** button is unavailable.</span></span> <span data-ttu-id="8f77c-130">Du kan heller ikke rette følgesedlen.</span><span class="sxs-lookup"><span data-stu-id="8f77c-130">You also can't correct the delivery note.</span></span> <span data-ttu-id="8f77c-131">Hvis du forsøger, får du vist denne fejlmeddelelse.</span><span class="sxs-lookup"><span data-stu-id="8f77c-131">If you try, you receive this error message.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8f77c-132">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8f77c-132">Issue resolution</span></span>

<span data-ttu-id="8f77c-133">Hvis du vil rette bogførte følgesedler for varer, der er aktiveret for avanceret lokationsstyring (WMS), skal bogføringen ske fra lasten, ikke direkte fra ordren.</span><span class="sxs-lookup"><span data-stu-id="8f77c-133">To correct posted packing slips for items that are enabled for advanced warehouse management (WMS), you must do the posting from the load, not directly from the order.</span></span>

## <a name="how-can-i-create-work-from-outbound-loads-instead-of-waves"></a><span data-ttu-id="8f77c-134">Hvordan kan jeg oprette arbejde ud fra udgående laster i stedet for bølger?</span><span class="sxs-lookup"><span data-stu-id="8f77c-134">How can I create work from outbound loads instead of waves?</span></span>

### <a name="issue-description"></a><span data-ttu-id="8f77c-135">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8f77c-135">Issue description</span></span>

<span data-ttu-id="8f77c-136">Her er en måde at genskabe dette problem på.</span><span class="sxs-lookup"><span data-stu-id="8f77c-136">Here is one way to reproduce this issue.</span></span>

1. <span data-ttu-id="8f77c-137">Opret en udgående last ved hjælp af en salgsordre eller flytteordre.</span><span class="sxs-lookup"><span data-stu-id="8f77c-137">Create an outbound load by using a sales order or transfer order.</span></span>
2. <span data-ttu-id="8f77c-138">Frigiv lasten til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="8f77c-138">Release the load to the warehouse.</span></span>
3. <span data-ttu-id="8f77c-139">Bemærk, at der endnu ikke er genereret noget plukarbejde.</span><span class="sxs-lookup"><span data-stu-id="8f77c-139">Notice that no picking work has yet been generated.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8f77c-140">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8f77c-140">Issue resolution</span></span>

<span data-ttu-id="8f77c-141">Hvis arbejdet skal genereres med det samme, når lasten frigives, skal du konfigurere bølgeskabelonen i overensstemmelse hermed.</span><span class="sxs-lookup"><span data-stu-id="8f77c-141">If work must be generated immediately when the load is released, you must configure the wave template accordingly.</span></span> <span data-ttu-id="8f77c-142">Angiv følgende indstillinger til *Ja* på bølgeskabelonen:</span><span class="sxs-lookup"><span data-stu-id="8f77c-142">On the wave template, set the following options to *Yes*:</span></span>

- <span data-ttu-id="8f77c-143">Automatiser bølgeoprettelse</span><span class="sxs-lookup"><span data-stu-id="8f77c-143">Automate wave creation</span></span>
- <span data-ttu-id="8f77c-144">Udfør behandling af bølgen ved frigivelse til lagerstedet</span><span class="sxs-lookup"><span data-stu-id="8f77c-144">Process wave at release to warehouse</span></span>
- <span data-ttu-id="8f77c-145">Automatiser frigivelse af bølge</span><span class="sxs-lookup"><span data-stu-id="8f77c-145">Automate wave release</span></span>

## <a name="i-cant-re-release-a-partially-shipped-load"></a><span data-ttu-id="8f77c-146">Jeg kan ikke frigive en delvist leveret last igen.</span><span class="sxs-lookup"><span data-stu-id="8f77c-146">I can't re-release a partially shipped load.</span></span>

### <a name="issue-description"></a><span data-ttu-id="8f77c-147">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="8f77c-147">Issue description</span></span>

<span data-ttu-id="8f77c-148">Du kan ikke frigive en delvist leveret last til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="8f77c-148">You can't release a partially shipped load to the warehouse.</span></span> <span data-ttu-id="8f77c-149">Når du foretager frigivelsen til lagerstedet, vises meddelelsen "Handlingen er fuldført", men der sker ingenting, og der oprettes ikke noget arbejde for det resterende antal.</span><span class="sxs-lookup"><span data-stu-id="8f77c-149">When you do the release to the warehouse, an "Operation complete" message appears, but nothing happens, and no work is created for the remaining quantity.</span></span> <span data-ttu-id="8f77c-150">Dette problem opstår, når du bruger funktionaliteten til transport af last, og der er en ufuldstændig reservation.</span><span class="sxs-lookup"><span data-stu-id="8f77c-150">This issue occurs when you use transport load functionality and there is an incomplete reservation.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="8f77c-151">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="8f77c-151">Issue resolution</span></span>

<span data-ttu-id="8f77c-152">[KB-fejl 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Delvist leverede laster kan få ny bølge og genbehandles") er løst [version 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span><span class="sxs-lookup"><span data-stu-id="8f77c-152">[KB issue 470069](https://fix.lcs.dynamics.com/Issue/Details?kb=4574490&bugId=470069&dbType=3&qc=84ce1e09d7032d8b8ef86f5a0c68b86badf3dfaf29686c5ebbe97c53c0957b5f) ("Partially shipped loads can be re-waved and re-processed") is fixed in [release 10.0.15](../get-started/whats-new-scm-10-0-15.md).</span></span>
