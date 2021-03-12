---
title: Foretage fejlfinding af udgående lagerstedsoperationer
description: Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med udgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.
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
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2020-10-19
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 165ac8145ad75c2c6619764b9abe855b9d32eb46
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 01/15/2021
ms.locfileid: "4993972"
---
# <a name="troubleshoot-outbound-warehouse-operations"></a><span data-ttu-id="37ee7-103">Foretage fejlfinding af udgående lagerstedsoperationer</span><span class="sxs-lookup"><span data-stu-id="37ee7-103">Troubleshoot outbound warehouse operations</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="37ee7-104">Dette emne beskriver, hvordan du løser almindelige problemer, der kan opstå, når du arbejder med udgående lagerstedsoperationer i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="37ee7-104">This topic describes how to fix common issues that you might encounter while you work with outbound warehouse operations in Microsoft Dynamics 365 Supply Chain Management.</span></span>

## <a name="i-receive-the-following-error-message-sales-order-could-not-be-released"></a><span data-ttu-id="37ee7-105">Jeg får vist følgende fejlmeddelelse: "Salgsordren kunne ikke frigives".</span><span class="sxs-lookup"><span data-stu-id="37ee7-105">I receive the following error message: "Sales order could not be released."</span></span>

### <a name="issue-description"></a><span data-ttu-id="37ee7-106">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="37ee7-106">Issue description</span></span>

<span data-ttu-id="37ee7-107">Dette problem kan opstå af flere årsager.</span><span class="sxs-lookup"><span data-stu-id="37ee7-107">This issue can occur for several reasons.</span></span> <span data-ttu-id="37ee7-108">Ordren er f.eks. på kreditstyringshold, og der kan ikke oprettes forsendelser, før der angives en gyldig postadresse for alle salgslinjer, der er knyttet til en salgsordre.</span><span class="sxs-lookup"><span data-stu-id="37ee7-108">For example, the order is on credit management hold, and no shipments can be created until a valid postal address is entered for all sales lines that are associated with a sales order.</span></span> <span data-ttu-id="37ee7-109">Alternativt er der et ordrehold, der skal håndteres, før ordren kan frigives til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="37ee7-109">Alternatively, there is an order hold that must be addressed before the order can be released to the warehouse.</span></span> <span data-ttu-id="37ee7-110">Dette hold kan være ordrespecifikt, eller det kan være på kundekontoen.</span><span class="sxs-lookup"><span data-stu-id="37ee7-110">This hold might be order-specific, or it might be on the customer account.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="37ee7-111">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="37ee7-111">Issue resolution</span></span>

<span data-ttu-id="37ee7-112">Tilføj eller opdater adressen på salgsordren og ordrelinjerne, og frigiv derefter ordren til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="37ee7-112">Add or update the address on the sales order and order lines, and then release the order to the warehouse.</span></span> <span data-ttu-id="37ee7-113">Ordrer kan kun frigives til lagerstedet, hvis de har en gyldig leveringsadresse (pr. adresseformatopsætningen i modulet **Organisationsadministration**).</span><span class="sxs-lookup"><span data-stu-id="37ee7-113">Orders can be released to the warehouse only if they have a valid delivery address (per the address format setup in the **Organization administration** module).</span></span>

<span data-ttu-id="37ee7-114">Undersøg ordreholdet, og løs problemerne.</span><span class="sxs-lookup"><span data-stu-id="37ee7-114">Investigate the order hold, and address the issues.</span></span> <span data-ttu-id="37ee7-115">Fjern derefter holdet fra ordren eller kunden, og frigiv ordren til lagerstedet.</span><span class="sxs-lookup"><span data-stu-id="37ee7-115">Then remove the hold from the order or customer, and release the order to the warehouse.</span></span>

## <a name="i-receive-the-following-message-the-shipment-for-load-1-has-been-confirmed-however-no-lines-are-posted"></a><span data-ttu-id="37ee7-116">Jeg får vist følgende meddelelse: "Forsendelsen for lasten 1% er bekræftet".</span><span class="sxs-lookup"><span data-stu-id="37ee7-116">I receive the following message: "The shipment for load 1% has been confirmed."</span></span> <span data-ttu-id="37ee7-117">Der bogføres dog ingen linjer.</span><span class="sxs-lookup"><span data-stu-id="37ee7-117">However, no lines are posted.</span></span>

### <a name="issue-description"></a><span data-ttu-id="37ee7-118">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="37ee7-118">Issue description</span></span>

<span data-ttu-id="37ee7-119">En forsendelse på en last blev bekræftet, men der opstod ikke en efterfølgende bogføring.</span><span class="sxs-lookup"><span data-stu-id="37ee7-119">A shipment on a load was confirmed, but no further posting occurred.</span></span>

### <a name="issue-resolution"></a><span data-ttu-id="37ee7-120">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="37ee7-120">Issue resolution</span></span>

<span data-ttu-id="37ee7-121">Forsendelsesbekræftelse påvirker ikke bogføringen.</span><span class="sxs-lookup"><span data-stu-id="37ee7-121">Shipment confirmation doesn't affect posting.</span></span> <span data-ttu-id="37ee7-122">Den opdaterer blot status for afsendelse og last.</span><span class="sxs-lookup"><span data-stu-id="37ee7-122">It just updates the shipment and load status.</span></span> <span data-ttu-id="37ee7-123">Bogføring skal finde sted i en separat proces.</span><span class="sxs-lookup"><span data-stu-id="37ee7-123">Posting must occur in a separate process.</span></span>

## <a name="i-receive-the-following-error-message-direct-delivery-is-not-able-to-process-for-warehouse-1-as-it-has-warehouse-management-enabled-please-specify-another-warehouse-that-is-not-enabled-for-warehouse-management"></a><span data-ttu-id="37ee7-124">Jeg får vist følgende fejlmeddelelse: "Direkte levering kan ikke behandles for lagersted 1%, da lokationsstyring er aktiveret.</span><span class="sxs-lookup"><span data-stu-id="37ee7-124">I receive the following error message: "Direct delivery is not able to process for warehouse 1% as it has warehouse management enabled.</span></span> <span data-ttu-id="37ee7-125">Angiv et andet lagersted, der ikke er aktiveret til lokationsstyring."</span><span class="sxs-lookup"><span data-stu-id="37ee7-125">Please specify another warehouse that is not enabled for warehouse management."</span></span>

### <a name="issue-description"></a><span data-ttu-id="37ee7-126">Problembeskrivelse</span><span class="sxs-lookup"><span data-stu-id="37ee7-126">Issue description</span></span>

<span data-ttu-id="37ee7-127">En vare føjes til en salgslinje til direkte levering fra et lagersted, der er aktiveret til lokationsstyring (WMS).</span><span class="sxs-lookup"><span data-stu-id="37ee7-127">An item is added to a sales line for direct delivery from a warehouse that is enabled for warehouse management (WMS).</span></span> <span data-ttu-id="37ee7-128">Du får vist denne fejlmeddelelse, når salgslinjen opdateres.</span><span class="sxs-lookup"><span data-stu-id="37ee7-128">You receive this error message when the sales line is updated.</span></span> 

### <a name="issue-resolution"></a><span data-ttu-id="37ee7-129">Problemløsning</span><span class="sxs-lookup"><span data-stu-id="37ee7-129">Issue resolution</span></span>

<span data-ttu-id="37ee7-130">Microsoft har evalueret dette problem og har fastslået, at det er en funktionsbegrænsning.</span><span class="sxs-lookup"><span data-stu-id="37ee7-130">Microsoft has evaluated this issue and has determined that it's a feature limitation.</span></span> <span data-ttu-id="37ee7-131">I øjeblikket understøtter WMS ikke direkte levering.</span><span class="sxs-lookup"><span data-stu-id="37ee7-131">Currently, WMS doesn't support direct delivery.</span></span> <span data-ttu-id="37ee7-132">Hvis du derfor vil bruge direkte levering, skal du vælge en ikke-WMS-vare og et lagersted.</span><span class="sxs-lookup"><span data-stu-id="37ee7-132">Therefore, to use direct delivery, you must select a non-WMS item and warehouse.</span></span>
