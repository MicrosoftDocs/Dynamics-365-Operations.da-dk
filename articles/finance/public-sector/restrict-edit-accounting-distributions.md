---
title: Begrænse redigeringen af regnskabsfordelinger på fakturaer
description: Denne artikel forklarer, hvordan du kan kræve, at de økonomiske dimensioner i en indkøbsordre svarer til dimensionerne på den tilsvarende kreditorfaktura.
author: v-kiarnd
ms.date: 10/14/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: twheeloc
ms.search.region: Global
ms.search.industry: public sector
ms.author: v-kiarnd
ms.search.validFrom: 2020-10-15
ms.dyn365.ops.version: 10.0.15
ms.openlocfilehash: 7d5e9138dbf92435f9b3a62721ab4d3761b74e5a
ms.sourcegitcommit: 427fe14824a9d937661ae21b9e9574be2bc9360b
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/09/2022
ms.locfileid: "8946130"
---
# <a name="restrict-editing-of-accounting-distributions-on-invoices"></a>Begrænse redigeringen af regnskabsfordelinger på fakturaer

[!include[banner](../includes/banner.md)]

Denne artikel forklarer, hvordan du kan kræve, at de økonomiske dimensioner i en indkøbsordre svarer til dimensionerne på den tilsvarende kreditorfaktura. Du kan konfigurere bestemte økonomiske dimensioner, der skal være ens mellem en indkøbsordre og en faktura, der oprettes ud fra den. Du kan f.eks. kræve, at alle økonomiske dimensioner stemmer overens mellem indkøbsordrer og fakturaer. På fakturaer, der er tilknyttet en indkøbsordre, kan du ikke ændre finanskontiene på fakturaens detaljelinjer, så de afviger fra de konti, der er angivet på indkøbsordrelinjerne.

## <a name="set-up-locked-financial-dimensions"></a>Konfigurere låste økonomiske dimensioner

Benyt følgende fremgangsmåde for at definere de økonomiske dimensioner, der skal være ens mellem en indkøbsordre og relaterede fakturaer.

1. Gå til **Kreditor \> Opsætning \> Kreditorparametre**.
2. På siden **Kreditorparametre** skal du vælge **Validering af indkøbsordre-/fakturasammenholdelse**.
3. Markér afkrydsningsfeltet **Påkrævet sammenholdelse** for de dimensioner, der skal være ens. Alle de økonomiske dimensioner, der er konfigureret på siden **Økonomiske dimensioner**, kan vælges.
4. Vælg **Luk**.

## <a name="work-with-locked-financial-dimensions-on-an-invoice"></a>Arbejde med låste økonomiske dimensioner på en faktura

Når du opretter en kreditorfaktura ud fra en indkøbsordre, kan du ikke redigere de låste økonomiske dimensioner. Hvis du forsøger at redigere en låst økonomisk dimension, modtager du en fejlmeddelelse, og hele den økonomiske dimensionsstreng går tilbage til den oprindelige streng.

Du kan se økonomiske dimensioner for fakturaen.

1. Gå til **Kreditor \> Generelt \> Kreditorfakturaer \> Ventende kreditorfakturaer**.
2. Åbn fakturaen.
3. På siden **Kreditorfaktura** skal du i oversigtspanelet **Linjer** vælge **Finans \> Fordel beløb**.

> [!NOTE]
> Økonomiske dimensioner er ikke låst på linjer, der manuelt føjes til en faktura og ikke er baseret på indkøbsordrer. I dette tilfælde kan du ændre de økonomiske dimensioner på fakturaen efter behov, indtil fakturaen er bogført.
