---
title: ER-funktionen COLLECTEDLIST
description: Denne artikel indeholder oplysninger om, hvordan funktionen COLLECTEDLIST til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/05/2019
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
ms.openlocfilehash: 5102035cf2a8667222beb7bc42ae9aec1b311790
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9280888"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
