---
title: Valutaomregningsproblemer i samhandelsaftale
description: Priserne i samhandelsaftaler genberegnes ikke i henhold til valutaen, når valutaen afviger på en indkøbsordre
author: kamaybac
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: PurchTable, PurchTablePart, PurchRFQTable
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: yanansong
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 1b6dc36c5f5ee6b611eebd81f378399ce1748c63
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475868"
---
# <a name="trade-agreement-currency-conversion-issues"></a>Valutaomregningsproblemer i samhandelsaftale

## <a name="symptoms"></a>Symptomer

Priserne i samhandelsaftaler genberegnes ikke i henhold til valutaen, når valutaen afviger på en indkøbsordre.

## <a name="resolution"></a>Løsning

Med funktionen *Generisk valuta* kan du kun definere priser og rabatter i én valuta. Du kan derefter omregne til andre valutaer efter behov. Når omregningen er udført, kan funktionen desuden automatisk anvende intelligent afrunding.
