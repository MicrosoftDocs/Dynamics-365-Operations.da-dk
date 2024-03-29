---
title: ER-funktionen REPLACE
description: Denne artikel indeholder oplysninger om, hvordan funktionen REPLACE til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: e7a27b5015615d9b0f26e8fcddd812b3f51fb945
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9278465"
---
# <a name="replace-er-function"></a>ER-funktionen REPLACE

[!include [banner](../includes/banner.md)]

Funktionen `REPLACE` returnerer den angivne tekststreng som en *Streng*-værdi, efter at hele eller en del af den er blevet erstattet med en anden streng.

## <a name="syntax"></a>Syntaks

```vb
REPLACE (text, pattern, replacement, regular expression flag)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

Den gyldige sti til en datakilde af typen *Streng*.

`pattern`: *Streng*

Hvis argumentet `regular expression flag` er **FALSK**, indeholder argumentet den tekst, der skal udskiftes.

Hvis argumentet `regular expression flag` er **SANDT**, indeholder dette argument et regulært udtryk, der definerer både et søgemønster og erstatningsteksten.

`replacement`: *Streng*

Hvis argumentet `regular expression flag` er **FALSK**, indeholder argumentet den tekst, der anvendes i stedet for.

Hvis argumentet `regular expression flag` er **SANDT**, bruges dette argument ikke.

`regular expression flag`: *Boolesk*

En *Boolesk* værdi, der angiver, om et regulært udtryk bruges til at udføre erstatningen.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Hvis argumentet `regular expression flag` er **SANDT**, returnerer denne funktion den angivne streng, når den er blevet ændret, ved at anvende det regulære udtryk, der er angivet af argumentet `pattern`. Dette regulære udtryk bruges til at søge efter de tegn, der skal erstattes.

Hvis argumentet `regular expression flag`er **FALSE**, returnerer denne funktion den angivne streng, efter at det sæt tegn, der er defineret i argumentet `pattern`, er erstattet af tegn i argumentet `replacement`. 

## <a name="example-1"></a>Eksempel 1

`REPLACE ("+1 923 456 4971", "[^0-9]", "", true)` anvender et almindeligt udtryk, der fjerner alle ikke-numeriske symboler og returnerer **"19234564971"**. 

## <a name="example-2"></a>Eksempel 2

`REPLACE ("abcdef", "cd", "GH", false)` erstatter mønsteret **"cd"** med strengen **"GH"** og returnerer **"abGHef"**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
