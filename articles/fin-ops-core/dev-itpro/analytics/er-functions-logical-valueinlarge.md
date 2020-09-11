---
title: ER-funktionen VALUEINLARGE
description: Dette emne indeholder oplysninger om, hvordan funktionen VALUEINLARGE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 08/17/2020
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
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.openlocfilehash: 4630ec20e7cbca97c5e43093e6a888a5e09f41a3
ms.sourcegitcommit: 38ad6f791c3d5688a5dc201a234ba89f155f7f03
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/19/2020
ms.locfileid: "3705137"
---
# <a name="valueinlarge-er-function"></a>ER-funktionen VALUEINLARGE

[!include [banner](../includes/banner.md)]

Funktionen `VALUEINLARGE` afgør, om det angivne input af typen *Int64* eller *Heltal* svarer til en værdi for et angivet element på den angivne liste. Funktionen returnerer en *Boolesk* værdi som værende **SAND**, hvis det angivne input svarer til resultatet af kørslen med det angivne udtryk for mindst én post på den angivne liste. Ellers returneres en *Boolesk* værdi på **FALSK**. Hvis du vil forstå forskellen med `VALUEIN`-funktionen, skal du se afsnittet [Bemærkninger til brug](#usage_note) senere i dette emne.

## <a name="syntax"></a>Syntaks

```vb
VALUEINLARGE (input, list, list item expression)
```

## <a name="arguments"></a>Argumenter

`input`: *Felt*

Den gyldige sti til et datakildeelement af typen *Postliste*. Værdien af dette element bliver sammenlignet.

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`list item expression`: *Betingelse*

Et gyldigt betinget udtryk, der enten peger på eller indeholder et enkelt felt fra den angivne liste, som skal bruges til sammenligningen.

## <a name="return-values"></a>Returnerede værdier

*Boolesk*

Den resulterende *Booleske* værdi.

## <a name=""></a><a name="usage_note">Bemærkninger til brug</a>

Når det angivne input repræsenterer en *Int64*- eller *Heltal*-type for et datakildeelement, vil det kald, der kan oversættes til en direkte SQL-sætning, blive konverteret til en midlertidig SQL-tabel, og matchning udføres i databasen ved at udføre en enkelt `EXISTS JOIN`-forespørgsel. Ellers virker denne funktion som funktionen [`VALUEIN`](er-functions-logical-valuein.md).

Når det angivne input repræsenterer et datakildeelement, der er designet som et andet element end *Int64*- og *Heltal*-typen, opstår der en fejl, på designtidspunktet om, at `VALUEINLARGE`-funktionen ikke kan anvendes til det konfigurerede ER-udtryk.

Når `VALUEINLARGE`-funktionsudtrykket udføres, og der bruges mere end én midlertidig tabel i området for denne udførelse, opstår der en kørselsfejl.

## <a name="example"></a>Eksempel

Du definerer følgende datakilder i din modeltilknytning:

- Datakilden **In** for typen *Tabelpost*.
    - Denne datakilde refererer til **Intrastat**-tabellen.
    - Indstillingen **På tværs af firma** er angivet til **Nej**.
- Datakilden **InMemory** af typen *Beregnet felt*.
    - Denne datakilde indeholder udtrykket `WHERE (In, In.Port <> "")`.
- Datakilden **InFiltered** af typen *Beregnet felt*.
    - Denne datakilde indeholder udtrykket `FILTER (In, VALUEINLARGE(In.RecId, InMemory, InMemory.RecId)`.

Når datakilden **InFiltered** kaldes i konteksten af firmaet **DEMF**, oprettes der en ny midlertidig tabel i programdatabasen, den indsamlede liste over postidentifikationskoder i hukommelsen indsættes i denne tabel, og følgende SQL-sætning genereres for at returnere filtrerede poster i **Intrastat**-tabellen.

```xpp
SELECT … from Intrastat T1
WHERE ((T1.PARTITION=?) AND (T1.DATAAREAID IN (N'DEMF'))) AND
EXISTS (SELECT 'x' FROM tempdb."DBO".? T2 WHERE ((T2.PARTITION=?) AND (T1.RecId=T2.RecId)))
```

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)

[VALUEIN-funktioner](er-functions-logical-valuein.md)
