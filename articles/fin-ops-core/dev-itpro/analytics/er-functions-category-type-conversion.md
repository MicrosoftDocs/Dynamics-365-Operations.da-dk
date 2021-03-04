---
title: Liste over ER-funktioner af kategorien typekonvertering
description: Dette emne indeholder oplysninger om de konverteringsfunktioner, der understøttes i elektronisk rapportering (ER).
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
ms.openlocfilehash: d160c02403bf067ed523fbd634e65c622b522b97
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686068"
---
# <a name="list-of-er-functions-in-the-type-conversion-category"></a>Liste over ER-funktioner af kategorien typekonvertering

[!include [banner](../includes/banner.md)]

Typekonverteringsfunktioner til elektronisk rapportering (ER) kan bruges til at konvertere værdier mellem typer. Dette emne indeholder en oversigt over disse funktioner.

## <a name="type-conversion-functions"></a>Typekonverteringsfunktioner

| Funktion | Beskrivelse |
|----------|-------------|
| [Int64Value](er-functions-conversion-int64value.md)   | Denne funktion returnerer en *Int64*-værdi, der repræsenterer den angivne streng. |
| [IntValue](er-functions-conversion-intvalue.md)       | Denne funktion returnerer en *Int*-værdi, der repræsenterer den angivne streng. |
| [NumberValue](er-functions-conversion-numbervalue.md) | Denne funktion returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi. Under konverteringen tages de specificerede decimal- og ciffergrupperingsseparatorer i betragtning. |
| [Værdi](er-functions-conversion-value.md)             | Denne funktion returnerer en *Reel* værdi, der konverteres fra den angivne *Streng*-værdi. |

## <a name="type-conversion-functions-in-the-date-and-time-category"></a>Typekonverteringsfunktioner i kategorien dato og klokkeslæt

I følgende tabel beskrives typekonverteringsfunktionerne i [kategorien dato og klokkeslæt](er-functions-category-datetime.md).

| Funktion | Beskrivelse |
|----------|-------------|
| [DateTimeValue](er-functions-datetime-datetimevalue.md)   | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som er konverteret fra en given *Streng*-værdi i det angivne format og i en eventuelt angivet kultur til en dato-/klokkeslætsværdi. |
| [DateToDateTime](er-functions-datetime-datetodatetime.md) | Denne funktion returnerer en værdi i form af *DatoKlokkeslæt*, som konverteres fra en given *Dato*-værdi til en dato-/klokkeslætsværdi i UTC-tid (Coordinated Universal Time) (Greenwich Mean Time \[GMT\]). |
| [DateValue](er-functions-datetime-datevalue.md)           | Denne funktion returnerer en værdi i form af en *Dato*, som er konverteret fra en given *Streng*-værdi i det angivne format og i en eventuelt angivet kultur til en datoværdi. |

## <a name="type-conversion-functions-in-the-list-category"></a>Typekonverteringsfunktioner i listekategorien

I følgende tabel beskrives typekonverteringsfunktionerne i [listekategorien](er-functions-category-list.md).

| Funktion | Beskrivelse |
|----------|-------------|
| [Liste](er-functions-list-list.md)                 | Denne funktion returnerer en ny *Postliste*-værdi som en ny liste, der er oprettet på grundlag af de angivne argumenter af typen *Container (post)*. |
| [ListOfFields](er-functions-list-listoffields.md) | Denne funktion returnerer en *Postliste*-værdi, der er oprettet på baggrund af strukturen af et angivet argument af typen *Optælling* eller *Container (post)*. |
| [Opdel](er-functions-list-split.md)               | Denne funktion opdeler den angivne *Streng*-værdi i understrenge og returnerer resultatet som en ny *Postliste*-værdi. |
| [StringJoin](er-functions-list-stringjoin.md)     | Denne funktion returnerer en *Streng*-værdi, der består af sammenføjede værdier for det angivne felt fra den angivne *Postliste*-værdi. Værdierne kan være adskilt af et angivet separatortegn. |

## <a name="type-conversion-functions-in-the-text-category"></a>Typekonverteringsfunktioner i tekstkategorien

I følgende tabel beskrives typekonverteringsfunktionerne i [tekstkategorien](er-functions-category-text.md).

| Funktion | Beskrivelse |
|----------|-------------|
| [Char](er-functions-text-char.md)                 | Denne funktion returnerer en *Streng*-værdi, som repræsenterer et enkelt tegn, der refereres til af det angivne Unicode-nummer. |
| [GuidValue](er-functions-text-guidvalue.md)       | Denne funktion konverterer det angivne input af typen *Streng* til et dataelement af typen *GUID*. |
| [NumberFormat](er-functions-text-numberformat.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer det angivne tal i det angivne format og i en eventuelt angivet kultur. |
| [QrCode](er-functions-text-qrcode.md)             | Denne funktion returnerer en *Container*-værdi, som præsenterer QR-kodebilledet (Quick Response-kode) for den angivne streng i binært format. |
| [Tekst](er-functions-text-text.md)                 | Denne funktion returnerer en *Streng*-værdi, som repræsenterer det angivne tal, efter at det er blevet konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard for den aktuelle forekomst. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]