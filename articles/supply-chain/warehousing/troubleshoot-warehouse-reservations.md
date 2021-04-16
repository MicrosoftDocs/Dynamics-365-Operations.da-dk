---
title: Foretage fejlfinding af reservationer i lokationsstyring
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsreservationer i Microsoft Dynamics 365 Supply Chain Management.
author: perlynne
ms.date: 10/19/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application user
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: d0d73396772ed9e8397797d6685fb550d911303b
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5828100"
---
# <a name="troubleshoot-reservations-in-warehouse-management"></a><span data-ttu-id="32dc5-103">Foretage fejlfinding af reservationer i lokationsstyring</span><span class="sxs-lookup"><span data-stu-id="32dc5-103">Troubleshoot reservations in warehouse management</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="32dc5-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med lagerstedsreservationer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="32dc5-104">This topic describes how to fix common issues that you might encounter while you work with warehouse reservations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="32dc5-105">Se [Fejlfinde batch- og seriereservationshierarkier for lagersteder](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md) for emner, der er relateret til batch- og serienummerregistreringer.</span><span class="sxs-lookup"><span data-stu-id="32dc5-105">For topics that are related to batch and serial number registrations, see [Troubleshoot warehouse batch and serial reservation hierarchies](troubleshoot-warehouse-batch-and-serial-reservation-hierarchies.md).</span></span>

## <a name="i-receive-the-following-error-message-reservations-cannot-be-removed-because-there-is-work-created-which-relies-on-the-reservations"></a><span data-ttu-id="32dc5-106">Jeg modtager fejlen "Reservationer kan ikke fjernes, fordi der er oprettet arbejde, der er afhængig af reservationerne".</span><span class="sxs-lookup"><span data-stu-id="32dc5-106">I receive the following error message: "Reservations cannot be removed because there is work created which relies on the reservations."</span></span>

### <a name="issue-description"></a><span data-ttu-id="32dc5-107">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="32dc5-107">Issue description</span></span>

<span data-ttu-id="32dc5-108">Du kan ikke annullere lagerreservation på en salgslinje, fordi der er åbent arbejde i forhold til linjen.</span><span class="sxs-lookup"><span data-stu-id="32dc5-108">You can't unreserve inventory on a sales line, because there is open work against the line.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="32dc5-109">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="32dc5-109">Issue resolution</span></span>

<span data-ttu-id="32dc5-110">Undersøg, om åbent pakkegruppearbejde findes for at bringe varen fra en pakkestation til et andet sted (f.eks. *Lagerport*).</span><span class="sxs-lookup"><span data-stu-id="32dc5-110">Investigate whether open packing group work exists to bring the item from a packing station to another location (such as *Baydoor*).</span></span> <span data-ttu-id="32dc5-111">Gennemse posterne på siden **Historik for oprettelse af arbejde** og **Arbejdsdetaljer** for at bestemme, hvad der fysisk reserverer lageret, og fuldfør eller slet derefter arbejdet for at frigøre reservationen.</span><span class="sxs-lookup"><span data-stu-id="32dc5-111">Review the records on the **Work creation history log** and **Work details** pages to determine what is physically reserving the inventory, and then complete or delete the work to free up the reservation.</span></span>

## <a name="i-receive-the-following-error-message-inventory-quantity--1-could-not-be-updated-due-to-insufficient-inventory-transactions-for-item-2"></a><span data-ttu-id="32dc5-112">Jeg modtager følgende fejlmeddelelse: "Lagerantal -%1 kunne ikke opdateres på grund af utilstrækkelige lagertransaktioner for varen %2...."</span><span class="sxs-lookup"><span data-stu-id="32dc5-112">I receive the following error message: "Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2...."</span></span>

### <a name="issue-description"></a><span data-ttu-id="32dc5-113">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="32dc5-113">Issue description</span></span>

<span data-ttu-id="32dc5-114">Dette problem kan opstå, hvis systemet ikke kan opdatere et lagerantal, fordi der ikke er lagertransaktioner nok med de angivne dimensioner.</span><span class="sxs-lookup"><span data-stu-id="32dc5-114">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="32dc5-115">Her er hele teksten i den fulde fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="32dc5-115">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="32dc5-116">Lagerantal -%1 kunne ikke opdateres på grund af utilstrækkelige lagertransaktioner for varen %2 med dimensionsstørrelse=%3, farve=%4, tillæg=%5, sted=%6, lagersted=%7, lokation=%8, lagerstatus=tilgængelig, nummerplade=%9, batchnummer=%10 for reference-id %11 på parti-id %12.</span><span class="sxs-lookup"><span data-stu-id="32dc5-116">Inventory quantity -%1 could not be updated due to insufficient inventory transactions for item %2 with dimensions Size=%3, Color=%4, Additions=%5, Site=%6, Warehouse=%7, Location=%8, Inventory status=Available, License plate=%9, Batch number=%10 for reference ID %11 on Lot ID %12.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="32dc5-117">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="32dc5-117">Issue resolution</span></span>

<span data-ttu-id="32dc5-118">Sørg for, at der ikke er lagertransaktioner, som fysisk reserverer antallet.</span><span class="sxs-lookup"><span data-stu-id="32dc5-118">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="32dc5-119">Disse transaktioner kan f.eks. have åbne kvalitetsordrer, lagerblokeringsposter eller udlagringsordrer.</span><span class="sxs-lookup"><span data-stu-id="32dc5-119">For example, these transactions might open quality orders, inventory blocking records, or output orders.</span></span>

## <a name="i-receive-the-following-error-message-physical-on-handcannot-be-reserved-because-only-000-are-available-in-the-inventory"></a><span data-ttu-id="32dc5-120">Jeg får vist følgende fejlmeddelelse: "Fysisk beholdning...kan ikke reserveres, da der kun er 0,00 tilgængelige på lageret".</span><span class="sxs-lookup"><span data-stu-id="32dc5-120">I receive the following error message: "Physical on-hand...cannot be reserved because only 0.00 are available in the inventory."</span></span>

### <a name="issue-description"></a><span data-ttu-id="32dc5-121">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="32dc5-121">Issue description</span></span>

<span data-ttu-id="32dc5-122">Dette problem kan opstå, hvis systemet ikke kan opdatere et lagerantal, fordi der ikke er lagertransaktioner nok med de angivne dimensioner.</span><span class="sxs-lookup"><span data-stu-id="32dc5-122">This issue can occur if the system can't update an inventory quantity because there aren't enough inventory transactions that have the specified dimensions.</span></span> <span data-ttu-id="32dc5-123">Her er hele teksten i den fulde fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="32dc5-123">Here is the full text of the full error message:</span></span>

> <span data-ttu-id="32dc5-124">Fysisk disponibel sted=%1, lagersted=%2, lagerstatus=tilgængelig, batchnummer=%3, ejer=%4: %5 kan ikke reserveres, da der kun er 0,00 tilgængelige på lageret.</span><span class="sxs-lookup"><span data-stu-id="32dc5-124">Physical on-hand Site=%1, Warehouse=%2, Inventory status=Available, Batch number=%3, Owner=%4: %5 cannot be reserved because only 0.00 are available in the inventory.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="32dc5-125">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="32dc5-125">Issue resolution</span></span>

<span data-ttu-id="32dc5-126">Dette problem skyldes sandsynligvis åbent arbejde.</span><span class="sxs-lookup"><span data-stu-id="32dc5-126">This issue is probably caused by open work.</span></span> <span data-ttu-id="32dc5-127">Du skal enten fuldføre arbejdet eller modtage uden arbejdsoprettelse.</span><span class="sxs-lookup"><span data-stu-id="32dc5-127">Either complete the work or receive without work creation.</span></span> <span data-ttu-id="32dc5-128">Sørg for, at der ikke er lagertransaktioner, som fysisk reserverer antallet.</span><span class="sxs-lookup"><span data-stu-id="32dc5-128">Make sure that no inventory transactions are physically reserving the quantity.</span></span> <span data-ttu-id="32dc5-129">Disse transaktioner kan f.eks. være åbne kvalitetsordrer, lagerblokeringsposter eller udlagringsordrer.</span><span class="sxs-lookup"><span data-stu-id="32dc5-129">For example, these transactions might be open quality orders, inventory blocking records, or output orders.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
