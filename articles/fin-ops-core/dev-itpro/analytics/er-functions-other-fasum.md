---
title: ER-funktionen FA_SUM
description: Dette emne indeholder oplysninger om, hvordan funktionen FA_SUM til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/17/2019
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
ms.openlocfilehash: 32eb07689598a3b6c852f272b480106670b88cd0
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2916976"
---
# <a name="FA_SUM">ER-funktionen FA_SUM</a>

[!include [banner](../includes/banner.md)]

Funktionen `FA_SUM` returnerer en *Container (post)*-værdi, der består af data for anlægsaktivbeløbene for den angivne anlægsaktivvare, værdimodelkode, rapporteringsår og datoperioder.

## <a name="syntax"></a>Syntaks

```
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