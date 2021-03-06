---
title: ER-funktionen JSONVALUE
description: Dette emne indeholder oplysninger om, hvordan funktionen JSONVALUE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/11/2019
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
ms.openlocfilehash: e8336e43a236e3f3b875fb3cb81bc139507673c2
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5746357"
---
# <a name="jsonvalue-er-function"></a>ER-funktionen JSONVALUE

[!include [banner](../includes/banner.md)]

Funktionen `JSONVALUE` opdeler data i JavaScript Object Notation (JSON)-format, som tilgås via den angivne sti og udtrækker en skalarværdi, der indeholder det angivne ID. Derefter returneres den udpakkede skalarværdi som en *Streng*-værdi.

## <a name="syntax"></a>Syntaks

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige sti til en datakilde af typen *Streng*, som indeholder JSON-data.

`path`: *Streng*

Identifikatoren for en skalarværdi af JSON-data.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

Datakilden **$JsonField** indeholder følgende data i JSON-format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. I dette tilfælde returnerer `JSONVALUE (JsonField, "BuildNumber")`-udtrykket følgende værdi af datatypen *Streng*: **"7.3.1234.1"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]