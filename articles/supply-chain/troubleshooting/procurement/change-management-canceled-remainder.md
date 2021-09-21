---
title: Annullering af restlevering flytter indkøbsordre til bekræftet tilstand
description: Hvis en leveringsrest annulleres på en indkøbsordre, hvor ændringsstyring er aktiveret, går indkøbsordren til en bekræftet tilstand
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1d8b331bc5699487dff3491d65daa36293f3212f
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475916"
---
# <a name="cancelling-delivery-remainder-moves-purchase-order-to-a-confirmed-state"></a>Annullering af restlevering flytter indkøbsordre til bekræftet tilstand

## <a name="symptoms"></a>Symptomer

I forbindelse med en indkøbsordre, der er underlagt ændringsstyring, og hvis den eneste anmodede ændring er at annullere en leveringsrest på en eller flere af linjerne, går indkøbsordren direkte til en *Bekræftet* tilstand, når den godkendes, og der oprettes ikke en kladde.

## <a name="resolution"></a>Løsning

Annullering af en leveringsrest påvirker ikke indholdet af bekræftelsesjournalen. Denne funktionalitet skal bruges, når linjen er blevet delvist modtaget, og restantallet skal annulleres i procestrinnet, når indkøbsordren er blevet bekræftet af leverandøren.

Hvis dette skal afspejles i indkøbsordrebekræftelsen, skal antallet justeres på indkøbsordrelinjen, så bekræftelsen bliver påkrævet. Hvis der ikke er modtaget noget på linjen, kan du også fjerne antallet. I dette tilfælde er ny bekræftelse påkrævet.
