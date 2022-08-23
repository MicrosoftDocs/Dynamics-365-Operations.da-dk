---
title: ER-funktionen TRIM
description: Denne artikel indeholder oplysninger om, hvordan funktionen TRIM til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 02/28/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 95b8d2989d705c4998da0af8e683adf567edfe92
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9273092"
---
# <a name="trim-er-function"></a>ER-funktionen TRIM

[!include [banner](../includes/banner.md)]

Funktionen `TRIM` returnerer den angivne tekststreng som en *Streng*-værdi efter tabulator, vognretur, linjeskift og sideskifttegn er blevet erstattet af et enkelt mellemrum, efter at foranstillede og efterfølgende mellemrum er blevet afkortet, og efter at flere mellemrum mellem ord er fjernet.

## <a name="syntax"></a>Syntaks

```vb
TRIM (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige sti til en datakilde af typen *Streng*.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

I visse tilfælde vil du måske afkorte foranstillede og efterfølgende mellemrum, men du foretrækker at formatere den angivne tekst. Hvis f.eks. denne tekst repræsenterer en adresse, der kan angives i tekstboksen med flere linjer og kan indeholde formatering af linjeskift og vognretur. I dette tilfælde skal du bruge følgende udtryk: `REPLACE(text,"^[ \t]+|[ \t]+$","", true)`, hvor `text` er det argument, der henviser til den angivne tekststreng.

## <a name="example-1"></a>Eksempel 1

`TRIM ("`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`")` returnerer **"Eksempeltekst"**.

## <a name="example-2"></a>Eksempel 2

`TRIM (CONCATENATE (CHAR(10), "`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`Sample`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(9),"`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`text`&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;`", CHAR(13)))` returnerer **"Eksempeltekst"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)

[ER-funktionen REPLACE](er-functions-text-replace.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
