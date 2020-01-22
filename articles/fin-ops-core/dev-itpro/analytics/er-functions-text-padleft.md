---
title: ER-funktionen PADLEFT
description: Dette emne indeholder oplysninger om, hvordan funktionen PADLEFT til elektronisk rapportering (ER) skal anvendes.
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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 28306b2e5fb1febce49ab55240c6d84ff240282a
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916769"
---
# <a name="PADLEFT">ER-funktionen PADLEFT</a>

[!include [banner](../includes/banner.md)]

Funktionen `PADLEFT` returnerer en *Streng*-værdi af den angivne længde, hvor begyndelsen af den angivne streng er udfyldt med de angivne tegn.

## <a name="syntax"></a>Syntaks

```
PADLEFT (text, length, padding chars)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *Streng*-værdi, der repræsenterer den oprindelige tekst.

`length`: *Heltal*

En *Heltals*-værdi, der repræsenterer det endelige antal tegn i den polstrede streng.

`padding chars`: *Streng*

De tegn, som skal bruges til udfyldning.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`PADLEFT ("1234", 10, "`&nbsp;`")` returnerer tekststrengen **"&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;1234"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
