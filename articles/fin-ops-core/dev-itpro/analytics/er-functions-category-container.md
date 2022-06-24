---
title: Liste over ER-funktioner i containerkategorien
description: Denne artikel indeholder oplysninger om de containerfunktioner, der understøttes i elektronisk rapportering (ER).
author: NickSelin
ms.date: 12/14/2020
ms.prod: ''
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
ms.openlocfilehash: 5c86b0ae6cbf4ac6515491b55390d42c371eae4b
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8883811"
---
# <a name="list-of-er-functions-in-the-container-category"></a>Liste over ER-funktioner i containerkategorien

[!include [banner](../includes/banner.md)]

Container-[funktioner](er-formula-language.md#Functions) til [elektronisk rapportering (ER)](general-electronic-reporting.md) kan bruges til at udføre handlinger på datakilder af datatypen *Container*. Disse operationer finder sted, når behandlingsdata repræsenterer en samling binære data i BLOB-format (binært stort objekt). Denne artikel indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion | Betegnelse |
|----------|-------------|
| [Base64StringToContainer](er-functions-container-base64stringtocontainer.md) | Denne funktion returnerer en *Container*-værdi, der består af binært indhold, der er afkodet fra den angivne ASCII-streng, som repræsenterer en Base64-gruppe af binær til tekst-kodningsskemaer. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
