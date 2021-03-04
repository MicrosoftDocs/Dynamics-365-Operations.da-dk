---
title: ER-funktionen FILTER
description: Dette emne indeholder oplysninger om, hvordan funktionen FILTER til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 12/12/2019
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
ms.openlocfilehash: 55fa3d4ad4427e2a45f7c5fce679c50a91c40b6d
ms.sourcegitcommit: 659375c4cc7f5524cbf91cf6160f6a410960ac16
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 12/05/2020
ms.locfileid: "4679432"
---
# <a name="filter-er-function"></a>ER-funktionen FILTER

[!include [banner](../includes/banner.md)]

Funktionen `FILTER` returnerer den angivne liste som en *Postliste*-værdi, når forespørgslen er blevet ændret, så den filtrerer for den angivne betingelse.

## <a name="syntax"></a>Syntaks

```vb
FILTER (list, condition)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`condition`: *Boolesk*

Et gyldigt betinget udtryk, der bruges til at filtrere poster på den angivne liste.

## <a name="return-values"></a>Returnerede værdier

*Postliste*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion adskiller sig fra funktionen [WHERE](er-functions-list-where.md), fordi den angivne betingelse anvendes på enhver elektronisk rapporteringsdatakilde (ER-datakilde) af typen *Tabelposter* på databaseniveau. Listen og betingelse kan defineres ved hjælp af tabeller og relationer.

Hvis et eller begge argumenter, der er konfigureret for denne funktion (`list` og `condition`), ikke tillader, at denne anmodning oversættes til det direkte SQL-kald, bliver der udløst en undtagelse på designtidspunktet. Denne undtagelse informerer brugeren om, at enten `list` eller `condition` ikke kan bruges til at forespørge på databasen.

## <a name="example-1"></a>Eksempel 1

Hvis **Leverandør** er konfigureret som en ER-datakilde, der henviser til tabellen VendTable, vil udtrykket `FILTER (Vendors, Vendors.VendGroup = "40")` alene returnere en liste over de leverandører, der tilhører leverandørgruppe 40.

## <a name="example-2"></a>Eksempel 2

Hvis **Leverandør** er konfigureret som en ER-datakilde, der henviser til VendTable-tabellen, og hvis **parmVendorBankGroup** er konfigureret som en ER-datakilde, der returnerer en værdi af datatypen *Streng*, returnerer udtrykket `FILTER ( Vendor.'<Relations'.VendBankAccount, Vendor.'<Relations'.VendBankAccount.BankGroupID = parmVendorBankGroup)` alene en liste over de leverandørkonti, der tilhører en bestemt bankgruppe.

## <a name="example-3"></a>Eksempel 3

Du indtaster datakilden **DS** af typen *Beregnet felt* og deri er indeholdt udtrykket `SPLIT ("A,B,C", ",")`. Derefter indtaster du et andet udtryk `FILTER( DS, DS.Value = "B")`. Når du forsøger at gemme dette udtryk i ER-formeldesigneren, bliver følgende undtagelse udløst: "Valideringsfejl: der kan ikke forespørges på listeudtrykket for funktionen FILTER."

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]