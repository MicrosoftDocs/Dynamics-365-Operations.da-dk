---
title: Importerede indkøbsordrer viser ugyldige linjenumre
description: Når indkøbsordrer importeres via datastyring, følger numrene på indkøbsordrelinjer ikke den forøgelse, der er defineret i systemparametrene
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
ms.openlocfilehash: e1cf5cf1d04824213f495ac3ebf556796c96611a
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475859"
---
# <a name="imported-purchase-orders-show-incorrect-line-numbers"></a>Importerede indkøbsordrer viser ugyldige linjenumre

## <a name="symptoms"></a>Symptomer

Automatisk genererede linjenumre for indkøbsordrelinjer, der er importeret via *Indkøbsordrelinjer V2*-dataenhed, bruger som standard ikke det stigende systemlinjenummer, der er angivet i systemparametrene. Hvis du opretter en indkøbsordre manuelt og tilføjer linjer via brugergrænsefladen, stiger linjenumrene korrekt. Men hvis du bruger datastyringsstrukturen (DMF - Data Management Framework), stiger de ikke korrekt.

Dette problem opstår, fordi systemet bruger DMF-metoden til at tildele dem, når du importerer linjer via DMF, hvis de ikke allerede er tildelt i den importerede enhed. Metoden øger altid linjenumrene med én.

## <a name="workaround"></a>Løsning

Sørg for, at de ønskede linjenumre allerede er angivet i felterne for linjenummer i dataenheden, når du importerer indkøbsordrelinjerne. I dette tilfælde overskriver DMF ikke linjenumrene.
