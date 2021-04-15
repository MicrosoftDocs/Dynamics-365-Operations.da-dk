---
title: Lagerafmærkning med planlægningsoptimering
description: Dette emne indeholder oplysninger om de indstillinger, der er tilgængelige for at afmærke lagerbeholdningen i autoriserede ordrer, når du bruger Planlægningsoptimering.
author: ChristianRytt
ms.date: 12/02/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MpsIntegrationParameters, MpsFitAnalysis
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2020-12-02
ms.dyn365.ops.version: AX 10.0.13
ms.openlocfilehash: 3b139673ddf17e13d6687db485208e1aeb3908dc
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/01/2021
ms.locfileid: "5809488"
---
# <a name="inventory-marking-with-planning-optimization"></a><span data-ttu-id="ccaf3-103">Lagerafmærkning med planlægningsoptimering</span><span class="sxs-lookup"><span data-stu-id="ccaf3-103">Inventory marking with Planning Optimization</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ccaf3-104">Dette emne indeholder oplysninger om de indstillinger, der er tilgængelige for at afmærke lagerbeholdningen i autoriserede ordrer, når du bruger Planlægningsoptimering.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-104">This topic provides information about the options that are available for marking inventory in firmed orders when you use Planning Optimization.</span></span>

<span data-ttu-id="ccaf3-105">*Afmærkning* bruges til at sammenkæde udbud og efterspørgsel.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-105">*Marking* is used to link supply and demand.</span></span> <span data-ttu-id="ccaf3-106">Det ligner *udligning*, som angiver, hvordan varedisponering forventer at dække behov.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-106">It resembles *pegging*, which indicates how master planning expects to cover demand.</span></span> <span data-ttu-id="ccaf3-107">Fra et planlægningssynspunkt er den væsentligste forskel, at afmærkning er mere permanent end udligning.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-107">From a planning point of view, the main difference is that marking is more permanent than pegging.</span></span>

<span data-ttu-id="ccaf3-108">Der blev introduceret afmærkning for at understøtte særlige efter efterkalkulationsscenarier for FIFO (First In, First Out) og LIFO (Last In First Out).</span><span class="sxs-lookup"><span data-stu-id="ccaf3-108">Marking was introduced to support special costing scenarios for first in, first out (FIFO) and last in, first out (LIFO).</span></span> <span data-ttu-id="ccaf3-109">Men det bruges nu også til visse ikke-efterkalkulationsscenarier.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-109">However, it's now also used for some non-costing scenarios.</span></span> <span data-ttu-id="ccaf3-110">Afmærkningen mellem udbud og efterspørgsel er valgfri og næsten permanent.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-110">Marking between supply and demand is optional and almost permanent.</span></span> <span data-ttu-id="ccaf3-111">Afmærkning kan fjernes manuelt af brugeren, eller den kan fjernes ved at køre en udfoldning af salgsordrelinje, hvor indstillingen **Fjern afmærkning** er valgt.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-111">Marking can be removed manually by a user, or it can be removed by running a sales order line explosion where the **Remove marking** option is selected.</span></span>

<span data-ttu-id="ccaf3-112">Udligning styres af varedisponeringen under disponeringen for at knytte efterspørgslen til det påkrævede udbud.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-112">Pegging is controlled by master planning during coverage to link demand with the required supply.</span></span> <span data-ttu-id="ccaf3-113">Udligningen kan opdateres for hver planlægningskørsel for at optimere den forsyning, der kræves for at dække behovet.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-113">Pegging can be updated for each planning run to optimize the supply that is required to cover demand.</span></span> <span data-ttu-id="ccaf3-114">Når varedisponering opdaterer oplysninger om udligning, respekteres de eventuelle eksisterende afmærkninger.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-114">When master planning updates pegging information, it respects any existing marking.</span></span>

<span data-ttu-id="ccaf3-115">Udligningen starter ved at inkludere relevant afmærkning, reservation af disponibelt lager og reservation ved ordreafgivelse i følgende rækkefølge:</span><span class="sxs-lookup"><span data-stu-id="ccaf3-115">Pegging starts by including relevant marking, on-hand reservations, and on-order reservations, in the following sequence:</span></span>

1. <span data-ttu-id="ccaf3-116">Afmærkning mellem efterspørgsel og udbud</span><span class="sxs-lookup"><span data-stu-id="ccaf3-116">Marking between demand and supply</span></span>
1. <span data-ttu-id="ccaf3-117">Reservationer af disponibelt lager</span><span class="sxs-lookup"><span data-stu-id="ccaf3-117">On-hand reservations</span></span>
1. <span data-ttu-id="ccaf3-118">Reservationer ved ordreafgivelse</span><span class="sxs-lookup"><span data-stu-id="ccaf3-118">On-order reservations</span></span>

<span data-ttu-id="ccaf3-119">Når du autoriserer et ordreforslag, indeholder dialogboksen **Autorisation** feltet **Opdater afmærkning**, som du bruger til at angive afmærkningsindstillinger for de ordrer, der oprettes under autorisation.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-119">When you firm a planned order, the **Firming** dialog box provides an **Update marking** field that you use to set marking options for the orders that are created during firming.</span></span> <span data-ttu-id="ccaf3-120">Vælg en af følgende værdier:</span><span class="sxs-lookup"><span data-stu-id="ccaf3-120">Select one of the following values:</span></span>

- <span data-ttu-id="ccaf3-121">**Nej** – Der anvendes ikke lagerafmærkning.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-121">**No** – No inventory marking is applied.</span></span>
- <span data-ttu-id="ccaf3-122">**Standard** – Lagerafmærkning opdateres i henhold til udligningen.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-122">**Standard** – Inventory marking is updated according to the pegging.</span></span> <span data-ttu-id="ccaf3-123">En behovsordre (efterspørgsel) afmærkes i forhold til en opfyldningsordre (udbud).</span><span class="sxs-lookup"><span data-stu-id="ccaf3-123">A requirement order (demand) is marked against a fulfillment order (supply).</span></span> <span data-ttu-id="ccaf3-124">Hvis der er et restantal på opfyldningsordren, er det ikke afmærket, og referenceoplysningerne er tomme.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-124">If some quantity remains on the fulfillment order, it isn't marked, and the reference information is left blank.</span></span> <span data-ttu-id="ccaf3-125">Hvis en salgsordre på 100 styk f.eks. udlignes mod en indkøbsordre på 150 styk, tildeles referenceoplysningerne kun til salgsordren.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-125">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned only to the sales order.</span></span>
- <span data-ttu-id="ccaf3-126">**Udvidet** – Både behovsordren (efterspørgsel) og opfyldningsordren (udbud) afmærkes, uafhængigt af om der er et restantal i opfyldningsordren.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-126">**Extended** – Both the requirement order (demand) and the fulfillment order (supply) are marked, regardless of any quantity that remains on the fulfillment order.</span></span> <span data-ttu-id="ccaf3-127">Hvis en salgsordre på 100 styk f.eks. udlignes mod en indkøbsordre på 150 styk, tildeles referenceoplysningerne både til salgsordren og indkøbsordren.</span><span class="sxs-lookup"><span data-stu-id="ccaf3-127">For example, if a sales order for 100 ea is pegged against a purchase order for 150 ea, reference information will be assigned to both the sales order and the purchase order.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]