---
title: Heltal afrundet forkert, når der beregnes produktkonfigurationsmodeller
description: Heltal afrundet forkert, når der beregnes produktkonfigurationsmodeller. Løs problemet med en tilføjet decimalattribut og beregning.
author: SmithaNataraj
ms.date: 06/24/2021
ms.topic: troubleshooting
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: smnatara
ms.search.validFrom: 2021-06-24
ms.dyn365.ops.version: 10.0.20
ms.openlocfilehash: b17145d7d17cb784fe11b3fbf65ddf5aa5530f27
ms.sourcegitcommit: 2d6e31648cf61abcb13362ef46a2cfb1326f0423
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/07/2021
ms.locfileid: "7475923"
---
# <a name="integers-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Heltal afrundet forkert, når der beregnes produktkonfigurationsmodeller

## <a name="symptoms"></a>Symptomer

Dette problem kan opstå, når du udfører følgende serie af handlinger:

1. Konfigurer disse attributter på en produktionskonfigurationsmodel:

    - Input (heltal)
    - Procent (decimal)
    - Resultat (heltal)

2. Opret en beregning, der har følgende udtryk:

    *Resultat* = *Input* × *Procent* ÷ 100

I dette tilfælde afrundes heltalsresultatet ikke altid korrekt. Hvis f.eks. inputtet er 1.000, og procenten er 2,40, forventer du, at resultatet af heltallet bliver 24, fordi 2,40 % af 1.000 er 24 (eller 24,00 i decimalform). Resultatet vises i stedet som 23. Men når procentsatsen er 2,39, afrundes beregningen til 24 i stedet for 23. Når procentsatsen er 2,50, afrundes beregningen til 25 som forventet.

## <a name="cause"></a>Årsag

Dette problem opstår på grund af den måde, som Microsoft Solver Foundation repræsenterer tal internt på ved at bruge brøker. I eksemplet ovenfor repræsenteres resultatet af beregningen, hvor procentdelen er 2,40, som 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375. Når .NET bruger denne værdi som et heltal, returnerer den 23.

## <a name="resolution"></a>Løsning

Denne funktionsmåde ændres ikke, fordi andre scenarier afhænger af den. I det foregående eksempel kan du løse problemet ved at indføre en ekstra decimalattribut og en beregning.

Konfigurer f.eks. følgende attributter på en produktionskonfigurationsmodel:

- Input (heltal)
- Procent (decimal)
- ResultDecimal (decimal)
- ResultInteger (heltal)

Du kan derefter tilføje følgende beregninger:

- *ResultDecimal* = *Input* × *Procent* ÷ 100
- *ResultInteger* = *ResultDecimal*
