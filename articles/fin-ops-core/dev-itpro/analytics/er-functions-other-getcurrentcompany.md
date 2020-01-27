---
title: ER-funktionen GETCURRENTCOMPANY
description: Dette emne indeholder oplysninger om, hvordan funktionen GETCURRENTCOMPANY til elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: a0b4c93a4705cd0e382b9b6c7af1d199beeceabe
ms.sourcegitcommit: 36857283d70664742c8c04f426b231c42daf4ceb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/20/2019
ms.locfileid: "2915987"
---
# <a name="GETCURRENTCOMPANY">ER-funktionen GETCURRENTCOMPANY</a>

[!include [banner](../includes/banner.md)]

Funktionen `GETCURRENTCOMPANY` returnerer en *Streng*-værdi, som repræsenterer koden for en juridisk enhed (firma), som en bruger i øjeblikket er logget på.

## <a name="syntax"></a>Syntaks

```
GETCURRENTCOMPANY ()
```

## <a name="return-values"></a>Returnerede værdier

*Streng*

Den returnerede tekstværdi.

## <a name="example"></a>Eksempel

`GETCURRENTCOMPANY ()` returnerer **USMF** for en bruger, der er logget på firmaet **Contoso Entertainment System USA**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)
