---
title: Dokumentrutelayout for id-nummeretiketter
description: I dette emne beskrives, hvordan du bruger formateringsmetoder til at udskrive værdier på etiketter.
author: perlynne
manager: tfehr
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: WHSLicensePlateLabel
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: Release 10.0.11
ms.openlocfilehash: ca7bf50800f3b376b809d89c5de969b2233c5e2b
ms.sourcegitcommit: d25d0feb3f8a5a760eba50ba5f46e1db02737d25
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 08/10/2020
ms.locfileid: "3677380"
---
# <a name="document-routing-layout-for-license-plate-labels"></a>Dokumentrutelayout for id-nummeretiketter

[!include [banner](../includes/banner.md)]

I dokumentrutelayoutet defineres layoutet for id-nummeretiketter og de data, der udskrives på dem. Du kan konfigurere udløsningspunkterne for udskrivning, når du konfigurerer menupunkter i mobilenheder og arbejdsskabeloner.

I et typisk scenarie vil de lagermedarbejdere, som modtager varen, udskrive id-nummeretiketter, umiddelbart efter at de har registreret indholdet af paller, der ankommer i modtagelsesområdet. De fysiske etiketter påsættes pallerne. De kan derefter bruges til validering som del af den læg-på-lager-proces, der følger efter, og fremtidige udgående pluk-handlinger.

Du kan udskrive meget komplekse etiketter, hvis udskrivningsenheden kan fortolke den tekst, der sendes til den. Et ZPL-layout (Zebra Programming Language), der indeholder en stregkode, kan f.eks. ligne følgende eksempel.

```dos
^XA~TA000~JSN^LT0^MNW^MTD^PON^PMN^LH0,0^JMA^PR2,2~SD15^JUS^LRN^CI0^XZ
^XA
^MMT
^PW320
^LL0160
^LS0
^FT20,58^A0N,28,28^FH\^FDLabel:^FS
^FT20,81^AAN,18,10^FH\^FD$LicensePlateId$^FS
^BY1,3,17^FT20,106^BCN,,Y,N,N,A
^FD$LicensePlateId$^FS
^PQ1,,,Y^XZ
```

Teksten `$LicensePlateId$` i dette eksempel vil blive erstattet af en dataværdi som del af etiketudskrivningen.

Hvis du vil have vist de værdier, der vil blive udskrevet, skal du gå til **Lokationsstyring \> Forespørgsler og rapporter \> Id-nummeretiketter**.

Flere meget tilgængelige værktøjer til oprettelse af etiketter kan hjælpe dig med at formatere teksten til etiketlayoutet. Mange af disse værktøjer understøtter `$FieldName$`-formatet. Microsoft Dynamics 365 Supply Chain Management bruger desuden en særlig formateringslogik som del af felttilknytningen for dokumentrutelayoutet.

## <a name="custom-number-formats"></a>Brugerdefinerede talformater

Du kan tilpasse formateringen af numeriske feltværdier, der udskrives, ved hjælp af koder, som har følgende format.

```dos
$FieldName:FormatString$
```

Her er en beskrivelse af dette format:

- `FieldName` er navnet på datafeltet (f.eks. **Antal**).
- `FormatString` definerer, hvordan dataene skal udskrives.

Følgende eksempler viser, hvordan du kan tilpasse feltet arbejdsantal (**Antal**):

- Hvis du altid vil have vist fire cifre (ved hjælp af nuller som pladsholdere), skal du bruge `$Qty:0000$`. Hvis antallet f.eks. er 10, vil etiketten vise "0010".
- Hvis du altid vil have vist to decimaler, skal du bruge `$Qty:0.00$`. Hvis antallet f.eks. er 10, vil etiketten vise "10,00".

Du kan få vist en komplet liste over de tilgængelige numeriske formatstrenge i [Brugerdefinerede numeriske formatstrenge ](https://docs.microsoft.com/dotnet/standard/base-types/custom-numeric-format-strings).

## <a name="custom-string-formats"></a>Brugerdefinerede strengformater

Du kan fjerne de første tegn i en streng ved hjælp af følgende felt og formateringskode.

```dos
$FieldName:#..$
```

Her angiver `#` det antal tegn, der skal springes over. Hvis du f.eks. vil udskrive et SSCC-id-nummer (Serial Shipping Container Code), der ikke indeholder de første to tegn, skal du bruge `$LicensePlateId:2..$`. I dette tilfælde udskrives id-nummeret 0011111111111222221 som "11111111111222221".

## <a name="custom-datetime-formats"></a>Brugerdefinerede dato/klokkeslætsformater

I følgende eksempel vises, hvordan du kan styre det format, der bruges til at udskrive datoer.

```dos
$PrintedDate:dd-MM-yyyy$
```

I dette eksempel vil datoen 30. april 2020 blive udskrevet som "30-04-2020".

Du kan få vist en komplet liste over de tilgængelige dato/klokkeslætsformater i [Brugerdefinerede dato/klokkeslætsformatstrenge ](https://docs.microsoft.com/dotnet/standard/base-types/custom-date-and-time-format-strings).

## <a name="print-individual-lines-from-multiline-data"></a>Udskrive individuelle linjer fra data på flere linjer

Hvis et datafelt indeholder flere linjer (dvs. linjer, der er adskilt af linjeskift), kan du udskrive en enkelt linje ved hjælp af følgende format.

```dos
$FieldName[#]$
```

Her er `#` det linjenummer, du vil udskrive. (Brug 1 til den første linje.)

Systemet har f.eks. et `AdditionalAddress`-felt, der indeholder følgende adresse med flere linjer:

Contoso Inc.  
Gadenavn 123  
En by, en stat

Du kan udskrive denne adresse, en linje ad gangen, ved hjælp af følgende koder.

| Kode | Tekst, der udskrives |
|---|---|
| `$AdditionalAddress[1]$` | Contoso Inc. |
| `$AdditionalAddress[2]$` | Gadenavn 123 |
| `$AdditionalAddress[3]$` | En by, en stat |

## <a name="print-and-format-from-a-display-method"></a>Udskrive og formatere fra en visningsmetode

Du kan udskrive fra en visningsmetode ved hjælp af følgende format.

```dos
$DisplayMethod()$
```

Du kan kombinere dette format med andre typer, der blev beskrevet tidligere i dette emne. Du har f.eks. en visningsmetode med navnet `DisplayListOfItemsNumbers()`, og du vil udskrive det første varenummer af denne metode. I dette tilfælde kan du bruge følgende kode.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Flere oplysninger om, hvordan du udskriver etiketter

Du kan få flere oplysninger om, hvordan du kan opsætte og udskrive etiketter, i [Aktivere udskrivning af id-etiket](tasks/license-plate-label-printing.md).
