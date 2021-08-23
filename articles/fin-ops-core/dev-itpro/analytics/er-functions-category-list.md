---
title: Liste over ER-funktioner i kategorien liste
description: Dette emne indeholder oplysninger om listefunktionerne, der understøttes i elektronisk rapportering (ER).
author: NickSelin
ms.date: 04/01/2020
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
ms.openlocfilehash: 4f0d9f83a1750ff51d76716147f5d16e96c0fb415608256a5dcc7524a1f2bd2f
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6734858"
---
# <a name="list-of-er-functions-in-the-list-category"></a>Liste over ER-funktioner i kategorien liste

[!include [banner](../includes/banner.md)]

Listefunktioner til elektronisk rapportering (ER) kan bruges til at udtrække oplysninger fra og udføre handlinger på datakilder for datatyperne *Postliste* og *Container (post)*. Dette emne indeholder en oversigt over disse funktioner.

## <a name="list-of-supported-functions"></a>Liste med understøttede funktioner

| Funktion | Beskrivelse |
|----------|-------------|
| [Allevarer](er-functions-list-allitems.md)                 | Denne funktion kører som en markering i hukommelsen. Den returnerer en ny fladtrykt *Postliste*-værdi, som består af en liste over poster, der repræsenterer alle elementer, der svarer til den angivne sti. |
| [AllItemsQuery](er-functions-list-allitemsquery.md)       | Denne funktion kører som en sammenkædet SQL-forespørgsel. Den returnerer en ny fladtrykt *Postliste*-værdi, som består af en liste over poster, der repræsenterer alle elementer, der svarer til den angivne sti. |
| [Antal](er-functions-list-count.md)                       | Denne funktion returnerer en *Heltals*-værdi, der repræsenterer antallet af poster på den angivne liste, hvis listen ikke er tom. Hvis listen er tom, returnerer denne funktion **0** (nul). |
| [EmptyList](er-functions-list-emptylist.md)               | Denne funktion returnerer en tom *Postliste*-værdi ved hjælp af den angivne liste som kilde til listestrukturen.|
| [Fasttekst](er-functions-list-enumerate.md)               | Denne funktion returnerer en ny *Postliste*-værdi, der består af optalte poster på den angivne liste. |
| [Filtrér](er-functions-list-filter.md)                     | Denne funktion returnerer den angivne liste som en *Postliste*-værdi, når forespørgslen er blevet ændret, så den filtrerer for den angivne betingelse. |
| [Første](er-functions-list-first.md)                       | Denne funktion returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne liste ikke er tom. Hvis listen er tom, udløser denne funktion en undtagelse. |
| [FirstOrNull](er-functions-list-firstornull.md)           | Denne funktion returnerer den første post på den angivne liste som en *Container (post)*-værdi, hvis denne post ikke er tom. Hvis posten er tom, returnerer denne funktion en nul *Container (post)*-værdi. |
| [Indeks](er-functions-list-index.md)                       | Denne funktion returnerer en *Container (post)*-værdi, der er valgt ved hjælp af det angivne numeriske indeks på den angivne liste. Hvis indekset er uden for området for posterne på den angivne liste, vil denne funktion resultere i en undtagelse. |
| [IsEmpty](er-functions-list-isempty.md)                   | Denne funktion returnerer en *Boolesk* værdi som værende **SAND**, hvis den angivne liste ikke indeholder nogen poster. Ellers returneres en *Boolesk* værdi på **FALSK**. |
| [Liste](er-functions-list-list.md)                         | Denne funktion returnerer en ny *Postliste*-værdi, der består af en ny liste, som er oprettet på grundlag af de angivne argumenter.|
| [ListDistinct](er-functions-list-listdistinct.md)         | Denne funktion beregner det angivne udtryk som en vælger for hver post på den angivne liste. Den returnerer en ny værdi for *Postliste*, som indeholder en enkelt post for hver entydig vælgerværdi.|
| [ListJoin](er-functions-list-listjoin.md)                 | Denne funktion returnerer en ny *Postliste*-værdi, der repræsenterer en ny forenet liste, som er oprettet på grundlag af de angivne argumenter.|
| [ListOfFields](er-functions-list-listoffields.md)         | Denne funktion returnerer en *Postliste*-værdi, der er oprettet på baggrund af strukturen af det angivne argument i typen *Optælling* eller *Container (post)*. |
| [ListOfFirstItem](er-functions-list-listoffirstitem.md)   | Denne funktion returnerer en ny *Postliste*-værdi, der udelukkende består af de første poster på den angivne liste.|
| [OrderBy](er-functions-list-orderby.md)                   | Denne funktion returnerer den angivne liste som en *Postliste*-værdi, efter at den er sorteret i henhold til de angivne argumenter. Disse argumenter kan defineres som udtryk. |
| [Tilbagefør](er-functions-list-reverse.md)                   | Denne funktion returnerer den angivne liste som en *Postliste*-værdi i omvendt sorteringsrækkefølge. |
| [Opdel](er-functions-list-split.md)                       | Denne funktion opdeler den angivne inputstreng i understrenge og returnerer resultatet som en ny *Postliste*-værdi. |
| [SplitList](er-functions-list-splitlist.md)               | Denne funktion opdeler den angivne liste i underlister (eller batches), som hver især indeholder det angivne antal poster. Derefter returneres resultatet som en ny *Postliste*-værdi, der består af batches. |
| [SplitListByLimit](er-functions-list-splitlistbylimit.md) | Denne funktion opdeler den angivne liste i en ny liste over underlister (batches). Antallet af poster i hvert batch beregnes dynamisk. Funktionen returnerer dernæst resultatet som en ny *Postliste*-værdi, der består af batches. |
| [StringJoin](er-functions-list-stringjoin.md)             | Denne funktion returnerer en *Streng*-værdi, der består af sammenføjede værdier for det angivne felt fra den angivne liste. Værdierne kan være adskilt af et angivet separatortegn. |
| [Placering](er-functions-list-where.md)                       | Denne funktion returnerer den angivne liste som en *Postliste*-værdi, efter at den er blevet filtreret i henhold til den angivne betingelse. |

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Formelsprog i elektronisk rapportering](er-formula-language.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]