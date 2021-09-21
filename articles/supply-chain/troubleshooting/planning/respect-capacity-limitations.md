---
title: Varedisponering planlægger der mere end den tilgængelige kapacitet
description: Varedisponering overholder tilsyneladende ikke kapacitetsbegrænsninger og planlægger mere end den tilgængelige kapacitet
author: ChristianRytt
ms.date: 05/31/2021
ms.topic: troubleshooting
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2021-05-31
ms.dyn365.ops.version: 10.0.13
ms.openlocfilehash: 48b3d179bb923ff6f6cc5b6be291408b3eb34d98
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475918"
---
# <a name="master-planning-is-scheduling-more-than-the-available-capacity"></a>Varedisponering planlægger der mere end den tilgængelige kapacitet

## <a name="symptoms"></a>Symptomer

Varedisponering overholder tilsyneladende ikke kapacitetsbegrænsninger og planlægger mere end den tilgængelige kapacitet.

Når du bruger grovplanlægning, hvor der er kapacitetsbegrænsning, og hvor ruten angiver en blanding af behov for både en ressourcegruppe og de enkelte ressourcer, er der en lille risiko for at overbooke på grund af den måde, som algoritmen validerer for kapacitetskonflikter. Denne overbooking kan forekomme, når du bruger hjælpefunktioner til at køre varedisponering. Det sker oftest, hvis der er mange job med forholdsvis kort kørselstid.

## <a name="resolution"></a>Løsning

Hvis det er vigtigt, at der ikke opstår nogen overbooking til grovplanlægning, kan du gøre planlægningsdelen af varedisponering enkelttrådet ved at aktivere indstillingen **Præcis kapacitetsbegrænsning for grovplanlægning** på siden **Parametre for varedisponering**. Denne indstilling er som standard ikke tilgængelig. Du skal manuelt føje den til siden ved hjælp af tilpasningsfunktioner. Når du bruger denne indstilling, kører planlægningen langsommere på grund af manglende parallel behandling.
