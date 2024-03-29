---
title: STARTSWITH ER-funktion
description: Denne artikel indeholder oplysninger om, hvordan funktionen STARTSWITH elektronisk rapportering (ER) skal anvendes.
author: kfend
ms.date: 02/11/2021
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2021-02-01
ms.dyn365.ops.version: AX 10.0.18
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: 010646d2ab96d9a326ffb01c369726790b6377a6
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9287212"
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

Denne funktion kan kun bruges til at angive et betingelsesudtryk for funktionen [FILTER](er-functions-list-filter.md), når den relevante tilknytning er konfigureret i [Regulatory Configuration Services](../../../finance/localizations/rcs-globalization-feature.md) til at få adgang til [Microsoft Dataverse](/power-platform/admin/data-integrator). Ellers sker der en undtagelse på designtid. Den meddelelse, du modtager, anbefaler, at du bruger funktionen [WHERE](er-functions-list-where.md) i stedet for funktionen `FILTER`.

## <a name="example-1"></a>Eksempel 1

Udtrykket returnerer `STARTSWITH ("abc", "d")` **FALSE**, mens udtrykket `STARTSWITH ("abc", "A")` returnerer **TRUE**.

## <a name="example-2"></a>Eksempel 2

Udtrykket `STARTSWITH (model.InvoiceBase.Customer.PostalAddress.Address, "123 Coffee Street")` returnerer **TRUE**, hvis værdien i feltet **Adresse** i datakilden **model** starter med strengen **123 Coffee Street**. Ellers returneres **FALSE**.

## <a name="additional-resources"></a>Yderligere ressourcer

[Logiske funktioner](er-functions-category-logical.md)
