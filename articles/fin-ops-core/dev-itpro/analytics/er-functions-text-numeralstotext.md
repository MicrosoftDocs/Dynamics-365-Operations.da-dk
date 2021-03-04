---
title: ER-funktionen NUMERALSTOTEXT
description: Dette emne indeholder oplysninger om, hvordan funktionen NUMERALSTOTEXT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: e4af3926998d128f8269ab9af46caeb8be896509
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4680212"
---
# <a name="numeralstotext-er-function"></a>ER-funktionen NUMERALSTOTEXT

[!include [banner](../includes/banner.md)]

Funktionen `NUMERALSTOTEXT` returnerer det angivne tal som en *Streng*-værdi, efter at det er blevet skrevet helt ud (det vil være konverteret til tekststrenge) på det angivne sprog.

## <a name="syntax"></a>Syntaks

```vb
NUMERALSTOTEXT (number, language, currency, print currency name flag, decimal points)
```

## <a name="arguments"></a>Argumenter

`number`: *Heltal* eller *Reel*

En numerisk værdi, der angiver det tal, der skal skrives helt ud.

`language`: *Streng*

En *Streng*-værdi, der repræsenterer sprogkoden.

`currency`: *Streng*

En *Streng*-værdi, der repræsenterer valutakoden.

`print currency name flag`: *Boolesk*

En *Boolesk* værdi, der angiver, om der skal føjes et valutanavn til den tekst, der skrives helt ud.

`decimal points`: *Heltal*

En *Heltals*-værdi, der angiver det antal decimaler, som den tekst, der er skrevet helt ud, skal have.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Sprogkoden er valgfri. Hvis den er defineret som en tom streng, bruges sprogkoden for kørselskonteksten. Standardsprogkoden er **EN-US**. Sprogkoden for den kørende kontekst er defineret i et **Mappe**- eller **Fil**-element i det elektroniske rapporteringsformat (ER), der kører.

Valutakoden er valgfri. Hvis den er defineret som en tom streng, bruges firmavalutaen for kørselskonteksten.

> [!NOTE] 
> Argumenterne `print currency name flag` og `decimal points` analyseres kun for følgende sprogkoder: **CS**, **ET**, **HU**, **LT**, **LV**, **PL**, and **RU**. Desuden analyseres argumentet `print currency name flag` kun for virksomheder, hvor landets eller områdets kontekst understøtter afvigelse af valutanavne.

## <a name="example-1"></a>Eksempel 1

`NUMERALSTOTEXT (1234.56, "EN-US", "", false, 2)` returnerer **"Ettusindtohundredeogfireogtredive samt 56"**.

## <a name="example-2"></a>Eksempel 2

`NUMERALSTOTEXT (120, "PL", "", false, 0)` returnerer **"Sto dwadzieścia"**. 

## <a name="example-3"></a>Eksempel 3

`NUMERALSTOTEXT (120.21, "RU", "EUR", true, 2)` returnerer **"сто двадцать евро 21 евроцент"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]