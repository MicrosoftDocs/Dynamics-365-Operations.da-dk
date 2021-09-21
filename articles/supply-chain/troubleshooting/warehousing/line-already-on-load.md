---
title: En af linjerne er allerede på en last
description: Denne side forklarer, hvorfor du kan have modtaget fejlen, "En af linjerne er allerede på en last. Det var ikke muligt at frigive til lagerstedet", og hvordan problemet kan løses.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 0bdfaed005b9c58f7bd5f87dd6dffe648de47261
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475954"
---
# <a name="one-of-the-lines-is-already-on-a-load"></a>En af linjerne er allerede på en last

## <a name="symptoms"></a>Symptomer

Når du arbejder med opbygning af last og forsendelser, kan du få vist følgende fejlmeddelelse:

> En af linjerne er allerede på en last. Kan ikke frigive til lagersted.

Hvis du opretter laster manuelt, eller hvis du konfigurerer processen, så der allerede er oprettet laster før indtastning af salgsordrelinjer, forudsættes det, at den efterfølgende frigivelse udføres manuelt, og at ruten og vurderingen fra lasten vil blive anvendt.

I et andet muligt scenario forsøger du at foretage automatisk frigivelse til lagerstedet, men bølgeprocessen kunne ikke oprette arbejde. Derfor oprettes der stadig en åben forsendelse eller last. Denne åbne forsendelse eller last blokerer derefter efterfølgende forsøg på automatisk at frigive ordren, indtil du enten sletter den åbne forsendelse eller last eller manuelt genbehandler bølgen.

## <a name="resolution"></a>Løsning

Du kan frigive fra salgsordresiden, eller automatisk frigivelse kan udføres fra siden Frigiv salgsordre, hvis der ikke findes en last før frigivelsen til lagerstedet. Lasten oprettes automatisk, når bølgen er behandlet.
