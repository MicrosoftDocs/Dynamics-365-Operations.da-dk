---
title: Fejl i det samlede antal gode, når en ordre forsøges stoppet
description: Når du forsøger at afslutte en produktionsordre og færdigmelde den, vises der muligvis en fejl i det samlede antal gode. Denne side forklarer, hvorfor og hvordan du udbedrer problemet.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 5f0c2c2ca64ada9d72c0ebd04e7de561aaa52039
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475894"
---
# <a name="total-good-quantity-error-when-trying-to-end-a-production-order"></a>Fejl i det samlede antal gode, når en produktionsordre forsøges stoppet

## <a name="symptoms"></a>Symptomer

Når du forsøger at bogføre en færdigmeldingskladde på en produktionsordre, får du vist følgende fejlmeddelelse:

> I alt færdigmeldt antal gode på produktionen bliver %1. På sidste operation er der i alt tilbagemeldt 0,00".

## <a name="cause"></a>Årsag

Dette problem opstår, hvis de antal, der blev bogført i de sidste operationer, var forkerte. Hvis f.eks. produktion er startet, men det antal, der skal sættes i gang, ikke er tildelt, vil rutekortkladden blive bogført uden nogen linjer. Hvis du vil bekræfte situationen, skal du åbne produktionsordren og derefter vælge **Rutekort** under fanen **Vis** i handlingsruden .

## <a name="resolution"></a>Løsning

Du kan løse dette problem ved at bogføre flere kladder for de operationer, som kladderne ikke er blevet bogført korrekt for. Genstart produktionsordren, og vælg at bogføre de ekstra kladder. Denne handling starter ikke produktionsordren, men den bogfører kladderne. På rutekortet vises derefter de antal, der er bogført, og du skal kunne afslutte produktionsordrerne korrekt.
