---
title: Konfigurere RFM-analyse
description: Dette emne forklarer, hvordan du konfigurerer en RFM-analyse (Recency, Frequency, Monetary) af dine kunder.
author: josaw1
manager: AnnBe
ms.date: 06/20/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-365-retail
ms.technology: 
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations, Retail
ms.custom: 78943
ms.assetid: 8ff9aac3-5ada-4150-85fd-18901c926d53
ms.search.region: global
ms.search.industry: Retail
ms.author: josaw
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0, Retail July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: d2ed273acd444045402e94f07ac9a8658bca2a66
ms.contentlocale: da-dk
ms.lasthandoff: 11/03/2017

---

# <a name="set-up-rfm-analysis"></a>Konfigurere RFM-analyse

[!include[banner](includes/banner.md)]


Dette emne forklarer, hvordan du konfigurerer en RFM-analyse (Recency, Frequency, Monetary) af dine kunder.

En RFM-analyse ((Recency, Frequency, Monetary)) er et marketingværktøj, som din organisation kan bruge til at evaluere de data, der genereres ved debitors køb. Når du har konfigureret RFM-analysen, får debitorer tildelt et beregnet RFM-point, når de foretager indkøb. RFM-resultatet kan være en trecifret vurdering eller et samlet tal, afhængigt af hvordan organisationen har konfigureret RFM-analysen. Hvis din organisation bruger et trecifret vurdering af resultatet, er det første ciffer debitorens recency-vurdering (har debitoren for nyligt foretaget et køb fra organisationen). Det andet ciffer er debitorens frequency-vurdering (hvor ofte debitoren foretager køb fra din organisation). Det tredje ciffer er debitorens monetary-vurdering (hvor mange penge, debitoren bruger, når vedkommende foretager køb fra din organisation). Din organisation har f.eks. oprettet vurderingerne på en skala fra 1 til 5, hvor 5 er den højeste vurdering. I dette tilfælde fortæller en debitorvurdering på 535 dig følgende oplysninger om debitoren:

-   **Recency-vurdering på 5** – Debitoren har foretaget et køb for nylig.
-   **Frequency-vurdering på 3** – Debitoren køber produkter fra din organisation med moderat hyppighed.
-   **Monetary-vurdering på 5** – Når debitoren foretager et køb, bruger vedkommende en betydelig mængde penge.

Hvis organisationen bruger en samlet tal for resultatet, lægges de enkelte vurderinger sammen. Debitoren har i samme eksempel en vurdering på 13 (5 + 3 + 5).




