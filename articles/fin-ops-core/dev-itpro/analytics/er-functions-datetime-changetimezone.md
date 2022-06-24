---
title: ER-funktionen CHANGETIMEZONE
description: Denne artikel indeholder oplysninger om, hvordan funktionen CHANGETIMEZONE til elektronisk rapportering (ER) skal anvendes.
author: NickSelin
ms.date: 09/09/2021
ms.prod: ''
ms.technology: ''
ms.search.form: ERDataModelDesigner, ERExpressionDesignerFormula, ERMappedFormatDesigner, ERModelMappingDesigner
audience: Application User, IT Pro
ms.reviewer: kfend
ms.custom: 58771
ms.assetid: ''
ms.search.region: Global
ms.author: nselin
ms.search.validFrom: 2021-09-01
ms.dyn365.ops.version: AX 10.0.23
ms.openlocfilehash: be94f57cfcb6115ea386a279c379662f7d401d11
ms.sourcegitcommit: 52b7225350daa29b1263d8e29c54ac9e20bcca70
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 06/03/2022
ms.locfileid: "8903579"
---
# <a name="changetimezone-er-function"></a>ER-funktionen CHANGETIMEZONE

[!include [banner](../includes/banner.md)]

Funktionen `CHANGETIMEZONE` returnerer en værdi i form af *[Dato/klokkeslæt](er-formula-supported-data-types-primitive.md#datetime)* i UTC-tid (Greenwich Mean Time \[GMT\]), som konverteres fra en given dato-/klokkeslætsværdi i én tidszone til en dato-/klokkeslætsværdi i en anden tidszone.

## <a name="syntax"></a>Syntaks

```vb
CHANGETIMEZONE (datetime, base time zone, target time zone)
```

## <a name="arguments"></a>Argumenter

`datetime`: *DatoKlokkeslæt*

En dato-/klokkeslætsværdi i tidszonen UTC-tid, der repræsenterer den dato-/klokkeslætsværdi, der skal konverteres.

`base time zone`: *[Streng](er-formula-supported-data-types-primitive.md#string)*

Navnet på den tidszone, som en bestemt dato-/klokkeslætsværdi skifter til før konvertering.

`target time zone`: *Streng*

Navnet på den tidszone, som en konverteret dato-/klokkeslætsværdi skifter til under konvertering.

## <a name="return-values"></a>Returnerede værdier

*Dato/klokkeslæt*

Den nye dato-/klokkeslætsværdi i tidszonen UTC-tid.

## <a name="usage-notes"></a>Bemærkninger til brug

Hvis du vil angive tidszoner for kilde og mål, kan du bruge tidszonenavne, der [leveres](https://data.iana.org/time-zones/releases/) af [IANA (Internet Assigned Numbers Authority)](https://www.iana.org/), eller som [understøttes](/windows-hardware/manufacture/desktop/default-time-zones) af Microsoft Windows.

Under kørsel opstår undtagelsen "Tidszonen '\<time zone name\>' findes ikke", hvis det angivne navn ikke findes på IANA-listen eller i Windows-registreringsdatabasen.

I forbindelse med tidszoner, hvor der er sommertid, tager konverteringen højde for sommertidens tidsforskel i UTC-tid. De seneste tilgængelige oplysninger om denne tidsforskel bruges under konvertering.

## <a name="example-1"></a>Eksempel 1

I dette eksempel bruges tidszonenavnene til Windows.

Du konfigurerer datakilden **DSX** af typen **Beregnet felt**. Den indeholder følgende udtryk.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "E. Europe Standard Time", "Hawaiian Standard Time"), "O")
)
```

Hvis du konfigurerer udtrykket for **DSY**-datakilden for den **beregnede felttype** som `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer **DSX**-datakilden teksten **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Denne tekst viser, at tidsforskellen mellem de to angivne tidszoner den 1. juni er mere end 24 timer. Den omregnede dato/tidsværdi er derfor en dag tidligere end den angivne dato/tidsværdi, da basistidszonen er foran måltidszonen.

Hvis du konfigurerer udtrykket for **DSY**-datakilden for den **beregnede felttype** som `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer **DSX**-datakilden teksten **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Denne tekst viser, at tidsforskellen mellem de to angivne tidszoner den 1. december er mindre end 24 timer. Den omregnede værdi for dato/tid svarer derfor til den givne dato-/tidsværdi.

> [!NOTE]
> Det samme udtryk returnerer en anden afvigelse mellem de angivne og omregnede dato-/tidsværdierne for det samme par tidszoner, da en anden forskel i sommertid for UTC-tid overholdes for de angivne tidszoner på en bestemt dato/klokkeslæt.

## <a name="example-2"></a>Eksempel 2

I dette eksempel bruges IANA-tidszonenavnene.

Du konfigurerer datakilden **DSX** af typen **Beregnet felt**. Den indeholder følgende udtryk.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "Europe/Athens", "US/Hawaii"), "O")
)
```

Hvis du konfigurerer udtrykket for **DSY**-datakilden for den **beregnede felttype** som `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer **DSX**-datakilden teksten **2021-06-01T12:55:00.0000000+00:00 -> 2021-05-31T23:55:00.0000000+00:00**. Denne tekst viser, at tidsforskellen mellem de to angivne tidszoner den 1. juni er mere end 24 timer. Den omregnede dato/tidsværdi er derfor en dag tidligere end den angivne dato/tidsværdi, da basistidszonen er foran måltidszonen.

Hvis du konfigurerer udtrykket for **DSY**-datakilden for den **beregnede felttype** som `DATETIMEVALUE ("01-Dec-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer **DSX**-datakilden teksten **2021-12-01T12:55:00.0000000+00:00 -> 2021-12-01T00:55:00.0000000+00:00**. Denne tekst viser, at tidsforskellen mellem de to angivne tidszoner den 1. december er mindre end 24 timer. Den omregnede værdi for dato/tid svarer derfor til den givne dato-/tidsværdi.

## <a name="example-3"></a>Eksempel 3

Du konfigurerer datakilden **DSX** af typen **Beregnet felt**. Den indeholder følgende udtryk.

```vb
CONCATENATE(
    DATETIMEFORMAT( DSY, "O"), 
    " -> ", 
    DATETIMEFORMAT( CHANGETIMEZONE(DSY, "US/Hawaii", "Europe/Athens"), "O")
)
```

Hvis du konfigurerer udtrykket for **DSY**-datakilden for den **beregnede felttype** som `DATETIMEVALUE ("01-Jun-2021 12:55:00", "dd-MMM-yyyy HH:mm:ss", "EN")`, returnerer **DSX**-datakilden teksten **2021-06-01T12:55:00.0000000+00:00 -> 2021-06-02T01:55:00.0000000+00:00'**. Denne tekst viser, at tidsforskellen mellem de to angivne tidszoner den 1. juni er mere end 24 timer. Den omregnede dato/tidsværdi er derfor en dag senere end den angivne dato-/tidsværdi, da måltidszonen er foran basistidszonen.

## <a name="example-4"></a>Eksempel 4

Du kan få et dato-/tidsstempel fra en ekstern kilde som tekst, der ikke indeholder tidszoneoplysninger. Du kan dog kende den tidszone, som kilden opererer i. Du kan f.eks. modtage dato-/tidsstemplet **01/12/2021 12:55:00** fra en tjeneste, der drives fra Spanien. Gennemfør følgende konvertering for at gemme denne værdi af dato/klokkeslæt korrekt i databasen:

- Konfigurer **DSY**-datakilden for **Beregnet felt**-typen for at konvertere et dato-/tidsstempel fra tekst til dato-/klokkeslætsværdien i UTC-tid.

    `DATETIMEVALUE ("01/12/2021 12:55:00", "dd/MM/yyyy HH:mm:ss", "ES")`

- Konfigurer **DSX**-datakilden for **Beregnet felt**-typen for at ændre den omregnede dato-/klokkeslætsværdi til UTC-tid som dato-/klokkeslætsværdi for tidszonen i den eksterne kilde.

    `CHANGETIMEZONE(DSY, "Romance Standard Time", "GMT Standard Time")`

> [!NOTE]
> Når du bruger funktionen `CHANGETIMEZONE` til dato-/tidskonvertering, skal du være opmærksom på, at alle dato-/klokkeslætsværdierne er gemt i databasen som værdien i tidszonen for UTC-tid. Før denne værdi kan præsenteres på programsiderne, bliver den konverteret. Transformationen tager højde for den tidszone, der er [angivet](../../fin-ops/organization-administration/tasks/set-users-preferred-time-zone.md) som foretrukken zone for den programbruger, der aktuelt er logget på.

## <a name="additional-resources"></a>Yderligere ressourcer

[Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)

[!INCLUDE[footer-include](../../../includes/footer-banner.md)]
