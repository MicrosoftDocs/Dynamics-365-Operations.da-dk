---
title: ER-funktionen QRCODE
description: Dette emne indeholder oplysninger om, hvordan funktionen QRCODE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/10/2019
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
ms.openlocfilehash: b62ed829202028ca0cbf95a0dbc3460d047ca5a5
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4682961"
---
# <a name="qrcode-er-function"></a>ER-funktionen QRCODE

[!include [banner](../includes/banner.md)]

Funktionen `QRCODE` returnerer en *Container*-værdi, som viser QR-kodebilledet (Quick Response-kode) for den angivne streng i binært format.

## <a name="syntax"></a>Syntaks

```vb
QRCODE (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En *Streng*-værdi, der repræsenterer den oprindelige tekst.

## <a name="return-values"></a>Returnerede værdier

*Container*

Den resulterende binære strøm.

## <a name="example"></a>Eksempel

Du kan konfigurere et format til elektronisk rapportering (ER) til at generere et udgående dokument i Microsoft Office-format (Excel-projektmapper eller Word-dokumenter) ved hjælp af en foruddefineret skabelon. Denne skabelon kan indeholde et **Billed**-objekt (Excel-projektmappe) eller et **Indholdskontrolelement (Picture Content Control)** (Word-dokument) som pladsholder for et QR-kodebillede. Du skal føje et **Celle**-element, der skal bruges til at udfylde denne pladsholder, til det konfigurerede ER-format. Hvis du vil angive, hvilke oplysninger der skal gemmes i en QR-kode, skal du definere en binding for dette **Celle**-element. For eksempel kan du konfigurere en sådan binding til at indeholde følgende udtryk:

```vb
QRCODE (model.ListOfShelfLabels.LabelText)`
```

Når du kører det konfigurerede ER-format, vil tekstværdien i feltet **EtiketTekst** i datakilden **model.ListOfShelfLabels** blive brugt til at generere et QR-kodebillede. Dette billede erstatter en QR-kodebilledepladshol.der i dokumentskabelonen og bruges til at generere et udgående dokument. Når dette billede af det genererede dokument scannes, returneres den tekst, der blev hentet fra feltet **EtiketTekst** i datakilden **model.ListOfShelfLabels**. Du kan finde flere oplysninger under [Integrer billeder og figurer i de dokumenter, du opretter ved hjælp af ER](electronic-reporting-embed-images-shapes.md).

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]