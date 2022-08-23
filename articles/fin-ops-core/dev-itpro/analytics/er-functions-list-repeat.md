---
title: ER-funktionen REPEAT
description: Denne artikel indeholder oplysninger om, hvordan funktionen REPEAT til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 08/01/2022
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2022-06-01
ms.dyn365.ops.version: AX 10.0.29
ms.openlocfilehash: c56139a3c63b03f907b1dcbf4365990d2a13c35a
ms.sourcegitcommit: c98d55a4a6e27239ae6b317872332f01cbe8b875
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/02/2022
ms.locfileid: "9220686"
---
# <a name="repeat-er-function"></a>ER-funktionen REPEAT

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funktionen `REPEAT` opbygger en post, der indeholder det felt, som har en værdi, der svarer til det angivne input. Derefter returneres en ny *Postliste* for en post, der gentages et bestemt antal gange.

## <a name="syntax"></a>Syntaks

```vb
REPEAT (item, number)
```

## <a name="arguments"></a>Argumenter

`item`: Enhver understøttet [primitiv](er-formula-supported-data-types-primitive.md) eller [sammensat](er-formula-supported-data-types-composite.md) datatype

Værdien, der skal gentages.

`number`: *Heltal*

Antal gentagelser.

## <a name="return-values"></a>Returnerede værdier

*Liste over poster*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Listen over gentagne poster, der returneres, viser følgende felter:

- Den angivne værdi (`Item`-felt)
- Det aktuelle postindeks (`Number`-felt)

> [!NOTE]
> Da der bruges ettalsbaseret nummerering til denne funktion, skal du angive værdien af feltet `Number` til **1** for den første post på resultatlisten.

Du kan bruge denne funktion til at multiplicere eksisterende data, så du kan udføre performance- og volumentest af [ER-løsninger (Electronic Reporting)](general-electronic-reporting.md) ved hjælp af [Regression Suite Automation Tool (RSAT)](../perf-test/rsat/rsat-overview.md).

## <a name="example"></a>Eksempel

Du vil generere et dokument i XML-format, der skal indeholde så mange `Party` XML-elementer, som du angiver i et dataindtastningsfelt i dialogboksen under kørslen, før kørslen af et ER-format begynder.

Følgende illustration viser ER-[formatet](er-overview-components.md#format-component). I dette format tilføjes det enkelte `Party` XML-element for at vise egenskaberne for en enkelt part.

<a href="./media/er-repeat-function-1.png"><img src="./media/er-repeat-function-1.png" alt="Format structure on the Format tab of the Format designer page." class="alignnone size-full" width="929" height="548" /></a>

I den næste illustration vises følgende konfigurerede datakilder:

- Den `Party`-datakilde, der repræsenterer en enkelt part. Feltet `Party.Value` bruges til at vise en enkelt tekstværdi.
- Den `NumberOfRepeats`-[datakilde](er-user-input-parameter-data-sources.md), der bruges til at tilbyde et dataindtastningsfelt i dialogboksen under kørslen, så du kan angive det antal parter, der skal indtastes i det genererede dokument.
- Datakilden `Party2`, der gentager posten `Party` det antal gange, du har angivet i `NumberOfRepeats`-datakilden.

<a href="./media/er-repeat-function-2.png"><img src="./media/er-repeat-function-2.png" alt="Configured data sources on the Mapping tab of the Format designer page." class="alignnone size-full" width="1044" height="411" /></a>

Den næste illustration viser databindinger for det ER-format, der kan redigeres, og som oprettes for at generere output i XML-format. Dette output viser individuelle parter som fasttekstnoder.

<a href="./media/er-repeat-function-3.png"><img src="./media/er-repeat-function-3.png" alt="Configured data bindings on the Mapping tab of the Format designer page." class="alignnone size-full" width="1051" height="417" /></a>

I følgende illustration vises resultatet, når det designede format køres, og værdien af `NumberOfRepeats`-datakilden er angivet til **5**.

<a href="./media/er-repeat-function-4.png"><img src="./media/er-repeat-function-4.png" alt="Result of running the format on a new web browser tab." class="alignnone wp-image-290711 size-full" width="400" height="380" /></a>

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
