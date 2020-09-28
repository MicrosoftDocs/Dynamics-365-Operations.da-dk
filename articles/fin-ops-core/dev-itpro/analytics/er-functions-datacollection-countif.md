---
title: ER-funktionen COUNTIF
description: Dette emne indeholder oplysninger om, hvordan funktionen COUNTIF til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: cc857a004d988a421c32722b1f69e86b7fefeb36
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743609"
---
# <a name="countif-er-function"></a>ER-funktionen COUNTIF

[!include [banner](../includes/banner.md)]

Funktionen `COUNTIF` returnerer en værdi bestående af *Heltal*, som repræsenterer det antal formatelementer, der blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder den angivne betingelse. Betingelsen består af et nøgleområde og en nøgleværdi.

## <a name="syntax"></a>Syntaks

```vb
COUNTIF (condition range, condition value)
```

## <a name="arguments"></a>Argumenter

`condition range`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i formatet elektronisk rapportering (ER).

`condition value`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format.

## <a name="return-values"></a>Returnerede værdier

*Heltal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Egenskaberne **Indsamlet datanøglenavn** og **Indsamlet datanøgleværdi** kan konfigureres til komponenten **Sekvens** eller til komponenten **XML-element** i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.

Denne funktion returnerer en værdi på **0** (nul), når indstillingen **Detaljer om indsamlingsoutput** for den aktuelle komponent **Fælles\\Fil** er slået fra.

I argumentet `condition range` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.

I argumentet `condition value` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.

## <a name="example"></a>Eksempel

Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dataindsamlingsfunktioner](er-functions-category-data-collection.md)
