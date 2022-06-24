---
title: ER-funktionen GUIDVALUE
description: Denne artikel indeholder oplysninger om, hvordan funktionen GUIDVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f3899d983f7c790ff2e3dc74dd91c44fc54e44d3
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8898734"
---
# <a name="guidvalue-er-function"></a>ER-funktionen GUIDVALUE

[!include [banner](../includes/banner.md)]

Funktionen `GUIDVALUE` konverterer det angivne input af typen *Streng* til et dataelement af typen *GUID*.

## <a name="syntax"></a>Syntaks

```vb
GUIDVALUE (input)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige sti til en datakilde af typen *Streng*.

## <a name="return-values"></a>Returnerede værdier

*GUID*

Den resulterende GUID-værdi (globalt entydigt identifikator).

## <a name="usage-notes"></a>Bemærkninger til brug

For at omregne i modsat retning (dvs. konvertering til et angivet input af datatypen *GUID* til et dataelement af datatypen *Streng*) kan du bruge funktionen [TEXT](er-functions-text-text.md).

## <a name="example"></a>Eksempel

Du definerer følgende datakilder i din modeltilknytning:

- En **mitID**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `GUIDVALUE ("AF5CCDAC-F728-4609-8C8B- A4B30B0C0AA0")`
- En **Brugere**-datakilde af typen *Tabelposter*, som refererer til tabellen BrugerInfo

Du kan derefter bruge et udtryk såsom `FILTER (Users, Users.objectId = myID)` til at filtrere tabellen BrugeInfo efter feltet **ObjektID** af datatypen *GUID*.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]