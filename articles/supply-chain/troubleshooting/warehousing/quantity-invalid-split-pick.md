---
title: Antallet er ikke gyldigt for enhed %1, når der udføres et opdelt pluk
description: Når du udfører et opdelt pluk på tværs af flere batches, kan du få vist en fejl om, at antallet ikke er gyldigt for %1-enheden. Denne side hjælper med at løse problemet.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: 4627db7400d6ccd81f25f100de4696058ce35c42
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475861"
---
# <a name="quantity-is-not-valid-when-performing-a-split-pick-across-multiple-batches"></a>Antallet er ikke gyldigt, når der udføres et opdelt pluk på tværs af flere batches

## <a name="symptoms"></a>Symptomer

Du får vist denne fejlmeddelelse, når du forsøger at udføre et *opdelt pluk* på tværs af flere batches.

> Antallet er ugyldigt for enheden %1.

## <a name="resolution"></a>Løsning

Lagermedarbejderen skal bruge *Kort pluk* som proces i mobilappen Warehouse Management. Hvis du forsøger at plukke flere batcher fra samme lokation, kan du også bruge indstillingen **Fuld** i appen.
