---
title: Liste over ER-funktioner i kategorien logisk
description: Dette emne indeholder oplysninger om de logiske funktioner, der understøttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 08/19/2020
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
ms.openlocfilehash: e622778c60646e5cc84cd6e23a5d4954a0fe0bb3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705089"
---
# <a name="list-of-er-functions-in-the-logical-category"></a>Liste over ER-funktioner i kategorien logisk

[!include [banner](../includes/banner.md)]

Logiske funktioner til elektronisk rapportering (ER) kan bruges til at arbejde med logiske værdier for at udføre mere end én sammenligning i et enkelt udtryk eller afprøve flere betingelser. Dette emne indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion | Beskrivelse |
|----------|-------------|
| [Og](er-functions-logical-and.md)                       | Denne funktion returnerer en *Boolesk* værdi som værende **SAND**, hvis alle de angivne betingelser er opfyldte. Ellers returneres en *Boolesk* værdi på **FALSK**. |
| [Sag](er-functions-logical-case.md)                     | Denne funktion evaluerer værdien af det angivne udtryk i forhold til de angivne alternative indstillinger og returnerer resultatet af den første indstilling, der er lig med værdien af det angivne udtryk. Ellers returneres et valgfrit standardresultat, hvis der er angivet et standardresultat som det sidste argument i den kaldte funktion, hvor der ikke er foretaget en forudgående indstilling. Den returnerede værdi kan være en værdi for en hvilken som helst af de understøttede datatyper. |
| [Hvis](er-functions-logical-if.md)                         | Denne funktion returnerer den først angivne værdi, hvis den angivne betingelse er opfyldt. Ellers returneres den anden angivne værdi. Den returnerede værdi kan være en værdi for en hvilken som helst af de understøttede datatyper. |
| [Negeret](er-functions-logical-not.md)                       | Denne funktion returnerer den omvendte logiske værdi af den angivne betingelse som en *Boolesk* værdi. |
| [Eller](er-functions-logical-or.md)                         | Denne funktion returnerer en *Boolesk* værdi som værende **FALSK**, hvis alle de angivne betingelser ikke er opfyldte. Hvis en eller flere af de angivne betingelser er opfyldte, returnerer denne funktion en *Boolesk* værdi som værende **SAND**. |
| [ValueIn](er-functions-logical-valuein.md)               | Denne funktion afgør, hvorvidt det angivne input svarer til en værdi for et angivet element på den angivne liste. Den returnerer en *Boolesk* værdi som værende **SANDT**, hvis det angivne input svarer til resultatet af kørslen med det angivne udtryk for mindst én post på den angivne liste. Ellers returneres en *Boolesk* værdi på **FALSK**. |
| [ValueInLarge](er-functions-logical-valueinlarge.md)     | Denne funktion afgør, om det angivne input af typen *Int64* eller *Heltal* svarer til en værdi for et angivet element på den angivne liste. Den returnerer en *Boolesk* værdi som værende **SANDT**, hvis det angivne input svarer til resultatet af kørslen med det angivne udtryk for mindst én post på den angivne liste. Ellers returneres en *Boolesk* værdi på **FALSK**. |


## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)
