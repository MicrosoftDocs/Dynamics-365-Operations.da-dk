---
title: CONTAINS ER-funktion
description: Dette emne indeholder oplysninger om, hvordan funktionen CONTAINS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.openlocfilehash: a31d89f036a6e821bea2b6733c0c646145d2a47c
ms.sourcegitcommit: 17cee26b03f7b5afe8a089a0a9b2380e8d377d70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 05/15/2021
ms.locfileid: "6048864"
---
# <a name="contains-er-function"></a>CONTAINS ER-funktion

[!include [banner](../includes/banner.md)]

Funktionen `CONTAINS` bestemmer, om det angivne input indeholder den angivne tekst. Den returnerer en *Boolesk værdi* for **TRUE**, hvis det angivne input indeholder den angivne tekst. Ellers returneres en *Boolesk* værdi på **FALSK**.

## <a name="syntax"></a>Syntaks

```vb
CONTAINS (input, search text)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan indeholder det andet argument.

`search text`: *Streng*

Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan indeholde det første argument.

## <a name="return-values"></a>Returnerede værdier

*Boolesk*

Den resulterende *Booleske* værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion kan kun bruges til at angive et betingelsesudtryk for funktionen [FILTER](er-functions-list-filter.md), når den relevante tilknytning er konfigureret i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til at få adgang til [Microsoft Dataverse](/power-platform/admin/data-integrator). Ellers sker der en undtagelse på designtid. Den meddelelse, du modtager, anbefaler, at du bruger funktionen [WHERE](er-functions-list-where.md) i stedet for funktionen `FILTER`.

## <a name="example-1"></a>Eksempel 1

Udtrykket returnerer `CONTAINS ("abc", "d")` **FALSE**, mens udtrykket `CONTAINS ("abc", "C")` returnerer **TRUE**.

## <a name="example-2"></a>Eksempel 2

Udtrykket `CONTAINS (model.InvoiceBase.Customer.PostalAddress.Address, "DEU")` returnerer **TRUE**, hvis værdien i feltet **Adresse** i datakilden **model** indeholder strengen **DEU**. Ellers returneres **FALSE**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)
