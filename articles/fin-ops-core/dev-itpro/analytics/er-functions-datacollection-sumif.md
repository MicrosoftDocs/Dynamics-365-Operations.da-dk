---
title: ER-funktionen SUMIF
description: Dette emne indeholder oplysninger om, hvordan funktionen SUMIF til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 04/27/2020
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
ms.openlocfilehash: 174ac28ee2b726ec7fb2ff6d3dda45906c56af65
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3745603"
---
# <a name="sumif-er-function"></a>ER-funktionen SUMIF

[!include [banner](../includes/banner.md)]

Funktionen `SUMIF` returnerer en *Reel* værdi, som repræsenterer summen af de værdier, der blev returneret af formatelementer og blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder den angivne betingelse. Betingelsen består af et nøgleområde og en nøgleværdi.

## <a name="syntax"></a>Syntaks

```vb
SUMIF (key name for summing, condition range, condition value)
```

## <a name="arguments"></a>Argumenter

`key name for summing`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for formatkomponenten til elektronisk rapportering (ER), for hvilken værdien af bindingen skal bruges til opsummerende formål.

Egenskaben **Indsamlet datanøgleværdi** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion returnerer en værdi på **0** (nul), når indstillingen **Detaljer om indsamlingsoutput** for den aktuelle komponent **Fælles\\Fil** er slået fra.

I argumentet `condition range` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.

I argumentet `condition value` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.

## <a name="example"></a>Eksempel

Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.

Yderligere oplysninger og eksempler på brug af denne funktion finder du under [Udskyde udførelse af sekvenselementer i ER-formater](er-defer-sequence-element.md#Example) og [Udskyde udførelse af XML-elementer i ER-formater](er-defer-xml-element.md#Example).

## <a name="additional-resources"></a>Yderligere ressourcer

[Dataindsamlingsfunktioner](er-functions-category-data-collection.md)
