---
title: ER-funktionen FA_SUM
description: Dette emne indeholder oplysninger om, hvordan funktionen FA_SUM til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/17/2019
ms.topic: article
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
ms.openlocfilehash: d6f380e384e591e7417cfa40c73f9be6575fb0f6
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5744289"
---
# <a name="fa_sum-er-function"></a>ER-funktionen FA_SUM

[!include [banner](../includes/banner.md)]

Funktionen `FA_SUM` returnerer en *Container (post)*-værdi, der består af data for anlægsaktivbeløbene for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og datoperioder.

## <a name="syntax"></a>Syntaks

```vb
FA_SUM (fixed asset code, value model code, start date, end date)
```

## <a name="arguments"></a>Argumenter

`fixed asset code`: *Streng*

En *Streng*-værdi, der repræsenterer koden for en anlægsaktivvare, som saldoen beregnes for.

`value model code`: *Streng*

En *Streng*-værdi, der repræsenterer koden for en værdimodel, som saldoen beregnes for.

`start date`: *Dato*

En *Dato*-værdi, der repræsenterer startdatoen for en periode, som anlægsaktiv beløbene beregnes for.

`end date`: *Dato*

En *Dato*-værdi, der repræsenterer slutdatoen for en periode, som anlægsaktiv beløbene beregnes for.

## <a name="return-values"></a>Returnerede værdier

*Container (post)*

Den resulterende postværdi.

## <a name="example"></a>Eksempel

`FA_SUM ("COMP-000001", "Current", Date1, Date2)` returnerer datacontaineren for anlægsaktivet **COMP-000001**, der er forberedt for den **Aktuelle** værdimodel og for en periode fra **Dato1** til **Dato2**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]