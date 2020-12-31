---
title: ER-funktionen TEXT
description: Dette emne indeholder oplysninger om, hvordan funktionen TEXT til elektronisk rapportering (ER) skal anvendes.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: d489da24d0589549153913bbc6db699e3c217e72
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682889"
---
# <a name="text-er-function"></a>ER-funktionen TEXT

[!include [banner](../includes/banner.md)]

Funktionen `TEXT` returnerer det angivne tal som en *Streng*-værdi, efter at det er blevet konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard for den aktuelle forekomst.

## <a name="syntax"></a>Syntaks

```vb
TEXT (number)
```

## <a name="arguments"></a>Argumenter

`number`: *Heltal* eller *Reel*

Et tal, der skal konverteres til en tekststreng.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

For værdier af typen *Reel* er strengkonverteringen begrænset til to decimaler.

## <a name="example"></a>Eksempel

Hvis serverens landestandard for Microsoft Dynamics 365 Finance-forekomsten er defineret som **EN-US**, returnerer `TEXT (NOW ())` den aktuelle Finance-sessionsdato, 17. december 2015, som tekststrengen **"17/12/2015 07:59:23"**. `TEXT (1/3)` returnerer **"0,33"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)
