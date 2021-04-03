---
title: STARTSWITH ER-funktion
description: Dette emne indeholder oplysninger om, hvordan funktionen STARTSWITH elektronisk rapportering (ER) skal anvendes.
author: NickSelin
manager: kfend
ms.date: 02/11/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-platform
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
ms.openlocfilehash: 22e99d9e131410820abd12536b8d4f3e868c6863
ms.sourcegitcommit: 08ac570bece3e4ee4a0f632f51623e328536dfcf
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/08/2021
ms.locfileid: "5557507"
---
# <a name="startswith-er-function"></a>STARTSWITH ER-funktion

[!include [banner](../includes/banner.md)]

Funktionen `STARTSWITH` bestemmer, om det angivne input starter med den angivne tekst. Den returnerer en *Boolesk værdi* for **TRUE**, hvis det angivne input starter med den angivne tekst. Ellers returneres en *Boolesk* værdi på **FALSK**.

## <a name="syntax"></a>Syntaks

```vb
STARTSWITH (input, start text)
```

## <a name="arguments"></a>Argumenter

`input`: *Streng*

Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan starte med det andet argument.

`start text`: *Streng*

Den gyldige sti til en vare med en datakilde af *strengtypen* eller en strengkonstant, hvis værdi kan starte med det første argument.

## <a name="return-values"></a>Returnerede værdier

*Boolesk*

Den resulterende *Booleske* værdi.

## <a name="usage-notes"></a>Bemærkninger til brug

Denne funktion kan kun bruges til at angive et betingelsesudtryk for funktionen [FILTER](er-functions-list-filter.md), når den relevante tilknytning er konfigureret i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til at få adgang til [Microsoft Dataverse](../data-entities/data-integration-cds.md). Ellers sker der en undtagelse på designtid. Den meddelelse, du modtager, anbefaler, at du bruger funktionen [WHERE](er-functions-list-where.md) i stedet for funktionen `FILTER`.

## <a name="example-1"></a>Eksempel 1

Udtrykket returnerer `STARTSWITH ("abc", "d")` **FALSE**, mens udtrykket `STARTSWITH ("abc", "A")` returnerer **TRUE**.

## <a name="example-2"></a>Eksempel 2

Udtrykket `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returnerer **TRUE**, hvis værdien i feltet **Adresse** i datakilden **model** starter med strengen **123 Coffee Street**. Ellers returneres **FALSE**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)
