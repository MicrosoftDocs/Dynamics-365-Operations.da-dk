---
title: ENDSWITH ER-funktion
description: Dette emne indeholder oplysninger om, hvordan funktionen ENDSWITH elektronisk rapportering (ER) skal anvendes.
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
ms.openlocfilehash: d2fa1c0e61e964de9b7dff36fe6a8c2813802e1cc22341ce4ddd73a17751a9c7
ms.sourcegitcommit: 42fe9790ddf0bdad911544deaa82123a396712fb
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/05/2021
ms.locfileid: "6771978"
---
# <a name="endswith-er-function"></a>ENDSWITH ER-funktion

[!include [banner](../includes/banner.md)]

Funktionen `ENDSWITH` bestemmer, om det angivne input slutter med den angivne tekst. Den returnerer en *Boolesk værdi* for **TRUE**, hvis det angivne input slutter med den angivne tekst. Ellers returneres en *Boolesk* værdi på **FALSK**.

## <a name="syntax"></a>Syntaks

```vb
ENDSWITH (input, end text)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan slutte med det andet argument.

`start text`: *Streng*

Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan slutte med det første argument.

## <a name="return-values"></a>Returnerede værdier

*Boolesk*

Den resulterende *Booleske* værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion kan kun bruges til at angive et betingelsesudtryk for funktionen [FILTER](er-functions-list-filter.md), når den relevante tilknytning er konfigureret i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til at få adgang til [Microsoft Dataverse](/power-platform/admin/data-integrator). Ellers sker der en undtagelse på designtid. Den meddelelse, du modtager, anbefaler, at du bruger funktionen [WHERE](er-functions-list-where.md) i stedet for funktionen `FILTER`.

## <a name="example-1"></a>Eksempel 1

Udtrykket returnerer `ENDSWITH ("abc", "d")` **FALSE**, mens udtrykket `ENDSWITH ("abc", "C")` returnerer **TRUE**.

## <a name="example-2"></a>Eksempel 2

Udtrykket `ENDSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "USA")` returnerer **TRUE**, hvis værdien i feltet **Adresse** i datakilden **model** slutter med strengen **USA**. Ellers returneres **FALSE**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)
