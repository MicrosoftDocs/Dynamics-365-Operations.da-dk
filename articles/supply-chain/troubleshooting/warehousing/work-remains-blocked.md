---
title: Arbejde forbliver blokeret
description: Arbejde forbliver blokeret
author: perlynne
ms.date: 04/15/2021
ms.topic: troubleshooting
ms.search.form: WHSWorkTableListPage_WHSWorkUnblocking
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-05-15
ms.dyn365.ops.version: 10.0.18
ms.openlocfilehash: f85364d1ecfadc36b26c3395ab4402d3cb3b1603
ms.sourcegitcommit: 5f5afb46431e1abd8fb6e92e0189914b598dc7fd
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/21/2021
ms.locfileid: "5924124"
---
# <a name="work-remains-blocked"></a><span data-ttu-id="ed406-103">Arbejde forbliver blokeret</span><span class="sxs-lookup"><span data-stu-id="ed406-103">Work remains blocked</span></span>

<span data-ttu-id="ed406-104">Fejlkode: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="ed406-104">Error code: WHSWorkBlockingExecutingWaveReason_ErrorMessage</span></span>

## <a name="symptoms"></a><span data-ttu-id="ed406-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="ed406-105">Symptoms</span></span>

<span data-ttu-id="ed406-106">Systemet viser følgende fejlmeddelelse:</span><span class="sxs-lookup"><span data-stu-id="ed406-106">The system shows the following error message:</span></span>

> <span data-ttu-id="ed406-107">Arbejde %1 forbliver spærret, fordi den relaterede bølge %2 har status %3.</span><span class="sxs-lookup"><span data-stu-id="ed406-107">Work %1 remains blocked because the related wave %2 has status %3.</span></span>

## <a name="cause"></a><span data-ttu-id="ed406-108">Årsag</span><span class="sxs-lookup"><span data-stu-id="ed406-108">Cause</span></span>

<span data-ttu-id="ed406-109">Arbejdet behandles i øjeblikket på en bølge og kan ikke låses op, som angivet med en af følgende forhold:</span><span class="sxs-lookup"><span data-stu-id="ed406-109">The work is currently being processed on a wave and can't be unblocked, as indicated by one of the following conditions:</span></span>

- <span data-ttu-id="ed406-110">Under fanen **Blokeringsårsager** er feltet **Årsag til blokering af arbejde** angivet for en eller flere linjer til *Behandler bølge*.</span><span class="sxs-lookup"><span data-stu-id="ed406-110">On the **Blocking reasons** tab, the **Work blocking reason** field for one or more lines is set to *Processing wave*.</span></span>
- <span data-ttu-id="ed406-111">Når du vælger **Bølge** i gruppen **Relaterede oplysninger** under fanen **Relaterede oplysninger** i handlingsruden, angives feltet **Bølgestatus** til *Behandler*.</span><span class="sxs-lookup"><span data-stu-id="ed406-111">When you select **Wave** in the **Related information** group on the **Related information** tab of the Action Pane, the **Wave status** field is set to *Processing*.</span></span>

## <a name="resolution"></a><span data-ttu-id="ed406-112">Løsning</span><span class="sxs-lookup"><span data-stu-id="ed406-112">Resolution</span></span>

<span data-ttu-id="ed406-113">Vælg **Bølge** i gruppen **Relaterede oplysninger** under fanen **Relaterede oplysninger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ed406-113">On the Action Pane, on the **Related information** tab, in the **Related information** group, select **Wave**.</span></span> <span data-ttu-id="ed406-114">Vælg **Ryd op i bølgedata** i gruppen **Bølge** under fanen **Bølge** på siden **Bølger** i handlingsruden.</span><span class="sxs-lookup"><span data-stu-id="ed406-114">Then, on the **Waves** page, on the Action Pane, on the **Wave** tab, in the **Wave** group, select **Cleanup wave data**.</span></span>

## <a name="workaround"></a><span data-ttu-id="ed406-115">Løsning</span><span class="sxs-lookup"><span data-stu-id="ed406-115">Workaround</span></span>

<span data-ttu-id="ed406-116">Hvis de foregående trin ikke løser problemet, kan du annullere arbejdet med følgende fremgangsmåde.</span><span class="sxs-lookup"><span data-stu-id="ed406-116">If the previous steps didn't fix the issue, you can cancel the work by following these steps.</span></span>

1. <span data-ttu-id="ed406-117">Gå til **Lagerstedsstyring \> Periodiske opgaver \> Oprydning \> Annuller arbejde**.</span><span class="sxs-lookup"><span data-stu-id="ed406-117">Go to **Warehouse management \> Periodic tasks \> Clean up \> Cancel work**.</span></span>
1. <span data-ttu-id="ed406-118">I feltet **Arbejds-id** skal du angive id'et for det arbejde, du vil annullere, og som i øjeblikket har en værdien for **Arbejdsstatus** *Åben*, *I gang*, *Annulleret*, *Kombineret* eller *Lukket*.</span><span class="sxs-lookup"><span data-stu-id="ed406-118">In the **Work ID** field, specify the ID of the work that you want to cancel, and that currently has a **Work status** value of *Open*, *In progress*, *Canceled*, *Combined*, or *Closed*.</span></span>
1. <span data-ttu-id="ed406-119">Vælg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed406-119">Select **OK**.</span></span>
1. <span data-ttu-id="ed406-120">Vælg **Ja** for at bekræfte, at du vil annullere arbejdet.</span><span class="sxs-lookup"><span data-stu-id="ed406-120">Select **Yes** to confirm that you want to cancel the work.</span></span>

<span data-ttu-id="ed406-121">Du kan finde flere oplysninger i [Annullere lagerstedsarbejde for undtagelseshåndtering](../../warehousing/cancel-warehouse-work.md).</span><span class="sxs-lookup"><span data-stu-id="ed406-121">For more information, see [Cancel warehouse work for exception handling](../../warehousing/cancel-warehouse-work.md).</span></span>
