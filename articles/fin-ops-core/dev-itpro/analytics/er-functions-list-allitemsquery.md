---
title: ER-funktionen ALLITEMSQUERY
description: Denne artikel indeholder oplysninger om, hvordan funktionen ALLITEMSQUERY til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 12/12/2019
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
ms.openlocfilehash: f5f8c69e7f67377c2e3d9ccc5a0da1fefe488921
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8877148"
---
# <a name="allitemsquery-er-function"></a>ER-funktionen ALLITEMSQUERY

[!include [banner](../includes/banner.md)]

Funktionen `ALLITEMSQUERY` kører som en sammenkædet SQL-forespørgsel. Den returnerer en ny fladtrykt *Postliste*-værdi, som består af en liste over poster, som repræsenterer alle elementer, der svarer til den angivne sti.

## <a name="syntax"></a>Syntaks

```vb
ALLITEMSQUERY (path)
```

## <a name="arguments"></a>Argumenter

`path`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*. Den skal indeholde mindst én relation.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Den angivne sti skal defineres som en gyldig datakildesti for et datakildeelement af datatypen *Postliste*. Den skal endvidere indeholde mindst én relation. Dataelementer som stiens *Streng* og *Dato* bør udløse en fejl i designfasen i udtryksgenerator til den elektroniske rapportering (ER).

Når denne funktion anvendes på datakilder af datatypen *Postliste*, der refererer til et programobjekt, der kan kaldes direkte ved hjælp af SQL (f.eks. en tabel, en enhed eller en forespørgsel), køres den som en sammenkædet SQL-forespørgsel. Ellers kører den i hukommelsen som funktionen [ALLITEM](er-functions-list-allitems.md).

## <a name="example"></a>Eksempel

Du definerer følgende datakilder i din modeltilknytning:

- En **CustInv** datakilde af typen *Tabelposter*, som refererer til tabellen CustInvoiceTable
- En **FilteredInv**-datakilde af typen *Beregnet felt*, der indeholder udtrykket `FILTER (CustInv, CustInv.InvoiceAccount = "US-001")`
- En **JourLines** af typen *Beregnet felt*, der indeholder udtrykket `ALLITEMSQUERY ( FilteredInv.'<Relations'.CustInvoiceJour.'<Relations'.CustInvoiceTrans)`

Når du kører modeltilknytningen for at kalde datakilden **JourLines**, udføres følgende SQL-sætning:

```sql
SELECT ... FROM CUSTINVOICETABLE T1 CROSS JOIN CUSTINVOICEJOUR T2 CROSS JOIN
CUSTINVOICETRANS T3 WHERE...
```

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]