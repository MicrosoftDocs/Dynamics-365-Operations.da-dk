---
title: Foretage fejlfinding af reservationer i lokationsstyring
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsreservationer i Microsoft Dynamics 365 Supply Chain Management.
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
ms.openlocfilehash: 6151797001b1ccdb7e371c70b90c304a5ab422d8
ms.sourcegitcommit: deb711c92251ed48cdf20ea514d03461c26a2262
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 11/25/2020
ms.locfileid: "4645113"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="1f7bf-103">Foretage fejlfinding af reservationer i lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="1f7bf-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="1f7bf-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsreservationer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="1f7bf-105">Jeg modtager fejlen "Reservationer kan ikke fjernes, fordi der er oprettet arbejde, der er afhængig af reservationerne".</span><span class="sxs-lookup"><span data-stu-id="1f7bf-105">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1f7bf-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1f7bf-106">Issue description</span></span>

<span data-ttu-id="1f7bf-107">Du kan ikke annullere lagerreservation på en salgslinje, fordi der er åbent arbejde i forhold til linjen.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-107">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1f7bf-108">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1f7bf-108">Issue resolution</span></span>

<span data-ttu-id="1f7bf-109">Undersøg, om åbent pakkegruppearbejde findes for at bringe varen fra en pakkestation til et andet sted (f.eks. *Lagerport*).</span><span class="sxs-lookup"><span data-stu-id="1f7bf-109">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="1f7bf-110">Gennemse posterne på siden **Historik for oprettelse af arbejde** og **Arbejdsdetaljer** for at bestemme, hvad der fysisk reserverer lageret, og fuldfør eller slet derefter arbejdet for at frigøre reservationen.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-110">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="1f7bf-111">Jeg modtager følgende fejlmeddelelse: "Lagerantal -%1 kunne ikke opdateres på grund af utilstrækkelige lagertransaktioner for varen %2...."</span><span class="sxs-lookup"><span data-stu-id="1f7bf-111">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1f7bf-112">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1f7bf-112">Issue description</span></span>

<span data-ttu-id="1f7bf-113">Dette problem kan opstå, hvis systemet ikke kan opdatere et lagerantal, fordi der ikke er lagertransaktioner nok med de angivne dimensioner.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-113">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="1f7bf-114">Her er hele teksten i den fulde fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="1f7bf-114">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="1f7bf-115">Lagerantal -%1 kunne ikke opdateres på grund af utilstrækkelige lagertransaktioner for varen %2 med dimensionsstørrelse=%3, farve=%4, tillæg=%5, sted=%6, lagersted=%7, lokation=%8, lagerstatus=tilgængelig, nummerplade=%9, batchnummer=%10 for reference-id %11 på parti-id %12.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-115">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1f7bf-116">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1f7bf-116">Issue resolution</span></span>

<span data-ttu-id="1f7bf-117">Sørg for, at der ikke er lagertransaktioner, som fysisk reserverer antallet.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-117">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="1f7bf-118">Disse transaktioner kan f.eks. have åbne kvalitetsordrer, lagerblokeringsposter eller udlagringsordrer.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-118">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="1f7bf-119">Jeg får vist følgende fejlmeddelelse: "Fysisk beholdning...kan ikke reserveres, da der kun er 0,00 tilgængelige på lageret".</span><span class="sxs-lookup"><span data-stu-id="1f7bf-119">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1f7bf-120">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1f7bf-120">Issue description</span></span>

<span data-ttu-id="1f7bf-121">Dette problem kan opstå, hvis systemet ikke kan opdatere et lagerantal, fordi der ikke er lagertransaktioner nok med de angivne dimensioner.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-121">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="1f7bf-122">Her er hele teksten i den fulde fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="1f7bf-122">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="1f7bf-123">Fysisk disponibel sted=%1, lagersted=%2, lagerstatus=tilgængelig, batchnummer=%3, ejer=%4: %5 kan ikke reserveres, da der kun er 0,00 tilgængelige på lageret.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-123">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1f7bf-124">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1f7bf-124">Issue resolution</span></span>

<span data-ttu-id="1f7bf-125">Dette problem skyldes sandsynligvis åbent arbejde.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-125">This issue is probably caused by open work.</span></span> <span data-ttu-id="1f7bf-126">Du skal enten fuldføre arbejdet eller modtage uden arbejdsoprettelse.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-126">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="1f7bf-127">Sørg for, at der ikke er lagertransaktioner, som fysisk reserverer antallet.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-127">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="1f7bf-128">Disse transaktioner kan f.eks. være åbne kvalitetsordrer, lagerblokeringsposter eller udlagringsordrer.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-128">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-to-be-assigned-to-wave-load-lines-must-specify-the-dimensions-above-the-location-to-assign-these-dimensions-reserve-and-recreate-the-load-line"></a><span data-ttu-id="1f7bf-129">Jeg får vist følgende fejlmeddelelse: "For at blive tildelt en bølge skal lastlinjer angive dimensionerne over lokationen.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-129">I receive the following error message: "To be assigned to wave, load lines must specify the dimensions above the location.</span></span> <span data-ttu-id="1f7bf-130">Du kan tildele disse dimensioner ved at reservere og genoprette lastlinjen".</span><span class="sxs-lookup"><span data-stu-id="1f7bf-130">To assign these dimensions, reserve and recreate the load line."</span></span>

### <a name="issue-description"></a><span data-ttu-id="1f7bf-131">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="1f7bf-131">Issue description</span></span>

<span data-ttu-id="1f7bf-132">Når du bruger en vare, der har et "batch over"-reservationshierarki (hvor **batchnummer**-dimensionen er placeret *oven over* **Lokation**-dimensionen), vil kommandoen **Frigiv til lagersted** på siden **Panelet Lastplanlægning** for en delmængde ikke fungere.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-132">When you use an item that has a "batch above" reservation hierarchy (with the **Batch number** dimension placed *above* the **Location** dimension), the **Release to warehouse** command on the **Load planning workbench** page for a partial quantity doesn't work.</span></span> <span data-ttu-id="1f7bf-133">Du får vist denne fejlmeddelelse, og der oprettes ikke noget arbejde for delmængden.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-133">You receive this error message, and no work is created for the partial quantity.</span></span>

<span data-ttu-id="1f7bf-134">Men, hvis du bruger en vare, der har et "batch under"-reservationshierarki (hvor **batchnummer**-dimensionen er placeret *under* **Lokation**-dimensionen), kan du frigive en last fra siden **Panelet Lastplanlægning** for en delmængde.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-134">However, if you use an item that has a "batch below" reservation hierarchy (with the **Batch number** dimension placed *below* the **Location** dimension), you can release a load from the **Load planning workbench** page for a partial quantity.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="1f7bf-135">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="1f7bf-135">Issue resolution</span></span>

<span data-ttu-id="1f7bf-136">Denne funktionsmåde er tilsigtet.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-136">This behavior is by design.</span></span> <span data-ttu-id="1f7bf-137">Hvis du placerer en dimension over **Lokation**-dimensionen i reservationshierarkiet, skal den angives før frigivelsen til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-137">If you put a dimension above the **Location** dimension in the reservation hierarchy, it must be specified before the release to the warehouse.</span></span> <span data-ttu-id="1f7bf-138">Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning under frigivelsen til lagerstedet fra lastplanlægningspanelet.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-138">Microsoft has evaluated this issue and has determined that it's a feature limitation during releases to the warehouse from the load planning workbench.</span></span> <span data-ttu-id="1f7bf-139">Delmængder kan ikke frigives, hvis en eller flere dimensioner over **Lokation** ikke er angivet.</span><span class="sxs-lookup"><span data-stu-id="1f7bf-139">Partial quantities can't be released if one or more dimensions above **Location** aren't specified.</span></span>

<span data-ttu-id="1f7bf-140">Du kan finde flere oplysninger under [Fleksibel reservationspolitik for dimension på lagerstedsniveau](flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="1f7bf-140">For more information, see [Flexible warehouse-level dimension reservation policy](flexible-warehouse-level-dimension-reservation.md).</span></span>
