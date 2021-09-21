---
title: Cluster-profilen blev ikke fundet
description: Når du arbejder med indgående lagerstedsops, kan du få vist en fejl om, at klyngeprofilen ikke kan findes. Kontroller, at klyngeprofiler er konfigureret korrekt.
author: perlynne
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: bbf9c5bc70c8f3ba1fa26db425249e65e82c0518
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475948"
---
# <a name="cluster-profile-cant-be-found"></a>Cluster-profilen blev ikke fundet

## <a name="symptoms"></a>Symptomer

Når du arbejder med indgående lagerstedshandlinger, kan du få vist følgende fejlmeddelelse:

> "Kvalitetsordren %1 er blevet genereret. Cluster-profilen blev ikke fundet. Kontroller konfigurationen."

Denne fejlmeddelelse er relateret til en modtagelsesproces, hvor kvalitetsstyring (QMS) er slået til. Afhængigt af konfigurationerne i dit miljø kan yderligere oplysninger om den transaktion, der genererer fejlmeddelelsen, måske løse problemet.

## <a name="resolution"></a>Løsning

Først skal du gennemse opsætningen for klyngepluk og kontrollere, at dine klyngeprofiler er konfigureret korrekt. Du kan ikke bruge et menupunkt til klyngepluk i mobilenheden, medmindre der er konfigureret klyngeprofiler. Afhængigt af miljøet skal du muligvis også gennemse andre relaterede konfigurationer.
