---
title: Det tager lang tid at opdatere ordreforslag
description: Når behovsantallet og/eller leveringsdatoen opdateres på et ordreforslag, tager det normalt mindst 30 sekunder pr. ordre at gemme opdateringen
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
ms.openlocfilehash: ccf3305cc18ea0ccf2ac3e9ca0dd507fd12a9da7
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475917"
---
# <a name="planned-orders-take-a-long-time-to-update"></a>Det tager lang tid at opdatere ordreforslag

## <a name="symptoms"></a>Symptomer

Når behovsantallet og/eller leveringsdatoen opdateres på et ordreforslag, tager det normalt mindst 30 sekunder pr. ordre at gemme opdateringen.

## <a name="resolution"></a>Løsning

Dette er et kendt problem med det indbyggede varedisponeringsprogram. Det skyldes den underliggende automatiske udfoldning via styklistestrukturen under redigeringer. Dette problem håndteres i Planlægningsoptimering, hvor en planlægger kan opdatere og godkende de relevante ordrer og, hvor det er relevant, udløse en planlægningskørsel for at opdatere ordreforslag for den underliggende styklistestruktur.

En måde at forbedre ydeevnen med det indbyggede varedisponeringsprogram på er at gennemføre følgende trin:

1. Gå til **Varedisponering \> Opsætning \> Planer \> Behovsplaner**.
1. Vælg en plan.
1. Udvid oversigtspanelet **Tidshorisont i dage**.
1. Angiv **Udfoldning** til *Ja*, og angiv feltet under denne indstilling til 0 (nul).

> [!NOTE]
> Dette vil begrænse den periode for udfoldning, der udføres for denne behovsplan, til en enkelt dag.
