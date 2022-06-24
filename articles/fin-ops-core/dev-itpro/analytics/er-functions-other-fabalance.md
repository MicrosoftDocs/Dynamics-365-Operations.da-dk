---
title: ER-funktionen FA_BALANCE
description: Denne artikel indeholder oplysninger om, hvordan funktionen FA_BALANCE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/17/2019
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
ms.openlocfilehash: c3dd44f0d5ff143189b2c55c4df80847c2161231
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8902677"
---
# <a name="fa_balance-er-function"></a>ER-funktionen FA_BALANCE

[!include [banner](../includes/banner.md)]

Funktionen `FA_BALANCE` returnerer en *Container (post)*-værdi, der består af data for anlægsaktivsaldoen for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og rapporteringsdato.

## <a name="syntax"></a>Syntaks

```vb
FA_BALANCE (fixed asset code, value model code, reporting year, reporting date)
```

## <a name="arguments"></a>Argumenter

`fixed asset code`: *Streng*

En *Streng*-værdi, der repræsenterer koden for en anlægsaktivvare, som saldoen beregnes for.

`value model code`: *Streng*

En *Streng*-værdi, der repræsenterer koden for en værdimodel, som saldoen beregnes for.

`reporting year`: *Fasttekstværdi*

En fasttekstværdi for programfasttekstgen **AssetYear**, der definerer en periode for saldoberegningen.

`reporting date`: *Dato*

En *Dato*-værdi, der definerer en dato for saldoberegningen.

## <a name="return-values"></a>Returnerede værdier

*Container (post)*

Den resulterende postværdi.

## <a name="example"></a>Eksempel

`FA_ BALANCE ("COMP-000001", "Current", AxEnumAssetYear.ThisYear, SESSIONTODAY ())` returnerer den datacontainer med saldi for anlægsaktivet **COMP-000001**, som er blevet forbedredt for værdimodellen **Aktuel** for den aktuelle programsessionsdato.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]