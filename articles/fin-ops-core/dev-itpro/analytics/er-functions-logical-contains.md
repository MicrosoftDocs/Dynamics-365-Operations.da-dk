---
title: CONTAINS ER-funktion
description: Dette emne indeholder oplysninger om, hvordan funktionen CONTAINS til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 02/11/2021
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
ms.openlocfilehash: ae6c96b5754946ee971a8f47d4c618751d25f7e86fb9fb115861e97c5e6f536e
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6765140"
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
