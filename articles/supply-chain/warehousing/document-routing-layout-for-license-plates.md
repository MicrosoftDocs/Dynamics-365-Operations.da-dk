---
title: Labellayout i dokumentruteplanlægning
description: Denne artikel beskriver, hvordan du bruger formateringsmetoder til at udskrive værdier på etiketter.
author: perlynne
ms.date: 04/01/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: WHSLicensePlateLabel, WHSLicensePlateLabelBuildConfig, WHSLicensePlateLabel, WHSDocumentRoutingLayout
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: perlynne
ms.search.validFrom: 2012-04-01
ms.dyn365.ops.version: 10.0.10
ms.openlocfilehash: a4e0c16b71c257cae832870ca58679884047ea16
ms.sourcegitcommit: 9e6a9d644a34158390c6e209e80053ccbdb7d974
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 10/20/2022
ms.locfileid: "9708638"
---
# <a name="document-routing-label-layout"></a>Labellayout i dokumentruteplanlægning

[!include [banner](../includes/banner.md)]

I denne artikel beskrives, hvordan der oprettes layout for nummerplade-, container- og bølgelabels. Den indeholder også retningslinjer for brug af ZPL (Zebra Programming Language), der bruges til at oprette layout.

Labellayout i dokumentruteplanlægning definerer layoutet for labels og de data, der udskrives på dem. Du kan konfigurere udløsningspunkterne for udskrivning, når du konfigurerer menupunkter i mobilenheder og arbejdsskabeloner.

Oplysningerne i denne artikel gælder for alle labellayout til dokumentruteplanlægning, herunder layout for [nummerpladelabels](tasks/license-plate-label-printing.md), [containerlabels](print-container-labels.md) og [bølgelabels](configure-wave-label-printing.md).

Du kan udskrive meget komplekse etiketter, hvis udskrivningsenheden kan fortolke den tekst, der sendes til den. Et ZPL-layout, der indeholder en stregkode, kan f.eks. ligne følgende eksempel.

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

Teksten `$LicensePlateId$` i dette eksempel vil blive erstattet af en dataværdi som del af etiketudskrivningen. Flere meget tilgængelige værktøjer til oprettelse af etiketter kan hjælpe dig med at formatere teksten til etiketlayoutet. Mange af disse værktøjer understøtter `$FieldName$`-formatet. Microsoft Dynamics 365 Supply Chain Management bruger desuden en særlig formateringslogik som del af felttilknytningen for dokumentrutelayoutet.

Hvis du vil have vist de værdier, der vil blive udskrevet, skal du gå til **Lokationsstyring \> Forespørgsler og rapporter \> Id-nummeretiketter**.

## <a name="turn-on-this-feature-for-your-system"></a>Aktivere denne funktion i dit system

Hvis systemet ikke allerede indeholder de funktioner, der er beskrevet i denne artikel, skal du gå til [Funktionsstyring](../../fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview.md) og aktivere funktionen *Udvidede layout for id-etiket*. (Fra og med Supply Chain Management version 10.0.21 er denne funktion som standard aktiveret. Fra og med Supply Chain Management version 10.0.25 er denne funktion obligatorisk og kan ikke deaktiveres.)

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

Du kan få vist en komplet liste over de tilgængelige numeriske formatstrenge i [Brugerdefinerede numeriske formatstrenge ](/dotnet/standard/base-types/custom-numeric-format-strings).

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

Du kan få vist en komplet liste over de tilgængelige dato/klokkeslætsformater i [Brugerdefinerede dato/klokkeslætsformatstrenge ](/dotnet/standard/base-types/custom-date-and-time-format-strings).

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

Du kan kombinere dette format med andre typer, der blev beskrevet tidligere i denne artikel. Du har f.eks. en visningsmetode med navnet `DisplayListOfItemsNumbers()`, og du vil udskrive det første varenummer af denne metode. I dette tilfælde kan du bruge følgende kode.

```dos
$DisplayListOfItemsNumbers()[1]$
```

## <a name="more-information-about-how-to-print-labels"></a>Flere oplysninger om, hvordan du udskriver etiketter

Du kan få flere oplysninger om, hvordan du kan opsætte og udskrive labels, i følgende artikler:

- [Udskrivning af nummerpladelabel](tasks/license-plate-label-printing.md)
- [Udskrive containerlabels](print-container-labels.md)
- [Bølgeetiketudskrivning](configure-wave-label-printing.md)

[!INCLUDE[footer-include](../../includes/footer-banner.md)]
