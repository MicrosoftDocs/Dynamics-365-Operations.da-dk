---
title: ER-funktionen COLLECTEDLIST
description: Dette emne indeholder oplysninger om, hvordan funktionen COLLECTEDLIST til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: d02f9ac4697a4d65417e522bffb5f40ebfdc237a
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681226"
---
# <a name="collectedlist-er-function"></a>ER-funktionen COLLECTEDLIST

[!include [banner](../includes/banner.md)]

Funktionen `COLLECTEDLIST` returnerer en *Postliste*-værdi, der indeholder listen over værdier, der blev returneret af egenskaben **Indsamlet datanøgleværdi** for formatelementer og indsamles, når formateringselementerne blev brugt til at generere udgående dokumenter under format kørslen, og som opfylder de angivne betingelser. Hver betingelse består af et nøgleområde og en nøgleværdi.

## <a name="syntax"></a>Syntaks

```vb
COLLECTEDLIST (condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Argumenter

`condition 1 range`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i formatet elektronisk rapportering (ER). Dette argument skal udfyldes.

`condition 1 value`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format. Dette argument skal udfyldes.

`condition N range`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i et ER-format. Disse yderligere argumenter er valgfrie.

`condition N value`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format. Disse yderligere argumenter er valgfrie.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Egenskaberne **Indsamlet datanøglenavn** og **Indsamlet datanøgleværdi** kan konfigureres til komponenten **Sekvens** eller til komponenten **XML-element** i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.

Denne funktion returnerer en tom liste, når indstillingen **Detaljer om indsamlingsoutput** for komponenten **Fælles\\Fil** er slået fra.

I `condition range` argumenter kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.

I `condition value` argumenter kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.

## <a name="example"></a>Eksempel

Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dataindsamlingsfunktioner](er-functions-category-data-collection.md)
