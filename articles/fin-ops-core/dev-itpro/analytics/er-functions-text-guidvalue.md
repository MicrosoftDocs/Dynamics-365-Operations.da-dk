---
title: ER-funktionen GUIDVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen GUIDVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a7b8c782aff488a433c40a49ab7f4fe2d0e944e4
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041153"
---
# <a name="GUIDVALUE">ER-funktionen GUIDVALUE</a>

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
