---
title: ER-funktionen LISTOFFIELDS
description: Denne artikel indeholder oplysninger om, hvordan funktionen LISTOFFIELDS til elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 12/12/2019
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.custom: 58771
ms.assetid: 24223e13-727a-4be6-a22d-4d427f504ac9
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: e795251004136469f64e8ebbb190a3bceaa382ed
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9288162"
---
# <a name="listoffields-er-function"></a>ER-funktionen LISTOFFIELDS

[!include [banner](../includes/banner.md)]

Funktionen `LISTOFFIELDS` returnerer en *Postliste*-værdi, der er oprettet på baggrund af strukturen af det angivne argument i typen *Fasttekst* eller *Container (post)*.

## <a name="syntax-1"></a>Syntaks 1

```vb
LISTOFFIELDS (path)
```

## <a name="syntax-2"></a>Syntaks 2

```vb
LISTOFFIELDS (path, language)
```

## <a name="arguments"></a>Argumenter

`path`: Datakildenreference

Den gyldige referencesti til en datakilde for en af følgende datatyper:

- Modelfasttekst
- Formatfasttekst
- Programfasttekst
- Container (post)

`language`: *Streng*

Tekst, der repræsenterer en sprogkode.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Den liste, der oprettes, består af poster, der har følgende felter:

- **Navn** (*Streng*-datatype)
- **Etiket** (*Streng*-datatype)
- **Beskrivelse** (*Streng*-datatype)
- **IsTranslated** (*Boolesk*-datatype)

Hvis `path`-argumentet refererer til en datakilde for typen *Container (post)*, føjes der en ny post til den liste, der oprettes, for hvert felt i den refererede containerpost. For hver post, der oprettes, returnerer feltet **Navn** navnet på feltet for den containerpost, der refereres til, som den aktuelle post blev oprettet for.

Hvis `path`-argumentet refererer til en datakilde af typen *Fasttekst*, føjes der en ny post til den liste, der oprettes, for hver fasttekstværdi i den refererede fasttekst. For hver post, der oprettes, returnerer feltet **Navn** værdien af den refererede fasttekst, som den aktuelle post er oprettet for; feltet **Beskrivelse** returnerer beskrivelsen af denne fasttekst, og feltet **Etiket** returnerer etiketten for den pågældende fasttekst.

Når der på kørselstidspunktet bruges syntaks 1, skal felterne **Etiket** og **Beskrivelse** returnere værdier, der er baseret på sprogindstillingerne i det elektroniske rapporteringsformat (ER), der kører:

- Hvis etiketterne og beskrivelserne for det ønskede sprog er tilgængelige, returnerer felterne **Etiket** og **Beskrivelse** værdier, der er baseret på det pågældende sprog, og feltet **IsTranslated** returnerer **Sandt**.
- Hvis etiketterne og beskrivelserne for det ønskede sprog ikke er tilgængelige, returnerer felterne **Etiket** og **Beskrivelse** værdier, der er baseret på standardsproget **EN-US**, og feltet **IsTranslated** returnerer **Falsk**.

Når der på kørselstidspunktet bruges syntaks 2, skal felterne **Etiket** og **Beskrivelse** returnere værdier, der er baseret på det sprog, som der er defineret som det andet argument i den kaldte funktion:

- Hvis etiketterne og beskrivelserne for det ønskede sprog er tilgængelige, returnerer felterne **Etiket** og **Beskrivelse** værdier, der er baseret på det pågældende sprog, og feltet **IsTranslated** returnerer **Sandt**.
- Hvis etiketterne og beskrivelserne for det ønskede sprog ikke er tilgængelige, returnerer felterne **Etiket** og **Beskrivelse** værdier, der er baseret på sproget **EN-US**, og feltet **IsTranslated** returnerer **Falsk**.

## <a name="example-1"></a>Eksempel 1

I følgende illustration introduceres en fasttekst i en ER-datamodel.

<a href="./media/ger-listoffields-function-model-enumeration.png"><img src="./media/ger-listoffields-function-model-enumeration-e1474545790761.png" alt="Enumeration in a model" class="alignnone wp-image-1203943 size-full" width="514" height="155" /></a>

Følgende illustration viser disse detaljer:

- Modelfastteksten indsættes i en rapport som en datakilde.
- Et ER-udtryk bruger modelfastteksten som et parameter til funktionen `LISTOFFIELDS`.
- En datakilde af typen *Postliste* indsættes i en rapport ved hjælp af det oprettede ER-udtryk.

<a href="./media/ger-listoffields-function-in-format-expression.png"><img src="./media/ger-listoffields-function-in-format-expression-e1474546110395.png" alt="Format" class="alignnone wp-image-1204033 size-full" width="549" height="318" /></a>

Følgende eksempel viser de ER-formatelementer, der er bundet til datakilden af typen *Postliste*, der blev oprettet ved hjælp af funktionen `LISTOFFIELDS`.

<a href="./media/ger-listoffields-function-format-design.png"><img src="./media/ger-listoffields-function-format-design.png" alt="Format design" class="alignnone size-full wp-image-1204043" width="466" height="221" /></a>

I følgende illustration vises resultatet, når det designede format køres.

<a href="./media/ger-listoffields-function-format-output.png"><img src="./media/ger-listoffields-function-format-output.png" alt="Format output" class="alignnone size-full wp-image-1204053" width="585" height="158" /></a>

> [!NOTE] 
> Baseret på sprogindstillingerne til de overordnede formatelementer for **FILE** og **FOLDER**, udfyldes oversat tekst til etiketter og beskrivelser i outputtet til ER-formatet.

## <a name="example-2"></a>Eksempel 2

Du bruger datakildetypen *Beregnet felt* til at konfigurere datakilderne **enumType\_de** og **enumType\_deCH** for datamodelfastteksten **enumType**:

- **enumType\_de** = `LISTOFFIELDS (enumType, "de")`
- **enumType\_deCH** = `LISTOFFIELDS (enumType, "de-CH")`

I dette tilfælde skal kan du bruge følgende udtryk til at få etiketten til tællerværdien på tysk (Schweiz), hvis den pågældende oversættelse er tilgængelig. Hvis oversættelsen til tysk (Schweiz) ikke er tilgængelig, er etiketten på tysk.

```vb
IF (NOT (enumType_deCH.IsTranslated), enumType_de.Label, enumType_deCH.Label)
```

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
