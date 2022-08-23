---
title: Liste over ER-funktioner i kategorien Dato og klokkeslæt
description: Denne artikel indeholder oplysninger om funktionerne dato og klokkeslæt, der understøttes i elektronisk rapportering (ER).
author: kfend
ms.date: 09/09/2021
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
ms.openlocfilehash: d77f41e10d927a9aae06b9ba0fc58ca237c071cd
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9291318"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Liste over ER-funktioner i kategorien Dato og klokkeslæt

[!include [banner](../includes/banner.md)]

Funktionerne dato og klokkeslæt for elektronisk rapportering (ER) kan bruges til at udtrække oplysninger fra dato- og klokkeslætsværdier og til at udføre handlinger på dem. Denne artikel indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion | Beskrivelse |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Denne funktion returnerer en *[Dato/klokkeslæt](er-formula-supported-data-types-primitive.md#datetime)*-værdi, der er det angivne antal dage før eller efter en angivet startdato. |
| [ChangeTimeZone](er-functions-datetime-changetimezone.md) | Denne funktion returnerer en værdi i form af *Dato/klokkeslæt*, som konverteres fra en given dato-/klokkeslætsværdi i én tidszone til dato-/klokkeslætsværdi i en anden tidszone. |
| [DateFormat](er-functions-datetime-dateformat.md) | Denne funktion returnerer en værdi i form af en *[Streng](er-formula-supported-data-types-primitive.md#string)*, som præsenterer en given datoværdi som tekst i det angivne format og i en eventuelt angivet kultur. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Denne funktion returnerer en værdi i form af en *Streng*, som præsenterer en given dato-/klokkeslætsværdi som tekst i det angivne format og i en eventuelt angivet kultur. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet kultur til en dato-/klokkeslætsværdi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som konverteres fra en given dato-/klokkeslætsværdi i UTC-tid (Coordinated Universal Time) (Greenwich Mean \[time\]GMT). |
| [DateValue](er-functions-datetime-datevalue.md) | Denne funktion returnerer en værdi i form af en *[Dato](er-formula-supported-data-types-primitive.md#date)*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet kultur til en datoværdi. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Denne funktion returnerer en værdi i form af et *[Heltal](er-formula-supported-data-types-primitive.md#integer)*, som repræsenterer antallet af dage mellem 1. januar og den angivne dato. |
| [Dage](er-functions-datetime-days.md) | Denne funktion returnerer en værdi i form af et *Heltal*, som repræsenterer antallet af dage mellem to angivne datoer. |
| [Now](er-functions-datetime-now.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer den aktuelle dato og klokkeslæt for den aktuelle programserver. |
| [NullDate](er-functions-datetime-nulldate.md) | Denne funktion returnerer en værdi i form af en *Dato*, som repræsenterer datoen **nul** (1. januar 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer dato-/klokkeslætsværdien **nul** (1. januar 1900) i UTC-tid (Coordinated Universal Time). |
| [SessionNow](er-functions-datetime-sessionnow.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer dato og klokkeslæt for den aktuelle programsession. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Denne funktion returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programsession. |
| [I dag](er-functions-datetime-today.md) | Denne funktion returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programserver. |
| [WeekNum](er-functions-datetime-weeknum.md) | Denne funktion returnerer værdien *Heltal*, der repræsenterer ugen i året. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
