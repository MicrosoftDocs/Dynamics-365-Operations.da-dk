---
title: Fysiske og økonomiske opdateringer
description: Dette emne indeholder en oversigt over, hvilke typer transaktioner der opskriver eller reducerer lagerantal.
author: AndersGirke
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventTrans, InventTransVoucher
audience: Application User
ms.reviewer: kamaybac
ms.custom: 75023
ms.assetid: 128340e1-c573-48e6-b835-6c350d8dd0fb
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: mguada
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 88432b9a5e564f9e81892e0bb379f95ff40d6c9d
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5842147"
---
# <a name="physical-and-financial-updates"></a><span data-ttu-id="f8048-103">Fysiske og økonomiske opdateringer</span><span class="sxs-lookup"><span data-stu-id="f8048-103">Physical and financial updates</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="f8048-104">Dette emne indeholder en oversigt over, hvilke typer transaktioner der opskriver eller reducerer lagerantal.</span><span class="sxs-lookup"><span data-stu-id="f8048-104">This topic provides an overview of which types of transactions increase or decrease inventory quantities.</span></span> 

<span data-ttu-id="f8048-105">Lagertransaktioner kan opdateres fysisk og økonomisk i Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="f8048-105">Inventory transactions can be physically updated and financially updated in Dynamics 365 Supply Chain Management.</span></span> <span data-ttu-id="f8048-106">Nogle typer fysiske og økonomiske posteringer øger lagermængderne, mens andre reducerer mængden.</span><span class="sxs-lookup"><span data-stu-id="f8048-106">Some types of physical and financial transactions increase inventory quantities, whereas others decrease the quantity.</span></span>

## <a name="physical-increases"></a><span data-ttu-id="f8048-107">Fysiske opskrivninger</span><span class="sxs-lookup"><span data-stu-id="f8048-107">Physical increases</span></span>
<span data-ttu-id="f8048-108">Når der bogføres en fysisk postering, ændres statussen for transaktionsposten til **Modtaget**.</span><span class="sxs-lookup"><span data-stu-id="f8048-108">When a physical transaction is posted, the status of the transaction record is **Received**.</span></span> <span data-ttu-id="f8048-109">Følgende transaktioner betragtes som fysiske opskrivninger:</span><span class="sxs-lookup"><span data-stu-id="f8048-109">The following transactions are considered physical increases:</span></span>

-   <span data-ttu-id="f8048-110">Indkøbsordretilgang</span><span class="sxs-lookup"><span data-stu-id="f8048-110">Purchase order receipt</span></span>
-   <span data-ttu-id="f8048-111">Salgsordrefølgeseddelretur</span><span class="sxs-lookup"><span data-stu-id="f8048-111">Sales order packing slip return</span></span>
-   <span data-ttu-id="f8048-112">Færdigmelde en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="f8048-112">Reporting a production order as finished</span></span>
-   <span data-ttu-id="f8048-113">Biprodukt på en produktionsordreplukliste</span><span class="sxs-lookup"><span data-stu-id="f8048-113">By-product on a production order picking list</span></span>

## <a name="financial-increases"></a><span data-ttu-id="f8048-114">Økonomiske opskrivninger</span><span class="sxs-lookup"><span data-stu-id="f8048-114">Financial increases</span></span>
<span data-ttu-id="f8048-115">Når en økonomisk tilgangspostering er bogført, er statussen for den transaktionspost, der opskriver mængden, **Købt**.</span><span class="sxs-lookup"><span data-stu-id="f8048-115">When a financial receipt transaction is posted, the status of the transaction record that increases the quantity is **Purchased**.</span></span> <span data-ttu-id="f8048-116">Følgende transaktioner betragtes som økonomiske opskrivninger:</span><span class="sxs-lookup"><span data-stu-id="f8048-116">The following transactions are considered financial increases:</span></span>

-   <span data-ttu-id="f8048-117">Kreditorfaktura</span><span class="sxs-lookup"><span data-stu-id="f8048-117">Vendor invoice</span></span>
-   <span data-ttu-id="f8048-118">Salgsordrefaktura for en returnering</span><span class="sxs-lookup"><span data-stu-id="f8048-118">Sales order invoice for a return</span></span>
-   <span data-ttu-id="f8048-119">Efterkalkulation af produktionsordre</span><span class="sxs-lookup"><span data-stu-id="f8048-119">Production order costing</span></span>
-   <span data-ttu-id="f8048-120">Lagerkladder med positiv mængde, f.eks. bevægelse, driftsregnskab, optælling, styklister og overførsel</span><span class="sxs-lookup"><span data-stu-id="f8048-120">Positive quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

## <a name="transactions-that-increase-quantity"></a><span data-ttu-id="f8048-121">Transaktioner, der opskriver antallet</span><span class="sxs-lookup"><span data-stu-id="f8048-121">Transactions that increase quantity</span></span>
<span data-ttu-id="f8048-122">Posteringer, der øger mængden, bogføres til den løbende gennemsnitskostpris.</span><span class="sxs-lookup"><span data-stu-id="f8048-122">Transactions that increase quantity are posted at the running average cost price.</span></span> <span data-ttu-id="f8048-123">Den beregnede løbende gennemsnitskostpris er baseret på kostprisen for hver af disse transaktioner for hver lagerdimension, der spores økonomisk.</span><span class="sxs-lookup"><span data-stu-id="f8048-123">The calculated running average cost price is based on the cost of each of these transactions for each inventory dimension that is being tracked financially.</span></span> <span data-ttu-id="f8048-124">Få mere at vide om kørsel af gennemsnitlige kostpriser på [Løbende gennemsnitskostpris](running-average-cost-price.md).</span><span class="sxs-lookup"><span data-stu-id="f8048-124">For information about running average cost prices, see [Running average cost price](running-average-cost-price.md).</span></span>

## <a name="transactions-that-decrease-quantity"></a><span data-ttu-id="f8048-125">Transaktioner, der reducerer antallet</span><span class="sxs-lookup"><span data-stu-id="f8048-125">Transactions that decrease quantity</span></span>
<span data-ttu-id="f8048-126">Den beregnede løbende gennemsnitskostpris bruges, når en transaktion, der reducerer mængden, bogføres, uanset hvilken lagermodel der knyttes til dette lager.</span><span class="sxs-lookup"><span data-stu-id="f8048-126">The calculated running average cost price is used  when a transaction that decreases quantity is posted, regardless of the inventory model that is associated with that inventory.</span></span> <span data-ttu-id="f8048-127">Posteringen, der reducerer mængden, må ikke tidligere have været afmærket til en anden posteringer, før den blev bogført.</span><span class="sxs-lookup"><span data-stu-id="f8048-127">The transaction that decreases quantity must not have been marked to another transaction before it was posted.</span></span> <span data-ttu-id="f8048-128">Hvis den fysisk disponible lagerbeholdning bliver negativ, bruges de lageromkostninger, der er defineret for varen på siden **Vare**.</span><span class="sxs-lookup"><span data-stu-id="f8048-128">If the physical on-hand inventory becomes negative, the inventory cost that is defined for the item on the **Item** page is used.</span></span> 

> [!NOTE]
> <span data-ttu-id="f8048-129">Hvis funktionen til brug af flere lokationer er aktiveret, vil denne lageromkostning i stedet blive defineret for en lokation på siden **Standardindstillinger for ordre**.</span><span class="sxs-lookup"><span data-stu-id="f8048-129">If multisite functionality is enabled, this cost will instead be the inventory cost that is defined for a site on the **Default order settings** page.</span></span>

## <a name="physical-issues-vs-financial-issues"></a><span data-ttu-id="f8048-130">Fysiske afgange vs. økonomiske afgange</span><span class="sxs-lookup"><span data-stu-id="f8048-130">Physical issues vs. financial issues</span></span>
<span data-ttu-id="f8048-131">Når der bogføres en fysisk afgangspostering, ændres statussen for transaktionsposten til **Trukket**.</span><span class="sxs-lookup"><span data-stu-id="f8048-131">When a physical issue transaction is posted, the status of the transaction record is **Deducted**.</span></span> <span data-ttu-id="f8048-132">Følgende transaktioner betragtes som fysiske afgange:</span><span class="sxs-lookup"><span data-stu-id="f8048-132">The following transactions are considered physical issues:</span></span>

-   <span data-ttu-id="f8048-133">Produktionsordrepluklistekladde</span><span class="sxs-lookup"><span data-stu-id="f8048-133">Production order picking list journal</span></span>
-   <span data-ttu-id="f8048-134">Salgsordrefølgeseddel</span><span class="sxs-lookup"><span data-stu-id="f8048-134">Sales order packing slip</span></span>
-   <span data-ttu-id="f8048-135">Indkøbsordrefølgeseddelreturnering</span><span class="sxs-lookup"><span data-stu-id="f8048-135">Purchase order packing slip return</span></span>

<span data-ttu-id="f8048-136">Når der bogføres en økonomisk postering, ændres statussen for transaktionsposten til **Solgt**.</span><span class="sxs-lookup"><span data-stu-id="f8048-136">When a financial transaction is posted, the status of the transaction record is **Sold**.</span></span> <span data-ttu-id="f8048-137">Følgende transaktioner betragtes som økonomiske afgange:</span><span class="sxs-lookup"><span data-stu-id="f8048-137">The following transactions are considered financial issues:</span></span>

-   <span data-ttu-id="f8048-138">Afslutte en produktionsordre</span><span class="sxs-lookup"><span data-stu-id="f8048-138">Ending a production order</span></span>
-   <span data-ttu-id="f8048-139">Salgsordrefaktura</span><span class="sxs-lookup"><span data-stu-id="f8048-139">Sales order invoice</span></span>
-   <span data-ttu-id="f8048-140">Kreditorfakturareturnering</span><span class="sxs-lookup"><span data-stu-id="f8048-140">Vendor invoice return</span></span>
-   <span data-ttu-id="f8048-141">Lagerkladder med negativ mængde, f.eks. bevægelse, driftsregnskab, optælling, styklister og overførsel</span><span class="sxs-lookup"><span data-stu-id="f8048-141">Negative quantity inventory journals, such as movement, profit and loss, counting, bill of materials, and transfer</span></span>

<span data-ttu-id="f8048-142">Transaktioner, der reducerer antallet, bogføres til den løbende gennemsnitskostpris.</span><span class="sxs-lookup"><span data-stu-id="f8048-142">Transactions that decrease quantity are posted at the running average cost price.</span></span> <span data-ttu-id="f8048-143">Proceduren til lagerlukning er derfor påkrævet for at udligne afgangsposteringer i forhold til tilgangsposteringer på baggrund af den lagermodel, der er knyttet til hver vare.</span><span class="sxs-lookup"><span data-stu-id="f8048-143">Therefore, the inventory close procedure is required in order to settle issue transactions to receipt transactions, based on the inventory model that is assigned to each item.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]