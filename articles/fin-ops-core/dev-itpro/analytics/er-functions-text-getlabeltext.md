---
title: ER-funktionen GETLABELTEXT
description: Denne artikel indeholder oplysninger om, hvordan funktionen GETLABELTEXT til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 03/18/2022
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2022-01-01
ms.dyn365.ops.version: AX 10.0.25
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: dad87548518b77f2def1cf2383a21607f45170e1
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285933"
---
# <a name="getlabeltext-er-function"></a>ER-funktionen GETLABELTEXT

[!include [banner](../includes/banner.md)]

Funktionen `GETLABELTEXT` søger efter en bestemt label for at returnere en *[Streng](er-formula-supported-data-types-primitive.md#string)*-værdi, der repræsenterer oversættelsen af den angivne label på det angivne sprog.

## <a name="syntax"></a>Syntaks

```vb
GETLABELTEXT (label id, language)
```

## <a name="arguments"></a>Argumenter

### <a name="label-id"></a>Label-id

`label id`: *Streng* eller *Label-id*

Det gyldige id for en af følgende labeltyper:

- [Elektronisk rapportering (ER)](general-electronic-reporting.md) label
- Microsoft Dynamics 365 Finance-etiket

#### <a name="usage-notes"></a>Bemærkninger til brug

Dette argument kan kun defineres som en konstant ved hjælp af en af følgende understøttede mønstre:

- For ER-labels:

    - `@"GER_LABEL:<LABEL ID>"`
    - `"GER_LABEL:<LABEL ID>"`

- Til finanslabels:

    - `@"<LABEL ID>"`
    - `"<LABEL ID>"`

> [!NOTE]
> På designtid vises der en valideringsfejlmeddelelse på **[formeldesignersiden](er-advanced-formula-editor.md)**, hvis der ikke kan findes nogen label ved hjælp af det leverede label-id.

### <a name="language"></a>Sprog

`language`: *Streng*

En streng, der repræsenterer en sprogkode.

#### <a name="usage-notes"></a>Bemærkninger til brug

Dette argument kan defineres enten som en tekstkonstant eller som stien til et datakildefelt, der returnerer en *strengværdi*.

> [!NOTE]
> Der vises en fejlmeddelelse om validering på designtidspunktet, hvis der ikke kan findes nogen sprogkode ved hjælp af det angivne `language`-argument, når det er defineret som en tekstkonstant.
>
> Under kørsel returneres oversættelsen for systemsproget `EN-US` for en angivet label, hvis der ikke er fundet nogen sprogkode ved hjælp af det angivne `language`-argument.

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example-1-system-label"></a><a name=example-1></a>Eksempel 1: Systemlabel

Udtrykkene `GETLABELTEXT (@"SYS70894", "en-us")` og `GETLABELTEXT ("SYS70894", "en-us")` returner den engelske oversættelse "Nothing to print" for programlabelen `@SYS70894`.

## <a name="example-2-er-label"></a><a name=example-2></a>Eksempel 2: ER-label

Du starter med at redigere en ER-[konfiguration](general-electronic-reporting.md#Configuration), som er [afledt](er-quick-start2-customize-report.md#DeriveProvidedFormat) af **ISO20022 Credit transfer (DE)**-konfigurationen, angiver en ny datakilde af typen *[Beregnet felt](er-calculated-field-ds-performance.md)* og konfigurerer udtrykket `GETLABELTEXT(@"GER_LABEL:VendorName", "de")` til denne datakilde. I dette tilfælde returnerer datakilden under kørsel den tyske oversættelse "Kreditorenname" for `@GER_LABEL:VendorName` ER-labelen, der oprindeligt blev konfigureret i den grundlæggende **ISO20022 Credit transfer (DE)** ER-konfiguration.

## <a name="additional-resources"></a>Yderligere ressourcer

[Tekstfunktioner](er-functions-category-text.md)

[Designe flersprogede rapporter i elektronisk rapportering](er-design-multilingual-reports.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
