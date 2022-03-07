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
# <a name="quantity-on-a-started-quarantine-order-isnt-updated-when-the-order-is-split"></a>Antal i en igangsat karantæneordre opdateres ikke, når ordren opdeles

KB-nummer: 4613113

## <a name="symptoms"></a>Symptomer

Når du opretter en karantæneordre og forsøger at opdele den, opdateres ordreantallet ikke til det opdelte antal efter opdelingen.

## <a name="resolution"></a>Løsning

Systemet ændrer ikke det oprindelige antal fra en karantæneordre for at sikre, at du kan spore det oprindelige antal, der blev oprettet for den pågældende karantæneordre. Systemet sporer dog det antal, der er opdelt fra en karantæneordre. Til denne sporing bruges et databasefelt med navnet `QuantityThatHasSplitIntoOtherQuarantineOrders`. Dette felt er dog ikke synligt i brugergrænsefladen (UI).
