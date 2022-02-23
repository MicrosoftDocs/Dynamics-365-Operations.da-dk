---
title: ER-funktionen TABLENAME2ID
description: Dette emne indeholder oplysninger om, hvordan funktionen TABLENAME2ID til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: a68a8e1f4afa378ab446eae12bc90cdb3aba8b19
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4681152"
---
# <a name="tablename2id-er-function"></a>ER-funktionen TABLENAME2ID

[!include [banner](../includes/banner.md)]

Funktionen `TABLENAME2ID` returnerer en numerisk gengivelse af tabel-ID'et for det angivne tabelnavn som en værdi angivet som et *Heltal*.

## <a name="syntax"></a>Syntaks

```vb
TABLENAME2ID (text)
```

## <a name="arguments"></a>Argumenter

`text`: *Streng*

En tekstværdi, der repræsenterer et gyldigt tabelnavn.

## <a name="return-values"></a>Returnerede værdier

*Heltal*

Den resulterende numeriske værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Udførelse af denne funktion kan have forskellige resultater i forskellige forekomster af Microsoft Dynamics 365 Finance, selvom det samme firmanavn bruges.

## <a name="example"></a>Eksempel

`TABLENAME2ID ("Intrastat")` returnerer **1510**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)
