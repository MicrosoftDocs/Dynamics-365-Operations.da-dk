---
title: Indkøbsordreforslag oprettes, når der findes et indkøb i negative dage
description: Hvis disponeringskoden er Min./maks., opretter planlægningsoptimering et indkøbsordreforslag, når der er et indkøb inden for negative dage.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo,MpsIntegrationParameters
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: ilebedev
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 826496c2de956ff949dd79ab8aa643053719bf75
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026377"
---
# <a name="planned-purchase-order-is-created-when-a-purchase-exists-within-negative-days"></a><span data-ttu-id="5b938-103">Indkøbsordreforslag oprettes, når der findes et indkøb i negative dage</span><span class="sxs-lookup"><span data-stu-id="5b938-103">Planned purchase order is created when a purchase exists within negative days</span></span>

<span data-ttu-id="5b938-104">KB-nummer: 4614298</span><span class="sxs-lookup"><span data-stu-id="5b938-104">KB number: 4614298</span></span>

## <a name="symptoms"></a><span data-ttu-id="5b938-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="5b938-105">Symptoms</span></span>

<span data-ttu-id="5b938-106">Hvis disponeringskoden er *Min./maks.*, opretter planlægningsoptimering et indkøbsordreforslag, når der er et indkøb inden for negative dage.</span><span class="sxs-lookup"><span data-stu-id="5b938-106">If the coverage code is *Min/max*, Planning Optimization creates a planned purchase order when a purchase exists within negative days.</span></span>

## <a name="resolution"></a><span data-ttu-id="5b938-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="5b938-107">Resolution</span></span>

<span data-ttu-id="5b938-108">Planlægningsoptimering understøtter ikke negative dage.</span><span class="sxs-lookup"><span data-stu-id="5b938-108">Planning Optimization doesn't support negative days.</span></span> <span data-ttu-id="5b938-109">Men funktionen sikrer altid, at ordreforslag ikke planlægges inden for leveringstiden i forhold til dags dato.</span><span class="sxs-lookup"><span data-stu-id="5b938-109">However, it always ensures that planned orders won't be scheduled within the lead time relative to the current date.</span></span> <span data-ttu-id="5b938-110">Leveringstiden for indkøbet er f.eks. 10 dage, og en indkøbsordre forventes at ankomme otte dage fra dags dato.</span><span class="sxs-lookup"><span data-stu-id="5b938-110">For example, the purchase lead time is 10 days, and a purchase order is expected to arrive eight days from today.</span></span> <span data-ttu-id="5b938-111">I dette tilfælde bruges indkøbsordren som levering for efterspørgsel, der ligger fem dage fra i dag.</span><span class="sxs-lookup"><span data-stu-id="5b938-111">In this case, the purchase order will be used as supply for demand that is five days from today.</span></span>

<span data-ttu-id="5b938-112">Det anbefales derfor, at du justerer leveringstiderne for at være dækket ind i alle (eller næsten alle) situationer.</span><span class="sxs-lookup"><span data-stu-id="5b938-112">Therefore, we recommend that you adjust your lead times to cover all (or almost all) of your scenarios.</span></span>
