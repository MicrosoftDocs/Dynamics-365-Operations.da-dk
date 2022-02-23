---
title: ER-funktionen FORMATELEMENTNAME
description: Dette emne indeholder oplysninger om, hvordan funktionen FORMATELEMENTNAME til elektronisk rapportering (ER) skal anvendes.
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
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: ef59bb44a7096f4c095ce37a89558a717748f02e
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4685321"
---
# <a name="formatelementname-er-function"></a>ER-funktionen FORMATELEMENTNAME

[!include [banner](../includes/banner.md)]

Funktionen `FORMATELEMENTNAME` returnerer en *Streng*-værdi, som repræsenterer navnet på det aktuelle element for elektronisk rapporteringsformat (ER).

## <a name="syntax"></a>Syntaks

```vb
FORMATELEMENTNAME ()
```

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion kan kaldes i ER-udtryk, som blev konfigureret for egenskaberne **Indsamlet datanøglenavn** og **Indsamlet datanøgleværdi** til en ER-formatkomponent fra gruppen **Tekst**, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.

## <a name="example"></a>Eksempel

Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dataindsamlingsfunktioner](er-functions-category-data-collection.md)
