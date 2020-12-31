---
title: ER-funktionen VALUEIN
description: Dette emne indeholder oplysninger om, hvordan funktionen VALUEIN til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 08/18/2020
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
ms.search.validFrom: 2016-02-28
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: 0a133067ab74c711084cc1d7f456cbe49acdf79d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4686924"
---
# <a name="valuein-er-function"></a>ER-funktionen VALUEIN

[!include [banner](../includes/banner.md)]

Funktionen `VALUEIN` afgør, hvorvidt det angivne input svarer til en værdi for et angivet element på den angivne liste. Den returnerer en *Boolesk* værdi som værende **SANDT**, hvis det angivne input svarer til resultatet af kørslen med det angivne udtryk for mindst én post på den angivne liste. Ellers returneres en *Boolesk* værdi på **FALSK**.

## <a name="syntax"></a>Syntaks

```vb
VALUEIN (input, list, list item expression)
```

## <a name="arguments"></a>Argumenter

`input`: *Felt*

Den gyldige sti til et element i en datakilde af typen *Postliste*. Værdien af dette element bliver sammenlignet.

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`list item expression`: *Boolesk*

Et gyldigt betinget udtryk, der enten peger på eller indeholder et enkelt felt fra den angivne liste, som skal bruges til sammenligningen.

## <a name="return-values"></a>Returnerede værdier

*Boolesk*

Den resulterende *Booleske* værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Generelt set oversættes funktionen `VALUEIN` til et sæt **ELLER**-betingelser. Hvis listen over **ELLER**-betingelserne er stor, og den maksimale samlede længde af en SQL-sætning muligvis overskrides, skal du overveje at bruge [`VALUEINLARGE`](er-functions-logical-valueinlarge.md) som funktion.

```vb
(input = list.item1.value) OR (input = list.item2.value) OR …
```

I nogle tilfælde kan den oversættes til en SQL-database-sætning ved hjælp af operatøren `EXISTS JOIN`.

## <a name="example-1"></a>Eksempel 1

Du kan i din modeltilknytning definere datakilden **Liste** af typen *Beregnet felt*. Denne datakilde indeholder udtrykket `SPLIT ("a,b,c", ",")`.

Når en datakilde kaldes, og hvis den er konfigureret som udtrykket `VALUEIN ("B", List, List.Value)`, returneres **SANDT**. I dette tilfælde oversættes funktionen `VALUEIN` til følgende sæt betingelser: `(("B" = "a") or ("B" = "b") or ("B" = "c"))`, når `("B" = "b")` er **SAND**.

Når en datakilde kaldes, og hvis den er konfigureret som udtrykket `VALUEIN ("B", List, LEFT(List.Value, 0))`, returneres **FALSK**. I dette tilfælde oversættes funktionen `VALUEIN` til følgende betingelse: `("B" = "")`, som ikke er lig med **SAND**.

Den øvre grænse for antallet af tegn i teksten i en sådan betingelse er 32.768 tegn. Du skal derfor ikke oprette datakilder, der kan overskride denne grænse på kørselstidspunktet. Hvis grænsen overskrides, stopper programmet med at køre, og der udløses en undtagelse. For eksempel kan denne situation opstå, hvis datakilden er konfigureret som `WHERE (List1, VALUEIN (List1.ID, List2, List2.ID)`, og listerne **Liste1** samt **Liste2** indeholder en stor mængde poster.

I nogle tilfælde kan funktionen `VALUEIN` oversættes til en databasesætning ved hjælp af operatøren `EXISTS JOIN`. Dette problem opstår, når funktionen [`FILTER`](er-functions-list-filter.md) anvendes, og følgende betingelser er opfyldt:

- Indstillingen **Spørg efter forespørgsel** er deaktiveret for datakilden til funktionen `VALUEIN`, der refererer til listen over poster. Der bliver ikke anvendt yderligere betingelser på denne datakilde på kørselstidspunktet.
- Ingen indlejrede udtryk konfigureres for datakilden til den `VALUEIN`-funktion, der refererer til listen over poster.
- Et listeelement i `VALUEIN`-funktionen refererer til et felt i den angivne datakilde og ikke til et udtryk eller en metode i den angivne datakilde.

Overvej at bruge denne indstilling i stedet for funktionen [`WHERE`](er-functions-list-where.md), som er beskrevet tidligere i dette eksempel.

## <a name="example-2"></a>Eksempel 2

Du definerer følgende datakilder i din modeltilknytning:

- Datakilden **In** for typen *Tabelpost*. Denne datakilde refererer til Intrastat-tabellen.
- Datakilden **Port** for typen *Tabelpost*. Denne datakilde refererer til IntrastatPort-tabellen.

Når en datakilde bliver kaldt, der konfigureret som udtrykket `FILTER (In, VALUEIN(In.Port, Port, Port.PortId)`, genereres følgende SQL-sætning for at returnere filtrerede poster fra tabellen Intrastat.

```vb
select … from Intrastat
exists join TableId from IntrastatPort
where IntrastatPort.PortId = Intrastat.Port
```

For felterne **dataAreaId** genereres den endelige SQL-sætning ved hjælp af `IN`-operatoren.

## <a name="example-3"></a>Eksempel 3

Du definerer følgende datakilder i din modeltilknytning:

- Datakilden **Le** for typen *Beregnet felt*. Denne datakilde indeholder udtrykket `SPLIT ("DEMF,GBSI,USMF", ",")`.
- Datakilden **In** for typen *Tabelpost*. Denne datakilde refererer til Intrastat-tabellen, og indstillingen **På tværs af virksomheden** er aktiveret for den.

Når en datakilde, der er blevet konfigureret som udtrykket `FILTER (In, VALUEIN (In.dataAreaId, Le, Le.Value)`, kaldes, indeholder den endelige SQL-sætning følgende betingelse.

```vb
Intrastat.dataAreaId IN ('DEMF', 'GBSI', 'USMF')
```

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)

[VALUEINLARGE-funktioner](er-functions-logical-valueinlarge.md)
