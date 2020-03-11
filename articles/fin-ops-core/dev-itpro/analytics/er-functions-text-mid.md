---
title: ER-funktionen MID
description: Dette emne indeholder oplysninger om, hvordan funktionen MID til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 6fbaf5952222d90a855956fb93713e0f9ef81305
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041020"
---
# <a name="MID">ER-funktionen MID</a>

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
