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
# <a name="reduce-balance-depreciation-after-a-split"></a>Reducere saldoafskrivning efter en opdeling

[!include [banner](../includes/banner.md)]

I dette emne beskrives den metode, der bruges i anlægsaktiver til at beregne afskrivninger, efter at et aktiv er opsplittet til et andet aktiv ved hjælp af metoden til reduktion af saldoen. Det afskrivningsår, der er konfigureret i anlægskartoteket, er regnskabsåret. Du kan finde flere oplysninger i [Reducere saldoafskrivning](reduce-balance-depreciation.md) og [Opdele et anlægsaktiv](tasks/split-fixed-asset.md).

Hvis du opdeler et anlægsaktiv i en regnskabsperiode, der ligger senere end den periode, hvor aktivet blev anskaffet, vil den reducerede saldoafskrivning være kontoen for aktivets bogførte nettoværdi (NBV) for det foregående år. Den vil også redegøre for de reguleringsposteringer for anskaffelse og afskrivning, der er genereret fra den postering, der opdeler aktivet. Det antages, at aktivet blev anskaffet i et regnskabsår og opdelt i et senere regnskabsår. Det beløb, der skal afskrives for det oprindelige aktiv, efter at opdelingen afspejler anlægsaktivets NBV, før aktivet blev opdelt, og den reguleringspostering for anskaffelse og afskrivning, der er bogført for opdelingen.

Følgende betingelser gælder f. eks.:

- Regnskabsperioden går fra 30. juni til 1. juli.
- Saldoen for reduceringsprocenten er 18 %, og et aktiv anskaffes i juni 2019 til en anskaffelsespris på $10.000.
- Afskrivningen af det første regnskabsår er lig med $18.000, den månedlige afskrivning er lig med $150, og aktivet afskrives derefter indtil november 2019 med $738.75.
- I november 2019 opdeles 80 procent af aktivet på et andet anlægsaktiv.

[![Reducere saldoafskrivning efter en opdeling](./media/reduce-balance-depreciation-after-split.png)](./media/reduce-balance-depreciation-after-split.png)

Det beløb, der skal afskrives for det oprindelige anlæg, er $1.822,25. Dette beløb er lig med NBV, før den opdelte transaktion bogføres ($9.111,25), plus den anskaffelsesregulering, der genereres under bogføring af den opdelte transaktion (-$8.000), plus den afskrivningsregulering, der genereres under den opdelte transaktion ($711). Derfor er afskrivningen for det andet år (1.822,25 × 18 procent) ÷ 12 = $27,33.

Det beløb, der skal afskrives for det nye anlægsaktiv i det første år, er (8.000 × 18 procent) ÷ 12 = $120.


[!INCLUDE[footer-include](../../includes/footer-banner.md)]