---
title: Antal i en igangsat karantæneordre opdateres ikke, når ordren opdeles
description: Når du opretter en karantæneordre og forsøger at opdele den, opdateres ordreantallet ikke til det opdelte restantal.
author: niwang
ms.date: 4/11/2021
ms.topic: troubleshooting
ms.search.form: InventQuarantineOrder
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: shawan
ms.search.validFrom: 2021-04-11
ms.dyn365.ops.version: 10.0.19
ms.openlocfilehash: a8af535257ce217629d5ba92e624623c3ea39345
ms.sourcegitcommit: c011a2ef66b38e71ddaf003f7d243677bb2707c5
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/12/2021
ms.locfileid: "6026384"
---
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a><span data-ttu-id="f6c33-103">Antal i en igangsat karantæneordre opdateres ikke, når ordren opdeles</span><span class="sxs-lookup"><span data-stu-id="f6c33-103">Quantity on a started quarantine order isn't updated when the order is split</span></span>

<span data-ttu-id="f6c33-104">KB-nummer: 4613113</span><span class="sxs-lookup"><span data-stu-id="f6c33-104">KB number: 4613113</span></span>

## <a name="symptoms"></a><span data-ttu-id="f6c33-105">Symptomer</span><span class="sxs-lookup"><span data-stu-id="f6c33-105">Symptoms</span></span>

<span data-ttu-id="f6c33-106">Når du opretter en karantæneordre og forsøger at opdele den, opdateres ordreantallet ikke til det opdelte antal efter opdelingen.</span><span class="sxs-lookup"><span data-stu-id="f6c33-106">When you create a quarantine order and try to split it, the order quantity isn't updated to the remaining quantity after the split.</span></span>

## <a name="resolution"></a><span data-ttu-id="f6c33-107">Løsning</span><span class="sxs-lookup"><span data-stu-id="f6c33-107">Resolution</span></span>

<span data-ttu-id="f6c33-108">Systemet ændrer ikke det oprindelige antal fra en karantæneordre for at sikre, at du kan spore det oprindelige antal, der blev oprettet for den pågældende karantæneordre.</span><span class="sxs-lookup"><span data-stu-id="f6c33-108">The system doesn't change the original quantity from a quarantine order to ensure that you can track the original quantity that was created for that quarantine order.</span></span> <span data-ttu-id="f6c33-109">Systemet sporer dog det antal, der er opdelt fra en karantæneordre.</span><span class="sxs-lookup"><span data-stu-id="f6c33-109">However, the system does track the quantity that is split from a quarantine order.</span></span> <span data-ttu-id="f6c33-110">Til denne sporing bruges et databasefelt med navnet `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span><span class="sxs-lookup"><span data-stu-id="f6c33-110">To do this tracking, it uses a database field that is named `QuantityThatHasSplitIntoOtherQuarantineOrders`.</span></span> <span data-ttu-id="f6c33-111">Dette felt er dog ikke synligt i brugergrænsefladen (UI).</span><span class="sxs-lookup"><span data-stu-id="f6c33-111">However, this field isn't visible in the user interface (UI).</span></span>
