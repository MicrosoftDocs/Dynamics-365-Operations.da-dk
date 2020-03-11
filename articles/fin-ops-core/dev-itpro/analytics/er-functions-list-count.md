---
title: ER-funktionen COUNT
description: Dette emne indeholder oplysninger om, hvordan funktionen COUNT til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: 72d2ea1b26c295c97575a3c7a479ee4e06762424
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042199"
---
# <a name="COUNT">ER-funktionen COUNT</a>

[!include [banner](../includes/banner.md)]

Funktionen `COUNT` returnerer en *Heltals*-værdi, der repræsenterer antallet af poster på den angivne liste, hvis listen ikke er tom. Hvis listen er tom, returnerer denne funktion **0** (nul).

## <a name="syntax"></a>Syntaks

```vb
COUNT (list)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

## <a name="return-values"></a>Returnerede værdier

*Heltal*

Den resulterende numeriske værdi.

## <a name="example"></a>Eksempel

`COUNT (SPLIT("abcd" , 3))` returnerer **2**, fordi den `SPLIT`-funktion, der bruges i dette eksempel, opretter en liste, der består af to poster.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)
