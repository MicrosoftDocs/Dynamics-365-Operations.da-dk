---
title: Reserver den samme batch til en salgsordre
description: I denne artikel beskrives det, hvordan du konfigurerer et produkt til at tillade reservation af lager i forhold til et enkelt batch af lageret.
author: omulvad
manager: tfehr
ms.date: 03/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResStorageDimensionGroup, EcoResTrackingDimensionGroup, InventBatch, InventModelGroup, PdsAskSameLotForm, PdsCustSellableDays, WHSReservationHierarchy, WHSInventTableReservationHierarchy
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.custom: 28911
ms.assetid: 5823d75e-f839-46dd-beb3-e09b79fc8aa4
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: kamaybac
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ce750745d6f094a296b43827568ee1745179de2d
ms.sourcegitcommit: 827d77c638555396b32d36af5d22d1b61dafb0e8
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/16/2020
ms.locfileid: "4425041"
---
# <a name="reserve-the-same-batch-for-a-sales-order"></a><span data-ttu-id="81993-103">Reserver den samme batch til en salgsordre</span><span class="sxs-lookup"><span data-stu-id="81993-103">Reserve the same batch for a sales order</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="81993-104">I denne artikel beskrives det, hvordan du konfigurerer et produkt til at tillade reservation af lager i forhold til et enkelt batch af lageret.</span><span class="sxs-lookup"><span data-stu-id="81993-104">This article explains how to set up a product to allow reservation of inventory against a single batch of inventory.</span></span>

<span data-ttu-id="81993-105">Hvis du reserverer fra samme batch, kan du reservere lager til en salgsordrelinje i forhold til en enkelt lagerbatch.</span><span class="sxs-lookup"><span data-stu-id="81993-105">Same batch reservation lets you reserve inventory for a sales order line against a single batch of inventory.</span></span> <span data-ttu-id="81993-106">En kunde, der f.eks. bestiller tapet, kan anmode om, at hele ordren skal bestilles fra det samme batch eller parti for at undgå, at rullerne er forskellige.</span><span class="sxs-lookup"><span data-stu-id="81993-106">For example, a customer who orders wallpaper can request that the whole order be filled from the same batch or lot, to avoid inconsistencies among the rolls.</span></span> <span data-ttu-id="81993-107">Hvis du vil konfigurere et produkt, så den anvender den samme batchreservation, skal følgende indstillinger være aktive i den varemodelgruppe, sporingsdimensionsgruppe og lagringsdimensionsgruppe, du knytter til produktet.</span><span class="sxs-lookup"><span data-stu-id="81993-107">To set up a product to use same batch reservation, the following settings must be active in the item model group, tracking dimension group, and storage dimension group that you assign to the product:</span></span>

- <span data-ttu-id="81993-108">**Varemodelgrupper** – For varemodelgruppen skal felterne **Valg af samme batch** og **Konsolider krav** være valgt for feltgruppen **Reservation** for lagerpolitikker.</span><span class="sxs-lookup"><span data-stu-id="81993-108">**Item model groups** – The item model group must have the **Same batch selection** and **Consolidate requirement** fields selected in the **Reservation** field group for inventory policies.</span></span>
- <span data-ttu-id="81993-109">**Sporingsdimensionsgrupper** – For sporingsdimensionsgruppen skal feltet **Disponer pr. dimension** være valgt for batchnummeret.</span><span class="sxs-lookup"><span data-stu-id="81993-109">**Tracking dimensions groups** – The tracking dimension group must have the **Coverage plan by dimension** field selected for the batch number.</span></span>
- <span data-ttu-id="81993-110">**Lagringsdimensionsgrupper** – For lagringsdimensionsgruppen skal feltet **Disponer pr. dimension** være valgt for **Lokation** og **Lagersted**.</span><span class="sxs-lookup"><span data-stu-id="81993-110">**Storage dimensions groups** – The storage dimension group must have the **Coverage plan by dimension** field selected for **Site** and **Warehouse**.</span></span>

<span data-ttu-id="81993-111">Når du reserverer lager til et produkt på en salgsordrelinje, der er konfigureret til valg af samme batch, forsøger systemet at reservere det antal, der er bestilt fra en enkelt lagerbatch.</span><span class="sxs-lookup"><span data-stu-id="81993-111">When you reserve inventory for a product on a sales order line that is set up for same batch selection, the system tries to reserve the ordered quantity from a single inventory batch.</span></span> <span data-ttu-id="81993-112">Der tages også højde for eventuelle specifikke krav til batchattributter.</span><span class="sxs-lookup"><span data-stu-id="81993-112">Any specific batch attribute requirements are also considered.</span></span> <span data-ttu-id="81993-113">Hvis antallet ikke kan opfyldes fra en enkelt batch, vises siden **Konflikt ved reservation af samme batch**.</span><span class="sxs-lookup"><span data-stu-id="81993-113">If the quantity can't be filled from a single batch, the **Same batch reservation conflict** page appears.</span></span> <span data-ttu-id="81993-114">Denne side beskriver problemerne og de handlinger, du kan udføre for at fortsætte reservationen.</span><span class="sxs-lookup"><span data-stu-id="81993-114">This page describes the issues and also the actions that you can take to continue with the reservation.</span></span> <span data-ttu-id="81993-115">Følgende betingelser kan forhindre, at batchen kan reserveres:</span><span class="sxs-lookup"><span data-stu-id="81993-115">The following conditions might prevent the batch from being reserved:</span></span>

- <span data-ttu-id="81993-116">Dispositionskoden for batchen har **Spær reservation** for salg angivet til **Blokeret**.</span><span class="sxs-lookup"><span data-stu-id="81993-116">The batch disposition code has **Block reservation** for sales flagged as **Blocked**.</span></span>
- <span data-ttu-id="81993-117">Batchen er udløbet på baggrund af udløbsdatoen og eventuelle salgbare dage for debitor.</span><span class="sxs-lookup"><span data-stu-id="81993-117">The batch has expired, based on the expiration date and any applicable customer sellable days.</span></span> <span data-ttu-id="81993-118">Varen kan stadig reserveres, hvis varemodelgruppen for varen er angivet til FEFO-datokontrolleret, og hvis sidste holdbarhedsdato er angivet under Kriterier for plukning.</span><span class="sxs-lookup"><span data-stu-id="81993-118">The item can still be considered for reservation if the item model group for the item is First Expiry First Out (FEFO) date–controlled, and if the best-before date is selected as the pick criterion.</span></span>
- <span data-ttu-id="81993-119">Batchen har ikke tilstrækkelige hyldelevetidsdage tilbage baseret på udløbsdatoen og sidste holdbarhedsdato samt eventuelle salgbare dage for debitor.</span><span class="sxs-lookup"><span data-stu-id="81993-119">The batch doesn't have enough shelf-life days remaining, based on the expiration date and best-before date, plus any customer sellable days.</span></span>

<span data-ttu-id="81993-120">For varer, der er tilknyttet en lagringsdimensionsgruppe, som **Brug lagerstedsstyringsprocesser** er aktiveret for, kan du reservere specifikke batchnumre ved at bruge et reservationshierarki med det batchnummer for lagerdimensionen, der er defineret over lokationsdimensionen.</span><span class="sxs-lookup"><span data-stu-id="81993-120">For items associated with a storage dimension group that has **Use warehouse management processes** enabled, you can reserve specific batch numbers by using a reservation hierarchy with the batch number inventory dimension defined above the location dimension.</span></span> <span data-ttu-id="81993-121">På siden **Batchreservation** for salgs- og flytteordrelinjer kan du også vælge og reservere flere linjer på baggrund af de tilgængelige batchnumre.</span><span class="sxs-lookup"><span data-stu-id="81993-121">The **Batch reservation** page for sales and transfer order lines also lets you select and reserve multiple lines based on the available batch numbers.</span></span> <span data-ttu-id="81993-122">Du kan finde flere oplysninger om, hvad du skal gøre, hvis du bruger et reservationshierarki, der har batchnummerdimensionen under lokationen, i [Fleksibel reservationspolitik for dimension på lagerstedsniveau](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span><span class="sxs-lookup"><span data-stu-id="81993-122">For more information about what to do if you are using a reservation hierarchy that has the batch number dimension below the location, see [Flexible warehouse-level dimension reservation policy](../warehousing/flexible-warehouse-level-dimension-reservation.md).</span></span>
