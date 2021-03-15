---
title: Liste over ER-funktioner i containerkategorien
description: Dette emne indeholder oplysninger om de containerfunktioner, der understøttes i elektronisk rapportering (ER).
author: NickSelin
manager: kfend
ms.date: 12/14/2020
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
ms.search.validFrom: 2020-12-01
ms.dyn365.ops.version: 10.0.17
ms.openlocfilehash: 46d1af85773f6c3d07865658c554dee74fae625f
ms.sourcegitcommit: e8a46e127d70986539c138b27a641bff6f6874d0
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/15/2020
ms.locfileid: "4739064"
---
# <a name="list-of-er-functions-in-the-container-category"></a>Liste over ER-funktioner i containerkategorien

[!include [banner](../includes/banner.md)]

Container-[funktioner](er-formula-language.md#functions) til [elektronisk rapportering (ER)](general-electronic-reporting.md) kan bruges til at udføre handlinger på datakilder af datatypen *Container*. Disse operationer finder sted, når behandlingsdata repræsenterer en samling binære data i BLOB-format (binært stort objekt). Dette emne indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion | Betegnelse |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Denne funktion returnerer en *Container*-værdi, der består af binært indhold, der er afkodet fra den angivne ASCII-streng, som repræsenterer en Base64-gruppe af binær til tekst-kodningsskemaer. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]