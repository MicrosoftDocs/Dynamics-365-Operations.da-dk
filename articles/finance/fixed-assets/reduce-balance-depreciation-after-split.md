---
title: Reducere saldoafskrivning efter en opdeling
description: I dette emne beskrives den metode, der bruges i anlægsaktiver til at beregne afskrivninger, efter at et aktiv er opsplittet ved hjælp af metoden til reduktion af saldoen.
author: moaamer
manager: Ann Beebe
ms.date: 11/17/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: roschlom
ms.custom: 4464
ms.assetid: 5f89daf1-acc2-4959-b48d-91542fb6bacb
ms.search.region: Global
ms.author: moaamer
ms.search.validFrom: 2020-11-17
ms.dyn365.ops.version: 10.0.14
ms.openlocfilehash: f276f49e5b1bc2814dc851f1ad4204a151d86c43
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/15/2021
ms.locfileid: "5222377"
---
# <a name="reduce-balance-depreciation-after-a-split"></a><span data-ttu-id="9fae0-103">Reducere saldoafskrivning efter en opdeling</span><span class="sxs-lookup"><span data-stu-id="9fae0-103">Reduce balance depreciation after a split</span></span>

[!include [banner](../includes/banner.md)]

<span data-ttu-id="9fae0-104">I dette emne beskrives den metode, der bruges i anlægsaktiver til at beregne afskrivninger, efter at et aktiv er opsplittet til et andet aktiv ved hjælp af metoden til reduktion af saldoen.</span><span class="sxs-lookup"><span data-stu-id="9fae0-104">This topic describes the method that is used in Fixed assets to calculate depreciation after an asset is split to another asset by using the reduce balance method.</span></span> <span data-ttu-id="9fae0-105">Det afskrivningsår, der er konfigureret i anlægskartoteket, er regnskabsåret.</span><span class="sxs-lookup"><span data-stu-id="9fae0-105">The depreciation year that is configured in the asset book is the fiscal year.</span></span> <span data-ttu-id="9fae0-106">Du kan finde flere oplysninger i [Reducere saldoafskrivning](reduce-balance-depreciation.md) og [Opdele et anlægsaktiv](tasks/split-fixed-asset.md).</span><span class="sxs-lookup"><span data-stu-id="9fae0-106">For more information, see [Reduce balance depreciation](reduce-balance-depreciation.md) and [Split a fixed asset](tasks/split-fixed-asset.md).</span></span>

<span data-ttu-id="9fae0-107">Hvis du opdeler et anlægsaktiv i en regnskabsperiode, der ligger senere end den periode, hvor aktivet blev anskaffet, vil den reducerede saldoafskrivning være kontoen for aktivets bogførte nettoværdi (NBV) for det foregående år.</span><span class="sxs-lookup"><span data-stu-id="9fae0-107">If you split a fixed asset during a fiscal period that is later than the period when the asset was acquired, the reduced balance depreciation will account for the asset's net book value (NBV) for the previous year.</span></span> <span data-ttu-id="9fae0-108">Den vil også redegøre for de reguleringsposteringer for anskaffelse og afskrivning, der er genereret fra den postering, der opdeler aktivet.</span><span class="sxs-lookup"><span data-stu-id="9fae0-108">It will also account for the acquisition and depreciation adjustment transactions that were generated from the transaction that split the asset.</span></span> <span data-ttu-id="9fae0-109">Det antages, at aktivet blev anskaffet i et regnskabsår og opdelt i et senere regnskabsår.</span><span class="sxs-lookup"><span data-stu-id="9fae0-109">This behavior assumes that the asset was acquired in one fiscal year and split in a later fiscal year.</span></span> <span data-ttu-id="9fae0-110">Det beløb, der skal afskrives for det oprindelige aktiv, efter at opdelingen afspejler anlægsaktivets NBV, før aktivet blev opdelt, og den reguleringspostering for anskaffelse og afskrivning, der er bogført for opdelingen.</span><span class="sxs-lookup"><span data-stu-id="9fae0-110">The amount that must be depreciated for the original asset after the split reflects the asset's NBV before the asset was split, and the acquisition and depreciation adjustment transaction that was posted for the split.</span></span>

<span data-ttu-id="9fae0-111">Følgende betingelser gælder f. eks.:</span><span class="sxs-lookup"><span data-stu-id="9fae0-111">For example, the following conditions are in effect:</span></span>

- <span data-ttu-id="9fae0-112">Regnskabsperioden går fra 30. juni til 1. juli.</span><span class="sxs-lookup"><span data-stu-id="9fae0-112">The fiscal period is from June 30 to July 1.</span></span>
- <span data-ttu-id="9fae0-113">Saldoen for reduceringsprocenten er 18 %, og et aktiv anskaffes i juni 2019 til en anskaffelsespris på $10.000.</span><span class="sxs-lookup"><span data-stu-id="9fae0-113">The reducing balance percentage is 18 percent, and an asset is acquired in June 2019 at an acquisition price of $10,000.</span></span>
- <span data-ttu-id="9fae0-114">Afskrivningen af det første regnskabsår er lig med $18.000, den månedlige afskrivning er lig med $150, og aktivet afskrives derefter indtil november 2019 med $738.75.</span><span class="sxs-lookup"><span data-stu-id="9fae0-114">The depreciation of the first fiscal year equals $18,000, the monthly depreciation equals $150, and the asset is then depreciated until November 2019, in the amount of $738.75.</span></span>
- <span data-ttu-id="9fae0-115">I november 2019 opdeles 80 procent af aktivet på et andet anlægsaktiv.</span><span class="sxs-lookup"><span data-stu-id="9fae0-115">In November 2019, 80 percent of the asset is split to another fixed asset.</span></span>

<span data-ttu-id="9fae0-116">[![Reducere saldoafskrivning efter en opdeling](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span><span class="sxs-lookup"><span data-stu-id="9fae0-116">[![Reduce balance depreciation after a split](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)</span></span>

<span data-ttu-id="9fae0-117">Det beløb, der skal afskrives for det oprindelige anlæg, er $1.822,25.</span><span class="sxs-lookup"><span data-stu-id="9fae0-117">The amount to depreciate for the original asset is $1,822.25.</span></span> <span data-ttu-id="9fae0-118">Dette beløb er lig med NBV, før den opdelte transaktion bogføres ($9.111,25), plus den anskaffelsesregulering, der genereres under bogføring af den opdelte transaktion (-$8.000), plus den afskrivningsregulering, der genereres under den opdelte transaktion ($711).</span><span class="sxs-lookup"><span data-stu-id="9fae0-118">This amount equals the NBV before the split transaction is posted ($9,111.25), plus the acquisition adjustment that is generated during posting of the split transaction (-$8,000), plus the depreciation adjustment that is generated during the split transaction ($711).</span></span> <span data-ttu-id="9fae0-119">Derfor er afskrivningen for det andet år (1.822,25 × 18 procent) ÷ 12 = $27,33.</span><span class="sxs-lookup"><span data-stu-id="9fae0-119">Therefore, the depreciation for the second year is (1,822.25 × 18 percent) ÷ 12 = $27.33.</span></span>

<span data-ttu-id="9fae0-120">Det beløb, der skal afskrives for det nye anlægsaktiv i det første år, er (8.000 × 18 procent) ÷ 12 = $120.</span><span class="sxs-lookup"><span data-stu-id="9fae0-120">The amount to depreciate for the new fixed asset in the first year is (8,000 × 18 percent) ÷ 12 = $120.</span></span>


[!INCLUDE[footer-include](../../includes/footer-banner.md)]