---
title: Ikke-reservere lager på en salgsordrelinje
description: Hvis der er åbent arbejde i forhold til en salgslinje, og du forsøger at reservere lager på linjen, får du vist en fejl. Fuldfør eller slet arbejde, der skal frigør reservationen.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 1a042065dc4cd637aff58e55cf16179b7022f6ca
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475913"
---
# <a name="cant-unreserve-inventory-on-a-sales-order-line"></a>Ikke-reservere lager på en salgsordrelinje

## <a name="symptoms"></a>Symptomer

Hvis der er åbent arbejde i forhold til en salgsordrelinje, og du forsøger at reservere lager på linjen, får du vist følgende fejlmeddelelse.

> Reservationer kan ikke fjernes, fordi der er oprettet arbejde, som er afhængigt af reservationerne.

## <a name="resolution"></a>Løsning

Undersøg, om åbent pakkegruppearbejde findes for at bringe varen fra en pakkestation til et andet sted (f.eks. *Lagerport*). Gennemse posterne på siden **Historik for oprettelse af arbejde** og **Arbejdsdetaljer** for at bestemme, hvad der fysisk reserverer lageret, og fuldfør eller slet derefter arbejdet for at frigøre reservationen.
