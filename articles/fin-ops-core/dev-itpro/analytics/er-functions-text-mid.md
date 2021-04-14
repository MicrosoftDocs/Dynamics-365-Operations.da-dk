---
title: ER-funktionen MID
description: Dette emne indeholder oplysninger om, hvordan funktionen MID til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/10/2019
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: 9a9ff3f1055f6757d6d4073dbb816773d8bfc8ba
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746261"
---
# <a name="mid-er-function"></a>ER-funktionen MID

[!include [banner](../includes/banner.md)]

Funktionen `MID` returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn fra den angivne streng fra begyndelsen af den angivne position.

## <a name="syntax"></a>Syntaks

```vb
MID (text, starting position, number of characters)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *Streng*-værdi, som angiver den tekst, der skal returneres tegn fra.

`starting position`: *Heltal*

En *Heltals*-værdi, der angiver placeringen af det første tegn, der skal returneres fra den angivne tekst.

`number of characters`: *Heltal*

En *Heltals*-værdi, der angiver antallet af tegn, der skal returneres, som starter ved den angivne start.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Hvis værdien af argumentet `starting position` er mindre end 0 (nul), opgøres antallet af de returnerede tegn fra den første position i den angivne streng.

Hvis værdien af argumentet `starting position` overskrider længden af den angivne streng, returneres en tom streng.

## <a name="example"></a>Eksempel

`MID ("Sample", 2, 3)` returnerer **"amp**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]