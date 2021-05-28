---
title: Ved varedisponering oprettes der ordreforslag til fantomprodukter
description: Der oprettes ordreforslag til fantomprodukter, når varedisponeringskørslen har fundet sted.
author: ChristianRytt
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: anderso
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: 1ea4bdb3729d163126234e02524cef331051cd48
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026378"
---
# <a name="master-planning-generates-planned-orders-for-phantom-products"></a><span data-ttu-id="3c8f9-103">Ved varedisponering oprettes der ordreforslag til fantomprodukter</span><span class="sxs-lookup"><span data-stu-id="3c8f9-103">Master planning generates planned orders for phantom products</span></span>

<span data-ttu-id="3c8f9-104">KB-nummer: 4614729</span><span class="sxs-lookup"><span data-stu-id="3c8f9-104">KB number: 4614729</span></span>

## <a name="symptoms"></a><span data-ttu-id="3c8f9-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="3c8f9-105">Symptoms</span></span>

<span data-ttu-id="3c8f9-106">Der oprettes ordreforslag til fantomprodukter, når varedisponeringskørslen har fundet sted.</span><span class="sxs-lookup"><span data-stu-id="3c8f9-106">Planned orders are generated for phantom products after master planning is run.</span></span>

## <a name="resolution"></a><span data-ttu-id="3c8f9-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="3c8f9-107">Resolution</span></span>

<span data-ttu-id="3c8f9-108">Valg for **Fantom**-indstillingen for frigivne produkter bestemmer standardlinjetypen på styklisten.</span><span class="sxs-lookup"><span data-stu-id="3c8f9-108">The setting of the **Phantom** option for released products determines the default line type on the bill of material (BOM).</span></span> <span data-ttu-id="3c8f9-109">Når indstillingen **Fantom** er angivet til *Ja*, opretter systemet stadig ordreforslag for varen, men indstillingen **Direkte afledt behov** for hvert ordreforslag angives til *Ja*.</span><span class="sxs-lookup"><span data-stu-id="3c8f9-109">When the **Phantom** option is set to *Yes*, the system will still create planned orders for the item, but the **Directly derived requirement** option for each planned order will be set to *Yes*.</span></span> <span data-ttu-id="3c8f9-110">Produktionsordreforslaget kan derfor ikke autoriseres alene.</span><span class="sxs-lookup"><span data-stu-id="3c8f9-110">Therefore, the planned production order can't be firmed on its own.</span></span> <span data-ttu-id="3c8f9-111">Det medtages i stedet altid automatisk, når den overordnede produktionsordre autoriseres automatisk.</span><span class="sxs-lookup"><span data-stu-id="3c8f9-111">Instead, it will always be automatically included when the parent production order is firmed.</span></span> <span data-ttu-id="3c8f9-112">Styklistelinjerne i fantomordreforslaget medtages desuden i styklisten for den overordnede produktionsordre.</span><span class="sxs-lookup"><span data-stu-id="3c8f9-112">Additionally, the BOM lines of the planned phantom order will be included in the BOM of the parent production order.</span></span>
