---
title: Almindelige kilder til produktionsafvigelser
description: I denne artikel beskrives forskellige kilder, der er typiske for de enkelte typer afvigelser i produktion.
author: JennySong-SH
ms.date: 06/20/2017
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: InventCostTrans, ProdCalcVarianceTrans
audience: Application User
ms.reviewer: kamaybac
ms.custom: 79753
ms.assetid: 14ac7db4-fb40-43c1-bb0d-1d51fc91d24f
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: yanansong
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 8b0f7a66c00540216887c7913e7f094c819b693a
ms.sourcegitcommit: 9166e531ae5773f5bc3bd02501b67331cf216da4
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/03/2022
ms.locfileid: "8673992"
---
# <a name="common-sources-of-production-variances"></a>Almindelige kilder til produktionsafvigelser

[!include [banner](../includes/banner.md)]

I denne artikel beskrives forskellige kilder, der er typiske for de enkelte typer afvigelser i produktion. 

Her er nogle typiske kilder til en afvigelse i **partistørrelse**:

-   Antallet af gode varer for en produktionsordre er forskelligt fra den beregningsmængde, der bruges i standardomkostningsberegningen. Antallet danner grundlag for amortisering af omkostninger.
-   Værdien af konstante omkostninger i produktionsordren er forskellig fra de konstante omkostninger, der bruges til beregning af standardomkostningerne. De konstante omkostninger i produktionsordren kan være forskellige af flere årsager. For eksempel kan de konstante omkostninger afspejle følgende faktorer:
    -   Manuelle ændringer af produktionsstyklisten eller ruten
    -   Valget af en anden styklisteversion eller ruteversion ved oprettelse af produktionsordren
    -   Planlagte engineering-ændringer i styklisteversionen eller ruteversionen, der er tildelt varen

Her er nogle typiske kilder til en afvigelse i **produktionspris**:

-   Omkostningsarten (og prisen for omkostningsarten) for det rapporterede forbrug af en ruteoperation er forskellig fra den omkostningsart, der bruges i standardomkostningsberegningen.
-   Den aktive omkostning for prisen for omkostningsarten er forskellig fra den pris for omkostningsarten, der bruges i standardomkostningsberegningen.

Her er nogle typiske kilder til en afvigelse i **produktionsantal**:

-   For stor afgang eller for lille afgang af en materialekomponent.
-   For lang eller for kort rapporteret tid for en ruteoperation.
-   Du modtager for stort eller lille antal af den overordnede vare i forhold til ordreantallet. Men du udsteder komponenter og rapportoperationer helt, baseret på ordreantallet for produktionsordren.

Her er nogle typiske kilder til en afvigelse i **produktionserstatning**:

-   Afgang af en materialekomponent, der ikke er del af produktionsstyklisten.
-   Manuel tilføjelse af en komponent på produktionsstyklisten og rapportering af komponenten som Forbrugt.
-   Rapportering af en vare som forbrugt uden, at den manuelt føjes til produktionsstyklisten.
-   Manuel tilføjelse af en operation til produktionsruten og rapportering af operationen som Forbrugt.
-   Valg af en anden styklisteversion ved oprettelse af produktionsordren, eller hvis styklisteversionen er forskellig fra den, der bruges i standardomkostningsberegningen.
-   Valg af en anden ruteversion ved oprettelse af produktionsordren, eller hvis ruteversionen er forskellig fra den, der bruges i standardomkostningsberegningen.






[!INCLUDE[footer-include](../../includes/footer-banner.md)]