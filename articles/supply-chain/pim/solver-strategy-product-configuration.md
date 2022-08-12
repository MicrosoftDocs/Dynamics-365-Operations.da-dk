---
title: Strategi for problemløser for produktkonfiguration
description: Denne artikel beskriver, hvordan du kan bruge strategien for problemløser til at forbedre ydeevnen for produktkonfiguration.
author: t-benebo
ms.date: 02/19/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: PCCreateProductConfigurationModel, PCProductConfigurationModelListPage
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: ''
ms.author: benebotg
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 9b0b53da17bd106be60966d856d29d81a1e57f91
ms.sourcegitcommit: 28a726b3b0726ecac7620b5736f5457bc75a5f84
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/29/2022
ms.locfileid: "9065511"
---
# <a name="solver-strategy-for-product-configuration"></a>Strategi for problemløser for produktkonfiguration

[!include [banner](../includes/banner.md)]

Denne artikel beskriver, hvordan du kan bruge strategien for problemløser til at forbedre ydeevnen for produktkonfiguration.

Begrebet strategi for problemløser blev først introduceret i Samlet opdatering 7 (CU7) til Microsoft Dynamics AX 2012 R2. Det blev udvidet i Samlet opdatering 8 (CU8) til Microsoft Dynamics AX 2012 R3 og programmer til finans og drift, Enterprise Edition 7.3.

Konceptet for strategi for problemløser består nu af følgende strategier:

- Standard
- Først minimale domæner
- Oppefra og ned
- Z3

## <a name="solver-strategy"></a>Strategi for problemløser 

En model til produktkonfiguration kan formuleres som et [begrænsningsbaseret problem (CSP)](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf). Microsoft Solver Foundation (MSF) indeholder to typer strategier for problemløser til at løse CSP'er, der kan bruges fra produktkonfigurationsmodeller. Disse strategier for problemløser er afhængige af [heuristik](https://techterms.com/definition/heuristic), som bruges til at bestemme den rækkefølge, som variablerne i CSP'erne anvendes i, når problemet beregnes. Heuristik kan påvirke ydeevnen betydeligt, når et problem eller en klasse af problemer beregnes.

Strategien for problemløser til produktkonfigurationsmodeller bestemmer, hvilken problemløser der bruges sammen med heuristik. Strategierne **Standard**, **Først minimale domæner**, og **Oppefra og ned** bruger de to problemløsere fra MSF, mens strategien **Z3** bruger Z3-problemløseren. 

Undersøgelse af virkelige kundeimplementeringer har vist, at en ændring i strategien for problemløser for en model til produktkonfiguration kan reducere svartiden fra minutter til millisekunder. Derfor er det indsatsen værd at prøve forskellige strategier for problemløser for at finde den mest effektive strategi for din model til produktkonfiguration.

## <a name="change-the-settings-for-the-solver-strategy"></a>Ændre indstillingerne for strategien for problemløser

Hvis du vil ændre strategien for problemløseren skal du vælge **Modelegenskaber** på siden **Produktkonfigurationsmodeller** under ruden Handling. Vælg derefter en strategi for problemløser i dialogboksen **Rediger detaljerne om modellen**.

[![Ændring af strategien for problemløser.](./media/solver-strategy.png)](./media/solver-strategy.png)

Der er i øjeblikket ingen logik, der automatisk registrerer, hvilken strategi for problemløseren der vil være den mest effektive strategi for begrænsningsbaseret produktkonfiguration. Derfor skal du prøve strategierne for problemløser én ad gangen.

Følgende tabel indeholder anbefalinger om, hvilken strategi for problemløser, der skal bruges i forskellige scenarier.

| Strategi for problemløser      | Du kan bruge strategien i dette scenario |
|----------------------|-----------------------------------|
| Standard              | Strategien **Standard** er blevet optimeret for at løse modeller, der er baseret på tabelbegrænsninger. Undersøgelser af kundeimplementeringer har vist, at denne strategi er den mest effektive strategi i scenarier, hvor brugen af tabelbegrænsninger er udbredt. |
| Først minimale domæner | Strategierne **Først minimale domæner** og **Oppefra og ned** er tæt forbundne. Undersøgelser af kundeimplementeringer har vist, at strategien **Oppefra og ned** overgår strategien **Først minimale domæner**. Men strategien **Først minimale domæner** bevares af hensyn til bagudkompatibilitet. Begge disse strategier for problemløser har vist at være mere effektive til løsning af modeller, der indeholder flere matematiske udtryk, hvor der ikke bruges tabelbegrænsninger. Men i nogle tilfælde strategien **Standard** overgå disse to strategier. Du skal derfor huske at prøve hver strategi. |
| Oppefra og ned             | Strategierne **Først minimale domæner** og **Oppefra og ned** er tæt forbundne. Undersøgelser af kundeimplementeringer har vist, at strategien **Oppefra og ned** overgår strategien **Først minimale domæner**. Men strategien **Først minimale domæner** bevares af hensyn til bagudkompatibilitet. Begge disse strategier for problemløser har vist at være mere effektive til løsning af modeller, der indeholder flere matematiske udtryk, hvor der ikke bruges tabelbegrænsninger. Men i nogle tilfælde strategien **Standard** overgå disse to strategier. Du skal derfor huske at prøve hver strategi. |
| Z3                   | Det anbefales, at du strategien **Z3**, som standardstrategien for problemløser. Hvis du er bekymret for ydeevne og skalerbarhed, kan du evaluere de andre strategier. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over produktkonfiguration](build-product-configuration-model.md)

[Heuristik](https://techterms.com/definition/heuristic)

[Begrænsningsbaseret problem](http://aima.cs.berkeley.edu/2nd-ed/newchap05.pdf)


[!INCLUDE[footer-include](../../includes/footer-banner.md)]
