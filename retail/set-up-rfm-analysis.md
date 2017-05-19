---
title: Konfigurere RFM-analyse
description: Dette emne forklarer, hvordan du konfigurerer en RFM-analyse (Recency, Frequency, Monetary) af dine kunder.
author: josaw1
manager: AnnBe
ms.date: 04/04/2017
ms.topic: article
ms.prod: 
ms.service: Dynamics365Operations
ms.technology: 
audience: Application User
ms.search.scope: AX 7.0.0, Operations, Core, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: Human Translation
ms.sourcegitcommit: 6b1f91f863c8da35362ebb3036e76aa10d95ba65
ms.openlocfilehash: b6f49413d6226a37e16a30a8f68095211faa6d3d
ms.contentlocale: da-dk
ms.lasthandoff: 04/26/2017


---

# <a name="set-up-rfm-analysis"></a>Konfigurere RFM-analyse

[!include[banner](includes/banner.md)]


Dette emne forklarer, hvordan du konfigurerer en RFM-analyse (Recency, Frequency, Monetary) af dine kunder.

En RFM-analyse ((Recency, Frequency, Monetary)) er et marketingværktøj, som din organisation kan bruge til at evaluere de data, der genereres ved debitors køb. Når du har konfigureret RFM-analysen, får debitorer tildelt et beregnet RFM-point, når de foretager indkøb. RFM-resultatet kan være en trecifret vurdering eller et samlet tal, afhængigt af hvordan organisationen har konfigureret RFM-analysen. Hvis din organisation bruger et trecifret vurdering af resultatet, er det første ciffer debitorens recency-vurdering (har debitoren for nyligt foretaget et køb fra organisationen). Det andet ciffer er debitorens frequency-vurdering (hvor ofte debitoren foretager køb fra din organisation). Det tredje ciffer er debitorens monetary-vurdering (hvor mange penge, debitoren bruger, når vedkommende foretager køb fra din organisation). Din organisation har f.eks. oprettet vurderingerne på en skala fra 1 til 5, hvor 5 er den højeste vurdering. I dette tilfælde fortæller en debitorvurdering på 535 dig følgende oplysninger om debitoren:

-   **Recency-vurdering på 5** – Debitoren har foretaget et køb for nylig.
-   **Frequency-vurdering på 3** – Debitoren køber produkter fra din organisation med moderat hyppighed.
-   **Monetary-vurdering på 5** – Når debitoren foretager et køb, bruger vedkommende en betydelig mængde penge.

Hvis organisationen bruger en samlet tal for resultatet, lægges de enkelte vurderinger sammen. Debitoren har i samme eksempel en vurdering på 13 (5 + 3 + 5).




