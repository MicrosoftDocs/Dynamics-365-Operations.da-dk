---
title: ER-funktionen ADDDAYS
description: Dette emne indeholder oplysninger om, hvordan funktionen ADDDAYS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/03/2019
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
ms.openlocfilehash: 998cf2c0dac67040814d4a32e433b465ec51f88c
ms.sourcegitcommit: 445f6d8d0df9f2cbac97e85e3ec3ed8b7d18d3a2
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 09/01/2020
ms.locfileid: "3743369"
---
# <a name="adddays-er-function"></a>ER-funktionen ADDDAYS

[!include [banner](../includes/banner.md)]

Funktionen `ADDDAYS` beregner en værdi med *DatoKlokkeslæt*, der er det angivne antal dage før eller efter en angivet startdato.

## <a name="syntax"></a>Syntaks

```vb
ADDDAYS (datetime, days)
```

## <a name="arguments"></a>Argumenter

`datetime`: *DatoKlokkeslæt*

En dato-/klokkeslætsværdi, der repræsenterer startdatoen.

`days`: *Heltal*

Antallet af dage inden eller efter `datetime`.

## <a name="return-values"></a>Returnerede værdier

*DateTime*

Den returnerede dato-/klokkeslætsværdi.

## <a name="usage-notes"></a>Bemærkninger til brug

En positiv værdi for `days` leverer en fremtidig dato. En negativ værdi giver en tidligere dato.

## <a name="example-1"></a>Eksempel 1

`ADDDAYS (NOW(), 7)` returnerer datoen og klokkeslættet syv dage ud i fremtiden.

## <a name="example-2"></a>Eksempel 2

`ADDDAYS (NOW(), -3)` returnerer datoen og klokkeslættet tre dage før.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)
