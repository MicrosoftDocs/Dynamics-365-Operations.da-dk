---
title: ER-funktionen ADDDAYS
description: Denne artikel indeholder oplysninger om, hvordan funktionen ADDDAYS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/03/2019
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
ms.openlocfilehash: 7cf2031c042ae93512cc85afe6a1b51558f6c8f7
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8858735"
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


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]