---
title: Liste over ER-funktioner i kategorien dataindsamling
description: Denne artikel indeholder oplysninger om de dataindsamlingsfunktioner, der understøttes i elektronisk rapportering (ER).
author: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: e01bed49646ffe344004f9eb51e9013e1b4c5430
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9286143"
---
# <a name="list-of-er-functions-in-the-data-collection-category"></a>Liste over ER-funktioner i kategorien dataindsamling

[!include [banner](../includes/banner.md)]

Dataindsamlingsfunktionerne til elektronisk rapportering (ER) bruges til at tælle og opsummere i et ER-format, der køres, og som er baseret på data fra det output, der allerede er genereret i formatet **Tekst** eller **XML**. Denne fremgangsmåde bruges til at forbedre ydeevnen i et ER-format, der køres, til at angive værdier for fortløbende totaler i genererede dokumenter og til andre formål. Denne artikel indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion | Beskrivelse |
|----------|-------------|
| [CollectedList](er-functions-datacollection-collectedlist.md) | Denne funktion returnerer en *Postliste*-værdi, der indeholder listen over værdier, der blev returneret af egenskaben **Indsamlet datanøgleværdi** for formatelementer og indsamles, når formateringselementerne blev brugt til at generere et udgående dokument under format kørslen, og som opfylder de angivne betingelser. Hver betingelse består af et nøgleområde og en nøgleværdi. |
| [CountIF](er-functions-datacollection-countif.md) | Denne funktion returnerer en værdi bestående af *Heltal*, som repræsenterer det antal formatelementer, der blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder den angivne betingelse. Betingelsen består af et nøgleområde og en nøgleværdi. |
| [CountIFs](er-functions-datacollection-countifs.md) | Denne funktion returnerer en værdi bestående af *Heltal*, som repræsenterer det antal formatelementer, der blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder de angivne betingelser. Hver betingelse består af et nøgleområde og en nøgleværdi. |
| [FormatElementName](er-functions-datacollection-formatelementname.md) | Denne funktion returnerer en værdi i form af en *Streng*, som repræsenterer navnet på det aktuelle ER-formatelement. |
| [SumIF](er-functions-datacollection-sumif.md) | Denne funktion returnerer en værdi bestående af *Reelle tal*, som repræsenterer summen af de værdier, der blev returneret af formatelementer og blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder den angivne betingelse. Betingelsen består af et nøgleområde og en nøgleværdi. |
| [SumIFs](er-functions-datacollection-sumifs.md) | Denne funktion returnerer en værdi bestående af *Reelle tal*, som repræsenterer summen af de værdier, der blev returneret af formatelementer og blev indsamlet, da formateringselementerne blev brugt til at generere et udgående dokument under kørsel af formatet, og som opfylder de angivne betingelser. Hver betingelse består af et nøgleområde og en nøgleværdi. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
