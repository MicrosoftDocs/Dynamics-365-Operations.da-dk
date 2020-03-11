---
title: ER-funktionen TRIM
description: Dette emne indeholder oplysninger om, hvordan funktionen TRIM til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: c95663f1aacaf93c1c4bfc8d36d9515f495bf61e
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3040819"
---
# <a name="TRIM">ER-funktionen TRIM</a>

[!include [banner](../includes/banner.md)]

Funktionen `TRIM` returnerer den angivne tekststreng som en *Streng*-værdi, når foranstillede og efterstillede mellemrum er blevet afkortet, og flere mellemrum mellem ord er blevet fjernet.

## <a name="syntax"></a>Syntaks

```vb
TRIM (text )
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige sti til en datakilde af typen *Streng*.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
