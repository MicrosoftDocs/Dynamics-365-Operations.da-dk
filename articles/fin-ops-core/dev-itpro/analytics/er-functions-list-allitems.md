---
title: ER-funktionen ALLITEMS
description: Dette emne indeholder oplysninger om, hvordan funktionen ALLITEMS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/04/2019
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
ms.openlocfilehash: 3aa226be8bc27817b4369b9e5b24faee8ea52b88
ms.sourcegitcommit: 3c1eb3d89c6ab9bd70b806ca42ef9df74cf850bc
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 02/12/2020
ms.locfileid: "3042222"
---
# <a name="ALLITEMS">ER-funktionen ALLITEMS</a>

[!include [banner](../includes/banner.md)]

Funktionen `ALLITEMS` kører som en markering i hukommelsen og returnerer en ny flad *Postliste*-værdi som en liste over poster, der repræsenterer alle elementer, der svarer til den angivne sti.

## <a name="syntax"></a>Syntaks

```vb
ALLITEMS (path)
```

## <a name="arguments"></a>Argumenter

`path`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Stien skal defineres som en gyldig datakildesti for et datakildeelement af datatypen *Postliste*. Dataelementer som strengen til stien og datoen bør udløse en fejl i designfasen i udtryksgenerator til den elektroniske rapportering (ER).

Vi anbefaler ikke, at du bruger denne funktion til transaktionsdatakilder, der kan indeholde en stor mængde data. Overvej i stedet at bruge funktionen [ALLTEMSQUERY](er-functions-list-allitemsquery.md).

## <a name="example-1"></a>Eksempel 1

Hvis du indtaster `SPLIT("abcdef" , 2)` som datakilde **DS**, returnerer `COUNT( ALLITEMS (DS))` udtrykket **3**.

## <a name="example-2"></a>Eksempel 2

Hvis du indtaster **Vend** som datakilde for datatypen *Postliste*, der refererer til programtabellen VendTable, returnerer udtrykket `ALLITEMS (Vend.'<Relations'.ContactPerson)` en flad liste over poster, der har tabelstrukturen **Kontaktperson**, og som indeholder alle kontaktpersoner, der kan tilgås ved hjælp af relationen **ContactPerson.ContactForParty == VendTable.Party**, og som er tilgængelig for alle leverandører fra den refererede leverandørtabel.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)
