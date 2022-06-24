---
title: Liste over ER-funktioner i kategorien tekst
description: Denne artikel indeholder oplysninger om tekstfunktionerne, der understøttes i elektronisk rapportering (ER).
author: NickSelin
ms.date: 02/28/2022
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
ms.openlocfilehash: 502a68d51705114adc096a1cd2217210f4e925bb
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8885537"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Liste over ER-funktioner i kategorien tekst

[!include [banner](../includes/banner.md)]

Tekstfunktioner til elektronisk rapportering (ER) kan bruges til at udføre handlinger på datakilder af datatypen *Streng*. Denne artikel indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion | Beskrivelse |
|----------|-------------|
| [Char](er-functions-text-char.md) | Denne funktion returnerer en *Streng*-værdi, som er udtryk for et enkelt tegn, der refereres til af det angivne Unicode-nummer. |
| [Sammenkæde](er-functions-text-concatenate.md) | Denne funktion returnerer alle de angivne tekststrenge som en *Streng*-værdi, når de er blevet forenet i en streng. |
| [Format](er-functions-text-format.md) | Denne funktion returnerer den angivne streng som en *Streng*-værdi, efter den er blevet formateret ved at erstatte alle forekomster af **%N** med det *N*'te argument. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Denne funktion søger efter en bestemt *Fasttekst*-værdi i den angivne optællingsdatakilde ved hjælp af det optællingsnavn, der er angivet som en *Streng*-værdi. Hvis *Fasttekst*-værdien findes, returnerer funktionen den. |
| [GetLabelText](er-functions-text-getlabeltext.md) | Denne funktion søger efter en bestemt label for at returnere en *[Streng](er-formula-supported-data-types-primitive.md#string)*-værdi, der repræsenterer oversættelsen af den angivne label på det angivne sprog. |
| [GuidValue](er-functions-text-guidvalue.md) | Denne funktion konverterer det angivne input af typen *Streng* til et dataelement af typen *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Denne funktion opdeler data i JavaScript Object Notation (JSON)-format, som tilgås via den angivne sti og udtrækker en skalarværdi, der er baseret på det angivne ID. Derefter returneres den udpakkede skalarværdi som en *Streng*-værdi. |
| [Venstre](er-functions-text-left.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i begyndelsen af den angivne streng. |
| [Len](er-functions-text-len.md) | Denne funktion returnerer en *Heltals*-værdi, som repræsenterer antallet af tegn i den angivne streng. |
| [Lower](er-functions-text-lower.md) | Denne funktion returnerer den angivne tekststreng som en *Streng*-værdi, når den er konverteret til små bogstaver. |
| [Mid](er-functions-text-mid.md) | Denne funktion returnerer en *[Streng](er-formula-supported-data-types-primitive.md#string)*-værdi, som repræsenterer det angivne antal tegn fra den angivne streng fra begyndelsen af den angivne position. |
| [NewGUID](er-functions-text-newguid.md) | Denne funktion returnerer en nyligt genereret *[GUID](er-formula-supported-data-types-primitive.md#guid)*-værdi. |
| [NumberFormat](er-functions-text-numberformat.md) | Denne funktion returnerer en værdi i form af en *Streng*, som præsenterer det angivne tal i det angivne format og i en eventuelt angivet kultur. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Denne funktion returnerer det angivne tal som en *Streng*-værdi, efter at det er blevet skrevet helt ud (det vil være konverteret til tekststrenge) på det angivne sprog. |
| [PadLeft](er-functions-text-padleft.md) | Denne funktion returnerer en *Streng*-værdi af den angivne længde, hvor begyndelsen af den angivne streng er udfyldt med en eller flere udgaver af de angivne tegn. |
| [QrCode](er-functions-text-qrcode.md) | Denne funktion returnerer en *Container*-værdi, som præsenterer QR-kodebilledet (Quick Response-kode) for den angivne streng i binært format. |
| [Erstatte](er-functions-text-replace.md) | Denne funktion returnerer den angivne tekststreng som en *Streng*-værdi, efter at hele eller en del af den er blevet erstattet med en anden streng. |
| [Højre](er-functions-text-right.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i slutningen af den angivne streng. |
| [Tekst](er-functions-text-text.md) | Denne funktion returnerer det angivne tal som en *Streng*-værdi, efter at det er blevet konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard for den aktuelle forekomst. |
| [Oversæt](er-functions-text-translate.md) | Denne funktion returnerer en *Streng*-værdi, der indeholder resultatet af erstatningen af den angivne tekst i tegn for et andet angivet sæt tegn. |
| [Trim](er-functions-text-trim.md) | Denne funktion returnerer den angivne tekststreng som en *Streng*-værdi efter tabulator, vognretur, linjeskift og sideskifttegn er blevet erstattet af et enkelt mellemrum, efter at foranstillede og efterfølgende mellemrum er blevet afkortet, og efter at flere mellemrum mellem ord er fjernet. |
| [Øverste](er-functions-text-upper.md) | Denne funktion returnerer den angivne tekststreng som en *Streng*-værdi, når den er konverteret til store bogstaver. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
