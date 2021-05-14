---
title: Du kan ikke bekræfte en forsendelse, fordi antallet overstiger overleveringsprocenten
description: Du kan ikke bekræfte en forsendelse, fordi antallet overstiger overleveringsprocenten
author: perlynne
ms.date: 04/21/2021
ms.topic: troubleshooting
ms.search.form: WHSLoadTable_WHSShipConfirm,WHSLoadPlanningListPage_WHSShipConfirm,WHSLoadPlanningWorkbench_WHSShipConfirm,WHSTransportLoad_WHSShipConfirm,WHSShipPlanningListPage_WHSShipConfirm,WHSShipmentDetails_WHSShipConfirm,WHSWorkTable_WHSShipConfirm,WHSWorkTableListPage_WHSShipConfirm,Dialog_WHSOutboundShipConfirmController_WHSOutboundShipConfirm
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: lbc
ms.search.validFrom: 2021-04-21
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: c9b5ba8dedb927ee049d7e53e9a666902f563f49
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938444"
---
# <a name="you-cant-confirm-a-shipment-because-the-quantity-exceeds-the-overdelivery-percentage"></a><span data-ttu-id="7ba8a-103">Du kan ikke bekræfte en forsendelse, fordi antallet overstiger overleveringsprocenten</span><span class="sxs-lookup"><span data-stu-id="7ba8a-103">You can't confirm a shipment because the quantity exceeds the overdelivery percentage</span></span>

<span data-ttu-id="7ba8a-104">Fejlkode: WAX1687</span><span class="sxs-lookup"><span data-stu-id="7ba8a-104">Error code: WAX1687</span></span>

## <a name="symptoms"></a><span data-ttu-id="7ba8a-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="7ba8a-105">Symptoms</span></span>

<span data-ttu-id="7ba8a-106">Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="7ba8a-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="7ba8a-107">Forsendelsen for last %1 kunne ikke bekræftes, da antallet for varen %2 overstiger den procentdel, der er defineret for overlevering.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-107">The shipment for load %1 could not be confirmed because the quantity for item %2 exceeds the percentage that is defined for overdelivery.</span></span>

<span data-ttu-id="7ba8a-108">Du kan derfor ikke bekræfte forsendelsen for lasten.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="7ba8a-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="7ba8a-109">Cause</span></span>

<span data-ttu-id="7ba8a-110">Antallet for lasten eller forsendelsen er kun delvist plukket.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-110">The quantity of the load or shipment has been only partially picked.</span></span> <span data-ttu-id="7ba8a-111">Antallet er i øjeblikket større end det plukkede antal med en procentdel, der ligger uden for den tilladte overleveringsprocent.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-111">The quantity currently exceeds the picked quantity by a percentage that is outside the allowed overdelivery percentage.</span></span>

## <a name="resolution"></a><span data-ttu-id="7ba8a-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="7ba8a-112">Resolution</span></span>

<span data-ttu-id="7ba8a-113">Du kan håndtere dette problem ved at udføre en eller flere af følgende opgaver:</span><span class="sxs-lookup"><span data-stu-id="7ba8a-113">To fix this issue, complete one of the following tasks:</span></span>

- <span data-ttu-id="7ba8a-114">Angiv antallet for lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-114">Set the load line quantity.</span></span>
- <span data-ttu-id="7ba8a-115">Angiv overleveringsprocenten.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-115">Set the overdelivery percentage.</span></span>

### <a name="set-the-load-line-quantity"></a><span data-ttu-id="7ba8a-116">Angive antallet for lastlinjen</span><span class="sxs-lookup"><span data-stu-id="7ba8a-116">Set the load line quantity</span></span>

<span data-ttu-id="7ba8a-117">Hvis du vil angive antallet for lastlinjen, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-117">To set the load line quantity, follow these steps.</span></span>

1. <span data-ttu-id="7ba8a-118">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-118">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7ba8a-119">Vælg den last, som forsendelsen ikke kan bekræftes for.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-119">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7ba8a-120">Vælg lastlinjen for den vare, der overstiger overleveringsprocenten, i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-120">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="7ba8a-121">I oversigtspanelet **Linjedetaljer** skal du vælge **Ordre**.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-121">On the **Line details** FastTab, select **Order**.</span></span>
1. <span data-ttu-id="7ba8a-122">I feltet **Antal** skal du angive værdien til det plukkede antal (dvs. værdien for **Antal oprettet under arbejde**), så der kan udstedes en forsendelsesbekræftelse.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-122">In the **Quantity** field, set the value to the picked quantity (that is, to the **Work created quantity** value), so that shipment confirmation can occur.</span></span>

### <a name="set-the-overdelivery-percentage"></a><span data-ttu-id="7ba8a-123">Angive overleveringsprocenten</span><span class="sxs-lookup"><span data-stu-id="7ba8a-123">Set the overdelivery percentage</span></span>

<span data-ttu-id="7ba8a-124">Hvis du vil angive overleveringsprocenten, skal du benytte følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-124">To set the underdelivery percentage, follow these steps.</span></span>

1. <span data-ttu-id="7ba8a-125">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-125">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="7ba8a-126">Vælg den last, som forsendelsen ikke kan bekræftes for.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-126">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="7ba8a-127">Vælg lastlinjen for den vare, der overstiger overleveringsprocenten, i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-127">On the **Load lines** FastTab, select the load line for the item that exceeds the overdelivery percentage.</span></span>
1. <span data-ttu-id="7ba8a-128">I oversigtspanelet **Linjedetaljer** skal du vælge **Generelt**.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-128">On the **Line details** FastTab, select **General**.</span></span>
1. <span data-ttu-id="7ba8a-129">I feltet **Overlevering** skal du angive værdien til en større procentdel, der tager højde for det antal, der er plukket i forhold til lastantallet, så der kan udstedes en forsendelsesbekræftelse.</span><span class="sxs-lookup"><span data-stu-id="7ba8a-129">In the **Overdelivery** field, set the value to a larger percentage that accommodates the quantity that has been picked against the load quantity, so that shipment confirmation can occur.</span></span>
