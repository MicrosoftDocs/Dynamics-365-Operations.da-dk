---
title: ER-funktionen SUMIFS
description: Dette emne indeholder oplysninger om, hvordan funktionen SUMIFS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 6820be1976e722f7b108b3e9303c8ed4d822ae9b
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2917597"
---
# <a name="SUMIFS">ER-funktionen SUMIFS</a>

[!include [banner](../includes/banner.md)]

Funktionen `SUMIFS` returnerer en *Reel* værdi, som repræsenterer summen af de værdier, der blev returneret af formatelementer og blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder de angivne betingelser. Hver betingelse består af et nøgleområde og en nøgleværdi.

## <a name="syntax"></a>Syntaks

```
SUMIFS (key name for summing, condition 1 range, condition 1 value[, condition 2 range, condition 2 value, …, condition N range, condition N value])
```

## <a name="arguments"></a>Argumenter

`key name for summing`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for formatkomponenten til elektronisk rapportering (ER), for hvilken værdien af bindingen skal bruges til opsummerende formål.

Egenskaben **Indsamlet datanøglenavn** kan konfigureres til enten en **Numerisk** komponent eller en **Streng**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.

`condition 1 range`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i et ER-format. Dette argument skal udfyldes.

Egenskaben **Indsamlet datanøglenavn** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.

`condition 1 value`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format. Dette argument skal udfyldes.

Egenskaben **Indsamlet datanøgleværdi** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.

`condition N range`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøglenavn** for en komponent i et ER-format. Disse yderligere argumenter er valgfrie.

Egenskaben **Indsamlet datanøglenavn** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.

`condition N value`: *Streng*

En værdi, der returneres af det udtryk, der er konfigureret i egenskaben **Indsamlet datanøgleværdi** for en komponent i et ER-format. Disse yderligere argumenter er valgfrie.

Egenskaben **Indsamlet datanøgleværdi** kan konfigureres til enten en **Sekvens**-komponent eller en **XML-element**-komponent i et ER-format, der er placeret under komponenten **Fælles\\Fil**, såfremt indstillingen **Detaljer om indsamlingsoutput** er aktiveret.

## <a name="return-values"></a>Returnerede værdier

*Kommatal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion returnerer en værdi på **0** (nul), når indstillingen **Detaljer om indsamlingsoutput** for den aktuelle komponent **Fælles\\Fil** er slået fra.

I argumenterne `condition range` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.

I argumenterne `condition value` kan jokertegnet **"\*"** bruges til at repræsentere flere tegn.

## <a name="example"></a>Eksempel

Du kan få flere oplysninger om brugen af denne funktion i opgaveguiden [Brug ER-data af formatoutput til optælling og sammenlægning](tasks/er-format-counting-summing-1.md) en del af forretningsprocessen **Anskaffe/udarbejde komponenter til it-servicer og -løsninger** til at lære mere om brugen af disse funktioner.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dataindsamlingsfunktioner](er-functions-category-data-collection.md)
