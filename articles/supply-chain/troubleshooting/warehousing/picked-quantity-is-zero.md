---
title: Du kan ikke bekræfte en forsendelse, fordi antallet er nul
description: Du kan ikke bekræfte en forsendelse, fordi antallet er nul
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
ms.openlocfilehash: 7a06f0651db741a867e1e9fe7dbab841a928c22b
ms.sourcegitcommit: cd9016e9787169cb800889d335b9c5919ddbe4af
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/23/2021
ms.locfileid: "5938440"
---
# <a name="you-cant-confirm-a-shipment-because-there-is-zero-quantity"></a><span data-ttu-id="1725c-103">Du kan ikke bekræfte en forsendelse, fordi antallet er nul</span><span class="sxs-lookup"><span data-stu-id="1725c-103">You can't confirm a shipment because there is zero quantity</span></span>

<span data-ttu-id="1725c-104">Fejlkode: LoadLineWarningUpdatedToZero</span><span class="sxs-lookup"><span data-stu-id="1725c-104">Error code: LoadLineWarningUpdatedToZero</span></span>

## <a name="symptoms"></a><span data-ttu-id="1725c-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="1725c-105">Symptoms</span></span>

<span data-ttu-id="1725c-106">Når du forsøger at bekræfte en forsendelse, vises følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="1725c-106">When you try to confirm a shipment, the system shows the following error message:</span></span>

> <span data-ttu-id="1725c-107">Lastlinje for varen %1 og forsendelsen %2 er blevet opdateret til at have et antal på nul på grund af konfiguration af underlevering, som ikke tillader, at der sendes nogen mængder af denne vare.</span><span class="sxs-lookup"><span data-stu-id="1725c-107">Load line for item %1 and shipment %2 has been updated to have zero quantity due to underdelivery setup allowing not to ship any quantities for this item.</span></span>

<span data-ttu-id="1725c-108">Du kan derfor ikke bekræfte forsendelsen for lasten.</span><span class="sxs-lookup"><span data-stu-id="1725c-108">Therefore, you can't confirm the shipment for the load.</span></span>

## <a name="cause"></a><span data-ttu-id="1725c-109">Årsag</span><span class="sxs-lookup"><span data-stu-id="1725c-109">Cause</span></span>

<span data-ttu-id="1725c-110">Systemet evaluerer, om det plukkede antal ligger inden for de forventede grænser baseret på plukket antal, lastlinjeantal og underleveringsprocent.</span><span class="sxs-lookup"><span data-stu-id="1725c-110">The system evaluates whether the picked quantity is within the expected limits, based on the picked quantity, load line quantity, and underdelivery percentage.</span></span> <span data-ttu-id="1725c-111">Hvis det plukkede antal på lastlinjen er 0 (nul), kan du ikke bekræfte forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="1725c-111">If the system finds that the picked quantity on the load line is 0 (zero), you can't confirm the shipment.</span></span> <span data-ttu-id="1725c-112">Dette problem kan f.eks. forekomme, hvis arbejdet er blevet annulleret, og underleveringsprocenten på lastlinjen er 100 procent.</span><span class="sxs-lookup"><span data-stu-id="1725c-112">For example, this issue might occur if work has been canceled, and the underdelivery percentage on the load line is 100 percent.</span></span>

## <a name="resolution"></a><span data-ttu-id="1725c-113">Løsning</span><span class="sxs-lookup"><span data-stu-id="1725c-113">Resolution</span></span>

<span data-ttu-id="1725c-114">Kontrollér lastlinjerne for at sikre, at underleveringsprocenten og -mængderne er tilpasset det plukkede arbejde.</span><span class="sxs-lookup"><span data-stu-id="1725c-114">Check your load lines to make sure that the underdelivery percentage and quantities are aligned with the picked work.</span></span>

1. <span data-ttu-id="1725c-115">Gå til **Lokationsstyring \> Laster \> Alle laster**.</span><span class="sxs-lookup"><span data-stu-id="1725c-115">Go to **Warehouse management \> Loads \> All loads**.</span></span>
1. <span data-ttu-id="1725c-116">Vælg den last, som forsendelsen ikke kan bekræftes for.</span><span class="sxs-lookup"><span data-stu-id="1725c-116">Select the load that the shipment can't be confirmed for.</span></span>
1. <span data-ttu-id="1725c-117">Vælg lastlinjen for den vare, der overstiger underleveringsprocenten, i oversigtspanelet **Lastlinjer**.</span><span class="sxs-lookup"><span data-stu-id="1725c-117">On the **Load lines** FastTab, select the load line for the item that exceeds the underdelivery percentage.</span></span>
1. <span data-ttu-id="1725c-118">Juster værdien i feltet **Underlevering** eller feltet **Antal** efter behov.</span><span class="sxs-lookup"><span data-stu-id="1725c-118">Adjust the value of the **Underdelivery** field or the **Quantity** field as required.</span></span>

> [!TIP]
> <span data-ttu-id="1725c-119">Hvis problemet stadig ikke er løst, skal du muligvis udføre mere plukarbejde for de relaterede salgsordrer eller flytteordrer, indtil det tilgængelige antal stemmer med lasten eller forsendelsen.</span><span class="sxs-lookup"><span data-stu-id="1725c-119">If the issue still isn't fixed, you might have to complete more picking work for the related sales orders or transfer orders until the available quantity is aligned with the load or shipment.</span></span>
