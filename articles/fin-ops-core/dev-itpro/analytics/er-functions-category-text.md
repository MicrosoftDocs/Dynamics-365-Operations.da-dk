---
title: Liste over ER-funktioner i kategorien tekst
description: Dette emne indeholder oplysninger om tekstfunktionerne, der understøttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 04/02/2020
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
ms.openlocfilehash: bd4dd7e9a3e1aa448adea5abd0c21b8133f34e3b
ms.sourcegitcommit: fb8ad8e2b142441a6530b364f3258bbcc0c724d2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 04/02/2020
ms.locfileid: "3201083"
---
# <a name="list-of-er-functions-of-the-text-category"></a>Liste over ER-funktioner i kategorien tekst

[!include [banner](../includes/banner.md)]

Tekstfunktioner til elektronisk rapportering (ER) kan bruges til at udføre handlinger på datakilder af datatypen *Streng*. Dette emne indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion | Beskrivelse |
|----------|-------------|
| [Char](er-functions-text-char.md) | Denne funktion returnerer en *Streng*-værdi, som er udtryk for et enkelt tegn, der refereres til af det angivne Unicode-nummer. |
| [Sammenkæde](er-functions-text-concatenate.md) | Denne funktion returnerer alle de angivne tekststrenge som en *Streng*-værdi, når de er blevet forenet i en streng. |
| [Format](er-functions-text-format.md) | Denne funktion returnerer den angivne streng som en *Streng*-værdi, efter den er blevet formateret ved at erstatte alle forekomster af **%N** med det *N*'te argument. |
| [GetEnumValueByName](er-functions-text-getenumvaluebyname.md) | Denne funktion søger efter en bestemt *Fasttekst*-værdi i den angivne optællingsdatakilde ved hjælp af det optællingsnavn, der er angivet som en *Streng*-værdi. Hvis *Fasttekst*-værdien findes, returnerer funktionen den. |
| [GuidValue](er-functions-text-guidvalue.md) | Denne funktion konverterer det angivne input af typen *Streng* til et dataelement af typen *GUID*. |
| [JsonValue](er-functions-text-jsonvalue.md) | Denne funktion opdeler data i JavaScript Object Notation (JSON)-format, som tilgås via den angivne sti og udtrækker en skalarværdi, der er baseret på det angivne ID. Derefter returneres den udpakkede skalarværdi som en *Streng*-værdi. |
| [Venstre](er-functions-text-left.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i begyndelsen af den angivne streng. |
| [Len](er-functions-text-len.md) | Denne funktion returnerer en *Heltals*-værdi, som repræsenterer antallet af tegn i den angivne streng. |
| [Lower](er-functions-text-lower.md) | Denne funktion returnerer den angivne tekststreng som en *Streng*-værdi, når den er konverteret til små bogstaver. |
| [Mid](er-functions-text-mid.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn fra den angivne streng fra begyndelsen af den angivne position. |
| [NumberFormat](er-functions-text-numberformat.md) | Denne funktion returnerer en værdi i form af en *Streng*, som præsenterer det angivne tal i det angivne format og i en eventuelt angivet kultur. |
| [NumeralsToText](er-functions-text-numeralstotext.md) | Denne funktion returnerer det angivne tal som en *Streng*-værdi, efter at det er blevet skrevet helt ud (det vil være konverteret til tekststrenge) på det angivne sprog. |
| [PadLeft](er-functions-text-padleft.md) | Denne funktion returnerer en *Streng*-værdi af den angivne længde, hvor begyndelsen af den angivne streng er udfyldt med en eller flere udgaver af de angivne tegn. |
| [QrCode](er-functions-text-qrcode.md) | Denne funktion returnerer en *Container*-værdi, som præsenterer QR-kodebilledet (Quick Response-kode) for den angivne streng i binært format. |
| [Erstatte](er-functions-text-replace.md) | Denne funktion returnerer den angivne tekststreng som en *Streng*-værdi, efter at hele eller en del af den er blevet erstattet med en anden streng. |
| [Højre](er-functions-text-right.md) | Denne funktion returnerer en *Streng*-værdi, som repræsenterer det angivne antal tegn i slutningen af den angivne streng. |
| [Tekst](er-functions-text-text.md) | Denne funktion returnerer det angivne tal som en *Streng*-værdi, efter at det er blevet konverteret til en tekststreng, der er formateret i henhold til indstillingerne for serverens landestandard for den aktuelle forekomst. |
| [Oversæt](er-functions-text-translate.md) | Denne funktion returnerer en *Streng*-værdi, der indeholder resultatet af erstatningen af den angivne tekst i tegn for et andet angivet sæt tegn. |
| [Trim](er-functions-text-trim.md) | Denne funktion returnerer den angivne streng som en *Streng*-værdi, når foranstillede og efterstillede mellemrum er blevet afkortet, og flere mellemrum mellem ord er blevet fjernet. |
| [Øverste](er-functions-text-upper.md) | Denne funktion returnerer den angivne tekststreng som en *Streng*-værdi, når den er konverteret til store bogstaver. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)
