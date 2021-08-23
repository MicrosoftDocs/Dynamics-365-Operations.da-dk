---
title: Liste over ER-funktioner i kategorien Dato og klokkeslæt
description: Dette emne indeholder oplysninger om funktionerne dato og klokkeslæt, der understøttes i elektronisk rapportering (ER).
author: NickSelin
ms.date: 12/05/2019
ms.prod: ''
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
ms.openlocfilehash: 5f0f421afcaf720366c76c2728721598540a37f0b627123b3386a3174c039a96
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6760044"
---
# <a name="list-of-er-functions-in-the-date-and-time-category"></a>Liste over ER-funktioner i kategorien Dato og klokkeslæt

[!include [banner](../includes/banner.md)]

Funktionerne dato og klokkeslæt for elektronisk rapportering (ER) kan bruges til at udtrække oplysninger fra dato- og klokkeslætsværdier og til at udføre handlinger på dem. Dette emne indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion | Beskrivelse |
|----------|-------------|
| [AddDays](er-functions-datetime-adddays.md) | Denne funktion returnerer en værdi med *DatoKlokkeslæt*, der er det angivne antal dage før eller efter en angivet startdato. |
| [DateFormat](er-functions-datetime-dateformat.md) | Denne funktion returnerer en værdi i form af en *Streng*, som præsenterer en given datoværdi som tekst i det angivne format og i en eventuelt angivet kultur. |
| [DateTimeFormat](er-functions-datetime-datetimeformat.md) | Denne funktion returnerer en værdi i form af en *Streng*, som præsenterer en given dato-/klokkeslætsværdi som tekst i det angivne format og i en eventuelt angivet kultur. |
| [DateTimeValue](er-functions-datetime-datetimevalue.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet kultur til en dato-/klokkeslætsværdi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som konverteres fra en given dato-/klokkeslætsværdi i UTC-tid (Coordinated Universal Time) (Greenwich Mean \[time\]GMT). |
| [DateValue](er-functions-datetime-datevalue.md) | Denne funktion returnerer en værdi i form af en *Dato*, som er konverteret fra en given tekst i det angivne format og i en eventuelt angivet kultur til en datoværdi. |
| [DayOfYear](er-functions-datetime-dayofyear.md) | Denne funktion returnerer en værdi i form af et *Heltal*, som repræsenterer antallet af dage mellem 1. januar og den angivne dato. |
| [Dage](er-functions-datetime-days.md) | Denne funktion returnerer en værdi i form af et *Heltal*, som repræsenterer antallet af dage mellem to angivne datoer. |
| [Now](er-functions-datetime-now.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer den aktuelle dato og klokkeslæt for den aktuelle programserver. |
| [NullDate](er-functions-datetime-nulldate.md) | Denne funktion returnerer en værdi i form af en *Dato*, som repræsenterer datoen **nul** (1. januar 1900). |
| [NullDateTime](er-functions-datetime-nulldatetime.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer dato-/klokkeslætsværdien **nul** (1. januar 1900) i UTC-tid (Coordinated Universal Time). |
| [SessionNow](er-functions-datetime-sessionnow.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som repræsenterer dato og klokkeslæt for den aktuelle programsession. |
| [SessionToday](er-functions-datetime-sessiontoday.md) | Denne funktion returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programsession. |
| [I dag](er-functions-datetime-today.md) | Denne funktion returnerer en værdi i form af en *Dato*, som repræsenterer datoen for den aktuelle programserver. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]