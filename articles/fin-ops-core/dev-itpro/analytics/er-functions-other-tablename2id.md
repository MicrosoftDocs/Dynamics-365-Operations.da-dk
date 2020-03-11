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
ms.search.scope: Core, Operations
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 951de1d1505508ebb6abeff5b80ecef10573e117
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3041256"
---
# <a name="TABLENAME2ID">ER-funktionen TABLENAME2ID</a>

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
