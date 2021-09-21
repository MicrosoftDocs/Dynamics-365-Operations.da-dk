---
title: Betingelser i samhandelsaftalen gælder ikke for importerede ordrelinjer
description: Priser og rabatter i samhandelsaftaler anvendes ikke på salgs- eller indkøbsordrelinjer, der er importeret via Dataadministration
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
ms.openlocfilehash: fef38819efaff2f2a927cf09fc7f469490149574
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475932"
---
# <a name="trade-agreement-conditions-arent-applied-to-imported-order-lines"></a>Betingelser i samhandelsaftalen gælder ikke for importerede ordrelinjer

## <a name="symptoms"></a>Symptomer

Samhandelsaftaler, der anvendes på salgs- eller indkøbsordrelinjer, gælder ikke på linjer, der er importeret via Dataadministration. De samme samhandelsaftaler anvendes dog på salgs- eller indkøbsordrelinjer, der er oprettet manuelt.

## <a name="cause"></a>Årsag

Hvis indkøbsordrelinjer, der importeres via Dataadministration, allerede indeholder prisoplysninger, evalueres samhandelsaftalen ikke igen for disse linjer. Hvis f.eks. **Linjerabatprocent** eller nogen af pris- og rabatværdierne er angivet for en linje, vil samhandelsaftaler ikke blive slået op for denne linje.

## <a name="workaround"></a>Løsning

Denne funktionsmåde forventes og er ens for både salgsordrer og indkøbsordrer.

Du kan løse problemet ved at importere indkøbsordrelinjerne uden at angive prisoplysninger. Samhandelsaftalerne vil derefter blive anvendt, og indkøbsordrelinjerne opdateres på baggrund af de definerede samhandelsaftaler.
