---
title: ER-funktionen UGE.NR
description: Dette emne indeholder oplysninger om, hvordan funktionen UGE.NR til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/03/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-12-03
ms.dyn365.ops.version: AX 10.0.24
ms.openlocfilehash: fe36d4142b6e4922e2cbca09bb0ca9f68f6680a0
ms.sourcegitcommit: c85eac17fbfbd311288b50664f9e2bae101c1fe6
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/03/2021
ms.locfileid: "7891338"
---
# <a name="weeknum-er-function"></a>ER-funktionen UGE.NR

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funktionen `WEEKNUM` returnerer en værdi i form af et *[Heltal](er-formula-supported-data-types-primitive.md#integer)*, som repræsenterer ugen i året, der inkluderer en angivet værdi af typen *[Dato](er-formula-supported-data-types-primitive.md#date)*. Beregningen er baseret på kulturafhængige regler, der definerer en kalenderuge og den første dag i ugen.

## <a name="syntax"></a>Syntaks

```vb
WEEKNUM (date, culture) as Integer
```

## <a name=""></a><a name="arguments">Argumenter</a>

`date`: *Dato*

En datoværdi, som repræsenterer den dato, der skal bruges til beregning af ugen i året.

`culture`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Den kultur, du vil bruge til beregning. Du kan bruge kulturkoder, der understøttes i overensstemmelse med .NET-[standarder](/dotnet/api/system.globalization.cultureinfo.getcultures?view=net-5.0).

## <a name="return-values"></a>Returnerede værdier

*Heltal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Ugen i året beregnes på basis af [ISO 8601](https://www.iso.org/iso-8601-date-and-time-format.html)-standarden, hvis denne standard er godkendt i et land eller område, som landestandarden er angivet for under kørslen. Ellers baseres beregningen på lande-/områdespecifikke nationale standarder.

Hvis der angives en ikke-understøttet [kultur](#arguments)kode som argument for funktionen `WEEKNUM` under kørsel, udløser det en undtagelse. Hvis den tomme streng leveres som en kulturkode, bruges den engelske landeneutrale kalender til beregning af ugenummeret.

## <a name="examples"></a>Eksempler

`WEEKNUM (DATEVALUE ("01-01-2020", "de"))` returnerer **1**.

`WEEKNUM (DATEVALUE ("01-01-2021", "de"))` returnerer **53**.

`WEEKNUM (DATEVALUE ("01-01-2022", "de"))` returnerer **52**.

`WEEKNUM (DATEVALUE ("01-01-2022", "ar"))` returnerer **21**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
