---
title: ER-funktionen GETCURRENTCOMPANY
description: Dette emne indeholder oplysninger om, hvordan funktionen GETCURRENTCOMPANY til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
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
ms.openlocfilehash: fcb5ef2f218a85bab25f830db583343504c46e98
ms.sourcegitcommit: 6cb174d1ec8b55946dca4db03d6a3c3f4c6fa2df
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/09/2021
ms.locfileid: "5567538"
---
# <a name="getcurrentcompany-er-function"></a>ER-funktionen GETCURRENTCOMPANY

[!include [banner](../includes/banner.md)]

Funktionen `GETCURRENTCOMPANY` returnerer en *Streng*-værdi, som repræsenterer koden for en juridisk enhed (firma), som en bruger i øjeblikket er logget på.

## <a name="syntax"></a>Syntaks

```vb
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruger, der er logget på firmaet **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]