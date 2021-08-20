---
title: Foretage fejlfinding af variantstyring
description: Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med variantstyring.
author: SmithaNataraj
ms.date: 11/04/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: smnatara
ms.search.validFrom: 2020-11-04
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: f09ca4e69ca4bd3e87ee425c483b7a338045a0f28312a92b154fa07eb125927a
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6772490"
---
# <a name="troubleshoot-the-product-configurator"></a>Foretage fejlfinding af variantstyring

Dette emne beskriver, hvordan du løser problemer, der kan opstå, når du arbejder med variantstyringen.

## <a name="item-text-is-overwritten-when-i-configure-a-product-on-a-sales-order-line"></a>Varetekst overskrives, når jeg konfigurerer et produkt på en salgsordrelinje.

### <a name="issue-description"></a>Problembeskrivelse

Dette problem opstår, når du opretter en salgsordrelinje for en vare, der kan konfigureres, og derefter redigere vareteksten. Når du konfigurerer varen og derefter vælger **OK**, overskrives teksten med standardteksten.

### <a name="issue-resolution"></a>Problemløsning

Denne funktionsmåde forventes. Tekstfeltet indeholder variantnavnet, som kun er udfyldt, når du har konfigureret linjen. Derfor skal du ændre teksten, efter at du har konfigureret linjen, og ikke før.

## <a name="integer-attributes-are-incorrectly-rounded-when-product-configuration-models-are-calculated"></a>Heltalsattributter afrundes forkert, når produktkonfigurationsmodeller beregnes.

### <a name="issue-description"></a>Problembeskrivelse

Dette problem kan opstå, når du udfører følgende serie af handlinger:

1. Konfigurer følgende attributter på en produktionskonfigurationsmodel:

    - Input (heltal)
    - Procent (decimal)
    - Resultat (heltal)

2. Opret en beregning, der har følgende udtryk:

    *Resultat* = *Input* × *Procent* ÷ 100

I dette tilfælde afrundes heltalsresultatet ikke altid korrekt. Input er f.eks. 1.000, og procentsatsen er 2,40. Derfor forventer du, at heltalsresultatet er 24, fordi 2,40 procent af 1.000 er 24 (eller 24,00 i decimalform). Resultatet vises i stedet som 23. Men når procentsatsen er 2,39, afrundes beregningen til 24 i stedet for 23. Når procentsatsen er 2,50, afrundes beregningen til 25 som forventet.

### <a name="issue-resolution"></a>Problemløsning

Dette problem opstår på grund af den måde, som Microsoft Solver Foundation repræsenterer tal internt på ved at bruge brøker. I eksemplet ovenfor repræsenteres resultatet af beregningen, hvor procentdelen er 2,40, som 27021597764222975 ÷ 1125899906842624 = 23,99999999999999911182158029987476766109466552734375. Når .NET bruger denne værdi som et heltal, returnerer den 23.

Denne funktionsmåde ændres ikke, fordi andre scenarier afhænger af den. I det foregående eksempel kan du løse problemet ved at indføre en ekstra decimalattribut og en beregning.

Konfigurer f.eks. følgende attributter på en produktionskonfigurationsmodel:

- Input (heltal)
- Procent (decimal)
- ResultDecimal (decimal)
- ResultInteger (heltal)

Du kan derefter tilføje følgende beregninger:

- *ResultDecimal* = *Input* × *Procent* ÷ 100
- *ResultInteger* = *ResultDecimal*


[!INCLUDE[footer-include](../../includes/footer-banner.md)]