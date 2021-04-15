---
title: Formelsprog i elektronisk rapportering
description: Dette emne indeholder generelle oplysninger om brug af formelsproget i elektronisk rapportering (ER).
author: NickSelin
ms.date: 05/04/2020
ms.topic: article
ms.prod: ''
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
ms.openlocfilehash: d2015405f3c7f89ba36f811ca125f3a73bc13c38
ms.sourcegitcommit: 074b6e212d19dd5d84881d1cdd096611a18c207f
ms.translationtype: HT
ms.contentlocale: da-DK
ms.lasthandoff: 03/31/2021
ms.locfileid: "5753258"
---
# <a name="electronic-reporting-formula-language"></a>Formelsprog i elektronisk rapportering

[!include [banner](../includes/banner.md)]

Elektronisk rapportering (ER) giver en effektiv datatransformationsoplevelse. Det sprog, der bruges til at udtrykke de påkrævede datamanipulationer i [ER-formeldesigneren](general-electronic-reporting-formula-designer.md), ligner formelsproget i Microsoft Excel.

## <a name="basic-syntax"></a>Grundlæggende syntaks

ER udtryk kan indeholde én eller flere af følgende elementer:

- [Konstanter](#Constants)
- [Operatorer](#Operators)
- [Referencer](#References)
- [Stier](#Paths)
- [Funktioner](#Functions)

## <a name=""></a><a name="Constants">Konstanter</a>

Når du designer udtryk, kan du bruge tekst og numeriske konstanter (værdier, der ikke beregnes). Den numeriske konstant `VALUE ("100") + 20` anvender den numeriske konstant **20** og strengkonstanten **"100"** samt returnerer den numeriske værdi **120**.

Elektronisk rapportering (ER) understøtter escape-sekvenser. Derfor kan du angive en udtryksstreng, der skal håndteres anderledes. For eksempel returnerer udtrykket `"Leo Tolstoy ""War and Peace"" Volume 1"` tekststrengen **Leo Tolstoy "Krig og Fred", bind 1**.

## <a name=""></a><a name="Operators">Operatorer</a>

Følgende tabel viser de aritmetiske operatorer, du kan bruge til at udføre grundlæggende matematiske funktioner som addition, subtraktion, multiplikation og division.

| Operatør | Betydning               | Eksempel     |
|----------|-----------------------|-------------|
| +        | Tilføjelse              | `1+2`       |
| -        | Subtraktion, negation | `5-2`, `-1` |
| \*       | Multiplikation        | `7\*8`      |
| /        | Afdeling              | `9/3`       |

Følgende tabel viser de sammenligningsoperatorer, der understøttes. Du kan bruge disse operatorer til at sammenligne to værdier.

| Operatør | Betydning                  | Eksempel      |
|----------|--------------------------|--------------|
| =        | Lig                    | `X=Y`        |
| &gt;     | Større end             | `X>Y`        |
| &lt;     | Mindre end                | `X<Y`        |
| &gt;=    | Større end eller lig med | `X>=Y`       |
| &lt;=    | Mindre end eller lig med    | `X<=Y`       |
| &lt;&gt; | Ikke lig med             | `X<>Y`       |

Du kan desuden bruge tegnet (&) som en operator til tekstsammenføjning. På denne måde kan du sammenføje eller sammenkæde en eller flere tekststrenge i et enkelt stykke tekst.

| Operatør | Betydning     | Eksempel                                               |
|----------|-------------|-------------------------------------------------------|
| &        | Sammenkæde | `"Nothing to print:" & " " & "no records found"`      |

### <a name="operator-precedence"></a>Den prioriterede operatorrækkefølge

Den rækkefølge, som delene af et sammensat udtryk evalueres i, er vigtig. For eksempel er resultatet af udtrykket `1 + 4 / 2` forskelligt, afhængigt af om der adderes eller divideres først. Du kan bruge parenteser til eksplicit at angive, hvordan et udtryk evalueres. Hvis du for eksempel vil angive, at addition skal udføres først, kan du ændre det foregående udtryk til `(1 + 4) / 2`. Hvis du ikke udtrykkelig angiver rækkefølgen af operationer i et udtryk, er rækkefølgen baseret på standardrangfølgen, der er tildelt de understøttede operatorer. Følgende tabel viser den prioritet, der er tildelt hver enkelt operator. Operatorer, der har højere prioritet (for eksempel 7), evalueres før operatorer, der har lavere prioritet (f.eks. 1).

| Prioritering | Operatorer      | Syntaks                                                                  |
|------------|----------------|-------------------------------------------------------------------------|
| 7          | Gruppering       | ( … )                                                                   |
| 6          | Medlemsadgang  | … . …                                                                   |
| 5          | Funktionskald  | … ( … )                                                                 |
| 4          | Multiplikation | … \* …<br>… / …                                                         |
| 3          | Tilføjelse       | … + …<br>… - …                                                          |
| 2          | Sammenligning     | … &lt; …<br>… &lt;= …<br>… =&gt; …<br>… &gt; …<br>… = …<br>… &lt;&gt; … |
| 1          | Separation     | … , …                                                                   |

Hvis et udtryk indeholder flere på hinanden følgende operatorer, der har samme prioritet, evalueres disse operationer fra venstre mod højre. For eksempel vil udtrykket `1 + 6 / 2 \* 3 > 5` returnere **sandt**. Vi anbefaler, at du bruger parenteser til at angive den ønskede rækkefølge af operationer i udtryk, så det bliver nemmere at læse og vedligeholde udtrykkene eksplicit.

## <a name=""></a><a name="References">Referencer</a>

Alle datakilder for den aktuelle ER-komponent, der er tilgængelige under designet af et udtryk, kan bruges som navngivne referencer. Den aktuelle ER-komponent kan enten være en modeltilknytning eller et format. For eksempel indeholder den aktuelle ER-modeltilknytning datakilden **ReportingDate**, der returnerer værdien af datatypen *DateTime*. Denne værdi i det genererende dokument skal formateres korrekt ved at referere til datakilden i udtrykket på følgende måde: `DATETIMEFORMAT (ReportingDate, "dd-MM-yyyy")`.

Alle tegn i navnet på en datakilde, der refereres til, som ikke repræsenterer et bogstav i alfabetet, skal indledes med et enkelt anførselstegn ('). Hvis navnet på en refererende datakilde indeholder mindst ét symbol, der ikke repræsenterer et bogstav i alfabetet, skal navnet stå i anførselstegn. F.eks. kan disse ikke-alfabetiske symboler være tegnsætningstegn eller andre skriftlige symboler. Her er nogle eksempler:

- Datakilden **Dags dato og tid** skal refereres til i et ER-udtryk på følgende måde `'Today''s date & time'`.
- Metoden **navn()** i datakilden **Customers** skal refereres til i ER-udtryk på følgende måde: `Customers.'name()'`.

Hvis metoderne i datakilder har parametre, bruges følgende syntaks til at kalde disse metoder:

- Hvis metoden **isLanguageRTL** i datakilden **System** har et **EN-US**-parameter af datatypen *Streng* skal denne metode refereres til i et ER-udtryk som `System.isLanguageRTL("EN-US")`.
- Anførselstegn er ikke påkrævede, når et metodenavn kun indeholder alfanumeriske symboler. Men de er obligatoriske til en metode for en tabel, hvis navnet indeholder kantede parenteser.

Når datakilden **System** føjes til en ER-tilknytning, der henviser til programklassen **Global**, returnerer udtrykket `System.isLanguageRTL("EN-US ")` den *Booleske* værdi **FALSK**. Det ændrede udtryk `System.isLanguageRTL("AR")` returnerer den *Booleske* værdi **SANDT**.

Du kan begrænse den måde, værdier sendes til parametrene på for denne type metode:

- Kun konstanter kan overføres til metoder af denne type. Værdierne af konstanter, der er defineret i designfasen.
- Kun primitive datatyper (basis) understøttes til parametrene for denne type. De primitive datatyper omfatter *Heltal*, *Reelt tal*, *Boolesk* og *Streng*.

## <a name=""></a><a name="Paths">Stier</a>

Når et udtryk refererer til en struktureret datakilde, kan du bruge definitionen af stien til at vælge et bestemt primitivt element i datakilden. Tegnet en prik (.) bruges til at adskille de enkelte elementer i en struktureret datakilde. For eksempel indeholder den aktuelle ER-modeltilknytning datakilden **InvoiceTransactions**, og denne datakilde returnerer en liste med poster. Poststrukturen **InvoiceTransactions** indeholder felterne **AmountDebit** og **AmountCredit**, og begge disse felter returnerer numeriske værdier. Du kan derfor designe følgende udtryk til beregning af det fakturerede beløb: `InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit`. Konstruktionen `InvoiceTransactions.AmountDebit` i dette udtryk er den sti, der bruges til at få adgang til feltet **AmountDebit** i datakilden **InvoiceTransactions** for typen *Postliste*.

### <a name="relative-path"></a>Relativ sti

Hvis stien til en struktureret datakilde starter med et "at"-tegn (@), er det en relativ sti. Tegnet "at" vises i stedet for den resterende del af den absolutte sti i den hierarkiske træstruktur, der bruges. Følgende illustration viser et eksempel. Her angiver den absolutte sti, `Ledger.'accountingCurrency()'`, at regnskabsvalutaværdien fra datakilden **Finans** angives i feltet **Regnskabsvaluta** i datamodellen.

![Eksempel på en absolut sti på siden ER-modeltilknytningsdesigner](./media/ER-FormulaLanguage-AbsolutePath.png)

Eksemplet i følgende illustration viser, hvordan en relativ kurve bruges. Den relative sti, `@.AccountNum`, angiver, at feltet **AccountNum** i datakilden **Intrastat** (som vises ét niveau over feltet **AccountNum** i datamodellens hierarkiske træ) bruges til at angive kundens eller leverandørens kontonummeret i datamodellens felt **AccountNum**.

![Eksempel på en relativ sti på siden ER-modeltilknytningsdesigner](./media/ER-FormulaLanguage-RelativePath1.png)

Den resterende del af den absolutte sti vises også i [ET-formeleditoren](general-electronic-reporting-formula-designer.md).

![Resterende del af den absolutte sti på siden ER-formeldesigner](./media/ER-FormulaLanguage-RelativePath2.png)

Du kan finde flere oplysninger under [Bruge en relativ sti i databindinger for ER-modeller og -formater](relative-path-data-bindings-er-models-format.md).

## <a name=""></a><a name="Functions">Funktioner</a>

Indbyggede ER-funktioner kan bruges i ER-udtryk. Alle datakilder i udtrykskonteksten (såsom ER-modeltilknytning eller ER-format) samt konstanter kan bruges som parametre til opkaldsfunktioner i henhold til listen over argumenter for opkaldsfunktioner. Konstanter kan også bruges som parametre til kald af funktioner. For eksempel indeholder den aktuelle ER-modeltilknytning datakilden **InvoiceTransactions**, og denne datakilde returnerer en liste med poster. Poststrukturen **InvoiceTransactions** indeholder felterne **AmountDebit** og **AmountCredit**, og begge disse felter returnerer numeriske værdier. Et udtryk til at beregne det fakturerede beløb kan derfor være udformet således ved at bruge den indbyggede ER-afrundingsfunktion: `ROUND (InvoiceTransactions.AmountDebit - InvoiceTransactions.AmountCredit, 2)`.

Når du designer ER-modeltilknytninger og ER-rapporter, kan du bruge ER-funktioner fra følgende kategorier:

- [Dato- og klokkeslætsfunktioner](er-functions-category-datetime.md)
- [Listefunktioner](er-functions-category-list.md)
- [Logiske funktioner](er-functions-category-logical.md)
- [Matematiske funktioner](er-functions-category-mathematical.md)
- [Postfunktioner](er-functions-category-record.md)
- [Tekstfunktioner](er-functions-category-text.md)
- [Dataindsamlingsfunktioner](er-functions-category-data-collection.md)
- [Andre (forretningsdomænespecifikke) funktioner](er-functions-category-other.md)
- [Typekonverteringsfunktioner](er-functions-category-type-conversion.md)

## <a name="functions-list-extension"></a>Funktionslistens udvidelse

ER understøtter muligheden for at udvide listen over funktioner, der bruges i ER-udtryk. Der kræves en vis teknisk indsats for at gøre dette. Yderligere oplysninger finder du under [Udvid listen med Elektroniske rapporteringsfunktioner (ER)](general-electronic-reporting-formulas-list-extension.md).

## <a name="compound-expressions"></a>Sammensatte udtryk

Du kan oprette sammensatte udtryk, der bruger funktioner fra forskellige kategorier, forudsat at datatyperne matcher. Når du bruger funktioner sammen, skal du matche datatypen for outputtet fra én funktion til den inputdata type, der kræves af en anden funktion. For eksempel, for at undgå en mulig "listen-er-tom" fejl i en binding af et felt til et ER-formatelement, kan du kombinere funktioner fra kategorien [Liste](er-functions-category-list.md) med en funktion fra kategorien [Logisk](er-functions-category-logical.md), som følgende eksempel viser. Her bruger formlen funktionen [HVIS](er-functions-logical-if.md) til at teste, om listen **IntrastatTotals** er tom, før den returnerer værdien af den påkrævede aggregering fra listen. Hvis listen **IntrastatTotals** er tom, returnerer formlen **0** (nul).

```vb
IF(ISEMPTY(IntrastatTotals), 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="multiple-solutions"></a>Flere løsninger

Ofte kan du få det samme datatransformationsresultat på flere måder ved at bruge funktioner fra forskellige kategorier eller forskellige funktioner fra samme kategori. F.eks. kan det forrige udtryk også konfigureres ved hjælp af funktionen [TÆL](er-functions-list-count.md) fra kategorien [Liste](er-functions-category-list.md).

```vb
IF(COUNT (IntrastatTotals)=0, 0.0, IntrastatTotals.aggregated.'$AmountMSTRounded') 
```

## <a name="additional-resources"></a>Yderligere ressourcer

[Oversigt over elektronisk rapportering](general-electronic-reporting.md)

[Formeldesigner i elektronisk rapportering](general-electronic-reporting-formula-designer.md)

[Udvide listen over elektroniske rapporteringsfunktioner](general-electronic-reporting-formulas-list-extension.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]