---
title: Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten
description: Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten Kontroller åbne antal.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventOpenQtyCritical
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 9508d6d75d8ebee7ca10140ed4c4215d7ad1dda7
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026371"
---
# <a name="physically-received-purchase-orders-dont-appear-on-the-inventory-closing-report"></a><span data-ttu-id="e98c2-103">Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten</span><span class="sxs-lookup"><span data-stu-id="e98c2-103">Physically received purchase orders don't appear on the inventory closing report</span></span>

<span data-ttu-id="e98c2-104">KB-nummer: 4612595</span><span class="sxs-lookup"><span data-stu-id="e98c2-104">KB number: 4612595</span></span>

## <a name="symptoms"></a><span data-ttu-id="e98c2-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="e98c2-105">Symptoms</span></span>

<span data-ttu-id="e98c2-106">Fysisk modtagne indkøbsordrer vises ikke i lagerlukningsrapporten **Kontroller åbne antal**.</span><span class="sxs-lookup"><span data-stu-id="e98c2-106">Physically received purchase orders don't appear on the **Check open quantities** inventory closing report.</span></span>

## <a name="resolution"></a><span data-ttu-id="e98c2-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="e98c2-107">Resolution</span></span>

<span data-ttu-id="e98c2-108">Rapporten **Kontroller åbne antal** viser afgangsposteringer, der ikke kan udlignes mod økonomisk opdaterede lagertilgange pr. den valgte slutdato.</span><span class="sxs-lookup"><span data-stu-id="e98c2-108">The **Check open quantities** report shows issue transactions that can't be settled against financially updated inventory receipts as of the selected closing date.</span></span> <span data-ttu-id="e98c2-109">Du kan vælge at medtage fysiske tilgange i rapporten.</span><span class="sxs-lookup"><span data-stu-id="e98c2-109">You can choose to include physical receipts on the report.</span></span> <span data-ttu-id="e98c2-110">Hvis du gør det, vises fysiske tilgange, hvis de kan dække afgangsposteringer, der ikke kan udlignes.</span><span class="sxs-lookup"><span data-stu-id="e98c2-110">In that case, physical receipts will be shown if they can cover the issue transactions that can't be settled.</span></span> <span data-ttu-id="e98c2-111">Du finder flere oplysninger under [Forberede kørsel af lagerlukning](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span><span class="sxs-lookup"><span data-stu-id="e98c2-111">For more information, see [Preparing to run inventory close](/dynamicsax-2012/appuser-itpro/preparing-to-run-inventory-close).</span></span>
