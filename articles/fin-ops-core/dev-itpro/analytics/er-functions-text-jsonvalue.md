---
title: ER-funktionen JSONVALUE
description: Denne artikel indeholder oplysninger om, hvordan funktionen JSONVALUE til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 10/25/2021
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
ms.openlocfilehash: fba1141bce91fd7c9da3cd21aef13ce99329f379
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9267957"
---
# <a name="jsonvalue-er-function"></a>ER-funktionen JSONVALUE

[!include [banner](../includes/banner.md)]

Funktionen `JSONVALUE` opdeler data i JavaScript Object Notation (JSON)-format, som tilgås via den angivne sti og udtrækker en skalarværdi, der indeholder det angivne ID. Derefter returneres den udpakkede skalarværdi som en *Streng*-værdi.

## <a name="syntax"></a>Syntaks

```vb
JSONVALUE (input, path)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige sti til en datakilde af typen *Streng*, som indeholder JSON-data.

`path`: *Streng*

Identifikatoren for en skalarværdi af JSON-data. Brug en skråstreg (/) til at adskille navnene på relaterede JSON-noder. Brug kantede parenteser (\[\]) til at angive indekset for en bestemt værdi i en JSON-matrix. Bemærk, at nulbaseret nummerering bruges til dette indeks.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example-1"></a>Eksempel 1

Datakilden **$JsonField** indeholder følgende data i JSON-format: **{"BuildNumber":"7.3.1234.1", "KeyThumbprint":"7366E"}**. I dette tilfælde returnerer `JSONVALUE (JsonField, "BuildNumber")`-udtrykket følgende værdi af datatypen *Streng*: **"7.3.1234.1"**.

## <a name="example-2"></a>Eksempel 2

Datakilden **JsonField** af typen *Beregnet felt* indeholder dette udtryk: `"{""workers"": [ {""name"": ""Adam"", ""age"": 30, ""emails"": [""AdamS@Contoso.com"", ""AdamS@Hotmail.com"" ]}, { ""name"": ""John"", ""age"": 21, ""emails"": [""JohnS@Contoso.com"", ""JohnS@Aol.com""]}]}"`

Dette udtryk er konfigureret til at returnere en [*Streng*](er-formula-supported-data-types-primitive.md#string)-værdi, der repræsenterer følgende data i JSON-format.

```json
{
    "workers": [
        {
            "name": "Adam",
            "age": 30,
            "emails": [ "AdamS@Contoso.com", "AdamS@Hotmail.com" ]
        },
        {
            "name": "John",
            "age": 21,
            "emails": [ "JohnS@Contoso.com", "JohnS@Aol.com" ]
        }
    ]
}
```

I dette tilfælde returnerer udtrykket `JSONVALUE(json, "workers/[1]/emails/[0]")` følgende værdi af datatypen *Streng*: `JohnS@Contoso.com`.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
