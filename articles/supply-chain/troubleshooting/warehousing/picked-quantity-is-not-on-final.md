---
title: Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer
description: Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer
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
ms.openlocfilehash: 23a517e7769dc86ebec30e4f17c62172a6ad8801
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938441"
---
# <a name="you-cant-confirm-a-shipment-because-items-havent-been-picked"></a><span data-ttu-id="49018-103">Du kan ikke bekræfte en forsendelse, fordi der ikke er plukket varer</span><span class="sxs-lookup"><span data-stu-id="49018-103">You can't confirm a shipment because items haven't been picked</span></span>

<span data-ttu-id="49018-104">Fejlkode: LoadNotPickedAndMovedToFinalShippingLocation</span><span class="sxs-lookup"><span data-stu-id="49018-104">Error code: LoadNotPickedAndMovedToFinalShippingLocation</span></span>

## <a name="symptoms"></a><span data-ttu-id="49018-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="49018-105">Symptoms</span></span>

<span data-ttu-id="49018-106">Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="49018-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="49018-107">Nogle af varerne, der skal bruges til lasten %1, er endnu ikke plukket og flyttet til den endelige afsendelseslokation.</span><span class="sxs-lookup"><span data-stu-id="49018-107">Some of the items that are needed for load %1 have not yet been picked and moved to the final shipping location.</span></span>

<span data-ttu-id="49018-108">Du kan derfor ikke bekræfte forsendelsen for lasten.</span><span class="sxs-lookup"><span data-stu-id="49018-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="49018-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="49018-109">Cause</span></span>

<span data-ttu-id="49018-110">Lasten eller forsendelsen kan ikke bekræftes i dens aktuelle tilstand, da en af følgende betingelser kan være til stede:</span><span class="sxs-lookup"><span data-stu-id="49018-110">The load or shipment can't be confirmed in its current state because one of the following conditions might exist:</span></span>

- <span data-ttu-id="49018-111">Det relaterede arbejde er endnu ikke plukket og flyttet til det endelige afsendelsessted.</span><span class="sxs-lookup"><span data-stu-id="49018-111">The related work hasn't yet been picked and moved to the final shipping location.</span></span>
- <span data-ttu-id="49018-112">Det plukkede arbejdsantal svarer ikke til det oprettede arbejdsantal på linjen for lasten.</span><span class="sxs-lookup"><span data-stu-id="49018-112">The picked work quantity doesn't match the created work quantity on the load line.</span></span>

## <a name="resolution"></a><span data-ttu-id="49018-113">Løsning</span><span class="sxs-lookup"><span data-stu-id="49018-113">Resolution</span></span>

<span data-ttu-id="49018-114">Kontrollér de relaterede salgsordrer eller flytteordrer for lasten eller forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="49018-114">Check the related sales orders or transfer orders for the load or shipment.</span></span> <span data-ttu-id="49018-115">Kontrollér, at alt det relaterede arbejde er fuldført på den endelige forsendelseslokation, og at mængderne stemmer overens.</span><span class="sxs-lookup"><span data-stu-id="49018-115">Make sure that all the related work has been completed at the final shipping location, and that the quantities match.</span></span>

1. <span data-ttu-id="49018-116">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="49018-116">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="49018-117">Vælg den last, som forsendelsen ikke kan bekræftes for.</span><span class="sxs-lookup"><span data-stu-id="49018-117">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="49018-118">Vælg linjen for lasten i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="49018-118">On the **Load lines** FastTab, select the load line.</span></span>
1. <span data-ttu-id="49018-119">Notér værdien for feltet **Antal oprettet under arbejde**.</span><span class="sxs-lookup"><span data-stu-id="49018-119">Make a note of the value of the **Work created quantity** field.</span></span>
1. <span data-ttu-id="49018-120">under fanen **Laster** i gruppen **Relaterede oplysninger** i handlingsruden skal du vælge **Arbejde**.</span><span class="sxs-lookup"><span data-stu-id="49018-120">On the Action Pane, on the **Loads** tab, in the **Related information** group, select **Work**.</span></span>
1. <span data-ttu-id="49018-121">Kontrollér, at arbejdet er udført på den endelige forsendelseslokation, og at det plukkede arbejdsantal svarer til det oprettede arbejdsantal på lastlinjen.</span><span class="sxs-lookup"><span data-stu-id="49018-121">Verify that the work has been completed at the final shipping location, and that the picked work quantity matches the created work quantity on the load line.</span></span>
1. <span data-ttu-id="49018-122">Gentag denne procedure for alle lastlinjer for at sikre, at alle kriterier er opfyldt.</span><span class="sxs-lookup"><span data-stu-id="49018-122">Repeat this procedure for all load lines to make sure that all criteria are met.</span></span>
