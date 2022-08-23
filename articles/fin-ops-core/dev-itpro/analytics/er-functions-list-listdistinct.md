---
title: Funktionen LISTDISTINCT ER
description: Denne artikel indeholder oplysninger om, hvordan funktionen til elektronisk LISTDISTINCT-rapportering (ER) skal anvendes.
author: kfend
ms.date: 07/30/2020
ms.prod: ''
ms.technology: ''
audience: Application User, IT Pro
ms.reviewer: kfend
ms.search.region: Global
ms.author: filatovm
ms.search.validFrom: 2020-08-01
ms.dyn365.ops.version: AX 10.0.14
ms.custom: ''
ms.assetid: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
ms.openlocfilehash: cd773f3455af1be1e952cb3852a648436670ce0f
ms.sourcegitcommit: 87e727005399c82cbb6509f5ce9fb33d18928d30
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/12/2022
ms.locfileid: "9285269"
---
# <a name="listdistinct-er-function"></a>Funktionen LISTDISTINCT ER

[!include [banner](../includes/banner.md)]
[!include [banner](../includes/preview-banner.md)]

Funktionen `LISTDISTINCT` beregner det angivne udtryk som en vælger for hver post på den angivne liste. Den returnerer en ny værdi for *Postliste*, som indeholder en enkelt post for hver entydig vælgerværdi.

## <a name="syntax"></a>Syntaks

```
LISTDISTINCT (list, selector)
```

## <a name="arguments"></a>Argumenter

`list`: *Postliste*

Den gyldige sti til en datakilde af datatypen *Postliste*.

`selector`: *Primitiv datatype*

Et gyldigt udtryk, der bruges til at beregne en vælgerværdi for hver post på den angivne liste.

Følgende datatyper understøttes for denne parameter:

- Boolesk
- Dato
- DateTime
- Guid
- Heltal
- Int64
- Kommatal
- Streng

## <a name="return-values"></a>Returnerede værdier

*Liste over poster*

Den resulterende liste over poster.

## <a name="usage-notes"></a>Bemærkninger til brug

Strukturen på den liste, der oprettes, svarer til strukturen i den angivne liste.

Den samme vælgerværdi kan beregnes for flere poster på den angivne liste. I dette tilfælde svarer feltværdierne for den tilsvarende post på den oprettede liste til værdierne i den første post fra den angivne liste, som vælgerværdien beregnes for.

Udførelsen af denne funktion udføres for enhver datakilde for [Elektronisk rapportering (ER)](general-electronic-reporting.md) for den type af *Postliste*, der findes i hukommelsen.

Datakilden **GROUPBY** kan også bruges til at generere den liste over poster, som den vælger, der har bestemte værdier, beregnes for. Set ud fra ydeevne og hukommelse i forbruget er det imidlertid bedre at bruge funktionen `LISTDISTINCT` end datakilden **GROUPBY**, da udførelsen af funktionen udføres i hukommelsen.

## <a name="example"></a>Eksempel

I følgende eksempel vises det, hvordan du kan få vist en liste over entydige kundekontonumre, som mindst én salgsfaktura eller projektfaktura er blevet udstedt til i en bestemt periode.

1. Angiv datakilden **SalesInvoice** for den type af `Record list`, der refererer til programtabellen **CustInvoiceJour** og filtrerer salgsfakturaer for bestemte perioder.

    Feltet `InvoiceAccount` i denne datakilde returnerer kontonummeret for en faktureret kunde.

2. Angiv datakilden **ProjectInvoice** for den type af `Record list`, der refererer til programtabellen **ProjInvoiceJour** og filtrerer projektfakturaer for bestemte perioder.

    Feltet `InvoiceAccount` i denne datakilde returnerer kontonummeret for en faktureret kunde.

3. Konfigurer datakilden **AllInvoices** af typen `Calculated field`, der indeholder udtrykket `LISTJOIN(SalesInvoice, ProjectInvoice)`.

    Denne datakilde returnerer den joinforbundne liste over salgsfakturaer og projektfakturaer.

4. Konfigurer datakilden **InvoicedCustomer** af typen `Record list`, der indeholder udtrykket `LISTDISTINCT(AllInvoices, AllInvoices.InvoiceAccount)`.

    Denne datakilde returnerer en ny liste, der indeholder en enkelt post for hver entydig kunde, der er faktureret i den angivne periode. Feltet `InvoiceAccount` på denne liste indeholder et kundekontonummer.

## <a name="additional-resources"></a>Yderligere ressourcer

[Listefunktioner](er-functions-category-list.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
