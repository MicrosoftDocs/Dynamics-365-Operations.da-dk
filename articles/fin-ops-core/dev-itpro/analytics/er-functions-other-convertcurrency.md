---
title: ER-funktionen CONVERTCURRENCY
description: Dette emne indeholder oplysninger om, hvordan funktionen CONVERTCURRENCY til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ae6e0069c6e9227d4cf1045eeebbb825a2f943c3
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3744305"
---
# <a name="convertcurrency-er-function"></a>ER-funktionen CONVERTCURRENCY

[!include [banner](../includes/banner.md)]

Funktionen `CONVERTCURRENCY` returnerer en *Reel* værdi, som repræsenterer resultatet af konverteringen af det angivne pengebeløb fra den angivne kildevaluta til den angivne målvaluta ved hjælp af indstillingerne for det angivne firma på den angivne dato.

## <a name="syntax"></a>Syntaks

```vb
CONVERTCURRENCY (amount, source currency, target currency, date, company)
```

## <a name="arguments"></a>Argumenter

`amount`: *Heltal* eller *Reel*

En numerisk værdi, der repræsenterer det pengebeløb, der skal konverteres.

`source currency`: *Streng*

Koden for kildevalutaen

`target currency`: *Streng*

Koden for målvalutaen

`date`: *Dato*

En *Dato*-værdi, der repræsenterer den dato, der bruges til at bestemme valutakursen for konverteringen.

`company`: *Streng*

En *Streng*-værdi, der repræsenterer koden for et firma, der leverer de indstillinger, der bruges til konverteringen.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="example"></a>Eksempel

`CONVERTCURRENCY (1, "EUR", "USD", TODAY(), "DEMF")` returnerer hvad der svarer til én euro i amerikanske dollar på den aktuelle sessionsdato, baseret på indstillingerne for **DEMF**-firmaet.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)
